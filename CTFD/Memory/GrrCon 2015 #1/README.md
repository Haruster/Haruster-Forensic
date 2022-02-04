- 오늘은 CTF-d(Forensic) 워게임의 Memory문제인 GrrCON 2015 #1를 한번 풀어보겠습니다.

![](https://images.velog.io/images/dsph9245/post/f5148073-2da1-4b6c-91df-4f5dceaac080/%ED%99%94%EB%A9%B4%20%EC%BA%A1%EC%B2%98%202021-12-23%20160357.png)

- 첨부 파일도 같이 받아주겠습니다. 

- 첨부 파일을 확인해보니 .vmss 확장자를 가지고 있네요.

![](https://images.velog.io/images/dsph9245/post/fce16f2c-b600-4d79-b02d-0a9be438db73/%ED%99%94%EB%A9%B4%20%EC%BA%A1%EC%B2%98%202021-12-23%20160411.png)

- .vmss는 Vmware에 사용하는 파일로 Suspended된 가상 머신의 상태를 저장하는 파일이네요

![](https://images.velog.io/images/dsph9245/post/a999d846-4c18-4184-8771-abc7b8b97ab5/%ED%99%94%EB%A9%B4%20%EC%BA%A1%EC%B2%98%202021-12-23%20160731.png)

- 먼저 Volatility를 이용해서 해당 .vmss 파일의 imageinfo를 알아보겠습니다.

![](https://images.velog.io/images/dsph9245/post/42081870-329f-4aaa-8a55-99570597e513/%ED%99%94%EB%A9%B4%20%EC%BA%A1%EC%B2%98%202021-12-23%20161157.png)

- 위의 imageinfo 명령으로 인해서 --profile에 넣어야 하는 값은 Win7SP0x86이라는 것을 알게 되었고, 메모리 관련 파일이므로 pslist 명령으로 프로세스를 확인해주겠습니다.

- 해당 명령을 실행해서 프로세스에 존재하는 .exe 파일 중 메일에 관련된 것은 OUTLOOK.EXE 밖에 없다는 것을 알 수 있습니다.

![](https://images.velog.io/images/dsph9245/post/077929df-191a-40a8-ab2c-5495a9e6b838/%ED%99%94%EB%A9%B4%20%EC%BA%A1%EC%B2%98%202021-12-23%20161504.png)

- OUTLOOK.EXE의 PID 값인 3196을 이용해서 메모리 덤프를 추출해줍니다.

![](https://images.velog.io/images/dsph9245/post/bca2705b-2710-4352-b3e9-a6b4eb49fcfb/%ED%99%94%EB%A9%B4%20%EC%BA%A1%EC%B2%98%202021-12-23%20161834.png)

- 마지막으로 3196.dmp 파일을 분석하여 메일 정보를 찾아봅니다.
- 저의 경우에는 strings라는 명령어를 사용해서 찾았습니다.

![](https://images.velog.io/images/dsph9245/post/70a50aa6-ade9-4384-9843-7beee0a766d6/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-12-23%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%204.47.55.png)

- 따라서 gmail.com으로 검색이 되고 th3wh1t3r0s3@gmail.com이 우리가 원하는 플래그라는 것을 알 수 있습니다. 

-이러한 flag 값을 submit을 하면 정상적으로 solve가 되는 것을 확인할 수 있습니다.

![](https://images.velog.io/images/dsph9245/post/fe954d73-91ab-4fb2-97a4-e9500e8beb13/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-12-23%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%204.50.11.png)

![](https://images.velog.io/images/dsph9245/post/7c17b399-6f0d-4c22-b746-37dda49f006d/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-12-23%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%204.50.22.png)

- 오늘은 CTF-d(Forensic) 워게임의 Muitimedia 문제인 우리는 이 파일에 플래그를... 이라는 문제를 한번 풀어보겠습니다.

![](https://images.velog.io/images/dsph9245/post/57d9949a-87da-436d-a057-e22cc9d7e319/4.png)

- 파일을 다운로드 한 후 strings와 명령어를 사용해서 파일에 숨겨진 정보가 있는 것이 아닌지 보았는데 중요한 정보는 존재하지 않아서 file 명령어를 사용해서 파일의 정보를 보니 파일이 gzip 파일이라는 것을 알게 되었습니다.

![](https://images.velog.io/images/dsph9245/post/026d859a-ede8-48f4-b2cd-0b0591a02f15/5.png)

- 파일의 압축을 풀어주면 flag라는 파일이 있습니다. (저는 반디집을 사용하였습니다.)

![](https://images.velog.io/images/dsph9245/post/1cb8b70c-d2a9-4c9d-a76f-c3efae25257f/6.png)

- 이를 열어주면 플래그를 확인할 수 있습니다.

![](https://images.velog.io/images/dsph9245/post/5417053e-f633-4ba5-8007-166ee05acde0/7.png)

- 해당 플래그를 submit하면 정상적으로 Solve가 되는 것을 확인할 수 있습니다.

![](https://images.velog.io/images/dsph9245/post/6042d367-7cb3-4bc3-85b8-98678244c08a/8.png)

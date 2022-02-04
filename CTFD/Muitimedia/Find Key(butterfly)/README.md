- 오늘은 CTF-d(Forensic) 워게임의 Muitimedia 문제인 Find Key(bufferfly)를 풀어보도록 하겠습니다.

![](https://images.velog.io/images/dsph9245/post/056a6057-cfcb-4215-a63c-ee1168aaf465/5.png)

- 파일을 다운로드하고 이를 열어보면 나비 사진이 있는 것을 확인할 수 있습니다.

![](https://images.velog.io/images/dsph9245/post/f36bb620-181a-4e37-b6f9-5d8b5adadadd/6.png)

- Strings 명령어를 사용해서 숨겨진 텍스트가 있는지 확인해보면 딱히 중요한 정보는 없다는 것을 확인할 수 있습니다.

![](https://images.velog.io/images/dsph9245/post/fb4cc6a1-51da-487b-a734-936aa8b2ee99/7.png)

- 그럼 다음으로 스테가노 그래피 툴은 stegsolve를 사용해서 이를 돌려보았는데 돌리던 중 flag가 나와서 이를 submit했더니 solve가 되는 것을 확인할 수 있었습니다.

![](https://images.velog.io/images/dsph9245/post/b02c8d34-68c9-4653-90fe-ad495735d594/8.png)

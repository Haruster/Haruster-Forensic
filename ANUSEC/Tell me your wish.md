해당 문제에 대한 설명은 다음과 같습니다. 

![](https://images.velog.io/images/dsph9245/post/90b4ae25-e511-42e2-88a5-811d51dca73f/1.PNG)

문제 파일은 압축이 되어 있는데 압축을 풀어보면 vmware file 즉, 가상머신 관련 파일들이 나옵니다.(용량이 큰 이유가 있네요;;;;) 

![](https://images.velog.io/images/dsph9245/post/f0ceada6-5160-40fe-bd95-e2422eb92833/2.PNG)

일단 vmware를 사용하여 해당 가상머신을 실행해보겠습니다. 
실행한 뒤 바탕화면을 보면 크롬, 웨일과 같은 프로그램들이 있습니다. 뭔가 단서가 있을 수 있으니 해당 프로그램들을 사용하여 방문기록을 확인하겠습니다. 

![](https://images.velog.io/images/dsph9245/post/e1ec6177-5814-4369-9991-934a2b540667/3.PNG)

검색기록을 찾아보면 타임머신, 타임캡슐, HXD와 같은 검색 기록이 나옵니다. 무언가를 HXD로 분석하는 것으로 예상이 됩니다. 

![](https://images.velog.io/images/dsph9245/post/5240ed04-9dae-4234-9637-a03149d76d7d/6.PNG)

![](https://images.velog.io/images/dsph9245/post/806ac724-ea5d-4f2e-a522-36aa234f4195/4.PNG)

![](https://images.velog.io/images/dsph9245/post/89f8f6de-ad3a-44b0-afa9-9b2370322abb/5.PNG)

time machine이라고 하니 Mac Os의 타임머신이 생각나네요(필자는 Mac OS를 메인으로 사용하고 있습니다.) 무언가를 시스템 복구해야할 것 같네요. 일단 복원 지점이 존재하는지 제어판 -> 시스템 복구로 이동하겠습니다.

![](https://images.velog.io/images/dsph9245/post/d1744a04-b3d5-4c2b-a87e-a908220ba842/7.PNG)

![](https://images.velog.io/images/dsph9245/post/8698d4dc-0303-4b3a-ad43-6111268eee2e/8.PNG)

예상대로(?) 복원지점이 존재하네요. ㅎㅎ 복원해주겠습니다.

![](https://images.velog.io/images/dsph9245/post/63618f2d-06c2-4b00-b951-48ab3a2b3353/9.PNG)

![](https://images.velog.io/images/dsph9245/post/ac2f59cb-18fd-4c13-931a-6b019aeec952/10.PNG)

복원을 완료하면 바탕화면에 다음과 같은 파일이 있습니다. HXD로 분석해보죠 ㅎㅎ

![](https://images.velog.io/images/dsph9245/post/643ba059-fb68-428b-8636-6b14090cd0e2/11.PNG)

![](https://images.velog.io/images/dsph9245/post/4f1b622a-e39f-42d6-ad02-826b597cdd53/12.PNG)

그리고 파일시그니처가 올바른지 확인해보겠습니다.

![](https://images.velog.io/images/dsph9245/post/6af658aa-3d85-44a2-8723-ac5cdc903ae0/13.PNG)

시그니처 정보를 확인해보면 해당 파일은 .exe파일이라는 것을 알 수 있습니다. 

![](https://images.velog.io/images/dsph9245/post/ae451512-9ee4-4a7d-a82b-74b43bb0c1f4/14.PNG)

-> 따라서 확장자를 .exe로 바꾸겠습니다. 

* HXD에서 다른 이름으로 저장을 누르고 ink를 exe로 바꿔줍니다. 

![](https://images.velog.io/images/dsph9245/post/6b921ef5-0b6d-41e4-843c-8e0c3db280d7/15.PNG)

그럼 다음과 같은 실행 파일이 생성되고 실행해보면 오류가 나는 것을 확인할 수 있습니다. ㅠㅠ 

![](https://images.velog.io/images/dsph9245/post/543ae033-a4da-4851-b92f-1eda89711a4c/16.PNG)

계속 삽질을 해보다가 혹시나 하는 마음에 제가 사용하고 있는 로컬 시스템에서 이를 실행해보니 실행이 되었습니다. (실행 파일 환경이 달랐던 것 같네요..... (더 공부를 해야겠네요.. ㅠㅠ)

![](https://images.velog.io/images/dsph9245/post/eac4bdcc-d3e7-47ea-94b0-0cb2f228813a/17.PNG)

Get Flag 버튼을 누르고 잠시만 기다려보면 다음과 같이 플래그가 나오는 것을 확인하실 수 있습니다. ^^

![](https://images.velog.io/images/dsph9245/post/9729434e-6f46-48cc-bd08-1efb5da23fc8/18.PNG)

> 문제 출저 : http://sc.anu.ac.kr/

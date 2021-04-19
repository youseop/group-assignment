### Group Assignment

5달 동안 거의 매주 조 배정을 새롭게 짜야하는 매니저님을 위해 프로그램을 만들어 봤습니다.

조를 짜주는 프로그램은 많지만, 최대한 구성원 간의 중복 없이 조를 짜주는 프로그램은 많지 않아서 프로그램을 새로 짰습니다. (Colab에서 Python으로 작성했습니다.)

중복되지 않게 조를 구성하는 것이 생각보다 어려운 문제이더라고요...

랜덤으로 섞어 놓고, 배치하며 중복이 없이 배치된 경우에만 결과를 도출하도록 코드를 짰는데, 혹시 다른 아이디어가 있으시면 조언 부탁드립니다.

🙏🙏

### Manual

1\. Github Link로 접속해, 조배정.ipynb파일을 클릭합니다.

[Github Link](https://github.com/youseop/group-assignment)

![crepe](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FB49gK%2FbtqRavnHwNg%2FuoD3VRKqFewxCr2mdBGPhk%2Fimg.png)

2\. Open in Colab 버튼을 클릭해 Colab에서 파일을 실행시킵니다.

![crepe](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FBPlAA%2FbtqQZwhHRRI%2F99CiKRJ4bMWSZ4A3MCZy2k%2Fimg.png)


3\. 첫 번째 코드를 실행시켜(shift + enter) Colab에 본인의 구글 드라이브를 마운트 시킵니다.

![crepe](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FJdtWY%2FbtqQ8MiXXio%2FCvB6t3zF7kNSIfyNn4IV9k%2Fimg.png)


4\. 아래와 같은 링크가 등장하면, 링크를 눌러 구글 계정 로그인을 해야 합니다. 로그인 후에 나오는 코드를 빈칸에 붙여 넣어주세요.

![crepe](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Ftx6yG%2FbtqQ8M4jplg%2FxD971zOl15s0nYiyLf7Zkk%2Fimg.png)


5\. 이전에 배정했던 조를 불러오고, 저장하기 위해 구글 드라이브에 result\_lunch라는 이름의 폴더를 생성합니다. 좌측 상단의 폴더를 클릭하면 원하는 위치에 마우스 오른쪽 클릭을 한 후에 new folder항목을 클릭하면 폴더가 생성됩니다.

파일을 읽고 쓸 path를 수정해야 합니다. result\_lunch폴더를 오른쪽 클릭한 후에 copy path를 눌러 경로를 복사한 후에 

path = '(copy path 붙여 넣기)/week\_%d' %(i)로 경로를 수정합니다.

저의 경우에는 아래와 같은 경로입니다. (Deeplearning과 제가 작성한 조배정 프로그램은 아무 관련이 없습니다.😂)

path = '/content/drive/MyDrive/Deeplearning\_pract/조배정프로그램/result\_lunch/week\_%d' %(i)

![crepe](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2F87kRq%2FbtqQ0Qmzm5H%2FpeL6GS9HKfB8CxWnMry201%2Fimg.png)


6\. 아래의 저장 경로도 동일하게 변경합니다.

path = '(copy path 붙여넣기)/week\_%d' %(week\_num)

![crepe](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FblwK3X%2FbtqQ1L6pT7l%2FfL2tSFiK8s51DA0HePyDl0%2Fimg.png)


7\. 변수값들을 설정해 줍니다.

기존 결과 파일이 result\_lunch폴더에 없는 경우 week\_num을 1부터 실행시켜야 합니다.

![crepe](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fc4ggro%2FbtqRawGVn4V%2Fjwp6UevqHKz0J1ooo6D8EK%2Fimg.png)


8\. **몇 번의 중복을 허용할지 설정해 줍니다.** 0으로 설정한 후에 실행하면, 단 한 명의 중복도 허용하지 않게 됩니다.

단, 중복을 허용하지 않은 채로 무한히 조를 생성할 수는 없음으로, 일정 수 이상의 조를 생성한 후에는 조가 생성되지 않습니다. 이때, value를 +1로 높여줘야 프로그램이 동작합니다.  

![crepe](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fd43dzk%2FbtqRcGWO0EW%2Fytt8Yc8Ypu6r4CSOTAARg0%2Fimg.png)

9\. shit+enter를 눌러 코드를 실행하고, 배치가 완료되면, result\_lunch폴더에서 결과를 확인할 수 있습니다. 

****주의**📢** 동일한 week\_num으로 코드를 다시 실행하면, 이 파일이 다시 변경됩니다. 보관하고 싶은 경우 별도의 공간에 백업해놓기를 권장드립니다.

![crepe](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fbpz2xf%2FbtqQ8MJ2gy0%2FYZBPuiWA1EUquTJsJ6puK0%2Fimg.png)

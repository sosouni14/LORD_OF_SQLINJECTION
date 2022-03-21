# 4

![image-20220321194436268](https://raw.githubusercontent.com/sosouni14/image_server/main/image_rev/image-20220321194436268.png)



비밀번호를 맞춰야하는 문제이다.

아이디는 그대로 admin 이며 비밀번호만 알아내면 되는 문제인 것 같다.

먼저 비밀번호 길이가 몇인지 알아봐야 할 것 같다.



---

### ?pw=%27or%20length(pw)=%275

![image-20220321200623176](https://raw.githubusercontent.com/sosouni14/image_server/main/image_rev/image-20220321200623176.png)

비밀번호 길이를 알아내기 위해 length 함수를 사용하였다.

0부터 숫자를 넣어서 길이가 몇인지 확인해보았다.



---

### ?pw=%27or%20length(pw)=%278

![image-20220321201938111](https://raw.githubusercontent.com/sosouni14/image_server/main/image_rev/image-20220321201938111.png)

`?pw=%27or%20length(pw)=%278` 을 넣으니깐 `Hello admin` 이 나왔다.

비밀번호는 총 8글자라는 것을 알아냈다.

---

### ?pw=%27or%20substr(pw,1,1)=0%23

![image-20220321202333069](https://raw.githubusercontent.com/sosouni14/image_server/main/image_rev/image-20220321202333069.png)

`substr(pw,1,1)=0%23` 이렇게 첫번째 비밀번호가 무엇인지 찾아낸다.

`substr(pw,?,1)=?%23` 첫번째 문자 1개를 숫자 0부터 시작하여 해당되는 문자를 넣을 경우 Hello admin 이 나온다.

---

### ?pw=%27or%20substr(pw,4,1)=0%23

![image-20220321203841892](https://raw.githubusercontent.com/sosouni14/image_server/main/image_rev/image-20220321203841892.png)

`substr(pw,4,1)=0%23` 으로 뒤를 주석처리 할 경우 4번째에 0을 넣으면 `Hello admin` 이 출력된다.



---

### ?pw=09509852

![image-20220321204012586](https://raw.githubusercontent.com/sosouni14/image_server/main/image_rev/image-20220321204012586.png)

`substr(pw,?,1)=?%23` 으로 뒤를 `%23`을 넣어서 8글자 비밀번호를 알아냈지만 옳지 않다고 나온다.

다시해도 `09509852` 가 각 순서대로 하나씩 넣을 때 맞다고 나온다. 하지만 전체적으로 넣으면 다르다고 나온다.



---

### ?pw=00950985

![image-20220321204940965](https://raw.githubusercontent.com/sosouni14/image_server/main/image_rev/image-20220321204940965.png)

`?pw=09509852` 가 맞지 않아서 `substr(pw,0,1)=0%23` 으로 해야지 맞다고 생각하여 0의 자리부터 하였다.

그래도 옳지 않았으며 0의 자리와 9의 자리에 0을 넣으면 다 `Hello admin` 이 출력된다.

하지만 인코딩, 디코딩 0은 0이다.  그래서 뭔가 잘못되었다고 느꼈다.

그래서 입력했을 때 `query` 부분에 원본 부분하고 똑같이 나오게 만들어 볼려고 하였다.



---

### ?pw=%27or%20substr(pw,0,1)=%270

![image-20220321205647505](https://raw.githubusercontent.com/sosouni14/image_server/main/image_rev/image-20220321205647505.png)

`substr(pw,0,1)=%270` 으로 하였더니 `Hello admin` 이 출력 되지않는다.

이렇게 1번째부터 8번째까지 숫자와 알파벳을 넣으면서 알아내었다.

결과는 4번째 문자열만 달랐다.

`095a9852` 이 나왔다.



---

### ?pw=095a9852

![image-20220321210104275](https://raw.githubusercontent.com/sosouni14/image_server/main/image_rev/image-20220321210104275.png)

`?pw=095a9852` 을 넣으니 성공했다.

왜 4번째 부분에서 싱글쿼터를 넣거나 주석처리를 하였을 때 다른 숫자를 넣을 때 다르게 뜨는지 잘 모르겠다.
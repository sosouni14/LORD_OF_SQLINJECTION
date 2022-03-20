# 3

![image-20220320210905905](https://raw.githubusercontent.com/sosouni14/image_server/main/image_rev/image-20220320210905905.png)

아이디가 guest 로 로그인 되어있다. 그리고 ''(싱글쿼터), ""(더블쿼터) 를 금지하고 있다.

이것을 admin 으로 바꾸어주면 될 것 같다. 

---

### ?no=0

![image-20220320211141738](https://raw.githubusercontent.com/sosouni14/image_server/main/image_rev/image-20220320211141738.png)

no= 이라고 써져있어서 먼저 0의 값을 써보았다.

?no=0 이라고 할때 아무 반응이 없었다.

---

### ?no=1

![image-20220320211254791](https://raw.githubusercontent.com/sosouni14/image_server/main/image_rev/image-20220320211254791.png)

?no=1 로 바꾸었을 때 Hello guest 라는 문구가 나왔다.

---

### ?no=2

![image-20220320211457137](https://raw.githubusercontent.com/sosouni14/image_server/main/image_rev/image-20220320211457137.png)

?no=2 은 admin 일거라고 생각하면서 넣었지만 반응이 없다.

3,4 을 넣어도 성공되지 않았다.

---

### ?no=2%20or%20no=2

![image-20220320211729902](https://raw.githubusercontent.com/sosouni14/image_server/main/image_rev/image-20220320211729902.png)

?no=2%20or%20no=2 을 넣었더니 정답이었다.

값을 똑같은 것을 2개 넣고 or 형식으로 만들어서 admin 값이 나오게 만들었다.
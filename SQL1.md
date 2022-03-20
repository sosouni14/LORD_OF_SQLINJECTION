# LORD OF SQLINJECTION_1

![image-20220320204421767](https://raw.githubusercontent.com/sosouni14/image_server/main/image_rev/image-20220320204421767.png)

아이디와 비번이 DB에 있는 것과 일치했을 때 문제가 통과되는 것 같다.

---

### ?id=abcd

아이디를 abcd 로 넣었다.

![image-20220320205205984](https://raw.githubusercontent.com/sosouni14/image_server/main/image_rev/image-20220320205205984.png)

원본에서 아이디가 적혀지는 것을 확인 할 수 있다.

이렇게 아이디를 admin 을 넣어서 문제를 넘어가보도록 하겠다.

---

### ?id=admin

![image-20220320205351926](https://raw.githubusercontent.com/sosouni14/image_server/main/image_rev/image-20220320205351926.png)

admin 이라고 바뀌였지만 성공했다는 메시지는 뜨지 않는다.

---

### pw=admin

![image-20220320205907933](https://raw.githubusercontent.com/sosouni14/image_server/main/image_rev/image-20220320205907933.png)

pw=admin 이라고 적었을 때 id 뒤에 적혀진다.

그래서 그 뒤를 주석처리로 바꿔보겠다.

---

### ?id=admin%27%23

![image-20220320210202919](https://raw.githubusercontent.com/sosouni14/image_server/main/image_rev/image-20220320210202919.png)

뒤에 주석처리를 주었더니 비번부분이 무시하게 되어서 성공되었다.
# 5

![image-20220321213823520](https://raw.githubusercontent.com/sosouni14/image_server/main/image_rev/image-20220321213823520.png)

아이디를 `admin` 으로 하면 풀리는 문제인 것 같다.

하지만 공백을 쓰지 못한다. 공백을 쓰지않고 id=admin 이라는 문자열을 넣어야 할 것 같다.



---

### ?pw=%23or%20

![image-20220321214105489](https://raw.githubusercontent.com/sosouni14/image_server/main/image_rev/image-20220321214105489.png)

`?pw=%23or%20` 을 쓰니 No whitespace ~_~ 이 출력되었다.

`or` 을 써야하는데 공백을 쓰지 못하여 문자 `or` 이 아닌 기호 `||` 을 사용해본다.



---

### ?pw=%23%27||id=%27admin

![image-20220321214425970](https://raw.githubusercontent.com/sosouni14/image_server/main/image_rev/image-20220321214425970.png)

`or` 을 사용하면 띄어쓰기 를 사용하기 때문에 `||` 기호를 사용하여 띄어쓰기 없이 `id=admin` 을 쓸 수 있었다.
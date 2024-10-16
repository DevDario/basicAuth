<h1 align="center">
  Authentication With SpringSecurity
</h1>

<p align="center">
 <img src="https://img.shields.io/static/v1?label=Purpose&message=Learn how authentication works in Spring &color=8257E5&labelColor=000000" alt="Desafio" />
</p>

> Authentication Logic with SpringBoot Security (using hard-coded users)

see this article [Authentication and Authorization in Spring Boot 3.0 with Spring Security](https://www.geeksforgeeks.org/authentication-and-authorization-in-spring-boot-3-0-with-spring-security/)

## System Users

1. John
    - name: john
    - password: 2033
    - role: USER & ADMIN

2. Maria
    - name: Maria
    - password: 3344
    - role: USER

- Now, with that in mind you can perform request to the controller


## How to Run

- First you need to clone this to your machine
```bash
  git clone https://github.com/DevDario/basicAuth
```

- Then access it
```bash
  cd basicAuth/
```

- Now you can build the project:
```bash
$ ./mvnw clean package
```
- and then run it:
```bash
$ java -jar target/basicAuth-0.0.1-SNAPSHOT.jar
```

You can access the API here: [localhost:8080](http://localhost:8080).
> You will be redirected to the login form

You can also access the not-secure endpoint at: [localhost:8080/welcome](http://localhost:8080/welcome).

## Endpoints (use a webclient,like a browser, to perform this requests)

```bash
$ http GET :8080/login
```

if you're already authenticated(as a **USER**) you can hit this _URL_:

```bash
$ http GET :8080/auth/user/userProfile
```

And if you're already authenticated(as a **ADMIN**) you can hit this _URL_:

```bash
$ http GET :8080/auth/admin/adminProfile
```
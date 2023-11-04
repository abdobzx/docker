Docker
Hello world this is just a small docker informal

<h1>1. Installing docker on Windows </h1> 
<p>(if you have UBUNTU or any linux distribution you can found the installing step on this Url:https://docs.docker.com/engine/install/ubuntu/)</p>

![Screenshot 2023-11-04 110113](https://github.com/abdobzx/docker/assets/61870589/0331b5ff-84d0-44f1-a886-390d10d6eafc)

<p>After the install you need to restart you pc </p>



![Screenshot 2023-11-04 110910](https://github.com/abdobzx/docker/assets/61870589/57fb511d-54ed-472c-ac13-636482673ce7)

<p>You need to enable that if you work on windows to can work with WSL</p>

<h1>2. To install WSL you just need to open powershell as admin </h1>


![Screenshot 2023-11-04 113454](https://github.com/abdobzx/docker/assets/61870589/07678112-3912-46b5-8c48-45c4580b4d25)

<p>WSL UBUNTU installation with this command :</p>

```sh
wsl --install -d Ubuntu
```

<p>3. put your username and password </p>

![Screenshot 2023-11-04 113843](https://github.com/abdobzx/docker/assets/61870589/6c57657a-5403-40e7-a8e8-6eb61813f8ab)



<p>4. Changing settings into docker APP and enabling UBUNTU </p>

![Screenshot 2023-11-04 114135](https://github.com/abdobzx/docker/assets/61870589/4afc2b30-4e8a-4cac-8d07-1439b8b3e581)

<p>now you can see the containers allready runing  </p>


<p>5. make a directory call it what ever you want </p>
```sh
mkdir www
```
```sh
cd www 
```
```sh
code .  # to open the vs code of your pc from the UBUNTU WSL
```

![Screenshot 2023-11-04 114911](https://github.com/abdobzx/docker/assets/61870589/12570d5b-e31e-4f4a-a2cd-a55793c3a459)
<p>6. You gonna see an empty a vs code in my case ,I upload a small website with static html and css you cand find it on my git hub </p>
the upload proces is to open explorer from you UBNTU WSL with the command :
```sh
explorer.exe .
```


![Screenshot 2023-11-04 120001](https://github.com/abdobzx/docker/assets/61870589/d51ca243-0112-443b-b42a-f7bbdafdc284)

<p>7. The results it two file a dir and Dockerfile the github dir contain the website files and Dockeefile you need to crate on call it Dockerfile </p>


![Screenshot 2023-11-04 120119](https://github.com/abdobzx/docker/assets/61870589/7226ee86-af1e-4502-ab6f-92e3de8bdcf7)


<p>8. The last step is Dockerfile configuration </p>

```sh
FROM httpd:latest #is for apache server

MAINTAINER "abdobzx@gail.com" # you can use ure email addrese

COPY ./github /usr/local/apache2/htdocs  # the importent line you neet to put you website files path first (like ./github) and the other path is for htdocs to host you files 
```

<p>9. On the bach terminal on UBUNTU WSL put the fallowing command :</p>

```sh
docker build -t test-website .
```


```sh
docker run -d --name test-website -p 8087:80 test-website
```
<h1> Now as we see it's runuing on port 8087 </h1>



![Screenshot 2023-11-04 121438](https://github.com/abdobzx/docker/assets/61870589/8cd98a81-1132-4417-9764-66fbd27e1f91)



<p> it's time to see the results </p>

you can run it with the localhost:8087 on you browser
```sh 
localhost:8087 
```

![Screenshot 2023-11-04 121715](https://github.com/abdobzx/docker/assets/61870589/335299c6-e3a1-4ad5-a09e-e7df265dbc89)


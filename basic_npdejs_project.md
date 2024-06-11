- First pulled the node.js image from Docker swarm u can pulled it from cli or directly from 
   docker desktop⬇️

-    ![Screenshot 2024-06-08 130209](https://github.com/Rjesh2006/-Containerized_basic_Node.js-Demo-Application/assets/143868643/52a152bd-d402-4306-8403-7253e7b50f99)
     ![Screenshot 2024-06-08 130923](https://github.com/Rjesh2006/-Containerized_basic_Node.js-Demo-Application/assets/143868643/1fc0bf68-ee51-4f0f-aa89-5c5b892db187)

-    now creaated a folder for our nodejs project:
-    ![Screenshot 2024-06-08 132146](https://github.com/Rjesh2006/-Containerized_basic_Node.js-Demo-Application/assets/143868643/020100af-dd5d-43d3-acbb-3f2aa35f508a)

- now instaall node and npm for the inbuilt code file (node mudule's).
- for node modules files write the command:

```
npm init 
```
Creating package.json file :

- After you provide the necessary information, npm init will generate a package.json file in 
    your project directory.
  -  ![Screenshot 2024-06-08 132523](https://github.com/Rjesh2006/-Containerized_basic_Node.js-Demo-Application/assets/143868643/b4594d86-d682-44f2-b530-e4b346afa9a1)
 
- now creating our index.js file for our basic _project:-
- ![Screenshot 2024-06-08 134306](https://github.com/Rjesh2006/-Containerized_basic_Node.js-Demo-Application/assets/143868643/c689b671-0b4b-4a0b-aa50-d6ba9fca6bb3)

- now first  simply running our project on our localhost port:3000:30000:-
  ```
  node index.js

  ```
![Screenshot 2024-06-08 134306](https://github.com/Rjesh2006/-Containerized_basic_Node.js-Demo-Application/assets/143868643/3ddfbb6f-42dd-44db-b110-9338ffa96369)


noe here is the interface of our project where we simple written there some employe id age name so that  we can better understanding :
![Screenshot 2024-06-08 134429](https://github.com/Rjesh2006/-Containerized_basic_Node.js-Demo-Application/assets/143868643/8af6bfcf-f234-46e4-a5ac-b58581e822ed)


- now creaating img of our project by creating docker file with some comands inside the file to 
  initilization of  server.
    1. creata docker file(Dockerfile) inside ur project directory.
    2. then we will creat a image of our applicattion by docker commands :-
    3. ```
       docker build -t <image-name>

       ```
    4. also your can see here all the commands and flow :-
        -![Screenshot 2024-06-08 141156](https://github.com/Rjesh2006/-Containerized_basic_Node.js-Demo-Application/assets/143868643/5b617c1e-d0d3-4a68-838b-50801b3ec7fd)
       now u can also see the image by cli and also u can see withinn ur doker desktop
       ```
       docker images
       ```
       ![Screenshot 2024-06-08 141456](https://github.com/Rjesh2006/-Containerized_basic_Node.js-Demo-Application/assets/143868643/afbd5254-a38e-47be-9400-ce4c93fd0126)


       docker dessktop:-
       ![Screenshot 2024-06-08 141303](https://github.com/Rjesh2006/-Containerized_basic_Node.js-Demo-Application/assets/143868643/877cedbb-0c81-46be-9e5e-cc4477bbf069)


       now creating container with docoker desktop:-
        - ![Screenshot 2024-06-08 143049](https://github.com/Rjesh2006/-Containerized_basic_Node.js-Demo-Application/assets/143868643/b3005fd6-5163-48f9-8b48-8f730ad6cc87)
      
       now after running with docker desktop running conatainer :
      - ![Screenshot 2024-06-08 143145](https://github.com/Rjesh2006/-Containerized_basic_Node.js-Demo-Application/assets/143868643/e6916d6e-ed89-4db9-b929-db3afd0510f8)


     - her is the better view:
     - ![Screenshot 2024-06-08 143225](https://github.com/Rjesh2006/-Containerized_basic_Node.js-Demo-Application/assets/143868643/75e49535-cd8f-41d6-b4e4-0759fce39e5c)
    
We need to address a problem with our server: updating our application currently requires manual intervention, which takes a significant amount of time and results in extended server downtime. To solve this, we need a solution that automates the server update process, minimizing downtime. This is where Nodemon comes into play. Nodemon is a server automation service that will restart the server within milliseconds during updates, greatly improving our efficiency.

```
npm i nodemon
```

  - also u can see in the given figure :
  - ![Screenshot 2024-06-09 132447](https://github.com/Rjesh2006/-Containerized_basic_Node.js-Demo-Application/assets/143868643/c1eab77e-f010-41f7-8f83-b1c8fcabc1e8)

  - then assign nodemon in your package,jason file cahnge running commands as-
  - (node run dev instead of node index.js)
  - ![Screenshot 2024-06-09 162802](https://github.com/Rjesh2006/-Containerized_basic_Node.js-Demo-Application/assets/143868643/4ef46ba2-9f8e-4542-802f-fe29ad9b9eee)


  - after that we will run our application via system local host :-
 ```
node run dev 
 ```
   - ![Screenshot 2024-06-09 133330](https://github.com/Rjesh2006/-Containerized_basic_Node.js-Demo-Application/assets/143868643/5f468e45-4ac5-4bdd-823f-765e0f4aa8c2)

   - if u will change somthng in server run time it auto update those thinnks also you  can see the update as greeen line while u willl update somethinng in ur application then u will be see
   - green lines comments :-

     - ![Screenshot 2024-06-09 133420](https://github.com/Rjesh2006/-Containerized_basic_Node.js-Demo-Application/assets/143868643/7ec7bfc4-c264-4b48-ba2b-86cd4272765d)


now re creating all this thinks for docker img now in docker we putiing nodemon so we have to change our commands in docker file simontaneously:-
![Screenshot 2024-06-09 135128](https://github.com/Rjesh2006/-Containerized_basic_Node.js-Demo-Application/assets/143868643/89e2a538-cb13-4d10-bb11-5a025fc3ec6c)

-  then  recreat the img :-
    - ![Screenshot 2024-06-09 135144](https://github.com/Rjesh2006/-Containerized_basic_Node.js-Demo-Application/assets/143868643/a514970b-f0c6-4f3a-ac8a-a87586c62f21)

then after the container establised you have to run app  by this commands -
```
node run dev 
```
then u will see:-  
  - ![Screenshot 2024-06-09 161615](https://github.com/Rjesh2006/-Containerized_basic_Node.js-Demo-Application/assets/143868643/1a3a4458-203e-4d7c-b391-23c97b59ea5d)

  - here the green line inside he docker terminal represents as update in application:-
   - ![Screenshot 2024-06-09 161638](https://github.com/Rjesh2006/-Containerized_basic_Node.js-Demo-Application/assets/143868643/60b89d8a-9bf2-44ef-ac45-7998e165be00)

now here is the final view where u can better iunderstand the update in the node.js project app :- 
   - ![Screenshot 2024-06-09 192745](https://github.com/Rjesh2006/-Containerized_basic_Node.js-Demo-Application/assets/143868643/2359ff55-3140-4670-ae6d-63d3404310e3)

     
                                               🥇

We will creat a compose docker :- file for the to get relax form these vast commands to start our application or u can saay for higher scalability and then we will push it on dockerhb soon .............⏬
Update to be continued >>>>>>>>>>>>>>>>>






   



       

       

  


# Build-and-deploy-a-ML-API-with-Python-and-AWS-Sagemaker

Architecture:

<img width="1121" alt="Screenshot 2024-03-21 at 17 45 02" src="https://github.com/redjules/Build-and-deploy-a-ML-API-with-Python-and-AWS-Sagemaker/assets/106017493/c279b6e2-4de0-4cc4-b87d-833be9fa84a4">

go to Sagemaker and Notebook, Notebook instances:

<img width="1304" alt="Screenshot 2024-03-21 at 17 55 49" src="https://github.com/redjules/Build-and-deploy-a-ML-API-with-Python-and-AWS-Sagemaker/assets/106017493/907fa1fe-0fde-400a-8075-cf5870949137">

you create a role:

<img width="654" alt="Screenshot 2024-03-21 at 17 56 32" src="https://github.com/redjules/Build-and-deploy-a-ML-API-with-Python-and-AWS-Sagemaker/assets/106017493/fe38adb4-2ebf-4237-9ade-13ac81c9a749">


we open the jupyter notebook:


<img width="613" alt="Screenshot 2024-03-21 at 17 57 59" src="https://github.com/redjules/Build-and-deploy-a-ML-API-with-Python-and-AWS-Sagemaker/assets/106017493/ace0f9ea-c8b5-4618-921b-db03275c7051">

We will be classifying the data in 3 classes:

- Iris setosa
  
- Iris versicolor
  
- Iris virginica


We have 4 features in our dataset:

<img width="426" alt="Screenshot 2024-03-21 at 18 01 19" src="https://github.com/redjules/Build-and-deploy-a-ML-API-with-Python-and-AWS-Sagemaker/assets/106017493/da6f37be-38af-4b80-b636-adaa82b9b0f0">

<img width="833" alt="Screenshot 2024-03-21 at 18 04 17" src="https://github.com/redjules/Build-and-deploy-a-ML-API-with-Python-and-AWS-Sagemaker/assets/106017493/ec168d3a-388d-4586-9b3e-79f93ffb6a45">

<img width="660" alt="Screenshot 2024-03-21 at 18 06 26" src="https://github.com/redjules/Build-and-deploy-a-ML-API-with-Python-and-AWS-Sagemaker/assets/106017493/92efb545-56a2-4925-9dfa-e6999fd57866">


![Screenshot 2024-03-21 at 22 37 50](https://github.com/redjules/Build-and-deploy-a-ML-API-with-Python-and-AWS-Sagemaker/assets/106017493/61bd3f88-b639-4283-af7b-2c6fd05913c9)

create a bucket in S3:


![Screenshot 2024-03-21 at 22 38 48](https://github.com/redjules/Build-and-deploy-a-ML-API-with-Python-and-AWS-Sagemaker/assets/106017493/9458251f-ebf6-4042-8287-edf80d46f92e)

![Screenshot 2024-03-21 at 23 56 16](https://github.com/redjules/Build-and-deploy-a-ML-API-with-Python-and-AWS-Sagemaker/assets/106017493/3571ff1c-506d-497c-8be0-19cae374bd1b)


we move the data into the s3 bucket:

![Screenshot 2024-03-21 at 23 36 09](https://github.com/redjules/Build-and-deploy-a-ML-API-with-Python-and-AWS-Sagemaker/assets/106017493/f12499cf-0f1b-47b5-a2d7-e4d2edcfadc6)

we create a model:

![Screenshot 2024-03-21 at 23 54 53](https://github.com/redjules/Build-and-deploy-a-ML-API-with-Python-and-AWS-Sagemaker/assets/106017493/84b131d5-81c8-4b34-a81f-26ae27ed875f)

![Screenshot 2024-03-21 at 23 58 11](https://github.com/redjules/Build-and-deploy-a-ML-API-with-Python-and-AWS-Sagemaker/assets/106017493/e0766ba1-2977-486b-8e54-627fcd3d3b7b)

![Screenshot 2024-03-21 at 23 58 30](https://github.com/redjules/Build-and-deploy-a-ML-API-with-Python-and-AWS-Sagemaker/assets/106017493/f4304aeb-dc17-4580-9390-81f58d7fb891)

and we deploy the model:

![Screenshot 2024-03-21 at 23 59 47](https://github.com/redjules/Build-and-deploy-a-ML-API-with-Python-and-AWS-Sagemaker/assets/106017493/411b771f-5b52-4bd6-884f-c5c16f97abaa)

![Screenshot 2024-03-22 at 00 01 14](https://github.com/redjules/Build-and-deploy-a-ML-API-with-Python-and-AWS-Sagemaker/assets/106017493/2ae82668-fe4e-4e72-8884-ea6000dd2195)

we create the lambda function:

![Screenshot 2024-03-22 at 00 15 47](https://github.com/redjules/Build-and-deploy-a-ML-API-with-Python-and-AWS-Sagemaker/assets/106017493/355f05a5-0078-47ef-a0d2-7adb28c6e83b)


we create an execution role with IAM:

![Screenshot 2024-03-22 at 00 18 15](https://github.com/redjules/Build-and-deploy-a-ML-API-with-Python-and-AWS-Sagemaker/assets/106017493/b9396a46-8d48-4f8b-a6ff-64309815145f)

![Screenshot 2024-03-22 at 00 18 43](https://github.com/redjules/Build-and-deploy-a-ML-API-with-Python-and-AWS-Sagemaker/assets/106017493/ef988ee8-8572-46bd-afce-fb9f90ad3bd9)

we define a test event:

![Screenshot 2024-03-22 at 00 19 50](https://github.com/redjules/Build-and-deploy-a-ML-API-with-Python-and-AWS-Sagemaker/assets/106017493/5f3a7e91-ae8c-4a4d-9b7b-834e5a181613)

![Screenshot 2024-03-22 at 00 20 50](https://github.com/redjules/Build-and-deploy-a-ML-API-with-Python-and-AWS-Sagemaker/assets/106017493/cb64285c-81e1-4fce-963e-1fd64937f705)

we go to API Gateway and create the API:

![Screenshot 2024-03-22 at 00 23 24](https://github.com/redjules/Build-and-deploy-a-ML-API-with-Python-and-AWS-Sagemaker/assets/106017493/f39a0545-01b0-4a55-b972-b777a807059b)

![Screenshot 2024-03-22 at 00 24 03](https://github.com/redjules/Build-and-deploy-a-ML-API-with-Python-and-AWS-Sagemaker/assets/106017493/a279a17d-5085-4e31-bd6e-f8a821f6aa73)

![Screenshot 2024-03-22 at 00 24 33](https://github.com/redjules/Build-and-deploy-a-ML-API-with-Python-and-AWS-Sagemaker/assets/106017493/7a26a095-fd00-467f-904a-16c26f6fa6f2)

![Screenshot 2024-03-22 at 00 28 36](https://github.com/redjules/Build-and-deploy-a-ML-API-with-Python-and-AWS-Sagemaker/assets/106017493/ac7e7d36-d3c4-46f0-9409-52babd9790a2)


![Screenshot 2024-03-22 at 00 31 12](https://github.com/redjules/Build-and-deploy-a-ML-API-with-Python-and-AWS-Sagemaker/assets/106017493/0b46bafd-8f37-49dc-a055-68737dc66034)


We go to Postman now and we copy the url of the API:

![Screenshot 2024-03-22 at 00 33 15](https://github.com/redjules/Build-and-deploy-a-ML-API-with-Python-and-AWS-Sagemaker/assets/106017493/13fb0d23-fbea-4dc0-9923-ee62b70db0ea)

we copy the values of an entry:

![Screenshot 2024-03-22 at 00 34 20](https://github.com/redjules/Build-and-deploy-a-ML-API-with-Python-and-AWS-Sagemaker/assets/106017493/d1f0827b-58a5-4880-94cc-3497e6d860cd)

and we get the right prediction so it works!:

![Screenshot 2024-03-22 at 00 35 13](https://github.com/redjules/Build-and-deploy-a-ML-API-with-Python-and-AWS-Sagemaker/assets/106017493/96710dac-620d-4384-8f47-80af5d5d89c7)

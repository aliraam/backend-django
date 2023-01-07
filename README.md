<!-- PROJECT LOGO -->
<br />
<div align="center">
  <h3 align="center">Backend-django</h3>

  <p align="center">
    backend api service / Django python
    <br />
    <a href="https://radeband.ir/">View Demo</a>
    ·
    <a href="https://github.com/radeband/backend-django/issues">Report Bug</a>
    ·
    <a href="https://github.com/radeband/backend-django/issues">Request Feature</a>
  </p>
</div>


<!-- ABOUT THE PROJECT -->
## About The Project

This is the central part of the Radeband project, which is responsible for communicating as API at the service backend.

Components:
* Base
* Account 
* Company

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- GETTING STARTED -->
## Getting Started


### Prerequisites

You'll need a Postgres database up and running to start this project. You can use the docker-compose.yml file in the project's root directory to set it up and run it or use your own before configuring the database.
```sh
docker compose up -d
```

#### Environment variables
django variables:

* **SECRET_KEY:** This value is the key to securing signed data – you must keep this secure, or attackers could use it to generate their own signed values.


database variables:
* **DB_HOST:** database host address 
* **DB_NAME:** database name
* **DB_USER:** database username
* **DB_PASS:** database password
* **DB_PORT:** database port (default=5432)


s3 variables:
* **S3_PROVIDER:** The provider name that used at the start of other variables to define which provider should be used. ex. {S3_PROVIDER}_S3_ACCESS_KEY
* **S3_CUSTOM_DOMAIN:**
* **{S3_PROVIDER}_S3_ACCESS_KEY:** S3 access ID
* **{S3_PROVIDER}_S3_SECRET_KEY:** S3 secret access key
* **{S3_PROVIDER}_S3_BUCKET_NAME:** S3 bucket name for staticfiles
* **{S3_PROVIDER}_S3_ENDPOINT_URL:** S3 url that points to your bucket



otp variables:
* **SMS_SECRET_KEY:** 
* **SMS_PROVIDER:** The provider name that used at the start of other variables to define which provider should be used. ex. {SMS_PROVIDER}_URL
* **{SMS_PROVIDER}_URL:** sms provider api url
* **{SMS_PROVIDER}_KEY:** sms provider api token
* **{SMS_PROVIDER}_SENDER:** sms provider sender line number


#### Migrations
Next, you need to make some migrations into your database. we already have pushed migration files in the repository, but you can make those files if you lost them via this command:
```sh
python manage.py makemigrations
```

So, you can run your migrations right now:
```sh
python manage.py migrate
```

<br/>

### Usage

1. Setup postgresql database
2. configure environment variables
3. run migrations
4. start the application

    You can start the application with python command or using docker.
    python cli:
    ```sh
    python manage.py runserver
    ```

    docker (recommended):
    <!-- TODO -->

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'feat(core-section): add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request


<!-- CONTACT -->
## Contact

Javad Naghiloo - contact@naghiloo.com

Project Link: [https://github.com/radeband/backend-django](https://github.com/radeband/backend-django)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

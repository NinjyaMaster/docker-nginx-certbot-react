# docker-nginx-certbot-react

<a name="readme-top"></a>
<!--
*** I use REAME.md template from https://github.com/othneildrew/Best-README-Template
*** -----------
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->


<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]


<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/NinjyaMaster/docker-nginx-certbot-react">
    <h3 align="center">Docker-Nginx-Certbot-React-Settings</h3>
  </a>



  <p align="center">
A basic sample of setting up React, NGINX, and Certbot in a Docker container:
    <br />
    <a href="https://github.com/NinjyaMaster/docker-nginx-certbot-react/"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    ·
    <a href="https://github.com/NinjyaMaster/docker-nginx-certbot-react/issues">Report Bug</a>
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    
  </ol>
</details>


<!-- ABOUT THE PROJECT -->
## About The Project


This project provides a simple yet straightforward guide on setting up a web application using React, Nginx, and Certbot, all neatly contained within Docker. This setup streamlines the deployment process and makes it effortless to host a secure, high-performing web application.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



### Built With

* [![React][React.js]][React-url]
* [![Docker][Docker.com]][Docker-url]
* [![NGINX][NGINX.com]][NGINX-url]
* [![Certbot][certbot.eff.org]][Certbot-url]

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- GETTING STARTED -->
## Getting Started

Before you start with the project setup, there are some prerequisites that you need to ensure are in place.

### Prerequisites

#### SSL/TLS Certificates

This project requires SSL/TLS certificates to be under the /etc/letsencrypt directory of your machine. The certificate files specifically needed are fullchain.pem and privkey.pem. These files are essential for setting up a secure HTTPS connection for your web application.

* Update your package lists for upgrades and new package
  ```sh
  sudo apt-get update
  ```

* Install certbot
  ```sh
  sudo apt-get install certbot
  ```
* Obtaining an SSL Certificate
  ```sh
  sudo certbot --nginx -d yourdomain.com -d www.yourdomain.com
  ```
* Close any servers running on port 80:
  If you're running Apache
  ```sh
  sudo service apache2 stop
  ```
  If you're running Nginx
  ```sh
  sudo service nginx stop
  ```

* Run Certbot in Standalone mode:
  ```sh
  sudo certbot certonly --standalone
  ```

* Cert files location:
  If everything was successful, your certificate and key will be generated and placed in the following directory:
  ```sh
  /etc/letsencrypt/live/your-domain-name/
  ```
  where your-domain-name is the domain for which you've received the certificate.




### Installation

1. Clone the repo
   ```sh
   git clone https://github.com/NinjyaMaster/docker-nginx-certbot-react.git
   ```
3. Edit  <a href='https://github.com/NinjyaMaster/docker-nginx-certbot-react/blob/main/nginx/default-https.conf'>default-https.conf</a>
   ```sh
   nano ./nginx/default-https.conf
   ```
   Please ensure that you replace yourdomain.com with your actual domain name.
4. Run Docker
   ```js
   docker-compose -f docker-compose-https.yml -d up
   ```

<p align="right">(<a href="#readme-top">back to top</a>)</p>





<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTACT -->
## Contact

Mia Noriko Watanabe - [@linkedin](https://linkedin.com/in/mia-noriko-watanabe-27727b2)

Project Link: [https://github.com/NinjyaMaster/docker-nginx-certbot-react](https://github.com/NinjyaMaster/docker-nginx-certbot-react)

<p align="right">(<a href="#readme-top">back to top</a>)</p>





<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/NinjyaMaster/docker-nginx-certbot-react.svg?style=for-the-badge
[contributors-url]: https://github.com/NinjyaMaster/docker-nginx-certbot-react/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/NinjyaMaster/docker-nginx-certbot-react.svg?style=for-the-badge
[forks-url]: https://github.com/NinjyaMaster/docker-nginx-certbot-react/network/members
[stars-shield]: https://img.shields.io/github/stars/NinjyaMaster/docker-nginx-certbot-react.svg?style=for-the-badge
[stars-url]: https://github.com/NinjyaMaster/docker-nginx-certbot-react/stargazers
[issues-shield]: https://img.shields.io/github/issues/NinjyaMaster/docker-nginx-certbot-react.svg?style=for-the-badge
[issues-url]: https://github.com/NinjyaMaster/docker-nginx-certbot-react/issues
[license-shield]: https://img.shields.io/github/license/NinjyaMaster/docker-nginx-certbot-react.svg?style=for-the-badge
[license-url]: https://github.com/NinjyaMaster/docker-nginx-certbot-react/blob/main/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/mia-noriko-watanabe-27727b2
[product-screenshot]: images/screenshot.png
[Next.js]: https://img.shields.io/badge/next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white
[Next-url]: https://nextjs.org/
[React.js]: https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB
[React-url]: https://reactjs.org/
[Vue.js]: https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vuedotjs&logoColor=4FC08D
[Vue-url]: https://vuejs.org/
[Angular.io]: https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white
[Angular-url]: https://angular.io/
[Svelte.dev]: https://img.shields.io/badge/Svelte-4A4A55?style=for-the-badge&logo=svelte&logoColor=FF3E00
[Svelte-url]: https://svelte.dev/
[Laravel.com]: https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white
[Laravel-url]: https://laravel.com
[Bootstrap.com]: https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white
[Bootstrap-url]: https://getbootstrap.com
[JQuery.com]: https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white
[JQuery-url]: https://jquery.com 
[Docker.com]: https://img.shields.io/badge/docker-0769AD?style=for-the-badge&logo=docker&logoColor=white
[Docker-url]: https://www.docker.com/
[NGINX.com]: https://img.shields.io/badge/nginx-0769AD?style=for-the-badge&logo=nginx&logoColor=white
[NGINX-url]: https://nginx.org/
[certbot.eff.org]: https://img.shields.io/badge/certbot-0769AD?style=for-the-badge&logo=certbot&logoColor=white
[Certbot-url]: https://certbot.eff.org/
[default-https-url]: https://github.com/NinjyaMaster/docker-nginx-certbot-react/blob/main/nginx/default-https.conf

# Spider Inductions '23 Onsites - Day 2
**NOTE**

We value your attempts. Try to do as much as possible. Happy learning !!!

# Application & API Pentesting
<details>
<summary>Brute Force (Day 1 - Unsolved)</summary>
An important part of securing your applications is having strong passwords. A weak password can be susceptible to brute force attacks which are when common passwords are directly fed into a website's login page. 

Your task is to log in to the admin account with the help of tools such as Burp-Suite and Hydra to execute a brute-force attack.

[Website link](http://testasp.vulnweb.com/)
</details>

<details>
<summary>Reverse Inductions (Day 1 - Unsolved)</summary>
Endpoint analysis is an important step in a penetration testing process that identifies all available endpoints of the target API. The Spider inductions portal interacts with a REST API to perform operations on the participants' data. 

You are assigned the task to reverse engineer the API and identify all accessible endpoints. You should also figure out the request and response schema. Submit your report as a postman collection.

[Spider Inductions Portal Link](https://inductions.spider-nitt.org)
</details>

<details>
<summary>Tech Stack Recon</summary>
The first step in successfully pen-testing any website is to fully understand the application. This is where active reconnaissance comes into play which is where you use various tools to probe an application to get information such as open ports, IP addresses, or the entire tech stack of a website.

Your first task is to find the OD(On Duty) website created by SPIDER. Once you have found the website, it is your job to get the public and private IPs as well as the tech stack of the website. This includes frontend, backend, DB, and proxy servers.

[Hint: The OD website is hosted on the local spider server]
</details>

# Web 2 Applications
<details>
<summary>OpenLDAP</summary>

Setup an OpenLDAP server with the following Directory Information Tree
- Organizational units(OU) = users, domains
- Groups = students, teachers (within users OU)

Create a user account for you within the student's group and perform the binding. Entities should be created only using LDIF files
</details>

<details>
<summary>Trusted Web Activity</summary>

Build a Progressive Web Application that hosts a stone paper scissor game against a bot that makes random choices. Trigger a notification at the end of each game. The "Update Available" button should appear when the service worker receives new content, and on clicking it, new content should appear in the app.
Generate an Android build for the application using Trusted Web Activity.

</details>

<details>
<summary>URL Shortner</summary>

Design a URL shortener service that takes a long URL as input and generates a short, unique code for it. When users access the short URL, they should be redirected to the original URL. For the front end, you can make either a mobile or web app.

</details>

# Computer Networking
<details>
<summary>Recursive Caching DNS Server</summary>

As a system architect, you are assigned the task of setup a recursive caching domain name server for the internal network with the below functionalities.
- Allow queries from a specific subnet
- Configure forwarding to Google's name server for outside domains
- Setup a DNS zone with reverse and forward zone configurations
- In the zone files, include records for a web server and cname for it.
For the demonstration purpose, you can use host the DNS server and the web server on the same machine. You can use any DNS server such as Bind, CoreDNS, etc. A simple web server will suffice.

</details>
<details>
<summary>SSH Honeypot</summary>

It is common for hackers to utilize brute force attacks in an attempt to gain unauthorized access to a victim's machine. Design and deploy an efficient honeypot on port 22 that convincingly emulates a vulnerable SSH server. Log all the information available about the attacker.

</details>

# System Design
<details>
<summary>InnoDB MySQL Cluster</summary>

During the production yesterday, we can see a significant load on the MySQL database. You are assigned to set up an InnoDB MySQL cluster that performs group replication. There should be two secondary nodes and a primary node. For the sake of demonstration, you can use MySQL containers.

</details>

# Web Automation
<details>
<summary>Reddit Bot</summary>

Create a Discord bot that fetches data from Reddit, such as top posts from a specified subreddit, and automatically shares this content in a designated Discord channel. The bot enhances community engagement by seamlessly delivering relevant Reddit content within the Discord server.

</details>
<details>
<summary>Site Docs Summarizer (Day 1 - Unsolved)</summary>
You have to build a Chrome extension that can be used to summarize all the links that lead to any document (.pdf, .doc, .xls, etc.) within a URL, and when a user clicks on the extension popup, it should show all the links along with the summary of the content within them. 

● For the summarization part **you are not required to create your own summarization pipleine**, Instead [Hugging Face](https://huggingface.co/) provides something called [Inference APIs](https://huggingface.co/inference-api). These are API endpoints for any particular model made available by Hugging Face. All you need to do is review the docs, figure out how to send proper Requests and get the summarized content.

   > For example, you could use something like the [Document Summarizer](https://huggingface.co/spaces/pszemraj/document-summarization) model with its Inference API (by going to "Use via API" at the bottom)
   > The above is just an example. You can use any model, and it's Inference API for this.

</details>

# Decentralized Applications
<details>
<summary>Decentralized Chat App (Day 1 - Unsolved)</summary>
Create a decentralized chat app that relies on peer-to-peer communication without depending on a central server.

- Allow the users to chat personally with other users.
- Implement a group chat feature.
</details>

<details>
<summary>Election DApp</summary>
Build a decentralized application (DApp) for holding an election between two candidates using the Ethereum blockchain. The smart contract should manage the election process, allowing accounts connected to the network to vote for their preferred candidate. Additionally, real-time vote count updates will be displayed during the election.
</details>

# DevOps

<details>
<summary>Movie docker container</summary>

Write a bash script that requests info from the [OMDB](https://www.omdbapi.com) for a given movie.

```bash
bash GetMovieData.sh Inception
```


The data should be saved into a Mongodb container with the following collections: 
- Movies 
- Actors  
- Directors 
- Genres 



 Store only `Title,` `Year,` `Release Date,` `Runtime,` `Director,` `Actor,` `Box Office`  in the **Movies** collection.

Parse the `Actors` field of JSON response and add each actor in the **Actors** collection, as follows using awk. Do the same for `Directors` and `Genres` collections.

```json
{
    "Actors": "Leonardo DiCaprio, Joseph Gordon-Levitt, Elliot Page"
}
```

```json
[
  {
    "name": "Leonardo DiCaprio"
  },
  {
    "name": "Joseph Gordon-Levitt"
  },
  {
    "name": "Elliot Page"
  }
]
```



Have a cronjob that takes a backup of the movie collection. 

Run a separate  container and save the movie poster in the `/images` directory.

</details>

<details>
<summary>Darkweb Site</summary>
As a cybercop of the dark web, it's your responsibility to know how websites are hosted in the dark web to prevent crimes. You are assigned the task of hosting a simple html page that's accessible on the Tor network. Feel free to use any web server.
</details>

<details>
<summary>Load Testing</summary>
A JWT-based authentication REST API goes into production next week. We expect around 100 concurrent users. Perform a load test on the given API and the flow of requests should be as mentioned below.
- /register
- /login
- /authenticated
Perform the load test and submit the response report. We suggest you use **Artillery** to perform the load testing. You can do your own research as well.

You have to set up the API locally.

[API LINK](https://github.com/tx2z/jwt-server)

**Note**
Use Mongo version<6 to avoid legacy errors. So, if you are using docker, update the docker-compose file accordingly.
## Documentation
### POST  /register

**Request body**
```json
{
    "email":"",
    "password":""
}
```
**Response**
```json
{
    "_id": "",
    "email": "",
    "password": "",
    "__v": 0
}
```
### POST  /login

**Request body**
```json
{
    "email":"",
    "password":""
}
```
**Response**
```json
{
    "token": ""
}
```
### GET /authenticated

**Request header**
```json
{
    "Authorization": "Bearer <token>"
}
```
**Response**
```json
{
    "msg": "Hey <email>"
}
```
</details>

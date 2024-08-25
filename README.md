<div align="center">
       <h1> 
        <p>
          <a href="https://github.com/RocketChat/RC.Guided.Tours">Graphical Guided Codetour</a> </a> for <a href="https://rocket.chat/">Rocket.Chat</a>
        </p>
      </h1>
    <a href="https://summerofcode.withgoogle.com/projects/#6521788818784256"><img src="https://i.imgur.com/pgkUceb.png" width="650" alt="google-summer-of-code"></a>
    <br>
</div>
<br>

### Project [link](https://github.com/RocketChat/RC.Guided.Tours)

## ⭐ Project Abstract

`Graphical Guided RC Code Tours` helps new contributors kickstart their open-source journey with rocket.chat.

VS Code comes with a CodeTour Extension, and with its help, any person can quickstart their journey by going through all the tours, instead of reading the complete documentation. It is something like someone with a handholding harness that explains the code in the editor while going through multiple steps in **Exact File And Exact Line**. 

This project involves the development of a set of guided tutorials with diagrams and flowcharts helping new developers to understand the codebase quickly and start contributing.

 Yearly more than 500 contributors show interest in contributing to Rocket.Chat but more than 90% of them end up leaving their journey but we hope decrease this percentage exponentially with the help of this project.

## ⚙️ Deliverables
The following are the Deliverables
- Added helpful diagrams, flowchart, edited old tours  and created new tours
- Created a node.js script to dynamically generate the .tours file attaching all tours steps to their approriate line number.
- Created set of 11 tours to make any contributor or developer familiar with the codebase

**All of the targets were completed during the GSOC period✨**

## ⚒  Demo Video
[](https://github.com/user-attachments/assets/44e2be20-43ea-4eb7-941d-e05aeaa8f95a)
- Do read the [project readme](https://github.com/RocketChat/RC.Guided.Tours?tab=readme-ov-file#rcguidedtours-for-rocketchat) to setup the project and give an honest feedback in this [channel](https://open.rocket.chat/channel/RC-Guided-Tours).

### 🚢 Available CodeTours

<div align="center">
    
| **S no.** | Tour |
|:--------------------|:-------------------|
| 01 | Rocket.Chat Onboarding |
| 02 | Understanding Monorepo Structure of Rocket.Chat |
| 03 | Repository Overview |
| 04 | How to send a message (Client Side) |
| 05 | How to send a message (Server Side) |
| 06 | How to create an endpoint |
| 07 | How to create a DB model |
| 08 | How to use DB model |
| 09 | Services in Rocket.Chat |
| 10 | How to Add a new Services |
| 11 | How to create a new Package |
</div>

## 😎 Posts regarding GSOC
    
Do Checkout my Linkedin Posts regarding GSOC
    
<div align="center">
    
| **S no.** | Post |
|:--------------------|:-------------------|
| 1 | [GSOC general guidance](https://www.linkedin.com/posts/sayan-banerjee-77603a23b_gsoc-organizations-activity-7206663891857072128-fdbL?utm_source=combined_share_message&utm_medium=member_desktop) |
| 2 | [Quick podcast with Harkirat Singh](https://www.linkedin.com/posts/sayan-banerjee-77603a23b_google-summer-of-code-what-have-they-done-activity-7203385681895673856-bn9d?utm_source=combined_share_message&utm_medium=member_desktop) |
    
</div>

## 🤯 Problems That I Faced During GSOC
### Understanding Codebase

In order to create or edit any tour, the first requirement was to have a good understanding of the Codebase and different tech stacks used by rocket.chat, I spent a good amount of time learning about different APIs, methods used in rocket.chat and solved serveral issues making [10+ merged Pull Reqeusts](https://github.com/search?q=type%3Apr+author%3ASayan4444+is%3Amerged+created%3A%3E%3D2023-11-20+repo%3ARocketChat%2FRocket.Chat+repo%3ARocketChat%2FRocket.Chat.Electron+repo%3ARocketChat%2FDocker.Official.Image+repo%3ARocketChat%2FRocket.Chat.ReactNative+repo%3ARocketChat%2FRocket.Chat.js.SDK+repo%3ARocketChat%2FRocket.Chat.py.SDK+repo%3ARocketChat%2FRocket.Chat.Livechat+repo%3ARocketChat%2FRocket.Chat.Embedded.arm64+repo%3ARocketChat%2FRocket.Chat.Embedded.armhf+repo%3ARocketChat%2Falexa-rocketchat+repo%3ARocketChat%2FOpensource-Contribution-Leaderboard+repo%3ARocketChat%2FApps.GitHub+repo%3ARocketChat%2Ffuselage+repo%3ARocketChat%2Falexa-rocketchat-notification+repo%3ARocketChat%2Falexa-rocketchat-flashbriefing+repo%3ARocketChat%2Falexa-news-publisher+repo%3ARocketChat%2Falexa-rc-multiserver-client+repo%3ARocketChat%2FApps.Rasa+repo%3ARocketChat%2FApps.Dialogflow+repo%3ARocketChat%2FRC4Github+repo%3ARocketChat%2Frocket.chat.app-poll+repo%3ARocketChat%2Fdeveloper-docs+repo%3ARocketChat%2FRC4Community+repo%3ARocketChat%2FRC4Conferences+repo%3ARocketChat%2FApps.Github22+repo%3ARocketChat%2FEmbeddedChat+repo%3ARocketChat%2FRocket.Chat.Demo.App+repo%3ARocketChat%2Fdocs+repo%3ARocketChat%2FApps.Notion+repo%3ARocketChat%2FApps.Whiteboard+-label%3Achore&type=pullrequests)

### Dynamic Codebase
A significant challenge developers encountered when using CodeTours is the ever-evolving nature of the codebase. To show a step, codetours assigns a line number to it, thus to ensure the smooth functioning of the tours, one had to regularly review and adapt them to accommodate these ongoing changes.

To solve this issue I created a node.js script which  dynamically generates the .tours folder assigning appropriate line numbers for each steps of the tours according to the present status of the codebase.

*How I did it?*

I am using a very basic string search algorithm, i.e. each tours needs to search a unique string on which the tour will be assigned to. One may argue that what if the searchString changes. This is a valid point but since in Rocket.Chat CodeTours is used to describe the core part of the codebase, the searchString assigned is very unlikely to change and something really major might have happened if it does.

### Merge issues with main codebase
For the node.js script to execute it needs access of the Rocket.Chat codebase. So initially I made a npm-script in the main codebase, which on execution will generate the tours. But later we got a strict instruction that nothing can be merged in the main codebase and this project must act `independently`


*How I solved it?*

I cam up with this architecture
![image](https://github.com/user-attachments/assets/5834ab00-a782-423c-a16f-d1ee720c3371)


Our main objective was to prevent the `.tours` and `RC.Guided.Tours` to be mistakenly pushed while making a contribution and thus must be gitignored. Since we cant make any change in the `.gitignore` file of the main repo, our shell scripts adds them inside `.git/info/exclude` file thus acting same like gitignore but for the local repository only.


### Making the tours interactive and fun

Its well known that how boring it can be for developers to read texts. I tried spice things up by adding some images but in most of the tours, the content is so well written written like adding an image is unecessarey.

## 🎓 Mentors

I would like to express my heartfelt gratitude to my mentor, Aditya Singh, without whom this journey would not have been this smooth. His unwavering support and guidance helped me grow both professionally and as a person.  


- **Aditya Singh** - [Github](https://github.com/AdityaSingh-02) [LinkedIn](https://www.linkedin.com/in/aditya-singh-76065422b/)

## 💬 Connect With Me    
I am 3rd year student at NIT Durgapur studying CSE and an upcoming Google SWE Summer Intern 2025. Want to discuss GSOC / OPEN SOURCE / DSA or how to increase your CGPA?? Lets connect!! 
<div align="center">

| **Student** | Sayan Banerjee |
|:--------------------|:-------------------|
| **Organization** | [Rocket.Chat](https://rocket.chat/) |
| **GitHub** | [Sayan4444](https://github.com/Sayan4444) |
| **LinkedIn** | [Sayan Banerjee](https://www.linkedin.com/in/sayan-banerjee-77603a23b/) |
| **Email** | sayanbanerjee2002@gmail.com |
| **Rocket.Chat** | [sayan.banerjee](https://open.rocket.chat/direct/sayan.banerjee) |
</div>

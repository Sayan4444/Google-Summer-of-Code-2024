<div align="center">
       <h1> 
        <p>
          <a href="https://github.com/Sayan4444/Rocket.Chat/tree/codetours">Graphical Guided Codetour</a> </a> for <a href="https://rocket.chat/">Rocket.Chat</a>
        </p>
      </h1>
    <a href="https://summerofcode.withgoogle.com/projects/#6521788818784256"><img src="https://i.imgur.com/pgkUceb.png" width="650" alt="google-summer-of-code"></a>
    <br>
</div>
<br>

## ⭐ Project Abstract

`Graphical Guided RC Code Tours` helps new contributors kickstart their open-source journey with rocket.chat.

VS Code comes with a CodeTour Extension, and with its help, any person can quickstart their journey by going through all the tours, instead of reading the complete documentation. It is something like someone with a handholding harness that explains the code in the editor while going through multiple steps in **Exact File And Exact Line**. 

This project involves the development of a set of guided tutorials with diagrams and flowcharts helping new developers to understand the codebase quickly and start contributing. The ever evolving nature of Rocket.Chat posses a challenge to us, thus we also have created a script to generate these .tours files dynamically.

 Yearly more than 500 contributors show interest in contributing to Rocket.Chat but more than 90% of them end up leaving their journey but we hope decrease this percentage exponential with the help of this project. In the coming years there will surely be an increase in contributors making worthy contributions to rocket.chat

## ⚙️ Deliverables
The following are the Deliverables
- Added helpful diagrams, flowchart, edited old tours  and created new tours
- Created a script to dynamically generate the .tours file
- Set of 11 essential tours which is enough to make any contributor or developer familiar with the codebase

**All of the targets were completed during the GSOC period✨**

## ⚒  Setup Instructions and Demo
- It is important to use node.js version 14, check your nodejs version by
```bash
node -v
``` 
- If using nvm, do set the default to 14.
```bash
nvm alias default 14
``` 
- Install the `CodeTour` extension from VsCode extensions

![Codetour extension](https://github.com/user-attachments/assets/06f30109-4818-47c3-a084-70bca9e8dd58)


- if cloned for the repo for the first time, install the node_modules
```bash
yarn
```
and then generate the .tours folder
```bash
yarn tours 
``` 
- The CodeTour Extension searches for a folder with a certain name i.e. `.tours` and all the tours created are stored inside the `.tours` folder in JSON format. and Each file inside the .tours folder contains data about the tour including Line Numbers, file and folder names and explanations, ***To know more about the CodeTour extension visit [here](https://marketplace.visualstudio.com/items?itemName=vsls-contrib.codetour)***

- Starting Tours:- Use `ctrl+shift+p` / `cmd+shift+p` to open all commands and then select the start tour option

https://github.com/user-attachments/assets/d3282488-cac1-4fd3-840f-5fee5c13539a

### 🚢 Tours Available

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

## 🎓 Mentors

I would like to express my heartfelt gratitude to my mentor, Aditya Singh, without whom this journey would not have been this smooth. His unwavering support and guidance helped me grow both professionally and as a person.  We held one productive meeting each week discussing the progress in that week and targets for the next week. We were also connected via chat and call,I can call and chat any time. I am so grateful for the faith and support he showed for me within this GSOC period.


- **Aditya Singh** - [Github](https://github.com/AdityaSingh-02) [LinkedIn](https://www.linkedin.com/in/aditya-singh-76065422b/)

## 🤯 Problems That I Faced During GSOC

### 😕 Understanding Codebase

In order to create or edit any tour, the first requirement was to have a good understanding of the Code and different tech stacks used by rocket.chat, I spent a good amount of time learning about different APIs and methods used in rocket.chat

### ⛑️ Making the tours interactive and fun

Its well known that how interesting the texts are, its very boring to read only texts. I tried spice things up by adding some images but in most of the tours, the content is written like adding an image is unecessarey.


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

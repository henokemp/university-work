# Reflection Paper

## Introduction

This following reflection piece will discuss the project *Feeling the Past*, which I created during the spring semester of 2020. This project was part of the module *History in a Digitized World* (DigiZeit) by Prof. Martin Dusinberre and Daniel McDonald, PhD, tutored by Leyla Feiner. DigiZeit is an exclusive module for students of the Master’s degree *History of the Contemporary World / Zeitgeschichte* at the University of Zürich.

This reflection piece is divided into two parts: one descriptive, another reflective. In the first, smaller part, the process beginning from the first thoughts up to the finished product will be discussed. The second part reflects on this and reviews the digital methods used, as well as the implications on future historical work. 

*Feeling the Past* is an interactive, text-based game in which the player slips into the role of a graduate student in History facing their last year at university. The implied main task at the beginning of the game is finding a research topic for a Master’s thesis. Through lucky circumstances the player begins an internship at a local museum, where they are confronted with a number of realistic tasks revolving around historical objects. By completing these tasks a deeper understanding of how to use objects as historical sources is developed. This understanding is then required for the final task, writing a short research outline based on the different objects the player encountered in the playthrough. 

The game was programmed using the **Marugoto** engine of *Lives in Transit*. It can be played using any web browser on computer. For a better understanding of this reflection piece it is best to recently have played *Feeling the Past*. This can be done on https://livesintransit.org/login. The playtime—depending on the playstyle—ranges between 15 and 30 minutes.

## Descriptive Part

### Idea

The main project idea—even before thinking about creating game—was the asking the question, how to introduce more objects into historical source selection. I began thinking about this question in Summer 2019 during an internship in a museum, where I encountered a large number of fascinating objects and histories but a significant lack of academic writing thereof. Furthermore I observed that in teaching at the University of Zürich there is a very strong focus on textual sources and only a handful of teachers actively bring forth objects.

In my opinion there are two key reasons for this: accessability and the lack of awareness. In comparison to most textual sources, objects are more difficult to represent digitally, impossible to replicate, and in general more challenging to gain historical insights from. Text-based sources are more convenient and therefore will be used more frequently. Additionally—speaking from my own experience—working with objects is only marginally taught in university. So reaching out to collections or museums and using their objects as historical sources is only rarely considered by students.

The first project-idea I considered, focussed on the accessability issue. It tried to re-conceptualize the databases used in collections and museums to pave the way for historians interested in objects. This idea never really went to anything concrete. Acting on Martin Dusinberre's suggestion during one of the first sessions of DigiZeit I then decided to write a chapter in *Lives in Transit*. I was already familiar with the limits and possibilities of the game as I acted as playtester in Summer 2019. This allowed me to quickly start planning the contents of my chapter, using the experiences I made during my internship as model for the game-content. The goal was to allow players to experience the possible benefits of using objects as historical sources themselves instead of an authority **telling** them.

### Workprocess

As I was the first student to write a *Lives in Transit* storyline, there wasn't much introductory content for creating a chapter available. The tutorial—which was still a work-in-progress by at that time—supplied only basic information on how the layouting and formatting worked. Therefore most of the 'learning how the system works' was done autodidactically analysing and editing the public **GitHub repository** of the [*Lives in Transit* demo](https://github.com/uzh/lit-demo). As essentially all the content programming in **Marugoto** is done in JSON—which is easily human readable—understanding the different variables was not difficult. For editing the JSON files I used **Sublime Text 3** and **Sublime Merge** as a Git client.

![01.](https://github.com/henokemp/university-work/blob/master/digizeit-reflection/pictures/i1.png)

**Picture 1:** Example for JSON code, textComponent2.json of page 1.2.0 of *Feeling the Past*

On the projects test-system I was then able to see my edits in effect. *Feeling the Past* utilizes only a smaller part of Marugoto's functionality. Firstly the playtime of my game is simply not long enough to incorporate everything. Secondly the *Lives in Transit* demo acted as a model for *Feeling the Past*, so it mainly uses the same (limited) functionality. Last the preparation time for the DigiZeit project was simply too short to learn the complete functionality of *Lives in Transit*.

After familiarizing myself with the basic workflow of **Marugoto** the next step was to construct my storyline. Martin Dusinberre adviced me—based on his own experience constructing *Plantation Lives*—to draw the story and the pages on a piece of paper. I followed this advice with a digital twist. Using the free open-source prototyping tool **Pencil** I created a UI interface system and a storyline flowchart.

![02.](https://github.com/henokemp/university-work/blob/master/digizeit-reflection/pictures/i2.png)

**Picture 2:** Basic UI of *Feeling the Past*, drawn using **Pencil**.

![03.](https://github.com/henokemp/university-work/blob/master/digizeit-reflection/pictures/i3.png)

**Picture 3:** Story flowchart of *Feeling the Past*, draw using **Pencil**.

The underlying idea of the UI interface system was to have an environmental picture on the left to create the setting of each page and a text module on the right for information exposure and giving tasks. Below these two elements there are the exercise modules and the page transition buttons, which connect one page to another. In the finished game most of pages follow this system, expect a few where additional pictures were added below the environmental picture and exposure text. By keeping a consistent UI interface system throughout the whole game the player quickly learns how to process the information on the page and can focus on the content.

The pictured storyline flowchart is one of the later drafts. The final story structure deviates slightly in the progression and how the tasks are presented by the characters as well as completed by the player. Central to the story already in early drafts were the main four tasks I’ll describe more in depth later. Since the time for creating the game was rather limited I felt like it was important to have a clear idea of the structure as early as possible. Over the course of writing the game I stuck to the above concept for the most part and added only small adjustments for smoothing out the storyline.

The larger part of creating the game was done repeating the following steps:
- Creating new and editing existing JSON files to create the **Marugoto** pages
- Running **maruval** to find any (game breaking) coding mistakes
- Pushing the *Feeling the Past* repository to **GitHub**
- Having Daniel McDonald add the updated repository to the test-system
- Testing the layout and exercises of the game using **Firefox** and **Google Chrome**

One recurring problem in this process posed the importer of**Marugoto**. Originally created to automatically import changes from the different **GitHub** repositories to the *Lives in Transit* test-system, it only worked for the *Plantation Lives* storyline. Changes to *Feeling the Past* therefore had to be imported manually by Daniel McDonald, who was responsible for the technical side of *Lives in Transit*. This created delays between changes to the repository and seeing their effects on the test-system. The solution was pushing a small number of bigger changes instead a large number of smaller ones.

Every picture of *Feeling the Past* except the garden picture in the first two pages were photographed by myself during one day using a **Nikon D750**. The garden picture is open license, therefore I could use it in this project without specifically acquiring the rights for it. While taking the pictures I tried to imitate the perspective of a person standing in front of the characters and objects. The goal was to support the immersiveness of the game by putting the player in the same position as a person confronted with these situations in real life. The pictures were edited using **Gimp**, so that they fit the vertical structure of the UI interface system.

By the fourth of May a closed beta was carried out involving the other students of DigiZeit, Leyla Feiner and Daniel McDonald. Martin Dusinberre did not participate in playtesting to avoid a possible conflict of interest leading both the *Lives in Transit* project and DigiZeit. In case of publication of *Feeling the Past* his feedback could affect the grading for DigiZeit. The closed beta ran for a week and was communicated using the issues page of the DigiZeit's **GitLab** repository. The feedback involved various topics like writing, overall flow of the story, the content and solutions of tasks, and typographical errors. In the following DigiZeit session this feedback was discussed in person using **Microsoft Teams**. In the following week I introduced several changes based on the inputs. 

The last two weeks until the deadline on the 26th of May were then used to refine *Feeling the Past*. I focussed on the writing and ensuring that on the technical side everything was working as intended. During some time in May there was a bug in **Marugoto** present, where the progression criteria of exercises were not working as expected. At first I assumed it was a coding error on my side but after consulting with the *Lives in Transit* team it was confirmed that the bug occured in other storylines as well. The bug was later fixed and on the 26th of May I submitted the finished version of *Feeling the Past*. 

Software  | Description
--- | ---
[Marugoto](https://github.com/uzh/marugoto) | The engine on which *Lives in Transit* runs, created specifically for the project. Utilizes folder hierarchy and JSON files to create webpages which can display multimedia content as well as interactive modules.
[maruval](https://github.com/uzh/marugoto-validator) | A tool written by Daniel McDonald to examine a *Lives in Transit* repository for possible coding errors. Runs from the command line and contains multiple utilities.
[Sublime Text 3](https://www.sublimetext.com/) | Proprietary text editor developed by Sublime HQ. For *Feeling the Past* I used the evaluation version of the software on Ubuntu 18.04 LTS.
[Pencil](https://pencil.evolus.vn/) | Open-source GUI prototyping tool developed by Evolus. 
[GIMP](https://www.gimp.org/) | Open-source image editor developed by The GIMP Development Team.
[Firefox](https://www.mozilla.org/de/firefox/browsers/) | Open-source web browser developed by the Mozilla Foundation.
[Google Chrome](https://www.google.com/chrome/) | Proprietary web browser developed by Google.
[Sublime Merge](https://www.sublimemerge.com/) | Proprietary Git Client developed by Sublime HQ.
[GitHub](https://github.com/) | Company which provides hosting for software development and version control using Git. Subsidiary of Microsoft since 2018. 
[GitLab](https://about.gitlab.com/) | Web-based DevOps tool providing version control using Git on the basis of open-source code. DigiZeit utilized the service via SWITCH—the telecommunication network of Swiss universities—to host the file exchange, written discussion, and student projects.  
[Microsoft Teams](https://www.microsoft.com/de-ch/microsoft-365/microsoft-teams/group-chat-software) | Proprietary communication and collaboration platform developed by Microsoft. 

**Table 1**: Programs used for the project with a short description based on online information by the respective developers. 

### The Four Tasks of the Game 

#### Task 1 (1.2.1)

#### Task 2 (1.3.0)

#### Task 3 (1.4.1-3)

#### Task 4 (1.5.1)
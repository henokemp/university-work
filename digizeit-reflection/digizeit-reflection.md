# Reflection Piece

## Introduction

This following reflection piece will discuss the project *Feeling the Past*, which I created during the spring semester of 2020. This project was part of the module *History in a Digitized World* (DigiZeit) by Prof. Martin Dusinberre and Daniel McDonald, PhD, tutored by Leyla Feiner. DigiZeit is an exclusive module for students of the Master’s degree *History of the Contemporary World / Zeitgeschichte* at the University of Zürich.

This reflection piece is divided into two parts: one descriptive, another reflective. In the first, the process beginning from the first thoughts up to the finished product will be discussed. The second part reflects on this and reviews the digital methods used, as well as the implications on future historical work. 

*Feeling the Past* is an interactive, text-based game in which the player slips into the role of a graduate student in History facing their last year at university. The implied main task at the beginning of the game is finding a research topic for a Master’s thesis. Through lucky circumstances the player begins an internship at a local museum, where they are confronted with a number of realistic tasks revolving around historical objects. By completing these tasks a deeper understanding of how to use objects as historical sources is developed. This understanding is then required for the final task: writing a short research outline based on the different objects the player encountered in the play-through. 

The game was programmed using the **Marugoto** engine of game-project*Lives in Transit* by Martin Dusinberre and was published in the initial release. It can be played using any web browser on computer. For a better understanding of this reflection piece it is best to recently have played *Feeling the Past*. This can be done on https://livesintransit.org/login. The playtime—depending on the play-style—ranges between 15 and 30 minutes and can be interrupted as well as resumed at any point.

## Descriptive Part

### Idea

The main project idea—even before thinking about creating game—was the asking the question, how to introduce more objects into historical source selection. I began thinking about this question in Summer 2019 during an internship at the *Historisches und Völkerkundemuseum St.Gallen* (HVM), where I encountered a large number of fascinating objects and histories but a significant lack of academic writing thereof. Furthermore I observed that in teaching at the University of Zürich there is a very strong focus on textual sources and only a handful of teachers actively including objects.

In my opinion there are two key reasons for this: accessibility and the lack of awareness. In comparison to most textual sources, objects are more difficult to represent digitally, impossible to replicate, and in general more challenging to gain historical insights from. Text-based sources are more convenient and therefore will be used more frequently. Additionally—speaking from my own experience—working with objects is only marginally taught in university. So reaching out to collections or museums and using their objects as historical sources is only rarely considered by students, who later become historical researchers.

The first project-idea I considered focused on the accessibility issue. It tried to re-conceptualize the databases used in collections and museums to pave the way for historians interested in objects. This idea never really went to anything concrete. Acting on Martin Dusinberre's suggestion during one of the first sessions of DigiZeit, I then decided to write a chapter in *Lives in Transit*. I was already familiar with the limits and possibilities of the game as I was a play-tester in the summer the previous year. This allowed me to quickly start planning the contents of my chapter, using the experiences I made during my internship as model for the game-content. The goal was to allow players to experience the possible benefits of using objects as historical sources themselves instead of an authority **telling** them.

### Work-process

As I was the first student to write a *Lives in Transit* storyline, there wasn't much introductory content availabe on how to create a chapter. The tutorial—which was still a work-in-progress at that time—supplied only basic information on how the layouting and formatting worked. Therefore most of the *learning how the system works* was done auto-didactically analysing and editing the public **GitHub repository** of the [*Lives in Transit*-demo](https://github.com/uzh/lit-demo). Essentially all the content programming in **Marugoto** is done in the easily human readable programming langue JSON, so understanding the different variables was not difficult. For editing the JSON files I used **Sublime Text 3** and **Sublime Merge** as a Git client. The repository was hosted on **GitHub**.

![01.](https://github.com/henokemp/university-work/blob/master/digizeit-reflection/pictures/i1.png)

**Picture 1:** Example for JSON code in **Sublime Text 3**, textComponent2.json of page 1.2.0 of *Feeling the Past*

On the *Lives in Transit's* test-system I was then able to see my edits in effect. *Feeling the Past* utilizes only a smaller part of **Marugoto's** functionality. The reasons for this are that the playtime of my game is simply not long enough to incorporate everything. Secondly, the *Lives in Transit*-demo acted as a model for *Feeling the Past*, so it mainly uses the same (limited) functionality. Lastly, the preparation time for the DigiZeit project was simply too short to learn the complete functionality of *Lives in Transit*.

After familiarizing myself with the basic work-flow of **Marugoto** learning from the existing repositories the next step was to construct my storyline. Martin Dusinberre advised me—based on his own experience constructing *Plantation Lives*—to draw the story and the individual pages on a piece of paper. I followed this advice with a digital twist. Using the free open-source prototyping tool **Pencil** I created a UI interface system and a storyline flowchart as PDFs.

![02.](https://github.com/henokemp/university-work/blob/master/digizeit-reflection/pictures/i2.png)

**Picture 2:** Basic UI of *Feeling the Past*, drawn using **Pencil**.

![03.](https://github.com/henokemp/university-work/blob/master/digizeit-reflection/pictures/i3.png)

**Picture 3:** Story flowchart of *Feeling the Past*, draw using **Pencil**.

The underlying idea of the UI interface system was to have an environmental picture on the left to create the setting of each page and a text module on the right for information exposure as well as giving tasks. Below these two elements there are the exercise modules and the page transition buttons, which connect one page to another. In the finished game most of pages follow this system, expect a few where additional pictures were added below the environmental picture and the exposure text. By keeping a consistent UI interface system throughout the whole game the player quickly learns how to process the information on a page and can focus on the content.

The pictured storyline flowchart is one of the later drafts. The final story structure deviates slightly in the progression and how the tasks are presented by the characters as well as completed by the player. Central to the story already in early drafts were the main four tasks I’ll describe more in depth later. Since the time for creating the game was rather limited I felt like it was important to have a clear idea of the structure as early as possible. Over the course of writing the game I stuck to the above concept for the most part and added only small adjustments for smoothing out the storyline.

The larger part of creating the game was done repeating the following steps:
- Creating new and editing existing JSON files to create the **Marugoto** pages
- Running **maruval** to find any (game breaking) coding mistakes
- Pushing the *Feeling the Past* repository to **GitHub**
- Having Daniel McDonald add the updated repository to the test-system
- Testing the layout and exercises of the game using **Firefox** and **Google Chrome**

One recurring problem in this process posed the importer of **Marugoto**. Originally created to automatically import changes from the different **GitHub** repositories to the *Lives in Transit* test-system, it only worked for the *Plantation Lives* storyline. Changes to *Feeling the Past* therefore had to be imported manually by Daniel McDonald, who was responsible for the technical side of *Lives in Transit*. This created delays between changes to the repository and seeing their effects on the test-system. The solution was pushing a small number of bigger changes instead a large number of smaller ones.

Every picture of *Feeling the Past* except the garden picture in the first two pages were photographed by myself during one day using a **Nikon D750**. As setting acted the HVM and all the characters pictured in the game are employees of the museum. The garden picture is open license, therefore I could use it in this project without specifically acquiring the rights for it. While taking the pictures I tried to imitate the perspective of a person standing in front of the characters and objects. The goal was to support the immersiveness of the game by putting the player in the same position as a person confronted with these situations in real life. The pictures were edited using **Gimp**, so that they fit the vertical structure of the UI interface system.

By the fourth of May a closed beta was carried out involving the other students of DigiZeit, Leyla Feiner and Daniel McDonald. Martin Dusinberre did not participate in play-testing to avoid a possible conflict of interest leading both the *Lives in Transit* project and DigiZeit. In case of publication of *Feeling the Past* his feedback could affect the grading for DigiZeit. The closed beta ran for a week and was communicated using the issues page of the DigiZeit's **GitLab** repository. The feedback involved various topics like writing, overall flow of the story, the content and solutions of tasks, and typographical errors. In the following DigiZeit session this feedback was discussed in person using **Microsoft Teams**. In the following week I introduced several changes to the game based on the inputs. 

The last two weeks until the deadline on the 26th of May were then used to refine *Feeling the Past*. I focused on writing and ensuring that on the technical side everything was working as intended. During some time in May there was a bug in **Marugoto** present, where the progression criteria of exercises were not working as expected. At first I assumed it was a coding error on my side but after consulting with the *Lives in Transit* team it was confirmed that the bug occurred in other story-lines as well. The bug was later fixed and on the 26th of May I submitted the finished version of *Feeling the Past*. 

Software  | Description
--- | ---
[Marugoto](https://github.com/uzh/marugoto) | The engine on which *Lives in Transit* runs, created specifically for the project. Utilizes folder hierarchy and JSON files to create web-pages which can display multimedia content as well as interactive modules.
[maruval](https://github.com/uzh/marugoto-validator) | A tool written by Daniel McDonald to examine a *Lives in Transit* repository for possible coding errors. Runs from the command line and contains multiple utilities.
[Sublime Text 3](https://www.sublimetext.com/) | Proprietary text editor developed by Sublime HQ. For *Feeling the Past* I used the evaluation version on Ubuntu 18.04 LTS.
[Pencil](https://pencil.evolus.vn/) | Open-source GUI prototyping tool developed by Evolus. 
[GIMP](https://www.gimp.org/) | Open-source image editor developed by The GIMP Development Team.
[Firefox](https://www.mozilla.org/de/firefox/browsers/) | Open-source web browser developed by the Mozilla Foundation.
[Google Chrome](https://www.google.com/chrome/) | Proprietary web browser developed by Google.
[Sublime Merge](https://www.sublimemerge.com/) | Proprietary Git client developed by Sublime HQ.
[GitHub](https://github.com/) | Company which provides hosting for software development and version control using Git. Subsidiary of Microsoft since 2018. 
[GitLab](https://about.gitlab.com/) | Web-based DevOps tool providing version control using Git on the basis of open-source code. DigiZeit utilized the service via SWITCH—the telecommunication network of Swiss universities—to host the file exchange, written discussion, and student projects.

**Table 1**: Programs used for the project with a short description based on online information by the respective developers. 

### The Four Tasks of the Game 

All the tasks in the game are based on real-life situations I encountered during my internship at the HVM. All the objects in the game are part of the historical collection of the HVM and I'm very grateful to the collection manager of the museum, Achim Schäfer, for allowing me to use them in the game. 

#### Task 1 (Page 1.2.1)

The first task of the game is to write a descriptive paragraph of a coffee-maker. The player receives four pictures from different angles and some information from the collection manager. They are also invited to do some research using the Internet. The minimum amount of character the player must write is 300. Once the player proceeds to the next page, their description—as with all the exercises in the game—is saved in the notebook. 

The goal of this exercise is to give the player a gentle introduction into asking themselves, what information they can get out of an object. This exercise—similar to the other ones—is posed intentionally open, so the player can interpret the task in relation to their own interests. 300 characters can both be very little or a lot of information, depending if the player utilizes bullet points or complete sentences, so it will vary in different play-throughs.

#### Task 2 (Page 1.3.0)

The second task approaches the question of objects and information from the other side. It's modeled after the real life problem of sometimes not knowing which objects are connected to which data-sets. The player is tasked with finding the correct corresponding object to a data-set. Additionally the player is given a picture of four different mortars, out of which they have to choose the correct one. The data-set contains a visual description, from which the player has to conclude the correct mortar.

In this exercise the player is confronted with the question what information a data-set can and cannot give. In the game the choice the player makes out of the four different mortars makes no difference to the later stages of the game. This initially might seem like laziness but there is a underlying thought. The task represents the real-life problem of most times simply not having a confirmation. There often is no way to unambiguously know if a object is connected to a data-set.

#### Task 3 (Pages 1.4.1—3)

The centerpiece of *Feeling the Past* is the third task of the game. Here the player is given the choice between three different objects with three different kinds of informations. The first object, an apothecary scale, comes with both a complete data-set and multiple pictures. This simulates being in a collection and standing right in front of the desired object. Basically the optimal case if someone is interested in using an object as a historical source. The second choice is missing, well, the object, a ventilator. The player only receives a data-set and a rather deficient picture. This is once again modeled after a real life problem, which is sometimes not knowing the exact location of an object and therefore having to deal with incomplete or bad information. The last object is a straight-jacket. The data-set is a reconceptualized version of the classic data-set seen in the upper two choices. It's a text written by myself in the style of Neil MacGregor's *A History of the World in 100 Objects*, based both on the original data-set of the HVM and my personal impressions of the object. This was an attempt to rethink how information in collections is stored and how it might be possible to facilitate the work of historians interested in objects. 

#### Task 4 (Page 1.5.1)

The last task of the game was already teased in the very first pages: writing a short research outline based on the objects the player encountered during their first day at the museum. Here the player is asked to explicitly think about how they might use the objects in their own research. The goal was to set an overarching goal very early in the game and come back to it at the end to give the story a basic structure.

## Reflective Part

### Work-process

My project was significantly shaped by working with an existing one. This both had advantages and disadvantages. For one, creating something as labourious as a computer game—something I surely wouldn't have been able to complete from scratch in roughly three months—was made possible by utilizing an existing framework. This meant adjusting to the limits of the project. In my case this didn't cause any conflicts between what I wanted to do and what was possible, but it surely influenced how I decided to design my storyline. The tasks are based on the exercises I encountered in the *Lives in Transit*-demo and what I remembered of the playtest of *Plantation Lives*. If I wanted for example the player to be able to virtually pick up an object in a 3D environment during an exercise and freely rotate it, this wouldn't have been possible.

Working with a project which used software specifically developed for it meant that if I encountered an issue or didn't understand something, I couldn't simply use Google to find a solution. While I was learning how to use **Marugoto**, the documentation was still a work-in-progress. So I either had to solve the issue by trial and error or consult someone more familiar with the project. This sometimes led to delays working on a certain page. Technical difficulties probably are a reality for all digital projects, but without a documentation troubleshooting is siginificantly more difficult. An unfinished project also meant suddenly dealing with new problems occasionally. In the case of *Lives in Transit* these were the disfunctional importer and the bug during May. As a writer in the project I contributed to the solution by reporting unexpected behaviour.  

Martin Dusinberre's advice on on drawing up the page-design and storyline facilitated both creating the pages and communicating what I wanted to achieve. It wasn't really necessary to use a prototyping tool to do this, but being able to directly output a PDF and making small changes without having to copy everything by hand was convenient. 

Learning how to use JSON was easy for me, as I had engaged with code before creating *Feeling the Past*. The easily human-readable JSON code also made learning how to use new modules simple. The folder hierarchy took a little more time, but by imitating the existing repositories it was possible to create a working version without completely understanding the mechanics behind it. Basic Git skills were taught in the first few session of DigiZeit and as I was mostly the only person pushing to the *Feeling the Past*-repository, no issues arose here. On the test-system the most difficult issues were of graphical nature, like ensuring that four pictures were properly aligned. 

The closed beta proved to be really useful for finding out how other people experienced the progression of the story as well as the exercises, the main part of the game. At the same time they were roughly the correct target group, something I will discuss in detail below. The various feedback definitely helped to improve the game and notice things which I overlooked like a not yet translated data-set or a word choice which didn't fit the character. The feedback was essential in shaping some parts of the final game.

### Tools

In the following section I will review the tools I used creating *Feeling the Past*. This discussion won't go into too much depth, as I simply don't have the expertise to critique these tools other than how well they achieved what I intended to use them for in my project.

**Marugoto** proved to be a good choice for creating a piece of interactive fiction with an educational intend. During the last session of DigiZeit I was asked if I had preferred something more complex like a 3D based engine. In my opinion this would have caused the game to be more focused on the experience of being in the museum instead of the exercises and what can be learned by them. Additionally the workload of creating a 3D game—even with a existing environment and presets—would have meant less freedom and less time to conceptually work on the game. Using a text-based engine and static pages allows the player to focus on the tasks, which were for my purposes the most important part of the game. My familiarity with *Lives in Transit* and its limits and possibilities before beginning the project helped me to quickly plan the contents of the game. There is a fair bit of functionality of **Marugoto** I didn't explore in my game. The main reason for this is the lack of time and partially a lack of awareness. The learning curve of Marugoto was steep, having to understand both how the folder hierarchy relates to the different pages displayed and what each variable controls. Once understood though, the work becomes fluent and quite direct, as the knowledge of one functionality facilitates the learning of the next. I think a person without much coding experience will be able to pick it up in a few days, even more so now that there exists a tutorial. 

**maruval** was an essential part of working with *Lives in Transit*. For one, dealing with the disfunctional importer was somewhat facilitated by first testing if there were any issues with the code. Secondly, having a tool to check the code of someone learning the engine by themselves was helpful getting feedback without having to consult someone with in depth experience of **Marugoto**. My own learning experience was accelerated by using **maruval**.

The text-editor I used, **Sublime Text 3**, and the version control software **Sublime Merge** proved to be good choices. The most useful feature of **Sublime Text 3** was the highlighting of the different parts of the JSON code. This facilitated my understanding of exisiting and new code as well as occasional mistakes. It's also pleasant to work with as there are very few distractions in the UI. Upon recommendation of Daniel McDonald I installed packages which further streamlined the workprocess, such as a package to automatically check if there's a newline at the end of code and if this is not the case to add one. **Sublime Merge's** most useful feature was displaying the changes to files in red and green, so proofreading any changes before pushing was quick and easy. For a solo project like mine, having the graphical representation of branches and forks of **Sublime Merge** wasn't very important, but I imagine for a bigger project it would proof useful.

The graphical software I used, **Pencil** and **Gimp**, both weren't used even remotely close to their full potential. This of course isn't a bad thing. With both programs I needed a moment to orientate myself, but afterwards I was able to quickly achieve what I wanted to do.

Both **Firefox** and **Google Chrome** were used to test *Feeling the Past*. Using two browsers wasn't really a deliberate choice, as I have been using **Google Chrome** on my desktop for while and started using **Firefox** once I switched to Linux on my laptop and stared trying to use more open-source software. As far as my knowledge of web-development goes, testing a website in multiple browsers is common practice because they sometimes differ in how they display content. 

The two content hosts used, **GitHub** and **GitLab**, were necessities for connecting the repository of *Feeling the Past* with the test-system and communicating with the other students of DigiZeit. The Git functionality made it easy for other people to take a look at my project in a unfinished state and make suggestions. In my opinion it could also be used for co-writing historical papers and other tasks, which have nothing to do with software development. I feel like the most important feature is having a master file, to which all involved people can make contributions to in form of pull requests, but at the same time allowing a clear hierarchy of who accepts and rejects these requests and who doesn't. This functionality could improve many existing workflows, which still rely on editing one file on a central server. One key issue here is that there can only one person who edits the file at the time which leads to people making copies which leads to different version of the same file floating around. This source of problem could be solved with using Git.

### Tasks

The discussion of the tasks will be based on the feedback of the play-test during May and my own impressions of how the tasks turned out in the finished product.

The first task is in my eyes a good introduction into both how the following exercises are designed and how a historian can get information from an object. In the close beta feedback the task was not mentioned, which I interpret as a good sign. The task achieves what I created it for. 

The most questionable task of the game is probably the second one. In the submitted version for DigiZeit, in which there is no correct answer given after the exercise, the message of the task is probably too subtle for the player to notice. Therefore the exercise only works as a way of reversing the first one and having the player think based on a data-set. In the published version the collection manager, Frederic, later tells the player that he found a inventory number and identified the right mortar. Here the original message of sometimes not knowing for sure which object fits to which data-set also is not conveyed. I'm not sure how I could communicate this idea without a character directly saying it to the player. 

The third exercise felt successful at exposing players to different kinds of information. The apothecary scale, the most complete set of information, simulates as close as possible, using **Marugoto**, physically standing in front of an object and using it as a source. If the engine included three-dimensional support this would of course improve the experience. I feel like the scale is an interesting object to examine, as it allows a number of different historical perspectives. It's a visually appealing object so having multiple pictures of it has a greater effect than the ventilator or the straight-jacket. 



### Target Group

The intended target group of *Feeling the Past* was university students doing their Bachelor's or Master's degree. I wanted to make an impact on the source selection in academic history. Because I'm only familiar with being a historian studying on Bachelor and Master level and wanted the game to be relatable, I chose a Master's student as the playable character. The story therefore assumes that the player has at least some knowledge of source analysis. During the feedback discussion in the last session of DigiZeit the question was raised, if the game would also be applicable for other people, for example high school students or museum visitors. The game of course is playable by people without prior knowledge of historical work and source selection. But the effect would not be the same. For museum visitors the game could present an insight behind the scenes of a museum. For high school student the game could also show what it feels like doing an internship at a museum or studying history. But for both groups the originally intended goal would not be met. 

Martin Dusinberre mentioned that there is a demand for new ways of teaching history for high school students. **Marugoto** could definitely be a way of conveying historical ideas on high school level. But I feel like the story has to be specifically written for the target group to be most effective. If I were to rewrite *Feeling the Past* for high school students I would change the main character to someone who has just finished their school years and is interested in history. The tasks would be more basic at the beginning, but could definitely become more complex depending on the length of the game. This way the player could become familiar with the work inside a museum and of a historian. (reference to paper about relatability in educational games?)

Another suggestion was playing the game from inside the museum. For *Feeling the Past* in the present state the added benefit of that wouldn't be big. But as a general idea this could offer a real addition to the classic museum experience. A rewrite could involve having the player physically finding the object in the collection and inspect it in person. This could potentially strengthen the argument that there is something to gain from using objects as historical sources. The play-through would have to be supervised if the players are dealing with real objects, but it would improve both the experience of being in the museum and learning about objects as historical sources. (reference to paper about games in the museum?)

### Games in Academic History

### Objects in Academic History

## Conclusion



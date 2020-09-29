## ***Feeling the Past***: How a interactive text-based educational game could influence historical source selection.

### Introduction

This reflection piece discusses the project *Feeling the Past*, which I created during the spring semester of 2020. The project was part of the module *History in a Digitized World* (DigiZeit) by Martin Dusinberre and Daniel McDonald, tutored by Leyla Feiner. DigiZeit is an exclusive module for students of the Master degree *History of the Contemporary World / Zeitgeschichte* at the University of Zürich.

*Feeling the Past* is an interactive, text-based educational game in which the player slips into the role of a graduate student in History facing their last year at university. The implied main task at the beginning of the game is finding a research topic for a Master thesis. Through lucky circumstances the player begins an internship at a local museum during which they are confronted with a number of realistic tasks revolving around historical objects. By completing these tasks, the player develops an understanding of how objects can be used as historical sources. The new-found knowledge is then required for the final task: writing a short research outline based on the objects the player encountered during the play-through. 

The game was programmed using the **Marugoto** engine of *Lives in Transit* by Martin Dusinberre et al. and was published in the initial release of the game project on the 6th of October 2020. It can be played using any web browser on computer. Mobile browsers are currently not supported. In order to better follow this reflection, it is recommended to first play *Feeling the Past*. This can be done on https://livesintransit.org/login. The playtime—depending on play-style—ranges between 15 and 30 minutes and can be interrupted as well as resumed at any point.

The reflection piece is divided into two parts: one descriptive, another reflective. In the first part, the thought and creative process will be illustrated, describing the practical aspects of game-creation. The second half reviews working on *Lives in Transit*, the digital tools used, the contents of the game, the target group, and the implications for future historical work, by using literature. In this paper I want to illustrate how *Feeling the Past* tries to influence the source selection of historians by confronting them with objects and allowing them to interpret these challenges based on their own interests. Discovering how objects might support their work on their own can possibly have an impact on the players considering objects more closely in future work. 

### Objects in History and Game Development

#### Why is there only a small number of objects in historical source selection?

My initial idea—even before thinking about creating a game—was asking the question of how to introduce more objects into the source selection of historians. I started thinking about this in Summer 2019 during an internship at the *Historisches und Völkerkundemuseum St.Gallen* (HVM), where I encountered a large number of fascinating objects and histories, but a significant lack of academic writing thereof. I furthermore observed that the teaching at the University of Zürich focuses strongly on textual sources and only a handful of lecturers actively instruct students how to work with objects. Objects often tell different stories or stories closer to the people of the past. There is an important part of history lost when disregarding them as historical sources and a lot of work can be enriched and supplemented considering them closely. Because I am passionate about this issue I wanted to create a project which tackles this problem. 

There are two key reasons for the current situation: accessibility, and the lack of awareness. In comparison to most textual sources, objects are more difficult to represent digitally, almost impossible to replicate, and in general more challenging to gain historical insights from. Text-based sources are more convenient and will therefore be used more frequently. As already mentioned—speaking from my own experience—working with objects is only marginally taught in university. Thus reaching out to collections or museums and using their objects as sources is only rarely considered by students, who later become researchers. The goal of *Feeling the Past* is to allow players to experience the possible benefits of using objects as historical sources for themselves instead of an authority telling them, similar to my own insights working closely with objects in the museum during my internship. This way motivating them to consider objects as possible sources in future work.

#### Process between March and May 2020

As I was the first student to write a *Lives in Transit* storyline, there was not much introductory content available on how to create a chapter. The tutorial—which was still a work-in-progress at that time—supplied only basic information on how the page layouting and formatting worked. Therefore, most of the familiarizing was done auto-didactically, analysing and editing a copy of the public **GitHub** repository of the [*Lives in Transit* demo](https://github.com/uzh/lit-demo). Essentially all the content programming in **Marugoto** is done in the easily human readable programming language JSON (Picture 1). For editing the JSON I used **Sublime Text 3** and **Sublime Merge** as a Git client. The repository was hosted on **GitHub**, from which **Marugoto** pulls the contents of the pages and the structure of each storyline. In Table 1 below there is a comprehensive of software I used while creating *Feeling the Past*.

![01.](https://github.com/henokemp/university-work/blob/master/digizeit-reflection/pictures/i1.png)

**Picture 1:** Example for JSON code in **Sublime Text 3**, textComponent2.json of page 1.2.0 of *Feeling the Past*.

The larger part of effectively creating the game was done repeating the following steps:
- Creating new and editing existing JSON files to create the **Marugoto** pages
- Running **maruval** to find any (functionally disruptive) coding mistakes
- Pushing the *Feeling the Past* repository to **GitHub**
- Having Daniel McDonald add the updated repository to the test system
- Testing the layout and functionality of the game using **Firefox** and **Google Chrome**

The following two pictures illustrate the the design drafts I created before writing the pages. The first being the user interface concept I followed throughout the whole game (Picture 2) and the second being an advanced draft of the story outline (Picture 3). Drawing up my ideas was very important for translating them into a more abstract form like JSON code. 

![02.](https://github.com/henokemp/university-work/blob/master/digizeit-reflection/pictures/i2.png)

**Picture 2:** Basic UI of *Feeling the Past*, drawn using **Pencil**.

![03.](https://github.com/henokemp/university-work/blob/master/digizeit-reflection/pictures/i3.png)

**Picture 3:** Story flowchart of *Feeling the Past*, draw using **Pencil**.

By the fourth of May a closed beta was carried out, involving the other students of DigiZeit, Leyla Feiner and Daniel McDonald. Martin Dusinberre did not participate in play testing to avoid a possible conflict of interest, leading both the *Lives in Transit* project and DigiZeit. In case of publication of *Feeling the Past*, his feedback could affect the grading for DigiZeit. The closed beta ran for a week and was communicated using the issues page of the DigiZeit **GitLab** repository. The feedback involved various topics like writing, overall flow of the story, the content and solutions of tasks, and typographical errors. In the following DigiZeit session this feedback was discussed using **Microsoft Teams**.

Software  | Description
--- | ---
[maruval](https://github.com/uzh/marugoto-validator) | A tool written by Daniel McDonald to examine a *Lives in Transit* repository for possible coding errors. Runs from the command line and contains multiple utilities.
[Marugoto](https://github.com/uzh/marugoto) | The engine on which *Lives in Transit* runs, created specifically for the project. Utilizes folder hierarchy and JSON files to create web-pages which can display multimedia content as well as interactive modules.
[Sublime Text 3](https://www.sublimetext.com/) | Proprietary text editor developed by Sublime HQ. For *Feeling the Past* I used the evaluation version on Ubuntu 18.04 LTS.
[Pencil](https://pencil.evolus.vn/) | Open-source GUI prototyping tool developed by Evolus. 
[Firefox](https://www.mozilla.org/de/firefox/browsers/) | Open-source web browser developed by the Mozilla Foundation.
[Google Chrome](https://www.google.com/chrome/) | Proprietary web browser developed by Google.
[Sublime Merge](https://www.sublimemerge.com/) | Proprietary Git client developed by Sublime HQ.
[GitHub](https://github.com/) | Company which provides hosting for software development and version control using Git. Subsidiary of Microsoft since 2018. 
[GitLab](https://about.gitlab.com/) | Web-based DevOps tool providing version control using Git on the basis of open-source code. DigiZeit utilized the service via SWITCH, the telecommunication network of Swiss universities, to host the file exchange, written discussion, and student projects.

**Table 1**: Programs used for the project with a short description based on online information by the respective developers. 

#### The Four Tasks of the Game 

All the tasks in the game except the last one are based on real-life situations I encountered during my internship at the HVM. All the objects in the game are part of the historical collection of the HVM. 

##### Introductory Task (Page 1.2.1)

The first task of the game is to write a descriptive paragraph for the data-set of a coffee-maker. The player receives four pictures from multiple different angles and some information from the collection manager. The minimum amount of characters the player must write is 300. Once the player proceeds to the next page, their description—as is the case with all the exercises in the game—is saved in the notebook. 

The goal of this exercise is to give the player a gentle introduction into asking themselves what information they can get out of the appearance an object. This exercise—similarly to the following ones—is posed intentionally open, so the player can interpret the task in relation to their own interests.

##### Information Reversal (Page 1.3.0)

The second task approaches the question of objects and information from the other side. The player is tasked with finding the correct object which corresponds to a data-set. The player is given a picture of four different mortars, out of which they have to choose the correct one. The data-set contains a visual description, from which the player has to conclude the correct mortar.

In this exercise the player is confronted with the question what information a conventional data-set can and cannot give. The in-game choice made by the player has no impact on the later stages of the game. The task represents the real-life problem of not knowing definitely if the correct choice was made. There often is no way to unambiguously know if a specific object is connected to a specific data-set.

##### Three different kinds of information (Pages 1.4.1—3)

The centerpiece of *Feeling the Past* is the third task of the game: The player has the choice between three different objects with different kinds of information. With every choice the player is simply asked to think freely think about the object and take notes. The first object, an apothecary scale, is displayed with both a complete data-set and multiple pictures. This simulates being in a collection and standing right in front of the desired object, the optimal case. The second choice is missing the object, a ventilator. The player only receives a data-set and a deficient picture. This exercise is once again modeled after a real life problem, having to deal with incomplete or bad information. The last object is a straitjacket. The data-set is a reconceptualized version of the conventional data-set seen in the upper two choices. It is a text written by myself in the style of Neil MacGregor's *A History of the World in 100 Objects*, based both on the original data-set of the HVM and my personal impressions of the object. This was an attempt to rethink how information is stored in collections, and how it might be possible to facilitate the work of historians interested in objects by changing how and which information is collected. 

##### The Research Outline (Page 1.5.1)

The last task of the game was already teased in the very first pages: writing a short research outline based on the objects the player encountered during their first day at the museum. Here the player is explicitly asked to think about how they might use the objects in their own research. The goal was to set an overarching goal very early in the game, and come back to it at the end to give the story structure as well as promote contextualizing the objects in the player's own interest.

### Can a computer game introduce objects into historical source selection?

#### Working with ***Lives in Transit***

Working with an existing project had both advantages and disadvantages. For one, creating something as labourious as a computer game—something I definitely would not have been able to complete from scratch in roughly three months—was made possible by utilizing an existing framework. In my case, this did not cause any conflicts between what I wanted to do and what was possible, but it surely influenced how I decided to design my storyline. The tasks are based on the exercises I encountered in the *Lives in Transit* demo and what I remembered of the playtest of *Plantation Lives*. If I had wanted for the player to be able to virtually pick up an object in a 3D environment during an exercise and freely rotate it, this would not have been possible as **Marugoto** does not support 3D modules.

Working with project specific software meant that if I encountered an issue or did not understand something, I could not simply use Google to find a solution. While I was learning how to use **Marugoto**, the documentation was still a work-in-progress. Therefore, I either had to solve the issue by trial and error or consult someone more familiar with the project. This sometimes led to delays working on a certain pages. An unfinished project also meant occasionally dealing with new problems. In the case of *Lives in Transit* these were the disfunctional importer and the bug during May. As a writer in the project I contributed to the solutions by reporting unexpected behaviour.  

The closed beta proved to be really useful for finding out how other people experienced the progression of the story as well as the exercises, the main part of the game. At the same time they were roughly the target group, something I will discuss below. The various feedback definitely helped to improving the game and noticing things which I overlooked like a not yet translated data-set or a word choice which did not fit the character. It was essential in shaping some parts of the final game.

#### The Tools of the Craftsman

In the following section I will review the most important tools I used while creating *Feeling the Past*. This discussion will not go into too much depth, as I simply do not have the expertise to critique these tools other than how well they achieved what I intended to use them for in my project.

**Marugoto** proved to be a good authoring tool for creating a piece of interactive fiction with an educational intent. Similar to **uAdventure** by Manuel et al., it allowed someone without a lot of technical experience to create a fully functional game by mainly using examples and a manual to learn without a great amount of specific training (Pérez-Colado et al., 2019). At the same time, the authors also found that in teaching a workshop-based approach to game-making allowed them to explore more advanced goals in smaller periods compared to a self-taught approach while possibly leading to "false successes" (p. 40). During the last session of DigiZeit I was asked if I had preferred something more complex like a 3D based engine. In my opinion this would have caused the game to be more focused on the experience of *being* in the museum instead of the exercises and what can be learned by them. Additionally the workload of creating a 3D game—even with a existing engine and presets—would have meant less freedom and less time to conceptually work on the game. Using a text-based engine and static pages allows the player to focus on the tasks, which, for me, were the most important part. My familiarity with *Lives in Transit* and its limits and possibilities before beginning the project helped me to quickly plan the contents of the game. There is a fair bit of functionality of **Marugoto** I did not explore in my game. The main reason for this is the lack of time and partially a lack of awareness. The learning curve of **Marugoto** was steep, having to understand both how the folder hierarchy relates to the different pages displayed and what each variable controls. Once understood though, the work becomes fluent, as the knowledge of one functionality facilitates the learning of the next. I think a person without much technical experience will be able to pick it up in a few days, even more so now that there exists a tutorial and a documentation.

**Sublime Text 3** and the version control software **Sublime Merge** proved to be good choices. The most useful feature of **Sublime Text 3** was the syntax highlighting. It facilitated the understanding of exisiting and new code as well as occasional mistakes. Upon recommendation of Daniel McDonald I installed packages, add-ons for **Sublime Text 3**, which further streamlined the workprocess, such as a package to automatically check if there is a newline at the end of code and add one, if it is absent. The most useful feature of **Sublime Merge** was displaying the changes to files in red and green, so proofreading changes before pushing was quick and easy. For a solo project like mine, having the extensive graphical representation of branches and forks of **Sublime Merge** was not too important, but I imagine for a bigger project it would prove useful.

The two content hosts used, **GitHub** and **GitLab**, were necessities for connecting the repository of *Feeling the Past* with the test system and communicating with the other students of DigiZeit. The Git functionality made it easy for other people to take a look at my project in an unfinished state and make suggestions. In my opinion it could also be used for co-writing historical papers and other tasks unrelated to software development. I feel like the most important feature is having a master file, which all involved people can contribute to in form of pull requests, but at the same time allowing a clear hierarchy of who accepts and rejects these requests and who does not. This functionality could improve many existing workflows, which still rely on editing one file on a central server. One key issue here is that there can only one person who edits the file at the time which leads to people making copies therefore having multiple different versions of the same file floating around. This problem can be solved with by Git.

#### Practical Tasks and Unmet Goals

The discussion of the tasks will be based on the feedback of the play-test during May and my own impressions of how the tasks turned out in the finished product.

The first task is, in my eyes, a good introduction into both how the following exercises are designed and how a historian can get information from an object. In the closed beta the task was not mentioned, which I interpret as a good sign. The task achieves what I created it for. 

The most questionable task of the game is most likely the second one. In the submitted version for DigiZeit, in which the correct answer is never revealed, the message of the task may be too subtle for the player to notice. The exercise therefore only works as a way of reversing the first one and having the player think based on a data-set. In the published version the collection manager, Frederic, later tells the player that he found the inventory number on a mortar and identified the right one. Here the intended message of sometimes not knowing for sure which object belongs to which data-set is also not conveyed. I am not sure how I could communicate this idea of uncertainty without a character directly telling the player. 

The third exercise was in my opinion successful at exposing players to different kinds of information and confronting them with real situations they might encounter if they choose work with objects. The apothecary scale, the most complete set of information, simulates as close as possible, using **Marugoto**, physically standing in front of an object and using it as a source. I feel like the scale is an interesting object to examine, as it allows a number of different historical perspectives. It is a visually appealing object thus having multiple pictures of it has a greater effect than the ventilator or the straitjacket. The limitations for the players working with the ventilator already showed up in the play-test, in which the question came up, what to do with it and how to work around the object's lack of physical appearance besides a rather bad picture. In that sense the exercise was successful in confronting the players with the correct issue while possibly overwhelming them. The reconceptualized data-set felt like a nice idea, but if I had more time I would have liked to develop it further. I think an clear argument can be made for how it might be beneficial for historians to store information in data-bases differently. But this aspect was not of high priority for the DigiZeit version of *Feeling the Past*, and the time was simply limited.

The last task ties the beginning and the end together nicely. Some of the play-testers felt like the game ended rather abruptly and would have liked a final reflection of the main character. In achieving the learning effect I aimed for, this ending is more appropriate, as the players can decide for themselves how they want to think about their first day in the museum and what insights they have gained. A pre-made reflection would have enforced a kind of authoritative teaching on what the players are supposed to take home from the game instead of having them make a conclusion themselves. 

#### Who is the Target Group?

The intended target group of *Feeling the Past* are university students doing their bachelor's or master's degree. I wanted to make an impact on the source selection in academic history, so apprentice scholars are an appropriate target group. Because I am only familiar with studying history on a bachelor's and master's level and wanted game to be relatable, I chose a Master student as the playable character instead for example a PhD student like in *Plantation Lives*. The story therefore assumes that the player has at least some knowledge of source analysis. During the feedback discussion in the last session of DigiZeit, the question was raised whether the game would also be applicable for other people, for example high school students or museum visitors. The game itself of course is playable by people without prior knowledge of historical work and source selection, but the effect would not be the same. For museum visitors the game could present an insight behind the scenes of a museum. For high school student the game could also show what it feels like doing an internship at a museum or studying history. But for both groups the intended goal would not be met. 

Martin Dusinberre mentioned that the demand of finding new ways to teach history exists among high school teachers. **Marugoto** could definitely be a way of conveying historical ideas on high school level. But I feel like the story has to be specifically written for the target group to be most effective. If I were to rewrite *Feeling the Past* for high school students, I would change the main character to someone who has just finished their school years and is interested in history. Erick Lauber raises the question of character in video games (Lauber, 2005). The ideal case for a game-designer in his opinion would be to have a character just like the user. This would increase "identifiability and, presumably, learning" (p. 53). I agree with this statement. The tasks in a rewrite would be more basic at the beginning, but could definitely become more complex as the game goes on. This way the player could become familiar with the work inside a museum and of a historian.

Another suggestion was playing the game from inside the museum. For *Feeling the Past* in the present state the added benefit would not be significant. But as a general idea, games offer a real addition to the classic museum experience. It has been shown that a collaborative learning strategy between schools and museums can reinforce students' learning experience (Griffin, 2004). Bossavit et al. argue that applying informal educational tools like games within a formal learning context can enhance museum experiences and link them to classrooms (Bossavit et al., 2018). A rewrite of *Feeling the Past* could involve having the player physically finding the object in the collection and inspect it in person. This would strengthen the main argument that there is something to gain from using objects as historical sources. The play-through, a mix of virtual and real experiences, would have to be supervised if the players are physically interacting with real objects, but it would improve both the experience of being in the museum and learning about objects as historical sources. Still, it is important for the game to be created with the museum context in mind. Jenner and de Araújo have created a learning game for the German Maritime Museum centered around a conserved cog (Jenner & de Araújo, 2009). They noted based on behavioural research of museum visitors that for a game to be played inside the museum it has to capture the potential player's attention within 1-2 minutes, otherwise they pass onto the next module. Furthermore, long instructions should be avoided and the overall playtime should not be over 10 to 15 minutes.

### Conclusion

*Feeling the Past* had (and still has) the ambitious goal to change how historians select the sources they use in their work. It is too early to make any assessment of success or failure. However, I feel like an educational game like *Feeling the Past* can be a way to achieve change and the literature seems to support this thesis. I consider the open approach of *Feeling the Past*—giving the player freedom and allowing them to interpret the exercises based on their own interests—one of the best ways to show people what can be gained from historical sources. The future for educational games seems bright as more funding is allocated for it and multiple fields are interested in pursuing their possibilites for the humanities. A lot of work is being done on how to achieve desired pedagogical goals trough games. The opportunities are countless and the creative freedom of game-making specifically allows for various new approaches in writing and teaching history.

### Bibliography

Bossavit, Benoît et al.: Educational Games to Enhance Museum Visits for Schools. In: Journal of Educational Technology & Society, Vol. 21, No. 4 (October 2018). pp. 171—186.

Griffin, Janette: Research on Students and Museums: Looking More Closely at the Students in School Groups. In: Science Education, Vol. 88, (Supplement 1), (June 2004). pp. S59—S70.

Jenner, Walter / de Araújo, Leonardo Moura: Hanse 1380 - A learning game for the German Maritime Museum. In: Lecture Notes in Computer Science (Conference Paper), (September 2009). pp. 1—6. 

Lauber, Erick: The Design of 3-D, Fast-Action Digital Games for the Classroom. In: Educational Technology, Vol. 45, No. 6 (November-December 2005). pp. 52—55.

Pérez-Colado, Víctor Manuel et al.: Simplifying the Creation of Adventure Serious Games with Educational-Oriented Features. In: Journal of Educational Technology & Society, Vol. 22, No. 3 (July 2019). pp. 32—46.

	Henrik Jochum

	Bachwiesstrasse 11

	9402 Mörschwil

	henrik.jochum@uzh.ch

	079 126 92 17

	Matrikelnummer: 15-731-367

	Major: History of the Contemporary World / Zeitgeschichte

	Minor: Wirtschaftsgeschichte und Ökonomie

	Module: History in a Digitized World (Martin Dusinberre, Daniel McDonald)
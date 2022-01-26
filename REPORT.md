# Report : software quality assignment


## 2 Project global presentation


### 2.1 Project utility

   This project models different ways to organise a championship. It provides three types of competition, which are Tournament, League and Master, and make them gather competitors that compete in matches in order to win, according to the rules.

   A tournament is played between an number of competitors, power of two, and raises an exception when it is not the case. A league is played between any number of competitors, playing twice against each other. A master splits the competitors into groups and makes them play a league, then uses several strategies to select the winners of all groups, so that they form a power of two and can play a tournament to win the master.

   Finally, a system had been set to allow journalists and bookmakers to follow the competitions and make observations to react to each result of them.


   To launch the project, it is necessary to compile first the whole code, and then run the different provided mains. To do so, please refer to the parts "Compile our code" and "Run our mains" of the readme. As you can see, there is no parameter to enter.


   The project returns as a result the unfolding of a competition depending on which main one deciced to run. It is list of the matches played in either a league or a tournament or a master, with reactions of journalists or bookmakers, or not. For more details, please refer to the part "Run the tests" of the readme which shows in the end an example of what one can be expecting while launching the project.


### 2.2 Project's Description

   In the project, a readme is provided with relevant informations. All one desires to know about the code, the tests, the organisation and the way of running the project is well explained, indicated and updated.


   There is a project's documentation as well. It explains all informations about the software. For more details, please refer to the readme, from part "Subject" to part "Run the tests".


   Regarding the relevance and the completeness of the documentation provided in the readme, all informations are updated, sufficient and allow to use and launch the software.


## 3 Software's history


### 3.1 Git's analysis

   What concerns the team's composition, there are three contributors according to the project's Git. In terms of balance, only two of them have contributed the most at its realisation, according to the content "Contributors".


   The project seems to be no longer active since the last commit had been performed one month ago. Furthermore, the commits have been done each month at the same period, which witnesses a certain constancy.


   There exists only one branch which is the branch called "main", according to the content "Branches". It is also the lone branch used.


   The "pull requests" mecanism is not used.


## 4 Software's architecture


### 4.1 External libraries' use

   There are two external libraries referenced in the project : java.util and org.junit .

   According to second screenshot, there are 16 unused dependencies to the library java.util (10) and the internal packages (6).

   The use of those libraries tell us about the relevance of their use. Each library is called each time with a method that is supposed to be useful once for all instances of the class. So, there are no libraries applying the same effect. 


### 4.2 Packages organisation

   In the source folder, we count 9 packages, while in the test folder, we find 8 packages.

   The package competition depends on packages competition.competitor, competition.match.util and competition.observer.util; then, The package competition.organization depends on the packages competition and competition.competitor; finally, the package competition.organization.masters depends on packages competition.organization, competition.competitor and competition. They form no cycles. 

   There are 4 levels of packages in the source folder, as well as in the test folder, whose packages follow the same hierarchy. Moreover, there is no package containing only one other without even a single class.


### 4.3 Classes' distribution in the packages

   There are at least one class per package, at most eight classes per package for an average of 2.56 classes per package. In total, there are 23 classes in the source folder.

   The distribution of the classes is more or less balanced and there is no package gathering the most part of them and as each package contains at least one class, the non-leave packages do contain classes.


### 4.4 Classes' organisation

   The classes' hierarchy is quite deep since there are 3 children for the class Competition (League, Master, Tournament), for a depth of 2 in the inheritance tree.

   In general, the classes are stable. But the most unstable class tends certainly to be the class Competition since it is the root of the project and the most called by the other classes while importing only 4 of them.


## 5 Deeper analysis


### 5.1 Tests

   There are 9 unit tests, 2 mock-type classes, 21 test methods and 42 assertions.

   By studying the tests, we get a code coverage of 29.5% according to the screenshot taken in Eclipse. Only parts that are not meant to be tested (the strategies or match classes for example) remain uncovered.

   The tests are exclusively unit and they all pass.


### 5.2 Comments

   As it is shown in the third and the fourth screenshots of SonarQube, there are 197 lines of comments, all of javadoc type.

   The parts without any comments are mostly the main classes since they are not documented. In SonarQube, they have just the name of the author which indicated, and therefore, have less than 5 lines of comments.


### 5.3 Deprecation

   There are no deprecated peace of code in the whole project.


### 5.4 Code duplication

   An analysis with SonarQube (fifth screenshot) revealed that the duplication code is present in the classes Strategy1 and Strategy2. 

   A good way to avoid this is to gather the common behaviour of both classes in an abstract class and make them inherit from it.


### 5.5 God classes

   What concerns this category of classes, Competition and Master possess the greatest numbers of method of the whole code.


### 5.6 Method analysis

   Please refer to the sixth screenshot for the cyclomatic complexity. There are in total 646 lines of codes, according to the seventh screenshot.









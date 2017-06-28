Development Environment
=======================

In this course we will use the following technologies for developing, testing, building, and submitting programs.

- [Eclipse](#eclipse)
- [Github](#github)
- [Maven](#maven/travis)
- [Travis](#maven/travis)

## Eclipse
Eclipse is an Integrated Development Environment (IDE) that provides a friendly interface for building large Java programs. If you wish you may use a different IDE, for example IntelliJ or NetBeans, or a text editor like Sublime Text along with the command line. The instructor and TAs will only provide support for Eclipse, however.

Make sure you are using Eclipse Mars or greater and that it is configured to use Java 8.

1. Download [Eclipse here](https://eclipse.org/). Select the Eclipse IDE for Java Developers.
2. Download [Java 8 here](http://www.oracle.com/technetwork/java/javase/downloads/index.html)
3. Make sure that Eclipse is configured correctly. `Eclipse > Preferences > Java > Compiler` should show a "Compiler compliance level" of 1.8 and `Installed JREs` should show Java SE 8. See the professor if you need help with this.


## Github
[Github](https://github.com/) is a web-based version control system. All notes and resources will be posted on github. In addition, all assignments will be distributed and submitted using github. 

Create a github user account if you do not already have one and sign up for the [Student Developer Pack](https://education.github.com/pack). This will be very useful throughout your CS career.

There are several ways to download code from and commit code to github.

1. [Command line](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) - If you are a Linux user, or if you want to prepare yourself for future CS classes you should use the command line.
2. [Egit](http://www.eclipse.org/egit/) - Eclipse has an integrated client that makes it easy to access git repositories. 
3. [Github Desktop](https://desktop.github.com/) - If you are a Mac or Windows users you may find it helpful to use the standalone client tool. 

The instructor will generally use some combination of 1 and 2. 

The instructor will use [Github Classroom](https://classroom.github.com/) to manage assignments. For each assignment, you will be provided with a link that you will click to create a new repository. When it is created, that repository will be seeded with skeleton code and test cases. You will download the repository and maintain and submit your code by committing to the repository.

For most assignments, you will follow the following procedure:

1. **Create Repo** - Use the link provided to create your initial repository.
2. **Clone** - Create an initial copy of the repository on your local computer.
3. **Edit/Test** - Edit and test your code. **Do not** modify the test files or any other configuration code provided.
3. **Add** - Add any files that have been modified. **Do not forget this step!**
4. **Commit** - Save the changes you just added.
5. **Push** - Upload the changes to the github servers.
6. **Take a break** - Sleep, shower, eat.
7. **Pull** - Before your start working again, make sure to download any changes. The instructor or TA may have made comments or edits to your code, or you may be working on multiple machines. It is always a good idea to make sure your local copy is consistent with what is on the github server before beginning work again.
8. **Repeat** - Start again at step 3.

It is *strongly* advised that you spend some time reading/watching git resources online. A good place to start is this set of [git videos](https://git-scm.com/videos).

<!--## Loading Projects into Eclipse
1. Open Eclipse specifying the directory created by the Github tool (e.g., `/Users/srollins/cs601/srollins-labs`). Make sure to select the `<username>/labs` repository.
2. Right-click under the `Package Explorer` and select `New > Java Project`.
3. In the `Project name:` field, type `CS601Labs`. Make sure to specify this exactly as it will see that there is a directory with this name and automatically import its contents.
4. Click `Finish`.
5. Modify your build path to include JUnit by right-clicking on the project folder, selecting `Build Path > Add Libraries`, then selecting `JUnit`. 
6. You're done!

## Pulling Down New Projects
The instructor may add new projects to your repositories as new work is assigned. In the Github tool, simply `Sync` to pull down the latest updates from github. Then, follow the steps listed in the [Loading Projects into Eclipse](#loading-projects-into-eclipse) section to load the projects into Eclipse and begin work.
-->

## Maven/Travis




## Submission
Commit your changes to Github *early and often*. You should *not* use Github as only a submission tool. Everytime you get a new method or feature working *commit your changes to Github*! 

### Using the Github Tool
1. On the `Changes` screen, select all of the files you wish to commit. This should *not* include classfiles or metadata, but should include any new Java files you have implemented, and any Java or other files you have changed. 
2. In the `Summary` enter a short, meaningful description of the change. Do *not* enter messages such as "commit 1", "commit 2". *DO* enter messages such as "Completed YelpStore addReview". In the `Description` box provide a more detailed description of the change you have made in this version of the code. 
3. Click `Commit to master`. 
4. Click `Sync` at the top right corner.
5. Congratulations! Your changes should be available on Github.

###Hints
1. Make sure *all* of the files you have changed or added are included. 
2. Verify that all changes have been committed as expected by using the Github website.


###To Submit
1. Make sure you are passing all tests as described in the assignment description, if unit tests are provided.
2. Follow the instructions for [creating a new release](https://help.github.com/articles/creating-releases/) for your project. 
3. The instructor will receive an automated email noting your submission. After your submission is verified, you will receive an email inviting you to sign up for code review.


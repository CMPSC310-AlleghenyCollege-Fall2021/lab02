# lab02_cs310f2021

## Deadlines:

- _Project Idea Exploration_: October 4th by 11:30am
- _Code and Report_: October 13th by 3pm
- _Project Demonstration_: September 13th, 3pm - 4:50pm

## Table of Contents

- [Summary](#summary)
- [Objectives](#objectives)
- [Agreement](#agreement)
- [Code of Conduct](#code-of-conduct)
- [Learning](#learning)
- [Assignment Specification](#assignment-specification)

  - [Set Up](#set-up)
  - [Arduino Programming](#arduino-programming)

- [Planning](#planning)

- [Project Walkthrough](#project-walkthrough)

- [Project Demonstration](#project-demonstration)

- [Required Deliverables](#required-deliverables)

- [Assignment Assessment](#assignment-assessment)

- [System Commands](#system-commands)

  - [Using Docker](#using-docker)
  - [Using Gradle](#using-gradle)
  - [Automated Checks with GatorGrader](#automated-checks-with-gatorgrader)

- [Receiving Assistance](receiving-assistance)

## Summary

Designed for use with [GitHub Classroom](https://classroom.github.com/), this repository contains the starter files for Laboratory 2 assignment in Computer Science 310.

This laboratory assignment invites you to work in a team of two or three to implement a learning agent for an object detection application. You are also responsible for writing a detailed report, stored in the file `writing/reflection.md`. This is a Markdown file that must adhere to the standards described in the [Markdown Syntax Guide](https://guides.github.com/features/mastering-markdown/).

## Objectives

To learn how to use a computer vision OpenCV software and a Python programming language for computer vision applications. To correctly apply image pre-processing (for example, smoothing, blurring, thresholding, edge detection) to images using OpenCV functions. To gain understanding of image processing techniques that can be used for specific computer vision applications. To apply a computer vision technique using supervised learning algorithm to a problem in object detection. To evaluate the performance of the developed system under various environmental conditions and to reflect on its design and development.

## Agreement

This laboratory assignment will be completed in groups of two or three (max). Each team member must follow the community guidelines, including team guidelines, developed by the students in this class, included in this repository.

By class time on Monday, October 4th, you must have a clearly defined project description, including the type of data and algorithms you will attempt to use. If your project requires any hardware, you must specify this as well by that date.

## Code of Conduct

Throughout the completion of this project you must adhere to the community guidelines that we developed as a class. In addition to reporting any violations of the code of conduct, please make sure that you attest to the fact that you followed the code of conduct. Students who think that the class should revise some aspect of the guidelines must use the GitHub issue tracker for that repository to suggest, discuss, and implement any required changes.

## Learning

To review what you have learned about learning and OpenCV, please read the supplemental chapter given in the lab repository and sections 7.1--7.3 from the [Artificial Intelligence: Foundations of Computational Agents](https://artint.info/2e/html/ArtInt2e.Ch1.html) textbook.

If you have not done so already, please read all of the relevant [GitHub Guides](https://guides.github.com/) that explain how to use many of the features that GitHub provides. In particular, please make sure that you have read the following GitHub guides: [Mastering Markdown](https://guides.github.com/features/mastering-markdown/), [Hello World](https://guides.github.com/activities/hello-world/), and [Documenting Your Projects on GitHub](https://guides.github.com/features/wikis/).

## Assignment Specification

In this two-week lab students are invited to implement a learning agent using an open-source learning platform, OpenCV, for an object detection application of your choosing. You must work with images, recorded videos, or a live video feed. As you select a specific application, you must first decide what type of object your agent will try to learn to identify by applying a classification algorithm and what environment it will operate in. Then, you need to select an algorithm to perform the classification and evaluate its effectiveness. You can utilize class programs, existing open source projects, and OpenCV documentation for usage examples of various methods. You are also free to select an algorithm not discussed in class with the approval of the instructor.

### Baseline Requirements

- Your project should be implemented in Python.
- You should use OpenCV and possibly sklearn library.
- While your project should be based on an existing project, it should NOT be just a copy of an existing project (for example, a class program or an online tutorial).
- You must include references to all resources used in your report as links to online resources or by specifying activity number or reading resource if using class resources.
- You must include and specify all the steps needed to successfully run your program(s). This include installation instructions or docker set up, depending on how you prefer the user run your tool.

### Steps to Project Completion

1. Select an application for object detection. What type of an object would you like to detect? Are the pre-trained samples for this object available? You can consult resources such as [kaggle](https://www.kaggle.com/datasets) and [opencv cascades](https://github.com/opencv/opencv/tree/master/data).

2. Select a supervised learning algorithm for object detection, a classifier, that uses certain features of the image to correctly label them as a specific object or not. You need to select a learning algorithm that you will utilize (e.g., SVM, Random Forest, etc.) and a feature descriptor that your algorithm will use (e.g., Haar, HOG, LBP). I suggest using LBP or HOG features, as they are integer, fewer and more discriminant in contrast to Haar features, so both training and detection with LBP and HOG are several times faster then with Haar features. You should use supervised learning algorithms that are available in OpenCV and/or sklearn library. Make sure the classifier you select has already been trained using specific data sets and a certain feature descriptor in OpenCV or select a feature descriptor that already has compiled labeled data set that can be used for training.

3. Conduct an experimental analysis. After you have conducted preliminary tests to ensure your program(s) runs without errors and you are satisfied with your detection accuracy, you need to conduct environment comparison experiments. Specifically, we are interested in learning the performance of object detection for different images or camera positions.

## Planning

Please take a few days to research and decide on your specific application. Make sure you have thought about steps 1 and 2 above before you commit to a project idea. Once you selected a specific application, and before the class time on October 4th, submit your project description by completing the appropriate section in the writing.

## Project Demonstration

At the beginning of the lab session on Wednesday, October 13th, each team will be given an opportunity to demonstrate their project. When the lab session starts, teams will be given a few minutes to set up their demonstrations and get them running. Then, class members will participate in an interactive demonstration session, where everyone will be able to view each demonstration.

## Required Deliverables

This assignment invites you to submit the following deliverables through your team repository.

1. Planning portion of the report due on October 4th by 11:30am. The rest of the written requirements are due at 3:00 pm on October 13th.
2. A properly completed and commented source program(s). Please make sure your source code is located inside "src" directory in your lab0s repository.
3. The report, stored in /writing/report.md and written in Markdown, that contains the planning portion as described above, and provides answers in all remaining sections (follow the prompts inside the report document).
4. Lab session on October 6th will be used for lab work.
5. The lab session on October 13th will be used for demonstrations.

## Assignment Assessment

The grade that a student receives on this assignment will have the following components.

- **GitHub Actions CI Build Status [up to 10%]:**: For lab02 repository associated with this assignment students will receive a checkmark grade if their last before-the-deadline build passes.

- **Mastery of Verbal Explanation during Demonstration [up to 15%]:**: Since the timely project development and the ability to communicate technical details of a project is crucial to building successful software applications, a portion of students' lab grade will be determined based on the quality of the project demonstration.

- **Mastery of Technical Writing [up to 15%]:**: Students will also receive a checkmark grade when the responses to the writing questions presented in the `report.md` reveal a proficiency of both writing skills and technical knowledge. To receive a checkmark grade, the submitted writing should have correct spelling, grammar, and punctuation in addition to following the rules of Markdown and providing conceptually and technically accurate answers.

- **Mastery of Technical Knowledge and Skills [up to 60%]**: Students will receive the largest portion of their assignment grade when their project implementation reveals that they have mastered all of the technical knowledge and skills developed during the completion of this project. As a part of this grade, the instructor will assess aspects of the project including, but not limited to, the completeness and the correctness of the program(s), the use of effective source code comments and Git commit messages, the effective experimental analysis.

All grades for this project will be reported through a student's gradebook GitHub repository and the feedback pull request in this repository if necessary.

## System Commands

### Using Docker

Once you have installed [Docker Desktop](https://www.docker.com/products/docker-desktop), you can use the following `docker run` command to start `gradle grade` as a containerized application, using the [DockaGator](https://github.com/GatorEducator/dockagator) Docker image available on [DockerHub](https://cloud.docker.com/u/gatoreducator/repository/docker/gatoreducator/dockagator).

```bash
docker run --rm --name dockagator \
  -v "$(pwd)":/project \
  -v "$HOME/.dockagator":/root/.local/share \
  gatoreducator/dockagator
```

The aforementioned command will use `"$(pwd)"` (i.e., the current directory) as the project directory and `"$HOME/.dockagator"` as the cached GatorGrader directory. Please note that both of these directories must exist, although only the project directory must contain something. Generally, the project directory should contain the source code and technical writing of this assignment, as provided to a student through GitHub. Additionally, the cache directory should not contain anything other than directories and programs created by DockaGator, thus ensuring that they are not otherwise overwritten during the completion of the assignment. To ensure that the previous command will work correctly, you should create the cache directory by running the command `mkdir $HOME/.dockagator`.

If you are running your program on a Windows Operating System, you should run the following command instead, replacing the word "user" with the username of your machine:

```bash
docker run --rm --name dockagator -v "%cd%":/project -v "C:\Users\user/.dockagator":/root/.local/share gatoreducator/dockagator
```

Here are some additional commands that you may need to run when using Docker:

- `docker info`: display information about how Docker runs on your workstation
- `docker images`: show the Docker images installed on your workstation
- `docker container list`: list the active images running on your workstation
- `docker system prune`: remove many types of "dangling" components from your workstation
- `docker image prune`: remove all "dangling" docker images from your workstation
- `docker container prune`: remove all stopped docker containers from your workstation
- `docker rmi $(docker images -q) --force`: remove all docker images from your workstation

### Using Gradle

Since the above `docker run` command uses a Docker image that, by default, runs `gradle grade` and then exits the Docker container, you may want to instead run the following command so that you enter an "interactive terminal" that will allow you to repeatedly run commands within the Docker container.

In Linux and Mac OS:

```bash
docker run -it --rm --name dockagator \
  -v "$(pwd)":/project \
  -v "$HOME/.dockagator":/root/.local/share \
  gatoreducator/dockagator /bin/bash
```

In Windows OS (replace `user` with your machine's username):

```bash
docker run -it --rm --name dockagator -v "%cd%":/project -v "C:\Users\user/.dockagator":/root/.local/share gatoreducator/dockagator /bin/bash
```

Once you have typed this command, you can use the [GatorGrader tool](https://github.com/GatorEducator/gatorgrader) in the Docker container by typing the command `gradle grade` in your terminal.

## Automated Checks with GatorGrader

In addition to meeting all of the requirements outlined in the assignment sheet, your submission must pass the following checks mainly related to writing and the number of commits that [GatorGrader](https://github.com/GatorEducator/gatorgrader) automatically assesses. If [GatorGrader's](https://github.com/GatorEducator/gatorgrader) automated checks pass correctly, the tool will produce the output similar to the one below.

```
✔  The report.md in writing has exactly 0 of the 'Add Your Names Here' fragment
✔  The Application.ino in src/lab01/Application has at least 2 single-line Java comment(s)
✔  The Application.ino in src/lab01/Application has exactly 0 of the 'TODO' fragment
✔  The Application.ino in src/lab01/Application has exactly 1 of the 'setup(' fragment
✔  The Application.ino in src/lab01/Application has exactly 0 of the 'Add Your Names Here' fragment
✔  The report.md in writing has at least 1 of the 'list' tag
✔  The report.md in writing has exactly 9 of the 'heading' tag
✔  The repository has at least 10 commit(s)
✔  The file Application.ino exists in the src/lab01/Application directory
✔  The report.md in writing has at least 200 word(s) in total
✔  The file report.md exists in the writing directory
✔  The Application.ino in src/lab01/Application has at least 1 of the 'loop(' fragment
✔  The report.md in writing has exactly 0 of the 'TODO' fragment
```

## Receiving Assistance

If you are having trouble completing any part of this project, then please talk with either the course instructor during the lab session. Alternatively, you may ask questions in the Slack workspace for this course. Finally, you can schedule a meeting during the course instructor's office hours.

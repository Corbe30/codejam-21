![OSDCodeJam Banner](./assets/codejam-banner.png)

<div align="center">

[![OSDC Discord Server](https://img.shields.io/discord/357949642266116108?color=magenta&label=discord&logo=discord&logoColor=white)](https://discord.gg/vfhyHW5BkJ) [![OSDC Telegram Chat](https://img.shields.io/badge/Telegram-osdc-blue?logo=telegram)](https://t.me/jiitosdc)

<hr>

# Welcome to OSDCodeJam'21!

</div>

## :ledger: Index

- [What is a Code Jam?](#what-is-a-code-jam)
- [Particulars](#particulars)
- [Timeline](#timeline)
- [Format](#format)
- [Submitting your Project](#submitting-your-project)
- [Rules](#rules)
- [Judging](#judging)

<hr>

## What is a Code Jam?

This is something you might be asking yourself. A Code Jam is a chance to create something with a team. You are paired up with a group of other participants just like yourself with whom you collaborate and make a project on a given theme. You then have around a week's time to create the best project you can. See [Format](#format) for detailed information.

## Particulars

- #### The winners get Amazon gift cards worth Rs. 1k, and swags!

- **Theme:** ***Combining Opposites***

## Timeline

- Registration: 1-5 January 2021
- Teams Announcement: 8 January 2021
- Theme Announcement: 8 January 2021
- Jamming (Coding Period): 9-14 January 2021
- Results Meetup: TBD

## Format

- Participants register individually for the Jam, mentioning their technical skills.
- The organizers group the participants in teams of 3 (or 4, depending on the number of registrations) based on their skills and experience to have teams with equal skill levels.
- The organizers announce the teams and theme for the Jam.
- Team members communicate and collaborate to make a project within the 6 days of the Jam, that fits their interpretation of the theme.
- The project is [submitted to this repo](#submitting-your-project) via a Pull Request.
- The guest judges choose the winners based on the [judging criteria](#judging), which will be announced, and their projects showcased on the Results Meetup.

## Submitting your Project

You can either use [Method 1](#method-1) or [Method 2](#method-2) to submit your project.

### Method 1: Through a PR

#### 1. Fork this repository
Start by [forking this repository](https://github.com/osdc/codejam-21/fork). Only one team member needs to do this, the other members can fork that person's fork and work on it.

#### 2. Find your team folder in the repository
The repository should already contain a subdirectory named after your team. _All your project files must be contained within your team's subdirectory only_. If you make any changes to files other than those in your team folder, we will not be able to merge your PR.

If you're using a CI/CD workflow, and require configuration files/folders in the root of the repository, either try to use a unique name (e.g. prefix the configuration files with your team name) or remove the files/directories just before the final submission.

#### 3. Create a Pull Request
Only one team member has to do this (The same one who forked this repo directly).<br>
Open a pull request from your fork's `main` to the `main` branch of this repository in order to submit your project. You should use the name of your team as the title of the Pull Request. Please open your Pull Request at the start of the Jam (see the next step for clarification).<br>
**Avoid opening spam PRs to the repo, and there should be only one PR from each team.**

#### 4. Keep pushing to your main branch
The Pull Request you created will keep getting updated automatically whenever you push code to `main` branch on your fork, so you can create the PR whenever you want, and you only have to do it once. You do not need to wait until the very end of the Jam to make the PR and risk missing the deadline. Just keep pushing code to your `main` branch as you keep progressing, and do your best to finish before the Jam ends!<br>
When working as a team, you should consider learning about feature branches so that you don't all work directly on the `main` branch and cause each other a bunch of conflicts. For a short explanation of how this works, [see this video](https://www.youtube.com/watch?v=j7YDbrS9I48).

### Method 2: Using git submodules

If you have already made a separate repository for your project, you can use git submodules to submit your project.

#### 1. Fork this repository

Start by [forking this repository](https://github.com/osdc/codejam-21/fork).

#### 2. Edit the `.gitmodules` file

Add the following to the file (make the required changes in `path`, `url`):

``` git-config
[submodule "<your team name>"]
	path = <your team name>
	url = <path to your project>
```

#### 3. Commit the changes and create a Pull Request

Commit the `.gitmodules` file and open a PR to the `main` branch of this repository.
You don't need to manually update submodules for every change, [dependabot](https://dependabot.com/submodules/) will automatically do that for you. So, you can just make this PR once.

## Rules

- This Jam is only open for JIIT Noida students (Both 62 and 128).
- Your project should be platform agnostic. For example, if you use filepaths in your submission, use pathlib (in Python) to create platform agnostic Path objects instead of hardcoding the paths.
- There is no restriction on the type of project you come up with, or the languages you use. It can be anything from a web app to a system library (Hardware projects excluded).
- You must document precisely how to install, setup and run your project. This should be as easy as possible (consider using dependency managers).
- All code must be written and committed within the time constrictions of the Jam. Late commits may be reverted, so make sure you leave enough time to bug test your program.
- You must get contributions from every member of your team, if you have an issue with someone on your team please contact a member of the administration team. These contributions do not necessarily have to be code, for example it's absolutely fine for someone to contribute management, documentation, graphics or audio. Team members that do not contribute will be removed from the Code Jam, and will not receive their share of any prizes the team may win.
- You must use GitHub as source control.
- All code and assets must be compatible with an Open-Source license. This is because we will be merging your submission into this repo at the end of the jam.

## Judging

Because programming is full of subtleties and judging is not an exact science, this section will inevitably fall short of being an exact guide for how to win, but it should at least give you an idea of what you should be mindful of as a participant.

- **Code Style:** How easy to read, pleasant to work with, well commented, and self-documenting your code is.
- **README:** How well your README file explains your project, its setup instructions and its features.
- **Uniqueness and Creativity:** In order to level the playing field a bit, we've decided that this is the most important factor. If your idea is an exceptionally good one and you are a beginner, we will cut you some slack on style and execution. It is therefore crucial that you consider _what_ to do more carefully than exactly _how_ to do it.
- **Adherence to Theme:** How uniquely you interpreted the theme and justified it with your idea.
- **Execution:** An important factor is whether your solution is the best solution to the problem you are solving. If your solution is overly convoluted, this will count against you in our evaluation. While the code jam is ongoing, organizers will be available to you for any help or suggestions.
- **Teamwork:** During the Jam, you will be assigned teammates. It is crucial that you find a way to work with your teammates, as we will be evaluating your ability to work as a team. Team members who constantly bicker, complain about each other, or fail to divide up tasks so that everyone can contribute will be penalized when we evaluate the code jam. This does not, however, mean that a team that has a "bad egg" will automatically be unable to win the code-jam. If a team member refuses to play well with the rest of the team or does not participate in the jam, we will usually remove that person from the team and attempt to find a new teammate for the team to replace them.

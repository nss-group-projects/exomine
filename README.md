# Exomine

This project has you building an application that lets governors of different colonies in our Solar System purchase minerals from various mining facilities that human have established.

> "This project has made me realize the importance of an ERD and quality design of your data structure and how to access that data."
>   - Former NSS Student

## Professional Collaboration

In this project, you are expected to start building your professional collaboration skills by writing issue tickets and having professional pull requests.

### Tickets

As a team, review the [Writing a proper GitHub issue](https://medium.com/nyc-planning-digital/writing-a-proper-github-issue-97427d62a20f) article so learn the basics of how you should approach creating a ticket to describe work that must be done on the project.

All tickets will be added to a project board. Here's how you set that up.

1. Go to the team's Github repository page.
2. Click on the **Projects** tab at the top.
3. At the top of this view, you will see a green **Link a project** button, click on the down arrow on the right of it.
4. Choose **New project** then click on the green button.
5. Choose **Board** from the types on the window that appears.
6. Enter in **Exomine** in the _Project name_ input field at the top.
7. Click green **Create project** at the bottom.

To create a issue ticket for your project, follow these steps.

1. Go to the team's Github repository page.
2. Click on the **Issues** tab at the top.
3. Click the **New Issue** button.

Finally, once a ticket is created...

1. Go to your project board.
2. At the bottom of the _To do_ column, click on the plus sign.
3. Click on the plus sign again.
4. Choose **Add item from repository**
5. In the window that appears, make sure your team repository is chosen in the dropdown.
6. All tickets that you have created will appear in a list.
7. Choose them all
8. Click the green **Add selected items** button at the bottom.


### Pull Requests

As a team, review the [Writing A Great Pull Request Description](https://www.pullrequest.com/blog/writing-a-great-pull-request-description/) article. When each teammate pushes a branch to be reviewed and/or approved by a peer, it is expected that a comprehensive, detailed description has been added to the pull request.

## Github Workflow

Here's the link again to the [Github Workflow Reference ](https://gist.github.com/Valerie-Freeman/171fd7e639fcd1f9129bc79144b5f5ea) that everyone must use during this project.

## Workflow Animation

This animation shows you the basic behavior of the application.

![](./images/exomine.gif)

## Features

**Given** a governor wants to purchase minerals for a colony<br/>
**When** a governor is chosen<br/>
**Then** the inventory for that governor's colony should be displayed _(the mineral names and quantities)_<br/>
**And** the facility select element should be enabled

**Given** a governor has been chosen<br/>
**When** a mining facility is chosen<br/>
**Then** the minerals available for purchase should be displayed _(the mineral names and quantities)_<br/>
**And** a radio button should be next to each

**Given** a governor has been chosen<br/>
**When** a mining facility is chosen<br/>
**Then** any minerals with a quantity of 0 should not have a radio button<br/>


**Given** a governor has been selected<br/>
**And** a facility has been selected<br/>
**When** a mineral has been selected<br/>
**Then** the chosen mineral should appear in a _Space Cart_ area with a button labeled _Purchase Mineral_


**Given** a governor has been selected<br/>
**And** a facility has been selected<br/>
**And** a mineral has been selected<br/>
**When** the _Purchase Mineral_ button is clicked<br/>
**Then** 1 ton of the chosen mineral should be added to the inventory of the active colony
**And** 1 ton of the chosen mineral should be removed from the inventory of the chosen mining facility<br/>

---

This last feature will require you to modify the data in your API. This is performed with an [HTTP request that uses the PUT method](https://dev.to/silvenleaf/fetch-api-easiest-explanation-part-3-4-put-by-silvenleaf-3oe8) instead of POST.

## Data Relationships

Below you can ready some basic information about the properties and relationships of the data you need for this application. 

### Governors

Each human habitation colony in the Solar System _(Earth, Mars, Europa, etc...)_ has a governor. To keep each colony running efficiently, the governor has to purchase essential minerals from lightly staffed mining facilities that have been established on asteroids, moons, and rocky planets.

From time to time, governors take leaves of absence, so their status can change from active to inactive. Only active governors should be displayed in the UI. By law, any person is eligible to become a Governor, but can only be a Governor of a since colony at any point in time.

### Colonies

Each colony can have one, or more, active governor depending on the size of the colony. For example, Earth could support up to five governors that are responsible for different regions of the planet.

### Mining Facilities

Each mining facility can be active or inactive depending on the changes of staffing from the various companies that operate the facilities. Each object representation should record the name of the facility and its active status.

If a mining facility is inactive, then the button in the UI should never be enabled, even after a governor is chosen.

### Minerals

Each mining facility can produce several kinds of minerals. Each mineral type can be produced at several mining facilities. Likewise, a colony can purchase many minerals. A single mineral _(Iron or Magnesium)_ can be purchased by many colonies.

Your team may want to consider that some of your tables will have more than one foreign key on them to handle this kind of relationship - called a many to many relationship.

* Read the [What Is a Many-to-Many Relationship in a Database?](https://www.vertabelo.com/blog/many-to-many-relationship/) article.
* Ask [ChatGPT to explain](https://chat.openai.com/) many to many relationships to the team.


## Algorithmic Planning

There is more to algorithmic thinking than just comments for a project like this.

1. Have we documented how the application UI should be structured?
2. Is our ERD complete and approved by our instructors?
3. Do we know which HTML elements we are going to use for each component?
4. Have we defined the CSS classes for each component?
5. Do we know which modules need to be created, and have the responsibility documented for each one?
6. Do we know the order in which the modules should be developed?

If anyone on the team is unsure about any of these questions, it leads to uncertainty, loss of productivity, and disagreements. We strongly urge you to solve this problem completely before writing any code. 


## Stretch Goal

**Do not attempt the stretch goal until you have completed the basic requirements above.**

If your team would like to do more advanced state manipulations, refactor your code to allow a governor to select minerals from multiple mining facilities before finalizing the purchase. A working example done by a previous team can be seen at [https://solar-mine.onrender.com/](https://solar-mine.onrender.com/). 

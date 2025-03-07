---
title: Warranty Wise
subtitle: An all in one warranty hub
---
## Overview
Warranty-Wise is a web application focused on providing users with a centralized platform where they can search, filter and view their product and service warranties. Users are also able to browse and explore our built in information hub, where they can find answers to questions pertaining to the warranty claim process along with its requirements, warranty acquisition process and requirements, warranty extension options and more. By using Warranty-Wise, users can stay organized with all of their warranties and be automatically reminded when certain ones are about to expire, and be offered extension options based on their needs. 

## Weekly Development History

### January 20th
During the initial week of development, after meeting with the project sponsor, we focused on solidifying the overall vision of the project, along with establishing some initial user stories reflecting the different features outlined in the vision and how users would utilize them. Because we had time, we also started researching potential tech stacks that could be utilized for this project. 

![](doc/initial-user-stories.png)

### January 27th
After reviewing the user stories from last week, we knew that we needed to make some changes and add more detail to the overall process that the user goes through while both navigating our site, as well as utilizing the feature. We also got started on creating initial mockups of the main pages of the application, as well as the high-level architecture and creating the GitHub organization and repositories that will hold the home page as well as the code base. 

![](doc/architecture1.png)
![](doc/architecture2.png)

### February 3rd
After the weekly meeting, most of the mockups were approved, with a few needing changes based on general agreement from the entire group about how we want to implement certain features. The high-level architecture was also approved, but will continue to be a work-in-progress as we go through the development of the project, adding or removing any features as time goes on. The next steps include officially launching the Github home page and finalizing the tech stack and getting started on thinking about the specifics of the database. Figma and other similar tools were brought up during the meeting as something we could use to get some initial code using the mockups that were already created. 

![](doc/mockups.png)

### February 10th
During the weekly meeting, we looked at a barebones entity relationship diagram on potential tables and fields in the database. The consensus was that more research needs to be done regarding different types of warranties, claims, and documents and information needed for these processes. Extra research also needs to be done on potential extended warranties other services we can provide to users through the AI feature. On the front end, we continue to add more detail and flesh out the previous mockups and will soon start turning the designs into code through Figma and builder.io, and eventually start having the development environment configured. 

### February 17th
The revised ERD was showcased during the meeting and was met with great feedback. More work also went into implementing the homepage and getting an overall theme for the front-end. A basic login and signup page, along with a profile/account update page has been setup to test authentication, more styling can be done on these pages at a later date. For next week, we plan to continue working on our current task of focusing on a user story and getting those features and pages implemented. 

![](doc/revised_ERD.png)
![](doc/log_in_and_sign_up.png)
![](doc/update_profile.png)
![](doc/initial_homepage.png)


### February 24th
After the ERD was approved, the warranties table was setup on Supabase and populated with some initial data that can be used to render dummy data onto the site. A basic form for manually inserting warranties was created and verified to be inserting into the table after the form has been submitted. It was brought up during the meeting that we should note down that an automatic ingesting process would be preferred over manual forms, and this was something that can be accomplished through AI and OCR. This will be looked into further as more of the basic functionalities are fleshed out. 

More pages have been created following the theme of the homepage and more pages will continue to be worked on, especially regarding the information laid out in each page. For log-in and sign-ups, more authentication will be provided, such as using one's Google, Github, and Facebook accounts to log-in/sign-up. 

![](doc/warranty_form.png)
![](doc/initial_landing.png)
![](doc/better_dash.png)
![](doc/login.png)

### March 3rd
For this week, we mainly focused on finishing up the core functionalities dealing with warranties, as well as styling the corresponding components related to each function. We have also moved towards rendering individual components instead of pages so that all actions allow the user to stay on the same page. As of this week, we have implemented, displaying the list of warranties the user owns, displaying more details about each warranty after their individual cards have been clicked, creating, editing, and deleting warranties. 

For the future, we plan on moving our focus towards more AI-related features, including mapping out the individual areas that we want to incorporate AI into the application, as well as researching different AI APIs or tech stacks that we can learn and utilize in the application. 

![](doc/landing-styled.png)
![](doc/warranty_items.png)
![](doc/Warranty_details.png)
![](doc/edit_warranty.png)
![](doc/delete_warranty.png)
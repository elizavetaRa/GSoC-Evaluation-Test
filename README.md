## CERN-HSF GSoC 2022
# Image Explorer for ownCloud Infinite Scale
Link to project: https://hepsoftwarefoundation.org/gsoc/2022/proposal_CERNBOXimageExplorer.html

## Evaluation test

Below are 4 evaluation tasks that you will perform to demonstrate the skills needed for the project.
We suggest you create a private Github repo (cloned from oCIS Web), give us read permissions, and send us the url once the tasks are finished. Also fee free to contact us in case you need any clarification.

### Task 1: Install OCIS & local web

* Install and run OCIS, either as a binary or as docker compose, following the instructions [here](https://owncloud.dev/ocis/getting-started/). Please make sure that you are taking the latest release version. 
* Fork the [web repository](https://github.com/owncloud/web) 
* Setup web with OCIS backend as described [here](https://owncloud.dev/clients/web/backend-ocis/). 

If you encounter problems with installation you can ask for help [here](https://talk.owncloud.com/channel/ocis).

### Task 2: Image filter

OCIS web is a [Vue.js](https://v2.vuejs.org/) project, consisting out of several packages. For this task you will need the package `web-app-files`. This package contains components for displaying the resources. It also implements the app views "Personal", "Shared with me", "Shared by me" and so on, which can be found under `packages/web-app-files/src/views`.

Your task is to implement a function that will apply a filter that ensures  only  image files (filter by some common image files extensions) are visible in the "Personal" view. 


### Task 3: Control the image filter from the interface

oCIS Web UI elements are taken from the library [ownCloud design system](https://owncloud.design/) (widgets like OcButton, OcCheckbox, etc). You can find examples of their usage in `packages/web-app-files/src/views/SharedWithMe.vue`.

In this task you have to implement a controlling element that allows switching on - or off - the images filter built in 1):
* The element should contain a widget from the aforementioned library and make use of the function from the previous task.
* Depending on the user input it should pass either the normal resources list or the filtered one to the resource table.
* You are free to be creative and implement any other visual indication of the images view in addition to the controlling element.

### Task 4: Bonus

The implemented filter function takes the paginated resources. It means, it filters only the current page. Can you find a way to implement it for the whole file list? Hint: look at the vuex store for files: `packages/web-app-files/src/store` and other customization options for the file list.


### Task 5: Description

* Describe and explain your coding and UX desicions. Where did you place the widget in the interface? Is the "image mode" recognizable as such? 
* Put the description in the README.md file of your repo.

Good luck!

# Stanford Robotics Seminar Website

This is the codebase for the Stanford Robotics Seminar website. Most things should be editable via the settings file (`_config.yml`), the yaml files in the `_data` folder or the markdown files in `_talks`.

## What a new quarter usually involves
- (OK until Spring 2021) Add the upcoming quarter if neeed in `_data/quarters.yml`
- Add the talks in `_talks` (see section below for details)
- Drop thew new syllabus in `assets/doc` (the tex file is also in this repo)
- Update the current list `_data/instructors.yml` and `_data/organizers.yml` as needed (you can add new pictures in `assets/img`)
- Update the following options in `_config.yml` as needed: `displayed-quarters`,`archived-quarters`,`current-syllabus`

## Adding a talk
To add a talk, just add a new file ending in `.md` in the folder `_talks`. Look at other files for an example, but the new talk should have the following fields:

    ---
    speaker: First Last
    affiliation: Some University
    website: "example.com"
    date: 2018-11-16T11:00:00-0800
    location: Building 1
    location-url: "https://campus-map.stanford.edu/?srch=McCullough+115"
    title: "Talk: Title"
    abstract: "The abstract goes here"
    ---

Make sure that fileds containing special characters like ":" are inside quotations like in the example above. The date is in YYYY-MM-DDTHH:MM::SS-0800 format (the last part is the time and -0800 corresponds to the PST time zone).

## Quarters
A list of quarters with start date and end dates is located in `/_data/quarters.yml`. Feel free to add additional quarters there. You can manage which quarter is displayed on the front page by changing `displayed-quarters` in `_config.yml`. You can also control which quarter is shown in the archive by changing `archived-quarters`.

## Organizers
The lists of instructors and organizers can be modified under `_data/instructors.yml` and `_data/organizers.yml` respectively. Add profile pictures of new people in the foler `assets/img`

## Class page
You can update the syllabus by droping the pdf in `assets/doc/Your_Syllabus.pdf` and updating the option `current-syllabus` in `_config.yml`.

## Developing
The whole website was developed using [Jekyl](https://jekyllrb.com/) with the default *minima* theme. Follow the instructions on the Jekyll website to develop more. You can run the website locally by cloning this repo, installing Jekyll and Bundler

    gem install jekyll bundler

and then compiling it

    bundle exec jekyll serve

## Hosting
The website is hosted directly on github via github pages. The hostname `robotics.stanford.edu/seminar/` is managed by the CS department and simply redirects to `stanfordasl.github.io/robotics_seminar/`. Our point of contact in the CS Computer Facilities is Jimmy Wu.

    Jimmy Wu - jimmyw@cs.stanford.edu
    Computer Science Department - Computer Facilities

## Old Website
The old website can be found [here](https://github.com/StanfordASL/robotics_seminar_archive)

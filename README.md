# Certificationy Data

Provide trainings data for [certificationy web platform](https://github.com/ProPheT777/certificationy-web-platform). 

See it in action [certificationy.com](http://www.certificationy.com)

Continuous inspection is available [here](http://www.certificationy.com/github/contribution/inspection), and provided by the web plateform.

# How it work

## Directory structure

```
+-- certification-name (name is related to context.yml
|   +-- context.yml
|   +-- yaml (One folder = one provider type, if we have json data, create json folder)
|     +-- category-of-data.yml
```

## Context

Context provide data about certification. 

Here an example : 

```yaml
name: doctrine2-orm # technical name
icons: devicons-doctrine # icon related to certification @see http://vorillaz.github.io/devicons/#/main
label: Doctrine 2 ORM # label of certification
availableLanguages: [ en ] # available language of certification, not implemented, we currently support only one language
availableLevels: ~ # not implmented yet
customize: #allow user to configure certification before start it
    exclude_categories: true # user can exclude some categories
    number_of_questions: true # user can change the number of questions within categories
threshold: # define rank on certification result. It's just for fun.
    newbie: 30
    beginner: 45
    good: 75
    very_good: 85
    expert: 95
    god: 100
defaults: # Default configuration
    language: en 
    questions_peer_category: 5
```

## Certification data schema

```yaml
category: "Entity Manager"
questions:
    -
        question: "Can you extend from Entity Manager to provide your own ?"
        answers:
            - { value: "No, because it's final class", correct: false }
            - { value: "No, I must rewrite her from scratch", correct: false }
            - { value: "Yes I can, but extend is wrong. Make decoration is the right way.", correct: true }
            - { value: "Yes", correct: false }
    -
        question: "From Entity Manager you can access to"
        answers:
            - { value: "Doctrine Configuration", correct: true }
            - { value: "Doctrine Event Manager", correct: true }
            - { value: "Doctrine Metadata Factory", correct: true }
            - { value: "Doctrine Unit Of Work", correct: true }
            - { value: "Doctrine Entity Factory", correct: false }
```
## Contributing file (`contributing_en.html.twig`)

The main goal of this file is to define some rules and help people to contribute in the right way.

It must contains :
 - git repository to fork
 - folder related to certification
 - rules about contribution
 - warn contributor if the certification is related to an official certification (like symfony2); The goal is only to train no to leak !!!
 
Thanks to all contributors :)
 




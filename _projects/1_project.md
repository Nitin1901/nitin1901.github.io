---
layout: page
title: SCIS Forum
description: A common platform for UoH
img: assets/img/uohyd_logo.png
importance: 1
category: work
---

GitHub - [SCIS Form](https://github.com/nitin-bommi/scis-forum)

Youtube - [Video](https://youtu.be/x0Ox5zY8wUA) 

I, along with my 3 amazing teammates [Yasaswini Tiramdas](https://yashi1011.github.io/), Roopa and Amruta have created this platform for all the university students.

## Back story

The pandemic struct and we moved from in-class to online classes. All the test, the marks, any notifications or even sharing tips were made online. Though there are applications that support these features, we had to use multiple apps to cover up for the diverse tasks. 

## Development

We then gave a thought of developing an integrated common platform for all the university students where they can:
* Upload posts (can vary from job openings to any important notifications) - *twitter*.
* Talk to individuals - *whatsapp*.
* Check any deadlines or post any assignment with deadlines - *calendar*.

These being the primary features, we embedded AI techniques to enhance them. 
* A user can login using both password and `face`.
* When a user creates a post, before storing it, we performed `profanity checks` to clear any unparliamentary words. 

## Success of the project

After several tests, we presented in infront of our board members! They were skeptic about the ethicality of capturing faces. But the model we deployed uses `one-shot learning` that needs only 1 image to identify the person. However, this comes at the cost of more false-negatives (a person may not be identified as the right one). This is an active area of research and we are keeping ourselves and the application up-to-date.

The board suggested a few tests and they were happy about the application! We then deployed it in our university's localhost.

## Tech stack

This project was a combination of our skills from web development, networking, artificial intelligence and software development. We followed `agile` approach where we added new features (*use cases*) in interative manner. Of course, we couldn't leave the use-case diagrams, the sequence diagrams, etc.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/scis_forum_usecase.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The application's use case diagram.
</div>

We used:
* `Python` as our primary programming language.
* `Flask` framework to develop the backend.
* `Javascript` to add calendar feature and to make the website a bit-more interactive.
* `SQLite` database as supported by Flask. 
* `scikit-learn` to build a model that checks the profanity.
* `face-detection` to authenticate users by face.
* `Jinja` for frontend.

## Contribution

This application is not limited to UoH. If you feel your institute needs one, follow the steps given in our [github repository](https://github.com/nitin-bommi/scis-forum) page.

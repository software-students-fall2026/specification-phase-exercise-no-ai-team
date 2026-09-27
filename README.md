# Specification Phase Exercise

A little exercise to get started with the specification phase of the software development lifecycle. In this exercise, your team specifies a set of improvements and new features for [The Slide Machine](https://theslidemachine.com) — see the [instructions](instructions.md) for detail, and the [background](background.md) for an introduction to the software product you are tasked with extending.

## Team members

Daran: dyt2010@nyu.edu | https://github.com/slvrtngd  

Tristan: ttm2041@nyu.edu | https://github.com/Trisolis

Levi: lg4493@nyu.edu | https://github.com/9021007

Robert: rf2789@nyu.edu | https://github.com/rfang1224 

Amitav: an4245@nyu.edu | https://github.com/AmitavNarayan


## Review of the Current Application
Our findings are listed below:  

1 - The app’s decisions about when to create or update a slide are inconsistent; for example, sometimes continued speech produced no new slide, even after a pause. As other examples, repeating a correction after a mistake created a new slide rather than fixing the current one, and speaking for a long stretch only resulted in one slide (weakness).  

2 - The dashboard/display for the API and usage is easily accessible, very clear, and provides an ample amount of detail. The instructor can easily tell whether he/she is running close to any limits on the app (strength).  

3 - The app supports English, French, Spanish, Russian, and Chinese, but other languages like German or Arabic are missing (gap).  

4  - Voice commands have to start their own phrase; for example, saying “Okay, Slide Machine, next” does not work because of the “Okay” and is treated as lecture speech. Having to start with “Slide Machine” every time is difficult and confusing (weakness).  

5 - There is no way to test or adjust the microphone (run a sample sentence, for example) prior to starting the lecture (gap).  

6 - Oftentimes during a live lecture, it’s unclear what the app has done or heard. In particular, after a few seconds of speech the caption text disappeared with no visible change to the deck and the user couldn’t tell which speech would ultimately become slide content. The caption line did not appear for long enough to really help the user (weakness).  

7 - The basic formatting control of the slides is limited. There is no clear way to change font size, move elements around a slide, or manually structure content as tables. The spoken transcript and the slide’s content have to be edited separately (gap).  

8 - When the app captures speech correctly, the content is well-done; the app can accurately display math notation, add helpful definitions, and knows not to duplicate slides when a topic is mentioned again (strength).  

9 - There is no way to search or sort your own lectures and projects. Lectures are always listed newest first (no option for alphabetical order, oldest first, etc.) and require manual rearranging, and you can search through public lectures using Discover, but not your own work specifically (gap).  

10 - The whiteboard tool works well; the instructor has options to immediately draw on the board with a pen, highlighter or an eraser, and slide generation will pause automatically, or he/she can easily create a new whiteboard slide to keep drawings separate. The tool greatly enhances the instructor’s ability to clarify and visualize concepts (strength). 


## Prior Art & Originality
Our Statement:  

We examined the Future Work and Open Questions sections of the Software Design Document, the delivery roadmap, and the repository’s open and closed issues and pull requests. Currently, the Slide Machine does not support video as content, but it includes the option to drag-and-drop slides in a list, and sets alt text for images to one of three default options: caption, slide title, or "Slide Image." Our proposal builds on this work by adding more extensive options for re-ordering and viewing slides and for editing alt text for slide images, and by establishing video as a new kind of content. Importantly, whilst the Software Design Document rules out general-purpose design and free-form graphic design, it emphasizes editing and templating content (potentially with AI’s help), and our proposal is a novel improvement in this regard. 


## Stakeholders

See instructions. Delete this line and replace with the name(s) of the stakeholder(s) you interviewed and lists showing their goals/needs, and problems/frustrations. Note which type of user each stakeholder represents. You may use pseudonyms or partial names to maintain their privacy, but you must privately share their full names and contact information as part of your submission of this exercise

## Product Vision Statement

Our contribution is to improve the post-lecture editing and sharing capabilities of the Slide Machine; we add new features for slide organization, video content, and alternative text, so the resulting deck is complete and accessible.

## User Requirements

User Stories - Instructors

As an instructor, while I’m lecturing, I want the app to suggest videos related to what I’m saying (that I can accept or remove afterwards), so that I don’t have to manually search for relevant videos myself. 
As an instructor, I want to be notified when a video in my lecture has been deleted or privatized, so that I can adjust my slides appropriately for the students. 
As an instructor, I want to add, replace, or remove the video in a slide’s video box, so that I can show the video that best fits my slide/lecture. 
As an instructor, I want to undo a slide re-ordering I made by mistake, so that I don’t have to manually fix the order.
As an instructor, I want to select multiple slides and move them simultaneously, so that I can quickly reorganize a long lecture. 
As an instructor, I want to move a slide to a specific position by typing its number, so that I don't have to manually move it across a long lecture.
As an instructor, I want to move a slide to a different lecture in the same project, so that I can reuse created content without having to repeat work. 
As an instructor, while I’m lecturing, I want the app to suggest alt text that I can accept or modify afterwards, so that creating alt text for images doesn't take a long time.
As an instructor, I want to be given new alt text that I can accept or modify whenever an image is replaced, so that the alt text doesn't describe the wrong image.
As an instructor, I want to mark an image as not needing alt text, so that students can skip pictures that aren’t useful to them.

User Stories - Students
As a student, I want to play a video right on the slide, so that I can follow along with the lecture and its context. 
As a student, I want to turn on captions for a video, so that I'm able to better follow the video and understand its content.
As a student, I want a downloaded PDF of the lecture to include each video's title and link, so that I can still watch the videos from my downloaded copy.
As a student, I want a video to pause when I move to the next slide, so that I don't hear a video interrupting the next slide. 
As a student, I want alt text to read aloud when appropriate, so that I understand the content of the image despite being unable to see or read properly. 
As a student, I want to move to a slide by typing its number, so that I can quickly access specific slides during lecture or while reviewing material. 
As a student, I want to see a list of every slide’s title and jump to any one, so that I can quickly access slides related to a specific topic. 
As a student, I want image alt text to be translated when it’s in another language, so that I’m able to understand the images (via the alt text) properly. 
As a student, I want to know when an image's alt text was AI-generated, so that I know how much to trust it and can ask my instructor if it seems wrong.
As a student, I want to click an image to see its alt text, so that I can clarify the meaning of the image. 



## Activity Diagrams

See instructions. Delete this line and place images of your UML Activity diagrams here, each with the text of the user story it illustrates.

## Wireframes

See instructions. Delete this line and place your wireframe diagrams here, covering every new screen and every existing screen your proposal changes, for every type of user.

## Clickable Prototype

See instructions. Delete this line and place a publicly-accessible link to your clickable prototype here.

## Stakeholder Demo

See instructions. Delete this line and place a link to the deck The Slide Machine generated during your presentation here, after you have presented.

## Exit Ticket

See instructions. Delete this line and place a link to the exit-ticket quiz you generated from your demo deck and distributed to the class, along with a short note on what — if anything — you had to correct in the generated questions before publishing.

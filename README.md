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

We examined the Software Design Document, delivery roadmap, repository issues, and pull requests to identify related existing and planned functionality. The current application already supports drag-and-drop slide reordering and automatically assigns image alt text using one of three options: caption, slide title, or “Slide Image.” Video is not currently supported as slide content.

Our proposal extends these existing capabilities by allowing instructors to move slides directly to a specified position, edit image alt text, and add video content to slides. These changes build on existing content-editing functionality without introducing general-purpose graphic design, which is outside the scope identified in the Software Design Document.

## Stakeholders

### Instructors

**Instructor A**
- Goals: Wants slides that are easy to read and uncluttered; wants proper mathematical notation/symbols for math content; wants slides clear and descriptive enough for students to follow the lecture from reading alone; wants quizzes that challenge students and promote critical thinking.
- Frustrations: The app didn't include graphs (e.g. binomial distributions) despite math-heavy content; generated quiz answer choices were too similar to each other and ambiguous; little to no LaTeX/math notation support; slides were generated in the wrong order, with title slides appearing mid-lecture.

**Instructor B**
- Goals: Wants slides that summarize lecture content using bullet points rather than paragraphs; wants all important definitions prioritized; wants images relevant to specific concepts (e.g. cinematography shots); wants the ability to link videos.
- Frustrations: Slides didn't clearly pinpoint the lecture's main topic; generated quizzes occasionally had inaccurate answers; wanted the option to use their own recorded voice for playback instead of a robotic voice; no images or videos were shown related to the lecture content.

**Instructor C**
- Goals: Wants the ability to add YouTube videos to slides; wants the ability to add alt text to images; wants a wider selection of themes, including the ability to set and actually apply a default theme.
- Frustrations: Slides did not accurately convey the lecture's content; text editing did not support click-to-place cursor; reordering slides required painful one-by-one dragging; the "API ok" indicator was confusing and distracting; found the overall site unintuitive and visually unappealing.

### Students

**Student A**
- Goals: Wants slides that include all relevant lecture information without omissions; wants the ability to download personal copies of slides to edit/comment on for studying; wants quiz questions that promote critical thinking rather than easily-searchable facts; wants all images/graphs referenced in the lecture included on slides.
- Frustrations: No easy way to download slides for personal annotation; quiz questions focused on obscure details rather than the most relevant topics; slide content wasn't specific enough for someone unfamiliar with the topic; images/graphs referenced during the lecture were missing from slides.

**Student B**
- Goals: Wants slide content specific and detailed enough to understand topics fully; wants sufficient context provided alongside content; wants quiz questions that help prepare for actual exams; wants the ability to reformat slides for better readability.
- Frustrations: Some slide text had poor grammar or unclear wording; quiz questions were too specific and didn't encourage critical thinking; slides didn't make the lecture's main topic explicit; missing images made some concepts hard to understand.

**Student C**
- Goals: Wants a wider selection of visual themes and slide transitions to stay engaged; wants image descriptions provided; wants the ability to easily identify image sources; wants an intro/conclusion slide generated automatically.
- Frustrations: Improperly-fitted images showed distracting gray borders; didn't notice the small "i" icon indicating image source; found the current visual style "painfully boring, bleak," and wanted a more polished look; would find embedded YouTube videos useful.

### Synthesis: Patterns Across Interviews

Clustering the goals/frustrations above by frequency surfaced several recurring patterns: content clarity/accuracy (5/6), missing visual content like images and graphs (4/6), quiz quality (4/6), desire for video support (3/6), manual editing/control limitations (3/6), and slide reordering specifically (2/6). Image alt text and aesthetics/theming each appeared in 2/6 interviews.

### Feature-to-Evidence Mapping

| Proposed feature | Evidence |
|---|---|
| Slide reordering | Instructor C requested easier slide reordering, our application review also found that reordering slides was awkward and required manual dragging. |
| Video support | Instructor B wanted the ability to link videos, Instructor C wanted YouTube videos on slides, and Student C identified embedded YouTube videos as useful. |
| Editable image alt text | Instructor C explicitly requested the ability to add alt text to images, and Student C wanted image descriptions and clearer access to image information. |
| Speaker notes | Instructor B wanted additional context associated with lecture content, which motivates giving instructors a way to provide additional information beyond the main slide content. |
| Bottom-bar / transcription changes | Our application review found that the live transcription display was unclear and disappeared too quickly. Instructor C also identified interface and usability issues with the existing presentation experience. |
| Clearer account entry / authentication | Our application review identified usability issues around the application's entry workflow, pushing us to make changes towards a simpler "Get Started" path and reduced friction when returning to the application. |

## Product Vision Statement

Our contribution is to improve the post-lecture editing and sharing capabilities of the Slide Machine; we add new features for slide organization, video content, and alternative text, so the resulting deck is complete and accessible.

## User Requirements

### User Stories - Instructors (13)

1. As an instructor, while I’m lecturing, I want the app to suggest videos related to what I’m saying (that I can accept or remove afterwards), so that I don’t have to manually search for relevant videos myself. 
2. As an instructor, I want to add, replace, or remove the video in a slide’s video box, so that I can show the video that best fits my slide/lecture. 
3. As an instructor, I want to move a slide to a specific position by typing its number, so that I don't have to manually move it across a long lecture.
4. As an instructor, while I’m lecturing, I want the app to suggest alt text that I can accept or modify afterwards, so that creating alt text for images doesn't take a long time.
5. As an instructor, I want to write or edit the alt text for any image, so that I can modify the results of AI-generated alt text as required for specific situations.
6. As an instructor, I want to mark an image as not needing alt text, so that students can skip pictures that aren’t useful to them.
7. As an instructor, I want to add private speaker notes to any slide, so that I have reminders and talking points visible only to me during the lecture.
8. As an instructor, I want to edit or delete speaker notes after they're created, so that I can revise my talking points as my lecture plan changes.
9. As an instructor, I want the option to make a slide's speaker notes visible to students, so that I can share extra context when it's useful for review.
10. As an instructor, I want the live transcription display removed from the bottom of the screen during lecture, so that it doesn't distract me or disappear before I can read it.
11. As an instructor, I want an alternative, less intrusive way to confirm the app is capturing my speech (without the current bottom bar), so that I still have feedback the system is working.
12. As an instructor, I want a single clear "Get Started" option on first visit, so that I'm not confused about whether to sign in or create an account.
13. As an instructor, I want to be logged in automatically after my first session, so that I don't have to repeatedly choose between sign-in and account creation.

### User Stories - Students (16)

1. As a student, I want to play a video right on the slide, so that I can follow along with the lecture and its context. 
2. As a student, I want to turn on captions for a video, so that I'm able to better follow the video and understand its content.
3. As a student, I want a downloaded PDF of the lecture to include each video's title and link, so that I can still watch the videos from my downloaded copy.
4. As a student, I want a video to pause when I move to the next slide, so that I don't hear a video interrupting the next slide. 
5. As a student, I want to see a video's title and link when it is removed or broken (and an instructor hasn't fixed it), so that I can view the video in all circumstances. 
6. As a student, I want alt text to read aloud when appropriate, so that I understand the content of the image despite being unable to see or read properly. 
7. As a student, I want to move to a slide by typing its number, so that I can quickly access specific slides during lecture or while reviewing material. 
8. As a student, I want to see a list of every slide’s title and jump to any one, so that I can quickly access slides related to a specific topic. 
9. As a student, I want image alt text to be translated when it’s in another language, so that I’m able to understand the images (via the alt text) properly. 
10. As a student, I want to know when an image's alt text was AI-generated, so that I know how much to trust it and can ask my instructor if it seems wrong.
11. As a student, I want to click an image to see its alt text, so that I can clarify the meaning of the image. 
12. As a student, I want to see speaker notes only on slides where the instructor has chosen to share them, so that I get extra context without seeing notes meant to be private.
13. As a student, I want a cleaner slide view without a distracting bottom bar during playback, so that I can focus on the slide content itself.
14. As a student, I want captions (if enabled) displayed in a way that doesn't disappear too quickly, so that I can actually read them while following along.
15. As a student, I want the same clear "Get Started" entry point, so that account setup doesn't require guessing which option applies to me.
16. As a student, I want to be recognized and logged in automatically, so I can get straight to viewing lecture content.

## Activity Diagrams

Our activity diagrams illustrate the primary workflows for each major feature area. Diagram 1 covers slide reordering; Diagram 2 covers speaker notes; Diagram 3 covers video playback; and Diagram 4 covers image alt text. The remaining user stories describe additional behaviors and variations within these feature areas, including captions, video failure states, PDF behavior, navigation, and authentication.

### Instructor Diagrams

#### Diagram 1: Move a Slide to a Specific Position

**User story:** As an instructor, I want to move a slide to a specific position by typing its number, so that I don't have to manually move it across a long lecture.

![Activity diagram: moving a slide by typing its position number](Instructor-Reordering-Slides.png)

Starting from the slide list in the lecture editor, the instructor selects a slide and enters a target position number. The system checks whether the number is valid: an invalid entry shows an error and lets the instructor try again, and cancelling returns to the slide list with nothing changed. On a valid entry the slide moves to the new position and all affected slides are renumbered.

#### Diagram 2: Add, Edit, and Share Speaker Notes

**User stories:**
- As an instructor, I want to add private speaker notes to any slide, so that I have reminders and talking points visible only to me during the lecture.
- As an instructor, I want to edit or delete speaker notes after they're created, so that I can revise my talking points as my lecture plan changes.
- As an instructor, I want the option to make a slide's speaker notes visible to students, so that I can share extra context when it's useful for review.

![Activity diagram: adding, editing, and sharing speaker notes](Instructor-Speaker-Notes.png)

From a slide in the lecture editor, the instructor adds speaker notes, which are private by default. They can later edit or delete the notes, and can choose to share a slide's notes with students. 

### Student Diagrams

#### Diagram 3: Play a Video on a Slide with Captions

**User story:** As a student, I want to play a video right on the slide, so that I can follow along with the lecture and its context.

![Activity diagram: playing a slide video](Student-Play-Video.png)

The student scrolls to a slide with at least one video. Among the videos which have loaded properly,
the student plays a video, and is able to watch it (network errors notwithstanding).

#### Diagram 4: View an Image's Alt Text

**User story:** As a student, I want to click an image to see its alt text, so that I can clarify the meaning of the image.

![Activity diagram: viewing an image's alt text](Student-Alt-Text.png)

While viewing a slide, the student clicks an image. The system first checks whether alt text is available/the instructor has marked the image as decorative, in which case a display message stating 'no alt text exists' pops up. Otherwise, alt text is displayed, with an "AI-generated" label when applicable. The student dismisses the alt text to return to the slide. 


## Wireframes

[Wireframes view](https://www.figma.com/design/MbmQkDATafc26n74g5i85L/Wireframe---no-ai-team?node-id=0-1&t=OWL8q17dJJD8U8ua-1)

## Clickable Prototype

[Clickable prototype](https://www.figma.com/proto/MbmQkDATafc26n74g5i85L/Wireframe---no-ai-team?node-id=128-13&p=f&t=OWL8q17dJJD8U8ua-0&scaling=scale-down&content-scaling=fixed&page-id=0%3A1&starting-point-node-id=128%3A13&show-proto-sidebar=1)

## Stakeholder Demo

See instructions. Delete this line and place a link to the deck The Slide Machine generated during your presentation here, after you have presented.

## Exit Ticket

See instructions. Delete this line and place a link to the exit-ticket quiz you generated from your demo deck and distributed to the class, along with a short note on what — if anything — you had to correct in the generated questions before publishing.

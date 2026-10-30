QRIOUS Quiz Control Centre

A browser-based control centre for Viraj International School's inter-house quiz competition. It brings questions, a countdown timer and team scores together on one screen for the Quiz Master and audience.

The four default houses are Agni, Jal, Prithvi and Vayu. The initial question bank contains editable placeholders for seven rounds.

Features

Show a question and reveal its answer when the Quiz Master is ready.

Start, pause and reset a countdown timer; play a sound when time is up.

Record scores for each house, display current-round and overall totals, and undo the last score change.

Show a round-by-round score table and final results.

Move to the previous or next question, or jump to the next round.

Add, edit, delete and reorder questions in the question manager.

Export the question bank as a JSON file.

Switch between Quiz Master and audience views and use full-screen mode.

Save the question bank, scores and event state in the browser's local storage.

Manually announce which house buzzed first.

Requirements

A modern browser such as Chrome or Microsoft Edge.

A computer connected to the projector and speakers for the event.

JavaScript and local storage enabled in the browser.

The app is a standalone HTML file. It does not require a server, database, installation or internet connection after the file has been downloaded. The school emblem is embedded in the HTML.

Run locally

Download the HTML file from this repository.

Open quiz-control-centre-updated (5).html in Chrome or Edge. If you rename it to index.html, open that file instead.

Use the controls on the right to prepare the quiz.

For GitHub Pages, place the HTML file in the repository root as index.html, enable Pages in the repository settings, and select the branch and root folder containing that file. The site will use the published URL shown in the Pages settings.

Preparing the quiz

Click Edit / import questions in the Question bank section.

Replace the placeholder text with your questions and answers. Set the round and time for each question.

Use Add question, Delete, and the up/down buttons to organise the list. Keep questions for the same round together so Next round jumps to the expected place.

Click Save questions and confirm the replacement. Saving a changed question bank resets existing event scores, so finish preparing before the competition.

Click Export quiz JSON to download a copy of the questions. This export contains the question bank, not the score history. The current visual editor does not provide a JSON file import button.

Running the event

Connect the projector and speakers. Open the app in the browser and check the sound.

Use Previous, Next, or Next round to select a question.

Check the time in the seconds field and click Start timer. Click it again to pause, or use Reset timer to set it back.

At zero, the app displays TIME UP and plays a sound. The question remains on screen until you move on.

Click Reveal answer when you are ready to show or hide the answer.

Set the Correct and Wrong values as needed, then use the house buttons to update the score. Defaults are +10 and −5. Scores are applied manually; change the correct value to 5 for a five-point round.

Use Undo score if you make a scoring mistake. Select Final results when the competition ends.

Use Audience view to hide the control panel and Quiz master view to bring it back. The audience sees the same browser window, so return to Quiz Master view whenever you need to operate the controls. Full screen expands the page.

Buzzer note

The Manual buzzer result buttons let an operator announce a house on screen. This HTML file does not receive live buzzer presses from team phones or synchronise devices over Wi-Fi. A separate networked buzzer application would be needed for that workflow.

Data and practical notes

Data is stored locally in the browser, on the same computer and browser profile. It is not shared across devices or backed up to GitHub.

Clearing site/browser data, using a different browser profile or switching from a local file to a hosted site can leave saved data unavailable. Export questions before the event and keep a separate written score backup.

Reset event clears scores and returns to the first question while retaining the question bank. Confirm carefully before resetting.

Audio depends on browser permissions, system volume and the selected speaker output. Test on the actual auditorium setup.

The displayed final ranking orders teams by score; handle tied scores according to your competition rules.

Technology

Built with HTML, CSS and vanilla JavaScript, using browser local storage and the Web Audio API. All app code is contained in the HTML file.

Repository contents

README.md
quiz-control-centre-updated (5).html  # Application (rename to index.html for Pag

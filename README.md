# 🏆 QRIOUS Quiz Control Centre

### Viraj International School | Inter-House Quiz Competition

A browser-based quiz management application that brings **questions, countdown timers, answers and house scores** together in one place.

Designed for school quiz competitions, QRIOUS helps the Quiz Master conduct each round smoothly while keeping scores visible to the audience.

> **Ready to use offline:** Download the HTML file and open it in a modern web browser. No installation, server or database is required.

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Default Houses](#-default-houses)
- [Getting Started](#-getting-started)
- [Preparing the Quiz](#-preparing-the-quiz)
- [Conducting the Competition](#-conducting-the-competition)
- [Scoring Guide](#-scoring-guide)
- [Audience and Quiz Master Views](#-audience-and-quiz-master-views)
- [Manual Buzzer](#-manual-buzzer)
- [Saving and Backup](#-saving-and-backup)
- [Deploying with GitHub Pages](#-deploying-with-github-pages)
- [Troubleshooting](#-troubleshooting)
- [Technology](#-technology)
- [Repository Structure](#-repository-structure)

---

## 🎯 Overview

QRIOUS Quiz Control Centre is a single-file web application for managing an inter-house quiz.

It allows the operator to:

1. Prepare and organise questions.
2. Display questions to participants and the audience.
3. Run a countdown timer.
4. Reveal answers at the right moment.
5. Record scores for each house.
6. Review round-wise scores and final results.

The initial question bank contains **editable placeholder questions for seven rounds**.

---

## ✨ Features

### 📝 Question management

- Add, edit and delete questions.
- Arrange questions using the up and down controls.
- Set the round and time for each question.
- Display a question and reveal or hide its answer.
- Export the question bank as a JSON file.

### ⏱️ Countdown timer

- Start, pause and reset the timer.
- Set the time in seconds.
- Display **TIME UP** when the countdown ends.
- Play an alert sound when time is up.

### 🏠 House scoring

- Keep scores for all four houses.
- Display current-round and overall totals.
- Set the points awarded for correct and wrong answers.
- Undo the most recent score change.
- View a round-by-round score table and final results.

### 🎮 Quiz controls

- Move to the previous or next question.
- Jump to the next round.
- Switch between Quiz Master and audience views.
- Use full-screen mode for projection.
- Announce the first house to buzz using manual controls.

### 💾 Local storage

- Save the question bank, scores and event state in the browser.
- Reopen the application in the same browser profile to access its locally saved data.

---

## 🏠 Default Houses

| House | Name |
|:---:|---|
| 🔥 | Agni |
| 💧 | Jal |
| 🌍 | Prithvi |
| 🌬️ | Vayu |

---

## 🚀 Getting Started

### Requirements

- A modern browser such as **Google Chrome** or **Microsoft Edge**.
- JavaScript and browser local storage enabled.
- A computer connected to a projector or display for the audience.
- Speakers connected to the computer for the timer alert.

### Run the application

1. Download the application HTML file from this repository.
2. Open:

   ```text
   quiz-control-centre-updated (5).html
   ```

3. The application will open in your browser.
4. Use the controls to prepare and conduct the quiz.

You may rename the application file to `index.html` if you prefer a shorter filename or want to publish it using GitHub Pages.

> **Offline use:** Once the HTML file has been downloaded, the application can run without an internet connection.

---

## 🛠️ Preparing the Quiz

Complete these steps before the competition begins.

### 1. Open the question editor

In the **Question bank** section, click:

```text
Edit / import questions
```

### 2. Replace the placeholders

Enter your own:

- Questions
- Answers
- Round details
- Time limits

### 3. Organise the question order

Use the available controls to:

- Add a question.
- Delete a question.
- Move a question up or down.

Keep questions from the same round together so that **Next round** jumps to the expected place.

### 4. Save the question bank

Click **Save questions** and confirm the replacement.

> ⚠️ **Important:** Saving a changed question bank resets existing event scores. Prepare and save the questions before the competition starts.

### 5. Export a backup

Click **Export quiz JSON** to download a copy of the question bank.

> The JSON export contains the question bank, not the score history. The current visual editor does not provide a JSON file import button.

---

## 🎤 Conducting the Competition

### Step 1: Set up the venue

1. Connect the computer to the projector or display.
2. Connect the speakers.
3. Open the application.
4. Check that the questions, answers and rounds are in the correct order.
5. Test the timer sound and volume.

### Step 2: Display a question

Use:

- **Previous** to return to the previous question.
- **Next** to move to the next question.
- **Next round** to jump to the next round.

### Step 3: Start the timer

1. Check the time in the seconds field.
2. Click **Start timer**.
3. Click the timer control again to pause it if necessary.
4. Use **Reset timer** to set it back.

When the timer reaches zero:

- **TIME UP** appears.
- An alert sound plays.
- The question remains on screen until the operator moves on.

### Step 4: Reveal the answer

Click **Reveal answer** when the Quiz Master is ready. Use the control again to hide the answer.

### Step 5: Update the scores

Set the appropriate values for **Correct** and **Wrong**, then use the house scoring buttons to apply the result.

### Step 6: Show the final results

After the last round, select **Final results** to display the standings.

---

## 🧮 Scoring Guide

Scoring is controlled manually by the operator.

The default values are:

| Result | Default score |
|---|---:|
| Correct answer | +10 |
| Wrong answer | −5 |

You can change the values to match the rules of each round.

### Example: A five-point round

If a correct answer is worth five points:

1. Change the **Correct** value to `5`.
2. Select the appropriate house scoring button when an answer is correct.
3. Adjust the **Wrong** value according to your competition rules.

### Correcting a mistake

If the wrong score is entered, use **Undo score** to reverse the most recent score change.

> Final rankings are ordered by score. Decide and announce your competition’s tie-breaking rules separately.

---

## 🖥️ Audience and Quiz Master Views

### Quiz Master view

Use this view to operate the quiz, including:

- Selecting questions and rounds.
- Starting or resetting the timer.
- Revealing answers.
- Updating scores.
- Managing the question bank.

### Audience view

Use **Audience view** to hide the control panel while displaying the quiz to participants and the audience.

Click **Quiz master view** to bring the controls back.

> Both views use the same browser window. When you return to Quiz Master view, the controls will also be visible on the projected display.

Use **Full screen** to expand the page for the event.

---

## 🔔 Manual Buzzer

The **Manual buzzer result** controls allow the operator to announce which house buzzed first.

This application does **not** receive live buzzer presses from team phones or synchronise devices over Wi-Fi. A separate networked buzzer system would be required for that setup.

---

## 💾 Saving and Backup

### How data is stored

The application stores the question bank, scores and event state in the browser’s **local storage**.

The saved data belongs to the browser and profile being used. It is not automatically:

- Shared with another computer.
- Synchronised between browsers.
- Backed up to GitHub.

### Recommended event backup

Before the event:

1. Export the question bank as JSON.
2. Keep a separate copy of the HTML file.
3. Test the application on the actual event computer.

During the event:

1. Keep a written or separate score backup.
2. Avoid clearing browser data.
3. Avoid changing the browser or browser profile.

> Switching from a local HTML file to a hosted website may make previously saved data unavailable because the browser treats them as different locations.

### Resetting the event

**Reset event** clears scores and returns to the first question while retaining the question bank.

Use it carefully and confirm the action only when you are ready to reset the competition.

---

## 🌐 Deploying with GitHub Pages

GitHub Pages can make the application accessible through a web link.

### Step 1: Rename the application file

Rename:

```text
quiz-control-centre-updated (5).html
```

to:

```text
index.html
```

### Step 2: Place the files in your repository

Your repository should contain:

```text
your-repository/
├── index.html
└── README.md
```

### Step 3: Enable GitHub Pages

1. Open your repository on GitHub.
2. Go to **Settings**.
3. Select **Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select the branch containing `index.html`, commonly `main`.
6. Select the root folder.
7. Click **Save**.

GitHub will display the published website address in the Pages settings once the site is available.

> The hosted application still stores data locally in each visitor’s browser. Publishing it does not create a shared online scoreboard.

---

## 🩺 Troubleshooting

### The timer sound is not playing

- Check the computer’s volume.
- Confirm that the correct speaker output is selected.
- Check browser audio permissions.
- Test the sound after interacting with the page.
- Test the complete setup on the event computer before the competition.

### My questions or scores are missing

- Make sure you are using the same computer, browser and browser profile.
- Check whether browser data was cleared.
- Check whether you switched from the local file to the hosted version, or vice versa.
- Refer to your exported question bank and separate score backup.

### The next round is not opening where expected

Keep questions from each round together in the question editor, then save the question bank before starting the event.

> Saving a changed question bank resets existing scores.

### The audience can see the controls

Select **Audience view** to hide the control panel. Remember that switching back to Quiz Master view will show the controls in the same projected browser window.

### The scoreboard is not updating on another computer

Scores are stored locally in the browser. Separate computers do not automatically share or synchronise event data.

---

## 💻 Technology

| Technology | Purpose |
|---|---|
| HTML | Application structure |
| CSS | Layout and visual design |
| Vanilla JavaScript | Quiz controls and scoring |
| Browser local storage | Local saving of quiz and event data |
| Web Audio API | Timer alert sound |

The school emblem and application code are embedded in the standalone HTML file.

---

## 📁 Repository Structure

```text
your-repository/
├── README.md
└── quiz-control-centre-updated (5).html
```

For GitHub Pages, the application file can be renamed:

```text
your-repository/
├── README.md
└── index.html
```

---

<p align="center">
  <strong>VIRAJ INTERNATIONAL SCHOOL</strong><br>
  QRIOUS • Inter-House Quiz Competition
</p>
````

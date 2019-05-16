# Homework 6: Plan verification

## 1\. IntroOutro Handler

### 1.1

- **Requirement**: Once the game has begun, regardless, of the fact that the player is in vertical view or horizontal view the question and action buttons will repositions itself to fit both screen displays.

- **Verification Plan**: In terms of verifying that this requirement is met, we will be utilizing user testing. This will be done towards the end when the game, question bank, user database is set up. Veronica, Yiran and Rhea will play the game from the beginning and test whether the application positions and sizes each screen and the buttons correctly, whilst Jin will act as the organizer. We will then rotate roles until everyone has acted as the organizer to ensure that the interface responds across different devices and performs on more than one occasion. Similarly, we will be testing on different browsers to make sure that the game behaves the same across different platforms.

During the user testing, if one of the users notice that there is a bug. For instance, Yiran may report that when she uses her Android phone the buttons are not correctly sized and oriented in the right direction. We will document this in Git Issues and assign someone responsible to fix this issue. This particular section of code will be analyzed by using the Developer Tools feature on Chrome. Rhea or Jin will inspect the CSS and make sure that the requirement is met.

## 2\. Question Manager

### 2.1

- **Requirement**: Players are able to choose the answer to the question through a single action.
- **Verification Plan**: To verify this requirement, we will conduct user testing. This will be done once the questionBank, user manager, room manager and game manager is set up. Veronica, Yiran and Jin will act as participants in the game, whilst Rhea will be the organizer. When the game has started, the players will choose their answers and Rhea will record the answers we have chosen on a piece of paper. Once the game is finished, Rhea will cross reference the answers recorded to the answers sent to the database. Rhea will make sure that the answers match the person who chose it. We will do this across all genres, including custom questions, whilst rotating roles. We will do this until we have completed all the genres. Additionally, we will alternate between playing a single game and restarting a game to see if the answers are recorded correctly.

During the user testing, if one of the users notice that there is a bug. For example, Jin may report that when she uses her Apple phone, her answer is not recorded for question 3\. We will document this in Git Issues and assign someone responsible to fix this issue. This particular section of code will be analyzed by using the Developer Tools feature on Chrome. Rhea or Jin will inspect the CSS and make sure that the requirement is met.

### 2.2

- **Requirement**: The Organizer can create their own questions. After clicking on the customize option, the organizer will be directed to a screen with a card deck. Each card deck will have an input box for the organizer to type in their question. There is no limitation on what the organizer can type in as the question.
- **Verification Plan**: To verify this requirement, we will conduct user testing. This will be done once the questionBank, user manager, room manager and game manager is set up. Each teammate will be organizers and click on the custom category. We will then input a variety of questions, including special characters, numbers and other languages. We will each then check in the database to see if the questions have been stored accurately. If the questions have been successfully stored, then we will start to rotate being players and organizers to test that the custom questions are appearing appropriately. If one of us notices a defect, we will record this in Git issues and assign someone responsible to fix this issue. This particular section of code will be analyzed by using the Developer Tools feature on Chrome. Rhea or Jin will inspect the CSS to make sure that the requirement is met. If the questions are not successfully stored, the same procedure will follow.

### 2.3

- **Requirement**: Organizer is able to choose the number of questions will appear in a single game, the minimum is 5 and the maximum is 15\. The default is 10.
- **Verification Plan**: To verify this requirement, we will conduct user testing. This will be done once the questionBank, user manager, room manager and game manager is set up. Each member of the team will rotate as organizer and participant. The person acting as organizer will first start the game as the default number, 5 questions. The participants will play the game till the end and confirm that 5 questions have been shown. Then, the next organizer will change the number of questions shown and the participants will play the game till the end and confirm the number of questions shown. We will repeat this across different devices and browsers, including MacBooks, HP computers, Chrome, Safari, Firefox. If one of us notices a defect, we will record this in Git issues and assign someone responsible to fix this issue. This particular section of code will be analyzed by using the Developer Tools feature on Chrome. Rhea or Jin will inspect the code to make sure that the requirement is met.

## 3\. Room Manager

### 3.1

- **Requirement**: When the user types in an incorrect room number, an error message appears and prompts the user to input the correct room number.
- **Verification Plan**: The team members will test this by inputting invalid room codes and see if the error message appears. We will perform regression tests by continually inputting invalid room codes 5 times and then input a valid one and see if the program allows the user to proceed. We chose the number 5 because after the user realizes they have mistakenly typed an incorrect room code, they are less likely to make a mistake with increasing tries. We decided that 5 times is sufficient to cover the majority of user's experiences in typing the correct code. Additionally, since we implemented a sharing feature to easily share room codes and allow the code to be copied to the clipboard quickly, it is even less likely for users to type in the code manually. We will test this across different devices and browsers. If one of us notices a defect, we will record this in Git issues and assign someone responsible to fix this issue. This particular section of code will be analyzed by using the Developer Tools feature on Chrome. Rhea or Jin will inspect the code to make sure that the requirement is met.

### 3.2

- **Requirement**: There must be at least two people including organizer in the room to start the game. If the Organizer presses "Start Game" without having at least two people then, an error message will show and prompt the Organizer to begin when they have enough people.
- **Verification Plan**: We will run automated tests on starting a game with no participants, one participant, two participant, and five participants. We will create and run three different Jest tests that examines these three different cases. These tests case will be check if there is greater than or equal to two participants (not inclusive). If the tests return a boolean value 'true' then, the test will have passed however, if it returns false it will have failed.

### 3.3

- **Requirement**: If players try to join a game while it has begun, they will be denied and be shown am error message.
- **Verification Plan**: We will conduct a walkthrough to evaluate this specific requirement and attempt to identify defects. The walkthrough process will be carried out by a walkthrough team, which will be led by Veronica. The leader will be responsible for management the task associated with the walkthrough -- trying to join a room in game.

The specific responsibilities of the leader include: prepare and set up the walkthrough, informing all participants of the date, place, and agenda of walkthrough meetings, distribution of the review elements to all participants before walkthrough meetings, chairing the walkthrough meeting, and issuing the walkthrough report. Jin and Rhea will be responsible for the production of the review elements, and for presenting them at the walkthrough meeting. They are also responsible for writing tests and self-review the review elements before walkthrough meeting. Tests may includes: testing the state of a react component at every point (white-box testing), and verifying what the component is being rendered (black-box testing), etc. Yiran will examine review components, review errors and recommend solutions.

The walkthrough process will consist of the two activities: preparation and review meeting. The walkthrough report should contain: an identification of the review element, a list of changes and defects noted during the walkthrough, a list of actions, with persons responsible identified and expected dates for completion defined, and recommendations made by the walkthrough team on how remedy defects and dispose of unresolved issued. Further walkthrough meetings might be needed for further verification.

## 4\. Game Manager

### 4.1

- **Requirement**: When the organizer clicks on the button to cancel the game, there will be an alert message confirming that they would like to cancel the game. This requires the organizer to click another button to return back to the game or cancel the game.
- **Verification Plan**: In order to verify this requirement, our team will be doing user testing after the game, question bank, user database is set up. Rhea, Veronica, and Yiran will play the game as players while Jin will be the organizer. Each user will rotate the role of organizer to demonstrate that this requirement is duplicated and verified. After pressing the "Start Game" button and the first question appears each organizer will test the cancel button and check if an alert message displays. Similarly, they will do this process twice, one to return back to the game and the other to cancel the game.

If there is a bug reported by any of the users then, the bug and the steps to reproduce that bug will be documented as a git issue. To ascertain that this requirement is met, Rhea or Jin will inspect the JavaScript code pertaining to alerting the organizer when they would like to leave the game.

### 4.2

- **Requirement**: Organizer is able to see how many people answered the question at all times through a number counter on their screen.
- **Verification Plan**: To test this particular behavior we will be using manual testing, particularly user testing to determine whether this requirement has been met. Veronica, Yiran, Rhea will take on the role of players while Jin will take on the role of the organizer. Each team member will exchange roles to ascertain that the requirement behavior is met and reflected regardless of the browser time or device. Once the organizer has pressed "Start Game" and the first question has appeared on each player's screen the organizer will verify that it displays how many players have answered the question. Similarly, while testing this behavior we will open Developer Tools to inspect the JavaScript code and the console to determine whether the requirement has been met.

### 4.3

- **Requirement**: After the organizer has adjusted their preferred settings, they may navigate to the category page by a single action.
- **Verification Plan**: Our team will first run automated Jest tests that will check whether the organizer's preferences were correctly set or not. This will be done by creating a set of dummy preferences and will be configured together with the new room via JavaScript. If the room contains these dummy settings then, it will return a boolean value 'true' however, if it does not it will return false. If the value returned is true then it will have passed the test conversely, if it returns false then the test will have failed.

To verify that the organizer can navigate to the category page, our team will manual test that behavior. Furthermore, we will monitor the HTML via developer tools to check that the navigation is correct.

### 4.4

- **Requirement**: Organizer can enable the timer option used during discussion time in the room settings. The Organizer inputs only number value into the text field and it does not accept text or special characters. When the Organizer clicks the "Discussion Time" button the timer will countdown and when it reaches zero the "next" button will appear allowing the Organizer to move to next question.
- **Verification Plan**: Our team will create several unit tests that will check whether the timer option was set. This will done by first sending a tester timer value and the unit test will examine whether the Firebase has correctly stored that value or not. If the return value is true, it will have passed the automated test. Likewise, if it has returned false, it will have failed the test. This test will mainly examine the JavaScript code for configuring that particular setting.

In order to determine whether the timer actually initiates, our team will use black-box testing particularly system testing and functional testing. By using this test method our team will be able to verify that the requirement is met and works as designed. If the test throws an error then the test will have failed otherwise, it will have passed the test.

--------------------------------------------------------------------------------

Reference: ESA PSS-05-10 (Issue-1) (Revision-1), [Guide to Software Verification and Validation](https://www.mobilefish.com/download/webdevelopment/pss-05-10.pdf). (1995, March).

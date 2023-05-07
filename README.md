Download Link: https://assignmentchef.com/product/solved-itis-cs-5180-assignment3-student-registration-form
<br>
In this assignment you will get familiar with intents and how to pass data between multiple activities. You are required to develop an “Student registration form” application that enables a new student to enter and edit their information. This assignment is composed of three activities namely: Main Activity, Display Activity and Edit Activity.

(a) Main Activity                                         (b) Clicking Submit button

<strong>Figure 1, Main Activity</strong>

<h2>Part 1 ): Main Activity</h2>

This is the main launching activity where the user enters their information. The interface should be created to match the user interface (UI) presented in Figure 1. To build the UI, please follow the following tasks: 1. Use the following components

<ul>

 <li>EditText for name and email address</li>

 <li>Radio buttons for your department (SIS, CS, BIO, Others)</li>

 <li>Seek Bar for current mood</li>

 <li>Button for the submitting information</li>

</ul>

<ol start="2">

 <li>Create a <strong>Student</strong> class consisting of five variables: name, email, department, and mood. The Student class should implement the Serializable or Parcelable interface.</li>

 <li>Upon clicking the submit button, the information should be retrieved from the form and populated in a Student object. If there are any missing entries, the user should be alerted by displaying a Toast message. If all the entered information is complete, create an <strong><em>explicit intent</em></strong>, start the Display Activity and pass it the <strong>Student object</strong> as part of the <strong><em>extras</em></strong>.</li>

</ol>

(a) Display Activity                                          (b) Clickable edit icon

<strong>Figure 2, Display Activity</strong>

<h2>Part 2 : Display Activity</h2>

This activity displays the student information entered in the Main Activity and allows the user to select which information item to edit. The interface should be created to match the user interface (UI) presented in Figure 2. To build the UI, please follow the following tasks:

<ol>

 <li>This activity is started by the Main Activity. When the Display Activity is created it should receive the Student object sent from the Main Activity in the intent’s extras.</li>

 <li>Display the student information as shown in Figure 3(a). Note that beside each displayed item there is an edit icon (ImageView). Clicking the edit icon beside an information item should start the Edit Activity (See Figure 3(b)). You are provided with the edit icon image. Perform the following requirements:

  <ol>

   <li>The Edit Activity should be started using an <strong><em>implicit intent</em></strong>. Send all the required information to the Edit Activity using <strong><em>extras</em></strong>.</li>

   <li>The Edit Activity should be <strong><em>started for result</em></strong>, as it is expected to send back the edited information to the Display Activity. Upon receiving a result from the Edit Activity, the Display Activity should update the displayed student information to reflect the edited information.</li>

  </ol></li>

</ol>

<h2>Part 3 : Edit Activity</h2>

This activity enables the user to edit the information item selected in the Display Activity and should send back the updated information to the Display Activity. The interface should be created to match the user interface (UI) presented in Figure 3. To build the UI, please follow the following tasks:

<ol>

 <li>This activity is started by the Display Activity. When the Edit Activity is created, it should retrieve the information sent from the Display Activity and display the required interface based on the information received.</li>

 <li>The Edit Activity should be designed to look similar to the Main Activity. However, only the component related to the information to be edited should be visible and all the other components should be invisible. Figure 3, shows the application expected flow, as the user clicks the Department edit icon in the Display Activity, it starts the Edit Activity which displays Department label and and radio buttons showing the current selection. The rest of the components are invisible. The user is able to edit the information, and then presses the save button, which sends the result to the Display activity and finishes the Edit Activity. The Display activity updates the displayed information to reflect the change in department.</li>

</ol>

<table width="128">

 <tbody>

  <tr>

   <td width="128"></td>

  </tr>

  <tr>

   <td width="128"><strong>Edit Information</strong></td>

  </tr>

 </tbody>

</table>

<ol start="3">

 <li>Similarly if the current mood is the selected information to be edited, then the Edit Activity should make the seek bar and its label visible and everything else invisible. If the Name or Email are selected the Edit Activity should show an EditText.</li>

</ol>

<table width="127">

 <tbody>

  <tr>

   <td width="127"></td>

  </tr>

  <tr>

   <td width="127"><strong>Edit Information</strong>Your current mood:</td>

  </tr>

 </tbody>

</table>

<strong>Figure 3, Editing the department</strong>

<strong>Figure 4, Editing the current mood</strong>
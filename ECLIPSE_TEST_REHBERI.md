Guide to Running Tests with Eclipse

🎯 How to Run Tests in Eclipse

There are 3 easy steps to run your tests in Eclipse!

📥 Step 1: Prepare Eclipse

If Eclipse Is Not Installed:

Download Eclipse IDE for Java Developers:
https://www.eclipse.org/downloads/

Click the "Download" button.

Select your operating system (Windows x64).

Run the Eclipse Installer:

Select "Eclipse IDE for Java Developers"

Choose the installation folder.

Click "Install"

📂 Step 2: Import the Project

1. Start Eclipse

Open Eclipse IDE.

2. Select a Workspace

You can use the default workspace.

Or use a workspace such as:
C:\Users\Ahmet Furkan\eclipse-workspace

3. Import the Maven Project

Go to File → Import.

Select Maven → Existing Maven Projects, then click Next.

4. Select the Project Folder

After clicking Next, click Browse and select the project folder:

C:\Users\Ahmet Furkan\Desktop\hospital-appointment-system-java

5. Select pom.xml

Eclipse will automatically find the pom.xml file:

/pom.xml - hospital-reservation-system-java

Click Finish.

6. Maven Update (Automatic)

Eclipse will automatically:

✅ Download Maven dependencies

✅ Add JUnit

✅ Build the project

Wait for the progress bar in the bottom-right corner.

This process may take 2–3 minutes. An internet connection is required.

🧪 Step 3: Run the Tests

Method 1: Run a Single Test File

In Package Explorer (left panel), open:
hospital-reservation-system-java → src/test/java → mertguler.Person → PersonTest.java

Right-click PersonTest.java.

Select Run As → JUnit Test.

The JUnit panel will open at the bottom.

Example result:

PersonTest                     15/15
  testPersonCreation            12ms
  testGetName                    3ms
  testSetName                    2ms
  testEquals_SameObject          2ms

Runs: 15/15   Errors: 0   Failures: 0

Method 2: Run All Tests

Right-click the src/test/java folder.

Select Run As → JUnit Test.

All 12 test classes (approximately 325 tests) will run.

Example:

mertguler.Person.PersonTest        15 passed
mertguler.Person.PatientTest       20 passed
mertguler.Person.DoctorTest        25 passed
mertguler.Hospital.HospitalTest    35 passed
... (more tests)

Total: 325 tests - 8.5 seconds

🎨 Visual Guide

The Eclipse screen will show the project in Package Explorer, the test file in the editor, and the results in the JUnit panel.

🔧 Troubleshooting

Problem 1: Maven Dependencies Are Not Downloading

Solution:

Right-click the project.

Select Maven → Update Project.

Check Force Update of Snapshots/Releases.

Click OK.

Problem 2: JUnit Cannot Be Found

Solution:

Open the pom.xml file.

Right-click anywhere in the file.

Select Maven → Add Dependency.

Search for junit.

Select junit:junit:4.12.

Click OK.

Problem 3: The Test Folder Is Not Recognized

Solution:

Right-click the src/test/java folder.

Select Build Path → Use as Source Folder.

Problem 4: "Cannot Resolve Symbol" Errors

Solution:

Go to Project → Clean.

Select Clean all projects.

Click OK.

Eclipse will automatically rebuild the project.

Problem 5: Java 21 Cannot Be Found

Solution:

Right-click the project.

Select Properties.

Select Java Build Path from the left menu.

Click the Libraries tab.

Select JRE System Library → Edit.

Click Installed JREs.

Click Add and specify the path to JDK 21.

⌨️ Eclipse Keyboard Shortcuts

Alt + Shift + X, T → Run JUnit Test

Ctrl + F11 → Run the last test again

F11 → Run in Debug mode

Ctrl + Shift + T → Search for a test file

📊 Success Indicators

If the tests run successfully, you should see:

✅ Green progress bar
✅ "Runs: X/X"
✅ "Errors: 0"
✅ "Failures: 0"
✅ A green check mark next to all tests

If there is an error:

❌ Red progress bar
❌ "Failures: X"
❌ A red X next to some tests

🎯 Understanding Test Results

Successful Test

✅ testPersonCreation    12ms

Green check mark = Test passed

12ms = Test execution time

Failed Test

❌ testPersonCreation    Failed
   Expected: <Person> but was: <null>
   at PersonTest.java:25

Red X = Test failed

The error message shows what was expected and what actually happened.

🚀 Advanced: Maven Terminal

You can also run Maven commands in Eclipse:

Right-click the project.

Select Run As → Maven build...

Enter the goal:
test

Click Run.

You will see Maven output in the Console:

[INFO] T E S T S
[INFO] Running mertguler.Person.PersonTest
[INFO] Tests run: 15, Failures: 0, Errors: 0, Skipped: 0
[INFO] BUILD SUCCESS

💡 Tips

✅ Automatic Test Execution

You can configure Eclipse to perform actions whenever you save a file:

Go to Window → Preferences.

Select Java → Editor → Save Actions.

Check Perform the selected actions on save.

Select Additional actions → Configure.

Choose the actions you want to perform.

✅ View Code Coverage

To view test coverage:

Right-click the test file.

Select Coverage As → JUnit Test.

Green = tested code, Red = untested code.

✅ Create a Test Quickly

To create a new test:

Open the class you want to test.

Press Ctrl + N → select JUnit Test Case.

Eclipse will automatically create a test template.

🎓 Eclipse vs IntelliJ

Feature

Eclipse

IntelliJ IDEA

Free

Completely free

Community Edition available

Maven

Manual update

Automatic

Memory usage

Lightweight

Slightly heavier

Ease of use

Moderate

Very easy

Setup

3–5 minutes

2 minutes

Both IDEs can run your tests.

📝 Checklist: Are the Tests Successful in Eclipse?

I imported the project as a Maven project.

I updated Maven (Right-click → Maven → Update Project).

The pom.xml file exists and opens correctly.

The src/test/java folder is visible.

Run As → JUnit Test is available for the test file.

The JUnit panel opens when I run a test.

I see a green progress bar.

All tests pass (Errors: 0, Failures: 0).

If all of these are checked, you have successfully run the tests.

📞 Need Help?

Common Errors

"Build path is incomplete" → Run Maven Update.

"JUnit not found" → Check pom.xml and run Maven Update.

"Tests not running" → Go to src/test/java → Build Path → Use as Source Folder.

"Java version mismatch" → Go to Properties → Java Compiler → Select 21.

✅ Done!

If the tests ran successfully, you have:

✅ Opened the Maven project in Eclipse.

✅ Run the JUnit tests.

✅ Understood the test results.

✅ Used modern Java development tools.

Congratulations! Your tests are running successfully in Eclipse! 🎉

Note: Eclipse is one of the oldest and most reliable IDEs for Java development. Many professional developers use Eclipse.

Happy testing! 🚀

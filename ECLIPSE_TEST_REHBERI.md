# Guide to Running Tests with Eclipse

## 🎯 How to Run Tests in Eclipse

There are 3 easy steps to run your tests in Eclipse:

1. Prepare Eclipse
2. Import the project
3. Run the tests

---

## 📥 Step 1: Prepare Eclipse

### If Eclipse Is Not Installed

1. Download **Eclipse IDE for Java Developers**:

   https://www.eclipse.org/downloads/

2. Click the **Download** button.

3. Select your operating system:
   - Windows x64

4. Run the Eclipse Installer:
   - Select **Eclipse IDE for Java Developers**
   - Choose the installation folder
   - Click **Install**

---

## 📂 Step 2: Import the Project

### 1. Start Eclipse

Open **Eclipse IDE**.

### 2. Select a Workspace

You can use the default workspace.

Or choose a workspace such as:

```text
C:\Users\Ahmet Furkan\eclipse-workspace
```

### 3. Import the Maven Project

Go to:

**File → Import**

Then select:

**Maven → Existing Maven Projects**

Click **Next**.

### 4. Select the Project Folder

After clicking **Next**:

Click **Browse** and select the project folder:

```text
C:\Users\Ahmet Furkan\Desktop\hospital-appointment-system-java
```

### 5. Select `pom.xml`

Eclipse will automatically find the `pom.xml` file.

You should see:

```text
/pom.xml - hospital-reservation-system-java
```

Click **Finish**.

### 6. Maven Update

Eclipse will automatically:

- ✅ Download Maven dependencies
- ✅ Add JUnit
- ✅ Build the project

Wait for the progress bar in the bottom-right corner.

You may see:

```text
Building workspace... (XX%)
```

This process may take **2–3 minutes**.

An internet connection is required.

---

## 🧪 Step 3: Run the Tests

### Method 1: Run a Single Test File

1. Open **Package Explorer** on the left side.

2. Open the following path:

```text
hospital-reservation-system-java
└── src
    └── test
        └── java
            └── mertguler.Person
                └── PersonTest.java
```

3. Right-click **PersonTest.java**.

4. Select:

**Run As → JUnit Test**

5. The **JUnit** panel will open at the bottom.

Example result:

```text
PersonTest                     15/15

  testPersonCreation            12ms
  testGetName                    3ms
  testSetName                    2ms
  testEquals_SameObject          2ms

Runs: 15/15
Errors: 0
Failures: 0
```

---

### Method 2: Run All Tests

1. Right-click the:

```text
src/test/java
```

folder.

2. Select:

**Run As → JUnit Test**

3. All 12 test classes will run.

Approximately **325 tests** will be executed.

Example:

```text
mertguler.Person.PersonTest        15 passed
mertguler.Person.PatientTest       20 passed
mertguler.Person.DoctorTest        25 passed
mertguler.Hospital.HospitalTest    35 passed
... (more tests)

Total: 325 tests
Time: 8.5 seconds
```

---

## 🎨 Visual Guide

The Eclipse screen will normally contain:

- **Package Explorer** on the left
- The Java test file in the center
- **JUnit results** at the bottom

Example structure:

```text
Eclipse IDE
│
├── Package Explorer
│   └── hospital-reservation-system-java
│       └── src
│           └── test
│               └── java
│
├── Test File
│   └── PersonTest.java
│
└── JUnit Panel
    ├── Tests
    ├── Runs
    ├── Errors
    └── Failures
```

---

# 🔧 Troubleshooting

## Problem 1: Maven Dependencies Are Not Downloading

### Solution

1. Right-click the project.
2. Select:

   **Maven → Update Project**

3. Check:

   **Force Update of Snapshots/Releases**

4. Click **OK**.

---

## Problem 2: JUnit Cannot Be Found

### Solution

1. Open the `pom.xml` file.
2. Right-click inside the file.
3. Select:

   **Maven → Add Dependency**

4. Search for:

```text
junit
```

5. Select:

```text
junit:junit:4.12
```

6. Click **OK**.

---

## Problem 3: The Test Folder Is Not Recognized

### Solution

1. Right-click:

```text
src/test/java
```

2. Select:

**Build Path → Use as Source Folder**

---

## Problem 4: "Cannot Resolve Symbol" Errors

### Solution

1. Go to:

**Project → Clean**

2. Select:

**Clean all projects**

3. Click **OK**.

4. Eclipse will automatically rebuild the project.

---

## Problem 5: Java 21 Cannot Be Found

### Solution

1. Right-click the project.
2. Select **Properties**.
3. Select **Java Build Path**.
4. Open the **Libraries** tab.
5. Select:

   **JRE System Library**

6. Click **Edit**.
7. Click **Installed JREs**.
8. Click **Add**.
9. Select the path to **JDK 21**.

---

# ⌨️ Eclipse Keyboard Shortcuts

| Shortcut | Function |
|---|---|
| `Alt + Shift + X, T` | Run JUnit Test |
| `Ctrl + F11` | Run the last test again |
| `F11` | Run in Debug mode |
| `Ctrl + Shift + T` | Search for a test file |

---

# 📊 Success Indicators

If the tests run successfully, you should see:

```text
✅ Green progress bar
✅ Runs: X/X
✅ Errors: 0
✅ Failures: 0
✅ Green check marks beside the tests
```

If there is an error, you may see:

```text
❌ Red progress bar
❌ Failures: X
❌ Red X beside some tests
```

---

# 🎯 Understanding Test Results

## Successful Test

Example:

```text
✅ testPersonCreation    12ms
```

Meaning:

- ✅ Green check mark = Test passed
- `12ms` = Test execution time

---

## Failed Test

Example:

```text
❌ testPersonCreation    Failed

Expected: <Person>
But was: <null>

at PersonTest.java:25
```

Meaning:

- ❌ Red X = Test failed
- The error message tells you what was expected
- It also shows what the program actually returned

---

# 🚀 Advanced: Maven Terminal

You can also run Maven commands directly from Eclipse.

### Steps

1. Right-click the project.
2. Select:

   **Run As → Maven build...**

3. Enter the goal:

```text
test
```

4. Click **Run**.

The Console will show output similar to:

```text
[INFO] -------------------------------------------------------
[INFO]  T E S T S
[INFO] -------------------------------------------------------

[INFO] Running mertguler.Person.PersonTest

[INFO] Tests run: 15
[INFO] Failures: 0
[INFO] Errors: 0
[INFO] Skipped: 0

[INFO] BUILD SUCCESS
```

---

# 💡 Tips

## ✅ Automatic Test Execution

You can configure Eclipse to perform actions whenever you save a file.

### Steps

1. Go to:

   **Window → Preferences**

2. Select:

   **Java → Editor → Save Actions**

3. Check:

   **Perform the selected actions on save**

4. Select:

   **Additional actions → Configure**

5. Choose the actions you want.

---

## ✅ View Code Coverage

To view test coverage:

1. Right-click the test file.
2. Select:

   **Coverage As → JUnit Test**

3. The colors indicate coverage:

- 🟢 Green = Tested code
- 🔴 Red = Untested code

---

## ✅ Create a Test Quickly

To create a new test:

1. Open the class you want to test.
2. Press:

   `Ctrl + N`

3. Select:

   **JUnit Test Case**

4. Eclipse will create a test template automatically.

---

# 🎓 Eclipse vs IntelliJ IDEA

| Feature | Eclipse | IntelliJ IDEA |
|---|---|---|
| Free | Completely free | Community Edition available |
| Maven | Manual update | Automatic |
| Memory Usage | Lightweight | Slightly heavier |
| Ease of Use | Moderate | Very easy |
| Setup Time | 3–5 minutes | 2 minutes |

**Both Eclipse and IntelliJ IDEA can run the project tests.**

---

# 📝 Checklist: Are the Tests Successful?

Before considering the testing setup complete, make sure:

- [ ] The project was imported as a Maven project.
- [ ] Maven Update was completed.
- [ ] The `pom.xml` file exists and opens correctly.
- [ ] The `src/test/java` folder is visible.
- [ ] The **Run As → JUnit Test** option is available.
- [ ] The JUnit panel opens.
- [ ] A green progress bar is displayed.
- [ ] All tests pass.
- [ ] Errors = 0
- [ ] Failures = 0

If all of these are completed, the tests have been successfully run in Eclipse.

---

# 📞 Need Help?

## Common Errors

### "Build path is incomplete"

Run:

**Maven → Update Project**

### "JUnit not found"

Check the `pom.xml` file and run:

**Maven → Update Project**

### "Tests not running"

Go to:

**src/test/java → Build Path → Use as Source Folder**

### "Java version mismatch"

Go to:

**Properties → Java Compiler → Select Java 21**

---

# ✅ Done!

If the tests run successfully, you have:

- ✅ Opened the Maven project in Eclipse
- ✅ Run the JUnit tests
- ✅ Understood the test results
- ✅ Used Java development tools successfully

## 🎉 Congratulations!

Your tests are running successfully in Eclipse!

---

**Note:** Eclipse is one of the oldest and widely used IDEs for Java development.

**Happy Testing! 🚀**

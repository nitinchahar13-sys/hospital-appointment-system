# 🧪 Test Running Guide

## ⚠️ Important Note

The test files are written for a **Maven project**. They cannot be compiled directly using `javac` because:

1. ❌ The main project code must be available in the classpath.
2. ❌ The JUnit library is required.
3. ❌ All dependencies must be added to the classpath.

---

# ✅ Recommended Methods

## 🥇 Method 1: IntelliJ IDEA (EASIEST - RECOMMENDED)

### Steps

### 1. Open the Project

- Open IntelliJ IDEA.
- Go to:

  **File → Open**

- Select the `hospital-appointment-system-java` project folder.
- Open the `pom.xml` file as a Maven project.

### 2. Download Maven Dependencies

- IntelliJ IDEA will automatically download the Maven dependencies.
- If necessary, click **"Load Maven Changes"** in the top-right corner.

### 3. Run the Tests

- Open the following folder in the project tree:

  ```text
  src/test/java
  ```

- Right-click any test class, for example:

  ```text
  PersonTest.java
  ```

- Select:

  **Run 'PersonTest'**

### 4. Run All Tests

- Right-click the:

  ```text
  src/test/java
  ```

  folder.

- Select:

  **Run 'All Tests'**

### Video Guide

[IntelliJ IDEA - Running JUnit Tests](https://www.jetbrains.com/help/idea/performing-tests.html)

---

# 🥈 Method 2: Eclipse IDE

### Steps

### 1. Import the Project

- Go to:

  **File → Import → Existing Maven Projects**

- Select the project folder.
- Click **Finish**.

### 2. Update Maven

- Right-click the project.
- Select:

  **Maven → Update Project**

- Check:

  **Force Update of Snapshots/Releases**

- Click **OK**.

### 3. Run the Tests

- Right-click the test file.
- Select:

  **Run As → JUnit Test**

---

# 🥉 Method 3: Maven Command Line

## Maven Installation

### Windows (Using Chocolatey)

If Chocolatey is not installed, install it first:

```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; 
[System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; 
iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```

Then install Maven:

```powershell
choco install maven
```

### Manual Installation

1. Download Maven from:

   https://maven.apache.org/download.cgi

2. Extract the ZIP file, for example:

   ```text
   C:\Program Files\Apache\maven
   ```

3. Add the following directory to the system `PATH`:

   ```text
   C:\Program Files\Apache\maven\bin
   ```

4. Open a new terminal and verify the installation:

   ```powershell
   mvn --version
   ```

---

## Run Tests Using Maven

### Go to the Project Directory

```powershell
cd "C:\Users\Ahmet Furkan\Desktop\hospital-appointment-system-java"
```

### Run All Tests

```powershell
mvn test
```

### Run a Specific Test Class

```powershell
mvn test -Dtest=PersonTest
```

### Run a Specific Test Method

```powershell
mvn test -Dtest=PersonTest#testPersonCreation
```

### Run with Verbose Output

```powershell
mvn test -X
```

### Expected Output

```text
[INFO] -------------------------------------------------------
[INFO]  T E S T S
[INFO] -------------------------------------------------------

[INFO] Running mertguler.Person.PersonTest
[INFO] Tests run: 15, Failures: 0, Errors: 0, Skipped: 0

[INFO] Running mertguler.Person.PatientTest
[INFO] Tests run: 20, Failures: 0, Errors: 0, Skipped: 0

...

[INFO] BUILD SUCCESS
```

---

# 🔧 Method 4: VS Code

## Requirements

Install the following extensions:

1. **Extension Pack for Java**
2. **Maven for Java**
3. **Test Runner for Java**

## Steps

1. Open the project in VS Code.
2. Click the **Testing** icon (beaker icon) on the left.
3. View the test files.
4. Run the required tests.

Alternatively, open a test file and click the **"Run Test"** button displayed at the top.

---

# 🚫 Do Not Do This

## ❌ Do Not Compile Directly Using `javac`

```powershell
# THIS WILL NOT WORK!
javac CRSTest.java
java CRSTest
```

### Why?

- The main project code has not been compiled.
- The JUnit library is not available.
- Classpath settings are missing.
- The module system configuration is required.

---

# 📊 What Do the Test Results Look Like?

## IntelliJ IDEA

```text
✓ PersonTest
  ✓ testPersonCreation (12ms)
  ✓ testGetName (3ms)
  ✓ testEquals_SameObject (2ms)
  ...

Tests passed: 15 of 15 tests - 150ms
```

## Maven

```text
Results:

Tests run: 325, Failures: 0, Errors: 0, Skipped: 0

[INFO] BUILD SUCCESS
[INFO] Total time: 8.523 s
```

---

# 🐛 Troubleshooting

## Problem: "Module not found"

### Solution

**In IntelliJ IDEA:**

Go to:

```text
File → Project Structure → Modules → Dependencies
```

Check the project dependencies.

**Using Maven:**

Run:

```powershell
mvn clean install
```

---

## Problem: JUnit Cannot Be Found

### Solution

- Download the Maven dependencies again.
- In IntelliJ IDEA, click **Reload Maven Project**.
- Make sure the `pom.xml` file is correct.

---

## Problem: Test Files Are Not Recognized

### Solution

Make sure the following folder is marked as a **Test Sources Root**:

```text
src/test/java
```

In IntelliJ IDEA:

```text
Right-click src/test/java
→ Mark Directory as
→ Test Sources Root
```

---

## Problem: Compile Error

### Solution

### Clean the Maven Cache

```powershell
mvn clean
```

### Download Dependencies Again

```powershell
mvn clean install -U
```

### Restart the IDE

Close and reopen IntelliJ IDEA or your preferred IDE.

---

# 📝 Quick Start - IntelliJ IDEA

```text
1. Open IntelliJ IDEA
2. Select Open → Choose the project folder
3. Maven will load automatically (wait for it to finish)
4. Open src/test/java/mertguler/Person/PersonTest.java
5. Click the green Play button ▶️
6. View the test results ✅
```

**That's it! ✨**

---

# 💡 Tips

### ✅ Easiest Option

Use **IntelliJ IDEA Community Edition (Free)**:

https://www.jetbrains.com/idea/download/

### ✅ While Writing Tests

- Run the tests automatically after making changes.
- Use the red/green feedback cycle.
- Use **Debug mode** to find and fix problems.

### ✅ For CI/CD

You can use:

- GitHub Actions for automatic testing.
- Maven for the build pipeline.

---

# 📞 Help

If you experience problems:

1. Check the IDE's Maven/Gradle console logs.
2. Verify Maven installation:

   ```powershell
   mvn --version
   ```

3. Make sure JDK 21 is installed:

   ```powershell
   java -version
   ```

---

## ✅ Final Note

The tests are written according to the **Maven standard** and can be used in a production development environment.

**Happy Testing! 🚀**

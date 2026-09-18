# ⚡ Run Tests in 2 Minutes

## 🎯 Step-by-Step Guide

### 📥 Step 1: Download IntelliJ IDEA (2 min)

1. Open the following website in your browser:

   https://www.jetbrains.com/idea/download/

2. Click the **Community Edition (FREE)** button.

3. After the download is complete, run the installation file.

4. During installation:
   - ✅ Select **"Add to PATH"**
   - ✅ Select **"Associate .java files"**
   - ✅ Continue with the default settings

---

## 📂 Step 2: Open the Project (30 sec)

1. Start **IntelliJ IDEA**.

2. Click the **"Open"** button.

3. Select the following folder:

   ```text
   C:\Users\Ahmet Furkan\Desktop\hospital-appointment-system-java
   ```

4. When the **"Trust Project"** dialog appears, select **"Trust Project"**.

5. Wait for IntelliJ IDEA to load the project.

   IntelliJ will automatically:

   - ✅ Detect Maven
   - ✅ Read `pom.xml`
   - ✅ Download JUnit
   - ✅ Build the project

   You will see a progress bar in the bottom-right corner. Wait until it finishes.

---

## 🧪 Step 3: Run the Test (10 sec)

1. In the **Project** panel on the left, open:

   ```text
   src → test → java → mertguler → Person
   ```

2. **Double-click** the `PersonTest.java` file.

3. When the file opens, you will see green **Play (▶️)** icons on the left side.

4. Click the green Play icon next to the **class name**.

5. Select:

   **"Run 'PersonTest'"**

6. 🎉 **Result:** The test results will appear at the bottom.

   ```text
   ✅ Tests passed: 15 of 15 tests
   ```

---

## 🎥 Visual Guide

### This is what it will look like:

```text
┌─────────────────────────────────────────────────┐
│ IntelliJ IDEA                          [- □ X]   │
├──────────┬──────────────────────────────────────┤
│ Project  │ PersonTest.java                      │
│          │                                       │
│ ▼ src    │ package mertguler.Person;            │
│   ▼ test │                                       │
│     ▼ java│ import org.junit.Test;              │
│       ▼ mertguler│                              │
│         ▶ CRS   │ public class PersonTest {     │
│         ▶ Hospital│   @Test                     │
│         ▶ Person  │   public void testPerson()  │
│           ▶ PersonTest.java  ◀── DOUBLE-CLICK    │
│         ▶ Exceptions│   }                       │
│                   │ }                            │
├───────────────────┴──────────────────────────────┤
│ ▶️ Run: PersonTest                               │
│ ✅ testPersonCreation                    12ms   │
│ ✅ testGetName                           3ms    │
│ ✅ testEquals_SameObject                 2ms    │
│                                                  │
│ Tests passed: 15 of 15 tests - 150ms           │
└──────────────────────────────────────────────────┘
```

---

## 🚀 Alternative: Run All Tests

1. In the left panel, **right-click** the:

   ```text
   src/test/java
   ```

   folder.

2. Select:

   **"Run 'All Tests'"**

3. All 325+ tests will run.

   Example:

   ```text
   ✅ PersonTest: 15 passed
   ✅ PatientTest: 20 passed
   ✅ DoctorTest: 25 passed
   ✅ HospitalTest: 35 passed
   ... (more tests)

   Total: 325 tests passed in 8.5s
   ```

---

## ❓ Why IntelliJ IDEA?

### ✅ It Handles Everything Automatically

- ✅ Detects Maven
- ✅ Downloads JUnit
- ✅ Compiles the project
- ✅ Configures the classpath
- ✅ Runs the tests

### 🆚 Manual Method vs IntelliJ IDEA

| Feature | Manual (`javac`) | IntelliJ IDEA |
|---|---|---|
| Installation | Download JUnit manually | Automatic |
| Build | Use `javac` commands | One click |
| Classpath | Configure manually | Automatic |
| Run Tests | Use `java` commands | One click ▶️ |
| Time | ~30 minutes | ~2 minutes |
| Difficulty | 😫😫😫 | 😊 |

---

## 🔄 Having Problems?

### Problem 1: Maven Is Not Downloading

**Solution:**

1. Click **"Import"** or **"Load Maven Changes"** in the bottom-right corner.

2. Or go to:

   **File → Invalidate Caches → Restart**

---

### Problem 2: Test Files Are Not Recognized

**Solution:**

1. Right-click the:

   ```text
   src/test/java
   ```

   folder.

2. Select:

   **Mark Directory as → Test Sources Root**

---

### Problem 3: JUnit Cannot Be Found

**Solution:**

1. Go to:

   **View → Tool Windows → Maven**

2. Click the **Refresh (🔄)** icon.

3. Run:

   **Lifecycle → clean**

4. Then run:

   **Lifecycle → install**

---

## 🎓 Bonus: Keyboard Shortcuts

- `Ctrl + Shift + F10` → Run the test
- `Shift + F10` → Run the last test again
- `Ctrl + Shift + F9` → Debug mode
- `Ctrl + F5` → Rerun the test

---

## ✅ Success Checklist

When the tests have run successfully, you should see:

```text
✅ Green check marks
✅ "Tests passed: X of X"
✅ Green bar at the bottom
✅ No red errors
```

---

## 📞 Still Having Problems?

If you are still having problems in IntelliJ IDEA:

### 1. Try this first

Go to:

```text
File → Invalidate Caches → Restart
```

### 2. Reload Maven

- Open the Maven panel on the right side.
- Click the **🔄 Reload** button.

### 3. Check the JDK

Go to:

```text
File → Project Structure → Project
```

Make sure:

```text
SDK: Java 21
```

---

## 🎉 Are You Done?

When the first test runs successfully, you have:

- ✅ Learned how to run tests
- ✅ Learned how to use JUnit
- ✅ Understood how a Maven project works
- ✅ Started using a modern Java IDE

**Congratulations! 🎊**

---

**Note:** This guide is written for beginners.

IntelliJ IDEA is one of the most popular IDEs for Java development.

**Happy Coding! 💻**

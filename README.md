# 🧾 YAML Basics Lab – Creating and Editing YAML Files

In this lab, I learned how to read, edit, and structure YAML files — including **key-value pairs**, **dictionaries**, and **arrays** — using the Linux `vi` editor.
The tasks reinforced indentation rules, data types, and how to build complex nested structures inside YAML files.

---

## 📋 Lab Overview

**Goal:**

* Understand YAML syntax and structure
* Edit YAML files using `vi`
* Create dictionaries and lists (arrays)
* Apply proper indentation and formatting rules

**Learning Outcomes:**

* Recognize how key–value pairs are defined using colons (`:`)
* Differentiate between **dictionaries** (unordered) and **lists** (ordered)
* Add nested dictionaries and arrays inside a YAML file
* Confidently edit YAML files via the command line

---

## 🛠 Step-by-Step Journey

### Step 1: Identify YAML Key–Value Separator

**Question:** Which of the following is used to separate the key and value in YAML?
✅ **Answer:** The colon (`:`)

---

### Step 2: Counting Keys

**Question:** How many keys are there in the YAML snippet?
✅ **Answer:** Two keys.

---

### Step 3: Dictionary vs List

**Question:** Which statement is true?
✅ **Answer:** A dictionary is **unordered**, whereas a list is **ordered**.

---

### Step 4: Add a New Key–Value Pair

**Task:** In `/home/bob/playbooks/practice.yaml`, add `property2: 2`.

```bash
sudo vi /home/bob/playbooks/practice.yaml
```

Inside `vi`:

* Press `i` to enter insert mode
* Add

  ```yaml
  property2: 2
  ```
* Press `ESC` → `:wq` to save and exit

✅ Verified successfully.

---

### Step 5: Extend an Existing Dictionary

**Task:** Add `color: red` and `weight: 90G` under the existing name and value.

```bash
sudo vi /home/bob/playbooks/practice.yaml
```

```yaml
name: Apple
color: red
weight: 90G
```

✅ File updated and validated.

---

### Step 6: Add Properties Inside a Nested Dictionary

**Task:** Add dictionary `employee` with properties.

```yaml
employee:
  name: John
  gender: male
  age: 24
```

✅ Saved and confirmed correct.

---

### Step 7: Add a Dictionary Inside Another Dictionary

**Task:** Add `address` dictionary inside `employee`.

```yaml
employee:
  name: John
  gender: male
  age: 24
  address:
    city: Edison
    state: New Jersey
    country: United States
```

✅ Proper indentation verified — dictionary inside a dictionary works correctly.

---

### Step 8: Work with Arrays (Lists)

**Task:** Add another apple to make a total of four.

```yaml
apples:
  - apple
  - apple
  - apple
  - apple
```

✅ Array extended to 4 elements.

---

### Step 9: Extend Array Further

**Task:** Add two more apples to make six total.

✅ Successfully appended; total elements now **6**.

---

### Step 10: Add Additional Item Details

**Task:** For each fruit, add color and weight properties.

```yaml
fruits:
  - name: apple
    color: red
    weight: 100g
  - name: orange
    color: orange
    weight: 90g
  - name: mango
    color: yellow
    weight: 150g
```

✅ Correct details verified for all items.

---

### Step 11: Convert a Dictionary to an Array

**Task:** Change `employee` dictionary into an array named `employees`.

```yaml
employees:
  - name: John
    gender: male
    age: 24
```

✅ Successfully converted.

---

### Step 12: Add Another Employee Entry

**Task:** Add a new employee named Sarah.

```yaml
employees:
  - name: John
    gender: male
    age: 24
  - name: Sarah
    gender: female
    age: 28
```

✅ File structure valid and saved.

---

### Step 13: Add Array of Dictionaries (Payslips)

**Task:** Add `payslips` array under each employee.

```yaml
employees:
  - name: John
    gender: male
    age: 24
    payslips:
      - month: June
        amount: 1400
      - month: July
        amount: 2400
      - month: August
        amount: 3400
```

✅ YAML indentation rules followed correctly — array of dictionaries created.

---

## 🏁 End of Lab

### ✅ Key Commands Summary

| Task               | Command                                     |
| ------------------ | ------------------------------------------- |
| Open YAML file     | `sudo vi /home/bob/playbooks/practice.yaml` |
| Enter insert mode  | `i`                                         |
| Save & exit        | `ESC :wq`                                   |
| Validate structure | `cat /home/bob/playbooks/practice.yaml`     |

---

### 💡 Notes / Tips

* YAML uses **indentation** (spaces, not tabs) to show structure — consistency is crucial.
* Dictionaries use key–value pairs; arrays use `-` before each element.
* Use `vi` navigation commands efficiently: `i` (insert), `ESC`, `:wq` (write & quit).
* Nested objects (like address or payslips) demonstrate **hierarchical data** formatting.

---

### ✅ References

* [YAML Official Specification](https://yaml.org/spec/)
* [YAML Basics on KodeKloud](https://kodekloud.com/)
* [YAML Tutorial – Beginners Guide](https://www.cloudbees.com/blog/yaml-tutorial)

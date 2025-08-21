# FLASK

```markdown
# Flask Result Redirect App

This is a simple **Flask application** that demonstrates URL routing, redirection, and dynamic parameters.  
The app checks student marks and redirects the user to either the **success** or **fail** page depending on the score.

---

## 📂 Project Structure

```

.
├── app.py       # Main Flask application
├── README.md    # Project documentation

````

---

## ⚙️ Requirements

- Python 3.x  
- Flask  

Install Flask using pip:

```bash
pip install flask
````

---

## ▶️ How to Run

1. Clone or download this repository.
2. Navigate to the project folder.
3. Run the app:

```bash
python app.py
```

4. Open your browser and visit:

```
http://127.0.0.1:5000/
```

---

## 📌 Routes

### `/`

* Home route.
* Returns: `"Welcome to my Youtube Channel."`

### `/success/<int:score>`

* Displays a success message if marks are greater than or equal to 50.
* Example: `/success/80` → `The person is passed and the marks is 80`

### `/fail/<int:score>`

* Displays a failure message if marks are less than 50.
* Example: `/fail/30` → `The person is failed and the marks is 30`

### `/results/<int:marks>`

* Checks the marks and redirects:

  * If marks < 50 → redirects to `/fail/<marks>`
  * If marks ≥ 50 → redirects to `/success/<marks>`

Example:

* `/results/45` → redirects to `/fail/45`
* `/results/75` → redirects to `/success/75`

---

## 🚀 Example Run

* Visit: `http://127.0.0.1:5000/results/72`
  Output: **The person is passed and the marks is 72**

* Visit: `http://127.0.0.1:5000/results/32`
  Output: **The person is failed and the marks is 32**

---

## 📝 Notes

* `debug=True` is enabled for development, remove it in production.
* This project is for learning Flask basics (routing, redirect, and url\_for).

---
in learning phase:)

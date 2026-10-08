# Online Course App with Assessment Feature

A Django online course application extended with an exam (assessment) feature:

- **Models:** `Question`, `Choice` and `Submission` in `onlinecourse/models.py`
- **Admin:** `QuestionInline`, `ChoiceInline`, `QuestionAdmin` and `LessonAdmin` in `onlinecourse/admin.py`
- **Course page:** `course_details_bootstrap.html` lists the lessons and a collapsible exam form
- **Views:** `submit` records the learner's selected choices; `show_exam_result` scores the exam
- **Result page:** pass (score above 80) shows a Congratulations message, the score and per-question results

## Run Locally

```bash
pip install -r requirements.txt
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```

Open http://127.0.0.1:8000/onlinecourse/ for the app and http://127.0.0.1:8000/admin/ for the admin site.


**General Notes**

An `onlinecourse` app has already been provided in this repo upon which you will be adding a new assesement feature.

- If you want to develop the final project on Theia hosted by [IBM Developer Skills Network](https://labs.cognitiveclass.ai/), you will need to create the same project structure on Theia workspace and save it everytime you close the browser
- Or you could develop the final project locally by setting up your own Python runtime and IDE
- Hints for the final project are left on source code files
- You may choose any cloud platform for deployment (default is IBM Cloud Foundry)
- Depends on your deployment, you may choose any SQL database Django supported such as SQLite3, PostgreSQL, and MySQL (default is SQLite3)

**ER Diagram**
For your reference, we have prepared the ER diagram design for the new assesement feature.

![Onlinecourse ER Diagram](https://github.com/ibm-developer-skills-network/final-cloud-app-with-database/blob/master/static/media/course_images/onlinecourse_app_er.png)

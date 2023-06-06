# Datasets
In this paper, we've used two databases:
 - `ASD`
 - `ADHD`

Both of these databases are SQLite. Each database has three different entities:
 - `Users`
 - `Questions`
 - `Comments`

There is also another dependent entity which is merge form of all other threes we called it `ExportData`.

`Users` entity structure:

<div align="center">

| Attribute   | Description                                      |
|-------------|--------------------------------------------------|
| UserID      | The user's ID on the website                     |
| Description | If the user has set a description for themselves |
| PostCount   | The number of posts the user has shared          |

</div>

`Questions` entity structure:

<div align="center">

| Attribute | Description                                         |
|-----------|-----------------------------------------------------|
| QID       | The question's ID                                   |
| QUserID   | The user ID of the person who released the question |
| QTitle    | The title of the question                           |
| QBody     | The body text of the question                       |
| QDate     | The date the question was released                  |
| QVisit    | The number of users who visited the question        |

</div>

`Comments` entity structure:

<div align="center">

| Attribute | Description                                                               |
|-----------|---------------------------------------------------------------------------|
| QID       | The ID of the question that the comment is in response to                 |
| CUserID   | The user ID of the person who posted the comment                          |
| CBody     | The body text of the reply                                                |
| CDate     | The date of the comment release                                           |
| IsReply   | A boolean that shows if this comment is a reply to another comment or not |
| QVisit    | The number of users who visited the question                              |
| ParentID  | The ID of the comment to which this comment is a reply                    |

</div>

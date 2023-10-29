# Debugging and Code Optimization Challenge

Welcome to the Debugging and Code Optimization Challenge! In this exercise, you'll be testing your debugging skills and optimizing code in a real-world application. This repository uses Express.js and Mongoose to create a backend server and perform MongoDB operations. Before you begin, please read the instructions carefully.

## Instructions

1. **Do not use any external libraries for pagination.**
2. **Pagination must be implemented on the database directly, not in JavaScript.**
3. Create a new `.env` file by copying the `.env.example` file. You can do this with the following command:

    ```
    cp .env.example .env
    ```

4. Install the necessary dependencies by running either of the following commands:

    ```
    yarn
    ```

    or

    ```
    npm i
    ```

5. Run the test cases using the following commands. Make sure that all test cases pass in your final submission; otherwise, the task will be considered incomplete.

    ```
    npm run test
    ```

    or

    ```
    yarn test
    ```

6. To populate the database with data, run the following command:

    ```
    npm run seed
    ```

    or

    ```
    yarn seed
    ```

   This command will create 100 users and 1-5 posts per user. You should use this seeder to populate the database.

7. You should focus on the `src/controllers/user.controller.js` file, specifically the `getUsersWithPostCount` section marked as "TODO."

## Task

Your main task is to implement a `[GET] http://localhost:3000/users` endpoint that returns all the users with their post count. This API should include server-side pagination.

The response from this API should follow the format shown below:

```json
{
    "data": {
        "users": [
            {
                "_id": "624bccc95debe2a2672738a0",
                "name": "Jacklyn",
                "posts": 2
            },
            {
                "_id": "624bccc95debe2a2672738a1",
                "name": "Jefferey",
                "posts": 2
            },
            {
                "_id": "624bccc95debe2a2672738a2",
                "name": "Mateo",
                "posts": 2
            },
            {
                "_id": "624bccc95debe2a2672738a3",
                "name": "Lyric",
                "posts": 2
            },
            {
                "_id": "624bccc95debe2a2672738a4",
                "name": "Shannon",
                "posts": 2
            },
            {
                "_id": "624bccc95debe2a2672738a5",
                "name": "Evelyn",
                "posts": 2
            },
            {
                "_id": "624bccc95debe2a2672738a6",
                "name": "Brad",
                "posts": 2
            },
            {
                "_id": "624bccc95debe2a2672738a7",
                "name": "Leslie",
                "posts": 2
            },
            {
                "_id": "624bccc95debe2a2672738a8",
                "name": "Laron",
                "posts": 2
            },
            {
                "_id": "624bccc95debe2a2672738a9",
                "name": "Lizeth",
                "posts": 2
            }
        ],
        "pagination": {
            "totalDocs": 100,
            "limit": 10,
            "page": 1,
            "totalPages": 10,
            "pagingCounter": 1,
            "hasPrevPage": false,
            "hasNextPage": true,
            "prevPage": null,
            "nextPage": 2
        }
    }
}

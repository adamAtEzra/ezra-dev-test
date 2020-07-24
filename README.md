# Ezra Full Stack developer test

## Overview

This is a take home test for Ezra. Your goal will be to implement and improve various stub methods in the frontend and backend. You're able to choose whichever frontend framework you wish to complete the test (ie. only complete the angular OR react OR vue not multiple).

Overall the test should take no more than 3 hours to finish, but you are welcome to take more time if you wish, and it doesn't have to be in one stretch.

To complete this test you will need the following
- dotnet core (we used and will test on 3.1): https://dotnet.microsoft.com/download/dotnet-core/3.1
- sqlite (we used and will test on 3.32.3): https://www.sqlite.org/download.html
- nodejs (we used and will test on 12.16.1): https://nodejs.org/en/download/
- we will be testing the frontend on the most recent version of Chrome
- note that you do not need Visual Studio to run the C# code, dotnet core will do this, you can use your text editor of choice
- note that the versions you use need not be the same, as long as there are no breaking changes between your version and ours
- note that you can complete this on linux, windows, or mac.

When ready to start, clone this repository, work on it, and then when complete send us an email letting us know. You may either provide a repository URL or a git bundle of the repo (see below for instructions on git bundle). In the email, also note which frontend framework you've decided to use, anything you were unable to complete, and how long you spent on the test. We'd also appreciate any feedback you have for us about the test (too easy/hard, confusing instructions, difficult to set up). You have maximum 1 week to complete the test and get it back to us.

Make sure to read the whole readme as we are marking on ability to follow instructions.

## Goal

### Front end

1. Complete `render` and `addMember` methods in the add member page
2. Complete `editMember` and `deleteMember` methods in the home page

    Note: You will need to create or reuse some sort of data entry for `editMember`

3. When making changes to members, either adding, editing, or deleting the table should reflect the changed data automatically

### Back end

1. Add endpoints to `api/Controllers/MembersController` to add, delete, and update a member
2. Complete `AddMember`, `UpdateMember` and `DeleteMember` methods in `api/DB/MembersRepository`
3. If you feel like a different route, return type, or method signature would make more sense, please update it

### Misc

1. There is a small bug somewhere in the existing code. Please find and fix

## Grading

- 50% of your mark will be based on correctness, i.e. the code runs, all tests pass, the frontend works
- The remaining 50% will be based on subjective measueres, such as code quality, efficiency, or front end UI/UX

## Notes

- All areas where we expect code to be completed have a comment of `TODO` on them. Use this to ensure you've completed everything
    - All frontend clients will have these comments, this does not mean you need to complete all three clients
- You may take as much time as you feel is appropriate to complete the test
- You should make regular commits to the repository so we can see your progress when we grade
- Copying code from the web is allowed as long as you don't copy everything and source what you do copy
- If you aren't able to complete something that is OK, leave in your attempts, and attempt to explain why you couldn't solve it
- If you have an idea for improvements or extras that you would like to do, write them down somewhere, and it will be considered.
- When you submit let us know which frontend framework you've decided to use, anything you were unable to complete, and how long you spent on the test. We'd also appreciate any feedback you have for us about the test (too easy/hard, confusing instructions, difficult to set up)
- If you want to restore the DB the creation script is in `api/DB/db_init.sql`
- We're looking for code we wouldn't mind working on, so make sure you're writing good code. Things we've noticed left in that is detrimental:
    - `console.log`
    - Commented out code
    - Build artifacts
    - Data from your tests left in the database
    - `node_modules`

## Git bundle

If you would rather submit the assignment as a file you can use git bundle to do so.

From your repo root run the following, and attach the resulting file (`submission.bundle`) to the email. Note, if you're not working off of master, change `master` in the following command to the name of the branch you are using.

```bash
git bundle create submission.bundle master
```

If you wish to test that the bundle works successfully, run the following from your repo root. The result should be a directory named `submission` which is a mirror of your repo.

```bash
git clone -b master ./submission.bundle ../submission
```


## To run

Frontend:

- Angular
    ```bash
    cd angular-client/ && npm start
    ```

- React
    ```bash
    cd react-client/ && npm start
    ```

- Vue
    ```bash
    cd vue-client/ && npm start
    ```

Backend:

```bash
cd api/ && dotnet run
```
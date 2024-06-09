## Demo 
http://158.140.167.180:43075/

## Development
- clone the project
    ```
    git clone https://github.com/bobbybof/timesheet.git
    ```
- pull submodules
    ```
    git submodule init
    git submodule update
    ```
### Backend
#### Prerequisite
1. Make sure you already installed PostgreSQL in your system, the [Link](https://www.postgresql.org/download/) to Download and the instruction to installing PostgreSQL
2. Setup `.env` file, you can copy the value from `.env.example` and adjust the value based on your machine
3. for migration, this project use [golang-migrate](https://github.com/golang-migrate/migrate)
4. I used [Air](https://github.com/cosmtrek/air) for hot reloading during development. If it is not yet installed in your machine, you may do the following command to install it
    ```
    go install github.com/cosmtrek/air@latest
    ```
#### Api Collections
- Bruno
 if you have installed [Bruno](https://github.com/usebruno/bruno) in your machine, you can import the `timsheet-backend/` collection
- Postman
if you have installed [Postman](https://www.postman.com/downloads/) in your machine, you can import the `timsheet-backend/timesheet_postman.json` collection

#### Runing
1. if you already adjust `.env` you can run 
    ```
    make migrateup
    make seed # Optional, for seeding
    ```
2. Run the project
    ```
    air
    ```
### Frontend
#### Running
1. Install the package dependency
    ```
    npm install # npm
    pnpm install # pnpm
    yarn # yarn
    bun install #bun
    ```
2. copy `.env.example` to `.env` and just the value with your backend host and port configuration
3. Run the project
    ```
    npm dev
    ```
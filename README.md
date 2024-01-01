# Setup local development
1. Download Visual Studio Code for mac: https://code.visualstudio.com/download
2. Install github: Open Terminal
 `brew install git`
3. Install rust: Open Terminal and follow those steps https://www.rust-lang.org/tools/install
4. Install rust-analyzer on Visual Code: Shift-Command-X and search for rust-analyzer 
5. Download code to local:
`git clone https://github.com/vanhoale/rustproject.git` . Change directory to `rustproject`
6. Install Docker Desktop (https://www.docker.com/products/docker-desktop/) and install to your Mac -> docker-compose and docker command line (CLI)
7. Start postgresql db by using command below:
`docker-compose up`
8. From terminal `export DATABASE_URL=postgresql://postgres:password@localhost:15432/postgres`
9. Build the code from terminal:
 - `brew install libpq`
 - `export LIBRARY_PATH=/opt/homebrew/opt/libpq/lib`
 - `cargo run`

10. Test APIs:
 - List users: `curl -X GET http://localhost:3000/user/list`
 - Create user: `curl -X POST -d '{"name":"Hoa Le","hair_color":"Black"}' -H "Content-Type: application/json" http://localhost:3000/user/create`


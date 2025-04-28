# Docker for WordPress
> One website one environment.


## How to use
1. Clone this repository and go to the directory:
    ```bash
    git clone https://github.com/garylab/dockerpress.git
    cd dockerpress
    ```
2. Copy `docker-compose.yml.sample` to `docker-compose.yml`:
    ```bash
    cp docker-compose.yml.sample docker-compose.yml
    ```
   Customize the `docker-compose.yml` file as needed.
   E.g. nginx expose port `80` to host default, change it to another one if it was occupied.
3. Run the following command:
    ```bash
    docker compose up -d
    ```
   This will download wordpress automatically and start the containers.
4. Open your browser and access [http://localhost](http://localhost).
5. The MySQL configurations default are (all of the values can be modified in `docker-compose.yml` file):
   - **Host**: `mysql`
   - **Port**: `3306`
   - **DB Name**: `wordpress`
   - **Username**: `root`
   - **Password**: `12345678`
   

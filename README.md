# Docker for WordPress
> One website one environment.


## How to use
1. Clone this repository and go to the directory:
    ```bash
    git clone https://github.com/yeszao/dockerpress.git
    cd dockerpress
    ```
2. Copy `docker-compose.yml.sample` to `docker-compose.yml`:
    ```bash
    cp docker-compose.yml.sample docker-compose.yml
    ```
   Customize the `docker-compose.yml` file as needed.
3. Run the following command:
    ```bash
    docker compose up -d
    ```
4. Download WordPress and unzip files to `src` directory.
    ```bash
   curl -s https://wordpress.org/latest.zip -o /tmp/latest.zip \
       && unzip -q /tmp/latest.zip -d /tmp \
       && mv /tmp/wordpress/* src/ \
       && rm -rf /tmp/wordpress /tmp/latest.zip
   ```
5. Open your browser and access [http://localhost](http://localhost).

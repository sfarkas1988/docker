## Installation

1. Create a `.env` from the `.env.dist` file.

    ```bash
    cp .env.dist .env
    ```


2. Build/run containers with (with and without detached mode)

    ```bash
    $ docker-compose build
    $ docker-compose up -d
    ```

3. Update your system host file

add domains according to your nginx/sites-available hosts

_Windows_
    ```C:\Windows\System32\drivers\etc```


_Mac_
    ```/etc/hosts```

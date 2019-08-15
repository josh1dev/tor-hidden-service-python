# tor-hidden-service-python

> A simple boilerplate of creating a `.onion` website for Tor using Flask and Python.

## Table of Contents

- [Instructions](#instructions)
- [Screenshots](#screenshots)
- [Contributing](#contributing)
- [License](#license)

## Instructions

- Download Tor using the following instructions: ([link](https://2019.www.torproject.org/docs/debian.html.en))

- Configure your hidden service.
    + Go to the tor directory.
    + Open the "torrc" file in an editor. (Probably located in `/etc/tor/torrc` directory)
    + Add the following lines to the file
    ```
    HiddenServiceDir /var/lib/tor/hidden_service/
    HiddenServicePort 80 127.0.0.1:5000
    ```
    + Save and close the file.

- Clone this repository in your local system
```sh
$ git clone https://github.com/satwikkansal/tor-hidden-service-python.git
$ cd tor-hidden-service
```

- Install the pypi requirements
```sh
$ pip install -r requirements.txt
```

- Run the server
```sh
$ python run.py
```

- Launch the Tor Browser

- Copy the url generated in the `hostname` file
```sh
$ cat /var/lib/tor/hidden_service/hostname
>>> some-obfuscated-url.onion
```

- Open this copied url in the Tor Browser and it should work :tada:


## Screenshots

![Screenshot](https://github.com/satwikkansal/tor-hidden-service-python/blob/master/screenshots/front.png)


## Contributing

All patches welcome!


## License

MIT License - see the [LICENSE](https://github.com/satwikkansal/tor-hidden-service-python/blob/master/LICENSE) file for details.

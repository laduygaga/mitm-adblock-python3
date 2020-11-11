# MITM Adblock
$ pip3 install cython  # for install pyre2
$ pip install -r requirements.txt
 Run `./update-blocklists` to download some blocklists
 Run `./go` to start the proxy server on port 8118 (or run `./go -c` for a curses interface which lets you inspect the requests/responses, or run `./go -d` to dump all flows to the 'flows/' directory)
 Do a quick test to make sure it's working: `curl --proxy localhost:8118 -L -k https://slashdot.org/`
 Setup your browser/phone to use `localhost:8118` or `lan-ip-address:8118` as an HTTP proxy server; then, visit http://mitm.it on that device to install the MITM SSL certificate so that your machine won't throw security warnings whenever the proxy server intercepts your secure connections.
If you'd like to change any of the mitmproxy settings (like port, and where/whether it logs your connections), edit the `go` script.


# content-disposition-check

Running `docker-compose up` will start a container running nginx, serving the contents from `content/`.

In `conf`, you'll find `nginx.conf`. In there, comment in/out the following line: `add_header Content-Disposition 'attachment';` 
to enable/disable the `Content-Disposition: 'attachment'` HTTP header. 

Clicking the "Download Now" link in index.html will either: open the image in the same tab
(without the `Content-Disposition: 'attachment'` HTTP header) or download the image when the correct header is present.

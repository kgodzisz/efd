# efd
With this image, you'll be able to run a container with a command that will remove empty directories.

Dockerfile file thanks to which you will create an image with a tar application for automatic archiving and compression of selected files.

I want to warn you that if you designate the root directory of your Linux distribution (/), it will remove all empty directories to which it has access. If I wanted a Linux learner to encounter a lot of problems, this is the command I'd use. Some of these directories are used to store temporary data, so if the responsible directory doesn't exist, it may not be automatically created in many cases. Therefore, it's important to use the command carefully, preferably on a specific directory and not the main system directory. I recommend running it for the first time on a virtual system and seeing how it works.

Check my github for Dockerfile: <a herf="https://github.com/kgodzisz/efd" target="_blank">https://github.com/kgodzisz/efd</a><br />
Check my blog for more: <a href="https://dockeryzacjaswiata.pl" target="_blank">https://dockeryzacjaswiata.pl</a><br />
Check my portfolio for more info: <a href="https://krzysztofgodzisz.pl" target="_blank">https://krzysztofgodzisz.pl</a><br />

Now, I would like to describe both mentioned options.

<b>To download the file from GitHub:</b>

<code>git clone https://github.com/kgodzisz/efd.git</code>

<b>To create your own image in your local repository:</b>

<code>docker build -t efd .</code>

<b>To run the tool:</b>

<code>docker run --rm -v /path/to/folder:/root efd</code>

<b>Another option is to download the prepared file from the Docker Hub repository:</b>

<code>docker run --rm -v /path/to/folder:/root kgodzisz/efd</code>

<b>Description of the options used in the commands: </b>

<code>--rm</code> - the container will automatically remove itself after completing the task;<br />
<code>-v</code> - address to the files you want to compress: the location where the files will be available for archiving and compression. If you don't set /root here, you need to designate the appropriate directory in the Dockerfile;<br />
<code>efd</code> - the name of the created image we want to use;<br />
<code>kgodzisz/efd</code> - the address of the image on the DockerHub platform;<br />

# PocketMoneyMaker

The following sites run a program where they pay little money for a very small part of your internet bandwidth.<p>
It won't make you rich, but opposed to other sites which require you to fill forms, play games etc. these apps require no action from you at all after setting up - a true "Passive Income" :) <p>
I created docker commands optimized for RaspberryPi 3/4 <p>

1. Sign up to one or more of the following sites
2. Use your relevant identification in the docker commands
3. Create the containers
4. Earn money

<a href="https://link.repocket.co/5Tyv" rel="noopener noreferrer" target="_blank">repocket.co</a><p>
<a href="https://traffmonetizer.com/?aff=813170" rel="noopener noreferrer" target="_blank">traffmonetizer.com</a><p>
<a href="https://p2pr.me/16694610166381f418aa4db" rel="noopener noreferrer" target="_blank">peer2profit</a><p>
<a href="https://packetstream.io/?psr=4Xc7" rel="noopener noreferrer" target="_blank">packetstream.io</a><p>
<a href="https://pawns.app?r=1062288" rel="noopener noreferrer" target="_blank">pawns.app</a><p>
<a href="https://r.honeygain.me/MRGAO7878C" rel="noopener noreferrer" target="_blank">honeygain.me</a><p>
<a href="https://earnapp.com/i/paIKIJnU" rel="noopener noreferrer" target="_blank">earnapp.com</a><p>

<a href="https://app.bitping.com?r=a5kAh17b" rel="noopener noreferrer" target="_blank">bitping.com</a><p>
<b>Bitping</b> requires a different setup - the app need to be started at least once in interactive mode for the first connection.
Use the following command in your home folder:
sudo docker run --rm -it -v ${PWD}/.data/.bitping/:/root/.bitping bitping/bitping-node:latest
The container will run and ask for your credentials, after you're succefully authenticated it will create a sub folder with the connection parameters.
Now you can use CTRL+C to stop the container and proceed with the standard docker setup. It will be faster since the image has already been downloaded.
<p> <p>
<b><u>Emulation for ARM devices (RPi)</b></u><p>
In some cases you may encounter an error:<p>
WARNING: The requested image's platform (linux/amd64) does not match the detected host platform (linux/arm64/v8) and no specific platform was requested<p>
To fix that you need to install an emulator using the following command:<p>
sudo docker run --privileged --rm tonistiigi/binfmt --install all<p>
You can find more info <a href="https://enlear.academy/run-amd64-docker-images-on-an-arm-computer-208929004510" rel="noopener noreferrer" target="_blank">here</a>.

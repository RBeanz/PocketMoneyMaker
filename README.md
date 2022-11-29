# PocketMoneyMaker

<p>It won&apos;t make you rich, but opposed to other sites which require you to fill forms, play games etc. these apps require no action from you at all after setting up - a true &quot;Passive Income&quot; &#128521;</p>
<p>I created docker commands optimized for RaspberryPi 3/4</p>
<ol>
    <li>Sign up to one or more of the following sites&nbsp;</li>
    <li>Use your relevant identification in the docker commands&nbsp;</li>
    <li>Create the containers (earnapp and bitping require special attention)&nbsp;</li>
    <li>Earn money</li>
</ol>
<p><a href="https://link.repocket.co/5Tyv" rel="noopener noreferrer" target="_blank">repocket.co</a></p>
<p><a href="https://traffmonetizer.com/?aff=813170" rel="noopener noreferrer" target="_blank">traffmonetizer.com</a></p>
<p><a href="https://p2pr.me/16694610166381f418aa4db" rel="noopener noreferrer" target="_blank">peer2profit</a></p>
<p><a href="https://packetstream.io/?psr=4Xc7" rel="noopener noreferrer" target="_blank">packetstream.io</a></p>
<p><a href="https://pawns.app?r=1062288" rel="noopener noreferrer" target="_blank">pawns.app</a></p>
<p><a href="https://r.honeygain.me/MRGAO7878C" rel="noopener noreferrer" target="_blank">honeygain.me</a></p>
<p><a href="https://earnapp.com/i/paIKIJnU" rel="noopener noreferrer" target="_blank">earnapp.com</a></p>
<p>To register your node with <strong>earnapp</strong>, you need to run the container with a unique hash that you can generate. After running for a few minutes, you will be able to register your hash with earnapp site.</p>
<p>To generate your hash (<em>YOUR_DEVICE_NAME</em> can be any string):</p>
<p><span style="background-color: rgb(239, 239, 239);">echo -n &apos;<em>YOUR_DEVICE_NAME</em>&apos; | md5sum | sed &apos;s/.*/sdk-node-&amp;/&apos;</span></p>
<p>To register your node using the hash use the following link: https://earnapp.com/r/YOUR_HASH</p>
<p><a href="https://app.bitping.com?r=a5kAh17b" rel="noopener noreferrer" target="_blank">bitping.com</a></p>
<p><strong>Bitping</strong> requires a different setup - the app need to be started at least once in interactive mode for the first connection. Use the following command in your home folder: sudo docker run --rm -it -v ${PWD}/.data/.bitping/:/root/.bitping bitping/bitping-node:latest The container will run and ask for your credentials, after you&apos;re succefully authenticated it will create a sub folder with the connection parameters. Now you can use CTRL+C to stop the container and proceed with the standard docker setup. It will be faster since the image has already been downloaded.</p>
<p><br></p>
<p><strong><u>Emulation for ARM devices (RPi)</u></strong></p>
<p>In some cases you may encounter an error:</p>
<p><span style="background-color: rgb(239, 239, 239);">WARNING: The requested image&apos;s platform (linux/amd64) does not match the detected host platform (linux/arm64/v8) and no specific platform was requested</span></p>
<p>To fix that, you need to install an emulator using the following command:</p>
<p><span style="background-color: rgb(239, 239, 239);">sudo docker run --privileged --rm tonistiigi/binfmt --install all</span></p>
<p>You can find more info <a href="https://enlear.academy/run-amd64-docker-images-on-an-arm-computer-208929004510" rel="noopener noreferrer" target="_blank">here</a>.</p>

<b>#Important Tips</b>
1. Do not use $ (dollar sign) in your passwords. Linux environments do not like it.
2. If you think about using a cheap hosted VPS (Virtual Private Server) to run these apps, unfortunately it won't work &#128533;. The apps check the ip address and when it's associated with a hosting platform or a VPN provider they won't use your bandwith.

Estimated reading time: 10 minutes, Audience: Curious party, Noob, [Somewhat experienced], Experienced, Expert
What you will need: Internet connectivity, Browser (Firefox, Chrome or Chromium), Google Account, Docker installation

The test-editor-web consists of the web ui and a couple of service backends that do the heavy lifting for the ui.

In order to get the examples running locally without using hosted services, you need to have a working docker installation including docker-compose. 
Please take a look at https://docs.docker.com/compose/install/ to get this installed quickly.
    
Get a copy of https://github.com/test-editor/tutorials (either by downloading and unpacking the (zip)[https://github.com/test-editor/tutorials/archive/master.zip] or by cloning the (repo)[https://github.com/test-editor/tutorials.git]).

Open a shell in the respective folder

```shell
cd heroes                          # switch to the heroes tutorial
bash run-hero-create-specification # bring up the first tutorial
```

Now is the time to grab a coffee. I'm afraid this will take a while.

The necessary images are fetched from docker-hub (https://hub.docker.com/u/testeditor/) which will take its time, depending on your connectivity. As soon as the images are fully downloaded and extracted the containers are started. Once the containers are ready, the browser is started automatically and you will be presented with the test-editor-web login screen. If something unexpected happens or the whole process is interrupted, it might help to just run `bash run-hero-create-specification` again. Already downloaded elements won't be downloaded again.

You will be asked to login with a Google Account. This will redirect you to Google where you are asked to login and to allow the test-editor-web application to use your account id. The test-editor-web will never know your credentials. Google provides the test-editor-web with an id (no credentials), that's all.

Once logged in, you will be redirected to your locally running instance of the test-editor again. Now the preconfigured tutorial workspace is loaded and you can start using the test-editor-web!

Keep in mind that the initial start of tests will again take some time, since a lot of software libraries that are not prepackaged need to be downloaded from the net. These will however be cached such that the next execution will be much quicker.
 
In order to stop your locally running instance of the test-editor-web, please execute `bash stop-tutorial`.
The images and containers constructed will be kept, so that the next time the test-editor-web is started, the command
`bash run-hero-create-specification` will be much faster, using the already downloaded images and constructed containers.
Keep in mind that all files you create within the test-editor-web will live within the respective docker container. Removing the containers will remove your files, too.
If you want to keep the files you write within this locally installed test-editor-web please run `bash save-repo` which will create an archive with your changes.

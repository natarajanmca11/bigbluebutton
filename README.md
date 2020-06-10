BigBlueButton
=============
BigBlueButton is an open source web conferencing system.  

BigBlueButton supports real-time sharing of audio, video, slides (with whiteboard controls), chat, and the screen.  Instructors can engage remote students with polling, emojis, multi-user whiteboard, and breakout rooms.  

Presenters can record and playback content for later sharing with others.

We designed BigBlueButton for online learning (though it can be used for many [other applications](http://www.c4isrnet.com/story/military-tech/disa/2015/02/11/disa-to-save-12m-defense-collaboration-services/23238997/)).  The educational use cases for BigBlueButton are

  * Online tutoring (one-to-one)
  * Flipped classrooms (recording content ahead of your session)
  * Group collaboration (many-to-many)
  * Online classes (one-to-many)

You can install on a Ubuntu 16.04 64-bit server.  We provide [bbb-install.sh](https://github.com/bigbluebutton/bbb-install) to let you have a server up and running within 30 minutes (or your money back :-).

For full technical documentation BigBlueButton -- including architecture, features, API, and GreenLight (the default front-end) -- see [http://docs.bigbluebutton.org/](http://docs.bigbluebutton.org/).

BigBlueButton and the BigBlueButton Logo are trademarks of [BigBlueButton Inc](http://bigbluebutton.org) .



# Order Of Execution
1. Mongo
2. Redis
3. bbb-html5
4. bbb-webhooks
5. bbb-coturn
6. bbb-freeswitch
7. bbb-kurento

8. bbb-webrtc-sfu
9. bbb-apps-akka
10. bbb-fsesl-akka
11. bbb-web
12. bbb-greenlight
13. bbb-nginx - done
14. traefik
15. bbb-lti

# Minikube start

```
minikube start --cpus=4 --memory=8g --container-runtime=docker --disk-size=25g 
eval $(minikube docker-env)

```

pmoust/red5
===========

[![Gitter](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/pmoust/docker-red5?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

[![Gitter](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/pmoust/docker-red5?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Red5 is an Open Source Flash Server written in Java that supports:

 * Streaming Video (FLV, F4V, MP4, 3GP)
 * Streaming Audio (MP3, F4A, M4A, AAC)
 * Recording Client Streams (FLV and AVC+AAC in FLV container)
 * Shared Objects
 * Live Stream Publishing
 * Remoting
 * Protocols: RTMP, RTMPT, RTMPS, and RTMPE
 * WebSocket (ws and wss)
 * HLS
 * RTSP (From Axis-type cameras)

Available Red5 releases/tags:

* pmoust/red5:1.0.2
* pmoust/red5:1.0.3
* pmoust/red5:1.0.4 (also :latest)

To run:
```
docker run --name red5 --rm -d -p 5080:5080 -p 1935:1935 pmoust/red5
```

To reach the Red5 manager UI visit `http://${DOCKER_HOST}:5080`

To build: 
```
make ${RED5_RELEASE}
```

If no version is passed in `make`, the current :latest is built.

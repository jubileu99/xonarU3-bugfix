## <p align="center"> Sound fix for xonar u3 on Ubuntu 19.10 [20.10 still working ]:sound:</p>

### If you're having some problems with crackles on the audio output consider doing this method.

1) open your terminal
2) gedit /etc/pulse/daemon.conf
3) copy this code below and paste at daemon.conf

#### You must have pulseaudio installed on your system before doing this.


```
    resample-method = src-sinc-best-quality
    default-sample-format = float32ne
    enable-remixing = yes
    default-sample-rate = 48000
    deferred-volume-safety-margin-usec = 16000
    default-fragments = 8
    default-fragment-size-msec = 60
    nice-level = -15
``` 

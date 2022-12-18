---
layout: default
---
![PipeWire](assets/pipewire.gif){:.full.pixels}


[PipeWire](https://gitlab.freedesktop.org/pipewire/pipewire) is a project that aims to greatly improve handling of audio and video under Linux. It provides a low-latency, graph-based processing engine on top of audio and video devices that can be used to support the use cases currently handled by both PulseAudio and JACK. PipeWire was designed with a powerful security model that makes interacting with audio and video devices from containerized applications easy, with support for Flatpak applications being the primary goal. Alongside Wayland and Flatpak, we expect PipeWire to provide a core building block for the future of Linux application development.



- Capture and playback of audio and video with minimal latency.
- Real-time multimedia processing on audio and video.
- Multiprocess architecture to let applications share multimedia content.
- Seamless support for PulseAudio, JACK, ALSA, and GStreamer applications.
- Sandboxed applications support. See Flatpak for more info. 

## Getting PipeWire

PipeWire (0.3) with support for audio use cases should be available in most distributions. Most distributions however will not have enabled the audio parts by default but you can [read here](https://gitlab.freedesktop.org/pipewire/pipewire/-/blob/master/README.md) how to run some examples.

If you want to get the code from GitLab, then the latest PipeWire source code is available at GitLab. To clone the repository, just:

  
```
git clone https://gitlab.freedesktop.org/pipewire/pipewire.git
```

### Setup

PipeWire is using the Meson build system and we provide a convenience script and makefile that makes building PipeWire fairly straightforward: 

```
./autogen.sh --prefix=$PREFIX
make
make install
```

The `$PREFIX` is commonly set to `/usr` or `/usr/local`.

### Running

You can test the PipeWire server from the source directory with:

```
make run
```

To test video capture and display with SDL from the source directory, try this in another window:

```
make shell
```

This sets up the environment variables to run the example apps from the build directory like this:

```
build/src/examples/video-play
```

You can play around with the other examples as well. Don't forget to set the correct environment variables as shown above or else the plugins and modules won't be found.

## Documentation

PipeWire is [documented here](https://docs.pipewire.org/).

Developers can also check out the (incomplete) [PipeWire API documentation](https://docs.pipewire.org/page_api.html).

A collection of other useful pages can be found on the [PipeWire wiki](https://gitlab.freedesktop.org/pipewire/pipewire/-/wikis/home).

## Get Involved

PipeWire is Free Software and is developed in the open. It was created by Wim Taymans, Principal Engineer at Red Hat and co-creator of the GStreamer multimedia framework. Code can be found on [GitLab](https://gitlab.freedesktop.org/pipewire/pipewire).

- Join us on IRC at *#pipewire* on [OFTC](https://www.oftc.net/).
- Issues are tracked on [GitLab Issues](https://gitlab.freedesktop.org/pipewire/pipewire/issues).
- We adhere to the Contributor Covenant for our [Code of Conduct](https://gitlab.freedesktop.org/pipewire/pipewire/blob/master/CODE_OF_CONDUCT.md).
- Follow us on [Mastodon](https://fosstodon.org/web/@pipewire).

<script src="https://liberapay.com/PipeWire/widgets/button.js"></script>
<noscript><a href="https://liberapay.com/PipeWire/donate"><img alt="Donate using Liberapay" src="https://liberapay.com/assets/widgets/donate.svg"></a></noscript>


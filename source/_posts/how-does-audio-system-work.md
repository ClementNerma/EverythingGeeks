---
layout: post
title: How does an audio system actually work?
date: 2020-08-20 22:51:18
categories: Audio series
tags: [Audio, Series]
---

Well, this first post will be about how an audio system works. I told that this blog may not talk only about computer science, and here we are :D !

A little disclaimer, though: this article is meant to be easily understable by people who don't know a bit about how sound and audio hardware works, so many things will be oversimplified for the sake of not losing anyone with complex explanations. I'll make other articles on how certain parts of the process work more precisely, but think of this one as a global overview.

Also, this post will be the first in a long series talking about audio: how does it works, what's the best way to get the best-in-class sound from a given pair of headphones or loudspeakers, and a lot of other things.

Now that these point have been said, let's start!

### The audio source

So first, what is an "audio system"? I'll stick to the simple definition of "a system taking a previously-recorded audio content and converting it to an actually audible sound". Which means, for instance, the path the music takes from your favorite music player to your headphones.

The first part of an audio system is the **source**. First thing to know is, before the sound is actually converted to something we can hear, it is encoded as an electric **signal**. In the vast majority of cases, the source is **digital**, which means it uses digital signals.

In a computer (this also applies to smartphones, tablets, etc.), digital signals work by encoding _bits_, which are base 2 numbers, meaning they can be equal to either `0` or `1`, no other. This corresponds to electricity going through a circuit or not. As digital signals can only encode a limited set of values, we say it carries _discrete values_.

### From digital to analog

So, let's say you're listening to your favorite album on Spotify, YouTube Music, or any other service. Your device streams the music from the service's servers, decodes it, and then transfers it to a little component a **Digital-to-Analog Converter**, or **DAC**.

This component's name is pretty explicit: it converts a digital signal to an **analog** one. What's the difference? Well, unlike digital signals which carries discrete values, analog ones don't. Instead, they just provide electricity like you would find in a power plug, for instance (this is really simplified for the sake of this article's simplicity).

But why do we need to convert our digital signal to an analog one? Well, that's because of how speakers produce sound.

### Amplifying the signal

Before diving into how speakers concretely produce sound, let's talk about a little problem: the signal's power. You see, after our signal was converted to an analog one, it's very weak in terms of electric power. Like, really weak. This _may_ be enough to drive some earphones and headphones, but it will definitely be insufficient for loudspeakers.

So, what do we do? The only we can do: _amplifying_ the signal's power, without degrading it, which is quite a complicated process. For that, we use another component called an **amplifier**.

Note that the amplifier also affects how the output sound... well, sounds, which is why it can be complicated to choose an adequate amplifier, unlike the DAC which is expected to be as neutral as possible when performing the conversion. This is why you may see debate over what is the best between transistor-based amplifiers and tube-based ones for example, but that's another story we'll talk about in another post ;)

### From analogic to audible sound

A speaker, be it headphones, earphones or loudspeakers, uses a _transducer_ to produce the sound. By definition, a transducer is something that converts energy from one form to another. Here, speakers' transducers transform an analog electric signal to a sound wave.

But there's an infinity of possible sounds. Which is why we need analog signals: digital would limit us to a set of possibilities, while analog is, by nature, unlimited.

I'm not going to enter the details of how a transducer works, as that's actually quite complex, but remember it's a component that converts analog signals to sound waves, and also that there's multiple types of transducers, depending on the type of speakers you use (headphones, loudspeakers, ...) as well as the technology chosen by the constructor (orthodynamic, planar magnetic, and a few others).

### The case of vinyls

Vinyls are a special case. Unlike CDs, DVDs, Blu-Rays, MP3 players, streaming services and MP3 files, which all carry digital informations, vinyls actually use analog signals.

When a sound recording is written to a vinyl, the information is written in a way that _can_ be infinitely precise ; and the same goes when reading it with a vinyl turntable. This is why, while CDs can be read by any low-cost player without any problem, vinyls require a good vinyl turntable if you want to get the best sound from it (at least if you have good speakers to listen from).

This also means that, when you're listening to a vinyl, you don't need a DAC to convert the sound.

### What about Bluetooth?

Bluetooth works just like streaming music from your favorite music provider: it transmits a digital signal from one device to another, but it does that completely wirelessly, while your internet connection is always wired (unless you use Wi-Fi of course, but your internet line in itself is still wired).

### Conclusion

So, know you know how an audio system work! Here's a sum up just in case:

```
       [Source]              Produce a digital signal

          ⬇

        [DAC]                Converts the digital signal to an analog one

          ⬇

     [Amplifier]             Amplifies the signal to get enough power

          ⬇

     [Transducer]            Produces sound wave from the amplified audio signal

          ⬇

  [Your ears d-_-b]          Enjoying the music 👌
```

I hope you enjoyed this article. If you found any issue here, feel free to [open an issue on GitHub](https://github.com/ClementNerma/EverythingGeeks/issues/new), where you can also find this blog's source code.

See you in the next article! ;)
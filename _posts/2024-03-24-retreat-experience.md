---
layout: post
title:  "Experiences from the first OCaml Retreat"
date:   2024-03-24 11:13:42 +0530
---

# Experiences from the first OCaml Retreat

## prometheansacrifice
Incredibly grateful for the retreat. Enjoyed meeting KC and all the other smart folks. Learnt a ton about compiler internals. Loved the late night discussions on Functional Programming, OCaml tooling. Looking forward to continue hacking on the compiler, markdown generation of odocs, using dune to build the compiler's sourcetree.

## Kaushik Hatti

Imagine a bug crawling near you. You decide to squish it with your thumb. When you lift your thumb, you realize that the bug is still alive. You show pity on it and decide not to squish again. The bug is humbled by your strength but decide to move forward anyway. It slowly yet steadily starts to crawl again.

I am the bug humbled by the awesome retreat!

My intention to come to the retreat was to know “What I didn’t know that I didn’t know”. Now that I have known what I didn’t know, I will start working on it. As a starter, I enjoyed toying with "Joy" using OCaml to draw. Now, I am trying to understand MirageOS and its unique capabilities. This, I feel is a new beginning to both me and our organization. Hoping to meet you again in the following retreat.

Best,
Kaushik

## Shakthi

At the retreat, I had a wonderful opportunity to interact with interested OCaml developers. While I continued to work on OCaml.org issues, I also spent time on MirageOS projects.

The steps to build the [mirage-www HTML documentation](https://hackmd.io/vemFYWJwRnibGz8mjmq-pA) pages for the MirageOS project and run the same on a solo5 unikernel on an x86_64 Ubuntu 22.04 LTS system have been tested and documented. I gave a brief presentation on the MirageOS library operating system, and also played the [demo video for Raspberry Pi](https://watch.ocaml.org/w/1RhQXW5NNqRtdxXgi12pD9).

The CI build failures for the MirageOS packages have been reproduced on Alpine 3.19 Docker images, and possible patches for some of the packages have been documented at [Fix MirageOS Libraries on CI](https://hackmd.io/_0QAwb0rS72wDx52hkegPA).

The changes required to build OCaml documentation from webman/<compiler-version> and webman/api folders in the OCaml sources have been made, and the corresponding [ocaml/ocaml/12976](https://github.com/ocaml/ocaml/pull/12976) PR was updated.

Although we were on a limited Internet connection, I managed to stream twice and covered the "Basic Data Types and Pattern Matching" documentation from the [Basic Data Types](https://ocaml.org/docs/basic-data-types) OCaml.org site. The video recordings of [Part I](https://www.youtube.com/watch?v=ky7dmhjVe4E) and [Part II](https://www.youtube.com/watch?v=ehU9u4-yAic) are available.

See you in the next retreat!

## Shubham

- Motive

    From the Hackacamel list I picked up working on the cdf plotter using TUI. Now I have never developed TUIs or GUIs so I thought this would be the perfect thing to do.

    The initial hurdle was choosing the library, I wanted to try use OCaml 5 so I chose Minttea which is TUI framework inspired by Bubble Tea implemented in Golang and uses the The elm architecture.

- Biggest Hurdles
    - Learning Minttea, Esy and Fmt

        Since Minttea is a nascent framework I knew it would be a little difficut to learn but the examples provided helped me get to
        a working mvp quickly although I added some of my own hurdles just to learn stuff. This was not my motive but I like shock therapy.

        And I have tinkering with esy for a while and I thought let's try and build a esy-dune workflow to build my projects.

        And it was simple to build and play with things. I realised I don't need to have a `.merlin` file if I am using dune.
        Dune has a nice way of getting the LSP up and running even with esy. One only needs to specify the dependencies 
        and dev dependencies : Tools that one plans to use like ocaml-lsp-server, ocamlformat etc.

        And one more thing : just use `esy` prefix to build stuff like : `esy dune build ./bin/main.exe` to build and `esy dune exec ./bin/main.exe`

        I was also scared with the Fmt library I have never been able to use the `Format` library because a lot of things don't make sense
        and I think this blurb wouldn't be enough for explaining that but I realised `Fmt` is a nice way to use `Format` because there are ways to sanity check
        using `Fmt.Dump.<data-structure>`. Later I got to know about `pp` pretty printer. Which is something that I didn't know and I am thankful for Thibbaut for that.

- Was I able to achieve my goal?

    Nope, it was hard for me to get a dot printed on the first day because I realised a lot of special characters weren't supported in my outdated version of alacritty.

    And then the second day I was able to get the cartesian axis but I couldn't go further in day 3 and day 4.

    Mostly because I was kind of having a hard time able to resize the axis for different sizes of terminals and also is there a better way to do it.

- What does it look like now
    [This](https://ibb.co/VmR6m3w) the repo is [here](https://github.com/shubhamkumar13/cdf-plotter). But I think even it looks like nothing (because it is nothing) I am happy that I started working on this.
- What next?

    Well for one, if you clone this repo there are things that might not work because I am trying to parse the output olly generates.
    My plan is to get the repo useful for plotting multiple benchmarks on TUI.

    And I am seriously considering working on more GUIs and TUIs because it was fun.

    I am hoping to it finish this weekend. At least plotting a static graph. 
    Resizing seems like a non-trivial problem but I am sure the TUI communities might have solved it.

- Thanks

    I want to thank KC, Sudha and Ganesh for organizing OCamlretreat, it was a blast I wish to come again next time. 


## Karthik Ravikanti

I found the retreat when I was at the bottom of a pit, motivationally. I've been trying to get out of a multi year rut and it seemed like something that could do the trick.

While my recovery is still a work in progress, I did walk away with a lot of value from the short retreat.

Coming from a Haskell and Rust background, I struggled to see the additional value I'd get from OCaml, so this was a perfect venue for me to explore it. Getting the facts straight from the source was very valuable. Seeing the faith and energy everybody put into this language was very inspiring.

Other than that, connecting to other functional programmers/learners in person after a long time felt amazing. Also great was being able to interact with people from my own culture with similar taste. The atmosphere at the retreat was very collegiate and I came out of my (recent) shell and felt like I could be useful again.

Going forward, I hope to contribute to the community in the form of meetups in Singapore and future collaboration with the peers I met at the retreat.

While I mostly spent the time going through tutorials and briefly teaching Haskell (gasp!), I'll be forever grateful for the very welcoming and generous disposition everyone displayed. Almost every conversation I had was either very therapeutic, encouraging, engaging or inspiring.

I can't wait for the next one.

## KC Sivaramakrishnan

My goal at the retreat was to spend some quality time hacking on a long list of things including the OCaml compiler (to break a long hiaitus of no OCaml compiler contributions), trying to port my CS3100 lecture notes to purely client-side pages using js_of_ocaml / wasm_of_ocaml, spend time playing around with LLMs and OCaml. As with any ambitious plan, I got nowhere close to working on everything that I had planned :-) But I did manage to break my OCaml compiler contribution rut by reviewing a couple of PRs and rebasing the [PR](https://github.com/ocaml/ocaml/pull/12309) that adds syntax support for effect handlers in OCaml. Generally, it was great to be surrounded by people who were keen to learn about OCaml and its ecosystem.

## C R Anish

I was very happy when I got the email offering a spot to attend the OCaml retreat at Auroville as I was not sure if I was qualified for it.

Being an OCaml newbie, I was not sure what to work on. The HackaCamel list of ideas to work on during the retreat (and beyond) helped me. I choose to go through the OCaml5 tutorial, Parallel Programming in multicore OCaml tutorial and OCaml Effects tutorial.

There was high energy level in the guest house. I was very productive and learnt much more OCaml in those four days than past few weeks. I could complete the first two tutorials and half of the Effects tutorial.

Interaction with KC helped me to understand Effects better and faster.

I consider myself an introvert and was apprehensive about spending four days with strangers. But the moment I stepped into the guest house, seeing the welcoming attitude of all, I knew I will enjoy the company. All were very friendly and approchable.

Thanks to Ganesh and Sudha for making excellant arrangements.

I wish I knew more OCaml to ask questions to the various experts who were present. Hope to do it in the next retreat.

My plan is to learn OCaml and contribute to its opensource projects this year. The retreat has provided enough motivation and ideas for this.

Thanks to the organisers for allowing my wife to work on her official project (not related to OCaml). She too had a great time.

## Kaustubh

I went to the retreat not knowing what to expect. All I had thought of was that there would be no distractions and this would be a good week to focus on getting something done. That was there, but the retreat was so much more than that. All the informal interactions - asking for help, discussing each other's work, talking about X interesting thing - were instead the highlight for me.  There was so much to learn from each other and with each other.

Being at a job where I don't write OCaml full-time, it was pleasant to have a week where I did not have any distractions and could easily ask for help when I needed it.

It was wonderful being in such company. I am glad I signed up.

## Puneeth

I really enjoyed being at the retreat with people who do cool things everyday,
and are eager to learn and teach OCaml and FP.

It gave me a chance to explore corners of the OCaml world that I'm usually not
in -- I really enjoyed deep diving into Effects and Effect handlers into OCaml,
and came out have a bunch of follow-up reading and coding to do. I spent a
bunch of time digging into things like OCaml's Format and the Fmt library too,
trying to understand the smart line breaks support.

I made a couple of small contributions to OCaml Joy while helping Ganesh make
his first contribution. Ganesh and I made a small contribution to Okra, as
well, along with some personal workflow improvements for Ganesh by
incorporating local okra runs into it.

I've an incomplete attempt at creating a template repo for YOCaml, along with a
nice theme, which I'll probably "finish" at some point. My experiments with
[mldoc](https://github.com/logseq/mldoc) as a parser for org-mode files didn't
go very well, and paused on them.

It was a really nice and friendly learning experience; I would sign-up again!


## Ganesh

The OCaml retreat at Auroville was a memorable one, especially for me. I made my first contribution to OCaml during this retreat.  

I came to this retreat to learn how Okra works. Since I'm working on extracting the raw data from the engineers' weekly reports, I wanted to understand how the tool(Okra) works, which could be helpful for me later. 

I was new to coding. So, Puneeth suggested starting with OCaml Joy. Thanks to Sudha and Kaustubh, I started learning OCaml Joy. It was fun playing with Joy. Later, I created a new [PR](https://github.com/Sudha247/ocaml-joy/pull/124) with the help of Puneeth, Sudha and Kaustubh to draw a smile emoji using Joy. 

I also worked on a couple of issues on Okra with Puneeth. Puneeth helped me understand how the code works. I shadowed his work while closing the issues on Okra. It was nice working with Puneeth.

It was nice to learn OCaml during this retreat. I was pleased that the retreat went very well. Thanks to Sudha for taking the initiative to organise the accommodation, stay, food and the architecture tour that we attended. 

In a time when it is challenging to meet your peers regularly, it was lovely to spend time together for a week and learn new things. 

    
## Sudha
    
I had a wonderful time at the OCaml retreat! I wanted to use the time at the retreat to do some stuff on [joy](https://github.com/Sudha247/ocaml-joy). I ended up reviewing some PRs, and we got many new users and contributors. With Kaustubh, we also played around a bit with mandelbrot simulations using joy.
    
I wanted to create a wasm backend for joy, similarly to the js_of_ocaml backend. I initially had some trouble installing wasm_of_ocaml on my machine, and later found workarounds to it and fixed it in the upstream repository too. It'd still be nice to experiment with joy on wasm.
    
I also ended up writing a Dream version of [Web Frameworks Benchmarks](https://web-frameworks-benchmark.netlify.app/result) (that I need to upstream!).
    
Apart from all the hacking, it was great to be amongst a bunch of OCaml and FP enthusiasts and learn from them. Looking forward to more OCaml retreats in the future!

[![Build Status](https://travis-ci.org/carlosrabelo/mars.png)](https://travis-ci.org/carlosrabelo/mars)

# MARS (MIPS Assembler and Runtime Simulator) 

MARS, but with various pointless patches. Maybe don't use this modification.

At some point I messed up the "fork" thing, but this is a fork of this: [https://github.com/gon1332/mars](https://github.com/gon1332/mars)

I wrote a [Nix](https://nixos.org/) shell script if you
don't want to bother with dependencies.

## New Features:

- [XKCD Off-By-One Fix](#xkcd-off-by-one-fix)
- [ChatGPT Integration](#chatgpt-thing)

### XKCD Off-By-One Fix

Inspired by [This Comic](https://xkcd.com/3062/), this setting fixes all
off-by-one errors by adding far more off-by-40–50 errors. Enable it in the
settings drop-down menu.

![Position of the XKCD setting](images/xkcd.png)

This happens entirely on the simulated CPU. This would not occur on an actual
VM or hardware (unless you really messed it up).

### ChatGPT thing

Edit the file at src/main/java/mars/tools/ChatGPT.java and put your OpenAI key
at the top in the OPENAI_API_KEY constant. You can also use Ollama by changing
the endpoint.

If you want to change the model, temperature, whatever, look in the
`buildRequestBody` method. As of writing, it is using gpt-3.5-turbo and a temp
of 1.

ChatGPT will be in the Tools menu.

![An image of the ChatGPT window](images/screenshot_of_chatgpt.png)

Yes, I know it gave an incorrect answer. Doubles cannot be loaded into $f3. Take
this as a warning to not rely on AI.

Original Readme follows:

# An IDE for MIPS Assembly Language Programming!

MARS has been jointly developed by Pete Sanderson (programming) and Ken Vollmar (details and paperwork).

CCSC-MW paper, "A MIPS Assembly Language Simulator Designed for Education." Ken Vollmar and Pete Sanderson. Journal of Computing Sciences in Colleges, 21:1, October 2005. Pages: 95 - 101.

SIGCSE 2006 paper, "MARS: An Education-Oriented MIPS Assembly Language Simulator," Kenneth Vollmar and Pete Sanderson. ACM SIGCSE Bulletin, 38:1 (March 2006), 239-243.

MARS presentations by Pete Sanderson at Bowling Green State Univ. (2006) and University of Pittsburgh (2007).

Tutorial on MARS at CCSC-CP, Drury University, Apr. 13-14, 2007, by Pete Sanderson and Ken Vollmar

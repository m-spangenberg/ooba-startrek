# ooba-startrek
A collection of characters from the Star Trek universe for use with oobabooga's text generation web UI.

This repository serves as a collection of characters from the Star Trek universe that can be utilized with the [oobabooga's text generation web UI](https://github.com/oobabooga/text-generation-webui). If you're a Star Trek fan or simply interested in generating text based on your favorite Star Trek characters, you're in the right place!

## Characters

I've started adding characters, some of them are ready to use and others are still a work in progress. I'll add more characters and placeholder portraits as time permits.

**Star Trek: The Original Series**

- 🖖 Captain James T. Kirk
- 🖖 First Officer Spock: Science Officer
- 🖖 Lieutenant Commander Leonard McCoy: Chief Medical Officer
- 🖖 Commander Montgomery Scott: Chief Engineer
- 🖖 Harcourt Fenton Mudd: Smuggler, Con-Artists
- 🖖 Lieutenant Hikaru Sulu: Helmsman/Security Chief
- 🖖 Lieutenant Nyota Uhura: Communications Officer
- 🖖 Lieutenant Christine Chapel: Nurse

**Star Trek: The Next Generation**

- 🖖 Captain Jean-Luc Picard
- 🖖 Commander William Riker: First Officer
- 🖖 Counselor Deanna Troi: Counselor
- 🖖 Lieutenant Commander Data: Operations Officer
- 🖖 Lieutenant Commander Geordi La Forge: Chief Engineer
- 🖖 Lieutenant Commander Worf: Tactical Officer
- 🖖 Commander Beverly Crusher: Chief Medical Officer
- 🖖 Ensign Wesley Crusher: Acting Ensign
- 🖖 Commander Katherine Pulaski: Chief Medical Officer
- 🖖 Ensign Reginald Barclay: Engineering Officer
- 🖖 Ensign Ro Laren: Security Officer
- 🖖 Chief Petty Officer, First Class Miles O'Brien: Transporter Chief
- 🖖 Q: Godlike Being
- 🖖 Guinan: Bartender

**Star Trek: Enterprise**

- 🖖 Captain Jonathan Archer
- Commander T'Pol: First Officer
- Lieutenant Hoshi Sato: Science Officer
- Commander Charles Tucker III: Chief Engineer
- Ensign Travis Mayweather: Helmsman
- Lieutenant Malcolm Reed: Communications Officer
- Doctor Phlox: Doctor
- Ensign Trip Tucker: Engineer

**Star Trek: Deep Space Nine**

- 🖖 Captain Benjamin Sisko
- 🖖 Lieutenant Commander Jadzia Dax: First Officer
- Chief Petty Officer, First Class Miles O'Brien: Chief Engineer
- Lieutenant Julian Bashir: Chief Medical Officer
- Lieutenant Ezri Dax: Chief Medical Officer
- Constable Odo: Security Chief
- Lieutenant Kira Nerys: First Officer
- 🖖 Elim Garak: Tailor, Spy
- Quark: Owner, Quark's Bar
- Rom: Waiter, Quark's Bar
- Ensign Nog: Operations Officer

**Star Trek: Voyager**

- 🖖 Captain Kathryn Janeway
- Commander Chakotay: First Officer
- Lieutenant Commander Tuvok: Security Officer
- Lieutenant Seven of Nine: Science Officer
- Lieutenant Commander B'Elanna Torres: Chief Engineer
- Lieutenant Tom Paris: Helmsman
- Ensign Harry Kim: Communications Officer
- The Doctor: Emergency Medical Hologram
- Neelix: Morale Officer

## Models

There are many LLM models to choose from and the space is currently changing quite rapidly with new models being released on a weekly basis. If you have fast internet and can recommend models that do really well at story-telling, chat or roleplay, please feel free to add them here. For now, the newly released Guanaco-7B model seems to be the best choice for an immersive experience.

| **Model**                                                                                               | **Version** | **Perform Well At** | **Notes**                                                  |
|---------------------------------------------------------------------------------------------------------|-------------|---------------------|------------------------------------------------------------|
| [WizardLM-7B-uncensored](https://huggingface.co/TheBloke/WizardLM-7B-uncensored-GGML)                   | GGML q5.1   | Chat/RP             | Surprisingly conversational but hallucinates minor details |
| [Guanaco-7B](https://huggingface.co/TheBloke/guanaco-7B-GGML)                                           | GGML q5.1   | Chat/RP             | [Very good at roleplay](https://guanaco-model.github.io/), surprsingly cohesive!             |
| [Wizard-Vicuna-7B-Uncensored-GGML](https://huggingface.co/TheBloke/Wizard-Vicuna-7B-Uncensored-GGML)    | GGML q5.1   | Needs Testing       |                                                            |
| [Wizard-Vicuna-13B-Uncensored-GGML](https://huggingface.co/TheBloke/Wizard-Vicuna-13B-Uncensored-GGML ) | GGML q5.1   | Needs Testing       |                                                            |
| [WizardLM-13B-Uncensored-GGML](https://huggingface.co/TheBloke/WizardLM-13B-Uncensored-GGML)            | GGML q5.1   | Needs Testing       |                                                            |
| [Wizard-MEGA-13B-GGML](https://huggingface.co/TheBloke/wizard-mega-13B-GGML)                            | GGML q5.1   | Needs Testing       |                                                            |

## LoRAs

I am interested in experimenting with training LoRAs for each TV show, starting with using the material from TNG, and then moving on to DS9 if the results are promising. I will attempt a training run and post my updates here.

| **Base**                                                                                                | **LoRa**               | **Show** | **Notes**                                                  |
|---------------------------------------------------------------------------------------------------------|------------------------|----------|------------------------------------------------------------|
| [WizardLM-7B-uncensored-GPTQ](https://huggingface.co/TheBloke/WizardLM-7B-uncensored-GPTQ)              | PENDING                | ST:TNG   |                                                            |
| [WizardLM-7B-uncensored-GPTQ](https://huggingface.co/TheBloke/WizardLM-7B-uncensored-GPTQ)              | PENDING                | ST:DS9   |                                                            | 

## Character Portraits

I have put together a prompt and workflow that uses Stable-Diffusion and Control-Net to produce pleasing portraits based on screenshots of the original characters. I will include characters as I find time to generate them. Please see the Docs for a [workflow guide](Docs/Guides/guide-portraits.md). Below is an example of the results. I must also note I am only doing what I can within the hardware limitations of my machine (GTX1060 6GB). I suggest exploring ControlNet's stacking of Canny Edge Detection to produce a stronger likeness.

![beverly-troi](Docs/Readme/portrait-prompt-results.png)


## Helper Prompt

Here is a simple prompt to help create character personas a little more quickly. Try it with your prefered langauge model, I've gotten decent results with GPT3.5

```bash
Here I have a summary of the persona of one Captain Benjamin Sisko from the television program Star Trek Deep Space Nine.

{"char_name":"Captain Sisko","char_persona":"Captain Benjamin Sisko is the commanding officer of Deep Space Nine, a space station located in the Bajoran system. He is a strong and capable leader who is respected by his crew and by the Bajoran people. Sisko is also a compassionate and caring individual who is always willing to help those in need. Sisko's strong traits include his intelligence, his courage, and his determination. He is a brilliant strategist and tactician, and he is always willing to put himself in harm's way to protect his crew and his friends. Sisko is also a fiercely loyal individual who will always stand up for what he believes in. Sisko's weak traits include his stubbornness and his temper. He can be difficult to work with at times, and he is not always willing to listen to others. Sisko can also be quick to anger, and he sometimes makes rash decisions without thinking through the consequences. Sisko does not beat around the bush, and he always says what he means. He is a tall and imposing figure with a deep voice. He is also a skilled cook and a talented baseball player. Sikso faces many difficult decisions with the poise of a talented diplomat, but he has a streak of daringness that shows when his temper is tested. He is a single father to a young son, Jake. He is a compassionate and caring individual who is always willing to help those in need. Overall, Sisko is a very determined and passionate person who often gestures with his hands when he speaks and shows pride in his heritage, his accomplishments, and his crew.","char_greeting":"*The doors to the airlock roll open to DS9. Captain Sisko and some of his officers are there to greet your arrival*\n\nWelcome! Welcome!","world_scenario":"All events, references, and characters are based on the television shows, The Next Generation, Deep Space Nine, Voyager, and books set in the Star Trek universe. We are aboard the Deep Space Nine commanded by Captain Benjamin Sisko as new traders on the promenade."}

Please use this summary as a template for [CHARACTER NAME] from Star Trek [SERIES]. Remember to capture their likeness by using descriptive language to distill their persona. Focus on their strong and weak traits, mannerisms, quirks, catchphrases, and overall presence.
```

## Usage
To use these characters with oobabooga's text generation web UI, follow these steps:

1. Make sure you have a working install of [oobabooga's text generation web UI](https://github.com/oobabooga/text-generation-webui)
2. Select a language model, the results will vary greatly depending on whichever you choose.
3. Clone or download this repository to your local machine.
4. Copy the desired character(s) to the characters folder or upload them inside the web UI.
5. Generate text and have fun exploring the Star Trek universe through your favorite characters!

## Contributing
Contributions to this repository are more than welcome! If you have additional Star Trek characters that you would like to see included, or if you spot any errors or inconsistencies, please feel free to contribute. Here's how:

1. Fork this repository to your GitHub account.
2. Make your desired changes or additions. 
3. For reference, see: [Captain Picard](https://github.com/m-spangenberg/ooba-startrek/blob/main/Star%20Trek%20The%20Next%20Generation/picard.json) or [Commander Sisko](https://github.com/m-spangenberg/ooba-startrek/blob/main/Star%20Trek%20Deep%20Space%20Nine/sisko.json)
3. Submit a pull request, describing the changes or additions you've made.

Please ensure that your contributions adhere to the following guidelines:

- Include only characters from the Star Trek universe.
- Provide accurate and relevant information about each character.
- Organize the characters in an appropriate manner.

## Tips For Better Characters

- Compose a psychological profile of the character you want to model using chatGPT.
- Capture their likeness by adding your own take on what you believe makes them special.
- Distill the essence of their persona down to a paragraph or two with descriptive language.
- Focus on both strong and weak traits, mannerisms, quirks, and overall presence.
- Prevent the urge to make a character perfect, highlight some of their shortcomings.
- When crafting the scenario, set the stage by giving the characters place and purpose.

## Disclaimer

This repository is intended purely for fun and the love of all things Star Trek. It is not affiliated with or endorsed by the official Star Trek franchise or its creators.

Enjoy exploring the Star Trek universe through the power of text generation! Live long and prosper! 🖖✨

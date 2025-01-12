# Munthy's EqualizerAPO Config

## How to add EQs for other headsets
1. Find headset at [Oratory1990 headset list](https://old.reddit.com/r/oratory1990/wiki/index/list_of_presets)
2. Open **harman target (over-ear)** pdf for headphones or **oratory1990 target** pdf for IEMs (in-ear plugs)
3. Copy **Filter settings** found in the lower left of the pdf
4. Tell AI chatbot of choice (I'm using ChatGPT) to format the copied settings in the following pattern:

```
Filter: ON LSC Fc 30 Hz Gain 9.0 dB Q 0.71  
Filter: ON LSC Fc 100 Hz Gain 5.5 dB Q 0.71  
Filter: ON PK Fc 200 Hz Gain -2.5 dB Q 0.8  
Filter: ON PK Fc 1330 Hz Gain -2.5 dB Q 1.8  
Filter: ON HSC Fc 1700 Hz Gain 4.0 dB Q 0.71  
Filter: ON PK Fc 3300 Hz Gain -2.1 dB Q 1.7  
Filter: ON PK Fc 5520 Hz Gain -6.4 dB Q 3.8  
Filter: ON PK Fc 8000 Hz Gain 3.0 dB Q 1.4  
Filter: ON HSC Fc 10000 Hz Gain -2.0 dB Q 0.71  
```

5. Copy the result to a `HEADSET_NAME_FILTER_NAME.txt` file and add it to the EqualizerAPO config folder
6. Add a Preamplification filter in EqualizerAPO main config file and set the value to **Preamp Gain** in the PDF
7. Add a Control -> Include node and set it to the `HEADSET_NAME_FILTER_NAME.txt` file

To switch between presets, turn turn both the preamp filter and include on and off for each corresponding headset.

***

You can also tune each EQ further by opening `HEADSET_NAME_FILTER_NAME.txt` file in EqualizerAPO. Just remember to only have preamp and include nodes in the main `config.txt` file.

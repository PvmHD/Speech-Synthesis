Speech-Synthesis
================
Speech synthesis is the artificial production of human speech. A computer system used for this purpose is called a speech synthesizer, and can be implemented in software or hardware products. A text-to-speech (TTS) system converts normal language text into speech; other systems render symbolic linguistic representations like phonetic transcriptions into speech.


The AVSpeechSynthesizer class produces synthesized speech from text on an iOS device, and provides methods for controlling or monitoring the progress of ongoing speech.

To speak some amount of text, you must first create an AVSpeechUtterance instance containing the text. (Optionally, you may also use the utterance object to control parameters affecting its speech, such as voice, pitch, and rate.) Then, pass it to the speakUtterance: method on a speech synthesizer instance to speak that utterance.

The speech synthesizer maintains a queue of utterances to be spoken. If the synthesizer is not currently speaking, calling speakUtterance: begins speaking that utterance immediately (or begin waiting through its preUtteranceDelay if one is set). If the synthesizer is speaking, utterances are added to a queue and spoken in the order they are received.

After speech has begun, you can use the synthesizer object to pause or stop speech. After speech is paused, it may be continued from the point at which it left off; stopping ends speech entirely, removing any utterances yet to be spoken from the synthesizer’s queue.

You may monitor the speech synthesizer by examining its speaking and paused properties, or by setting a delegate. Messages in the AVSpeechSynthesizerDelegate protocol are sent as significant events occur during speech synthesis.

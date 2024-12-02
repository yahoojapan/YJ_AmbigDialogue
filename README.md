# YJ_AmbigDialogue
In intelligent assistants that perform both chatting and tasks through dialogue, like Siri and Alexa, users often make ambiguous utterances such as "I'm hungry" or "I have a headache," which can be interpreted as either chat or task intents. Naively determining these intents can lead to mismatched responses, spoiling the user experience. Therefore, it is desirable to determine the ambiguity of user utterances. 

We created a dataset from an actual Japanese intelligent assistant ([Yahoo! Voice Assist](https://v-assist.yahoo.co.jp/)) via crowdsourcing. Using this labeled data of chat, task, and ambiguous intents, we can develop an intent classification model capable of detecting ambiguous utterances.

For more information, please check the descriptions in the [paper](https://aclanthology.org/2024.emnlp-industry.28.pdf).

## Dataset description
Each line contains labels and dialogue data separated by tabs.
The label in the first column corresponds to: '0' for casual conversation, '1' for task-oriented dialogue, and '2' for ambiguous intent.
The columns following the second contain the dialogue data corresponding to the label, where each column stores either a user utterance (u) or a system response (r).
Specifically, the second column corresponds to \(u_0\), the third to \(r_{-1}\), the fourth to \(u_{-1}\), the fifth to \(r_{-2}\), and the sixth to \(u_{-3}\).

## License
[Creative Commons Attribution 4.0 License](https://creativecommons.org/licenses/by/4.0/legalcode)

## Citation

```
@inproceedings{akasaki-sassano-2024-detecting,
    title = "Detecting Ambiguous Utterances in an Intelligent Assistant",
    author = "Akasaki, Satoshi  and
      Sassano, Manabu",
    editor = "Dernoncourt, Franck  and
      Preo{\c{t}}iuc-Pietro, Daniel  and
      Shimorina, Anastasia",
    booktitle = "Proceedings of the 2024 Conference on Empirical Methods in Natural Language Processing: Industry Track",
    month = nov,
    year = "2024",
    address = "Miami, Florida, US",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2024.emnlp-industry.28",
    pages = "386--394",
    abstract = "In intelligent assistants that perform both chatting and tasks through dialogue, like Siri and Alexa, users often make ambiguous utterances such as {``}I{'}m hungry{''} or {``}I have a headache,{''} which can be interpreted as either chat or task intents. Naively determining these intents can lead to mismatched responses, spoiling the user experience. Therefore, it is desirable to determine the ambiguity of user utterances. We created a dataset from an actual intelligent assistant via crowdsourcing and analyzed tendencies of ambiguous utterances. Using this labeled data of chat, task, and ambiguous intents, we developed a supervised intent classification model. To detect ambiguous utterances robustly, we propose feeding sentence embeddings developed from microblogs and search logs with a self-attention mechanism. Experiments showed that our model outperformed two baselines, including a strong LLM-based one. We will release the dataset.",
}
```

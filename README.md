# Transformer Training 09 — Memory: Sixteen Bytes per Parameter, and Activations

LLaMA 7B's weights take 13.5 GB, yet training it needs far more. Sixteen bytes per parameter for mixed-precision Adam, activations that grow with sequence and batch, and the trade activation checkpointing makes: a live calculator.

**Live site:** https://brendanjameslynskey.github.io/Transformer_Training_09_Memory/

Sixteen bytes per parameter; Korthikanti et al.'s activation formula; LLaMA 7B by the calculator (interactive); full and selective activation checkpointing; the Decoder's model counted against the formula.

## Live, animated companion

This deck is the slide companion to [Training](https://transformer-training-explained.vercel.app/training), the second site of the Foundations track (after Decoder), where the Decoder's model trains in your browser:

- [Chapter 10: Memory](https://transformer-training-explained.vercel.app/training/10-memory)

## Where the numbers come from

Every measured number on these slides comes from the site's [results.md](https://github.com/BrendanJamesLynskey/transformer-explainer/blob/main/results.md) (seeded NumPy reference runs; CI recomputes them), filled in at build time from its `results.json`. Numbers from papers are cited on the slide with a link. The model is tiny (5,376 parameters, one book, a CPU): its runs show mechanisms, not what happens at scale, and the slides say so where it matters. GPU runs of the site's Colab notebooks are pending; no GPU number appears here.

Part of the [Transformer Training sub-hub](https://github.com/BrendanJamesLynskey/LLM_Hub_Transformer_Training) &middot; [LLMs hub](https://github.com/BrendanJamesLynskey/LLMs)

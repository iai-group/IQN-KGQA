# Would You Ask it that Way? Measuring and Improving Question Naturalness for Knowledge Graph Question Answering

This repository provides resources developed within the following article:

> T. Linjordet, K. Balog. **Would You Ask it that Way? Measuring and Improving Question Naturalness for Knowledge Graph Question Answering.** SIGIR’22.  [[PDF](https://arxiv.org/pdf/2205.12768.pdf)]

## Summary

*Knowledge graph question answering (KGQA) facilitates information access by leveraging structured data without requiring formal query language expertise from the user.  Instead, users can express their information needs by simply asking their questions in natural language (NL).  Datasets used to train KGQA models that would provide such a service are expensive to construct, both in terms of expert and crowdsourced labor.  However, the resulting datasets often fall short of representing genuinely natural and fluent language.  In the present work, we investigate ways to characterize and remedy these shortcomings.  We create a KGQA test collection by sampling questions from existing KGQA datasets and evaluating them with regards to five different aspects of naturalness.  Then, the questions are rewritten to improve their fluency.  Finally, the performance of existing KGQA models is compared on the original and rewritten versions of the NL questions.  We see that some KGQA systems fare worse when presented with more realistic formulations of NL questions.  The new test collection is provided to help evaluate KGQA systems in a more realistic setting.  The construction of this new test collection also sheds light on the challenges of constructing large-scale KGQA datasets with genuinely NL questions.*

## IGN-KGQA test collection

The main resource developed in our paper was the "Improving Question Naturalness for Knowledge Graph Question Answering" (IQN-KGQA) test colletion. 

This repository is structured as follows:

- `test_collection/`: Contains the files that constitute the test collection IQN-KGQA.
    - `final_questions.csv`: Original and final NL questions in test collection. This CSV file has four columns: `Dataset`, `QID`, `OriginalQuestion`, and `FinalQuestion`. 
    - `DBNQA\*/`: Contains the files corresponding the NL questions sampled from DBNQA*. 
       - `test_sample_original.en`: The original NL questions sampled from DBNQA* test split. 
       - `test_sample_final.en`: The final NL questions after crowdsourced rewrites were substituted. 
       - `test_sample.sparql`: The SPARQL queries corresponding line-by-line to either of the two preceding NL questions files.
    - `GrailQA_v1.0/`: Contains the files corresponding to the instances sampled from GrailQA v1.0.
        - `grailqa_v1.0_dev_sample_original.json`: The original instances (including NL questions) sampled from GrailQA dev split.
        - `grailqa_v1.0_dev_sample_final.json`: The final instances with NL questions substituted by crowdsourced rewrites.
    - `LC_QuAD_2.0/`: Contains the files corresponding to the instances sampled from LC-QuAD v2.0.
        - `test_sample_original.json`: The original instances (including NL questions) sampled from LC-QuAD v2.0 test split.
        - `test_sample_final.json`: The final instances with NL questions substituted by crowdsourced rewrites.

### Detailed description of `final_questions.csv`

In the file `test_collection/final_questions.csv`, the QID column is populated by the respective question ID from the original dataset (`Dataset`), except for those rows with original questions sampled from DBNQA*, where the QID is taken to be the line number in the test split of the original dataset. See Linjordet & Balog 2020. 

For each row, the sampled original question is given in the column `OriginalQuestion`. The column `FinalQuestion` contains either the same string, or else the rewritten question which was found by crowd workers to be a more natural way of asking the question. 

## Contact

Should you have any questions, please contact `Trond Linjordet` at `trond.linjordet`[AT]uis.no (with [AT] replaced by @).

# Would You Ask it that Way? Measuring and Improving Question Naturalness for Knowledge Graph Question Answering

This repository provides resources developed within the following article:

> T. Linjordet, K. Balog. **Would You Ask it that Way? Measuring and Improving Question Naturalness for Knowledge Graph Question Answering.** Submitted for review. 2022. 

## Summary

*Knowledge graph question answering (KGQA) facilitates information access by leveraging structured data without requiring formal query language expertise from the user.  Instead, users can express their information needs by simply asking their questions in natural language (NL).  Datasets used to train KGQA models that would provide such a service are expensive to construct, both in terms of expert and crowdsourced labor.  However, the resulting datasets often fall short of representing genuinely natural and fluent language.  In the present work, we investigate ways to characterize and remedy these shortcomings.  We create a KGQA test collection by sampling questions from existing KGQA datasets and evaluating them with regards to five different aspects of naturalness.  Then, the questions are rewritten to improve their fluency.  Finally, the performance of existing KGQA models is compared on the original and rewritten versions of the NL questions.  We see that some KGQA systems fare worse when presented with more realistic formulations of NL questions.  The new test collection is provided to help evaluate KGQA systems in a more realistic setting.  The construction of this new test collection also sheds light on the challenges of constructing large-scale KGQA datasets with genuinely NL questions.*

## IGN-KGQA test collection

The main resource developed in our paper was the IGN-KGQA test collection, which includes 

This repository is structured as follows:

- `test_collection/`: bla bla.
- `test_collection/final_questions.csv`: This CSV file has four columns: `Dataset`, `QID`, `Original Question`, and `Final Question`. 
- ...`directory_ble/script_xyz.py`: ble ble Python script.

- ..`directory_bli/abc.json`: a JSON file containing bli bli.

### Detailed descriptions

In the file `test_collection/final_questions.csv`, the QID column is populated by the respective question ID from the original dataset (`Dataset`), except for those rows with original questions sampled from DBNQA*, where the QID is taken to be the line number in the test split of the original dataset. See Linjordet & Balog 2020. 

For each row, the sampled original question is given in the column `Original Question`. The column `Final Question` contains either the same string, or else the rewritten question which was found by crowd workers to be a more natural way of asking the question. 

## Citation

If you use the resources presented in this repository, please cite:

```
@inproceedings{Lastname:YYYY:ABC,
  author =    {...},
  title =     {...},
  booktitle = {Full proceedings title},
  series =    {...},
  year =      {...},
  pages =     {...--...},
  doi =       {XX.XXXX/XXXXXXX.XXXXXXX},
  publisher = {ACM or Springer, usually; choose your faith}
}
```

## Contact

Should you have any questions, please contact `<some guy>` at `<some_actual_email_localpart>`[AT]uis.no (with [AT] replaced by @).

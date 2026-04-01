# Anti-Immigrant Misinformation Dataset

A synthetic dataset of 100 social media posts for training and tuning text classifiers to detect anti-immigrant misinformation. Created for use with [Zentropi](https://zentropi.ai) and similar policy-configurable AI labeling tools.

## Background

This dataset was created as a classroom exercise for a graduate seminar on AI and migration management. It accompanies a guest lecture on content moderation, vulnerable populations, and open-source trust and safety infrastructure.

It is synthetic -- posts were generated to reflect realistic patterns of anti-immigrant misinformation observed on social media platforms, drawing on academic research and documented disinformation campaigns. It is not scraped from any platform.

## Files

| File | Description |
|------|-------------|
| `anti_immigrant_misinformation_zentropi.csv` | Zentropi-formatted dataset with `sample_id`, `content_text`, and `expected_label` columns |
| `anti_immigrant_misinformation_dataset.csv` | Full dataset with additional `category` and `notes` columns for reference |

## Labels

- `1` = misinformation (positive class)
- `0` = not misinformation (negative class)

The dataset is roughly balanced: 47 positive (misinformation) and 53 negative examples.

## Categories of Misinformation Covered

- Great replacement theory
- Fabricated crime and welfare statistics
- Disease myths
- Asylum system myths
- Conspiracy framing
- Dehumanizing language
- Coded and dog-whistle language
- False causal claims about resources and crime

## Deliberately Ambiguous Cases

A subset of examples are intentionally hard to classify. These include:

- True statements used selectively to imply a broader false pattern
- Policy opinions that are not misinformation but frequently precede it
- Grievance framing without explicit false claims
- Individual true incidents used to generalize about a population

These cases are designed to surface discussion about where the line is drawn and who draws it -- the central policy question that BYOP (bring your own policy) tools are designed to address.

## Limitations

- English only
- US and Western European context
- Does not capture AI-generated synthetic media, coordinated inauthentic behavior, or visual content
- Annotation reflects one policy perspective -- reasonable annotators will disagree on ambiguous cases
- Should not be used as a production training dataset without expert review and community input

## Related Resources

- [SemEval-2019 Task 5](https://github.com/cicl2018/semeval-2018-task-1) -- Multilingual detection of hate speech against immigrants and women on Twitter (real, academic dataset)
- [Zentropi](https://zentropi.ai) -- Policy-configurable AI labeling

## License

CC0 1.0 Universal -- public domain. Use freely, no attribution required.

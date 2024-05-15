# CAMERA<sup>3</sup> dataset

CAMERA<sup>3</sup> is an evaluation dataset for controllable text generation in the advertising domain in Japanese.
CAMERA<sup>3</sup>  includes 3,980 ad texts written by expert annotators, taking into account various aspects of ad appeals in LP (Landing Page).

- The annotated data is available at [`data/`](data/) directory in this repository in `json` and `jsonl`.
- The LP images are available [here](https://storage.googleapis.com/camera-cubed-public/camera-cubed-v1-lp-screenshot-sliced.tar.gz) (2.3GB).

## Dataset
- json: [`data/camera3-v1.json`](data/camera3-v1.json)
- jsonl: [`data/camera3-v1.jsonl`](data/camera3-v1.jsonl)
- lp_images: `camera3-v1-lp-screenshot-sliced/screen-1200-{lp_image_sliced}.png`

| Name | Description |
| --- | ---- |
| instance_id | unique id|
| lp_image_sliced | id associated with LP image |
| annotator_id | annotator id |
| kw | search keyword |
| lp_meta_description | meta description extracted from LP |
| lp_image_sliced_ocr_text | OCR results for LP imagge |
| ad_appeal_type | ad appeal type |
| ad_text | ad text |


- Example `json` entry:
    ```json
    {
        "instance_id":0,
        "lp_image_sliced":"screen-1200-100303_00.png",
        "annotator_id":5,
        "kw":"マイカー 共済",
        "lp_meta_description":"2022年最新の自動車保険のランキングを発表！...",
        "lp_image_sliced_ocr_text":"コのほけん!\n保険比較のコのほけん!>...",
        "ad_appeal_type":"価格",
        "ad_text":"ネットからの契約だと割引あり"
    }
    ```

## Citation
```
@inproceedings{inoue-etal-2024-camera3,
    title = "CAMERA³: An Evaluation Dataset for Controllable Ad Text Generation in Japanese",
    author = "Inoue, Go and
    Kato, Akihiko and
    Mita, Masato and
    Honda, Ukyo and
    Zhang, Peinan",
    booktitle = "Proceedings of the Fourteenth Language Resources and Evaluation Conference",
    month = may,
    year = "2024",
    address = "Turin, Italy",
    publisher = "European Language Resources Association"
}
```

## License
The dataset is licensed under [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-nc-sa/4.0/).

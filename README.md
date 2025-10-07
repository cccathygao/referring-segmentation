# referring-segmentation

## Data curation output
```
output
├── 12149
├── 15146
├── 63509
│...
│ 
└── result.json
```
Each folder (named with image id) contains the groundtruth mask image and generated noisy mask images.
Each entry in result.json represents either a groundtruth mask or a generated mask.
```
{
    "id": "63509", (image id)
    "problem": "back left guy", (referring expression)
    "image_path": "output/63509/mask.png", 
    "label": "wrong-instance", (category of noise)
    "iou": 0.0,
    "indices": [ 
      11
    ], (the indices of the SAM-generated masks used to generate the final mask image)
    "bbox": null (bbox used to generate the mask)
}
```

## grefcoco dataset
```
https://huggingface.co/datasets/qixiangbupt/grefcoco/viewer/default/train
```

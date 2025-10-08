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

An example entry:
```
id 982
problem bag being held up
answer <seg>(36.76, 233.51)(46.49, 252.97)(65.95, 300.54)(82.16, 311.35)(94.05, 313.51)(190.27, 263.78)(207.57, 244.32)(198.92, 215.14)(187.03, 188.11)(167.57, 175.14)(150.27, 175.14)(123.24, 181.62)(102.7, 183.78)(95.14, 181.62)(82.16, 192.43)(78.92, 204.32)(35.68, 232.43)</seg>
images [<PIL.JpegImagePlugin.JpegImageFile image mode=RGB size=640x480 at 0x7E7E60FD7B90>]
img_height 480
img_width 640
mask_images [<PIL.JpegImagePlugin.JpegImageFile image mode=RGB size=640x480 at 0x7E7E60FD4C20>]
segmentation_source ['ann_1186831_seg_0']
```

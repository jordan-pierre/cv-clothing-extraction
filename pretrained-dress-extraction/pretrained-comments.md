# Comments on using save_ckp_froze.h5

Note: Pretrained model is too large to store in free github.  Download from [link](https://drive.google.com/u/0/uc?id=1l7PUB8uAGRyqvZ0ti0ZACoI2CzJxOVoI&export=download).

## Benefits

- Off-the-shelf model easy to implement
- Reliably cuts out face and background compared to other pretrained models so far.
- Including skin in front of the dress *may* give future algorithms a more complete picture of the shirt/dress itself

## Drawbacks

- includes skin and some background surrounding clothes
  - Should ideally only include shirt/dress
- detects all shirts/dresses in image instead of most promenent
  - Could try foreground detection first using cv2.grabCut()
  - Could grab largest continuous section of processed image

## TODO if moving forward

- Convert to a py file that accepts sys args for file names
- Parameterize output file names
- Make a table/key that relates original image to processed image
- Write a shell script to process all images in a directory

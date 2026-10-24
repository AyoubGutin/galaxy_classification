# Notes supporting the learning + completion of the galaxy classification project for DAT6501.

## Dataset:

- https://zenodo.org/records/10844811 - Zenodo Link
- https://astronn.readthedocs.io/en/latest/galaxy10sdss.html - via astronn

Might want to make a function myself to ingest dataset in runtime rather than rely on astronn library, for learning purposes.

Dataset contains 21785 69x69 pixels representing coloured galaxy images (g, r, i band).

Separated into 10 classes, describing the galaxy. The images come from [Sloane Digital Sky Survey](https://www.sdss.org/), and labels come from [GalaxyZoo](https://www.zooniverse.org/projects/zookeeper/galaxy-zoo).

Classes are mutually exclusive, and is labelled based on volunteers to classify galaxy images, only contains images for which > 55% of the votes agree on the class.

55% was chosen as 50% was noisier (labels likely weong), and 55% was cleaner and similar accuracy to CIFAR-10. 60% was similar, but fewer images are kept.

Original images - 424x424, but cropped to 207x207 at the center, and downscaled 3 times via bilinear interpolation due to resource constraints.

Not a balanced dataset.

Cite Galaxy Zoo and Sloan Digital Sky Survey.

![alt text](image.png)

### Techincal Metadata

Size:
200MB

SHA256 for Verification:
`969A6B1CEFCC36E09FFFA86FEBD2F699A4AA19B837BA0427F01B0BC6DED458AF`

## Models

- Might do a normal NN learned recently - maybe work upwards to CNN and see how it differs
- Another method thats not a nn to see how it lacks

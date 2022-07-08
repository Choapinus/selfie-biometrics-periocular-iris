# Selfie Periocular Verification using an Efficient Super-Resolution Approach

Juan E. Tapia, Andres Valenzuela, Rodrigo Lara, Marta Gomez-Barrero and~Christoph Busch.

# Abstract
Selfie-based biometrics has great potential for a wide range of applications since, e.g.
periocular verification is contactless and is safe to use in pandemics such as COVID-19, when a major
portion of a face is covered by a facial mask. Despite its advantages, selfie-based biometrics presents
challenges since there is limited control over data acquisition at different distances. Therefore, Super-
Resolution (SR) has to be used to increase the quality of the eye images and to keep or improve the
recognition performance. We propose an Efficient Single Image Super-Resolution algorithm, which takes
into account a trade-off between the efficiency and the size of its filters. To that end, the method implements
a loss function based on the Sharpness metric used to evaluate iris images quality. Our method drastically
reduces the number of parameters compared to the state-of-the-art: from 2,170,142 to 28,654. Our best
results on remote verification systems with no redimensioning reached an EER of 8.89% for FaceNet,
12.14% for VGGFace, and 12.81% for ArcFace. Then, embedding vectors were extracted from SR images,
the FaceNet-based system yielded an EER of 8.92% for a resizing of x2, 8.85% for x3, and 9.32% for x4.

![Figure1_graphical_abstract](https://user-images.githubusercontent.com/45126159/173895776-e3033d81-ee3f-4e61-8bff-620f7f07a8c7.png)


# SR-ESISR Models

* [ESISR x2](https://github.com/Choapinus/selfie-biometrics-periocular-iris/tree/master/weights/ESIR/x2/models)
* [ESISR x3](https://github.com/Choapinus/selfie-biometrics-periocular-iris/tree/master/weights/ESIR/x3/models)
* [ESISR x4](https://github.com/Choapinus/selfie-biometrics-periocular-iris/tree/master/weights/ESIR/x4/models)

# Databases

Available netx days.

# Instructions
### How to create conda environment and use ESISR models

```
conda create --file env.yml
conda activate super-res

# do super-resolution x2
python sr.py --folder_images /path/to/input/images/ --output_dir /output/folder/dir --checkpoint_dir weights/ESIR/x2/models --scale=2 --layers=7 --filters=32 --min_filters=8 --filters_decay_gamma=1.2 --nin_filters=24 --nin_filters2=8 --reconstruct_layers=0 --self_ensemble=1 --pixel_shuffler_filters=1

# do super-resolution x3
python sr.py --folder_images /path/to/input/images/ --output_dir /output/folder/dir --checkpoint_dir weights/ESIR/x3/models --scale=3 --layers=7 --filters=32 --min_filters=8 --filters_decay_gamma=1.2 --nin_filters=24 --nin_filters2=8 --reconstruct_layers=0 --self_ensemble=1 --pixel_shuffler_filters=1

# do super-resolution x4
python sr.py --folder_images /path/to/input/images/ --output_dir /output/folder/dir --checkpoint_dir weights/ESIR/x4/models --scale=3 --layers=7 --filters=32 --min_filters=8 --filters_decay_gamma=1.2 --nin_filters=24 --nin_filters2=8 --reconstruct_layers=0 --self_ensemble=1 --pixel_shuffler_filters=1
```

More examples in [shell-codes folder](https://github.com/Choapinus/selfie-biometrics-periocular-iris/tree/master/NTNU_SR_shell_codes)

# Citation 
```
@ARTICLE{9800712,
  author={Tapia, Juan E. and Valenzuela, Andres and Lara, Rodrigo and Gomez-Barrero, Marta and Busch, Christoph},
  journal={IEEE Access}, 
  title={Selfie Periocular Verification using an Efficient Super-Resolution Approach}, 
  year={2022},
  volume={},
  number={},
  pages={1-1},
  doi={10.1109/ACCESS.2022.3184301}}
```

# Information
juan.tapia-farias@h-da.de
andres.valenzuela@tocbiometrics.com

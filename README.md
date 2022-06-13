# CondenseNeXt
CondenseNeXt is remarkably efficient by reducing trainable parameters and FLOPs required to train the network whilst maintaining a balance between the trained model size of less than 3.0 MB and accuracy trade-off resulting in an unprecedented computational efficiency.

### Citation

If you find my work useful, please consider citing my work:

```
@inproceedings{kalgaonkar2021condensenext,
  title={CondenseNeXt: An Ultra-Efficient Deep Neural Network for Embedded Systems},
  author={Kalgaonkar, Priyank and El-Sharkawy, Mohamed},
  booktitle={2021 IEEE 11th Annual Computing and Communication Workshop and Conference (CCWC)},
  pages={0524--0528},
  year={2021},
  organization={IEEE}
}
```

DOI: 10.1109/CCWC51732.2021.9375950

## Usage

### Dependencies

- [Python 3.8.10](https://www.python.org/downloads/)
- [PyTorch 1.9.0](http://pytorch.org)
- [Torchvision 0.10.0](https://pytorch.org/vision/stable/index.html)
- [CUDA Toolkit 10.2.89](https://developer.nvidia.com/cuda-toolkit)

### Train

To train CondenseNeXt on your target dataset of images, for example, CIFAR-10, use the following sample command:

```
python main.py --model condensenext -b 64 -j 12 cifar10 --stages 4-4-4 --growth 8-8-8 --gpu 0,1
```

Note: you can modify the stages, batch sizes, learning rate, growth and number of epochs to your desired accuracy and model size. This can be done either via aforementioned command line or by editing the corresponding hyperparameters in `main.py`.

## Contact
pkalgaon@purdue.edu

Any discussions or concerns are welcomed!
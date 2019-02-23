# Stop Sign Detection using Tensorflow

This project target is to train a model to detect Stop Sign - Traffic signs with GTSDB dataset + Google Image search Images and Tensorflow object detection API.

This was done in  macOS High Sierra 10.13.6

## Getting Started

These instructions will (hopefully) get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.


### Installing

* Follow the <a href='https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/installation.md'>Installation</a> instructions. Also find the Prerequisites.

* <a href='https://github.com/tzutalin/labelImg'>labelImg</a> was used to label Stopsign Images

## Running

### Protobuf Compilation

The Tensorflow Object Detection API uses Protobufs to configure model and
training parameters. Before the framework can be used, the Protobuf libraries
must be compiled. This should be done by running the following command from
the models/research/ directory:


```bash
# From models/research/
protoc object_detection/protos/*.proto --python_out=.
```

### Add Libraries to PYTHONPATH

When running locally, the models/research/ and slim directories
should be appended to PYTHONPATH. This can be done by running the following from
tensorflow/models/research/:


``` bash
# From tensorflow/models/research/
export PYTHONPATH=$PYTHONPATH:`pwd`:`pwd`/slim
```

Note: This command needs to run from every new terminal you start. If you wish
to avoid running this manually, you can add it as a new line to the end of your
~/.bashrc file, replacing \`pwd\` with the absolute path of
tensorflow/models/research on your system.


### From within ```models/research/object_detection``` run:

```bash
python train.py --logtostderr --train_dir=training/ --pipeline_config_path=training/faster_rcnn_inception_v2_pets.config
```
## Contribution(s)

1. [This repository](https://github.com/EdjeElectronics/TensorFlow-Object-Detection-API-Tutorial-Train-Multiple-Objects-Windows-10)
2. Also check [this video](https://www.youtube.com/watch?v=Rgpfk6eYxJA)

**Please let me know if you have any issues or if you have any suggestions for making this README better. If you thought a certain step was unclear, let me know and I'll try my best to edit the README and make any clarifications.**


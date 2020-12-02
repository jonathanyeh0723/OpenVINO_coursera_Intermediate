## Course 1 Quiz

---

#### 1. What is the acronym of the model format created by the model optimizer and used by the inference engine?

`     IR     `

Feedback: Correct! IR stands for Intermediate Representation, and contains not only a translated model but also an optimized model.

#### 2.	What is the difference between converting a TensorFlow* model and Caffe* model with model optimizer?

- [ ] TensorFlow models do not need to be converted with model optimizer
- [ ] TensorFlow models require additional flags to specify subgraphs to use
- [ ] TensorFlow models need to go through a special preprocessor script before model optimizer
- [x] `None of the above`

Feedback: Correct! By design, there is minimal change associated with going from one framework to another.

#### 3.	While using the inference engine, when do you need to specify the framework used in the original model?

- [ ] When loading the network to IENetwork
- [ ] When specifying the device to use for inference
- [ ] When starting the inference with ExecutableNetwork
- [x] `Never`

Feedback: Correct! Once converted to IR, inference engine does not care what the original format was.


#### 4.	Which model optimizer flag is used to specify the model to convert?

- [ ] --input
- [x] `--input_model`
- [ ] --model
- [ ] None of the above

Feedback: Correct! Be careful with --input, because that is a valid flag that controls the shape of the input.

#### 5.	What model optimizer flags do you need to set for enabling model-level optimizations?

- [ ] --enable
- [ ] --enable_optimizations
- [ ] --model_optimizations
- [x] `No flag is needed`

Feedback: Correct! Optimizations are enabled by default, so no need to specify anything.


#### 6. The following are input layer shapes of models we want to convert. Which shapes require us to specify the input_shape for model optimizer? Select all that apply.

- [ ] [1, 3, 127, 127]
- [x] `[-1, 3, 127, 127]`
- [ ] [10, 3, 127, 127]
- [ ] [1, 127, 127, 3]

Feedback: Correct! Shapes can't be undefined for inference.

#### 7. Model optimizer can remove layers from

- [ ] Only the start of the model
- [ ] Only the end of the model
- [x] `Both the start and the end of the model`
- [ ] Anywhere. Start, end or the middle of the model

Feedback: Correct! This can be useful if parts of the model was only there for training or processing certain datasets.

#### 8. Which devices can TensorFlow* offloading use? Select all that apply.

- [x] `CPU`
- [ ] GPU
- [ ] VPU
- [ ] FPGA

Feedback: Correct! If you need acceleration for these subgraphs, you will have to write custom layer extensions.

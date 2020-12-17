## Course 2 Quiz

---

#### 1. The course recommends applying optimization techniques as much as possible during validation so that you can get as accurate of a comparison as possible. True or False?

- [ ] True
- [x] `False`

Feedback: Correct! Optimization is a time consuming process, and can be impractical to do this for every system you want to try.

#### 2. Intel® VPUs are:

- [ ] general purpose processor for all workloads
- [ ] onchip accelerator for image processing
- [x] `specialized external accelerator for vision processing`
- [ ] external processors that are programmable with bitstreams

Feedback: Correct! VPU stands for Vision Processing Units, and are, as the name suggests, built for computer vision. The VPUs also tend to have a low power cost for the computer power.

#### 3. What device_name string should you use for heterogeneous mode with CPU and GPU? Please put CPU before GPU for this question.

`HETERO:CPU,GPU`

Feedback: Correct! In general, this string is the only thing you need to change in order to change the device to use for inference.

#### 4.	Where can you find the information on which device handles each layer?

- [x] `Dictionary returned by query_network method of IECore object`
- [ ] By looking at the “device” attribute for IELayer objects in layers attribute of IENetwork
- [ ] Dictionary from get_devices method of ExecutableNetwork
- [ ] From the “device” attribute found in IENetlayer objects from ExecutableNetwork

Feedback: Correct! The dictionary has the default mapping created by the developers.
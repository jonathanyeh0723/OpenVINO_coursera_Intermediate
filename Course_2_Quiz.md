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


#### 5.	What device_name should you use for multi-device mode with CPU and a single GPU, with GPU  prioritized over CPU?

`MULTI:GPU,CPU`

Feedback: Correct! The device that appears earlier in the list is preferentially used.

#### 6.	How many requests should you use for multi-device mode?

- [ ] Only one request
- [ ] As many requests as there are devices
- [ ] Number found by calling optimal_number_of_requests()
- [x] `Number found in the config parameter OPTIMAL_NUMBER_OF_REQUESTS for ExecutableNetwork`

Feedback: Correct! The optimal number of requests can be far larger than the number of devices, so always check this value for maximum performance.


#### 7. Suppose that you ran a benchmark to measure hybrid CPU and VPU inference. You found that preprocessing is taking longer than the inference. Which of the following is a good candidate for the next system to test? (Assume all else being equal)

- [ ] System with an additional VPU card
- [ ] System with a FPGA card
- [x] `System with a higher performance CPU`
- [ ] System with a higher power GPU

Feedback: Correct! CPUs typically handle preprocessing, so getting a higher performance CPU is the best bet in this situation.

#### 8. To enable performance counters:

- [ ] Set perf_count attribute of IECore to True
- [ ] Set perf_count attribute of ExecutableNetwork to True
- [x] `Set the PERF_COUNT config to YES in load_network method of IECore`
- [ ] Set the PERF_COUNT config to YES in the IECore constructor

Feedback: Correct! If you are using the heterogeneous mode, performance counter can be really helpful in determining what the best devices is for each layer.

#### 9. Which of the following can limit the lowest precision level? Select all that apply.

- [x] `The devices used in the inference`

Feedback: Correct! Some devices will support half precision computation, but others may only support float

- [ ] The precision level used in the original model

- [x] `Accuracy requirement for the application`

Feedback: Correct! Because lower precision means higher compute performance, it is usually a good idea to use the lowest precision that these constraints allow for

- [ ] The framework used in the original model

#### 10. What attribute of IENetLayer should you set to change the device that handles the layer?

`affinity`

Feedback: Correct! Remember to set this for every layer in the network. Use query_network to get the reference for default values for layers that aren’t of interest.

#### 11. Using asynchronous mode to run inference in parallel with preprocessing has no benefit if you are only using CPU. True or False?

- [ ] True
- [x] `False`

Feedback: Correct! Most CPUs will get some benefit, because most CPUs have multiple cores.

#### 12. Suppose you want to mask preprocessing and postprocessing time with inference time while using a single request slot. Starting at the wait function, what is the set of operations for handling starting i-th inference? Ignore edge cases.



#### 13. Which of the following methods returns the status code for the inference?

- [ ] get_status() method for the InferenceRequest object
- [x] `wait() method for InferenceRequest object`
- [ ] get_status() method for IECore object
- [ ] wait() method for IECore object

Feedback: Correct! The wait() method is per inference request. So if you have multiple requests, using timeout argument of wait() lets check every request.

#### 14. Which inference status codes should you handle in your code?

- [ ] only 0
- [ ] only -9
- [ ] only -9 and -11
- [ ] every status code

Feedback: Correct! 

#### 15. Imagine that you have an application that handles video streams from a variable number of devices. Which of the following implementations are generally NOT a good fit for this scenario. Select all that apply.

- [ ] xxx
- [ ] 
- [ ] 
- [ ] 

#### 16. Using Python* multithreading library is NOT recommended if a CPU is used for inference.  True or False? 

#### 17. The callback function is set by calling the set_completion_callback() method of:

- [ ] xxx
- [ ] 
- [ ] 
- [ ] 

#### 18. If you call the wait() method for an inference that has a callback, the callback is called before the wait method returns. True or False?

- [ ] xxx
- [ ] 
- [ ] 
- [ ] 

 
#### 19. Lab question: Which device performed the best (lowest time) in the benchmark workload for exercise-2?

- [ ] CPU
- [ ] GPU
- [x] FPGA (HETERO:CPU,FPGA) 

Feedback: Correct! For this particular workload, FPGA seems to perform the best.

#### 20. Lab Question: What is the average number of detected vehicles in the video?





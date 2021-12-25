# Asynchronous API:

When we have a very small file or data to upload then it makes sense to wait for the response,  
as we typically get the response in milli seconds or few seconds.  

But, when we have a huge data to upload or share across, waiting for the response does not make any sense,  
because the transfer of file/data over the network is anyway gonna to take significant time,  
Hence, in such cases, it's better to return a response/status which indicates that the processing is in progress,  
and the details could be found at a given location.  

**Approach-1:**  
Just return an Http Status Code as 202 (accepted), that means the request has been accepted and is in progress.  
as well as a `location`, that client can access to know the status of upload operation.  

![image](https://user-images.githubusercontent.com/26399543/147393473-0497e9fa-6601-4585-a67b-bce224336f72.png)

**Approach-2:**  

![image](https://user-images.githubusercontent.com/26399543/147393486-9dded746-bcfd-4710-ba7f-22227f1a8826.png)

**Usecase:**  
- The computation in API takes time.  

**Conclusion:**  
When ever an API is not able to give the response back to requester in a very small amount of time or in a very small latency,  
which are long running operations or which we know it would take time,  
in those cases, we use Asynchronous APIs,

this whole pattern is also known as : `Asynchronous Request/Response Pattern`  

**Reference:**  
1. https://www.youtube.com/watch?v=J4J-eHq_Oms


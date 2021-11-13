## Welcome to My GitHub Pages

### How to install pytorch and cuda in your local system

Please follow the below steps to install pytorch and cuda in your windows system. This is when you have GPU in your local system, else you can install pytorch without GPU also.
1. You have to install CUDA in your system.
   visit https://developer.nvidia.com/cuda-zone for installing CUDA and follow the steps provided there.
2. Once you have CUDA in your system, verify it from your installed CUDA location.
   For me, it was installed in the following path - "C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v10.2"
   As you can see I have CUDA version 10.2 installed in my local system
3. My suggestion would be to create a separate env for the pytorch. Make sure that Anaconda is installed in your system. 
   If not you can follow https://docs.anaconda.com/anaconda/install/windows/
   
   you can follow the steps to create a new environment.
   3.1 open a command prompt under admin privilege
   3.2 Execute:  conda create --name <your env name>
5. Now all you have to do is to visit https://pytorch.org/get-started/locally/ and follow the below table to select suitable prerequisites you need.
   ![pytorch1](https://user-images.githubusercontent.com/48651817/141610129-c7b86cf9-6572-493b-a2b1-429c8f88246c.png)
6. DO NOT FORGET TO TEST THE BELOW COMMANDS, this will give you confidence that pytorch with cuda is installed in your system for sure. 
    From the command line, type:
    ```
    python
    ```
    then enter the following code:
    ```
    import torch
    x = torch.rand(5, 3)
    print(x)
    ```
  
    Additionally you can execute below codes to make sure everything is all right:
    ```
    torch.cuda.is_available()
    torch.cuda.device_count()
    torch.cuda.get_device_name(torch.cuda.current_device())
    ```
    

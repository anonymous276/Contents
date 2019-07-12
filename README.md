# Simulation environments used for experiments in the papar "Reward-Driven U-Net Training for Collision Avoidance Drone"

Develope Environment:

OS: Ubuntu 18.04  
CPU: Intel i5-7600 3.5GHz
Memory: 16 GiB  
GPU: NVIDIA Geforce GTX 1060/ 3GB  
Unreal Engine version: 4.18  
Airsim version: 1.2.0  

## How to use

1. Install Airsim and Unreal Engine: https://github.com/microsoft/AirSim  
2. Run Unreal Editor.  
3. Go to 'New Project' and choose 'Basic Code' in 'C++'.  
4. Create the project(Rememer the path of your project).  
5. Open $your_path_to_the_project/your_project_name.uproject with textediting program.  
6. Add the following configuration and then save:
...  
"LoadingPhase": "Defalut",  
"AdditionalDependencies":[  
      "AirSim"  
      ]  
   }
   ],

   "Plugins": [  
        {  
              "Name": "AirSim",  
              "Enabled": true  
        }  
    ]  
   }  
 
   Final uproject file should look like 'sample.uproject' attached in this repository.  
 7. Copy Airsim plugin directory into your project.    
 Example command in Ubuntu : cp -r your_path_to_Airsim/Unreal/Plugins your_path_to_the_project/  
 8. Remove the 'Content' directory in your project  
 Example command in Ubuntu : rm -r your_path_to_the_project/Content  
 9. Download one of our simulation environments and extract it into your_path to_the_project 
 
     Environment 1 : https://drive.google.com/open?id=1qTx6P4VxBNrIUkctbkCI9arOyT1gthQc  
     Environment 2 : https://drive.google.com/open?id=1kTaOvz7hDMvBpg0XU2ZUr0ktVxacmprZ  
     Environment 3 : https://drive.google.com/open?id=12bGhzgSYC02n5RoMlo_3ynccj3CVQ9iL  
 
 10. Run UE4Editor and open your project. It will take some time to compile the environment.  
 
 11. From 'Windown Menu' select 'World Settings', and change 'Game Mode' to 'AirsimGameMode'.   
 
 12. Click 'Play' button and enjoy! Control commands can be found in 'PythonClient' provided by Airsim.




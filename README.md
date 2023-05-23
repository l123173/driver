# driver

## 速查  
PREC 是显示精度
HLM, LLM, DHLM, DLLM  软行程限位 （如果DHLM=DLLM=0,则禁用）  
VBAS  起始速度  Base Velocity (EGU/s)。  VELO,  最大速度， the full speed。  ACCL 加速时间  
increase linearly from the base speed, VBAS, to the full speed, VELO, in ACCL seconds  

VMAX,	Max Velocity (EGU/s)
VBAS <= VELO <= VMAX  

https://github.com/ISISComputingGroup/ibex_developers_manual/wiki/ASYN-Trace-Masks-%28Debugging-IOC%2C-ASYN%29  
## asynSetTraceIOMask 是干这个用的
Print commands and responses to screen  
The two commands you need are:  
asynSetTraceIOMask("L0", -1, 0x2)  
asynSetTraceMask("L0", -1, 0x9)  

Note: if the device's messages are longer than 80 characters, you should increase the buffer size by also running:

asynSetTraceIOTruncateSize("L0", -1, 1024)
Where 1024 is the maximum message length you expect - could be increased if your device requires it.

to turn off use

asynSetTraceMask("L0", -1, 0x1)  

##  这个还是有点东西的  
https://blog.csdn.net/yuyuyuliang00/article/details/129271803  



https://www.freesion.com/article/19691220463/  

https://epics.anl.gov/tech-talk/2021/msg01998.php  


## 这是各种VBLS  MERS 的  
https://epics.anl.gov/bcda/synApps/motor/motorRecord.html  

**multiply ioc  
https://wiki-ext.aps.anl.gov/epics/index.php/How_to_Make_Channel_Access_Reach_Multiple_Soft_IOCs_on_a_Linux_Host  

**Docker container  
https://epics.anl.gov/tech-talk/2019/msg01143.php   

**gui epics web  
https://epics.anl.gov/tech-talk/2014/msg01839.php  

**interface lab and epics  
https://epics.anl.gov/tech-talk/2014/msg01721.php  

**first stumle ioc  
https://epics.anl.gov/tech-talk/2014/msg01523.php  

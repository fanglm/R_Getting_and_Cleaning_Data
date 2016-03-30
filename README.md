# R_Getting_and_Cleaning_Data
swirl包安装失败

    在学习R_Getting_and_Cleaning_Data课程时，安装swirl的Getting_and_Cleaning_Data包失败，但是在R_Programming安装时，没有遇到类似问题。
    具体报错：
    Error in curl::curl_fetch_memory(url, handle = handle) : 
    Failure when receiving data from the peer
    或者
    Error in curl::curl_fetch_memory(url, handle = handle) : 
    Failed sending data to the peer
    
    第一判断：路径问题。改了半天，没有效果。
    解决方法：更改配置
                      library(RCurl)
                      library(httr) 
                      set_config( config( ssl_verifypeer = 0L ) )
    分析原因：ssl的peer参数影响通信。
    
总算成功了。

# drm_flv
文件访问流程 用户访问边缘节点的文件时,分为从头播放和拖拽播放两种情况。

####从头播放
    正常回源,并将 pcf 或 pcm 文件缓存至边缘节点,直接输出该文件即可,不需做额外处理。 

####拖拽播放
    拖拽播放的情况较复杂,由于加密后文件无法直接支持拖拽播放,所以必须先对加密文件进行解密,
    生成flv或mp4文件后,通过flv 和 mp4 的拖拽模块输出新的flv和mp4文件,并对该文件重新进行加密输出。


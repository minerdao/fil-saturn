# fil_saturn



官网：https://strn.network/

GitHub：https://github.com/filecoin-saturn

slack：https://app.slack.com/client/TEHTVS1L6/C03DH0BL02E/thread/C03DH0BL02E-1667303540.087069

浏览器：
        
        https://dashboard.strn.network   - 查看有关您的带宽贡献、FIL 收入等的历史数据。

        https://orchestrator.strn.pl/stats   - 查看每个土星节点的详细实时统计数据。
        
        https://ipinfo.io/tools/map/67efddb5-ab3b-40a5-924a-c8e45e08b64b    -全球节点分布地图

群友分享的性价比云：

# 大家 可以在这提交遇到的bug与改进方案（能提供代码更好了）


----------------------------------------------------------------------------
问题1：遇到了这个错误，容器都运行两天了，突然检测CPU不符合要求了，大佬们有遇到么
node-main Failed to register Error Not enough CPU cores. Required: 6, current: 2 +13s

解决方案：官方计算问题，已经处理！：https://orchestrator.strn.pl/requirements
 
------------------------------------------------------------
问题2：不通过后不会停止程序 docker重复重启  浪费流量
 
 解决方案：https://github.com/filecoin-saturn/L1-node/issues/81
 即将修复： https://github.com/filecoin-saturn/L1-node/commit/4694b96d963bf2557fd8a6d280fd8350f68327f6
 
---------------------------------------------------------------
 
问题3：节点挂了邮箱提醒希望大佬提供--可以参考https://github.com/lyjmry/cycles-
         做好后奖励10Fil 请留下打赏地址
 
 解决方案：https://github.com/minerdao/fil-saturn-monitor
 最新版本：https://github.com/qianhh/saturn-monitor
 Fil Address: f14nowmvdhutcr3zbbymmzqbkrtzy6r3gveqscp4q
 
-------------------------------------------------------------

问题4：如果硬件配置不够或必须资源被识别错误从而不能启动怎么办？  
> 此教程仅为帮助那些配置够，但被识别错误的节点，请勿胡乱使用。助力Web3。
1. 先按官方方式启动docker容器(这个时候容器可能在无限重启，不用管他)
2. 将容器内的代码目录复制出来，`docker cp -a 容器ID:/usr/src/app .`
3. 修改代码检查检查资源返回值部分，位置在`app/src/utils/system.js`  
比如内存给他改成10倍，就直接在返回值部分 * 10 ，注意格式<img width="1019" alt="image" src="https://user-images.githubusercontent.com/34204218/200993257-37f2d76f-fde4-46d0-9c57-a5f081d4545e.png">
比如网络这部分，它不是直接返回单个值，是返回一个结构体，所以我们在返回之前把结构体的字段给他放大<img width="1006" alt="image" src="https://user-images.githubusercontent.com/34204218/200993432-04d46757-bd7d-4403-9385-c686160c697f.png">
4. 将代码复制回原来的地方 `docker cp -a app 容器ID:/usr/src/`
5. 重启容器 `docker restart 容器ID`  

TRC20收款: `TGtSyY5v8C5vv14ewygESU3GeP1mLzeXap`  
FIL收款：`f1i64dht6jd6blfbxmt4xwss4wvf37kn7wjaxe3ui`
----------------------------------------------------------

问题5




----------------------------------------------------------

---
layout: page
title: loadworld
comments: true
permalink: /loadworld/
---

<script>
function getRequests() {
    var s1 = location.search.substring(1, location.search.length).split('&'),
        r = {}, s2, i;
    for (i = 0; i < s1.length; i += 1) {
        s2 = s1[i].split('=');
        r[decodeURIComponent(s2[0]).toLowerCase()] = decodeURIComponent(s2[1]);
    }
    return r;
};
function LoadWorld(){
    var QueryString = getRequests();
    if(QueryString["world"]){
        var url = "paracraft://cmd/loadworld " + QueryString["world"];
        document.getElementById('myframe').src = url;
        document.getElementById('url').innerHTML = url;
    }
}
$(LoadWorld);
</script>

## 加载世界 / Load World
<div id="url"></div>
<iframe id="myframe" width="0px" height="0px" style="display:none"></iframe>

---

### 需要安装Paracraft才能打开世界

> 请点击[这里](http://www.paracraft.cn/)下载并安装
    
在Paracraft中输入命令激活URL协议：`/registerurlprotocol`

---
        
### Paracraft software is required to open the world 

> please click [here](http://www.paracraft.cn/) to download and install.

In paracraft, activate url protocol with command: `/registerurlprotocol`

---

* **Usage:**  `loadworld?world=[world_filename.zip]`
* **Example:** `http://lixizhi.github.io/ParaCraft/loadworld?world=https://github.com/LiXizhi/HourOfCode/archive/master.zip`

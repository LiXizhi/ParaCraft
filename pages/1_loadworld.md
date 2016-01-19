---
layout: page
title: loadworld
comments: true
permalink: /loadworld/
icon: glyphicon-file
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

<h3>Load World with Paracraft</h3>
<div id="url"></div>
<p>
    <iframe id="myframe" width="100%" height="300px">
        loadworld.html?world=111.zip
    </iframe>
</p>
<div style="clear:both"></div>
<div style="float:left;min-width:380px;padding:5px;margin:5px;border :2px solid black;">
    <b>中文: 如果世界没有自动加载</b>
    <p>
        请点击<a href="http://www.paracraft.cn/">这里</a>下载并安装paracraft客户端.
    </p>
    <b>手工激活paracraft网络协议</b>
    <p>
        在paracraft中输入命令: <b>/registerurlprotocol</b>
    </p>
</div>
<div style="float:left;min-width:380px;padding:5px;margin:5px;border :2px solid black;">
    <b>English: If world does not load automatically</b>
    <p>
        please click <a href="http://www.paracraft.cn/">here</a> to download and install the software.
    </p>
    <b>manually activate paracraft network protocol </b>
    <p>
        In paracraft, enter command: <b>/registerurlprotocol</b>
    </p>
</div>
<div style="clear:both"></div>

> **Usage:**  `loadworld/?world=[world_filename.zip]`

> **Example:** `{{page.url}}?world=https://github.com/LiXizhi/HourOfCode/archive/master.zip`


基于快递100分析的接口
官方没有提供自动判断快递公司的接口,这就得自己分析了
欢迎补充~
##根据单号判断快递公司`get`

请求网址:http://www.kuaidi100.com/autonumber/autoComNum?text=[快递单号]

请求参数:`text`

返回数据格式:`json`

    {"comCode":"","num":"快递单号","auto":[{"comCode":"快递公司","id":"","noCount":4211,"noPre":"786187","startTime":""}]}
    
暂时可以确定意义的参数:




##获取快递包裹物流信息`get`
请求网址:http://www.kuaidi100.com/query?type=[快递公司名]&postid=快递单号
请求参数:`type`,`postid`
返回数据格式:`json`

    {"nu":"786187979245",
    "com":"shunfeng",
    "updatetime":"2016-07-28 07:40:53",
    "signname":"",
    "condition":"00",
    "status":"200",
    "signedtime":"",
    "data":[{"time":"2016-07-28 02:09:46",
    "location":"",
    "context":"快件离开【齐齐哈尔鹤城集散中心】,正发往下一站",
    "ftime":"2016-07-28 02:09:46"},
    {"time":"2016-07-28 02:08:36","location":"","context":"快件到达 【齐齐哈尔鹤城集散中心】","ftime":"2016-07-28 02:08:36"},{"time":"2016-07-27 18:35:02","location":"","context":"快件离开【哈尔滨哈安集散中心】,正发往 【齐齐哈尔鹤城集散中心】","ftime":"2016-07-27 18:35:02"}],
    "state":"0",
    "departure":"深圳市",
    "addressee":"",
    "destination":"呼伦贝尔市",
    "message":"ok",
    "ischeck":"0",
    "pickuptime":""}

快递公司代号说明:查看快递100官方文档:[https://www.kuaidi100.com/openapi/api_post.shtml#d07](https://www.kuaidi100.com/openapi/api_post.shtml#d07)







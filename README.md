### 1.Selenium+Chrome/PhantomJS爬取淘宝美食

* 搜索关键字
利⽤Selenium驱动浏览器搜索关键字，得到查询后的商品列表。
* 分析⻚码并翻⻚
得到商品⻚码数，模拟翻⻚，得到后续⻚⾯的商品列表。
* 分析提取商品内容
利⽤PyQuery分析源码，解析得到商品列表。
* 存储⾄MongoDB
 将商品列表信息存储到数据库MongoDB。
 
 ### 2.函数介绍
 def search(): 获取网页响应，并查找输入框，输入关键词进行搜索
 def next_page(page_number): 查找翻页的css，并进行翻页和确认
 def get_products(): 获得每页宝贝的详细内容
 def save_to_mongo(result): 保存到mongo数据库
 def main(): 主函数

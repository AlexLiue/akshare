# Akshare 引入 Proxy 代理解决  IP 被限问题
## 安装部署 
```
# 安装python安装工具
pip install setuptools
pip install 
python setup.py check
python setup.py sdist bdist_wheel
twine upload dist/*
twine upload --repository testpypi dist/*
twine upload --repository pypi dist/*

pip install akshare-proxy==1.17.87.dev0

pip install --upgrade --index-url https://test.pypi.org/simple/ akshare-proxy==1.17.87.dev2

## 本地调试安装
pip install .
```
## 验证安装
```python
import akshare as ak
print(ak.__version__)
```
## 代理配置
```python
from akshare.utils.context import AkshareConfig
import akshare as ak

""" 创建代理字典 """
proxies = {
    "http": "http://xxx.con:xxx",
    "https": "https://xxx.con:xxx"
}
""" 创建代理字典 """
AkshareConfig.set_proxies(proxies)

stock_sse_summary_df = ak.stock_sse_summary()
print(stock_sse_summary_df)

```

## IP 代理搭建
### 免费代理
[https://github.com/AlexLiue/proxy_pool](https://github.com/AlexLiue/proxy_pool)

## 收费代理
[https://cheapproxy.net/](https://cheapproxy.net/)


## 代码更新管理脚本备注
```
# 克隆项目
git clone https://github.com/AlexLiue/akshare.git
# 查看分支
git remote -v

# 添加上游仓库地址
git remote add upstream https://github.com/akfamily/akshare.git

# 合并上游更新到本地项目 （先本地创建合并分支，然后合并）
git checkout develop
git fetch upstream
git merge upstream/main

# 提交
git add .
git commit -m '20250401'

# 合并更新到主分支
git checkout main
git pull origin main
git merge develop

<<<<<<< HEAD
# 提交主分支
git add .
git commit -m '20250401'
git tag v0.0.1
git push  origin master
```
=======
Thanks for the data provided by [99期货网站](http://www.99qh.com/);

Thanks for the data provided by [中国外汇交易中心暨全国银行间同业拆借中心网站](http://www.chinamoney.com.cn/chinese/);

Thanks for the data provided by [和讯财经网站](http://www.hexun.com/);

Thanks for the data provided by [DACHENG-XIU 网站](https://dachxiu.chicagobooth.edu/);

Thanks for the data provided by [上海证券交易所网站](http://www.sse.com.cn/assortment/options/price/);

Thanks for the data provided by [深证证券交易所网站](http://www.szse.cn/);

Thanks for the data provided by [北京证券交易所网站](http://www.bse.cn/);

Thanks for the data provided by [中国金融期货交易所网站](http://www.cffex.com.cn/);

Thanks for the data provided by [上海期货交易所网站](http://www.shfe.com.cn/);

Thanks for the data provided by [大连商品交易所网站](http://www.dce.com.cn/);

Thanks for the data provided by [郑州商品交易所网站](http://www.czce.com.cn/);

Thanks for the data provided by [上海国际能源交易中心网站](http://www.ine.com.cn/);

Thanks for the data provided by [Timeanddate 网站](https://www.timeanddate.com/);

Thanks for the data provided by [河北省空气质量预报信息发布系统网站](http://110.249.223.67/publish/);

Thanks for the data provided by [Economic Policy Uncertainty 网站](http://www.nanhua.net/nhzc/varietytrend.html);

Thanks for the data provided by [申万指数网站](http://www.swsindex.com/idx0120.aspx?columnid=8832);

Thanks for the data provided by [真气网网站](https://www.zq12369.com/);

Thanks for the data provided by [财富网站](http://www.fortunechina.com/);

Thanks for the data provided by [中国证券投资基金业协会网站](http://gs.amac.org.cn/);

Thanks for the data provided by [Expatistan 网站](https://www.expatistan.com/cost-of-living);

Thanks for the data provided by [北京市碳排放权电子交易平台网站](https://www.bjets.com.cn/article/jyxx/);

Thanks for the data provided by [国家金融与发展实验室网站](http://www.nifd.cn/);

Thanks for the data provided by [义乌小商品指数网站](http://www.ywindex.com/Home/Product/index/);

Thanks for the data provided by [百度迁徙网站](https://qianxi.baidu.com/?from=shoubai#city=0);

Thanks for the data provided by [思知网站](https://www.ownthink.com/);

Thanks for the data provided by [Currencyscoop 网站](https://currencyscoop.com/);

Thanks for the data provided by [新加坡交易所网站](https://www.sgx.com/zh-hans/research-education/derivatives);
>>>>>>> upstream/main

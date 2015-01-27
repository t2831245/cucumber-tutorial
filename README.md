cucumber
=
###安裝
###介紹
###除錯

##安裝
在STS的**[Package Explorer]** new 一個 **[Maven Project]**  
![](https://raw.githubusercontent.com/t2831245/cucumber-tutorial/master/img/001.png)

勾選[Create a simple project]  
![](https://raw.githubusercontent.com/t2831245/cucumber-tutorial/master/img/002.png)

在**[Artifact]**部分輸入[Group Id]及[Artifact Id]   
![](https://raw.githubusercontent.com/t2831245/cucumber-tutorial/master/img/003.png)

在**[pom.xml]**檔案新增dependencies內容  
![](https://raw.githubusercontent.com/t2831245/cucumber-tutorial/master/img/004.png)

##介紹
在**[src/test/java]**底下新增一個[package]，並放入下例圖中的3個檔案  
[.feature]是動作腳本，目的在於記錄使用者想要達到怎麼樣的功能 
![](https://raw.githubusercontent.com/t2831245/cucumber-tutorial/master/img/005.png)

第二個程式則要實作剛剛寫好的腳本動作  
在 @Give @When @Then 裡的內容必須和[.feature]寫的一樣才能抓到
![](https://raw.githubusercontent.com/t2831245/cucumber-tutorial/master/img/006.png)

在 @Give @When @Then 的內容可以使用規則表示法，來使腳本會有更靈活的判斷  
像例圖中的 @Give 就是使用規賊表示法表示，如果有要輸入參數的需求，必須要像 @Give 的寫法，括號裡面是參數，然後參數才會進到method裡
![](https://raw.githubusercontent.com/t2831245/cucumber-tutorial/master/img/011.png)  


第三個程式是拿來啟動用的  
![](https://raw.githubusercontent.com/t2831245/cucumber-tutorial/master/img/007.png)  

啟動測試  
![](https://raw.githubusercontent.com/t2831245/cucumber-tutorial/master/img/012.png)  
![](https://raw.githubusercontent.com/t2831245/cucumber-tutorial/master/img/013.png)   
成功的話，圖示會有綠色的勾  
![](https://raw.githubusercontent.com/t2831245/cucumber-tutorial/master/img/014.png)  


##除錯
如果發生下圖問題  
![](https://raw.githubusercontent.com/t2831245/cucumber-tutorial/master/img/error.png)  
解決辦法就是右鍵選取專案，並選擇[Properties]，然後選擇[Java Build Path]來新增[JUnit4]  
![](https://raw.githubusercontent.com/t2831245/cucumber-tutorial/master/img/008.png)  
![](https://raw.githubusercontent.com/t2831245/cucumber-tutorial/master/img/009.png)  
![](https://raw.githubusercontent.com/t2831245/cucumber-tutorial/master/img/010.png)  

下圖表示 method 沒有對應到.feature 的動作，  
![](https://raw.githubusercontent.com/t2831245/cucumber-tutorial/master/img/015.png)  
下圖圖示代表測試沒有成功執行  
![](https://raw.githubusercontent.com/t2831245/cucumber-tutorial/master/img/016.png)  

如果沒有使用規則表示法帶參數的話，會發生以下問題  
![](https://raw.githubusercontent.com/t2831245/cucumber-tutorial/master/img/017.png)  
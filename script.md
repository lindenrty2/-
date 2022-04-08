## 自动看视频
```
this.setInterval(() => {console.log("checking"); var a = $(".layui-layer-btn0");if(a.length > 0){ a.click()} var b = $(".popup_operate .whaty-button");if(b.length > 0){ document.querySelectorAll(".checkbox-inline").forEach(x => { var s = angular.element(x).scope(); s.optionObj.isChecked = s.optionObj.isAnswer; if(s.optionObj.isChecked) { var event1 = document.createEvent('HTMLEvents');event1.initEvent("click", true, true);event1.eventType = 'message';x.dispatchEvent(event1);}} ); b.click(); }  var c = $(".popup_operate .btn whaty-button");if(c.length > 0){ c.click();$(".vjs-tech")[0].play();}  },5000)
```


## 自动填选择题作业答案
### 勾选题
```
document.querySelectorAll(".question-option-item input[type='checkbox']").forEach(x => { var s = angular.element(x).scope(); x.checked = s.topicItemObj.isAnswer == "true"; var event1 = document.createEvent('HTMLEvents');event1.initEvent("click", true, true);event1.eventType = 'message';x.dispatchEvent(event1); }   )
```

### 单选题
```
document.querySelectorAll(".topic-item input[type='radio']").forEach(x => { var s = angular.element(x).scope(); x.checked = s.topicItemObj.isAnswer == "true"; var event1 = document.createEvent('HTMLEvents');event1.initEvent("click", true, true);event1.eventType = 'message';x.dispatchEvent(event1); }   )
```

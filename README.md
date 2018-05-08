# wx-calender
小程序日历，已经封装成组件，显示今天起的统一价格日历，已组件形式导入进去

## 效果图
!(日历图片)[https://github.com/orangekingliness/image-folder/wx-canlendar/wx-calendar.png]

## 使用方法
json中引入
```
"usingComponents": {
      "unifyCalendar":"路径/unifyCalendar/dataselect"
    }
```

wxml内
```
<unifyCalendar 
  id="unifyCalendar" 
  bind:okFunc="_okFunc">
</unifyCalendar>
```
js中
```
this.calender = this.selectComponent("#unifyCalendar");

this.calender.calenderInit();

_okFunc: function () {
    var obj = this.calender.getSelect()
    this.setData({
      time: obj.time
    })
    console.log(obj)
    this.calender.hideCalender()

  },
  showCalender: function () {
    console.log("A")
    this.calender.showCalender();
    console.log(this);
  },

```



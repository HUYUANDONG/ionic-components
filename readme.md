
插件fork fromhttps://github.com/woodstream/ionic-components 在此基础上进行修改的版本
1.修复了在手机端点击右侧字母左侧滚动不平滑;
2.修复左侧滚动右侧不随动

>代码为index-list（原来代码基本没动，只改动锚点滚动逻辑）和index-group（重新实现）共两个组件，所以会发现两种不同的代码风格。
# 示范使用
然后就可以用了，示范用法如下：
```
<index-list radio-group [(ngModel)]="vm.selectedValue">
    <index-group *ngFor="let group of groups" index="{{group.key}}">
      <ion-item *ngFor="let item of group.items">
        <ion-label>{{item.name || item.title}}</ion-label>
        <ion-radio value="{{item.value}}"></ion-radio>
      </ion-item>
    </index-group>
  </index-list>
```

# 总结
因为只花了一点时间来改，可能有bug，若有，给我留言。另外，index-list其实应该可以再精简的，只是我目前懒得花时间去改了，留给你们谁有兴趣再改吧。

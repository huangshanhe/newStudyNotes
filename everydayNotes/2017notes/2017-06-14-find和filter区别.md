
# .find()和.filter()方法的区别 #
    
    这是jQuery里常用的2个方法。
    他们2者功能是完全不同的，而初学者往往会被误导。

    现在有一个页面，里面HTML代码为;
    <div >
    <p class="rain">测试1</p>
    </div>

    <div class="rain">
         <p>测试2</p>
    </div>


    ①如果我们使用find()方法：
    var result = $("div").find(".rain");
    alert(result.html() ) ;
    结果:测试1



    ②如果使用filter()方法：
    var result = $("div").filter(".rain");
    alert(result.html() );
    结果:<p>测试2</p>


    find()会在div元素内寻找class为rain 的元素，是对它的子集操作
    filter()则是筛选div的class为rain的元素，是对它自身集合元素筛选

    另外find()其实还可以用选择器表示:
    var $select = $("div .rain");
    明白他们的区别了吗？

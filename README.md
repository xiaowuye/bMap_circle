此功能可以在地图上画出多个圆形

如果要添加点击事件可以在绘画完之后添加一下事件

//给标注点添加点击事件
(function() {
    var thePoint = points[i];
    marker.addEventListener("click", function() {
        // showInfo(this, thePoint);
    });
})();
//显示信息窗口，显示标注点的信息
function showInfo(thisMaker, point) {
    var sContent = '';
    if (point.type == "故障") {
        sContent += '<ul class="info_ul info_ui_img">';
        sContent += '   <li class="info_lierr">文字</li>';
        sContent += '</ul>';
    }

    // 创建信息窗口对象
    var infoWindow = new BMap.InfoWindow(sContent);

    //图片加载完毕重绘infowindow
    thisMaker.openInfoWindow(infoWindow);
};

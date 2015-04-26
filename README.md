# MedicalApplicition
湘雅医疗数据 （基于android平台医疗数据采集系统）
##项目整体介绍
  * 旨在为医生打造医疗数据信息采集平台<br>
  * 实现随时随地上传文字，图片，视频，音频等病人记录信息<br>
  * 主要功能架构图<br>
<div class='raw'>
 <img src='https://github.com/sjaiwl/image_folder/blob/master/MedicalApplication/app.png' height="300px" width="500px" style='border: #f1f1f1 solid 1px'/>
</div>

##项目主体采用fragmentactivity实现fragment切换
  * 需要了解fragment工作机制和生命周期<br>
```xml
mFragments = new Fragment[3];
fragmentManager = getSupportFragmentManager();
mFragments[0] = fragmentManager.findFragmentById(R.id.fragment_main);
mFragments[1] = fragmentManager.findFragmentById(R.id.fragment_file);
mFragments[2] = fragmentManager.findFragmentById(R.id.fragment_mine);
fragmentTransaction = fragmentManager.beginTransaction().hide(mFragments[0]).hide(mFragments[1]).hide(mFragments[2]);
fragmentTransaction.show(mFragments[0]).commit();
```
  * 实现效果图<br>
<div class='row'>
        <img src='https://github.com/sjaiwl/image_folder/blob/master/MedicalApplication/mainPage.png' width="250px" style='border: #f1f1f1 solid 1px'/>
        <img src='https://github.com/sjaiwl/image_folder/blob/master/MedicalApplication/filePage.png' width="250px" style='border: #f1f1f1 solid 1px'/>
        <img src='https://github.com/sjaiwl/image_folder/blob/master/MedicalApplication/minePage.png' width="250px" style='border: #f1f1f1 solid 1px'/>
    </div>

###主体中的关键技术
```
<dependency>
    <groupId>in.srain.cube</groupId>
    <artifactId>ultra-ptr</artifactId>
    <type>aar</type>
    <!-- or apklib format, if you want -->
    <!-- <type>apklib</type> -->
    <version>1.0.8.4-SNAPSHOT</version>
</dependency>
```

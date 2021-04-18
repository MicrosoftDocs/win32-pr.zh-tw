---
title: 透過大小定義和調整原則自訂功能區
description: 功能區命令列中裝載的控制項受限於 Windows 功能區架構所強制執行的版面配置規則，並根據預設行為和版面配置範本的組合 (在功能區標記中宣告的架構定義和自訂) 。 這些規則會定義功能區架構的調適型配置行為，此行為會影響命令列中的控制項在執行時間如何適應各種功能區大小。
ms.assetid: b5869394-3fa9-4817-add9-54487434fc4f
keywords:
- Windows 功能區，自訂
- 功能區，自訂
- Windows 功能區，SizeDefinition 範本
- 功能區、SizeDefinition 範本
- Windows 功能區，自訂範本
- 功能區、自訂範本
- 自訂 Windows 功能區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b12618f88576cddeff119534215e501216193c3
ms.sourcegitcommit: 2387bc0339a1764564c1509e72ed5f2e8ae60b36
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/30/2020
ms.locfileid: "104558315"
---
# <a name="customizing-a-ribbon-through-size-definitions-and-scaling-policies"></a>透過大小定義和調整原則自訂功能區

功能區命令列中裝載的控制項受限於 Windows 功能區架構所強制執行的版面配置規則，並根據預設行為和版面配置範本的組合 (在功能區標記中宣告的架構定義和自訂) 。 這些規則會定義功能區架構的調適型配置行為，此行為會影響命令列中的控制項在執行時間如何適應各種功能區大小。

-   [簡介](#introduction)
    -   [功能區 SizeDefinition 範本](#customizing-a-ribbon-through-size-definitions-and-scaling-policies)
    -   [自訂範本](#custom-templates)
-   [相關主題](#related-topics)

## <a name="introduction"></a>簡介

自訂版面配置是由功能區架構所定義，因此功能區 UI 中的所有控制項都能根據執行時間的功能區大小變更，動態調整其組織、大小、格式和相對比例。

架構會透過一組專門用來指定和自訂各種版面配置行為的標記元素來公開自訂版面配置功能。 範本的集合（稱為 [**SizeDefinitions**](windowsribbon-element-sizedefinition.md)）是由架構所定義，每個範本都支援各種控制項和版面配置案例。 但是，如果預先定義的範本不提供應用程式所需的 UI 體驗或版面配置，架構也支援自訂範本。

若要在特定功能區大小以慣用的版面配置顯示控制項，預先定義的範本和自訂範本會與 [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) 元素一起使用。 這個元素包含大小喜好設定的資訊清單，在轉譯功能區時，架構會使用這些喜好設定做為指南。

> [!Note]  
> 功能區架構會根據一組內建的啟發學習法提供預設的版面配置行為，並在執行時間呈現控制項，而不需要預先定義的 [**SizeDefinition**](windowsribbon-element-sizedefinition.md) 範本。 不過，這項功能僅適用于原型設計用途。

 

### <a name="ribbon-sizedefinition-templates"></a>功能區 SizeDefinition 範本

功能區架構會提供一組完整的 [**SizeDefinition**](windowsribbon-element-sizedefinition.md) 範本，這些範本會指定功能區控制項 [群組](windowsribbon-controls-group.md) 的大小和版面配置行為。 這些範本涵蓋了在功能區應用程式中組織控制項的最常見案例。

為了在功能區應用程式之間強制執行一致的使用者體驗，每個 [**SizeDefinition**](windowsribbon-element-sizedefinition.md) 範本會對其支援的控制項或控制項系列施加限制。

例如，按鈕系列的控制項包括：

-   [按鈕](windowsribbon-controls-button.md)
-   [切換按鈕](windowsribbon-controls-togglebutton.md)
-   [下拉式按鈕](windowsribbon-controls-dropdownbutton.md)
-   [分割按鈕](windowsribbon-controls-splitbutton.md)
-   [下拉式圖庫](windowsribbon-controls-dropdowngallery.md)
-   [分割按鈕資源庫](windowsribbon-controls-splitbuttongallery.md)
-   [下拉式色彩選擇器](windowsribbon-controls-dropdowncolorpicker.md)

控制項的輸入系列包括：

-   [下拉式方塊](windowsribbon-controls-combobox.md)
-   [Spinner](windowsribbon-controls-spinner.md)

[核取方塊](windowsribbon-controls-checkbox.md) 和 [功能區圖庫](windowsribbon-controls-inribbongallery.md) 都不屬於按鈕系列或輸入系列。 這兩個控制項只能用在 [**SizeDefinition**](windowsribbon-element-sizedefinition.md) 範本中明確指出的位置。

以下是 [**SizeDefinition**](windowsribbon-element-sizedefinition.md) 範本的清單，其中包含每個範本所允許的版面配置和控制項的描述。

> [!IMPORTANT]
> 如果在標記中宣告的控制項無法完全對應至關聯範本中定義的控制項類型、順序和數量，則[標記編譯器](windowsribbon-intentcl.md)會記錄[驗證錯誤](windowsribbon-compilationerrors.md)，並終止編譯。

 



OneButton

一個按鈕系列控制項。<br/> 僅支援大型群組大小。<br/>

![onebutton sizedefinition 範本的圖片。](images/overviews/sizedefinition-onebutton.png)

TwoButtons

兩個按鈕系列控制項。<br/> 僅支援大型和中型群組的大小。<br/>

![twobuttons 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-twobuttons-large.png)

![twobuttons medium sizedefinition 範本的圖片。](images/overviews/sizedefinition-twobuttons-medium.png)

ThreeButtons

三個按鈕系列控制項。<br/> 僅支援大型和中型群組的大小。<br/>

![threebuttons 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-threebuttons-large.png)

![threebuttons medium sizedefinition 範本的圖片。](images/overviews/sizedefinition-threebuttons-medium.png)

ThreeButtons-OneBigAndTwoSmall

三個按鈕系列控制項。<br/> 第一個按鈕會以三種大小醒目顯示。<br/>

![threebuttons-onebigandtwosmall 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-large.png)

![threebuttons-onebigandtwosmall medium sizedefinition 範本的圖片。](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-medium.png)

![threebuttons-onebigandtwosmall small sizedefinition 範本的圖片。](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-small.png)

ThreeButtonsAndOneCheckBox

三個按鈕系列控制項，伴隨著單一核取方塊控制項。<br/> 僅支援大型和中型群組的大小。<br/>

![threebuttonsandonecheckbox 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-threebuttonsandonecheckbox-large.png)

![threebuttonsandonecheckbox medium sizedefinition 範本的圖片。](images/overviews/sizedefinition-threebuttonsandonecheckbox-medium.png)

FourButtons

四個按鈕系列控制項。<br/>

![fourbuttons 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-fourbuttons-large.png)

![fourbuttons medium sizedefinition 範本的圖片。](images/overviews/sizedefinition-fourbuttons-medium.png)

![fourbuttons small sizedefinition 範本的圖片。](images/overviews/sizedefinition-fourbuttons-small.png)

FiveButtons

五個按鈕系列控制項。<br/>

![fivebuttons 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-fivebuttons-large.png)

![fivebuttons medium sizedefinition 範本的圖片。](images/overviews/sizedefinition-fivebuttons-medium.png)

![fivebuttons small sizedefinition 範本的圖片。](images/overviews/sizedefinition-fivebuttons-small.png)

FiveOrSixButtons

五個按鈕系列控制項和選擇性的第六個按鈕。<br/>

![fiveorsixbuttons 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-fiveorsixbuttons-large.png)

![fiveorsixbuttons medium sizedefinition 範本的圖片。](images/overviews/sizedefinition-fiveorsixbuttons-medium.png)

![fiveorsixbuttons small sizedefinition 範本的圖片。](images/overviews/sizedefinition-fiveorsixbuttons-small.png)

SixButtons

六個按鈕系列控制項。<br/>

![sixbuttons 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-sixbuttons-large.png)

![sixbuttons medium sizedefinition 範本的圖片。](images/overviews/sizedefinition-sixbuttons-medium.png)

![sixbuttons small sizedefinition 範本的圖片。](images/overviews/sizedefinition-sixbuttons-small.png)

SixButtons-TwoColumns

六個按鈕系列控制項 (替代的簡報) 。<br/>

![sixbuttons-twocolumns 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-sixbuttons-twocolumns-large.png)

![sixbuttons-twocolumns 中型 sizedefinition 範本。](images/overviews/sizedefinition-sixbuttons-twocolumns-medium.png)

![sixbuttons-twocolumns small sizedefinition 範本的圖片。](images/overviews/sizedefinition-sixbuttons-twocolumns-small.png)

SevenButtons

七個按鈕系列控制項。<br/>

![sevenbuttons 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-sevenbuttons-large.png)

![sevenbuttons mediumsizedefinition 範本的圖片。](images/overviews/sizedefinition-sevenbuttons-medium.png)

![sevenbuttons small sizedefinition 範本的圖片。](images/overviews/sizedefinition-sevenbuttons-small.png)

EightButtons

八個按鈕系列控制項。<br/>

![eightbuttons-lastthreesmall 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-eightbuttons-lastthreesmall-large.png)

![eightbuttons-lastthreesmall medium sizedefinition 範本的圖片。](images/overviews/sizedefinition-eightbuttons-lastthreesmall-medium.png)

![eightbuttons-lastthreesmall small sizedefinition 範本的圖片。](images/overviews/sizedefinition-eightbuttons-lastthreesmall-small.png)

EightButtons-LastThreeSmall

八個按鈕系列控制項 (替代的簡報) 。<br/>

> [!Note]  
> 所有以此範本宣告的控制項元素都必須包含在兩個 [**ControlGroup**](windowsribbon-element-controlgroup.md) 元素中：一個用於前五個元素，另一個用於最後三個元素。

<br/> 下列範例示範此範本所需的標記。<br/>

```
<Group CommandName="cmdSizeDefinitionsGroup" 
       SizeDefinition="EightButtons-LastThreeSmall">
  <ControlGroup>
    <Button CommandName="cmdSDButton1" />
    <Button CommandName="cmdSDButton2" />
    <Button CommandName="cmdSDButton3" />
    <Button CommandName="cmdSDButton4" />
    <Button CommandName="cmdSDButton5" />
  </ControlGroup>
  <ControlGroup>
    <Button CommandName="cmdSDButton6" />
    <Button CommandName="cmdSDButton7" />
    <Button CommandName="cmdSDButton8" />
  </ControlGroup>
</Group>
```



![eightbuttons 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-eightbuttons-large.png)

![eightbuttons medium sizedefinition 範本的圖片。](images/overviews/sizedefinition-eightbuttons-medium.png)

![eightbuttons small sizedefinition 範本的圖片。](images/overviews/sizedefinition-eightbuttons-small.png)

NineButtons

九個按鈕系列控制項。

![ninebuttons 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-ninebuttons-large.png)

![ninebuttons medium sizedefinition 範本的圖片。](images/overviews/sizedefinition-ninebuttons-medium.png)

![ninebuttons small sizedefinition 範本的圖片。](images/overviews/sizedefinition-ninebuttons-small.png)

TenButtons

十個按鈕系列控制項。

![tenbuttons 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-tenbuttons-large.png)

![tenbuttons medium sizedefinition 範本的圖片。](images/overviews/sizedefinition-tenbuttons-medium.png)

![tenbuttons small sizedefinition 範本的圖片。](images/overviews/sizedefinition-tenbuttons-small.png)

ElevenButtons

11個按鈕系列控制項。

![elevenbuttons 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-elevenbuttons-large.png)

![elevenbuttons medium sizedefinition 範本的圖片。](images/overviews/sizedefinition-elevenbuttons-medium.png)

![elevenbuttons small sizedefinition 範本的圖片。](images/overviews/sizedefinition-elevenbuttons-small.png)

OneFontControl

其中一個 [**FontControl**](windowsribbon-element-fontcontrol.md)。

僅支援大型和中型群組的大小。

> [!IMPORTANT]
> 架構不支援在自訂範本定義中包含 [**FontControl**](windowsribbon-element-fontcontrol.md) 。

 

![onefontcontrol 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-onefontcontrol-large.png)

![onefontcontrol medium sizedefinition 範本的圖片。](images/overviews/sizedefinition-onefontcontrol-medium.png)

OneInRibbonGallery

一個 [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) 控制項。

僅支援大型和小型群組的大小。

![oneinribbongallery 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-oneinribbongallery-large.png)

![oneinribbongallery small sizedefinition 範本的圖片。](images/overviews/sizedefinition-oneinribbongallery-small.png)

InRibbonGalleryAndBigButton

一個 [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) 控制項和一個按鈕系列控制項。

僅支援大型和小型群組的大小。

![inribbongalleryandbigbutton 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-inribbongalleryandbigbutton-large.png)

![inribbongalleryandbigbutton small sizedefinition 範本的圖片。](images/overviews/sizedefinition-inribbongalleryandbigbutton-small.png)

InRibbonGalleryAndButtons-GalleryScalesFirst

一個 [功能區圖庫](windowsribbon-controls-inribbongallery.md) 控制項，以及兩個或三個按鈕系列控制項。

資源庫會折迭為中等和小型群組大小的快顯視窗表示。

![inribbongalleryandbuttons-galleryscalesfirst 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-large.png)

![inribbongalleryandbuttons-galleryscalesfirst medium sizedefinition 範本的圖片。](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-medium.png)

![inribbongalleryandbuttons-galleryscalesfirst small sizedefinition 範本的圖片。](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-small.png)

ButtonGroups

32按鈕系列控制項的複雜排列 (大多數都是選擇性) 。

> [!Note]  
> 除了大型 ButtonGroups 範本的選擇性完整大小按鈕之外，以此範本宣告的所有控制項元素都必須包含在 [**ControlGroup**](windowsribbon-element-controlgroup.md) 元素中。

 

下列範例示範使用這個範本 (必要和選擇性) 顯示所有32控制項元素所需的標記。


```
<Group CommandName="cmdSizeDefinitionsGroup"
       SizeDefinition="ButtonGroups">
  <!-- Row 1 -->
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton1" />
      <Button CommandName="cmdSDButton2" />
      <Button CommandName="cmdSDButton3" />
      <Button CommandName="cmdSDButton4" />
      <Button CommandName="cmdSDButton5" />
      <Button CommandName="cmdSDButton6" />
      <Button CommandName="cmdSDButton7" />
      <Button CommandName="cmdSDButton8" />
      <Button CommandName="cmdSDButton9" />
      <Button CommandName="cmdSDButton10" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton11" />
      <Button CommandName="cmdSDButton12" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton13" />
      <Button CommandName="cmdSDButton14" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton15" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton16" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton17" />
      <Button CommandName="cmdSDButton18" />
    </ControlGroup>
  </ControlGroup>
  <!-- Row 2 -->
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton19" />
      <Button CommandName="cmdSDButton20" />
      <Button CommandName="cmdSDButton21" />
      <Button CommandName="cmdSDButton22" />
      <Button CommandName="cmdSDButton23" />
      <Button CommandName="cmdSDButton24" />
      <Button CommandName="cmdSDButton25" />
      <Button CommandName="cmdSDButton26" />
      <Button CommandName="cmdSDButton27" />
      <Button CommandName="cmdSDButton28" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton29" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton30" />
      <Button CommandName="cmdSDButton31" />
    </ControlGroup>
  </ControlGroup>
  <Button CommandName="cmdSDButton32" />            
</Group>
```



![buttongroups 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-buttongroups-large.png)

![buttongroups medium sizedefinition 範本的圖片。](images/overviews/sizedefinition-buttongroups-medium.png)

![buttongroups small sizedefinition 範本的圖片。](images/overviews/sizedefinition-buttongroups-small.png)

ButtonGroupsAndInputs

第二個輸入系列控制項 (第二個是選擇性的) 接著是29個按鈕系列控制項的複雜相片順序 (大部分都是選擇性的) 。

僅支援大型和中型群組的大小。

> [!Note]  
> 所有以此範本宣告的控制項元素都必須包含在 [**ControlGroup**](windowsribbon-element-controlgroup.md) 元素中。

 

下列範例示範使用這個範本 (必要和選擇性) 顯示所有控制項元素所需的標記。


```
<Group CommandName="cmdSizeDefinitionsGroup" 
       SizeDefinition="ButtonGroupsAndInputs">
  <!-- Row 1 -->
  <ControlGroup>
    <ControlGroup>
      <ComboBox CommandName="cmdSDComboBox" />
      <Spinner CommandName="cmdSDSpinner" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton1" />
      <Button CommandName="cmdSDButton2" />
      <Button CommandName="cmdSDButton3" />
      <Button CommandName="cmdSDButton4" />
      <Button CommandName="cmdSDButton5" />
      <Button CommandName="cmdSDButton6" />
      <Button CommandName="cmdSDButton7" />
      <Button CommandName="cmdSDButton8" />
      <Button CommandName="cmdSDButton9" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton10" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton11" />
      <Button CommandName="cmdSDButton12" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton13" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton14" />
    </ControlGroup>
  </ControlGroup>
  <!-- Row 2 -->  
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton15" />
      <Button CommandName="cmdSDButton16" />
      <Button CommandName="cmdSDButton17" />
      <Button CommandName="cmdSDButton18" />
      <Button CommandName="cmdSDButton19" />
      <Button CommandName="cmdSDButton20" />
      <Button CommandName="cmdSDButton21" />
      <Button CommandName="cmdSDButton22" />
      <Button CommandName="cmdSDButton23" />
      <Button CommandName="cmdSDButton24" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton25" />
      <Button CommandName="cmdSDButton26" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton27" />
      <Button CommandName="cmdSDButton28" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton29" />
    </ControlGroup>
  </ControlGroup>
</Group>
```



![buttongroupsandinputs 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-buttongroupsandinputs-large.png)

![buttongroupsandinputs medium sizedefinition 範本的圖片。](images/overviews/sizedefinition-buttongroupsandinputs-medium.png)

BigButtonsAndSmallButtonsOrInputs

兩個按鈕系列控制項 (選用) 後面接著二或三個按鈕或輸入系列控制項。

僅支援大型和中型群組的大小。

![bigbuttonsandsmallbuttonsorinputs 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-bigbuttonsandsmallbuttonsorinputs-large.png)

![bigbuttonsandsmallbuttonsorinputs medium sizedefinition 範本的圖片。](images/overviews/sizedefinition-bigbuttonsandsmallbuttonsorinputs-medium.png)



 

### <a name="basic-sizedefinition-example"></a>基本 SizeDefinition 範例

下列程式碼範例提供如何在功能區標記中宣告 [**SizeDefinition**](windowsribbon-element-sizedefinition.md) 範本的基本示範。

*OneInRibbonGallery* [**SizeDefinition**](windowsribbon-element-sizedefinition.md)用於此特定範例，但所有架構範本都是以類似的方式指定。


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



### <a name="complex-sizedefinition-example-with-scaling-policies"></a>具有調整原則的複雜 SizeDefinition 範例

您可以使用功能區標記中的調整原則來控制 [**SizeDefinition**](windowsribbon-element-sizedefinition.md) 範本的折迭行為。

[**ScalingPolicy**](windowsribbon-element-scalingpolicy.md)元素包含 [**ScalingPolicy**](windowsribbon-element-scalingpolicy-idealsizes.md)的資訊清單，並在調整大小功能區 [**時，指定**](windowsribbon-element-scale.md)一或多個 [**群組**](windowsribbon-element-group.md)元素的自我調整版面配置喜好設定。

> [!Note]  
> 強烈建議您指定適當的調整原則詳細資料，如此一來，大部分的 [**群組**](windowsribbon-element-group.md)元素都會與 *大小* 屬性等於的 [**縮放**](windowsribbon-element-scale.md)元素相關聯 `Popup` 。 這麼做可讓架構盡可能以最小的大小轉譯功能區，並支援最大範圍的顯示裝置，再自動導入滾動機制。

 

下列程式碼範例會示範 [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md)資訊清單，該資訊清單會針對 [**主** 資料夾] 索引標籤上的四個控制項群組，指定 [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md)喜好設定。此外，也會指定 [**小**](windowsribbon-element-scale.md)數位數元素，以影響每個群組的折迭行為（依遞減大小排序）。


```C++
<Tab CommandName="Home">
  <Tab.ScalingPolicy>
    <ScalingPolicy>
      <ScalingPolicy.IdealSizes>
        <Scale Group="GroupClipboard" Size="Medium"/>
        <Scale Group="GroupView" Size="Large"/>
        <Scale Group="GroupFont" Size="Large"/>
        <Scale Group="GroupParagraph" Size="Large"/>
      </ScalingPolicy.IdealSizes>
      <Scale Group="GroupClipboard" Size="Small"/>
      <Scale Group="GroupClipboard" Size="Popup"/>
      <Scale Group="GroupFont" Size="Medium"/>
      <Scale Group="GroupFont" Size="Popup"/>
      <Scale Group="GroupParagraph" Size="Medium"/>
      <Scale Group="GroupParagraph" Size="Popup"/>
      <!-- 
        GroupView group is associated with the OneButton SizeDefinition.
        Since this template is constrained to one size (Large) there
        is no need to declare further scaling preferences.
      -->
    </ScalingPolicy>
  </Tab.ScalingPolicy>

  <Group CommandName="GroupClipboard" SizeDefinition="FourButtons">
    <Button CommandName="Paste"/>
    <Button CommandName="Cut"/>
    <Button CommandName="Copy"/>
    <Button CommandName="SelectAll"/>
  </Group>

  <Group CommandName="GroupFont"  ApplicationModes="1">
    <FontControl CommandName="Font" FontType="FontWithColor" />
  </Group>

  <Group CommandName="GroupParagraph"  ApplicationModes="1" SizeDefinition="ButtonGroups">
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="Numbered" />
        <ToggleButton CommandName="Bulleted" />
      </ControlGroup>
    </ControlGroup>
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="LeftJustify" />
        <ToggleButton CommandName="CenterJustify" />
        <ToggleButton CommandName="RightJustify" />
      </ControlGroup>
      <ControlGroup/>
      <ControlGroup>
        <Button CommandName="Outdent" />
        <Button CommandName="Indent" />
      </ControlGroup>
    </ControlGroup>
  </Group>

  <Group CommandName="GroupView" SizeDefinition="OneButton" >
    <ToggleButton CommandName="ViewSource"/>
  </Group>

</Tab>
```



### <a name="custom-templates"></a>自訂範本

如果預設的版面配置行為和預先定義的 [**SizeDefinition**](windowsribbon-element-sizedefinition.md) 範本未提供特定版面配置案例的彈性或支援，功能區架構會透過 [**SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) 元素來支援自訂範本。

您可以使用下列兩種方式宣告自訂範本：使用 [**SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) 專案的獨立方法，宣告可重複使用的、命名範本或 [**群組**](windowsribbon-element-group.md)特定的內嵌方法。

### <a name="standalone-template"></a>獨立範本

下列程式碼範例說明基本、可重複使用的自訂範本。


```
<Ribbon.SizeDefinitions>
  <SizeDefinition Name="CustomTemplate">
    <GroupSizeDefinition Size="Large">
      <ControlSizeDefinition ImageSize="Large" IsLabelVisible="true" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Medium">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Small">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
  </SizeDefinition>
</Ribbon.SizeDefinitions>
```



### <a name="inline-template"></a>內嵌範本

下列程式碼範例說明四個按鈕群組的基本內嵌自訂範本。

這段程式碼會顯示一組按鈕的命令宣告。 您也可以在這裡指定大型和小型影像資源。


```XML
<!-- Button -->
<Command Name="cmdButtonGroup"
         Symbol="cmdButtonGroup"
         Comment="Button Group"
         LabelTitle="ButtonGroup"/>
<Command Name="cmdButton1"
         Symbol="cmdButton1"
         Comment="Button1"
         LabelTitle="Button1"/>
<Command Name="cmdButton2"
         Symbol="cmdButton2"
         Comment="Button2"
         LabelTitle="Button2"/>
<Command Name="cmdButton3"
         Symbol="cmdButton3"
         Comment="Button3"
         LabelTitle="Button3"/>
<Command Name="cmdButtonGroup2"
         Symbol="cmdButtonGroup2"
         Comment="Button Group2"
         LabelTitle="ButtonGroup2"/>
<Command Name="cmdButtonG21"
         Symbol="cmdButtonG21"
         Comment="ButtonG21"
         LabelTitle="ButtonG21">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG22"
         Symbol="cmdButtonG22"
         Comment="ButtonG22"
         LabelTitle="ButtonG22">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG23"
         Symbol="cmdButtonG23"
         Comment="ButtonG23"
         LabelTitle="ButtonG23">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG24"
         Symbol="cmdButtonG24"
         Comment="ButtonG24"
         LabelTitle="ButtonG24">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
```



這一節的程式碼示範如何定義大型、中型和 small [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) 範本，以顯示各種不同大小和版面配置的四個按鈕。 索引標籤的 [ [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) ] 宣告會根據 [使用中] 索引標籤所需的功能區大小和空間，定義要用於控制項群組的範本。


```XML
        <Tab CommandName="cmdTab6">
          <Tab.ScalingPolicy>
            <ScalingPolicy>
              <ScalingPolicy.IdealSizes>
                <Scale Group="cmdButtonGroup"
                       Size="Large"/>
                <Scale Group="cmdButtonGroup2"
                       Size="Large"/>
                <Scale Group="cmdToggleButtonGroup"
                       Size="Large"/>
              </ScalingPolicy.IdealSizes>
              <Scale Group="cmdButtonGroup"
                     Size="Medium"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Medium"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Small"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Popup"/>
            </ScalingPolicy>
          </Tab.ScalingPolicy>

          <Group CommandName="cmdButtonGroup2">
            <SizeDefinition>
              <ControlNameMap>
                <ControlNameDefinition Name="button1"/>
                <ControlNameDefinition Name="button2"/>
                <ControlNameDefinition Name="button3"/>
                <ControlNameDefinition Name="button4"/>
              </ControlNameMap>
              <GroupSizeDefinition Size="Large">
                <ControlGroup>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Large"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Large"
                                         IsLabelVisible="true" />
                </ControlGroup>
                <ColumnBreak ShowSeparator="true"/>
                <ControlGroup>
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Large"
                                        IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                        ImageSize="Large"
                                        IsLabelVisible="true" />
                </ControlGroup>
              </GroupSizeDefinition>
              <GroupSizeDefinition Size="Medium">
                <Row>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                </Row>
                <Row>
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                </Row>
              </GroupSizeDefinition>
              <GroupSizeDefinition Size="Small">
                <Row>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Small"
                                         IsLabelVisible="false" />
                </Row>
                <Row>
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                         ImageSize="Small"
                                         IsLabelVisible="false" />
                </Row>
              </GroupSizeDefinition>
            </SizeDefinition>
            <Button CommandName="cmdButtonG21"></Button>
            <Button CommandName="cmdButtonG22"></Button>
            <Button CommandName="cmdButtonG23"></Button>
            <Button CommandName="cmdButtonG24"></Button>
          </Group>
          <Group CommandName="cmdCheckBoxGroup">
            <CheckBox CommandName="cmdCheckBox"></CheckBox>
          </Group>
          <Group CommandName="cmdToggleButtonGroup"
                 SizeDefinition="OneButton">
            <ToggleButton CommandName="cmdToggleButton"></ToggleButton>
          </Group>
          <Group CommandName="cmdButtonGroup"
                 SizeDefinition="ThreeButtons">
            <Button CommandName="cmdButton1"></Button>
            <Button CommandName="cmdButton2"></Button>
            <Button CommandName="cmdButton3"></Button>
          </Group>
        </Tab>
```



下圖顯示上一個範例中的範本如何套用至功能區 UI，以配合功能區大小的減少。



|        |                                                                                                    |
|--------|----------------------------------------------------------------------------------------------------|
| 大  | ![內嵌大型自訂範本的圖片。](images/overviews/sizedefinition-custom-large.png)   |
| 中 | ![內嵌中型自訂範本的圖片。](images/overviews/sizedefinition-custom-medium.png) |
| 小  | ![內嵌小型自訂範本的圖片。](images/overviews/sizedefinition-custom-small.png)   |
| 快顯  | ![內嵌快顯視窗自訂範本的圖片。](images/overviews/sizedefinition-custom-popup.png)   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**SizeDefinition**](windowsribbon-element-sizedefinition.md)
</dt> <dt>

[**調整**](windowsribbon-element-scale.md)
</dt> <dt>

[**Group**](windowsribbon-element-group.md)
</dt> </dl>

 

 






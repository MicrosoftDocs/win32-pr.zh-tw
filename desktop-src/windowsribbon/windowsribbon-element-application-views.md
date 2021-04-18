---
title: Views 屬性
description: 表示每個功能區架構視圖的容器，特別是功能區和 CoNtextPopup。
ms.assetid: e7549b8b-0f95-477a-9024-1a99ee1412c2
keywords:
- 應用程式。 Views 屬性視窗功能區
topic_type:
- apiref
api_name:
- Application.Views
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57e7d106d346a790ee3bd8879b2367f38341f0a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968560"
---
# <a name="applicationviews-property"></a>Views 屬性

表示每個功能區架構視圖的容器，特別是 [**功能區**](windowsribbon-element-ribbon.md) 和 [**CoNtextPopup**](windowsribbon-element-contextpopup.md)。

## <a name="usage"></a>使用方式

``` syntax
<Application.Views>
  child elements
</Application.Views>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



| 元素                                                               | 描述                                        |
|-----------------------------------------------------------------------|----------------------------------------------------|
| [**CoNtextPopup**](windowsribbon-element-contextpopup.md)<br/> | 可能會發生一次或多次<br/> <br/> |
| [**功能區**](windowsribbon-element-ribbon.md)<br/>             | 必須剛好發生一次<br/> <br/>     |



## <a name="parent-elements"></a>父元素



| 元素                                                             |
|---------------------------------------------------------------------|
| [**應用程式**](windowsribbon-element-application.md)<br/> |



## <a name="remarks"></a>備註

必要。

必須針對每個 [**應用程式**](windowsribbon-element-application.md) 元素剛好出現一次。

## <a name="examples"></a>範例

下列範例顯示的是一個 **應用程式。 Views** 元素包含功能區控制項的資訊清單，而且每個專案都有一個在 [**Application 命令**](windowsribbon-element-application-commands.md) 專案中宣告之命令的參考。


```C++
<Application.Views>
  <Ribbon Name="ScenicRibbonSampleApp">
    <Ribbon.Tabs>
```




```C++
<Tab CommandName="cmdHomeTab">
  <Group CommandName="cmdClipboardGroup" 
         SizeDefinition="ThreeButtons">
    <Button CommandName="cmdCopy"/>
    <Button CommandName="cmdPaste"/>
    <ToggleButton CommandName="cmdMinimize"/>
  </Group>
</Tab>
```




```C++
    </Ribbon.Tabs>
  </Ribbon>
</Application.Views>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**應用程式。命令**](windowsribbon-element-application-commands.md)
</dt> </dl>

 

 






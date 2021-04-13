---
title: '[功能區] 索引標籤屬性'
description: 代表功能區中所有核心索引標籤的容器。
ms.assetid: b43d0544-c110-4785-85d7-935842b8f03e
keywords:
- '[功能區] 屬性視窗功能區'
topic_type:
- apiref
api_name:
- Ribbon.Tabs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4300a2385b6ada64e05e16671802460930cc2a7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464441"
---
# <a name="ribbontabs-property"></a>[功能區] 索引標籤屬性

代表功能區中所有核心索引標籤的容器。

## <a name="usage"></a>使用方式

``` syntax
<Ribbon.Tabs>
  child elements
</Ribbon.Tabs>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



| 元素                                             | 描述                                     |
|-----------------------------------------------------|-------------------------------------------------|
| [**索引標籤**](windowsribbon-element-tab.md)<br/> | 至少必須發生一次<br/> <br/> |



## <a name="parent-elements"></a>父元素



| 元素                                                   |
|-----------------------------------------------------------|
| [**功能區**](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a>備註

必要。

每個 [**功能區**](windowsribbon-element-ribbon.md)可能會出現一次或多次。

## <a name="examples"></a>範例

下列範例會示範 **功能區** 的基本標記，其中包含 **首頁** [](windowsribbon-element-tab.md)索引標籤宣告。


```C++
<Ribbon Name="ScenicRibbonSampleApp">
  <Ribbon.QuickAccessToolbar>
  ...
  </Ribbon.QuickAccessToolbar>
  <Ribbon.ApplicationMenu>
  ...
  </Ribbon.ApplicationMenu>
  <Ribbon.SizeDefinitions>
  ...
  </Ribbon.SizeDefinitions>
  <Ribbon.Tabs>
  ...
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
  ...
  </Ribbon.Tabs>
  <Ribbon.ContextualTabs>
  ...
  </Ribbon.ContextualTabs>
  <Ribbon.HelpButton>
  ...
  </Ribbon.HelpButton>
</Ribbon>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**功能區. CoNtextualTabs**](windowsribbon-element-ribbon-contextualtabs.md)
</dt> </dl>

 

 






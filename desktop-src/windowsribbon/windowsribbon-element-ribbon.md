---
title: 功能區元素
description: 表示功能區視圖中的功能區控制項。
ms.assetid: 51083180-4e86-4c90-9fd1-a58c12bcc756
keywords:
- 功能區元素 Windows 功能區
topic_type:
- apiref
api_name:
- Ribbon
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 70841866ec656dc840fb467d598cc42bf919283b
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122630914"
---
# <a name="ribbon-element"></a>功能區元素

表示功能區視圖中的功能區控制項。

## <a name="usage"></a>使用方式

``` syntax
<Ribbon
  Name = "xs:string"
  GroupSpacing = "xs:string">
  child elements
</Ribbon>
```

## <a name="attributes"></a>屬性



<table>
<colgroup>
<col  />
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>屬性</th>
<th>類型</th>
<th>必要</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>GroupSpacing</strong><br/></td>
<td>xs:string<br/></td>
<td>否<br/></td>
<td><dt><span></span><span></span><strong></strong> (Small) <br/> </dt> <dd> 預設值。 <br/> </dd> <dt><span></span><span></span><strong></strong> (中) <br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (大型) <br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>名稱</strong><br/></td>
<td>xs:string<br/></td>
<td>否<br/></td>
<td>用來批註命令元素。<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： string) <br/> </dt> <dd> 任何零或多個字元的序列。<br/> 長度上限為未系結。<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>子元素



| 元素                                                                                         | 描述                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [**功能區. ApplicationMenu**](windowsribbon-element-ribbon-applicationmenu.md)<br/>       | 最多可能發生一次<br/> <br/> |
| [**功能區. CoNtextualTabs**](windowsribbon-element-ribbon-contextualtabs.md)<br/>         | 最多可能發生一次<br/> <br/> |
| [**功能區. HelpButton**](windowsribbon-element-ribbon-helpbutton.md)<br/>                 | 最多可能發生一次<br/> <br/> |
| [**功能區. QuickAccessToolbar**](windowsribbon-element-ribbon-quickaccesstoolbar.md)<br/> | 最多可能發生一次<br/> <br/> |
| [**功能區. SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md)<br/>       | 最多可能發生一次<br/> <br/> |
| [**功能區] 索引標籤**](windowsribbon-element-ribbon-tabs.md)<br/>                             | 最多可能發生一次<br/> <br/> |



## <a name="parent-elements"></a>父元素



| 元素                                                                         |
|---------------------------------------------------------------------------------|
| [**應用程式。 Views**](windowsribbon-element-application-views.md)<br/> |



## <a name="remarks"></a>備註

必要。

每個應用程式都必須剛好發生一次 [**。 Views**](windowsribbon-element-application-views.md) 元素。

## <a name="examples"></a>範例

下列範例會示範 **功能區** 視圖的基本標記。


```XML
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
  </Ribbon.Tabs>
  <Ribbon.ContextualTabs>
  ...
  </Ribbon.ContextualTabs>
  <Ribbon.HelpButton>
  ...
  </Ribbon.HelpButton>
</Ribbon>
```



## <a name="element-information"></a>項目資訊




* **最低支援系統**： Windows 7
* **可以是空** 的：否



 

 






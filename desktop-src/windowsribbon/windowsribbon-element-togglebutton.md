---
title: 切換按鈕元素
description: 代表切換按鈕控制項。
ms.assetid: f26a90e6-9e9a-4fde-8753-50b8b1d09f80
keywords:
- 切換按鈕元素視窗功能區
topic_type:
- apiref
api_name:
- ToggleButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 652ea7b535f41cc3dbb40f25bbe49ab4fe52f5ff
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/11/2020
ms.locfileid: "104314136"
---
# <a name="togglebutton-element"></a>切換按鈕元素

代表 [切換按鈕](windowsribbon-controls-togglebutton.md) 控制項。

## <a name="usage"></a>使用方式

``` syntax
<ToggleButton
  CommandName = "xs:positiveInteger or xs:string"
  ApplicationDefaults.IsChecked = "Boolean"/>
```

## <a name="attributes"></a>屬性



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
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
<td><strong>S. IsChecked</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>只有當 <strong>切換按鈕</strong> 專案是 <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar. s</strong></a>的子系時，這個屬性才有效。 <br/> 限制為下列其中一個值：<br/> <br/>
<dt><span></span><span></span><strong></strong> (true) <br/> </dt> <dd> 預設值。 <br/> </dd> <dt><span></span><span></span><strong></strong> (false) <br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs： positiveInteger 或 xs： string<br/></td>
<td>No<br/></td>
<td>將元素與 <a href="windowsribbon-element-command.md"><strong>命令</strong></a>產生關聯。<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) <br/> </dt> <dd> 字串、介於2與59999（含）之間的整數值，或介於0x2 與0xea5f （含）之間的十六進位值。 <br/> 值在功能區 XML 檔中必須是唯一的。 <br/> 最大長度：100個字元。 <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>子元素

沒有任何子項目。

## <a name="parent-elements"></a>父元素



| 元素                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/>                                                     |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>                                                 |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>                                               |
| [**Group**](windowsribbon-element-group.md)<br/>                                                                   |
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/>                                                           |
| [**QuickAccessToolbar. s**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                                                       |
| [**SplitButton. ButtonItem**](windowsribbon-element-splitbutton-buttonitem.md)<br/>                                 |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/>                                         |



## <a name="remarks"></a>備註

選擇性或必要，視父元素而定。

每個 [**SplitButton. ButtonItem**](windowsribbon-element-splitbutton-buttonitem.md) 元素最多可能會發生一次。

可能會針對每個 [**ControlGroup**](windowsribbon-element-controlgroup.md)、 [**DropDownButton**](windowsribbon-element-dropdownbutton.md)、 [**Group**](windowsribbon-element-group.md)、 [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)、 [**MenuGroup**](windowsribbon-element-menugroup.md)、 [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)、s、 [**SplitButton**](windowsribbon-element-splitbutton.md)或 [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) 元素執行一次或多次。

## <a name="examples"></a>範例

下列範例示範 **切換按鈕** 元素的基本標記。

這段程式碼會顯示 [**QuickAccessToolbar. s**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)元素內的 **切換按鈕** 元素宣告。


```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```



## <a name="element-information"></a>項目資訊



|                                     |           |
|-------------------------------------|-----------|
| 最低支援系統<br/> | Windows 7 |
| 可以是空的                        | Yes       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[切換按鈕控制項](windowsribbon-controls-togglebutton.md)
</dt> </dl>

 

 






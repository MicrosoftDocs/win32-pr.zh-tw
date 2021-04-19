---
title: QuickAccessToolbar. s 屬性
description: 代表快速存取工具列 (QAT) 中預設命令的容器。
ms.assetid: 8f44d7c0-1a39-4a88-ae01-7d7d1bb6bf7e
keywords:
- QuickAccessToolbar. s 屬性 Windows 功能區
topic_type:
- apiref
api_name:
- QuickAccessToolbar.ApplicationDefaults
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 084ea334441cb0cf545adaa3d1016f7d02da1b88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106995161"
---
# <a name="quickaccesstoolbarapplicationdefaults-property"></a>QuickAccessToolbar. s 屬性

代表 [快速存取工具列 (QAT) ](windowsribbon-controls-quickaccesstoolbar.md)中預設命令的容器。

## <a name="usage"></a>使用方式

``` syntax
<QuickAccessToolbar.ApplicationDefaults>
  child elements
</QuickAccessToolbar.ApplicationDefaults>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>元素</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="windowsribbon-element-button.md"><strong>Button</strong></a><br/></td>
<td>必須至少發生一次。<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-element-checkbox.md"><strong>相應</strong></a><br/></td>
<td>必須至少發生一次。<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-element-combobox.md"><strong>ComboBox</strong></a><br/></td>
<td>必須至少發生一次。<br/>
<blockquote>
[!Note]<br />
Windows 8 和更新版本。
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-element-dropdowngallery.md"><strong>DropDownGallery</strong></a><br/></td>
<td>必須至少發生一次。<br/>
<blockquote>
[!Note]<br />
Windows 8 和更新版本。
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-element-inribbongallery.md"><strong>InRibbonGallery</strong></a><br/></td>
<td>必須至少發生一次。<br/>
<blockquote>
[!Note]<br />
Windows 8 和更新版本。
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-element-splitbuttongallery.md"><strong>SplitButtonGallery</strong></a><br/></td>
<td>必須至少發生一次。<br/>
<blockquote>
[!Note]<br />
Windows 8 和更新版本。
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-element-togglebutton.md"><strong>ToggleButton</strong></a><br/></td>
<td>必須至少發生一次。<br/> <br/></td>
</tr>
</tbody>
</table>



## <a name="parent-elements"></a>父元素



| 元素                                                                           |
|-----------------------------------------------------------------------------------|
| [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md)<br/> |



## <a name="remarks"></a>備註

選擇性。

每個 [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md)最多可能會發生一次。

至少必須指定一個子項目。

最多可以指定20個子項目。

## <a name="examples"></a>範例

下列範例示範 [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md)的基本標記。

這段程式碼會顯示 **QuickAccessToolbar s** 控制項宣告。


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



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[快速存取工具列控制項](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 






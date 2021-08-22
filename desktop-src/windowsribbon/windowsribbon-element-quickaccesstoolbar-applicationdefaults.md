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
ms.openlocfilehash: 701a7c72e40b1efe9104d6794fa739c556b0fb4b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473744"
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




| 元素 | 描述 | 
|---------|-------------|
| <a href="windowsribbon-element-button.md"><strong>Button</strong></a><br /> | 必須至少發生一次。<br /><br /> | 
| <a href="windowsribbon-element-checkbox.md"><strong>CheckBox</strong></a><br /> | 必須至少發生一次。<br /><br /> | 
| <a href="windowsribbon-element-combobox.md"><strong>ComboBox</strong></a><br /> | 必須至少發生一次。<br /><blockquote>[!Note]<br />Windows 8 和更新版本。</blockquote><br /><br /> | 
| <a href="windowsribbon-element-dropdowngallery.md"><strong>DropDownGallery</strong></a><br /> | 必須至少發生一次。<br /><blockquote>[!Note]<br />Windows 8 和更新版本。</blockquote><br /><br /> | 
| <a href="windowsribbon-element-inribbongallery.md"><strong>InRibbonGallery</strong></a><br /> | 必須至少發生一次。<br /><blockquote>[!Note]<br />Windows 8 和更新版本。</blockquote><br /><br /> | 
| <a href="windowsribbon-element-splitbuttongallery.md"><strong>SplitButtonGallery</strong></a><br /> | 必須至少發生一次。<br /><blockquote>[!Note]<br />Windows 8 和更新版本。</blockquote><br /><br /> | 
| <a href="windowsribbon-element-togglebutton.md"><strong>ToggleButton</strong></a><br /> | 必須至少發生一次。<br /><br /> | 




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
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[快速存取工具列控制項](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 






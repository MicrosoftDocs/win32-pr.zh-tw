---
title: CoNtextMenu 元素
description: 表示內容功能表控制項。
ms.assetid: 08cc0514-0795-4e6b-b80c-33d920783032
keywords:
- CoNtextMenu 元素 Windows 功能區
topic_type:
- apiref
api_name:
- ContextMenu
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4fb061c08635cff46ca80d803089ebc01c48c19cdcc9136b1052c5a0ef2c3a1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118707431"
---
# <a name="contextmenu-element"></a>CoNtextMenu 元素

表示內容功能表控制項。

## <a name="usage"></a>使用方式

``` syntax
<ContextMenu
  Name = "xs:string">
  child elements
</ContextMenu>
```

## <a name="attributes"></a>屬性



| 屬性           | 類型                 | 必要       | 描述                                                                                                                                                                                                                |
|---------------------|----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **名稱**<br/> | xs:string<br/> | Yes<br/> | <dt> (xs： string) <br/> </dt> <dd> 由任何字元序列組成的字串，包括空白字元和分行符號字元。<br/> </dd> </dl> |



## <a name="child-elements"></a>子元素



| 元素                                                         | 描述                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/> | 至少必須發生一次<br/> <br/> |



## <a name="parent-elements"></a>父元素



| 元素                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [**CoNtextPopup. CoNtextmenu**](windowsribbon-element-contextpopup-contextmenus.md)<br/> |



## <a name="remarks"></a>備註

選擇性。

每個 [**CoNtextPopup coNtextmenu**](windowsribbon-element-contextpopup-contextmenus.md)可能會發生一次或多次。

> [!IMPORTANT]
> **CoNtextMenu** 無法裝載 [下拉式](windowsribbon-controls-combobox.md)方塊或 [微調](windowsribbon-controls-spinner.md)控制項。

 

## <a name="examples"></a>範例

下列範例示範 [**CoNtextPopup**](windowsribbon-element-contextpopup.md) View 的基本標記。

這段程式碼會顯示一組 **CoNtextMenu** 控制項宣告。


```XML
    <ContextPopup>
      <!--
        The MiniToolbars and Context Menus are the basic ingredients for 
        the contextual UI popup. 
        Mix-and-match and associate each combination with a ContextMap Command 
        invoked in code.
      -->
      <ContextPopup.MiniToolbars>
        <MiniToolbar Name="MiniToolbar1">
          <MenuGroup Class="MajorItems">
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdPaste" />
          </MenuGroup>
          <MenuGroup>
            <ToggleButton CommandName="cmdToggleButton" />
            <DropDownButton CommandName="cmdButtons">
              <MenuGroup>
                <Button CommandName="cmdButton1" />
                <Button CommandName="cmdButton2" />
                <Button CommandName="cmdButton3" />
              </MenuGroup>
            </DropDownButton>
          </MenuGroup>
        </MiniToolbar>
        <MiniToolbar Name="MiniToolbar2">
          <MenuGroup>
            <Button CommandName="cmdButton1" />
            <Button CommandName="cmdButton2" />
            <Button CommandName="cmdButton3" />
          </MenuGroup>
        </MiniToolbar>
      </ContextPopup.MiniToolbars>
      <ContextPopup.ContextMenus>
        <ContextMenu Name="ContextMenu1">
          <MenuGroup>
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdPaste" />
          </MenuGroup>
        </ContextMenu>
        <ContextMenu Name="ContextMenu2">
          <MenuGroup>
            <ToggleButton CommandName="cmdToggleButton" />
          </MenuGroup>
          <MenuGroup>
            <Button CommandName="cmdButton1" />
            <Button CommandName="cmdButton2" />
            <Button CommandName="cmdButton3" />
          </MenuGroup>
        </ContextMenu>
        <ContextMenu Name="ContextMenu4">
          <MenuGroup>
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdPaste" />
          </MenuGroup>
          <MenuGroup>
            <ToggleButton CommandName="cmdToggleButton" />
          </MenuGroup>
          <MenuGroup>
            <Button CommandName="cmdButton1" />
            <Button CommandName="cmdButton2" />
            <Button CommandName="cmdButton3" />
          </MenuGroup>
        </ContextMenu>
      </ContextPopup.ContextMenus>
      <ContextPopup.ContextMaps>
        <ContextMap CommandName="cmdContextMap1"
                    ContextMenu="ContextMenu1"/>
        <ContextMap CommandName="cmdContextMap2"
                    ContextMenu="ContextMenu2"
                    MiniToolbar="MiniToolbar1"/>
        <ContextMap CommandName="cmdContextMap3"
                    MiniToolbar="MiniToolbar2"/>
        <ContextMap CommandName="cmdContextMap4"
                    ContextMenu="ContextMenu4"/>
      </ContextPopup.ContextMaps>
    </ContextPopup>
```



## <a name="element-information"></a>項目資訊

* **最低支援系統**： Windows 7
* **可以是空** 的：否



## <a name="see-also"></a>另請參閱

<dl> <dt>

[CoNtext Popup 控制項](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 






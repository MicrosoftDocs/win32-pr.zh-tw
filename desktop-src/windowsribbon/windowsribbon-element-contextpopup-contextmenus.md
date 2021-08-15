---
title: CoNtextPopup. CoNtextmenu 屬性
description: 代表 CoNtextMenu 元素的容器。
ms.assetid: 92633689-a892-421e-a5fb-e494f4cd1ea8
keywords:
- CoNtextPopup. coNtextmenu 屬性 Windows 功能區
topic_type:
- apiref
api_name:
- ContextPopup.ContextMenus
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45641f1431726ec75c60be48683f19fb3139cbd9159baaed9def3b293a48772d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117851014"
---
# <a name="contextpopupcontextmenus-property"></a>CoNtextPopup. CoNtextmenu 屬性

代表 [**CoNtextMenu**](windowsribbon-element-contextmenu.md) 元素的容器。

## <a name="usage"></a>使用方式

``` syntax
<ContextPopup.ContextMenus>
  child elements
</ContextPopup.ContextMenus>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



| 元素                                                             | 描述                                        |
|---------------------------------------------------------------------|----------------------------------------------------|
| [**ContextMenu**](windowsribbon-element-contextmenu.md)<br/> | 可能會發生一次或多次<br/> <br/> |



## <a name="parent-elements"></a>父元素



| 元素                                                               |
|-----------------------------------------------------------------------|
| [**CoNtextPopup**](windowsribbon-element-contextpopup.md)<br/> |



## <a name="remarks"></a>備註

選擇性。

每個 [**CoNtextPopup**](windowsribbon-element-contextpopup.md)最多可能會發生一次。

## <a name="examples"></a>範例

下列範例示範 [**CoNtextPopup**](windowsribbon-element-contextpopup.md) View 的基本標記。

這一節的程式碼顯示 **CoNtextPopup coNtextmenu** 控制項宣告。


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



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[CoNtext Popup 控制項](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 






---
title: CoNtextPopup 元素
description: 表示 CoNtextPopup View 中的內容快顯視窗控制項。
ms.assetid: b955be16-803e-47b5-a72d-f993180fbf14
keywords:
- CoNtextPopup 元素視窗功能區
topic_type:
- apiref
api_name:
- ContextPopup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4feb7c4fbd2ca538fe4d0c2b2584163ee8c9fcea
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022520"
---
# <a name="contextpopup-element"></a>CoNtextPopup 元素

表示 CoNtextPopup View 中的 [內容快顯視窗](windowsribbon-controls-contextpopup.md) 控制項。

## <a name="usage"></a>使用方式

``` syntax
<ContextPopup>
  child elements
</ContextPopup>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



| 元素                                                                                         | 描述                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [**CoNtextPopup.CoNtextMaps**](windowsribbon-element-contextpopup-contextmaps.md)<br/>   | 最多可能發生一次<br/> <br/> |
| [**CoNtextPopup. CoNtextmenu**](windowsribbon-element-contextpopup-contextmenus.md)<br/> | 最多可能發生一次<br/> <br/> |
| [**CoNtextPopup.MiniToolbars**](windowsribbon-element-contextpopup-minitoolbars.md)<br/> | 最多可能發生一次<br/> <br/> |



## <a name="parent-elements"></a>父元素



| 元素                                                                         |
|---------------------------------------------------------------------------------|
| [**應用程式。 Views**](windowsribbon-element-application-views.md)<br/> |



## <a name="remarks"></a>備註

選擇性。

每個 [**應用程式**](windowsribbon-element-application-views.md)最多可能會發生一次。

## <a name="examples"></a>範例

下列範例示範 **CoNtextPopup** View 的基本標記。


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



|                                     |           |
|-------------------------------------|-----------|
| 最低支援系統<br/> | Windows 7 |
| 可以是空的                        | 否        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[CoNtext Popup 控制項](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 






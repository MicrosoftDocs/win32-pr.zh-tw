---
title: 浮動工具列元素
description: 表示內容相關的工具列。
ms.assetid: bb50890d-554a-4add-a583-d4fd48b823bf
keywords:
- 浮動工具列元素 Windows 功能區
topic_type:
- apiref
api_name:
- MiniToolbar
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e47fee9fbf2b6b0bc95153fd512f6484129dc7f3edebd56e1d97664ecc2bbef0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881738"
---
# <a name="minitoolbar-element"></a>浮動工具列元素

表示內容相關的工具列。

## <a name="usage"></a>使用方式

``` syntax
<MiniToolbar
  Name = "xs:string">
  child elements
</MiniToolbar>
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
| [**CoNtextPopup.MiniToolbars**](windowsribbon-element-contextpopup-minitoolbars.md)<br/> |



## <a name="remarks"></a>備註

選擇性。

每個 [**CoNtextPopup MiniToolbars**](windowsribbon-element-contextpopup-minitoolbars.md)可能會發生一次或多次。

與 [**CoNtextMenu**](windowsribbon-element-contextmenu.md) 元素不同，按一下工具列上的專案時， **浮動工具列** 會保持可見。

如果在沒有 [**CoNtextMenu**](windowsribbon-element-contextmenu.md)的情況下顯示，當滑鼠指標移開時， **浮動工具列** 就會淡出。

> [!Note]  
> 由於這種淡化行為的緣故， [**CoNtextMenu**](windowsribbon-element-contextmenu.md) 應該會顯示在靠近滑鼠指標的附近。

 

因為 **浮動工具列** 中的控制項無法存取鍵盤，所以它們所公開的命令應該可在功能區 UI 中的其他位置使用。

## <a name="examples"></a>範例

下列範例示範 [**CoNtextPopup**](windowsribbon-element-contextpopup.md) View 的基本標記。

這段程式碼會顯示一組 **浮動工具列** 控制項宣告。


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

 

 






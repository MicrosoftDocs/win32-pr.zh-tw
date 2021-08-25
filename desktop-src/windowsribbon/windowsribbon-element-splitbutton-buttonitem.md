---
title: SplitButton. ButtonItem 屬性
description: 代表按鈕或切換按鈕的容器，該按鈕會公開分割按鈕的預設命令。
ms.assetid: 3d46d606-238d-46d4-b92e-dfd759951770
keywords:
- SplitButton. ButtonItem 屬性 Windows 功能區
topic_type:
- apiref
api_name:
- SplitButton.ButtonItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f49f316f7c740b434f761bbe4c00906c8f76b5027af9fcc87317af2a51960dab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119840688"
---
# <a name="splitbuttonbuttonitem-property"></a>SplitButton. ButtonItem 屬性

代表 [按鈕](windowsribbon-controls-button.md) 或 [切換按鈕](windowsribbon-controls-togglebutton.md) 的容器，該按鈕會公開 [分割按鈕](windowsribbon-controls-splitbutton.md)的預設命令。

## <a name="usage"></a>使用方式

``` syntax
<SplitButton.ButtonItem>
  child elements
</SplitButton.ButtonItem>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



| 元素                                                               | 描述                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| [**Button**](windowsribbon-element-button.md)<br/>             | 最多可能發生一次<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/> | 最多可能發生一次<br/> <br/> |



## <a name="parent-elements"></a>父元素



| 元素                                                             |
|---------------------------------------------------------------------|
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/> |



## <a name="remarks"></a>備註

選擇性。

每個 [**SplitButton**](windowsribbon-element-splitbutton.md)最多可能會發生一次。

每個 **SplitButton. ButtonItem** 只能包含一個 [**按鈕**](windowsribbon-element-button.md) 或 [**切換**](windowsribbon-element-togglebutton.md) 按鈕子項目。

## <a name="examples"></a>範例

下列範例示範 [分割按鈕](windowsribbon-controls-splitbutton.md)的基本標記。

這段程式碼會顯示 [**SplitButton**](windowsribbon-element-splitbutton.md)和 **SplitButton ButtonItem** 命令宣告，以及可作為 **SplitButton** 元素父容器的相關聯 [**群組**](windowsribbon-element-group.md)。


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



這段程式碼會顯示 [**SplitButton**](windowsribbon-element-splitbutton.md) 和 **SplitButton ButtonItem** 控制項宣告。


```XML
<Group CommandName="cmdSplitButtonGroup">
  <SplitButton CommandName="cmdSplitButton">
    <SplitButton.ButtonItem>
      <Button CommandName="cmdSBButtonItem"/>
    </SplitButton.ButtonItem>
    <SplitButton.MenuGroups>
      <MenuGroup CommandName="cmdSBMajorItems" 
                 Class="MajorItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup CommandName="cmdSBStandardItems"
                 Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
    </SplitButton.MenuGroups>
  </SplitButton>
</Group>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[分割按鈕控制項](windowsribbon-controls-splitbutton.md)
</dt> </dl>

 

 






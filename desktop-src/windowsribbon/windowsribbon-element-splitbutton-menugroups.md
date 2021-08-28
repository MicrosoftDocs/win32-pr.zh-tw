---
title: SplitButton. MenuGroups 屬性
description: 表示標準分割按鈕控制項中一組下拉式功能表專案的容器。
ms.assetid: 6328ad49-037b-4cd5-90f6-b91646e260ee
keywords:
- SplitButton. MenuGroups 屬性 Windows 功能區
topic_type:
- apiref
api_name:
- SplitButton.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bdc92ba966cab09d2f417fdedbc046d7ec400ea93bdb2d0434194ff1d1824d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119933178"
---
# <a name="splitbuttonmenugroups-property"></a>SplitButton. MenuGroups 屬性

表示標準 [分割按鈕](windowsribbon-controls-splitbutton.md) 控制項中一組下拉式功能表專案的容器。

## <a name="usage"></a>使用方式

``` syntax
<SplitButton.MenuGroups>
  child elements
</SplitButton.MenuGroups>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



| 元素                                                         | 描述                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/> | 至少必須發生一次<br/> <br/> |



## <a name="parent-elements"></a>父元素



| 元素                                                             |
|---------------------------------------------------------------------|
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/> |



## <a name="remarks"></a>備註

選擇性。

每個 [**SplitButton**](windowsribbon-element-splitbutton.md)最多可能會發生一次。

## <a name="examples"></a>範例

下列範例示範 [分割按鈕](windowsribbon-controls-splitbutton.md)的基本標記。

這段程式碼會顯示 [**SplitButton**](windowsribbon-element-splitbutton.md)和 **SplitButton MenuGroups** 命令宣告，以及可作為 **SplitButton** 元素父容器的相關聯 [**群組**](windowsribbon-element-group.md)。


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



這段程式碼會顯示 [**SplitButton**](windowsribbon-element-splitbutton.md) 和 **SplitButton MenuGroups** 控制項宣告。


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

 

 






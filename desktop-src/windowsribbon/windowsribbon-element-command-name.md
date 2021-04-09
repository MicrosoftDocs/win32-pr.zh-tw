---
title: Command.Name 屬性
description: 表示命令的名稱。
ms.assetid: 36fb0b93-143f-4706-8c32-e6c818cce16f
keywords:
- Command.Name 屬性視窗功能區
topic_type:
- apiref
api_name:
- Command.Name
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d93b830e29ca271052a4693b00ba64eee94309f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025390"
---
# <a name="commandname-property"></a>Command.Name 屬性

表示命令的名稱。

## <a name="usage"></a>使用方式

``` syntax
<Command.Name/>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素

沒有任何子項目。

## <a name="parent-elements"></a>父元素



| 元素                                                     |
|-------------------------------------------------------------|
| [**命令**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>備註

選擇性。

每個 [**命令**](windowsribbon-element-command.md)最多可能會發生一次。

標記中會參考 **Command.Name** ，以透過控制項的 *CommandName* 屬性將命令與控制項產生關聯。

這個元素包含 *xs： string* 類型的值。

此值受限於包含字母或底線的字串，後面接著字母、數位和底線的任何序列。

長度上限為100個字元。

## <a name="examples"></a>範例

下列範例示範具有 **Command.Name** 宣告之 [**Command**](windowsribbon-element-command.md)元素的標記。


```XML
<Command>
  <Command.Name>cmdSave</Command.Name>
  <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
  <Command.Comment>Save</Command.Comment>
  <Command.Id>25003</Command.Id>
  <Command.LabelTitle>
    <String>
      <String.Content>Label for Save</String.Content>
      <String.Id>59999</String.Id>
      <String.Symbol>strSave</String.Symbol>
    </String>
  </Command.LabelTitle>
  <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
  <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
  <Command.Keytip>s1</Command.Keytip>
</Command>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/> |



 

 






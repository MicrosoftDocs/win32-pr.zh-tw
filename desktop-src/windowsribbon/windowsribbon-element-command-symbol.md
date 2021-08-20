---
title: Command. Symbol 屬性
description: 代表可在外部參考的命令名稱。
ms.assetid: affa5f3f-f641-4bec-9165-6102509cf355
keywords:
- 命令符號屬性 Windows 功能區
topic_type:
- apiref
api_name:
- Command.Symbol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb0a391b56c5d44809735d32b9d3e3dfa47dc2b9f1ce686176fa077e99bf987c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117656483"
---
# <a name="commandsymbol-property"></a>Command. Symbol 屬性

代表可在外部參考的 [**命令**](windowsribbon-element-command.md) 名稱。

## <a name="usage"></a>使用方式

``` syntax
<Command.Symbol/>
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

符號會與功能區標頭檔中的命令定義相關聯，例如 `#define cmdSave 25003 /* Save */` 。

這個元素包含 *xs： string* 類型的值。

此值受限於包含字母或底線的字串，後面接著字母、數位和底線的任何序列。

長度上限為100個字元。

## <a name="examples"></a>範例

下列範例示範 [**命令**](windowsribbon-element-command.md) 專案的標記與 **命令符號** 宣告。


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
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/> |



 

 






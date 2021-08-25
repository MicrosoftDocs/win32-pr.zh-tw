---
title: Command.Id 屬性
description: 表示命令的唯一識別碼。
ms.assetid: 937ca9d6-6910-4133-9cfa-d7e3f895f876
keywords:
- Command.Id 屬性 Windows 功能區
topic_type:
- apiref
api_name:
- Command.Id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50c542cbf4103c6063a177990d454a45e5f937745720c7c0a7bc5c60c4c1047e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931610"
---
# <a name="commandid-property"></a>Command.Id 屬性

表示命令的唯一識別碼。

## <a name="usage"></a>使用方式

``` syntax
<Command.Id/>
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

此識別碼與功能區標頭檔中的命令定義相關聯，例如 `#define cmdSave 25003 /* Save */` 。

這個元素包含的值，是由類型 *xs： positiveInteger* 和 *xs： string* 的等位所限制為整數值，介於2和59999（含）之間，或0x2 與0xea5f （十六進位）（含）之間。

最大長度為10個字元，包括選擇性前置零。

## <a name="examples"></a>範例

下列範例示範具有 **Command.Id** 宣告之 [**Command**](windowsribbon-element-command.md)元素的標記。


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



 

 






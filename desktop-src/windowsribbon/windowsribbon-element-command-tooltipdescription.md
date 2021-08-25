---
title: TooltipDescription 屬性
description: 表示工具提示描述。
ms.assetid: 2d3ea497-2d96-4420-8fcf-39ac2c472bf1
keywords:
- TooltipDescription 屬性 Windows 功能區
topic_type:
- apiref
api_name:
- Command.TooltipDescription
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5dd356ae3bcfa5949e8469240330a3a09a11f01b5a919ed02f4eb55683fbc15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119933208"
---
# <a name="commandtooltipdescription-property"></a>TooltipDescription 屬性

表示工具提示描述。

## <a name="usage"></a>使用方式

``` syntax
<Command.TooltipDescription>
  child elements
</Command.TooltipDescription>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



| 元素                                                   | 描述                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [**字串**](windowsribbon-element-string.md)<br/> | 最多可能發生一次<br/> <br/> |



## <a name="parent-elements"></a>父元素



| 元素                                                     |
|-------------------------------------------------------------|
| [**命令**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>備註

選擇性。

每個 [**命令**](windowsribbon-element-command.md)最多可能會發生一次。

**TooltipDescription** 可以包含限制為任何字元序列之 *xs： string* 類型的值，包括空白字元和分行符號字元。

> [!Note]  
> 使用通用字元集 (UCS) XML 字元參考 `&#xA;` 來指定分行符號。

 

長度上限為未系結。

如果未提供 **TooltipDescription** 的值，則需要 [**字串**](windowsribbon-element-string.md) 子項目。

> [!Note]  
> 如果 **TooltipDescription** 同時包含值和 [**字串**](windowsribbon-element-string.md) 子項目，則會優先使用 **字串** 。

 

**TooltipDescription** 只支援靠左對齊。

## <a name="examples"></a>範例

下列範例示範 [**命令**](windowsribbon-element-command.md) 專案的標記，以及 **TooltipDescription** 宣告。


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



## <a name="see-also"></a>另請參閱

<dl> <dt>

[UI \_ PKEY \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md)
</dt> </dl>

 

 






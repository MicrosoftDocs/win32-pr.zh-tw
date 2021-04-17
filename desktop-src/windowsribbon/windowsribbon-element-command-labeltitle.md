---
title: LabelTitle 屬性
description: 表示標籤標題。
ms.assetid: 97378ec3-7988-4e39-9cf5-c382b246c5c9
keywords:
- LabelTitle 屬性 Windows 功能區
topic_type:
- apiref
api_name:
- Command.LabelTitle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed6d6c72ddd60cca63834fdcf21cf8f8b726ad22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509183"
---
# <a name="commandlabeltitle-property"></a>LabelTitle 屬性

表示標籤標題。

## <a name="usage"></a>使用方式

``` syntax
<Command.LabelTitle>
  child elements
</Command.LabelTitle>
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

**LabelTitle** 可以包含限制為任何字元序列之 *xs： string* 類型的值，包括空白字元和分行符號字元。

> [!Note]  
> 使用通用字元集 (UCS) XML 字元參考 `&#xA;` 來指定分行符號。

 

長度上限為未系結。

如果未提供 **LabelTitle** 的值，則需要 [**字串**](windowsribbon-element-string.md) 子項目。

> [!Note]  
> 如果 **LabelTitle** 同時包含值和 [**字串**](windowsribbon-element-string.md) 子項目，則會優先使用 **字串** 。

 

**LabelTitle** 只支援靠左對齊。

如果命令是透過功能表項目公開，而且 **LabelTitle** 或 [UI \_ PKEY \_ 標籤](windowsribbon-reference-properties-uipkey-label.md) 的值包含前面加上連字號的字母，如下列範例所示，則會將這個字母視為使用者介面的快速鍵，以及功能區架構的鍵盤對應鍵。


```XML
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
```



若要在標籤中顯示 & 符號，請將特殊字元指定換成雙符號 (`&&`) ，如下列範例所示。


```XML
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
```



## <a name="examples"></a>範例

下列範例示範 [**命令**](windowsribbon-element-command.md) 專案的標記，以及 **LabelTitle** 宣告。


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



## <a name="see-also"></a>另請參閱

<dl> <dt>

[UI \_ PKEY \_ 標籤](windowsribbon-reference-properties-uipkey-label.md)
</dt> </dl>

 

 






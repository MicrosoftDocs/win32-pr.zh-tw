---
title: Content 屬性
description: 表示字串資源的內容。
ms.assetid: 86f34cdc-1311-4f52-979f-201d71bbb9e9
keywords:
- 字串內容視窗功能區
topic_type:
- apiref
api_name:
- String.Content
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8912264e4f55568c190212227d2e305f9d676a1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969968"
---
# <a name="stringcontent-property"></a>Content 屬性

表示字串資源的內容。

## <a name="usage"></a>使用方式

``` syntax
<String.Content/>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素

沒有任何子項目。

## <a name="parent-elements"></a>父元素



| 元素                                                   |
|-----------------------------------------------------------|
| [**字串**](windowsribbon-element-string.md)<br/> |



## <a name="remarks"></a>備註

選擇性。

每個 [**字串**](windowsribbon-element-string.md) 元素最多可能會發生一次。

這個元素包含 *xs： string* 類型的值。 此值受限於由任何字元序列組成的字串，包括空白字元和分行符號字元。

長度上限為未系結。

## <a name="examples"></a>範例

下列範例示範 [**LabelTitle**](windowsribbon-element-command-labeltitle.md) 專案的標記，其中包含 **字串. 內容** 宣告。


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/> |



 

 






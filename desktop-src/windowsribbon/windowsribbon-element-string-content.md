---
title: Content 屬性
description: 表示字串資源的內容。
ms.assetid: 86f34cdc-1311-4f52-979f-201d71bbb9e9
keywords:
- Content 屬性 Windows 功能區
topic_type:
- apiref
api_name:
- String.Content
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 526062956c6ab7498caac8712ba932d6e7ac1f2dd6307359183d2529e35fc8a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118439503"
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
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/> |



 

 






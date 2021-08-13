---
title: String.Id 屬性
description: 表示字串資源的唯一識別碼。
ms.assetid: 393da279-bdf6-4796-a546-1931cbe49113
keywords:
- String.Id 屬性 Windows 功能區
topic_type:
- apiref
api_name:
- String.Id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15f9c1af4ba32982ce52ba470f6b3d1996abe11c81bdd520a4e50203adb56093
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119441648"
---
# <a name="stringid-property"></a>String.Id 屬性

表示字串資源的唯一識別碼。

## <a name="usage"></a>使用量

``` syntax
<String.Id/>
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

**String.Id** 的值必須是唯一的。

此識別碼與功能區標頭檔中的字串定義相關聯，例如 `#define strSave 59999` 。

這個元素包含類型 *xs： positiveInteger* 和 *xs： string* 等位的值。 值受限於介於2到59999（含）之間的整數值，或以十六進位（含）表示的0xea5f。

最大長度為10個字元，選擇性前置零。

## <a name="examples"></a>範例

下列範例示範具有 **String.Id** 宣告的 [**LabelTitle**](windowsribbon-element-command-labeltitle.md)元素標記。


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



 

 






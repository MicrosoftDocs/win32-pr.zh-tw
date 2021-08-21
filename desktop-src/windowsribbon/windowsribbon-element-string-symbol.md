---
title: String. Symbol 屬性
description: 表示字串資源的名稱。
ms.assetid: 7c1d0197-2c9b-4f42-afba-73fd1c366deb
keywords:
- 符號屬性 Windows 功能區
topic_type:
- apiref
api_name:
- String.Symbol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe6c071461fcdeb5f2bbbdbb15fce0f3f6e6031edddf4bd18e034416ba8c49e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118706859"
---
# <a name="stringsymbol-property"></a>String. Symbol 屬性

表示字串資源的名稱。

## <a name="usage"></a>使用方式

``` syntax
<String.Symbol/>
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

符號會與功能區標頭檔中的字串定義相關聯，例如 `#define strSave 59999` 。

這個元素包含 *xs： string* 類型的值。 此值受限於包含字母或底線的字串，後面接著字母、數位或底線的任何序列。

長度上限為100個字元。

## <a name="examples"></a>範例

下列範例會示範 [**LabelTitle**](windowsribbon-element-command-labeltitle.md) 元素的標記，並以 **字串符號** 宣告。


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



 

 






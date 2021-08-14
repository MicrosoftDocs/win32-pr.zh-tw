---
title: " (RPC) 的字串"
description: " (RPC) 的三種字串類型和遠端程序呼叫。"
ms.assetid: 186cabeb-ea3f-4213-ba71-53afe91e6e14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b15467ed5a1425443cbc5a53cf35aba71725c5db68c542c292af38eb0d238cfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924834"
---
# <a name="strings-rpc"></a> (RPC) 的字串

有三個字串類型以格式字元中的下列結束子字串表示。



| 類型                  | Substring |
|-----------------------|-----------|
| 字元字串      | CSTRING   |
| 寬字元字串 | WSTRING   |
| 可字串結構 | SSTRING   |



 

### <a name="nonconformant-strings"></a>Nonconformant 字串

Nonconformant 字串的範例是固定大小陣列上的 **\[ 字串 \]** 。

``` syntax
FC_CSTRING | FC _WSTRING 
FC_PAD 
string_size<2>
```

### <a name="conformant-strings"></a>符合標準的字串

``` syntax
FC_C_CSTRING | FC_C_WSTRING
FC_PAD 
```

–或–

``` syntax
FC_C_CSTRING | FC_C_WSTRING 
FC_STRING_SIZED 
conformance_description<> 
```

第一個格式描述一般字串，例如 **\[ 字串 \]** char \* 引數。 大小一致的字串具有後者的描述。

一致性 \_ 描述<> 是相互關聯描述項，而且有4或6個位元組，視是否使用 [**/robust**](/windows/desktop/Midl/-robust) 而定。

### <a name="structure-strings"></a>結構字串

以下是可 nonconformant 字串的結構：

``` syntax
FC_SSTRING 
element_size<1> 
number_of_elements<2>
```

符合字串能力的結構：

``` syntax
FC_C_SSTRING 
element_size<1>
```

等於

``` syntax
FC_C_SSTRING 
elements_size<1> 
FC_STRING_SIZED FC_PAD 
conformance_description<>
```

第二個描述適用于大小可進行字串的結構。

 

 
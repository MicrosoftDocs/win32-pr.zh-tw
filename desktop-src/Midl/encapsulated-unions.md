---
title: 封裝聯集
description: 內的結構中包含其判別的聯集是封裝聯集。
ms.assetid: d32c18b4-b2f6-4ce2-94fe-a495a3c15d14
keywords:
- 資料類型 MIDL、封裝聯集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4489a043ff3690ddb31a8acccf359dcd76940aa7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965394"
---
# <a name="encapsulated-unions"></a>封裝聯集

內的結構中包含其判別的聯集是封裝聯集。 封裝聯集是由 [**switch**](switch.md) 關鍵字的存在所表示。 這種類型的等位是因為 MIDL 編譯器會自動將等位和其判別封裝在遠端程序呼叫期間進行傳輸的結構中。

如果上述範例中遺漏了 union 標記 (U1 \_ 型別) ，則編譯器會產生具有加上卷 *標聯 \_ 集* 之聯集欄位的結構。

等位的形狀在各平臺之間必須相同，以確保互連能力。

如需封裝聯集之格式的描述，請參閱聯 [**集**](union.md)。

## <a name="examples"></a>範例

``` syntax
typedef union _S1_TYPE switch (long l1) U1_TYPE 
{ 
    case 1024: 
        float f1; 
    case 2048: 
        double d2; 
} S1_TYPE; 
 
/* in generated header file */ 
typedef struct _S1_TYPE 
{ 
    long l1; 
    union 
    { 
        float f1; 
        double d2; 
    } U1_TYPE; 
} S1_TYPE;
```

如需相關資訊，請參閱 [MIDL 基底類型](midl-base-types.md)、 [**char**](char-idl.md)、 **\[** [**coNtext \_ handle**](context-handle.md) **\]** 、 [**enum**](enum.md)、 **\[** [**\_ first**](first-is.md) **\]** 、 **\[** [**handle**](handle.md) **\]** 、 **\[** [**ignore**](ignore.md) **\]** 、 [**int**](int.md)、 **\[** [**ignore**](ignore.md) **\]** 、 **\[** [**last \_**](last-is.md) **\]** 、 **\[** [**length、length \_**](length-is.md)、 **\]** **\[** [**max \_**](max-is.md)、 **\]** **\[** [**ms \_ union**](ms-union-attrib.md) **\]** 、 [Nonencapsulated](nonencapsulated-unions.md)等位、 **\[** [**ptr**](ptr.md) **\]** 、 **\[** [**ref**](ref.md)、 **\]** **\[** [**\_**](size-is.md) **\]** **\[** switch as、 [**string**](string.md) **\]** 、 [**struct**](struct.md)、 [**switch**](switch.md)、switch、switch **\[** [**\_**](switch-is.md) **\]** **\[** [**\_ type**](switch-type.md) **\]** 、 **\[** [**傳輸 \_ as**](transmit-as.md) **\]** 、 [**union**](union.md)和 **\[** [**unique**](unique.md)**\]**

 

 





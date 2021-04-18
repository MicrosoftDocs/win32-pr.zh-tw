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
# <a name="encapsulated-unions"></a><span data-ttu-id="b8744-104">封裝聯集</span><span class="sxs-lookup"><span data-stu-id="b8744-104">Encapsulated Unions</span></span>

<span data-ttu-id="b8744-105">內的結構中包含其判別的聯集是封裝聯集。</span><span class="sxs-lookup"><span data-stu-id="b8744-105">A union that is contained with its discriminant in a structure within is an encapsulated union.</span></span> <span data-ttu-id="b8744-106">封裝聯集是由 [**switch**](switch.md) 關鍵字的存在所表示。</span><span class="sxs-lookup"><span data-stu-id="b8744-106">The encapsulated union is indicated by the presence of the [**switch**](switch.md) keyword.</span></span> <span data-ttu-id="b8744-107">這種類型的等位是因為 MIDL 編譯器會自動將等位和其判別封裝在遠端程序呼叫期間進行傳輸的結構中。</span><span class="sxs-lookup"><span data-stu-id="b8744-107">This type of union is so named because the MIDL compiler automatically encapsulates the union and its discriminant in a structure for transmission during a remote procedure call.</span></span>

<span data-ttu-id="b8744-108">如果上述範例中遺漏了 union 標記 (U1 \_ 型別) ，則編譯器會產生具有加上卷 *標聯 \_ 集* 之聯集欄位的結構。</span><span class="sxs-lookup"><span data-stu-id="b8744-108">If the union tag is missing (U1\_TYPE in the example above), the compiler will generate the structure with the union field named *tagged\_union*.</span></span>

<span data-ttu-id="b8744-109">等位的形狀在各平臺之間必須相同，以確保互連能力。</span><span class="sxs-lookup"><span data-stu-id="b8744-109">The shape of unions must be the same across platforms to ensure interconnectivity.</span></span>

<span data-ttu-id="b8744-110">如需封裝聯集之格式的描述，請參閱聯 [**集**](union.md)。</span><span class="sxs-lookup"><span data-stu-id="b8744-110">For a description of the form of an encapsulated union, see [**union**](union.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b8744-111">範例</span><span class="sxs-lookup"><span data-stu-id="b8744-111">Examples</span></span>

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

<span data-ttu-id="b8744-112">如需相關資訊，請參閱 [MIDL 基底類型](midl-base-types.md)、 [**char**](char-idl.md)、 **\[** [**coNtext \_ handle**](context-handle.md) **\]** 、 [**enum**](enum.md)、 **\[** [**\_ first**](first-is.md) **\]** 、 **\[** [**handle**](handle.md) **\]** 、 **\[** [**ignore**](ignore.md) **\]** 、 [**int**](int.md)、 **\[** [**ignore**](ignore.md) **\]** 、 **\[** [**last \_**](last-is.md) **\]** 、 **\[** [**length、length \_**](length-is.md)、 **\]** **\[** [**max \_**](max-is.md)、 **\]** **\[** [**ms \_ union**](ms-union-attrib.md) **\]** 、 [Nonencapsulated](nonencapsulated-unions.md)等位、 **\[** [**ptr**](ptr.md) **\]** 、 **\[** [**ref**](ref.md)、 **\]** **\[** [**\_**](size-is.md) **\]** **\[** switch as、 [**string**](string.md) **\]** 、 [**struct**](struct.md)、 [**switch**](switch.md)、switch、switch **\[** [**\_**](switch-is.md) **\]** **\[** [**\_ type**](switch-type.md) **\]** 、 **\[** [**傳輸 \_ as**](transmit-as.md) **\]** 、 [**union**](union.md)和 **\[** [**unique**](unique.md)**\]**</span><span class="sxs-lookup"><span data-stu-id="b8744-112">For related information, see [MIDL Base Types](midl-base-types.md), [**char**](char-idl.md), **\[**[**context\_handle**](context-handle.md)**\]**, [**enum**](enum.md), **\[**[**first\_is**](first-is.md)**\]**, **\[**[**handle**](handle.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, [**int**](int.md), **\[**[**ignore**](ignore.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**ms\_union**](ms-union-attrib.md)**\]**, [Nonencapsulated Unions](nonencapsulated-unions.md), **\[**[**ptr**](ptr.md)**\]**, **\[**[**ref**](ref.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**, **\[**[**string**](string.md)**\]**, [**struct**](struct.md), [**switch**](switch.md), **\[**[**switch\_is**](switch-is.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**, [**union**](union.md), and **\[**[**unique**](unique.md)**\]**</span></span>

 

 





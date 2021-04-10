---
description: 查詢包含内嵌物件的事件類別時，您有幾個選項可供查詢所用的表單使用。 查詢所傳回的結果會根據您所使用的查詢格式而有所不同。
ms.assetid: b959a695-be15-4aa7-9368-b840962ae0da
ms.tgt_platform: multiple
title: 查詢内嵌物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed2e13bd9d9dc798891a723a6fed1b1734e1735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692204"
---
# <a name="querying-embedded-objects"></a><span data-ttu-id="9c83f-104">查詢内嵌物件</span><span class="sxs-lookup"><span data-stu-id="9c83f-104">Querying Embedded Objects</span></span>

<span data-ttu-id="9c83f-105">查詢包含内嵌物件的事件類別時，您有幾個選項可供查詢所用的表單使用。</span><span class="sxs-lookup"><span data-stu-id="9c83f-105">You have several options as to the form a query takes when querying an event class that contains embedded objects.</span></span> <span data-ttu-id="9c83f-106">查詢所傳回的結果會根據您所使用的查詢格式而有所不同。</span><span class="sxs-lookup"><span data-stu-id="9c83f-106">The results returned by the query vary, depending on the form of the query you use.</span></span>

## <a name="class-definitions"></a><span data-ttu-id="9c83f-107">類別定義</span><span class="sxs-lookup"><span data-stu-id="9c83f-107">Class Definitions</span></span>

<span data-ttu-id="9c83f-108">下列範例顯示在本主題中用於 WQL 查詢的類別定義。</span><span class="sxs-lookup"><span data-stu-id="9c83f-108">The following example shows the class definitions that are used for the WQL queries in this topic.</span></span>

``` syntax
class MyClass
{
   string Prop1;
   string Prop2;
};

class MyEvent : __ExtrinsicEvent
{
   MyClass E1;
   MyClass E2;
};
```

## <a name="examples"></a><span data-ttu-id="9c83f-109">範例</span><span class="sxs-lookup"><span data-stu-id="9c83f-109">Examples</span></span>

<span data-ttu-id="9c83f-110">下列查詢會傳回內嵌式類別（ **E1** 和 **E2**），每個都有 **Prop1** 和 **this.prop2** 填入資料。</span><span class="sxs-lookup"><span data-stu-id="9c83f-110">The following query returns both embedded classes, **E1** and **E2**, each having **Prop1** and **Prop2** populated with data.</span></span>

`SELECT * FROM MyEvent`

<span data-ttu-id="9c83f-111">下列查詢會傳回 **E1** embedded 物件，但 **Prop1** 和 **this.prop2** 都不會填入資料。</span><span class="sxs-lookup"><span data-stu-id="9c83f-111">The following query returns the **E1** embedded object, but with neither **Prop1** nor **Prop2** populated with data.</span></span>

`SELECT E1 FROM MyEvent`

<span data-ttu-id="9c83f-112">下列查詢會傳回內嵌類別 **E1** ，其中只包含填入資料的 **Prop1** 。</span><span class="sxs-lookup"><span data-stu-id="9c83f-112">The following query returns the embedded class **E1** with only **Prop1** populated with data.</span></span>

`SELECT E1.Prop1 FROM MyEvent`

<span data-ttu-id="9c83f-113">下列查詢會傳回內嵌式類別（ **E1** 和 **E2**），每個都有 **Prop1** 和 **this.prop2** 填入資料。</span><span class="sxs-lookup"><span data-stu-id="9c83f-113">The following query returns both embedded classes, **E1** and **E2**, each having **Prop1** and **Prop2** populated with data.</span></span>

`ELECT E1.Prop1, E1.Prop2, E2.Prop1, E2.Prop2 FROM MyEvent`

<span data-ttu-id="9c83f-114">這相當於使用星號 () 的第一個查詢， \* 而不是指定每個物件和屬性。</span><span class="sxs-lookup"><span data-stu-id="9c83f-114">This is equivalent to the first query using the asterisk (\*) instead of specifying each object and property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c83f-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="9c83f-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c83f-116">使用 WQL 查詢</span><span class="sxs-lookup"><span data-stu-id="9c83f-116">Querying with WQL</span></span>](querying-with-wql.md)
</dt> </dl>

 

 




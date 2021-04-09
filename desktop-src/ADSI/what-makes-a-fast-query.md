---
title: 什麼可進行快速查詢
description: 本主題列出查詢目錄時要使用的慣用程式設計方法。
ms.assetid: d96f330f-3c57-4edc-9fd2-970f908b54c2
ms.tgt_platform: multiple
keywords:
- 什麼是讓 Fast Query ADSI
- 查詢 ADSI，如何進行快速查詢
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 883db1e9de7b7b7a1179c814d6f66f774685083e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842731"
---
# <a name="what-makes-a-fast-query"></a><span data-ttu-id="5bcb7-105">什麼是快速查詢？</span><span class="sxs-lookup"><span data-stu-id="5bcb7-105">What Makes a Fast Query?</span></span>

<span data-ttu-id="5bcb7-106">執行查詢時，請考慮下列效能增強概念：</span><span class="sxs-lookup"><span data-stu-id="5bcb7-106">Consider the following performance enhancement concepts when executing a query:</span></span>

-   <span data-ttu-id="5bcb7-107">可能的話，請只篩選索引屬性。</span><span class="sxs-lookup"><span data-stu-id="5bcb7-107">If possible, filter on indexed attributes only.</span></span> <span data-ttu-id="5bcb7-108">使用您預期會產生最少點擊次數的索引屬性。</span><span class="sxs-lookup"><span data-stu-id="5bcb7-108">Use index attributes that you expect will generate the fewest number of hits.</span></span> <span data-ttu-id="5bcb7-109">如需詳細資訊和 Windows 索引屬性的完整清單，請參閱 [Active Directory 架構](/windows/desktop/ADSchema/active-directory-schema)。</span><span class="sxs-lookup"><span data-stu-id="5bcb7-109">For more information and a comprehensive list of indexed attributes for Windows, see [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema).</span></span>
-   <span data-ttu-id="5bcb7-110">搜尋 **objectCategory** 而非 **Objectclass** ，因為 **objectClass** 不是索引屬性。</span><span class="sxs-lookup"><span data-stu-id="5bcb7-110">Search on **objectCategory** instead of **objectClass** because **objectClass** is not an indexed property.</span></span>
-   <span data-ttu-id="5bcb7-111">請留意參考。</span><span class="sxs-lookup"><span data-stu-id="5bcb7-111">Be aware of referrals.</span></span> <span data-ttu-id="5bcb7-112">如果您的屬性列為 GC 已複寫，請考慮搜尋通用類別目錄。</span><span class="sxs-lookup"><span data-stu-id="5bcb7-112">Consider searching the global catalog if your attributes are listed as GC replicated.</span></span>
-   <span data-ttu-id="5bcb7-113">避免搜尋字串中間和結尾的文字。</span><span class="sxs-lookup"><span data-stu-id="5bcb7-113">Avoid searching for text in the middle and at the end of a string.</span></span> <span data-ttu-id="5bcb7-114">例如，"cn = \* hille \* " 或 "cn = \* larouse"。</span><span class="sxs-lookup"><span data-stu-id="5bcb7-114">For example, "cn=\*hille\*" or "cn=\*larouse".</span></span>
-   <span data-ttu-id="5bcb7-115">假設子樹搜尋將傳回大型結果集。</span><span class="sxs-lookup"><span data-stu-id="5bcb7-115">Assume that a subtree search will return a large result set.</span></span> <span data-ttu-id="5bcb7-116">執行子樹搜尋時，請使用分頁。</span><span class="sxs-lookup"><span data-stu-id="5bcb7-116">Use paging when performing subtree searches.</span></span> <span data-ttu-id="5bcb7-117">如此一來，伺服器就能夠以區塊來串流大型結果集，以減少伺服器端記憶體資源。</span><span class="sxs-lookup"><span data-stu-id="5bcb7-117">The server will then be able to stream a large result set in chunks reducing the server-side memory resources.</span></span> <span data-ttu-id="5bcb7-118">這可有效地將網路使用量壓平合併，並減少透過網路傳送極大區塊資料的需求。</span><span class="sxs-lookup"><span data-stu-id="5bcb7-118">This effectively flattens out network usage and reduces the need for sending extremely large chunks of data over the network.</span></span>
-   <span data-ttu-id="5bcb7-119">適當地界定搜尋範圍，如此就不需要取得超過的範圍。</span><span class="sxs-lookup"><span data-stu-id="5bcb7-119">Properly scope your searches so as to not retrieve more than is necessary.</span></span>
-   <span data-ttu-id="5bcb7-120">對多個屬性執行複雜的搜尋，因為它比執行多個搜尋的效能低。</span><span class="sxs-lookup"><span data-stu-id="5bcb7-120">Perform a complex search on multiple attributes, because it is less performance intensive than performing multiple searches.</span></span> <span data-ttu-id="5bcb7-121">針對讀取兩個屬性的物件進行一項搜尋，會比對相同物件的兩個搜尋更有效率，每個都傳回一個屬性。</span><span class="sxs-lookup"><span data-stu-id="5bcb7-121">One search for an object that reads two attributes is more efficient than two searches for the same object, each returning one attribute.</span></span>
-   <span data-ttu-id="5bcb7-122">若要讀取具有大量值的屬性，請使用範圍限制將搜尋大小降到最低，讓您一次可以讀取數千個成員。</span><span class="sxs-lookup"><span data-stu-id="5bcb7-122">For reading attribute with a large number of values, use range limits to minimize the search size so that you can read a few thousand members at a time.</span></span> <span data-ttu-id="5bcb7-123">如需有關指定屬性範圍限制的詳細資訊，請參閱 [屬性範圍](attribute-range-retrieval.md)抓取。</span><span class="sxs-lookup"><span data-stu-id="5bcb7-123">For more information about specifying attribute range limits, see [Attribute Range Retrieval](attribute-range-retrieval.md).</span></span>
-   <span data-ttu-id="5bcb7-124">系結至物件，以保存會話其餘部分的系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="5bcb7-124">Bind to an object hold the binding handle for the remainder of your session.</span></span> <span data-ttu-id="5bcb7-125">請勿系結和解除系結每個呼叫。</span><span class="sxs-lookup"><span data-stu-id="5bcb7-125">Do not bind and unbind for each call.</span></span> <span data-ttu-id="5bcb7-126">如果您使用的是 ADO 或 OLE DB，請勿建立許多連線物件。</span><span class="sxs-lookup"><span data-stu-id="5bcb7-126">If you are using ADO or OLE DB, do not create many connection objects.</span></span>
-   <span data-ttu-id="5bcb7-127">讀取 rootDSE 一次，並記住其內容以供會話的其餘部分之用。</span><span class="sxs-lookup"><span data-stu-id="5bcb7-127">Read the rootDSE once and remember its contents for the remainder of your session.</span></span>

 

 
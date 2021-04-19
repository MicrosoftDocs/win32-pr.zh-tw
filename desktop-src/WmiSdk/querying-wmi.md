---
description: Windows Management Instrumentation (WMI) 的主要工具之一，就是能夠查詢 WMI 存放庫中的類別和實例資訊。
ms.assetid: 0cceda42-fba0-4a08-90dd-43f022d0be41
ms.tgt_platform: multiple
title: 查詢 WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdae44d4c40e1127bfc4d3436d6230eafd52146a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985629"
---
# <a name="querying-wmi"></a><span data-ttu-id="b5498-103">查詢 WMI</span><span class="sxs-lookup"><span data-stu-id="b5498-103">Querying WMI</span></span>

<span data-ttu-id="b5498-104">Windows Management Instrumentation (WMI) 的主要工具之一，就是能夠查詢 WMI 存放庫中的類別和實例資訊。</span><span class="sxs-lookup"><span data-stu-id="b5498-104">One of the main tools of Windows Management Instrumentation (WMI) is the ability to query the WMI repository for class and instance information.</span></span> <span data-ttu-id="b5498-105">例如，您可以要求 WMI 傳回代表桌面系統關機事件的所有物件。</span><span class="sxs-lookup"><span data-stu-id="b5498-105">For example, you can request that WMI return all the objects representing shut-down events from your desktop system.</span></span> <span data-ttu-id="b5498-106">您也可以取出類別、實例或架構資料。</span><span class="sxs-lookup"><span data-stu-id="b5498-106">You can also retrieve class, instance, or schema data.</span></span> <span data-ttu-id="b5498-107">下表列出您可以進行的不同查詢類型。</span><span class="sxs-lookup"><span data-stu-id="b5498-107">The following table lists the different types of queries you can make.</span></span>



| <span data-ttu-id="b5498-108">主題</span><span class="sxs-lookup"><span data-stu-id="b5498-108">Topic</span></span>                                                                | <span data-ttu-id="b5498-109">描述</span><span class="sxs-lookup"><span data-stu-id="b5498-109">Description</span></span>                                                                                                                                                                                      |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b5498-110">叫用同步查詢</span><span class="sxs-lookup"><span data-stu-id="b5498-110">Invoking a Synchronous Query</span></span>](invoking-a-synchronous-query.md)     | <span data-ttu-id="b5498-111">描述如何在整個查詢過程中維護 WMI 的連結。</span><span class="sxs-lookup"><span data-stu-id="b5498-111">Describes how to maintain a link with WMI throughout the query process.</span></span> <span data-ttu-id="b5498-112">同步查詢適用于對本機系統進行小型查詢或查詢。</span><span class="sxs-lookup"><span data-stu-id="b5498-112">Synchronous queries are good for small queries or queries to a local system.</span></span><br/>                                  |
| [<span data-ttu-id="b5498-113">叫用非同步查詢</span><span class="sxs-lookup"><span data-stu-id="b5498-113">Invoking an Asynchronous Query</span></span>](invoking-an-asynchronous-query.md) | <span data-ttu-id="b5498-114">說明如何設定個別的進程來接收查詢。</span><span class="sxs-lookup"><span data-stu-id="b5498-114">Describes how to set up a separate process to receive queries.</span></span> <span data-ttu-id="b5498-115">非同步查詢比較複雜，並提供較低層級的安全性，但通常可改善系統效能。</span><span class="sxs-lookup"><span data-stu-id="b5498-115">Asynchronous queries are more complex and provide a lower level of security, but generally improve system performance.</span></span><br/> |



 

<span data-ttu-id="b5498-116">除了查詢 WMI 儲存機制，您也可以使用 [*WMI 查詢語言 (WQL)*](gloss-w.md) 將通知事件路由傳送至您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="b5498-116">In addition to querying the WMI repository, you can also use the [*WMI Query Language (WQL)*](gloss-w.md) to route notification events to your application.</span></span> <span data-ttu-id="b5498-117">如需詳細資訊，請參閱 [接收 WMI 事件](receiving-a-wmi-event.md)。</span><span class="sxs-lookup"><span data-stu-id="b5498-117">For more information, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

> [!Note]
>
> <span data-ttu-id="b5498-118">若要適當地查詢 WMI，您必須對 WQL 有充分的瞭解。</span><span class="sxs-lookup"><span data-stu-id="b5498-118">To properly query WMI, you must have a good understanding of WQL.</span></span> <span data-ttu-id="b5498-119">不正確、太複雜或不當的查詢可能會導致查詢處理器傳回錯誤或非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="b5498-119">A query that is incorrect, too complex, or inappropriate can cause the query processor to return an error or unexpected results.</span></span> <span data-ttu-id="b5498-120">如需 WQL 的完整指南，請參閱 [使用 Wql 查詢](querying-with-wql.md)。</span><span class="sxs-lookup"><span data-stu-id="b5498-120">For a comprehensive guide to WQL, see [Querying with WQL](querying-with-wql.md).</span></span>
>
> <span data-ttu-id="b5498-121">WQL 查詢中可使用的 **和** 和 **或** 關鍵字數目有一些限制。</span><span class="sxs-lookup"><span data-stu-id="b5498-121">There are limits to the number of **AND** and **OR** keywords that can be used in WQL queries.</span></span> <span data-ttu-id="b5498-122">複雜查詢中使用的大量 WQL 關鍵字可能會導致 WMI 將 **WBEM \_ E \_ 配額 \_ 違規** 錯誤碼傳回為 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="b5498-122">Large numbers of WQL keywords used in a complex query can cause WMI to return the **WBEM\_E\_QUOTA\_VIOLATION** error code as an **HRESULT** value.</span></span> <span data-ttu-id="b5498-123">WQL 關鍵字的限制取決於查詢的複雜程度。</span><span class="sxs-lookup"><span data-stu-id="b5498-123">The limit of WQL keywords depends on how complex the query is.</span></span>
>
> <span data-ttu-id="b5498-124">使用指令碼語言（例如 VBScript）查詢具有 **uint64** 或 **sint64** 資料類型的屬性值時，WMI 會傳回字串值。</span><span class="sxs-lookup"><span data-stu-id="b5498-124">When querying for property values with a **uint64** or **sint64** data type in a scripting language like VBScript, WMI returns string values.</span></span> <span data-ttu-id="b5498-125">比較這些值時，可能會發生非預期的結果，因為比較字串會傳回與比較數位不同的結果。</span><span class="sxs-lookup"><span data-stu-id="b5498-125">Unexpected results can occur when comparing these values, because comparing strings returns different results than comparing numbers.</span></span> <span data-ttu-id="b5498-126">例如，比較字串時，"10000000000" 小於 "9"，而在比較數位時，則為9小於10000000000。</span><span class="sxs-lookup"><span data-stu-id="b5498-126">For example, "10000000000" is less than "9" when comparing strings, and 9 is less than 10000000000 when comparing numbers.</span></span> <span data-ttu-id="b5498-127">為了避免混淆，當從 WMI 抓取類型 **uint64** 或 **sint64** 的屬性時，您應該使用 VBScript 中的 [CDbl](/previous-versions//ftekwwt0(v=vs.85))方法。</span><span class="sxs-lookup"><span data-stu-id="b5498-127">To avoid confusion you should use the [CDbl](/previous-versions//ftekwwt0(v=vs.85)) method in VBScript when properties of type **uint64** or **sint64** are retrieved from WMI.</span></span>

 

> [!Note]  

 

<span data-ttu-id="b5498-128">如需詳細資訊，請參閱 [操作類別和實例資訊](manipulating-class-and-instance-information.md)。</span><span class="sxs-lookup"><span data-stu-id="b5498-128">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

 


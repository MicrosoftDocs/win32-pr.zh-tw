---
title: '排序 (ADSI) '
description: 用戶端可以要求伺服器來排序結果集。
ms.assetid: 795d27f0-0bfa-417e-aa1f-f2471f92dc45
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4ee790a646367366afe33639abd8f5aa57ed4f
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/11/2019
ms.locfileid: "106968881"
---
# <a name="sorting-adsi"></a><span data-ttu-id="894a9-103">排序 (ADSI) </span><span class="sxs-lookup"><span data-stu-id="894a9-103">Sorting (ADSI)</span></span>

<span data-ttu-id="894a9-104">用戶端可以要求伺服器來排序結果集。</span><span class="sxs-lookup"><span data-stu-id="894a9-104">A client can request a server to sort the result set.</span></span> <span data-ttu-id="894a9-105">您可以指定：</span><span class="sxs-lookup"><span data-stu-id="894a9-105">You can specify:</span></span>

-   <span data-ttu-id="894a9-106">排序次序：可以指定遞增或遞減排序次序。</span><span class="sxs-lookup"><span data-stu-id="894a9-106">Sort order: Either ascending or descending sort order can be specified.</span></span>
-   <span data-ttu-id="894a9-107">排序屬性：您可以在排序字串中指定多個屬性。</span><span class="sxs-lookup"><span data-stu-id="894a9-107">Sort attributes: Multiple attributes can be specified in a sort string.</span></span> <span data-ttu-id="894a9-108">例如，依姓氏、名字和名字排序。</span><span class="sxs-lookup"><span data-stu-id="894a9-108">For example, sort by Last Name, then First Name.</span></span>

<span data-ttu-id="894a9-109">當您指定排序次序時，您應該嘗試使用其中一個索引屬性。</span><span class="sxs-lookup"><span data-stu-id="894a9-109">When you specify sort order, you should try to use one of the indexed attributes.</span></span> <span data-ttu-id="894a9-110">否則，伺服器必須先計算完整的結果集，才能將它傳送至用戶端。</span><span class="sxs-lookup"><span data-stu-id="894a9-110">Otherwise, the server must calculate a complete result set before sending it to the client.</span></span> <span data-ttu-id="894a9-111">即使您已要求分頁搜尋並指定頁面大小，也是如此。</span><span class="sxs-lookup"><span data-stu-id="894a9-111">This is true even if you have requested a paged search and specified a page size.</span></span>

> [!Note]  
> <span data-ttu-id="894a9-112">並非所有目錄伺服器都支援多個屬性排序或排序次序。</span><span class="sxs-lookup"><span data-stu-id="894a9-112">Not all directory servers support multiple attribute sorts or sort order.</span></span>

 

 

 





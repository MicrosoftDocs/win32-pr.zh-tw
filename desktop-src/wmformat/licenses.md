---
title: 授權
description: 授權
ms.assetid: 74717519-bfd5-4a64-88eb-680d4bdfe74a
keywords:
- 'Windows Media 格式 SDK、數位版權管理 (DRM) '
- Windows Media Format SDK，DRM 授權
- Windows Media Format SDK，DRM 的授權
- 數位版權管理 (DRM) 、授權
- DRM (數位版權管理) 、授權
- 數位版權管理 (DRM) 、受保護的檔案授權
- DRM (數位版權管理) 、受保護的檔案授權
- 授權，DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0fbf2d7c0a25b2b19241d90743f43f46a71d7e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311259"
---
# <a name="licenses"></a><span data-ttu-id="dd543-111">授權</span><span class="sxs-lookup"><span data-stu-id="dd543-111">Licenses</span></span>

<span data-ttu-id="dd543-112">授權是一組資料，其描述可讀取受保護檔案中資料的條件。</span><span class="sxs-lookup"><span data-stu-id="dd543-112">A license is a set of data that describes the conditions under which data in protected files can be read.</span></span> <span data-ttu-id="dd543-113">每個授權都會套用至金鑰識別碼，通常會指派給單一媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="dd543-113">Each license applies to a key identifier, which is typically assigned to a single media file.</span></span> <span data-ttu-id="dd543-114">此識別碼是用來識別授權中受保護內容的識別碼。</span><span class="sxs-lookup"><span data-stu-id="dd543-114">This identifier is what is used to identify the protected content in the license.</span></span>

<span data-ttu-id="dd543-115">每個授權都會指定一或多個可以使用受保護內容執行的動作。</span><span class="sxs-lookup"><span data-stu-id="dd543-115">Each license specifies one or more actions that can be performed with the protected content.</span></span> <span data-ttu-id="dd543-116">這些動作也稱為許可權，可透過許多方式來限制。</span><span class="sxs-lookup"><span data-stu-id="dd543-116">These actions, also called rights, can be limited in a number of ways.</span></span> <span data-ttu-id="dd543-117">藉由合併開始日期、結束日期、計數和時間限制，授權簽發者可以在右方建立幾乎任何想像得到限制。</span><span class="sxs-lookup"><span data-stu-id="dd543-117">By combining start dates, end dates, counts, and time limits, the license issuer can create almost any imaginable limitation on a right.</span></span>

<span data-ttu-id="dd543-118">授權是由 Web 服務所發出。</span><span class="sxs-lookup"><span data-stu-id="dd543-118">Licenses are issued by a Web service.</span></span> <span data-ttu-id="dd543-119">取得授權時，它會儲存在用戶端電腦上的本機授權存放區中，該電腦是包含授權和其他 DRM 資料的受保護檔案。</span><span class="sxs-lookup"><span data-stu-id="dd543-119">When a license is acquired, it is stored on the client computer in the local license store, which is a protected file that contains licenses and other DRM data.</span></span> <span data-ttu-id="dd543-120">當應用程式存取受保護的內容時，DRM 子系統會在本機授權存放區中搜尋授與適當許可權的授權。</span><span class="sxs-lookup"><span data-stu-id="dd543-120">When protected content is accessed by an application, the DRM subsystem searches the local license store for a license that grants the appropriate right.</span></span> <span data-ttu-id="dd543-121">如果找不到授權，則應用程式可以根據儲存在檔案 DRM 標頭中的資訊取得一個授權。</span><span class="sxs-lookup"><span data-stu-id="dd543-121">If no license is found, the application can acquire one based on information stored in the DRM header of the file.</span></span>

<span data-ttu-id="dd543-122">可以針對相同的受保護檔案發出多個授權。</span><span class="sxs-lookup"><span data-stu-id="dd543-122">Multiple licenses can be issued for the same protected file.</span></span> <span data-ttu-id="dd543-123">當 DRM 子系統決定是否允許某項動作時，它會從所有套用的授權匯總許可權。</span><span class="sxs-lookup"><span data-stu-id="dd543-123">When the DRM subsystem determines whether an action is allowed, it aggregates the rights from all licenses that apply.</span></span> <span data-ttu-id="dd543-124">每個授權都可以指派優先順序。</span><span class="sxs-lookup"><span data-stu-id="dd543-124">Each license can be assigned a priority.</span></span> <span data-ttu-id="dd543-125">如果某個動作套用了一個以上的授權，則會檢查最高優先順序的授權，以判斷是否需要減少計數。</span><span class="sxs-lookup"><span data-stu-id="dd543-125">If more than one license applies to an action, the highest priority license is checked to determine whether counts need to be decremented.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd543-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="dd543-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd543-127">**概念**</span><span class="sxs-lookup"><span data-stu-id="dd543-127">**Concepts**</span></span>](drmconcepts.md)
</dt> </dl>

 

 





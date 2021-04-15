---
title: 本機授權商店
description: 本機授權商店
ms.assetid: f50e4535-1d4d-4486-8308-c3314b1f5414
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
ms.openlocfilehash: 56d28703a0387d8676c4c8d5bf08f9e27a3ecf5f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372620"
---
# <a name="local-license-store"></a><span data-ttu-id="be914-111">本機授權商店</span><span class="sxs-lookup"><span data-stu-id="be914-111">Local License Store</span></span>

<span data-ttu-id="be914-112">當 DRM 授權傳遞至用戶端電腦時，會將它放入本機授權存放區。</span><span class="sxs-lookup"><span data-stu-id="be914-112">When a DRM license is delivered to the client computer it is put into the local license store.</span></span> <span data-ttu-id="be914-113">這是硬碟上受保護的檔案，其中包含對使用者發出的所有授權，以及其他 DRM 資訊。</span><span class="sxs-lookup"><span data-stu-id="be914-113">This is a protected file on the hard disk that contains all the licenses issued to the user along with other DRM information.</span></span>

<span data-ttu-id="be914-114">您可以使用 Windows Media DRM 用戶端擴充 Api，以幾個有限的方式操作本機授權存放區中的資料。</span><span class="sxs-lookup"><span data-stu-id="be914-114">You can manipulate data in the local license store in a few, limited ways by using the Windows Media DRM Client Extended APIs.</span></span>

<span data-ttu-id="be914-115">除了本機授權存放區之外，某些物件也會使用暫時的授權存放。</span><span class="sxs-lookup"><span data-stu-id="be914-115">In addition to the local license store, some objects make use of a temporary license store.</span></span> <span data-ttu-id="be914-116">暫時存放區中的授權只會在短時間記憶體在。</span><span class="sxs-lookup"><span data-stu-id="be914-116">A license in a temporary store exists only for a short period of time.</span></span> <span data-ttu-id="be914-117">不過，某些在暫存存放區中開始的授權可以儲存到一般本機授權存放區。</span><span class="sxs-lookup"><span data-stu-id="be914-117">However, some licenses that begin in a temporary store can be saved to the regular local license store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="be914-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="be914-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be914-119">**概念**</span><span class="sxs-lookup"><span data-stu-id="be914-119">**Concepts**</span></span>](drmconcepts.md)
</dt> </dl>

 

 





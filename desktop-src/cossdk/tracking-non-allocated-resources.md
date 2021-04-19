---
description: 追蹤未配置的資源
ms.assetid: ebaca876-5249-4b6b-b0d5-08f098e3f5f5
title: 追蹤未配置的資源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9c9f814e08798b4fbb0f160e0d0e0f8aabebba7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106984153"
---
# <a name="tracking-non-allocated-resources"></a><span data-ttu-id="10d9e-103">追蹤未配置的資源</span><span class="sxs-lookup"><span data-stu-id="10d9e-103">Tracking Non-Allocated Resources</span></span>

<span data-ttu-id="10d9e-104">根據物件的存留期知識，分配者管理員可以追蹤未清查的資源。</span><span class="sxs-lookup"><span data-stu-id="10d9e-104">The dispenser manager can track a resource that is not inventoried, based on knowledge of the object's lifetime.</span></span> <span data-ttu-id="10d9e-105">當追蹤的非配置資源釋出時，它會被終結，因此不會傳回給清查。</span><span class="sxs-lookup"><span data-stu-id="10d9e-105">When a tracked, non-allocated resource is freed, it is destroyed and therefore not returned to inventory.</span></span> <span data-ttu-id="10d9e-106">這項僅限追蹤模式適用于不需要建立和終結的資源，比將這些資源儲存在清查中更為實用。</span><span class="sxs-lookup"><span data-stu-id="10d9e-106">This track-only mode for resources that are inexpensive to create and destroy is more useful than storing them in inventory.</span></span> <span data-ttu-id="10d9e-107">這種模式也適用于管理記憶體分配程式，或針對難以清查的資源，因為有太多不同的類型。</span><span class="sxs-lookup"><span data-stu-id="10d9e-107">This mode is also useful for managing a memory dispenser or for a resource that is difficult to inventory because there are too many different types.</span></span>

<span data-ttu-id="10d9e-108">在僅限追蹤模式中，資源配置器會直接建立要求的資源，而不是要求分配者管理員從清查配置一個。</span><span class="sxs-lookup"><span data-stu-id="10d9e-108">In track-only mode, a resource dispenser directly creates a requested resource instead of asking the dispenser manager to allocate one from inventory.</span></span> <span data-ttu-id="10d9e-109">在將此資源傳回給提出要求的應用程式元件之前，資源配置器會告知分配者管理員追蹤資源，這可確保即使元件在忘了釋出資源，當元件的存留期結束時，分配器管理員也會這麼做。</span><span class="sxs-lookup"><span data-stu-id="10d9e-109">Before returning this resource to the requesting application component, the resource dispenser tells the dispenser manager to track the resource, which ensures that even if the component neglects to free the resource, the dispenser manager will do so when the component's lifetime is over.</span></span>

## <a name="related-topics"></a><span data-ttu-id="10d9e-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="10d9e-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10d9e-111">COM + 資源配置器概念</span><span class="sxs-lookup"><span data-stu-id="10d9e-111">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 




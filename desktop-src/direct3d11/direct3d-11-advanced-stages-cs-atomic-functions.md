---
title: 不可部分完成函式
description: 若要存取新的資源類型或共用記憶體，請使用連鎖內建函式。 連鎖函式保證會以不可部分完成的方式運作。 也就是說，它們保證會以程式設計的順序發生。 本節列出不可部分完成的函式。
ms.assetid: de75482f-2919-4761-82d7-c8a8811046bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1b152560eeb97e1e8d3daf69edb7a094fd04b7d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104508024"
---
# <a name="atomic-functions"></a><span data-ttu-id="a1d59-106">不可部分完成函式</span><span class="sxs-lookup"><span data-stu-id="a1d59-106">Atomic Functions</span></span>

<span data-ttu-id="a1d59-107">若要存取新的資源類型或共用記憶體，請使用連鎖內建函式。</span><span class="sxs-lookup"><span data-stu-id="a1d59-107">To access a new resource type or shared memory, use an interlocked intrinsic function.</span></span> <span data-ttu-id="a1d59-108">連鎖函式保證會以不可部分完成的方式運作。</span><span class="sxs-lookup"><span data-stu-id="a1d59-108">Interlocked functions are guaranteed to operate atomically.</span></span> <span data-ttu-id="a1d59-109">也就是說，它們保證會以程式設計的順序發生。</span><span class="sxs-lookup"><span data-stu-id="a1d59-109">That is, they are guaranteed to occur in the order programmed.</span></span> <span data-ttu-id="a1d59-110">本節列出不可部分完成的函式。</span><span class="sxs-lookup"><span data-stu-id="a1d59-110">This section lists the atomic functions.</span></span>

-   [<span data-ttu-id="a1d59-111">**InterlockedAdd**</span><span class="sxs-lookup"><span data-stu-id="a1d59-111">**InterlockedAdd**</span></span>](/windows/desktop/direct3dhlsl/interlockedadd)
-   [<span data-ttu-id="a1d59-112">**InterlockedMin**</span><span class="sxs-lookup"><span data-stu-id="a1d59-112">**InterlockedMin**</span></span>](/windows/desktop/direct3dhlsl/interlockedmin)
-   [<span data-ttu-id="a1d59-113">**InterlockedMax**</span><span class="sxs-lookup"><span data-stu-id="a1d59-113">**InterlockedMax**</span></span>](/windows/desktop/direct3dhlsl/interlockedmax)
-   [<span data-ttu-id="a1d59-114">**InterlockedOr**</span><span class="sxs-lookup"><span data-stu-id="a1d59-114">**InterlockedOr**</span></span>](/windows/desktop/direct3dhlsl/interlockedor)
-   [<span data-ttu-id="a1d59-115">**InterlockedAnd**</span><span class="sxs-lookup"><span data-stu-id="a1d59-115">**InterlockedAnd**</span></span>](/windows/desktop/direct3dhlsl/interlockedand)
-   [<span data-ttu-id="a1d59-116">**InterlockedXor**</span><span class="sxs-lookup"><span data-stu-id="a1d59-116">**InterlockedXor**</span></span>](/windows/desktop/direct3dhlsl/interlockedxor)
-   [<span data-ttu-id="a1d59-117">**InterlockedCompareStore**</span><span class="sxs-lookup"><span data-stu-id="a1d59-117">**InterlockedCompareStore**</span></span>](/windows/desktop/direct3dhlsl/interlockedcomparestore)
-   [<span data-ttu-id="a1d59-118">**InterlockedCompareExchange**</span><span class="sxs-lookup"><span data-stu-id="a1d59-118">**InterlockedCompareExchange**</span></span>](/windows/desktop/direct3dhlsl/interlockedcompareexchange)
-   [<span data-ttu-id="a1d59-119">**InterlockedExchange**</span><span class="sxs-lookup"><span data-stu-id="a1d59-119">**InterlockedExchange**</span></span>](/windows/desktop/direct3dhlsl/interlockedexchange)

## <a name="related-topics"></a><span data-ttu-id="a1d59-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="a1d59-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1d59-121">計算著色器總覽</span><span class="sxs-lookup"><span data-stu-id="a1d59-121">Compute Shader Overview</span></span>](direct3d-11-advanced-stages-compute-shader.md)
</dt> </dl>

 

 
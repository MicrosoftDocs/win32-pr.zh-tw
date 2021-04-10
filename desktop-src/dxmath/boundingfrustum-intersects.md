---
description: 測試 BoundingFrustum 與另一個物件的交集。
ms.assetid: b087761c-b298-4b64-86e7-60cd73543144
title: BoundingFrustum 交集方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9eb0082fda21978fdf6371267e4cfa0bf531622b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691759"
---
# <a name="boundingfrustumintersects-methods"></a><span data-ttu-id="b5dbe-103">BoundingFrustum 交集方法</span><span class="sxs-lookup"><span data-stu-id="b5dbe-103">BoundingFrustum.Intersects methods</span></span>

<span data-ttu-id="b5dbe-104">測試 [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) 與另一個物件的交集。</span><span class="sxs-lookup"><span data-stu-id="b5dbe-104">Tests the [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) for intersection with another object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="b5dbe-105">多載清單</span><span class="sxs-lookup"><span data-stu-id="b5dbe-105">Overload list</span></span>



| <span data-ttu-id="b5dbe-106">方法</span><span class="sxs-lookup"><span data-stu-id="b5dbe-106">Method</span></span>                                                                                           | <span data-ttu-id="b5dbe-107">描述</span><span class="sxs-lookup"><span data-stu-id="b5dbe-107">Description</span></span>                                                                                                                                |
|:-------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5dbe-108">[**BoundingFrustum：：交集 (XMVECTOR)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingfrustum-intersects(fxmvector))</span><span class="sxs-lookup"><span data-stu-id="b5dbe-108">[**BoundingFrustum::Intersects (XMVECTOR)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingfrustum-intersects(fxmvector))</span></span>                   | <span data-ttu-id="b5dbe-109">測試 [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) 與平面的交集。</span><span class="sxs-lookup"><span data-stu-id="b5dbe-109">Test the [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) for intersection with a plane.</span></span><br/>                                              |
| <span data-ttu-id="b5dbe-110">[**BoundingFrustum：：交集 (const BoundingBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingfrustum-intersects(constboundingbox_))</span><span class="sxs-lookup"><span data-stu-id="b5dbe-110">[**BoundingFrustum::Intersects (const BoundingBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingfrustum-intersects(constboundingbox_))</span></span>         | <span data-ttu-id="b5dbe-111">測試 [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) 與 [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox)的交集。</span><span class="sxs-lookup"><span data-stu-id="b5dbe-111">Test the [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) for intersection with a [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox).</span></span><br/>                 |
| <span data-ttu-id="b5dbe-112">[**BoundingFrustum：：交集 (const BoundingSphere&)**](/previous-versions/windows/desktop/legacy/hh855929(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b5dbe-112">[**BoundingFrustum::Intersects (const BoundingSphere&)**](/previous-versions/windows/desktop/legacy/hh855929(v=vs.85))</span></span>      | <span data-ttu-id="b5dbe-113">測試 [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) 與 [**BoundingSphere**](/windows/win32/api/directxcollision/ns-directxcollision-boundingsphere)的交集。</span><span class="sxs-lookup"><span data-stu-id="b5dbe-113">Test the [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) for intersection with a [**BoundingSphere**](/windows/win32/api/directxcollision/ns-directxcollision-boundingsphere).</span></span><br/>           |
| <span data-ttu-id="b5dbe-114">[**BoundingFrustum：：交集 (const BoundingFrustum&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingfrustum-intersects(constboundingfrustum_))</span><span class="sxs-lookup"><span data-stu-id="b5dbe-114">[**BoundingFrustum::Intersects (const BoundingFrustum&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingfrustum-intersects(constboundingfrustum_))</span></span>     | <span data-ttu-id="b5dbe-115">測試 [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) 與另一個 **BoundingFrustum** 的交集。</span><span class="sxs-lookup"><span data-stu-id="b5dbe-115">Test the [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) for intersection with another **BoundingFrustum**.</span></span><br/>                          |
| <span data-ttu-id="b5dbe-116">[**BoundingFrustum：：交集 (XMVECTOR、XMVECTOR、float&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingfrustum-intersects(fxmvector_fxmvector_float_))</span><span class="sxs-lookup"><span data-stu-id="b5dbe-116">[**BoundingFrustum::Intersects (XMVECTOR,XMVECTOR,float&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingfrustum-intersects(fxmvector_fxmvector_float_))</span></span>   | <span data-ttu-id="b5dbe-117">測試 [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) 與光線的交集。</span><span class="sxs-lookup"><span data-stu-id="b5dbe-117">Test the [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) for intersection with a ray.</span></span><br/>                                                |
| <span data-ttu-id="b5dbe-118">[**BoundingFrustum：：交集 (XMVECTOR、XMVECTOR、XMVECTOR)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingfrustum-intersects(fxmvector_fxmvector_fxmvector))</span><span class="sxs-lookup"><span data-stu-id="b5dbe-118">[**BoundingFrustum::Intersects (XMVECTOR,XMVECTOR,XMVECTOR)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingfrustum-intersects(fxmvector_fxmvector_fxmvector))</span></span> | <span data-ttu-id="b5dbe-119">測試 [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) 與三角形的交集。</span><span class="sxs-lookup"><span data-stu-id="b5dbe-119">Test the [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) for intersection with a triangle.</span></span><br/>                                           |
| <span data-ttu-id="b5dbe-120">[**BoundingFrustum：：交集 (const BoundingOrientedBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingfrustum-intersects(constboundingorientedbox_))</span><span class="sxs-lookup"><span data-stu-id="b5dbe-120">[**BoundingFrustum::Intersects (const BoundingOrientedBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingfrustum-intersects(constboundingorientedbox_))</span></span> | <span data-ttu-id="b5dbe-121">測試 [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) 與 [**BoundingOrientedBox**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox)的交集。</span><span class="sxs-lookup"><span data-stu-id="b5dbe-121">Test the [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) for intersection with a [**BoundingOrientedBox**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox).</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b5dbe-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b5dbe-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5dbe-123">方法</span><span class="sxs-lookup"><span data-stu-id="b5dbe-123">Methods</span></span>](boundingfrustum-methods.md)
</dt> <dt>

<span data-ttu-id="b5dbe-124">**參考**</span><span class="sxs-lookup"><span data-stu-id="b5dbe-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b5dbe-125">**BoundingFrustum**</span><span class="sxs-lookup"><span data-stu-id="b5dbe-125">**BoundingFrustum**</span></span>](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum)
</dt> </dl>

 

 

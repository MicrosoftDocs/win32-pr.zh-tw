---
description: 測試 BoundingOrientedBox 與另一個物件的交集。
ms.assetid: a79b9c1c-58fe-4c7d-b11e-7d2c22534bf6
title: BoundingOrientedBox 交集方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0e2441b9f9a41d533c31c35729cf0a33c583f85f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691743"
---
# <a name="boundingorientedboxintersects-methods"></a><span data-ttu-id="101b9-103">BoundingOrientedBox 交集方法</span><span class="sxs-lookup"><span data-stu-id="101b9-103">BoundingOrientedBox.Intersects methods</span></span>

<span data-ttu-id="101b9-104">測試 [**BoundingOrientedBox**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox) 與另一個物件的交集。</span><span class="sxs-lookup"><span data-stu-id="101b9-104">Tests the [**BoundingOrientedBox**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox) for intersection with another object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="101b9-105">多載清單</span><span class="sxs-lookup"><span data-stu-id="101b9-105">Overload list</span></span>



| <span data-ttu-id="101b9-106">方法</span><span class="sxs-lookup"><span data-stu-id="101b9-106">Method</span></span>                                                                                                   | <span data-ttu-id="101b9-107">描述</span><span class="sxs-lookup"><span data-stu-id="101b9-107">Description</span></span>                                                                                                                                 |
|:---------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="101b9-108">[**BoundingOrientedBox：：交集 (XMVECTOR)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingorientedbox-intersects(fxmvector))</span><span class="sxs-lookup"><span data-stu-id="101b9-108">[**BoundingOrientedBox::Intersects (XMVECTOR)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingorientedbox-intersects(fxmvector))</span></span>                   | <span data-ttu-id="101b9-109">測試與平面交集的 [**BoundingOrientedBox**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox) 。</span><span class="sxs-lookup"><span data-stu-id="101b9-109">Tests the [**BoundingOrientedBox**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox) for intersection with a plane.</span></span><br/>                                      |
| <span data-ttu-id="101b9-110">[**BoundingOrientedBox：：交集 (const BoundingBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingorientedbox-intersects(constboundingbox_))</span><span class="sxs-lookup"><span data-stu-id="101b9-110">[**BoundingOrientedBox::Intersects (const BoundingBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingorientedbox-intersects(constboundingbox_))</span></span>         | <span data-ttu-id="101b9-111">測試 [**BoundingOrientedBox**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox) 與 [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox)的交集。</span><span class="sxs-lookup"><span data-stu-id="101b9-111">Tests the [**BoundingOrientedBox**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox) for intersection with a [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox).</span></span><br/>         |
| <span data-ttu-id="101b9-112">[**BoundingOrientedBox：：交集 (const BoundingSphere&)**](/previous-versions/windows/desktop/legacy/hh855930(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="101b9-112">[**BoundingOrientedBox::Intersects (const BoundingSphere&)**](/previous-versions/windows/desktop/legacy/hh855930(v=vs.85))</span></span>      | <span data-ttu-id="101b9-113">測試 [**BoundingOrientedBox**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox) 與 [**BoundingSphere**](/windows/win32/api/directxcollision/ns-directxcollision-boundingsphere)的交集。</span><span class="sxs-lookup"><span data-stu-id="101b9-113">Tests the [**BoundingOrientedBox**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox) for intersection with a [**BoundingSphere**](/windows/win32/api/directxcollision/ns-directxcollision-boundingsphere).</span></span><br/>   |
| <span data-ttu-id="101b9-114">[**BoundingOrientedBox：：交集 (const BoundingFrustum&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingorientedbox-intersects(constboundingfrustum_))</span><span class="sxs-lookup"><span data-stu-id="101b9-114">[**BoundingOrientedBox::Intersects (const BoundingFrustum&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingorientedbox-intersects(constboundingfrustum_))</span></span>     | <span data-ttu-id="101b9-115">測試 [**BoundingOrientedBox**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox) 與 [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum)的交集。</span><span class="sxs-lookup"><span data-stu-id="101b9-115">Tests the [**BoundingOrientedBox**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox) for intersection with a [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum).</span></span><br/> |
| <span data-ttu-id="101b9-116">[**BoundingOrientedBox：：交集 (XMVECTOR、XMVECTOR、float&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingorientedbox-intersects(fxmvector_fxmvector_float_))</span><span class="sxs-lookup"><span data-stu-id="101b9-116">[**BoundingOrientedBox::Intersects (XMVECTOR,XMVECTOR,float&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingorientedbox-intersects(fxmvector_fxmvector_float_))</span></span>   | <span data-ttu-id="101b9-117">測試 [**BoundingOrientedBox**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox) 與光線的交集。</span><span class="sxs-lookup"><span data-stu-id="101b9-117">Tests the [**BoundingOrientedBox**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox) for intersection with a ray.</span></span><br/>                                        |
| <span data-ttu-id="101b9-118">[**BoundingOrientedBox：：交集 (XMVECTOR、XMVECTOR、XMVECTOR)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingorientedbox-intersects(fxmvector_fxmvector_fxmvector))</span><span class="sxs-lookup"><span data-stu-id="101b9-118">[**BoundingOrientedBox::Intersects (XMVECTOR,XMVECTOR,XMVECTOR)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingorientedbox-intersects(fxmvector_fxmvector_fxmvector))</span></span> | <span data-ttu-id="101b9-119">測試 [**BoundingOrientedBox**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox) 與三角形的交集。</span><span class="sxs-lookup"><span data-stu-id="101b9-119">Tests the [**BoundingOrientedBox**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox) for intersection with a triangle.</span></span><br/>                                   |
| <span data-ttu-id="101b9-120">[**BoundingOrientedBox：：交集 (const BoundingOrientedBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingorientedbox-intersects(constboundingorientedbox_))</span><span class="sxs-lookup"><span data-stu-id="101b9-120">[**BoundingOrientedBox::Intersects (const BoundingOrientedBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingorientedbox-intersects(constboundingorientedbox_))</span></span> | <span data-ttu-id="101b9-121">測試 [**BoundingOrientedBox**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox) 與 **BoundingOrientedBox** 的交集。</span><span class="sxs-lookup"><span data-stu-id="101b9-121">Tests the [**BoundingOrientedBox**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox) for intersection with a **BoundingOrientedBox**.</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="101b9-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="101b9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="101b9-123">方法</span><span class="sxs-lookup"><span data-stu-id="101b9-123">Methods</span></span>](boundingorientedbox-methods.md)
</dt> <dt>

<span data-ttu-id="101b9-124">**參考**</span><span class="sxs-lookup"><span data-stu-id="101b9-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="101b9-125">**BoundingOrientedBox**</span><span class="sxs-lookup"><span data-stu-id="101b9-125">**BoundingOrientedBox**</span></span>](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox)
</dt> </dl>

 

 

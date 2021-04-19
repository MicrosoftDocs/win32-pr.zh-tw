---
description: 測試 BoundingSphere 與物件的交集。
ms.assetid: 0326c5b4-c8c9-409d-b694-3203252a52a8
title: BoundingSphere 交集方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: e6b64cd56a6e222ad9f245c6d9e35b48edbf96ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974361"
---
# <a name="boundingsphereintersects-methods"></a><span data-ttu-id="0a890-103">BoundingSphere 交集方法</span><span class="sxs-lookup"><span data-stu-id="0a890-103">BoundingSphere.Intersects methods</span></span>

<span data-ttu-id="0a890-104">測試 BoundingSphere 與物件的交集。</span><span class="sxs-lookup"><span data-stu-id="0a890-104">Tests the BoundingSphere for intersection with an object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="0a890-105">多載清單</span><span class="sxs-lookup"><span data-stu-id="0a890-105">Overload list</span></span>



| <span data-ttu-id="0a890-106">方法</span><span class="sxs-lookup"><span data-stu-id="0a890-106">Method</span></span>                                                                                         | <span data-ttu-id="0a890-107">描述</span><span class="sxs-lookup"><span data-stu-id="0a890-107">Description</span></span>                                                                                                                              |
|:-----------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a890-108">[**BoundingSphere：：交集 (XMVECTOR)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingsphere-intersects(fxmvector))</span><span class="sxs-lookup"><span data-stu-id="0a890-108">[**BoundingSphere::Intersects (XMVECTOR)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingsphere-intersects(fxmvector))</span></span>                   | <span data-ttu-id="0a890-109">測試與平面交集的 BoundingSphere。</span><span class="sxs-lookup"><span data-stu-id="0a890-109">Tests the BoundingSphere for intersection with a Plane.</span></span><br/>                                                                       |
| <span data-ttu-id="0a890-110">[**BoundingSphere：：交集 (const BoundingBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingsphere-intersects(constboundingbox_))</span><span class="sxs-lookup"><span data-stu-id="0a890-110">[**BoundingSphere::Intersects (const BoundingBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingsphere-intersects(constboundingbox_))</span></span>         | <span data-ttu-id="0a890-111">測試 BoundingSphere 與 BoundingBox 的交集。</span><span class="sxs-lookup"><span data-stu-id="0a890-111">Tests the BoundingSphere for intersection with a BoundingBox.</span></span><br/>                                                                 |
| <span data-ttu-id="0a890-112">[**BoundingSphere：：交集 (const BoundingSphere&)**](/previous-versions/windows/desktop/legacy/hh437826(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0a890-112">[**BoundingSphere::Intersects (const BoundingSphere&)**](/previous-versions/windows/desktop/legacy/hh437826(v=vs.85))</span></span>      | <span data-ttu-id="0a890-113">測試 BoundingSphere 與 BoundingSphere 的交集。</span><span class="sxs-lookup"><span data-stu-id="0a890-113">Tests the BoundingSphere for intersection with a BoundingSphere.</span></span><br/>                                                              |
| <span data-ttu-id="0a890-114">[**BoundingSphere：：交集 (const BoundingFrustum&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingsphere-intersects(constboundingfrustum_))</span><span class="sxs-lookup"><span data-stu-id="0a890-114">[**BoundingSphere::Intersects (const BoundingFrustum&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingsphere-intersects(constboundingfrustum_))</span></span>     | <span data-ttu-id="0a890-115">測試 [**BoundingSphere**](/windows/win32/api/directxcollision/ns-directxcollision-boundingsphere) 與 [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum)的交集。</span><span class="sxs-lookup"><span data-stu-id="0a890-115">Test the [**BoundingSphere**](/windows/win32/api/directxcollision/ns-directxcollision-boundingsphere) for intersection with a [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum).</span></span><br/>         |
| <span data-ttu-id="0a890-116">[**BoundingSphere：：交集 (XMVECTOR、XMVECTOR、float&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingsphere-intersects(fxmvector_fxmvector_float_))</span><span class="sxs-lookup"><span data-stu-id="0a890-116">[**BoundingSphere::Intersects (XMVECTOR,XMVECTOR,float&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingsphere-intersects(fxmvector_fxmvector_float_))</span></span>   | <span data-ttu-id="0a890-117">測試 BoundingSphere 與光線的交集。</span><span class="sxs-lookup"><span data-stu-id="0a890-117">Tests the BoundingSphere for intersection with a ray.</span></span><br/>                                                                         |
| <span data-ttu-id="0a890-118">[**BoundingSphere：：交集 (XMVECTOR、XMVECTOR、XMVECTOR)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingsphere-intersects(fxmvector_fxmvector_fxmvector))</span><span class="sxs-lookup"><span data-stu-id="0a890-118">[**BoundingSphere::Intersects (XMVECTOR,XMVECTOR,XMVECTOR)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingsphere-intersects(fxmvector_fxmvector_fxmvector))</span></span> | <span data-ttu-id="0a890-119">測試 BoundingSphere 與三角形的交集。</span><span class="sxs-lookup"><span data-stu-id="0a890-119">Tests the BoundingSphere for intersection with a triangle.</span></span><br/>                                                                    |
| <span data-ttu-id="0a890-120">[**BoundingSphere：：交集 (const BoundingOrientedBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingsphere-intersects(constboundingorientedbox_))</span><span class="sxs-lookup"><span data-stu-id="0a890-120">[**BoundingSphere::Intersects (const BoundingOrientedBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingsphere-intersects(constboundingorientedbox_))</span></span> | <span data-ttu-id="0a890-121">測試 [**BoundingSphere**](/windows/win32/api/directxcollision/ns-directxcollision-boundingsphere) 與 [**BoundingOrientedBox**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox)的交集。</span><span class="sxs-lookup"><span data-stu-id="0a890-121">Test the [**BoundingSphere**](/windows/win32/api/directxcollision/ns-directxcollision-boundingsphere) for intersection with a [**BoundingOrientedBox**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox).</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0a890-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0a890-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a890-123">方法</span><span class="sxs-lookup"><span data-stu-id="0a890-123">Methods</span></span>](boundingsphere-methods.md)
</dt> <dt>

<span data-ttu-id="0a890-124">**參考**</span><span class="sxs-lookup"><span data-stu-id="0a890-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0a890-125">**BoundingSphere**</span><span class="sxs-lookup"><span data-stu-id="0a890-125">**BoundingSphere**</span></span>](/windows/win32/api/directxcollision/ns-directxcollision-boundingsphere)
</dt> </dl>

 

 

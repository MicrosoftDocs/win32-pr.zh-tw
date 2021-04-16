---
description: 測試 BoundingBox 與另一個物件的交集。
ms.assetid: df3d3df9-aa74-413d-808c-f7b276d11279
title: BoundingBox 交集方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9039d99640ae3989d0b20e9d48f681edabb021f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512737"
---
# <a name="boundingboxintersects-methods"></a><span data-ttu-id="2beb2-103">BoundingBox 交集方法</span><span class="sxs-lookup"><span data-stu-id="2beb2-103">BoundingBox.Intersects methods</span></span>

<span data-ttu-id="2beb2-104">測試 BoundingBox 與另一個物件的交集。</span><span class="sxs-lookup"><span data-stu-id="2beb2-104">Tests the BoundingBox for intersection with another object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="2beb2-105">多載清單</span><span class="sxs-lookup"><span data-stu-id="2beb2-105">Overload list</span></span>



| <span data-ttu-id="2beb2-106">方法</span><span class="sxs-lookup"><span data-stu-id="2beb2-106">Method</span></span>                                                                                   | <span data-ttu-id="2beb2-107">描述</span><span class="sxs-lookup"><span data-stu-id="2beb2-107">Description</span></span>                                                                                                                        |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2beb2-108">[**BoundingBox：：交集 (XMVECTOR)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(fxmvector))</span><span class="sxs-lookup"><span data-stu-id="2beb2-108">[**BoundingBox::Intersects (XMVECTOR)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(fxmvector))</span></span>                   | <span data-ttu-id="2beb2-109">測試 BoundingBox 與平面的交集。</span><span class="sxs-lookup"><span data-stu-id="2beb2-109">Test the BoundingBox for intersection with a plane.</span></span><br/>                                                                     |
| <span data-ttu-id="2beb2-110">[**BoundingBox：：交集 (const BoundingBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(constboundingbox_))</span><span class="sxs-lookup"><span data-stu-id="2beb2-110">[**BoundingBox::Intersects (const BoundingBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(constboundingbox_))</span></span>         | <span data-ttu-id="2beb2-111">測試 BoundingBox 與另一個 BoundingBox 的交集。</span><span class="sxs-lookup"><span data-stu-id="2beb2-111">Tests the BoundingBox for intersection with another BoundingBox.</span></span><br/>                                                        |
| <span data-ttu-id="2beb2-112">[**BoundingBox：：交集 (const BoundingSphere&)**](/previous-versions/windows/desktop/legacy/hh437825(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2beb2-112">[**BoundingBox::Intersects (const BoundingSphere&)**](/previous-versions/windows/desktop/legacy/hh437825(v=vs.85))</span></span>      | <span data-ttu-id="2beb2-113">測試 BoundingBox 與 BoundingSphere 的交集。</span><span class="sxs-lookup"><span data-stu-id="2beb2-113">Tests the BoundingBox for intersection with a BoundingSphere.</span></span><br/>                                                           |
| <span data-ttu-id="2beb2-114">[**BoundingBox：：交集 (const BoundingFrustum&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(constboundingfrustum_))</span><span class="sxs-lookup"><span data-stu-id="2beb2-114">[**BoundingBox::Intersects (const BoundingFrustum&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(constboundingfrustum_))</span></span>     | <span data-ttu-id="2beb2-115">測試 [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) 與 [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum)的交集。</span><span class="sxs-lookup"><span data-stu-id="2beb2-115">Test the [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) for intersection with a [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum).</span></span><br/>         |
| <span data-ttu-id="2beb2-116">[**BoundingBox：：交集 (XMVECTOR、XMVECTOR、float&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(fxmvector_fxmvector_float_))</span><span class="sxs-lookup"><span data-stu-id="2beb2-116">[**BoundingBox::Intersects (XMVECTOR,XMVECTOR,float&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(fxmvector_fxmvector_float_))</span></span>   | <span data-ttu-id="2beb2-117">測試 BoundingBox 與光線的交集。</span><span class="sxs-lookup"><span data-stu-id="2beb2-117">Test the BoundingBox for intersection with a ray.</span></span><br/>                                                                       |
| <span data-ttu-id="2beb2-118">[**BoundingBox：：交集 (XMVECTOR、XMVECTOR、XMVECTOR)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(fxmvector_fxmvector_fxmvector))</span><span class="sxs-lookup"><span data-stu-id="2beb2-118">[**BoundingBox::Intersects (XMVECTOR,XMVECTOR,XMVECTOR)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(fxmvector_fxmvector_fxmvector))</span></span> | <span data-ttu-id="2beb2-119">測試 BoundingBox 與三角形的交集。</span><span class="sxs-lookup"><span data-stu-id="2beb2-119">Test the BoundingBox for intersection with a triangle.</span></span><br/>                                                                  |
| <span data-ttu-id="2beb2-120">[**BoundingBox：：交集 (const BoundingOrientedBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(constboundingorientedbox_))</span><span class="sxs-lookup"><span data-stu-id="2beb2-120">[**BoundingBox::Intersects (const BoundingOrientedBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(constboundingorientedbox_))</span></span> | <span data-ttu-id="2beb2-121">測試 [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) 與 [**BoundingOrientedBox**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox)的交集。</span><span class="sxs-lookup"><span data-stu-id="2beb2-121">Test the [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) for intersection with a [**BoundingOrientedBox**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox).</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2beb2-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2beb2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2beb2-123">方法</span><span class="sxs-lookup"><span data-stu-id="2beb2-123">Methods</span></span>](boundingbox-methods.md)
</dt> <dt>

<span data-ttu-id="2beb2-124">**參考**</span><span class="sxs-lookup"><span data-stu-id="2beb2-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2beb2-125">**BoundingBox**</span><span class="sxs-lookup"><span data-stu-id="2beb2-125">**BoundingBox**</span></span>](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox)
</dt> </dl>

 

 

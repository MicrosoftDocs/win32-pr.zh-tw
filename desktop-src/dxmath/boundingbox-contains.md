---
description: 測試 BoundingBox 是否包含指定的物件。
ms.assetid: 876c7764-9378-48e5-812c-3646930900c5
title: BoundingBox 包含方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 485dbbaf5ab4522eb50fe598325e5ecbb48fff57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512741"
---
# <a name="boundingboxcontains-methods"></a><span data-ttu-id="ef8f7-103">BoundingBox 包含方法</span><span class="sxs-lookup"><span data-stu-id="ef8f7-103">BoundingBox.Contains methods</span></span>

<span data-ttu-id="ef8f7-104">測試 BoundingBox 是否包含指定的物件。</span><span class="sxs-lookup"><span data-stu-id="ef8f7-104">Tests whether the BoundingBox contains a specified object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="ef8f7-105">多載清單</span><span class="sxs-lookup"><span data-stu-id="ef8f7-105">Overload list</span></span>



| <span data-ttu-id="ef8f7-106">方法</span><span class="sxs-lookup"><span data-stu-id="ef8f7-106">Method</span></span>                                                                               | <span data-ttu-id="ef8f7-107">描述</span><span class="sxs-lookup"><span data-stu-id="ef8f7-107">Description</span></span>                                                                                                                                |
|:-------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ef8f7-108">**BoundingBox：： Contains (XMVECTOR)**</span><span class="sxs-lookup"><span data-stu-id="ef8f7-108">**BoundingBox::Contains (XMVECTOR)**</span></span>](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-contains)                   | <span data-ttu-id="ef8f7-109">測試 BoundingBox 是否包含指定的點。</span><span class="sxs-lookup"><span data-stu-id="ef8f7-109">Tests the whether the BoundingBox contains a specified point.</span></span><br/>                                                                   |
| <span data-ttu-id="ef8f7-110">[**BoundingBox：： Contains (const BoundingBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-contains(constboundingbox_))</span><span class="sxs-lookup"><span data-stu-id="ef8f7-110">[**BoundingBox::Contains (const BoundingBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-contains(constboundingbox_))</span></span>         | <span data-ttu-id="ef8f7-111">測試 BoundingBox 是否包含另一個 BoundingBox。</span><span class="sxs-lookup"><span data-stu-id="ef8f7-111">Tests whether the BoundingBox contains another BoundingBox.</span></span><br/>                                                                     |
| <span data-ttu-id="ef8f7-112">[**BoundingBox：： Contains (const BoundingSphere&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-contains(constboundingsphere_))</span><span class="sxs-lookup"><span data-stu-id="ef8f7-112">[**BoundingBox::Contains (const BoundingSphere&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-contains(constboundingsphere_))</span></span>      | <span data-ttu-id="ef8f7-113">測試 BoundingBox 是否包含指定的 BoundingSphere。</span><span class="sxs-lookup"><span data-stu-id="ef8f7-113">Tests whether the BoundingBox contains a specified BoundingSphere.</span></span><br/>                                                              |
| <span data-ttu-id="ef8f7-114">[**BoundingBox：： Contains (const BoundingFrustum&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-contains(constboundingfrustum_))</span><span class="sxs-lookup"><span data-stu-id="ef8f7-114">[**BoundingBox::Contains (const BoundingFrustum&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-contains(constboundingfrustum_))</span></span>     | <span data-ttu-id="ef8f7-115">測試 [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) 是否包含指定的 [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum)。</span><span class="sxs-lookup"><span data-stu-id="ef8f7-115">Tests whether the [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) contains the specified [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum).</span></span><br/>         |
| <span data-ttu-id="ef8f7-116">[**BoundingBox：： Contains (XMVECTOR、XMVECTOR、XMVECTOR)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-contains(fxmvector_fxmvector_fxmvector))</span><span class="sxs-lookup"><span data-stu-id="ef8f7-116">[**BoundingBox::Contains (XMVECTOR,XMVECTOR,XMVECTOR)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-contains(fxmvector_fxmvector_fxmvector))</span></span> | <span data-ttu-id="ef8f7-117">測試 BoundingBox 是否包含指定的三角形。</span><span class="sxs-lookup"><span data-stu-id="ef8f7-117">Test whether the BoundingBox contains a specified triangle.</span></span><br/>                                                                     |
| <span data-ttu-id="ef8f7-118">[**BoundingBox：： Contains (const BoundingOrientedBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-contains(constboundingorientedbox_))</span><span class="sxs-lookup"><span data-stu-id="ef8f7-118">[**BoundingBox::Contains (const BoundingOrientedBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-contains(constboundingorientedbox_))</span></span> | <span data-ttu-id="ef8f7-119">測試 [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) 是否包含指定的 [**BoundingOrientedBox**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox)。</span><span class="sxs-lookup"><span data-stu-id="ef8f7-119">Tests whether the [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) contains the specified [**BoundingOrientedBox**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox).</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ef8f7-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ef8f7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef8f7-121">方法</span><span class="sxs-lookup"><span data-stu-id="ef8f7-121">Methods</span></span>](boundingbox-methods.md)
</dt> <dt>

<span data-ttu-id="ef8f7-122">**參考**</span><span class="sxs-lookup"><span data-stu-id="ef8f7-122">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ef8f7-123">**BoundingBox**</span><span class="sxs-lookup"><span data-stu-id="ef8f7-123">**BoundingBox**</span></span>](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox)
</dt> </dl>

 

 

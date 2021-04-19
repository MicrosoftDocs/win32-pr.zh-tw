---
description: BoundingBox 方法
ms.assetid: 68db5936-f0f8-4dbd-a183-b6c3089af0f0
title: BoundingBox 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b58c79f202304a289bf1e30447b76ba9ad6dc83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974990"
---
# <a name="boundingbox-methods"></a><span data-ttu-id="dc96a-103">BoundingBox 方法</span><span class="sxs-lookup"><span data-stu-id="dc96a-103">BoundingBox Methods</span></span>



| <span data-ttu-id="dc96a-104">方法</span><span class="sxs-lookup"><span data-stu-id="dc96a-104">Method</span></span>                                                              | <span data-ttu-id="dc96a-105">描述</span><span class="sxs-lookup"><span data-stu-id="dc96a-105">Description</span></span>                                                                                            |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dc96a-106">**包含**</span><span class="sxs-lookup"><span data-stu-id="dc96a-106">**Contains**</span></span>](boundingbox-contains.md)<br/>                 | <span data-ttu-id="dc96a-107">測試 BoundingBox 是否包含指定的物件。</span><span class="sxs-lookup"><span data-stu-id="dc96a-107">Tests whether the BoundingBox contains a specified object.</span></span><br/>                                  |
| [<span data-ttu-id="dc96a-108">**CreateFromPoints**</span><span class="sxs-lookup"><span data-stu-id="dc96a-108">**CreateFromPoints**</span></span>](boundingbox-createfrompoints.md)<br/> | <span data-ttu-id="dc96a-109">從點建立 BoundingBox。</span><span class="sxs-lookup"><span data-stu-id="dc96a-109">Creates a BoundingBox from points.</span></span><br/>                                                          |
| [<span data-ttu-id="dc96a-110">**相交**</span><span class="sxs-lookup"><span data-stu-id="dc96a-110">**Intersects**</span></span>](boundingbox-intersects.md)<br/>             | <span data-ttu-id="dc96a-111">測試 BoundingBox 與另一個物件的交集。</span><span class="sxs-lookup"><span data-stu-id="dc96a-111">Tests the BoundingBox for intersection with another object.</span></span><br/>                                 |
| [<span data-ttu-id="dc96a-112">**Transform**</span><span class="sxs-lookup"><span data-stu-id="dc96a-112">**Transform**</span></span>](boundingbox-transform.md)<br/>               | <span data-ttu-id="dc96a-113">轉換 BoundingBox。</span><span class="sxs-lookup"><span data-stu-id="dc96a-113">Transforms the BoundingBox.</span></span><br/>                                                                 |
| [<span data-ttu-id="dc96a-114">**ContainedBy**</span><span class="sxs-lookup"><span data-stu-id="dc96a-114">**ContainedBy**</span></span>](/windows/desktop/api/DirectXCollision/nf-directxcollision-boundingbox-containedby)<br/>           | <span data-ttu-id="dc96a-115">測試 [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) 是否包含在指定的錐中。</span><span class="sxs-lookup"><span data-stu-id="dc96a-115">Tests whether the [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) is contained by the specified frustum.</span></span><br/> |
| [<span data-ttu-id="dc96a-116">**CreateFromSphere**</span><span class="sxs-lookup"><span data-stu-id="dc96a-116">**CreateFromSphere**</span></span>](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-createfromsphere)<br/> | <span data-ttu-id="dc96a-117">建立夠大的 BoundingBox，以包含指定的 BoundingSphere。</span><span class="sxs-lookup"><span data-stu-id="dc96a-117">Creates a BoundingBox large enough to contain the a specified BoundingSphere.</span></span><br/>               |
| [<span data-ttu-id="dc96a-118">**CreateMerged**</span><span class="sxs-lookup"><span data-stu-id="dc96a-118">**CreateMerged**</span></span>](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-createmerged)<br/>         | <span data-ttu-id="dc96a-119">建立夠大的 BoundingBox，以包含兩個指定的 BoundBox 實例。</span><span class="sxs-lookup"><span data-stu-id="dc96a-119">Creates a BoundingBox large enough to contains two specified BoundBox intances.</span></span><br/>             |
| [<span data-ttu-id="dc96a-120">**GetCorners**</span><span class="sxs-lookup"><span data-stu-id="dc96a-120">**GetCorners**</span></span>](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-getcorners)<br/>             | <span data-ttu-id="dc96a-121">抓取 BoundingBox 的角落。</span><span class="sxs-lookup"><span data-stu-id="dc96a-121">Retrieves the corners of the BoundingBox.</span></span><br/>                                                   |
| [<span data-ttu-id="dc96a-122">**op \_ 指派**</span><span class="sxs-lookup"><span data-stu-id="dc96a-122">**op\_Assignment**</span></span>](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-operator-assign)<br/>      | <span data-ttu-id="dc96a-123">從另一個 BoundingBox 複製值。</span><span class="sxs-lookup"><span data-stu-id="dc96a-123">Copies values from another BoundingBox.</span></span><br/>                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="dc96a-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="dc96a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc96a-125">BoundingBox</span><span class="sxs-lookup"><span data-stu-id="dc96a-125">BoundingBox</span></span>](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox)
</dt> </dl>

 

 

---
title: '裁剪 (OpenGL) '
description: 裁剪會以兩個步驟進行
ms.assetid: f6f60135-f43b-4595-bfd3-33e750413e70
keywords:
- OpenGL 處理管線，裁剪
- 裁剪 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08aa35458e7e0a137759fe22be95f4b399b4d56b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383673"
---
# <a name="clipping-opengl"></a><span data-ttu-id="fb811-105">裁剪 (OpenGL) </span><span class="sxs-lookup"><span data-stu-id="fb811-105">Clipping (OpenGL)</span></span>

<span data-ttu-id="fb811-106">裁剪會以兩個步驟進行：</span><span class="sxs-lookup"><span data-stu-id="fb811-106">Clipping occurs in two steps:</span></span>

1.  <span data-ttu-id="fb811-107">**查看磁片區 clippingApplication 特定的剪輯。**</span><span class="sxs-lookup"><span data-stu-id="fb811-107">**View volume clippingApplication-specific clipping.**</span></span> <span data-ttu-id="fb811-108">在組合基本專案之後，就會視需要針對您使用 [**glClipPlane**](glclipplane.md)定義的任何裁剪平面，將它們裁剪為眼睛座標。</span><span class="sxs-lookup"><span data-stu-id="fb811-108">Immediately after primitives are assembled, they're clipped in eye coordinates as necessary for any clipping planes you've defined with [**glClipPlane**](glclipplane.md).</span></span> <span data-ttu-id="fb811-109"> (OpenGL 必須支援至少六個這類應用程式特定的裁剪平面。 ) </span><span class="sxs-lookup"><span data-stu-id="fb811-109">(OpenGL requires support for at least six such application-specific clipping planes.)</span></span>
2.  <span data-ttu-id="fb811-110">投射矩陣會將基本專案轉換成剪輯座標，並由對應的視圖音量裁剪。</span><span class="sxs-lookup"><span data-stu-id="fb811-110">Primitives are transformed by the projection matrix into clip coordinates and clipped by the corresponding view volume.</span></span> <span data-ttu-id="fb811-111">此矩陣可由矩陣轉換函式控制 (查看 [矩陣轉換](matrix-transformations.md)) 但通常是由 [**glFrustum**](glfrustum.md) 或 [**glOrtho**](glortho.md)所指定。</span><span class="sxs-lookup"><span data-stu-id="fb811-111">This matrix can be controlled by the matrix transformation functions (see [Matrix Transformations](matrix-transformations.md)) but is typically specified by [**glFrustum**](glfrustum.md) or [**glOrtho**](glortho.md).</span></span>

<span data-ttu-id="fb811-112">點、線段和多邊形會在裁剪期間以不同方式處理：</span><span class="sxs-lookup"><span data-stu-id="fb811-112">Points, line segments, and polygons are handled differently during clipping:</span></span>

-   <span data-ttu-id="fb811-113">點會以原始狀態保留 (如果它們位於剪輯磁片區中) 或捨棄 (（如果它們位於剪輯磁片區) 以外）。</span><span class="sxs-lookup"><span data-stu-id="fb811-113">Points are either retained in their original state (if they're inside the clip volume) or discarded (if they're outside the clip volume).</span></span>
-   <span data-ttu-id="fb811-114">如果線段或多邊形的部分位於剪輯音量之外，就會在剪輯點產生新頂點。</span><span class="sxs-lookup"><span data-stu-id="fb811-114">If portions of line segments or polygons are outside the clip volume, new vertices are generated at the clip points.</span></span>
-   <span data-ttu-id="fb811-115">若為多邊形，可能需要在剪輯點產生的新頂點之間建立整個邊緣。</span><span class="sxs-lookup"><span data-stu-id="fb811-115">For polygons, an entire edge may need to be constructed between new vertices generated at the clip points.</span></span>
-   <span data-ttu-id="fb811-116">若為已裁剪的線段和多邊形，則會將邊緣旗標、色彩和材質資訊指派給所有新頂點。</span><span class="sxs-lookup"><span data-stu-id="fb811-116">For line segments and polygons that are clipped, the edge flag, color, and texture information is assigned to all new vertices.</span></span>

 

 





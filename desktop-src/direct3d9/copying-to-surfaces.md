---
description: 使用 IDirect3DDevice9：： UpdateSurface 時，請在來源介面上傳遞矩形，或使用 Null 來指定整個表面。
ms.assetid: 2219d037-8480-4c36-b04e-0c23406a2e7e
title: 複製到 (Direct3D 9) 的表面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 163907aada5b2396a2a103d94af49d7ddd01d5ef
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468505"
---
# <a name="copying-to-surfaces-direct3d-9"></a><span data-ttu-id="96ec5-103">複製到 (Direct3D 9) 的表面</span><span class="sxs-lookup"><span data-stu-id="96ec5-103">Copying to Surfaces (Direct3D 9)</span></span>

<span data-ttu-id="96ec5-104">使用 [**IDirect3DDevice9：： UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface)時，請在來源介面上傳遞矩形，或使用 **Null** 來指定整個表面。</span><span class="sxs-lookup"><span data-stu-id="96ec5-104">When using [**IDirect3DDevice9::UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface), pass a rectangle on the source surface, or use **NULL** to specify the entire surface.</span></span> <span data-ttu-id="96ec5-105">您也可以在目的地介面上傳遞點，以複製來源影像上的矩形左上角位置。</span><span class="sxs-lookup"><span data-stu-id="96ec5-105">You also pass a point on the destination surface to which the upper left position of the rectangle on the source image is copied.</span></span> <span data-ttu-id="96ec5-106">這個方法不支援裁剪。</span><span class="sxs-lookup"><span data-stu-id="96ec5-106">This method does not support clipping.</span></span> <span data-ttu-id="96ec5-107">除非來源矩形和對應的目的矩形分別包含在來源和目的介面內，否則作業將會失敗。</span><span class="sxs-lookup"><span data-stu-id="96ec5-107">The operation will fail unless the source rectangle and the corresponding destination rectangle are completely contained within the source and destination surfaces respectively.</span></span> <span data-ttu-id="96ec5-108">這個方法不支援 Alpha 混色、色彩按鍵或格式轉換。</span><span class="sxs-lookup"><span data-stu-id="96ec5-108">This method does not support alpha blending, color keys, or format conversion.</span></span> <span data-ttu-id="96ec5-109">請注意，目的地和來源表面必須是相異的。</span><span class="sxs-lookup"><span data-stu-id="96ec5-109">Note that the destination and source surfaces must be distinct.</span></span>

<span data-ttu-id="96ec5-110">如需使用 UpdateSurface 的其他限制，請參閱 [**IDirect3DDevice9：： UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface)。</span><span class="sxs-lookup"><span data-stu-id="96ec5-110">For other restrictions when using UpdateSurface, see [**IDirect3DDevice9::UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface).</span></span>

<span data-ttu-id="96ec5-111">C + +/C 也提供下列方法，可將影像複製到 Direct3D 介面。</span><span class="sxs-lookup"><span data-stu-id="96ec5-111">The following methods are also available in C++/C for copying images to a Direct3D surface.</span></span>

-   [<span data-ttu-id="96ec5-112">**D3DXLoadSurfaceFromFile**</span><span class="sxs-lookup"><span data-stu-id="96ec5-112">**D3DXLoadSurfaceFromFile**</span></span>](d3dxloadsurfacefromfile.md)
-   [<span data-ttu-id="96ec5-113">**D3DXLoadSurfaceFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="96ec5-113">**D3DXLoadSurfaceFromFileInMemory**</span></span>](d3dxloadsurfacefromfileinmemory.md)
-   [<span data-ttu-id="96ec5-114">**D3DXLoadSurfaceFromMemory**</span><span class="sxs-lookup"><span data-stu-id="96ec5-114">**D3DXLoadSurfaceFromMemory**</span></span>](d3dxloadsurfacefrommemory.md)
-   [<span data-ttu-id="96ec5-115">**D3DXLoadSurfaceFromResource**</span><span class="sxs-lookup"><span data-stu-id="96ec5-115">**D3DXLoadSurfaceFromResource**</span></span>](d3dxloadsurfacefromresource.md)
-   [<span data-ttu-id="96ec5-116">**D3DXLoadSurfaceFromSurface**</span><span class="sxs-lookup"><span data-stu-id="96ec5-116">**D3DXLoadSurfaceFromSurface**</span></span>](d3dxloadsurfacefromsurface.md)
-   [<span data-ttu-id="96ec5-117">**IDirect3DDevice9::UpdateSurface**</span><span class="sxs-lookup"><span data-stu-id="96ec5-117">**IDirect3DDevice9::UpdateSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface)

## <a name="updatesurface-example"></a><span data-ttu-id="96ec5-118">UpdateSurface 範例</span><span class="sxs-lookup"><span data-stu-id="96ec5-118">UpdateSurface Example</span></span>

<span data-ttu-id="96ec5-119">下列範例會將兩個矩形從來源介面複製到目的介面。</span><span class="sxs-lookup"><span data-stu-id="96ec5-119">The following example copies two rectangles from the source surface to a destination surface.</span></span> <span data-ttu-id="96ec5-120">第一個矩形會從來源介面上的 (0、0、50、50) 複製到目的地介面上的相同位置，而第二個矩形會從來源介面上 (50、50、100、100) 複製到目的介面上的 (150、150、200、200) 。</span><span class="sxs-lookup"><span data-stu-id="96ec5-120">The first rectangle is copied from (0, 0, 50, 50) on the source surface to the same location on the destination surface, and the second rectangle is copied from (50, 50, 100, 100) on the source surface to (150, 150, 200, 200) on the destination surface.</span></span>


```
//The following assumptions are made:
// -d3dDevice is a valid Direct3DDevice9 object.
// -pSource and pDest are valid IDirect3DSurface9 pointers.

RECT  rcSource[] = {  0,  0,  50,  50,
                     50, 50, 100, 100 };
POINT ptDest[]   = {  0,  0, 150, 150 };

d3dDevice->UpdateSurface( pSource, rcSource, 2, pDest, ptDest);
```



## <a name="related-topics"></a><span data-ttu-id="96ec5-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="96ec5-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96ec5-122">Direct3D 表面</span><span class="sxs-lookup"><span data-stu-id="96ec5-122">Direct3D Surfaces</span></span>](direct3d-surfaces.md)
</dt> <dt>

[<span data-ttu-id="96ec5-123">**IDirect3DDevice9::StretchRect**</span><span class="sxs-lookup"><span data-stu-id="96ec5-123">**IDirect3DDevice9::StretchRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect)
</dt> </dl>

 

 

---
description: 介面代表顯示記憶體的線性區域，而且通常位於顯示配接器的顯示記憶體中，雖然表面可以存在於系統記憶體中。 介面是由 IDirect3DSurface9 介面所管理。
ms.assetid: 17add726-3d95-46bc-8e15-3be0e570c49c
title: 'Direct3d (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08729cc7252c39ddf71048991a796469f2e8b0b2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687376"
---
# <a name="direct3d-surfaces-direct3d-9"></a><span data-ttu-id="8cdcb-104">Direct3d (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="8cdcb-104">Direct3D Surfaces (Direct3D 9)</span></span>

<span data-ttu-id="8cdcb-105">介面代表顯示記憶體的線性區域，而且通常位於顯示配接器的顯示記憶體中，雖然表面可以存在於系統記憶體中。</span><span class="sxs-lookup"><span data-stu-id="8cdcb-105">A surface represents a linear area of display memory and usually resides in the display memory of the display card, although surfaces can exist in system memory.</span></span> <span data-ttu-id="8cdcb-106">介面是由 [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) 介面所管理。</span><span class="sxs-lookup"><span data-stu-id="8cdcb-106">Surfaces are managed by the [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface.</span></span>

-   <span data-ttu-id="8cdcb-107">前端緩衝區。</span><span class="sxs-lookup"><span data-stu-id="8cdcb-107">Front Buffer.</span></span> <span data-ttu-id="8cdcb-108">由圖形介面卡轉譯並顯示在監視器上的記憶體矩形。</span><span class="sxs-lookup"><span data-stu-id="8cdcb-108">A rectangle of memory that is translated by the graphics adapter and displayed on the monitor.</span></span> <span data-ttu-id="8cdcb-109">在 Direct3D 中，應用程式永遠不會直接寫入至前端緩衝區。</span><span class="sxs-lookup"><span data-stu-id="8cdcb-109">In Direct3D an application never writes directly to the front buffer.</span></span>
-   <span data-ttu-id="8cdcb-110">背景緩衝區。</span><span class="sxs-lookup"><span data-stu-id="8cdcb-110">Back Buffer.</span></span> <span data-ttu-id="8cdcb-111">應用程式可直接寫入的記憶體矩形。</span><span class="sxs-lookup"><span data-stu-id="8cdcb-111">A rectangle of memory that an application can directly write to.</span></span> <span data-ttu-id="8cdcb-112">背景緩衝區永遠不會直接顯示在監視器上。</span><span class="sxs-lookup"><span data-stu-id="8cdcb-112">The back buffer is never directly displayed on the monitor.</span></span>
-   <span data-ttu-id="8cdcb-113">翻轉表面。</span><span class="sxs-lookup"><span data-stu-id="8cdcb-113">Flipping surfaces.</span></span> <span data-ttu-id="8cdcb-114">將背景緩衝區移至前端緩衝區的進程。</span><span class="sxs-lookup"><span data-stu-id="8cdcb-114">The process of moving the back buffer to the front buffer.</span></span>
-   <span data-ttu-id="8cdcb-115">交換鏈。</span><span class="sxs-lookup"><span data-stu-id="8cdcb-115">Swap chain.</span></span> <span data-ttu-id="8cdcb-116">一或多個後置緩衝區的集合，可連續呈現給前端緩衝區。</span><span class="sxs-lookup"><span data-stu-id="8cdcb-116">A collection of one or more back buffers that can be serially presented to the front buffer.</span></span>

## <a name="getting-a-surface"></a><span data-ttu-id="8cdcb-117">取得介面</span><span class="sxs-lookup"><span data-stu-id="8cdcb-117">Getting a Surface</span></span>

<span data-ttu-id="8cdcb-118">藉由呼叫下列其中一種方法來建立介面：</span><span class="sxs-lookup"><span data-stu-id="8cdcb-118">Create a surface by calling any of these methods:</span></span>

-   [<span data-ttu-id="8cdcb-119">**CreateDepthStencilSurface**</span><span class="sxs-lookup"><span data-stu-id="8cdcb-119">**CreateDepthStencilSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)
-   [<span data-ttu-id="8cdcb-120">**CreateOffscreenPlainSurface**</span><span class="sxs-lookup"><span data-stu-id="8cdcb-120">**CreateOffscreenPlainSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface)
-   [<span data-ttu-id="8cdcb-121">**CreateRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="8cdcb-121">**CreateRenderTarget**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)

<span data-ttu-id="8cdcb-122">介面格式決定如何解讀介面記憶體中每個圖元的資料。</span><span class="sxs-lookup"><span data-stu-id="8cdcb-122">Surface formats determine how data for each pixel in surface memory is interpreted.</span></span> <span data-ttu-id="8cdcb-123">Direct3D 會使用 [**D3DSURFACE \_ DESC**](d3dsurface-desc.md)結構的 [D3DFORMAT](d3dformat.md)成員來描述介面格式。</span><span class="sxs-lookup"><span data-stu-id="8cdcb-123">Direct3D uses the [D3DFORMAT](d3dformat.md) member of the [**D3DSURFACE\_DESC**](d3dsurface-desc.md) structure to describe the surface format.</span></span> <span data-ttu-id="8cdcb-124">您可以藉由呼叫 [**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdesc) 方法來取出現有介面的格式。</span><span class="sxs-lookup"><span data-stu-id="8cdcb-124">You can retrieve the format of an existing surface by calling the [**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdesc) method.</span></span>

<span data-ttu-id="8cdcb-125">建立介面之後，您可以藉由呼叫下列其中一種方法來取得其指標：</span><span class="sxs-lookup"><span data-stu-id="8cdcb-125">Once a surface is created, you can get a pointer to it by calling any of these methods:</span></span>

-   [<span data-ttu-id="8cdcb-126">**GetCubeMapSurface**</span><span class="sxs-lookup"><span data-stu-id="8cdcb-126">**GetCubeMapSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface)
-   [<span data-ttu-id="8cdcb-127">**GetBackBuffer**</span><span class="sxs-lookup"><span data-stu-id="8cdcb-127">**GetBackBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
-   [<span data-ttu-id="8cdcb-128">**GetDepthStencilSurface**</span><span class="sxs-lookup"><span data-stu-id="8cdcb-128">**GetDepthStencilSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdepthstencilsurface)
-   [<span data-ttu-id="8cdcb-129">**GetFrontBufferData**</span><span class="sxs-lookup"><span data-stu-id="8cdcb-129">**GetFrontBufferData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getfrontbufferdata)
-   [<span data-ttu-id="8cdcb-130">**GetRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="8cdcb-130">**GetRenderTarget**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrendertarget)
-   [<span data-ttu-id="8cdcb-131">**GetBackBuffer**</span><span class="sxs-lookup"><span data-stu-id="8cdcb-131">**GetBackBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
-   [<span data-ttu-id="8cdcb-132">**GetSurfaceLevel**</span><span class="sxs-lookup"><span data-stu-id="8cdcb-132">**GetSurfaceLevel**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel)

<span data-ttu-id="8cdcb-133">[**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)介面可讓您透過 [**UpdateSurface**](/windows/desktop/api)方法間接存取記憶體。</span><span class="sxs-lookup"><span data-stu-id="8cdcb-133">The [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface enables you to indirectly access memory through the [**UpdateSurface**](/windows/desktop/api) method.</span></span> <span data-ttu-id="8cdcb-134">這個方法可讓您從一個 **IDirect3DSurface9** 介面，將一個圖元的矩形區域複製到另一個 **IDirect3DSurface9** 介面。</span><span class="sxs-lookup"><span data-stu-id="8cdcb-134">This method allows you to copy a rectangular region of pixels from one **IDirect3DSurface9** interface to another **IDirect3DSurface9** interface.</span></span> <span data-ttu-id="8cdcb-135">介面介面也有可直接存取顯示記憶體的方法。</span><span class="sxs-lookup"><span data-stu-id="8cdcb-135">The surface interface also has methods to directly access display memory.</span></span> <span data-ttu-id="8cdcb-136">例如，您可以使用 [**LockRect**](/windows/desktop/api) 方法來鎖定顯示記憶體的矩形區域。</span><span class="sxs-lookup"><span data-stu-id="8cdcb-136">For example, you can use the [**LockRect**](/windows/desktop/api) method to lock a rectangular region of display memory.</span></span> <span data-ttu-id="8cdcb-137">在表面上使用鎖定的矩形區域完成之後，請務必呼叫 [**UnlockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-unlockrect) 。</span><span class="sxs-lookup"><span data-stu-id="8cdcb-137">It is important to call [**UnlockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-unlockrect) after you are done working with the locked rectangular region on the surface.</span></span>

## <a name="additional-surface-topics"></a><span data-ttu-id="8cdcb-138">其他表面主題</span><span class="sxs-lookup"><span data-stu-id="8cdcb-138">Additional Surface Topics</span></span>

<span data-ttu-id="8cdcb-139">深入瞭解如何搭配下列任何主題使用介面：</span><span class="sxs-lookup"><span data-stu-id="8cdcb-139">Find out more about how to use surfaces with any of these topics:</span></span>

-   [<span data-ttu-id="8cdcb-140"> (Direct3D 9) 的表面格式 </span><span class="sxs-lookup"><span data-stu-id="8cdcb-140">Surface Formats (Direct3D 9)</span></span>](surface-formats.md)
-   [<span data-ttu-id="8cdcb-141">什麼是交換鏈？ (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="8cdcb-141">What Is a Swap Chain? (Direct3D 9)</span></span>](what-is-a-swap-chain-.md)
-   [<span data-ttu-id="8cdcb-142">寬度與音調 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="8cdcb-142">Width vs. Pitch (Direct3D 9)</span></span>](width-vs--pitch.md)
-   [<span data-ttu-id="8cdcb-143"> (Direct3D 9 中翻轉表面) </span><span class="sxs-lookup"><span data-stu-id="8cdcb-143">Flipping Surfaces (Direct3D 9)</span></span>](flipping-surfaces.md)
-   [<span data-ttu-id="8cdcb-144"> (Direct3D 9 的頁面翻轉和後臺緩衝) </span><span class="sxs-lookup"><span data-stu-id="8cdcb-144">Page Flipping and Back Buffering (Direct3D 9)</span></span>](page-flipping-and-back-buffering.md)
-   [<span data-ttu-id="8cdcb-145">複製到 (Direct3D 9) 的表面 </span><span class="sxs-lookup"><span data-stu-id="8cdcb-145">Copying to Surfaces (Direct3D 9)</span></span>](copying-to-surfaces.md)
-   [<span data-ttu-id="8cdcb-146"> (Direct3D 9) 複製表面 </span><span class="sxs-lookup"><span data-stu-id="8cdcb-146">Copying Surfaces (Direct3D 9)</span></span>](copying-surfaces.md)
-   [<span data-ttu-id="8cdcb-147">直接存取 (Direct3D 9) 的介面記憶體 </span><span class="sxs-lookup"><span data-stu-id="8cdcb-147">Accessing Surface Memory Directly (Direct3D 9)</span></span>](accessing-surface-memory-directly.md)
-   [<span data-ttu-id="8cdcb-148">私用介面資料 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="8cdcb-148">Private Surface Data (Direct3D 9)</span></span>](private-surface-data.md)
-   [<span data-ttu-id="8cdcb-149"> (Direct3D 9) 的 Gamma 控制項 </span><span class="sxs-lookup"><span data-stu-id="8cdcb-149">Gamma Controls (Direct3D 9)</span></span>](gamma-controls.md)

## <a name="related-topics"></a><span data-ttu-id="8cdcb-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="8cdcb-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cdcb-151">快速入門</span><span class="sxs-lookup"><span data-stu-id="8cdcb-151">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 

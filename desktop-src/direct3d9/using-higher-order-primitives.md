---
description: 本節說明如何在您的應用程式中使用較高順序的基本專案。
ms.assetid: 7aa4f3ab-cfce-4f8f-a538-384f038fd324
title: '使用 Higher-Order 基本 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8d1447635c38e5e5df3d16ebca5ee3ee142020
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104553216"
---
# <a name="using-higher-order-primitives-direct3d-9"></a><span data-ttu-id="d2ebf-103">使用 Higher-Order 基本 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="d2ebf-103">Using Higher-Order Primitives (Direct3D 9)</span></span>

<span data-ttu-id="d2ebf-104">本節說明如何在您的應用程式中使用較高順序的基本專案。</span><span class="sxs-lookup"><span data-stu-id="d2ebf-104">This section shows you how to use higher-order primitives in your application.</span></span>

-   [<span data-ttu-id="d2ebf-105">判斷 Higher-Order 基本支援</span><span class="sxs-lookup"><span data-stu-id="d2ebf-105">Determining Higher-Order Primitive Support</span></span>](#determining-higher-order-primitive-support)
-   [<span data-ttu-id="d2ebf-106">繪圖修補程式</span><span class="sxs-lookup"><span data-stu-id="d2ebf-106">Drawing Patches</span></span>](#drawing-patches)
-   [<span data-ttu-id="d2ebf-107">產生法線和材質座標</span><span class="sxs-lookup"><span data-stu-id="d2ebf-107">Generating Normals and Texture Coordinates</span></span>](#generating-normals-and-texture-coordinates)

## <a name="determining-higher-order-primitive-support"></a><span data-ttu-id="d2ebf-108">判斷 Higher-Order 基本支援</span><span class="sxs-lookup"><span data-stu-id="d2ebf-108">Determining Higher-Order Primitive Support</span></span>

<span data-ttu-id="d2ebf-109">您可以查詢 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 結構的 DevCaps 成員，以判斷涉及較高訂單基本專案之作業的支援層級。</span><span class="sxs-lookup"><span data-stu-id="d2ebf-109">The [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure's DevCaps member can be queried to determine the level of support for operations involving higher-order primitives.</span></span> <span data-ttu-id="d2ebf-110">下表列出 Direct3D 9 中與較高順序基本專案相關的裝置功能。</span><span class="sxs-lookup"><span data-stu-id="d2ebf-110">The following table lists the device capabilities related to higher-order primitives in Direct3D 9.</span></span>



| <span data-ttu-id="d2ebf-111">裝置功能</span><span class="sxs-lookup"><span data-stu-id="d2ebf-111">Device capability</span></span>             | <span data-ttu-id="d2ebf-112">Description</span><span class="sxs-lookup"><span data-stu-id="d2ebf-112">Description</span></span>                                                                                                                                                  |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2ebf-113">D3DDEVCAPS \_ NPATCHES</span><span class="sxs-lookup"><span data-stu-id="d2ebf-113">D3DDEVCAPS\_NPATCHES</span></span>          | <span data-ttu-id="d2ebf-114">裝置支援 N 個修補程式，並根據 [曲線的 PN 三角形](https://alex.vlachos.com/graphics/CurvedPNTriangles.pdf) (一種特殊的三次貝塞爾三角形) 。</span><span class="sxs-lookup"><span data-stu-id="d2ebf-114">Device supports N-patches and is based on [Curved PN Triangles](https://alex.vlachos.com/graphics/CurvedPNTriangles.pdf) (a special kind of cubic Bézier triangles).</span></span> |
| <span data-ttu-id="d2ebf-115">D3DDEVCAPS \_ QUINTICRTPATCHES</span><span class="sxs-lookup"><span data-stu-id="d2ebf-115">D3DDEVCAPS\_QUINTICRTPATCHES</span></span>  | <span data-ttu-id="d2ebf-116">裝置支援 quintic 貝茲曲線和 B 曲線。</span><span class="sxs-lookup"><span data-stu-id="d2ebf-116">Device supports quintic Bezier curves and B-splines.</span></span>                                                                                                         |
| <span data-ttu-id="d2ebf-117">D3DDEVCAPS \_ RTPATCHES</span><span class="sxs-lookup"><span data-stu-id="d2ebf-117">D3DDEVCAPS\_RTPATCHES</span></span>         | <span data-ttu-id="d2ebf-118">裝置支援 (RT-修補程式) 的矩形和三角形修補程式。</span><span class="sxs-lookup"><span data-stu-id="d2ebf-118">Device supports rectangular and triangular patches (RT-patches).</span></span>                                                                                             |
| <span data-ttu-id="d2ebf-119">D3DDEVCAPS \_ RTPATCHHANDLEZERO</span><span class="sxs-lookup"><span data-stu-id="d2ebf-119">D3DDEVCAPS\_RTPATCHHANDLEZERO</span></span> | <span data-ttu-id="d2ebf-120">RT-修補程式可能會使用控制碼零來有效率地繪製。</span><span class="sxs-lookup"><span data-stu-id="d2ebf-120">RT-patches might be drawn efficiently using handle zero.</span></span>                                                                                                     |



 

<span data-ttu-id="d2ebf-121">請注意，D3DDEVCAPS \_ RTPATCHHANDLEZERO 並不表示可以繪製控制碼為零的修補程式。</span><span class="sxs-lookup"><span data-stu-id="d2ebf-121">Note that D3DDEVCAPS\_RTPATCHHANDLEZERO does not mean that a patch with handle zero can be drawn.</span></span> <span data-ttu-id="d2ebf-122">不論是否已設定此裝置功能，都可以繪製控制碼零修補程式。</span><span class="sxs-lookup"><span data-stu-id="d2ebf-122">A handle zero patch can always be drawn, whether this device capability is set or not.</span></span> <span data-ttu-id="d2ebf-123">當設定這項功能時，硬體架構不需要快取任何資訊，且未快取的修補程式 (處理零) 會以快取的方式有效率地繪製。</span><span class="sxs-lookup"><span data-stu-id="d2ebf-123">When this capability is set, the hardware architecture does not require caching of any information and that uncached patches (handle zero) be drawn as efficiently as cached ones.</span></span>

## <a name="drawing-patches"></a><span data-ttu-id="d2ebf-124">繪圖修補程式</span><span class="sxs-lookup"><span data-stu-id="d2ebf-124">Drawing Patches</span></span>

<span data-ttu-id="d2ebf-125">Direct3D 9 支援兩種類型的高序位基本專案或修補程式。</span><span class="sxs-lookup"><span data-stu-id="d2ebf-125">Direct3D 9 supports two types of higher-order primitives, or patches.</span></span> <span data-ttu-id="d2ebf-126">這些稱為 N 修補程式和 Rect/三個修補程式。</span><span class="sxs-lookup"><span data-stu-id="d2ebf-126">These are referred to as N-Patches and Rect/Tri patches.</span></span> <span data-ttu-id="d2ebf-127">N 修補程式可以使用任何三角形轉譯呼叫來呈現，方法是透過呼叫 [**IDirect3DDevice9：： SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) ( nSegments ) ，其 nSegments 值大於1.0。</span><span class="sxs-lookup"><span data-stu-id="d2ebf-127">N-patches can be rendered using any triangle rendering call by enabling N-patches through the call to [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode)( nSegments ) with nSegments value greater than 1.0.</span></span> <span data-ttu-id="d2ebf-128">Rect/三個修補程式必須使用下列明確的進入點來呈現。</span><span class="sxs-lookup"><span data-stu-id="d2ebf-128">Rect/Tri patches must be rendered using the following explicit entry points.</span></span>

<span data-ttu-id="d2ebf-129">您可以使用下列方法來繪製修補程式。</span><span class="sxs-lookup"><span data-stu-id="d2ebf-129">You can use the following methods to draw patches.</span></span>

-   <span data-ttu-id="d2ebf-130">[**IDirect3DDevice9：:D rawrectpatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch)。</span><span class="sxs-lookup"><span data-stu-id="d2ebf-130">[**IDirect3DDevice9::DrawRectPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch).</span></span> <span data-ttu-id="d2ebf-131">若要進一步瞭解如何在頂點緩衝區中參考修補程式資料，請參閱 [**D3DRECTPATCH \_ 資訊**](d3drectpatch-info.md)。</span><span class="sxs-lookup"><span data-stu-id="d2ebf-131">To better understand how the patch data is referenced in the vertex buffer, see [**D3DRECTPATCH\_INFO**](d3drectpatch-info.md).</span></span>
-   <span data-ttu-id="d2ebf-132">[**IDirect3DDevice9：:D rawtripatch**](/windows/desktop/api)。</span><span class="sxs-lookup"><span data-stu-id="d2ebf-132">[**IDirect3DDevice9::DrawTriPatch**](/windows/desktop/api).</span></span> <span data-ttu-id="d2ebf-133">若要進一步瞭解如何在頂點緩衝區中參考修補程式資料，請參閱 [**D3DTRIPATCH \_ 資訊**](d3dtripatch-info.md)。</span><span class="sxs-lookup"><span data-stu-id="d2ebf-133">To better understand how the patch data is referenced in the vertex buffer, see [**D3DTRIPATCH\_INFO**](d3dtripatch-info.md).</span></span>

<span data-ttu-id="d2ebf-134">[**IDirect3DDevice9：:D rawrectpatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch) 會使用目前設定的資料流程，繪製 pRectPatchInfo 參數所指定的矩形高序位修補程式。</span><span class="sxs-lookup"><span data-stu-id="d2ebf-134">[**IDirect3DDevice9::DrawRectPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch) draws a rectangular high-order patch specified by the pRectPatchInfo parameter using the currently set streams.</span></span> <span data-ttu-id="d2ebf-135">控制碼參數是用來將修補程式關聯至控制碼，因此下次繪製修補程式時，不需要重新指定 pRectPatchInfo。</span><span class="sxs-lookup"><span data-stu-id="d2ebf-135">The Handle parameter is used to associate the patch with a handle, so that the next time the patch is drawn, there is no need to respecify pRectPatchInfo.</span></span> <span data-ttu-id="d2ebf-136">如此一來，就可以預先計算和快取向前差異係數或其他資訊，進而讓後續呼叫 IDirect3DDevice9：使用相同的控制碼有效率地執行 **：:D rawrectpatch** 。</span><span class="sxs-lookup"><span data-stu-id="d2ebf-136">This makes it possible to precompute and cache forward difference coefficients or other information, which in turn enables subsequent calls to **IDirect3DDevice9::DrawRectPatch** using the same handle to run efficiently.</span></span>

<span data-ttu-id="d2ebf-137">它適用于靜態修補程式，應用程式會設定頂點著色器和適當的資料流程、在 pRectPatchInfo 參數中提供修補程式資訊，以及指定一個控制碼，讓 Direct3D 可以捕獲和快取資訊。</span><span class="sxs-lookup"><span data-stu-id="d2ebf-137">It is intended that for static patches, an application would set the vertex shader and appropriate streams, supply patch information in the pRectPatchInfo parameter, and specify a handle so that Direct3D can capture and cache information.</span></span> <span data-ttu-id="d2ebf-138">然後，應用程式可以呼叫 [**IDirect3DDevice9：:D rawrectpatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch) 接著將 pRectPatchInfo 設定為 **Null** ，以有效率地繪製修補程式。</span><span class="sxs-lookup"><span data-stu-id="d2ebf-138">The application can then call [**IDirect3DDevice9::DrawRectPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch) subsequently with pRectPatchInfo set to **NULL** to efficiently draw the patch.</span></span> <span data-ttu-id="d2ebf-139">繪製快取的修補程式時，會忽略目前設定的資料流程。</span><span class="sxs-lookup"><span data-stu-id="d2ebf-139">When drawing a cached patch, the currently set streams are ignored.</span></span> <span data-ttu-id="d2ebf-140">不過，您可以藉由指定 pNumSegs 的新值來覆寫快取的 pNumSegs。</span><span class="sxs-lookup"><span data-stu-id="d2ebf-140">However, it is possible to override the cached pNumSegs by specifying new values for pNumSegs.</span></span> <span data-ttu-id="d2ebf-141">此外，在轉譯快取的修補程式時，也必須設定相同的頂點著色器（當它被捕捉時所設定）。</span><span class="sxs-lookup"><span data-stu-id="d2ebf-141">Also, it is required to set the same vertex shader when rendering a cached patch as was set when it was captured.</span></span>

<span data-ttu-id="d2ebf-142">若為動態修補程式，修補程式資料會隨著修補程式的每個轉譯而變更，因此快取資訊的效率並不高。</span><span class="sxs-lookup"><span data-stu-id="d2ebf-142">For dynamic patches, the patch data changes for every rendering of the patch, so it is not efficient to cache information.</span></span> <span data-ttu-id="d2ebf-143">應用程式可以將控制碼設定為0，以將此傳遞給 Direct3D。</span><span class="sxs-lookup"><span data-stu-id="d2ebf-143">The application can convey this to Direct3D by setting Handle to 0.</span></span> <span data-ttu-id="d2ebf-144">在此情況下，Direct3D 會使用目前設定的資料流程和 pNumSegs 值來繪製修補程式，而不會快取任何資訊。</span><span class="sxs-lookup"><span data-stu-id="d2ebf-144">In this case, Direct3D draws the patch using the currently set streams and the pNumSegs values and does not cache any information.</span></span> <span data-ttu-id="d2ebf-145">同時將控制碼設定為0，並將 pPatch 設定為 **Null**，是不正確。</span><span class="sxs-lookup"><span data-stu-id="d2ebf-145">It is not valid to simultaneously set Handle to 0 and pPatch to **NULL**.</span></span>

<span data-ttu-id="d2ebf-146">藉由針對相同的控制碼 respecifying pRectPatchInfo，應用程式可以覆寫先前快取的資訊。</span><span class="sxs-lookup"><span data-stu-id="d2ebf-146">By respecifying pRectPatchInfo for the same handle, the application can overwrite the previously cached information.</span></span>

<span data-ttu-id="d2ebf-147">[**IDirect3DDevice9：:D rawtripatch**](/windows/desktop/api) 與 [**IDirect3DDevice9：:D rawrectpatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch) 類似，不同之處在于它會繪製三角形的高序位修補程式。</span><span class="sxs-lookup"><span data-stu-id="d2ebf-147">[**IDirect3DDevice9::DrawTriPatch**](/windows/desktop/api) is similar to [**IDirect3DDevice9::DrawRectPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch) except that it draws a triangular high-order patch.</span></span>

## <a name="generating-normals-and-texture-coordinates"></a><span data-ttu-id="d2ebf-148">產生法線和材質座標</span><span class="sxs-lookup"><span data-stu-id="d2ebf-148">Generating Normals and Texture Coordinates</span></span>

<span data-ttu-id="d2ebf-149">如果您使用彈性頂點格式 (FVF) 著色器，就無法自動產生法線和材質座標。</span><span class="sxs-lookup"><span data-stu-id="d2ebf-149">If you are using a flexible vertex format (FVF) shader, automatic generation of normals and texture coordinates is not possible.</span></span>

<span data-ttu-id="d2ebf-150">針對法線，您可以直接提供它們，或讓 Direct3D 為您計算。</span><span class="sxs-lookup"><span data-stu-id="d2ebf-150">For normals, you can either directly supply them or have Direct3D calculate them for you.</span></span>

<span data-ttu-id="d2ebf-151">針對矩形修補程式產生的座標是以曲線為基礎的座標，如下列圖例所示。</span><span class="sxs-lookup"><span data-stu-id="d2ebf-151">The coordinates generated for rectangular patches are spline-based coordinates, as shown in the following illustrations.</span></span>

![使用以曲線為基礎之座標的原始材質和材質圖例](images/texturespline.png)

<span data-ttu-id="d2ebf-153">為三角形修補程式產生的座標是以 barycentric 曲線為基礎的座標，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="d2ebf-153">The coordinates generated for triangular patches are barycentric spline-based coordinates, as shown in the following illustrations.</span></span>

![使用 barycentric 曲線座標的原始材質和材質圖例](images/texturebarycentricspline.png)

<span data-ttu-id="d2ebf-155">如果應用程式必須變更產生的材質座標範圍，則可以使用材質轉換來完成。</span><span class="sxs-lookup"><span data-stu-id="d2ebf-155">If an application must change the range of the generated texture coordinates, this can be done using texture transforms.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2ebf-156">相關主題</span><span class="sxs-lookup"><span data-stu-id="d2ebf-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2ebf-157">較高順序的基本專案</span><span class="sxs-lookup"><span data-stu-id="d2ebf-157">Higher-Order Primitives</span></span>](higher-order-primitives.md)
</dt> </dl>

 

 

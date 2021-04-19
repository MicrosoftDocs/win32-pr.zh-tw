---
description: 本檔特別提到適用于 DirectX 圖形的 Windows Vista 擴充功能。
ms.assetid: 3cc0b08c-e126-4f1b-b5d1-0d6c1ebeb0c5
title: Windows Vista) 的功能摘要 (Direct3D 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d5cf2447297b7f24edf7d0200e640d5aef90bff
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970692"
---
# <a name="feature-summary-direct3d-9-for-windows-vista"></a><span data-ttu-id="defc0-103">Windows Vista) 的功能摘要 (Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="defc0-103">Feature Summary (Direct3D 9 for Windows Vista)</span></span>

<span data-ttu-id="defc0-104">本檔特別提到適用于 DirectX 圖形的 Windows Vista 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="defc0-104">This documentation specifically refers to the Windows Vista extensions for DirectX graphics.</span></span> <span data-ttu-id="defc0-105">若要開發 Windows Vista 的 DirectX 功能，您必須安裝 Windows Vista SDK 和 DirectX SDK。</span><span class="sxs-lookup"><span data-stu-id="defc0-105">To develop the power of DirectX for Windows Vista, you must install the Windows Vista SDK as well as the DirectX SDK.</span></span> <span data-ttu-id="defc0-106">使用適用于 Windows Vista 的 DirectX 的應用程式必須使用使用 WDDM 驅動程式 (Windows 設備磁碟機模型) 而非 (XP 驅動程式模型) ;未執行 WDDM 的驅動程式無法具現化 Windows Vista DirectX 圖形介面。</span><span class="sxs-lookup"><span data-stu-id="defc0-106">Applications using DirectX for Windows Vista must be using hardware that uses the WDDM driver (Windows Device Driver Model) as opposed to the XPDM (XP Driver Model); drivers that do not implement the WDDM cannot instantiate Windows Vista DirectX graphics interfaces.</span></span>

<span data-ttu-id="defc0-107">在下列其中一節中探索 Windows Vista 的新 DirectX 圖形功能：</span><span class="sxs-lookup"><span data-stu-id="defc0-107">Discover the new DirectX graphics features in Windows Vista in one of these sections:</span></span>

-   [<span data-ttu-id="defc0-108">裝置行為變更</span><span class="sxs-lookup"><span data-stu-id="defc0-108">Device Behavior Changes</span></span>](#device-behavior-changes)
-   [<span data-ttu-id="defc0-109">停用多執行緒軟體頂點處理</span><span class="sxs-lookup"><span data-stu-id="defc0-109">Disabling Multithreaded Software Vertex Processing</span></span>](#disabling-multithreaded-software-vertex-processing)
-   [<span data-ttu-id="defc0-110">一個位表面</span><span class="sxs-lookup"><span data-stu-id="defc0-110">One Bit Surfaces</span></span>](#one-bit-surfaces)
-   [<span data-ttu-id="defc0-111">讀取深度/樣板緩衝區</span><span class="sxs-lookup"><span data-stu-id="defc0-111">Reading Depth/Stencil Buffers</span></span>](#reading-depthstencil-buffers)
-   [<span data-ttu-id="defc0-112">共用資源</span><span class="sxs-lookup"><span data-stu-id="defc0-112">Sharing Resources</span></span>](#sharing-resources)
-   [<span data-ttu-id="defc0-113">混合之前的 sRGB 轉換</span><span class="sxs-lookup"><span data-stu-id="defc0-113">sRGB Conversion Before Blending</span></span>](#srgb-conversion-before-blending)
-   [<span data-ttu-id="defc0-114">StretchRect 改進</span><span class="sxs-lookup"><span data-stu-id="defc0-114">StretchRect Improvements</span></span>](#stretchrect-improvements)
-   [<span data-ttu-id="defc0-115">系統記憶體中的材質建立</span><span class="sxs-lookup"><span data-stu-id="defc0-115">Texture Creation in System Memory</span></span>](#texture-creation-in-system-memory)

## <a name="device-behavior-changes"></a><span data-ttu-id="defc0-116">裝置行為變更</span><span class="sxs-lookup"><span data-stu-id="defc0-116">Device Behavior Changes</span></span>

<span data-ttu-id="defc0-117">裝置現在只會在兩個情況下遺失;當硬體因為停止運作而重設時，以及設備磁碟機停止時。</span><span class="sxs-lookup"><span data-stu-id="defc0-117">Devices are now only lost under two circumstances; when the hardware is reset because it is hanging, and when the device driver is stopped.</span></span> <span data-ttu-id="defc0-118">當硬體停止回應時，可以藉由呼叫 [**ResetEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex)來重設裝置。</span><span class="sxs-lookup"><span data-stu-id="defc0-118">When hardware hangs, the device can be reset by calling [**ResetEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex).</span></span> <span data-ttu-id="defc0-119">如果硬體停止回應，則會遺失紋理記憶體。</span><span class="sxs-lookup"><span data-stu-id="defc0-119">If hardware hangs, texture memory is lost.</span></span>

<span data-ttu-id="defc0-120">停止驅動程式之後，必須重新建立 IDirect9Ex 物件才能繼續轉譯。</span><span class="sxs-lookup"><span data-stu-id="defc0-120">After a driver is stopped, the IDirect9Ex object must be recreated to resume rendering.</span></span>

<span data-ttu-id="defc0-121">當視窗模式中的另一個視窗隱藏表示區，或將全螢幕應用程式最小化時， [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) 會傳回 S \_ D3DPRESENTATIONOCCLUDED。</span><span class="sxs-lookup"><span data-stu-id="defc0-121">When the presentation area is obscured by another window in windowed mode, or when a fullscreen application is minimized, [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) will return S\_D3DPRESENTATIONOCCLUDED.</span></span> <span data-ttu-id="defc0-122">全螢幕應用程式可在收到 [**WM \_ ACTI加值稅EAPP**](../winmsg/wm-activateapp.md) 回呼訊息時繼續呈現。</span><span class="sxs-lookup"><span data-stu-id="defc0-122">Full screen applications can resume rendering when they receive a [**WM\_ACTIVATEAPP**](../winmsg/wm-activateapp.md) callback message.</span></span>

<span data-ttu-id="defc0-123">在舊版 DirectX 中，當應用程式發生模式變更時，復原的唯一方法是重設裝置，並重新建立所有的視訊記憶體資源和交換鏈。</span><span class="sxs-lookup"><span data-stu-id="defc0-123">In previous versions of DirectX, when an application experienced a mode change, the only way to recover was to reset the device and re-create all video memory resources and swap chains.</span></span> <span data-ttu-id="defc0-124">現在有了適用于 Windows Vista 的 DirectX，在模式變更之後呼叫 Reset，並不會造成材質記憶體表面、材質和狀態資訊遺失，也不需要重新建立這些資源。</span><span class="sxs-lookup"><span data-stu-id="defc0-124">Now with DirectX for Windows Vista, calling Reset after a mode change does not cause texture memory surfaces, textures and state information to be lost and these resources do not need to be recreated.</span></span>

## <a name="disabling-multithreaded-software-vertex-processing"></a><span data-ttu-id="defc0-125">停用多執行緒軟體頂點處理</span><span class="sxs-lookup"><span data-stu-id="defc0-125">Disabling Multithreaded Software Vertex Processing</span></span>

<span data-ttu-id="defc0-126">新的 cap 位 (D3DCREATE \_ 停用 \_ PSGP \_ 執行緒) 已加入，將會停用 (swvp) 之軟體頂點處理的多執行緒處理。</span><span class="sxs-lookup"><span data-stu-id="defc0-126">A new caps bit (D3DCREATE\_DISABLE\_PSGP\_THREADING) has been added that will disable multithreading for software vertex processing (swvp).</span></span> <span data-ttu-id="defc0-127">使用此宏來產生 IDirect3D9：： CreateDevice 的行為旗標。</span><span class="sxs-lookup"><span data-stu-id="defc0-127">Use this macro to generate a behavior flag for IDirect3D9::CreateDevice.</span></span>


```
#define D3DCREATE_DISABLE_PSGP_THREADING
```



## <a name="one-bit-surfaces"></a><span data-ttu-id="defc0-128">一個位表面</span><span class="sxs-lookup"><span data-stu-id="defc0-128">One Bit Surfaces</span></span>

<span data-ttu-id="defc0-129">有一個新的 bit 介面格式類型，特別適合用來處理文字字元。</span><span class="sxs-lookup"><span data-stu-id="defc0-129">There is a new one bit surface format type which can be especially useful for processing text glyphs.</span></span> <span data-ttu-id="defc0-130">新的格式稱為 D3DFMT \_ A1。</span><span class="sxs-lookup"><span data-stu-id="defc0-130">The new format is called D3DFMT\_A1.</span></span> <span data-ttu-id="defc0-131">一個位介面是設計用來作為個別圖元材質，或是 ComposeRects 或 ColorFill 所產生的轉譯目標輸出。</span><span class="sxs-lookup"><span data-stu-id="defc0-131">A one-bit surface is designed to be either used as a per-pixel texture, or the render target output generated by ComposeRects or ColorFill.</span></span> <span data-ttu-id="defc0-132">表面寬度和高度沒有個別的帽;實作為必須支援2K 材質 x 8K 材質的單一大小介面。</span><span class="sxs-lookup"><span data-stu-id="defc0-132">There are no separate caps for the surface width and height; an implementation must support a single size surface that is 2K texels x 8K texels.</span></span>

<span data-ttu-id="defc0-133">每個材質都有一個位介面;因此，其中一個表示所有元件 (r、g、b、圖元的) 為1，而零則表示所有的元件都等於0。</span><span class="sxs-lookup"><span data-stu-id="defc0-133">A one-bit surface has one bit per texel; therefore, a one would mean that all components (r,g,b,a) of a pixel are 1, and zero would mean that all components are equal to 0.</span></span> <span data-ttu-id="defc0-134">您可以搭配下列 Api 使用一個位介面： ColorFill、UpdateSurface 和 UpdateTexture。</span><span class="sxs-lookup"><span data-stu-id="defc0-134">You may use one-bit surfaces with the following APIs: ColorFill, UpdateSurface and UpdateTexture.</span></span>

<span data-ttu-id="defc0-135">當某個位介面被讀取時，執行時間可以執行 point 樣本或卷積篩選。</span><span class="sxs-lookup"><span data-stu-id="defc0-135">When a one-bit surface is read, the runtime can perform either point sample or convolution filtering.</span></span> <span data-ttu-id="defc0-136">您可以調整卷積篩選 (查看 [**SetConvolutionMonoKernel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-setconvolutionmonokernel)) 。</span><span class="sxs-lookup"><span data-stu-id="defc0-136">The convolution filter is adjustable (see [**SetConvolutionMonoKernel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-setconvolutionmonokernel)).</span></span>

<span data-ttu-id="defc0-137">一個位介面有一些限制：</span><span class="sxs-lookup"><span data-stu-id="defc0-137">There are some restrictions for one-bit surfaces:</span></span>

-   <span data-ttu-id="defc0-138">Mip-不支援對應</span><span class="sxs-lookup"><span data-stu-id="defc0-138">Mip-mapping is not supported</span></span>
-   <span data-ttu-id="defc0-139">sRGB 資料無法讀取或寫入至單一位介面。</span><span class="sxs-lookup"><span data-stu-id="defc0-139">sRGB data cannot be read or written to a one-bit surface.</span></span>
-   <span data-ttu-id="defc0-140">一個位介面不能當做頂點材質或用於交叉取樣。</span><span class="sxs-lookup"><span data-stu-id="defc0-140">A one-bit surface cannot be used as a vertex texture or for multisampling.</span></span>

## <a name="reading-depthstencil-buffers"></a><span data-ttu-id="defc0-141">讀取深度/樣板緩衝區</span><span class="sxs-lookup"><span data-stu-id="defc0-141">Reading Depth/Stencil Buffers</span></span>

<span data-ttu-id="defc0-142">使用 IDirect3DDevice9：： UpdateSurface 來讀取或寫入從 IDirect3DDevice9：： CreateDepthStencilSurface 或 IDirect3DDevice9：： GetDepthStencilSurface 取得之表面的深度/樣板資料。</span><span class="sxs-lookup"><span data-stu-id="defc0-142">Use IDirect3DDevice9::UpdateSurface to read or write depth/stencil data from surfaces obtained from IDirect3DDevice9::CreateDepthStencilSurface or IDirect3DDevice9::GetDepthStencilSurface.</span></span>

<span data-ttu-id="defc0-143">首先，使用 IDirect3DDevice9：： CreateOffscreenPlainSurface 建立僅限「鎖定」、「僅深度」或「僅樣板」介面。</span><span class="sxs-lookup"><span data-stu-id="defc0-143">First, create a lockable, depth only or stencil only surface using IDirect3DDevice9::CreateOffscreenPlainSurface.</span></span> <span data-ttu-id="defc0-144">請使用下列其中一個格式：</span><span class="sxs-lookup"><span data-stu-id="defc0-144">Use one of the following formats:</span></span>

-   <span data-ttu-id="defc0-145">D3DFMT \_ D16 的 \_ 鎖定</span><span class="sxs-lookup"><span data-stu-id="defc0-145">D3DFMT\_D16\_LOCKABLE</span></span>
-   <span data-ttu-id="defc0-146">D3DFMT \_ D32F 的 \_ 鎖定</span><span class="sxs-lookup"><span data-stu-id="defc0-146">D3DFMT\_D32F\_LOCKABLE</span></span>
-   <span data-ttu-id="defc0-147">D3DFMT \_ D32 的 \_ 鎖定</span><span class="sxs-lookup"><span data-stu-id="defc0-147">D3DFMT\_D32\_LOCKABLE</span></span>
-   <span data-ttu-id="defc0-148">D3DFMT \_ S8 的 \_ 鎖定</span><span class="sxs-lookup"><span data-stu-id="defc0-148">D3DFMT\_S8\_LOCKABLE</span></span>

<span data-ttu-id="defc0-149">其次，在深度/樣板緩衝區和新建立的「鎖定深度」或「樣板介面」之間傳輸資料。</span><span class="sxs-lookup"><span data-stu-id="defc0-149">Second, transfer data between the depth/stencil buffer and the newly-created lockable depth or stencil surface.</span></span> <span data-ttu-id="defc0-150">此傳輸會使用 IDirect3DDevice9：： UpdateSurface 來執行。</span><span class="sxs-lookup"><span data-stu-id="defc0-150">The transfer is performed using IDirect3DDevice9::UpdateSurface.</span></span>

<span data-ttu-id="defc0-151">當兩個介面都是可鎖定的格式，或兩者都不是可鎖定時，UpdateSurface 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="defc0-151">UpdateSurface will fail when both surfaces are a LOCKABLE format or both are non-lockable.</span></span>

<span data-ttu-id="defc0-152">傳送不存在的資料會導致錯誤 (例如，從非可鎖定深度介面傳送到 D3DFMT \_ S8 可 \_ 鎖定的介面) 。</span><span class="sxs-lookup"><span data-stu-id="defc0-152">Transferring non-existent data will result in an error (for example, transferring from a non-lockable depth-only surface to a D3DFMT\_S8\_LOCKABLE surface).</span></span>

<span data-ttu-id="defc0-153">IDirect3DDevice9：： UpdateSurface 的其餘限制仍然適用。</span><span class="sxs-lookup"><span data-stu-id="defc0-153">The rest of the restrictions for IDirect3DDevice9::UpdateSurface still apply.</span></span>

## <a name="sharing-resources"></a><span data-ttu-id="defc0-154">共用資源</span><span class="sxs-lookup"><span data-stu-id="defc0-154">Sharing Resources</span></span>

<span data-ttu-id="defc0-155">Direct3D 資源現在可以在裝置或進程之間共用。</span><span class="sxs-lookup"><span data-stu-id="defc0-155">Direct3D resources can now be shared between devices or processes.</span></span> <span data-ttu-id="defc0-156">這適用于任何 Direct3D 資源，包括紋理、頂點緩衝區、索引緩衝區或介面 (例如轉譯目標、深度樣板緩衝區或螢幕一般表面) 。</span><span class="sxs-lookup"><span data-stu-id="defc0-156">This applies to any Direct3D resource including textures, vertex buffers, index buffers, or surfaces (such as render targets, depth stencil buffers or off-screen plain surfaces).</span></span> <span data-ttu-id="defc0-157">若要共用，您必須在建立時指定要共用的資源，並在預設集區中找出資源 (D3DPOOL \_ 預設) 。</span><span class="sxs-lookup"><span data-stu-id="defc0-157">To be shared, you need to designate a resource for sharing at the time of creation, and locate the resource in the default pool (D3DPOOL\_DEFAULT).</span></span> <span data-ttu-id="defc0-158">建立資源以供共用之後，就可以在程式內的所有裝置間共用，或在進程間共用。</span><span class="sxs-lookup"><span data-stu-id="defc0-158">Once a resource is created for sharing, it can be shared across devices within a process, or shared across processes.</span></span>

<span data-ttu-id="defc0-159">若要啟用共用資源，資源建立 Api 會有額外的控制碼參數。</span><span class="sxs-lookup"><span data-stu-id="defc0-159">To enable shared resources, the resource creation APIs have an additional handle parameter.</span></span> <span data-ttu-id="defc0-160">這是指向共用資源的控制碼。</span><span class="sxs-lookup"><span data-stu-id="defc0-160">This is a HANDLE that points to the shared resource.</span></span> <span data-ttu-id="defc0-161">在先前的 DirectX 版本中，此引數已是 API 簽章的一部分，但是未使用且必須設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="defc0-161">In previous revisions of DirectX, this argument has been part of the API signature, but has been unused and must be set to **NULL**.</span></span> <span data-ttu-id="defc0-162">從 Windows Vista 開始，請以下列方式使用 pSharedHandle：</span><span class="sxs-lookup"><span data-stu-id="defc0-162">Starting with Windows Vista, use pSharedHandle in the following ways:</span></span>

-   <span data-ttu-id="defc0-163">將指標 (pSharedHandle) 設定為 **Null** ，就不會共用資源。</span><span class="sxs-lookup"><span data-stu-id="defc0-163">Set the pointer (pSharedHandle) to **NULL** to not share a resource.</span></span> <span data-ttu-id="defc0-164">這就像是 Windows Vista 之前的 DirectX 行為。</span><span class="sxs-lookup"><span data-stu-id="defc0-164">This is just like the behavior of DirectX prior to Windows Vista.</span></span>
-   <span data-ttu-id="defc0-165">若要建立共用資源，請呼叫任何資源建立 API (查看下列) 使用未初始化的控制碼 (指標本身不是 **null** (pSharedHandle！ = **null**) ，但指標指向 **null** 值 (\* pSharedHandle = = **null**) ) 。</span><span class="sxs-lookup"><span data-stu-id="defc0-165">To create a shared resource, call any resource creation API (see below) with an uninitialized handle (the pointer itself is not **NULL** (pSharedHandle != **NULL**), but the pointer points to a **NULL** value (\*pSharedHandle == **NULL**)).</span></span> <span data-ttu-id="defc0-166">API 將會產生共用資源，並傳回有效的控制碼。</span><span class="sxs-lookup"><span data-stu-id="defc0-166">The API will generate a shared resource and return a valid handle.</span></span>
-   <span data-ttu-id="defc0-167">若要使用非 Null 共用資源控制碼來開啟和存取先前建立的共用資源，請將 pSharedHandle 設定為該控制碼的位址。</span><span class="sxs-lookup"><span data-stu-id="defc0-167">To open and access a previously created shared resource by using a nonNULL shared resource handle, set pSharedHandle to the address of that handle.</span></span> <span data-ttu-id="defc0-168">以這種方式開啟先前建立的共用資源之後，您可以在 Direct3D 9 或 Direct3D 9Ex API 中使用傳回的介面，如同介面是該類型的一般資源。</span><span class="sxs-lookup"><span data-stu-id="defc0-168">After you open the previously created shared resource in this manner, you can use the returned interface in the Direct3D 9 or Direct3D 9Ex API as if the interface were a typical resource of that type.</span></span>

<span data-ttu-id="defc0-169">資源建立 Api 包括- [**CreateTexture**](/windows/desktop/api)、 [**CreateVolumeTexture**](/windows/desktop/api)、 [**CreateCubeTexture**](/windows/desktop/api)、 [**CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)、 [**CreateVertexBuffer**](/windows/desktop/api)、 [**CreateIndexBuffer**](/windows/desktop/api)、 [**CreateDepthStencilSurface**](/windows/desktop/api)、 [**CreateOffscreenPlainSurface**](/windows/desktop/api)、 [**CreateDepthStencilSurfaceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createdepthstencilsurfaceex)、 [**CreateOffscreenPlainSurfaceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createoffscreenplainsurfaceex)和 [**CreateRenderTargetEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createrendertargetex)。</span><span class="sxs-lookup"><span data-stu-id="defc0-169">Resource creation APIs include - [**CreateTexture**](/windows/desktop/api), [**CreateVolumeTexture**](/windows/desktop/api), [**CreateCubeTexture**](/windows/desktop/api), [**CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget), [**CreateVertexBuffer**](/windows/desktop/api), [**CreateIndexBuffer**](/windows/desktop/api), [**CreateDepthStencilSurface**](/windows/desktop/api), [**CreateOffscreenPlainSurface**](/windows/desktop/api), [**CreateDepthStencilSurfaceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createdepthstencilsurfaceex), [**CreateOffscreenPlainSurfaceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createoffscreenplainsurfaceex), and [**CreateRenderTargetEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createrendertargetex).</span></span>

<span data-ttu-id="defc0-170">使用共用資源有一些限制。</span><span class="sxs-lookup"><span data-stu-id="defc0-170">There are some restrictions for using shared resources.</span></span> <span data-ttu-id="defc0-171">這些包括：</span><span class="sxs-lookup"><span data-stu-id="defc0-171">These include:</span></span>

-   <span data-ttu-id="defc0-172">您用來開啟共用資源的 API 必須符合您用來建立共用資源的 API。</span><span class="sxs-lookup"><span data-stu-id="defc0-172">The API that you use to open a shared resource must match the API that you used to create the shared resource.</span></span> <span data-ttu-id="defc0-173">例如，如果您使用 [**CreateTexture**](/windows/desktop/api) 來建立共用資源，就必須使用 **CreateTexture** 來開啟該共用資源;如果您使用 [**CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget) 來建立共用資源，就必須使用 **CreateRenderTarget** 來開啟該共用資源; 依此類推。</span><span class="sxs-lookup"><span data-stu-id="defc0-173">For example, if you used [**CreateTexture**](/windows/desktop/api) to create a shared resource, you must use **CreateTexture** to open that shared resource; if you used [**CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget) to create a shared resource, you must use **CreateRenderTarget** to open that shared resource;and so on.</span></span>
-   <span data-ttu-id="defc0-174">當您開啟共用資源時，您必須指定 D3DPOOL \_ 預設值。</span><span class="sxs-lookup"><span data-stu-id="defc0-174">When you open a shared resource, you must specify D3DPOOL\_DEFAULT.</span></span>
-   <span data-ttu-id="defc0-175">使用 D3DUSAGE \_ 動態、頂點緩衝區和索引緩衝區的可鎖定資源 (紋理，例如) 可能會在共用時遇到效能不佳的情況。</span><span class="sxs-lookup"><span data-stu-id="defc0-175">Lockable resources (textures with D3DUSAGE\_DYNAMIC, vertex buffers and index buffers, for instance) can experience poor performance when shared.</span></span> <span data-ttu-id="defc0-176">某些硬體上無法共用可鎖定的 rendertargets。</span><span class="sxs-lookup"><span data-stu-id="defc0-176">Lockable rendertargets will fail to be shared on some hardware.</span></span>
-   <span data-ttu-id="defc0-177">跨進程共用資源的參考必須與原始資源具有相同的維度。</span><span class="sxs-lookup"><span data-stu-id="defc0-177">References to a cross-process shared resource must have the same dimensions as the original resource.</span></span> <span data-ttu-id="defc0-178">當跨進程傳遞控制碼時，請包含維度資訊，如此就能以相同的方式建立參考。</span><span class="sxs-lookup"><span data-stu-id="defc0-178">When passing a handle across process, include the dimension information so that the reference can be created identically.</span></span>
-   <span data-ttu-id="defc0-179">共用的跨進程表面不提供同步處理機制。</span><span class="sxs-lookup"><span data-stu-id="defc0-179">Shared cross-process surfaces provide no synchronization mechanism.</span></span> <span data-ttu-id="defc0-180">對共用介面的讀取/寫入變更可能不會在預期的情況反映參考進程的外觀。</span><span class="sxs-lookup"><span data-stu-id="defc0-180">Read/write changes to a shared surface may not reflect a referencing process's view of the surface when expected.</span></span> <span data-ttu-id="defc0-181">若要提供同步處理，請使用事件查詢或鎖定紋理。</span><span class="sxs-lookup"><span data-stu-id="defc0-181">To provide synchronization, use event queries or lock the texture.</span></span>
-   <span data-ttu-id="defc0-182">只有一開始建立共用資源的進程才能將其鎖定 (任何開啟該共用資源參考的進程都無法將其鎖定) 。</span><span class="sxs-lookup"><span data-stu-id="defc0-182">Only the process that initially creates a shared resource can lock it (any process that opens a reference to that shared resource cannot lock it).</span></span>
-   <span data-ttu-id="defc0-183">如果共用資源已鎖定，其他進程就不會進行驗證，以得知資源是否可用。</span><span class="sxs-lookup"><span data-stu-id="defc0-183">If a shared resource is locked, there is no validation for other processes to know if the resource is available.</span></span>

## <a name="srgb-conversion-before-blending"></a><span data-ttu-id="defc0-184">混合之前的 sRGB 轉換</span><span class="sxs-lookup"><span data-stu-id="defc0-184">sRGB Conversion Before Blending</span></span>

<span data-ttu-id="defc0-185">您現在可以檢查裝置是否可以在框架緩衝區混合之前，將管線資料轉換成 sRGB。</span><span class="sxs-lookup"><span data-stu-id="defc0-185">You can now check to see if the device can convert pipeline data to sRGB before frame-buffer blending.</span></span> <span data-ttu-id="defc0-186">這表示裝置會從 sRGB 轉換轉譯目標值。</span><span class="sxs-lookup"><span data-stu-id="defc0-186">This implies that the device converts the render-target values from sRGB.</span></span> <span data-ttu-id="defc0-187">若要查看硬體是否支援轉換，請檢查此上限：</span><span class="sxs-lookup"><span data-stu-id="defc0-187">To see if conversion is supported by the hardware, check for this cap:</span></span>


```
D3DPMISCCAPS_POSTBLENDSRGBCONVERT
```



<span data-ttu-id="defc0-188">此端點會識別在混合之前支援轉換為 sRGB 的硬體。</span><span class="sxs-lookup"><span data-stu-id="defc0-188">This cap identifies hardware that supports conversion to sRGB before blending.</span></span> <span data-ttu-id="defc0-189">這項功能對於從桌面視窗管理員 fp16 框架緩衝區的高品質轉譯而言很重要， (DWM) 。</span><span class="sxs-lookup"><span data-stu-id="defc0-189">This capability is important for the high quality rendering from fp16 frame buffers in the desktop window manager (DWM).</span></span>

## <a name="stretchrect-improvements"></a><span data-ttu-id="defc0-190">StretchRect 改進</span><span class="sxs-lookup"><span data-stu-id="defc0-190">StretchRect Improvements</span></span>

<span data-ttu-id="defc0-191">在舊版的 DirectX 中，StretchRect 有許多限制來容納不同的驅動程式 (請參閱 IDirect3DDevice9：： StretchRect) 。</span><span class="sxs-lookup"><span data-stu-id="defc0-191">In previous versions of DirectX, StretchRect has many restrictions to accommodate different drivers (see IDirect3DDevice9::StretchRect).</span></span> <span data-ttu-id="defc0-192">Windows Vista 建基於 Windows 設備磁碟機模型 (WDDM) 。</span><span class="sxs-lookup"><span data-stu-id="defc0-192">Windows Vista is built on the Windows Device Driver Model (WDDM).</span></span> <span data-ttu-id="defc0-193">這個新的驅動程式模型更為穩固，而且可讓驅動程式處理硬體中的特殊情況。</span><span class="sxs-lookup"><span data-stu-id="defc0-193">This new driver model is much more robust, and allows drivers to handle special cases in the hardware.</span></span>

<span data-ttu-id="defc0-194">一般而言，唯一的限制是必須以轉譯目標使用方式建立轉譯目標 (D3DUSAGE \_ RENDERTARGET) 。</span><span class="sxs-lookup"><span data-stu-id="defc0-194">In general, the only remaining restriction is that the render target must have been created with render-target usage (D3DUSAGE\_RENDERTARGET).</span></span> <span data-ttu-id="defc0-195">如果您要執行簡單的複製 (，其中來源和目的地的格式相同，而且沒有子矩形) ，則會提高此限制。</span><span class="sxs-lookup"><span data-stu-id="defc0-195">This restriction is lifted if you are doing a simple copy (where the source and dest are the same format, same size and there are no sub-rectangles).</span></span>

## <a name="texture-creation-in-system-memory"></a><span data-ttu-id="defc0-196">系統記憶體中的材質建立</span><span class="sxs-lookup"><span data-stu-id="defc0-196">Texture Creation in System Memory</span></span>

<span data-ttu-id="defc0-197">在使用、配置和刪除系統記憶體時需要更多彈性的應用程式，現在可以從系統記憶體指標建立紋理。</span><span class="sxs-lookup"><span data-stu-id="defc0-197">Applications that need more flexibility over the use, allocation and deletion of the system memory can now create textures from a system memory pointer.</span></span> <span data-ttu-id="defc0-198">例如，應用程式可以從 GDI 系統記憶體點陣圖指標建立 Direct3D 材質。</span><span class="sxs-lookup"><span data-stu-id="defc0-198">For example, an application could create a Direct3D texture from a GDI system-memory bitmap pointer.</span></span>

<span data-ttu-id="defc0-199">您需要做兩件事來建立這類紋理：</span><span class="sxs-lookup"><span data-stu-id="defc0-199">You need to do two things to create such a texture:</span></span>

-   <span data-ttu-id="defc0-200">配置足夠的系統記憶體來保存材質介面。</span><span class="sxs-lookup"><span data-stu-id="defc0-200">Allocate enough system memory to hold the texture surface.</span></span> <span data-ttu-id="defc0-201">最小的位元組數目是每圖元的寬度 x 高度 x 位元組。</span><span class="sxs-lookup"><span data-stu-id="defc0-201">The minimum number of bytes is width x height x bytes per pixel.</span></span>
-   <span data-ttu-id="defc0-202">將控制碼參數的指標位址傳遞至 \* IDirect3DDevice9：： CreateTexture 的系統記憶體介面。</span><span class="sxs-lookup"><span data-stu-id="defc0-202">Pass the address of a pointer to your system memory surface for the HANDLE\* parameter to IDirect3DDevice9::CreateTexture.</span></span>

<span data-ttu-id="defc0-203">以下是 IDirect3DDevice9：： CreateTexture 的函式原型：</span><span class="sxs-lookup"><span data-stu-id="defc0-203">Here is the function prototype for IDirect3DDevice9::CreateTexture:</span></span>


```
STDMETHOD(CreateTexture)(THIS_ UINT Width, UINT Height, UINT Levels, 
    DWORD Usage, D3DFORMAT Format, D3DPOOL Pool, IDirect3DTexture9** ppTexture, 
    HANDLE* pSharedHandle)
```



<span data-ttu-id="defc0-204">系統記憶體材質有下列限制：</span><span class="sxs-lookup"><span data-stu-id="defc0-204">A system-memory texture has the following restrictions:</span></span>

-   <span data-ttu-id="defc0-205">材質間距必須等於材質寬度乘以每圖元的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="defc0-205">The texture pitch must equal texture width times the number of bytes per pixel.</span></span>
-   <span data-ttu-id="defc0-206">使用壓縮格式 (DXT 格式) 時，應用程式會負責配置正確的大小。</span><span class="sxs-lookup"><span data-stu-id="defc0-206">When using compressed formats (DXT formats), the application is responsible for allocating the correct size.</span></span>
-   <span data-ttu-id="defc0-207">僅支援具有單一 mipmap 層級的材質。</span><span class="sxs-lookup"><span data-stu-id="defc0-207">Only textures with a single mipmap level are supported.</span></span>
-   <span data-ttu-id="defc0-208">針對集區引數傳遞給 CreateTexture 的值必須是 D3DPOOL \_ SYSTEMMEM。</span><span class="sxs-lookup"><span data-stu-id="defc0-208">The value passed to CreateTexture for the Pool argument must be D3DPOOL\_SYSTEMMEM.</span></span>
-   <span data-ttu-id="defc0-209">此 API 會將提供的記憶體包裝在材質中。</span><span class="sxs-lookup"><span data-stu-id="defc0-209">This API wraps the supplied memory in a texture.</span></span> <span data-ttu-id="defc0-210">請勿將此記憶體解除配置，直到完成為止。</span><span class="sxs-lookup"><span data-stu-id="defc0-210">Do not deallocate this memory until you are done with it.</span></span>

 

 

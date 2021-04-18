---
description: Microsoft Direct3D 9 中的下列功能已變更。 如果您使用這些功能，請參閱下面所列的變更，協助您將應用程式移植到 Direct3D 9。
ms.assetid: 6f5b2cc1-5415-4af8-a964-051a5af42680
title: 轉換成 Direct3D 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: becdb878ad462bfc0157fb15b3c9c1ef2ba158dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971323"
---
# <a name="converting-to-direct3d-9"></a><span data-ttu-id="ef925-104">轉換成 Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="ef925-104">Converting to Direct3D 9</span></span>

<span data-ttu-id="ef925-105">Microsoft Direct3D 9 中的下列功能已變更。</span><span class="sxs-lookup"><span data-stu-id="ef925-105">The following features were changed in Microsoft Direct3D 9.</span></span> <span data-ttu-id="ef925-106">如果您使用這些功能，請參閱下面所列的變更，協助您將應用程式移植到 Direct3D 9。</span><span class="sxs-lookup"><span data-stu-id="ef925-106">If you are using these features, see the changes listed below to help you port your application to Direct3D 9.</span></span>

-   [<span data-ttu-id="ef925-107">BaseVertexIndex 變更</span><span class="sxs-lookup"><span data-stu-id="ef925-107">BaseVertexIndex Changes</span></span>](#basevertexindex-changes)
-   [<span data-ttu-id="ef925-108">CreateImageSurface 變更</span><span class="sxs-lookup"><span data-stu-id="ef925-108">CreateImageSurface Changes</span></span>](#createimagesurface-changes)
-   [<span data-ttu-id="ef925-109">D3DENUM \_ 沒有 \_ WHQL \_ 層級變更</span><span class="sxs-lookup"><span data-stu-id="ef925-109">D3DENUM\_NO\_WHQL\_LEVEL Changes</span></span>](/windows)
-   [<span data-ttu-id="ef925-110">建立資源變更</span><span class="sxs-lookup"><span data-stu-id="ef925-110">Create Resource Changes</span></span>](#create-resource-changes)
-   [<span data-ttu-id="ef925-111">EnumAdapterModes 變更</span><span class="sxs-lookup"><span data-stu-id="ef925-111">EnumAdapterModes Changes</span></span>](#enumadaptermodes-changes)
-   [<span data-ttu-id="ef925-112">取得/SetStreamSource \_ 變更</span><span class="sxs-lookup"><span data-stu-id="ef925-112">Get/SetStreamSource\_Changes</span></span>](#getsetstreamsource-changes)
-   [<span data-ttu-id="ef925-113">多級取樣品質變更</span><span class="sxs-lookup"><span data-stu-id="ef925-113">Multisampling Quality Changes</span></span>](#multisampling-quality-changes)
-   [<span data-ttu-id="ef925-114">ResourceManagerDiscardBytes 變更</span><span class="sxs-lookup"><span data-stu-id="ef925-114">ResourceManagerDiscardBytes Changes</span></span>](#resourcemanagerdiscardbytes-changes)
-   [<span data-ttu-id="ef925-115">SetSoftwareVertexProcessing 變更</span><span class="sxs-lookup"><span data-stu-id="ef925-115">SetSoftwareVertexProcessing Changes</span></span>](#setsoftwarevertexprocessing-changes)
-   [<span data-ttu-id="ef925-116">紋理取樣器變更</span><span class="sxs-lookup"><span data-stu-id="ef925-116">Texture Sampler Changes</span></span>](#texture-sampler-changes)
-   [<span data-ttu-id="ef925-117">頂點宣告變更</span><span class="sxs-lookup"><span data-stu-id="ef925-117">Vertex Declaration Changes</span></span>](#vertex-declaration-changes)
-   [<span data-ttu-id="ef925-118">間隔 \_ 和 \_ SwapEffects \_ 變更</span><span class="sxs-lookup"><span data-stu-id="ef925-118">Intervals,\_and\_SwapEffects\_Changes</span></span>](#intervals-and-swapeffects-changes)

## <a name="basevertexindex-changes"></a><span data-ttu-id="ef925-119">BaseVertexIndex 變更</span><span class="sxs-lookup"><span data-stu-id="ef925-119">BaseVertexIndex Changes</span></span>

<span data-ttu-id="ef925-120">在 DirectX 8.x 中，IDirect3DDevice8：： SetIndices 需要索引緩衝區的指標，以及頂點緩衝區中開始位置的 BaseVertexIndex。</span><span class="sxs-lookup"><span data-stu-id="ef925-120">In DirectX 8.x, IDirect3DDevice8::SetIndices required a pointer to the index buffer and a BaseVertexIndex for the starting position in the vertex buffer.</span></span> <span data-ttu-id="ef925-121">將不同物件批次處理到頂點緩衝區的應用程式必須先切換索引緩衝區 (或呼叫 IDirect3DDevice8：： SetIndices) ，然後再呼叫 IDirect3DDevice8：:D rawIndexedPrimitive。</span><span class="sxs-lookup"><span data-stu-id="ef925-121">An application batching different objects into the vertex buffer had to switch the index buffer (or make a call to IDirect3DDevice8::SetIndices) before calling IDirect3DDevice8::DrawIndexedPrimitive.</span></span>

<span data-ttu-id="ef925-122">在 Direct3D 9 中，頂點緩衝區 *BaseVertexIndex* 中的開始位置已移至 IDirect3DDevice9：:D rawindexedprimitive，而且其資料類型從 DWORD 變更為整數。</span><span class="sxs-lookup"><span data-stu-id="ef925-122">In Direct3D 9, the starting position in the vertex buffer, *BaseVertexIndex*, has been moved to IDirect3DDevice9::DrawIndexedPrimitive, and its data type changed from a DWORD to an INT.</span></span>


```
HRESULT IDirect3DDevice9::DrawIndexedPrimitive( 
    D3DPRIMITIVETYPE PrimType, 
    INT BaseVertexIndex, 
    UINT minIndex, 
    UINT NumVertices, 
    UINT startIndex, 
    UINT primCount); 

HRESULT SetIndices(IDirect3DIndexBuffer9* pIndexData); 
```



## <a name="createimagesurface-changes"></a><span data-ttu-id="ef925-123">CreateImageSurface 變更</span><span class="sxs-lookup"><span data-stu-id="ef925-123">CreateImageSurface Changes</span></span>

<span data-ttu-id="ef925-124">IDirect3DDevice8：： CreateImageSurface 已重新命名為 [**CreateOffscreenPlainSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface)。</span><span class="sxs-lookup"><span data-stu-id="ef925-124">IDirect3DDevice8::CreateImageSurface was renamed [**CreateOffscreenPlainSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface).</span></span> <span data-ttu-id="ef925-125">已新增採用 D3DPOOL 類型的其他參數。</span><span class="sxs-lookup"><span data-stu-id="ef925-125">An additional parameter that takes a D3DPOOL type was added.</span></span> <span data-ttu-id="ef925-126">D3DPOOL 的 \_ 臨時將會傳回與 IDirect3DDevice8：： CreateImageSurface 所建立之介面具有相同特性的介面。</span><span class="sxs-lookup"><span data-stu-id="ef925-126">D3DPOOL\_SCRATCH will return a surface that has identical characteristics to a surface created by IDirect3DDevice8::CreateImageSurface.</span></span> <span data-ttu-id="ef925-127">D3DPOOL \_ 預設值是搭配 [**StretchRect**](/windows/desktop/api) 和 [**ColorFill**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-colorfill)使用的適當集區。</span><span class="sxs-lookup"><span data-stu-id="ef925-127">D3DPOOL\_DEFAULT is the appropriate pool for use with [**StretchRect**](/windows/desktop/api) and [**ColorFill**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-colorfill).</span></span>

## <a name="d3denum_no_whql_level-changes"></a><span data-ttu-id="ef925-128">D3DENUM \_ 沒有 \_ WHQL \_ 層級變更</span><span class="sxs-lookup"><span data-stu-id="ef925-128">D3DENUM\_NO\_WHQL\_LEVEL Changes</span></span>

<span data-ttu-id="ef925-129">應用程式現在必須明確要求 Microsoft Windows 硬體品質實驗室 (的 WHQL) ，因為回應的時間相當長 (幾秒鐘) 。</span><span class="sxs-lookup"><span data-stu-id="ef925-129">Applications now have to explicitly ask for the Microsoft Windows Hardware Quality Labs (WHQL) because the response takes relatively long (a few seconds).</span></span> <span data-ttu-id="ef925-130">D3DENUM \_ 未 \_ \_ 移除 whql 層級，且已 \_ 新增 D3DENUM whql \_ 等級。</span><span class="sxs-lookup"><span data-stu-id="ef925-130">D3DENUM\_NO\_WHQL\_LEVEL has been removed and D3DENUM\_WHQL\_LEVEL has been added.</span></span>

## <a name="create-resource-changes"></a><span data-ttu-id="ef925-131">建立資源變更</span><span class="sxs-lookup"><span data-stu-id="ef925-131">Create Resource Changes</span></span>

<span data-ttu-id="ef925-132">控制碼已新增至數個方法，應設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="ef925-132">A handle has been added to several methods and should be set to **NULL**.</span></span> <span data-ttu-id="ef925-133">受影響的方法包括：</span><span class="sxs-lookup"><span data-stu-id="ef925-133">The methods affected include:</span></span>

-   [<span data-ttu-id="ef925-134">**CreateTexture**</span><span class="sxs-lookup"><span data-stu-id="ef925-134">**CreateTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
-   [<span data-ttu-id="ef925-135">**CreateVolumeTexture**</span><span class="sxs-lookup"><span data-stu-id="ef925-135">**CreateVolumeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)
-   [<span data-ttu-id="ef925-136">**CreateCubeTexture**</span><span class="sxs-lookup"><span data-stu-id="ef925-136">**CreateCubeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
-   [<span data-ttu-id="ef925-137">**CreateVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="ef925-137">**CreateVertexBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer)
-   [<span data-ttu-id="ef925-138">**CreateIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="ef925-138">**CreateIndexBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer)
-   [<span data-ttu-id="ef925-139">**CreateRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="ef925-139">**CreateRenderTarget**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)
-   [<span data-ttu-id="ef925-140">**CreateDepthStencilSurface**</span><span class="sxs-lookup"><span data-stu-id="ef925-140">**CreateDepthStencilSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)
-   [<span data-ttu-id="ef925-141">**CreateOffscreenPlainSurface**</span><span class="sxs-lookup"><span data-stu-id="ef925-141">**CreateOffscreenPlainSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface)

## <a name="enumadaptermodes-changes"></a><span data-ttu-id="ef925-142">EnumAdapterModes 變更</span><span class="sxs-lookup"><span data-stu-id="ef925-142">EnumAdapterModes Changes</span></span>

<span data-ttu-id="ef925-143">[**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes)現在會採用 D3DFORMAT。</span><span class="sxs-lookup"><span data-stu-id="ef925-143">The [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) now takes a D3DFORMAT.</span></span>


```
HRESULT IDirect3D9::EnumAdapterModes( 
       UINT Adapter, 
       D3DFORMAT Format, 
       UINT Mode, 
       D3DDISPLAYMODE *pMode); 
```



<span data-ttu-id="ef925-144">此格式支援一組展開的顯示模式。</span><span class="sxs-lookup"><span data-stu-id="ef925-144">The format supports an expanding set of display modes.</span></span> <span data-ttu-id="ef925-145">為了保護應用程式不會列舉應用程式隨附時未衍生的格式，應用程式必須告訴 Direct3D 應該列舉的顯示模式格式。</span><span class="sxs-lookup"><span data-stu-id="ef925-145">To protect applications from enumerating formats that were not invented when the application shipped, the application must tell Direct3D the format for the display modes that should be enumerated.</span></span> <span data-ttu-id="ef925-146">顯示模式的產生陣列只會隨著寬度、高度和重新整理率不同。</span><span class="sxs-lookup"><span data-stu-id="ef925-146">The resulting array of display modes will differ only by width, height, and refresh rate.</span></span>

<span data-ttu-id="ef925-147">應用程式會指定像素格式，且列舉會限制為完全符合格式的顯示模式。</span><span class="sxs-lookup"><span data-stu-id="ef925-147">The application specifies a pixel format and the enumeration is restricted to those display modes that exactly match the format.</span></span> <span data-ttu-id="ef925-148">以下是允許的格式清單：</span><span class="sxs-lookup"><span data-stu-id="ef925-148">The following is a list of the allowed formats:</span></span>

-   <span data-ttu-id="ef925-149">D3DFMT \_ A1R5G5B5</span><span class="sxs-lookup"><span data-stu-id="ef925-149">D3DFMT\_A1R5G5B5</span></span>
-   <span data-ttu-id="ef925-150">D3DFMT \_ A2B10G10R10</span><span class="sxs-lookup"><span data-stu-id="ef925-150">D3DFMT\_A2B10G10R10</span></span>
-   <span data-ttu-id="ef925-151">D3DFMT \_ A8R8G8B8</span><span class="sxs-lookup"><span data-stu-id="ef925-151">D3DFMT\_A8R8G8B8</span></span>
-   <span data-ttu-id="ef925-152">D3DFMT \_ R5G6B5</span><span class="sxs-lookup"><span data-stu-id="ef925-152">D3DFMT\_R5G6B5</span></span>
-   <span data-ttu-id="ef925-153">D3DFMT \_ X1R5G5B5</span><span class="sxs-lookup"><span data-stu-id="ef925-153">D3DFMT\_X1R5G5B5</span></span>
-   <span data-ttu-id="ef925-154">D3DFMT \_ X8R8G8B8</span><span class="sxs-lookup"><span data-stu-id="ef925-154">D3DFMT\_X8R8G8B8</span></span>

<span data-ttu-id="ef925-155">列舉等同于相同格式的 Alpha 和 nonAlpha 版本。</span><span class="sxs-lookup"><span data-stu-id="ef925-155">Enumeration is equivalent for alpha and nonalpha versions of the same format.</span></span> <span data-ttu-id="ef925-156">傳回的格式一律會填入應用程式所提供的相同格式。</span><span class="sxs-lookup"><span data-stu-id="ef925-156">The returned Format will always be filled with the same format supplied by the application.</span></span>

<span data-ttu-id="ef925-157">這個方法會將565和555視為對等，並傳回格式正確的版本。</span><span class="sxs-lookup"><span data-stu-id="ef925-157">This method treats 565 and 555 as equivalent, and returns the correct version in the Format.</span></span> <span data-ttu-id="ef925-158">只有當應用程式鎖定背景緩衝區，而且應用程式必須設定明確旗標才能完成此動作時，才會發生差異。</span><span class="sxs-lookup"><span data-stu-id="ef925-158">The difference comes into play only when the application locks the back buffer, and there is an explicit flag that the application must set in order to accomplish this.</span></span>

## <a name="getsetstreamsource-changes"></a><span data-ttu-id="ef925-159">取得/SetStreamSource 變更</span><span class="sxs-lookup"><span data-stu-id="ef925-159">Get/SetStreamSource Changes</span></span>

<span data-ttu-id="ef925-160">已將一個參數加入至 [**GetStreamSource**](/windows/desktop/api) 和 [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) 方法。</span><span class="sxs-lookup"><span data-stu-id="ef925-160">One parameter has been added to the [**GetStreamSource**](/windows/desktop/api) and [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) methods.</span></span> <span data-ttu-id="ef925-161">位移是資料流程開頭與頂點資料開頭之間的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="ef925-161">The offset is the number of bytes between the beginning of the stream and the beginning of the vertex data.</span></span> <span data-ttu-id="ef925-162">其測量單位是位元組。</span><span class="sxs-lookup"><span data-stu-id="ef925-162">It is measured in bytes.</span></span> <span data-ttu-id="ef925-163">這可讓管線支援資料流程位移。</span><span class="sxs-lookup"><span data-stu-id="ef925-163">This enables the pipeline to support stream offsets.</span></span> <span data-ttu-id="ef925-164">若要找出裝置是否支援資料流程位移，請參閱 D3DDEVCAPS2 \_ STREAMOFFSET。</span><span class="sxs-lookup"><span data-stu-id="ef925-164">To find out if the device supports stream offsets, see D3DDEVCAPS2\_STREAMOFFSET.</span></span>


```
HRESULT GetStreamSource(
    UINT StreamNumber,
    IDirect3DVertexBuffer9 **ppStreamData,
    UINT *pOffsetInBytes,
    UINT *pStride);
```



## <a name="multisampling-quality-changes"></a><span data-ttu-id="ef925-165">多級取樣品質變更</span><span class="sxs-lookup"><span data-stu-id="ef925-165">Multisampling Quality Changes</span></span>

<span data-ttu-id="ef925-166">先前只有 D3DMULTISAMPLE \_ 類型列舉。</span><span class="sxs-lookup"><span data-stu-id="ef925-166">Previously, there was only the D3DMULTISAMPLE\_TYPE enumeration.</span></span> <span data-ttu-id="ef925-167">Direct3D 9 會保留此列舉，並為列舉的每個元素加入品質層級的概念。</span><span class="sxs-lookup"><span data-stu-id="ef925-167">Direct3D 9 retains this enumeration and adds the idea of a quality level for each element of the enumeration.</span></span> <span data-ttu-id="ef925-168">品質層級表示在視覺品質與效能之間的取捨，方法是以 D3DRS MULTISAMPLEMASK) 的意義，指出 (的遮罩樣本數目 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ef925-168">The quality level indicates a trade-off between visual quality and performance by indicating the number of maskable samples (in the sense of D3DRS\_MULTISAMPLEMASK).</span></span>

<span data-ttu-id="ef925-169">應用程式應該選擇所需的遮罩樣本數目，然後參閱 pQualityLevels。</span><span class="sxs-lookup"><span data-stu-id="ef925-169">An application should choose how many maskable samples it requires, and then consult pQualityLevels.</span></span> <span data-ttu-id="ef925-170">如果是非零值，則這個值表示應用程式可以透過 MultiSampleQuality 傳遞至各種建立函式的品質層級數目。</span><span class="sxs-lookup"><span data-stu-id="ef925-170">If nonzero, this value indicates the number of quality levels the application can pass to the various creation functions through MultiSampleQuality.</span></span> <span data-ttu-id="ef925-171">因為驅動程式會將其所有的多型配置以 D3DMULTISAMPLE NONMASKABLE 的品質層級公開 \_ ，所以如果您的應用程式不需要遮罩範例，您可以透過這種類型來列舉所有可用的取樣。</span><span class="sxs-lookup"><span data-stu-id="ef925-171">Because drivers expose all their multisample schemes as quality levels at D3DMULTISAMPLE\_NONMASKABLE, you can enumerate all available multisampling schemes through this one type if your application does not need to mask samples.</span></span>

<span data-ttu-id="ef925-172">D3DPRASTERCAPS \_ STRETCHBLTMULTISAMPLE caps bit 已淘汰。</span><span class="sxs-lookup"><span data-stu-id="ef925-172">The D3DPRASTERCAPS\_STRETCHBLTMULTISAMPLE caps bit has been retired.</span></span> <span data-ttu-id="ef925-173">這個位用來表示取樣方法不支援寫入遮罩，而且無法在 [**BeginScene**](/windows/desktop/api) 和 [**EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene)之間切換。</span><span class="sxs-lookup"><span data-stu-id="ef925-173">This bit used to mean that the multisampling method did not support write masks, and could not be toggled on and off between [**BeginScene**](/windows/desktop/api) and [**EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene).</span></span> <span data-ttu-id="ef925-174">這類 nonmaskable 方法現在會透過 D3DMULTISAMPLE \_ nonmaskable 公開。</span><span class="sxs-lookup"><span data-stu-id="ef925-174">Such nonmaskable methods are now exposed through D3DMULTISAMPLE\_NONMASKABLE.</span></span>


```
HRESULT CheckDeviceMultiSampleType( 
       UINT Adapter, 
       D3DDEVTYPE DeviceType, 
       D3DFORMAT SurfaceFormat, 
       BOOL Windowed, 
       D3DMULTISAMPLE_TYPE MultiSampleType, 
       DWORD * pQualityLevels); 
```



<span data-ttu-id="ef925-175">每個可遮罩樣本數目的最大值各有不同。</span><span class="sxs-lookup"><span data-stu-id="ef925-175">There is a different maximum for each number of maskable samples.</span></span> <span data-ttu-id="ef925-176">例如，D3DMULTISAMPLE \_ 4 \_ 範例可能有三個品質層級，而 D3DMULTISAMPLE \_ 2 個 \_ 範例可能只有一個。</span><span class="sxs-lookup"><span data-stu-id="ef925-176">For example, D3DMULTISAMPLE\_4\_SAMPLES might have three levels of quality, while D3DMULTISAMPLE\_2\_SAMPLES might have only one.</span></span> <span data-ttu-id="ef925-177">每個遮罩樣本數目最多有八個品質層級 (不允許驅動程式表達更) 。</span><span class="sxs-lookup"><span data-stu-id="ef925-177">There are at most eight levels of quality for each number of maskable samples (the driver is not allowed to express more).</span></span> <span data-ttu-id="ef925-178">品質範圍從零到 (\* pQualityLevels-1) 。</span><span class="sxs-lookup"><span data-stu-id="ef925-178">The quality ranges from zero to (\*pQualityLevels - 1).</span></span>

## <a name="resourcemanagerdiscardbytes-changes"></a><span data-ttu-id="ef925-179">ResourceManagerDiscardBytes 變更</span><span class="sxs-lookup"><span data-stu-id="ef925-179">ResourceManagerDiscardBytes Changes</span></span>

<span data-ttu-id="ef925-180">ResourceManagerDiscardBytes 已由 IDirect3DDevice9：： EvictManagedResources 取代。</span><span class="sxs-lookup"><span data-stu-id="ef925-180">ResourceManagerDiscardBytes has been replaced by IDirect3DDevice9::EvictManagedResources.</span></span> <span data-ttu-id="ef925-181">它可以收回所有資源，包括 Direct3D 和驅動程式資源。</span><span class="sxs-lookup"><span data-stu-id="ef925-181">It can evict all resources, both Direct3D and driver resources.</span></span>

<span data-ttu-id="ef925-182">資源管理員現在會在資源 (管理或非受管理) 因為沒有足夠的視訊記憶體而無法建立時，進行諮詢。</span><span class="sxs-lookup"><span data-stu-id="ef925-182">The resource manager is now consulted when a resource (whether managed or nonmanaged) fails creation because there is insufficient video memory.</span></span> <span data-ttu-id="ef925-183">系統會自動要求管理員釋放足夠的資源，才能成功建立。</span><span class="sxs-lookup"><span data-stu-id="ef925-183">The manager will automatically be asked to free enough resources for the creation to succeed.</span></span> <span data-ttu-id="ef925-184">在 DirectX 8.0 中，這並不是自動化的流程。</span><span class="sxs-lookup"><span data-stu-id="ef925-184">In DirectX 8.0, this was not an automated process.</span></span>

## <a name="setsoftwarevertexprocessing-changes"></a><span data-ttu-id="ef925-185">SetSoftwareVertexProcessing 變更</span><span class="sxs-lookup"><span data-stu-id="ef925-185">SetSoftwareVertexProcessing Changes</span></span>

<span data-ttu-id="ef925-186">應用程式可以建立混合模式裝置，以使用軟體和硬體頂點處理。</span><span class="sxs-lookup"><span data-stu-id="ef925-186">An application can create a mixed-mode device to use software and hardware vertex processing.</span></span>

<span data-ttu-id="ef925-187">若要在 DirectX 8.x 的兩個頂點處理模式之間切換，請呼叫 IDirect3DDevice8：： Graphicsdevice。</span><span class="sxs-lookup"><span data-stu-id="ef925-187">To switch between the two vertex processing modes in DirectX 8.x, call IDirect3DDevice8::SetRenderState.</span></span> <span data-ttu-id="ef925-188">這已由 [**SetSoftwareVertexProcessing**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsoftwarevertexprocessing) 取代，以簡化狀態欄塊所造成的問題。</span><span class="sxs-lookup"><span data-stu-id="ef925-188">This has been replaced with [**SetSoftwareVertexProcessing**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsoftwarevertexprocessing) to ease problems caused by state blocks.</span></span> <span data-ttu-id="ef925-189">狀態欄塊不會記錄這個新的方法。</span><span class="sxs-lookup"><span data-stu-id="ef925-189">This new method is not recorded by state blocks.</span></span>

## <a name="texture-sampler-changes"></a><span data-ttu-id="ef925-190">紋理取樣器變更</span><span class="sxs-lookup"><span data-stu-id="ef925-190">Texture Sampler Changes</span></span>

<span data-ttu-id="ef925-191">Direct3D 9 在一次使用圖元著色器 2 0 模型最多支援16個材質介面 \_ ; 不過，材質座標的數目維持限制為8。</span><span class="sxs-lookup"><span data-stu-id="ef925-191">Direct3D 9 supports up to sixteen texture surfaces in one pass using the pixel shader 2\_0 model; however, the number of texture coordinates remains limited to eight.</span></span> <span data-ttu-id="ef925-192">材質階段狀態是與表面、座標集合、頂點處理和圖元處理相關聯。</span><span class="sxs-lookup"><span data-stu-id="ef925-192">Texture stage state is associated with surfaces, coordinate sets, vertex processing, and pixel processing.</span></span> <span data-ttu-id="ef925-193">為了在編譯時期管理這些差異， [**SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) 已分為兩種方法：</span><span class="sxs-lookup"><span data-stu-id="ef925-193">To manage these differences at compile time, [**SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) has been broken into two methods:</span></span>

-   <span data-ttu-id="ef925-194">IDirect3DDevice9：： SetTextureStageState 仍會用於材質座標狀態，例如換行模式和材質座標產生。</span><span class="sxs-lookup"><span data-stu-id="ef925-194">IDirect3DDevice9::SetTextureStageState will still be used for texture coordinate state, such as wrap modes and texture coordinate generation.</span></span>
-   <span data-ttu-id="ef925-195">[**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) 已加入，現在將用於篩選、平平接、固定、MIPLOD 等等。</span><span class="sxs-lookup"><span data-stu-id="ef925-195">[**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) has been added and will now be used for filtering, tiling, clamping, MIPLOD, and so forth.</span></span> <span data-ttu-id="ef925-196">這最多可以使用十六個取樣器。</span><span class="sxs-lookup"><span data-stu-id="ef925-196">This will work for up to sixteen samplers.</span></span>

### <a name="settexturestagestate-changes"></a><span data-ttu-id="ef925-197">SetTextureStageState 變更</span><span class="sxs-lookup"><span data-stu-id="ef925-197">SetTextureStageState Changes</span></span>

<span data-ttu-id="ef925-198">IDirect3DDevice9：： SetTextureStageState 現在會設定下列狀態：</span><span class="sxs-lookup"><span data-stu-id="ef925-198">IDirect3DDevice9::SetTextureStageState now sets the following states:</span></span>

-   <span data-ttu-id="ef925-199">固定函式頂點處理狀態。</span><span class="sxs-lookup"><span data-stu-id="ef925-199">Fixed function vertex processing state.</span></span> <span data-ttu-id="ef925-200">此狀態控制紋理座標的操作 D3DTSS \_ TEXTURETRANSFORMFLAGS 和 D3DTSS \_ TEXCOORDINDEX。</span><span class="sxs-lookup"><span data-stu-id="ef925-200">This state controls the manipulation of texture coordinates D3DTSS\_TEXTURETRANSFORMFLAGS and D3DTSS\_TEXCOORDINDEX.</span></span> <span data-ttu-id="ef925-201">最多可以將 (設定為8個，因為一律支援8個材質座標) 。</span><span class="sxs-lookup"><span data-stu-id="ef925-201">Up to eight of each can be set (because eight texture coordinates are always supported).</span></span> <span data-ttu-id="ef925-202">D3DTSS \_ TEXCOORDINDEX 是固定的函式頂點處理狀態。</span><span class="sxs-lookup"><span data-stu-id="ef925-202">D3DTSS\_TEXCOORDINDEX is a fixed function vertex processing state.</span></span> <span data-ttu-id="ef925-203">如果使用可程式化的頂點著色器，則會忽略此狀態。</span><span class="sxs-lookup"><span data-stu-id="ef925-203">If a programmable vertex shader is used, this state is ignored.</span></span>
-   <span data-ttu-id="ef925-204">固定的函式圖元著色器狀態 (舊版 TextureStageState) 。</span><span class="sxs-lookup"><span data-stu-id="ef925-204">Fixed function pixel shader state (the legacy TextureStageState).</span></span>

    -   <span data-ttu-id="ef925-205">D3DTSS \_ ALPHAARG0</span><span class="sxs-lookup"><span data-stu-id="ef925-205">D3DTSS\_ALPHAARG0</span></span>
    -   <span data-ttu-id="ef925-206">D3DTSS \_ ALPHAARG1</span><span class="sxs-lookup"><span data-stu-id="ef925-206">D3DTSS\_ALPHAARG1</span></span>
    -   <span data-ttu-id="ef925-207">D3DTSS \_ ALPHAARG2</span><span class="sxs-lookup"><span data-stu-id="ef925-207">D3DTSS\_ALPHAARG2</span></span>
    -   <span data-ttu-id="ef925-208">D3DTSS \_ ALPHAOP</span><span class="sxs-lookup"><span data-stu-id="ef925-208">D3DTSS\_ALPHAOP</span></span>
    -   <span data-ttu-id="ef925-209">D3DTSS \_ BUMPENVLOFFSET</span><span class="sxs-lookup"><span data-stu-id="ef925-209">D3DTSS\_BUMPENVLOFFSET</span></span>
    -   <span data-ttu-id="ef925-210">D3DTSS \_ BUMPENVLSCALE</span><span class="sxs-lookup"><span data-stu-id="ef925-210">D3DTSS\_BUMPENVLSCALE</span></span>
    -   <span data-ttu-id="ef925-211">D3DTSS \_ BUMPENVMAT00</span><span class="sxs-lookup"><span data-stu-id="ef925-211">D3DTSS\_BUMPENVMAT00</span></span>
    -   <span data-ttu-id="ef925-212">D3DTSS \_ BUMPENVMAT01</span><span class="sxs-lookup"><span data-stu-id="ef925-212">D3DTSS\_BUMPENVMAT01</span></span>
    -   <span data-ttu-id="ef925-213">D3DTSS \_ BUMPENVMAT10</span><span class="sxs-lookup"><span data-stu-id="ef925-213">D3DTSS\_BUMPENVMAT10</span></span>
    -   <span data-ttu-id="ef925-214">D3DTSS \_ BUMPENVMAT11</span><span class="sxs-lookup"><span data-stu-id="ef925-214">D3DTSS\_BUMPENVMAT11</span></span>
    -   <span data-ttu-id="ef925-215">D3DTSS \_ COLORARG0</span><span class="sxs-lookup"><span data-stu-id="ef925-215">D3DTSS\_COLORARG0</span></span>
    -   <span data-ttu-id="ef925-216">D3DTSS \_ COLORARG1</span><span class="sxs-lookup"><span data-stu-id="ef925-216">D3DTSS\_COLORARG1</span></span>
    -   <span data-ttu-id="ef925-217">D3DTSS \_ COLORARG2</span><span class="sxs-lookup"><span data-stu-id="ef925-217">D3DTSS\_COLORARG2</span></span>
    -   <span data-ttu-id="ef925-218">D3DTSS \_ COLOROP</span><span class="sxs-lookup"><span data-stu-id="ef925-218">D3DTSS\_COLOROP</span></span>
    -   <span data-ttu-id="ef925-219">D3DTSS \_ RESULTARG</span><span class="sxs-lookup"><span data-stu-id="ef925-219">D3DTSS\_RESULTARG</span></span>

    <span data-ttu-id="ef925-220">可以設定的固定函式圖元著色器狀態數目小於或等於 MaxTextureBlendStages 所代表的數位。</span><span class="sxs-lookup"><span data-stu-id="ef925-220">The number of fixed function pixel shader states that can be set is less than or equal to the number represented by MaxTextureBlendStages.</span></span>

<span data-ttu-id="ef925-221">應用程式可用的紋理取樣器數目取決於圖元著色器版本，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="ef925-221">The number of texture samplers available to the application is determined by the pixel shader version, as indicated in the following table.</span></span>



| <span data-ttu-id="ef925-222">Name</span><span class="sxs-lookup"><span data-stu-id="ef925-222">Name</span></span>                    | <span data-ttu-id="ef925-223">Number</span><span class="sxs-lookup"><span data-stu-id="ef925-223">Number</span></span>                                                         |
|-------------------------|----------------------------------------------------------------|
| <span data-ttu-id="ef925-224">ps \_ 1 \_ 1 到 ps \_ 1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="ef925-224">ps\_1\_1 to ps\_1\_3</span></span>    | <span data-ttu-id="ef925-225">4紋理取樣器</span><span class="sxs-lookup"><span data-stu-id="ef925-225">4 texture samplers</span></span>                                             |
| <span data-ttu-id="ef925-226">ps \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="ef925-226">ps\_1\_4</span></span>                | <span data-ttu-id="ef925-227">6紋理取樣器</span><span class="sxs-lookup"><span data-stu-id="ef925-227">6 texture samplers</span></span>                                             |
| <span data-ttu-id="ef925-228">ps \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ef925-228">ps\_2\_0</span></span>                | <span data-ttu-id="ef925-229">16個材質取樣器</span><span class="sxs-lookup"><span data-stu-id="ef925-229">16 texture samplers</span></span>                                            |
| <span data-ttu-id="ef925-230">固定函式管線</span><span class="sxs-lookup"><span data-stu-id="ef925-230">fixed function pipeline</span></span> | <span data-ttu-id="ef925-231">MaxTextureBlendStages/MaxSimultaneousTextures 材質取樣器</span><span class="sxs-lookup"><span data-stu-id="ef925-231">MaxTextureBlendStages/MaxSimultaneousTextures texture samplers</span></span> |



 

<span data-ttu-id="ef925-232">在 Direct3D 9 中支援置換對應的裝置將會支援額外的取樣器 (D3DDMAPSAMPLER) ，以取樣鑲嵌單位中的置換地圖。</span><span class="sxs-lookup"><span data-stu-id="ef925-232">Devices that support displacement mapping in Direct3D 9 will support an additional sampler (D3DDMAPSAMPLER), which samples the displacement maps in the tessellator unit.</span></span>

### <a name="setsamplerstate-changes"></a><span data-ttu-id="ef925-233">SetSamplerState 變更</span><span class="sxs-lookup"><span data-stu-id="ef925-233">SetSamplerState Changes</span></span>

<span data-ttu-id="ef925-234">IDirect3DDevice9：： SetSamplerState 會將取樣器狀態 (，包括鑲嵌單位中用來取樣置換地圖) 。</span><span class="sxs-lookup"><span data-stu-id="ef925-234">IDirect3DDevice9::SetSamplerState sets the sampler state (including the one used in the tessellator unit to sample displacement maps).</span></span> <span data-ttu-id="ef925-235">這些已重新命名為 D3DSAMP \_ 前置詞，以在從 DirectX 8.x 移植時啟用編譯時期錯誤偵測。</span><span class="sxs-lookup"><span data-stu-id="ef925-235">These have been renamed with a D3DSAMP\_ prefix to enable compile-time error detection when porting from DirectX 8.x.</span></span> <span data-ttu-id="ef925-236">這些狀態包括：</span><span class="sxs-lookup"><span data-stu-id="ef925-236">The states include:</span></span>

-   <span data-ttu-id="ef925-237">D3DSAMP \_ ADDRESSU</span><span class="sxs-lookup"><span data-stu-id="ef925-237">D3DSAMP\_ADDRESSU</span></span>
-   <span data-ttu-id="ef925-238">D3DSAMP \_ ADDRESSV</span><span class="sxs-lookup"><span data-stu-id="ef925-238">D3DSAMP\_ADDRESSV</span></span>
-   <span data-ttu-id="ef925-239">D3DSAMP \_ ADDRESSW</span><span class="sxs-lookup"><span data-stu-id="ef925-239">D3DSAMP\_ADDRESSW</span></span>
-   <span data-ttu-id="ef925-240">D3DSAMP \_ 邊框</span><span class="sxs-lookup"><span data-stu-id="ef925-240">D3DSAMP\_BORDERCOLOR</span></span>
-   <span data-ttu-id="ef925-241">D3DSAMP \_ MAGFILTER</span><span class="sxs-lookup"><span data-stu-id="ef925-241">D3DSAMP\_MAGFILTER</span></span>
-   <span data-ttu-id="ef925-242">D3DSAMP \_ MAXANISOTROPY</span><span class="sxs-lookup"><span data-stu-id="ef925-242">D3DSAMP\_MAXANISOTROPY</span></span>
-   <span data-ttu-id="ef925-243">D3DSAMP \_ MAXMIPLEVEL</span><span class="sxs-lookup"><span data-stu-id="ef925-243">D3DSAMP\_MAXMIPLEVEL</span></span>
-   <span data-ttu-id="ef925-244">D3DSAMP \_ MINFILTER</span><span class="sxs-lookup"><span data-stu-id="ef925-244">D3DSAMP\_MINFILTER</span></span>
-   <span data-ttu-id="ef925-245">D3DSAMP \_ MIPFILTER</span><span class="sxs-lookup"><span data-stu-id="ef925-245">D3DSAMP\_MIPFILTER</span></span>
-   <span data-ttu-id="ef925-246">D3DSAMP \_ MIPMAPLODBIAS</span><span class="sxs-lookup"><span data-stu-id="ef925-246">D3DSAMP\_MIPMAPLODBIAS</span></span>

## <a name="vertex-declaration-changes"></a><span data-ttu-id="ef925-247">頂點宣告變更</span><span class="sxs-lookup"><span data-stu-id="ef925-247">Vertex Declaration Changes</span></span>

<span data-ttu-id="ef925-248">頂點宣告現在會與建立頂點著色器分離。</span><span class="sxs-lookup"><span data-stu-id="ef925-248">Vertex declarations are now decoupled from vertex shader creation.</span></span> <span data-ttu-id="ef925-249">頂點宣告現在會使用元件物件模型 (COM) 介面。</span><span class="sxs-lookup"><span data-stu-id="ef925-249">Vertex declarations now use a Component Object Model (COM) interface.</span></span>

<span data-ttu-id="ef925-250">針對 DirectX 8.x，頂點宣告會系結至頂點著色器。</span><span class="sxs-lookup"><span data-stu-id="ef925-250">For DirectX 8.x, vertex declarations are tied to vertex shaders.</span></span>

-   <span data-ttu-id="ef925-251">針對固定函式管線，使用彈性頂點格式來呼叫 [**SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) ， (FVF 頂點緩衝區的) 代碼。</span><span class="sxs-lookup"><span data-stu-id="ef925-251">For the fixed function pipeline, call [**SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) with the flexible vertex format (FVF) code of the vertex buffer.</span></span>
-   <span data-ttu-id="ef925-252">針對頂點著色器，請使用先前建立頂點著色器的控制碼來呼叫 IDirect3DDevice9：： SetVertexShader。</span><span class="sxs-lookup"><span data-stu-id="ef925-252">For vertex shaders, call IDirect3DDevice9::SetVertexShader with a handle to a previously create vertex shader.</span></span> <span data-ttu-id="ef925-253">著色器包含頂點宣告。</span><span class="sxs-lookup"><span data-stu-id="ef925-253">The shader includes a vertex declaration.</span></span>

<span data-ttu-id="ef925-254">針對 Direct3D 9，頂點宣告會從頂點著色器分離出來，而且可以搭配 fixed 函數管線或著色器使用。</span><span class="sxs-lookup"><span data-stu-id="ef925-254">For Direct3D 9, vertex declarations are decoupled from vertex shaders and they can be used with either the fixed function pipeline or with shaders.</span></span>

-   <span data-ttu-id="ef925-255">對於 fixed 函數管線，不需要呼叫 IDirect3DDevice9：： SetVertexShader。</span><span class="sxs-lookup"><span data-stu-id="ef925-255">For the fixed function pipeline, there is no need to call IDirect3DDevice9::SetVertexShader.</span></span> <span data-ttu-id="ef925-256">但是，如果您想要切換至固定函式管線，且先前已使用頂點著色器，請呼叫 IDirect3DDevice9：： SetVertexShader (**Null**) 。</span><span class="sxs-lookup"><span data-stu-id="ef925-256">If, however, you want to switch to the fixed function pipeline and have previously used a vertex shader, call IDirect3DDevice9::SetVertexShader(**NULL**).</span></span> <span data-ttu-id="ef925-257">完成這項操作之後，您仍然需要呼叫 [**SetFVF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf) 來宣告 FVF 程式碼。</span><span class="sxs-lookup"><span data-stu-id="ef925-257">When this is done, you will still need to call [**SetFVF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf) to declare the FVF code.</span></span>
-   <span data-ttu-id="ef925-258">使用頂點著色器時，請使用頂點著色器物件來呼叫 IDirect3DDevice9：： SetVertexShader。</span><span class="sxs-lookup"><span data-stu-id="ef925-258">When using vertex shaders, call IDirect3DDevice9::SetVertexShader with the vertex shader object.</span></span> <span data-ttu-id="ef925-259">此外，呼叫 IDirect3DDevice9：： SetFVF 來設定頂點宣告。</span><span class="sxs-lookup"><span data-stu-id="ef925-259">Additionally, call IDirect3DDevice9::SetFVF to set up a vertex declaration.</span></span> <span data-ttu-id="ef925-260">這會使用 FVF 中隱含的資訊。</span><span class="sxs-lookup"><span data-stu-id="ef925-260">This uses the information implicit in the FVF.</span></span> <span data-ttu-id="ef925-261">您可以呼叫 [**SetVertexDeclaration**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexdeclaration)取代 IDirect3DDevice9：： SetFVF，因為它支援無法以 FVF 表示的頂點宣告。</span><span class="sxs-lookup"><span data-stu-id="ef925-261">[**SetVertexDeclaration**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexdeclaration) can be called in place of IDirect3DDevice9::SetFVF because it supports vertex declarations that cannot be expressed with an FVF.</span></span>

## <a name="intervals-and-swapeffects-changes"></a><span data-ttu-id="ef925-262">間隔和 SwapEffects 變更</span><span class="sxs-lookup"><span data-stu-id="ef925-262">Intervals, and SwapEffects Changes</span></span>

<span data-ttu-id="ef925-263">有幾項變更可讓使用者更充分掌控監視器重新整理速率、呈現速率，以及前端緩衝區與背景緩衝區的繪製。</span><span class="sxs-lookup"><span data-stu-id="ef925-263">Several changes were made to give the user more control over monitor refresh rate, presentation rate, and front-buffer versus back-buffer drawing.</span></span> <span data-ttu-id="ef925-264">如下所示：</span><span class="sxs-lookup"><span data-stu-id="ef925-264">They are as follows:</span></span>

-   <span data-ttu-id="ef925-265">已移除一個交換效果、D3DSWAPEFFECT \_ 複製 \_ VSYNC，以及一個表示速率（D3DPRESENT \_ 率 \_ 無限制）。</span><span class="sxs-lookup"><span data-stu-id="ef925-265">Removed one swap effect, D3DSWAPEFFECT\_COPY\_VSYNC, and one presentation rate, D3DPRESENT\_RATE\_UNLIMITED.</span></span>
-   <span data-ttu-id="ef925-266">已重新命名 D3DPRESENT \_ 參數。\_PresentationIntervals 的全螢幕 PresentationInterval。</span><span class="sxs-lookup"><span data-stu-id="ef925-266">Renamed D3DPRESENT\_PARAMETERS.FullScreen\_PresentationInterval to PresentationIntervals.</span></span>
-   <span data-ttu-id="ef925-267">新增 D3DPRESENT \_ 間隔 \_ 立即，這表示簡報不會與垂直同步處理同步。如同 DirectX 8.x，D3DPRESENT \_ INTERVAL \_ 預設值定義為零，相當於 D3DPRESENT \_ INTERVAL \_ 1。</span><span class="sxs-lookup"><span data-stu-id="ef925-267">Added D3DPRESENT\_INTERVAL\_IMMEDIATE, which means that the presentation is not synchronized with the vertical sync. As in DirectX 8.x, D3DPRESENT\_INTERVAL\_DEFAULT is defined as zero and is equivalent to D3DPRESENT\_INTERVAL\_ONE.</span></span> <span data-ttu-id="ef925-268">D3DPRESENT \_ 間隔 \_ 預設是將 D3DPRESENT \_ 參數初始化為零的便利性。</span><span class="sxs-lookup"><span data-stu-id="ef925-268">D3DPRESENT\_INTERVAL\_DEFAULT is a convenience for initializing D3DPRESENT\_PARAMETERS to zero.</span></span>

<span data-ttu-id="ef925-269">如需模式和所支援間隔的詳細說明，請參閱 D3DPRESENT。</span><span class="sxs-lookup"><span data-stu-id="ef925-269">For a detailed explanation of the modes and the intervals that are supported, see D3DPRESENT.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef925-270">相關主題</span><span class="sxs-lookup"><span data-stu-id="ef925-270">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef925-271">Direct3D 9 圖形</span><span class="sxs-lookup"><span data-stu-id="ef925-271">Direct3D 9 Graphics</span></span>](dx9-graphics.md)
</dt> </dl>

 

 

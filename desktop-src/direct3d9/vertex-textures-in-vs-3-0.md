---
description: 頂點著色器3.0 模型支援使用 texldl-vs 材質 load 語句，在頂點著色器中進行紋理查閱。
ms.assetid: 595cb5c0-da12-4fe9-944c-a61d8ed990b4
title: Vs_3_0 (DirectX HLSL) 中的頂點紋理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a4e8e7bbf7e1ae9764fe5b30647f318dfaeb3ba
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688256"
---
# <a name="vertex-textures-in-vs_3_0-directx-hlsl"></a><span data-ttu-id="2aca2-103">Vs \_ 3 \_ 0 (DirectX HLSL) 的頂點紋理</span><span class="sxs-lookup"><span data-stu-id="2aca2-103">Vertex Textures in vs\_3\_0 (DirectX HLSL)</span></span>

<span data-ttu-id="2aca2-104">頂點著色器3.0 模型支援使用 [texldl-vs](../direct3dhlsl/texldl---vs.md) 材質 load 語句，在頂點著色器中進行紋理查閱。</span><span class="sxs-lookup"><span data-stu-id="2aca2-104">The vertex shader 3.0 model supports texture lookup in the vertex shader using the [texldl - vs](../direct3dhlsl/texldl---vs.md) texture load statement.</span></span> <span data-ttu-id="2aca2-105">頂點引擎包含四個紋理取樣器階段，名稱為 [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md)、D3DVERTEXTEXTURESAMPLER1、D3DVERTEXTEXTURESAMPLER2 和 D3DVERTEXTEXTURESAMPLER3。</span><span class="sxs-lookup"><span data-stu-id="2aca2-105">The vertex engine contains four texture sampler stages, named [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md), D3DVERTEXTEXTURESAMPLER1, D3DVERTEXTEXTURESAMPLER2, and D3DVERTEXTEXTURESAMPLER3.</span></span> <span data-ttu-id="2aca2-106">這些與圖元引擎中的置換地圖取樣器和紋理取樣器不同。</span><span class="sxs-lookup"><span data-stu-id="2aca2-106">These are distinct from the displacement map sampler and texture samplers in the pixel engine.</span></span>

<span data-ttu-id="2aca2-107">若要在這四個階段設定範例紋理，您可以使用頂點引擎並使用 [**CheckDeviceFormat**](/windows/desktop/api) 方法來程式設計階段。</span><span class="sxs-lookup"><span data-stu-id="2aca2-107">To sample textures set at those four stages, you can use the vertex engine and program the stages with the [**CheckDeviceFormat**](/windows/desktop/api) method.</span></span> <span data-ttu-id="2aca2-108">使用 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)在階段索引 [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md) 到 D3DVERTEXTEXTURESAMPLER3 的階段設定紋理。</span><span class="sxs-lookup"><span data-stu-id="2aca2-108">Set textures at those stages using [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture), with the stage index [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md) through D3DVERTEXTEXTURESAMPLER3.</span></span> <span data-ttu-id="2aca2-109">端點著色器中引進了新的暫存器，取樣器註冊 (如 ps \_ 2 0) 中所示 \_ ，這代表頂點紋理取樣器。</span><span class="sxs-lookup"><span data-stu-id="2aca2-109">A new register has been introduced in the vertex shader, the sampler register (like in ps\_2\_0), which represents the vertex texture sampler.</span></span> <span data-ttu-id="2aca2-110">在使用之前，必須先在著色器中定義這個暫存器。</span><span class="sxs-lookup"><span data-stu-id="2aca2-110">This register needs to be defined in the shader before using it.</span></span>

<span data-ttu-id="2aca2-111">應用程式可以藉由呼叫 [**CheckDeviceFormat**](/windows/desktop/api) with [D3DUSAGE \_ query \_ VERTEXTEXTURE](d3dusage-query.md)，查詢是否支援將格式作為頂點紋理。</span><span class="sxs-lookup"><span data-stu-id="2aca2-111">An application can query if a format is supported as a vertex texture by calling [**CheckDeviceFormat**](/windows/desktop/api) with [D3DUSAGE\_QUERY\_VERTEXTEXTURE](d3dusage-query.md).</span></span>

> [!Note]  
> <span data-ttu-id="2aca2-112">這是查詢旗標，因此不接受任何 Createxxx 函數。</span><span class="sxs-lookup"><span data-stu-id="2aca2-112">This is a query flag so it is not accepted in any Createxxx function.</span></span> <span data-ttu-id="2aca2-113">在預設集區中建立的頂點紋理可以設定為圖元材質，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="2aca2-113">A vertex texture created in the default pool can be set as a pixel texture and vice versa.</span></span> <span data-ttu-id="2aca2-114">不過，若要使用軟體頂點處理，您必須在暫存集區中建立頂點材質 (無論是混合模式裝置或軟體頂點處理裝置) 。</span><span class="sxs-lookup"><span data-stu-id="2aca2-114">However, to use the software vertex processing, the vertex texture must be created in the scratch pool (no matter if it is a mixed-mode device or a software vertex processing device).</span></span>

 

<span data-ttu-id="2aca2-115">這項功能與圖元材質相同，不同之處如下：</span><span class="sxs-lookup"><span data-stu-id="2aca2-115">The functionality is identical to the pixel textures, except for the following:</span></span>

-   <span data-ttu-id="2aca2-116">不支援非等向材質篩選，因此 \_ 會忽略 D3DSAMP MAXANISOTROPY，而且無法針對 [ \_ 放大] 或 [縮短] 設定這些階段的 D3DTEXF。</span><span class="sxs-lookup"><span data-stu-id="2aca2-116">Anisotropic texture filtering is not supported, hence D3DSAMP\_MAXANISOTROPY is ignored and D3DTEXF\_ANISOTROPIC cannot be set for magnify, or minify for these stages.</span></span>
-   <span data-ttu-id="2aca2-117">無法使用變更資訊的速率，因此應用程式必須計算詳細資料層級，並將該資訊以參數的形式提供給 [texldl-vs](../direct3dhlsl/texldl---vs.md)。</span><span class="sxs-lookup"><span data-stu-id="2aca2-117">Rate of change information is not available, hence the application has to compute the level of detail and provide that information as a parameter to [texldl - vs](../direct3dhlsl/texldl---vs.md).</span></span>

<span data-ttu-id="2aca2-118">限制包含：</span><span class="sxs-lookup"><span data-stu-id="2aca2-118">Restrictions include:</span></span>

-   <span data-ttu-id="2aca2-119">如同圖元著色器，如果支援 multielement 紋理， \_ 則會使用 D3DSAMP ELEMENTINDEX 來找出要取樣的元素。</span><span class="sxs-lookup"><span data-stu-id="2aca2-119">As in pixel shaders, if multielement textures are supported, D3DSAMP\_ELEMENTINDEX is used to figure out which element to sample from.</span></span>
-   <span data-ttu-id="2aca2-120">\_這些階段會忽略狀態 D3DSAMP DMAPOFFSET。</span><span class="sxs-lookup"><span data-stu-id="2aca2-120">The state D3DSAMP\_DMAPOFFSET is ignored for these stages.</span></span>
-   <span data-ttu-id="2aca2-121">使用 [**CheckDeviceFormat**](/windows/desktop/api) 搭配 [D3DUSAGE \_ query \_ VERTEXTEXTURE "](d3dusage-query.md) 來查詢材質，以查看是否可將其當做頂點材質使用。</span><span class="sxs-lookup"><span data-stu-id="2aca2-121">Use [**CheckDeviceFormat**](/windows/desktop/api) with [D3DUSAGE\_QUERY\_VERTEXTEXTURE"](d3dusage-query.md) to query a texture to see if it can be used as a vertex texture.</span></span>
-   <span data-ttu-id="2aca2-122">VertexTextureFilterCaps 指出頂點紋理取樣器允許何種篩選。</span><span class="sxs-lookup"><span data-stu-id="2aca2-122">VertexTextureFilterCaps indicates what kind of filters are allowed at the vertex texture samplers.</span></span> <span data-ttu-id="2aca2-123">[D3DPTFILTERCAPS \_](d3dptfiltercaps.md)不允許 MINFANISOTROPIC 和 D3DPTFILTERCAPS \_ MAGFANISOTROPIC。</span><span class="sxs-lookup"><span data-stu-id="2aca2-123">[D3DPTFILTERCAPS\_MINFANISOTROPIC](d3dptfiltercaps.md) and D3DPTFILTERCAPS\_MAGFANISOTROPIC are disallowed.</span></span>

## <a name="sampling-stage-registers"></a><span data-ttu-id="2aca2-124">取樣階段暫存器</span><span class="sxs-lookup"><span data-stu-id="2aca2-124">Sampling Stage Registers</span></span>

<span data-ttu-id="2aca2-125">取樣階段暫存器會識別可在材質載入語句中使用的取樣單位。</span><span class="sxs-lookup"><span data-stu-id="2aca2-125">A sampling stage register identifies a sampling unit that can be used in texture load statements.</span></span> <span data-ttu-id="2aca2-126">取樣單位會對應至材質取樣階段，封裝 [**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)中提供的取樣特定狀態。</span><span class="sxs-lookup"><span data-stu-id="2aca2-126">A sampling unit corresponds to the texture sampling stage, encapsulating the sampling-specific state provided in [**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate).</span></span>

<span data-ttu-id="2aca2-127">每個取樣器都會使用 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)來唯一識別設定為對應取樣器的單一材質介面。</span><span class="sxs-lookup"><span data-stu-id="2aca2-127">Each sampler uniquely identifies a single texture surface that is set to the corresponding sampler using [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span></span> <span data-ttu-id="2aca2-128">不過，您可以在多個取樣器設定相同的材質介面。</span><span class="sxs-lookup"><span data-stu-id="2aca2-128">However, the same texture surface can be set at multiple samplers.</span></span>

<span data-ttu-id="2aca2-129">在繪圖時，紋理不能同時設定為轉譯目標和某個階段的材質。</span><span class="sxs-lookup"><span data-stu-id="2aca2-129">At draw time, a texture cannot be simultaneously set as a render target and a texture at a stage.</span></span>

<span data-ttu-id="2aca2-130">由於 vs \_ 3 \_ 0 支援四個取樣器，因此在單一著色器階段中最多可以讀取四個材質表面。</span><span class="sxs-lookup"><span data-stu-id="2aca2-130">Because vs\_3\_0 supports four samplers, up to four texture surfaces can be read from in a single shader pass.</span></span> <span data-ttu-id="2aca2-131">取樣器暫存器可能只會顯示為材質 load 語句中的引數： [texldl-vs](../direct3dhlsl/texldl---vs.md)。</span><span class="sxs-lookup"><span data-stu-id="2aca2-131">A sampler register might appear only as an argument in the texture load statement: [texldl - vs](../direct3dhlsl/texldl---vs.md).</span></span>

<span data-ttu-id="2aca2-132">在 vs \_ 3 \_ 0 中，如果您使用取樣器，則必須在著色器程式的開頭宣告它，並使用 [ (samplerType] 的 [ [ \_ sm3-vs asm]) ](../direct3dhlsl/dcl-samplertype---vs.md) (和 ps \_ 2 0) 中的相同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="2aca2-132">In vs\_3\_0, if you use a sampler, it must be declared at the beginning of the shader program, using the [dcl\_samplerType (sm3 - vs asm)](../direct3dhlsl/dcl-samplertype---vs.md) (as in ps\_2\_0).</span></span>

## <a name="software-processing"></a><span data-ttu-id="2aca2-133">軟體處理</span><span class="sxs-lookup"><span data-stu-id="2aca2-133">Software Processing</span></span>

<span data-ttu-id="2aca2-134">軟體頂點處理將支援這項功能。</span><span class="sxs-lookup"><span data-stu-id="2aca2-134">This feature will be supported in software vertex processing.</span></span> <span data-ttu-id="2aca2-135">您可以藉由呼叫 [**GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) 和檢查 VertexTextureFilterCaps，檢查支援的特定篩選類型。</span><span class="sxs-lookup"><span data-stu-id="2aca2-135">The specific filter types supported can be checked by calling [**GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) and checking VertexTextureFilterCaps.</span></span> <span data-ttu-id="2aca2-136">所有已發佈的材質格式在軟體頂點處理中都支援做為頂點紋理。</span><span class="sxs-lookup"><span data-stu-id="2aca2-136">All published texture formats will be supported as vertex textures in software vertex processing.</span></span>

<span data-ttu-id="2aca2-137">應用程式可以藉由呼叫 [**CheckDeviceFormat**](/windows/desktop/api) 並提供 (D3DVERTEXTEXTURESAMPLER \| [**D3DUSAGE \_ SOFTWAREPROCESSING**](d3dusage.md)) 為使用方式，檢查軟體頂點處理模式中是否支援特定的材質格式。</span><span class="sxs-lookup"><span data-stu-id="2aca2-137">Applications can check if a particular texture format is supported in the software vertex processing mode by calling [**CheckDeviceFormat**](/windows/desktop/api) and providing (D3DVERTEXTEXTURESAMPLER \| [**D3DUSAGE\_SOFTWAREPROCESSING**](d3dusage.md)) as usage.</span></span> <span data-ttu-id="2aca2-138">所有格式都支援軟體頂點處理。</span><span class="sxs-lookup"><span data-stu-id="2aca2-138">All formats are supported for software vertex processing.</span></span> <span data-ttu-id="2aca2-139">臨時集區是軟體頂點處理的必要項。</span><span class="sxs-lookup"><span data-stu-id="2aca2-139">The scratch pool is required for software vertex processing.</span></span>

## <a name="api-changes"></a><span data-ttu-id="2aca2-140">API 變更</span><span class="sxs-lookup"><span data-stu-id="2aca2-140">API Changes</span></span>


```
   
// New define
#define D3DVERTEXTEXTURESAMPLER0 (D3DDMAPSAMPLER+1)
#define D3DVERTEXTEXTURESAMPLER1 (D3DDMAPSAMPLER+2)
#define D3DVERTEXTEXTURESAMPLER2 (D3DDMAPSAMPLER+3)
#define D3DVERTEXTEXTURESAMPLER3 (D3DDMAPSAMPLER+4)
    

#define D3DVERTEXTEXTURESAMPLER  (0x00100000L)

// New caps field in D3DCAPS9
DWORD VertexTextureFilterCaps;
```



## <a name="related-topics"></a><span data-ttu-id="2aca2-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="2aca2-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2aca2-142">頂點管線</span><span class="sxs-lookup"><span data-stu-id="2aca2-142">Vertex Pipeline</span></span>](vertex-pipeline.md)
</dt> </dl>

 

 

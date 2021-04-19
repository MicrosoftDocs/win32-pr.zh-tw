---
description: 材質內容通常會以 sRGB 格式儲存。
ms.assetid: d076140d-3e91-412a-b099-9baa52f8d7d8
title: " (Direct3D 9) 的 Gamma"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cea4b3ba224452e1c3be8f96b7136f4e4f649c8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106971272"
---
# <a name="gamma-direct3d-9"></a><span data-ttu-id="e71bf-103"> (Direct3D 9) 的 Gamma</span><span class="sxs-lookup"><span data-stu-id="e71bf-103">Gamma (Direct3D 9)</span></span>

<span data-ttu-id="e71bf-104">材質內容通常會以 sRGB 格式儲存。</span><span class="sxs-lookup"><span data-stu-id="e71bf-104">Texture content is often stored in sRGB format.</span></span> <span data-ttu-id="e71bf-105">傳統上，圖元管線假設色彩為線性，因此會以線性空間執行混合作業。</span><span class="sxs-lookup"><span data-stu-id="e71bf-105">Traditionally, pixel pipelines assumed the colors to be linear so blending operations were performed in linear space.</span></span> <span data-ttu-id="e71bf-106">不過，由於 sRGB 內容是由 gamma 修正，因此線性空間中的混合作業將會產生不正確的結果。</span><span class="sxs-lookup"><span data-stu-id="e71bf-106">However, since sRGB content is gamma corrected, blending operations in linear space will produce incorrect results.</span></span> <span data-ttu-id="e71bf-107">視訊卡現在可以修正此問題，方法是在讀取任何 sRGB 內容時復原 gamma 修正，並在寫出圖元時將圖元資料轉換回 sRGB 格式。</span><span class="sxs-lookup"><span data-stu-id="e71bf-107">Video cards can now fix this problem by undoing the gamma correction when they read any sRGB content, and convert pixel data back to the sRGB format when writing out pixels.</span></span> <span data-ttu-id="e71bf-108">在此情況下，圖元管線內的所有作業都會線上性空間中執行。</span><span class="sxs-lookup"><span data-stu-id="e71bf-108">In this case, all operations inside the pixel pipeline are performed in the linear space.</span></span>

## <a name="gamma-correction"></a><span data-ttu-id="e71bf-109">Gamma 修正</span><span class="sxs-lookup"><span data-stu-id="e71bf-109">Gamma Correction</span></span>

<span data-ttu-id="e71bf-110">Direct3D 9 可以：</span><span class="sxs-lookup"><span data-stu-id="e71bf-110">Direct3D 9 can:</span></span>

-   <span data-ttu-id="e71bf-111">指出材質是否已更正為 gamma 2.2，或不 (sRGB 或不) 。</span><span class="sxs-lookup"><span data-stu-id="e71bf-111">Indicate whether a texture is gamma 2.2 corrected or not (sRGB or not).</span></span> <span data-ttu-id="e71bf-112">驅動程式會在 SetTexture 階段轉換成線性 gamma 以進行混合作業，或取樣器會在查閱時將它轉換成線性資料。</span><span class="sxs-lookup"><span data-stu-id="e71bf-112">The driver will either convert to a linear gamma for blending operations at SetTexture time, or the sampler will convert it to linear data at lookup time.</span></span>
-   <span data-ttu-id="e71bf-113">指出將圖元管線寫出至轉譯目標時，是否應將其 gamma 校正為 sRGB 空間。</span><span class="sxs-lookup"><span data-stu-id="e71bf-113">Indicate whether the pixel pipeline should gamma correct back to sRGB space when writing out to the render target.</span></span>

<span data-ttu-id="e71bf-114">所有其他色彩 (清除色彩、材質色彩、頂點色彩等等 ) 都會假設線上性空間中。</span><span class="sxs-lookup"><span data-stu-id="e71bf-114">All other colors (clear color, material color, vertex color, etc.) are assumed to be in linear space.</span></span> <span data-ttu-id="e71bf-115">應用程式可以使用圖元著色器指令，以 gamma 更正寫入框架緩衝區的色彩。</span><span class="sxs-lookup"><span data-stu-id="e71bf-115">Applications can gamma-correct the colors written into the frame buffer using pixel shader instructions.</span></span> <span data-ttu-id="e71bf-116">Linearization 只能套用至 RGB 通道，而不應套用至 Alpha 色板。</span><span class="sxs-lookup"><span data-stu-id="e71bf-116">The linearization should be applied only to the RGB channels and not to the alpha channel.</span></span>

<span data-ttu-id="e71bf-117">並非所有的表面格式都可以 linearized。</span><span class="sxs-lookup"><span data-stu-id="e71bf-117">Not all surface formats can be linearized.</span></span> <span data-ttu-id="e71bf-118">只有通過 [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) with D3DUSAGE \_ QUERY SRGBREAD 的格式 \_ 可以是 linearized。</span><span class="sxs-lookup"><span data-stu-id="e71bf-118">Only the formats that pass [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) with D3DUSAGE\_QUERY\_SRGBREAD can be linearized.</span></span> <span data-ttu-id="e71bf-119">\_其餘部分會忽略取樣器狀態 D3DSAMP SRGBTEXTURE。</span><span class="sxs-lookup"><span data-stu-id="e71bf-119">The sampler state D3DSAMP\_SRGBTEXTURE is ignored for the rest.</span></span> <span data-ttu-id="e71bf-120">只有未簽署的材質格式才支援這種轉換。</span><span class="sxs-lookup"><span data-stu-id="e71bf-120">Only unsigned texture formats are expected to support this conversion.</span></span> <span data-ttu-id="e71bf-121">不帶正負號的材質格式只包含 R、G、B 和 L 元件。</span><span class="sxs-lookup"><span data-stu-id="e71bf-121">Unsigned texture formats include only R, G, B, and L components.</span></span> <span data-ttu-id="e71bf-122">如果 Alpha 色板存在，則會予以忽略。</span><span class="sxs-lookup"><span data-stu-id="e71bf-122">If the alpha channel is present, it is ignored.</span></span> <span data-ttu-id="e71bf-123">如果混合格式支援 sRGB linearization，則只會影響不帶正負號的通道。</span><span class="sxs-lookup"><span data-stu-id="e71bf-123">If mixed formats support sRGB linearization, only the unsigned channels are affected.</span></span> <span data-ttu-id="e71bf-124">在理想的情況下，硬體應該在篩選之前執行 linearization，但在 Direct3D 9 中，硬體可以在篩選之後執行 linearization。</span><span class="sxs-lookup"><span data-stu-id="e71bf-124">Ideally, hardware should perform the linearization before filtering but in Direct3D 9, hardware is allowed to perform the linearization after filtering.</span></span>

<span data-ttu-id="e71bf-125">並非所有表面格式都可以在 sRGB 空間中撰寫。</span><span class="sxs-lookup"><span data-stu-id="e71bf-125">Not all surface formats can be written in sRGB space.</span></span> <span data-ttu-id="e71bf-126">只有傳遞 [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) 與使用旗標 D3DUSAGE 查詢 SRGBWRITE 的格式 \_ \_ 可以是 linearized。</span><span class="sxs-lookup"><span data-stu-id="e71bf-126">Only the formats that pass the [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) with the usage flag D3DUSAGE\_QUERY\_SRGBWRITE can be linearized.</span></span> <span data-ttu-id="e71bf-127">\_其餘部分會忽略轉譯狀態 D3DRS SRGBWRITEENABLE。</span><span class="sxs-lookup"><span data-stu-id="e71bf-127">The render state D3DRS\_SRGBWRITEENABLE is ignored for the rest.</span></span> <span data-ttu-id="e71bf-128">每個通道 RGB 未簽署格式的8個位預期會公開此功能。</span><span class="sxs-lookup"><span data-stu-id="e71bf-128">Eight bits per channel RGB unsigned formats are expected to expose this ability.</span></span>

<span data-ttu-id="e71bf-129">在理想的情況下，硬體應該線上性空間中執行框架緩衝區混合作業，但硬體可以在圖元著色器之後，但在框架緩衝區 blender 之前執行。</span><span class="sxs-lookup"><span data-stu-id="e71bf-129">Ideally, hardware should perform the frame buffer blending operations in the linear space, but hardware is allowed to perform it after the pixel shader but before the frame buffer blender.</span></span> <span data-ttu-id="e71bf-130">這表示在 sRGB 空間中進行的框架緩衝區混合作業將會產生不正確的結果。</span><span class="sxs-lookup"><span data-stu-id="e71bf-130">This means that the frame buffer blending operations that take place in sRGB space will produce incorrect results.</span></span> <span data-ttu-id="e71bf-131">\_執行明確轉譯目標時，會接受 D3DRS SRGBWRITEENABLE。</span><span class="sxs-lookup"><span data-stu-id="e71bf-131">D3DRS\_SRGBWRITEENABLE is honored while performing a clear of the render target.</span></span> <span data-ttu-id="e71bf-132">針對支援 [多個轉譯目標的硬體 (direct3d 9) ](multiple-render-targets.md) 或 [多元素紋理 (direct3d 9) ](multiple-element-textures.md)，則只會寫入第一個轉譯目標或元素。</span><span class="sxs-lookup"><span data-stu-id="e71bf-132">For hardware that supports [Multiple Render Targets (Direct3D 9)](multiple-render-targets.md) or [Multiple-element Textures (Direct3D 9)](multiple-element-textures.md), only the first render target or element is written.</span></span>

### <a name="api-changes"></a><span data-ttu-id="e71bf-133">API 變更</span><span class="sxs-lookup"><span data-stu-id="e71bf-133">API Changes</span></span>


```
// New sampler state (DWORD)
// If this is nonzero, the texture is linearized on lookup.
D3DSAMP_SRGBTEXTURE       // Default FALSE

// New render state (DWORD)
D3DRS_SRGBWRITEENABLE     // Default FALSE

// New usage flags
D3DUSAGE_QUERY_SRGBWRITE
D3DUSAGE_QUERY_SRGBREAD
```



### <a name="windowed-swap-chains"></a><span data-ttu-id="e71bf-134">視窗型交換鏈</span><span class="sxs-lookup"><span data-stu-id="e71bf-134">Windowed Swap Chains</span></span>

<span data-ttu-id="e71bf-135">應用程式會將其交換鏈的背景緩衝區保留線上性空間中，以啟用正確的混色作業，是很重要的。</span><span class="sxs-lookup"><span data-stu-id="e71bf-135">It is valuable for applications to keep the back buffers of their swap chains in linear space in order to enable correct blending operations.</span></span> <span data-ttu-id="e71bf-136">由於桌面通常不線上性空間中，因此必須先進行 gamma 修正，然後才能呈現背景緩衝區的內容。</span><span class="sxs-lookup"><span data-stu-id="e71bf-136">Since the desktop is typically not in linear space, a gamma correction is required before the contents of the back buffer can be presented.</span></span> <span data-ttu-id="e71bf-137">應用程式可以藉由配置額外的緩衝區，並從線性緩衝區執行自己的更正複製到背景緩衝區，來影響此修正本身。</span><span class="sxs-lookup"><span data-stu-id="e71bf-137">The application can effect this correction itself by allocating an additional buffer and performing its own correcting copy from the linear buffer to the back buffer.</span></span> <span data-ttu-id="e71bf-138">這需要額外的複本，如果驅動程式在展示 array.blit 中執行 gamma 修正，則可以避免此情況。</span><span class="sxs-lookup"><span data-stu-id="e71bf-138">This necessitates an extra copy which can be avoided if the driver performs gamma correction as part of the presentation blit.</span></span>

<span data-ttu-id="e71bf-139">在 Direct3D 9 中，有一個新的旗標（ [D3DPRESENT \_ 線性 \_ 內容](d3dpresent.md)） [**可供使用**](/windows/desktop/api) ，讓簡報從線性空間隱含轉換為 sRGB/gamma 2.2。</span><span class="sxs-lookup"><span data-stu-id="e71bf-139">In Direct3D 9 a new flag, [D3DPRESENT\_LINEAR\_CONTENT](d3dpresent.md), is available for [**Present**](/windows/desktop/api) that allows the presentation to implicitly convert from linear space to sRGB/gamma 2.2.</span></span> <span data-ttu-id="e71bf-140">如果背景緩衝區格式為16位浮點數以符合全螢幕 gamma 行為的視窗模式，則應用程式應指定此旗標， \_ \_ \_ \_ 並針對透過 [**GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps)抓取的裝置功能傳回 D3DCAPS3 線性至 SRGB 簡報。</span><span class="sxs-lookup"><span data-stu-id="e71bf-140">Applications should specify this flag if the backbuffer format is 16-bit floating point in order to match windowed mode present to full screen gamma behavior, provided D3DCAPS3\_LINEAR\_TO\_SRGB\_PRESENTATION is returned for device capabilities retrieved through [**GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e71bf-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="e71bf-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e71bf-142">框架緩衝區</span><span class="sxs-lookup"><span data-stu-id="e71bf-142">Frame Buffer</span></span>](frame-buffer.md)
</dt> </dl>

 

 

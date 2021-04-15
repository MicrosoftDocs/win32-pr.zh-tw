---
description: 當 Direct3D 轉譯原始物件時，會將 3D 原始物件對應到 2D 畫面上。
ms.assetid: vs|directx_sdk|~\texture_filtering.htm
title: " (Direct3D 9) 的材質篩選"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faeeb83e1a3bc7fc03534771b15b6076aeb48f8c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467771"
---
# <a name="texture-filtering-direct3d-9"></a><span data-ttu-id="fb02d-103"> (Direct3D 9) 的材質篩選</span><span class="sxs-lookup"><span data-stu-id="fb02d-103">Texture Filtering (Direct3D 9)</span></span>

<span data-ttu-id="fb02d-104">當 Direct3D 轉譯原始物件時，會將 3D 原始物件對應到 2D 畫面上。</span><span class="sxs-lookup"><span data-stu-id="fb02d-104">When Direct3D renders a primitive, it maps the 3D primitive onto a 2D screen.</span></span> <span data-ttu-id="fb02d-105">若原始物件帶有紋理，Direct3D 必須使用該紋理為原始物件的 2D 轉譯影像中的每個像素產生色彩。</span><span class="sxs-lookup"><span data-stu-id="fb02d-105">If the primitive has a texture, Direct3D must use that texture to produce a color for each pixel in the primitive's 2D rendered image.</span></span> <span data-ttu-id="fb02d-106">針對畫面上原始物件影像的每個像素，程式必須從紋理中取得色彩值。</span><span class="sxs-lookup"><span data-stu-id="fb02d-106">For every pixel in the primitive's on-screen image, it must obtain a color value from the texture.</span></span> <span data-ttu-id="fb02d-107">這個過程稱為「紋理篩選」。</span><span class="sxs-lookup"><span data-stu-id="fb02d-107">This process is called texture filtering.</span></span>

<span data-ttu-id="fb02d-108">執行紋理篩選作業時，通常也會放大或縮小使用的紋理。</span><span class="sxs-lookup"><span data-stu-id="fb02d-108">When a texture filter operation is performed, the texture being used is typically also being magnified or minified.</span></span> <span data-ttu-id="fb02d-109">換句話說，其會對應到比自身大或小的原始影像。</span><span class="sxs-lookup"><span data-stu-id="fb02d-109">In other words, it is being mapped into a primitive image that is larger or smaller than itself.</span></span> <span data-ttu-id="fb02d-110">放大紋理可能會導致許多像素對應到一個材質。</span><span class="sxs-lookup"><span data-stu-id="fb02d-110">Magnification of a texture can result in many pixels being mapped to one texel.</span></span> <span data-ttu-id="fb02d-111">其結果可能為外觀粗短。</span><span class="sxs-lookup"><span data-stu-id="fb02d-111">The result can be a chunky appearance.</span></span> <span data-ttu-id="fb02d-112">縮小紋理通常表示一個像素會對應到許多材質。</span><span class="sxs-lookup"><span data-stu-id="fb02d-112">Minification of a texture often means that a single pixel is mapped to many texels.</span></span> <span data-ttu-id="fb02d-113">其結果影像可能會顯得模糊或帶有鋸齒。</span><span class="sxs-lookup"><span data-stu-id="fb02d-113">The resulting image can be blurry or aliased.</span></span> <span data-ttu-id="fb02d-114">若要解決這些問題，您必須對材質色彩稍作混合，以達到像素的色彩。</span><span class="sxs-lookup"><span data-stu-id="fb02d-114">To resolve these problems, some blending of the texel colors must be performed to arrive at a color for the pixel.</span></span>

<span data-ttu-id="fb02d-115">Direct3D 將複雜的紋理篩選過程予以簡化。</span><span class="sxs-lookup"><span data-stu-id="fb02d-115">Direct3D simplifies the complex process of texture filtering.</span></span> <span data-ttu-id="fb02d-116">Direct3D 提供您三種紋理篩選的類型：線性篩選、非等向性篩選，及 Mipmap 篩選。</span><span class="sxs-lookup"><span data-stu-id="fb02d-116">It provides you with three types of texture filtering - linear filtering, anisotropic filtering, and mipmap filtering.</span></span> <span data-ttu-id="fb02d-117">如果您並未選擇任何紋理篩選方式，Direct3D 會使用一種稱作「最近點取樣」的技術。</span><span class="sxs-lookup"><span data-stu-id="fb02d-117">If you select no texture filtering, Direct3D uses a technique called nearest-point sampling.</span></span>

<span data-ttu-id="fb02d-118">每一種紋理篩選都有優點和缺點。</span><span class="sxs-lookup"><span data-stu-id="fb02d-118">Each type of texture filtering has advantages and disadvantages.</span></span> <span data-ttu-id="fb02d-119">例如：線性紋理篩選可能會使最終影像產生鋸齒狀的邊緣，或是矮胖的外觀。</span><span class="sxs-lookup"><span data-stu-id="fb02d-119">For instance, linear texture filtering can produce jagged edges or a chunky appearance in the final image.</span></span> <span data-ttu-id="fb02d-120">然而，其為運算上低負荷的一種紋理篩選方法。</span><span class="sxs-lookup"><span data-stu-id="fb02d-120">However, it is a computationally low-overhead method of texture filtering.</span></span> <span data-ttu-id="fb02d-121">使用 Mipmap 進行紋理篩選通常會產生最好的結果，特別是與非等向性篩選搭配使用時。</span><span class="sxs-lookup"><span data-stu-id="fb02d-121">Filtering with mipmaps usually produces the best results, especially when combined with anisotropic filtering.</span></span> <span data-ttu-id="fb02d-122">然而，其在 Direct3D 支援的技術中是最消耗記憶體的一種。</span><span class="sxs-lookup"><span data-stu-id="fb02d-122">However, it requires the most memory of the techniques that Direct3D supports.</span></span>

<span data-ttu-id="fb02d-123">使用紋理介面指標的應用程式應該透過呼叫 [**IDirect3DDevice9：： SetSamplerState**](/windows/desktop/api) 方法來設定目前的材質篩選方法。</span><span class="sxs-lookup"><span data-stu-id="fb02d-123">Applications that use texture interface pointers should set the current texture filtering method by calling the [**IDirect3DDevice9::SetSamplerState**](/windows/desktop/api) method.</span></span> <span data-ttu-id="fb02d-124">將第一個參數的值設定為您要選取材質篩選方法之材質 (0-7) 的整數索引編號。</span><span class="sxs-lookup"><span data-stu-id="fb02d-124">Set the value of the first parameter to the integer index number (0-7) of the texture for which you are selecting a texture filtering method.</span></span> <span data-ttu-id="fb02d-125">\_ \_ 針對第二個參數傳遞 D3DSAMP MAGFILTER、D3DSAMP MINFILTER 或 D3DSAMP \_ MIPFILTER，以設定放大、縮制或 mipmap 篩選。</span><span class="sxs-lookup"><span data-stu-id="fb02d-125">Pass D3DSAMP\_MAGFILTER, D3DSAMP\_MINFILTER, or D3DSAMP\_MIPFILTER for the second parameter to set the magnification, minification, or mipmapping filter.</span></span> <span data-ttu-id="fb02d-126">傳遞 [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) 列舉類型的成員作為第三個參數中的值。</span><span class="sxs-lookup"><span data-stu-id="fb02d-126">Pass a member of the [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) enumerated type as the value in the third parameter.</span></span>

<span data-ttu-id="fb02d-127">本節提供 Direct3D 支援的材質篩選方法。</span><span class="sxs-lookup"><span data-stu-id="fb02d-127">This section presents the texture filtering methods that Direct3D supports.</span></span> <span data-ttu-id="fb02d-128">它會組織成下列主題。</span><span class="sxs-lookup"><span data-stu-id="fb02d-128">It is organized into the following topics.</span></span>

-   [<span data-ttu-id="fb02d-129">最接近點取樣 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="fb02d-129">Nearest-Point Sampling (Direct3D 9)</span></span>](nearest-point-sampling.md)
-   [<span data-ttu-id="fb02d-130"> (Direct3D 9) 的線性材質篩選 </span><span class="sxs-lookup"><span data-stu-id="fb02d-130">Linear Texture Filtering (Direct3D 9)</span></span>](linear-texture-filtering.md)
-   [<span data-ttu-id="fb02d-131"> (Direct3D 9) 的雙線性材質篩選 </span><span class="sxs-lookup"><span data-stu-id="fb02d-131">Bilinear Texture Filtering (Direct3D 9)</span></span>](bilinear-texture-filtering.md)
-   [<span data-ttu-id="fb02d-132"> (Direct3D 9) 的非等向材質篩選 </span><span class="sxs-lookup"><span data-stu-id="fb02d-132">Anisotropic Texture Filtering (Direct3D 9)</span></span>](anisotropic-texture-filtering.md)
-   [<span data-ttu-id="fb02d-133">使用 Mipmap (Direct3D 9) 的材質篩選 </span><span class="sxs-lookup"><span data-stu-id="fb02d-133">Texture Filtering with Mipmaps (Direct3D 9)</span></span>](texture-filtering-with-mipmaps.md)

> [!Note]  
> <span data-ttu-id="fb02d-134">雖然 [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) 列舉型別中顯示的材質篩選轉譯狀態會被材質階段狀態取代，但 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)（相對於 IDirect3DDevice2 版本）不會在您嘗試使用時失敗。</span><span class="sxs-lookup"><span data-stu-id="fb02d-134">Although the texture-filtering render states present in the [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) enumerated type are superseded by texture stage states, the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate), as opposed to the IDirect3DDevice2 version, does not fail if you attempt to use them.</span></span> <span data-ttu-id="fb02d-135">相反地，系統會將這些轉譯狀態的效果對應至多紋理串聯（階段0）中的第一個階段。</span><span class="sxs-lookup"><span data-stu-id="fb02d-135">Rather, the system maps the effects of these render states to the first stage in the multitexture cascade, stage 0.</span></span> <span data-ttu-id="fb02d-136">應用程式不應該混用舊版轉譯狀態與其對應的材質階段狀態，因為可能會發生無法預期的結果。</span><span class="sxs-lookup"><span data-stu-id="fb02d-136">Applications should not mix the legacy render states with their corresponding texture stage states, as unpredictable results can occur.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="fb02d-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="fb02d-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb02d-138">Direct3D 紋理</span><span class="sxs-lookup"><span data-stu-id="fb02d-138">Direct3D Textures</span></span>](direct3d-textures.md)
</dt> </dl>

 

 

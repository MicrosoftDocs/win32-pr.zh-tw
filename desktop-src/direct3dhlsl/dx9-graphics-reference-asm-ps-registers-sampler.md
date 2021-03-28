---
title: " (Direct3D 9 asm-ps) 的取樣器"
description: 取樣器是圖元著色器的輸入虛擬註冊，用來識別取樣階段。
ms.assetid: 37cc28ae-fbd0-4f81-9e8e-f9609980d84e
keywords:
- '取樣器，輸入 (Direct3D 9 asm-ps) '
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77875eed0827ad6bcb6d89111b13b6a31232dd86
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023654"
---
# <a name="sampler-direct3d-9-asm-ps"></a><span data-ttu-id="6af59-104"> (Direct3D 9 asm-ps) 的取樣器</span><span class="sxs-lookup"><span data-stu-id="6af59-104">Sampler (Direct3D 9 asm-ps)</span></span>

<span data-ttu-id="6af59-105">取樣器是圖元著色器的輸入虛擬註冊，用來識別取樣階段。</span><span class="sxs-lookup"><span data-stu-id="6af59-105">A sampler is a input pseudo-register for a pixel shader, which is used to identify the sampling stage.</span></span> <span data-ttu-id="6af59-106">有16個圖元著色器取樣階段暫存器： s0 至 s15。</span><span class="sxs-lookup"><span data-stu-id="6af59-106">There are 16 pixel shader sampling stage registers: s0 to s15.</span></span> <span data-ttu-id="6af59-107">因此，您可以在單一著色器階段中讀取最多16個材質表面。</span><span class="sxs-lookup"><span data-stu-id="6af59-107">Therefore, up to 16 texture surfaces can be read in a single shader pass.</span></span> <span data-ttu-id="6af59-108">使用取樣器註冊的指示為 texld 和 texldp。</span><span class="sxs-lookup"><span data-stu-id="6af59-108">The instructions that use a sampler register are texld and texldp.</span></span>

<span data-ttu-id="6af59-109">在搭配使用 [ \_ (sm2、sm3-ps asm) ](dcl-samplertype---ps.md) 指令的 dcl 之前，必須先宣告取樣器。</span><span class="sxs-lookup"><span data-stu-id="6af59-109">Sampler must be declared before use with the [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md) instruction.</span></span>



| <span data-ttu-id="6af59-110">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="6af59-110">Pixel shader versions</span></span> | <span data-ttu-id="6af59-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="6af59-111">1\_1</span></span> | <span data-ttu-id="6af59-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="6af59-112">1\_2</span></span> | <span data-ttu-id="6af59-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="6af59-113">1\_3</span></span> | <span data-ttu-id="6af59-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="6af59-114">1\_4</span></span> | <span data-ttu-id="6af59-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6af59-115">2\_0</span></span> | <span data-ttu-id="6af59-116">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="6af59-116">2\_sw</span></span> | <span data-ttu-id="6af59-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="6af59-117">2\_x</span></span> | <span data-ttu-id="6af59-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6af59-118">3\_0</span></span> | <span data-ttu-id="6af59-119">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="6af59-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="6af59-120">取樣器</span><span class="sxs-lookup"><span data-stu-id="6af59-120">Sampler</span></span>               |      |      |      |      | <span data-ttu-id="6af59-121">x</span><span class="sxs-lookup"><span data-stu-id="6af59-121">x</span></span>    | <span data-ttu-id="6af59-122">x</span><span class="sxs-lookup"><span data-stu-id="6af59-122">x</span></span>     | <span data-ttu-id="6af59-123">x</span><span class="sxs-lookup"><span data-stu-id="6af59-123">x</span></span>    | <span data-ttu-id="6af59-124">x</span><span class="sxs-lookup"><span data-stu-id="6af59-124">x</span></span>    | <span data-ttu-id="6af59-125">x</span><span class="sxs-lookup"><span data-stu-id="6af59-125">x</span></span>     |



 

<span data-ttu-id="6af59-126">取樣器是虛擬暫存器，因為您無法直接讀取或寫入它們。</span><span class="sxs-lookup"><span data-stu-id="6af59-126">Samplers are pseudo registers because you cannot directly read or write to them.</span></span>

<span data-ttu-id="6af59-127">取樣單位會對應至材質取樣階段，封裝 [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate)所提供的取樣特定狀態。</span><span class="sxs-lookup"><span data-stu-id="6af59-127">A sampling unit corresponds to the texture sampling stage, encapsulating the sampling-specific state provided by [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).</span></span> <span data-ttu-id="6af59-128">每個取樣器都會唯一識別單一材質介面，此介面會使用 [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)設定為對應的取樣器。</span><span class="sxs-lookup"><span data-stu-id="6af59-128">Each sampler uniquely identifies a single texture surface, which is set to the corresponding sampler using the [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span></span> <span data-ttu-id="6af59-129">不過，您可以在多個取樣器設定相同的材質介面。</span><span class="sxs-lookup"><span data-stu-id="6af59-129">However, the same texture surface can be set at multiple samplers.</span></span>

<span data-ttu-id="6af59-130">在繪圖時，紋理不能同時設定為轉譯目標和某個階段的材質。</span><span class="sxs-lookup"><span data-stu-id="6af59-130">At draw time, a texture cannot be simultaneously set as a render target and a texture at a stage.</span></span>

<span data-ttu-id="6af59-131">取樣器可能會顯示為材質載入指令中的唯一引數： [texldl-ps](texldl---ps.md)。</span><span class="sxs-lookup"><span data-stu-id="6af59-131">A sampler might appear as the only argument in the texture load instruction: [texldl - ps](texldl---ps.md).</span></span>

<span data-ttu-id="6af59-132">在 ps \_ 3 \_ 0 中，如果使用取樣器，則必須使用 [dcl \_ samplerType (sm2、sm3 ps asm) ](dcl-samplertype---ps.md) 指令，在著色器程式的開頭宣告它。</span><span class="sxs-lookup"><span data-stu-id="6af59-132">In ps\_3\_0, if a sampler is used, it needs to be declared at the beginning of the shader program using the [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md) instruction.</span></span>

<span data-ttu-id="6af59-133">使用具有較高維度的材質來取樣紋理座標中的材質不合法。</span><span class="sxs-lookup"><span data-stu-id="6af59-133">Sampling a texture with a higher dimension than is present in the texture coordinates is illegal.</span></span> <span data-ttu-id="6af59-134">以較低的維度來取樣紋理座標中的材質將會忽略額外的材質座標。</span><span class="sxs-lookup"><span data-stu-id="6af59-134">Sampling a texture with a lower dimension than is present in the texture coordinates will ignore the extra texture coordinates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6af59-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="6af59-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6af59-136">寄存 器</span><span class="sxs-lookup"><span data-stu-id="6af59-136">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 
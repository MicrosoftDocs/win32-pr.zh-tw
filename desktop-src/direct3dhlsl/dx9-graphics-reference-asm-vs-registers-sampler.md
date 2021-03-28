---
title: " (Direct3D 9 asm 的取樣器-vs) "
description: 取樣器是頂點著色器的輸入虛擬登錄，用來識別取樣階段。 有四個頂點著色器 s0 至 s3。 您可以在單一著色器階段中讀取四個材質表面。
ms.assetid: a4588ced-24e2-4d4e-93e4-35a985bafaa4
keywords:
- '取樣器，輸入 (Direct3D 9 asm-vs) '
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 685f261da9d56dc29c0632d01cabbf29cd13a00f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382742"
---
# <a name="sampler-direct3d-9-asm-vs"></a><span data-ttu-id="f1fa4-106"> (Direct3D 9 asm 的取樣器-vs) </span><span class="sxs-lookup"><span data-stu-id="f1fa4-106">Sampler (Direct3D 9 asm-vs)</span></span>

<span data-ttu-id="f1fa4-107">取樣器是頂點著色器的輸入虛擬登錄，用來識別取樣階段。</span><span class="sxs-lookup"><span data-stu-id="f1fa4-107">A sampler is a input pseudo-register for a vertex shader, which is used to identify the sampling stage.</span></span> <span data-ttu-id="f1fa4-108">有四個頂點著色器取樣器： s0 至 s3。</span><span class="sxs-lookup"><span data-stu-id="f1fa4-108">There are four vertex shader samplers: s0 to s3.</span></span> <span data-ttu-id="f1fa4-109">您可以在單一著色器階段中讀取四個材質表面。</span><span class="sxs-lookup"><span data-stu-id="f1fa4-109">Four texture surfaces can be read in a single shader pass.</span></span>

<span data-ttu-id="f1fa4-110"> (Direct3D 9 asm-vs) s 的取樣器是虛擬暫存器，因為您無法直接讀取或寫入它們。</span><span class="sxs-lookup"><span data-stu-id="f1fa4-110">Sampler (Direct3D 9 asm-vs)s are pseudo registers because you cannot directly read or write to them.</span></span>

<span data-ttu-id="f1fa4-111">取樣單位會對應至材質取樣階段，封裝 [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate)所提供的取樣特定狀態。</span><span class="sxs-lookup"><span data-stu-id="f1fa4-111">A sampling unit corresponds to the texture sampling stage, encapsulating the sampling-specific state provided by [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).</span></span> <span data-ttu-id="f1fa4-112">每個取樣器都會唯一識別單一材質介面，此介面會使用 [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)設定為對應的取樣器。</span><span class="sxs-lookup"><span data-stu-id="f1fa4-112">Each sampler uniquely identifies a single texture surface, which is set to the corresponding sampler using the [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span></span> <span data-ttu-id="f1fa4-113">不過，您可以在多個取樣器設定相同的材質介面。</span><span class="sxs-lookup"><span data-stu-id="f1fa4-113">However, the same texture surface can be set at multiple samplers.</span></span>

<span data-ttu-id="f1fa4-114">在繪圖時，紋理不能同時設定為轉譯目標和某個階段的材質。</span><span class="sxs-lookup"><span data-stu-id="f1fa4-114">At draw time, a texture cannot be simultaneously set as a render target and a texture at a stage.</span></span>

<span data-ttu-id="f1fa4-115">由於有四個取樣器，因此在單一著色器階段中最多可以讀取四個材質表面。</span><span class="sxs-lookup"><span data-stu-id="f1fa4-115">Because there are four samplers, up to four texture surfaces can be read from in a single shader pass.</span></span> <span data-ttu-id="f1fa4-116">取樣器可能會在材質載入指示中顯示為唯一的引數： [texldl-vs](texldl---vs.md)。</span><span class="sxs-lookup"><span data-stu-id="f1fa4-116">A sampler might appear as the only argument in the texture load instruction: [texldl - vs](texldl---vs.md).</span></span>

<span data-ttu-id="f1fa4-117">在 vs \_ 3 \_ 0 中，如果使用取樣器，則必須在著色器程式的開頭使用 samplerType 來宣告， [ \_ (sm3-vs asm) ](dcl-samplertype---vs.md) 指令。</span><span class="sxs-lookup"><span data-stu-id="f1fa4-117">In vs\_3\_0, if a sampler is used, it needs to be declared at the beginning of the shader program using the [dcl\_samplerType (sm3 - vs asm)](dcl-samplertype---vs.md) instruction.</span></span>



| <span data-ttu-id="f1fa4-118">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="f1fa4-118">Vertex shader versions</span></span> | <span data-ttu-id="f1fa4-119">1\_1</span><span class="sxs-lookup"><span data-stu-id="f1fa4-119">1\_1</span></span> | <span data-ttu-id="f1fa4-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f1fa4-120">2\_0</span></span> | <span data-ttu-id="f1fa4-121">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="f1fa4-121">2\_sw</span></span> | <span data-ttu-id="f1fa4-122">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f1fa4-122">2\_x</span></span> | <span data-ttu-id="f1fa4-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f1fa4-123">3\_0</span></span> | <span data-ttu-id="f1fa4-124">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="f1fa4-124">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="f1fa4-125">取樣器</span><span class="sxs-lookup"><span data-stu-id="f1fa4-125">Sampler</span></span>                |      |      |       |      | <span data-ttu-id="f1fa4-126">x</span><span class="sxs-lookup"><span data-stu-id="f1fa4-126">x</span></span>    | <span data-ttu-id="f1fa4-127">x</span><span class="sxs-lookup"><span data-stu-id="f1fa4-127">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="f1fa4-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="f1fa4-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1fa4-129">頂點著色器暫存器</span><span class="sxs-lookup"><span data-stu-id="f1fa4-129">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> <dt>

[<span data-ttu-id="f1fa4-130">Vs \_ 3 \_ 0 (DirectX HLSL) 的頂點紋理 </span><span class="sxs-lookup"><span data-stu-id="f1fa4-130">Vertex Textures in vs\_3\_0 (DirectX HLSL)</span></span>](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0)
</dt> </dl>

 

 
---
title: texldd-ps
description: 使用額外的漸層輸入來取樣材質。
ms.assetid: 6d6b3180-d82e-4be4-929b-e5a6431bec38
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 72f3c4aaf9ac7e6beaad1343c024aa28bd2a85ab
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375368"
---
# <a name="texldd---ps"></a><span data-ttu-id="adb5a-103">texldd-ps</span><span class="sxs-lookup"><span data-stu-id="adb5a-103">texldd - ps</span></span>

<span data-ttu-id="adb5a-104">使用額外的漸層輸入來取樣材質。</span><span class="sxs-lookup"><span data-stu-id="adb5a-104">Samples a texture with additional gradient inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="adb5a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="adb5a-105">Syntax</span></span>



| <span data-ttu-id="adb5a-106">texldd、dst、src0、src1、src2 收取、src3</span><span class="sxs-lookup"><span data-stu-id="adb5a-106">texldd, dst, src0, src1, src2, src3</span></span> |
|-------------------------------------|



 

<span data-ttu-id="adb5a-107">其中：</span><span class="sxs-lookup"><span data-stu-id="adb5a-107">Where:</span></span>

-   <span data-ttu-id="adb5a-108">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="adb5a-108">dst is a destination register.</span></span>
-   <span data-ttu-id="adb5a-109">src0 是一種來源暫存器，可提供紋理範例的材質座標。</span><span class="sxs-lookup"><span data-stu-id="adb5a-109">src0 is a source register that provides the texture coordinates for the texture sample.</span></span> <span data-ttu-id="adb5a-110">請參閱 [材質座標註冊](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)。</span><span class="sxs-lookup"><span data-stu-id="adb5a-110">See [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span></span>
-   <span data-ttu-id="adb5a-111">src1 會識別來源取樣器 (s \#) ，其中 \# 指定要取樣的材質取樣器數目。</span><span class="sxs-lookup"><span data-stu-id="adb5a-111">src1 identifies the source sampler register (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="adb5a-112">取樣器已將材質與 [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) 列舉所定義的材質和控制項狀態相關聯 (例如。</span><span class="sxs-lookup"><span data-stu-id="adb5a-112">The sampler has associated with it a texture and a control state defined by the [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) enumeration (ex.</span></span> <span data-ttu-id="adb5a-113">D3DSAMP \_ MINFILTER) 。</span><span class="sxs-lookup"><span data-stu-id="adb5a-113">D3DSAMP\_MINFILTER).</span></span>
-   <span data-ttu-id="adb5a-114">src2 收取是指定 x 漸層的輸入來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="adb5a-114">src2 is an input source register that specifies the x gradient.</span></span>
-   <span data-ttu-id="adb5a-115">src3 是指定 y 漸層的輸入來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="adb5a-115">src3 is an input source register that specifies the y gradient.</span></span>

## <a name="remarks"></a><span data-ttu-id="adb5a-116">備註</span><span class="sxs-lookup"><span data-stu-id="adb5a-116">Remarks</span></span>



| <span data-ttu-id="adb5a-117">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="adb5a-117">Pixel shader versions</span></span> | <span data-ttu-id="adb5a-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="adb5a-118">1\_1</span></span> | <span data-ttu-id="adb5a-119">1\_2</span><span class="sxs-lookup"><span data-stu-id="adb5a-119">1\_2</span></span> | <span data-ttu-id="adb5a-120">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="adb5a-120">1\_3</span></span> | <span data-ttu-id="adb5a-121">1\_4</span><span class="sxs-lookup"><span data-stu-id="adb5a-121">1\_4</span></span> | <span data-ttu-id="adb5a-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="adb5a-122">2\_0</span></span> | <span data-ttu-id="adb5a-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="adb5a-123">2\_x</span></span> | <span data-ttu-id="adb5a-124">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="adb5a-124">2\_sw</span></span> | <span data-ttu-id="adb5a-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="adb5a-125">3\_0</span></span> | <span data-ttu-id="adb5a-126">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="adb5a-126">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="adb5a-127">texldd</span><span class="sxs-lookup"><span data-stu-id="adb5a-127">texldd</span></span>                |      |      |      |      |      | <span data-ttu-id="adb5a-128">X \*</span><span class="sxs-lookup"><span data-stu-id="adb5a-128">x \*</span></span> | <span data-ttu-id="adb5a-129">x</span><span class="sxs-lookup"><span data-stu-id="adb5a-129">x</span></span>     | <span data-ttu-id="adb5a-130">x</span><span class="sxs-lookup"><span data-stu-id="adb5a-130">x</span></span>    | <span data-ttu-id="adb5a-131">x</span><span class="sxs-lookup"><span data-stu-id="adb5a-131">x</span></span>     |



 

<span data-ttu-id="adb5a-132">\* 只有 ps 2 a 才支援此 \_ 指令 \_ 。</span><span class="sxs-lookup"><span data-stu-id="adb5a-132">\* This instruction is only supported by ps\_2\_a.</span></span> <span data-ttu-id="adb5a-133">Ps 2 b 不支援此 \_ 功能 \_ 。</span><span class="sxs-lookup"><span data-stu-id="adb5a-133">It is not supported by ps\_2\_b.</span></span> <span data-ttu-id="adb5a-134">如需設定檔的詳細資訊，請參閱 [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)。</span><span class="sxs-lookup"><span data-stu-id="adb5a-134">For more information about profiles, see [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile).</span></span>

<span data-ttu-id="adb5a-135">此指示會使用 src0、src1 所指定的取樣器和漸層 DSX 和 DSY 的材質座標來取樣材質。</span><span class="sxs-lookup"><span data-stu-id="adb5a-135">This instruction samples a texture using the texture coordinates at src0, the sampler specified by src1, and the gradients DSX and DSY coming from src2 and src3.</span></span> <span data-ttu-id="adb5a-136">X 和 y 漸層值是用來為取樣選取適當的紋理 mipmap 層級。</span><span class="sxs-lookup"><span data-stu-id="adb5a-136">The x and y gradient values are used to select the appropriate mipmap level of the texture for sampling.</span></span>

<span data-ttu-id="adb5a-137">所有來源都支援任意 swizzles。</span><span class="sxs-lookup"><span data-stu-id="adb5a-137">All sources support arbitrary swizzles.</span></span>

<span data-ttu-id="adb5a-138">所有寫入遮罩在目的地都有效。</span><span class="sxs-lookup"><span data-stu-id="adb5a-138">All write masks are valid on the destination.</span></span>

## <a name="related-topics"></a><span data-ttu-id="adb5a-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="adb5a-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="adb5a-140">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="adb5a-140">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
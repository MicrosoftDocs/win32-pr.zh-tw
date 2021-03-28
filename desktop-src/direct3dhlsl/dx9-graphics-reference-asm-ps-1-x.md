---
title: ps_1_1、ps_1_2、ps_1_3、ps_1_4
description: 圖元著色器組合器是由一組對暫存器中包含的圖元資料操作的指令所組成。
ms.assetid: 51b59f98-2fa8-4280-bc36-f4328a646168
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 761721a4de64e8a9168bcfea49ce7adf567ea7ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104182972"
---
# <a name="ps_1_1-ps_1_2-ps_1_3-ps_1_4"></a><span data-ttu-id="310b5-103">ps \_ 1 \_ 1、ps \_ 1 \_ 2、ps \_ 1 \_ 3、ps \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="310b5-103">ps\_1\_1, ps\_1\_2, ps\_1\_3, ps\_1\_4</span></span>

<span data-ttu-id="310b5-104">圖元著色器組合器是由一組對暫存器中包含的圖元資料操作的指令所組成。</span><span class="sxs-lookup"><span data-stu-id="310b5-104">The pixel shader assembler is made up of a set of instructions that operate on pixel data contained in registers.</span></span> <span data-ttu-id="310b5-105">作業會以運算子和一或多個運算元組成的指示來表示。</span><span class="sxs-lookup"><span data-stu-id="310b5-105">Operations are expressed as instructions comprised of an operator and one or more operands.</span></span> <span data-ttu-id="310b5-106">指示使用暫存器，將資料傳入和傳出圖元著色器 ALU。</span><span class="sxs-lookup"><span data-stu-id="310b5-106">Instructions use registers to transfer data in and out of the pixel shader ALU.</span></span> <span data-ttu-id="310b5-107">某些指示也可以使用暫存器來保留暫存結果。</span><span class="sxs-lookup"><span data-stu-id="310b5-107">Registers can also be used by some instructions to hold temporary results.</span></span>

> [!Note]  
> <span data-ttu-id="310b5-108">圖元著色器1.x 的 HLSL 支援已被取代。</span><span class="sxs-lookup"><span data-stu-id="310b5-108">HLSL support for pixel shader 1.x is deprecated.</span></span>

 

## <a name="instructions"></a><span data-ttu-id="310b5-109">指示</span><span class="sxs-lookup"><span data-stu-id="310b5-109">Instructions</span></span>

<span data-ttu-id="310b5-110">有兩個主要的圖元著色器指令類別：算術指令和材質定址指示。</span><span class="sxs-lookup"><span data-stu-id="310b5-110">There are two main categories of pixel shader instructions: arithmetic instructions and texture addressing instructions.</span></span> <span data-ttu-id="310b5-111">算術指令會修改色彩資料。</span><span class="sxs-lookup"><span data-stu-id="310b5-111">Arithmetic instructions modify color data.</span></span> <span data-ttu-id="310b5-112">材質定址作業會處理材質座標資料，在大部分情況下，則會取樣材質。</span><span class="sxs-lookup"><span data-stu-id="310b5-112">Texture addressing operations process texture coordinate data and in most cases, sample a texture.</span></span> <span data-ttu-id="310b5-113">圖元著色器指令會以每圖元為基礎執行;也就是說，它們不知道管線中的其他圖元。</span><span class="sxs-lookup"><span data-stu-id="310b5-113">Pixel shader instructions are run on a per-pixel basis; that is, they have no knowledge of other pixels in the pipeline.</span></span>

<span data-ttu-id="310b5-114">材質定址指示每個都使用一個位置，但可以將算術指令配對，以啟用兩個色彩元件 (RGB) 和一個插槽中的 Alpha 元件指令。</span><span class="sxs-lookup"><span data-stu-id="310b5-114">Texture addressing instructions each consume one slot, but arithmetic instructions can be paired to enable both color components (RGB) and an alpha component instruction in a single slot.</span></span>

<span data-ttu-id="310b5-115">[ps \_ 1 \_ 1、ps \_ 1 \_ 2、ps \_ 1 \_ 3、ps \_ 1 \_ 4 指示](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md) 包含可用指令的清單。</span><span class="sxs-lookup"><span data-stu-id="310b5-115">[ps\_1\_1, ps\_1\_2, ps\_1\_3, ps\_1\_4 Instructions](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md) contains a list of the available instructions.</span></span>

<span data-ttu-id="310b5-116">啟用取樣時，圖元著色器每圖元只會執行一次，而不是每個子圖元執行一次。</span><span class="sxs-lookup"><span data-stu-id="310b5-116">When multisampling is enabled, pixel shaders only get run once per pixel, not once for every subpixel.</span></span> <span data-ttu-id="310b5-117">取樣只會增加多邊形邊緣的解析度，以及深度和樣板測試。</span><span class="sxs-lookup"><span data-stu-id="310b5-117">Multisampling only increases the resolution of polygon edges, as well as depth and stencil tests.</span></span> <span data-ttu-id="310b5-118">例如，如果已啟用3x3 取樣，而且發現有一條圖元的三角形涵蓋了特定圖元之九個 subpixels 的五個，則圖元著色器會執行一次，而且相同的色彩結果會套用至所有五個 subpixels。</span><span class="sxs-lookup"><span data-stu-id="310b5-118">For example, if 3x3 multisampling is enabled, and a triangle being rasterized is found to cover five of the nine subpixels for a particular pixel, the pixel shader gets run once and the same color result is applied to all five subpixels.</span></span>

## <a name="registers"></a><span data-ttu-id="310b5-119">暫存器</span><span class="sxs-lookup"><span data-stu-id="310b5-119">Registers</span></span>

<span data-ttu-id="310b5-120">[ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 \_ \_ ps \_ 1 \_ 3 \_ \_ ps \_ 1 \_ 4 註冊](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)表列出著色器 ALU 所使用的不同暫存器。</span><span class="sxs-lookup"><span data-stu-id="310b5-120">[ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) lists the different registers used by the shader ALU.</span></span>

## <a name="modifiers"></a><span data-ttu-id="310b5-121">修飾詞</span><span class="sxs-lookup"><span data-stu-id="310b5-121">Modifiers</span></span>

<span data-ttu-id="310b5-122">您可以使用[ps \_ 1 \_ X](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-1-x.md)的修飾詞來變更指令的功能，或從登錄讀取或寫入的資料。</span><span class="sxs-lookup"><span data-stu-id="310b5-122">[Modifiers for ps\_1\_X](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-1-x.md) can be used to change the functionality of an instruction, or the data read from or written to a register.</span></span>

<span data-ttu-id="310b5-123">Direct3D 9 需要中繼計算以針對所有表面格式維持至少8位的有效位數。</span><span class="sxs-lookup"><span data-stu-id="310b5-123">Direct3D 9 requires intermediate computations to maintain at least 8-bit precision for all surface formats.</span></span> <span data-ttu-id="310b5-124">針對進行中的數學，較高的精確度 (12 位) ，建議使用紋理階段之間的飽和度到8位。</span><span class="sxs-lookup"><span data-stu-id="310b5-124">Both higher precision (12-bit) for in-stage math, and saturation to 8-bits between texture stages are recommended.</span></span> <span data-ttu-id="310b5-125">不支援可修改的舍入模式或例外狀況。</span><span class="sxs-lookup"><span data-stu-id="310b5-125">No modifiable rounding modes or exceptions are supported.</span></span> <span data-ttu-id="310b5-126">應以四捨五入到最接近的精確度來支援乘法，以保持最小精確度的精確度。</span><span class="sxs-lookup"><span data-stu-id="310b5-126">Multiplication should be supported with a round-to-nearest precision to keep precision loss to a minimum.</span></span>

## <a name="sampler-count"></a><span data-ttu-id="310b5-127">取樣器計數</span><span class="sxs-lookup"><span data-stu-id="310b5-127">Sampler Count</span></span>

<span data-ttu-id="310b5-128">可用的紋理取樣器數目如下：</span><span class="sxs-lookup"><span data-stu-id="310b5-128">The number of texture samplers available is:</span></span>

-   <span data-ttu-id="310b5-129">若是 ps \_ 1 \_ 0-ps \_ 1 \_ 3，最大值為4。</span><span class="sxs-lookup"><span data-stu-id="310b5-129">For ps\_1\_0 - ps\_1\_3, the maximum is 4.</span></span>
-   <span data-ttu-id="310b5-130">針對 ps \_ 1 \_ 4，最大值為6。</span><span class="sxs-lookup"><span data-stu-id="310b5-130">For ps\_1\_4, the maximum is 6.</span></span>

## <a name="related-topics"></a><span data-ttu-id="310b5-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="310b5-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="310b5-132">圖元著色器</span><span class="sxs-lookup"><span data-stu-id="310b5-132">Pixel Shaders</span></span>](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 





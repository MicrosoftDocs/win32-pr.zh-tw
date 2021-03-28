---
title: 圖元著色器階段
description: 圖元著色器階段 (PS) 啟用豐富的陰影技術，例如每圖元光源和後置處理。
ms.assetid: 09831B10-4FD1-41E7-8D81-5AA63DC90020
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57142e9c32919a6959a7fac14bf544cca1dacd79
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093043"
---
# <a name="pixel-shader-stage"></a><span data-ttu-id="be176-103">圖元著色器階段</span><span class="sxs-lookup"><span data-stu-id="be176-103">Pixel Shader Stage</span></span>

<span data-ttu-id="be176-104">圖元著色器階段 (PS) 啟用豐富的陰影技術，例如每圖元光源和後置處理。</span><span class="sxs-lookup"><span data-stu-id="be176-104">The pixel-shader stage (PS) enables rich shading techniques such as per-pixel lighting and post-processing.</span></span> <span data-ttu-id="be176-105">像素著色器是結合常數變數、紋理資料、插補每個頂點值和其他資料的程式，以產生每個像素的輸出。</span><span class="sxs-lookup"><span data-stu-id="be176-105">A pixel shader is a program that combines constant variables, texture data, interpolated per-vertex values, and other data to produce per-pixel outputs.</span></span> <span data-ttu-id="be176-106">轉譯器階段會針對基本型別所涵蓋的每個圖元叫用一次圖元著色器，不過，您可以指定 **Null** 著色器來避免執行著色器。</span><span class="sxs-lookup"><span data-stu-id="be176-106">The rasterizer stage invokes a pixel shader once for each pixel covered by a primitive, however, it is possible to specify a **NULL** shader to avoid running a shader.</span></span>

## <a name="the-pixel-shader"></a><span data-ttu-id="be176-107">圖元著色器</span><span class="sxs-lookup"><span data-stu-id="be176-107">The Pixel Shader</span></span>

<span data-ttu-id="be176-108">多重取樣紋理時，像素著色器會在每個涵蓋的多重取樣發生深度/樣板測試期間，叫用一次每個涵蓋像素。</span><span class="sxs-lookup"><span data-stu-id="be176-108">When multisampling a texture, a pixel shader is invoked once per-covered pixel while a depth/stencil test occurs for each covered multisample.</span></span> <span data-ttu-id="be176-109">通過深度/樣板測試的樣本會以像素著色器輸出色彩進行更新。</span><span class="sxs-lookup"><span data-stu-id="be176-109">Samples that pass the depth/stencil test are updated with the pixel shader output color.</span></span>

<span data-ttu-id="be176-110">像素著色器的內建功能會產生或使用數量的導數，與螢幕空間 x 和 y 相關。</span><span class="sxs-lookup"><span data-stu-id="be176-110">The pixel shader intrinsic functions produce or use derivatives of quantities with respect to screen space x and y.</span></span> <span data-ttu-id="be176-111">導數的常見用途是計算紋理取樣的詳細層級，而在非等向性篩選的案例中，選取樣本連同非等向性軸。</span><span class="sxs-lookup"><span data-stu-id="be176-111">The most common use for derivatives is to compute level-of-detail calculations for texture sampling and in the case of anisotropic filtering, selecting samples along the axis of anisotropy.</span></span> <span data-ttu-id="be176-112">通常的硬體實作會同時對多個像素執行像素著色器 (例如 2x2 格線)，如此在像素著色器中運算的數量導數可以合理地在相鄰的相同執行點大略估算為差異值。</span><span class="sxs-lookup"><span data-stu-id="be176-112">Typically, a hardware implementation runs a pixel shader on multiple pixels (for example a 2x2 grid) simultaneously, so that derivatives of quantities computed in the pixel shader can be reasonably approximated as deltas of the values at the same point of execution in adjacent pixels.</span></span>

### <a name="inputs"></a><span data-ttu-id="be176-113">輸入</span><span class="sxs-lookup"><span data-stu-id="be176-113">Inputs</span></span>

<span data-ttu-id="be176-114">若管線設定後沒有幾何著色器，像素著色器限於 16、32 位元、4 個元件的輸入。</span><span class="sxs-lookup"><span data-stu-id="be176-114">When the pipeline is configured without a geometry shader, a pixel shader is limited to 16, 32-bit, 4-component inputs.</span></span> <span data-ttu-id="be176-115">否則，像素著色器最多可以採用 32、32 位元、4 個元件的輸入。</span><span class="sxs-lookup"><span data-stu-id="be176-115">Otherwise, a pixel shader can take up to 32, 32-bit, 4-component inputs.</span></span>

<span data-ttu-id="be176-116">像素著色器輸入資料包括頂點屬性 (可插補，無論是否有透視修正)，也可以視為每個基本類型常數。</span><span class="sxs-lookup"><span data-stu-id="be176-116">Pixel shader input data includes vertex attributes (that can be interpolated with or without perspective correction) or can be treated as per-primitive constants.</span></span> <span data-ttu-id="be176-117">像素著色器輸入會從點陣化的基本類型的頂點屬性插補，根據宣告的插補模式。</span><span class="sxs-lookup"><span data-stu-id="be176-117">Pixel shader inputs are interpolated from the vertex attributes of the primitive being rasterized, based on the interpolation mode declared.</span></span> <span data-ttu-id="be176-118">如果在點陣化之前基本類型被裁剪，則插補模式也會在裁剪過程中採用。</span><span class="sxs-lookup"><span data-stu-id="be176-118">If a primitive gets clipped before rasterization, the interpolation mode is honored during the clipping process as well.</span></span>

<span data-ttu-id="be176-119">頂點屬性是在像素著色器中心位置插補 (或評估)。</span><span class="sxs-lookup"><span data-stu-id="be176-119">Vertex attributes are interpolated (or evaluated) at pixel shader center locations.</span></span> <span data-ttu-id="be176-120">像素著色器屬性插補模式會在輸入登錄宣告中宣告，以每個元素為基礎，如[引數](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-parameters)或[輸入結構](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-struct)。</span><span class="sxs-lookup"><span data-stu-id="be176-120">Pixel shader attribute interpolation modes are declared in an input register declaration, on a per-element basis in either an [argument](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-parameters) or an [input structure](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-struct).</span></span> <span data-ttu-id="be176-121">可以用線性方式或使用 [距心取樣](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx)來插入屬性。</span><span class="sxs-lookup"><span data-stu-id="be176-121">Attributes can be interpolated linearly, or with [centroid sampling](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx).</span></span> <span data-ttu-id="be176-122">距心評估只在多重取樣到基本類型所涵蓋的像素時相關，但像素中心可能不是；距心評估盡可能發生在靠近 (非涵蓋) 像素中心。</span><span class="sxs-lookup"><span data-stu-id="be176-122">Centroid evaluation is relevant only during multisampling to cover cases where a pixel is covered by a primitive but a pixel center may not be; centroid evaluation occurs as close as possible to the (non-covered) pixel center.</span></span>

<span data-ttu-id="be176-123">輸入也可以使用[系統值語意](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)宣告，這會由其他管線階段使用的參數標記。</span><span class="sxs-lookup"><span data-stu-id="be176-123">Inputs may also be declared with a [system-value semantic](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics), which marks a parameter that is consumed by other pipeline stages.</span></span> <span data-ttu-id="be176-124">例如，圖元位置應該以 SV \_ 位置語義標記。</span><span class="sxs-lookup"><span data-stu-id="be176-124">For instance, a pixel position should be marked with the SV\_Position semantic.</span></span> <span data-ttu-id="be176-125">IA 階段可以針對使用 SV PrimitiveID)  (的圖元著色器產生一個純量 \_ ; 轉譯器階段也可以為圖元著色器產生一個純量， (使用 sv \_ IsFrontFace) 。</span><span class="sxs-lookup"><span data-stu-id="be176-125">The IA stage can produce one scalar for a pixel shader (using SV\_PrimitiveID); the rasterizer stage can also generate one scalar for a pixel shader (using SV\_IsFrontFace).</span></span>

### <a name="outputs"></a><span data-ttu-id="be176-126">輸出</span><span class="sxs-lookup"><span data-stu-id="be176-126">Outputs</span></span>

<span data-ttu-id="be176-127">像素著色器可以輸出最多 8、32 位元、4 個元件的色彩，或無色彩 (如果捨棄像素)。</span><span class="sxs-lookup"><span data-stu-id="be176-127">A pixel shader can output up to 8, 32-bit, 4-component colors, or no color if the pixel is discarded.</span></span> <span data-ttu-id="be176-128">像素著色器輸出暫存器元件必須先宣告，才能使用；每個暫存器可以有不同的輸出寫入遮罩。</span><span class="sxs-lookup"><span data-stu-id="be176-128">Pixel shader output register components must be declared before they can be used; each register is allowed a distinct output-write mask.</span></span>

<span data-ttu-id="be176-129">您可以使用 [輸出合併] 階段中的深度寫入啟用狀態 () 來控制是否要將深度資料寫入深度緩衝區 (或使用捨棄指令來捨棄該圖元) 的資料。</span><span class="sxs-lookup"><span data-stu-id="be176-129">Use the depth-write-enable state (in the output-merger stage) to control whether depth data gets written to a depth buffer (or use the discard instruction to discard data for that pixel).</span></span> <span data-ttu-id="be176-130">圖元著色器也可以輸出選擇性的32位、1元件、浮點數、深度測試值，以使用 SV \_ 深度語義)  (深度測試。</span><span class="sxs-lookup"><span data-stu-id="be176-130">A pixel shader can also output an optional 32-bit, 1-component, floating-point, depth value for depth testing (using the SV\_Depth semantic).</span></span> <span data-ttu-id="be176-131">深度值是在 oDepth 登錄中輸出，並會取代深度測試的插補深度值 (假設已啟用深度測試的話)。</span><span class="sxs-lookup"><span data-stu-id="be176-131">The depth value is output in the oDepth register, and replaces the interpolated depth value for depth testing (assuming depth testing is enabled).</span></span> <span data-ttu-id="be176-132">無法在使用固定函式深度或著色器 oDepth 之間動態變更。</span><span class="sxs-lookup"><span data-stu-id="be176-132">There is no way to dynamically change between using fixed-function depth or shader oDepth.</span></span>

<span data-ttu-id="be176-133">像素著色器無法輸出樣板值。</span><span class="sxs-lookup"><span data-stu-id="be176-133">A pixel shader cannot output a stencil value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="be176-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="be176-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be176-135">圖形管線</span><span class="sxs-lookup"><span data-stu-id="be176-135">Graphics Pipeline</span></span>](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[<span data-ttu-id="be176-136"> (Direct3D 10) 的管線階段 </span><span class="sxs-lookup"><span data-stu-id="be176-136">Pipeline Stages (Direct3D 10)</span></span>](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 
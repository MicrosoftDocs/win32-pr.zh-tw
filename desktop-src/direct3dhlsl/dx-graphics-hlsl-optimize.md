---
title: 優化 HLSL 著色器
description: 本章節描述您可以用來優化著色器的一般用途策略。 您可以在任何平臺上，將這些策略套用到以任何語言撰寫的著色器。
ms.assetid: 014b9cb3-a489-48d7-8174-b97de168bf3a
keywords:
- 高階著色器語言
- HLSL，效能
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 06d3bb806e98e489020aa1755ef2a6c952459d86
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021836"
---
# <a name="optimizing-hlsl-shaders"></a><span data-ttu-id="0afe2-106">優化 HLSL 著色器</span><span class="sxs-lookup"><span data-stu-id="0afe2-106">Optimizing HLSL Shaders</span></span>

<span data-ttu-id="0afe2-107">本章節描述您可以用來優化著色器的一般用途策略。</span><span class="sxs-lookup"><span data-stu-id="0afe2-107">This section describes general-purpose strategies that you can use to optimize your shaders.</span></span> <span data-ttu-id="0afe2-108">您可以在任何平臺上，將這些策略套用到以任何語言撰寫的著色器。</span><span class="sxs-lookup"><span data-stu-id="0afe2-108">You can apply these strategies to shaders that are written in any language, on any platform.</span></span>

-   [<span data-ttu-id="0afe2-109">知道要在哪裡執行著色器計算</span><span class="sxs-lookup"><span data-stu-id="0afe2-109">Know Where To Perform Shader Calculations</span></span>](#know-where-to-perform-shader-calculations)
-   [<span data-ttu-id="0afe2-110">略過不必要的指示</span><span class="sxs-lookup"><span data-stu-id="0afe2-110">Skip Unnecessary Instructions</span></span>](#skip-unnecessary-instructions)
-   [<span data-ttu-id="0afe2-111">套件變數和 Interpolants</span><span class="sxs-lookup"><span data-stu-id="0afe2-111">Pack Variables and Interpolants</span></span>](#pack-variables-and-interpolants)
-   [<span data-ttu-id="0afe2-112">減少著色器複雜度</span><span class="sxs-lookup"><span data-stu-id="0afe2-112">Reduce Shader Complexity</span></span>](#reduce-shader-complexity)
-   [<span data-ttu-id="0afe2-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="0afe2-113">Related Topics</span></span>](#related-topics)
-   [<span data-ttu-id="0afe2-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="0afe2-114">Related topics</span></span>](#related-topics)

## <a name="know-where-to-perform-shader-calculations"></a><span data-ttu-id="0afe2-115">知道要在哪裡執行著色器計算</span><span class="sxs-lookup"><span data-stu-id="0afe2-115">Know Where To Perform Shader Calculations</span></span>

<span data-ttu-id="0afe2-116">頂點著色器會執行作業，包括提取頂點和執行矩陣資料的矩陣轉換。</span><span class="sxs-lookup"><span data-stu-id="0afe2-116">Vertex shaders perform operations that include fetching vertices and performing matrix transformation of vertex data.</span></span> <span data-ttu-id="0afe2-117">一般來說，每個頂點都會執行一次頂點著色器。</span><span class="sxs-lookup"><span data-stu-id="0afe2-117">Typically, vertex shaders are executed once per vertex.</span></span>

<span data-ttu-id="0afe2-118">圖元著色器會執行包括提取材質資料和執行光源計算的作業。</span><span class="sxs-lookup"><span data-stu-id="0afe2-118">Pixel Shaders perform operations that include fetching texture data and performing lighting calculations.</span></span> <span data-ttu-id="0afe2-119">一般而言，圖元著色器會針對指定的幾何片段，每個圖元執行一次。</span><span class="sxs-lookup"><span data-stu-id="0afe2-119">Typically, pixel shaders are executed once per pixel for a given piece of geometry.</span></span>

<span data-ttu-id="0afe2-120">一般而言，圖元會人數超過場景中的頂點，因此圖元著色器的執行頻率會比頂點著色器更頻繁。</span><span class="sxs-lookup"><span data-stu-id="0afe2-120">Typically, pixels outnumber vertices in a scene, so pixel shaders execute more often than vertex shaders.</span></span>

<span data-ttu-id="0afe2-121">當您設計著色器演算法時，請記住下列事項：</span><span class="sxs-lookup"><span data-stu-id="0afe2-121">When you design shader algorithms, keep the following in mind:</span></span>

-   <span data-ttu-id="0afe2-122">可能的話，請在頂點著色器上執行計算。</span><span class="sxs-lookup"><span data-stu-id="0afe2-122">Perform calculations on the vertex shader if possible.</span></span> <span data-ttu-id="0afe2-123">在圖元著色器上執行的計算，比在頂點著色器上執行的計算更昂貴。</span><span class="sxs-lookup"><span data-stu-id="0afe2-123">A calculation that is performed on a pixel shader is much more expensive than a calculation that is performed on a vertex shader.</span></span>
-   <span data-ttu-id="0afe2-124">考慮使用每個頂點計算，以改善密集網格等情況下的效能。</span><span class="sxs-lookup"><span data-stu-id="0afe2-124">Consider using per-vertex calculations to improve performance in situations such as dense meshes.</span></span> <span data-ttu-id="0afe2-125">針對密集網格，每個頂點計算可能產生的結果，會與每個圖元計算產生的結果以視覺化方式區分。</span><span class="sxs-lookup"><span data-stu-id="0afe2-125">For dense meshes, per-vertex calculations may produce results that are visually indistinguishable from results produced with per-pixel calculations.</span></span>

## <a name="skip-unnecessary-instructions"></a><span data-ttu-id="0afe2-126">略過不必要的指示</span><span class="sxs-lookup"><span data-stu-id="0afe2-126">Skip Unnecessary Instructions</span></span>

<span data-ttu-id="0afe2-127">在 HLSL 中，動態分支能讓您限制執行的指令數目。</span><span class="sxs-lookup"><span data-stu-id="0afe2-127">In HLSL, dynamic branching provides the ability to limit the number of instructions that are executed.</span></span> <span data-ttu-id="0afe2-128">因此，動態分支可協助加速著色器執行時間。</span><span class="sxs-lookup"><span data-stu-id="0afe2-128">Therefore, dynamic branching can help speed up shader execution time.</span></span> <span data-ttu-id="0afe2-129">如果未顯示幾何或圖元，請使用動態分支來結束著色器或限制指令。</span><span class="sxs-lookup"><span data-stu-id="0afe2-129">If geometry or pixels are not displayed, use dynamic branching to exit the shader or to limit instructions.</span></span> <span data-ttu-id="0afe2-130">例如，如果圖元不亮，則不會有執行光源演算法的點。</span><span class="sxs-lookup"><span data-stu-id="0afe2-130">For example, if a pixel is not lit, there is no point in executing the lighting algorithm.</span></span>

<span data-ttu-id="0afe2-131">下表列出您可以在著色器中測試條件，並使用動態分支來略過不必要指示的一些案例。</span><span class="sxs-lookup"><span data-stu-id="0afe2-131">The following table lists some cases where you can test conditions in your shader and use dynamic branching to skip unnecessary instructions.</span></span> <span data-ttu-id="0afe2-132">資料表並不完整。</span><span class="sxs-lookup"><span data-stu-id="0afe2-132">The table not comprehensive.</span></span> <span data-ttu-id="0afe2-133">相反地，它的目的是要提供您將程式碼優化的概念。</span><span class="sxs-lookup"><span data-stu-id="0afe2-133">Rather, it is intended to give you ideas for optimizing your code.</span></span>



| <span data-ttu-id="0afe2-134">要檢查的條件</span><span class="sxs-lookup"><span data-stu-id="0afe2-134">Condition to Check</span></span>                                    | <span data-ttu-id="0afe2-135">著色器中的回應</span><span class="sxs-lookup"><span data-stu-id="0afe2-135">Response in the Shader</span></span>       |
|-------------------------------------------------------|------------------------------|
| <span data-ttu-id="0afe2-136">Alpha 檢查會判斷不會顯示圖元。</span><span class="sxs-lookup"><span data-stu-id="0afe2-136">Alpha check determines that a pixel will not be seen.</span></span> | <span data-ttu-id="0afe2-137">略過著色器的其餘部分。</span><span class="sxs-lookup"><span data-stu-id="0afe2-137">Skip the rest of the shader.</span></span> |
| <span data-ttu-id="0afe2-138">圖元或幾何完全 fogged。</span><span class="sxs-lookup"><span data-stu-id="0afe2-138">The pixel or geometry is fully fogged.</span></span>                | <span data-ttu-id="0afe2-139">略過著色器的其餘部分。</span><span class="sxs-lookup"><span data-stu-id="0afe2-139">Skip the rest of the shader.</span></span> |
| <span data-ttu-id="0afe2-140">外觀權重為零。</span><span class="sxs-lookup"><span data-stu-id="0afe2-140">Skin weights are zero.</span></span>                                | <span data-ttu-id="0afe2-141">略過骨骼。</span><span class="sxs-lookup"><span data-stu-id="0afe2-141">Skip bones.</span></span>                  |
| <span data-ttu-id="0afe2-142">淺衰減是零。</span><span class="sxs-lookup"><span data-stu-id="0afe2-142">Light attenuation is zero.</span></span>                            | <span data-ttu-id="0afe2-143">略過光源。</span><span class="sxs-lookup"><span data-stu-id="0afe2-143">Skip lighting.</span></span>               |
| <span data-ttu-id="0afe2-144">非正面的 Lambertian 字詞。</span><span class="sxs-lookup"><span data-stu-id="0afe2-144">Non-positive Lambertian term.</span></span>                         | <span data-ttu-id="0afe2-145">略過光源。</span><span class="sxs-lookup"><span data-stu-id="0afe2-145">Skip lighting.</span></span>               |



 

## <a name="pack-variables-and-interpolants"></a><span data-ttu-id="0afe2-146">套件變數和 Interpolants</span><span class="sxs-lookup"><span data-stu-id="0afe2-146">Pack Variables and Interpolants</span></span>

<span data-ttu-id="0afe2-147">請注意著色器資料所需的空間。</span><span class="sxs-lookup"><span data-stu-id="0afe2-147">Be mindful of the space required for shader data.</span></span> <span data-ttu-id="0afe2-148">盡可能將最多的資訊封裝到變數或 interpolant 中。</span><span class="sxs-lookup"><span data-stu-id="0afe2-148">Pack as much information into a variable or interpolant as possible.</span></span> <span data-ttu-id="0afe2-149">有時候，來自兩個變數的資訊可以封裝至單一變數的記憶體空間中。</span><span class="sxs-lookup"><span data-stu-id="0afe2-149">Sometimes, the information from two variables can be packed into the memory space of a single variable.</span></span>

## <a name="reduce-shader-complexity"></a><span data-ttu-id="0afe2-150">減少著色器複雜度</span><span class="sxs-lookup"><span data-stu-id="0afe2-150">Reduce Shader Complexity</span></span>

<span data-ttu-id="0afe2-151">將著色器保持在小型和簡單的部分。</span><span class="sxs-lookup"><span data-stu-id="0afe2-151">Keep your shaders small and simple.</span></span> <span data-ttu-id="0afe2-152">一般情況下，使用較少指令執行的著色器會以更多的指令著色器執行得更快。</span><span class="sxs-lookup"><span data-stu-id="0afe2-152">In general, shaders with fewer instructions execute more quickly than shaders with more instructions.</span></span> <span data-ttu-id="0afe2-153">您也可以更輕鬆地對較小、較不復雜的著色器進行調試和優化。</span><span class="sxs-lookup"><span data-stu-id="0afe2-153">It is also easier to debug and optimize smaller, less complex shaders.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0afe2-154">[相關主題]</span><span class="sxs-lookup"><span data-stu-id="0afe2-154">Related Topics</span></span>

[<span data-ttu-id="0afe2-155">HLSL 的程式設計指南</span><span class="sxs-lookup"><span data-stu-id="0afe2-155">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a><span data-ttu-id="0afe2-156">相關主題</span><span class="sxs-lookup"><span data-stu-id="0afe2-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0afe2-157">HLSL 的程式設計指南</span><span class="sxs-lookup"><span data-stu-id="0afe2-157">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 





---
title: HLSL 程式設計指南
description: 資料會將圖形管線輸入為基本類型的資料流程，並由著色器階段處理。
ms.assetid: 4894e085-30e7-4cc5-8ae6-a84b601e4ce3
ms.topic: article
ms.date: 02/21/2019
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cd242efaaf3cdb44f424a603f2fc522dda540ec8
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/12/2021
ms.locfileid: "104973860"
---
# <a name="programming-guide-for-hlsl"></a><span data-ttu-id="ca217-103">HLSL 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="ca217-103">Programming guide for HLSL</span></span>

<span data-ttu-id="ca217-104">資料會將圖形管線輸入為基本類型的資料流程，並由著色器階段處理。</span><span class="sxs-lookup"><span data-stu-id="ca217-104">Data enters the graphics pipeline as a stream of primitives and is processed by the shader stages.</span></span> <span data-ttu-id="ca217-105">實際的著色器階段相依于 Direct3D 版本，但一定要包含頂點、圖元和幾何階段。</span><span class="sxs-lookup"><span data-stu-id="ca217-105">The actual shader stages depend on the version of Direct3D, but certainly include the vertex, pixel and geometry stages.</span></span> <span data-ttu-id="ca217-106">其他階段包括鑲嵌和計算著色器的輪廓和網域著色器。</span><span class="sxs-lookup"><span data-stu-id="ca217-106">Other stages include the hull and domain shaders for tessellation, and the compute shader.</span></span> <span data-ttu-id="ca217-107">這些階段可使用高階的陰影語言 ([HLSL](dx-graphics-hlsl-reference.md)) 來完全進行程式設計。</span><span class="sxs-lookup"><span data-stu-id="ca217-107">These stages are completely programmable using the High Level Shading Language ([HLSL](dx-graphics-hlsl-reference.md)).</span></span>

<span data-ttu-id="ca217-108">HLSL 著色器可以在作者或執行時間進行編譯，並在執行時間設定為適當的管線階段。</span><span class="sxs-lookup"><span data-stu-id="ca217-108">HLSL shaders can be compiled at author-time or at runtime, and set at runtime into the appropriate pipeline stage.</span></span> <span data-ttu-id="ca217-109">Direct3D 9 著色器可以使用 [著色器模型 1](dx-graphics-hlsl-sm1.md)、 [著色器模型 2](dx-graphics-hlsl-sm2.md) 和 [著色器模型 3](dx-graphics-hlsl-sm3.md)來設計;Direct3D 10 著色器只能設計于 [著色器模型 4](dx-graphics-hlsl-sm4.md)。</span><span class="sxs-lookup"><span data-stu-id="ca217-109">Direct3D 9 shaders can be designed using [shader model 1](dx-graphics-hlsl-sm1.md), [shader model 2](dx-graphics-hlsl-sm2.md) and [shader model 3](dx-graphics-hlsl-sm3.md); Direct3D 10 shaders can only be designed on [shader model 4](dx-graphics-hlsl-sm4.md).</span></span> <span data-ttu-id="ca217-110">您可以在 [著色器模型 5](d3d11-graphics-reference-sm5.md)上設計 Direct3D 11 著色器。</span><span class="sxs-lookup"><span data-stu-id="ca217-110">Direct3D 11 shaders can be designed on [shader model 5](d3d11-graphics-reference-sm5.md).</span></span> <span data-ttu-id="ca217-111">您可以在 [著色器模型 5.1](shader-model-5-1.md)上設計 direct3d 11.3 和 direct3d 12，而且也可以在 [著色器模型 6](shader-model-6-0.md)上設計 direct3d 12。</span><span class="sxs-lookup"><span data-stu-id="ca217-111">Direct3D 11.3 and Direct3D 12 can be designed on [shader model 5.1](shader-model-5-1.md), and Direct3D 12 can also be designed on [shader model 6](shader-model-6-0.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ca217-112">本節內容</span><span class="sxs-lookup"><span data-stu-id="ca217-112">In this section</span></span>

| <span data-ttu-id="ca217-113">主題</span><span class="sxs-lookup"><span data-stu-id="ca217-113">Topic</span></span> | <span data-ttu-id="ca217-114">描述</span><span class="sxs-lookup"><span data-stu-id="ca217-114">Description</span></span> |
|-|-|
| [<span data-ttu-id="ca217-115">使用著色器連結</span><span class="sxs-lookup"><span data-stu-id="ca217-115">Using shader linking</span></span>](using-shader-linking.md) | <span data-ttu-id="ca217-116">我們會示範如何建立先行編譯的 HLSL 函式、將它們封裝至程式庫，並在執行時間將它們連結到完整的著色器。</span><span class="sxs-lookup"><span data-stu-id="ca217-116">We show how to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run-time.</span></span> |
| [<span data-ttu-id="ca217-117">在 Direct3D 9 撰寫 HLSL 著色器</span><span class="sxs-lookup"><span data-stu-id="ca217-117">Writing HLSL Shaders in Direct3D 9</span></span>](dx-graphics-hlsl-writing-shaders-9.md) | |
| [<span data-ttu-id="ca217-118">在 Direct3D 9 中使用著色器</span><span class="sxs-lookup"><span data-stu-id="ca217-118">Using Shaders in Direct3D 9</span></span>](dx-graphics-hlsl-using-shaders-9.md) | |
| [<span data-ttu-id="ca217-119">使用 Direct3D 10 中的著色器</span><span class="sxs-lookup"><span data-stu-id="ca217-119">Using Shaders in Direct3D 10</span></span>](dx-graphics-hlsl-using-shaders-10.md) | |
| [<span data-ttu-id="ca217-120">優化 HLSL 著色器</span><span class="sxs-lookup"><span data-stu-id="ca217-120">Optimizing HLSL Shaders</span></span>](dx-graphics-hlsl-optimize.md) | |
| [<span data-ttu-id="ca217-121">Visual Studio 中的調試著色器</span><span class="sxs-lookup"><span data-stu-id="ca217-121">Debugging Shaders in Visual Studio</span></span>](dx-graphics-hlsl-debug-visual-studio.md) | <span data-ttu-id="ca217-122">偵錯工具的最新工具現在以 Microsoft Visual Studio 的功能形式隨附，稱為 Visual Studio 圖形偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="ca217-122">The latest tool for debugging shaders now ships as a feature in Microsoft Visual Studio, called Visual Studio Graphics Debugger.</span></span>  |
| [<span data-ttu-id="ca217-123">編譯著色器</span><span class="sxs-lookup"><span data-stu-id="ca217-123">Compiling Shaders</span></span>](dx-graphics-hlsl-part1.md) | <span data-ttu-id="ca217-124">現在讓我們看看如何編譯著色器程式碼的各種方式，以及著色器程式碼副檔名的慣例。</span><span class="sxs-lookup"><span data-stu-id="ca217-124">Let's now look at various ways to compile your shader code and conventions for file extensions for shader code.</span></span> |
| [<span data-ttu-id="ca217-125">指定編譯器目標</span><span class="sxs-lookup"><span data-stu-id="ca217-125">Specifying Compiler Targets</span></span>](specifying-compiler-targets.md) | <span data-ttu-id="ca217-126">在這裡，我們會列出 \**D3DCompile \** _ 函式和 HLSL 編譯器支援之各種設定檔的目標。</span><span class="sxs-lookup"><span data-stu-id="ca217-126">Here we list the targets for various profiles that the \**D3DCompile\** _ functions and the HLSL compiler support.</span></span> |
| [<span data-ttu-id="ca217-127">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="ca217-127">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md) | |
| [<span data-ttu-id="ca217-128">使用 HLSL 最小有效位數</span><span class="sxs-lookup"><span data-stu-id="ca217-128">Using HLSL minimum precision</span></span>](using-hlsl-minimum-precision.md) | <span data-ttu-id="ca217-129">從 Windows 8 開始，圖形驅動程式可以使用任何有效位數大於或等於指定的位精確度，來執行最小有效位數 HLSL 純量 [資料類型](dx-graphics-hlsl-scalar.md) 。</span><span class="sxs-lookup"><span data-stu-id="ca217-129">Starting with Windows 8, graphics drivers can implement minimum precision [HLSL scalar data types](dx-graphics-hlsl-scalar.md) by using any precision greater than or equal to their specified bit precision.</span></span>  |
| [<span data-ttu-id="ca217-130">HLSL 著色器模型5</span><span class="sxs-lookup"><span data-stu-id="ca217-130">HLSL Shader Model 5</span></span>](overviews-direct3d-11-hlsl.md) | |
| [<span data-ttu-id="ca217-131">HLSL 著色器模型5。1</span><span class="sxs-lookup"><span data-stu-id="ca217-131">HLSL Shader Model 5.1</span></span>](hlsl-shader-model-5-1-features-for-direct3d-12.md) | <span data-ttu-id="ca217-132">本節說明著色器模型5.1 的功能，在實務上適用于 D3D12 和 D3D 11.3。</span><span class="sxs-lookup"><span data-stu-id="ca217-132">This section describes the features of Shader Model 5.1 as they apply in practice to D3D12 and D3D11.3.</span></span> <span data-ttu-id="ca217-133">所有 DirectX 12 硬體都支援著色器模型5.1。</span><span class="sxs-lookup"><span data-stu-id="ca217-133">All DirectX 12 hardware supports Shader Model 5.1.</span></span> |
| [<span data-ttu-id="ca217-134">HLSL 著色器模型6。0</span><span class="sxs-lookup"><span data-stu-id="ca217-134">HLSL Shader Model 6.0</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md) | <span data-ttu-id="ca217-135">描述新增至 HLSL 著色器模型6.0 的 wave 作業內建。</span><span class="sxs-lookup"><span data-stu-id="ca217-135">Describes the wave operation intrinsics added to HLSL Shader Model 6.0.</span></span> |
| [<span data-ttu-id="ca217-136">HLSL 著色器模型6。4</span><span class="sxs-lookup"><span data-stu-id="ca217-136">HLSL Shader Model 6.4</span></span>](hlsl-shader-model-6-4-features-for-direct3d-12.md) | <span data-ttu-id="ca217-137">描述新增至 HLSL 著色器模型6.4 的機器學習內建函式。</span><span class="sxs-lookup"><span data-stu-id="ca217-137">Describes the machine learning intrinsics added to HLSL Shader Model 6.4.</span></span> |

## <a name="related-topics"></a><span data-ttu-id="ca217-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="ca217-138">Related topics</span></span>

<span data-ttu-id="ca217-139">_ [HLSL](dx-graphics-hlsl.md)</span><span class="sxs-lookup"><span data-stu-id="ca217-139">_ [HLSL](dx-graphics-hlsl.md)</span></span>
* [<span data-ttu-id="ca217-140">HLSL 的參考</span><span class="sxs-lookup"><span data-stu-id="ca217-140">Reference for HLSL</span></span>](dx-graphics-hlsl-reference.md)

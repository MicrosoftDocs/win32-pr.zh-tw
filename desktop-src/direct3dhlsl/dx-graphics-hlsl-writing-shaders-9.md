---
title: 在 Direct3D 9 撰寫 HLSL 著色器
description: 在 Direct3D 9 撰寫 HLSL 著色器
ms.assetid: 7db6b264-c96c-4298-9b8a-d0c488390e4e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 64a64d08518cb987850c87da3fb19c264519a7f7
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335382"
---
# <a name="writing-hlsl-shaders-in-direct3d-9"></a><span data-ttu-id="d2052-103">在 Direct3D 9 撰寫 HLSL 著色器</span><span class="sxs-lookup"><span data-stu-id="d2052-103">Writing HLSL Shaders in Direct3D 9</span></span>

-   [<span data-ttu-id="d2052-104">頂點-著色器基本概念</span><span class="sxs-lookup"><span data-stu-id="d2052-104">Vertex-Shader Basics</span></span>](#vertex-shader-basics)
-   [<span data-ttu-id="d2052-105">圖元著色器基本概念</span><span class="sxs-lookup"><span data-stu-id="d2052-105">Pixel-Shader Basics</span></span>](#pixel-shader-basics)
    -   [<span data-ttu-id="d2052-106">材質階段和取樣器狀態</span><span class="sxs-lookup"><span data-stu-id="d2052-106">Texture Stage and Sampler States</span></span>](#texture-stage-and-sampler-states)
    -   [<span data-ttu-id="d2052-107">圖元著色器輸入</span><span class="sxs-lookup"><span data-stu-id="d2052-107">Pixel Shader Inputs</span></span>](#pixel-shader-inputs)
    -   [<span data-ttu-id="d2052-108">圖元著色器輸出</span><span class="sxs-lookup"><span data-stu-id="d2052-108">Pixel Shader Outputs</span></span>](#pixel-shader-outputs)
-   [<span data-ttu-id="d2052-109">著色器輸入和著色器變數</span><span class="sxs-lookup"><span data-stu-id="d2052-109">Shader Inputs and Shader Variables</span></span>](#shader-inputs-and-shader-variables)
    -   [<span data-ttu-id="d2052-110">宣告著色器變數</span><span class="sxs-lookup"><span data-stu-id="d2052-110">Declaring Shader Variables</span></span>](#declaring-shader-variables)
    -   [<span data-ttu-id="d2052-111">統一著色器輸入</span><span class="sxs-lookup"><span data-stu-id="d2052-111">Uniform Shader Inputs</span></span>](#uniform-shader-inputs)
    -   [<span data-ttu-id="d2052-112">不同的著色器輸入和語義</span><span class="sxs-lookup"><span data-stu-id="d2052-112">Varying Shader Inputs and Semantics</span></span>](#varying-shader-inputs-and-semantics)
    -   [<span data-ttu-id="d2052-113">取樣器和材質物件</span><span class="sxs-lookup"><span data-stu-id="d2052-113">Samplers and Texture Objects</span></span>](#samplers-and-texture-objects)
-   [<span data-ttu-id="d2052-114">撰寫函數</span><span class="sxs-lookup"><span data-stu-id="d2052-114">Writing Functions</span></span>](#writing-functions)
-   [<span data-ttu-id="d2052-115">流程式控制制</span><span class="sxs-lookup"><span data-stu-id="d2052-115">Flow Control</span></span>](#flow-control)
-   [<span data-ttu-id="d2052-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="d2052-116">Related topics</span></span>](#related-topics)

## <a name="vertex-shader-basics"></a><span data-ttu-id="d2052-117">Vertex-Shader 基本概念</span><span class="sxs-lookup"><span data-stu-id="d2052-117">Vertex-Shader Basics</span></span>

<span data-ttu-id="d2052-118">在作業中，可程式化的頂點著色器會取代 Microsoft Direct3D 圖形管線所完成的頂點處理。</span><span class="sxs-lookup"><span data-stu-id="d2052-118">When in operation, a programmable vertex shader replaces the vertex processing done by the Microsoft Direct3D graphics pipeline.</span></span> <span data-ttu-id="d2052-119">使用頂點著色器時，固定函式管線會忽略關於轉換和光源作業的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="d2052-119">While using a vertex shader, state information regarding transformation and lighting operations is ignored by the fixed function pipeline.</span></span> <span data-ttu-id="d2052-120">當頂點著色器已停用，且傳回固定的函式處理時，會套用所有目前的狀態設定。</span><span class="sxs-lookup"><span data-stu-id="d2052-120">When the vertex shader is disabled and fixed function processing is returned, all current state settings apply.</span></span>

<span data-ttu-id="d2052-121">在頂點著色器執行之前，必須先完成高序位基本專案的鑲嵌。</span><span class="sxs-lookup"><span data-stu-id="d2052-121">Tessellation of high-order primitives should be done before the vertex shader executes.</span></span> <span data-ttu-id="d2052-122">著色器處理之後執行表面鑲嵌的執行必須以對應用程式和著色器程式碼不明顯的方式來執行。</span><span class="sxs-lookup"><span data-stu-id="d2052-122">Implementations that perform surface tessellation after the shader processing must do so in a way that is not apparent to the application and shader code.</span></span>

<span data-ttu-id="d2052-123">頂點著色器最少必須在同質剪輯空間中輸出頂點位置。</span><span class="sxs-lookup"><span data-stu-id="d2052-123">As a minimum, a vertex shader must output vertex position in homogeneous clip space.</span></span> <span data-ttu-id="d2052-124">（選擇性）頂點著色器可以輸出材質座標、頂點色彩、頂點光源、霧化因數等等。</span><span class="sxs-lookup"><span data-stu-id="d2052-124">Optionally, the vertex shader can output texture coordinates, vertex color, vertex lighting, fog factors, and so on.</span></span>

## <a name="pixel-shader-basics"></a><span data-ttu-id="d2052-125">Pixel-Shader 基本概念</span><span class="sxs-lookup"><span data-stu-id="d2052-125">Pixel-Shader Basics</span></span>

<span data-ttu-id="d2052-126">圖元處理是由個別圖元上的圖元著色器所執行。</span><span class="sxs-lookup"><span data-stu-id="d2052-126">Pixel processing is performed by pixel shaders on individual pixels.</span></span> <span data-ttu-id="d2052-127">圖元著色器與頂點著色器搭配運作;頂點著色器的輸出會提供圖元著色器的輸入。</span><span class="sxs-lookup"><span data-stu-id="d2052-127">Pixel shaders work in concert with vertex shaders; the output of a vertex shader provides the inputs for a pixel shader.</span></span> <span data-ttu-id="d2052-128">其他圖元運算 (霧化混色、樣板作業和轉譯目標混色) 在著色器執行之後發生。</span><span class="sxs-lookup"><span data-stu-id="d2052-128">Other pixel operations (fog blending, stencil operations, and render-target blending) occur after execution of the shader.</span></span>

### <a name="texture-stage-and-sampler-states"></a><span data-ttu-id="d2052-129">材質階段和取樣器狀態</span><span class="sxs-lookup"><span data-stu-id="d2052-129">Texture Stage and Sampler States</span></span>

<span data-ttu-id="d2052-130">圖元著色器會完全取代多紋理 blender 所指定的圖元混合功能，包括材質階段狀態之前所定義的作業。</span><span class="sxs-lookup"><span data-stu-id="d2052-130">A pixel shader completely replaces the pixel-blending functionality specified by the multi-texture blender including operations previously defined by the texture stage states.</span></span> <span data-ttu-id="d2052-131">針對縮制、縮放比例、mip 篩選和 wrap 定址模式所控制的材質取樣和篩選作業，可以在著色器中初始化。</span><span class="sxs-lookup"><span data-stu-id="d2052-131">Texture sampling and filtering operations which were controlled by the standard texture stage states for minification, magnification, mip filtering, and the wrap addressing modes, can be initialized in shaders.</span></span> <span data-ttu-id="d2052-132">應用程式可自由變更這些狀態，而不需要重新產生目前系結的著色器。</span><span class="sxs-lookup"><span data-stu-id="d2052-132">The application is free to change these states without requiring the regeneration of the currently bound shader.</span></span> <span data-ttu-id="d2052-133">如果您的著色器是在效果內設計，則設定狀態可以更容易進行。</span><span class="sxs-lookup"><span data-stu-id="d2052-133">Setting state can be made even easier if your shaders are designed within an effect.</span></span>

### <a name="pixel-shader-inputs"></a><span data-ttu-id="d2052-134">圖元著色器輸入</span><span class="sxs-lookup"><span data-stu-id="d2052-134">Pixel Shader Inputs</span></span>

<span data-ttu-id="d2052-135">針對圖元著色器版本 ps \_ 1 \_ 1-ps \_ 2 \_ 0，擴散和反射色彩是在著色器使用之前的範圍 (壓制) 的飽和。</span><span class="sxs-lookup"><span data-stu-id="d2052-135">For pixel shader versions ps\_1\_1 - ps\_2\_0, diffuse and specular colors are saturated (clamped) in the range 0 to 1 before use by the shader.</span></span>

<span data-ttu-id="d2052-136">系統會假設圖元著色器的色彩值輸入是正確的，但並非所有硬體) 都能 (。</span><span class="sxs-lookup"><span data-stu-id="d2052-136">Color values input to the pixel shader are assumed to be perspective correct, but this is not guaranteed (for all hardware).</span></span> <span data-ttu-id="d2052-137">從紋理座標取樣的色彩會以正確的角度進行反覆運算，並在反復專案期間壓制至0到1的範圍。</span><span class="sxs-lookup"><span data-stu-id="d2052-137">Colors sampled from texture coordinates are iterated in a perspective correct manner, and are clamped to the 0 to 1 range during iteration.</span></span>

### <a name="pixel-shader-outputs"></a><span data-ttu-id="d2052-138">圖元著色器輸出</span><span class="sxs-lookup"><span data-stu-id="d2052-138">Pixel Shader Outputs</span></span>

<span data-ttu-id="d2052-139">針對圖元著色器版本 ps \_ 1 \_ 1-ps \_ 1 \_ 4，圖元著色器發出的結果是 register r0 的內容。</span><span class="sxs-lookup"><span data-stu-id="d2052-139">For pixel shader versions ps\_1\_1 - ps\_1\_4, the result emitted by the pixel shader is the contents of register r0.</span></span> <span data-ttu-id="d2052-140">著色器完成處理時所包含的任何內容都會傳送至霧化階段和轉譯目標 blender。</span><span class="sxs-lookup"><span data-stu-id="d2052-140">Whatever it contains when the shader completes processing is sent to the fog stage and render-target blender.</span></span>

<span data-ttu-id="d2052-141">若是圖元著色器版本 ps \_ 2 \_ 0 和更新版本，則會從 OC0-oC4 發出輸出色彩。</span><span class="sxs-lookup"><span data-stu-id="d2052-141">For pixel shader versions ps\_2\_0 and above, output color is emitted from oC0 - oC4.</span></span>

## <a name="shader-inputs-and-shader-variables"></a><span data-ttu-id="d2052-142">著色器輸入和著色器變數</span><span class="sxs-lookup"><span data-stu-id="d2052-142">Shader Inputs and Shader Variables</span></span>

-   [<span data-ttu-id="d2052-143">宣告著色器變數</span><span class="sxs-lookup"><span data-stu-id="d2052-143">Declaring Shader Variables</span></span>](#declaring-shader-variables)
-   [<span data-ttu-id="d2052-144">統一著色器輸入</span><span class="sxs-lookup"><span data-stu-id="d2052-144">Uniform Shader Inputs</span></span>](#uniform-shader-inputs)
-   [<span data-ttu-id="d2052-145">不同的著色器輸入和語義</span><span class="sxs-lookup"><span data-stu-id="d2052-145">Varying Shader Inputs and Semantics</span></span>](#varying-shader-inputs-and-semantics)
-   [<span data-ttu-id="d2052-146">取樣器和材質物件</span><span class="sxs-lookup"><span data-stu-id="d2052-146">Samplers and Texture Objects</span></span>](#samplers-and-texture-objects)

### <a name="declaring-shader-variables"></a><span data-ttu-id="d2052-147">宣告著色器變數</span><span class="sxs-lookup"><span data-stu-id="d2052-147">Declaring Shader Variables</span></span>

<span data-ttu-id="d2052-148">最簡單的變數宣告包括型別和變數名稱，例如：</span><span class="sxs-lookup"><span data-stu-id="d2052-148">The simplest variable declaration includes a type and a variable name, such as this floating-point declaration:</span></span>


```
float fVar;
```



<span data-ttu-id="d2052-149">您可以在相同的語句中初始化變數。</span><span class="sxs-lookup"><span data-stu-id="d2052-149">You can initialize a variable in the same statement.</span></span>


```
float fVar = 3.1f;
```



<span data-ttu-id="d2052-150">可以宣告變數陣列，</span><span class="sxs-lookup"><span data-stu-id="d2052-150">An array of variables can be declared,</span></span>


```
int iVar[3];
```



<span data-ttu-id="d2052-151">或在相同的語句中宣告和初始化。</span><span class="sxs-lookup"><span data-stu-id="d2052-151">or declared and initialized in the same statement.</span></span>


```
int iVar[3] = {1,2,3};
```



<span data-ttu-id="d2052-152">以下是一些宣告，示範高階著色器語言 (HLSL) 變數的許多特性：</span><span class="sxs-lookup"><span data-stu-id="d2052-152">Here are a few declarations that demonstrate many of the characteristics of high-level shader language (HLSL) variables:</span></span>


```
float4 color;
uniform float4 position : POSITION; 
const float4 lightDirection = {0,0,1};
```



<span data-ttu-id="d2052-153">資料宣告可以使用任何有效的類型，包括：</span><span class="sxs-lookup"><span data-stu-id="d2052-153">Data declarations can use any valid type including:</span></span>

-   [<span data-ttu-id="d2052-154"> (DirectX HLSL) 的資料類型 </span><span class="sxs-lookup"><span data-stu-id="d2052-154">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
-   [<span data-ttu-id="d2052-155"> (DirectX HLSL) 的向量類型 </span><span class="sxs-lookup"><span data-stu-id="d2052-155">Vector Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-vector.md)
-   [<span data-ttu-id="d2052-156"> (DirectX HLSL) 的矩陣類型 </span><span class="sxs-lookup"><span data-stu-id="d2052-156">Matrix Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-matrix.md)
-   [<span data-ttu-id="d2052-157"> (DirectX HLSL) 的著色器類型 </span><span class="sxs-lookup"><span data-stu-id="d2052-157">Shader Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-shader.md)
-   [<span data-ttu-id="d2052-158"> (DirectX HLSL) 的取樣器類型 </span><span class="sxs-lookup"><span data-stu-id="d2052-158">Sampler Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-sampler.md)
-   [<span data-ttu-id="d2052-159"> (DirectX HLSL) 的使用者自訂類型 </span><span class="sxs-lookup"><span data-stu-id="d2052-159">User-Defined Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-user-defined.md)

<span data-ttu-id="d2052-160">著色器可以具有最上層變數、引數和函數。</span><span class="sxs-lookup"><span data-stu-id="d2052-160">A shader can have top-level variables, arguments, and functions.</span></span>


```
// top-level variable
float globalShaderVariable; 

// top-level function
void function(
in float4 position: POSITION0 // top-level argument
              )
{
  float localShaderVariable; // local variable
  function2(...)
}

void function2()
{
  ...
}
```



<span data-ttu-id="d2052-161">最上層變數是在所有函式之外宣告的。</span><span class="sxs-lookup"><span data-stu-id="d2052-161">Top-level variables are declared outside of all functions.</span></span> <span data-ttu-id="d2052-162">最上層引數是最上層函數的參數。</span><span class="sxs-lookup"><span data-stu-id="d2052-162">Top-level arguments are parameters to a top-level function.</span></span> <span data-ttu-id="d2052-163">最上層函式是由應用程式所呼叫的任何函式 (，而不是由另一個函式) 所呼叫的函式所呼叫的函數。</span><span class="sxs-lookup"><span data-stu-id="d2052-163">A top-level function is any function called by the application (as opposed to a function that is called by another function).</span></span>

### <a name="uniform-shader-inputs"></a><span data-ttu-id="d2052-164">統一著色器輸入</span><span class="sxs-lookup"><span data-stu-id="d2052-164">Uniform Shader Inputs</span></span>

<span data-ttu-id="d2052-165">頂點和圖元著色器接受兩種類型的輸入資料：差異和統一。</span><span class="sxs-lookup"><span data-stu-id="d2052-165">Vertex and pixel shaders accept two kinds of input data: varying and uniform.</span></span> <span data-ttu-id="d2052-166">不同的輸入是每次執行著色器的唯一資料。</span><span class="sxs-lookup"><span data-stu-id="d2052-166">The varying input is the data that is unique to each execution of the shader.</span></span> <span data-ttu-id="d2052-167">針對頂點著色器，不同的資料 (例如：位置、正常等 ) 來自于頂點資料流程。</span><span class="sxs-lookup"><span data-stu-id="d2052-167">For a vertex shader, the varying data (for example: position, normal, etc.) comes from the vertex streams.</span></span> <span data-ttu-id="d2052-168">統一資料 (例如：材質色彩、世界轉換等 ) 對於著色器的多個執行都是常數。</span><span class="sxs-lookup"><span data-stu-id="d2052-168">The uniform data (for example: material color, world transform, etc.) is constant for multiple executions of a shader.</span></span> <span data-ttu-id="d2052-169">針對熟悉的元件著色器模型的人，會由常數暫存器和由 v 和 t 註冊的不同資料來指定統一的資料。</span><span class="sxs-lookup"><span data-stu-id="d2052-169">For those familiar with the assembly shader models, uniform data is specified by constant registers and varying data by the v and t registers.</span></span>

<span data-ttu-id="d2052-170">您可以透過兩種方法來指定統一的資料。</span><span class="sxs-lookup"><span data-stu-id="d2052-170">Uniform data can be specified by two methods.</span></span> <span data-ttu-id="d2052-171">最常見的方法是宣告全域變數，並在著色器中使用它們。</span><span class="sxs-lookup"><span data-stu-id="d2052-171">The most common method is to declare global variables and use them within a shader.</span></span> <span data-ttu-id="d2052-172">在著色器中使用全域變數，會導致將該變數加入至該著色器所需的統一變數清單。</span><span class="sxs-lookup"><span data-stu-id="d2052-172">Any use of global variables within a shader will result in adding that variable to the list of uniform variables required by that shader.</span></span> <span data-ttu-id="d2052-173">第二種方法是將最上層著色器函式的輸入參數標示為統一。</span><span class="sxs-lookup"><span data-stu-id="d2052-173">The second method is to mark an input parameter of the top-level shader function as uniform.</span></span> <span data-ttu-id="d2052-174">這項標示會指定應該將指定的變數加入至統一變數清單。</span><span class="sxs-lookup"><span data-stu-id="d2052-174">This marking specifies that the given variable should be added to the list of uniform variables.</span></span>

<span data-ttu-id="d2052-175">著色器所使用的統一變數會透過常數資料表傳回給應用程式。</span><span class="sxs-lookup"><span data-stu-id="d2052-175">Uniform variables used by a shader are communicated back to the application via the constant table.</span></span> <span data-ttu-id="d2052-176">常數資料表是符號表的名稱，定義著色器所使用的統一變數如何融入常數暫存器中。</span><span class="sxs-lookup"><span data-stu-id="d2052-176">The constant table is the name for the symbol table that defines how the uniform variables used by a shader fit into the constant registers.</span></span> <span data-ttu-id="d2052-177">統一函式參數會出現在常數資料表中，且前面加上貨幣符號 ($) ，與全域變數不同。</span><span class="sxs-lookup"><span data-stu-id="d2052-177">The uniform function parameters appear in the constant table prepended with a dollar sign ($), unlike the global variables.</span></span> <span data-ttu-id="d2052-178">需要貨幣符號，以避免本機統一輸入與相同名稱的全域變數之間發生名稱衝突。</span><span class="sxs-lookup"><span data-stu-id="d2052-178">The dollar sign is required to avoid name collisions between local uniform inputs and global variables of the same name.</span></span>

<span data-ttu-id="d2052-179">常數資料表包含著色器所使用之所有統一變數的常數註冊位置。</span><span class="sxs-lookup"><span data-stu-id="d2052-179">The constant table contains the constant register locations of all uniform variables used by the shader.</span></span> <span data-ttu-id="d2052-180">資料表也包含型別資訊和預設值（如果有指定的話）。</span><span class="sxs-lookup"><span data-stu-id="d2052-180">The table also includes the type information and the default value, if specified.</span></span>

### <a name="varying-shader-inputs-and-semantics"></a><span data-ttu-id="d2052-181">不同的著色器輸入和語義</span><span class="sxs-lookup"><span data-stu-id="d2052-181">Varying Shader Inputs and Semantics</span></span>

<span data-ttu-id="d2052-182">最上層著色器函式 (的不同輸入參數) 必須以語義或統一關鍵字標示，表示執行著色器的值是常數。</span><span class="sxs-lookup"><span data-stu-id="d2052-182">Varying input parameters (of a top-level shader function) must be marked either with a semantic or uniform keyword indicating the value is constant for the execution of the shader.</span></span> <span data-ttu-id="d2052-183">如果最上層著色器輸入未以語義或統一關鍵字標示，則著色器將無法編譯。</span><span class="sxs-lookup"><span data-stu-id="d2052-183">If a top-level shader input is not marked with a semantic or uniform keyword, then the shader will fail to compile.</span></span>

<span data-ttu-id="d2052-184">輸入語義是用來將指定的輸入連結至圖形管線上一個部分之輸出的名稱。</span><span class="sxs-lookup"><span data-stu-id="d2052-184">The input semantic is a name used to link the given input to an output of the previous part of the graphics pipeline.</span></span> <span data-ttu-id="d2052-185">例如，頂點著色器會使用輸入語義 POSITION0 來指定應從頂點緩衝區連結位置資料的位置。</span><span class="sxs-lookup"><span data-stu-id="d2052-185">For example, the input semantic POSITION0 is used by the vertex shaders to specify where the position data from the vertex buffer should be linked.</span></span>

<span data-ttu-id="d2052-186">圖元和頂點著色器有不同的輸入語義集合，因為圖形管線的不同部分會送入每個著色器單位。</span><span class="sxs-lookup"><span data-stu-id="d2052-186">Pixel and vertex shaders have different sets of input semantics due to the different parts of the graphics pipeline that feed into each shader unit.</span></span> <span data-ttu-id="d2052-187">頂點著色器輸入語義描述每個頂點的資訊 (例如：位置、標準、材質座標、色彩、正切、binormal 等 ) 要從頂點緩衝區載入至可供頂點著色器使用的表單。</span><span class="sxs-lookup"><span data-stu-id="d2052-187">Vertex shader input semantics describe the per-vertex information (for example: position, normal, texture coordinates, color, tangent, binormal, etc.) to be loaded from a vertex buffer into a form that can be consumed by the vertex shader.</span></span> <span data-ttu-id="d2052-188">輸入語義會直接對應到頂點宣告的使用方式和使用方式索引。</span><span class="sxs-lookup"><span data-stu-id="d2052-188">The input semantics directly map to the vertex declaration usage and the usage index.</span></span>

<span data-ttu-id="d2052-189">圖元著色器輸入語義會描述由點陣化單位提供的每個圖元所提供的資訊。</span><span class="sxs-lookup"><span data-stu-id="d2052-189">Pixel shader input semantics describe the information that is provided per pixel by the rasterization unit.</span></span> <span data-ttu-id="d2052-190">資料是藉由在目前基本物件的每個頂點的頂點著色器輸出之間插上插上而產生。</span><span class="sxs-lookup"><span data-stu-id="d2052-190">The data is generated by interpolating between outputs of the vertex shader for each vertex of the current primitive.</span></span> <span data-ttu-id="d2052-191">基本圖元著色器輸入語義會將輸出色彩和材質座標資訊連結至輸入參數。</span><span class="sxs-lookup"><span data-stu-id="d2052-191">The basic pixel shader input semantics link the output color and texture coordinate information to input parameters.</span></span>

<span data-ttu-id="d2052-192">您可以透過兩種方法將輸入語義指派給著色器輸入：</span><span class="sxs-lookup"><span data-stu-id="d2052-192">Input semantics can be assigned to shader input by two methods:</span></span>

-   <span data-ttu-id="d2052-193">將冒號和語義名稱附加至參數宣告。</span><span class="sxs-lookup"><span data-stu-id="d2052-193">Appending a colon and the semantic name to the parameter declaration.</span></span>
-   <span data-ttu-id="d2052-194">使用指派給每個結構成員的輸入語義來定義輸入結構。</span><span class="sxs-lookup"><span data-stu-id="d2052-194">Defining an input structure with input semantics assigned to each structure member.</span></span>

<span data-ttu-id="d2052-195">頂點和圖元著色器會將輸出資料提供給後續的圖形管線階段。</span><span class="sxs-lookup"><span data-stu-id="d2052-195">Vertex and pixel shaders provide output data to the subsequent graphics pipeline stage.</span></span> <span data-ttu-id="d2052-196">輸出語義可用來指定著色器產生的資料應該如何連結至下一個階段的輸入。</span><span class="sxs-lookup"><span data-stu-id="d2052-196">Output semantics are used to specify how data generated by the shader should be linked to the inputs of the next stage.</span></span> <span data-ttu-id="d2052-197">例如，頂點著色器的輸出語義會用來連結轉譯器中 interpolators 的輸出，以產生圖元著色器的輸入資料。</span><span class="sxs-lookup"><span data-stu-id="d2052-197">For example, the output semantics for a vertex shader are used to link the outputs of the interpolators in the rasterizer to generate the input data for the pixel shader.</span></span> <span data-ttu-id="d2052-198">圖元著色器輸出是針對每個轉譯目標提供給 Alpha 混色單位的值，或寫入深度緩衝區的深度值。</span><span class="sxs-lookup"><span data-stu-id="d2052-198">The pixel shader outputs are the values provided to the alpha blending unit for each of the render targets or the depth value written to the depth buffer.</span></span>

<span data-ttu-id="d2052-199">頂點著色器輸出語義是用來將著色器連結到圖元著色器和轉譯器階段。</span><span class="sxs-lookup"><span data-stu-id="d2052-199">Vertex shader output semantics are used to link the shader both to the pixel shader and to the rasterizer stage.</span></span> <span data-ttu-id="d2052-200">由轉譯器取用但未公開給圖元著色器的頂點著色器，必須以最小值產生位置資料。</span><span class="sxs-lookup"><span data-stu-id="d2052-200">A vertex shader that is consumed by the rasterizer and not exposed to the pixel shader must generate position data as a minimum.</span></span> <span data-ttu-id="d2052-201">產生材質座標和色彩資料的頂點著色器會在插補完成之後，將該資料提供給圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="d2052-201">Vertex shaders that generate texture coordinate and color data provide that data to a pixel shader after interpolation is done.</span></span>

<span data-ttu-id="d2052-202">圖元著色器輸出語義會以正確的轉譯目標來系結圖元著色器的輸出色彩。</span><span class="sxs-lookup"><span data-stu-id="d2052-202">Pixel shader output semantics bind the output colors of a pixel shader with the correct render target.</span></span> <span data-ttu-id="d2052-203">圖元著色器輸出色彩會連結到 Alpha blend 階段，以決定如何修改目的地呈現目標。</span><span class="sxs-lookup"><span data-stu-id="d2052-203">The pixel shader output color is linked to the alpha blend stage, which determines how the destination render targets are modified.</span></span> <span data-ttu-id="d2052-204">圖元著色器深度輸出可以用來變更目前點陣位置的目的地深度值。</span><span class="sxs-lookup"><span data-stu-id="d2052-204">The pixel shader depth output can be used to change the destination depth values at the current raster location.</span></span> <span data-ttu-id="d2052-205">只有某些著色器模型支援深度輸出和多個呈現目標。</span><span class="sxs-lookup"><span data-stu-id="d2052-205">The depth output and multiple render targets are only supported with some shader models.</span></span>

<span data-ttu-id="d2052-206">輸出語義的語法與指定輸入語義的語法相同。</span><span class="sxs-lookup"><span data-stu-id="d2052-206">The syntax for output semantics is identical to the syntax for specifying input semantics.</span></span> <span data-ttu-id="d2052-207">您可以直接在宣告為 "out" 參數或在結構定義期間（以 "out" 參數或函式的傳回值形式傳回）的參數上指定語義。</span><span class="sxs-lookup"><span data-stu-id="d2052-207">The semantics can be either specified directly on parameters declared as "out" parameters or assigned during the definition of a structure that either returned as an "out" parameter or the return value of a function.</span></span>

<span data-ttu-id="d2052-208">語法可識別資料的來源。</span><span class="sxs-lookup"><span data-stu-id="d2052-208">Semantics identify where data comes from.</span></span> <span data-ttu-id="d2052-209">語義是識別著色器輸入和輸出的選擇性識別碼。</span><span class="sxs-lookup"><span data-stu-id="d2052-209">Semantics are optional identifiers that identify shader inputs and outputs.</span></span> <span data-ttu-id="d2052-210">語義會出現在下列三個位置之一：</span><span class="sxs-lookup"><span data-stu-id="d2052-210">Semantics appear in one of three places:</span></span>

-   <span data-ttu-id="d2052-211">結構成員之後。</span><span class="sxs-lookup"><span data-stu-id="d2052-211">After a structure member.</span></span>
-   <span data-ttu-id="d2052-212">在函數的輸入引數清單中的引數之後。</span><span class="sxs-lookup"><span data-stu-id="d2052-212">After an argument in a function's input argument list.</span></span>
-   <span data-ttu-id="d2052-213">在函數的輸入引數清單之後。</span><span class="sxs-lookup"><span data-stu-id="d2052-213">After the function's input argument list.</span></span>

<span data-ttu-id="d2052-214">此範例會使用結構來提供一或多個頂點著色器輸入，並使用另一個結構來提供一或多個頂點著色器輸出。</span><span class="sxs-lookup"><span data-stu-id="d2052-214">This example uses a structure to provide one or more vertex shader inputs, and another structure to provide one or more vertex shader outputs.</span></span> <span data-ttu-id="d2052-215">每個結構成員都使用語義。</span><span class="sxs-lookup"><span data-stu-id="d2052-215">Each of the structure members uses a semantic.</span></span>


```
vector vClr;

struct VS_INPUT
{
    float4 vPosition : POSITION;
    float3 vNormal : NORMAL;
    float4 vBlendWeights : BLENDWEIGHT;
};

struct VS_OUTPUT
{
    float4  vPosition : POSITION;
    float4  vDiffuse : COLOR;

};

float4x4 mWld1;
float4x4 mWld2;
float4x4 mWld3;
float4x4 mWld4;

float Len;
float4 vLight;

float4x4 mTot;

VS_OUTPUT VS_Skinning_Example(const VS_INPUT v, uniform float len=100)
{
    VS_OUTPUT out;

    // Skin position (to world space)
    float3 vPosition = 
        mul(v.vPosition, (float4x3) mWld1) * v.vBlendWeights.x +
        mul(v.vPosition, (float4x3) mWld2) * v.vBlendWeights.y +
        mul(v.vPosition, (float4x3) mWld3) * v.vBlendWeights.z +
        mul(v.vPosition, (float4x3) mWld4) * v.vBlendWeights.w;
    // Skin normal (to world space)
    float3 vNormal =
        mul(v.vNormal, (float3x3) mWld1) * v.vBlendWeights.x + 
        mul(v.vNormal, (float3x3) mWld2) * v.vBlendWeights.y + 
        mul(v.vNormal, (float3x3) mWld3) * v.vBlendWeights.z + 
        mul(v.vNormal, (float3x3) mWld4) * v.vBlendWeights.w;
    
    // Output stuff
    out.vPosition    = mul(float4(vPosition + vNormal * Len, 1), mTot);
    out.vDiffuse  = dot(vLight,vNormal);

    return out;
}
```



<span data-ttu-id="d2052-216">輸入結構會識別可提供著色器輸入之頂點緩衝區中的資料。</span><span class="sxs-lookup"><span data-stu-id="d2052-216">The input structure identifies the data from the vertex buffer that will provide the shader inputs.</span></span> <span data-ttu-id="d2052-217">這個著色器會將資料從頂點緩衝區的位置、標準和 blendweight 元素對應到頂點著色器暫存器。</span><span class="sxs-lookup"><span data-stu-id="d2052-217">This shader maps the data from the position, normal, and blendweight elements of the vertex buffer into vertex shader registers.</span></span> <span data-ttu-id="d2052-218">輸入資料類型不需要完全符合頂點宣告資料類型。</span><span class="sxs-lookup"><span data-stu-id="d2052-218">The input data type does not have to exactly match the vertex declaration data type.</span></span> <span data-ttu-id="d2052-219">如果它不完全相符，頂點資料會在寫入著色器暫存器時自動轉換成 HLSL 的資料類型。</span><span class="sxs-lookup"><span data-stu-id="d2052-219">If it doesn't exactly match, the vertex data will automatically be converted into the HLSL's data type when it is written into the shader registers.</span></span> <span data-ttu-id="d2052-220">比方說，如果一般資料定義為應用程式的 UINT 型別，則會在著色器讀取時將它轉換成 float3。</span><span class="sxs-lookup"><span data-stu-id="d2052-220">For instance, if the normal data were defined to be of type UINT by the application, it would be converted into a float3 when read by the shader.</span></span>

<span data-ttu-id="d2052-221">如果頂點資料流程中的資料包含的元件比對應的著色器資料類型少，遺漏的元件將會初始化為 0 (但 w 除外，後者會初始化為 1) 。</span><span class="sxs-lookup"><span data-stu-id="d2052-221">If the data in the vertex stream contains fewer components than the corresponding shader data type, the missing components will be initialized to 0 (except for w, which is initialized to 1).</span></span>

<span data-ttu-id="d2052-222">輸入語義類似于 [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage)中的值。</span><span class="sxs-lookup"><span data-stu-id="d2052-222">Input semantics are similar to the values in the [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage).</span></span>

<span data-ttu-id="d2052-223">輸出結構會識別位置和色彩的頂點著色器輸出參數。</span><span class="sxs-lookup"><span data-stu-id="d2052-223">The output structure identifies the vertex shader output parameters of position and color.</span></span> <span data-ttu-id="d2052-224">管線會使用這些輸出 (基本處理) 中的三角形柵格化。</span><span class="sxs-lookup"><span data-stu-id="d2052-224">These outputs will be used by the pipeline for triangle rasterization (in primitive processing).</span></span> <span data-ttu-id="d2052-225">標示為位置資料的輸出會代表頂點在同質空間中的位置。</span><span class="sxs-lookup"><span data-stu-id="d2052-225">The output marked as position data denotes the position of a vertex in homogeneous space.</span></span> <span data-ttu-id="d2052-226">頂點著色器至少必須產生位置資料。</span><span class="sxs-lookup"><span data-stu-id="d2052-226">As a minimum, a vertex shader must generate position data.</span></span> <span data-ttu-id="d2052-227">藉由將 (x，y，z) 座標除以 w，在頂點著色器完成後，會計算螢幕空間位置。</span><span class="sxs-lookup"><span data-stu-id="d2052-227">The screen space position is computed after the vertex shader completes by dividing the (x, y, z) coordinate by w.</span></span> <span data-ttu-id="d2052-228">在螢幕空間中，-1 和1是區界界限的最小和最大 x 和 y 值，而 z 則用於 z 緩衝區測試。</span><span class="sxs-lookup"><span data-stu-id="d2052-228">In screen space, -1 and 1 are the minimum and maximum x and y values of the boundaries of the viewport, while z is used for z-buffer testing.</span></span>

<span data-ttu-id="d2052-229">輸出語義也類似于 [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage)中的值。</span><span class="sxs-lookup"><span data-stu-id="d2052-229">Output semantics are also similar to the values in [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage).</span></span> <span data-ttu-id="d2052-230">一般而言，頂點著色器的輸出結構也可以當做圖元著色器的輸入結構使用，但前提是圖元著色器不會讀取任何標記有位置、點大小或霧化語義的變數。</span><span class="sxs-lookup"><span data-stu-id="d2052-230">In general, an output structure for a vertex shader can also be used as the input structure for a pixel shader, provided the pixel shader does not read from any variable marked with the position, point size, or fog semantics.</span></span> <span data-ttu-id="d2052-231">這些語義與圖元著色器未使用的每個頂點純量值相關聯。</span><span class="sxs-lookup"><span data-stu-id="d2052-231">These semantics are associated with per-vertex scalar values that are not used by a pixel shader.</span></span> <span data-ttu-id="d2052-232">如果圖元著色器需要這些值，則可以將它們複製到另一個使用圖元著色器語義的輸出變數。</span><span class="sxs-lookup"><span data-stu-id="d2052-232">If these values are needed for the pixel shader, they can be copied into another output variable that uses a pixel shader semantic.</span></span>

<span data-ttu-id="d2052-233">全域變數會由編譯器自動指派給註冊。</span><span class="sxs-lookup"><span data-stu-id="d2052-233">Global variables are assigned to registers automatically by the compiler.</span></span> <span data-ttu-id="d2052-234">全域變數也稱為統一參數，因為每次呼叫著色器時所處理的所有圖元的變數內容都相同。</span><span class="sxs-lookup"><span data-stu-id="d2052-234">Global variables are also called uniform parameters because the contents of the variable is the same for all pixels processed each time the shader is called.</span></span> <span data-ttu-id="d2052-235">暫存器包含在常數資料表中，您可以使用 [**ID3DXConstantTable**](/windows/desktop/direct3d9/id3dxconstanttable) 介面來讀取這些暫存器。</span><span class="sxs-lookup"><span data-stu-id="d2052-235">The registers are contained in the constant table, which can be read using the [**ID3DXConstantTable**](/windows/desktop/direct3d9/id3dxconstanttable) interface.</span></span>

<span data-ttu-id="d2052-236">圖元著色器的輸入語義可將值對應至端點著色器和圖元著色器之間傳輸的特定硬體暫存器。</span><span class="sxs-lookup"><span data-stu-id="d2052-236">Input semantics for pixel shaders map values into specific hardware registers for transport between vertex shaders and pixel shaders.</span></span> <span data-ttu-id="d2052-237">每個註冊類型都有特定屬性。</span><span class="sxs-lookup"><span data-stu-id="d2052-237">Each register type has specific properties.</span></span> <span data-ttu-id="d2052-238">由於色彩和材質座標目前只有兩個語義，因此大部分的資料通常會被標示為材質座標（即使沒有的話）。</span><span class="sxs-lookup"><span data-stu-id="d2052-238">Because there are currently only two semantics for color and texture coordinates, it is common for most data to be marked as a texture coordinate even when it is not.</span></span>

<span data-ttu-id="d2052-239">請注意，頂點著色器輸出結構使用的輸入具有位置資料，而圖元著色器不會使用此輸入。</span><span class="sxs-lookup"><span data-stu-id="d2052-239">Notice that the vertex shader output structure used an input with position data, which is not used by the pixel shader.</span></span> <span data-ttu-id="d2052-240">HLSL 可讓頂點著色器的有效輸出資料不是圖元著色器的有效輸入資料，前提是它不是在圖元著色器中參考。</span><span class="sxs-lookup"><span data-stu-id="d2052-240">HLSL allows valid output data of a vertex shader that is not valid input data for a pixel shader, provided that it is not referenced in the pixel shader.</span></span>

<span data-ttu-id="d2052-241">輸入引數也可以是陣列。</span><span class="sxs-lookup"><span data-stu-id="d2052-241">Input arguments can also be arrays.</span></span> <span data-ttu-id="d2052-242">編譯器會針對陣列的每個元素自動遞增語法。</span><span class="sxs-lookup"><span data-stu-id="d2052-242">Semantics are automatically incremented by the compiler for each element of the array.</span></span> <span data-ttu-id="d2052-243">例如，請考慮下列明確宣告：</span><span class="sxs-lookup"><span data-stu-id="d2052-243">For instance, consider the following explicit declaration:</span></span>


```
struct VS_OUTPUT
{
    float4 Position   : POSITION;
    float3 Diffuse    : COLOR0;
    float3 Specular   : COLOR1;               
    float3 HalfVector : TEXCOORD3;
    float3 Fresnel    : TEXCOORD2;               
    float3 Reflection : TEXCOORD0;               
    float3 NoiseCoord : TEXCOORD1;               
};

float4 Sparkle(VS_OUTPUT In) : COLOR
```



<span data-ttu-id="d2052-244">上述的明確宣告相當於下列宣告，此宣告將會自動遞增編譯器的語義：</span><span class="sxs-lookup"><span data-stu-id="d2052-244">The explicit declaration given above is equivalent to the following declaration that will have semantics automatically incremented by the compiler:</span></span>


```
float4 Sparkle(float4 Position : POSITION,
                 float3 Col[2] : COLOR0,
                 float3 Tex[4] : TEXCOORD0) : COLOR0
{
   // shader statements
   ...
```



<span data-ttu-id="d2052-245">就像輸入語義一樣，輸出語義也會識別圖元著色器輸出資料的資料使用狀況。</span><span class="sxs-lookup"><span data-stu-id="d2052-245">Just like input semantics, output semantics identify data usage for pixel shader output data.</span></span> <span data-ttu-id="d2052-246">許多圖元著色器只會寫入一個輸出色彩。</span><span class="sxs-lookup"><span data-stu-id="d2052-246">Many pixel shaders write to only one output color.</span></span> <span data-ttu-id="d2052-247">圖元著色器也可以同時將深度值寫出一個或多個轉譯目標， (多達四個) 。</span><span class="sxs-lookup"><span data-stu-id="d2052-247">Pixel shaders can also write out a depth value into one or more multiple render targets at the same time (up to four).</span></span> <span data-ttu-id="d2052-248">和頂點著色器一樣，圖元著色器會使用結構來傳回多個輸出。</span><span class="sxs-lookup"><span data-stu-id="d2052-248">Like vertex shaders, pixel shaders use a structure to return more than one output.</span></span> <span data-ttu-id="d2052-249">此著色器會將0寫入色彩元件以及深度元件。</span><span class="sxs-lookup"><span data-stu-id="d2052-249">This shader writes 0 to the color components, as well as to the depth component.</span></span>


```
struct PS_OUTPUT
{
    float4 Color[4] : COLOR0;
    float  Depth  : DEPTH;
};

PS_OUTPUT main(void)
{
    PS_OUTPUT out;

   // Shader statements
   ...

  // Write up to four pixel shader output colors
  out.Color[0] =  ...
  out.Color[1] =  ...
  out.Color[2] =  ...
  out.Color[3] =  ...

  // Write pixel depth 
  out.Depth =  ...

    return out;
}
```



<span data-ttu-id="d2052-250">圖元著色器輸出色彩的類型必須是 float4。</span><span class="sxs-lookup"><span data-stu-id="d2052-250">Pixel shader output colors must be of type float4.</span></span> <span data-ttu-id="d2052-251">撰寫多個色彩時，必須連續使用所有的輸出色彩。</span><span class="sxs-lookup"><span data-stu-id="d2052-251">When writing multiple colors, all output colors must be used contiguously.</span></span> <span data-ttu-id="d2052-252">換句話說，除非已寫入[COLOR0](dx-graphics-hlsl-semantics.md) ，否則[COLOR1](dx-graphics-hlsl-semantics.md)不能是輸出。</span><span class="sxs-lookup"><span data-stu-id="d2052-252">In other words, [COLOR1](dx-graphics-hlsl-semantics.md) cannot be an output unless [COLOR0](dx-graphics-hlsl-semantics.md) has already been written.</span></span> <span data-ttu-id="d2052-253">圖元著色器深度輸出的類型必須是 float1。</span><span class="sxs-lookup"><span data-stu-id="d2052-253">Pixel shader depth output must be of type float1.</span></span>

### <a name="samplers-and-texture-objects"></a><span data-ttu-id="d2052-254">取樣器和材質物件</span><span class="sxs-lookup"><span data-stu-id="d2052-254">Samplers and Texture Objects</span></span>

<span data-ttu-id="d2052-255">取樣器包含取樣器狀態。</span><span class="sxs-lookup"><span data-stu-id="d2052-255">A sampler contains sampler state.</span></span> <span data-ttu-id="d2052-256">取樣器狀態會指定要取樣的材質，並控制取樣期間完成的篩選。</span><span class="sxs-lookup"><span data-stu-id="d2052-256">Sampler state specifies the texture to be sampled, and controls the filtering that is done during sampling.</span></span> <span data-ttu-id="d2052-257">範例材質需要三個專案：</span><span class="sxs-lookup"><span data-stu-id="d2052-257">Three things are required to sample a texture:</span></span>

-   <span data-ttu-id="d2052-258">材質</span><span class="sxs-lookup"><span data-stu-id="d2052-258">A texture</span></span>
-   <span data-ttu-id="d2052-259">使用取樣器狀態的取樣器 () </span><span class="sxs-lookup"><span data-stu-id="d2052-259">A sampler (with sampler state)</span></span>
-   <span data-ttu-id="d2052-260">取樣指令</span><span class="sxs-lookup"><span data-stu-id="d2052-260">A sampling instruction</span></span>

<span data-ttu-id="d2052-261">您可以使用紋理和取樣器狀態來初始化取樣器，如下所示：</span><span class="sxs-lookup"><span data-stu-id="d2052-261">Samplers can be initialized with textures and sampler state as shown here:</span></span>


```
sampler s = sampler_state 
{ 
  texture = NULL; 
  mipfilter = LINEAR; 
};
```



<span data-ttu-id="d2052-262">以下是範例2D 材質的程式碼範例：</span><span class="sxs-lookup"><span data-stu-id="d2052-262">Here's an example of the code to sample a 2D texture:</span></span>


```
texture tex0;
sampler2D s_2D;

float2 sample_2D(float2 tex : TEXCOORD0) : COLOR
{
  return tex2D(s_2D, tex);
}
```



<span data-ttu-id="d2052-263">紋理會以材質變數 tex0 來宣告。</span><span class="sxs-lookup"><span data-stu-id="d2052-263">The texture is declared with a texture variable tex0.</span></span>

<span data-ttu-id="d2052-264">在此範例中，會宣告名為 s 2d 的取樣器變數 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d2052-264">In this example, a sampler variable named s\_2D is declared.</span></span> <span data-ttu-id="d2052-265">取樣器包含大括弧內的取樣器狀態。</span><span class="sxs-lookup"><span data-stu-id="d2052-265">The sampler contains the sampler state inside of curly braces.</span></span> <span data-ttu-id="d2052-266">這包括將取樣的材質，以及（選擇性）篩選狀態 (也就是包裝模式、篩選模式等 ) 。</span><span class="sxs-lookup"><span data-stu-id="d2052-266">This includes the texture that will be sampled and, optionally, the filter state (that is, wrap modes, filter modes, etc.).</span></span> <span data-ttu-id="d2052-267">如果省略取樣器狀態，則會套用預設取樣器狀態，並指定紋理座標的線性篩選和換行模式。</span><span class="sxs-lookup"><span data-stu-id="d2052-267">If the sampler state is omitted, a default sampler state is applied specifying linear filtering and a wrap mode for the texture coordinates.</span></span> <span data-ttu-id="d2052-268">取樣器函式會採用雙元件浮點紋理座標，並傳回兩個元件的色彩。</span><span class="sxs-lookup"><span data-stu-id="d2052-268">The sampler function takes a two-component floating-point texture coordinate, and returns a two-component color.</span></span> <span data-ttu-id="d2052-269">這會以 float2 傳回類型表示，並代表紅色和綠色元件中的資料。</span><span class="sxs-lookup"><span data-stu-id="d2052-269">This is represented with the float2 return type and represents data in the red and green components.</span></span>

<span data-ttu-id="d2052-270">定義了四種類型的取樣器 (請參閱 [關鍵字](dx-graphics-hlsl-appendix.md)) 和材質查閱是由內建函式執行： [**tex1D (s、t)  (directx HLSL)**](dx-graphics-hlsl-tex1d.md)、 [**tex2D (s、t)  (directx HLSL)**](dx-graphics-hlsl-tex2d.md) [**、tex3D (**](dx-graphics-hlsl-tex3d.md)s、t)  (directx HLSL) 、TEXCUBE (s、t)  ([**directx HLSL)**](dx-graphics-hlsl-texcube.md)。</span><span class="sxs-lookup"><span data-stu-id="d2052-270">Four types of samplers are defined (see [Keywords](dx-graphics-hlsl-appendix.md)) and texture lookups are performed by the intrinsic functions: [**tex1D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md), [**tex2D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md), [**tex3D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex3d.md), [**texCUBE(s, t) (DirectX HLSL)**](dx-graphics-hlsl-texcube.md).</span></span> <span data-ttu-id="d2052-271">以下是3D 取樣的範例：</span><span class="sxs-lookup"><span data-stu-id="d2052-271">Here is an example of 3D sampling:</span></span>


```
texture tex0;
sampler3D s_3D;

float3 sample_3D(float3 tex : TEXCOORD0) : COLOR
{
  return tex3D(s_3D, tex);
}
```



<span data-ttu-id="d2052-272">這個取樣器宣告使用篩選設定和位址模式的預設取樣器狀態。</span><span class="sxs-lookup"><span data-stu-id="d2052-272">This sampler declaration uses default sampler state for the filter settings and address mode.</span></span>

<span data-ttu-id="d2052-273">以下是對應的 cube 取樣範例：</span><span class="sxs-lookup"><span data-stu-id="d2052-273">Here is the corresponding cube sampling example:</span></span>


```
texture tex0;
samplerCUBE s_CUBE;

float3 sample_CUBE(float3 tex : TEXCOORD0) : COLOR
{
  return texCUBE(s_CUBE, tex);
}
```



<span data-ttu-id="d2052-274">最後，以下是1D 取樣範例：</span><span class="sxs-lookup"><span data-stu-id="d2052-274">And finally, here is the 1D sampling example:</span></span>


```
texture tex0;
sampler1D s_1D;

float sample_1D(float tex : TEXCOORD0) : COLOR
{
  return tex1D(s_1D, tex);
}
```



<span data-ttu-id="d2052-275">因為執行時間不支援1D 紋理，所以編譯器會使用2D 材質，並知道 y 座標不重要。</span><span class="sxs-lookup"><span data-stu-id="d2052-275">Because the runtime does not support 1D textures, the compiler will use a 2D texture with the knowledge that the y-coordinate is unimportant.</span></span> <span data-ttu-id="d2052-276">由於 [**tex1D (s，t)  (DIRECTX HLSL)**](dx-graphics-hlsl-tex1d.md) 會實作為2d 材質查閱，因此編譯器可以用有效率的方式自由選擇 y 元件。</span><span class="sxs-lookup"><span data-stu-id="d2052-276">Since [**tex1D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) is implemented as a 2D texture lookup, the compiler is free to choose the y-component in an efficient manner.</span></span> <span data-ttu-id="d2052-277">在某些罕見的情況下，編譯器無法選擇有效率的 y 元件，在此情況下會發出警告。</span><span class="sxs-lookup"><span data-stu-id="d2052-277">In some rare scenarios, the compiler cannot choose an efficient y-component, in which case it will issue a warning.</span></span>


```
texture tex0;
sampler s_1D_float;

float4 main(float texCoords : TEXCOORD) : COLOR
{
    return tex1D(s_1D_float, texCoords);
}
```



<span data-ttu-id="d2052-278">此特定範例效率不佳，因為編譯器必須將輸入座標移至另一個暫存器 (，因為1D 查閱會實作為2D 查閱，並將材質座標宣告為 float1) 。</span><span class="sxs-lookup"><span data-stu-id="d2052-278">This particular example is inefficient because the compiler must move the input coordinate into another register (because a 1D lookup is implemented as a 2D lookup and the texture coordinate is declared as a float1).</span></span> <span data-ttu-id="d2052-279">如果使用 float2 輸入（而非 float1）來重寫程式碼，則編譯器可以使用輸入材質座標，因為它知道 y 會初始化為某個東西。</span><span class="sxs-lookup"><span data-stu-id="d2052-279">If the code is rewritten using a float2 input instead of a float1, the compiler can use the input texture coordinate because it knows that y is initialized to something.</span></span>


```
texture tex0;
sampler s_1D_float2;

float4 main(float2 texCoords : TEXCOORD) : COLOR
{
    return tex1D(s_1D_float2, texCoords);
}
```



<span data-ttu-id="d2052-280">所有紋理查閱都可以使用「偏差」或「proj」 (，也就是 [**tex2Dbias (DIRECTX HLSL)**](dx-graphics-hlsl-tex2dbias.md) [**TEXCUBEPROJ (directx HLSL)**](dx-graphics-hlsl-texcubeproj.md)) 。</span><span class="sxs-lookup"><span data-stu-id="d2052-280">All texture lookups can be appended with "bias" or "proj" (that is, [**tex2Dbias (DirectX HLSL)**](dx-graphics-hlsl-tex2dbias.md), [**texCUBEproj (DirectX HLSL)**](dx-graphics-hlsl-texcubeproj.md)).</span></span> <span data-ttu-id="d2052-281">使用 "proj" 尾碼時，材質座標會除以 w 元件。</span><span class="sxs-lookup"><span data-stu-id="d2052-281">With the "proj" suffix, the texture coordinate is divided by the w-component.</span></span> <span data-ttu-id="d2052-282">使用「偏差」時，會以 w 元件移位 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="d2052-282">With "bias," the mip level is shifted by the w-component.</span></span> <span data-ttu-id="d2052-283">因此，所有具有尾碼的材質查閱一律會採用 float4 輸入。</span><span class="sxs-lookup"><span data-stu-id="d2052-283">Thus, all texture lookups with a suffix always take a float4 input.</span></span> <span data-ttu-id="d2052-284">[**tex1D (s、t)  (DIRECTX HLSL)**](dx-graphics-hlsl-tex1d.md) 和 [**tex2D (s，t)  (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md) 會分別忽略 yz 和 z 元件。</span><span class="sxs-lookup"><span data-stu-id="d2052-284">[**tex1D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) and [**tex2D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md) ignore the yz- and z-components respectively.</span></span>

<span data-ttu-id="d2052-285">您也可以在陣列中使用取樣器，雖然沒有後端目前支援取樣器的動態陣列存取。</span><span class="sxs-lookup"><span data-stu-id="d2052-285">Samplers may also be used in array, although no back end currently supports dynamic array access of samplers.</span></span> <span data-ttu-id="d2052-286">因此，下列是有效的，因為它可以在編譯時期解決：</span><span class="sxs-lookup"><span data-stu-id="d2052-286">Therefore, the following is valid because it can be resolved at compile time:</span></span>


```
tex2D(s[0],tex)
```



<span data-ttu-id="d2052-287">不過，此範例無效。</span><span class="sxs-lookup"><span data-stu-id="d2052-287">However, this example is not valid.</span></span>


```
tex2D(s[a],tex)
```



<span data-ttu-id="d2052-288">取樣器的動態存取主要適用于使用常值迴圈來撰寫程式。</span><span class="sxs-lookup"><span data-stu-id="d2052-288">Dynamic access of samplers is primarily useful for writing programs with literal loops.</span></span> <span data-ttu-id="d2052-289">下列程式碼說明存取的取樣器陣列：</span><span class="sxs-lookup"><span data-stu-id="d2052-289">The following code illustrates sampler array accessing:</span></span>


```
sampler sm[4];

float4 main(float4 tex[4] : TEXCOORD) : COLOR
{
    float4 retColor = 1;

    for(int i = 0; i < 4;i++)
    {
        retColor *= tex2D(sm[i],tex[i]);
    }

    return retColor;
}
```



> [!Note]
>
> <span data-ttu-id="d2052-290">使用 Microsoft Direct3D debug runtime 可協助您捕捉材質中的元件數目與取樣器之間的不符情形。</span><span class="sxs-lookup"><span data-stu-id="d2052-290">Using the Microsoft Direct3D debug runtime can help you catch mismatches between the number of components in a texture and a sampler.</span></span>

 

## <a name="writing-functions"></a><span data-ttu-id="d2052-291">撰寫函數</span><span class="sxs-lookup"><span data-stu-id="d2052-291">Writing Functions</span></span>

<span data-ttu-id="d2052-292">函式會將大型工作分成較小的工作。</span><span class="sxs-lookup"><span data-stu-id="d2052-292">Functions break large tasks into smaller ones.</span></span> <span data-ttu-id="d2052-293">您可以輕鬆地進行較小的工作，而且可以在經過證實之後重複使用。</span><span class="sxs-lookup"><span data-stu-id="d2052-293">Small tasks are easier to debug and can be reused, once proven.</span></span> <span data-ttu-id="d2052-294">函數可用來隱藏其他函式的詳細資料，讓函式組成的程式更容易遵循。</span><span class="sxs-lookup"><span data-stu-id="d2052-294">Functions can be used to hide details of other functions, which makes a program composed of functions easier to follow.</span></span>

<span data-ttu-id="d2052-295">HLSL 函式類似于 C 函式，有數種方式：它們都包含定義和函式主體，而且兩者都宣告傳回型別和引數清單。</span><span class="sxs-lookup"><span data-stu-id="d2052-295">HLSL functions are similar to C functions in several ways: They both contain a definition and a function body and they both declare return types and argument lists.</span></span> <span data-ttu-id="d2052-296">如同 C 函式，HLSL 驗證會在著色器編譯期間，針對引數、引數類型和傳回值進行型別檢查。</span><span class="sxs-lookup"><span data-stu-id="d2052-296">Like C functions, HLSL validation does type checking on the arguments, argument types, and the return value during shader compilation.</span></span>

<span data-ttu-id="d2052-297">與 C 函式不同的是，HLSL 進入點函式會使用語義將函式引數系結至著色器輸入和輸出 (HLSL 函式會在內部忽略語義) 。</span><span class="sxs-lookup"><span data-stu-id="d2052-297">Unlike C functions, HLSL entry point functions use semantics to bind function arguments to shader inputs and outputs (HLSL functions called internally ignore semantics).</span></span> <span data-ttu-id="d2052-298">這可讓您更輕鬆地將緩衝區資料系結至著色器，並將著色器輸出系結至著色器輸入。</span><span class="sxs-lookup"><span data-stu-id="d2052-298">This makes it easier to bind buffer data to a shader, and bind shader outputs to shader inputs.</span></span>

<span data-ttu-id="d2052-299">函式包含宣告和主體，且宣告必須在主體之前。</span><span class="sxs-lookup"><span data-stu-id="d2052-299">A function contains a declaration and a body, and the declaration must precede the body.</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
    return mul(inPos, WorldViewProj );
};
```



<span data-ttu-id="d2052-300">函式宣告包含大括弧前面的所有專案：</span><span class="sxs-lookup"><span data-stu-id="d2052-300">The function declaration includes everything in front of the curly braces:</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
```



<span data-ttu-id="d2052-301">函式宣告包含：</span><span class="sxs-lookup"><span data-stu-id="d2052-301">A function declaration contains:</span></span>

-   <span data-ttu-id="d2052-302">傳回型別</span><span class="sxs-lookup"><span data-stu-id="d2052-302">A return type</span></span>
-   <span data-ttu-id="d2052-303">函數名稱</span><span class="sxs-lookup"><span data-stu-id="d2052-303">A function name</span></span>
-   <span data-ttu-id="d2052-304">引數清單 (選擇性) </span><span class="sxs-lookup"><span data-stu-id="d2052-304">An argument list (optional)</span></span>
-   <span data-ttu-id="d2052-305">輸出語義 (選擇性) </span><span class="sxs-lookup"><span data-stu-id="d2052-305">An output semantic (optional)</span></span>
-   <span data-ttu-id="d2052-306">批註 (選擇性) </span><span class="sxs-lookup"><span data-stu-id="d2052-306">An annotation (optional)</span></span>

<span data-ttu-id="d2052-307">傳回類型可以是任何 HLSL 基本資料類型，例如 float4：</span><span class="sxs-lookup"><span data-stu-id="d2052-307">The return type can be any of the HLSL basic data types such as a float4:</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
   ...
}
```



<span data-ttu-id="d2052-308">傳回型別可以是已定義的結構：</span><span class="sxs-lookup"><span data-stu-id="d2052-308">The return type can be a structure that has already been defined:</span></span>


```
struct VS_OUTPUT
{
    float4  vPosition        : POSITION;
    float4  vDiffuse         : COLOR;
}; 

VS_OUTPUT VertexShader_Tutorial_1(float4 inPos : POSITION )
{
   ...
}
```



<span data-ttu-id="d2052-309">如果函式不會傳回值，void 可以當做傳回型別使用。</span><span class="sxs-lookup"><span data-stu-id="d2052-309">If the function does not return a value, void can be used as the return type.</span></span>


```
void VertexShader_Tutorial_1(float4 inPos : POSITION )
{
   ...
}
```



<span data-ttu-id="d2052-310">傳回型別一律會先出現在函式宣告中。</span><span class="sxs-lookup"><span data-stu-id="d2052-310">The return type always appears first in a function declaration.</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
```



<span data-ttu-id="d2052-311">引數清單會宣告函式的輸入引數。</span><span class="sxs-lookup"><span data-stu-id="d2052-311">An argument list declares the input arguments to a function.</span></span> <span data-ttu-id="d2052-312">它也可以宣告將傳回的值。</span><span class="sxs-lookup"><span data-stu-id="d2052-312">It may also declare values that will be returned.</span></span> <span data-ttu-id="d2052-313">某些引數同時為輸入和輸出引數。</span><span class="sxs-lookup"><span data-stu-id="d2052-313">Some arguments are both input and output arguments.</span></span> <span data-ttu-id="d2052-314">以下是採用四個輸入引數的著色器範例。</span><span class="sxs-lookup"><span data-stu-id="d2052-314">Here is an example of a shader that takes four input arguments.</span></span>


```
float4 Light(float3 LightDir : TEXCOORD1, 
             uniform float4 LightColor,  
             float2 texcrd : TEXCOORD0, 
             uniform sampler samp) : COLOR 
{
    float3 Normal = tex2D(samp,texcrd);

    return dot((Normal*2 - 1), LightDir)*LightColor;
}
```



<span data-ttu-id="d2052-315">此函式會傳回最終色彩，也就是材質樣本和淺色色彩的 blend。</span><span class="sxs-lookup"><span data-stu-id="d2052-315">This function returns a final color, that is a blend of a texture sample and the light color.</span></span> <span data-ttu-id="d2052-316">此函數會接受四個輸入。</span><span class="sxs-lookup"><span data-stu-id="d2052-316">The function takes four inputs.</span></span> <span data-ttu-id="d2052-317">兩個輸入具有語義： LightDir 具有 [TEXCOORD1](dx-graphics-hlsl-semantics.md) 語義，而 Texcrd 具有 [TEXCOORD0](dx-graphics-hlsl-semantics.md) 語義。</span><span class="sxs-lookup"><span data-stu-id="d2052-317">Two inputs have semantics: LightDir has the [TEXCOORD1](dx-graphics-hlsl-semantics.md) semantic, and texcrd has the [TEXCOORD0](dx-graphics-hlsl-semantics.md) semantic.</span></span> <span data-ttu-id="d2052-318">此語義表示這些變數的資料將來自頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d2052-318">The semantics mean that the data for these variables will come from the vertex buffer.</span></span> <span data-ttu-id="d2052-319">雖然 LightDir 變數有 [TEXCOORD1](dx-graphics-hlsl-semantics.md) 語義，但參數可能不是材質座標。</span><span class="sxs-lookup"><span data-stu-id="d2052-319">Even though the LightDir variable has a [TEXCOORD1](dx-graphics-hlsl-semantics.md) semantic, the parameter is probably not a texture coordinate.</span></span> <span data-ttu-id="d2052-320">TEXCOORDn 語義型別通常用來提供未預先定義之型別的語義， (沒有淺色方向) 的頂點著色器輸入語義。</span><span class="sxs-lookup"><span data-stu-id="d2052-320">The TEXCOORDn semantic type is often used to supply a semantic for a type that is not predefined (there is no vertex shader input semantic for a light direction).</span></span>

<span data-ttu-id="d2052-321">另外兩個輸入 LightColor 和 samp 會以 [統一](dx-graphics-hlsl-appendix.md) 關鍵字標記。</span><span class="sxs-lookup"><span data-stu-id="d2052-321">The other two inputs LightColor and samp are labeled with the [uniform](dx-graphics-hlsl-appendix.md) keyword.</span></span> <span data-ttu-id="d2052-322">這些是不會在繪製呼叫之間變更的統一常數。</span><span class="sxs-lookup"><span data-stu-id="d2052-322">These are uniform constants that will not change between draw calls.</span></span> <span data-ttu-id="d2052-323">這些參數的值來自于著色器全域變數。</span><span class="sxs-lookup"><span data-stu-id="d2052-323">The values for these parameters come from shader global variables.</span></span>

<span data-ttu-id="d2052-324">您可以使用 in 關鍵字將引數標記為輸入，並使用 out 關鍵字來標記輸出引數。</span><span class="sxs-lookup"><span data-stu-id="d2052-324">Arguments can be labeled as inputs with the in keyword, and output arguments with the out keyword.</span></span> <span data-ttu-id="d2052-325">無法以傳址方式傳遞引數;但是，如果是使用 inout 關鍵字宣告，則引數可以是輸入和輸出。</span><span class="sxs-lookup"><span data-stu-id="d2052-325">Arguments cannot be passed by reference; however, an argument can be both an input and an output if it is declared with the inout keyword.</span></span> <span data-ttu-id="d2052-326">傳遞給以 inout 關鍵字標記之函式的引數會被視為原來的複本，直到函式傳回為止，然後再複製回來。</span><span class="sxs-lookup"><span data-stu-id="d2052-326">Arguments passed to a function that are marked with the inout keyword are considered copies of the original until the function returns, and they are copied back.</span></span> <span data-ttu-id="d2052-327">以下是使用 inout 的範例：</span><span class="sxs-lookup"><span data-stu-id="d2052-327">Here's an example using inout:</span></span>


```
void Increment_ByVal(inout float A, inout float B) 
{ 
    A++; B++;
}
```



<span data-ttu-id="d2052-328">此函式會遞增 A 和 B 中的值，並傳回這些值。</span><span class="sxs-lookup"><span data-stu-id="d2052-328">This function increments the values in A and B and returns them.</span></span>

<span data-ttu-id="d2052-329">函數主體是函式宣告之後的所有程式碼。</span><span class="sxs-lookup"><span data-stu-id="d2052-329">The function body is all of the code after the function declaration.</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
    return mul(inPos, WorldViewProj );
};
```



<span data-ttu-id="d2052-330">主體是由以大括弧括住的語句所組成。</span><span class="sxs-lookup"><span data-stu-id="d2052-330">The body consists of statements which are surrounded by curly braces.</span></span> <span data-ttu-id="d2052-331">函數主體會使用變數、常值、運算式和語句來執行所有功能。</span><span class="sxs-lookup"><span data-stu-id="d2052-331">The function body implements all of the functionality using variables, literals, expressions, and statements.</span></span>

<span data-ttu-id="d2052-332">著色器主體會執行兩項作業：它會執行矩陣相乘，並傳回 float4 結果。</span><span class="sxs-lookup"><span data-stu-id="d2052-332">The shader body does two things: it performs a matrix multiply and returns a float4 result.</span></span> <span data-ttu-id="d2052-333">矩陣相乘是利用 [**mul (DIRECTX HLSL)**](dx-graphics-hlsl-mul.md) 函式來完成，這會執行4x4 矩陣相乘。</span><span class="sxs-lookup"><span data-stu-id="d2052-333">The matrix multiply is accomplished with the [**mul (DirectX HLSL)**](dx-graphics-hlsl-mul.md) function, which performs a 4x4 matrix multiply.</span></span> <span data-ttu-id="d2052-334">**mul (DIRECTX HLSL)** 稱為內建函式，因為它已經內建在函式的 HLSL 程式庫中。</span><span class="sxs-lookup"><span data-stu-id="d2052-334">**mul (DirectX HLSL)** is called an intrinsic function because it is already built into the HLSL library of functions.</span></span> <span data-ttu-id="d2052-335">下一節將更詳細地討論內建函式。</span><span class="sxs-lookup"><span data-stu-id="d2052-335">Intrinsic functions will be covered in more detail in the next section.</span></span>

<span data-ttu-id="d2052-336">矩陣乘合併輸入向量 Pos 和複合矩陣 WorldViewProj。</span><span class="sxs-lookup"><span data-stu-id="d2052-336">The matrix multiply combines an input vector Pos and a composite matrix WorldViewProj.</span></span> <span data-ttu-id="d2052-337">結果是將資料轉換為螢幕空間。</span><span class="sxs-lookup"><span data-stu-id="d2052-337">The result is position data transformed into screen space.</span></span> <span data-ttu-id="d2052-338">這是我們可以進行的最小頂點著色器處理。</span><span class="sxs-lookup"><span data-stu-id="d2052-338">This is the minimum vertex shader processing we can do.</span></span> <span data-ttu-id="d2052-339">如果我們使用的是固定函式管線，而不是頂點著色器，則可以在執行這項轉換之後繪製頂點資料。</span><span class="sxs-lookup"><span data-stu-id="d2052-339">If we were using the fixed function pipeline instead of a vertex shader, the vertex data could be drawn after doing this transform.</span></span>

<span data-ttu-id="d2052-340">函數主體中的最後一個語句是 return 語句。</span><span class="sxs-lookup"><span data-stu-id="d2052-340">The last statement in a function body is a return statement.</span></span> <span data-ttu-id="d2052-341">就像 C 一樣，這個語句會將 control 從函式傳回給呼叫函數的語句。</span><span class="sxs-lookup"><span data-stu-id="d2052-341">Just like C, this statement returns control from the function to the statement that called the function.</span></span>

<span data-ttu-id="d2052-342">函數傳回類型可以是在 HLSL 中定義的任何單一資料型別，包括 bool、int 半形、float 和 double。</span><span class="sxs-lookup"><span data-stu-id="d2052-342">Function return types can be any of the simple data types defined in HLSL, including bool, int half, float, and double.</span></span> <span data-ttu-id="d2052-343">傳回類型可以是其中一種複雜的資料類型，例如向量和矩陣。</span><span class="sxs-lookup"><span data-stu-id="d2052-343">Return types can be one of the complex data types such as vectors and matrices.</span></span> <span data-ttu-id="d2052-344">參考物件的 HLSL 類型不能當做傳回類型使用。</span><span class="sxs-lookup"><span data-stu-id="d2052-344">HLSL types that refer to objects cannot be used as return types.</span></span> <span data-ttu-id="d2052-345">這包括無效、vertexshader、材質和取樣器。</span><span class="sxs-lookup"><span data-stu-id="d2052-345">This includes pixelshader, vertexshader, texture, and sampler.</span></span>

<span data-ttu-id="d2052-346">以下是使用傳回型別之結構的函式範例。</span><span class="sxs-lookup"><span data-stu-id="d2052-346">Here is an example of a function that uses a structure for a return type.</span></span>


```
float4x4 WorldViewProj : WORLDVIEWPROJ;

struct VS_OUTPUT
{
    float4 Pos  : POSITION;
};

VS_OUTPUT VS_HLL_Example(float4 inPos : POSITION )
{
    VS_OUTPUT Out;

    Out.Pos = mul(inPos,  WorldViewProj );

    return Out;
};
```



<span data-ttu-id="d2052-347">Float4 傳回型別已取代為結構和 \_ 輸出，現在包含單一 float4 成員。</span><span class="sxs-lookup"><span data-stu-id="d2052-347">The float4 return type has been replaced with the structure VS\_OUTPUT, which now contains a single float4 member.</span></span>

<span data-ttu-id="d2052-348">Return 語句表示函式的結尾。</span><span class="sxs-lookup"><span data-stu-id="d2052-348">A return statement signals the end of a function.</span></span> <span data-ttu-id="d2052-349">這是最簡單的 return 語句。</span><span class="sxs-lookup"><span data-stu-id="d2052-349">This is the simplest return statement.</span></span> <span data-ttu-id="d2052-350">它會將函數的控制權傳回給呼叫程式。</span><span class="sxs-lookup"><span data-stu-id="d2052-350">It returns control from the function to the calling program.</span></span> <span data-ttu-id="d2052-351">它不會傳回任何值。</span><span class="sxs-lookup"><span data-stu-id="d2052-351">It returns no value.</span></span>


```
void main()
{
    return ;
}
```



<span data-ttu-id="d2052-352">Return 語句可以傳回一或多個值。</span><span class="sxs-lookup"><span data-stu-id="d2052-352">A return statement can return one or more values.</span></span> <span data-ttu-id="d2052-353">此範例會傳回常值：</span><span class="sxs-lookup"><span data-stu-id="d2052-353">This example returns a literal value:</span></span>


```
float main( float input : COLOR0) : COLOR0
{
    return 0;
}
```



<span data-ttu-id="d2052-354">此範例會傳回運算式的純量結果：</span><span class="sxs-lookup"><span data-stu-id="d2052-354">This example returns the scalar result of an expression:</span></span>


```
return  light.enabled;
```



<span data-ttu-id="d2052-355">此範例會傳回由區域變數和常值所構成的 float4：</span><span class="sxs-lookup"><span data-stu-id="d2052-355">This example returns a float4 constructed from a local variable and a literal:</span></span>


```
return  float4(color.rgb, 1) ;
```



<span data-ttu-id="d2052-356">此範例會傳回從內建函式傳回的結果所建立的 float4，以及一些常值：</span><span class="sxs-lookup"><span data-stu-id="d2052-356">This example returns a float4 that is constructed from the result returned from an intrinsic function, and a few literal values:</span></span>


```
float4 func(float2 a: POSITION): COLOR
{
    return float4(sin(length(a) * 100.0) * 0.5 + 0.5, sin(a.y * 50.0), 0, 1);
}
```



<span data-ttu-id="d2052-357">這個範例會傳回包含一或多個成員的結構：</span><span class="sxs-lookup"><span data-stu-id="d2052-357">This example returns a structure that contains one or more members:</span></span>


```
float4x4 WorldViewProj;

struct VS_OUTPUT
{
    float4 Pos  : POSITION;
};

VS_OUTPUT VertexShader_Tutorial_1(float4 inPos : POSITION )
{
    VS_OUTPUT out;
    out.Pos = mul(inPos, WorldViewProj );
    return out;
};
```



## <a name="flow-control"></a><span data-ttu-id="d2052-358">流量控制</span><span class="sxs-lookup"><span data-stu-id="d2052-358">Flow Control</span></span>

<span data-ttu-id="d2052-359">最新的頂點和圖元著色器硬體設計為逐行執行著色器，並執行每個指令。</span><span class="sxs-lookup"><span data-stu-id="d2052-359">Most current vertex and pixel shader hardware is designed to run a shader line by line, executing each instruction once.</span></span> <span data-ttu-id="d2052-360">HLSL 支援 flow 控制，其中包括靜態分支、前提指示、靜態迴圈、動態分支和動態迴圈。</span><span class="sxs-lookup"><span data-stu-id="d2052-360">HLSL supports flow control, which includes static branching, predicated instructions, static looping, dynamic branching, and dynamic looping.</span></span>

<span data-ttu-id="d2052-361">先前，使用 if 語句會產生組合語言著色器程式碼，該程式碼會同時執行程式碼流程的 if 端和 else 端。</span><span class="sxs-lookup"><span data-stu-id="d2052-361">Previously, using an if statement resulted in assembly-language shader code that implements both the if side and the else side of the code flow.</span></span> <span data-ttu-id="d2052-362">以下是針對 vs 1 1 編譯的 HLSL 程式碼範例 \_ \_ ：</span><span class="sxs-lookup"><span data-stu-id="d2052-362">Here is an example of the in HLSL code that was compiled for vs\_1\_1:</span></span>


```
if (Value > 0)
    oPos = Value1; 
else
    oPos = Value2; 
```



<span data-ttu-id="d2052-363">以下是產生的元件程式碼：</span><span class="sxs-lookup"><span data-stu-id="d2052-363">And here is the resulting assembly code:</span></span>


```
// Calculate linear interpolation value in r0.w
mov r1.w, c2.x               
slt r0.w, c3.x, r1.w         
// Linear interpolation between value1 and value2
mov r7, -c1                      
add r2, r7, c0                   
mad oPos, r0.w, r2, c1  
```



<span data-ttu-id="d2052-364">有些硬體允許靜態或動態迴圈，但大部分都需要線性執行。</span><span class="sxs-lookup"><span data-stu-id="d2052-364">Some hardware allows for either static or dynamic looping, but most require linear execution.</span></span> <span data-ttu-id="d2052-365">在不支援迴圈的模型上，所有迴圈都必須是展開。</span><span class="sxs-lookup"><span data-stu-id="d2052-365">On the models that do not support looping, all loops must be unrolled.</span></span> <span data-ttu-id="d2052-366">例如，即使是 ps 1 1 著色器，也會使用展開迴圈的 [DepthOfField 範例](https://msdn.microsoft.com/library/Ee416592(v=VS.85).aspx) 範例 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="d2052-366">An example is the [DepthOfField Sample](https://msdn.microsoft.com/library/Ee416592(v=VS.85).aspx) sample that uses unrolled loops even for ps\_1\_1 shaders.</span></span>

<span data-ttu-id="d2052-367">HLSL 現在支援下列每種類型的流量控制：</span><span class="sxs-lookup"><span data-stu-id="d2052-367">HLSL now includes support for each of these types of flow control:</span></span>

-   <span data-ttu-id="d2052-368">靜態分支</span><span class="sxs-lookup"><span data-stu-id="d2052-368">static branching</span></span>
-   <span data-ttu-id="d2052-369">前提指示</span><span class="sxs-lookup"><span data-stu-id="d2052-369">predicated instructions</span></span>
-   <span data-ttu-id="d2052-370">靜態迴圈</span><span class="sxs-lookup"><span data-stu-id="d2052-370">static looping</span></span>
-   <span data-ttu-id="d2052-371">動態分支</span><span class="sxs-lookup"><span data-stu-id="d2052-371">dynamic branching</span></span>
-   <span data-ttu-id="d2052-372">動態迴圈</span><span class="sxs-lookup"><span data-stu-id="d2052-372">dynamic looping</span></span>

<span data-ttu-id="d2052-373">靜態分支可讓您根據布林著色器常數，開啟或關閉著色器程式碼區塊。</span><span class="sxs-lookup"><span data-stu-id="d2052-373">Static branching allows blocks of shader code to be switched on or off based on a Boolean shader constant.</span></span> <span data-ttu-id="d2052-374">這是一種方便的方法，可根據目前轉譯的物件類型來啟用或停用程式碼路徑。</span><span class="sxs-lookup"><span data-stu-id="d2052-374">This is a convenient method for enabling or disabling code paths based on the type of object currently being rendered.</span></span> <span data-ttu-id="d2052-375">您可以使用目前的著色器來決定要支援的功能，然後設定取得該行為所需的布林值旗標，以進行繪製呼叫。</span><span class="sxs-lookup"><span data-stu-id="d2052-375">Between draw calls, you can decide which features you want to support with the current shader and then set the Boolean flags required to get that behavior.</span></span> <span data-ttu-id="d2052-376">在著色器執行期間，會略過布林值常數停用的任何語句。</span><span class="sxs-lookup"><span data-stu-id="d2052-376">Any statements that are disabled by a Boolean constant are skipped during shader execution.</span></span>

<span data-ttu-id="d2052-377">最熟悉的分支支援是動態分支。</span><span class="sxs-lookup"><span data-stu-id="d2052-377">The most familiar branching support is dynamic branching.</span></span> <span data-ttu-id="d2052-378">使用動態分支時，比較準則位於變數中，這表示會在執行時間針對每個頂點或每個圖元進行比較 (而不是在編譯時期進行比較，或在兩個繪製呼叫之間) 。</span><span class="sxs-lookup"><span data-stu-id="d2052-378">With dynamic branching, the comparison condition resides in a variable, which means that the comparison is done for each vertex or each pixel at run time (as opposed to the comparison occurring at compile time, or between two draw calls).</span></span> <span data-ttu-id="d2052-379">效能衝擊是分支的成本加上所採用之分支端的指示成本。</span><span class="sxs-lookup"><span data-stu-id="d2052-379">The performance hit is the cost of the branch plus the cost of the instructions on the side of the branch taken.</span></span> <span data-ttu-id="d2052-380">動態分支是在著色器模型3或更高版本中執行。</span><span class="sxs-lookup"><span data-stu-id="d2052-380">Dynamic branching is implemented in shader model 3 or higher.</span></span> <span data-ttu-id="d2052-381">將使用這些模型的著色器優化，類似于將 CPU 上執行的程式碼優化。</span><span class="sxs-lookup"><span data-stu-id="d2052-381">Optimizing shaders that work with these models is similar to optimizing code that runs on a CPU.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2052-382">相關主題</span><span class="sxs-lookup"><span data-stu-id="d2052-382">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2052-383">HLSL 的程式設計指南</span><span class="sxs-lookup"><span data-stu-id="d2052-383">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 

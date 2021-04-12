---
title: 使用著色器和著色器資源
description: 現在就來瞭解如何使用著色器和著色器資源來開發 Windows 8 的 Microsoft DirectX 遊戲。
ms.assetid: 25a11983-e3f6-4bd3-86f1-d660edc4cd4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ac147971221b04b02f2a45af8e8d4f6855a5e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375712"
---
# <a name="work-with-shaders-and-shader-resources"></a><span data-ttu-id="18541-103">使用著色器和著色器資源</span><span class="sxs-lookup"><span data-stu-id="18541-103">Work with shaders and shader resources</span></span>

<span data-ttu-id="18541-104">現在就來瞭解如何使用著色器和著色器資源來開發 Windows 8 的 Microsoft DirectX 遊戲。</span><span class="sxs-lookup"><span data-stu-id="18541-104">It's time to learn how to work with shaders and shader resources in developing your Microsoft DirectX game for Windows 8.</span></span> <span data-ttu-id="18541-105">我們已瞭解如何設定圖形裝置和資源，而且您可能甚至已開始修改其管線。</span><span class="sxs-lookup"><span data-stu-id="18541-105">We've seen how to set up the graphics device and resources, and perhaps you've even started modifying its pipeline.</span></span> <span data-ttu-id="18541-106">現在讓我們來看一下圖元和頂點著色器。</span><span class="sxs-lookup"><span data-stu-id="18541-106">So now let's look at pixel and vertex shaders.</span></span>

<span data-ttu-id="18541-107">如果您不熟悉著色器語言，則會依序進行快速討論。</span><span class="sxs-lookup"><span data-stu-id="18541-107">If you aren't familiar with shader languages, a quick discussion is in order.</span></span> <span data-ttu-id="18541-108">著色器是小型的低層級程式，會在圖形管線中的特定階段進行編譯和執行。</span><span class="sxs-lookup"><span data-stu-id="18541-108">Shaders are small, low-level programs that are compiled and run at specific stages in the graphics pipeline.</span></span> <span data-ttu-id="18541-109">其專長是非常快速的浮點數學運算。</span><span class="sxs-lookup"><span data-stu-id="18541-109">Their specialty is very fast floating-point mathematical operations.</span></span> <span data-ttu-id="18541-110">最常見的著色器程式如下：</span><span class="sxs-lookup"><span data-stu-id="18541-110">The most common shader programs are:</span></span>

-   <span data-ttu-id="18541-111">**頂點著色器**—針對場景中的每個頂點執行。</span><span class="sxs-lookup"><span data-stu-id="18541-111">**Vertex shader**—Executed for each vertex in a scene.</span></span> <span data-ttu-id="18541-112">此著色器會在呼叫端應用程式提供給它的頂點緩衝區元素上運作，而且會以最少的方式產生4個元件的位置向量，以將其柵格化到圖元位置。</span><span class="sxs-lookup"><span data-stu-id="18541-112">This shader operates on vertex buffer elements provided to it by the calling app, and minimally results in a 4-component position vector that will be rasterized into a pixel position.</span></span>
-   <span data-ttu-id="18541-113">**圖元著色器**—針對轉譯目標中的每個圖元執行。</span><span class="sxs-lookup"><span data-stu-id="18541-113">**Pixel shader**—Executed for each pixel in a render target.</span></span> <span data-ttu-id="18541-114">此著色器會從最簡單管線中 (的上一個著色器階段接收柵格化座標，這會是頂點著色器) ，並傳回該圖元位置) 的色彩 (或其他4個元件值，然後寫入轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="18541-114">This shader receives rasterized coordinates from previous shader stages (in the simplest pipelines, this would be the vertex shader) and returns a color (or other 4-component value) for that pixel position, which is then written into a render target.</span></span>

<span data-ttu-id="18541-115">此範例包括非常基本的頂點和圖元著色器，只繪製幾何，以及更複雜的著色器，以新增基本的光源計算。</span><span class="sxs-lookup"><span data-stu-id="18541-115">This example includes very basic vertex and pixel shaders that only draw geometry, and more complex shaders that add basic lighting calculations.</span></span>

<span data-ttu-id="18541-116">著色器程式是以 Microsoft 高階著色器語言撰寫 (HLSL) 。</span><span class="sxs-lookup"><span data-stu-id="18541-116">Shader programs are written in Microsoft High Level Shader Language (HLSL).</span></span> <span data-ttu-id="18541-117">HLSL 語法看起來很像 C，但是沒有指標。</span><span class="sxs-lookup"><span data-stu-id="18541-117">HLSL syntax looks a lot like C, but without the pointers.</span></span> <span data-ttu-id="18541-118">著色器程式必須非常精簡且有效率。</span><span class="sxs-lookup"><span data-stu-id="18541-118">Shader programs must be very compact and efficient.</span></span> <span data-ttu-id="18541-119">如果您的著色器編譯為太多指示，則無法執行，而且會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="18541-119">If your shader compiles to too many instructions, it cannot be run and an error is returned.</span></span> <span data-ttu-id="18541-120"> (請注意，所允許的確切指令數目是 [Direct3D 功能等級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)的一部分。 ) </span><span class="sxs-lookup"><span data-stu-id="18541-120">(Note that the exact number of instructions allowed is part of the [Direct3D feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro).)</span></span>

<span data-ttu-id="18541-121">在 Direct3D 中，著色器不會在執行時間編譯;這些專案會在編譯器的其餘部分編譯時進行編譯。</span><span class="sxs-lookup"><span data-stu-id="18541-121">In Direct3D, shaders are not compiled at run time; they are compiled when the rest of the program is compiled.</span></span> <span data-ttu-id="18541-122">當您使用 Microsoft Visual Studio 2013 來編譯應用程式時，HLSL 檔案會編譯成 CSO () 您的應用程式必須先載入並置於 GPU 記憶體中的檔案，才能進行繪製。</span><span class="sxs-lookup"><span data-stu-id="18541-122">When you compile your app with Microsoft Visual Studio 2013, the HLSL files are compiled to CSO (.cso) files that your app must load and place in GPU memory prior to drawing.</span></span> <span data-ttu-id="18541-123">當您封裝應用程式時，請確定您已將這些 CSO 檔案包含在您的應用程式中;這些資產就像是網格和材質一樣。</span><span class="sxs-lookup"><span data-stu-id="18541-123">Make sure you include these CSO files with your app when you package it; they are assets just like meshes and textures.</span></span>

## <a name="understand-hlsl-semantics"></a><span data-ttu-id="18541-124">瞭解 HLSL 語義</span><span class="sxs-lookup"><span data-stu-id="18541-124">Understand HLSL semantics</span></span>

<span data-ttu-id="18541-125">在繼續之前，請務必花點時間討論 HLSL 語義，因為它們通常是新 Direct3D 開發人員的混淆點。</span><span class="sxs-lookup"><span data-stu-id="18541-125">It's important to take a moment to discuss HLSL semantics before we continue, because they are often a point of confusion for new Direct3D developers.</span></span> <span data-ttu-id="18541-126">HLSL 語義是識別應用程式與著色器程式之間傳遞之值的字串。</span><span class="sxs-lookup"><span data-stu-id="18541-126">HLSL semantics are strings that identify a value passed between the app and a shader program.</span></span> <span data-ttu-id="18541-127">雖然它們可以是各種可能的字串，但最佳做法是使用表示使用方式的字串 `POSITION` 或 `COLOR` 。</span><span class="sxs-lookup"><span data-stu-id="18541-127">Although they can be any of a variety of possible strings, the best practice is to use a string like `POSITION` or `COLOR` that indicates the usage.</span></span> <span data-ttu-id="18541-128">當您要建立常數緩衝區或輸入配置時，可以指派這些語義。</span><span class="sxs-lookup"><span data-stu-id="18541-128">You assign these semantics when you are constructing a constant buffer or input layout.</span></span> <span data-ttu-id="18541-129">您也可以在語意後附加 0 到 7 的數字，在類似的值使用不同的登錄。</span><span class="sxs-lookup"><span data-stu-id="18541-129">You can also append a number between 0 and 7 to the semantic so that you use separate registers for similar values.</span></span> <span data-ttu-id="18541-130">例如：COLOR0、COLOR1、COLOR2...</span><span class="sxs-lookup"><span data-stu-id="18541-130">For example: COLOR0, COLOR1, COLOR2...</span></span>

<span data-ttu-id="18541-131">前置詞為 "SV" 的語義 \_ 是由著色器程式寫入的 *系統值* 語義; 您的遊戲本身 (在 CPU 上執行) 無法修改它們。</span><span class="sxs-lookup"><span data-stu-id="18541-131">Semantics that are prefixed with "SV\_" are *system value* semantics that are written to by your shader program; your game itself (running on the CPU) cannot modify them.</span></span> <span data-ttu-id="18541-132">一般而言，這些語義包含的值，是來自圖形管線中另一個著色器階段的輸入或輸出，或是由 GPU 完全產生的輸入或輸出。</span><span class="sxs-lookup"><span data-stu-id="18541-132">Typically, these semantics contain values that are inputs or outputs from another shader stage in the graphics pipeline, or that are generated entirely by the GPU.</span></span>

<span data-ttu-id="18541-133">此外， `SV_` 當語義用來指定著色器階段的輸入或輸出時，也會有不同的行為。</span><span class="sxs-lookup"><span data-stu-id="18541-133">Additionally, `SV_` semantics have different behaviors when they are used to specify input to or output from a shader stage.</span></span> <span data-ttu-id="18541-134">例如， `SV_POSITION` (輸出) 包含在頂點著色器階段期間轉換的頂點資料，而 `SV_POSITION` (*輸入*) 包含圖元位置值，這些值是在點陣化階段期間由 GPU 所插入。</span><span class="sxs-lookup"><span data-stu-id="18541-134">For example, `SV_POSITION` (output) contains the vertex data transformed during the vertex shader stage, and `SV_POSITION` (*input*) contains the pixel position values that were interpolated by the GPU during the rasterization stage.</span></span>

<span data-ttu-id="18541-135">以下是一些常見的 HLSL 語義：</span><span class="sxs-lookup"><span data-stu-id="18541-135">Here are a few common HLSL semantics:</span></span>

-   <span data-ttu-id="18541-136">`POSITION` 針對頂點緩衝區資料 (*n*) 。</span><span class="sxs-lookup"><span data-stu-id="18541-136">`POSITION`(*n*) for vertex buffer data.</span></span> <span data-ttu-id="18541-137">`SV_POSITION` 提供圖元的圖元位置給圖元著色器，且無法由您的遊戲撰寫。</span><span class="sxs-lookup"><span data-stu-id="18541-137">`SV_POSITION` provides a pixel position to the pixel shader and cannot be written by your game.</span></span>
-   <span data-ttu-id="18541-138">`NORMAL` 針對頂點緩衝區所提供的一般資料， (*n*) 。</span><span class="sxs-lookup"><span data-stu-id="18541-138">`NORMAL`(*n*) for normal data provided by the vertex buffer.</span></span>
-   <span data-ttu-id="18541-139">`TEXCOORD` (*n*) 提供給著色器的材質 UV 座標資料。</span><span class="sxs-lookup"><span data-stu-id="18541-139">`TEXCOORD`(*n*) for texture UV coordinate data supplied to a shader.</span></span>
-   <span data-ttu-id="18541-140">`COLOR` (n) 提供給著色器的 RGBA 色彩資料。</span><span class="sxs-lookup"><span data-stu-id="18541-140">`COLOR`(n) for RGBA color data supplied to a shader.</span></span> <span data-ttu-id="18541-141">請注意，它的處理方式相同以協調資料，包括在點陣化期間插即值;此語義只是協助您識別它是色彩資料。</span><span class="sxs-lookup"><span data-stu-id="18541-141">Note that it is treated identically to coordinate data, including interpolating the value during rasterization; the semantic simply helps you identify that it is color data.</span></span>
-   <span data-ttu-id="18541-142">`SV_Target`\[n \] 用於從圖元著色器寫入目標材質或其他圖元緩衝區。</span><span class="sxs-lookup"><span data-stu-id="18541-142">`SV_Target`\[n\] for writing from a pixel shader to a target texture or other pixel buffer.</span></span>

<span data-ttu-id="18541-143">我們會在討論範例時看到 HLSL 語義的一些範例。</span><span class="sxs-lookup"><span data-stu-id="18541-143">We'll see some examples of HLSL semantics as we review the example.</span></span>

## <a name="read-from-the-constant-buffers"></a><span data-ttu-id="18541-144">從常數緩衝區讀取</span><span class="sxs-lookup"><span data-stu-id="18541-144">Read from the constant buffers</span></span>

<span data-ttu-id="18541-145">如果該緩衝區以資源的形式附加到其階段，任何著色器都可以從常數緩衝區讀取。</span><span class="sxs-lookup"><span data-stu-id="18541-145">Any shader can read from a constant buffer if that buffer is attached to its stage as a resource.</span></span> <span data-ttu-id="18541-146">在此範例中，只會指派常數緩衝區給頂點著色器。</span><span class="sxs-lookup"><span data-stu-id="18541-146">In this example, only the vertex shader is assigned a constant buffer.</span></span>

<span data-ttu-id="18541-147">常數緩衝區會在兩個位置中宣告：在 c + + 程式碼中，以及將存取它的對應 HLSL 檔中。</span><span class="sxs-lookup"><span data-stu-id="18541-147">The constant buffer is declared in two places: in the C++ code, and in the corresponding HLSL files that will access it.</span></span>

<span data-ttu-id="18541-148">以下是在 c + + 程式碼中宣告常數緩衝區結構的方式。</span><span class="sxs-lookup"><span data-stu-id="18541-148">Here's how the constant buffer struct is declared in the C++ code.</span></span>


```C++
typedef struct _constantBufferStruct {
    DirectX::XMFLOAT4X4 world;
    DirectX::XMFLOAT4X4 view;
    DirectX::XMFLOAT4X4 projection;
} ConstantBufferStruct;
```



<span data-ttu-id="18541-149">當您在 c + + 程式碼中宣告常數緩衝區的結構時，請確定所有資料都已正確對齊16位元組的界限。</span><span class="sxs-lookup"><span data-stu-id="18541-149">When declaring the structure for the constant buffer in your C++ code, ensure that all of the data is correctly aligned along 16-byte boundaries.</span></span> <span data-ttu-id="18541-150">若要這麼做，最簡單的方式是使用 [DirectXMath](/windows/desktop/dxmath/directxmath-portal) 類型，例如 **XMFLOAT4** 或 **XMFLOAT4X4**，如範例程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="18541-150">The easiest way to do this is to use [DirectXMath](/windows/desktop/dxmath/directxmath-portal) types, like **XMFLOAT4** or **XMFLOAT4X4**, as seen in the example code.</span></span> <span data-ttu-id="18541-151">您也可以藉由宣告靜態判斷提示，來防止未對齊的緩衝區：</span><span class="sxs-lookup"><span data-stu-id="18541-151">You can also guard against misaligned buffers by declaring a static assert:</span></span>


```C++
// Assert that the constant buffer remains 16-byte aligned.
static_assert((sizeof(ConstantBufferStruct) % 16) == 0, "Constant Buffer size must be 16-byte aligned");
```



<span data-ttu-id="18541-152">如果 **ConstantBufferStruct** 未對齊16位元組，這行程式碼會在編譯時期造成錯誤。</span><span class="sxs-lookup"><span data-stu-id="18541-152">This line of code will cause an error at compile time if **ConstantBufferStruct** is not 16-byte aligned.</span></span> <span data-ttu-id="18541-153">如需常數緩衝區對齊和封裝的詳細資訊，請參閱 [常數變數的封裝規則](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules)。</span><span class="sxs-lookup"><span data-stu-id="18541-153">For more information about constant buffer alignment and packing, see [Packing Rules for Constant Variables](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules).</span></span>

<span data-ttu-id="18541-154">現在，以下是在頂點著色器 HLSL 中宣告常數緩衝區的方式。</span><span class="sxs-lookup"><span data-stu-id="18541-154">Now, here's how the constant buffer is declared in the vertex shader HLSL.</span></span>


```C++
cbuffer ModelViewProjectionConstantBuffer : register(b0)
{
    matrix mWorld;      // world matrix for object
    matrix View;        // view matrix
    matrix Projection;  // projection matrix
};
```



<span data-ttu-id="18541-155">所有緩衝區（常數、材質、取樣器或其他）都必須定義暫存器，以便 GPU 可以存取它們。</span><span class="sxs-lookup"><span data-stu-id="18541-155">All buffers—constant, texture, sampler, or other—must have a register defined so the GPU can access them.</span></span> <span data-ttu-id="18541-156">每個著色器階段最多可允許15個常數緩衝區，而且每個緩衝區最多可以容納4096個常數變數。</span><span class="sxs-lookup"><span data-stu-id="18541-156">Each shader stage allows up to 15 constant buffers, and each buffer can hold up to 4,096 constant variables.</span></span> <span data-ttu-id="18541-157">使用 register 宣告語法如下所示：</span><span class="sxs-lookup"><span data-stu-id="18541-157">The register-usage declaration syntax is as follows:</span></span>

-   <span data-ttu-id="18541-158">**b \* \* *\#* ：常數緩衝區的註冊 (** cbuffer \* \* ) 。</span><span class="sxs-lookup"><span data-stu-id="18541-158">**b\*\**\#*: A register for a constant buffer (** cbuffer\*\*).</span></span>
-   <span data-ttu-id="18541-159">**t \* \* *\#* ： (** tbuffer \* \* ) 的材質緩衝區註冊。</span><span class="sxs-lookup"><span data-stu-id="18541-159">**t\*\**\#*: A register for a texture buffer (** tbuffer\*\*).</span></span>
-   <span data-ttu-id="18541-160">**s \* \#**：為取樣器註冊。</span><span class="sxs-lookup"><span data-stu-id="18541-160">\**s\*\*\*\#*: A register for a sampler.</span></span> <span data-ttu-id="18541-161"> (取樣器會定義材質資源中材質的查閱行為。 ) </span><span class="sxs-lookup"><span data-stu-id="18541-161">(A sampler defines the lookup behavior for texels in the texture resource.)</span></span>

<span data-ttu-id="18541-162">例如，圖元著色器的 HLSL 可能會採用材質和取樣器做為輸入，如下所示。</span><span class="sxs-lookup"><span data-stu-id="18541-162">For example, the HLSL for a pixel shader might take a texture and a sampler as input with a declaration like this.</span></span>

``` syntax
Texture2D simpleTexture : register(t0);
SamplerState simpleSampler : register(s0);
```

<span data-ttu-id="18541-163">您可自行將常數緩衝區指派給暫存器—當您設定管線時，會將常數緩衝區附加至您在 HLSL 檔案中指派給它的相同位置。</span><span class="sxs-lookup"><span data-stu-id="18541-163">It's up to you to assign constant buffers to registers—when you set up the pipeline, you attach a constant buffer to the same slot you assigned it to in the HLSL file.</span></span> <span data-ttu-id="18541-164">例如，在上一個主題中，呼叫 [**VSSetConstantBuffers**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vssetconstantbuffers) 會對第一個參數表示 ' 0 '。</span><span class="sxs-lookup"><span data-stu-id="18541-164">For example, in the previous topic the call to [**VSSetConstantBuffers**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vssetconstantbuffers) indicates '0' for the first parameter.</span></span> <span data-ttu-id="18541-165">這會告知 Direct3D 將常數緩衝區資源附加至 register 0，以符合緩衝區的指派，在 HLSL 檔中 **註冊 (b0)** 。</span><span class="sxs-lookup"><span data-stu-id="18541-165">That tells Direct3D to attach the constant buffer resource to register 0, which matches the buffer's assignment to **register(b0)** in the HLSL file.</span></span>

## <a name="read-from-the-vertex-buffers"></a><span data-ttu-id="18541-166">從頂點緩衝區讀取</span><span class="sxs-lookup"><span data-stu-id="18541-166">Read from the vertex buffers</span></span>

<span data-ttu-id="18541-167">頂點緩衝區會將場景物件的三角形資料提供給頂點著色器 (s) 。</span><span class="sxs-lookup"><span data-stu-id="18541-167">The vertex buffer supplies the triangle data for the scene objects to the vertex shader(s).</span></span> <span data-ttu-id="18541-168">如同常數緩衝區，頂點緩衝區結構是在 c + + 程式碼中使用類似的封裝規則來宣告。</span><span class="sxs-lookup"><span data-stu-id="18541-168">As with the constant buffer, the vertex buffer struct is declared in the C++ code, using similar packing rules.</span></span>


```C++
typedef struct _vertexPositionColor
{
    DirectX::XMFLOAT3 pos;
    DirectX::XMFLOAT3 color;
} VertexPositionColor;
```



<span data-ttu-id="18541-169">在 Direct3D 11 中，沒有適用于頂點資料的標準格式。</span><span class="sxs-lookup"><span data-stu-id="18541-169">There is no standard format for vertex data in Direct3D 11.</span></span> <span data-ttu-id="18541-170">相反地，我們會使用描述元來定義自己的頂點資料版面配置;資料欄位會使用 [**D3D11 \_ 輸入 \_ 元素 \_ DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_input_element_desc) 結構的陣列來定義。</span><span class="sxs-lookup"><span data-stu-id="18541-170">Instead, we define our own vertex data layout using a descriptor; the data fields are defined using an array of [**D3D11\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_input_element_desc) structures.</span></span> <span data-ttu-id="18541-171">在這裡，我們會顯示簡單的輸入版面配置，其描述與上述結構相同的頂點格式：</span><span class="sxs-lookup"><span data-stu-id="18541-171">Here, we show a simple input layout that describes the same vertex format as the preceding struct:</span></span>


```C++
D3D11_INPUT_ELEMENT_DESC iaDesc [] =
{
    { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 0, D3D11_INPUT_PER_VERTEX_DATA, 0 },

    { "COLOR", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },
};

hr = device->CreateInputLayout(
    iaDesc,
    ARRAYSIZE(iaDesc),
    bytes,
    bytesRead,
    &m_pInputLayout
    );
```



<span data-ttu-id="18541-172">如果您在修改範例程式碼時，將資料新增至頂點格式，請務必更新輸入版面配置，否則著色器將無法解讀。</span><span class="sxs-lookup"><span data-stu-id="18541-172">If you add data to the vertex format when modifying the example code, be sure to update the input layout as well, or the shader will not be able to interpret it.</span></span> <span data-ttu-id="18541-173">您可以修改頂點配置，如下所示：</span><span class="sxs-lookup"><span data-stu-id="18541-173">You might modify the vertex layout like this:</span></span>


```C++
typedef struct _vertexPositionColorTangent
{
    DirectX::XMFLOAT3 pos;
    DirectX::XMFLOAT3 normal;
    DirectX::XMFLOAT3 tangent;
} VertexPositionColorTangent;
```



<span data-ttu-id="18541-174">在這種情況下，您將修改輸入版面配置定義，如下所示。</span><span class="sxs-lookup"><span data-stu-id="18541-174">In that case, you'd modify the input-layout definition as follows.</span></span>


```C++
D3D11_INPUT_ELEMENT_DESC iaDescExtended[] =
{
    { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 0, D3D11_INPUT_PER_VERTEX_DATA, 0 },

    { "NORMAL", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },

    { "TANGENT", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },
};

hr = device->CreateInputLayout(
    iaDesc,
    ARRAYSIZE(iaDesc),
    bytes,
    bytesRead,
    &m_pInputLayoutExtended
    );
```



<span data-ttu-id="18541-175">每個輸入設定項目定義的前面都會加上字串（例如「位置」或「一般」），這是我們稍早在本主題中討論的語法。</span><span class="sxs-lookup"><span data-stu-id="18541-175">Each of the input-layout element definitions is prefixed with a string, like "POSITION" or "NORMAL"—that is the semantic we discussed earlier in this topic.</span></span> <span data-ttu-id="18541-176">它就像一個控制碼，可協助 GPU 在處理頂點時識別出該元素。</span><span class="sxs-lookup"><span data-stu-id="18541-176">It's like a handle that helps the GPU identify that element when processing the vertex.</span></span> <span data-ttu-id="18541-177">為您的頂點元素選擇常用、有意義的名稱。</span><span class="sxs-lookup"><span data-stu-id="18541-177">Choose common, meaningful names for your vertex elements.</span></span>

<span data-ttu-id="18541-178">就像常數緩衝區一樣，頂點著色器具有連入頂點元素的對應緩衝區定義。</span><span class="sxs-lookup"><span data-stu-id="18541-178">Just as with the constant buffer, the vertex shader has a corresponding buffer definition for incoming vertex elements.</span></span> <span data-ttu-id="18541-179"> (這就是我們在建立輸入配置時提供端點著色器資源參考的原因-Direct3D 會使用著色器的輸入結構來驗證每個頂點的資料版面配置。 ) 請注意，輸入配置定義與這個 HLSL 緩衝區宣告之間的語義相符。</span><span class="sxs-lookup"><span data-stu-id="18541-179">(That's why we provided a reference to the vertex shader resource when creating the input layout - Direct3D validates the per-vertex data layout with the shader's input struct.) Note how the semantics match between the input layout definition and this HLSL buffer declaration.</span></span> <span data-ttu-id="18541-180">不過， `COLOR` 它後面會加上 "0"。</span><span class="sxs-lookup"><span data-stu-id="18541-180">However, `COLOR` has a "0" appended to it.</span></span> <span data-ttu-id="18541-181">如果配置中只宣告一個元素，則不需要新增0，但如果您在 `COLOR` 未來加入宣告更多色彩元素，則最好將它附加。</span><span class="sxs-lookup"><span data-stu-id="18541-181">It isn't necessary to add the 0 if you have only one `COLOR` element declared in the layout, but it's a good practice to append it in case you you choose to add more color elements in the future.</span></span>


```C++
struct VS_INPUT
{
    float3 vPos   : POSITION;
    float3 vColor : COLOR0;
};
```



## <a name="pass-data-between-shaders"></a><span data-ttu-id="18541-182">在著色器之間傳遞資料</span><span class="sxs-lookup"><span data-stu-id="18541-182">Pass data between shaders</span></span>

<span data-ttu-id="18541-183">著色器會在執行時採用輸入類型，並從其主要函數傳回輸出類型。</span><span class="sxs-lookup"><span data-stu-id="18541-183">Shaders take input types and return output types from their main functions upon execution.</span></span> <span data-ttu-id="18541-184">在上一節中定義的頂點著色器中，輸入類型是 VS \_ 輸入結構，而且我們定義了相符的輸入配置和 c + + 結構。</span><span class="sxs-lookup"><span data-stu-id="18541-184">For the vertex shader defined in the previous section, the input type was the VS\_INPUT structure, and we defined a matching input layout and C++ struct.</span></span> <span data-ttu-id="18541-185">此結構的陣列用來在 **CreateCube** 方法中建立頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="18541-185">An array of this struct is used to create a vertex buffer in the **CreateCube** method.</span></span>

<span data-ttu-id="18541-186">頂點著色器會傳回 PS \_ 輸入結構，其至少必須包含4個元件 (float4) 最終頂點位置。</span><span class="sxs-lookup"><span data-stu-id="18541-186">The vertex shader returns a PS\_INPUT structure, which must minimally contain the 4-component (float4) final vertex position.</span></span> <span data-ttu-id="18541-187">這個位置值必須具有系統值語義， `SV_POSITION` 並為其宣告，使 GPU 具有執行下一個繪製步驟所需的資料。</span><span class="sxs-lookup"><span data-stu-id="18541-187">This position value must have the system value semantic, `SV_POSITION`, declared for it so the GPU has the data it needs to perform the next drawing step.</span></span> <span data-ttu-id="18541-188">請注意，頂點著色器輸出和圖元著色器輸入之間沒有1:1 對應;頂點著色器會為每個指定的頂點傳回一個結構，但是圖元著色器會針對每個圖元執行一次。</span><span class="sxs-lookup"><span data-stu-id="18541-188">Notice that there is not a 1:1 correspondence between vertex shader output and pixel shader input; the vertex shader returns one structure for each vertex it is given, but the pixel shader runs once for each pixel.</span></span> <span data-ttu-id="18541-189">這是因為每個頂點的資料會先經過點陣化階段。</span><span class="sxs-lookup"><span data-stu-id="18541-189">That's because the per-vertex data first passes through the rasterization stage.</span></span> <span data-ttu-id="18541-190">這個階段會決定您所繪製幾何的「涵蓋」哪些圖元、計算每個圖元的每個頂點資料，然後針對每個圖元呼叫圖元著色器一次。</span><span class="sxs-lookup"><span data-stu-id="18541-190">This stage decides which pixels "cover" the geometry you're drawing, computes interpolated per-vertex data for each pixel, and then calls the pixel shader once for each of those pixels.</span></span> <span data-ttu-id="18541-191">當您將輸出值進行柵格化時，插補是預設的行為，特別是為了正確處理輸出向量資料 (光向量、每個頂點法線和正切，以及其他) 。</span><span class="sxs-lookup"><span data-stu-id="18541-191">Interpolation is the default behavior when rasterizing output values, and is essential in particular for the correct processing of output vector data (light vectors, per-vertex normals and tangents, and others).</span></span>


```C++
struct PS_INPUT
{
    float4 Position : SV_POSITION;  // interpolated vertex position (system value)
    float4 Color    : COLOR0;       // interpolated diffuse color
};
```



## <a name="review-the-vertex-shader"></a><span data-ttu-id="18541-192">檢查頂點著色器</span><span class="sxs-lookup"><span data-stu-id="18541-192">Review the vertex shader</span></span>

<span data-ttu-id="18541-193">範例頂點著色器非常簡單：採用頂點 (位置和色彩) 、將模型座標中的位置轉換成透視圖投影座標，並將其 (以及轉譯器的色彩) 傳回。</span><span class="sxs-lookup"><span data-stu-id="18541-193">The example vertex shader is very simple: take in a vertex (position and color), transform the position from model coordinates into perspective projected coordinates, and return it (along with the color) to the rasterizer.</span></span> <span data-ttu-id="18541-194">請注意，色彩值會與位置資料直接插入，為每個圖元提供不同的值，即使頂點著色器未對色彩值執行任何計算也是一樣。</span><span class="sxs-lookup"><span data-stu-id="18541-194">Notice that the color value is interpolated right along with the position data, providing a different value for each pixel even though the vertex shader didn't perform any calculations on the color value.</span></span>


```C++
VS_OUTPUT main(VS_INPUT input) // main is the default function name
{
    VS_OUTPUT Output;

    float4 pos = float4(input.vPos, 1.0f);

    // Transform the position from object space to homogeneous projection space
    pos = mul(pos, mWorld);
    pos = mul(pos, View);
    pos = mul(pos, Projection);
    Output.Position = pos;

    // Just pass through the color data
    Output.Color = float4(input.vColor, 1.0f);

    return Output;
}
```



<span data-ttu-id="18541-195">較複雜的端點著色器，例如設定物件頂點以進行 Phong 的陰影，可能看起來更像這樣。</span><span class="sxs-lookup"><span data-stu-id="18541-195">A more complex vertex shader, such as one that sets up an object's vertices for Phong shading, might look more like this.</span></span> <span data-ttu-id="18541-196">在此情況下，我們會利用將向量和法線插到接近美觀表面的事實。</span><span class="sxs-lookup"><span data-stu-id="18541-196">In this case, we're taking advantage of the fact that the vectors and normals are interpolated to approximate a smooth-looking surface.</span></span>

``` syntax
// A constant buffer that stores the three basic column-major matrices for composing geometry.
cbuffer ModelViewProjectionConstantBuffer : register(b0)
{
    matrix model;
    matrix view;
    matrix projection;
};

cbuffer LightConstantBuffer : register(b1)
{
    float4 lightPos;
};

struct VertexShaderInput
{
    float3 pos : POSITION;
    float3 normal : NORMAL;
};

// Per-pixel color data passed through the pixel shader.

struct PixelShaderInput
{
    float4 position : SV_POSITION; 
    float3 outVec : POSITION0;
    float3 outNormal : NORMAL0;
    float3 outLightVec : POSITION1;
};

PixelShaderInput main(VertexShaderInput input)
{
    // Inefficient -- doing this only for instruction. Normally, you would
 // premultiply them on the CPU and place them in the cbuffer.
    matrix mvMatrix = mul(model, view);
    matrix mvpMatrix = mul(mvMatrix, projection);

    PixelShaderInput output;

    float4 pos = float4(input.pos, 1.0f);
    float4 normal = float4(input.normal, 1.0f);
    float4 light = float4(lightPos.xyz, 1.0f);

    // 
    float4 eye = float4(0.0f, 0.0f, -2.0f, 1.0f);

    // Transform the vertex position into projected space.
    output.gl_Position = mul(pos, mvpMatrix);
    output.outNormal = mul(normal, mvMatrix).xyz;
    output.outVec = -(eye - mul(pos, mvMatrix)).xyz;
    output.outLightVec = mul(light, mvMatrix).xyz;

    return output;
}
```

## <a name="review-the-pixel-shader"></a><span data-ttu-id="18541-197">檢查圖元著色器</span><span class="sxs-lookup"><span data-stu-id="18541-197">Review the pixel shader</span></span>

<span data-ttu-id="18541-198">此範例中的這個圖元著色器很可能是您在圖元著色器中可以擁有的最小程式代碼數量。</span><span class="sxs-lookup"><span data-stu-id="18541-198">This pixel shader in this example is quite possibly the absolute minimum amount of code you can have in a pixel shader.</span></span> <span data-ttu-id="18541-199">它會採用在點陣化期間產生的插補圖元色彩資料，並將其傳回做為輸出，然後將它寫入轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="18541-199">It takes the interpolated pixel color data generated during rasterization and returns it as output, where it will be written to a render target.</span></span> <span data-ttu-id="18541-200">乏味！</span><span class="sxs-lookup"><span data-stu-id="18541-200">How boring!</span></span>


```C++
PS_OUTPUT main(PS_INPUT In)
{
    PS_OUTPUT Output;

    Output.RGBColor = In.Color;

    return Output;
}
```



<span data-ttu-id="18541-201">重要的部分是傳回 `SV_TARGET` 值的系統值語義。</span><span class="sxs-lookup"><span data-stu-id="18541-201">The important part is the `SV_TARGET` system-value semantic on the return value.</span></span> <span data-ttu-id="18541-202">它指出輸出會寫入主要轉譯目標，也就是提供給交換鏈的材質緩衝區以供顯示。</span><span class="sxs-lookup"><span data-stu-id="18541-202">It indicates that the output is to be written to the primary render target, which is the texture buffer supplied to the swap chain for display.</span></span> <span data-ttu-id="18541-203">這是圖元著色器的必要項（沒有圖元著色器的色彩資料），Direct3D 沒有任何要顯示的資料！</span><span class="sxs-lookup"><span data-stu-id="18541-203">This is required for pixel shaders - without the color data from the pixel shader, Direct3D wouldn't have anything to display!</span></span>

<span data-ttu-id="18541-204">更複雜的圖元著色器範例可執行 Phong 陰影，如下所示。</span><span class="sxs-lookup"><span data-stu-id="18541-204">An example of a more complex pixel shader to perform Phong shading might look like this.</span></span> <span data-ttu-id="18541-205">由於向量和法線是插補的，因此不需要以每圖元為基礎來計算。</span><span class="sxs-lookup"><span data-stu-id="18541-205">Since the vectors and normals were interpolated, we don't have to compute them on a per-pixel basis.</span></span> <span data-ttu-id="18541-206">不過，我們必須重新正規化它們，因為插補的運作方式;就概念而言，我們必須從頂點 A 方向的方向逐漸「旋轉」至頂點 B 的方向，以維持其長度— wheras 插補會改為在兩個向量端點之間的直線之間剪下。</span><span class="sxs-lookup"><span data-stu-id="18541-206">However, we do have to re-normalize them because of how interpolation works; conceptually, we need to gradually "spin" the vector from direction at vertex A to direction at vertex B, maintaining its length—wheras interpolation instead cuts across a straight line between the two vector endpoints.</span></span>

``` syntax
cbuffer MaterialConstantBuffer : register(b2)
{
    float4 lightColor;
    float4 Ka;
    float4 Kd;
    float4 Ks;
    float4 shininess;
};

struct PixelShaderInput
{
    float4 position : SV_POSITION;
    float3 outVec : POSITION0;
    float3 normal : NORMAL0;
    float3 light : POSITION1;
};

float4 main(PixelShaderInput input) : SV_TARGET
{
    float3 L = normalize(input.light);
    float3 V = normalize(input.outVec);
    float3 R = normalize(reflect(L, input.normal));

    float4 diffuse = Ka + (lightColor * Kd * max(dot(input.normal, L), 0.0f));
    diffuse = saturate(diffuse);

    float4 specular = Ks * pow(max(dot(R, V), 0.0f), shininess.x - 50.0f);
    specular = saturate(specular);

    float4 finalColor = diffuse + specular;

    return finalColor;
}
```

<span data-ttu-id="18541-207">在另一個範例中，圖元著色器會採用自己的常數緩衝區，其中包含燈光和材質資訊。</span><span class="sxs-lookup"><span data-stu-id="18541-207">In another example, the pixel shader takes its own constant buffers that contain light and material information.</span></span> <span data-ttu-id="18541-208">端點著色器中的輸入配置會展開成包含一般資料，而該頂點著色器的輸出應該包含頂點的轉換向量、燈光，以及視圖座標系統中的頂點。</span><span class="sxs-lookup"><span data-stu-id="18541-208">The input layout in the vertex shader would be expanded to include normal data, and the output from that vertex shader is expected to include transformed vectors for the vertex, the light, and the vertex normal in the view coordinate system.</span></span>

<span data-ttu-id="18541-209">如果您的材質緩衝區和取樣器具有指派的暫存器 (**t** 和 **s** 分別) ，您也可以在圖元著色器中存取它們。</span><span class="sxs-lookup"><span data-stu-id="18541-209">If you have texture buffers and samplers with assigned registers (**t** and **s**, respectively), you can access them in the pixel shader also.</span></span>

``` syntax
Texture2D simpleTexture : register(t0);
SamplerState simpleSampler : register(s0);

struct PixelShaderInput
{
    float4 pos : SV_POSITION;
    float3 norm : NORMAL;
    float2 tex : TEXCOORD0;
};

float4 SimplePixelShader(PixelShaderInput input) : SV_TARGET
{
    float3 lightDirection = normalize(float3(1, -1, 0));
    float4 texelColor = simpleTexture.Sample(simpleSampler, input.tex);
    float lightMagnitude = 0.8f * saturate(dot(input.norm, -lightDirection)) + 0.2f;
    return texelColor * lightMagnitude;
}
```

<span data-ttu-id="18541-210">著色器是功能強大的工具，可用來產生像是陰影地圖或雜訊紋理等程式性資源。</span><span class="sxs-lookup"><span data-stu-id="18541-210">Shaders are very powerful tools that can be used to generate procedural resources like shadow maps or noise textures.</span></span> <span data-ttu-id="18541-211">事實上，先進的技術要求您將紋理視為更以抽象方式，而不是視覺元素，但作為緩衝區。</span><span class="sxs-lookup"><span data-stu-id="18541-211">In fact, advanced techniques require that you think of textures more abstractly, not as visual elements but as buffers.</span></span> <span data-ttu-id="18541-212">它們包含高度資訊等資料，或其他可在最終圖元著色器階段中取樣的資料，或是在多階段效果通過時，可在該特定框架中取樣的資料。</span><span class="sxs-lookup"><span data-stu-id="18541-212">They hold data like height information, or other data that can be sampled in the final pixel shader pass or in that particular frame as part of a multi-stage effects pass.</span></span> <span data-ttu-id="18541-213">多取樣是一種功能強大的工具，以及許多新式視覺效果的骨幹。</span><span class="sxs-lookup"><span data-stu-id="18541-213">Multi-sampling is a powerful tool and the backbone of many modern visual effects.</span></span>

## <a name="next-steps"></a><span data-ttu-id="18541-214">下一步</span><span class="sxs-lookup"><span data-stu-id="18541-214">Next steps</span></span>

<span data-ttu-id="18541-215">希望您現在已熟悉 DirectX 11at，並已準備好開始處理您的專案。</span><span class="sxs-lookup"><span data-stu-id="18541-215">Hopefully, you're comfortable with DirectX 11at this point and are ready to start working on your project.</span></span> <span data-ttu-id="18541-216">以下連結可協助您回答使用 DirectX 和 c + + 進行開發時可能遇到的其他問題：</span><span class="sxs-lookup"><span data-stu-id="18541-216">Here are some links to help answer other questions you may have about development with DirectX and C++:</span></span>

-   <span data-ttu-id="18541-217">[開發遊戲](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="18541-217">[Developing games](/previous-versions/windows/apps/hh452744(v=win.10))</span></span>
-   <span data-ttu-id="18541-218">[使用 Visual Studio 工具進行 DirectX 遊戲程式設計](/previous-versions/windows/apps/dn166877(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="18541-218">[Use Visual Studio tools for DirectX game programming](/previous-versions/windows/apps/dn166877(v=win.10))</span></span>
-   <span data-ttu-id="18541-219">[DirectX 遊戲開發和範例逐步解說](/previous-versions/windows/apps/hh465149(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="18541-219">[DirectX game development and sample walkthroughs](/previous-versions/windows/apps/hh465149(v=win.10))</span></span>
-   <span data-ttu-id="18541-220">[其他遊戲程式設計資源](/previous-versions/windows/apps/dn194515(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="18541-220">[Additional game programming resources](/previous-versions/windows/apps/dn194515(v=win.10))</span></span>

## <a name="related-topics"></a><span data-ttu-id="18541-221">相關主題</span><span class="sxs-lookup"><span data-stu-id="18541-221">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18541-222">使用 DirectX 裝置資源</span><span class="sxs-lookup"><span data-stu-id="18541-222">Work with DirectX device resources</span></span>](work-with-dxgi.md)
</dt> <dt>

[<span data-ttu-id="18541-223">瞭解 Direct3D 11 轉譯管線</span><span class="sxs-lookup"><span data-stu-id="18541-223">Understand the Direct3D 11 rendering pipeline</span></span>](understand-the-directx-11-2-graphics-pipeline.md)
</dt> </dl>

 

 
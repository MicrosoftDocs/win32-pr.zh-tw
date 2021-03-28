---
title: 在 Direct3D 9 中使用著色器
description: 在 Direct3D 9 中使用著色器
ms.assetid: 8d8f5124-fbf3-4af5-8399-43ba28aa6eb9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6455b47d24c1c83683ce8b85c48990bb32e221ae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990903"
---
# <a name="using-shaders-in-direct3d-9"></a><span data-ttu-id="9428a-103">在 Direct3D 9 中使用著色器</span><span class="sxs-lookup"><span data-stu-id="9428a-103">Using Shaders in Direct3D 9</span></span>

-   [<span data-ttu-id="9428a-104">針對特定硬體編譯著色器</span><span class="sxs-lookup"><span data-stu-id="9428a-104">Compiling a Shader for Specific Hardware</span></span>](#compiling-a-shader-for-specific-hardware)
-   [<span data-ttu-id="9428a-105">初始化著色器常數</span><span class="sxs-lookup"><span data-stu-id="9428a-105">Initializing Shader Constants</span></span>](#initializing-shader-constants)
-   [<span data-ttu-id="9428a-106">將著色器參數系結至特定的註冊</span><span class="sxs-lookup"><span data-stu-id="9428a-106">Binding a Shader Parameter to a Particular Register</span></span>](#binding-a-shader-parameter-to-a-particular-register)
-   [<span data-ttu-id="9428a-107">呈現可程式化著色器</span><span class="sxs-lookup"><span data-stu-id="9428a-107">Rendering a Programmable Shader</span></span>](#rendering-a-programmable-shader)
-   [<span data-ttu-id="9428a-108">調試著色器</span><span class="sxs-lookup"><span data-stu-id="9428a-108">Debugging Shaders</span></span>](#debugging-shaders)
-   [<span data-ttu-id="9428a-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="9428a-109">Related topics</span></span>](#related-topics)

## <a name="compiling-a-shader-for-specific-hardware"></a><span data-ttu-id="9428a-110">針對特定硬體編譯著色器</span><span class="sxs-lookup"><span data-stu-id="9428a-110">Compiling a Shader for Specific Hardware</span></span>

<span data-ttu-id="9428a-111">第一次將著色器新增至 DirectX 8.0 中的 Microsoft DirectX。</span><span class="sxs-lookup"><span data-stu-id="9428a-111">Shaders were first added to Microsoft DirectX in DirectX 8.0.</span></span> <span data-ttu-id="9428a-112">屆時，已定義數個虛擬著色器機器，每個機器大致對應于前幾個3D 圖形廠商所產生的特定圖形處理器。</span><span class="sxs-lookup"><span data-stu-id="9428a-112">At that time, several virtual shader machines were defined, each roughly corresponding to a particular graphics processor produced by the top 3D graphics vendors.</span></span> <span data-ttu-id="9428a-113">每個虛擬著色器機器都有設計組合語言。</span><span class="sxs-lookup"><span data-stu-id="9428a-113">For each of these virtual shader machines, an assembly language was designed.</span></span> <span data-ttu-id="9428a-114">寫入著色器模型的程式 (名稱與 \_ 1 \_ 1 和 ps \_ 1 \_ 1-ps \_ 1 \_ 4) 相對較短，通常是由開發人員直接以適當的元件語言撰寫。</span><span class="sxs-lookup"><span data-stu-id="9428a-114">Programs written to the shader models (names vs\_1\_1 and ps\_1\_1 - ps\_1\_4) were relatively short and were generally written by developers directly in the appropriate assembly language.</span></span> <span data-ttu-id="9428a-115">應用程式會使用 [**D3DXAssembleShader**](/windows/desktop/direct3d9/d3dxassembleshader) 將這個人類可讀取的元件語言程式碼傳遞至 D3DX 程式庫，並取得著色器的二進位標記法，然後再使用 [**CreateVertexShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvertexshader) 或 [**CreatePixelShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createpixelshader)來傳遞。</span><span class="sxs-lookup"><span data-stu-id="9428a-115">The application would pass this human-readable assembly language code to the D3DX library using [**D3DXAssembleShader**](/windows/desktop/direct3d9/d3dxassembleshader) and get back a binary representation of the shader which would in turn get passed using [**CreateVertexShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvertexshader) or [**CreatePixelShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createpixelshader).</span></span> <span data-ttu-id="9428a-116">如需詳細資訊，請參閱軟體發展工具組 (SDK) 。</span><span class="sxs-lookup"><span data-stu-id="9428a-116">For more detail, see the software development kit (SDK).</span></span>

<span data-ttu-id="9428a-117">Direct3D 9 的情況很類似。</span><span class="sxs-lookup"><span data-stu-id="9428a-117">The situation in Direct3D 9 is similar.</span></span> <span data-ttu-id="9428a-118">應用程式會使用 [**D3DXCompileShader**](/windows/desktop/direct3d9/d3dxcompileshader) 將 HLSL 著色器傳遞給 D3DX，並取得已編譯著色器的二進位標記法，然後使用 [**CreatePixelShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createpixelshader) 或 [**CreateVertexShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvertexshader)將它傳遞給 Microsoft Direct3D。</span><span class="sxs-lookup"><span data-stu-id="9428a-118">An application passes an HLSL shader to D3DX using [**D3DXCompileShader**](/windows/desktop/direct3d9/d3dxcompileshader) and gets back a binary representation of the compiled shader which in turn is passed to Microsoft Direct3D using [**CreatePixelShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createpixelshader) or [**CreateVertexShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvertexshader).</span></span> <span data-ttu-id="9428a-119">執行時間不知道任何關於 HLSL 的作業，只是二進位的元件著色器模型。</span><span class="sxs-lookup"><span data-stu-id="9428a-119">The runtime does not know anything about HLSL, only the binary assembly shader models.</span></span> <span data-ttu-id="9428a-120">這很好用，因為這表示 HLSL 編譯器可以獨立于 Direct3D 執行時間進行更新。</span><span class="sxs-lookup"><span data-stu-id="9428a-120">This is nice because it means that the HLSL compiler can be updated independent of the Direct3D runtime.</span></span> <span data-ttu-id="9428a-121">您也可以使用 [fxc.exe](/windows/desktop/direct3dtools/fxc)，離線編譯著色器。</span><span class="sxs-lookup"><span data-stu-id="9428a-121">You can also compile shaders offline using [fxc](/windows/desktop/direct3dtools/fxc).</span></span>

<span data-ttu-id="9428a-122">除了開發 HLSL 編譯器之外，Direct3D 9 也引進了元件層級的著色器模型，以公開最新一代圖形硬體的功能。</span><span class="sxs-lookup"><span data-stu-id="9428a-122">In addition to the development of the HLSL compiler, Direct3D 9 also introduced the assembly-level shader models to expose the functionality of the latest generation of graphics hardware.</span></span> <span data-ttu-id="9428a-123">應用程式開發人員可以在元件中使用這些新模型 (vs \_ 2 \_ 0、vs \_ 3 \_ 0、ps \_ 2 \_ 0、ps \_ 3 \_ 0) ，但我們預期大部分的開發人員都可以移至 HLSL 進行著色器開發。</span><span class="sxs-lookup"><span data-stu-id="9428a-123">Application developers can work in assembly for these new models (vs\_2\_0, vs\_3\_0, ps\_2\_0, ps\_3\_0) but we expect most developers to move to HLSL for shader development.</span></span>

<span data-ttu-id="9428a-124">當然，撰寫 HLSL 程式以表示特定網底演算法的能力並不會自動讓它在任何指定的硬體上執行。</span><span class="sxs-lookup"><span data-stu-id="9428a-124">Of course, the ability to write an HLSL program to express a particular shading algorithm does not automatically enable it to run on any given hardware.</span></span> <span data-ttu-id="9428a-125">應用程式會呼叫 D3DX，使用 [**D3DXCompileShader**](/windows/desktop/direct3d9/d3dxcompileshader)將著色器編譯成二進位元件程式碼。</span><span class="sxs-lookup"><span data-stu-id="9428a-125">An application calls D3DX to compile a shader into binary assembly code with [**D3DXCompileShader**](/windows/desktop/direct3d9/d3dxcompileshader).</span></span> <span data-ttu-id="9428a-126">這個進入點的其中一個限制是參數，其定義 (或編譯目標的元件層級模型，) HLSL 編譯器應該使用這些模型來表示最後的著色器程式碼。</span><span class="sxs-lookup"><span data-stu-id="9428a-126">One of the limitations with this entry point is a parameter that defines which of the assembly-level models (or compilation targets) the HLSL compiler should use to express the final shader code.</span></span> <span data-ttu-id="9428a-127">如果應用程式在執行時間執行 HLSL 著色器編譯 (而不是編譯時間或離線) ，則應用程式可以檢查 Direct3D 裝置的功能，並選取要比對的編譯目標。</span><span class="sxs-lookup"><span data-stu-id="9428a-127">If an application is doing HLSL shader compilation at run time (as opposed to compile time or offline), the application could examine the capabilities of the Direct3D device and select the compilation target to match.</span></span> <span data-ttu-id="9428a-128">如果 HLSL 著色器中表示的演算法太複雜而無法在選取的編譯目標上執行，編譯將會失敗。</span><span class="sxs-lookup"><span data-stu-id="9428a-128">If the algorithm expressed in the HLSL shader is too complex to execute on the selected compilation target, compilation will fail.</span></span> <span data-ttu-id="9428a-129">這表示，雖然 HLSL 對著色器開發有很大的好處，但它並不能讓開發人員從將遊戲交付給具有不同功能之圖形裝置的目標物件。</span><span class="sxs-lookup"><span data-stu-id="9428a-129">This means that while HLSL is a huge benefit to shader development, it does not free developers from the realities of shipping games to a target audience with graphics devices of varying capabilities.</span></span> <span data-ttu-id="9428a-130">作為遊戲開發人員，您仍然必須管理視覺效果的分層式方法;這表示為更多功能的圖形卡片撰寫更好的著色器，並為較舊的卡片撰寫更基本的版本。</span><span class="sxs-lookup"><span data-stu-id="9428a-130">As a game developer, you still have to manage a tiered approach to your visuals; this means writing better shaders for more capable graphics cards and writing more basic versions for older cards.</span></span> <span data-ttu-id="9428a-131">不過，有了妥善撰寫的 HLSL，就可以大幅分階段減緩這種負擔。</span><span class="sxs-lookup"><span data-stu-id="9428a-131">With well written HLSL, however, this burden can be eased significantly.</span></span>

<span data-ttu-id="9428a-132">許多開發人員會在應用程式載入時間或第一次使用時，選擇在客戶的電腦上使用 D3DX 編譯 HLSL 著色器，而不是在出貨之前，將其著色器從 HLSL 編譯成二進位程式碼。</span><span class="sxs-lookup"><span data-stu-id="9428a-132">Rather than compile HLSL shaders using D3DX on the customer's machine at application load time or on first use, many developers choose to compile their shader from HLSL to binary assembly code before they even ship.</span></span> <span data-ttu-id="9428a-133">這會讓其 HLSL 的原始程式碼遠離窺探的眼睛，也可確保其應用程式執行的所有著色器都已通過其內部品質保證程式。</span><span class="sxs-lookup"><span data-stu-id="9428a-133">This keeps their HLSL source code away from prying eyes and also ensures that all the shaders their application will ever run have gone through their internal quality assurance process.</span></span> <span data-ttu-id="9428a-134">離線編譯著色器的方便公用程式是 [fxc.exe](/windows/desktop/direct3dtools/fxc)。</span><span class="sxs-lookup"><span data-stu-id="9428a-134">A convenient utility for compiling shaders offline is [fxc](/windows/desktop/direct3dtools/fxc).</span></span> <span data-ttu-id="9428a-135">此工具有許多選項，可讓您用來編譯指定之編譯目標的程式碼。</span><span class="sxs-lookup"><span data-stu-id="9428a-135">This tool has a number of options that you can use to compile code for the specified compile target.</span></span> <span data-ttu-id="9428a-136">如果您想要將您的著色器優化，或通常會在更詳細的層級上瞭解虛擬著色器電腦的功能，在開發期間，將拆解的輸出視為非常教育。</span><span class="sxs-lookup"><span data-stu-id="9428a-136">Studying the disassembled output can be very educational during development if you want to optimize your shaders or just generally get to know the virtual shader machine's capabilities at a more detailed level.</span></span> <span data-ttu-id="9428a-137">以下摘要說明這些選項：</span><span class="sxs-lookup"><span data-stu-id="9428a-137">These options are summarized below:</span></span>

## <a name="initializing-shader-constants"></a><span data-ttu-id="9428a-138">初始化著色器常數</span><span class="sxs-lookup"><span data-stu-id="9428a-138">Initializing Shader Constants</span></span>

<span data-ttu-id="9428a-139">著色器常數包含在常數資料表中。</span><span class="sxs-lookup"><span data-stu-id="9428a-139">Shader constants are contained in the constant table.</span></span> <span data-ttu-id="9428a-140">您可以使用 [**ID3DXConstantTable**](/windows/desktop/direct3d9/id3dxconstanttable) 介面來存取此。</span><span class="sxs-lookup"><span data-stu-id="9428a-140">This can be accessed with the [**ID3DXConstantTable**](/windows/desktop/direct3d9/id3dxconstanttable) interface.</span></span> <span data-ttu-id="9428a-141">全域著色器變數可以在著色器程式碼中初始化。</span><span class="sxs-lookup"><span data-stu-id="9428a-141">Global shader variables can be initialized in shader code.</span></span> <span data-ttu-id="9428a-142">這些會藉由呼叫 [**SetDefaults**](/windows/desktop/direct3d9/id3dxconstanttable--setdefaults)在執行時間初始化。</span><span class="sxs-lookup"><span data-stu-id="9428a-142">These are initialized at run time by calling [**SetDefaults**](/windows/desktop/direct3d9/id3dxconstanttable--setdefaults).</span></span>

## <a name="binding-a-shader-parameter-to-a-particular-register"></a><span data-ttu-id="9428a-143">將著色器參數系結至特定的註冊</span><span class="sxs-lookup"><span data-stu-id="9428a-143">Binding a Shader Parameter to a Particular Register</span></span>

<span data-ttu-id="9428a-144">編譯器會自動將暫存器指派給全域變數。</span><span class="sxs-lookup"><span data-stu-id="9428a-144">The compiler will automatically assign registers to global variables.</span></span> <span data-ttu-id="9428a-145">編譯器會將環境指派給取樣器 register s0、SparkleNoise 至取樣器 register s1，以及 k \_ s 到常數登錄 c0 (假設尚未針對下列三個全域變數指派) 的其他取樣器或常數暫存器：</span><span class="sxs-lookup"><span data-stu-id="9428a-145">The compiler would assign Environment to sampler register s0, SparkleNoise to sampler register s1, and k\_s to constant register c0 (assuming no other sampler or constant registers were already assigned) for the following three global variables:</span></span>


```
sampler Environment;
sampler SparkleNoise;
float4 k_s;
```



<span data-ttu-id="9428a-146">您也可以將變數系結至特定的註冊。</span><span class="sxs-lookup"><span data-stu-id="9428a-146">It is also possible to bind variables to a specific register.</span></span> <span data-ttu-id="9428a-147">若要強制編譯器指派給特定的註冊，請使用下列語法：</span><span class="sxs-lookup"><span data-stu-id="9428a-147">To force the compiler to assign to a particular register, use the following syntax:</span></span>


```
register(RegisterName)
```



<span data-ttu-id="9428a-148">其中 register 是特定暫存器的名稱。</span><span class="sxs-lookup"><span data-stu-id="9428a-148">where RegisterName is the name of the specific register.</span></span> <span data-ttu-id="9428a-149">下列範例示範特定的暫存器指派語法，其中取樣器環境會系結至取樣器 register s1、SparkleNoise 會系結至取樣器 register s0，而 k s 將會系結 \_ 至常數暫存器 c12：</span><span class="sxs-lookup"><span data-stu-id="9428a-149">The following examples demonstrate the specific register assignment syntax, where the sampler Environment will be bound to sampler register s1, SparkleNoise will be bound to sampler register s0, and k\_s will be bound to constant register c12:</span></span>


```
sampler Environment : register(s1);
sampler SparkleNoise : register(s0);
float4 k_s : register(c12);
```



## <a name="rendering-a-programmable-shader"></a><span data-ttu-id="9428a-150">呈現可程式化著色器</span><span class="sxs-lookup"><span data-stu-id="9428a-150">Rendering a Programmable Shader</span></span>

<span data-ttu-id="9428a-151">著色器的呈現方式是在裝置中設定目前的著色器、初始化著色器常數、告知裝置有不同輸入資料的來源，最後呈現基本專案。</span><span class="sxs-lookup"><span data-stu-id="9428a-151">A shader is rendered by setting the current shader in the device, initializing the shader constants, telling the device where the varying input data is coming from, and finally rendering the primitives.</span></span> <span data-ttu-id="9428a-152">每個都可以藉由分別呼叫下列方法來完成：</span><span class="sxs-lookup"><span data-stu-id="9428a-152">Each of these can be accomplished by calling the following methods respectively:</span></span>

-   [<span data-ttu-id="9428a-153">**SetVertexShader**</span><span class="sxs-lookup"><span data-stu-id="9428a-153">**SetVertexShader**</span></span>](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader)
-   [<span data-ttu-id="9428a-154">**SetVertexShaderConstantF**</span><span class="sxs-lookup"><span data-stu-id="9428a-154">**SetVertexShaderConstantF**</span></span>](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf)
-   [<span data-ttu-id="9428a-155">**SetStreamSource**</span><span class="sxs-lookup"><span data-stu-id="9428a-155">**SetStreamSource**</span></span>](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource)
-   [<span data-ttu-id="9428a-156">**DrawPrimitive**</span><span class="sxs-lookup"><span data-stu-id="9428a-156">**DrawPrimitive**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawprimitive)

## <a name="debugging-shaders"></a><span data-ttu-id="9428a-157">調試著色器</span><span class="sxs-lookup"><span data-stu-id="9428a-157">Debugging Shaders</span></span>

<span data-ttu-id="9428a-158">適用于 Microsoft Visual Studio .NET 的 DirectX 擴充功能可在 Visual Studio .NET 整合式開發環境中，提供完全整合的 HLSL 偵錯工具 (IDE) 。</span><span class="sxs-lookup"><span data-stu-id="9428a-158">The DirectX extension for Microsoft Visual Studio .NET is provides a fully integrated HLSL debugger within the Visual Studio .NET Integrated Development Environment (IDE).</span></span> <span data-ttu-id="9428a-159">為了準備著色器的偵錯工具，您必須在您的電腦上安裝正確的工具 (請參閱 [Visual Studio (Direct3D 9) ) 中的偵錯工具著色 ](dx-graphics-hlsl-debug-visual-studio.md) 器。</span><span class="sxs-lookup"><span data-stu-id="9428a-159">In order to prepare for shader debugging, you must install the right tools on your machine (see [Debugging Shaders in Visual Studio (Direct3D 9)](dx-graphics-hlsl-debug-visual-studio.md)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9428a-160">相關主題</span><span class="sxs-lookup"><span data-stu-id="9428a-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9428a-161">HLSL 的程式設計指南</span><span class="sxs-lookup"><span data-stu-id="9428a-161">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 
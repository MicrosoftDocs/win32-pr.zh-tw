---
title: 使用 Direct3D 10 中的著色器
description: 使用 Direct3D 10 中的著色器
ms.assetid: cff6f901-cb9b-44d5-a75b-9a4029a37215
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c0d6212851e4603aac4db7ec85dd20714dc87774
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826286"
---
# <a name="using-shaders-in-direct3d-10"></a><span data-ttu-id="2a437-103">使用 Direct3D 10 中的著色器</span><span class="sxs-lookup"><span data-stu-id="2a437-103">Using Shaders in Direct3D 10</span></span>

<span data-ttu-id="2a437-104">管線有三個著色器階段，而每一個都是使用 HLSL 著色器進行程式設計。</span><span class="sxs-lookup"><span data-stu-id="2a437-104">The pipeline has three shader stages and each one is programmed with an HLSL shader.</span></span> <span data-ttu-id="2a437-105">所有 Direct3D 10 著色器都會以 HLSL 撰寫，並以著色器模型4為目標。</span><span class="sxs-lookup"><span data-stu-id="2a437-105">All Direct3D 10 shaders are written in HLSL, targeting shader model 4.</span></span>


<span data-ttu-id="2a437-106">Direct3D 9 與 Direct3D 10 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="2a437-106">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="2a437-107">與可使用中繼元件語言撰寫的 Direct3D 9 著色器模型不同，著色器模型4.0 著色器只會在 HLSL 中撰寫。</span><span class="sxs-lookup"><span data-stu-id="2a437-107">Unlike Direct3D 9 shader models which could be authored in an intermediate assembly language, shader model 4.0 shaders are only authored in HLSL.</span></span> <span data-ttu-id="2a437-108">仍支援將著色器離線編譯成裝置可耗用的位元組程式碼，並建議用於大部分的案例。</span><span class="sxs-lookup"><span data-stu-id="2a437-108">Offline compilation of shaders into device-consumable bytecode is still supported, and recommended for most scenarios.</span></span>



 

<span data-ttu-id="2a437-109">這個範例只會使用頂點著色器。</span><span class="sxs-lookup"><span data-stu-id="2a437-109">This example uses only a vertex shader.</span></span> <span data-ttu-id="2a437-110">由於所有著色器都是從通用著色器核心建立的，因此學習如何使用頂點著色器非常類似于使用幾何或圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="2a437-110">Because all shaders are built from the common shader core, learning how to use a vertex shader is very similar to using a geometry or pixel shader.</span></span>

<span data-ttu-id="2a437-111">一旦您撰寫了 HLSL 著色器 (這個範例會使用頂點著色器 HLSLWithoutFX. vsh) ，您必須為將使用它的特定管線階段做好準備。</span><span class="sxs-lookup"><span data-stu-id="2a437-111">Once you have authored an HLSL shader (this example uses the vertex shader HLSLWithoutFX.vsh), you will need to prepare it for the particular pipeline stage that will use it.</span></span> <span data-ttu-id="2a437-112">若要這樣做，您需要：</span><span class="sxs-lookup"><span data-stu-id="2a437-112">To do this you need to:</span></span>

-   [<span data-ttu-id="2a437-113">編譯著色器</span><span class="sxs-lookup"><span data-stu-id="2a437-113">Compile a Shader</span></span>](#compile-a-shader)
-   [<span data-ttu-id="2a437-114">建立著色器物件</span><span class="sxs-lookup"><span data-stu-id="2a437-114">Create a Shader Object</span></span>](#create-a-shader-object)
-   [<span data-ttu-id="2a437-115">設定著色器物件</span><span class="sxs-lookup"><span data-stu-id="2a437-115">Set the Shader Object</span></span>](#set-the-shader-object)
-   [<span data-ttu-id="2a437-116">針對所有3個著色器階段重複</span><span class="sxs-lookup"><span data-stu-id="2a437-116">Repeat for all 3 Shader Stages</span></span>](#repeat-for-all-3-shader-stages)

<span data-ttu-id="2a437-117">這些步驟必須針對管線中的每個著色器重複執行。</span><span class="sxs-lookup"><span data-stu-id="2a437-117">These steps need to be repeated for each shader in the pipeline.</span></span>

## <a name="compile-a-shader"></a><span data-ttu-id="2a437-118">編譯著色器</span><span class="sxs-lookup"><span data-stu-id="2a437-118">Compile a Shader</span></span>

<span data-ttu-id="2a437-119">第一個步驟是編譯著色器，以檢查您是否已正確編碼 HLSL 語句。</span><span class="sxs-lookup"><span data-stu-id="2a437-119">The first step is to compile the shader, to check to see that you have coded the HLSL statements correctly.</span></span> <span data-ttu-id="2a437-120">這是藉由呼叫 D3D10CompileShader 並提供數個參數來完成，如下所示：</span><span class="sxs-lookup"><span data-stu-id="2a437-120">This is done by calling D3D10CompileShader and supplying it with several parameters as shown here:</span></span>


```
    IPD3D10Blob * pBlob;
    
        
    // Compile the vertex shader from the file
    D3D10CompileShader( strPath, strlen( strPath ), "HLSLWithoutFX.vsh", 
        NULL, NULL, "Ripple", "vs_4_0", dwShaderFlags, &pBlob, NULL );
```



<span data-ttu-id="2a437-121">此函數會採用下列參數：</span><span class="sxs-lookup"><span data-stu-id="2a437-121">This function takes the following parameters:</span></span>

-   <span data-ttu-id="2a437-122">檔案名 ( 的檔案名，以及包含著色器的位元組 ) 長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2a437-122">The name of the file ( and length of the name string in bytes ) that contains the shader.</span></span> <span data-ttu-id="2a437-123">此範例只會在 HLSLWithoutFX 檔案中使用頂點著色器 (，其中副檔名是頂點著色器) 的縮寫。</span><span class="sxs-lookup"><span data-stu-id="2a437-123">This example uses a vertex shader only (in the file HLSLWithoutFX.vsh file where the file extension .vsh is an abbreviation for vertex shader).</span></span>
-   <span data-ttu-id="2a437-124">著色器函數名稱。</span><span class="sxs-lookup"><span data-stu-id="2a437-124">The shader function name.</span></span> <span data-ttu-id="2a437-125">此範例會從 Ripple 函式編譯頂點著色器，此函式會採用單一輸入，並傳回輸出結構 (函式是來自 HLSLWithoutFX 範例) ：</span><span class="sxs-lookup"><span data-stu-id="2a437-125">This example compiles a vertex shader from the Ripple function which takes a single input and returns an output struct (the function is from the HLSLWithoutFX sample):</span></span>
    ```
    VS_OUTPUT Ripple( in float2 vPosition : POSITION )
    ```

    

-   <span data-ttu-id="2a437-126">著色器所使用之所有宏的指標。</span><span class="sxs-lookup"><span data-stu-id="2a437-126">A pointer to all macros used by the shader.</span></span> <span data-ttu-id="2a437-127">使用 D3D10 \_ 著色器 \_ 宏可協助定義您的宏; 只要建立包含所有宏 (名稱的名稱字串，其中每個名稱都以空格分隔) 和每個宏主體 (的定義字串（以空格分隔）) 。</span><span class="sxs-lookup"><span data-stu-id="2a437-127">Use D3D10\_SHADER\_MACRO to help define your macros; simply create a name string that contains all the macro names (with each name separated by a space) and a definition string (with each macro body separated by a space).</span></span> <span data-ttu-id="2a437-128">這兩個字串都必須以 Null 結束。</span><span class="sxs-lookup"><span data-stu-id="2a437-128">Both strings need to be NULL terminated.</span></span>
-   <span data-ttu-id="2a437-129">您需要包含的任何其他檔案的指標，以使您的著色器進行編譯。</span><span class="sxs-lookup"><span data-stu-id="2a437-129">A pointer to any other files that you need included to get your shaders to compile.</span></span> <span data-ttu-id="2a437-130">這會使用具有兩個使用者執行方法的 ID3D10Include 介面：開啟和關閉。</span><span class="sxs-lookup"><span data-stu-id="2a437-130">This uses the ID3D10Include interface which has two user-implemented methods: Open and Close.</span></span> <span data-ttu-id="2a437-131">若要進行這項工作，您必須執行開放式和 Close 方法的主體;在 Open 方法中，新增您要用來開啟所需檔案的程式碼，在 Close 函式中，新增程式碼以在完成這些檔案時加以關閉。</span><span class="sxs-lookup"><span data-stu-id="2a437-131">To make this work, you will need to implement the body of the Open and Close methods; in the Open method add the code you would use to open whatever include files you want, in the Close function add the code to close the files when you are done with them.</span></span>
-   <span data-ttu-id="2a437-132">要編譯的著色器函式名稱。</span><span class="sxs-lookup"><span data-stu-id="2a437-132">The name of the shader function to compile.</span></span> <span data-ttu-id="2a437-133">此著色器會編譯 Ripple 函數。</span><span class="sxs-lookup"><span data-stu-id="2a437-133">This shader compiles the Ripple function.</span></span>
-   <span data-ttu-id="2a437-134">編譯時要設為目標的著色器設定檔。</span><span class="sxs-lookup"><span data-stu-id="2a437-134">The shader profile to target when compiling.</span></span> <span data-ttu-id="2a437-135">由於您可以將函式編譯成頂點、幾何或圖元著色器，因此設定檔會告知編譯器要將哪一種著色器類型以及要比較程式碼的著色器模型。</span><span class="sxs-lookup"><span data-stu-id="2a437-135">Since you can compile a function into a vertex, geometry, or pixel shader, the profile tells the compiler which type of shader and which shader model to compare the code against.</span></span>
-   <span data-ttu-id="2a437-136">著色器編譯器旗標。</span><span class="sxs-lookup"><span data-stu-id="2a437-136">Shader compiler flags.</span></span> <span data-ttu-id="2a437-137">這些旗標會告訴編譯器要將哪些資訊放入編譯的輸出，以及您想要如何優化輸出程式碼：速度、偵錯工具等。如需可用旗標的清單，請參閱 [效果常數 (Direct3D 10) ](/windows/desktop/direct3d10/d3d10-graphics-reference-effect-constants) 。</span><span class="sxs-lookup"><span data-stu-id="2a437-137">These flags tell the compiler what information to put into the compiled output and how you want the output code optimized: for speed, for debug, etc. See [Effect Constants (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-reference-effect-constants) for a listing of the available flags.</span></span> <span data-ttu-id="2a437-138">此範例包含一些程式碼，您可以使用這些程式碼來設定專案的編譯器旗標值，這主要是您是否要產生偵錯工具資訊的問題。</span><span class="sxs-lookup"><span data-stu-id="2a437-138">The sample contains some code you can use to set the compiler flag values for your project - this is mainly a question of whether or not you want to generate debug information.</span></span>
-   <span data-ttu-id="2a437-139">緩衝區的指標，其中包含已編譯的著色器程式碼。</span><span class="sxs-lookup"><span data-stu-id="2a437-139">A pointer to the buffer that contains the compiled shader code.</span></span> <span data-ttu-id="2a437-140">緩衝區也包含編譯器旗標所要求的任何內嵌的 debug 錯和符號表資訊。</span><span class="sxs-lookup"><span data-stu-id="2a437-140">The buffer also contains any embedded debug and symbol table information requested by the compiler flags.</span></span>
-   <span data-ttu-id="2a437-141">包含在編譯期間遇到之錯誤和警告清單的緩衝區指標，如果您在編譯著色器時執行偵錯工具，就會在偵錯工具輸出中看到相同的訊息。</span><span class="sxs-lookup"><span data-stu-id="2a437-141">A pointer to a buffer that contains a listing of errors and warnings that were encountered during the compile, which are the same messages you would see in the debug output if you were running the debugger while compiling the shader.</span></span> <span data-ttu-id="2a437-142">如果您不想要傳回給緩衝區的錯誤，則 **Null** 是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="2a437-142">**NULL** is an acceptable value when you don't want the errors returned to a buffer.</span></span>

<span data-ttu-id="2a437-143">如果著色器編譯成功，則會以 ID3D10Blob 介面傳回著色器程式碼的指標。</span><span class="sxs-lookup"><span data-stu-id="2a437-143">If the shader compiles successfully, a pointer to the shader code is returned as a ID3D10Blob interface.</span></span> <span data-ttu-id="2a437-144">因為指標是由 DWORD 陣列所組成的記憶體位置，所以稱為 Blob 介面。</span><span class="sxs-lookup"><span data-stu-id="2a437-144">It is called the Blob interface because the pointer is to a location in memory that is made up of an array of DWORD's.</span></span> <span data-ttu-id="2a437-145">系統會提供介面，讓您可以在下一個步驟中取得所需的已編譯著色器指標。</span><span class="sxs-lookup"><span data-stu-id="2a437-145">The interface is provided so that you can get a pointer to the compiled shader which you will need in the next step.</span></span>

<span data-ttu-id="2a437-146">自2006年12月起的 SDK 起，DirectX 10 HLSL 編譯器現在是 DirectX 9 和 DirectX 10 中的預設編譯器。</span><span class="sxs-lookup"><span data-stu-id="2a437-146">Beginning with the December 2006 SDK, the DirectX 10 HLSL compiler is now the default compiler in both DirectX 9 and DirectX 10.</span></span> <span data-ttu-id="2a437-147">請參閱 [效果-編譯器工具](/windows/desktop/direct3dtools/fxc) 以取得詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2a437-147">See [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) for details.</span></span>

### <a name="get-a-pointer-to-a-compiled-shader"></a><span data-ttu-id="2a437-148">取得已編譯著色器的指標</span><span class="sxs-lookup"><span data-stu-id="2a437-148">Get a Pointer to a Compiled Shader</span></span>

<span data-ttu-id="2a437-149">數個 API 方法需要已編譯著色器的指標。</span><span class="sxs-lookup"><span data-stu-id="2a437-149">Several API methods require a pointer to a compiled shader.</span></span> <span data-ttu-id="2a437-150">這個引數通常稱為 *pShaderBytecode* ，因為它指向以位元組碼序清單示的已編譯著色器。</span><span class="sxs-lookup"><span data-stu-id="2a437-150">This argument is usually called *pShaderBytecode* because it points to a compiled shader represented as a sequence of byte codes.</span></span> <span data-ttu-id="2a437-151">若要取得已編譯之著色器的指標，請先呼叫 [**D3D10CompileShader**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10compileshader) 或類似的函式來編譯著色器。</span><span class="sxs-lookup"><span data-stu-id="2a437-151">To get a pointer to a compiled shader, first compile the shader by calling [**D3D10CompileShader**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10compileshader) or a similar function.</span></span> <span data-ttu-id="2a437-152">如果編譯成功，則會在 [**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob) 介面中傳回已編譯的著色器。</span><span class="sxs-lookup"><span data-stu-id="2a437-152">If compilation is successful, the compiled shader is returned in an [**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob) interface.</span></span> <span data-ttu-id="2a437-153">最後，使用 [**GetBufferPointer**](/windows/desktop/api/d3dcommon/nf-d3dcommon-id3d10blob-getbufferpointer) 方法來傳回指標。</span><span class="sxs-lookup"><span data-stu-id="2a437-153">Finally, use the [**GetBufferPointer**](/windows/desktop/api/d3dcommon/nf-d3dcommon-id3d10blob-getbufferpointer) method to return the pointer.</span></span>

## <a name="create-a-shader-object"></a><span data-ttu-id="2a437-154">建立著色器物件</span><span class="sxs-lookup"><span data-stu-id="2a437-154">Create a Shader Object</span></span>

<span data-ttu-id="2a437-155">編譯著色器之後，請呼叫 CreateVertexShader 來建立著色器物件：</span><span class="sxs-lookup"><span data-stu-id="2a437-155">Once the shader is compiled, call CreateVertexShader to create the shader object:</span></span>


```
    ID3D10VertexShader ** ppVertexShader
    ID3D10Blob pBlob;


    // Create the vertex shader
    hr = pd3dDevice->CreateVertexShader( (DWORD*)pBlob->GetBufferPointer(),
        pBlob->GetBufferSize(), &ppVertexShader );

    // Release the pointer to the compiled shader once you are done with it
    pBlob->Release();
```



<span data-ttu-id="2a437-156">若要建立著色器物件，請將已編譯的著色器指標傳遞至 CreateVertexShader。</span><span class="sxs-lookup"><span data-stu-id="2a437-156">To create the shader object, pass the pointer to the compiled shader into CreateVertexShader.</span></span> <span data-ttu-id="2a437-157">因為您必須先成功編譯著色器，否則除非您的電腦上有記憶體問題，否則此呼叫幾乎當然會通過。</span><span class="sxs-lookup"><span data-stu-id="2a437-157">Since you had to successfully compile the shader first, this call will almost certainly pass, unless you have a memory problem on your machine.</span></span>

<span data-ttu-id="2a437-158">您可以根據自己的需要建立任意數量的著色器物件，並只保留其指標。</span><span class="sxs-lookup"><span data-stu-id="2a437-158">You can create as many shader objects as you like and simply keep pointers to them.</span></span> <span data-ttu-id="2a437-159">這項相同的機制適用于幾何和圖元著色器，假設您符合著色器設定檔 (當您在呼叫 create 方法) 時，)  (的介面名稱。</span><span class="sxs-lookup"><span data-stu-id="2a437-159">This same mechanism works for geometry and pixel shaders assuming you match the shader profiles (when you call the compile method) to the interface names (when you call the create method).</span></span>

## <a name="set-the-shader-object"></a><span data-ttu-id="2a437-160">設定著色器物件</span><span class="sxs-lookup"><span data-stu-id="2a437-160">Set the Shader Object</span></span>

<span data-ttu-id="2a437-161">最後一個步驟是將著色器設定為管線階段。</span><span class="sxs-lookup"><span data-stu-id="2a437-161">The last step is set the shader to the pipeline stage.</span></span> <span data-ttu-id="2a437-162">因為管線中有三個著色器階段，所以您需要進行三個 API 呼叫，每個階段各一個。</span><span class="sxs-lookup"><span data-stu-id="2a437-162">Since there are three shader stages in the pipeline, you will need to make three API calls, one for each stage.</span></span>


```
    // Set a vertex shader
    pd3dDevice->VSSetShader( g_pVS10 );
```



<span data-ttu-id="2a437-163">對 VSSetShader 的呼叫會將指標移至在步驟1中建立的頂點著色器。</span><span class="sxs-lookup"><span data-stu-id="2a437-163">The call to VSSetShader takes the pointer to the vertex shader created in step 1.</span></span> <span data-ttu-id="2a437-164">這會設定裝置中的著色器。</span><span class="sxs-lookup"><span data-stu-id="2a437-164">This sets the shader in the device.</span></span> <span data-ttu-id="2a437-165">端點著色器階段現在會以其頂點著色器程式碼進行初始化，剩下的就是初始化任何著色器變數。</span><span class="sxs-lookup"><span data-stu-id="2a437-165">The vertex shader stage is now initialized with its vertex shader code, all that remains is initializing any shader variables.</span></span>

## <a name="repeat-for-all-3-shader-stages"></a><span data-ttu-id="2a437-166">針對所有3個著色器階段重複</span><span class="sxs-lookup"><span data-stu-id="2a437-166">Repeat for all 3 Shader Stages</span></span>

<span data-ttu-id="2a437-167">重複執行這組相同的步驟，以建立任何頂點或圖元著色器，或甚至是輸出至圖元著色器的幾何著色器。</span><span class="sxs-lookup"><span data-stu-id="2a437-167">Repeat these same set of steps to build any vertex or pixel shader or even a geometry shader that outputs to the pixel shader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a437-168">[相關主題]</span><span class="sxs-lookup"><span data-stu-id="2a437-168">Related Topics</span></span>

[<span data-ttu-id="2a437-169">編譯著色器</span><span class="sxs-lookup"><span data-stu-id="2a437-169">Compiling Shaders</span></span>](dx-graphics-hlsl-part1.md)


## <a name="related-topics"></a><span data-ttu-id="2a437-170">相關主題</span><span class="sxs-lookup"><span data-stu-id="2a437-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a437-171">HLSL 的程式設計指南</span><span class="sxs-lookup"><span data-stu-id="2a437-171">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 


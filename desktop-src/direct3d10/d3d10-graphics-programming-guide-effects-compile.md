---
description: 一旦撰寫好效果之後，第一個步驟就是編譯器代碼以檢查語法問題。
ms.assetid: b8d8a0b7-b520-44e4-8691-6eb46202c092
title: 編譯效果 (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab6183f2f71b07c482fa24efc4f9fed199216d75
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187653"
---
# <a name="compile-an-effect-direct3d-10"></a><span data-ttu-id="4adaa-103">編譯效果 (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="4adaa-103">Compile an Effect (Direct3D 10)</span></span>

<span data-ttu-id="4adaa-104">一旦撰寫好效果之後，第一個步驟就是編譯器代碼以檢查語法問題。</span><span class="sxs-lookup"><span data-stu-id="4adaa-104">Once an effect has been authored, the first step is to compile the code to check for syntax problems.</span></span> <span data-ttu-id="4adaa-105">這是藉由呼叫其中一個編譯 Api 來完成， (例如 D3DX10CompileEffectFromFile、D3DX10CompileEffectFromResource、D3DX10CompileEffectFromMemory) 。</span><span class="sxs-lookup"><span data-stu-id="4adaa-105">This is done by calling one of the compile APIs (like D3DX10CompileEffectFromFile, D3DX10CompileEffectFromResource, D3DX10CompileEffectFromMemory).</span></span> <span data-ttu-id="4adaa-106">這些 API 會叫用效果編譯器 fxc.exe 編譯器用來編譯 HLSL 程式碼。</span><span class="sxs-lookup"><span data-stu-id="4adaa-106">These API's invoke the effect compiler fxc.exe which is the compiler used to compile HLSL code.</span></span> <span data-ttu-id="4adaa-107">這就是為什麼效果中程式碼的語法看起來很像 HLSL 程式碼 (有一些例外狀況會在稍後) 處理。</span><span class="sxs-lookup"><span data-stu-id="4adaa-107">This is why the syntax for code in an effect looks very much like HLSL code (there are a few exceptions that will be handled later).</span></span> <span data-ttu-id="4adaa-108">順便一提，編譯器/hlsl 編譯器 (fxc.exe) 會在 [公用程式] 資料夾的 SDK 中，讓您可以編譯著色器 (或在您選擇時) 離線效果。</span><span class="sxs-lookup"><span data-stu-id="4adaa-108">By the way, the effect compiler/hlsl compiler (fxc.exe) is in the SDK in the utilities folder so that you can compile your shaders (or effects) offline if you choose.</span></span> <span data-ttu-id="4adaa-109">請參閱從命令列執行編譯器的檔。</span><span class="sxs-lookup"><span data-stu-id="4adaa-109">See the documentation for running the compiler from the command line.</span></span>

-   [<span data-ttu-id="4adaa-110">Includes</span><span class="sxs-lookup"><span data-stu-id="4adaa-110">Includes</span></span>](#includes)
-   [<span data-ttu-id="4adaa-111">巨集</span><span class="sxs-lookup"><span data-stu-id="4adaa-111">Macros</span></span>](#macros)
-   [<span data-ttu-id="4adaa-112">HLSL 著色器旗標</span><span class="sxs-lookup"><span data-stu-id="4adaa-112">HLSL Shader Flags</span></span>](#hlsl-shader-flags)
-   [<span data-ttu-id="4adaa-113">FX 旗標</span><span class="sxs-lookup"><span data-stu-id="4adaa-113">FX Flags</span></span>](#fx-flags)
-   [<span data-ttu-id="4adaa-114">檢查錯誤</span><span class="sxs-lookup"><span data-stu-id="4adaa-114">Checking Errors</span></span>](#checking-errors)
-   [<span data-ttu-id="4adaa-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="4adaa-115">Related topics</span></span>](#related-topics)

<span data-ttu-id="4adaa-116">以下是從 BasicHLSL10 範例) 編譯效果檔案 (的範例。</span><span class="sxs-lookup"><span data-stu-id="4adaa-116">Here's an example of compiling an effect file (from the BasicHLSL10 sample).</span></span>


```
WCHAR str[MAX_PATH];
DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );

hr = D3DX10CompileEffectFromFile( str, NULL, NULL, "fx_4_0", 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
    &l_pBlob_Effect, &l_pBlob_Errors, NULL );
```



## <a name="includes"></a><span data-ttu-id="4adaa-117">Includes</span><span class="sxs-lookup"><span data-stu-id="4adaa-117">Includes</span></span>

<span data-ttu-id="4adaa-118">其中一個參數是 include 介面。</span><span class="sxs-lookup"><span data-stu-id="4adaa-118">One parameter is an include interface.</span></span> <span data-ttu-id="4adaa-119">如果您想要在讀取包含檔案時包含自訂的行為，請產生其中一種。</span><span class="sxs-lookup"><span data-stu-id="4adaa-119">Generate one of these if you want to include a customized behavior when reading an include file.</span></span> <span data-ttu-id="4adaa-120">此自訂行為會在每次建立使用 include 指標) 的效果 (，或編譯使用 include 指標) 的效果 (時執行。</span><span class="sxs-lookup"><span data-stu-id="4adaa-120">This custom behavior is executed each time an effect (that uses the include pointer) is created or when an effect (that uses the include pointer) is compiled.</span></span> <span data-ttu-id="4adaa-121">若要執行自訂的 include 行為，請從 Include 介面衍生類別。</span><span class="sxs-lookup"><span data-stu-id="4adaa-121">To implement customized include behavior, derive a class from the Include interface.</span></span> <span data-ttu-id="4adaa-122">這會提供您的類別兩種方法：開啟和關閉。</span><span class="sxs-lookup"><span data-stu-id="4adaa-122">This provides your class two methods: Open and Close.</span></span> <span data-ttu-id="4adaa-123">在 Open 和 Close 方法中執行自訂行為。</span><span class="sxs-lookup"><span data-stu-id="4adaa-123">Implement the custom behavior in the Open and Close methods.</span></span>

## <a name="macros"></a><span data-ttu-id="4adaa-124">巨集</span><span class="sxs-lookup"><span data-stu-id="4adaa-124">Macros</span></span>

<span data-ttu-id="4adaa-125">效果編譯也可以取得在其他位置定義的宏指標。</span><span class="sxs-lookup"><span data-stu-id="4adaa-125">Effect compilation can also take a pointer to macros that are defined elsewhere.</span></span> <span data-ttu-id="4adaa-126">例如，假設您要在 BasicHLSL10 中修改效果，以使用兩個宏：零和一。</span><span class="sxs-lookup"><span data-stu-id="4adaa-126">For example, suppose you were to modify the effect in BasicHLSL10, to use two macros: zero and one.</span></span> <span data-ttu-id="4adaa-127">使用這兩個宏的效果程式碼如下所示。</span><span class="sxs-lookup"><span data-stu-id="4adaa-127">The effect code that uses the two macros is shown here.</span></span>


```
if( bAnimate )
    vAnimatedPos += float4(vNormal, zero) *  
        (sin(g_fTime+5.5)+0.5)*5;
        
    Output.Diffuse.a = one;         
```



<span data-ttu-id="4adaa-128">以下是兩個宏的宣告。</span><span class="sxs-lookup"><span data-stu-id="4adaa-128">Here is the declaration for the two macros.</span></span>


```
D3D_SHADER_MACRO Shader_Macros[3] = { "zero", "0", "one", "1.0f", NULL, NULL };
```



<span data-ttu-id="4adaa-129">宏是以 Null 結束的宏陣列;其中每個宏都使用 [**D3D \_ 著色器 \_ 宏**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) 結構來定義。</span><span class="sxs-lookup"><span data-stu-id="4adaa-129">The macros are a NULL terminated array of macros; where each macro is defined with a [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) struct.</span></span>

<span data-ttu-id="4adaa-130">最後，修改編譯效果呼叫以取得宏的指標。</span><span class="sxs-lookup"><span data-stu-id="4adaa-130">Lastly, modify the compile effect call to take a pointer to the macros.</span></span>


```
D3DX10CreateEffectFromFile( str, Shader_Macros, NULL, 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
    &g_pEffect10, NULL );
```



## <a name="hlsl-shader-flags"></a><span data-ttu-id="4adaa-131">HLSL 著色器旗標</span><span class="sxs-lookup"><span data-stu-id="4adaa-131">HLSL Shader Flags</span></span>

<span data-ttu-id="4adaa-132">著色器旗標會指定 HLSL 編譯器的著色器條件約束。</span><span class="sxs-lookup"><span data-stu-id="4adaa-132">Shader flags specify shader constraints to the HLSL compiler.</span></span> <span data-ttu-id="4adaa-133">這些旗標會影響著色器編譯器產生的程式碼，包括：</span><span class="sxs-lookup"><span data-stu-id="4adaa-133">These flags impact the code generated by the shader compiler including:</span></span>

-   <span data-ttu-id="4adaa-134">大小考慮：將程式碼優化。</span><span class="sxs-lookup"><span data-stu-id="4adaa-134">Size considerations: optimize the code.</span></span>
-   <span data-ttu-id="4adaa-135">調試因素：包含調試資訊，防止流量控制。</span><span class="sxs-lookup"><span data-stu-id="4adaa-135">Debug considerations: including debug information, preventing flow control.</span></span>
-   <span data-ttu-id="4adaa-136">硬體考慮：編譯目標以及著色器是否可以在舊版硬體上執行。</span><span class="sxs-lookup"><span data-stu-id="4adaa-136">Hardware considerations: the compile target and whether or not a shader can run on legacy hardware.</span></span>

<span data-ttu-id="4adaa-137">一般而言，如果您未指定兩個衝突的特性，這些旗標可以邏輯方式結合。</span><span class="sxs-lookup"><span data-stu-id="4adaa-137">In general, these flags can be logically combined, assuming you have not specified two conflicting characteristics.</span></span> <span data-ttu-id="4adaa-138">如需旗標的清單，請參閱 [ (Direct3D 10) 的效果常數 ](d3d10-graphics-reference-effect-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="4adaa-138">For a listing of the flags see [Effect Constants (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).</span></span>

## <a name="fx-flags"></a><span data-ttu-id="4adaa-139">FX 旗標</span><span class="sxs-lookup"><span data-stu-id="4adaa-139">FX Flags</span></span>

<span data-ttu-id="4adaa-140">這些旗標是在建立效果來定義編譯行為或執行時間效果行為時使用。</span><span class="sxs-lookup"><span data-stu-id="4adaa-140">These flags used when creating an effect to define either compilation behavior or runtime effect behavior.</span></span> <span data-ttu-id="4adaa-141">如需旗標的清單，請參閱 [ (Direct3D 10) 的效果常數 ](d3d10-graphics-reference-effect-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="4adaa-141">For a listing of the flags see [Effect Constants (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).</span></span>

## <a name="checking-errors"></a><span data-ttu-id="4adaa-142">檢查錯誤</span><span class="sxs-lookup"><span data-stu-id="4adaa-142">Checking Errors</span></span>

<span data-ttu-id="4adaa-143">如果在編譯期間發生錯誤，則 API 會傳回包含效果編譯器所傳回之錯誤的介面。</span><span class="sxs-lookup"><span data-stu-id="4adaa-143">If during compilation, an error occurs, the API returns an interface which contains the errors returned from the effect compiler.</span></span> <span data-ttu-id="4adaa-144">這個介面稱為 ID3D10Blob。</span><span class="sxs-lookup"><span data-stu-id="4adaa-144">This interface is called ID3D10Blob.</span></span> <span data-ttu-id="4adaa-145">但是，它無法直接讀取，但藉由將指標傳回至包含資料 (的緩衝區（這是) 的字串），您就可以看到任何編譯錯誤。</span><span class="sxs-lookup"><span data-stu-id="4adaa-145">It is not directly readable, however, by returning a pointer to the buffer that contains the data (which is a string), you can see any compilation errors.</span></span>

<span data-ttu-id="4adaa-146">在此範例中，藉由複製第一個變數宣告兩次，將錯誤引入 BasicHLSL。</span><span class="sxs-lookup"><span data-stu-id="4adaa-146">In this example, an error was introduced into the BasicHLSL.fx effect by copying the first variable declaration twice.</span></span>


```
//-------------------------------------------------------------------
// Global variables
//-------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color

// Declare the same variable twice
float4 g_MaterialAmbientColor;      // Material's ambient color
```



<span data-ttu-id="4adaa-147">此錯誤會導致編譯器傳回下列錯誤，如 Microsoft Visual Studio 的 [監看式] 視窗的下列螢幕擷取畫面所示。</span><span class="sxs-lookup"><span data-stu-id="4adaa-147">This error caused the compiler to return the following error, as shown in the following screen shot of the watch window in Microsoft Visual Studio.</span></span>

![visual studio [監看式] 視窗的螢幕擷取畫面](images/effect-compile-errors-2.jpg)

<span data-ttu-id="4adaa-149">由於錯誤會在 LPVOID 指標中傳回，因此會將它轉換成 [監看式] 視窗中的字元字串。</span><span class="sxs-lookup"><span data-stu-id="4adaa-149">Since the error is returned in a LPVOID pointer, cast it to a character string in the watch window.</span></span>

<span data-ttu-id="4adaa-150">以下是用來從失敗的編譯傳回錯誤的程式碼。</span><span class="sxs-lookup"><span data-stu-id="4adaa-150">Here is the code used to return the error from the failed compile.</span></span>


```
// Read the D3DX effect file
WCHAR str[MAX_PATH];
ID3D10Blob* l_pBlob_Effect = NULL;
ID3D10Blob* l_pBlob_Errors = NULL;
hr = DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );
hr = D3DX10CompileEffectFromFile( str, NULL, NULL, 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, NULL, 
    &l_pBlob_Effect, &l_pBlob_Errors );

LPVOID l_pError = NULL;
if( l_pBlob_Errors )
{
    l_pError = l_pBlob_Errors->GetBufferPointer();
    // then cast to a char* to see it in the locals window
}
```



## <a name="related-topics"></a><span data-ttu-id="4adaa-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="4adaa-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4adaa-152">轉譯 (Direct3D 10) 的效果 </span><span class="sxs-lookup"><span data-stu-id="4adaa-152">Rendering an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 




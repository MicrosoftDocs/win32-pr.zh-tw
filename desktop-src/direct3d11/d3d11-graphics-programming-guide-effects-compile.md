---
title: '將效果編譯 (Direct3D 11) '
description: 在撰寫效果之後，下一步是要編譯器代碼以檢查語法問題。
ms.assetid: 7624d55e-6466-4156-8f31-30f0d25a2883
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3df304a7b657af19984008bd90a1be4bfe5219c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933356"
---
# <a name="compile-an-effect-direct3d-11"></a><span data-ttu-id="3ac83-103">將效果編譯 (Direct3D 11) </span><span class="sxs-lookup"><span data-stu-id="3ac83-103">Compile an Effect (Direct3D 11)</span></span>

<span data-ttu-id="3ac83-104">在撰寫效果之後，下一步是要編譯器代碼以檢查語法問題。</span><span class="sxs-lookup"><span data-stu-id="3ac83-104">After an effect has been authored, the next step is to compile the code to check for syntax problems.</span></span>

<span data-ttu-id="3ac83-105">若要這麼做，請呼叫其中一個編譯 Api ([**D3DX11CompileFromFile**](d3dx11compilefromfile.md)、 [**D3DX11CompileFromMemory**](d3dx11compilefrommemory.md)或 [**D3DX11CompileFromResource**](d3dx11compilefromresource.md) ) 。</span><span class="sxs-lookup"><span data-stu-id="3ac83-105">You do so by calling one of the compile APIs ([**D3DX11CompileFromFile**](d3dx11compilefromfile.md), [**D3DX11CompileFromMemory**](d3dx11compilefrommemory.md), or [**D3DX11CompileFromResource**](d3dx11compilefromresource.md) ).</span></span> <span data-ttu-id="3ac83-106">這些 Api 會叫用效果編譯器 fxc.exe，以編譯 HLSL 程式碼。</span><span class="sxs-lookup"><span data-stu-id="3ac83-106">These APIs invoke the effect compiler fxc.exe, which compiles HLSL code.</span></span> <span data-ttu-id="3ac83-107">這就是為什麼效果中的程式碼語法看起來非常類似 HLSL 程式碼的原因。</span><span class="sxs-lookup"><span data-stu-id="3ac83-107">This is why the syntax for code in an effect looks very much like HLSL code.</span></span> <span data-ttu-id="3ac83-108"> (有一些例外狀況會在稍後) 處理。</span><span class="sxs-lookup"><span data-stu-id="3ac83-108">(There are a few exceptions that will be handled later).</span></span> <span data-ttu-id="3ac83-109">您可以在 [公用程式] 資料夾的 SDK 中使用效果編譯器/hlsl 編譯器 fxc.exe，以在您選擇的情況下離線編譯著色器 (或效果) 。</span><span class="sxs-lookup"><span data-stu-id="3ac83-109">The effect compiler/hlsl compiler, fxc.exe, is available in the SDK in the utilities folder so that shaders (or effects) can be compiled offline if you choose.</span></span> <span data-ttu-id="3ac83-110">請參閱從命令列執行編譯器的檔。</span><span class="sxs-lookup"><span data-stu-id="3ac83-110">See the documentation for running the compiler from the command line.</span></span>

-   [<span data-ttu-id="3ac83-111">範例</span><span class="sxs-lookup"><span data-stu-id="3ac83-111">Example</span></span>](#example)
-   [<span data-ttu-id="3ac83-112">Includes</span><span class="sxs-lookup"><span data-stu-id="3ac83-112">Includes</span></span>](#includes)
-   [<span data-ttu-id="3ac83-113">搜尋 Include 檔</span><span class="sxs-lookup"><span data-stu-id="3ac83-113">Searching for Include Files</span></span>](#searching-for-include-files)
-   [<span data-ttu-id="3ac83-114">巨集</span><span class="sxs-lookup"><span data-stu-id="3ac83-114">Macros</span></span>](#macros)
-   [<span data-ttu-id="3ac83-115">HLSL 著色器旗標</span><span class="sxs-lookup"><span data-stu-id="3ac83-115">HLSL Shader Flags</span></span>](#hlsl-shader-flags)
-   [<span data-ttu-id="3ac83-116">FX 旗標</span><span class="sxs-lookup"><span data-stu-id="3ac83-116">FX Flags</span></span>](#fx-flags)
-   [<span data-ttu-id="3ac83-117">檢查錯誤</span><span class="sxs-lookup"><span data-stu-id="3ac83-117">Checking Errors</span></span>](#checking-errors)
-   [<span data-ttu-id="3ac83-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="3ac83-118">Related topics</span></span>](#related-topics)

## <a name="example"></a><span data-ttu-id="3ac83-119">範例</span><span class="sxs-lookup"><span data-stu-id="3ac83-119">Example</span></span>

<span data-ttu-id="3ac83-120">以下是編譯效果檔案的範例。</span><span class="sxs-lookup"><span data-stu-id="3ac83-120">Here's an example of compiling an effect file.</span></span>


```
WCHAR str[MAX_PATH];
DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );

hr = D3DX11CompileFromFile( str, NULL, NULL, pFunctionName, pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, NULL, &pBlob, &pErrorBlob, NULL );
```



## <a name="includes"></a><span data-ttu-id="3ac83-121">Includes</span><span class="sxs-lookup"><span data-stu-id="3ac83-121">Includes</span></span>

<span data-ttu-id="3ac83-122">編譯 Api 的一個參數是包含介面。</span><span class="sxs-lookup"><span data-stu-id="3ac83-122">One parameter of the compile APIs is an include interface.</span></span> <span data-ttu-id="3ac83-123">如果您想要在編譯器讀取 include 檔時包含自訂的行為，請產生其中一種。</span><span class="sxs-lookup"><span data-stu-id="3ac83-123">Generate one of these if you want to include a customized behavior when the compiler reads an include file.</span></span> <span data-ttu-id="3ac83-124">編譯器會在每次建立或編譯使用 include 指標) 的效果 (時，執行這個自訂行為。</span><span class="sxs-lookup"><span data-stu-id="3ac83-124">The compiler executes this custom behavior each time it creates or compiles an effect (that uses the include pointer).</span></span> <span data-ttu-id="3ac83-125">若要執行自訂的 include 行為，請從 [**ID3DInclude**](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) 介面衍生類別。</span><span class="sxs-lookup"><span data-stu-id="3ac83-125">To implement customized include behavior, derive a class from the [**ID3DInclude**](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) interface.</span></span> <span data-ttu-id="3ac83-126">這可為您的類別提供兩種方法： [**開啟**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) 和 [**關閉**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-close)。</span><span class="sxs-lookup"><span data-stu-id="3ac83-126">This provides your class with two methods: [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) and [**Close**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-close).</span></span> <span data-ttu-id="3ac83-127">在這些方法中執行自訂行為。</span><span class="sxs-lookup"><span data-stu-id="3ac83-127">Implement the custom behavior in these methods.</span></span>

## <a name="searching-for-include-files"></a><span data-ttu-id="3ac83-128">搜尋 Include 檔</span><span class="sxs-lookup"><span data-stu-id="3ac83-128">Searching for Include Files</span></span>

<span data-ttu-id="3ac83-129">編譯器在 *pParentData* 參數中傳遞給包含處理常式 [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) 方法的指標，可能不會指向包含 \# 編譯器編譯著色器程式碼所需之 include 檔的容器。</span><span class="sxs-lookup"><span data-stu-id="3ac83-129">The pointer that the compiler passes in the *pParentData* parameter to your include handler's [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) method might not point to the container that includes the \#include file that the compiler needs to compile your shader code.</span></span> <span data-ttu-id="3ac83-130">也就是說，編譯器可能會在 *pParentData* 中傳遞 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="3ac83-130">That is, the compiler might pass **NULL** in *pParentData*.</span></span> <span data-ttu-id="3ac83-131">因此，我們建議您的 include 處理常式搜尋自己的內容包含位置清單。</span><span class="sxs-lookup"><span data-stu-id="3ac83-131">Therefore, we recommend that your include handler search its own list of include locations for content.</span></span> <span data-ttu-id="3ac83-132">您的 include 處理常式可以動態地加入新的 include 位置，因為它會在呼叫其 **Open** 方法時接收這些位置。</span><span class="sxs-lookup"><span data-stu-id="3ac83-132">Your include handler can dynamically add new include locations as it receives those locations in calls to its **Open** method.</span></span>

<span data-ttu-id="3ac83-133">在下列範例中，假設著色器程式碼的 include 檔案都儲存在 *somewhereelse* 目錄中。</span><span class="sxs-lookup"><span data-stu-id="3ac83-133">In the following example, suppose that the shader code's include files are both stored in the *somewhereelse* directory.</span></span> <span data-ttu-id="3ac83-134">當編譯器呼叫 include 處理常式的 [**open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) 方法來開啟和讀取 *somewhereelse \\ foo .h* 的內容時，include 處理常式可以儲存 **somewhereelse** 目錄的位置。</span><span class="sxs-lookup"><span data-stu-id="3ac83-134">When the compiler calls the include handler's [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) method to open and read the contents of *somewhereelse\\foo.h*, the include handler can save the location of the **somewhereelse** directory.</span></span> <span data-ttu-id="3ac83-135">稍後，當編譯器呼叫 include 處理常式的 **open** 方法來開啟和讀取 *bar* 的內容時，include 處理常式可以在 *somewhereelse* 目錄中自動搜尋 *bar. h*。</span><span class="sxs-lookup"><span data-stu-id="3ac83-135">Later, when the compiler calls the include handler's **Open** method to open and read the contents of *bar.h*, the include handler can automatically search in the *somewhereelse* directory for *bar.h*.</span></span>


```
Main.hlsl:
#include "somewhereelse\foo.h"

Foo.h:
#include "bar.h"
```



## <a name="macros"></a><span data-ttu-id="3ac83-136">巨集</span><span class="sxs-lookup"><span data-stu-id="3ac83-136">Macros</span></span>

<span data-ttu-id="3ac83-137">效果編譯也可以取得在其他位置定義的宏指標。</span><span class="sxs-lookup"><span data-stu-id="3ac83-137">Effect compilation can also take a pointer to macros that are defined elsewhere.</span></span> <span data-ttu-id="3ac83-138">例如，假設您想要修改 BasicHLSL10 中的效果，以使用兩個宏：零和一。</span><span class="sxs-lookup"><span data-stu-id="3ac83-138">For example, suppose you want to modify the effect in BasicHLSL10, to use two macros: zero and one.</span></span> <span data-ttu-id="3ac83-139">使用這兩個宏的效果程式碼如下所示。</span><span class="sxs-lookup"><span data-stu-id="3ac83-139">The effect code that uses the two macros is shown here.</span></span>


```
if( bAnimate )
    vAnimatedPos += float4(vNormal, zero) *  
        (sin(g_fTime+5.5)+0.5)*5;
        
    Output.Diffuse.a = one;         
```



<span data-ttu-id="3ac83-140">以下是兩個宏的宣告。</span><span class="sxs-lookup"><span data-stu-id="3ac83-140">Here is the declaration for the two macros.</span></span>


```
D3D10_SHADER_MACRO Shader_Macros[3] = { "zero", "0", "one", "1.0f", NULL, NULL };
```



<span data-ttu-id="3ac83-141">宏是以 Null 結束的宏陣列;其中每個宏都是使用 [**D3D10 \_ 著色器 \_ 宏**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) 結構來定義。</span><span class="sxs-lookup"><span data-stu-id="3ac83-141">The macros are a NULL-terminated array of macros; where each macro is defined by using a [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) struct.</span></span>

<span data-ttu-id="3ac83-142">修改編譯效果呼叫以取得宏的指標。</span><span class="sxs-lookup"><span data-stu-id="3ac83-142">Modify the compile effect call to take a pointer to the macros.</span></span>


```
D3DX11CompileFromFile( str, Shader_Macros, NULL, pFunctionName, 
                       pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, 
                       NULL, &pBlob, &pErrorBlob, NULL );    
```



## <a name="hlsl-shader-flags"></a><span data-ttu-id="3ac83-143">HLSL 著色器旗標</span><span class="sxs-lookup"><span data-stu-id="3ac83-143">HLSL Shader Flags</span></span>

<span data-ttu-id="3ac83-144">著色器旗標會指定 HLSL 編譯器的著色器條件約束。</span><span class="sxs-lookup"><span data-stu-id="3ac83-144">Shader flags specify shader constraints to the HLSL compiler.</span></span> <span data-ttu-id="3ac83-145">這些旗標會以下列方式影響著色器編譯器產生的程式碼：</span><span class="sxs-lookup"><span data-stu-id="3ac83-145">These flags affect the code generated by the shader compiler in the following ways:</span></span>

-   <span data-ttu-id="3ac83-146">優化程式碼大小。</span><span class="sxs-lookup"><span data-stu-id="3ac83-146">Optimize the code size.</span></span>
-   <span data-ttu-id="3ac83-147">包含可防止流量控制的調試資訊。</span><span class="sxs-lookup"><span data-stu-id="3ac83-147">Including debug information, which prevents flow control.</span></span>
-   <span data-ttu-id="3ac83-148">會影響編譯目標，以及著色器是否可以在舊版硬體上執行。</span><span class="sxs-lookup"><span data-stu-id="3ac83-148">Affects the compile target and whether a shader can run on legacy hardware.</span></span>

<span data-ttu-id="3ac83-149">如果您未指定兩個衝突的特性，這些旗標可以邏輯方式結合。</span><span class="sxs-lookup"><span data-stu-id="3ac83-149">These flags can be logically combined if you have not specified two conflicting characteristics.</span></span> <span data-ttu-id="3ac83-150">如需旗標的清單，請參閱 [D3D10 \_ 著色器常數](/windows/desktop/direct3d10/d3d10-shader)。</span><span class="sxs-lookup"><span data-stu-id="3ac83-150">For a listing of the flags see [D3D10\_SHADER Constants](/windows/desktop/direct3d10/d3d10-shader).</span></span>

## <a name="fx-flags"></a><span data-ttu-id="3ac83-151">FX 旗標</span><span class="sxs-lookup"><span data-stu-id="3ac83-151">FX Flags</span></span>

<span data-ttu-id="3ac83-152">當您建立效果來定義編譯行為或執行時間效果行為時，請使用這些旗標。</span><span class="sxs-lookup"><span data-stu-id="3ac83-152">Use these flags when you create an effect to define either compilation behavior or runtime effect behavior.</span></span> <span data-ttu-id="3ac83-153">如需旗標的清單，請參閱 [D3D10 \_ 效果常數](/windows/desktop/direct3d10/d3d10-effect)。</span><span class="sxs-lookup"><span data-stu-id="3ac83-153">For a listing of the flags see [D3D10\_EFFECT Constants](/windows/desktop/direct3d10/d3d10-effect).</span></span>

## <a name="checking-errors"></a><span data-ttu-id="3ac83-154">檢查錯誤</span><span class="sxs-lookup"><span data-stu-id="3ac83-154">Checking Errors</span></span>

<span data-ttu-id="3ac83-155">如果在編譯期間發生錯誤，則 API 會傳回包含效果編譯器錯誤的介面。</span><span class="sxs-lookup"><span data-stu-id="3ac83-155">If during compilation an error occurs, the API returns an interface that contains the errors from the effect compiler.</span></span> <span data-ttu-id="3ac83-156">這個介面稱為 [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="3ac83-156">This interface is called [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)).</span></span> <span data-ttu-id="3ac83-157">它無法直接讀取;不過，藉由將指標傳回至包含資料 (的緩衝區（這是) 的字串），您可以看到任何編譯錯誤。</span><span class="sxs-lookup"><span data-stu-id="3ac83-157">It is not directly readable; however, by returning a pointer to the buffer that contains the data (which is a string), you can see any compilation errors.</span></span>

<span data-ttu-id="3ac83-158">此範例包含 BasicHLSL 中的錯誤，第一個變數宣告會出現兩次。</span><span class="sxs-lookup"><span data-stu-id="3ac83-158">This example contains an error in the BasicHLSL.fx, the first variable declaration occurs twice.</span></span>


```
//-------------------------------------------------------------------
// Global variables
//-------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color

// Declare the same variable twice
float4 g_MaterialAmbientColor;      // Material's ambient color
```



<span data-ttu-id="3ac83-159">此錯誤會導致編譯器傳回下列錯誤，如 Microsoft Visual Studio 中監看式視窗的下列螢幕擷取畫面所示。</span><span class="sxs-lookup"><span data-stu-id="3ac83-159">This error causes the compiler to return the following error, as shown in the following screen shot of the Watch window in Microsoft Visual Studio.</span></span>

![visual studio 監看式視窗的螢幕擷取畫面，其中包含0x01997fb8 錯誤](images/effect-compile-errors-2.jpg)

<span data-ttu-id="3ac83-161">因為編譯器會在 LPVOID 指標中傳回錯誤，所以會將它轉換成監看式視窗中的字元字串。</span><span class="sxs-lookup"><span data-stu-id="3ac83-161">Because the compiler returns the error in a LPVOID pointer, cast it to a character string in the Watch window.</span></span>

<span data-ttu-id="3ac83-162">以下是從失敗的編譯傳回錯誤的程式碼。</span><span class="sxs-lookup"><span data-stu-id="3ac83-162">Here is the code that returns the error from the failed compile.</span></span>


```
// Read the D3DX effect file
WCHAR str[MAX_PATH];
ID3DBlob*   l_pBlob_Effect = NULL;
ID3DBlob*   l_pBlob_Errors = NULL;
hr = DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );
hr = D3DX11CompileFromFile( str, NULL, NULL, pFunctionName, 
                       pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, 
                       NULL, &pBlob, &pErrorBlob, NULL );      

LPVOID l_pError = NULL;
if( pErrorBlob )
{
    l_pError = pErrorBlob->GetBufferPointer();
    // then cast to a char* to see it in the locals window
}
```



## <a name="related-topics"></a><span data-ttu-id="3ac83-163">相關主題</span><span class="sxs-lookup"><span data-stu-id="3ac83-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ac83-164">轉譯 (Direct3D 11) 的效果 </span><span class="sxs-lookup"><span data-stu-id="3ac83-164">Rendering an Effect (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 
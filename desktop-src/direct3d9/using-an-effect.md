---
description: 此頁面將示範如何產生和使用效果。
ms.assetid: d9fdafed-5958-4995-a1b5-8881feca1291
title: '使用效果 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1170fde625e5eee5e9665f0759d302b5f5450a41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109884"
---
# <a name="using-an-effect-direct3d-9"></a><span data-ttu-id="d1834-103">使用效果 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="d1834-103">Using an Effect (Direct3D 9)</span></span>

<span data-ttu-id="d1834-104">此頁面將示範如何產生和使用效果。</span><span class="sxs-lookup"><span data-stu-id="d1834-104">This page will show you how to generate and use an effect.</span></span> <span data-ttu-id="d1834-105">涵蓋的主題包括如何：</span><span class="sxs-lookup"><span data-stu-id="d1834-105">The topics covered include how to:</span></span>

-   [<span data-ttu-id="d1834-106">建立效果</span><span class="sxs-lookup"><span data-stu-id="d1834-106">Create an Effect</span></span>](#create-an-effect)
-   [<span data-ttu-id="d1834-107">呈現效果</span><span class="sxs-lookup"><span data-stu-id="d1834-107">Render an Effect</span></span>](#render-an-effect)
-   [<span data-ttu-id="d1834-108">使用語義來尋找效果參數</span><span class="sxs-lookup"><span data-stu-id="d1834-108">Use Semantics to Find Effect Parameters</span></span>](#use-semantics-to-find-effect-parameters)
-   [<span data-ttu-id="d1834-109">使用控制碼有效率地取得和設定參數</span><span class="sxs-lookup"><span data-stu-id="d1834-109">Use Handles to Get and Set Parameters Efficiently</span></span>](#use-handles-to-get-and-set-parameters-efficiently)
-   [<span data-ttu-id="d1834-110">使用批註新增參數資訊</span><span class="sxs-lookup"><span data-stu-id="d1834-110">Add Parameter Information with Annotations</span></span>](#add-parameter-information-with-annotations)
-   [<span data-ttu-id="d1834-111">共用效果參數</span><span class="sxs-lookup"><span data-stu-id="d1834-111">Share Effect Parameters</span></span>](#share-effect-parameters)
-   [<span data-ttu-id="d1834-112">離線編譯效果</span><span class="sxs-lookup"><span data-stu-id="d1834-112">Compile an Effect Offline</span></span>](#compile-an-effect-offline)
-   [<span data-ttu-id="d1834-113">使用 Preshaders 改善效能</span><span class="sxs-lookup"><span data-stu-id="d1834-113">Improve Performance with Preshaders</span></span>](#improve-performance-with-preshaders)
-   [<span data-ttu-id="d1834-114">使用參數區塊來管理效果參數</span><span class="sxs-lookup"><span data-stu-id="d1834-114">Use Parameter Blocks to Manage Effect Parameters</span></span>](#use-parameter-blocks-to-manage-effect-parameters)

## <a name="create-an-effect"></a><span data-ttu-id="d1834-115">建立效果</span><span class="sxs-lookup"><span data-stu-id="d1834-115">Create an Effect</span></span>

<span data-ttu-id="d1834-116">以下是建立從 [BasicHLSL 範例](../directx-sdk--august-2009-.md)取得之效果的範例。</span><span class="sxs-lookup"><span data-stu-id="d1834-116">Here is an example of creating an effect taken from the [BasicHLSL Sample](../directx-sdk--august-2009-.md).</span></span> <span data-ttu-id="d1834-117">建立偵錯工具著色器的效果建立程式碼是來自 **OnCreateDevice**：</span><span class="sxs-lookup"><span data-stu-id="d1834-117">The effect creation code for creating a debug shader is from **OnCreateDevice**:</span></span>


```
ID3DXEffect* g_pEffect = NULL;
DWORD dwShaderFlags = 0;

    dwShaderFlags |= D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT;
    dwShaderFlags |= D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT;
    dwShaderFlags |= D3DXSHADER_NO_PRESHADER;

    // Read the D3DX effect file
    WCHAR str[MAX_PATH];
    DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL.fx" );

    D3DXCreateEffectFromFile( 
        pd3dDevice, 
        str, 
        NULL, // CONST D3DXMACRO* pDefines,
        NULL, // LPD3DXINCLUDE pInclude,
        dwShaderFlags, 
        NULL, // LPD3DXEFFECTPOOL pPool,
        &g_pEffect, 
        NULL );
```



<span data-ttu-id="d1834-118">此函式會採用下列引數：</span><span class="sxs-lookup"><span data-stu-id="d1834-118">This function takes these arguments:</span></span>

-   <span data-ttu-id="d1834-119">裝置。</span><span class="sxs-lookup"><span data-stu-id="d1834-119">The device.</span></span>
-   <span data-ttu-id="d1834-120">效果檔案的檔案名。</span><span class="sxs-lookup"><span data-stu-id="d1834-120">The file name of the effect file.</span></span>
-   <span data-ttu-id="d1834-121">以 Null 終止的定義清單的指標，可在 \# 剖析著色器時使用。</span><span class="sxs-lookup"><span data-stu-id="d1834-121">A pointer to a NULL-terminated list of \#defines, to be used while parsing the shader.</span></span>
-   <span data-ttu-id="d1834-122">使用者撰寫的 include 處理常式的選擇性指標。</span><span class="sxs-lookup"><span data-stu-id="d1834-122">An optional pointer to a user-written include handler.</span></span> <span data-ttu-id="d1834-123">每當處理器需要解析包含時，就會呼叫此處理程式 \# 。</span><span class="sxs-lookup"><span data-stu-id="d1834-123">The handler is called by the processor whenever it needs to resolve a \#include.</span></span>
-   <span data-ttu-id="d1834-124">著色器編譯旗標，可讓編譯器提示您瞭解如何使用著色器。</span><span class="sxs-lookup"><span data-stu-id="d1834-124">A shader compile flag that gives the compiler hints about how the shader will be used.</span></span> <span data-ttu-id="d1834-125">選項包括：</span><span class="sxs-lookup"><span data-stu-id="d1834-125">The options include:</span></span>
    -   <span data-ttu-id="d1834-126">如果正在編譯已知的良好著色器，則略過驗證。</span><span class="sxs-lookup"><span data-stu-id="d1834-126">Skipping validation, if known good shaders are being compiled.</span></span>
    -   <span data-ttu-id="d1834-127">略過優化 (有時會在優化使) 更難進行調試時使用。</span><span class="sxs-lookup"><span data-stu-id="d1834-127">Skipping optimization (sometimes used when optimizations make debugging harder).</span></span>
    -   <span data-ttu-id="d1834-128">要求要包含在著色器中的 debug 資訊，讓它可以進行調試。</span><span class="sxs-lookup"><span data-stu-id="d1834-128">Requesting debug information to be included in the shader so it can be debugged.</span></span>
-   <span data-ttu-id="d1834-129">效果集區。</span><span class="sxs-lookup"><span data-stu-id="d1834-129">The effect pool.</span></span> <span data-ttu-id="d1834-130">如果有多個效果使用相同的記憶體集區指標，則效果中的全域變數會彼此共用。</span><span class="sxs-lookup"><span data-stu-id="d1834-130">If more than one effect uses the same memory pool pointer, the global variables in the effects are shared with each other.</span></span> <span data-ttu-id="d1834-131">如果不需要共用效果變數，記憶體集區可以設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d1834-131">If there is no need to share effect variables, the memory pool can be set to **NULL**.</span></span>
-   <span data-ttu-id="d1834-132">新效果的指標。</span><span class="sxs-lookup"><span data-stu-id="d1834-132">A pointer to the new effect.</span></span>
-   <span data-ttu-id="d1834-133">可傳送驗證錯誤之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="d1834-133">A pointer to a buffer to which validation errors can be sent.</span></span> <span data-ttu-id="d1834-134">在此範例中，參數已設為 **Null** 且未使用。</span><span class="sxs-lookup"><span data-stu-id="d1834-134">In this example, the parameter was set to **NULL** and not used.</span></span>

> [!Note]  
> <span data-ttu-id="d1834-135">自2006年12月起的 SDK 起，DirectX 10 HLSL 編譯器現在是 DirectX 9 和 DirectX 10 中的預設編譯器。</span><span class="sxs-lookup"><span data-stu-id="d1834-135">Beginning with the December 2006 SDK, the DirectX 10 HLSL compiler is now the default compiler in both DirectX 9 and DirectX 10.</span></span> <span data-ttu-id="d1834-136">請參閱 [效果-編譯器工具](../direct3dtools/fxc.md) 以取得詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d1834-136">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

 

## <a name="render-an-effect"></a><span data-ttu-id="d1834-137">呈現效果</span><span class="sxs-lookup"><span data-stu-id="d1834-137">Render an Effect</span></span>

<span data-ttu-id="d1834-138">將效果狀態套用至裝置的呼叫順序為：</span><span class="sxs-lookup"><span data-stu-id="d1834-138">The sequence of calls for applying effect state to a device is:</span></span>

-   <span data-ttu-id="d1834-139">[**ID3DXEffect：： Begin**](id3dxeffect--begin.md) 設定使用中的技術。</span><span class="sxs-lookup"><span data-stu-id="d1834-139">[**ID3DXEffect::Begin**](id3dxeffect--begin.md) sets the active technique.</span></span>
-   <span data-ttu-id="d1834-140">[**ID3DXEffect：： BeginPass**](id3dxeffect--beginpass.md) 會設定主動傳遞。</span><span class="sxs-lookup"><span data-stu-id="d1834-140">[**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) sets the active pass.</span></span>
-   <span data-ttu-id="d1834-141">[**ID3DXEffect：： CommitChanges**](id3dxeffect--commitchanges.md) 會更新傳遞中任何 set 呼叫的變更。</span><span class="sxs-lookup"><span data-stu-id="d1834-141">[**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md) updates changes to any set calls in the pass.</span></span> <span data-ttu-id="d1834-142">這應該在任何繪製呼叫之前呼叫。</span><span class="sxs-lookup"><span data-stu-id="d1834-142">This should be called before any draw call.</span></span>
-   <span data-ttu-id="d1834-143">[**ID3DXEffect：： EndPass**](id3dxeffect--endpass.md) 結束傳遞。</span><span class="sxs-lookup"><span data-stu-id="d1834-143">[**ID3DXEffect::EndPass**](id3dxeffect--endpass.md) ends a pass.</span></span>
-   <span data-ttu-id="d1834-144">[**ID3DXEffect：： End**](id3dxeffect--end.md) 結束使用中的技術。</span><span class="sxs-lookup"><span data-stu-id="d1834-144">[**ID3DXEffect::End**](id3dxeffect--end.md) ends the active technique.</span></span>

<span data-ttu-id="d1834-145">效果轉譯程式碼也比對應的轉譯程式碼還簡單，而不會有效果。</span><span class="sxs-lookup"><span data-stu-id="d1834-145">Effect render code is also simpler than the corresponding render code without an effect.</span></span> <span data-ttu-id="d1834-146">以下是具有效果的轉譯程式碼：</span><span class="sxs-lookup"><span data-stu-id="d1834-146">Here's the render code with an effect:</span></span>


```
// Apply the technique contained in the effect 
g_pEffect->Begin(&cPasses, 0);

for (iPass = 0; iPass < cPasses; iPass++)
{
    g_pEffect->BeginPass(iPass);

    // Only call CommitChanges if any state changes have happened
    // after BeginPass is called
    g_pEffect->CommitChanges();

    // Render the mesh with the applied technique
    g_pMesh->DrawSubset(0);

    g_pEffect->EndPass();
}
g_pEffect->End();
```



<span data-ttu-id="d1834-147">轉譯迴圈包含查詢效果，以查看其中包含多少個傳遞，然後呼叫一項技術的所有階段。</span><span class="sxs-lookup"><span data-stu-id="d1834-147">The render loop consists of querying the effect to see how many passes it contains, and then calling all the passes for a technique.</span></span> <span data-ttu-id="d1834-148">您可以展開轉譯迴圈來呼叫多個技術，每個都有多個階段。</span><span class="sxs-lookup"><span data-stu-id="d1834-148">The render loop could be expanded to call multiple techniques, each with multiple passes.</span></span>

## <a name="use-semantics-to-find-effect-parameters"></a><span data-ttu-id="d1834-149">使用語義來尋找效果參數</span><span class="sxs-lookup"><span data-stu-id="d1834-149">Use Semantics to Find Effect Parameters</span></span>

<span data-ttu-id="d1834-150">語義是附加至效果參數的識別碼，可讓應用程式搜尋參數。</span><span class="sxs-lookup"><span data-stu-id="d1834-150">A semantic is an identifier that is attached to an effect parameter to allow an application to search for the parameter.</span></span> <span data-ttu-id="d1834-151">參數最多隻能有一個語義。</span><span class="sxs-lookup"><span data-stu-id="d1834-151">A parameter can have at most one semantic.</span></span> <span data-ttu-id="d1834-152">語義位於冒號 (：在參數名稱之後 ) 。</span><span class="sxs-lookup"><span data-stu-id="d1834-152">The semantic is located following a colon (:) after the parameter name.</span></span> <span data-ttu-id="d1834-153">例如：</span><span class="sxs-lookup"><span data-stu-id="d1834-153">For instance:</span></span>


```
float4x4 matWorldViewProj : WORLDVIEWPROJ;
```



<span data-ttu-id="d1834-154">如果您在未使用語義的情況下宣告效果全域變數，則會改為這樣：</span><span class="sxs-lookup"><span data-stu-id="d1834-154">If you declared the effect global variable without using a semantic, it would look like this instead:</span></span>


```
float4x4 matWorldViewProj;
```



<span data-ttu-id="d1834-155">效果介面可以使用語義來取得特定效果參數的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d1834-155">The effect interface can use a semantic to get a handle to a particular effect parameter.</span></span> <span data-ttu-id="d1834-156">例如，下列範例會傳回矩陣的控制碼：</span><span class="sxs-lookup"><span data-stu-id="d1834-156">For instance, the following returns the handle of the matrix:</span></span>


```
D3DHANDLE handle = 
    m_pEffect->GetParameterBySemantic(NULL, "WORLDVIEWPROJ");
```



<span data-ttu-id="d1834-157">除了依語義名稱搜尋，效果介面還有許多其他方法可搜尋參數。</span><span class="sxs-lookup"><span data-stu-id="d1834-157">In addition to searching by semantic name, the effect interface has many other methods to search for parameters.</span></span>

## <a name="use-handles-to-get-and-set-parameters-efficiently"></a><span data-ttu-id="d1834-158">使用控制碼有效率地取得和設定參數</span><span class="sxs-lookup"><span data-stu-id="d1834-158">Use Handles to Get and Set Parameters Efficiently</span></span>

<span data-ttu-id="d1834-159">控點提供有效的方法來參考效果參數、技術、傳遞和具有效果的批註。</span><span class="sxs-lookup"><span data-stu-id="d1834-159">Handles provide an efficient means for referencing effect parameters, techniques, passes, and annotations with an effect.</span></span> <span data-ttu-id="d1834-160">處理屬於 D3DXHANDLE) 類型的 (是字串指標。</span><span class="sxs-lookup"><span data-stu-id="d1834-160">Handles (which are of type D3DXHANDLE) are string pointers.</span></span> <span data-ttu-id="d1834-161">傳遞至函式（例如 GetParameterxxx 或 GetAnnotationxxx）的控制碼可以是下列三種形式的其中一種：</span><span class="sxs-lookup"><span data-stu-id="d1834-161">The handles that are passed into functions such as GetParameterxxx or GetAnnotationxxx can be in one of three forms:</span></span>

-   <span data-ttu-id="d1834-162">函數所傳回的控制碼，例如 GetParameterxxx。</span><span class="sxs-lookup"><span data-stu-id="d1834-162">A handle returned by a function such as GetParameterxxx.</span></span>
-   <span data-ttu-id="d1834-163">字串，其中包含參數、技術、傳遞或注釋的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1834-163">A string containing the name of the parameter, technique, pass, or annotation.</span></span>
-   <span data-ttu-id="d1834-164">控制碼設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d1834-164">A handle set to **NULL**.</span></span>

<span data-ttu-id="d1834-165">此範例會將控制碼傳回給已附加 WORLDVIEWPROJ 語義的參數：</span><span class="sxs-lookup"><span data-stu-id="d1834-165">This example returns a handle to the parameter that has the WORLDVIEWPROJ semantic attached to it:</span></span>


```
D3DHANDLE handle = 
    m_pEffect->GetParameterBySemantic(NULL, "WORLDVIEWPROJ");
```



## <a name="add-parameter-information-with-annotations"></a><span data-ttu-id="d1834-166">使用批註新增參數資訊</span><span class="sxs-lookup"><span data-stu-id="d1834-166">Add Parameter Information with Annotations</span></span>

<span data-ttu-id="d1834-167">批註是使用者特定的資料，可附加至任何技術、傳遞或參數。</span><span class="sxs-lookup"><span data-stu-id="d1834-167">Annotations are user-specific data that can be attached to any technique, pass, or parameter.</span></span> <span data-ttu-id="d1834-168">批註是將資訊新增至個別參數的彈性方式。</span><span class="sxs-lookup"><span data-stu-id="d1834-168">An annotation is a flexible way to add information to individual parameters.</span></span> <span data-ttu-id="d1834-169">您可以使用應用程式選擇的任何方式來讀回信息。</span><span class="sxs-lookup"><span data-stu-id="d1834-169">The information can be read back and used any way the application chooses.</span></span> <span data-ttu-id="d1834-170">批註可以是任何資料類型，而且可以動態加入。</span><span class="sxs-lookup"><span data-stu-id="d1834-170">An annotation can be of any data type and can be added dynamically.</span></span> <span data-ttu-id="d1834-171">批註宣告是以角括弧分隔。</span><span class="sxs-lookup"><span data-stu-id="d1834-171">Annotation declarations are delimited by angle brackets.</span></span> <span data-ttu-id="d1834-172">批註包含：</span><span class="sxs-lookup"><span data-stu-id="d1834-172">An annotation contains:</span></span>

-   <span data-ttu-id="d1834-173">資料類型。</span><span class="sxs-lookup"><span data-stu-id="d1834-173">A data type.</span></span>
-   <span data-ttu-id="d1834-174">變數名稱。</span><span class="sxs-lookup"><span data-stu-id="d1834-174">A variable name.</span></span>
-   <span data-ttu-id="d1834-175">等號 (=) 。</span><span class="sxs-lookup"><span data-stu-id="d1834-175">An equals sign (=).</span></span>
-   <span data-ttu-id="d1834-176">資料值。</span><span class="sxs-lookup"><span data-stu-id="d1834-176">The data value.</span></span>
-   <span data-ttu-id="d1834-177">結束分號 (; ) 。</span><span class="sxs-lookup"><span data-stu-id="d1834-177">A ending semicolon (;).</span></span>

<span data-ttu-id="d1834-178">比方說，這份檔中的上述兩個範例都包含這個批註：</span><span class="sxs-lookup"><span data-stu-id="d1834-178">For instance, both of the previous examples in this paper contain this annotation:</span></span>


```
texture Tex0 < string name = "tiger.bmp"; >;
```



<span data-ttu-id="d1834-179">批註會附加至材質物件，並指定應該用來初始化材質物件的材質檔。</span><span class="sxs-lookup"><span data-stu-id="d1834-179">The annotation is attached to the texture object and specifies the texture file that should be used to initialize the texture object.</span></span> <span data-ttu-id="d1834-180">批註不會初始化材質物件，它只是附加至變數的一段使用者資訊。</span><span class="sxs-lookup"><span data-stu-id="d1834-180">The annotation does not initialize the texture object, it is simply a piece of user information that is attached to the variable.</span></span> <span data-ttu-id="d1834-181">應用程式可以使用 [**ID3DXBaseEffect：： GetAnnotation**](id3dxbaseeffect--getannotation.md) 或 [**ID3DXBaseEffect：： GetAnnotationByName**](id3dxbaseeffect--getannotationbyname.md) 來讀取注釋，以傳回字串。</span><span class="sxs-lookup"><span data-stu-id="d1834-181">An application can read the annotation with either [**ID3DXBaseEffect::GetAnnotation**](id3dxbaseeffect--getannotation.md) or [**ID3DXBaseEffect::GetAnnotationByName**](id3dxbaseeffect--getannotationbyname.md) to return the string.</span></span> <span data-ttu-id="d1834-182">應用程式也可以新增批註。</span><span class="sxs-lookup"><span data-stu-id="d1834-182">Annotations can also be added by the application.</span></span>

<span data-ttu-id="d1834-183">每個批註：</span><span class="sxs-lookup"><span data-stu-id="d1834-183">Each annotation:</span></span>

-   <span data-ttu-id="d1834-184">必須是數值或字串。</span><span class="sxs-lookup"><span data-stu-id="d1834-184">Must be either numeric or strings.</span></span>
-   <span data-ttu-id="d1834-185">必須一律以預設值初始化。</span><span class="sxs-lookup"><span data-stu-id="d1834-185">Must always be initialized with a default value.</span></span>
-   <span data-ttu-id="d1834-186">可以與技術建立關聯 [，並將 (Direct3D 9) ](techniques-and-passes.md) 和最上層 [效果參數](/previous-versions/windows/desktop/ee417539(v=vs.85))傳遞。</span><span class="sxs-lookup"><span data-stu-id="d1834-186">Can be associated with [Techniques and Passes (Direct3D 9)](techniques-and-passes.md) and top-level [Effect Parameters](/previous-versions/windows/desktop/ee417539(v=vs.85)).</span></span>
-   <span data-ttu-id="d1834-187">可以使用 [**ID3DXEffect**](id3dxeffect.md) 或 [**ID3DXEffectCompiler**](id3dxeffectcompiler.md)來寫入和讀取。</span><span class="sxs-lookup"><span data-stu-id="d1834-187">Can be written to and read from with either [**ID3DXEffect**](id3dxeffect.md) or [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span></span>
-   <span data-ttu-id="d1834-188">可以使用 [**ID3DXEffect**](id3dxeffect.md)新增。</span><span class="sxs-lookup"><span data-stu-id="d1834-188">Can be added with [**ID3DXEffect**](id3dxeffect.md).</span></span>
-   <span data-ttu-id="d1834-189">無法在效果內部參考。</span><span class="sxs-lookup"><span data-stu-id="d1834-189">Cannot be referenced inside the effect.</span></span>
-   <span data-ttu-id="d1834-190">不能有子語義或子批註。</span><span class="sxs-lookup"><span data-stu-id="d1834-190">Cannot have sub-semantics or sub-annotations.</span></span>

## <a name="share-effect-parameters"></a><span data-ttu-id="d1834-191">共用效果參數</span><span class="sxs-lookup"><span data-stu-id="d1834-191">Share Effect Parameters</span></span>

<span data-ttu-id="d1834-192">效果參數是在效果中宣告的所有非靜態變數。</span><span class="sxs-lookup"><span data-stu-id="d1834-192">Effect parameters are all the non-static variables declared in an effect.</span></span> <span data-ttu-id="d1834-193">這可能包括全域變數和批註。</span><span class="sxs-lookup"><span data-stu-id="d1834-193">This can include global variables and annotations.</span></span> <span data-ttu-id="d1834-194">您可以使用 "shared" 關鍵字宣告參數，然後使用效果集區來建立效果，以在不同效果之間共用效果參數。</span><span class="sxs-lookup"><span data-stu-id="d1834-194">Effect parameters can be shared between different effects by declaring parameters with the "shared" keyword and then creating the effect with an effect pool.</span></span>

<span data-ttu-id="d1834-195">效果集區包含共用效果參數。</span><span class="sxs-lookup"><span data-stu-id="d1834-195">An effect pool contains shared effect parameters.</span></span> <span data-ttu-id="d1834-196">集區的建立方式是呼叫 [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md)，它會傳回 [**ID3DXEffectPool**](id3dxeffectpool.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="d1834-196">The pool is created by calling [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md), which returns an [**ID3DXEffectPool**](id3dxeffectpool.md) interface.</span></span> <span data-ttu-id="d1834-197">建立效果時，可以將介面提供為任何 D3DXCreateEffectxxx 函數的輸入。</span><span class="sxs-lookup"><span data-stu-id="d1834-197">The interface can be supplied as an input to any of the D3DXCreateEffectxxx functions when an effect is created.</span></span> <span data-ttu-id="d1834-198">若要讓參數跨多個效果共用，參數在每個共用效果中都必須具有相同的名稱、類型和語義。</span><span class="sxs-lookup"><span data-stu-id="d1834-198">For a parameter to be shared across multiple effects, the parameter must have the same name, type, and semantic in each of the shared effects.</span></span>


```
ID3DXEffectPool* g_pEffectPool = NULL;   // Effect pool for sharing parameters

    D3DXCreateEffectPool( &g_pEffectPool );
```



<span data-ttu-id="d1834-199">共用參數必須使用相同裝置的效果。</span><span class="sxs-lookup"><span data-stu-id="d1834-199">Effects that share parameters must use the same device.</span></span> <span data-ttu-id="d1834-200">這會強制執行，以防止在不同裝置上共用裝置相依參數 (例如著色器或紋理) 。</span><span class="sxs-lookup"><span data-stu-id="d1834-200">This is enforced to prevent the sharing of device-dependent parameters (such as shaders or textures) across different devices.</span></span> <span data-ttu-id="d1834-201">只要釋放包含共用參數的效果，就會從集區中刪除參數。</span><span class="sxs-lookup"><span data-stu-id="d1834-201">Parameters are deleted from the pool whenever the effects that contain the shared parameters are released.</span></span> <span data-ttu-id="d1834-202">如果不需要共用參數，則在建立效果時為效果集區提供 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="d1834-202">If sharing parameters is not necessary, supply **NULL** for the effect pool when an effect is created.</span></span>

<span data-ttu-id="d1834-203">複製的效果會使用與複製的效果相同的效果集區。</span><span class="sxs-lookup"><span data-stu-id="d1834-203">Cloned effects use the same effect pool as the effect from which they are cloned.</span></span> <span data-ttu-id="d1834-204">複製效果會產生效果的完整複本，包括全域變數、技術、傳遞和批註。</span><span class="sxs-lookup"><span data-stu-id="d1834-204">Cloning an effect makes an exact copy of an effect, including global variables, techniques, passes, and annotations.</span></span>

## <a name="compile-an-effect-offline"></a><span data-ttu-id="d1834-205">離線編譯效果</span><span class="sxs-lookup"><span data-stu-id="d1834-205">Compile an Effect Offline</span></span>

<span data-ttu-id="d1834-206">您可以使用 [**D3DXCreateEffect**](d3dxcreateeffect.md)在執行時間編譯效果，也可以使用命令列編譯器工具 fxc.exe 離線編譯效果。</span><span class="sxs-lookup"><span data-stu-id="d1834-206">You can compile an effect at run time with [**D3DXCreateEffect**](d3dxcreateeffect.md), or you can compile an effect offline using the command-line compiler tool fxc.exe.</span></span> <span data-ttu-id="d1834-207">[CompiledEffect 範例](https://msdn.microsoft.com/library/Ee416326(v=VS.85).aspx)中的效果包含頂點著色器、圖元著色器和一項技術：</span><span class="sxs-lookup"><span data-stu-id="d1834-207">The effect in the [CompiledEffect Sample](https://msdn.microsoft.com/library/Ee416326(v=VS.85).aspx) contains a vertex shader, a pixel shader, and one technique:</span></span>


```
// File: CompiledEffect.fx

// Global variables
float4 g_MaterialAmbientColor;    // Material's ambient color
...

// Texture samplers
sampler RenderTargetSampler = 
   ...

// Type: Vertex shader                                      
VS_OUTPUT RenderSceneVS( float4 vPos : POSITION, 
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0 )
{
   ...
};
// Type: Pixel shader
PS_OUTPUT RenderScenePS( VS_OUTPUT In ) 
{ 
   ...
}

// Type: Technique                                     
technique RenderScene
{
    pass P0
    {          
        ZENABLE = true;
        VertexShader = compile vs_1_1 RenderSceneVS();
        PixelShader  = compile ps_1_1 RenderScenePS();
    }
}
```



<span data-ttu-id="d1834-208">使用 [效果編譯器工具](../direct3dtools/fxc.md) 來編譯 vs 1 1 的著色器時，會 \_ \_ 產生下列元件著色器指示：</span><span class="sxs-lookup"><span data-stu-id="d1834-208">Using [Effect-Compiler Tool](../direct3dtools/fxc.md) to compile the shader for vs\_1\_1 generated the following assembly shader instructions:</span></span>


```
//
// Generated by Microsoft (R) D3DX9 Shader Compiler 4.09.02.1188
//
//   fxc /T vs_1_1 /E RenderSceneVS /Fc CompiledEffect.txt CompiledEffect.fx
//
//
// Parameters:
//
//   float4 g_LightAmbient;
//   float4 g_LightDiffuse;
//   float3 g_LightDir;
//   float4 g_MaterialAmbientColor;
//   float4 g_MaterialDiffuseColor;
//   float g_fTime;
//   float4x4 g_mWorld;
//   float4x4 g_mWorldViewProjection;
//
//
// Registers:
//
//   Name                   Reg   Size
//   ---------------------- ----- ----
//   g_mWorldViewProjection c0       4
//   g_mWorld               c4       3
//   g_MaterialAmbientColor c7       1
//   g_MaterialDiffuseColor c8       1
//   g_LightDir             c9       1
//   g_LightAmbient         c10      1
//   g_LightDiffuse         c11      1
//   g_fTime                c12      1
//
//
// Default values:
//
//   g_LightDir
//     c9   = { 0.57735, 0.57735, 0.57735, 0 };
//
//   g_LightAmbient
//     c10  = { 1, 1, 1, 1 };
//
//   g_LightDiffuse
//     c11  = { 1, 1, 1, 1 };
//

    vs_1_1
    def c13, 0.159154937, 0.25, 6.28318548, -3.14159274
    def c14, -2.52398507e-007, 2.47609005e-005, -0.00138883968, 0.0416666418
    def c15, -0.5, 1, 0.5, 0
    dcl_position v0
    dcl_normal v1
    dcl_texcoord v2
    mov r0.w, c12.x
    mad r0.w, r0.w, c13.x, c13.y
    expp r3.y, r0.w
    mov r0.w, r3.y
    mad r0.w, r0.w, c13.z, c13.w
    mul r0.w, r0.w, r0.w
    mad r1.w, r0.w, c14.x, c14.y
    mad r1.w, r0.w, r1.w, c14.z
    mad r1.w, r0.w, r1.w, c14.w
    mad r1.w, r0.w, r1.w, c15.x
    mad r0.w, r0.w, r1.w, c15.y
    mul r0.w, r0.w, v0.x
    mul r0.x, r0.w, c15.z
    dp3 r1.x, v1, c4
    dp3 r1.y, v1, c5
    dp3 r1.z, v1, c6
    mov r0.yzw, c15.w
    dp3 r2.x, r1, r1
    add r0, r0, v0
    rsq r1.w, r2.x
    dp4 oPos.x, r0, c0
    mul r1.xyz, r1, r1.w
    dp4 oPos.y, r0, c1
    dp3 r1.x, r1, c9
    dp4 oPos.z, r0, c2
    max r1.w, r1.x, c15.w
    mov r1.xyz, c8
    mul r1.xyz, r1, c11
    mov r2.xyz, c7
    mul r2.xyz, r2, c10
    dp4 oPos.w, r0, c3
    mad oD0.xyz, r1, r1.w, r2
    mov oD0.w, c15.y
    mov oT0.xy, v2

// approximately 34 instruction slots used
```



## <a name="improve-performance-with-preshaders"></a><span data-ttu-id="d1834-209">使用 Preshaders 改善效能</span><span class="sxs-lookup"><span data-stu-id="d1834-209">Improve Performance with Preshaders</span></span>

<span data-ttu-id="d1834-210">Preshader 是藉由預先計算常數著色器運算式來提高著色器效率的技巧。</span><span class="sxs-lookup"><span data-stu-id="d1834-210">A preshader is a technique for increasing shader efficiency by pre-calculating constant shader expressions.</span></span> <span data-ttu-id="d1834-211">效果編譯器會自動從著色器的主體取出著色器計算，並在執行著色器之前的 CPU 上執行它們。</span><span class="sxs-lookup"><span data-stu-id="d1834-211">The effect compiler automatically pulls out shader computations from the body of a shader and executes them on the CPU prior to the shader running.</span></span> <span data-ttu-id="d1834-212">因此，preshaders 只會處理效果。</span><span class="sxs-lookup"><span data-stu-id="d1834-212">Consequently, preshaders only work with effects.</span></span> <span data-ttu-id="d1834-213">比方說，這兩個運算式可以在著色器之外進行評估，然後再執行。</span><span class="sxs-lookup"><span data-stu-id="d1834-213">For instance, these two expressions can be evaluated outside of the shader before it runs.</span></span>


```
mul(World,mul(View, Projection));
sin(time)
```



<span data-ttu-id="d1834-214">可以移動的著色器計算是與統一參數相關聯的計算;也就是說，每個頂點或圖元的計算都不會變更。</span><span class="sxs-lookup"><span data-stu-id="d1834-214">Shader computations that can be moved are those associated with uniform parameters; that is, the computations do not change for each vertex or pixel.</span></span> <span data-ttu-id="d1834-215">如果您使用效果，則效果編譯器會自動為您產生並執行 preshader;沒有可啟用的旗標。</span><span class="sxs-lookup"><span data-stu-id="d1834-215">If you are using effects, the effect compiler automatically generates and runs a preshader for you; there are no flags to enable.</span></span> <span data-ttu-id="d1834-216">Preshaders 可以減少每個著色器的指令數目，也可以減少著色器取用的常數暫存器數目。</span><span class="sxs-lookup"><span data-stu-id="d1834-216">Preshaders can reduce the number of instructions per shader and can also reduce the number of constant registers a shader consumes.</span></span>

<span data-ttu-id="d1834-217">將效果編譯器視為多處理器編譯器的一種，因為它會針對兩種類型的處理器編譯著色器程式碼： CPU 和 GPU。</span><span class="sxs-lookup"><span data-stu-id="d1834-217">Think of the effect compiler as a sort of multi-processor compiler because it compiles shader code for two types of processors: a CPU and a GPU.</span></span> <span data-ttu-id="d1834-218">此外，效果編譯器的設計目的是要將程式碼從 GPU 移到 CPU，進而改善著色器效能。</span><span class="sxs-lookup"><span data-stu-id="d1834-218">In addition, the effect compiler is designed to move code from the GPU to the CPU and therefore improve shader performance.</span></span> <span data-ttu-id="d1834-219">這非常類似于從迴圈中提取靜態運算式。</span><span class="sxs-lookup"><span data-stu-id="d1834-219">This is very similar to pulling a static expression out of a loop.</span></span> <span data-ttu-id="d1834-220">將位置從世界空間轉換成投射空間的著色器，以及複製材質座標在 HLSL 中看起來像這樣：</span><span class="sxs-lookup"><span data-stu-id="d1834-220">A shader that transforms position from world space to projection space, and copies texture coordinates would look like this in HLSL:</span></span>


```
float4x4 g_mWorldViewProjection;    // World * View * Projection matrix
float4x4 g_mWorldInverse;           // Inverse World matrix
float3 g_LightDir;                  // Light direction in world space
float4 g_LightDiffuse;              // Diffuse color of the light

struct VS_OUTPUT
{
    float4 Position   : POSITION;   // vertex position 
    float2 TextureUV  : TEXCOORD0;  // vertex texture coords 
    float4 Diffuse    : COLOR0;     // vertex diffuse color
};

VS_OUTPUT RenderSceneVS( float4 vPos : POSITION, 
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0)
{
    VS_OUTPUT Output;
    
    // Transform the position from object space to projection space
    Output.Position = mul(vPos, g_mWorldViewProjection);

    // Transform the light from world space to object space    
    float3 vLightObjectSpace = normalize(mul(g_LightDir, (float3x3)g_mWorldInverse)); 

    // N dot L lighting
    Output.Diffuse = max(0,dot(vNormal, vLightObjectSpace));
    
    // Copy the texture coordinate
    Output.TextureUV = vTexCoord0; 
    
    return Output;    
}
technique RenderVS
{
    pass P0
    {          
        VertexShader = compile vs_1_1 RenderSceneVS();
    }
}
```



<span data-ttu-id="d1834-221">使用 [效果編譯器工具](../direct3dtools/fxc.md) 來編譯 vs 1 1 的著色器會 \_ \_ 產生下列元件指示：</span><span class="sxs-lookup"><span data-stu-id="d1834-221">Using [Effect-Compiler Tool](../direct3dtools/fxc.md) to compile the shader for vs\_1\_1 generates the following assembly instructions:</span></span>


```
technique RenderVS
{
    pass P0
    {
        vertexshader = 
            asm {
            //
            // Generated by Microsoft (R) D3DX9 Shader Compiler 9.15.779.0000
            //
            // Parameters:
            //
            //   float3 g_LightDir;
            //   float4x4 g_mWorldInverse;
            //   float4x4 g_mWorldViewProjection;
            //
            //
            // Registers:
            //
            //   Name                   Reg   Size
            //   ---------------------- ----- ----
            //   g_mWorldViewProjection c0       4
            //   g_mWorldInverse        c4       3
            //   g_LightDir             c7       1
            //
            
                vs_1_1
                def c8, 0, 0, 0, 0
                dcl_position v0
                dcl_normal v1
                dcl_texcoord v2
                mov r1.xyz, c7
                dp3 r0.x, r1, c4
                dp3 r0.y, r1, c5
                dp3 r0.z, r1, c6
                dp4 oPos.x, v0, c0
                dp3 r1.x, r0, r0
                dp4 oPos.y, v0, c1
                rsq r0.w, r1.x
                dp4 oPos.z, v0, c2
                mul r0.xyz, r0, r0.w
                dp4 oPos.w, v0, c3
                dp3 r0.x, v1, r0
                max oD0, r0.x, c8.x
                mov oT0.xy, v2
            
            // approximately 14 instruction slots used
            };

        //No embedded pixel shader
    }
}
```



<span data-ttu-id="d1834-222">這會使用大約14個插槽，並取用9個常數暫存器。</span><span class="sxs-lookup"><span data-stu-id="d1834-222">This uses up approximately 14 slots and consumes 9 constant registers.</span></span> <span data-ttu-id="d1834-223">使用 preshader 時，編譯器會將靜態運算式移出著色器和 preshader。</span><span class="sxs-lookup"><span data-stu-id="d1834-223">With a preshader, the compiler moves the static expressions out of the shader and into the preshader.</span></span> <span data-ttu-id="d1834-224">使用 preshader 時，相同的著色器看起來像這樣：</span><span class="sxs-lookup"><span data-stu-id="d1834-224">The same shader would look like this with a preshader:</span></span>


```
technique RenderVS
{
    pass P0
    {
        vertexshader = 
            asm {
            //
            // Generated by Microsoft (R) D3DX9 Shader Compiler 9.15.779.0000
            //
            // Parameters:
            //
            //   float3 g_LightDir;
            //   float4x4 g_mWorldInverse;
            //
            //
            // Registers:
            //
            //   Name            Reg   Size
            //   --------------- ----- ----
            //   g_mWorldInverse c0       3
            //   g_LightDir      c3       1
            //
            
                preshader
                dot r0.x, c3.xyz, c0.xyz
                dot r0.y, c3.xyz, c1.xyz
                dot r0.z, c3.xyz, c2.xyz
                dot r1.w, r0.xyz, r0.xyz
                rsq r0.w, r1.w
                mul c4.xyz, r0.w, r0.xyz
            
            // approximately 6 instructions used
            //
            // Generated by Microsoft (R) D3DX9 Shader Compiler 9.15.779.0000
            //
            // Parameters:
            //
            //   float4x4 g_mWorldViewProjection;
            //
            //
            // Registers:
            //
            //   Name                   Reg   Size
            //   ---------------------- ----- ----
            //   g_mWorldViewProjection c0       4
            //
            
                vs_1_1
                def c5, 0, 0, 0, 0
                dcl_position v0
                dcl_normal v1
                dcl_texcoord v2
                dp4 oPos.x, v0, c0
                dp4 oPos.y, v0, c1
                dp4 oPos.z, v0, c2
                dp4 oPos.w, v0, c3
                dp3 r0.x, v1, c4
                max oD0, r0.x, c5.x
                mov oT0.xy, v2
            
            // approximately 7 instruction slots used
            };

        //No embedded pixel shader
    }
}
```



<span data-ttu-id="d1834-225">效果會在執行著色器之前執行 preshader。</span><span class="sxs-lookup"><span data-stu-id="d1834-225">An effect executes a preshader just before executing a shader.</span></span> <span data-ttu-id="d1834-226">結果會與著色器效能增加的功能相同，因為每個頂點或圖元所需執行的指令數目 (，視著色) 器的類型而定，這可能會減少。</span><span class="sxs-lookup"><span data-stu-id="d1834-226">The result is the same functionality with increased shader performance because the number of instructions that need to be executed (for each vertex or pixel depending on the type of shader) has been reduced.</span></span> <span data-ttu-id="d1834-227">此外，著色器會使用較少的常數暫存器，做為將靜態運算式移至 preshader 的結果。</span><span class="sxs-lookup"><span data-stu-id="d1834-227">In addition, fewer constant registers are consumed by the shader as a result of the static expressions being moved to the preshader.</span></span> <span data-ttu-id="d1834-228">這表示，預先著色器先前受限於所需的常數暫存器數目，現在可能會進行編譯，因為它們需要較少的常數暫存器。</span><span class="sxs-lookup"><span data-stu-id="d1834-228">This means that shaders previously limited by the number of constant registers they required may now compile because they require fewer constant registers.</span></span> <span data-ttu-id="d1834-229">從 preshaders 得到5% 的效能和20% 的效能改進相當合理。</span><span class="sxs-lookup"><span data-stu-id="d1834-229">It is reasonable to expect a 5 percent and a 20 percent performance improvement from preshaders.</span></span>

<span data-ttu-id="d1834-230">請記住，輸入常數與 preshader 中的輸出常數不同。</span><span class="sxs-lookup"><span data-stu-id="d1834-230">Keep in mind that the input constants are different from the output constants in a preshader.</span></span> <span data-ttu-id="d1834-231">輸出 c1 與輸入 c1 暫存器不同。</span><span class="sxs-lookup"><span data-stu-id="d1834-231">The output c1 is not the same as the input c1 register.</span></span> <span data-ttu-id="d1834-232">寫入至 preshader 中的常數暫存器實際上會寫入對應的著色器輸入 (常數) 位置。</span><span class="sxs-lookup"><span data-stu-id="d1834-232">Writing to a constant register in a preshader actually writes into the corresponding shader's input (constant) slot.</span></span>


```
// BaseDelta c0 1
// Refinements c1 1
preshader
mul c1.x, c0.x, (-2)
add c0.x, c0.x, c0.x
cmp c5.x, c1.x, (1), (0)
```



<span data-ttu-id="d1834-233">上述的 cmp 指令會讀取 preshader c1 值，而 mul 指令則會寫入至頂點著色器所使用的硬體著色器暫存器。</span><span class="sxs-lookup"><span data-stu-id="d1834-233">The cmp instruction above will read the preshader c1 value, while the mul instruction will write to the hardware shader registers to be used by the vertex shader.</span></span>

## <a name="use-parameter-blocks-to-manage-effect-parameters"></a><span data-ttu-id="d1834-234">使用參數區塊來管理效果參數</span><span class="sxs-lookup"><span data-stu-id="d1834-234">Use Parameter Blocks to Manage Effect Parameters</span></span>

<span data-ttu-id="d1834-235">參數區塊是作用中狀態變更的區塊。</span><span class="sxs-lookup"><span data-stu-id="d1834-235">Parameter blocks are blocks of effect state changes.</span></span> <span data-ttu-id="d1834-236">參數區塊可以記錄狀態變更，以便稍後透過單一呼叫來套用。</span><span class="sxs-lookup"><span data-stu-id="d1834-236">A parameter block can record state changes, so that they can be applied later on with a single call.</span></span> <span data-ttu-id="d1834-237">藉由呼叫 [**ID3DXEffect：： BeginParameterBlock**](id3dxeffect--beginparameterblock.md)來建立參數區塊：</span><span class="sxs-lookup"><span data-stu-id="d1834-237">Create a parameter block by calling [**ID3DXEffect::BeginParameterBlock**](id3dxeffect--beginparameterblock.md):</span></span>


```
    m_pEffect->SetTechnique( "RenderScene" );

    m_pEffect->BeginParameterBlock();
    D3DXVECTOR4 v4( Diffuse.r, Diffuse.g, Diffuse.b, Diffuse.a );
    m_pEffect->SetVector( "g_vDiffuse", &v4 );
    m_pEffect->SetFloat( "g_fReflectivity", fReflectivity );
    m_pEffect->SetFloat( "g_fAnimSpeed", fAnimSpeed );
    m_pEffect->SetFloat( "g_fSizeMul", fSize );
    m_hParameters = m_pEffect->EndParameterBlock();
```



<span data-ttu-id="d1834-238">參數區塊可節省 API 呼叫所套用的四項變更。</span><span class="sxs-lookup"><span data-stu-id="d1834-238">The parameter block saves four changes applied by the API calls.</span></span> <span data-ttu-id="d1834-239">呼叫 [**ID3DXEffect：： BeginParameterBlock**](id3dxeffect--beginparameterblock.md) 會開始記錄狀態變更。</span><span class="sxs-lookup"><span data-stu-id="d1834-239">Calling [**ID3DXEffect::BeginParameterBlock**](id3dxeffect--beginparameterblock.md) starts recording the state changes.</span></span> <span data-ttu-id="d1834-240">[**ID3DXEffect：： EndParameterBlock**](id3dxeffect--endparameterblock.md) 會停止將變更新增至參數區塊，並傳回控制碼。</span><span class="sxs-lookup"><span data-stu-id="d1834-240">[**ID3DXEffect::EndParameterBlock**](id3dxeffect--endparameterblock.md) stops adding the changes to the parameter block and returns a handle.</span></span> <span data-ttu-id="d1834-241">呼叫 [**ID3DXEffect：： ApplyParameterBlock**](id3dxeffect--applyparameterblock.md)時，將會使用此控制碼。</span><span class="sxs-lookup"><span data-stu-id="d1834-241">The handle will be used when calling [**ID3DXEffect::ApplyParameterBlock**](id3dxeffect--applyparameterblock.md).</span></span>

<span data-ttu-id="d1834-242">在 [EffectParam 範例](https://msdn.microsoft.com/library/Ee417535(v=VS.85).aspx)中，參數區塊會套用於轉譯順序中：</span><span class="sxs-lookup"><span data-stu-id="d1834-242">In the [EffectParam Sample](https://msdn.microsoft.com/library/Ee417535(v=VS.85).aspx), the parameter block is applied in the render sequence:</span></span>


```
CObj g_aObj[NUM_OBJS];       // Object instances

    if( SUCCEEDED( pd3dDevice->BeginScene() ) )
    {
        // Set the shared parameters using the first mesh's effect.

        // Render the mesh objects
        for( int i = 0; i < NUM_OBJS; ++i )
        {
            ID3DXEffect *pEffect = g_aObj[i].m_pEffect;

            // Apply the parameters
            pEffect->ApplyParameterBlock( g_aObj[i].m_hParameters );

            ...

            pEffect->Begin( &cPasses, 0 );
            for( iPass = 0; iPass < cPasses; iPass++ )
            {
              ...
            }
            pEffect->End();
        }

        ...
        pd3dDevice->EndScene();
    }
```



<span data-ttu-id="d1834-243">參數區塊會在呼叫 [**ID3DXEffect：： Begin**](id3dxeffect--begin.md) 之前，設定全部四個狀態變更的值。</span><span class="sxs-lookup"><span data-stu-id="d1834-243">The parameter block sets the value of all four of the state changes just before [**ID3DXEffect::Begin**](id3dxeffect--begin.md) is called.</span></span> <span data-ttu-id="d1834-244">參數區塊是使用單一 API 呼叫來設定多個狀態變更的便利方式。</span><span class="sxs-lookup"><span data-stu-id="d1834-244">Parameter blocks are a handy way to set multiple state changes with a single API call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1834-245">相關主題</span><span class="sxs-lookup"><span data-stu-id="d1834-245">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1834-246">影響</span><span class="sxs-lookup"><span data-stu-id="d1834-246">Effects</span></span>](effects.md)
</dt> </dl>

 

 

---
title: " (Direct3D 11) 的效果技巧語法"
description: 效果技術會以本節所述的語法來宣告。
ms.assetid: 54a6ebd1-a6b4-473b-bf53-a3323445de71
keywords:
- technique11，Direct3D 11 效果
- pass，Direct3D 11 效果
- CompileShader，Direct3D 11 效果
- SetStateGroup，Direct3D 11 效果
- SetBlendState，Direct3D 11 效果
- SetDepthStencilState，Direct3D 11 效果
- SetRasterizerState，Direct3D 11 效果
- SetVertexShader，Direct3D 11 效果
- SetGeometryShader，Direct3D 11 效果
- SetPixelShader，Direct3D 11 效果
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73fb668f308869ef9cca5cce99d522f18a287f3c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104092467"
---
# <a name="effect-technique-syntax-direct3d-11"></a><span data-ttu-id="50794-113"> (Direct3D 11) 的效果技巧語法</span><span class="sxs-lookup"><span data-stu-id="50794-113">Effect Technique Syntax (Direct3D 11)</span></span>

<span data-ttu-id="50794-114">效果技術會以本節所述的語法來宣告。</span><span class="sxs-lookup"><span data-stu-id="50794-114">An effect technique is declared with the syntax described in this section.</span></span>

<span data-ttu-id="50794-115">TechniqueVersion *TechniqueName* \[  < *注釋* > \]</span><span class="sxs-lookup"><span data-stu-id="50794-115">TechniqueVersion *TechniqueName* \[ <*Annotations* > \]</span></span>

<span data-ttu-id="50794-116">{</span><span class="sxs-lookup"><span data-stu-id="50794-116">{</span></span>

<dl> <span data-ttu-id="50794-117">傳遞 *PassName* \[  < *注釋* > \]</span><span class="sxs-lookup"><span data-stu-id="50794-117">pass *PassName* \[ <*Annotations* > \]</span></span>  
<span data-ttu-id="50794-118">{</span><span class="sxs-lookup"><span data-stu-id="50794-118">{</span></span>
<dl> <span data-ttu-id="50794-119">\[*SetStateGroup*;\] \[ *SetStateGroup*;\]</span><span class="sxs-lookup"><span data-stu-id="50794-119">\[ *SetStateGroup*; \] \[ *SetStateGroup*; \]</span></span>  
<span data-ttu-id="50794-120">...</span><span class="sxs-lookup"><span data-stu-id="50794-120">...</span></span>  
<span data-ttu-id="50794-121">\[*SetStateGroup*;\]</span><span class="sxs-lookup"><span data-stu-id="50794-121">\[ *SetStateGroup*; \]</span></span>
</dl> </dd> }  
</dl>

<span data-ttu-id="50794-122">}</span><span class="sxs-lookup"><span data-stu-id="50794-122">}</span></span>

## <a name="parameters"></a><span data-ttu-id="50794-123">參數</span><span class="sxs-lookup"><span data-stu-id="50794-123">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="50794-124">項目</span><span class="sxs-lookup"><span data-stu-id="50794-124">Item</span></span></th>
<th><span data-ttu-id="50794-125">描述</span><span class="sxs-lookup"><span data-stu-id="50794-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="50794-126"><span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>TechniqueVersion</span><span class="sxs-lookup"><span data-stu-id="50794-126"><span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>TechniqueVersion</span></span><br/></td>
<td><span data-ttu-id="50794-127">可能是 technique10 或 technique11。</span><span class="sxs-lookup"><span data-stu-id="50794-127">Either technique10 or technique11.</span></span> <span data-ttu-id="50794-128">使用 Direct3D 11 (5_0 著色器、BindInterfaces) 等功能的技術，必須使用 technique11。</span><span class="sxs-lookup"><span data-stu-id="50794-128">Techniques which use functionality new to Direct3D 11 (5_0 shaders, BindInterfaces, etc) must use technique11.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50794-129"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span><em>TechniqueName</em></span><span class="sxs-lookup"><span data-stu-id="50794-129"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span><em>TechniqueName</em></span></span><br/></td>
<td><span data-ttu-id="50794-130">選擇性。</span><span class="sxs-lookup"><span data-stu-id="50794-130">Optional.</span></span> <span data-ttu-id="50794-131">可唯一識別效果技巧名稱的 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="50794-131">An ASCII string that uniquely identifies the name of the effect technique.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="50794-132"><span id="______________Annotations__"></span><span id="______________annotations__"></span><span id="______________ANNOTATIONS__"></span> <<em>注釋</em> ></span><span class="sxs-lookup"><span data-stu-id="50794-132"><span id="______________Annotations__"></span><span id="______________annotations__"></span><span id="______________ANNOTATIONS__"></span> <<em>Annotations</em> ></span></span><br/></td>
<td><span data-ttu-id="50794-133">[in] 選用。</span><span class="sxs-lookup"><span data-stu-id="50794-133">[in] Optional.</span></span> <span data-ttu-id="50794-134"> (中繼資料) 的一或多個使用者提供的資訊，會被效果系統忽略。</span><span class="sxs-lookup"><span data-stu-id="50794-134">One or more pieces of user-supplied information (metadata) that is ignored by the effect system.</span></span> <span data-ttu-id="50794-135">如需語法，請參閱 <a href="d3d11-effect-annotation-syntax.md"> (Direct3D 11) 的批註語法 </a>。</span><span class="sxs-lookup"><span data-stu-id="50794-135">For syntax, see <a href="d3d11-effect-annotation-syntax.md">Annotation Syntax (Direct3D 11)</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50794-136"><span id="pass"></span><span id="PASS"></span>通過</span><span class="sxs-lookup"><span data-stu-id="50794-136"><span id="pass"></span><span id="PASS"></span>pass</span></span><br/></td>
<td><span data-ttu-id="50794-137">必要關鍵字。</span><span class="sxs-lookup"><span data-stu-id="50794-137">Required keyword.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="50794-138"><span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span><em>PassName</em></span><span class="sxs-lookup"><span data-stu-id="50794-138"><span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span><em>PassName</em></span></span><br/></td>
<td><span data-ttu-id="50794-139">[in] 選用。</span><span class="sxs-lookup"><span data-stu-id="50794-139">[in] Optional.</span></span> <span data-ttu-id="50794-140">可唯一識別傳遞名稱的 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="50794-140">An ASCII string that uniquely identifies the name of the pass.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50794-141"><span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span><em>SetStateGroup</em></span><span class="sxs-lookup"><span data-stu-id="50794-141"><span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span><em>SetStateGroup</em></span></span><br/></td>
<td><span data-ttu-id="50794-142">在設定一或多個狀態群組，例如：</span><span class="sxs-lookup"><span data-stu-id="50794-142">[in] Set one or more state groups such as:</span></span> <br/> 
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="50794-143">StateGroup</span><span class="sxs-lookup"><span data-stu-id="50794-143">StateGroup</span></span></th>
<th><span data-ttu-id="50794-144">Syntax</span><span class="sxs-lookup"><span data-stu-id="50794-144">Syntax</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="50794-145">混色狀態</span><span class="sxs-lookup"><span data-stu-id="50794-145">Blend State</span></span></td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetBlendState( arguments ); </code></pre></td>
</tr>
</tbody>
</table>

<p><span data-ttu-id="50794-146">請參閱 [<strong>>id3d11devicecoNtext：： OMSetBlendState</strong>] (引數清單的/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecoNtext-omsetblendstate) 。</span><span class="sxs-lookup"><span data-stu-id="50794-146">See [<strong>ID3D11DeviceContext::OMSetBlendState</strong>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetblendstate) for the argument list.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50794-147">深度樣板狀態</span><span class="sxs-lookup"><span data-stu-id="50794-147">Depth-stencil State</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetDepthStencilState( arguments ); </code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="50794-148">如需引數清單，請參閱 <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate"><strong>>id3d11devicecoNtext：： OMSetDepthStencilState</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="50794-148">See <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate"><strong>ID3D11DeviceContext::OMSetDepthStencilState</strong></a> for the argument list.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="50794-149">轉譯器狀態</span><span class="sxs-lookup"><span data-stu-id="50794-149">Rasterizer State</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetRasterizerState( arguments ); </code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="50794-150">請參閱 [<strong>>id3d11devicecoNtext：： RSSetState</strong>] (引數清單的/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecoNtext-rssetstate) 。</span><span class="sxs-lookup"><span data-stu-id="50794-150">See [<strong>ID3D11DeviceContext::RSSetState</strong>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetstate) for the argument list.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50794-151">著色器狀態</span><span class="sxs-lookup"><span data-stu-id="50794-151">Shader State</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetXXXShader( Shader );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="50794-152">SetXXXShader 是 SetVertexShader、SetDomainShader、SetHullShader、SetGeometryShader、SetPixelShader 或 SetComputeShader (的其中一種，類似于 API 方法 <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader"><strong>>id3d11devicecoNtext：： VSSetShader</strong></a>、 <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader"><strong>>id3d11devicecoNtext：:D ssetshader</strong></a>、 <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader"><strong>>id3d11devicecoNtext：： HSSetShader</strong></a>、 <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gssetshader"><strong>>id3d11devicecoNtext：： GSSetShader</strong></a>、 <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader"><strong>>id3d11devicecoNtext：:P ssetshader</strong></a> 和 <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetshader"><strong>>id3d11devicecoNtext：： CSSetShader</strong></a>) 。</span><span class="sxs-lookup"><span data-stu-id="50794-152">SetXXXShader is one of SetVertexShader, SetDomainShader, SetHullShader, SetGeometryShader, SetPixelShader or SetComputeShader (which are similar to the API methods <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader"><strong>ID3D11DeviceContext::VSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader"><strong>ID3D11DeviceContext::DSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader"><strong>ID3D11DeviceContext::HSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gssetshader"><strong>ID3D11DeviceContext::GSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader"><strong>ID3D11DeviceContext::PSSetShader</strong></a> and <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetshader"><strong>ID3D11DeviceContext::CSSetShader</strong></a>).</span></span></p>
<p><span data-ttu-id="50794-153">著色器是一種著色器變數，可透過許多方式取得：</span><span class="sxs-lookup"><span data-stu-id="50794-153">Shader is a shader variable, which can be obtained in many ways:</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetXXXShader( CompileShader( shader_profile, ShaderFunction( args ) ) );
SetXXXShader( CompileShader( NULL ) );
SetXXXShader( NULL );
SetXXXShader( myShaderVar );
SetXXXShader( myShaderArray[2] );
SetXXXShader( myShaderArray[uIndex] );
SetGeometryShader( ConstructGSWithSO( Shader, strStream0 ) );
SetGeometryShader( ConstructGSWithSO( Shader, strStream0, strStream1, strStream2, strStream3, RastStream ) );</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="50794-154">呈現目標狀態</span><span class="sxs-lookup"><span data-stu-id="50794-154">Render Target State</span></span></td>
<td><span data-ttu-id="50794-155">值為下列其中之一：</span><span class="sxs-lookup"><span data-stu-id="50794-155">One of:</span></span>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetRenderTargets( RTV0, DSV );
SetRenderTargets( RTV0, RTV1, DSV );
...
SetRenderTargets( RTV0, RTV1, RTV2, RTV3, RTV4, RTV5, RTV6, RTV7, DSV );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="50794-156">類似于 <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets"><strong>>id3d11devicecoNtext：： OMSetRenderTargets</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="50794-156">Similar to <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets"><strong>ID3D11DeviceContext::OMSetRenderTargets</strong></a>.</span></span></p></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a><span data-ttu-id="50794-157">範例</span><span class="sxs-lookup"><span data-stu-id="50794-157">Examples</span></span>

<span data-ttu-id="50794-158">此範例會設定混合狀態。</span><span class="sxs-lookup"><span data-stu-id="50794-158">This example sets blending state.</span></span>


```
BlendState NoBlend
{ 
    BlendEnable[0] = False;
};

...

technique10
{
    pass p2 
    {
        ...
        SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
    }
}
```



<span data-ttu-id="50794-159">此範例會設定轉譯器的狀態，以線上框中呈現物件。</span><span class="sxs-lookup"><span data-stu-id="50794-159">This example sets up the rasterizer state to render an object in wireframe.</span></span>


```
RasterizerState rsWireframe { FillMode = WireFrame; };

...

technique10
{
    pass p1 
    {
        ....
        SetRasterizerState( rsWireframe );
    }
}
```



<span data-ttu-id="50794-160">此範例會設定著色器狀態。</span><span class="sxs-lookup"><span data-stu-id="50794-160">This example sets shader state.</span></span>


```
technique10 RenderSceneWithTexture1Light
{
    pass P0
    {
        SetVertexShader( CompileShader( vs_4_0, RenderSceneVS( 1, true, true ) ) );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, RenderScenePS( true ) ) );
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="50794-161">相關主題</span><span class="sxs-lookup"><span data-stu-id="50794-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50794-162">效果格式</span><span class="sxs-lookup"><span data-stu-id="50794-162">Effect Format</span></span>](d3d11-effect-format.md)
</dt> <dt>

[<span data-ttu-id="50794-163"> (Direct3D 11) 的效果群組語法 </span><span class="sxs-lookup"><span data-stu-id="50794-163">Effect Group Syntax (Direct3D 11)</span></span>](d3d11-effect-group-syntax.md)
</dt> <dt>

[<span data-ttu-id="50794-164">效果狀態群組</span><span class="sxs-lookup"><span data-stu-id="50794-164">Effect State Groups</span></span>](d3d11-effect-states.md)
</dt> </dl>

 

 






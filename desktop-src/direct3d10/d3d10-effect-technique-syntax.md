---
description: 效果技術會使用下列語法來宣告。
ms.assetid: 84f9b74d-8397-4cd5-91a0-7f910ba7b19e
title: " (Direct3D 10) 的效果技巧語法"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f781a0e1ea247e9ffae02e6afc9de77c8e0c6b68
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110541"
---
# <a name="effect-technique-syntax-direct3d-10"></a><span data-ttu-id="c9468-103"> (Direct3D 10) 的效果技巧語法</span><span class="sxs-lookup"><span data-stu-id="c9468-103">Effect Technique Syntax (Direct3D 10)</span></span>

<span data-ttu-id="c9468-104">效果技術會使用下列語法來宣告。</span><span class="sxs-lookup"><span data-stu-id="c9468-104">An effect technique is declared with the following syntax.</span></span>

<span data-ttu-id="c9468-105">technique10 *TechniqueName* \[  < *注釋* > \]</span><span class="sxs-lookup"><span data-stu-id="c9468-105">technique10 *TechniqueName* \[ <*Annotations* > \]</span></span>

<span data-ttu-id="c9468-106">{</span><span class="sxs-lookup"><span data-stu-id="c9468-106">{</span></span>

<dl> <span data-ttu-id="c9468-107">傳遞 *PassName* \[  < *注釋* > \]</span><span class="sxs-lookup"><span data-stu-id="c9468-107">pass *PassName* \[ <*Annotations* > \]</span></span>  
<span data-ttu-id="c9468-108">{</span><span class="sxs-lookup"><span data-stu-id="c9468-108">{</span></span>
<dl> <span data-ttu-id="c9468-109">\[*SetStateGroup*;\] \[ *SetStateGroup*;\]</span><span class="sxs-lookup"><span data-stu-id="c9468-109">\[ *SetStateGroup*; \] \[ *SetStateGroup*; \]</span></span>  
<span data-ttu-id="c9468-110">...</span><span class="sxs-lookup"><span data-stu-id="c9468-110">...</span></span>  
<span data-ttu-id="c9468-111">\[*SetStateGroup*;\]</span><span class="sxs-lookup"><span data-stu-id="c9468-111">\[ *SetStateGroup*; \]</span></span>
</dl> </dd> }  
</dl>

<span data-ttu-id="c9468-112">}</span><span class="sxs-lookup"><span data-stu-id="c9468-112">}</span></span>

## <a name="parameters"></a><span data-ttu-id="c9468-113">參數</span><span class="sxs-lookup"><span data-stu-id="c9468-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9468-114"><span id="technique10"></span><span id="TECHNIQUE10"></span>technique10</span><span class="sxs-lookup"><span data-stu-id="c9468-114"><span id="technique10"></span><span id="TECHNIQUE10"></span>technique10</span></span>
</dt> <dd>

<span data-ttu-id="c9468-115">必要關鍵字。</span><span class="sxs-lookup"><span data-stu-id="c9468-115">Required keyword.</span></span>

</dd> <dt>

<span data-ttu-id="c9468-116"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>*TechniqueName*</span><span class="sxs-lookup"><span data-stu-id="c9468-116"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>*TechniqueName*</span></span>
</dt> <dd>

<span data-ttu-id="c9468-117">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c9468-117">Optional.</span></span> <span data-ttu-id="c9468-118">可唯一識別效果技巧名稱的 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="c9468-118">An ASCII string that uniquely identifies the name of the effect technique.</span></span>

</dd> <dt>

<span data-ttu-id="c9468-119"><span id="Annotations"></span><span id="annotations"></span><span id="ANNOTATIONS"></span>*注釋*</span><span class="sxs-lookup"><span data-stu-id="c9468-119"><span id="Annotations"></span><span id="annotations"></span><span id="ANNOTATIONS"></span>*Annotations*</span></span>
</dt> <dd>

<span data-ttu-id="c9468-120">\[（ \] 選擇性）。</span><span class="sxs-lookup"><span data-stu-id="c9468-120">\[in\] Optional.</span></span> <span data-ttu-id="c9468-121"> (中繼資料) 的一或多個使用者提供的資訊，會被效果系統忽略。</span><span class="sxs-lookup"><span data-stu-id="c9468-121">One or more pieces of user-supplied information (metadata) that is ignored by the effect system.</span></span> <span data-ttu-id="c9468-122">如需語法，請參閱 [ (Direct3D 10) 的批註語法 ](d3d10-effect-annotation-syntax.md)。</span><span class="sxs-lookup"><span data-stu-id="c9468-122">For syntax, see [Annotation Syntax (Direct3D 10)](d3d10-effect-annotation-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9468-123"><span id="pass"></span><span id="PASS"></span>通過</span><span class="sxs-lookup"><span data-stu-id="c9468-123"><span id="pass"></span><span id="PASS"></span>pass</span></span>
</dt> <dd>

<span data-ttu-id="c9468-124">必要關鍵字。</span><span class="sxs-lookup"><span data-stu-id="c9468-124">Required keyword.</span></span>

</dd> <dt>

<span data-ttu-id="c9468-125"><span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span>*PassName*</span><span class="sxs-lookup"><span data-stu-id="c9468-125"><span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span>*PassName*</span></span>
</dt> <dd>

<span data-ttu-id="c9468-126">\[（ \] 選擇性）。</span><span class="sxs-lookup"><span data-stu-id="c9468-126">\[in\] Optional.</span></span> <span data-ttu-id="c9468-127">可唯一識別傳遞名稱的 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="c9468-127">An ASCII string that uniquely identifies the name of the pass.</span></span>

</dd> <dt>

<span data-ttu-id="c9468-128"><span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span>*SetStateGroup*</span><span class="sxs-lookup"><span data-stu-id="c9468-128"><span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span>*SetStateGroup*</span></span>
</dt> <dd>

<span data-ttu-id="c9468-129">\[在中， \] 設定一或多個狀態群組，例如：</span><span class="sxs-lookup"><span data-stu-id="c9468-129">\[in\] Set one or more state groups such as:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c9468-130">StateGroup</span><span class="sxs-lookup"><span data-stu-id="c9468-130">StateGroup</span></span></th>
<th><span data-ttu-id="c9468-131">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9468-131">Syntax</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c9468-132">混色狀態</span><span class="sxs-lookup"><span data-stu-id="c9468-132">Blend State</span></span></td>
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

<p><span data-ttu-id="c9468-133">如需引數清單，請參閱 [<strong>OMSetBlendState</strong>] (/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetblendstate) 。</span><span class="sxs-lookup"><span data-stu-id="c9468-133">See [<strong>OMSetBlendState</strong>](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetblendstate) for the argument list.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9468-134">深度樣板狀態</span><span class="sxs-lookup"><span data-stu-id="c9468-134">Depth-stencil State</span></span></td>
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
<p><span data-ttu-id="c9468-135">如需引數清單，請參閱 <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetdepthstencilstate"><strong>OMSetDepthStencilState</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="c9468-135">See <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetdepthstencilstate"><strong>OMSetDepthStencilState</strong></a> for the argument list.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9468-136">轉譯器狀態</span><span class="sxs-lookup"><span data-stu-id="c9468-136">Rasterizer State</span></span></td>
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
<p><span data-ttu-id="c9468-137">如需引數清單，請參閱 [<strong>RSSetState</strong>] (/windows/desktop/api/D3D10/nf-d3d10-id3d10device-rssetstate) 。</span><span class="sxs-lookup"><span data-stu-id="c9468-137">See [<strong>RSSetState</strong>](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-rssetstate) for the argument list.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9468-138">著色器狀態</span><span class="sxs-lookup"><span data-stu-id="c9468-138">Shader State</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetXXXShader( CompileShader( shader_profile, ShaderFunction( args ) ) );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="c9468-139">或</span><span class="sxs-lookup"><span data-stu-id="c9468-139">or</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetXXXShader( CompileShader( NULL ) );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="c9468-140">或</span><span class="sxs-lookup"><span data-stu-id="c9468-140">or</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetXXXShader( NULL );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="c9468-141">SetXXXShader 是 <strong>SetVertexShader</strong>、 <strong>SetGeometryShader</strong>或 <strong>SetPixelShader</strong> (的其中一種，類似于 API 方法 <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader"><strong>VSSetShader</strong></a>、 <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetshader"><strong>GSSetShader</strong></a>和 <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetshader"><strong>pssetshade</strong></a>) 。</span><span class="sxs-lookup"><span data-stu-id="c9468-141">SetXXXShader is one of <strong>SetVertexShader</strong>, <strong>SetGeometryShader</strong>, or <strong>SetPixelShader</strong> (which are similar to the API methods <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader"><strong>VSSetShader</strong></a>, <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetshader"><strong>GSSetShader</strong></a>, and <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetshader"><strong>PSSetShader</strong></a>).</span></span></p></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

<span data-ttu-id="c9468-142">效果狀態群組會以 [作用狀態](d3d10-effect-states.md)列出。</span><span class="sxs-lookup"><span data-stu-id="c9468-142">Effect state groups are listed in [effect state](d3d10-effect-states.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c9468-143">範例</span><span class="sxs-lookup"><span data-stu-id="c9468-143">Examples</span></span>

<span data-ttu-id="c9468-144">此範例會從 [CubeMapGS 範例](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx) () 設定混合狀態。</span><span class="sxs-lookup"><span data-stu-id="c9468-144">This example (from [CubeMapGS sample](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) sets blending state.</span></span>


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



<span data-ttu-id="c9468-145">此範例會設定轉譯器的狀態，以線上框中呈現物件。</span><span class="sxs-lookup"><span data-stu-id="c9468-145">This example sets up the rasterizer state to render an object in wireframe.</span></span>


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



<span data-ttu-id="c9468-146">此範例會從 [BasicHLSL10 範例](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)) 設定著色器狀態 (;它會使用頂點和圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="c9468-146">This example sets shader state (from [BasicHLSL10 sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)); which uses a vertex and pixel shader.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="c9468-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="c9468-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9468-148">效果格式</span><span class="sxs-lookup"><span data-stu-id="c9468-148">Effect Format</span></span>](d3d10-effect-format.md)
</dt> </dl>

 

 




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
# <a name="effect-technique-syntax-direct3d-11"></a> (Direct3D 11) 的效果技巧語法

效果技術會以本節所述的語法來宣告。

TechniqueVersion *TechniqueName* \[  < *注釋* > \]

{

<dl> 傳遞 *PassName* \[  < *注釋* > \]  
{
<dl> \[*SetStateGroup*;\] \[ *SetStateGroup*;\]  
...  
\[*SetStateGroup*;\]
</dl> </dd> }  
</dl>

}

## <a name="parameters"></a>參數



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>項目</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>TechniqueVersion<br/></td>
<td>可能是 technique10 或 technique11。 使用 Direct3D 11 (5_0 著色器、BindInterfaces) 等功能的技術，必須使用 technique11。<br/></td>
</tr>
<tr class="even">
<td><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span><em>TechniqueName</em><br/></td>
<td>選擇性。 可唯一識別效果技巧名稱的 ASCII 字串。<br/></td>
</tr>
<tr class="odd">
<td><span id="______________Annotations__"></span><span id="______________annotations__"></span><span id="______________ANNOTATIONS__"></span> <<em>注釋</em> ><br/></td>
<td>[in] 選用。  (中繼資料) 的一或多個使用者提供的資訊，會被效果系統忽略。 如需語法，請參閱 <a href="d3d11-effect-annotation-syntax.md"> (Direct3D 11) 的批註語法 </a>。<br/></td>
</tr>
<tr class="even">
<td><span id="pass"></span><span id="PASS"></span>通過<br/></td>
<td>必要關鍵字。<br/></td>
</tr>
<tr class="odd">
<td><span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span><em>PassName</em><br/></td>
<td>[in] 選用。 可唯一識別傳遞名稱的 ASCII 字串。<br/></td>
</tr>
<tr class="even">
<td><span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span><em>SetStateGroup</em><br/></td>
<td>在設定一或多個狀態群組，例如： <br/> 
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>StateGroup</th>
<th>Syntax</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>混色狀態</td>
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

<p>請參閱 [<strong>>id3d11devicecoNtext：： OMSetBlendState</strong>] (引數清單的/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecoNtext-omsetblendstate) 。</p></td>
</tr>
<tr class="even">
<td>深度樣板狀態</td>
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
<p>如需引數清單，請參閱 <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate"><strong>>id3d11devicecoNtext：： OMSetDepthStencilState</strong></a> 。</p></td>
</tr>
<tr class="odd">
<td>轉譯器狀態</td>
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
<p>請參閱 [<strong>>id3d11devicecoNtext：： RSSetState</strong>] (引數清單的/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecoNtext-rssetstate) 。</p></td>
</tr>
<tr class="even">
<td>著色器狀態</td>
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
<p>SetXXXShader 是 SetVertexShader、SetDomainShader、SetHullShader、SetGeometryShader、SetPixelShader 或 SetComputeShader (的其中一種，類似于 API 方法 <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader"><strong>>id3d11devicecoNtext：： VSSetShader</strong></a>、 <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader"><strong>>id3d11devicecoNtext：:D ssetshader</strong></a>、 <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader"><strong>>id3d11devicecoNtext：： HSSetShader</strong></a>、 <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gssetshader"><strong>>id3d11devicecoNtext：： GSSetShader</strong></a>、 <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader"><strong>>id3d11devicecoNtext：:P ssetshader</strong></a> 和 <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetshader"><strong>>id3d11devicecoNtext：： CSSetShader</strong></a>) 。</p>
<p>著色器是一種著色器變數，可透過許多方式取得：</p>
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
<td>呈現目標狀態</td>
<td>值為下列其中之一：
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
<p>類似于 <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets"><strong>>id3d11devicecoNtext：： OMSetRenderTargets</strong></a>。</p></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a>範例

此範例會設定混合狀態。


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



此範例會設定轉譯器的狀態，以線上框中呈現物件。


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



此範例會設定著色器狀態。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[效果格式](d3d11-effect-format.md)
</dt> <dt>

[ (Direct3D 11) 的效果群組語法 ](d3d11-effect-group-syntax.md)
</dt> <dt>

[效果狀態群組](d3d11-effect-states.md)
</dt> </dl>

 

 






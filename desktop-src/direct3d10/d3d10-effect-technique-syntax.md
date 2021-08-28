---
description: 效果技術會使用下列語法來宣告。
ms.assetid: 84f9b74d-8397-4cd5-91a0-7f910ba7b19e
title: " (Direct3D 10) 的效果技巧語法"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 106abd47e1148ce30127733f113a1b43a0058f60
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625124"
---
# <a name="effect-technique-syntax-direct3d-10"></a> (Direct3D 10) 的效果技巧語法

效果技術會使用下列語法來宣告。

technique10 *TechniqueName* \[  < *注釋* > \]

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

<dl> <dt>

<span id="technique10"></span><span id="TECHNIQUE10"></span>technique10
</dt> <dd>

必要關鍵字。

</dd> <dt>

<span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>*TechniqueName*
</dt> <dd>

選擇性。 可唯一識別效果技巧名稱的 ASCII 字串。

</dd> <dt>

<span id="Annotations"></span><span id="annotations"></span><span id="ANNOTATIONS"></span>*注釋*
</dt> <dd>

\[（ \] 選擇性）。  (中繼資料) 的一或多個使用者提供的資訊，會被效果系統忽略。 如需語法，請參閱 [ (Direct3D 10) 的批註語法 ](d3d10-effect-annotation-syntax.md)。

</dd> <dt>

<span id="pass"></span><span id="PASS"></span>通過
</dt> <dd>

必要關鍵字。

</dd> <dt>

<span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span>*PassName*
</dt> <dd>

\[（ \] 選擇性）。 可唯一識別傳遞名稱的 ASCII 字串。

</dd> <dt>

<span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span>*SetStateGroup*
</dt> <dd>

\[在中， \] 設定一或多個狀態群組，例如：



<table>
<colgroup>
<col  />
<col  />
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
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetBlendState( arguments ); </code></pre></td>
</tr>
</tbody>
</table>

<p>如需引數清單，請參閱 [<strong>OMSetBlendState</strong>] (/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetblendstate) 。</p></td>
</tr>
<tr class="even">
<td>深度樣板狀態</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetDepthStencilState( arguments ); </code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>如需引數清單，請參閱 <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetdepthstencilstate"><strong>OMSetDepthStencilState</strong></a> 。</p></td>
</tr>
<tr class="odd">
<td>轉譯器狀態</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetRasterizerState( arguments ); </code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>如需引數清單，請參閱 [<strong>RSSetState</strong>] (/windows/desktop/api/D3D10/nf-d3d10-id3d10device-rssetstate) 。</p></td>
</tr>
<tr class="even">
<td>著色器狀態</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetXXXShader( CompileShader( shader_profile, ShaderFunction( args ) ) );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>或</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetXXXShader( CompileShader( NULL ) );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>或</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetXXXShader( NULL );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>SetXXXShader 是 <strong>SetVertexShader</strong>、 <strong>SetGeometryShader</strong>或 <strong>SetPixelShader</strong> (的其中一種，類似于 API 方法 <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader"><strong>VSSetShader</strong></a>、 <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetshader"><strong>GSSetShader</strong></a>和 <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetshader"><strong>pssetshade</strong></a>) 。</p></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

效果狀態群組會以 [作用狀態](d3d10-effect-states.md)列出。

## <a name="examples"></a>範例

此範例會從 [CubeMapGS 範例](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx) () 設定混合狀態。


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



此範例會從 [BasicHLSL10 範例](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)) 設定著色器狀態 (;它會使用頂點和圖元著色器。


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

[效果格式](d3d10-effect-format.md)
</dt> </dl>

 

 




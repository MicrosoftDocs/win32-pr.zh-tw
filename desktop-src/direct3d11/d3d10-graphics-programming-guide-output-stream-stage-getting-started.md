---
title: 使用 Stream-Output 階段開始使用
description: 本節說明如何搭配資料流程輸出階段使用幾何著色器。
ms.assetid: 37146486-5922-4833-850c-cc4a51de0957
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f00b469b28601322358f348de98354f15263483
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122621874"
---
# <a name="getting-started-with-the-stream-output-stage"></a>使用 Stream-Output 階段開始使用

本節說明如何搭配資料流程輸出階段使用幾何著色器。

## <a name="compile-a-geometry-shader"></a>編譯幾何著色器

這個幾何著色器 (GS) 計算每個三角形的臉部，以及輸出位置、正常和材質座標資料。


```
struct GSPS_INPUT
{
    float4 Pos : SV_POSITION;
    float3 Norm : TEXCOORD0;
    float2 Tex : TEXCOORD1;
};

[maxvertexcount(12)]
void GS( triangle GSPS_INPUT input[3], inout TriangleStream<GSPS_INPUT> TriStream )
{
    GSPS_INPUT output;
    
    //
    // Calculate the face normal
    //
    float3 faceEdgeA = input[1].Pos - input[0].Pos;
    float3 faceEdgeB = input[2].Pos - input[0].Pos;
    float3 faceNormal = normalize( cross(faceEdgeA, faceEdgeB) );
    float3 ExplodeAmt = faceNormal*Explode;
    
    //
    // Calculate the face center
    //
    float3 centerPos = (input[0].Pos.xyz + input[1].Pos.xyz + input[2].Pos.xyz)/3.0;
    float2 centerTex = (input[0].Tex + input[1].Tex + input[2].Tex)/3.0;
    centerPos += faceNormal*Explode;
    
    //
    // Output the pyramid
    //
    for( int i=0; i<3; i++ )
    {
        output.Pos = input[i].Pos + float4(ExplodeAmt,0);
        output.Pos = mul( output.Pos, View );
        output.Pos = mul( output.Pos, Projection );
        output.Norm = input[i].Norm;
        output.Tex = input[i].Tex;
        TriStream.Append( output );
        
        int iNext = (i+1)%3;
        output.Pos = input[iNext].Pos + float4(ExplodeAmt,0);
        output.Pos = mul( output.Pos, View );
        output.Pos = mul( output.Pos, Projection );
        output.Norm = input[iNext].Norm;
        output.Tex = input[iNext].Tex;
        TriStream.Append( output );
        
        output.Pos = float4(centerPos,1) + float4(ExplodeAmt,0);
        output.Pos = mul( output.Pos, View );
        output.Pos = mul( output.Pos, Projection );
        output.Norm = faceNormal;
        output.Tex = centerTex;
        TriStream.Append( output );
        
        TriStream.RestartStrip();
    }
    
    for( int i=2; i>=0; i-- )
    {
        output.Pos = input[i].Pos + float4(ExplodeAmt,0);
        output.Pos = mul( output.Pos, View );
        output.Pos = mul( output.Pos, Projection );
        output.Norm = -input[i].Norm;
        output.Tex = input[i].Tex;
        TriStream.Append( output );
    }
    TriStream.RestartStrip();
}
```



記住這段程式碼，請考慮幾何著色器看起來很像頂點或圖元著色器，但有下列例外狀況：函式傳回的類型、輸入參數宣告，以及內建函式。



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Item</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Function_return_type"></span><span id="function_return_type"></span><span id="FUNCTION_RETURN_TYPE"></span>函數傳回類型<br/></td>
<td>函式傳回類型會執行其中一項工作，宣告著色器可以輸出的最大頂點數目。 在此情況下， <span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>maxvertexcount(12)</code></pre></td>
</tr>
</tbody>
</table>

定義最多12個頂點的輸出。</td>
</tr>
<tr class="even">
<td><p><span id="Input_parameter_declarations"></span><span id="input_parameter_declarations"></span><span id="INPUT_PARAMETER_DECLARATIONS"></span>輸入參數聲明</p></td>
<td><p>此函式會採用兩個輸入參數：</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>triangle GSPS_INPUT input[3] , inout TriangleStream&lt;GSPS_INPUTT&gt; TriStream</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>第一個參數是頂點 (3 的陣列，在此案例中) 由 GSPS_INPUT 結構定義， (會將每個頂點的資料定義為位置、一般和材質座標) 。 第一個參數也會使用三角形關鍵字，這表示輸入組合語言階段必須將資料輸出到幾何著色器，做為其中一個三角形基本型別 (三角形清單或三角形帶狀) 。</p>
<p>第二個參數是由型別 TriangleStream GSPS_INPUTT 所定義的三角形資料流程 &lt; &gt; 。 這表示參數是三角形的陣列，其中每個都是由三個頂點組成 (其中包含 GSPS_INPUT) 成員的資料。</p>
<p>使用三角形和 trianglestream 關鍵字來識別 GS 中的個別三角形或三角形串流。</p></td>
</tr>
<tr class="odd">
<td><p><span id="Intrinsic_function"></span><span id="intrinsic_function"></span><span id="INTRINSIC_FUNCTION"></span>內建函式</p></td>
<td><p>著色器函式中的程式程式碼會使用常見的著色器核心 HLSL 內建函式，但最後兩行除外，其會呼叫 Append 和 RestartStrip。 這些函式僅適用于幾何著色器。 附加會告知幾何著色器將輸出附加至目前的區域：RestartStrip 會建立新的基本帶狀。 每次叫用 GS 階段時，會隱含地建立新的帶狀。</p></td>
</tr>
</tbody>
</table>



 

著色器的其餘部分看起來非常類似頂點或圖元著色器。 幾何著色器會使用結構來宣告輸入參數，並使用 SV 位置語義來標記位置成員， \_ 以告訴硬體此為位置資料。 輸入結構會將其他兩個輸入參數識別為材質座標 (，即使其中一個參數會包含臉部正常) 。 如果您想要的話，您可以使用自己的自訂語義作為一般臉部。

設計幾何著色器之後，請呼叫 [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) 進行編譯，如下列程式碼範例所示。


```
DWORD dwShaderFlags = D3DCOMPILE_ENABLE_STRICTNESS;
ID3DBlob** ppShader;

D3DCompile( pSrcData, sizeof( pSrcData ), 
  "Tutorial13.fx", NULL, NULL, "GS", "gs_4_0", 
  dwShaderFlags, 0, &ppShader, NULL );
```



就像頂點和圖元著色器一樣，您需要著色器旗標來告訴編譯器如何將著色器編譯 (進行偵錯工具、針對速度優化，以及在) 、進入點函數和著色器模型進行驗證。 此範例會使用 GS 函數，建立從 Tutorial13 檔案建立的幾何著色器。 著色器會針對著色器模型4.0 進行編譯。

## <a name="create-a-geometry-shader-object-with-stream-output"></a>使用資料流程輸出建立 Geometry-Shader 物件

一旦您知道將會從幾何串流資料，而且您已成功編譯著色器，下一步就是呼叫 [**ID3D11Device：： CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) 來建立幾何著色器物件。

但首先，您需要宣告流輸出 (因此) 階段輸入簽章。 此簽章符合或驗證 GS 輸出，以及在建立物件時的輸入。 下列程式碼是宣告的範例。


```
D3D11_SO_DECLARATION_ENTRY pDecl[] =
{
    // semantic name, semantic index, start component, component count, output slot
    { "SV_POSITION", 0, 0, 4, 0 },   // output all components of position
    { "TEXCOORD0", 0, 0, 3, 0 },     // output the first 3 of the normal
    { "TEXCOORD1", 0, 0, 2, 0 },     // output the first 2 texture coordinates
};

D3D11Device->CreateGeometryShaderWithStreamOut( pShaderBytecode, ShaderBytecodesize, pDecl, 
    sizeof(pDecl), NULL, 0, 0, NULL, &pStreamOutGS );
```



此函式會採用數個參數，包括：

-   已編譯之幾何著色器的指標 (或頂點著色器的指標，如果沒有幾何著色器，將會直接從頂點著色器) 串流資料。 如需如何取得這個指標的詳細資訊，請參閱 [取得已編譯著色器的指標](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-using-shaders-10)。
-   宣告陣列的指標，這些宣告會描述資料流程輸出階段的輸入資料。  (，請參閱 D3D11 的宣告 [**\_ \_ \_ 專案**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_so_declaration_entry)。 ) 您可以提供最多64的宣告，每個不同類型的元素都要從該階段輸出。 宣告專案的陣列描述資料版面配置，不論是否只針對資料流程輸出系結單一緩衝區或多個緩衝區。
-   由這個階段所寫出的元素數目。
-   幾何著色器物件的指標，該物件是建立 (請參閱 [**ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader)) 。

在這種情況下，緩衝區跨距為 Null，要傳送給轉譯器的資料流程索引為0，而類別連結介面為 Null。

資料流程輸出宣告會定義將資料寫入緩衝區資源的方式。 您可以將所需數量的元件加入至輸出宣告。 您可以使用此階段來寫入單一緩衝區資源或許多緩衝區資源。 針對單一緩衝區，此階段可以為每個頂點撰寫許多不同的元素。 針對多個緩衝區，此階段只能將每個頂點資料的單一元素寫入至每個緩衝區。

若要在不使用幾何著色器的情況下使用此階段，請呼叫 [**ID3D11Device：： CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) ，並將指向頂點著色器的指標傳遞至 *pShaderBytecode* 參數。

## <a name="set-the-output-targets"></a>設定輸出目標

最後一個步驟是設定暫存緩衝區。 資料可以串流至記憶體中的一或多個緩衝區，以供稍後使用。 下列程式碼示範如何建立可用於頂點資料的單一緩衝區，以及要將資料串流至的這個階段。


```
ID3D11Buffer *m_pBuffer;
int m_nBufferSize = 1000000;

D3D11_BUFFER_DESC bufferDesc =
{
    m_nBufferSize,
    D3D11_USAGE_DEFAULT,
    D3D11_BIND_STREAM_OUTPUT,
    0,
    0,
    0
};
D3D11Device->CreateBuffer( &bufferDesc, NULL, &m_pBuffer );
```



藉由呼叫 [**ID3D11Device：： CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer)來建立緩衝區。 此範例說明預設使用方式，這通常適用于預期會由 CPU 相當頻繁更新的緩衝區資源。 系結旗標會識別資源可以系結的管線階段。 使用系結旗標 D3D10 系結資料流程輸出時，也必須使用系結旗標來建立此階段所使用的任何資源 \_ \_ \_ 。

成功建立緩衝區之後，藉由呼叫 [**>id3d11devicecoNtext：： SOSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets)，將它設定為目前的裝置：


```
UINT offset[1] = 0;
D3D11Device->SOSetTargets( 1, &m_pBuffer, offset );
```



此呼叫會採用緩衝區數目、緩衝區的指標，以及位移的陣列 (每個緩衝區的一個位移，指出開始寫入資料的位置) 。 呼叫 draw 函式時，資料會寫入至這些資料流程輸出緩衝區。 內部變數會追蹤開始將資料寫入串流輸出緩衝區的位置，而變數會繼續遞增，直到再次呼叫 [**SOSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets) 並指定新的位移值為止。

所有寫入目標緩衝區的資料都將是32位值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[資料流程-輸出階段](d3d10-graphics-programming-guide-output-stream-stage.md)
</dt> </dl>

 


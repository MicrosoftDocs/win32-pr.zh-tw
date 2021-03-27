---
title: 使用 Stream-Output 階段開始使用
description: 本節說明如何搭配資料流程輸出階段使用幾何著色器。
ms.assetid: 37146486-5922-4833-850c-cc4a51de0957
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 909b3ba37e8b80201a4afc3e5bf18f016fed38a0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971741"
---
# <a name="getting-started-with-the-stream-output-stage"></a><span data-ttu-id="93be1-103">使用 Stream-Output 階段開始使用</span><span class="sxs-lookup"><span data-stu-id="93be1-103">Getting Started with the Stream-Output Stage</span></span>

<span data-ttu-id="93be1-104">本節說明如何搭配資料流程輸出階段使用幾何著色器。</span><span class="sxs-lookup"><span data-stu-id="93be1-104">This section describes how to use a geometry shader with the stream output stage.</span></span>

## <a name="compile-a-geometry-shader"></a><span data-ttu-id="93be1-105">編譯幾何著色器</span><span class="sxs-lookup"><span data-stu-id="93be1-105">Compile a Geometry Shader</span></span>

<span data-ttu-id="93be1-106">這個幾何著色器 (GS) 計算每個三角形的臉部，以及輸出位置、正常和材質座標資料。</span><span class="sxs-lookup"><span data-stu-id="93be1-106">This geometry shader (GS) calculates a face normal for each triangle, and outputs position, normal and texture coordinate data.</span></span>


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



<span data-ttu-id="93be1-107">記住這段程式碼，請考慮幾何著色器看起來很像頂點或圖元著色器，但有下列例外狀況：函式傳回的類型、輸入參數宣告，以及內建函式。</span><span class="sxs-lookup"><span data-stu-id="93be1-107">Keeping that code in mind, consider that a geometry shader looks much like a vertex or pixel shader, but with the following exceptions: the type returned by the function, the input parameter declarations, and the intrinsic function.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93be1-108">項目</span><span class="sxs-lookup"><span data-stu-id="93be1-108">Item</span></span></th>
<th><span data-ttu-id="93be1-109">描述</span><span class="sxs-lookup"><span data-stu-id="93be1-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93be1-110"><span id="Function_return_type"></span><span id="function_return_type"></span><span id="FUNCTION_RETURN_TYPE"></span>函數傳回類型</span><span class="sxs-lookup"><span data-stu-id="93be1-110"><span id="Function_return_type"></span><span id="function_return_type"></span><span id="FUNCTION_RETURN_TYPE"></span>Function return type</span></span><br/></td>
<td><span data-ttu-id="93be1-111">函式傳回類型會執行其中一項工作，宣告著色器可以輸出的最大頂點數目。</span><span class="sxs-lookup"><span data-stu-id="93be1-111">The function return type does one thing, declares the maximum number of vertices that can be output by the shader.</span></span> <span data-ttu-id="93be1-112">在此情況下， <span data-codelanguage=""></span>
</span><span class="sxs-lookup"><span data-stu-id="93be1-112">In this case, <span data-codelanguage=""></span>
</span></span><table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>maxvertexcount(12)</code></pre></td>
</tr>
</tbody>
</table>

<span data-ttu-id="93be1-113">定義最多12個頂點的輸出。</span><span class="sxs-lookup"><span data-stu-id="93be1-113">defines the output to be a maximum of 12 vertices.</span></span></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93be1-114"><span id="Input_parameter_declarations"></span><span id="input_parameter_declarations"></span><span id="INPUT_PARAMETER_DECLARATIONS"></span>輸入參數聲明</span><span class="sxs-lookup"><span data-stu-id="93be1-114"><span id="Input_parameter_declarations"></span><span id="input_parameter_declarations"></span><span id="INPUT_PARAMETER_DECLARATIONS"></span>Input parameter declarations</span></span></p></td>
<td><p><span data-ttu-id="93be1-115">此函式會採用兩個輸入參數：</span><span class="sxs-lookup"><span data-stu-id="93be1-115">This function takes two input parameters:</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>triangle GSPS_INPUT input[3] , inout TriangleStream<GSPS_INPUT> TriStream</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="93be1-116">第一個參數是頂點 (3 的陣列，在此案例中) 由 GSPS_INPUT 結構定義， (會將每個頂點的資料定義為位置、一般和材質座標) 。</span><span class="sxs-lookup"><span data-stu-id="93be1-116">The first parameter is an array of vertices (3 in this case) defined by a GSPS_INPUT structure (which defines per-vertex data as a position, a normal and a texture coordinate).</span></span> <span data-ttu-id="93be1-117">第一個參數也會使用三角形關鍵字，這表示輸入組合語言階段必須將資料輸出到幾何著色器，做為其中一個三角形基本型別 (三角形清單或三角形帶狀) 。</span><span class="sxs-lookup"><span data-stu-id="93be1-117">The first parameter also uses the triangle keyword, which means the input assembler stage must output data to the geometry shader as one of the triangle primitive types (triangle list or triangle strip).</span></span></p>
<p><span data-ttu-id="93be1-118">第二個參數是 TriangleStream 類型所定義的三角形資料流程 <GSPS_INPUT> 。</span><span class="sxs-lookup"><span data-stu-id="93be1-118">The second parameter is a triangle stream defined by the type TriangleStream<GSPS_INPUT>.</span></span> <span data-ttu-id="93be1-119">這表示參數是三角形的陣列，其中每個都是由三個頂點組成 (其中包含 GSPS_INPUT) 成員的資料。</span><span class="sxs-lookup"><span data-stu-id="93be1-119">This means the parameter is an array of triangles, each of which is made up of three vertices (that contain the data from the members of GSPS_INPUT).</span></span></p>
<p><span data-ttu-id="93be1-120">使用三角形和 trianglestream 關鍵字來識別 GS 中的個別三角形或三角形串流。</span><span class="sxs-lookup"><span data-stu-id="93be1-120">Use the triangle and trianglestream keywords to identify individual triangles or a stream of triangles in a GS.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93be1-121"><span id="Intrinsic_function"></span><span id="intrinsic_function"></span><span id="INTRINSIC_FUNCTION"></span>內建函式</span><span class="sxs-lookup"><span data-stu-id="93be1-121"><span id="Intrinsic_function"></span><span id="intrinsic_function"></span><span id="INTRINSIC_FUNCTION"></span>Intrinsic function</span></span></p></td>
<td><p><span data-ttu-id="93be1-122">著色器函式中的程式程式碼會使用常見的著色器核心 HLSL 內建函式，但最後兩行除外，其會呼叫 Append 和 RestartStrip。</span><span class="sxs-lookup"><span data-stu-id="93be1-122">The lines of code in the shader function use common-shader-core HLSL intrinsic functions except the last two lines, which call Append and RestartStrip.</span></span> <span data-ttu-id="93be1-123">這些函式僅適用于幾何著色器。</span><span class="sxs-lookup"><span data-stu-id="93be1-123">These functions are only available to a geometry shader.</span></span> <span data-ttu-id="93be1-124">附加會告知幾何著色器將輸出附加至目前的區域：RestartStrip 會建立新的基本帶狀。</span><span class="sxs-lookup"><span data-stu-id="93be1-124">Append informs the geometry shader to append the output to the current strip; RestartStrip creates a new primitive strip.</span></span> <span data-ttu-id="93be1-125">每次叫用 GS 階段時，會隱含地建立新的帶狀。</span><span class="sxs-lookup"><span data-stu-id="93be1-125">A new strip is implicitly created in every invocation of the GS stage.</span></span></p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="93be1-126">著色器的其餘部分看起來非常類似頂點或圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="93be1-126">The rest of the shader looks very similar to a vertex or pixel shader.</span></span> <span data-ttu-id="93be1-127">幾何著色器會使用結構來宣告輸入參數，並使用 SV 位置語義來標記位置成員， \_ 以告訴硬體此為位置資料。</span><span class="sxs-lookup"><span data-stu-id="93be1-127">The geometry shader uses a structure to declare input parameters and marks the position member with the SV\_POSITION semantic to tell the hardware that this is positional data.</span></span> <span data-ttu-id="93be1-128">輸入結構會將其他兩個輸入參數識別為材質座標 (，即使其中一個參數會包含臉部正常) 。</span><span class="sxs-lookup"><span data-stu-id="93be1-128">The input structure identifies the other two input parameters as texture coordinates (even though one of them will contain a face normal).</span></span> <span data-ttu-id="93be1-129">如果您想要的話，您可以使用自己的自訂語義作為一般臉部。</span><span class="sxs-lookup"><span data-stu-id="93be1-129">You could use your own custom semantic for the face normal if you prefer.</span></span>

<span data-ttu-id="93be1-130">設計幾何著色器之後，請呼叫 [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) 進行編譯，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="93be1-130">Having designed the geometry shader, call [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) to compile as shown in the following code example.</span></span>


```
DWORD dwShaderFlags = D3DCOMPILE_ENABLE_STRICTNESS;
ID3DBlob** ppShader;

D3DCompile( pSrcData, sizeof( pSrcData ), 
  "Tutorial13.fx", NULL, NULL, "GS", "gs_4_0", 
  dwShaderFlags, 0, &ppShader, NULL );
```



<span data-ttu-id="93be1-131">就像頂點和圖元著色器一樣，您需要著色器旗標來告訴編譯器如何將著色器編譯 (進行偵錯工具、針對速度優化，以及在) 、進入點函數和著色器模型進行驗證。</span><span class="sxs-lookup"><span data-stu-id="93be1-131">Just like vertex and pixel shaders, you need a shader flag to tell the compiler how you want the shader compiled (for debugging, optimized for speed, and so on), the entry point function, and the shader model to validate against.</span></span> <span data-ttu-id="93be1-132">此範例會使用 GS 函數，建立從 Tutorial13 檔案建立的幾何著色器。</span><span class="sxs-lookup"><span data-stu-id="93be1-132">This example creates a geometry shader built from the Tutorial13.fx file, by using the GS function.</span></span> <span data-ttu-id="93be1-133">著色器會針對著色器模型4.0 進行編譯。</span><span class="sxs-lookup"><span data-stu-id="93be1-133">The shader is compiled for shader model 4.0.</span></span>

## <a name="create-a-geometry-shader-object-with-stream-output"></a><span data-ttu-id="93be1-134">使用資料流程輸出建立 Geometry-Shader 物件</span><span class="sxs-lookup"><span data-stu-id="93be1-134">Create a Geometry-Shader Object with Stream Output</span></span>

<span data-ttu-id="93be1-135">一旦您知道將會從幾何串流資料，而且您已成功編譯著色器，下一步就是呼叫 [**ID3D11Device：： CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) 來建立幾何著色器物件。</span><span class="sxs-lookup"><span data-stu-id="93be1-135">Once you know that you will be streaming the data from the geometry, and you have successfully compiled the shader, the next step is to call [**ID3D11Device::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) to create the geometry shader object.</span></span>

<span data-ttu-id="93be1-136">但首先，您需要宣告流輸出 (因此) 階段輸入簽章。</span><span class="sxs-lookup"><span data-stu-id="93be1-136">But first, you need to declare the steam output (SO) stage input signature.</span></span> <span data-ttu-id="93be1-137">此簽章符合或驗證 GS 輸出，以及在建立物件時的輸入。</span><span class="sxs-lookup"><span data-stu-id="93be1-137">This signature matches or validates the GS outputs and the SO inputs at the time of object creation.</span></span> <span data-ttu-id="93be1-138">下列程式碼是宣告的範例。</span><span class="sxs-lookup"><span data-stu-id="93be1-138">The following code is an example of the SO declaration.</span></span>


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



<span data-ttu-id="93be1-139">此函式會採用數個參數，包括：</span><span class="sxs-lookup"><span data-stu-id="93be1-139">This function takes several parameters including:</span></span>

-   <span data-ttu-id="93be1-140">已編譯之幾何著色器的指標 (或頂點著色器的指標，如果沒有幾何著色器，將會直接從頂點著色器) 串流資料。</span><span class="sxs-lookup"><span data-stu-id="93be1-140">A pointer to the compiled geometry shader (or vertex shader if no geometry shader will be present and data will be streamed out directly from the vertex shader).</span></span> <span data-ttu-id="93be1-141">如需如何取得這個指標的詳細資訊，請參閱 [取得已編譯著色器的指標](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-using-shaders-10)。</span><span class="sxs-lookup"><span data-stu-id="93be1-141">For information about how to get this pointer, see [Getting a Pointer to a Compiled Shader](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-using-shaders-10).</span></span>
-   <span data-ttu-id="93be1-142">宣告陣列的指標，這些宣告會描述資料流程輸出階段的輸入資料。</span><span class="sxs-lookup"><span data-stu-id="93be1-142">A pointer to an array of declarations that describe the input data for the stream output stage.</span></span> <span data-ttu-id="93be1-143"> (，請參閱 D3D11 的宣告 [**\_ \_ \_ 專案**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_so_declaration_entry)。 ) 您可以提供最多64的宣告，每個不同類型的元素都要從該階段輸出。</span><span class="sxs-lookup"><span data-stu-id="93be1-143">(See [**D3D11\_SO\_DECLARATION\_ENTRY**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_so_declaration_entry).) You can supply up to 64 declarations, one for each different type of element to be output from the SO stage.</span></span> <span data-ttu-id="93be1-144">宣告專案的陣列描述資料版面配置，不論是否只針對資料流程輸出系結單一緩衝區或多個緩衝區。</span><span class="sxs-lookup"><span data-stu-id="93be1-144">The array of declaration entries describes the data layout regardless of whether only a single buffer or multiple buffers are to be bound for stream output.</span></span>
-   <span data-ttu-id="93be1-145">由這個階段所寫出的元素數目。</span><span class="sxs-lookup"><span data-stu-id="93be1-145">The number of elements that are written out by the SO stage.</span></span>
-   <span data-ttu-id="93be1-146">幾何著色器物件的指標，該物件是建立 (請參閱 [**ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader)) 。</span><span class="sxs-lookup"><span data-stu-id="93be1-146">A pointer to the geometry shader object that is created (see [**ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader)).</span></span>

<span data-ttu-id="93be1-147">在這種情況下，緩衝區跨距為 Null，要傳送給轉譯器的資料流程索引為0，而類別連結介面為 Null。</span><span class="sxs-lookup"><span data-stu-id="93be1-147">In this situation, the buffer stride is NULL, the index of the stream to be sent to the rasterizer is 0, and the class linkage interface is NULL.</span></span>

<span data-ttu-id="93be1-148">資料流程輸出宣告會定義將資料寫入緩衝區資源的方式。</span><span class="sxs-lookup"><span data-stu-id="93be1-148">The stream output declaration defines the way that data is written to a buffer resource.</span></span> <span data-ttu-id="93be1-149">您可以將所需數量的元件加入至輸出宣告。</span><span class="sxs-lookup"><span data-stu-id="93be1-149">You can add as many components as you want to the output declaration.</span></span> <span data-ttu-id="93be1-150">您可以使用此階段來寫入單一緩衝區資源或許多緩衝區資源。</span><span class="sxs-lookup"><span data-stu-id="93be1-150">Use the SO stage to write to a single buffer resource or many buffer resources.</span></span> <span data-ttu-id="93be1-151">針對單一緩衝區，此階段可以為每個頂點撰寫許多不同的元素。</span><span class="sxs-lookup"><span data-stu-id="93be1-151">For a single buffer, the SO stage can write many different elements per-vertex.</span></span> <span data-ttu-id="93be1-152">針對多個緩衝區，此階段只能將每個頂點資料的單一元素寫入至每個緩衝區。</span><span class="sxs-lookup"><span data-stu-id="93be1-152">For multiple buffers, the SO stage can only write a single element of per-vertex data to each buffer.</span></span>

<span data-ttu-id="93be1-153">若要在不使用幾何著色器的情況下使用此階段，請呼叫 [**ID3D11Device：： CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) ，並將指向頂點著色器的指標傳遞至 *pShaderBytecode* 參數。</span><span class="sxs-lookup"><span data-stu-id="93be1-153">To use the SO stage without using a geometry shader, call [**ID3D11Device::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) and pass a pointer to a vertex shader to the *pShaderBytecode* parameter.</span></span>

## <a name="set-the-output-targets"></a><span data-ttu-id="93be1-154">設定輸出目標</span><span class="sxs-lookup"><span data-stu-id="93be1-154">Set the Output Targets</span></span>

<span data-ttu-id="93be1-155">最後一個步驟是設定暫存緩衝區。</span><span class="sxs-lookup"><span data-stu-id="93be1-155">The last step is to set the SO stage buffers.</span></span> <span data-ttu-id="93be1-156">資料可以串流至記憶體中的一或多個緩衝區，以供稍後使用。</span><span class="sxs-lookup"><span data-stu-id="93be1-156">Data can be streamed into one or more buffers in memory for use later.</span></span> <span data-ttu-id="93be1-157">下列程式碼示範如何建立可用於頂點資料的單一緩衝區，以及要將資料串流至的這個階段。</span><span class="sxs-lookup"><span data-stu-id="93be1-157">The following code shows how to create a single buffer that can be used for vertex data, as well as for the SO stage to stream data into.</span></span>


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



<span data-ttu-id="93be1-158">藉由呼叫 [**ID3D11Device：： CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer)來建立緩衝區。</span><span class="sxs-lookup"><span data-stu-id="93be1-158">Create a buffer by calling [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer).</span></span> <span data-ttu-id="93be1-159">此範例說明預設使用方式，這通常適用于預期會由 CPU 相當頻繁更新的緩衝區資源。</span><span class="sxs-lookup"><span data-stu-id="93be1-159">This example illustrates default usage, which is typical for a buffer resource that is expected to be updated fairly frequently by the CPU.</span></span> <span data-ttu-id="93be1-160">系結旗標會識別資源可以系結的管線階段。</span><span class="sxs-lookup"><span data-stu-id="93be1-160">The binding flag identifies the pipeline stage that the resource can be bound to.</span></span> <span data-ttu-id="93be1-161">使用系結旗標 D3D10 系結資料流程輸出時，也必須使用系結旗標來建立此階段所使用的任何資源 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="93be1-161">Any resource used by the SO stage must also be created with the bind flag D3D10\_BIND\_STREAM\_OUTPUT.</span></span>

<span data-ttu-id="93be1-162">成功建立緩衝區之後，藉由呼叫 [**>id3d11devicecoNtext：： SOSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets)，將它設定為目前的裝置：</span><span class="sxs-lookup"><span data-stu-id="93be1-162">Once the buffer is successfully created, set it to the current device by calling [**ID3D11DeviceContext::SOSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets):</span></span>


```
UINT offset[1] = 0;
D3D11Device->SOSetTargets( 1, &m_pBuffer, offset );
```



<span data-ttu-id="93be1-163">此呼叫會採用緩衝區數目、緩衝區的指標，以及位移的陣列 (每個緩衝區的一個位移，指出開始寫入資料的位置) 。</span><span class="sxs-lookup"><span data-stu-id="93be1-163">This call takes the number of buffers, a pointer to the buffers, and an array of offsets (one offset into each of the buffers that indicates where to begin writing data).</span></span> <span data-ttu-id="93be1-164">呼叫 draw 函式時，資料會寫入至這些資料流程輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="93be1-164">Data will be written to these streaming-output buffers when a draw function is called.</span></span> <span data-ttu-id="93be1-165">內部變數會追蹤開始將資料寫入串流輸出緩衝區的位置，而變數會繼續遞增，直到再次呼叫 [**SOSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets) 並指定新的位移值為止。</span><span class="sxs-lookup"><span data-stu-id="93be1-165">An internal variable keeps track of the position for where to begin writing data to the streaming-output buffers, and that variables will continue to increment until [**SOSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets) is called again and a new offset value is specified.</span></span>

<span data-ttu-id="93be1-166">所有寫入目標緩衝區的資料都將是32位值。</span><span class="sxs-lookup"><span data-stu-id="93be1-166">All data written out to the target buffers will be 32-bit values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="93be1-167">相關主題</span><span class="sxs-lookup"><span data-stu-id="93be1-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93be1-168">資料流程-輸出階段</span><span class="sxs-lookup"><span data-stu-id="93be1-168">Stream-Output Stage</span></span>](d3d10-graphics-programming-guide-output-stream-stage.md)
</dt> </dl>

 


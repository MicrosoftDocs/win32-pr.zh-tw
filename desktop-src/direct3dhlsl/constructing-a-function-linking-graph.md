---
title: 建立函式連結-圖形，並將它連結至已編譯的程式碼
description: 在這裡，我們將示範如何為著色器建立函式連結圖形 (FLGs) ，以及如何將這些著色器連結至著色器程式庫，以產生 Direct3D 執行時間可使用的著色器 blob。
ms.assetid: 82C3109E-8571-49D2-A8BF-298E30E1281B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c037e7ea111d11d24df173ffba7e56c8f486af82
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842563"
---
# <a name="constructing-a-function-linking-graph-and-linking-it-to-compiled-code"></a>建立函式連結-圖形，並將它連結至已編譯的程式碼

在這裡，我們將示範如何為著色器建立函式連結圖形 (FLGs) ，以及如何將這些著色器連結至著色器程式庫，以產生 Direct3D 執行時間可使用的著色器 blob。

**目標：** 若要建立函式連結-graph，並將其連結至已編譯的程式碼。

## <a name="prerequisites"></a>必要條件

我們假設您熟悉 C++。 您還需要圖形程式設計概念的基本經驗。

我們也假設您已完成 [封裝著色器程式庫](pachaging-a-shader-library.md)。

**完成時間：** 30 分鐘。

## <a name="instructions"></a>指示

### <a name="1-construct-a-function-linking-graph-for-the-vertex-shader"></a>1. 建立頂點著色器的函式連結-graph。

呼叫 [**D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) 函式，以建立函式連結-Graph ([**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)) 來代表頂點著色器。

使用 [**D3D11 \_ 參數 \_ DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) 結構的陣列來定義頂點著色器的輸入參數。 [輸入組合語言階段](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage)會將輸入參數摘要送入頂點著色器。 頂點著色器輸入參數的版面配置符合已編譯器代碼中頂點著色器的版面配置。 在您定義輸入參數之後，請呼叫 [**ID3D11FunctionLinkingGraph：： SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) 方法，以定義頂點著色器 ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) 的輸入節點。


```C++
            ComPtr<ID3D11FunctionLinkingGraph> vertexShaderGraph;
            DX::ThrowIfFailed(D3DCreateFunctionLinkingGraph(0, &vertexShaderGraph));

            // Define the main input node which will be fed by the Input Assembler pipeline stage.
            static const D3D11_PARAMETER_DESC vertexShaderInputParameters[] =
            {
                {"inputPos",  "POSITION0", D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 3, D3D_INTERPOLATION_LINEAR, D3D_PF_IN, 0, 0, 0, 0},
                {"inputTex",  "TEXCOORD0", D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 2, D3D_INTERPOLATION_LINEAR, D3D_PF_IN, 0, 0, 0, 0},
                {"inputNorm", "NORMAL0",   D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 3, D3D_INTERPOLATION_LINEAR, D3D_PF_IN, 0, 0, 0, 0}
            };
            ComPtr<ID3D11LinkingNode> vertexShaderInputNode;
            LinkingThrowIfFailed(vertexShaderGraph->SetInputSignature(vertexShaderInputParameters, ARRAYSIZE(vertexShaderInputParameters), 
                &vertexShaderInputNode), vertexShaderGraph.Get());
```



呼叫 [**ID3D11FunctionLinkingGraph：： CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) 方法，以建立主要頂點著色器函式的節點，並呼叫 [**ID3D11FunctionLinkingGraph：:P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) ，將輸入節點的值傳遞至主要頂點著色器函式的節點。


```C++
            // Create a node for the main VertexFunction call using the output of the helper functions.
            ComPtr<ID3D11LinkingNode> vertexFunctionCallNode;
            LinkingThrowIfFailed(vertexShaderGraph->CallFunction("", shaderLibrary.Get(), "VertexFunction", &vertexFunctionCallNode), 
                vertexShaderGraph.Get());

            // Define the graph edges from the input node and helper function nodes.
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(homogenizeCallNodeForPos.Get(), D3D_RETURN_PARAMETER_INDEX, 
                vertexFunctionCallNode.Get(), 0), vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexShaderInputNode.Get(), 1, vertexFunctionCallNode.Get(), 1), 
                vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(homogenizeCallNodeForNorm.Get(), D3D_RETURN_PARAMETER_INDEX, 
                vertexFunctionCallNode.Get(), 2), vertexShaderGraph.Get());
```



使用 [**D3D11 \_ 參數 \_ DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) 結構的陣列來定義頂點著色器的輸出參數。 頂點著色器會將其輸出參數饋送至圖元著色器。 頂點著色器輸出參數的版面配置符合已編譯器代碼中圖元著色器的版面配置。 在您定義輸出參數之後，請呼叫 [**ID3D11FunctionLinkingGraph：： SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) 方法，以定義頂點著色器 ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) 的輸出節點。


```C++
            // Define the main output node which will feed the Pixel Shader pipeline stage.
            static const D3D11_PARAMETER_DESC vertexShaderOutputParameters[] =
            {
                {"outputTex",  "TEXCOORD0",   D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 2, D3D_INTERPOLATION_UNDEFINED, D3D_PF_OUT, 0, 0, 0, 0},
                {"outputNorm", "NORMAL0",     D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 3, D3D_INTERPOLATION_UNDEFINED, D3D_PF_OUT, 0, 0, 0, 0},
                {"outputPos",  "SV_POSITION", D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 4, D3D_INTERPOLATION_UNDEFINED, D3D_PF_OUT, 0, 0, 0, 0}
            };
            ComPtr<ID3D11LinkingNode> vertexShaderOutputNode;
            LinkingThrowIfFailed(vertexShaderGraph->SetOutputSignature(vertexShaderOutputParameters, ARRAYSIZE(vertexShaderOutputParameters), 
                &vertexShaderOutputNode), vertexShaderGraph.Get());
```



呼叫 [**ID3D11FunctionLinkingGraph：:P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) ，將主要頂點著色器函式的節點值傳遞給輸出節點。


```C++
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexFunctionCallNode.Get(), 0, vertexShaderOutputNode.Get(), 2), 
                vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexFunctionCallNode.Get(), 1, vertexShaderOutputNode.Get(), 0), 
                vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexFunctionCallNode.Get(), 2, vertexShaderOutputNode.Get(), 1), 
                vertexShaderGraph.Get());
```



呼叫 [**ID3D11FunctionLinkingGraph：： CreateModuleInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) 方法來完成頂點著色器圖形。


```C++
            // Finalize the vertex shader graph.
            ComPtr<ID3D11ModuleInstance> vertexShaderGraphInstance;
            LinkingThrowIfFailed(vertexShaderGraph->CreateModuleInstance(&vertexShaderGraphInstance, nullptr), vertexShaderGraph.Get());
```



### <a name="2-link-the-vertex-shader"></a>2. 連結頂點著色器

呼叫 [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) 函式來建立連結器 ([**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)) ，您可以使用此程式庫，將使用您在上一個步驟中建立的頂點著色器圖形實例，來連結您在 [封裝著色器程式庫](pachaging-a-shader-library.md) 中建立的著色器程式庫實例。 呼叫 [**ID3D11Linker：： UseLibrary**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) 方法，以指定要用於連結的著色器程式庫。 呼叫 [**ID3D11Linker：： link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) 方法以連結著色器程式庫與頂點著色器圖形，以及產生 [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) 介面的指標，您可以用來存取已編譯的頂點著色器程式碼。 然後，您可以將此編譯的頂點著色器程式碼傳遞至 [**ID3D11Device：： CreateVertexShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) 方法，以建立頂點著色器物件和 [**ID3D11Device：： CreateInputLayout**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createinputlayout) 方法來建立輸入設定物件。


```C++
            // Create a linker and hook up the module instance.
            ComPtr<ID3D11Linker> linker;
            DX::ThrowIfFailed(D3DCreateLinker(&linker));
            DX::ThrowIfFailed(linker->UseLibrary(shaderLibraryInstance.Get()));

            // Link the vertex shader.
            ComPtr<ID3DBlob> errorBlob;
            if (FAILED(linker->Link(vertexShaderGraphInstance.Get(), "main", ("vs" + m_shaderModelSuffix).c_str(), 0, &vertexShaderBlob, 
                &errorBlob)))
            {
                throw errorBlob;
            }


    ComPtr<ID3D11VertexShader> vertexShader;
    DX::ThrowIfFailed(
        device->CreateVertexShader(
            vertexShaderBlob->GetBufferPointer(),
            vertexShaderBlob->GetBufferSize(),
            nullptr,
            &vertexShader
            )
        );
    context->VSSetShader(vertexShader.Get(), nullptr, 0);
    D3D11_INPUT_ELEMENT_DESC inputLayoutDesc[] =
    {
        { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 0,  D3D11_INPUT_PER_VERTEX_DATA, 0 },
        { "TEXCOORD", 0, DXGI_FORMAT_R32G32_FLOAT,    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },
        { "NORMAL",   0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 20, D3D11_INPUT_PER_VERTEX_DATA, 0 }
    };
    ComPtr<ID3D11InputLayout> inputLayout;
    DX::ThrowIfFailed(device->CreateInputLayout(inputLayoutDesc, ARRAYSIZE(inputLayoutDesc), vertexShaderBlob->GetBufferPointer(), vertexShaderBlob->GetBufferSize(), &inputLayout));
    context->IASetInputLayout(inputLayout.Get());
```



### <a name="3-construct-a-function-linking-graph-for-the-pixel-shader"></a>3. 建立圖元著色器的函式連結圖形。

呼叫 [**D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) 函式，以建立函式連結-Graph ([**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)) 來代表圖元著色器。

使用 [**D3D11 \_ 參數 \_ DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) 結構的陣列來定義圖元著色器的輸入參數。 頂點著色器階段會將輸入參數饋送至圖元著色器。 圖元著色器輸入參數的版面配置符合已編譯器代碼中圖元著色器的配置。 定義輸入參數之後，請呼叫 [**ID3D11FunctionLinkingGraph：： SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) 方法，以定義圖元著色器 ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) 的輸入節點。


```C++
            ComPtr<ID3D11FunctionLinkingGraph> pixelShaderGraph;
            DX::ThrowIfFailed(D3DCreateFunctionLinkingGraph(0, &pixelShaderGraph));

            // Define the main input node which will be fed by the vertex shader pipeline stage.
            static const D3D11_PARAMETER_DESC pixelShaderInputParameters[] =
            {
                {"inputTex",  "TEXCOORD0",   D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 2, D3D_INTERPOLATION_UNDEFINED, D3D_PF_IN, 0, 0, 0, 0},
                {"inputNorm", "NORMAL0",     D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 3, D3D_INTERPOLATION_UNDEFINED, D3D_PF_IN, 0, 0, 0, 0},
                {"inputPos",  "SV_POSITION", D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 4, D3D_INTERPOLATION_UNDEFINED, D3D_PF_IN, 0, 0, 0, 0}
            };
            ComPtr<ID3D11LinkingNode> pixelShaderInputNode;
            LinkingThrowIfFailed(pixelShaderGraph->SetInputSignature(pixelShaderInputParameters, ARRAYSIZE(pixelShaderInputParameters), 
                &pixelShaderInputNode), pixelShaderGraph.Get());
```



呼叫 [**ID3D11FunctionLinkingGraph：： CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) 方法，以建立主要圖元著色器函式的節點，並呼叫 [**ID3D11FunctionLinkingGraph：:P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) ，將輸入節點的值傳遞至主要圖元著色器函式的節點。


```C++
            // Create a node for the main ColorFunction call and connect it to the pixel shader inputs.
            ComPtr<ID3D11LinkingNode> colorValueNode;
            LinkingThrowIfFailed(pixelShaderGraph->CallFunction("", shaderLibrary.Get(), "ColorFunction", &colorValueNode), 
                pixelShaderGraph.Get());

            // Define the graph edges from the input node.
            LinkingThrowIfFailed(pixelShaderGraph->PassValue(pixelShaderInputNode.Get(), 0, colorValueNode.Get(), 0), 
                pixelShaderGraph.Get());
            LinkingThrowIfFailed(pixelShaderGraph->PassValue(pixelShaderInputNode.Get(), 1, colorValueNode.Get(), 1), 
                pixelShaderGraph.Get());
```



使用 [**D3D11 \_ 參數 \_ DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) 結構的陣列來定義圖元著色器的輸出參數。 圖元著色器會將其輸出參數送入 [輸出合併階段](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage)。 在您定義輸出參數之後，請呼叫 [**ID3D11FunctionLinkingGraph：： SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) 方法來定義輸出節點 (圖元著色器的 [**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) ，以及對 [**ID3D11FunctionLinkingGraph：:P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) 的呼叫，將值從圖元著色器函式節點傳遞至輸出節點。


```C++
            // Define the main output node which will feed the Output Merger pipeline stage.
            D3D11_PARAMETER_DESC pixelShaderOutputParameters[] =
            {
                {"outputColor", "SV_TARGET", D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 4, D3D_INTERPOLATION_UNDEFINED, D3D_PF_OUT, 0, 0, 0, 0}
            };
            ComPtr<ID3D11LinkingNode> pixelShaderOutputNode;
            LinkingThrowIfFailed(pixelShaderGraph->SetOutputSignature(pixelShaderOutputParameters, ARRAYSIZE(pixelShaderOutputParameters), 
                &pixelShaderOutputNode), pixelShaderGraph.Get());
            LinkingThrowIfFailed(pixelShaderGraph->PassValue(fillAlphaCallNode.Get(), D3D_RETURN_PARAMETER_INDEX, pixelShaderOutputNode.Get(), 0), 
                pixelShaderGraph.Get());
```



呼叫 [**ID3D11FunctionLinkingGraph：： CreateModuleInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) 方法來完成圖元著色器圖形。


```C++
            // Finalize the pixel shader graph.
            ComPtr<ID3D11ModuleInstance> pixelShaderGraphInstance;
            LinkingThrowIfFailed(pixelShaderGraph->CreateModuleInstance(&pixelShaderGraphInstance, nullptr), pixelShaderGraph.Get());
```



### <a name="4-link-the-pixel-shader"></a>4. 連結圖元著色器

呼叫 [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) 函式來建立連結器 ([**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)) ，您可以使用此程式庫，將使用您在上 [一個](pachaging-a-shader-library.md) 步驟中建立的圖元著色器圖形實例，建立的著色器程式庫實例連結。 呼叫 [**ID3D11Linker：： UseLibrary**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) 方法，以指定要用於連結的著色器程式庫。 呼叫 [**ID3D11Linker：： link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) 方法以連結著色器程式庫與圖元著色器圖形，以及產生 [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) 介面的指標，您可以用來存取編譯的圖元著色器程式碼。 然後，您可以將此編譯的圖元著色器程式碼傳遞至 [**ID3D11Device：： CreatePixelShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader) 方法，以建立圖元著色器物件。


```C++
            // Create a linker and hook up the module instance.
            ComPtr<ID3D11Linker> linker;
            DX::ThrowIfFailed(D3DCreateLinker(&linker));
            DX::ThrowIfFailed(linker->UseLibrary(shaderLibraryInstance.Get()));

            // Link the pixel shader.
            ComPtr<ID3DBlob> errorBlob;
            if (FAILED(linker->Link(pixelShaderGraphInstance.Get(), "main", ("ps" + m_shaderModelSuffix).c_str(), 0, &pixelShaderBlob, &errorBlob)))
            {
                throw errorBlob;
            }


    ComPtr<ID3D11PixelShader> pixelShader;
    DX::ThrowIfFailed(
        device->CreatePixelShader(
            pixelShaderBlob->GetBufferPointer(),
            pixelShaderBlob->GetBufferSize(),
            nullptr,
            &pixelShader
            )
        );
    context->PSSetShader(pixelShader.Get(), nullptr, 0);
```



## <a name="summary"></a>總結

我們使用 [**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph) 方法來建立頂點和圖元著色器圖形，並以程式設計方式指定著色器結構。

這些圖形結構包含可將值傳遞給彼此的先行編譯函式呼叫序列。 FLG 節點 ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) 代表輸入和輸出著色器節點，以及先行編譯程式庫函數的調用。 您註冊函式呼叫節點的順序會定義調用的順序。 您必須先指定輸入節點 ([**ID3D11FunctionLinkingGraph：： SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature)) first 和 output 節點 Last ([**ID3D11FunctionLinkingGraph：： SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature)) 。 FLG 邊緣定義值如何從一個節點傳遞至另一個節點。 傳遞值的資料類型必須相同;沒有隱含類型轉換。 Shape 和 swizzling 規則會遵循 HLSL 行為。 值只能以這個順序向前傳遞。

我們也使用了 [**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker) 方法，將著色器程式庫與著色器圖形連結在一起，以產生可供 Direct3D 執行時間使用的著色器 blob。

恭喜！ 您現在已準備好在您自己的應用程式中使用著色器連結。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用著色器連結](using-shader-linking.md)
</dt> </dl>

 

 
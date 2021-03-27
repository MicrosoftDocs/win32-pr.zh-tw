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
# <a name="constructing-a-function-linking-graph-and-linking-it-to-compiled-code"></a><span data-ttu-id="ce8af-103">建立函式連結-圖形，並將它連結至已編譯的程式碼</span><span class="sxs-lookup"><span data-stu-id="ce8af-103">Constructing a function-linking-graph and linking it to compiled code</span></span>

<span data-ttu-id="ce8af-104">在這裡，我們將示範如何為著色器建立函式連結圖形 (FLGs) ，以及如何將這些著色器連結至著色器程式庫，以產生 Direct3D 執行時間可使用的著色器 blob。</span><span class="sxs-lookup"><span data-stu-id="ce8af-104">Here we show you how to construct function-linking-graphs (FLGs) for shaders and how to link those shaders with a shader library to produce shader blobs that the Direct3D runtime can use.</span></span>

<span data-ttu-id="ce8af-105">**目標：** 若要建立函式連結-graph，並將其連結至已編譯的程式碼。</span><span class="sxs-lookup"><span data-stu-id="ce8af-105">**Objective:** To construct a function-linking-graph and link it to compiled code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ce8af-106">必要條件</span><span class="sxs-lookup"><span data-stu-id="ce8af-106">Prerequisites</span></span>

<span data-ttu-id="ce8af-107">我們假設您熟悉 C++。</span><span class="sxs-lookup"><span data-stu-id="ce8af-107">We assume that you are familiar with C++.</span></span> <span data-ttu-id="ce8af-108">您還需要圖形程式設計概念的基本經驗。</span><span class="sxs-lookup"><span data-stu-id="ce8af-108">You also need basic experience with graphics programming concepts.</span></span>

<span data-ttu-id="ce8af-109">我們也假設您已完成 [封裝著色器程式庫](pachaging-a-shader-library.md)。</span><span class="sxs-lookup"><span data-stu-id="ce8af-109">We also assume that you went through [Packaging a shader library](pachaging-a-shader-library.md).</span></span>

<span data-ttu-id="ce8af-110">**完成時間：** 30 分鐘。</span><span class="sxs-lookup"><span data-stu-id="ce8af-110">**Time to complete:** 30 minutes.</span></span>

## <a name="instructions"></a><span data-ttu-id="ce8af-111">指示</span><span class="sxs-lookup"><span data-stu-id="ce8af-111">Instructions</span></span>

### <a name="1-construct-a-function-linking-graph-for-the-vertex-shader"></a><span data-ttu-id="ce8af-112">1. 建立頂點著色器的函式連結-graph。</span><span class="sxs-lookup"><span data-stu-id="ce8af-112">1. Construct a function-linking-graph for the vertex shader.</span></span>

<span data-ttu-id="ce8af-113">呼叫 [**D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) 函式，以建立函式連結-Graph ([**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)) 來代表頂點著色器。</span><span class="sxs-lookup"><span data-stu-id="ce8af-113">Call the [**D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) function to create a function-linking-graph ([**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)) to represent the vertex shader.</span></span>

<span data-ttu-id="ce8af-114">使用 [**D3D11 \_ 參數 \_ DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) 結構的陣列來定義頂點著色器的輸入參數。</span><span class="sxs-lookup"><span data-stu-id="ce8af-114">Use an array of [**D3D11\_PARAMETER\_DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) structures to define the input parameters for the vertex shader.</span></span> <span data-ttu-id="ce8af-115">[輸入組合語言階段](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage)會將輸入參數摘要送入頂點著色器。</span><span class="sxs-lookup"><span data-stu-id="ce8af-115">The [Input-Assembler Stage](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage) feeds the input parameters to the vertex shader.</span></span> <span data-ttu-id="ce8af-116">頂點著色器輸入參數的版面配置符合已編譯器代碼中頂點著色器的版面配置。</span><span class="sxs-lookup"><span data-stu-id="ce8af-116">The layout of the vertex shader’s input parameters matches the layout of the vertex shader in the compiled code.</span></span> <span data-ttu-id="ce8af-117">在您定義輸入參數之後，請呼叫 [**ID3D11FunctionLinkingGraph：： SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) 方法，以定義頂點著色器 ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) 的輸入節點。</span><span class="sxs-lookup"><span data-stu-id="ce8af-117">After you define the input parameters, call the [**ID3D11FunctionLinkingGraph::SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) method to define the input node ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) for the vertex shader.</span></span>


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



<span data-ttu-id="ce8af-118">呼叫 [**ID3D11FunctionLinkingGraph：： CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) 方法，以建立主要頂點著色器函式的節點，並呼叫 [**ID3D11FunctionLinkingGraph：:P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) ，將輸入節點的值傳遞至主要頂點著色器函式的節點。</span><span class="sxs-lookup"><span data-stu-id="ce8af-118">Call the [**ID3D11FunctionLinkingGraph::CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) method to create a node for the main vertex shader function and make calls to [**ID3D11FunctionLinkingGraph::PassValue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) to pass values from the input node to the node for the main vertex shader function.</span></span>


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



<span data-ttu-id="ce8af-119">使用 [**D3D11 \_ 參數 \_ DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) 結構的陣列來定義頂點著色器的輸出參數。</span><span class="sxs-lookup"><span data-stu-id="ce8af-119">Use an array of [**D3D11\_PARAMETER\_DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) structures to define the output parameters for the vertex shader.</span></span> <span data-ttu-id="ce8af-120">頂點著色器會將其輸出參數饋送至圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="ce8af-120">The vertex shader feeds its output parameters to the pixel shader.</span></span> <span data-ttu-id="ce8af-121">頂點著色器輸出參數的版面配置符合已編譯器代碼中圖元著色器的版面配置。</span><span class="sxs-lookup"><span data-stu-id="ce8af-121">The layout of the vertex shader’s output parameters matches the layout of the pixel shader in the compiled code.</span></span> <span data-ttu-id="ce8af-122">在您定義輸出參數之後，請呼叫 [**ID3D11FunctionLinkingGraph：： SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) 方法，以定義頂點著色器 ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) 的輸出節點。</span><span class="sxs-lookup"><span data-stu-id="ce8af-122">After you define the output parameters, call the [**ID3D11FunctionLinkingGraph::SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) method to define the output node ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) for the vertex shader.</span></span>


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



<span data-ttu-id="ce8af-123">呼叫 [**ID3D11FunctionLinkingGraph：:P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) ，將主要頂點著色器函式的節點值傳遞給輸出節點。</span><span class="sxs-lookup"><span data-stu-id="ce8af-123">Make calls to [**ID3D11FunctionLinkingGraph::PassValue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) to pass values from the node for the main vertex shader function to the output node.</span></span>


```C++
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexFunctionCallNode.Get(), 0, vertexShaderOutputNode.Get(), 2), 
                vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexFunctionCallNode.Get(), 1, vertexShaderOutputNode.Get(), 0), 
                vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexFunctionCallNode.Get(), 2, vertexShaderOutputNode.Get(), 1), 
                vertexShaderGraph.Get());
```



<span data-ttu-id="ce8af-124">呼叫 [**ID3D11FunctionLinkingGraph：： CreateModuleInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) 方法來完成頂點著色器圖形。</span><span class="sxs-lookup"><span data-stu-id="ce8af-124">Call the [**ID3D11FunctionLinkingGraph::CreateModuleInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) method to finalize the vertex shader graph.</span></span>


```C++
            // Finalize the vertex shader graph.
            ComPtr<ID3D11ModuleInstance> vertexShaderGraphInstance;
            LinkingThrowIfFailed(vertexShaderGraph->CreateModuleInstance(&vertexShaderGraphInstance, nullptr), vertexShaderGraph.Get());
```



### <a name="2-link-the-vertex-shader"></a><span data-ttu-id="ce8af-125">2. 連結頂點著色器</span><span class="sxs-lookup"><span data-stu-id="ce8af-125">2. Link the vertex shader</span></span>

<span data-ttu-id="ce8af-126">呼叫 [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) 函式來建立連結器 ([**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)) ，您可以使用此程式庫，將使用您在上一個步驟中建立的頂點著色器圖形實例，來連結您在 [封裝著色器程式庫](pachaging-a-shader-library.md) 中建立的著色器程式庫實例。</span><span class="sxs-lookup"><span data-stu-id="ce8af-126">Call the [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) function to create a linker ([**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)) that you can use to link the instance of the shader library that you created in [Packaging a shader library](pachaging-a-shader-library.md) with the instance of the vertex shader graph that you created in the preceding step.</span></span> <span data-ttu-id="ce8af-127">呼叫 [**ID3D11Linker：： UseLibrary**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) 方法，以指定要用於連結的著色器程式庫。</span><span class="sxs-lookup"><span data-stu-id="ce8af-127">Call the [**ID3D11Linker::UseLibrary**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) method to specify the shader library to use for linking.</span></span> <span data-ttu-id="ce8af-128">呼叫 [**ID3D11Linker：： link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) 方法以連結著色器程式庫與頂點著色器圖形，以及產生 [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) 介面的指標，您可以用來存取已編譯的頂點著色器程式碼。</span><span class="sxs-lookup"><span data-stu-id="ce8af-128">Call the [**ID3D11Linker::Link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) method to link the shader library with the vertex shader graph and to produce a pointer to the [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) interface that you can use to access the compiled vertex shader code.</span></span> <span data-ttu-id="ce8af-129">然後，您可以將此編譯的頂點著色器程式碼傳遞至 [**ID3D11Device：： CreateVertexShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) 方法，以建立頂點著色器物件和 [**ID3D11Device：： CreateInputLayout**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createinputlayout) 方法來建立輸入設定物件。</span><span class="sxs-lookup"><span data-stu-id="ce8af-129">You can then pass this compiled vertex shader code to the [**ID3D11Device::CreateVertexShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) method to create the vertex shader object and to the [**ID3D11Device::CreateInputLayout**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createinputlayout) method to create the input-layout object.</span></span>


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



### <a name="3-construct-a-function-linking-graph-for-the-pixel-shader"></a><span data-ttu-id="ce8af-130">3. 建立圖元著色器的函式連結圖形。</span><span class="sxs-lookup"><span data-stu-id="ce8af-130">3. Construct a function-linking-graph for the pixel shader.</span></span>

<span data-ttu-id="ce8af-131">呼叫 [**D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) 函式，以建立函式連結-Graph ([**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)) 來代表圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="ce8af-131">Call the [**D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) function to create a function-linking-graph ([**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)) to represent the pixel shader.</span></span>

<span data-ttu-id="ce8af-132">使用 [**D3D11 \_ 參數 \_ DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) 結構的陣列來定義圖元著色器的輸入參數。</span><span class="sxs-lookup"><span data-stu-id="ce8af-132">Use an array of [**D3D11\_PARAMETER\_DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) structures to define the input parameters for the pixel shader.</span></span> <span data-ttu-id="ce8af-133">頂點著色器階段會將輸入參數饋送至圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="ce8af-133">The vertex shader stage feeds the input parameters to the pixel shader.</span></span> <span data-ttu-id="ce8af-134">圖元著色器輸入參數的版面配置符合已編譯器代碼中圖元著色器的配置。</span><span class="sxs-lookup"><span data-stu-id="ce8af-134">The layout of the pixel shader’s input parameters matches the layout of the pixel shader in the compiled code.</span></span> <span data-ttu-id="ce8af-135">定義輸入參數之後，請呼叫 [**ID3D11FunctionLinkingGraph：： SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) 方法，以定義圖元著色器 ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) 的輸入節點。</span><span class="sxs-lookup"><span data-stu-id="ce8af-135">After you define the input parameters, call the [**ID3D11FunctionLinkingGraph::SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) method to define the input node ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) for the pixel shader.</span></span>


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



<span data-ttu-id="ce8af-136">呼叫 [**ID3D11FunctionLinkingGraph：： CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) 方法，以建立主要圖元著色器函式的節點，並呼叫 [**ID3D11FunctionLinkingGraph：:P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) ，將輸入節點的值傳遞至主要圖元著色器函式的節點。</span><span class="sxs-lookup"><span data-stu-id="ce8af-136">Call the [**ID3D11FunctionLinkingGraph::CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) method to create a node for the main pixel shader function and make calls to [**ID3D11FunctionLinkingGraph::PassValue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) to pass values from the input node to the node for the main pixel shader function.</span></span>


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



<span data-ttu-id="ce8af-137">使用 [**D3D11 \_ 參數 \_ DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) 結構的陣列來定義圖元著色器的輸出參數。</span><span class="sxs-lookup"><span data-stu-id="ce8af-137">Use an array of [**D3D11\_PARAMETER\_DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) structures to define the output parameters for the pixel shader.</span></span> <span data-ttu-id="ce8af-138">圖元著色器會將其輸出參數送入 [輸出合併階段](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage)。</span><span class="sxs-lookup"><span data-stu-id="ce8af-138">The pixel shader feeds its output parameters to the [Output-Merger Stage](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage).</span></span> <span data-ttu-id="ce8af-139">在您定義輸出參數之後，請呼叫 [**ID3D11FunctionLinkingGraph：： SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) 方法來定義輸出節點 (圖元著色器的 [**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) ，以及對 [**ID3D11FunctionLinkingGraph：:P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) 的呼叫，將值從圖元著色器函式節點傳遞至輸出節點。</span><span class="sxs-lookup"><span data-stu-id="ce8af-139">After you define the output parameters, call the [**ID3D11FunctionLinkingGraph::SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) method to define the output node ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) for the pixel shader and make calls to [**ID3D11FunctionLinkingGraph::PassValue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) to pass values from a pixel shader function node to the output node.</span></span>


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



<span data-ttu-id="ce8af-140">呼叫 [**ID3D11FunctionLinkingGraph：： CreateModuleInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) 方法來完成圖元著色器圖形。</span><span class="sxs-lookup"><span data-stu-id="ce8af-140">Call the [**ID3D11FunctionLinkingGraph::CreateModuleInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) method to finalize the pixel shader graph.</span></span>


```C++
            // Finalize the pixel shader graph.
            ComPtr<ID3D11ModuleInstance> pixelShaderGraphInstance;
            LinkingThrowIfFailed(pixelShaderGraph->CreateModuleInstance(&pixelShaderGraphInstance, nullptr), pixelShaderGraph.Get());
```



### <a name="4-link-the-pixel-shader"></a><span data-ttu-id="ce8af-141">4. 連結圖元著色器</span><span class="sxs-lookup"><span data-stu-id="ce8af-141">4. Link the pixel shader</span></span>

<span data-ttu-id="ce8af-142">呼叫 [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) 函式來建立連結器 ([**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)) ，您可以使用此程式庫，將使用您在上 [一個](pachaging-a-shader-library.md) 步驟中建立的圖元著色器圖形實例，建立的著色器程式庫實例連結。</span><span class="sxs-lookup"><span data-stu-id="ce8af-142">Call the [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) function to create a linker ([**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)) that you can use to link the instance of the shader library that you created in [Packaging a shader library](pachaging-a-shader-library.md) with the instance of the pixel shader graph that you created in the preceding step.</span></span> <span data-ttu-id="ce8af-143">呼叫 [**ID3D11Linker：： UseLibrary**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) 方法，以指定要用於連結的著色器程式庫。</span><span class="sxs-lookup"><span data-stu-id="ce8af-143">Call the [**ID3D11Linker::UseLibrary**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) method to specify the shader library to use for linking.</span></span> <span data-ttu-id="ce8af-144">呼叫 [**ID3D11Linker：： link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) 方法以連結著色器程式庫與圖元著色器圖形，以及產生 [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) 介面的指標，您可以用來存取編譯的圖元著色器程式碼。</span><span class="sxs-lookup"><span data-stu-id="ce8af-144">Call the [**ID3D11Linker::Link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) method to link the shader library with the pixel shader graph and to produce a pointer to the [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) interface that you can use to access the compiled pixel shader code.</span></span> <span data-ttu-id="ce8af-145">然後，您可以將此編譯的圖元著色器程式碼傳遞至 [**ID3D11Device：： CreatePixelShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader) 方法，以建立圖元著色器物件。</span><span class="sxs-lookup"><span data-stu-id="ce8af-145">You can then pass this compiled pixel shader code to the [**ID3D11Device::CreatePixelShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader) method to create the pixel shader object.</span></span>


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



## <a name="summary"></a><span data-ttu-id="ce8af-146">總結</span><span class="sxs-lookup"><span data-stu-id="ce8af-146">Summary</span></span>

<span data-ttu-id="ce8af-147">我們使用 [**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph) 方法來建立頂點和圖元著色器圖形，並以程式設計方式指定著色器結構。</span><span class="sxs-lookup"><span data-stu-id="ce8af-147">We used the [**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph) methods to construct the vertex and pixel shader graphs and to specify the shader structure programmatically.</span></span>

<span data-ttu-id="ce8af-148">這些圖形結構包含可將值傳遞給彼此的先行編譯函式呼叫序列。</span><span class="sxs-lookup"><span data-stu-id="ce8af-148">These graph constructions consist of sequences of precompiled function calls that pass values to each other.</span></span> <span data-ttu-id="ce8af-149">FLG 節點 ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) 代表輸入和輸出著色器節點，以及先行編譯程式庫函數的調用。</span><span class="sxs-lookup"><span data-stu-id="ce8af-149">FLG nodes ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) represent input and output shader nodes and invocations of precompiled library functions.</span></span> <span data-ttu-id="ce8af-150">您註冊函式呼叫節點的順序會定義調用的順序。</span><span class="sxs-lookup"><span data-stu-id="ce8af-150">The order in which you register the function-call nodes defines the sequence of invocations.</span></span> <span data-ttu-id="ce8af-151">您必須先指定輸入節點 ([**ID3D11FunctionLinkingGraph：： SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature)) first 和 output 節點 Last ([**ID3D11FunctionLinkingGraph：： SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature)) 。</span><span class="sxs-lookup"><span data-stu-id="ce8af-151">You must specify the input node ([**ID3D11FunctionLinkingGraph::SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature)) first and the output node last ([**ID3D11FunctionLinkingGraph::SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature)).</span></span> <span data-ttu-id="ce8af-152">FLG 邊緣定義值如何從一個節點傳遞至另一個節點。</span><span class="sxs-lookup"><span data-stu-id="ce8af-152">FLG edges define how values are passed from one node to another.</span></span> <span data-ttu-id="ce8af-153">傳遞值的資料類型必須相同;沒有隱含類型轉換。</span><span class="sxs-lookup"><span data-stu-id="ce8af-153">The data types of passed values must be the same; there is no implicit type conversion.</span></span> <span data-ttu-id="ce8af-154">Shape 和 swizzling 規則會遵循 HLSL 行為。</span><span class="sxs-lookup"><span data-stu-id="ce8af-154">Shape and swizzling rules follow the HLSL behavior.</span></span> <span data-ttu-id="ce8af-155">值只能以這個順序向前傳遞。</span><span class="sxs-lookup"><span data-stu-id="ce8af-155">Values can only be passed forward in this sequence.</span></span>

<span data-ttu-id="ce8af-156">我們也使用了 [**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker) 方法，將著色器程式庫與著色器圖形連結在一起，以產生可供 Direct3D 執行時間使用的著色器 blob。</span><span class="sxs-lookup"><span data-stu-id="ce8af-156">We also used [**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker) methods to link the shader library with the shader graphs and to produce shader blobs for the Direct3D runtime to use.</span></span>

<span data-ttu-id="ce8af-157">恭喜！</span><span class="sxs-lookup"><span data-stu-id="ce8af-157">Congratulations!</span></span> <span data-ttu-id="ce8af-158">您現在已準備好在您自己的應用程式中使用著色器連結。</span><span class="sxs-lookup"><span data-stu-id="ce8af-158">You are now ready to use shader linking in your own apps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce8af-159">相關主題</span><span class="sxs-lookup"><span data-stu-id="ce8af-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce8af-160">使用著色器連結</span><span class="sxs-lookup"><span data-stu-id="ce8af-160">Using shader linking</span></span>](using-shader-linking.md)
</dt> </dl>

 

 
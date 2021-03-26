---
title: 封裝著色器程式庫
description: 在這裡，我們將示範如何編譯著色器程式碼、將已編譯的程式碼載入著色器程式庫，以及將資源從來源位置系結至目的地位置。
ms.assetid: ED2EB1DE-3C25-4633-BFA7-C535ABBBAD28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90124ca9753a390b924d5ba702e1986e32eee9e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104991002"
---
# <a name="packaging-a-shader-library"></a><span data-ttu-id="37807-103">封裝著色器程式庫</span><span class="sxs-lookup"><span data-stu-id="37807-103">Packaging a shader library</span></span>

<span data-ttu-id="37807-104">在這裡，我們將示範如何編譯著色器程式碼、將已編譯的程式碼載入著色器程式庫，以及將資源從來源位置系結至目的地位置。</span><span class="sxs-lookup"><span data-stu-id="37807-104">Here we show you how to compile your shader code, load the compiled code into a shader library, and bind resources from source slots to destination slots.</span></span>

<span data-ttu-id="37807-105">**目標：** 封裝著色器程式庫以用於著色器連結。</span><span class="sxs-lookup"><span data-stu-id="37807-105">**Objective:** To package a shader library to use for shader linking.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="37807-106">必要條件</span><span class="sxs-lookup"><span data-stu-id="37807-106">Prerequisites</span></span>

<span data-ttu-id="37807-107">我們假設您熟悉 C++。</span><span class="sxs-lookup"><span data-stu-id="37807-107">We assume that you are familiar with C++.</span></span> <span data-ttu-id="37807-108">您還需要圖形程式設計概念的基本經驗。</span><span class="sxs-lookup"><span data-stu-id="37807-108">You also need basic experience with graphics programming concepts.</span></span>

<span data-ttu-id="37807-109">**完成時間：** 30 分鐘。</span><span class="sxs-lookup"><span data-stu-id="37807-109">**Time to complete:** 30 minutes.</span></span>

## <a name="instructions"></a><span data-ttu-id="37807-110">指示</span><span class="sxs-lookup"><span data-stu-id="37807-110">Instructions</span></span>

### <a name="1-compiling-your-shader-code"></a><span data-ttu-id="37807-111">1. 編譯著色器程式碼</span><span class="sxs-lookup"><span data-stu-id="37807-111">1. Compiling your shader code</span></span>

<span data-ttu-id="37807-112">使用其中一個編譯函數來編譯您的著色器程式碼。</span><span class="sxs-lookup"><span data-stu-id="37807-112">Compile your shader code with one of the compile functions.</span></span> <span data-ttu-id="37807-113">例如，此程式碼片段使用 [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile)。</span><span class="sxs-lookup"><span data-stu-id="37807-113">For example, this code snippet uses [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile).</span></span>

```cpp
    string source;
 
    ComPtr<ID3DBlob> codeBlob;
    ComPtr<ID3DBlob> errorBlob;
    HRESULT hr = D3DCompile(
        source.c_str(),
        source.size(),
        "ShaderModule",
        NULL,
        NULL,
        NULL,
        ("lib" + m_shaderModelSuffix).c_str(),
        D3DCOMPILE_OPTIMIZATION_LEVEL3,
        0,
        &codeBlob,
        &errorBlob
        );
```

<span data-ttu-id="37807-114">來源字串包含未編譯的 ASCII HLSL 碼。</span><span class="sxs-lookup"><span data-stu-id="37807-114">The source string contains the uncompiled ASCII HLSL code.</span></span>

### <a name="2-load-the-compiled-code-into-a-shader-library"></a><span data-ttu-id="37807-115">2. 將已編譯的程式碼載入著色器程式庫中。</span><span class="sxs-lookup"><span data-stu-id="37807-115">2. Load the compiled code into a shader library.</span></span>

<span data-ttu-id="37807-116">呼叫 [**D3DLoadModule**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule) 函式，將已編譯的程式碼 ([**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))) 載入表示著色器程式庫的模組 ([**ID3D11Module**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11module)) 。</span><span class="sxs-lookup"><span data-stu-id="37807-116">Call the [**D3DLoadModule**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule) function to load the compiled code ([**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))) into a module ([**ID3D11Module**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11module)) that represents a shader library.</span></span>


```C++
    // Load the compiled library code into a module object.
    ComPtr<ID3D11Module> shaderLibrary;
    DX::ThrowIfFailed(D3DLoadModule(codeBlob->GetBufferPointer(), codeBlob->GetBufferSize(), &shaderLibrary));
```



### <a name="3-bind-resources-from-source-slots-to-destination-slots"></a><span data-ttu-id="37807-117">3. 將資源從來源位置系結到目的地位置。</span><span class="sxs-lookup"><span data-stu-id="37807-117">3. Bind resources from source slots to destination slots.</span></span>

<span data-ttu-id="37807-118">呼叫 [**ID3D11Module：： CreateInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11module-createinstance) 方法來建立程式庫 ([**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance)) 的實例，讓您可以定義實例的資源系結。</span><span class="sxs-lookup"><span data-stu-id="37807-118">Call the [**ID3D11Module::CreateInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11module-createinstance) method to create an instance ([**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance)) of the library so you can then define resource bindings for the instance.</span></span>

<span data-ttu-id="37807-119">呼叫 [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance) 的系結方法，從來源位置將您需要的資源系結到目的地位置。</span><span class="sxs-lookup"><span data-stu-id="37807-119">Call the bind methods of [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance) to bind the resources you need from source slots to destination slots.</span></span> <span data-ttu-id="37807-120">這些資源可以是紋理、緩衝區、取樣器、常數緩衝區或 UAVs。</span><span class="sxs-lookup"><span data-stu-id="37807-120">The resources can be textures, buffers, samplers, constant buffers, or UAVs.</span></span> <span data-ttu-id="37807-121">通常，您會使用與來源程式庫相同的位置。</span><span class="sxs-lookup"><span data-stu-id="37807-121">Typically, you will use the same slots as the source library.</span></span>


```C++
    // Create an instance of the library and define resource bindings for it.
    // In this sample we use the same slots as the source library however this is not required.
    ComPtr<ID3D11ModuleInstance> shaderLibraryInstance;
    DX::ThrowIfFailed(shaderLibrary->CreateInstance("", &shaderLibraryInstance));
    // HRESULTs for Bind methods are intentionally ignored as compiler optimizations may eliminate the source
    // bindings. In these cases, the Bind operation will fail, but the final shader will function normally.
    shaderLibraryInstance->BindResource(0, 0, 1);
    shaderLibraryInstance->BindSampler(0, 0, 1);
    shaderLibraryInstance->BindConstantBuffer(0, 0, 0);
    shaderLibraryInstance->BindConstantBuffer(1, 1, 0);
    shaderLibraryInstance->BindConstantBuffer(2, 2, 0);
```



<span data-ttu-id="37807-122">此 HLSL 程式碼顯示來源程式庫使用相同的位置 (t0、s0、B0、b1 和 b2) 作為先前系結 [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance)方法中所使用的位置。</span><span class="sxs-lookup"><span data-stu-id="37807-122">This HLSL code shows that the source library uses the same slots (t0, s0, b0, b1, and b2) as the slots used in the preceding bind methods of [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance).</span></span>

``` syntax
// This is the default code in the fixed header section.
Texture2D<float3> Texture : register(t0);
SamplerState Anisotropic : register(s0);
cbuffer CameraData : register(b0)
{
    float4x4 Model;
    float4x4 View;
    float4x4 Projection;
};
cbuffer TimeVariantSignals : register(b1)
{
    float SineWave;
    float SquareWave;
    float TriangleWave;
    float SawtoothWave;
};

// This code is not displayed, but is used as part of the linking process.
cbuffer HiddenBuffer : register(b2)
{
    float3 LightDirection;
};
```

## <a name="summary-and-next-steps"></a><span data-ttu-id="37807-123">摘要和後續步驟</span><span class="sxs-lookup"><span data-stu-id="37807-123">Summary and next steps</span></span>

<span data-ttu-id="37807-124">我們已編譯著色器程式碼，將已編譯的程式碼載入著色器程式庫，並將來源位置的資源系結到目的地位置。</span><span class="sxs-lookup"><span data-stu-id="37807-124">We compiled shader code, loaded the compiled code into a shader library, and bound resources from source slots to destination slots.</span></span>

<span data-ttu-id="37807-125">接下來，我們將 FLGs 著色器的函式連結圖形 () ，將其連結至已編譯的程式碼，並產生 Direct3D 執行時間可使用的著色器 blob。</span><span class="sxs-lookup"><span data-stu-id="37807-125">Next we construct function-linking-graphs (FLGs) for shaders, link them to compiled code, and produce shader blobs that the Direct3D runtime can use.</span></span>

[<span data-ttu-id="37807-126">建立函式連結-圖形，並將它連結至已編譯的程式碼</span><span class="sxs-lookup"><span data-stu-id="37807-126">Constructing a function-linking-graph and linking it to compiled code</span></span>](constructing-a-function-linking-graph.md)

## <a name="related-topics"></a><span data-ttu-id="37807-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="37807-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37807-128">使用著色器連結</span><span class="sxs-lookup"><span data-stu-id="37807-128">Using shader linking</span></span>](using-shader-linking.md)
</dt> </dl>

 

 
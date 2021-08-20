---
title: 封裝著色器程式庫
description: 在這裡，我們將示範如何編譯著色器程式碼、將已編譯的程式碼載入著色器程式庫，以及將資源從來源位置系結至目的地位置。
ms.assetid: ED2EB1DE-3C25-4633-BFA7-C535ABBBAD28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afb0f16d226357aca63259a9cc014a3c149d84b87d1b9340b1452b802e0df410
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117906436"
---
# <a name="packaging-a-shader-library"></a>封裝著色器程式庫

在這裡，我們將示範如何編譯著色器程式碼、將已編譯的程式碼載入著色器程式庫，以及將資源從來源位置系結至目的地位置。

**目標：** 封裝著色器程式庫以用於著色器連結。

## <a name="prerequisites"></a>必要條件

我們假設您熟悉 C++。 您還需要圖形程式設計概念的基本經驗。

**完成時間：** 30 分鐘。

## <a name="instructions"></a>指示

### <a name="1-compiling-your-shader-code"></a>1. 編譯著色器程式碼

使用其中一個編譯函數來編譯您的著色器程式碼。 例如，此程式碼片段使用 [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile)。

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

來源字串包含未編譯的 ASCII HLSL 碼。

### <a name="2-load-the-compiled-code-into-a-shader-library"></a>2. 將已編譯的程式碼載入著色器程式庫中。

呼叫 [**D3DLoadModule**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule) 函式，將已編譯的程式碼 ([**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))) 載入表示著色器程式庫的模組 ([**ID3D11Module**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11module)) 。


```C++
    // Load the compiled library code into a module object.
    ComPtr<ID3D11Module> shaderLibrary;
    DX::ThrowIfFailed(D3DLoadModule(codeBlob->GetBufferPointer(), codeBlob->GetBufferSize(), &shaderLibrary));
```



### <a name="3-bind-resources-from-source-slots-to-destination-slots"></a>3. 將資源從來源位置系結到目的地位置。

呼叫 [**ID3D11Module：： CreateInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11module-createinstance) 方法來建立程式庫 ([**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance)) 的實例，讓您可以定義實例的資源系結。

呼叫 [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance) 的系結方法，從來源位置將您需要的資源系結到目的地位置。 這些資源可以是紋理、緩衝區、取樣器、常數緩衝區或 UAVs。 通常，您會使用與來源程式庫相同的位置。


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



此 HLSL 程式碼顯示來源程式庫使用相同的位置 (t0、s0、B0、b1 和 b2) 作為先前系結 [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance)方法中所使用的位置。

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

## <a name="summary-and-next-steps"></a>摘要和後續步驟

我們已編譯著色器程式碼，將已編譯的程式碼載入著色器程式庫，並將來源位置的資源系結到目的地位置。

接下來，我們將 FLGs 著色器的函式連結圖形 () ，將其連結至已編譯的程式碼，並產生 Direct3D 執行時間可使用的著色器 blob。

[建立函式連結-圖形，並將它連結至已編譯的程式碼](constructing-a-function-linking-graph.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用著色器連結](using-shader-linking.md)
</dt> </dl>

 

 
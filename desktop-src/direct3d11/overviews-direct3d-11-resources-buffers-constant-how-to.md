---
title: 如何建立常數緩衝區
description: 本主題說明如何初始化常數緩衝區以準備轉譯。
ms.assetid: 78694ac2-e850-402d-8c99-6afb0bd5d660
keywords:
- 常數緩衝區，建立
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2359698c4dfc72bfe3c3c9747e29ddfa5f6aecd2aaa32b99d75fbe38e956ac4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117912819"
---
# <a name="how-to-create-a-constant-buffer"></a>如何：建立常數緩衝區

[常數緩衝區](overviews-direct3d-11-resources-buffers-intro.md) 包含著色器常數資料。 本主題說明如何初始化 [常數緩衝區](overviews-direct3d-11-resources-buffers-intro.md) 以準備轉譯。

**初始化常數緩衝區**

1.  定義描述頂點著色器常數資料的結構。
2.  為您在步驟1中定義的結構配置記憶體。 使用頂點著色器常數資料來填滿此緩衝區。 您可以使用 **malloc** 或 **new** 來配置記憶體，也可以從堆疊配置結構的記憶體。
3.  填入 [**D3D11 \_ 緩衝區 \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) 結構來建立緩衝區描述。 將 D3D11 系 \_ 結 \_ 常數 \_ 緩衝區旗標傳遞給 **BindFlags** 成員，並將常數緩衝區描述結構的大小（以位元組為單位）傳遞給 **ByteWidth** 成員。

    > [!Note]  
    > D3D11 系 \_ 結 \_ 常數 \_ 緩衝區旗標無法與任何其他旗標合併。

     

4.  填入 [**D3D11 \_ subresource \_ 資料**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) 結構，以建立 subresource 資料描述。 **D3D11 \_ SUBRESOURCE \_ 資料** 結構的 **pSysMem** 成員必須直接指向您在步驟2中建立的頂點著色器常數資料。
5.  傳遞 [**D3D11 \_ 緩衝區 \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc)結構、 [**D3D11 \_ SUBRESOURCE \_ 資料**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data)結構，以及要初始化之 [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)介面指標的位址時，呼叫 [**ID3D11Device：： CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) 。

這些程式碼範例示範如何建立常數緩衝區。

此範例假設 **g \_ pd3dDevice** 是有效的 [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) 物件，且 **g \_ pd3dCoNtext** 是有效的 [**>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) 物件。


```C++
ID3D11Buffer*   g_pConstantBuffer11 = NULL;

// Define the constant data used to communicate with shaders.
struct VS_CONSTANT_BUFFER
{
    XMFLOAT4X4 mWorldViewProj;                              
    XMFLOAT4 vSomeVectorThatMayBeNeededByASpecificShader;
    float fSomeFloatThatMayBeNeededByASpecificShader;
    float fTime;                                            
    float fSomeFloatThatMayBeNeededByASpecificShader2;
    float fSomeFloatThatMayBeNeededByASpecificShader3;
} VS_CONSTANT_BUFFER;

// Supply the vertex shader constant data.
VS_CONSTANT_BUFFER VsConstData;
VsConstData.mWorldViewProj = {...};
VsConstData.vSomeVectorThatMayBeNeededByASpecificShader = XMFLOAT4(1,2,3,4);
VsConstData.fSomeFloatThatMayBeNeededByASpecificShader = 3.0f;
VsConstData.fTime = 1.0f;
VsConstData.fSomeFloatThatMayBeNeededByASpecificShader2 = 2.0f;
VsConstData.fSomeFloatThatMayBeNeededByASpecificShader3 = 4.0f;

// Fill in a buffer description.
D3D11_BUFFER_DESC cbDesc;
cbDesc.ByteWidth = sizeof( VS_CONSTANT_BUFFER );
cbDesc.Usage = D3D11_USAGE_DYNAMIC;
cbDesc.BindFlags = D3D11_BIND_CONSTANT_BUFFER;
cbDesc.CPUAccessFlags = D3D11_CPU_ACCESS_WRITE;
cbDesc.MiscFlags = 0;
cbDesc.StructureByteStride = 0;

// Fill in the subresource data.
D3D11_SUBRESOURCE_DATA InitData;
InitData.pSysMem = &VsConstData;
InitData.SysMemPitch = 0;
InitData.SysMemSlicePitch = 0;

// Create the buffer.
hr = g_pd3dDevice->CreateBuffer( &cbDesc, &InitData, 
                                 &g_pConstantBuffer11 );

if( FAILED( hr ) )
   return hr;

// Set the buffer.
g_pd3dContext->VSSetConstantBuffers( 0, 1, &g_pConstantBuffer11 );
    
```



這個範例會顯示相關聯的 HLSL cbuffer 定義。

``` syntax
cbuffer VS_CONSTANT_BUFFER : register(b0)
{
    matrix mWorldViewProj;
    float4  vSomeVectorThatMayBeNeededByASpecificShader;
    float fSomeFloatThatMayBeNeededByASpecificShader;
    float fTime;
    float fSomeFloatThatMayBeNeededByASpecificShader2;
    float fSomeFloatThatMayBeNeededByASpecificShader3;
};
```

> [!Note]  
> 請務必將 \_ \_ c + + 中的 VS 常數緩衝區記憶體配置與 HLSL 版面配置相符。 如需 HLSL 如何處理記憶體中配置的詳細資訊，請參閱 [常數變數的封裝規則](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules)。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[緩衝區](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[如何使用 Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 
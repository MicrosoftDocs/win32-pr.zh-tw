---
title: 如何建立常數緩衝區
description: 本主題說明如何初始化常數緩衝區以準備轉譯。
ms.assetid: 78694ac2-e850-402d-8c99-6afb0bd5d660
keywords:
- 常數緩衝區，建立
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1abb6718ad223ff389aa0b7ebf10ad1ec8bacd71
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682923"
---
# <a name="how-to-create-a-constant-buffer"></a><span data-ttu-id="e6d2b-104">如何：建立常數緩衝區</span><span class="sxs-lookup"><span data-stu-id="e6d2b-104">How to: Create a Constant Buffer</span></span>

<span data-ttu-id="e6d2b-105">[常數緩衝區](overviews-direct3d-11-resources-buffers-intro.md) 包含著色器常數資料。</span><span class="sxs-lookup"><span data-stu-id="e6d2b-105">[Constant buffers](overviews-direct3d-11-resources-buffers-intro.md) contain shader constant data.</span></span> <span data-ttu-id="e6d2b-106">本主題說明如何初始化 [常數緩衝區](overviews-direct3d-11-resources-buffers-intro.md) 以準備轉譯。</span><span class="sxs-lookup"><span data-stu-id="e6d2b-106">This topic shows how to initialize a [constant buffer](overviews-direct3d-11-resources-buffers-intro.md) in preparation for rendering.</span></span>

<span data-ttu-id="e6d2b-107">**初始化常數緩衝區**</span><span class="sxs-lookup"><span data-stu-id="e6d2b-107">**To initialize a constant buffer**</span></span>

1.  <span data-ttu-id="e6d2b-108">定義描述頂點著色器常數資料的結構。</span><span class="sxs-lookup"><span data-stu-id="e6d2b-108">Define a structure that describes the vertex shader constant data.</span></span>
2.  <span data-ttu-id="e6d2b-109">為您在步驟1中定義的結構配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="e6d2b-109">Allocate memory for the structure that you defined in step one.</span></span> <span data-ttu-id="e6d2b-110">使用頂點著色器常數資料來填滿此緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e6d2b-110">Fill this buffer with vertex shader constant data.</span></span> <span data-ttu-id="e6d2b-111">您可以使用 **malloc** 或 **new** 來配置記憶體，也可以從堆疊配置結構的記憶體。</span><span class="sxs-lookup"><span data-stu-id="e6d2b-111">You can use **malloc** or **new** to allocate the memory, or you can allocate memory for the structure from the stack.</span></span>
3.  <span data-ttu-id="e6d2b-112">填入 [**D3D11 \_ 緩衝區 \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) 結構來建立緩衝區描述。</span><span class="sxs-lookup"><span data-stu-id="e6d2b-112">Create a buffer description by filling in a [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure.</span></span> <span data-ttu-id="e6d2b-113">將 D3D11 系 \_ 結 \_ 常數 \_ 緩衝區旗標傳遞給 **BindFlags** 成員，並將常數緩衝區描述結構的大小（以位元組為單位）傳遞給 **ByteWidth** 成員。</span><span class="sxs-lookup"><span data-stu-id="e6d2b-113">Pass the D3D11\_BIND\_CONSTANT\_BUFFER flag to the **BindFlags** member and pass the size of the constant buffer description structure in bytes to the **ByteWidth** member.</span></span>

    > [!Note]  
    > <span data-ttu-id="e6d2b-114">D3D11 系 \_ 結 \_ 常數 \_ 緩衝區旗標無法與任何其他旗標合併。</span><span class="sxs-lookup"><span data-stu-id="e6d2b-114">The D3D11\_BIND\_CONSTANT\_BUFFER flag cannot be combined with any other flags.</span></span>

     

4.  <span data-ttu-id="e6d2b-115">填入 [**D3D11 \_ subresource \_ 資料**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) 結構，以建立 subresource 資料描述。</span><span class="sxs-lookup"><span data-stu-id="e6d2b-115">Create a subresource data description by filling in a [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure.</span></span> <span data-ttu-id="e6d2b-116">**D3D11 \_ SUBRESOURCE \_ 資料** 結構的 **pSysMem** 成員必須直接指向您在步驟2中建立的頂點著色器常數資料。</span><span class="sxs-lookup"><span data-stu-id="e6d2b-116">The **pSysMem** member of the **D3D11\_SUBRESOURCE\_DATA** structure must point directly to the vertex shader constant data that you created in step two.</span></span>
5.  <span data-ttu-id="e6d2b-117">傳遞 [**D3D11 \_ 緩衝區 \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc)結構、 [**D3D11 \_ SUBRESOURCE \_ 資料**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data)結構，以及要初始化之 [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)介面指標的位址時，呼叫 [**ID3D11Device：： CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) 。</span><span class="sxs-lookup"><span data-stu-id="e6d2b-117">Call [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) while passing the [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure, the [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure, and the address of a pointer to the [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) interface to initialize.</span></span>

<span data-ttu-id="e6d2b-118">這些程式碼範例示範如何建立常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e6d2b-118">These code examples demonstrate how to create a constant buffer.</span></span>

<span data-ttu-id="e6d2b-119">此範例假設 **g \_ pd3dDevice** 是有效的 [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) 物件，且 **g \_ pd3dCoNtext** 是有效的 [**>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) 物件。</span><span class="sxs-lookup"><span data-stu-id="e6d2b-119">This example assumes that **g\_pd3dDevice** is a valid [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) object and that **g\_pd3dContext** is a valid [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>


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



<span data-ttu-id="e6d2b-120">這個範例會顯示相關聯的 HLSL cbuffer 定義。</span><span class="sxs-lookup"><span data-stu-id="e6d2b-120">This example shows the associated HLSL cbuffer definition.</span></span>

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
> <span data-ttu-id="e6d2b-121">請務必將 \_ \_ c + + 中的 VS 常數緩衝區記憶體配置與 HLSL 版面配置相符。</span><span class="sxs-lookup"><span data-stu-id="e6d2b-121">Make sure to match the VS\_CONSTANT\_BUFFER memory layout in C++ with the HLSL layout.</span></span> <span data-ttu-id="e6d2b-122">如需 HLSL 如何處理記憶體中配置的詳細資訊，請參閱 [常數變數的封裝規則](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules)。</span><span class="sxs-lookup"><span data-stu-id="e6d2b-122">For info about how HLSL handles layout in memory, see [Packing Rules for Constant Variables](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e6d2b-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="e6d2b-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6d2b-124">緩衝區</span><span class="sxs-lookup"><span data-stu-id="e6d2b-124">Buffers</span></span>](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[<span data-ttu-id="e6d2b-125">如何使用 Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="e6d2b-125">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 
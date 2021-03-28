---
title: 如何建立索引緩衝區
description: 本主題說明如何在準備轉譯時初始化索引緩衝區。
ms.assetid: 4b33d32a-27fd-4652-87ac-3b7268881f89
keywords:
- 索引緩衝區，建立
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c4c99639748876a5f5fd84e546aaf299885c76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183823"
---
# <a name="how-to-create-an-index-buffer"></a><span data-ttu-id="b39da-104">如何：建立索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="b39da-104">How to: Create an Index Buffer</span></span>

<span data-ttu-id="b39da-105">[索引緩衝區](overviews-direct3d-11-resources-buffers-intro.md) 包含索引資料。</span><span class="sxs-lookup"><span data-stu-id="b39da-105">[Index buffers](overviews-direct3d-11-resources-buffers-intro.md) contain index data.</span></span> <span data-ttu-id="b39da-106">本主題說明如何在準備轉譯時初始化 [索引緩衝區](overviews-direct3d-11-resources-buffers-intro.md) 。</span><span class="sxs-lookup"><span data-stu-id="b39da-106">This topic shows how to initialize an [index buffer](overviews-direct3d-11-resources-buffers-intro.md) in preparation for rendering.</span></span>

<span data-ttu-id="b39da-107">**初始化索引緩衝區**</span><span class="sxs-lookup"><span data-stu-id="b39da-107">**To initialize an index buffer**</span></span>

1.  <span data-ttu-id="b39da-108">建立包含索引資訊的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b39da-108">Create a buffer that contains your index information.</span></span>
2.  <span data-ttu-id="b39da-109">填入 [**D3D11 \_ 緩衝區 \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) 結構來建立緩衝區描述。</span><span class="sxs-lookup"><span data-stu-id="b39da-109">Create a buffer description by filling in a [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure.</span></span> <span data-ttu-id="b39da-110">將 D3D11 系 \_ 結 \_ 索引 \_ 緩衝區旗標傳遞給 **BindFlags** 成員，並將緩衝區的大小以位元組傳遞給 **ByteWidth** 成員。</span><span class="sxs-lookup"><span data-stu-id="b39da-110">Pass the D3D11\_BIND\_INDEX\_BUFFER flag to the **BindFlags** member and pass the size of the buffer in bytes to the **ByteWidth** member.</span></span>
3.  <span data-ttu-id="b39da-111">填入 [**D3D11 \_ subresource \_ 資料**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) 結構，以建立 subresource 資料描述。</span><span class="sxs-lookup"><span data-stu-id="b39da-111">Create a subresource data description by filling in a [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure.</span></span> <span data-ttu-id="b39da-112">**PSysMem** 成員應該直接指向在步驟一中建立的索引資料。</span><span class="sxs-lookup"><span data-stu-id="b39da-112">The **pSysMem** member should point directly to the index data created in step one.</span></span>
4.  <span data-ttu-id="b39da-113">傳遞 [**D3D11 \_ 緩衝區 \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc)結構、 [**D3D11 \_ SUBRESOURCE \_ 資料**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data)結構，以及要初始化之 [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)介面指標的位址時，呼叫 [**ID3D11Device：： CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) 。</span><span class="sxs-lookup"><span data-stu-id="b39da-113">Call [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) while passing the [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure, the [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure, and the address of a pointer to the [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) interface to initialize.</span></span>

<span data-ttu-id="b39da-114">下列程式碼範例示範如何建立索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b39da-114">The following code example demonstrates how to create an index buffer.</span></span> <span data-ttu-id="b39da-115">此範例假設</span><span class="sxs-lookup"><span data-stu-id="b39da-115">This example assumes that</span></span>


```
g_pd3dDevice
```



<span data-ttu-id="b39da-116">是有效的 [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) 物件，而且</span><span class="sxs-lookup"><span data-stu-id="b39da-116">is a valid [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) object and that</span></span>


```
g_pd3dContext
```



<span data-ttu-id="b39da-117">這是有效的 [**>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) 物件。</span><span class="sxs-lookup"><span data-stu-id="b39da-117">is a valid [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>


```
ID3D11Buffer *g_pIndexBuffer = NULL;

// Create indices.
unsigned int indices[] = { 0, 1, 2 };

// Fill in a buffer description.
D3D11_BUFFER_DESC bufferDesc;
bufferDesc.Usage           = D3D11_USAGE_DEFAULT;
bufferDesc.ByteWidth       = sizeof( unsigned int ) * 3;
bufferDesc.BindFlags       = D3D11_BIND_INDEX_BUFFER;
bufferDesc.CPUAccessFlags  = 0;
bufferDesc.MiscFlags       = 0;

// Define the resource data.
D3D11_SUBRESOURCE_DATA InitData;
InitData.pSysMem = indices;
InitData.SysMemPitch = 0;
InitData.SysMemSlicePitch = 0;

// Create the buffer with the device.
hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pIndexBuffer );
if( FAILED( hr ) )
    return hr;

// Set the buffer.
g_pd3dContext->IASetIndexBuffer( g_pIndexBuffer, DXGI_FORMAT_R32_UINT, 0 );
    
```



## <a name="related-topics"></a><span data-ttu-id="b39da-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="b39da-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b39da-119">緩衝區</span><span class="sxs-lookup"><span data-stu-id="b39da-119">Buffers</span></span>](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[<span data-ttu-id="b39da-120">如何使用 Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="b39da-120">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 





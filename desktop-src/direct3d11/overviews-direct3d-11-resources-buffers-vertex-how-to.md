---
title: 如何建立頂點緩衝區
description: 本主題說明如何初始化靜態頂點緩衝區，也就是不會變更的頂點緩衝區。
ms.assetid: 584a39d1-7629-429a-b451-64b1432cb48f
keywords:
- 頂點緩衝區，建立
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55e0b3d9d8f731b01e7c919105c21c8d150f864a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301275"
---
# <a name="how-to-create-a-vertex-buffer"></a><span data-ttu-id="9b830-104">如何：建立頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="9b830-104">How to: Create a Vertex Buffer</span></span>

<span data-ttu-id="9b830-105">[頂點緩衝區](overviews-direct3d-11-resources-buffers-intro.md) 包含每個頂點資料。</span><span class="sxs-lookup"><span data-stu-id="9b830-105">[Vertex buffers](overviews-direct3d-11-resources-buffers-intro.md) contain per vertex data.</span></span> <span data-ttu-id="9b830-106">本主題說明如何初始化靜態 [頂點緩衝區](overviews-direct3d-11-resources-buffers-intro.md)，也就是不會變更的頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="9b830-106">This topic shows how to initialize a static [vertex buffer](overviews-direct3d-11-resources-buffers-intro.md), that is, a vertex buffer that does not change.</span></span> <span data-ttu-id="9b830-107">如需初始化非靜態緩衝區的說明，請參閱「 [備註](#remarks) 」一節。</span><span class="sxs-lookup"><span data-stu-id="9b830-107">For help initializing a non-static buffer, see the [remarks](#remarks) section.</span></span>

<span data-ttu-id="9b830-108">**若要初始化靜態頂點緩衝區**</span><span class="sxs-lookup"><span data-stu-id="9b830-108">**To initialize a static vertex buffer**</span></span>

1.  <span data-ttu-id="9b830-109">定義描述頂點的結構。</span><span class="sxs-lookup"><span data-stu-id="9b830-109">Define a structure that describes a vertex.</span></span> <span data-ttu-id="9b830-110">例如，如果您的頂點資料包含位置資料和色彩資料，您的結構會有一個描述位置的向量，另一個則會描述色彩。</span><span class="sxs-lookup"><span data-stu-id="9b830-110">For example, if your vertex data contains position data and color data, your structure would have one vector that describes the position and another that describes the color.</span></span>
2.  <span data-ttu-id="9b830-111">針對您在步驟1中定義的結構，使用 malloc 或新的) 配置記憶體 (。</span><span class="sxs-lookup"><span data-stu-id="9b830-111">Allocate memory (using malloc or new) for the structure that you defined in step one.</span></span> <span data-ttu-id="9b830-112">使用描述您幾何的實際頂點資料來填滿此緩衝區。</span><span class="sxs-lookup"><span data-stu-id="9b830-112">Fill this buffer with the actual vertex data that describes your geometry.</span></span>
3.  <span data-ttu-id="9b830-113">填入 [**D3D11 \_ 緩衝區 \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) 結構來建立緩衝區描述。</span><span class="sxs-lookup"><span data-stu-id="9b830-113">Create a buffer description by filling in a [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure.</span></span> <span data-ttu-id="9b830-114">將 D3D11 系 \_ 結 \_ 頂點 \_ 緩衝區旗標傳遞給 **BindFlags** 成員，然後將步驟1的結構大小傳遞給 **ByteWidth** 成員。</span><span class="sxs-lookup"><span data-stu-id="9b830-114">Pass the D3D11\_BIND\_VERTEX\_BUFFER flag to the **BindFlags** member and pass the size of the structure from step one to the **ByteWidth** member.</span></span>
4.  <span data-ttu-id="9b830-115">填入 [**D3D11 \_ subresource \_ 資料**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) 結構，以建立 subresource 資料描述。</span><span class="sxs-lookup"><span data-stu-id="9b830-115">Create a subresource data description by filling in a [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure.</span></span> <span data-ttu-id="9b830-116">[**D3D11 \_ SUBRESOURCE \_ 資料**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data)結構的 **pSysMem** 成員應該直接指向步驟2中建立的資源資料。</span><span class="sxs-lookup"><span data-stu-id="9b830-116">The **pSysMem** member of the [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure should point directly to the resource data created in step two.</span></span>
5.  <span data-ttu-id="9b830-117">傳遞 [**D3D11 \_ 緩衝區 \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc)結構、 [**D3D11 \_ SUBRESOURCE \_ 資料**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data)結構，以及要初始化之 [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)介面指標的位址時，呼叫 [**ID3D11Device：： CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) 。</span><span class="sxs-lookup"><span data-stu-id="9b830-117">Call [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) while passing the [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure, the [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure, and the address of a pointer to the [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) interface to initialize.</span></span>

<span data-ttu-id="9b830-118">下列程式碼範例示範如何建立頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="9b830-118">The following code example demonstrates how to create a vertex buffer.</span></span> <span data-ttu-id="9b830-119">此範例假設 **g \_ pd3dDevice** 是有效的 [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) 物件。</span><span class="sxs-lookup"><span data-stu-id="9b830-119">This example assumes that **g\_pd3dDevice** is a valid [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) object.</span></span>


```
ID3D11Buffer*      g_pVertexBuffer;

// Define the data-type that
// describes a vertex.
struct SimpleVertexCombined
{
    XMFLOAT3 Pos;  
    XMFLOAT3 Col;  
};

// Supply the actual vertex data.
SimpleVertexCombined verticesCombo[] =
{
    XMFLOAT3( 0.0f, 0.5f, 0.5f ),
    XMFLOAT3( 0.0f, 0.0f, 0.5f ),
    XMFLOAT3( 0.5f, -0.5f, 0.5f ),
    XMFLOAT3( 0.5f, 0.0f, 0.0f ),
    XMFLOAT3( -0.5f, -0.5f, 0.5f ),
    XMFLOAT3( 0.0f, 0.5f, 0.0f ),
};

// Fill in a buffer description.
D3D11_BUFFER_DESC bufferDesc;
bufferDesc.Usage            = D3D11_USAGE_DEFAULT;
bufferDesc.ByteWidth        = sizeof( SimpleVertexCombined ) * 3;
bufferDesc.BindFlags        = D3D11_BIND_VERTEX_BUFFER;
bufferDesc.CPUAccessFlags   = 0;
bufferDesc.MiscFlags        = 0;

// Fill in the subresource data.
D3D11_SUBRESOURCE_DATA InitData;
InitData.pSysMem = verticesCombo;
InitData.SysMemPitch = 0;
InitData.SysMemSlicePitch = 0;

// Create the vertex buffer.
hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pVertexBuffer );
    
```



## <a name="remarks"></a><span data-ttu-id="9b830-120">備註</span><span class="sxs-lookup"><span data-stu-id="9b830-120">Remarks</span></span>

<span data-ttu-id="9b830-121">以下是一些初始化隨著時間變更之頂點緩衝區的方式。</span><span class="sxs-lookup"><span data-stu-id="9b830-121">Here are some ways to initialize a vertex buffer that changes over time.</span></span>

1.  <span data-ttu-id="9b830-122">使用 [**D3D11 \_ 使用方式 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)建立第2個緩衝區; 使用 [**>id3d11devicecoNtext：： Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)、 [**>id3d11devicecoNtext：：**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap)Map 來填滿第二個緩衝區; 使用 [**>id3d11devicecoNtext：： CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) 從暫存緩衝區複製到預設緩衝區。</span><span class="sxs-lookup"><span data-stu-id="9b830-122">Create a 2nd buffer with [**D3D11\_USAGE\_STAGING**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage); fill the second buffer using [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap); use [**ID3D11DeviceContext::CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) to copy from the staging buffer to the default buffer.</span></span>
2.  <span data-ttu-id="9b830-123">使用 [**>id3d11devicecoNtext：： UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) 從記憶體複製資料。</span><span class="sxs-lookup"><span data-stu-id="9b830-123">Use [**ID3D11DeviceContext::UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) to copy data from memory.</span></span>
3.  <span data-ttu-id="9b830-124">使用 [**D3D11 使用 \_ \_ 動態**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)來建立緩衝區，並將 [**>id3d11devicecoNtext：： Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)、 [**>id3d11devicecoNtext：：**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) 取消對應 (適當地使用捨棄和 NoOverwrite 旗標) 來填滿。</span><span class="sxs-lookup"><span data-stu-id="9b830-124">Create a buffer with [**D3D11\_USAGE\_DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), and fill it with [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) (using the Discard and NoOverwrite flags appropriately).</span></span>

<span data-ttu-id="9b830-125">\#1和 \# 2 適用于每個畫面格不到一次變更的內容。</span><span class="sxs-lookup"><span data-stu-id="9b830-125">\#1 and \#2 are useful for content that changes less than once per frame.</span></span> <span data-ttu-id="9b830-126">一般而言，GPU 讀取速度很快，CPU 更新將會變慢。</span><span class="sxs-lookup"><span data-stu-id="9b830-126">In general, GPU reads will be fast and CPU updates will be slower.</span></span>

<span data-ttu-id="9b830-127">\#3對每個畫面格變更一次以上的內容很有用。</span><span class="sxs-lookup"><span data-stu-id="9b830-127">\#3 is useful for content that changes more than once per frame.</span></span> <span data-ttu-id="9b830-128">一般而言，GPU 讀取速度會變慢，但是 CPU 更新會更快。</span><span class="sxs-lookup"><span data-stu-id="9b830-128">In general, GPU reads will be slower, but CPU updates will be faster.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b830-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="9b830-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b830-130">緩衝區</span><span class="sxs-lookup"><span data-stu-id="9b830-130">Buffers</span></span>](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[<span data-ttu-id="9b830-131">如何使用 Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="9b830-131">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 





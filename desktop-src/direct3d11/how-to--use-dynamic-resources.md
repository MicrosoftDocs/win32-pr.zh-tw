---
title: 如何使用動態資源
description: 當您的應用程式需要變更這些資源中的資料時，您會建立和使用動態資源。 您可以建立動態使用方式的材質和緩衝區。
ms.assetid: E73EA4B0-BD14-430C-89CA-4CFCF92C7548
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e41e00cda7236040679c7863454e4cc18d81106b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183113"
---
# <a name="how-to-use-dynamic-resources"></a><span data-ttu-id="40f93-104">如何：使用動態資源</span><span class="sxs-lookup"><span data-stu-id="40f93-104">How to: Use dynamic resources</span></span>

<span data-ttu-id="40f93-105">**重要 API**</span><span class="sxs-lookup"><span data-stu-id="40f93-105">**Important APIs**</span></span>

-   [<span data-ttu-id="40f93-106">**>id3d11devicecoNtext：： Map**</span><span class="sxs-lookup"><span data-stu-id="40f93-106">**ID3D11DeviceContext::Map**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)
-   [<span data-ttu-id="40f93-107">**>id3d11devicecoNtext：：取消對應**</span><span class="sxs-lookup"><span data-stu-id="40f93-107">**ID3D11DeviceContext::Unmap**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap)
-   [<span data-ttu-id="40f93-108">**D3D11 \_ 使用方式**</span><span class="sxs-lookup"><span data-stu-id="40f93-108">**D3D11\_USAGE**</span></span>](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)

<span data-ttu-id="40f93-109">當您的應用程式需要變更這些資源中的資料時，您會建立和使用動態資源。</span><span class="sxs-lookup"><span data-stu-id="40f93-109">You create and use dynamic resources when your app needs to change data in those resources.</span></span> <span data-ttu-id="40f93-110">您可以建立動態使用方式的材質和緩衝區。</span><span class="sxs-lookup"><span data-stu-id="40f93-110">You can create textures and buffers for dynamic usage.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="40f93-111">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="40f93-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="40f93-112">技術</span><span class="sxs-lookup"><span data-stu-id="40f93-112">Technologies</span></span>

-   [<span data-ttu-id="40f93-113">如何：建立材質</span><span class="sxs-lookup"><span data-stu-id="40f93-113">How to: Create a Texture</span></span>](overviews-direct3d-11-resources-textures-create.md)
-   [<span data-ttu-id="40f93-114">如何：以程式設計方式初始化材質</span><span class="sxs-lookup"><span data-stu-id="40f93-114">How to: Initialize a Texture Programmatically</span></span>](overviews-direct3d-11-resources-textures-how-to-fill-manually.md)
-   [<span data-ttu-id="40f93-115">如何：建立常數緩衝區</span><span class="sxs-lookup"><span data-stu-id="40f93-115">How to: Create a Constant Buffer</span></span>](overviews-direct3d-11-resources-buffers-constant-how-to.md)

### <a name="prerequisites"></a><span data-ttu-id="40f93-116">必要條件</span><span class="sxs-lookup"><span data-stu-id="40f93-116">Prerequisites</span></span>

<span data-ttu-id="40f93-117">我們假設您熟悉 C++。</span><span class="sxs-lookup"><span data-stu-id="40f93-117">We assume that you are familiar with C++.</span></span> <span data-ttu-id="40f93-118">您還需要圖形程式設計概念的基本經驗。</span><span class="sxs-lookup"><span data-stu-id="40f93-118">You also need basic experience with graphics programming concepts.</span></span>

## <a name="instructions"></a><span data-ttu-id="40f93-119">指示</span><span class="sxs-lookup"><span data-stu-id="40f93-119">Instructions</span></span>

### <a name="step-1-specify-dynamic-usage"></a><span data-ttu-id="40f93-120">步驟1：指定動態使用方式</span><span class="sxs-lookup"><span data-stu-id="40f93-120">Step 1: Specify dynamic usage</span></span>

<span data-ttu-id="40f93-121">如果您想要讓應用程式能夠變更資源，您必須在建立資源時將這些資源指定為動態和可寫入。</span><span class="sxs-lookup"><span data-stu-id="40f93-121">If you want your app to be able to make changes to resources, you must specify those resources as dynamic and writable when you create them.</span></span>

<span data-ttu-id="40f93-122">**若要指定動態使用方式**</span><span class="sxs-lookup"><span data-stu-id="40f93-122">**To specify dynamic usage**</span></span>

1.  <span data-ttu-id="40f93-123">將資源使用方式指定為動態。</span><span class="sxs-lookup"><span data-stu-id="40f93-123">Specify the resource usage as dynamic.</span></span> <span data-ttu-id="40f93-124">例如，在頂點或常數緩衝區之 [**D3D11 \_ 緩衝區 \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc)的 **usage** 成員中指定 [**D3D11 \_ 使用 \_ 動態**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)值，並在 [**D3D11 \_ TEXTURE2D \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc)的 **usage** 成員中，為2d 材質指定 **D3D11 \_ 使用 \_ 動態** 值。</span><span class="sxs-lookup"><span data-stu-id="40f93-124">For example, specify the [**D3D11\_USAGE\_DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) value in the **Usage** member of [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) for a vertex or constant buffer and specify the **D3D11\_USAGE\_DYNAMIC** value in the **Usage** member of [**D3D11\_TEXTURE2D\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) for a 2D texture.</span></span>
2.  <span data-ttu-id="40f93-125">將資源指定為可寫入。</span><span class="sxs-lookup"><span data-stu-id="40f93-125">Specify the resource as writable.</span></span> <span data-ttu-id="40f93-126">例如，在 [**D3D11 \_ BUFFER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc)或 [**D3D11 \_ TEXTURE2D \_ Desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc)的 **CPUAccessFlags** 成員中，指定 [**D3D11 \_ CPU \_ 存取 \_ 寫入**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag)值。</span><span class="sxs-lookup"><span data-stu-id="40f93-126">For example, specify the [**D3D11\_CPU\_ACCESS\_WRITE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag) value in the **CPUAccessFlags** member of [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) or [**D3D11\_TEXTURE2D\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc).</span></span>
3.  <span data-ttu-id="40f93-127">將資源描述傳遞給建立函數。</span><span class="sxs-lookup"><span data-stu-id="40f93-127">Pass the resource description to the creation function.</span></span> <span data-ttu-id="40f93-128">例如，將 [**D3D11 \_ 緩衝區 \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) 的位址傳遞至 [**ID3D11Device：： CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) ，並將 [**D3D11 \_ TEXTURE2D \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) 的位址傳遞至 [**ID3D11Device：： CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d)。</span><span class="sxs-lookup"><span data-stu-id="40f93-128">For example, pass the address of [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) to [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) and pass the address of [**D3D11\_TEXTURE2D\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) to [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d).</span></span>

<span data-ttu-id="40f93-129">以下是建立動態頂點緩衝區的範例：</span><span class="sxs-lookup"><span data-stu-id="40f93-129">Here is an example of creating a dynamic vertex buffer:</span></span>


```C++
    // Create a vertex buffer for a triangle.

    float2 triangleVertices[] =
    {
        float2(-0.5f, -0.5f),
        float2(0.0f, 0.5f),
        float2(0.5f, -0.5f),
    };

    D3D11_BUFFER_DESC vertexBufferDesc = { 0 };
    vertexBufferDesc.ByteWidth = sizeof(float2)* ARRAYSIZE(triangleVertices);
    vertexBufferDesc.Usage = D3D11_USAGE_DYNAMIC;
    vertexBufferDesc.BindFlags = D3D11_BIND_VERTEX_BUFFER;
    vertexBufferDesc.CPUAccessFlags = D3D11_CPU_ACCESS_WRITE;
    vertexBufferDesc.MiscFlags = 0;
    vertexBufferDesc.StructureByteStride = 0;

    D3D11_SUBRESOURCE_DATA vertexBufferData;
    vertexBufferData.pSysMem = triangleVertices;
    vertexBufferData.SysMemPitch = 0;
    vertexBufferData.SysMemSlicePitch = 0;

    DX::ThrowIfFailed(
        m_d3dDevice->CreateBuffer(
        &vertexBufferDesc,
        &vertexBufferData,
        &vertexBuffer2
        )
        );

```



### <a name="step-2-change-a-dynamic-resource"></a><span data-ttu-id="40f93-130">步驟2：變更動態資源</span><span class="sxs-lookup"><span data-stu-id="40f93-130">Step 2: Change a dynamic resource</span></span>

<span data-ttu-id="40f93-131">如果您在建立資源時將其指定為動態，您稍後可以對該資源進行變更。</span><span class="sxs-lookup"><span data-stu-id="40f93-131">If you specified a resource as dynamic and writable when you created it, you can later make changes to that resource.</span></span>

<span data-ttu-id="40f93-132">**變更動態資源中的資料**</span><span class="sxs-lookup"><span data-stu-id="40f93-132">**To change data in a dynamic resource**</span></span>

1.  <span data-ttu-id="40f93-133">設定資源的新資料。</span><span class="sxs-lookup"><span data-stu-id="40f93-133">Set up the new data for the resource.</span></span> <span data-ttu-id="40f93-134">宣告 [**D3D11 \_ 對應的 \_ SUBRESOURCE**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) 類型變數，並將它初始化為零。</span><span class="sxs-lookup"><span data-stu-id="40f93-134">Declare a [**D3D11\_MAPPED\_SUBRESOURCE**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) type variable and initialize it to zero.</span></span> <span data-ttu-id="40f93-135">您將使用此變數來變更資源。</span><span class="sxs-lookup"><span data-stu-id="40f93-135">You'll use this variable to change the resource.</span></span>
2.  <span data-ttu-id="40f93-136">停用圖形處理單元 (GPU) 您要變更的資料存取，並取得包含資料之記憶體的指標。</span><span class="sxs-lookup"><span data-stu-id="40f93-136">Disable graphics processing unit (GPU) access to the data that you want to change and get a pointer to the memory that contains the data.</span></span> <span data-ttu-id="40f93-137">若要取得這個指標，請在呼叫 [**>id3d11devicecoNtext：： MAP**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)時，將 [**D3D11 \_ MAP \_ WRITE \_ 捨棄**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map)傳遞給 *MapType* 參數。</span><span class="sxs-lookup"><span data-stu-id="40f93-137">To get this pointer, pass [**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) to the *MapType* parameter when you call [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).</span></span> <span data-ttu-id="40f93-138">將此指標設定為上一個步驟中 [**D3D11 \_ 對應 \_ SUBRESOURCE**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) 變數的位址。</span><span class="sxs-lookup"><span data-stu-id="40f93-138">Set this pointer to the address of the [**D3D11\_MAPPED\_SUBRESOURCE**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) variable from the previous step.</span></span>
3.  <span data-ttu-id="40f93-139">將新資料寫入至記憶體。</span><span class="sxs-lookup"><span data-stu-id="40f93-139">Write the new data to the memory.</span></span>
4.  <span data-ttu-id="40f93-140">當您完成寫入新資料時，請呼叫 [**>id3d11devicecoNtext：：**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) 取消對應來重新啟用資料的 GPU 存取。</span><span class="sxs-lookup"><span data-stu-id="40f93-140">Call [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) to reenable GPU access to the data when you're finished writing the new data.</span></span>

<span data-ttu-id="40f93-141">以下是變更動態頂點緩衝區的範例：</span><span class="sxs-lookup"><span data-stu-id="40f93-141">Here is an example of changing a dynamic vertex buffer:</span></span>


```C++
// This might get called as the result of a click event to double the size of the triangle.
void TriangleRenderer::MapDoubleVertices()
{
    D3D11_MAPPED_SUBRESOURCE mappedResource;
    ZeroMemory(&mappedResource, sizeof(D3D11_MAPPED_SUBRESOURCE));
    float2 vertices[] =
    {
        float2(-1.0f, -1.0f),
        float2(0.0f, 1.0f),
        float2(1.0f, -1.0f),
    };
    //  Disable GPU access to the vertex buffer data.
    auto m_d3dContext = m_deviceResources->GetD3DDeviceContext();
    m_d3dContext->Map(vertexBuffer2.Get(), 0, D3D11_MAP_WRITE_DISCARD, 0, &mappedResource);
    //  Update the vertex buffer here.
    memcpy(mappedResource.pData, vertices, sizeof(vertices));
    //  Reenable GPU access to the vertex buffer data.
    m_d3dContext->Unmap(vertexBuffer2.Get(), 0);
}
```



## <a name="remarks"></a><span data-ttu-id="40f93-142">備註</span><span class="sxs-lookup"><span data-stu-id="40f93-142">Remarks</span></span>

### <a name="using-dynamic-textures"></a><span data-ttu-id="40f93-143">使用動態紋理</span><span class="sxs-lookup"><span data-stu-id="40f93-143">Using dynamic textures</span></span>

<span data-ttu-id="40f93-144">建議您只針對每個格式建立一個動態材質，而且可能每個大小。</span><span class="sxs-lookup"><span data-stu-id="40f93-144">We recommend that you create only one dynamic texture per format and possibly per size.</span></span> <span data-ttu-id="40f93-145">由於對應每個層級的額外負荷，因此不建議您建立動態 mipmap、cube 和磁片區。</span><span class="sxs-lookup"><span data-stu-id="40f93-145">We don't recommend creating dynamic mipmaps, cubes, and volumes because of the additional overhead in mapping every level.</span></span> <span data-ttu-id="40f93-146">針對 mipmap，您可以在最上層指定 [**D3D11 \_ 對應 \_ 寫入 \_ 捨棄**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) 。</span><span class="sxs-lookup"><span data-stu-id="40f93-146">For mipmaps, you can specify [**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) only on the top level.</span></span> <span data-ttu-id="40f93-147">所有層級都是藉由只對應最上層來捨棄。</span><span class="sxs-lookup"><span data-stu-id="40f93-147">All levels are discarded by mapping just the top level.</span></span> <span data-ttu-id="40f93-148">此行為對於磁片區和 cube 而言是相同的。</span><span class="sxs-lookup"><span data-stu-id="40f93-148">This behavior is the same for volumes and cubes.</span></span> <span data-ttu-id="40f93-149">針對 cube，會對應最上層和臉部0。</span><span class="sxs-lookup"><span data-stu-id="40f93-149">For cubes, the top level and face 0 are mapped.</span></span>

### <a name="using-dynamic-buffers"></a><span data-ttu-id="40f93-150">使用動態緩衝區</span><span class="sxs-lookup"><span data-stu-id="40f93-150">Using dynamic buffers</span></span>

<span data-ttu-id="40f93-151">當您在 GPU 使用緩衝區時，于靜態頂點緩衝區上呼叫 [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) 時，會產生顯著的效能影響。</span><span class="sxs-lookup"><span data-stu-id="40f93-151">When you call [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) on a static vertex buffer while the GPU is using the buffer, you get a significant performance penalty.</span></span> <span data-ttu-id="40f93-152">在這種情況下， **map** 必須等到 GPU 完成從緩衝區讀取頂點或索引資料之後， **對應** 才能返回呼叫的應用程式，這會導致明顯的延遲。</span><span class="sxs-lookup"><span data-stu-id="40f93-152">In this situation, **Map** must wait until the GPU is finished reading vertex or index data from the buffer before **Map** can return to the calling app, which causes a significant delay.</span></span> <span data-ttu-id="40f93-153">呼叫 **map** ，然後針對每個框架從靜態緩衝區轉譯數次，也可防止 GPU 緩衝轉譯命令，因為它必須在傳回 Map 指標之前完成命令。</span><span class="sxs-lookup"><span data-stu-id="40f93-153">Calling **Map** and then rendering from a static buffer several times per frame also prevents the GPU from buffering rendering commands because it must finish commands before returning the map pointer.</span></span> <span data-ttu-id="40f93-154">如果沒有緩衝的命令，GPU 會保持閒置，直到應用程式完成填滿頂點緩衝區或索引緩衝區，併發出轉譯命令為止。</span><span class="sxs-lookup"><span data-stu-id="40f93-154">Without buffered commands, the GPU remains idle until after the app is finished filling the vertex buffer or index buffer and issues a rendering command.</span></span>

<span data-ttu-id="40f93-155">在理想的情況下，頂點或索引資料永遠不會變更，但這並不一定可行。</span><span class="sxs-lookup"><span data-stu-id="40f93-155">Ideally the vertex or index data would never change, but this is not always possible.</span></span> <span data-ttu-id="40f93-156">在許多情況下，應用程式需要變更每個畫面格的頂點或索引資料，甚至是每個框架的次數。</span><span class="sxs-lookup"><span data-stu-id="40f93-156">There are many situations where the app needs to change vertex or index data every frame, perhaps even multiple times per frame.</span></span> <span data-ttu-id="40f93-157">在這些情況下，我們建議您建立具有 [**\_ \_ 動態 D3D11 使用**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)方式的頂點或索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="40f93-157">For these situations, we recommend that you create the vertex or index buffer with [**D3D11\_USAGE\_DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage).</span></span> <span data-ttu-id="40f93-158">此使用旗標會讓執行時間針對頻繁的對應作業進行優化。</span><span class="sxs-lookup"><span data-stu-id="40f93-158">This usage flag causes the runtime to optimize for frequent map operations.</span></span> <span data-ttu-id="40f93-159">**D3D11 \_只有 \_** 當緩衝區經常對應時，使用動態才有用;如果資料仍維持不變，請將該資料放在靜態頂點或索引緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="40f93-159">**D3D11\_USAGE\_DYNAMIC** is only useful when the buffer is mapped frequently; if data is to remain constant, place that data in a static vertex or index buffer.</span></span>

<span data-ttu-id="40f93-160">若要在使用動態頂點緩衝區時獲得效能改進，您的應用程式必須使用適當的 [**D3D11 \_ 對應**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map)值來呼叫 [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) 。</span><span class="sxs-lookup"><span data-stu-id="40f93-160">To receive a performance improvement when you use dynamic vertex buffers, your app must call [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) with the appropriate [**D3D11\_MAP**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) values.</span></span> <span data-ttu-id="40f93-161">[**D3D11 \_對應 \_ 寫入 \_ 捨棄**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) 表示應用程式不需要將舊的頂點或索引資料保留在緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="40f93-161">[**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) indicates that the app doesn't need to keep the old vertex or index data in the buffer.</span></span> <span data-ttu-id="40f93-162">當您使用 **D3D11 \_ 對應 \_ 寫入 \_ 捨棄** 來呼叫 **Map** 時，如果 GPU 仍在使用緩衝區，則執行時間會傳回新的記憶體區域的指標，而不是舊的緩衝區資料。</span><span class="sxs-lookup"><span data-stu-id="40f93-162">If the GPU is still using the buffer when you call **Map** with **D3D11\_MAP\_WRITE\_DISCARD**, the runtime returns a pointer to a new region of memory instead of the old buffer data.</span></span> <span data-ttu-id="40f93-163">這可讓 GPU 在應用程式將資料放在新的緩衝區時，繼續使用舊的資料。</span><span class="sxs-lookup"><span data-stu-id="40f93-163">This allows the GPU to continue using the old data while the app places data in the new buffer.</span></span> <span data-ttu-id="40f93-164">應用程式不需要額外的記憶體管理;當 GPU 完成時，會自動重複使用或終結舊的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="40f93-164">No additional memory management is required in the app; the old buffer is reused or destroyed automatically when the GPU is finished with it.</span></span>

> [!Note]  
> <span data-ttu-id="40f93-165">當您對應具有 [**D3D11 \_ 對應 \_ 寫入 \_ 捨棄**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map)的緩衝區時，執行時間一律會捨棄整個緩衝區。</span><span class="sxs-lookup"><span data-stu-id="40f93-165">When you map a buffer with [**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map), the runtime always discards the entire buffer.</span></span> <span data-ttu-id="40f93-166">您無法藉由指定非零位移或受限大小欄位，來保留緩衝區未對應區域中的資訊。</span><span class="sxs-lookup"><span data-stu-id="40f93-166">You can't preserve info in unmapped areas of the buffer by specifying a nonzero offset or limited size field.</span></span>

 

<span data-ttu-id="40f93-167">在某些情況下，應用程式在每個地圖上儲存的資料量很小，例如新增四個頂點以呈現 sprite。</span><span class="sxs-lookup"><span data-stu-id="40f93-167">There are cases where the amount of data the app needs to store per map is small, such as adding four vertices to render a sprite.</span></span> <span data-ttu-id="40f93-168">[**D3D11 \_「對應 \_ 寫入 \_ 無 \_ 覆寫**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) 」表示應用程式不會覆寫動態緩衝區中已在使用中的資料。</span><span class="sxs-lookup"><span data-stu-id="40f93-168">[**D3D11\_MAP\_WRITE\_NO\_OVERWRITE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) indicates that the app will not overwrite data already in use in the dynamic buffer.</span></span> <span data-ttu-id="40f93-169">[**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)呼叫會傳回舊資料的指標，讓應用程式能夠在頂點或索引緩衝區未使用的區域中加入新的資料。</span><span class="sxs-lookup"><span data-stu-id="40f93-169">The [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) call will return a pointer to the old data, which will allow the app to add new data in unused regions of the vertex or index buffer.</span></span> <span data-ttu-id="40f93-170">應用程式不能修改繪製作業中使用的頂點或索引，因為它們可能仍在 GPU 中使用。</span><span class="sxs-lookup"><span data-stu-id="40f93-170">The app must not modify vertices or indices that are used in a draw operation as they might still be in use by the GPU.</span></span> <span data-ttu-id="40f93-171">我們建議應用程式在動態緩衝區填滿之後，使用 [**D3D11 \_ 對應 \_ 寫入 \_ 捨棄**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) ，以接收新的記憶體區域，這會在 GPU 完成之後捨棄舊的頂點或索引資料。</span><span class="sxs-lookup"><span data-stu-id="40f93-171">We recommend that the app then use [**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) after the dynamic buffer is full to receive a new region of memory, which discards the old vertex or index data after the GPU is finished.</span></span>

<span data-ttu-id="40f93-172">非同步查詢機制很適合用來判斷 GPU 是否仍在使用頂點。</span><span class="sxs-lookup"><span data-stu-id="40f93-172">The asynchronous query mechanism is useful to determine if vertices are still in use by the GPU.</span></span> <span data-ttu-id="40f93-173">在使用頂點的最後一個繪製呼叫之後，發出類型 [**D3D11 \_ query \_ 事件**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_query) 的查詢。</span><span class="sxs-lookup"><span data-stu-id="40f93-173">Issue a query of type [**D3D11\_QUERY\_EVENT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_query) after the last draw call that uses the vertices.</span></span> <span data-ttu-id="40f93-174">當 [**>id3d11devicecoNtext：：：：：：**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-getdata) 時，不會再使用頂點 \_ 。</span><span class="sxs-lookup"><span data-stu-id="40f93-174">The vertices are no longer in use when [**ID3D11DeviceContext::GetData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-getdata) returns S\_OK.</span></span> <span data-ttu-id="40f93-175">當您對應具有 [**D3D11 \_ map \_ WRITE \_ 捨棄**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) 或無對應值的緩衝區時，一律保證頂點會與 GPU 正確地同步處理。</span><span class="sxs-lookup"><span data-stu-id="40f93-175">When you map a buffer with [**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) or no map values, you are always guaranteed that the vertices are synchronized properly with the GPU.</span></span> <span data-ttu-id="40f93-176">但是，當您對應但未對應值時，將會產生稍早所述的效能負面影響。</span><span class="sxs-lookup"><span data-stu-id="40f93-176">But, when you map without map values, you will incur the performance penalty described earlier.</span></span>

> [!Note]  
> <span data-ttu-id="40f93-177">從 Windows 8 開始提供的 Direct3D 11.1 執行時間，可讓您將動態常數緩衝區和著色器資源流覽 (SRVs) 動態緩衝區，並將 [**D3D11 \_ 對應 \_ 寫入 [ \_ 不 \_ 覆寫**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map)]。</span><span class="sxs-lookup"><span data-stu-id="40f93-177">The Direct3D 11.1 runtime, which is available starting with Windows 8, enables mapping dynamic constant buffers and shader resource views (SRVs) of dynamic buffers with [**D3D11\_MAP\_WRITE\_NO\_OVERWRITE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map).</span></span> <span data-ttu-id="40f93-178">Direct3D 11 和舊版執行時間限制對頂點或索引緩衝區的無覆寫部分更新對應。</span><span class="sxs-lookup"><span data-stu-id="40f93-178">The Direct3D 11 and earlier runtimes limited no-overwrite partial-update mapping to vertex or index buffers.</span></span> <span data-ttu-id="40f93-179">若要判斷 Direct3D 裝置是否支援這些功能，請使用 [**D3D11 \_ 功能 \_ D3D11 \_ 選項**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature)來呼叫 [**ID3D11Device：： CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) 。</span><span class="sxs-lookup"><span data-stu-id="40f93-179">To determine if a Direct3D device supports these features, call [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) with [**D3D11\_FEATURE\_D3D11\_OPTIONS**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature).</span></span> <span data-ttu-id="40f93-180">**CheckFeatureSupport** 會以裝置的功能填滿 [**D3D11 \_ 功能 \_ 資料 \_ D3D11 \_ 選項**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) 結構的成員。</span><span class="sxs-lookup"><span data-stu-id="40f93-180">**CheckFeatureSupport** fills members of a [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) structure with the device's features.</span></span> <span data-ttu-id="40f93-181">這裡的相關成員是 **MapNoOverwriteOnDynamicConstantBuffer** 和 **MapNoOverwriteOnDynamicBufferSRV**。</span><span class="sxs-lookup"><span data-stu-id="40f93-181">The relevant members here are **MapNoOverwriteOnDynamicConstantBuffer** and **MapNoOverwriteOnDynamicBufferSRV**.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="40f93-182">相關主題</span><span class="sxs-lookup"><span data-stu-id="40f93-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40f93-183">如何使用 Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="40f93-183">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 





---
description: 建立緩衝區需要定義緩衝區將儲存的資料、提供初始化資料，以及設定適當的使用方式和系結旗標。 若要建立紋理，請參閱建立 (Direct3D 10) 的材質資源。
ms.assetid: 9787b153-9301-4a0f-bd6f-21cc6f7fc650
title: " (Direct3D 10) 建立緩衝區資源"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d711265775c430728fbcffecd364f746580a566
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688935"
---
# <a name="creating-buffer-resources-direct3d-10"></a><span data-ttu-id="6ab45-104"> (Direct3D 10) 建立緩衝區資源</span><span class="sxs-lookup"><span data-stu-id="6ab45-104">Creating Buffer Resources (Direct3D 10)</span></span>

<span data-ttu-id="6ab45-105">建立緩衝區需要定義緩衝區將儲存的資料、提供初始化資料，以及設定適當的使用方式和系結旗標。</span><span class="sxs-lookup"><span data-stu-id="6ab45-105">Creating buffers requires defining the data that the buffer will store, providing initialization data, and setting up appropriate usage and binding flags.</span></span> <span data-ttu-id="6ab45-106">若要建立紋理，請參閱 [建立 (Direct3D 10) 的材質資源 ](d3d10-graphics-programming-guide-resources-creating-textures.md)。</span><span class="sxs-lookup"><span data-stu-id="6ab45-106">To create textures, see [Creating Texture Resources (Direct3D 10)](d3d10-graphics-programming-guide-resources-creating-textures.md).</span></span>

-   [<span data-ttu-id="6ab45-107">建立頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6ab45-107">Create a Vertex Buffer</span></span>](#create-a-vertex-buffer)
    -   [<span data-ttu-id="6ab45-108">建立緩衝區描述</span><span class="sxs-lookup"><span data-stu-id="6ab45-108">Create a Buffer Description</span></span>](#create-a-buffer-description)
    -   [<span data-ttu-id="6ab45-109">建立緩衝區的初始化資料</span><span class="sxs-lookup"><span data-stu-id="6ab45-109">Create the Initialization Data for the Buffer</span></span>](#create-the-initialization-data-for-the-buffer)
    -   [<span data-ttu-id="6ab45-110">建立緩衝區</span><span class="sxs-lookup"><span data-stu-id="6ab45-110">Create the Buffer</span></span>](#create-the-buffer)
-   [<span data-ttu-id="6ab45-111">建立索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6ab45-111">Create an Index Buffer</span></span>](#create-an-index-buffer)
-   [<span data-ttu-id="6ab45-112">建立常數緩衝區</span><span class="sxs-lookup"><span data-stu-id="6ab45-112">Create a Constant Buffer</span></span>](#create-a-constant-buffer)
-   [<span data-ttu-id="6ab45-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="6ab45-113">Related topics</span></span>](#related-topics)

## <a name="create-a-vertex-buffer"></a><span data-ttu-id="6ab45-114">建立頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6ab45-114">Create a Vertex Buffer</span></span>

<span data-ttu-id="6ab45-115">建立 [頂點緩衝區](d3d10-graphics-programming-guide-resources-types.md) 的步驟如下所示。</span><span class="sxs-lookup"><span data-stu-id="6ab45-115">The steps to creating a [vertex buffer](d3d10-graphics-programming-guide-resources-types.md) are as follows.</span></span>

-   [<span data-ttu-id="6ab45-116">建立緩衝區描述</span><span class="sxs-lookup"><span data-stu-id="6ab45-116">Create a Buffer Description</span></span>](#create-a-buffer-description)
-   [<span data-ttu-id="6ab45-117">建立緩衝區的初始化資料</span><span class="sxs-lookup"><span data-stu-id="6ab45-117">Create the Initialization Data for the Buffer</span></span>](#create-the-initialization-data-for-the-buffer)
-   [<span data-ttu-id="6ab45-118">建立緩衝區</span><span class="sxs-lookup"><span data-stu-id="6ab45-118">Create the Buffer</span></span>](#create-the-buffer)

### <a name="create-a-buffer-description"></a><span data-ttu-id="6ab45-119">建立緩衝區描述</span><span class="sxs-lookup"><span data-stu-id="6ab45-119">Create a Buffer Description</span></span>

<span data-ttu-id="6ab45-120">建立頂點緩衝區時，緩衝區描述 (查看 [**D3D10 \_ 緩衝區 \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_buffer_desc)) 用來定義資料在緩衝區內的組織方式、管線如何存取緩衝區，以及將如何使用緩衝區。</span><span class="sxs-lookup"><span data-stu-id="6ab45-120">When creating a vertex buffer, a buffer description (see [**D3D10\_BUFFER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_buffer_desc)) is used to define how data is organized within the buffer, how the pipeline can access the buffer, and how the buffer will be used.</span></span>

<span data-ttu-id="6ab45-121">下列範例示範如何針對包含位置和色彩值的頂點，建立單一三角形的緩衝區描述。</span><span class="sxs-lookup"><span data-stu-id="6ab45-121">The following example demonstrates how to create a buffer description for a single triangle with vertices that contain position and color values.</span></span>


```
struct SimpleVertex
{
    D3DXVECTOR3 Position;  
    D3DXVECTOR3 Color;  
};

    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage            = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth        = sizeof( SimpleVertex ) * 3;
    bufferDesc.BindFlags        = D3D10_BIND_VERTEX_BUFFER;
    bufferDesc.CPUAccessFlags   = 0;
    bufferDesc.MiscFlags        = 0;
```



<span data-ttu-id="6ab45-122">在此範例中，會使用幾乎所有預設設定來初始化緩衝區描述，以 [**使用**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)、 [**CPU 存取**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag) 和 [**其他旗標**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)。</span><span class="sxs-lookup"><span data-stu-id="6ab45-122">In this example, the buffer description is initialized with almost all default settings for [**usage**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage), [**CPU access**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag) and [**miscellaneous flags**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag).</span></span> <span data-ttu-id="6ab45-123">其他設定適用于系結 [**旗**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag) 標，將資源識別為僅限頂點緩衝區，以及緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="6ab45-123">The other settings are for the [**bind flag**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag) which identifies the resource as a vertex buffer only, and the size of the buffer.</span></span>

<span data-ttu-id="6ab45-124">使用方式和 CPU 存取旗標對於效能而言很重要。</span><span class="sxs-lookup"><span data-stu-id="6ab45-124">The usage and CPU access flags are important for performance.</span></span> <span data-ttu-id="6ab45-125">這兩個旗標一起決定了資源的存取頻率、資源可以載入哪些記憶體類型，以及哪些處理器需要存取資源。</span><span class="sxs-lookup"><span data-stu-id="6ab45-125">These two flags together determine how often a resource gets accessed, what type of memory the resource could be loaded into, and what processor needs to access the resource.</span></span> <span data-ttu-id="6ab45-126">預設使用此資源將不會經常更新。</span><span class="sxs-lookup"><span data-stu-id="6ab45-126">Default usage this resource will not be updated very often.</span></span> <span data-ttu-id="6ab45-127">將 CPU 存取設定為0表示 CPU 將不需要讀取或寫入資源。</span><span class="sxs-lookup"><span data-stu-id="6ab45-127">Setting CPU access to 0 means that the CPU will not need to either read or write the resource.</span></span> <span data-ttu-id="6ab45-128">這表示由於資源不需要 CPU 存取，因此執行時間可以將資源載入至 GPU 最高效能的記憶體。</span><span class="sxs-lookup"><span data-stu-id="6ab45-128">Taken in combination, this means that the runtime can load the resource into the highest performing memory for the GPU since the resource does not require CPU access.</span></span>

<span data-ttu-id="6ab45-129">如同預期，這兩個處理器之間的最佳效能與任何時間可存取性之間有取捨。</span><span class="sxs-lookup"><span data-stu-id="6ab45-129">As expected, there is a tradeoff between best performance and any-time accessibility by either processor.</span></span> <span data-ttu-id="6ab45-130">例如，沒有 CPU 存取的預設使用方式表示可將資源提供給 GPU 專用。</span><span class="sxs-lookup"><span data-stu-id="6ab45-130">For example, the default usage with no CPU access means that the resource can be made available to the GPU exclusively.</span></span> <span data-ttu-id="6ab45-131">這可能包括將資源載入至記憶體中，但 CPU 無法直接存取。</span><span class="sxs-lookup"><span data-stu-id="6ab45-131">This could include loading the resource into memory not directly accessible by the CPU.</span></span> <span data-ttu-id="6ab45-132">資源只能使用 [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource)來修改。</span><span class="sxs-lookup"><span data-stu-id="6ab45-132">The resource could only be modified with [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource).</span></span>

### <a name="create-the-initialization-data-for-the-buffer"></a><span data-ttu-id="6ab45-133">建立緩衝區的初始化資料</span><span class="sxs-lookup"><span data-stu-id="6ab45-133">Create the Initialization Data for the Buffer</span></span>

<span data-ttu-id="6ab45-134">緩衝區只是專案的集合，而且會配置為一維陣列。</span><span class="sxs-lookup"><span data-stu-id="6ab45-134">A buffer is just a collection of elements and is laid out as a 1D array.</span></span> <span data-ttu-id="6ab45-135">如此一來，系統記憶體的間距和系統記憶體配量的兩端都相同;頂點資料宣告的大小。</span><span class="sxs-lookup"><span data-stu-id="6ab45-135">As a result, the system memory pitch and system memory slice pitch are both the same; the size of the vertex data declaration.</span></span> <span data-ttu-id="6ab45-136">當使用 [**subresource 描述**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_subresource_data)建立緩衝區時，應用程式可以提供初始化資料，其中包含實際資源資料的指標，以及包含該資料之大小和配置的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6ab45-136">An application can provide initialization data when a buffer is created using a [**subresource description**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_subresource_data), which contains a pointer to the actual resource data and contains information about the size and layout of that data.</span></span>

<span data-ttu-id="6ab45-137">以不可變的使用方式建立的任何緩衝區 (查看 [**D3D10 \_ 用法 \_ 不可變**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) 的) 必須在建立時初始化。</span><span class="sxs-lookup"><span data-stu-id="6ab45-137">Any buffer created with immutable usage (see [**D3D10\_USAGE\_IMMUTABLE**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)) must be initialized at creation time.</span></span> <span data-ttu-id="6ab45-138">使用 [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource)、 [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion)和 [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource)進行初始化之後，或使用 [**Map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10buffer-map) 方法存取其基礎記憶體之後，可以更新使用任何其他使用旗標的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="6ab45-138">Buffers that use any of the other usage flags can be updated after initialization using [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource), [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion), and [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource), or by accessing its underlying memory using the [**Map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10buffer-map) method.</span></span>

### <a name="create-the-buffer"></a><span data-ttu-id="6ab45-139">建立緩衝區</span><span class="sxs-lookup"><span data-stu-id="6ab45-139">Create the Buffer</span></span>

<span data-ttu-id="6ab45-140">使用緩衝區描述和初始化資料 (這是選擇性的) 呼叫 [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer) 來建立頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="6ab45-140">Using the buffer description and the initialization data (which is optional) call [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer) to create a vertex buffer.</span></span> <span data-ttu-id="6ab45-141">下列程式碼片段示範如何從應用程式所宣告的頂點資料陣列建立頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="6ab45-141">The following code snippet demonstrates how to create a vertex buffer from an array of vertex data declared by the application.</span></span>


```
struct SimpleVertexCombined
{
    D3DXVECTOR3 Pos;  
    D3DXVECTOR3 Col;  
};


ID3D10InputLayout* g_pVertexLayout = NULL;
ID3D10Buffer*      g_pVertexBuffer[2] = { NULL, NULL };
ID3D10Buffer*      g_pIndexBuffer = NULL;


SimpleVertexCombined verticesCombo[] =
{
    D3DXVECTOR3( 0.0f, 0.5f, 0.5f ),
    D3DXVECTOR3( 0.0f, 0.0f, 0.5f ),
    D3DXVECTOR3( 0.5f, -0.5f, 0.5f ),
    D3DXVECTOR3( 0.5f, 0.0f, 0.0f ),
    D3DXVECTOR3( -0.5f, -0.5f, 0.5f ),
    D3DXVECTOR3( 0.0f, 0.5f, 0.0f ),
};


    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage            = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth        = sizeof( SimpleVertexCombined ) * 3;
    bufferDesc.BindFlags        = D3D10_BIND_VERTEX_BUFFER;
    bufferDesc.CPUAccessFlags   = 0;
    bufferDesc.MiscFlags        = 0;
    
    D3D10_SUBRESOURCE_DATA InitData;
    InitData.pSysMem = verticesCombo;
    InitData.SysMemPitch = 0;
    InitData.SysMemSlicePitch = 0;
    hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pVertexBuffer[0] );
```



## <a name="create-an-index-buffer"></a><span data-ttu-id="6ab45-142">建立索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6ab45-142">Create an Index Buffer</span></span>

<span data-ttu-id="6ab45-143">建立索引緩衝區與建立頂點緩衝區非常類似;有兩個差異。</span><span class="sxs-lookup"><span data-stu-id="6ab45-143">Creating an index buffer is very similar to creating a vertex buffer; with two differences.</span></span> <span data-ttu-id="6ab45-144">索引緩衝區只包含16位或32位的資料 (，而不是頂點緩衝區可用的各種格式。</span><span class="sxs-lookup"><span data-stu-id="6ab45-144">An index buffer contains only 16-bit or 32-bit data (instead of the wide range of formats available to a vertex buffer.</span></span> <span data-ttu-id="6ab45-145">索引緩衝區也需要索引緩衝區系結旗標。</span><span class="sxs-lookup"><span data-stu-id="6ab45-145">An index buffer also requires an index-buffer bind flag.</span></span>

<span data-ttu-id="6ab45-146">下列範例示範如何從索引資料的陣列建立索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="6ab45-146">The following example demonstrates how to create an index buffer from an array of index data.</span></span>


```
ID3D10Buffer *g_pIndexBuffer = NULL;

    // Create indices
    unsigned int indices[] = { 0, 1, 2 };

    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage           = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth       = sizeof( unsigned int ) * 3;
    bufferDesc.BindFlags       = D3D10_BIND_INDEX_BUFFER;
    bufferDesc.CPUAccessFlags  = 0;
    bufferDesc.MiscFlags       = 0;

    D3D10_SUBRESOURCE_DATA InitData;
    InitData.pSysMem = indices;
    InitData.SysMemPitch = 0;
    InitData.SysMemSlicePitch = 0;
    hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pIndexBuffer );
    if( FAILED( hr ) )
        return hr;
  
    g_pd3dDevice->IASetIndexBuffer( g_pIndexBuffer, DXGI_FORMAT_R32_UINT, 0 );
```



## <a name="create-a-constant-buffer"></a><span data-ttu-id="6ab45-147">建立常數緩衝區</span><span class="sxs-lookup"><span data-stu-id="6ab45-147">Create a Constant Buffer</span></span>

<span data-ttu-id="6ab45-148">Direct3D 10 引進常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="6ab45-148">Direct3D 10 introduces a constant buffer.</span></span> <span data-ttu-id="6ab45-149">常數緩衝區（或著色器常數緩衝區）是包含著色器常數的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="6ab45-149">A constant buffer, or shader constant buffer, is a buffer that contains shader constants.</span></span> <span data-ttu-id="6ab45-150">以下是建立常數緩衝區（取自 [HLSLWithoutFX10 範例](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)）的範例。</span><span class="sxs-lookup"><span data-stu-id="6ab45-150">Here is an example of creating a constant buffer, taken from the [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span></span>


```
ID3D10Buffer*   g_pConstantBuffer10 = NULL;

struct VS_CONSTANT_BUFFER
{
    D3DXMATRIX mWorldViewProj;      //mWorldViewProj will probably be global to all shaders in a project.
                                    //It's a good idea not to move it around between shaders.
    D3DXVECTOR4 vSomeVectorThatMayBeNeededByASpecificShader;
    float fSomeFloatThatMayBeNeededByASpecificShader;
    float fTime;                    //fTime may also be global to all shaders in a project.
    float fSomeFloatThatMayBeNeededByASpecificShader2;
    float fSomeFloatThatMayBeNeededByASpecificShader3;
};

    D3D10_BUFFER_DESC cbDesc;
    cbDesc.ByteWidth = sizeof( VS_CONSTANT_BUFFER );
    cbDesc.Usage = D3D10_USAGE_DYNAMIC;
    cbDesc.BindFlags = D3D10_BIND_CONSTANT_BUFFER;
    cbDesc.CPUAccessFlags = D3D10_CPU_ACCESS_WRITE;
    cbDesc.MiscFlags = 0;
    hr = g_pd3dDevice->CreateBuffer( &cbDesc, NULL, &g_pConstantBuffer10 );
    if( FAILED( hr ) )
       return hr;

    g_pd3dDevice->VSSetConstantBuffers( 0, 1, g_pConstantBuffer10 );
```



<span data-ttu-id="6ab45-151">請注意，使用 [**ID3D10Effect 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect) 介面時， **ID3D10Effect 介面** 實例會處理建立、系結和 comitting 常數緩衝區的進程。</span><span class="sxs-lookup"><span data-stu-id="6ab45-151">Note that when using the [**ID3D10Effect Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect) interface the process of creating, binding and comitting a constant buffer is handled by the **ID3D10Effect Interface** instance.</span></span> <span data-ttu-id="6ab45-152">在這種情況下，只會 nescesary 使用其中一個 GetVariable 方法（例如 [**GetVariableByName**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-getvariablebyname) ）來從效果中取得變數，並使用其中一個 SetVariable 方法（例如 [**SetMatrix**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectmatrixvariable-setmatrix)）來更新變數。</span><span class="sxs-lookup"><span data-stu-id="6ab45-152">In that case it is only nescesary to get the variable from the effect with one of the GetVariable methods such as [**GetVariableByName**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-getvariablebyname) and update the variable with one of the SetVariable methods such as [**SetMatrix**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectmatrixvariable-setmatrix).</span></span> <span data-ttu-id="6ab45-153">如需使用 **ID3D10Effect 介面** 管理常數緩衝區的範例，請參閱 [教學課程7：材質對應和常數緩衝區](https://msdn.microsoft.com/library/Ee416442(v=VS.85).aspx)。</span><span class="sxs-lookup"><span data-stu-id="6ab45-153">For an example of using **ID3D10Effect Interface** to manage a constant buffer see [Tutorial 7: Texture Mapping and Constant Buffers](https://msdn.microsoft.com/library/Ee416442(v=VS.85).aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ab45-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="6ab45-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ab45-155"> (Direct3D 10) 的資源 </span><span class="sxs-lookup"><span data-stu-id="6ab45-155">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




---
description: 如果場景包含許多使用相同幾何的物件，您可以藉由減少您需要提供給轉譯器的資料量，以不同的方向、大小、色彩等來繪製該幾何的許多實例，並大幅提升效能。
ms.assetid: d8d9b0c8-b1c4-406d-bf2a-9716d725aec7
title: '有效率地繪製多個 Geometry 實例 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9981dff913b704fca5e6b211b57e3647fddd28c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845972"
---
# <a name="efficiently-drawing-multiple-instances-of-geometry-direct3d-9"></a><span data-ttu-id="c84a3-103">有效率地繪製多個 Geometry 實例 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="c84a3-103">Efficiently Drawing Multiple Instances of Geometry (Direct3D 9)</span></span>

<span data-ttu-id="c84a3-104">如果場景包含許多使用相同幾何的物件，您可以藉由減少您需要提供給轉譯器的資料量，以不同的方向、大小、色彩等來繪製該幾何的許多實例，並大幅提升效能。</span><span class="sxs-lookup"><span data-stu-id="c84a3-104">Given a scene that contains many objects that use the same geometry, you can draw many instances of that geometry at different orientations, sizes, colors, and so on with dramatically better performance by reducing the amount of data you need to supply to the renderer.</span></span>

<span data-ttu-id="c84a3-105">您可以使用兩種方法來完成這項作業：第一個用於繪製索引幾何，第二個用於非索引幾何。</span><span class="sxs-lookup"><span data-stu-id="c84a3-105">This can be accomplished through the use of two techniques: the first for drawing indexed geometry and the second for non-indexed geometry.</span></span> <span data-ttu-id="c84a3-106">這兩種技術都使用兩個頂點緩衝區：一個用來提供幾何資料，另一個用來提供每個物件的實例資料。</span><span class="sxs-lookup"><span data-stu-id="c84a3-106">Both techniques use two vertex buffers: one to supply geometry data and one to supply per-object instance data.</span></span> <span data-ttu-id="c84a3-107">實例資料可以是各種不同的資訊，例如轉換、色彩資料或光來源資料-基本上，您可以在頂點宣告中描述的任何內容。</span><span class="sxs-lookup"><span data-stu-id="c84a3-107">The instance data can be a wide variety of information such as a transform, color data, or lighting data - basically anything that you can describe in a vertex declaration.</span></span> <span data-ttu-id="c84a3-108">使用這些技術來繪製許多幾何實例，可以大幅減少傳送至轉譯器的資料量。</span><span class="sxs-lookup"><span data-stu-id="c84a3-108">Drawing many instances of geometry with these techniques can dramatically reduce the amount of data sent to the renderer.</span></span>

-   [<span data-ttu-id="c84a3-109">繪圖索引幾何</span><span class="sxs-lookup"><span data-stu-id="c84a3-109">Drawing Indexed Geometry</span></span>](#drawing-indexed-geometry)
    -   [<span data-ttu-id="c84a3-110">索引幾何效能比較</span><span class="sxs-lookup"><span data-stu-id="c84a3-110">Indexed Geometry Performance Comparison</span></span>](#indexed-geometry-performance-comparison)
-   [<span data-ttu-id="c84a3-111">繪圖非索引幾何</span><span class="sxs-lookup"><span data-stu-id="c84a3-111">Drawing Non-Indexed Geometry</span></span>](#drawing-non-indexed-geometry)
    -   [<span data-ttu-id="c84a3-112">非索引幾何效能比較</span><span class="sxs-lookup"><span data-stu-id="c84a3-112">Non-Indexed Geometry Performance Comparison</span></span>](#non-indexed-geometry-performance-comparison)
-   [<span data-ttu-id="c84a3-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="c84a3-113">Related topics</span></span>](#related-topics)

## <a name="drawing-indexed-geometry"></a><span data-ttu-id="c84a3-114">繪圖索引幾何</span><span class="sxs-lookup"><span data-stu-id="c84a3-114">Drawing Indexed Geometry</span></span>

<span data-ttu-id="c84a3-115">頂點緩衝區包含頂點宣告所定義的每個頂點資料。</span><span class="sxs-lookup"><span data-stu-id="c84a3-115">The vertex buffer contains per-vertex data that is defined by a vertex declaration.</span></span> <span data-ttu-id="c84a3-116">假設每個頂點的部分包含幾何資料，而每個頂點的一部分包含每個物件的實例資料，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="c84a3-116">Suppose that part of each vertex contains geometry data, and part of each vertex contains per-object instance data, as shown in the following diagram.</span></span>

![索引幾何的頂點緩衝區圖表](images/drawingmultipleinstances.png)

<span data-ttu-id="c84a3-118">這項技術需要支援 3 \_ 0 頂點著色器模型的裝置。</span><span class="sxs-lookup"><span data-stu-id="c84a3-118">This technique requires a device that supports the 3\_0 vertex shader model.</span></span> <span data-ttu-id="c84a3-119">這項技術適用于任何可程式化的著色器，但不適用於固定函式管線。</span><span class="sxs-lookup"><span data-stu-id="c84a3-119">This technique works with any programmable shader but not with the fixed function pipeline.</span></span>

<span data-ttu-id="c84a3-120">針對上方所示的頂點緩衝區，以下是對應的頂點緩衝區宣告：</span><span class="sxs-lookup"><span data-stu-id="c84a3-120">For the vertex buffers shown above, here are the corresponding vertex buffer declarations:</span></span>


```
const D3DVERTEXELEMENT9 g_VBDecl_Geometry[] =
{
{0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
{0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL,   0},
{0, 24, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TANGENT,  0},
{0, 36, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BINORMAL, 0},
{0, 48, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0},
D3DDECL_END()
};

const D3DVERTEXELEMENT9 g_VBDecl_InstanceData[] =
{
{1, 0,  D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1},
{1, 16, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 2},
{1, 32, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 3},
{1, 48, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 4},
{1, 64, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_COLOR,    0},
D3DDECL_END()
};
```



<span data-ttu-id="c84a3-121">這些宣告會定義兩個頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="c84a3-121">These declarations define two vertex buffers.</span></span> <span data-ttu-id="c84a3-122">資料流程0的第一個宣告 (（以資料行1中的零表示）) 定義由： position、normal、正切、binormal 和材質座標資料組成的幾何資料。</span><span class="sxs-lookup"><span data-stu-id="c84a3-122">The first declaration (for stream 0, indicated by the zeros in column 1) defines the geometry data which consists of: position, normal, tangent, binormal, and texture coordinate data.</span></span>

<span data-ttu-id="c84a3-123">資料流程1的第二個宣告 (，由資料行1中的宣告所表示) 定義每個物件的實例資料。</span><span class="sxs-lookup"><span data-stu-id="c84a3-123">The second declaration (for stream 1, indicated by the ones in column 1) defines the per-object instance data.</span></span> <span data-ttu-id="c84a3-124">每個實例都是由 4 4-元件浮點數和四個元件的色彩所定義。</span><span class="sxs-lookup"><span data-stu-id="c84a3-124">Each instance is defined by four four-component floating point numbers, and a four-component color.</span></span> <span data-ttu-id="c84a3-125">前四個值可用來初始化4x4 矩陣，這表示此資料將會唯一調整、定位和旋轉幾何的每個實例。</span><span class="sxs-lookup"><span data-stu-id="c84a3-125">The first four values could be used to initialize a 4x4 matrix, which means that this data will uniquely size, position, and rotate each instance of the geometry.</span></span> <span data-ttu-id="c84a3-126">前四個元件使用紋理座標語義，在此案例中表示「這是一般四個元件的數位」。</span><span class="sxs-lookup"><span data-stu-id="c84a3-126">The first four components use a texture coordinate semantic which, in this case, means "this is a general four-component number."</span></span> <span data-ttu-id="c84a3-127">當您在頂點宣告中使用任意資料時，請使用材質座標語義來標示它。</span><span class="sxs-lookup"><span data-stu-id="c84a3-127">When you use arbitrary data in a vertex declaration, use a texture coordinate semantic to mark it.</span></span> <span data-ttu-id="c84a3-128">資料流程中的最後一個元素用於色彩資料。</span><span class="sxs-lookup"><span data-stu-id="c84a3-128">The last element in the stream is used for color data.</span></span> <span data-ttu-id="c84a3-129">這可以套用在頂點著色器中，為每個實例提供獨特的色彩。</span><span class="sxs-lookup"><span data-stu-id="c84a3-129">This could be applied in the vertex shader to give each instance a unique color.</span></span>

<span data-ttu-id="c84a3-130">轉譯之前，您必須呼叫 [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) ，以將頂點緩衝區資料流程系結至裝置。</span><span class="sxs-lookup"><span data-stu-id="c84a3-130">Before rendering, you need to call [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) to bind the vertex buffer streams to the device.</span></span> <span data-ttu-id="c84a3-131">以下是系結兩個頂點緩衝區的範例：</span><span class="sxs-lookup"><span data-stu-id="c84a3-131">Here is an example that binds both vertex buffers:</span></span>


```
// Set up the geometry data stream
pd3dDevice->SetStreamSourceFreq(0,
    (D3DSTREAMSOURCE_INDEXEDDATA | g_numInstancesToDraw));
pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
    D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

// Set up the instance data stream
pd3dDevice->SetStreamSourceFreq(1,
    (D3DSTREAMSOURCE_INSTANCEDATA | 1));
pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
    D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));
```



<span data-ttu-id="c84a3-132">[**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) 會使用 [D3DSTREAMSOURCE \_ INDEXEDDATA](other-direct3d-constants.md) 來識別索引幾何資料。</span><span class="sxs-lookup"><span data-stu-id="c84a3-132">[**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) uses [D3DSTREAMSOURCE\_INDEXEDDATA](other-direct3d-constants.md) to identify the indexed geometry data.</span></span> <span data-ttu-id="c84a3-133">在此情況下，stream 0 包含描述物件幾何的索引資料。</span><span class="sxs-lookup"><span data-stu-id="c84a3-133">In this case, stream 0 contains the indexed data that describes the object geometry.</span></span> <span data-ttu-id="c84a3-134">此值會以邏輯方式結合要繪製之幾何的實例數目。</span><span class="sxs-lookup"><span data-stu-id="c84a3-134">This value is logically combined with the number of instances of the geometry to draw.</span></span>

<span data-ttu-id="c84a3-135">請注意，D3DSTREAMSOURCE \_ INDEXEDDATA 和要繪製的實例數目必須一律設定在資料流程零中。</span><span class="sxs-lookup"><span data-stu-id="c84a3-135">Note that D3DSTREAMSOURCE\_INDEXEDDATA and the number of instances to draw must always be set in stream zero.</span></span>

<span data-ttu-id="c84a3-136">在第二個呼叫中， [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) 會使用 [D3DSTREAMSOURCE \_ INSTANCEDATA](other-direct3d-constants.md) 來識別包含實例資料的資料流程。</span><span class="sxs-lookup"><span data-stu-id="c84a3-136">In the second call, [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) uses [D3DSTREAMSOURCE\_INSTANCEDATA](other-direct3d-constants.md) to identify the stream containing the instance data.</span></span> <span data-ttu-id="c84a3-137">此值會以邏輯方式結合1，因為每個頂點都包含一組實例資料。</span><span class="sxs-lookup"><span data-stu-id="c84a3-137">This value is logically combined with 1 since each vertex contains one set of instance data.</span></span>

<span data-ttu-id="c84a3-138">[**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource)的最後兩個呼叫會將頂點緩衝區指標系結至裝置。</span><span class="sxs-lookup"><span data-stu-id="c84a3-138">The last two calls to [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) bind the vertex buffer pointers to the device.</span></span>

<span data-ttu-id="c84a3-139">當您完成轉譯實例資料時，請務必將頂點資料流程頻率重設回其預設狀態 (而不會使用實例) 。</span><span class="sxs-lookup"><span data-stu-id="c84a3-139">When you are finished rendering the instance data, be sure to reset the vertex stream frequency back to its default state (which does not use instancing).</span></span> <span data-ttu-id="c84a3-140">因為此範例使用兩個數據流，所以請設定這兩個數據流，如下所示：</span><span class="sxs-lookup"><span data-stu-id="c84a3-140">Because this example used two streams, set both streams as shown below:</span></span>


```
pd3dDevice->SetStreamSourceFreq(0,1);
pd3dDevice->SetStreamSourceFreq(1,1);
```



### <a name="indexed-geometry-performance-comparison"></a><span data-ttu-id="c84a3-141">索引幾何效能比較</span><span class="sxs-lookup"><span data-stu-id="c84a3-141">Indexed Geometry Performance Comparison</span></span>

<span data-ttu-id="c84a3-142">雖然這項技術可能會降低每個應用程式中轉譯時間的結果，但請考慮串流處理到執行時間的資料量差異，以及如果您使用實例技術將會降低的狀態變更數目。</span><span class="sxs-lookup"><span data-stu-id="c84a3-142">While it is not possible to make a single conclusion about how much this technique could reduce the render time in every application, consider the difference in the amount of data streamed into the runtime and the number of state changes that will be reduced if you use the instancing technique.</span></span> <span data-ttu-id="c84a3-143">此轉譯順序會利用繪製相同幾何之多個實例的優點：</span><span class="sxs-lookup"><span data-stu-id="c84a3-143">This render sequence takes advantage of drawing multiple instances of the same geometry:</span></span>


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    // Set up the geometry data stream
    pd3dDevice->SetStreamSourceFreq(0,
                (D3DSTREAMSOURCE_INDEXEDDATA | g_numInstancesToDraw));
    pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

    // Set up the instance data stream
    pd3dDevice->SetStreamSourceFreq(1,
                (D3DSTREAMSOURCE_INSTANCEDATA | 1));
    pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
                D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));

    pd3dDevice->SetVertexDeclaration( ... );
    pd3dDevice->SetVertexShader( ... );
    pd3dDevice->SetIndices( ... );

    pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    
    pd3dDevice->EndScene();
}
```



<span data-ttu-id="c84a3-144">請注意，轉譯迴圈會呼叫一次，而幾何資料會串流處理一次，而 n 個實例則會進行一次資料流程處理。</span><span class="sxs-lookup"><span data-stu-id="c84a3-144">Notice that the render loop is called once, the geometry data is streamed once, and n instances are streamed once.</span></span> <span data-ttu-id="c84a3-145">下一個轉譯順序與功能相同，但不會利用實例：</span><span class="sxs-lookup"><span data-stu-id="c84a3-145">This next render sequence is identical in functionality, but does not take advantage of instancing:</span></span>


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    for(int i=0; i < g_numObjects; i++)
    {
        pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));


        pd3dDevice->SetVertexDeclaration( ... );
        pd3dDevice->SetVertexShader( ... );
        pd3dDevice->SetIndices( ... );

        pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    }                             
    
    pd3dDevice->EndScene();
}
```



<span data-ttu-id="c84a3-146">請注意，整個轉譯迴圈是由第二個迴圈所包裝，以繪製每個物件。</span><span class="sxs-lookup"><span data-stu-id="c84a3-146">Notice that the entire render loop is wrapped by a second loop to draw each object.</span></span> <span data-ttu-id="c84a3-147">現在幾何資料會串流處理到轉譯器 n 次 (而不是一次) 而且任何管線狀態也可能會針對每個繪製的物件進行重複設定。</span><span class="sxs-lookup"><span data-stu-id="c84a3-147">Now the geometry data is streamed into the renderer n times (instead of once) and any pipeline states may also be set redundantly for each object drawn.</span></span> <span data-ttu-id="c84a3-148">此轉譯順序很可能會變得很慢。</span><span class="sxs-lookup"><span data-stu-id="c84a3-148">This render sequence is very likely to be significantly slower.</span></span> <span data-ttu-id="c84a3-149">另外也請注意，在這兩個轉譯迴圈之間， [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) 的參數並未變更。</span><span class="sxs-lookup"><span data-stu-id="c84a3-149">Notice also that the parameters to [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) have not changed between the two render loops.</span></span>

## <a name="drawing-non-indexed-geometry"></a><span data-ttu-id="c84a3-150">繪圖非索引幾何</span><span class="sxs-lookup"><span data-stu-id="c84a3-150">Drawing Non-Indexed Geometry</span></span>

<span data-ttu-id="c84a3-151">在 [繪圖索引幾何](#drawing-indexed-geometry)中，頂點緩衝區已設定為以較高的效率繪製多個索引幾何的實例。</span><span class="sxs-lookup"><span data-stu-id="c84a3-151">In [Drawing Indexed Geometry](#drawing-indexed-geometry), vertex buffers were configured to draw multiple instances of indexed geometry with greater efficiency.</span></span> <span data-ttu-id="c84a3-152">您也可以使用 [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) 來繪製非索引的幾何。</span><span class="sxs-lookup"><span data-stu-id="c84a3-152">You can also use [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) to draw non-indexed geometry.</span></span> <span data-ttu-id="c84a3-153">這需要不同的頂點緩衝區配置，且具有不同的條件約束。</span><span class="sxs-lookup"><span data-stu-id="c84a3-153">This requires a different vertex buffer layout and has different constraints.</span></span> <span data-ttu-id="c84a3-154">若要繪製非索引幾何，請準備您的頂點緩衝區，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="c84a3-154">To draw non-indexed geometry, prepare your vertex buffers like the following diagram.</span></span>

![非索引幾何的頂點緩衝區圖表](images/olderstyleinstancing.png)

<span data-ttu-id="c84a3-156">任何裝置上的硬體加速都不支援此技術。</span><span class="sxs-lookup"><span data-stu-id="c84a3-156">This technique is not supported by hardware acceleration on any device.</span></span> <span data-ttu-id="c84a3-157">它僅受軟體頂點處理的支援，而且只適用于 [vs \_ 3 \_ 0](../direct3dhlsl/dx9-graphics-reference-asm-vs-3-0.md) 著色器。</span><span class="sxs-lookup"><span data-stu-id="c84a3-157">It is only supported by software vertex processing and will work only with [vs\_3\_0](../direct3dhlsl/dx9-graphics-reference-asm-vs-3-0.md) shaders.</span></span>

<span data-ttu-id="c84a3-158">因為這項技術適用于非索引幾何，所以沒有索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="c84a3-158">Because this technique works with non-indexed geometry, there is no index buffer.</span></span> <span data-ttu-id="c84a3-159">如圖所示，包含幾何的頂點緩衝區包含幾何資料的 n 個複本。</span><span class="sxs-lookup"><span data-stu-id="c84a3-159">As the diagram shows, the vertex buffer that contains geometry contains n copies of the geometry data.</span></span> <span data-ttu-id="c84a3-160">針對每個繪製的實例，會從第一個頂點緩衝區讀取幾何資料，並從第二個頂點緩衝區讀取實例資料。</span><span class="sxs-lookup"><span data-stu-id="c84a3-160">For each instance drawn, the geometry data is read from the first vertex buffer and the instance data is read from the second vertex buffer.</span></span>

<span data-ttu-id="c84a3-161">以下是對應的頂點緩衝區宣告：</span><span class="sxs-lookup"><span data-stu-id="c84a3-161">Here are the corresponding vertex buffer declarations:</span></span>


```
const D3DVERTEXELEMENT9 g_VBDecl_Geometry[] =
{
{0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
{0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL,   0},
{0, 24, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TANGENT,  0},
{0, 36, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BINORMAL, 0},
{0, 48, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0},
D3DDECL_END()
};

const D3DVERTEXELEMENT9 g_VBDecl_InstanceData[] =
{
{1, 0,  D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1},
{1, 16, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 2},
{1, 32, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 3},
{1, 48, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 4},
{1, 64, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_COLOR,    0},
D3DDECL_END()
};
```



<span data-ttu-id="c84a3-162">這些宣告與索引幾何範例中所做的宣告相同。</span><span class="sxs-lookup"><span data-stu-id="c84a3-162">These declarations are identical to the declarations made in the indexed geometry example.</span></span> <span data-ttu-id="c84a3-163">同樣地，資料流程0的第一個宣告 () 會定義幾何資料，而針對資料流程) 1 的第二個宣告 (會定義每個物件的實例資料。</span><span class="sxs-lookup"><span data-stu-id="c84a3-163">Once again, the first declaration (for stream 0) defines the geometry data and the second declaration (for stream 1) defines the per-object instance data.</span></span> <span data-ttu-id="c84a3-164">當您建立第一個頂點緩衝區時，請務必使用您將繪製之幾何資料的實例數目來載入它。</span><span class="sxs-lookup"><span data-stu-id="c84a3-164">When you create the first vertex buffer, be sure to load it with the number of instances of the geometry data that you will be drawing.</span></span>

<span data-ttu-id="c84a3-165">在轉譯之前，您必須設定分隔線，以告訴執行時間如何將第一個頂點緩衝區分割成 n 個實例。</span><span class="sxs-lookup"><span data-stu-id="c84a3-165">Before rendering, you need to set up the divider which tells the runtime how to divide up the first vertex buffer into n instances.</span></span> <span data-ttu-id="c84a3-166">然後使用 [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) 來設定分割，如下所示：</span><span class="sxs-lookup"><span data-stu-id="c84a3-166">Then set the divider using [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) like this:</span></span>


```
// Set the divider
pd3dDevice->SetStreamSourceFreq(0, 1);
// Bind the stream to the vertex buffer
pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
        D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

// Set up the instance data stream
pd3dDevice->SetStreamSourceFreq(1, verticesPerInstance);
pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
        D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));
```



<span data-ttu-id="c84a3-167">第一次呼叫 [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) 時，會指出資料流程0包含 m 個頂點的 n 個實例。</span><span class="sxs-lookup"><span data-stu-id="c84a3-167">The first call to [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) says that stream 0 contains n instances of m vertices.</span></span> <span data-ttu-id="c84a3-168">然後， [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource)會將資料流程0系結至 geometry 頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="c84a3-168">[**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) then binds stream 0 to the geometry vertex buffer.</span></span>

<span data-ttu-id="c84a3-169">在第二個呼叫中， [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) 會將資料流程1識別為實例資料的來源。</span><span class="sxs-lookup"><span data-stu-id="c84a3-169">In the second call, [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) identifies stream 1 as the source of the instance data.</span></span> <span data-ttu-id="c84a3-170">第二個參數是每個物件中的頂點數目 (m) 。</span><span class="sxs-lookup"><span data-stu-id="c84a3-170">The second parameter is the number of vertices in each object (m).</span></span> <span data-ttu-id="c84a3-171">請記住，實例資料流程必須一律宣告為第二個數據流。</span><span class="sxs-lookup"><span data-stu-id="c84a3-171">Remember that the instance data stream must always be declared as the second stream.</span></span> <span data-ttu-id="c84a3-172">然後， [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource)會將資料流程1系結至包含實例資料的頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="c84a3-172">[**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) then binds stream 1 to the vertex buffer that contains the instance data.</span></span>

<span data-ttu-id="c84a3-173">當您完成轉譯實例資料時，請務必將頂點資料流程頻率重設回其預設狀態。</span><span class="sxs-lookup"><span data-stu-id="c84a3-173">When you are finished rendering the instance data, be sure to reset the vertex stream frequency back to its default state.</span></span> <span data-ttu-id="c84a3-174">因為此範例使用兩個數據流，所以請設定這兩個數據流，如下所示：</span><span class="sxs-lookup"><span data-stu-id="c84a3-174">Because this example used two streams, set both streams as shown below:</span></span>


```
pd3dDevice->SetStreamSourceFreq(0,1);
pd3dDevice->SetStreamSourceFreq(1,1);
```



### <a name="non-indexed-geometry-performance-comparison"></a><span data-ttu-id="c84a3-175">非索引幾何效能比較</span><span class="sxs-lookup"><span data-stu-id="c84a3-175">Non-Indexed Geometry Performance Comparison</span></span>

<span data-ttu-id="c84a3-176">此實例樣式的主要優點是它可以用於非索引的幾何。</span><span class="sxs-lookup"><span data-stu-id="c84a3-176">The major advantage of this instancing style is that it can be used on non-indexed geometry.</span></span> <span data-ttu-id="c84a3-177">雖然這項技術可能會降低每個應用程式中轉譯時間的結果，但請考慮串流處理到執行時間的資料量差異，以及將針對下列轉譯順序減少的狀態變更數目：</span><span class="sxs-lookup"><span data-stu-id="c84a3-177">While it is not possible to make a single conclusion about how much this technique could reduce the render time in every application, consider the difference in the amount of data streamed into the runtime, and the number of state changes that will be reduced for the following render sequence:</span></span>


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    // Set the divider
    pd3dDevice->SetStreamSourceFreq(0, 1);
    pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

    // Set up the instance data stream
    pd3dDevice->SetStreamSourceFreq(1, verticesPerInstance));
    pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
                D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));

    pd3dDevice->SetVertexDeclaration( ... );
    pd3dDevice->SetVertexShader( ... );
    pd3dDevice->SetIndices( ... );

    pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    
    pd3dDevice->EndScene();
}
```



<span data-ttu-id="c84a3-178">請注意，轉譯迴圈會呼叫一次。</span><span class="sxs-lookup"><span data-stu-id="c84a3-178">Notice that the render loop is called once.</span></span> <span data-ttu-id="c84a3-179">雖然資料流程的幾何有 n 個實例，但幾何資料會經過資料流程處理。</span><span class="sxs-lookup"><span data-stu-id="c84a3-179">The geometry data is streamed once although there are n instances of the geometry being streamed.</span></span> <span data-ttu-id="c84a3-180">來自實例頂點緩衝區的資料會經過資料流程處理。</span><span class="sxs-lookup"><span data-stu-id="c84a3-180">The data from the instance vertex buffer is streamed once.</span></span> <span data-ttu-id="c84a3-181">下一個轉譯順序與功能相同，但不會利用實例：</span><span class="sxs-lookup"><span data-stu-id="c84a3-181">This next render sequence is identical in functionality, but does not take advantage of instancing:</span></span>


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    for(int i=0; i < g_numObjects; i++)
    {
        pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

        pd3dDevice->SetVertexDeclaration( ... );
        pd3dDevice->SetVertexShader( ... );
        pd3dDevice->SetIndices( ... );

        pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    }
    
    pd3dDevice->EndScene();
}
```



<span data-ttu-id="c84a3-182">如果沒有實例，則必須以第二個迴圈來包裝轉譯迴圈，以繪製每個物件。</span><span class="sxs-lookup"><span data-stu-id="c84a3-182">Without instancing, the render loop needs to be wrapped by a second loop to draw each object.</span></span> <span data-ttu-id="c84a3-183">藉由消除第二個轉譯迴圈，您應該會因為在迴圈內呼叫的轉譯狀態變更較少，而預期會有較佳的效能。</span><span class="sxs-lookup"><span data-stu-id="c84a3-183">By eliminating the second render loop, you should expect better performance due to fewer render state changes that are called inside the loop.</span></span>

<span data-ttu-id="c84a3-184">整體來說，預期索引的技巧 ([繪製索引的幾何](#drawing-indexed-geometry)) 比非索引的技巧更好， ([繪製非索引的幾何](#drawing-non-indexed-geometry)) ，因為索引技巧只會串流處理一個幾何資料複本。</span><span class="sxs-lookup"><span data-stu-id="c84a3-184">Overall, it is reasonable to expect the indexed technique ([Drawing Indexed Geometry](#drawing-indexed-geometry)) to perform better than the non-indexed technique ([Drawing Non-Indexed Geometry](#drawing-non-indexed-geometry)) because the indexed technique only streams one copy of the geometry data.</span></span> <span data-ttu-id="c84a3-185">請注意，任何轉譯序列的 [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) 參數都未變更。</span><span class="sxs-lookup"><span data-stu-id="c84a3-185">Notice that the parameters to [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) have not changed for any of the render sequences.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c84a3-186">相關主題</span><span class="sxs-lookup"><span data-stu-id="c84a3-186">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c84a3-187">Advanced 主題</span><span class="sxs-lookup"><span data-stu-id="c84a3-187">Advanced Topics</span></span>](advanced-topics.md)
</dt> <dt>

<span data-ttu-id="c84a3-188">[實例範例](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="c84a3-188">[Instancing Sample](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 

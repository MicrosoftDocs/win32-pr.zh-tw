---
description: Direct3D 支援索引和非索引的繪圖方法。
ms.assetid: 9b94ab86-2a6a-4abd-ab56-95315f473226
title: '從頂點和索引緩衝區轉譯 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbc42da3f25787d42b0bdccdd808013f51bfa3e4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845960"
---
# <a name="rendering-from-vertex-and-index-buffers-direct3d-9"></a><span data-ttu-id="1cb94-103">從頂點和索引緩衝區轉譯 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="1cb94-103">Rendering from Vertex and Index Buffers (Direct3D 9)</span></span>

<span data-ttu-id="1cb94-104">Direct3D 支援索引和非索引的繪圖方法。</span><span class="sxs-lookup"><span data-stu-id="1cb94-104">Both indexed and nonindexed drawing methods are supported by Direct3D.</span></span> <span data-ttu-id="1cb94-105">索引的方法會針對所有頂點元件使用一組索引。</span><span class="sxs-lookup"><span data-stu-id="1cb94-105">The indexed methods use a single set of indices for all vertex components.</span></span> <span data-ttu-id="1cb94-106">頂點資料會儲存在頂點緩衝區中，而索引資料會儲存在索引緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="1cb94-106">Vertex data is stored in vertex buffers, and index data is stored in index buffers.</span></span> <span data-ttu-id="1cb94-107">以下列出使用頂點和索引緩衝區繪製基本專案的一些常見案例。</span><span class="sxs-lookup"><span data-stu-id="1cb94-107">Listed below are a few common scenarios for drawing primitives using vertex and index buffers.</span></span>

<span data-ttu-id="1cb94-108">這些範例會比較 IDirect3DDevice9 的使用 [**：:D rawprimitive**](/windows/desktop/api) 和 [**IDirect3DDevice9：:D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)</span><span class="sxs-lookup"><span data-stu-id="1cb94-108">These examples compare the use of [**IDirect3DDevice9::DrawPrimitive**](/windows/desktop/api) and [**IDirect3DDevice9::DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)</span></span>

## <a name="scenario-1-drawing-two-triangles-without-indexing"></a><span data-ttu-id="1cb94-109">案例1：繪製兩個三角形但不編制索引</span><span class="sxs-lookup"><span data-stu-id="1cb94-109">Scenario 1: Drawing Two Triangles without Indexing</span></span>

<span data-ttu-id="1cb94-110">假設您想要繪製下圖所示的四顆四個。</span><span class="sxs-lookup"><span data-stu-id="1cb94-110">Let's say you want to draw the quad that is shown in the following illustration.</span></span>

![由兩個三角形組成的正方形圖例](images/dip-fig1.png)

<span data-ttu-id="1cb94-112">如果您使用三角形清單基本型別來呈現兩個三角形，每個三角形都會儲存為3個個別頂點，並產生類似的頂點緩衝區給下圖。</span><span class="sxs-lookup"><span data-stu-id="1cb94-112">If you use the Triangle List primitive type to render the two triangles, each triangle will be stored as 3 individual vertices, resulting in a similar vertex buffer to the following illustration.</span></span>

![頂點緩衝區的圖表，定義兩個三角形的三個頂點](images/dip-fig2.png)

<span data-ttu-id="1cb94-114">繪圖呼叫很簡單;從頂點緩衝區內的位置0開始，繪製兩個三角形。</span><span class="sxs-lookup"><span data-stu-id="1cb94-114">The drawing call is very straightforward; starting at location 0 within the vertex buffer, draw two triangles.</span></span> <span data-ttu-id="1cb94-115">如果已啟用 [剔除]，頂點的順序將會很重要。</span><span class="sxs-lookup"><span data-stu-id="1cb94-115">If culling is enabled, the order of the vertices will be important.</span></span> <span data-ttu-id="1cb94-116">此範例假設預設的逆時針剔除狀態，因此必須以順時針順序繪製可見的三角形。</span><span class="sxs-lookup"><span data-stu-id="1cb94-116">This example assumes the default counter-clockwise culling state, so visible triangles must be drawn in clockwise order.</span></span> <span data-ttu-id="1cb94-117">三角形清單基本型別直接從每個三角形的緩衝區讀取三個頂點，因此此呼叫會繪製三角形 (0、1、2) 和 (3、4、5) ：</span><span class="sxs-lookup"><span data-stu-id="1cb94-117">The Triangle List primitive type simply reads three vertices in linear order from the buffer for each triangle, so this call will draw triangles (0, 1, 2) and (3, 4, 5):</span></span>


```
DrawPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
               0,                  // StartVertex
               2 );                // PrimitiveCount
```



## <a name="scenario-2-drawing-two-triangles-with-indexing"></a><span data-ttu-id="1cb94-118">案例2：繪製具有索引的兩個三角形</span><span class="sxs-lookup"><span data-stu-id="1cb94-118">Scenario 2: Drawing Two Triangles with Indexing</span></span>

<span data-ttu-id="1cb94-119">您將會注意到，頂點緩衝區包含位置0和4、2和5中的重復資料。</span><span class="sxs-lookup"><span data-stu-id="1cb94-119">As you'll notice, the vertex buffer contains duplicate data in locations 0 and 4, 2 and 5.</span></span> <span data-ttu-id="1cb94-120">這是合理的，因為這兩個三角形共用兩個共通頂點。</span><span class="sxs-lookup"><span data-stu-id="1cb94-120">That makes sense because the two triangles share two common vertices.</span></span> <span data-ttu-id="1cb94-121">這項重複的資料很浪費，而且可以使用索引緩衝區來壓縮頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1cb94-121">This duplicate data is wasteful, and the vertex buffer can be compressed by using an index buffer.</span></span> <span data-ttu-id="1cb94-122">較小的頂點緩衝區可減少必須傳送至圖形介面卡的頂點資料量。</span><span class="sxs-lookup"><span data-stu-id="1cb94-122">A smaller vertex buffer reduces the amount of vertex data that has to be sent to the graphics adapter.</span></span> <span data-ttu-id="1cb94-123">更重要的是，使用索引緩衝區可讓介面卡在頂點快取中儲存頂點;如果所繪製的基本物件包含最近使用的頂點，則可以從快取中提取該頂點，而不是從頂點緩衝區中讀取，這會導致大幅提升效能。</span><span class="sxs-lookup"><span data-stu-id="1cb94-123">Even more importantly, using an index buffer allows the adapter to store vertices in a vertex cache; if the primitive being drawn contains a recently-used vertex, that vertex can be fetched from the cache instead of reading it from the vertex buffer, which results in a big performance increase.</span></span>

<span data-ttu-id="1cb94-124">索引緩衝區在頂點緩衝區中的索引，因此每個唯一頂點都只需要在頂點緩衝區中儲存一次。</span><span class="sxs-lookup"><span data-stu-id="1cb94-124">An index buffer 'indexes' into the vertex buffer so each unique vertex needs to be stored only once in the vertex buffer.</span></span> <span data-ttu-id="1cb94-125">下圖顯示先前繪圖案例的索引方法。</span><span class="sxs-lookup"><span data-stu-id="1cb94-125">The following diagram shows an indexed approach to the earlier drawing scenario.</span></span>

![先前頂點緩衝區的索引緩衝區圖表](images/dip-fig3.png)

<span data-ttu-id="1cb94-127">索引緩衝區會儲存 VB 索引值，而這些值會參考頂點緩衝區內的特定頂點。</span><span class="sxs-lookup"><span data-stu-id="1cb94-127">The index buffer stores VB Index values, which reference a particular vertex within the vertex buffer.</span></span> <span data-ttu-id="1cb94-128">頂點緩衝區可以視為頂點的陣列，因此 VB 索引只是目標頂點之頂點緩衝區中的索引。</span><span class="sxs-lookup"><span data-stu-id="1cb94-128">A vertex buffer can be thought of as an array of vertices, so the VB Index is simply the index into the vertex buffer for the target vertex.</span></span> <span data-ttu-id="1cb94-129">同樣地，IB 索引是索引緩衝區中的索引。</span><span class="sxs-lookup"><span data-stu-id="1cb94-129">Similarly, an IB Index is an index into the index buffer.</span></span> <span data-ttu-id="1cb94-130">如果您不小心，這可能會非常混淆，因此請確定您已清楚使用的詞彙：在頂點緩衝區中使用 VB 索引值索引、將 IB 索引值索引放入索引緩衝區，以及索引緩衝區本身儲存 VB 索引值。</span><span class="sxs-lookup"><span data-stu-id="1cb94-130">This can get very confusing very quickly if you're not careful, so make sure you're clear on the vocabulary being used: VB Index values index into the vertex buffer, IB Index values index into the index buffer, and the index buffer itself stores VB Index values.</span></span>

<span data-ttu-id="1cb94-131">繪圖呼叫如下所示。</span><span class="sxs-lookup"><span data-stu-id="1cb94-131">The drawing call is shown below.</span></span> <span data-ttu-id="1cb94-132">在下一個繪製案例中，所有引數的意義都會以最長的時間進行討論;現在，請注意，此呼叫會再次指示 Direct3D 轉譯包含兩個三角形的三角形清單（從索引緩衝區中的位置0開始）。</span><span class="sxs-lookup"><span data-stu-id="1cb94-132">The meanings of all the arguments are discussed at length for the next drawing scenario; for now, just note that this call is again instructing Direct3D to render a triangle list containing two triangles, starting at location 0 within the index buffer.</span></span> <span data-ttu-id="1cb94-133">此呼叫會以與之前完全相同的順序繪製相同的兩個三角形，以確保適當的順時針方向：</span><span class="sxs-lookup"><span data-stu-id="1cb94-133">This call will draw the same two triangles in the exact same order as before, ensuring a proper clockwise orientation:</span></span>


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    0,                  // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    0,                  // StartIndex
                    2 );                // PrimitiveCount
```



## <a name="scenario-3-drawing-one-triangle-with-indexing"></a><span data-ttu-id="1cb94-134">案例3：使用索引繪製一個三角形</span><span class="sxs-lookup"><span data-stu-id="1cb94-134">Scenario 3: Drawing One Triangle with Indexing</span></span>

<span data-ttu-id="1cb94-135">假設您現在只想要繪製第二個三角形，但是您想要使用繪製整個四個時所使用的相同頂點緩衝區和索引緩衝區，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="1cb94-135">Pretend now that you want to draw only the second triangle, but you want to use the same vertex buffer and index buffer that are used when drawing the entire quad, as shown in the following diagram.</span></span>

![第二個三角形的索引緩衝區和頂點緩衝區圖表](images/dip-fig4.png)

<span data-ttu-id="1cb94-137">針對此繪製呼叫，第一個使用的 IB 索引為 3;此值稱為 StartIndex。</span><span class="sxs-lookup"><span data-stu-id="1cb94-137">For this drawing call, the first IB Index used is 3; this value is called the StartIndex.</span></span> <span data-ttu-id="1cb94-138">使用的最低 VB 索引為 0;此值稱為 MinIndex。</span><span class="sxs-lookup"><span data-stu-id="1cb94-138">The lowest VB Index used is 0; this value is called the MinIndex.</span></span> <span data-ttu-id="1cb94-139">雖然繪製三角形只需要三個頂點，但這三個頂點會散佈到頂點緩衝區中的四個相鄰位置;繪製呼叫所需的相鄰頂點緩衝區記憶體區塊中的位置數目稱為 NumVertices，在此呼叫中將設定為4。</span><span class="sxs-lookup"><span data-stu-id="1cb94-139">Even though only three vertices are required to draw the triangle, those three vertices are spread across four adjacent locations in the vertex buffer; the number of locations within the contiguous block of vertex buffer memory required for the drawing call is called NumVertices, and will be set to 4 in this call.</span></span> <span data-ttu-id="1cb94-140">MinIndex 和 NumVertices 值其實只是協助 Direct3D 在軟體頂點處理期間優化記憶體存取的提示，而且可以直接設定為包含整個頂點緩衝區（以效能的價格為限）。</span><span class="sxs-lookup"><span data-stu-id="1cb94-140">The MinIndex and NumVertices values are really just hints to help Direct3D optimize memory access during software vertex processing, and could simply be set to include the entire vertex buffer at the price of performance.</span></span>

<span data-ttu-id="1cb94-141">以下是單一三角形案例的繪圖呼叫;接下來會說明 BaseVertexIndex 引數的意義：</span><span class="sxs-lookup"><span data-stu-id="1cb94-141">Here is the drawing call for the single triangle case; the meaning of the BaseVertexIndex argument will be explained next:</span></span>


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    0,                  // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    3,                  // StartIndex
                    1 );                // PrimitiveCount
```



## <a name="scenario-4-drawing-one-triangle-with-offset-indexing"></a><span data-ttu-id="1cb94-142">案例4：使用位移索引繪製一個三角形</span><span class="sxs-lookup"><span data-stu-id="1cb94-142">Scenario 4: Drawing One Triangle with Offset Indexing</span></span>

<span data-ttu-id="1cb94-143">BaseVertexIndex 是一個值，可有效地新增至儲存在索引緩衝區中的每個 VB 索引。</span><span class="sxs-lookup"><span data-stu-id="1cb94-143">BaseVertexIndex is a value that's effectively added to every VB Index stored in the index buffer.</span></span> <span data-ttu-id="1cb94-144">例如，如果我們在上一個呼叫期間為 BaseVertexIndex 傳遞的值為50，則在 DrawIndexedPrimitive 呼叫的持續時間內，其功能與使用下圖中的索引緩衝區相同：</span><span class="sxs-lookup"><span data-stu-id="1cb94-144">For example, if we had passed in a value of 50 for BaseVertexIndex during the previous call, that would functionally be the same as using the index buffer in the following diagram for the duration of the DrawIndexedPrimitive call:</span></span>

![索引緩衝區的圖表，其值為50表示 basevertexindex](images/dip-fig5.png)

<span data-ttu-id="1cb94-146">此值很少會設定為0以外的任何值，但如果您想要將索引緩衝區與頂點緩衝區分離，則會很有用：如果在特定網格中填入索引緩衝區時，在頂點緩衝區內找不到網格的位置，您可以直接假裝網格頂點位於頂點緩衝區的開頭;當您需要進行繪製呼叫時，只要將實際的開始位置當作 BaseVertexIndex 傳遞。</span><span class="sxs-lookup"><span data-stu-id="1cb94-146">This value is rarely set to anything other than 0, but can be useful if you want to decouple the index buffer from the vertex buffer: If when filling in the index buffer for a particular mesh the location of the mesh within the vertex buffer isn't yet known, you can simply pretend the mesh vertices will be located at the start of the vertex buffer; when it comes time to make the draw call, simply pass the actual starting location as the BaseVertexIndex.</span></span>

<span data-ttu-id="1cb94-147">這項技術也可以在使用單一索引緩衝區繪製多個網格實例時使用;例如，如果頂點緩衝區包含兩個具有相同繪製順序但不同頂點 (可能有不同的擴散色彩或紋理座標) 的網格，則可以使用不同的 BaseVertexIndex 值來繪製這兩個格線。</span><span class="sxs-lookup"><span data-stu-id="1cb94-147">This technique can also be used when drawing multiple instances of a mesh using a single index buffer; for example, if the vertex buffer contained two meshes with identical draw order but slightly different vertices (perhaps different diffuse colors or texture coordinates), both meshes could be drawn by using different values for BaseVertexIndex.</span></span> <span data-ttu-id="1cb94-148">進一步瞭解這個概念，您可以使用一個索引緩衝區來繪製網格的多個實例，每個實例都包含在不同的頂點緩衝區中，只要迴圈的是作用中的頂點緩衝區，然後視需要調整 BaseVertexIndex。</span><span class="sxs-lookup"><span data-stu-id="1cb94-148">Taking this concept one step further, you could use one index buffer to draw multiple instances of a mesh, each contained in a different vertex buffer, simply by cycling which vertex buffer is active and adjusting the BaseVertexIndex as needed.</span></span> <span data-ttu-id="1cb94-149">請注意，BaseVertexIndex 值也會自動加入至 MinIndex 引數，這在您看到其使用方式時很合理：</span><span class="sxs-lookup"><span data-stu-id="1cb94-149">Note that the BaseVertexIndex value is also automatically added to the MinIndex argument, which makes sense when you see how it's used:</span></span>

<span data-ttu-id="1cb94-150">假設我們現在再次想要使用與之前相同的索引緩衝區來繪製四個四個三角形;不過，在使用不同的頂點緩衝區時，四位在 VB 索引50。</span><span class="sxs-lookup"><span data-stu-id="1cb94-150">Pretend now that we again want to draw only the second triangle of the quad using the same index buffer as before; however, a different vertex buffer is being used in which the quad is located at VB Index 50.</span></span> <span data-ttu-id="1cb94-151">四個頂點的相對順序保持不變，只有頂點緩衝區內的起始位置不同。</span><span class="sxs-lookup"><span data-stu-id="1cb94-151">The relative order of the quad vertices remains unchanged, only the starting location within the vertex buffer is different.</span></span> <span data-ttu-id="1cb94-152">索引緩衝區和頂點緩衝區看起來如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="1cb94-152">The index buffer and vertex buffer would look like the following diagram.</span></span>

![具有 vb 索引50的索引緩衝區和頂點緩衝區圖表](images/dip-fig6.png)

<span data-ttu-id="1cb94-154">以下是適當的繪製呼叫;請注意，BaseVertexIndex 是從上一個案例中變更的唯一值：</span><span class="sxs-lookup"><span data-stu-id="1cb94-154">Here is the appropriate draw call; note that BaseVertexIndex is the only value which has changed from the previous scenario:</span></span>


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    50,                 // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    3,                  // StartIndex
                    1 );                // PrimitiveCount
```



## <a name="related-topics"></a><span data-ttu-id="1cb94-155">相關主題</span><span class="sxs-lookup"><span data-stu-id="1cb94-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1cb94-156">呈現基本專案</span><span class="sxs-lookup"><span data-stu-id="1cb94-156">Rendering Primitives</span></span>](rendering-primitives.md)
</dt> </dl>

 

 

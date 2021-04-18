---
description: Direct3D 管線使用的所有資源都衍生自兩個基本資源類型︰緩衝區和紋理。 緩衝區是原始資料 (元素) 的集合，紋理是紋素 (紋理元素) 的集合。
ms.assetid: c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69
title: " (Direct3D 10) 的資源類型"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ec6ec9b57a2e504c137d424b19c61f2353d685e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104566375"
---
# <a name="resource-types-direct3d-10"></a><span data-ttu-id="5dbb5-104"> (Direct3D 10) 的資源類型</span><span class="sxs-lookup"><span data-stu-id="5dbb5-104">Resource Types (Direct3D 10)</span></span>

<span data-ttu-id="5dbb5-105">Direct3D 管線使用的所有資源都衍生自兩個基本資源類型︰[緩衝區](#buffer-resources)和[紋理](#texture-resources)。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-105">All resources used by the Direct3D pipeline derive from two basic resource types: [buffers](#buffer-resources) and [textures](#texture-resources).</span></span> <span data-ttu-id="5dbb5-106">緩衝區是原始資料 (元素) 的集合，紋理是紋素 (紋理元素) 的集合。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-106">A buffer is a collection of raw data (elements); a texture is a collection of texels (texture elements).</span></span>

-   [<span data-ttu-id="5dbb5-107">緩衝區資源</span><span class="sxs-lookup"><span data-stu-id="5dbb5-107">Buffer Resources</span></span>](#buffer-resources)
    -   [<span data-ttu-id="5dbb5-108">緩衝區類型</span><span class="sxs-lookup"><span data-stu-id="5dbb5-108">Buffer Types</span></span>](#buffer-types)
-   [<span data-ttu-id="5dbb5-109">材質資源</span><span class="sxs-lookup"><span data-stu-id="5dbb5-109">Texture Resources</span></span>](#texture-resources)
    -   [<span data-ttu-id="5dbb5-110">材質類型</span><span class="sxs-lookup"><span data-stu-id="5dbb5-110">Texture Types</span></span>](#texture-types)
    -   [<span data-ttu-id="5dbb5-111">子資源</span><span class="sxs-lookup"><span data-stu-id="5dbb5-111">Subresources</span></span>](#subresources)
    -   [<span data-ttu-id="5dbb5-112">強式與弱式類型</span><span class="sxs-lookup"><span data-stu-id="5dbb5-112">Strong vs. Weak Typing</span></span>](#strong-vs-weak-typing)
-   [<span data-ttu-id="5dbb5-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="5dbb5-113">Related topics</span></span>](#related-topics)

<span data-ttu-id="5dbb5-114">有兩種方式可以完整指定資源的配置 (或記憶體使用量)︰</span><span class="sxs-lookup"><span data-stu-id="5dbb5-114">There are two ways to fully specify the layout (or memory footprint) of a resource:</span></span>



| <span data-ttu-id="5dbb5-115">項目</span><span class="sxs-lookup"><span data-stu-id="5dbb5-115">Item</span></span>                                                                                                 | <span data-ttu-id="5dbb5-116">描述</span><span class="sxs-lookup"><span data-stu-id="5dbb5-116">Description</span></span>                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="5dbb5-117"><span id="Typed"></span><span id="typed"></span><span id="TYPED"></span>類型</span><span class="sxs-lookup"><span data-stu-id="5dbb5-117"><span id="Typed"></span><span id="typed"></span><span id="TYPED"></span>Typed</span></span><br/>             | <span data-ttu-id="5dbb5-118">建立資源時完整指定類型。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-118">Fully specify the type when the resource is created.</span></span><br/>               |
| <span data-ttu-id="5dbb5-119"><span id="Typeless"></span><span id="typeless"></span><span id="TYPELESS"></span>無</span><span class="sxs-lookup"><span data-stu-id="5dbb5-119"><span id="Typeless"></span><span id="typeless"></span><span id="TYPELESS"></span>Typeless</span></span><br/> | <span data-ttu-id="5dbb5-120">資源繫結到管線時完整指定類型。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-120">Fully specify the type when the resource is bound to the pipeline.</span></span><br/> |



 

## <a name="buffer-resources"></a><span data-ttu-id="5dbb5-121">緩衝區資源</span><span class="sxs-lookup"><span data-stu-id="5dbb5-121">Buffer Resources</span></span>

<span data-ttu-id="5dbb5-122">緩衝資源是完整具類型的資料的集合，緩衝區則包含元素。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-122">A buffer resource is a collection of fully typed data; internally, a buffer contains elements.</span></span> <span data-ttu-id="5dbb5-123">一個元素由 1 到 4 個元件組成。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-123">An element is made up of 1 to 4 components.</span></span> <span data-ttu-id="5dbb5-124">元素資料類型的範例包括︰封裝資料值 (例如 R8G8B8A8)、單一的 8 位元整數、四個 32 位元浮點值。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-124">Examples of element data types include: a packed data value (like R8G8B8A8), a single 8-bit integer, four 32-bit float values.</span></span> <span data-ttu-id="5dbb5-125">這些資料類型是用來儲存資料，例如位置向量、一般向量、頂點緩衝區中的紋理座標、索引緩衝區中的索引，或者裝置狀態。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-125">These data types are used to store data, such as a position vector, a normal vector, a texture coordinate in a vertex buffer, an index in an index buffer, or device state.</span></span>

<span data-ttu-id="5dbb5-126">建立緩衝區做為未結構化的資源。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-126">A buffer is created as an unstructured resource.</span></span> <span data-ttu-id="5dbb5-127">因為未建構，所以緩衝區無法包含任何 Mipmap 層次，在讀取時不會篩選，而且無法多重取樣。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-127">Because it is unstructured, a buffer cannot contain any mipmap levels, is not filtered when read, and cannot be multisampled.</span></span>

### <a name="buffer-types"></a><span data-ttu-id="5dbb5-128">緩衝區類型</span><span class="sxs-lookup"><span data-stu-id="5dbb5-128">Buffer Types</span></span>

-   [<span data-ttu-id="5dbb5-129">頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="5dbb5-129">Vertex Buffer</span></span>](#vertex-buffer)
-   [<span data-ttu-id="5dbb5-130">索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="5dbb5-130">Index Buffer</span></span>](#index-buffer)
-   [<span data-ttu-id="5dbb5-131">常數緩衝區</span><span class="sxs-lookup"><span data-stu-id="5dbb5-131">Constant Buffer</span></span>](#constant-buffer)

### <a name="vertex-buffer"></a><span data-ttu-id="5dbb5-132">頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="5dbb5-132">Vertex Buffer</span></span>

<span data-ttu-id="5dbb5-133">緩衝區是元素的集合；頂點緩衝區包含每個頂點資料。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-133">A buffer is a collection of elements; a vertex buffer contains per-vertex data.</span></span> <span data-ttu-id="5dbb5-134">最簡單的範例是包含一種類型資料的頂點緩衝區，例如位置資料。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-134">The simplest example is a vertex buffer that contains one type of data, such as position data.</span></span> <span data-ttu-id="5dbb5-135">它可以像下圖一樣視覺化。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-135">It can be visualized like the following illustration.</span></span>

![包含位置資料的頂點緩衝區圖例](images/d3d10-resources-single-element-vb2.png)

<span data-ttu-id="5dbb5-137">頂點緩衝區經常包含可完整指定 3D 頂點所需的所有資料。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-137">More often, a vertex buffer contains all the data needed to fully specify 3D vertices.</span></span> <span data-ttu-id="5dbb5-138">例如，可能會包含每個頂點位置、一般及紋理座標的頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-138">An example of this could be a vertex buffer that contains per-vertex position, normal and texture coordinates.</span></span> <span data-ttu-id="5dbb5-139">此資料通常組織成每個頂點元素集，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-139">This data is usually organized as sets of per-vertex elements, as shown in the following illustration.</span></span>

![頂點緩區的圖例，其包含位置、一般和紋理資料](images/d3d10-vertex-buffer-element.png)

<span data-ttu-id="5dbb5-141">這個頂點緩衝區包含八個頂點的每個頂點資料；每個頂點儲存三個元素 (位置、一般和紋理座標)。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-141">This vertex buffer contains per-vertex data for eight vertices; each vertex stores three elements (position, normal, and texture coordinates).</span></span> <span data-ttu-id="5dbb5-142">位置和一般都是使用 3 32 位浮點數 (DXGI \_ 格式 \_ R32G32B32 \_ FLOAT) 和材質座標（使用 2 32 位浮點數 (\_ \_ float 格式 R32G32 \_ FLOAT) ）來指定。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-142">The position and normal are each typically specified using three 32-bit floats (DXGI\_FORMAT\_R32G32B32\_FLOAT) and the texture coordinates using two 32-bit floats (DXGI\_FORMAT\_R32G32\_FLOAT).</span></span>

<span data-ttu-id="5dbb5-143">若要存取頂點緩衝區的資料，您必須知道要存取哪個頂點以及這些其他緩衝區參數︰</span><span class="sxs-lookup"><span data-stu-id="5dbb5-143">To access data from a vertex buffer, you need to know which vertex to access and these other buffer parameters:</span></span>

-   <span data-ttu-id="5dbb5-144">位移 - 從緩衝區的起始到第一個頂點資料的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-144">Offset - the number of bytes from the start of the buffer to the data for the first vertex.</span></span> <span data-ttu-id="5dbb5-145">提供給 [**IASetVertexBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetvertexbuffers)的位移。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-145">The offset is supplied to [**IASetVertexBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetvertexbuffers).</span></span>
-   <span data-ttu-id="5dbb5-146">BaseVertexLocation-相對於適當繪製呼叫所使用之第一個頂點之位移的位元組數目 (參閱 [繪製方法](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)) 。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-146">BaseVertexLocation - the number of bytes from the offset to the first vertex used by the appropriate draw call (see [Draw Methods](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)).</span></span>

<span data-ttu-id="5dbb5-147">建立頂點緩衝區之前，您必須建立 [**輸入設定物件**](/windows/win32/api/d3d10/nn-d3d10-id3d10inputlayout)來定義其配置;這是藉由呼叫 [**CreateInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout)來完成。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-147">Before you create a vertex buffer, you need to define its layout by creating an [**input-layout object**](/windows/win32/api/d3d10/nn-d3d10-id3d10inputlayout); this is done by calling [**CreateInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).</span></span> <span data-ttu-id="5dbb5-148">一旦建立了輸入設定物件，請呼叫 [**IASetInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetinputlayout)，將它系結至輸入組合語言階段。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-148">Once the input-layout object is created, bind it to the input-assembler stage by calling [**IASetInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetinputlayout).</span></span>

<span data-ttu-id="5dbb5-149">若要建立頂點緩衝區，請呼叫 [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer)。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-149">To create a vertex buffer, call [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer).</span></span>

### <a name="index-buffer"></a><span data-ttu-id="5dbb5-150">索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="5dbb5-150">Index Buffer</span></span>

<span data-ttu-id="5dbb5-151">索引緩衝區包含連續的 16 位元或 32 位元索引集，而每個索引用來識別頂點緩衝區中的頂點。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-151">An index buffer contains a sequential set of 16-bit or 32-bit indices; each index is used to identify a vertex in a vertex buffer.</span></span> <span data-ttu-id="5dbb5-152">使用具有一個或多個頂點緩衝區的索引緩衝區，來提供資料給 IA 階段即稱為編製索引。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-152">Using an index buffer with one or more vertex buffers to supply data to the IA stage is called indexing.</span></span> <span data-ttu-id="5dbb5-153">索引緩衝區可以視覺化，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-153">An index buffer can be visualized like the following illustration.</span></span>

![索引緩衝區的圖例](images/d3d10-index-buffer.png)

<span data-ttu-id="5dbb5-155">儲存在索引緩衝區中的循序索引，使用以下參數尋找︰</span><span class="sxs-lookup"><span data-stu-id="5dbb5-155">The sequential indices stored in an index buffer are located with the following parameters:</span></span>

-   <span data-ttu-id="5dbb5-156">位移 - 從緩衝區的起始到第一個索引的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-156">Offset - the number of bytes from the start of the buffer to the first index.</span></span> <span data-ttu-id="5dbb5-157">提供給 [**IASetIndexBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetindexbuffer)的位移。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-157">The offset is supplied to [**IASetIndexBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetindexbuffer).</span></span>
-   <span data-ttu-id="5dbb5-158">StartIndexLocation-相對於適當繪製呼叫所使用之第一個頂點之位移的位元組數目 (參閱 [繪製方法](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)) 。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-158">StartIndexLocation - the number of bytes from the offset to the first vertex used by the appropriate draw call (see [Draw Methods](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)).</span></span>
-   <span data-ttu-id="5dbb5-159">IndexCount - 要呈現的索引數目。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-159">IndexCount - the number of indices to render.</span></span>

<span data-ttu-id="5dbb5-160">若要建立索引緩衝區，請呼叫 [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer)。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-160">To create an index buffer, call [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer).</span></span>

<span data-ttu-id="5dbb5-161">索引緩衝區可以將多行或三角形的分隔線，藉由分隔每個 [線條或三角形](../direct3d11/d3d10-graphics-programming-guide-primitive-topologies.md) 的分隔線來將它們拼接在一起。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-161">An index buffer can stitch together multiple [line or triangle strips](../direct3d11/d3d10-graphics-programming-guide-primitive-topologies.md) by separating each with a strip-cut index.</span></span> <span data-ttu-id="5dbb5-162">區域切割索引允許使用單一繪製呼叫來繪製多行或三角形連環。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-162">A strip-cut index allows multiple line or triangle strips to be drawn with a single draw call.</span></span> <span data-ttu-id="5dbb5-163">區域剪下索引只是索引的最大可能值 (0xffff 的16位索引，0xffffffff 用於32位的索引) 。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-163">A strip-cut index is simply the maximum possible value for the index (0xffff for a 16-bit index, 0xffffffff for a 32-bit index).</span></span> <span data-ttu-id="5dbb5-164">區域切割索引會重設已編制索引的基本類型的捲繞順序，並且可以用來消除對於變質三角形的需求，否則可能需要先維護適當的三角形連環的捲繞順序。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-164">The strip-cut index resets the winding order in indexed primitives and can be used to remove the need for degenerate triangles that may otherwise be required to maintain proper winding order in a triangle strip.</span></span> <span data-ttu-id="5dbb5-165">下列圖例顯示區域切割索引的範例。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-165">The following illustration shows an example of a strip-cut index.</span></span>

![區域切割索引的圖例](images/d3d10-ia-strips-cut-value.png)

### <a name="constant-buffer"></a><span data-ttu-id="5dbb5-167">常數緩衝區</span><span class="sxs-lookup"><span data-stu-id="5dbb5-167">Constant Buffer</span></span>

<span data-ttu-id="5dbb5-168">Direct3D 10 引進了新的緩衝區，以提供稱為著色器常數緩衝區或單純常數緩衝區的著色器常數。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-168">Direct3D 10 introduced a new buffer for supplying shader constants called a shader-constant buffer or simply a constant buffer.</span></span> <span data-ttu-id="5dbb5-169">就概念而言，它看起來就像單一元素的頂點緩衝區，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-169">Conceptually, it looks just like a single-element vertex buffer, as shown in the following illustration.</span></span>

![著色器常數緩衝區的圖例](images/d3d10-shader-resource-buffer.png)

<span data-ttu-id="5dbb5-171">每個元素會儲存 1 到 4 個元件常數，取決於儲存的資料格式。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-171">Each element stores a 1-to-4 component constant, determined by the format of the data stored.</span></span>

<span data-ttu-id="5dbb5-172">常數緩衝區透過允許著色器常數群組在一起並且同時認可，而不是進行個別呼叫以分別認可每一個常數，來減少更新著色器常數所需的頻寬。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-172">Constant buffers reduce the bandwidth required to update shader constants by allowing shader constants to be grouped together and committed at the same time rather than making individual calls to commit each constant separately.</span></span>

<span data-ttu-id="5dbb5-173">若要建立著色器常數緩衝區，請呼叫 [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer) 並指定常數緩衝區系結旗標 D3D10 系結 \_ \_ 常數 \_ 緩衝區 (參閱 D3D10 系結 [**\_ \_ 旗**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag) 標) 。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-173">To create a shader-constant buffer, call [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer) and specify the constant-buffer bind flag D3D10\_BIND\_CONSTANT\_BUFFER (see [**D3D10\_BIND\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag)).</span></span>

<span data-ttu-id="5dbb5-174">若要將著色器常數緩衝區系結至管線，請呼叫下列其中一種方法： [**GSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetconstantbuffers)、 [**PSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetconstantbuffers)或 [**VSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetconstantbuffers)。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-174">To bind a shader-constant buffer to the pipeline, call one of these methods: [**GSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetconstantbuffers), [**PSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetconstantbuffers), or [**VSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetconstantbuffers).</span></span>

<span data-ttu-id="5dbb5-175">請注意，使用 [**ID3D10Effect 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect) 介面時， **ID3D10Effect 介面** 實例會處理建立、系結和 comitting 常數緩衝區的進程。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-175">Note that when using the [**ID3D10Effect Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect) interface the process of creating, binding and comitting a constant buffer is handled by the **ID3D10Effect Interface** instance.</span></span> <span data-ttu-id="5dbb5-176">在這種情況下，只會 nescesary 使用其中一個 GetVariable 方法（例如 [**GetVariableByName**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-getvariablebyname) ）來從效果中取得變數，並使用其中一個 SetVariable 方法（例如 [**SetMatrix**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectmatrixvariable-setmatrix)）來更新變數。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-176">In that case it is only nescesary to get the variable from the effect with one of the GetVariable methods such as [**GetVariableByName**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-getvariablebyname) and update the variable with one of the SetVariable methods such as [**SetMatrix**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectmatrixvariable-setmatrix).</span></span> <span data-ttu-id="5dbb5-177">如需使用 **ID3D10Effect 介面** 管理常數緩衝區的範例，請參閱 [教學課程 07](https://msdn.microsoft.com/library/Ee416442(v=VS.85).aspx)。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-177">For an example of using **ID3D10Effect Interface** to manage a constant buffer see [tutorial 07](https://msdn.microsoft.com/library/Ee416442(v=VS.85).aspx).</span></span>

<span data-ttu-id="5dbb5-178">著色器會繼續以不是常數緩衝區一部分的變數的相同方式，按照變數名稱直接讀取常數緩衝區中的變數。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-178">A shader continues to read variables in a constant buffer directly by variable name in the same manner variables that are not part of a constant buffer are read.</span></span>

<span data-ttu-id="5dbb5-179">每個著色器階段允許最多 15 個著色器常數緩衝區，而每個緩衝區可保留最多 4096 個常數。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-179">Each shader stage allows up to 15 shader-constant buffers; each buffer can hold up to 4096 constants.</span></span>

<span data-ttu-id="5dbb5-180">使用常數緩衝區來儲存資料流輸出階段的結果。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-180">Use a constant buffer to store the results of the stream-output stage.</span></span>

<span data-ttu-id="5dbb5-181">如需在著色器中宣告常數緩衝區的範例，請參閱[著色器常數 (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-181">See [Shader Constants (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-constants.md) for an example of declaring a constant buffer in a shader.</span></span>

## <a name="texture-resources"></a><span data-ttu-id="5dbb5-182">材質資源</span><span class="sxs-lookup"><span data-stu-id="5dbb5-182">Texture Resources</span></span>

<span data-ttu-id="5dbb5-183">紋理資源是設計來儲存紋素的結構化資料集合。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-183">A texture resource is a structured collection of data designed to store texels.</span></span> <span data-ttu-id="5dbb5-184">和緩衝區不同的是，紋理可依紋理樣本篩選，由著色器單位讀取。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-184">Unlike buffers, textures can be filtered by texture samplers as they are read by shader units.</span></span> <span data-ttu-id="5dbb5-185">紋理類型會影響篩選紋理的方式。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-185">The type of texture impacts how the texture is filtered.</span></span> <span data-ttu-id="5dbb5-186">紋素代表管線可讀取或寫入的最小紋理單位。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-186">A texel represents the smallest unit of a texture that can be read or written to by the pipeline.</span></span> <span data-ttu-id="5dbb5-187">每個材質都包含1至4個元件，以其中一個 DXGI 格式排列 (請參閱 [**dxgi \_ 格式**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)) 。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-187">Each texel contains 1 to 4 components, arranged in one of the DXGI formats (see [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span></span>

<span data-ttu-id="5dbb5-188">紋裡會建立結構化資源，以便得知其大小。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-188">Textures are created as a structured resource so that their size is known.</span></span> <span data-ttu-id="5dbb5-189">不過，只要在材質系結至管線時使用 view 完全指定型別，就可以在資源建立時間輸入每個材質或輸入較少的材質。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-189">However, each texture may be typed or type less at resource-creation time, as long as the type is fully specified using a view when the texture is bound to the pipeline.</span></span>

-   [<span data-ttu-id="5dbb5-190">材質類型</span><span class="sxs-lookup"><span data-stu-id="5dbb5-190">Texture Types</span></span>](#texture-types)
-   [<span data-ttu-id="5dbb5-191">子資源</span><span class="sxs-lookup"><span data-stu-id="5dbb5-191">Subresources</span></span>](#subresources)
-   [<span data-ttu-id="5dbb5-192">強式與弱式類型</span><span class="sxs-lookup"><span data-stu-id="5dbb5-192">Strong vs. Weak Typing</span></span>](#strong-vs-weak-typing)

### <a name="texture-types"></a><span data-ttu-id="5dbb5-193">材質類型</span><span class="sxs-lookup"><span data-stu-id="5dbb5-193">Texture Types</span></span>

<span data-ttu-id="5dbb5-194">有數種紋理類型︰1D、2D、3D，每一個都可使用或不使用 Mipmap 建立。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-194">There are several types of textures: 1D, 2D, 3D, each of which can be created with or without mipmaps.</span></span> <span data-ttu-id="5dbb5-195">Direct3D 10 也支援材質陣列和多重取樣材質。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-195">Direct3D 10 also supports texture arrays and multisampled textures.</span></span>

-   [<span data-ttu-id="5dbb5-196">1D 材質</span><span class="sxs-lookup"><span data-stu-id="5dbb5-196">1D Texture</span></span>](#1d-texture)
-   [<span data-ttu-id="5dbb5-197">1D 材質陣列</span><span class="sxs-lookup"><span data-stu-id="5dbb5-197">1D Texture Array</span></span>](#1d-texture-array)
-   [<span data-ttu-id="5dbb5-198">2D 材質和2D 材質陣列</span><span class="sxs-lookup"><span data-stu-id="5dbb5-198">2D Texture and 2D Texture Array</span></span>](#2d-texture-and-2d-texture-array)
-   [<span data-ttu-id="5dbb5-199">3D 材質</span><span class="sxs-lookup"><span data-stu-id="5dbb5-199">3D Texture</span></span>](#3d-texture)

### <a name="1d-texture"></a><span data-ttu-id="5dbb5-200">1D 紋理</span><span class="sxs-lookup"><span data-stu-id="5dbb5-200">1D Texture</span></span>

<span data-ttu-id="5dbb5-201">最簡單形式的 1D 紋理所包含的紋理資料，可以使用單一紋理座標處理，它可以視覺化為紋素陣列，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-201">A 1D texture in its simplest form contains texture data that can be addressed with a single texture coordinate; it can be visualized as an array of texels, as shown in the following illustration.</span></span>

![1D 紋理的圖例](images/d3d10-1d-texture.png)

<span data-ttu-id="5dbb5-203">每個紋素根據所儲存的資料格式包含許多色彩元件。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-203">Each texel contains a number of color components depending on the format of the data stored.</span></span> <span data-ttu-id="5dbb5-204">增加更多複雜度，您可以使用 Mipmap 層次建立 1D 紋理，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-204">Adding more complexity, you can create a 1D texture with mipmap levels, as shown in the following illustration.</span></span>

![具有 Mipmap 層次之 1D 紋理的圖例](images/d3d10-resource-texture1d.png)

<span data-ttu-id="5dbb5-206">Mipmap 層次是比上層小二的 n 次方的紋理。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-206">A mipmap level is a texture that is a power-of-two smaller than the level above it.</span></span> <span data-ttu-id="5dbb5-207">最上層包含大部分的詳細資料，每個後續層級較小；若是 1D 的 Mipmap，最小層級包含一個紋素。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-207">The top-most level contains the most detail, each subsequent level is smaller; for a 1D mipmap, the smallest level contains one texel.</span></span> <span data-ttu-id="5dbb5-208">不同層級是以稱為 LOD (詳細層級) 的索引來識別；您可以在呈現不是那麼靠近相機的幾何圖形時，使用 LOD 存取較小的紋理。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-208">The differing levels are identified by an index called a LOD (level-of-detail); you can use the LOD to access a smaller texture when rendering geometry that is not as close to the camera.</span></span>

### <a name="1d-texture-array"></a><span data-ttu-id="5dbb5-209">1D 材質陣列</span><span class="sxs-lookup"><span data-stu-id="5dbb5-209">1D Texture Array</span></span>

<span data-ttu-id="5dbb5-210">Direct3D 10 對於紋理陣列也有新的資料結構。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-210">Direct3D 10 also has a new data structure for an array of textures.</span></span> <span data-ttu-id="5dbb5-211">1D 紋理陣列概念上看起來像下圖。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-211">An array of 1D textures looks conceptually like the following illustration.</span></span>

![1d 紋理陣列的圖例](images/d3d10-resource-texture1darray.png)

<span data-ttu-id="5dbb5-213">這個紋理陣列包含三種紋理。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-213">This texture array contains three textures.</span></span> <span data-ttu-id="5dbb5-214">三個紋理的每一個都具有紋理寬度 5 (也就是第一層的元素數目)。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-214">Each of the three textures has a texture width of 5 (which is the number of elements in the first layer).</span></span> <span data-ttu-id="5dbb5-215">每個紋理也包含 3 層 Mipmap。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-215">Each texture also contains a 3 layer mipmap.</span></span>

<span data-ttu-id="5dbb5-216">在 Direct3D 中的所有紋理陣列都是同質紋理陣列，這表示紋理陣列中的每種紋理必須有相同資料格式和大小 (包括紋理寬度和 Mipmap 層次數目)。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-216">All texture arrays in Direct3D are a homogeneous array of textures; this means that every texture in a texture array must have the same data format and size (including texture width and number of mipmap levels).</span></span> <span data-ttu-id="5dbb5-217">只要每一個紋理陣列中的所有紋理大小都相符，您可以建立不同大小的紋理陣列。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-217">You may create texture arrays of different sizes, as long as all the textures in each array match in size.</span></span>

### <a name="2d-texture-and-2d-texture-array"></a><span data-ttu-id="5dbb5-218">2D 紋理和 2D 紋理陣列</span><span class="sxs-lookup"><span data-stu-id="5dbb5-218">2D Texture and 2D Texture Array</span></span>

<span data-ttu-id="5dbb5-219">Texture2D 資源包含 2D 紋格。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-219">A Texture2D resource contains a 2D grid of texels.</span></span> <span data-ttu-id="5dbb5-220">每個紋素是由 u、v 向量定位。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-220">Each texel is addressable by a u, v vector.</span></span> <span data-ttu-id="5dbb5-221">因為是紋理資源，它可能包含 Mipmap 層次和子資源。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-221">Because it is a texture resource, it may contain mipmap levels, and subresources.</span></span> <span data-ttu-id="5dbb5-222">完全填充的 2D 紋理資源看起來如下圖。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-222">A fully populated 2D texture resource looks like the following illustration.</span></span>

![2D 紋理資源的圖例](images/d3d10-resource-texture2d.png)

<span data-ttu-id="5dbb5-224">這個紋理資源包含具三個 Mipmap 層次的單一 3x5 紋理。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-224">This texture resource contains a single 3x5 texture with three mipmap levels.</span></span>

<span data-ttu-id="5dbb5-225">Texture2DArray 資源是同質 2D 紋理陣列；也就是每個紋理都有相同的資料格式和維度 (包括 Mipmap 層次)。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-225">A Texture2DArray resource is a homogeneous array of 2D textures; that is, each texture has the same data format and dimensions (including mipmap levels).</span></span> <span data-ttu-id="5dbb5-226">它與 1D 紋理陣列具有類似的配置，除了紋理現在包含 2D 資料以外，因此其外觀如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-226">It has a similar layout as the 1D texture array except that the textures now contain 2D data, and therefore looks like the following illustration.</span></span>

![2D 紋理資源陣列的圖例](images/d3d10-resource-texture2darray.png)

<span data-ttu-id="5dbb5-228">這個紋理包含三個紋理，每個紋理為 3x5 含兩個 Mipmap 層次。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-228">This texture array contains three textures; each texture is 3x5 with two mipmap levels.</span></span>

### <a name="using-a-texture2darray-as-a-texture-cube"></a><span data-ttu-id="5dbb5-229">使用 Texture2DArray 做為紋理立方體</span><span class="sxs-lookup"><span data-stu-id="5dbb5-229">Using a Texture2DArray as a Texture Cube</span></span>

<span data-ttu-id="5dbb5-230">紋理立方體是包含 6 個紋理的 2D 紋理陣列，每個立方體表面一個紋理。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-230">A texture cube is a 2D texture array that contains 6 textures, one for each face of the cube.</span></span> <span data-ttu-id="5dbb5-231">完全填充的紋理立方體如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-231">A fully populated texture cube looks like the following illustration.</span></span>

![代表紋理立方體之 2D 紋理資源的圖例](images/d3d10-resource-texturecube.png)

<span data-ttu-id="5dbb5-233">包含 6 個紋理的 2D 紋理陣列，在使用立方體紋理視圖結合管線後，可使用立方體內建功能從著色器內讀取。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-233">A 2D texture array that contains 6 textures may be read from within shaders with the cube map intrinsic functions, after they are bound to the pipeline with a cube-texture view.</span></span> <span data-ttu-id="5dbb5-234">使用從紋理立方體中心指出的 3D 向量，從著色器處理紋理。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-234">Texture cubes are addressed from the shader with a 3D vector pointing out from the center of the texture cube.</span></span>

### <a name="3d-texture"></a><span data-ttu-id="5dbb5-235">3D 紋理</span><span class="sxs-lookup"><span data-stu-id="5dbb5-235">3D Texture</span></span>

<span data-ttu-id="5dbb5-236">Texture3D 資源 (也稱為容積紋理) 包含 3D 容積的紋素。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-236">A Texture3D resource (also known as a volume texture) contains a 3D volume of texels.</span></span> <span data-ttu-id="5dbb5-237">因為是紋理資源，所以可能包含 Mipmap 層次。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-237">Since it is a texture resource, it may contain mipmap levels.</span></span> <span data-ttu-id="5dbb5-238">完整填入的 [**3d 紋理**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture3d) 看起來如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-238">A fully populated [**3D texture**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture3d) looks like the following illustration.</span></span>

![3D 紋理資源的圖例](images/d3d10-resource-texture3d.png)

<span data-ttu-id="5dbb5-240">3D 紋理 Mipmap 切片繫結為描繪目標輸出 (描繪目標視圖) 時，3D 紋理行為等同於具 n 切片的 2D 紋理陣列。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-240">When a 3D texture mipmap slice is bound as a render target output (with a render-target view), the 3D texture behaves identically to a 2D texture array with n slices.</span></span> <span data-ttu-id="5dbb5-241">您可以透過將輸出資料的純量元件宣告為 SV RenderTargetArrayIndex 系統值，從 [幾何著色器] 階段選擇特定轉譯配量 \_ 。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-241">The particular render slice is chosen from the geometry-shader stage, by declaring a scalar component of output data as the SV\_RenderTargetArrayIndex system-value.</span></span>

<span data-ttu-id="5dbb5-242">沒有 3D 紋理陣列概念，因此 3D 紋理子資源是單一 Mipmap 層次。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-242">There is no concept of a 3D texture array; therefore a 3D texture subresource is a single mipmap level.</span></span>

### <a name="subresources"></a><span data-ttu-id="5dbb5-243">子資源</span><span class="sxs-lookup"><span data-stu-id="5dbb5-243">Subresources</span></span>

<span data-ttu-id="5dbb5-244">Direct3D 10 API 會參考整個資源或資源子集。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-244">The Direct3D 10 API references entire resources or subsets of resources.</span></span> <span data-ttu-id="5dbb5-245">為了指定部分資源，Direct3D 已創造字詞子資源，這表示資源的子集。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-245">To specify portion of resources, Direct3D has coined the term subresources which means a subset of a resource.</span></span>

<span data-ttu-id="5dbb5-246">緩衝區定義為單一的子資源。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-246">A buffer is defined as a single subresource.</span></span> <span data-ttu-id="5dbb5-247">紋理則稍微複雜，因為有數種不同紋理類型 (1D、2D 等)，其中部分支援 Mipmap 層次和/或紋理陣列。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-247">Textures are a little more complicated as there are several different texture types (1D, 2D, etc.) some of which support mipmap levels and/or texture arrays.</span></span> <span data-ttu-id="5dbb5-248">從最簡單的案例開始，1D 紋理定義為單一子資源，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-248">Beginning with the simplest case, a 1D texture is defined as a single subresource, as shown in the following illustration.</span></span>

![1D 紋理的圖例](images/d3d10-1d-texture.png)

<span data-ttu-id="5dbb5-250">這表示組成 1D 紋理的紋理陣列包含在單一子資源中。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-250">This means that the array of texels that make up a 1D texture are contained in a single subresource.</span></span>

<span data-ttu-id="5dbb5-251">如果展開含有三個 Mipmap 層次的 1D 紋理，它可以視覺化如下。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-251">If you expand a 1D texture with three mipmap levels, it can be visualized like this.</span></span>

![具有 Mipmap 層次之 1D 紋理的圖例](images/d3d10-resource-texture1d.png)

<span data-ttu-id="5dbb5-253">將此視為三個子紋理組成的單一紋理。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-253">Think of this as a single texture that is made up of three subtextures.</span></span> <span data-ttu-id="5dbb5-254">每個子紋理計算為一個子資源，所以這個 1D 紋理包含 3 個子資源。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-254">Each subtexture is counted as a subresource, so this 1D texture contains 3 subresources.</span></span> <span data-ttu-id="5dbb5-255">子紋理 (或子資源) 可以對單一紋理使用詳細層級 (LOD) 編制索引。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-255">A subtexture (or subresource) can be indexed using the level-of-detail (LOD) for a single texture.</span></span> <span data-ttu-id="5dbb5-256">使用紋理陣列時，存取特定子紋理需要 LOD 和特定紋理二者。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-256">When using an array of textures, accessing a particular subtexture requires both the LOD and the particular texture.</span></span> <span data-ttu-id="5dbb5-257">或者，API 結合這兩個資訊為單一以零起始的子資源索引，如此處所示。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-257">Alternately, the API combines these two pieces of information into a single zero-based subresource index as shown here.</span></span>

![以零起始的子資源索引的圖例](images/d3d10-resource-texture1darray-sub-indexing.png)

### <a name="selecting-subresources"></a><span data-ttu-id="5dbb5-259">選取子資源</span><span class="sxs-lookup"><span data-stu-id="5dbb5-259">Selecting Subresources</span></span>

<span data-ttu-id="5dbb5-260">某些 API 會存取整個資源 (例如 [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource)) ，其他人會存取一部分的資源 (例如 [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource) 或 [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion)) 。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-260">Some API's access an entire resource (for example [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource)), others access a portion of a resource (for example [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource) or [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion)).</span></span> <span data-ttu-id="5dbb5-261">存取部分資源的 API 通常會使用 view description (例如 [**D3D10 \_ TEX2D \_ ARRAY \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_dsv)) 來指定要存取的子資源。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-261">The API's that access a portion of a resource generally use a view description (such as [**D3D10\_TEX2D\_ARRAY\_DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_dsv)) to specify the subresources to access.</span></span>

<span data-ttu-id="5dbb5-262">這些圖闡述檢視描述在存取紋理陣列時使用的詞彙。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-262">These figures illustrate the terms used by a view description when accessing an array of textures.</span></span>

### <a name="array-slice"></a><span data-ttu-id="5dbb5-263">陣列切片</span><span class="sxs-lookup"><span data-stu-id="5dbb5-263">Array Slice</span></span>

<span data-ttu-id="5dbb5-264">提供紋理陣列，每個紋理含有 Mipmap，陣列切片 (以白色矩形代表) 則包含一個紋理及其所有子紋理，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-264">Given an array of textures, each texture with mipmaps, an array slice (represented by the white rectangle) includes one texture and all of its subtextures, as shown in the following illustration.</span></span>

![陣列切片的圖例](images/d3d10-resource-array-slice.png)

### <a name="mip-slice"></a><span data-ttu-id="5dbb5-266">Mip 切片</span><span class="sxs-lookup"><span data-stu-id="5dbb5-266">Mip Slice</span></span>

<span data-ttu-id="5dbb5-267">Mip 切片 (以白色矩形代表) 對於陣列中的每個紋理包含一個 Mipmap 層次，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-267">A mip slice (represented by the white rectangle) includes one mipmap level for every texture in an array, as shown in the following illustration.</span></span>

![Mip 切片的圖例](images/d3d10-resource-mip-slice.png)

### <a name="selecting-a-single-subresource"></a><span data-ttu-id="5dbb5-269">選取單一子資源</span><span class="sxs-lookup"><span data-stu-id="5dbb5-269">Selecting a Single Subresource</span></span>

<span data-ttu-id="5dbb5-270">您可以使用這兩種切片來選擇單一子資源，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-270">You can use these two types of slices to choose a single subresource, as shown in the following illustration.</span></span>

![使用陣列切片和 Mip 切片選擇子資源的圖例](images/d3d10-resource-subresources-1.png)

### <a name="selecting-multiple-subresources"></a><span data-ttu-id="5dbb5-272">選取多個子資源</span><span class="sxs-lookup"><span data-stu-id="5dbb5-272">Selecting Multiple Subresources</span></span>

<span data-ttu-id="5dbb5-273">或者，您也可以使用含有數個 Mipmap 層次和/或數個紋理的這兩種切片，來選取多個子資源。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-273">Or you can use these two types of slices with the number of mipmap levels and/or number of textures, to choose multiple subresources.</span></span>

![選取多個子資源的圖例](images/d3d10-resource-subresources-2.png)

<span data-ttu-id="5dbb5-275">無論您使用何種材質類型（不論是否有 mipmap），不論是否有材質陣列，您都可以使用 helper 函數 [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource)來計算特定 subresource 的索引。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-275">Regardless of what texture type you are using, with or without mipmaps, with or without a texture array, you can use the helper function, [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource), to compute the index of a particular subresource.</span></span>

### <a name="strong-vs-weak-typing"></a><span data-ttu-id="5dbb5-276">強輸入與弱輸入</span><span class="sxs-lookup"><span data-stu-id="5dbb5-276">Strong vs. Weak Typing</span></span>

<span data-ttu-id="5dbb5-277">建立完整具類型的資源會限制資源為其建立時使用的格式。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-277">Creating a fully-typed resource restricts the resource to the format it was created with.</span></span> <span data-ttu-id="5dbb5-278">這可讓執行時間將存取優化，特別是在建立資源時，其旗標表示應用程式無法 [對應](d3d10-graphics-programming-guide-resources-mapping.md) 。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-278">This enables the runtime to optimize access, especially if the resource is created with flags indicating that it cannot be [mapped](d3d10-graphics-programming-guide-resources-mapping.md) by the application.</span></span> <span data-ttu-id="5dbb5-279">使用特定類型建立的資源無法使用檢視機制重新解譯。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-279">Resources created with a specific type cannot be reinterpreted using the view mechanism.</span></span>

<span data-ttu-id="5dbb5-280">在類型較少的資源中，第一次建立資源時，資料類型是未知的。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-280">In a type less resource, the data type is unknown when the resource is first created.</span></span> <span data-ttu-id="5dbb5-281">應用程式必須從可用的類型格式較少選擇 (查看 [**DXGI \_ 格式**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)) 。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-281">The application must choose from the available type less formats (see [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span></span> <span data-ttu-id="5dbb5-282">您必須指定要配置的記憶體大小，以及執行階段是否需要在 Mipmap 中產生子紋理。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-282">You must specify the size of the memory to allocate and whether the runtime will need to generate the subtextures in a mipmap.</span></span> <span data-ttu-id="5dbb5-283">不過，確實的資料格式 (記憶體是否解釋為整數、浮點值、未簽署的整數等) 要到資源使用檢視繫結到管線時才能確定。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-283">However, the exact data format (whether the memory will be interpreted as integers, floating point values, unsigned integers etc.) is not determined until the resource is bound to the pipeline with a view.</span></span> <span data-ttu-id="5dbb5-284">因為直到紋理繫結到管線，紋理格式均維持彈性，所以資源稱為弱輸入的儲存空間。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-284">As the texture format remains flexible until the texture is bound to the pipeline, the resource is referred to as weakly typed storage.</span></span> <span data-ttu-id="5dbb5-285">弱輸入儲存空間的優點，是可以重複使用或重新解譯 (使用另一種格式)，只要新格式的元件位元符合舊格式的位元計數。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-285">Weakly typed storage has the advantage that it can be reused or reinterpreted (in another format) as long as the component bit of the new format matches the bit count of the old format.</span></span>

<span data-ttu-id="5dbb5-286">單一資源可以繫結至多個管線階段，只要每一個都有唯一檢視，而這完全符合每個位置的格式。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-286">A single resource can be bound to multiple pipeline stages as long as each has a unique view, which fully qualifies the formats at each location.</span></span> <span data-ttu-id="5dbb5-287">例如，使用格式 DXGI 格式 R32G32B32A32 的資源， \_ \_ 可以當做 \_ dxgi \_ 格式 \_ R32G32B32A32 \_ FLOAT，也可以在 \_ \_ \_ 管線中的不同位置同時使用 dxgi 格式 R32G32B32A32 UINT。</span><span class="sxs-lookup"><span data-stu-id="5dbb5-287">For example, a resource created with the format DXGI\_FORMAT\_R32G32B32A32\_TYPELESS could be used as an DXGI\_FORMAT\_R32G32B32A32\_FLOAT and an DXGI\_FORMAT\_R32G32B32A32\_UINT at different locations in the pipeline simultaneously.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5dbb5-288">相關主題</span><span class="sxs-lookup"><span data-stu-id="5dbb5-288">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5dbb5-289"> (Direct3D 10) 的資源 </span><span class="sxs-lookup"><span data-stu-id="5dbb5-289">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 

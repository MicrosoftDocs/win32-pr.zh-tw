---
title: Direct3D 11 中的緩衝區簡介
description: 緩衝區資源是一個完整輸入的資料集合，由元素所組成。
ms.assetid: e33ca01e-f13c-4f91-b0db-2b2bc6b4fd8f
keywords:
- 常數緩衝區，什麼是
- 頂點緩衝區，什麼是
- 索引緩衝區，什麼是
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 241ade0721ae87b1371586bc901ee18f8975b53f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315451"
---
# <a name="introduction-to-buffers-in-direct3d-11"></a><span data-ttu-id="e94eb-106">Direct3D 11 中的緩衝區簡介</span><span class="sxs-lookup"><span data-stu-id="e94eb-106">Introduction to Buffers in Direct3D 11</span></span>

<span data-ttu-id="e94eb-107">緩衝區資源是一個完整輸入的資料集合，由元素所組成。</span><span class="sxs-lookup"><span data-stu-id="e94eb-107">A buffer resource is a collection of fully typed data grouped into elements.</span></span> <span data-ttu-id="e94eb-108">您可以使用緩衝區存放各式各樣的資料，包含位置向量、法向向量、頂點緩衝區中的紋理座標、索引緩衝區中的索引、或裝置狀態。</span><span class="sxs-lookup"><span data-stu-id="e94eb-108">You can use buffers to store a wide variety of data, including position vectors, normal vectors, texture coordinates in a vertex buffer, indexes in an index buffer, or device state.</span></span> <span data-ttu-id="e94eb-109">緩衝元素由 1 到 4 個元件組成。</span><span class="sxs-lookup"><span data-stu-id="e94eb-109">A buffer element is made up of 1 to 4 components.</span></span> <span data-ttu-id="e94eb-110">緩衝元素可以包含封裝資料值 (像是 R8G8B8A8 面值)、單一 8 位整數，或四個 32 位元浮點數值。</span><span class="sxs-lookup"><span data-stu-id="e94eb-110">Buffer elements can include packed data values (like R8G8B8A8 surface values), single 8-bit integers, or four 32-bit floating point values.</span></span>

<span data-ttu-id="e94eb-111">建立緩衝區做為未結構化的資源。</span><span class="sxs-lookup"><span data-stu-id="e94eb-111">A buffer is created as an unstructured resource.</span></span> <span data-ttu-id="e94eb-112">因為未建立，緩衝不能包含任何 mipmap 層次，當讀取時無法篩選，而且無法多重採樣。</span><span class="sxs-lookup"><span data-stu-id="e94eb-112">Because it is unstructured, a buffer cannot contain any mipmap levels, it cannot get filtered when read, and it cannot be multisampled.</span></span>

## <a name="buffer-types"></a><span data-ttu-id="e94eb-113">緩衝區類型</span><span class="sxs-lookup"><span data-stu-id="e94eb-113">Buffer Types</span></span>

<span data-ttu-id="e94eb-114">以下是 Direct3D 11 支援的緩衝區資源類型。</span><span class="sxs-lookup"><span data-stu-id="e94eb-114">The following are the buffer resource types supported by Direct3D 11.</span></span> <span data-ttu-id="e94eb-115">所有緩衝區類型都是由 [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) 介面所封裝。</span><span class="sxs-lookup"><span data-stu-id="e94eb-115">All buffer types are encapsulated by the [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) interface.</span></span>

-   [<span data-ttu-id="e94eb-116">頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="e94eb-116">Vertex Buffer</span></span>](#vertex-buffer)
-   [<span data-ttu-id="e94eb-117">索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="e94eb-117">Index Buffer</span></span>](#index-buffer)
-   [<span data-ttu-id="e94eb-118">常數緩衝區</span><span class="sxs-lookup"><span data-stu-id="e94eb-118">Constant Buffer</span></span>](#constant-buffer)

### <a name="vertex-buffer"></a><span data-ttu-id="e94eb-119">頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="e94eb-119">Vertex Buffer</span></span>

<span data-ttu-id="e94eb-120">頂點緩衝區包含用來定義您的幾何頂點資料。</span><span class="sxs-lookup"><span data-stu-id="e94eb-120">A vertex buffer contains the vertex data used to define your geometry.</span></span> <span data-ttu-id="e94eb-121">頂點資料包括位置座標、色彩資料、紋理座標資料、一般資料等等。</span><span class="sxs-lookup"><span data-stu-id="e94eb-121">Vertex data includes position coordinates, color data, texture coordinate data, normal data, and so on.</span></span>

<span data-ttu-id="e94eb-122">最簡單的頂點緩衝區範例是僅包含位置資料者。</span><span class="sxs-lookup"><span data-stu-id="e94eb-122">The simplest example of a vertex buffer is one that only contains position data.</span></span> <span data-ttu-id="e94eb-123">它可以像下圖一樣視覺化。</span><span class="sxs-lookup"><span data-stu-id="e94eb-123">It can be visualized like the following illustration.</span></span>

![包含位置資料的頂點緩衝區圖例](images/d3d10-resources-single-element-vb2.png)

<span data-ttu-id="e94eb-125">頂點緩衝區經常包含可完整指定 3D 頂點所需的所有資料。</span><span class="sxs-lookup"><span data-stu-id="e94eb-125">More often, a vertex buffer contains all the data needed to fully specify 3D vertices.</span></span> <span data-ttu-id="e94eb-126">例如，可能會包含每個頂點位置、一般及紋理座標的頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e94eb-126">An example of this could be a vertex buffer that contains per-vertex position, normal and texture coordinates.</span></span> <span data-ttu-id="e94eb-127">此資料通常組織成每個頂點元素集，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="e94eb-127">This data is usually organized as sets of per-vertex elements, as shown in the following illustration.</span></span>

![頂點緩區的圖例，其包含位置、一般和紋理資料](images/d3d10-vertex-buffer-element.png)

<span data-ttu-id="e94eb-129">這個頂點緩衝區包含每個頂點資料，而每個頂點儲存三個元素 (位置、一般和紋理座標)。</span><span class="sxs-lookup"><span data-stu-id="e94eb-129">This vertex buffer contains per-vertex data; each vertex stores three elements (position, normal, and texture coordinates).</span></span> <span data-ttu-id="e94eb-130">位置和一般都是使用 3 32 位浮點數 (DXGI \_ 格式 \_ R32G32B32 \_ FLOAT) 和材質座標（使用 2 32 位浮點數 (\_ \_ float 格式 R32G32 \_ FLOAT) ）來指定。</span><span class="sxs-lookup"><span data-stu-id="e94eb-130">The position and normal are each typically specified using three 32-bit floats (DXGI\_FORMAT\_R32G32B32\_FLOAT) and the texture coordinates using two 32-bit floats (DXGI\_FORMAT\_R32G32\_FLOAT).</span></span>

<span data-ttu-id="e94eb-131">若要存取頂點緩衝區的資料，您需要知道所存取的頂點，再加上以下額外緩衝區參數︰</span><span class="sxs-lookup"><span data-stu-id="e94eb-131">To access data from a vertex buffer you need to know which vertex to access, plus the following additional buffer parameters:</span></span>

-   <span data-ttu-id="e94eb-132">位移 - 從緩衝區的起始到第一個頂點資料的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="e94eb-132">Offset - the number of bytes from the start of the buffer to the data for the first vertex.</span></span> <span data-ttu-id="e94eb-133">您可以使用 [**>id3d11devicecoNtext：： IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers) 方法來指定位移。</span><span class="sxs-lookup"><span data-stu-id="e94eb-133">You can specify the offset using the [**ID3D11DeviceContext::IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers) method.</span></span>
-   <span data-ttu-id="e94eb-134">BaseVertexLocation - 從位移到適當繪製呼叫所使用的第一個頂點的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="e94eb-134">BaseVertexLocation - the number of bytes from the offset to the first vertex used by the appropriate draw call.</span></span>

<span data-ttu-id="e94eb-135">在建立頂點緩衝區之前，您必須先建立 [**ID3D11InputLayout**](/windows/win32/api/d3d11/nn-d3d11-id3d11inputlayout) 介面來定義其版面配置;這是藉由呼叫 [**ID3D11Device：： CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout) 方法來完成。</span><span class="sxs-lookup"><span data-stu-id="e94eb-135">Before you create a vertex buffer, you need to define its layout by creating an [**ID3D11InputLayout**](/windows/win32/api/d3d11/nn-d3d11-id3d11inputlayout) interface; this is done by calling the [**ID3D11Device::CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout) method.</span></span> <span data-ttu-id="e94eb-136">在建立輸入設定物件之後，您可以藉由呼叫 [**>id3d11devicecoNtext：： IASetInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetinputlayout)，將它系結至輸入組合語言階段。</span><span class="sxs-lookup"><span data-stu-id="e94eb-136">After the input-layout object is created, you can bind it to the input-assembler stage by calling the [**ID3D11DeviceContext::IASetInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetinputlayout).</span></span>

<span data-ttu-id="e94eb-137">若要建立頂點緩衝區，請呼叫 [**ID3D11Device：： CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer)。</span><span class="sxs-lookup"><span data-stu-id="e94eb-137">To create a vertex buffer, call [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer).</span></span>

### <a name="index-buffer"></a><span data-ttu-id="e94eb-138">索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="e94eb-138">Index Buffer</span></span>

<span data-ttu-id="e94eb-139">索引緩衝包含整數位移至頂點緩衝區，可用於更有效率地呈現基本類型。</span><span class="sxs-lookup"><span data-stu-id="e94eb-139">Index buffers contain integer offsets into vertex buffers and are used to render primitives more efficiently.</span></span> <span data-ttu-id="e94eb-140">索引緩衝區包含連續的 16 位元或 32 位元索引集，而每個索引用來識別頂點緩衝區中的頂點。</span><span class="sxs-lookup"><span data-stu-id="e94eb-140">An index buffer contains a sequential set of 16-bit or 32-bit indices; each index is used to identify a vertex in a vertex buffer.</span></span> <span data-ttu-id="e94eb-141">索引緩衝區可以視覺化，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="e94eb-141">An index buffer can be visualized like the following illustration.</span></span>

![索引緩衝區的圖例](images/d3d10-index-buffer.png)

<span data-ttu-id="e94eb-143">儲存在索引緩衝區中的循序索引，使用以下參數尋找︰</span><span class="sxs-lookup"><span data-stu-id="e94eb-143">The sequential indices stored in an index buffer are located with the following parameters:</span></span>

-   <span data-ttu-id="e94eb-144">Offset - 索引緩衝的基底位址的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="e94eb-144">Offset - the number of bytes from the base address of the index buffer.</span></span> <span data-ttu-id="e94eb-145">位移會提供給 [**>id3d11devicecoNtext：： IASetIndexBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer) 方法。</span><span class="sxs-lookup"><span data-stu-id="e94eb-145">The offset is supplied to the [**ID3D11DeviceContext::IASetIndexBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer) method.</span></span>
-   <span data-ttu-id="e94eb-146">StartIndexLocation-指定基底位址中的第一個索引緩衝區元素，以及 [**IASetIndexBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer)中提供的位移。</span><span class="sxs-lookup"><span data-stu-id="e94eb-146">StartIndexLocation - specifies the first index buffer element from the base address and the offset provided in [**IASetIndexBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer).</span></span> <span data-ttu-id="e94eb-147">開始位置會提供給 [**>id3d11devicecoNtext：:D rawindexed**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed) 或 [**>id3d11devicecoNtext：:D rawindexedinstanced**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced) 方法，並代表要轉譯的第一個索引。</span><span class="sxs-lookup"><span data-stu-id="e94eb-147">The start location is supplied to the [**ID3D11DeviceContext::DrawIndexed**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed) or [**ID3D11DeviceContext::DrawIndexedInstanced**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced) method and represents the first index to render.</span></span>
-   <span data-ttu-id="e94eb-148">IndexCount - 要呈現的索引數目。</span><span class="sxs-lookup"><span data-stu-id="e94eb-148">IndexCount - the number of indices to render.</span></span> <span data-ttu-id="e94eb-149">此數位會提供給 [**DrawIndexed**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed) 方法</span><span class="sxs-lookup"><span data-stu-id="e94eb-149">The number is supplied to the [**DrawIndexed**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed) method</span></span>

<span data-ttu-id="e94eb-150">索引緩衝區的開頭 = 索引緩衝區基底位址 + 位移 (位元組) + StartIndexLocation \* ElementSize (位元組) ;</span><span class="sxs-lookup"><span data-stu-id="e94eb-150">Start of Index Buffer = Index Buffer Base Address + Offset (bytes) + StartIndexLocation \* ElementSize (bytes);</span></span>

<span data-ttu-id="e94eb-151">在這個運算中，ElementSize 是各索引緩衝元素的大小，不是兩個就是四個位元組。</span><span class="sxs-lookup"><span data-stu-id="e94eb-151">In this calculation, ElementSize is the size of each index buffer element, which is either two or four bytes.</span></span>

<span data-ttu-id="e94eb-152">若要建立索引緩衝區，請呼叫 [**ID3D11Device：： CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer)。</span><span class="sxs-lookup"><span data-stu-id="e94eb-152">To create an index buffer, call [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer).</span></span>

### <a name="constant-buffer"></a><span data-ttu-id="e94eb-153">常數緩衝區</span><span class="sxs-lookup"><span data-stu-id="e94eb-153">Constant Buffer</span></span>

<span data-ttu-id="e94eb-154">常數緩衝區可讓您有效率地提供著色器常數資料至管線。</span><span class="sxs-lookup"><span data-stu-id="e94eb-154">A constant buffer allows you to efficiently supply shader constants data to the pipeline.</span></span> <span data-ttu-id="e94eb-155">您可以使用常數緩衝區來儲存資料流輸出階段的結果。</span><span class="sxs-lookup"><span data-stu-id="e94eb-155">You can use a constant buffer to store the results of the stream-output stage.</span></span> <span data-ttu-id="e94eb-156">概念上，常數緩衝區看起來很像單一元素頂點緩衝區，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="e94eb-156">Conceptually, a constant buffer looks just like a single-element vertex buffer, as shown in the following illustration.</span></span>

![著色器常數緩衝區的圖例](images/d3d10-shader-resource-buffer.png)

<span data-ttu-id="e94eb-158">每個元素會儲存 1 到 4 個元件常數，取決於儲存的資料格式。</span><span class="sxs-lookup"><span data-stu-id="e94eb-158">Each element stores a 1-to-4 component constant, determined by the format of the data stored.</span></span> <span data-ttu-id="e94eb-159">若要建立著色器常數緩衝區，請呼叫 [**ID3D11Device：： CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) ，並指定 D3D11 系結 [**\_ \_ 旗**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)標列舉型別的 D3D11 系結 **\_ \_ 常數 \_ 緩衝區** 成員。</span><span class="sxs-lookup"><span data-stu-id="e94eb-159">To create a shader-constant buffer, call [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) and specify the **D3D11\_BIND\_CONSTANT\_BUFFER** member of the [**D3D11\_BIND\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) enumerated type.</span></span>

<span data-ttu-id="e94eb-160">常數緩衝區只能使用單一系結旗標 (**D3D11 系 \_ 結 \_ 常數 \_ 緩衝區**) ，其無法與任何其他系結旗標合併。</span><span class="sxs-lookup"><span data-stu-id="e94eb-160">A constant buffer can only use a single bind flag (**D3D11\_BIND\_CONSTANT\_BUFFER**), which cannot be combined with any other bind flag.</span></span> <span data-ttu-id="e94eb-161">若要將著色器常數緩衝區系結至管線，請呼叫下列其中一種方法： [**>id3d11devicecoNtext：： GSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gssetconstantbuffers)、 [**>id3d11devicecoNtext：:P ssetconstantbuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetconstantbuffers)或 [**>id3d11devicecoNtext：： VSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetconstantbuffers)。</span><span class="sxs-lookup"><span data-stu-id="e94eb-161">To bind a shader-constant buffer to the pipeline, call one of the following methods: [**ID3D11DeviceContext::GSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gssetconstantbuffers), [**ID3D11DeviceContext::PSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetconstantbuffers), or [**ID3D11DeviceContext::VSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetconstantbuffers).</span></span>

<span data-ttu-id="e94eb-162">若要從著色器讀取著色器常數緩衝區，請使用 HLSL load 函數 (例如 [**load**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load)) 。</span><span class="sxs-lookup"><span data-stu-id="e94eb-162">To read a shader-constant buffer from a shader, use a HLSL load function (for example, [**Load**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load)).</span></span> <span data-ttu-id="e94eb-163">每個著色器階段允許最多 15 個著色器常數緩衝區，而每個緩衝區可保留最多 4096 個常數。</span><span class="sxs-lookup"><span data-stu-id="e94eb-163">Each shader stage allows up to 15 shader-constant buffers; each buffer can hold up to 4096 constants.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e94eb-164">相關主題</span><span class="sxs-lookup"><span data-stu-id="e94eb-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e94eb-165">緩衝區</span><span class="sxs-lookup"><span data-stu-id="e94eb-165">Buffers</span></span>](overviews-direct3d-11-resources-buffers.md)
</dt> </dl>

 

 
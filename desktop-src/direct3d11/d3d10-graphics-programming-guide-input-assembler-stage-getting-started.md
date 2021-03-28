---
title: 使用 Input-Assembler 階段開始使用
description: 有幾個步驟需要初始化輸入組合語言 (IA) 階段。
ms.assetid: 84c0ca29-2356-4b7f-98ee-ff1758edc540
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901b3facfef781e3f44acf75bee737f280dece55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375800"
---
# <a name="getting-started-with-the-input-assembler-stage"></a><span data-ttu-id="0a56d-103">使用 Input-Assembler 階段開始使用</span><span class="sxs-lookup"><span data-stu-id="0a56d-103">Getting Started with the Input-Assembler Stage</span></span>

<span data-ttu-id="0a56d-104">有幾個步驟需要初始化輸入組合語言 (IA) 階段。</span><span class="sxs-lookup"><span data-stu-id="0a56d-104">There are a few steps necessary to initialize the input-assembler (IA) stage.</span></span> <span data-ttu-id="0a56d-105">例如，您需要使用管線所需的頂點資料來建立緩衝區資源、告知 IA 階段，其中緩衝區是和它們所包含的資料類型，並指定要從資料組合的基本類型。</span><span class="sxs-lookup"><span data-stu-id="0a56d-105">For example, you need to create buffer resources with the vertex data that the pipeline needs, tell the IA stage where the buffers are and what type of data they contain, and specify the type of primitives to assemble from the data.</span></span>

<span data-ttu-id="0a56d-106">本主題將涵蓋設定 IA 階段所需的基本步驟（如下表所示）。</span><span class="sxs-lookup"><span data-stu-id="0a56d-106">The basic steps involved in setting up the IA stage, shown in the following table, are covered in this topic.</span></span>



| <span data-ttu-id="0a56d-107">步驟</span><span class="sxs-lookup"><span data-stu-id="0a56d-107">Step</span></span>                                                                                    | <span data-ttu-id="0a56d-108">描述</span><span class="sxs-lookup"><span data-stu-id="0a56d-108">Description</span></span>                                                                                           |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0a56d-109">建立輸入緩衝區</span><span class="sxs-lookup"><span data-stu-id="0a56d-109">Create Input Buffers</span></span>](#create-input-buffers)                                           | <span data-ttu-id="0a56d-110">使用輸入頂點資料來建立和初始化輸入緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0a56d-110">Create and initialize input buffers with input vertex data.</span></span>                                           |
| [<span data-ttu-id="0a56d-111">建立 Input-Layout 物件</span><span class="sxs-lookup"><span data-stu-id="0a56d-111">Create the Input-Layout Object</span></span>](#create-the-input-layout-object)                       | <span data-ttu-id="0a56d-112">定義如何使用輸入設定物件，將頂點緩衝區資料串流至 IA 階段。</span><span class="sxs-lookup"><span data-stu-id="0a56d-112">Define how the vertex buffer data will be streamed into the IA stage by using an input-layout object.</span></span> |
| [<span data-ttu-id="0a56d-113">將物件系結至 Input-Assembler 階段</span><span class="sxs-lookup"><span data-stu-id="0a56d-113">Bind Objects to the Input-Assembler Stage</span></span>](#bind-objects-to-the-input-assembler-stage) | <span data-ttu-id="0a56d-114">將建立的物件 (輸入緩衝區和輸入設定物件) 系結至 IA 階段。</span><span class="sxs-lookup"><span data-stu-id="0a56d-114">Bind the created objects (input buffers and the input-layout object) to the IA stage.</span></span>                 |
| [<span data-ttu-id="0a56d-115">指定基本類型</span><span class="sxs-lookup"><span data-stu-id="0a56d-115">Specify the Primitive Type</span></span>](#specify-the-primitive-type)                               | <span data-ttu-id="0a56d-116">識別如何將頂點組合成基本專案。</span><span class="sxs-lookup"><span data-stu-id="0a56d-116">Identify how the vertices will be assembled into primitives.</span></span>                                          |
| [<span data-ttu-id="0a56d-117">呼叫 Draw 方法</span><span class="sxs-lookup"><span data-stu-id="0a56d-117">Call Draw Methods</span></span>](#call-draw-methods)                                                 | <span data-ttu-id="0a56d-118">透過管線傳送系結至 IA 階段的資料。</span><span class="sxs-lookup"><span data-stu-id="0a56d-118">Send the data bound to the IA stage through the pipeline.</span></span>                                             |



 

<span data-ttu-id="0a56d-119">在您瞭解這些步驟之後，請繼續 [使用 System-Generated 的值](d3d10-graphics-programming-guide-input-assembler-stage-using.md)。</span><span class="sxs-lookup"><span data-stu-id="0a56d-119">After you understand these steps, move on to [Using System-Generated Values](d3d10-graphics-programming-guide-input-assembler-stage-using.md).</span></span>

## <a name="create-input-buffers"></a><span data-ttu-id="0a56d-120">建立輸入緩衝區</span><span class="sxs-lookup"><span data-stu-id="0a56d-120">Create Input Buffers</span></span>

<span data-ttu-id="0a56d-121">輸入緩衝區有兩種類型： [頂點緩衝區](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) 和索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0a56d-121">There are two types of input buffers: [vertex buffers](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) and index buffers.</span></span> <span data-ttu-id="0a56d-122">頂點緩衝區可提供頂點資料給 IA 階段。</span><span class="sxs-lookup"><span data-stu-id="0a56d-122">Vertex buffers supply vertex data to the IA stage.</span></span> <span data-ttu-id="0a56d-123">索引緩衝區是選擇性的;它們會從頂點緩衝區提供頂點的索引。</span><span class="sxs-lookup"><span data-stu-id="0a56d-123">Index buffers are optional; they provide indices to vertices from the vertex buffer.</span></span> <span data-ttu-id="0a56d-124">您可以建立一或多個頂點緩衝區，並選擇性地建立索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0a56d-124">You may create one or more vertex buffers and, optionally, an index buffer.</span></span>

<span data-ttu-id="0a56d-125">建立緩衝區資源之後，您必須建立輸入設定物件來描述 IA 階段的資料版面配置，然後您必須將緩衝區資源系結至 IA 階段。</span><span class="sxs-lookup"><span data-stu-id="0a56d-125">After you create the buffer resources, you need to create an input-layout object to describe the data layout to the IA stage, and then you need to bind the buffer resources to the IA stage.</span></span> <span data-ttu-id="0a56d-126">如果您的著色器未使用緩衝區，則不需要建立和系結緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0a56d-126">Creating and binding buffers is not necessary if your shaders don't use buffers.</span></span> <span data-ttu-id="0a56d-127">如需繪製單一三角形的簡單頂點和圖元著色器範例，請參閱 [使用不含緩衝區的 Input-Assembler 階段](d3d10-graphics-programming-guide-input-assembler-stage-no-buffers.md)。</span><span class="sxs-lookup"><span data-stu-id="0a56d-127">For an example of a simple vertex and pixel shader that draws a single triangle, see [Using the Input-Assembler Stage without Buffers](d3d10-graphics-programming-guide-input-assembler-stage-no-buffers.md).</span></span>

<span data-ttu-id="0a56d-128">如需建立頂點緩衝區的協助，請參閱 [建立頂點緩衝區](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating)。</span><span class="sxs-lookup"><span data-stu-id="0a56d-128">For help with creating a vertex buffer, see [Create a Vertex Buffer](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating).</span></span> <span data-ttu-id="0a56d-129">如需建立索引緩衝區的協助，請參閱建立索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0a56d-129">For help with creating an index buffer, see Create an Index Buffer.</span></span>

## <a name="create-the-input-layout-object"></a><span data-ttu-id="0a56d-130">建立 Input-Layout 物件</span><span class="sxs-lookup"><span data-stu-id="0a56d-130">Create the Input-Layout Object</span></span>

<span data-ttu-id="0a56d-131">輸入設定物件會封裝 IA 階段的輸入狀態。</span><span class="sxs-lookup"><span data-stu-id="0a56d-131">The input-layout object encapsulates the input state of the IA stage.</span></span> <span data-ttu-id="0a56d-132">這包括系結至 IA 階段之輸入資料的描述。</span><span class="sxs-lookup"><span data-stu-id="0a56d-132">This includes a description of the input data that is bound to the IA stage.</span></span> <span data-ttu-id="0a56d-133">從一或多個頂點緩衝區，將資料從記憶體串流至 IA 階段。</span><span class="sxs-lookup"><span data-stu-id="0a56d-133">The data is streamed into the IA stage from memory, from one or more vertex buffers.</span></span> <span data-ttu-id="0a56d-134">描述會識別從一個或多個頂點緩衝區系結的輸入資料，並讓執行時間能夠根據著色器輸入參數類型來檢查輸入資料類型。</span><span class="sxs-lookup"><span data-stu-id="0a56d-134">The description identifies the input data that is bound from one or more vertex buffers and gives the runtime the ability to check the input data types against the shader input parameter types.</span></span> <span data-ttu-id="0a56d-135">這種類型檢查不只會驗證類型是否相容，而且每個著色器所需的元素都可在緩衝區資源中使用。</span><span class="sxs-lookup"><span data-stu-id="0a56d-135">This type checking not only verifies that the types are compatible, but also that each of the elements that the shader requires is available in the buffer resources.</span></span>

<span data-ttu-id="0a56d-136">輸入設定物件是從輸入-元素描述的陣列和已編譯著色器的指標所建立 (請參閱 [**ID3D11Device：： CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout)) 。</span><span class="sxs-lookup"><span data-stu-id="0a56d-136">An input-layout object is created from an array of input-element descriptions and a pointer to the compiled shader (see [**ID3D11Device::CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout)).</span></span> <span data-ttu-id="0a56d-137">陣列包含一或多個輸入元素;每個輸入元素都會從單一頂點緩衝區描述單一頂點資料元素。</span><span class="sxs-lookup"><span data-stu-id="0a56d-137">The array contains one or more input elements; each input element describes a single vertex-data element from a single vertex buffer.</span></span> <span data-ttu-id="0a56d-138">整組輸入元素描述會描述所有將繫結至 IA 階段的端點緩衝區中的所有頂點資料元素。</span><span class="sxs-lookup"><span data-stu-id="0a56d-138">The entire set of input-element descriptions describes all of the vertex-data elements from all of the vertex buffers that will be bound to the IA stage.</span></span>

<span data-ttu-id="0a56d-139">下列版面配置描述描述包含三個頂點資料元素的單一頂點緩衝區：</span><span class="sxs-lookup"><span data-stu-id="0a56d-139">The following layout description describes a single vertex buffer that contains three vertex-data elements:</span></span>


```
D3D11_INPUT_ELEMENT_DESC layout[] =
{
    { L"POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 0, 
          D3D11_INPUT_PER_VERTEX_DATA, 0 },
    { L"TEXCOORD", 0, DXGI_FORMAT_R32G32_FLOAT, 0, 12, 
          D3D11_INPUT_PER_VERTEX_DATA, 0 },
    { L"NORMAL", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 20, 
          D3D11_INPUT_PER_VERTEX_DATA, 0 },
};
```



<span data-ttu-id="0a56d-140">輸入專案描述會描述頂點緩衝區中單一頂點所包含的每個專案，包括大小、類型、位置和用途。</span><span class="sxs-lookup"><span data-stu-id="0a56d-140">An input-element description describes each element contained by a single vertex in a vertex buffer, including size, type, location, and purpose.</span></span> <span data-ttu-id="0a56d-141">每個資料列都會使用語義、語義索引和資料格式來識別資料的類型。</span><span class="sxs-lookup"><span data-stu-id="0a56d-141">Each row identifies the type of data by using the semantic, the semantic index, and the data format.</span></span> <span data-ttu-id="0a56d-142">[語義](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)是識別資料使用方式的文字字串。</span><span class="sxs-lookup"><span data-stu-id="0a56d-142">A [semantic](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) is a text string that identifies how the data will be used.</span></span> <span data-ttu-id="0a56d-143">在此範例中，第一個資料列會識別3個元件的位置資料 (*xyz*，例如) ;第二個數據列會識別兩個元件的材質資料 (*UV*，例如) ;第三個數據列會識別一般資料。</span><span class="sxs-lookup"><span data-stu-id="0a56d-143">In this example, the first row identifies 3-component position data (*xyz*, for example); the second row identifies 2-component texture data (*UV*, for example); and the third row identifies normal data.</span></span>

<span data-ttu-id="0a56d-144">在此輸入專案描述的範例中，語義索引 (這三個數據列的第二個參數) 設定為零。</span><span class="sxs-lookup"><span data-stu-id="0a56d-144">In this example of an input-element description, the semantic index (which is the second parameter) is set to zero for all three rows.</span></span> <span data-ttu-id="0a56d-145">語義索引可協助您區分兩個使用相同語義的資料列。</span><span class="sxs-lookup"><span data-stu-id="0a56d-145">The semantic index helps distinguish between two rows that use the same semantics.</span></span> <span data-ttu-id="0a56d-146">因為此範例中沒有類似的語法，所以可以將語義索引設定為其預設值零。</span><span class="sxs-lookup"><span data-stu-id="0a56d-146">Since there are no similar semantics in this example, the semantic index can be set to its default value, zero.</span></span>

<span data-ttu-id="0a56d-147">第三個參數是 *格式*。</span><span class="sxs-lookup"><span data-stu-id="0a56d-147">The third parameter is the *format*.</span></span> <span data-ttu-id="0a56d-148">格式 (請參閱 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) 指定每個元素的元件數目，以及資料類型，該資料類型會定義每個元素的資料大小。</span><span class="sxs-lookup"><span data-stu-id="0a56d-148">The format (see [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) specifies the number of components per element, and the data type, which defines the size of the data for each element.</span></span> <span data-ttu-id="0a56d-149">在建立資源時可以完全輸入格式，或您可以使用 **DXGI \_ 格式** 來建立資源，以識別元素中的元件數目，但不定義資料類型。</span><span class="sxs-lookup"><span data-stu-id="0a56d-149">The format can be fully typed at the time of resource creation, or you may create a resource by using a **DXGI\_FORMAT**, which identifies the number of components in an element, but leaves the data type undefined.</span></span>

### <a name="input-slots"></a><span data-ttu-id="0a56d-150">輸入位置</span><span class="sxs-lookup"><span data-stu-id="0a56d-150">Input Slots</span></span>

<span data-ttu-id="0a56d-151">資料會透過稱為 *輸入* 位置的輸入進入 IA 階段，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="0a56d-151">Data enters the IA stage through inputs called *input slots*, as shown in the following illustration.</span></span> <span data-ttu-id="0a56d-152">IA 階段有 *n* 個輸入位置，其設計目的是要容納最多可提供輸入資料的 *n* 個頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0a56d-152">The IA stage has *n* input slots, which are designed to accommodate up to *n* vertex buffers that provide input data.</span></span> <span data-ttu-id="0a56d-153">每個頂點緩衝區都必須指派給不同的位置;當輸入設定物件建立時，這項資訊會儲存在輸入配置宣告中。</span><span class="sxs-lookup"><span data-stu-id="0a56d-153">Each vertex buffer must be assigned to a different slot; this information is stored in the input-layout declaration when the input-layout object is created.</span></span> <span data-ttu-id="0a56d-154">您也可以指定從每個緩衝區開頭到要讀取之緩衝區中第一個元素的位移。</span><span class="sxs-lookup"><span data-stu-id="0a56d-154">You may also specify an offset from the start of each buffer to the first element in the buffer to be read.</span></span>

![ia 階段輸入位置的圖例](images/d3d10-ia-slots.png)

<span data-ttu-id="0a56d-156">接下來的兩個參數是 *輸入* 位置和 *輸入位移*。</span><span class="sxs-lookup"><span data-stu-id="0a56d-156">The next two parameters are the *input slot* and the *input offset*.</span></span> <span data-ttu-id="0a56d-157">當您使用多個緩衝區時，可以將它們系結至一或多個輸入位置。</span><span class="sxs-lookup"><span data-stu-id="0a56d-157">When you use multiple buffers, you can bind them to one or more input slots.</span></span> <span data-ttu-id="0a56d-158">輸入位移是緩衝區開頭與資料開頭之間的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="0a56d-158">The input offset is the number of bytes between the start of the buffer and the beginning of the data.</span></span>

### <a name="reusing-input-layout-objects"></a><span data-ttu-id="0a56d-159">重複使用 Input-Layout 物件</span><span class="sxs-lookup"><span data-stu-id="0a56d-159">Reusing Input-Layout Objects</span></span>

<span data-ttu-id="0a56d-160">每個輸入設定物件都會根據著色器簽章建立;這可讓 API 針對著色器輸入簽章來驗證輸入設定物件元素，以確保與類型和語義完全相符。</span><span class="sxs-lookup"><span data-stu-id="0a56d-160">Each input-layout object is created based on a shader signature; this allows the API to validate the input-layout-object elements against the shader-input signature to make sure that there is an exact match of types and semantics.</span></span> <span data-ttu-id="0a56d-161">只要所有著色器輸入簽章完全相符，您就可以為許多著色器建立單一的輸入版面設定物件。</span><span class="sxs-lookup"><span data-stu-id="0a56d-161">You can create a single input-layout object for many shaders, as long as all of the shader-input signatures exactly match.</span></span>

## <a name="bind-objects-to-the-input-assembler-stage"></a><span data-ttu-id="0a56d-162">將物件系結至 Input-Assembler 階段</span><span class="sxs-lookup"><span data-stu-id="0a56d-162">Bind Objects to the Input-Assembler Stage</span></span>

<span data-ttu-id="0a56d-163">建立頂點緩衝區資源和輸入設定物件之後，您可以藉由呼叫 [**>id3d11devicecoNtext：： IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers) 和 [**>id3d11devicecoNtext：： IASetInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetinputlayout)，將這些資源系結至 IA 階段。</span><span class="sxs-lookup"><span data-stu-id="0a56d-163">After you create vertex buffer resources and an input layout object, you can bind them to the IA stage by calling [**ID3D11DeviceContext::IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers) and [**ID3D11DeviceContext::IASetInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetinputlayout).</span></span> <span data-ttu-id="0a56d-164">下列範例顯示將單一頂點緩衝區和輸入設定物件系結至 IA 階段：</span><span class="sxs-lookup"><span data-stu-id="0a56d-164">The following example shows the binding of a single vertex buffer and an input-layout object to the IA stage:</span></span>


```
UINT stride = sizeof( SimpleVertex );
UINT offset = 0;
g_pd3dDevice->IASetVertexBuffers( 
    0,                // the first input slot for binding
    1,                // the number of buffers in the array
    &g_pVertexBuffer, // the array of vertex buffers
    &stride,          // array of stride values, one for each buffer
    &offset );        // array of offset values, one for each buffer

// Set the input layout
g_pd3dDevice->IASetInputLayout( g_pVertexLayout );
```



<span data-ttu-id="0a56d-165">系結輸入版面設定物件只需要物件的指標。</span><span class="sxs-lookup"><span data-stu-id="0a56d-165">Binding the input-layout object only requires a pointer to the object.</span></span>

<span data-ttu-id="0a56d-166">在上述範例中，會系結單一頂點緩衝區;不過，多個頂點緩衝區可透過單一呼叫 [**>id3d11devicecoNtext：： IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers)來系結，而下列程式碼會顯示系結三個頂點緩衝區的呼叫：</span><span class="sxs-lookup"><span data-stu-id="0a56d-166">In the preceding example, a single vertex buffer is bound; however, multiple vertex buffers can be bound by a single call to [**ID3D11DeviceContext::IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers), and the following code shows such a call to bind three vertex buffers:</span></span>


```
UINT strides[3];
strides[0] = sizeof(SimpleVertex1);
strides[1] = sizeof(SimpleVertex2);
strides[2] = sizeof(SimpleVertex3);
UINT offsets[3] = { 0, 0, 0 };
g_pd3dDevice->IASetVertexBuffers( 
    0,                 //first input slot for binding
    3,                 //number of buffers in the array
    &g_pVertexBuffers, //array of three vertex buffers
    &strides,          //array of stride values, one for each buffer
    &offsets );        //array of offset values, one for each buffer
```



<span data-ttu-id="0a56d-167">索引緩衝區會藉由呼叫 [**>id3d11devicecoNtext：： IASetIndexBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer)來系結至 IA 階段。</span><span class="sxs-lookup"><span data-stu-id="0a56d-167">An index buffer is bound to the IA stage by calling [**ID3D11DeviceContext::IASetIndexBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer).</span></span>

## <a name="specify-the-primitive-type"></a><span data-ttu-id="0a56d-168">指定基本類型</span><span class="sxs-lookup"><span data-stu-id="0a56d-168">Specify the Primitive Type</span></span>

<span data-ttu-id="0a56d-169">系結輸入緩衝區之後，必須告知 IA 階段如何將頂點組合成基本專案。</span><span class="sxs-lookup"><span data-stu-id="0a56d-169">After the input buffers have been bound, the IA stage must be told how to assemble the vertices into primitives.</span></span> <span data-ttu-id="0a56d-170">這是藉由呼叫 [**>id3d11devicecoNtext：： IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology); 指定 [基本類型](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-primitive-topologies)來完成下列程式碼會呼叫這個函式，將資料定義為不連續的三角形清單：</span><span class="sxs-lookup"><span data-stu-id="0a56d-170">This is done by specifying the [primitive type](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-primitive-topologies) by calling [**ID3D11DeviceContext::IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology); the following code calls this function to define the data as a triangle list without adjacency:</span></span>


```
g_pd3dDevice->IASetPrimitiveTopology( D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST );
```



<span data-ttu-id="0a56d-171">其餘的基本類型會列在 D3D 基本型 [**\_ \_ 拓撲**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology)中。</span><span class="sxs-lookup"><span data-stu-id="0a56d-171">The rest of the primitive types are listed in [**D3D\_PRIMITIVE\_TOPOLOGY**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology).</span></span>

## <a name="call-draw-methods"></a><span data-ttu-id="0a56d-172">呼叫 Draw 方法</span><span class="sxs-lookup"><span data-stu-id="0a56d-172">Call Draw Methods</span></span>

<span data-ttu-id="0a56d-173">當輸入資源系結至管線之後，應用程式會呼叫 draw 方法來呈現基本專案。</span><span class="sxs-lookup"><span data-stu-id="0a56d-173">After input resources have been bound to the pipeline, an application calls a draw method to render primitives.</span></span> <span data-ttu-id="0a56d-174">有幾個 draw 方法，如下表所示：有些用途是使用索引緩衝區、某些使用實例資料，以及一些從資料流程輸出階段重複使用資料作為輸入組合語言階段輸入的資料。</span><span class="sxs-lookup"><span data-stu-id="0a56d-174">There are several draw methods, which are shown in the following table; some use index buffers, some use instance data, and some reuse data from the streaming-output stage as input to the input-assembler stage.</span></span>



| <span data-ttu-id="0a56d-175">Draw 方法</span><span class="sxs-lookup"><span data-stu-id="0a56d-175">Draw Methods</span></span>                                                                                  | <span data-ttu-id="0a56d-176">Description</span><span class="sxs-lookup"><span data-stu-id="0a56d-176">Description</span></span>                                                                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0a56d-177">**ID3D11DeviceContext::Draw**</span><span class="sxs-lookup"><span data-stu-id="0a56d-177">**ID3D11DeviceContext::Draw**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw)                                 | <span data-ttu-id="0a56d-178">繪製非索引、非實例的基本類型。</span><span class="sxs-lookup"><span data-stu-id="0a56d-178">Draw non-indexed, non-instanced primitives.</span></span>                                                            |
| [<span data-ttu-id="0a56d-179">**ID3D11DeviceContext::DrawInstanced**</span><span class="sxs-lookup"><span data-stu-id="0a56d-179">**ID3D11DeviceContext::DrawInstanced**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawinstanced)               | <span data-ttu-id="0a56d-180">繪製非索引的實例基本專案。</span><span class="sxs-lookup"><span data-stu-id="0a56d-180">Draw non-indexed, instanced primitives.</span></span>                                                                |
| [<span data-ttu-id="0a56d-181">**ID3D11DeviceContext::DrawIndexed**</span><span class="sxs-lookup"><span data-stu-id="0a56d-181">**ID3D11DeviceContext::DrawIndexed**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed)                   | <span data-ttu-id="0a56d-182">繪製索引、非實例的基本類型。</span><span class="sxs-lookup"><span data-stu-id="0a56d-182">Draw indexed, non-instanced primitives.</span></span>                                                                |
| [<span data-ttu-id="0a56d-183">**ID3D11DeviceContext::DrawIndexedInstanced**</span><span class="sxs-lookup"><span data-stu-id="0a56d-183">**ID3D11DeviceContext::DrawIndexedInstanced**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced) | <span data-ttu-id="0a56d-184">繪製已編制索引的實例基本專案。</span><span class="sxs-lookup"><span data-stu-id="0a56d-184">Draw indexed, instanced primitives.</span></span>                                                                    |
| [<span data-ttu-id="0a56d-185">**ID3D11DeviceContext::DrawAuto**</span><span class="sxs-lookup"><span data-stu-id="0a56d-185">**ID3D11DeviceContext::DrawAuto**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawauto)                         | <span data-ttu-id="0a56d-186">從來自資料流程輸出階段的輸入資料，繪製非索引、非實例的基本類型。</span><span class="sxs-lookup"><span data-stu-id="0a56d-186">Draw non-indexed, non-instanced primitives from input data that comes from the streaming-output stage.</span></span> |



 

<span data-ttu-id="0a56d-187">每個 draw 方法都會呈現單一拓撲類型。</span><span class="sxs-lookup"><span data-stu-id="0a56d-187">Each draw method renders a single topology type.</span></span> <span data-ttu-id="0a56d-188">在轉譯期間，不完整的基本 (沒有足夠頂點的專案、缺少索引、部分基本專案，等等) 會以無訊息方式捨棄。</span><span class="sxs-lookup"><span data-stu-id="0a56d-188">During rendering, incomplete primitives (those without enough vertices, lacking indices, partial primitives, and so on) are silently discarded.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a56d-189">相關主題</span><span class="sxs-lookup"><span data-stu-id="0a56d-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a56d-190">輸入組合階段</span><span class="sxs-lookup"><span data-stu-id="0a56d-190">Input-Assembler Stage</span></span>](d3d10-graphics-programming-guide-input-assembler-stage.md)
</dt> </dl>

 

 
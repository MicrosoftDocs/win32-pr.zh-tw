---
title: 間接繪圖和 GPU 剔除
description: D3D12ExecuteIndirect 範例會示範如何使用間接命令來繪製內容。 它也會示範如何在發行之前，在計算著色器中的 GPU 上操作這些命令。
ms.assetid: 09F90837-D6BF-498E-8018-5C28EDD9BDC3
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b016170fbd3b675d5d5a20c1de87f24b04d4804
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "104548363"
---
# <a name="indirect-drawing-and-gpu-culling"></a><span data-ttu-id="155fd-104">間接繪圖和 GPU 剔除</span><span class="sxs-lookup"><span data-stu-id="155fd-104">Indirect drawing and GPU culling</span></span>

<span data-ttu-id="155fd-105">D3D12ExecuteIndirect 範例會示範如何使用間接命令來繪製內容。</span><span class="sxs-lookup"><span data-stu-id="155fd-105">The D3D12ExecuteIndirect sample demonstrates how to use indirect commands to draw content.</span></span> <span data-ttu-id="155fd-106">它也會示範如何在發行之前，在計算著色器中的 GPU 上操作這些命令。</span><span class="sxs-lookup"><span data-stu-id="155fd-106">It also demonstrates how these commands can be manipulated on the GPU in a compute shader before they are issued.</span></span>

-   [<span data-ttu-id="155fd-107">定義間接命令</span><span class="sxs-lookup"><span data-stu-id="155fd-107">Define the indirect commands</span></span>](#define-the-indirect-commands)
-   [<span data-ttu-id="155fd-108">建立圖形並計算根簽章</span><span class="sxs-lookup"><span data-stu-id="155fd-108">Create a graphics and compute root signature</span></span>](#create-a-graphics-and-compute-root-signature)
-   [<span data-ttu-id="155fd-109">建立計算著色器 (SRV) 的著色器資源檢視器</span><span class="sxs-lookup"><span data-stu-id="155fd-109">Create a shader resource view (SRV) for the compute shader</span></span>](#create-a-shader-resource-view-srv-for-the-compute-shader)
-   [<span data-ttu-id="155fd-110">建立間接命令緩衝區</span><span class="sxs-lookup"><span data-stu-id="155fd-110">Create the indirect command buffers</span></span>](#create-the-indirect-command-buffers)
-   [<span data-ttu-id="155fd-111">建立計算 UAVs</span><span class="sxs-lookup"><span data-stu-id="155fd-111">Create the compute UAVs</span></span>](#create-the-compute-uavs)
-   [<span data-ttu-id="155fd-112">繪製框架</span><span class="sxs-lookup"><span data-stu-id="155fd-112">Drawing the frame</span></span>](#drawing-the-frame)
-   [<span data-ttu-id="155fd-113">執行範例</span><span class="sxs-lookup"><span data-stu-id="155fd-113">Run the sample</span></span>](#run-the-sample)
-   [<span data-ttu-id="155fd-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="155fd-114">Related topics</span></span>](#related-topics)

<span data-ttu-id="155fd-115">此範例會建立一個命令緩衝區來描述1024繪製呼叫。</span><span class="sxs-lookup"><span data-stu-id="155fd-115">The sample creates a command buffer that describes 1024 draw calls.</span></span> <span data-ttu-id="155fd-116">每個繪製呼叫都會呈現具有隨機色彩、位置和速度的三角形。</span><span class="sxs-lookup"><span data-stu-id="155fd-116">Each draw call renders a triangle with a random color, position, and velocity.</span></span> <span data-ttu-id="155fd-117">三角形會在螢幕上無休止地建立動畫。</span><span class="sxs-lookup"><span data-stu-id="155fd-117">The triangles animate endlessly across the screen.</span></span> <span data-ttu-id="155fd-118">此範例中有兩種模式。</span><span class="sxs-lookup"><span data-stu-id="155fd-118">There are two modes in this sample.</span></span> <span data-ttu-id="155fd-119">在第一個模式中，計算著色器會檢查間接命令，並決定是否要將該命令新增至未排序的存取視圖 (UAV) 描述應該執行的命令。</span><span class="sxs-lookup"><span data-stu-id="155fd-119">In the first mode, a compute shader inspects the indirect commands and decides whether or not to add that command to an unordered access view (UAV) describing which commands that should be executed.</span></span> <span data-ttu-id="155fd-120">在第二個模式中，只會執行所有命令。</span><span class="sxs-lookup"><span data-stu-id="155fd-120">In the second mode, all commands are simply executed.</span></span> <span data-ttu-id="155fd-121">按空格鍵會在模式之間切換。</span><span class="sxs-lookup"><span data-stu-id="155fd-121">Pressing the spacebar will toggle between modes.</span></span>

## <a name="define-the-indirect-commands"></a><span data-ttu-id="155fd-122">定義間接命令</span><span class="sxs-lookup"><span data-stu-id="155fd-122">Define the indirect commands</span></span>

<span data-ttu-id="155fd-123">我們一開始要先定義間接命令的外觀。</span><span class="sxs-lookup"><span data-stu-id="155fd-123">We start out by defining what the indirect commands should look like.</span></span> <span data-ttu-id="155fd-124">在此範例中，我們想要執行的命令如下：</span><span class="sxs-lookup"><span data-stu-id="155fd-124">In this sample the commands we want to execute are to:</span></span>

<dl> 1. <span data-ttu-id="155fd-125"> (CBV) 更新常數緩衝區視圖。</span><span class="sxs-lookup"><span data-stu-id="155fd-125">Update the constant buffer view (CBV).</span></span>  
2. <span data-ttu-id="155fd-126">繪製三角形。</span><span class="sxs-lookup"><span data-stu-id="155fd-126">Draw the triangle.</span></span>  
</dl>

<span data-ttu-id="155fd-127">這些繪製命令會以 **D3D12ExecuteIndirect** 類別定義中的下列結構表示。</span><span class="sxs-lookup"><span data-stu-id="155fd-127">These drawing commands are represented by the following structure in the **D3D12ExecuteIndirect** class definition.</span></span> <span data-ttu-id="155fd-128">命令會依照其在此結構中的定義順序循序執行。</span><span class="sxs-lookup"><span data-stu-id="155fd-128">Commands are executed sequentially in the order they are defined in this structure.</span></span>

``` syntax
  
// Data structure to match the command signature used for ExecuteIndirect.
struct IndirectCommand
{
       D3D12_GPU_VIRTUAL_ADDRESS cbv;
       D3D12_DRAW_ARGUMENTS drawArguments;
};
```



| <span data-ttu-id="155fd-129">呼叫流程</span><span class="sxs-lookup"><span data-stu-id="155fd-129">Call flow</span></span>                                              | <span data-ttu-id="155fd-130">參數</span><span class="sxs-lookup"><span data-stu-id="155fd-130">Parameters</span></span> |
|--------------------------------------------------------|------------|
| <span data-ttu-id="155fd-131">D3D12 \_ GPU \_ 虛擬 \_ 位址 (單純的 UINT64) </span><span class="sxs-lookup"><span data-stu-id="155fd-131">D3D12\_GPU\_VIRTUAL\_ADDRESS (simply a UINT64)</span></span>         |            |
| [<span data-ttu-id="155fd-132">**D3D12 \_ DRAW \_ 引數**</span><span class="sxs-lookup"><span data-stu-id="155fd-132">**D3D12\_DRAW\_ARGUMENTS**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_draw_arguments) |            |



 

<span data-ttu-id="155fd-133">為了伴隨資料結構，也會建立命令簽章，以指示 GPU 如何解讀傳遞給 [**ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) API 的資料。</span><span class="sxs-lookup"><span data-stu-id="155fd-133">To accompany the data structure, a command signature is also created which instructs the GPU how to interpret the data passed in to the [**ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) API.</span></span> <span data-ttu-id="155fd-134">這個程式碼和大部分的程式碼都會加入至 **LoadAssets** 方法。</span><span class="sxs-lookup"><span data-stu-id="155fd-134">This, and the most of the following code, is added to the **LoadAssets** method.</span></span>

``` syntax
// Create the command signature used for indirect drawing.
{
       // Each command consists of a CBV update and a DrawInstanced call.
       D3D12_INDIRECT_ARGUMENT_DESC argumentDescs[2] = {};
       argumentDescs[0].Type = D3D12_INDIRECT_ARGUMENT_TYPE_CONSTANT_BUFFER_VIEW;
       argumentDescs[0].ConstantBufferView.RootParameterIndex = Cbv;
       argumentDescs[1].Type = D3D12_INDIRECT_ARGUMENT_TYPE_DRAW;

       D3D12_COMMAND_SIGNATURE_DESC commandSignatureDesc = {};
       commandSignatureDesc.pArgumentDescs = argumentDescs;
       commandSignatureDesc.NumArgumentDescs = _countof(argumentDescs);
       commandSignatureDesc.ByteStride = sizeof(IndirectCommand);

       ThrowIfFailed(m_device->CreateCommandSignature(&commandSignatureDesc, m_rootSignature.Get(), IID_PPV_ARGS(&m_commandSignature)));
}
```



| <span data-ttu-id="155fd-135">呼叫流程</span><span class="sxs-lookup"><span data-stu-id="155fd-135">Call flow</span></span>                                                               | <span data-ttu-id="155fd-136">參數</span><span class="sxs-lookup"><span data-stu-id="155fd-136">Parameters</span></span>                                                              |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="155fd-137">**D3D12 \_ 間接 \_ 引數 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="155fd-137">**D3D12\_INDIRECT\_ARGUMENT\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_indirect_argument_desc) | [<span data-ttu-id="155fd-138">**D3D12 \_ 間接 \_ 引數 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="155fd-138">**D3D12\_INDIRECT\_ARGUMENT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_indirect_argument_type) |
| [<span data-ttu-id="155fd-139">**D3D12 \_ 命令 \_ 簽名 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="155fd-139">**D3D12\_COMMAND\_SIGNATURE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_command_signature_desc) |                                                                         |
| [<span data-ttu-id="155fd-140">**CreateCommandSignature**</span><span class="sxs-lookup"><span data-stu-id="155fd-140">**CreateCommandSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandsignature)   |                                                                         |



 

## <a name="create-a-graphics-and-compute-root-signature"></a><span data-ttu-id="155fd-141">建立圖形並計算根簽章</span><span class="sxs-lookup"><span data-stu-id="155fd-141">Create a graphics and compute root signature</span></span>

<span data-ttu-id="155fd-142">我們也會同時建立圖形和計算根簽章。</span><span class="sxs-lookup"><span data-stu-id="155fd-142">We also create both a graphics and a compute root signature.</span></span> <span data-ttu-id="155fd-143">圖形根簽章只會定義根 CBV。</span><span class="sxs-lookup"><span data-stu-id="155fd-143">The graphics root signature just defines a root CBV.</span></span> <span data-ttu-id="155fd-144">請注意，我們會在定義命令簽章時，將這個根參數的索引對應至 [**D3D12 \_ 間接 \_ 引數 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_indirect_argument_desc) (所示的) 。</span><span class="sxs-lookup"><span data-stu-id="155fd-144">Note that we map the index of this root parameter in the [**D3D12\_INDIRECT\_ARGUMENT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_indirect_argument_desc) (shown above) when the command signature is defined.</span></span> <span data-ttu-id="155fd-145">計算根簽章定義：</span><span class="sxs-lookup"><span data-stu-id="155fd-145">The compute root signature defines:</span></span>

-   <span data-ttu-id="155fd-146">具有三個插槽的通用描述中繼資料表 (兩個 SRV 和一個 UAV) ：</span><span class="sxs-lookup"><span data-stu-id="155fd-146">A common descriptor table with three slots (two SRV’s and one UAV):</span></span>
    -   <span data-ttu-id="155fd-147">一個 SRV 會將常數緩衝區公開給計算著色器</span><span class="sxs-lookup"><span data-stu-id="155fd-147">One SRV exposes the constant buffers to the compute shader</span></span>
    -   <span data-ttu-id="155fd-148">一個 SRV 將命令緩衝區公開給計算著色器</span><span class="sxs-lookup"><span data-stu-id="155fd-148">One SRV exposes the command buffer to the compute shader</span></span>
    -   <span data-ttu-id="155fd-149">UAV 是計算著色器儲存可見三角形命令的位置</span><span class="sxs-lookup"><span data-stu-id="155fd-149">The UAV is where the compute shader saves the commands for the visible triangles</span></span>
-   <span data-ttu-id="155fd-150">四個根常數：</span><span class="sxs-lookup"><span data-stu-id="155fd-150">Four root constants:</span></span>
    -   <span data-ttu-id="155fd-151">三角形一端的一半寬度</span><span class="sxs-lookup"><span data-stu-id="155fd-151">Half the width of one side of the triangle</span></span>
    -   <span data-ttu-id="155fd-152">三角形頂點的 z 位置</span><span class="sxs-lookup"><span data-stu-id="155fd-152">The z position of the triangle vertices</span></span>
    -   <span data-ttu-id="155fd-153">同質空間中的剔除平面 +/-x 位移 \[ -1，1\]</span><span class="sxs-lookup"><span data-stu-id="155fd-153">The +/- x offset of the culling plane in homogenous space \[-1,1\]</span></span>
    -   <span data-ttu-id="155fd-154">命令緩衝區中的間接命令數目</span><span class="sxs-lookup"><span data-stu-id="155fd-154">The number of indirect commands in the command buffer</span></span>

``` syntax
// Create the root signatures.
{
       CD3DX12_ROOT_PARAMETER rootParameters[GraphicsRootParametersCount];
       rootParameters[Cbv].InitAsConstantBufferView(0, 0, D3D12_SHADER_VISIBILITY_VERTEX);

       CD3DX12_ROOT_SIGNATURE_DESC rootSignatureDesc;
       rootSignatureDesc.Init(_countof(rootParameters), rootParameters, 0, nullptr, D3D12_ROOT_SIGNATURE_FLAG_ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT);

       ComPtr<ID3DBlob> signature;
       ComPtr<ID3DBlob> error;
       ThrowIfFailed(D3D12SerializeRootSignature(&rootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));
       ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_rootSignature)));

       // Create compute signature.
       CD3DX12_DESCRIPTOR_RANGE ranges[2];
       ranges[0].Init(D3D12_DESCRIPTOR_RANGE_TYPE_SRV, 2, 0);
       ranges[1].Init(D3D12_DESCRIPTOR_RANGE_TYPE_UAV, 1, 0);

       CD3DX12_ROOT_PARAMETER computeRootParameters[ComputeRootParametersCount];
       computeRootParameters[SrvUavTable].InitAsDescriptorTable(2, ranges);
       computeRootParameters[RootConstants].InitAsConstants(4, 0);

       CD3DX12_ROOT_SIGNATURE_DESC computeRootSignatureDesc;
       computeRootSignatureDesc.Init(_countof(computeRootParameters), computeRootParameters);

       ThrowIfFailed(D3D12SerializeRootSignature(&computeRootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));
       ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_computeRootSignature)));
}
```



| <span data-ttu-id="155fd-155">呼叫流程</span><span class="sxs-lookup"><span data-stu-id="155fd-155">Call flow</span></span>                                                             | <span data-ttu-id="155fd-156">參數</span><span class="sxs-lookup"><span data-stu-id="155fd-156">Parameters</span></span>                                                            |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="155fd-157">**CD3DX12 \_ 根 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="155fd-157">**CD3DX12\_ROOT\_PARAMETER**</span></span>](cd3dx12-root-parameter.md)            | [<span data-ttu-id="155fd-158">**D3D12 \_ 著色器 \_ 可見度**</span><span class="sxs-lookup"><span data-stu-id="155fd-158">**D3D12\_SHADER\_VISIBILITY**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)          |
| [<span data-ttu-id="155fd-159">**CD3DX12 \_ 根目錄 \_ 簽名 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="155fd-159">**CD3DX12\_ROOT\_SIGNATURE\_DESC**</span></span>](cd3dx12-root-signature-desc.md) | [<span data-ttu-id="155fd-160">**D3D12 \_ 根簽章 \_ \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="155fd-160">**D3D12\_ROOT\_SIGNATURE\_FLAGS**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags)   |
| <span data-ttu-id="155fd-161">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="155fd-161">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span></span>                                   |                                                                       |
| [<span data-ttu-id="155fd-162">**D3D12SerializeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="155fd-162">**D3D12SerializeRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [<span data-ttu-id="155fd-163">**D3D \_ 根簽章 \_ \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="155fd-163">**D3D\_ROOT\_SIGNATURE\_VERSION**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [<span data-ttu-id="155fd-164">**CreateRootSignature**</span><span class="sxs-lookup"><span data-stu-id="155fd-164">**CreateRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |
| [<span data-ttu-id="155fd-165">**CD3DX12 \_ 描述元 \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="155fd-165">**CD3DX12\_DESCRIPTOR\_RANGE**</span></span>](cd3dx12-descriptor-range.md)        | [<span data-ttu-id="155fd-166">**D3D12 \_ 描述項 \_ 範圍 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="155fd-166">**D3D12\_DESCRIPTOR\_RANGE\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) |
| [<span data-ttu-id="155fd-167">**CD3DX12 \_ 根 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="155fd-167">**CD3DX12\_ROOT\_PARAMETER**</span></span>](cd3dx12-root-parameter.md)            | [<span data-ttu-id="155fd-168">**D3D12 \_ 著色器 \_ 可見度**</span><span class="sxs-lookup"><span data-stu-id="155fd-168">**D3D12\_SHADER\_VISIBILITY**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)          |
| [<span data-ttu-id="155fd-169">**CD3DX12 \_ 根目錄 \_ 簽名 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="155fd-169">**CD3DX12\_ROOT\_SIGNATURE\_DESC**</span></span>](cd3dx12-root-signature-desc.md) | [<span data-ttu-id="155fd-170">**D3D12 \_ 根簽章 \_ \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="155fd-170">**D3D12\_ROOT\_SIGNATURE\_FLAGS**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags)   |
| <span data-ttu-id="155fd-171">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="155fd-171">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span></span>                                   |                                                                       |
| [<span data-ttu-id="155fd-172">**D3D12SerializeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="155fd-172">**D3D12SerializeRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [<span data-ttu-id="155fd-173">**D3D \_ 根簽章 \_ \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="155fd-173">**D3D\_ROOT\_SIGNATURE\_VERSION**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [<span data-ttu-id="155fd-174">**CreateRootSignature**</span><span class="sxs-lookup"><span data-stu-id="155fd-174">**CreateRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |



 

## <a name="create-a-shader-resource-view-srv-for-the-compute-shader"></a><span data-ttu-id="155fd-175">建立計算著色器 (SRV) 的著色器資源檢視器</span><span class="sxs-lookup"><span data-stu-id="155fd-175">Create a shader resource view (SRV) for the compute shader</span></span>

<span data-ttu-id="155fd-176">建立管線狀態物件、頂點緩衝區、深度樣板和常數緩衝區之後，此範例會建立一個著色器資源檢視 (常數緩衝區的 SRV) ，讓計算著色器可以存取常數緩衝區中的資料。</span><span class="sxs-lookup"><span data-stu-id="155fd-176">After creating the pipeline state objects, vertex buffers, a depth stencil, and the constant buffers, the sample then creates a shader resource view (SRV) of the constant buffer so that the compute shader can access the data in the constant buffer.</span></span>

``` syntax
// Create shader resource views (SRV) of the constant buffers for the
// compute shader to read from.
       D3D12_SHADER_RESOURCE_VIEW_DESC srvDesc = {};
       srvDesc.Format = DXGI_FORMAT_UNKNOWN;
       srvDesc.ViewDimension = D3D12_SRV_DIMENSION_BUFFER;
       srvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
       srvDesc.Buffer.NumElements = TriangleCount;
       srvDesc.Buffer.StructureByteStride = sizeof(ConstantBufferData);
       srvDesc.Buffer.Flags = D3D12_BUFFER_SRV_FLAG_NONE;

       CD3DX12_CPU_DESCRIPTOR_HANDLE cbvSrvHandle(m_cbvSrvUavHeap->GetCPUDescriptorHandleForHeapStart(), CbvSrvOffset, m_cbvSrvUavDescriptorSize);
       for (UINT frame = 0; frame < FrameCount; frame++)
       {
              srvDesc.Buffer.FirstElement = frame * TriangleCount;
              m_device->CreateShaderResourceView(m_constantBuffer.Get(), &srvDesc, cbvSrvHandle);
              cbvSrvHandle.Offset(CbvSrvUavDescriptorCountPerFrame, m_cbvSrvUavDescriptorSize);
       }
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="155fd-177">呼叫流程</span><span class="sxs-lookup"><span data-stu-id="155fd-177">Call flow</span></span></th>
<th><span data-ttu-id="155fd-178">參數</span><span class="sxs-lookup"><span data-stu-id="155fd-178">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="155fd-179"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-179"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="155fd-180"><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-180"><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span></span><br /><span data-ttu-id="155fd-181">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-181">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a></span></span><br /><span data-ttu-id="155fd-182">
<a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a></span><span class="sxs-lookup"><span data-stu-id="155fd-182">
<a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="155fd-183"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-183"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span></span></td>
<td><span data-ttu-id="155fd-184"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-184"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="155fd-185"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>CreateShaderResourceView</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-185"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>CreateShaderResourceView</strong></a></span></span></td>

</tr>
</tbody>
</table>



 

## <a name="create-the-indirect-command-buffers"></a><span data-ttu-id="155fd-186">建立間接命令緩衝區</span><span class="sxs-lookup"><span data-stu-id="155fd-186">Create the indirect command buffers</span></span>

<span data-ttu-id="155fd-187">接著，我們會建立間接命令緩衝區，並使用下列程式碼定義其內容。</span><span class="sxs-lookup"><span data-stu-id="155fd-187">We then create the indirect command buffers and define their content using the following code.</span></span> <span data-ttu-id="155fd-188">我們繪製相同的三角形頂點1024次，但指向每個繪製呼叫的不同常數緩衝區位置。</span><span class="sxs-lookup"><span data-stu-id="155fd-188">We draw the same triangle vertices 1024 times, but point to a different constant buffer location with each draw call.</span></span>

``` syntax
       D3D12_GPU_VIRTUAL_ADDRESS gpuAddress = m_constantBuffer->GetGPUVirtualAddress();
       UINT commandIndex = 0;

       for (UINT frame = 0; frame < FrameCount; frame++)
       {
              for (UINT n = 0; n < TriangleCount; n++)
              {
                    commands[commandIndex].cbv = gpuAddress;
                    commands[commandIndex].drawArguments.VertexCountPerInstance = 3;
                    commands[commandIndex].drawArguments.InstanceCount = 1;
                    commands[commandIndex].drawArguments.StartVertexLocation = 0;
                    commands[commandIndex].drawArguments.StartInstanceLocation = 0;

                    commandIndex++;
                    gpuAddress += sizeof(ConstantBufferData);
              }
       }
```



| <span data-ttu-id="155fd-189">呼叫流程</span><span class="sxs-lookup"><span data-stu-id="155fd-189">Call flow</span></span>                    | <span data-ttu-id="155fd-190">參數</span><span class="sxs-lookup"><span data-stu-id="155fd-190">Parameters</span></span>                                                          |
|------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="155fd-191">D3D12 \_ GPU \_ 虛擬 \_ 位址</span><span class="sxs-lookup"><span data-stu-id="155fd-191">D3D12\_GPU\_VIRTUAL\_ADDRESS</span></span> | [<span data-ttu-id="155fd-192">**GetGPUVirtualAddress**</span><span class="sxs-lookup"><span data-stu-id="155fd-192">**GetGPUVirtualAddress**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress) |



 

<span data-ttu-id="155fd-193">將命令緩衝區上傳到 GPU 之後，我們也會建立其 SRV 以供計算著色器讀取。</span><span class="sxs-lookup"><span data-stu-id="155fd-193">After uploading the command buffers to the GPU, we also create an SRV of them for the compute shader to read from.</span></span> <span data-ttu-id="155fd-194">這非常類似于常數緩衝區建立的 SRV。</span><span class="sxs-lookup"><span data-stu-id="155fd-194">This is very similar to the SRV created of the constant buffer.</span></span>

``` syntax
// Create SRVs for the command buffers.
       D3D12_SHADER_RESOURCE_VIEW_DESC srvDesc = {};
       srvDesc.Format = DXGI_FORMAT_UNKNOWN;
       srvDesc.ViewDimension = D3D12_SRV_DIMENSION_BUFFER;
       srvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
       srvDesc.Buffer.NumElements = TriangleCount;
       srvDesc.Buffer.StructureByteStride = sizeof(IndirectCommand);
       srvDesc.Buffer.Flags = D3D12_BUFFER_SRV_FLAG_NONE;

       CD3DX12_CPU_DESCRIPTOR_HANDLE commandsHandle(m_cbvSrvUavHeap->GetCPUDescriptorHandleForHeapStart(), CommandsOffset, m_cbvSrvUavDescriptorSize);
       for (UINT frame = 0; frame < FrameCount; frame++)
       {
              srvDesc.Buffer.FirstElement = frame * TriangleCount;
              m_device->CreateShaderResourceView(m_commandBuffer.Get(), &srvDesc, commandsHandle);
              commandsHandle.Offset(CbvSrvUavDescriptorCountPerFrame, m_cbvSrvUavDescriptorSize);
       }
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="155fd-195">呼叫流程</span><span class="sxs-lookup"><span data-stu-id="155fd-195">Call flow</span></span></th>
<th><span data-ttu-id="155fd-196">參數</span><span class="sxs-lookup"><span data-stu-id="155fd-196">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="155fd-197"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-197"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="155fd-198"><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-198"><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span></span><br /><span data-ttu-id="155fd-199">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-199">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a></span></span><br /><span data-ttu-id="155fd-200">
<a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a></span><span class="sxs-lookup"><span data-stu-id="155fd-200">
<a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a></span></span><br /><span data-ttu-id="155fd-201">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_srv_flags"><strong>D3D12_BUFFER_SRV_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-201">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_srv_flags"><strong>D3D12_BUFFER_SRV_FLAG</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="155fd-202"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-202"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span></span></td>
<td><span data-ttu-id="155fd-203"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-203"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="155fd-204"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>CreateShaderResourceView</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-204"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>CreateShaderResourceView</strong></a></span></span></td>

</tr>
</tbody>
</table>



 

## <a name="create-the-compute-uavs"></a><span data-ttu-id="155fd-205">建立計算 UAVs</span><span class="sxs-lookup"><span data-stu-id="155fd-205">Create the compute UAVs</span></span>

<span data-ttu-id="155fd-206">我們需要建立 UAVs 來儲存計算工作的結果。</span><span class="sxs-lookup"><span data-stu-id="155fd-206">We need to create the UAVs that will store the results of the compute work.</span></span> <span data-ttu-id="155fd-207">當轉譯目標可看到三角形的計算著色器時，它會附加至這個 UAV，然後由 [**ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) API 取用。</span><span class="sxs-lookup"><span data-stu-id="155fd-207">When a triangle is deemed by the compute shader to be visible to the render target, it will be appended to this UAV and then consumed by the [**ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) API.</span></span>

``` syntax
CD3DX12_CPU_DESCRIPTOR_HANDLE processedCommandsHandle(m_cbvSrvUavHeap->GetCPUDescriptorHandleForHeapStart(), ProcessedCommandsOffset, m_cbvSrvUavDescriptorSize);
for (UINT frame = 0; frame < FrameCount; frame++)
{
       // Allocate a buffer large enough to hold all of the indirect commands
       // for a single frame as well as a UAV counter.
       commandBufferDesc = CD3DX12_RESOURCE_DESC::Buffer(CommandBufferSizePerFrame + sizeof(UINT), D3D12_RESOURCE_FLAG_ALLOW_UNORDERED_ACCESS);
       CD3DX12_HEAP_PROPERTIES heapProps(D3D12_HEAP_TYPE_DEFAULT);
       ThrowIfFailed(m_device->CreateCommittedResource(
             &heapProps,
             D3D12_HEAP_FLAG_NONE,
             &commandBufferDesc,
             D3D12_RESOURCE_STATE_COPY_DEST,
             nullptr,
             IID_PPV_ARGS(&m_processedCommandBuffers[frame])));

       D3D12_UNORDERED_ACCESS_VIEW_DESC uavDesc = {};
       uavDesc.Format = DXGI_FORMAT_UNKNOWN;
       uavDesc.ViewDimension = D3D12_UAV_DIMENSION_BUFFER;
       uavDesc.Buffer.FirstElement = 0;
       uavDesc.Buffer.NumElements = TriangleCount;
       uavDesc.Buffer.StructureByteStride = sizeof(IndirectCommand);
       uavDesc.Buffer.CounterOffsetInBytes = CommandBufferSizePerFrame;
       uavDesc.Buffer.Flags = D3D12_BUFFER_UAV_FLAG_NONE;

       m_device->CreateUnorderedAccessView(
             m_processedCommandBuffers[frame].Get(),
             m_processedCommandBuffers[frame].Get(),
             &uavDesc,
             processedCommandsHandle);

       processedCommandsHandle.Offset(CbvSrvUavDescriptorCountPerFrame, m_cbvSrvUavDescriptorSize);
}
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="155fd-208">呼叫流程</span><span class="sxs-lookup"><span data-stu-id="155fd-208">Call flow</span></span></th>
<th><span data-ttu-id="155fd-209">參數</span><span class="sxs-lookup"><span data-stu-id="155fd-209">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="155fd-210"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-210"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span></span></td>
<td><span data-ttu-id="155fd-211"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-211"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="155fd-212"><a href="cd3dx12-resource-desc.md"><strong>CD3DX12_RESOURCE_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-212"><a href="cd3dx12-resource-desc.md"><strong>CD3DX12_RESOURCE_DESC</strong></a></span></span></td>
<td><span data-ttu-id="155fd-213"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags"><strong>D3D12_RESOURCE_FLAGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-213"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags"><strong>D3D12_RESOURCE_FLAGS</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="155fd-214"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-214"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span></span></td>
<td><dl><span data-ttu-id="155fd-215"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-215"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span></span><br /><span data-ttu-id="155fd-216">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-216">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span></span><br /><span data-ttu-id="155fd-217">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-217">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a></span></span><br /><span data-ttu-id="155fd-218">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-218">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="155fd-219"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_unordered_access_view_desc"><strong>D3D12_UNORDERED_ACCESS_VIEW_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-219"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_unordered_access_view_desc"><strong>D3D12_UNORDERED_ACCESS_VIEW_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="155fd-220"><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-220"><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span></span><br /><span data-ttu-id="155fd-221">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_uav_dimension"><strong>D3D12_UAV_DIMENSION</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-221">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_uav_dimension"><strong>D3D12_UAV_DIMENSION</strong></a></span></span><br /><span data-ttu-id="155fd-222">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags"><strong>D3D12_BUFFER_UAV_FLAGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-222">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags"><strong>D3D12_BUFFER_UAV_FLAGS</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="155fd-223"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview"><strong>CreateUnorderedAccessView</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-223"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview"><strong>CreateUnorderedAccessView</strong></a></span></span></td>

</tr>
</tbody>
</table>



 

## <a name="drawing-the-frame"></a><span data-ttu-id="155fd-224">繪製框架</span><span class="sxs-lookup"><span data-stu-id="155fd-224">Drawing the frame</span></span>

<span data-ttu-id="155fd-225">當繪製框架時，如果我們處於正在叫用計算著色器的模式中，而且 GPU 正在處理間接命令，我們會先 [**分派**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch) 該工作來填入 [**ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect)的命令緩衝區。</span><span class="sxs-lookup"><span data-stu-id="155fd-225">When it comes time to draw the frame, if we are in the mode when the compute shader is being invoked and indirect commands are being processed by the GPU, we will first [**Dispatch**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch) that work to populate our command buffer for [**ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect).</span></span> <span data-ttu-id="155fd-226">下列程式碼片段會新增至 **PopulateCommandLists** 方法。</span><span class="sxs-lookup"><span data-stu-id="155fd-226">The following code snippets are added to the **PopulateCommandLists** method.</span></span>

``` syntax
// Record the compute commands that will cull triangles and prevent them from being processed by the vertex shader.
if (m_enableCulling)
{
       UINT frameDescriptorOffset = m_frameIndex * CbvSrvUavDescriptorCountPerFrame;
       D3D12_GPU_DESCRIPTOR_HANDLE cbvSrvUavHandle = m_cbvSrvUavHeap->GetGPUDescriptorHandleForHeapStart();

       m_computeCommandList->SetComputeRootSignature(m_computeRootSignature.Get());

       ID3D12DescriptorHeap* ppHeaps[] = { m_cbvSrvUavHeap.Get() };
       m_computeCommandList->SetDescriptorHeaps(_countof(ppHeaps), ppHeaps);

       m_computeCommandList->SetComputeRootDescriptorTable(
              SrvUavTable,
              CD3DX12_GPU_DESCRIPTOR_HANDLE(cbvSrvUavHandle, CbvSrvOffset + frameDescriptorOffset, m_cbvSrvUavDescriptorSize));

       m_computeCommandList->SetComputeRoot32BitConstants(RootConstants, 4, reinterpret_cast<void*>(&m_csRootConstants), 0);

       // Reset the UAV counter for this frame.
       m_computeCommandList->CopyBufferRegion(m_processedCommandBuffers[m_frameIndex].Get(), CommandBufferSizePerFrame, m_processedCommandBufferCounterReset.Get(), 0, sizeof(UINT));

       D3D12_RESOURCE_BARRIER barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_processedCommandBuffers[m_frameIndex].Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_UNORDERED_ACCESS);
       m_computeCommandList->ResourceBarrier(1, &barrier);

       m_computeCommandList->Dispatch(static_cast<UINT>(ceil(TriangleCount / float(ComputeThreadBlockSize))), 1, 1);
}

ThrowIfFailed(m_computeCommandList->Close());
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="155fd-227">呼叫流程</span><span class="sxs-lookup"><span data-stu-id="155fd-227">Call flow</span></span></th>
<th><span data-ttu-id="155fd-228">參數</span><span class="sxs-lookup"><span data-stu-id="155fd-228">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="155fd-229"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle"><strong>D3D12_GPU_DESCRIPTOR_HANDLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-229"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle"><strong>D3D12_GPU_DESCRIPTOR_HANDLE</strong></a></span></span></td>
<td><span data-ttu-id="155fd-230"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart"><strong>GetGPUDescriptorHandleForHeapStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-230"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart"><strong>GetGPUDescriptorHandleForHeapStart</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="155fd-231"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature"><strong>SetComputeRootSignature</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-231"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature"><strong>SetComputeRootSignature</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="155fd-232"><a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap"><strong>ID3D12DescriptorHeap</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-232"><a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap"><strong>ID3D12DescriptorHeap</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="155fd-233"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps"><strong>SetDescriptorHeaps</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-233"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps"><strong>SetDescriptorHeaps</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="155fd-234"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable"><strong>SetComputeRootDescriptorTable</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-234"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable"><strong>SetComputeRootDescriptorTable</strong></a></span></span></td>
<td><span data-ttu-id="155fd-235"><a href="cd3dx12-gpu-descriptor-handle.md"><strong>CD3DX12_GPU_DESCRIPTOR_HANDLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-235"><a href="cd3dx12-gpu-descriptor-handle.md"><strong>CD3DX12_GPU_DESCRIPTOR_HANDLE</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="155fd-236"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants"><strong>SetComputeRoot32BitConstants</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-236"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants"><strong>SetComputeRoot32BitConstants</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="155fd-237"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion"><strong>CopyBufferRegion</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-237"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion"><strong>CopyBufferRegion</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="155fd-238"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier"><strong>D3D12_RESOURCE_BARRIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-238"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier"><strong>D3D12_RESOURCE_BARRIER</strong></a></span></span></td>
<td><dl><span data-ttu-id="155fd-239"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-239"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span></span><br /><span data-ttu-id="155fd-240">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-240">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="155fd-241"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-241"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="155fd-242"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch"><strong>分派</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-242"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch"><strong>Dispatch</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="155fd-243"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close"><strong>關閉</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-243"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close"><strong>Close</strong></a></span></span></td>

</tr>
</tbody>
</table>



 

<span data-ttu-id="155fd-244">接著，我們會在已啟用 UAV (GPU 剔除) 或完整命令緩衝區 (已停用的 GPU 剔除) 中執行命令。</span><span class="sxs-lookup"><span data-stu-id="155fd-244">Then we will execute the commands in either the UAV (GPU culling enabled) or the full command buffer (GPU culling disabled).</span></span>

``` syntax
// Record the rendering commands.
{
       // Set necessary state.
       m_commandList->SetGraphicsRootSignature(m_rootSignature.Get());

       ID3D12DescriptorHeap* ppHeaps[] = { m_cbvSrvUavHeap.Get() };
       m_commandList->SetDescriptorHeaps(_countof(ppHeaps), ppHeaps);

       m_commandList->RSSetViewports(1, &m_viewport);
       m_commandList->RSSetScissorRects(1, m_enableCulling ? &m_cullingScissorRect : &m_scissorRect);

       // Indicate that the command buffer will be used for indirect drawing
       // and that the back buffer will be used as a render target.
       D3D12_RESOURCE_BARRIER barriers[2] = {
              CD3DX12_RESOURCE_BARRIER::Transition(
                    m_enableCulling ? m_processedCommandBuffers[m_frameIndex].Get() : m_commandBuffer.Get(),
                    m_enableCulling ? D3D12_RESOURCE_STATE_UNORDERED_ACCESS : D3D12_RESOURCE_STATE_NON_PIXEL_SHADER_RESOURCE,
                    D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT),
              CD3DX12_RESOURCE_BARRIER::Transition(
                    m_renderTargets[m_frameIndex].Get(),
                    D3D12_RESOURCE_STATE_PRESENT,
                    D3D12_RESOURCE_STATE_RENDER_TARGET)
       };

       m_commandList->ResourceBarrier(_countof(barriers), barriers);

       CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
       CD3DX12_CPU_DESCRIPTOR_HANDLE dsvHandle(m_dsvHeap->GetCPUDescriptorHandleForHeapStart());
       m_commandList->OMSetRenderTargets(1, &rtvHandle, FALSE, &dsvHandle);

       // Record commands.
       const float clearColor[] = { 0.0f, 0.2f, 0.4f, 1.0f };
       m_commandList->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
       m_commandList->ClearDepthStencilView(dsvHandle, D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

       m_commandList->IASetPrimitiveTopology(D3D_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP);
       m_commandList->IASetVertexBuffers(0, 1, &m_vertexBufferView);

       if (m_enableCulling)
       {
              // Draw the triangles that have not been culled.
              m_commandList->ExecuteIndirect(
                    m_commandSignature.Get(),
                    TriangleCount,
                    m_processedCommandBuffers[m_frameIndex].Get(),
                    0,
                    m_processedCommandBuffers[m_frameIndex].Get(),
                    CommandBufferSizePerFrame);
       }
       else
       {
              // Draw all of the triangles.
              m_commandList->ExecuteIndirect(
                    m_commandSignature.Get(),
                    TriangleCount,
                    m_commandBuffer.Get(),
                    CommandBufferSizePerFrame * m_frameIndex,
                    nullptr,
                    0);
       }

       // Indicate that the command buffer may be used by the compute shader
       // and that the back buffer will now be used to present.
       barriers[0].Transition.StateBefore = D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT;
       barriers[0].Transition.StateAfter = m_enableCulling ? D3D12_RESOURCE_STATE_COPY_DEST : D3D12_RESOURCE_STATE_NON_PIXEL_SHADER_RESOURCE;
       barriers[1].Transition.StateBefore = D3D12_RESOURCE_STATE_RENDER_TARGET;
       barriers[1].Transition.StateAfter = D3D12_RESOURCE_STATE_PRESENT;

       m_commandList->ResourceBarrier(_countof(barriers), barriers);

       ThrowIfFailed(m_commandList->Close());
}
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="155fd-245">呼叫流程</span><span class="sxs-lookup"><span data-stu-id="155fd-245">Call flow</span></span></th>
<th><span data-ttu-id="155fd-246">參數</span><span class="sxs-lookup"><span data-stu-id="155fd-246">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="155fd-247"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature"><strong>SetGraphicsRootSignature</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-247"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature"><strong>SetGraphicsRootSignature</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="155fd-248"><a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap"><strong>ID3D12DescriptorHeap</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-248"><a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap"><strong>ID3D12DescriptorHeap</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="155fd-249"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps"><strong>SetDescriptorHeaps</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-249"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps"><strong>SetDescriptorHeaps</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="155fd-250"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports"><strong>RSSetViewports</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-250"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports"><strong>RSSetViewports</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="155fd-251"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects"><strong>RSSetScissorRects</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-251"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects"><strong>RSSetScissorRects</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="155fd-252"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier"><strong>D3D12_RESOURCE_BARRIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-252"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier"><strong>D3D12_RESOURCE_BARRIER</strong></a></span></span></td>
<td><dl><span data-ttu-id="155fd-253"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-253"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span></span><br /><span data-ttu-id="155fd-254">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-254">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="155fd-255"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-255"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="155fd-256"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-256"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span></span></td>
<td><span data-ttu-id="155fd-257"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-257"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="155fd-258"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets"><strong>OMSetRenderTargets</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-258"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets"><strong>OMSetRenderTargets</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="155fd-259"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview"><strong>ClearRenderTargetView</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-259"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview"><strong>ClearRenderTargetView</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="155fd-260"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview"><strong>ClearDepthStencilView</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-260"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview"><strong>ClearDepthStencilView</strong></a></span></span></td>
<td><span data-ttu-id="155fd-261"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_clear_flags"><strong>D3D12_CLEAR_FLAGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-261"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_clear_flags"><strong>D3D12_CLEAR_FLAGS</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="155fd-262"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology"><strong>IASetPrimitiveTopology</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-262"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology"><strong>IASetPrimitiveTopology</strong></a></span></span></td>
<td><span data-ttu-id="155fd-263"><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology"><strong>D3D_PRIMITIVE_TOPOLOGY</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-263"><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology"><strong>D3D_PRIMITIVE_TOPOLOGY</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="155fd-264"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers"><strong>IASetVertexBuffers</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-264"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers"><strong>IASetVertexBuffers</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="155fd-265"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect"><strong>ExecuteIndirect</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-265"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect"><strong>ExecuteIndirect</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="155fd-266"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-266"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span></span></td>
<td><span data-ttu-id="155fd-267"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-267"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="155fd-268"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close"><strong>關閉</strong></a></span><span class="sxs-lookup"><span data-stu-id="155fd-268"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close"><strong>Close</strong></a></span></span></td>

</tr>
</tbody>
</table>



 

<span data-ttu-id="155fd-269">如果我們使用 GPU 剔除模式，則會讓圖形命令佇列等待計算工作完成，再開始執行間接命令。</span><span class="sxs-lookup"><span data-stu-id="155fd-269">If we are in GPU culling mode, we will have the graphics command queue wait for the compute work to complete before it begins executing the indirect commands.</span></span> <span data-ttu-id="155fd-270">在 **OnRender** 方法中，會新增下列程式碼片段。</span><span class="sxs-lookup"><span data-stu-id="155fd-270">In the **OnRender** method the following snippet is added.</span></span>

``` syntax
// Execute the compute work.
if (m_enableCulling)
{
       ID3D12CommandList* ppCommandLists[] = { m_computeCommandList.Get() };
       m_computeCommandQueue->ExecuteCommandLists(_countof(ppCommandLists), ppCommandLists);
       m_computeCommandQueue->Signal(m_computeFence.Get(), m_fenceValues[m_frameIndex]);

       // Execute the rendering work only when the compute work is complete.
       m_commandQueue->Wait(m_computeFence.Get(), m_fenceValues[m_frameIndex]);
}

// Execute the rendering work.
ID3D12CommandList* ppCommandLists[] = { m_commandList.Get() };
m_commandQueue->ExecuteCommandLists(_countof(ppCommandLists), ppCommandLists);
```



| <span data-ttu-id="155fd-271">呼叫流程</span><span class="sxs-lookup"><span data-stu-id="155fd-271">Call flow</span></span>                                                             | <span data-ttu-id="155fd-272">參數</span><span class="sxs-lookup"><span data-stu-id="155fd-272">Parameters</span></span> |
|-----------------------------------------------------------------------|------------|
| [<span data-ttu-id="155fd-273">**ID3D12CommandList**</span><span class="sxs-lookup"><span data-stu-id="155fd-273">**ID3D12CommandList**</span></span>](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist)                        |            |
| [<span data-ttu-id="155fd-274">**ExecuteCommandLists**</span><span class="sxs-lookup"><span data-stu-id="155fd-274">**ExecuteCommandLists**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) |            |
| [<span data-ttu-id="155fd-275">**信號**</span><span class="sxs-lookup"><span data-stu-id="155fd-275">**Signal**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-signal)                           |            |
| [<span data-ttu-id="155fd-276">**等候**</span><span class="sxs-lookup"><span data-stu-id="155fd-276">**Wait**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-wait)                               |            |
| [<span data-ttu-id="155fd-277">**ID3D12CommandList**</span><span class="sxs-lookup"><span data-stu-id="155fd-277">**ID3D12CommandList**</span></span>](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist)                        |            |
| [<span data-ttu-id="155fd-278">**ExecuteCommandLists**</span><span class="sxs-lookup"><span data-stu-id="155fd-278">**ExecuteCommandLists**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) |            |



 

## <a name="run-the-sample"></a><span data-ttu-id="155fd-279">執行範例</span><span class="sxs-lookup"><span data-stu-id="155fd-279">Run the sample</span></span>

<span data-ttu-id="155fd-280">具有 GPU 基本物件的範例會進行挑選。</span><span class="sxs-lookup"><span data-stu-id="155fd-280">The sample with GPU primitive culling.</span></span>

![使用 gpu 剔除的 exectue 間接範例螢幕擷取畫面](images/executeindirect-withculling.png)

<span data-ttu-id="155fd-282">沒有 GPU 基本的範例會進行剔除。</span><span class="sxs-lookup"><span data-stu-id="155fd-282">The sample without GPU primitive culling.</span></span>

![沒有 gpu 剔除的 exectue 間接範例螢幕擷取畫面](images/executeindirect-withoutculling.png)

## <a name="related-topics"></a><span data-ttu-id="155fd-284">相關主題</span><span class="sxs-lookup"><span data-stu-id="155fd-284">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="155fd-285">D3D12 程式碼逐步解說-解說</span><span class="sxs-lookup"><span data-stu-id="155fd-285">D3D12 Code Walk-Throughs</span></span>](d3d12-code-walk-throughs.md)
</dt> <dt>

[<span data-ttu-id="155fd-286">DirectX advanced learning 影片教學課程：執行間接和非同步 GPU 剔除</span><span class="sxs-lookup"><span data-stu-id="155fd-286">DirectX advanced learning video tutorials : Execute Indirect and Async GPU culling</span></span>](https://www.youtube.com/watch?v=fKD-VKJeeds)
</dt> <dt>

[<span data-ttu-id="155fd-287">間接繪圖</span><span class="sxs-lookup"><span data-stu-id="155fd-287">Indirect Drawing</span></span>](indirect-drawing.md)
</dt> </dl>

 

 

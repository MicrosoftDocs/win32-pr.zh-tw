---
title: 間接繪圖和 GPU 剔除
description: D3D12ExecuteIndirect 範例會示範如何使用間接命令來繪製內容。 它也會示範如何在發行之前，在計算著色器中的 GPU 上操作這些命令。
ms.assetid: 09F90837-D6BF-498E-8018-5C28EDD9BDC3
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1eaab70be1f376856991156fe520919256e8f811c32ead4a5ce937fb4abc185
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119280132"
---
# <a name="indirect-drawing-and-gpu-culling"></a>間接繪圖和 GPU 剔除

D3D12ExecuteIndirect 範例會示範如何使用間接命令來繪製內容。 它也會示範如何在發行之前，在計算著色器中的 GPU 上操作這些命令。

-   [定義間接命令](#define-the-indirect-commands)
-   [建立圖形並計算根簽章](#create-a-graphics-and-compute-root-signature)
-   [建立計算著色器 (SRV) 的著色器資源檢視器](#create-a-shader-resource-view-srv-for-the-compute-shader)
-   [建立間接命令緩衝區](#create-the-indirect-command-buffers)
-   [建立計算 UAVs](#create-the-compute-uavs)
-   [繪製框架](#drawing-the-frame)
-   [執行範例](#run-the-sample)
-   [相關主題](#related-topics)

此範例會建立一個命令緩衝區來描述1024繪製呼叫。 每個繪製呼叫都會呈現具有隨機色彩、位置和速度的三角形。 三角形會在螢幕上無休止地建立動畫。 此範例中有兩種模式。 在第一個模式中，計算著色器會檢查間接命令，並決定是否要將該命令新增至未排序的存取視圖 (UAV) 描述應該執行的命令。 在第二個模式中，只會執行所有命令。 按空格鍵會在模式之間切換。

## <a name="define-the-indirect-commands"></a>定義間接命令

我們一開始要先定義間接命令的外觀。 在此範例中，我們想要執行的命令如下：

<dl> 1.  (CBV) 更新常數緩衝區視圖。  
2. 繪製三角形。  
</dl>

這些繪製命令會以 **D3D12ExecuteIndirect** 類別定義中的下列結構表示。 命令會依照其在此結構中的定義順序循序執行。

``` syntax
  
// Data structure to match the command signature used for ExecuteIndirect.
struct IndirectCommand
{
       D3D12_GPU_VIRTUAL_ADDRESS cbv;
       D3D12_DRAW_ARGUMENTS drawArguments;
};
```



| 呼叫流程                                              | 參數 |
|--------------------------------------------------------|------------|
| D3D12 \_ GPU \_ 虛擬 \_ 位址 (單純的 UINT64)          |            |
| [**D3D12 \_ DRAW \_ 引數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_draw_arguments) |            |



 

為了伴隨資料結構，也會建立命令簽章，以指示 GPU 如何解讀傳遞給 [**ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) API 的資料。 這個程式碼和大部分的程式碼都會加入至 **LoadAssets** 方法。

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



| 呼叫流程                                                               | 參數                                                              |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**D3D12 \_ 間接 \_ 引數 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_indirect_argument_desc) | [**D3D12 \_ 間接 \_ 引數 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_indirect_argument_type) |
| [**D3D12 \_ 命令 \_ 簽名 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_command_signature_desc) |                                                                         |
| [**CreateCommandSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandsignature)   |                                                                         |



 

## <a name="create-a-graphics-and-compute-root-signature"></a>建立圖形並計算根簽章

我們也會同時建立圖形和計算根簽章。 圖形根簽章只會定義根 CBV。 請注意，我們會在定義命令簽章時，將這個根參數的索引對應至 [**D3D12 \_ 間接 \_ 引數 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_indirect_argument_desc) (所示的) 。 計算根簽章定義：

-   具有三個插槽的通用描述中繼資料表 (兩個 SRV 和一個 UAV) ：
    -   一個 SRV 會將常數緩衝區公開給計算著色器
    -   一個 SRV 將命令緩衝區公開給計算著色器
    -   UAV 是計算著色器儲存可見三角形命令的位置
-   四個根常數：
    -   三角形一端的一半寬度
    -   三角形頂點的 z 位置
    -   同質空間中的剔除平面 +/-x 位移 \[ -1，1\]
    -   命令緩衝區中的間接命令數目

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



| 呼叫流程                                                             | 參數                                                            |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------|
| [**CD3DX12 \_ 根 \_ 參數**](cd3dx12-root-parameter.md)            | [**D3D12 \_ 著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)          |
| [**CD3DX12 \_ 根目錄 \_ 簽名 \_ DESC**](cd3dx12-root-signature-desc.md) | [**D3D12 \_ 根簽章 \_ \_ 旗標**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags)   |
| [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))                                   |                                                                       |
| [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [**D3D \_ 根簽章 \_ \_ 版本**](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [**CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |
| [**CD3DX12 \_ 描述元 \_ 範圍**](cd3dx12-descriptor-range.md)        | [**D3D12 \_ 描述項 \_ 範圍 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) |
| [**CD3DX12 \_ 根 \_ 參數**](cd3dx12-root-parameter.md)            | [**D3D12 \_ 著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)          |
| [**CD3DX12 \_ 根目錄 \_ 簽名 \_ DESC**](cd3dx12-root-signature-desc.md) | [**D3D12 \_ 根簽章 \_ \_ 旗標**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags)   |
| [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))                                   |                                                                       |
| [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [**D3D \_ 根簽章 \_ \_ 版本**](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [**CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |



 

## <a name="create-a-shader-resource-view-srv-for-the-compute-shader"></a>建立計算著色器 (SRV) 的著色器資源檢視器

建立管線狀態物件、頂點緩衝區、深度樣板和常數緩衝區之後，此範例會建立一個著色器資源檢視 (常數緩衝區的 SRV) ，讓計算著色器可以存取常數緩衝區中的資料。

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
<th>呼叫流程</th>
<th>參數</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></td>
<td><dl><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a><br />
<a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a><br />
</dl></td>
</tr>
<tr class="even">
<td><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>CreateShaderResourceView</strong></a></td>

</tr>
</tbody>
</table>



 

## <a name="create-the-indirect-command-buffers"></a>建立間接命令緩衝區

接著，我們會建立間接命令緩衝區，並使用下列程式碼定義其內容。 我們繪製相同的三角形頂點1024次，但指向每個繪製呼叫的不同常數緩衝區位置。

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



| 呼叫流程                    | 參數                                                          |
|------------------------------|---------------------------------------------------------------------|
| D3D12 \_ GPU \_ 虛擬 \_ 位址 | [**GetGPUVirtualAddress**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress) |



 

將命令緩衝區上傳到 GPU 之後，我們也會建立其 SRV 以供計算著色器讀取。 這非常類似于常數緩衝區建立的 SRV。

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
<th>呼叫流程</th>
<th>參數</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></td>
<td><dl><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a><br />
<a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_srv_flags"><strong>D3D12_BUFFER_SRV_FLAG</strong></a><br />
</dl></td>
</tr>
<tr class="even">
<td><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>CreateShaderResourceView</strong></a></td>

</tr>
</tbody>
</table>



 

## <a name="create-the-compute-uavs"></a>建立計算 UAVs

我們需要建立 UAVs 來儲存計算工作的結果。 當轉譯目標可看到三角形的計算著色器時，它會附加至這個 UAV，然後由 [**ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) API 取用。

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
<th>呼叫流程</th>
<th>參數</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></td>
</tr>
<tr class="even">
<td><a href="cd3dx12-resource-desc.md"><strong>CD3DX12_RESOURCE_DESC</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags"><strong>D3D12_RESOURCE_FLAGS</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></td>
<td><dl><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a><br />
</dl></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_unordered_access_view_desc"><strong>D3D12_UNORDERED_ACCESS_VIEW_DESC</strong></a></td>
<td><dl><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_uav_dimension"><strong>D3D12_UAV_DIMENSION</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags"><strong>D3D12_BUFFER_UAV_FLAGS</strong></a><br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview"><strong>CreateUnorderedAccessView</strong></a></td>

</tr>
</tbody>
</table>



 

## <a name="drawing-the-frame"></a>繪製框架

當繪製框架時，如果我們處於正在叫用計算著色器的模式中，而且 GPU 正在處理間接命令，我們會先 [**分派**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch) 該工作來填入 [**ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect)的命令緩衝區。 下列程式碼片段會新增至 **PopulateCommandLists** 方法。

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
<th>呼叫流程</th>
<th>參數</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle"><strong>D3D12_GPU_DESCRIPTOR_HANDLE</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart"><strong>GetGPUDescriptorHandleForHeapStart</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature"><strong>SetComputeRootSignature</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap"><strong>ID3D12DescriptorHeap</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps"><strong>SetDescriptorHeaps</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable"><strong>SetComputeRootDescriptorTable</strong></a></td>
<td><a href="cd3dx12-gpu-descriptor-handle.md"><strong>CD3DX12_GPU_DESCRIPTOR_HANDLE</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants"><strong>SetComputeRoot32BitConstants</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion"><strong>CopyBufferRegion</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier"><strong>D3D12_RESOURCE_BARRIER</strong></a></td>
<td><dl><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a><br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch"><strong>分派</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close"><strong>關閉</strong></a></td>

</tr>
</tbody>
</table>



 

接著，我們會在已啟用 UAV (GPU 剔除) 或完整命令緩衝區 (已停用的 GPU 剔除) 中執行命令。

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
<th>呼叫流程</th>
<th>參數</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature"><strong>SetGraphicsRootSignature</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap"><strong>ID3D12DescriptorHeap</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps"><strong>SetDescriptorHeaps</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports"><strong>RSSetViewports</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects"><strong>RSSetScissorRects</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier"><strong>D3D12_RESOURCE_BARRIER</strong></a></td>
<td><dl><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a><br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></td>

</tr>
<tr class="even">
<td><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets"><strong>OMSetRenderTargets</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview"><strong>ClearRenderTargetView</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview"><strong>ClearDepthStencilView</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_clear_flags"><strong>D3D12_CLEAR_FLAGS</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology"><strong>IASetPrimitiveTopology</strong></a></td>
<td><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology"><strong>D3D_PRIMITIVE_TOPOLOGY</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers"><strong>IASetVertexBuffers</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect"><strong>ExecuteIndirect</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close"><strong>關閉</strong></a></td>

</tr>
</tbody>
</table>



 

如果我們使用 GPU 剔除模式，則會讓圖形命令佇列等待計算工作完成，再開始執行間接命令。 在 **OnRender** 方法中，會新增下列程式碼片段。

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



| 呼叫流程                                                             | 參數 |
|-----------------------------------------------------------------------|------------|
| [**ID3D12CommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist)                        |            |
| [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) |            |
| [**訊號**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-signal)                           |            |
| [**等候**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-wait)                               |            |
| [**ID3D12CommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist)                        |            |
| [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) |            |



 

## <a name="run-the-sample"></a>執行範例

具有 GPU 基本物件的範例會進行挑選。

![使用 gpu 剔除的 exectue 間接範例螢幕擷取畫面](images/executeindirect-withculling.png)

沒有 GPU 基本的範例會進行剔除。

![沒有 gpu 剔除的 exectue 間接範例螢幕擷取畫面](images/executeindirect-withoutculling.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[D3D12 程式碼逐步解說-解說](d3d12-code-walk-throughs.md)
</dt> <dt>

[DirectX advanced learning 影片教學課程：執行間接和非同步 GPU 剔除](https://www.youtube.com/watch?v=fKD-VKJeeds)
</dt> <dt>

[間接繪圖](indirect-drawing.md)
</dt> </dl>

 

 

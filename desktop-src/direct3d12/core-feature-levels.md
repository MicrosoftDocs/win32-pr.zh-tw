---
title: Direct3D 12 Core 1.0 功能層級
description: 核心1.0 功能層級是完整的 Direct3D 12 功能集的子集。
ms.topic: article
ms.date: 11/05/2019
ms.openlocfilehash: 42d13b71c516e55ecce378cf9cb415c45e520ba9
ms.sourcegitcommit: bba068130240d16de8a3f3468b7cd72b2cd760f6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/03/2020
ms.locfileid: "106965419"
---
# <a name="the-direct3d-12-core-10-feature-level"></a>Direct3D 12 Core 1.0 功能層級

核心1.0 功能層級是完整的 Direct3D 12 功能集的子集。 核心1.0 功能等級可以由稱為 *僅限計算裝置* 的裝置類別公開。 計算專用裝置的整體驅動程式模型是 Microsoft 計算驅動程式模型 (MCDM) 。 MCDM 是 Windows 設備磁碟機模型的向下調整對等， (WDDM) ，其範圍較大。

*僅* 支援核心功能等級內功能的裝置稱為 *核心裝置*。

> [!NOTE]
> *僅限計算的裝置*、 *MCDM 裝置*、 *核心功能等級裝置* 和 *核心裝置* 都代表相同的東西。 為了簡單起見，我們偏好使用 *核心裝置* 。

## <a name="creating-a-core-device"></a>建立核心裝置

一般而言，若要建立 Direct3D 12 裝置，您必須呼叫 [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) 函式，並指定最小功能層級。

如果您指定9到12的功能層級，則傳回的裝置會是功能豐富的裝置，例如傳統的 GPU (，可支援核心裝置) 功能的超集合。 這一系列的功能層級絕不會傳回核心裝置。

另一方面，如果您指定核心功能等級 (例如 [**D3D_FEATURE_LEVEL：:D 3D_FEATURE_LEVEL_1_0_CORE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)) ，則傳回的裝置可能會有豐富功能，或可能是核心裝置。

```cpp
// d3dcommon.h
D3D_FEATURE_LEVEL_1_0_CORE = 0x1000
```

如果您指定 `_CORE` 功能等級，則執行時間/debug 層會驗證該功能層級是否允許您的應用程式所使用的功能 `_CORE` 。 本主題稍後會定義這組功能。

## <a name="shader-model-for-core-devices"></a>核心裝置的著色器模型

核心裝置支援著色器模型 5.0 +。

執行時間會執行 5. x 非 DXIL 著色器模型至 6.0 DXIL 的轉換。 因此驅動程式只需要支援6.x。

## <a name="resource-management-model-for-core-devices"></a>核心裝置的資源管理模型

- 支援的資源維度：原始和結構化緩衝區只 (沒有具類型的緩衝區、texture1d/2D 等等 ) 
- 不支援保留的 (磚) 資源
- 不支援自訂堆積
- 不支援下列任何堆積旗標：
  - D3D12_HEAP_FLAG_HARDWARE_PROTECTED
  - D3D12_HEAP_FLAG_ALLOW_WRITE_WATCH
  - D3D12_HEAP_FLAG_ALLOW_DISPLAY
  - D3D12_HEAP_FLAG_ALLOW_SHADER_ATOMICS (附注著色器 ATOMICS 是必要的，此旗標適用于另一項功能，也就是交叉配接器 ATOMICS) 

## <a name="resource-binding-model-for-core-devices"></a>核心裝置的資源系結模型

- 僅支援資源系結層1
- 例外狀況：
  - 不支援材質取樣器
  - 支援 64 UAVs，例如功能等級 11.1 + (，而不只是 8) 
  - 在對資源的著色器存取中，執行不需要透過描述項來執行界限檢查，而超出範圍的存取會產生未定義的行為。
    - 做為副產品，不支援根簽章中 D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_STATIC_KEEPING_BUFFER_BOUNDS_CHECKS 描述項範圍旗標。
- UAV/CBV 描述項只能在 (預設堆積的資源上進行，所以沒有上傳/readback 堆積) 。 這會強制您的應用程式執行複本，以取得跨 CPU< >GPU 的資料。
- 儘管是最低的系結功能層級，但仍有一些必要的功能，即使在這一層中也值得呼叫：
  - 描述項堆積可以在記錄命令清單之後更新 (請參閱資源系結規格中的 D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE) 
  - 根目錄描述元基本上是 GPUVA 指標
    - 即使沒有 MMU/VA 支援，在根描述項中使用的緩衝區 VAs 也可以藉由執行位址修補來模擬。

### <a name="structured-buffer-restrictions"></a>結構化緩衝區限制

結構化緩衝區必須有4位元組對齊的基底位址，而跨距必須是2或4的倍數。 2 stride 的案例是針對具有16位資料的應用程式，特別是在 D3D_FEATURE_LEVEL_1_0_CORE 中不支援輸入緩衝區。

描述項中指定的 stride 必須與 HLSL 中指定的 stride 相符。  

## <a name="command-queue-support-for-core-devices"></a>核心裝置的命令佇列支援

計算和複製佇列只 (沒有3D、影片等) 的佇列。

## <a name="shader-support-for-core-devices"></a>核心裝置的著色器支援

僅計算著色器，沒有任何圖形著色器 (頂點、圖元著色器等，) 或任何相關的功能，例如呈現目標、交換鏈、輸入組合語言。

### <a name="arithmetic-precision"></a>算術精確度

核心裝置不需要支援16位浮點運算的 denorms。

## <a name="supported-apis-for-core-devices"></a>核心裝置支援的 Api

下列清單代表受支援的完整應用程式開發介面子集 *(不會**在) 中列出核心* 1.0 功能等級所支援的 api。

### <a name="id3d12device-methods"></a>ID3D12Device 方法

* [ID3D12Device::CheckFeatureSupport](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)
* [ID3D12Device::CopyDescriptors](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptors)
* [ID3D12Device::CopyDescriptorsSimple](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple)
* [ID3D12Device::CreateCommandAllocator](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator)
* [ID3D12Device::CreateCommandList](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist)
* [ID3D12Device::CreateCommandQueue](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue)
* [ID3D12Device::CreateCommandSignature](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandsignature)
* [ID3D12Device::CreateCommittedResource](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource)
* [ID3D12Device::CreateComputePipelineState](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate)
* [ID3D12Device::CreateConstantBufferView](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
* [ID3D12Device::CreateDescriptorHeap](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap)
* [ID3D12Device::CreateFence](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence)
* [ID3D12Device::CreateHeap](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createheap)
* [ID3D12Device::CreatePlacedResource](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource)
* [ID3D12Device::CreateQueryHeap](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createqueryheap)
* [ID3D12Device::CreateRootSignature](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)
* [ID3D12Device::CreateShaderResourceView](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)
* [ID3D12Device::CreateSharedHandle](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle)
* [ID3D12Device::CreateUnorderedAccessView](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)
* [ID3D12Device：：收回](/windows/win32/api/d3d12/nf-d3d12-id3d12device-evict)
* [ID3D12Device::GetAdapterLuid](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getadapterluid)
* [ID3D12Device::GetCopyableFootprints](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)
* [ID3D12Device::GetCustomHeapProperties](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties)
* [ID3D12Device::GetDescriptorHandleIncrementSize](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)
* [ID3D12Device::GetDeviceRemovedReason](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdeviceremovedreason)
* [ID3D12Device::GetNodeCount](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getnodecount)
* [ID3D12Device::GetResourceAllocationInfo](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)
* [ID3D12Device::MakeResident](/windows/win32/api/d3d12/nf-d3d12-id3d12device-makeresident)
* [ID3D12Device::OpenSharedHandle](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandle)
* [ID3D12Device::OpenSharedHandleByName](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandlebyname)
* [ID3D12Device::SetStablePowerState](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)

### <a name="id3d12device1-methods"></a>ID3D12Device1 方法

* [ID3D12Device1::CreatePipelineLibrary](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-createpipelinelibrary)
* [ID3D12Device1::SetEventOnMultipleFenceCompletion](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-seteventonmultiplefencecompletion)
* [ID3D12Device1::SetResidencySetEventOnMultipleFenceCompletionPriority](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-setresidencypriority)

### <a name="id3d12device2-methods"></a>ID3D12Device2 方法

* [ID3D12Device2::CreatePipelineState](/windows/win32/api/d3d12/nf-d3d12-id3d12device2-createpipelinestate)

### <a name="id3d12device3-methods"></a>ID3D12Device3 方法

* [ID3D12Device3::OpenExistingHeapFromAddress](/windows/win32/api/d3d12/nf-d3d12-id3d12device3-openexistingheapfromaddress)
* [ID3D12Device3::OpenExistingHeapFromFileMapping](/previous-versions/windows/desktop/legacy/mt813613(v%3Dvs.85))
* [ID3D12Device3::EnqueueMakeResident](/windows/win32/api/d3d12/nf-d3d12-id3d12device3-enqueuemakeresident)

### <a name="id3d12device4-methods"></a>ID3D12Device4 方法

* [ID3D12Device4::GetResourceAllocationInfo1](/windows/win32/api/d3d12/nf-d3d12-id3d12device4-getresourceallocationinfo1)

### <a name="id3d12device5-methods"></a>ID3D12Device5 方法

* [ID3D12Device5::CreateMetaCommand](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-createmetacommand)
* [ID3D12Device5::CreateStateObject](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-createstateobject)
* [ID3D12Device5::EnumerateMetaCommandParameters](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-enumeratemetacommandparameters)
* [ID3D12Device5::EnumerateMetaCommands](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-enumeratemetacommands)
* [ID3D12Device5::RemoveDevice](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-removedevice)

### <a name="id3d12commandqueue-methods"></a>ID3D12CommandQueue 方法

* [ID3D12CommandQueue::BeginEvent](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-beginevent)
* [ID3D12CommandQueue::EndEvent](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-endevent)
* [ID3D12CommandQueue::ExecuteCommandLists](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)
* [ID3D12CommandQueue::GetClockCalibration](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration)
* [ID3D12CommandQueue::GetDesc](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getdesc)
* [ID3D12CommandQueue::GetTimestampFrequency](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency)
* [ID3D12CommandQueue::SetMarker](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-setmarker)
* [ID3D12CommandQueue：：信號](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)
* [ID3D12CommandQueue：： Wait](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait)

### <a name="id3d12commandlist-methods"></a>ID3D12CommandList 方法

* [ID3D12CommandList：： GetType](/windows/win32/api/d3d12/nf-d3d12-id3d12commandlist-gettype)

### <a name="id3d12graphicscommandlist-methods"></a>ID3D12GraphicsCommandList 方法

* [ID3D12GraphicsCommandList::BeginEvent](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginevent)
* [ID3D12GraphicsCommandList::BeginQuery](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery)
* [ID3D12GraphicsCommandList::ClearState](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate)
* [ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
* [ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
* [ID3D12GraphicsCommandList：： Close](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)
* [ID3D12GraphicsCommandList::CopyBufferRegion](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
* [ID3D12GraphicsCommandList::CopyResource](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
* [ID3D12GraphicsCommandList::CopyTextureRegion](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
* [ID3D12GraphicsCommandList：:D ispatch](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
* [ID3D12GraphicsCommandList::EndEvent](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endevent)
* [ID3D12GraphicsCommandList::EndQuery](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery)
* [ID3D12GraphicsCommandList：： Reset](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)
* [ID3D12GraphicsCommandList::ResolveQueryData](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata)
* [ID3D12GraphicsCommandList::ResourceBarrier](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)
* [ID3D12GraphicsCommandList::SetComputeRoot32BitConstant](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
* [ID3D12GraphicsCommandList::SetComputeRoot32BitConstants](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)
* [ID3D12GraphicsCommandList::SetComputeRootConstantBufferView](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
* [ID3D12GraphicsCommandList::SetComputeRootDescriptorTable](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable)
* [ID3D12GraphicsCommandList::SetComputeRootShaderResourceView](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
* [ID3D12GraphicsCommandList::SetComputeRootSignature](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature)
* [ID3D12GraphicsCommandList::SetComputeRootUnorderedAccessView](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
* [ID3D12GraphicsCommandList::SetDescriptorHeaps](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)
* [ID3D12GraphicsCommandList::SetMarker](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setmarker)
* [ID3D12GraphicsCommandList::SetPipelineState](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)
* [ID3D12GraphicsCommandList::SetPredication](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)

### <a name="id3d12graphicscommandlist1-methods"></a>ID3D12GraphicsCommandList1 方法

* [ID3D12GraphicsCommandList1::AtomicCopyBufferUINT](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint)
* [ID3D12GraphicsCommandList1::AtomicCopyBufferUINT64](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint64)

### <a name="id3d12graphicscommandlist2-methods"></a>ID3D12GraphicsCommandList2 方法

* [ID3D12GraphicsCommandList2::WriteBufferImmediate](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist2-writebufferimmediate)

### <a name="id3d12graphicscommandlist4-methods"></a>ID3D12GraphicsCommandList4 方法

* [ID3D12GraphicsCommandList4::ExecuteMetaCommand](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-executemetacommand)
* [ID3D12GraphicsCommandList4::InitializeMetaCommand](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-initializemetacommand)

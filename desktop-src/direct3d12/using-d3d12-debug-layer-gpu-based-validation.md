---
title: 以 GPU 為基礎的驗證和 Direct3D 12 Debug 層
description: 本主題說明如何充分利用 Direct3D 12 Debug 層。 以 GPU 為基礎的驗證 (GBV) 啟用 GPU 時間軸上的驗證案例，這在 CPU 上的 API 呼叫期間無法執行。
ms.assetid: 01D1F94F-4DD4-4781-86EF-6C639E8B1069
ms.localizationpriority: high
ms.topic: article
ms.date: 02/12/2019
ms.openlocfilehash: 3160df3faf994df2abf9cf878088e84564bb5fe1
ms.sourcegitcommit: 00e0a8e56d28c4c720b97f0cf424c29f547460d7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "104548443"
---
# <a name="gpu-based-validation-and-the-direct3d-12-debug-layer"></a><span data-ttu-id="33584-104">以 GPU 為基礎的驗證和 Direct3D 12 Debug 層</span><span class="sxs-lookup"><span data-stu-id="33584-104">GPU-based validation and the Direct3D 12 Debug Layer</span></span>

<span data-ttu-id="33584-105">本主題說明如何充分利用 Direct3D 12 Debug 層。</span><span class="sxs-lookup"><span data-stu-id="33584-105">This topic describes how to make best use of the Direct3D 12 Debug Layer.</span></span> <span data-ttu-id="33584-106">以 GPU 為基礎的驗證 (GBV) 啟用 GPU 時間軸上的驗證案例，這在 CPU 上的 API 呼叫期間無法執行。</span><span class="sxs-lookup"><span data-stu-id="33584-106">GPU-based validation (GBV) enables validation scenarios on the GPU timeline that are not possible during API calls on the CPU.</span></span> <span data-ttu-id="33584-107">從「適用于 Windows 10 年度更新版的圖形工具」開始，可以使用 GBV。</span><span class="sxs-lookup"><span data-stu-id="33584-107">GBV is available starting with the Graphics Tools for Windows 10 Anniversary Update.</span></span>

## <a name="purpose-of-gpu-based-validation"></a><span data-ttu-id="33584-108">以 GPU 為基礎的驗證用途</span><span class="sxs-lookup"><span data-stu-id="33584-108">Purpose of GPU-based validation</span></span>

<span data-ttu-id="33584-109">以 GPU 為基礎的驗證有助於識別下列錯誤：</span><span class="sxs-lookup"><span data-stu-id="33584-109">GPU-based validation helps to identify the following errors:</span></span>

- <span data-ttu-id="33584-110">在著色器中使用未初始化或不相容的描述項。</span><span class="sxs-lookup"><span data-stu-id="33584-110">Use of uninitialized or incompatible descriptors in a shader.</span></span>
- <span data-ttu-id="33584-111">在著色器中使用參考已刪除資源的描述項。</span><span class="sxs-lookup"><span data-stu-id="33584-111">Use of descriptors referencing deleted Resources in a shader.</span></span>
- <span data-ttu-id="33584-112">驗證已升級的資源狀態和資源狀態衰減。</span><span class="sxs-lookup"><span data-stu-id="33584-112">Validation of promoted resource states and resource state decay.</span></span>
- <span data-ttu-id="33584-113">在著色器中超出描述元堆積結尾的索引。</span><span class="sxs-lookup"><span data-stu-id="33584-113">Indexing beyond the end of the descriptor heap in a shader.</span></span>
- <span data-ttu-id="33584-114">著色器存取不相容狀態的資源。</span><span class="sxs-lookup"><span data-stu-id="33584-114">Shader accesses of resources in incompatible state.</span></span>
- <span data-ttu-id="33584-115">在著色器中使用未初始化或不相容的取樣器。</span><span class="sxs-lookup"><span data-stu-id="33584-115">Use of uninitialized or incompatible Samplers in a shader.</span></span>

<span data-ttu-id="33584-116">GBV 的運作方式是建立已修補的著色器，並將驗證直接新增至著色器。</span><span class="sxs-lookup"><span data-stu-id="33584-116">GBV works by creating patched shaders that have validation added directly to the shader.</span></span> <span data-ttu-id="33584-117">經過修補的著色器會檢查著色器執行期間所存取的根引數和資源，並將錯誤報表給記錄緩衝區。</span><span class="sxs-lookup"><span data-stu-id="33584-117">The patched shaders inspect root arguments and resources accessed during shader execution and report errors to a log buffer.</span></span> <span data-ttu-id="33584-118">GBV 也會在應用程式命令清單中插入額外的作業和分派呼叫，以驗證及追蹤 GPU 時間軸上命令清單所加諸的資源狀態變更。</span><span class="sxs-lookup"><span data-stu-id="33584-118">GBV also injects extra operations and Dispatch calls into the application command lists to validate and track changes to resource state imposed by the command list on the GPU-timeline.</span></span>

<span data-ttu-id="33584-119">由於 GBV 需要能夠執行著色器，因此複製命令清單是由計算命令清單所模擬。</span><span class="sxs-lookup"><span data-stu-id="33584-119">Because GBV requires the ability to execute shaders, COPY command lists are emulated by a COMPUTE command list.</span></span> <span data-ttu-id="33584-120">這可能會變更硬體執行複製的方式，但不應該變更最終結果。</span><span class="sxs-lookup"><span data-stu-id="33584-120">This may potentially change how hardware performs copies though the end result should not be changed.</span></span> <span data-ttu-id="33584-121">應用程式仍然會察覺到這些都是複製命令清單，而 debug 層會以這樣的方式驗證它們。</span><span class="sxs-lookup"><span data-stu-id="33584-121">The application will still perceive these are COPY command lists and the debug layer will validate them as such.</span></span>

## <a name="turning-on-gpu-based-validation"></a><span data-ttu-id="33584-122">開啟以 GPU 為基礎的驗證</span><span class="sxs-lookup"><span data-stu-id="33584-122">Turning on GPU-based validation</span></span>

<span data-ttu-id="33584-123">您可以強制執行 Direct3D 12 Debug 層，並在 [控制台] 的 [新增] 索引標籤) 中強制執行以 GPU 為基礎的 (驗證，以強制 GBV DXCPL) 使用 DirectX (控制台來強制執行。</span><span class="sxs-lookup"><span data-stu-id="33584-123">GBV can be forced on using the DirectX Control Panel (DXCPL) by forcing on the Direct3D 12 Debug Layer and additionally forcing on GPU-based validation (new tab in the control panel).</span></span> <span data-ttu-id="33584-124">啟用之後，GBV 就會維持啟用狀態，直到您釋放 Direct3D 12 裝置為止。</span><span class="sxs-lookup"><span data-stu-id="33584-124">Once enabled, GBV will remain enabled until the Direct3D 12 device is released.</span></span> <span data-ttu-id="33584-125">或者，您可以在建立 Direct3D 12 裝置之前，以程式設計方式啟用 GBV：</span><span class="sxs-lookup"><span data-stu-id="33584-125">Alternatively, GBV can be enabled programmatically prior to creating the Direct3D 12 Device:</span></span>

```cpp
void EnableShaderBasedValidation()
{
    CComPtr<ID3D12Debug> spDebugController0;
    CComPtr<ID3D12Debug1> spDebugController1;
    VERIFY(D3D12GetDebugInterface(IID_PPV_ARGS(&spDebugController0)));
    VERIFY(spDebugController0->QueryInterface(IID_PPV_ARGS(&spDebugController1)));
    spDebugController1->SetEnableGPUBasedValidation(true);
}
```

## <a name="recommended-usage"></a><span data-ttu-id="33584-126">建議用法</span><span class="sxs-lookup"><span data-stu-id="33584-126">Recommended usage</span></span>

<span data-ttu-id="33584-127">一般而言，您應該在大部分的情況下，執行您的程式碼並啟用偵錯工具層。</span><span class="sxs-lookup"><span data-stu-id="33584-127">Generally, you should run your code with the debug layer enabled most of the time.</span></span> <span data-ttu-id="33584-128">不過，GBV 可能會使問題變慢。</span><span class="sxs-lookup"><span data-stu-id="33584-128">However, GBV can slow things down a lot.</span></span> <span data-ttu-id="33584-129">開發人員可以考慮使用較小的資料集來啟用 GBV (例如，使用較少 PSO 和) 資源的引擎示範或小型遊戲層級，或在早期應用程式啟動時減少效能問題。</span><span class="sxs-lookup"><span data-stu-id="33584-129">Developers may consider enabling GBV with smaller data sets (for example, engine demos or small game levels with fewer PSO’s and resources) or during early application bring-up to reduce performance problems.</span></span> <span data-ttu-id="33584-130">使用較大的內容時，請考慮在夜間測試階段中的一或兩部測試電腦上開啟 GBV。</span><span class="sxs-lookup"><span data-stu-id="33584-130">With larger content consider turning on GBV on one or two test machines in a nightly test pass.</span></span>

## <a name="debug-output"></a><span data-ttu-id="33584-131">調試輸出</span><span class="sxs-lookup"><span data-stu-id="33584-131">Debug output</span></span>

<span data-ttu-id="33584-132">GBV 會在對 GPU 執行 [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) 的呼叫完成後，產生調試輸出。</span><span class="sxs-lookup"><span data-stu-id="33584-132">GBV produces debug output after a call to [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) completes execution on the GPU.</span></span> <span data-ttu-id="33584-133">因為這是在 GPU-時間軸上，所以 debug 輸出可能會與其他 CPU 時間軸驗證進行非同步處理。</span><span class="sxs-lookup"><span data-stu-id="33584-133">Since this is on the GPU-timeline the debug output may be asynchronous with other CPU-timeline validation.</span></span> <span data-ttu-id="33584-134">應用程式開發人員可能會想要插入自己的等候後執行，以同步處理 debug 輸出。</span><span class="sxs-lookup"><span data-stu-id="33584-134">Application developers may want to inject their own wait-after-execute to synchronize debug output.</span></span>

<span data-ttu-id="33584-135">GBV 輸出會識別著色器中發生錯誤的位置，以及相關物件的目前繪製/分派計數和識別 (例如命令清單、佇列、PSO 等) 。</span><span class="sxs-lookup"><span data-stu-id="33584-135">GBV output identifies where in a shader an error occurred, along with the current draw/dispatch count and identities of related objects (e.g. command list, queue, PSO, etc).</span></span>

## <a name="example-debug-message"></a><span data-ttu-id="33584-136">範例 debug 訊息</span><span class="sxs-lookup"><span data-stu-id="33584-136">Example debug message</span></span>

<span data-ttu-id="33584-137">下列錯誤訊息表示名稱為「主要色彩緩衝區」的資源，在著色器中已存取為著色器資源，但在 GPU 上執行著色器時處於未排序的存取狀態。</span><span class="sxs-lookup"><span data-stu-id="33584-137">The following error message indicates that a resource named “Main Color Buffer” was accessed in a shader as a shader resource but was in the unordered access state when the shader ran on the GPU.</span></span> <span data-ttu-id="33584-138">此外也會提供其他資訊，例如著色器來源中的位置、命令清單的名稱和繪製計數 (繪製索引) ，以及相關的 D3D 介面物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="33584-138">Additional information, such as the location in the shader source, the name of the command list and the Draw count (Draw Index), and the names of related D3D interface objects are also provided.</span></span>

```cmd
D3D12 ERROR: Incompatible resource state: Resource: 0x0000016F61A6EA80:'Main Color Buffer', 
Subresource Index: [0], 
Descriptor heap index: [0], 
Binding Type In Descriptor: SRV, 
Resource State: D3D12_RESOURCE_STATE_UNORDERED_ACCESS(0x8), 
Shader Stage: PIXEL, 
Root Parameter Index: [0], 
Draw Index: [0], 
Shader Code: E:\FileShare\MiniEngine_GitHub_160128\MiniEngine_GitHub\Core\Shaders\SharpeningUpsamplePS.hlsl(37,2-59), 
Asm Instruction Range: [0x138-0x16b], 
Asm Operand Index: [3], 
Command List: 0x0000016F6F75F740:'CommandList', SRV/UAV/CBV Descriptor Heap: 0x0000016F6F76F280:'Unnamed ID3D12DescriptorHeap Object', 
Sampler Descriptor Heap: <not set>, 
Pipeline State: 0x0000016F572C89F0:'Unnamed ID3D12PipelineState Object',  
[ EXECUTION ERROR #942: GPU_BASED_VALIDATION_INCOMPATIBLE_RESOURCE_STATE]
```

## <a name="debug-layer-apis"></a><span data-ttu-id="33584-139">Debug Layer Api</span><span class="sxs-lookup"><span data-stu-id="33584-139">Debug Layer APIs</span></span>

<span data-ttu-id="33584-140">若要啟用 debug 層，請呼叫 [**EnableDebugLayer**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug-enabledebuglayer)。</span><span class="sxs-lookup"><span data-stu-id="33584-140">To enable the debug layer, call [**EnableDebugLayer**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug-enabledebuglayer).</span></span>

<span data-ttu-id="33584-141">若要啟用以 GPU 為基礎的驗證，請呼叫 [**SetEnableGPUBasedValidation**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug1-setenablegpubasedvalidation)，然後參考下列介面的方法：</span><span class="sxs-lookup"><span data-stu-id="33584-141">To enable GPU-based validation, call [**SetEnableGPUBasedValidation**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug1-setenablegpubasedvalidation), and refer to the methods of the following interfaces:</span></span>

- [<span data-ttu-id="33584-142">**ID3D12Debug1**</span><span class="sxs-lookup"><span data-stu-id="33584-142">**ID3D12Debug1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1)
- [<span data-ttu-id="33584-143">**ID3D12DebugCommandList1**</span><span class="sxs-lookup"><span data-stu-id="33584-143">**ID3D12DebugCommandList1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1)
- [<span data-ttu-id="33584-144">**ID3D12DebugDevice1**</span><span class="sxs-lookup"><span data-stu-id="33584-144">**ID3D12DebugDevice1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1)

<span data-ttu-id="33584-145">請參閱下列列舉和結構：</span><span class="sxs-lookup"><span data-stu-id="33584-145">Refer to the following enumerations and structures:</span></span>

- [<span data-ttu-id="33584-146">**D3D12 \_ DEBUG \_ 命令 \_ 清單 \_ 參數 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="33584-146">**D3D12\_DEBUG\_COMMAND\_LIST\_PARAMETER\_TYPE**</span></span>](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_command_list_parameter_type)
- [<span data-ttu-id="33584-147">**D3D12 \_ DEBUG \_ 裝置 \_ 參數 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="33584-147">**D3D12\_DEBUG\_DEVICE\_PARAMETER\_TYPE**</span></span>](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_device_parameter_type)
- [<span data-ttu-id="33584-148">**D3D12 以 \_ GPU 為 \_ 基礎的 \_ 驗證 \_ 管線 \_ 狀態 \_ 建立 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="33584-148">**D3D12\_GPU\_BASED\_VALIDATION\_PIPELINE\_STATE\_CREATE\_FLAGS**</span></span>](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_pipeline_state_create_flags)
- [<span data-ttu-id="33584-149">**D3D12 以 \_ GPU 為 \_ 基礎的 \_ 驗證 \_ 著色器 \_ 修補 \_ 模式**</span><span class="sxs-lookup"><span data-stu-id="33584-149">**D3D12\_GPU\_BASED\_VALIDATION\_SHADER\_PATCH\_MODE**</span></span>](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_shader_patch_mode)
- [<span data-ttu-id="33584-150">**D3D12 \_ DEBUG \_ 命令 \_ 清單以 \_ GPU 為基礎的 \_ \_ 驗證 \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="33584-150">**D3D12\_DEBUG\_COMMAND\_LIST\_GPU\_BASED\_VALIDATION\_SETTINGS**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_command_list_gpu_based_validation_settings)
- [<span data-ttu-id="33584-151">**D3D12 \_ DEBUG \_ 裝置 \_ GPU \_ 型 \_ 驗證 \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="33584-151">**D3D12\_DEBUG\_DEVICE\_GPU\_BASED\_VALIDATION\_SETTINGS**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_device_gpu_based_validation_settings)

## <a name="related-topics"></a><span data-ttu-id="33584-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="33584-152">Related topics</span></span>

* [<span data-ttu-id="33584-153">瞭解 Direct3D 12 Debug 層</span><span class="sxs-lookup"><span data-stu-id="33584-153">Understanding the Direct3D 12 Debug Layer</span></span>](understanding-the-d3d12-debug-layer.md)

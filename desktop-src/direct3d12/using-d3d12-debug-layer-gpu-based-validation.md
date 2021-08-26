---
title: 以 GPU 為基礎的驗證和 Direct3D 12 Debug 層
description: 本主題說明如何充分利用 Direct3D 12 Debug 層。 以 GPU 為基礎的驗證 (GBV) 啟用 GPU 時間軸上的驗證案例，這在 CPU 上的 API 呼叫期間無法執行。
ms.assetid: 01D1F94F-4DD4-4781-86EF-6C639E8B1069
ms.localizationpriority: high
ms.topic: article
ms.date: 02/12/2019
ms.openlocfilehash: 63e1ebbe34bbb94fbdf52b374b10283100e3bfa432338521a9807497b236d868
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952738"
---
# <a name="gpu-based-validation-and-the-direct3d-12-debug-layer"></a>以 GPU 為基礎的驗證和 Direct3D 12 Debug 層

本主題說明如何充分利用 Direct3D 12 Debug 層。 以 GPU 為基礎的驗證 (GBV) 啟用 GPU 時間軸上的驗證案例，這在 CPU 上的 API 呼叫期間無法執行。 從 Windows 10 周年更新的圖形工具開始提供 GBV。

## <a name="purpose-of-gpu-based-validation"></a>以 GPU 為基礎的驗證用途

以 GPU 為基礎的驗證有助於識別下列錯誤：

- 在著色器中使用未初始化或不相容的描述項。
- 在著色器中使用參考已刪除資源的描述項。
- 驗證已升級的資源狀態和資源狀態衰減。
- 在著色器中超出描述元堆積結尾的索引。
- 著色器存取不相容狀態的資源。
- 在著色器中使用未初始化或不相容的取樣器。

GBV 的運作方式是建立已修補的著色器，並將驗證直接新增至著色器。 經過修補的著色器會檢查著色器執行期間所存取的根引數和資源，並將錯誤報表給記錄緩衝區。 GBV 也會在應用程式命令清單中插入額外的作業和分派呼叫，以驗證及追蹤 GPU 時間軸上命令清單所加諸的資源狀態變更。

由於 GBV 需要能夠執行著色器，因此複製命令清單是由計算命令清單所模擬。 這可能會變更硬體執行複製的方式，但不應該變更最終結果。 應用程式仍然會察覺到這些都是複製命令清單，而 debug 層會以這樣的方式驗證它們。

## <a name="turning-on-gpu-based-validation"></a>開啟以 GPU 為基礎的驗證

您可以強制執行 Direct3D 12 Debug 層，並在 [控制台]) 的 [新增] 索引標籤上強制執行以 GPU 為基礎的 (驗證，以強制執行 GBV (DXCPL) 主控台的。 啟用之後，GBV 就會維持啟用狀態，直到您釋放 Direct3D 12 裝置為止。 或者，您可以在建立 Direct3D 12 裝置之前，以程式設計方式啟用 GBV：

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

## <a name="recommended-usage"></a>建議用法

一般而言，您應該在大部分的情況下，執行您的程式碼並啟用偵錯工具層。 不過，GBV 可能會使問題變慢。 開發人員可以考慮使用較小的資料集來啟用 GBV (例如，使用較少 PSO 和) 資源的引擎示範或小型遊戲層級，或在早期應用程式啟動時減少效能問題。 使用較大的內容時，請考慮在夜間測試階段中的一或兩部測試電腦上開啟 GBV。

## <a name="debug-output"></a>調試輸出

GBV 會在對 GPU 執行 [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) 的呼叫完成後，產生調試輸出。 因為這是在 GPU-時間軸上，所以 debug 輸出可能會與其他 CPU 時間軸驗證進行非同步處理。 應用程式開發人員可能會想要插入自己的等候後執行，以同步處理 debug 輸出。

GBV 輸出會識別著色器中發生錯誤的位置，以及相關物件的目前繪製/分派計數和識別 (例如命令清單、佇列、PSO 等) 。

## <a name="example-debug-message"></a>範例 debug 訊息

下列錯誤訊息表示名稱為「主要色彩緩衝區」的資源，在著色器中已存取為著色器資源，但在 GPU 上執行著色器時處於未排序的存取狀態。 此外也會提供其他資訊，例如著色器來源中的位置、命令清單的名稱和繪製計數 (繪製索引) ，以及相關的 D3D 介面物件的名稱。

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

## <a name="debug-layer-apis"></a>Debug Layer Api

若要啟用 debug 層，請呼叫 [**EnableDebugLayer**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug-enabledebuglayer)。

若要啟用以 GPU 為基礎的驗證，請呼叫 [**SetEnableGPUBasedValidation**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug1-setenablegpubasedvalidation)，然後參考下列介面的方法：

- [**ID3D12Debug1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1)
- [**ID3D12DebugCommandList1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1)
- [**ID3D12DebugDevice1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1)

請參閱下列列舉和結構：

- [**D3D12 \_ DEBUG \_ 命令 \_ 清單 \_ 參數 \_ 類型**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_command_list_parameter_type)
- [**D3D12 \_ DEBUG \_ 裝置 \_ 參數 \_ 類型**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_device_parameter_type)
- [**D3D12 以 \_ GPU 為 \_ 基礎的 \_ 驗證 \_ 管線 \_ 狀態 \_ 建立 \_ 旗標**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_pipeline_state_create_flags)
- [**D3D12 以 \_ GPU 為 \_ 基礎的 \_ 驗證 \_ 著色器 \_ 修補 \_ 模式**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_shader_patch_mode)
- [**D3D12 \_ DEBUG \_ 命令 \_ 清單以 \_ GPU 為基礎的 \_ \_ 驗證 \_ 設定**](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_command_list_gpu_based_validation_settings)
- [**D3D12 \_ DEBUG \_ 裝置 \_ GPU \_ 型 \_ 驗證 \_ 設定**](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_device_gpu_based_validation_settings)

## <a name="related-topics"></a>相關主題

* [瞭解 Direct3D 12 Debug 層](understanding-the-d3d12-debug-layer.md)

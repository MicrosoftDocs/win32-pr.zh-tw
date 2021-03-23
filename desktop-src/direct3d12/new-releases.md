---
title: Direct3D 12 的新功能
description: 本主題說明適用于各種版本之最重要的新 Direct3D 12 檔。
ms.assetid: 38F41E05-FECB-41DE-8D30-09733FBEAC48
ms.localizationpriority: high
ms.topic: article
ms.date: 12/05/2019
ms.openlocfilehash: ec3ecc9e68fc4711def2c364793eca32804d8d04
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548341"
---
# <a name="whats-new-in-direct3d-12"></a>Direct3D 12 的新功能

本主題說明適用于各種版本之最重要的新 Direct3D 12 檔。

如需取得和安裝 Direct3D 的詳細資訊，請參閱 [direct3d 12 程式設計環境設定](./directx-12-programming-environment-set-up.md)。

## <a name="direct3d-12-on-windows-7"></a>Windows 7 上的 Direct3D 12

- [Windows 7 上的 Direct3D 12](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/) 現在可供開發人員使用。

## <a name="windows-10-may-2019-update"></a>Windows 10 2019 年 5 月更新

這些功能和 Api 已新增或更新為 Windows 10 1903 版 (10.0;組建 18362) &mdash; 也稱為 Windows 10 的2019更新。

- [可變速率陰影 (VRS) ](./vrs.md)。 可讓您以不同于轉譯影像的速率配置轉譯效能/電源。
- [HLSL 著色器模型 6.4](../direct3dhlsl/hlsl-shader-model-6-4-features-for-direct3d-12.md)。 描述新增至 HLSL 著色器模型6.4 的機器學習內建函式。
- [**D3D12_DRED_VERSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_version) 列舉。 定義常數，以指定裝置的版本 (DR) 移除擴充的資料。
- [**D3D12_FEATURE_DATA_D3D12_OPTIONS6**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6) 結構。 指出介面卡為 metacommands 提供的支援層級。
- [**D3D12_FEATURE_DATA_QUERY_META_COMMAND**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_query_meta_command) 結構。 指出介面卡為 metacommands 提供的支援層級。
- [**D3D12_VARIABLE_SHADING_RATE_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) 列舉。 定義常數，指定 VRS) 的陰影速率層 (。
- [**ID3D12Device6**](/windows/win32/api/d3d12/nn-d3d12-id3d12device6) 介面和其方法。 用來設定驅動程式背景處理優化的模式。 另請參閱 [背景著色器優化](https://devblogs.microsoft.com/directx/background-shader-optimizations/)。
- [**ID3D12DeviceRemovedExtendedData**](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddata) 介面和其方法。 提供裝置的執行時間存取， (DR) 資料來移除擴充的資料。
- [**ID3D12DeviceRemovedExtendedDataSettings**](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddatasettings) 介面和其方法。 控制裝置 (DR) 設定移除擴充的資料。
- [**D3D12GraphicsCommandList5**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist5) 介面和其方法。 支援 (VRS) 的可變速率陰影。

[**D3D_SHADER_MODEL**](/windows/win32/api/d3d12/ne-d3d12-d3d_shader_model)的列舉已更新，並 (實驗層級的功能) 新增 **D3D_SHADER_MODEL_6_5** 常數。

[**D3D12_COMMAND_LIST_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type)的列舉已透過新增 **D3D12_COMMAND_LIST_TYPE_VIDEO_ENCODE** 常數進行更新。

[**D3D12_FEATURE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_feature)的列舉已透過新增 **D3D12_FEATURE_D3D12_OPTIONS6** 和 **D3D12_FEATURE_QUERY_META_COMMAND** 常數進行更新。

[**D3D12_RESOURCE_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)的列舉已透過新增 **D3D12_RESOURCE_STATE_SHADING_RATE_SOURCE** 常數進行更新。

## <a name="windows-10-version-1809"></a>Windows 10 版本 1809

這些功能和 Api 已新增或更新為 Windows 10 1809 版 (10.0;組建 17763) &mdash; 也稱為 Windows 10 2018 年10月更新。

- [Direct3D 12 Raytracing](./direct3d-12-raytracing.md)
- [Direct3D 12 轉譯階段](./direct3d-12-render-passes.md)

## <a name="windows-10-version-1709"></a>Windows 10 (版本 1709)

這些介面已新增至 Windows 10 1709 版的 Direct3D 檔。

-   [**ID3D12Fence1**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence1) 藉由支援抓取傳入來建立範圍的旗標，來擴充建立範圍的功能。
-   [**ID3D12GraphicsCommandList2**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist2) 藉由直接將立即值寫入緩衝區，來擴充可用圖形命令的清單。
-   [**ID3D12Device3**](/windows/win32/api/d3d12/nn-d3d12-id3d12device3) 藉由在系統記憶體中建立特殊用途的診斷堆積來擴充虛擬配接器的功能，即使在發生 GPU 錯誤或裝置移除的情況下，仍會持續保存。

[**D3d \_ 著色器 \_ 模型**](/windows/win32/api/d3d12/ne-d3d12-d3d_shader_model)列舉已新增新的 **D3D \_ 著色器 \_ 模型 \_ 6 \_ 1** 值，以描述著色器模型6.1。

[**D3D12 \_ 功能**](/windows/win32/api/d3d12/ne-d3d12-d3d12_feature)列舉也有新的 **D3D12 \_ 功能 \_ D3D12 \_ OPTIONS3** 和 **D3D12 \_ 功能 \_ 現有 \_** 的堆積值。 顧名思義，這些值可讓您檢查是否有其他 Direct3D12 選項，以及檢查是否支援現有的堆積。

## <a name="windows-10-version-1703"></a>Windows 10 (版本 1703)

這些主題已新增至 Windows 10 1703 版的 Direct3D 檔。

-   [**ID3D12Device2：： CreatePipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device2-createpipelinestate)方法和 [**D3D12 \_ 管線 \_ 狀態 \_ 資料流程 \_ Desc**](/windows/win32/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc)結構代表新的、更健全的建立 pso 方法，並統一建立圖形和計算管線的介面。
-   [**ID3D12Device1：： CreatePipelineLibrary1**](https://www.bing.com/search?q=**ID3D12Device1::CreatePipelineLibrary1**)方法會展開管線程式庫介面，以接受以新的統一 [**D3D12 \_ 管線 \_ 狀態 \_ 資料流程 \_ Desc**](/windows/win32/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc)結構建立的 pso。
-   [**D3D12EnableExperimentalFeatures**](/windows/win32/api/d3d12/nf-d3d12-d3d12enableexperimentalfeatures)函式可讓開發人員在開發人員模式下，使用電腦進行特定的開發功能實驗。
-   有五個新介面 (參考 [介面](interface-hierarchy.md) 階層) ：
    -   [**ID3D12GraphicsCommandList1**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist1)
    -   [**ID3D12PipelineLibrary1**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary1)
    -   [**ID3D12Device2**](/windows/win32/api/d3d12/nn-d3d12-id3d12device2)
    -   [**ID3D12Debug2**](/windows/win32/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug2)
    -   [**ID3D12Tools**](/windows/win32/api/d3d12/nn-d3d12-id3d12tools)
-   請參閱 [HLSL 著色器模型6.0 總覽](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md)，其中描述多執行緒圖元和計算著色器的 wave 內建作業。
-   [**ID3D12Device：： SetStablePowerState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)的使用已變更。
-   Direct3d 11 的一些新功能會在 [direct3d 11.4 功能](../direct3d11/direct3d-11-4-features.md)中說明。
-   [**AtomicCopyBufferUINT**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint) 和 [**AtomicCopyBufferUINT64**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint64) 可啟用 **延遲閂鎖** 以減少 pervieved 延遲。
-   [**ID3D12Device2：： CreatePipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device2-createpipelinestate) 和 [**OMSetDepthBounds**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-omsetdepthbounds) 可在支援的硬體上啟用 **深度界限測試** 。
-   [**ResolveSubresourceRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-resolvesubresourceregion) 可啟用子資源的 **部分解析** ，以協助將效能優化。
-   [**SetSamplePositions**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-setsamplepositions) 可在支援的硬體上啟用 **programable 範例位置** 。

## <a name="november-2016-documentation-update"></a>2016年11月檔更新

-   ID3D12GraphicsCommandList 的備註修訂 [**：:D iscardresource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource)。
-   說明「狀態衰減至一般」 (請參閱 [使用資源阻礙來同步處理 Direct3D 12) 中的資源狀態](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md) 。
-   [D3D12 的 Helper 結構和](helper-structures-and-functions-for-d3d12.md)函式中所指的 D3dx12 .h 標頭檔，可以直接從[D3D12 Helper 程式庫](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries/D3DX12)下載。

## <a name="august-2016-documentation-update-2"></a>2016年8月檔更新2

-   標題為 [瞭解 D3D12 Debug 層的](understanding-the-d3d12-debug-layer.md)新指南區段。

    在預覽模式中 (三個新的 debug layer 介面) 描述： [**ID3D12Debug1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1)、 [**ID3D12DebugCommandList1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1)、 [**ID3D12DebugDevice1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1)。

## <a name="august-2016-documentation-update-1"></a>2016年8月檔更新1

-   [使用資源阻礙在 Direct3D 12 中同步處理資源狀態](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)的修訂。
-   [多重佇列資源存取](./user-mode-heap-synchronization.md#multi-queue-resource-access)的修訂。

## <a name="windows-10-version-1607"></a>Windows 10 (版本 1607)

這些主題已新增至 Windows 10 1607 版的 Direct3D 檔。

-   [根簽章版本 1.1](root-signature-version-1-1.md) ：已更新之根簽章的總覽，可讓應用程式指定靜態或 volatile 描述元和資料的方式，以協助圖形驅動程式優化。
-   [**ID3D12Device1：： CreatePipelineLibrary**](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-createpipelinelibrary)方法說明建立管線程式庫的優點。
-   有三個新介面 (參考 [介面](interface-hierarchy.md) 階層) ：
    -   [**ID3D12PipelineLibrary**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary)
    -   [**ID3D12Device1**](/windows/win32/api/d3d12/nn-d3d12-id3d12device1)
    -   [**ID3D12VersionedRootSignatureDeserializer**](/windows/win32/api/d3d12/nn-d3d12-id3d12versionedrootsignaturedeserializer)
-   請參閱 [HLSL 著色器模型6.0 總覽](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md)，其中描述多執行緒圖元和計算著色器的 wave 內建作業。
-   [**ID3D12Device：： SetStablePowerState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)的使用已變更。
-   Direct3d 11 的一些新功能會在 [direct3d 11.4 功能](../direct3d11/direct3d-11-4-features.md)中說明。
-   已更新 Direct3D 12 的支援程式庫範圍，請參閱 [direct3d 12 程式設計環境設定](directx-12-programming-environment-set-up.md)的 **支援工具和程式庫** 一節。
-   [使用 DirectX 搭配高動態範圍顯示和進階色彩](../direct3darticles/high-dynamic-range.md)
-   [變數重新整理率顯示](../direct3ddxgi/variable-refresh-rate-displays.md)
-   [DXGI 1.5 改進](../direct3ddxgi/dxgi-1-5-improvements.md)

## <a name="related-topics"></a>相關主題

* [Direct3D 12 程式設計指南](directx-12-programming-guide.md)
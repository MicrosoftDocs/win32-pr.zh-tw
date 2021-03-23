---
title: 硬體功能等級
description: 描述 11 \_ 0 至 12 \_ 1 硬體功能層級的功能。
ms.assetid: B8304E29-A532-464E-8FAF-075228D8FB73
keywords:
- DX 功能等級
- DirectX 功能層級
- 功能等級，DX
- 功能等級，DirectX
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d464f6cc52539e31fee5e234af2c045dfff7e413
ms.sourcegitcommit: 218b1ff779402c3ebe1786679e1aa80a5c0d6c95
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "104548349"
---
# <a name="hardware-feature-levels"></a>硬體功能等級

描述 11 \_ 0 至 12 \_ 1 硬體功能層級的功能。

-   [編號系統](#numbering-systems)
-   [功能層級支援](#feature-level-support)
-   [DXGI 格式的硬體支援](#hardware-support-for-dxgi-formats)
-   [相關主題](#related-topics)

為了處理新電腦和現有電腦的視訊卡多樣性，Microsoft Direct3D 11 引進了功能等級的概念。 每張視訊卡都能根據安裝的圖形處理單位 () Gpu) 功能，來執行特定層級的 Microsoft DirectX (DX。 功能層級是一組定義完善的 GPU 功能。 例如，11 \_ 0 功能層級會執行 Direct3D 11 中所執行的功能。

現在當您建立裝置時，您可以嘗試針對您想要要求的功能層級建立裝置。 如果裝置建立運作，該功能層級則存在，否則，硬體不支援該功能層級。 您可以嘗試重新建立較低功能層級的裝置，或您可以選擇離開應用程式。

功能層級的基本屬性如下：

-   所有 Direct3D 12 驅動程式的功能等級為 11 \_ 0 或更好。
-   允許建立裝置的 GPU 符合或超過該功能等級的功能。
-   功能層級一律包含先前或較低功能層級的功能。
-   功能層級不表示效能，而只是功能。 效能取決於硬體實行。
-   當您呼叫 [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice)時，會選擇一個功能等級。
-   如需支援功能的詳細資訊 (特別是下表中標示為 *選擇性* 的功能，這表示硬體可能會支援該功能，但不需要) 呼叫 [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)。

如需在特定功能層級上建立非硬體類型裝置之限制的相關資訊，請參閱 [建立彎曲和參照裝置的限制](/windows/desktop/direct3d11/overviews-direct3d-11-devices-limitations)。 如需功能層級簡介的詳細資訊，請參閱 [direct3d 功能等級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)上的 direct3d 11 檔。

## <a name="numbering-systems"></a>編號系統

硬體功能層級 *與 API* 版本不同。 例如，有 D3D 11.3 API，但沒有 11 \_ 3 的硬體功能層級。 功能層級是在 [**D3D \_ 功能 \_ 層級**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) 列舉中定義。

有三個不同的編號系統：

-   Direct3D 版本使用句點;例如，Direct3D 12.0。
-   著色器模型使用句號;例如，著色器模型5.1。
-   功能層級使用底線;例如，功能層級 12 \_ 0。

## <a name="feature-level-support"></a>功能層級支援

以下是每個 Direct3D 功能層級的可用功能。

頂端資料列上的標題是 Direct3D 功能等級。 左邊資料行中的標題是功能。



| 功能 \\ 功能等級                                                                                                 | 12 \_ 1 ⁰                    | 12 \_ 0 ⁰                    | 11 \_ 1 ¹                   | 11 \_ 0                    |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------|---------------------------|--------------------------|--------------------------|
| 著色器模型                                                                                                             | 5.1                       | 5.1                       | 5.1 ²                     | 5.1 ²                     |
| [資源系結層](hardware-support.md)                                                                            | 第2層³                    | 第2層³                    | 第1層³                   | 第1層³                   |
| [磚資源](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)                                                                        | 第2層³                    | 第2層³                    | 選用                 | 選用                 |
| [保守的點陣化](conservative-rasterization.md)                                                             | 第1層³                    | 選用                  | 選用                 | 否                       |
| [依轉譯器排序的視圖](rasterizer-order-views.md)                                                                   | 是                       | 選用                  | 選用                 | 否                       |
| [最小/最大篩選](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter)                                                                                      | 是                       | 是                       | 選用                 | 否                       |
| 對應預設緩衝區                                                                                                       | 選用                  | 選用                  | 選用                 | 選用                 |
| [著色器指定的樣板參考值](shader-specified-stencil-reference-value.md)                                 | 選用                  | 選用                  | 選用                 | 否                       |
| [具類型的未排序存取視圖載入](typed-unordered-access-view-loads.md)                                               | 18種格式，更選擇性 | 18種格式，更選擇性 | 3種格式，更選擇性 | 3種格式，更選擇性 |
| [幾何著色器](/previous-versions//bb205146(v=vs.85)) | 是                       | 是                       | 是                      | 是                      |
| [串流輸出](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage)                                            | 是                       | 是                       | 是                      | 是                      |
| [DirectCompute/計算著色器](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader)                                  | 是                       | 是                       | 是                      | 是                      |
| [輪廓和網域著色器](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)                                           | 是                       | 是                       | 是                      | 是                      |
| [材質資源陣列](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-intro)                                     | 是                       | 是                       | 是                      | 是                      |
| [立方體貼圖資源陣列](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-intro)                                     | 是                       | 是                       | 是                      | 是                      |
| [BC1 至 BC7 壓縮](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression)                        | 是                       | 是                       | 是                      | 是                      |
| [Alpha 到涵蓋範圍](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-blend-state)         | 是                       | 是                       | 是                      | 是                      |
| [ (輸出合併的邏輯作業) ](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options)                                          | 是                       | 是                       | 是                      | 選用                 |
| 目標獨立的點陣化                                                                                         | 是                       | 是                       | 是                      | 否                       |
| [多重轉譯目標 (MRT.LOG) 與 ForcedSampleCount 1](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options)                      | 是                       | 是                       | 是                      | 選用                 |
| [僅限 UAV 轉譯的強制樣本計數上限](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options)                            | 16                        | 16                        | 16                       | 8                        |
| 最大材質維度                                                                                                    | 16384                     | 16384                     | 16384                    | 16384                    |
| 最大立方體貼圖維度                                                                                                    | 16384                     | 16384                     | 16384                    | 16384                    |
| 最大磁片區範圍                                                                                                        | 2048                      | 2048                      | 2048                     | 2048                     |
| 最大材質重複                                                                                                       | 16384                     | 16384                     | 16384                    | 16384                    |
| 最大 Anisotropy                                                                                                           | 16                        | 16                        | 16                       | 16                       |
| 最大基本計數                                                                                                      | 2 ^ 32-1                  | 2 ^ 32-1                  | 2 ^ 32-1                 | 2 ^ 32-1                 |
| 最大頂點索引                                                                                                         | 2 ^ 32-1                  | 2 ^ 32-1                  | 2 ^ 32-1                 | 2 ^ 32-1                 |
| 最大輸入位置                                                                                                          | 32                        | 32                        | 32                       | 32                       |
| 同時呈現目標                                                                                              | 8                         | 8                         | 8                        | 8                        |
| 遮蔽查詢                                                                                                        | 是                       | 是                       | 是                      | 是                      |
| 分隔 Alpha Blend                                                                                                     | 是                       | 是                       | 是                      | 是                      |
| 鏡像一次                                                                                                              | 是                       | 是                       | 是                      | 是                      |
| 重迭頂點元素                                                                                              | 是                       | 是                       | 是                      | 是                      |
| 獨立寫入遮罩                                                                                                  | 是                       | 是                       | 是                      | 是                      |
| 實例                                                                                                               | 是                       | 是                       | 是                      | 是                      |



 

-   ⁰需要 Direct3D 11.3 或 Direct3D 12 執行時間。
-   ¹需要 Direct3D 11.1 執行時間。
-   ²著色器模型5.0 可選擇性地支援雙精確度著色器、擴充的雙精確度著色器、 **SAD4** 著色器指令和部分精確度著色器。 若要判斷可用的著色器模型5.0 選項，請呼叫 [**ID3D12Device：： CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)。 某些相容性取決於您執行的硬體：只有支援 DirectX 12 API 的硬體支援著色器模型5.1，不論所使用的功能層級為何。 DirectX 11 硬體最多隻支援著色器模型5.0。 DirectX 12 API 只會往下移至功能等級 11 \_ 0。
-   ³較高的層級是選擇性的。
-   功能層級 12 \_ 0 和 12 \_ 1 需要 direct3d 11.3 或 direct3d 12 執行時間。
-   功能等級 11 \_ 1 需要 Direct3D 11.1 執行時間。
-   功能等級 11 \_ 0 需要 Direct3D 11.0 執行時間。

## <a name="hardware-support-for-dxgi-formats"></a>DXGI 格式的硬體支援

若要查看 DXGI 格式和硬體功能的表格，請參閱：

-   [Direct3D 功能等級12.1 硬體的 DXGI 格式支援](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-1-formats)
-   [Direct3D 功能等級12.0 硬體的 DXGI 格式支援](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-0-formats)
-   [Direct3D 功能等級11.1 硬體的 DXGI 格式支援](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-1-feature-level-hardware)
-   [Direct3D 功能等級11.0 硬體的 DXGI 格式支援](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-0-feature-level-hardware)
-   [Direct3D 10Level9 格式的硬體支援](/previous-versions//ff471324(v=vs.85))
-   [Direct3D 10.1 格式的硬體支援](/previous-versions//cc627091(v=vs.85))
-   [適用于 Direct3D 10 格式的硬體支援](/previous-versions//cc627090(v=vs.85))

## <a name="related-topics"></a>相關主題

<dl> <dt>

[功能查詢](capability-querying.md)
</dt> <dt>

[瞭解 Direct3D 12](directx-12-getting-started.md)
</dt> </dl>

 

 

---
title: 使用 Direct3D 11 功能資料來補充 Direct3D 功能等級
description: 瞭解如何檢查裝置支援的選用功能，包括最近版本的 Windows 中新增的功能。
ms.assetid: 91D9706A-47C5-4220-8AC7-167095E74F74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03c2e7392f576b8c0dca059a4ef2fdd2ee6415230e5fd41e497d60899332f674
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124046"
---
# <a name="using-direct3d-11-feature-data-to-supplement-direct3d-feature-levels"></a>使用 Direct3D 11 功能資料來補充 Direct3D 功能等級

瞭解如何檢查裝置支援的選用功能，包括最近版本的 Windows 中新增的功能。

[Direct3D 功能等級](overviews-direct3d-11-devices-downlevel-intro.md) 表示定義完善的 GPU 功能集，大致上與不同的圖形硬體世代相對應。 這可大幅簡化檢查硬體 capaibilities 的工作，同時也能在各式各樣的不同裝置上提供一致的體驗。

若要考慮各種不同硬體（包括舊版硬體、行動硬體和新式硬體）之間的部分變異數，則會將某些功能視為選擇性。 您可以藉由呼叫 [**ID3D11Device：： CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)並提供相關的 D3D11 \_ 功能 \_ 資料結構，來判斷這些功能的支援 \_ \* 。 本主題說明各種選擇性的 Direct3D 11 功能、這些功能如何搭配運作，以及如何避免檢查每一個選擇性的功能。

## <a name="how-to-check-for-optional-feature-support"></a>如何檢查選用功能支援

呼叫 [**ID3D11Device：： CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)，並提供代表您要使用之選用功能的結構。 如果方法傳回 **S \_ OK**，這表示您是在支援選擇性功能的 Direct3D 執行時間版本上。 如果它傳回 **E \_ INVALIDARG**，表示您是在新增選擇性功能之前的 Direct3D 11 執行時間版本，這表示您無法使用選用功能，以及在相同版本的 Direct3D 11 或更新版本中引進的任何其他選用功能。

## <a name="can-i-minimize-the-work-required-for-feature-support-checks"></a>是否可以將功能支援檢查所需的工作減到最少？

除了具有正確的 Direct3D 11 執行時間 (通常與 Windows 版本相關聯) 圖形驅動程式也必須足以支援選擇性功能。 WDDM 規格需要可支援的選用功能（如果硬體可以支援的話）。 因此，當圖形驅動程式支援在特定版本的 Windows 中新增的其中一項選用功能時，通常表示圖形驅動程式支援該 Windows 版本中新增的其他功能。 例如，如果設備磁碟機支援功能層級9上的陰影，則您知道設備磁碟機至少是 WDDM 1.2。

**注意** 如果 Microsoft Direct3D 裝置支援 [功能層級](overviews-direct3d-11-devices-downlevel-intro.md)11.1，除了 **SAD4ShaderInstructions** 和 **ExtendedDoublesShaderInstructions** 之外，也會自動支援 [**D3D11 \_ 功能 \_ 資料 \_ D3D11 \_ 選項**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options)所指出的所有選用功能。

執行時間一律會以相同方式設定下列成員群組。 也就是說，群組中的所有值都是 **TRUE** 或 **FALSE** ：

-   **DiscardAPIsSeenByDriver** 和 **FlagsForUpdateAndCopySeenByDriver**
-   **ClearView**、 **CopyWithOverlap**、 **ConstantBufferPartialUpdate**、 **ConstantBufferOffsetting** 和 **MapNoOverwriteOnDynamicConstantBuffer**
-   **MapNoOverwriteOnDynamicBufferSRV** 和 **MultisampleRTVWithForcedSampleCountOne**

**功能等級11.2 選項 ([**D3D11 \_ 功能 \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature)) ：** 此欄位所指出的選用功能是獨立的，而且必須個別檢查。

### <a name="feature-support-on-windows-rt-81-and-windows-phone-81-devices"></a>Windows RT 8.1 和 Windows Phone 8.1 裝置上的功能支援

Windows RT 平板裝置可支援各種功能等級和選用功能、已針對減少耗電量進行優化，並使用整合式圖形而非離散 gpu。 Windows適用于 ARM 裝置的儲存應用程式必須支援功能層級9.1。 適用于 Windows RT 的 DirectX 應用程式應該利用可以節省電源和迴圈的選用功能，例如簡單的實例（如果有的話）。

Windows Phone 8 行動裝置支援具有特定選用功能的功能等級9.3。 請參閱[ \_ Windows Phone 8 的 Direct3D 功能等級 9 3](/previous-versions/windows/apps/jj714085(v=vs.105))。

## <a name="what-are-the-direct3d-11-optional-features"></a>什麼是 Direct3D 11 選用功能？

本文的其餘部分將說明 Direct3D 11.2 中可用的選擇性功能。 這些功能會依時間順序來說明，因為它們已加入，因此您可以在不同版本的 Direct3D 11 中取得哪些功能的意義。

## <a name="optional-compute-shader-support-for-feature-level-10"></a>功能層級10的選擇性計算著色器支援

功能層級10裝置一律提供下列功能：

**[**D3D11 \_功能 \_ 資料 \_ D3D10 \_ X \_ 硬體 \_ 選項**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options)：** 若為 **TRUE**，則裝置支援計算著色器。 這包括對原始和結構化緩衝區的支援。

當功能層級 10 \_ 0 或 10 \_ 1 裝置支援這項功能時，不保證裝置支援計算著色器4.1。 如果 [**ID3D11Device：： CreateComputeShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader) 擲回具有計算著色器4.1 程式的例外狀況，則應用程式應該準備好切換回計算著色器4.0。

## <a name="optional-capabilities-for-feature-level-9"></a>功能層級9的選用功能

從 Windows 8 開始，會為功能層級9新增下列功能：

**[**D3D11 \_ 功能 \_ 資料 \_ D3D9 \_ 選項**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options)：** 表示支援包裝紋理定址，但不含2乘冪紋理。 如果支援這種情況，D3D11 \_ 材質 \_ 位址 \_ 模式 \_ WRAP 可用於這類紋理。

**[**D3D11 \_ FEATURE \_ DATA \_ D3D9 \_ SHADOW \_ support**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_shadow_support)：** 表示支援著色器模型4.0 功能層級 9 x 著色器中的比較取樣器 \_ 。 這可用於圖元著色器中的深度測試，以支援一般技術，例如陰影對應和樣板。

針對從 Windows 8.1 開始的功能層級9裝置，已新增下列功能：

**[**D3D11 \_ 功能 \_ 資料 \_ D3D9 \_ 簡單的 \_ 實例 \_ 支援**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_simple_instancing_support)：** 指出可在 DirectX 9 層級硬體上使用的簡單實例功能支援。 簡單實例表示用來定義輸入配置的 [**D3D11 \_ 輸入 \_ 元素 \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_input_element_desc)結構的所有 **InstanceDataStepRate** 成員都必須等於1。 支援功能等級9.3 或更高版本的裝置已包含實例的完整支援。

## <a name="optional-floating-point-precision-support-for-shader-programs"></a>著色器程式的選擇性浮點精確度支援

**[**D3D11 \_ 功能 \_ 資料 \_ 著色器 \_ 最小 \_ 精確度 \_ 支援**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support)：** 此結構中的欄位表示啟用最小有效位數時的浮點數長度，如果只支援完整的32位浮點精確度，則為0。

若為功能層級9裝置，頂點著色器的最小有效位數可以不同于圖元著色器。 頂點著色器的有效位數會在 **AllOtherShaderStagesMinPrecision** 欄位中指出。

**[**D3D11 \_ 功能 \_ 資料 \_ 雙精度**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_doubles)** 浮點數：功能層級11裝置可支援著色器模型5.0 程式內的雙精確度計算。 著色器內的雙精確度計算支援表示浮動可以轉換成計算著色器程式內的雙精度浮點數，以提供每個著色器內更高精確度計算的優點。 在將雙精確度數位寫入輸出緩衝區之前，必須先將其轉換回浮點數。 請注意，不一定要支援雙精確度除法。

## <a name="additional-capabilities-for-direct3d-112"></a>Direct3D 11.2 的其他功能

Direct3D 11.2 新增了可由 Direct3D 11 裝置支援的四個新的選擇性功能。 這些功能位於 [**D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1) 結構中：

**TiledResourcesTier：** 指出支援並排顯示的資源，並指出支援的階層層級。

**MinMaxFiltering：** 指出支援 D3D11 \_ filter 的 \_ 最小值 \_ \* 和 D3D11 \_ 篩選篩選 \_ \_ \* 選項，可將篩選結果與最小 (或最大) 值進行比較。 請參閱 [**D3D11 \_ 篩選**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_filter)。

**ClearViewAlsoSupportsDepthOnlyFormats：** 指出支援清除深度緩衝區資源檢視。

**MapOnDefaultBuffers：** 表示支援以 **D3D11 \_ USAGE \_ DEFAULT** 旗標建立的對應轉譯目標緩衝區。

## <a name="tile-based-rendering"></a>以磚為基礎的轉譯

**[**D3D11 \_ 功能 \_ 資料 \_ 結構 \_ 資訊**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_architecture_info)：** 指出圖形裝置是否批次轉譯命令，並根據預設執行磚型轉譯。 這可以用來做為圖形引擎優化的提示。

## <a name="optional-features-for-development-and-debugging"></a>適用于開發和偵錯工具的選擇性功能

**D3D11 \_功能 \_ 資料 \_ D3D11 \_ 選項：:D iscardapisseenbydriver：** 您可以在開發期間監視此成員，以排除硬體上的舊版驅動程式，也就是 [**DiscardView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) 和 [**DiscardResource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) 可能會有説明。

**[**D3D11 \_ 功能 \_ 資料 \_ 標記 \_ 支援**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_marker_support)：** 如果硬體和驅動程式支援資料標記以進行 GPU 分析，則支援此功能。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[裝置](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 
---
title: Direct3D 11.3 保守的點陣化
description: 保守地柵格化可為圖元轉譯新增一些確定性，這對碰撞偵測演算法特別有用。
ms.assetid: 83F223C0-9282-4149-86CF-471B88829F76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd33b7c7d237fc30adb349f1c1b24ce16c2740ce93fc97445a6e3f69d0949aeb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119408568"
---
# <a name="direct3d-113-conservative-rasterization"></a>Direct3D 11.3 保守的點陣化

保守地柵格化可為圖元轉譯新增一些確定性，這對碰撞偵測演算法特別有用。

-   [概觀](#overview)
-   [與管線的互動](#interactions-with-the-pipeline)
-   [執行詳細資料](#implementation-details)
-   [API 摘要](#api-summary)
-   [相關主題](#related-topics)

## <a name="overview"></a>概觀

保守的點陣化表示所有圖元都是由轉譯的基本型別所涵蓋的所有圖元都是柵格化的，這表示會叫用圖元著色器。 一般行為是取樣，如果已啟用保守的點陣化，則不會使用它。

保守的點陣化在許多情況下都很有用，包括對碰撞偵測、遮蔽剔除和可見度偵測有確定性。

例如，下圖顯示使用保守點陣化所呈現的綠色三角形。 棕色區域稱為「不確定性區域」，這是一個區域，其中舍入錯誤和其他問題會對三角形的精確維度新增一些不確定性。 每個頂點的紅色三角形會顯示不確定性區域的計算方式。 大型灰色方塊會顯示將呈現的圖元。 粉紅色方塊顯示使用「左上角規則」所呈現的圖元，在三角形的邊緣與圖元邊緣相交時，即會開始播放。 可能會有誤報 (的圖元設定，但系統通常不會將其視為系統通常不會進行挑選的) 。

![顯示左上方的規則](images/conservative-rasterization-0.png)

## <a name="interactions-with-the-pipeline"></a>與管線的互動

如需有關保守圖，如何與圖形管線互動的許多詳細資料，請參閱 [D3D12 保守的光柵](/windows/desktop/direct3d12/conservative-rasterization)化。

## <a name="implementation-details"></a>實作詳細資料

Direct3D 12 中支援的光柵類型有時稱為「非常重要保守的點陣化」。 此外，也有「低估的保守點陣化」概念，這表示只有經過轉譯的原始物件完全涵蓋的圖元才會進行柵格化。 您可以透過使用輸入涵蓋範圍資料，透過圖元著色器取得低估的保守點陣化資訊，而且只有非常重要的保守點陣化可作為光柵模式。

如果基本型別的任何部分與圖元重迭，則會將該圖元視為涵蓋範圍，然後再進行柵格化。 當基本的邊緣或角落落在圖元的邊緣或角落時，「左上角規則」的應用程式就會是執行特定的。 不過，對於支援退化三角形的執行，沿著邊緣或角落的退化三角形必須至少涵蓋一個圖元。

保守的點陣化執行會因不同的硬體而異，而且會產生誤報，這表示它們可能會不正確地判斷所涵蓋的圖元。 發生這種情況的原因可能是因為執行特定的詳細資料，例如在柵格化中使用的固定點頂點座標中有基本的成長或貼齊錯誤。 針對固定點頂點座標 (的原因誤報) 有效的原因是，需要某些數量的誤報，才能讓執行作業對貼齊的頂點進行涵蓋範圍評估 (也就是已從浮點數轉換為轉譯器) 所使用16.8 固定點的頂點座標，但接受原始浮點數頂點座標所產生的涵蓋範圍。

保守式的點陣化執行不會對非退化貼齊基本專案的浮點圖元座標產生錯誤否定：如果基本專案的任何部分與圖元的任何部分重迭，則該圖元會進行點陣處理。

為退化 (索引緩衝區中的重複索引或 3D) 中的內建三角形，或在固定點轉換之後變成退化 (在轉譯器) 中的外線頂點，可能或可能不會挑選;兩者都是有效的行為。 退化三角形必須被視為對等，因此，如果應用程式需要特定的行為，則可以使用反面的剔除或測試進行正面測試。 退化三角形會針對所有插入值使用指派給頂點0的值。

除了硬體不支援這項功能的可能性之外，還有三個層級的硬體支援。

-   第1層支援1/2 圖元不確定性區域，而且沒有貼齊會變質。 這適用于並排顯示、紋理塔圖、輕量圖產生和子圖元陰影對應。
-   第2層會新增貼齊會變質和1/256 不確定性區域。 它也新增了支援以 CPU 為基礎的演算法加速 (例如體素化) 。
-   第3層新增1/512 個不確定性區域、內部輸入涵蓋範圍，並支援遮蔽的挑選。 輸入涵蓋範圍會將新值新增 `SV_InnerCoverage` 至高階網底語言 (HLSL) 。 這是一種32位純量整數，可在圖元著色器的輸入上指定，並代表低估的保守式點陣化資訊 (也就是，是否保證) 完全涵蓋圖元。

## <a name="api-summary"></a>API summary

下列方法、結構、列舉和 helper 類別都會參考保守的點陣化：

-   [**D3D11 \_轉譯器 \_ DESC2**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2) ：包含轉譯器描述的結構，請注意 CD3D12 轉譯 \_ \_ 器 DESC2 協助程式類別來建立轉譯器描述。
-   [**D3D11 \_保守 \_ 點陣化 \_ 模式**](/windows/desktop/api/D3D11_3/ne-d3d11_3-d3d11_conservative_rasterization_mode) ：模式的列舉值 (on 或 off) 。
-   [**D3D11 \_功能 \_ 資料 \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) ：保存支援層的結構。
-   [**D3D11 \_保守的 \_ 點陣化 \_ 層**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_conservative_rasterization_tier) ：每個硬體支援層的列舉值。
-   [**ID3D11Device：： CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) ：存取支援功能的方法。

## <a name="related-topics"></a>相關主題
* [Direct3D 11.3 功能](direct3d-11-3-features.md)
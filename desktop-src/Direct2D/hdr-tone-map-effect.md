---
title: HDR 音調地圖效果
description: 此效果會調整影像的動態範圍，使其更符合輸出顯示功能的內容。
ms.topic: article
ms.date: 02/01/2019
ms.openlocfilehash: 4c9234e1b50e155173630a2ff7d94756c5be6130
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843760"
---
# <a name="hdr-tone-map-effect"></a>HDR 音調地圖效果

此效果會調整影像的動態範圍，使其更符合輸出顯示功能的內容。

這項效果的屬性是由 [**D2D1_HDRTONEMAP_PROP 列舉**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_hdrtonemap_prop)識別，而 CLSID 是 **CLSID_D2D1HdrToneMap**。

## <a name="effect-properties"></a>效果屬性

| 顯示名稱和索引列舉 | 類型和預設值 | Description |
|-|-|-|
| InputMaxLuminance、D2D1_HDRTONEMAP_PROP_INPUT_MAX_LUMINANCE | FLOAT | 影像的最大淺色 (或 MaxCLL) ，以 nits。 |
| OutputMaxLuminance、D2D1_HDRTONEMAP_PROP_OUTPUT_MAX_LUMINANCE | FLOAT | 輸出目標所支援的 MaxCLL，通常是在 nits 中 &mdash; 設定為顯示的 MaxCLL。 |
| >displaymode、D2D1_HDRTONEMAP_PROP_DISPLAY_MODE | [**D2D1_HDRTONEMAP_DISPLAY_MODE**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_hdrtonemap_display_mode) | 當設定為 **_HDR** 時，音調對應曲線會調整為更符合一般 HDR 顯示器的行為。 |

## <a name="remarks"></a>備註
的值 `InputMaxLuminance` 通常衍生自影像中繼資料。 如果中繼資料不存在，您可以使用 [Direct2D advanced color image 轉譯範例](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages)中的 **D2DAdvancedColorImagesRenderer：： ComputeHdrMetadata** 函式 () ，以在 nits 中計算影像的最大光源 (MaxCLL) 。

的值 `OutputMaxLuminance` 是設計成使用 [**DXGI_OUTPUT_DESC1：： MaxLuminance**](/windows/desktop/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1)從顯示衍生的。

根據顯示器是 HDR 顯示器或 SDR/WCG 顯示，HDR 色調地圖效果會有不同的色調地圖曲線。

此效果旨在結合 [白色層級調整效果](white-level-adjustment-effect.md) ，可讓您在 Direct2D 中使用適當的色彩管理和色調對應轉譯 HDR 影像。 它是以任何想要提供最多功能的 HDR 影像觀賞體驗來處理所有 Windows HDR 影像格式的架構為目標，並根據顯示 () 的 HDR 或 WCG/SDR 來調整其功能。 這項效果的目的是要依序串連在一起，如下所述。

- 取得輸入影像，其色彩空間由其編解碼器定義。 中繼資料可指定 whitePoint。 中繼資料可指定輸入的亮度等級。
- 套用色彩管理效果。 轉換成 scRGB (CCCS) 空間。
- 套用 HDR 音調地圖效果。 將影像的淺色較低至所需的層級。
- 套用白色層級調整效果。 將影像的白色層級調整為交換鏈所需的白色層級。
- 再次套用色彩管理效果。 如果轉譯為8bpc，則轉換成 sRGB。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-|-|
| 最低支援的用戶端 | Windows 10 版本 1809 (10.0;組建 17763) \[ 桌面應用程式 \| UWP 應用程式\] |
| 標頭 | d2d1effects \_ 2。h |
| 程式庫 | d2d1 .lib，dxguid .lib |

## <a name="related-topics"></a>相關主題

* [ID2D1Effect 介面](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
* [D2D1_HDRTONEMAP_PROP 列舉](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_hdrtonemap_prop)

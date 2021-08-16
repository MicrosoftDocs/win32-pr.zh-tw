---
title: 色彩管理效果
description: 使用色彩管理效果，將影像從一個 ICC (國際色彩協會) 色彩設定檔轉換成另一個。 效果會根據 ICC 規格來轉換影像。
ms.assetid: 7351C4B4-F289-4236-BB42-1B3BD8753248
keywords:
- 色彩管理效果
ms.topic: article
ms.date: 02/05/2019
ms.openlocfilehash: 274591312ab110a24fb315d01f72d23a22a938ad41f380620d94a865602e82a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826696"
---
# <a name="color-management-effect"></a>色彩管理效果

使用色彩管理效果，將影像從一個 ICC (國際色彩協會) 色彩設定檔轉換成另一個。 效果會根據 [ICC 規格](https://www.color.org)來轉換影像。

這項效果的 CLSID 是 CLSID \_ D2D1ColorManagement。

- [效果屬性](#effect-properties)
- [轉譯意圖模式](#rendering-intent-modes)
- [輸入影像 Alpha 模式](#input-image-alpha-modes)
- [符合 ICC 規格](#compliance-with-icc-specification)
- [Alpha 通道行為](#alpha-channel-behavior)
- [品質模式](#quality-modes)
- [範例程式碼](#sample-code)
- [需求](#requirements)
- [相關主題](#related-topics)

## <a name="effect-properties"></a>效果屬性

| 顯示名稱和索引列舉 | 描述 |
|-|-|
| SourceContext<br/> D2D1 \_ COLORMANAGEMENT \_ 的 \_ \_ 內容來源色彩 \_ 內容<br/> | 來源色彩空間資訊。 此類型為 [**ID2D1ColorCoNtext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext)。<br/> 預設值是 NULL。<br/> |
| SourceIntent<br/> D2D1 \_ COLORMANAGEMENT \_ 的 \_ 版本 \_ 轉譯 \_ 意圖<br/> | 要使用哪一種 ICC 轉譯意圖。 此類型為 D2D1 \_ COLORMANAGEMENT \_ 轉譯 \_ 意圖。<br/> 預設值為 D2D1 \_ COLORMANAGEMENT 轉譯 \_ 意圖 \_ 可 \_ 感知。<br/> |
| DestinationCoNtext<br/> D2D1 \_ COLORMANAGEMENT \_ 的 \_ \_ 內容目的地色彩 \_ 內容<br/> | 目的地色彩空間資訊。 此類型為 [**ID2D1ColorCoNtext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext)。<br/> 預設值是 NULL。<br/> |
| DestinationIntent<br/> D2D1 \_ COLORMANAGEMENT \_ 的 \_ \_ 外觀轉譯 \_ 意圖<br/> | 要使用哪一種 ICC 轉譯意圖。 此類型為 D2D1 \_ COLORMANAGEMENT \_ 轉譯 \_ 意圖。<br/> 預設值為 D2D1 \_ COLORMANAGEMENT 轉譯 \_ 意圖 \_ 可 \_ 感知。<br/> |
| AlphaMode<br/> D2D1 \_ COLORMANAGEMENT \_ 的 \_ ALPHA \_ 模式<br/> | 如何解讀輸入影像中包含的 Alpha 資料。 此類型為 D2D1 \_ COLORMANAGEMENT \_ ALPHA \_ 模式。<br/> 預設值是預乘的 D2D1 \_ COLORMANAGEMENT \_ ALPHA \_ 模式 \_ 。<br/> |
| 品質<br/> D2D1 \_ COLORMANAGEMENT \_ 的 \_ 品質<br/> | 轉換的品質等級。 此類型為 D2D1 \_ COLORMANAGEMENT \_ QUALITY。<br/> 預設值為 D2D1 \_ COLORMANAGEMENT \_ QUALITY \_ NORMAL。<br/> |

## <a name="rendering-intent-modes"></a>轉譯意圖模式

| 列舉型別 | 描述 |
|-|-|
| D2D1 \_ COLORMANAGEMENT \_ 轉譯 \_ 意圖的 \_ 視覺效果 | 效果會壓縮或展開影像的完整色彩範圍，以填滿裝置的色彩範圍，因此會保留灰色平衡，但不會保留色階的精確度。 |
| D2D1 \_ COLORMANAGEMENT \_ 轉譯 \_ 意圖 \_ 相對 \_ 色度 | 效果會以色調和亮度的可能費用，將色彩的色度保留在影像中。 |
| D2D1 \_ COLORMANAGEMENT \_ 轉譯 \_ 意圖 \_ 飽和度 | 效果會調整輸出裝置呈現的色彩範圍超出最接近可用色彩的色彩。 它不會保留白色點。 |
| D2D1 \_ COLORMANAGEMENT \_ 轉譯 \_ 意圖 \_ 絕對 \_ 色度 | 效果會調整在輸出裝置可轉譯為最接近可轉譯之色彩範圍之外的任何色彩。 效果不會變更其他色彩，並保留白色點。 |

## <a name="input-image-alpha-modes"></a>輸入影像 Alpha 模式

| 列舉型別 | 描述 |
|-|-|
| 預 \_ 乘的 D2D1 COLORMANAGEMENT \_ ALPHA \_ 模式 \_ | 效果會假設 Alpha 模式為預乘。 |
| D2D1 \_ COLORMANAGEMENT \_ ALPHA \_ 模式 \_ 直接 | 效果會假設 Alpha 模式是直接的。 |

## <a name="d2d1_gamma1_g2084-behavior-changes"></a>D2D1_GAMMA1_G2084 行為變更
    
如果您的應用程式使用 [D2D1_GAMMA1_G2084](/windows/desktop/api/d2d1_3/ne-d2d1_3-d2d1_gamma1) 空間，或是使用 2084 (可感知 Quantizer) 色彩空間的其中一個 [DXGI_COLOR_SPACE_TYPE](/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) 列舉值，則應用程式打算使用 HDR 資料。

[**ID2D1DeviceCoNtext5：： CreateColorCoNtextFromSimpleColorProfile**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromsimplecolorprofile(constd2d1_simple_color_profile__id2d1colorcontext1))和 [**ID2D1DeviceCoNtext5：： CreateColorCoNtextFromDxgiColorSpace**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromdxgicolorspace) api 不會考慮該情況;相反地，在 G2084 DeGamma 作業期間，會調整 HDR 內容以納入0-1 範圍。

實際上，在此 gamma 空間中編碼的內容會使用 10000 Nits 的參考 WhiteLevel，通常會在 CCCS 中表示為 10000/80 = 125.0。 因此，為了更有效地加速您的應用程式，此 gamma 轉換最簡單，也就是將亮度調整為125的係數。 從 Windows 10 版本 1809 (10.0;組建 17763) ，色彩管理效果的行為是套用此調整。 這表示，如同開發人員，您不需要將第二個 [白色層級調整效果](white-level-adjustment-effect.md) 套用至管線。

## <a name="compliance-with-icc-specification"></a>符合 ICC 規格

色彩管理效果與 ICC 4.3 規格相容，但有下列限制：

- 效果支援1、3和4個通道色彩空間。
- 效果不支援 ColorSpace 或命名色彩設定檔。

## <a name="alpha-channel-behavior"></a>Alpha 通道行為

一般而言，如果來源影像中沒有任何 Alpha 資料，則效果會將 Alpha 設定為 1 (不透明) ，而且如果目的影像中沒有空間，則會捨棄 Alpha 資料。 此處的表格說明 Alpha 行為。

<table>
<thead>
<tr class="header">
<th>來源 colorspace，像素格式</th>
<th>目的地 colorspace，像素格式</th>
<th>Alpha 行為</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="4">1個通道，R 像素格式 $ {REMOVE} $<br />
</td>
<td>1個通道，R 像素格式</td>
<td> (沒有任何 Alpha 資料) </td>
</tr>
<tr class="even">
<td>1個通道，RGBA 像素格式</td>
<td>Alpha 資料設定為 1 (不透明) </td>

</tr>
<tr class="odd">
<td>3通道，RGBA 像素格式</td>
<td>Alpha 資料設定為 1 (不透明) </td>

</tr>
<tr class="even">
<td>4通道，RGBA 像素格式</td>
<td> (沒有任何 Alpha 資料) </td>

</tr>
<tr class="odd">
<td rowspan="4">1個通道，RGBA 像素格式 $ {REMOVE} $<br />
</td>
<td>1個通道，R 像素格式</td>
<td>已捨棄 Alpha 資料</td>
</tr>
<tr class="even">
<td>1個通道，RGBA 像素格式</td>
<td>Alpha 資料的傳遞</td>

</tr>
<tr class="odd">
<td>3通道，RGBA 像素格式</td>
<td>Alpha 資料的傳遞</td>

</tr>
<tr class="even">
<td>4通道，RGBA 像素格式</td>
<td>已捨棄 Alpha 資料</td>

</tr>
<tr class="odd">
<td rowspan="4">3個通道，RGBA 像素格式 $ {REMOVE} $<br />
</td>
<td>1個通道，R 像素格式</td>
<td>已捨棄 Alpha 資料</td>
</tr>
<tr class="even">
<td>1個通道，RGBA 像素格式</td>
<td>Alpha 資料的傳遞</td>

</tr>
<tr class="odd">
<td>3通道，RGBA 像素格式</td>
<td>Alpha 資料的傳遞</td>

</tr>
<tr class="even">
<td>4通道，RGBA 像素格式</td>
<td>已捨棄 Alpha 資料</td>

</tr>
<tr class="odd">
<td rowspan="4">4個通道，RGBA 像素格式 $ {REMOVE} $<br />
</td>
<td>1個通道，R 像素格式</td>
<td> (沒有任何 Alpha 資料) </td>
</tr>
<tr class="even">
<td>1個通道，RGBA 像素格式</td>
<td>Alpha 資料設定為 1 (不透明) </td>

</tr>
<tr class="odd">
<td>3通道，RGBA 像素格式</td>
<td>Alpha 資料設定為 1 (不透明) </td>

</tr>
<tr class="even">
<td>4通道，RGBA 像素格式</td>
<td> (沒有任何 Alpha 資料) </td>

</tr>
</tbody>
</table>

## <a name="quality-modes"></a>品質模式

| [模式] | 描述 |
|-|-|
| D2D1 \_ COLORMANAGEMENT \_ 品質 \_ 證明 | 最低品質模式。 此模式需要功能層級 9 \_ 1 或以上。 |
| D2D1 \_ COLORMANAGEMENT \_ 品質 \_ 正常 | 標準品質模式。 此模式需要功能層級 9 \_ 1 或以上。 |
| D2D1 \_ COLORMANAGEMENT \_ 品質 \_ 最佳 | 最佳品質模式。 此模式需要功能層級 10 \_ 0 或以上，以及浮點精確度緩衝區。 此模式支援浮點精確度，以及在 ICC 4.3 規格中定義的延伸範圍。 |

當應用程式要求的品質模式不受硬體支援時，色彩管理效果會失敗。 您可以在呼叫 [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice)時判斷功能等級。 您可以藉由呼叫 [**ID2D1EffectCoNtext：： IsBufferPrecisionSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isbufferprecisionsupported) 與值 [**D2D1 \_ 緩衝區有效 \_ 位數 \_ 32BPC \_ FLOAT**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_buffer_precision)來檢查浮點緩衝區支援。

## <a name="sample-code"></a>範例程式碼

如需此效果的範例，請下載 [Direct2D 效果相片調整範例](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)，並參閱範例的第4課。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-|-|
| 最低支援的用戶端 | Windows 7 傳統型應用程式的 Windows 8 和平臺更新 \[ \| Windows 儲存應用程式\] |
| 最低支援的伺服器 | Windows 7 傳統型應用程式的 Windows 8 和平臺更新 \[ \| Windows 儲存應用程式\] |
| 標頭 | d2d1effects。h |
| 程式庫 | d2d1 .lib，dxguid .lib |

## <a name="related-topics"></a>相關主題

* [ID2D1Effect 介面](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)

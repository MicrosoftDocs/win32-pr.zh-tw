---
title: 白色色調地圖效果
description: 此效果可讓影像的白色層級以線性方式調整。 當您在顯示參考的亮度空間和場景參考的亮度空間之間轉換時，這會特別有用，反之亦然。
ms.topic: article
ms.date: 02/01/2019
ms.openlocfilehash: 646ad47ad671618f29d1691878de93b5e5141855787c53fdad44025487835ad4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119292628"
---
# <a name="white-level-adjustment-effect"></a>白色層級調整效果

此效果可讓影像的白色層級以線性方式調整。 當您在顯示參考的亮度空間和場景參考的亮度空間之間轉換時，這會特別有用，反之亦然。

這項效果的屬性是由 [**D2D1_WHITELEVELADJUSTMENT_PROP 列舉**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_whiteleveladjustment_prop)識別，而 CLSID 是 **CLSID_D2D1WhiteLevelAdjustment**。

## <a name="effect-properties"></a>效果屬性

| 顯示名稱和索引列舉 | 類型和預設值 | 描述 |
|-|-|-|
| InputWhiteLevel、D2D1_WHITELEVELADJUSTMENT_PROP_INPUT_WHITE_LEVEL | FLOAT | 輸入影像的白色層級，以 nits。 |
| OutputWhiteLevel、D2D1_WHITELEVELADJUSTMENT_PROP_OUTPUT_WHITE_LEVEL | FLOAT | 輸出影像的白色層級（nits）。 |

## <a name="remarks"></a>備註
這項效果的目的是要結合 [HDR 語氣地圖效果](hdr-tone-map-effect.md) ，讓您在 Direct2D 中使用適當的色彩管理和色調對應來轉譯 HDR 影像。 如需詳細資訊，請參閱該主題的 **備註** 。 這些效果的目標是想要提供最多功能的 hdr 影像觀賞體驗，以處理所有 Windows hdr 影像格式，並適應顯示 (是否) hdr 或 WCG/SDR 的架構。

在 Windows 上，會假設所有的 SDR/WCG 內容都在顯示參考的亮度空間中，表示內容的白色層級應該在顯示的白色層級向上擴充，然後才會呈現。 不過，這不一定會讓您的應用程式負責進行此作業。 相反地，HDR 內容會假設在場景參考的亮度空間中，這表示它最後不應調整以符合顯示器的白色層級。 也就是說，在某些情況下，您的應用程式可能需要在轉譯 HDR 內容時執行調整，以確保這是淨結果。

當 Windows 桌面處於 SDR 或 WCG 模式時，桌面會以顯示參考的亮度空間組成。 但是，如果 Windows desktop 處於 HDR 模式，則桌面電腦群組合會在場景參考的亮度空間中進行。 話雖如此，桌面視窗管理員 (DWM) 本身會執行亮度調整， (通常稱為8位組合表面的 SDRBoost) ，可簡化應用程式的情況。 即使是這樣，自動提升也表示您的應用程式從一個亮度空間轉換到另一個亮度空間的角色，取決於您的應用程式用來呈現其內容的組合格式。

下表描述您的應用程式應該和不應執行白色層級調整的案例，以及該調整的大小。 一般而言，調整取決於三個因素。

1. 輸入內容 colorspace。 您的輸入內容是否包含高動態範圍 (HDR) 亮度值。 WCG 內容的行為與 SDR 相同，適用于亮度行為。
2. 組合格式。 呈現給 DWM 的目標介面的像素格式 &mdash; ，例如 [交換鏈](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) 或 [複合表面](/uwp/api/Windows.UI.Composition.ICompositionSurface)。 使用 Direct2D 轉譯時，這可能是 **UINT8** 或 **FP16**。
3. 桌面 advanced 色彩模式。 DWM 是在目前顯示的 SDR、WCG 或 HDR 模式中執行。 透過 [**DXGI_OUTPUT_DESC1：： ColorSpace**](/windows/desktop/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1) 或 [**AdvancedColorInfo. CurrentAdvancedColorKind**](/uwp/api/windows.graphics.display.advancedcolorinfo.currentadvancedcolorkind)取得此資訊。

根據這三個因素，您應該針對和屬性設定適當的 `InputWhiteLevel` 值 `OutputWhiteLevel` 。

|輸入內容|組合格式|Advanced color 模式|InputWhiteLevel|OutputWhiteLevel|
|-|-|-|-|-|
|SDR/WCG|**UINT8**|任意|N/A|N/A|
|SDR/WCG|**FP16**|SDR/WCG|N/A|N/A|
|SDR/WCG|**FP16**|HDR|SDRWhite|80|
|HDR|任意|SDR/WCG|80|[**DXGI_OUTPUT_DESC1：： MaxLuminance**](/windows/desktop/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1)|
|HDR|**UINT8**|HDR|80|SDRWhite|
|HDR|**FP16**|HDR|N/A|N/A|

在資料表中，值80是適用于 sRGB 或 scRGB 內容的參考白色層級（以 nits）。 若要這樣做，您可以使用[](/windows/desktop/direct2d/direct2d-constants)在中定義的常數 D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL `d2d1effects_2.h` 。 此值 `SDRWhite` 是顯示器應用來顯示白色 sRGB 內容的 nits 數目。 您可以藉由存取 [**AdvancedColorInfo. SdrWhiteLevelInNits**](/uwp/api/windows.graphics.display.advancedcolorinfo.sdrwhitelevelinnits) 屬性來取得此值。 值 N/A 表示此案例中不會使用白色層級調整;您可以從圖形中移除效果，或設定無作業的值。

請注意，在應用程式不需要白色層級調整的情況下，DWM 或顯示可能會處理從顯示參考的亮度空間轉換成場景參考的亮度空間的轉換。

- 在 SDR/WCG 模式中，轉換會在 DWM 組合之後進行，並套用至顯示的所有內容。 顯示會以隱含方式執行這種轉換。
- 在 HDR 模式中，在撰寫之前，DWM 會自動執行轉換，只要您的應用程式組合介面為 SDR 即可。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-|-|
| 最低支援的用戶端 | Windows 10 版本 1809 (10.0;組建 17763) \[ 桌面應用程式 \| UWP 應用程式\] |
| 標頭 | d2d1effects \_ 2。h |
| 程式庫 | d2d1 .lib，dxguid .lib |

## <a name="related-topics"></a>相關主題

* [ID2D1Effect 介面](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
* [D2D1_WHITELEVELADJUSTMENT_PROP 列舉](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_whiteleveladjustment_prop)

---
description: VMR 中的座標組應
ms.assetid: f0821b90-51d1-4e77-8aed-04337a3dd623
title: VMR 中的座標組應
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad128e4d4e40fe3141f0b23edde1e06df8c5044e0a9877e2d9a2fcc3f293a9fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073788"
---
# <a name="coordinate-mapping-in-the-vmr"></a>VMR 中的座標組應

本節說明在 VMR 將其對應至最終輸出影像之前，套用至來源映射的五個轉換。

1.  轉換 *T (Src)* 將來源矩形對應至目的地矩形。 這些是由媒體類型中 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)或 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)結構的 **rcSource** 和 **rcTarget** 成員所指定。 此對應會在傳遞至 VMR 時，將來源影像進行前置處理。
2.  轉換 *T (旗標)* 執行媒體範例中的旗標所指定的任何影像操作。 這些包含的轉換（例如垂直轉譯和尺規）可容納 bob 交錯旗標。 交錯轉換會將影像高度加倍，而且可能會將影像轉譯成非奇數位段中的一半的影片線。
3.  轉換 *T (AR)* 會根據影像外觀比例，將影像調整為正方形圖元。 針對 **VIDEOINFOHEADER** 媒體類型，外觀比例取決於影像大小。 針對 **VIDEOINFOHEADER2** 類型，外觀比例取決於 **dwPictAspectRatioX** 和 **dwPictAspectRatioY** 欄位，除非 \_ \_ 已設定 AMCONTROL PAD to \_ 16x9 或 AMCONTROL \_ PAD \_ to \_ 4x3 旗標。 這項轉換假設監視器顯示設定符合監視的實體外觀比例。 例如，如果使用者具有具有 4 x 3 外觀比例的監視器，但將顯示器設定為 1280 x 768 圖元 (5 x 3) ，則影像將沒有正確的外觀比例。
4.  轉換 *T (混合)* 轉換會使用 [**IVMRMixerControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) 方法中指定的正規化矩形，在目的影像內放置影像。 正規化的矩形可讓應用程式組織來來源資料流的放置和縮放方式（相對於彼此）。 VMR 藉由計算所有來源影像的最大尺寸，並將每個影像集中在整體周框內，來計算目的影像。 周框的邊角會被指派範圍 (0，0) 至 (1，1) 。 在圖形執行之前，周框是固定的，而且即使已新增或刪除資料流程，也會維持不變。 每個資料流程的目的地矩形可以位於範圍 (0、0) 至 (1、1) ，而且仍然有效。
5.  最後，混合影像的一部分可以由對應 *T (Dst)*（由 VMR 的 [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) 介面中的來源和目的地矩形所指定）進行轉換。 如果 Allocator-Presenter 已被取代，而且未使用 **IBasicVideo** 介面，應用程式必須執行 [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) 介面，並將座標組應回2d 線性空間。 傳回至 DVD 導覽器的滑鼠座標也必須在此空間中。 例如，如果應用程式將影片轉譯為旋轉立方體，則會回報無視窗控制項的整個顯示，並傳回相對於顯示器的滑鼠座標。

從來源資料到最終轉譯器的整體影像轉換如下：

T = T (Src) \* t (旗標) T (Ar) t (混合) \* t (Dst) \*

其中 \* 指出映射可以裁剪至該階段的目的地影像。 請注意，這些都是仿射轉換，所以 VMR 可以將它們合併成單一轉換。

轉換的反向為：

![反向轉換](images/vmrmapping-t-1.png)

 (Src 的因數 T) T (旗標) T (Ar) 相對於來源解析。 在因數 T (混合) 中，正規化來源矩形相對於外觀更正影像。 正規化的目的地矩形相對於輸出解析度。 下圖顯示這些關聯性。

![映射轉換步驟](images/vmrmapping-transform-steps.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[針對 DirectShow 濾波器開發人員使用 VMR](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 




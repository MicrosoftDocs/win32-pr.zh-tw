---
description: Windows Vista 中的 DVD 播放增強功能
ms.assetid: b3cf043f-c974-4240-8291-5c717bd8afaa
title: Windows Vista 中的 DVD 播放增強功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 159056d2c7acaec18a73a30b21f79bcd6267ca33
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970080"
---
# <a name="dvd-playback-enhancements-in-windows-vista"></a>Windows Vista 中的 DVD 播放增強功能

本章節說明 Windows Vista 中 DVD 播放和流覽的改進。

**指定解碼器**

在舊版的 DirectShow 中，建立 DVD 播放圖形時，很難指定特定的 MPEG-2 解碼器。 從 Windows Vista 開始，應用程式可以指定解碼器，如下所示：

1.  在呼叫 [**IDvdGraphBuilder：： RenderDvdVideoVolume**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume)之前，先將此解碼器新增至圖形。
2.  呼叫 **RenderDvdVideoVolume** 並設定 AM \_ DVD 不 \_ \_ \_ 清除旗標。 DVD 導覽器會為您新增的解碼器提供喜好設定。

**增強型影片轉譯器的支援**

建議針對 Windows Vista 或更新版本所撰寫的應用程式使用 [**增強型影片**](enhanced-video-renderer-filter.md) 轉譯器 (EVR) 播放影片。 若要在 DVD 播放應用程式中使用 EVR，請在 \_ 呼叫 RenderDvdVideoVolume 時，設定 AM DVD \_ EVR \_ ONLY 旗標。 

若要在建立圖形之前設定 EVR，請呼叫 [**IDvdGraphBuilder：： GetDvdInterface**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getdvdinterface) ，然後查詢 **IEVRFilterConfig** 或 **IMFVideoRenderer** 介面。  (這些介面記載于媒體基礎 SDK 檔集 ) 。如需有關在 DVD 播放圖形中設定影片轉譯器的詳細資訊，請參閱 [建立 Dvd 篩選圖形](building-the-dvd-filter-graph.md)。

除非解碼器的 [**IAMDecoderCaps：： GetDecoderCaps**](/windows/desktop/api/Strmif/nf-strmif-iamdecodercaps-getdecodercaps) 方法傳回 AM \_ GETDECODERCAP \_ QUERY \_ EVR \_ SUPPORT 旗標，否則 DVD 導覽器不會使用 EVR。 定義此旗標是為了確保應用程式與現有的解碼器相容。 如果 **RenderDvdVideoVolume** 無法使用 AM \_ DVD \_ EVR 旗標，則會在沒有旗標的 \_ 情況下再次呼叫方法，以切換回另一個影片轉譯器。

**順暢地反向播放**

DVD 導覽器現在可以執行流暢的反向播放。 在流暢的反向播放中，DVD 導覽器會將整個影片物件單位 (VOBUs) 傳送給解碼器，而解碼器會以反向順序發出畫面格。 這項功能需要這些解碼器支援順利反向播放。

當應用程式將播放速度設定為負值時，DVD 導覽器會查詢 [**AM \_ 速率 \_ ReverseMaxFullDataRate**](am-rate-reversemaxfulldatarate-property.md) 屬性的解碼器。 這個屬性的值是最大反向速度 x 10000 的絕對值。 例如，如果最大的反向速度是-2.0，則此值為20000。

如果影片解碼支援屬性，則 DVD 導覽器會使用順暢的反向播放。 如果音訊解碼支援屬性，則會反轉播放音訊串流;否則，音訊串流會靜音。 如果影片解碼器不支援屬性，或播放速率超過影片解碼器的最大反向速率，則 DVD 導覽器會切換至 *掃描模式*。 在掃描模式中，DVD 導覽器只會將畫面格傳送至解碼器，並卸載所有 B 和 P 框架。

在流暢的反向播放期間，DVD 導覽器會將完整的 VOBUs 傳送至該解碼器。 DVD 導覽器會以反向順序傳送 VOBUs，但會以其正常順向順序傳送每個 VOBU 中的框架。 在每個 VOBU 的開頭，DVD 導覽器會在 \_ 此範例上設定 AM ReverseBlockStart 旗標。 在 VOBU 結束時，DVD 導覽器會傳送含有 AM ReverseBlockEnd 旗標的空白範例 \_ 。 若要取得這些旗標，請在範例上呼叫 [**IMediaSample2：： GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) 。 旗標是設定在 [**AM \_ sample2.xml \_ 屬性**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties)結構的 **dwTypeSpecificFlags** 成員中。

此解碼器會快取影片資料，直到收到具有 AM ReverseBlockEnd 旗標的範例 \_ 。 屆時，解碼器會以反向順序傳遞已解碼的框架。 例如，如果 VOBU 1 包含畫面格1–4，而 VOBU 2 包含框架5–8，則 DVD 導覽器會依下列順序傳送框架：

 (區塊開始) F5 F6 F7 F8 (區塊結束)  (區塊開始) F1 F2 F3 F4 (區塊結束) 

此解碼器應該會處理框架，如下所示：

1.  解碼 VOBU 2。
2.  輸出畫面格： F8 F7 F6 F5
3.  解碼 VOBU 1。
4.  輸出框架： F4 F3 F2 F1

DVD 導覽器會在此範例) 的 VOBU (F1 和 F5 中的第一個範例上設定時間戳記，但時間戳記會包含區塊開頭的呈現時間，因此，此時間戳記應該將此時間套用到區塊中的最後一個樣本 (F4 和 F8) 。 呈現時間會在反向播放期間增加。

一般而言，VOBU 最多可包含42的框架，而且可能包含多個圖片群組 (GOP) 。 為了讓整個 VOBU 進行解碼，解碼器應該快取已解碼的 I 和 P 框架。 Dvd 上的 VOBUs 不會 Gop 關閉，因此 GOP 內的 B 框架可能需要解碼先前 GOP 中的所有參考框架。 如果此解碼器沒有足夠的表面來保存所有已解碼的框架，可能需要重新解碼選取的框架。

**速率變更**

根據預設，DVD 導覽器會在速率變更之間排清圖形。 但是，如果此解碼器支援 [**AM \_ RATE \_ ResetOnTimeDisc**](am-rate-resetontimedisc-property.md) 屬性，則 DVD 導覽器不會排清圖形，因此可在播放速率之間進行更順暢的轉換。

無論實際的播放速度為何，DVD 導覽器一律會以最快的速度來戳記播放範例以達1x。 此解碼器必須調整已解碼樣本上的時間戳記，以符合實際的播放速度。  (如需詳細資訊，請參閱 [**AM \_ RATE \_ SimpleRateChange 屬性**](am-rate-simpleratechange-property.md)。 ) 如此一來，當您以低於1x 的速度播放時，經過解碼的框架上的時間戳記就會與編碼的框架上的時間戳記分離開來。 只要 DVD 導覽器 \_ \_ 在範例上設定 AM 範例 TIMEDISCONTINUITY 旗標，該解碼器就應該重新同步處理它的時間戳記。 換句話說，已解碼的框架應該具有與輸入框架相同的時間戳記。 若要取出 AM \_ 範例 \_ TIMEDISCONTINUITY 旗標，請在範例上呼叫 [**IMediaSample2：： GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) 。 旗標是設定在 [**AM \_ sample2.xml \_ 屬性**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties)結構的 **dwSampleFlags** 成員中。

**電源管理**

在 Windows Vista 中，DVD 導覽器可對電源管理進行下列改善：

-   更高的計時器解析度
-   較大的資料快取

**計時器解析度**：應用程式可以藉由呼叫 **timeBeginPeriod** 函式來要求最小計時器解析度。 較高的解析度 (較短的期間) 會提高系統對週期性事件的回應，例如超時，但也會增加執行緒內容切換的頻率。

根據預設，DirectShow 中的參考時鐘會將計時器解析度設定為1毫秒。 在該解析度上，CPU 將不會進入任何省電模式。 從 Windows Vista 開始，DVD 導覽器會藉由在參考時鐘上呼叫 [**IReferenceClockTimerControl：： SetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-setdefaulttimerresolution) ，來覆寫參考時鐘的預設行為。 這會移除時鐘對1毫秒計時器解析度的要求。 這可能會讓 CPU 進入省電模式。

計時器解析度是全域設定;Windows 挑選要求的最低值。 影片混合轉譯器 (VMR) 篩選 (VMR-7 和 VMR-9) 將計時器解析度設定為1毫秒。 EVR 通常會將解析度設定為4到8毫秒之間的值，取決於是否啟用桌面電腦群組合，以及 EVR 是否處於全螢幕模式。 其他應用程式也可能會設定解決方法。

快取 **大小**：應用程式可以 \_ 在 [**IDvdControl2：： SETOPTION**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption)方法中設定 dvd CACHESIZEINMB 選項，以指定 dvd 瀏覽器快取的資料量。 如果應用程式將此旗標設定為大數值 (> 50 MB) ，DVD 光碟機可能會在初始預先提取之後關閉，視硬體而定，這可能會降低耗電量。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DVD 應用程式](dvd-applications.md)
</dt> </dl>

 

 




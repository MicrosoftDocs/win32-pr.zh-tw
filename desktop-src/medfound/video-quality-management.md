---
description: 影片品質管制
ms.assetid: 3617adf2-ed7b-4788-abce-58bc22a14511
title: 影片品質管制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233ccd54cfcb98742abef9a91241e903c07ba549
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943721"
---
# <a name="video-quality-management"></a>影片品質管制

本主題說明 Windows 7 中影片管線的一些改良功能，包括 Microsoft 媒體基礎和 Microsoft DirectShow。

在完美的世界中，不論影片解析度或 CPU/GPU 負載為何，影片都不會有任何問題。 當然，在實際的情況下，影片管線必須能夠處理有限的硬體資源，而且必須以量身打造的方式自訂播放到系統內容。 影片品質管制的目標是：

-   減少瑕疵 (捨棄或延遲的畫面) 。
-   減少記憶體使用量，尤其是在 GPU 中。
-   減少耗電量，尤其是在以電池電源執行的膝上型電腦上。
-   在給定的資源條件約束下，獲得最佳的影像品質。
-   讓影片與音訊保持同步。

其中某些目標相反，特別是在低終端系統上。 一般來說，速度和品質之間會有取捨。 瑕疵比中等減少視覺品質更令人討厭。 電源耗用量的相對重要性隨環境而異;在以電池電力執行的膝上型電腦中，這點非常重要。

在 Windows 7 中，增強型影片轉譯器 (EVR) 具有更佳的影片品質管制支援。 媒體基礎管線和 DirectShow 管線都已更新，可利用這些功能。 使用的方法有兩種：

-   開始播放之前，管線可以根據使用者的電源管理設定和硬體的相關資訊，執行靜態優化。
-   播放開始之後，管線可以根據執行時間效能套用動態優化。

## <a name="quality-management-in-media-foundation"></a>媒體基礎中的品質管制

若要啟用靜態優化，請在解析拓撲之前，先在部分拓撲上設定 [MF \_ 拓撲 \_ 靜態 \_ 播放 \_ 優化](mf-topology-static-playback-optimizations.md) 屬性。 拓撲載入器會在其 [**IMFTopoLoader：： Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) 方法中查詢此屬性。

如果您啟用靜態優化，則應該在拓撲上設定兩個其他屬性：



| 屬性                                                                                                                                      | 描述                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="MF_TOPOLOGY_PLAYBACK_MAX_DIMS"></span><span id="mf_topology_playback_max_dims"></span>MF \_ 拓撲 \_ 播放 \_ 最大 \_ 亮度<br/>   | 指定影片播放視窗的大小上限。<br/> |
| <span id="MF_TOPOLOGY_PLAYBACK_FRAMERATE"></span><span id="mf_topology_playback_framerate"></span>MF \_ 拓撲 \_ 播放 \_ 畫面播放速率<br/> | 指定監視器的重新整理頻率。<br/>                      |



 

這兩個屬性可協助管線計算品質管制最有效的設定。

「品質管制員」會執行動態優化。 您不需要採取任何動作來啟用品質管制員;它會自動啟用。 品質管制員存在於 Windows Vista 中;在 Windows 7 中，EVR 可以更妥善地回應品質管制員的訊息。

## <a name="quality-management-in-directshow"></a>DirectShow 中的品質管制

DirectShow 支援 DVD 播放的靜態和動態優化。 若要在 DVD 播放應用程式中啟用這些優化，請在 **IDvdGraphBuilder：： RenderDvdVideoVolume** 方法的 *dwFlags* 參數中設定下列旗標：



| 旗標                  | 描述                    |
|-----------------------|--------------------------------|
| 上午 \_ DVD \_ 調整 \_ 圖形 | 啟用靜態優化。  |
| AM \_ DVD \_ EVR \_ QOS     | 啟用動態優化。 |



 

其他的 DirectShow 應用程式可以直接在 EVR 篩選上呼叫 [**IEVRFilterConfigEx：： SetConfigPrefs**](/windows/desktop/api/evr/nf-evr-ievrfilterconfigex-setconfigprefs) 方法來啟用動態優化。 指定 **EVRFilterConfigPrefs \_ EnableQoS** 旗標。

> [!Note]  
> DirectShow 中的靜態優化僅限於 DVD 播放。

 

## <a name="quality-management-in-the-evr"></a>EVR 中的品質管制

EVR 支援一些新的設定旗標來進行品質管制。 如果您啟用先前所述的品質管制優化，則不需要直接設定這些旗標。 不過，它們會針對想要更細微地控制 EVR 的應用程式記載。

藉由呼叫 [**IMFVideoMixerControl2：： SetMixingPrefs**](/windows/desktop/api/evr/nf-evr-imfvideomixercontrol2-setmixingprefs) 方法，在 EVR 混音器上設定下列旗標：



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Flags</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><strong>MFVideoMixPrefs_ForceHalfInterlace</strong></li>
<li><strong>MFVideoMixPrefs_AllowDropToHalfInterlace</strong></li>
</ul></td>
<td>略過每個交錯框架的第二個欄位。</td>
</tr>
<tr class="even">
<td><ul>
<li><strong>MFVideoMixPrefs_AllowDropToBob</strong></li>
<li><strong>MFVideoMixPrefs_ForceBob</strong></li>
</ul></td>
<td>使用 bob 去交錯，即使驅動程式支援較高品質的交錯模式也是如此。</td>
</tr>
</tbody>
</table>



 

藉由呼叫 [**IMFVideoDisplayControl：： SetRenderingPrefs**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setrenderingprefs) 方法，在 EVR 展示者上設定下列旗標：



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Flags</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><strong>MFVideoRenderPrefs_ForceOutputThrottling</strong></li>
<li><strong>MFVideoRenderPrefs_AllowOutputThrottling</strong></li>
</ul></td>
<td>節流輸出以符合 GPU 頻寬。</td>
</tr>
<tr class="even">
<td><ul>
<li><strong>MFVideoRenderPrefs_ForceBatching</strong></li>
<li><strong>MFVideoRenderPrefs_AllowBatching</strong></li>
</ul></td>
<td>Batch Direct3D 目前的呼叫。 這種優化可讓系統更頻繁進入閒置狀態，進而降低耗電量。</td>
</tr>
<tr class="odd">
<td><ul>
<li>MFVideoRenderPrefs_ForceScaling</li>
<li>MFVideoRenderPrefs_AllowScaling</li>
</ul></td>
<td>使用小於輸出矩形的矩形來執行混合的影片。 將結果調整為正確的輸出大小。</td>
</tr>
</tbody>
</table>



 

此外，EVR 媒體接收器還支援對應至每個旗標的設定屬性：

-   [EVRConfig \_ AllowBatching](evrconfig-allowbatching.md)
-   [EVRConfig \_ AllowDropToBob](evrconfig-allowdroptobob.md)
-   [EVRConfig \_ AllowDropToHalfInterlace](evrconfig-allowdroptohalfinterlace.md)
-   [EVRConfig \_ AllowScaling](evrconfig-allowscaling.md)
-   [EVRConfig \_ AllowDropToThrottle](evrconfig-allowdroptothrottle.md)
-   [EVRConfig \_ ForceBatching](evrconfig-forcebatching.md)
-   [EVRConfig \_ ForceBob](evrconfig-forcebob.md)
-   [EVRConfig \_ ForceHalfInterlace](evrconfig-forcehalfinterlace.md)
-   [EVRConfig \_ ForceScaling](evrconfig-forcescaling.md)
-   [EVRConfig \_ ForceThrottle](evrconfig-forcethrottle.md)

開始播放之前，您可以直接在 EVR 媒體接收上設定這些屬性，做為呼叫 [**IMFVideoMixerControl2**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol2) 和 [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) 方法的替代方法。 若要設定這些屬性，請查詢 EVR 媒體接收器以取得 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體會話](media-session.md)
</dt> </dl>

 

 





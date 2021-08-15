---
description: 事件通知碼
ms.assetid: 339ffcd9-7724-4c92-b241-afbed81d9380
title: 事件通知碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54792e433535ceefad416033d7758f4398b7777951173256c9be9b83913d61f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015786"
---
# <a name="event-notification-codes"></a>事件通知碼

這幾節列出並非 DVD 專用的 DirectShow 事件。 如需 DVD 的特定事件，請參閱 [Dvd 事件通知碼](dvd-notification-codes.md)。

篩選準則會藉由呼叫 [**IMediaEventSink：： Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify)方法，將事件傳送至篩選 Graph 管理員。 篩選 Graph 管理員會處理一些事件，並將應用程式的其他事件排在佇列中。 應用程式會藉由呼叫 [**IMediaEvent：： GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) 方法來抓取它們。

在接下來的各節中，每個專案會列出事件程式碼、事件參數的意義，以及事件 Graph 管理員的預設動作（如果有的話）。 若要覆寫預設動作，請呼叫 [**IMediaEvent：： CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling)。 事件代碼會定義在標頭檔 Evcode .h 和 Audevcod 中。 如果沒有預設動作，則篩選 Graph 管理員會透過事件佇列) ，自動將事件轉送至應用程式 (。

**自訂事件**

篩選準則可以定義事件代碼範圍為 EC \_ 使用者及更高範圍的自訂事件。 篩選 Graph 管理員會直接將這些專案放在事件佇列中。 但是，下列注意事項適用：

-   篩選 Graph 管理員無法使用一般 [**IMediaEvent：： FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams)方法釋放事件參數。 應用程式必須釋放任何與事件參數相關聯的記憶體或參考計數。
-   篩選器只應從已準備處理事件的應用程式中傳送事件。  (可能的應用程式可以設定篩選器上的自訂屬性，以表示可以安全地傳送事件。 ) 



| 事件通知碼                                                 | Description                                                                                                               |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**EC \_ 啟用**](ec-activate.md)                                     | 正在啟用或停用影片視窗。                                                                         |
| [**EC \_ BANDWIDTHCHANGE**](ec-bandwidthchange.md)                       | 不支援。                                                                                                            |
| [**EC \_ 緩衝 \_ 資料**](ec-buffering-data.md)                        | 圖形正在緩衝處理資料，或已停止緩衝資料。                                                               |
| [**EC \_ 建**](ec-built.md)                                           | 在建立圖表時由影片控制項傳送。 未轉送至應用程式。                                     |
| [**EC \_ 時鐘 \_ 已變更**](ec-clock-changed.md)                          | 參考時鐘已變更。                                                                                          |
| [**EC \_ 時鐘未設定 \_**](ec-clock-unset.md)                              | 時鐘提供者已中斷連線。                                                                                      |
| [**EC \_ CODECAPI \_ 活動**](ec-codecapi-event.md)                        | 由編碼器傳送以發出編碼事件。                                                                           |
| [**EC \_ 完成**](ec-complete.md)                                     | 已轉譯特定資料流程中的所有資料。                                                                      |
| [**EC \_ CONTENTPROPERTY \_ 已變更**](ec-contentproperty-changed.md)      | 不支援。                                                                                                            |
| [**EC \_ 裝置 \_ 遺失**](ec-device-lost.md)                              | 隨插即用裝置已移除或已再次變成可用。                                                         |
| [**EC \_ 顯示 \_ 已變更**](ec-display-changed.md)                      | 顯示模式已變更。                                                                                             |
| [**EC \_ 結尾 \_ 的 \_ 區段**](ec-end-of-segment.md)                       | 已到達區段的結尾。                                                                                    |
| [**EC \_ EOS \_ 即將推出**](ec-eos-soon.md)                                    | 不支援。                                                                                                            |
| [**EC \_ 錯誤 \_ STILLPLAYING**](ec-error-stillplaying.md)                | 執行圖形的非同步命令失敗。                                                                      |
| [**EC \_ ERRORABORT**](ec-errorabort.md)                                 | 作業已中止，因為發生錯誤。                                                                             |
| [**EC \_ ERRORABORTEX**](ec-errorabortex.md)                             | 作業已中止，因為發生錯誤。                                                                             |
| [**EC \_ EXTDEVICE \_ 模式 \_ 變更**](ec-extdevice-mode-change.md)         | 不支援。                                                                                                            |
| [**EC \_ 檔案 \_ 已關閉**](ec-file-closed.md)                              | 因為發生未預期的事件，所以已關閉原始程式檔。                                                                |
| [**EC \_ 全螢幕 \_ 遺失**](ec-fullscreen-lost.md)                      | 影片轉譯器正在切換至全螢幕模式。                                                                  |
| [**EC \_ 圖形 \_ 已變更**](ec-graph-changed.md)                          | 篩選圖形已變更。                                                                                             |
| [**EC \_ 長度 \_ 已變更**](ec-length-changed.md)                        | 來源的長度已變更。                                                                                       |
| [**EC \_ LOADSTATUS**](ec-loadstatus.md)                                 | 開啟網路檔案時，通知應用程式的進度。                                                         |
| [**已 \_ 點擊的 EC 標記 \_**](ec-marker-hit.md)                                | 不支援。                                                                                                            |
| [**EC \_ 需要 \_ 重新開機**](ec-need-restart.md)                            | 篩選器要求重新開機圖形。                                                                       |
| [**EC \_ 新的 \_ PIN**](ec-new-pin.md)                                      | 不支援。                                                                                                            |
| [**EC \_ 通知 \_ 視窗**](ec-notify-window.md)                          | 通知影片轉譯器視窗的篩選。                                                                         |
| [**EC \_ OLE \_ 事件**](ec-ole-event.md)                                  | 篩選準則會將文字字串傳遞至應用程式。                                                                     |
| [**EC \_ 開啟 \_ 檔案**](ec-opening-file.md)                            | 圖形正在開啟檔案，或已完成檔案的開啟。                                                              |
| [**\_ \_ 已變更 EC 元件**](ec-palette-changed.md)                      | 視頻板已變更。                                                                                            |
| [**已 \_ 暫停 EC**](ec-paused.md)                                         | 暫停要求已完成。                                                                                            |
| [**EC \_ 請 \_ 重新開啟**](ec-please-reopen.md)                          | 原始程式檔已變更。                                                                                              |
| [**EC 前置處理 \_ \_ 完成**](ec-preprocess-complete.md)              | 當 [WM ASF 寫入](wm-asf-writer-filter.md) 器篩選器完成 multipass 編碼的前置處理時傳送。 |
| [**EC \_ 處理 \_ 延遲**](ec-processing-latency.md)                | 表示元件花費在處理每個樣本的時間量。                                           |
| [**EC \_ 品質 \_ 變更**](ec-quality-change.md)                        | 圖形正在卸載範例，以提供品質控制。                                                                       |
| [**EC \_ 轉譯 \_ 完成**](ec-render-finished.md)                      | 不支援。                                                                                                            |
| [**EC 重新 \_ 繪製**](ec-repaint.md)                                       | 影片轉譯器需要重新繪製。                                                                                      |
| [**EC \_ 範例 \_ 延遲**](ec-sample-latency.md)                        | 指定元件排程處理範例的進度。                                                  |
| [**\_需要 EC 範例 \_**](ec-sample-needed.md)                          | 從增強型影片轉譯器 (EVR) 篩選要求新的輸入範例。                                                |
| [**EC \_ 清理 \_ 時間**](ec-scrub-time.md)                                | 指定最新框架步驟的時間戳記。                                                                  |
| [**\_ \_ 已開始 EC 區段**](ec-segment-started.md)                      | 已開始新的區段。                                                                                                |
| [**EC \_ 關機 \_**](ec-shutting-down.md)                          | 篩選圖形正在進行終結之前，正在關閉。                                                              |
| [**EC \_ SNDDEV \_ \_ 發生錯誤**](ec-snddev-in-error.md)                     | 音訊捕獲篩選器中發生裝置錯誤。                                                                   |
| [**EC \_ SNDDEV \_ 輸出 \_ 錯誤**](ec-snddev-out-error.md)                   | 音訊轉譯器篩選器中發生裝置錯誤。                                                                  |
| [**EC \_ 耗盡**](ec-starvation.md)                                 | 篩選未收到足夠的資料。                                                                                    |
| [**EC \_ 狀態 \_ 變更**](ec-state-change.md)                            | 篩選圖形的狀態已變更。                                                                                       |
| [**EC \_ 狀態**](ec-status.md)                                         | 包含兩個任意狀態字串。                                                                                    |
| [**EC \_ 步驟 \_ 完成**](ec-step-complete.md)                          | 執行框架逐步執行的篩選器會將指定的框架數目分層。                                            |
| [**\_已開始使用 EC 資料流程 \_ 控制項 \_**](ec-stream-control-started.md)       | 資料流程控制項啟動命令已生效。                                                                          |
| [**EC \_ 資料流程 \_ 控制 \_ 已停止**](ec-stream-control-stopped.md)       | 資料流程控制停止命令已生效。                                                                           |
| [**EC \_ 資料流程 \_ 錯誤 \_ STILLPLAYING**](ec-stream-error-stillplaying.md) | 資料流程中發生錯誤。 資料流程仍在播放中。                                                           |
| [**EC \_ 資料流程 \_ 錯誤 \_ 已停止**](ec-stream-error-stopped.md)           | 資料流程已停止，因為發生錯誤。                                                                                 |
| [**有 EC 時間 \_ 碼 \_ 可用**](ec-timecode-available.md)                | 不支援。                                                                                                            |
| [**EC \_ UNBUILT**](ec-unbuilt.md)                                       | 當圖形已中斷時，由影片控制項傳送。 未轉送至應用程式。                                 |
| [**EC \_ USERABORT**](ec-userabort.md)                                   | 使用者已結束播放。                                                                                         |
| [**EC \_ 影片 \_ 大小 \_ 已變更**](ec-video-size-changed.md)               | 原生影片大小已變更。                                                                                        |
| [**EC \_ VIDEOFRAMEREADY**](ec-videoframeready.md)                       | 您可以使用影片畫面來顯示。                                                                                       |
| [**EC \_ VMR 重新 \_ 連接 \_ 失敗**](ec-vmr-reconnection-failed.md)     | 當它無法接受來自上游解碼器的動態格式變更要求時，由 VMR-7 和 VMR-9 傳送。   |
| [**EC \_ VMR \_ RENDERDEVICE \_ 集**](ec-vmr-renderdevice-set.md)           | VMR 已選取其轉譯機制時傳送。                                                                   |
| [**已 \_ 翻轉 EC VMR \_ 介面 \_**](ec-vmr-surface-flipped.md)             | 當 VMR 7's 配置器展示者在呈現的介面上呼叫 DirectDraw Flip 方法時傳送。           |
| [**EC \_ 視窗已 \_ 損毀**](ec-window-destroyed.md)                    | 影片轉譯器已從圖形終結或移除。                                                               |
| [**EC \_ WMT \_ 活動**](ec-wmt-event.md)                                  | 由 WM ASF 讀取器篩選器在讀取受數位版權管理保護的 ASF 檔案 (DRM) 時傳送。                    |
| [**EC \_ WMT \_ 索引 \_ 事件**](ec-wmt-index-event.md)                     | 當應用程式使用 WM ASF 寫入器來編制 Windows Media 視訊檔案的索引時傳送。                                       |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[常數和 Guid](constants-and-guids.md)
</dt> <dt>

[DirectShow 中的事件通知](event-notification-in-directshow.md)
</dt> </dl>

 

 




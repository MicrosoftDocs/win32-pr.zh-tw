---
description: DVD 事件通知碼
ms.assetid: c028918e-aba2-49b2-a6ce-c620ab38b558
title: DVD 事件通知碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e15172e8eba3da048e7c7704a90d7992fa21714a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106967010"
---
# <a name="dvd-event-notification-codes"></a>DVD 事件通知碼

本節列出 DirectShow 中 DVD 播放和流覽的事件通知碼。

如需有關在 DirectShow 中接收事件的詳細資訊，請參閱 [directshow 中的事件通知](event-notification-in-directshow.md)。

如需其他非 DVD 事件的程式碼，請參閱 [事件通知碼](event-notification-codes.md)。



| 事件通知碼                                                        | Description                                                                                                                                                               |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EC \_ DVD \_ 角度 \_ 變更**](ec-dvd-angle-change.md)                          | 表示可用的角度數目變更或目前的角度數位已變更。                                                                      |
| [**EC \_ DVD \_ 角度 \_ 可用**](ec-dvd-angles-available.md)                  | 指出是否現正播放角度區塊，以及是否可以執行角度變更。                                                                                      |
| [**EC \_ DVD \_ 音訊 \_ 串流 \_ 變更**](ec-dvd-audio-stream-change.md)           | 表示主要標題的目前音訊串流號碼已變更。                                                                                                  |
| [**EC \_ DVD \_ BeginNavigationCommands**](ec-dvd-beginnavigationcommands.md)     | 在一組 DVD 流覽命令開始時傳送。                                                                                                                  |
| [**\_ \_ \_ 自動啟用 EC DVD \_ 按鈕**](ec-dvd-button-auto-activated.md)       | 表示已根據光碟上的指示自動啟用功能表按鈕。                                                                                 |
| [**EC \_ DVD \_ 按鈕 \_ 變更**](ec-dvd-button-change.md)                        | 表示可用按鈕的數目已變更，或目前選取的按鈕數目已變更。                                                         |
| [**EC \_ DVD \_ 章節 \_ AUTOSTOP**](ec-dvd-chapter-autostop.md)                  | 指出由於呼叫 [**IDvdControl2：:P laychaptersautostop**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playchaptersautostop) 方法而停止播放。                    |
| [**EC \_ DVD \_ 章節 \_ 入門**](ec-dvd-chapter-start.md)                        | 指示 DVD 導覽器開始在目前的標題中播放新的章節。                                                                                    |
| [**EC \_ DVD \_ CMD \_ 啟動**](ec-dvd-cmd-start.md)                                | 通知特定命令已開始。                                                                                                                              |
| [**EC \_ DVD \_ CMD \_ END**](ec-dvd-cmd-end.md)                                    | 發出特定命令已完成的信號。                                                                                                                          |
| [**EC \_ DVD \_ 目前 \_ HMSF \_ 時間**](ec-dvd-current-hmsf-time.md)               | 在每個影片物件單位的開頭，以 [**DVD \_ HMSF 時間 \_ 碼**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) 格式表示目前的時間， (VOBU) 。                                   |
| [**EC \_ DVD \_ 目前 \_ 時間**](ec-dvd-current-time.md)                          | 發出每個 VOBU 的開頭。                                                                                                                                      |
| [**EC \_ DVD \_ 光碟已 \_ 退出**](ec-dvd-disc-ejected.md)                          | 表示光碟已從磁片磁碟機中取出。                                                                                                                      |
| [**插入的 EC \_ DVD \_ 光碟 \_**](ec-dvd-disc-inserted.md)                        | 表示光碟已插入磁片磁碟機。                                                                                                                     |
| [**EC \_ DVD \_ 網域 \_ 變更**](ec-dvd-domain-change.md)                        | 表示 DVD Navigator 的新網域。                                                                                                                                 |
| [**EC \_ DVD \_ 錯誤**](ec-dvd-error.md)                                         | 發出 DVD 錯誤狀況信號。                                                                                                                                            |
| [**EC \_ DVD \_ GPRM \_ 變更**](ec-dvd-gprm-change.md)                            | 當一般參數的值註冊 (GPRM) 變更時傳送。                                                                                                       |
| [**EC \_ DVD \_ 卡拉卡拉 \_ 模式**](ec-dvd-karaoke-mode.md)                          | 指出導覽器已開始播放或已完成播放卡拉卡拉卡拉的資料。                                                                                   |
| [**EC \_ DVD \_ NavigationCommand**](ec-dvd-navigationcommand.md)                 | 當 Dvd 導覽 [器](dvd-navigator-filter.md) 處理 dvd 流覽命令時傳送。                                                                               |
| [**EC \_ DVD \_ NO \_ FP \_ .PGC**](ec-dvd-no-fp-pgc.md)                               | 表示 DVD 光碟沒有 FP \_ .pgc (第一次播放程式鏈) 。                                                                                           |
| [**EC \_ DVD \_ 家長監護 \_ 層級 \_ 變更**](ec-dvd-parental-level-change.md)       | 表示撰寫內容的家長監護即將變更。                                                                                               |
| [**EC \_ DVD \_ 播放 \_ 速率 \_ 變更**](ec-dvd-playback-rate-change.md)         | 表示已起始播放速率變更，而新的速率在參數中。                                                                            |
| [**EC \_ DVD \_ 播放 \_ 已停止**](ec-dvd-playback-stopped.md)                  | 表示播放已停止。 DVD 導覽器已完成標題的播放，且找不到後續播放的任何其他分支指示。 |
| [**EC \_ DVD \_ PLAYPERIOD \_ AUTOSTOP**](ec-dvd-playperiod-autostop.md)            | 表示導覽器已完成播放 PlayPeriodInTitleAutoStop 呼叫中指定的區段。                                                           |
| [**EC \_ DVD \_ 程式 \_ 儲存格 \_ 變更**](ec-dvd-program-cell-change.md)           | 當 DVD 程式號碼或儲存格編號變更時傳送。                                                                                                                  |
| [**EC \_ DVD \_ 程式 \_ 鏈 \_ 變更**](ec-dvd-program-chain-change.md)         | 當目前的程式鏈 (PGC) 變更時傳送。                                                                                                                            |
| [**EC \_ DVD \_ SPRM \_ 變更**](ec-dvd-sprm-change.md)                            | 當系統參數的值註冊 (SPRM) 變更時傳送。                                                                                                        |
| [**EC \_ DVD \_ 仍 \_ 關閉**](ec-dvd-still-off.md)                                | 表示任何仍然結束的信號。                                                                                                                                             |
| [**EC \_ DVD \_ 仍 \_ 在開啟**](ec-dvd-still-on.md)                                  | 表示任何靜止的開頭。                                                                                                                                       |
| [**EC \_ DVD \_ 子圖片 \_ 串流 \_ 變更**](ec-dvd-subpicture-stream-change.md) | 表示主要標題的目前子圖片串流號碼已變更。                                                                                             |
| [**EC \_ DVD \_ 標題 \_ 設定 \_ 變更**](ec-dvd-title-set-change.md)                 | 當目前的影片標題設定 (VTS) 變更時傳送。                                                                                                                          |
| [**EC \_ DVD \_ 標題 \_ 變更**](ec-dvd-title-change.md)                          | 指出目前的標題編號何時變更。                                                                                                                          |
| [**EC \_ DVD \_ 有效 \_ UOPS \_ 變更**](ec-dvd-valid-uops-change.md)               | 表示 [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) 介面方法的可用集合已變更。                                                                     |
| [**EC \_ DVD \_ VOBU \_ 位移**](ec-dvd-vobu-offset.md)                            | 當 DVD 導覽 [器](dvd-navigator-filter.md) 剖析 PCI 封包時傳送。                                                                                              |
| [**EC \_ DVD \_ VOBU \_ 時間戳記**](ec-dvd-vobu-timestamp.md)                      | 當 DVD 導覽 [器](dvd-navigator-filter.md) 剖析 PCI 封包時傳送。                                                                                              |
| [**EC \_ DVD \_ 警告**](ec-dvd-warning.md)                                     | 發出 DVD 警告條件的信號。                                                                                                                                          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[常數和 Guid](constants-and-guids.md)
</dt> </dl>

 

 




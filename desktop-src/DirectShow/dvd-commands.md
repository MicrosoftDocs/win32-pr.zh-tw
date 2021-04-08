---
description: DVD 命令
ms.assetid: 1204c73e-c3de-4488-8ee3-e76edbf72da0
title: DVD 命令
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5bf06127ab3829ed6cdcbbb70c3b2c1d1b41cf0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688248"
---
# <a name="dvd-commands"></a>DVD 命令

DVD 流覽和播放命令會定義在名為附錄 J 的 DVD 規格區段中，因此，DirectShow 檔通常會參考「附錄 J 命令」。 附錄 J 中提供的名稱不一定很直覺，因此，DirectShow 會使用可能更容易瞭解的名稱。

下表列出附錄 J 命令及其 DirectShow 對等專案。



| 附錄 J 命令                                                                           | Description                                                                  | IDvdControl2 方法                                                                           |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| 標題 \_ 播放                                                                               | 播放標題。                                                                | [**PlayTitle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playtitle)                                                   |
| PLATFORM PTT \_ Play                                                                                 | 在標題中播放章節。                                                   | [**PlayChapterInTitle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playchapterintitle)                                 |
| 時間 \_ 播放                                                                                | 從指定的時間開始播放標題。                                 | [**PlayAtTimeInTitle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playattimeintitle)                                   |
| 停止                                                                                      | 停止播放。                                                               | [**停止**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stop)                                                             |
| 群組                                                                                      | 從子功能表返回父功能表。                                    | [**ReturnFromSubmenu**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-returnfromsubmenu)                                   |
| 時間 \_ 搜尋                                                                              | 在目前標題內的指定時間播放。                           | [**PlayAtTime**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playattime)                                                 |
| PLATFORM PTT \_ 搜尋                                                                               | 在目前的標題內播放一章。                                     | [**PlayChapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playchapter)                                               |
| PrevPG \_ 搜尋                                                                            | 移至上一章的開頭並繼續播放。                 | [**PlayPrevChapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playprevchapter)                                       |
| TopPG \_ 搜尋                                                                             | 移至目前章節的開頭並繼續播放。                  | [**ReplayChapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-replaychapter)                                           |
| NextPG \_ 搜尋                                                                            | 移至下一章的開頭並繼續播放。                     | [**PlayNextChapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playnextchapter)                                       |
| 轉寄 \_ 掃描                                                                             | 以指定的播放速率向前播放。 預設播放速率為1.0。 | [**PlayForwards**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playforwards)                                             |
| 反向 \_ 掃描                                                                            | 以指定的播放速率向前播放。                                  | [**PlayBackwards**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playbackwards)                                           |
| 功能表 \_ 呼叫                                                                                | 顯示功能表。                                                                 | [**ShowMenu**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-showmenu)                                                     |
| 繼續                                                                                    | 從功能表返回並繼續播放。                                      | [**繼續**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-resume)                                                         |
| 上 \_ 按鈕選取 \_ 、下方 \_ 按鈕 \_ 選取、左 \_ 按鈕 \_ 選取、右邊 \_ 按鈕 \_ 選取 | 選取其位置相對於目前選取之按鈕的按鈕。 | [**SelectButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectbutton)                                             |
| 按鈕 \_ 啟用                                                                          | 啟動選取的按鈕。                                                | [**ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton)                                         |
| 按鈕 \_ 選取 \_ 並 \_ 啟用                                                             | 選取並啟用按鈕。                                                | [**SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton)                       |
| 仍 \_ 關閉                                                                                | 顯示靜止影像時繼續播放。                               | [**StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff)                                                     |
| 暫停 \_ 于                                                                                 | 暫停播放。                                                              | [**暫停**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-pause)                                                           |
| 暫停 \_                                                                                | 從暫停的狀態繼續播放。                                       | [**暫停**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-pause)                                                           |
| 功能表 \_ 語言 \_ 選取                                                                    | 選取功能表的語言。                                               | [**SelectDefaultMenuLanguage**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectdefaultmenulanguage)                   |
| 音訊 \_ 串流 \_ 變更                                                                     | 設定音訊串流。                                                        | [**SelectAudioStream**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectaudiostream)                                   |
| 子圖片 \_ 資料流程 \_ 變更                                                               | 設定子圖片資料流程;啟用或停用子圖片顯示。             | [**SelectSubpictureStream**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectsubpicturestream)                         |
| 角度 \_ 變化                                                                             | 設定相機角度。                                                        | [**SelectAngle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectangle)                                               |
| 父 \_ 層級 \_ 選取                                                                   | 設定 [家長] 層級。                                                      | [**SelectParentalLevel**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectparentallevel)                               |
| 家長 \_ 監護 \_ 選取                                                                 | 設定 [家長管理] 的國家/地區。                              | [**SelectParentalCountry**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectparentalcountry)                           |
| 卡拉卡拉 \_ 音訊 \_ 簡報 \_ 模式 \_ 變更                                                | 設定卡拉卡拉的音訊混合模式。                                       | [**SelectKaraokeAudioPresentationMode**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectkaraokeaudiopresentationmode) |
| 影片 \_ 簡報 \_ 模式 \_ 變更                                                         | 將長寬比模式設定為寬螢幕、黑邊或平移掃描。             | [**SelectVideoModePreference**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectvideomodepreference)                   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DVD 應用程式](dvd-applications.md)
</dt> </dl>

 

 




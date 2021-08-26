---
description: MSWebDVD 事件
ms.assetid: e43ea4ad-8ebe-4096-a9f3-a8f618b46877
title: MSWebDVD 事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e61a37eda7b8c2ebafc704d96195cc9e92e70fbd9d8bfda4aa7c971cd890e41c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042708"
---
# <a name="mswebdvd-events"></a>MSWebDVD 事件

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

> [!Note]  
> 此 API 即將淘汰。 如需 DirectShow dvd 播放和流覽的相關資訊，請參閱[dvd 應用程式](dvd-applications.md)。

 

MSWebDVD Microsoft® ActiveX®控制項會在發生各種類型的內部事件或在光碟上遇到特定資訊時，通知您的應用程式。

大部分的事件都與使用者作業 (UOP) 控制項相關。 DVD 作者可以將光碟編碼，以便隨時都可以停用任何 DVD 命令 (例如 **PlayForwards**、 **Pause**、 **ShowMenu** 等) 。 例如，大部分的光碟都不會讓使用者在 FBI 警告現正播放時，向前快轉或顯示功能表。 出現警告之後，光碟會允許這些作業。 藉由處理 UOP 事件，您的應用程式可以更新其使用者介面，以向使用者顯示光碟目前允許的命令。最常見的方法是停用按鈕。 例如，如果您的應用程式收到 PlayForwards 事件， **bEnabled** 設定為 **FALSE**，您可以停用 [播放] 按鈕。 當它收到 **bEnabled** 設為 **TRUE** 的事件時，您可以再次啟用此按鈕。

有三個事件與 UOP 控制項無關。 **DVDNotify** 事件會通知您應用程式有許多不同類型的 DVD 相關事件，這些事件會在 *EventCode* 參數中識別。 某些事件在 *Param1* 和 *Param2* 參數中有其他資訊。 **ReadyStateChange** 事件會通知您應用程式 MSWebDVD ReadyState 屬性中的變更，這是所有 ActiveX 控制項的通用屬性。 **UpdateOverlay** 事件只有在以無視窗模式裝載 MSWebDVD 時，才會傳送至應用程式。 只有當應用程式在全螢幕模式中的影片矩形上顯示浮動按鈕時，才需要回應此事件。



| 事件                                                                  | 描述                                                                           |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**ChangeCurrentAngle**](changecurrentangle.md)                       | 當光碟啟用或停用變更角度時傳送。                            |
| [**ChangeCurrentAudioStream**](changecurrentaudiostream.md)           | 當光碟啟用或停用變更音訊串流時傳送。                     |
| [**ChangeCurrentSubpictureStream**](changecurrentsubpicturestream.md) | 在 **ChangeCurrentSubpictureStream** 命令啟用或停用時傳送。 |
| [**DVDNotify**](dvdnotify.md)                                         | 通知應用程式有許多不同的 DVD 事件和光碟指令。           |
| [**PauseOn**](pauseon.md)                                             | 當 **暫停** 命令已啟用或停用時傳送。                         |
| [**PlayAtTime**](playattime.md)                                       | 在 **PlayAtTime** 命令啟用或停用時傳送。                    |
| [**PlayAtTimeInTitle**](playattimeintitle.md)                         | 在 **PlayAtTimeInTitle** 命令啟用或停用時傳送。             |
| [**PlayBackwards**](playbackwards.md)                                 | 在 **PlayBackwards** 命令啟用或停用時傳送。                 |
| [**PlayChapter**](playchapter.md)                                     | 在 **PlayChapter** 命令啟用或停用時傳送。                   |
| [**PlayChapterInTitle**](playchapterintitle.md)                       | 在 **PlayChapterInTitle** 命令啟用或停用時傳送。            |
| [**PlayForwards**](playforwards.md)                                   | 在 **PlayForwards** 命令啟用或停用時傳送。                  |
| [**PlayNextChapter**](playnextchapter.md)                             | 在 **PlayNextChapter** 命令啟用或停用時傳送。               |
| [**PlayPrevChapter**](playprevchapter.md)                             | 在 **PlayPrevChapter** 命令啟用或停用時傳送。               |
| [**PlayTitle**](playtitle.md)                                         | 在 **PlayTitle** 命令啟用或停用時傳送。                     |
| [**ReadyStateChange**](readystatechange.md)                           | 當 MSWebDVD 控制項的 **ReadyState** 屬性變更時傳送。            |
| [**ReplayChapter**](replaychapter.md)                                 | 在 **ReplayChapter** 命令啟用或停用時傳送。                 |
| [**繼續**](resume.md)                                               | 當 **Resume** 命令已啟用或停用時傳送。                        |
| [**ReturnFromSubmenu**](returnfromsubmenu.md)                         | 在 **ReturnFromSubmenu** 命令啟用或停用時傳送。             |
| [**SelectOrActivatButton**](selectoractivatbutton.md)                 | 當光碟啟用或停用功能表按鈕的選取專案或啟用時傳送。   |
| [**ShowMenu**](showmenu.md)                                           | 當光碟啟用或停用顯示功能表時傳送。                         |
| [**StillOff**](stilloff.md)                                           | 在 **StillOff** 命令啟用或停用時傳送。                      |
| [**停止**](stop.md)                                                   | 當 **停止** 命令已啟用或停用時傳送。                          |
| [**UpdateOverlay**](updateoverlay.md)                                 | 在重迭表面已移動或調整大小，或其色彩索引鍵已變更時傳送。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[MSWebDVD 物件](mswebdvd-object.md)
</dt> </dl>

 

 




---
title: Player 物件
description: Player 物件是 Windows Media Player 控制項的根物件。 它支援下表所列的屬性、方法和事件。
ms.assetid: 694bd6cc-c816-478a-87b9-1526e2d18869
keywords:
- Player 物件 Windows Media Player
topic_type:
- apiref
api_name:
- Player Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0bdf6443557477c15497a36d4976b13d0cfea2fc
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2019
ms.locfileid: "104507653"
---
# <a name="player-object"></a>Player 物件

Player 物件是 Windows Media Player 控制項的根物件。 它支援下表所列的屬性、方法和事件。

Player 物件支援下列屬性。 以星號 () 標記的屬性 \* 無法供面板存取。



| 屬性                                             | 描述                                                                                                                                  |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [cdromCollection](player-cdromcollection.md)        | 抓取 [CdromCollection](cdromcollection-object.md) 物件。                                                                          |
| [closedCaption](player-closedcaption.md)            | 抓取 [ClosedCaption](closedcaption-object.md) 物件。                                                                              |
| [控制](player-controls.md)                      | 抓取 [控制項](controls-object.md) 物件。                                                                                        |
| [currentMedia](player-currentmedia.md)              | 指定或抓取目前的 [媒體](media-object.md) 物件。                                                                         |
| [currentPlaylist](player-currentplaylist.md)        | 指定或抓取目前的 [播放清單](playlist-object.md) 物件。                                                                   |
| [Dvd](player-dvd.md)                                | 抓取 [DVD](dvd-object.md) 物件。                                                                                                  |
| [enableCoNtextMenu](player-enablecontextmenu.md)\* | 指定或抓取值，指出是否要啟用操作功能表，這會在按下滑鼠右鍵時顯示。          |
| [已啟用](player-enabled.md)\*                     | 指定或抓取值，指出是否已啟用 Windows Media Player 控制項。                                               |
| [error](player-error.md)                            | 捕獲 [Error](error-object.md) 物件。                                                                                              |
| [全螢幕](player-fullscreen.md)\*               | 指定或抓取值，指出是否以全螢幕模式播放影片內容。                                          |
| [isOnline](player-isonline.md)                      | 抓取值，指出使用者是否已連接到網路。                                                                     |
| [isRemote](player-isremote.md)\*                   | 抓取值，指出 Windows Media Player 控制項是否正在遠端模式中執行。                                             |
| [mediaCollection](player-mediacollection.md)        | 抓取 [MediaCollection](mediacollection-object.md) 物件。                                                                          |
| [network](player-network.md)                        | 抓取 [Network](network-object.md) 物件。                                                                                          |
| [openState](player-openstate.md)                    | 抓取值，指出內容來源的狀態。                                                                                |
| [playerApplication](player-playerapplication.md)\* | 當遠端 Windows Media Player 控制項正在執行時，會抓取 [PlayerApplication](playerapplication-object.md) 物件。               |
| [playlistCollection](player-playlistcollection.md)  | 抓取 [PlaylistCollection](playlistcollection-object.md) 物件。                                                                    |
| [playState](player-playstate.md)                    | 抓取值，指出 Windows Media Player 操作的狀態。                                                                |
| [設定](player-settings.md)                      | 抓取 [Settings](settings-object.md) 物件。                                                                                        |
| [status](player-status.md)                          | 抓取值，指出 Windows Media Player 的目前狀態。                                                                     |
| [stretchToFit](player-stretchtofit.md)\*           | 指定或抓取值，指出影片是否會延展以符合 Windows Media Player 控制項影片顯示的大小。          |
| [uiMode](player-uimode.md)\*                       | 指定或抓取值，指出當 Windows Media Player 內嵌在網頁中時，使用者介面中所顯示的控制項。 |
| [URL](player-url.md)                                | 指定或抓取要播放之剪輯的名稱。                                                                                         |
| [versionInfo](player-versioninfo.md)                | 抓取指定 Windows Media Player 版本的字串值。                                                                 |
| [windowlessVideo](player-windowlessvideo.md)\*     | 指定或抓取值，指出 Windows Media Player 控制項是否以無視窗模式呈現影片。                         |



 

\* 無法存取外觀。

Player 物件支援下列方法。



| 方法                                | 描述                                               |
|---------------------------------------|-----------------------------------------------------------|
| [close](player-close.md)             | 釋放 Windows Media Player 資源。                  |
| [launchURL](player-launchurl.md)     | 將 URL 傳送給使用者的預設瀏覽器，以進行轉譯。 |
| [newMedia](player-newmedia.md)       | 建立新的 [媒體](media-object.md) 物件。           |
| [[]](player-newplaylist.md) | 建立新的 [播放清單](playlist-object.md) 物件。     |
| [openPlayer](player-openplayer.md)   | 使用指定的 URL 開啟 Windows Media Player。       |



 

Player 物件支援下列事件。 以星號 () 標記的事件 \* 無法供面板存取。 如需在面板中處理滑鼠和鍵盤事件的相關資訊，請參閱 [外來事件](external-events.md)。



| 事件                                                                                            | 描述                                                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [AudioLanguageChange](player-player-audiolanguagechange.md)                                     | 發生于目前的音訊語言變更時。                                  |
| [緩衝處理](player-player-buffering.md)                                                         | 當 Windows Media Player 控制項開始或結束緩衝時發生。           |
| [CdromMediaChange](player-player-cdrommediachange.md)                                           | 從 CD 或 DVD 光碟機插入或退出 CD 或 DVD 時發生。      |
| [按一下](player-player-click.md) \*                                                              | 發生于使用者按一下滑鼠按鍵時。                                      |
| [CurrentItemChange](player-player-currentitemchange.md)                                         | 發生于 *控制項* 時。**currentItem** 變更。                                  |
| [CurrentMediaItemAvailable](player-player-currentmediaitemavailable.md)                         | 發生于目前媒體專案中的圖形中繼資料專案變成可用時。 |
| [CurrentPlaylistChange](player-player-currentplaylistchange.md)                                 | 發生于目前的播放清單中發生某個變更時。                       |
| [CurrentPlaylistItemAvailable](player-player-currentplaylistitemavailable.md)                   | 發生于目前的播放清單專案變成可用時。                         |
| **中斷連線**                                                                                   | 保留供未來使用。                                                         |
| [DomainChange](player-player-domainchange.md)                                                   | 發生于 DVD 網域變更時。                                              |
| [DoubleClick](player-player-doubleclick.md)\*                                                  | 發生于使用者按兩下滑鼠按鍵時。                               |
| **DurationUnitChange**                                                                           | 保留供未來使用。                                                         |
| **EndOfStream**                                                                                  | 保留供未來使用。                                                         |
| [錯誤](player-player-error.md)                                                                 | 當 Windows Media Player 控制項有錯誤條件時發生。             |
| [KeyDown](player-player-keydown.md) \*                                                          | 發生於按下按鍵時。                                                    |
| [按鍵](player-player-keypress.md)\*                                                        | 發生于按下並放開按鍵時。                                  |
| [KeyUp](player-player-keyup.md) \*                                                              | 發生於放開按鍵時。                                                   |
| [MarkerHit](player-player-markerhit.md)                                                         | 當到達標記時發生。                                                 |
| [MediaChange](player-player-mediachange.md)                                                     | 發生于媒體專案變更時。                                                |
| [MediaCollectionAttributeStringAdded](player-player-mediacollectionattributestringadded.md)     | 當屬性值新增至程式庫時發生。                          |
| [MediaCollectionAttributeStringChanged](player-player-mediacollectionattributestringchanged.md) | 發生于程式庫中的屬性值變更時。                        |
| [MediaCollectionAttributeStringRemoved](player-player-mediacollectionattributestringremoved.md) | 從程式庫移除屬性值時發生。                      |
| [MediaCollectionChange](player-player-mediacollectionchange.md)                                 | 發生于媒體集合變更時。                                        |
| [MediaCollectionMediaAdded](player-player-mediacollectionmediaadded.md)                         | 當媒體專案加入至本機程式庫時發生。                          |
| [MediaCollectionMediaRemoved](player-player-mediacollectionmediaremoved.md)                     | 當媒體專案從本機程式庫中移除時發生。                      |
| [MediaError](player-player-mediaerror.md)                                                       | 發生于 **媒體** 物件有錯誤狀況時。                         |
| [ModeChange](player-player-modechange.md)                                                       | 當 Windows Media Player 模式變更時發生。                           |
| [MouseDown](player-player-mousedown.md)\*                                                      | 發生于按下滑鼠按鍵時。                                           |
| [MouseMove](player-player-mousemove.md)\*                                                      | 發生于移動滑鼠指標時。                                          |
| [MouseUp](player-player-mouseup.md)\*                                                          | 發生于放開滑鼠按鍵時。                                          |
| **NewStream**                                                                                    | 保留供未來使用。                                                         |
| [OpenPlaylistSwitch](player-player-openplaylistswitch.md)                                       | 發生于 DVD 上的標題開始播放時。                                     |
| [OpenStateChange](player-player-openstatechange.md)                                             | 當 Windows Media Player 控制項變更狀態時發生。                      |
| [PlaylistChange](player-player-playlistchange.md)                                               | 當播放清單變更時發生。                                                  |
| [PlaylistCollectionChange](player-player-playlistcollectionchange.md)                           | 發生于播放清單集合中的某些變更時。                        |
| [PlaylistCollectionPlaylistAdded](player-player-playlistcollectionplaylistadded.md)             | 當播放清單新增至播放清單集合時發生。                      |
| [PlaylistCollectionPlaylistRemoved](player-player-playlistcollectionplaylistremoved.md)         | 從播放清單集合移除播放清單時發生。                  |
| **PlaylistCollectionPlaylistSetAsDeleted**                                                       | 保留供未來使用。                                                         |
| [PlayStateChange](player-player-playstatechange.md)                                             | 當 Windows Media Player 控制項的播放狀態變更時發生。          |
| [PositionChange](player-player-positionchange.md)                                               | 當媒體專案目前的位置已變更時發生。             |
| [ScriptCommand](player-player-scriptcommand.md)                                                 | 當收到同步處理的命令或 URL 時發生。                           |
| [StatusChange](player-player-statuschange.md)                                                   | 當 **status** 屬性變更值時發生。                               |
| [StringCollectionChange](player-player-stringcollectionchange.md)                               | 當字串集合變更時發生。                                         |
| **警告**                                                                                      | 保留供未來使用。                                                         |



 

\* 無法存取外觀。 如需有關在外觀中處理滑鼠和鍵盤事件的詳細資訊，請參閱 [環境事件處理常式](ambient-event-handlers.md)。

內嵌在網頁中時，可以使用物件標記中指定的識別碼值來存取 **Player** 物件。 在面板定義檔中，它是使用 **media player** 全域屬性來存取。 為了方便說明，在參考語法區段中，會使用 **player** 作為物件識別碼。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**腳本的物件模型參考**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 





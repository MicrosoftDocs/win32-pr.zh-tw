---
title: AxWindowsMediaPlayer 物件 (VB 和 C)
description: 'AxWindowsMediaPlayer 物件 (VB 和 C \ ) '
ms.assetid: d7eeac20-1afa-4e73-9af6-9772fbb65516
keywords:
- Windows Media Player，AxWindowsMediaPlayer 物件
- Windows Media PlayerMobile、AxWindowsMediaPlayer 物件
- Windows Media Player 物件模型，AxWindowsMediaPlayer 物件
- 物件模型，AxWindowsMediaPlayer 物件
- ActiveX control、AxWindowsMediaPlayer 物件
- Windows Media Player ActiveX control、AxWindowsMediaPlayer 物件
- Windows Media PlayerMobile ActiveX control、AxWindowsMediaPlayer 物件
- 物件模型的參考，AxWindowsMediaPlayer 物件
- AxWindowsMediaPlayer 物件
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1d0c66360e80ea293795442472ce163292c38152baa859889086a5687f03764f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765278"
---
# <a name="axwindowsmediaplayer-object-vb-and-c"></a>AxWindowsMediaPlayer 物件 (VB 和 c # ) 

AxWindowsMediaPlayer 物件是 Windows Media Player 控制項的根物件。 它支援下表所列的屬性、方法和事件。

AxWindowsMediaPlayer 物件支援下列屬性。



| 屬性                                                                             | 描述                                                                                                                        |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [cdromCollection](axwmplib-axwindowsmediaplayer-cdromcollection--vb-and-c.md)       | 取得 **IWMPCdromCollection** 介面。                                                                                         |
| [closedCaption](axwmplib-axwindowsmediaplayer-closedcaption--vb-and-c.md)           | 取得 IWMPClosedCaption 介面。                                                                                               |
| [Ctlcontrols](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md)               | 取得 IWMPControls 介面。                                                                                                    |
| [Ctlenabled](axwmplib-axwindowsmediaplayer-ctlenabled--vb-and-c.md)                 | 取得或設定值，這個值表示是否已啟用 Windows Media Player 控制項。                                               |
| [currentMedia](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)             | 取得或設定對應至目前媒體專案的 IWMPMedia 介面。                                                   |
| [currentPlaylist](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)       | 取得或設定目前的 **IWMPPlaylist** 介面。                                                                               |
| [Dvd](axwmplib-axwindowsmediaplayer-dvd--vb-and-c.md)                               | 取得 IWMPDVD 介面。                                                                                                         |
| [enableCoNtextMenu](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md)   | 取得或設定值，指出是否要啟用操作功能表，這會在按一下滑鼠右鍵時出現。          |
| [錯誤](axwmplib-axwindowsmediaplayer-error--vb-and-c.md)                           | 取得 IWMPError 介面。                                                                                                       |
| [全屏](axwmplib-axwindowsmediaplayer-fullscreen--vb-and-c.md)                 | 取得或設定值，指出是否以全螢幕模式播放影片內容。                                          |
| [isOnline](axwmplib-axwindowsmediaplayer-isonline--vb-and-c.md)                     | 取得值，指出使用者是否已連接到網路。                                                                |
| isRemote                                                                             | 不支援 .NET 程式設計。                                                                                                |
| [mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)       | 取得 IWMPMediaCollection 介面。                                                                                             |
| [網路](axwmplib-axwindowsmediaplayer-network--vb-and-c.md)                       | 取得 IWMPNetwork 介面。                                                                                                     |
| [openState](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md)                   | 取得值，指出內容來源的狀態。                                                                           |
| playerApplication                                                                    | 不支援 .NET 程式設計。                                                                                                |
| [playlistCollection](axwmplib-axwindowsmediaplayer-playlistcollection--vb-and-c.md) | 取得 IWMPPlaylistCollection 介面。                                                                                          |
| [playState](axwmplib-axwindowsmediaplayer-playstate--vb-and-c.md)                   | 取得值，指出 Windows Media Player 操作的狀態。                                                           |
| [設定](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md)                     | 取得 IWMPSettings 介面。                                                                                                    |
| [status](axwmplib-axwindowsmediaplayer-status--vb-and-c.md)                         | 取得值，指出 Windows Media Player 的目前狀態。                                                                |
| [stretchToFit](axwmplib-axwindowsmediaplayer-stretchtofit--vb-and-c.md)             | 取得或設定值，指出影片是否會延展以符合 Windows Media Player 控制項影片顯示的大小。          |
| [uiMode](axwmplib-axwindowsmediaplayer-uimode--vb-and-c.md)                         | 取得或設定值，指出當 Windows Media Player 內嵌在網頁中時，使用者介面中所顯示的控制項。 |
| [URL](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)                               | 取得或設定要播放之剪輯的名稱。                                                                                         |
| [versionInfo](axwmplib-axwindowsmediaplayer-versioninfo--vb-and-c.md)               | 取得值，這個值會指定 Windows Media Player 的版本。                                                               |
| [windowlessVideo](axwmplib-axwindowsmediaplayer-windowlessvideo--vb-and-c.md)       | 取得或設定值，這個值表示 Windows Media Player 控制項是否以無視窗模式呈現影片。                         |



 

AxWindowsMediaPlayer 物件支援下列方法。



| 方法                                                       | 描述                                               |
|--------------------------------------------------------------|-----------------------------------------------------------|
| [close](axwmplib-axwindowsmediaplayer-close.md)             | 釋放 Windows Media Player 資源。                  |
| [launchURL](axwmplib-axwindowsmediaplayer-launchurl.md)     | 將 URL 傳送給使用者的預設瀏覽器，以進行轉譯。 |
| [newMedia](axwmplib-axwindowsmediaplayer-newmedia.md)       | 傳回新媒體專案的 IWMPMedia 介面。      |
| [[]](axwmplib-axwindowsmediaplayer-newplaylist.md) | 傳回新播放清單的 IWMPPlaylist 介面。     |
| [openPlayer](axwmplib-axwindowsmediaplayer-openplayer.md)   | 使用指定的 URL 開啟 Windows Media Player。       |



 

AxWindowsMediaPlayer 物件支援下列事件。



| 事件                                                                                                              | 描述                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [AudioLanguageChange](axwmplib-axwindowsmediaplayer-audiolanguagechange.md)                                       | 發生于目前的音訊語言變更時。                                                            |
| [緩衝處理](axwmplib-axwindowsmediaplayer-buffering.md)                                                           | 當 Windows Media Player 控制項開始或結束緩衝時發生。                                     |
| [CdromBurnError](axwmplib-axwindowsmediaplayer-cdromburnerror.md)                                                 | 在 CD 燒錄操作期間發生一般錯誤時發生。                                         |
| [CdromBurnMediaError](axwmplib-axwindowsmediaplayer-cdromburnmediaerror.md)                                       | 將個別媒體專案燒錄至 CD 時發生錯誤。                               |
| [CdromBurnStateChange](axwmplib-axwindowsmediaplayer-cdromburnstatechange.md)                                     | 當 CD 燒錄操作變更狀態時發生。                                                          |
| [CdromMediaChange](axwmplib-axwindowsmediaplayer-cdrommediachange.md)                                             | 從 CD 或 DVD 光碟機插入或退出 CD 或 DVD 時發生。                                |
| [CdromRipMediaError](axwmplib-axwindowsmediaplayer-cdromripmediaerror.md)                                         | 從 CD 翻錄個別播放軌時發生錯誤。                                  |
| [CdromRipStateChange](axwmplib-axwindowsmediaplayer-cdromripstatechange.md)                                       | 當 CD 翻錄作業變更狀態時發生。                                                          |
| [按一下](axwmplib-axwindowsmediaplayer-click.md)                                                                   | 發生于使用者按一下滑鼠按鍵時。                                                                |
| CreatePartnershipComplete                                                                                          | 不支援 .NET 程式設計。                                                                        |
| [CurrentItemChange](axwmplib-axwindowsmediaplayer-currentitemchange.md)                                           | 發生于 [IWMPControls. currentItem](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md) 變更時。 |
| [CurrentMediaItemAvailable](axwmplib-axwindowsmediaplayer-currentmediaitemavailable.md)                           | 發生于目前媒體專案中的圖形中繼資料專案變成可用時。                           |
| [CurrentPlaylistChange](axwmplib-axwindowsmediaplayer-currentplaylistchange.md)                                   | 發生于目前的播放清單中發生某個變更時。                                                 |
| [CurrentPlaylistItemAvailable](axwmplib-axwindowsmediaplayer-currentplaylistitemavailable.md)                     | 發生于目前的播放清單專案變成可用時。                                                   |
| DeviceConnect                                                                                                      | 不支援 .NET 程式設計。                                                                        |
| DeviceDisconnect                                                                                                   | 不支援 .NET 程式設計。                                                                        |
| DeviceStatusChange                                                                                                 | 不支援 .NET 程式設計。                                                                        |
| DeviceSyncError                                                                                                    | 不支援 .NET 程式設計。                                                                        |
| DeviceSyncStateChange                                                                                              | 不支援 .NET 程式設計。                                                                        |
| [中斷連線](axwmplib-axwindowsmediaplayer-disconnect.md)                                                         | 保留供未來使用。                                                                                   |
| [DomainChange](axwmplib-axwindowsmediaplayer-domainchange.md)                                                     | 發生于 DVD 網域變更時。                                                                        |
| [按兩下](axwmplib-axwindowsmediaplayer-doubleclick.md)                                                       | 發生于使用者按兩下滑鼠按鍵時。                                                         |
| [DurationUnitChange](axwmplib-axwindowsmediaplayer-durationunitchange.md)                                         | 保留供未來使用。                                                                                   |
| [EndOfStream](axwmplib-axwindowsmediaplayer-endofstream.md)                                                       | 保留供未來使用。                                                                                   |
| [錯誤](axwmplib-axwindowsmediaplayer-error.md)                                                                   | 當 Windows Media Player 控制項有錯誤條件時發生。                                       |
| [FolderScanStateChange](axwmplib-axwindowsmediaplayer-folderscanstatechange.md)                                   | 當資料夾監控作業變更狀態時發生。                                                   |
| [KeyDown](axwmplib-axwindowsmediaplayer-keydown.md)                                                               | 發生於按下按鍵時。                                                                              |
| [KeyPress](axwmplib-axwindowsmediaplayer-keypress.md)                                                             | 發生于按下並放開按鍵時。                                                            |
| [KeyUp](axwmplib-axwindowsmediaplayer-keyup.md)                                                                   | 發生於放開按鍵時。                                                                             |
| [LibraryConnect](axwmplib-axwindowsmediaplayer-libraryconnect.md)                                                 | 發生于程式庫變成可用時。                                                                   |
| [LibraryDisconnect](axwmplib-axwindowsmediaplayer-librarydisconnect.md)                                           | 當程式庫不再可用時發生。                                                              |
| [MarkerHit](axwmplib-axwindowsmediaplayer-markerhit.md)                                                           | 當到達標記時發生。                                                                           |
| [MediaChange](axwmplib-axwindowsmediaplayer-mediachange.md)                                                       | 發生于媒體專案變更時。                                                                          |
| [MediaCollectionAttributeStringAdded](axwmplib-axwindowsmediaplayer-mediacollectionattributestringadded.md)       | 當屬性值新增至程式庫時發生。                                                    |
| [MediaCollectionAttributeStringChanged](axwmplib-axwindowsmediaplayer-mediacollectionattributestringchanged.md)   | 發生于程式庫中的屬性值變更時。                                                  |
| [MediaCollectionAttributeStringRemoved](axwmplib-axwindowsmediaplayer-mediacollectionattributestringremoved.md)   | 從程式庫移除屬性值時發生。                                                |
| [MediaCollectionChange](axwmplib-axwindowsmediaplayer-mediacollectionchange.md)                                   | 發生于媒體集合變更時。                                                                  |
| [MediaCollectionMediaAdded](axwmplib-axwindowsmediaplayer-mediacollectionmediaadded.md)                           | 當媒體專案加入至本機程式庫時發生。                                                    |
| [MediaCollectionMediaRemoved](axwmplib-axwindowsmediaplayer-mediacollectionmediaremoved.md)                       | 當媒體專案從本機程式庫中移除時發生。                                                |
| [MediaError](axwmplib-axwindowsmediaplayer-mediaerror.md)                                                         | 發生于 **媒體** 物件有錯誤狀況時。                                                   |
| [ModeChange](axwmplib-axwindowsmediaplayer-modechange.md)                                                         | 當 Windows Media Player 模式變更時發生。                                                     |
| [MouseDown](axwmplib-axwindowsmediaplayer-mousedown.md)                                                           | 發生于按下滑鼠按鍵時。                                                                     |
| [MouseMove](axwmplib-axwindowsmediaplayer-mousemove.md)                                                           | 發生于移動滑鼠指標時。                                                                    |
| [MouseUp](axwmplib-axwindowsmediaplayer-mouseup.md)                                                               | 發生于放開滑鼠按鍵時。                                                                    |
| [NewStream](axwmplib-axwindowsmediaplayer-newstream.md)                                                           | 保留供未來使用。                                                                                   |
| [OpenPlaylistSwitch](axwmplib-axwindowsmediaplayer-openplaylistswitch.md)                                         | 發生于 DVD 上的標題開始播放時。                                                               |
| [OpenStateChange](axwmplib-axwindowsmediaplayer-openstatechange.md)                                               | 當 Windows Media Player 控制項變更狀態時發生。                                                |
| PlayerDockedStateChange                                                                                            | 不支援 .NET 程式設計。                                                                        |
| PlayerReconnect                                                                                                    | 不支援 .NET 程式設計。                                                                        |
| [PlaylistChange](axwmplib-axwindowsmediaplayer-playlistchange.md)                                                 | 當播放清單變更時發生。                                                                            |
| [PlaylistCollectionChange](axwmplib-axwindowsmediaplayer-playlistcollectionchange.md)                             | 發生于播放清單集合中的某些變更時。                                                  |
| [PlaylistCollectionPlaylistAdded](axwmplib-axwindowsmediaplayer-playlistcollectionplaylistadded.md)               | 當播放清單新增至播放清單集合時發生。                                                |
| [PlaylistCollectionPlaylistRemoved](axwmplib-axwindowsmediaplayer-playlistcollectionplaylistremoved.md)           | 從播放清單集合移除播放清單時發生。                                            |
| [PlaylistCollectionPlaylistSetAsDeleted](axwmplib-axwindowsmediaplayer-playlistcollectionplaylistsetasdeleted.md) | 保留供未來使用。                                                                                   |
| [PlayStateChange](axwmplib-axwindowsmediaplayer-playstatechange.md)                                               | 當 Windows Media Player 控制項的播放狀態變更時發生。                                    |
| [PositionChange](axwmplib-axwindowsmediaplayer-positionchange.md)                                                 | 當媒體專案目前的位置已變更時發生。                                       |
| [ScriptCommand](axwmplib-axwindowsmediaplayer-scriptcommand.md)                                                   | 當收到同步處理的命令或 URL 時發生。                                                     |
| [StatusChange](axwmplib-axwindowsmediaplayer-statuschange.md)                                                     | 當 **status** 屬性變更值時發生。                                                         |
| [StringCollectionChange](axwmplib-axwindowsmediaplayer-stringcollectionchange.md)                                 | 當字串集合變更時發生。                                                                   |
| SwitchedToControl                                                                                                  | 不支援 .NET 程式設計。                                                                        |
| SwitchedToPlayerApplication                                                                                        | 不支援 .NET 程式設計。                                                                        |
| [警告](axwmplib-axwindowsmediaplayer-warning.md)                                                               | 保留供未來使用。                                                                                   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**適用于 Visual Basic .net 和 C 的介面#**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**IWMPCdromCollection 介面 (VB 和 c # )**](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption 介面 (VB 和 c # )**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**IWMPControls 介面 (VB 和 c # )**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPDVD 介面 (VB 和 c # )**](iwmpdvd--vb-and-c.md)
</dt> <dt>

[**IWMPError 介面 (VB 和 c # )**](iwmperror--vb-and-c.md)
</dt> <dt>

[**IWMPMedia 介面 (VB 和 c # )**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection 介面 (VB 和 c # )**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork 介面 (VB 和 c # )**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist 介面 (VB 和 c # )**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection 介面 (VB 和 c # )**](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings 介面 (VB 和 c # )**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**Visual Basic .net 和 C 的物件模型參考#**](object-model-reference-for-visual-basic--net-and-c.md)
</dt> <dt>

[**WMPOpenState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpopenstate)
</dt> <dt>

[**WMPPlayState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpplaystate)
</dt> </dl>

 

 





---
title: PLAYER 元素
description: PLAYER 元素
ms.assetid: 009090b3-0055-4700-9078-0749da239674
keywords:
- Windows Media Player 的面板、播放機元素
- 面板、播放機元素
- PLAYER 元素
- 面板的參考、播放程式元素
- 元素，播放者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8bef2e7758a0146ae6197d17dc3790011a758f9d2fa4e3d54af9461a8b870c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338114"
---
# <a name="player-element"></a>PLAYER 元素

**Player** 元素可讓您定義事件處理常式，並在面板定義檔內的設計階段指定 **PLAYER** 物件的 **URL** 屬性。 在腳本程式碼中， **player** 物件是透過 **player** global 屬性來存取，而不是透過由 **player** 元素不支援的 **識別碼** 屬性所指定的名稱來存取。

**PLAYER** 元素支援下列屬性。



| 屬性             | 描述                                          |
|-----------------------|------------------------------------------------------|
| [URL](player-url.md) | 指定或抓取要播放的檔案名。 |



 

**Player** 元素可以針對從 **PLAYER** 物件引發的下列事件，執行事件處理常式。



| 事件                                                                                            | 描述                                                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [AudioLanguageChange](player-player-audiolanguagechange.md)                                     | 發生于目前的音訊語言變更時。                                  |
| [緩衝處理](player-player-buffering.md)                                                         | 當 Windows Media Player 開始或結束緩衝時發生。                       |
| [CdromMediaChange](player-player-cdrommediachange.md)                                           | 當 CD 媒體變更時發生。                                                |
| [CurrentItemChange](player-player-currentitemchange.md)                                         | 發生于目前專案變更時。                                            |
| [CurrentMediaItemAvailable](player-player-currentmediaitemavailable.md)                         | 發生于目前的媒體專案變成可用時。                            |
| [CurrentPlaylistChange](player-player-currentplaylistchange.md)                                 | 發生于目前的播放清單變更時。                                        |
| [CurrentPlaylistItemAvailable](player-player-currentplaylistitemavailable.md)                   | 發生于目前的播放清單專案變成可用時。                         |
| [DomainChange](player-player-domainchange.md)                                                   | 發生于 DVD 網域變更時。                                              |
| [錯誤](player-player-error.md)                                                                 | 當 Windows Media Player 控制項有錯誤條件時發生。             |
| [MarkerHit](player-player-markerhit.md)                                                         | 當 Windows Media Player 在剪輯中遇到標記時發生。                |
| [MediaChange](player-player-mediachange.md)                                                     | 發生于媒體專案變更時。                                                |
| [MediaCollectionAttributeStringAdded](player-player-mediacollectionattributestringadded.md)     | 當屬性值新增至程式庫時發生。                          |
| [MediaCollectionAttributeStringChanged](player-player-mediacollectionattributestringchanged.md) | 發生于程式庫中的屬性值變更時。                        |
| [MediaCollectionAttributeStringRemoved](player-player-mediacollectionattributestringremoved.md) | 從程式庫移除屬性值時發生。                      |
| [MediaCollectionChange](player-player-mediacollectionchange.md)                                 | 當 **MediaCollection** 物件變更時發生。                              |
| [MediaError](player-player-mediaerror.md)                                                       | 發生于 **媒體** 物件有錯誤狀況時。                         |
| [ModeChange](player-player-modechange.md)                                                       | 在隨機和一般模式之間切換時發生。                           |
| [OpenPlaylistSwitch](player-player-openplaylistswitch.md)                                       | 發生于 DVD 上的標題開始播放時。                                     |
| [OpenStateChange](player-player-openstatechange.md)                                             | 發生于 *播放玩家*。**openState** 變更。                                      |
| [PlaylistChange](player-player-playlistchange.md)                                               | 當播放清單變更時發生。                                                  |
| [PlaylistCollectionChange](player-player-playlistcollectionchange.md)                           | 發生于播放清單集合中的某些變更時。                        |
| [PlaylistCollectionPlaylistAdded](player-player-playlistcollectionplaylistadded.md)             | 當播放清單新增至播放清單集合時發生。                      |
| [PlaylistCollectionPlaylistRemoved](player-player-playlistcollectionplaylistremoved.md)         | 從播放清單集合移除播放清單時發生。                  |
| [PlayStateChange](player-player-playstatechange.md)                                             | 發生于 *播放玩家*。**playState** 變更。                                      |
| [PositionChange](player-player-positionchange.md)                                               | 發生于 *播放玩家*。*控制項*。**currentPosition** 變更。                     |
| [ScriptCommand](player-player-scriptcommand.md)                                                 | 當 Windows Media Player 遇到內嵌于檔案中的指令碼命令時發生。 |
| [StatusChange](player-player-statuschange.md)                                                   | 當 **status** 屬性變更值時發生。                               |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Player 物件**](player-object.md)
</dt> <dt>

[**外觀程式設計參考**](skin-programming-reference.md)
</dt> </dl>

 

 





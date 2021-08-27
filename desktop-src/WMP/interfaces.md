---
title: WMP SDK 介面
description: WMP SDK 介面
ms.assetid: 68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd
keywords:
- Windows Media Player，介面
- Windows Media Player行動裝置，介面
- Windows Media Player 物件模型，介面
- 物件模型，介面
- ActiveX 控制項，介面
- Windows Media Player ActiveX 控制項、介面
- Windows Media PlayerMobile ActiveX 控制項、介面
- 物件模型、介面的參考
- 介面物件模型參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7db8e5ebe29e38da9f92370f60a622fad70f36395b271eb7bd86ef49f49a3d49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123498"
---
# <a name="wmp-sdk-interfaces"></a>WMP SDK 介面

本節記載由 Windows Media Player ActiveX 控制項和 Windows Media Player Mobile ActiveX 控制項公開的 COM 介面。

**IWMPCore** 或 **IWMPPlayer** 介面的存取子方法是用來取出特定介面。 這些介面接著可能具有存取子方法，可供您抓取進一步的介面。 只有當您取得介面的基底版本，而且想要在較新版本的相同介面上呼叫方法時，才需要呼叫其中一個介面上的 **QueryInterface** 。

> [!Note]  
> 除非另行明確陳述，否則 Windows Media Player 10 行動版和更新版本中完全支援所有方法和事件。

Windows Media Player 控制項會公開下列介面。

| 介面                                                    | 描述                                                                                                                                                                               |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_WMPOCXEvents](-wmpocxevents-interface.md)                | 提供源自內嵌程式可回應之 Windows Media Player 控制項的事件。                                                                              |
| [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom)                                   | 存取磁片磁碟機中的 CD 或 DVD。                                                                                                                                                          |
| [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)                           | 提供管理音訊 Cd 建立方式的方法。                                                                                                                                            |
| [IWMPCdromCollection](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)               | 存取 CD 或 DVD 光碟機的集合。                                                                                                                                                |
| [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)                             | 提供從音訊 CD 管理複製曲目的方法。                                                                                                                               |
| [IWMPClosedCaption](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpclosedcaption)                   | 包含具有媒體剪輯的標題。                                                                                                                                                      |
| [IWMPClosedCaption2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpclosedcaption2)                 | 提供其他隱藏式字幕方法。                                                                                                                                            |
| [IWMPControls](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols)                             | 代表 Windows Media Player 的傳輸控制項，例如播放、停止和暫停。                                                                                                 |
| [IWMPControls2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols2)                           | 提供額外的控制方法。                                                                                                                                                      |
| [IWMPControls3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols3)                           | 提供額外的控制方法。                                                                                                                                                      |
| [IWMPCore](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore)                                     | 抓取其他介面的指標，並存取控制項的基本功能。 這是 Windows Media Player 物件模型的根介面。                                  |
| [IWMPCore2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore2)                                   | 提供其他核心方法。                                                                                                                                                         |
| [IWMPCore3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore3)                                   | 提供其他核心方法。                                                                                                                                                         |
| [IWMPDVD](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpdvd)                                       | 存取 DVD 的內容功能表。                                                                                                                                                       |
| [IWMPError](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperror)                                   | 存取 [IWMPErrorItem](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperroritem) 指標的集合。                                                                                                                     |
| [IWMPErrorItem](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperroritem)                           | 提供有關錯誤的資訊。                                                                                                                                                        |
| [IWMPErrorItem2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperroritem2)                         | 提供其他錯誤專案方法。                                                                                                                                                   |
| [IWMPEvents](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)                       | 公開源自內嵌程式可回應之 Windows Media Player 控制項的事件。                                                                            |
| [IWMPEvents2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)                     | 公開源自內嵌程式可回應之 Windows Media Player 10 控制項的事件。 這些事件專門用於裝置同步處理常式。 |
| [IWMPEvents3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)                               | 提供與 CD 翻錄、CD 燒錄、資料夾監控和遠端程式庫服務相關的事件。                                                                                        |
| [IWMPFolderMonitorServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)   | 提供方法來列舉、掃描及修改 Windows Media Player 監視數位媒體內容的檔案資料夾。                                                                |
| [IWMPGraphCreation](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpgraphcreation)                   | 管理 DirectShow 圖形。                                                                                                                                                             |
| [IWMPLibrary](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)                               | 代表程式庫。                                                                                                                                                                     |
| [IWMPLibraryServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)               | 提供列舉程式庫的方法。                                                                                                                                                  |
| [IWMPLibrarySharingServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrarysharingservices) | 提供管理程式庫共用的方法。                                                                                                                                               |
| [IWMPMedia](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)                                   | 設定和捕獲媒體專案的屬性。                                                                                                                                        |
| [IWMPMedia2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia2)                                 | 提供其他方法來設定和取出媒體專案的屬性。                                                                                                           |
| [IWMPMedia3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia3)                                 | 提供其他方法來設定和取出媒體專案的屬性。                                                                                                           |
| [IWMPMediaCollection](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection)               | 存取 [IWMPMedia](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) 指標的集合。                                                                                                                             |
| [IWMPMediaCollection2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2)             | 提供補充 **IWMPMediaCollection** 介面的方法。                                                                                                                   |
| [IWMPMetadataPicture](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmetadatapicture)               | 捕獲 **WM/圖片** 中繼資料屬性的相關資訊。                                                                                                                        |
| [IWMPMetadataText](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmetadatatext)                     | 抓取複雜文字中繼資料屬性的相關資訊。                                                                                                                          |
| [IWMPNetwork](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpnetwork)                               | 設定和抓取 Windows Media Player 使用的網路連接屬性。                                                                                                 |
| [IWMPPlayer](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer)                                 | 控制 Windows Media Player 控制項使用者介面的行為。                                                                                                                 |
| [IWMPPlayer2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer2)                               | 提供控制 Windows Media Player 的其他方法。                                                                                                                         |
| [IWMPPlayer3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer3)                               | 提供控制 Windows Media Player 的其他方法。                                                                                                                         |
| [IWMPPlayer4](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer4)                               | 提供控制 Windows Media Player 的其他方法。                                                                                                                         |
| [IWMPPlayerApplication](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerapplication)           | 在遠端 Windows Media Player 控制項和播放程式的完整模式之間切換。 專為將控制項內嵌于遠端模式的 c + + 程式所設計。                          |
| [IWMPPlayerServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)                 | 由遠端控制項的主機用來操作 Windows Media Player 的完整模式。 專為與 c + + 搭配使用所設計。                                                                     |
| [IWMPPlayerServices2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices2)               | 設定背景處理優先權。                                                                                                                                                  |
| [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)                             | 建立及管理播放清單。                                                                                                                                                            |
| [IWMPPlaylistArray](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylistarray)                   | 依索引編號存取 [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist) 指標的集合。                                                                                                       |
| [IWMPPlaylistCollection](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylistcollection)         | 操縱 [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist) 和 [IWMPPlaylistArray](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylistarray) 指標。                                                                                     |
| [IWMPQuery](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)                                   | 表示複合查詢。                                                                                                                                                              |
| [IWMPRemoteMediaServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)       | 提供從裝載播放機控制項的程式中 Windows Media Player 的服務。 專為與 c + + 搭配使用所設計。                                                                        |
| [IWMPRenderConfig](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmprenderconfig)                     | 提供方法來指定或抓取值，指出是否只會在目前的進程中進行播放。                                                                          |
| [IWMPSettings](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings)                             | 設定或抓取 Windows Media Player 設定。                                                                                                                                          |
| [IWMPSettings2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings2)                           | 設定或抓取 Windows Media Player 設定。                                                                                                                                          |
| [IWMPSkinManager](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpskinmanager)                       | 指定搭配 Windows Media Player 使用的外觀。                                                                                                                                        |
| [IWMPStringCollection](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection)             | 存取字串的集合。                                                                                                                                                         |
| [IWMPStringCollection2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2)           | 提供補充 **IWMPStringCollection** 介面的方法。                                                                                                                  |
| [IWMPSyncDevice](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)                         | 代表可將數位媒體檔案與 Windows Media Player 10 同步處理的裝置。                                                                                                |
| [IWMPSyncDevice2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice2)                       | 提供補充 **IWMPSyncDevice** 介面的方法。                                                                                                                      |
| [IWMPSyncServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)                     | 列舉可將數位媒體檔案與 Windows Media Player 10 同步處理的可用裝置。                                                                                       |
| [IWMPTranscodePolicy](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmptranscodepolicy)               | 提供由 DirectShow 來源篩選器所執行的方法，以管理變更數位媒體檔案的格式。                                                                          |
| [IWMPVideoRenderConfig](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig)           | 提供可設定 Windows Media Player 所使用之增強型影片轉譯器的方法。                                                                                               |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**C + + 的物件模型參考**](object-model-reference-for-c.md)
</dt> </dl>

 

 





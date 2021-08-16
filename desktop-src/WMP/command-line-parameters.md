---
title: 命令列參數
description: 命令列參數
ms.assetid: c4af8a03-2cab-4ecd-bbd8-c83869822901
keywords:
- Windows Media Player，參數
- Windows Media Player，命令列參數
- Windows Media Player、Wmplayer
- Windows Media Player、Wmpconfig
- Windows Media Player、Wmpnscfg
- 命令列參數
- Wmplayer
- Wmpconfig
- Wmpnscfg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2240040453bc60a7a03ca56f205643f97202eb840a501fd13aa417b86aef060d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118341948"
---
# <a name="command-line-parameters"></a>命令列參數

## <a name="command-line-parameters-for-wmplayer"></a>Wmplayer 的命令列參數

Windows Media Player 支援一組命令列參數，可指定播放程式啟動時的行為。 下表詳細說明參數和其行為。



| Syntax                                                                                                              | 行為                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 「*路徑 \\ 檔案名*」 (例如： `wmplayer "c:\filename.wma"`) <br/>                                            | 啟動播放玩家並播放該檔案。                                                                                                                                                                                                                                                                                                        |
| "*path \\ filename*"/fullscreen (例如： `wmplayer "c:\filename.wmv" /fullscreen`) <br/>                    | 以全螢幕模式播放指定的檔案。您必須指定要播放之內容的路徑和檔案名。<br/>                                                                                                                                                                                                                     |
| /Device： {DVD \| AudioCD} (例如： `wmplayer /device:audio CD`) <br/>                                         | 播放 DVD 或音訊 CD。                                                                                                                                                                                                                                                                                                                    |
| "*路徑 \\ 檔案名*？WMPSkin =*外觀名稱*"例如： `wmplayer "c:\filename.wma?wmpskin=headspace"`<br/>        | 開啟播放機，套用指定的面板。                                                                                                                                                                                                                                                                                              |
| /Service：*keyname*                                                                                                  | 開啟播放程式，顯示 *keyname* 指定的線上商店。需要 Windows Media Player 10 或更新版本。<br/>                                                                                                                                                                                                                      |
| /Task NowPlaying                                                                                                    | 在 [ **立即播放** ] 功能中開啟播放機。                                                                                                                                                                                                                                                                                            |
| /Task MediaGuide                                                                                                    | 以 Windows Media Player 10 或更新版本) 中 (目前作用中的線上商店，在 **媒體節目表** 功能中開啟播放機。                                                                                                                                                                                                                          |
| /Task CDAudio                                                                                                       | 以 Windows Media Player 10 或 Windows Media Player 11) 中的 [**從 CD 複製**] 功能 ([ **Rip** ] 功能開啟播放機。 Windows Media Player 12 不支援這個參數。                                                                                                                                                       |
| /Task CDWrite                                                                                                       | 在 **燒錄** 功能中開啟播放機。需要 Windows Media Player 10。<br/>                                                                                                                                                                                                                                                       |
| /Task MediaLibrary                                                                                                  | 在 [ **媒體** 櫃] 功能中開啟播放機。                                                                                                                                                                                                                                                                                                |
| /Task RadioTuner                                                                                                    | 在 [**收音機調諧器**] 功能中開啟播放機， (Windows Media Player 10 或更新版本) 中目前有效的線上商店。                                                                                                                                                                                                                          |
| /Task PortableDevice                                                                                                | 在 Windows Media Player 10 或更新版本的) 中，開啟 **複製到 CD 或裝置** 功能 (**同步** 處理功能的播放裝置。                                                                                                                                                                                                                            |
| /Task Services/Service *servicename*                                                                               | 在 [**進階版 Services** ] 功能中開啟播放機，顯示 *servicename* 參數所指定的服務。 此值是服務的唯一名稱。 如果先前未看到指定的服務，則會忽略 *servicename* 參數。  (在 Windows Media Player 10 或更新版本中開啟指定的線上商店。 )  |
| /Task ServiceTask *X*                                                                                                | 在 *X* 所指定的線上商店服務工作窗格中開啟播放機。例如，/Task ServiceTask1 會在第一個線上商店服務工作窗格中開啟播放機。                                                                                                                                                                      |
| /Task SkinViewer                                                                                                    | 在 **外觀選擇器** 功能中開啟播放機。                                                                                                                                                                                                                                                                                           |
| /Playlist *PlaylistName*                                                                                            | 開啟播放機並播放指定的播放清單。                                                                                                                                                                                                                                                                                           |
| /Schema： { \| \| Video Video Other 的音樂圖片） \| \| 例如： `wmplayer /Schema:Pictures /Task:PortableDevice`<br/> | 開啟播放機，並顯示指定的媒體類別目錄。 需要 Windows Media Player 11。                                                                                                                                                                                                                                                   |



 

## <a name="command-line-parameters-for-wmpconfig"></a>Wmpconfig 的命令列參數

Wmpconfig.exe 用來在 Windows Media Player 中執行需要系統管理員許可權的特定命令。 範例包括啟動和停止流覽和共用服務，以及啟用 Windows 防火牆中的例外狀況。 下表描述命令列參數的可能值。



| Syntax                                                                                    | 行為                                                                   |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| DisableHMEDevice *MAC*                                                                    | 停用媒體存取控制 (MAC) 識別碼所指定的裝置。  |
| HMEOff 範例：<br/> wmpconfig HMEOff<br/>                                    | 停用 Windows Media Player 網路共用服務。                 |
| HMEOn 範例：<br/> wmpconfig HMEOn<br/>                                      | 啟用共用、流覽和防火牆例外。                     |
| RemoveHMEDevice *MAC*                                                                     | 移除 MAC 識別碼所指定的裝置。                          |
| RestoreHMEDevice *MAC*                                                                    | 還原 MAC 識別碼所指定的裝置。                         |
| SetDVDParentalLevel *層級* 範例：<br/> wmpconfig SetDVDParentalLevel 3<br/> | 設定 DVD 家長監護層級。 層級會指定為整數。 |



 

## <a name="command-line-parameters-for-wmpnscfg"></a>Wmpnscfg 的命令列參數

Microsoft Windows 會在網路上找到媒體轉譯裝置時，使用 wmpnscfg.exe 來警示使用者。 Wmpnscfg 會啟動 Windows Media Player 網路共用服務 (NSS) 然後等候來自服務的通知。 當 wmpnscfg 收到網路上可用的新媒體裝置時，它會在系統匣中顯示快顯視窗，通知使用者有新裝置的可用性。 如果使用者按一下快顯視窗，wmpnscfg 會啟動 Windows Media Player，此對話方塊會顯示對話方塊，要求使用者允許或拒絕與新裝置共用。

一般來說，Windows 會呼叫 wmpnscfg，而不使用任何命令列參數。 不過，有一個可用的參數，如下表所述。



| 參數 | 行為                         |
|-----------|----------------------------------|
| /Close    | 關閉 wmpnscfg 的所有實例。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Windows Media Player**](windows-media-player.md)
</dt> </dl>

 

 






---
title: 關於資料夾監控
description: 關於資料夾監控
ms.assetid: d3d83e60-ecc7-4501-a6dd-15f7680a6ec9
keywords:
- Windows Media Player，資料夾監控
- Windows Media Player 物件模型，資料夾監控
- 物件模型，資料夾監控
- Windows Media Player ActiveX 控制項、資料夾監控
- ActiveX 控制項，資料夾監控
- Windows Media PlayerMobile ActiveX 控制項，資料夾監控
- Windows Media Player行動、資料夾監控
- 資料夾監控
- 監視資料夾
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1206defcdc387659567ceedcf7347a3ab99ca45d9926a9bd32c4f75280a8a46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055506"
---
# <a name="about-folder-monitoring"></a>關於資料夾監控

Windows Media Player 可以監視包含數位媒體檔案的資料夾，並在新增或移除檔案時更新文件庫。 此資料夾監控功能是由 [IWMPFolderMonitorServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices) 介面提供。

若要使用資料夾監控服務，您必須以遠端狀態建立 Player 物件。 如需遠端處理的詳細資訊，請參閱[遠端處理 Windows Media Player 控制項](remoting-the-windows-media-player-control.md)。 當您建立了播放程式的遠端實例之後，請呼叫 [IWMPPlayer](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer)介面上的 **QueryInterface** 來取得 **IWMPFolderMonitorServices** 介面的指標。

Windows Media Player 會保留受監視的資料夾清單。 若要取得受監視的資料夾清單，請使用 [IWMPFolderMonitorServices：： get \_ Count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_count) 和 [IWMPFolderMonitorServices：： item](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-item) 方法。 若要將資料夾加入清單或從清單中移除它們，請分別使用 [IWMPFolderMonitorServices：： add](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-add) 和 [remove](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-remove) 方法。

**開始掃描**

資料夾的監視通常是不需要明確呼叫的背景進程。 如果您想要主動掃描資料夾，請呼叫 [IWMPFolderMonitorServices：： startScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-startscan)。 您可以使用 [IWMPFolderMonitorServices：： stopScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-stopscan) 方法停止進行中的掃描。

**正在抓取資料夾監控狀態**

**IWMPFolderMonitorServices** 提供的功能可讓您取得資料夾監控程式的狀態。

資料夾掃描是在兩個階段中完成。 在第一次通過時，播放程式會一併掃描 [受監視的資料夾] 清單中所命名的資料夾，並建立要新增至程式庫的檔案清單。 在第二個階段中，它會流覽檔案清單並將檔案新增至程式庫，也會從程式庫移除已從檔案系統中刪除對應實體檔案的任何媒體專案。

[FolderScanStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-folderscanstatechange)事件可用來在玩家切換至新狀態時通知您的程式。 您也可以藉由呼叫 [get \_ scanState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scanstate)來取得目前的狀態。 當第一次行程開始時，會 wmpfssScanning 目前的狀態值。 在第二個階段中，狀態會切換至 wmpfssUpdating。 程式完成後，狀態會變更為 wmpfssStopped。

當播放程式在第一次行程掃描受監視的資料夾時，請呼叫 [get \_ scannedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scannedfilescount) 來檢查已掃描的檔案數目。 [Get \_ currentFolder](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_currentfolder)方法會告訴您目前正在掃描哪個資料夾。

第二次傳遞之後，請呼叫 [get \_ addedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_addedfilescount) 來檢查已新增至媒體櫃的檔案數目。 [Get \_ updateProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_updateprogress)方法會告訴您第二次行程的進度，以從0到100的百分比表示。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於 Player 物件模型**](about-the-player-object-model.md)
</dt> <dt>

[**IWMPFolderMonitorServices 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
</dt> </dl>

 

 





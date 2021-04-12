---
title: 從用戶端啟用快速快取串流
description: 從用戶端啟用快速快取串流
ms.assetid: 2a850d6f-8e1d-4aeb-9791-c51c3debf118
keywords:
- Windows Media Format SDK，啟用快取記憶體串流
- Windows Media Format SDK，快速快取串流
- Advanced Systems Format (ASF) ，啟用快速快取串流
- ASF (Advanced Systems Format) ，啟用快速快取串流
- Advanced Systems Format (ASF) 、Fast Cache 串流
- ASF (Advanced Systems Format) 、Fast Cache 串流
- 資料流程，啟用快取記憶體串流
- 快取記憶體串流，啟用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3f8423a6f71b86ea91a05ed74b931eaa28a64be
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374431"
---
# <a name="enabling-fast-cache-streaming-from-the-client"></a>從用戶端啟用快速快取串流

快取是一種串流技術，在此技術中，伺服器伺機會以比播放所需的位元速率更高的位元速率來串流處理內容。

如果可用的頻寬高於內容的位元速率，以較高的速率快取資料流程，並緩衝處理內容。 這有助於在網路變得擁塞時減少中斷。 如果網路頻寬低於內容的位元速率，則快速快取會在播放開始之前緩衝部分資料。 針對不可靠的網路（例如無線網路），或遇到網路流量（例如纜線數據機）大量波動的網路，建議使用 Fast Cache。 此外，也建議將變數位元速率 (VBR) 內容。 VBR 內容的頻寬需求不是常數，而 Fast Cache 可讓讀取器在較低位的部分期間緩衝串流。

快速快取串流僅支援隨選內容。 此外，伺服器必須設定為使用快速快取串流。

若要啟用讀取器物件中的快速快取，請使用值 **TRUE** 來呼叫 [**IWMReaderNetworkConfig2：： SetEnableContentCaching**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablecontentcaching)和 [**IWMReaderNetworkConfig2：： SetEnableFastCache**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablefastcache)方法。 第一個方法可讓讀取器快取資料流程處理的內容。 第二個可讓您特別使用快速快取。

使用這些設定時，如果網路頻寬明顯高於或低於內容的位元速率，且伺服器支援，則讀取器會依預設啟用快速快取。 使用者也可以藉由將下列一或多個修飾詞新增至 URL，來控制 reader 物件是否使用快速快取。



| 修飾詞         | Description                                                                                                                                                                                                                                                                                                                                      |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMCache          | 如果有此修飾詞，值 ' 0 ' 會明確停用快取，而值 ' 1 ' 則會明確啟用快取。                                                                                                                                                                                                                            |
| WMBitrate        | 此修飾詞會指定伺服器的最大位元速率。 此修飾詞可用來限制快速快取為特定的頻寬限制。 如果已透過呼叫 [**IWMReaderNetworkConfig：： SetConnectionBandwidth**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setconnectionbandwidth)來設定明確的連接頻寬，則會忽略此修飾詞。 |
| WMContentBitrate | 此修飾詞會指定內容的位元速率。 如果有的話，讀取器會使用這個修飾詞（如果有的話）會從多位元率選取資料流程 (MBR) 檔。 這可能會導致讀取器透過慢速連線接收較高的位元速率內容，這會導致很長的緩衝時間和延遲。                                          |



 

無論網路頻寬或內容的位元速率，WMCache = 1 都會強制讀取器使用快速快取串流，而不考慮任何先前對 **SetEnableFastCache** 的呼叫。 但是，它不會覆寫讀取器上的 **SetEnableContentCaching** 設定;也不會覆寫伺服器設定。

URL 修飾詞的格式如下：

*url*？*修飾* = 詞 *值*

例如：

mms://MyServer/MyVideo.wmv 嗎？WMCache = 1

可以指定一個以上的修飾詞;使用連字號 (&) 來分隔它們：

mms://MyServer/MyVideo.wmv 嗎？WMCache = 1&WMContentBitrate = 56000

 

 





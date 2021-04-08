---
title: 通訊協定變換
description: 通訊協定變換
ms.assetid: 61db5e2b-4858-446e-9a27-e0305b46683d
keywords:
- Windows Media Format SDK，通訊協定變換
- Advanced Systems Format (ASF) ，通訊協定變換
- ASF (Advanced Systems Format) ，通訊協定變換
- 通訊協定變換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2de8d0496467535f5740a10082f82e285c11ef6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023046"
---
# <a name="protocol-rollover"></a>通訊協定變換

通訊協定變換是一種程式，讓讀取器物件探索伺服器所提供的最佳串流通訊協定。 只要開啟包含 "mms" 配置的 URL，讀取器就會使用通訊協定變換。

讀取器支援數個通訊協定：

-   即時串流通訊協定 (RTSP) 
-   超文字傳輸通訊協定 (HTTP)
-   Microsoft Media Server (MMS) 

RTSP 和 MMS 通訊協定兩者都有兩種，一種是使用 [*UDP*](wmformat-glossary.md) 作為基礎傳遞通訊協定，而另一種使用 TCP。

讀取器物件一律會使用 TCP 來執行播放控制命令，但它可以使用 TCP 或 UDP 來傳遞資料流程內容。 UDP 是內容傳遞的慣用方式，因為它的頻寬額外負荷較于 TCP。 TCP 通訊協定可透過使用「虛擬電路」確保可靠的傳輸，但是這麼做的代價是，TCP 並不適合用於數位媒體串流，在此情況下，有效的頻寬使用會比較重要，因為這種情況偶爾會遺失封包。

當 URL 指定 "mms://" 時，讀取器會嘗試使用下列通訊協定來傳遞資料（依下列順序）：

1.  使用 UDP) RTSPU (RTSP
2.  使用 TCP) RTSPT (RTSP
3.  使用 UDP) MMSU (MMS
4.  使用 TCP) MMST (MMS
5.  HTTP

HTTP 是以 TCP 為基礎的單向通訊協定，它是 Web 服務器所使用的通訊協定。 使用 RTSP 進行串流處理的效率較低。 不過，大部分的防火牆都會設定為接受 HTTP 要求，而通常會拒絕其他串流通訊協定。

Microsoft Windows Server 2003 中的 windows Media Services 9 系列將會拒絕 Windows Media Format SDK 讀取器中的任何 MMSU 或 MMST 要求，因為 RTSP 是慣用的串流通訊協定。 Windows Media Services 4.1 版及更早版本不支援 RTSP。 在此情況下，讀取器物件會切換回 MMSU 或 HTTP。

如果 URL 配置提供特定的通訊協定（例如 RTSPU 的 "rtspu://" 或 HTTP 的 "HTTPs://"），則不適用通訊協定變換。 如果 URL 配置為 "rtsp://"，則讀取器會嘗試 RTSPU 和 RTSPT，但不會嘗試其他專案。

讀取器開啟檔案之後，您可以在讀取器上呼叫 [**IWMReaderAdvanced2：： GetProtocolName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname) 方法，以查詢所使用的通訊協定。 在串流或下載內容時，此方法會在完全快取內容時立即傳回名稱， **GetProtocolName** 方法會傳回字串 "Cache"。

若要取得讀取器支援的所有 Windows Media server 通訊協定的名稱，請在讀取器上呼叫 [**IWMReaderNetworkConfig：： GetSupportedProtocolName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getsupportedprotocolname) 方法。 您可以使用 **IWMReaderNetworkConfig** 介面，在讀取器的通訊協定變換清單中停用一或多個通訊協定。 例如， [**IWMReaderNetworkConfig：： SetEnableTCP**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setenabletcp) 方法會啟用或停用以 TCP 為基礎的通訊協定，而 [**IWMReaderNetworkConfig：： SetEnableUDP**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setenableudp) 會啟用或停用以 UDP 為基礎的通訊協定。 這些方法只適用于通訊協定變換;如果 URL 配置包含特定的通訊協定，仍然可以使用這些通訊協定。 通常沒有理由停用通訊協定變換中使用的任何通訊協定;這樣做可能會降低效能。 不過，它可能適用于測試。

 

 





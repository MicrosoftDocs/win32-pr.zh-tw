---
title: 從網路來源播放檔案
description: 從網路來源播放檔案
ms.assetid: 72f2d685-56fc-4da2-8372-3774cc65f59d
keywords:
- Windows媒體格式 SDK，讀取 ASF 資料
- Windows媒體格式 SDK，從網路來源播放檔案
- Advanced Systems Format (ASF) ，讀取資料
- ASF (Advanced Systems Format) ，讀取資料
- Advanced Systems Format (ASF) ，從網路來源播放檔案
- ASF (Advanced Systems Format) ，播放來自網路來源的檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8473a2feb4edd567c15d640dfd20e65c2893fe12de6c25a957cc5f730fde0baf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027376"
---
# <a name="playing-files-from-a-network-source"></a>從網路來源播放檔案

從網路讀取的本質與讀取本機檔案並不一樣。 應用程式會將 URL 傳遞給 reader 物件的 [**IWMReader：： Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) 方法，而 reader 物件會處理網路通訊協定的詳細資料。 讀取器物件使用智慧型緩衝區管理來提供最順暢的播放。 如果應用程式需要對讀取器物件的網路設定有更多控制權，可以透過 [**IWMReaderNetworkConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig) 和 [**IWMReaderNetworkConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2) 介面取得這些設定。

來自網路來源的內容屬於下列兩個類別的其中一種：

-   流。 資料會及時傳輸，以便在本機電腦上播放。 執行 Windows Media Services 的伺服器可以提供串流資料。 如果有多個位元速率 (MBR) 內容已串流處理，用戶端可以在串流處理時，從伺服器要求不同的位元速率。
-   下載。 所有資料都會儘快傳輸，以便在本機電腦上儲存為檔案。 Web 服務器提供下載的資料。 下載開始之後，就不會從用戶端到伺服器之間進行通訊。

當讀取器物件從 Web 服務器下載檔案時，它會使用稱為漸進式串流處理的技巧，讓播放程式在下載完成之前開始轉譯內容。 資料會經過緩衝處理，以提供不中斷的資料流程給玩家。 內容的傳輸速率和持續時間等資訊，會用來決定資料緩衝之前的時間，然後再提供給播放程式。

若要透過網路開啟檔案或資料流程，請使用適當的 URL 呼叫 reader 物件的 **IWMReader：： open** 方法。 **Open** 是非同步呼叫，因此它會立即返回。 當來源準備好進行讀取時，讀取器物件會將 WMT \_ 開啟的通知傳送至應用程式的 [**IWMStatusCallback：： OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) 回呼方法。 此時，應用程式可以藉由呼叫 [**IWMReaderAdvanced2：： GetPlayMode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)來查詢傳遞模式的讀取器。 若為網路內容，此方法將會傳回 WMT \_ 播放 \_ 模式 \_ 下載，指出下載的內容，或 WMT \_ 播放 \_ 模式 \_ 串流，指出已串流處理的內容。

若要開始讀取檔案或資料流程，請呼叫 [**IWMReader：： Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) 方法。 當讀取器開始 \_ 緩衝處理內容時，讀取器會傳送 WMT 緩衝 \_ 啟動通知，而 WMT \_ 緩衝處理 \_ 完成時則會停止通知。 當讀取器正在緩衝內容 (也就是在這兩個通知) 之間，您可能會想要對使用者顯示緩衝進度。 [**IWMReaderAdvanced2：： GetBufferProgress**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress)方法會傳回已緩衝處理的資料百分比，以及剩餘的預估時間。 針對下載的內容，您也可以呼叫 [**IWMReaderAdvanced2：： GetDownloadProgress**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress) 來取得下載進度。 重複呼叫這些方法以更新您的顯示，直到緩衝處理完成為止。 在播放期間可能會因為網路擁塞等因素而再次發生緩衝。 如果發生這種情況，應用程式會收到另一個 WMT \_ 緩衝處理 \_ 開始通知。

當讀取器物件開始播放內容時，會傳送 WMT \_ 已啟動的通知。 當每個範例都經過解碼並可供轉譯時，讀取器會透過 [**IWMReaderCallback：： OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) 回呼方法將它傳遞給應用程式。 此時，此程式與本機檔案播放的流程相同。 當播放停止時，讀取器會 \_ \_ \_ 傳送串流通知的 WMT 結束。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**讀取 ASF 檔案**](reading-asf-files.md)
</dt> </dl>

 

 





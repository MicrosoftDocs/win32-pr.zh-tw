---
title: 儲存內容
description: 儲存內容
ms.assetid: 22f4e580-43a4-48b5-8eb3-90e1346a1093
keywords:
- Windows Media Format SDK，儲存內容
- Windows Media Format SDK，快速快取串流
- Advanced Systems Format (ASF) ，儲存內容
- ASF (Advanced Systems Format) ，儲存內容
- Advanced Systems Format (ASF) 、Fast Cache 串流
- ASF (Advanced Systems Format) 、Fast Cache 串流
- 串流，儲存內容
- 快取記憶體串流，儲存內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba6c215a81accef29f8943ed52ca24264f785d94
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "103681553"
---
# <a name="saving-content"></a>儲存內容

藉由使用此 SDK，應用程式可以在讀取器物件上呼叫 [**IWMReaderAdvanced2：： savefileas 並**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) 方法，將下載或串流處理的內容儲存至使用者的本機電腦。 針對已串流處理的內容，伺服器必須使用快速快取串流，如 [從用戶端啟用快速快取串流](enabling-fast-cache-streaming-from-the-client.md)一節中所述。 針對串流的內容， **savefileas 並** 方法會建立一個 ASX 檔案，指向包含已儲存內容的 ASF 檔案。 如果讀取器物件正在串流處理伺服器端播放清單，則每個專案都會儲存為個別的 ASF 檔案，而 ASX 檔案會指向每個 ASF 檔案。 針對下載的內容， **savefileas 並** 方法只會建立一個 ASF 檔案。

若要將內容儲存到本機檔案，請執行下列動作：

1.  使用 URL 呼叫 [**IWMReader：： Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) 。 **Open** 是非同步呼叫，並會立即傳回。 等候作業完成，如中所述， [建立讀取器並開啟](to-create-a-reader-and-open-a-file.md)檔案。
2.  查詢 [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) 介面的 reader 物件。
3.  藉由呼叫 [**IWMReaderAdvanced4：： CanSaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cansavefileas) 方法來檢查內容是否可以儲存。 如果此方法傳回 False，則無法在本機儲存內容。 否則，請繼續進行步驟4。
4.  呼叫 [**IWMReaderAdvanced4：： IsUsingFastCache**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-isusingfastcache) 方法，以判斷伺服器是否使用快速快取串流。
5.  使用本機檔案的檔案名來呼叫 [**IWMReaderAdvanced2：： savefileas 並**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) 。 如果 **IsUsingFastCache** 方法傳回 True，請提供檔案名為 .asx 的副檔名。 否則，請將檔案名命名為 .asf、.wma 或 .wmv 副檔名。

應用程式可以藉由呼叫 [**IWMReaderAdvanced4：： CancelSaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cancelsavefileas) 方法，在進行中時取消儲存作業。

儲存的內容可能會受到 DRM 保護，因此可能無法在另一部電腦上播放該檔案。 如需有關內容保護的詳細資訊，請參閱 [數位 Rights Management 功能](digital-rights-management-features.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMReader 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**IWMReaderAdvanced2 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> </dl>

 

 





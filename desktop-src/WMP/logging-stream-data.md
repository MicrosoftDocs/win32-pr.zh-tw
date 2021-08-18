---
title: 記錄資料流程資料
description: 記錄資料流程資料
ms.assetid: c902a755-afdd-4dea-bc3e-036555fdff10
keywords:
- Windows媒體中繼檔播放清單，記錄資料流程資料
- 播放清單、記錄資料流程資料
- 中繼檔播放清單，記錄資料流程資料
- Windows媒體中繼檔播放清單，資料流程資料記錄
- 播放清單、串流資料記錄
- 中繼檔播放清單，資料流程資料記錄
- 記錄資料流程資料
- 串流資料記錄
- Windows Media Player，記錄串流資料
- Windows Media Player，資料流程資料記錄
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c0a2ae6fe4b647e8a5c19fc6f30562973b3280f37cd3af3a1b9d9093771959de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118118862"
---
# <a name="logging-stream-data"></a>記錄資料流程資料

您可以取得並使用已記錄的資訊來判斷檢視器行為，例如，查看資料流程的頻率，或特定使用者是否已查看串流以及品質的時間長度。

記錄資訊會自動傳送至從中產生播放清單的伺服器。 您也可以將記錄資訊傳送到其他伺服器，包括您專門用於記錄的網頁伺服器。 若要這樣做，請使用 **LOGURL** 元素，並指定 **HREF** 屬性的有效 URL。 您可以將 **LOGURL** 元素包含為 **ASX** 元素的子系，以及做為個別 **專案** 元素的子系。 當播放清單第一次開啟時，會將記錄資訊傳送至源伺服器，並傳送至該 **ASX** 元素的 **LOGURL** 子系中指定的每個 URL。 然後，當達到每個專案時，就會將該專案特定的記錄資訊傳送至 **Entry 專案** 的 **LOGURL** 子系中指定的每個 URL。

Windows 媒體格式 SDK 透過 **IWMSReaderNetworkConfig** 介面和下列方法支援 **LOGURL** 元素：


```XML
HRESULT AddLoggingUrl(LPCWSTR pwszUrl);
HRESULT GetLoggingUrl(DWORD dwIndex, LPCWSTR pwszUrl, DWORD *pcchUrl);
HRESULT GetLoggingUrlCount(DWORD *pdwUrlCount);
HRESULT ResetLoggingUrlList();

```



除了自動記錄的資訊之外，中繼檔播放清單也可以透過使用 **PARAM** 元素來記錄自訂資訊。 若要以這種方式使用 **PARAM** 專案，請將 **NAME** 屬性設定為 "log："，後面接著另一個冒號 ( "：" ) ，並以另一個冒號分隔的記錄功能變數名稱和選擇性 XML 命名空間。 第二個冒號之後的所有專案都會被視為命名空間，因此功能變數名稱不應包含冒號。

**NAME** 屬性中指定的記錄欄位設定為 **value** 屬性的值。 如果記錄檔尚未包含具有指定名稱的欄位，則會加入該欄位。

**範例程式碼**


```XML

    <ASX version="3.0">
      <LOGURL href="https://www.proseware.com/log.asp?SomeArg=SomeVal" />
      <ENTRY>
        <REF href="mms://ucast.proseware.com/Media1.wma" />
        <LOGURL href="https://www.proseware.com/cgi-bin/logging.pl?SomeArg=SomeVal" />
        <LOGURL href="https://www.proseware.com/WMLogging.dll?SomeArg=SomeVal" />
        <PARAM name="log:cs-media-role" value="Advertisement"/>
        <PARAM name="log:cs-media-name:namespace" value="Music"/>
        <REF href=rtsp://ucast.proseware.com/Media1.wma"/>
      </ENTRY>
      <ENTRY>
        <REF href="mms://ucast.proseware.com/Media2.wma"/>
      </ENTRY>
    </ASX>
    

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**中繼檔播放清單**](metafile-playlists.md)
</dt> <dt>

[**Windows媒體中繼檔元素參考**](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 





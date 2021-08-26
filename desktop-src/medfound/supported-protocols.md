---
description: 支援的通訊協定
ms.assetid: 3c026426-c2b7-4909-9524-9cc0bd45347e
title: 支援的通訊協定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20cc5e47bddec9e00fbb62e853db5a492172da84
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468025"
---
# <a name="supported-protocols"></a>支援的通訊協定

媒體基礎支援下列通訊協定：

-   即時串流通訊協定 (RTSP) 

    RTSP 主要用於串流處理媒體內容。 它可以使用 UDP 或 TCP 作為傳輸通訊協定。 UDP 是內容傳遞最有效率的方式，因為頻寬額外負荷低於 TCP 通訊協定。 雖然 TCP 通訊協定可確保可靠的封包傳遞，但 TCP 並不適用于數位媒體串流，但有效使用頻寬比偶爾遺失的封包來得重要。

-   超文字傳輸通訊協定 (HTTP)

    HTTP 使用 TCP，並由 web 伺服器使用。 "Httpd://" 配置表示來源可從 web 伺服器下載。 HTTP 也適用于防火牆，其通常設定為接受 HTTP 要求，且通常會拒絕其他串流通訊協定。

應用程式可以使用 [**IMFNetSchemeHandlerConfig**](/windows/desktop/api/mfidl/nn-mfidl-imfnetschemehandlerconfig) 介面取得媒體基礎所支援的通訊協定。 若要這樣做，應用程式必須先藉由呼叫 [**IMFNetSchemeHandlerConfig：： GetNumberOfSupportedProtocols**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getnumberofsupportedprotocols) 來取得通訊協定的數目，然後藉由呼叫 [**IMFNetSchemeHandlerConfig：： GetSupportedProtocolType**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getsupportedprotocoltype)取得以索引為基礎的通訊協定類型。 這個方法會傳回 [**MFNETSOURCE \_ 通訊協定 \_ 類型**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) 列舉中所定義的其中一個值。

應用程式也可以藉由呼叫 [**MFGetSupportedSchemes**](/windows/desktop/api/mfidl/nf-mfidl-mfgetsupportedschemes) 函數來取得來源解析程式所支援的配置。

## <a name="protocol-rollover"></a>通訊協定變換

當應用程式將 "mms://" 指定為 URL 配置時，來源解析程式會執行 *通訊協定變換* 操作。 在此程式中，來源解析程式會決定網路來源用來取得內容的最佳通訊協定。 一般來說，針對媒體串流，具有 UDP (RTSPU) 的 RTSP 比 HTTP 更有效率。 但是，如果內容是裝載在 web 伺服器上，則 HTTP 是較佳的選擇。

當嘗試使用 URL 配置中指定的通訊協定失敗時，也會發生通訊協定變換。 例如，當防火牆封鎖 UDP 封包時，通訊協定可能會失敗。 在此情況下，來源解析程式會切換至 HTTP。

如果 URL 配置包含特定的通訊協定（例如 "rtspu://"），則不適用通訊協定變換。 此外，如果驗證失敗，或伺服器已達到用戶端連線的限制，就不會執行變換。 建議應用程式指定 "mms://" 配置，並允許來源解析程式為案例選取最佳的通訊協定。

下表列出變換順序。




| 允許的架構 | 通訊協定變換順序 | 
|-----------------|-------------------------|
| mms://或 rtsp:// | 快速快取已啟用：<br /><ol><li>使用 TCP 的 RTSP (RTSPT) <br /></li><li>使用 UDP (RTSPU) 的 RTSP<br /></li><li>HTTP 串流<br /></li><li> (HTTPD) 的 HTTP 下載<br /></li></ol>快取已停用：<br /><ol><li>RTSPU<br /></li><li>RTSPT<br /></li><li>HTTP 串流<br /></li><li>HTTP 下載<br /></li></ol> | 
| rtspu:// | RTSPU | 
| rtspt:// | RTSPT | 
| https:// | <ol><li>HTTP<br /></li><li>HTTPD<br /></li></ol> | 
| HTTPd:// | HTTPD | 




 

## <a name="retrieving-the-current-protocol"></a>正在抓取目前的通訊協定

在通訊協定變換作業之後，網路來源可能會使用應用程式在 URL 配置中所指定的通訊協定。 在網路來源建立與媒體伺服器的連線之後，應用程式就可以使用通訊協定變換結果。

為了取得用來取得內容的通訊協定和傳輸，應用程式可以從網路來源抓取 [MFNETSOURCE \_ 通訊協定](mfnetsource-protocol-property.md)屬性的屬性值，以及 **IPropertyStore** 物件的 [MFNETSOURCE \_ 傳輸](mfnetsource-transport-property.md)屬性。

下列程式碼顯示如何取得這些值。


```C++
// Create an IPropertyStore object.
    IPropertyStore *pProp = NULL;
    hr = CreatePropertyStore(&pProp);

    PROPVARIANT var;
    PropVariantInit(&var);

// Get the property store from the network source.
// The network source is created by the source resolver. Not shown.
    if (SUCCEEDED(hr))
    {
        hr = pNetworkSource->QueryInterface 
                (__uuidof(IPropertyStore), 
                (void**)&pProp);
    }
    if (SUCCEEDED(hr))
    {
        // Create a property key.
        PROPERTYKEY key;
        // Get the MFNETSOURCE_PROTOCOL property value.
        key.fmtid = MFNETSOURCE_PROTOCOL;
        hr = pProp->GetValue (key, &var);

        // Get the MFNETSOURCE_TRANSPORT property value.
        key.fmtid = MFNETSOURCE_TRANSPORT;
        key.pid = 0;
        hr = pProp->GetValue (key, &var);

    }
```



在上述的範例程式碼中， **IPropertyStore：： GetValue** 會抓取 MFNETSOURCE \_ 通訊協定值，這是 [**MFNETSOURCE \_ 通訊協定 \_ 類型**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) 列舉的成員。 針對 MFNETSOURCE \_ 傳輸，此值是 [**MFNETSOURCE \_ 傳輸 \_ 類型**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type) 列舉的成員。

或者，應用程式可以使用 MFNETSOURCE \_ STATISTICS service 服務來取得相同的值 \_ 。 若要使用這種服務，應用程式可以呼叫 [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) 函數，從網路來源取得屬性存放區。 這個屬性存放區包含 [MFNETSOURCE \_ statistics](mfnetsource-statistics-property.md) 屬性中的網路統計資料。 您可以藉由指定 MFNETSOURCE \_ 通訊協定 \_ 識別碼和 MFNETSOURCE \_ 傳輸 \_ 識別碼（定義于 [**MFNETSOURCE \_ 統計資料 \_ 識別碼**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) 列舉中）來抓取通訊協定和傳輸值。 下列程式碼顯示如何使用 MFNETSOURCE \_ STATISTICS service 服務來取得通訊協定和傳輸值 \_ 。


```C++
// Create an IPropertyStore object.
    IPropertyStore *pProp = NULL;
    hr = CreatePropertyStore(&pProp);

    HRESULT hr = S_OK;

    hr = MFGetService(
        pMediaSource, 
        MFNETSOURCE_STATISTICS_SERVICE, 
        IID_IPropertyStore, 
        (void**) & pProp); 

    if (SUCCEEDED(hr))
    {
        // Create a property key.
        PROPERTYKEY key;
        // Get the property value.
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_PROTOCOL_ID;
        hr = pProp->GetValue (key, &var);

        // Get the transport value.
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_TRANSPORT_ID;
        hr = pProp->GetValue (key, &var);

    }
```



## <a name="enabling-and-disabling-protocols"></a>啟用和停用通訊協定

應用程式可以設定網路來源，以便在變換程式期間略過特定的通訊協定。 若要這樣做，會使用網路來源屬性來停用特定的通訊協定。 下表顯示其所控制的屬性和通訊協定。



| 屬性                                                                    | 描述                                 |
|-----------------------------------------------------------------------------|---------------------------------------------|
| [MFNETSOURCE \_ 啟用 \_ HTTP](mfnetsource-enable-http-property.md)           | 啟用或停用 HTTP 和 HTTPD。         |
| [MFNETSOURCE \_ 啟用 \_ RTSP](mfnetsource-enable-rtsp-property.md)           | 啟用或停用 RTSPU 和 RTSPT。        |
| [MFNETSOURCE \_ 啟用 \_ TCP](mfnetsource-enable-tcp-property.md)             | 啟用或停用 RTSPT。                  |
| [MFNETSOURCE \_ 啟用 \_ UDP](mfnetsource-enable-udp-property.md)             | 啟用或停用 RTSPU。                  |
| [MFNETSOURCE \_ 啟用 \_ 下載](mfnetsource-enable-download-property.md)   | 啟用或停用 HTTPD。                  |
| [MFNETSOURCE \_ 啟用 \_ 串流](mfnetsource-enable-streaming-property.md) | 啟用或停用 RTSPU、RTSPT 和 HTTP。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎中的網路功能](networking-in-media-foundation.md)
</dt> </dl>

 

 





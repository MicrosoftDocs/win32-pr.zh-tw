---
description: 本主題說明來源解析程式如何建立媒體來源的內部詳細資料。
ms.assetid: b0113527-f22c-4519-b1cf-fea54bff4090
title: 配置處理常式和 Byte-Stream 處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc7bde81a02762cd9c82e0a7d031582c856da6984ab231775580ddf249caca23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118058225"
---
# <a name="scheme-handlers-and-byte-stream-handlers"></a>配置處理常式和 Byte-Stream 處理常式

本主題說明來源解析程式如何建立媒體來源的內部詳細資料。 如果您要為媒體基礎執行自訂媒體來源，而且想要透過來源解析程式將媒體來源提供給應用程式，請閱讀本主題。

來源解析程式可以從 URL 或位元組資料流程建立媒體來源 (也就是 [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) 指標) 。 若要這樣做，它會使用稱為 *處理常式* 的 helper 物件。 針對 Url，來源解析程式會使用 *配置處理常式*。 若為位元組資料流程，它會使用 *位元組資料流程處理常式*。

配置處理常式會使用 URL 做為輸入，並建立媒體來源或位元組資料流程。 如果建立位元組資料流程，來源解析程式會將它傳遞至位元組資料流程處理常式，該處理常式會建立媒體來源。 下圖說明此程式。

![顯示來源解析流程的圖表](images/f2ade1a8-6f2a-4e40-8cda-2ccf576880c6.gif)

## <a name="scheme-handlers"></a>配置處理常式

當應用程式呼叫 [**IMFSourceResolver：： CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) 或它的非同步對等專案 [**BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl)時，會使用配置處理常式。

來源解析程式會在登錄中查看配置處理常式。 配置處理常式會依 URL 配置列在下列機碼底下：

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows Media Foundation
            SchemeHandlers
               <scheme>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Media Foundation
            SchemeHandlers
               <scheme>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

其中 *<scheme>* 是處理常式設計來剖析的 URL 配置。 配置包含尾端的 '： ' 字元;例如，"HTTP："。

若要註冊新的配置處理常式，請新增名稱為配置處理常式 CLSID 的專案，其名稱為標準字串格式： `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}` 。 專案的值是字串 (REG \_ SZ) 包含處理常式的簡短描述，例如「我的配置處理常式」。 專案的重要部分是 CLSID。 來源解析程式會使用此 CLSID 呼叫 **CoCreateInstance** 來建立處理常式。

配置處理常式會公開 [**IMFSchemeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler) 介面。 如果來源解析程式找到符合 URL 配置的配置處理常式，來源解析程式就會呼叫 [**IMFSchemeHandler：： BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject)，並傳入原始 url。 配置處理常式會開啟 URL，並嘗試剖析內容。 這時，配置處理常式有兩個選項：

-   建立媒體來源。
-   建立位元組資料流程。

如果它建立媒體來源，則來源解析程式會將媒體來源傳回給應用程式。 如果它建立位元組資料流程，來源解析程式會嘗試尋找適當的位元組資料流程處理常式，如下一節中所述。

## <a name="byte-stream-handlers"></a>Byte-Stream 處理常式

當應用程式呼叫 [**IMFSourceResolver：： CreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream) 或它的非同步對等專案 [**BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream)時，會使用位元組資料流程處理常式。 如先前所述，當配置處理常式傳回位元組資料流程時，也會使用它們。

如同配置處理常式，位元組資料流程處理常式會列在登錄中。 它們會依副檔名或 MIME (類型（) ），在下列機碼底下列出：

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows Media Foundation
            ByteStreamHandlers
               <ExtensionOrMimeType>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Media Foundation
            ByteStreamHandlers
               <ExtensionOrMimeType>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

其中 *<ExtensionOrMimeType>* 是檔案名副檔名或 MIME 類型。 副檔名包含初始 '. ' 字元;例如，".wmv"。

副檔名是由應用程式提供的 URL 的一部分。 MIME 類型可透過位元組資料流程上的 [**MF \_ BYTESTREAM \_ 內容 \_ 類型**](mf-bytestream-content-type-attribute.md) 屬性取得。

若要註冊新的位元組資料流程處理常式，請以標準字串格式加入名稱為處理常式 CLSID 的專案。 專案的值是字串 (REG \_ SZ) 包含處理常式的簡短描述，例如「我的 Byte-Stream 處理常式」。 來源解析程式會呼叫 **CoCreateInstance** 以從 CLSID 建立處理常式。 您可以在一個以上的延伸模組或 MIME 類型中註冊相同的處理常式。

位元組資料流程處理常式會公開 [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) 介面。 如果來源解析程式找到相符的位元組資料流程處理常式，則會呼叫 [**IMFByteStreamHandler：： BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject)。 此方法的輸入是位元組資料流程的指標，以及原始的 URL （如果有的話）。 位元組資料流程處理常式會讀取位元組資料流程，直到它剖析足夠的資料來建立媒體來源為止。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[來源解析程式](source-resolver.md)
</dt> </dl>

 

 




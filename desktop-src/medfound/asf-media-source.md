---
description: 媒體基礎提供 ASF 媒體來源，可讓應用程式用來代表架構的管線層中的 ASF 檔案。
ms.assetid: a2d2b382-d666-4a37-a6a9-0b839fbfbec3
title: ASF 媒體來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b3222f32649aa5cb3f4d1d4688a9f7fb7402167e7831377fd8b04d6c879e23b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117881149"
---
# <a name="asf-media-source"></a>ASF 媒體來源

媒體基礎提供 ASF 媒體來源，可讓應用程式用來代表架構的管線層中的 ASF 檔案。

為了播放 ASF 檔案，應用程式可以使用 ASF 媒體來源將資料送入播放管線。 在編碼案例中，應用程式可以使用 ASF 媒體來源作為來源，以轉換成另一種格式，或將較高的位元速率檔案轉換成較低的位元速率檔案，而不變更格式。 您必須在管線層中使用 ASF 媒體來源，也就是應用程式必須使用媒體會話來控制操作。 此存取層級可讓應用程式在媒體會話進行時取得事件。 若要取得更低層級的 ASF 內容存取權，應用程式必須使用 WMContainer 層 ASF 元件。

ASF 媒體來源會實 [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) 介面，這是媒體基礎中媒體來源的泛型介面。 如同任何其他媒體來源，ASF 媒體來源提供的簡報描述項主要描述 ASF 標頭物件。 此外，ASF 媒體來源會提供代表媒體內容中每個資料流程的資料流程描述項。 如需詳細資訊，請參閱 [ASF 檔案結構](asf-file-structure.md)。

-   [建立 ASF 媒體來源](#creating-the-asf-media-source)
-   [ASF 媒體來源的設定設定](#configuration-settings-for-the-asf-media-source)
-   [ASF 媒體來源物件模型](#asf-media-source-object-model)
-   [ASF 媒體來源服務](#asf-media-source-services)
    -   [時間碼轉譯](#timecode-translation)
-   [相關主題](#related-topics)

## <a name="creating-the-asf-media-source"></a>建立 ASF 媒體來源

若要建立 ASF 媒體來源，應用程式必須使用 [來源解析](source-resolver.md)程式。 為了建立 ASF 媒體來源，應用程式必須提供來源解析程式建立 ASF 媒體來源的來源。 您必須指定來源檔案的 URL 或包含媒體的位元組資料流程，以提供來源資訊。 如果應用程式選擇藉由指定 URL 來建立 ASF 媒體來源，則必須針對同步作業呼叫 [**IMFSourceResolver：： CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) 或 **IMFSourceResolver：： Begin .。。** 非同步作業的 EndCreateObjectFromURL。 從位元組串流建立媒體來源的程式很類似。 應用程式必須呼叫 [**IMFSourceResolver：： CreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream) 進行同步作業或 **IMFSourceResolver：： Begin .。。** 非同步作業的 EndCreateObjectFromBytestream。 這些呼叫必須 \_ \_ 在 *dwFlags* 參數中指定 MF 解析 MEDIASOURCE。 如需使用此旗標的詳細資訊，請參閱使用來源解析程式。

如果應用程式指定 URL，則在本機檔案中，URL 字串可以包含媒體檔案的路徑，也可以使用 "file：" 配置作為前置詞。 副檔名必須是 ".asf"、"wm"、L ".wma" 或 ".wmv"。 若為網路上的 ASF 檔案，來源解析程式會建立使用 ASF 媒體來源的 [網路來源](network-source-features.md)。

在建立物件期間，來源解析程式會在系統登錄中尋找配置處理常式和位元組資料流程處理常式的清單，並載入最接近的相符處理常式，以便剖析媒體內容，也會在下方建立媒體來源物件。 無論用來建立媒體來源 (URL 和位元組串流) 的方法，來源解析程式都會建立位元組資料流程，並將來源媒體的內容讀入位元組資料流程中。 如需詳細資訊，請參閱 [配置處理常式和 Byte-Stream 處理常式](scheme-handlers-and-byte-stream-handlers.md)。

如需有關如何建立媒體來源的程式碼範例，請參閱 [使用來源解析程式](using-the-source-resolver.md)。

## <a name="configuration-settings-for-the-asf-media-source"></a>ASF 媒體來源的設定設定

來源解析程式會查詢基礎位元組資料流程的功能，並決定新建立之媒體來源上允許的作業。 其中一項功能是搜尋。 如果允許搜尋作業，應用程式可以指定媒體來源在搜尋簡報中的特定點時，所使用的搜尋模式。

應用程式可以在建立物件期間，設定要使用之媒體來源的搜尋模式。 使用指定的搜尋模式建立 ASF 媒體來源之後，就無法在媒體來源上修改或在簡報期間動態變更。 搜尋喜好設定會指定為應用程式呼叫中用來建立媒體來源之相關來源解析程式方法的屬性。 這些屬性集合會在屬性存放區中設定，並傳遞至 *pProps* 參數。 如果未傳遞這些屬性，則會使用預設設定來處理媒體來源功能。 如需有關設定這些屬性的詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。

如果允許搜尋，ASF 媒體來源支援下列搜尋模式：

-   確切搜尋：在此模式中，ASF 媒體來源依賴 ASF 檔案的 ASF 索引物件。 如果檔案沒有 Index 物件，則會停用確切搜尋，而且會根據媒體來源上設定的應用程式指定屬性，使用其中一個其他模式。
-   近似搜尋：此模式是由應用程式所要求，方法是將屬性存放區中的 [**MFPKEY \_ ASFMediaSource \_ ApproxSeek**](mfpkey-asfmediasource-approxseek-property.md) 傳遞給相關的來源解析程式方法。 不過，只有在位元組資料流程不支援以時間為基礎的搜尋時，才會使用大約的搜尋。 在此模式中，媒體來源會判斷相對於搜尋時間的開始時間。 如果 ASF 檔案包含 ASF 索引物件，則會用來計算開始時間。 近似的搜尋較不精確，但是比確切的搜尋更快，因為所花的時間會以預先決定的開始時間轉譯第一個樣本的時間更快。
-   反復搜尋：若要設定此模式，應用程式必須設定 [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) 屬性。 反復搜尋是一種演算法，可在 ASF 檔案中尋找不包含 ASF 索引物件的位置。 在此模式中，媒體來源會藉由讀取位元組資料流程位移來 determins 搜尋點的粗略估計。 它會根據平均位元速率來使用一連串的近似值，以逐漸接近目標搜尋時間。  (演算法類似于二進位搜尋。 ) 反復的搜尋可能需要比使用 Index 物件搜尋更長的時間，因此預設為停用。 如果設定此屬性，請使用下列屬性來設定搜尋參數： [MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ Max \_ Count](mfpkey-asfmediasource-iterativeseek-max-count.md)[MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ 容忍度（ \_ \_ 毫秒）](mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md)。 這些屬性會分別設定反覆運算次數和容錯值的最大數目。 當演算法達到反覆運算次數上限時，或當它找到的封包與搜尋時間的距離在指定的容錯範圍內時，就會中止。

總而言之，當 ASF 檔案未包含 ASF 索引物件時，應用程式可以選擇近似值或反復搜尋。

## <a name="asf-media-source-object-model"></a>ASF 媒體來源物件模型

ASF 媒體來源會實 [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) 介面並公開下列介面。 應用程式可以藉由呼叫 ASF 媒體來源上的 **IMFMediaSource：： QueryInterface** 來取得這些介面的參考。



| 介面                                                | 描述                                                                                                                                        |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                 | 所有媒體來源都需要。                                                                                                                    |
| [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | 所有媒體來源都需要。 允許應用程式透過媒體會話從媒體來源取得事件。                                 |
| [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                   | 查詢指定服務介面的媒體來源。                                                                                      |
| [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)               | 設定並取得媒體來源的屬性。 每個屬性都包含描述性名稱和值。                                               |
| [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)                       | 描述 ASF 檔案的中繼資料。                                                                                                           |
| [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)       | 取得中繼資料的集合，不論是針對整個簡報，或是簡報中的一個資料流程。                                      |
| [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                 | 查詢支援的播放率範圍，包括反向播放。                                                                |
| [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)                 | 取得或設定播放速率。                                                                                                                    |
| [**IMFTrustedInput**](/windows/desktop/api/mfidl/nn-mfidl-imftrustedinput)               | 取得來源中包含之每個 ASF 資料流程的 ITA。                                                                                  |
| [**IMFPMPClient**](/windows/desktop/api/mfidl/nn-mfidl-imfpmpclient)                     | 讓媒體來源接收指向 [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) 介面的指標，該介面是用來在 PMP 進程中建立物件。 |
| [**IMFTimecodeTranslate**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate)     | 轉換運動圖片和電視工程師 (的) 時間碼和 100-納秒時間單位。                              |



 

## <a name="asf-media-source-services"></a>ASF 媒體來源服務

ASF 媒體來源提供適用于 ASF 檔案範圍的各種服務。 若要取得特定服務的指標，應用程式必須在呼叫 [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice)時，使用下列其中一個服務識別碼。 如需詳細資訊，請參閱 [服務介面](service-interfaces.md)。



| 服務識別碼               | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MF \_ 速率 \_ 控制 \_ 服務       | 藉由使用此識別碼，應用程式可以取得 [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) 或 [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) 介面的指標。 藉由使用媒體來源所實行的速率支持對象，應用程式可以檢查基礎 ASF 媒體檔案是否支援特定的速率，同時也能取得最快且最慢的速率。 藉由使用速率控制物件，應用程式可以取得並設定播放速率。 如果應用程式指定播放的特定速率，ASF 媒體來源會先檢查要求的速率是否在速率限制內 (由 fasted 和最慢的速率決定) 然後設定速率。 這不會檢查變數條件，因為位元速率可能會因為網路頻寬而變更。 如需詳細資訊，請按 [速率控制](rate-control.md)。 |
| MF \_ 中繼資料 \_ 提供者 \_ 服務  | 藉由使用此識別碼，應用程式可以取得 ASF 媒體來源之 [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) 介面的指標。 此介面可讓您存取 ASF 檔案的相關資訊，尤其是 ASF 標頭物件和媒體內容中包含的串流。 標頭資訊是透過呈現描述元屬性公開，而資料流程資訊則是透過資料流程描述元屬性提供。 如需這些屬性的詳細資訊，請參閱 [媒體基礎 ASF 標頭物件的屬性](media-foundation-attributes-for-asf-header-objects.md)。 除了透過屬性公開的資訊之外，還存在描述中繼資料（設定為屬性）。                                                                                                 |
| MF \_ 屬性 \_ 處理常式 \_ 服務   | 藉由使用此識別碼，應用程式可以取得 ASF 媒體來源之 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 介面的指標。 屬性存放區包含與 ASF 檔案相關的所有中繼資料。 此識別碼是 Windows 7 中的新識別碼，取代了 \_ \_ \_ 用於取得中繼資料屬性的 MF 中繼資料提供者服務。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| MFNETSOURCE \_ 統計資料 \_ 服務 | 如需詳細資訊，請參閱在 [用戶端記錄](client-logging.md)中取出網路統計資料。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| MF 時間 \_ 碼 \_ 服務            | 藉由使用此識別碼，應用程式可以取得媒體來源 [**IMFTimecodeTranslate**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate) 介面的指標。 這種實現可用來執行時間程式碼轉譯，例如將 SMPTE 時間代碼轉換為 100-nano 秒單位及背面。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

### <a name="timecode-translation"></a>時間碼轉譯

ASF 媒體來源提供時間程式碼轉譯服務，可讓您的應用程式將 SMPTE 時間代碼轉換為 100-納秒單位) 中最接近的呈現時間 (。 相反地，應用程式也可以取得要求的呈現時間的時間碼。 服務可透過 [**IMFTimecodeTranslate**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate) 介面（ASF 媒體來源所實行）來取得。 這個介面指標上的方法呼叫是非同步，可從您的主應用程式執行緒執行，而不會封鎖應用程式的使用者介面。

下列步驟摘要說明時間程式碼轉譯的程式：

1.  藉由呼叫 [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice)並指定 **MF 時間 \_ 碼 \_ 服務** 識別碼，取得 ASF 媒體來源 [**IMFTimecodeTranslate**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate)介面的指標。
2.  呼叫 [**IMFTimecodeTranslate：： BeginConvertTimecodeToHNS**](/windows/desktop/api/mfidl/nf-mfidl-imftimecodetranslate-beginconverttimecodetohns) 或 [**IMFTimecodeTranslate：： BeginConvertHNSToTimecode**](/windows/desktop/api/mfidl/nf-mfidl-imftimecodetranslate-beginconverthnstotimecode) ，並指定要轉譯的時間。 若為 **BeginConvertTimecodeToHNS** ，必須將時間代碼指定為具有 **VT \_ I8** 資料類型的 [**PROPVARIANT**](/windows/win32/api/propidl/ns-propidl-propvariant)變數。 **BeginConvertHNSToTimecode** 方法所需的時間是 100-納秒的單位做為 [**MFTIME**](mftime.md)類型。
3.  適當地呼叫 [**IMFTimecodeTranslate：： EndConvertTimecodeToHNS**](/windows/desktop/api/mfidl/nf-mfidl-imftimecodetranslate-endconverttimecodetohns) 或 **IMFTimecodeTranslate：： EndConvertTimecodeToHNS** 來完成非同步作業。

在建立媒體來源期間，來源解析程式會建立檔案的位元組資料流程，媒體來源會從該檔案讀取 ASF 內容。 為了讓時間轉換成功，與 ASF 檔案相關聯的位元組資料流程必須具備搜尋功能;否則，應用程式 \_ \_ \_ 會 \_ 從 **開始 ...** 呼叫取得 MF E BYTESTREAM 無法搜尋的錯誤。 時間轉換的另一項需求是，asf 檔案（以 ASF 媒體來源表示）必須具有 ASF 索引物件。 系統會從可維護所有索引的 ASF 索引物件和 ASF 檔案的對應搜尋點解壓縮呈現時間和時間碼。 針對簡報時間程式碼轉譯，ASF 檔案必須包含簡單的索引物件;對於時間代碼對簡報時間轉譯，ASF 檔案必須有 Index 物件。 轉換作業依賴基礎 *索引子* (WMContainer 元件) 來剖析和讀取與 ASF 檔案相關聯的索引物件。 如果檔案不包含索引物件，應用程式會以非同步方式接收 MF \_ E \_ NO \_ index 錯誤碼。

為了轉譯應用程式所要求的時間，媒體來源會列舉檔案內的資料流程，並尋找包含適當 ASF 索引物件的資料流程。 如果找到這類串流，媒體來源會剖析串流的 ASF 封包，直到到達正確的時間碼為止。 找到正確的範例之後，它會從範例中取出對應的呈現時間或時間代碼，然後將它傳回給呼叫者。

### <a name="script-command-support"></a>指令碼命令支援

當您建立包含腳本資料流程的 ASF 拓撲時，腳本資料流程節點會加入拓撲中。 此節點會在適當的時間傳送 IMFSamples。 腳本來源節點所提供的 IMFSample 會將資料儲存在與範例相關聯的 IMFMediaBuffer 中。 您可以在範例上呼叫 CopyToBuffer 來取得 IMFMediaBuffer，然後呼叫緩衝區上的鎖定來取得資料。 

腳本資料流程承載會以類型字串的形式封裝到緩衝區中，後面接著 Null、命令字串，後面接著 Null。 字串是具有 ASF 格式的 Unicode。

例如，承載可能看起來如下 (其中 \ 0 表示 Null 字元) ：

*URL\0http://contoso.com\0*

*Text\0This 是 caption\0*



## <a name="related-topics"></a>相關主題

<dl> <dt>

[管線層 ASF 元件](pipeline-layer-asf-components.md)
</dt> <dt>

[媒體基礎中的 ASF 支援](asf-support-in-media-foundation.md)
</dt> </dl>

 

 

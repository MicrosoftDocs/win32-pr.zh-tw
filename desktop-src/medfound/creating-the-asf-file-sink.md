---
description: ASF 檔案接收是媒體基礎所提供的 IMFMediaSink，可讓應用程式用來將 ASF 媒體資料封存至檔案。 如需 ASF 媒體接收物件模型和一般使用方式的相關資訊，請參閱 ASF 媒體接收器。
ms.assetid: 991f3345-a6b4-45c2-a89d-3c13c70b6bbc
title: 建立 ASF 檔接收器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c43625bcbc581b4967d4db99cef71a0fc779f070
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111828"
---
# <a name="creating-the-asf-file-sink"></a>建立 ASF 檔接收器

ASF 檔案接收是媒體基礎所提供的 [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) ，可讓應用程式用來將 ASF 媒體資料封存至檔案。 如需 ASF 媒體接收器的物件模型和一般使用方式的相關資訊，請參閱 [Asf 媒體接收器](asf-media-sinks.md)。

有兩種方式可以建立 ASF 檔案接收的實例。 您可以呼叫 [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink) 或 [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)。

如果您呼叫 [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)，就必須指定輸出檔案的位元組資料流程，接收會在編碼會話期間寫入 ASF 內容。 指定的位元組資料流程必須具有可搜尋和可寫入的功能，否則 **MFCreateASFMediaSink** 呼叫會失敗，並出現 E \_ 失敗的錯誤碼。 此呼叫會建立同進程的檔案接收物件，並將指標傳回至 file 接收器的 [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) 介面。

如果您呼叫 [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)，就必須指定檔案接收寫入媒體資料的輸出檔案的 URL。 在此情況下，檔案接收會在內部建立位元組資料流程。 函數會傳回檔案接收之 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 介面的指標。 收件者

當您的編碼拓撲設計如下時，請考慮 [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate) 而不是 [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)：

-   編碼拓撲適用于受保護的媒體路徑 (PMP) ，而 file 接收器則是跨進程使用。
-   拓撲的輸出節點會使用傳回到檔案接收之啟始物件的指標來建立，而您的應用程式會依資料流程號碼追蹤檔案接收中的資料流程。
    > [!Note]  
    > 您可以藉由呼叫 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)來啟動 file 接收器。 不過，您不需要啟用物件明確。 媒體會話會追蹤啟用物件，並在編碼會話期間自動啟動檔案接收。

     

-   資料流程資訊是在 ContentInfo 物件中設定。 Disucssed 下一個子區段。

建立 ASF 檔案接收之後，必須先設定它，才能建立拓撲。 檔案接收必須知道下列資訊，才能產生輸出檔。

-   基本資料流程資訊
-   編碼模式資訊
-   中繼資料

檔案接收會執行 [ASF ContentInfo 物件](asf-contentinfo-object.md) 並公開 [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) 介面，讓應用程式可以使用它來設定與資料流程及編碼相關的資訊。 根據您呼叫來建立檔案接收的函式而定，有兩種方式可以取得 **IMFASFContentInfo** 介面的參考。

-   如果您呼叫 [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)函數，應用程式必須在傳回的檔案接收上呼叫 **IMFMediaSink：： QueryInterface** ，以查詢 [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)介面。
-   如果您選擇呼叫 [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)，此函式會預期您在呼叫之前已有完整設定的 ContentInfo 物件。 若要這樣做，您必須藉由呼叫 [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) 來建立空的 ContentInfo 物件，然後使用所有必要的資訊進行設定。 將設定的 ContentInfo 物件傳遞至 **MFCreateASFMediaSinkActivate** ，以接收接收啟始物件的指標。 您無法使用傳回的啟用物件來啟動檔案接收，然後變更任何資料流程或編碼資訊。

如需有關設定接收資料流程和特定屬性的詳細資訊，請參閱下列主題：

-   [將資料流程資訊新增至 ASF 檔案接收](adding-stream-information-to-the-asf-file-sink.md)
-   [設定 File 接收中的屬性](setting-properties-in-the-file-sink.md)
-   [將中繼資料新增至 File 接收器](adding-metadata-to-the-file-sink.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ASF 媒體接收](asf-media-sinks.md)
</dt> <dt>

[管線層 ASF 元件](pipeline-layer-asf-components.md)
</dt> <dt>

[媒體基礎中的 ASF 支援](asf-support-in-media-foundation.md)
</dt> </dl>

 

 




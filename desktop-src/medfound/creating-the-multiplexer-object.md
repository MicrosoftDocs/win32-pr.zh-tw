---
description: 建立多工器物件
ms.assetid: a5adc40c-abb4-4012-b6f2-eb871eaed7b9
title: 建立多工器物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28dd7933bdd7c3a8587c96cb490c4e4122ecc04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191075"
---
# <a name="creating-the-multiplexer-object"></a>建立多工器物件

ASF 多工器是一種 WMContainer 層物件，可與 [ASF 資料物件](asf-file-structure.md) 搭配使用，並讓應用程式能夠為媒體資料流程產生 ASF 資料封包。

多工器物件會公開 [**IMFASFMultiplexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmultiplexer) 介面。 若要建立多工器，請呼叫 [**MFCreateASFMultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer)。 此函數會傳回空物件的指標。 如果應用程式正在撰寫新的 ASF 檔案，應用程式必須使用 ContentInfo 物件初始化多工器。 若要這樣做，請呼叫 [**IMFASFMultiplexer：： Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize)。 指定的 ContentInfo 物件代表新檔案的 ASF 標頭物件。 如需有關為新檔案建立及初始化 ContentInfo 物件的詳細資訊，請參閱 [初始化新 ASF 檔案的 ContentInfo 物件](initializing-the-contentinfo-object-of-a-new-asf-file.md)。

[**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize)方法會剖析 ContentInfo 物件，以收集資料流程設定資訊，例如資料流程數目、封包大小、預先處理。 （選擇性）多工器也可能需要有漏洞值區參數和承載延伸模組單位。 需要這項資訊，才能產生符合 ASF 標頭物件中所定義之需求的資料封包。 **Initialize** 方法會根據資料流程的媒體類型和設定來設定多工器。 例如，如果資料流程設定為具有承載延伸 (請參閱) [建立及設定 ASF 資料流程](creating-and-configuring-asf-streams.md) ，然後將多工器設定為將這些值新增至產生的資料封包。

[**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize)方法也會取得初始資料物件的控制碼，該物件是建立 ContentInfo 物件以進行寫入時所建立的物件。 產生資料封包時，多工器會將封包新增至資料物件，並適當地加以更新。 當多工器產生所有的資料封包之後，它會更新提供的 ContentInfo 物件，以便更新特定的值，例如資料封包數目。

下列程式碼範例顯示如何建立多工器，並使用 ContentInfo 物件將它初始化。


```C++
//-------------------------------------------------------------------
// CreateOutputGenerators
//
// Creates the ASF mux and the ASF Content Info object for the 
// output file.
//-------------------------------------------------------------------

HRESULT CreateOutputGenerators(
    IMFASFProfile *pProfile, 
    IMFASFContentInfo **ppContentInfo, 
    IMFASFMultiplexer **ppMux
    )
{
    IMFASFContentInfo *pContentInfo = NULL;
    IMFASFMultiplexer *pMux = NULL;

    // Use the ASF profile to create the ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);

    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->SetProfile(pProfile);
    }

    // Create the ASF Multiplexer object.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateASFMultiplexer(&pMux);
    }
    
    // Initialize it using the new ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pMux->Initialize(pContentInfo);
    }

    // Return the pointers to the caller.
    if (SUCCEEDED(hr))
    {
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();

        *ppMux = pMux;
        (*ppMux)->AddRef();
    }

    SafeRelease(&pContentInfo);
    SafeRelease(&pMux);

    return hr;
}
```



若要查看完整應用程式中使用的此函式，請參閱 [教學課程：將 ASF 資料流程從一個檔案複製到另](tutorial--copying-asf-streams-from-one-file-to-another.md)一個檔案。

## <a name="multiplexer-initialization-and-leaky-bucket-settings"></a>多工器初始化和有漏洞 Bucket 設定

[**IMFASFMultiplexer：： Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize)方法會設定多工器，以判斷有漏洞值區資料流程。 若要設定這些參數，請確定已在指定的 ContentInfo 物件上設定下列屬性值。 如需有關設定這些屬性的詳細資訊，請參閱 [設定 ContentInfo 物件中的屬性](setting-properties-in-the-contentinfo-object.md)。

-   [**MFPKEY \_ASFMEDIASINK \_ AUTOADJUST \_ 位元速率**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) 屬性：這表示多工器是否需要自動調整位元速率，以維護有漏洞 bucket 中的資料流程。 藉由呼叫 [**IMFASFMultiplexer：： SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) 並傳遞 MFASF 多工器 **\_ \_ AUTOADJUST \_ 位元速率** 旗標，應用程式可以變更此設定。

-   [**MFPKEY \_ASFMEDIASINK \_ BASE \_ SENDTIME**](mfpkey-asfmediasink-base-sendtime-property.md) 屬性： send time 會指出將釋放有漏洞 bucket 內的承載。 傳送時間必須等於或早于呈現時間，因為承載必須有時間才能在呈現時間之前取得目的地。

    這個屬性值是第一個傳送時間。 多工器會使用此值來計算後續的傳送時間，以確保資料會穩定地流經值區。 如果已在多工器上設定 MFASF 多工器 **\_ \_ AUTOADJUST \_ 位元速率** 旗標，則多工器將會調整位元速率，如此當緩衝區視窗接近已滿時，就會送出承載。 如果未設定旗標，則多工器無法產生資料封包，因為頻寬溢出。

多工器會從與 [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) 方法中指定之 ContentInfo 物件相關聯的 ASF 設定檔取得串流設定資訊。 串流設定資訊包括有漏洞 bucket 參數。 多工器需要此值，才能產生資料封包。

若要指定有漏洞值區參數，請在代表設定檔中之資料流程的串流設定物件上，設定 [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) 屬性中的值。 若要使用編碼器所使用的緩衝區視窗值，請呼叫 [**IWMCodecLeakyBucket：： GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md)。 只有在設定編碼器的輸出媒體類型之後，才知道實際的緩衝區視窗值。 如需設定輸出媒體類型的相關資訊，請參閱 [編碼器上的媒體類型協商](media-type-negotiation-on-the-encoder.md)。

> [!Note]  
> 編碼器所使用的有漏洞值區值，在用來建立多工器的 ASF 設定檔所提供的 ContentInfo 物件中可能不同。

 

[**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize)方法會更新 ContentInfo 物件，讓正確的值反映在最終的 ASF 標頭物件中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ASF 多工器](asf-multiplexer.md)
</dt> <dt>

[產生新的 ASF 資料封包](generating-new-asf-data-packets.md)
</dt> </dl>

 

 

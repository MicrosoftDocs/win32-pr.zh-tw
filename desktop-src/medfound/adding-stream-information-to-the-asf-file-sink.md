---
description: ASF 檔案接收是媒體基礎所提供的 IMFMediaSink，可讓應用程式用來將 ASF 媒體資料封存至檔案。 如需 ASF 媒體接收物件模型和一般使用方式的相關資訊，請參閱 ASF 媒體接收器。
ms.assetid: 21cbde27-a2ca-4298-9197-43bcaf05588d
title: 將資料流程資訊新增至 ASF 檔案接收
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e08c6997d9c77836f379d4ca7b75720ddea245
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970803"
---
# <a name="adding-stream-information-to-the-asf-file-sink"></a>將資料流程資訊新增至 ASF 檔案接收

ASF 檔案接收是媒體基礎所提供的 [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) ，可讓應用程式用來將 ASF 媒體資料封存至檔案。 如需 ASF 媒體接收器的物件模型和一般使用方式的相關資訊，請參閱 [Asf 媒體接收器](asf-media-sinks.md)。

在具現化檔案接收之後，必須先設定它，才能建立拓撲。 檔案接收需要知道輸出檔中的資料流程、編碼模式資訊和中繼資料。 本主題說明在檔案接收中加入資料流程的程式。

-   [在 ASF 檔案接收中新增資料流程](#adding-streams-in-the-asf-file-sink)
-   [列舉資料流程接收](#enumerating-stream-sinks)
-   [相關主題](#related-topics)

## <a name="adding-streams-in-the-asf-file-sink"></a>在 ASF 檔案接收中新增資料流程

檔案接收必須知道輸出資料流程及其屬性，才能據以產生輸出範例，並將其新增至輸出 ASF 檔案。 這些設定會寫入到最後一個 ASF 標頭物件。

若要設定資料流程資訊，您必須有 file 接收器的 ASF ContentInfo 物件的參考。 如需詳細資訊，請參閱 [建立 ASF 檔案接收](creating-the-asf-file-sink.md)。

下列程式摘要說明使用 ASF 設定檔物件來設定資料流程的一般步驟。

**在 ASF 檔案接收中設定串流資訊**

1.  藉由呼叫 [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile)來建立 ASF 設定檔物件。
2.  針對輸出檔中的每個資料流程，建立要在檔案接收中加入之目標資料流程的媒體類型。 媒體類型必須與 Windows Media 編碼器支援的輸出類型相容。

    如需將音訊串流新增至設定檔的相關資訊，請參閱建立適用于 ASF 編碼的音訊資料流程。

    如需將視頻串流新增至設定檔的相關資訊，請參閱建立適用于 ASF 編碼的影片串流。

3.  藉由呼叫 [**IMFASFProfile：： CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream)，根據步驟2中建立的媒體類型建立資料流程。
4.  藉由呼叫步驟3中所收到的 [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) 介面指標，指派新建立資料流程的資料流程號碼。
5.  選擇性地使用下列資訊設定資料流程：
    -   藉由設定屬性來有漏洞 bucket 參數： [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) 或 [**mf \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)
    -   裝載延伸，藉由呼叫 [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) 方法相互排除。
6.  藉由設定 [**mf \_ ASFPROFILE \_ MINPACKETSIZE**](mf-asfprofile-minpacketsize-attribute.md) 和 [**mf \_ ASFPROFILE \_ MAXPACKETSIZE**](mf-asfprofile-maxpacketsize-attribute.md) 屬性，選擇性地設定設定檔的資料封包大小。 ASF 設定檔會公開 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面，應用程式可以藉由呼叫 **IMFASFProfile：： QueryInterface** 來取得其參考。
7.  在檔案接收中設定資料流程的編碼資訊。 在 [檔接收器中設定屬性的](setting-properties-in-the-file-sink.md)討論。
8.  藉由呼叫 [**IMFASFProfile：： SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream)，將資料流程新增至設定檔。
9.  藉由呼叫 [**IMFASFContentInfo：： SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile)，將設定檔與 ContentInfo 物件產生關聯。

若要修改現有的資料流程，應用程式可以取得資料流程 [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) 介面的參考，並根據需求加以重新設定。 若要加入或移除資料流程，應用程式必須呼叫 [**IMFASFProfile：： RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream)。 若要套用這些變更、串流修改或移除，您必須在 ContentInfo 物件中再次設定設定檔。 這會覆寫已與 ContentInfo 物件相關聯的現有設定檔。


```C++
//-------------------------------------------------------------------
//  CreateVideoStream
//  Create an video stream and add it to the profile.
//
//  pProfile: A pointer to the ASF profile.
//  wStreamNumber: Stream number to assign for the new stream.
//    pType: A pointer to the source's video media type.
//-------------------------------------------------------------------

HRESULT CreateVideoStream(IMFASFProfile* pProfile, WORD wStreamNumber, IMFMediaType* pType)
{
    if (!pProfile)
    {
        return E_INVALIDARG;
    }
    if (wStreamNumber < 1 || wStreamNumber > 127 )
    {
        return MF_E_INVALIDSTREAMNUMBER;
    }

    HRESULT hr = S_OK;

    
    IMFMediaType* pVideoType = NULL;
    IMFASFStreamConfig* pVideoStream = NULL;

    UINT32 dwBitRate = 0;
        
    //Create a new video type from the source type
    hr = CreateCompressedVideoType(pType, &pVideoType);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create a new stream with the video type
    hr = pProfile->CreateStream(pVideoType, &pVideoStream);
    if (FAILED(hr))
    {
        goto done;
    }
    

    //Set a valid stream number
    hr = pVideoStream->SetStreamNumber(wStreamNumber);
    if (FAILED(hr))
    {
        goto done;
    }

    //Add the stream to the profile
    hr = pProfile->SetStream(pVideoStream);
    if (FAILED(hr))
    {
        goto done;
    }

    wprintf_s(L"Video Stream created. Stream Number: %d .\n", wStreamNumber);

done:

    SafeRelease(&pVideoStream);
    SafeRelease(&pVideoType);

    return hr;
}
```



## <a name="enumerating-stream-sinks"></a>列舉資料流程接收

針對 ContentInfo 物件感知的設定檔中的每個資料流程，ASF 檔案接收會建立並加入包含已編碼資料流程之所有屬性的資料流程接收。 ASF file 接收器的設計目的是要包含固定的資料流程。 這表示您無法藉由呼叫 [**IMFMediaSink：： AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink) 或 [**IMFMediaSink：： RemoveStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-removestreamsink)來新增或移除資料流程。 這些對檔案接收的呼叫會失敗，並出現 MF \_ E \_ STREAMSINKS \_ 固定錯誤碼。 在設定檔中新增或移除資料流程時，不會自動新增或移除檔案接收中的串流接收器。 如果設定檔中的資料流程已變更，您必須捨棄檔案的現有實例，並以新的資料流程資訊重新建立它。

下列程式摘要說明在 ASF 檔案接收中列舉串流接收器的一般步驟。

**列舉資料流程接收**

1.  呼叫 [**IMFMediaSink：： GetStreamSinkCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkcount) ，以取得 ASF 檔案接收中的串流接收器總數。
2.  流經串流接收器的迴圈會取得資料流程接收器 [**GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) 介面的參考。

    -或-

    呼叫 [**IMFMediaSink：： GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) ，藉由指定資料流程號碼來取得資料流程接收。 每個資料流程接收都會以您在設定檔中建立資料流程時所設定的資料流程號碼來識別。

如果您要建立部分拓撲來編碼媒體檔案，您必須將檔案接收以輸出拓撲節點的形式加入拓撲中。 您可以藉由指定檔案接收中的每個流出接收，或是藉由設定「檔案接收」啟始物件和「串流接收器」識別碼，來進行這項操作。 如需詳細資訊和程式碼範例，請參閱 [建立輸出節點](creating-output-nodes.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ASF 媒體接收](asf-media-sinks.md)
</dt> <dt>

[媒體基礎中的 ASF 支援](asf-support-in-media-foundation.md)
</dt> </dl>

 

 




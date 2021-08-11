---
description: 簡報描述項
ms.assetid: 714c8bda-5ce1-47e2-ba73-9304e26b3129
title: 簡報描述項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 963faeebbb180b504cc11202645a9432bbb3a94e988495b9ddcf96e550b05519
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238829"
---
# <a name="presentation-descriptors"></a>簡報描述項

*簡報* 是一組共用常見展示時間的相關媒體串流。 例如，簡報可能包含電影的音訊和影片串流。 *簡報描述* 項是一個物件，其中包含特定簡報的描述。 簡報描述項可用來設定媒體來源和某些媒體接收器。

每個呈現描述項都包含一或多個 *資料流程描述* 項的清單。 這些會描述簡報中的資料流程。 您可以選取或取消選取資料流程。 只有選取的資料流程會產生資料。 取消選取的資料流程不在使用中，也不會產生任何資料。 每個資料流程描述項都有 *媒體類型處理常式*，可用來變更資料流程的媒體類型，或取得資料流程的目前媒體類型。  (如需有關媒體類型的詳細資訊，請參閱 [媒體類型](media-types.md)。 ) 

下表顯示這些物件所公開的主要介面。



| Object                  | 介面                                                      |
|-------------------------|----------------------------------------------------------------|
| 簡報描述項 | [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) |
| 資料流程描述項       | [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)             |
| 媒體類型處理常式      | [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)             |



 

## <a name="media-source-presentations"></a>媒體來源簡報

每個媒體來源都提供描述來源預設設定的簡報描述項。 在預設設定中，至少選取一個資料流程，而每個選取的資料流程都有媒體類型。 若要取得簡報描述項，請呼叫 [**IMFMediaSource：： CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)。 方法會傳回 [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) 指標。

您可以修改來源的展示描述項，以選取一組不同的資料流程。 除非媒體來源已停止，否則請勿修改表示描述項。 當您呼叫 [**IMFMediaSource：： start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) 來啟動來源時，會套用這些變更。

若要取得資料流程的數目，請呼叫 [**IMFPresentationDescriptor：： GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount)。 若要取得資料流程的資料流程描述元，請呼叫 [**IMFPresentationDescriptor：： GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) ，並傳入資料流程的索引。 資料流程是從零開始編制索引。 **GetStreamDescriptorByIndex** 方法會傳回 [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)指標。 它也會傳回布林值旗標，指出是否已選取資料流程。 如果選取資料流程，媒體來源會產生該資料流程的資料。 否則，來源不會產生該資料流程的任何資料。 若要選取資料流程，請使用資料流程的索引來呼叫 [**IMFPresentationDescriptor：： SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) 。 若要取消選取資料流程，請呼叫 [**IMFPresentationDescriptor：:D eselectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream)。

下列程式碼示範如何從媒體來源取得簡報描述項，並列舉資料流程。


```C++
HRESULT hr = S_OK;
DWORD cStreams = 0;
BOOL  fSelected = FALSE;

IMFPresentationDescriptor *pPresentation = NULL;
IMFStreamDescriptor *pStreamDesc = NULL;

hr = pSource->CreatePresentationDescriptor(&pPresentation);

if (SUCCEEDED(hr))
{
    hr = pPresentation->GetStreamDescriptorCount(&cStreams);
}

if (SUCCEEDED(hr))
{
    for (DWORD iStream = 0; iStream < cStreams; iStream++)
    {
        hr = pPresentation->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);

        if (FAILED(hr))
        {
            break;
        }

        /*  Use the stream descriptor. (Not shown.) */

        SAFE_RELEASE(pStreamDesc);
    }
}
SAFE_RELEASE(pPresentation);
SAFE_RELEASE(pStreamDesc);
```



## <a name="media-type-handlers"></a>媒體類型處理常式

若要變更資料流程的媒體類型或取得資料流程目前的媒體類型，請使用資料流程描述項的媒體類型處理常式。 呼叫 [**IMFStreamDescriptor：： GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) 以取得媒體類型處理常式。 這個方法會傳回 [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) 指標。

如果您只想要知道串流中的資料類型（例如音訊或影片），請呼叫 [**IMFMediaTypeHandler：： GetMajorType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype)。 這個方法會傳回主要媒體類型的 GUID。 例如，播放應用程式通常會將音訊串流連接到音訊轉譯器和影片轉譯器。 如果您使用媒體會話或拓撲載入器來建立拓撲，主要類型 GUID 可能是您唯一需要的格式資訊。

如果您的應用程式需要更多有關目前格式的詳細資訊，請呼叫 [**IMFMediaTypeHandler：： GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype)。 這個方法會傳回媒體類型之 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) 介面的指標。 使用此介面可取得格式的詳細資料。

媒體類型處理常式也包含資料流程支援的媒體類型清單。 若要取得清單的大小，請呼叫 [**IMFMediaTypeHandler：： GetMediaTypeCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount)。 若要從清單中取得媒體類型，請使用媒體類型的索引來呼叫 [**IMFMediaTypeHandler：： GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) 。 媒體類型會依喜好設定的近似順序傳回。 例如，針對音訊格式，較高的取樣率優先于較低的取樣率。 不過，沒有任何可控制順序的明確規則，因此您應該將它視為指導方針。

支援的類型清單可能不包含資料流程所支援的每種可能媒體類型。 若要測試是否支援特定的媒體類型，請呼叫 [**IMFMediaTypeHandler：： IsMediaTypeSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-ismediatypesupported)。 若要設定媒體類型，請呼叫 [**IMFMediaTypeHandler：： SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype)。 如果方法成功，資料流程將會包含符合指定格式的資料。 **SetCurrentMediaType** 方法不會變更慣用類型的清單。

下列程式碼示範如何取得媒體類型處理常式、列舉慣用的媒體類型，以及設定媒體類型。 此範例假設應用程式有一些演算法，而不是此處所示，無法選取媒體類型。 細節會大幅依賴您的應用程式。


```C++
HRESULT hr = S_OK;
DWORD cTypes = 0;
BOOL  bTypeOK = FALSE;

IMFMediaTypeHandler *pHandler = NULL;
IMFMediaType *pMediaType = NULL;

hr = pStreamDesc->GetMediaTypeHandler(&pHandler);

if (SUCCEEDED(hr))
{
    hr = pHandler->GetMediaTypeCount(&cTypes);
}

if (SUCCEEDED(hr))
{
    for (DWORD iType = 0; iType < cTypes; iType++)
    {   
        hr = pHandler->GetMediaTypeByIndex(iType, &pMediaType);

        if (FAILED(hr))
        {
            break;
        }

        /* Examine the media type. (Not shown.)  */

        /* If this media type is acceptable, set the media type. */

        if (bTypeOK)
        {
            hr = pHandler->SetCurrentMediaType(pMediaType);
            break;
        }

        SAFE_RELEASE(pMediaType);
    }
}    

SAFE_RELEASE(pMediaType);
SAFE_RELEASE(pHandler);
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體來源](media-sources.md)
</dt> <dt>

[媒體基礎平臺 Api](media-foundation-platform-apis.md)
</dt> </dl>

 

 




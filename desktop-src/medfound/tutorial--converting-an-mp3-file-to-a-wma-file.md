---
description: 本教學課程示範如何使用轉碼 API 來編碼 Windows Media 音訊的 (WMA) 檔。
ms.assetid: 2397ca78-edb5-4756-bd07-00529db28f76
title: 教學課程：編碼 WMA 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f491a9d460771dae91a49ab42982fbe97b24c42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988733"
---
# <a name="tutorial-encoding-a-wma-file"></a>教學課程：編碼 WMA 檔案

本教學課程示範如何使用 [轉碼 API](transcode-api.md) 來編碼 Windows Media 音訊的 (WMA) 檔。

本教學課程會重複使用教學課程中大部分的程式碼， [編碼一個](tutorial--encoding-an-mp4-file-.md)數量的檔案，因此您應該先閱讀該教學課程。 唯一不同的程式碼是函數 `CreateTranscodeProfile` ，它會建立轉碼設定檔。

## <a name="create-the-transcode-profile"></a>建立轉碼設定檔

*轉碼設定檔* 說明編碼參數和檔案容器。 針對 WMA，檔案容器是 (ASF) 檔案的 Advanced 串流格式。 ASF 檔案包含音訊串流，使用 [**Windows Media 音訊編碼器**](windowsmediaaudioencoder.md)進行編碼。

若要建立轉碼拓撲，請建立轉碼設定檔，並指定音訊串流和容器的參數。 然後藉由指定輸入來源、輸出 URL 和轉碼設定檔來建立拓撲。

若要建立設定檔，請執行下列步驟。

1.  呼叫 [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) 函式以建立空的轉碼設定檔。
2.  呼叫 [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) 以從編碼器取得音訊媒體類型的清單。 此函式會傳回代表 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)指標集合的 [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection)指標。
3.  選擇符合轉碼需求的音訊媒體類型，並將屬性複製到屬性存放區。 在本教學課程中，會使用清單中的第一個媒體類型。
    -   呼叫 [**IMFCollection：： GetElement**](/windows/desktop/api/mfobjects/nf-mfobjects-imfcollection-getelement) ，以從清單中選取音訊媒體類型。
    -   查詢媒體類型以取得媒體類型屬性存放區之 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面的指標。
    -   呼叫 [**IMFAttributes：： GetCount**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getcount) 來取得媒體類型中包含的屬性數目。
    -   呼叫 [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) 來建立新的屬性存放區。
    -   呼叫 [**IMFAttributes：： CopyAllItems**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-copyallitems) ，將屬性從媒體類型複製到新的屬性存放區。
4.  呼叫 [**IMFTranscodeProfile：： SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) 來設定音訊串流的屬性。
5.  呼叫 [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) 來建立容器層級屬性的屬性存放區。
6.  將 [MF \_ 轉碼 \_ CONTAINERTYPE](mf-transcode-containertype.md) 屬性設定為 **MFTRANSCODECONTAINERTYPE \_ asf**，以指定 asf 檔案容器。
7.  呼叫 [**IMFTranscodeProfile：： SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) ，以設定設定檔上的容器層級屬性。


```C++
template <class Q>
HRESULT GetCollectionObject(IMFCollection *pCollection, DWORD index, Q **ppObj)
{
    IUnknown *pUnk;
    HRESULT hr = pCollection->GetElement(index, &pUnk);
    if (SUCCEEDED(hr))
    {
        hr = pUnk->QueryInterface(IID_PPV_ARGS(ppObj));
        pUnk->Release();
    }
    return hr;
}

HRESULT CreateTranscodeProfile(IMFTranscodeProfile **ppProfile)
{
    IMFTranscodeProfile *pProfile = NULL;     // Transcode profile.
    IMFCollection   *pAvailableTypes = NULL;  // List of audio media types.
    IMFMediaType    *pAudioType = NULL;       // Audio media type.
    IMFAttributes   *pAudioAttrs = NULL;      // Copy of the audio media type.
    IMFAttributes   *pContainer = NULL;       // Container attributes.

    DWORD dwMTCount = 0;
    
    // Create an empty transcode profile.
    HRESULT hr = MFCreateTranscodeProfile(&pProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get output media types for the Windows Media audio encoder.

    // Enumerate all codecs except for codecs with field-of-use restrictions.
    // Sort the results.

    DWORD dwFlags = 
        (MFT_ENUM_FLAG_ALL & (~MFT_ENUM_FLAG_FIELDOFUSE)) | 
        MFT_ENUM_FLAG_SORTANDFILTER;

    hr = MFTranscodeGetAudioOutputAvailableTypes(MFAudioFormat_WMAudioV9, 
        dwFlags, NULL, &pAvailableTypes);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAvailableTypes->GetElementCount(&dwMTCount);
    if (FAILED(hr))
    {
        goto done;
    }
    if (dwMTCount == 0)
    {
        hr = E_FAIL;
        goto done;
    }

    // Get the first audio type in the collection and make a copy.
    hr = GetCollectionObject(pAvailableTypes, 0, &pAudioType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateAttributes(&pAudioAttrs, 0);       
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAudioType->CopyAllItems(pAudioAttrs);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the audio attributes on the profile.
    hr = pProfile->SetAudioAttributes(pAudioAttrs);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the container attributes.
    hr = MFCreateAttributes(&pContainer, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pContainer->SetGUID(MF_TRANSCODE_CONTAINERTYPE, MFTranscodeContainerType_ASF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProfile->SetContainerAttributes(pContainer);
    if (FAILED(hr))
    {
        goto done;
    }

    *ppProfile = pProfile;
    (*ppProfile)->AddRef();

done:
    SafeRelease(&pProfile);
    SafeRelease(&pAvailableTypes);
    SafeRelease(&pAudioType);
    SafeRelease(&pAudioAttrs);
    SafeRelease(&pContainer);
    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[轉碼 API](transcode-api.md)
</dt> </dl>

 

 




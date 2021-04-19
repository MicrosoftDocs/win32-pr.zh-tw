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
# <a name="tutorial-encoding-a-wma-file"></a><span data-ttu-id="92248-103">教學課程：編碼 WMA 檔案</span><span class="sxs-lookup"><span data-stu-id="92248-103">Tutorial: Encoding a WMA File</span></span>

<span data-ttu-id="92248-104">本教學課程示範如何使用 [轉碼 API](transcode-api.md) 來編碼 Windows Media 音訊的 (WMA) 檔。</span><span class="sxs-lookup"><span data-stu-id="92248-104">This tutorial shows how to use the [Transcode API](transcode-api.md) to encode a Windows Media Audio (WMA) file.</span></span>

<span data-ttu-id="92248-105">本教學課程會重複使用教學課程中大部分的程式碼， [編碼一個](tutorial--encoding-an-mp4-file-.md)數量的檔案，因此您應該先閱讀該教學課程。</span><span class="sxs-lookup"><span data-stu-id="92248-105">This tutorial reuses most of the code from the tutorial [Encoding an MP4 File](tutorial--encoding-an-mp4-file-.md), so you should read that tutorial first.</span></span> <span data-ttu-id="92248-106">唯一不同的程式碼是函數 `CreateTranscodeProfile` ，它會建立轉碼設定檔。</span><span class="sxs-lookup"><span data-stu-id="92248-106">The only code that differs is the function `CreateTranscodeProfile`, which creates the transcode profile.</span></span>

## <a name="create-the-transcode-profile"></a><span data-ttu-id="92248-107">建立轉碼設定檔</span><span class="sxs-lookup"><span data-stu-id="92248-107">Create the Transcode Profile</span></span>

<span data-ttu-id="92248-108">*轉碼設定檔* 說明編碼參數和檔案容器。</span><span class="sxs-lookup"><span data-stu-id="92248-108">A *transcode profile* describes the encoding parameters and the file container.</span></span> <span data-ttu-id="92248-109">針對 WMA，檔案容器是 (ASF) 檔案的 Advanced 串流格式。</span><span class="sxs-lookup"><span data-stu-id="92248-109">For WMA, the file container is an Advanced Streaming Format (ASF) file.</span></span> <span data-ttu-id="92248-110">ASF 檔案包含音訊串流，使用 [**Windows Media 音訊編碼器**](windowsmediaaudioencoder.md)進行編碼。</span><span class="sxs-lookup"><span data-stu-id="92248-110">The ASF file contains an audio stream, which is encoded using the [**Windows Media Audio Encoder**](windowsmediaaudioencoder.md).</span></span>

<span data-ttu-id="92248-111">若要建立轉碼拓撲，請建立轉碼設定檔，並指定音訊串流和容器的參數。</span><span class="sxs-lookup"><span data-stu-id="92248-111">To build the transcode topology, create the transcode profile and specify the parameters for the audio stream and the container.</span></span> <span data-ttu-id="92248-112">然後藉由指定輸入來源、輸出 URL 和轉碼設定檔來建立拓撲。</span><span class="sxs-lookup"><span data-stu-id="92248-112">Then create the topology by specifying the input source, the output URL, and the transcode profile.</span></span>

<span data-ttu-id="92248-113">若要建立設定檔，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="92248-113">To create the profile, perform the following steps.</span></span>

1.  <span data-ttu-id="92248-114">呼叫 [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) 函式以建立空的轉碼設定檔。</span><span class="sxs-lookup"><span data-stu-id="92248-114">Call the [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) function to create an empty transcode profile.</span></span>
2.  <span data-ttu-id="92248-115">呼叫 [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) 以從編碼器取得音訊媒體類型的清單。</span><span class="sxs-lookup"><span data-stu-id="92248-115">Call [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) to get a list of audio media types from the encoder.</span></span> <span data-ttu-id="92248-116">此函式會傳回代表 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)指標集合的 [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection)指標。</span><span class="sxs-lookup"><span data-stu-id="92248-116">This function returns an [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) pointer that represents a collection of [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) pointers.</span></span>
3.  <span data-ttu-id="92248-117">選擇符合轉碼需求的音訊媒體類型，並將屬性複製到屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="92248-117">Choose the audio media type that matches your transcoding requirements and copy the attributes to an attribute store.</span></span> <span data-ttu-id="92248-118">在本教學課程中，會使用清單中的第一個媒體類型。</span><span class="sxs-lookup"><span data-stu-id="92248-118">For this tutorial, the first media type in the list is used.</span></span>
    -   <span data-ttu-id="92248-119">呼叫 [**IMFCollection：： GetElement**](/windows/desktop/api/mfobjects/nf-mfobjects-imfcollection-getelement) ，以從清單中選取音訊媒體類型。</span><span class="sxs-lookup"><span data-stu-id="92248-119">Call [**IMFCollection::GetElement**](/windows/desktop/api/mfobjects/nf-mfobjects-imfcollection-getelement) to select an audio media type from the list.</span></span>
    -   <span data-ttu-id="92248-120">查詢媒體類型以取得媒體類型屬性存放區之 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="92248-120">Query the media type to get a pointer to the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface of the media type's attribute store.</span></span>
    -   <span data-ttu-id="92248-121">呼叫 [**IMFAttributes：： GetCount**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getcount) 來取得媒體類型中包含的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="92248-121">Call [**IMFAttributes::GetCount**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getcount) to get the number of attributes contained in the media type.</span></span>
    -   <span data-ttu-id="92248-122">呼叫 [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) 來建立新的屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="92248-122">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create a new attribute store.</span></span>
    -   <span data-ttu-id="92248-123">呼叫 [**IMFAttributes：： CopyAllItems**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-copyallitems) ，將屬性從媒體類型複製到新的屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="92248-123">Call [**IMFAttributes::CopyAllItems**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-copyallitems) to copy the attributes from the media type to the new attribute store.</span></span>
4.  <span data-ttu-id="92248-124">呼叫 [**IMFTranscodeProfile：： SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) 來設定音訊串流的屬性。</span><span class="sxs-lookup"><span data-stu-id="92248-124">Call [**IMFTranscodeProfile::SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) to set the attributes for the audio stream.</span></span>
5.  <span data-ttu-id="92248-125">呼叫 [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) 來建立容器層級屬性的屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="92248-125">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create an attribute store for the container-level attributes.</span></span>
6.  <span data-ttu-id="92248-126">將 [MF \_ 轉碼 \_ CONTAINERTYPE](mf-transcode-containertype.md) 屬性設定為 **MFTRANSCODECONTAINERTYPE \_ asf**，以指定 asf 檔案容器。</span><span class="sxs-lookup"><span data-stu-id="92248-126">Set the [MF\_TRANSCODE\_CONTAINERTYPE](mf-transcode-containertype.md) attribute to **MFTranscodeContainerType\_ASF**, which specifies an ASF file container.</span></span>
7.  <span data-ttu-id="92248-127">呼叫 [**IMFTranscodeProfile：： SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) ，以設定設定檔上的容器層級屬性。</span><span class="sxs-lookup"><span data-stu-id="92248-127">Call [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) to set the container-level attributes on the profile.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="92248-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="92248-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92248-129">轉碼 API</span><span class="sxs-lookup"><span data-stu-id="92248-129">Transcode API</span></span>](transcode-api.md)
</dt> </dl>

 

 




---
description: 使用影片編解碼器私用資料
ms.assetid: 0cc24fe4-a5b6-4805-8c8e-3066d12ec4bd
title: '使用影片編解碼器私用資料 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83e86fc31a50d2c4e553b5947717ea930698d812
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977253"
---
# <a name="using-video-codec-private-data-microsoft-media-foundation"></a><span data-ttu-id="e764e-103">使用影片編解碼器私用資料 (Microsoft 媒體基礎) </span><span class="sxs-lookup"><span data-stu-id="e764e-103">Using Video Codec Private Data (Microsoft Media Foundation)</span></span>

<span data-ttu-id="e764e-104">Windows Media 視訊9編解碼器所產生的壓縮輸出不能正確解壓縮，而不需要編碼器提供的某些資料。</span><span class="sxs-lookup"><span data-stu-id="e764e-104">The compressed output produced by the Windows Media Video 9 codecs cannot be properly decompressed without some data provided by the encoder.</span></span> <span data-ttu-id="e764e-105">此資料（稱為編解碼器私用資料）必須附加至輸出媒體類型。</span><span class="sxs-lookup"><span data-stu-id="e764e-105">This data, called codec private data, must be appended to the output media type.</span></span> <span data-ttu-id="e764e-106">您可以藉由呼叫 [IWMCodecPrivateData](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecprivatedata) 介面的方法來取得編解碼器私用資料。</span><span class="sxs-lookup"><span data-stu-id="e764e-106">You can get the codec private data by calling the methods of the [IWMCodecPrivateData](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecprivatedata) interface.</span></span> <span data-ttu-id="e764e-107">將其他完整的 [**Sql-dmo \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) 結構傳遞給 [IWMCodecPrivateData：： SetPartialOutputType](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-setpartialoutputtype)。</span><span class="sxs-lookup"><span data-stu-id="e764e-107">Pass the otherwise complete [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure to [IWMCodecPrivateData::SetPartialOutputType](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-setpartialoutputtype).</span></span> <span data-ttu-id="e764e-108">然後呼叫 [IWMCodecPrivateData：： GetPrivateData](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-getprivatedata) 兩次，一次取得資料的大小，然後再將資料複製到該大小的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e764e-108">Then call [IWMCodecPrivateData::GetPrivateData](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-getprivatedata) twice, once to get the size of the data, and then again to copy the data to a buffer of that size.</span></span> <span data-ttu-id="e764e-109">建立新的緩衝區以保存已附加私用資料的 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 結構，並將結構和資料複製到該緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e764e-109">Create a new buffer to hold the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure with the private data appended, and copy the structure and the data to that buffer.</span></span> <span data-ttu-id="e764e-110">最後，將 **Sql-dmo \_ 媒體 \_ 類型** 結構的 **pbFormat** 成員設定為新建立之緩衝區的位址，並將 **cbFormat** 成員設定為 **VIDEOINFOHEADER** 和私用資料的組合大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e764e-110">Finally, set the **pbFormat** member of the **DMO\_MEDIA\_TYPE** structure to the address of the newly created buffer and set the **cbFormat** member to the combined size, in bytes, of the **VIDEOINFOHEADER** and the private data.</span></span>

<span data-ttu-id="e764e-111">如果您使用的是 MediaFoundation，您可以藉由呼叫 [**MFCreateAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype)，從 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)介面建立 [**sql-dmo \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type)結構。</span><span class="sxs-lookup"><span data-stu-id="e764e-111">If you are using MediaFoundation you can construct a [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure from an [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface by calling [**MFCreateAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype).</span></span>

<span data-ttu-id="e764e-112">在第一次設定編碼器的屬性之後，您必須使用取得的編解碼器私用資料。</span><span class="sxs-lookup"><span data-stu-id="e764e-112">You must use the codec private data obtained after first setting the properties on the encoder.</span></span> <span data-ttu-id="e764e-113">如果有任何屬性變更，您就必須取得新的私用資料。</span><span class="sxs-lookup"><span data-stu-id="e764e-113">If any properties are changed, you must get new private data.</span></span> <span data-ttu-id="e764e-114">如果您未在針對編碼會話設定所有屬性之後，使用所取得的私用資料，則編碼器可能無法解壓縮資料。</span><span class="sxs-lookup"><span data-stu-id="e764e-114">If you do not use the private data obtained after all the properties are set for the encoding session, the decoder may not be able to decompress the data.</span></span>

<span data-ttu-id="e764e-115">下列程式碼範例示範如何取得影片類型的私用資料：</span><span class="sxs-lookup"><span data-stu-id="e764e-115">The following code example demonstrates how to obtain the private data for a video type:</span></span>


```
HRESULT GetFinalOutputType(DMO_MEDIA_TYPE* pMedia, IMediaObject* pDMO)
{
    // WARNING //
    // This function does not deallocate the memory pointed to by 
    // pMedia->pbFormat. If the VIDEOINFOHEADER referenced by pbFormat
    // was dynamically allocated, a reference to it must be kept before
    //  calling this function so that it can be freed.

    // Perform simple parameter checks.
    if(pMedia == NULL || pDMO == NULL)
        return E_POINTER;
    if(pMedia->formattype != MEDIATYPE_VideoInfo)
        return E_INVALIDARG;

    HRESULT hr = S_OK;

    IWMCodecPrivateData* pPrivData = NULL;
    BYTE* pbData = NULL;
    DWORD cbData = 0;

    BYTE* pbNewVidInf  = NULL;
    DWORD cbNewVidInf  = 0;
    BYTE* pbNewPriv    = NULL;

    // Get the private data interface.
    hr = pDMO->QueryInterface(IID_IWMCodecPrivateData,
                              (void**)&pPrivData);
    GOTO_EXIT_IF_FAILED(hr);

    // Set the partial media type.
    hr = pPrivData->SetPartialOutputType(pMedia);
    GOTO_EXIT_IF_FAILED(hr);

    // Get the size of the private data.
    hr = pPrivData->GetPrivateData(NULL, &cbData);
    GOTO_EXIT_IF_FAILED(hr);

    // Allocate memory for the private data.
    pbData = new BYTE[cbData];
    if(pbData == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto Exit:
    }

    // Get the private data.
    hr = pPrivData->GetPrivateData(pbData, &cbData);

    // Allocate memory for the new VIDEOINFOHEADER.
    cbNewVidInf = pMedia->cbFormat + cbData;
    pbNewVidInf = new BYTE[cbNewVidInf];

    // Copy the VIDEOINFOHEADER to the new buffer.
    memcpy((void*)pbNewVidInf, (void*)pMedia->pbFormat, pMedia->cbFormat);

    // Get the address of the first byte following the VIDEOINFOHEADER.
    pbNewPriv = pbNewVidInf + pMedia->cbFormat;

    // Copy the private data to the new buffer.
    memcpy((void*)pbNewPriv, (void*)pbData, cbData);

    // Set the new VIDEOINFOHEADER in the DMO_MEDIA_TYPE.
    pMedia->pbFormat = pbNewVidInf;
    pMedia->cbFormat = cbNewVidInf;

Exit:
    SAFE_RELEASE(pPrivData);
    SAFE_ARRAY_DELETE(pbData);
    pbNewPriv = NULL;
    return hr;
}
```



> [!Note]  
> <span data-ttu-id="e764e-116">影片編碼器所傳遞的編解碼器私用資料，不保證與相同設定的相同編解碼器的不同執行所提供的私用資料相同。</span><span class="sxs-lookup"><span data-stu-id="e764e-116">The codec private data delivered by a video encoder is not guaranteed to be the same as the private data delivered by a different implementation of the same codec for the same configuration.</span></span> <span data-ttu-id="e764e-117">您必須一律使用本主題中的步驟來產生此值;永遠不會從另一個檔案複製私用資料。</span><span class="sxs-lookup"><span data-stu-id="e764e-117">You must always generate this value using the steps in this topic; never copy the private data from another file.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e764e-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="e764e-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e764e-119">設定影片編碼</span><span class="sxs-lookup"><span data-stu-id="e764e-119">Configuring Video Encoding</span></span>](configuringvideoencoding.md)
</dt> <dt>

[<span data-ttu-id="e764e-120">使用影片</span><span class="sxs-lookup"><span data-stu-id="e764e-120">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 

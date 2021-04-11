---
description: 設定 WMV 編碼器
ms.assetid: 6e690d17-da17-452a-aa9a-9701a560856b
title: 設定 WMV 編碼器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6324071257dd9d56e33d1dc6ece4886ee73661ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111844"
---
# <a name="configuring-a-wmv-encoder"></a><span data-ttu-id="1e789-103">設定 WMV 編碼器</span><span class="sxs-lookup"><span data-stu-id="1e789-103">Configuring a WMV Encoder</span></span>

<span data-ttu-id="1e789-104">若要建立 Windows Media 視訊 (WMV) 編碼器的有效輸出類型，您必須擁有下列資訊：</span><span class="sxs-lookup"><span data-stu-id="1e789-104">To create a valid output type for a Windows Media Video (WMV) encoder, you must have the following information:</span></span>

-   <span data-ttu-id="1e789-105">您將編碼之未壓縮影片的格式。</span><span class="sxs-lookup"><span data-stu-id="1e789-105">The format of the uncompressed video that you will encode.</span></span>
-   <span data-ttu-id="1e789-106">Repesents 編碼的 WMV 格式的影片子類型。</span><span class="sxs-lookup"><span data-stu-id="1e789-106">The video subtype that repesents the encoded WMV format.</span></span> <span data-ttu-id="1e789-107">請參閱 [影片子類型 guid](video-subtype-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="1e789-107">See [Video Subtype GUIDs](video-subtype-guids.md).</span></span>
-   <span data-ttu-id="1e789-108">編碼資料流程的目標位元速率。</span><span class="sxs-lookup"><span data-stu-id="1e789-108">The target bitrate for the encoded stream.</span></span>
-   <span data-ttu-id="1e789-109">要在編碼器上設定的設定屬性。</span><span class="sxs-lookup"><span data-stu-id="1e789-109">The configuration properties to set on the encoder.</span></span>

<span data-ttu-id="1e789-110">設定屬性記載于 Windows Media 音訊和影片編解碼器和 DSP Api 檔中。</span><span class="sxs-lookup"><span data-stu-id="1e789-110">The configuration properties are documented in the Windows Media Audio and Video Codec and DSP APIs documentation.</span></span> <span data-ttu-id="1e789-111">如需詳細資訊，請參閱 [編碼屬性](configuring-the-encoder.md)中的「影片資料流程屬性」。</span><span class="sxs-lookup"><span data-stu-id="1e789-111">For more information, see "Video Stream Properties" in [Encoding Properties](configuring-the-encoder.md).</span></span>

<span data-ttu-id="1e789-112">若要取得編碼器的有效輸出型別，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="1e789-112">To get a valid output type for the encoder, perform the following steps.</span></span>

1.  <span data-ttu-id="1e789-113">使用 [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) 或 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) 函數來建立編碼器的實例。</span><span class="sxs-lookup"><span data-stu-id="1e789-113">Use the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) or [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function to create an instance of the encoder.</span></span>
2.  <span data-ttu-id="1e789-114">查詢編碼器以取得 **IPropertyStore** 介面。</span><span class="sxs-lookup"><span data-stu-id="1e789-114">Query the encoder for the **IPropertyStore** interface.</span></span>
3.  <span data-ttu-id="1e789-115">使用 **IPropertyStore** 介面設定編碼器。</span><span class="sxs-lookup"><span data-stu-id="1e789-115">Use the **IPropertyStore** interface to configure the encoder.</span></span>
4.  <span data-ttu-id="1e789-116">呼叫 [**IMFTransform：： SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) ，以在編碼器上設定未壓縮的影片類型。</span><span class="sxs-lookup"><span data-stu-id="1e789-116">Call [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) to set the uncompressed video type on the encoder.</span></span>
5.  <span data-ttu-id="1e789-117">呼叫 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) ，以從編碼器取得壓縮格式的清單。</span><span class="sxs-lookup"><span data-stu-id="1e789-117">Call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) to get the list of compression formats from the encoder.</span></span> <span data-ttu-id="1e789-118">WMV 編碼器不會從這個方法傳回完整的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="1e789-118">The WMV encoders do not return a complete media type from this method.</span></span> <span data-ttu-id="1e789-119">媒體類型缺少兩項資訊：</span><span class="sxs-lookup"><span data-stu-id="1e789-119">The media types are missing two pieces of information:</span></span>

    -   <span data-ttu-id="1e789-120">目標位元速率。</span><span class="sxs-lookup"><span data-stu-id="1e789-120">The target bitrate.</span></span>
    -   <span data-ttu-id="1e789-121">編碼器中的私用編解碼器資料。</span><span class="sxs-lookup"><span data-stu-id="1e789-121">Private codec data from the encoder.</span></span>

    <span data-ttu-id="1e789-122">在編碼器上設定輸出類型之前，您必須將這兩個專案新增至媒體類型。</span><span class="sxs-lookup"><span data-stu-id="1e789-122">Before setting the output type on the encoder, you must add both of these items to the media type.</span></span>

6.  <span data-ttu-id="1e789-123">若要指定目標位元速率，請在媒體類型上設定 [ [**MF \_ MT \_ 平均 \_ 位元速率**](mf-mt-avg-bitrate-attribute.md) ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="1e789-123">To specify the target bitrate, set the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute on the media type.</span></span>
7.  <span data-ttu-id="1e789-124">將私用編解碼器資料新增至媒體類型，如下一節中所述。</span><span class="sxs-lookup"><span data-stu-id="1e789-124">Add the private codec data to the media type, as explained in the next section.</span></span>
8.  <span data-ttu-id="1e789-125">呼叫 [**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) 來設定編碼器上的壓縮媒體類型。</span><span class="sxs-lookup"><span data-stu-id="1e789-125">Call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) to set the compression media type on the encoder.</span></span>

### <a name="private-codec-data"></a><span data-ttu-id="1e789-126">私用編解碼器資料</span><span class="sxs-lookup"><span data-stu-id="1e789-126">Private Codec Data</span></span>

<span data-ttu-id="1e789-127">私用編解碼器資料是不透明的資料結構，您必須從 WMV 編碼器取得該資料結構，並新增至壓縮類型，才能在編碼器上設定壓縮類型。</span><span class="sxs-lookup"><span data-stu-id="1e789-127">The private codec data is an opaque data structure that you must get from the WMV encoder and add to the compression type, before setting the compression type on the encoder.</span></span> <span data-ttu-id="1e789-128">若要取得私用資料，您必須使用 Windows Media Format 11 SDK 中記載的 **IWMCodecPrivateData** 介面。</span><span class="sxs-lookup"><span data-stu-id="1e789-128">To get the private data, you must use the **IWMCodecPrivateData** interface, which is documented in the Windows Media Format 11 SDK.</span></span>

<span data-ttu-id="1e789-129">若要取得私用編解碼器資料，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="1e789-129">To get the private codec data, perform the following steps:</span></span>

1.  <span data-ttu-id="1e789-130">呼叫 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) ，以從編碼器取得媒體類型。</span><span class="sxs-lookup"><span data-stu-id="1e789-130">Call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) to get a media type from the encoder.</span></span> <span data-ttu-id="1e789-131"> (這是上一節中的步驟6。 ) </span><span class="sxs-lookup"><span data-stu-id="1e789-131">(This is step 6 from the previous section.)</span></span>
2.  <span data-ttu-id="1e789-132">在媒體類型上設定 [ [**MF \_ MT \_ 平均 \_ 位元速率**](mf-mt-avg-bitrate-attribute.md) ] 屬性，以指定目標位元速率。</span><span class="sxs-lookup"><span data-stu-id="1e789-132">Specify the target bitrate by setting the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute on the media type.</span></span>
3.  <span data-ttu-id="1e789-133">藉由呼叫 [**MFInitAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfinitammediatypefrommfmediatype)函式，將媒體類型轉換為一 [**\_ \_ 種媒體類型**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type)結構。</span><span class="sxs-lookup"><span data-stu-id="1e789-133">Convert the media type into a [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure by calling the [**MFInitAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfinitammediatypefrommfmediatype) function.</span></span>
4.  <span data-ttu-id="1e789-134">查詢編碼器以取得 **IWMCodecPrivateData** 介面。</span><span class="sxs-lookup"><span data-stu-id="1e789-134">Query the encoder for the **IWMCodecPrivateData** interface.</span></span>
5.  <span data-ttu-id="1e789-135">呼叫 **IWMCodecPrivateData：： SetPartialOutputType** 方法，並傳入轉換的 [**sql-dmo \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) 結構。</span><span class="sxs-lookup"><span data-stu-id="1e789-135">Call the **IWMCodecPrivateData::SetPartialOutputType** method, passing in the converted [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure.</span></span>
6.  <span data-ttu-id="1e789-136">呼叫 **IWMCodecPrivateData：： GetPrivateData** 方法兩次，一次取得私用資料的緩衝區大小，以及將資料複製到緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1e789-136">Call the **IWMCodecPrivateData::GetPrivateData** method twice, once to get the size of the buffer for the private data, and once to copy the data into the buffer.</span></span>
7.  <span data-ttu-id="1e789-137">藉由在類型上設定 [**MF \_ MT \_ 使用者 \_ 資料**](mf-mt-user-data-attribute.md) 屬性，將私用資料新增至媒體類型。</span><span class="sxs-lookup"><span data-stu-id="1e789-137">Add the private data to the media type by setting the [**MF\_MT\_USER\_DATA**](mf-mt-user-data-attribute.md) attribute on the type.</span></span>

<span data-ttu-id="1e789-138">下列擴充的範例顯示如何從未壓縮的影片類型建立 WMV 壓縮格式：</span><span class="sxs-lookup"><span data-stu-id="1e789-138">The following extended example shows how to create a WMV compression format from an uncompressed video type:</span></span>


```C++
#include <wmcodecdsp.h>
#include <Wmsdk.h>
#include <Dmo.h>
#include <mfapi.h>
#include <uuids.h>

#include <mfidl.h>
#include <mftransform.h>
#include <mferror.h>

#pragma comment(lib, "Msdmo")
#pragma comment(lib, "mfplat")
#pragma comment(lib, "mfuuid")
#pragma comment(lib, "strmiids")
#pragma comment(lib, "propsys")

HRESULT GetEncodedVideoType(
    IMFMediaType *pTypeIn, 
    REFGUID subtype,
    UINT32 TargetBitrate, 
    IPropertyStore *pEncoderProps, 
    IMFMediaType **ppEncodingType,
    DWORD mftEnumFlags = MFT_ENUM_FLAG_SYNCMFT
    );

HRESULT CreateVideoEncoder(REFGUID subtype, DWORD mftEnumFlags, IMFTransform **ppMFT);
HRESULT AddPrivateData(IMFTransform *pMFT, IMFMediaType *pTypeOut);
HRESULT CopyPropertyStore(IPropertyStore *pSrc, IPropertyStore *pDest);

//
// GetEncodedVideoType
// Given an uncompressed video type, finds a suitable WMV type.
//

HRESULT GetEncodedVideoType(
    IMFMediaType *pTypeIn,          // Uncompressed format
    REFGUID subtype,                // Compression format
    UINT32 TargetBitrate,           // Target bit rate
    IPropertyStore *pEncoderProps,  // Encoder properties (can be NULL)
    IMFMediaType **ppEncodingType,  // Receives the WMV type.
    DWORD mftEnumFlags              // MFTEnumEx flags
    )
{
    HRESULT hr = S_OK;

    IMFTransform *pMFT = NULL;
    IPropertyStore *pPropStore = NULL;
    IMFMediaType *pTypeOut = NULL;

    // Instantiate the encoder
    hr = CreateVideoEncoder(subtype, mftEnumFlags, &pMFT);

    // Copy the properties to the encoder.

    if (SUCCEEDED(hr))
    {
        if (pEncoderProps)
        {
            hr = pMFT->QueryInterface(IID_PPV_ARGS(&pPropStore));

            if (SUCCEEDED(hr))
            {
                hr = CopyPropertyStore(pEncoderProps, pPropStore);
            }
        }
    }

    // Set the uncompressed type.
    if (SUCCEEDED(hr))
    {
        hr = pMFT->SetInputType(0, pTypeIn, 0);
    }

    // Get the partial output type
    if (SUCCEEDED(hr))
    {
        hr = pMFT->GetOutputAvailableType(0, 0, &pTypeOut);
    }

    // Set the bit rate.
    // You must set this before getting the codec private data.

    if (SUCCEEDED(hr))
    {
        hr = pTypeOut->SetUINT32(MF_MT_AVG_BITRATE, TargetBitrate);   
    }

    if (SUCCEEDED(hr))
    {
        hr = AddPrivateData(pMFT, pTypeOut);
    }

    if (SUCCEEDED(hr))
    {
        hr = pMFT->SetOutputType(0, pTypeOut, 0);
    }

    if (SUCCEEDED(hr))
    {
        *ppEncodingType = pTypeOut;
        (*ppEncodingType)->AddRef();
    }

    SafeRelease(&pMFT);
    SafeRelease(&pPropStore);
    SafeRelease(&pTypeOut);
    return hr;
}
```



<span data-ttu-id="1e789-139">CreateVideoEncoder 函式會為指定的影片子類型建立影片編碼器，例如 **MFVideoFormat \_ WMV3**：</span><span class="sxs-lookup"><span data-stu-id="1e789-139">The CreateVideoEncoder function creates a video encoder for a specified video subtype, such as **MFVideoFormat\_WMV3**:</span></span>


```C++
//
// CreateVideoEncoder
// Creates a video encoder for a specified video subtype.
//

HRESULT CreateVideoEncoder(
    REFGUID subtype,            // Encoding subtype.
    DWORD mftEnumFlags,         // Flags for MFTEnumEx
    IMFTransform **ppMFT        // Receives a pointer to the encoder.
    )
{
    HRESULT hr = S_OK;
    IMFTransform *pMFT = NULL;

    MFT_REGISTER_TYPE_INFO info;
    info.guidMajorType = MFMediaType_Video;
    info.guidSubtype = subtype;

    IMFActivate **ppActivates = NULL;    
    UINT32 count = 0;

    hr = MFTEnumEx(
        MFT_CATEGORY_VIDEO_ENCODER,
        mftEnumFlags | MFT_ENUM_FLAG_SORTANDFILTER,
        NULL,
        &info,
        &ppActivates,
        &count
        );

    if (count == 0)
    {
        hr = E_FAIL;
    }

    if (SUCCEEDED(hr))
    {
        hr = ppActivates[0]->ActivateObject(
            __uuidof(IMFTransform),
            (void**)&pMFT
            );
    }

    if (SUCCEEDED(hr))
    {
        *ppMFT = pMFT;
        (*ppMFT)->AddRef();
    }

    // Clean up

    for (DWORD i = 0; i < count; i++)
    {
        ppActivates[i]->Release();
    }
    CoTaskMemFree(ppActivates);
    SafeRelease(&pMFT);
    return hr;
}
```



<span data-ttu-id="1e789-140">AddPrivateData 函式會將私用編解碼器資料新增至壓縮類型：</span><span class="sxs-lookup"><span data-stu-id="1e789-140">The AddPrivateData function adds the private codec data to the compression type:</span></span>


```C++
//
// AddPrivateData
// Appends the private codec data to a media type.
//
// pMFT: The video encoder
// pTypeOut: A video type from the encoder's type list.
//
// The function modifies pTypeOut by adding the codec data.
//

HRESULT AddPrivateData(IMFTransform *pMFT, IMFMediaType *pTypeOut)
{
    HRESULT hr = S_OK;
    ULONG cbData = 0;
    BYTE *pData = NULL;

    IWMCodecPrivateData *pPrivData = NULL;

    DMO_MEDIA_TYPE mtOut = { 0 };

    // Convert the type to a DMO type.
    hr = MFInitAMMediaTypeFromMFMediaType(
        pTypeOut, 
        FORMAT_VideoInfo, 
        (AM_MEDIA_TYPE*)&mtOut
        );
    
    if (SUCCEEDED(hr))
    {
        hr = pMFT->QueryInterface(IID_PPV_ARGS(&pPrivData));
    }

    if (SUCCEEDED(hr))
    {
        hr = pPrivData->SetPartialOutputType(&mtOut);
    }

    //
    // Get the private codec data
    //

    // First get the buffer size.
    if (SUCCEEDED(hr))
    {
        hr = pPrivData->GetPrivateData(NULL, &cbData);
    }

    if (SUCCEEDED(hr))
    {
        pData = new BYTE[cbData];

        if (pData == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
    }

    // Now get the data.
    if (SUCCEEDED(hr))
    {
        hr = pPrivData->GetPrivateData(pData, &cbData);
    }

    // Add the data to the media type.
    if (SUCCEEDED(hr))
    {
        hr = pTypeOut->SetBlob(MF_MT_USER_DATA, pData, cbData);
    }

    delete [] pData;
    MoFreeMediaType(&mtOut);
    SafeRelease(&pPrivData);
    return hr;
}
```



<span data-ttu-id="1e789-141">CopyPropertyStore 函式是協助程式函式，可將屬性從一個屬性存放區複製到另一個：</span><span class="sxs-lookup"><span data-stu-id="1e789-141">The CopyPropertyStore function is a helper function that copies properties from one property store to another:</span></span>


```C++
//
// CopyPropertyStore
// Helper function to copy properties from one property
// store to another property store.
//

HRESULT CopyPropertyStore(IPropertyStore *pSrc, IPropertyStore *pDest)
{
    HRESULT hr = S_OK;
    DWORD cProps = 0;

    PROPERTYKEY key;
    PROPVARIANT var;

    PropVariantInit(&var);

    hr = pSrc->GetCount(&cProps);

    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cProps; i++)
        {
            hr = pSrc->GetAt(i, &key);

            if (FAILED(hr)) { break; }

            hr = pSrc->GetValue(key, &var);

            if (FAILED(hr)) { break; }

            hr = pDest->SetValue(key, var);

            if (FAILED(hr)) { break; }

            PropVariantClear(&var);
        }
    }

    PropVariantClear(&var);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="1e789-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="1e789-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e789-143">具現化編碼器 MFT</span><span class="sxs-lookup"><span data-stu-id="1e789-143">Instantiating an Encoder MFT</span></span>](instantiating-the-encoder-mft.md)
</dt> <dt>

[<span data-ttu-id="1e789-144">Windows Media 編碼器</span><span class="sxs-lookup"><span data-stu-id="1e789-144">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 

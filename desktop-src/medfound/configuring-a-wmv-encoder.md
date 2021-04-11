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
# <a name="configuring-a-wmv-encoder"></a>設定 WMV 編碼器

若要建立 Windows Media 視訊 (WMV) 編碼器的有效輸出類型，您必須擁有下列資訊：

-   您將編碼之未壓縮影片的格式。
-   Repesents 編碼的 WMV 格式的影片子類型。 請參閱 [影片子類型 guid](video-subtype-guids.md)。
-   編碼資料流程的目標位元速率。
-   要在編碼器上設定的設定屬性。

設定屬性記載于 Windows Media 音訊和影片編解碼器和 DSP Api 檔中。 如需詳細資訊，請參閱 [編碼屬性](configuring-the-encoder.md)中的「影片資料流程屬性」。

若要取得編碼器的有效輸出型別，請執行下列步驟。

1.  使用 [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) 或 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) 函數來建立編碼器的實例。
2.  查詢編碼器以取得 **IPropertyStore** 介面。
3.  使用 **IPropertyStore** 介面設定編碼器。
4.  呼叫 [**IMFTransform：： SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) ，以在編碼器上設定未壓縮的影片類型。
5.  呼叫 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) ，以從編碼器取得壓縮格式的清單。 WMV 編碼器不會從這個方法傳回完整的媒體類型。 媒體類型缺少兩項資訊：

    -   目標位元速率。
    -   編碼器中的私用編解碼器資料。

    在編碼器上設定輸出類型之前，您必須將這兩個專案新增至媒體類型。

6.  若要指定目標位元速率，請在媒體類型上設定 [ [**MF \_ MT \_ 平均 \_ 位元速率**](mf-mt-avg-bitrate-attribute.md) ] 屬性。
7.  將私用編解碼器資料新增至媒體類型，如下一節中所述。
8.  呼叫 [**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) 來設定編碼器上的壓縮媒體類型。

### <a name="private-codec-data"></a>私用編解碼器資料

私用編解碼器資料是不透明的資料結構，您必須從 WMV 編碼器取得該資料結構，並新增至壓縮類型，才能在編碼器上設定壓縮類型。 若要取得私用資料，您必須使用 Windows Media Format 11 SDK 中記載的 **IWMCodecPrivateData** 介面。

若要取得私用編解碼器資料，請執行下列步驟：

1.  呼叫 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) ，以從編碼器取得媒體類型。  (這是上一節中的步驟6。 ) 
2.  在媒體類型上設定 [ [**MF \_ MT \_ 平均 \_ 位元速率**](mf-mt-avg-bitrate-attribute.md) ] 屬性，以指定目標位元速率。
3.  藉由呼叫 [**MFInitAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfinitammediatypefrommfmediatype)函式，將媒體類型轉換為一 [**\_ \_ 種媒體類型**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type)結構。
4.  查詢編碼器以取得 **IWMCodecPrivateData** 介面。
5.  呼叫 **IWMCodecPrivateData：： SetPartialOutputType** 方法，並傳入轉換的 [**sql-dmo \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) 結構。
6.  呼叫 **IWMCodecPrivateData：： GetPrivateData** 方法兩次，一次取得私用資料的緩衝區大小，以及將資料複製到緩衝區。
7.  藉由在類型上設定 [**MF \_ MT \_ 使用者 \_ 資料**](mf-mt-user-data-attribute.md) 屬性，將私用資料新增至媒體類型。

下列擴充的範例顯示如何從未壓縮的影片類型建立 WMV 壓縮格式：


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



CreateVideoEncoder 函式會為指定的影片子類型建立影片編碼器，例如 **MFVideoFormat \_ WMV3**：


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



AddPrivateData 函式會將私用編解碼器資料新增至壓縮類型：


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



CopyPropertyStore 函式是協助程式函式，可將屬性從一個屬性存放區複製到另一個：


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[具現化編碼器 MFT](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Media 編碼器](windows-media-encoders.md)
</dt> </dl>

 

 

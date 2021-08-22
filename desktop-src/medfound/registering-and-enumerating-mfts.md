---
description: 本節說明如何列舉媒體基礎轉換，以及如何註冊自訂的 MFT，讓應用程式可以探索它。
ms.assetid: 76d2a703-4162-428e-a4ff-643e346eacfb
title: 註冊和列舉 MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a3110351479f2a906d68b6c054d9e23886cbcd4cdb031fc8a4951a1d4b8d1e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119101827"
---
# <a name="registering-and-enumerating-mfts"></a>註冊和列舉 MFTs

本節說明如何列舉媒體基礎轉換，以及如何註冊自訂的 MFT，讓應用程式可以探索它。

-   [列舉 MFTs](#registering-and-enumerating-mfts)
-   [註冊 MFTs](#registering-mfts)
-   [相關主題](#related-topics)

## <a name="enumerating-mfts"></a>列舉 MFTs

若要探索在系統上註冊的 MFTs，應用程式可以呼叫 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) 函數。

> [!Note]  
> 此函數需要 Windows 7。 在 Windows 7 之前，應用程式應該改用 [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum)函數。

 

此函式會採用下列資訊作為輸入：

-   要列舉的 MFT 類別，例如影片解碼或音訊解碼器。
-   要比對的輸入或輸出格式。
-   指定其他搜尋條件的旗標。

此函式會傳回 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 指標的陣列，每個指標都代表符合列舉準則的一個 MFT。

例如，下列程式碼會列舉 Windows Media 視訊的解碼器：


```C++
HRESULT hr = S_OK;
UINT32 count = 0;

IMFActivate **ppActivate = NULL;    // Array of activation objects.
IMFTransform *pDecoder = NULL;      // Pointer to the decoder.

// Match WMV3 video.
MFT_REGISTER_TYPE_INFO info = { MFMediaType_Video, MFVideoFormat_WMV3 };

UINT32 unFlags = MFT_ENUM_FLAG_SYNCMFT  | 
                 MFT_ENUM_FLAG_LOCALMFT | 
                 MFT_ENUM_FLAG_SORTANDFILTER;

hr = MFTEnumEx(
    MFT_CATEGORY_VIDEO_DECODER,
    unFlags,
    &info,      // Input type
    NULL,       // Output type
    &ppActivate,
    &count
    );


if (SUCCEEDED(hr) && count == 0)
{
    hr = MF_E_TOPO_CODEC_NOT_FOUND;
}

// Create the first decoder in the list.

if (SUCCEEDED(hr))
{
    hr = ppActivate[0]->ActivateObject(IID_PPV_ARGS(&pDecoder));
}

for (UINT32 i = 0; i < count; i++)
{
    ppActivate[i]->Release();
}
CoTaskMemFree(ppActivate);
```



根據預設，某些類型的 MFT 會從列舉中排除，包括非同步 MFTs、硬體 MFTs，以及使用「使用中」 restructions 的 MFTs。 這些會被排除，因為它們都需要某種類型的特殊處理。 使用 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)的 *Flags* 參數變更預設值。 例如，若要在列舉結果中包含硬體 MFTs，請設定 **MFT \_ 列舉 \_ 旗標 \_ 硬體** 旗標：


```C++
UINT32 unFlags = MFT_ENUM_FLAG_HARDWARE |
                 MFT_ENUM_FLAG_SYNCMFT  | 
                 MFT_ENUM_FLAG_LOCALMFT | 
                 MFT_ENUM_FLAG_SORTANDFILTER;
hr = MFTEnumEx(
    MFT_CATEGORY_VIDEO_DECODER,
    unFlags,
    &info,      // Input type
    NULL,       // Output type
    &ppActivate,
    &count
    );
```



## <a name="registering-mfts"></a>註冊 MFTs

當您註冊媒體基礎轉換 (MFT) 時，會將兩種類型的資訊寫入登錄：

-   MFT 的 CLSID，讓用戶端可以呼叫 **CoCreateInstance** 或 **CoGetClassObject** 來建立該 mft 的實例。 此登錄專案會遵循 COM class factory 的標準格式。 如需詳細資訊，請參閱 (COM) 的元件物件模型 Windows SDK 檔。
-   可讓應用程式依功能類別列舉 MFTs 的資訊。

若要在登錄中建立 MFT 列舉專案，請呼叫 [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) 函數。 您可以包含下列有關 MFT 的資訊：

-   MFT 的類別，例如影片編碼器或影片編碼器。 如需分類清單，請參閱 [**MFT \_ 類別目錄**](mft-category.md)。
-   MFT 支援的輸入和輸出格式清單。 每種格式都是由主要類型和子類型所定義。  (若要取得更詳細的格式資訊，用戶端必須建立 MFT 並呼叫 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 方法。 ) 拓撲載入器會在解析部分拓撲時使用此資訊。

若要從登錄中移除專案，請呼叫 [**MFTUnregister**](/windows/desktop/api/mfapi/nf-mfapi-mftunregister)。

下列程式碼說明如何註冊 MFT。 此範例假設 MFT 是支援輸入和輸出相同格式的影片效果。


```C++
// CLSID of the MFT.
extern const GUID CLSID_MyVideoEffectMFT;

// DllRegisterServer: Creates the registry entries.
STDAPI DllRegisterServer()
{
    HRESULT hr = S_OK;

    // Array of media types.
    MFT_REGISTER_TYPE_INFO aMediaTypes[] =
    {
        {   MFMediaType_Video, MFVideoFormat_NV12 },
        {   MFMediaType_Video, MFVideoFormat_YUY2 },
        {   MFMediaType_Video, MFVideoFormat_UYVY },
    };

    // Size of the array.
    const DWORD cNumMediaTypes = ARRAY_SIZE(aMediaTypes);

    hr = MFTRegister(
        CLSID_MyVideoEffectMFT,     // CLSID.
        MFT_CATEGORY_VIDEO_EFFECT,  // Category.
        L"My Video Effect",         // Friendly name.
        0,                          // Reserved, must be zero.
        cNumMediaTypes,             // Number of input types.
        aMediaTypes,                // Input types.
        cNumMediaTypes,             // Number of output types.
        aMediaTypes,                // Output types.
        NULL                        // Attributes (optional).
        );

    if (SUCCEEDED(hr))
    {
        // Register the CLSID for CoCreateInstance (not shown).
    }
    return hr;
}

// DllUnregisterServer: Removes the registry entries.
STDAPI DllUnregisterServer()
{
    HRESULT hr = MFTUnregister(CLSID_MyVideoEffectMFT);

    // Unregister the CLSID for CoCreateInstance (not shown).

    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用限制領域](field-of-use-restrictions.md)
</dt> <dt>

[媒體基礎轉換](media-foundation-transforms.md)
</dt> </dl>

 

 




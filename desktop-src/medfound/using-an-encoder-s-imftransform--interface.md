---
description: 若要將媒體檔案轉換成 ASF 格式，您可以使用 Windows 媒體編碼器。 瞭解如何使用 CoCreateInstance 建立編碼器。
ms.assetid: 96f19dfb-a328-41db-8fa8-77f052b1a192
title: 使用 CoCreateInstance 建立編碼器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbd48931b7bc8e0b449ee8ffaa0141a6413f2699ebaae6e1ba01fdd1f4b38a0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092318"
---
# <a name="creating-an-encoder-by-using-cocreateinstance"></a>使用 CoCreateInstance 建立編碼器

若要將媒體檔案轉換成 ASF 格式，您可以使用 Windows 媒體編碼器。 若要使用這些編碼器，必須向系統註冊。 編碼器會實作為 [媒體基礎轉換](media-foundation-transforms.md) (MFTs) 且必須公開 IMFTransform 介面。 本主題說明應用程式如何取得所需的 MFT 編碼器 IMFTransform 介面的指標，並將其具現化以供使用。

如需編碼器註冊的相關資訊，請參閱具現 [化編碼器 MFT](instantiating-the-encoder-mft.md)。

-   [使用編碼器的 IMFTransform 介面](#creating-an-encoder-by-using-cocreateinstance)
    -   [編碼器建立範例](#encoder-creation-example)
-   [相關主題](#related-topics)

## <a name="using-an-encoders-imftransform-interface"></a>使用編碼器的 IMFTransform 介面

成功向系統註冊 Windows 媒體編碼器之後，應用程式就可以藉由呼叫 [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum)來列舉編碼器。 若要搜尋正確的編碼器，您必須指定下列各項：

-   代表分類的 GUID，也就是 **mft \_ 類別 \_ 音訊 \_ 編碼器** 或 **mft 類別的 \_ \_ 影片 \_ 編碼器**。

-   要比對的格式。 這是設定在 [**MFT 登錄 \_ \_ 類型 \_ 資訊**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) 結構中，指定編碼器將在其中產生範例之媒體類型的主要類型和子類型。 此結構會在 *pOutputType* 參數中傳遞。 如需支援類型的詳細資訊，請參閱 [媒體類型 guid](media-type-guids.md)。

    > [!Note]  
    > *PInputType* 參數中的輸入類型資訊不是必要的。 這是因為應用程式知道輸入型別，而編碼器預期輸入資料流程的格式不是壓縮。

     

[**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) 會傳回符合搜尋準則之編碼器 MFTs 的 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 指標陣列。 您可以呼叫 COM 函式 **CoCreateInstance** 來具現化編碼器，並傳遞您要使用之編碼器的 CLSID。 此函式會傳回代表編碼器之 **IMFTransform** 介面的指標。 如需此函式呼叫的詳細資訊，請參閱 (COM) 的元件物件模型 Windows SDK 檔。

### <a name="encoder-creation-example"></a>編碼器建立範例

下列程式碼範例顯示如何建立音訊或影片編碼器。


```C++
HRESULT FindEncoder(
    const GUID& subtype, 
    BOOL bAudio, 
    IMFTransform **ppEncoder
    )
{
    HRESULT hr = S_OK;
    UINT32 count = 0;

    CLSID *ppCLSIDs = NULL;

    MFT_REGISTER_TYPE_INFO info = { 0 };

    info.guidMajorType = bAudio ? MFMediaType_Audio : MFMediaType_Video;
    info.guidSubtype = subtype;

    hr = MFTEnum(   
        bAudio ? MFT_CATEGORY_AUDIO_ENCODER : MFT_CATEGORY_VIDEO_ENCODER,
        0,          // Reserved
        NULL,       // Input type
        &info,      // Output type
        NULL,       // Reserved
        &ppCLSIDs,
        &count
        );

    if (SUCCEEDED(hr) && count == 0)
    {
        hr = MF_E_TOPO_CODEC_NOT_FOUND;
    }

    // Create the first encoder in the list.

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(ppCLSIDs[0], NULL,
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(ppEncoder));
    }

    CoTaskMemFree(ppCLSIDs);
    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[具現化編碼器 MFT](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows媒體編碼器](windows-media-encoders.md)
</dt> </dl>

 

 




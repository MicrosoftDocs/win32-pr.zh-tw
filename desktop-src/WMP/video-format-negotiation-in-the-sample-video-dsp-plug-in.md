---
title: 範例影片 DSP 外掛程式中的影片格式協調
description: 範例影片 DSP 外掛程式中的影片格式協調
ms.assetid: 3e92ce10-2b9b-4689-a181-f56c33472fea
keywords:
- Windows Media Player 外掛程式、影片 DSP
- 外掛程式、視頻 DSP
- 數位信號處理外掛程式、影片格式的協商
- DSP 外掛程式、影片格式的協商
- 影片 DSP 外掛程式，格式協商
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c287a38fbfcf11f1b9d74087a91c5825b22f1243
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301003"
---
# <a name="video-format-negotiation-in-the-sample-video-dsp-plug-in"></a>範例影片 DSP 外掛程式中的影片格式協調

在 Windows Media Player 將視頻 DSP 外掛程式插入信號鏈之前，播放程式必須判斷外掛程式是否可以處理所播放的影片。 外掛程式和播放程式用來與支援的影片格式進行通訊的程式稱為格式的協商。

## <a name="providing-the-supported-input-and-output-types"></a>提供支援的輸入和輸出類型

如果 DSP 外掛程式作為 DirectX 媒體物件 (的) ，播放程式會對 **IMediaObject：： GetInputType** 和 **IMediaObject：： GetOutputType** 進行一連串的呼叫，以查詢外掛程式的支援格式。

如果 DSP 外掛程式做為媒體基礎轉換 (MFT) ，則播放程式會對 **IMFTransform：： GetInputAvailableType** 和 **IMFTransform：： GetOutputAvailableType** 進行一連串的呼叫，藉以查詢外掛程式的支援格式。

Windows Media Player 外掛程式 Wizard 產生的範例影片外掛程式，會將支援的影片格式清單儲存為 Guid 陣列。 下列程式碼來自主要 .cpp 檔案：


```C++
static const GUID*    k_guidValidSubtypes[] = {
    &MEDIASUBTYPE_NV12,
    &MEDIASUBTYPE_YV12,
    &MEDIASUBTYPE_YUY2,
    &MEDIASUBTYPE_UYVY,
    &MEDIASUBTYPE_RGB32,
    &MEDIASUBTYPE_RGB24,
    &MEDIASUBTYPE RGB555,
    &MEDIASUBTYPE RGB565
};

```



播放程式可以依任何順序呼叫 **IMediaObject：： GetInputType** 和 **IMediaObject：： GetOutputType** ，因此外掛程式程式碼必須預期這一點。 同樣地，Player 可以依任何順序呼叫 **IMFTransform：： GetInputAvailableType** 和 **IMFTransform：： GetOutputAvailableType** 。 **GetOutputType** 和 **GetOutputAvailableType** 的範例執行會測試是否已定義輸入型別。 如果有，外掛程式會回應它只支援該類型。 否則，外掛程式會傳回對應至提供之索引的型別，如下列程式碼所示：


```C++
// If input type has been defined, then use that as output type.
if (GUID_NULL != m_mtInput.majortype)
{
    hr = ::MoCopyMediaType( pmt, &m_mtInput );
}
else // Otherwise use default for this plug-in.
{
    ::ZeroMemory( pmt, sizeof( DMO_MEDIA_TYPE ) );
    pmt->majortype = MEDIATYPE_Video;
    pmt->subtype = *k_guidValidSubtypes[dwTypeIndex];     
}

```



## <a name="setting-the-input-and-output-types"></a>設定輸入和輸出類型

如果 DSP 外掛程式是做為，Windows Media Player 藉由呼叫 **IMediaObject：： SetInputType** 和 **IMediaObject：： SetOutputType** 來設定媒體類型，並將代表所要求媒體 **類型的物件 \_ \_** 指標傳遞給每個函式。

如果 DSP 外掛程式做為 MFT，Windows Media Player 藉由呼叫 **IMFTransform：： SetInputType** 和 **IMFTransform：： SetOutputType** 來設定媒體類型，並將指向代表所要求媒體類型的 **IMFMediaType** 介面指標傳遞至每個函式。

不保證播放程式會以任何特定順序呼叫格式的協商方法，因此外掛程式程式碼必須處理任何大小寫。 比方說，如果播放程式在呼叫 **SetInputType** 之前呼叫 **SetOutputType** ，它是一種有效的動作，可讓外掛程式拒絕建議的輸出媒體類型。 下列 **IMediaObject：： SetOutputType** 範例中的程式碼示範：


```C++
if( GUID_NULL != m_mtInput.majortype )
{
    // Validate that the output media type matches our requirements 
    // and matches our input type (if set).
    hr = ValidateMediaType(pmt, &m_mtInput);
}
else
{
    hr = DMO_E_TYPE_NOT_ACCEPTED;
}

```



**SetInputType** 和 **SetOutputType** 的範例外掛程式實作為呼叫名為 **ValidateMediaType** 的自訂函數。 此外掛程式函式會針對建議的媒體類型執行一系列的測試，以確保媒體類型的格式是否正確且受外掛程式支援。 **ValidateMediaType** 會執行下列測試：

-   確認 **majortype** 和 **formattype** 成員包含正確的值。
-   確認 **子類型** 成員符合其中一個支援的格式。
-   確認 **BITMAPINFOHEADER** 和 **VIDEOINFOHEADER** 或 **VIDEOINFOHEADER2** 結構中的資訊包含有效的值。
-   測試輸入和輸出媒體類型是否相符，因為外掛程式不會將格式從輸入轉換成輸出。

如果建議的媒體類型通過驗證測試，則會儲存在成員變數中：輸入媒體類型的 **m \_ mtInput** 、輸出媒體類型的 **m \_ mtOutput** 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**執行 Video DSP 外掛程式**](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 





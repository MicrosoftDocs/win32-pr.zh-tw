---
description: 具現化編解碼器 MFTs
ms.assetid: 171f9a0f-effb-4ed7-8aff-d7b1ee6e4973
title: 具現化編解碼器 MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a73af4055aee1d5b7e6a3ea137ab2204c9e59194f57ae4776e6c8368429db877
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827608"
---
# <a name="instantiating-codec-mfts"></a>具現化編解碼器 MFTs

[媒體基礎轉換](media-foundation-transforms.md) (MFTs) 是執行 [**IMFTRANSFORM**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面的 COM 物件。 MFT 是一種物件，可將多媒體資料轉換為管線的一部分。 管線是由媒體來源、媒體轉換和媒體接收所組成的有向非循環圖表。 管線會以非同步方式處理串流處理多媒體資料。

雖然 MFTs 可具現化並獨立于媒體基礎管線基礎結構之外使用，但最好盡可能使用 MediaFoundation 架構。

您可以藉由呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 函數來建立編解碼器 MFT。 您必須傳遞 MFT 的類別識別碼、 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)的介面識別碼，以及指向 **IMFTransform** 指標的指標。

編解碼器 MFTs 的類別識別碼會定義為 wmcodecdsp .h 標頭檔中的常數。

[**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)介面識別碼的常數是 IID \_ IMFTransform。

下列程式碼範例示範如何建立編解碼器 MFT 的實例：


```
HRESULT CreateVideoEncoderMFT(IMFTransform** ppMFT)
{
    if (ppMFT == NULL)
        return E_POINTER;

    return CoCreateInstance(CLSID_CWMV9EncMediaObject,
                            NULL,
                            CLSCTX_INPROC_SERVER, 
                            IID_IMFTransform, 
                            (void**)ppMFT);
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用編解碼器 MFTs](workingwithcodecmfts.md)
</dt> </dl>

 

 

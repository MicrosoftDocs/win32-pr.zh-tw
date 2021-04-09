---
description: 使用媒體範例
ms.assetid: 10b547b1-6624-4d49-9852-a5fff4eb70e7
title: 使用媒體範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a31fa8ff17c2dabcac9d110b530751d22fdf7b0
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103945600"
---
# <a name="working-with-media-samples"></a>使用媒體範例

本主題說明如何使用 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 介面操作媒體範例物件。 如需媒體範例的一般總覽，請參閱 [媒體範例](media-samples.md)。

若要建立新的媒體範例，請呼叫 [**MFCreateSample**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) 函數。 一開始，範例的緩衝區清單是空的。 若要在清單結尾加入緩衝區，請呼叫 [**IMFSample：： AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer)。

下列程式碼示範如何建立範例，並在其中新增緩衝區。


```C++
HRESULT CreateMediaSample(DWORD cbData, IMFSample **ppSample)
{
    HRESULT hr = S_OK;

    IMFSample *pSample = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    hr = MFCreateSample(&pSample);

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(cbData, &pBuffer);
    }

    if (SUCCEEDED(hr))
    {
        hr = pSample->AddBuffer(pBuffer);
    }

    if (SUCCEEDED(hr))
    {
        *ppSample = pSample;
        (*ppSample)->AddRef();
    }

    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



從範例取得緩衝區的建議方式是呼叫 [**IMFSample：： ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer)。 這個方法會傳回單一 continguous 緩衝區。

若要逐一查看清單中的緩衝區，請從呼叫 [**IMFSample：： GetBufferCount**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbuffercount)開始。 這個方法會傳回緩衝區的數目。 然後呼叫 [**IMFSample：： GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) ，並指定要取出的緩衝區索引。 緩衝區是從零開始編制索引。

下列程式碼示範如何逐一查看範例中的緩衝區。


```C++
IMFMediaBuffer *pBuffer = NULL;
DWORD cBuffers = 0;

hr = pSample->GetBufferCount(&cBuffers);

if (SUCCEEDED(hr))
{
    for (DWORD i = 0; i < cBuffers; i++)
    {
        hr = pSample->GetBufferByIndex(i, &pBuffer);

        // Use buffer (not shown).

        SafeRelease(&pBuffer);

        if (FAILED(hr))
        {
            break;
        }
    }
}
```



範例有時間戳記和持續時間。 時間戳記會指出應轉譯樣本中的資料（相對於呈現時鐘）。 持續時間是應呈現資料的時間長度。 通常產生資料的元件會設定初始時間戳記和持續時間。 媒體會話可能會修改這些值。 若要設定時間戳記，請呼叫 [**IMFSample：： SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime)。 若要設定持續時間，請呼叫 [**IMFSample：： SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration)。

範例也可以有屬性，其中包含有關範例的其他資訊。 如需範例屬性的清單，請參閱 [範例屬性](sample-attributes.md)。 若要設定和取出屬性，請使用 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)繼承的 [**IMFAttributes 介面**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體範例](media-samples.md)
</dt> <dt>

[媒體緩衝區](media-buffers.md)
</dt> </dl>

 

 




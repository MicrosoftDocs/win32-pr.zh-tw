---
description: 使用媒體緩衝區
ms.assetid: c7e079e0-99f3-4bff-9163-1c5a022c14ae
title: '使用媒體緩衝區 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c559e54d38c5a601a51bf3d6a879cbfe5b8403e1df48117e15d23f6264554437
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118736609"
---
# <a name="working-with-media-buffers-microsoft-media-foundation"></a>使用媒體緩衝區 (Microsoft 媒體基礎) 

本主題說明如何使用 [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) 介面存取媒體緩衝區中的資料。 所有媒體緩衝區都會公開 **IMFMediaBuffer**，這是針對任何類型的資料所設計。 未壓縮的影片畫面是特殊案例，如 [未壓縮的影片緩衝區](uncompressed-video-buffers.md)主題所述。

## <a name="buffer-size"></a>緩衝區大小

媒體緩衝區有兩種與其相關聯的大小：

-   *最大長度* 是配置給緩衝區之記憶體的實體大小。 當建立緩衝區時，就會設定此值，而且在緩衝區存留期內不會變更。 最大長度表示可儲存在緩衝區中的資料量。 若要尋找大小上限，請呼叫 [**IMFMediaBuffer：： GetMaxLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getmaxlength)。

-   目前的 *長度* 是目前在緩衝區中的有效資料量。 第一次配置緩衝區時，目前的長度為零，因為緩衝區中沒有有效的資料。 如果您將任何資料寫入至緩衝區，則必須藉由呼叫 [**IMFMediaBuffer：： SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength)來更新目前的長度。 例如，如果您將100個位元組的資料寫入緩衝區，請使用值100來呼叫 **SetCurrentLength** 。 如果您從媒體緩衝區讀取資料，請呼叫 [**IMFMediaBuffer：： GetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) ，以找出緩衝區目前的資料量。 請勿讀取超過目前的長度。 目前的長度絕不能超過緩衝區的最大長度。

## <a name="accessing-the-buffer-memory"></a>存取緩衝區記憶體

若要存取緩衝區中的記憶體，請呼叫 [**IMFMediaBuffer：： Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock)。 這個方法會傳回記憶體區塊開頭的指標。 它也會傳回最大長度和目前的長度。 當您使用指標完成時，請呼叫 [**IMFMediaBuffer：： Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock)。

若要將資料寫入媒體緩衝區：

1.  呼叫 [**IMFMediaBuffer：： Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) 以取得記憶體的指標。 方法也會傳回緩衝區的最大長度。
2.  將您的資料寫入記憶體，最多可達緩衝區的最大長度。
3.  呼叫 [**IMFMediaBuffer：： SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) ，以更新目前的長度。 將目前的長度設為等於您在步驟2中所撰寫的資料量。
4.  呼叫 [**IMFMediaBuffer：： unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) 以解除鎖定緩衝區。

從媒體緩衝區讀取資料：

1.  呼叫 [**IMFMediaBuffer：： Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) 以取得記憶體的指標。 方法也會傳回緩衝區目前的長度 (緩衝區) 中的有效資料量。
2.  讀取記憶體的內容，最多可達目前的長度。
3.  呼叫 [**IMFMediaBuffer：： unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) 以解除鎖定緩衝區。

## <a name="creating-system-memory-buffers"></a>建立系統記憶體緩衝區

系統記憶體緩衝區是管理系統記憶體區塊的媒體緩衝區。 若要建立這個物件的實例，請呼叫 [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) 或 [**MFCreateAlignedMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatealignedmemorybuffer) ，並指定緩衝區大小。 這兩個函數都會配置記憶體區塊，並傳回 [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) 指標。 當媒體緩衝區的參考計數到達零且物件已損毀時，就會自動釋放記憶體。

下列範例示範如何建立系統記憶體緩衝區，並寫入至緩衝區。


```C++
HRESULT CreateSystemMemoryBuffer(
    BYTE *pSrc, 
    DWORD cbData, 
    IMFMediaBuffer **ppBuffer
    )
{
    HRESULT hr = S_OK;
    BYTE *pData = NULL;

    IMFMediaBuffer *pBuffer = NULL;

    // Create the media buffer.
    hr = MFCreateMemoryBuffer(
        cbData,   // Amount of memory to allocate, in bytes.
        &pBuffer        
        );

    // Lock the buffer to get a pointer to the memory.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->Lock(&pData, NULL, NULL);
    }

    if (SUCCEEDED(hr))
    {
        memcpy_s(pData, cbData, pSrc, cbData);
    }

    // Update the current length.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbData);
    }

    // Unlock the buffer.
    if (pData)
    {
        hr = pBuffer->Unlock();
    }

    if (SUCCEEDED(hr))
    {
        *ppBuffer = pBuffer;
        (*ppBuffer)->AddRef();
    }

    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體緩衝區](media-buffers.md)
</dt> <dt>

[媒體基礎平臺 Api](media-foundation-platform-apis.md)
</dt> </dl>

 

 




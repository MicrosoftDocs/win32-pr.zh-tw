---
title: 執行 IMediaObject AllocateStreamingResources
description: 執行 IMediaObject AllocateStreamingResources
ms.assetid: 630550fe-2cca-4bfa-a824-a355f7fc5e02
keywords:
- Windows Media Player 外掛程式，Echo 範例串流資源
- 外掛程式，Echo 範例串流資源
- 數位信號處理外掛程式，Echo 範例串流資源
- DSP 外掛程式，Echo 範例串流資源
- Echo DSP 外掛程式範例，串流資源
- Echo DSP 外掛程式範例，延遲緩衝區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f1e347e35eaabbcbcc00a586e4cba0d8ad31cc6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372319"
---
# <a name="implementing-imediaobjectallocatestreamingresources"></a>執行 IMediaObject：： AllocateStreamingResources

在 Echo 範例中， **AllocateStreamingResources** 方法會建立延遲緩衝區。 做法是執行下列動作：

1.  計算對應至指定媒體類型之指定延遲時間的緩衝區大小。
2.  配置新的記憶體或重新配置緩衝區大小（如果已經存在的話）。
3.  呼叫以代表無聲的值來填滿緩衝區的方法。

無回應的值會根據位深度而有所不同。 若為8位音訊，無回應會以十六進位值80表示;若是16位音訊，無回應會以零表示。

## <a name="calculating-the-delay-buffer-size"></a>計算延遲緩衝區大小

為了計算延遲緩衝區所需的大小，您必須先取出包含音訊資料相關資訊的 **WAVEFORMATEX** 結構。 The following example retrieves a pointer to this structure from the input **DMO\_MEDIA\_TYPE** structure:


```
// Get a pointer to the WAVEFORMATEX structure.
WAVEFORMATEX *pWave = ( WAVEFORMATEX * ) m_mtInput.pbFormat;
if (NULL == pWave)
{
    return E_FAIL;
}
```



一旦將指標儲存至適當的 **WAVEFORMATEX** 結構之後，您就可以檢查其成員並使用它們來計算所需的緩衝區大小。 下列程式碼範例將示範此範例：


```
// Get the size of the buffer required.
m_cbDelayBuffer = (m_dwDelayTime * pWave->nSamplesPerSec * pWave->nBlockAlign) / 1000;
```



此演算法會藉由將延遲時間（以毫秒為單位）乘以每毫秒樣本數來計算緩衝區大小，然後將結果乘以通道數目，然後將結果乘以每個樣本的位元組數目。 通道數目和每個樣本的位元組數目並不明顯;它們是在 nBlockAlign 成員中進行編碼。 除以1000可將 nSamplesPerSec 值縮減為每毫秒樣本數;毫秒是所需的單位，因為延遲時間以毫碼錶示。

## <a name="allocating-the-delay-buffer-memory"></a>配置延遲緩衝區記憶體

當您計算出記憶體需求之後，就可以配置緩衝區。 緩衝區可能需要刪除（如果存在的話），例如當使用者叫用屬性頁來變更延遲時間值時。 下列程式碼示範如何配置延遲緩衝區：


```
// Test whether a buffer exists.
if (m_pbDelayBuffer)
{
    // A buffer already exists.
    // Delete the delay buffer.
    delete m_pbDelayBuffer;
    m_pbDelayBuffer = NULL;
}

// Allocate the buffer.
m_pbDelayBuffer = new BYTE[m_cbDelayBuffer];

if (!m_pbDelayBuffer)
    return E_OUTOFMEMORY;
```



如果緩衝區已成功配置，您應該將可移動指標移至緩衝區的標頭，如下列範例所示：


```
// Move the echo pointer to the head of the delay buffer.
m_pbDelayPointer = m_pbDelayBuffer;
```



## <a name="filling-the-delay-buffer-with-silence"></a>使用無聲填滿延遲緩衝區

撰寫一個方法來填滿延遲緩衝區，並以代表無聲的值來填滿延遲緩衝區是很方便的。 方法應該接收有效 WAVEFORMATEX 結構的指標，然後檢查 wBitsPerSample 成員以判斷音訊是否為8位或更高。 下列範例會以正確的無聲值填入延遲緩衝區：


```
void CEcho::FillBufferWithSilence(WAVEFORMATEX *pWfex)
{
    if (8 == pWfex->wBitsPerSample)
    {
    ::FillMemory(m_pbDelayBuffer, m_cbDelayBuffer, 0x80);
    }
    else
    ::ZeroMemory(m_pbDelayBuffer, m_cbDelayBuffer);
}
```



請記得將函式的向前宣告新增至私用區段中的標頭檔 Echo：


```
void FillBufferWithSilence(WAVEFORMATEX *pWfex);
```



您應該在 AllocateStreamingResources 結尾加入程式碼，以便在每次建立或調整延遲緩衝區時呼叫這個方法。 下列範例程式碼會將名為 pWave 的 WAVEFORMATEX 指標傳遞給新的方法：


```
// Fill the buffer with values representing silence.
FillBufferWithSilence(pWave);
```



## <a name="reallocating-the-delay-buffer-memory"></a>重新配置延遲緩衝區記憶體

當使用者使用 [屬性] 頁面變更延遲時間時，延遲緩衝區的大小也必須變更。 您已將程式碼新增至 AllocateStreamingResources 以調整緩衝區大小，但您需要將程式程式碼加入至 CEcho：:p \_ 每次屬性值變更時，呼叫資源配置方法。 程式碼如下：


```
// Reallocate the delay buffer.
AllocateStreamingResources();
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用串流資源**](working-with-streaming-resources.md)
</dt> </dl>

 

 





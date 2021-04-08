---
title: 建立 Echo 效果
description: 建立 Echo 效果
ms.assetid: 3fac6c74-8221-4656-997b-0f903fae85b7
keywords:
- Windows Media Player 外掛程式，Echo 範例 DoProcessOutput 方法
- 外掛程式，Echo 範例 DoProcessOutput 方法
- 數位信號處理外掛程式，Echo 範例 DoProcessOutput 方法
- DSP 外掛程式，Echo 範例 DoProcessOutput 方法
- Echo DSP 外掛程式範例，DoProcessOutput 方法
- Echo DSP 外掛程式範例，建立 echo 效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e978562ff4cdee016f92409d183990cd4bb178b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020886"
---
# <a name="creating-the-echo-effect"></a>建立 Echo 效果

您必須先從可調整音訊的 wizard 範例中移除程式碼。 從8位區段中，移除下列程式碼：


```C++
// Apply scale factor to sample.
i = int( ((double) i) * m_dwDelayTime );

```



 (記得 m \_ fScaleFactor 已被 m dwDelayTime 取代 \_ 。 ) 

從16位區段中，移除下列程式碼：


```C++
// Apply scale factor to sample.
i = int( ((double) i) * m_dwDelayTime );

```



外掛程式 wizard 範例程式碼所提供的 **DoProcessOutput** 執行會建立 while 迴圈，以針對 Windows Media Player 所提供之輸入緩衝區中的每個樣本逐一查看一次。 此迴圈的運作方式與8位和16位音訊相同，不過每個迴圈都需要個別的迴圈。 在每個案例中，迴圈都會以下列測試起始：


```C++
while (dwSamplesToProcess--)

```



在迴圈內，處理常式在8位和16位音訊方面都非常類似。 主要差異在於8位區段中的程式碼會將資料值的範圍變更為-128 到127，然後在將資料寫入輸出緩衝區之前再次將範圍轉換回來。 在處理期間保留音訊波形的對稱是很重要的。

現在您可以開始新增和取代處理迴圈中的程式碼。

## <a name="retrieve-a-sample-from-the-input-buffer"></a>從輸入緩衝區取出範例

在迴圈的每個反復專案期間，會從輸入緩衝區取出單一樣本。 若為8位音訊，此範例會移至新的範圍，然後輸入緩衝區的指標會前進到下一個範例。 下列程式碼來自于外掛程式 wizard：


```C++
// Get the input sample and normalize to -128 .. 127
int i = (*pbInputData++) - 128;

```



若是16位音訊，除了正規化以外，程式也相同：


```C++
// Get the input sample.
int i = *pwInputData++;

```



請記住，16位程式碼中的指標已轉換成 **short** 類型。

## <a name="retrieve-a-sample-from-the-delay-buffer"></a>從延遲緩衝區取出範例

接下來，從延遲緩衝區取出單一範例。 若為8位程式碼，延遲樣本會儲存在其原生範圍0到255。 您必須加入的下列程式碼會捕獲8位延遲範例：


```C++
// Get the delay sample and normalize to -128 .. 127
int delay = m_pbDelayPointer[0] - 128;

```



若是16位音訊，此程式很類似：


```C++
// Get the delay sample.
int delay = *pwDelayPointer;

```



## <a name="write-the-input-sample-to-the-delay-buffer"></a>將輸入範例寫入延遲緩衝區

現在，您必須將輸入範例儲存在延遲緩衝區中您抓取延遲樣本的相同位置。 以下是您必須為8位音訊新增的程式碼：


```C++
// Write the input sample into the delay buffer.
m_pbDelayPointer[0] = i + 128;

```



這是要為16位區段新增的程式碼：


```C++
// Write the input sample to the delay buffer.
*pwDelayPointer = i;

```



## <a name="move-the-delay-buffer-pointer"></a>移動延遲緩衝區指標

現在，延遲緩衝區中的工作已完成此反復專案，您可以將可移動指標前進至延遲緩衝區。 如果指標到達迴圈緩衝區的結尾，您必須變更其值以指向緩衝區的標頭。 若要為8位音訊執行這項操作，請使用下列程式碼：


```C++
// Increment the delay pointer.
// If it has passed the end of the buffer,
// then move it to the head of the buffer.
if (++m_pbDelayPointer > pbEOFDelayBuffer)
    m_pbDelayPointer = m_pbDelayBuffer;

```



以下是16位區段的程式碼：


```C++
// Increment the local delay pointer.
// If it is past the end of the buffer,
// then move it to the head of the buffer.
if (++pwDelayPointer > pwEOFDelayBuffer)
    pwDelayPointer = pwDelayBuffer;

```



由於16位區段中的指標其實是成員變數的複本，因此您必須記得使用新的位址來更新成員變數中的值。 如果您無法這麼做，延遲緩衝區指標會重複指向緩衝區的標頭，而且您的 echo 效果將無法如預期般運作。 將下列程式碼新增至16位區段：


```C++
// Move the global delay pointer.
m_pbDelayPointer = (BYTE *) pwDelayPointer;

```



## <a name="mix-the-input-sample-with-the-delay-sample"></a>使用 Delay 範例混合輸入範例

這是您使用濕混合和幹混合值的位置，以建立最終的輸出範例。 您只需將每個範例乘以表示樣本最後信號百分比的浮點值。 將輸入範例乘以儲存在 m fDryMix 中的值， \_ 然後將延遲樣本乘以 m fWetMix 中儲存的值 \_ 。 然後，新增兩個值。 您必須新增的程式碼在8位和16位區段中都是相同的：


```C++
// Mix the delay with the dry signal.
i = (int)((i * m_fDryMix ) + (delay * m_fWetMix));   

```



## <a name="write-the-data-to-the-output-buffer"></a>將資料寫入輸出緩衝區

最後，將混合範例複製到輸出緩衝區，然後前進輸出緩衝區指標。 若為8位音訊，外掛程式 wizard 會使用下列程式碼，將範例傳回至其原始範圍：


```C++
// Convert back to 0..255 and write to output buffer.
*pbOutputData++ = (BYTE)(i + 128);

```



若是16位音訊，嚮導會使用下列程式碼做為處理迴圈中的最後一個步驟：


```C++
// Write to output buffer.
*pwOutputData++ = i;

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**執行 CEcho：:D oProcessOutput**](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 





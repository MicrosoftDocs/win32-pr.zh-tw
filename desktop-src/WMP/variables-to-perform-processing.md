---
title: 要執行處理的變數
description: 要執行處理的變數
ms.assetid: 02f194ea-cac0-410f-886f-2894dd6971c8
keywords:
- Windows Media Player 外掛程式，Echo 範例 DoProcessOutput 方法
- 外掛程式，Echo 範例 DoProcessOutput 方法
- 數位信號處理外掛程式，Echo 範例 DoProcessOutput 方法
- DSP 外掛程式，Echo 範例 DoProcessOutput 方法
- Echo DSP 外掛程式範例，DoProcessOutput 方法
- Echo DSP 外掛程式範例，處理變數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e44f044aee6d893fba97cf921360444ec43db871
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673604"
---
# <a name="variables-to-perform-processing"></a>要執行處理的變數

用來處理延遲緩衝區的成員變數會處理 **位元組** 數量;它們是 **位元組** 指標，以及用來儲存位元組計數的整數。 這很適合用來處理8位的音訊，因為8位範例可妥善容納一個位元組的記憶體。 不過，在處理16位音訊時，將它們轉換成 **簡短** 指標會比較方便，因此處理可以一次出現兩個位元組。

下列程式碼範例會配置新的16位指標，並新增指標變數來儲存延遲緩衝區結尾的位址。 將它插入至迴圈進入點之前的「案例16」區段：


```C++
// Store local pointers to the delay buffer.
short    *pwDelayPointer = (short *)m_pbDelayPointer;
short    *pwDelayBuffer = (short *) m_pbDelayBuffer;
// Store the address of the last word of the delay buffer.
short    *pwEOFDelayBuffer = (short *)(m_pbDelayBuffer + m_cbDelayBuffer - sizeof(short)); 

```



8位處理常式的程式碼也會組態變數，以儲存延遲緩衝區結尾的位址。 儲存此值可讓您輕鬆地測試可移動的延遲緩衝區指標是否已到達延遲緩衝區的結尾。 下列範例程式碼會計算值：


```C++
// Store the address of the end of the delay buffer.
BYTE * pbEOFDelayBuffer = (m_pbDelayBuffer + m_cbDelayBuffer - sizeof(BYTE));

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**執行 CEcho：:D oProcessOutput**](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 





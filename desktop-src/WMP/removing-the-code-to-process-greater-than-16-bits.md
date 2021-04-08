---
title: 移除程式碼以處理大於16個位的程式碼
description: 移除程式碼以處理大於16個位的程式碼
ms.assetid: 90c165e1-bc77-42a5-878d-056762c62991
keywords:
- Windows Media Player 外掛程式，Echo 範例 DoProcessOutput 方法
- 外掛程式，Echo 範例 DoProcessOutput 方法
- 數位信號處理外掛程式，Echo 範例 DoProcessOutput 方法
- DSP 外掛程式，Echo 範例 DoProcessOutput 方法
- Echo DSP 外掛程式範例，DoProcessOutput 方法
- Echo DSP 外掛程式範例，處理大於16個位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec33332ee332d0ca7b615844ba8ad5cd7b00eb2f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840067"
---
# <a name="removing-the-code-to-process-greater-than-16-bits"></a>移除程式碼以處理大於16個位的程式碼

因為此範例只會處理8位或16位的音訊，所以您必須修改 **CEcho：： ValidateMediaType** 中的程式碼，以 \_ 傳回 \_ \_ \_ 大於16位之媒體類型不接受的 sql-dmo E 類型。 若要完成這項工作，您必須變更 switch 區塊中的程式碼，以測試可延伸的型別 WAVE 格式的格式 \_ \_ 。 將嚮導程式碼取代為下列範例程式碼：


```C++
case WAVE_FORMAT_EXTENSIBLE:
    {
         // Sample size is greater than 16-bit or is multichannel.
        WAVEFORMATEXTENSIBLE *pWaveXT = (WAVEFORMATEXTENSIBLE *) pWave;

        if (KSDATAFORMAT_SUBTYPE_PCM != pWaveXT->SubFormat)
        {
            return DMO_E_TYPE_NOT_ACCEPTED;
        }
    }
    break;

```



接下來，刪除或批註 **DoProcessOutput** 中處理高位解析度音訊的程式碼區段。 這些是以案例24和案例32為開頭的區段。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**執行 CEcho：:D oProcessOutput**](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 





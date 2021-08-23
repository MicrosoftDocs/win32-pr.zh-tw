---
title: 使用 PlaySound 來播放 Waveform-Audio 檔案
description: 使用 PlaySound 來播放 Waveform-Audio 檔案
ms.assetid: 8b7d191b-6b0c-4dff-84de-cb3a5c314b80
keywords:
- 波形音訊，PlaySound 函式
- 波形音訊，播放檔案
- 波形音訊、WAV 副檔名
- PlaySound 函式，播放波形-音訊檔案
- 播放波形-音訊檔案，PlaySound 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa83125665e2a99cc0f47da0893cbc113c0be7a251d62eb66a91e7a1218dac5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687848"
---
# <a name="using-playsound-to-play-waveform-audio-files"></a>使用 PlaySound 來播放 Waveform-Audio 檔案

大部分的波形音訊檔案都使用。WAV 副檔名。

下列語句會播放 C：音效 \\ \\ 功能對。WAV 檔：


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_SYNC); 
```



如果指定的檔案不存在，或檔案無法放入可用的記憶體中， [**PlaySound**](/previous-versions//dd743680(v=vs.85)) 會播放預設的系統音效。 如果未定義任何預設系統音效， **PlaySound** 會失敗，而不會產生任何音效。 如果您不想讓預設系統音效播放，請指定 OPERATORS.SND \_ NODEFAULT 旗標，如下列範例所示：


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_SYNC | SND_NODEFAULT); 
```



 

 
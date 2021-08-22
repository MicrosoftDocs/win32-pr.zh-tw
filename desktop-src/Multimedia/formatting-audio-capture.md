---
title: 格式化音訊捕獲
description: 格式化音訊捕獲
ms.assetid: 3bbe34a6-8fd6-4780-b5af-fcf3d34ef701
keywords:
- capSetAudioFormat 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36acf1f98bcb6ea5d6786264406c28da78e909e3e57c5d796eac080139229f77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119496378"
---
# <a name="formatting-audio-capture"></a>格式化音訊捕獲

下列範例會使用 [**capSetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) 將音訊格式設定為 11-kHz PCM 8 位、身歷聲。


```C++
WAVEFORMATEX wfex;

wfex.wFormatTag = WAVE_FORMAT_PCM;
wfex.nChannels = 2;                // Use stereo
wfex.nSamplesPerSec = 11025;
wfex.nAvgBytesPerSec = 22050;
wfex.nBlockAlign = 2;
wfex.wBitsPerSample = 8;
wfex.cbSize = 0;

capSetAudioFormat(hWndC, &wfex, sizeof(WAVEFORMATEX)); 
 
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用影片捕獲](using-video-capture.md)
</dt> </dl>

 

 





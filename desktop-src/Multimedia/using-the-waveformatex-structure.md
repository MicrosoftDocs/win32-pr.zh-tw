---
title: 使用 WAVEFORMATEX 結構
description: 使用 WAVEFORMATEX 結構
ms.assetid: 9b668e1e-cb5f-4065-802b-23974925eacf
keywords:
- 波形音訊、WAVEFORMATEX 結構
- 輔助音訊，WAVEFORMATEX 結構
- WAVEFORMATEX 結構
- PCM 音訊資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1534cf660c2f2423dc526c3d29f8eca06878fc0c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463029"
---
# <a name="using-the-waveformatex-structure"></a>使用 WAVEFORMATEX 結構

針對不超過兩個通道的 PCM 音訊資料，以及8位或16位的範例，請使用 [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) 結構來指定資料格式。

下列範例顯示如何設定11.025 千赫茲 (kHz) 8 位 mono 和 44.1 kHz 16 位身歷聲的 **WAVEFORMATEX** 結構。 設定 **WAVEFORMATEX** 之後，此範例會呼叫 IsFormatSupported 函式，以確認 PCM 波形輸出裝置支援此格式。 IsFormatSupported 的原始程式碼顯示在 [判斷非標準格式支援](determining-nonstandard-format-support.md)的範例中。


```C++
UINT wReturn; 
WAVEFORMATEX pcmWaveFormat; 
 
// Set up WAVEFORMATEX for 11 kHz 8-bit mono. 
 
pcmWaveFormat.wFormatTag = WAVE_FORMAT_PCM; 
pcmWaveFormat.nChannels = 1; 
pcmWaveFormat.nSamplesPerSec = 11025L; 
pcmWaveFormat.nAvgBytesPerSec = 11025L; 
pcmWaveFormat.nBlockAlign = 1; 
pcmWaveFormat.wBitsPerSample = 8; 
pcmWaveFormat.cbSize = 0;
 
// See if format is supported by any device in system. 
 
wReturn = IsFormatSupported(&pcmWaveFormat, WAVE_MAPPER); 
 
// Report results. 
 
if (wReturn == 0) 
     MessageBox(hMainWnd, "11 kHz 8-bit mono is supported.", 
       "", MB_ICONINFORMATION); 
else if (wReturn == WAVERR_BADFORMAT) 
     MessageBox(hMainWnd, "11 kHz 8-bit mono NOT supported.", 
       "", MB_ICONINFORMATION); 
else 
     MessageBox(hMainWnd, "Error opening waveform device.", 
       "Error", MB_ICONEXCLAMATION); 
 
// Set up WAVEFORMATEX for 44.1 kHz 16-bit stereo. 
 
pcmWaveFormat.wFormatTag = WAVE_FORMAT_PCM; 
pcmWaveFormat.nChannels = 2; 
pcmWaveFormat.nSamplesPerSec = 44100L; 
pcmWaveFormat.nAvgBytesPerSec = 176400L; 
pcmWaveFormat.nBlockAlign = 4; 
pcmWaveFormat.wBitsPerSample = 16; 
pcmWaveFormat.cbSize = 0;
 
// See if format is supported by any device in the system. 
 
wReturn = IsFormatSupported(&pcmWaveFormat, WAVE_MAPPER); 
 
// Report results. 
 
if (wReturn == 0) 
    MessageBox(hMainWnd, "44.1 kHz 16-bit stereo is supported.", 
      "", MB_ICONINFORMATION); 
else if (wReturn == WAVERR_BADFORMAT) 
    MessageBox(hMainWnd, "44.1 kHz 16-bit stereo NOT supported.", 
      "", MB_ICONINFORMATION); 
else 
    MessageBox(hMainWnd, "Error opening waveform device.", 
      "Error", MB_ICONEXCLAMATION); 

```



 

 
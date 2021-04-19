---
title: '迴圈播放 (波形音訊) '
description: '迴圈播放 (波形音訊) '
ms.assetid: 8411290b-a3c5-4347-bee3-43c35188f736
keywords:
- 波形音訊，迴圈聲音
- 波形-音訊介面，迴圈聲音
- 波形音訊、迴圈播放
- 波形-音訊介面、迴圈播放
- 迴圈波形-音效
- 迴圈波形-音訊播放
- waveOutWrite 函式
- waveOutBreakLoop 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c233799e2d4faf8107b4a2a68a261b544ec1274
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/26/2021
ms.locfileid: "107000447"
---
# <a name="looping-playback"></a>迴圈播放

使用 [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite)函式傳遞至裝置的 [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)結構中的 **dwLoops** 和 **dwFlags** 成員，可控制音效的迴圈。 使用 **dwFlags** 成員中的 **WHDR \_ BEGINLOOP** 和 **WHDR \_ ENDLOOP** 旗標，指定迴圈的開始和結束資料區塊。

若要迴圈單一資料區塊，請指定相同區塊的兩個旗標。 若要指定迴圈的數目，請針對迴圈中的第一個區塊使用 [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)結構中的 **dwLoops** 成員。

您可以呼叫 [**waveOutBreakLoop**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop) 函數來停止迴圈音效。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[播放 Waveform-Audio 檔案](playing-waveform-audio-files.md)
</dt> </dl>

 

 

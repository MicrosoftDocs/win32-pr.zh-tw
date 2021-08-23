---
title: 停止、暫停及重新開機播放
description: 停止、暫停及重新開機播放
ms.assetid: 39751342-63bc-4e68-bf9e-38665db8a05c
keywords:
- 波形音訊，停止播放
- 波形-音訊介面，停止播放
- 播放波形-音訊檔案，停止播放
- 波形音訊，暫停播放
- 波形-音訊介面，暫停播放
- 播放波形-音訊檔案，暫停播放
- 波形音訊，重新開機播放
- 波形-音訊介面，重新開機播放
- 播放波形-音訊檔案，重新開機播放
- waveOutPause 函式
- waveOutReset 函式
- waveOutRestart 函式
- 停止波形-音訊播放
- 暫停波形-音訊播放
- 重新開機波形-音訊播放
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b04491a676a104e288d274da7dd70eb759e363adc6476805b261a9651444bf1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688488"
---
# <a name="stopping-pausing-and-restarting-playback"></a>停止、暫停及重新開機播放

您可以在波形音訊播放時停止或暫停播放。 暫停播放之後，您可以重新開機。 Windows 提供下列功能來控制波形音訊播放。



| 函式                                 | 描述                                                                                 |
|------------------------------------------|---------------------------------------------------------------------------------------------|
| [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause)     | 暫停波形音訊輸出裝置上的播放。                                          |
| [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)     | 停止在波形音訊輸出裝置上播放，並將所有暫止的資料區塊標示為已完成。 |
| [**waveOutRestart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart) | 繼續在暫停的波形音訊輸出裝置上播放。                                  |



 

使用 [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause) 暫停波形音訊裝置可能不會立即進行;驅動程式可能會在暫停播放之前完成播放目前的區塊。

一般來說，只要使用 [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) 函式來傳送第一個波形-音訊資料區塊，就會開始播放波形音訊裝置。 如果您不想讓音效立即開始播放，請先呼叫 **waveOutPause** 再呼叫 **waveOutWrite**。 然後，當您想要開始播放波形音訊資料時，請呼叫 [**waveOutRestart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart)。

您無法使用 **waveOutRestart** 重新開機已使用 [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)停止的裝置;您必須使用 **waveOutWrite** 來傳送第一個資料區塊，以繼續在裝置上播放。

 

 
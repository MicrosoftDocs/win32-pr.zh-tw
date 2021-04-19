---
title: 使用回呼函式來處理驅動程式訊息
description: 使用回呼函式來處理驅動程式訊息
ms.assetid: 7fef400f-5040-4d33-9a2f-bb12aa9369e0
keywords:
- 波形音訊，回呼函數
- 音訊資料區塊，回呼函數
- 波形音訊，處理驅動程式訊息
- 音訊資料區塊，處理驅動程式訊息
- 處理驅動程式訊息
- waveInOpen 函式
- waveOutOpen 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3e7541a00b43b5fb2267a17d4de8bb017823c3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106969704"
---
# <a name="using-a-callback-function-to-process-driver-messages"></a>使用回呼函式來處理驅動程式訊息

您可以撰寫自己的回呼函式來處理設備磁碟機所傳送的訊息。 若要使用回呼函式，請在 \_ *fdwOpen* 參數中指定回呼函數旗標，並在 [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen)或 [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen)函數的 *dwCallback* 參數中指定回呼的位址。

傳送至回呼函式的訊息類似于傳送至視窗的訊息，但它們有兩個 **DWORD** 參數，而不是 **UINT** 和 **DWORD** 參數。 如需這些訊息的詳細資訊，請參閱 [播放 Waveform-Audio](playing-waveform-audio-files.md)的檔案。

若要將實例資料從應用程式傳遞給回呼函式，請使用下列其中一種技術：

-   使用開啟設備磁碟機的函式的 *dwInstance* 參數傳遞實例資料。
-   使用 [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)結構的 **dwUser** 成員（識別要傳送到設備磁碟機的音訊資料區塊）來傳遞實例資料。

如果您需要超過32個位的實例資料，請將指標傳遞至包含其他資訊的結構。

 

 
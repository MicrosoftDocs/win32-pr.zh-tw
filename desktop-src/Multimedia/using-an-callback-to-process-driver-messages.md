---
title: 使用事件回呼處理驅動程式訊息
description: 使用事件回呼處理驅動程式訊息
ms.assetid: 5b17ff93-ed00-46ee-828c-baf716c9257c
keywords:
- 波形音訊、事件回呼
- 音訊資料區塊，事件回呼
- 波形音訊，處理驅動程式訊息
- 音訊資料區塊，處理驅動程式訊息
- 處理驅動程式訊息
- CreateEvent 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cbfeb95fcf0e5d83f9a54fc0cf3cd223ac6ce19
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681886"
---
# <a name="using-an-event-callback-to-process-driver-messages"></a>使用事件回呼處理驅動程式訊息

若要使用事件回呼，請使用 [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) 函數建立手動重設事件。 在 [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen)函數的呼叫中，指定 *FdwOpen* 參數的 **回呼 \_ 事件**。 在您呼叫 [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader) 函式，但在將波形音訊資料傳送至裝置之前，請呼叫 [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent) 函式，將事件放入未收到信號狀態。 然後，在檢查 **WHDR \_ DONE** 旗標是否在 [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)結構的 **dwFlags** 成員中設定的迴圈內，呼叫 [WaitForSingleObject](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)函數，並將事件處理常式和超時值指定為參數。

由於事件回呼不會收到特定的關閉、完成或開啟的通知，因此應用程式可能必須檢查它在事件發生之後所等待的進程狀態。 [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)傳回的時間可能已完成許多工具。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊資料區塊](audio-data-blocks.md)
</dt> </dl>

 

 
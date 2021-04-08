---
title: 計時器解析度
description: 計時器解析度
ms.assetid: 2e5e94fe-8175-417f-8c59-9d5cf052ea89
keywords:
- 多媒體計時器，解析度
- 計時器，解決
- 最小計時器解析度
- 最大計時器解析度
- 多媒體計時器，最大解析度
- 計時器，最大解析度
- 多媒體計時器，最低解析度
- 計時器，最低解析度
- timeGetDevCaps 函式
- timeBeginPeriod 函式
- timeEndPeriod 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e96f1b410f2e18203af794ea124bb6b83bccce
ms.sourcegitcommit: a0b531d335bc691100149830b256d5af7e136c24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/28/2019
ms.locfileid: "103670860"
---
# <a name="timer-resolution"></a>計時器解析度

若要判斷計時器服務所支援的最小和最大計時器解析度，請使用 [**timeGetDevCaps**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetdevcaps) 函數。 此函式會以最小和最大解析度填滿 [**TIMECAPS**](/windows/desktop/api/TimeAPI/ns-timeapi-timecaps)結構的 **wPeriodMin** 和 **wPeriodMax** 成員。 此範圍在電腦和 Windows 平臺上可能會有所不同。

判斷可用計時器解析度的最小和最大值之後，您必須建立應用程式所要使用的最小解析度。 您可以使用 [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) 和 [**timeEndPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod) 函數來設定和清除此解決方法。 您必須使用 **timeEndPeriod** 的呼叫來比對 **timeBeginPeriod** 的每個呼叫，並在兩個呼叫中指定相同的最小解析度。 只要每個呼叫都與 **timeEndPeriod** 的呼叫相符，應用程式就可以進行多個 **timeBeginPeriod** 呼叫。

在 [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) 和 [**TimeEndPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod)中， *uPeriod* 參數表示最小計時器解析度（以毫秒為單位）。 您可以在計時器所支援的範圍內指定任何計時器解析度值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於多媒體計時器](about-multimedia-timers.md)
</dt> </dl>

 

 





---
description: 只要系統判斷有使用者或應用程式活動，它就不會進入睡眠狀態。
ms.assetid: 83c9394a-1813-405a-802a-0623e5de50d3
title: 系統睡眠準則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90950b980ec1e0fa06171d7a57d76b410534f96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103693019"
---
# <a name="system-sleep-criteria"></a>系統睡眠準則

只要系統判斷有使用者或應用程式活動，它就不會進入睡眠狀態。 系統可以偵測到某些活動，例如使用者輸入或網路通訊。 但是，系統無法偵測到其他活動。 例如，簡報應用程式需要畫面才能顯示。 不過，可能會顯示應用程式在簡報期間閒置，導致系統關閉顯示。

若要通知系統您的應用程式忙碌中，請使用 [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) 函數。 此函式可防止系統進入睡眠狀態，或在應用程式執行時關閉顯示。

簡報和多媒體應用程式必須以 **\_ \_ 所需的 ES 顯示** 呼叫 [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate)函式，這樣系統才能知道它不應該讓顯示器裝置進入睡眠狀態。 事件處理應用程式（例如用來管理傳入傳真的工具）必須以 **需要的 \_ ES \_ 系統** 呼叫 **SetThreadExecutionState** 、處理事件，然後清除旗標，讓系統可以回到睡眠狀態。 請注意，大部分的生產力應用程式都不需要使用 **SetThreadExecutionState** ，因為系統通常可以根據使用者輸入來決定活動。

為了維護最後一次使用者輸入的時間，系統會使用「顯示閒置計時器」和「系統閒置計時器」。 系統會將閒置計時器與電源計劃中所設定的值進行比較。 如果顯示閒置計時器值大於顯示超時值，而且沒有任何執行緒透過呼叫 [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) 和 **\_ \_ 所需的 ES 顯示** 來要求顯示，則系統會關閉顯示器的電源。 同樣地，如果系統閒置計時器大於系統超時值，而且沒有任何應用程式透過呼叫 **\_ \_ 需要 ES 系統** 的 **SetThreadExecutionState** 來要求系統，系統就會進入睡眠狀態。

系統會維護已呼叫 [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate)的應用程式計數。 系統會追蹤呼叫 **SetThreadExecutionState** 的每個執行緒，並據以調整計數器。 如果此計數器到達零，而且沒有任何使用者輸入，系統就會進入睡眠狀態。

如果電力不足，應用程式可以要求使用者介入，或要求系統暫停本身。 您可以使用 [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) 函數來暫停系統作業。

如果系統自動喚醒 ([PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md)) ，就不會有任何計時器相關。 如需詳細資訊，請參閱 [系統喚醒事件](system-wake-up-events.md)。

## <a name="entering-sleep"></a>進入睡眠狀態

當系統進入睡眠狀態時，會自動保留整個系統和所有應用程式的狀態。 因此，大部分的應用程式都不需要採取任何特殊動作。 需要在系統轉換之前執行特定動作的應用程式可以註冊電源事件。

當系統傳送 [PBT \_ APMSUSPEND](pbt-apmsuspend.md) 事件時，每個應用程式都有兩秒鐘的時間來執行任何必要的動作，然後系統才會開始轉換到睡眠狀態。 應用程式必須限制在回應此事件時所採取的動作，以確保它們會在分配的時間內完成所有作業。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於電源管理](about-power-management.md)
</dt> <dt>

[系統喚醒事件](system-wake-up-events.md)
</dt> </dl>

 

 




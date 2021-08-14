---
description: Wait 函數可讓執行緒封鎖本身的執行。
ms.assetid: 9c66c71d-fdfd-42ae-895c-2fc842b5bc7a
title: Wait 函式
ms.topic: article
ms.date: 06/25/2020
ms.openlocfilehash: 15bfc37dcd8fe541c14b9a0693c7b743cae6ed3e548c418baf0585f078e6d59a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764962"
---
# <a name="wait-functions"></a>Wait 函式

*Wait 函數* 可讓執行緒封鎖本身的執行。 直到符合指定的準則時，等候函式才會傳回。 Wait 函式的類型會決定所使用的準則集合。 呼叫 wait 函式時，它會檢查是否符合等候準則。 如果未符合準則，呼叫端執行緒會進入等候狀態，直到符合等候準則的條件或超過指定的逾時間隔為止。

-   [單一物件等候函式](#single-object-wait-functions)
-   [多物件等候函式](#multiple-object-wait-functions)
-   [可提供警示 Wait 函式](#alertable-wait-functions)
-   [已註冊的等候函式](#registered-wait-functions)
-   [等候位址](#waiting-on-an-address)
-   [等候函式和逾時間隔](#wait-functions-and-time-out-intervals)
-   [Wait 函數和同步處理物件](#wait-functions-and-synchronization-objects)
-   [Wait 函式和建立 Windows](#wait-functions-and-creating-windows)

## <a name="single-object-wait-functions"></a>單一物件等候函式

[**SignalObjectAndWait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait)、 [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)和 [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex)函數需要一個同步處理物件的控制碼。 當發生下列其中一種情況時，這些函數會傳回：

-   指定的物件處於已發出信號的狀態。
-   經過逾時間隔。 逾時間隔可以設定為 [ **無限** ]，以指定等待時間不會過期。

[**SignalObjectAndWait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait)函式可讓呼叫執行緒以不可部分完成的方式將物件的狀態設定為已發出信號，並等候另一個物件的狀態設定為已發出信號。

## <a name="multiple-object-wait-functions"></a>多物件等候函式

[**WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects)、 [**WaitForMultipleObjectsEx**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjectsex)、 [**MsgWaitForMultipleObjects**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjects)和 [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex)函數可讓呼叫執行緒指定包含一或多個同步處理物件控制碼的陣列。 當發生下列其中一種情況時，這些函數會傳回：

-   任何一個指定物件的狀態會設定為 [已發出信號]，或所有物件的狀態都已設定為 [已發出信號]。 您可以控制是否要在函式呼叫中使用一個或所有的狀態。
-   經過逾時間隔。 逾時間隔可以設定為 [ **無限** ]，以指定等待時間不會過期。

[**MsgWaitForMultipleObjects**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjects)和 [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex)函數可讓您指定物件控制碼陣列中的輸入事件物件。 當您線上程的輸入佇列中指定要等候的輸入類型時，就會執行這項操作。 例如，執行緒可以使用 **MsgWaitForMultipleObjects** 來封鎖其執行，直到指定物件的狀態已設定為 [已發出信號]，並且線上程的輸入佇列中有可用的滑鼠輸入為止。 執行緒可以使用 [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) 或 [**PeekMessageA**](/windows/win32/api/winuser/nf-winuser-peekmessagea) 或 [**PeekMessageW**](/windows/win32/api/winuser/nf-winuser-peekmessagew) 函數來取出輸入。

在等候所有物件的狀態設定為已發出信號時，這些多物件函式不會修改指定物件的狀態，直到所有物件的狀態都已設定為信號為止。 例如，mutex 物件的狀態可以是信號，但是呼叫的執行緒不會取得擁有權，直到陣列中所指定之其他物件的狀態也已設定為已發出信號為止。 在此同時，其他執行緒可能會取得 mutex 物件的擁有權，因此將其狀態設定為未收到信號。

在等候單一物件的狀態設定為已發出信號時，這些多物件函式會依序從索引0開始檢查陣列中的控制碼，直到其中一個物件有信號為止。 如果有多個物件變成信號，則函式會傳回陣列中物件的第一個控制碼的索引。

## <a name="alertable-wait-functions"></a>可提供警示 Wait 函式

[**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex)、 [**SignalObjectAndWait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait)、 [**WaitForMultipleObjectsEx**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjectsex)和 [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex)函數與其他等候函式不同，因為它們可以選擇性地執行 *可提供警示等候* 作業。 在可提供警示等候作業中，此函式會在符合指定的條件時傳回，但如果系統將 i/o 完成常式或 APC 排入佇列以供等候執行緒執行，則也會傳回此函式。 如需可提供警示等候作業和 i/o 完成常式的詳細資訊，請參閱 [同步處理和重迭的輸入和輸出](synchronization-and-overlapped-input-and-output.md)。 如需 Apc 的詳細資訊，請參閱 [非同步程序呼叫](asynchronous-procedure-calls.md)。

## <a name="registered-wait-functions"></a>已註冊的等候函式

[**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject)函式與其他等候函式不同，因為等候作業是由執行緒 [集](../procthread/thread-pooling.md)區中的執行緒執行。 當符合指定的條件時，回呼函式會由執行緒集區中的工作者執行緒執行。

依預設，已註冊的等候作業是一項多等待操作。 系統會在每次發出事件時將計時器重設 (或逾時間隔) 直到您呼叫 [**UnregisterWaitEx**](unregisterwaitex.md) 函式來取消作業為止。 若要指定只執行一次等待作業，請將 [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject)的 *dwFlags* 參數設定為 **wt. \_ EXECUTEONLYONCE**。

如果執行緒呼叫使用 Apc 的函數，請將 [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject)的 *dwFlags* 參數設定為 **wt. \_ EXECUTEINPERSISTENTTHREAD**。

## <a name="waiting-on-an-address"></a>等候位址

執行緒可以使用 [**WaitOnAddress**](/windows/desktop/api/SynchAPI/nf-synchapi-waitonaddress) 函式，等候目標位址的值從某些不想要的值變更為任何其他值。 這可讓執行緒等候值變更，而不需要微調或處理當執行緒捕捉到不想要的值，但線上程可以等候之前的值變更時可能會發生的同步處理問題。

修改目標值的程式碼會藉由呼叫 [**WakeByAddressSingle**](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddresssingle)喚醒單一等候執行緒或 [**WakeByAddressAll**](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddressall)來喚醒所有等候中的執行緒，以 [**WaitOnAddress**](/windows/desktop/api/SynchAPI/nf-synchapi-waitonaddress)傳回的變更。 如果使用 **WaitOnAddress** 指定逾時間隔，而且沒有任何執行緒呼叫喚醒函式，則函式會在逾時間隔過期時傳回。 如果未指定逾時間隔，執行緒就會無限期等候。

## <a name="wait-functions-and-time-out-intervals"></a>等候函式和逾時間隔

指定逾時間隔的精確度取決於系統時鐘的解析度。 以固定速率的系統時鐘「刻度」。 如果逾時間隔小於系統時鐘的解析度，等候時間可能會低於指定的時間長度。 如果逾時間隔大於一個刻度但小於二，則等候可以是介於一到兩個刻度之間的任何位置，依此類推。

若要增加等候函式的逾時間隔精確度，請呼叫 **timeGetDevCaps** 函式來判斷支援的最小計時器解析度，以及 **timeBeginPeriod** 函數將計時器解析度設定為最小值。 呼叫 **timeBeginPeriod** 時請特別小心，因為頻繁的呼叫可能會大幅影響系統時鐘、系統電源使用量和排程器。 如果您呼叫 **timeBeginPeriod**，請在應用程式初期呼叫它一次，並務必在應用程式的最一端呼叫 **timeEndPeriod** 函式。

## <a name="wait-functions-and-synchronization-objects"></a>Wait 函數和同步處理物件

等候函式可以修改某些類型的 [同步處理物件](synchronization-objects.md)的狀態。 只有當物件或物件的已發出信號狀態導致函式傳回時，才會進行修改。 Wait 函數可以修改同步處理物件的狀態，如下所示：

-   信號物件的計數會減少1，而且如果其計數為零，則會將信號的狀態設定為未收到信號。
-   Mutex、自動重設事件和變更通知物件的狀態會設定為未收到信號。
-   同步處理計時器的狀態設定為未收到信號。
-   手動重設事件、手動重設計時器、進程、執行緒和主控台輸入物件的狀態不會受到 wait 函式的影響。

## <a name="wait-functions-and-creating-windows"></a>Wait 函式和建立 Windows

當您使用直接或間接建立視窗的等候函式和程式碼時，必須特別小心。 如果執行緒建立任何視窗，則必須處理訊息。 系統會將訊息廣播傳送至系統中的所有視窗。 如果您有使用 wait 函式且沒有逾時間隔的執行緒，系統將會鎖死。 間接建立 windows 的兩個程式碼範例是 DDE 和 **CoInitialize** 函數。 因此，如果您有建立 windows 的執行緒，請使用 [**MsgWaitForMultipleObjects**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjects) 或 [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex)，而不是其他等候函式。

 

 

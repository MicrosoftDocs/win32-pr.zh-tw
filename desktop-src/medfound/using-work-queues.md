---
description: 本主題說明如何使用 Microsoft 媒體基礎中的工作佇列。
ms.assetid: 6be05df7-e8ff-4110-8f73-a62eb31fd414
title: 使用工作佇列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7bb41b830742ca871d44cadac9bd26a9967aa1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191747"
---
# <a name="using-work-queues"></a>使用工作佇列

本主題說明如何使用 Microsoft 媒體基礎中的工作佇列。

-   [使用工作佇列](#using-work-queues)
-   [關閉工作佇列](#shutting-down-work-queues)
-   [使用已排程的工作專案](#using-scheduled-work-items)
-   [使用定期回呼](#using-periodic-callbacks)
-   [相關主題](#related-topics)

## <a name="using-work-queues"></a>使用工作佇列

工作佇列是在另一個執行緒上執行非同步作業的有效方式。 在概念上，您會將工作專案放入佇列中，而佇列會有一個執行緒從佇列提取每個專案，然後將其分派。 使用 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 介面，將工作專案實作為回呼。

媒體基礎會建立數個標準工作佇列，稱為「 *平臺工作佇列*」。 應用程式也可以建立自己的工作佇列，稱為 *私用工作佇列*。 如需平臺工作佇列的清單，請參閱 [工作佇列識別碼](work-queue-identifiers.md)。 若要建立私用工作佇列，請呼叫 [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue)。 此函數會傳回新工作佇列的識別碼。 若要將專案放在佇列中，請呼叫 [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) 或 [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex)。 在這兩種情況下，您都必須指定回呼介面。

-   [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) 會使用 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 介面的指標，加上可實執行 **IUnknown** 的選擇性狀態物件。 這些是在非同步方法中使用的相同參數，如 [非同步回呼方法](asynchronous-callback-methods.md)主題中所述。 就內部而言，此函式會建立非同步結果物件，並將它傳遞給回呼的 [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) 方法。
-   [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) 會使用 [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) 介面的指標。 此介面代表非同步結果物件。 藉由呼叫 [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) ，並指定您的回呼介面和（選擇性）狀態物件來建立這個物件。

在這兩種情況下，工作佇列執行緒都會呼叫您的 [**IMFAsyncCallback：： Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) 方法。 使用 **Invoke** 方法來執行工作專案。

如果有多個執行緒或元件共用相同的工作佇列，您可以呼叫 [**MFLockWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mflockworkqueue) 來鎖定工作佇列，以防止平臺釋放它。 每次呼叫 [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue) 或 **MFLockWorkQueue** 時，您都必須呼叫 [**MFUnlockWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockworkqueue) 一次，才能釋放工作佇列。 例如，如果您建立新的工作佇列，然後將它鎖定一次，則必須呼叫 **MFUnlockWorkQueue** 兩次，一次呼叫 **MFAllocateWorkQueue** ，一次用於 **MFLockWorkQueue** 的呼叫。

下列程式碼示範如何建立新的工作佇列、將工作專案放入佇列中，以及釋放工作佇列。

如需 Windows 8 中工作佇列的詳細資訊，請參閱 [工作佇列和執行緒改善](media-foundation-work-queue-and-threading-improvements.md) 。


```C++
DWORD idWorkQueue = 0;
HRESULT hr = S_OK;

// Create a new work queue.
hr = MFAllocateWorkQueue(&idWorkQueue);

// Put an item on the queue.
if (SUCCEEDED(hr))
{
    hr = MFPutWorkItem(idWorkQueue, pCallback, NULL);
}

// Wait for the callback to be invoked.
if (SUCCEEDED(hr))
{
    WaitForSingleObject(hEvent, INFINITE);
}

// Release the work queue.
if (SUCCEEDED(hr))
{
    hr = MFUnlockWorkQueue(idWorkQueue);
}
```



此範例假設 *pCallback* 為應用程式的 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 介面指標。 它也會假設回呼會設定 *hEvent* 事件控制碼。 程式碼會在呼叫 [**MFUnlockWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockworkqueue)之前等候設定此事件。

工作佇列執行緒一律會在呼叫端的進程中建立。 在每個工作佇列中，會序列化回呼。 如果您使用相同的工作佇列呼叫 [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) 兩次，則不會叫用第二個回呼，直到第一個回呼傳回為止。

## <a name="shutting-down-work-queues"></a>關閉工作佇列

在呼叫 [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown)之前，請釋放工作佇列執行緒所使用的任何資源。 若要同步處理這個進程，您可以鎖定媒體基礎的平臺，這可防止 **MFShutdown** 函式關閉任何工作佇列執行緒。 如果在平臺鎖定時呼叫 **MFShutdown** ， **MFShutdown** 會等候數百毫秒讓平臺解除鎖定。 如果在該時間內未解除鎖定， **MFShutdown** 會關閉工作佇列執行緒。

[**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult)的預設執行會在建立結果物件時，自動鎖定媒體基礎平臺。 釋放介面會將平臺解除鎖定。 因此，您幾乎都不需要直接鎖定平臺。 但是，如果您撰寫自己的 **IMFAsyncResult** 自訂執行，就應該手動鎖定和解除鎖定平臺。 若要鎖定平臺，請呼叫 [**MFLockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mflockplatform)。 若要將平臺解除鎖定，請呼叫 [**MFUnlockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockplatform)。 如需範例，請參閱 [自訂非同步結果物件](custom-asynchronous-result-objects.md)。

在您呼叫 [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown)之後，您必須確保平臺會在5秒的超時期間內解除鎖定。 若要這樣做，請釋放所有 [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) 的指標，並呼叫 [**MFUnlockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockplatform) （如果您以手動方式鎖定平臺）。 請務必釋放工作佇列執行緒所使用的任何資源，否則您的應用程式可能會流失記憶體。

一般來說，如果您的應用程式在呼叫 [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown)之前關閉並釋出每個媒體基礎物件，就不必擔心鎖定。 鎖定機制只是在您呼叫 **MFShutdown** 之後，讓工作佇列執行緒正常結束。

## <a name="using-scheduled-work-items"></a>使用已排程的工作專案

您可以藉由呼叫 [**MFScheduleWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem) 或 [**MFScheduleWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex)，將回呼排程在一段時間後發生。

-   [**MFScheduleWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem) 會接受回呼的指標、選擇性的狀態物件，以及逾時間隔。
-   [**MFScheduleWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex) 會採用非同步結果物件的指標和超時值。

以毫秒為單位，將超時指定為負數值。 例如，若要排定在5秒鐘內叫用回呼，請使用值−5000。 這兩個函式都會傳回 **MFWORKITEM 索引 \_ 鍵值** ，您可以用來取消回呼，方法是將它傳遞至 [**MFCancelWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfcancelworkitem) 函數。

排程的工作專案一律使用 MFASYNC \_ 回呼 \_ 佇列 \_ 計時器平臺工作佇列。

## <a name="using-periodic-callbacks"></a>使用定期回呼

[**MFAddPeriodicCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfaddperiodiccallback)函式會排定要定期叫用的回呼，直到您取消為止。 回呼間隔是固定的;應用程式無法變更它。 若要找出確切的間隔，請呼叫 [**MFGetTimerPeriodicity**](/windows/desktop/api/mfapi/nf-mfapi-mfgettimerperiodicity)。 間隔是以10毫秒為單位，因此，此函式適用于您需要經常進行「滴答」的情況，例如執行簡報時鐘。 如果您想要將作業排程為較不頻繁地進行，請使用先前所述的排程工作專案。

不同于本主題中所述的其他回呼，定期回呼不會使用 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 介面。 相反地，它會使用函式指標。 如需詳細資訊，請參閱 [**MFPERIODICCALLBACK 回呼**](/windows/win32/api/mfapi/nc-mfapi-mfperiodiccallback)。

若要取消定期回呼，請呼叫 [**MFRemovePeriodicCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfremoveperiodiccallback)。

定期回呼會使用 MFASYNC \_ 回呼 \_ 佇列 \_ 計時器平臺工作佇列。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[工作佇列](work-queues.md)
</dt> <dt>

[**MFASYNCRESULT**](/windows/win32/api/mfapi/ns-mfapi-mfasyncresult)
</dt> <dt>

[工作佇列和執行緒改進](media-foundation-work-queue-and-threading-improvements.md)
</dt> </dl>

 

 

---
description: LSA 提供的函式可讓您在本機系統上的原則變更時，用來接收通知。
ms.assetid: 29c693f5-db2b-4fda-847c-4e5220eadfd3
title: 接收原則變更事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33145974ce712f21b338ba35f1571c8f3046c42c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970588"
---
# <a name="receiving-policy-change-events"></a><span data-ttu-id="346ad-103">接收原則變更事件</span><span class="sxs-lookup"><span data-stu-id="346ad-103">Receiving Policy Change Events</span></span>

<span data-ttu-id="346ad-104">LSA 提供的函式可讓您在本機系統上的原則變更時，用來接收通知。</span><span class="sxs-lookup"><span data-stu-id="346ad-104">The LSA provides functions you can use to receive notification when there is a change in policy on the local system.</span></span>

<span data-ttu-id="346ad-105">若要接收通知，請呼叫 [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) 函數來建立新的事件物件，然後呼叫 [**LsaRegisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaregisterpolicychangenotification) 函式。</span><span class="sxs-lookup"><span data-stu-id="346ad-105">To receive notification, create a new event object by calling the [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) function, and then call the [**LsaRegisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaregisterpolicychangenotification) function.</span></span> <span data-ttu-id="346ad-106">然後，您的應用程式可以呼叫等候函式（例如 [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)、 [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)或 [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) ）來等候事件發生。</span><span class="sxs-lookup"><span data-stu-id="346ad-106">Your application can then call a wait function such as [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex), or [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) to wait for the event to occur.</span></span> <span data-ttu-id="346ad-107">當事件發生時，或當超時時間過期時，wait 函式會傳回。</span><span class="sxs-lookup"><span data-stu-id="346ad-107">The wait function returns when the event occurs, or when the time-out period expires.</span></span> <span data-ttu-id="346ad-108">一般情況下，通知事件會用於多執行緒應用程式中，其中一個執行緒會等待事件，而其他執行緒則繼續處理。</span><span class="sxs-lookup"><span data-stu-id="346ad-108">Typically, notification events are used in multithreaded applications, in which one thread waits for an event, while other threads continue processing.</span></span>

<span data-ttu-id="346ad-109">當您的應用程式不再需要接收通知時，它應該呼叫 [**LsaUnregisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaunregisterpolicychangenotification) ，然後呼叫 [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) 來釋放事件物件控制碼。</span><span class="sxs-lookup"><span data-stu-id="346ad-109">When your application no longer needs to receive notifications, it should call [**LsaUnregisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaunregisterpolicychangenotification) and then call [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) to free the event object handle.</span></span>

<span data-ttu-id="346ad-110">下列範例顯示當系統的稽核原則變更時，單一執行緒應用程式可以接收通知事件的方式。</span><span class="sxs-lookup"><span data-stu-id="346ad-110">The following example shows how a single-threaded application can receive notification events when the system's auditing policy changes.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

void WaitForPolicyChanges()
{
  HANDLE hEvent;
  NTSTATUS ntsResult;
  DWORD dwResult;

  // Create an event object.
  hEvent = CreateEvent( 
    NULL,  // child processes cannot inherit 
    FALSE, // automatically reset event
    FALSE, // start as a nonsignaled event
    NULL   // do not need a name
  );

  // Check that the event was created.
  if (hEvent == NULL) 
  {
    wprintf(L"Event object creation failed: %d\n",GetLastError());
    return;
  }
  // Register to receive auditing policy change notifications.
  ntsResult = LsaRegisterPolicyChangeNotification(
    PolicyNotifyAuditEventsInformation,
    hEvent
  );
  if (STATUS_SUCCESS != ntsResult)
  {
    wprintf(L"LsaRegisterPolicyChangeNotification failed.\n");
    CloseHandle(hEvent);
    return;
  }

  // Wait for the event to be triggered.
  dwResult = WaitForSingleObject( 
    hEvent, // handle to the event object
    300000  // time-out interval, in milliseconds
  );

  // The wait function returned.
  if (dwResult == WAIT_OBJECT_0)
  {  // received the notification signal
    wprintf(L"Notification received.\n");
  } 
  else 
  {  // received a time-out or error
    wprintf(L"Notification was not received.\n");
  }
  // Unregister for notification.
  LsaUnregisterPolicyChangeNotification(
    PolicyNotifyAuditEventsInformation,
    hEvent
  );

  // Free the event handle.
  CloseHandle(hEvent);
}
```



<span data-ttu-id="346ad-111">如需事件物件、等候函式和同步處理的詳細資訊，請參閱 [使用事件物件](/windows/desktop/Sync/using-event-objects)。</span><span class="sxs-lookup"><span data-stu-id="346ad-111">For more information about event objects, wait functions, and synchronization, see [Using Event Objects](/windows/desktop/Sync/using-event-objects).</span></span>

 

 

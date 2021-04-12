---
description: 下列範例示範一次性初始化函式的使用。
ms.assetid: 47e68fbb-29f8-4930-beba-01d44263eb1e
title: 使用 One-Time 初始化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f89cbe0e2d3e7c45d4f18863533c8c161037ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513840"
---
# <a name="using-one-time-initialization"></a><span data-ttu-id="22852-103">使用 One-Time 初始化</span><span class="sxs-lookup"><span data-stu-id="22852-103">Using One-Time Initialization</span></span>

<span data-ttu-id="22852-104">下列範例示範一次性初始化函式的使用。</span><span class="sxs-lookup"><span data-stu-id="22852-104">The following examples demonstrate the use of the one-time initialization functions.</span></span>

## <a name="synchronous-example"></a><span data-ttu-id="22852-105">同步範例</span><span class="sxs-lookup"><span data-stu-id="22852-105">Synchronous Example</span></span>

<span data-ttu-id="22852-106">在此範例中， `g_InitOnce` 全域變數是一次性的初始化結構。</span><span class="sxs-lookup"><span data-stu-id="22852-106">In this example, the `g_InitOnce` global variable is the one-time initialization structure.</span></span> <span data-ttu-id="22852-107">它會使用 INIT 來 **靜態 \_ 初始化 \_ \_**。</span><span class="sxs-lookup"><span data-stu-id="22852-107">It is initialized statically using **INIT\_ONCE\_STATIC\_INIT**.</span></span>

<span data-ttu-id="22852-108">`OpenEventHandleSync`函數會將控制碼傳回給只建立一次的事件。</span><span class="sxs-lookup"><span data-stu-id="22852-108">The `OpenEventHandleSync` function returns a handle to an event that is created only once.</span></span> <span data-ttu-id="22852-109">它會呼叫 [**InitOnceExecuteOnce**](/windows/win32/api/synchapi/nf-synchapi-initonceexecuteonce) 函數，以執行回呼函式中所包含的初始化程式碼 `InitHandleFunction` 。</span><span class="sxs-lookup"><span data-stu-id="22852-109">It calls the [**InitOnceExecuteOnce**](/windows/win32/api/synchapi/nf-synchapi-initonceexecuteonce) function to execute the initialization code contained in the `InitHandleFunction` callback function.</span></span> <span data-ttu-id="22852-110">如果回呼函式成功，則 `OpenEventHandleSync` 傳回 *lpCoNtext* 中傳回的事件控制碼; 否則，它會傳回 **不正確 \_ 控制碼 \_ 值**。</span><span class="sxs-lookup"><span data-stu-id="22852-110">If the callback function succeeds, `OpenEventHandleSync` returns the event handle returned in *lpContext*; otherwise, it returns **INVALID\_HANDLE\_VALUE**.</span></span>

<span data-ttu-id="22852-111">`InitHandleFunction`函數是單次[初始化回呼函數](/windows/win32/api/synchapi/nc-synchapi-pinit_once_fn)。</span><span class="sxs-lookup"><span data-stu-id="22852-111">The `InitHandleFunction` function is the [one-time initialization callback function](/windows/win32/api/synchapi/nc-synchapi-pinit_once_fn).</span></span> <span data-ttu-id="22852-112">`InitHandleFunction` 呼叫 [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) 函數以建立事件，並傳回 *lpCoNtext* 參數中的事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="22852-112">`InitHandleFunction` calls the [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) function to create the event and returns the event handle in the *lpContext* parameter.</span></span>


```C++
#define _WIN32_WINNT 0x0600
#include <windows.h>

// Global variable for one-time initialization structure
INIT_ONCE g_InitOnce = INIT_ONCE_STATIC_INIT; // Static initialization

// Initialization callback function 
BOOL CALLBACK InitHandleFunction (
    PINIT_ONCE InitOnce,        
    PVOID Parameter,            
    PVOID *lpContext);           

// Returns a handle to an event object that is created only once
HANDLE OpenEventHandleSync()
{
  PVOID lpContext;
  BOOL  bStatus;
  
  // Execute the initialization callback function 
  bStatus = InitOnceExecuteOnce(&g_InitOnce,          // One-time initialization structure
                                InitHandleFunction,   // Pointer to initialization callback function
                                NULL,                 // Optional parameter to callback function (not used)
                                &lpContext);          // Receives pointer to event object stored in g_InitOnce

  // InitOnceExecuteOnce function succeeded. Return event object.
  if (bStatus)
  {
    return (HANDLE)lpContext;
  }
  else
  {
    return (INVALID_HANDLE_VALUE);
  }
}

// Initialization callback function that creates the event object 
BOOL CALLBACK InitHandleFunction (
    PINIT_ONCE InitOnce,        // Pointer to one-time initialization structure        
    PVOID Parameter,            // Optional parameter passed by InitOnceExecuteOnce            
    PVOID *lpContext)           // Receives pointer to event object           
{
  HANDLE hEvent;

  // Create event object
  hEvent = CreateEvent(NULL,    // Default security descriptor
                       TRUE,    // Manual-reset event object
                       TRUE,    // Initial state of object is signaled 
                       NULL);   // Object is unnamed

  // Event object creation failed.
  if (NULL == hEvent)
  {
    return FALSE;
  }
  // Event object creation succeeded.
  else
  {
    *lpContext = hEvent;
    return TRUE;
  }
}
```



## <a name="asynchronous-example"></a><span data-ttu-id="22852-113">非同步範例</span><span class="sxs-lookup"><span data-stu-id="22852-113">Asynchronous Example</span></span>

<span data-ttu-id="22852-114">在此範例中， `g_InitOnce` 全域變數是一次性的初始化結構。</span><span class="sxs-lookup"><span data-stu-id="22852-114">In this example, the `g_InitOnce` global variable is the one-time initialization structure.</span></span> <span data-ttu-id="22852-115">它會使用 INIT 來 **靜態 \_ 初始化 \_ \_**。</span><span class="sxs-lookup"><span data-stu-id="22852-115">It is initialized statically using **INIT\_ONCE\_STATIC\_INIT**.</span></span>

<span data-ttu-id="22852-116">`OpenEventHandleAsync`函數會將控制碼傳回給只建立一次的事件。</span><span class="sxs-lookup"><span data-stu-id="22852-116">The `OpenEventHandleAsync` function returns a handle to an event that is created only once.</span></span> <span data-ttu-id="22852-117">`OpenEventHandleAsync` 呼叫 [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) 函式以進入初始化狀態。</span><span class="sxs-lookup"><span data-stu-id="22852-117">`OpenEventHandleAsync` calls the [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) function to enter the initializing state.</span></span>

<span data-ttu-id="22852-118">如果呼叫成功，程式碼就會檢查 *fPending* 參數的值，以判斷是否要建立事件，或只將控制碼傳回給另一個執行緒所建立的事件。</span><span class="sxs-lookup"><span data-stu-id="22852-118">If the call succeeds, the code checks the value of the *fPending* parameter to determine whether to create the event or simply return a handle to the event created by another thread.</span></span> <span data-ttu-id="22852-119">如果 *fPending* 為 **FALSE**，初始化已完成，因此會 `OpenEventHandleAsync` 傳回 *lpCoNtext* 參數中所傳回的事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="22852-119">If *fPending* is **FALSE**, initialization has already completed so `OpenEventHandleAsync` returns the event handle returned in the *lpContext* parameter.</span></span> <span data-ttu-id="22852-120">否則，它會呼叫 [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) 函數來建立事件和 [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) 函式來完成初始化。</span><span class="sxs-lookup"><span data-stu-id="22852-120">Otherwise, it calls the [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) function to create the event and the [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) function to complete the initialization.</span></span>

<span data-ttu-id="22852-121">如果 [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) 的呼叫成功，會傳回 `OpenEventHandleAsync` 新的事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="22852-121">If the call to [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) succeeds, `OpenEventHandleAsync` returns the new event handle.</span></span> <span data-ttu-id="22852-122">否則，它會關閉事件控制碼，並使用 INIT 呼叫 [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) **\_ 一次 \_ \_** ，以判斷初始化失敗或其他執行緒是否已完成。</span><span class="sxs-lookup"><span data-stu-id="22852-122">Otherwise, it closes the event handle and calls [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) with **INIT\_ONCE\_CHECK\_ONLY** to determine whether initialization failed or was completed by another thread.</span></span>

<span data-ttu-id="22852-123">如果初始化是由另一個執行緒完成，則會 `OpenEventHandleAsync` 傳回 *lpCoNtext* 中傳回的事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="22852-123">If the initialization was completed by another thread, `OpenEventHandleAsync` returns the event handle returned in *lpContext*.</span></span> <span data-ttu-id="22852-124">否則，它會傳回 **不正確 \_ 控制碼 \_ 值**。</span><span class="sxs-lookup"><span data-stu-id="22852-124">Otherwise, it returns **INVALID\_HANDLE\_VALUE**.</span></span>


```C++
#define _WIN32_WINNT 0x0600
#include <windows.h>

// Global variable for one-time initialization structure
INIT_ONCE g_InitOnce = INIT_ONCE_STATIC_INIT; // Static initialization

// Returns a handle to an event object that is created only once
HANDLE OpenEventHandleAsync()
{
  PVOID  lpContext;
  BOOL   fStatus;
  BOOL   fPending;
  HANDLE hEvent;
  
  // Begin one-time initialization
  fStatus = InitOnceBeginInitialize(&g_InitOnce,       // Pointer to one-time initialization structure
                                    INIT_ONCE_ASYNC,   // Asynchronous one-time initialization
                                    &fPending,         // Receives initialization status
                                    &lpContext);       // Receives pointer to data in g_InitOnce  

  // InitOnceBeginInitialize function failed.
  if (!fStatus)
  {
    return (INVALID_HANDLE_VALUE);
  }

  // Initialization has already completed and lpContext contains event object.
  if (!fPending)
  {
    return (HANDLE)lpContext;
  }

  // Create event object for one-time initialization.
  hEvent = CreateEvent(NULL,    // Default security descriptor
                       TRUE,    // Manual-reset event object
                       TRUE,    // Initial state of object is signaled 
                       NULL);   // Object is unnamed

  // Event object creation failed.
  if (NULL == hEvent)
  {
    return (INVALID_HANDLE_VALUE);
  }

  // Complete one-time initialization.
  fStatus = InitOnceComplete(&g_InitOnce,             // Pointer to one-time initialization structure
                             INIT_ONCE_ASYNC,         // Asynchronous initialization
                             (PVOID)hEvent);          // Pointer to event object to be stored in g_InitOnce

  // InitOnceComplete function succeeded. Return event object.
  if (fStatus)
  {
    return hEvent;
  }
  
  // Initialization has already completed. Free the local event.
  CloseHandle(hEvent);


  // Retrieve the final context data.
  fStatus = InitOnceBeginInitialize(&g_InitOnce,            // Pointer to one-time initialization structure
                                    INIT_ONCE_CHECK_ONLY,   // Check whether initialization is complete
                                    &fPending,              // Receives initialization status
                                    &lpContext);            // Receives pointer to event object in g_InitOnce
  
  // Initialization is complete. Return handle.
  if (fStatus && !fPending)
  {
    return (HANDLE)lpContext;
  }
  else
  {
    return INVALID_HANDLE_VALUE;
  }
}
```



## <a name="related-topics"></a><span data-ttu-id="22852-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="22852-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22852-126">單次初始化</span><span class="sxs-lookup"><span data-stu-id="22852-126">One-Time Initialization</span></span>](one-time-initialization.md)
</dt> </dl>

 

 

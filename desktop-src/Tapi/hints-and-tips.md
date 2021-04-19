---
description: 以下是撰寫適用于 TAPI 3 的應用程式時應考慮的提示和秘訣
ms.assetid: 55aae46a-af5c-4b6d-89fc-9063f078bcd6
title: 提示和秘訣
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9202bdef97fb87b9f0736ed032b298af56917d8c
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106982165"
---
# <a name="hints-and-tips"></a><span data-ttu-id="59638-103">提示和秘訣</span><span class="sxs-lookup"><span data-stu-id="59638-103">Hints and Tips</span></span>

<span data-ttu-id="59638-104">以下是撰寫適用于 TAPI 3 的應用程式時所需考慮的提示和秘訣：</span><span class="sxs-lookup"><span data-stu-id="59638-104">The following are hints and tips to consider when writing an application for TAPI 3:</span></span>

1.  <span data-ttu-id="59638-105">COM [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) 會間接建立 windows;這對單元執行緒來說特別重要。</span><span class="sxs-lookup"><span data-stu-id="59638-105">COM [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) indirectly creates windows; this is especially important for apartment threading.</span></span> <span data-ttu-id="59638-106">如果執行緒建立任何視窗，則必須處理訊息。</span><span class="sxs-lookup"><span data-stu-id="59638-106">If a thread creates any windows, it must process messages.</span></span> <span data-ttu-id="59638-107">如果您的執行緒呼叫 **CoInitialize**，請執行訊息提取以防止發生問題。</span><span class="sxs-lookup"><span data-stu-id="59638-107">If your threads call **CoInitialize**, run a message pump to prevent problems.</span></span> <span data-ttu-id="59638-108">例如，COM 可能會停止正確地封送處理，或 COM 介面（例如 **IGlobalInterfaceTable** ）上的方法可能會停止回應。</span><span class="sxs-lookup"><span data-stu-id="59638-108">For example, COM might stop marshalling properly, or methods on COM interfaces, such as **IGlobalInterfaceTable** might hang.</span></span>

    <span data-ttu-id="59638-109">在單元執行緒中，不論您是否等候同步處理物件，您都必須擁有訊息抽取。</span><span class="sxs-lookup"><span data-stu-id="59638-109">In apartment threading you must have a message pump regardless of whether you wait for synchronization objects.</span></span> <span data-ttu-id="59638-110">如果您有一個主控台應用程式，或您在沒有主控台或 GUI 的情況下寫入 COM 本機/遠端伺服器 (物件，但控制項只是在系統) 中執行，則這點特別重要。</span><span class="sxs-lookup"><span data-stu-id="59638-110">This is particularly important if you have a console application or you write a COM local/remote server object that is apartment threaded (where you do not have a console or a GUI, but the control just "runs" in the system).</span></span>

    > [!Caution]  
    > <span data-ttu-id="59638-111">呼叫等候和同步處理函數時，例如 [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep)、 [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects)、 [**WaitForMultipleObjectsEx**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex)、 [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)、 [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)等等。</span><span class="sxs-lookup"><span data-stu-id="59638-111">When calling the wait and synchronization functions, such as [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep), [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects), [**WaitForMultipleObjectsEx**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex), [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex), and so on.</span></span> <span data-ttu-id="59638-112">相反地，請使用 [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) 和處理訊息，或使用 [**CoWaitForMultipleHandles**](/windows/desktop/api/combaseapi/nf-combaseapi-cowaitformultiplehandles)，這會自動偵測執行緒在 (STA 或 MTA) 中的哪一種類型，並 (在 **WaitForMultipleObjects** (上的 sta) 或封鎖時，等候) 的 mta。</span><span class="sxs-lookup"><span data-stu-id="59638-112">Instead, use [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) and process the messages, or use [**CoWaitForMultipleHandles**](/windows/desktop/api/combaseapi/nf-combaseapi-cowaitformultiplehandles), which will automatically detect what type of apartment the thread is in (STA or MTA) and will wait either in a COM modal loop (if STA) or block on **WaitForMultipleObjects** (if MTA).</span></span> <span data-ttu-id="59638-113">**MsgWaitForMultipleObjects** 和 **CoWaitForMultipleHandles** 也會根據 COM 規則來處理 windows 訊息。</span><span class="sxs-lookup"><span data-stu-id="59638-113">**MsgWaitForMultipleObjects** and **CoWaitForMultipleHandles** also process windows messages according to the COM rules.</span></span>

     

    <span data-ttu-id="59638-114">例如，不要這樣撰寫：</span><span class="sxs-lookup"><span data-stu-id="59638-114">For example, instead of:</span></span>

    `Sleep (5000);`

    <span data-ttu-id="59638-115">使用︰</span><span class="sxs-lookup"><span data-stu-id="59638-115">Use:</span></span>

    ``` syntax
     {
       DWORD dwSignalled;
       HANDLE heventDone = CreateEvent(0, FALSE, FALSE, 0);

       CoWaitForMultipleHandles (COWAIT_ALERTABLE,
                             5000,
                             1,
                             &heventDone,
                             &dwSignalled);

       CloseHandle(heventDone);
     }
    ```

2.  <span data-ttu-id="59638-116">**ITTAPIEventNotification：： Event** 是在 TAPI 3 回呼執行緒上呼叫的 apps 事件函數。</span><span class="sxs-lookup"><span data-stu-id="59638-116">**ITTAPIEventNotification::Event** is the apps Event function called on a TAPI 3 callback thread.</span></span>

    <span data-ttu-id="59638-117">在事件常式中完成最小值;相反地，請盡可能使用您自己的執行緒。</span><span class="sxs-lookup"><span data-stu-id="59638-117">Do the minimum in the Event routine; instead, use your own thread where possible.</span></span>

    <span data-ttu-id="59638-118">請注意，已提供下列程式碼範例，但不是必要條件。</span><span class="sxs-lookup"><span data-stu-id="59638-118">Be aware that the following code example is provided, but is not a requirement.</span></span>

    ```syntax
    #include <windows.h>

    HRESULT
    STDMETHODCALLTYPE
    CTAPIEventNotification::Event(
        TAPI_EVENT TapiEvent,
        IDispatch *pEvent)
    {
        //
        // Addref the event so that it does not go away.
        //
        pEvent->AddRef();

        //
        // Post a message for reference.
        //
        BOOL RetVal = PostMessage(
                                  ghDlg,
                                  WM_PRIVATETAPIEVENT,
                                  (WPARAM) TapiEvent,
                                  (LPARAM) pEvent
                                  );

        // If (RetVal == 0 ) process error here.

        return S_OK;
    }     
    ```

3.  <span data-ttu-id="59638-119">呼叫 [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize)之後，請勿操作 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="59638-119">Do not manipulate COM objects after calling [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize).</span></span> <span data-ttu-id="59638-120">結果無法預期，且對狀況良好的應用程式不利。</span><span class="sxs-lookup"><span data-stu-id="59638-120">The results are unpredictable and detrimental to a healthy application.</span></span> <span data-ttu-id="59638-121">可能會發生這種情況的一些範例，就是在應用程式呼叫 **CoUninitialize** 之後可能會執行的工作者執行緒和 c + + 析構函數。</span><span class="sxs-lookup"><span data-stu-id="59638-121">Some examples in which this can happen are worker threads and C++ destructors that may execute after an application calls **CoUninitialize**.</span></span>

 

 

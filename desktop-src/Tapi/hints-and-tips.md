---
description: 以下是撰寫適用于 TAPI 3 的應用程式時應考慮的提示和秘訣
ms.assetid: 55aae46a-af5c-4b6d-89fc-9063f078bcd6
title: 提示和提示
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57d51e8c7e3f8c6e4a9e38b27fa5cfe4c10e45d37cfa67af095d573eea319614
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762929"
---
# <a name="hints-and-tips"></a>提示和提示

以下是撰寫適用于 TAPI 3 的應用程式時所需考慮的提示和秘訣：

1.  COM [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) 會間接建立 windows;這對單元執行緒來說特別重要。 如果執行緒建立任何視窗，則必須處理訊息。 如果您的執行緒呼叫 **CoInitialize**，請執行訊息提取以防止發生問題。 例如，COM 可能會停止正確地封送處理，或 COM 介面（例如 **IGlobalInterfaceTable** ）上的方法可能會停止回應。

    在單元執行緒中，不論您是否等候同步處理物件，您都必須擁有訊息抽取。 如果您有一個主控台應用程式，或您在沒有主控台或 GUI 的情況下寫入 COM 本機/遠端伺服器 (物件，但控制項只是在系統) 中執行，則這點特別重要。

    > [!Caution]  
    > 呼叫等候和同步處理函數時，例如 [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep)、 [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects)、 [**WaitForMultipleObjectsEx**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex)、 [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)、 [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)等等。 相反地，請使用 [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) 和處理訊息，或使用 [**CoWaitForMultipleHandles**](/windows/desktop/api/combaseapi/nf-combaseapi-cowaitformultiplehandles)，這會自動偵測執行緒在 (STA 或 MTA) 中的哪一種類型，並 (在 **WaitForMultipleObjects** (上的 sta) 或封鎖時，等候) 的 mta。 **MsgWaitForMultipleObjects** 和 **CoWaitForMultipleHandles** 也會根據 COM 規則來處理 windows 訊息。

     

    例如，不要這樣撰寫：

    `Sleep (5000);`

    使用︰

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

2.  **ITTAPIEventNotification：： Event** 是在 TAPI 3 回呼執行緒上呼叫的 apps 事件函數。

    在事件常式中完成最小值;相反地，請盡可能使用您自己的執行緒。

    請注意，已提供下列程式碼範例，但不是必要條件。

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

3.  呼叫 [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize)之後，請勿操作 COM 物件。 結果無法預期，且對狀況良好的應用程式不利。 可能會發生這種情況的一些範例，就是在應用程式呼叫 **CoUninitialize** 之後可能會執行的工作者執行緒和 c + + 析構函數。

 

 

---
description: 非同步事件通知是一種技術，可讓應用程式在不需要獨佔系統資源的情況下，持續監視事件。
ms.assetid: 69ec8ead-9073-4689-bc66-5134728ab147
ms.tgt_platform: multiple
title: 接收非同步事件通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c84f6c441fc5c468b0ce7d39477d52911c6ae3becb1c4c15b5130ffb041040c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130890"
---
# <a name="receiving-asynchronous-event-notifications"></a>接收非同步事件通知

非同步事件通知是一種技術，可讓應用程式在不需要獨佔系統資源的情況下，持續監視事件。 非同步事件通知具有與其他非同步呼叫相同的安全性限制。 您可以改為進行半執行呼叫。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

路由至用戶端的非同步事件佇列可能會變得很大。 因此，WMI 會實行全系統的原則，以避免記憶體不足。 WMI 會減緩事件，或當佇列成長超過特定大小時，從佇列開始卸載事件。

WMI 會使用 [**Win32 \_ WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting)類別的 [**LowThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting)和 [**HighThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting)屬性，來設定記憶體外避免的限制。 最小值會指出 WMI 何時會開始減緩事件通知，而最大值則指出何時要開始卸載事件。 低和高臨界值的預設值為 1000000 (10 MB) 和 2000000 (20 MB) 。 此外，您可以設定 [**MaxWaitOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) 屬性來描述 WMI 在卸載事件之前應等待的時間量。 **MaxWaitOnEvents** 的預設值為2000或2秒。

## <a name="receiving-asynchronous-event-notifications-in-vbscript"></a>在 VBScript 中接收非同步事件通知

接收事件通知的腳本呼叫基本上與所有具有相同安全性問題的非同步呼叫相同。 如需詳細資訊，請參閱 [使用 VBScript 進行非同步呼叫](making-an-asynchronous-call-with-vbscript.md)。

**若要在 VBScript 中接收非同步事件通知**

1.  藉由呼叫 [Wscript.echo CreateObject](/previous-versions//xzysf6hc(v=vs.85)) ，並指定 "WbemScripting" 的 Progid 和 [**SWbemSink**](swbemsink.md)的物件類型，以建立接收物件。 接收物件會收到通知。
2.  針對您想要處理的每個事件撰寫副程式。 下表列出 [**SWbemSink**](swbemsink.md) 事件。

    

    | 事件                                            | 意義                                                                                                                         |
    |--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
    | [**OnObjectReady**](swbemsink-onobjectready.md) | 回報將物件傳回至接收。 使用這個呼叫會每次都傳回一個物件，直到作業完成為止。     |
    | [**OnCompleted**](swbemsink-oncompleted.md)     | 報告非同步呼叫完成的時間。 如果作業沒有限制，則永遠不會發生此事件。                          |
    | [**OnObjectPut**](swbemsink-onobjectput.md)     | 報告非同步 put 作業的完成。 此事件會傳回實例或已儲存類別的物件路徑。 |
    | [**OnProgress**](swbemsink-onprogress.md)       | 報告進行中之非同步呼叫的狀態。 並非所有提供者都支援過渡進度報表。             |
    | [**取消**](swbemsink-cancel.md)               | 取消與這個物件接收相關聯的所有未完成非同步作業。                                        |

    

     

下列 VBScript 程式碼範例會以10秒的輪詢間隔，通知刪除進程。 在此腳本中，副程式接收器 \_ OnObjectReady 會處理事件發生。 在此範例中，接收物件會命名為 "Sink"，不過您可以依照您的選擇來命名此物件。


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set MySink = WScript.CreateObject( _
    "WbemScripting.SWbemSink","SINK_")

objWMIservice.ExecNotificationQueryAsync MySink, _
    "SELECT * FROM __InstanceDeletionEvent" _
    & " WITHIN 10 WHERE TargetInstance ISA 'Win32_Process'"


WScript.Echo "Waiting for events..."

While (True)
    Wscript.Sleep(1000)
Wend

Sub SINK_OnObjectReady(objObject, objAsyncContext)
    Wscript.Echo "__InstanceDeletionEvent event has occurred."
End Sub

Sub SINK_OnCompleted(objObject, objAsyncContext)
    WScript.Echo "Event call complete."
End Sub
```



## <a name="receiving-asynchronous-event-notifications-in-c"></a>在 c + + 中接收非同步事件通知

若要執行非同步通知，您只需建立個別的執行緒來監視和接收來自 Windows Management Instrumentation (WMI) 的事件。 當該執行緒收到訊息時，執行緒會通知您的主應用程式。

藉由專門建立個別的執行緒，您可以允許您的主要進程在等候事件抵達時執行其他活動。 非同步傳遞通知可改善效能，但可提供比您想要更低的安全性。 在 c + + 中，您可以選擇使用 [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) 介面，或對安全描述項執行存取檢查。 如需詳細資訊，請參閱 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)。

**若要設定非同步事件通知**

1.  在初始化任何非同步通知之前，請確定已在 [**Win32 \_ WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting)中正確設定您的記憶體不足的規避參數。

2.  決定您想要接收的事件種類。

    WMI 支援內部和外來事件。 內建事件是 WMI 預先定義的事件，而外建事件則是由協力廠商提供者所定義的事件。 如需詳細資訊，請參閱 [決定要接收的事件種類](determining-the-type-of-event-to-receive.md)。

下列程式描述如何在 c + + 中接收非同步事件通知。

**若要在 c + + 中接收非同步事件通知**

1.  使用 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) 和 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) 函數的呼叫來設定應用程式。

    呼叫 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) 會初始化 COM，而 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) 則會授與 WMI 呼叫取用者進程的許可權。 **CoInitializeEx** 函式也會授與您設計多執行緒應用程式的能力，這是非同步通知的必要專案。 如需詳細資訊，請參閱 [維護 WMI 安全性](maintaining-wmi-security.md)。

    本主題中的程式碼需要下列參考，且必須 \# 要有語句才能正確編譯。

    ```C++
    #define _WIN32_DCOM
    #include <iostream>
    using namespace std;
    #include <wbemidl.h>
    ```

    

    下列程式碼範例說明如何使用 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) 和 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)的呼叫來設定暫時性事件取用者。

    ```C++
    void main(int argc, char **argv)
    {
        HRESULT hr = 0;
        hr = CoInitializeEx (0, COINIT_MULTITHREADED);
        hr = CoInitializeSecurity (NULL, 
           -1, 
           NULL, 
           NULL,   
           RPC_C_AUTHN_LEVEL_NONE, 
           RPC_C_IMP_LEVEL_IMPERSONATE, 
           NULL,
           EOAC_NONE,
           NULL); 

        if (FAILED(hr))
        {
           CoUninitialize();
           cout << "Failed to initialize security. Error code = 0x"
               << hex << hr << endl;
           return;
        }

    // ...
    }
    ```

    

2.  透過 [**IWbemObjectSink**](iwbemobjectsink.md) 介面建立接收器物件。

    WMI 使用 [**IWbemObjectSink**](iwbemobjectsink.md) 來傳送事件通知，以及報告非同步作業或事件通知的狀態。

3.  透過呼叫 [**IWbemServices：： ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) 方法來註冊您的事件取用者。

    請確定 *pResponseHandler* 參數指向在上一個步驟中建立的接收器物件。

    註冊的目的是只接收必要的通知。 接收多餘的通知會浪費處理和傳遞時間;而且不會使用 WMI 的篩選能力來發揮最大潛力。

    不過，暫時取用者可以接收一個以上的事件種類。 在此情況下，暫存取用者必須針對每個事件種類進行個別的 [**IWbemServices：： ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) 呼叫。 例如，取用者可能會在建立新的進程 (實例建立事件或 [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)) ，以及 (登錄事件（例如 [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)) ）的變更時，要求通知。 因此，取用者會對 [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) 進行一次呼叫，以註冊實例建立事件和另一個對 **ExecNotificationQueryAsync** 的呼叫，以註冊註冊事件。

    如果您選擇建立事件取用者來註冊多個事件，您應該避免使用相同的接收來註冊多個類別。 相反地，請針對每個已註冊事件的類別使用個別的接收。 具有專用接收可簡化處理和輔助維護，讓您可以取消一個註冊，而不會影響其他註冊。

4.  在事件取用者中執行任何必要的活動。

    此步驟應該包含大部分的程式碼，並包含將事件顯示為使用者介面的這類活動。

5.  完成時，透過呼叫 [**IWbemServices：： CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) 事件來取消註冊暫存事件取用者。

    不論 [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) 的呼叫成功或失敗，除非物件參考計數到達零，否則請勿刪除接收器物件。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

 

 

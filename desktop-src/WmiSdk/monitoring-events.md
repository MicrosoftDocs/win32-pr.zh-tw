---
description: 系統管理員可以使用 WMI 來監視網路上的事件。
ms.assetid: 871d4add-a7b1-4ec9-a202-3821fdf09e9f
ms.tgt_platform: multiple
title: 監視事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb90a0a6eef87f88543e8f2414bc38bdea4f7d89c577471d79d23393f331b053
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118317112"
---
# <a name="monitoring-events"></a>監視事件

系統管理員可以使用 WMI 來監視網路上的事件。 例如：

-   服務意外停止。
-   伺服器變得無法使用。
-   磁片磁碟機填滿80% 的容量。
-   安全性事件會回報給 NT 事件記錄檔。

WMI 支援事件偵測並傳遞給事件取用者，因為某些 WMI 提供者是事件提供者。 如需詳細資訊，請參閱 [接收 WMI 事件](receiving-a-wmi-event.md)。

[*事件取用者*](gloss-e.md) 是要求事件通知的應用程式或腳本，然後在發生特定事件時執行工作。 您可以建立事件監視腳本，或在事件發生時暫時監視的應用程式。 WMI 也提供一組預先安裝的永久事件提供者和永久的取用者類別，可讓您永久監視事件。 如需詳細資訊，請參閱 [使用標準取用者監視及回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。

本主題將討論下列各節：

-   [使用暫存事件取用者](#using-temporary-event-consumers)
-   [使用永久事件取用者](#using-permanent-event-consumers)

## <a name="using-temporary-event-consumers"></a>使用暫存事件取用者

暫存事件取用者是傳回符合事件查詢或篩選準則之事件的腳本或應用程式。 暫存事件查詢通常會使用 c + + 應用程式中的 [**IWbemServices：： ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery)或腳本和 Visual Basic 中的 [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) 。

事件查詢會要求事件類別的實例，以指定特定類型的事件，例如 [**Win32 \_ ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) 或 [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)。

下列 VBScript 程式碼範例會在建立 [**Win32 \_ ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) 的實例時要求通知。 當處理常式啟動或停止時，就會產生這個類別的實例。

若要執行腳本，請將它複製到名為 event.vbs 的檔案，並使用下列命令列： **cscript event.vbs**。 您可以啟動 Notepad.exe 或任何其他進程，查看腳本的輸出。 腳本會在五個進程啟動或停止之後停止。

此腳本會呼叫 [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md)，這是方法的最 [*半同步*](gloss-s.md) 版本。 請參閱下一個腳本，以取得透過呼叫 [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md)來設定非同步暫存事件訂閱的範例。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。 腳本會呼叫 [**SWbemEventSource**](swbemeventsource-nextevent.md) ，以在每個事件抵達時取得並處理它。 將腳本儲存在副檔名為 .vbs 的檔案中，並使用 CScript： **cscript file.vbs** 在命令列上執行腳本。


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" _
    & strComputer & "\root\CIMV2") 
Set objEvents = objWMIService.ExecNotificationQuery _
    ("SELECT * FROM Win32_ProcessTrace")

Wscript.Echo "Waiting for events ..."
i = 0
Do Until i=5
    Set objReceivedEvent = objEvents.NextEvent
    'report an event
    Wscript.Echo "Win32_ProcessTrace event occurred" & VBNewLine _
        & "Process Name = " _
            & objReceivedEvent.ProcessName & VBNewLine _
        & "Process ID = " _
            & objReceivedEvent.Processid & VBNewLine _
        & "Session ID = " & objReceivedEvent.SessionID 
i = i+ 1
Loop
```



暫存事件取用者必須以手動方式啟動，而且不得跨 WMI 重新開機或作業系統重新開機來保存。 暫存事件取用者只能在執行時處理事件。

下列程式描述如何建立暫存事件取用者。

**建立暫存事件取用者**

1.  決定要使用的程式設計語言。

    程式設計語言會決定要使用的 API。

    -   針對 c + + 程式設計語言，請使用 [適用于 WMI 的 COM API](com-api-for-wmi.md)。
    -   針對 Visual Basic 或指令碼語言，請使用[適用于 WMI 的腳本 API](scripting-api-for-wmi.md)。

2.  以您啟動 WMI 應用程式的相同方式開始撰寫暫存事件取用者應用程式的程式碼。

    程式碼的第一個步驟取決於程式設計語言。 一般來說，您會登入 WMI 並設定安全性設定。 如需詳細資訊，請參閱 [建立 WMI 應用程式或腳本](creating-a-wmi-application-or-script.md)。

3.  定義您想要使用的事件查詢。

    若要取得某些類型的效能資料，您可能需要使用高效能提供者所提供的類別。 如需詳細資訊，請參閱 [監視效能資料](monitoring-performance-data.md)、 [判斷要接收的事件種類](determining-the-type-of-event-to-receive.md)，以及 [使用 WQL 查詢](querying-with-wql.md)。

4.  決定要進行非同步呼叫或半執行呼叫，然後選擇 API 方法。

    非同步呼叫可讓您避免輪詢資料的額外負荷。 不過，半同步呼叫可提供類似的效能，並提供更高的安全性。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

5.  進行非同步或半同步方法呼叫，並將事件查詢包含為 *strQuery* 參數。

    若是 c + + 應用程式，請呼叫下列方法：

    -   [**IWbemServices：： ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery)
    -   [**IWbemServices：： ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)

    針對腳本，請呼叫下列方法：

    -   [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md)
    -   [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md)

6.  撰寫程式碼來處理傳回的事件物件。

    若為非同步事件查詢，請將程式碼放在物件接收的各種方法或事件中。 若為半活動查詢，每個物件會在 WMI 取得時傳回，因此程式碼應該在處理每個物件的迴圈中。

下列腳本程式碼範例是 [**Win32 \_ ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) 腳本的非同步版本。 由於非同步作業會立即傳回，因此當腳本正在等候事件時，對話方塊會保持作用中狀態。

腳本會有 [**SWbemSink OnObjectReady**](swbemsink-onobjectready.md)事件的事件處理常式，而不是呼叫 [**SWbemEventSource NextEvent**](swbemeventsource-nextevent.md)來接收每個事件。


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\CIMV2") 
Set EventSink = WScript.CreateObject( _
    "WbemScripting.SWbemSink","SINK_")

objWMIservice.ExecNotificationQueryAsync EventSink, _
    "SELECT * FROM Win32_ProcessTrace WITHIN 10"
WScript.Echo "Waiting for events..."

i = 0
While (True)
    Wscript.Sleep(1000)
Wend

Sub SINK_OnObjectReady(objObject, objAsyncContext)
    Wscript.Echo "Win32_ProcessTrace event has occurred."
    i = i+1
    If i = 3 Then WScript.Quit 0 
End Sub

```



> [!Note]
>
> 非同步回呼，例如副程式所處理的回呼 `SINK_OnObjectReady` ，可讓 nonauthenticated 使用者提供資料給接收。 為了獲得更好的安全性，請使用兩個同步通訊或同步通訊。 如需詳細資訊，請參閱下列主題：
>
> -   [使用 c + + 進行半同步呼叫](making-a-semisynchronous-call-with-c--.md)
> -   [使用 VBScript 進行半同步呼叫](making-a-semisynchronous-call-with-vbscript.md)
> -   [使用 c + + 進行非同步呼叫](making-an-asynchronous-call-with-c--.md)
> -   [使用 VBScript 進行非同步呼叫](making-an-asynchronous-call-with-vbscript.md)
> -   [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)
> -   [保護腳本用戶端](securing-scripting-clients.md)

 

## <a name="using-permanent-event-consumers"></a>使用永久事件取用者

永久事件取用者會執行，直到明確取消其註冊，然後在 WMI 或系統重新開機時啟動。

永久事件取用者是系統上 WMI 類別、篩選和 COM 物件的組合。

下列清單會識別建立永久性事件取用者所需的元件：

-   COM 物件，其中包含可執行永久取用者的程式碼。
-   新的永久取用者類別。
-   永久取用者類別的實例。
-   包含事件查詢的篩選準則。
-   取用者與篩選之間的連結。

如需詳細資訊，請參閱 [所有時間的接收事件](--filtertoconsumerbinding.md)。

WMI 提供數個永久取用者。 已預先安裝包含程式碼的取用者類別和 COM 物件。 例如，您可以建立並設定 [**ActiveScriptEventConsumer**](activescripteventconsumer.md) 類別的實例，以便在發生事件時執行腳本。 如需詳細資訊，請參閱 [使用標準取用者監視及回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。 如需使用 **ActiveScriptEventConsumer** 的範例，請參閱 [根據事件執行腳本](running-a-script-based-on-an-event.md)。

下列程式描述如何建立永久事件取用者。

**建立永久事件取用者**

1.  向您使用的命名空間[註冊事件提供者](registering-a-provider.md)。

    某些事件提供者只能使用特定的命名空間。 例如， [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)是 [Win32 提供者](/windows/desktop/CIMWin32Prov/win32-provider)所支援的內建事件，並且預設會與 \\ 根 \\ cimv2 命名空間一起註冊。

    > [!Note]  
    > 您可以使用註冊中所使用之 [**\_ \_ >eventfilter**](--eventfilter.md)的 **EventNamespace** 屬性來建立跨命名空間的訂用帳戶。 如需詳細資訊，請參閱 [實施跨命名空間永久事件訂閱](implementing-cross-namespace-permanent-event-subscriptions.md)。

     

2.  向事件類別所在的命名空間[註冊事件取用者提供](registering-an-event-consumer-provider.md)者。

    WMI 使用事件取用者提供者來尋找永久的事件取用者。 永久事件取用者是 WMI 在收到事件時所啟動的應用程式。 為了註冊事件取用者，提供者會建立 [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md)的實例。

3.  建立類別的實例，代表您要使用的永久事件取用者。

    事件取用者類別衍生自類別 [**\_ \_ EventConsumer**](--eventconsumer.md)。 設定事件取用者實例所需的屬性。

4.  使用 **regsvr32** 公用程式向 COM 註冊取用者。
5.  建立事件篩選類別 [**\_ \_ >eventfilter**](--eventfilter.md)的實例。

    設定事件篩選準則實例的必要欄位。 [**\_ \_ >Eventfilter**](--eventfilter.md)的必要欄位為 **Name**、 **QueryLanguage** 和 **Query**。 **Name** 屬性可以是這個類別之實例的任何唯一名稱。 **QueryLanguage** 屬性一律設為 "WQL"。 **查詢** 屬性是包含事件查詢的字串。 當永久事件取用者的查詢失敗時，就會產生事件。 事件的來源為 WinMgmt，事件識別碼為10，而事件種類為「錯誤」。

6.  建立 [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md)類別的實例，以將邏輯事件取用者與事件篩選器產生關聯。

    WMI 會使用關聯來尋找與事件相關聯的事件取用者，該事件符合事件篩選準則中指定的準則。 WMI 使用事件取用者提供者來尋找要啟動的永久事件取用者應用程式。

 

 

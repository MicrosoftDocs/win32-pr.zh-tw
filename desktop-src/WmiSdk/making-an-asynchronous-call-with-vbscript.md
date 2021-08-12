---
description: 對 WMI 方法或提供者方法進行非同步呼叫，可讓腳本在物件返回 SWbemSink 物件時繼續執行，而且會由 SWbemSink. OnObjectReady 等方法來處理。
ms.assetid: 61f401d9-c874-472d-8dd3-7cf9d7f20a12
ms.tgt_platform: multiple
title: 使用 VBScript 進行非同步呼叫
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee8c4737ff7513441532275e24f2cfe20f8e30fa2932e854cc566eb032c49d0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118555134"
---
# <a name="making-an-asynchronous-call-with-vbscript"></a>使用 VBScript 進行非同步呼叫

對 [*WMI 方法*](gloss-w.md) 或 [*提供者方法*](gloss-p.md) 進行非同步呼叫，可讓腳本在物件返回 [**SWbemSink**](swbemsink.md) 物件時繼續執行，而且會由 [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md)等方法來處理。 但是，不建議使用非同步呼叫，因為在進行呼叫時，資料可能不會以相同的安全性層級傳回。

使用非同步接收呼叫（例如 [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) ）來取得傳回的資料時，您可以設定下列登錄值。

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **UnsecAppAccessControlDefault**

設定此登錄值可確保傳回至接收的資料物件驗證。 如果 **UnsecAppAccessControlDefault** 設定為一個 (1) ，則 WMI 會執行資料傳回的存取檢查。 存取檢查會確認資料來自正確的來源。 如需詳細資訊，請參閱 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)。

名稱結尾為 "Async" 的非同步方法 \_ 一律會在呼叫後立即傳回，讓程式可以繼續執行。 例如， [**SWbemServices.ExecQuery**](swbemservices-execquery.md) 是同步的，並且會封鎖執行，直到傳回所有物件為止。 [**SWbemServices.Exe的 cQueryAsync**](swbemservices-execqueryasync.md)方法是非封鎖的非同步版本。 以更安全的方式呼叫 **SWbemServices.ExecQuery** 非封鎖的方式，就是進行呼叫 [*半同步方式*](gloss-s.md)。 如需詳細資訊，請參閱 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md) ，並 [使用 VBScript 進行半同步呼叫](making-a-semisynchronous-call-with-vbscript.md)。

非同步呼叫的 *iFlags* 參數一律預設為零 (0) 。 非同步方法不會提供 [**swbemobjectset 搭配使用**](swbemobjectset.md) 集合給接收器副程式。 相反地，您的腳本或應用程式中的 [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) 事件副程式會在每個物件提供時收到。

當原始非同步呼叫完成時，它會呼叫物件接收的 [**SWbemSink. OnCompleted**](swbemsink-oncompleted.md) 事件，然後執行您放置於其中的程式碼，以處理呼叫的結果。

> [!Note]  
> 使用中的伺服器頁 (ASP) 作為腳本主機，並不支援非同步呼叫。

 

下列程式描述如何使用 VBScript 進行非同步呼叫。

**使用 VBScript 進行非同步呼叫**

1.  連線至 WMI 並取得 [**SWbemServices**](swbemservices.md)物件。

    ```VB
    Set Service = GetObject("Winmgmts:")
    ```

    

2.  使用 [CreateObject](/previous-versions//xzysf6hc(v=vs.85))或 (為 Windows 腳本主機2.0 建立物件接收，只) 將 events 屬性設為 **TRUE** 的物件標記。

    ```VB
    Set sink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
    ```

    

    -或-

    ```VB
    <OBJECT progid="WbemScripting.SWbemSink" ID="SINK" events="true"/>
    ```

    

3.  針對非同步事件可以觸發的每個事件建立副程式。 這些事件會定義為 [**SWbemObject**](swbemobject.md)上的方法。 例如，WMI 會在每個實例傳回時，對 [**SWbemSink OnObjectReady 回呼。**](swbemsink-onobjectready.md)

    當您建立副程式時，請將程式碼放在副程式中，以在收到每個事件時處理。

    ```VB
    Sub SINK_OnCompleted(
          iHResult, 
          objErrorObject, 
          objAsyncContext
          )
        WScript.Echo "Asynchronous operation is done."
    End Sub

    Sub SINK_OnObjectReady(objObject, objAsyncContext)
        WScript.Echo (objObject.Name)
    End Sub
    ```

    

    檢查 [**OnCompleted**](swbemsink-oncompleted.md)事件所傳回的 *iHresult* 參數，以判斷非同步呼叫是否成功，或是否發生錯誤。 如果成功，在 *iHresult* 參數中傳遞的值等於零 (0) 。 任何其他值可能會指出錯誤，而您應該檢查 *objErrorObject* 參數中所傳回錯誤物件的值。

4.  進行非同步呼叫，並在 *objWbemSink* 參數中傳遞您接收器的名稱。

    ```VB
    Service.InstancesOfAsync sink, "Win32_process"
    ```

    

5.  進行呼叫，以防止腳本在接收到所有事件之前結束。 如果您的腳本可以使用螢幕介面執行，簡單的方式就是使用 Windows 腳本主機 (WSH) `Echo` 命令，如下列範例所示。

    ```VB
    WScript.Echo "Waiting for instances."
    ```

    

    當您執行此腳本時，您可能會在 **等候實例** 訊息之前看到第一個實例傳回，或您可能會看到它。 這是非同步處理的本質。 如果您太快關閉 [ **等待實例** ] 訊息方塊，則可能不會看到所有的實例。

6.  如果您有數個不同的非同步呼叫傳回相同接收的結果，請將任何必要的區分資料儲存在 *objWbemAsyncCoNtext* 內容參數中。

7.  完成接收時，請使用 [**cancel**](swbemsink-cancel.md) 方法取消您的非同步呼叫。

    ```VB
    objwbemsink.Cancel()
    ```

    

    [**Cancel**](swbemsink-cancel.md)方法會指示 WSH 取消與指定接收器物件相關聯的所有非同步呼叫。 因此，您可能會想要針對必須獨立的非同步作業使用不同的接收。

8.  藉由將接收器物件指派給來釋放接收器物件 `Nothing` 。

    ```VB
    set objwbemsink= Nothing
    ```

    

下列程式碼範例顯示本機電腦上所有 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process) 實例的非同步查詢。 如需相同方法的半同步版本，請參閱 [呼叫方法](calling-a-method.md)。


```VB
' Create an object sink
set oSink = WScript.CreateObject("wbemscripting.swbemsink","sink_")
' Connect to WMI and the cimv2 namespace, and obtain
' an SWbemServices object
set oSvc = GetObject("winmgmts:root\cimv2")

bdone = false
' Query for all Win32_Process objects
osvc.ExecQueryAsync oSink, "SELECT Name FROM Win32_Process"
' Wait until all instances are returned. 
' The bdone flag prevents the script from exiting until
' the sink.OnCompleted subroutine is executed when
' all the objects are returned.
while not bdone    
    wscript.sleep 1000
wend

' The sink subroutine to handle the OnObjectReady 
' event. This is called as each object returns.
sub sink_OnObjectReady(oInst, octx)
    WScript.Echo "Got Instance: " & oInst.Name
end sub
' The sink subroutine to handle the OnCompleted event.
' This is called when all the objects are returned. 
' The oErr parameter obtains an SWbemLastError object,
' if available from the provider.
sub sink_OnCompleted(HResult, oErr, oCtx)
    WScript.Echo "ExecQueryAsync completed"
    bdone = true
end sub
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[呼叫方法](calling-a-method.md)
</dt> <dt>

[維護 WMI 安全性](maintaining-wmi-security.md)
</dt> </dl>

 

 

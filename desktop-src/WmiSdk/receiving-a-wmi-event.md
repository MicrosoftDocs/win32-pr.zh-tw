---
description: WMI 包含的事件基礎結構會產生有關 WMI 資料和服務中變更的通知。 WMI 事件類別會在特定事件發生時提供通知。
ms.assetid: 347808a7-0f7b-4687-93f4-bea55c96795a
ms.tgt_platform: multiple
title: 接收 WMI 事件
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5dac8aba93cc841211cbdc02bc5e75773ab444eaa2763c4b0367fbd36ada37b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992588"
---
# <a name="receiving-a-wmi-event"></a>接收 WMI 事件

WMI 包含的事件基礎結構會產生有關 WMI 資料和服務中變更的通知。 WMI [*事件類別*](gloss-e.md) 會在特定事件發生時提供通知。

本主題將討論下列各節：

-   [事件查詢](#event-queries)
-   [範例](#example)
-   [事件取用者](#event-consumers)
-   [提供事件](#providing-events)
-   [訂用帳戶配額](#subscription-quotas)
-   [相關主題](#related-topics)

## <a name="event-queries"></a>事件查詢

您可以建立 [半同步](receiving-synchronous-and-semisynchronous-event-notifications.md) 或 [**非同步**](receiving-asynchronous-event-notifications.md) 查詢來監視事件記錄檔、進程建立、服務狀態、電腦可用性或磁片磁碟機可用空間，以及其他實體或事件的變更。 在腳本中，會使用 [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) 方法來訂閱事件。 在 c + + 中，會使用 [**IWbemServices：： ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) 。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

標準 WMI 資料模型中的變更通知稱為內建 [*事件*](gloss-i.md)。 [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)或 [**\_ \_ NamespaceDeletionEvent**](--namespacedeletionevent.md)是內部事件的範例。 提供者用來定義提供者事件之變更的通知，稱為 [*外來事件*](gloss-e.md)。 例如， [系統登錄提供者](/previous-versions/windows/desktop/regprov/system-registry-provider)、 [電源管理事件提供者](/windows/desktop/CIMWin32Prov/power-management-event-provider)和 [Win32 提供者](/windows/desktop/CIMWin32Prov/win32-provider) 會定義自己的事件。 如需詳細資訊，請參閱 [決定要接收的事件種類](determining-the-type-of-event-to-receive.md)。

## <a name="example"></a>範例

下列腳本程式碼範例是事件類別 [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent)內建 [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)的查詢。 您可以在背景中執行此程式，當發生事件時，就會出現一則訊息。 如果您關閉 [ **正在等候事件** ] 對話方塊，程式就會停止等候事件。 請注意，必須啟用 **SeSecurityPrivilege** 。


```VB
Sub SINK_OnObjectReady(objObject, objAsyncContext)
    WScript.Echo (objObject.TargetInstance.Message)
End Sub

Set objWMIServices = GetObject( _
    "WinMgmts:{impersonationLevel=impersonate, (security)}") 

' Create the event sink object that receives the events
Set sink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
 
' Set up the event selection. SINK_OnObjectReady is called when
' a Win32_NTLogEvent event occurs
objWMIServices.ExecNotificationQueryAsync sink,"SELECT * FROM __InstanceCreationEvent " & "WHERE TargetInstance ISA 'Win32_NTLogEvent' "

WScript.Echo "Waiting for events"
```


```PowerShell

# Define event Query
$query = "SELECT * FROM __InstanceCreationEvent 
          WHERE TargetInstance ISA 'Win32_NTLogEvent' "

<# Register for event - also specify an action that
displays the log event when the event fires.#>

Register-WmiEvent -Source Demo1 -Query $query -Action {
                Write-Host "Log Event occured"
                $global:myevent = $event
                Write-Host "EVENT MESSAGE"
                Write-Host $event.SourceEventArgs.NewEvent.TargetInstance.Message}
<# So wait #>
"Waiting for events"
```





下列 VBScript 程式碼範例顯示登錄提供者所定義的外建事件[ \_ \_ registryvaluechangeeven](registering-for-system-registry-events.md) 。 腳本會使用 [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md)的呼叫來建立暫時的取用者，而且只會在腳本執行時接收事件。 下列腳本會無限期地執行，直到電腦重新開機、WMI 已停止或腳本停止。 若要手動停止腳本，請使用工作管理員停止進程。 若要以程式設計方式停止它，請在 Win32 Process 類別中使用 [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) 方法 \_ 。 如需詳細資訊，請參閱 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)。


```VB
strComputer = "."

Set objWMIServices=GetObject( _
    "winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\default")

set objSink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")


objWMIServices.ExecNotificationQueryAsync objSink, _
    "Select * from RegistryValueChangeEvent Where Hive = 'HKEY_LOCAL_MACHINE' and KeyPath = 'SYSTEM\\ControlSet001\\Control' and ValueName = 'CurrentUser'"

WScript.Echo "Waiting for events..."

While (True) 
     WScript.Sleep (1000)
Wend

 
WScript.Echo "Listening for Registry Change Events..." & vbCrLf 

While(True) 
    WScript.Sleep 1000 
Wend 

Sub SINK_OnObjectReady(wmiObject, wmiAsyncContext) 
    WScript.Echo "Received Registry Value Change Event" & vbCrLf & wmiObject.GetObjectText_() 
End Sub
```



## <a name="event-consumers"></a>事件取用者

當腳本或應用程式正在執行時，您可以使用下列取用者來監視或取用事件：

-   暫存事件取用者

    [*暫時性取用者*](gloss-t.md)是接收 wmi 事件的 wmi 用戶端應用程式。 WMI 包含一個唯一的介面，用來指定要傳送至用戶端應用程式的 WMI 事件。 暫時的事件取用者被視為暫時性，因為它只有在使用者特別載入時才能運作。 如需詳細資訊，請參閱 [在您的應用程式期間接收事件](receiving-events-for-the-duration-of-your-application.md)。

-   永久事件取用者

    [*永久取用者*](gloss-p.md)是一種可隨時接收 WMI 事件的 COM 物件。 永久事件取用者會使用一組持續性物件和篩選來捕捉 WMI 事件。 如同暫時性的事件取用者，您可以設定一系列的 WMI 物件和篩選器來捕捉 WMI 事件。 當符合篩選準則的事件發生時，WMI 會載入永久事件取用者，並通知事件。 因為永久性取用者是在 WMI 存放庫中執行，而且是在 WMI 中註冊的可執行檔，所以永久事件取用者會在建立事件之後，以及在作業系統重新開機之後（只要 WMI 正在執行），就會操作和接收事件。 如需詳細資訊，請參閱 [所有時間的接收事件](receiving-events-at-all-times.md)。

接收事件的腳本或應用程式有特殊的安全性考慮。 如需詳細資訊，請參閱 [保護 WMI 事件](securing-wmi-events.md)。

應用程式或腳本可以使用內建的 WMI 事件提供者，以提供 [標準取用者類別](standard-consumer-classes.md)。 每個標準取用者類別都會傳送電子郵件訊息或執行腳本，以不同的動作來回應事件。 您不需要撰寫提供者程式碼，就能使用標準取用者類別來建立永久事件取用者。 如需詳細資訊，請參閱 [使用標準取用者監視及回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。

## <a name="providing-events"></a>提供事件

事件提供者是將事件傳送至 WMI 的 COM 元件。 您可以建立事件提供者，以在 c + + 或 c # 應用程式中傳送事件。 大部分的事件提供者會管理 WMI 的物件，例如應用程式或硬體專案。 如需詳細資訊，請參閱 [撰寫事件提供者](writing-an-event-provider.md)。

計時或重複事件是在預先定義的時間發生的事件。

WMI 提供下列方法來為您的應用程式建立計時或重複事件：

-   標準的 Microsoft 事件基礎結構。
-   特製化計時器類別。

如需詳細資訊，請參閱 [接收計時或重複事件](receiving-a-timed-or-repeating-event.md)。 當您撰寫事件提供者時，請考慮安全 [地提供事件](providing-events-securely.md)中所識別的安全性資訊。

建議將永久性事件訂閱編譯成根訂用帳戶 \\ \\ 命名空間。 如需詳細資訊，請參閱 [實施跨命名空間永久事件訂閱](implementing-cross-namespace-permanent-event-subscriptions.md)。

## <a name="subscription-quotas"></a>訂用帳戶配額

針對大型資料集支援查詢的提供者，輪詢事件可能會降低效能。 此外，對於具有動態提供者之命名空間的讀取權限的任何使用者，都可以執行拒絕服務 (DoS) 攻擊。 WMI 會針對位在根命名空間中 [**\_ \_ ArbitratorConfiguration**](--arbitratorconfiguration.md)單一實例的每個事件取用者，維護所有使用者的配額 \\ 。 這些配額是全域的，而不是每個命名空間。 您無法變更配額。

WMI 目前使用 [**\_ \_ ArbitratorConfiguration**](--arbitratorconfiguration.md)的屬性來強制執行配額。 每個配額都有每個使用者和包含所有使用者組合的總版本，而不是每個命名空間。 下表列出適用于 **\_ \_ ArbitratorConfiguration** 屬性的配額。



| Total/PerUser                                                                   | 配額                                                                       |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| TemporarySubscriptionsTotal<br/> TemporarySubscriptionsPerUser<br/> | 10,000<br/> 1,000<br/>                                          |
| PermanentSubscriptionsTotal<br/> PermanentSubscriptionsPerUser<br/> | 10,000<br/> 1,000<br/>                                          |
| PollingInstructionsTotal<br/> PollingInstructionsPerUser<br/>       | 10,000<br/> 1,000<br/>                                          |
| PollingMemoryTotal<br/> PollingMemoryPerUser<br/>                   | 10000000 (0x989680) 位元組<br/> 5000000 (0x4CB40) 位元組<br/> |



 

具有命名空間 **完整 \_ 寫入** 許可權的系統管理員或使用者可以修改 [**\_ \_ ArbitratorConfiguration**](--arbitratorconfiguration.md)的單一實例。 WMI 會追蹤每位使用者的配額。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 WMI](using-wmi.md)
</dt> </dl>

 


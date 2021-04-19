---
description: WMI 提供 COM API 和腳本 API 中的方法，以取得資訊或操作企業系統中的物件。
ms.assetid: 7a1eda93-014e-4067-b6d0-361a3d2fd1df
ms.tgt_platform: multiple
title: 呼叫 WMI 方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c327bbf0c4c90ad05d1c5026e3308e5fd8447aec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980713"
---
# <a name="calling-a-wmi-method"></a>呼叫 WMI 方法

WMI 提供 [COM API](com-api-for-wmi.md) 和 [腳本 API](scripting-api-for-wmi.md) 中的方法，以取得資訊或操作企業系統中的物件。 例如，WMI 腳本方法 [**SWbemServices.ExecQuery**](swbemservices-execquery.md) 查詢資料。 提供者也有在其註冊的類別中定義的方法。 範例包括 win32 [**\_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)方法 [**Chkdsk**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk)和 [Win32 提供者](/windows/desktop/CIMWin32Prov/win32-provider)所提供的 [**ScheduleAutoChk**](/windows/desktop/CIMWin32Prov/scheduleautochk-method-in-class-win32-logicaldisk) 。

本主題將討論下列各節：

-   [與提供者方法相較之下的 WMI 方法](#wmi-methods-compared-to-provider-methods)
-   [WMI 中的方法呼叫模式](#method-calling-modes-in-wmi)
    -   [同步模式](#synchronous-mode)
    -   [非同步模式](#asynchronous-mode)
    -   [半同步模式](#semisynchronous-mode)
-   [相關主題](#related-topics)

## <a name="wmi-methods-compared-to-provider-methods"></a>與提供者方法相較之下的 WMI 方法

藉由使用與 [*提供者方法*](gloss-p.md)呼叫結合的 [*WMI 方法*](gloss-w.md)呼叫，您可以取得和操作企業的相關資訊。 如需詳細資訊，請參閱 [呼叫 WMI 方法](calling-a-wmi-method.md) 和 [呼叫提供者方法](calling-a-provider-method.md)。

WMI 腳本物件 [**SWbemObject**](swbemobject.md) 的方法具有特殊狀態，因為它們可以套用至任何 WMI 資料類別。 如需詳細資訊，請參閱 [使用 SWbemObject 編寫腳本](scripting-with-swbemobject.md)。

下列程式碼範例會呼叫 WMI 和提供者方法。

下列 WMI 和提供者方法位於 [適用于 WMI 的腳本 API](scripting-api-for-wmi.md)：

-   **objWMIService.ExecQuery** 會呼叫 WMI 腳本方法 [ **SWbemServices.ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)
-   **objService. StopService ()** 會呼叫提供者方法 [ **Win32 \_ Service. StopService**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service)

您可以在 [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service)的 [傳回碼] 區段中，查詢可能出現在 [傳回] 中的程式碼。


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colServices = objWMIService.ExecQuery ("Select * from Win32_Service where Name='Alerter'")
For Each objService in colServices
    Return = objService.StopService()
    If Return <> 0 Then
        Wscript.Echo "Failed " &VBNewLine & "Error code = " & Return 
    Else
       WScript.Echo "Succeeded"
    End If
Next
```


```PowerShell

$colServices= Get-WmiObject -Class Win32_Service -Filter 'Name = &quot;Alerter&quot;'
foreach ($objService in $colServices)
{
    $objService.StopService()
}
```





## <a name="method-calling-modes-in-wmi"></a>WMI 中的 Method-Calling 模式

半同步呼叫模式通常會在安全性與效能之間提供最佳平衡。

如需每個可能模式的詳細資訊，請參閱下列各項：

-   [同步](#synchronous-mode)
-   [非同步](#asynchronous-mode)
-   [半同步](#semisynchronous-mode)

### <a name="synchronous-mode"></a>同步模式

當程式或腳本在方法呼叫傳回 [**swbemobjectset 搭配使用**](swbemobjectset.md) 集合物件之前暫停時，就會發生同步模式。 WMI 會在記憶體中建立此集合，然後將集合物件傳回給呼叫的程式或腳本。

在執行程式或腳本的電腦上，同步模式可能會對程式或腳本效能造成負面影響。 例如，從事件記錄檔同步取出上千個事件可能需要很長的時間，而且會耗用大量的記憶體，因為 WMI 會從每個事件建立一個物件，然後將這些物件放入集合，然後再將集合傳遞給方法。

您應該只呼叫不會在同步模式中傳回大型資料集的方法。 您可以在同步模式中安全地呼叫下列 [**SWbemServices**](swbemservices.md) 方法：

-   [**SWbemServices。刪除**](swbemservices-delete.md)
-   [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)
-   [**SWbemServices。 Get**](swbemservices-get.md)

您可以藉由在 *iFlags* 參數中設定 **wbemFlagReturnWhenComplete** 值，在名稱中使用 "Async" 這個字的任何 [**SWbemServices**](swbemservices.md)方法，都可以在同步模式中呼叫。

### <a name="asynchronous-mode"></a>非同步模式

當程式或腳本在呼叫方法之後繼續執行時，就會發生非同步模式。 當建立每個物件時，WMI 會將所有物件從方法傳回 [**SWbemSink**](swbemsink.md) 物件。 呼叫程式或腳本必須有 **SWbemSink** 物件和 [**SWbemSink OnObjectReady**](swbemsink-onobjectready.md) 事件處理常式，才能處理傳回的物件。 如需有關為非同步模式建立事件處理常式的詳細資訊，請參閱 [接收 WMI 事件](receiving-a-wmi-event.md)。

雖然此模式沒有同步模式的效能和資源影響，但非同步模式可能會造成嚴重的安全性風險，因為儲存在 [**SWbemSink**](swbemsink.md) 物件中的結果可能不是來自呼叫的程式或腳本。 WMI 會減少 **SWbemSink** 物件的驗證層級，直到方法成功為止。 如需如何減輕這些安全性風險的詳細資訊，請參閱 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)。

以 Async 這個字附加的方法是非同步模式的方法。 以下是非同步呼叫的方法：

-   [**SWbemServices. AssociatorsOfAsync**](swbemservices-associatorsofasync.md)
-   [**SWbemServices. DeleteAsync**](swbemservices-deleteasync.md)
-   [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md)
-   [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md)
-   [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md)
-   [**SWbemServices. InstancesOfAsync**](swbemservices-instancesofasync.md)
-   [**SWbemServices. ReferencesToAsync**](swbemservices-referencesto.md)
-   [**SWbemServices. SubclassesOfAsync**](swbemservices-subclassesofasync.md)

如需非同步模式的詳細資訊，請參閱：

-   [使用 c + + 進行非同步呼叫](making-an-asynchronous-call-with-c--.md)
-   [使用 VBScript 進行非同步呼叫](making-an-asynchronous-call-with-vbscript.md)

### <a name="semisynchronous-mode"></a>半同步模式

最半同步模式與非同步模式類似，因為程式或腳本會在呼叫方法之後繼續執行。 在半同步模式中，WMI 會在您的腳本或程式繼續執行時，在背景中抓取物件。 WMI 會在建立物件之後，將傳回的每個物件傳回給呼叫方法。

由於 WMI 會管理物件，因此，半同步模式比非同步模式更安全。 但是，如果您使用的是超過1000個實例的半同步模式，實例抓取可以獨佔可用的資源，這可能會降低程式或腳本的效能，以及使用程式或腳本的電腦。 在釋放記憶體之前，每個物件都會佔用必要的資源。

若要解決此狀況，您可以使用 *iFlags* 參數設定的 **wbemFlagForwardOnly** 和 **wbemFlagReturnImmediately** 旗標來呼叫方法，以指示 WMI 傳回順向 [**swbemobjectset 搭配使用**](swbemobjectset.md)。 順向 **swbemobjectset 搭配使用** 可在列舉物件之後釋放記憶體，以消除大型資料集所造成的效能問題。

任何無法在同步或非同步模式中呼叫的 [**SWbemServices**](swbemservices.md) 方法，都會以半同步模式來呼叫。

以半同步模式呼叫下列方法：

-   [**SWbemServices. AssociatorsOf**](swbemservices-associatorsof.md)
-   [**SWbemServices。刪除**](swbemservices-delete.md)
-   [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)
-   [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md)
-   [**SWbemServices.ExecQuery**](swbemservices-execquery.md)
-   [**SWbemServices。 Get**](swbemservices-get.md)
-   [**SWbemServices. InstancesOf**](swbemservices-instancesof.md)
-   [**SWbemServices. ReferencesTo**](swbemservices-referencesto.md)
-   [**SWbemServices. SubclassesOf**](swbemservices-subclassesof.md)
-   [**SWbemServices。 Put**](swbemservicesex-put.md)

如需有關半同步處理模式的詳細資訊，請參閱使用 [c + + 進行半進行呼叫](making-a-semisynchronous-call-with-c--.md) ，並 [使用 VBScript 進行半同步呼叫](making-a-semisynchronous-call-with-vbscript.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[改善列舉效能](improving-enumeration-performance.md)
</dt> <dt>

[使用 SWbemObject 編寫腳本](scripting-with-swbemobject.md)
</dt> <dt>

[**WbemFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)
</dt> </dl>

 

 

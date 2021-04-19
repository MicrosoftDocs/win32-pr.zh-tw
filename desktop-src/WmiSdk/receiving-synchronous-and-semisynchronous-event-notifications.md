---
description: 使用 SWbemServices.ExecQuery 來要求所有現有的事件。
ms.assetid: bc99719a-7e33-4e2d-8355-f8fc97c66f71
ms.tgt_platform: multiple
title: 接收同步和同步事件通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15327c66f7ba3e59824c94d54a206ec348c85952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987238"
---
# <a name="receiving-synchronous-and-semisynchronous-event-notifications"></a>接收同步和同步事件通知

使用 [**SWbemServices.ExecQuery**](swbemservices-execquery.md) 來要求所有現有的事件。

下列程式碼範例示範如何查詢記錄檔中的事件。

`Select * from Win32_NTLogEvent`

如需詳細資訊，請參閱 [判斷要接收的事件種類](determining-the-type-of-event-to-receive.md)、 [接收事件通知](receiving-event-notifications.md)和 [WQL (適用于 WMI 的 SQL) ](wql-sql-for-wmi.md)。

[**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md)的預設呼叫會使用半同步通訊。 *Iflags* 參數預設會設定 **wbemFlagForwardOnly** 和 **wbemFlagReturnImmediately** 旗標。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

下列程式描述如何使用 VBScript 接收半同步事件通知。

**在 VBScript 中接收半同步事件通知**

1.  針對您想要接收的事件種類建立查詢。 如需詳細資訊，請參閱 [決定要接收的事件種類](determining-the-type-of-event-to-receive.md)。

2.  如果您要求事件的實例類型（例如 [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)），請在查詢中指出目標實例的類型，例如 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)。

3.  如有必要，請在要求特定命名空間的未來 [**\_ \_ NamespaceModificationEvent**](--namespacemodificationevent.md)實例時，指定實例，例如命名空間的名稱。

4.  指定查詢中 Windows Management Instrumentation (WMI) 的輪詢間隔，例如「在10內」），以每隔10秒輪詢一次。 如需詳細資訊，請參閱 [內部子句](within-clause.md)。

5.  使用查詢呼叫 [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) 。

6.  對您收到的集合執行迴圈。

下列範例顯示如何從本機電腦上的磁片磁碟機，監視磁片的插入和移除。 腳本會要求 \_ 磁片磁碟機 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)實例的 [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md)實例，並每隔10秒輪詢新的實例。 此腳本是暫時性事件取用者的範例，並會繼續執行，直到工作管理員中停止或系統重新開機為止。 如需詳細資訊，請參閱 [在您的應用程式期間接收事件](receiving-events-for-the-duration-of-your-application.md)。


```VB
Const FLOPPY_DISK = 2
Set colMonitoredDisks = GetObject("Winmgmts:").ExecNotificationQuery _
    ("Select * from __InstanceModificationEvent within 10 WHERE " _
        & "TargetInstance ISA 'Win32_LogicalDisk'")
i = 0
Do While i = 0
    Set strDiskChange = colMonitoredDisks.NextEvent
    If strDiskChange.TargetInstance.DriveType = FLOPPY_DISK Then
        If strDiskChange.TargetInstance.Size > 0 Then
            Wscript.Echo "A disk has been inserted" & _
                " into the floppy drive."
    Else
            Wscript.Echo "A disk has been removed" & _
                " from the floppy drive."
        End If
    End If
Loop
```



下列程式說明如何使用 c + + 接收半同步事件通知。

**若要在 c + + 中接收半同步事件通知**

1.  使用 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) 和 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) 函數的呼叫來設定應用程式。

    由於 WMI 是以 COM 為基礎，因此呼叫 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) 和 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) 是 wmi 應用程式的必要步驟。 如需詳細資訊，請參閱 [建立 WMI 應用程式或腳本](creating-a-wmi-application-or-script.md)。

2.  判斷您想要接收的事件種類。

    WMI 支援內部和外來事件。 內建事件是 WMI 預先定義的事件。 外建事件是由協力廠商提供者所定義的事件。 如需詳細資訊，請參閱 [決定要接收的事件種類](determining-the-type-of-event-to-receive.md)。

3.  註冊，以透過呼叫 [**IWbemServices：： ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) 方法來接收特定類別的事件。

    讓每個查詢都非常明確。 註冊的目標是要只接收所需的通知。 不需要浪費處理和傳遞時間的通知。

    您可以設計事件取用者來接收多個事件。 例如，取用者可能需要針對特定類別的裝置和安全性違規事件的實例修改事件通知。 在此情況下，取用者在接收實例修改事件時所執行的工作，對兩個事件都是不同的。 因此，取用者應該呼叫 [**IWbemServices：： ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) 來註冊實例修改事件，以及對 **ExecNotificationQuery** 進行另一次呼叫，以註冊安全性違規事件。

    在 [**ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery)的呼叫中，將 *lFlags* 參數設定為 **WBEM \_ 旗 \_ \_** 標會立即傳回，而 **WBEM 旗標 \_ \_ \_ 只** 會順向。 **Wbem 旗標會 \_ \_ \_ 立即** 傳回旗標要求的最半處理，而 **wbem 旗標 \_ \_ \_ 僅向前** 旗標會要求順向列舉值。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。 **ExecNotificationQuery** 函式會傳回 [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)介面的指標。

4.  對 [**IEnumWbemClassObject：： Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) 方法進行重複呼叫，以輪詢已註冊的事件通知。
5.  完成時，請釋放指向 [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) 物件的列舉值。

    您可以釋放與註冊相關聯的 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 指標。 釋放 **IWbemServices** 指標會導致 WMI 停止將事件傳遞給所有相關聯的暫時取用者。

 

 

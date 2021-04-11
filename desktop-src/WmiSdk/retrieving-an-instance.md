---
description: 抓取實例是您可能會在 WMI 中執行的其中一個最常見的抓取程式。
ms.assetid: c3258783-ffcd-4c40-aaf2-7c65617cf9f8
ms.tgt_platform: multiple
title: 正在抓取 WMI 實例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdacf5fe5c86618eb84d70a5505897a94a7ace2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027482"
---
# <a name="retrieving-a-wmi-instance"></a>正在抓取 WMI 實例

抓取實例是您可能會在 WMI 中執行的其中一個最常見的抓取程式。 您可以取出現有的實例，或建立新的未命名實例。 現有實例的 WMI 路徑是必要參數。 如需詳細資訊，請參閱 [描述 WMI 物件的位置](describing-the-location-of-a-wmi-object.md)。

> [!Note]  
> 提供實例時，提供者可能無法提供特定屬性的值。 除非在屬性描述中另有說明，否則您無法從空白值推斷任何意義。 這不會與具有 **Null** 值的字串混淆。 在此情況下，會填入值。 它是空的，但具有值： **Null**。

 

使用 PowerShell [>get-wmiobject 指令程式](https://technet.microsoft.com/library/dd315379.aspx) 的呼叫來取出實例的本機複本。

**使用 PowerShell 取出 WMI 類別的實例**

-   您可以使用 *-class* 和 *-filter* 參數來取得特定的實例。

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM Win32_logicalDisk WHERE DeviceID = 'C:'"
    ```

    

您可以使用 c # 來取得 WMI 實例，方法是使用 [CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))建立搜尋物件，然後將相關的索引鍵值填入，然後使用 [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)) 呼叫來搜尋該物件。

**若要使用 c # (的) 取得 WMI 類別的實例。基礎結構**

1.  使用 [Microsoft. 基礎結構](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) 命名空間，建立具有相關類別名稱和命名空間的新 [CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85)) 物件。

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "Win32_LogicalDisk";

    CimInstance myDrive = new CimInstance(className, Namespace);
    ```

    

2.  建立包含您要搜尋之實例之索引鍵屬性名稱和值的 [CimProperty](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832461(v=vs.85)) ，並將該屬性加入至您的類別物件。

    ```CSharp
    myDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));
    ```

    

3.  使用 [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)) ，從 WMI 取出物件。

    ```CSharp
    CimSession mySession = CimSession.Create("localhost");
    CimInstance searchInstance = mySession.GetInstance(Namespace, myDrive);
    ```

    

您可以使用 [system.servicemodel 命名空間中的類別](/dotnet/api/system.management) ，來取得特定 wmi 類別實例或 wmi 類別實例的集合。

> [!Note]  
> **系統管理** 是用來存取 WMI 的原始 .net 命名空間;不過，這個命名空間中的 Api 通常會較慢，而且也不會相對於其較新式的 **Microsoft 管理元件** 對應專案。

 

**使用 c # (System. Management) 來取出 WMI 類別的實例**

1.  藉由建立新的 [system.management.managementobject](/dotnet/api/system.management.managementobject)，並透過 *ManagementPath* 參數傳入的名稱和特定實例值，來取出特定實例的本機複本。 然後，您可以明確呼叫 [system.management.managementobject](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get)來取得實例資料。

    ```CSharp
    using System.Management;
    ...
    ManagementObject objInst = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    objInst.Get();
    ```

    

2.  或者，您也可以使用 [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher)搜尋 WMI 類別的所有實例，然後再列舉傳回的 [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection)。

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher("SELECT * FROM Win32_LogicalDisk");
    ManagementObjectCollection colDisks = mgmtObjSearcher.Get();

    foreach (ManagementObject objDisk in colDisks)
    {
       Console.WriteLine("Device ID : {0}", objDisk["DeviceID"]);
    }

    Console.ReadLine();
    ```

    

    您可以藉由存取實例，以隱含方式呼叫 **Get** 方法。 如需詳細資訊，請參閱 [取出 WMI 實例的一部分](retrieving-part-of-an-instance.md)。

使用 VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) 方法的呼叫來取出實例的本機複本。

**使用 VBScript 取出 WMI 類別的實例**

-   使用實例的物件路徑來呼叫 [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) ，如下列範例所示。

    ```VB
    Set objinst = GetObject("WinMgmts:Win32_LogicalDisk='C:'")
    ```

    

    若要抓取特定的實例，您必須提供名稱做為物件路徑的一部分。

在 c + + 中，呼叫 [**IWbemServices：： GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)。

**使用 c + + 取出 WMI 類別的實例**

-   藉由呼叫 [**IWbemServices：： GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) 或 [**Iwbemservices：： GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)，取出實例的本機複本。 必須包含物件的 WMI 路徑。

    顧名思義， [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) 會以非同步方式抓取實例，而 [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) 會以同步方式抓取實例。 如果您想要使用非同步抓取，則必須執行 [**IWbemObjectSink**](iwbemobjectsink.md) 介面。

## <a name="examples"></a>範例

如需使用做為範本的 VBScript 範例來取出類別和實例資訊，請參閱 TechNet 資源庫上的 [WMI 範本腳本](https://Gallery.TechNet.Microsoft.Com/aded1ef3-d2af-4821-8a92-b5c22ca2ecd8) 範例。 這個特定的範例會使用 GetObject 來取得 WMI 服務。

 

 

---
description: 列舉是指移動一組物件，並且可能會在執行此動作時修改每個物件的動作。
ms.assetid: fe7e3259-9a7c-4f73-af30-192bbbace1b3
ms.tgt_platform: multiple
title: 列舉 WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d94f4a1fcff06423bad9d2bf5570ec1b9705fdef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969309"
---
# <a name="enumerating-wmi"></a>列舉 WMI

列舉是指移動一組物件，並且可能會在執行此動作時修改每個物件的動作。 例如，您可以列舉一組 [**Win32 \_ DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive) 物件來尋找特定的序號。 請注意，雖然您可以列舉任何物件，但 WMI 只會傳回您具有安全性存取權的物件。

大型資料集的列舉可能需要大量的資源，並降低效能。 如需詳細資訊，請參閱 [改善列舉效能](improving-enumeration-performance.md)。 您也可以使用更特定的查詢來要求資料。 如需詳細資訊，請參閱 [查詢 WMI](querying-wmi.md)。

本主題將討論下列各節：

-   [使用 PowerShell 列舉 WMI](#enumerating-wmi-using-powershell)
-   [使用 c # (Microsoft 管理) 列舉 WMI ](#enumerating-wmi-using-c-microsoftmanagementinfrastructure)
-   [使用 c # (System. Management) 來列舉 WMI ](#enumerating-wmi-using-c-systemmanagement)
-   [使用 VBScript 列舉 WMI](#enumerating-wmi-using-vbscript)
-   [使用 c + + 列舉 WMI](#enumerating-wmi-using-c-microsoftmanagementinfrastructure)

## <a name="enumerating-wmi-using-powershell"></a>使用 PowerShell 列舉 WMI

如果您不知道特定實例的物件路徑，或想要取得特定類別的所有實例，請使用 [>get-wmiobject](https://technet.microsoft.com/library/dd315379.aspx)，並在 *-class* 參數中使用類別的名稱。 如果您想要使用查詢，可以使用 *-query* 參數。

下列程式描述如何使用 PowerShell 列舉類別的實例。

**使用 PowerShell 列舉類別的實例**

1.  使用 [>get-wmiobject](https://technet.microsoft.com/library/dd315379.aspx) Cmdlet 的呼叫來列舉實例。

    [>get-wmiobject](https://technet.microsoft.com/library/dd315379.aspx) 會傳回一或多個 WMI 物件的集合，您可以透過這些物件來列舉。 如需詳細資訊，請參閱 [存取集合](accessing-a-collection.md)。

    如果您想要在另一個命名空間或不同的電腦上取出 WMI 類別實例，請分別在 *-computer* 和 *-namespace* 參數中指定電腦和命名空間。 如需詳細資訊，請參閱 [建立 WMI 腳本](creating-a-wmi-script.md)。 只有當您有適當的存取權限時，才適用此功能。 如需詳細資訊，請參閱 [維護 WMI 安全性](maintaining-wmi-security.md) 和執行具特殊 [許可權的作業](executing-privileged-operations.md)。

2.  使用集合的成員抓取任何您想要的個別實例。

下列程式碼範例會抓取 PowerShell 集合，然後顯示本機電腦上所有邏輯磁碟機實例的大小屬性。


```PowerShell
$objCol = get-wmiobject -class "Win32_LogicalDisk"

# Or, alternately
#$objCol = get-wmiobject -Query "SELECT * FROM Win32_LogicalDisk"

foreach ($Drive in $objCol)
{
    if ($Drive.size -ne $null)
    { "Drive " + $Drive.deviceID + " contains " + $Drive.size + " bytes" }
    else
    { "Drive " + $Drive.deviceID + " is not available." }
}
```



## <a name="enumerating-wmi-using-c-microsoftmanagementinfrastructure"></a>使用 c # (Microsoft 管理) 列舉 WMI

1.  新增參考至 **Microsoft. 管理基礎結構** 參考元件。  (此元件隨附于 [Windows 8 Windows 軟體開發套件 (SDK) ](https://msdn.microsoft.com/library/windows/desktop/hh852363.aspx)的一部分。 ) 
2.  針對 **Microsoft. 基礎結構** 命名空間加入 **using** 語句。

```CSharp
    using Microsoft.Management.Infrastructure;
```

    

3.  具現化 [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) 物件。 下列程式碼片段會使用 [**CimSession. Create**](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)) 方法的標準 "localhost" 值。

```CSharp
    CimSession cimSession = CimSession.Create("localhost");
```

    

4.  呼叫 [**CimSession QueryInstances**](https://www.bing.com/search?q=**CimSession.QueryInstances**) 方法，傳遞所需的 CIM 命名空間和 WQL 來使用。 下列程式碼片段會傳回兩個實例，代表兩個標準 Windows 進程，其中 handle 屬性 (代表處理序識別碼，或 PID) 的值為0或4。

```CSharp
    IEnumerable<CimInstance> queryInstances =     
      cimSession.QueryInstances(@"root\cimv2", 
                                "WQL", 
                                @"select name from win32_process where handle = 0 or handle = 4");
```

    

5.  對傳回的 [**CimInstance**](https://www.bing.com/search?q=**CimInstance**) 物件執行迴圈。

```CSharp
    foreach (CimInstance cimInstance in enumeratedInstances)
    { 
      Console.WriteLine("Process name: {0}", cimInstance.CimInstanceProperties["Name"].Value);  
    }
```

    

下列程式碼範例會列舉 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process) 類別的所有實例， (代表本機電腦上) 的使用中進程，並列印每個進程的名稱。

> [!Note]  
> 在實際的應用程式中，您會將電腦名稱稱 ( "localhost" ) 和 CIM 命名空間 ( "root cimv2" ) 的參數定義為參數 \\ 。 為了簡單起見，在此範例中，這些都已硬式編碼。

 


```CSharp
using System;
using System.Collections.Generic;
using Microsoft.Management.Infrastructure;

public partial class MI
{
    static void PrintCimInstance(CimInstance cimInstance)
    {
        Console.ForegroundColor = ConsoleColor.Blue;
        Console.WriteLine("{0} properties", cimInstance.CimSystemProperties.ClassName);
        Console.ResetColor();

        Console.WriteLine(String.Format("{0,-5}{1,-30}{2,-15}{3,-10}", 
                                        "Key?", "Property", "Type", "Value"));

        foreach (var enumeratedProperty in cimInstance.CimInstanceProperties)
        {
            bool isKey = ((enumeratedProperty.Flags & CimFlags.Key) == CimFlags.Key);

            if (enumeratedProperty.Value != null)
            {
                Console.WriteLine(
                    "{0,-5}{1,-30}{2,-15}{3,-10}",
                    isKey == true ? "Y" : string.Empty,
                    enumeratedProperty.Name,
                    enumeratedProperty.CimType,
                    enumeratedProperty.Value);
            }
        }
        Console.WriteLine();
    }

    public static void QueryInstance(string query)
    {
        try
        {
            CimSession cimSession = CimSession.Create("localhost");

            IEnumerable<CimInstance> queryInstances = 
              cimSession.QueryInstances(@"root\cimv2", "WQL", query);
            foreach (CimInstance cimInstance in queryInstances)
            {
                //Use the current instance. This example prints the instance. 
                PrintCimInstance(cimInstance);
            }
        }
         catch (CimException ex) 
        { 
            // Handle the exception as appropriate.
            // This example prints the message.
            Console.WriteLine(ex.Message); 
        }
    }
}
```


```CSharp

using System;

namespace MIClientManaged
{
    class Program
    {
        static void Main(string[] args)
        {
            while (true)
            {
                Console.Write(&quot;Enter WQL (x = Quit): &quot;);
                string query = Console.ReadLine().ToUpper();
                if (query.CompareTo(&quot;X&quot;) == 0) break;
                MI.QueryInstance(query);
            }
        }
    }
}
```





## <a name="enumerating-wmi-using-c-systemmanagement"></a>使用 c # (System. Management) 來列舉 WMI

如果您不知道特定實例的物件路徑，或您想要取出特定類別的所有實例，請使用 [ManagementClass](/dotnet/api/system.management.managementclass) 物件來取出 [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) ，其中包含 WMI 命名空間中指定類別的所有實例。 或者，您也可以透過 [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher) 來查詢 WMI，以取得相同的物件集合。

> [!Note]  
> **系統管理** 是用來存取 WMI 的原始 .net 命名空間;不過，這個命名空間中的 Api 通常會較慢，而且也不會相對於其較新式的 **Microsoft 管理元件** 對應專案。

 

下列程式說明如何使用 c # 列舉類別的實例。

**使用 C 列舉類別的實例#**

1.  使用 [ManagementClass. GetInstances](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances)的呼叫來列舉實例。

    [GetInstances](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances)方法會傳回可供您列舉的物件集合（或集合）。 如需詳細資訊，請參閱 [存取集合](accessing-a-collection.md)。 傳回的集合實際上是 [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) 物件，因此可以呼叫該物件的任何方法。

    如果您想要在另一個命名空間或不同的電腦上取出 WMI 類別實例，請在 *path* 參數中指定電腦和命名空間。 如需詳細資訊，請參閱 [建立 WMI 腳本](creating-a-wmi-script.md)。 只有當您有適當的存取權限時，才適用此功能。 如需詳細資訊，請參閱 [維護 WMI 安全性](maintaining-wmi-security.md) 和執行具特殊 [許可權的作業](executing-privileged-operations.md)。

2.  使用集合的成員抓取任何您想要的個別實例。

下列程式碼範例會抓取 c # 集合，然後顯示本機電腦上所有邏輯磁碟機實例的 size 屬性。


```PowerShell
using System.Management;
...

ManagementClass mc = new ManagementClass("Win32_LogicalDisk");
ManagementObjectCollection objCol = mc.GetInstances();

//or, alternately
//ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher("SELECT * FROM Win32_LogicalDisk");
//ManagementObjectCollection objCol = mgmtObjSearcher.Get();

if (objCol.Count != 0)
{
   foreach (ManagementObject Drive in objCol)
   {
      if (Drive["size"] != null)
      {
         Console.WriteLine("Drive {0} contains {1} bytes.", Drive["deviceID"], Drive["size"]);
      }
      else
      {
         Console.WriteLine("Drive {0} is not available.", Drive["deviceID"]);
      }
   }
}
Console.ReadLine();
```



## <a name="enumerating-wmi-using-vbscript"></a>使用 VBScript 列舉 WMI

如果您不知道特定實例的物件路徑，或想要取得特定類別的所有實例，請使用 [**SWbemServices. InstancesOf**](swbemservices-instancesof.md) 方法來傳回類別所有實例的 [**swbemobjectset 搭配使用**](swbemobjectset.md) 列舉。 或者，您也可以透過 [**SWbemServices.ExecQuery**](swbemservices-execquery.md) 來查詢 WMI，以取得相同的物件集。

下列程式描述如何使用 VBScript 列舉類別的實例。

**使用 VBScript 列舉類別的實例**

1.  使用 [**SWbemServices. InstancesOf**](swbemservices-instancesof.md) 方法的呼叫來列舉實例。

    [**InstancesOf**](swbemservices-instancesof.md)方法會傳回可供您列舉的物件集合（或集合）。 如需詳細資訊，請參閱 [存取集合](accessing-a-collection.md)。 傳回的集合實際上是 [**swbemobjectset 搭配使用**](swbemobjectset.md) 物件，因此可以呼叫該物件的任何方法。

    如果您想要在另一個命名空間或不同的電腦上取出 WMI 類別實例，請在 [標記] 中指定電腦和命名空間。 如需詳細資訊，請參閱 [建立 WMI 腳本](creating-a-wmi-script.md)。 只有當您有適當的存取權限時，才適用此功能。 如需詳細資訊，請參閱 [維護 WMI 安全性](maintaining-wmi-security.md) 和執行具特殊 [許可權的作業](executing-privileged-operations.md)。

2.  使用集合方法抓取您想要的任何個別實例。

下列程式碼範例會抓取 [**SWbemServices**](swbemservices.md) 物件，然後執行 [**InstancesOf**](swbemservices-instancesof.md) 方法，以顯示本機電腦上所有邏輯磁碟機實例的大小屬性。


```VB
Set objCol = GetObject("WinMgmts:").InstancesOf("Win32_LogicalDisk")
For Each Drive In objCol
    If Not IsNull(Drive.Size) Then    
       WScript.Echo ("Drive " & Drive.deviceid & " contains " & Drive.Size & " bytes")
    Else
       WScript.Echo ("Drive " & Drive.deviceid & " is not available.")
    End If
Next
```



## <a name="enumerating-wmi-using-c"></a>使用 c + + 列舉 WMI

除了執行基本欄舉之外，您還可以設定數個旗標和屬性來提升列舉的效能。 如需詳細資訊，請參閱 [改善列舉效能](improving-enumeration-performance.md)。

**列舉 WMI 中的物件集**

1.  建立 [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) 介面，以描述您想要列舉的物件集合。

    [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)物件包含描述一組 WMI 物件的清單。 您可以使用 **IEnumWbemClassObject** 方法來列舉轉寄、略過物件、從開頭開始，以及複製列舉值。 下表列出用來針對不同類型的 WMI 物件建立枚舉器的方法。

    

    <table>
    <thead>
    <tr class="header">
    <th>Object</th>
    <th>方法</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>類別</td>
    <td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum"><strong>IWbemServices：： CreateClassEnum</strong></a><br />
[<strong>IWbemServices：： CreateClassEnumAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) <br />
    </dl></td>
    </tr>
    <tr class="even">
    <td>執行個體</td>
    <td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum"><strong>IWbemServices：： CreateInstanceEnum</strong></a><br />
[<strong>IWbemServices：： CreateInstanceEnumAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) <br />
    </dl></td>
    </tr>
    <tr class="odd">
    <td>查詢結果</td>
    <td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery"><strong>IWbemServices：： ExecQuery</strong></a><br />
[<strong>IWbemServices：： ExecQueryAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) <br />
    </dl></td>
    </tr>
    <tr class="even">
    <td>事件通知</td>
    <td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery"><strong>IWbemServices：： ExecNotificationQuery</strong></a><br />
[<strong>IWbemServices：： ExecNotificationQueryAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) <br />
    </dl></td>
    </tr>
    </tbody>
    </table>

    

     

2.  使用多個對 [**IEnumWbemClassObject：： Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) 或 [**IEnumWbemClassObject：： NextAsync**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync)的呼叫，以遍歷傳回的列舉。

如需詳細資訊，請參閱 [操作類別和實例資訊](manipulating-class-and-instance-information.md)。

 

 

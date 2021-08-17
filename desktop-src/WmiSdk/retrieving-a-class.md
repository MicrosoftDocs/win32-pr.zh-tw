---
description: 您可以取出的第一種物件是 WMI 類別。
ms.assetid: cfe4bcca-692e-45cd-a840-93ebfe4ae267
ms.tgt_platform: multiple
title: 正在抓取 WMI 類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e2695a934436e6e53fe84ee11c6008615b3d6f5d1807039d76b72fa704a2cf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739877"
---
# <a name="retrieving-a-wmi-class"></a>正在抓取 WMI 類別

您可以取出的第一種物件是 WMI 類別。 在抓取 WMI 類別時，您實際上會取出類別定義，也就是完整描述類別的屬性、限定詞和方法的清單。 不過，類別定義基本上是類別本身。

PowerShell 會使用標準查詢來取出類別定義，並使用 **中繼 \_ 類別** 類別。

**若要在 PowerShell 中取出類別定義**

-   搭配使用 [>get-wmiobject](https://technet.microsoft.com/library/dd315379.aspx) 與 **中繼 \_ 類別** 的查詢，並使用 WHERE 子句，其中包含您要取出的類別名稱。

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'"
    ```

    

    [>Get-wmiobject](https://technet.microsoft.com/library/dd315379.aspx) 是標準 Cmdlet，可讓 PowerShell 用來從 WMI 取出類別和實例資訊。 **中繼 \_ 類別** 類別會將查詢定義為架構查詢。 若沒有 **中繼 \_ 類別** 類別，此查詢會傳回 Win32 LogicalDisk 的所有實例 \_ 。 如需查詢 WMI 的詳細資訊，請參閱 [架構查詢的 SELECT 語句](select-statement-for-schema-queries.md)。

在 c # 中取得 WMI 定義的目前進程是使用 **CIMInstance** 類別。

**若要在 c # 中取出類別定義 (Microsoft. 管理. 基礎結構)**

1.  使用 CIMInstance 類別，以指定的 **命名空間和** 類別名稱建立一個類別。

    建立的類別將會包含所有類別資訊，但不包含實例資料。

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "Win32_LogicalDisk";

    CimInstance diskDrive = new CimInstance(className, Namespace);
    ```

    

2.  或者，如同使用 PowerShell，您也可以使用 **中繼 \_ 類別** 標記作為查詢的一部分來執行查詢。

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string diskDriveQuery = "SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'";

    CimSession mySession = CimSession.Create("localhost");
    IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", diskDriveQuery);
    ```

    

如同 PowerShell，c # 會使用 **中繼 \_ 類別** 查詢來取出類別定義。 或者，您也可以建立 **ManagementClass** 物件來直接存取類別定義。

> [!Note]  
> **系統管理** 是用來存取 WMI 的原始 .net 命名空間;不過，這個命名空間中的 Api 通常會較慢，而且也不會相對於其較新式的 **Microsoft 管理元件** 對應專案。

 

**若要在 c # 中取出類別定義 (System. Management)**

1.  您可以搭配使用 [ManagementObjectSerarcher](/dotnet/api/system.management.managementobjectsearcher) 與 **中繼 \_ 類別** 的查詢，其中 WHERE 子句包含您要取出的類別名稱。

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher searcher = new ManagementObjectSearcher("SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'");
    ManagementObjectCollection myDiskCollection = searcher.Get();
    ```

    

    [ManagementObjectSerarcher](/dotnet/api/system.management.managementobjectsearcher) 是 .net 的標準類別，用來從 WMI 取出類別和實例資訊。 [ManagementObjectSerarcher： Get](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get) 會傳回包含架構定義類別的 [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) 。 **中繼 \_ 類別** 類別會將查詢定義為架構查詢。 若沒有 **中繼 \_ 類別** 類別，此查詢會傳回 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)的所有實例。 如需查詢 WMI 的詳細資訊，請參閱 [架構查詢的 SELECT 語句](select-statement-for-schema-queries.md)。

2.  或者，使用名稱做為路徑來建立新的 [ManagementClass](/dotnet/api/system.management.managementclass) 物件，以取出類別。

    ```CSharp
    using System.Management;
    ...
    ManagementClass objInst = new ManagementClass("Win32_LogicalDisk");
    ```

    

您可以使用類似的方式，在 VBScript 中取出類別定義，以抓取特定的實例。

**若要在 VBScript 中取出類別定義**

1.  呼叫 [**SWbemServices**](swbemservices-get.md) ，但不識別類別的物件路徑中的特定實例。
2.  下列程式碼範例會抓取描述電腦上邏輯磁碟機之類別的類別定義。

    ```VB
    Set objinst = GetObject("WinMgmts:Win32_LogicalDisk")
    ```

    

    Windows (WSH 的腳本主機) 也支援下列各項。

    ```VB
    <OBJECT id="myLocator" progid="WbemScripting.SWbemLocator"></OBJECT>
    ```

    

    在 [Active Server Pages (ASP) 在伺服器端腳本中使用 [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) 或 [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) 。 如需詳細資訊，請參閱 [建立 WMI 的 Active Server Pages （WMI](creating-active-server-pages-for-wmi.md)）。

3.  也可以指定類別或實例，在此情況下，傳回的物件是 WMI 物件，例如 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)的實例，而不是服務物件。 請注意，您不能使用 VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) 函數來建立泛型物件 [**SWbemObject**](swbemobject.md)的實例。
4.  在 Microsoft Internet Explorer (IE) 的 HTML 網頁中， [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx)和 [CreateObject](/previous-versions//xzysf6hc(v=vs.85))可能會失敗，因為 WMI 腳本物件（例如 ActiveX 控制項）未標示為安全的腳本。 其中一個例外狀況是 [**SWbemDateTime**](swbemdatetime.md) 物件。 這些呼叫的唯一方法就是當您降低 IE 安全性設定時（不建議這麼做）。

在 c + + 中取出類別時，請呼叫 [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)的 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)版本。

**若要在 c + + 中取出類別定義**

1.  呼叫 [**IWbemServices：： GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) 或 [**IWbemServices：： GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) 方法，以取出類別的定義。
2.  一個類別可以有多個類別定義，通常會在您將一個以上的類別提供者載入一個命名空間時進行。 當某個類別有多個類別定義時，WMI 會傳回探索到的第一個定義和 **WBEM \_ S \_ 重複的 \_ 物件** 狀態碼。

因為 [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) 會傳回類別定義，所以通常是用來做為建立實例的第一個步驟。 如需如何使用 **GetObject** 的詳細資訊，請參閱 [使用 c + + 建立和宣告實例](creating-and-declaring-an-instance-using-c-.md)。

 

 

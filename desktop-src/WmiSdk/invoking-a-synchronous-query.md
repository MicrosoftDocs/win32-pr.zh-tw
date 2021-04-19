---
description: 同步查詢是一項查詢，可在查詢期間維持對您應用程式進程的控制權。
ms.assetid: 628e9a31-7b0d-4099-bfa5-56330bb4eb6b
ms.tgt_platform: multiple
title: 叫用同步查詢
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d4bb2ff61a1c94bf7390a65d51e773ad943a45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996994"
---
# <a name="invoking-a-synchronous-query"></a>叫用同步查詢

同步查詢是一項查詢，可在查詢期間維持對您應用程式進程的控制權。 同步查詢需要單一介面呼叫，因此比非同步呼叫更簡單。 不過，同步查詢有可能會鎖定您的應用程式，以便在網路上進行大型查詢或查詢。

下列程式描述如何使用 PowerShell 發出同步資料查詢。

**若要在 PowerShell 中發出同步資料查詢**

-   使用 WMI [>get-wmiobject](https://technet.microsoft.com/library/dd315379.aspx) 指令程式和 *-query* 參數來描述您的 wmi 查詢。 此 Cmdlet 會傳回單一物件或物件的集合，視查詢符合的物件數目而定。

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM Win32_logicalDisk WHERE DeviceID = 'C:'"
    ```

    

下列程式說明如何使用 c # 來發出同步資料查詢。

**若要在 c # 中發出同步資料查詢 (Microsoft. 管理. 基礎結構)**

1.  使用 CimSession 來描述您的 WMI 查詢。 這個方法會傳回 CimInstance 物件的集合。

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string diskDriveQuery = "SELECT * FROM Win32_LogicalDisk";
    CimSession mySession = CimSession.Create("localhost");
    IEnumerable<CimInstance> queryInstances = mySession.QueryInstances(Namespace, "WQL", diskDriveQuery);
    ```

    

2.  使用標準 c # 語言收集技術來存取每個傳回的物件。

    ```CSharp
    foreach (CimInstance drive in queryInstances)
    {
       Console.WriteLine(drive.CimInstanceProperties["DeviceID"]);
    }
    ```

    

下列程式說明如何使用 c # 來發出同步資料查詢。

**若要在 c # 中發出同步資料查詢 (System. Management)**

1.  使用 [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher) 物件來建立查詢，並透過呼叫 [ManagementObjectSearcher 取得](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get)資訊。

    這個方法會傳回 [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) 物件。

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher("SELECT * FROM Win32_LogicalDisk");
    ManagementObjectCollection objCol = mgmtObjSearcher.Get();
    ```

    

2.  使用標準 c # 語言收集技術來存取每個傳回的物件。

    ```CSharp
    foreach (ManagementObject drive in objCol)
    {
       Console.WriteLine(drive["DeviceID"]);
    }
    ```

    

下列程式描述如何使用 VBScript 發出同步資料查詢。

**若要在 VBScript 中發出同步資料查詢**

1.  使用 [**SWbemServices.ExecQuery**](swbemservices-execquery.md)描述您的 WMI 查詢。 這個方法會傳回 [**swbemobjectset 搭配使用**](swbemobjectset.md)。

    ```VB
    GetObject("winmgmts:").ExecQuery _
            ("Select * from Win32_Service where State='Stopped'")
    ```

    

2.  使用標準指令碼語言 [收集](accessing-a-collection.md) 技術來存取每個傳回的物件。

    ```VB
    for each Service in _ 
        GetObject("winmgmts:").ExecQuery _
            ("Select * from Win32_Service where State='Stopped'")
        WScript.Echo "  "& Service.DisplayName & " [", Service.Name, "]"
    next
    ```

    

下列程式描述如何使用 c + + 發出同步資料查詢。

**若要在 c + + 中發出同步查詢**

1.  透過呼叫 [**IWbemServices：： ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)來描述對 WMI 的查詢。

    [**ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)方法會採用 WQL 搜尋字串做為描述查詢的參數。 WMI 會執行查詢，並傳回 [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) 介面指標。 透過 **IEnumWbemClassObject** 介面，您可以存取組成結果集的類別或實例。

2.  收到查詢之後，您可以呼叫 [**IEnumWbemClassObject：： Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next)來列舉查詢。 如需詳細資訊，請參閱 [列舉 WMI](enumerating-wmi.md)。

    下列程式碼範例需要下列參考和 \# include 語句才能正確編譯。

    ```C++
    #include <wbemidl.h>
    #include <iostream>
    using namespace std;
    ```

    

    下列程式碼範例描述如何查詢代表 WMI 中使用者和群組的物件。

    ```C++
    void ExecQuerySync(IWbemServices *pSvc)
    {
        // Query for all users and groups.

        BSTR Language = SysAllocString(L"WQL");
        BSTR Query = SysAllocString(L"SELECT * FROM __Namespace");

        // Initialize the IEnumWbemClassObject pointer.
        IEnumWbemClassObject *pEnum = 0;

        // Issue the query.
        HRESULT hRes = pSvc->ExecQuery(
            Language,
            Query,
            WBEM_FLAG_FORWARD_ONLY,         // Flags
            0,                              // Context
            &pEnum
            );

        SysFreeString(Query);
        SysFreeString(Language);

        if (hRes != 0)
        {
            printf("Error\n");
            return;
        }
        
        ULONG uTotal = 0;

        // Retrieve the objects in the result set.
        for (;;)
        {
            IWbemClassObject *pObj = 0;
            ULONG uReturned = 0;

            hRes = pEnum->Next(
                0,                  // Time out
                1,                  // One object
                &pObj,
                &uReturned
                );

            uTotal += uReturned;

            if (uReturned == 0)
                break;

            // Use the object.
            
            // ...
            
            // Release it.
            // ===========
            
            pObj->Release();    // Release objects not owned.            
        }

        // All done.
        pEnum->Release();
    }
    ```

    

 

 

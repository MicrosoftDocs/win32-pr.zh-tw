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
# <a name="invoking-a-synchronous-query"></a><span data-ttu-id="c91c3-103">叫用同步查詢</span><span class="sxs-lookup"><span data-stu-id="c91c3-103">Invoking a Synchronous Query</span></span>

<span data-ttu-id="c91c3-104">同步查詢是一項查詢，可在查詢期間維持對您應用程式進程的控制權。</span><span class="sxs-lookup"><span data-stu-id="c91c3-104">A synchronous query is a query that maintains control over the process of your application for the duration of the query.</span></span> <span data-ttu-id="c91c3-105">同步查詢需要單一介面呼叫，因此比非同步呼叫更簡單。</span><span class="sxs-lookup"><span data-stu-id="c91c3-105">A synchronous query requires a single interface call, and is therefore more simple than an asynchronous call.</span></span> <span data-ttu-id="c91c3-106">不過，同步查詢有可能會鎖定您的應用程式，以便在網路上進行大型查詢或查詢。</span><span class="sxs-lookup"><span data-stu-id="c91c3-106">However, a synchronous query has the potential of locking up your application for large queries or queries over a network.</span></span>

<span data-ttu-id="c91c3-107">下列程式描述如何使用 PowerShell 發出同步資料查詢。</span><span class="sxs-lookup"><span data-stu-id="c91c3-107">The following procedure describes how to issue a synchronous data query using PowerShell.</span></span>

<span data-ttu-id="c91c3-108">**若要在 PowerShell 中發出同步資料查詢**</span><span class="sxs-lookup"><span data-stu-id="c91c3-108">**To issue a synchronous data query in PowerShell**</span></span>

-   <span data-ttu-id="c91c3-109">使用 WMI [>get-wmiobject](https://technet.microsoft.com/library/dd315379.aspx) 指令程式和 *-query* 參數來描述您的 wmi 查詢。</span><span class="sxs-lookup"><span data-stu-id="c91c3-109">Describe your query to WMI using the WMI [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) cmdlet and the *-query* parameter.</span></span> <span data-ttu-id="c91c3-110">此 Cmdlet 會傳回單一物件或物件的集合，視查詢符合的物件數目而定。</span><span class="sxs-lookup"><span data-stu-id="c91c3-110">The cmdlet returns either a single object, or a collection of objects, depending on how many objects fit the query.</span></span>

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM Win32_logicalDisk WHERE DeviceID = 'C:'"
    ```

    

<span data-ttu-id="c91c3-111">下列程式說明如何使用 c # 來發出同步資料查詢。</span><span class="sxs-lookup"><span data-stu-id="c91c3-111">The following procedure describes how to issue a synchronous data query using C#.</span></span>

<span data-ttu-id="c91c3-112">**若要在 c # 中發出同步資料查詢 (Microsoft. 管理. 基礎結構)**</span><span class="sxs-lookup"><span data-stu-id="c91c3-112">**To issue a synchronous data query in C# (Microsoft.Management.Infrastructure)**</span></span>

1.  <span data-ttu-id="c91c3-113">使用 CimSession 來描述您的 WMI 查詢。</span><span class="sxs-lookup"><span data-stu-id="c91c3-113">Describe your query to WMI using CimSession.QueryInstances.</span></span> <span data-ttu-id="c91c3-114">這個方法會傳回 CimInstance 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="c91c3-114">This method returns a collection of CimInstance objects.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string diskDriveQuery = "SELECT * FROM Win32_LogicalDisk";
    CimSession mySession = CimSession.Create("localhost");
    IEnumerable<CimInstance> queryInstances = mySession.QueryInstances(Namespace, "WQL", diskDriveQuery);
    ```

    

2.  <span data-ttu-id="c91c3-115">使用標準 c # 語言收集技術來存取每個傳回的物件。</span><span class="sxs-lookup"><span data-stu-id="c91c3-115">Use standard C# language collection techniques to access each returned object.</span></span>

    ```CSharp
    foreach (CimInstance drive in queryInstances)
    {
       Console.WriteLine(drive.CimInstanceProperties["DeviceID"]);
    }
    ```

    

<span data-ttu-id="c91c3-116">下列程式說明如何使用 c # 來發出同步資料查詢。</span><span class="sxs-lookup"><span data-stu-id="c91c3-116">The following procedure describes how to issue a synchronous data query using C#.</span></span>

<span data-ttu-id="c91c3-117">**若要在 c # 中發出同步資料查詢 (System. Management)**</span><span class="sxs-lookup"><span data-stu-id="c91c3-117">**To issue a synchronous data query in C# (System.Management)**</span></span>

1.  <span data-ttu-id="c91c3-118">使用 [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher) 物件來建立查詢，並透過呼叫 [ManagementObjectSearcher 取得](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get)資訊。</span><span class="sxs-lookup"><span data-stu-id="c91c3-118">Create the query with a [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher) object, and retrieve the information with a call to [ManagementObjectSearcher.Get](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get).</span></span>

    <span data-ttu-id="c91c3-119">這個方法會傳回 [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) 物件。</span><span class="sxs-lookup"><span data-stu-id="c91c3-119">This method returns a [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) object.</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher("SELECT * FROM Win32_LogicalDisk");
    ManagementObjectCollection objCol = mgmtObjSearcher.Get();
    ```

    

2.  <span data-ttu-id="c91c3-120">使用標準 c # 語言收集技術來存取每個傳回的物件。</span><span class="sxs-lookup"><span data-stu-id="c91c3-120">Use standard C# language collection techniques to access each returned object.</span></span>

    ```CSharp
    foreach (ManagementObject drive in objCol)
    {
       Console.WriteLine(drive["DeviceID"]);
    }
    ```

    

<span data-ttu-id="c91c3-121">下列程式描述如何使用 VBScript 發出同步資料查詢。</span><span class="sxs-lookup"><span data-stu-id="c91c3-121">The following procedure describes how to issue a synchronous data query using VBScript.</span></span>

<span data-ttu-id="c91c3-122">**若要在 VBScript 中發出同步資料查詢**</span><span class="sxs-lookup"><span data-stu-id="c91c3-122">**To issue a synchronous data query in VBScript**</span></span>

1.  <span data-ttu-id="c91c3-123">使用 [**SWbemServices.ExecQuery**](swbemservices-execquery.md)描述您的 WMI 查詢。</span><span class="sxs-lookup"><span data-stu-id="c91c3-123">Describe your query to WMI using [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span> <span data-ttu-id="c91c3-124">這個方法會傳回 [**swbemobjectset 搭配使用**](swbemobjectset.md)。</span><span class="sxs-lookup"><span data-stu-id="c91c3-124">This method returns an [**SWbemObjectSet**](swbemobjectset.md).</span></span>

    ```VB
    GetObject("winmgmts:").ExecQuery _
            ("Select * from Win32_Service where State='Stopped'")
    ```

    

2.  <span data-ttu-id="c91c3-125">使用標準指令碼語言 [收集](accessing-a-collection.md) 技術來存取每個傳回的物件。</span><span class="sxs-lookup"><span data-stu-id="c91c3-125">Use standard scripting language [collection](accessing-a-collection.md) techniques to access each returned object.</span></span>

    ```VB
    for each Service in _ 
        GetObject("winmgmts:").ExecQuery _
            ("Select * from Win32_Service where State='Stopped'")
        WScript.Echo "  "& Service.DisplayName & " [", Service.Name, "]"
    next
    ```

    

<span data-ttu-id="c91c3-126">下列程式描述如何使用 c + + 發出同步資料查詢。</span><span class="sxs-lookup"><span data-stu-id="c91c3-126">The following procedure describes how to issue a synchronous data query using C++.</span></span>

<span data-ttu-id="c91c3-127">**若要在 c + + 中發出同步查詢**</span><span class="sxs-lookup"><span data-stu-id="c91c3-127">**To issue a synchronous query in C++**</span></span>

1.  <span data-ttu-id="c91c3-128">透過呼叫 [**IWbemServices：： ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)來描述對 WMI 的查詢。</span><span class="sxs-lookup"><span data-stu-id="c91c3-128">Describe your query to WMI through a call to [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery).</span></span>

    <span data-ttu-id="c91c3-129">[**ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)方法會採用 WQL 搜尋字串做為描述查詢的參數。</span><span class="sxs-lookup"><span data-stu-id="c91c3-129">The [**ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) method takes a WQL search string as a parameter that describes your query.</span></span> <span data-ttu-id="c91c3-130">WMI 會執行查詢，並傳回 [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="c91c3-130">WMI performs the query and returns an [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) interface pointer.</span></span> <span data-ttu-id="c91c3-131">透過 **IEnumWbemClassObject** 介面，您可以存取組成結果集的類別或實例。</span><span class="sxs-lookup"><span data-stu-id="c91c3-131">Through the **IEnumWbemClassObject** interface, you can access the classes or instances that make up the result set.</span></span>

2.  <span data-ttu-id="c91c3-132">收到查詢之後，您可以呼叫 [**IEnumWbemClassObject：： Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next)來列舉查詢。</span><span class="sxs-lookup"><span data-stu-id="c91c3-132">After you receive your query, you can enumerate your query with a call to [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next).</span></span> <span data-ttu-id="c91c3-133">如需詳細資訊，請參閱 [列舉 WMI](enumerating-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="c91c3-133">For more information, see [Enumerating WMI](enumerating-wmi.md).</span></span>

    <span data-ttu-id="c91c3-134">下列程式碼範例需要下列參考和 \# include 語句才能正確編譯。</span><span class="sxs-lookup"><span data-stu-id="c91c3-134">The following code example requires the following references and \#include statements to compile correctly.</span></span>

    ```C++
    #include <wbemidl.h>
    #include <iostream>
    using namespace std;
    ```

    

    <span data-ttu-id="c91c3-135">下列程式碼範例描述如何查詢代表 WMI 中使用者和群組的物件。</span><span class="sxs-lookup"><span data-stu-id="c91c3-135">The following code example describes how to query for the objects that represent the users and groups in WMI.</span></span>

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

    

 

 

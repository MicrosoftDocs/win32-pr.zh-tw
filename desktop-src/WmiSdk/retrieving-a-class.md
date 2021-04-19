---
description: 您可以取出的第一種物件是 WMI 類別。
ms.assetid: cfe4bcca-692e-45cd-a840-93ebfe4ae267
ms.tgt_platform: multiple
title: 正在抓取 WMI 類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9378854eb483c6cdac7ddee47d581d8876270e97
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "106976407"
---
# <a name="retrieving-a-wmi-class"></a><span data-ttu-id="a2a9c-103">正在抓取 WMI 類別</span><span class="sxs-lookup"><span data-stu-id="a2a9c-103">Retrieving a WMI Class</span></span>

<span data-ttu-id="a2a9c-104">您可以取出的第一種物件是 WMI 類別。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-104">The first type of object you can retrieve is a WMI class.</span></span> <span data-ttu-id="a2a9c-105">在抓取 WMI 類別時，您實際上會取出類別定義，也就是完整描述類別的屬性、限定詞和方法的清單。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-105">When retrieving a WMI class, you actually retrieve a class definition, which is a listing of the properties, qualifiers, and methods that fully describe the class.</span></span> <span data-ttu-id="a2a9c-106">不過，類別定義基本上是類別本身。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-106">However, a class definition is basically the class itself.</span></span>

<span data-ttu-id="a2a9c-107">PowerShell 會使用標準查詢來取出類別定義，並使用 **中繼 \_ 類別** 類別。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-107">PowerShell uses a standard query to retrieve class definitions, using the **meta\_class** class.</span></span>

<span data-ttu-id="a2a9c-108">**若要在 PowerShell 中取出類別定義**</span><span class="sxs-lookup"><span data-stu-id="a2a9c-108">**To retrieve a class definition in PowerShell**</span></span>

-   <span data-ttu-id="a2a9c-109">搭配使用 [>get-wmiobject](https://technet.microsoft.com/library/dd315379.aspx) 與 **中繼 \_ 類別** 的查詢，並使用 WHERE 子句，其中包含您要取出的類別名稱。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-109">Use the [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) with a query to **meta\_class**, with the WHERE clause containing the name of the class you with to retrieve.</span></span>

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'"
    ```

    

    <span data-ttu-id="a2a9c-110">[>get-wmiobject](https://technet.microsoft.com/library/dd315379.aspx) 是標準 Cmdlet，可讓 PowerShell 用來從 WMI 取出類別和實例資訊。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-110">[Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) is the standard cmdlet PowerShell uses to retrieve class and instance information from WMI.</span></span> <span data-ttu-id="a2a9c-111">**中繼 \_ 類別** 類別會將查詢定義為架構查詢。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-111">The **meta\_class** class defines the query as a schema query.</span></span> <span data-ttu-id="a2a9c-112">若沒有 **中繼 \_ 類別** 類別，此查詢會傳回 Win32 LogicalDisk 的所有實例 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-112">Without the **meta\_class** class, this query would return all instances of Win32\_LogicalDisk.</span></span> <span data-ttu-id="a2a9c-113">如需查詢 WMI 的詳細資訊，請參閱 [架構查詢的 SELECT 語句](select-statement-for-schema-queries.md)。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-113">For more information about querying WMI, see [SELECT Statement for Schema Queries](select-statement-for-schema-queries.md).</span></span>

<span data-ttu-id="a2a9c-114">在 c # 中取得 WMI 定義的目前進程是使用 **CIMInstance** 類別。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-114">The current process for retrieving a WMI definition in C# is to use **CIMInstance** class.</span></span>

<span data-ttu-id="a2a9c-115">**若要在 c # 中取出類別定義 (Microsoft. 管理. 基礎結構)**</span><span class="sxs-lookup"><span data-stu-id="a2a9c-115">**To retrieve a class definition in C# (Microsoft.Management.Infrastructure)**</span></span>

1.  <span data-ttu-id="a2a9c-116">使用 CIMInstance 類別，以指定的 **命名空間和** 類別名稱建立一個類別。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-116">Using the **Microsoft.Management.Infrastructure** namespace, create a **CIMInstance** class with the specified namespace and class name.</span></span>

    <span data-ttu-id="a2a9c-117">建立的類別將會包含所有類別資訊，但不包含實例資料。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-117">The created class will contain all of the class information, but no instance data.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "Win32_LogicalDisk";

    CimInstance diskDrive = new CimInstance(className, Namespace);
    ```

    

2.  <span data-ttu-id="a2a9c-118">或者，如同使用 PowerShell，您也可以使用 **中繼 \_ 類別** 標記作為查詢的一部分來執行查詢。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-118">Alternately, as with PowerShell, you could also perform a query, using the **meta\_class** tag as part of the query.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string diskDriveQuery = "SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'";

    CimSession mySession = CimSession.Create("localhost");
    IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", diskDriveQuery);
    ```

    

<span data-ttu-id="a2a9c-119">如同 PowerShell，c # 會使用 **中繼 \_ 類別** 查詢來取出類別定義。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-119">As with PowerShell, C# uses a **meta\_class** query to retrieve class definitions.</span></span> <span data-ttu-id="a2a9c-120">或者，您也可以建立 **ManagementClass** 物件來直接存取類別定義。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-120">Alternately, you can create a **ManagementClass** object to access the class definition directly.</span></span>

> [!Note]  
> <span data-ttu-id="a2a9c-121">**系統管理** 是用來存取 WMI 的原始 .net 命名空間;不過，這個命名空間中的 Api 通常會較慢，而且也不會相對於其較新式的 **Microsoft 管理元件** 對應專案。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-121">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="a2a9c-122">**若要在 c # 中取出類別定義 (System. Management)**</span><span class="sxs-lookup"><span data-stu-id="a2a9c-122">**To retrieve a class definition in C# (System.Management)**</span></span>

1.  <span data-ttu-id="a2a9c-123">您可以搭配使用 [ManagementObjectSerarcher](/dotnet/api/system.management.managementobjectsearcher) 與 **中繼 \_ 類別** 的查詢，其中 WHERE 子句包含您要取出的類別名稱。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-123">You can use the [ManagementObjectSerarcher](/dotnet/api/system.management.managementobjectsearcher) with a query to **meta\_class**, with the WHERE clause containing the name of the class you with to retrieve.</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher searcher = new ManagementObjectSearcher("SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'");
    ManagementObjectCollection myDiskCollection = searcher.Get();
    ```

    

    <span data-ttu-id="a2a9c-124">[ManagementObjectSerarcher](/dotnet/api/system.management.managementobjectsearcher) 是 .net 的標準類別，用來從 WMI 取出類別和實例資訊。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-124">[ManagementObjectSerarcher](/dotnet/api/system.management.managementobjectsearcher) is the standard class .NET uses to retrieve class and instance information from WMI.</span></span> <span data-ttu-id="a2a9c-125">[ManagementObjectSerarcher： Get](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get) 會傳回包含架構定義類別的 [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) 。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-125">[ManagementObjectSerarcher.Get](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get) returns a [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) that contains the schema definition class.</span></span> <span data-ttu-id="a2a9c-126">**中繼 \_ 類別** 類別會將查詢定義為架構查詢。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-126">The **meta\_class** class defines the query as a schema query.</span></span> <span data-ttu-id="a2a9c-127">若沒有 **中繼 \_ 類別** 類別，此查詢會傳回 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)的所有實例。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-127">Without the **meta\_class** class, this query would return all instances of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span></span> <span data-ttu-id="a2a9c-128">如需查詢 WMI 的詳細資訊，請參閱 [架構查詢的 SELECT 語句](select-statement-for-schema-queries.md)。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-128">For more information about querying WMI, see [SELECT Statement for Schema Queries](select-statement-for-schema-queries.md).</span></span>

2.  <span data-ttu-id="a2a9c-129">或者，使用名稱做為路徑來建立新的 [ManagementClass](/dotnet/api/system.management.managementclass) 物件，以取出類別。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-129">Alternately, create a new [ManagementClass](/dotnet/api/system.management.managementclass) object, with the name as the path, to retrieve the class.</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementClass objInst = new ManagementClass("Win32_LogicalDisk");
    ```

    

<span data-ttu-id="a2a9c-130">您可以使用類似的方式，在 VBScript 中取出類別定義，以抓取特定的實例。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-130">You can retrieve a class definition in VBScript in a similar way to retrieving a specific instance.</span></span>

<span data-ttu-id="a2a9c-131">**若要在 VBScript 中取出類別定義**</span><span class="sxs-lookup"><span data-stu-id="a2a9c-131">**To retrieve a class definition in VBScript**</span></span>

1.  <span data-ttu-id="a2a9c-132">呼叫 [**SWbemServices**](swbemservices-get.md) ，但不識別類別的物件路徑中的特定實例。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-132">Call [**SWbemServices.Get**](swbemservices-get.md) but do not identify a specific instance in the object path for the class.</span></span>
2.  <span data-ttu-id="a2a9c-133">下列程式碼範例會抓取描述電腦上邏輯磁碟機之類別的類別定義。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-133">The following code example retrieves the class definition for the class that describes logical drives on your computer.</span></span>

    ```VB
    Set objinst = GetObject("WinMgmts:Win32_LogicalDisk")
    ```

    

    <span data-ttu-id="a2a9c-134">Windows Script Host (WSH) 也支援下列各項。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-134">Windows Script Host (WSH) also supports the following.</span></span>

    ```VB
    <OBJECT id="myLocator" progid="WbemScripting.SWbemLocator"></OBJECT>
    ```

    

    <span data-ttu-id="a2a9c-135">在 [Active Server Pages (ASP) 在伺服器端腳本中使用 [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) 或 [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) 。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-135">On Active Server Pages (ASP) use [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) or [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) in the server-side script.</span></span> <span data-ttu-id="a2a9c-136">如需詳細資訊，請參閱 [建立 WMI 的 Active Server Pages （WMI](creating-active-server-pages-for-wmi.md)）。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-136">For more information, see [Creating Active Server Pages for WMI](creating-active-server-pages-for-wmi.md).</span></span>

3.  <span data-ttu-id="a2a9c-137">也可以指定類別或實例，在此情況下，傳回的物件是 WMI 物件，例如 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)的實例，而不是服務物件。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-137">A class or instance can also be specified, in which case the returned object is a WMI object, for example, an instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), rather than a services object.</span></span> <span data-ttu-id="a2a9c-138">請注意，您不能使用 VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) 函數來建立泛型物件 [**SWbemObject**](swbemobject.md)的實例。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-138">Note that you cannot use the VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) functions to create an instance of the generic object [**SWbemObject**](swbemobject.md).</span></span>
4.  <span data-ttu-id="a2a9c-139">在 Microsoft Internet Explorer (IE) 的 HTML 網頁中， [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) 和 [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) 可能會失敗，因為 WMI 腳本物件（例如 ActiveX 控制項）不會標示為安全的腳本。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-139">In HTML pages running in Microsoft Internet Explorer (IE), [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) and [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) can fail because WMI scripting objects, like ActiveX controls, are not marked as safe for scripting.</span></span> <span data-ttu-id="a2a9c-140">其中一個例外狀況是 [**SWbemDateTime**](swbemdatetime.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-140">The one exception is the [**SWbemDateTime**](swbemdatetime.md) object.</span></span> <span data-ttu-id="a2a9c-141">這些呼叫的唯一方法就是當您降低 IE 安全性設定時（不建議這麼做）。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-141">The only way that these calls can succeed is when you lower the IE security settings, which is not recommended.</span></span>

<span data-ttu-id="a2a9c-142">在 c + + 中取出類別時，請呼叫 [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)的 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)版本。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-142">When retrieving a class in C++, call the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) version of [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>

<span data-ttu-id="a2a9c-143">**若要在 c + + 中取出類別定義**</span><span class="sxs-lookup"><span data-stu-id="a2a9c-143">**To retrieve a class definition in C++**</span></span>

1.  <span data-ttu-id="a2a9c-144">呼叫 [**IWbemServices：： GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) 或 [**IWbemServices：： GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) 方法，以取出類別的定義。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-144">Call the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) methods to retrieve the definition of a class.</span></span>
2.  <span data-ttu-id="a2a9c-145">一個類別可以有多個類別定義，通常會在您將一個以上的類別提供者載入一個命名空間時進行。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-145">One class can have multiple class definitions, which happens typically when you have more than one class provider loaded into one namespace.</span></span> <span data-ttu-id="a2a9c-146">當某個類別有多個類別定義時，WMI 會傳回探索到的第一個定義和 **WBEM \_ S \_ 重複的 \_ 物件** 狀態碼。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-146">When a class has multiple class definitions, WMI returns the first definition discovered and the **WBEM\_S\_DUPLICATE\_OBJECTS** status code.</span></span>

<span data-ttu-id="a2a9c-147">因為 [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) 會傳回類別定義，所以通常是用來做為建立實例的第一個步驟。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-147">Because [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) returns a class definition, it is commonly used as the first step in creating an instance.</span></span> <span data-ttu-id="a2a9c-148">如需如何使用 **GetObject** 的詳細資訊，請參閱 [使用 c + + 建立和宣告實例](creating-and-declaring-an-instance-using-c-.md)。</span><span class="sxs-lookup"><span data-stu-id="a2a9c-148">For more information on how to use **GetObject**, see [Creating and Declaring an Instance Using C++](creating-and-declaring-an-instance-using-c-.md).</span></span>

 

 

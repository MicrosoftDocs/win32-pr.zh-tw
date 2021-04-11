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
# <a name="retrieving-a-wmi-instance"></a><span data-ttu-id="7f738-103">正在抓取 WMI 實例</span><span class="sxs-lookup"><span data-stu-id="7f738-103">Retrieving a WMI Instance</span></span>

<span data-ttu-id="7f738-104">抓取實例是您可能會在 WMI 中執行的其中一個最常見的抓取程式。</span><span class="sxs-lookup"><span data-stu-id="7f738-104">Retrieving an instance is one of the most common retrieval procedures you are likely to perform in WMI.</span></span> <span data-ttu-id="7f738-105">您可以取出現有的實例，或建立新的未命名實例。</span><span class="sxs-lookup"><span data-stu-id="7f738-105">You can retrieve an existing instance or create a new unnamed instance.</span></span> <span data-ttu-id="7f738-106">現有實例的 WMI 路徑是必要參數。</span><span class="sxs-lookup"><span data-stu-id="7f738-106">The WMI path to the existing instance is a required parameter.</span></span> <span data-ttu-id="7f738-107">如需詳細資訊，請參閱 [描述 WMI 物件的位置](describing-the-location-of-a-wmi-object.md)。</span><span class="sxs-lookup"><span data-stu-id="7f738-107">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

> [!Note]  
> <span data-ttu-id="7f738-108">提供實例時，提供者可能無法提供特定屬性的值。</span><span class="sxs-lookup"><span data-stu-id="7f738-108">When providing an instance, a provider may be unable to provide a value for certain properties.</span></span> <span data-ttu-id="7f738-109">除非在屬性描述中另有說明，否則您無法從空白值推斷任何意義。</span><span class="sxs-lookup"><span data-stu-id="7f738-109">Unless otherwise stated in the property description, you cannot infer any meaning from an empty value.</span></span> <span data-ttu-id="7f738-110">這不會與具有 **Null** 值的字串混淆。</span><span class="sxs-lookup"><span data-stu-id="7f738-110">This is not to be confused with a string which has a **NULL** value.</span></span> <span data-ttu-id="7f738-111">在此情況下，會填入值。</span><span class="sxs-lookup"><span data-stu-id="7f738-111">In this case, the value is populated.</span></span> <span data-ttu-id="7f738-112">它是空的，但具有值： **Null**。</span><span class="sxs-lookup"><span data-stu-id="7f738-112">It is empty but has a value: **NULL**.</span></span>

 

<span data-ttu-id="7f738-113">使用 PowerShell [>get-wmiobject 指令程式](https://technet.microsoft.com/library/dd315379.aspx) 的呼叫來取出實例的本機複本。</span><span class="sxs-lookup"><span data-stu-id="7f738-113">Retrieve a local copy of the instance with a call to the PowerShell [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) cmdlet.</span></span>

<span data-ttu-id="7f738-114">**使用 PowerShell 取出 WMI 類別的實例**</span><span class="sxs-lookup"><span data-stu-id="7f738-114">**To retrieve an instance of a WMI class using PowerShell**</span></span>

-   <span data-ttu-id="7f738-115">您可以使用 *-class* 和 *-filter* 參數來取得特定的實例。</span><span class="sxs-lookup"><span data-stu-id="7f738-115">You can retrieve specific instances using the *-class* and *-filter* parameters.</span></span>

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM Win32_logicalDisk WHERE DeviceID = 'C:'"
    ```

    

<span data-ttu-id="7f738-116">您可以使用 c # 來取得 WMI 實例，方法是使用 [CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))建立搜尋物件，然後將相關的索引鍵值填入，然後使用 [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)) 呼叫來搜尋該物件。</span><span class="sxs-lookup"><span data-stu-id="7f738-116">You can retrieve a WMI instance using C# by creating a search object using [CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85)), and then filling it with the relevant key values, and then searching for that object with a [CimSession.GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)) call.</span></span>

<span data-ttu-id="7f738-117">**若要使用 c # (的) 取得 WMI 類別的實例。基礎結構**</span><span class="sxs-lookup"><span data-stu-id="7f738-117">**To retrieve an instance of a WMI class using C# (Microsoft.Management.Infrastructure)**</span></span>

1.  <span data-ttu-id="7f738-118">使用 [Microsoft. 基礎結構](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) 命名空間，建立具有相關類別名稱和命名空間的新 [CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85)) 物件。</span><span class="sxs-lookup"><span data-stu-id="7f738-118">Using the [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) namespace, create a new [CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85)) object with the relevant class name and namespace.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "Win32_LogicalDisk";

    CimInstance myDrive = new CimInstance(className, Namespace);
    ```

    

2.  <span data-ttu-id="7f738-119">建立包含您要搜尋之實例之索引鍵屬性名稱和值的 [CimProperty](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832461(v=vs.85)) ，並將該屬性加入至您的類別物件。</span><span class="sxs-lookup"><span data-stu-id="7f738-119">Create a [CimProperty](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832461(v=vs.85)) that contains the name and value of the key property of the instance you wish to search for, and add that property to your class object.</span></span>

    ```CSharp
    myDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));
    ```

    

3.  <span data-ttu-id="7f738-120">使用 [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)) ，從 WMI 取出物件。</span><span class="sxs-lookup"><span data-stu-id="7f738-120">Retrieve the object from WMI with a [CimSession.GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)) call.</span></span>

    ```CSharp
    CimSession mySession = CimSession.Create("localhost");
    CimInstance searchInstance = mySession.GetInstance(Namespace, myDrive);
    ```

    

<span data-ttu-id="7f738-121">您可以使用 [system.servicemodel 命名空間中的類別](/dotnet/api/system.management) ，來取得特定 wmi 類別實例或 wmi 類別實例的集合。</span><span class="sxs-lookup"><span data-stu-id="7f738-121">You can retrieve either a specific WMI class instance, or a collection of WMI class instances, using classes in the [System.Management](/dotnet/api/system.management) namespace.</span></span>

> [!Note]  
> <span data-ttu-id="7f738-122">**系統管理** 是用來存取 WMI 的原始 .net 命名空間;不過，這個命名空間中的 Api 通常會較慢，而且也不會相對於其較新式的 **Microsoft 管理元件** 對應專案。</span><span class="sxs-lookup"><span data-stu-id="7f738-122">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="7f738-123">**使用 c # (System. Management) 來取出 WMI 類別的實例**</span><span class="sxs-lookup"><span data-stu-id="7f738-123">**To retrieve an instance of a WMI class using C# (System.Management)**</span></span>

1.  <span data-ttu-id="7f738-124">藉由建立新的 [system.management.managementobject](/dotnet/api/system.management.managementobject)，並透過 *ManagementPath* 參數傳入的名稱和特定實例值，來取出特定實例的本機複本。</span><span class="sxs-lookup"><span data-stu-id="7f738-124">Retrieve a local copy of a specific instance by creating a new [ManagementObject](/dotnet/api/system.management.managementobject), with the name and specific instance value passed in though the *ManagementPath* parameter.</span></span> <span data-ttu-id="7f738-125">然後，您可以明確呼叫 [system.management.managementobject](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get)來取得實例資料。</span><span class="sxs-lookup"><span data-stu-id="7f738-125">You can then retrieve the instance data by explicitly calling [ManagementObject.Get](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get).</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementObject objInst = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    objInst.Get();
    ```

    

2.  <span data-ttu-id="7f738-126">或者，您也可以使用 [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher)搜尋 WMI 類別的所有實例，然後再列舉傳回的 [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection)。</span><span class="sxs-lookup"><span data-stu-id="7f738-126">Alternately, you can retrieve all instances of a WMI class by searching for them with a [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher), and then enumerating through the returned [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection).</span></span>

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

    

    <span data-ttu-id="7f738-127">您可以藉由存取實例，以隱含方式呼叫 **Get** 方法。</span><span class="sxs-lookup"><span data-stu-id="7f738-127">You can implicitly call the **Get** method by accessing the instance.</span></span> <span data-ttu-id="7f738-128">如需詳細資訊，請參閱 [取出 WMI 實例的一部分](retrieving-part-of-an-instance.md)。</span><span class="sxs-lookup"><span data-stu-id="7f738-128">For more information, see [Retrieving Part of a WMI Instance](retrieving-part-of-an-instance.md).</span></span>

<span data-ttu-id="7f738-129">使用 VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) 方法的呼叫來取出實例的本機複本。</span><span class="sxs-lookup"><span data-stu-id="7f738-129">Retrieve a local copy of the instance with a call to the VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) method.</span></span>

<span data-ttu-id="7f738-130">**使用 VBScript 取出 WMI 類別的實例**</span><span class="sxs-lookup"><span data-stu-id="7f738-130">**To retrieve an instance of a WMI class using VBScript**</span></span>

-   <span data-ttu-id="7f738-131">使用實例的物件路徑來呼叫 [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) ，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="7f738-131">Call [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) with the object path of the instance as shown in the following example.</span></span>

    ```VB
    Set objinst = GetObject("WinMgmts:Win32_LogicalDisk='C:'")
    ```

    

    <span data-ttu-id="7f738-132">若要抓取特定的實例，您必須提供名稱做為物件路徑的一部分。</span><span class="sxs-lookup"><span data-stu-id="7f738-132">Retrieving a specific instance requires giving a name as part of the object path.</span></span>

<span data-ttu-id="7f738-133">在 c + + 中，呼叫 [**IWbemServices：： GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)。</span><span class="sxs-lookup"><span data-stu-id="7f738-133">In C++, call [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>

<span data-ttu-id="7f738-134">**使用 c + + 取出 WMI 類別的實例**</span><span class="sxs-lookup"><span data-stu-id="7f738-134">**To retrieve an instance of a WMI class using C++**</span></span>

-   <span data-ttu-id="7f738-135">藉由呼叫 [**IWbemServices：： GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) 或 [**Iwbemservices：： GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)，取出實例的本機複本。</span><span class="sxs-lookup"><span data-stu-id="7f738-135">Retrieve a local copy of the instance with a call to [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span> <span data-ttu-id="7f738-136">必須包含物件的 WMI 路徑。</span><span class="sxs-lookup"><span data-stu-id="7f738-136">The WMI path to the object must be included.</span></span>

    <span data-ttu-id="7f738-137">顧名思義， [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) 會以非同步方式抓取實例，而 [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) 會以同步方式抓取實例。</span><span class="sxs-lookup"><span data-stu-id="7f738-137">As the name implies, [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) retrieves the instance asynchronously, while [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) retrieves the instance synchronously.</span></span> <span data-ttu-id="7f738-138">如果您想要使用非同步抓取，則必須執行 [**IWbemObjectSink**](iwbemobjectsink.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="7f738-138">If you want to use asynchronous retrieval, you must implement the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="7f738-139">範例</span><span class="sxs-lookup"><span data-stu-id="7f738-139">Examples</span></span>

<span data-ttu-id="7f738-140">如需使用做為範本的 VBScript 範例來取出類別和實例資訊，請參閱 TechNet 資源庫上的 [WMI 範本腳本](https://Gallery.TechNet.Microsoft.Com/aded1ef3-d2af-4821-8a92-b5c22ca2ecd8) 範例。</span><span class="sxs-lookup"><span data-stu-id="7f738-140">For a VBScript example to use as a template to retrieve class and instance information, see the [WMI Template Script](https://Gallery.TechNet.Microsoft.Com/aded1ef3-d2af-4821-8a92-b5c22ca2ecd8) example on TechNet Gallery.</span></span> <span data-ttu-id="7f738-141">這個特定的範例會使用 GetObject 來取得 WMI 服務。</span><span class="sxs-lookup"><span data-stu-id="7f738-141">This particular example uses GetObject to retrieve the WMI Service.</span></span>

 

 

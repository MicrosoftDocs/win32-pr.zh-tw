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
# <a name="enumerating-wmi"></a><span data-ttu-id="47c29-103">列舉 WMI</span><span class="sxs-lookup"><span data-stu-id="47c29-103">Enumerating WMI</span></span>

<span data-ttu-id="47c29-104">列舉是指移動一組物件，並且可能會在執行此動作時修改每個物件的動作。</span><span class="sxs-lookup"><span data-stu-id="47c29-104">Enumeration is the act of moving through a set of objects and possibly modifying each object as you do so.</span></span> <span data-ttu-id="47c29-105">例如，您可以列舉一組 [**Win32 \_ DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive) 物件來尋找特定的序號。</span><span class="sxs-lookup"><span data-stu-id="47c29-105">For example, you can enumerate through a set of [**Win32\_DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive) objects to find a particular serial number.</span></span> <span data-ttu-id="47c29-106">請注意，雖然您可以列舉任何物件，但 WMI 只會傳回您具有安全性存取權的物件。</span><span class="sxs-lookup"><span data-stu-id="47c29-106">Note that although you can enumerate any object, WMI only returns objects to which you have security access.</span></span>

<span data-ttu-id="47c29-107">大型資料集的列舉可能需要大量的資源，並降低效能。</span><span class="sxs-lookup"><span data-stu-id="47c29-107">Enumerations of large data sets can require a large amount of resources and degrade performance.</span></span> <span data-ttu-id="47c29-108">如需詳細資訊，請參閱 [改善列舉效能](improving-enumeration-performance.md)。</span><span class="sxs-lookup"><span data-stu-id="47c29-108">For more information, see [Improving Enumeration Performance](improving-enumeration-performance.md).</span></span> <span data-ttu-id="47c29-109">您也可以使用更特定的查詢來要求資料。</span><span class="sxs-lookup"><span data-stu-id="47c29-109">You also can request data with a more specific query.</span></span> <span data-ttu-id="47c29-110">如需詳細資訊，請參閱 [查詢 WMI](querying-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="47c29-110">For more information, see [Querying WMI](querying-wmi.md).</span></span>

<span data-ttu-id="47c29-111">本主題將討論下列各節：</span><span class="sxs-lookup"><span data-stu-id="47c29-111">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="47c29-112">使用 PowerShell 列舉 WMI</span><span class="sxs-lookup"><span data-stu-id="47c29-112">Enumerating WMI Using PowerShell</span></span>](#enumerating-wmi-using-powershell)
-   [<span data-ttu-id="47c29-113">使用 c # (Microsoft 管理) 列舉 WMI </span><span class="sxs-lookup"><span data-stu-id="47c29-113">Enumerating WMI Using C# (Microsoft.Management.Infrastructure)</span></span>](#enumerating-wmi-using-c-microsoftmanagementinfrastructure)
-   [<span data-ttu-id="47c29-114">使用 c # (System. Management) 來列舉 WMI </span><span class="sxs-lookup"><span data-stu-id="47c29-114">Enumerating WMI Using C# (System.Management)</span></span>](#enumerating-wmi-using-c-systemmanagement)
-   [<span data-ttu-id="47c29-115">使用 VBScript 列舉 WMI</span><span class="sxs-lookup"><span data-stu-id="47c29-115">Enumerating WMI Using VBScript</span></span>](#enumerating-wmi-using-vbscript)
-   [<span data-ttu-id="47c29-116">使用 c + + 列舉 WMI</span><span class="sxs-lookup"><span data-stu-id="47c29-116">Enumerating WMI Using C++</span></span>](#enumerating-wmi-using-c-microsoftmanagementinfrastructure)

## <a name="enumerating-wmi-using-powershell"></a><span data-ttu-id="47c29-117">使用 PowerShell 列舉 WMI</span><span class="sxs-lookup"><span data-stu-id="47c29-117">Enumerating WMI Using PowerShell</span></span>

<span data-ttu-id="47c29-118">如果您不知道特定實例的物件路徑，或想要取得特定類別的所有實例，請使用 [>get-wmiobject](https://technet.microsoft.com/library/dd315379.aspx)，並在 *-class* 參數中使用類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="47c29-118">If you do not know the object path for a specific instance, or you want to retrieve all the instances for a specific class, use [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx), with the name of the class in the *-class* parameter.</span></span> <span data-ttu-id="47c29-119">如果您想要使用查詢，可以使用 *-query* 參數。</span><span class="sxs-lookup"><span data-stu-id="47c29-119">If you want to use a query, you can use the *-query* parameter.</span></span>

<span data-ttu-id="47c29-120">下列程式描述如何使用 PowerShell 列舉類別的實例。</span><span class="sxs-lookup"><span data-stu-id="47c29-120">The following procedure describes how to enumerate the instances of a class using PowerShell.</span></span>

<span data-ttu-id="47c29-121">**使用 PowerShell 列舉類別的實例**</span><span class="sxs-lookup"><span data-stu-id="47c29-121">**To enumerate the instances of a class using PowerShell**</span></span>

1.  <span data-ttu-id="47c29-122">使用 [>get-wmiobject](https://technet.microsoft.com/library/dd315379.aspx) Cmdlet 的呼叫來列舉實例。</span><span class="sxs-lookup"><span data-stu-id="47c29-122">Enumerate the instances with a call to [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) cmdlet.</span></span>

    <span data-ttu-id="47c29-123">[>get-wmiobject](https://technet.microsoft.com/library/dd315379.aspx) 會傳回一或多個 WMI 物件的集合，您可以透過這些物件來列舉。</span><span class="sxs-lookup"><span data-stu-id="47c29-123">[Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) returns a collection of one or more WMI objects, through which you can enumerate.</span></span> <span data-ttu-id="47c29-124">如需詳細資訊，請參閱 [存取集合](accessing-a-collection.md)。</span><span class="sxs-lookup"><span data-stu-id="47c29-124">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

    <span data-ttu-id="47c29-125">如果您想要在另一個命名空間或不同的電腦上取出 WMI 類別實例，請分別在 *-computer* 和 *-namespace* 參數中指定電腦和命名空間。</span><span class="sxs-lookup"><span data-stu-id="47c29-125">If you wish to retrieve a WMI class instance in another namespace or on a different computer, specify the computer and namespace in the *-computer* and *-namespace* parameters, respectively.</span></span> <span data-ttu-id="47c29-126">如需詳細資訊，請參閱 [建立 WMI 腳本](creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="47c29-126">For more information, see [Creating a WMI Script](creating-a-wmi-script.md).</span></span> <span data-ttu-id="47c29-127">只有當您有適當的存取權限時，才適用此功能。</span><span class="sxs-lookup"><span data-stu-id="47c29-127">This only works if you have the appropriate access privileges.</span></span> <span data-ttu-id="47c29-128">如需詳細資訊，請參閱 [維護 WMI 安全性](maintaining-wmi-security.md) 和執行具特殊 [許可權的作業](executing-privileged-operations.md)。</span><span class="sxs-lookup"><span data-stu-id="47c29-128">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md) and [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

2.  <span data-ttu-id="47c29-129">使用集合的成員抓取任何您想要的個別實例。</span><span class="sxs-lookup"><span data-stu-id="47c29-129">Retrieve any individual instances you wish using the collection's members.</span></span>

<span data-ttu-id="47c29-130">下列程式碼範例會抓取 PowerShell 集合，然後顯示本機電腦上所有邏輯磁碟機實例的大小屬性。</span><span class="sxs-lookup"><span data-stu-id="47c29-130">The following code example retrieves an PowerShell collection and then displays the size property for all instances of logical drives on the local computer.</span></span>


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



## <a name="enumerating-wmi-using-c-microsoftmanagementinfrastructure"></a><span data-ttu-id="47c29-131">使用 c # (Microsoft 管理) 列舉 WMI</span><span class="sxs-lookup"><span data-stu-id="47c29-131">Enumerating WMI Using C# (Microsoft.Management.Infrastructure)</span></span>

1.  <span data-ttu-id="47c29-132">新增參考至 **Microsoft. 管理基礎結構** 參考元件。</span><span class="sxs-lookup"><span data-stu-id="47c29-132">Add a reference to the **Microsoft.Management.Infrastructure** reference assembly.</span></span> <span data-ttu-id="47c29-133"> (此元件隨附于 [Windows 8 Windows 軟體開發套件 (SDK) ](https://msdn.microsoft.com/library/windows/desktop/hh852363.aspx)的一部分。 ) </span><span class="sxs-lookup"><span data-stu-id="47c29-133">(This assembly ships as part of the [Windows Software Development Kit (SDK) for Windows 8](https://msdn.microsoft.com/library/windows/desktop/hh852363.aspx).)</span></span>
2.  <span data-ttu-id="47c29-134">針對 **Microsoft. 基礎結構** 命名空間加入 **using** 語句。</span><span class="sxs-lookup"><span data-stu-id="47c29-134">Add a **using** statement for the **Microsoft.Management.Infrastructure** namespace.</span></span>

```CSharp
    using Microsoft.Management.Infrastructure;
```

    

3.  <span data-ttu-id="47c29-135">具現化 [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) 物件。</span><span class="sxs-lookup"><span data-stu-id="47c29-135">Instantiate a [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) object.</span></span> <span data-ttu-id="47c29-136">下列程式碼片段會使用 [**CimSession. Create**](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)) 方法的標準 "localhost" 值。</span><span class="sxs-lookup"><span data-stu-id="47c29-136">The following snippet uses the standard "localhost" value for the [**CimSession.Create**](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)) method.</span></span>

```CSharp
    CimSession cimSession = CimSession.Create("localhost");
```

    

4.  <span data-ttu-id="47c29-137">呼叫 [**CimSession QueryInstances**](https://www.bing.com/search?q=**CimSession.QueryInstances**) 方法，傳遞所需的 CIM 命名空間和 WQL 來使用。</span><span class="sxs-lookup"><span data-stu-id="47c29-137">Call the [**CimSession.QueryInstances**](https://www.bing.com/search?q=**CimSession.QueryInstances**) method passing the desired CIM namespace and WQL to use.</span></span> <span data-ttu-id="47c29-138">下列程式碼片段會傳回兩個實例，代表兩個標準 Windows 進程，其中 handle 屬性 (代表處理序識別碼，或 PID) 的值為0或4。</span><span class="sxs-lookup"><span data-stu-id="47c29-138">The following snippet will return two instances representing two standard Windows processes where the handle property (representing a process ID, or PID) has a value of either 0 or 4.</span></span>

```CSharp
    IEnumerable<CimInstance> queryInstances =     
      cimSession.QueryInstances(@"root\cimv2", 
                                "WQL", 
                                @"select name from win32_process where handle = 0 or handle = 4");
```

    

5.  <span data-ttu-id="47c29-139">對傳回的 [**CimInstance**](https://www.bing.com/search?q=**CimInstance**) 物件執行迴圈。</span><span class="sxs-lookup"><span data-stu-id="47c29-139">Loop through the returned [**CimInstance**](https://www.bing.com/search?q=**CimInstance**) objects.</span></span>

```CSharp
    foreach (CimInstance cimInstance in enumeratedInstances)
    { 
      Console.WriteLine("Process name: {0}", cimInstance.CimInstanceProperties["Name"].Value);  
    }
```

    

<span data-ttu-id="47c29-140">下列程式碼範例會列舉 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process) 類別的所有實例， (代表本機電腦上) 的使用中進程，並列印每個進程的名稱。</span><span class="sxs-lookup"><span data-stu-id="47c29-140">The following code sample enumerates all instances of the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class (which represents active processes) on the local machine, and prints the name of each process.</span></span>

> [!Note]  
> <span data-ttu-id="47c29-141">在實際的應用程式中，您會將電腦名稱稱 ( "localhost" ) 和 CIM 命名空間 ( "root cimv2" ) 的參數定義為參數 \\ 。</span><span class="sxs-lookup"><span data-stu-id="47c29-141">In a real application you would define as parameters the computer name ("localhost") and CIM namespace ("root\\cimv2").</span></span> <span data-ttu-id="47c29-142">為了簡單起見，在此範例中，這些都已硬式編碼。</span><span class="sxs-lookup"><span data-stu-id="47c29-142">For purposes of simplicity, these have been hardcoded in this example.</span></span>

 


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





## <a name="enumerating-wmi-using-c-systemmanagement"></a><span data-ttu-id="47c29-143">使用 c # (System. Management) 來列舉 WMI</span><span class="sxs-lookup"><span data-stu-id="47c29-143">Enumerating WMI Using C# (System.Management)</span></span>

<span data-ttu-id="47c29-144">如果您不知道特定實例的物件路徑，或您想要取出特定類別的所有實例，請使用 [ManagementClass](/dotnet/api/system.management.managementclass) 物件來取出 [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) ，其中包含 WMI 命名空間中指定類別的所有實例。</span><span class="sxs-lookup"><span data-stu-id="47c29-144">If you do not know the object path for a specific instance, or you want to retrieve all the instances for a specific class, use the [ManagementClass](/dotnet/api/system.management.managementclass) object to retrieve a [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) that contains all instances of a given class in the WMI namespace.</span></span> <span data-ttu-id="47c29-145">或者，您也可以透過 [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher) 來查詢 WMI，以取得相同的物件集合。</span><span class="sxs-lookup"><span data-stu-id="47c29-145">Alternately, you can query WMI through a [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher) to obtain the same set of objects.</span></span>

> [!Note]  
> <span data-ttu-id="47c29-146">**系統管理** 是用來存取 WMI 的原始 .net 命名空間;不過，這個命名空間中的 Api 通常會較慢，而且也不會相對於其較新式的 **Microsoft 管理元件** 對應專案。</span><span class="sxs-lookup"><span data-stu-id="47c29-146">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="47c29-147">下列程式說明如何使用 c # 列舉類別的實例。</span><span class="sxs-lookup"><span data-stu-id="47c29-147">The following procedure describes how to enumerate the instances of a class using C#.</span></span>

<span data-ttu-id="47c29-148">**使用 C 列舉類別的實例#**</span><span class="sxs-lookup"><span data-stu-id="47c29-148">**To enumerate the instances of a class using C#**</span></span>

1.  <span data-ttu-id="47c29-149">使用 [ManagementClass. GetInstances](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances)的呼叫來列舉實例。</span><span class="sxs-lookup"><span data-stu-id="47c29-149">Enumerate the instances with a call to [ManagementClass.GetInstances](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances).</span></span>

    <span data-ttu-id="47c29-150">[GetInstances](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances)方法會傳回可供您列舉的物件集合（或集合）。</span><span class="sxs-lookup"><span data-stu-id="47c29-150">The [GetInstances](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances) method returns a collection, or set, of objects through which you can enumerate.</span></span> <span data-ttu-id="47c29-151">如需詳細資訊，請參閱 [存取集合](accessing-a-collection.md)。</span><span class="sxs-lookup"><span data-stu-id="47c29-151">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span> <span data-ttu-id="47c29-152">傳回的集合實際上是 [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) 物件，因此可以呼叫該物件的任何方法。</span><span class="sxs-lookup"><span data-stu-id="47c29-152">The returned collection is actually an [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) object, so any of the methods of that object can be called.</span></span>

    <span data-ttu-id="47c29-153">如果您想要在另一個命名空間或不同的電腦上取出 WMI 類別實例，請在 *path* 參數中指定電腦和命名空間。</span><span class="sxs-lookup"><span data-stu-id="47c29-153">If you wish to retrieve a WMI class instance in another namespace or on a different computer, specify the computer and namespace in the *path* parameter.</span></span> <span data-ttu-id="47c29-154">如需詳細資訊，請參閱 [建立 WMI 腳本](creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="47c29-154">For more information, see [Creating a WMI Script](creating-a-wmi-script.md).</span></span> <span data-ttu-id="47c29-155">只有當您有適當的存取權限時，才適用此功能。</span><span class="sxs-lookup"><span data-stu-id="47c29-155">This only works if you have the appropriate access privileges.</span></span> <span data-ttu-id="47c29-156">如需詳細資訊，請參閱 [維護 WMI 安全性](maintaining-wmi-security.md) 和執行具特殊 [許可權的作業](executing-privileged-operations.md)。</span><span class="sxs-lookup"><span data-stu-id="47c29-156">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md) and [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

2.  <span data-ttu-id="47c29-157">使用集合的成員抓取任何您想要的個別實例。</span><span class="sxs-lookup"><span data-stu-id="47c29-157">Retrieve any individual instances you wish using the collection's members.</span></span>

<span data-ttu-id="47c29-158">下列程式碼範例會抓取 c # 集合，然後顯示本機電腦上所有邏輯磁碟機實例的 size 屬性。</span><span class="sxs-lookup"><span data-stu-id="47c29-158">The following code example retrieves an C# collection and then displays the size property for all instances of logical drives on the local computer.</span></span>


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



## <a name="enumerating-wmi-using-vbscript"></a><span data-ttu-id="47c29-159">使用 VBScript 列舉 WMI</span><span class="sxs-lookup"><span data-stu-id="47c29-159">Enumerating WMI Using VBScript</span></span>

<span data-ttu-id="47c29-160">如果您不知道特定實例的物件路徑，或想要取得特定類別的所有實例，請使用 [**SWbemServices. InstancesOf**](swbemservices-instancesof.md) 方法來傳回類別所有實例的 [**swbemobjectset 搭配使用**](swbemobjectset.md) 列舉。</span><span class="sxs-lookup"><span data-stu-id="47c29-160">If you do not know the object path for a specific instance, or you want to retrieve all the instances for a specific class, use the [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) method to return an [**SWbemObjectSet**](swbemobjectset.md) enumeration of all the instances of a class.</span></span> <span data-ttu-id="47c29-161">或者，您也可以透過 [**SWbemServices.ExecQuery**](swbemservices-execquery.md) 來查詢 WMI，以取得相同的物件集。</span><span class="sxs-lookup"><span data-stu-id="47c29-161">Alternatively you can query WMI through [**SWbemServices.ExecQuery**](swbemservices-execquery.md) to obtain the same set of objects.</span></span>

<span data-ttu-id="47c29-162">下列程式描述如何使用 VBScript 列舉類別的實例。</span><span class="sxs-lookup"><span data-stu-id="47c29-162">The following procedure describes how to enumerate the instances of a class using VBScript.</span></span>

<span data-ttu-id="47c29-163">**使用 VBScript 列舉類別的實例**</span><span class="sxs-lookup"><span data-stu-id="47c29-163">**To enumerate the instances of a class using VBScript**</span></span>

1.  <span data-ttu-id="47c29-164">使用 [**SWbemServices. InstancesOf**](swbemservices-instancesof.md) 方法的呼叫來列舉實例。</span><span class="sxs-lookup"><span data-stu-id="47c29-164">Enumerate the instances with a call to the [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) method.</span></span>

    <span data-ttu-id="47c29-165">[**InstancesOf**](swbemservices-instancesof.md)方法會傳回可供您列舉的物件集合（或集合）。</span><span class="sxs-lookup"><span data-stu-id="47c29-165">The [**InstancesOf**](swbemservices-instancesof.md) method returns a collection, or set, of objects through which you can enumerate.</span></span> <span data-ttu-id="47c29-166">如需詳細資訊，請參閱 [存取集合](accessing-a-collection.md)。</span><span class="sxs-lookup"><span data-stu-id="47c29-166">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span> <span data-ttu-id="47c29-167">傳回的集合實際上是 [**swbemobjectset 搭配使用**](swbemobjectset.md) 物件，因此可以呼叫該物件的任何方法。</span><span class="sxs-lookup"><span data-stu-id="47c29-167">The returned collection is actually an [**SWbemObjectSet**](swbemobjectset.md) object, so any of the methods of that object can be called.</span></span>

    <span data-ttu-id="47c29-168">如果您想要在另一個命名空間或不同的電腦上取出 WMI 類別實例，請在 [標記] 中指定電腦和命名空間。</span><span class="sxs-lookup"><span data-stu-id="47c29-168">If you wish to retrieve a WMI class instance in another namespace or on a different computer, specify the computer and namespace in the moniker.</span></span> <span data-ttu-id="47c29-169">如需詳細資訊，請參閱 [建立 WMI 腳本](creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="47c29-169">For more information, see [Creating a WMI Script](creating-a-wmi-script.md).</span></span> <span data-ttu-id="47c29-170">只有當您有適當的存取權限時，才適用此功能。</span><span class="sxs-lookup"><span data-stu-id="47c29-170">This only works if you have the appropriate access privileges.</span></span> <span data-ttu-id="47c29-171">如需詳細資訊，請參閱 [維護 WMI 安全性](maintaining-wmi-security.md) 和執行具特殊 [許可權的作業](executing-privileged-operations.md)。</span><span class="sxs-lookup"><span data-stu-id="47c29-171">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md) and [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

2.  <span data-ttu-id="47c29-172">使用集合方法抓取您想要的任何個別實例。</span><span class="sxs-lookup"><span data-stu-id="47c29-172">Retrieve any individual instances you wish using the collections methods.</span></span>

<span data-ttu-id="47c29-173">下列程式碼範例會抓取 [**SWbemServices**](swbemservices.md) 物件，然後執行 [**InstancesOf**](swbemservices-instancesof.md) 方法，以顯示本機電腦上所有邏輯磁碟機實例的大小屬性。</span><span class="sxs-lookup"><span data-stu-id="47c29-173">The following code example retrieves an [**SWbemServices**](swbemservices.md) object and then executes the [**InstancesOf**](swbemservices-instancesof.md) method to display the size property for all instances of logical drives on the local computer.</span></span>


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



## <a name="enumerating-wmi-using-c"></a><span data-ttu-id="47c29-174">使用 c + + 列舉 WMI</span><span class="sxs-lookup"><span data-stu-id="47c29-174">Enumerating WMI Using C++</span></span>

<span data-ttu-id="47c29-175">除了執行基本欄舉之外，您還可以設定數個旗標和屬性來提升列舉的效能。</span><span class="sxs-lookup"><span data-stu-id="47c29-175">In addition to performing basic enumeration, you can set several flags and properties to increase the performance of your enumeration.</span></span> <span data-ttu-id="47c29-176">如需詳細資訊，請參閱 [改善列舉效能](improving-enumeration-performance.md)。</span><span class="sxs-lookup"><span data-stu-id="47c29-176">For more information, see [Improving Enumeration Performance](improving-enumeration-performance.md).</span></span>

<span data-ttu-id="47c29-177">**列舉 WMI 中的物件集**</span><span class="sxs-lookup"><span data-stu-id="47c29-177">**To enumerate an object set in WMI**</span></span>

1.  <span data-ttu-id="47c29-178">建立 [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) 介面，以描述您想要列舉的物件集合。</span><span class="sxs-lookup"><span data-stu-id="47c29-178">Create an [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) interface describing the set of objects you wish to enumerate.</span></span>

    <span data-ttu-id="47c29-179">[**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)物件包含描述一組 WMI 物件的清單。</span><span class="sxs-lookup"><span data-stu-id="47c29-179">An [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) object contains a list describing a set of WMI objects.</span></span> <span data-ttu-id="47c29-180">您可以使用 **IEnumWbemClassObject** 方法來列舉轉寄、略過物件、從開頭開始，以及複製列舉值。</span><span class="sxs-lookup"><span data-stu-id="47c29-180">You can use the **IEnumWbemClassObject** methods to enumerate forwards, skip objects, begin at the beginning, and copy the enumerator.</span></span> <span data-ttu-id="47c29-181">下表列出用來針對不同類型的 WMI 物件建立枚舉器的方法。</span><span class="sxs-lookup"><span data-stu-id="47c29-181">The following table lists the methods use to create enumerators for different types of WMI objects.</span></span>

    

    <table>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="47c29-182">Object</span><span class="sxs-lookup"><span data-stu-id="47c29-182">Object</span></span></th>
    <th><span data-ttu-id="47c29-183">方法</span><span class="sxs-lookup"><span data-stu-id="47c29-183">Method</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="47c29-184">類別</span><span class="sxs-lookup"><span data-stu-id="47c29-184">Class</span></span></td>
    <td><dl><span data-ttu-id="47c29-185"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum"><strong>IWbemServices：： CreateClassEnum</strong></a></span><span class="sxs-lookup"><span data-stu-id="47c29-185"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum"><strong>IWbemServices::CreateClassEnum</strong></a></span></span><br />
<span data-ttu-id="47c29-186">[<strong>IWbemServices：： CreateClassEnumAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) </span><span class="sxs-lookup"><span data-stu-id="47c29-186">[<strong>IWbemServices::CreateClassEnumAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)</span></span><br />
    </dl></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="47c29-187">執行個體</span><span class="sxs-lookup"><span data-stu-id="47c29-187">Instance</span></span></td>
    <td><dl><span data-ttu-id="47c29-188"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum"><strong>IWbemServices：： CreateInstanceEnum</strong></a></span><span class="sxs-lookup"><span data-stu-id="47c29-188"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum"><strong>IWbemServices::CreateInstanceEnum</strong></a></span></span><br />
<span data-ttu-id="47c29-189">[<strong>IWbemServices：： CreateInstanceEnumAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) </span><span class="sxs-lookup"><span data-stu-id="47c29-189">[<strong>IWbemServices::CreateInstanceEnumAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)</span></span><br />
    </dl></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="47c29-190">查詢結果</span><span class="sxs-lookup"><span data-stu-id="47c29-190">Query result</span></span></td>
    <td><dl><span data-ttu-id="47c29-191"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery"><strong>IWbemServices：： ExecQuery</strong></a></span><span class="sxs-lookup"><span data-stu-id="47c29-191"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery"><strong>IWbemServices::ExecQuery</strong></a></span></span><br />
<span data-ttu-id="47c29-192">[<strong>IWbemServices：： ExecQueryAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) </span><span class="sxs-lookup"><span data-stu-id="47c29-192">[<strong>IWbemServices::ExecQueryAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)</span></span><br />
    </dl></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="47c29-193">事件通知</span><span class="sxs-lookup"><span data-stu-id="47c29-193">Event notification</span></span></td>
    <td><dl><span data-ttu-id="47c29-194"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery"><strong>IWbemServices：： ExecNotificationQuery</strong></a></span><span class="sxs-lookup"><span data-stu-id="47c29-194"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery"><strong>IWbemServices::ExecNotificationQuery</strong></a></span></span><br />
<span data-ttu-id="47c29-195">[<strong>IWbemServices：： ExecNotificationQueryAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) </span><span class="sxs-lookup"><span data-stu-id="47c29-195">[<strong>IWbemServices::ExecNotificationQueryAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)</span></span><br />
    </dl></td>
    </tr>
    </tbody>
    </table>

    

     

2.  <span data-ttu-id="47c29-196">使用多個對 [**IEnumWbemClassObject：： Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) 或 [**IEnumWbemClassObject：： NextAsync**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync)的呼叫，以遍歷傳回的列舉。</span><span class="sxs-lookup"><span data-stu-id="47c29-196">Traverse through the returned enumeration using multiple calls to [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) or [**IEnumWbemClassObject::NextAsync**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync).</span></span>

<span data-ttu-id="47c29-197">如需詳細資訊，請參閱 [操作類別和實例資訊](manipulating-class-and-instance-information.md)。</span><span class="sxs-lookup"><span data-stu-id="47c29-197">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

 

 

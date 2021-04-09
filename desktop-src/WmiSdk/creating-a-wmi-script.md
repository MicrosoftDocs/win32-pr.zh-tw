---
description: 您可以使用腳本來查看或操作 WMI 所提供的任何資訊。
ms.assetid: 90e71e17-c2e7-42ad-a72e-2b475e6163fe
ms.tgt_platform: multiple
title: 建立 WMI 腳本
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1ef13a5f9269dbc24566e95ce37101d10afa6c90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945390"
---
# <a name="creating-a-wmi-script"></a><span data-ttu-id="870bb-103">建立 WMI 腳本</span><span class="sxs-lookup"><span data-stu-id="870bb-103">Creating a WMI Script</span></span>

<span data-ttu-id="870bb-104">您可以使用腳本來查看或操作 WMI 所提供的任何資訊。</span><span class="sxs-lookup"><span data-stu-id="870bb-104">You can view or manipulate any information made available through WMI using scripts.</span></span> <span data-ttu-id="870bb-105">腳本可以用任何支援 Microsoft ActiveX script 裝載的指令碼語言撰寫，包括 Visual Basic Scripting Edition (VBScript) 、PowerShell 和 Perl。</span><span class="sxs-lookup"><span data-stu-id="870bb-105">Scripts can be written in any scripting language that supports Microsoft ActiveX script hosting, including Visual Basic Scripting Edition (VBScript), PowerShell, and Perl.</span></span> <span data-ttu-id="870bb-106">Windows Script Host (WSH) 、Active Server Pages 和 Internet Explorer 都可以裝載 WMI 腳本。</span><span class="sxs-lookup"><span data-stu-id="870bb-106">Windows Script Host (WSH), Active Server Pages, and Internet Explorer can all host WMI scripts.</span></span>

> [!Note]
>
> <span data-ttu-id="870bb-107">WMI 目前支援的主要指令碼語言是 PowerShell。</span><span class="sxs-lookup"><span data-stu-id="870bb-107">The primary scripting language currently supported by WMI is PowerShell.</span></span> <span data-ttu-id="870bb-108">但是 WMI 也包含一套強大的腳本支援主體，也就是存取 [WMI 的腳本 API](scripting-api-for-wmi.md)的 VBScript 和其他語言。</span><span class="sxs-lookup"><span data-stu-id="870bb-108">However, WMI also contains a robust body of scripting support for VBScript and other languages that access the [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

 

## <a name="wmi-scripting-languages"></a><span data-ttu-id="870bb-109">WMI 指令碼語言</span><span class="sxs-lookup"><span data-stu-id="870bb-109">WMI Scripting Languages</span></span>

<span data-ttu-id="870bb-110">WMI 所支援的兩種主要語言，是透過 Windows Script Host 或 WSH)  (PowerShell 和 VBScript。</span><span class="sxs-lookup"><span data-stu-id="870bb-110">The two main languages supported by WMI are PowerShell and VBScript (through the Windows Script Host, or WSH).</span></span>

-   <span data-ttu-id="870bb-111">**PowerShell** 是設計成與 WMI 緊密整合的概念。</span><span class="sxs-lookup"><span data-stu-id="870bb-111">**PowerShell** was designed with tight integration with WMI in mind.</span></span> <span data-ttu-id="870bb-112">因此，WMI 的許多基礎元素都內建于 WMI Cmdlet 中： [>get-wmiobject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1)、 [set-wmiinstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1)、 [>invoke-wmimethod](/powershell/module/microsoft.powershell.management/invoke-wmimethod?view=powershell-5.1)和 [Remove->get-wmiobject](/powershell/module/microsoft.powershell.management/remove-wmiobject?view=powershell-5.1)。</span><span class="sxs-lookup"><span data-stu-id="870bb-112">As such, much of the underlying elements of WMI are built into the WMI cmdlets: [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1), [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1), [Invoke-WmiMethod](/powershell/module/microsoft.powershell.management/invoke-wmimethod?view=powershell-5.1), and [Remove-WmiObject](/powershell/module/microsoft.powershell.management/remove-wmiobject?view=powershell-5.1).</span></span> <span data-ttu-id="870bb-113">下表說明用來存取 WMI 資訊的一般處理常式。</span><span class="sxs-lookup"><span data-stu-id="870bb-113">The following table describes the general processes used for accessing WMI information.</span></span> <span data-ttu-id="870bb-114">請注意，雖然這些範例大多使用 >get-wmiobject，但許多 PowerShell WMI Cmdlet 都有相同的參數，例如 *類別* 或 *-認證*。</span><span class="sxs-lookup"><span data-stu-id="870bb-114">Note that while most of these examples use Get-WMIObject, many of the PowerShell WMI cmdlets have the same parameters, such as *-Class* or *-Credentials*.</span></span> <span data-ttu-id="870bb-115">因此，其中許多程式也適用于其他物件。</span><span class="sxs-lookup"><span data-stu-id="870bb-115">Therefore, many of these processes also work for other objects.</span></span> <span data-ttu-id="870bb-116">如需更深入的 PowerShell 和 WMI 討論，請參閱 [使用 Get-WMiObject Cmdlet](/previous-versions/windows/it-pro/windows-powershell-1.0/ee176860(v=technet.10)) 和 [Windows PowerShell-WMI 連接](/previous-versions/technet-magazine/cc162365(v=msdn.10))。</span><span class="sxs-lookup"><span data-stu-id="870bb-116">For a more in-depth discussion of PowerShell and WMI, see [Using the Get-WMiObject Cmdlet](/previous-versions/windows/it-pro/windows-powershell-1.0/ee176860(v=technet.10)) and [Windows PowerShell - the WMI Connection](/previous-versions/technet-magazine/cc162365(v=msdn.10)).</span></span>

-   <span data-ttu-id="870bb-117">相反地， **VBScript** 會明確呼叫 [WMI 的腳本 API](scripting-api-for-wmi.md)（如上所述）。</span><span class="sxs-lookup"><span data-stu-id="870bb-117">**VBScript**, in contrast, explicitly makes calls to the [Scripting API for WMI](scripting-api-for-wmi.md), as mentioned above.</span></span> <span data-ttu-id="870bb-118">其他語言（例如 Perl）也可以使用適用于 WMI 的腳本 API。</span><span class="sxs-lookup"><span data-stu-id="870bb-118">Other languages, such as Perl, can also use the scripting API for WMI.</span></span> <span data-ttu-id="870bb-119">不過，基於本檔的目的，大部分示範適用于 WMI 的腳本 API 的範例都會使用 VBScript。</span><span class="sxs-lookup"><span data-stu-id="870bb-119">However, for the purposes of this documentation, most samples that demonstrate the scripting API for WMI will use VBScript.</span></span> <span data-ttu-id="870bb-120">不過，當程式設計技術是 VBScript 專屬的時候，就會呼叫它。</span><span class="sxs-lookup"><span data-stu-id="870bb-120">When a programming technique is specific to VBScript, however, it will be called out.</span></span>

    <span data-ttu-id="870bb-121">VBScript 基本上有兩種不同的方式可以存取 WMI。</span><span class="sxs-lookup"><span data-stu-id="870bb-121">VBScript has essentially two separate ways of accessing WMI.</span></span> <span data-ttu-id="870bb-122">第一個是使用 [**wbemscripting.swbemlocator**](swbemlocator.md) 物件來連接至 WMI。</span><span class="sxs-lookup"><span data-stu-id="870bb-122">The first is using an [**SWbemLocator**](swbemlocator.md) object to connect to WMI.</span></span> <span data-ttu-id="870bb-123">或者，您也可以使用 [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)) 和名字標記。</span><span class="sxs-lookup"><span data-stu-id="870bb-123">Alternately, you can use [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)) and a moniker.</span></span> <span data-ttu-id="870bb-124">「名字標記」（namespace）是一種字串，可描述數個元素：您的認證、模擬設定、要連接的目的電腦、WMI [*命名空間*](gloss-n.md) (IE、wmi 用來儲存物件群組) 的一般位置，以及您想要取出的 wmi 物件。</span><span class="sxs-lookup"><span data-stu-id="870bb-124">A moniker is a string that can describe a number of elements: your credentials, impersonation settings, what computer you want to connect to, the WMI [*namespace*](gloss-n.md) (ie, the general location where WMI stores groups of objects), and what WMI object you want to retrieve.</span></span> <span data-ttu-id="870bb-125">下列許多範例都會說明這兩種技術。</span><span class="sxs-lookup"><span data-stu-id="870bb-125">Many of the examples below describe both techniques.</span></span> <span data-ttu-id="870bb-126">如需詳細資訊，請參閱 [建立標記字串](constructing-a-moniker-string.md) 和 [描述 WMI 物件的位置](describing-the-location-of-a-wmi-object.md)。</span><span class="sxs-lookup"><span data-stu-id="870bb-126">For more information, see [Constructing a Moniker String](constructing-a-moniker-string.md) and [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

    <span data-ttu-id="870bb-127">無論您使用哪一種技術來連接至 WMI，都可能會從腳本 API 中取出一或多個物件。</span><span class="sxs-lookup"><span data-stu-id="870bb-127">Regardless of what technique you use to connect to WMI, you will likely retrieve one or more objects from the Scripting API.</span></span> <span data-ttu-id="870bb-128">最常見的 [**SWbemObject**](swbemobject.md)是 wmi 用來描述 wmi 物件的。</span><span class="sxs-lookup"><span data-stu-id="870bb-128">The most common is [**SWbemObject**](swbemobject.md), which WMI uses to describe a WMI object.</span></span> <span data-ttu-id="870bb-129">或者，您可以使用 [**SWbemServices**](swbemservices.md) 物件來描述 wmi 服務本身，或使用 [**SWbemObjectPath**](swbemobjectpath.md) 物件來描述 wmi 物件的位置。</span><span class="sxs-lookup"><span data-stu-id="870bb-129">Alternately, you may use an [**SWbemServices**](swbemservices.md) object to describe the WMI service itself, or an [**SWbemObjectPath**](swbemobjectpath.md) object to describe the location of a WMI object.</span></span> <span data-ttu-id="870bb-130">如需詳細資訊，請參閱使用 SWbemObject 和腳本協助程式[物件](scripting-helper-objects.md)[編寫腳本](scripting-with-swbemobject.md)。</span><span class="sxs-lookup"><span data-stu-id="870bb-130">For more information, see [Scripting with SWbemObject](scripting-with-swbemobject.md) and [Scripting Helper Objects](scripting-helper-objects.md).</span></span>

## <a name="using-wmi-and-a-scripting-language-how-do-i"></a><span data-ttu-id="870bb-131">使用 WMI 和指令碼語言，如何 .。。</span><span class="sxs-lookup"><span data-stu-id="870bb-131">Using WMI and a Scripting Language, How Do I...</span></span>

<dl> <dt>

<span data-ttu-id="870bb-132"><span id="...connect_to_WMI_"></span><span id="...connect_to_wmi_"></span><span id="...CONNECT_TO_WMI_"></span>...連接到 WMI？</span><span class="sxs-lookup"><span data-stu-id="870bb-132"><span id="...connect_to_WMI_"></span><span id="...connect_to_wmi_"></span><span id="...CONNECT_TO_WMI_"></span>...connect to WMI?</span></span>
</dt> <dd>

<span data-ttu-id="870bb-133">若為 VBScript 和適用于 WMI 的腳本 API，請使用具有標記的 [**SWbemServices**](swbemservices.md) 物件和對 [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_))的呼叫來取出。</span><span class="sxs-lookup"><span data-stu-id="870bb-133">For VBScript and the Scripting API for WMI, retrieve an [**SWbemServices**](swbemservices.md) object with a moniker and a call to [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)).</span></span> <span data-ttu-id="870bb-134">或者，您也可以呼叫 [**wbemscripting.swbemlocator. ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)來連接到伺服器。</span><span class="sxs-lookup"><span data-stu-id="870bb-134">Alternately, you can connect to the server with a call to [**SWbemLocator.ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span> <span data-ttu-id="870bb-135">然後，您可以使用物件來存取特定的 WMI 命名空間或 WMI 類別實例。</span><span class="sxs-lookup"><span data-stu-id="870bb-135">You can then use the object to access a specific WMI namespace or WMI class instance.</span></span>

<span data-ttu-id="870bb-136">針對 PowerShell，連線至 WMI 通常會直接在 Cmdlet 呼叫中執行;因此，不需要額外的步驟。</span><span class="sxs-lookup"><span data-stu-id="870bb-136">For PowerShell, connecting to WMI is generally done directly in the cmdlet call; as such, no additional steps are necessary.</span></span>

<span data-ttu-id="870bb-137">如需詳細資訊，請參閱 [描述 WMI 物件的位置](describing-the-location-of-a-wmi-object.md)、 [建立標記字串](constructing-a-moniker-string.md)，以及 [使用 VBScript 連接至 WMI](connecting-to-wmi-with-vbscript.md)。</span><span class="sxs-lookup"><span data-stu-id="870bb-137">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md), [Constructing a Moniker String](constructing-a-moniker-string.md), and [Connecting to WMI with VBScript](connecting-to-wmi-with-vbscript.md).</span></span>


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer(".", "root\cimv2")

' Second example: implicitly uses the local compuer (.) and default namespace ("root\cimv2")
Set objWMIService = GetObject("winmgmts:")
```


```PowerShell

#Already has all the defaults set
get-WmiObject Win32_LogicalDisk

#Or, to be explicit,
get-WmiObject -class Win32_LogicalDisk -Computer &quot;.&quot; -Namespace &quot;root\cimv2&quot; -Impersonation Impersonate
```





</dd> <dt>

<span data-ttu-id="870bb-138"><span id="...retrieve_information_from_WMI_"></span><span id="...retrieve_information_from_wmi_"></span><span id="...RETRIEVE_INFORMATION_FROM_WMI_"></span>...從 WMI 取出資訊？</span><span class="sxs-lookup"><span data-stu-id="870bb-138"><span id="...retrieve_information_from_WMI_"></span><span id="...retrieve_information_from_wmi_"></span><span id="...RETRIEVE_INFORMATION_FROM_WMI_"></span>...retrieve information from WMI?</span></span>
</dt> <dd>

<span data-ttu-id="870bb-139">針對 VBScript 和適用于 WMI 的腳本 API，請使用抓取函式，例如 [**WbemServices. Get**](swbemservices-get.md) 或 [**WbemServices. InstancesOf**](swbemservices-instancesof.md)。</span><span class="sxs-lookup"><span data-stu-id="870bb-139">For VBScript and the Scripting API for WMI, use a retrieval function, such as [**WbemServices.Get**](swbemservices-get.md) or [**WbemServices.InstancesOf**](swbemservices-instancesof.md).</span></span> <span data-ttu-id="870bb-140">您也可以放置物件的類別名稱，以便在標記中取得，這可能更有效率。</span><span class="sxs-lookup"><span data-stu-id="870bb-140">You may also place the class name of the object to retrieve in a moniker, which may be more efficient.</span></span>

<span data-ttu-id="870bb-141">針對 PowerShell，請使用 *-Class* 參數。</span><span class="sxs-lookup"><span data-stu-id="870bb-141">For PowerShell, use the *-Class* parameter.</span></span> <span data-ttu-id="870bb-142">請注意，-Class 是預設參數;因此，您不需要明確陳述。</span><span class="sxs-lookup"><span data-stu-id="870bb-142">Note that -Class is the default parameter; as such, you don't need to explicitly state it.</span></span>

<span data-ttu-id="870bb-143">如需詳細資訊，請參閱抓取 [WMI 類別或實例資料](retrieving-class-or-instance-data.md)。</span><span class="sxs-lookup"><span data-stu-id="870bb-143">For more information, see [Retrieving WMI Class or Instance Data](retrieving-class-or-instance-data.md).</span></span>


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer(".", "root\cimv2")
Set colScheduledJobs = objService.InstancesOf("Win32_ScheduledJob")

' Second example
SSet Service = GetObject("WinMgmts:{impersonationLevel=impersonate}!Win32_Service=""ALERTER""")
```


```PowerShell

#default - you don't actually need to use the -Class parameter
Get-WMIObject Win32_WmiSetting

#but you can if you want to
Get-WMIObject -Class Win32_WmiSetting
```





</dd> <dt>

<span data-ttu-id="870bb-144"><span id="...create_a_WMI_query_"></span><span id="...create_a_wmi_query_"></span><span id="...CREATE_A_WMI_QUERY_"></span>...建立 WMI 查詢？</span><span class="sxs-lookup"><span data-stu-id="870bb-144"><span id="...create_a_WMI_query_"></span><span id="...create_a_wmi_query_"></span><span id="...CREATE_A_WMI_QUERY_"></span>...create a WMI query?</span></span>
</dt> <dd>

<span data-ttu-id="870bb-145">針對 VBScript 和適用于 WMI 的腳本 API，請使用 [**SWbemServices.ExecQuery**](swbemservices-execquery.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="870bb-145">For VBScript and the Scripting API for WMI, use the [**SWbemServices.ExecQuery**](swbemservices-execquery.md) method.</span></span>

<span data-ttu-id="870bb-146">針對 PowerShell，請使用 *-Query* 參數。</span><span class="sxs-lookup"><span data-stu-id="870bb-146">For PowerShell, use the *-Query* parameter.</span></span> <span data-ttu-id="870bb-147">您也可以使用 *-filter* 參數進行篩選。</span><span class="sxs-lookup"><span data-stu-id="870bb-147">You can also filter using the *-Filter* parameter.</span></span>

<span data-ttu-id="870bb-148">如需詳細資訊，請參閱 [查詢 WMI](querying-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="870bb-148">For more information, see [Querying WMI](querying-wmi.md).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colScheduledJobs = objWMIService.ExecQuery("Select * from Win32_ScheduledJob")
For Each objJob in colScheduledJobs
    Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine
```


```PowerShell

Get-WmiObject -query &quot;SELECT * FROM Win32_logicalDisk WHERE DeviceID = 'C:'&quot;

#or

get-wmiObject -Class Win32_LogicalDisk -Filter &quot;DeviceID = &#39;C:&#39;&quot;
```





</dd> <dt>

<span data-ttu-id="870bb-149"><span id="...enumerate_through_a_list_of_WMI_objects_"></span><span id="...enumerate_through_a_list_of_wmi_objects_"></span><span id="...ENUMERATE_THROUGH_A_LIST_OF_WMI_OBJECTS_"></span>...列舉 WMI 物件清單嗎？</span><span class="sxs-lookup"><span data-stu-id="870bb-149"><span id="...enumerate_through_a_list_of_WMI_objects_"></span><span id="...enumerate_through_a_list_of_wmi_objects_"></span><span id="...ENUMERATE_THROUGH_A_LIST_OF_WMI_OBJECTS_"></span>...enumerate through a list of WMI objects?</span></span>
</dt> <dd>

<span data-ttu-id="870bb-150">針對 VBScript 和適用于 WMI 的腳本 API，請使用 [**swbemobjectset 搭配使用**](swbemobjectset.md) 容器物件，該物件在腳本中會被視為可列舉的集合。</span><span class="sxs-lookup"><span data-stu-id="870bb-150">For VBScript and the Scripting API for WMI, use the [**SWbemObjectSet**](swbemobjectset.md) container object, which is treated in script as a collection that can be enumerated.</span></span> <span data-ttu-id="870bb-151">您可以從 [**SWbemServices. InstancesOf**](swbemservices-instancesof.md)或 [**SWbemServices.ExecQuery**](swbemservices-execquery.md)的呼叫取出 **swbemobjectset 搭配使用**。</span><span class="sxs-lookup"><span data-stu-id="870bb-151">You can retrieve an **SWbemObjectSet** from a call from [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) or [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span>

<span data-ttu-id="870bb-152">PowerShell 可以像處理任何其他物件一樣，取得和處理列舉;WMI 沒有什麼特別唯一的。</span><span class="sxs-lookup"><span data-stu-id="870bb-152">PowerShell is able to retrieve and handle enumerations as it would any other object; there is nothing particularly unique to WMI.</span></span>

<span data-ttu-id="870bb-153">如需詳細資訊，請參閱 [存取集合](accessing-a-collection.md)。</span><span class="sxs-lookup"><span data-stu-id="870bb-153">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>


```VB
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDevice")
```


```PowerShell

$logicalDevices = Get-WmiObject CIM_LogicalDevice
foreach ($device in $logicalDevices)
{
    $device.name
}

#or, to be more compact

Get-WmiObject cim_logicalDevice | ForEach-Object { $_.name }

```





</dd> <dt>

<span data-ttu-id="870bb-154"><span id="...access_a_different_WMI_namespace_"></span><span id="...access_a_different_wmi_namespace_"></span><span id="...ACCESS_A_DIFFERENT_WMI_NAMESPACE_"></span>...存取不同的 WMI 命名空間？</span><span class="sxs-lookup"><span data-stu-id="870bb-154"><span id="...access_a_different_WMI_namespace_"></span><span id="...access_a_different_wmi_namespace_"></span><span id="...ACCESS_A_DIFFERENT_WMI_NAMESPACE_"></span>...access a different WMI namespace?</span></span>
</dt> <dd>

<span data-ttu-id="870bb-155">若為 VBScript 和適用于 WMI 的腳本 API，請在 [標記] 中陳述命名空間，否則您可以在 [**wbemscripting.swbemlocator**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)的呼叫中明確陳述命名空間。</span><span class="sxs-lookup"><span data-stu-id="870bb-155">For VBScript and the Scripting API for WMI, state the namespace in the moniker, or else you can explicitly state the namespace in the call to [**SwbemLocator.ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span>

<span data-ttu-id="870bb-156">針對 PowerShell，請使用 *-Namespace* 參數。</span><span class="sxs-lookup"><span data-stu-id="870bb-156">For PowerShell, use the *-Namespace* parameter.</span></span> <span data-ttu-id="870bb-157">預設命名空間是「根 \\ cimV2」; 不過，許多較舊的類別會儲存為「根 \\ 預設值」。</span><span class="sxs-lookup"><span data-stu-id="870bb-157">The default namespace is "root\\cimV2"; however, many older classes are stored in "root\\default".</span></span>

<span data-ttu-id="870bb-158">若要尋找指定 WMI 類別的位置，請查看參考頁面。</span><span class="sxs-lookup"><span data-stu-id="870bb-158">To find the location of a given WMI class, look at the reference page.</span></span> <span data-ttu-id="870bb-159">或者，您也可以使用 >get-wmiobject 手動探索命名空間。</span><span class="sxs-lookup"><span data-stu-id="870bb-159">Alternately, you can manually explore a namespace using get-WmiObject.</span></span>


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer(".", "root\cimv2")

' Second example
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & "." & "\root\cimv2")
```


```PowerShell

Get-WmiObject -list * -Namespace root\default

#or, to retrieve all namespaces,
Get-WmiObject -Namespace root -Class __Namespace
```





</dd> <dt>

<span data-ttu-id="870bb-160"><span id="...retrieve_all_child_instances_of_a_class_"></span><span id="...RETRIEVE_ALL_CHILD_INSTANCES_OF_A_CLASS_"></span>...取出類別的所有子實例？</span><span class="sxs-lookup"><span data-stu-id="870bb-160"><span id="...retrieve_all_child_instances_of_a_class_"></span><span id="...RETRIEVE_ALL_CHILD_INSTANCES_OF_A_CLASS_"></span>...retrieve all child instances of a class?</span></span>
</dt> <dd>

<span data-ttu-id="870bb-161">針對直接針對 WMI 和 PowerShell 使用腳本 API 的語言，WMI 支援抓取基類的子類別。</span><span class="sxs-lookup"><span data-stu-id="870bb-161">For languages that directly use the Scripting API for WMI and PowerShell, WMI supports retrieving the child classes of a base class.</span></span> <span data-ttu-id="870bb-162">因此，為了抓取子實例，您只需要搜尋父類別。</span><span class="sxs-lookup"><span data-stu-id="870bb-162">As such, in order to retrieve the child instances, you need to only search for the parent class.</span></span> <span data-ttu-id="870bb-163">下列範例會搜尋 [**CIM \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/cim-logicaldisk)，這是預先安裝的 WMI 類別，代表 Windows 電腦系統上的邏輯磁片。</span><span class="sxs-lookup"><span data-stu-id="870bb-163">The following example searches for [**CIM\_LogicalDisk**](/windows/desktop/CIMWin32Prov/cim-logicaldisk), which is a preinstalled WMI class that represents logical disks on a Windows-based computer system.</span></span> <span data-ttu-id="870bb-164">因此，搜尋這個父類別也會傳回 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)的實例，這是 Windows 用來描述硬碟的實例。</span><span class="sxs-lookup"><span data-stu-id="870bb-164">As such, searching for this parent class also returns instances of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), which is what Windows uses to describe hard drives.</span></span> <span data-ttu-id="870bb-165">如需詳細資訊，請參閱 [通用訊息模型](common-information-model.md)。</span><span class="sxs-lookup"><span data-stu-id="870bb-165">For more information, see [Common Information Model](common-information-model.md).</span></span> <span data-ttu-id="870bb-166">WMI 提供這類預先安裝類別的完整架構，可讓您存取和控制受管理的物件。</span><span class="sxs-lookup"><span data-stu-id="870bb-166">WMI supplies an entire schema of such preinstalled classes that allow you to access and control managed objects.</span></span> <span data-ttu-id="870bb-167">如需詳細資訊，請參閱 [Win32 類別](/windows/desktop/CIMWin32Prov/win32-provider) 和 [WMI 類別](wmi-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="870bb-167">For more information, see [Win32 Classes](/windows/desktop/CIMWin32Prov/win32-provider) and [WMI Classes](wmi-classes.md)..</span></span>


```VB
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")
  WScript.Echo "Instance:", Disk.Name
```




```PowerShell
Get-WmiObject CIM_LogicalDisk | ForEach-Object { "Instance: " + $_.Name  }
```



</dd> <dt>

<span data-ttu-id="870bb-168"><span id="...locate_a_WMI_object_"></span><span id="...locate_a_wmi_object_"></span><span id="...LOCATE_A_WMI_OBJECT_"></span>...找出 WMI 物件？</span><span class="sxs-lookup"><span data-stu-id="870bb-168"><span id="...locate_a_WMI_object_"></span><span id="...locate_a_wmi_object_"></span><span id="...LOCATE_A_WMI_OBJECT_"></span>...locate a WMI object?</span></span>
</dt> <dd>

<span data-ttu-id="870bb-169">針對 WMI 和 PowerShell 的腳本 API，WMI 會使用命名空間、類別名稱和索引鍵屬性的組合，來唯一識別指定的 WMI 實例。</span><span class="sxs-lookup"><span data-stu-id="870bb-169">For both the Scripting API for WMI and PowerShell, WMI uses a combination of namespace, class name, and key properties to uniquely identify a given WMI instance.</span></span> <span data-ttu-id="870bb-170">這就是所謂的 WMI 物件路徑。</span><span class="sxs-lookup"><span data-stu-id="870bb-170">Together, this is known as the WMI object path.</span></span> <span data-ttu-id="870bb-171">對於 VBScript 而言， [**SWbemObject \_**](swbemobject-path-.md)屬性會描述腳本 API 所傳回之任何指定物件的路徑。</span><span class="sxs-lookup"><span data-stu-id="870bb-171">For VBScript, the [**SWbemObject.Path\_**](swbemobject-path-.md) property describes the path for any given object returned by the scripting API.</span></span> <span data-ttu-id="870bb-172">針對 PowerShell，每個 WMI 物件都會有一個 \_ \_ PATH 屬性。</span><span class="sxs-lookup"><span data-stu-id="870bb-172">For PowerShell, every WMI object will have a \_\_PATH property.</span></span> <span data-ttu-id="870bb-173">如需詳細資訊，請參閱[描述 WMI 物件的位置](describing-the-location-of-a-wmi-object.md)。</span><span class="sxs-lookup"><span data-stu-id="870bb-173">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md)</span></span>

<span data-ttu-id="870bb-174">除了命名空間和類別名稱之外，WMI 物件也會有一個索引鍵屬性，它可唯一識別該實例與您電腦上的其他實例的比較。</span><span class="sxs-lookup"><span data-stu-id="870bb-174">In addition to namespace and class name, a WMI object will also have a key property, which uniquely identifies that instance compared to other instances on your machine.</span></span> <span data-ttu-id="870bb-175">例如， **DeviceID** 屬性是 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別的索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="870bb-175">For example, the **DeviceID** property is the key property for the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span> <span data-ttu-id="870bb-176">如需詳細資訊，請參閱 [受控物件格式 (MOF) ](managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="870bb-176">For more information, see [Managed Object Format (MOF)](managed-object-format--mof-.md).</span></span>

<span data-ttu-id="870bb-177">最後，相對路徑只是路徑的縮寫形式，並且包含類別名稱和金鑰值。</span><span class="sxs-lookup"><span data-stu-id="870bb-177">Finally, the Relative path is simply a shortened form of the path, and includes the class name and key value.</span></span> <span data-ttu-id="870bb-178">在下列範例中，路徑可能是 " \\ \\ computerName \\ Root \\ Cimv2： Win32 \_ LogicalDisk DeviceID =" d： ""，而相對路徑則是 "" Win32LogicalDisk. deviceid = "D" ""。</span><span class="sxs-lookup"><span data-stu-id="870bb-178">In the examples below, the path may be "\\\\computerName\\root\\cimv2:Win32\_LogicalDisk.DeviceID="D:"", while the relative path would be ""Win32LogicalDisk.DeviceID="D""".</span></span>


```VB
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")
  WScript.Echo "Instance:", Disk.Path_.Relpath

'or to get the path
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")
  WScript.Echo "Instance:", Disk.Path_
```




```PowerShell
#retrieving the path
Get-WmiObject CIM_LogicalDisk | ForEach-Object { "Instance: " + $_.__PATH  }

#retrieving the relative path
Get-WmiObject CIM_LogicalDisk | ForEach-Object { "Instance: " + $_.__RELPATH  }
```



</dd> <dt>

<span data-ttu-id="870bb-179"><span id="...set_information_in_WMI_"></span><span id="...set_information_in_wmi_"></span><span id="...SET_INFORMATION_IN_WMI_"></span>...設定 WMI 中的資訊？</span><span class="sxs-lookup"><span data-stu-id="870bb-179"><span id="...set_information_in_WMI_"></span><span id="...set_information_in_wmi_"></span><span id="...SET_INFORMATION_IN_WMI_"></span>...set information in WMI?</span></span>
</dt> <dd>

<span data-ttu-id="870bb-180">針對 VBScript 和適用于 WMI 的腳本 API，請使用 [**SWbemObject. \_ Put**](swbemobject-put-.md)方法。</span><span class="sxs-lookup"><span data-stu-id="870bb-180">For VBScript and the Scripting API for WMI, use the [**SWbemObject.Put\_**](swbemobject-put-.md) method.</span></span>

<span data-ttu-id="870bb-181">針對 PowerShell，您可以使用 Put 方法，或 [設定-set-wmiinstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true)。</span><span class="sxs-lookup"><span data-stu-id="870bb-181">For PowerShell, you can either use the Put method, or else [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true).</span></span>

<span data-ttu-id="870bb-182">如需詳細資訊，請參閱 [修改實例屬性](modifying-an-instance-property.md)。</span><span class="sxs-lookup"><span data-stu-id="870bb-182">For more information, see [Modifying an Instance Property](modifying-an-instance-property.md).</span></span>


```VB
wbemCimtypeString = 8
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' String property
objClass.Properties_.add "PropertyName", wbemCimtypeString  
' Make the property a key property 
objClass.Properties_("PropertyName").Qualifiers_.add "key", true

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
WScript.Echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject("Winmgmts:root\default:NewClass").Spawninstance_

objNewInst.PropertyName = "My Instance"

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
WScript.Echo objInstancePath.Path
```


```PowerShell

$mySettings = get-WMIObject Win32_WmiSetting
$mySettings.LoggingLevel = 1
$mySettings.Put()

#or

Set-WMIInstance -class Win32_WMISetting -argument @{LoggingLevel=1}
```





</dd> <dt>

<span data-ttu-id="870bb-183"><span id="...use_different_credentials_"></span><span id="...USE_DIFFERENT_CREDENTIALS_"></span>...使用不同的認證？</span><span class="sxs-lookup"><span data-stu-id="870bb-183"><span id="...use_different_credentials_"></span><span id="...USE_DIFFERENT_CREDENTIALS_"></span>...use different credentials?</span></span>
</dt> <dd>

<span data-ttu-id="870bb-184">針對 VBScript 和適用于 WMI 的腳本 API，請使用 [**wbemscripting.swbemlocator. ConnectServer**](swbemlocator-connectserver.md)方法中的使用者 *名稱* 和 *密碼* 參數。</span><span class="sxs-lookup"><span data-stu-id="870bb-184">For VBScript and the Scripting API for WMI, use the *UserName* and *Password* parameters in the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method.</span></span>

<span data-ttu-id="870bb-185">針對 PowerShell，請使用 *-Credential* 參數。</span><span class="sxs-lookup"><span data-stu-id="870bb-185">For PowerShell, use the *-Credential* parameter.</span></span>

<span data-ttu-id="870bb-186">請注意，您只能在遠端系統上使用替代認證。</span><span class="sxs-lookup"><span data-stu-id="870bb-186">Note that you can only use alternate credentials on a remote system.</span></span> <span data-ttu-id="870bb-187">如需詳細資訊，請參閱 [保護腳本用戶端](securing-scripting-clients.md)。</span><span class="sxs-lookup"><span data-stu-id="870bb-187">For more information, see [Securing Scripting Clients](securing-scripting-clients.md).</span></span>


```VB
strComputer = "remoteComputerName" 
strDomain = "DOMAIN" 
Wscript.StdOut.Write "Please enter your user name:"
strUser = Wscript.StdIn.ReadLine 
Set objPassword = CreateObject("ScriptPW.Password")
Wscript.StdOut.Write "Please enter your password:"
strPassword = objPassword.GetPassword()
 
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, _
                                                     "Root\CIMv2", _
                                                     strUser, _
                                                     strPassword, _
                                                     "MS_409", _
                                                     "ntlmdomain:" + strDomain)
Set colSwbemObjectSet = objSWbemServices.ExecQuery("Select * From Win32_Process")
For Each objProcess in colSWbemObjectSet
    Wscript.Echo "Process Name: " & objProcess.Name 
Next
```


```PowerShell

$Computer = &quot;atl-dc-01&quot;

Get-WmiObject -Namespace &quot;root\cimv2&quot; -Class Win32_Process -Credential FABRIKAM\administrator  `
-ComputerName $Computer
```





</dd> <dt>

<span data-ttu-id="870bb-188"><span id="...access_a_remote_computer_"></span><span id="...ACCESS_A_REMOTE_COMPUTER_"></span>...要存取遠端電腦嗎？</span><span class="sxs-lookup"><span data-stu-id="870bb-188"><span id="...access_a_remote_computer_"></span><span id="...ACCESS_A_REMOTE_COMPUTER_"></span>...access a remote computer?</span></span>
</dt> <dd>

<span data-ttu-id="870bb-189">若為 VBScript 和適用于 WMI 的腳本 API，請明確地在 [**wbemscripting.swbemlocator. ConnectServer**](swbemlocator-connectserver.md)的呼叫中陳述電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="870bb-189">For VBScript and the Scripting API for WMI, explicitly state the name of the computer in either the moniker, or else in the call to [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md).</span></span> <span data-ttu-id="870bb-190">如需詳細資訊，請參閱 [使用 VBScript 從遠端連線到 WMI](connecting-to-wmi-remotely-with-vbscript.md)。</span><span class="sxs-lookup"><span data-stu-id="870bb-190">For more information, see [Connecting to WMI Remotely with VBScript](connecting-to-wmi-remotely-with-vbscript.md).</span></span>

<span data-ttu-id="870bb-191">針對 PowerShell，使用 *-ComputerName* 參數。</span><span class="sxs-lookup"><span data-stu-id="870bb-191">For PowerShell, use the *-ComputerName* parameter.</span></span> <span data-ttu-id="870bb-192">如需詳細資訊，請參閱 [使用 PowerShell 從遠端連線到 WMI](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)。</span><span class="sxs-lookup"><span data-stu-id="870bb-192">For more information, see [Connecting to WMI Remotely with PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md).</span></span>


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer("myRemoteServerName", "root\cimv2")
Set colScheduledJobs = objService.ExecQuery("SELECT * FROM Win32_ScheduledJob")
For Each objJob in colScheduledJobs
    Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine

'example 2

strComputer = "myRemoteServerName"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colScheduledJobs = objWMIService.ExecQuery("Select * from Win32_ScheduledJob")
For Each objJob in colScheduledJobs
    Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine
```


```PowerShell

$Computer = &quot;atl-dc-01&quot;

Get-WmiObject -Namespace &quot;root\cimv2&quot; -Class Win32_logicalDisk -ComputerName $Computer
```





</dd> <dt>

<span data-ttu-id="870bb-193"><span id="...set_the_Authentication_and_Impersonation_levels_"></span><span id="...set_the_authentication_and_impersonation_levels_"></span><span id="...SET_THE_AUTHENTICATION_AND_IMPERSONATION_LEVELS_"></span>...要設定驗證和模擬層級嗎？</span><span class="sxs-lookup"><span data-stu-id="870bb-193"><span id="...set_the_Authentication_and_Impersonation_levels_"></span><span id="...set_the_authentication_and_impersonation_levels_"></span><span id="...SET_THE_AUTHENTICATION_AND_IMPERSONATION_LEVELS_"></span>...set the Authentication and Impersonation levels?</span></span>
</dt> <dd>

<span data-ttu-id="870bb-194">若為 VBScript 和適用于 WMI 的腳本 API，請在傳回的伺服器物件上使用 [**SWbemServices \_**](swbemlocator-security-.md)屬性，否則請在 [名字] 中設定相關的值。</span><span class="sxs-lookup"><span data-stu-id="870bb-194">For VBScript and the Scripting API for WMI, use the [**SWbemServices.Security\_**](swbemlocator-security-.md) property on the returned server object, or else set the relevant values in the moniker.</span></span>

<span data-ttu-id="870bb-195">針對 PowerShell，請分別使用 *-驗證* 和 *-* 模擬參數。</span><span class="sxs-lookup"><span data-stu-id="870bb-195">For PowerShell, use the *-Authentication* and *-Impersonation* parameters, respectively.</span></span> <span data-ttu-id="870bb-196">如需詳細資訊，請參閱 [保護腳本用戶端](securing-scripting-clients.md)。</span><span class="sxs-lookup"><span data-stu-id="870bb-196">For more information, see [Securing Scripting Clients](securing-scripting-clients.md).</span></span>

<span data-ttu-id="870bb-197">如需詳細資訊，請參閱 [保護腳本用戶端](securing-scripting-clients.md)。</span><span class="sxs-lookup"><span data-stu-id="870bb-197">For more information, see [Securing Scripting Clients](securing-scripting-clients.md).</span></span>


```VB
' First example
Set Service = GetObject("WinMgmts:{impersonationLevel=impersonate}!Win32_Service=""ALERTER""")

' Second example
Set Locator = CreateObject("WbemScripting.SWbemLocator")
Set Service = Locator.ConnectServer       
service.Security_.ImpersonationLevel = wbemImpersonationLevelImpersonate  
Set objinstance = Service.Get("Win32_Service=""ALERTER""")
```


```PowerShell

$Computer = &quot;atl-dc-01&quot;

Get-WmiObject -Namespace &quot;root\cimv2&quot; -Class Win32_Process -Impersonation Impersonate `
 -Authentication PacketIntegrity -Credential FABRIKAM\administrator -ComputerName $Computer
```





</dd> <dt>

<span data-ttu-id="870bb-198"><span id="...handle_errors_in_WMI_"></span><span id="...handle_errors_in_wmi_"></span><span id="...HANDLE_ERRORS_IN_WMI_"></span>...處理 WMI 中的錯誤？</span><span class="sxs-lookup"><span data-stu-id="870bb-198"><span id="...handle_errors_in_WMI_"></span><span id="...handle_errors_in_wmi_"></span><span id="...HANDLE_ERRORS_IN_WMI_"></span>...handle errors in WMI?</span></span>
</dt> <dd>

<span data-ttu-id="870bb-199">針對 WMI 的腳本 API，提供者可能會提供 [**SWbemLastError**](swbemlasterror.md) 物件，以提供有關錯誤的進一步資訊。</span><span class="sxs-lookup"><span data-stu-id="870bb-199">For the Scripting API for WMI, the provider may supply an [**SWbemLastError**](swbemlasterror.md) object to give further information on an error.</span></span>

<span data-ttu-id="870bb-200">尤其在 VBScript 中，使用原生 **Err** 物件也支援錯誤處理。</span><span class="sxs-lookup"><span data-stu-id="870bb-200">In VBScript in particular, error handling is also supported using the native **Err** object.</span></span> <span data-ttu-id="870bb-201">您也可以如上面所述存取 [**SWbemLastError**](swbemlasterror.md)物件。</span><span class="sxs-lookup"><span data-stu-id="870bb-201">You may also access the [**SWbemLastError**](swbemlasterror.md)object, as described above.</span></span> <span data-ttu-id="870bb-202">如需詳細資訊，請參閱 [取出錯誤碼](retrieving-an-error-code.md)。</span><span class="sxs-lookup"><span data-stu-id="870bb-202">For more information, see [Retrieving an Error Code](retrieving-an-error-code.md).</span></span>

<span data-ttu-id="870bb-203">針對 PowerShell，您可以使用標準 PowerShell 錯誤處理技術。</span><span class="sxs-lookup"><span data-stu-id="870bb-203">For PowerShell, you can use the standard PowerShell error handling techniques.</span></span> <span data-ttu-id="870bb-204">如需詳細資訊，請參閱 [PowerShell 中的錯誤處理簡介](/archive/blogs/kebab/an-introduction-to-error-handling-in-powershell)。</span><span class="sxs-lookup"><span data-stu-id="870bb-204">For more information, see [An Introduction to Error Handling in PowerShell](/archive/blogs/kebab/an-introduction-to-error-handling-in-powershell).</span></span>


```VB
'using Err
On Error Resume Next
Set objProcess = GetObject("winmgmts:root\cimv2:Win32_Process.Handle='one'")
Wscript.Echo Err.Number

'using SWbemLastError

On Error Resume Next
Set obj = GetObject("winmgmts:root\cimv2:Win32_Process.Handle='one'")
Set LastError = createobject("wbemscripting.swbemlasterror")
Wscript.Echo "Operation = " & LastError.operation & VBCRLF & "ParameterInfo = " _
            & LastError.ParameterInfo & VBCRLF & "ProviderName = " & LastError.ProviderName
```



</dd> </dl>

 

 

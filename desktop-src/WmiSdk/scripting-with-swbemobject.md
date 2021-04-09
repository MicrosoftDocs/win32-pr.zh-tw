---
description: SWbemObject 腳本物件是一般的 WMI 物件，定義可使用的屬性和方法，不論 SWbemObject 物件系結的特定 WMI 物件為何。
ms.assetid: 33252b49-00d4-4c43-8abe-9368ed82f34b
ms.tgt_platform: multiple
title: 使用 SWbemObject 編寫腳本
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3ce9a48779b13f1b1917ad189b2297b60329ba04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114892"
---
# <a name="scripting-with-swbemobject"></a><span data-ttu-id="4cbe8-103">使用 SWbemObject 編寫腳本</span><span class="sxs-lookup"><span data-stu-id="4cbe8-103">Scripting with SWbemObject</span></span>

<span data-ttu-id="4cbe8-104">[**SWbemObject**](swbemobject.md)腳本物件是一般的 wmi 物件，定義可使用的屬性和方法，不論 **SWbemObject** 物件系結的特定 WMI 物件為何。</span><span class="sxs-lookup"><span data-stu-id="4cbe8-104">The [**SWbemObject**](swbemobject.md) scripting object is the generic WMI object, defining properties and methods that can be used regardless of the specific WMI object to which the **SWbemObject** object is bound.</span></span> <span data-ttu-id="4cbe8-105">所有 WMI 物件（例如 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process) 或任何其他 wmi 資料類別的實例）都會以 [**SWbemObject**](swbemobject.md) 表示，而且除了各自的特定屬性和方法之外，還可以使用 **SWbemObject** 的通用屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="4cbe8-105">All WMI objects, such as an instance of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) or any other WMI data class, are represented by [**SWbemObject**](swbemobject.md) and can use the **SWbemObject** common properties and methods in addition to their own particular properties and methods.</span></span>

<span data-ttu-id="4cbe8-106">例如，您可以使用下列腳本，藉由呼叫 [**SWbemObject 實例 \_**](swbemobject-instances-.md)方法來取得 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process)的所有實例。</span><span class="sxs-lookup"><span data-stu-id="4cbe8-106">For example, use the following script to obtain all of the instances of a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) by calling the [**SWbemObject.Instances\_**](swbemobject-instances-.md) method.</span></span> <span data-ttu-id="4cbe8-107">ClsobjProcess 同時代表 **Win32 \_ 進程** 類別定義和 [**SWbemObject**](swbemobject.md)。</span><span class="sxs-lookup"><span data-stu-id="4cbe8-107">The clsobjProcess represents both the **Win32\_Process** class definition and an [**SWbemObject**](swbemobject.md).</span></span>


```VB
strComputer = "."
Set objWMIServices = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set clsobjProcess = objWMIServices.Get("Win32_Process")
Set colProcesses = clsobjProcess.Instances_()
For Each Process in colProcesses
    WScript.Echo Process.Name
Next
```



<span data-ttu-id="4cbe8-108">下列範例會取得代表警報器服務的特定 [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service) 實例，並將其儲存在 objAlerter 中。</span><span class="sxs-lookup"><span data-stu-id="4cbe8-108">The following example obtains a specific instance of [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) that represents the Alerter service and stores it in objAlerter.</span></span> <span data-ttu-id="4cbe8-109">然後，您可以呼叫 [**SWbemObject**](swbemobject.md) 方法，例如 Wscript.echo. echo ObjAlerter. Path \_ 或資料類別所定義的方法，例如 Wscript.echo. Echo objAlerter. State。</span><span class="sxs-lookup"><span data-stu-id="4cbe8-109">You can then call either [**SWbemObject**](swbemobject.md) methods, such as WScript.Echo objAlerter.Path\_, or methods defined by the data class, such as WScript.Echo objAlerter.State.</span></span> <span data-ttu-id="4cbe8-110">objAlerter，代表 Win32 服務的實例 \_ 和 **SWbemObject**。</span><span class="sxs-lookup"><span data-stu-id="4cbe8-110">objAlerter which represents both an instance of Win32\_Service and an **SWbemObject**.</span></span>


```VB
strComputer = "." 
Set objWMIServices = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set objAlerter = objWMIServices.Get("Win32_Service.Name='Alerter'")
WScript.Echo objAlerter.Path_
objAlerter.StopService()
WScript.Echo objAlerter.State
```




```VB
For each Prop in myObject.Properties_
    Wscript.Echo Prop.Name
Next
```



<span data-ttu-id="4cbe8-111">呼叫 [**SWbemObject \_**](swbemobject-instances-.md)時，會取得另一個泛型 WMI 腳本物件 [**swbemobjectset 搭配使用**](swbemobjectset.md)。</span><span class="sxs-lookup"><span data-stu-id="4cbe8-111">The call to [**SWbemObject.Instances\_**](swbemobject-instances-.md) obtains another generic WMI scripting object, [**SWbemObjectSet**](swbemobjectset.md).</span></span> <span data-ttu-id="4cbe8-112">如所示， **swbemobjectset 搭配使用** 物件可視為 [集合](accessing-a-collection.md)。</span><span class="sxs-lookup"><span data-stu-id="4cbe8-112">As shown, the **SWbemObjectSet** object can be treated as a [collection](accessing-a-collection.md).</span></span>


```VB
Set clsobjProcess = objWMIServices.Get("Win32_Process")
```



<span data-ttu-id="4cbe8-113">您可以識別 [**SWbemObject**](swbemobject.md)方法，因為它們的結尾都是底線 (\_) ，例如 [**SWbemObject \_ 實例**](swbemobject-instances-.md)。</span><span class="sxs-lookup"><span data-stu-id="4cbe8-113">You can identify the [**SWbemObject**](swbemobject.md) methods because they all end with an underscore (\_), for example, [**SWbemObject.Instances\_**](swbemobject-instances-.md).</span></span>

<span data-ttu-id="4cbe8-114">[**SWbemObjectEx**](swbemobjectex.md) 會擴充 [**SWbemObject**](swbemobject.md)的屬性。</span><span class="sxs-lookup"><span data-stu-id="4cbe8-114">[**SWbemObjectEx**](swbemobjectex.md) extends the properties of [**SWbemObject**](swbemobject.md).</span></span> <span data-ttu-id="4cbe8-115">例如，您現在可以藉由呼叫 [**\_ SWbemObjectEx**](swbemobjectex-refresh-.md)來更新任何 WMI 物件的資料，例如 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process)的實例。</span><span class="sxs-lookup"><span data-stu-id="4cbe8-115">For example, you can now update the data of any WMI object, such as an instance of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process), by a call to [**SWbemObjectEx.Refresh\_**](swbemobjectex-refresh-.md).</span></span>

<span data-ttu-id="4cbe8-116">下列範例顯示每五秒可重新整理系統進程分頁錯誤資料的方式。</span><span class="sxs-lookup"><span data-stu-id="4cbe8-116">The following example shows how the system process page fault data can be refreshed every five seconds.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2")
Set colProcesses = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'System'",,48) 
For Each Process in colProcesses
        i = 0
        Do Until i = 5
            i = i + 1
            Wscript.Echo "PageFaults = " & Process.PageFaults 
            Wscript.Sleep 10000
            Process.Refresh_
        Loop
Next
```



<span data-ttu-id="4cbe8-117">如需有關使用 [**SWbemRefresher**](swbemrefresher.md) 物件重新整理資料的詳細資訊，請參閱 [在腳本中重新整理 WMI 資料](refreshing-wmi-data-in-scripts.md)。</span><span class="sxs-lookup"><span data-stu-id="4cbe8-117">For more information about refreshing data using an [**SWbemRefresher**](swbemrefresher.md) object, see [Refreshing WMI Data in Scripts](refreshing-wmi-data-in-scripts.md).</span></span>

<span data-ttu-id="4cbe8-118">[**SWbemObject \_**](swbemobject-put-.md)和 [**PutAsync \_**](swbemobject-putasync-.md)可讓您將變更寫回任何 WMI 物件。</span><span class="sxs-lookup"><span data-stu-id="4cbe8-118">The [**SWbemObject.Put\_**](swbemobject-put-.md) and [**PutAsync\_**](swbemobject-putasync-.md) allow you to write changes back to any WMI object.</span></span> <span data-ttu-id="4cbe8-119">這些方法只會在建立物件的命名空間中，認可物件的變更。</span><span class="sxs-lookup"><span data-stu-id="4cbe8-119">These methods only commit changes to an object in the namespace where the object was created.</span></span> <span data-ttu-id="4cbe8-120">您可以使用 [**SWbemServicesEx 將**](swbemservicesex-put.md) 物件寫入至不同的命名空間，或使用 [**SWbemServicesEx. PutAsync**](swbemservicesex-putasync.md)。</span><span class="sxs-lookup"><span data-stu-id="4cbe8-120">You can write the object to a different namespace using [**SWbemServicesEx.Put**](swbemservicesex-put.md) or [**SWbemServicesEx.PutAsync**](swbemservicesex-putasync.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4cbe8-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="4cbe8-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4cbe8-122">適用于 WMI 的腳本 API</span><span class="sxs-lookup"><span data-stu-id="4cbe8-122">Scripting API for WMI</span></span>](scripting-api-for-wmi.md)
</dt> <dt>

[<span data-ttu-id="4cbe8-123">建立 WMI 腳本</span><span class="sxs-lookup"><span data-stu-id="4cbe8-123">Creating a WMI Script</span></span>](creating-a-wmi-script.md)
</dt> <dt>

[<span data-ttu-id="4cbe8-124">更新整個實例</span><span class="sxs-lookup"><span data-stu-id="4cbe8-124">Updating an Entire Instance</span></span>](updating-an-entire-instance.md)
</dt> <dt>

[<span data-ttu-id="4cbe8-125">呼叫方法</span><span class="sxs-lookup"><span data-stu-id="4cbe8-125">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 

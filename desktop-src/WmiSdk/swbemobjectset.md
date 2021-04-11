---
description: Swbemobjectset 搭配使用物件是 SWbemObject 物件的集合。 如需詳細資訊，請參閱存取集合。 VBScript CreateObject 呼叫無法建立這個物件。
ms.assetid: 00f5317e-eb8e-42f9-bada-963e11aadda4
ms.tgt_platform: multiple
title: 'Swbemobjectset 搭配使用物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet
- ISWbemObjectSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a6992658214d7ea5acbadbea396992edf0e3e9d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195038"
---
# <a name="swbemobjectset-object"></a><span data-ttu-id="726b9-105">Swbemobjectset 搭配使用物件</span><span class="sxs-lookup"><span data-stu-id="726b9-105">SWbemObjectSet object</span></span>

<span data-ttu-id="726b9-106">**Swbemobjectset 搭配使用** 物件是 [**SWbemObject**](swbemobject.md)物件的集合。</span><span class="sxs-lookup"><span data-stu-id="726b9-106">An **SWbemObjectSet** object is a collection of [**SWbemObject**](swbemobject.md) objects.</span></span> <span data-ttu-id="726b9-107">如需詳細資訊，請參閱 [存取集合](accessing-a-collection.md)。</span><span class="sxs-lookup"><span data-stu-id="726b9-107">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span> <span data-ttu-id="726b9-108">VBScript **CreateObject** 呼叫無法建立這個物件。</span><span class="sxs-lookup"><span data-stu-id="726b9-108">This object cannot be created by the VBScript **CreateObject** call.</span></span>

<span data-ttu-id="726b9-109">您可以藉由呼叫下列任何一種方法或其非同步對應來取得 **swbemobjectset 搭配使用** 物件：</span><span class="sxs-lookup"><span data-stu-id="726b9-109">You can get an **SWbemObjectSet** object by calling any of the following methods or their asynchronous equivalents:</span></span>

-   [<span data-ttu-id="726b9-110">**SWbemObject. Associators of\_**</span><span class="sxs-lookup"><span data-stu-id="726b9-110">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
-   [<span data-ttu-id="726b9-111">**SWbemObject 實例\_**</span><span class="sxs-lookup"><span data-stu-id="726b9-111">**SWbemObject.Instances\_**</span></span>](swbemobject-instances-.md)
-   [<span data-ttu-id="726b9-112">**SWbemObject 參考\_**</span><span class="sxs-lookup"><span data-stu-id="726b9-112">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
-   [<span data-ttu-id="726b9-113">**SWbemObject 子類別\_**</span><span class="sxs-lookup"><span data-stu-id="726b9-113">**SWbemObject.Subclasses\_**</span></span>](swbemobject-subclasses-.md)
-   [<span data-ttu-id="726b9-114">**SWbemServices. AssociatorsOf**</span><span class="sxs-lookup"><span data-stu-id="726b9-114">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
-   [<span data-ttu-id="726b9-115">**SWbemServices.ExecQuery**</span><span class="sxs-lookup"><span data-stu-id="726b9-115">**SWbemServices.ExecQuery**</span></span>](swbemservices-execquery.md)
-   [<span data-ttu-id="726b9-116">**SWbemServices. InstancesOf**</span><span class="sxs-lookup"><span data-stu-id="726b9-116">**SWbemServices.InstancesOf**</span></span>](swbemservices-instancesof.md)
-   [<span data-ttu-id="726b9-117">**SWbemServices. ReferencesTo**</span><span class="sxs-lookup"><span data-stu-id="726b9-117">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
-   [<span data-ttu-id="726b9-118">**SWbemServices. SubclassesOf**</span><span class="sxs-lookup"><span data-stu-id="726b9-118">**SWbemServices.SubclassesOf**</span></span>](swbemservices-subclassesof.md)

> [!Note]  
> <span data-ttu-id="726b9-119">**Swbemobjectset 搭配使用** 物件不支援選擇性的 **加入** 和 **移除** 收集方法。</span><span class="sxs-lookup"><span data-stu-id="726b9-119">The **SWbemObjectSet** object does not support the optional **Add** and **Remove** collection methods.</span></span>

 

> [!Note]  
> <span data-ttu-id="726b9-120">由於回呼的回呼可能不會與用戶端所需的驗證層級傳回，因此建議您使用 [半同步] 而非 [非同步通訊]。</span><span class="sxs-lookup"><span data-stu-id="726b9-120">Because the call-back to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="726b9-121">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="726b9-121">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

## <a name="members"></a><span data-ttu-id="726b9-122">成員</span><span class="sxs-lookup"><span data-stu-id="726b9-122">Members</span></span>

<span data-ttu-id="726b9-123">**Swbemobjectset 搭配使用** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="726b9-123">The **SWbemObjectSet** object has these types of members:</span></span>

-   [<span data-ttu-id="726b9-124">方法</span><span class="sxs-lookup"><span data-stu-id="726b9-124">Methods</span></span>](#methods)
-   [<span data-ttu-id="726b9-125">屬性</span><span class="sxs-lookup"><span data-stu-id="726b9-125">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="726b9-126">方法</span><span class="sxs-lookup"><span data-stu-id="726b9-126">Methods</span></span>

<span data-ttu-id="726b9-127">**Swbemobjectset 搭配使用** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="726b9-127">The **SWbemObjectSet** object has these methods.</span></span>



| <span data-ttu-id="726b9-128">方法</span><span class="sxs-lookup"><span data-stu-id="726b9-128">Method</span></span>                              | <span data-ttu-id="726b9-129">描述</span><span class="sxs-lookup"><span data-stu-id="726b9-129">Description</span></span>                                                                                                                      |
|:------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="726b9-130">**Item**</span><span class="sxs-lookup"><span data-stu-id="726b9-130">**Item**</span></span>](swbemobjectset-item.md) | <span data-ttu-id="726b9-131">從集合中捕獲 [**SWbemObject**](swbemobject.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="726b9-131">Retrieves an [**SWbemObject**](swbemobject.md) object from the collection.</span></span> <span data-ttu-id="726b9-132">這是物件的預設方法。</span><span class="sxs-lookup"><span data-stu-id="726b9-132">This is the default method of the object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="726b9-133">屬性</span><span class="sxs-lookup"><span data-stu-id="726b9-133">Properties</span></span>

<span data-ttu-id="726b9-134">**Swbemobjectset 搭配使用** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="726b9-134">The **SWbemObjectSet** object has these properties.</span></span>



| <span data-ttu-id="726b9-135">屬性</span><span class="sxs-lookup"><span data-stu-id="726b9-135">Property</span></span>                                                  | <span data-ttu-id="726b9-136">存取類型</span><span class="sxs-lookup"><span data-stu-id="726b9-136">Access type</span></span>          | <span data-ttu-id="726b9-137">Description</span><span class="sxs-lookup"><span data-stu-id="726b9-137">Description</span></span>                                              |
|:----------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [<span data-ttu-id="726b9-138">**計數**</span><span class="sxs-lookup"><span data-stu-id="726b9-138">**Count**</span></span>](swbemobjectset-count.md)<br/>          | <span data-ttu-id="726b9-139">唯讀</span><span class="sxs-lookup"><span data-stu-id="726b9-139">Read-only</span></span><br/> | <span data-ttu-id="726b9-140">集合中的項目數目</span><span class="sxs-lookup"><span data-stu-id="726b9-140">The number of items in the collection.</span></span><br/>        |
| [<span data-ttu-id="726b9-141">**安全性\_**</span><span class="sxs-lookup"><span data-stu-id="726b9-141">**Security\_**</span></span>](swbemobjectset-security-.md)<br/> | <span data-ttu-id="726b9-142">唯讀</span><span class="sxs-lookup"><span data-stu-id="726b9-142">Read-only</span></span><br/> | <span data-ttu-id="726b9-143">用來讀取或變更安全性設定。</span><span class="sxs-lookup"><span data-stu-id="726b9-143">Used to read or change the security settings.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="726b9-144">備註</span><span class="sxs-lookup"><span data-stu-id="726b9-144">Remarks</span></span>

<span data-ttu-id="726b9-145">**Swbemobjectset 搭配使用** 是零或多個 [**SWbemObject**](swbemobject.md)物件的集合。</span><span class="sxs-lookup"><span data-stu-id="726b9-145">An **SWbemObjectSet** is a collection of zero or more [**SWbemObject**](swbemobject.md) objects.</span></span> <span data-ttu-id="726b9-146">**Swbemobjectset 搭配使用** 中的每個 **SWbemObject** 都可以代表兩個專案的其中一個：</span><span class="sxs-lookup"><span data-stu-id="726b9-146">Each **SWbemObject** in a **SWbemObjectSet** can represent one of two things:</span></span>

-   <span data-ttu-id="726b9-147">受 WMI 管理之資源的實例。</span><span class="sxs-lookup"><span data-stu-id="726b9-147">An instance of a WMI-managed resource.</span></span>
-   <span data-ttu-id="726b9-148">類別定義的實例。</span><span class="sxs-lookup"><span data-stu-id="726b9-148">An instance of a class definition.</span></span>

<span data-ttu-id="726b9-149">此類別在 WMI 中最常見的用法是作為 [**ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) 或 [**InstancesOf**](swbemservices-instancesof.md) 呼叫的傳回值，如下列程式碼範例所述：</span><span class="sxs-lookup"><span data-stu-id="726b9-149">The most common use of this class in WMI is as the return value for an [**ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) or [**InstancesOf**](swbemservices-instancesof.md) call, as described in the following code sample:</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colServices = objSWbemServices.ExecQuery("SELECT State FROM Win32_Service")
For Each objService In colServices
    Wscript.Echo objService.Name, objService.State
Next
```



<span data-ttu-id="726b9-150">在大部分的情況下，您只會對 **swbemobjectset 搭配使用** 列舉集合本身所包含的所有物件。</span><span class="sxs-lookup"><span data-stu-id="726b9-150">For the most part, the only thing you will ever do with an **SWbemObjectSet** is enumerate all the objects contained within the collection itself.</span></span> <span data-ttu-id="726b9-151">不過， **swbemobjectset 搭配使用** 確實包含可在系統管理腳本中使用的屬性計數。</span><span class="sxs-lookup"><span data-stu-id="726b9-151">However, **SWbemObjectSet** does include a property Count that can be useful in system administration scripting.</span></span> <span data-ttu-id="726b9-152">顧名思義，Count 會告訴您集合中的專案數。</span><span class="sxs-lookup"><span data-stu-id="726b9-152">As the name implies, Count tells you the number of items in the collection.</span></span> <span data-ttu-id="726b9-153">例如，此腳本會取得電腦上安裝的所有服務的集合，然後回顯找到的服務總數：</span><span class="sxs-lookup"><span data-stu-id="726b9-153">For example, this script retrieves a collection of all the services installed on a computer and then echoes the total number of services found:</span></span>

<span data-ttu-id="726b9-154">如需如何使用這個類別的詳細資訊，請參閱 [列舉 WMI](enumerating-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="726b9-154">For more information on how to use this class, see [Enumerating WMI](enumerating-wmi.md).</span></span>

## <a name="examples"></a><span data-ttu-id="726b9-155">範例</span><span class="sxs-lookup"><span data-stu-id="726b9-155">Examples</span></span>

<span data-ttu-id="726b9-156">下列 VBScript 程式碼範例說明如何操作 **swbemobjectset 搭配使用** 集合。</span><span class="sxs-lookup"><span data-stu-id="726b9-156">The following VBScript code sample illustrates how **SWbemObjectSet** collections are manipulated.</span></span>


```VB
On Error Resume Next

Set Disks = GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")

WScript.Echo "There are", Disks.Count, " Disks"

Set Disk = Disks("Win32_LogicalDisk.DeviceID=""C:""")
WScript.Echo Disk.Path_.Path

if Err <> 0 Then
 WScript.Echo Err.Description
 Err.Clear
End if
```



<span data-ttu-id="726b9-157">下列 Perl 程式碼範例說明如何操作 **swbemobjectset 搭配使用** 集合。</span><span class="sxs-lookup"><span data-stu-id="726b9-157">The following Perl code sample illustrates how **SWbemObjectSet** collections are manipulated.</span></span>


```
use strict;
use Win32::OLE;

my ($disks,$disk);

eval { $disks = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
   InstancesOf("CIM_LogicalDisk"); };
unless($@)
{
 print "\nThere are ", $disks->{Count}, " Disks \n";

 eval { $disk = $disks->Item("Win32_LogicalDisk.DeviceID=\"C:\""); };
 unless($@)
 {
  print $disk->{Path_}->{Path}, "\n";
 }
 else
 {
  print STDERR Win32::OLE->LastError, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="726b9-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="726b9-158">Requirements</span></span>



| <span data-ttu-id="726b9-159">需求</span><span class="sxs-lookup"><span data-stu-id="726b9-159">Requirement</span></span> | <span data-ttu-id="726b9-160">值</span><span class="sxs-lookup"><span data-stu-id="726b9-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="726b9-161">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="726b9-161">Minimum supported client</span></span><br/> | <span data-ttu-id="726b9-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="726b9-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="726b9-163">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="726b9-163">Minimum supported server</span></span><br/> | <span data-ttu-id="726b9-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="726b9-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="726b9-165">標頭</span><span class="sxs-lookup"><span data-stu-id="726b9-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="726b9-166"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="726b9-166"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="726b9-167">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="726b9-167">Type library</span></span><br/>             | <dl> <span data-ttu-id="726b9-168"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="726b9-168"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="726b9-169">DLL</span><span class="sxs-lookup"><span data-stu-id="726b9-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="726b9-170"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="726b9-170"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="726b9-171">CLSID</span><span class="sxs-lookup"><span data-stu-id="726b9-171">CLSID</span></span><br/>                    | <span data-ttu-id="726b9-172">CLSID \_ swbemobjectset 搭配使用</span><span class="sxs-lookup"><span data-stu-id="726b9-172">CLSID\_SWbemObjectSet</span></span><br/>                                                        |
| <span data-ttu-id="726b9-173">IID</span><span class="sxs-lookup"><span data-stu-id="726b9-173">IID</span></span><br/>                      | <span data-ttu-id="726b9-174">IID \_ ISWbemObjectSet</span><span class="sxs-lookup"><span data-stu-id="726b9-174">IID\_ISWbemObjectSet</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="726b9-175">另請參閱</span><span class="sxs-lookup"><span data-stu-id="726b9-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="726b9-176">腳本 API 物件</span><span class="sxs-lookup"><span data-stu-id="726b9-176">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 





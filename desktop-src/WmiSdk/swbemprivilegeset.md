---
description: SWbemPrivilegeSet 物件是 SWbemSecurity 物件中 SWbemPrivilege 物件的集合，該物件會要求 Windows Management Instrumentation (WMI) 物件的特定許可權。
ms.assetid: 073cf2d4-f7ee-45a6-8fa6-ca77a4870346
ms.tgt_platform: multiple
title: 'SWbemPrivilegeSet 物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet
- ISWbemPrivilegeSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b2946f8b1f745c0db123ed33dab312cbbe9d16c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318864"
---
# <a name="swbemprivilegeset-object"></a><span data-ttu-id="90ac2-103">SWbemPrivilegeSet 物件</span><span class="sxs-lookup"><span data-stu-id="90ac2-103">SWbemPrivilegeSet object</span></span>

<span data-ttu-id="90ac2-104">**SWbemPrivilegeSet** 物件是 [**SWbemSecurity**](swbemsecurity.md)物件中 [**SWbemPrivilege**](swbemprivilege.md)物件的集合，該物件會要求 Windows Management Instrumentation (WMI) 物件的特定許可權。</span><span class="sxs-lookup"><span data-stu-id="90ac2-104">An **SWbemPrivilegeSet** object is a collection of [**SWbemPrivilege**](swbemprivilege.md) objects in an [**SWbemSecurity**](swbemsecurity.md) object that requests specific privileges for a Windows Management Instrumentation (WMI) object.</span></span> <span data-ttu-id="90ac2-105">請參閱 [**許可權常數**](privilege-constants.md)中的許可權清單。</span><span class="sxs-lookup"><span data-stu-id="90ac2-105">See the list of privileges in [**Privilege Constants**](privilege-constants.md).</span></span> <span data-ttu-id="90ac2-106">使用 [**Add**](swbemprivilegeset-add.md) 和 [**AddAsString**](swbemprivilegeset-addasstring.md) 方法，將專案加入至集合。</span><span class="sxs-lookup"><span data-stu-id="90ac2-106">Items are added to the collection using the [**Add**](swbemprivilegeset-add.md) and [**AddAsString**](swbemprivilegeset-addasstring.md) methods.</span></span> <span data-ttu-id="90ac2-107">專案是使用 [**Item**](swbemprivilegeset-item.md) 方法從集合中取出，並使用 [**Remove**](swbemprivilegeset-remove.md) 方法移除。</span><span class="sxs-lookup"><span data-stu-id="90ac2-107">Items are retrieved from the collection using the [**Item**](swbemprivilegeset-item.md) method, and removed using the [**Remove**](swbemprivilegeset-remove.md) method.</span></span> <span data-ttu-id="90ac2-108">VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) 方法呼叫無法建立這個物件。</span><span class="sxs-lookup"><span data-stu-id="90ac2-108">This object cannot be created by the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) method call.</span></span> <span data-ttu-id="90ac2-109">如需詳細資訊，請參閱 [存取集合](accessing-a-collection.md)。</span><span class="sxs-lookup"><span data-stu-id="90ac2-109">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

<span data-ttu-id="90ac2-110">**SWbemPrivilegeSet** 物件是特定物件的一組許可權覆寫要求。</span><span class="sxs-lookup"><span data-stu-id="90ac2-110">An **SWbemPrivilegeSet** object is a set of privilege override requests for a specific object.</span></span> <span data-ttu-id="90ac2-111">使用這個物件進行 API 呼叫時，會嘗試許可權覆寫要求。</span><span class="sxs-lookup"><span data-stu-id="90ac2-111">When an API call is made using this object, the privilege override requests are attempted.</span></span> <span data-ttu-id="90ac2-112">**SWbemPrivilegeSet** 物件不會定義目前使用者或進程可用的許可權。</span><span class="sxs-lookup"><span data-stu-id="90ac2-112">The **SWbemPrivilegeSet** object does not define the privileges available to the current user or process.</span></span> <span data-ttu-id="90ac2-113">換句話說，取得任何 WMI 物件的許可權，並不會識別連接至 WMI 時所進行的許可權設定，或是將物件傳遞到接收時的作用中許可權。</span><span class="sxs-lookup"><span data-stu-id="90ac2-113">In other words, obtaining the privileges for any WMI object does not identify the privilege settings that are made on the connection to WMI, or the privileges in effect when an object is delivered to a sink.</span></span>

## <a name="members"></a><span data-ttu-id="90ac2-114">成員</span><span class="sxs-lookup"><span data-stu-id="90ac2-114">Members</span></span>

<span data-ttu-id="90ac2-115">**SWbemPrivilegeSet** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="90ac2-115">The **SWbemPrivilegeSet** object has these types of members:</span></span>

-   [<span data-ttu-id="90ac2-116">方法</span><span class="sxs-lookup"><span data-stu-id="90ac2-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="90ac2-117">屬性</span><span class="sxs-lookup"><span data-stu-id="90ac2-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="90ac2-118">方法</span><span class="sxs-lookup"><span data-stu-id="90ac2-118">Methods</span></span>

<span data-ttu-id="90ac2-119">**SWbemPrivilegeSet** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="90ac2-119">The **SWbemPrivilegeSet** object has these methods.</span></span>



| <span data-ttu-id="90ac2-120">方法</span><span class="sxs-lookup"><span data-stu-id="90ac2-120">Method</span></span>                                               | <span data-ttu-id="90ac2-121">描述</span><span class="sxs-lookup"><span data-stu-id="90ac2-121">Description</span></span>                                                                                                                                                             |
|:-----------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="90ac2-122">**添加**</span><span class="sxs-lookup"><span data-stu-id="90ac2-122">**Add**</span></span>](swbemprivilegeset-add.md)                 | <span data-ttu-id="90ac2-123">使用 [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)常數，將 [**SWbemPrivilege**](swbemprivilege.md)物件加入至 **SWbemPrivilegeSet** 集合。</span><span class="sxs-lookup"><span data-stu-id="90ac2-123">Adds an [**SWbemPrivilege**](swbemprivilege.md) object to the **SWbemPrivilegeSet** collection using a [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) constant.</span></span><br/> |
| [<span data-ttu-id="90ac2-124">**AddAsString**</span><span class="sxs-lookup"><span data-stu-id="90ac2-124">**AddAsString**</span></span>](swbemprivilegeset-addasstring.md) | <span data-ttu-id="90ac2-125">使用許可權字串，將 [**SWbemPrivilege**](swbemprivilege.md) 物件加入至 **SWbemPrivilegeSet** 集合。</span><span class="sxs-lookup"><span data-stu-id="90ac2-125">Adds an [**SWbemPrivilege**](swbemprivilege.md) object to the **SWbemPrivilegeSet** collection using a privilege string.</span></span><br/>                                    |
| [<span data-ttu-id="90ac2-126">**DeleteAll**</span><span class="sxs-lookup"><span data-stu-id="90ac2-126">**DeleteAll**</span></span>](swbemprivilegeset-deleteall.md)     | <span data-ttu-id="90ac2-127">從集合中刪除擁有權限。</span><span class="sxs-lookup"><span data-stu-id="90ac2-127">Deletes all the privileges from the collection.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="90ac2-128">**項目**</span><span class="sxs-lookup"><span data-stu-id="90ac2-128">**Item**</span></span>](swbemprivilegeset-item.md)               | <span data-ttu-id="90ac2-129">從集合中捕獲 [**SWbemPrivilege**](swbemprivilege.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="90ac2-129">Retrieves an [**SWbemPrivilege**](swbemprivilege.md) object from the collection.</span></span> <span data-ttu-id="90ac2-130">這是這個物件的預設方法。</span><span class="sxs-lookup"><span data-stu-id="90ac2-130">This is the default method of this object.</span></span><br/>                                 |
| [<span data-ttu-id="90ac2-131">**移除**</span><span class="sxs-lookup"><span data-stu-id="90ac2-131">**Remove**</span></span>](swbemprivilegeset-remove.md)           | <span data-ttu-id="90ac2-132">從集合中移除 [**SWbemPrivilege**](swbemprivilege.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="90ac2-132">Removes an [**SWbemPrivilege**](swbemprivilege.md) object from the collection.</span></span><br/>                                                                              |



 

### <a name="properties"></a><span data-ttu-id="90ac2-133">屬性</span><span class="sxs-lookup"><span data-stu-id="90ac2-133">Properties</span></span>

<span data-ttu-id="90ac2-134">**SWbemPrivilegeSet** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="90ac2-134">The **SWbemPrivilegeSet** object has these properties.</span></span>



| <span data-ttu-id="90ac2-135">屬性</span><span class="sxs-lookup"><span data-stu-id="90ac2-135">Property</span></span>                                            | <span data-ttu-id="90ac2-136">存取類型</span><span class="sxs-lookup"><span data-stu-id="90ac2-136">Access type</span></span>          | <span data-ttu-id="90ac2-137">Description</span><span class="sxs-lookup"><span data-stu-id="90ac2-137">Description</span></span>                                       |
|:----------------------------------------------------|:---------------------|:--------------------------------------------------|
| [<span data-ttu-id="90ac2-138">**計數**</span><span class="sxs-lookup"><span data-stu-id="90ac2-138">**Count**</span></span>](swbemprivilegeset-count.md)<br/> | <span data-ttu-id="90ac2-139">唯讀</span><span class="sxs-lookup"><span data-stu-id="90ac2-139">Read-only</span></span><br/> | <span data-ttu-id="90ac2-140">集合中的項目數目</span><span class="sxs-lookup"><span data-stu-id="90ac2-140">The number of items in the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="90ac2-141">範例</span><span class="sxs-lookup"><span data-stu-id="90ac2-141">Examples</span></span>

<span data-ttu-id="90ac2-142">下列 VBScript 程式碼範例會取得 SWbemPrivileges 物件，並依許可權值將所有可用的許可權新增至集合，如 [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)中所定義。</span><span class="sxs-lookup"><span data-stu-id="90ac2-142">The following VBScript code example obtains an SWbemPrivileges object and adds all the available privileges to the collection by privilege value, as defined in [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" _
    & strComputer & "\root\cimv2")
set colPrivileges = objWMIService.Security_.Privileges
For I = 1 To 27
colPrivileges.Add(I)
Next
' Display information about each privilege 
For Each objItem In colPrivileges
wscript.echo objItem.Identifier & vbtab & objItem.Name _
    & vbtab & objItem.Displayname _
    & vbtab & "Enabled = " & objItem.IsEnabled
Next
```



<span data-ttu-id="90ac2-143">下列 VBScript 程式碼範例示範如何使用 **SWbemPrivilegeSet** 物件來加入許可權。</span><span class="sxs-lookup"><span data-stu-id="90ac2-143">The following VBScript code example demonstrates how to add privileges using the **SWbemPrivilegeSet** object.</span></span>


```VB
on error resume next

const wbemPrivilegeSecurity = 8
const wbemPrivilegeDebug = 20

set locator = CreateObject("WbemScripting.SWbemLocator")

' Add a single privilege using SWbemPrivilegeSet.Add

locator.Security_.Privileges.Add wbemPrivilegeSecurity 
Set Privilege = locator.Security_.Privileges(wbemPrivilegeSecurity)
WScript.Echo Privilege.Name

' Attempt to add an illegal privilege using SWbemPrivilegeSet.Add
locator.Security_.Privileges.Add 6535
if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
 err.clear
end if 

locator.Security_.Privileges.Add wbemPrivilegeDebug 

locator.Security_.Privileges(wbemPrivilegeDebug).IsEnabled = false

' Add a single privilege using SWbemPrivilegeSet.AddAsString

Set Privilege = locator.Security_.Privileges.AddAsString ("SeChangeNotifyPrivilege")
WScript.Echo Privilege.Name

' Attempt to add an illegal privilege using SWbemPrivilegeSet.AddAsString
locator.Security_.Privileges.AddAsString "SeChungeNotifyPrivilege"
if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
 err.clear
end if 

WScript.Echo ""
for each Privilege in locator.Security_.Privileges
 WScript.Echo "[" & Privilege.DisplayName & "]", Privilege.Identifier, Privilege.Name, Privilege.IsEnabled
next

if err <> 0 then
 WScript.Echo Err.Number, Err.Description, Err.Source
end if 
```



<span data-ttu-id="90ac2-144">下列 Perl 程式碼範例示範如何使用 **SWbemPrivilegeSet** 物件來加入許可權。</span><span class="sxs-lookup"><span data-stu-id="90ac2-144">The following Perl code example demonstrates how to add privileges using the **SWbemPrivilegeSet** object.</span></span>


```
use strict;
use Win32::OLE;

close(STDERR);

my ($locator, $Privilege);
my $wbemPrivilegeSecurity = 8;
my $wbemPrivilegeDebug = 20;

eval { $locator = new Win32::OLE 'WbemScripting.SWbemLocator';};

if (!$@ && defined $locator)
{
 # Add a single privilege using SWbemPrivilegeSet.Add
 $locator->{Security_}->{Privileges}->Add($wbemPrivilegeSecurity);
 $Privilege = $locator->{Security_}->Privileges($wbemPrivilegeSecurity);
 print "\n", $Privilege->{Name}, "\n\n";

 # Attempt to add an illegal privilege using SWbemPrivilegeSet.Add
 eval { $locator->{Security_}->{Privileges}->Add(6535); };
 print Win32::OLE->LastError, "\n" if ($@ || Win32::OLE->LastError);

 $locator->{Security_}->{Privileges}->Add($wbemPrivilegeDebug); 
 $locator->{Security_}->Privileges($wbemPrivilegeDebug)->{IsEnabled} = 0;

 # Add a single privilege using SWbemPrivilegeSet.AddAsString
 $Privilege = $locator->{Security_}->{Privileges}->AddAsString ("SeChangeNotifyPrivilege");
 print "\n", $Privilege->{Name}, "\n\n";

 # Attempt to add an illegal privilege using SWbemPrivilegeSet.AddAsString
 eval {$locator->{Security_}->{Privileges}->AddAsString ("SeChungeNotifyPrivilege"); };
 print Win32::OLE->LastError, "\n" if ($@ || Win32::OLE->LastError);
 print "\n";

 foreach $Privilege (in {$locator->{Security_}->{Privileges}})
 {
  printf "[%s] %d %s %d \n" , $Privilege->{DisplayName}, $Privilege->{Identifier}, $Privilege->{Name}, $Privilege->{IsEnabled};
 }
}
else
{
 print Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="90ac2-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="90ac2-145">Requirements</span></span>



| <span data-ttu-id="90ac2-146">需求</span><span class="sxs-lookup"><span data-stu-id="90ac2-146">Requirement</span></span> | <span data-ttu-id="90ac2-147">值</span><span class="sxs-lookup"><span data-stu-id="90ac2-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="90ac2-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="90ac2-148">Minimum supported client</span></span><br/> | <span data-ttu-id="90ac2-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="90ac2-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="90ac2-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="90ac2-150">Minimum supported server</span></span><br/> | <span data-ttu-id="90ac2-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="90ac2-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="90ac2-152">標頭</span><span class="sxs-lookup"><span data-stu-id="90ac2-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="90ac2-153"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="90ac2-153"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="90ac2-154">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="90ac2-154">Type library</span></span><br/>             | <dl> <span data-ttu-id="90ac2-155"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="90ac2-155"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="90ac2-156">DLL</span><span class="sxs-lookup"><span data-stu-id="90ac2-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90ac2-157"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90ac2-157"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="90ac2-158">CLSID</span><span class="sxs-lookup"><span data-stu-id="90ac2-158">CLSID</span></span><br/>                    | <span data-ttu-id="90ac2-159">CLSID \_ SWbemPrivilegeSet</span><span class="sxs-lookup"><span data-stu-id="90ac2-159">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="90ac2-160">IID</span><span class="sxs-lookup"><span data-stu-id="90ac2-160">IID</span></span><br/>                      | <span data-ttu-id="90ac2-161">IID \_ ISWbemPrivilegeSet</span><span class="sxs-lookup"><span data-stu-id="90ac2-161">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="90ac2-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="90ac2-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90ac2-163">執行具有特殊許可權的作業</span><span class="sxs-lookup"><span data-stu-id="90ac2-163">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="90ac2-164">使用 VBScript 執行特殊許可權作業</span><span class="sxs-lookup"><span data-stu-id="90ac2-164">Executing Privileged Operations Using VBScript</span></span>](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[<span data-ttu-id="90ac2-165">WbemPrivilegeEnum</span><span class="sxs-lookup"><span data-stu-id="90ac2-165">WbemPrivilegeEnum</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[<span data-ttu-id="90ac2-166">腳本 API 物件</span><span class="sxs-lookup"><span data-stu-id="90ac2-166">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> <dt>

[<span data-ttu-id="90ac2-167">**許可權常數**</span><span class="sxs-lookup"><span data-stu-id="90ac2-167">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> </dl>

 


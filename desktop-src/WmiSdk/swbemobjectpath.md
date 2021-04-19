---
description: 使用 SWbemObjectPath 物件的方法和屬性來建立和驗證物件路徑。 這個物件可以由 VBScript CreateObject 呼叫建立。
ms.assetid: f2cf489d-d2a9-4926-84cf-fb33fe3d726a
ms.tgt_platform: multiple
title: 'SWbemObjectPath 物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath
- ISWbemObjectPath
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1e6836cd58970f3667d8f629a678d55bec5185a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993052"
---
# <a name="swbemobjectpath-object"></a><span data-ttu-id="6d750-104">SWbemObjectPath 物件</span><span class="sxs-lookup"><span data-stu-id="6d750-104">SWbemObjectPath object</span></span>

<span data-ttu-id="6d750-105">使用 **SWbemObjectPath** 物件的方法和屬性來建立和驗證物件路徑。</span><span class="sxs-lookup"><span data-stu-id="6d750-105">Use the methods and properties of the **SWbemObjectPath** object to construct and validate an object path.</span></span> <span data-ttu-id="6d750-106">這個物件可以由 VBScript **CreateObject** 呼叫建立。</span><span class="sxs-lookup"><span data-stu-id="6d750-106">This object can be created by the VBScript **CreateObject** call.</span></span>

## <a name="members"></a><span data-ttu-id="6d750-107">成員</span><span class="sxs-lookup"><span data-stu-id="6d750-107">Members</span></span>

<span data-ttu-id="6d750-108">**SWbemObjectPath** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6d750-108">The **SWbemObjectPath** object has these types of members:</span></span>

-   [<span data-ttu-id="6d750-109">方法</span><span class="sxs-lookup"><span data-stu-id="6d750-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="6d750-110">屬性</span><span class="sxs-lookup"><span data-stu-id="6d750-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6d750-111">方法</span><span class="sxs-lookup"><span data-stu-id="6d750-111">Methods</span></span>

<span data-ttu-id="6d750-112">**SWbemObjectPath** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="6d750-112">The **SWbemObjectPath** object has these methods.</span></span>



| <span data-ttu-id="6d750-113">方法</span><span class="sxs-lookup"><span data-stu-id="6d750-113">Method</span></span>                                                   | <span data-ttu-id="6d750-114">描述</span><span class="sxs-lookup"><span data-stu-id="6d750-114">Description</span></span>                                                     |
|:---------------------------------------------------------|:----------------------------------------------------------------|
| [<span data-ttu-id="6d750-115">**SetAsClass**</span><span class="sxs-lookup"><span data-stu-id="6d750-115">**SetAsClass**</span></span>](swbemobjectpath-setasclass.md)         | <span data-ttu-id="6d750-116">強制路徑為 WMI 類別定址。</span><span class="sxs-lookup"><span data-stu-id="6d750-116">Forces the path to address a WMI class.</span></span><br/>              |
| [<span data-ttu-id="6d750-117">**SetAsSingleton**</span><span class="sxs-lookup"><span data-stu-id="6d750-117">**SetAsSingleton**</span></span>](swbemobjectpath-setassingleton.md) | <span data-ttu-id="6d750-118">強制路徑處理單一 WMI 實例。</span><span class="sxs-lookup"><span data-stu-id="6d750-118">Forces the path to address a singleton WMI instance.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6d750-119">屬性</span><span class="sxs-lookup"><span data-stu-id="6d750-119">Properties</span></span>

<span data-ttu-id="6d750-120">**SWbemObjectPath** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6d750-120">The **SWbemObjectPath** object has these properties.</span></span>



| <span data-ttu-id="6d750-121">屬性</span><span class="sxs-lookup"><span data-stu-id="6d750-121">Property</span></span>                                                              | <span data-ttu-id="6d750-122">存取類型</span><span class="sxs-lookup"><span data-stu-id="6d750-122">Access type</span></span>           | <span data-ttu-id="6d750-123">Description</span><span class="sxs-lookup"><span data-stu-id="6d750-123">Description</span></span>                                                                                                                                                                          |
|:----------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d750-124">**授權單位**</span><span class="sxs-lookup"><span data-stu-id="6d750-124">**Authority**</span></span>](swbemobjectpath-authority.md)<br/>             | <span data-ttu-id="6d750-125">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6d750-125">Read/write</span></span><br/> | <span data-ttu-id="6d750-126">定義物件路徑之授權單位元件的字串。</span><span class="sxs-lookup"><span data-stu-id="6d750-126">String that defines the Authority component of the object path.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="6d750-127">**類別**</span><span class="sxs-lookup"><span data-stu-id="6d750-127">**Class**</span></span>](swbemobjectpath-class.md)<br/>                     | <span data-ttu-id="6d750-128">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6d750-128">Read/write</span></span><br/> | <span data-ttu-id="6d750-129">屬於物件路徑的類別名稱。</span><span class="sxs-lookup"><span data-stu-id="6d750-129">Name of the class that is part of the object path.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="6d750-130">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="6d750-130">**DisplayName**</span></span>](swbemobjectpath-displayname.md)<br/>         | <span data-ttu-id="6d750-131">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6d750-131">Read/write</span></span><br/> | <span data-ttu-id="6d750-132">字串，其中包含格式的路徑，該路徑可當做標記顯示名稱使用。</span><span class="sxs-lookup"><span data-stu-id="6d750-132">String that contains the path in a form that can be used as a moniker display name.</span></span> <span data-ttu-id="6d750-133">請參閱 [建立 WMI 應用程式或腳本](creating-a-wmi-application-or-script.md)。</span><span class="sxs-lookup"><span data-stu-id="6d750-133">See [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span><br/> |
| [<span data-ttu-id="6d750-134">**IsClass**</span><span class="sxs-lookup"><span data-stu-id="6d750-134">**IsClass**</span></span>](swbemobjectpath-isclass.md)<br/>                 | <span data-ttu-id="6d750-135">唯讀</span><span class="sxs-lookup"><span data-stu-id="6d750-135">Read-only</span></span><br/>  | <span data-ttu-id="6d750-136">指出此路徑是否代表類別的布林值。</span><span class="sxs-lookup"><span data-stu-id="6d750-136">Boolean value that indicates if this path represents a class.</span></span> <span data-ttu-id="6d750-137">這類似于 COM API 中的[ \_ \_ 拼出動植物](wmi-system-properties.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="6d750-137">This is analogous to the [\_\_Genus](wmi-system-properties.md) property in the COM API.</span></span><br/>                    |
| [<span data-ttu-id="6d750-138">**IsSingleton**</span><span class="sxs-lookup"><span data-stu-id="6d750-138">**IsSingleton**</span></span>](swbemobjectpath-issingleton.md)<br/>         | <span data-ttu-id="6d750-139">唯讀</span><span class="sxs-lookup"><span data-stu-id="6d750-139">Read-only</span></span><br/>  | <span data-ttu-id="6d750-140">指出此路徑是否代表單一實例的布林值。</span><span class="sxs-lookup"><span data-stu-id="6d750-140">Boolean value that indicates if this path represents a singleton instance.</span></span><br/>                                                                                                |
| [<span data-ttu-id="6d750-141">**索引鍵**</span><span class="sxs-lookup"><span data-stu-id="6d750-141">**Keys**</span></span>](swbemobjectpath-keys.md)<br/>                       | <span data-ttu-id="6d750-142">唯讀</span><span class="sxs-lookup"><span data-stu-id="6d750-142">Read-only</span></span><br/>  | <span data-ttu-id="6d750-143">[**SWbemNamedValueSet**](swbemnamedvalueset.md)物件，其中包含索引鍵值系結。</span><span class="sxs-lookup"><span data-stu-id="6d750-143">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that contains the key value bindings.</span></span><br/>                                                                          |
| [<span data-ttu-id="6d750-144">**Locale**</span><span class="sxs-lookup"><span data-stu-id="6d750-144">**Locale**</span></span>](swbemobjectpath-locale.md)<br/>                   | <span data-ttu-id="6d750-145">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6d750-145">Read/write</span></span><br/> | <span data-ttu-id="6d750-146">包含此物件路徑之地區設定的字串。</span><span class="sxs-lookup"><span data-stu-id="6d750-146">String that contains the locale for this object path.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="6d750-147">**命名空間**</span><span class="sxs-lookup"><span data-stu-id="6d750-147">**Namespace**</span></span>](swbemobjectpath-namespace.md)<br/>             | <span data-ttu-id="6d750-148">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6d750-148">Read/write</span></span><br/> | <span data-ttu-id="6d750-149">屬於物件路徑一部分的命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="6d750-149">Name of the namespace that is part of the object path.</span></span> <span data-ttu-id="6d750-150">這與 COM API 中的[ \_ \_ Namespace](wmi-system-properties.md)屬性相同。</span><span class="sxs-lookup"><span data-stu-id="6d750-150">This is the same as the [\_\_Namespace](wmi-system-properties.md) property in the COM API.</span></span><br/>                        |
| [<span data-ttu-id="6d750-151">**ParentNamespace**</span><span class="sxs-lookup"><span data-stu-id="6d750-151">**ParentNamespace**</span></span>](swbemobjectpath-parentnamespace.md)<br/> | <span data-ttu-id="6d750-152">唯讀</span><span class="sxs-lookup"><span data-stu-id="6d750-152">Read-only</span></span><br/>  | <span data-ttu-id="6d750-153">屬於物件路徑一部分之命名空間的父系名稱。</span><span class="sxs-lookup"><span data-stu-id="6d750-153">Name of the parent of the namespace that is part of the object path.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="6d750-154">**路徑**</span><span class="sxs-lookup"><span data-stu-id="6d750-154">**Path**</span></span>](swbemobjectpath-path.md)<br/>                       | <span data-ttu-id="6d750-155">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6d750-155">Read/write</span></span><br/> | <span data-ttu-id="6d750-156">包含絕對路徑。</span><span class="sxs-lookup"><span data-stu-id="6d750-156">Contains the absolute path.</span></span> <span data-ttu-id="6d750-157">這與 COM API 中的[ \_ \_ Path](wmi-system-properties.md) system 屬性相同。</span><span class="sxs-lookup"><span data-stu-id="6d750-157">This is the same as the [\_\_Path](wmi-system-properties.md) system property in the COM API.</span></span> <span data-ttu-id="6d750-158">這是此物件的預設屬性。</span><span class="sxs-lookup"><span data-stu-id="6d750-158">This is the default property of this object.</span></span><br/>    |
| [<span data-ttu-id="6d750-159">**Relpath**</span><span class="sxs-lookup"><span data-stu-id="6d750-159">**Relpath**</span></span>](swbemobjectpath-relpath.md)<br/>                 | <span data-ttu-id="6d750-160">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6d750-160">Read/write</span></span><br/> | <span data-ttu-id="6d750-161">包含相對路徑。</span><span class="sxs-lookup"><span data-stu-id="6d750-161">Contains the relative path.</span></span> <span data-ttu-id="6d750-162">這與 COM API 中的[ \_ \_ Relpath](wmi-system-properties.md)系統屬性相同。</span><span class="sxs-lookup"><span data-stu-id="6d750-162">This is the same as the [\_\_Relpath](wmi-system-properties.md) system property in the COM API.</span></span><br/>                                              |
| [<span data-ttu-id="6d750-163">**安全性\_**</span><span class="sxs-lookup"><span data-stu-id="6d750-163">**Security\_**</span></span>](swbemobjectpath-security-.md)<br/>            | <span data-ttu-id="6d750-164">唯讀</span><span class="sxs-lookup"><span data-stu-id="6d750-164">Read-only</span></span><br/>  | <span data-ttu-id="6d750-165">用來讀取或變更安全性設定。</span><span class="sxs-lookup"><span data-stu-id="6d750-165">Used to read or change the security settings.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="6d750-166">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="6d750-166">**Server**</span></span>](swbemobjectpath-server.md)<br/>                   | <span data-ttu-id="6d750-167">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6d750-167">Read/write</span></span><br/> | <span data-ttu-id="6d750-168">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="6d750-168">Name of the server.</span></span> <span data-ttu-id="6d750-169">這與 COM API 中的[ \_ \_ 伺服器](wmi-system-properties.md)系統屬性相同。</span><span class="sxs-lookup"><span data-stu-id="6d750-169">This is the same as the [\_\_Server](wmi-system-properties.md) system property in the COM API.</span></span><br/>                                                       |



 

## <a name="examples"></a><span data-ttu-id="6d750-170">範例</span><span class="sxs-lookup"><span data-stu-id="6d750-170">Examples</span></span>

<span data-ttu-id="6d750-171">下列 VBScript 程式碼範例示範如何建立物件路徑。</span><span class="sxs-lookup"><span data-stu-id="6d750-171">The following VBScript code sample demonstrates how to build object paths.</span></span>


```VB
on error resume next 
Set ObjectPath = CreateObject("WbemScripting.SWbemObjectPath")
ObjectPath.Server = "dingle"
ObjectPath.Namespace = "root/default/something"
ObjectPath.Class = "ho"
ObjectPath.Keys.Add "fred1", 10
ObjectPath.Keys.Add "fred2", -34
ObjectPath.Keys.Add "fred3", 65234654
ObjectPath.Keys.Add "fred4", "Wahaay"
ObjectPath.Keys.Add "fred5", -786186777

if err <> 0 then 
 WScript.Echo err.number
end if 

WScript.Echo "Pass 1:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.Security_.ImpersonationLevel = 3

WScript.Echo "Pass 2:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.Security_.AuthenticationLevel = 5

WScript.Echo "Pass 3:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

Set Privileges = ObjectPath.Security_.Privileges
if err <> 0 then
 WScript.Echo Hex(Err.Number), Err.Description
end if
Privileges.Add 8
Privileges.Add 20, false

WScript.Echo "Pass 4:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.DisplayName = "winmgmts:{impersonationLevel=impersonate,authenticationLevel=pktprivacy,(Debug,!IncreaseQuota, CreatePagefile ) }!//fred/root/blah"

WScript.Echo "Pass 5:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""
```



<span data-ttu-id="6d750-172">下列 Perl 程式碼範例示範如何建立物件路徑。</span><span class="sxs-lookup"><span data-stu-id="6d750-172">The following Perl code sample demonstrates how to build object paths.</span></span>


```
use strict;
use Win32::OLE;
use constant FALSE=>"false";

my ( $ObjectPath, $Privileges );

eval { $ObjectPath = new Win32::OLE 'WbemScripting.SWbemObjectPath'; };
unless($@)
{
 eval
 {
  $ObjectPath->{Server} = "dingle";
  $ObjectPath->{Namespace} = "root/default/something";
  $ObjectPath->{Class} = "ho";
  $ObjectPath->{Keys}->Add("fred1", 10);
  $ObjectPath->{Keys}->Add("fred2", -34);
  $ObjectPath->{Keys}->Add("fred3", 65234654);
  $ObjectPath->{Keys}->Add("fred4", "Wahaay");
  $ObjectPath->{Keys}->Add("fred5", -786186777);
 };
 unless($@)
 {
  print "\n";
  print "Pass 1:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  $ObjectPath->{Security_}->{ImpersonationLevel} = 3 ;

  print "Pass 2:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  $ObjectPath->{Security_}->{AuthenticationLevel} = 5 ;

  print "Pass 3:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  eval { $Privileges = $ObjectPath->{Security_}->{Privileges}; };
  unless($@)
  {
   $Privileges->Add(8);
   $Privileges->Add(20,FALSE);

   print "Pass 4:\n";
   print $ObjectPath->{Path}, "\n";
   print $ObjectPath->{DisplayName} , "\n\n";

   $ObjectPath->{DisplayName} = "winmgmts:{impersonationLevel=impersonate,authenticationLevel=pktprivacy,(Debug,!IncreaseQuota, CreatePagefile ) }!//fred/root/blah";

   print "Pass 5:\n";
   print $ObjectPath->{Path}, "\n";
   print $ObjectPath->{DisplayName} , "\n";
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
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="6d750-173">規格需求</span><span class="sxs-lookup"><span data-stu-id="6d750-173">Requirements</span></span>



| <span data-ttu-id="6d750-174">需求</span><span class="sxs-lookup"><span data-stu-id="6d750-174">Requirement</span></span> | <span data-ttu-id="6d750-175">值</span><span class="sxs-lookup"><span data-stu-id="6d750-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d750-176">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6d750-176">Minimum supported client</span></span><br/> | <span data-ttu-id="6d750-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6d750-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6d750-178">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6d750-178">Minimum supported server</span></span><br/> | <span data-ttu-id="6d750-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6d750-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6d750-180">標頭</span><span class="sxs-lookup"><span data-stu-id="6d750-180">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d750-181"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="6d750-181"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6d750-182">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="6d750-182">Type library</span></span><br/>             | <dl> <span data-ttu-id="6d750-183"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6d750-183"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6d750-184">DLL</span><span class="sxs-lookup"><span data-stu-id="6d750-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d750-185"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d750-185"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6d750-186">CLSID</span><span class="sxs-lookup"><span data-stu-id="6d750-186">CLSID</span></span><br/>                    | <span data-ttu-id="6d750-187">CLSID \_ SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="6d750-187">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="6d750-188">IID</span><span class="sxs-lookup"><span data-stu-id="6d750-188">IID</span></span><br/>                      | <span data-ttu-id="6d750-189">IID \_ ISWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="6d750-189">IID\_ISWbemObjectPath</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="6d750-190">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6d750-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d750-191">腳本 API 物件</span><span class="sxs-lookup"><span data-stu-id="6d750-191">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 





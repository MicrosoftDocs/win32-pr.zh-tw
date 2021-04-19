---
description: SWbemLastError 物件的方法和屬性包含和操作錯誤物件。
ms.assetid: 11a652fa-29e8-437b-8e62-e28e56a8a38d
ms.tgt_platform: multiple
title: 'SWbemLastError 物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError
- Associators_
- AssociatorsAsync_
- Delete_
- DeleteAsync_
- ExecMethod_
- ExecMethodAsync_
- Instances_
- InstancesAsync_
- Put_
- PutAsync_
- References_
- ReferencesAsync_
- SpawnDerivedClass_
- SpawnInstance_
- Subclasses_
- SubclassesAsync_
- Derivation_
- get_Derivation_
- Methods_
- get_Methods_
- Qualifiers_
- get_Qualifiers_
- Security_
- get_Security_
- ISWbemLastError
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a00d8e3421800acab7cc4958ddc1e6a75f101958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986839"
---
# <a name="swbemlasterror-object"></a><span data-ttu-id="04926-103">SWbemLastError 物件</span><span class="sxs-lookup"><span data-stu-id="04926-103">SWbemLastError object</span></span>

<span data-ttu-id="04926-104">**SWbemLastError** 物件的方法和屬性包含和操作錯誤物件。</span><span class="sxs-lookup"><span data-stu-id="04926-104">The methods and properties of the **SWbemLastError** object contain and manipulate error objects.</span></span> <span data-ttu-id="04926-105">這個物件的方法和屬性與 [**SWbemObject**](swbemobject.md) 物件的方法和屬性完全相同，但用來包含錯誤資訊，而不是 WMI 類別資訊。</span><span class="sxs-lookup"><span data-stu-id="04926-105">The methods and properties of this object are exactly the same as those of the [**SWbemObject**](swbemobject.md) object, but are used to contain error information instead of WMI class information.</span></span> <span data-ttu-id="04926-106">這個物件可以由 VBScript **CreateObject** 呼叫建立。</span><span class="sxs-lookup"><span data-stu-id="04926-106">This object can be created by the VBScript **CreateObject** call.</span></span>

<span data-ttu-id="04926-107">您可以建立 **SWbemLastError** error 物件，以檢查與先前的方法呼叫相關聯的延伸錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="04926-107">You can create an **SWbemLastError** error object to inspect the extended error information that is associated with a previous method call.</span></span> <span data-ttu-id="04926-108">如果錯誤資訊無法使用，則嘗試建立錯誤物件將會失敗。</span><span class="sxs-lookup"><span data-stu-id="04926-108">If error information is not available, an attempt to create an error object will fail.</span></span> <span data-ttu-id="04926-109">如果呼叫成功，並傳回錯誤物件，則會重設物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="04926-109">If the call succeeds and an error object returns, the status of the object is reset.</span></span> <span data-ttu-id="04926-110">後續嘗試抓取錯誤物件將會失敗，直到發生新的錯誤為止。</span><span class="sxs-lookup"><span data-stu-id="04926-110">Further attempts to retrieve an error object will fail until a new error occurs.</span></span> <span data-ttu-id="04926-111">如果您進行失敗的非同步呼叫， **SWbemLastError** 物件可能會由 *objWbemErrorObject* 參數中的 [**SWbemSink. OnCompleted**](swbemsink-oncompleted.md)事件傳回給您。</span><span class="sxs-lookup"><span data-stu-id="04926-111">If you make an asynchronous call that fails, an **SWbemLastError** object may be returned to you by the [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) event in the *objWbemErrorObject* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="04926-112">成員</span><span class="sxs-lookup"><span data-stu-id="04926-112">Members</span></span>

<span data-ttu-id="04926-113">**SWbemLastError** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="04926-113">The **SWbemLastError** object has these types of members:</span></span>

-   [<span data-ttu-id="04926-114">方法</span><span class="sxs-lookup"><span data-stu-id="04926-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="04926-115">屬性</span><span class="sxs-lookup"><span data-stu-id="04926-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="04926-116">方法</span><span class="sxs-lookup"><span data-stu-id="04926-116">Methods</span></span>

<span data-ttu-id="04926-117">**SWbemLastError** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="04926-117">The **SWbemLastError** object has these methods.</span></span>



| <span data-ttu-id="04926-118">方法</span><span class="sxs-lookup"><span data-stu-id="04926-118">Method</span></span>                                                   | <span data-ttu-id="04926-119">描述</span><span class="sxs-lookup"><span data-stu-id="04926-119">Description</span></span>                                                                                  |
|:---------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| <span data-ttu-id="04926-120">**Associators of\_**</span><span class="sxs-lookup"><span data-stu-id="04926-120">**Associators\_**</span></span>                                        | <span data-ttu-id="04926-121">未使用。</span><span class="sxs-lookup"><span data-stu-id="04926-121">Not used.</span></span> <span data-ttu-id="04926-122">[**SWbemObject**](swbemobject.md)物件提供相同的方法。</span><span class="sxs-lookup"><span data-stu-id="04926-122">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="04926-123">**AssociatorsAsync\_**</span><span class="sxs-lookup"><span data-stu-id="04926-123">**AssociatorsAsync\_**</span></span>                                   | <span data-ttu-id="04926-124">未使用。</span><span class="sxs-lookup"><span data-stu-id="04926-124">Not used.</span></span> <span data-ttu-id="04926-125">[**SWbemObject**](swbemobject.md)物件提供相同的方法。</span><span class="sxs-lookup"><span data-stu-id="04926-125">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| [<span data-ttu-id="04926-126">**克隆\_**</span><span class="sxs-lookup"><span data-stu-id="04926-126">**Clone\_**</span></span>](swbemlasterror-clone-.md)                 | <span data-ttu-id="04926-127">建立目前物件的複本。</span><span class="sxs-lookup"><span data-stu-id="04926-127">Makes a copy of the current object.</span></span><br/>                                               |
| [<span data-ttu-id="04926-128">**CompareTo\_**</span><span class="sxs-lookup"><span data-stu-id="04926-128">**CompareTo\_**</span></span>](swbemlasterror-compareto-.md)         | <span data-ttu-id="04926-129">測試兩個物件是否相等。</span><span class="sxs-lookup"><span data-stu-id="04926-129">Tests two objects for equality.</span></span><br/>                                                   |
| <span data-ttu-id="04926-130">**刪除\_**</span><span class="sxs-lookup"><span data-stu-id="04926-130">**Delete\_**</span></span>                                             | <span data-ttu-id="04926-131">未使用。</span><span class="sxs-lookup"><span data-stu-id="04926-131">Not used.</span></span> <span data-ttu-id="04926-132">[**SWbemObject**](swbemobject.md)物件提供相同的方法。</span><span class="sxs-lookup"><span data-stu-id="04926-132">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="04926-133">**DeleteAsync\_**</span><span class="sxs-lookup"><span data-stu-id="04926-133">**DeleteAsync\_**</span></span>                                        | <span data-ttu-id="04926-134">未使用。</span><span class="sxs-lookup"><span data-stu-id="04926-134">Not used.</span></span> <span data-ttu-id="04926-135">[**SWbemObject**](swbemobject.md)物件提供相同的方法。</span><span class="sxs-lookup"><span data-stu-id="04926-135">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="04926-136">**ExecMethod\_**</span><span class="sxs-lookup"><span data-stu-id="04926-136">**ExecMethod\_**</span></span>                                         | <span data-ttu-id="04926-137">未使用。</span><span class="sxs-lookup"><span data-stu-id="04926-137">Not used.</span></span> <span data-ttu-id="04926-138">[**SWbemObject**](swbemobject.md)物件提供相同的方法。</span><span class="sxs-lookup"><span data-stu-id="04926-138">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="04926-139">**ExecMethodAsync\_**</span><span class="sxs-lookup"><span data-stu-id="04926-139">**ExecMethodAsync\_**</span></span>                                    | <span data-ttu-id="04926-140">未使用。</span><span class="sxs-lookup"><span data-stu-id="04926-140">Not used.</span></span> <span data-ttu-id="04926-141">[**SWbemObject**](swbemobject.md)物件提供相同的方法。</span><span class="sxs-lookup"><span data-stu-id="04926-141">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| [<span data-ttu-id="04926-142">**GetObjectText\_**</span><span class="sxs-lookup"><span data-stu-id="04926-142">**GetObjectText\_**</span></span>](swbemlasterror-getobjecttext-.md) | <span data-ttu-id="04926-143">抓取以 MOF 語法撰寫之物件的文字標記法。</span><span class="sxs-lookup"><span data-stu-id="04926-143">Retrieves the textual representation of the object written with MOF syntax.</span></span><br/>       |
| <span data-ttu-id="04926-144">**執行個體\_**</span><span class="sxs-lookup"><span data-stu-id="04926-144">**Instances\_**</span></span>                                          | <span data-ttu-id="04926-145">未使用。</span><span class="sxs-lookup"><span data-stu-id="04926-145">Not used.</span></span> <span data-ttu-id="04926-146">[**SWbemObject**](swbemobject.md)物件提供相同的方法。</span><span class="sxs-lookup"><span data-stu-id="04926-146">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="04926-147">**InstancesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="04926-147">**InstancesAsync\_**</span></span>                                     | <span data-ttu-id="04926-148">未使用。</span><span class="sxs-lookup"><span data-stu-id="04926-148">Not used.</span></span> <span data-ttu-id="04926-149">[**SWbemObject**](swbemobject.md)物件提供相同的方法。</span><span class="sxs-lookup"><span data-stu-id="04926-149">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="04926-150">**把\_**</span><span class="sxs-lookup"><span data-stu-id="04926-150">**Put\_**</span></span>                                                | <span data-ttu-id="04926-151">未使用。</span><span class="sxs-lookup"><span data-stu-id="04926-151">Not used.</span></span> <span data-ttu-id="04926-152">[**SWbemObject**](swbemobject.md)物件提供相同的方法。</span><span class="sxs-lookup"><span data-stu-id="04926-152">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="04926-153">**PutAsync\_**</span><span class="sxs-lookup"><span data-stu-id="04926-153">**PutAsync\_**</span></span>                                           | <span data-ttu-id="04926-154">未使用。</span><span class="sxs-lookup"><span data-stu-id="04926-154">Not used.</span></span> <span data-ttu-id="04926-155">[**SWbemObject**](swbemobject.md)物件提供相同的方法。</span><span class="sxs-lookup"><span data-stu-id="04926-155">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="04926-156">**參考資料\_**</span><span class="sxs-lookup"><span data-stu-id="04926-156">**References\_**</span></span>                                         | <span data-ttu-id="04926-157">未使用。</span><span class="sxs-lookup"><span data-stu-id="04926-157">Not used.</span></span> <span data-ttu-id="04926-158">[**SWbemObject**](swbemobject.md)物件提供相同的方法。</span><span class="sxs-lookup"><span data-stu-id="04926-158">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="04926-159">**ReferencesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="04926-159">**ReferencesAsync\_**</span></span>                                    | <span data-ttu-id="04926-160">未使用。</span><span class="sxs-lookup"><span data-stu-id="04926-160">Not used.</span></span> <span data-ttu-id="04926-161">[**SWbemObject**](swbemobject.md)物件提供相同的方法。</span><span class="sxs-lookup"><span data-stu-id="04926-161">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="04926-162">**SpawnDerivedClass\_**</span><span class="sxs-lookup"><span data-stu-id="04926-162">**SpawnDerivedClass\_**</span></span>                                  | <span data-ttu-id="04926-163">未使用。</span><span class="sxs-lookup"><span data-stu-id="04926-163">Not used.</span></span> <span data-ttu-id="04926-164">[**SWbemObject**](swbemobject.md)物件提供相同的方法。</span><span class="sxs-lookup"><span data-stu-id="04926-164">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="04926-165">**SpawnInstance\_**</span><span class="sxs-lookup"><span data-stu-id="04926-165">**SpawnInstance\_**</span></span>                                      | <span data-ttu-id="04926-166">未使用。</span><span class="sxs-lookup"><span data-stu-id="04926-166">Not used.</span></span> <span data-ttu-id="04926-167">[**SWbemObject**](swbemobject.md)物件提供相同的方法。</span><span class="sxs-lookup"><span data-stu-id="04926-167">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="04926-168">**子\_**</span><span class="sxs-lookup"><span data-stu-id="04926-168">**Subclasses\_**</span></span>                                         | <span data-ttu-id="04926-169">未使用。</span><span class="sxs-lookup"><span data-stu-id="04926-169">Not used.</span></span> <span data-ttu-id="04926-170">[**SWbemObject**](swbemobject.md)物件提供相同的方法。</span><span class="sxs-lookup"><span data-stu-id="04926-170">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="04926-171">**SubclassesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="04926-171">**SubclassesAsync\_**</span></span>                                    | <span data-ttu-id="04926-172">未使用。</span><span class="sxs-lookup"><span data-stu-id="04926-172">Not used.</span></span> <span data-ttu-id="04926-173">[**SWbemObject**](swbemobject.md)物件提供相同的方法。</span><span class="sxs-lookup"><span data-stu-id="04926-173">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="04926-174">屬性</span><span class="sxs-lookup"><span data-stu-id="04926-174">Properties</span></span>

<span data-ttu-id="04926-175">**SWbemLastError** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="04926-175">The **SWbemLastError** object has these properties.</span></span>



| <span data-ttu-id="04926-176">屬性</span><span class="sxs-lookup"><span data-stu-id="04926-176">Property</span></span>                                                      | <span data-ttu-id="04926-177">存取類型</span><span class="sxs-lookup"><span data-stu-id="04926-177">Access type</span></span>          | <span data-ttu-id="04926-178">Description</span><span class="sxs-lookup"><span data-stu-id="04926-178">Description</span></span>                                                                                                                                                   |
|:--------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04926-179">**衍生\_**</span><span class="sxs-lookup"><span data-stu-id="04926-179">**Derivation\_**</span></span><br/>                                   | <span data-ttu-id="04926-180">唯讀</span><span class="sxs-lookup"><span data-stu-id="04926-180">Read-only</span></span><br/> | <span data-ttu-id="04926-181">未使用。</span><span class="sxs-lookup"><span data-stu-id="04926-181">Not used.</span></span> <span data-ttu-id="04926-182">[**SWbemObject**](swbemobject.md)物件提供相同的方法。</span><span class="sxs-lookup"><span data-stu-id="04926-182">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/>                                                                  |
| <span data-ttu-id="04926-183">**方法\_**</span><span class="sxs-lookup"><span data-stu-id="04926-183">**Methods\_**</span></span> <br/>                                     | <span data-ttu-id="04926-184">唯讀</span><span class="sxs-lookup"><span data-stu-id="04926-184">Read-only</span></span><br/> | <span data-ttu-id="04926-185">未使用。</span><span class="sxs-lookup"><span data-stu-id="04926-185">Not used.</span></span> <span data-ttu-id="04926-186">[**SWbemObject**](swbemobject.md)物件提供相同的方法。</span><span class="sxs-lookup"><span data-stu-id="04926-186">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/>                                                                  |
| [<span data-ttu-id="04926-187">**路徑\_**</span><span class="sxs-lookup"><span data-stu-id="04926-187">**Path\_**</span></span>](swbemlasterror-path-.md)<br/>             | <span data-ttu-id="04926-188">唯讀</span><span class="sxs-lookup"><span data-stu-id="04926-188">Read-only</span></span><br/> | <span data-ttu-id="04926-189">包含 [**SWbemObjectPath**](swbemobjectpath.md) 物件，該物件表示目前類別或實例的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="04926-189">Contains an [**SWbemObjectPath**](swbemobjectpath.md) object that represents the object path of the current class or instance.</span></span><br/>                    |
| [<span data-ttu-id="04926-190">**屬性\_**</span><span class="sxs-lookup"><span data-stu-id="04926-190">**Properties\_**</span></span>](swbemlasterror-properties-.md)<br/> | <span data-ttu-id="04926-191">唯讀</span><span class="sxs-lookup"><span data-stu-id="04926-191">Read-only</span></span><br/> | <span data-ttu-id="04926-192">表示 **SWbemLastError** 物件的屬性集合。</span><span class="sxs-lookup"><span data-stu-id="04926-192">Represents the collection of properties of the **SWbemLastError** object.</span></span> <span data-ttu-id="04926-193">這個屬性是 [**內含**](swbempropertyset.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="04926-193">This property is an [**SWbemPropertySet**](swbempropertyset.md) object.</span></span><br/> |
| <span data-ttu-id="04926-194">**限定詞\_**</span><span class="sxs-lookup"><span data-stu-id="04926-194">**Qualifiers\_**</span></span><br/>                                   | <span data-ttu-id="04926-195">唯讀</span><span class="sxs-lookup"><span data-stu-id="04926-195">Read-only</span></span><br/> | <span data-ttu-id="04926-196">未使用。</span><span class="sxs-lookup"><span data-stu-id="04926-196">Not used.</span></span> <span data-ttu-id="04926-197">[**SWbemObject**](swbemobject.md)物件提供相同的方法。</span><span class="sxs-lookup"><span data-stu-id="04926-197">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/>                                                                  |
| <span data-ttu-id="04926-198">**安全性\_**</span><span class="sxs-lookup"><span data-stu-id="04926-198">**Security\_**</span></span><br/>                                     | <span data-ttu-id="04926-199">唯讀</span><span class="sxs-lookup"><span data-stu-id="04926-199">Read-only</span></span><br/> | <span data-ttu-id="04926-200">未使用。</span><span class="sxs-lookup"><span data-stu-id="04926-200">Not used.</span></span> <span data-ttu-id="04926-201">[**SWbemObject**](swbemobject.md)物件提供相同的方法。</span><span class="sxs-lookup"><span data-stu-id="04926-201">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/>                                                                  |



 

## <a name="examples"></a><span data-ttu-id="04926-202">範例</span><span class="sxs-lookup"><span data-stu-id="04926-202">Examples</span></span>

<span data-ttu-id="04926-203">下列 VBScript 範例示範如何檢查錯誤和錯誤物件資訊。</span><span class="sxs-lookup"><span data-stu-id="04926-203">The following VBScript sample demonstrates how to inspect error and error object information.</span></span>


```VB
On Error Resume Next

'Ask for non-existent class to force error

Set t_Service = GetObject("winmgmts://./root/default")
Set t_Object = t_Service.Get("Nosuchclass000")

if Err = 0 Then
 WScript.Echo "Got a class"
Else
 WScript.Echo ""
 WScript.Echo "Err Information:"
 WScript.Echo ""
 WScript.Echo "  Source:", Err.Source
 WScript.Echo "  Description:", Err.Description
 WScript.Echo "  Number", "0x" & Hex(Err.Number)

 'Create the last error object
 set t_Object = CreateObject("WbemScripting.SWbemLastError")
 WScript.Echo ""
 WScript.Echo "WMI Last Error Information:"
 WScript.Echo ""
 WScript.Echo " Operation:", t_Object.Operation
 WScript.Echo " Provider:", t_Object.ProviderName

 strDescr = t_Object.Description
 strPInfo = t_Object.ParameterInfo
 strCode = t_Object.StatusCode

 if (strDescr <> nothing) Then
  WScript.Echo " Description:", strDescr  
 end if

 if (strPInfo <> nothing) Then
  WScript.Echo " Parameter Info:", strPInfo  
 end if

 if (strCode <> nothing) Then
  WScript.Echo " Status:", strCode  
 end if

 WScript.Echo ""
 Err.Clear
 set t_Object2 = CreateObject("WbemScripting.SWbemLastError")
 if Err = 0 Then
    WScript.Echo "Got the error object again - this shouldn't have happened!" 
 Else
    Err.Clear
    WScript.Echo "Couldn't get last error again - as expected"
 End if
End If

```



<span data-ttu-id="04926-204">下列 Perl 範例示範如何檢查錯誤和錯誤物件資訊。</span><span class="sxs-lookup"><span data-stu-id="04926-204">The following Perl sample demonstrates how to inspect error and error object information.</span></span>


```
use strict;
use Win32::OLE;

my ( $t_Service, $t_Object, $t_Object2, $strDescr, $strPInfo, $strCode );

# Close STDERR file handle to eliminate redundant error message
close(STDERR);

# Ask for non-existent class to force error 
$t_Service = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\default"); 
$t_Object = $t_Service->Get("Nosuchclass000");

if (defined $t_Object)
{
 print "Got a class\n"; 
}
else
{
 print "\nErr Information:\n\n";
 print Win32::OLE->LastError, "\n";

 # Create the last error object
 $t_Object = new Win32::OLE 'WbemScripting.SWbemLastError';
 print "\nWMI Last Error Information:\n\n";
 print " Operation: ", $t_Object->{Operation}, "\n";
 print " Provider: ", $t_Object->{ProviderName}, "\n";
 
 $strDescr = $t_Object->{Description};
 $strPInfo = $t_Object->{ParameterInfo};
 $strCode = $t_Object->{StatusCode};

 if (defined $strDescr)
 {
  print " Description: ", $strDescr, "\n";  
 }

 if (defined $strPInfo)
 {
  print " Parameter Info: ", $strPInfo, "\n";  
 }

 if (defined $strCode)
 {
  print " Status: ", $strCode, "\n";  
 }

 print "\n";

 $t_Object2 = new Win32::OLE 'WbemScripting.SWbemLastError';
 if (defined $t_Object2)
 {
  print "Got the error object again - this shouldn't have happened!\n";
 }
 else
 {
  print "Couldn't get last error again - as expected\n";
 }
}
```



## <a name="requirements"></a><span data-ttu-id="04926-205">規格需求</span><span class="sxs-lookup"><span data-stu-id="04926-205">Requirements</span></span>



| <span data-ttu-id="04926-206">需求</span><span class="sxs-lookup"><span data-stu-id="04926-206">Requirement</span></span> | <span data-ttu-id="04926-207">值</span><span class="sxs-lookup"><span data-stu-id="04926-207">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="04926-208">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="04926-208">Minimum supported client</span></span><br/> | <span data-ttu-id="04926-209">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="04926-209">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="04926-210">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="04926-210">Minimum supported server</span></span><br/> | <span data-ttu-id="04926-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="04926-211">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="04926-212">標頭</span><span class="sxs-lookup"><span data-stu-id="04926-212">Header</span></span><br/>                   | <dl> <span data-ttu-id="04926-213"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="04926-213"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="04926-214">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="04926-214">Type library</span></span><br/>             | <dl> <span data-ttu-id="04926-215"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="04926-215"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="04926-216">DLL</span><span class="sxs-lookup"><span data-stu-id="04926-216">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04926-217"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04926-217"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="04926-218">CLSID</span><span class="sxs-lookup"><span data-stu-id="04926-218">CLSID</span></span><br/>                    | <span data-ttu-id="04926-219">CLSID \_ SWbemLastError</span><span class="sxs-lookup"><span data-stu-id="04926-219">CLSID\_SWbemLastError</span></span><br/>                                                        |
| <span data-ttu-id="04926-220">IID</span><span class="sxs-lookup"><span data-stu-id="04926-220">IID</span></span><br/>                      | <span data-ttu-id="04926-221">IID \_ ISWbemLastError</span><span class="sxs-lookup"><span data-stu-id="04926-221">IID\_ISWbemLastError</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="04926-222">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04926-222">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04926-223">腳本 API 物件</span><span class="sxs-lookup"><span data-stu-id="04926-223">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 





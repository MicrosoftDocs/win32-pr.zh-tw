---
description: SWbemNamedValueSet 物件是 SWbemNamedValue 物件的集合。
ms.assetid: 7d1c3a28-d0d3-4108-9628-74ad483e328e
ms.tgt_platform: multiple
title: 'SWbemNamedValueSet 物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet
- ISWbemNamedValueSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2b3048b8589666a07958251ed4c0d56100132fd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982340"
---
# <a name="swbemnamedvalueset-object"></a><span data-ttu-id="7f33d-103">SWbemNamedValueSet 物件</span><span class="sxs-lookup"><span data-stu-id="7f33d-103">SWbemNamedValueSet object</span></span>

<span data-ttu-id="7f33d-104">**SWbemNamedValueSet** 物件是 [**SWbemNamedValue**](swbemnamedvalue.md)物件的集合。</span><span class="sxs-lookup"><span data-stu-id="7f33d-104">An **SWbemNamedValueSet** object is a collection of [**SWbemNamedValue**](swbemnamedvalue.md) objects.</span></span> <span data-ttu-id="7f33d-105">**SWbemNamedValueSet** 的方法和屬性主要是在送出 WMI 的某些呼叫時，將更多資訊傳送給提供者。</span><span class="sxs-lookup"><span data-stu-id="7f33d-105">The methods and properties of **SWbemNamedValueSet** are used principally to send more information to providers when submitting certain calls to WMI.</span></span> <span data-ttu-id="7f33d-106">[**SWbemServices**](swbemservices.md)中的所有呼叫，以及 [**SWbemObject**](swbemobject.md)中的某些呼叫，會採用屬於此類型之物件的選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="7f33d-106">All calls in [**SWbemServices**](swbemservices.md), and some calls in [**SWbemObject**](swbemobject.md), take an optional parameter that is an object of this type.</span></span> <span data-ttu-id="7f33d-107">用戶端可以將資訊新增至 **SWbemNamedValueSet** 物件，並以呼叫的其中一個參數來傳送 **SWbemNamedValueSet** 物件。</span><span class="sxs-lookup"><span data-stu-id="7f33d-107">A client can add information to an **SWbemNamedValueSet** object, and send the **SWbemNamedValueSet** object with the call as one of the parameters.</span></span> <span data-ttu-id="7f33d-108">這個物件可以由 VBScript **CreateObject** 呼叫建立。</span><span class="sxs-lookup"><span data-stu-id="7f33d-108">This object can be created by the VBScript **CreateObject** call.</span></span>

<span data-ttu-id="7f33d-109">如需詳細資訊，請參閱 [存取集合](accessing-a-collection.md)。</span><span class="sxs-lookup"><span data-stu-id="7f33d-109">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

> [!Note]  
> <span data-ttu-id="7f33d-110">重要-可能的話，請勿使用這項機制，因為它可以中斷以 WMI 為基礎的統一存取模型。</span><span class="sxs-lookup"><span data-stu-id="7f33d-110">Important - If possible, do not use this mechanism because it can break the uniform access model that is the basis of WMI.</span></span> <span data-ttu-id="7f33d-111">如果提供者使用此機制，請務必盡可能謹慎使用這項機制。</span><span class="sxs-lookup"><span data-stu-id="7f33d-111">If a provider does use this mechanism, it is important that this mechanism is used as sparingly as possible.</span></span> <span data-ttu-id="7f33d-112">如果提供者需要大量的高度特定內容資訊來回應要求，則必須撰寫所有用戶端的程式碼，以提供這項資訊。</span><span class="sxs-lookup"><span data-stu-id="7f33d-112">If a provider requires a large amount of highly specific context information to respond to a request, all clients must be coded to provide this information.</span></span> <span data-ttu-id="7f33d-113">這種機制可讓您視需要存取這類提供者。</span><span class="sxs-lookup"><span data-stu-id="7f33d-113">This mechanism allows you to access such providers, if necessary.</span></span>

 

<span data-ttu-id="7f33d-114">**SWbemNamedValueSet** 物件是 [**SWbemNamedValue**](swbemnamedvalue.md)元素的集合。</span><span class="sxs-lookup"><span data-stu-id="7f33d-114">An **SWbemNamedValueSet** object is a collection of [**SWbemNamedValue**](swbemnamedvalue.md) elements.</span></span> <span data-ttu-id="7f33d-115">這些專案會使用 [**SWbemNamedValueSet**](swbemnamedvalueset-add.md) 加入至集合。</span><span class="sxs-lookup"><span data-stu-id="7f33d-115">These items are added to the collection using the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method.</span></span> <span data-ttu-id="7f33d-116">它們是使用 [**SWbemNamedValueSet**](swbemnamedvalueset-remove.md) 方法來移除，並使用 [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) 方法抓取。</span><span class="sxs-lookup"><span data-stu-id="7f33d-116">They are removed using the [**SWbemNamedValueSet.Remove**](swbemnamedvalueset-remove.md) method and retrieved using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="7f33d-117">您可以存取方法，以填入動態提供者所需的任何內容資訊。</span><span class="sxs-lookup"><span data-stu-id="7f33d-117">You can access the methods to fill in any context information that is required by a dynamic provider.</span></span> <span data-ttu-id="7f33d-118">呼叫其中一個 [**SWbemServices**](swbemservices.md) 方法之後，您可以重複使用 **SWbemNamedValueSet** 物件進行另一個呼叫。</span><span class="sxs-lookup"><span data-stu-id="7f33d-118">After you call one of the [**SWbemServices**](swbemservices.md) methods, you can reuse the **SWbemNamedValueSet** object for another call.</span></span>

<span data-ttu-id="7f33d-119">基礎提供者會決定包含在 **SWbemNamedValueSet** 物件中的資訊。</span><span class="sxs-lookup"><span data-stu-id="7f33d-119">The underlying provider determines the information that is contained in an **SWbemNamedValueSet** object.</span></span> <span data-ttu-id="7f33d-120">WMI 不會使用該資訊，而只是將它轉寄給提供者。</span><span class="sxs-lookup"><span data-stu-id="7f33d-120">WMI makes no use of the information, but simply forwards it to the provider.</span></span> <span data-ttu-id="7f33d-121">提供者必須發佈服務要求所需的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="7f33d-121">Providers must publish the context information they require to service requests.</span></span>

## <a name="members"></a><span data-ttu-id="7f33d-122">成員</span><span class="sxs-lookup"><span data-stu-id="7f33d-122">Members</span></span>

<span data-ttu-id="7f33d-123">**SWbemNamedValueSet** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7f33d-123">The **SWbemNamedValueSet** object has these types of members:</span></span>

-   [<span data-ttu-id="7f33d-124">方法</span><span class="sxs-lookup"><span data-stu-id="7f33d-124">Methods</span></span>](#methods)
-   [<span data-ttu-id="7f33d-125">屬性</span><span class="sxs-lookup"><span data-stu-id="7f33d-125">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7f33d-126">方法</span><span class="sxs-lookup"><span data-stu-id="7f33d-126">Methods</span></span>

<span data-ttu-id="7f33d-127">**SWbemNamedValueSet** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="7f33d-127">The **SWbemNamedValueSet** object has these methods.</span></span>



| <span data-ttu-id="7f33d-128">方法</span><span class="sxs-lookup"><span data-stu-id="7f33d-128">Method</span></span>                                            | <span data-ttu-id="7f33d-129">描述</span><span class="sxs-lookup"><span data-stu-id="7f33d-129">Description</span></span>                                                                                                                              |
|:--------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7f33d-130">**添加**</span><span class="sxs-lookup"><span data-stu-id="7f33d-130">**Add**</span></span>](swbemnamedvalueset-add.md)             | <span data-ttu-id="7f33d-131">將 [**SWbemNamedValue**](swbemnamedvalue.md) 物件加入至集合。</span><span class="sxs-lookup"><span data-stu-id="7f33d-131">Adds an [**SWbemNamedValue**](swbemnamedvalue.md) object to the collection.</span></span><br/>                                                  |
| [<span data-ttu-id="7f33d-132">**克隆**</span><span class="sxs-lookup"><span data-stu-id="7f33d-132">**Clone**</span></span>](swbemnamedvalueset-clone.md)         | <span data-ttu-id="7f33d-133">製作這個 **SWbemNamedValueSet** 集合的複本。</span><span class="sxs-lookup"><span data-stu-id="7f33d-133">Makes a copy of this **SWbemNamedValueSet** collection.</span></span><br/>                                                                       |
| [<span data-ttu-id="7f33d-134">**DeleteAll**</span><span class="sxs-lookup"><span data-stu-id="7f33d-134">**DeleteAll**</span></span>](swbemnamedvalueset-deleteall.md) | <span data-ttu-id="7f33d-135">從集合中移除所有專案，使 **SWbemNamedValueSet** 物件空白。</span><span class="sxs-lookup"><span data-stu-id="7f33d-135">Removes all items from the collection, making the **SWbemNamedValueSet** object empty.</span></span><br/>                                        |
| [<span data-ttu-id="7f33d-136">**項目**</span><span class="sxs-lookup"><span data-stu-id="7f33d-136">**Item**</span></span>](swbemnamedvalueset-item.md)           | <span data-ttu-id="7f33d-137">從集合中捕獲 [**SWbemNamedValue**](swbemnamedvalue.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="7f33d-137">Retrieves an [**SWbemNamedValue**](swbemnamedvalue.md) object from the collection.</span></span> <span data-ttu-id="7f33d-138">這是物件的預設方法。</span><span class="sxs-lookup"><span data-stu-id="7f33d-138">This is the default method of the object.</span></span><br/> |
| [<span data-ttu-id="7f33d-139">**移除**</span><span class="sxs-lookup"><span data-stu-id="7f33d-139">**Remove**</span></span>](swbemnamedvalueset-remove.md)       | <span data-ttu-id="7f33d-140">從集合中移除 [**SWbemNamedValue**](swbemnamedvalue.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="7f33d-140">Removes an [**SWbemNamedValue**](swbemnamedvalue.md) object from the collection.</span></span><br/>                                             |



 

### <a name="properties"></a><span data-ttu-id="7f33d-141">屬性</span><span class="sxs-lookup"><span data-stu-id="7f33d-141">Properties</span></span>

<span data-ttu-id="7f33d-142">**SWbemNamedValueSet** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7f33d-142">The **SWbemNamedValueSet** object has these properties.</span></span>



| <span data-ttu-id="7f33d-143">屬性</span><span class="sxs-lookup"><span data-stu-id="7f33d-143">Property</span></span>                                             | <span data-ttu-id="7f33d-144">存取類型</span><span class="sxs-lookup"><span data-stu-id="7f33d-144">Access type</span></span>          | <span data-ttu-id="7f33d-145">Description</span><span class="sxs-lookup"><span data-stu-id="7f33d-145">Description</span></span>                                       |
|:-----------------------------------------------------|:---------------------|:--------------------------------------------------|
| [<span data-ttu-id="7f33d-146">**計數**</span><span class="sxs-lookup"><span data-stu-id="7f33d-146">**Count**</span></span>](swbemnamedvalueset-count.md)<br/> | <span data-ttu-id="7f33d-147">唯讀</span><span class="sxs-lookup"><span data-stu-id="7f33d-147">Read-only</span></span><br/> | <span data-ttu-id="7f33d-148">集合中的項目數目</span><span class="sxs-lookup"><span data-stu-id="7f33d-148">The number of items in the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="7f33d-149">範例</span><span class="sxs-lookup"><span data-stu-id="7f33d-149">Examples</span></span>

<span data-ttu-id="7f33d-150">下列 VBScript 範例示範如何操作命名值集，在此案例中，命名值為數組類型。</span><span class="sxs-lookup"><span data-stu-id="7f33d-150">The following VBScript sample demonstrates the manipulation of named value sets, in the case that the named value is an array type.</span></span>


```VB
Set Context = CreateObject("WbemScripting.SWbemNamedValueSet")

On Error Resume Next

Context.Add "n1", Array (1, 2, 3)
str = "The initial value of n1 is {"
for x=LBound(Context("n1")) to UBound(Context("n1"))
 str = str & Context("n1")(x)
 if x <> UBound(Context("n1")) Then
  str = str & ", "
 End if
next
str = str & "}"
WScript.Echo str

WScript.Echo ""

' report the value of an element of the context value
v = Context("n1")
WScript.Echo "By indirection the first element of n1 has value:",v(0)

' report the value directly
WScript.Echo "By direct access the first element of n1 has value:", Context("n1")(0)

' set the value of a single named value element
Context("n1")(1) = 11 
WScript.Echo "After direct assignment the first element of n1 has value:", Context("n1")(1)

' set the value of a single named value element
Set v = Context("n1")
v(1) = 345
WScript.Echo "After indirect assignment the first element of n1 has value:", Context("n1")(1)

' set the value of an entire context value
Context("n1") = Array (5, 34, 178871)
WScript.Echo "After direct array assignment the first element of n1 has value:", Context("n1")(1)

str = "After direct assignment the entire value of n1 is {"
for x=LBound(Context("n1")) to UBound(Context("n1"))
 str = str & Context("n1")(x)
 if x <> UBound(Context("n1")) Then
  str = str & ", "
 End if
next
str = str & "}"
WScript.Echo str

if Err <> 0 Then
 WScript.Echo Err.Description
 Err.Clear
End if
```



<span data-ttu-id="7f33d-151">下列 Perl 範例示範如何操作命名值集，在此案例中，命名值為數組類型。</span><span class="sxs-lookup"><span data-stu-id="7f33d-151">The following Perl sample demonstrates the manipulation of named value sets, in the case that the named value is an array type.</span></span>


```
use strict;
use Win32::OLE;

my ( $Context, $str, $x, @v);

eval {$Context = new Win32::OLE 'WbemScripting.SWbemNamedValueSet'; };
unless($@)
{
 $Context->Add("n1", [1, 2, 3]);
 $str = "The initial value of n1 is {";
 for ($x = 0; $x < @{$Context->Item("n1")->{Value}}; $x++)
 {
  $str = $str.@{$Context->Item("n1")->{Value}}[$x];
  if ($x != (@{$Context->Item("n1")->{Value}}) - 1 )
  {
   $str = $str.", ";
  }
 }
 $str = $str."}";
 print $str,"\n\n";

 # report the value of an element of the context value
 @v = @{$Context->Item("n1")->{Value}};
 print "By indirection the first element of n1 has value:", $v[0], "\n";

 # report the value directly
 print "By direct access the first element of n1 has value:", @{$Context->Item("n1")->{Value}}[0], "\n";

 # set the value of a single named value element
 @{$Context->Item("n1")->{Value}}[1] = 11;
 print "After direct assignment the first element of n1 has value:", 
       @{$Context->Item("n1")->{Value}}[1], "\n";

 # set the value of a single named value element
 @v = @{$Context->Item("n1")->{Value}};
 $v[1] = 345;
 print "After indirect assignment the first element of n1 has value:", 
    @{$Context->Item("n1")->{Value}}[1], "\n";

 # set the value of an entire context value
 $Context->Item("n1")->{Value} = [5, 34, 178871];
 print "After direct array assignment the first element of n1 has value:", 
   @{$Context->Item("n1")->{Value}}[1], "\n";

 $str = "After direct assignment the entire value of n1 is {";
 for ($x = 0; $x < @{$Context->Item("n1")->{Value}}; $x++)
 {
  $str = $str.@{$Context->Item("n1")->{Value}}[$x];
  if ($x != (@{$Context->Item("n1")->{Value}}) - 1 )
  {
   $str = $str.", ";
  }
 }
 $str = $str."}";
 print $str,"\n";
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="7f33d-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f33d-152">Requirements</span></span>



| <span data-ttu-id="7f33d-153">需求</span><span class="sxs-lookup"><span data-stu-id="7f33d-153">Requirement</span></span> | <span data-ttu-id="7f33d-154">值</span><span class="sxs-lookup"><span data-stu-id="7f33d-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f33d-155">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7f33d-155">Minimum supported client</span></span><br/> | <span data-ttu-id="7f33d-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7f33d-156">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7f33d-157">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7f33d-157">Minimum supported server</span></span><br/> | <span data-ttu-id="7f33d-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7f33d-158">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7f33d-159">標頭</span><span class="sxs-lookup"><span data-stu-id="7f33d-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f33d-160"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="7f33d-160"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7f33d-161">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="7f33d-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="7f33d-162"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7f33d-162"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7f33d-163">DLL</span><span class="sxs-lookup"><span data-stu-id="7f33d-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f33d-164"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f33d-164"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7f33d-165">CLSID</span><span class="sxs-lookup"><span data-stu-id="7f33d-165">CLSID</span></span><br/>                    | <span data-ttu-id="7f33d-166">CLSID \_ SWbemNamedValueSet</span><span class="sxs-lookup"><span data-stu-id="7f33d-166">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="7f33d-167">IID</span><span class="sxs-lookup"><span data-stu-id="7f33d-167">IID</span></span><br/>                      | <span data-ttu-id="7f33d-168">IID \_ ISWbemNamedValueSet</span><span class="sxs-lookup"><span data-stu-id="7f33d-168">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="7f33d-169">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f33d-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f33d-170">腳本 API 物件</span><span class="sxs-lookup"><span data-stu-id="7f33d-170">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 





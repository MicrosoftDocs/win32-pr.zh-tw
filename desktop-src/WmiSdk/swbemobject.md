---
description: 您可以使用 SWbemObject 物件的方法和屬性，來代表 (WMI) 類別定義或物件實例的一個 Windows Management Instrumentation。
ms.assetid: d303ec1a-5e0c-4a5e-8ed3-ed353a138755
ms.tgt_platform: multiple
title: 'SWbemObject 物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject
- ISWbemObject
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 287395b976177170c8bdffa0e1817a8755a4d397
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971715"
---
# <a name="swbemobject-object"></a><span data-ttu-id="1b8da-103">SWbemObject 物件</span><span class="sxs-lookup"><span data-stu-id="1b8da-103">SWbemObject object</span></span>

<span data-ttu-id="1b8da-104">您可以使用 **SWbemObject** 物件的方法和屬性，來代表 (WMI) 類別定義或物件實例的一個 Windows Management Instrumentation。</span><span class="sxs-lookup"><span data-stu-id="1b8da-104">You can use the methods and properties of the **SWbemObject** object to represent one Windows Management Instrumentation (WMI) class definition or object instance.</span></span> <span data-ttu-id="1b8da-105">VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) 呼叫無法建立這個物件。</span><span class="sxs-lookup"><span data-stu-id="1b8da-105">This object cannot be created by the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) call.</span></span>

<span data-ttu-id="1b8da-106">此物件支援兩種類型的屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="1b8da-106">This object supports two types of properties and methods.</span></span> <span data-ttu-id="1b8da-107">本節中定義的屬性是套用至所有 WMI 物件的一般屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="1b8da-107">Those defined in this section are generic properties and methods that apply to all WMI objects.</span></span> <span data-ttu-id="1b8da-108">此外，這個物件會公開基礎物件的屬性和方法，作為動態 automation 屬性和 **SWbemObject** 的方法。</span><span class="sxs-lookup"><span data-stu-id="1b8da-108">In addition, this object exposes the properties and methods of the underlying object as dynamic automation properties and methods of **SWbemObject**.</span></span> <span data-ttu-id="1b8da-109">這些屬性和方法的名稱和類型相依于基礎 WMI 物件。</span><span class="sxs-lookup"><span data-stu-id="1b8da-109">The names and types of these properties and methods depend on the underlying WMI object.</span></span> <span data-ttu-id="1b8da-110">如需如何公開這些動態屬性和方法的詳細資訊，請參閱 [操作類別和實例資訊](manipulating-class-and-instance-information.md)。</span><span class="sxs-lookup"><span data-stu-id="1b8da-110">For more information about how these dynamic properties and methods are exposed, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="1b8da-111">從 WMI 用戶端的觀點來看，這個物件永遠都是同進程。</span><span class="sxs-lookup"><span data-stu-id="1b8da-111">From the WMI client perspective, this object is always in-process.</span></span> <span data-ttu-id="1b8da-112">寫入作業只會影響物件的本機複本，而讀取作業一律會從本機複本取出值。</span><span class="sxs-lookup"><span data-stu-id="1b8da-112">Write operations only affect the local copy of the object, and read operations always retrieve values from the local copy.</span></span> <span data-ttu-id="1b8da-113">只有在使用 [**SWbemObject \_**](swbemobject-put-.md)的呼叫來寫入整個物件時，才會執行 WMI 的更新。</span><span class="sxs-lookup"><span data-stu-id="1b8da-113">Updates to WMI are performed only when entire objects are written using a call to the [**SWbemObject.Put\_**](swbemobject-put-.md) method.</span></span> <span data-ttu-id="1b8da-114">如果您修改 **SWbemObject** 物件中的屬性或方法，則在呼叫 **SWbemObject \_** 之前，您的變更不會寫入至 WMI。</span><span class="sxs-lookup"><span data-stu-id="1b8da-114">If you modify the properties or methods in an **SWbemObject** object, your changes are not written to WMI until you call **SWbemObject.Put\_**.</span></span>

<span data-ttu-id="1b8da-115">此區段中定義的泛型方法和屬性名稱一律以尾端底線結尾 ( " \_ " ) 來區別它們與基礎物件的動態 WMI 方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="1b8da-115">The generic method and property names defined in this section always end with a trailing underscore ("\_") to differentiate them from the dynamic WMI methods and properties of the underlying object.</span></span>

<span data-ttu-id="1b8da-116">請注意， **SWbemObject** 無法使用 VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx). 方法來建立。</span><span class="sxs-lookup"><span data-stu-id="1b8da-116">Note that **SWbemObject** cannot be created using the VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx).method.</span></span> <span data-ttu-id="1b8da-117">如果您想要建立新的空白類別，請使用 [**SWbemServices。 Get**](swbemservices-get.md) 具有空的 path 參數。</span><span class="sxs-lookup"><span data-stu-id="1b8da-117">If you want to create a new, empty class use [**SWbemServices.Get**](swbemservices-get.md) with an empty path parameter.</span></span> <span data-ttu-id="1b8da-118">此呼叫會傳回空的 **SWbemObject** 物件，該物件可以成為類別。</span><span class="sxs-lookup"><span data-stu-id="1b8da-118">This call returns an empty **SWbemObject** object that can become a class.</span></span> <span data-ttu-id="1b8da-119">然後，您可以為 [**\_ 路徑**](swbemobject-path-.md)呼叫所傳回之 [**SWbemObjectPath**](swbemobjectpath.md)物件的 [**class**](swbemobjectpath-class.md)屬性提供類別名稱。</span><span class="sxs-lookup"><span data-stu-id="1b8da-119">You can then supply a class name for the [**Class**](swbemobjectpath-class.md) property of the [**SWbemObjectPath**](swbemobjectpath.md) object returned by the [**Path\_**](swbemobject-path-.md) call.</span></span> <span data-ttu-id="1b8da-120">由 [**properties \_**](swbemobject-properties-.md)方法將屬性加入至新的類別。</span><span class="sxs-lookup"><span data-stu-id="1b8da-120">Add properties to the new class by the [**Properties\_**](swbemobject-properties-.md) method.</span></span> <span data-ttu-id="1b8da-121">若要建立實例，請在新類別上呼叫 **GetObject** 。</span><span class="sxs-lookup"><span data-stu-id="1b8da-121">To create an instance, call **GetObject** on the new class.</span></span>

<span data-ttu-id="1b8da-122">下列程式碼範例示範如何取得新的類別，並在其中加入屬性。</span><span class="sxs-lookup"><span data-stu-id="1b8da-122">The following code example shows how to obtain a new class and add a property to it.</span></span> <span data-ttu-id="1b8da-123">代表類別的 **SWbemObject** 物件必須透過呼叫 Put 寫回至 WMI [**存放 \_**](swbemobject-put-.md)庫。</span><span class="sxs-lookup"><span data-stu-id="1b8da-123">The **SWbemObject** object that represents the class must be written back to the WMI repository by a call to [**Put\_**](swbemobject-put-.md).</span></span>


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
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").Spawninstance_

objNewInst.PropertyName = "My Instance"

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
WScript.Echo objInstancePath.Path

```



<span data-ttu-id="1b8da-124">您可以使用 [CIM Studio](further-information.md) 之類的查看工具來檢查存放庫，以確認新的類別和實例出現。</span><span class="sxs-lookup"><span data-stu-id="1b8da-124">You can examine the repository with a viewing tool such as [CIM Studio](further-information.md) to verify that the new class and instance appear.</span></span> <span data-ttu-id="1b8da-125">如需從存放庫中移除類別和實例的範例，請參閱 [**SWbemServices。刪除**](swbemservices-delete.md)或 [**\_ SWbemObject。**](swbemobject-delete-.md)</span><span class="sxs-lookup"><span data-stu-id="1b8da-125">For an example of removing a class and instance from the repository, see [**SWbemServices.Delete**](swbemservices-delete.md) or [**SWbemObject.Delete\_**](swbemobject-delete-.md).</span></span>

## <a name="members"></a><span data-ttu-id="1b8da-126">成員</span><span class="sxs-lookup"><span data-stu-id="1b8da-126">Members</span></span>

<span data-ttu-id="1b8da-127">**SWbemObject** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1b8da-127">The **SWbemObject** object has these types of members:</span></span>

-   [<span data-ttu-id="1b8da-128">方法</span><span class="sxs-lookup"><span data-stu-id="1b8da-128">Methods</span></span>](#methods)
-   [<span data-ttu-id="1b8da-129">屬性</span><span class="sxs-lookup"><span data-stu-id="1b8da-129">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1b8da-130">方法</span><span class="sxs-lookup"><span data-stu-id="1b8da-130">Methods</span></span>

<span data-ttu-id="1b8da-131">**SWbemObject** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="1b8da-131">The **SWbemObject** object has these methods.</span></span>



| <span data-ttu-id="1b8da-132">方法</span><span class="sxs-lookup"><span data-stu-id="1b8da-132">Method</span></span>                                                        | <span data-ttu-id="1b8da-133">描述</span><span class="sxs-lookup"><span data-stu-id="1b8da-133">Description</span></span>                                                                                             |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1b8da-134">**Associators of\_**</span><span class="sxs-lookup"><span data-stu-id="1b8da-134">**Associators\_**</span></span>](swbemobject-associators-.md)             | <span data-ttu-id="1b8da-135">抓取物件的 associators of。</span><span class="sxs-lookup"><span data-stu-id="1b8da-135">Retrieves the associators of the object.</span></span><br/>                                                     |
| [<span data-ttu-id="1b8da-136">**AssociatorsAsync\_**</span><span class="sxs-lookup"><span data-stu-id="1b8da-136">**AssociatorsAsync\_**</span></span>](swbemobject-associatorsasync-.md)   | <span data-ttu-id="1b8da-137">以非同步方式抓取物件的 associators of。</span><span class="sxs-lookup"><span data-stu-id="1b8da-137">Asynchronously retrieves the associators of the object.</span></span><br/>                                      |
| [<span data-ttu-id="1b8da-138">**克隆\_**</span><span class="sxs-lookup"><span data-stu-id="1b8da-138">**Clone\_**</span></span>](swbemobject-clone-.md)                         | <span data-ttu-id="1b8da-139">建立目前物件的複本。</span><span class="sxs-lookup"><span data-stu-id="1b8da-139">Makes a copy of the current object.</span></span><br/>                                                          |
| [<span data-ttu-id="1b8da-140">**CompareTo\_**</span><span class="sxs-lookup"><span data-stu-id="1b8da-140">**CompareTo\_**</span></span>](swbemobject-compareto-.md)                 | <span data-ttu-id="1b8da-141">測試兩個物件是否相等。</span><span class="sxs-lookup"><span data-stu-id="1b8da-141">Tests two objects for equality.</span></span><br/>                                                              |
| [<span data-ttu-id="1b8da-142">**刪除\_**</span><span class="sxs-lookup"><span data-stu-id="1b8da-142">**Delete\_**</span></span>](swbemobject-delete-.md)                       | <span data-ttu-id="1b8da-143">從 WMI 刪除物件。</span><span class="sxs-lookup"><span data-stu-id="1b8da-143">Deletes the object from WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="1b8da-144">**DeleteAsync\_**</span><span class="sxs-lookup"><span data-stu-id="1b8da-144">**DeleteAsync\_**</span></span>](swbemobject-deleteasync-.md)             | <span data-ttu-id="1b8da-145">以非同步方式從 WMI 刪除物件。</span><span class="sxs-lookup"><span data-stu-id="1b8da-145">Asynchronously deletes the object from WMI.</span></span><br/>                                                  |
| [<span data-ttu-id="1b8da-146">**ExecMethod\_**</span><span class="sxs-lookup"><span data-stu-id="1b8da-146">**ExecMethod\_**</span></span>](swbemobject-execmethod-.md)               | <span data-ttu-id="1b8da-147">執行方法提供者所匯出的方法。</span><span class="sxs-lookup"><span data-stu-id="1b8da-147">Executes a method exported by a method provider.</span></span><br/>                                             |
| [<span data-ttu-id="1b8da-148">**ExecMethodAsync\_**</span><span class="sxs-lookup"><span data-stu-id="1b8da-148">**ExecMethodAsync\_**</span></span>](swbemobject-execmethodasync-.md)     | <span data-ttu-id="1b8da-149">以非同步方式執行方法提供者所匯出的方法。</span><span class="sxs-lookup"><span data-stu-id="1b8da-149">Asynchronously executes a method exported by a method provider.</span></span><br/>                              |
| [<span data-ttu-id="1b8da-150">**GetObjectText\_**</span><span class="sxs-lookup"><span data-stu-id="1b8da-150">**GetObjectText\_**</span></span>](swbemobject-getobjecttext-.md)         | <span data-ttu-id="1b8da-151">抓取物件 (MOF 語法) 的文字標記法。</span><span class="sxs-lookup"><span data-stu-id="1b8da-151">Retrieves the textual representation of the object (MOF syntax).</span></span><br/>                             |
| [<span data-ttu-id="1b8da-152">**執行個體\_**</span><span class="sxs-lookup"><span data-stu-id="1b8da-152">**Instances\_**</span></span>](swbemobject-instances-.md)                 | <span data-ttu-id="1b8da-153">傳回物件的實例集合， (必須是) 的 WMI 類別。</span><span class="sxs-lookup"><span data-stu-id="1b8da-153">Returns a collection of instances of the object (which must be a WMI class).</span></span><br/>                 |
| [<span data-ttu-id="1b8da-154">**InstancesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="1b8da-154">**InstancesAsync\_**</span></span>](swbemobject-instancesasync-.md)       | <span data-ttu-id="1b8da-155">以非同步方式傳回物件的實例集合 (必須是 WMI 類別) 。</span><span class="sxs-lookup"><span data-stu-id="1b8da-155">Asynchronously returns a collection of instances of the object (which must be a WMI class).</span></span><br/>  |
| [<span data-ttu-id="1b8da-156">**把\_**</span><span class="sxs-lookup"><span data-stu-id="1b8da-156">**Put\_**</span></span>](swbemobject-put-.md)                             | <span data-ttu-id="1b8da-157">在 WMI 中建立或更新物件。</span><span class="sxs-lookup"><span data-stu-id="1b8da-157">Creates or updates the object in WMI.</span></span><br/>                                                        |
| [<span data-ttu-id="1b8da-158">**PutAsync\_**</span><span class="sxs-lookup"><span data-stu-id="1b8da-158">**PutAsync\_**</span></span>](swbemobject-putasync-.md)                   | <span data-ttu-id="1b8da-159">在 WMI 中以非同步方式建立或更新物件。</span><span class="sxs-lookup"><span data-stu-id="1b8da-159">Asynchronously creates or updates the object in WMI.</span></span><br/>                                         |
| [<span data-ttu-id="1b8da-160">**參考資料\_**</span><span class="sxs-lookup"><span data-stu-id="1b8da-160">**References\_**</span></span>](swbemobject-references-.md)               | <span data-ttu-id="1b8da-161">傳回物件的參考。</span><span class="sxs-lookup"><span data-stu-id="1b8da-161">Returns references to the object.</span></span><br/>                                                            |
| [<span data-ttu-id="1b8da-162">**ReferencesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="1b8da-162">**ReferencesAsync\_**</span></span>](swbemobject-referencesasync-.md)     | <span data-ttu-id="1b8da-163">以非同步方式傳回物件的參考。</span><span class="sxs-lookup"><span data-stu-id="1b8da-163">Asynchronously returns references to the object.</span></span><br/>                                             |
| [<span data-ttu-id="1b8da-164">**SpawnDerivedClass\_**</span><span class="sxs-lookup"><span data-stu-id="1b8da-164">**SpawnDerivedClass\_**</span></span>](swbemobject-spawnderivedclass-.md) | <span data-ttu-id="1b8da-165">從目前物件建立新的衍生類別， (必須是) 的 WMI 類別。</span><span class="sxs-lookup"><span data-stu-id="1b8da-165">Creates a new derived class from the current object (which must be a WMI class).</span></span><br/>             |
| [<span data-ttu-id="1b8da-166">**SpawnInstance\_**</span><span class="sxs-lookup"><span data-stu-id="1b8da-166">**SpawnInstance\_**</span></span>](swbemobject-spawninstance-.md)         | <span data-ttu-id="1b8da-167">從目前的物件建立新的實例。</span><span class="sxs-lookup"><span data-stu-id="1b8da-167">Creates a new instance from the current object.</span></span><br/>                                              |
| [<span data-ttu-id="1b8da-168">**子\_**</span><span class="sxs-lookup"><span data-stu-id="1b8da-168">**Subclasses\_**</span></span>](swbemobject-subclasses-.md)               | <span data-ttu-id="1b8da-169">傳回物件的子類別集合 (必須是) 的 WMI 類別。</span><span class="sxs-lookup"><span data-stu-id="1b8da-169">Returns a collection of subclasses of the object (which must be a WMI class).</span></span><br/>                |
| [<span data-ttu-id="1b8da-170">**SubclassesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="1b8da-170">**SubclassesAsync\_**</span></span>](swbemobject-subclassesasync-.md)     | <span data-ttu-id="1b8da-171">以非同步方式傳回物件的子類別集合 (必須是) 的 WMI 類別。</span><span class="sxs-lookup"><span data-stu-id="1b8da-171">Asynchronously returns a collection of subclasses of the object (which must be a WMI class).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1b8da-172">屬性</span><span class="sxs-lookup"><span data-stu-id="1b8da-172">Properties</span></span>

<span data-ttu-id="1b8da-173">**SWbemObject** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1b8da-173">The **SWbemObject** object has these properties.</span></span>



| <span data-ttu-id="1b8da-174">屬性</span><span class="sxs-lookup"><span data-stu-id="1b8da-174">Property</span></span>                                                   | <span data-ttu-id="1b8da-175">存取類型</span><span class="sxs-lookup"><span data-stu-id="1b8da-175">Access type</span></span>          | <span data-ttu-id="1b8da-176">Description</span><span class="sxs-lookup"><span data-stu-id="1b8da-176">Description</span></span>                                                                                                                                |
|:-----------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1b8da-177">**衍生\_**</span><span class="sxs-lookup"><span data-stu-id="1b8da-177">**Derivation\_**</span></span>](swbemobject-derivation-.md)<br/> | <span data-ttu-id="1b8da-178">唯讀</span><span class="sxs-lookup"><span data-stu-id="1b8da-178">Read-only</span></span><br/> | <span data-ttu-id="1b8da-179">包含描述類別之衍生階層的字串陣列。</span><span class="sxs-lookup"><span data-stu-id="1b8da-179">Contains an array of strings that describes the derivation hierarchy for the class.</span></span><br/>                                             |
| [<span data-ttu-id="1b8da-180">**方法\_**</span><span class="sxs-lookup"><span data-stu-id="1b8da-180">**Methods\_**</span></span>](swbemobject-methods-.md)<br/>       | <span data-ttu-id="1b8da-181">唯讀</span><span class="sxs-lookup"><span data-stu-id="1b8da-181">Read-only</span></span><br/> | <span data-ttu-id="1b8da-182">[**SWbemMethodSet**](swbemmethodset.md)物件，此物件為這個物件的方法集合。</span><span class="sxs-lookup"><span data-stu-id="1b8da-182">An [**SWbemMethodSet**](swbemmethodset.md) object that is the collection of methods for this object.</span></span><br/>                           |
| [<span data-ttu-id="1b8da-183">**路徑\_**</span><span class="sxs-lookup"><span data-stu-id="1b8da-183">**Path\_**</span></span>](swbemobject-path-.md)<br/>             | <span data-ttu-id="1b8da-184">唯讀</span><span class="sxs-lookup"><span data-stu-id="1b8da-184">Read-only</span></span><br/> | <span data-ttu-id="1b8da-185">包含 [**SWbemObjectPath**](swbemobjectpath.md) 物件，該物件表示目前類別或實例的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="1b8da-185">Contains an [**SWbemObjectPath**](swbemobjectpath.md) object that represents the object path of the current class or instance.</span></span><br/> |
| [<span data-ttu-id="1b8da-186">**屬性\_**</span><span class="sxs-lookup"><span data-stu-id="1b8da-186">**Properties\_**</span></span>](swbemobject-properties-.md)<br/> | <span data-ttu-id="1b8da-187">唯讀</span><span class="sxs-lookup"><span data-stu-id="1b8da-187">Read-only</span></span><br/> | <span data-ttu-id="1b8da-188">[**內含**](swbempropertyset.md)物件，此物件為這個物件的屬性集合。</span><span class="sxs-lookup"><span data-stu-id="1b8da-188">An [**SWbemPropertySet**](swbempropertyset.md) object that is the collection of properties for this object.</span></span><br/>                    |
| [<span data-ttu-id="1b8da-189">**限定詞\_**</span><span class="sxs-lookup"><span data-stu-id="1b8da-189">**Qualifiers\_**</span></span>](swbemobject-qualifiers-.md)<br/> | <span data-ttu-id="1b8da-190">唯讀</span><span class="sxs-lookup"><span data-stu-id="1b8da-190">Read-only</span></span><br/> | <span data-ttu-id="1b8da-191">[**SWbemQualifierSet**](swbemqualifierset.md)物件，此物件為這個物件的限定詞集合。</span><span class="sxs-lookup"><span data-stu-id="1b8da-191">An [**SWbemQualifierSet**](swbemqualifierset.md) object that is the collection of qualifiers for this object.</span></span><br/>                  |
| [<span data-ttu-id="1b8da-192">**安全性\_**</span><span class="sxs-lookup"><span data-stu-id="1b8da-192">**Security\_**</span></span>](swbemobject-security-.md)<br/>     | <span data-ttu-id="1b8da-193">唯讀</span><span class="sxs-lookup"><span data-stu-id="1b8da-193">Read-only</span></span><br/> | <span data-ttu-id="1b8da-194">包含用來讀取或變更安全性設定的 [**SWbemSecurity**](swbemsecurity.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="1b8da-194">Contains an [**SWbemSecurity**](swbemsecurity.md) object used to read or change the security settings.</span></span><br/>                         |



 

## <a name="examples"></a><span data-ttu-id="1b8da-195">範例</span><span class="sxs-lookup"><span data-stu-id="1b8da-195">Examples</span></span>

<span data-ttu-id="1b8da-196">這份清單列出了 TechNet 資源庫上 WMI 類別 VBScript 程式碼範例的 [所有屬性和方法](https://Gallery.TechNet.Microsoft.Com/f0666124-3b67-4254-8ff1-3b75ae15776d) ，會使用 SWbemObject 來列出所指定 WMI 類別的所有方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="1b8da-196">The [List All the Properties and Methods for a WMI Class](https://Gallery.TechNet.Microsoft.Com/f0666124-3b67-4254-8ff1-3b75ae15776d) VBScript code sample on TechNet Gallery uses the SWbemObject to list all of the methods and properties for a specified WMI class.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b8da-197">規格需求</span><span class="sxs-lookup"><span data-stu-id="1b8da-197">Requirements</span></span>



| <span data-ttu-id="1b8da-198">需求</span><span class="sxs-lookup"><span data-stu-id="1b8da-198">Requirement</span></span> | <span data-ttu-id="1b8da-199">值</span><span class="sxs-lookup"><span data-stu-id="1b8da-199">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b8da-200">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1b8da-200">Minimum supported client</span></span><br/> | <span data-ttu-id="1b8da-201">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1b8da-201">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1b8da-202">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1b8da-202">Minimum supported server</span></span><br/> | <span data-ttu-id="1b8da-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1b8da-203">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1b8da-204">標頭</span><span class="sxs-lookup"><span data-stu-id="1b8da-204">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b8da-205"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="1b8da-205"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1b8da-206">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="1b8da-206">Type library</span></span><br/>             | <dl> <span data-ttu-id="1b8da-207"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1b8da-207"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1b8da-208">DLL</span><span class="sxs-lookup"><span data-stu-id="1b8da-208">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b8da-209"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b8da-209"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1b8da-210">CLSID</span><span class="sxs-lookup"><span data-stu-id="1b8da-210">CLSID</span></span><br/>                    | <span data-ttu-id="1b8da-211">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="1b8da-211">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="1b8da-212">IID</span><span class="sxs-lookup"><span data-stu-id="1b8da-212">IID</span></span><br/>                      | <span data-ttu-id="1b8da-213">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="1b8da-213">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="1b8da-214">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1b8da-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b8da-215">**SWbemObjectEx**</span><span class="sxs-lookup"><span data-stu-id="1b8da-215">**SWbemObjectEx**</span></span>](swbemobjectex.md)
</dt> <dt>

[<span data-ttu-id="1b8da-216">腳本 API 物件</span><span class="sxs-lookup"><span data-stu-id="1b8da-216">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 


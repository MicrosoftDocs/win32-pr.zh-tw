---
description: 內含物件是 Swbempropertyset 物件的集合。
ms.assetid: 0edad17b-facc-4885-9ce4-561ca6f57a66
ms.tgt_platform: multiple
title: '內含物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet
- ISWbemPropertySet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 05ae5d5e0bfbc5ab0733e00e4649baa2849d3446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983904"
---
# <a name="swbempropertyset-object"></a><span data-ttu-id="dbe6d-103">內含物件</span><span class="sxs-lookup"><span data-stu-id="dbe6d-103">SWbemPropertySet object</span></span>

<span data-ttu-id="dbe6d-104">**內含** 物件是 [**swbempropertyset**](swbemproperty.md)物件的集合。</span><span class="sxs-lookup"><span data-stu-id="dbe6d-104">An **SWbemPropertySet** object is a collection of [**SWbemProperty**](swbemproperty.md) objects.</span></span> <span data-ttu-id="dbe6d-105">您可以使用 [**add**](swbempropertyset-add.md) 方法將專案加入集合、使用 [**Item**](swbempropertyset-item.md) 方法從集合取出專案，以及使用 [**remove**](swbempropertyset-remove.md) 方法從集合中移除專案。</span><span class="sxs-lookup"><span data-stu-id="dbe6d-105">You can add items to the collection using the [**Add**](swbempropertyset-add.md) method, retrieve items from the collection using the [**Item**](swbempropertyset-item.md) method, and remove items from the collection using the [**Remove**](swbempropertyset-remove.md) method.</span></span> <span data-ttu-id="dbe6d-106">如需詳細資訊，請參閱 [存取集合](accessing-a-collection.md)。</span><span class="sxs-lookup"><span data-stu-id="dbe6d-106">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span> <span data-ttu-id="dbe6d-107">VBScript [CreateObject](creating-an-object-using-vbscript.md) 呼叫無法建立這個物件。</span><span class="sxs-lookup"><span data-stu-id="dbe6d-107">This object cannot be created by the VBScript [CreateObject](creating-an-object-using-vbscript.md) call.</span></span>

<span data-ttu-id="dbe6d-108">組成 **內含** 集合的 [**swbempropertyset**](swbemproperty.md)物件是用來描述單一 WMI 類別或實例的屬性。</span><span class="sxs-lookup"><span data-stu-id="dbe6d-108">The [**SWbemProperty**](swbemproperty.md) objects that make up an **SWbemPropertySet** collection are used to describe the properties of a single WMI class or instance.</span></span>

## <a name="members"></a><span data-ttu-id="dbe6d-109">成員</span><span class="sxs-lookup"><span data-stu-id="dbe6d-109">Members</span></span>

<span data-ttu-id="dbe6d-110">**內含** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="dbe6d-110">The **SWbemPropertySet** object has these types of members:</span></span>

-   [<span data-ttu-id="dbe6d-111">方法</span><span class="sxs-lookup"><span data-stu-id="dbe6d-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="dbe6d-112">屬性</span><span class="sxs-lookup"><span data-stu-id="dbe6d-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dbe6d-113">方法</span><span class="sxs-lookup"><span data-stu-id="dbe6d-113">Methods</span></span>

<span data-ttu-id="dbe6d-114">**內含** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="dbe6d-114">The **SWbemPropertySet** object has these methods.</span></span>



| <span data-ttu-id="dbe6d-115">方法</span><span class="sxs-lookup"><span data-stu-id="dbe6d-115">Method</span></span>                                    | <span data-ttu-id="dbe6d-116">描述</span><span class="sxs-lookup"><span data-stu-id="dbe6d-116">Description</span></span>                                                                                                                     |
|:------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dbe6d-117">**添加**</span><span class="sxs-lookup"><span data-stu-id="dbe6d-117">**Add**</span></span>](swbempropertyset-add.md)       | <span data-ttu-id="dbe6d-118">將 [**swbempropertyset**](swbemproperty.md) 物件加入至 **內含** 集合。</span><span class="sxs-lookup"><span data-stu-id="dbe6d-118">Adds an [**SWbemProperty**](swbemproperty.md) object to the **SWbemPropertySet** collection.</span></span><br/>                        |
| [<span data-ttu-id="dbe6d-119">**項目**</span><span class="sxs-lookup"><span data-stu-id="dbe6d-119">**Item**</span></span>](swbempropertyset-item.md)     | <span data-ttu-id="dbe6d-120">從集合中取得名為 [**swbempropertyset**](swbemproperty.md) 的。</span><span class="sxs-lookup"><span data-stu-id="dbe6d-120">Gets a named [**SWbemProperty**](swbemproperty.md) from the collection.</span></span> <span data-ttu-id="dbe6d-121">這是這個物件的預設方法。</span><span class="sxs-lookup"><span data-stu-id="dbe6d-121">This is the default method for this object.</span></span><br/> |
| [<span data-ttu-id="dbe6d-122">**移除**</span><span class="sxs-lookup"><span data-stu-id="dbe6d-122">**Remove**</span></span>](swbempropertyset-remove.md) | <span data-ttu-id="dbe6d-123">從集合中刪除 [**swbempropertyset**](swbemproperty.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="dbe6d-123">Deletes an [**SWbemProperty**](swbemproperty.md) object from the collection.</span></span><br/>                                        |



 

### <a name="properties"></a><span data-ttu-id="dbe6d-124">屬性</span><span class="sxs-lookup"><span data-stu-id="dbe6d-124">Properties</span></span>

<span data-ttu-id="dbe6d-125">**內含** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="dbe6d-125">The **SWbemPropertySet** object has these properties.</span></span>



| <span data-ttu-id="dbe6d-126">屬性</span><span class="sxs-lookup"><span data-stu-id="dbe6d-126">Property</span></span>                                           | <span data-ttu-id="dbe6d-127">存取類型</span><span class="sxs-lookup"><span data-stu-id="dbe6d-127">Access type</span></span>          | <span data-ttu-id="dbe6d-128">Description</span><span class="sxs-lookup"><span data-stu-id="dbe6d-128">Description</span></span>                                                            |
|:---------------------------------------------------|:---------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="dbe6d-129">**計數**</span><span class="sxs-lookup"><span data-stu-id="dbe6d-129">**Count**</span></span>](swbempropertyset-count.md)<br/> | <span data-ttu-id="dbe6d-130">唯讀</span><span class="sxs-lookup"><span data-stu-id="dbe6d-130">Read-only</span></span><br/> | <span data-ttu-id="dbe6d-131">**內含** 集合中的專案數。</span><span class="sxs-lookup"><span data-stu-id="dbe6d-131">The number of items in the **SWbemPropertySet** collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="dbe6d-132">範例</span><span class="sxs-lookup"><span data-stu-id="dbe6d-132">Examples</span></span>

<span data-ttu-id="dbe6d-133">下列 VBScript 範例將示範如何在屬性被覆寫時， [**內含**](swbempropertyset-remove.md) 會傳回 **wbemErrResetToDefault** 。</span><span class="sxs-lookup"><span data-stu-id="dbe6d-133">The following VBScript sample demonstrates how [**SWbemPropertySet.Remove**](swbempropertyset-remove.md) can return **wbemErrResetToDefault** if the property is overridden.</span></span>


```VB
on error resume next 

'Create a keyed class with a defaulted property
set service = GetObject("Winmgmts:")
set emptyclass = service.Get
emptyclass.path_.class = "REMOVETEST00"
set prop = emptyclass.properties_.add ("p", 19)

prop.qualifiers_.add "key", true
emptyclass.properties_.add ("q", 19).Value = 12

emptyclass.put_

'create an instance and override the property
set instance = service.get ("RemoveTest00").spawninstance_

instance.properties_("q").Value = 24
instance.properties_("p").Value = 1
instance.put_

'retrieve the instance and remove the property
set instance = service.get ("removetest00=1")
set property = instance.properties_ ("q")

WScript.echo "Overridden value of property is [24]:", property.value
WScript.echo ""

instance.properties_.remove "q"
set property = instance.properties_ ("q")
WScript.echo "Value of property after removal is [12]:", property.value
WScript.echo ""

if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
end if
```



## <a name="requirements"></a><span data-ttu-id="dbe6d-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="dbe6d-134">Requirements</span></span>



| <span data-ttu-id="dbe6d-135">需求</span><span class="sxs-lookup"><span data-stu-id="dbe6d-135">Requirement</span></span> | <span data-ttu-id="dbe6d-136">值</span><span class="sxs-lookup"><span data-stu-id="dbe6d-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbe6d-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dbe6d-137">Minimum supported client</span></span><br/> | <span data-ttu-id="dbe6d-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dbe6d-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dbe6d-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dbe6d-139">Minimum supported server</span></span><br/> | <span data-ttu-id="dbe6d-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dbe6d-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dbe6d-141">標頭</span><span class="sxs-lookup"><span data-stu-id="dbe6d-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbe6d-142"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="dbe6d-142"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="dbe6d-143">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="dbe6d-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="dbe6d-144"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="dbe6d-144"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="dbe6d-145">DLL</span><span class="sxs-lookup"><span data-stu-id="dbe6d-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbe6d-146"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbe6d-146"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="dbe6d-147">CLSID</span><span class="sxs-lookup"><span data-stu-id="dbe6d-147">CLSID</span></span><br/>                    | <span data-ttu-id="dbe6d-148">CLSID \_ 內含</span><span class="sxs-lookup"><span data-stu-id="dbe6d-148">CLSID\_SWbemPropertySet</span></span><br/>                                                      |
| <span data-ttu-id="dbe6d-149">IID</span><span class="sxs-lookup"><span data-stu-id="dbe6d-149">IID</span></span><br/>                      | <span data-ttu-id="dbe6d-150">IID \_ ISWbemPropertySet</span><span class="sxs-lookup"><span data-stu-id="dbe6d-150">IID\_ISWbemPropertySet</span></span><br/>                                                       |



## <a name="see-also"></a><span data-ttu-id="dbe6d-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dbe6d-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbe6d-152">腳本 API 物件</span><span class="sxs-lookup"><span data-stu-id="dbe6d-152">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 





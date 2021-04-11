---
description: SWbemQualifierSet 物件是 SWbemQualifier 物件的集合。
ms.assetid: 7ac5469c-357b-499d-a558-30bf760c5311
ms.tgt_platform: multiple
title: 'SWbemQualifierSet 物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet
- ISWbemQualifierSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e74b495313e8061cc6e08e255d1d055bb2f72a92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027478"
---
# <a name="swbemqualifierset-object"></a><span data-ttu-id="4a941-103">SWbemQualifierSet 物件</span><span class="sxs-lookup"><span data-stu-id="4a941-103">SWbemQualifierSet object</span></span>

<span data-ttu-id="4a941-104">**SWbemQualifierSet** 物件是 [**SWbemQualifier**](swbemqualifier.md)物件的集合。</span><span class="sxs-lookup"><span data-stu-id="4a941-104">An **SWbemQualifierSet** object is a collection of [**SWbemQualifier**](swbemqualifier.md) objects.</span></span> <span data-ttu-id="4a941-105">使用 [**Add**](swbemqualifierset-add.md) 方法將專案加入至集合，使用 [**Item**](swbemqualifierset-item.md) 方法從集合中取出，並使用 [**Remove**](swbemqualifierset-remove.md) 方法從集合中移除。</span><span class="sxs-lookup"><span data-stu-id="4a941-105">Items are added to the collection using the [**Add**](swbemqualifierset-add.md) method, retrieved from the collection using the [**Item**](swbemqualifierset-item.md) method, and removed from the collection using the [**Remove**](swbemqualifierset-remove.md) method.</span></span> <span data-ttu-id="4a941-106">VBScript [CreateObject](creating-an-object-using-vbscript.md) 呼叫無法建立這個物件。</span><span class="sxs-lookup"><span data-stu-id="4a941-106">This object cannot be created by the VBScript [CreateObject](creating-an-object-using-vbscript.md) call.</span></span>

<span data-ttu-id="4a941-107">如需詳細資訊，請參閱 [存取集合](accessing-a-collection.md)。</span><span class="sxs-lookup"><span data-stu-id="4a941-107">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

<span data-ttu-id="4a941-108">組成 **SWbemQualifierSet** 集合的 [**SWbemQualifier**](swbemqualifier.md)物件會描述附加至 WMI 類別、實例、方法或方法參數的限定詞。</span><span class="sxs-lookup"><span data-stu-id="4a941-108">The [**SWbemQualifier**](swbemqualifier.md) objects that make up an **SWbemQualifierSet** collection describe the qualifiers attached to a WMI class, instance, method, or method parameter.</span></span>

## <a name="members"></a><span data-ttu-id="4a941-109">成員</span><span class="sxs-lookup"><span data-stu-id="4a941-109">Members</span></span>

<span data-ttu-id="4a941-110">**SWbemQualifierSet** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4a941-110">The **SWbemQualifierSet** object has these types of members:</span></span>

-   [<span data-ttu-id="4a941-111">方法</span><span class="sxs-lookup"><span data-stu-id="4a941-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="4a941-112">屬性</span><span class="sxs-lookup"><span data-stu-id="4a941-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4a941-113">方法</span><span class="sxs-lookup"><span data-stu-id="4a941-113">Methods</span></span>

<span data-ttu-id="4a941-114">**SWbemQualifierSet** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="4a941-114">The **SWbemQualifierSet** object has these methods.</span></span>



| <span data-ttu-id="4a941-115">方法</span><span class="sxs-lookup"><span data-stu-id="4a941-115">Method</span></span>                                     | <span data-ttu-id="4a941-116">描述</span><span class="sxs-lookup"><span data-stu-id="4a941-116">Description</span></span>                                                                                                 |
|:-------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4a941-117">**添加**</span><span class="sxs-lookup"><span data-stu-id="4a941-117">**Add**</span></span>](swbemqualifierset-add.md)       | <span data-ttu-id="4a941-118">將 [**SWbemQualifier**](swbemqualifier.md) 物件加入至 **SWbemQualifierSet** 集合。</span><span class="sxs-lookup"><span data-stu-id="4a941-118">Adds an [**SWbemQualifier**](swbemqualifier.md) object to the **SWbemQualifierSet** collection.</span></span><br/> |
| [<span data-ttu-id="4a941-119">**項目**</span><span class="sxs-lookup"><span data-stu-id="4a941-119">**Item**</span></span>](swbemqualifierset-item.md)     | <span data-ttu-id="4a941-120">從集合傳回名為 [**SWbemQualifier**](swbemqualifier.md) 的物件。</span><span class="sxs-lookup"><span data-stu-id="4a941-120">Returns a named [**SWbemQualifier**](swbemqualifier.md) object from the collection.</span></span><br/>             |
| [<span data-ttu-id="4a941-121">**移除**</span><span class="sxs-lookup"><span data-stu-id="4a941-121">**Remove**</span></span>](swbemqualifierset-remove.md) | <span data-ttu-id="4a941-122">從集合中刪除已命名的辨識符號。</span><span class="sxs-lookup"><span data-stu-id="4a941-122">Deletes a named qualifier from the collection.</span></span><br/>                                                   |



 

### <a name="properties"></a><span data-ttu-id="4a941-123">屬性</span><span class="sxs-lookup"><span data-stu-id="4a941-123">Properties</span></span>

<span data-ttu-id="4a941-124">**SWbemQualifierSet** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4a941-124">The **SWbemQualifierSet** object has these properties.</span></span>



| <span data-ttu-id="4a941-125">屬性</span><span class="sxs-lookup"><span data-stu-id="4a941-125">Property</span></span>                                            | <span data-ttu-id="4a941-126">存取類型</span><span class="sxs-lookup"><span data-stu-id="4a941-126">Access type</span></span>          | <span data-ttu-id="4a941-127">Description</span><span class="sxs-lookup"><span data-stu-id="4a941-127">Description</span></span>                                                                     |
|:----------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="4a941-128">**計數**</span><span class="sxs-lookup"><span data-stu-id="4a941-128">**Count**</span></span>](swbemqualifierset-count.md)<br/> | <span data-ttu-id="4a941-129">唯讀</span><span class="sxs-lookup"><span data-stu-id="4a941-129">Read-only</span></span><br/> | <span data-ttu-id="4a941-130">包含 **SWbemQualifierSet** 集合中的專案數。</span><span class="sxs-lookup"><span data-stu-id="4a941-130">Contains the number of items in an **SWbemQualifierSet** collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4a941-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="4a941-131">Requirements</span></span>



| <span data-ttu-id="4a941-132">需求</span><span class="sxs-lookup"><span data-stu-id="4a941-132">Requirement</span></span> | <span data-ttu-id="4a941-133">值</span><span class="sxs-lookup"><span data-stu-id="4a941-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a941-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4a941-134">Minimum supported client</span></span><br/> | <span data-ttu-id="4a941-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4a941-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4a941-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4a941-136">Minimum supported server</span></span><br/> | <span data-ttu-id="4a941-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4a941-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4a941-138">標頭</span><span class="sxs-lookup"><span data-stu-id="4a941-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a941-139"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="4a941-139"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4a941-140">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="4a941-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="4a941-141"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4a941-141"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4a941-142">DLL</span><span class="sxs-lookup"><span data-stu-id="4a941-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a941-143"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a941-143"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4a941-144">CLSID</span><span class="sxs-lookup"><span data-stu-id="4a941-144">CLSID</span></span><br/>                    | <span data-ttu-id="4a941-145">CLSID \_ SWbemQualifierSet</span><span class="sxs-lookup"><span data-stu-id="4a941-145">CLSID\_SWbemQualifierSet</span></span><br/>                                                     |
| <span data-ttu-id="4a941-146">IID</span><span class="sxs-lookup"><span data-stu-id="4a941-146">IID</span></span><br/>                      | <span data-ttu-id="4a941-147">IID \_ ISWbemQualifierSet</span><span class="sxs-lookup"><span data-stu-id="4a941-147">IID\_ISWbemQualifierSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="4a941-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4a941-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a941-149">腳本 API 物件</span><span class="sxs-lookup"><span data-stu-id="4a941-149">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 





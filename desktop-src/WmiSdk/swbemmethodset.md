---
description: SWbemMethodSet 物件是 SWbemMethod 物件的集合。 使用 Item 方法抓取專案。 如需詳細資訊，請參閱存取集合。 VBScript CreateObject 呼叫無法建立這個物件。
ms.assetid: 0ca2601f-ed40-472e-b4f2-eee750c8c8d1
ms.tgt_platform: multiple
title: 'SWbemMethodSet 物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethodSet
- ISWbemMethodSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d47c4dc8335077d6f8568be4b56200558942ac39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849563"
---
# <a name="swbemmethodset-object"></a><span data-ttu-id="7dedf-106">SWbemMethodSet 物件</span><span class="sxs-lookup"><span data-stu-id="7dedf-106">SWbemMethodSet object</span></span>

<span data-ttu-id="7dedf-107">**SWbemMethodSet** 物件是 [**SWbemMethod**](swbemmethod.md)物件的集合。</span><span class="sxs-lookup"><span data-stu-id="7dedf-107">An **SWbemMethodSet** object is a collection of [**SWbemMethod**](swbemmethod.md) objects.</span></span> <span data-ttu-id="7dedf-108">使用 [**Item**](swbemmethodset-item.md) 方法抓取專案。</span><span class="sxs-lookup"><span data-stu-id="7dedf-108">Items are retrieved using the [**Item**](swbemmethodset-item.md) method.</span></span> <span data-ttu-id="7dedf-109">如需詳細資訊，請參閱 [存取集合](accessing-a-collection.md)。</span><span class="sxs-lookup"><span data-stu-id="7dedf-109">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span> <span data-ttu-id="7dedf-110">VBScript **CreateObject** 呼叫無法建立這個物件。</span><span class="sxs-lookup"><span data-stu-id="7dedf-110">This object cannot be created by the VBScript **CreateObject** call.</span></span>

> [!Note]  
> <span data-ttu-id="7dedf-111">在此版本的 API 中，不支援方法資訊的寫入權限。</span><span class="sxs-lookup"><span data-stu-id="7dedf-111">In this version of the API, write access to method information is not supported.</span></span> <span data-ttu-id="7dedf-112">如果您想要定義方法或修改現有的方法定義，可以在 MOF 檔案中定義方法變更，然後使用 MOF 編譯器來提交變更。</span><span class="sxs-lookup"><span data-stu-id="7dedf-112">If you want to define methods or modify existing method definitions, you can define the method changes in a MOF file and submit the changes using the MOF Compiler.</span></span> <span data-ttu-id="7dedf-113">或者，使用 WMI COM API。</span><span class="sxs-lookup"><span data-stu-id="7dedf-113">Alternatively, use the WMI COM API.</span></span>

 

## <a name="members"></a><span data-ttu-id="7dedf-114">成員</span><span class="sxs-lookup"><span data-stu-id="7dedf-114">Members</span></span>

<span data-ttu-id="7dedf-115">**SWbemMethodSet** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7dedf-115">The **SWbemMethodSet** object has these types of members:</span></span>

-   [<span data-ttu-id="7dedf-116">方法</span><span class="sxs-lookup"><span data-stu-id="7dedf-116">Methods</span></span>](#swbemmethodset-object)
-   [<span data-ttu-id="7dedf-117">屬性</span><span class="sxs-lookup"><span data-stu-id="7dedf-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7dedf-118">方法</span><span class="sxs-lookup"><span data-stu-id="7dedf-118">Methods</span></span>

<span data-ttu-id="7dedf-119">**SWbemMethodSet** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="7dedf-119">The **SWbemMethodSet** object has these methods.</span></span>



| <span data-ttu-id="7dedf-120">方法</span><span class="sxs-lookup"><span data-stu-id="7dedf-120">Method</span></span>                              | <span data-ttu-id="7dedf-121">描述</span><span class="sxs-lookup"><span data-stu-id="7dedf-121">Description</span></span>                                                                                                                                  |
|:------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7dedf-122">**Item**</span><span class="sxs-lookup"><span data-stu-id="7dedf-122">**Item**</span></span>](swbemmethodset-item.md) | <span data-ttu-id="7dedf-123">從集合中捕獲 [**SWbemMethod**](swbemmethod.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="7dedf-123">Retrieves an [**SWbemMethod**](swbemmethod.md) object from the collection.</span></span> <span data-ttu-id="7dedf-124">這是這個物件的預設自動化方法。</span><span class="sxs-lookup"><span data-stu-id="7dedf-124">This is the default automation method of this object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7dedf-125">屬性</span><span class="sxs-lookup"><span data-stu-id="7dedf-125">Properties</span></span>

<span data-ttu-id="7dedf-126">**SWbemMethodSet** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7dedf-126">The **SWbemMethodSet** object has these properties.</span></span>



| <span data-ttu-id="7dedf-127">屬性</span><span class="sxs-lookup"><span data-stu-id="7dedf-127">Property</span></span>                                         | <span data-ttu-id="7dedf-128">存取類型</span><span class="sxs-lookup"><span data-stu-id="7dedf-128">Access type</span></span>          | <span data-ttu-id="7dedf-129">Description</span><span class="sxs-lookup"><span data-stu-id="7dedf-129">Description</span></span>                                       |
|:-------------------------------------------------|:---------------------|:--------------------------------------------------|
| [<span data-ttu-id="7dedf-130">**計數**</span><span class="sxs-lookup"><span data-stu-id="7dedf-130">**Count**</span></span>](swbemmethodset-count.md)<br/> | <span data-ttu-id="7dedf-131">唯讀</span><span class="sxs-lookup"><span data-stu-id="7dedf-131">Read-only</span></span><br/> | <span data-ttu-id="7dedf-132">集合中的項目數目</span><span class="sxs-lookup"><span data-stu-id="7dedf-132">The number of items in the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7dedf-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="7dedf-133">Requirements</span></span>



| <span data-ttu-id="7dedf-134">需求</span><span class="sxs-lookup"><span data-stu-id="7dedf-134">Requirement</span></span> | <span data-ttu-id="7dedf-135">值</span><span class="sxs-lookup"><span data-stu-id="7dedf-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7dedf-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7dedf-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7dedf-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7dedf-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7dedf-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7dedf-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7dedf-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7dedf-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7dedf-140">標頭</span><span class="sxs-lookup"><span data-stu-id="7dedf-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dedf-141"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="7dedf-141"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7dedf-142">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="7dedf-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="7dedf-143"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7dedf-143"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7dedf-144">DLL</span><span class="sxs-lookup"><span data-stu-id="7dedf-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7dedf-145"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7dedf-145"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7dedf-146">CLSID</span><span class="sxs-lookup"><span data-stu-id="7dedf-146">CLSID</span></span><br/>                    | <span data-ttu-id="7dedf-147">CLSID \_ SWbemMethodSet</span><span class="sxs-lookup"><span data-stu-id="7dedf-147">CLSID\_SWbemMethodSet</span></span><br/>                                                        |
| <span data-ttu-id="7dedf-148">IID</span><span class="sxs-lookup"><span data-stu-id="7dedf-148">IID</span></span><br/>                      | <span data-ttu-id="7dedf-149">IID \_ ISWbemMethodSet</span><span class="sxs-lookup"><span data-stu-id="7dedf-149">IID\_ISWbemMethodSet</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="7dedf-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7dedf-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dedf-151">腳本 API 物件</span><span class="sxs-lookup"><span data-stu-id="7dedf-151">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 





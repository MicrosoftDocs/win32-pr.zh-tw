---
description: 針對與集合相關的介面上的每個方法，各包含一個物件。
ms.assetid: e64b007f-e44d-4b6b-97b2-1e017c5a7dbe
title: MethodsForInterface 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MethodsForInterface
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6057d06d4a67222095d5bb0b5ae6da0d603fb4ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386008"
---
# <a name="methodsforinterface-collection"></a><span data-ttu-id="e3c70-103">MethodsForInterface 集合</span><span class="sxs-lookup"><span data-stu-id="e3c70-103">MethodsForInterface collection</span></span>

<span data-ttu-id="e3c70-104">針對與集合相關的介面上的每個方法，各包含一個物件。</span><span class="sxs-lookup"><span data-stu-id="e3c70-104">Contains an object for each method on the interface to which the collection is related.</span></span>

<span data-ttu-id="e3c70-105">此集合不支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。</span><span class="sxs-lookup"><span data-stu-id="e3c70-105">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="e3c70-106">成員</span><span class="sxs-lookup"><span data-stu-id="e3c70-106">Members</span></span>

<span data-ttu-id="e3c70-107">**MethodsForInterface** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。</span><span class="sxs-lookup"><span data-stu-id="e3c70-107">The **MethodsForInterface** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="e3c70-108">相關集合</span><span class="sxs-lookup"><span data-stu-id="e3c70-108">Related Collections</span></span>

<span data-ttu-id="e3c70-109">您可以從這個集合流覽至下列任何集合：</span><span class="sxs-lookup"><span data-stu-id="e3c70-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="e3c70-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="e3c70-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="e3c70-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="e3c70-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="e3c70-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="e3c70-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="e3c70-113">**RolesForMethod**</span><span class="sxs-lookup"><span data-stu-id="e3c70-113">**RolesForMethod**</span></span>](rolesformethod.md)

<span data-ttu-id="e3c70-114">您可以從下列集合流覽至這個集合：</span><span class="sxs-lookup"><span data-stu-id="e3c70-114">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="e3c70-115">**InterfacesForComponent**</span><span class="sxs-lookup"><span data-stu-id="e3c70-115">**InterfacesForComponent**</span></span>](interfacesforcomponent.md)

## <a name="properties"></a><span data-ttu-id="e3c70-116">屬性</span><span class="sxs-lookup"><span data-stu-id="e3c70-116">Properties</span></span>

<span data-ttu-id="e3c70-117">集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="e3c70-117">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="e3c70-118">'</span><span class="sxs-lookup"><span data-stu-id="e3c70-118">AutoComplete</span></span>](#autocomplete)
-   [<span data-ttu-id="e3c70-119">Clsid</span><span class="sxs-lookup"><span data-stu-id="e3c70-119">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="e3c70-120">說明</span><span class="sxs-lookup"><span data-stu-id="e3c70-120">Description</span></span>](#description)
-   [<span data-ttu-id="e3c70-121">IID</span><span class="sxs-lookup"><span data-stu-id="e3c70-121">IID</span></span>](#iid)
-   [<span data-ttu-id="e3c70-122">Index</span><span class="sxs-lookup"><span data-stu-id="e3c70-122">Index</span></span>](#index)
-   [<span data-ttu-id="e3c70-123">名稱</span><span class="sxs-lookup"><span data-stu-id="e3c70-123">Name</span></span>](#name)

### <a name="autocomplete"></a><span data-ttu-id="e3c70-124">自動完成</span><span class="sxs-lookup"><span data-stu-id="e3c70-124">AutoComplete</span></span>



| <span data-ttu-id="e3c70-125">進入</span><span class="sxs-lookup"><span data-stu-id="e3c70-125">Entry</span></span> | <span data-ttu-id="e3c70-126">值</span><span class="sxs-lookup"><span data-stu-id="e3c70-126">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3c70-127">描述</span><span class="sxs-lookup"><span data-stu-id="e3c70-127">Description</span></span>    | <span data-ttu-id="e3c70-128">決定當方法完成時，物件是否會自動停用，而不需要呼叫 SetComplete 或 SetAbort。</span><span class="sxs-lookup"><span data-stu-id="e3c70-128">Determines whether the object is automatically deactivated when the method completes, without SetComplete or SetAbort necessarily being called.</span></span> <span data-ttu-id="e3c70-129">這只會影響在方法開始時 JIT 啟用「完成」位的預設設定。這個位可以重設 (為方法內的 SetComplete 或 SetAbort) ，以覆寫預設值。</span><span class="sxs-lookup"><span data-stu-id="e3c70-129">This affects only the default setting of the JIT Activation "Done" bit at method start; this bit can be reset (as with SetComplete or SetAbort) within the method to override the default.</span></span> |
| <span data-ttu-id="e3c70-130">Access</span><span class="sxs-lookup"><span data-stu-id="e3c70-130">Access</span></span>         | <span data-ttu-id="e3c70-131">讀寫</span><span class="sxs-lookup"><span data-stu-id="e3c70-131">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="e3c70-132">類型</span><span class="sxs-lookup"><span data-stu-id="e3c70-132">Type</span></span>           | <span data-ttu-id="e3c70-133">Bool</span><span class="sxs-lookup"><span data-stu-id="e3c70-133">Bool</span></span>                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="e3c70-134">預設</span><span class="sxs-lookup"><span data-stu-id="e3c70-134">Default</span></span>        | <span data-ttu-id="e3c70-135">否</span><span class="sxs-lookup"><span data-stu-id="e3c70-135">False</span></span>                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="e3c70-136">最小系統</span><span class="sxs-lookup"><span data-stu-id="e3c70-136">Minimum system</span></span> | <span data-ttu-id="e3c70-137">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="e3c70-137">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                               |



 

### <a name="clsid"></a><span data-ttu-id="e3c70-138">CLSID</span><span class="sxs-lookup"><span data-stu-id="e3c70-138">CLSID</span></span>



| <span data-ttu-id="e3c70-139">進入</span><span class="sxs-lookup"><span data-stu-id="e3c70-139">Entry</span></span> | <span data-ttu-id="e3c70-140">值</span><span class="sxs-lookup"><span data-stu-id="e3c70-140">Value</span></span> |
|----------------|---------------------------|
| <span data-ttu-id="e3c70-141">描述</span><span class="sxs-lookup"><span data-stu-id="e3c70-141">Description</span></span>    | <span data-ttu-id="e3c70-142">元件的 GUID。</span><span class="sxs-lookup"><span data-stu-id="e3c70-142">A GUID for the component.</span></span> |
| <span data-ttu-id="e3c70-143">Access</span><span class="sxs-lookup"><span data-stu-id="e3c70-143">Access</span></span>         | <span data-ttu-id="e3c70-144">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="e3c70-144">ReadOnly</span></span>                  |
| <span data-ttu-id="e3c70-145">類型</span><span class="sxs-lookup"><span data-stu-id="e3c70-145">Type</span></span>           | <span data-ttu-id="e3c70-146">String</span><span class="sxs-lookup"><span data-stu-id="e3c70-146">String</span></span>                    |
| <span data-ttu-id="e3c70-147">預設值</span><span class="sxs-lookup"><span data-stu-id="e3c70-147">Default</span></span>        | <span data-ttu-id="e3c70-148">N/A</span><span class="sxs-lookup"><span data-stu-id="e3c70-148">N/A</span></span>                       |
| <span data-ttu-id="e3c70-149">最小系統</span><span class="sxs-lookup"><span data-stu-id="e3c70-149">Minimum system</span></span> | <span data-ttu-id="e3c70-150">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="e3c70-150">Windows 2000</span></span>              |



 

### <a name="description"></a><span data-ttu-id="e3c70-151">Description</span><span class="sxs-lookup"><span data-stu-id="e3c70-151">Description</span></span>



| <span data-ttu-id="e3c70-152">進入</span><span class="sxs-lookup"><span data-stu-id="e3c70-152">Entry</span></span> | <span data-ttu-id="e3c70-153">值</span><span class="sxs-lookup"><span data-stu-id="e3c70-153">Value</span></span> |
|----------------|------------------------------|
| <span data-ttu-id="e3c70-154">描述</span><span class="sxs-lookup"><span data-stu-id="e3c70-154">Description</span></span>    | <span data-ttu-id="e3c70-155">方法的描述。</span><span class="sxs-lookup"><span data-stu-id="e3c70-155">A description of the method.</span></span> |
| <span data-ttu-id="e3c70-156">Access</span><span class="sxs-lookup"><span data-stu-id="e3c70-156">Access</span></span>         | <span data-ttu-id="e3c70-157">讀寫</span><span class="sxs-lookup"><span data-stu-id="e3c70-157">ReadWrite</span></span>                    |
| <span data-ttu-id="e3c70-158">類型</span><span class="sxs-lookup"><span data-stu-id="e3c70-158">Type</span></span>           | <span data-ttu-id="e3c70-159">String</span><span class="sxs-lookup"><span data-stu-id="e3c70-159">String</span></span>                       |
| <span data-ttu-id="e3c70-160">預設值</span><span class="sxs-lookup"><span data-stu-id="e3c70-160">Default</span></span>        | <span data-ttu-id="e3c70-161">""</span><span class="sxs-lookup"><span data-stu-id="e3c70-161">""</span></span>                           |
| <span data-ttu-id="e3c70-162">最小系統</span><span class="sxs-lookup"><span data-stu-id="e3c70-162">Minimum system</span></span> | <span data-ttu-id="e3c70-163">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="e3c70-163">Windows 2000</span></span>                 |



 

### <a name="iid"></a><span data-ttu-id="e3c70-164">IID</span><span class="sxs-lookup"><span data-stu-id="e3c70-164">IID</span></span>



| <span data-ttu-id="e3c70-165">進入</span><span class="sxs-lookup"><span data-stu-id="e3c70-165">Entry</span></span> | <span data-ttu-id="e3c70-166">值</span><span class="sxs-lookup"><span data-stu-id="e3c70-166">Value</span></span> |
|----------------|---------------------------|
| <span data-ttu-id="e3c70-167">描述</span><span class="sxs-lookup"><span data-stu-id="e3c70-167">Description</span></span>    | <span data-ttu-id="e3c70-168">介面的 GUID。</span><span class="sxs-lookup"><span data-stu-id="e3c70-168">A GUID for the interface.</span></span> |
| <span data-ttu-id="e3c70-169">Access</span><span class="sxs-lookup"><span data-stu-id="e3c70-169">Access</span></span>         | <span data-ttu-id="e3c70-170">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="e3c70-170">ReadOnly</span></span>                  |
| <span data-ttu-id="e3c70-171">類型</span><span class="sxs-lookup"><span data-stu-id="e3c70-171">Type</span></span>           | <span data-ttu-id="e3c70-172">String</span><span class="sxs-lookup"><span data-stu-id="e3c70-172">String</span></span>                    |
| <span data-ttu-id="e3c70-173">預設值</span><span class="sxs-lookup"><span data-stu-id="e3c70-173">Default</span></span>        | <span data-ttu-id="e3c70-174">N/A</span><span class="sxs-lookup"><span data-stu-id="e3c70-174">N/A</span></span>                       |
| <span data-ttu-id="e3c70-175">最小系統</span><span class="sxs-lookup"><span data-stu-id="e3c70-175">Minimum system</span></span> | <span data-ttu-id="e3c70-176">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="e3c70-176">Windows 2000</span></span>              |



 

### <a name="index"></a><span data-ttu-id="e3c70-177">索引</span><span class="sxs-lookup"><span data-stu-id="e3c70-177">Index</span></span>



| <span data-ttu-id="e3c70-178">進入</span><span class="sxs-lookup"><span data-stu-id="e3c70-178">Entry</span></span> | <span data-ttu-id="e3c70-179">值</span><span class="sxs-lookup"><span data-stu-id="e3c70-179">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3c70-180">描述</span><span class="sxs-lookup"><span data-stu-id="e3c70-180">Description</span></span>    | <span data-ttu-id="e3c70-181">方法分派識別碼。</span><span class="sxs-lookup"><span data-stu-id="e3c70-181">The method dispatch identifier.</span></span> <span data-ttu-id="e3c70-182">當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="e3c70-182">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="e3c70-183">Access</span><span class="sxs-lookup"><span data-stu-id="e3c70-183">Access</span></span>         | <span data-ttu-id="e3c70-184">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="e3c70-184">ReadOnly</span></span>                                                                                                                                                        |
| <span data-ttu-id="e3c70-185">類型</span><span class="sxs-lookup"><span data-stu-id="e3c70-185">Type</span></span>           | <span data-ttu-id="e3c70-186">**Dword**</span><span class="sxs-lookup"><span data-stu-id="e3c70-186">**DWORD**</span></span>                                                                                                                                                       |
| <span data-ttu-id="e3c70-187">預設</span><span class="sxs-lookup"><span data-stu-id="e3c70-187">Default</span></span>        | <span data-ttu-id="e3c70-188">N/A</span><span class="sxs-lookup"><span data-stu-id="e3c70-188">N/A</span></span>                                                                                                                                                             |
| <span data-ttu-id="e3c70-189">最小系統</span><span class="sxs-lookup"><span data-stu-id="e3c70-189">Minimum system</span></span> | <span data-ttu-id="e3c70-190">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="e3c70-190">Windows 2000</span></span>                                                                                                                                                    |



 

### <a name="name"></a><span data-ttu-id="e3c70-191">Name</span><span class="sxs-lookup"><span data-stu-id="e3c70-191">Name</span></span>



| <span data-ttu-id="e3c70-192">進入</span><span class="sxs-lookup"><span data-stu-id="e3c70-192">Entry</span></span> | <span data-ttu-id="e3c70-193">值</span><span class="sxs-lookup"><span data-stu-id="e3c70-193">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3c70-194">描述</span><span class="sxs-lookup"><span data-stu-id="e3c70-194">Description</span></span>    | <span data-ttu-id="e3c70-195">方法名稱。</span><span class="sxs-lookup"><span data-stu-id="e3c70-195">The method name.</span></span> <span data-ttu-id="e3c70-196">在這個集合的物件上呼叫 [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="e3c70-196">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="e3c70-197">Access</span><span class="sxs-lookup"><span data-stu-id="e3c70-197">Access</span></span>         | <span data-ttu-id="e3c70-198">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="e3c70-198">ReadOnly</span></span>                                                                                                                                           |
| <span data-ttu-id="e3c70-199">類型</span><span class="sxs-lookup"><span data-stu-id="e3c70-199">Type</span></span>           | <span data-ttu-id="e3c70-200">String</span><span class="sxs-lookup"><span data-stu-id="e3c70-200">String</span></span>                                                                                                                                             |
| <span data-ttu-id="e3c70-201">預設值</span><span class="sxs-lookup"><span data-stu-id="e3c70-201">Default</span></span>        | <span data-ttu-id="e3c70-202">N/A</span><span class="sxs-lookup"><span data-stu-id="e3c70-202">N/A</span></span>                                                                                                                                                |
| <span data-ttu-id="e3c70-203">最小系統</span><span class="sxs-lookup"><span data-stu-id="e3c70-203">Minimum system</span></span> | <span data-ttu-id="e3c70-204">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="e3c70-204">Windows 2000</span></span>                                                                                                                                       |



 

## <a name="see-also"></a><span data-ttu-id="e3c70-205">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3c70-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3c70-206">COM + 系統管理集合</span><span class="sxs-lookup"><span data-stu-id="e3c70-206">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 

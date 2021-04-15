---
description: 抓取有關執行中應用程式的資訊。
ms.assetid: 148e42aa-e99e-4fa2-8b74-a7ebf82b99d0
title: ApplicationInstances 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplicationInstances
api_type:
- COM
api_location: ''
ms.openlocfilehash: 56680a81cc564466dc3586bf0381cf4db97f914b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468168"
---
# <a name="applicationinstances-collection"></a><span data-ttu-id="91565-103">ApplicationInstances 集合</span><span class="sxs-lookup"><span data-stu-id="91565-103">ApplicationInstances collection</span></span>

<span data-ttu-id="91565-104">抓取有關執行中應用程式的資訊。</span><span class="sxs-lookup"><span data-stu-id="91565-104">Retrieves information regarding running applications.</span></span>

<span data-ttu-id="91565-105">此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**加入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**移除**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。</span><span class="sxs-lookup"><span data-stu-id="91565-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="91565-106">成員</span><span class="sxs-lookup"><span data-stu-id="91565-106">Members</span></span>

<span data-ttu-id="91565-107">**ApplicationInstances** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。</span><span class="sxs-lookup"><span data-stu-id="91565-107">The **ApplicationInstances** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="91565-108">相關集合</span><span class="sxs-lookup"><span data-stu-id="91565-108">Related Collections</span></span>

<span data-ttu-id="91565-109">您可以從這個集合流覽至下列任何集合：</span><span class="sxs-lookup"><span data-stu-id="91565-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="91565-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="91565-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="91565-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="91565-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="91565-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="91565-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="91565-113">您可以從下列集合流覽至這個集合：</span><span class="sxs-lookup"><span data-stu-id="91565-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="91565-114">**應用程式**</span><span class="sxs-lookup"><span data-stu-id="91565-114">**Applications**</span></span>](applications.md)
-   [<span data-ttu-id="91565-115">**根**</span><span class="sxs-lookup"><span data-stu-id="91565-115">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="91565-116">屬性</span><span class="sxs-lookup"><span data-stu-id="91565-116">Properties</span></span>

<span data-ttu-id="91565-117">集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="91565-117">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="91565-118">應用程式</span><span class="sxs-lookup"><span data-stu-id="91565-118">Application</span></span>](#applicationinstances-collection)
-   [<span data-ttu-id="91565-119">HasRecycled</span><span class="sxs-lookup"><span data-stu-id="91565-119">HasRecycled</span></span>](#hasrecycled)
-   [<span data-ttu-id="91565-120">InstanceID</span><span class="sxs-lookup"><span data-stu-id="91565-120">InstanceID</span></span>](#instanceid)
-   [<span data-ttu-id="91565-121">IsPaused</span><span class="sxs-lookup"><span data-stu-id="91565-121">IsPaused</span></span>](#ispaused)
-   [<span data-ttu-id="91565-122">PartitionID</span><span class="sxs-lookup"><span data-stu-id="91565-122">PartitionID</span></span>](#partitionid)
-   [<span data-ttu-id="91565-123">ProcessID</span><span class="sxs-lookup"><span data-stu-id="91565-123">ProcessID</span></span>](#processid)

### <a name="application"></a><span data-ttu-id="91565-124">應用程式</span><span class="sxs-lookup"><span data-stu-id="91565-124">Application</span></span>



| <span data-ttu-id="91565-125">進入</span><span class="sxs-lookup"><span data-stu-id="91565-125">Entry</span></span> | <span data-ttu-id="91565-126">值</span><span class="sxs-lookup"><span data-stu-id="91565-126">Value</span></span> |
|----------------|-------------------------------------|
| <span data-ttu-id="91565-127">描述</span><span class="sxs-lookup"><span data-stu-id="91565-127">Description</span></span>    | <span data-ttu-id="91565-128">正在執行之應用程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="91565-128">The ID for the running application.</span></span> |
| <span data-ttu-id="91565-129">Access</span><span class="sxs-lookup"><span data-stu-id="91565-129">Access</span></span>         | <span data-ttu-id="91565-130">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="91565-130">ReadOnly</span></span>                            |
| <span data-ttu-id="91565-131">類型</span><span class="sxs-lookup"><span data-stu-id="91565-131">Type</span></span>           | <span data-ttu-id="91565-132">String</span><span class="sxs-lookup"><span data-stu-id="91565-132">String</span></span>                              |
| <span data-ttu-id="91565-133">預設值</span><span class="sxs-lookup"><span data-stu-id="91565-133">Default</span></span>        | <span data-ttu-id="91565-134">N/A</span><span class="sxs-lookup"><span data-stu-id="91565-134">N/A</span></span>                                 |
| <span data-ttu-id="91565-135">最小系統</span><span class="sxs-lookup"><span data-stu-id="91565-135">Minimum system</span></span> | <span data-ttu-id="91565-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="91565-136">Windows XP</span></span>                          |



 

### <a name="hasrecycled"></a><span data-ttu-id="91565-137">HasRecycled</span><span class="sxs-lookup"><span data-stu-id="91565-137">HasRecycled</span></span>



| <span data-ttu-id="91565-138">進入</span><span class="sxs-lookup"><span data-stu-id="91565-138">Entry</span></span> | <span data-ttu-id="91565-139">值</span><span class="sxs-lookup"><span data-stu-id="91565-139">Value</span></span> |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="91565-140">描述</span><span class="sxs-lookup"><span data-stu-id="91565-140">Description</span></span>    | <span data-ttu-id="91565-141">指出是否已回收應用程式實例。</span><span class="sxs-lookup"><span data-stu-id="91565-141">Indicates whether the application instance has been recycled.</span></span> |
| <span data-ttu-id="91565-142">Access</span><span class="sxs-lookup"><span data-stu-id="91565-142">Access</span></span>         | <span data-ttu-id="91565-143">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="91565-143">ReadOnly</span></span>                                                      |
| <span data-ttu-id="91565-144">類型</span><span class="sxs-lookup"><span data-stu-id="91565-144">Type</span></span>           | <span data-ttu-id="91565-145">Bool</span><span class="sxs-lookup"><span data-stu-id="91565-145">Bool</span></span>                                                          |
| <span data-ttu-id="91565-146">預設</span><span class="sxs-lookup"><span data-stu-id="91565-146">Default</span></span>        | <span data-ttu-id="91565-147">否</span><span class="sxs-lookup"><span data-stu-id="91565-147">False</span></span>                                                         |
| <span data-ttu-id="91565-148">最小系統</span><span class="sxs-lookup"><span data-stu-id="91565-148">Minimum system</span></span> | <span data-ttu-id="91565-149">Windows XP</span><span class="sxs-lookup"><span data-stu-id="91565-149">Windows XP</span></span>                                                    |



 

### <a name="instanceid"></a><span data-ttu-id="91565-150">InstanceID</span><span class="sxs-lookup"><span data-stu-id="91565-150">InstanceID</span></span>



| <span data-ttu-id="91565-151">進入</span><span class="sxs-lookup"><span data-stu-id="91565-151">Entry</span></span> | <span data-ttu-id="91565-152">值</span><span class="sxs-lookup"><span data-stu-id="91565-152">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91565-153">描述</span><span class="sxs-lookup"><span data-stu-id="91565-153">Description</span></span>    | <span data-ttu-id="91565-154">應用程式實例的全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="91565-154">The globally unique identifier for the application instance.</span></span> <span data-ttu-id="91565-155">當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 或 [**名稱**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="91565-155">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="91565-156">Access</span><span class="sxs-lookup"><span data-stu-id="91565-156">Access</span></span>         | <span data-ttu-id="91565-157">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="91565-157">ReadOnly</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="91565-158">類型</span><span class="sxs-lookup"><span data-stu-id="91565-158">Type</span></span>           | <span data-ttu-id="91565-159">String</span><span class="sxs-lookup"><span data-stu-id="91565-159">String</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="91565-160">預設值</span><span class="sxs-lookup"><span data-stu-id="91565-160">Default</span></span>        | <span data-ttu-id="91565-161">N/A</span><span class="sxs-lookup"><span data-stu-id="91565-161">N/A</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="91565-162">最小系統</span><span class="sxs-lookup"><span data-stu-id="91565-162">Minimum system</span></span> | <span data-ttu-id="91565-163">Windows XP</span><span class="sxs-lookup"><span data-stu-id="91565-163">Windows XP</span></span>                                                                                                                                                                                                                          |



 

### <a name="ispaused"></a><span data-ttu-id="91565-164">IsPaused</span><span class="sxs-lookup"><span data-stu-id="91565-164">IsPaused</span></span>



| <span data-ttu-id="91565-165">進入</span><span class="sxs-lookup"><span data-stu-id="91565-165">Entry</span></span> | <span data-ttu-id="91565-166">值</span><span class="sxs-lookup"><span data-stu-id="91565-166">Value</span></span> |
|----------------|-----------------------------------------------------------------|
| <span data-ttu-id="91565-167">描述</span><span class="sxs-lookup"><span data-stu-id="91565-167">Description</span></span>    | <span data-ttu-id="91565-168">指出應用程式實例是否目前已暫停。</span><span class="sxs-lookup"><span data-stu-id="91565-168">Indicates whether the application instance is currently paused.</span></span> |
| <span data-ttu-id="91565-169">Access</span><span class="sxs-lookup"><span data-stu-id="91565-169">Access</span></span>         | <span data-ttu-id="91565-170">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="91565-170">ReadOnly</span></span>                                                        |
| <span data-ttu-id="91565-171">類型</span><span class="sxs-lookup"><span data-stu-id="91565-171">Type</span></span>           | <span data-ttu-id="91565-172">Bool</span><span class="sxs-lookup"><span data-stu-id="91565-172">Bool</span></span>                                                            |
| <span data-ttu-id="91565-173">預設</span><span class="sxs-lookup"><span data-stu-id="91565-173">Default</span></span>        | <span data-ttu-id="91565-174">否</span><span class="sxs-lookup"><span data-stu-id="91565-174">False</span></span>                                                           |
| <span data-ttu-id="91565-175">最小系統</span><span class="sxs-lookup"><span data-stu-id="91565-175">Minimum system</span></span> | <span data-ttu-id="91565-176">Windows XP</span><span class="sxs-lookup"><span data-stu-id="91565-176">Windows XP</span></span>                                                      |



 

### <a name="partitionid"></a><span data-ttu-id="91565-177">PartitionID</span><span class="sxs-lookup"><span data-stu-id="91565-177">PartitionID</span></span>



| <span data-ttu-id="91565-178">進入</span><span class="sxs-lookup"><span data-stu-id="91565-178">Entry</span></span> | <span data-ttu-id="91565-179">值</span><span class="sxs-lookup"><span data-stu-id="91565-179">Value</span></span> |
|----------------|-------------------------------------------------|
| <span data-ttu-id="91565-180">描述</span><span class="sxs-lookup"><span data-stu-id="91565-180">Description</span></span>    | <span data-ttu-id="91565-181">應用程式所使用的資料分割識別碼。</span><span class="sxs-lookup"><span data-stu-id="91565-181">The partition ID that the application is using.</span></span> |
| <span data-ttu-id="91565-182">Access</span><span class="sxs-lookup"><span data-stu-id="91565-182">Access</span></span>         | <span data-ttu-id="91565-183">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="91565-183">ReadOnly</span></span>                                        |
| <span data-ttu-id="91565-184">類型</span><span class="sxs-lookup"><span data-stu-id="91565-184">Type</span></span>           | <span data-ttu-id="91565-185">String</span><span class="sxs-lookup"><span data-stu-id="91565-185">String</span></span>                                          |
| <span data-ttu-id="91565-186">預設值</span><span class="sxs-lookup"><span data-stu-id="91565-186">Default</span></span>        | <span data-ttu-id="91565-187">N/A</span><span class="sxs-lookup"><span data-stu-id="91565-187">N/A</span></span>                                             |
| <span data-ttu-id="91565-188">最小系統</span><span class="sxs-lookup"><span data-stu-id="91565-188">Minimum system</span></span> | <span data-ttu-id="91565-189">Windows XP</span><span class="sxs-lookup"><span data-stu-id="91565-189">Windows XP</span></span>                                      |



 

### <a name="processid"></a><span data-ttu-id="91565-190">ProcessID</span><span class="sxs-lookup"><span data-stu-id="91565-190">ProcessID</span></span>



| <span data-ttu-id="91565-191">進入</span><span class="sxs-lookup"><span data-stu-id="91565-191">Entry</span></span> | <span data-ttu-id="91565-192">值</span><span class="sxs-lookup"><span data-stu-id="91565-192">Value</span></span> |
|----------------|---------------------------------------------|
| <span data-ttu-id="91565-193">描述</span><span class="sxs-lookup"><span data-stu-id="91565-193">Description</span></span>    | <span data-ttu-id="91565-194">應用程式例項的處理程序識別碼。</span><span class="sxs-lookup"><span data-stu-id="91565-194">The process ID of the application instance.</span></span> |
| <span data-ttu-id="91565-195">Access</span><span class="sxs-lookup"><span data-stu-id="91565-195">Access</span></span>         | <span data-ttu-id="91565-196">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="91565-196">ReadOnly</span></span>                                    |
| <span data-ttu-id="91565-197">類型</span><span class="sxs-lookup"><span data-stu-id="91565-197">Type</span></span>           | <span data-ttu-id="91565-198">String</span><span class="sxs-lookup"><span data-stu-id="91565-198">String</span></span>                                      |
| <span data-ttu-id="91565-199">預設值</span><span class="sxs-lookup"><span data-stu-id="91565-199">Default</span></span>        | <span data-ttu-id="91565-200">N/A</span><span class="sxs-lookup"><span data-stu-id="91565-200">N/A</span></span>                                         |
| <span data-ttu-id="91565-201">最小系統</span><span class="sxs-lookup"><span data-stu-id="91565-201">Minimum system</span></span> | <span data-ttu-id="91565-202">Windows XP</span><span class="sxs-lookup"><span data-stu-id="91565-202">Windows XP</span></span>                                  |



 

## <a name="see-also"></a><span data-ttu-id="91565-203">另請參閱</span><span class="sxs-lookup"><span data-stu-id="91565-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91565-204">COM + 系統管理集合</span><span class="sxs-lookup"><span data-stu-id="91565-204">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 

---
description: 包含每個暫時性訂用帳戶的物件。 您可以針對執行中的物件實例執行暫時的訂閱，並在物件終結時消失。
ms.assetid: beee291c-e03f-4ee0-b1f2-99dcf113c46e
title: TransientSubscriptions 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransientSubscriptions
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6421cff326f4c33f0c77ae47d00e17c79c971443
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847374"
---
# <a name="transientsubscriptions-collection"></a><span data-ttu-id="29c22-104">TransientSubscriptions 集合</span><span class="sxs-lookup"><span data-stu-id="29c22-104">TransientSubscriptions collection</span></span>

<span data-ttu-id="29c22-105">包含每個暫時性訂用帳戶的物件。</span><span class="sxs-lookup"><span data-stu-id="29c22-105">Contains an object for each transient subscription.</span></span> <span data-ttu-id="29c22-106">您可以針對執行中的物件實例執行暫時的訂閱，並在物件終結時消失。</span><span class="sxs-lookup"><span data-stu-id="29c22-106">Transient subscriptions can be created on the fly for running object instances, and they vanish when the object is destroyed.</span></span>

<span data-ttu-id="29c22-107">此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**加入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**移除**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。</span><span class="sxs-lookup"><span data-stu-id="29c22-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="29c22-108">成員</span><span class="sxs-lookup"><span data-stu-id="29c22-108">Members</span></span>

<span data-ttu-id="29c22-109">**TransientSubscriptions** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。</span><span class="sxs-lookup"><span data-stu-id="29c22-109">The **TransientSubscriptions** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="29c22-110">相關集合</span><span class="sxs-lookup"><span data-stu-id="29c22-110">Related Collections</span></span>

<span data-ttu-id="29c22-111">您可以從這個集合流覽至下列任何集合：</span><span class="sxs-lookup"><span data-stu-id="29c22-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="29c22-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="29c22-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="29c22-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="29c22-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="29c22-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="29c22-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="29c22-115">**TransientPublisherProperties**</span><span class="sxs-lookup"><span data-stu-id="29c22-115">**TransientPublisherProperties**</span></span>](transientpublisherproperties.md)
-   [<span data-ttu-id="29c22-116">**TransientSubscriberProperties**</span><span class="sxs-lookup"><span data-stu-id="29c22-116">**TransientSubscriberProperties**</span></span>](transientsubscriberproperties.md)

<span data-ttu-id="29c22-117">您可以從下列集合流覽至這個集合：</span><span class="sxs-lookup"><span data-stu-id="29c22-117">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="29c22-118">**根**</span><span class="sxs-lookup"><span data-stu-id="29c22-118">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="29c22-119">屬性</span><span class="sxs-lookup"><span data-stu-id="29c22-119">Properties</span></span>

<span data-ttu-id="29c22-120">集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="29c22-120">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="29c22-121">說明</span><span class="sxs-lookup"><span data-stu-id="29c22-121">Description</span></span>](#description)
-   [<span data-ttu-id="29c22-122">Enabled</span><span class="sxs-lookup"><span data-stu-id="29c22-122">Enabled</span></span>](#enabled)
-   [<span data-ttu-id="29c22-123">EventClassPartitionID</span><span class="sxs-lookup"><span data-stu-id="29c22-123">EventClassPartitionID</span></span>](#eventclasspartitionid)
-   [<span data-ttu-id="29c22-124">EventCLSID</span><span class="sxs-lookup"><span data-stu-id="29c22-124">EventCLSID</span></span>](#eventclsid)
-   [<span data-ttu-id="29c22-125">>filtercriteria</span><span class="sxs-lookup"><span data-stu-id="29c22-125">FilterCriteria</span></span>](#filtercriteria)
-   [<span data-ttu-id="29c22-126">識別碼</span><span class="sxs-lookup"><span data-stu-id="29c22-126">ID</span></span>](#transientsubscriptions-collection)
-   [<span data-ttu-id="29c22-127">InterfaceID</span><span class="sxs-lookup"><span data-stu-id="29c22-127">InterfaceID</span></span>](#interfaceid)
-   [<span data-ttu-id="29c22-128">MethodName</span><span class="sxs-lookup"><span data-stu-id="29c22-128">MethodName</span></span>](#methodname)
-   [<span data-ttu-id="29c22-129">名稱</span><span class="sxs-lookup"><span data-stu-id="29c22-129">Name</span></span>](#methodname)
-   [<span data-ttu-id="29c22-130">PerUser</span><span class="sxs-lookup"><span data-stu-id="29c22-130">PerUser</span></span>](#peruser)
-   [<span data-ttu-id="29c22-131">PublisherID</span><span class="sxs-lookup"><span data-stu-id="29c22-131">PublisherID</span></span>](#publisherid)
-   [<span data-ttu-id="29c22-132">SubscriberInterface</span><span class="sxs-lookup"><span data-stu-id="29c22-132">SubscriberInterface</span></span>](#subscriberinterface)
-   [<span data-ttu-id="29c22-133">SubscriberPartitionID</span><span class="sxs-lookup"><span data-stu-id="29c22-133">SubscriberPartitionID</span></span>](#subscriberpartitionid)
-   [<span data-ttu-id="29c22-134">使用者名稱</span><span class="sxs-lookup"><span data-stu-id="29c22-134">UserName</span></span>](#username)

### <a name="description"></a><span data-ttu-id="29c22-135">Description</span><span class="sxs-lookup"><span data-stu-id="29c22-135">Description</span></span>



| <span data-ttu-id="29c22-136">進入</span><span class="sxs-lookup"><span data-stu-id="29c22-136">Entry</span></span> | <span data-ttu-id="29c22-137">值</span><span class="sxs-lookup"><span data-stu-id="29c22-137">Value</span></span> |
|----------------|-------------------------------------|
| <span data-ttu-id="29c22-138">描述</span><span class="sxs-lookup"><span data-stu-id="29c22-138">Description</span></span>    | <span data-ttu-id="29c22-139">訂用帳戶的描述。</span><span class="sxs-lookup"><span data-stu-id="29c22-139">A description for the subscription.</span></span> |
| <span data-ttu-id="29c22-140">Access</span><span class="sxs-lookup"><span data-stu-id="29c22-140">Access</span></span>         | <span data-ttu-id="29c22-141">讀寫</span><span class="sxs-lookup"><span data-stu-id="29c22-141">ReadWrite</span></span>                           |
| <span data-ttu-id="29c22-142">類型</span><span class="sxs-lookup"><span data-stu-id="29c22-142">Type</span></span>           | <span data-ttu-id="29c22-143">String</span><span class="sxs-lookup"><span data-stu-id="29c22-143">String</span></span>                              |
| <span data-ttu-id="29c22-144">預設值</span><span class="sxs-lookup"><span data-stu-id="29c22-144">Default</span></span>        | <span data-ttu-id="29c22-145">""</span><span class="sxs-lookup"><span data-stu-id="29c22-145">""</span></span>                                  |
| <span data-ttu-id="29c22-146">最小系統</span><span class="sxs-lookup"><span data-stu-id="29c22-146">Minimum system</span></span> | <span data-ttu-id="29c22-147">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="29c22-147">Windows 2000</span></span>                        |



 

### <a name="enabled"></a><span data-ttu-id="29c22-148">已啟用</span><span class="sxs-lookup"><span data-stu-id="29c22-148">Enabled</span></span>



| <span data-ttu-id="29c22-149">進入</span><span class="sxs-lookup"><span data-stu-id="29c22-149">Entry</span></span> | <span data-ttu-id="29c22-150">值</span><span class="sxs-lookup"><span data-stu-id="29c22-150">Value</span></span> |
|----------------|----------------------------------------------------------|
| <span data-ttu-id="29c22-151">描述</span><span class="sxs-lookup"><span data-stu-id="29c22-151">Description</span></span>    | <span data-ttu-id="29c22-152">指出目前是否已啟用訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="29c22-152">Indicates whether the subscription is presently enabled.</span></span> |
| <span data-ttu-id="29c22-153">Access</span><span class="sxs-lookup"><span data-stu-id="29c22-153">Access</span></span>         | <span data-ttu-id="29c22-154">讀寫</span><span class="sxs-lookup"><span data-stu-id="29c22-154">ReadWrite</span></span>                                                |
| <span data-ttu-id="29c22-155">類型</span><span class="sxs-lookup"><span data-stu-id="29c22-155">Type</span></span>           | <span data-ttu-id="29c22-156">Bool</span><span class="sxs-lookup"><span data-stu-id="29c22-156">Bool</span></span>                                                     |
| <span data-ttu-id="29c22-157">預設</span><span class="sxs-lookup"><span data-stu-id="29c22-157">Default</span></span>        | <span data-ttu-id="29c22-158">對</span><span class="sxs-lookup"><span data-stu-id="29c22-158">True</span></span>                                                     |
| <span data-ttu-id="29c22-159">最小系統</span><span class="sxs-lookup"><span data-stu-id="29c22-159">Minimum system</span></span> | <span data-ttu-id="29c22-160">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="29c22-160">Windows 2000</span></span>                                             |



 

### <a name="eventclasspartitionid"></a><span data-ttu-id="29c22-161">EventClassPartitionID</span><span class="sxs-lookup"><span data-stu-id="29c22-161">EventClassPartitionID</span></span>



| <span data-ttu-id="29c22-162">進入</span><span class="sxs-lookup"><span data-stu-id="29c22-162">Entry</span></span> | <span data-ttu-id="29c22-163">值</span><span class="sxs-lookup"><span data-stu-id="29c22-163">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29c22-164">描述</span><span class="sxs-lookup"><span data-stu-id="29c22-164">Description</span></span>    | <span data-ttu-id="29c22-165">訂閱事件類別時，用來代表包含事件類別之資料分割識別碼的 GUID。</span><span class="sxs-lookup"><span data-stu-id="29c22-165">When subscribing to an event class, used to represent the GUID of the partition ID containing the event class.</span></span> <span data-ttu-id="29c22-166">訂閱事件類別時，訂閱者可以選擇訂閱相同或不同資料分割中的事件類別。</span><span class="sxs-lookup"><span data-stu-id="29c22-166">When subscribing to event classes, the subscriber has the option to subscribe to an event class in the same or different partition.</span></span> |
| <span data-ttu-id="29c22-167">Access</span><span class="sxs-lookup"><span data-stu-id="29c22-167">Access</span></span>         | <span data-ttu-id="29c22-168">讀寫</span><span class="sxs-lookup"><span data-stu-id="29c22-168">ReadWrite</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="29c22-169">類型</span><span class="sxs-lookup"><span data-stu-id="29c22-169">Type</span></span>           | <span data-ttu-id="29c22-170">String</span><span class="sxs-lookup"><span data-stu-id="29c22-170">String</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="29c22-171">預設值</span><span class="sxs-lookup"><span data-stu-id="29c22-171">Default</span></span>        | <span data-ttu-id="29c22-172">NULL</span><span class="sxs-lookup"><span data-stu-id="29c22-172">NULL</span></span>                                                                                                                                                                                                                                               |
| <span data-ttu-id="29c22-173">最小系統</span><span class="sxs-lookup"><span data-stu-id="29c22-173">Minimum system</span></span> | <span data-ttu-id="29c22-174">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="29c22-174">Windows Server 2003</span></span>                                                                                                                                                                                                                                |



 

### <a name="eventclsid"></a><span data-ttu-id="29c22-175">EventCLSID</span><span class="sxs-lookup"><span data-stu-id="29c22-175">EventCLSID</span></span>



| <span data-ttu-id="29c22-176">進入</span><span class="sxs-lookup"><span data-stu-id="29c22-176">Entry</span></span> | <span data-ttu-id="29c22-177">值</span><span class="sxs-lookup"><span data-stu-id="29c22-177">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="29c22-178">描述</span><span class="sxs-lookup"><span data-stu-id="29c22-178">Description</span></span>    | <span data-ttu-id="29c22-179">事件類別的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="29c22-179">The CLSID for the event class.</span></span> <span data-ttu-id="29c22-180">您可以指定 EventCLSID 或 PublisherID，但不能同時指定兩者。</span><span class="sxs-lookup"><span data-stu-id="29c22-180">You can indicate an EventCLSID or a PublisherID but not both.</span></span> |
| <span data-ttu-id="29c22-181">Access</span><span class="sxs-lookup"><span data-stu-id="29c22-181">Access</span></span>         | <span data-ttu-id="29c22-182">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="29c22-182">WriteOnce</span></span>                                                                                    |
| <span data-ttu-id="29c22-183">類型</span><span class="sxs-lookup"><span data-stu-id="29c22-183">Type</span></span>           | <span data-ttu-id="29c22-184">String</span><span class="sxs-lookup"><span data-stu-id="29c22-184">String</span></span>                                                                                       |
| <span data-ttu-id="29c22-185">預設值</span><span class="sxs-lookup"><span data-stu-id="29c22-185">Default</span></span>        | <span data-ttu-id="29c22-186">N/A</span><span class="sxs-lookup"><span data-stu-id="29c22-186">N/A</span></span>                                                                                          |
| <span data-ttu-id="29c22-187">最小系統</span><span class="sxs-lookup"><span data-stu-id="29c22-187">Minimum system</span></span> | <span data-ttu-id="29c22-188">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="29c22-188">Windows 2000</span></span>                                                                                 |



 

### <a name="filtercriteria"></a><span data-ttu-id="29c22-189">>filtercriteria</span><span class="sxs-lookup"><span data-stu-id="29c22-189">FilterCriteria</span></span>



| <span data-ttu-id="29c22-190">進入</span><span class="sxs-lookup"><span data-stu-id="29c22-190">Entry</span></span> | <span data-ttu-id="29c22-191">值</span><span class="sxs-lookup"><span data-stu-id="29c22-191">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29c22-192">描述</span><span class="sxs-lookup"><span data-stu-id="29c22-192">Description</span></span>    | <span data-ttu-id="29c22-193">指出篩選準則的字串。</span><span class="sxs-lookup"><span data-stu-id="29c22-193">A string that indicates the filter criteria.</span></span> <span data-ttu-id="29c22-194">可以是 [**PublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) 類別的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="29c22-194">Can be a CLSID for a [**PublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) class.</span></span> |
| <span data-ttu-id="29c22-195">Access</span><span class="sxs-lookup"><span data-stu-id="29c22-195">Access</span></span>         | <span data-ttu-id="29c22-196">讀寫</span><span class="sxs-lookup"><span data-stu-id="29c22-196">ReadWrite</span></span>                                                                                                            |
| <span data-ttu-id="29c22-197">類型</span><span class="sxs-lookup"><span data-stu-id="29c22-197">Type</span></span>           | <span data-ttu-id="29c22-198">String</span><span class="sxs-lookup"><span data-stu-id="29c22-198">String</span></span>                                                                                                               |
| <span data-ttu-id="29c22-199">預設值</span><span class="sxs-lookup"><span data-stu-id="29c22-199">Default</span></span>        | <span data-ttu-id="29c22-200">N/A</span><span class="sxs-lookup"><span data-stu-id="29c22-200">N/A</span></span>                                                                                                                  |
| <span data-ttu-id="29c22-201">最小系統</span><span class="sxs-lookup"><span data-stu-id="29c22-201">Minimum system</span></span> | <span data-ttu-id="29c22-202">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="29c22-202">Windows 2000</span></span>                                                                                                         |



 

### <a name="id"></a><span data-ttu-id="29c22-203">識別碼</span><span class="sxs-lookup"><span data-stu-id="29c22-203">ID</span></span>



| <span data-ttu-id="29c22-204">進入</span><span class="sxs-lookup"><span data-stu-id="29c22-204">Entry</span></span> | <span data-ttu-id="29c22-205">值</span><span class="sxs-lookup"><span data-stu-id="29c22-205">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29c22-206">描述</span><span class="sxs-lookup"><span data-stu-id="29c22-206">Description</span></span>    | <span data-ttu-id="29c22-207">訂用帳戶的識別碼。</span><span class="sxs-lookup"><span data-stu-id="29c22-207">Identifier for the subscription.</span></span> <span data-ttu-id="29c22-208">當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="29c22-208">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="29c22-209">Access</span><span class="sxs-lookup"><span data-stu-id="29c22-209">Access</span></span>         | <span data-ttu-id="29c22-210">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="29c22-210">WriteOnce</span></span>                                                                                                                                                        |
| <span data-ttu-id="29c22-211">類型</span><span class="sxs-lookup"><span data-stu-id="29c22-211">Type</span></span>           | <span data-ttu-id="29c22-212">String</span><span class="sxs-lookup"><span data-stu-id="29c22-212">String</span></span>                                                                                                                                                           |
| <span data-ttu-id="29c22-213">預設值</span><span class="sxs-lookup"><span data-stu-id="29c22-213">Default</span></span>        | <Generated>                                                                                                                                                |
| <span data-ttu-id="29c22-214">最小系統</span><span class="sxs-lookup"><span data-stu-id="29c22-214">Minimum system</span></span> | <span data-ttu-id="29c22-215">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="29c22-215">Windows 2000</span></span>                                                                                                                                                     |



 

### <a name="interfaceid"></a><span data-ttu-id="29c22-216">InterfaceID</span><span class="sxs-lookup"><span data-stu-id="29c22-216">InterfaceID</span></span>



| <span data-ttu-id="29c22-217">進入</span><span class="sxs-lookup"><span data-stu-id="29c22-217">Entry</span></span> | <span data-ttu-id="29c22-218">值</span><span class="sxs-lookup"><span data-stu-id="29c22-218">Value</span></span> |
|----------------|----------------------------------|
| <span data-ttu-id="29c22-219">描述</span><span class="sxs-lookup"><span data-stu-id="29c22-219">Description</span></span>    | <span data-ttu-id="29c22-220">已訂閱之介面的 IID。</span><span class="sxs-lookup"><span data-stu-id="29c22-220">IID for interface subscribed to.</span></span> |
| <span data-ttu-id="29c22-221">Access</span><span class="sxs-lookup"><span data-stu-id="29c22-221">Access</span></span>         | <span data-ttu-id="29c22-222">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="29c22-222">WriteOnce</span></span>                        |
| <span data-ttu-id="29c22-223">類型</span><span class="sxs-lookup"><span data-stu-id="29c22-223">Type</span></span>           | <span data-ttu-id="29c22-224">String</span><span class="sxs-lookup"><span data-stu-id="29c22-224">String</span></span>                           |
| <span data-ttu-id="29c22-225">預設值</span><span class="sxs-lookup"><span data-stu-id="29c22-225">Default</span></span>        | <span data-ttu-id="29c22-226">N/A</span><span class="sxs-lookup"><span data-stu-id="29c22-226">N/A</span></span>                              |
| <span data-ttu-id="29c22-227">最小系統</span><span class="sxs-lookup"><span data-stu-id="29c22-227">Minimum system</span></span> | <span data-ttu-id="29c22-228">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="29c22-228">Windows 2000</span></span>                     |



 

### <a name="methodname"></a><span data-ttu-id="29c22-229">MethodName</span><span class="sxs-lookup"><span data-stu-id="29c22-229">MethodName</span></span>



| <span data-ttu-id="29c22-230">進入</span><span class="sxs-lookup"><span data-stu-id="29c22-230">Entry</span></span> | <span data-ttu-id="29c22-231">值</span><span class="sxs-lookup"><span data-stu-id="29c22-231">Value</span></span> |
|----------------|----------------------------------------------|
| <span data-ttu-id="29c22-232">描述</span><span class="sxs-lookup"><span data-stu-id="29c22-232">Description</span></span>    | <span data-ttu-id="29c22-233">要在其上訂閱的介面上的方法。</span><span class="sxs-lookup"><span data-stu-id="29c22-233">Method on the interface being subscribed to.</span></span> |
| <span data-ttu-id="29c22-234">Access</span><span class="sxs-lookup"><span data-stu-id="29c22-234">Access</span></span>         | <span data-ttu-id="29c22-235">讀寫</span><span class="sxs-lookup"><span data-stu-id="29c22-235">ReadWrite</span></span>                                    |
| <span data-ttu-id="29c22-236">類型</span><span class="sxs-lookup"><span data-stu-id="29c22-236">Type</span></span>           | <span data-ttu-id="29c22-237">String</span><span class="sxs-lookup"><span data-stu-id="29c22-237">String</span></span>                                       |
| <span data-ttu-id="29c22-238">預設值</span><span class="sxs-lookup"><span data-stu-id="29c22-238">Default</span></span>        | <span data-ttu-id="29c22-239">N/A</span><span class="sxs-lookup"><span data-stu-id="29c22-239">N/A</span></span>                                          |
| <span data-ttu-id="29c22-240">最小系統</span><span class="sxs-lookup"><span data-stu-id="29c22-240">Minimum system</span></span> | <span data-ttu-id="29c22-241">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="29c22-241">Windows 2000</span></span>                                 |



 

### <a name="name"></a><span data-ttu-id="29c22-242">Name</span><span class="sxs-lookup"><span data-stu-id="29c22-242">Name</span></span>



| <span data-ttu-id="29c22-243">進入</span><span class="sxs-lookup"><span data-stu-id="29c22-243">Entry</span></span> | <span data-ttu-id="29c22-244">值</span><span class="sxs-lookup"><span data-stu-id="29c22-244">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29c22-245">描述</span><span class="sxs-lookup"><span data-stu-id="29c22-245">Description</span></span>    | <span data-ttu-id="29c22-246">訂用帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="29c22-246">The name for the subscription.</span></span> <span data-ttu-id="29c22-247">移除字串開頭和結尾的額外空間。在這個集合的物件上呼叫 [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="29c22-247">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="29c22-248">Access</span><span class="sxs-lookup"><span data-stu-id="29c22-248">Access</span></span>         | <span data-ttu-id="29c22-249">讀寫</span><span class="sxs-lookup"><span data-stu-id="29c22-249">ReadWrite</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="29c22-250">類型</span><span class="sxs-lookup"><span data-stu-id="29c22-250">Type</span></span>           | <span data-ttu-id="29c22-251">String</span><span class="sxs-lookup"><span data-stu-id="29c22-251">String</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="29c22-252">預設值</span><span class="sxs-lookup"><span data-stu-id="29c22-252">Default</span></span>        | <span data-ttu-id="29c22-253">[新增訂用帳戶]</span><span class="sxs-lookup"><span data-stu-id="29c22-253">"New Subscription"</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="29c22-254">最小系統</span><span class="sxs-lookup"><span data-stu-id="29c22-254">Minimum system</span></span> | <span data-ttu-id="29c22-255">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="29c22-255">Windows 2000</span></span>                                                                                                                                                                                                                           |



 

### <a name="peruser"></a><span data-ttu-id="29c22-256">PerUser</span><span class="sxs-lookup"><span data-stu-id="29c22-256">PerUser</span></span>



| <span data-ttu-id="29c22-257">進入</span><span class="sxs-lookup"><span data-stu-id="29c22-257">Entry</span></span> | <span data-ttu-id="29c22-258">值</span><span class="sxs-lookup"><span data-stu-id="29c22-258">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29c22-259">描述</span><span class="sxs-lookup"><span data-stu-id="29c22-259">Description</span></span>    | <span data-ttu-id="29c22-260">指出訂閱是否只適用于指定的使用者（以 UserName 屬性工作表示）。</span><span class="sxs-lookup"><span data-stu-id="29c22-260">Indicates whether the subscription applies only for a given user, represented by the UserName property.</span></span> |
| <span data-ttu-id="29c22-261">Access</span><span class="sxs-lookup"><span data-stu-id="29c22-261">Access</span></span>         | <span data-ttu-id="29c22-262">讀寫</span><span class="sxs-lookup"><span data-stu-id="29c22-262">ReadWrite</span></span>                                                                                               |
| <span data-ttu-id="29c22-263">類型</span><span class="sxs-lookup"><span data-stu-id="29c22-263">Type</span></span>           | <span data-ttu-id="29c22-264">Bool</span><span class="sxs-lookup"><span data-stu-id="29c22-264">Bool</span></span>                                                                                                    |
| <span data-ttu-id="29c22-265">預設</span><span class="sxs-lookup"><span data-stu-id="29c22-265">Default</span></span>        | <span data-ttu-id="29c22-266">否</span><span class="sxs-lookup"><span data-stu-id="29c22-266">False</span></span>                                                                                                   |
| <span data-ttu-id="29c22-267">最小系統</span><span class="sxs-lookup"><span data-stu-id="29c22-267">Minimum system</span></span> | <span data-ttu-id="29c22-268">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="29c22-268">Windows 2000</span></span>                                                                                            |



 

### <a name="publisherid"></a><span data-ttu-id="29c22-269">PublisherID</span><span class="sxs-lookup"><span data-stu-id="29c22-269">PublisherID</span></span>



| <span data-ttu-id="29c22-270">進入</span><span class="sxs-lookup"><span data-stu-id="29c22-270">Entry</span></span> | <span data-ttu-id="29c22-271">值</span><span class="sxs-lookup"><span data-stu-id="29c22-271">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="29c22-272">描述</span><span class="sxs-lookup"><span data-stu-id="29c22-272">Description</span></span>    | <span data-ttu-id="29c22-273">發行者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="29c22-273">ID for the publisher.</span></span> <span data-ttu-id="29c22-274">您可以指定 EventCLSID 或 PublisherID，但不能同時指定兩者。</span><span class="sxs-lookup"><span data-stu-id="29c22-274">You can indicate an EventCLSID or a PublisherID but not both.</span></span> |
| <span data-ttu-id="29c22-275">Access</span><span class="sxs-lookup"><span data-stu-id="29c22-275">Access</span></span>         | <span data-ttu-id="29c22-276">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="29c22-276">WriteOnce</span></span>                                                                           |
| <span data-ttu-id="29c22-277">類型</span><span class="sxs-lookup"><span data-stu-id="29c22-277">Type</span></span>           | <span data-ttu-id="29c22-278">String</span><span class="sxs-lookup"><span data-stu-id="29c22-278">String</span></span>                                                                              |
| <span data-ttu-id="29c22-279">預設值</span><span class="sxs-lookup"><span data-stu-id="29c22-279">Default</span></span>        | <span data-ttu-id="29c22-280">""</span><span class="sxs-lookup"><span data-stu-id="29c22-280">""</span></span>                                                                                  |
| <span data-ttu-id="29c22-281">最小系統</span><span class="sxs-lookup"><span data-stu-id="29c22-281">Minimum system</span></span> | <span data-ttu-id="29c22-282">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="29c22-282">Windows 2000</span></span>                                                                        |



 

### <a name="subscriberinterface"></a><span data-ttu-id="29c22-283">SubscriberInterface</span><span class="sxs-lookup"><span data-stu-id="29c22-283">SubscriberInterface</span></span>



| <span data-ttu-id="29c22-284">進入</span><span class="sxs-lookup"><span data-stu-id="29c22-284">Entry</span></span> | <span data-ttu-id="29c22-285">值</span><span class="sxs-lookup"><span data-stu-id="29c22-285">Value</span></span> |
|----------------|------------------------------------------|
| <span data-ttu-id="29c22-286">描述</span><span class="sxs-lookup"><span data-stu-id="29c22-286">Description</span></span>    | <span data-ttu-id="29c22-287">訂閱者介面的指標。</span><span class="sxs-lookup"><span data-stu-id="29c22-287">A pointer to the subscriber's interface.</span></span> |
| <span data-ttu-id="29c22-288">Access</span><span class="sxs-lookup"><span data-stu-id="29c22-288">Access</span></span>         | <span data-ttu-id="29c22-289">讀寫</span><span class="sxs-lookup"><span data-stu-id="29c22-289">ReadWrite</span></span>                                |
| <span data-ttu-id="29c22-290">類型</span><span class="sxs-lookup"><span data-stu-id="29c22-290">Type</span></span>           | <span data-ttu-id="29c22-291">Variant</span><span class="sxs-lookup"><span data-stu-id="29c22-291">Variant</span></span>                                  |
| <span data-ttu-id="29c22-292">預設</span><span class="sxs-lookup"><span data-stu-id="29c22-292">Default</span></span>        | <span data-ttu-id="29c22-293">N/A</span><span class="sxs-lookup"><span data-stu-id="29c22-293">N/A</span></span>                                      |
| <span data-ttu-id="29c22-294">最小系統</span><span class="sxs-lookup"><span data-stu-id="29c22-294">Minimum system</span></span> | <span data-ttu-id="29c22-295">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="29c22-295">Windows 2000</span></span>                             |



 

### <a name="subscriberpartitionid"></a><span data-ttu-id="29c22-296">SubscriberPartitionID</span><span class="sxs-lookup"><span data-stu-id="29c22-296">SubscriberPartitionID</span></span>



| <span data-ttu-id="29c22-297">進入</span><span class="sxs-lookup"><span data-stu-id="29c22-297">Entry</span></span> | <span data-ttu-id="29c22-298">值</span><span class="sxs-lookup"><span data-stu-id="29c22-298">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29c22-299">描述</span><span class="sxs-lookup"><span data-stu-id="29c22-299">Description</span></span>    | <span data-ttu-id="29c22-300">訂閱相同資料分割中的事件類別時，用來代表訂閱者之資料分割識別碼的 GUID。</span><span class="sxs-lookup"><span data-stu-id="29c22-300">When subscribing to an event class in the same partition, used to represent the GUID of the partition ID of the subscriber.</span></span> <span data-ttu-id="29c22-301">訂閱事件類別時，訂閱者可以選擇訂閱相同或不同資料分割中的事件類別。</span><span class="sxs-lookup"><span data-stu-id="29c22-301">When subscribing to event classes, the subscriber has the option to subscribe to an event class in the same or different partition.</span></span> |
| <span data-ttu-id="29c22-302">Access</span><span class="sxs-lookup"><span data-stu-id="29c22-302">Access</span></span>         | <span data-ttu-id="29c22-303">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="29c22-303">WriteOnce</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="29c22-304">類型</span><span class="sxs-lookup"><span data-stu-id="29c22-304">Type</span></span>           | <span data-ttu-id="29c22-305">String</span><span class="sxs-lookup"><span data-stu-id="29c22-305">String</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="29c22-306">預設值</span><span class="sxs-lookup"><span data-stu-id="29c22-306">Default</span></span>        | <Generated>                                                                                                                                                                                                                                               |
| <span data-ttu-id="29c22-307">最小系統</span><span class="sxs-lookup"><span data-stu-id="29c22-307">Minimum system</span></span> | <span data-ttu-id="29c22-308">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="29c22-308">Windows Server 2003</span></span>                                                                                                                                                                                                                                             |



 

### <a name="username"></a><span data-ttu-id="29c22-309">UserName</span><span class="sxs-lookup"><span data-stu-id="29c22-309">UserName</span></span>



| <span data-ttu-id="29c22-310">進入</span><span class="sxs-lookup"><span data-stu-id="29c22-310">Entry</span></span> | <span data-ttu-id="29c22-311">值</span><span class="sxs-lookup"><span data-stu-id="29c22-311">Value</span></span> |
|----------------|-------------------------------------------------------------------------|
| <span data-ttu-id="29c22-312">描述</span><span class="sxs-lookup"><span data-stu-id="29c22-312">Description</span></span>    | <span data-ttu-id="29c22-313">當 PerUser 為 True 時，訂用帳戶適用的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="29c22-313">The name of user that the subscription applies to when PerUser is True.</span></span> |
| <span data-ttu-id="29c22-314">Access</span><span class="sxs-lookup"><span data-stu-id="29c22-314">Access</span></span>         | <span data-ttu-id="29c22-315">讀寫</span><span class="sxs-lookup"><span data-stu-id="29c22-315">ReadWrite</span></span>                                                               |
| <span data-ttu-id="29c22-316">類型</span><span class="sxs-lookup"><span data-stu-id="29c22-316">Type</span></span>           | <span data-ttu-id="29c22-317">String</span><span class="sxs-lookup"><span data-stu-id="29c22-317">String</span></span>                                                                  |
| <span data-ttu-id="29c22-318">預設值</span><span class="sxs-lookup"><span data-stu-id="29c22-318">Default</span></span>        | <span data-ttu-id="29c22-319">N/A</span><span class="sxs-lookup"><span data-stu-id="29c22-319">N/A</span></span>                                                                     |
| <span data-ttu-id="29c22-320">最小系統</span><span class="sxs-lookup"><span data-stu-id="29c22-320">Minimum system</span></span> | <span data-ttu-id="29c22-321">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="29c22-321">Windows 2000</span></span>                                                            |



 

## <a name="see-also"></a><span data-ttu-id="29c22-322">另請參閱</span><span class="sxs-lookup"><span data-stu-id="29c22-322">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29c22-323">COM + 系統管理集合</span><span class="sxs-lookup"><span data-stu-id="29c22-323">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 

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
# <a name="transientsubscriptions-collection"></a><span data-ttu-id="b6ec8-104">TransientSubscriptions 集合</span><span class="sxs-lookup"><span data-stu-id="b6ec8-104">TransientSubscriptions collection</span></span>

<span data-ttu-id="b6ec8-105">包含每個暫時性訂用帳戶的物件。</span><span class="sxs-lookup"><span data-stu-id="b6ec8-105">Contains an object for each transient subscription.</span></span> <span data-ttu-id="b6ec8-106">您可以針對執行中的物件實例執行暫時的訂閱，並在物件終結時消失。</span><span class="sxs-lookup"><span data-stu-id="b6ec8-106">Transient subscriptions can be created on the fly for running object instances, and they vanish when the object is destroyed.</span></span>

<span data-ttu-id="b6ec8-107">此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**加入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**移除**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。</span><span class="sxs-lookup"><span data-stu-id="b6ec8-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="b6ec8-108">成員</span><span class="sxs-lookup"><span data-stu-id="b6ec8-108">Members</span></span>

<span data-ttu-id="b6ec8-109">**TransientSubscriptions** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。</span><span class="sxs-lookup"><span data-stu-id="b6ec8-109">The **TransientSubscriptions** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="b6ec8-110">相關集合</span><span class="sxs-lookup"><span data-stu-id="b6ec8-110">Related Collections</span></span>

<span data-ttu-id="b6ec8-111">您可以從這個集合流覽至下列任何集合：</span><span class="sxs-lookup"><span data-stu-id="b6ec8-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="b6ec8-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="b6ec8-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="b6ec8-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="b6ec8-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="b6ec8-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="b6ec8-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="b6ec8-115">**TransientPublisherProperties**</span><span class="sxs-lookup"><span data-stu-id="b6ec8-115">**TransientPublisherProperties**</span></span>](transientpublisherproperties.md)
-   [<span data-ttu-id="b6ec8-116">**TransientSubscriberProperties**</span><span class="sxs-lookup"><span data-stu-id="b6ec8-116">**TransientSubscriberProperties**</span></span>](transientsubscriberproperties.md)

<span data-ttu-id="b6ec8-117">您可以從下列集合流覽至這個集合：</span><span class="sxs-lookup"><span data-stu-id="b6ec8-117">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="b6ec8-118">**根**</span><span class="sxs-lookup"><span data-stu-id="b6ec8-118">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="b6ec8-119">屬性</span><span class="sxs-lookup"><span data-stu-id="b6ec8-119">Properties</span></span>

<span data-ttu-id="b6ec8-120">集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="b6ec8-120">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="b6ec8-121">說明</span><span class="sxs-lookup"><span data-stu-id="b6ec8-121">Description</span></span>](#description)
-   [<span data-ttu-id="b6ec8-122">Enabled</span><span class="sxs-lookup"><span data-stu-id="b6ec8-122">Enabled</span></span>](#enabled)
-   [<span data-ttu-id="b6ec8-123">EventClassPartitionID</span><span class="sxs-lookup"><span data-stu-id="b6ec8-123">EventClassPartitionID</span></span>](#eventclasspartitionid)
-   [<span data-ttu-id="b6ec8-124">EventCLSID</span><span class="sxs-lookup"><span data-stu-id="b6ec8-124">EventCLSID</span></span>](#eventclsid)
-   [<span data-ttu-id="b6ec8-125">>filtercriteria</span><span class="sxs-lookup"><span data-stu-id="b6ec8-125">FilterCriteria</span></span>](#filtercriteria)
-   [<span data-ttu-id="b6ec8-126">識別碼</span><span class="sxs-lookup"><span data-stu-id="b6ec8-126">ID</span></span>](#transientsubscriptions-collection)
-   [<span data-ttu-id="b6ec8-127">InterfaceID</span><span class="sxs-lookup"><span data-stu-id="b6ec8-127">InterfaceID</span></span>](#interfaceid)
-   [<span data-ttu-id="b6ec8-128">MethodName</span><span class="sxs-lookup"><span data-stu-id="b6ec8-128">MethodName</span></span>](#methodname)
-   [<span data-ttu-id="b6ec8-129">名稱</span><span class="sxs-lookup"><span data-stu-id="b6ec8-129">Name</span></span>](#methodname)
-   [<span data-ttu-id="b6ec8-130">PerUser</span><span class="sxs-lookup"><span data-stu-id="b6ec8-130">PerUser</span></span>](#peruser)
-   [<span data-ttu-id="b6ec8-131">PublisherID</span><span class="sxs-lookup"><span data-stu-id="b6ec8-131">PublisherID</span></span>](#publisherid)
-   [<span data-ttu-id="b6ec8-132">SubscriberInterface</span><span class="sxs-lookup"><span data-stu-id="b6ec8-132">SubscriberInterface</span></span>](#subscriberinterface)
-   [<span data-ttu-id="b6ec8-133">SubscriberPartitionID</span><span class="sxs-lookup"><span data-stu-id="b6ec8-133">SubscriberPartitionID</span></span>](#subscriberpartitionid)
-   [<span data-ttu-id="b6ec8-134">使用者名稱</span><span class="sxs-lookup"><span data-stu-id="b6ec8-134">UserName</span></span>](#username)

### <a name="description"></a><span data-ttu-id="b6ec8-135">Description</span><span class="sxs-lookup"><span data-stu-id="b6ec8-135">Description</span></span>



| <span data-ttu-id="b6ec8-136">進入</span><span class="sxs-lookup"><span data-stu-id="b6ec8-136">Entry</span></span> | <span data-ttu-id="b6ec8-137">值</span><span class="sxs-lookup"><span data-stu-id="b6ec8-137">Value</span></span> |
|----------------|-------------------------------------|
| <span data-ttu-id="b6ec8-138">描述</span><span class="sxs-lookup"><span data-stu-id="b6ec8-138">Description</span></span>    | <span data-ttu-id="b6ec8-139">訂用帳戶的描述。</span><span class="sxs-lookup"><span data-stu-id="b6ec8-139">A description for the subscription.</span></span> |
| <span data-ttu-id="b6ec8-140">Access</span><span class="sxs-lookup"><span data-stu-id="b6ec8-140">Access</span></span>         | <span data-ttu-id="b6ec8-141">讀寫</span><span class="sxs-lookup"><span data-stu-id="b6ec8-141">ReadWrite</span></span>                           |
| <span data-ttu-id="b6ec8-142">類型</span><span class="sxs-lookup"><span data-stu-id="b6ec8-142">Type</span></span>           | <span data-ttu-id="b6ec8-143">String</span><span class="sxs-lookup"><span data-stu-id="b6ec8-143">String</span></span>                              |
| <span data-ttu-id="b6ec8-144">預設值</span><span class="sxs-lookup"><span data-stu-id="b6ec8-144">Default</span></span>        | <span data-ttu-id="b6ec8-145">""</span><span class="sxs-lookup"><span data-stu-id="b6ec8-145">""</span></span>                                  |
| <span data-ttu-id="b6ec8-146">最小系統</span><span class="sxs-lookup"><span data-stu-id="b6ec8-146">Minimum system</span></span> | <span data-ttu-id="b6ec8-147">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b6ec8-147">Windows 2000</span></span>                        |



 

### <a name="enabled"></a><span data-ttu-id="b6ec8-148">已啟用</span><span class="sxs-lookup"><span data-stu-id="b6ec8-148">Enabled</span></span>



| <span data-ttu-id="b6ec8-149">進入</span><span class="sxs-lookup"><span data-stu-id="b6ec8-149">Entry</span></span> | <span data-ttu-id="b6ec8-150">值</span><span class="sxs-lookup"><span data-stu-id="b6ec8-150">Value</span></span> |
|----------------|----------------------------------------------------------|
| <span data-ttu-id="b6ec8-151">描述</span><span class="sxs-lookup"><span data-stu-id="b6ec8-151">Description</span></span>    | <span data-ttu-id="b6ec8-152">指出目前是否已啟用訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="b6ec8-152">Indicates whether the subscription is presently enabled.</span></span> |
| <span data-ttu-id="b6ec8-153">Access</span><span class="sxs-lookup"><span data-stu-id="b6ec8-153">Access</span></span>         | <span data-ttu-id="b6ec8-154">讀寫</span><span class="sxs-lookup"><span data-stu-id="b6ec8-154">ReadWrite</span></span>                                                |
| <span data-ttu-id="b6ec8-155">類型</span><span class="sxs-lookup"><span data-stu-id="b6ec8-155">Type</span></span>           | <span data-ttu-id="b6ec8-156">Bool</span><span class="sxs-lookup"><span data-stu-id="b6ec8-156">Bool</span></span>                                                     |
| <span data-ttu-id="b6ec8-157">預設</span><span class="sxs-lookup"><span data-stu-id="b6ec8-157">Default</span></span>        | <span data-ttu-id="b6ec8-158">對</span><span class="sxs-lookup"><span data-stu-id="b6ec8-158">True</span></span>                                                     |
| <span data-ttu-id="b6ec8-159">最小系統</span><span class="sxs-lookup"><span data-stu-id="b6ec8-159">Minimum system</span></span> | <span data-ttu-id="b6ec8-160">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b6ec8-160">Windows 2000</span></span>                                             |



 

### <a name="eventclasspartitionid"></a><span data-ttu-id="b6ec8-161">EventClassPartitionID</span><span class="sxs-lookup"><span data-stu-id="b6ec8-161">EventClassPartitionID</span></span>



| <span data-ttu-id="b6ec8-162">進入</span><span class="sxs-lookup"><span data-stu-id="b6ec8-162">Entry</span></span> | <span data-ttu-id="b6ec8-163">值</span><span class="sxs-lookup"><span data-stu-id="b6ec8-163">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6ec8-164">描述</span><span class="sxs-lookup"><span data-stu-id="b6ec8-164">Description</span></span>    | <span data-ttu-id="b6ec8-165">訂閱事件類別時，用來代表包含事件類別之資料分割識別碼的 GUID。</span><span class="sxs-lookup"><span data-stu-id="b6ec8-165">When subscribing to an event class, used to represent the GUID of the partition ID containing the event class.</span></span> <span data-ttu-id="b6ec8-166">訂閱事件類別時，訂閱者可以選擇訂閱相同或不同資料分割中的事件類別。</span><span class="sxs-lookup"><span data-stu-id="b6ec8-166">When subscribing to event classes, the subscriber has the option to subscribe to an event class in the same or different partition.</span></span> |
| <span data-ttu-id="b6ec8-167">Access</span><span class="sxs-lookup"><span data-stu-id="b6ec8-167">Access</span></span>         | <span data-ttu-id="b6ec8-168">讀寫</span><span class="sxs-lookup"><span data-stu-id="b6ec8-168">ReadWrite</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="b6ec8-169">類型</span><span class="sxs-lookup"><span data-stu-id="b6ec8-169">Type</span></span>           | <span data-ttu-id="b6ec8-170">String</span><span class="sxs-lookup"><span data-stu-id="b6ec8-170">String</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="b6ec8-171">預設值</span><span class="sxs-lookup"><span data-stu-id="b6ec8-171">Default</span></span>        | <span data-ttu-id="b6ec8-172">NULL</span><span class="sxs-lookup"><span data-stu-id="b6ec8-172">NULL</span></span>                                                                                                                                                                                                                                               |
| <span data-ttu-id="b6ec8-173">最小系統</span><span class="sxs-lookup"><span data-stu-id="b6ec8-173">Minimum system</span></span> | <span data-ttu-id="b6ec8-174">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b6ec8-174">Windows Server 2003</span></span>                                                                                                                                                                                                                                |



 

### <a name="eventclsid"></a><span data-ttu-id="b6ec8-175">EventCLSID</span><span class="sxs-lookup"><span data-stu-id="b6ec8-175">EventCLSID</span></span>



| <span data-ttu-id="b6ec8-176">進入</span><span class="sxs-lookup"><span data-stu-id="b6ec8-176">Entry</span></span> | <span data-ttu-id="b6ec8-177">值</span><span class="sxs-lookup"><span data-stu-id="b6ec8-177">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6ec8-178">描述</span><span class="sxs-lookup"><span data-stu-id="b6ec8-178">Description</span></span>    | <span data-ttu-id="b6ec8-179">事件類別的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="b6ec8-179">The CLSID for the event class.</span></span> <span data-ttu-id="b6ec8-180">您可以指定 EventCLSID 或 PublisherID，但不能同時指定兩者。</span><span class="sxs-lookup"><span data-stu-id="b6ec8-180">You can indicate an EventCLSID or a PublisherID but not both.</span></span> |
| <span data-ttu-id="b6ec8-181">Access</span><span class="sxs-lookup"><span data-stu-id="b6ec8-181">Access</span></span>         | <span data-ttu-id="b6ec8-182">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="b6ec8-182">WriteOnce</span></span>                                                                                    |
| <span data-ttu-id="b6ec8-183">類型</span><span class="sxs-lookup"><span data-stu-id="b6ec8-183">Type</span></span>           | <span data-ttu-id="b6ec8-184">String</span><span class="sxs-lookup"><span data-stu-id="b6ec8-184">String</span></span>                                                                                       |
| <span data-ttu-id="b6ec8-185">預設值</span><span class="sxs-lookup"><span data-stu-id="b6ec8-185">Default</span></span>        | <span data-ttu-id="b6ec8-186">N/A</span><span class="sxs-lookup"><span data-stu-id="b6ec8-186">N/A</span></span>                                                                                          |
| <span data-ttu-id="b6ec8-187">最小系統</span><span class="sxs-lookup"><span data-stu-id="b6ec8-187">Minimum system</span></span> | <span data-ttu-id="b6ec8-188">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b6ec8-188">Windows 2000</span></span>                                                                                 |



 

### <a name="filtercriteria"></a><span data-ttu-id="b6ec8-189">>filtercriteria</span><span class="sxs-lookup"><span data-stu-id="b6ec8-189">FilterCriteria</span></span>



| <span data-ttu-id="b6ec8-190">進入</span><span class="sxs-lookup"><span data-stu-id="b6ec8-190">Entry</span></span> | <span data-ttu-id="b6ec8-191">值</span><span class="sxs-lookup"><span data-stu-id="b6ec8-191">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6ec8-192">描述</span><span class="sxs-lookup"><span data-stu-id="b6ec8-192">Description</span></span>    | <span data-ttu-id="b6ec8-193">指出篩選準則的字串。</span><span class="sxs-lookup"><span data-stu-id="b6ec8-193">A string that indicates the filter criteria.</span></span> <span data-ttu-id="b6ec8-194">可以是 [**PublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) 類別的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="b6ec8-194">Can be a CLSID for a [**PublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) class.</span></span> |
| <span data-ttu-id="b6ec8-195">Access</span><span class="sxs-lookup"><span data-stu-id="b6ec8-195">Access</span></span>         | <span data-ttu-id="b6ec8-196">讀寫</span><span class="sxs-lookup"><span data-stu-id="b6ec8-196">ReadWrite</span></span>                                                                                                            |
| <span data-ttu-id="b6ec8-197">類型</span><span class="sxs-lookup"><span data-stu-id="b6ec8-197">Type</span></span>           | <span data-ttu-id="b6ec8-198">String</span><span class="sxs-lookup"><span data-stu-id="b6ec8-198">String</span></span>                                                                                                               |
| <span data-ttu-id="b6ec8-199">預設值</span><span class="sxs-lookup"><span data-stu-id="b6ec8-199">Default</span></span>        | <span data-ttu-id="b6ec8-200">N/A</span><span class="sxs-lookup"><span data-stu-id="b6ec8-200">N/A</span></span>                                                                                                                  |
| <span data-ttu-id="b6ec8-201">最小系統</span><span class="sxs-lookup"><span data-stu-id="b6ec8-201">Minimum system</span></span> | <span data-ttu-id="b6ec8-202">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b6ec8-202">Windows 2000</span></span>                                                                                                         |



 

### <a name="id"></a><span data-ttu-id="b6ec8-203">識別碼</span><span class="sxs-lookup"><span data-stu-id="b6ec8-203">ID</span></span>



| <span data-ttu-id="b6ec8-204">進入</span><span class="sxs-lookup"><span data-stu-id="b6ec8-204">Entry</span></span> | <span data-ttu-id="b6ec8-205">值</span><span class="sxs-lookup"><span data-stu-id="b6ec8-205">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6ec8-206">描述</span><span class="sxs-lookup"><span data-stu-id="b6ec8-206">Description</span></span>    | <span data-ttu-id="b6ec8-207">訂用帳戶的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b6ec8-207">Identifier for the subscription.</span></span> <span data-ttu-id="b6ec8-208">當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="b6ec8-208">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="b6ec8-209">Access</span><span class="sxs-lookup"><span data-stu-id="b6ec8-209">Access</span></span>         | <span data-ttu-id="b6ec8-210">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="b6ec8-210">WriteOnce</span></span>                                                                                                                                                        |
| <span data-ttu-id="b6ec8-211">類型</span><span class="sxs-lookup"><span data-stu-id="b6ec8-211">Type</span></span>           | <span data-ttu-id="b6ec8-212">String</span><span class="sxs-lookup"><span data-stu-id="b6ec8-212">String</span></span>                                                                                                                                                           |
| <span data-ttu-id="b6ec8-213">預設值</span><span class="sxs-lookup"><span data-stu-id="b6ec8-213">Default</span></span>        | <Generated>                                                                                                                                                |
| <span data-ttu-id="b6ec8-214">最小系統</span><span class="sxs-lookup"><span data-stu-id="b6ec8-214">Minimum system</span></span> | <span data-ttu-id="b6ec8-215">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b6ec8-215">Windows 2000</span></span>                                                                                                                                                     |



 

### <a name="interfaceid"></a><span data-ttu-id="b6ec8-216">InterfaceID</span><span class="sxs-lookup"><span data-stu-id="b6ec8-216">InterfaceID</span></span>



| <span data-ttu-id="b6ec8-217">進入</span><span class="sxs-lookup"><span data-stu-id="b6ec8-217">Entry</span></span> | <span data-ttu-id="b6ec8-218">值</span><span class="sxs-lookup"><span data-stu-id="b6ec8-218">Value</span></span> |
|----------------|----------------------------------|
| <span data-ttu-id="b6ec8-219">描述</span><span class="sxs-lookup"><span data-stu-id="b6ec8-219">Description</span></span>    | <span data-ttu-id="b6ec8-220">已訂閱之介面的 IID。</span><span class="sxs-lookup"><span data-stu-id="b6ec8-220">IID for interface subscribed to.</span></span> |
| <span data-ttu-id="b6ec8-221">Access</span><span class="sxs-lookup"><span data-stu-id="b6ec8-221">Access</span></span>         | <span data-ttu-id="b6ec8-222">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="b6ec8-222">WriteOnce</span></span>                        |
| <span data-ttu-id="b6ec8-223">類型</span><span class="sxs-lookup"><span data-stu-id="b6ec8-223">Type</span></span>           | <span data-ttu-id="b6ec8-224">String</span><span class="sxs-lookup"><span data-stu-id="b6ec8-224">String</span></span>                           |
| <span data-ttu-id="b6ec8-225">預設值</span><span class="sxs-lookup"><span data-stu-id="b6ec8-225">Default</span></span>        | <span data-ttu-id="b6ec8-226">N/A</span><span class="sxs-lookup"><span data-stu-id="b6ec8-226">N/A</span></span>                              |
| <span data-ttu-id="b6ec8-227">最小系統</span><span class="sxs-lookup"><span data-stu-id="b6ec8-227">Minimum system</span></span> | <span data-ttu-id="b6ec8-228">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b6ec8-228">Windows 2000</span></span>                     |



 

### <a name="methodname"></a><span data-ttu-id="b6ec8-229">MethodName</span><span class="sxs-lookup"><span data-stu-id="b6ec8-229">MethodName</span></span>



| <span data-ttu-id="b6ec8-230">進入</span><span class="sxs-lookup"><span data-stu-id="b6ec8-230">Entry</span></span> | <span data-ttu-id="b6ec8-231">值</span><span class="sxs-lookup"><span data-stu-id="b6ec8-231">Value</span></span> |
|----------------|----------------------------------------------|
| <span data-ttu-id="b6ec8-232">描述</span><span class="sxs-lookup"><span data-stu-id="b6ec8-232">Description</span></span>    | <span data-ttu-id="b6ec8-233">要在其上訂閱的介面上的方法。</span><span class="sxs-lookup"><span data-stu-id="b6ec8-233">Method on the interface being subscribed to.</span></span> |
| <span data-ttu-id="b6ec8-234">Access</span><span class="sxs-lookup"><span data-stu-id="b6ec8-234">Access</span></span>         | <span data-ttu-id="b6ec8-235">讀寫</span><span class="sxs-lookup"><span data-stu-id="b6ec8-235">ReadWrite</span></span>                                    |
| <span data-ttu-id="b6ec8-236">類型</span><span class="sxs-lookup"><span data-stu-id="b6ec8-236">Type</span></span>           | <span data-ttu-id="b6ec8-237">String</span><span class="sxs-lookup"><span data-stu-id="b6ec8-237">String</span></span>                                       |
| <span data-ttu-id="b6ec8-238">預設值</span><span class="sxs-lookup"><span data-stu-id="b6ec8-238">Default</span></span>        | <span data-ttu-id="b6ec8-239">N/A</span><span class="sxs-lookup"><span data-stu-id="b6ec8-239">N/A</span></span>                                          |
| <span data-ttu-id="b6ec8-240">最小系統</span><span class="sxs-lookup"><span data-stu-id="b6ec8-240">Minimum system</span></span> | <span data-ttu-id="b6ec8-241">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b6ec8-241">Windows 2000</span></span>                                 |



 

### <a name="name"></a><span data-ttu-id="b6ec8-242">Name</span><span class="sxs-lookup"><span data-stu-id="b6ec8-242">Name</span></span>



| <span data-ttu-id="b6ec8-243">進入</span><span class="sxs-lookup"><span data-stu-id="b6ec8-243">Entry</span></span> | <span data-ttu-id="b6ec8-244">值</span><span class="sxs-lookup"><span data-stu-id="b6ec8-244">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6ec8-245">描述</span><span class="sxs-lookup"><span data-stu-id="b6ec8-245">Description</span></span>    | <span data-ttu-id="b6ec8-246">訂用帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="b6ec8-246">The name for the subscription.</span></span> <span data-ttu-id="b6ec8-247">移除字串開頭和結尾的額外空間。在這個集合的物件上呼叫 [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="b6ec8-247">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="b6ec8-248">Access</span><span class="sxs-lookup"><span data-stu-id="b6ec8-248">Access</span></span>         | <span data-ttu-id="b6ec8-249">讀寫</span><span class="sxs-lookup"><span data-stu-id="b6ec8-249">ReadWrite</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="b6ec8-250">類型</span><span class="sxs-lookup"><span data-stu-id="b6ec8-250">Type</span></span>           | <span data-ttu-id="b6ec8-251">String</span><span class="sxs-lookup"><span data-stu-id="b6ec8-251">String</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="b6ec8-252">預設值</span><span class="sxs-lookup"><span data-stu-id="b6ec8-252">Default</span></span>        | <span data-ttu-id="b6ec8-253">[新增訂用帳戶]</span><span class="sxs-lookup"><span data-stu-id="b6ec8-253">"New Subscription"</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="b6ec8-254">最小系統</span><span class="sxs-lookup"><span data-stu-id="b6ec8-254">Minimum system</span></span> | <span data-ttu-id="b6ec8-255">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b6ec8-255">Windows 2000</span></span>                                                                                                                                                                                                                           |



 

### <a name="peruser"></a><span data-ttu-id="b6ec8-256">PerUser</span><span class="sxs-lookup"><span data-stu-id="b6ec8-256">PerUser</span></span>



| <span data-ttu-id="b6ec8-257">進入</span><span class="sxs-lookup"><span data-stu-id="b6ec8-257">Entry</span></span> | <span data-ttu-id="b6ec8-258">值</span><span class="sxs-lookup"><span data-stu-id="b6ec8-258">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6ec8-259">描述</span><span class="sxs-lookup"><span data-stu-id="b6ec8-259">Description</span></span>    | <span data-ttu-id="b6ec8-260">指出訂閱是否只適用于指定的使用者（以 UserName 屬性工作表示）。</span><span class="sxs-lookup"><span data-stu-id="b6ec8-260">Indicates whether the subscription applies only for a given user, represented by the UserName property.</span></span> |
| <span data-ttu-id="b6ec8-261">Access</span><span class="sxs-lookup"><span data-stu-id="b6ec8-261">Access</span></span>         | <span data-ttu-id="b6ec8-262">讀寫</span><span class="sxs-lookup"><span data-stu-id="b6ec8-262">ReadWrite</span></span>                                                                                               |
| <span data-ttu-id="b6ec8-263">類型</span><span class="sxs-lookup"><span data-stu-id="b6ec8-263">Type</span></span>           | <span data-ttu-id="b6ec8-264">Bool</span><span class="sxs-lookup"><span data-stu-id="b6ec8-264">Bool</span></span>                                                                                                    |
| <span data-ttu-id="b6ec8-265">預設</span><span class="sxs-lookup"><span data-stu-id="b6ec8-265">Default</span></span>        | <span data-ttu-id="b6ec8-266">否</span><span class="sxs-lookup"><span data-stu-id="b6ec8-266">False</span></span>                                                                                                   |
| <span data-ttu-id="b6ec8-267">最小系統</span><span class="sxs-lookup"><span data-stu-id="b6ec8-267">Minimum system</span></span> | <span data-ttu-id="b6ec8-268">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b6ec8-268">Windows 2000</span></span>                                                                                            |



 

### <a name="publisherid"></a><span data-ttu-id="b6ec8-269">PublisherID</span><span class="sxs-lookup"><span data-stu-id="b6ec8-269">PublisherID</span></span>



| <span data-ttu-id="b6ec8-270">進入</span><span class="sxs-lookup"><span data-stu-id="b6ec8-270">Entry</span></span> | <span data-ttu-id="b6ec8-271">值</span><span class="sxs-lookup"><span data-stu-id="b6ec8-271">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b6ec8-272">描述</span><span class="sxs-lookup"><span data-stu-id="b6ec8-272">Description</span></span>    | <span data-ttu-id="b6ec8-273">發行者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b6ec8-273">ID for the publisher.</span></span> <span data-ttu-id="b6ec8-274">您可以指定 EventCLSID 或 PublisherID，但不能同時指定兩者。</span><span class="sxs-lookup"><span data-stu-id="b6ec8-274">You can indicate an EventCLSID or a PublisherID but not both.</span></span> |
| <span data-ttu-id="b6ec8-275">Access</span><span class="sxs-lookup"><span data-stu-id="b6ec8-275">Access</span></span>         | <span data-ttu-id="b6ec8-276">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="b6ec8-276">WriteOnce</span></span>                                                                           |
| <span data-ttu-id="b6ec8-277">類型</span><span class="sxs-lookup"><span data-stu-id="b6ec8-277">Type</span></span>           | <span data-ttu-id="b6ec8-278">String</span><span class="sxs-lookup"><span data-stu-id="b6ec8-278">String</span></span>                                                                              |
| <span data-ttu-id="b6ec8-279">預設值</span><span class="sxs-lookup"><span data-stu-id="b6ec8-279">Default</span></span>        | <span data-ttu-id="b6ec8-280">""</span><span class="sxs-lookup"><span data-stu-id="b6ec8-280">""</span></span>                                                                                  |
| <span data-ttu-id="b6ec8-281">最小系統</span><span class="sxs-lookup"><span data-stu-id="b6ec8-281">Minimum system</span></span> | <span data-ttu-id="b6ec8-282">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b6ec8-282">Windows 2000</span></span>                                                                        |



 

### <a name="subscriberinterface"></a><span data-ttu-id="b6ec8-283">SubscriberInterface</span><span class="sxs-lookup"><span data-stu-id="b6ec8-283">SubscriberInterface</span></span>



| <span data-ttu-id="b6ec8-284">進入</span><span class="sxs-lookup"><span data-stu-id="b6ec8-284">Entry</span></span> | <span data-ttu-id="b6ec8-285">值</span><span class="sxs-lookup"><span data-stu-id="b6ec8-285">Value</span></span> |
|----------------|------------------------------------------|
| <span data-ttu-id="b6ec8-286">描述</span><span class="sxs-lookup"><span data-stu-id="b6ec8-286">Description</span></span>    | <span data-ttu-id="b6ec8-287">訂閱者介面的指標。</span><span class="sxs-lookup"><span data-stu-id="b6ec8-287">A pointer to the subscriber's interface.</span></span> |
| <span data-ttu-id="b6ec8-288">Access</span><span class="sxs-lookup"><span data-stu-id="b6ec8-288">Access</span></span>         | <span data-ttu-id="b6ec8-289">讀寫</span><span class="sxs-lookup"><span data-stu-id="b6ec8-289">ReadWrite</span></span>                                |
| <span data-ttu-id="b6ec8-290">類型</span><span class="sxs-lookup"><span data-stu-id="b6ec8-290">Type</span></span>           | <span data-ttu-id="b6ec8-291">Variant</span><span class="sxs-lookup"><span data-stu-id="b6ec8-291">Variant</span></span>                                  |
| <span data-ttu-id="b6ec8-292">預設</span><span class="sxs-lookup"><span data-stu-id="b6ec8-292">Default</span></span>        | <span data-ttu-id="b6ec8-293">N/A</span><span class="sxs-lookup"><span data-stu-id="b6ec8-293">N/A</span></span>                                      |
| <span data-ttu-id="b6ec8-294">最小系統</span><span class="sxs-lookup"><span data-stu-id="b6ec8-294">Minimum system</span></span> | <span data-ttu-id="b6ec8-295">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b6ec8-295">Windows 2000</span></span>                             |



 

### <a name="subscriberpartitionid"></a><span data-ttu-id="b6ec8-296">SubscriberPartitionID</span><span class="sxs-lookup"><span data-stu-id="b6ec8-296">SubscriberPartitionID</span></span>



| <span data-ttu-id="b6ec8-297">進入</span><span class="sxs-lookup"><span data-stu-id="b6ec8-297">Entry</span></span> | <span data-ttu-id="b6ec8-298">值</span><span class="sxs-lookup"><span data-stu-id="b6ec8-298">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6ec8-299">描述</span><span class="sxs-lookup"><span data-stu-id="b6ec8-299">Description</span></span>    | <span data-ttu-id="b6ec8-300">訂閱相同資料分割中的事件類別時，用來代表訂閱者之資料分割識別碼的 GUID。</span><span class="sxs-lookup"><span data-stu-id="b6ec8-300">When subscribing to an event class in the same partition, used to represent the GUID of the partition ID of the subscriber.</span></span> <span data-ttu-id="b6ec8-301">訂閱事件類別時，訂閱者可以選擇訂閱相同或不同資料分割中的事件類別。</span><span class="sxs-lookup"><span data-stu-id="b6ec8-301">When subscribing to event classes, the subscriber has the option to subscribe to an event class in the same or different partition.</span></span> |
| <span data-ttu-id="b6ec8-302">Access</span><span class="sxs-lookup"><span data-stu-id="b6ec8-302">Access</span></span>         | <span data-ttu-id="b6ec8-303">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="b6ec8-303">WriteOnce</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="b6ec8-304">類型</span><span class="sxs-lookup"><span data-stu-id="b6ec8-304">Type</span></span>           | <span data-ttu-id="b6ec8-305">String</span><span class="sxs-lookup"><span data-stu-id="b6ec8-305">String</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="b6ec8-306">預設值</span><span class="sxs-lookup"><span data-stu-id="b6ec8-306">Default</span></span>        | <Generated>                                                                                                                                                                                                                                               |
| <span data-ttu-id="b6ec8-307">最小系統</span><span class="sxs-lookup"><span data-stu-id="b6ec8-307">Minimum system</span></span> | <span data-ttu-id="b6ec8-308">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b6ec8-308">Windows Server 2003</span></span>                                                                                                                                                                                                                                             |



 

### <a name="username"></a><span data-ttu-id="b6ec8-309">UserName</span><span class="sxs-lookup"><span data-stu-id="b6ec8-309">UserName</span></span>



| <span data-ttu-id="b6ec8-310">進入</span><span class="sxs-lookup"><span data-stu-id="b6ec8-310">Entry</span></span> | <span data-ttu-id="b6ec8-311">值</span><span class="sxs-lookup"><span data-stu-id="b6ec8-311">Value</span></span> |
|----------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b6ec8-312">描述</span><span class="sxs-lookup"><span data-stu-id="b6ec8-312">Description</span></span>    | <span data-ttu-id="b6ec8-313">當 PerUser 為 True 時，訂用帳戶適用的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="b6ec8-313">The name of user that the subscription applies to when PerUser is True.</span></span> |
| <span data-ttu-id="b6ec8-314">Access</span><span class="sxs-lookup"><span data-stu-id="b6ec8-314">Access</span></span>         | <span data-ttu-id="b6ec8-315">讀寫</span><span class="sxs-lookup"><span data-stu-id="b6ec8-315">ReadWrite</span></span>                                                               |
| <span data-ttu-id="b6ec8-316">類型</span><span class="sxs-lookup"><span data-stu-id="b6ec8-316">Type</span></span>           | <span data-ttu-id="b6ec8-317">String</span><span class="sxs-lookup"><span data-stu-id="b6ec8-317">String</span></span>                                                                  |
| <span data-ttu-id="b6ec8-318">預設值</span><span class="sxs-lookup"><span data-stu-id="b6ec8-318">Default</span></span>        | <span data-ttu-id="b6ec8-319">N/A</span><span class="sxs-lookup"><span data-stu-id="b6ec8-319">N/A</span></span>                                                                     |
| <span data-ttu-id="b6ec8-320">最小系統</span><span class="sxs-lookup"><span data-stu-id="b6ec8-320">Minimum system</span></span> | <span data-ttu-id="b6ec8-321">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b6ec8-321">Windows 2000</span></span>                                                            |



 

## <a name="see-also"></a><span data-ttu-id="b6ec8-322">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b6ec8-322">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6ec8-323">COM + 系統管理集合</span><span class="sxs-lookup"><span data-stu-id="b6ec8-323">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 

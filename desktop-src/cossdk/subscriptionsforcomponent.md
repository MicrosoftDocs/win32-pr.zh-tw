---
description: 包含父元件集合之每個訂用帳戶的物件。
ms.assetid: ec93d500-32bf-4e67-9eda-c1fe0349faa2
title: SubscriptionsForComponent 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscriptionsForComponent
api_type:
- COM
api_location: ''
ms.openlocfilehash: c8334aa54b56a9dccaa7aa0787d8c997baf0445e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973572"
---
# <a name="subscriptionsforcomponent-collection"></a><span data-ttu-id="041ed-103">SubscriptionsForComponent 集合</span><span class="sxs-lookup"><span data-stu-id="041ed-103">SubscriptionsForComponent collection</span></span>

<span data-ttu-id="041ed-104">包含父 [**元件**](components.md) 集合之每個訂用帳戶的物件。</span><span class="sxs-lookup"><span data-stu-id="041ed-104">Contains an object for each subscription for the parent [**Components**](components.md) collection.</span></span>

<span data-ttu-id="041ed-105">此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**加入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**移除**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。</span><span class="sxs-lookup"><span data-stu-id="041ed-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="041ed-106">成員</span><span class="sxs-lookup"><span data-stu-id="041ed-106">Members</span></span>

<span data-ttu-id="041ed-107">**SubscriptionsForComponent** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。</span><span class="sxs-lookup"><span data-stu-id="041ed-107">The **SubscriptionsForComponent** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="041ed-108">相關集合</span><span class="sxs-lookup"><span data-stu-id="041ed-108">Related Collections</span></span>

<span data-ttu-id="041ed-109">您可以從這個集合流覽至下列任何集合：</span><span class="sxs-lookup"><span data-stu-id="041ed-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="041ed-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="041ed-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="041ed-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="041ed-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="041ed-112">**PublisherProperties**</span><span class="sxs-lookup"><span data-stu-id="041ed-112">**PublisherProperties**</span></span>](publisherproperties.md)
-   [<span data-ttu-id="041ed-113">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="041ed-113">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="041ed-114">**SubscriberProperties**</span><span class="sxs-lookup"><span data-stu-id="041ed-114">**SubscriberProperties**</span></span>](subscriberproperties.md)

<span data-ttu-id="041ed-115">您可以從下列集合流覽至這個集合：</span><span class="sxs-lookup"><span data-stu-id="041ed-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="041ed-116">**單元**</span><span class="sxs-lookup"><span data-stu-id="041ed-116">**Components**</span></span>](components.md)

## <a name="properties"></a><span data-ttu-id="041ed-117">屬性</span><span class="sxs-lookup"><span data-stu-id="041ed-117">Properties</span></span>

<span data-ttu-id="041ed-118">集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="041ed-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="041ed-119">說明</span><span class="sxs-lookup"><span data-stu-id="041ed-119">Description</span></span>](#description)
-   [<span data-ttu-id="041ed-120">Enabled</span><span class="sxs-lookup"><span data-stu-id="041ed-120">Enabled</span></span>](#enabled)
-   [<span data-ttu-id="041ed-121">EventClassPartitionID</span><span class="sxs-lookup"><span data-stu-id="041ed-121">EventClassPartitionID</span></span>](#eventclasspartitionid)
-   [<span data-ttu-id="041ed-122">EventCLSID</span><span class="sxs-lookup"><span data-stu-id="041ed-122">EventCLSID</span></span>](#eventclsid)
-   [<span data-ttu-id="041ed-123">>filtercriteria</span><span class="sxs-lookup"><span data-stu-id="041ed-123">FilterCriteria</span></span>](#filtercriteria)
-   [<span data-ttu-id="041ed-124">識別碼</span><span class="sxs-lookup"><span data-stu-id="041ed-124">ID</span></span>](#subscriptionsforcomponent-collection)
-   [<span data-ttu-id="041ed-125">InterfaceID</span><span class="sxs-lookup"><span data-stu-id="041ed-125">InterfaceID</span></span>](#interfaceid)
-   [<span data-ttu-id="041ed-126">MachineName</span><span class="sxs-lookup"><span data-stu-id="041ed-126">MachineName</span></span>](#machinename)
-   [<span data-ttu-id="041ed-127">MethodName</span><span class="sxs-lookup"><span data-stu-id="041ed-127">MethodName</span></span>](#methodname)
-   [<span data-ttu-id="041ed-128">名稱</span><span class="sxs-lookup"><span data-stu-id="041ed-128">Name</span></span>](#machinename)
-   [<span data-ttu-id="041ed-129">PerUser</span><span class="sxs-lookup"><span data-stu-id="041ed-129">PerUser</span></span>](#peruser)
-   [<span data-ttu-id="041ed-130">PublisherID</span><span class="sxs-lookup"><span data-stu-id="041ed-130">PublisherID</span></span>](#publisherid)
-   [<span data-ttu-id="041ed-131">已排入佇列</span><span class="sxs-lookup"><span data-stu-id="041ed-131">Queued</span></span>](#queued)
-   [<span data-ttu-id="041ed-132">SubscriberMoniker</span><span class="sxs-lookup"><span data-stu-id="041ed-132">SubscriberMoniker</span></span>](#subscribermoniker)
-   [<span data-ttu-id="041ed-133">SubscriberPartitionID</span><span class="sxs-lookup"><span data-stu-id="041ed-133">SubscriberPartitionID</span></span>](#subscriberpartitionid)
-   [<span data-ttu-id="041ed-134">使用者名稱</span><span class="sxs-lookup"><span data-stu-id="041ed-134">UserName</span></span>](#username)

### <a name="description"></a><span data-ttu-id="041ed-135">Description</span><span class="sxs-lookup"><span data-stu-id="041ed-135">Description</span></span>



| <span data-ttu-id="041ed-136">進入</span><span class="sxs-lookup"><span data-stu-id="041ed-136">Entry</span></span> | <span data-ttu-id="041ed-137">值</span><span class="sxs-lookup"><span data-stu-id="041ed-137">Value</span></span> |
|----------------|-------------------------------------|
| <span data-ttu-id="041ed-138">描述</span><span class="sxs-lookup"><span data-stu-id="041ed-138">Description</span></span>    | <span data-ttu-id="041ed-139">訂用帳戶的描述。</span><span class="sxs-lookup"><span data-stu-id="041ed-139">A description for the subscription.</span></span> |
| <span data-ttu-id="041ed-140">Access</span><span class="sxs-lookup"><span data-stu-id="041ed-140">Access</span></span>         | <span data-ttu-id="041ed-141">讀寫</span><span class="sxs-lookup"><span data-stu-id="041ed-141">ReadWrite</span></span>                           |
| <span data-ttu-id="041ed-142">類型</span><span class="sxs-lookup"><span data-stu-id="041ed-142">Type</span></span>           | <span data-ttu-id="041ed-143">String</span><span class="sxs-lookup"><span data-stu-id="041ed-143">String</span></span>                              |
| <span data-ttu-id="041ed-144">預設值</span><span class="sxs-lookup"><span data-stu-id="041ed-144">Default</span></span>        | <span data-ttu-id="041ed-145">""</span><span class="sxs-lookup"><span data-stu-id="041ed-145">""</span></span>                                  |
| <span data-ttu-id="041ed-146">最小系統</span><span class="sxs-lookup"><span data-stu-id="041ed-146">Minimum system</span></span> | <span data-ttu-id="041ed-147">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="041ed-147">Windows 2000</span></span>                        |



 

### <a name="enabled"></a><span data-ttu-id="041ed-148">已啟用</span><span class="sxs-lookup"><span data-stu-id="041ed-148">Enabled</span></span>



| <span data-ttu-id="041ed-149">進入</span><span class="sxs-lookup"><span data-stu-id="041ed-149">Entry</span></span> | <span data-ttu-id="041ed-150">值</span><span class="sxs-lookup"><span data-stu-id="041ed-150">Value</span></span> |
|----------------|----------------------------------------------------------|
| <span data-ttu-id="041ed-151">描述</span><span class="sxs-lookup"><span data-stu-id="041ed-151">Description</span></span>    | <span data-ttu-id="041ed-152">指出目前是否已啟用訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="041ed-152">Indicates whether the subscription is presently enabled.</span></span> |
| <span data-ttu-id="041ed-153">Access</span><span class="sxs-lookup"><span data-stu-id="041ed-153">Access</span></span>         | <span data-ttu-id="041ed-154">讀寫</span><span class="sxs-lookup"><span data-stu-id="041ed-154">ReadWrite</span></span>                                                |
| <span data-ttu-id="041ed-155">類型</span><span class="sxs-lookup"><span data-stu-id="041ed-155">Type</span></span>           | <span data-ttu-id="041ed-156">Bool</span><span class="sxs-lookup"><span data-stu-id="041ed-156">Bool</span></span>                                                     |
| <span data-ttu-id="041ed-157">預設</span><span class="sxs-lookup"><span data-stu-id="041ed-157">Default</span></span>        | <span data-ttu-id="041ed-158">對</span><span class="sxs-lookup"><span data-stu-id="041ed-158">True</span></span>                                                     |
| <span data-ttu-id="041ed-159">最小系統</span><span class="sxs-lookup"><span data-stu-id="041ed-159">Minimum system</span></span> | <span data-ttu-id="041ed-160">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="041ed-160">Windows 2000</span></span>                                             |



 

### <a name="eventclasspartitionid"></a><span data-ttu-id="041ed-161">EventClassPartitionID</span><span class="sxs-lookup"><span data-stu-id="041ed-161">EventClassPartitionID</span></span>



| <span data-ttu-id="041ed-162">進入</span><span class="sxs-lookup"><span data-stu-id="041ed-162">Entry</span></span> | <span data-ttu-id="041ed-163">值</span><span class="sxs-lookup"><span data-stu-id="041ed-163">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="041ed-164">描述</span><span class="sxs-lookup"><span data-stu-id="041ed-164">Description</span></span>    | <span data-ttu-id="041ed-165">訂閱事件類別時，用來代表包含事件類別之資料分割識別碼的 GUID。</span><span class="sxs-lookup"><span data-stu-id="041ed-165">When subscribing to an event class, used to represent the GUID of the partition ID containing the event class.</span></span> <span data-ttu-id="041ed-166">訂閱事件類別時，訂閱者可以選擇訂閱相同或不同資料分割中的事件類別。</span><span class="sxs-lookup"><span data-stu-id="041ed-166">When subscribing to event classes, the subscriber has the option to subscribe to an event class in the same or different partition.</span></span> |
| <span data-ttu-id="041ed-167">Access</span><span class="sxs-lookup"><span data-stu-id="041ed-167">Access</span></span>         | <span data-ttu-id="041ed-168">讀寫</span><span class="sxs-lookup"><span data-stu-id="041ed-168">ReadWrite</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="041ed-169">類型</span><span class="sxs-lookup"><span data-stu-id="041ed-169">Type</span></span>           | <span data-ttu-id="041ed-170">String</span><span class="sxs-lookup"><span data-stu-id="041ed-170">String</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="041ed-171">預設值</span><span class="sxs-lookup"><span data-stu-id="041ed-171">Default</span></span>        | <span data-ttu-id="041ed-172">NULL</span><span class="sxs-lookup"><span data-stu-id="041ed-172">NULL</span></span>                                                                                                                                                                                                                                               |
| <span data-ttu-id="041ed-173">最小系統</span><span class="sxs-lookup"><span data-stu-id="041ed-173">Minimum system</span></span> | <span data-ttu-id="041ed-174">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="041ed-174">Windows Server 2003</span></span>                                                                                                                                                                                                                                |



 

### <a name="eventclsid"></a><span data-ttu-id="041ed-175">EventCLSID</span><span class="sxs-lookup"><span data-stu-id="041ed-175">EventCLSID</span></span>



| <span data-ttu-id="041ed-176">進入</span><span class="sxs-lookup"><span data-stu-id="041ed-176">Entry</span></span> | <span data-ttu-id="041ed-177">值</span><span class="sxs-lookup"><span data-stu-id="041ed-177">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="041ed-178">描述</span><span class="sxs-lookup"><span data-stu-id="041ed-178">Description</span></span>    | <span data-ttu-id="041ed-179">事件類別的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="041ed-179">The CLSID for the event class.</span></span> <span data-ttu-id="041ed-180">您可以指定 EventCLSID 或 PublisherID，但不能同時指定兩者。</span><span class="sxs-lookup"><span data-stu-id="041ed-180">You can indicate an EventCLSID or a PublisherID but not both.</span></span> |
| <span data-ttu-id="041ed-181">Access</span><span class="sxs-lookup"><span data-stu-id="041ed-181">Access</span></span>         | <span data-ttu-id="041ed-182">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="041ed-182">WriteOnce</span></span>                                                                                    |
| <span data-ttu-id="041ed-183">類型</span><span class="sxs-lookup"><span data-stu-id="041ed-183">Type</span></span>           | <span data-ttu-id="041ed-184">String</span><span class="sxs-lookup"><span data-stu-id="041ed-184">String</span></span>                                                                                       |
| <span data-ttu-id="041ed-185">預設值</span><span class="sxs-lookup"><span data-stu-id="041ed-185">Default</span></span>        | <span data-ttu-id="041ed-186">N/A</span><span class="sxs-lookup"><span data-stu-id="041ed-186">N/A</span></span>                                                                                          |
| <span data-ttu-id="041ed-187">最小系統</span><span class="sxs-lookup"><span data-stu-id="041ed-187">Minimum system</span></span> | <span data-ttu-id="041ed-188">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="041ed-188">Windows 2000</span></span>                                                                                 |



 

### <a name="filtercriteria"></a><span data-ttu-id="041ed-189">>filtercriteria</span><span class="sxs-lookup"><span data-stu-id="041ed-189">FilterCriteria</span></span>



| <span data-ttu-id="041ed-190">進入</span><span class="sxs-lookup"><span data-stu-id="041ed-190">Entry</span></span> | <span data-ttu-id="041ed-191">值</span><span class="sxs-lookup"><span data-stu-id="041ed-191">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="041ed-192">描述</span><span class="sxs-lookup"><span data-stu-id="041ed-192">Description</span></span>    | <span data-ttu-id="041ed-193">指出篩選準則的字串。</span><span class="sxs-lookup"><span data-stu-id="041ed-193">A string indicating the filter criteria.</span></span> <span data-ttu-id="041ed-194">可以是 [**PublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) 類別的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="041ed-194">Can be a CLSID for a [**PublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) class.</span></span> |
| <span data-ttu-id="041ed-195">Access</span><span class="sxs-lookup"><span data-stu-id="041ed-195">Access</span></span>         | <span data-ttu-id="041ed-196">讀寫</span><span class="sxs-lookup"><span data-stu-id="041ed-196">ReadWrite</span></span>                                                                                                        |
| <span data-ttu-id="041ed-197">類型</span><span class="sxs-lookup"><span data-stu-id="041ed-197">Type</span></span>           | <span data-ttu-id="041ed-198">String</span><span class="sxs-lookup"><span data-stu-id="041ed-198">String</span></span>                                                                                                           |
| <span data-ttu-id="041ed-199">預設值</span><span class="sxs-lookup"><span data-stu-id="041ed-199">Default</span></span>        | <span data-ttu-id="041ed-200">N/A</span><span class="sxs-lookup"><span data-stu-id="041ed-200">N/A</span></span>                                                                                                              |
| <span data-ttu-id="041ed-201">最小系統</span><span class="sxs-lookup"><span data-stu-id="041ed-201">Minimum system</span></span> | <span data-ttu-id="041ed-202">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="041ed-202">Windows 2000</span></span>                                                                                                     |



 

### <a name="id"></a><span data-ttu-id="041ed-203">識別碼</span><span class="sxs-lookup"><span data-stu-id="041ed-203">ID</span></span>



| <span data-ttu-id="041ed-204">進入</span><span class="sxs-lookup"><span data-stu-id="041ed-204">Entry</span></span> | <span data-ttu-id="041ed-205">值</span><span class="sxs-lookup"><span data-stu-id="041ed-205">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="041ed-206">描述</span><span class="sxs-lookup"><span data-stu-id="041ed-206">Description</span></span>    | <span data-ttu-id="041ed-207">訂用帳戶的識別碼。</span><span class="sxs-lookup"><span data-stu-id="041ed-207">Identifier for the subscription.</span></span> <span data-ttu-id="041ed-208">當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="041ed-208">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="041ed-209">Access</span><span class="sxs-lookup"><span data-stu-id="041ed-209">Access</span></span>         | <span data-ttu-id="041ed-210">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="041ed-210">WriteOnce</span></span>                                                                                                                                                        |
| <span data-ttu-id="041ed-211">類型</span><span class="sxs-lookup"><span data-stu-id="041ed-211">Type</span></span>           | <span data-ttu-id="041ed-212">String</span><span class="sxs-lookup"><span data-stu-id="041ed-212">String</span></span>                                                                                                                                                           |
| <span data-ttu-id="041ed-213">預設值</span><span class="sxs-lookup"><span data-stu-id="041ed-213">Default</span></span>        | <Generated>                                                                                                                                                |
| <span data-ttu-id="041ed-214">最小系統</span><span class="sxs-lookup"><span data-stu-id="041ed-214">Minimum system</span></span> | <span data-ttu-id="041ed-215">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="041ed-215">Windows 2000</span></span>                                                                                                                                                     |



 

### <a name="interfaceid"></a><span data-ttu-id="041ed-216">InterfaceID</span><span class="sxs-lookup"><span data-stu-id="041ed-216">InterfaceID</span></span>



| <span data-ttu-id="041ed-217">進入</span><span class="sxs-lookup"><span data-stu-id="041ed-217">Entry</span></span> | <span data-ttu-id="041ed-218">值</span><span class="sxs-lookup"><span data-stu-id="041ed-218">Value</span></span> |
|----------------|------------------------------------------|
| <span data-ttu-id="041ed-219">描述</span><span class="sxs-lookup"><span data-stu-id="041ed-219">Description</span></span>    | <span data-ttu-id="041ed-220">已訂閱之介面的 IID。</span><span class="sxs-lookup"><span data-stu-id="041ed-220">The IID for the interface subscribed to.</span></span> |
| <span data-ttu-id="041ed-221">Access</span><span class="sxs-lookup"><span data-stu-id="041ed-221">Access</span></span>         | <span data-ttu-id="041ed-222">讀寫</span><span class="sxs-lookup"><span data-stu-id="041ed-222">ReadWrite</span></span>                                |
| <span data-ttu-id="041ed-223">類型</span><span class="sxs-lookup"><span data-stu-id="041ed-223">Type</span></span>           | <span data-ttu-id="041ed-224">String</span><span class="sxs-lookup"><span data-stu-id="041ed-224">String</span></span>                                   |
| <span data-ttu-id="041ed-225">預設值</span><span class="sxs-lookup"><span data-stu-id="041ed-225">Default</span></span>        | <span data-ttu-id="041ed-226">N/A</span><span class="sxs-lookup"><span data-stu-id="041ed-226">N/A</span></span>                                      |
| <span data-ttu-id="041ed-227">最小系統</span><span class="sxs-lookup"><span data-stu-id="041ed-227">Minimum system</span></span> | <span data-ttu-id="041ed-228">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="041ed-228">Windows 2000</span></span>                             |



 

### <a name="machinename"></a><span data-ttu-id="041ed-229">MachineName</span><span class="sxs-lookup"><span data-stu-id="041ed-229">MachineName</span></span>



| <span data-ttu-id="041ed-230">進入</span><span class="sxs-lookup"><span data-stu-id="041ed-230">Entry</span></span> | <span data-ttu-id="041ed-231">值</span><span class="sxs-lookup"><span data-stu-id="041ed-231">Value</span></span> |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="041ed-232">描述</span><span class="sxs-lookup"><span data-stu-id="041ed-232">Description</span></span>    | <span data-ttu-id="041ed-233">遠端電腦上的事件類別訂閱的遠端電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="041ed-233">A remote computer name for subscriptions to event classes on a remote computer.</span></span> |
| <span data-ttu-id="041ed-234">Access</span><span class="sxs-lookup"><span data-stu-id="041ed-234">Access</span></span>         | <span data-ttu-id="041ed-235">讀寫</span><span class="sxs-lookup"><span data-stu-id="041ed-235">ReadWrite</span></span>                                                                       |
| <span data-ttu-id="041ed-236">類型</span><span class="sxs-lookup"><span data-stu-id="041ed-236">Type</span></span>           | <span data-ttu-id="041ed-237">String</span><span class="sxs-lookup"><span data-stu-id="041ed-237">String</span></span>                                                                          |
| <span data-ttu-id="041ed-238">預設值</span><span class="sxs-lookup"><span data-stu-id="041ed-238">Default</span></span>        | <span data-ttu-id="041ed-239">""</span><span class="sxs-lookup"><span data-stu-id="041ed-239">""</span></span>                                                                              |
| <span data-ttu-id="041ed-240">最小系統</span><span class="sxs-lookup"><span data-stu-id="041ed-240">Minimum system</span></span> | <span data-ttu-id="041ed-241">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="041ed-241">Windows 2000</span></span>                                                                    |



 

### <a name="methodname"></a><span data-ttu-id="041ed-242">MethodName</span><span class="sxs-lookup"><span data-stu-id="041ed-242">MethodName</span></span>



| <span data-ttu-id="041ed-243">進入</span><span class="sxs-lookup"><span data-stu-id="041ed-243">Entry</span></span> | <span data-ttu-id="041ed-244">值</span><span class="sxs-lookup"><span data-stu-id="041ed-244">Value</span></span> |
|----------------|----------------------------------------------|
| <span data-ttu-id="041ed-245">描述</span><span class="sxs-lookup"><span data-stu-id="041ed-245">Description</span></span>    | <span data-ttu-id="041ed-246">要在其上訂閱的介面上的方法。</span><span class="sxs-lookup"><span data-stu-id="041ed-246">Method on the interface being subscribed to.</span></span> |
| <span data-ttu-id="041ed-247">Access</span><span class="sxs-lookup"><span data-stu-id="041ed-247">Access</span></span>         | <span data-ttu-id="041ed-248">讀寫</span><span class="sxs-lookup"><span data-stu-id="041ed-248">ReadWrite</span></span>                                    |
| <span data-ttu-id="041ed-249">類型</span><span class="sxs-lookup"><span data-stu-id="041ed-249">Type</span></span>           | <span data-ttu-id="041ed-250">String</span><span class="sxs-lookup"><span data-stu-id="041ed-250">String</span></span>                                       |
| <span data-ttu-id="041ed-251">預設值</span><span class="sxs-lookup"><span data-stu-id="041ed-251">Default</span></span>        | <span data-ttu-id="041ed-252">N/A</span><span class="sxs-lookup"><span data-stu-id="041ed-252">N/A</span></span>                                          |
| <span data-ttu-id="041ed-253">最小系統</span><span class="sxs-lookup"><span data-stu-id="041ed-253">Minimum system</span></span> | <span data-ttu-id="041ed-254">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="041ed-254">Windows 2000</span></span>                                 |



 

### <a name="name"></a><span data-ttu-id="041ed-255">Name</span><span class="sxs-lookup"><span data-stu-id="041ed-255">Name</span></span>



| <span data-ttu-id="041ed-256">進入</span><span class="sxs-lookup"><span data-stu-id="041ed-256">Entry</span></span> | <span data-ttu-id="041ed-257">值</span><span class="sxs-lookup"><span data-stu-id="041ed-257">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="041ed-258">描述</span><span class="sxs-lookup"><span data-stu-id="041ed-258">Description</span></span>    | <span data-ttu-id="041ed-259">訂用帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="041ed-259">Name for the subscription.</span></span> <span data-ttu-id="041ed-260">移除字串開頭和結尾的額外空間。在這個集合的物件上呼叫 [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="041ed-260">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="041ed-261">Access</span><span class="sxs-lookup"><span data-stu-id="041ed-261">Access</span></span>         | <span data-ttu-id="041ed-262">讀寫</span><span class="sxs-lookup"><span data-stu-id="041ed-262">ReadWrite</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="041ed-263">類型</span><span class="sxs-lookup"><span data-stu-id="041ed-263">Type</span></span>           | <span data-ttu-id="041ed-264">String</span><span class="sxs-lookup"><span data-stu-id="041ed-264">String</span></span>                                                                                                                                                                                                                             |
| <span data-ttu-id="041ed-265">預設值</span><span class="sxs-lookup"><span data-stu-id="041ed-265">Default</span></span>        | <span data-ttu-id="041ed-266">[新增訂用帳戶]</span><span class="sxs-lookup"><span data-stu-id="041ed-266">"New Subscription"</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="041ed-267">最小系統</span><span class="sxs-lookup"><span data-stu-id="041ed-267">Minimum system</span></span> | <span data-ttu-id="041ed-268">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="041ed-268">Windows 2000</span></span>                                                                                                                                                                                                                       |



 

### <a name="peruser"></a><span data-ttu-id="041ed-269">PerUser</span><span class="sxs-lookup"><span data-stu-id="041ed-269">PerUser</span></span>



| <span data-ttu-id="041ed-270">進入</span><span class="sxs-lookup"><span data-stu-id="041ed-270">Entry</span></span> | <span data-ttu-id="041ed-271">值</span><span class="sxs-lookup"><span data-stu-id="041ed-271">Value</span></span> |
|----------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="041ed-272">描述</span><span class="sxs-lookup"><span data-stu-id="041ed-272">Description</span></span>    | <span data-ttu-id="041ed-273">指出訂用帳戶是否只適用于指定的使用者、使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="041ed-273">Indicates whether the subscription applies only for a given user, UserName.</span></span> |
| <span data-ttu-id="041ed-274">Access</span><span class="sxs-lookup"><span data-stu-id="041ed-274">Access</span></span>         | <span data-ttu-id="041ed-275">讀寫</span><span class="sxs-lookup"><span data-stu-id="041ed-275">ReadWrite</span></span>                                                                   |
| <span data-ttu-id="041ed-276">類型</span><span class="sxs-lookup"><span data-stu-id="041ed-276">Type</span></span>           | <span data-ttu-id="041ed-277">Bool</span><span class="sxs-lookup"><span data-stu-id="041ed-277">Bool</span></span>                                                                        |
| <span data-ttu-id="041ed-278">預設</span><span class="sxs-lookup"><span data-stu-id="041ed-278">Default</span></span>        | <span data-ttu-id="041ed-279">否</span><span class="sxs-lookup"><span data-stu-id="041ed-279">False</span></span>                                                                       |
| <span data-ttu-id="041ed-280">最小系統</span><span class="sxs-lookup"><span data-stu-id="041ed-280">Minimum system</span></span> | <span data-ttu-id="041ed-281">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="041ed-281">Windows 2000</span></span>                                                                |



 

### <a name="publisherid"></a><span data-ttu-id="041ed-282">PublisherID</span><span class="sxs-lookup"><span data-stu-id="041ed-282">PublisherID</span></span>



| <span data-ttu-id="041ed-283">進入</span><span class="sxs-lookup"><span data-stu-id="041ed-283">Entry</span></span> | <span data-ttu-id="041ed-284">值</span><span class="sxs-lookup"><span data-stu-id="041ed-284">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="041ed-285">描述</span><span class="sxs-lookup"><span data-stu-id="041ed-285">Description</span></span>    | <span data-ttu-id="041ed-286">發行者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="041ed-286">The ID for the publisher.</span></span> <span data-ttu-id="041ed-287">您可以指定 EventCLSID 或 PublisherID，但不能同時指定兩者。</span><span class="sxs-lookup"><span data-stu-id="041ed-287">You can indicate an EventCLSID or a PublisherID but not both.</span></span> |
| <span data-ttu-id="041ed-288">Access</span><span class="sxs-lookup"><span data-stu-id="041ed-288">Access</span></span>         | <span data-ttu-id="041ed-289">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="041ed-289">WriteOnce</span></span>                                                                               |
| <span data-ttu-id="041ed-290">類型</span><span class="sxs-lookup"><span data-stu-id="041ed-290">Type</span></span>           | <span data-ttu-id="041ed-291">String</span><span class="sxs-lookup"><span data-stu-id="041ed-291">String</span></span>                                                                                  |
| <span data-ttu-id="041ed-292">預設值</span><span class="sxs-lookup"><span data-stu-id="041ed-292">Default</span></span>        | <span data-ttu-id="041ed-293">""</span><span class="sxs-lookup"><span data-stu-id="041ed-293">""</span></span>                                                                                      |
| <span data-ttu-id="041ed-294">最小系統</span><span class="sxs-lookup"><span data-stu-id="041ed-294">Minimum system</span></span> | <span data-ttu-id="041ed-295">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="041ed-295">Windows 2000</span></span>                                                                            |



 

### <a name="queued"></a><span data-ttu-id="041ed-296">已排入佇列</span><span class="sxs-lookup"><span data-stu-id="041ed-296">Queued</span></span>



| <span data-ttu-id="041ed-297">進入</span><span class="sxs-lookup"><span data-stu-id="041ed-297">Entry</span></span> | <span data-ttu-id="041ed-298">值</span><span class="sxs-lookup"><span data-stu-id="041ed-298">Value</span></span> |
|----------------|-----------------------------------------------|
| <span data-ttu-id="041ed-299">描述</span><span class="sxs-lookup"><span data-stu-id="041ed-299">Description</span></span>    | <span data-ttu-id="041ed-300">指出訂閱是否已排入佇列。</span><span class="sxs-lookup"><span data-stu-id="041ed-300">Indicates whether the subscription is queued.</span></span> |
| <span data-ttu-id="041ed-301">Access</span><span class="sxs-lookup"><span data-stu-id="041ed-301">Access</span></span>         | <span data-ttu-id="041ed-302">讀寫</span><span class="sxs-lookup"><span data-stu-id="041ed-302">ReadWrite</span></span>                                     |
| <span data-ttu-id="041ed-303">類型</span><span class="sxs-lookup"><span data-stu-id="041ed-303">Type</span></span>           | <span data-ttu-id="041ed-304">Bool</span><span class="sxs-lookup"><span data-stu-id="041ed-304">Bool</span></span>                                          |
| <span data-ttu-id="041ed-305">預設</span><span class="sxs-lookup"><span data-stu-id="041ed-305">Default</span></span>        | <span data-ttu-id="041ed-306">否</span><span class="sxs-lookup"><span data-stu-id="041ed-306">False</span></span>                                         |
| <span data-ttu-id="041ed-307">最小系統</span><span class="sxs-lookup"><span data-stu-id="041ed-307">Minimum system</span></span> | <span data-ttu-id="041ed-308">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="041ed-308">Windows 2000</span></span>                                  |



 

### <a name="subscribermoniker"></a><span data-ttu-id="041ed-309">SubscriberMoniker</span><span class="sxs-lookup"><span data-stu-id="041ed-309">SubscriberMoniker</span></span>



| <span data-ttu-id="041ed-310">進入</span><span class="sxs-lookup"><span data-stu-id="041ed-310">Entry</span></span> | <span data-ttu-id="041ed-311">值</span><span class="sxs-lookup"><span data-stu-id="041ed-311">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="041ed-312">描述</span><span class="sxs-lookup"><span data-stu-id="041ed-312">Description</span></span>    | <span data-ttu-id="041ed-313">標示為已排入佇列的訂閱者的標記。</span><span class="sxs-lookup"><span data-stu-id="041ed-313">A moniker for a subscriber marked as Queued.</span></span> <span data-ttu-id="041ed-314">當佇列最初設定為 True 時，就會產生預設值。</span><span class="sxs-lookup"><span data-stu-id="041ed-314">A default value is generated when Queued is initially set to True.</span></span> |
| <span data-ttu-id="041ed-315">Access</span><span class="sxs-lookup"><span data-stu-id="041ed-315">Access</span></span>         | <span data-ttu-id="041ed-316">讀寫</span><span class="sxs-lookup"><span data-stu-id="041ed-316">ReadWrite</span></span>                                                                                                       |
| <span data-ttu-id="041ed-317">類型</span><span class="sxs-lookup"><span data-stu-id="041ed-317">Type</span></span>           | <span data-ttu-id="041ed-318">String</span><span class="sxs-lookup"><span data-stu-id="041ed-318">String</span></span>                                                                                                          |
| <span data-ttu-id="041ed-319">預設值</span><span class="sxs-lookup"><span data-stu-id="041ed-319">Default</span></span>        | <span data-ttu-id="041ed-320">N/A</span><span class="sxs-lookup"><span data-stu-id="041ed-320">N/A</span></span>                                                                                                             |
| <span data-ttu-id="041ed-321">最小系統</span><span class="sxs-lookup"><span data-stu-id="041ed-321">Minimum system</span></span> | <span data-ttu-id="041ed-322">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="041ed-322">Windows 2000</span></span>                                                                                                    |



 

### <a name="subscriberpartitionid"></a><span data-ttu-id="041ed-323">SubscriberPartitionID</span><span class="sxs-lookup"><span data-stu-id="041ed-323">SubscriberPartitionID</span></span>



| <span data-ttu-id="041ed-324">進入</span><span class="sxs-lookup"><span data-stu-id="041ed-324">Entry</span></span> | <span data-ttu-id="041ed-325">值</span><span class="sxs-lookup"><span data-stu-id="041ed-325">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="041ed-326">描述</span><span class="sxs-lookup"><span data-stu-id="041ed-326">Description</span></span>    | <span data-ttu-id="041ed-327">訂閱相同資料分割中的事件類別時，用來代表訂閱者之資料分割識別碼的 GUID。</span><span class="sxs-lookup"><span data-stu-id="041ed-327">When subscribing to an event class in the same partition, used to represent the GUID of the partition ID of the subscriber.</span></span> <span data-ttu-id="041ed-328">訂閱事件類別時，訂閱者可以選擇訂閱相同或不同資料分割中的事件類別。</span><span class="sxs-lookup"><span data-stu-id="041ed-328">When subscribing to event classes, the subscriber has the option to subscribe to an event class in the same or different partition.</span></span> |
| <span data-ttu-id="041ed-329">Access</span><span class="sxs-lookup"><span data-stu-id="041ed-329">Access</span></span>         | <span data-ttu-id="041ed-330">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="041ed-330">WriteOnce</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="041ed-331">類型</span><span class="sxs-lookup"><span data-stu-id="041ed-331">Type</span></span>           | <span data-ttu-id="041ed-332">String</span><span class="sxs-lookup"><span data-stu-id="041ed-332">String</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="041ed-333">預設值</span><span class="sxs-lookup"><span data-stu-id="041ed-333">Default</span></span>        | <Generated>                                                                                                                                                                                                                                               |
| <span data-ttu-id="041ed-334">最小系統</span><span class="sxs-lookup"><span data-stu-id="041ed-334">Minimum system</span></span> | <span data-ttu-id="041ed-335">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="041ed-335">Windows Server 2003</span></span>                                                                                                                                                                                                                                             |



 

### <a name="username"></a><span data-ttu-id="041ed-336">UserName</span><span class="sxs-lookup"><span data-stu-id="041ed-336">UserName</span></span>



| <span data-ttu-id="041ed-337">進入</span><span class="sxs-lookup"><span data-stu-id="041ed-337">Entry</span></span> | <span data-ttu-id="041ed-338">值</span><span class="sxs-lookup"><span data-stu-id="041ed-338">Value</span></span> |
|----------------|--------------------------------------------------------------------------|
| <span data-ttu-id="041ed-339">描述</span><span class="sxs-lookup"><span data-stu-id="041ed-339">Description</span></span>    | <span data-ttu-id="041ed-340">當 PerUser 為 True 時，套用訂用帳戶的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="041ed-340">The name of user that the subscription applies to, when PerUser is True.</span></span> |
| <span data-ttu-id="041ed-341">Access</span><span class="sxs-lookup"><span data-stu-id="041ed-341">Access</span></span>         | <span data-ttu-id="041ed-342">讀寫</span><span class="sxs-lookup"><span data-stu-id="041ed-342">ReadWrite</span></span>                                                                |
| <span data-ttu-id="041ed-343">類型</span><span class="sxs-lookup"><span data-stu-id="041ed-343">Type</span></span>           | <span data-ttu-id="041ed-344">String</span><span class="sxs-lookup"><span data-stu-id="041ed-344">String</span></span>                                                                   |
| <span data-ttu-id="041ed-345">預設值</span><span class="sxs-lookup"><span data-stu-id="041ed-345">Default</span></span>        | <span data-ttu-id="041ed-346">N/A</span><span class="sxs-lookup"><span data-stu-id="041ed-346">N/A</span></span>                                                                      |
| <span data-ttu-id="041ed-347">最小系統</span><span class="sxs-lookup"><span data-stu-id="041ed-347">Minimum system</span></span> | <span data-ttu-id="041ed-348">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="041ed-348">Windows 2000</span></span>                                                             |



 

## <a name="see-also"></a><span data-ttu-id="041ed-349">另請參閱</span><span class="sxs-lookup"><span data-stu-id="041ed-349">See also</span></span>

<dl> <dt>

[<span data-ttu-id="041ed-350">COM + 系統管理集合</span><span class="sxs-lookup"><span data-stu-id="041ed-350">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 

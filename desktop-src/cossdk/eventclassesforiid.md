---
description: 捕獲事件類別的相關資訊。
ms.assetid: 33a87692-cacf-4a1c-974e-8d0e20295333
title: EventClassesForIID 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventClassesForIID
api_type:
- COM
api_location: ''
ms.openlocfilehash: 635ff6e87d68bfdcb4e82a24673c4ced00a7f81d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110560"
---
# <a name="eventclassesforiid-collection"></a><span data-ttu-id="4a65a-103">EventClassesForIID 集合</span><span class="sxs-lookup"><span data-stu-id="4a65a-103">EventClassesForIID collection</span></span>

<span data-ttu-id="4a65a-104">捕獲事件類別的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4a65a-104">Retrieves information regarding event classes.</span></span>

<span data-ttu-id="4a65a-105">「發行者」與「訂閱者」 (s) 之間的連接，是由 [**EventClass**](/windows/desktop/api/eventsys/nn-eventsys-ieventclass) 物件管理，它是一個 com + 元件，其中包含發行者用來引發事件的介面和方法。</span><span class="sxs-lookup"><span data-stu-id="4a65a-105">The connection between publisher and subscriber(s) is managed by an [**EventClass**](/windows/desktop/api/eventsys/nn-eventsys-ieventclass) object, which is a COM+ component that contains the interfaces and methods used by a publisher to fire events.</span></span>

<span data-ttu-id="4a65a-106">此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**加入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**移除**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。</span><span class="sxs-lookup"><span data-stu-id="4a65a-106">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="4a65a-107">成員</span><span class="sxs-lookup"><span data-stu-id="4a65a-107">Members</span></span>

<span data-ttu-id="4a65a-108">**EventClassesForIID** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。</span><span class="sxs-lookup"><span data-stu-id="4a65a-108">The **EventClassesForIID** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="4a65a-109">相關集合</span><span class="sxs-lookup"><span data-stu-id="4a65a-109">Related Collections</span></span>

<span data-ttu-id="4a65a-110">您可以從這個集合流覽至下列任何集合：</span><span class="sxs-lookup"><span data-stu-id="4a65a-110">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="4a65a-111">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="4a65a-111">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="4a65a-112">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="4a65a-112">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="4a65a-113">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="4a65a-113">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="4a65a-114">您可以從下列集合流覽至這個集合：</span><span class="sxs-lookup"><span data-stu-id="4a65a-114">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="4a65a-115">**根**</span><span class="sxs-lookup"><span data-stu-id="4a65a-115">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="4a65a-116">屬性</span><span class="sxs-lookup"><span data-stu-id="4a65a-116">Properties</span></span>

<span data-ttu-id="4a65a-117">集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="4a65a-117">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="4a65a-118">應用程式</span><span class="sxs-lookup"><span data-stu-id="4a65a-118">Application</span></span>](#application)
-   [<span data-ttu-id="4a65a-119">位元</span><span class="sxs-lookup"><span data-stu-id="4a65a-119">Bitness</span></span>](#bitness)
-   [<span data-ttu-id="4a65a-120">Clsid</span><span class="sxs-lookup"><span data-stu-id="4a65a-120">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="4a65a-121">說明</span><span class="sxs-lookup"><span data-stu-id="4a65a-121">Description</span></span>](#description)
-   [<span data-ttu-id="4a65a-122">IsPrivateComponent</span><span class="sxs-lookup"><span data-stu-id="4a65a-122">IsPrivateComponent</span></span>](#isprivatecomponent)
-   [<span data-ttu-id="4a65a-123">ProgID</span><span class="sxs-lookup"><span data-stu-id="4a65a-123">ProgID</span></span>](#progid)

### <a name="application"></a><span data-ttu-id="4a65a-124">應用程式</span><span class="sxs-lookup"><span data-stu-id="4a65a-124">Application</span></span>



| <span data-ttu-id="4a65a-125">進入</span><span class="sxs-lookup"><span data-stu-id="4a65a-125">Entry</span></span> | <span data-ttu-id="4a65a-126">值</span><span class="sxs-lookup"><span data-stu-id="4a65a-126">Value</span></span> |
|----------------|----------------------------------------------------------|
| <span data-ttu-id="4a65a-127">描述</span><span class="sxs-lookup"><span data-stu-id="4a65a-127">Description</span></span>    | <span data-ttu-id="4a65a-128">包含事件類別的應用程式 GUID。</span><span class="sxs-lookup"><span data-stu-id="4a65a-128">The GUID for the application containing the event class.</span></span> |
| <span data-ttu-id="4a65a-129">Access</span><span class="sxs-lookup"><span data-stu-id="4a65a-129">Access</span></span>         | <span data-ttu-id="4a65a-130">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="4a65a-130">ReadOnly</span></span>                                                 |
| <span data-ttu-id="4a65a-131">類型</span><span class="sxs-lookup"><span data-stu-id="4a65a-131">Type</span></span>           | <span data-ttu-id="4a65a-132">String</span><span class="sxs-lookup"><span data-stu-id="4a65a-132">String</span></span>                                                   |
| <span data-ttu-id="4a65a-133">預設值</span><span class="sxs-lookup"><span data-stu-id="4a65a-133">Default</span></span>        | <span data-ttu-id="4a65a-134">N/A</span><span class="sxs-lookup"><span data-stu-id="4a65a-134">N/A</span></span>                                                      |
| <span data-ttu-id="4a65a-135">最小系統</span><span class="sxs-lookup"><span data-stu-id="4a65a-135">Minimum system</span></span> | <span data-ttu-id="4a65a-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4a65a-136">Windows XP</span></span>                                               |



 

### <a name="bitness"></a><span data-ttu-id="4a65a-137">位元</span><span class="sxs-lookup"><span data-stu-id="4a65a-137">Bitness</span></span>



| <span data-ttu-id="4a65a-138">進入</span><span class="sxs-lookup"><span data-stu-id="4a65a-138">Entry</span></span> | <span data-ttu-id="4a65a-139">值</span><span class="sxs-lookup"><span data-stu-id="4a65a-139">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a65a-140">描述</span><span class="sxs-lookup"><span data-stu-id="4a65a-140">Description</span></span>    | <span data-ttu-id="4a65a-141">表示事件類別的二進位位數類型。</span><span class="sxs-lookup"><span data-stu-id="4a65a-141">Represents the binary bitness type of the event class.</span></span> <span data-ttu-id="4a65a-142">在使用64位 Windows 的系統上，這個屬性會區分64位元件與32位元件。</span><span class="sxs-lookup"><span data-stu-id="4a65a-142">On systems that use 64-bit Windows, this property distinguishes between 64-bit components and 32-bit components.</span></span> |
| <span data-ttu-id="4a65a-143">Access</span><span class="sxs-lookup"><span data-stu-id="4a65a-143">Access</span></span>         | <span data-ttu-id="4a65a-144">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="4a65a-144">ReadOnly</span></span>                                                                                                                                                                |
| <span data-ttu-id="4a65a-145">類型</span><span class="sxs-lookup"><span data-stu-id="4a65a-145">Type</span></span>           | <span data-ttu-id="4a65a-146">很長可能的值： COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0x2) </span><span class="sxs-lookup"><span data-stu-id="4a65a-146">Long Possible values:COMAdmin32BitComponent (0x1)COMAdmin64BitComponent (0x2)</span></span>                                                                                           |
| <span data-ttu-id="4a65a-147">預設</span><span class="sxs-lookup"><span data-stu-id="4a65a-147">Default</span></span>        | <span data-ttu-id="4a65a-148">N/A</span><span class="sxs-lookup"><span data-stu-id="4a65a-148">N/A</span></span>                                                                                                                                                                     |
| <span data-ttu-id="4a65a-149">最小系統</span><span class="sxs-lookup"><span data-stu-id="4a65a-149">Minimum system</span></span> | <span data-ttu-id="4a65a-150">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4a65a-150">Windows XP</span></span>                                                                                                                                                              |



 

### <a name="clsid"></a><span data-ttu-id="4a65a-151">CLSID</span><span class="sxs-lookup"><span data-stu-id="4a65a-151">CLSID</span></span>



| <span data-ttu-id="4a65a-152">進入</span><span class="sxs-lookup"><span data-stu-id="4a65a-152">Entry</span></span> | <span data-ttu-id="4a65a-153">值</span><span class="sxs-lookup"><span data-stu-id="4a65a-153">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a65a-154">描述</span><span class="sxs-lookup"><span data-stu-id="4a65a-154">Description</span></span>    | <span data-ttu-id="4a65a-155">事件類別的 GUID。</span><span class="sxs-lookup"><span data-stu-id="4a65a-155">The GUID for the event class.</span></span> <span data-ttu-id="4a65a-156">當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="4a65a-156">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="4a65a-157">Access</span><span class="sxs-lookup"><span data-stu-id="4a65a-157">Access</span></span>         | <span data-ttu-id="4a65a-158">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="4a65a-158">ReadOnly</span></span>                                                                                                                                                      |
| <span data-ttu-id="4a65a-159">類型</span><span class="sxs-lookup"><span data-stu-id="4a65a-159">Type</span></span>           | <span data-ttu-id="4a65a-160">String</span><span class="sxs-lookup"><span data-stu-id="4a65a-160">String</span></span>                                                                                                                                                        |
| <span data-ttu-id="4a65a-161">預設值</span><span class="sxs-lookup"><span data-stu-id="4a65a-161">Default</span></span>        | <span data-ttu-id="4a65a-162">N/A</span><span class="sxs-lookup"><span data-stu-id="4a65a-162">N/A</span></span>                                                                                                                                                           |
| <span data-ttu-id="4a65a-163">最小系統</span><span class="sxs-lookup"><span data-stu-id="4a65a-163">Minimum system</span></span> | <span data-ttu-id="4a65a-164">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4a65a-164">Windows XP</span></span>                                                                                                                                                    |



 

### <a name="description"></a><span data-ttu-id="4a65a-165">Description</span><span class="sxs-lookup"><span data-stu-id="4a65a-165">Description</span></span>



| <span data-ttu-id="4a65a-166">進入</span><span class="sxs-lookup"><span data-stu-id="4a65a-166">Entry</span></span> | <span data-ttu-id="4a65a-167">值</span><span class="sxs-lookup"><span data-stu-id="4a65a-167">Value</span></span> |
|----------------|----------------------------|
| <span data-ttu-id="4a65a-168">描述</span><span class="sxs-lookup"><span data-stu-id="4a65a-168">Description</span></span>    | <span data-ttu-id="4a65a-169">描述事件類別。</span><span class="sxs-lookup"><span data-stu-id="4a65a-169">Describes the event class.</span></span> |
| <span data-ttu-id="4a65a-170">Access</span><span class="sxs-lookup"><span data-stu-id="4a65a-170">Access</span></span>         | <span data-ttu-id="4a65a-171">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="4a65a-171">ReadOnly</span></span>                   |
| <span data-ttu-id="4a65a-172">類型</span><span class="sxs-lookup"><span data-stu-id="4a65a-172">Type</span></span>           | <span data-ttu-id="4a65a-173">String</span><span class="sxs-lookup"><span data-stu-id="4a65a-173">String</span></span>                     |
| <span data-ttu-id="4a65a-174">預設值</span><span class="sxs-lookup"><span data-stu-id="4a65a-174">Default</span></span>        | <span data-ttu-id="4a65a-175">""</span><span class="sxs-lookup"><span data-stu-id="4a65a-175">""</span></span>                         |
| <span data-ttu-id="4a65a-176">最小系統</span><span class="sxs-lookup"><span data-stu-id="4a65a-176">Minimum system</span></span> | <span data-ttu-id="4a65a-177">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4a65a-177">Windows XP</span></span>                 |



 

### <a name="isprivatecomponent"></a><span data-ttu-id="4a65a-178">IsPrivateComponent</span><span class="sxs-lookup"><span data-stu-id="4a65a-178">IsPrivateComponent</span></span>



| <span data-ttu-id="4a65a-179">進入</span><span class="sxs-lookup"><span data-stu-id="4a65a-179">Entry</span></span> | <span data-ttu-id="4a65a-180">值</span><span class="sxs-lookup"><span data-stu-id="4a65a-180">Value</span></span> |
|----------------|---------------------------------------------------------|
| <span data-ttu-id="4a65a-181">描述</span><span class="sxs-lookup"><span data-stu-id="4a65a-181">Description</span></span>    | <span data-ttu-id="4a65a-182">指出事件類別元件是否為私用。</span><span class="sxs-lookup"><span data-stu-id="4a65a-182">Indicates whether the event class component is private.</span></span> |
| <span data-ttu-id="4a65a-183">Access</span><span class="sxs-lookup"><span data-stu-id="4a65a-183">Access</span></span>         | <span data-ttu-id="4a65a-184">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="4a65a-184">ReadOnly</span></span>                                                |
| <span data-ttu-id="4a65a-185">類型</span><span class="sxs-lookup"><span data-stu-id="4a65a-185">Type</span></span>           | <span data-ttu-id="4a65a-186">Bool</span><span class="sxs-lookup"><span data-stu-id="4a65a-186">Bool</span></span>                                                    |
| <span data-ttu-id="4a65a-187">預設</span><span class="sxs-lookup"><span data-stu-id="4a65a-187">Default</span></span>        | <span data-ttu-id="4a65a-188">否</span><span class="sxs-lookup"><span data-stu-id="4a65a-188">False</span></span>                                                   |
| <span data-ttu-id="4a65a-189">最小系統</span><span class="sxs-lookup"><span data-stu-id="4a65a-189">Minimum system</span></span> | <span data-ttu-id="4a65a-190">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4a65a-190">Windows XP</span></span>                                              |



 

### <a name="progid"></a><span data-ttu-id="4a65a-191">ProgID</span><span class="sxs-lookup"><span data-stu-id="4a65a-191">ProgID</span></span>



| <span data-ttu-id="4a65a-192">進入</span><span class="sxs-lookup"><span data-stu-id="4a65a-192">Entry</span></span> | <span data-ttu-id="4a65a-193">值</span><span class="sxs-lookup"><span data-stu-id="4a65a-193">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a65a-194">描述</span><span class="sxs-lookup"><span data-stu-id="4a65a-194">Description</span></span>    | <span data-ttu-id="4a65a-195">用來識別事件類別的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="4a65a-195">A friendly name used to identify the event class.</span></span> <span data-ttu-id="4a65a-196">在這個集合的物件上呼叫 [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="4a65a-196">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="4a65a-197">Access</span><span class="sxs-lookup"><span data-stu-id="4a65a-197">Access</span></span>         | <span data-ttu-id="4a65a-198">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="4a65a-198">ReadOnly</span></span>                                                                                                                                                                            |
| <span data-ttu-id="4a65a-199">類型</span><span class="sxs-lookup"><span data-stu-id="4a65a-199">Type</span></span>           | <span data-ttu-id="4a65a-200">String</span><span class="sxs-lookup"><span data-stu-id="4a65a-200">String</span></span>                                                                                                                                                                              |
| <span data-ttu-id="4a65a-201">預設值</span><span class="sxs-lookup"><span data-stu-id="4a65a-201">Default</span></span>        | <span data-ttu-id="4a65a-202">""</span><span class="sxs-lookup"><span data-stu-id="4a65a-202">""</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="4a65a-203">最小系統</span><span class="sxs-lookup"><span data-stu-id="4a65a-203">Minimum system</span></span> | <span data-ttu-id="4a65a-204">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4a65a-204">Windows XP</span></span>                                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="4a65a-205">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4a65a-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a65a-206">COM + 系統管理集合</span><span class="sxs-lookup"><span data-stu-id="4a65a-206">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 

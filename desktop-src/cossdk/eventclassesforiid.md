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
# <a name="eventclassesforiid-collection"></a><span data-ttu-id="81893-103">EventClassesForIID 集合</span><span class="sxs-lookup"><span data-stu-id="81893-103">EventClassesForIID collection</span></span>

<span data-ttu-id="81893-104">捕獲事件類別的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="81893-104">Retrieves information regarding event classes.</span></span>

<span data-ttu-id="81893-105">「發行者」與「訂閱者」 (s) 之間的連接，是由 [**EventClass**](/windows/desktop/api/eventsys/nn-eventsys-ieventclass) 物件管理，它是一個 com + 元件，其中包含發行者用來引發事件的介面和方法。</span><span class="sxs-lookup"><span data-stu-id="81893-105">The connection between publisher and subscriber(s) is managed by an [**EventClass**](/windows/desktop/api/eventsys/nn-eventsys-ieventclass) object, which is a COM+ component that contains the interfaces and methods used by a publisher to fire events.</span></span>

<span data-ttu-id="81893-106">此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**加入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**移除**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。</span><span class="sxs-lookup"><span data-stu-id="81893-106">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="81893-107">成員</span><span class="sxs-lookup"><span data-stu-id="81893-107">Members</span></span>

<span data-ttu-id="81893-108">**EventClassesForIID** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。</span><span class="sxs-lookup"><span data-stu-id="81893-108">The **EventClassesForIID** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="81893-109">相關集合</span><span class="sxs-lookup"><span data-stu-id="81893-109">Related Collections</span></span>

<span data-ttu-id="81893-110">您可以從這個集合流覽至下列任何集合：</span><span class="sxs-lookup"><span data-stu-id="81893-110">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="81893-111">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="81893-111">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="81893-112">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="81893-112">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="81893-113">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="81893-113">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="81893-114">您可以從下列集合流覽至這個集合：</span><span class="sxs-lookup"><span data-stu-id="81893-114">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="81893-115">**根**</span><span class="sxs-lookup"><span data-stu-id="81893-115">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="81893-116">屬性</span><span class="sxs-lookup"><span data-stu-id="81893-116">Properties</span></span>

<span data-ttu-id="81893-117">集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="81893-117">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="81893-118">應用程式</span><span class="sxs-lookup"><span data-stu-id="81893-118">Application</span></span>](#application)
-   [<span data-ttu-id="81893-119">位元</span><span class="sxs-lookup"><span data-stu-id="81893-119">Bitness</span></span>](#bitness)
-   [<span data-ttu-id="81893-120">Clsid</span><span class="sxs-lookup"><span data-stu-id="81893-120">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="81893-121">說明</span><span class="sxs-lookup"><span data-stu-id="81893-121">Description</span></span>](#description)
-   [<span data-ttu-id="81893-122">IsPrivateComponent</span><span class="sxs-lookup"><span data-stu-id="81893-122">IsPrivateComponent</span></span>](#isprivatecomponent)
-   [<span data-ttu-id="81893-123">ProgID</span><span class="sxs-lookup"><span data-stu-id="81893-123">ProgID</span></span>](#progid)

### <a name="application"></a><span data-ttu-id="81893-124">應用程式</span><span class="sxs-lookup"><span data-stu-id="81893-124">Application</span></span>



| <span data-ttu-id="81893-125">進入</span><span class="sxs-lookup"><span data-stu-id="81893-125">Entry</span></span> | <span data-ttu-id="81893-126">值</span><span class="sxs-lookup"><span data-stu-id="81893-126">Value</span></span> |
|----------------|----------------------------------------------------------|
| <span data-ttu-id="81893-127">描述</span><span class="sxs-lookup"><span data-stu-id="81893-127">Description</span></span>    | <span data-ttu-id="81893-128">包含事件類別的應用程式 GUID。</span><span class="sxs-lookup"><span data-stu-id="81893-128">The GUID for the application containing the event class.</span></span> |
| <span data-ttu-id="81893-129">Access</span><span class="sxs-lookup"><span data-stu-id="81893-129">Access</span></span>         | <span data-ttu-id="81893-130">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="81893-130">ReadOnly</span></span>                                                 |
| <span data-ttu-id="81893-131">類型</span><span class="sxs-lookup"><span data-stu-id="81893-131">Type</span></span>           | <span data-ttu-id="81893-132">String</span><span class="sxs-lookup"><span data-stu-id="81893-132">String</span></span>                                                   |
| <span data-ttu-id="81893-133">預設值</span><span class="sxs-lookup"><span data-stu-id="81893-133">Default</span></span>        | <span data-ttu-id="81893-134">N/A</span><span class="sxs-lookup"><span data-stu-id="81893-134">N/A</span></span>                                                      |
| <span data-ttu-id="81893-135">最小系統</span><span class="sxs-lookup"><span data-stu-id="81893-135">Minimum system</span></span> | <span data-ttu-id="81893-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="81893-136">Windows XP</span></span>                                               |



 

### <a name="bitness"></a><span data-ttu-id="81893-137">位元</span><span class="sxs-lookup"><span data-stu-id="81893-137">Bitness</span></span>



| <span data-ttu-id="81893-138">進入</span><span class="sxs-lookup"><span data-stu-id="81893-138">Entry</span></span> | <span data-ttu-id="81893-139">值</span><span class="sxs-lookup"><span data-stu-id="81893-139">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81893-140">描述</span><span class="sxs-lookup"><span data-stu-id="81893-140">Description</span></span>    | <span data-ttu-id="81893-141">表示事件類別的二進位位數類型。</span><span class="sxs-lookup"><span data-stu-id="81893-141">Represents the binary bitness type of the event class.</span></span> <span data-ttu-id="81893-142">在使用64位 Windows 的系統上，這個屬性會區分64位元件與32位元件。</span><span class="sxs-lookup"><span data-stu-id="81893-142">On systems that use 64-bit Windows, this property distinguishes between 64-bit components and 32-bit components.</span></span> |
| <span data-ttu-id="81893-143">Access</span><span class="sxs-lookup"><span data-stu-id="81893-143">Access</span></span>         | <span data-ttu-id="81893-144">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="81893-144">ReadOnly</span></span>                                                                                                                                                                |
| <span data-ttu-id="81893-145">類型</span><span class="sxs-lookup"><span data-stu-id="81893-145">Type</span></span>           | <span data-ttu-id="81893-146">很長可能的值： COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0x2) </span><span class="sxs-lookup"><span data-stu-id="81893-146">Long Possible values:COMAdmin32BitComponent (0x1)COMAdmin64BitComponent (0x2)</span></span>                                                                                           |
| <span data-ttu-id="81893-147">預設</span><span class="sxs-lookup"><span data-stu-id="81893-147">Default</span></span>        | <span data-ttu-id="81893-148">N/A</span><span class="sxs-lookup"><span data-stu-id="81893-148">N/A</span></span>                                                                                                                                                                     |
| <span data-ttu-id="81893-149">最小系統</span><span class="sxs-lookup"><span data-stu-id="81893-149">Minimum system</span></span> | <span data-ttu-id="81893-150">Windows XP</span><span class="sxs-lookup"><span data-stu-id="81893-150">Windows XP</span></span>                                                                                                                                                              |



 

### <a name="clsid"></a><span data-ttu-id="81893-151">CLSID</span><span class="sxs-lookup"><span data-stu-id="81893-151">CLSID</span></span>



| <span data-ttu-id="81893-152">進入</span><span class="sxs-lookup"><span data-stu-id="81893-152">Entry</span></span> | <span data-ttu-id="81893-153">值</span><span class="sxs-lookup"><span data-stu-id="81893-153">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81893-154">描述</span><span class="sxs-lookup"><span data-stu-id="81893-154">Description</span></span>    | <span data-ttu-id="81893-155">事件類別的 GUID。</span><span class="sxs-lookup"><span data-stu-id="81893-155">The GUID for the event class.</span></span> <span data-ttu-id="81893-156">當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="81893-156">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="81893-157">Access</span><span class="sxs-lookup"><span data-stu-id="81893-157">Access</span></span>         | <span data-ttu-id="81893-158">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="81893-158">ReadOnly</span></span>                                                                                                                                                      |
| <span data-ttu-id="81893-159">類型</span><span class="sxs-lookup"><span data-stu-id="81893-159">Type</span></span>           | <span data-ttu-id="81893-160">String</span><span class="sxs-lookup"><span data-stu-id="81893-160">String</span></span>                                                                                                                                                        |
| <span data-ttu-id="81893-161">預設值</span><span class="sxs-lookup"><span data-stu-id="81893-161">Default</span></span>        | <span data-ttu-id="81893-162">N/A</span><span class="sxs-lookup"><span data-stu-id="81893-162">N/A</span></span>                                                                                                                                                           |
| <span data-ttu-id="81893-163">最小系統</span><span class="sxs-lookup"><span data-stu-id="81893-163">Minimum system</span></span> | <span data-ttu-id="81893-164">Windows XP</span><span class="sxs-lookup"><span data-stu-id="81893-164">Windows XP</span></span>                                                                                                                                                    |



 

### <a name="description"></a><span data-ttu-id="81893-165">Description</span><span class="sxs-lookup"><span data-stu-id="81893-165">Description</span></span>



| <span data-ttu-id="81893-166">進入</span><span class="sxs-lookup"><span data-stu-id="81893-166">Entry</span></span> | <span data-ttu-id="81893-167">值</span><span class="sxs-lookup"><span data-stu-id="81893-167">Value</span></span> |
|----------------|----------------------------|
| <span data-ttu-id="81893-168">描述</span><span class="sxs-lookup"><span data-stu-id="81893-168">Description</span></span>    | <span data-ttu-id="81893-169">描述事件類別。</span><span class="sxs-lookup"><span data-stu-id="81893-169">Describes the event class.</span></span> |
| <span data-ttu-id="81893-170">Access</span><span class="sxs-lookup"><span data-stu-id="81893-170">Access</span></span>         | <span data-ttu-id="81893-171">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="81893-171">ReadOnly</span></span>                   |
| <span data-ttu-id="81893-172">類型</span><span class="sxs-lookup"><span data-stu-id="81893-172">Type</span></span>           | <span data-ttu-id="81893-173">String</span><span class="sxs-lookup"><span data-stu-id="81893-173">String</span></span>                     |
| <span data-ttu-id="81893-174">預設值</span><span class="sxs-lookup"><span data-stu-id="81893-174">Default</span></span>        | <span data-ttu-id="81893-175">""</span><span class="sxs-lookup"><span data-stu-id="81893-175">""</span></span>                         |
| <span data-ttu-id="81893-176">最小系統</span><span class="sxs-lookup"><span data-stu-id="81893-176">Minimum system</span></span> | <span data-ttu-id="81893-177">Windows XP</span><span class="sxs-lookup"><span data-stu-id="81893-177">Windows XP</span></span>                 |



 

### <a name="isprivatecomponent"></a><span data-ttu-id="81893-178">IsPrivateComponent</span><span class="sxs-lookup"><span data-stu-id="81893-178">IsPrivateComponent</span></span>



| <span data-ttu-id="81893-179">進入</span><span class="sxs-lookup"><span data-stu-id="81893-179">Entry</span></span> | <span data-ttu-id="81893-180">值</span><span class="sxs-lookup"><span data-stu-id="81893-180">Value</span></span> |
|----------------|---------------------------------------------------------|
| <span data-ttu-id="81893-181">描述</span><span class="sxs-lookup"><span data-stu-id="81893-181">Description</span></span>    | <span data-ttu-id="81893-182">指出事件類別元件是否為私用。</span><span class="sxs-lookup"><span data-stu-id="81893-182">Indicates whether the event class component is private.</span></span> |
| <span data-ttu-id="81893-183">Access</span><span class="sxs-lookup"><span data-stu-id="81893-183">Access</span></span>         | <span data-ttu-id="81893-184">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="81893-184">ReadOnly</span></span>                                                |
| <span data-ttu-id="81893-185">類型</span><span class="sxs-lookup"><span data-stu-id="81893-185">Type</span></span>           | <span data-ttu-id="81893-186">Bool</span><span class="sxs-lookup"><span data-stu-id="81893-186">Bool</span></span>                                                    |
| <span data-ttu-id="81893-187">預設</span><span class="sxs-lookup"><span data-stu-id="81893-187">Default</span></span>        | <span data-ttu-id="81893-188">否</span><span class="sxs-lookup"><span data-stu-id="81893-188">False</span></span>                                                   |
| <span data-ttu-id="81893-189">最小系統</span><span class="sxs-lookup"><span data-stu-id="81893-189">Minimum system</span></span> | <span data-ttu-id="81893-190">Windows XP</span><span class="sxs-lookup"><span data-stu-id="81893-190">Windows XP</span></span>                                              |



 

### <a name="progid"></a><span data-ttu-id="81893-191">ProgID</span><span class="sxs-lookup"><span data-stu-id="81893-191">ProgID</span></span>



| <span data-ttu-id="81893-192">進入</span><span class="sxs-lookup"><span data-stu-id="81893-192">Entry</span></span> | <span data-ttu-id="81893-193">值</span><span class="sxs-lookup"><span data-stu-id="81893-193">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81893-194">描述</span><span class="sxs-lookup"><span data-stu-id="81893-194">Description</span></span>    | <span data-ttu-id="81893-195">用來識別事件類別的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="81893-195">A friendly name used to identify the event class.</span></span> <span data-ttu-id="81893-196">在這個集合的物件上呼叫 [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="81893-196">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="81893-197">Access</span><span class="sxs-lookup"><span data-stu-id="81893-197">Access</span></span>         | <span data-ttu-id="81893-198">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="81893-198">ReadOnly</span></span>                                                                                                                                                                            |
| <span data-ttu-id="81893-199">類型</span><span class="sxs-lookup"><span data-stu-id="81893-199">Type</span></span>           | <span data-ttu-id="81893-200">String</span><span class="sxs-lookup"><span data-stu-id="81893-200">String</span></span>                                                                                                                                                                              |
| <span data-ttu-id="81893-201">預設值</span><span class="sxs-lookup"><span data-stu-id="81893-201">Default</span></span>        | <span data-ttu-id="81893-202">""</span><span class="sxs-lookup"><span data-stu-id="81893-202">""</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="81893-203">最小系統</span><span class="sxs-lookup"><span data-stu-id="81893-203">Minimum system</span></span> | <span data-ttu-id="81893-204">Windows XP</span><span class="sxs-lookup"><span data-stu-id="81893-204">Windows XP</span></span>                                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="81893-205">另請參閱</span><span class="sxs-lookup"><span data-stu-id="81893-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81893-206">COM + 系統管理集合</span><span class="sxs-lookup"><span data-stu-id="81893-206">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 

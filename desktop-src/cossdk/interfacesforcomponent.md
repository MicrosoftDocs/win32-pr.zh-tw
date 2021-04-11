---
description: 針對集合所關聯的元件所公開的每個介面，各包含一個物件。
ms.assetid: ee755693-e3ff-4bb1-9fde-a2bfee9c3d29
title: InterfacesForComponent 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InterfacesForComponent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9450c898e694e5459dbb126d7f7bf11b853e33d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110909"
---
# <a name="interfacesforcomponent-collection"></a><span data-ttu-id="08702-103">InterfacesForComponent 集合</span><span class="sxs-lookup"><span data-stu-id="08702-103">InterfacesForComponent collection</span></span>

<span data-ttu-id="08702-104">針對集合所關聯的元件所公開的每個介面，各包含一個物件。</span><span class="sxs-lookup"><span data-stu-id="08702-104">Contains an object for each interface exposed by the component to which the collection is related.</span></span>

<span data-ttu-id="08702-105">此集合不支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。</span><span class="sxs-lookup"><span data-stu-id="08702-105">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="08702-106">成員</span><span class="sxs-lookup"><span data-stu-id="08702-106">Members</span></span>

<span data-ttu-id="08702-107">**InterfacesForComponent** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。</span><span class="sxs-lookup"><span data-stu-id="08702-107">The **InterfacesForComponent** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="08702-108">相關集合</span><span class="sxs-lookup"><span data-stu-id="08702-108">Related Collections</span></span>

<span data-ttu-id="08702-109">您可以從這個集合流覽至下列任何集合：</span><span class="sxs-lookup"><span data-stu-id="08702-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="08702-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="08702-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="08702-111">**MethodsForInterface**</span><span class="sxs-lookup"><span data-stu-id="08702-111">**MethodsForInterface**</span></span>](methodsforinterface.md)
-   [<span data-ttu-id="08702-112">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="08702-112">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="08702-113">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="08702-113">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="08702-114">**RolesForInterface**</span><span class="sxs-lookup"><span data-stu-id="08702-114">**RolesForInterface**</span></span>](rolesforinterface.md)

<span data-ttu-id="08702-115">您可以從下列集合流覽至這個集合：</span><span class="sxs-lookup"><span data-stu-id="08702-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="08702-116">**單元**</span><span class="sxs-lookup"><span data-stu-id="08702-116">**Components**</span></span>](components.md)

## <a name="properties"></a><span data-ttu-id="08702-117">屬性</span><span class="sxs-lookup"><span data-stu-id="08702-117">Properties</span></span>

<span data-ttu-id="08702-118">集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="08702-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="08702-119">Clsid</span><span class="sxs-lookup"><span data-stu-id="08702-119">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="08702-120">說明</span><span class="sxs-lookup"><span data-stu-id="08702-120">Description</span></span>](#description)
-   [<span data-ttu-id="08702-121">IID</span><span class="sxs-lookup"><span data-stu-id="08702-121">IID</span></span>](#iid)
-   [<span data-ttu-id="08702-122">名稱</span><span class="sxs-lookup"><span data-stu-id="08702-122">Name</span></span>](#name)
-   [<span data-ttu-id="08702-123">QueuingEnabled</span><span class="sxs-lookup"><span data-stu-id="08702-123">QueuingEnabled</span></span>](#queuingenabled)
-   [<span data-ttu-id="08702-124">QueueingSupported</span><span class="sxs-lookup"><span data-stu-id="08702-124">QueueingSupported</span></span>](#queueingsupported)

### <a name="clsid"></a><span data-ttu-id="08702-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="08702-125">CLSID</span></span>



| <span data-ttu-id="08702-126">進入</span><span class="sxs-lookup"><span data-stu-id="08702-126">Entry</span></span> | <span data-ttu-id="08702-127">值</span><span class="sxs-lookup"><span data-stu-id="08702-127">Value</span></span> |
|----------------|---------------------------|
| <span data-ttu-id="08702-128">描述</span><span class="sxs-lookup"><span data-stu-id="08702-128">Description</span></span>    | <span data-ttu-id="08702-129">元件的 GUID。</span><span class="sxs-lookup"><span data-stu-id="08702-129">A GUID for the component.</span></span> |
| <span data-ttu-id="08702-130">Access</span><span class="sxs-lookup"><span data-stu-id="08702-130">Access</span></span>         | <span data-ttu-id="08702-131">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="08702-131">ReadOnly</span></span>                  |
| <span data-ttu-id="08702-132">類型</span><span class="sxs-lookup"><span data-stu-id="08702-132">Type</span></span>           | <span data-ttu-id="08702-133">String</span><span class="sxs-lookup"><span data-stu-id="08702-133">String</span></span>                    |
| <span data-ttu-id="08702-134">預設值</span><span class="sxs-lookup"><span data-stu-id="08702-134">Default</span></span>        | <span data-ttu-id="08702-135">N/A</span><span class="sxs-lookup"><span data-stu-id="08702-135">N/A</span></span>                       |
| <span data-ttu-id="08702-136">最小系統</span><span class="sxs-lookup"><span data-stu-id="08702-136">Minimum system</span></span> | <span data-ttu-id="08702-137">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="08702-137">Windows 2000</span></span>              |



 

### <a name="description"></a><span data-ttu-id="08702-138">Description</span><span class="sxs-lookup"><span data-stu-id="08702-138">Description</span></span>



| <span data-ttu-id="08702-139">進入</span><span class="sxs-lookup"><span data-stu-id="08702-139">Entry</span></span> | <span data-ttu-id="08702-140">值</span><span class="sxs-lookup"><span data-stu-id="08702-140">Value</span></span> |
|----------------|----------------------------------|
| <span data-ttu-id="08702-141">描述</span><span class="sxs-lookup"><span data-stu-id="08702-141">Description</span></span>    | <span data-ttu-id="08702-142">介面的描述。</span><span class="sxs-lookup"><span data-stu-id="08702-142">A description for the interface.</span></span> |
| <span data-ttu-id="08702-143">Access</span><span class="sxs-lookup"><span data-stu-id="08702-143">Access</span></span>         | <span data-ttu-id="08702-144">讀寫</span><span class="sxs-lookup"><span data-stu-id="08702-144">ReadWrite</span></span>                        |
| <span data-ttu-id="08702-145">類型</span><span class="sxs-lookup"><span data-stu-id="08702-145">Type</span></span>           | <span data-ttu-id="08702-146">String</span><span class="sxs-lookup"><span data-stu-id="08702-146">String</span></span>                           |
| <span data-ttu-id="08702-147">預設值</span><span class="sxs-lookup"><span data-stu-id="08702-147">Default</span></span>        | <span data-ttu-id="08702-148">""</span><span class="sxs-lookup"><span data-stu-id="08702-148">""</span></span>                               |
| <span data-ttu-id="08702-149">最小系統</span><span class="sxs-lookup"><span data-stu-id="08702-149">Minimum system</span></span> | <span data-ttu-id="08702-150">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="08702-150">Windows 2000</span></span>                     |



 

### <a name="iid"></a><span data-ttu-id="08702-151">IID</span><span class="sxs-lookup"><span data-stu-id="08702-151">IID</span></span>



| <span data-ttu-id="08702-152">進入</span><span class="sxs-lookup"><span data-stu-id="08702-152">Entry</span></span> | <span data-ttu-id="08702-153">值</span><span class="sxs-lookup"><span data-stu-id="08702-153">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08702-154">描述</span><span class="sxs-lookup"><span data-stu-id="08702-154">Description</span></span>    | <span data-ttu-id="08702-155">介面的 GUID。</span><span class="sxs-lookup"><span data-stu-id="08702-155">A GUID for the interface.</span></span> <span data-ttu-id="08702-156">當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="08702-156">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="08702-157">Access</span><span class="sxs-lookup"><span data-stu-id="08702-157">Access</span></span>         | <span data-ttu-id="08702-158">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="08702-158">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="08702-159">類型</span><span class="sxs-lookup"><span data-stu-id="08702-159">Type</span></span>           | <span data-ttu-id="08702-160">String</span><span class="sxs-lookup"><span data-stu-id="08702-160">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="08702-161">預設值</span><span class="sxs-lookup"><span data-stu-id="08702-161">Default</span></span>        | <span data-ttu-id="08702-162">N/A</span><span class="sxs-lookup"><span data-stu-id="08702-162">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="08702-163">最小系統</span><span class="sxs-lookup"><span data-stu-id="08702-163">Minimum system</span></span> | <span data-ttu-id="08702-164">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="08702-164">Windows 2000</span></span>                                                                                                                                              |



 

### <a name="name"></a><span data-ttu-id="08702-165">Name</span><span class="sxs-lookup"><span data-stu-id="08702-165">Name</span></span>



| <span data-ttu-id="08702-166">進入</span><span class="sxs-lookup"><span data-stu-id="08702-166">Entry</span></span> | <span data-ttu-id="08702-167">值</span><span class="sxs-lookup"><span data-stu-id="08702-167">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08702-168">描述</span><span class="sxs-lookup"><span data-stu-id="08702-168">Description</span></span>    | <span data-ttu-id="08702-169">介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="08702-169">A name for the interface.</span></span> <span data-ttu-id="08702-170">在這個集合的物件上呼叫 [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="08702-170">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="08702-171">Access</span><span class="sxs-lookup"><span data-stu-id="08702-171">Access</span></span>         | <span data-ttu-id="08702-172">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="08702-172">ReadOnly</span></span>                                                                                                                                                    |
| <span data-ttu-id="08702-173">類型</span><span class="sxs-lookup"><span data-stu-id="08702-173">Type</span></span>           | <span data-ttu-id="08702-174">String</span><span class="sxs-lookup"><span data-stu-id="08702-174">String</span></span>                                                                                                                                                      |
| <span data-ttu-id="08702-175">預設值</span><span class="sxs-lookup"><span data-stu-id="08702-175">Default</span></span>        | <span data-ttu-id="08702-176">N/A</span><span class="sxs-lookup"><span data-stu-id="08702-176">N/A</span></span>                                                                                                                                                         |
| <span data-ttu-id="08702-177">最小系統</span><span class="sxs-lookup"><span data-stu-id="08702-177">Minimum system</span></span> | <span data-ttu-id="08702-178">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="08702-178">Windows 2000</span></span>                                                                                                                                                |



 

### <a name="queuingenabled"></a><span data-ttu-id="08702-179">QueuingEnabled</span><span class="sxs-lookup"><span data-stu-id="08702-179">QueuingEnabled</span></span>



| <span data-ttu-id="08702-180">進入</span><span class="sxs-lookup"><span data-stu-id="08702-180">Entry</span></span> | <span data-ttu-id="08702-181">值</span><span class="sxs-lookup"><span data-stu-id="08702-181">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08702-182">描述</span><span class="sxs-lookup"><span data-stu-id="08702-182">Description</span></span>    | <span data-ttu-id="08702-183">將介面標示為 queuable，而且可以使用管理 SDK 或元件服務系統管理工具來設定。</span><span class="sxs-lookup"><span data-stu-id="08702-183">Marks the interface as queuable and can be set by using the Admin SDK or Component Services administrative tool.</span></span> <span data-ttu-id="08702-184">不過，只有具有 **佇列支援** 旗標集的介面可以設定 **佇列啟用** 旗標。</span><span class="sxs-lookup"><span data-stu-id="08702-184">However, only an interface that has the **Queuing Supported** flag set can have the **Queuing Enabled** flag set.</span></span> |
| <span data-ttu-id="08702-185">Access</span><span class="sxs-lookup"><span data-stu-id="08702-185">Access</span></span>         | <span data-ttu-id="08702-186">讀寫</span><span class="sxs-lookup"><span data-stu-id="08702-186">ReadWrite</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="08702-187">類型</span><span class="sxs-lookup"><span data-stu-id="08702-187">Type</span></span>           | <span data-ttu-id="08702-188">Bool</span><span class="sxs-lookup"><span data-stu-id="08702-188">Bool</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="08702-189">預設</span><span class="sxs-lookup"><span data-stu-id="08702-189">Default</span></span>        | <span data-ttu-id="08702-190">否</span><span class="sxs-lookup"><span data-stu-id="08702-190">False</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="08702-191">最小系統</span><span class="sxs-lookup"><span data-stu-id="08702-191">Minimum system</span></span> | <span data-ttu-id="08702-192">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="08702-192">Windows 2000</span></span>                                                                                                                                                                                                                       |



 

### <a name="queueingsupported"></a><span data-ttu-id="08702-193">QueueingSupported</span><span class="sxs-lookup"><span data-stu-id="08702-193">QueueingSupported</span></span>



| <span data-ttu-id="08702-194">進入</span><span class="sxs-lookup"><span data-stu-id="08702-194">Entry</span></span> | <span data-ttu-id="08702-195">值</span><span class="sxs-lookup"><span data-stu-id="08702-195">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08702-196">描述</span><span class="sxs-lookup"><span data-stu-id="08702-196">Description</span></span>    | <span data-ttu-id="08702-197">介面支援佇列。</span><span class="sxs-lookup"><span data-stu-id="08702-197">Interface supports queuing.</span></span> <span data-ttu-id="08702-198">針對支援佇列的介面，所有方法都只能在參數中。</span><span class="sxs-lookup"><span data-stu-id="08702-198">For an interface to support queuing, all methods should have only in parameters.</span></span> <span data-ttu-id="08702-199">**支援的佇列** 會公開為唯讀屬性。</span><span class="sxs-lookup"><span data-stu-id="08702-199">**Queuing Supported** is exposed as a read-only property.</span></span> |
| <span data-ttu-id="08702-200">Access</span><span class="sxs-lookup"><span data-stu-id="08702-200">Access</span></span>         | <span data-ttu-id="08702-201">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="08702-201">ReadOnly</span></span>                                                                                                                                                               |
| <span data-ttu-id="08702-202">類型</span><span class="sxs-lookup"><span data-stu-id="08702-202">Type</span></span>           | <span data-ttu-id="08702-203">Bool</span><span class="sxs-lookup"><span data-stu-id="08702-203">Bool</span></span>                                                                                                                                                                   |
| <span data-ttu-id="08702-204">預設</span><span class="sxs-lookup"><span data-stu-id="08702-204">Default</span></span>        | <span data-ttu-id="08702-205">否</span><span class="sxs-lookup"><span data-stu-id="08702-205">False</span></span>                                                                                                                                                                  |
| <span data-ttu-id="08702-206">最小系統</span><span class="sxs-lookup"><span data-stu-id="08702-206">Minimum system</span></span> | <span data-ttu-id="08702-207">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="08702-207">Windows 2000</span></span>                                                                                                                                                           |



 

## <a name="see-also"></a><span data-ttu-id="08702-208">另請參閱</span><span class="sxs-lookup"><span data-stu-id="08702-208">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08702-209">COM + 系統管理集合</span><span class="sxs-lookup"><span data-stu-id="08702-209">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 

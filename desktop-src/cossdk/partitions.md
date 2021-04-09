---
description: 指定每個資料分割內包含的應用程式。
ms.assetid: 264a35fd-ba71-4ae9-908a-24a72167c26b
title: 分割區集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Partitions
api_type:
- COM
api_location: ''
ms.openlocfilehash: b1016ae932d6841a5db590f2d24496113d3cefc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689216"
---
# <a name="partitions-collection"></a><span data-ttu-id="b73ce-103">分割區集合</span><span class="sxs-lookup"><span data-stu-id="b73ce-103">Partitions collection</span></span>

<span data-ttu-id="b73ce-104">指定每個資料分割內包含的應用程式。</span><span class="sxs-lookup"><span data-stu-id="b73ce-104">Specifies the applications contained within each partition.</span></span>

<span data-ttu-id="b73ce-105">此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**加入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**移除**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。</span><span class="sxs-lookup"><span data-stu-id="b73ce-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="b73ce-106">成員</span><span class="sxs-lookup"><span data-stu-id="b73ce-106">Members</span></span>

<span data-ttu-id="b73ce-107">分割 **區集合繼承** 自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) 介面，但沒有其他成員。</span><span class="sxs-lookup"><span data-stu-id="b73ce-107">The **Partitions** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="b73ce-108">相關集合</span><span class="sxs-lookup"><span data-stu-id="b73ce-108">Related Collections</span></span>

<span data-ttu-id="b73ce-109">您可以從這個集合流覽至下列任何集合：</span><span class="sxs-lookup"><span data-stu-id="b73ce-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="b73ce-110">**應用程式**</span><span class="sxs-lookup"><span data-stu-id="b73ce-110">**Applications**</span></span>](applications.md)
-   [<span data-ttu-id="b73ce-111">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="b73ce-111">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="b73ce-112">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="b73ce-112">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="b73ce-113">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="b73ce-113">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="b73ce-114">**RolesForPartition**</span><span class="sxs-lookup"><span data-stu-id="b73ce-114">**RolesForPartition**</span></span>](rolesforpartition.md)

<span data-ttu-id="b73ce-115">您可以從下列集合流覽至這個集合：</span><span class="sxs-lookup"><span data-stu-id="b73ce-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="b73ce-116">**根**</span><span class="sxs-lookup"><span data-stu-id="b73ce-116">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="b73ce-117">屬性</span><span class="sxs-lookup"><span data-stu-id="b73ce-117">Properties</span></span>

<span data-ttu-id="b73ce-118">集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="b73ce-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="b73ce-119">多變</span><span class="sxs-lookup"><span data-stu-id="b73ce-119">Changeable</span></span>](#changeable)
-   [<span data-ttu-id="b73ce-120">刪除</span><span class="sxs-lookup"><span data-stu-id="b73ce-120">Deleteable</span></span>](#deleteable)
-   [<span data-ttu-id="b73ce-121">說明</span><span class="sxs-lookup"><span data-stu-id="b73ce-121">Description</span></span>](#description)
-   [<span data-ttu-id="b73ce-122">識別碼</span><span class="sxs-lookup"><span data-stu-id="b73ce-122">ID</span></span>](#partitions-collection)
-   [<span data-ttu-id="b73ce-123">名稱</span><span class="sxs-lookup"><span data-stu-id="b73ce-123">Name</span></span>](#name)

### <a name="changeable"></a><span data-ttu-id="b73ce-124">多變</span><span class="sxs-lookup"><span data-stu-id="b73ce-124">Changeable</span></span>



| <span data-ttu-id="b73ce-125">進入</span><span class="sxs-lookup"><span data-stu-id="b73ce-125">Entry</span></span> | <span data-ttu-id="b73ce-126">值</span><span class="sxs-lookup"><span data-stu-id="b73ce-126">Value</span></span> |
|----------------|--------------------------------------------------|
| <span data-ttu-id="b73ce-127">描述</span><span class="sxs-lookup"><span data-stu-id="b73ce-127">Description</span></span>    | <span data-ttu-id="b73ce-128">判斷此分割區是否可變更。</span><span class="sxs-lookup"><span data-stu-id="b73ce-128">Determines whether this partition is changeable.</span></span> |
| <span data-ttu-id="b73ce-129">Access</span><span class="sxs-lookup"><span data-stu-id="b73ce-129">Access</span></span>         | <span data-ttu-id="b73ce-130">讀寫</span><span class="sxs-lookup"><span data-stu-id="b73ce-130">ReadWrite</span></span>                                        |
| <span data-ttu-id="b73ce-131">類型</span><span class="sxs-lookup"><span data-stu-id="b73ce-131">Type</span></span>           | <span data-ttu-id="b73ce-132">Bool</span><span class="sxs-lookup"><span data-stu-id="b73ce-132">Bool</span></span>                                             |
| <span data-ttu-id="b73ce-133">預設</span><span class="sxs-lookup"><span data-stu-id="b73ce-133">Default</span></span>        | <span data-ttu-id="b73ce-134">對</span><span class="sxs-lookup"><span data-stu-id="b73ce-134">True</span></span>                                             |
| <span data-ttu-id="b73ce-135">最小系統</span><span class="sxs-lookup"><span data-stu-id="b73ce-135">Minimum system</span></span> | <span data-ttu-id="b73ce-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b73ce-136">Windows Server 2003</span></span>                              |



 

### <a name="deleteable"></a><span data-ttu-id="b73ce-137">刪除</span><span class="sxs-lookup"><span data-stu-id="b73ce-137">Deleteable</span></span>



| <span data-ttu-id="b73ce-138">進入</span><span class="sxs-lookup"><span data-stu-id="b73ce-138">Entry</span></span> | <span data-ttu-id="b73ce-139">值</span><span class="sxs-lookup"><span data-stu-id="b73ce-139">Value</span></span> |
|----------------|---------------------------------------------------|
| <span data-ttu-id="b73ce-140">描述</span><span class="sxs-lookup"><span data-stu-id="b73ce-140">Description</span></span>    | <span data-ttu-id="b73ce-141">判斷此分割區是否可刪除。</span><span class="sxs-lookup"><span data-stu-id="b73ce-141">Determines whether this partition can be deleted.</span></span> |
| <span data-ttu-id="b73ce-142">Access</span><span class="sxs-lookup"><span data-stu-id="b73ce-142">Access</span></span>         | <span data-ttu-id="b73ce-143">讀寫</span><span class="sxs-lookup"><span data-stu-id="b73ce-143">ReadWrite</span></span>                                         |
| <span data-ttu-id="b73ce-144">類型</span><span class="sxs-lookup"><span data-stu-id="b73ce-144">Type</span></span>           | <span data-ttu-id="b73ce-145">Bool</span><span class="sxs-lookup"><span data-stu-id="b73ce-145">Bool</span></span>                                              |
| <span data-ttu-id="b73ce-146">預設</span><span class="sxs-lookup"><span data-stu-id="b73ce-146">Default</span></span>        | <span data-ttu-id="b73ce-147">對</span><span class="sxs-lookup"><span data-stu-id="b73ce-147">True</span></span>                                              |
| <span data-ttu-id="b73ce-148">最小系統</span><span class="sxs-lookup"><span data-stu-id="b73ce-148">Minimum system</span></span> | <span data-ttu-id="b73ce-149">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b73ce-149">Windows Server 2003</span></span>                               |



 

### <a name="description"></a><span data-ttu-id="b73ce-150">Description</span><span class="sxs-lookup"><span data-stu-id="b73ce-150">Description</span></span>



| <span data-ttu-id="b73ce-151">進入</span><span class="sxs-lookup"><span data-stu-id="b73ce-151">Entry</span></span> | <span data-ttu-id="b73ce-152">值</span><span class="sxs-lookup"><span data-stu-id="b73ce-152">Value</span></span> |
|----------------|---------------------------------------------------------------------|
| <span data-ttu-id="b73ce-153">描述</span><span class="sxs-lookup"><span data-stu-id="b73ce-153">Description</span></span>    | <span data-ttu-id="b73ce-154">這個屬性工作表示識別資料分割的描述。</span><span class="sxs-lookup"><span data-stu-id="b73ce-154">This property represents the description identifying the partition.</span></span> |
| <span data-ttu-id="b73ce-155">Access</span><span class="sxs-lookup"><span data-stu-id="b73ce-155">Access</span></span>         | <span data-ttu-id="b73ce-156">讀寫</span><span class="sxs-lookup"><span data-stu-id="b73ce-156">ReadWrite</span></span>                                                           |
| <span data-ttu-id="b73ce-157">類型</span><span class="sxs-lookup"><span data-stu-id="b73ce-157">Type</span></span>           | <span data-ttu-id="b73ce-158">String</span><span class="sxs-lookup"><span data-stu-id="b73ce-158">String</span></span>                                                              |
| <span data-ttu-id="b73ce-159">預設值</span><span class="sxs-lookup"><span data-stu-id="b73ce-159">Default</span></span>        | <span data-ttu-id="b73ce-160">""</span><span class="sxs-lookup"><span data-stu-id="b73ce-160">""</span></span>                                                                  |
| <span data-ttu-id="b73ce-161">最小系統</span><span class="sxs-lookup"><span data-stu-id="b73ce-161">Minimum system</span></span> | <span data-ttu-id="b73ce-162">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b73ce-162">Windows Server 2003</span></span>                                                 |



 

### <a name="id"></a><span data-ttu-id="b73ce-163">識別碼</span><span class="sxs-lookup"><span data-stu-id="b73ce-163">ID</span></span>



| <span data-ttu-id="b73ce-164">進入</span><span class="sxs-lookup"><span data-stu-id="b73ce-164">Entry</span></span> | <span data-ttu-id="b73ce-165">值</span><span class="sxs-lookup"><span data-stu-id="b73ce-165">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b73ce-166">描述</span><span class="sxs-lookup"><span data-stu-id="b73ce-166">Description</span></span>    | <span data-ttu-id="b73ce-167">表示資料分割的 GUID。</span><span class="sxs-lookup"><span data-stu-id="b73ce-167">A GUID representing the partition.</span></span> <span data-ttu-id="b73ce-168">當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="b73ce-168">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="b73ce-169">Access</span><span class="sxs-lookup"><span data-stu-id="b73ce-169">Access</span></span>         | <span data-ttu-id="b73ce-170">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="b73ce-170">WriteOnce</span></span>                                                                                                                                                          |
| <span data-ttu-id="b73ce-171">類型</span><span class="sxs-lookup"><span data-stu-id="b73ce-171">Type</span></span>           | <span data-ttu-id="b73ce-172">String</span><span class="sxs-lookup"><span data-stu-id="b73ce-172">String</span></span>                                                                                                                                                             |
| <span data-ttu-id="b73ce-173">預設值</span><span class="sxs-lookup"><span data-stu-id="b73ce-173">Default</span></span>        | <Generated>                                                                                                                                                  |
| <span data-ttu-id="b73ce-174">最小系統</span><span class="sxs-lookup"><span data-stu-id="b73ce-174">Minimum system</span></span> | <span data-ttu-id="b73ce-175">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b73ce-175">Windows Server 2003</span></span>                                                                                                                                                |



 

### <a name="name"></a><span data-ttu-id="b73ce-176">Name</span><span class="sxs-lookup"><span data-stu-id="b73ce-176">Name</span></span>



| <span data-ttu-id="b73ce-177">進入</span><span class="sxs-lookup"><span data-stu-id="b73ce-177">Entry</span></span> | <span data-ttu-id="b73ce-178">值</span><span class="sxs-lookup"><span data-stu-id="b73ce-178">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b73ce-179">描述</span><span class="sxs-lookup"><span data-stu-id="b73ce-179">Description</span></span>    | <span data-ttu-id="b73ce-180">表示資料分割名稱。</span><span class="sxs-lookup"><span data-stu-id="b73ce-180">Represents the partition name.</span></span> <span data-ttu-id="b73ce-181">移除字串開頭和結尾的額外空間。在這個集合的物件上呼叫 [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="b73ce-181">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="b73ce-182">Access</span><span class="sxs-lookup"><span data-stu-id="b73ce-182">Access</span></span>         | <span data-ttu-id="b73ce-183">讀寫</span><span class="sxs-lookup"><span data-stu-id="b73ce-183">ReadWrite</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="b73ce-184">類型</span><span class="sxs-lookup"><span data-stu-id="b73ce-184">Type</span></span>           | <span data-ttu-id="b73ce-185">String</span><span class="sxs-lookup"><span data-stu-id="b73ce-185">String</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="b73ce-186">預設值</span><span class="sxs-lookup"><span data-stu-id="b73ce-186">Default</span></span>        | <span data-ttu-id="b73ce-187">「新增分割區」</span><span class="sxs-lookup"><span data-stu-id="b73ce-187">"New Partition"</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="b73ce-188">最小系統</span><span class="sxs-lookup"><span data-stu-id="b73ce-188">Minimum system</span></span> | <span data-ttu-id="b73ce-189">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b73ce-189">Windows Server 2003</span></span>                                                                                                                                                                                                                    |



 

## <a name="see-also"></a><span data-ttu-id="b73ce-190">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b73ce-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b73ce-191">COM + 系統管理集合</span><span class="sxs-lookup"><span data-stu-id="b73ce-191">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 

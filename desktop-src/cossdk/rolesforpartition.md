---
description: RolesForPartition 集合一律與分割區集合中的物件相關。 它會針對每個指派給與其相關之分割區的角色保存物件。
ms.assetid: 56985f55-d6e8-4066-b6d5-21c62d4278ce
title: RolesForPartition 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RolesForPartition
api_type:
- COM
api_location: ''
ms.openlocfilehash: c97d524e3fc516086db3a815396d6d59f9369b31
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110389"
---
# <a name="rolesforpartition-collection"></a><span data-ttu-id="068c4-104">RolesForPartition 集合</span><span class="sxs-lookup"><span data-stu-id="068c4-104">RolesForPartition collection</span></span>

<span data-ttu-id="068c4-105">**RolesForPartition** 集合一律與分割 [**區集合中的物件**](partitions.md)相關。</span><span class="sxs-lookup"><span data-stu-id="068c4-105">The **RolesForPartition** collection is always related to an object in the [**Partitions**](partitions.md) collection.</span></span> <span data-ttu-id="068c4-106">它會針對每個指派給與其相關之分割區的角色保存物件。</span><span class="sxs-lookup"><span data-stu-id="068c4-106">It holds an object for each role assigned to the partition to which it is related.</span></span>

<span data-ttu-id="068c4-107">此集合不支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。</span><span class="sxs-lookup"><span data-stu-id="068c4-107">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="068c4-108">成員</span><span class="sxs-lookup"><span data-stu-id="068c4-108">Members</span></span>

<span data-ttu-id="068c4-109">**RolesForPartition** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。</span><span class="sxs-lookup"><span data-stu-id="068c4-109">The **RolesForPartition** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="068c4-110">相關集合</span><span class="sxs-lookup"><span data-stu-id="068c4-110">Related Collections</span></span>

<span data-ttu-id="068c4-111">您可以從這個集合流覽至下列任何集合：</span><span class="sxs-lookup"><span data-stu-id="068c4-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="068c4-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="068c4-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="068c4-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="068c4-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="068c4-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="068c4-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="068c4-115">**UsersInPartitionRole**</span><span class="sxs-lookup"><span data-stu-id="068c4-115">**UsersInPartitionRole**</span></span>](usersinpartitionrole.md)

<span data-ttu-id="068c4-116">您可以從下列集合流覽至這個集合：</span><span class="sxs-lookup"><span data-stu-id="068c4-116">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="068c4-117">**分區**</span><span class="sxs-lookup"><span data-stu-id="068c4-117">**Partitions**</span></span>](partitions.md)

## <a name="properties"></a><span data-ttu-id="068c4-118">屬性</span><span class="sxs-lookup"><span data-stu-id="068c4-118">Properties</span></span>

<span data-ttu-id="068c4-119">集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="068c4-119">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="068c4-120">描述</span><span class="sxs-lookup"><span data-stu-id="068c4-120">Description</span></span>](#description)
-   [<span data-ttu-id="068c4-121">Name</span><span class="sxs-lookup"><span data-stu-id="068c4-121">Name</span></span>](#name)

### <a name="description"></a><span data-ttu-id="068c4-122">Description</span><span class="sxs-lookup"><span data-stu-id="068c4-122">Description</span></span>



| <span data-ttu-id="068c4-123">進入</span><span class="sxs-lookup"><span data-stu-id="068c4-123">Entry</span></span> | <span data-ttu-id="068c4-124">值</span><span class="sxs-lookup"><span data-stu-id="068c4-124">Value</span></span> |
|----------------|----------------------------|
| <span data-ttu-id="068c4-125">描述</span><span class="sxs-lookup"><span data-stu-id="068c4-125">Description</span></span>    | <span data-ttu-id="068c4-126">角色的描述。</span><span class="sxs-lookup"><span data-stu-id="068c4-126">A description of the role.</span></span> |
| <span data-ttu-id="068c4-127">Access</span><span class="sxs-lookup"><span data-stu-id="068c4-127">Access</span></span>         | <span data-ttu-id="068c4-128">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="068c4-128">ReadOnly</span></span>                   |
| <span data-ttu-id="068c4-129">類型</span><span class="sxs-lookup"><span data-stu-id="068c4-129">Type</span></span>           | <span data-ttu-id="068c4-130">String</span><span class="sxs-lookup"><span data-stu-id="068c4-130">String</span></span>                     |
| <span data-ttu-id="068c4-131">預設值</span><span class="sxs-lookup"><span data-stu-id="068c4-131">Default</span></span>        | <span data-ttu-id="068c4-132">""</span><span class="sxs-lookup"><span data-stu-id="068c4-132">""</span></span>                         |
| <span data-ttu-id="068c4-133">最小系統</span><span class="sxs-lookup"><span data-stu-id="068c4-133">Minimum system</span></span> | <span data-ttu-id="068c4-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="068c4-134">Windows Server 2003</span></span>        |



 

### <a name="name"></a><span data-ttu-id="068c4-135">Name</span><span class="sxs-lookup"><span data-stu-id="068c4-135">Name</span></span>



| <span data-ttu-id="068c4-136">進入</span><span class="sxs-lookup"><span data-stu-id="068c4-136">Entry</span></span> | <span data-ttu-id="068c4-137">值</span><span class="sxs-lookup"><span data-stu-id="068c4-137">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="068c4-138">描述</span><span class="sxs-lookup"><span data-stu-id="068c4-138">Description</span></span>    | <span data-ttu-id="068c4-139">角色名稱。</span><span class="sxs-lookup"><span data-stu-id="068c4-139">The role name.</span></span> <span data-ttu-id="068c4-140">移除字串開頭和結尾的額外空間。當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 或 [**名稱**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="068c4-140">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="068c4-141">Access</span><span class="sxs-lookup"><span data-stu-id="068c4-141">Access</span></span>         | <span data-ttu-id="068c4-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="068c4-142">ReadOnly</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="068c4-143">類型</span><span class="sxs-lookup"><span data-stu-id="068c4-143">Type</span></span>           | <span data-ttu-id="068c4-144">String</span><span class="sxs-lookup"><span data-stu-id="068c4-144">String</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="068c4-145">預設值</span><span class="sxs-lookup"><span data-stu-id="068c4-145">Default</span></span>        | <span data-ttu-id="068c4-146">""</span><span class="sxs-lookup"><span data-stu-id="068c4-146">""</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="068c4-147">最小系統</span><span class="sxs-lookup"><span data-stu-id="068c4-147">Minimum system</span></span> | <span data-ttu-id="068c4-148">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="068c4-148">Windows Server 2003</span></span>                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a><span data-ttu-id="068c4-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="068c4-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="068c4-150">COM + 系統管理集合</span><span class="sxs-lookup"><span data-stu-id="068c4-150">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 

---
description: 包含每個資料分割使用者的物件。
ms.assetid: baec56ae-be8a-42a7-90bc-1db7c5cd7fe2
title: PartitionUsers 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PartitionUsers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1521642879037938451decd873a9aa14211ce296
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989900"
---
# <a name="partitionusers-collection"></a><span data-ttu-id="e92ef-103">PartitionUsers 集合</span><span class="sxs-lookup"><span data-stu-id="e92ef-103">PartitionUsers collection</span></span>

<span data-ttu-id="e92ef-104">包含每個資料分割使用者的物件。</span><span class="sxs-lookup"><span data-stu-id="e92ef-104">Contains an object for each partition user.</span></span>

<span data-ttu-id="e92ef-105">此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**加入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**移除**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。</span><span class="sxs-lookup"><span data-stu-id="e92ef-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="e92ef-106">成員</span><span class="sxs-lookup"><span data-stu-id="e92ef-106">Members</span></span>

<span data-ttu-id="e92ef-107">**PartitionUsers** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。</span><span class="sxs-lookup"><span data-stu-id="e92ef-107">The **PartitionUsers** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="e92ef-108">相關集合</span><span class="sxs-lookup"><span data-stu-id="e92ef-108">Related Collections</span></span>

<span data-ttu-id="e92ef-109">您可以從這個集合流覽至下列任何集合：</span><span class="sxs-lookup"><span data-stu-id="e92ef-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="e92ef-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="e92ef-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="e92ef-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="e92ef-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="e92ef-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="e92ef-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="e92ef-113">您可以從下列集合流覽至這個集合：</span><span class="sxs-lookup"><span data-stu-id="e92ef-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="e92ef-114">**根**</span><span class="sxs-lookup"><span data-stu-id="e92ef-114">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="e92ef-115">屬性</span><span class="sxs-lookup"><span data-stu-id="e92ef-115">Properties</span></span>

<span data-ttu-id="e92ef-116">集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="e92ef-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="e92ef-117">AccountName</span><span class="sxs-lookup"><span data-stu-id="e92ef-117">AccountName</span></span>](#accountname)
-   [<span data-ttu-id="e92ef-118">DefaultPartitionID</span><span class="sxs-lookup"><span data-stu-id="e92ef-118">DefaultPartitionID</span></span>](#defaultpartitionid)

### <a name="accountname"></a><span data-ttu-id="e92ef-119">AccountName</span><span class="sxs-lookup"><span data-stu-id="e92ef-119">AccountName</span></span>



| <span data-ttu-id="e92ef-120">進入</span><span class="sxs-lookup"><span data-stu-id="e92ef-120">Entry</span></span> | <span data-ttu-id="e92ef-121">值</span><span class="sxs-lookup"><span data-stu-id="e92ef-121">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e92ef-122">描述</span><span class="sxs-lookup"><span data-stu-id="e92ef-122">Description</span></span>    | <span data-ttu-id="e92ef-123">分割區使用者帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="e92ef-123">Name of the partition user's account.</span></span> <span data-ttu-id="e92ef-124">當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 或 [**名稱**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="e92ef-124">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="e92ef-125">Access</span><span class="sxs-lookup"><span data-stu-id="e92ef-125">Access</span></span>         | <span data-ttu-id="e92ef-126">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="e92ef-126">WriteOnce</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="e92ef-127">類型</span><span class="sxs-lookup"><span data-stu-id="e92ef-127">Type</span></span>           | <span data-ttu-id="e92ef-128">String</span><span class="sxs-lookup"><span data-stu-id="e92ef-128">String</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="e92ef-129">預設值</span><span class="sxs-lookup"><span data-stu-id="e92ef-129">Default</span></span>        | <span data-ttu-id="e92ef-130">[新增使用者]</span><span class="sxs-lookup"><span data-stu-id="e92ef-130">"New User"</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="e92ef-131">最小系統</span><span class="sxs-lookup"><span data-stu-id="e92ef-131">Minimum system</span></span> | <span data-ttu-id="e92ef-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e92ef-132">Windows Server 2003</span></span>                                                                                                                                                                                          |



 

### <a name="defaultpartitionid"></a><span data-ttu-id="e92ef-133">DefaultPartitionID</span><span class="sxs-lookup"><span data-stu-id="e92ef-133">DefaultPartitionID</span></span>



| <span data-ttu-id="e92ef-134">進入</span><span class="sxs-lookup"><span data-stu-id="e92ef-134">Entry</span></span> | <span data-ttu-id="e92ef-135">值</span><span class="sxs-lookup"><span data-stu-id="e92ef-135">Value</span></span> |
|----------------|--------------------------------------------------------------------|
| <span data-ttu-id="e92ef-136">描述</span><span class="sxs-lookup"><span data-stu-id="e92ef-136">Description</span></span>    | <span data-ttu-id="e92ef-137">基底應用程式分割區的全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="e92ef-137">The globally unique identifier for the base application partition.</span></span> |
| <span data-ttu-id="e92ef-138">Access</span><span class="sxs-lookup"><span data-stu-id="e92ef-138">Access</span></span>         | <span data-ttu-id="e92ef-139">讀寫</span><span class="sxs-lookup"><span data-stu-id="e92ef-139">ReadWrite</span></span>                                                          |
| <span data-ttu-id="e92ef-140">類型</span><span class="sxs-lookup"><span data-stu-id="e92ef-140">Type</span></span>           | <span data-ttu-id="e92ef-141">String</span><span class="sxs-lookup"><span data-stu-id="e92ef-141">String</span></span>                                                             |
| <span data-ttu-id="e92ef-142">預設值</span><span class="sxs-lookup"><span data-stu-id="e92ef-142">Default</span></span>        | <span data-ttu-id="e92ef-143">{41E90F3E-56C1-4633-81C3-6E8BAC8BDD70}</span><span class="sxs-lookup"><span data-stu-id="e92ef-143">{41E90F3E-56C1-4633-81C3-6E8BAC8BDD70}</span></span>                             |
| <span data-ttu-id="e92ef-144">最小系統</span><span class="sxs-lookup"><span data-stu-id="e92ef-144">Minimum system</span></span> | <span data-ttu-id="e92ef-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e92ef-145">Windows Server 2003</span></span>                                                |



 

## <a name="see-also"></a><span data-ttu-id="e92ef-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e92ef-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e92ef-147">COM + 系統管理集合</span><span class="sxs-lookup"><span data-stu-id="e92ef-147">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 

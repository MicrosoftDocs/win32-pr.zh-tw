---
description: 針對與集合相關的角色中的每個使用者，各包含一個物件。
ms.assetid: c6aebf7a-04d1-4c7c-a015-bc6fb4841c4a
title: UsersInPartitionRole 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UsersInPartitionRole
api_type:
- COM
api_location: ''
ms.openlocfilehash: fce1577636a7b2e678bdade9c32f706c7ccbf158
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110892"
---
# <a name="usersinpartitionrole-collection"></a><span data-ttu-id="b3f81-103">UsersInPartitionRole 集合</span><span class="sxs-lookup"><span data-stu-id="b3f81-103">UsersInPartitionRole collection</span></span>

<span data-ttu-id="b3f81-104">針對與集合相關的角色中的每個使用者，各包含一個物件。</span><span class="sxs-lookup"><span data-stu-id="b3f81-104">Contains an object for each user in the role to which the collection is related.</span></span>

<span data-ttu-id="b3f81-105">此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**加入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**移除**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。</span><span class="sxs-lookup"><span data-stu-id="b3f81-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="b3f81-106">成員</span><span class="sxs-lookup"><span data-stu-id="b3f81-106">Members</span></span>

<span data-ttu-id="b3f81-107">**UsersInPartitionRole** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。</span><span class="sxs-lookup"><span data-stu-id="b3f81-107">The **UsersInPartitionRole** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="b3f81-108">相關集合</span><span class="sxs-lookup"><span data-stu-id="b3f81-108">Related Collections</span></span>

<span data-ttu-id="b3f81-109">您可以從這個集合流覽至下列任何集合：</span><span class="sxs-lookup"><span data-stu-id="b3f81-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="b3f81-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="b3f81-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="b3f81-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="b3f81-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="b3f81-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="b3f81-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="b3f81-113">您可以從下列集合流覽至這個集合：</span><span class="sxs-lookup"><span data-stu-id="b3f81-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="b3f81-114">**RolesForPartition**</span><span class="sxs-lookup"><span data-stu-id="b3f81-114">**RolesForPartition**</span></span>](rolesforpartition.md)

## <a name="properties"></a><span data-ttu-id="b3f81-115">屬性</span><span class="sxs-lookup"><span data-stu-id="b3f81-115">Properties</span></span>

<span data-ttu-id="b3f81-116">集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="b3f81-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="b3f81-117">使用者</span><span class="sxs-lookup"><span data-stu-id="b3f81-117">User</span></span>](#usersinpartitionrole-collection)

### <a name="user"></a><span data-ttu-id="b3f81-118">User</span><span class="sxs-lookup"><span data-stu-id="b3f81-118">User</span></span>



| <span data-ttu-id="b3f81-119">進入</span><span class="sxs-lookup"><span data-stu-id="b3f81-119">Entry</span></span> | <span data-ttu-id="b3f81-120">值</span><span class="sxs-lookup"><span data-stu-id="b3f81-120">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3f81-121">描述</span><span class="sxs-lookup"><span data-stu-id="b3f81-121">Description</span></span>    | <span data-ttu-id="b3f81-122">使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="b3f81-122">The user name.</span></span> <span data-ttu-id="b3f81-123">當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 或 [**名稱**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="b3f81-123">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="b3f81-124">Access</span><span class="sxs-lookup"><span data-stu-id="b3f81-124">Access</span></span>         | <span data-ttu-id="b3f81-125">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="b3f81-125">WriteOnce</span></span>                                                                                                                                                                             |
| <span data-ttu-id="b3f81-126">類型</span><span class="sxs-lookup"><span data-stu-id="b3f81-126">Type</span></span>           | <span data-ttu-id="b3f81-127">String</span><span class="sxs-lookup"><span data-stu-id="b3f81-127">String</span></span>                                                                                                                                                                                |
| <span data-ttu-id="b3f81-128">預設值</span><span class="sxs-lookup"><span data-stu-id="b3f81-128">Default</span></span>        | <span data-ttu-id="b3f81-129">[新增使用者]</span><span class="sxs-lookup"><span data-stu-id="b3f81-129">"New User"</span></span>                                                                                                                                                                            |
| <span data-ttu-id="b3f81-130">最小系統</span><span class="sxs-lookup"><span data-stu-id="b3f81-130">Minimum system</span></span> | <span data-ttu-id="b3f81-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b3f81-131">Windows Server 2003</span></span>                                                                                                                                                                   |



 

## <a name="see-also"></a><span data-ttu-id="b3f81-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b3f81-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3f81-133">COM + 系統管理集合</span><span class="sxs-lookup"><span data-stu-id="b3f81-133">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 

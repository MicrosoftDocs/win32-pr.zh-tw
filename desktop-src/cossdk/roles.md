---
description: Role 集合一律與應用程式集合中的物件相關。 它會針對指派給與其相關聯之應用程式的每個角色保存物件。
ms.assetid: 87f39c2a-ad66-4390-9220-06751dcebd95
title: 角色集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Roles
api_type:
- COM
api_location: ''
ms.openlocfilehash: f676a53f5fe54e42ca2a489ad834b9c91e4e0ef5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191006"
---
# <a name="roles-collection"></a><span data-ttu-id="69fe0-104">角色集合</span><span class="sxs-lookup"><span data-stu-id="69fe0-104">Roles collection</span></span>

<span data-ttu-id="69fe0-105">**Role** 集合一律與 [**應用程式**](applications.md)集合中的物件相關。</span><span class="sxs-lookup"><span data-stu-id="69fe0-105">The **Roles** collection is always related to an object in the [**Applications**](applications.md) collection.</span></span> <span data-ttu-id="69fe0-106">它會針對指派給與其相關聯之應用程式的每個角色保存物件。</span><span class="sxs-lookup"><span data-stu-id="69fe0-106">It holds an object for each role assigned to the application to which it is related.</span></span>

<span data-ttu-id="69fe0-107">此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**加入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**移除**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。</span><span class="sxs-lookup"><span data-stu-id="69fe0-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="69fe0-108">成員</span><span class="sxs-lookup"><span data-stu-id="69fe0-108">Members</span></span>

<span data-ttu-id="69fe0-109">**Roles** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。</span><span class="sxs-lookup"><span data-stu-id="69fe0-109">The **Roles** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="69fe0-110">相關集合</span><span class="sxs-lookup"><span data-stu-id="69fe0-110">Related Collections</span></span>

<span data-ttu-id="69fe0-111">您可以從這個集合流覽至下列任何集合：</span><span class="sxs-lookup"><span data-stu-id="69fe0-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="69fe0-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="69fe0-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="69fe0-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="69fe0-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="69fe0-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="69fe0-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="69fe0-115">**UsersInRole**</span><span class="sxs-lookup"><span data-stu-id="69fe0-115">**UsersInRole**</span></span>](usersinrole.md)

<span data-ttu-id="69fe0-116">您可以從下列集合流覽至這個集合：</span><span class="sxs-lookup"><span data-stu-id="69fe0-116">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="69fe0-117">**應用程式**</span><span class="sxs-lookup"><span data-stu-id="69fe0-117">**Applications**</span></span>](applications.md)

## <a name="properties"></a><span data-ttu-id="69fe0-118">屬性</span><span class="sxs-lookup"><span data-stu-id="69fe0-118">Properties</span></span>

<span data-ttu-id="69fe0-119">集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="69fe0-119">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="69fe0-120">描述</span><span class="sxs-lookup"><span data-stu-id="69fe0-120">Description</span></span>](#description)
-   [<span data-ttu-id="69fe0-121">Name</span><span class="sxs-lookup"><span data-stu-id="69fe0-121">Name</span></span>](#name)

### <a name="description"></a><span data-ttu-id="69fe0-122">Description</span><span class="sxs-lookup"><span data-stu-id="69fe0-122">Description</span></span>



| <span data-ttu-id="69fe0-123">進入</span><span class="sxs-lookup"><span data-stu-id="69fe0-123">Entry</span></span> | <span data-ttu-id="69fe0-124">值</span><span class="sxs-lookup"><span data-stu-id="69fe0-124">Value</span></span> |
|----------------|----------------------------|
| <span data-ttu-id="69fe0-125">描述</span><span class="sxs-lookup"><span data-stu-id="69fe0-125">Description</span></span>    | <span data-ttu-id="69fe0-126">角色的描述。</span><span class="sxs-lookup"><span data-stu-id="69fe0-126">A description of the role.</span></span> |
| <span data-ttu-id="69fe0-127">Access</span><span class="sxs-lookup"><span data-stu-id="69fe0-127">Access</span></span>         | <span data-ttu-id="69fe0-128">讀寫</span><span class="sxs-lookup"><span data-stu-id="69fe0-128">ReadWrite</span></span>                  |
| <span data-ttu-id="69fe0-129">類型</span><span class="sxs-lookup"><span data-stu-id="69fe0-129">Type</span></span>           | <span data-ttu-id="69fe0-130">String</span><span class="sxs-lookup"><span data-stu-id="69fe0-130">String</span></span>                     |
| <span data-ttu-id="69fe0-131">預設值</span><span class="sxs-lookup"><span data-stu-id="69fe0-131">Default</span></span>        | <span data-ttu-id="69fe0-132">""</span><span class="sxs-lookup"><span data-stu-id="69fe0-132">""</span></span>                         |
| <span data-ttu-id="69fe0-133">最小系統</span><span class="sxs-lookup"><span data-stu-id="69fe0-133">Minimum system</span></span> | <span data-ttu-id="69fe0-134">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="69fe0-134">Windows 2000</span></span>               |



 

### <a name="name"></a><span data-ttu-id="69fe0-135">Name</span><span class="sxs-lookup"><span data-stu-id="69fe0-135">Name</span></span>



| <span data-ttu-id="69fe0-136">進入</span><span class="sxs-lookup"><span data-stu-id="69fe0-136">Entry</span></span> | <span data-ttu-id="69fe0-137">值</span><span class="sxs-lookup"><span data-stu-id="69fe0-137">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69fe0-138">描述</span><span class="sxs-lookup"><span data-stu-id="69fe0-138">Description</span></span>    | <span data-ttu-id="69fe0-139">角色名稱。</span><span class="sxs-lookup"><span data-stu-id="69fe0-139">The role name.</span></span> <span data-ttu-id="69fe0-140">移除字串開頭和結尾的額外空間。當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 或 [**名稱**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="69fe0-140">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="69fe0-141">Access</span><span class="sxs-lookup"><span data-stu-id="69fe0-141">Access</span></span>         | <span data-ttu-id="69fe0-142">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="69fe0-142">WriteOnce</span></span>                                                                                                                                                                                                                                                   |
| <span data-ttu-id="69fe0-143">類型</span><span class="sxs-lookup"><span data-stu-id="69fe0-143">Type</span></span>           | <span data-ttu-id="69fe0-144">String</span><span class="sxs-lookup"><span data-stu-id="69fe0-144">String</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="69fe0-145">預設值</span><span class="sxs-lookup"><span data-stu-id="69fe0-145">Default</span></span>        | <span data-ttu-id="69fe0-146">「新角色」</span><span class="sxs-lookup"><span data-stu-id="69fe0-146">"New Role"</span></span>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="69fe0-147">最小系統</span><span class="sxs-lookup"><span data-stu-id="69fe0-147">Minimum system</span></span> | <span data-ttu-id="69fe0-148">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="69fe0-148">Windows 2000</span></span>                                                                                                                                                                                                                                                |



 

## <a name="see-also"></a><span data-ttu-id="69fe0-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69fe0-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69fe0-150">COM + 系統管理集合</span><span class="sxs-lookup"><span data-stu-id="69fe0-150">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 

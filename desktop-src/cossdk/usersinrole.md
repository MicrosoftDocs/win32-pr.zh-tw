---
description: UsersInRole 集合-包含與集合相關的角色中每位使用者的物件。
ms.assetid: e7d9e5e8-1927-42b2-bdd5-0c49a562c31f
title: UsersInRole 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UsersInRole
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1b73c495a1af1dec9114e5a59274e457c1d09694
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105536"
---
# <a name="usersinrole-collection"></a><span data-ttu-id="a6097-103">UsersInRole 集合</span><span class="sxs-lookup"><span data-stu-id="a6097-103">UsersInRole collection</span></span>

<span data-ttu-id="a6097-104">針對與集合相關的角色中的每個使用者，各包含一個物件。</span><span class="sxs-lookup"><span data-stu-id="a6097-104">Contains an object for each user in the role to which the collection is related.</span></span>

<span data-ttu-id="a6097-105">此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**加入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**移除**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。</span><span class="sxs-lookup"><span data-stu-id="a6097-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="a6097-106">成員</span><span class="sxs-lookup"><span data-stu-id="a6097-106">Members</span></span>

<span data-ttu-id="a6097-107">**UsersInRole** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。</span><span class="sxs-lookup"><span data-stu-id="a6097-107">The **UsersInRole** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="a6097-108">相關集合</span><span class="sxs-lookup"><span data-stu-id="a6097-108">Related Collections</span></span>

<span data-ttu-id="a6097-109">您可以從這個集合流覽至下列任何集合：</span><span class="sxs-lookup"><span data-stu-id="a6097-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="a6097-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="a6097-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="a6097-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="a6097-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="a6097-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="a6097-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="a6097-113">您可以從下列集合流覽至這個集合：</span><span class="sxs-lookup"><span data-stu-id="a6097-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="a6097-114">**角色**</span><span class="sxs-lookup"><span data-stu-id="a6097-114">**Roles**</span></span>](roles.md)

## <a name="properties"></a><span data-ttu-id="a6097-115">屬性</span><span class="sxs-lookup"><span data-stu-id="a6097-115">Properties</span></span>

<span data-ttu-id="a6097-116">集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="a6097-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="a6097-117">使用者</span><span class="sxs-lookup"><span data-stu-id="a6097-117">User</span></span>](#usersinrole-collection)

### <a name="user"></a><span data-ttu-id="a6097-118">User</span><span class="sxs-lookup"><span data-stu-id="a6097-118">User</span></span>



| <span data-ttu-id="a6097-119">進入</span><span class="sxs-lookup"><span data-stu-id="a6097-119">Entry</span></span> | <span data-ttu-id="a6097-120">值</span><span class="sxs-lookup"><span data-stu-id="a6097-120">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6097-121">描述</span><span class="sxs-lookup"><span data-stu-id="a6097-121">Description</span></span>    | <span data-ttu-id="a6097-122">使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="a6097-122">The user name.</span></span> <span data-ttu-id="a6097-123">當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 或 [**名稱**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="a6097-123">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="a6097-124">Access</span><span class="sxs-lookup"><span data-stu-id="a6097-124">Access</span></span>         | <span data-ttu-id="a6097-125">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="a6097-125">WriteOnce</span></span>                                                                                                                                                                             |
| <span data-ttu-id="a6097-126">類型</span><span class="sxs-lookup"><span data-stu-id="a6097-126">Type</span></span>           | <span data-ttu-id="a6097-127">String</span><span class="sxs-lookup"><span data-stu-id="a6097-127">String</span></span>                                                                                                                                                                                |
| <span data-ttu-id="a6097-128">預設值</span><span class="sxs-lookup"><span data-stu-id="a6097-128">Default</span></span>        | <span data-ttu-id="a6097-129">[新增使用者]</span><span class="sxs-lookup"><span data-stu-id="a6097-129">"New User"</span></span>                                                                                                                                                                            |
| <span data-ttu-id="a6097-130">最小系統</span><span class="sxs-lookup"><span data-stu-id="a6097-130">Minimum system</span></span> | <span data-ttu-id="a6097-131">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a6097-131">Windows 2000</span></span>                                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="a6097-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a6097-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6097-133">COM + 系統管理集合</span><span class="sxs-lookup"><span data-stu-id="a6097-133">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 

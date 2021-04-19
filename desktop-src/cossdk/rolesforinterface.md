---
description: 針對指派給集合所關聯之介面的每個角色，各包含一個物件。 角色必須已在應用層級指派。
ms.assetid: f5c1dc9a-13da-4504-a244-4ce8058240b8
title: RolesForInterface 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RolesForInterface
api_type:
- COM
api_location: ''
ms.openlocfilehash: 60c52e3cb48adc0ed52ef10bd9e0a73e716fabfc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973155"
---
# <a name="rolesforinterface-collection"></a><span data-ttu-id="15951-104">RolesForInterface 集合</span><span class="sxs-lookup"><span data-stu-id="15951-104">RolesForInterface collection</span></span>

<span data-ttu-id="15951-105">針對指派給集合所關聯之介面的每個角色，各包含一個物件。</span><span class="sxs-lookup"><span data-stu-id="15951-105">Contains an object for each role assigned to the interface to which the collection is related.</span></span> <span data-ttu-id="15951-106">角色必須已在應用層級指派。</span><span class="sxs-lookup"><span data-stu-id="15951-106">The roles must already be assigned at the application level.</span></span>

<span data-ttu-id="15951-107">此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**加入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**移除**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。</span><span class="sxs-lookup"><span data-stu-id="15951-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="15951-108">成員</span><span class="sxs-lookup"><span data-stu-id="15951-108">Members</span></span>

<span data-ttu-id="15951-109">**RolesForInterface** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。</span><span class="sxs-lookup"><span data-stu-id="15951-109">The **RolesForInterface** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="15951-110">相關集合</span><span class="sxs-lookup"><span data-stu-id="15951-110">Related Collections</span></span>

<span data-ttu-id="15951-111">您可以從這個集合流覽至下列任何集合：</span><span class="sxs-lookup"><span data-stu-id="15951-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="15951-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="15951-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="15951-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="15951-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="15951-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="15951-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="15951-115">您可以從下列集合流覽至這個集合：</span><span class="sxs-lookup"><span data-stu-id="15951-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="15951-116">**InterfacesForComponent**</span><span class="sxs-lookup"><span data-stu-id="15951-116">**InterfacesForComponent**</span></span>](interfacesforcomponent.md)

## <a name="properties"></a><span data-ttu-id="15951-117">屬性</span><span class="sxs-lookup"><span data-stu-id="15951-117">Properties</span></span>

<span data-ttu-id="15951-118">集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="15951-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="15951-119">名稱</span><span class="sxs-lookup"><span data-stu-id="15951-119">Name</span></span>](#name)

### <a name="name"></a><span data-ttu-id="15951-120">Name</span><span class="sxs-lookup"><span data-stu-id="15951-120">Name</span></span>



| <span data-ttu-id="15951-121">進入</span><span class="sxs-lookup"><span data-stu-id="15951-121">Entry</span></span> | <span data-ttu-id="15951-122">值</span><span class="sxs-lookup"><span data-stu-id="15951-122">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15951-123">描述</span><span class="sxs-lookup"><span data-stu-id="15951-123">Description</span></span>    | <span data-ttu-id="15951-124">角色名稱。</span><span class="sxs-lookup"><span data-stu-id="15951-124">The role name.</span></span> <span data-ttu-id="15951-125">必須已經是指派給應用程式的角色， (出現在 [角色] 集合) 中。</span><span class="sxs-lookup"><span data-stu-id="15951-125">Must already be a role assigned to the application (appearing in the Roles collection).</span></span> <span data-ttu-id="15951-126">移除字串開頭和結尾的額外空間。當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 或 [**名稱**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="15951-126">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="15951-127">Access</span><span class="sxs-lookup"><span data-stu-id="15951-127">Access</span></span>         | <span data-ttu-id="15951-128">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="15951-128">WriteOnce</span></span>                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="15951-129">類型</span><span class="sxs-lookup"><span data-stu-id="15951-129">Type</span></span>           | <span data-ttu-id="15951-130">String</span><span class="sxs-lookup"><span data-stu-id="15951-130">String</span></span>                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="15951-131">預設值</span><span class="sxs-lookup"><span data-stu-id="15951-131">Default</span></span>        | <span data-ttu-id="15951-132">「新角色」</span><span class="sxs-lookup"><span data-stu-id="15951-132">"New Role"</span></span>                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="15951-133">最小系統</span><span class="sxs-lookup"><span data-stu-id="15951-133">Minimum system</span></span> | <span data-ttu-id="15951-134">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="15951-134">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="see-also"></a><span data-ttu-id="15951-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="15951-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15951-136">COM + 系統管理集合</span><span class="sxs-lookup"><span data-stu-id="15951-136">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 

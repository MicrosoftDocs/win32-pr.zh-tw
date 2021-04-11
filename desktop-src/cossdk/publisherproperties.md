---
description: 包含父 SubscriptionsForComponent 集合之每個發行者屬性的物件。
ms.assetid: 7699c258-ca11-4652-b2f7-b2f2307c01fc
title: PublisherProperties 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublisherProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: bdab3e8143ea3d35d07adb5caa73639fcb568cd1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110900"
---
# <a name="publisherproperties-collection"></a><span data-ttu-id="e8557-103">PublisherProperties 集合</span><span class="sxs-lookup"><span data-stu-id="e8557-103">PublisherProperties collection</span></span>

<span data-ttu-id="e8557-104">包含父 [**SubscriptionsForComponent**](subscriptionsforcomponent.md) 集合之每個發行者屬性的物件。</span><span class="sxs-lookup"><span data-stu-id="e8557-104">Contains an object for each publisher property for the parent [**SubscriptionsForComponent**](subscriptionsforcomponent.md) collection.</span></span>

<span data-ttu-id="e8557-105">此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**加入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**移除**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。</span><span class="sxs-lookup"><span data-stu-id="e8557-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="e8557-106">成員</span><span class="sxs-lookup"><span data-stu-id="e8557-106">Members</span></span>

<span data-ttu-id="e8557-107">**PublisherProperties** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。</span><span class="sxs-lookup"><span data-stu-id="e8557-107">The **PublisherProperties** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="e8557-108">相關集合</span><span class="sxs-lookup"><span data-stu-id="e8557-108">Related Collections</span></span>

<span data-ttu-id="e8557-109">您可以從這個集合流覽至下列任何集合：</span><span class="sxs-lookup"><span data-stu-id="e8557-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="e8557-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="e8557-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="e8557-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="e8557-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="e8557-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="e8557-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="e8557-113">您可以從下列集合流覽至這個集合：</span><span class="sxs-lookup"><span data-stu-id="e8557-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="e8557-114">**SubscriptionsForComponent**</span><span class="sxs-lookup"><span data-stu-id="e8557-114">**SubscriptionsForComponent**</span></span>](subscriptionsforcomponent.md)

## <a name="properties"></a><span data-ttu-id="e8557-115">屬性</span><span class="sxs-lookup"><span data-stu-id="e8557-115">Properties</span></span>

<span data-ttu-id="e8557-116">集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="e8557-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="e8557-117">名稱</span><span class="sxs-lookup"><span data-stu-id="e8557-117">Name</span></span>](#name)
-   [<span data-ttu-id="e8557-118">ReplTest1</span><span class="sxs-lookup"><span data-stu-id="e8557-118">Value</span></span>](#value)

### <a name="name"></a><span data-ttu-id="e8557-119">名稱</span><span class="sxs-lookup"><span data-stu-id="e8557-119">Name</span></span>



| <span data-ttu-id="e8557-120">進入</span><span class="sxs-lookup"><span data-stu-id="e8557-120">Entry</span></span> | <span data-ttu-id="e8557-121">值</span><span class="sxs-lookup"><span data-stu-id="e8557-121">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8557-122">描述</span><span class="sxs-lookup"><span data-stu-id="e8557-122">Description</span></span>    | <span data-ttu-id="e8557-123">屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8557-123">The name of the property.</span></span> <span data-ttu-id="e8557-124">移除字串開頭和結尾的額外空間。當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 或 [**名稱**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="e8557-124">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="e8557-125">Access</span><span class="sxs-lookup"><span data-stu-id="e8557-125">Access</span></span>         | <span data-ttu-id="e8557-126">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="e8557-126">WriteOnce</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="e8557-127">類型</span><span class="sxs-lookup"><span data-stu-id="e8557-127">Type</span></span>           | <span data-ttu-id="e8557-128">String</span><span class="sxs-lookup"><span data-stu-id="e8557-128">String</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="e8557-129">預設值</span><span class="sxs-lookup"><span data-stu-id="e8557-129">Default</span></span>        | <span data-ttu-id="e8557-130">[新增屬性]</span><span class="sxs-lookup"><span data-stu-id="e8557-130">"New Property"</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="e8557-131">最小系統</span><span class="sxs-lookup"><span data-stu-id="e8557-131">Minimum system</span></span> | <span data-ttu-id="e8557-132">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="e8557-132">Windows 2000</span></span>                                                                                                                                                                                                                                                           |



 

### <a name="value"></a><span data-ttu-id="e8557-133">值</span><span class="sxs-lookup"><span data-stu-id="e8557-133">Value</span></span>



| <span data-ttu-id="e8557-134">進入</span><span class="sxs-lookup"><span data-stu-id="e8557-134">Entry</span></span> | <span data-ttu-id="e8557-135">值</span><span class="sxs-lookup"><span data-stu-id="e8557-135">Value</span></span> |
|----------------|---------------------------|
| <span data-ttu-id="e8557-136">描述</span><span class="sxs-lookup"><span data-stu-id="e8557-136">Description</span></span>    | <span data-ttu-id="e8557-137">屬性的值。</span><span class="sxs-lookup"><span data-stu-id="e8557-137">A value for the property.</span></span> |
| <span data-ttu-id="e8557-138">Access</span><span class="sxs-lookup"><span data-stu-id="e8557-138">Access</span></span>         | <span data-ttu-id="e8557-139">讀寫</span><span class="sxs-lookup"><span data-stu-id="e8557-139">ReadWrite</span></span>                 |
| <span data-ttu-id="e8557-140">類型</span><span class="sxs-lookup"><span data-stu-id="e8557-140">Type</span></span>           | <span data-ttu-id="e8557-141">Variant</span><span class="sxs-lookup"><span data-stu-id="e8557-141">Variant</span></span>                   |
| <span data-ttu-id="e8557-142">預設</span><span class="sxs-lookup"><span data-stu-id="e8557-142">Default</span></span>        | <span data-ttu-id="e8557-143">N/A</span><span class="sxs-lookup"><span data-stu-id="e8557-143">N/A</span></span>                       |
| <span data-ttu-id="e8557-144">最小系統</span><span class="sxs-lookup"><span data-stu-id="e8557-144">Minimum system</span></span> | <span data-ttu-id="e8557-145">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="e8557-145">Windows 2000</span></span>              |



 

## <a name="see-also"></a><span data-ttu-id="e8557-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e8557-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8557-147">COM + 系統管理集合</span><span class="sxs-lookup"><span data-stu-id="e8557-147">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 

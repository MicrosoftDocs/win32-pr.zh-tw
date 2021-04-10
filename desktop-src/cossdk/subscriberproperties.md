---
description: 包含父 SubscriptionsForComponent 集合之每個訂閱者屬性的物件。
ms.assetid: 58c9edbd-1128-4b8c-bb5a-528c212aa6a7
title: SubscriberProperties 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscriberProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7c7a563e3fd3e917812426e34debd87bfd534b46
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847217"
---
# <a name="subscriberproperties-collection"></a><span data-ttu-id="3b76e-103">SubscriberProperties 集合</span><span class="sxs-lookup"><span data-stu-id="3b76e-103">SubscriberProperties collection</span></span>

<span data-ttu-id="3b76e-104">包含父 [**SubscriptionsForComponent**](subscriptionsforcomponent.md) 集合之每個訂閱者屬性的物件。</span><span class="sxs-lookup"><span data-stu-id="3b76e-104">Contains an object for each subscriber property for the parent [**SubscriptionsForComponent**](subscriptionsforcomponent.md) collection.</span></span>

<span data-ttu-id="3b76e-105">此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**加入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**移除**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。</span><span class="sxs-lookup"><span data-stu-id="3b76e-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="3b76e-106">成員</span><span class="sxs-lookup"><span data-stu-id="3b76e-106">Members</span></span>

<span data-ttu-id="3b76e-107">**SubscriberProperties** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。</span><span class="sxs-lookup"><span data-stu-id="3b76e-107">The **SubscriberProperties** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="3b76e-108">相關集合</span><span class="sxs-lookup"><span data-stu-id="3b76e-108">Related Collections</span></span>

<span data-ttu-id="3b76e-109">您可以從這個集合流覽至下列任何集合：</span><span class="sxs-lookup"><span data-stu-id="3b76e-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="3b76e-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="3b76e-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="3b76e-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="3b76e-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="3b76e-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="3b76e-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="3b76e-113">您可以從下列集合流覽至這個集合：</span><span class="sxs-lookup"><span data-stu-id="3b76e-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="3b76e-114">**SubscriptionsForComponent**</span><span class="sxs-lookup"><span data-stu-id="3b76e-114">**SubscriptionsForComponent**</span></span>](subscriptionsforcomponent.md)

## <a name="properties"></a><span data-ttu-id="3b76e-115">屬性</span><span class="sxs-lookup"><span data-stu-id="3b76e-115">Properties</span></span>

<span data-ttu-id="3b76e-116">集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="3b76e-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="3b76e-117">名稱</span><span class="sxs-lookup"><span data-stu-id="3b76e-117">Name</span></span>](#name)
-   [<span data-ttu-id="3b76e-118">ReplTest1</span><span class="sxs-lookup"><span data-stu-id="3b76e-118">Value</span></span>](#value)

### <a name="name"></a><span data-ttu-id="3b76e-119">名稱</span><span class="sxs-lookup"><span data-stu-id="3b76e-119">Name</span></span>



| <span data-ttu-id="3b76e-120">進入</span><span class="sxs-lookup"><span data-stu-id="3b76e-120">Entry</span></span> | <span data-ttu-id="3b76e-121">值</span><span class="sxs-lookup"><span data-stu-id="3b76e-121">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b76e-122">描述</span><span class="sxs-lookup"><span data-stu-id="3b76e-122">Description</span></span>    | <span data-ttu-id="3b76e-123">屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="3b76e-123">The name of the property.</span></span> <span data-ttu-id="3b76e-124">移除字串開頭和結尾的額外空間。當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 或 [**名稱**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="3b76e-124">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="3b76e-125">Access</span><span class="sxs-lookup"><span data-stu-id="3b76e-125">Access</span></span>         | <span data-ttu-id="3b76e-126">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="3b76e-126">WriteOnce</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="3b76e-127">類型</span><span class="sxs-lookup"><span data-stu-id="3b76e-127">Type</span></span>           | <span data-ttu-id="3b76e-128">String</span><span class="sxs-lookup"><span data-stu-id="3b76e-128">String</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="3b76e-129">預設值</span><span class="sxs-lookup"><span data-stu-id="3b76e-129">Default</span></span>        | <span data-ttu-id="3b76e-130">[新增屬性]</span><span class="sxs-lookup"><span data-stu-id="3b76e-130">"New Property"</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="3b76e-131">最小系統</span><span class="sxs-lookup"><span data-stu-id="3b76e-131">Minimum system</span></span> | <span data-ttu-id="3b76e-132">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3b76e-132">Windows 2000</span></span>                                                                                                                                                                                                                                                           |



 

### <a name="value"></a><span data-ttu-id="3b76e-133">值</span><span class="sxs-lookup"><span data-stu-id="3b76e-133">Value</span></span>



| <span data-ttu-id="3b76e-134">進入</span><span class="sxs-lookup"><span data-stu-id="3b76e-134">Entry</span></span> | <span data-ttu-id="3b76e-135">值</span><span class="sxs-lookup"><span data-stu-id="3b76e-135">Value</span></span> |
|----------------|---------------------------|
| <span data-ttu-id="3b76e-136">描述</span><span class="sxs-lookup"><span data-stu-id="3b76e-136">Description</span></span>    | <span data-ttu-id="3b76e-137">屬性的值。</span><span class="sxs-lookup"><span data-stu-id="3b76e-137">A value for the property.</span></span> |
| <span data-ttu-id="3b76e-138">Access</span><span class="sxs-lookup"><span data-stu-id="3b76e-138">Access</span></span>         | <span data-ttu-id="3b76e-139">讀寫</span><span class="sxs-lookup"><span data-stu-id="3b76e-139">ReadWrite</span></span>                 |
| <span data-ttu-id="3b76e-140">類型</span><span class="sxs-lookup"><span data-stu-id="3b76e-140">Type</span></span>           | <span data-ttu-id="3b76e-141">Variant</span><span class="sxs-lookup"><span data-stu-id="3b76e-141">Variant</span></span>                   |
| <span data-ttu-id="3b76e-142">預設</span><span class="sxs-lookup"><span data-stu-id="3b76e-142">Default</span></span>        | <span data-ttu-id="3b76e-143">N/A</span><span class="sxs-lookup"><span data-stu-id="3b76e-143">N/A</span></span>                       |
| <span data-ttu-id="3b76e-144">最小系統</span><span class="sxs-lookup"><span data-stu-id="3b76e-144">Minimum system</span></span> | <span data-ttu-id="3b76e-145">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3b76e-145">Windows 2000</span></span>              |



 

## <a name="see-also"></a><span data-ttu-id="3b76e-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b76e-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b76e-147">COM + 系統管理集合</span><span class="sxs-lookup"><span data-stu-id="3b76e-147">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 

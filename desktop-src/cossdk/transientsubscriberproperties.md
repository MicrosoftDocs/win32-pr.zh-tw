---
description: 包含父 TransientSubscriptions 集合之每個訂閱者屬性的物件。 您可以針對執行中的物件實例執行暫時的訂閱，並在物件終結時消失。
ms.assetid: b4f003b0-db9d-45f1-a57d-3e4d321289ca
title: TransientSubscriberProperties 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransientSubscriberProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: 17f89638efe232f2cdf06e1206f74a0df44601b2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970735"
---
# <a name="transientsubscriberproperties-collection"></a><span data-ttu-id="e96dd-104">TransientSubscriberProperties 集合</span><span class="sxs-lookup"><span data-stu-id="e96dd-104">TransientSubscriberProperties collection</span></span>

<span data-ttu-id="e96dd-105">包含父 [**TransientSubscriptions**](transientsubscriptions.md) 集合之每個訂閱者屬性的物件。</span><span class="sxs-lookup"><span data-stu-id="e96dd-105">Contains an object for each subscriber property for the parent [**TransientSubscriptions**](transientsubscriptions.md) collection.</span></span> <span data-ttu-id="e96dd-106">您可以針對執行中的物件實例執行暫時的訂閱，並在物件終結時消失。</span><span class="sxs-lookup"><span data-stu-id="e96dd-106">Transient subscriptions can be created on the fly for running object instances, and they vanish when the object is destroyed.</span></span>

<span data-ttu-id="e96dd-107">此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**加入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**移除**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。</span><span class="sxs-lookup"><span data-stu-id="e96dd-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="e96dd-108">成員</span><span class="sxs-lookup"><span data-stu-id="e96dd-108">Members</span></span>

<span data-ttu-id="e96dd-109">**TransientSubscriberProperties** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。</span><span class="sxs-lookup"><span data-stu-id="e96dd-109">The **TransientSubscriberProperties** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="e96dd-110">相關集合</span><span class="sxs-lookup"><span data-stu-id="e96dd-110">Related Collections</span></span>

<span data-ttu-id="e96dd-111">您可以從這個集合流覽至下列任何集合：</span><span class="sxs-lookup"><span data-stu-id="e96dd-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="e96dd-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="e96dd-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="e96dd-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="e96dd-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="e96dd-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="e96dd-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="e96dd-115">您可以從下列集合流覽至這個集合：</span><span class="sxs-lookup"><span data-stu-id="e96dd-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="e96dd-116">**TransientSubscriptions**</span><span class="sxs-lookup"><span data-stu-id="e96dd-116">**TransientSubscriptions**</span></span>](transientsubscriptions.md)

## <a name="properties"></a><span data-ttu-id="e96dd-117">屬性</span><span class="sxs-lookup"><span data-stu-id="e96dd-117">Properties</span></span>

<span data-ttu-id="e96dd-118">集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="e96dd-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="e96dd-119">名稱</span><span class="sxs-lookup"><span data-stu-id="e96dd-119">Name</span></span>](#name)
-   [<span data-ttu-id="e96dd-120">ReplTest1</span><span class="sxs-lookup"><span data-stu-id="e96dd-120">Value</span></span>](#value)

### <a name="name"></a><span data-ttu-id="e96dd-121">名稱</span><span class="sxs-lookup"><span data-stu-id="e96dd-121">Name</span></span>



| <span data-ttu-id="e96dd-122">進入</span><span class="sxs-lookup"><span data-stu-id="e96dd-122">Entry</span></span> | <span data-ttu-id="e96dd-123">值</span><span class="sxs-lookup"><span data-stu-id="e96dd-123">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e96dd-124">描述</span><span class="sxs-lookup"><span data-stu-id="e96dd-124">Description</span></span>    | <span data-ttu-id="e96dd-125">屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="e96dd-125">The name of the property.</span></span> <span data-ttu-id="e96dd-126">移除字串開頭和結尾的額外空間。當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 或 [**名稱**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="e96dd-126">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="e96dd-127">Access</span><span class="sxs-lookup"><span data-stu-id="e96dd-127">Access</span></span>         | <span data-ttu-id="e96dd-128">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="e96dd-128">WriteOnce</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="e96dd-129">類型</span><span class="sxs-lookup"><span data-stu-id="e96dd-129">Type</span></span>           | <span data-ttu-id="e96dd-130">String</span><span class="sxs-lookup"><span data-stu-id="e96dd-130">String</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="e96dd-131">預設值</span><span class="sxs-lookup"><span data-stu-id="e96dd-131">Default</span></span>        | <span data-ttu-id="e96dd-132">[新增屬性]</span><span class="sxs-lookup"><span data-stu-id="e96dd-132">"New Property"</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="e96dd-133">最小系統</span><span class="sxs-lookup"><span data-stu-id="e96dd-133">Minimum system</span></span> | <span data-ttu-id="e96dd-134">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="e96dd-134">Windows 2000</span></span>                                                                                                                                                                                                                                                           |



 

### <a name="value"></a><span data-ttu-id="e96dd-135">值</span><span class="sxs-lookup"><span data-stu-id="e96dd-135">Value</span></span>



| <span data-ttu-id="e96dd-136">進入</span><span class="sxs-lookup"><span data-stu-id="e96dd-136">Entry</span></span> | <span data-ttu-id="e96dd-137">值</span><span class="sxs-lookup"><span data-stu-id="e96dd-137">Value</span></span> |
|----------------|---------------------------|
| <span data-ttu-id="e96dd-138">描述</span><span class="sxs-lookup"><span data-stu-id="e96dd-138">Description</span></span>    | <span data-ttu-id="e96dd-139">屬性的值。</span><span class="sxs-lookup"><span data-stu-id="e96dd-139">A value for the property.</span></span> |
| <span data-ttu-id="e96dd-140">Access</span><span class="sxs-lookup"><span data-stu-id="e96dd-140">Access</span></span>         | <span data-ttu-id="e96dd-141">讀寫</span><span class="sxs-lookup"><span data-stu-id="e96dd-141">ReadWrite</span></span>                 |
| <span data-ttu-id="e96dd-142">類型</span><span class="sxs-lookup"><span data-stu-id="e96dd-142">Type</span></span>           | <span data-ttu-id="e96dd-143">Variant</span><span class="sxs-lookup"><span data-stu-id="e96dd-143">Variant</span></span>                   |
| <span data-ttu-id="e96dd-144">預設</span><span class="sxs-lookup"><span data-stu-id="e96dd-144">Default</span></span>        | <span data-ttu-id="e96dd-145">N/A</span><span class="sxs-lookup"><span data-stu-id="e96dd-145">N/A</span></span>                       |
| <span data-ttu-id="e96dd-146">最小系統</span><span class="sxs-lookup"><span data-stu-id="e96dd-146">Minimum system</span></span> | <span data-ttu-id="e96dd-147">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="e96dd-147">Windows 2000</span></span>              |



 

## <a name="see-also"></a><span data-ttu-id="e96dd-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e96dd-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e96dd-149">COM + 系統管理集合</span><span class="sxs-lookup"><span data-stu-id="e96dd-149">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 

---
description: 抓取與所呼叫之集合相關的其他集合相關資訊。
ms.assetid: daea5b23-6a13-46f4-89c8-0d93b614311e
title: RelatedCollectionInfo 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RelatedCollectionInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: 21a9a1905d75c81d605f30a3f6cffced8837034d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187710"
---
# <a name="relatedcollectioninfo-collection"></a><span data-ttu-id="2c0a6-103">RelatedCollectionInfo 集合</span><span class="sxs-lookup"><span data-stu-id="2c0a6-103">RelatedCollectionInfo collection</span></span>

<span data-ttu-id="2c0a6-104">抓取與所呼叫之集合相關的其他集合相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2c0a6-104">Retrieves information about other collections related to the collection from which it is called.</span></span> <span data-ttu-id="2c0a6-105">您可以使用 [**>getcollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection)方法，從任何 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件存取 **RelatedCollectionInfo** 集合。</span><span class="sxs-lookup"><span data-stu-id="2c0a6-105">The **RelatedCollectionInfo** collection is accessible from any [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object by using the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) method.</span></span> <span data-ttu-id="2c0a6-106">**RelatedCollectionInfo** 集合針對可從原創組合存取的每個集合，各包含一個物件。</span><span class="sxs-lookup"><span data-stu-id="2c0a6-106">The **RelatedCollectionInfo** collection contains one object for each collection that is accessible from the original collection.</span></span> <span data-ttu-id="2c0a6-107">相關的集合會遵循「元件服務」系統管理工具集合階層。</span><span class="sxs-lookup"><span data-stu-id="2c0a6-107">Related collections follow the Component Services administration tool collection hierarchy.</span></span>

<span data-ttu-id="2c0a6-108">此集合不支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。</span><span class="sxs-lookup"><span data-stu-id="2c0a6-108">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="2c0a6-109">成員</span><span class="sxs-lookup"><span data-stu-id="2c0a6-109">Members</span></span>

<span data-ttu-id="2c0a6-110">**RelatedCollectionInfo** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。</span><span class="sxs-lookup"><span data-stu-id="2c0a6-110">The **RelatedCollectionInfo** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="2c0a6-111">相關集合</span><span class="sxs-lookup"><span data-stu-id="2c0a6-111">Related Collections</span></span>

<span data-ttu-id="2c0a6-112">您可以從這個集合流覽至下列任何集合：</span><span class="sxs-lookup"><span data-stu-id="2c0a6-112">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="2c0a6-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="2c0a6-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   <span data-ttu-id="2c0a6-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="2c0a6-114">**RelatedCollectionInfo**</span></span>

<span data-ttu-id="2c0a6-115">您可以從每個集合流覽至這個集合。</span><span class="sxs-lookup"><span data-stu-id="2c0a6-115">You can navigate to this collection from every collection.</span></span>

## <a name="properties"></a><span data-ttu-id="2c0a6-116">屬性</span><span class="sxs-lookup"><span data-stu-id="2c0a6-116">Properties</span></span>

<span data-ttu-id="2c0a6-117">集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="2c0a6-117">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="2c0a6-118">名稱</span><span class="sxs-lookup"><span data-stu-id="2c0a6-118">Name</span></span>](#name)

### <a name="name"></a><span data-ttu-id="2c0a6-119">Name</span><span class="sxs-lookup"><span data-stu-id="2c0a6-119">Name</span></span>



| <span data-ttu-id="2c0a6-120">進入</span><span class="sxs-lookup"><span data-stu-id="2c0a6-120">Entry</span></span> | <span data-ttu-id="2c0a6-121">值</span><span class="sxs-lookup"><span data-stu-id="2c0a6-121">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c0a6-122">描述</span><span class="sxs-lookup"><span data-stu-id="2c0a6-122">Description</span></span>    | <span data-ttu-id="2c0a6-123">相關集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c0a6-123">The name of the related collection.</span></span> <span data-ttu-id="2c0a6-124">當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 或 [**名稱**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="2c0a6-124">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="2c0a6-125">Access</span><span class="sxs-lookup"><span data-stu-id="2c0a6-125">Access</span></span>         | <span data-ttu-id="2c0a6-126">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="2c0a6-126">ReadOnly</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="2c0a6-127">類型</span><span class="sxs-lookup"><span data-stu-id="2c0a6-127">Type</span></span>           | <span data-ttu-id="2c0a6-128">String</span><span class="sxs-lookup"><span data-stu-id="2c0a6-128">String</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="2c0a6-129">預設</span><span class="sxs-lookup"><span data-stu-id="2c0a6-129">Default</span></span>        | <span data-ttu-id="2c0a6-130">None</span><span class="sxs-lookup"><span data-stu-id="2c0a6-130">None</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="2c0a6-131">最小系統</span><span class="sxs-lookup"><span data-stu-id="2c0a6-131">Minimum system</span></span> | <span data-ttu-id="2c0a6-132">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="2c0a6-132">Windows 2000</span></span>                                                                                                                                                                                               |



 

## <a name="see-also"></a><span data-ttu-id="2c0a6-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c0a6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c0a6-134">COM + 系統管理集合</span><span class="sxs-lookup"><span data-stu-id="2c0a6-134">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 

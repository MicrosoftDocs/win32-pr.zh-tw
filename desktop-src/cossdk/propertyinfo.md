---
description: 抓取指定集合所支援之屬性的相關資訊。
ms.assetid: 5e3963c0-6769-4b5b-8636-2d8c98a8776b
title: PropertyInfo 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PropertyInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: bd9fdd2262d4499efd6a86fbc5b99bae786016f3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110904"
---
# <a name="propertyinfo-collection"></a><span data-ttu-id="782fd-103">PropertyInfo 集合</span><span class="sxs-lookup"><span data-stu-id="782fd-103">PropertyInfo collection</span></span>

<span data-ttu-id="782fd-104">抓取指定集合所支援之屬性的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="782fd-104">Retrieves information about the properties that a specified collection supports.</span></span> <span data-ttu-id="782fd-105">您可以使用 [**>getcollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection)方法，從任何 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件存取 **PropertyInfo** 集合。</span><span class="sxs-lookup"><span data-stu-id="782fd-105">The **PropertyInfo** collection is accessible from any [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object by using the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) method.</span></span> <span data-ttu-id="782fd-106">**PropertyInfo** 集合會針對原創組合所支援的每個屬性，各包含一個物件。</span><span class="sxs-lookup"><span data-stu-id="782fd-106">The **PropertyInfo** collection contains one object for each property that is supported by the original collection.</span></span>

## <a name="members"></a><span data-ttu-id="782fd-107">成員</span><span class="sxs-lookup"><span data-stu-id="782fd-107">Members</span></span>

<span data-ttu-id="782fd-108">**PropertyInfo** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。</span><span class="sxs-lookup"><span data-stu-id="782fd-108">The **PropertyInfo** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="782fd-109">相關集合</span><span class="sxs-lookup"><span data-stu-id="782fd-109">Related Collections</span></span>

<span data-ttu-id="782fd-110">您可以從這個集合流覽至下列任何集合：</span><span class="sxs-lookup"><span data-stu-id="782fd-110">You can navigate from this collection to any of the following collections:</span></span>

-   <span data-ttu-id="782fd-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="782fd-111">**PropertyInfo**</span></span>
-   [<span data-ttu-id="782fd-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="782fd-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="782fd-113">您可以從每個集合流覽至這個集合。</span><span class="sxs-lookup"><span data-stu-id="782fd-113">You can navigate to this collection from every collection.</span></span>

## <a name="properties"></a><span data-ttu-id="782fd-114">屬性</span><span class="sxs-lookup"><span data-stu-id="782fd-114">Properties</span></span>

<span data-ttu-id="782fd-115">集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="782fd-115">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="782fd-116">名稱</span><span class="sxs-lookup"><span data-stu-id="782fd-116">Name</span></span>](#name)

### <a name="name"></a><span data-ttu-id="782fd-117">Name</span><span class="sxs-lookup"><span data-stu-id="782fd-117">Name</span></span>



| <span data-ttu-id="782fd-118">進入</span><span class="sxs-lookup"><span data-stu-id="782fd-118">Entry</span></span> | <span data-ttu-id="782fd-119">值</span><span class="sxs-lookup"><span data-stu-id="782fd-119">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="782fd-120">描述</span><span class="sxs-lookup"><span data-stu-id="782fd-120">Description</span></span>    | <span data-ttu-id="782fd-121">屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="782fd-121">The name of the property.</span></span> <span data-ttu-id="782fd-122">當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 或 [**名稱**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="782fd-122">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="782fd-123">Access</span><span class="sxs-lookup"><span data-stu-id="782fd-123">Access</span></span>         | <span data-ttu-id="782fd-124">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="782fd-124">ReadOnly</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="782fd-125">類型</span><span class="sxs-lookup"><span data-stu-id="782fd-125">Type</span></span>           | <span data-ttu-id="782fd-126">String</span><span class="sxs-lookup"><span data-stu-id="782fd-126">String</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="782fd-127">預設</span><span class="sxs-lookup"><span data-stu-id="782fd-127">Default</span></span>        | <span data-ttu-id="782fd-128">None</span><span class="sxs-lookup"><span data-stu-id="782fd-128">None</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="782fd-129">最小系統</span><span class="sxs-lookup"><span data-stu-id="782fd-129">Minimum system</span></span> | <span data-ttu-id="782fd-130">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="782fd-130">Windows 2000</span></span>                                                                                                                                                                                     |



 

## <a name="see-also"></a><span data-ttu-id="782fd-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="782fd-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="782fd-132">COM + 系統管理集合</span><span class="sxs-lookup"><span data-stu-id="782fd-132">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 

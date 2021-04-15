---
description: 包含 [元件服務] 系統管理工具的 [電腦] 資料夾中的電腦清單。 它包含每一部電腦的物件。
ms.assetid: 56e32b47-a9f5-4888-b727-71ad0499da00
title: ComputerList 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ComputerList
api_type:
- COM
api_location: ''
ms.openlocfilehash: 379e5e07a86d06961de3f8f3936a260451bf43ae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468197"
---
# <a name="computerlist-collection"></a><span data-ttu-id="a990f-104">ComputerList 集合</span><span class="sxs-lookup"><span data-stu-id="a990f-104">ComputerList collection</span></span>

<span data-ttu-id="a990f-105">包含 [元件服務] 系統管理工具的 [ **電腦** ] 資料夾中的電腦清單。</span><span class="sxs-lookup"><span data-stu-id="a990f-105">Contains a list of the computers in the **Computers** folder of the Component Services administration tool.</span></span> <span data-ttu-id="a990f-106">它包含每一部電腦的物件。</span><span class="sxs-lookup"><span data-stu-id="a990f-106">It contains an object for each computer.</span></span>

<span data-ttu-id="a990f-107">此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**加入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**移除**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。</span><span class="sxs-lookup"><span data-stu-id="a990f-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="a990f-108">成員</span><span class="sxs-lookup"><span data-stu-id="a990f-108">Members</span></span>

<span data-ttu-id="a990f-109">**ComputerList** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。</span><span class="sxs-lookup"><span data-stu-id="a990f-109">The **ComputerList** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="a990f-110">相關集合</span><span class="sxs-lookup"><span data-stu-id="a990f-110">Related Collections</span></span>

<span data-ttu-id="a990f-111">您可以從這個集合流覽至下列任何集合：</span><span class="sxs-lookup"><span data-stu-id="a990f-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="a990f-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="a990f-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="a990f-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="a990f-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="a990f-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="a990f-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="a990f-115">您可以從下列集合流覽至這個集合：</span><span class="sxs-lookup"><span data-stu-id="a990f-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="a990f-116">**根**</span><span class="sxs-lookup"><span data-stu-id="a990f-116">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="a990f-117">屬性</span><span class="sxs-lookup"><span data-stu-id="a990f-117">Properties</span></span>

<span data-ttu-id="a990f-118">集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="a990f-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="a990f-119">名稱</span><span class="sxs-lookup"><span data-stu-id="a990f-119">Name</span></span>](#name)

### <a name="name"></a><span data-ttu-id="a990f-120">Name</span><span class="sxs-lookup"><span data-stu-id="a990f-120">Name</span></span>



| <span data-ttu-id="a990f-121">進入</span><span class="sxs-lookup"><span data-stu-id="a990f-121">Entry</span></span> | <span data-ttu-id="a990f-122">值</span><span class="sxs-lookup"><span data-stu-id="a990f-122">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a990f-123">描述</span><span class="sxs-lookup"><span data-stu-id="a990f-123">Description</span></span>    | <span data-ttu-id="a990f-124">電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="a990f-124">The name of the computer.</span></span> <span data-ttu-id="a990f-125">移除字串開頭和結尾的額外空間。當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 或 [**名稱**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="a990f-125">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="a990f-126">Access</span><span class="sxs-lookup"><span data-stu-id="a990f-126">Access</span></span>         | <span data-ttu-id="a990f-127">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="a990f-127">WriteOnce</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="a990f-128">類型</span><span class="sxs-lookup"><span data-stu-id="a990f-128">Type</span></span>           | <span data-ttu-id="a990f-129">String</span><span class="sxs-lookup"><span data-stu-id="a990f-129">String</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="a990f-130">預設值</span><span class="sxs-lookup"><span data-stu-id="a990f-130">Default</span></span>        | <span data-ttu-id="a990f-131">「新增電腦」</span><span class="sxs-lookup"><span data-stu-id="a990f-131">"New Computer"</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="a990f-132">最小系統</span><span class="sxs-lookup"><span data-stu-id="a990f-132">Minimum system</span></span> | <span data-ttu-id="a990f-133">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a990f-133">Windows 2000</span></span>                                                                                                                                                                                                                                                           |



 

## <a name="see-also"></a><span data-ttu-id="a990f-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a990f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a990f-135">COM + 系統管理集合</span><span class="sxs-lookup"><span data-stu-id="a990f-135">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 

---
description: 包含應用程式叢集中的伺服器電腦清單。 它包含每一部伺服器的物件。
ms.assetid: 8722080a-cf95-4c29-9eb7-99c6df93611f
title: ApplicationCluster 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplicationCluster
api_type:
- COM
api_location: ''
ms.openlocfilehash: 00a54f5c79bcbaf4ef61b130db556fc27f264101
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110565"
---
# <a name="applicationcluster-collection"></a><span data-ttu-id="cb0be-104">ApplicationCluster 集合</span><span class="sxs-lookup"><span data-stu-id="cb0be-104">ApplicationCluster collection</span></span>

<span data-ttu-id="cb0be-105">包含應用程式叢集中的伺服器電腦清單。</span><span class="sxs-lookup"><span data-stu-id="cb0be-105">Contains a list of the server computers in the application cluster.</span></span> <span data-ttu-id="cb0be-106">它包含每一部伺服器的物件。</span><span class="sxs-lookup"><span data-stu-id="cb0be-106">It contains an object for each server.</span></span> <span data-ttu-id="cb0be-107">這是最上層集合。</span><span class="sxs-lookup"><span data-stu-id="cb0be-107">This is a top-level collection.</span></span>

<span data-ttu-id="cb0be-108">應用程式叢集是針對 (CLB) 服務的元件負載平衡而定義的。</span><span class="sxs-lookup"><span data-stu-id="cb0be-108">The application cluster is defined for purposes of the component load balancing (CLB) service.</span></span> <span data-ttu-id="cb0be-109">針對要使用的應用程式叢集集合，必須在電腦上安裝 CLB 服務。</span><span class="sxs-lookup"><span data-stu-id="cb0be-109">For the application cluster collection to be used, the CLB service must be installed on the computer.</span></span>

<span data-ttu-id="cb0be-110">您可以使用 [**LocalComputer**](localcomputer.md) 集合物件上的 IsRouter 屬性，指定應用程式叢集中的路由器，然後指定指定的元件應該與 [**元件**](components.md) 集合物件上的 LoadBalancingSupported 屬性進行負載平衡。</span><span class="sxs-lookup"><span data-stu-id="cb0be-110">You designate a router in the application cluster with the IsRouter property on the [**LocalComputer**](localcomputer.md) collection object, and you designate that a given component should be load balanced with the LoadBalancingSupported property on a [**Components**](components.md) collection object.</span></span>

<span data-ttu-id="cb0be-111">此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**加入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**移除**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。</span><span class="sxs-lookup"><span data-stu-id="cb0be-111">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="cb0be-112">成員</span><span class="sxs-lookup"><span data-stu-id="cb0be-112">Members</span></span>

<span data-ttu-id="cb0be-113">**ApplicationCluster** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。</span><span class="sxs-lookup"><span data-stu-id="cb0be-113">The **ApplicationCluster** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="cb0be-114">相關集合</span><span class="sxs-lookup"><span data-stu-id="cb0be-114">Related Collections</span></span>

<span data-ttu-id="cb0be-115">您可以從這個集合流覽至下列任何集合：</span><span class="sxs-lookup"><span data-stu-id="cb0be-115">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="cb0be-116">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="cb0be-116">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="cb0be-117">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="cb0be-117">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="cb0be-118">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="cb0be-118">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="cb0be-119">您可以從下列集合流覽至這個集合：</span><span class="sxs-lookup"><span data-stu-id="cb0be-119">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="cb0be-120">**根**</span><span class="sxs-lookup"><span data-stu-id="cb0be-120">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="cb0be-121">屬性</span><span class="sxs-lookup"><span data-stu-id="cb0be-121">Properties</span></span>

<span data-ttu-id="cb0be-122">集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="cb0be-122">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="cb0be-123">名稱</span><span class="sxs-lookup"><span data-stu-id="cb0be-123">Name</span></span>](#name)

### <a name="name"></a><span data-ttu-id="cb0be-124">Name</span><span class="sxs-lookup"><span data-stu-id="cb0be-124">Name</span></span>



| <span data-ttu-id="cb0be-125">進入</span><span class="sxs-lookup"><span data-stu-id="cb0be-125">Entry</span></span> | <span data-ttu-id="cb0be-126">值</span><span class="sxs-lookup"><span data-stu-id="cb0be-126">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb0be-127">描述</span><span class="sxs-lookup"><span data-stu-id="cb0be-127">Description</span></span>    | <span data-ttu-id="cb0be-128">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb0be-128">The name of the server.</span></span> <span data-ttu-id="cb0be-129">移除字串開頭和結尾的額外空間。當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 或 [**名稱**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="cb0be-129">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="cb0be-130">Access</span><span class="sxs-lookup"><span data-stu-id="cb0be-130">Access</span></span>         | <span data-ttu-id="cb0be-131">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="cb0be-131">WriteOnce</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="cb0be-132">類型</span><span class="sxs-lookup"><span data-stu-id="cb0be-132">Type</span></span>           | <span data-ttu-id="cb0be-133">String</span><span class="sxs-lookup"><span data-stu-id="cb0be-133">String</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="cb0be-134">預設值</span><span class="sxs-lookup"><span data-stu-id="cb0be-134">Default</span></span>        | <span data-ttu-id="cb0be-135">「新增電腦」</span><span class="sxs-lookup"><span data-stu-id="cb0be-135">"New Computer"</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="cb0be-136">最小系統</span><span class="sxs-lookup"><span data-stu-id="cb0be-136">Minimum system</span></span> | <span data-ttu-id="cb0be-137">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="cb0be-137">Windows 2000</span></span>                                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a><span data-ttu-id="cb0be-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb0be-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb0be-139">COM + 系統管理集合</span><span class="sxs-lookup"><span data-stu-id="cb0be-139">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 

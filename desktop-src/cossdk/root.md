---
description: 包含目錄中的最上層集合。
ms.assetid: 6cd23e6a-53b8-42ec-97df-59281f019252
title: 根集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Root
api_type:
- COM
api_location: ''
ms.openlocfilehash: ad896c69ab6fad75179c9bb30668143aa2ea741e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000045"
---
# <a name="root-collection"></a><span data-ttu-id="2e012-103">根集合</span><span class="sxs-lookup"><span data-stu-id="2e012-103">Root collection</span></span>

<span data-ttu-id="2e012-104">包含目錄中的最上層集合。</span><span class="sxs-lookup"><span data-stu-id="2e012-104">Contains the top-level collections in the catalog.</span></span> <span data-ttu-id="2e012-105">它不包含任何 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件或支援任何屬性。</span><span class="sxs-lookup"><span data-stu-id="2e012-105">It does not contain any [**COMAdminCatalogObject**](comadmincatalogobject.md) objects or support any properties.</span></span>

<span data-ttu-id="2e012-106">**根** 集合不支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**加入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**移除**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。</span><span class="sxs-lookup"><span data-stu-id="2e012-106">The **Root** collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

<span data-ttu-id="2e012-107">您無法從任何集合流覽至 **根** 集合。</span><span class="sxs-lookup"><span data-stu-id="2e012-107">You cannot navigate to the **Root** collection from any collection.</span></span>

## <a name="members"></a><span data-ttu-id="2e012-108">成員</span><span class="sxs-lookup"><span data-stu-id="2e012-108">Members</span></span>

<span data-ttu-id="2e012-109">**根** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。</span><span class="sxs-lookup"><span data-stu-id="2e012-109">The **Root** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="2e012-110">相關集合</span><span class="sxs-lookup"><span data-stu-id="2e012-110">Related Collections</span></span>

<span data-ttu-id="2e012-111">以下是目錄中的最上層集合：</span><span class="sxs-lookup"><span data-stu-id="2e012-111">The following are the top-level collections in the catalog:</span></span>

-   [<span data-ttu-id="2e012-112">**ApplicationCluster**</span><span class="sxs-lookup"><span data-stu-id="2e012-112">**ApplicationCluster**</span></span>](applicationcluster.md)
-   [<span data-ttu-id="2e012-113">**ApplicationInstances**</span><span class="sxs-lookup"><span data-stu-id="2e012-113">**ApplicationInstances**</span></span>](applicationinstances.md)
-   [<span data-ttu-id="2e012-114">**應用程式**</span><span class="sxs-lookup"><span data-stu-id="2e012-114">**Applications**</span></span>](applications.md)
-   [<span data-ttu-id="2e012-115">**ComputerList**</span><span class="sxs-lookup"><span data-stu-id="2e012-115">**ComputerList**</span></span>](computerlist.md)
-   [<span data-ttu-id="2e012-116">**DCOMProtocols**</span><span class="sxs-lookup"><span data-stu-id="2e012-116">**DCOMProtocols**</span></span>](dcomprotocols.md)
-   [<span data-ttu-id="2e012-117">**EventClassesForIID**</span><span class="sxs-lookup"><span data-stu-id="2e012-117">**EventClassesForIID**</span></span>](eventclassesforiid.md)
-   [<span data-ttu-id="2e012-118">**FilesForImport**</span><span class="sxs-lookup"><span data-stu-id="2e012-118">**FilesForImport**</span></span>](filesforimport.md)
-   [<span data-ttu-id="2e012-119">**InprocServers**</span><span class="sxs-lookup"><span data-stu-id="2e012-119">**InprocServers**</span></span>](inprocservers.md)
-   [<span data-ttu-id="2e012-120">**LegacyServers**</span><span class="sxs-lookup"><span data-stu-id="2e012-120">**LegacyServers**</span></span>](legacyservers.md)
-   [<span data-ttu-id="2e012-121">**LocalComputer**</span><span class="sxs-lookup"><span data-stu-id="2e012-121">**LocalComputer**</span></span>](localcomputer.md)
-   [<span data-ttu-id="2e012-122">**分區**</span><span class="sxs-lookup"><span data-stu-id="2e012-122">**Partitions**</span></span>](partitions.md)
-   [<span data-ttu-id="2e012-123">**PartitionUsers**</span><span class="sxs-lookup"><span data-stu-id="2e012-123">**PartitionUsers**</span></span>](partitionusers.md)
-   [<span data-ttu-id="2e012-124">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="2e012-124">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="2e012-125">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="2e012-125">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="2e012-126">**TransientSubscriptions**</span><span class="sxs-lookup"><span data-stu-id="2e012-126">**TransientSubscriptions**</span></span>](transientsubscriptions.md)
-   [<span data-ttu-id="2e012-127">**WOWInprocServers**</span><span class="sxs-lookup"><span data-stu-id="2e012-127">**WOWInprocServers**</span></span>](wowinprocservers.md)
-   [<span data-ttu-id="2e012-128">**WOWLegacyServers**</span><span class="sxs-lookup"><span data-stu-id="2e012-128">**WOWLegacyServers**</span></span>](wowlegacyservers.md)

## <a name="see-also"></a><span data-ttu-id="2e012-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2e012-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e012-130">COM + 系統管理集合</span><span class="sxs-lookup"><span data-stu-id="2e012-130">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 

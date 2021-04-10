---
description: 查詢可用的屬性
ms.assetid: 9acf10cd-19a8-4542-8078-3e4ee275d4d5
title: 查詢可用的屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22238e04404d2b88efa81ce98d0b0fb0e09d245f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111285"
---
# <a name="querying-for-available-properties"></a><span data-ttu-id="1c66d-103">查詢可用的屬性</span><span class="sxs-lookup"><span data-stu-id="1c66d-103">Querying for Available Properties</span></span>

<span data-ttu-id="1c66d-104">如果您撰寫的是一般用途的系統管理工具，您很可能需要撰寫常式來設定完整的屬性（property）。</span><span class="sxs-lookup"><span data-stu-id="1c66d-104">If you are writing a general-purpose administration tool, you most likely will need to write routines for setting properties in full generality.</span></span> <span data-ttu-id="1c66d-105">為了支援此功能，有一項工具可讓您以動態方式查詢任何指定集合中的專案可用的屬性。</span><span class="sxs-lookup"><span data-stu-id="1c66d-105">To support this, there is a facility that enables you to dynamically query for the properties that are available for the items in any given collection.</span></span>

<span data-ttu-id="1c66d-106">您可能保留的任何集合都可以使用 [**PropertyInfo**](propertyinfo.md) 集合。</span><span class="sxs-lookup"><span data-stu-id="1c66d-106">The [**PropertyInfo**](propertyinfo.md) collection is available from any collection that you might be holding.</span></span> <span data-ttu-id="1c66d-107">**PropertyInfo** 集合包含每個可用屬性的專案。</span><span class="sxs-lookup"><span data-stu-id="1c66d-107">The **PropertyInfo** collection contains an item for each available property.</span></span> <span data-ttu-id="1c66d-108">您可以列舉這些專案，以判斷指定的屬性是否可用。</span><span class="sxs-lookup"><span data-stu-id="1c66d-108">You can enumerate through these items to determine whether a given property is available.</span></span>

<span data-ttu-id="1c66d-109">您可以使用 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件上的 [**>getcollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection)方法，從您持有的任何集合取得 [**PropertyInfo**](propertyinfo.md)集合，將第二個參數保留空白，您通常會在此指定父專案的索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="1c66d-109">You can get the [**PropertyInfo**](propertyinfo.md) collection from any collection you are holding by using the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) method on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, leaving the second parameter blank where you would normally specify a parent item's Key property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c66d-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="1c66d-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c66d-111">取得和設定屬性</span><span class="sxs-lookup"><span data-stu-id="1c66d-111">Getting and Setting Properties</span></span>](getting-and-setting-properties.md)
</dt> <dt>

[<span data-ttu-id="1c66d-112">屬性之間的相互相關性</span><span class="sxs-lookup"><span data-stu-id="1c66d-112">Interdependencies Between Properties</span></span>](interdependencies-between-properties.md)
</dt> <dt>

[<span data-ttu-id="1c66d-113">儲存或捨棄變更</span><span class="sxs-lookup"><span data-stu-id="1c66d-113">Saving or Discarding Changes</span></span>](saving-or-discarding-changes.md)
</dt> </dl>

 

 




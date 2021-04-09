---
title: 物件導覽屬性和方法
description: 用戶端會使用 IAccessible accNavigate 和 IAccessible accHitTest 等方法，從某個物件流覽至另一個物件。
ms.assetid: c6bcd044-bf70-4eec-92ae-66f9bd836c33
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e7645d5179015280fd40f6618722191e588c74a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932111"
---
# <a name="object-navigation-properties-and-methods"></a><span data-ttu-id="e538b-103">物件導覽屬性和方法</span><span class="sxs-lookup"><span data-stu-id="e538b-103">Object Navigation Properties and Methods</span></span>

<span data-ttu-id="e538b-104">用戶端會使用 [**IAccessible：： accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)和 [**IAccessible：： accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)之類的方法，從某個物件 *流覽* 至另一個物件。</span><span class="sxs-lookup"><span data-stu-id="e538b-104">Clients *navigate* from one object to another using methods such as [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) and [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest).</span></span> <span data-ttu-id="e538b-105">這些方法可讓用戶端取得子識別碼或另一個物件之 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面的位址。</span><span class="sxs-lookup"><span data-stu-id="e538b-105">These methods allow clients to retrieve either a child ID or the address of another object's [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="e538b-106">流覽可讓用戶端探索物件彼此之間的關係。</span><span class="sxs-lookup"><span data-stu-id="e538b-106">Navigation allows clients to explore how objects are related to each other.</span></span> <span data-ttu-id="e538b-107">請注意，流覽至另一個物件不會變更選取範圍或焦點。</span><span class="sxs-lookup"><span data-stu-id="e538b-107">Note that navigating to another object does not change the selection or focus.</span></span>

<span data-ttu-id="e538b-108">[**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)介面提供的屬性和方法支援下列類型的導覽：</span><span class="sxs-lookup"><span data-stu-id="e538b-108">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface provides properties and methods that support the following kinds of navigation:</span></span>

-   [<span data-ttu-id="e538b-109">階層式導覽</span><span class="sxs-lookup"><span data-stu-id="e538b-109">Hierarchical Navigation</span></span>](hierarchical-navigation.md)
-   [<span data-ttu-id="e538b-110">空間和邏輯導覽</span><span class="sxs-lookup"><span data-stu-id="e538b-110">Spatial and Logical Navigation</span></span>](spatial-and-logical-navigation.md)
-   [<span data-ttu-id="e538b-111">流覽點擊測試和螢幕位置</span><span class="sxs-lookup"><span data-stu-id="e538b-111">Navigation Through Hit Testing and Screen Location</span></span>](navigation-through-hit-testing-and-screen-location.md)

 

 





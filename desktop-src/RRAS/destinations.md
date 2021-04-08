---
title: 目的地
description: 路由表中的目的地是以網路位址和網路遮罩表示的網路專案。
ms.assetid: 115d86e3-f933-4601-af10-abaab287b509
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49c0c758720824284147c2f35be004622157edb3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840163"
---
# <a name="destinations"></a><span data-ttu-id="3ce1d-103">目的地</span><span class="sxs-lookup"><span data-stu-id="3ce1d-103">Destinations</span></span>

<span data-ttu-id="3ce1d-104">路由表中的目的地是以網路位址和網路遮罩表示的網路專案。</span><span class="sxs-lookup"><span data-stu-id="3ce1d-104">A destination in the routing table is a network entry represented by a network address and a network mask.</span></span>

<span data-ttu-id="3ce1d-105">路由表中的目的地專案包含：</span><span class="sxs-lookup"><span data-stu-id="3ce1d-105">A destination entry in the routing table includes:</span></span>

-   <span data-ttu-id="3ce1d-106">位址，以網路位址和網路遮罩表示。</span><span class="sxs-lookup"><span data-stu-id="3ce1d-106">The address, expressed as a network address and network mask.</span></span>
-   <span data-ttu-id="3ce1d-107">目的地的路由清單。</span><span class="sxs-lookup"><span data-stu-id="3ce1d-107">A list of routes to the destination.</span></span>
-   <span data-ttu-id="3ce1d-108">不透明指標位置的清單。</span><span class="sxs-lookup"><span data-stu-id="3ce1d-108">A list of opaque pointer slots.</span></span>
-   <span data-ttu-id="3ce1d-109">此目的地有效的視圖。</span><span class="sxs-lookup"><span data-stu-id="3ce1d-109">The views in which this destination is valid.</span></span> <span data-ttu-id="3ce1d-110">目的地包含每個包含下列資訊之視圖的結構：</span><span class="sxs-lookup"><span data-stu-id="3ce1d-110">The destination contains a structure for each view that contains the following information:</span></span>
    -   <span data-ttu-id="3ce1d-111">視圖的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3ce1d-111">An identifier for the view.</span></span>
    -   <span data-ttu-id="3ce1d-112">此視圖中目的地的最佳路由指標。</span><span class="sxs-lookup"><span data-stu-id="3ce1d-112">A pointer to the best route to the destination in this view.</span></span>
    -   <span data-ttu-id="3ce1d-113">此視圖中最佳路線的擁有者。</span><span class="sxs-lookup"><span data-stu-id="3ce1d-113">The owner of the best route in this view.</span></span>
    -   <span data-ttu-id="3ce1d-114">與此視圖中最佳路由相關聯的旗標。</span><span class="sxs-lookup"><span data-stu-id="3ce1d-114">Flags associated with the best route in this view.</span></span>
    -   <span data-ttu-id="3ce1d-115">此視圖中處於按住狀態的任何路由的控制碼。</span><span class="sxs-lookup"><span data-stu-id="3ce1d-115">Handle to any routes that are in a hold-down state in this view.</span></span>

 

 





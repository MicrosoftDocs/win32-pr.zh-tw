---
description: 通常視為比所有路由廣播更容易使用的網路，導向的廣播會將自己限制在您指定的區域網路。
ms.assetid: e2358580-5a65-434d-ba4c-a6b0615bccc3
title: 導向廣播
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f3a47bd47e9800e1f9c93cffa555b76feb77373
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970605"
---
# <a name="directed-broadcast"></a><span data-ttu-id="3e6c1-103">導向廣播</span><span class="sxs-lookup"><span data-stu-id="3e6c1-103">Directed Broadcast</span></span>

<span data-ttu-id="3e6c1-104">通常視為比所有路由廣播更容易使用的網路，導向的廣播會將自己限制在您指定的區域網路。</span><span class="sxs-lookup"><span data-stu-id="3e6c1-104">Generally considered more network friendly than an all-routes broadcast, a directed broadcast limits itself to the local network that you specify.</span></span> <span data-ttu-id="3e6c1-105">以二進位的網路編號和 **sa \_ nodenum** 填入 **sa \_ netnum** 。</span><span class="sxs-lookup"><span data-stu-id="3e6c1-105">Fill **sa\_netnum** with the target network number and **sa\_nodenum** with binary ones.</span></span> <span data-ttu-id="3e6c1-106">路由器會將此要求轉送到目的地網路，以作為本機廣播。</span><span class="sxs-lookup"><span data-stu-id="3e6c1-106">Routers forward this request to the destination network where it becomes a local broadcast.</span></span> <span data-ttu-id="3e6c1-107">中繼網路不會看到此封包為廣播。</span><span class="sxs-lookup"><span data-stu-id="3e6c1-107">Intermediate networks do not see this packet as a broadcast.</span></span>

 

 




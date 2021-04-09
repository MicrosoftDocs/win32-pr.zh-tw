---
title: 使用不透明的指標
description: 用戶端通常必須儲存其他用戶端特定的目的地相關資訊。
ms.assetid: e96805b0-680f-411c-a02c-2c3fda7276ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9893b3a8b8e8a69ab78f33156efbe872b86d83ca
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840416"
---
# <a name="using-opaque-pointers"></a><span data-ttu-id="1d4ad-103">使用不透明的指標</span><span class="sxs-lookup"><span data-stu-id="1d4ad-103">Using Opaque Pointers</span></span>

<span data-ttu-id="1d4ad-104">用戶端通常必須儲存其他用戶端特定的目的地相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1d4ad-104">Clients often must store additional, client-specific information about destinations.</span></span> <span data-ttu-id="1d4ad-105">路由表管理員可讓用戶端將此資訊儲存在路由表的目的地結構中。</span><span class="sxs-lookup"><span data-stu-id="1d4ad-105">The routing table manager enables clients to store this information in destination structures in the routing table.</span></span> <span data-ttu-id="1d4ad-106">您可以使用不 *透明的指標* 來儲存和取出資訊。</span><span class="sxs-lookup"><span data-stu-id="1d4ad-106">The information is stored and retrieved by using *opaque pointers*.</span></span> <span data-ttu-id="1d4ad-107">儲存的資訊是私用的，而且只有擁有不透明指標的用戶端才能存取。</span><span class="sxs-lookup"><span data-stu-id="1d4ad-107">The information stored is private, and accessible only to the client that owns the opaque pointer.</span></span>

<span data-ttu-id="1d4ad-108">例如，多播群組管理員會保留相依于特定目的地的多播轉送專案清單。</span><span class="sxs-lookup"><span data-stu-id="1d4ad-108">For example, the multicast group manager keeps a list of multicast forwarding entries that are dependent on a particular destination.</span></span> <span data-ttu-id="1d4ad-109">多播群組管理員會在該目的地中使用不透明的指標。</span><span class="sxs-lookup"><span data-stu-id="1d4ad-109">The multicast group manager uses an opaque pointer in that destination.</span></span> <span data-ttu-id="1d4ad-110">在另一個範例中，通告特定目的地的路由通訊協定可以使用不透明的指標，來保存其本身的路由公告相關資訊，即使它沒有最佳路由也一樣。</span><span class="sxs-lookup"><span data-stu-id="1d4ad-110">In another example, a routing protocol that advertises a particular destination can keep information related to its own route advertisement of the destination using an opaque pointer, even though it does not own the best route.</span></span>

<span data-ttu-id="1d4ad-111">不透明指標的數目有限;這些指標會先以先服務的基礎來配置給用戶端。</span><span class="sxs-lookup"><span data-stu-id="1d4ad-111">The number of opaque pointers is limited; these pointers are allocated to clients on a first-come, first-served basis.</span></span> <span data-ttu-id="1d4ad-112">路由器系統管理員必須在路由器設定期間配置正確的指標數目;因此，路由通訊協定和其他用戶端必須記錄其使用不透明指標。</span><span class="sxs-lookup"><span data-stu-id="1d4ad-112">The router administrator must allocate the correct number of pointers during the router configuration; therefore, routing protocols and other clients must document their use of opaque pointers.</span></span>

 

 





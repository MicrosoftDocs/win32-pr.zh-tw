---
description: 對等群組和圖形基礎結構會使用雲端。
ms.assetid: 01327211-0461-4922-925e-67bebe3e6158
title: 雲端
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 743d668387c78b3c22e49e98585494a36506cc74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115580"
---
# <a name="clouds"></a><span data-ttu-id="e1353-103">雲端</span><span class="sxs-lookup"><span data-stu-id="e1353-103">Clouds</span></span>

<span data-ttu-id="e1353-104">對等 [群組](grouping-api.md) 和 [圖形](graphing-api.md) 基礎結構會使用雲端。</span><span class="sxs-lookup"><span data-stu-id="e1353-104">Clouds are used by the Peer [Grouping](grouping-api.md) and [Graphing](graphing-api.md) Infrastructures.</span></span> <span data-ttu-id="e1353-105">[對等名稱解析通訊協定 (PNRP) ](pnrp-namespace-provider-api.md)將雲端識別為可在相同 IPv6 範圍內進行通訊的一組對等。</span><span class="sxs-lookup"><span data-stu-id="e1353-105">The [Peer Name Resolution Protocol (PNRP)](pnrp-namespace-provider-api.md) identifies a cloud as a set of peers that can communicate within the same IPv6 scope.</span></span> <span data-ttu-id="e1353-106">雲端與 IPv6 範圍密切相關。</span><span class="sxs-lookup"><span data-stu-id="e1353-106">Clouds are closely related to the IPv6 scopes.</span></span> <span data-ttu-id="e1353-107">下列清單指出一些獨特的雲端功能：</span><span class="sxs-lookup"><span data-stu-id="e1353-107">The following list identifies some of the unique cloud features:</span></span>

-   <span data-ttu-id="e1353-108">雲端是以名稱來識別，而可用的雲端則可以使用 [**WSALookupServiceBegin**](pnrp-and-wsalookupservicebegin.md)來列舉。</span><span class="sxs-lookup"><span data-stu-id="e1353-108">A cloud is identified by a name, and available clouds can be enumerated by using [**WSALookupServiceBegin**](pnrp-and-wsalookupservicebegin.md).</span></span>
-   <span data-ttu-id="e1353-109">如果電腦已連線到網際網路，則它是全域雲端的一部分，以字串 "Global \_ " 識別。</span><span class="sxs-lookup"><span data-stu-id="e1353-109">If a computer is connected to the Internet, it is part of a global cloud, which is identified by the string "Global\_".</span></span>
-   <span data-ttu-id="e1353-110">如果電腦連線到一或多個區域網路 (LAN) ，則每個連結都可使用個別的雲端。</span><span class="sxs-lookup"><span data-stu-id="e1353-110">If a computer is connected to one or more local area networks (LAN), individual clouds are available for each link.</span></span>
-   <span data-ttu-id="e1353-111">您可以透過多個網路介面卡或使用虛擬私人網路 (VPN) ，將一部電腦連線到許多網路，這表示在許多雲端中都可以看到具有一個介面的電腦。</span><span class="sxs-lookup"><span data-stu-id="e1353-111">One computer can be connected to many networks by having multiple network adapters or by using a virtual private network (VPN), which means that a computer with one interface can be visible in many clouds.</span></span>
-   <span data-ttu-id="e1353-112">您可以使用 PNRP 來註冊和解析特定雲端中的對等名稱。</span><span class="sxs-lookup"><span data-stu-id="e1353-112">You can use PNRP to register and resolve peer names in a specific cloud.</span></span>

 

 




---
title: " (RRAS) 的介面"
description: 介面是與網路的邏輯連接。 每個介面都是由唯一索引來識別。 多播路由通訊協定 (例如 MOSPF) 處理所有類型的介面。
ms.assetid: 761a033c-b95e-46f0-948b-d0a60337390f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdd1e3988eac75bd465bf9a9b890f360f850a0d7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103933814"
---
# <a name="interface-rras"></a><span data-ttu-id="613df-105"> (RRAS) 的介面</span><span class="sxs-lookup"><span data-stu-id="613df-105">Interface (RRAS)</span></span>

<span data-ttu-id="613df-106">介面是與網路的邏輯連接。</span><span class="sxs-lookup"><span data-stu-id="613df-106">An interface is a logical connection to a network.</span></span> <span data-ttu-id="613df-107">每個介面都是由唯一索引來識別。</span><span class="sxs-lookup"><span data-stu-id="613df-107">Each interface is identified by a unique index.</span></span> <span data-ttu-id="613df-108">多播路由通訊協定 (例如 MOSPF) 處理所有類型的介面。</span><span class="sxs-lookup"><span data-stu-id="613df-108">Multicast routing protocols (such as MOSPF) deal with all types of interfaces similarly.</span></span>

<span data-ttu-id="613df-109">如果是 LAN 介面，介面會對應到電腦中的實際實體裝置， (LAN 介面卡) 。</span><span class="sxs-lookup"><span data-stu-id="613df-109">In the case of a LAN interface, the interface corresponds to an actual physical device in the computer (the LAN adapter).</span></span> <span data-ttu-id="613df-110">如果是 WAN 介面，則在建立連線時，介面會對應至埠。</span><span class="sxs-lookup"><span data-stu-id="613df-110">In the case of a WAN interface, the interface is mapped to a port when a connection is established.</span></span> <span data-ttu-id="613df-111">WAN 介面可以是以通道為基礎，而埠可能是虛擬私人網路 (VPN) 埠。</span><span class="sxs-lookup"><span data-stu-id="613df-111">WAN interfaces can be based on tunnels and the port could be a virtual private network (VPN) port.</span></span>

<span data-ttu-id="613df-112">Windows 2000 和更新版本的作業系統支援「點對 multipoint」介面。</span><span class="sxs-lookup"><span data-stu-id="613df-112">Windows 2000 and later operating systems support a "point-to-multipoint" interface.</span></span> <span data-ttu-id="613df-113">這種類型的介面可以視為共用單一終止點的點對點連結集合。</span><span class="sxs-lookup"><span data-stu-id="613df-113">This type of interface can be viewed as a collection of point-to-point links that share a single termination point.</span></span>

<span data-ttu-id="613df-114">若要在點對點介面中唯一識別確切的連結，MGM API 會使用介面識別碼的下一個躍點位址。</span><span class="sxs-lookup"><span data-stu-id="613df-114">To uniquely identify an exact link in a point-to-multipoint interface, the MGM API uses the next hop address of the interface ID.</span></span> <span data-ttu-id="613df-115">為了支援此識別，MGM API 會使用擴充的介面識別碼，其中包含 [下一個躍點](next-hop.md) 位址。</span><span class="sxs-lookup"><span data-stu-id="613df-115">To support this identification, the MGM API uses an extended interface ID, which includes a [next hop](next-hop.md) address.</span></span>

 

 





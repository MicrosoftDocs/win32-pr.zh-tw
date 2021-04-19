---
description: 本主題討論使用對等基礎結構時的特定程式設計考慮。
ms.assetid: 525b0625-ec13-4aba-a741-dbacff3587f9
title: 對等)  (程式設計考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89956cbdbbc8d2ed89226a490bbae505862ab18f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976899"
---
# <a name="programming-considerations-peer-to-peer"></a><span data-ttu-id="b88bc-103">對等)  (程式設計考慮</span><span class="sxs-lookup"><span data-stu-id="b88bc-103">Programming Considerations (Peer-to-Peer)</span></span>

<span data-ttu-id="b88bc-104">本主題討論使用對等基礎結構時的特定程式設計考慮。</span><span class="sxs-lookup"><span data-stu-id="b88bc-104">This topic discusses specific programming considerations when using the Peer Infrastructure.</span></span>

<span data-ttu-id="b88bc-105">使用對等基礎結構開發對等應用程式時，您必須考慮下列程式設計考慮：</span><span class="sxs-lookup"><span data-stu-id="b88bc-105">When using the Peer Infrastructure to develop peer applications, you must take the following programming considerations into account:</span></span>

-   <span data-ttu-id="b88bc-106">IPv6</span><span class="sxs-lookup"><span data-stu-id="b88bc-106">IPv6</span></span>

    <span data-ttu-id="b88bc-107">對等基礎結構需要安裝並啟動 IPv6，才能讓對等網路應用程式運作。</span><span class="sxs-lookup"><span data-stu-id="b88bc-107">The Peer Infrastructure requires that IPv6 be installed and started to enable peer networking applications to function.</span></span>

-   <span data-ttu-id="b88bc-108">防火牆埠</span><span class="sxs-lookup"><span data-stu-id="b88bc-108">Firewall Ports</span></span>

    <span data-ttu-id="b88bc-109">在網路上使用防火牆時 (例如 IPv6 網際網路連線防火牆) ，必須開啟特定埠，才能讓對等基礎結構運作。</span><span class="sxs-lookup"><span data-stu-id="b88bc-109">When a firewall is being used on a network (such as the IPv6 Internet Connection firewall), specific ports must be opened to allow the Peer Infrastructure to function.</span></span> <span data-ttu-id="b88bc-110">必須開啟下列埠：</span><span class="sxs-lookup"><span data-stu-id="b88bc-110">The following ports must be open:</span></span>

    <span data-ttu-id="b88bc-111">對等群組基礎結構的 TCP 通訊埠3587。</span><span class="sxs-lookup"><span data-stu-id="b88bc-111">TCP port 3587 for the Peer Grouping Infrastructure.</span></span>

    <span data-ttu-id="b88bc-112">適用于對等圖形基礎結構的 UDP 埠3540。</span><span class="sxs-lookup"><span data-stu-id="b88bc-112">UDP port 3540 for the Peer Graphing Infrastructure.</span></span>

    > [!Note]  
    > <span data-ttu-id="b88bc-113">在 TCP 上使用對等圖形基礎結構的應用程式在呼叫 [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten)時，會選擇自己的 tcp 通訊埠。</span><span class="sxs-lookup"><span data-stu-id="b88bc-113">Applications that use the Peer Graphing Infrastructure over TCP choose their own TCP port when calling [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten).</span></span>

     

-   <span data-ttu-id="b88bc-114">通訊端選項</span><span class="sxs-lookup"><span data-stu-id="b88bc-114">Socket Option</span></span>

    <span data-ttu-id="b88bc-115">嘗試直接連線到其他 IPv6 對等節點 (但未使用對等基礎結構) 時，請確定通訊端選項 [IPV6 \_ 保護 \_ 等級] 設為 [不 **\_ \_ 受限制] 的保護層** 級。</span><span class="sxs-lookup"><span data-stu-id="b88bc-115">When attempting to connect to other IPv6 peer nodes directly (without using the Peer Infrastructure), ensure that the socket option IPV6\_PROTECTION\_LEVEL is set to **PROTECTION\_LEVEL\_UNRESTRICTED**.</span></span>

-   <span data-ttu-id="b88bc-116">頻寬</span><span class="sxs-lookup"><span data-stu-id="b88bc-116">Bandwidth</span></span>

    <span data-ttu-id="b88bc-117">使用 PNRP 時，應用程式可以發行一個或多個可解析的 [對等名稱](peer-names.md) 。</span><span class="sxs-lookup"><span data-stu-id="b88bc-117">When using PNRP, an application can publish one or more [peer names](peer-names.md) that can be resolved.</span></span> <span data-ttu-id="b88bc-118">針對以 PNRP 註冊的每一個對等名稱，PNRP 用來發行對等名稱的網路頻寬會增加，並讓其他節點可以加以解析。</span><span class="sxs-lookup"><span data-stu-id="b88bc-118">For each peer name registered with PNRP, there is an increase in the network bandwidth that PNRP uses to publish the peer name, and keep it available to be resolved by other nodes.</span></span>

    <span data-ttu-id="b88bc-119">為了避免使用過多的頻寬，應用程式應該避免在電腦上註冊大量的對等名稱。</span><span class="sxs-lookup"><span data-stu-id="b88bc-119">To prevent using too much bandwidth, applications should avoid registering large numbers of peer names on a computer.</span></span> <span data-ttu-id="b88bc-120">例如，發行圖片的應用程式不應該為每張圖片建立對等名稱，但應該為發行圖片的服務建立一個對等名稱，並使用不同的通訊協定來讓用戶端查詢特定圖片的服務。</span><span class="sxs-lookup"><span data-stu-id="b88bc-120">For example, an application that publishes pictures should not create a peer name for each picture, but should create one peer name for the service that publishes pictures, and use a different protocol for clients to query the service for specific pictures.</span></span>

-   <span data-ttu-id="b88bc-121">對等名稱註冊</span><span class="sxs-lookup"><span data-stu-id="b88bc-121">Peer Name Registration</span></span>

    <span data-ttu-id="b88bc-122">有些應用程式可能需要在一部以上的電腦上註冊相同的 [對等名稱](peer-names.md) 。</span><span class="sxs-lookup"><span data-stu-id="b88bc-122">Some applications may be required to register the same [peer name](peer-names.md) on more than one computer.</span></span> <span data-ttu-id="b88bc-123">一般來說，如果對等名稱與使用一部以上電腦的人員相關聯，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="b88bc-123">Typically, this happens if a peer name is associated with a person who uses more than one computer.</span></span> <span data-ttu-id="b88bc-124">您可以用來在多部電腦上註冊相同對等名稱的方法之一，是為該人員建立對等群組，並從所有電腦連接到該群組。</span><span class="sxs-lookup"><span data-stu-id="b88bc-124">One method that you can use to register the same peer name on multiple computers is to create a peer group for the person, and connect to that group from all computers.</span></span> <span data-ttu-id="b88bc-125">另一種方法是在一部電腦上建立對等身分識別和對等名稱，從該電腦匯出對等身分識別，然後將其匯入到其他電腦上。</span><span class="sxs-lookup"><span data-stu-id="b88bc-125">Another method is to create a peer identity and peer name on one computer, export the peer identity from that computer, and import it on other computers.</span></span> <span data-ttu-id="b88bc-126">如此一來，就可以在所有已匯入對等身分識別的電腦上建立相同的安全對等名稱。</span><span class="sxs-lookup"><span data-stu-id="b88bc-126">This allows the same secure peer name to be created on all the computers that have imported the peer identity.</span></span>

 

 




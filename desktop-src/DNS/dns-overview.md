---
title: DNS 概觀
description: DNS 是一種業界標準的服務，用來在網際網路通訊協定上找出 (IP) 網路的電腦。
ms.assetid: 98ecf24b-8bd5-4a75-a487-8af3080e8987
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 470807a5775b022834a3ca2f0ee3f91db8bdd5de
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2021
ms.locfileid: "104196157"
---
# <a name="dns-overview"></a><span data-ttu-id="53993-103">DNS 概觀</span><span class="sxs-lookup"><span data-stu-id="53993-103">DNS Overview</span></span>

<span data-ttu-id="53993-104">DNS 是一種業界標準的服務，用來在網際網路通訊協定上找出 (IP) 網路的電腦。</span><span class="sxs-lookup"><span data-stu-id="53993-104">DNS is an industry-standard service used to locate computers on an Internet Protocol (IP)-based network.</span></span> <span data-ttu-id="53993-105">IP 網路（例如網際網路和 Windows 2000 網路）依賴以數位為基礎的位址，例如 207.46.131.137) 簡單以 ferry 整個網路中的資訊。</span><span class="sxs-lookup"><span data-stu-id="53993-105">IP networks, such as the Internet and Windows 2000 networks, rely on number-based addresses, such as 207.46.131.137 to ferry information throughout the network.</span></span> <span data-ttu-id="53993-106">網路使用者依賴以字元為基礎的名稱，例如 `www.microsoft.com` 。</span><span class="sxs-lookup"><span data-stu-id="53993-106">Network users rely on character-based names, such as `www.microsoft.com`.</span></span> <span data-ttu-id="53993-107">因此，您必須將字元或方便使用的位址轉譯 (`www.microsoft.com`) 到網路可辨識的 (207.46.131.137) 簡單) 數位位址。</span><span class="sxs-lookup"><span data-stu-id="53993-107">Therefore, it is necessary to translate character or user-friendly addresses (`www.microsoft.com`) into the number-based addresses (207.46.131.137) that the network can recognize.</span></span> <span data-ttu-id="53993-108">DNS 是 Windows 2000 中選擇的服務，用來找出資源並將其轉譯成對應的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="53993-108">DNS is the service of choice in Windows 2000 to locate resources and translate them into their corresponding IP addresses.</span></span>

<span data-ttu-id="53993-109">DNS 會使用資源記錄的特製化資料庫（通常稱為 Rr）來回應用戶端名稱解析查詢。</span><span class="sxs-lookup"><span data-stu-id="53993-109">DNS uses a specialized database of resource records, commonly referred to simply as RRs, to respond to client name-resolution queries.</span></span> <span data-ttu-id="53993-110">在 DNS 之前，網際網路上的名稱解析是透過 [*主機*](h-gly.md)檔案來達成，這是以手動方式建立的檔案，與 IP 位址相關聯的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="53993-110">Before DNS, name resolution on the Internet was achieved with [*hosts file*](h-gly.md), which are manually created files that associated host names with IP addresses.</span></span>

<span data-ttu-id="53993-111">當新的用戶端新增至網路時，系統管理員必須手動更新 hosts 檔案，然後將 (複寫) 該檔案複製到網路上的所有其他電腦，讓新的主機可以全部連線。</span><span class="sxs-lookup"><span data-stu-id="53993-111">When a new client was added to the network, an administrator had to manually update the hosts file and then copy (replicate) that file to all other computers on the network so that the new host could be reached by all.</span></span> <span data-ttu-id="53993-112">隨著網際網路的成長，這種形式的名稱解析顯然沒有足夠;管理密集，而且沒有 [*調整*](s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="53993-112">As the Internet grew, this form of name resolution was clearly insufficient; it was too management intensive, and it did not [*scale*](s-gly.md).</span></span> <span data-ttu-id="53993-113">Hosts 檔案變得更大，因為它使用了一般 [*命名空間*](f-gly.md) (另請參閱 [命名空間](name-space.md)) ，它無法進行分割，而且必須全部散發。</span><span class="sxs-lookup"><span data-stu-id="53993-113">The hosts file just got bigger, and because it used a [*flat name space*](f-gly.md) (see also [Name Space](name-space.md)), it could not be partitioned and had to be distributed in its entirety.</span></span> <span data-ttu-id="53993-114">解決方案是 DNS。</span><span class="sxs-lookup"><span data-stu-id="53993-114">The solution was DNS.</span></span>

-   <span data-ttu-id="53993-115">DNS 已將主機檔案的一般命名空間取代為 [*階層式命名空間*](h-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="53993-115">DNS replaced the hosts file's flat name space with a [*hierarchical name space*](h-gly.md).</span></span> <span data-ttu-id="53993-116">使用階層式命名空間時，可分割和散發主機名稱和 IP 位址的相關資訊;因此，可進行擴充性。</span><span class="sxs-lookup"><span data-stu-id="53993-116">With a hierarchical name space, information about host names and IP addresses can be partitioned and distributed; thus, scalability is achieved.</span></span> <span data-ttu-id="53993-117">例如，在虛構的 widgets.products.microsoft.com 網域中，可以分割名稱解析的責任，讓不同的伺服器可以針對命名空間的不同部分處理名稱解析：</span><span class="sxs-lookup"><span data-stu-id="53993-117">For example, in the fictional widgets.products.microsoft.com domain, responsibility for name resolution can be partitioned so that various servers can handle name resolution for different parts of the name space:</span></span>
    -   <span data-ttu-id="53993-118">一部伺服器可以負責解析第一個部分 (microsoft.com) ，然後可以將名稱解析要求轉送到階層中的下一個 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="53993-118">One server can be responsible for resolving the first part (microsoft.com), and can then forward the name-resolution request to the next DNS Server in the hierarchy.</span></span>
    -   <span data-ttu-id="53993-119">下一部 DNS 伺服器可以負責解析 (產品) 的下一個部分的命名空間。</span><span class="sxs-lookup"><span data-stu-id="53993-119">The next DNS Server can be responsible for resolving the next part of the name space (products).</span></span>
    -   <span data-ttu-id="53993-120">最後，您可以將要求轉送到第三部 DNS 伺服器，該伺服器負責解析名稱 (widget) 的最後部分。</span><span class="sxs-lookup"><span data-stu-id="53993-120">Finally, the request can be forwarded to a third DNS server that is responsible for resolving the last part of the name (widgets).</span></span>

<span data-ttu-id="53993-121">在階層式命名空間的每個部分中的 DNS 伺服器，都必須維護主機的資源記錄資料庫，但只限于階層中的部分。</span><span class="sxs-lookup"><span data-stu-id="53993-121">DNS Servers in each part of the hierarchical name space need to maintain a database of resource records for hosts, but only in their part of the hierarchy.</span></span> <span data-ttu-id="53993-122">因此，widgets.products.microsoft.com 的 products 部分中的伺服器 (或伺服器) 只針對階層式命名空間的 products 部分維護 Rr，而不是針對 microsoft.com 部分或命名空間的 widget 部分。</span><span class="sxs-lookup"><span data-stu-id="53993-122">Thus, the server (or servers) in the products part of widgets.products.microsoft.com maintain RRs for only the products part of the hierarchical name space — not for the microsoft.com part or the widgets part of the name space.</span></span>

 

 





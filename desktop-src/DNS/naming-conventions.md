---
title: 命名規範
description: 命名慣例共用常見的目標，以明確地將名稱解析為網路位址，通常是 IP 位址。 命名慣例之間的差異在於每個慣例解決名稱的不同方法。
ms.assetid: 1ec96d2d-bb5a-4938-88c2-4d2802a326cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2091123ed2bf1022910231cd08cb0e6cccae51a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021733"
---
# <a name="naming-conventions"></a><span data-ttu-id="b368c-104">命名規範</span><span class="sxs-lookup"><span data-stu-id="b368c-104">Naming Conventions</span></span>

<span data-ttu-id="b368c-105">命名慣例共用共同的目標：明確地將名稱解析為網路位址，通常是 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="b368c-105">Naming conventions share a common goal: to unambiguously resolve a name to a network address, generally an IP address.</span></span> <span data-ttu-id="b368c-106">命名慣例之間的差異在於每個慣例解決名稱的不同方法。</span><span class="sxs-lookup"><span data-stu-id="b368c-106">The difference between naming conventions lies in each convention's distinct approach to resolving names.</span></span>

<span data-ttu-id="b368c-107">下列命名慣例可用來識別各種系統名稱解析方法中的電腦，包括 Windows 2000 方法：</span><span class="sxs-lookup"><span data-stu-id="b368c-107">The following naming conventions are used to identify computers in various system name-resolution methods, including the Windows 2000 method:</span></span>

-   [<span data-ttu-id="b368c-108">電腦名稱</span><span class="sxs-lookup"><span data-stu-id="b368c-108">Computer name</span></span>](#computer-name)
-   [<span data-ttu-id="b368c-109">主機名稱</span><span class="sxs-lookup"><span data-stu-id="b368c-109">Host name</span></span>](#host-name)
-   [<span data-ttu-id="b368c-110"> (FQDN) 的完整功能變數名稱 </span><span class="sxs-lookup"><span data-stu-id="b368c-110">Fully qualified domain name (FQDN)</span></span>](#fully-qualified-domain-name)
-   [<span data-ttu-id="b368c-111">相對辨別名稱</span><span class="sxs-lookup"><span data-stu-id="b368c-111">Relative distinguished name</span></span>](#relative-distinguished-name)

## <a name="computer-name"></a><span data-ttu-id="b368c-112">電腦名稱</span><span class="sxs-lookup"><span data-stu-id="b368c-112">Computer Name</span></span>

<span data-ttu-id="b368c-113">在一般 NetBIOS 命名空間中，單一名稱會將電腦名稱稱明確解析為網路位址。</span><span class="sxs-lookup"><span data-stu-id="b368c-113">In the flat NetBIOS name space, a single name unambiguously resolves a computer name to a network address.</span></span> <span data-ttu-id="b368c-114">這是先前的 Windows 版本儲存在瀏覽器和主要瀏覽器清單中的名稱，可讓對等 Windows 網路流覽網路上 Windows 電腦上的資源。</span><span class="sxs-lookup"><span data-stu-id="b368c-114">This is the name that previous Windows versions stored in browser and master browser lists, enabling peer Windows networks to browse resources on networked Windows computers.</span></span> <span data-ttu-id="b368c-115">在此案例中，與電腦相關聯的詞彙是 *電腦名稱稱*。</span><span class="sxs-lookup"><span data-stu-id="b368c-115">In this scenario, the term associated with the computer was *computer name*.</span></span> <span data-ttu-id="b368c-116">電腦名稱稱的註冊相依于網路廣播 (和主要瀏覽器，這取決於稍後的 Windows 版本號碼或 Windows NT 使用方式所贏得的選舉或) 的組合。</span><span class="sxs-lookup"><span data-stu-id="b368c-116">Registration of the computer name depended on network broadcasts (and a master browser, determined by elections won by later Windows version numbers or Windows NT usage, or a combination).</span></span> <span data-ttu-id="b368c-117">這適用于小型、對等式的 Windows 網路，但網路即將成長超過使用廣播和簡單一般檔案的主要瀏覽器清單可以提供服務。</span><span class="sxs-lookup"><span data-stu-id="b368c-117">This was useful for small, peer-based Windows networks, but networks soon grew beyond what the use of broadcasts and simple flat-file master browser lists could service.</span></span>

## <a name="host-name"></a><span data-ttu-id="b368c-118">主機名稱</span><span class="sxs-lookup"><span data-stu-id="b368c-118">Host Name</span></span>

<span data-ttu-id="b368c-119">接下來，Windows Internet 命名服務 (WINS) ，它已啟用以 NetBIOS 為基礎之電腦名稱稱的動態和集中式存放庫，儲存在 WINS 伺服器上。</span><span class="sxs-lookup"><span data-stu-id="b368c-119">Next came the Windows Internet Naming Service (WINS), which enabled a dynamic and centralized repository of NetBIOS-based computer names stored on WINS servers.</span></span> <span data-ttu-id="b368c-120">這些存放庫可以為較大的網路提供服務。</span><span class="sxs-lookup"><span data-stu-id="b368c-120">These repositories could service a larger network.</span></span> <span data-ttu-id="b368c-121">透過這種開發，可將名稱解析查詢導向至 WINS 伺服器 (而不是廣播) ，而且可能會集中仲裁衝突。</span><span class="sxs-lookup"><span data-stu-id="b368c-121">With this development, name-resolution queries could be directed to a WINS server (rather than being broadcast) and conflicts could be centrally arbitrated.</span></span> <span data-ttu-id="b368c-122">使用 WINS 時，會保留「電腦名稱稱」這一詞，但「 *主機名稱* 」一詞也會出現，並與電腦名稱稱交換使用。</span><span class="sxs-lookup"><span data-stu-id="b368c-122">With WINS, the term computer name was retained, but the term *host name* also appeared and was used interchangeably with computer name.</span></span> <span data-ttu-id="b368c-123">在此期間，WINS 是 Windows 平臺的預設名稱解析程式，但 DNS 已取得較大型和較大型網路的熱門程度和激增。</span><span class="sxs-lookup"><span data-stu-id="b368c-123">At the time, WINS was the default name-resolver for Windows platforms, but DNS was gaining with the popularity and proliferation of larger and larger networks.</span></span>

<span data-ttu-id="b368c-124">網路成長，且 WINS 變得較不能處理日益成長的名稱數量。</span><span class="sxs-lookup"><span data-stu-id="b368c-124">Networks grew, and WINS became less capable of handling the growing volume of names.</span></span> <span data-ttu-id="b368c-125">WINS 用來處理名稱解析負載的減少功能不是因為解決所需的處理能力，而是為大量電腦產生唯一名稱的事實，就是不斷增加的管理負擔。</span><span class="sxs-lookup"><span data-stu-id="b368c-125">The decreasing capability of WINS to handle the name-resolution load was not due to the processing power required for resolution, but instead, to the fact that generating unique names for lots of computers became an ever-increasing management burden.</span></span>

## <a name="fully-qualified-domain-name"></a><span data-ttu-id="b368c-126">完整網域名稱</span><span class="sxs-lookup"><span data-stu-id="b368c-126">Fully Qualified Domain Name</span></span>

<span data-ttu-id="b368c-127">DNS 是較佳的解決方案;使用其階層式命名空間時，唯一電腦名稱稱的需求會隔離到指定的網域，讓電腦名稱稱（例如 *server1* ）存在於相同階層中的不同網域位置。</span><span class="sxs-lookup"><span data-stu-id="b368c-127">DNS is a better solution; with its hierarchical name space, the need for unique computer names is isolated to a given domain, enabling a computer name such as *server1* to exist in different domain locations in the same hierarchy.</span></span> <span data-ttu-id="b368c-128">由於具有在不同網域中具有相同主機名稱的功能，因此需要出現正確定址 DNS 階層的名稱。</span><span class="sxs-lookup"><span data-stu-id="b368c-128">With the capability to have the same host name in different domains, the necessity arose for a name that properly addressed the DNS hierarchy.</span></span> <span data-ttu-id="b368c-129">名稱必須包含不只是電腦名稱稱或主機名稱，也必須包含可在整個 DNS 階層內明確識別或完全符合該電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="b368c-129">The name had to include not only the computer name or host name, but also a name that could unambiguously identify, or fully qualify, that computer within the entire DNS hierarchy.</span></span> <span data-ttu-id="b368c-130">該名稱是 (FQDN) 的 [*完整功能變數名稱*](f-gly.md) ，例如 server1.widgets.microsoft.com。</span><span class="sxs-lookup"><span data-stu-id="b368c-130">That name is the [*fully qualified domain name*](f-gly.md) (FQDN) — for example, server1.widgets.microsoft.com.</span></span>

<span data-ttu-id="b368c-131">不過，在某些情況下，FQDN 的網域階層部分相當繁瑣，而指定電腦 (或任何其他 DNS 主機) （相對於需要主機所在的 DNS 網域）則為本機名稱。</span><span class="sxs-lookup"><span data-stu-id="b368c-131">However, in certain situations, the domain-hierarchy part of the FQDN is cumbersome and a local name for a given computer (or any other DNS host) that is relative to the DNS domain in which the host resides is needed.</span></span> <span data-ttu-id="b368c-132">該名稱是 [*相對的分辨名稱*](r-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="b368c-132">That name is the [*relative distinguished name*](r-gly.md).</span></span> <span data-ttu-id="b368c-133">相對分辨名稱只是 FQDN 中最左邊點左邊的單一主機名稱，因此 server1.widgets.microsoft.com 的 FQDN 會有 server1 作為其相對分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="b368c-133">The relative distinguished name is simply the single host name to the left of the leftmost dot in the FQDN, such that an FQDN of server1.widgets.microsoft.com has server1 as its relative distinguished name.</span></span>

## <a name="relative-distinguished-name"></a><span data-ttu-id="b368c-134">相對辨別名稱</span><span class="sxs-lookup"><span data-stu-id="b368c-134">Relative Distinguished Name</span></span>

<span data-ttu-id="b368c-135">DNS 不會在 NetBIOS 名稱的使用者上採用新的名稱或新的命名慣例，而是使用 (主機名稱) 的電腦名稱稱做為相對辨別名稱，並將 DNS 網域階層附加至該名稱以建立 FQDN。</span><span class="sxs-lookup"><span data-stu-id="b368c-135">Rather than imposing new names or new naming conventions on users of NetBIOS names, DNS simply uses the computer name (host name) as the relative distinguished name and appends the DNS domain hierarchy to that name to create the FQDN.</span></span> <span data-ttu-id="b368c-136">下圖說明如何識別電腦名稱稱 (或主機名稱，或) 部分 FQDN 的相對辨別名稱：</span><span class="sxs-lookup"><span data-stu-id="b368c-136">The following figure illustrates how to identify the computer-name (or host-name, or relative distinguished name) part of the FQDN:</span></span>

![rdn 和 dns 網域階層合併以建立 fqdn](images/fqdn.png)

 

 





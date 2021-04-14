---
description: 本節說明將 IPv6 廣播應用程式移植到 Windows 通訊端所提供的多播功能的最佳作法。
ms.assetid: 12e491fd-650f-43b4-afa1-9f37b1c30240
title: 將廣播應用程式移植至 IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9f7dce09db6822a6f9b0a61873ca6bbff5a256b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469045"
---
# <a name="porting-broadcast-applications-to-ipv6"></a><span data-ttu-id="9cd54-103">將廣播應用程式移植至 IPv6</span><span class="sxs-lookup"><span data-stu-id="9cd54-103">Porting Broadcast Applications to IPv6</span></span>

<span data-ttu-id="9cd54-104">本節說明將 IPv6 廣播應用程式移植到 Windows 通訊端所提供的多播功能的最佳作法。</span><span class="sxs-lookup"><span data-stu-id="9cd54-104">This section describes best practices for porting an IPv6 broadcast application to the multicast capabilities available with Windows Sockets.</span></span>

## <a name="comparing-ipv4-to-ipv6"></a><span data-ttu-id="9cd54-105">比較 IPv4 與 IPv6</span><span class="sxs-lookup"><span data-stu-id="9cd54-105">Comparing IPv4 to IPv6</span></span>

<span data-ttu-id="9cd54-106">準備將 IPv4 廣播應用程式移植到 IPv6 時，最顯著的考慮是： IPv6 沒有任何已實行的廣播概念。</span><span class="sxs-lookup"><span data-stu-id="9cd54-106">The most notable consideration when preparing to port an IPv4 broadcast application to IPv6 is this: IPv6 has no implemented concept of broadcast.</span></span> <span data-ttu-id="9cd54-107">IPv6 會改為使用多播。</span><span class="sxs-lookup"><span data-stu-id="9cd54-107">Instead, IPv6 uses multicast.</span></span>

<span data-ttu-id="9cd54-108">IPv6 的多播可以模擬在 IPv4 中找到的傳統廣播功能。</span><span class="sxs-lookup"><span data-stu-id="9cd54-108">Multicast for IPv6 can emulate traditional broadcast capabilities found in IPv4.</span></span> <span data-ttu-id="9cd54-109">設定 [ipv6 \_ 新增 \_ 成員資格](ipproto-ipv6-socket-options.md) 通訊端選項，將 ipv6 位址設定為連結-本機範圍的所有節點位址 (FF02：： 1) 相當於使用 [ [SO \_ 廣播](socket-options.md) 通訊端] 選項來廣播 IPv4 廣播位址。</span><span class="sxs-lookup"><span data-stu-id="9cd54-109">Setting the [IPV6\_ADD\_MEMBERSHIP](ipproto-ipv6-socket-options.md) socket option with the IPv6 address set to the link-local scope all nodes address (FF02::1) is equivalent to broadcasting on IPv4 broadcast addresses using the [SO\_BROADCAST](socket-options.md) socket option.</span></span> <span data-ttu-id="9cd54-110">此位址有時稱為 *全部節點多播群組*。</span><span class="sxs-lookup"><span data-stu-id="9cd54-110">This address is sometimes called the *all-nodes multicast group*.</span></span> <span data-ttu-id="9cd54-111">針對只想要廣播模擬 IPv6 的應用程式，該方法的運作方式相當。</span><span class="sxs-lookup"><span data-stu-id="9cd54-111">For applications that simply want broadcast emulation for IPv6, that approach is operationally equivalent.</span></span> <span data-ttu-id="9cd54-112">但是 IPv6 有一個值得注意的差異，就是預設不會收到所有節點多播群組位址上的多播 (預設會收到 IPv4 廣播) 。</span><span class="sxs-lookup"><span data-stu-id="9cd54-112">One notable difference with IPv6, however, is that multicasts on the all-nodes multicast group address are not received by default (IPv4 broadcasts are received by default).</span></span> <span data-ttu-id="9cd54-113">應用程式設計人員必須使用 IPV6 \_ 新增 \_ 成員資格通訊端選項，以啟用來自任何來源的多播接收，包括所有節點的多播群組位址。</span><span class="sxs-lookup"><span data-stu-id="9cd54-113">Application programmers must use the IPV6\_ADD\_MEMBERSHIP socket option to enable multicast reception from any source, including the all-nodes multicast group address.</span></span>

> [!Note]  
> <span data-ttu-id="9cd54-114">在 IPv6 中，會在傳遞至多播通訊端選項或 IOCTL 的引數結構中指定介面選取。</span><span class="sxs-lookup"><span data-stu-id="9cd54-114">In IPv6, interface selection is specified in the argument structure passed to the multicast socket option or IOCTL.</span></span>

 

<span data-ttu-id="9cd54-115">但是，針對多部主機提供更豐富、更健全、更有彈性且更容易管理的傳輸，應用程式開發人員應該考慮移至多播模型。</span><span class="sxs-lookup"><span data-stu-id="9cd54-115">But for richer, more robust, more selective and more manageable transmissions to multiple hosts, application developers should consider moving to a multicast model.</span></span>

## <a name="moving-to-multicast"></a><span data-ttu-id="9cd54-116">移至多播</span><span class="sxs-lookup"><span data-stu-id="9cd54-116">Moving to Multicast</span></span>

<span data-ttu-id="9cd54-117">使用多播時，應用程式設計人員可以選擇性地選擇特定的來源/群組配對，以啟用選擇性的接收模型。</span><span class="sxs-lookup"><span data-stu-id="9cd54-117">With multicast, application programmers can selectively choose a particular source/group pair, enabling a selective reception model.</span></span> <span data-ttu-id="9cd54-118">多播接聽程式探索 (IPv6 和第3版的網際網路群組管理通訊協定上的 MLD)  (IGMPv3) IPv4 支援多播程式設計。</span><span class="sxs-lookup"><span data-stu-id="9cd54-118">The Multicast Listener Discovery (MLD) on IPv6 and version 3 of the Internet Group Management Protocol (IGMPv3) on IPv4 support multicasting programming.</span></span> <span data-ttu-id="9cd54-119">此外，多播可讓應用程式特別封鎖群組內的 (或解除封鎖) 的寄件者，進一步保護應用程式免于 rogue 的廣播者。</span><span class="sxs-lookup"><span data-stu-id="9cd54-119">In addition, multicast enables applications to specifically block (or unblock) senders within a group, further protecting applications from rogue broadcasters.</span></span> <span data-ttu-id="9cd54-120">這項功能適用于 IPv4 (需要 IGMPv3) 和 IPv6 (需要 MLDv2) 。</span><span class="sxs-lookup"><span data-stu-id="9cd54-120">This capability is available for IPv4 (requires IGMPv3) as well as IPv6 (requires MLDv2).</span></span>

<span data-ttu-id="9cd54-121">使用多播的應用程式程式設計人員有兩個主要案例：從 IPv4 廣播移植 (或多播) 應用程式傳送至 IPv6，以及建立新的 IPv6 多播應用程式。</span><span class="sxs-lookup"><span data-stu-id="9cd54-121">There are two primary scenarios for application programmers using multicast: those porting from IPv4 broadcast (or multicast) applications to IPv6, and those creating new IPv6 multicast applications.</span></span>

<span data-ttu-id="9cd54-122">若要移植現有的應用程式，有兩個選項可移至 IPv6 多播：使用通訊端選項和使用 IOCTLs。</span><span class="sxs-lookup"><span data-stu-id="9cd54-122">For porting existing applications, there are two options to move to IPv6 multicast: using socket options and using IOCTLs.</span></span>

-   <span data-ttu-id="9cd54-123">使用通訊端選項是以變更為基礎的方法，可讓開發人員視需要變更通訊端屬性 (例如封鎖或解除封鎖寄件者、新增來源等) 。</span><span class="sxs-lookup"><span data-stu-id="9cd54-123">Using socket options is a change-based approach, which enables developers to change the socket properties as required (such as blocking or unblocking a sender, adding a new source, and so on).</span></span> <span data-ttu-id="9cd54-124">這種方法比較直覺，也是建議的方法。</span><span class="sxs-lookup"><span data-stu-id="9cd54-124">This approach is more intuitive and the recommended approach.</span></span> <span data-ttu-id="9cd54-125">如需以變更為基礎的多播方法的詳細資訊，請參閱 [使用 Windows 通訊端的 MLD 和 IGMP](igmp-and-windows-sockets.md)。</span><span class="sxs-lookup"><span data-stu-id="9cd54-125">For more information on the change-based approach to multicast programming, see [MLD and IGMP Using Windows Sockets](igmp-and-windows-sockets.md).</span></span>
-   <span data-ttu-id="9cd54-126">使用 IOCTLs 是以最終狀態為基礎的方法，因為它可讓開發人員提供完整設定的通訊端狀態，包括包含和排除清單，以及一個呼叫。</span><span class="sxs-lookup"><span data-stu-id="9cd54-126">Using IOCTLs is a final-state based approach, because it enables developers to provide a fully-configured socket state, including inclusion and exclusion lists, with one call.</span></span> <span data-ttu-id="9cd54-127">如需以最終狀態為基礎之方法的詳細資訊，請參閱 [最終狀態式多播程式設計](final-state-based-multicast-programming.md)。</span><span class="sxs-lookup"><span data-stu-id="9cd54-127">For more information on the final-state based approach, see [Final-State-Based Multicast Programming](final-state-based-multicast-programming.md).</span></span>

<span data-ttu-id="9cd54-128">針對建立新 IPv6 多播應用程式的應用程式，建議的作法是使用通訊端選項，而不是使用 IOCTLs。</span><span class="sxs-lookup"><span data-stu-id="9cd54-128">For those creating new IPv6 multicast applications, the recommended practice is to use socket options, rather than using IOCTLs.</span></span>

<span data-ttu-id="9cd54-129">另一種方法是使用 IPv6 來建立多播應用程式，而這需要使用 [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) 功能。</span><span class="sxs-lookup"><span data-stu-id="9cd54-129">There is one other approach to creating multicast applications with IPv6, and that entails using the [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) function.</span></span> <span data-ttu-id="9cd54-130">雖然不建議使用 **WSAJoinLeaf** 函式，但在某些情況下可能會用到它。</span><span class="sxs-lookup"><span data-stu-id="9cd54-130">While using the **WSAJoinLeaf** function is not the recommended practice, there are situations that may dictate its use.</span></span> <span data-ttu-id="9cd54-131">例如，在 Windows Server 2003 及更早版本上使用通訊端選項的其中一個缺點是它們都是 IP 版本專屬的。</span><span class="sxs-lookup"><span data-stu-id="9cd54-131">For example, one drawback to using socket options on Windows Server 2003 and earlier is that they are IP version specific.</span></span> <span data-ttu-id="9cd54-132">在這些較舊版本的 Windows 上，IPv6 和 IPv4 必須有不同的通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="9cd54-132">On these older versions of Windows, different sockets options must be for IPv6 and IPv4.</span></span> <span data-ttu-id="9cd54-133">在 Windows Vista 和更新版本上，支援的新通訊端選項可搭配 IPv4 和 IPv6 使用。</span><span class="sxs-lookup"><span data-stu-id="9cd54-133">On Windows Vista and later, new socket options are supported that can be used with both IPv4 and IPv6.</span></span> <span data-ttu-id="9cd54-134">相反地， **WSAJoinLeaf** 函式是與 IP 版本和通訊協定無關，因此在建立必須在 Windows Server 2003 及更早版本上使用多個 IP 版本的應用程式時，這是很有用的方法。</span><span class="sxs-lookup"><span data-stu-id="9cd54-134">The **WSAJoinLeaf** function, in contrast, is IP version and protocol agnostic, and therefore it can be a useful approach for building an application that must work with multiple IP versions on Windows Server 2003 and earlier.</span></span> <span data-ttu-id="9cd54-135">在需要通訊協定和 IP 版本 agnosticism 的特定情況下，使用 **WSAJoinLeaf** 函數可能更適合。</span><span class="sxs-lookup"><span data-stu-id="9cd54-135">Using the **WSAJoinLeaf** function may be more appropriate in certain situations where protocol and IP-version agnosticism is required.</span></span>

 

 




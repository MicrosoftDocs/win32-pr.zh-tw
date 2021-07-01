---
title: 適用于遊戲開發人員的 Windows 防火牆
description: 本文說明 Windows 防火牆的原因、其存在的原因，以及其運作方式。 最重要的是，它會說明如何設定您的遊戲來與防火牆搭配運作。
ms.assetid: 2ee9f769-03dc-3661-5d5b-6a4ecd151fd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15c7ff3c9b651b6264703732f0eec57054784034
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120233"
---
# <a name="windows-firewall-for-game-developers"></a><span data-ttu-id="5a30d-104">適用于遊戲開發人員的 Windows 防火牆</span><span class="sxs-lookup"><span data-stu-id="5a30d-104">Windows Firewall for Game Developers</span></span>

<span data-ttu-id="5a30d-105">本文說明 Windows 防火牆的原因、其存在的原因，以及其運作方式。</span><span class="sxs-lookup"><span data-stu-id="5a30d-105">This article describes the Windows Firewall - why it exists, what it accomplishes, and how it does so.</span></span> <span data-ttu-id="5a30d-106">最重要的是，它會說明如何設定您的遊戲來與防火牆搭配運作。</span><span class="sxs-lookup"><span data-stu-id="5a30d-106">Most importantly, it describes how to configure your game to work well with the firewall.</span></span>

<span data-ttu-id="5a30d-107">內容: </span><span class="sxs-lookup"><span data-stu-id="5a30d-107">Contents:</span></span>

-   [<span data-ttu-id="5a30d-108">什麼是防火牆？</span><span class="sxs-lookup"><span data-stu-id="5a30d-108">What is a Firewall?</span></span>](#what-is-a-firewall)
-   [<span data-ttu-id="5a30d-109">如何判斷遊戲是否受到影響？</span><span class="sxs-lookup"><span data-stu-id="5a30d-109">How can I tell if my game is affected?</span></span>](#how-can-i-tell-if-my-game-is-affected)
-   [<span data-ttu-id="5a30d-110">Windows XP SP2 之前的防火牆</span><span class="sxs-lookup"><span data-stu-id="5a30d-110">The Firewall Before Windows XP SP2</span></span>](#the-firewall-before-windows-xp-sp2)
-   [<span data-ttu-id="5a30d-111">Windows XP SP2 防火牆更好用</span><span class="sxs-lookup"><span data-stu-id="5a30d-111">Windows XP SP2 Firewall Is Better</span></span>](#windows-xp-sp2-firewall-is-better)
-   [<span data-ttu-id="5a30d-112">使用 Windows 防火牆</span><span class="sxs-lookup"><span data-stu-id="5a30d-112">Working with the Windows Firewall</span></span>](#working-with-the-windows-firewall)
-   [<span data-ttu-id="5a30d-113">使用 InstallShield InstallScript 整合</span><span class="sxs-lookup"><span data-stu-id="5a30d-113">Integrating using InstallShield InstallScript</span></span>](#integrating-using-installshield-installscript)
-   [<span data-ttu-id="5a30d-114">Windows Installer 的明智整合</span><span class="sxs-lookup"><span data-stu-id="5a30d-114">Integrating into Wise for Windows Installer</span></span>](#integrating-into-wise-for-windows-installer)
-   [<span data-ttu-id="5a30d-115">整合至 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="5a30d-115">Integrating into Windows Installer</span></span>](#integrating-into-windows-installer)
-   [<span data-ttu-id="5a30d-116">建議</span><span class="sxs-lookup"><span data-stu-id="5a30d-116">Recommendations</span></span>](#recommendations)

## <a name="what-is-a-firewall"></a><span data-ttu-id="5a30d-117">什麼是防火牆？</span><span class="sxs-lookup"><span data-stu-id="5a30d-117">What is a Firewall?</span></span>

<span data-ttu-id="5a30d-118">防火牆可針對網路型入侵提供阻礙。</span><span class="sxs-lookup"><span data-stu-id="5a30d-118">The firewall provides a barrier against network-based intrusions.</span></span> <span data-ttu-id="5a30d-119">它會封鎖未經要求的連入流量，並藉由拒絕 (ICMP) 要求的網際網路控制訊息通訊協定，讓系統在網際網路上大多不可見。</span><span class="sxs-lookup"><span data-stu-id="5a30d-119">It blocks unsolicited incoming traffic, and makes the system mostly invisible on the internet by rejecting Internet Control Message Protocol (ICMP) requests.</span></span> <span data-ttu-id="5a30d-120">這表示 ping 和 tracert 將無法運作。</span><span class="sxs-lookup"><span data-stu-id="5a30d-120">This means that ping and tracert will not work.</span></span> <span data-ttu-id="5a30d-121">防火牆也會尋找並拒絕不正確封包。</span><span class="sxs-lookup"><span data-stu-id="5a30d-121">The firewall also looks and rejects invalid packets.</span></span>

<span data-ttu-id="5a30d-122">此屏障可防止隨機攻擊。</span><span class="sxs-lookup"><span data-stu-id="5a30d-122">This barrier prevents opportunistic attacks.</span></span> <span data-ttu-id="5a30d-123">攻擊是藉由尋找具有相同弱點的許多系統來散佈。</span><span class="sxs-lookup"><span data-stu-id="5a30d-123">Attacks spread by finding many systems with the same vulnerability.</span></span> <span data-ttu-id="5a30d-124">防火牆可以針對目前未使用的功能，加上「請勿打擾」符號，來對抗許多攻擊;攻擊會被忽略，且不會被刪除。</span><span class="sxs-lookup"><span data-stu-id="5a30d-124">The firewall can thwart many attacks by putting up a "do not disturb" sign for those features not currently in use; the attack is ignored and does not strike home.</span></span> <span data-ttu-id="5a30d-125">Windows 防火牆的基本優點是，未使用的功能和應用程式無法作為攻擊的途徑。</span><span class="sxs-lookup"><span data-stu-id="5a30d-125">The essential benefit of the Windows Firewall is that features and applications that are not in use cannot be avenues for attack.</span></span>

<span data-ttu-id="5a30d-126">使用者將系統設定為識別所需的應用程式和功能，並應對網路開放。</span><span class="sxs-lookup"><span data-stu-id="5a30d-126">The user configures the system to identify what applications and features are needed and should be open to the network.</span></span> <span data-ttu-id="5a30d-127">當應用程式已安裝，或是當應用程式嘗試對網路開啟本身時，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="5a30d-127">This happens either when an application is installed or when it tries to open itself to the network.</span></span>

## <a name="how-can-i-tell-if-my-game-is-affected"></a><span data-ttu-id="5a30d-128">如何判斷遊戲是否受到影響？</span><span class="sxs-lookup"><span data-stu-id="5a30d-128">How can I tell if my game is affected?</span></span>

<span data-ttu-id="5a30d-129">隨著 Windows XP SP2 的抵達，Windows 防火牆已廣泛部署。</span><span class="sxs-lookup"><span data-stu-id="5a30d-129">With the arrival of Windows XP SP2, the Windows Firewall has been widely deployed.</span></span> <span data-ttu-id="5a30d-130">所有多人遊戲的 Windows 遊戲都會受到某種程度的影響。</span><span class="sxs-lookup"><span data-stu-id="5a30d-130">All multiplayer Windows games are affected to some degree.</span></span> <span data-ttu-id="5a30d-131">用戶端通常是在良好的圖形中，而伺服器、主機和對等的對等都需要設定防火牆才能繼續運作。</span><span class="sxs-lookup"><span data-stu-id="5a30d-131">While clients are generally in good shape, servers, hosts, and peers in peer-to-peer all need the firewall configured to continue working.</span></span> <span data-ttu-id="5a30d-132">具體而言，會捨棄傳入的未經要求流量。</span><span class="sxs-lookup"><span data-stu-id="5a30d-132">Specifically, incoming unsolicited traffic is dropped.</span></span> <span data-ttu-id="5a30d-133">防火牆會根據封包內容和最近的網路活動來攔截網路流量篩選封包。</span><span class="sxs-lookup"><span data-stu-id="5a30d-133">The firewall intercepts network-traffic filter packets based on the packet contents and recent network activity.</span></span> <span data-ttu-id="5a30d-134">防火牆會使用 [內容] 和 [活動] 來決定要轉寄或捨棄封包。</span><span class="sxs-lookup"><span data-stu-id="5a30d-134">The firewall uses the contents and activity to decide to forward or drop a packet.</span></span> <span data-ttu-id="5a30d-135">一旦正確設定防火牆之後，遊戲就能像之前一樣接受輸入的未經要求流量。</span><span class="sxs-lookup"><span data-stu-id="5a30d-135">Once the firewall is properly configured, a game will be able to accept inbound unsolicited traffic as before.</span></span>

<span data-ttu-id="5a30d-136">誰有輸入未經要求的流量？</span><span class="sxs-lookup"><span data-stu-id="5a30d-136">Who has inbound unsolicited traffic?</span></span>

-   <span data-ttu-id="5a30d-137">用戶端/伺服器：所有參與者連接到中央伺服器。</span><span class="sxs-lookup"><span data-stu-id="5a30d-137">Client/Server: All participants connect to a central server.</span></span> <span data-ttu-id="5a30d-138">中央伺服器是具有連入未經要求流量的伺服器。</span><span class="sxs-lookup"><span data-stu-id="5a30d-138">The central server is the one with incoming unsolicited traffic.</span></span> <span data-ttu-id="5a30d-139">連線到伺服器的用戶端會請求傳回流量，如果遵循用戶端的規則，系統就會允許該流量通過防火牆。</span><span class="sxs-lookup"><span data-stu-id="5a30d-139">The clients connecting to the server are soliciting return traffic, which is expected and is allowed to pass through the firewall if the rules for clients are followed.</span></span> <span data-ttu-id="5a30d-140">中央伺服器必須設定為接受未經要求的流量，才能讓用戶端流量通過防火牆。</span><span class="sxs-lookup"><span data-stu-id="5a30d-140">The central server must be configured to accept the unsolicited traffic to allow the client traffic to pass through the firewall.</span></span>
-   <span data-ttu-id="5a30d-141">大量多人 (MMP) ：所有參與者都連線至資料中心。</span><span class="sxs-lookup"><span data-stu-id="5a30d-141">Massively Multiplayer (MMP): All participants are connected to a data center.</span></span> <span data-ttu-id="5a30d-142">這相當於複雜的用戶端/伺服器關聯性，因為資料中心具有輸入的未經要求流量。</span><span class="sxs-lookup"><span data-stu-id="5a30d-142">This amounts to a complex client/server relationship, as the data center has the inbound unsolicited traffic.</span></span> <span data-ttu-id="5a30d-143">參與者是用戶端，而且通常不需要接受未經要求的流量。</span><span class="sxs-lookup"><span data-stu-id="5a30d-143">The participants are clients, and in general do not need to accept unsolicited traffic.</span></span>
-   <span data-ttu-id="5a30d-144">點對點，也就是所有參與者都直接彼此連接：所有參與者都必須準備好接受來自加入群組之任何新玩家的未經要求流量。</span><span class="sxs-lookup"><span data-stu-id="5a30d-144">Peer-to-Peer, where all participants are connected to each other directly: All participants must be ready to accept unsolicited traffic from any new player joining the group.</span></span> <span data-ttu-id="5a30d-145">就某種意義而言，每個參與者都必須以主機的形式運作，因此必須全部設定為主機。</span><span class="sxs-lookup"><span data-stu-id="5a30d-145">In a sense, each of the participants must function as a host, so they must all be configured as if they were hosts.</span></span>

<span data-ttu-id="5a30d-146">用戶端通常是不錯的圖形。</span><span class="sxs-lookup"><span data-stu-id="5a30d-146">Clients are generally in good shape.</span></span> <span data-ttu-id="5a30d-147">其連出的傳輸控制通訊協定/網際網路通訊協定 (TCP/IP) 連線可以正常運作，因為輸出使用者資料包協定 (UDP) 訊息，以及及時回應這些訊息，防火牆會在每個外寄訊息之後，將埠保持開啟狀態達90秒，以預期回復。</span><span class="sxs-lookup"><span data-stu-id="5a30d-147">Their outgoing Transmission Control Protocol/Internet Protocol (TCP/IP) connections will work fine, as will outgoing User Datagram Protocol (UDP) messages along with timely responses to those messages - the firewall keeps the port open for 90 seconds after each outgoing message in anticipation of a reply.</span></span>

## <a name="the-firewall-before-windows-xp-sp2"></a><span data-ttu-id="5a30d-148">Windows XP SP2 之前的防火牆</span><span class="sxs-lookup"><span data-stu-id="5a30d-148">The Firewall Before Windows XP SP2</span></span>

<span data-ttu-id="5a30d-149">Windows XP 和 Windows Server 2003 中的網際網路連線防火牆 (ICF) 是具狀態的封包篩選器，可處理網際網路通訊協定第4版 (IPv4) 和網際網路通訊協定第6版 (IPv6) 。</span><span class="sxs-lookup"><span data-stu-id="5a30d-149">The Internet Connection Firewall (ICF) in Windows XP and Windows Server 2003 is a stateful packet filter, and handles both Internet Protocol, version 4 (IPv4) and Internet Protocol, version 6 (IPv6).</span></span> <span data-ttu-id="5a30d-150">不過，它並不會預設為開啟，且不支援協力廠商網路堆疊，在世界中有很大的數位，例如大型的網際網路提供者（包括全國電話公司）。</span><span class="sxs-lookup"><span data-stu-id="5a30d-150">However, it is not on by default and does not support 3rd party network stacks, of which there are a significant number in the world, such as large internet providers including national telephone companies.</span></span>

<span data-ttu-id="5a30d-151">針對不在 Windows XP SP2 上的，強烈建議開啟 ICF。</span><span class="sxs-lookup"><span data-stu-id="5a30d-151">For those not on Windows XP SP2, turning on the ICF is highly recommended.</span></span> <span data-ttu-id="5a30d-152">請參閱中的「使用網際網路防火牆」， https://www.microsoft.com/security/protect 作為保護您電腦的第一步。</span><span class="sxs-lookup"><span data-stu-id="5a30d-152">See the instructions "Use an Internet Firewall" on https://www.microsoft.com/security/protect as the first step to securing your PC.</span></span> <span data-ttu-id="5a30d-153">網際網路連線防火牆 (ICF) 提供埠對應以覆寫封包篩選器。</span><span class="sxs-lookup"><span data-stu-id="5a30d-153">The Internet Connection Firewall (ICF) provides port mapping to override the packet filter.</span></span> <span data-ttu-id="5a30d-154">基本上，您會指定要開啟的埠，並在關閉它之前保持開啟狀態。</span><span class="sxs-lookup"><span data-stu-id="5a30d-154">Essentially, you specify the port to open and it remains opened until you close it.</span></span> <span data-ttu-id="5a30d-155">如果使用者在關閉之前重新開機，它將保持開啟狀態，直到特別關閉為止。</span><span class="sxs-lookup"><span data-stu-id="5a30d-155">If the user reboots before it is closed, it will remain open until specifically closed.</span></span> <span data-ttu-id="5a30d-156">防火牆的控制和埠對應的管理是透過 [**INetSharingManager**](/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingmanager) (IPv4) 和 [**INetFwV6Mgr**](/previous-versions/windows/desktop/ics/inetfwv6mgr) (IPv6) 來完成。</span><span class="sxs-lookup"><span data-stu-id="5a30d-156">The control of the firewall and the management of the port mappings is done via [**INetSharingManager**](/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingmanager) (IPv4) and [**INetFwV6Mgr**](/previous-versions/windows/desktop/ics/inetfwv6mgr) (IPv6).</span></span>

<span data-ttu-id="5a30d-157">適用于 Windows XP SP2 的 Windows 防火牆是更完整的解決方案，可支援協力廠商網路堆疊，並更聰明地處理埠：只有在需要它們的應用程式仍在使用中時，埠才會保持開啟狀態。</span><span class="sxs-lookup"><span data-stu-id="5a30d-157">The Windows Firewall for Windows XP SP2 is a more comprehensive solution that does support 3rd party network stacks, and handles ports more intelligently: ports are kept open only so long as the application that needs them is still active.</span></span>

## <a name="windows-xp-sp2-firewall-is-better"></a><span data-ttu-id="5a30d-158">Windows XP SP2 防火牆更好用</span><span class="sxs-lookup"><span data-stu-id="5a30d-158">Windows XP SP2 Firewall Is Better</span></span>

<span data-ttu-id="5a30d-159">Windows XP SP2 將安全性選項和設定放在前方。</span><span class="sxs-lookup"><span data-stu-id="5a30d-159">Windows XP SP2 puts the security choices and settings out front.</span></span> <span data-ttu-id="5a30d-160">目標是要預設保護，並允許使用者對其電腦上允許執行哪些應用程式做出明智的選擇。</span><span class="sxs-lookup"><span data-stu-id="5a30d-160">The goal is to protect by default, and allow the user to make informed choices about what applications are allowed to run on their machine.</span></span>

<span data-ttu-id="5a30d-161">Windows XP SP2 和 Windows Server 2003 Service Pack 1 (SP1) 都有提供新的 Windows 防火牆。</span><span class="sxs-lookup"><span data-stu-id="5a30d-161">The new Windows Firewall is available on both Windows XP SP2 and Windows Server 2003 Service Pack 1 (SP1).</span></span> <span data-ttu-id="5a30d-162">就像 ICF 一樣，它是一種同時支援 IPv4 和 IPv6 的軟體防火牆，但不同于 ICF 的 Windows 防火牆：</span><span class="sxs-lookup"><span data-stu-id="5a30d-162">Like the ICF, it is a software firewall that supports both IPv4 and IPv6, but unlike ICF the Windows Firewall:</span></span>

-   <span data-ttu-id="5a30d-163">具有系統的開機時間保護，在開機期間消除一小部分的弱點。</span><span class="sxs-lookup"><span data-stu-id="5a30d-163">Has boot-time protection of the system, eliminating a small window of vulnerability during boot.</span></span>
-   <span data-ttu-id="5a30d-164">支援協力廠商網路堆疊。</span><span class="sxs-lookup"><span data-stu-id="5a30d-164">Supports 3rd party network stacks.</span></span>
-   <span data-ttu-id="5a30d-165">具有「開啟但沒有例外狀況」模式，會封鎖所有未經要求的連入封包。</span><span class="sxs-lookup"><span data-stu-id="5a30d-165">Has an "on with no exceptions" mode that blocks all unsolicited incoming packets.</span></span> <span data-ttu-id="5a30d-166">當您使用公用網路（例如機場或咖啡廳）時，這就很好用。</span><span class="sxs-lookup"><span data-stu-id="5a30d-166">This is great when you're using a public network, such as in an airport or coffee shop.</span></span>

<span data-ttu-id="5a30d-167">在「沒有例外狀況的開啟」模式中，所有的靜態洞都會關閉。</span><span class="sxs-lookup"><span data-stu-id="5a30d-167">In the "on with no exceptions" mode, all static holes are closed.</span></span> <span data-ttu-id="5a30d-168">允許用來開啟靜態洞的 API 呼叫，但會延後;也就是說，在防火牆切換回正常作業之前，它們都不會套用。</span><span class="sxs-lookup"><span data-stu-id="5a30d-168">API calls to open a static hole are allowed but deferred; that is, they are not applied until the firewall switches back to normal operation.</span></span> <span data-ttu-id="5a30d-169">應用程式的所有接聽要求也會被忽略。</span><span class="sxs-lookup"><span data-stu-id="5a30d-169">All listen requests by applications will also be ignored.</span></span> <span data-ttu-id="5a30d-170">輸出連接仍然會成功。</span><span class="sxs-lookup"><span data-stu-id="5a30d-170">Outbound connections will still succeed.</span></span>

<span data-ttu-id="5a30d-171">針對新的應用程式，請在安裝期間將您的應用程式新增至「例外狀況清單」。</span><span class="sxs-lookup"><span data-stu-id="5a30d-171">For new applications, add your application to the "Exceptions List" during installation.</span></span> <span data-ttu-id="5a30d-172">您可以使用 [**INetFwAuthorizedApplications**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwauthorizedapplications) 介面來新增應用程式，並提供完整的路徑。</span><span class="sxs-lookup"><span data-stu-id="5a30d-172">You can add the application using the [**INetFwAuthorizedApplications**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwauthorizedapplications) interface, supplying the full path.</span></span> <span data-ttu-id="5a30d-173">我們將在此討論範例中的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="5a30d-173">We'll cover the details in the sample.</span></span>

<span data-ttu-id="5a30d-174">請注意，您可能會想知道它是否有安全性風險，也就是應用程式可以從例外狀況清單中新增和移除應用程式，以因應使用者的介入，或您認為較大的風險是，應用程式可以完全停用防火牆。</span><span class="sxs-lookup"><span data-stu-id="5a30d-174">As a side note, you may be wondering if it is a security risk that applications can add and remove applications from the exceptions list any user intervention, or perhaps you think that the bigger risk is that applications can disable the firewall altogether.</span></span> <span data-ttu-id="5a30d-175">若要執行這些無比理智，應用程式必須具有系統管理員許可權。</span><span class="sxs-lookup"><span data-stu-id="5a30d-175">To perform these feats, the application must have administrator privileges.</span></span> <span data-ttu-id="5a30d-176">如果您在系統上以系統管理員模式執行惡意程式碼，則遊戲已經結束，而且駭客已經獲勝。</span><span class="sxs-lookup"><span data-stu-id="5a30d-176">If you have malicious code running in administrator mode on your system, the game is already over and the hacker has already won.</span></span> <span data-ttu-id="5a30d-177">駭客停用防火牆的功能只需要使用註腳。</span><span class="sxs-lookup"><span data-stu-id="5a30d-177">The hacker's ability to disable the firewall would merit little more than a footnote.</span></span>

<span data-ttu-id="5a30d-178">繼承應用程式（包括在使用者升級至 Windows XP SP2 之前安裝的應用程式）會以例外狀況清單快顯視窗來處理 (請參閱 [圖 1]) 。</span><span class="sxs-lookup"><span data-stu-id="5a30d-178">Legacy applications, including applications installed before the user upgraded to Windows XP SP2, are handled with the Exceptions List popup (see Figure 1).</span></span> <span data-ttu-id="5a30d-179">此對話方塊會顯示當應用程式嘗試為連入流量開啟埠時，可能是使用非零埠的 UDP 呼叫 bind () ，或接受 TCP/IP 通訊協定的 () 。</span><span class="sxs-lookup"><span data-stu-id="5a30d-179">This dialog shows when an application tries to open a port for incoming traffic - either when calling bind() with a non-zero port for UDP, or accept() for TCP/IP protocol.</span></span> <span data-ttu-id="5a30d-180">您必須以系統管理員身分執行，才能「解除封鎖」應用程式，而「稍後詢問我」則不允許這段時間，但會在下一次重新詢問。</span><span class="sxs-lookup"><span data-stu-id="5a30d-180">You must be running as an Administrator to "Unblock" applications, while "Ask Me Later" disallows this time around but asks again next time.</span></span>

<span data-ttu-id="5a30d-181">這是未封鎖的系統強制回應對話方塊。</span><span class="sxs-lookup"><span data-stu-id="5a30d-181">This is a non-blocking, system modal dialog box.</span></span> <span data-ttu-id="5a30d-182">執行全螢幕的 Microsoft Direct3D 應用程式時，對話方塊會出現在下方;然後使用者可以在應用程式結束全螢幕模式或 alt 索引標籤回桌面時處理它。</span><span class="sxs-lookup"><span data-stu-id="5a30d-182">When running a fullscreen Microsoft Direct3D application, the dialog comes in underneath; and the user can then handle it when the application exits fullscreen mode or alt-tabs back to the desktop.</span></span> <span data-ttu-id="5a30d-183">不過，使用者在遊戲執行全螢幕時，不一定會看到這個對話方塊出現的情況，因此請務必避免使用 [**INetFwAuthorizedApplications**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwauthorizedapplications) 介面讓這個對話方塊出現，如下所述。</span><span class="sxs-lookup"><span data-stu-id="5a30d-183">However, it is not always obvious to the user that this dialog has appeared when a game is running fullscreen, so it is important to avoid causing this dialog to appear by using [**INetFwAuthorizedApplications**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwauthorizedapplications) interface as discussed below.</span></span>

<span data-ttu-id="5a30d-184">**圖1。例外狀況清單快顯視窗對話方塊**</span><span class="sxs-lookup"><span data-stu-id="5a30d-184">**Figure 1. Exceptions List Popup Dialog**</span></span>

![例外狀況清單快顯視窗對話方塊](images/firewalls1.jpg)

<span data-ttu-id="5a30d-186">您將會注意到快顯視窗知道應用程式的名稱和發行者。</span><span class="sxs-lookup"><span data-stu-id="5a30d-186">You'll notice that the popup knows the name and publisher of the application.</span></span> <span data-ttu-id="5a30d-187">這裡沒有什麼神奇之處-它是從可執行檔的版本資訊中提取。</span><span class="sxs-lookup"><span data-stu-id="5a30d-187">There's no magic here - it's pulled from the executable's version information.</span></span> <span data-ttu-id="5a30d-188">這項資訊是很重要的系統管理工具;它甚至可以用來進行應用程式相容性工作。</span><span class="sxs-lookup"><span data-stu-id="5a30d-188">This information is an important system administration tool; it is even used for ongoing application compatibility work.</span></span> <span data-ttu-id="5a30d-189">有些應用程式會忽略將此版本資訊保持在最新狀態。</span><span class="sxs-lookup"><span data-stu-id="5a30d-189">Some applications neglect to keep this version information up-to-date.</span></span>

<span data-ttu-id="5a30d-190">使用者也可以透過使用者介面 (UI 來新增其應用程式)  (請參閱圖 2) </span><span class="sxs-lookup"><span data-stu-id="5a30d-190">Users can also add their applications through the user interface (UI) (see Figure 2)</span></span>

<span data-ttu-id="5a30d-191">**[圖 2]設定防火牆**</span><span class="sxs-lookup"><span data-stu-id="5a30d-191">**Figure 2. Configuring the Firewall**</span></span>

![設定防火牆](images/firewalls2.jpg)

<span data-ttu-id="5a30d-193">**圖3。將程式新增至防火牆例外清單**</span><span class="sxs-lookup"><span data-stu-id="5a30d-193">**Figure 3. Adding a Program to the Firewall Exceptions List**</span></span>

![將程式新增至防火牆例外清單](images/firewalls3.jpg)

<span data-ttu-id="5a30d-195">最佳情況是從例外狀況清單自動進行新增和移除。</span><span class="sxs-lookup"><span data-stu-id="5a30d-195">The best scenario is to make additions and removals from the exception list automated.</span></span> <span data-ttu-id="5a30d-196">執行這些新增和移除的最佳時機是在安裝和卸載程式期間。</span><span class="sxs-lookup"><span data-stu-id="5a30d-196">The best time to perform these additions and removals is during the install and uninstall process.</span></span> <span data-ttu-id="5a30d-197">在防火牆例外清單中新增或移除需要系統管理員許可權，因此請務必將此納入考慮。</span><span class="sxs-lookup"><span data-stu-id="5a30d-197">Adding or removing from the firewall exception list requires administrator privileges, so be sure to take this into account.</span></span>

## <a name="working-with-the-windows-firewall"></a><span data-ttu-id="5a30d-198">使用 Windows 防火牆</span><span class="sxs-lookup"><span data-stu-id="5a30d-198">Working with the Windows Firewall</span></span>

<span data-ttu-id="5a30d-199">同樣地，大部分的遊戲都只需要新增到防火牆例外清單中，如果它們可以作為伺服器或執行對等通訊協定。</span><span class="sxs-lookup"><span data-stu-id="5a30d-199">Again, most games only need to be added to the firewall exception list if they can function as a server or if they implement a peer-to-peer communication protocol.</span></span> <span data-ttu-id="5a30d-200">FirewallInstallHelper.dll 是可從安裝程式呼叫的範例 DLL。</span><span class="sxs-lookup"><span data-stu-id="5a30d-200">The FirewallInstallHelper.dll is a sample DLL that can be called from an installer.</span></span> <span data-ttu-id="5a30d-201">如果您想要將來源直接整合到自己的應用程式，則會提供來源。</span><span class="sxs-lookup"><span data-stu-id="5a30d-201">Source is provided if you want to integrate the source directly into your own application.</span></span> <span data-ttu-id="5a30d-202">您可以在這裡找到範例：</span><span class="sxs-lookup"><span data-stu-id="5a30d-202">The sample can be found here:</span></span>



|             | <span data-ttu-id="5a30d-203">檔案</span><span class="sxs-lookup"><span data-stu-id="5a30d-203">File</span></span>                                                                             |
|-------------|------------------------------------------------------------------------------|
| <span data-ttu-id="5a30d-204">**來源：**</span><span class="sxs-lookup"><span data-stu-id="5a30d-204">**Source:**</span></span>     | <span data-ttu-id="5a30d-205"> (SDK 根) \\ 範例 \\ c + + \\ 其他 \\ FirewallInstallHelper</span><span class="sxs-lookup"><span data-stu-id="5a30d-205">(SDK root)\\Samples\\C++\\Misc\\FirewallInstallHelper</span></span>                        |
| <span data-ttu-id="5a30d-206">**可執行：**</span><span class="sxs-lookup"><span data-stu-id="5a30d-206">**Executable:**</span></span> | <span data-ttu-id="5a30d-207"> (SDK 根) \\ 範例 \\ c + + \\ 其他 \\ Bin \\ <arch> \\FirewallInstallHelper.dll</span><span class="sxs-lookup"><span data-stu-id="5a30d-207">(SDK root)\\Samples\\C++\\Misc\\Bin\\<arch>\\FirewallInstallHelper.dll</span></span> |



 

<span data-ttu-id="5a30d-208">此 DLL 匯出的函式如下：</span><span class="sxs-lookup"><span data-stu-id="5a30d-208">The functions exported by this DLL are the following:</span></span>

<dl> <dt>

<span data-ttu-id="5a30d-209"><span id="AddApplicationToExceptionListW"></span><span id="addapplicationtoexceptionlistw"></span><span id="ADDAPPLICATIONTOEXCEPTIONLISTW"></span>**AddApplicationToExceptionListW**</span><span class="sxs-lookup"><span data-stu-id="5a30d-209"><span id="AddApplicationToExceptionListW"></span><span id="addapplicationtoexceptionlistw"></span><span id="ADDAPPLICATIONTOEXCEPTIONLISTW"></span>**AddApplicationToExceptionListW**</span></span>
</dt> <dd>

<span data-ttu-id="5a30d-210">此函式會將應用程式新增至例外狀況清單。</span><span class="sxs-lookup"><span data-stu-id="5a30d-210">This function adds an application to the exception list.</span></span> <span data-ttu-id="5a30d-211">它會取得可執行檔的完整路徑，以及將出現在防火牆例外清單中的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="5a30d-211">It takes a complete path to the executable and a friendly name that will appear in the firewall exception list.</span></span> <span data-ttu-id="5a30d-212">此函數需要系統管理員許可權。</span><span class="sxs-lookup"><span data-stu-id="5a30d-212">This function requires administrator privileges.</span></span>

</dd> <dt>

<span data-ttu-id="5a30d-213"><span id="AddApplicationToExceptionListA"></span><span id="addapplicationtoexceptionlista"></span><span id="ADDAPPLICATIONTOEXCEPTIONLISTA"></span>**AddApplicationToExceptionListA**</span><span class="sxs-lookup"><span data-stu-id="5a30d-213"><span id="AddApplicationToExceptionListA"></span><span id="addapplicationtoexceptionlista"></span><span id="ADDAPPLICATIONTOEXCEPTIONLISTA"></span>**AddApplicationToExceptionListA**</span></span>
</dt> <dd>

<span data-ttu-id="5a30d-214">**AddApplicationToExceptionListW** 的 ANSI 版本</span><span class="sxs-lookup"><span data-stu-id="5a30d-214">ANSI version of **AddApplicationToExceptionListW**</span></span>

</dd> <dt>

<span data-ttu-id="5a30d-215"><span id="RemoveApplicationFromExceptionListW"></span><span id="removeapplicationfromexceptionlistw"></span><span id="REMOVEAPPLICATIONFROMEXCEPTIONLISTW"></span>**RemoveApplicationFromExceptionListW**</span><span class="sxs-lookup"><span data-stu-id="5a30d-215"><span id="RemoveApplicationFromExceptionListW"></span><span id="removeapplicationfromexceptionlistw"></span><span id="REMOVEAPPLICATIONFROMEXCEPTIONLISTW"></span>**RemoveApplicationFromExceptionListW**</span></span>
</dt> <dd>

<span data-ttu-id="5a30d-216">此函數會從例外狀況清單中移除應用程式。</span><span class="sxs-lookup"><span data-stu-id="5a30d-216">This function removes the application from the exception list.</span></span> <span data-ttu-id="5a30d-217">它會取得可執行檔的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="5a30d-217">It takes in a complete path to the executable.</span></span> <span data-ttu-id="5a30d-218">此函數需要系統管理員許可權</span><span class="sxs-lookup"><span data-stu-id="5a30d-218">This function requires administrator privileges</span></span>

</dd> <dt>

<span data-ttu-id="5a30d-219"><span id="RemoveApplicationFromExceptionListA"></span><span id="removeapplicationfromexceptionlista"></span><span id="REMOVEAPPLICATIONFROMEXCEPTIONLISTA"></span>**RemoveApplicationFromExceptionListA**</span><span class="sxs-lookup"><span data-stu-id="5a30d-219"><span id="RemoveApplicationFromExceptionListA"></span><span id="removeapplicationfromexceptionlista"></span><span id="REMOVEAPPLICATIONFROMEXCEPTIONLISTA"></span>**RemoveApplicationFromExceptionListA**</span></span>
</dt> <dd>

<span data-ttu-id="5a30d-220">**RemoveApplicationFromExceptionListW** 的 ANSI 版本</span><span class="sxs-lookup"><span data-stu-id="5a30d-220">ANSI version of **RemoveApplicationFromExceptionListW**</span></span>

</dd> <dt>

<span data-ttu-id="5a30d-221"><span id="CanLaunchMultiplayerGameW"></span><span id="canlaunchmultiplayergamew"></span><span id="CANLAUNCHMULTIPLAYERGAMEW"></span>**CanLaunchMultiplayerGameW**</span><span class="sxs-lookup"><span data-stu-id="5a30d-221"><span id="CanLaunchMultiplayerGameW"></span><span id="canlaunchmultiplayergamew"></span><span id="CANLAUNCHMULTIPLAYERGAMEW"></span>**CanLaunchMultiplayerGameW**</span></span>
</dt> <dd>

<span data-ttu-id="5a30d-222">此函數會報告應用程式是否已停用或從例外狀況清單中移除。</span><span class="sxs-lookup"><span data-stu-id="5a30d-222">This function reports if the application has been disabled or removed from the exceptions list.</span></span> <span data-ttu-id="5a30d-223">您應該在每次執行遊戲時呼叫它。</span><span class="sxs-lookup"><span data-stu-id="5a30d-223">It should be called every time the game is run.</span></span> <span data-ttu-id="5a30d-224">函數會取得可執行檔的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="5a30d-224">The function takes in a complete path to the executable.</span></span> <span data-ttu-id="5a30d-225">此函數不需要系統管理員許可權。</span><span class="sxs-lookup"><span data-stu-id="5a30d-225">This function does not require administrator privileges.</span></span>

</dd> <dt>

<span data-ttu-id="5a30d-226"><span id="CanLaunchMultiplayerGameA"></span><span id="canlaunchmultiplayergamea"></span><span id="CANLAUNCHMULTIPLAYERGAMEA"></span>**CanLaunchMultiplayerGameA**</span><span class="sxs-lookup"><span data-stu-id="5a30d-226"><span id="CanLaunchMultiplayerGameA"></span><span id="canlaunchmultiplayergamea"></span><span id="CANLAUNCHMULTIPLAYERGAMEA"></span>**CanLaunchMultiplayerGameA**</span></span>
</dt> <dd>

<span data-ttu-id="5a30d-227">**CanLaunchMultiplayerGameW** 的 ANSI 版本</span><span class="sxs-lookup"><span data-stu-id="5a30d-227">ANSI version of **CanLaunchMultiplayerGameW**</span></span>

</dd> <dt>

<span data-ttu-id="5a30d-228"><span id="SetMSIFirewallProperties"></span><span id="setmsifirewallproperties"></span><span id="SETMSIFIREWALLPROPERTIES"></span>**SetMSIFirewallProperties**</span><span class="sxs-lookup"><span data-stu-id="5a30d-228"><span id="SetMSIFirewallProperties"></span><span id="setmsifirewallproperties"></span><span id="SETMSIFIREWALLPROPERTIES"></span>**SetMSIFirewallProperties**</span></span>
</dt> <dd>

<span data-ttu-id="5a30d-229">只有當您在 Windows Installer 中使用自訂動作時，才需要呼叫此項。</span><span class="sxs-lookup"><span data-stu-id="5a30d-229">Call this only if you are using custom actions in Windows Installer.</span></span> <span data-ttu-id="5a30d-230">詳細資訊請見下文。</span><span class="sxs-lookup"><span data-stu-id="5a30d-230">See below for more details.</span></span>

</dd> <dt>

<span data-ttu-id="5a30d-231"><span id="AddToExceptionListUsingMSI"></span><span id="addtoexceptionlistusingmsi"></span><span id="ADDTOEXCEPTIONLISTUSINGMSI"></span>**AddToExceptionListUsingMSI**</span><span class="sxs-lookup"><span data-stu-id="5a30d-231"><span id="AddToExceptionListUsingMSI"></span><span id="addtoexceptionlistusingmsi"></span><span id="ADDTOEXCEPTIONLISTUSINGMSI"></span>**AddToExceptionListUsingMSI**</span></span>
</dt> <dd>

<span data-ttu-id="5a30d-232">只有當您在 Windows Installer 中使用自訂動作時，才需要呼叫此項。</span><span class="sxs-lookup"><span data-stu-id="5a30d-232">Call this only if you are using custom actions in Windows Installer.</span></span> <span data-ttu-id="5a30d-233">詳細資訊請見下文。</span><span class="sxs-lookup"><span data-stu-id="5a30d-233">See below for more details.</span></span>

</dd> <dt>

<span data-ttu-id="5a30d-234"><span id="RemoveFromExceptionListUsingMSI"></span><span id="removefromexceptionlistusingmsi"></span><span id="REMOVEFROMEXCEPTIONLISTUSINGMSI"></span>**RemoveFromExceptionListUsingMSI**</span><span class="sxs-lookup"><span data-stu-id="5a30d-234"><span id="RemoveFromExceptionListUsingMSI"></span><span id="removefromexceptionlistusingmsi"></span><span id="REMOVEFROMEXCEPTIONLISTUSINGMSI"></span>**RemoveFromExceptionListUsingMSI**</span></span>
</dt> <dd>

<span data-ttu-id="5a30d-235">只有當您在 Windows Installer 中使用自訂動作時，才需要呼叫此項。</span><span class="sxs-lookup"><span data-stu-id="5a30d-235">Call this only if you are using custom actions in Windows Installer.</span></span> <span data-ttu-id="5a30d-236">詳細資訊請見下文。</span><span class="sxs-lookup"><span data-stu-id="5a30d-236">See below for more details.</span></span>

</dd> </dl>

<span data-ttu-id="5a30d-237">下列各節說明從 InstallShield、明智或 Windows Installer 的封裝中，呼叫從此 FirewallInstallHelper 匯出之 DLL 函數的特定方法。</span><span class="sxs-lookup"><span data-stu-id="5a30d-237">The following sections describe specific methods of calling the exported DLL functions from this FirewallInstallHelper from within an InstallShield, Wise, or Windows Installer package.</span></span> <span data-ttu-id="5a30d-238">所有方法都會轉譯相同的結果，並由開發人員決定要執行的方法。</span><span class="sxs-lookup"><span data-stu-id="5a30d-238">All methods render the same results and it is up to the developer to determine which method to implement.</span></span>

## <a name="integrating-using-installshield-installscript"></a><span data-ttu-id="5a30d-239">使用 InstallShield InstallScript 整合</span><span class="sxs-lookup"><span data-stu-id="5a30d-239">Integrating using InstallShield InstallScript</span></span>

<span data-ttu-id="5a30d-240">使用防火牆 Api 的替代方法是將函式呼叫新增至 InstallShield InstallScript。</span><span class="sxs-lookup"><span data-stu-id="5a30d-240">An alternate method of using the Firewall APIs is to add the function calls to an InstallShield InstallScript.</span></span> <span data-ttu-id="5a30d-241">整合所需的步驟相當簡單：</span><span class="sxs-lookup"><span data-stu-id="5a30d-241">The steps required to integrate are fairly simple:</span></span>

1.  <span data-ttu-id="5a30d-242">在 InstallShield 編輯器中開啟 InstallScript 專案。</span><span class="sxs-lookup"><span data-stu-id="5a30d-242">Open an InstallScript project in the InstallShield editor.</span></span>
2.  <span data-ttu-id="5a30d-243">將 FirewallInstallHelper.dll 新增至專案做為支援檔。</span><span class="sxs-lookup"><span data-stu-id="5a30d-243">Add the FirewallInstallHelper.dll to the project as a support file.</span></span>

    1.  <span data-ttu-id="5a30d-244">在 [專案助理] 索引標籤底下開啟 [應用程式檔] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="5a30d-244">Under Project Assistant tab, open the Application Files tab.</span></span>
    2.  <span data-ttu-id="5a30d-245">按一下 [新增檔案] 按鈕，將檔案新增至應用程式目的檔案夾。</span><span class="sxs-lookup"><span data-stu-id="5a30d-245">Click on the Add Files button to add files to the Application Target Folder.</span></span>
    3.  <span data-ttu-id="5a30d-246">流覽至您所建立的 FirewallInstallHelper.dll，或使用 DirectX SDK 中所提供的，並將它新增至專案。</span><span class="sxs-lookup"><span data-stu-id="5a30d-246">Browse to the FirewallInstallHelper.dll that you have built or use the one provided in the DirectX SDK and add it to the project.</span></span>

3.  <span data-ttu-id="5a30d-247">將 InstallScript 新增至專案。</span><span class="sxs-lookup"><span data-stu-id="5a30d-247">Add InstallScript to the project.</span></span>

    1.  <span data-ttu-id="5a30d-248">開啟安裝設計工具視圖，然後按一下 [行為] 和 [邏輯] \| InstallScript</span><span class="sxs-lookup"><span data-stu-id="5a30d-248">Open the Installation Designer view, and click on the Behavior and Logic \| InstallScript</span></span>
    2.  <span data-ttu-id="5a30d-249">按一下 InstallScript 檔案， (通常設定 rul) 在編輯器中開啟它</span><span class="sxs-lookup"><span data-stu-id="5a30d-249">Click on the InstallScript file (usually setup.rul) to open it in the editor</span></span>
    3.  <span data-ttu-id="5a30d-250">將下列程式碼貼入 InstallScript 檔案：</span><span class="sxs-lookup"><span data-stu-id="5a30d-250">Paste the following code into the InstallScript file:</span></span>

    ``` syntax
    #include "ifx.h"

    prototype BOOL FirewallInstallHelper.AddApplicationToExceptionListW( WSTRING, WSTRING );
    prototype BOOL FirewallInstallHelper.RemoveApplicationFromExceptionListW( WSTRING );

    function OnMoved()
        WSTRING path[256];
    begin
        // The DLL has been installed into the TARGETDIR
        if !MAINTENANCE then // TRUE when installing
            UseDLL( TARGETDIR ^ "FirewallInstallHelper.dll" );
            path = TARGETDIR ^ "TODO: change to relative path to executable from install directory";
            FirewallInstallHelper.AddApplicationToExceptionListW( path, "TODO: change to friendly app name" );
            UnUseDLL( TARGETDIR ^ "FirewallInstallHelper.dll" );
        endif;
    end;
          

    function OnMoving()
        WSTRING path[256];
    begin
        // The DLL is about to be removed from TARGETDIR
        if MAINTENANCE && UNINST != "" then // TRUE when uninstalling
            UseDLL( TARGETDIR ^ "FirewallInstallHelper.dll" );
            path = TARGETDIR ^ "TODO: change to relative path to executable from install directory";
            FirewallInstallHelper.RemoveApplicationFromExceptionListW( path );
            UnUseDLL( TARGETDIR ^ "FirewallInstallHelper.dll" );
        endif;
    end;
    ```

    4.  <span data-ttu-id="5a30d-251">使用將顯示在防火牆例外清單中的應用程式名稱，以及與安裝目錄相關之遊戲可執行檔的路徑，來變更 TODO 批註。</span><span class="sxs-lookup"><span data-stu-id="5a30d-251">Change the TODO comments with the application name that will be shown in the Firewall Exception List and the path to the game executable relative to the installation directory.</span></span>

## <a name="integrating-into-wise-for-windows-installer"></a><span data-ttu-id="5a30d-252">Windows Installer 的明智整合</span><span class="sxs-lookup"><span data-stu-id="5a30d-252">Integrating into Wise for Windows Installer</span></span>

<span data-ttu-id="5a30d-253">若要 Windows Installer 的明智整合，必須執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="5a30d-253">To integrate with Wise for Windows Installer, these steps have to be done:</span></span>

1.  <span data-ttu-id="5a30d-254">以您的 Windows Installer 專案為您開放。</span><span class="sxs-lookup"><span data-stu-id="5a30d-254">Open your Wise for Windows Installer project.</span></span>
2.  <span data-ttu-id="5a30d-255">選取底部的 [安裝專家] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="5a30d-255">Select the "Installation Expert" tab at the bottom.</span></span>
3.  <span data-ttu-id="5a30d-256">按一下 [檔案]，然後將 FirewallInstallHelper.dll 從 DXSDK 新增至遊戲的安裝目錄。</span><span class="sxs-lookup"><span data-stu-id="5a30d-256">Click on Files, and add the FirewallInstallHelper.dll from the DXSDK to the game's install directory.</span></span>
4.  <span data-ttu-id="5a30d-257">選取底部的 [MSI 腳本] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="5a30d-257">Select the "MSI script" tab at the bottom.</span></span>
5.  <span data-ttu-id="5a30d-258">選取靠近底部的 [立即執行] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="5a30d-258">Select the "Execute Immediate" tab near the bottom.</span></span>
6.  <span data-ttu-id="5a30d-259">CostFinalize 之後，新增「設定屬性」動作，將 FULLPATH 設定為「 \[ \] 從安裝目錄 INSTALLDIR 可執行檔的相對路徑」。</span><span class="sxs-lookup"><span data-stu-id="5a30d-259">After CostFinalize, add a "Set Property" action that sets FULLPATH to "\[INSTALLDIR\]relative path to executable from install directory".</span></span> <span data-ttu-id="5a30d-260">例如，" \[ INSTALLDIR \]game.exe"，沒有引號</span><span class="sxs-lookup"><span data-stu-id="5a30d-260">For example, "\[INSTALLDIR\]game.exe" without the quotes</span></span>
7.  <span data-ttu-id="5a30d-261">選取靠近底部的 [執行延後] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="5a30d-261">Select the "Execute Deferred" tab near the bottom.</span></span>
8.  <span data-ttu-id="5a30d-262">PublishProduct 之後，請將 "If 語句" 加入條件為「未安裝」 (區分大小寫的) 。</span><span class="sxs-lookup"><span data-stu-id="5a30d-262">After PublishProduct, add an "If statement" with the condition "NOT Installed" (case sensitive).</span></span>
9.  <span data-ttu-id="5a30d-263">在 If 區塊內，新增「從目的地呼叫自訂 DLL」動作。</span><span class="sxs-lookup"><span data-stu-id="5a30d-263">Within the If block, add a "Call Custom DLL from Destination" action.</span></span>

    1.  <span data-ttu-id="5a30d-264">將 [DLL 檔案] 欄位設定為 [ \[ INSTALLDIR \]FirewallInstallHelper.dll]。</span><span class="sxs-lookup"><span data-stu-id="5a30d-264">Set the DLL File field to "\[INSTALLDIR\]FirewallInstallHelper.dll."</span></span>
    2.  <span data-ttu-id="5a30d-265">將 [函數名稱] 欄位設定為 "AddApplicationToExceptionListA"。</span><span class="sxs-lookup"><span data-stu-id="5a30d-265">Set the Function Name field to "AddApplicationToExceptionListA."</span></span>
    3.  <span data-ttu-id="5a30d-266">新增類型為 "string 指標"、值來源為 "Property" 和屬性名稱 "FULLPATH" 的參數。</span><span class="sxs-lookup"><span data-stu-id="5a30d-266">Add a parameter with type "string pointer", value source "Property", and property name "FULLPATH."</span></span>
    4.  <span data-ttu-id="5a30d-267">新增類型為「字串指標」、值來源為「常數」的第二個參數，並將常數值設定為您想要在防火牆例外清單中顯示的易記應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="5a30d-267">Add a second parameter with type "string pointer", value source "Constant", and set the constant value to the friendly application name you want displayed in the firewall exception list.</span></span>
    5.  <span data-ttu-id="5a30d-268">藉由新增 "End 語句" 來關閉 If 區塊。</span><span class="sxs-lookup"><span data-stu-id="5a30d-268">Close the If block by adding an "End Statement."</span></span>

10. <span data-ttu-id="5a30d-269">在靠近頂端的 RemoveFiles 動作正上方，新增另一個 If block，條件為 "REMOVE ~ =" ALL "" (區分大小寫，且不含外部引號) 。</span><span class="sxs-lookup"><span data-stu-id="5a30d-269">Just above the RemoveFiles action near the top, add another If block, with the condition to be "REMOVE~="ALL"" (case sensitive and without the outer quotes).</span></span>
11. <span data-ttu-id="5a30d-270">在第二個 If 區塊內，新增「從目的地呼叫自訂 DLL」動作。</span><span class="sxs-lookup"><span data-stu-id="5a30d-270">Within the second If block, add a "Call Custom DLL from Destination" action.</span></span>

    1.  <span data-ttu-id="5a30d-271">將 [DLL 檔案] 欄位設定為 [ \[ INSTALLDIR \]FirewallInstallHelper.dll]。</span><span class="sxs-lookup"><span data-stu-id="5a30d-271">Set the DLL File field to "\[INSTALLDIR\]FirewallInstallHelper.dll."</span></span>
    2.  <span data-ttu-id="5a30d-272">將 [函數名稱] 欄位設定為 "RemoveApplicationFromExceptionListA"。</span><span class="sxs-lookup"><span data-stu-id="5a30d-272">Set the Function Name field to "RemoveApplicationFromExceptionListA."</span></span>
    3.  <span data-ttu-id="5a30d-273">新增類型為 "string 指標"、值來源為 "Property" 和屬性名稱 "FULLPATH" 的參數。</span><span class="sxs-lookup"><span data-stu-id="5a30d-273">Add a parameter with type "string pointer", value source "Property", and property name "FULLPATH."</span></span>
    4.  <span data-ttu-id="5a30d-274">藉由新增「結束語句」來關閉第二個 If 區塊。</span><span class="sxs-lookup"><span data-stu-id="5a30d-274">Close the second If block by adding an "End Statement."</span></span>

## <a name="integrating-into-windows-installer"></a><span data-ttu-id="5a30d-275">整合至 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="5a30d-275">Integrating into Windows Installer</span></span>

<span data-ttu-id="5a30d-276">若要與高階 Windows Installer 整合，必須執行這些步驟。</span><span class="sxs-lookup"><span data-stu-id="5a30d-276">To integrate with Windows Installer at the high level, these steps have to be done.</span></span> <span data-ttu-id="5a30d-277">以下將詳細說明這些步驟：</span><span class="sxs-lookup"><span data-stu-id="5a30d-277">They will be explained in detail below:</span></span>

-   <span data-ttu-id="5a30d-278">新增2個屬性 "FriendlyNameForFirewall" 和 "RelativePathToExeForFirewall"，如下所述。</span><span class="sxs-lookup"><span data-stu-id="5a30d-278">Add 2 properties "FriendlyNameForFirewall" and "RelativePathToExeForFirewall" as described below.</span></span>
-   <span data-ttu-id="5a30d-279">在 CostFinalize 動作之後，請在立即自訂動作中呼叫 "SetMSIFirewallProperties"，以針對其他自訂動作設定適當的 MSI 屬性。</span><span class="sxs-lookup"><span data-stu-id="5a30d-279">After the CostFinalize action, call "SetMSIFirewallProperties" in an immediate custom action to set the appropriate MSI properties for the other custom actions.</span></span>
-   <span data-ttu-id="5a30d-280">在安裝 InstallFiles 動作之後，請呼叫使用 FirewallInstallHelper 之 "AddToExceptionListUsingMSI" 函式的延遲自訂動作。</span><span class="sxs-lookup"><span data-stu-id="5a30d-280">During install after the InstallFiles action, call a deferred custom action that uses the FirewallInstallHelper's "AddToExceptionListUsingMSI" function.</span></span>
-   <span data-ttu-id="5a30d-281">在 InstallFiles 動作之後的卸載期間，呼叫使用 FirewallInstallHelper 之 "RemoveFromExceptionListUsingMSI" 函式的延遲自訂動作。</span><span class="sxs-lookup"><span data-stu-id="5a30d-281">During uninstall after the InstallFiles action, call a deferred custom action that uses the FirewallInstallHelper's "RemoveFromExceptionListUsingMSI" function.</span></span>
-   <span data-ttu-id="5a30d-282">在復原期間，呼叫延遲的自訂動作，此動作也會呼叫 FirewallInstallHelper 的 "RemoveFromExceptionListUsingMSI" 函式。</span><span class="sxs-lookup"><span data-stu-id="5a30d-282">During rollback, call a deferred custom action which also calls the FirewallInstallHelper's "RemoveFromExceptionListUsingMSI" function.</span></span>

<span data-ttu-id="5a30d-283">以下是使用 MSI 編輯器（例如在 Platform SDK 中找到的 Orca）執行這項作業所需的步驟。</span><span class="sxs-lookup"><span data-stu-id="5a30d-283">The following is the steps needed to do this using an MSI editor such as Orca found in the Platform SDK.</span></span> <span data-ttu-id="5a30d-284">請注意，有些編輯器具有可簡化其中一些步驟的嚮導：</span><span class="sxs-lookup"><span data-stu-id="5a30d-284">Note that some editors have wizards that simplify some of these steps:</span></span>

1.  <span data-ttu-id="5a30d-285">以 Orca 開啟 MSI 套件。</span><span class="sxs-lookup"><span data-stu-id="5a30d-285">Open the MSI package in Orca.</span></span>
2.  <span data-ttu-id="5a30d-286">將下列內容新增至二進位資料表：</span><span class="sxs-lookup"><span data-stu-id="5a30d-286">Add the following to the Binary table:</span></span>

    

    | <span data-ttu-id="5a30d-287">Name</span><span class="sxs-lookup"><span data-stu-id="5a30d-287">Name</span></span>     | <span data-ttu-id="5a30d-288">資料</span><span class="sxs-lookup"><span data-stu-id="5a30d-288">Data</span></span>                                                                                                                                                                          |
    |----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="5a30d-289">防火牆</span><span class="sxs-lookup"><span data-stu-id="5a30d-289">FIREWALL</span></span> | <span data-ttu-id="5a30d-290">將它指向 FirewallInstallHelper.dll。</span><span class="sxs-lookup"><span data-stu-id="5a30d-290">Point it to the FirewallInstallHelper.dll.</span></span> <span data-ttu-id="5a30d-291">此檔案將內嵌在 MSI 套件中，因此每次重新編譯 FirewallInstallHelper.dll 時，您都必須執行此步驟。</span><span class="sxs-lookup"><span data-stu-id="5a30d-291">This file will be embedded in the MSI package so you will have to do this step every time you recompile FirewallInstallHelper.dll.</span></span> |

    

     

3.  <span data-ttu-id="5a30d-292">將下列內容新增至 CustomAction 資料表：</span><span class="sxs-lookup"><span data-stu-id="5a30d-292">Add the following to CustomAction table:</span></span>

    

    | <span data-ttu-id="5a30d-293">動作</span><span class="sxs-lookup"><span data-stu-id="5a30d-293">Action</span></span>                   | <span data-ttu-id="5a30d-294">類型</span><span class="sxs-lookup"><span data-stu-id="5a30d-294">Type</span></span>                                                                                                                                                                                                   | <span data-ttu-id="5a30d-295">來源</span><span class="sxs-lookup"><span data-stu-id="5a30d-295">Source</span></span>   | <span data-ttu-id="5a30d-296">目標</span><span class="sxs-lookup"><span data-stu-id="5a30d-296">Target</span></span>                          |
    |--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------|---------------------------------|
    | <span data-ttu-id="5a30d-297">FirewallSetMSIProperties</span><span class="sxs-lookup"><span data-stu-id="5a30d-297">FirewallSetMSIProperties</span></span> | <span data-ttu-id="5a30d-298">msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue = 65</span><span class="sxs-lookup"><span data-stu-id="5a30d-298">msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue = 65</span></span>                                                                                                        | <span data-ttu-id="5a30d-299">防火牆</span><span class="sxs-lookup"><span data-stu-id="5a30d-299">FIREWALL</span></span> | <span data-ttu-id="5a30d-300">SetMSIFirewallProperties</span><span class="sxs-lookup"><span data-stu-id="5a30d-300">SetMSIFirewallProperties</span></span>        |
    | <span data-ttu-id="5a30d-301">FirewallAdd</span><span class="sxs-lookup"><span data-stu-id="5a30d-301">FirewallAdd</span></span>              | <span data-ttu-id="5a30d-302">msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137</span><span class="sxs-lookup"><span data-stu-id="5a30d-302">msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137</span></span>                                 | <span data-ttu-id="5a30d-303">防火牆</span><span class="sxs-lookup"><span data-stu-id="5a30d-303">FIREWALL</span></span> | <span data-ttu-id="5a30d-304">AddToExceptionListUsingMSI</span><span class="sxs-lookup"><span data-stu-id="5a30d-304">AddToExceptionListUsingMSI</span></span>      |
    | <span data-ttu-id="5a30d-305">FirewallRemove</span><span class="sxs-lookup"><span data-stu-id="5a30d-305">FirewallRemove</span></span>           | <span data-ttu-id="5a30d-306">msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137</span><span class="sxs-lookup"><span data-stu-id="5a30d-306">msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137</span></span>                                 | <span data-ttu-id="5a30d-307">防火牆</span><span class="sxs-lookup"><span data-stu-id="5a30d-307">FIREWALL</span></span> | <span data-ttu-id="5a30d-308">RemoveFromExceptionListUsingMSI</span><span class="sxs-lookup"><span data-stu-id="5a30d-308">RemoveFromExceptionListUsingMSI</span></span> |
    | <span data-ttu-id="5a30d-309">FirewallRollBackAdd</span><span class="sxs-lookup"><span data-stu-id="5a30d-309">FirewallRollBackAdd</span></span>      | <span data-ttu-id="5a30d-310">msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3393</span><span class="sxs-lookup"><span data-stu-id="5a30d-310">msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3393</span></span> | <span data-ttu-id="5a30d-311">防火牆</span><span class="sxs-lookup"><span data-stu-id="5a30d-311">FIREWALL</span></span> | <span data-ttu-id="5a30d-312">RemoveFromExceptionListUsingMSI</span><span class="sxs-lookup"><span data-stu-id="5a30d-312">RemoveFromExceptionListUsingMSI</span></span> |
    | <span data-ttu-id="5a30d-313">FirewallRollBackRemove</span><span class="sxs-lookup"><span data-stu-id="5a30d-313">FirewallRollBackRemove</span></span>   | <span data-ttu-id="5a30d-314">msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3393</span><span class="sxs-lookup"><span data-stu-id="5a30d-314">msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3393</span></span> | <span data-ttu-id="5a30d-315">防火牆</span><span class="sxs-lookup"><span data-stu-id="5a30d-315">FIREWALL</span></span> | <span data-ttu-id="5a30d-316">AddToExceptionListUsingMSI</span><span class="sxs-lookup"><span data-stu-id="5a30d-316">AddToExceptionListUsingMSI</span></span>      |

    

     

4.  <span data-ttu-id="5a30d-317">將下列內容新增至 InstallExecuteSequence 資料表：</span><span class="sxs-lookup"><span data-stu-id="5a30d-317">Add the following to the InstallExecuteSequence table:</span></span>

    

    | <span data-ttu-id="5a30d-318">動作</span><span class="sxs-lookup"><span data-stu-id="5a30d-318">Action</span></span>                   | <span data-ttu-id="5a30d-319">條件</span><span class="sxs-lookup"><span data-stu-id="5a30d-319">Condition</span></span>     | <span data-ttu-id="5a30d-320">順序</span><span class="sxs-lookup"><span data-stu-id="5a30d-320">Sequence</span></span> | <span data-ttu-id="5a30d-321">備註</span><span class="sxs-lookup"><span data-stu-id="5a30d-321">Notes</span></span>                                                                                                                                                                      |
    |--------------------------|---------------|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="5a30d-322">FirewallSetMSIProperties</span><span class="sxs-lookup"><span data-stu-id="5a30d-322">FirewallSetMSIProperties</span></span> |               | <span data-ttu-id="5a30d-323">1010</span><span class="sxs-lookup"><span data-stu-id="5a30d-323">1010</span></span>     | <span data-ttu-id="5a30d-324">CostFinalize 之後，就會有這種情況。</span><span class="sxs-lookup"><span data-stu-id="5a30d-324">This places soon after CostFinalize.</span></span>                                                                                                                                       |
    | <span data-ttu-id="5a30d-325">FirewallAdd</span><span class="sxs-lookup"><span data-stu-id="5a30d-325">FirewallAdd</span></span>              | <span data-ttu-id="5a30d-326">未安裝</span><span class="sxs-lookup"><span data-stu-id="5a30d-326">NOT Installed</span></span> | <span data-ttu-id="5a30d-327">4021</span><span class="sxs-lookup"><span data-stu-id="5a30d-327">4021</span></span>     | <span data-ttu-id="5a30d-328">此自訂動作只會在全新安裝期間發生。</span><span class="sxs-lookup"><span data-stu-id="5a30d-328">This custom action will only happen during a fresh install.</span></span> <span data-ttu-id="5a30d-329">序號會將動作放在 InstallFiles 之後和復原之後。</span><span class="sxs-lookup"><span data-stu-id="5a30d-329">The sequence number places the action after InstallFiles and after the rollbacks.</span></span>                              |
    | <span data-ttu-id="5a30d-330">FirewallRollBackAdd</span><span class="sxs-lookup"><span data-stu-id="5a30d-330">FirewallRollBackAdd</span></span>      | <span data-ttu-id="5a30d-331">未安裝</span><span class="sxs-lookup"><span data-stu-id="5a30d-331">NOT Installed</span></span> | <span data-ttu-id="5a30d-332">4020</span><span class="sxs-lookup"><span data-stu-id="5a30d-332">4020</span></span>     | <span data-ttu-id="5a30d-333">只有在取消全新安裝時，才會發生此自訂動作。</span><span class="sxs-lookup"><span data-stu-id="5a30d-333">This custom action will only happen when a fresh install is cancelled.</span></span> <span data-ttu-id="5a30d-334">序號會將動作放在 InstallFiles 之後，以及加入自訂動作之前。</span><span class="sxs-lookup"><span data-stu-id="5a30d-334">The sequence number places the action after InstallFiles and before the Add custom action.</span></span>          |
    | <span data-ttu-id="5a30d-335">FirewallRemove</span><span class="sxs-lookup"><span data-stu-id="5a30d-335">FirewallRemove</span></span>           | <span data-ttu-id="5a30d-336">已安裝</span><span class="sxs-lookup"><span data-stu-id="5a30d-336">Installed</span></span>     | <span data-ttu-id="5a30d-337">3461</span><span class="sxs-lookup"><span data-stu-id="5a30d-337">3461</span></span>     | <span data-ttu-id="5a30d-338">此自訂動作只會在卸載期間發生。</span><span class="sxs-lookup"><span data-stu-id="5a30d-338">This custom action will only happen during uninstall.</span></span> <span data-ttu-id="5a30d-339">序號會在 RemoveFiles 之前和復原之後直接放置動作。</span><span class="sxs-lookup"><span data-stu-id="5a30d-339">The sequence number places the action directly before RemoveFiles and after the rollbacks.</span></span>                           |
    | <span data-ttu-id="5a30d-340">FirewallRollBackRemove</span><span class="sxs-lookup"><span data-stu-id="5a30d-340">FirewallRollBackRemove</span></span>   | <span data-ttu-id="5a30d-341">未安裝</span><span class="sxs-lookup"><span data-stu-id="5a30d-341">NOT Installed</span></span> | <span data-ttu-id="5a30d-342">3460</span><span class="sxs-lookup"><span data-stu-id="5a30d-342">3460</span></span>     | <span data-ttu-id="5a30d-343">只有在取消卸載時，才會發生此自訂動作。</span><span class="sxs-lookup"><span data-stu-id="5a30d-343">This custom action will only happen when an uninstall is cancelled.</span></span> <span data-ttu-id="5a30d-344">序號會在 RemoveFiles 之前，以及在移除自訂動作之前，直接放置動作。</span><span class="sxs-lookup"><span data-stu-id="5a30d-344">The sequence number places the action directly before RemoveFiles and before the Remove custom action.</span></span> |

    

     

5.  <span data-ttu-id="5a30d-345">將下列內容新增至屬性工作表：</span><span class="sxs-lookup"><span data-stu-id="5a30d-345">Add the following to the Property table:</span></span>

    

    | <span data-ttu-id="5a30d-346">屬性</span><span class="sxs-lookup"><span data-stu-id="5a30d-346">Property</span></span>                     | <span data-ttu-id="5a30d-347">值</span><span class="sxs-lookup"><span data-stu-id="5a30d-347">Value</span></span>                                                                             |
    |------------------------------|-----------------------------------------------------------------------------------|
    | <span data-ttu-id="5a30d-348">FriendlyNameForFirewall</span><span class="sxs-lookup"><span data-stu-id="5a30d-348">FriendlyNameForFirewall</span></span>      | <span data-ttu-id="5a30d-349">必須是例外狀況清單會顯示的名稱。</span><span class="sxs-lookup"><span data-stu-id="5a30d-349">Needs to be the name the exception list will display.</span></span> <span data-ttu-id="5a30d-350">例如，「範例遊戲」</span><span class="sxs-lookup"><span data-stu-id="5a30d-350">For example, "Example Game"</span></span> |
    | <span data-ttu-id="5a30d-351">RelativePathToExeForFirewall</span><span class="sxs-lookup"><span data-stu-id="5a30d-351">RelativePathToExeForFirewall</span></span> | <span data-ttu-id="5a30d-352">必須是遊戲已安裝的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="5a30d-352">Needs to be the installed executable of the game.</span></span> <span data-ttu-id="5a30d-353">例如，"ExampleGame.exe"</span><span class="sxs-lookup"><span data-stu-id="5a30d-353">For example, "ExampleGame.exe"</span></span>  |

    

     

<span data-ttu-id="5a30d-354">如需 Windows Installer 的詳細資訊，請參閱 [Windows Installer](/windows/desktop/Msi/windows-installer-portal)。</span><span class="sxs-lookup"><span data-stu-id="5a30d-354">For more information on Windows Installer, see [Windows Installer](/windows/desktop/Msi/windows-installer-portal).</span></span>

## <a name="recommendations"></a><span data-ttu-id="5a30d-355">建議</span><span class="sxs-lookup"><span data-stu-id="5a30d-355">Recommendations</span></span>

<span data-ttu-id="5a30d-356">防火牆在此保持不變。</span><span class="sxs-lookup"><span data-stu-id="5a30d-356">The firewall is here to stay.</span></span> <span data-ttu-id="5a30d-357">這些建議會為您的客戶提供良好的 Windows 遊戲防火牆體驗：</span><span class="sxs-lookup"><span data-stu-id="5a30d-357">These recommendations will give your customers a good firewall experience with your Windows game:</span></span>

-   <span data-ttu-id="5a30d-358">不要告訴使用者停用防火牆來播放您的遊戲。</span><span class="sxs-lookup"><span data-stu-id="5a30d-358">Don't tell users to disable the firewall to play your game.</span></span> <span data-ttu-id="5a30d-359">這樣一來，即使電腦不在玩遊戲時，也會讓整個電腦容易受到攻擊。</span><span class="sxs-lookup"><span data-stu-id="5a30d-359">This makes the entire machine vulnerable even when they aren't playing your game.</span></span>
-   <span data-ttu-id="5a30d-360">讓您的使用者無縫設定防火牆。</span><span class="sxs-lookup"><span data-stu-id="5a30d-360">Make the firewall configuration seamless for your users.</span></span> <span data-ttu-id="5a30d-361">在安裝期間將您的應用程式新增至例外狀況清單，並在安裝期間從例外清單中移除您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="5a30d-361">Add your application to the exception list during installation, and remove your application from the exception list during installation.</span></span>
-   <span data-ttu-id="5a30d-362">如果有多人遭到防火牆狀態封鎖，請將意見反應提供給使用者。</span><span class="sxs-lookup"><span data-stu-id="5a30d-362">Give feedback to the user if multiplayer is blocked by the firewall state.</span></span> <span data-ttu-id="5a30d-363">例如，如果網路功能無法運作，請停用它們，因為應用程式不允許或因為系統處於「無例外狀況」模式。</span><span class="sxs-lookup"><span data-stu-id="5a30d-363">For example, disable networking features if they won't work either because the application is disallowed or because the system is in the "no exceptions" mode.</span></span>

 

 
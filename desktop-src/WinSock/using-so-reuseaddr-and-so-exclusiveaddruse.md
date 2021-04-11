---
description: 開發安全的高階網路基礎結構是大部分網路應用程式開發人員的優先考慮。 不過，在考慮完全安全的解決方案時，通常會忽略通訊端安全性，儘管非常重要。
ms.assetid: b37a3e33-65ee-43b1-bc8b-3280db7ebee4
title: 使用 SO_REUSEADDR 和 SO_EXCLUSIVEADDRUSE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaa4024f031102cbd634c235bb39f4c7860e6c1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693307"
---
# <a name="using-so_reuseaddr-and-so_exclusiveaddruse"></a><span data-ttu-id="cb8d0-104">使用 \_ REUSEADDR 等 \_ EXCLUSIVEADDRUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-104">Using SO\_REUSEADDR and SO\_EXCLUSIVEADDRUSE</span></span>

<span data-ttu-id="cb8d0-105">開發安全的高階網路基礎結構是大部分網路應用程式開發人員的優先考慮。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-105">Developing a secure high-level network infrastructure is a priority for most network application developers.</span></span> <span data-ttu-id="cb8d0-106">不過，在考慮完全安全的解決方案時，通常會忽略通訊端安全性，儘管非常重要。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-106">However, socket security is often overlooked despite being very critical when considering a fully secure solution.</span></span> <span data-ttu-id="cb8d0-107">通訊端安全性特別是處理系結至先前由另一個應用程式進程所系結之相同埠的處理常式。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-107">Socket security, specifically, deals with processes that bind to the same port previously bound by another application process.</span></span> <span data-ttu-id="cb8d0-108">在過去，網路應用程式可能會「劫持」另一個應用程式的埠，而這可能會造成「阻絕服務」攻擊或資料遭竊。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-108">In the past, it was possible for a network application to "hijack" the port of another application, which could easily lead to a "denial of service" attack or data theft.</span></span>

<span data-ttu-id="cb8d0-109">通常，通訊端安全性適用于伺服器端進程。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-109">In general, socket security applies to server-side processes.</span></span> <span data-ttu-id="cb8d0-110">更具體來說，通訊端安全性適用于接受連線並接收 IP 資料包流量的任何網路應用程式。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-110">More specifically, socket security applies to any network application that accepts connections and receives IP datagram traffic.</span></span> <span data-ttu-id="cb8d0-111">這些應用程式通常會系結至知名的埠，且為惡意網路程式碼的常見目標。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-111">These applications typically bind to a well-known port and are common targets for malicious network code.</span></span>

<span data-ttu-id="cb8d0-112">用戶端應用程式較不可能是這類攻擊的目標，因為它們較不容易受到影響，但因為大部分的用戶端系結至「暫時」本機埠，而不是靜態「服務」埠。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-112">Client applications are less likely to be the targets of such attacks — not because they are less susceptible, but because most clients bind to "ephemeral" local ports rather than static "service" ports.</span></span> <span data-ttu-id="cb8d0-113">用戶端網路應用程式應該一律系結至暫時埠 (方法是在呼叫系結函式時，于 *name* 參數所 [](/windows/win32/api/winsock/nf-winsock-bind)指向的 [**SOCKADDR**](sockaddr-2.md)結構中指定埠0，) 除非有吸引人的架構原因。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-113">Client network applications should always bind to ephemeral ports (by specifying port 0 in the [**SOCKADDR**](sockaddr-2.md) structure pointed to by the *name* parameter when calling the [**bind**](/windows/win32/api/winsock/nf-winsock-bind) function) unless there is a compelling architectural reason not to.</span></span> <span data-ttu-id="cb8d0-114">暫時本機埠是由埠49151以上的埠所組成。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-114">The ephemeral local ports consist of ports greater than port 49151.</span></span> <span data-ttu-id="cb8d0-115">專用服務的大部分伺服器應用程式都會系結至小於或等於埠49151的知名保留埠。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-115">Most server applications for dedicated services bind to a well-known reserved port that is less than or equal to port 49151.</span></span> <span data-ttu-id="cb8d0-116">因此，在大部分的應用程式中，用戶端與伺服器應用程式之間的系結要求通常不會發生衝突。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-116">So for most applications, there is not usually a conflict for bind requests between client and server applications.</span></span>

<span data-ttu-id="cb8d0-117">本節說明各種 Microsoft Windows 平臺上的預設安全性層級，以及特定通訊端選項 **\_ REUSEADDR** 和 [ \_ EXCLUSIVEADDRUSE](so-exclusiveaddruse.md) 的影響，以及對網路應用程式安全性的影響。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-117">This section describes the default level of security on various Microsoft Windows platforms and how the specific socket options **SO\_REUSEADDR** and [SO\_EXCLUSIVEADDRUSE](so-exclusiveaddruse.md) impact and affect network application security.</span></span> <span data-ttu-id="cb8d0-118">Windows Server 2003 和更新版本上提供另一項稱為增強通訊端安全性的功能。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-118">An additional feature called enhanced socket security is available on Windows Server 2003 and later.</span></span> <span data-ttu-id="cb8d0-119">這些通訊端選項和增強通訊端安全性的可用性會因不同的 Microsoft 作業系統版本而異，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-119">The availability of these socket options and enhanced socket security varies across versions of Microsoft operating systems, as shown in the table below.</span></span>

| <span data-ttu-id="cb8d0-120">平台</span><span class="sxs-lookup"><span data-stu-id="cb8d0-120">Platform</span></span>            | <span data-ttu-id="cb8d0-121">\_REUSEADDR</span><span class="sxs-lookup"><span data-stu-id="cb8d0-121">SO\_REUSEADDR</span></span> | <span data-ttu-id="cb8d0-122">\_EXCLUSIVEADDRUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-122">SO\_EXCLUSIVEADDRUSE</span></span>                  | <span data-ttu-id="cb8d0-123">增強通訊端安全性</span><span class="sxs-lookup"><span data-stu-id="cb8d0-123">Enhanced socket security</span></span> |
|---------------------|---------------|---------------------------------------|--------------------------|
| <span data-ttu-id="cb8d0-124">Windows 95</span><span class="sxs-lookup"><span data-stu-id="cb8d0-124">Windows 95</span></span>          | <span data-ttu-id="cb8d0-125">可用</span><span class="sxs-lookup"><span data-stu-id="cb8d0-125">Available</span></span>     | <span data-ttu-id="cb8d0-126">無法使用</span><span class="sxs-lookup"><span data-stu-id="cb8d0-126">Not Available</span></span>                         | <span data-ttu-id="cb8d0-127">無法使用</span><span class="sxs-lookup"><span data-stu-id="cb8d0-127">Not Available</span></span>            |
| <span data-ttu-id="cb8d0-128">Windows 98</span><span class="sxs-lookup"><span data-stu-id="cb8d0-128">Windows 98</span></span>          | <span data-ttu-id="cb8d0-129">可用</span><span class="sxs-lookup"><span data-stu-id="cb8d0-129">Available</span></span>     | <span data-ttu-id="cb8d0-130">無法使用</span><span class="sxs-lookup"><span data-stu-id="cb8d0-130">Not Available</span></span>                         | <span data-ttu-id="cb8d0-131">無法使用</span><span class="sxs-lookup"><span data-stu-id="cb8d0-131">Not Available</span></span>            |
| <span data-ttu-id="cb8d0-132">Windows Me</span><span class="sxs-lookup"><span data-stu-id="cb8d0-132">Windows Me</span></span>          | <span data-ttu-id="cb8d0-133">可用</span><span class="sxs-lookup"><span data-stu-id="cb8d0-133">Available</span></span>     | <span data-ttu-id="cb8d0-134">無法使用</span><span class="sxs-lookup"><span data-stu-id="cb8d0-134">Not Available</span></span>                         | <span data-ttu-id="cb8d0-135">無法使用</span><span class="sxs-lookup"><span data-stu-id="cb8d0-135">Not Available</span></span>            |
| <span data-ttu-id="cb8d0-136">Windows NT 4.0</span><span class="sxs-lookup"><span data-stu-id="cb8d0-136">Windows NT 4.0</span></span>      | <span data-ttu-id="cb8d0-137">可用</span><span class="sxs-lookup"><span data-stu-id="cb8d0-137">Available</span></span>     | <span data-ttu-id="cb8d0-138">可在 Service Pack 4 和更新版本中使用</span><span class="sxs-lookup"><span data-stu-id="cb8d0-138">Available in Service Pack 4 and later</span></span> | <span data-ttu-id="cb8d0-139">無法使用</span><span class="sxs-lookup"><span data-stu-id="cb8d0-139">Not Available</span></span>            |
| <span data-ttu-id="cb8d0-140">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="cb8d0-140">Windows 2000</span></span>        | <span data-ttu-id="cb8d0-141">可用</span><span class="sxs-lookup"><span data-stu-id="cb8d0-141">Available</span></span>     | <span data-ttu-id="cb8d0-142">可用</span><span class="sxs-lookup"><span data-stu-id="cb8d0-142">Available</span></span>                             | <span data-ttu-id="cb8d0-143">無法使用</span><span class="sxs-lookup"><span data-stu-id="cb8d0-143">Not Available</span></span>            |
| <span data-ttu-id="cb8d0-144">Windows XP</span><span class="sxs-lookup"><span data-stu-id="cb8d0-144">Windows XP</span></span>          | <span data-ttu-id="cb8d0-145">可用</span><span class="sxs-lookup"><span data-stu-id="cb8d0-145">Available</span></span>     | <span data-ttu-id="cb8d0-146">可用</span><span class="sxs-lookup"><span data-stu-id="cb8d0-146">Available</span></span>                             | <span data-ttu-id="cb8d0-147">無法使用</span><span class="sxs-lookup"><span data-stu-id="cb8d0-147">Not Available</span></span>            |
| <span data-ttu-id="cb8d0-148">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cb8d0-148">Windows Server 2003</span></span> | <span data-ttu-id="cb8d0-149">可用</span><span class="sxs-lookup"><span data-stu-id="cb8d0-149">Available</span></span>     | <span data-ttu-id="cb8d0-150">可用</span><span class="sxs-lookup"><span data-stu-id="cb8d0-150">Available</span></span>                             | <span data-ttu-id="cb8d0-151">可用</span><span class="sxs-lookup"><span data-stu-id="cb8d0-151">Available</span></span>                |
| <span data-ttu-id="cb8d0-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cb8d0-152">Windows Vista</span></span>       | <span data-ttu-id="cb8d0-153">可用</span><span class="sxs-lookup"><span data-stu-id="cb8d0-153">Available</span></span>     | <span data-ttu-id="cb8d0-154">可用</span><span class="sxs-lookup"><span data-stu-id="cb8d0-154">Available</span></span>                             | <span data-ttu-id="cb8d0-155">可用</span><span class="sxs-lookup"><span data-stu-id="cb8d0-155">Available</span></span>                |
| <span data-ttu-id="cb8d0-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cb8d0-156">Windows Server 2008</span></span> | <span data-ttu-id="cb8d0-157">可用</span><span class="sxs-lookup"><span data-stu-id="cb8d0-157">Available</span></span>     | <span data-ttu-id="cb8d0-158">可用</span><span class="sxs-lookup"><span data-stu-id="cb8d0-158">Available</span></span>                             | <span data-ttu-id="cb8d0-159">可用</span><span class="sxs-lookup"><span data-stu-id="cb8d0-159">Available</span></span>                |
| <span data-ttu-id="cb8d0-160">Windows 7and 更新版本</span><span class="sxs-lookup"><span data-stu-id="cb8d0-160">Windows 7and newer</span></span>  | <span data-ttu-id="cb8d0-161">可用</span><span class="sxs-lookup"><span data-stu-id="cb8d0-161">Available</span></span>     | <span data-ttu-id="cb8d0-162">可用</span><span class="sxs-lookup"><span data-stu-id="cb8d0-162">Available</span></span>                             | <span data-ttu-id="cb8d0-163">可用</span><span class="sxs-lookup"><span data-stu-id="cb8d0-163">Available</span></span>                |

## <a name="using-so_reuseaddr"></a><span data-ttu-id="cb8d0-164">使用 \_ REUSEADDR</span><span class="sxs-lookup"><span data-stu-id="cb8d0-164">Using SO\_REUSEADDR</span></span>

<span data-ttu-id="cb8d0-165">**SO \_ REUSEADDR** 通訊端選項可讓通訊端強制系結至另一個通訊端使用的埠。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-165">The **SO\_REUSEADDR** socket option allows a socket to forcibly bind to a port in use by another socket.</span></span> <span data-ttu-id="cb8d0-166">第二個通訊端會呼叫 [**setsockopt**](/windows/win32/api/winsock/nf-winsock-setsockopt) ，並將 *optname* 參數設定為 **\_ REUSEADDR** ，並將 *optval* 參數設定為布林值 **TRUE** ，然後再于與原始通訊端相同的 [**埠上呼叫**](/windows/win32/api/winsock/nf-winsock-bind) 系結。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-166">The second socket calls [**setsockopt**](/windows/win32/api/winsock/nf-winsock-setsockopt) with the *optname* parameter set to **SO\_REUSEADDR** and the *optval* parameter set to a boolean value of **TRUE** before calling [**bind**](/windows/win32/api/winsock/nf-winsock-bind) on the same port as the original socket.</span></span> <span data-ttu-id="cb8d0-167">第二個通訊端成功系結之後，系結至該通訊埠的所有通訊端行為都不確定。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-167">Once the second socket has successfully bound, the behavior for all sockets bound to that port is indeterminate.</span></span> <span data-ttu-id="cb8d0-168">例如，如果相同埠上的所有通訊端都提供 TCP 服務，則透過埠的任何連入 TCP 連線要求都無法保證由正確的通訊端處理，因為行為是不具決定性的。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-168">For example, if all of the sockets on the same port provide TCP service, any incoming TCP connection requests over the port cannot be guaranteed to be handled by the correct socket — the behavior is non-deterministic.</span></span> <span data-ttu-id="cb8d0-169">惡意的程式可以使用 **\_ REUSEADDR** 強制系結已用於標準網路通訊協定服務的通訊端，以拒絕存取這些服務。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-169">A malicious program can use **SO\_REUSEADDR** to forcibly bind sockets already in use for standard network protocol services in order to deny access to those service.</span></span> <span data-ttu-id="cb8d0-170">使用這個選項不需要任何特殊許可權。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-170">No special privileges are required to use this option.</span></span>

<span data-ttu-id="cb8d0-171">如果用戶端應用程式在伺服器應用程式能夠系結至相同的埠之前系結至埠，則可能會產生問題。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-171">If a client application binds to a port before a server application is able to bind to the same port, then problems may result.</span></span> <span data-ttu-id="cb8d0-172">如果伺服器應用程式使用 **\_ REUSEADDR** 通訊端選項強制系結至相同的埠，則系結至該埠的所有通訊端行為都不確定。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-172">If the server application forcibly binds using the **SO\_REUSEADDR** socket option to the same port, then the behavior for all sockets bound to that port is indeterminate.</span></span>

<span data-ttu-id="cb8d0-173">這種不具決定性行為的例外狀況是多播通訊端。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-173">The exception to this non-deterministic behavior is multicast sockets.</span></span> <span data-ttu-id="cb8d0-174">如果有兩個通訊端系結至相同的介面和埠，而且是相同多播群組的成員，則會將資料傳遞給這兩個通訊端，而非任意選。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-174">If two sockets are bound to the same interface and port and are members of the same multicast group, data will be delivered to both sockets, rather than an arbitrarily chosen one.</span></span>

## <a name="using-so_exclusiveaddruse"></a><span data-ttu-id="cb8d0-175">使用 \_ EXCLUSIVEADDRUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-175">Using SO\_EXCLUSIVEADDRUSE</span></span>

<span data-ttu-id="cb8d0-176">在引進 **\_ EXCLUSIVEADDRUSE** 通訊端選項之前，有幾個網路應用程式開發人員可以避免惡意的程式系結到網路應用程式有自己的通訊端系結的埠。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-176">Before the **SO\_EXCLUSIVEADDRUSE** socket option was introduced, there was very little a network application developer could do to prevent a malicious program from binding to the port on which the network application had its own sockets bound.</span></span> <span data-ttu-id="cb8d0-177">為了解決此安全性問題，Windows 通訊端引進了 **\_ EXCLUSIVEADDRUSE** 通訊端選項，此選項可在 Windows NT 4.0 Service PACK 4 (SP4) 和更新版本中取得。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-177">In order to address this security issue, Windows Sockets introduced the **SO\_EXCLUSIVEADDRUSE** socket option, which became available on Windows NT 4.0 with Service Pack 4 (SP4) and later.</span></span>

<span data-ttu-id="cb8d0-178">**\_ EXCLUSIVEADDRUSE** 通訊端選項只可供 Windows XP 及更早版本上的 Administrators 安全性群組成員使用。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-178">The **SO\_EXCLUSIVEADDRUSE** socket option can only be used by members of the Administrators security group on Windows XP and earlier.</span></span> <span data-ttu-id="cb8d0-179">本文稍後將討論這項需求在 Windows Server 2003 和更新版本上的變更原因。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-179">The reasons why this requirement was changed on Windows Server 2003 and later are discussed later in the article.</span></span>

<span data-ttu-id="cb8d0-180">**\_ EXCLUSIVEADDRUSE** 選項的設定方式是呼叫 [**setsockopt**](/windows/win32/api/winsock/nf-winsock-setsockopt)函數，並將 *optname* 參數設定為 **\_ EXCLUSIVEADDRUSE** ，並在系結器之前，將 *optval* 參數設定為布林值 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-180">The **SO\_EXCLUSIVEADDRUSE** option is set by calling the [**setsockopt**](/windows/win32/api/winsock/nf-winsock-setsockopt) function with the *optname* parameter set to **SO\_EXCLUSIVEADDRUSE** and the *optval* parameter set to a boolean value of **TRUE** before the socket is bound.</span></span> <span data-ttu-id="cb8d0-181">設定選項之後，後續系 **結呼叫的** 行為會視每個系 [**結呼叫中**](/windows/win32/api/winsock/nf-winsock-bind)指定的網路位址而有所不同。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-181">After the option is set, the behavior of subsequent [**bind**](/windows/win32/api/winsock/nf-winsock-bind) calls differs depending on the network address specified in each **bind** call.</span></span>

<span data-ttu-id="cb8d0-182">下表說明當第二個通訊端嘗試系結至使用特定通訊端選項的第一個通訊端之前所系結的位址時，Windows XP 及更早版本中發生的行為。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-182">The table below describes the behavior that occurs in Windows XP and earlier when a second socket attempts to bind to an address previously bound to by a first socket using specific socket options.</span></span>

> [!NOTE]  
> <span data-ttu-id="cb8d0-183">在下表中，"萬用字元" 代表指定通訊協定 (的萬用字元位址，例如 IPv4 的 "0.0.0.0" 和 IPv6) 的 "：："。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-183">In the table below, "wildcard" denotes the wildcard address for the given protocol (such as "0.0.0.0" for IPv4 and "::" for IPv6).</span></span> <span data-ttu-id="cb8d0-184">「特定」代表指派了介面的特定 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-184">"Specific" denotes a specific IP address assigned an interface.</span></span> <span data-ttu-id="cb8d0-185">資料表資料格指出系結是否成功 ( 「成功」 ) ，或針對 [WSAEADDRINUSE](windows-sockets-error-codes-2.md) 錯誤傳回 ( "INUSE" 的錯誤; [WSAEACCES](windows-sockets-error-codes-2.md) 錯誤) 的「存取」。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-185">The table cells indicate whether or not the bind is successful ("Success") or an error is returned ("INUSE" for the [WSAEADDRINUSE](windows-sockets-error-codes-2.md) error; "ACCESS" for the [WSAEACCES](windows-sockets-error-codes-2.md) error).</span></span>

<table>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2" rowspan="3"><span data-ttu-id="cb8d0-186">第 <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>一個</strong></a> 系結呼叫</span><span class="sxs-lookup"><span data-stu-id="cb8d0-186">First <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>bind</strong></a> call</span></span></td>
        <td bgcolor="#C0C0C0" colspan="6"><span data-ttu-id="cb8d0-187">第 <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>二</strong></a> 個系結呼叫</span><span class="sxs-lookup"><span data-stu-id="cb8d0-187">Second <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>bind</strong></a> call</span></span></td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2"><span data-ttu-id="cb8d0-188">預設</span><span class="sxs-lookup"><span data-stu-id="cb8d0-188">Default</span></span></td>
        <td bgcolor="#C0C0C0" colspan="2"><span data-ttu-id="cb8d0-189">SO_REUSEADDR</span><span class="sxs-lookup"><span data-stu-id="cb8d0-189">SO_REUSEADDR</span></span></td>
        <td bgcolor="#C0C0C0" colspan="2"><span data-ttu-id="cb8d0-190">SO_EXCLUSIVEADDRUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-190">SO_EXCLUSIVEADDRUSE</span></span></td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0"><span data-ttu-id="cb8d0-191">萬用字元</span><span class="sxs-lookup"><span data-stu-id="cb8d0-191">Wildcard</span></span></td>
        <td bgcolor="#C0C0C0"><span data-ttu-id="cb8d0-192">特定</span><span class="sxs-lookup"><span data-stu-id="cb8d0-192">Specific</span></span></td>
        <td bgcolor="#C0C0C0"><span data-ttu-id="cb8d0-193">萬用字元</span><span class="sxs-lookup"><span data-stu-id="cb8d0-193">Wildcard</span></span></td>
        <td bgcolor="#C0C0C0"><span data-ttu-id="cb8d0-194">特定</span><span class="sxs-lookup"><span data-stu-id="cb8d0-194">Specific</span></span></td>
        <td bgcolor="#C0C0C0"><span data-ttu-id="cb8d0-195">萬用字元</span><span class="sxs-lookup"><span data-stu-id="cb8d0-195">Wildcard</span></span></td>
        <td bgcolor="#C0C0C0"><span data-ttu-id="cb8d0-196">特定</span><span class="sxs-lookup"><span data-stu-id="cb8d0-196">Specific</span></span></td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2"><span data-ttu-id="cb8d0-197">預設</span><span class="sxs-lookup"><span data-stu-id="cb8d0-197">Default</span></span></td>
        <td bgcolor="#C0C0C0"><span data-ttu-id="cb8d0-198">萬用字元</span><span class="sxs-lookup"><span data-stu-id="cb8d0-198">Wildcard</span></span></td>
        <td><span data-ttu-id="cb8d0-199">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-199">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-200">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-200">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-201">成功</span><span class="sxs-lookup"><span data-stu-id="cb8d0-201">Success</span></span></td>
        <td><span data-ttu-id="cb8d0-202">成功</span><span class="sxs-lookup"><span data-stu-id="cb8d0-202">Success</span></span></td>
        <td><span data-ttu-id="cb8d0-203">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-203">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-204">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-204">INUSE</span></span></td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0"><span data-ttu-id="cb8d0-205">特定</span><span class="sxs-lookup"><span data-stu-id="cb8d0-205">Specific</span></span></td>
        <td><span data-ttu-id="cb8d0-206">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-206">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-207">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-207">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-208">成功</span><span class="sxs-lookup"><span data-stu-id="cb8d0-208">Success</span></span></td>
        <td><span data-ttu-id="cb8d0-209">成功</span><span class="sxs-lookup"><span data-stu-id="cb8d0-209">Success</span></span></td>
        <td><span data-ttu-id="cb8d0-210">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-210">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-211">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-211">INUSE</span></span></td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2"><span data-ttu-id="cb8d0-212">SO_REUSEADDR</span><span class="sxs-lookup"><span data-stu-id="cb8d0-212">SO_REUSEADDR</span></span></td>
        <td bgcolor="#C0C0C0"><span data-ttu-id="cb8d0-213">萬用字元</span><span class="sxs-lookup"><span data-stu-id="cb8d0-213">Wildcard</span></span></td>
        <td><span data-ttu-id="cb8d0-214">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-214">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-215">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-215">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-216">成功</span><span class="sxs-lookup"><span data-stu-id="cb8d0-216">Success</span></span></td>
        <td><span data-ttu-id="cb8d0-217">成功</span><span class="sxs-lookup"><span data-stu-id="cb8d0-217">Success</span></span></td>
        <td><span data-ttu-id="cb8d0-218">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-218">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-219">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-219">INUSE</span></span></td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0"><span data-ttu-id="cb8d0-220">特定</span><span class="sxs-lookup"><span data-stu-id="cb8d0-220">Specific</span></span></td>
        <td><span data-ttu-id="cb8d0-221">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-221">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-222">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-222">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-223">成功</span><span class="sxs-lookup"><span data-stu-id="cb8d0-223">Success</span></span></td>
        <td><span data-ttu-id="cb8d0-224">成功</span><span class="sxs-lookup"><span data-stu-id="cb8d0-224">Success</span></span></td>
        <td><span data-ttu-id="cb8d0-225">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-225">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-226">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-226">INUSE</span></span></td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2"><span data-ttu-id="cb8d0-227">SO_EXCLUSIVEADDRUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-227">SO_EXCLUSIVEADDRUSE</span></span></td>
        <td bgcolor="#C0C0C0"><span data-ttu-id="cb8d0-228">萬用字元</span><span class="sxs-lookup"><span data-stu-id="cb8d0-228">Wildcard</span></span></td>
        <td><span data-ttu-id="cb8d0-229">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-229">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-230">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-230">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-231">ACCESS</span><span class="sxs-lookup"><span data-stu-id="cb8d0-231">ACCESS</span></span></td>
        <td><span data-ttu-id="cb8d0-232">ACCESS</span><span class="sxs-lookup"><span data-stu-id="cb8d0-232">ACCESS</span></span></td>
        <td><span data-ttu-id="cb8d0-233">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-233">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-234">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-234">INUSE</span></span></td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0"><span data-ttu-id="cb8d0-235">特定</span><span class="sxs-lookup"><span data-stu-id="cb8d0-235">Specific</span></span></td>
        <td><span data-ttu-id="cb8d0-236">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-236">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-237">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-237">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-238">ACCESS</span><span class="sxs-lookup"><span data-stu-id="cb8d0-238">ACCESS</span></span></td>
        <td><span data-ttu-id="cb8d0-239">ACCESS</span><span class="sxs-lookup"><span data-stu-id="cb8d0-239">ACCESS</span></span></td>
        <td><span data-ttu-id="cb8d0-240">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-240">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-241">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-241">INUSE</span></span></td>
    </tr>
</table>

<span data-ttu-id="cb8d0-242">當兩個通訊端系結至相同的埠號碼時，但在不同的明確介面上，就不會發生衝突。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-242">When two sockets are bound to the same port number but on different explicit interfaces, there is no conflict.</span></span> <span data-ttu-id="cb8d0-243">例如，在電腦有兩個 IP 介面10.0.0.1 和10.99.99.99 的情況下，如果第一次呼叫系結的位置是10.0.0.1，且埠設定為5150，**而 \_ EXCLUSIVEADDRUSE** 指定了，則第二次 **呼叫在10.99.99.99 上系**[**結時，**](/windows/win32/api/winsock/nf-winsock-bind)埠也會設定為5150，而未指定任何選項則會成功。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-243">For example, in the case where a computer has two IP interfaces, 10.0.0.1 and 10.99.99.99, if the first call to [**bind**](/windows/win32/api/winsock/nf-winsock-bind) is on 10.0.0.1 with the port set to 5150 and **SO\_EXCLUSIVEADDRUSE** specified, then a second call to **bind** on 10.99.99.99 with the port also set to 5150 and no options specified will succeed.</span></span> <span data-ttu-id="cb8d0-244">但是，如果第一個通訊端系結至萬用字元位址和埠5150，則任何後續對埠5150的系結呼叫（ **\_ EXCLUSIVEADDRUSE** 設定）都會失敗，並傳回系結作業 **所傳回的** [WSAEADDRINUSE](windows-sockets-error-codes-2.md)或 [WSAEACCES](windows-sockets-error-codes-2.md) 。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-244">However, if the first socket is bound to the wildcard address and port 5150, then any subsequent bind call to port 5150 with **SO\_EXCLUSIVEADDRUSE** set will fail with either [WSAEADDRINUSE](windows-sockets-error-codes-2.md) or [WSAEACCES](windows-sockets-error-codes-2.md) returned by the **bind** operation.</span></span>

<span data-ttu-id="cb8d0-245">在第一次呼叫系 [**結設定為**](/windows/win32/api/winsock/nf-winsock-bind) **\_ REUSEADDR** 或沒有通訊端選項的情況下，第二個系結呼叫將會「劫持」埠，而應用程式將無法判斷 **哪一個套** 接字收到傳送至「共用」埠的特定封包。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-245">In the case where the first call to [**bind**](/windows/win32/api/winsock/nf-winsock-bind) sets either **SO\_REUSEADDR** or no socket options at all, the second **bind** call will "hijack" the port and the application will be unable to determine which of the two sockets received specific packets sent to the "shared" port.</span></span>

<span data-ttu-id="cb8d0-246">除非在呼叫系結函式之前呼叫 **\_ EXCLUSIVEADDRUSE** 通訊端選項，否則呼叫 [**bind**](/windows/win32/api/winsock/nf-winsock-bind)函式的一般應用程式不會配置系結的通訊端來進行獨佔使用。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-246">A typical application that calls the [**bind**](/windows/win32/api/winsock/nf-winsock-bind) function does not allocate the bound socket for exclusive use, unless the **SO\_EXCLUSIVEADDRUSE** socket option is called on the socket before the call to the **bind** function.</span></span> <span data-ttu-id="cb8d0-247">如果用戶端應用程式在伺服器應用程式系結至相同的埠之前，系結至暫時埠或特定埠，則可能會產生問題。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-247">If a client application binds to an ephemeral port or a specific port before a server application binds to the same port, then problems can result.</span></span> <span data-ttu-id="cb8d0-248">在呼叫系結函式之前，伺服器應用程式可以使用通訊端上的 **SO \_ REUSEADDR** 通訊端選項， 強制系結至相同的埠，但系結至該埠之所有通訊端的行為則為不定。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-248">The server application can forcibly bind to the same port by using the **SO\_REUSEADDR** socket option on the socket before calling the **bind** function, but the behavior for all sockets bound to that port is then indeterminate.</span></span> <span data-ttu-id="cb8d0-249">如果伺服器應用程式嘗試使用 **\_ EXCLUSIVEADDRUSE** 通訊端選項來獨佔使用埠，要求將會失敗。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-249">If the server application tries to use the **SO\_EXCLUSIVEADDRUSE** socket option for exclusive use of the port, the request will fail.</span></span>

<span data-ttu-id="cb8d0-250">相反地，在通訊端關閉之後，就不一定要立即重複使用具有 **\_ EXCLUSIVEADDRUSE** 設定的通訊端。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-250">Conversely, a socket with the **SO\_EXCLUSIVEADDRUSE** set cannot necessarily be reused immediately after socket closure.</span></span> <span data-ttu-id="cb8d0-251">例如，如果具有 **\_ EXCLUSIVEADDRUSE** 設定的接聽通訊端接受連接，之後再關閉，另一個通訊端也 (另一個通訊端，也就是 **\_ EXCLUSIVEADDRUSE**) 無法系結至與第一個通訊端相同的埠，直到原始連接變成非使用中。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-251">For example, if a listening socket with **SO\_EXCLUSIVEADDRUSE** set accepts a connection and is then subsequently closed, another socket (also with **SO\_EXCLUSIVEADDRUSE**) cannot bind to the same port as the first socket until the original connection becomes inactive.</span></span>

<span data-ttu-id="cb8d0-252">這個問題可能會變得很複雜，因為基礎傳輸通訊協定可能不會終止連接，即使通訊端已關閉也一樣。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-252">This issue can become complicated because the underlying transport protocol may not terminate the connection even though the socket has been closed.</span></span> <span data-ttu-id="cb8d0-253">即使應用程式關閉通訊端之後，系統仍必須傳輸任何緩衝的資料、將無訊息的中斷連線訊息傳送給對等，並等候對等的適當無訊息中斷連線訊息。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-253">Even after the socket has been closed by the application, the system must transmit any buffered data, send a graceful disconnect message to the peer, and wait for a corresponding graceful disconnect message from the peer.</span></span> <span data-ttu-id="cb8d0-254">基礎傳輸通訊協定可能永遠不會釋放連接;例如，參與原始連接的對等可能會通告零大小的視窗，或是其他形式的「攻擊」設定。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-254">It is possible that the underlying transport protocol might never release the connection; for example, the peer participating in the original connection might advertise a zero-size window, or some other form of "attack" configuration.</span></span> <span data-ttu-id="cb8d0-255">在這種情況下，用戶端連線會保持作用中狀態，儘管要求關閉它，因為未確認的資料會保留在緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-255">In such a case, the client connection remains in an active state despite the request to close it, since unacknowledged data remains in the buffer.</span></span>

<span data-ttu-id="cb8d0-256">為了避免這種情況，網路應用程式應該透過使用 SD 傳送旗標集呼叫 [**shutdown**](/windows/win32/api/winsock/nf-winsock-shutdown) 來確保正常關機 \_ ，然後等候 [**接收**](/windows/win32/api/winsock/nf-winsock-recv) 迴圈，直到透過連接傳回零個位元組為止。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-256">To avoid this situation, network applications should ensure a graceful shutdown by calling [**shutdown**](/windows/win32/api/winsock/nf-winsock-shutdown) with the SD\_SEND flag set, and then wait in a [**recv**](/windows/win32/api/winsock/nf-winsock-recv) loop until zero bytes are returned over the connection.</span></span> <span data-ttu-id="cb8d0-257">這可確保對等端接收所有資料，並同樣確認其已接收到所有傳輸的資料，以及避免前述的埠重複使用問題。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-257">This guarantees that all data is received by the peer and likewise confirms with the peer that it has received all of the transmitted data, as well as avoiding the aforementioned port reuse issue.</span></span>

<span data-ttu-id="cb8d0-258">您可以 \_ 在通訊端上設定 wait socket 選項，以防止埠轉換為「作用中」的等候狀態; 不過，這不建議您這麼做，因為它可能會導致所需的效果，例如重設連接。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-258">The SO\_LINGER socket option may be set on a socket to prevent the port from transitioning to an "active" wait state; however, this is discouraged as it can lead to desired effects, such as reset connections.</span></span> <span data-ttu-id="cb8d0-259">例如，如果資料是由對等接收，但是仍維持未認可狀態，而且本機電腦關閉通訊端，並 \_ 在其上進行設定，則兩部電腦之間的連線會重設，且對等會捨棄未認可的資料。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-259">For example, if data is received by the peer but remains unacknowledged by it, and the local computer closes the socket with SO\_LINGER set on it, the connection between the two computers is reset and the unacknowledged data discarded by the peer.</span></span> <span data-ttu-id="cb8d0-260">挑選適當的延遲時間很難，因為較小的超時值通常會導致突然中止的連接，而較大的超時值會讓系統容易遭受拒絕服務攻擊 (藉由建立許多連線，以及可能會) 拖延/封鎖應用程式執行緒。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-260">Picking a suitable time to linger is difficult as a smaller timeout value often results in suddenly aborted connections, whereas larger timeout values leave the system vulnerable to denial-of-service attacks (by establishing many connections and potentially stalling/blocking application threads).</span></span> <span data-ttu-id="cb8d0-261">關閉具有非零延遲超時值的通訊端，也可能導致 [**導致 closesocket**](/windows/win32/api/winsock/nf-winsock-closesocket) 呼叫封鎖。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-261">Closing a socket that has a nonzero linger timeout value may also cause the [**closesocket**](/windows/win32/api/winsock/nf-winsock-closesocket) call to block.</span></span>

## <a name="enhanced-socket-security"></a><span data-ttu-id="cb8d0-262">增強通訊端安全性</span><span class="sxs-lookup"><span data-stu-id="cb8d0-262">Enhanced Socket Security</span></span>

<span data-ttu-id="cb8d0-263">增強通訊端安全性是隨著 Windows Server 2003 的發行而新增的。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-263">Enhanced socket security was added with the release of Windows Server 2003.</span></span> <span data-ttu-id="cb8d0-264">在舊版的 Microsoft server 作業系統版本中，預設的通訊端安全性可輕易地讓程式從不受信任的應用程式劫持埠。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-264">In previous Microsoft server operating system releases, the default socket security easily allowed processes to hijack ports from unsuspecting applications.</span></span> <span data-ttu-id="cb8d0-265">在 Windows Server 2003 中，通訊端預設不會處於可共用狀態。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-265">In Windows Server 2003, sockets are not in a sharable state by default.</span></span> <span data-ttu-id="cb8d0-266">因此，如果應用程式想要允許其他進程重複使用通訊端已系結的埠，則必須特別啟用它。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-266">Therefore, if an application wants to allow other processes to reuse a port on which a socket is already bound, it must specifically enable it.</span></span> <span data-ttu-id="cb8d0-267">如果是這種情況，則在埠上呼叫 [**bind**](/windows/win32/api/winsock/nf-winsock-bind) 的第一個通訊端必須在通訊端上設定 **\_ REUSEADDR** 。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-267">If that is the case, the first socket to call [**bind**](/windows/win32/api/winsock/nf-winsock-bind) on the port must have **SO\_REUSEADDR** set on the socket.</span></span> <span data-ttu-id="cb8d0-268">這種情況的唯一例外狀況是，當 **第二** 個系結呼叫是由進行原始 **呼叫進行系** 結的相同使用者帳戶執行時。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-268">The only exception to this case occurs when the second **bind** call is performed by the same user account that made the original call to **bind**.</span></span> <span data-ttu-id="cb8d0-269">這個例外狀況僅為了提供回溯相容性而存在。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-269">This exception exists solely to provide backward compatibility.</span></span>

<span data-ttu-id="cb8d0-270">下表說明當第二個通訊端嘗試系結至使用特定通訊端選項的第一個通訊端之前系結的位址時，在 Windows Server 2003 和更新版本作業系統中發生的行為。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-270">The table below describes the behavior that occurs in Windows Server 2003 and later operating systems when a second socket attempts to bind to an address previously bound to by a first socket using specific socket options.</span></span>

> [!NOTE]
> <span data-ttu-id="cb8d0-271">在下表中，"萬用字元" 代表指定通訊協定 (的萬用字元位址，例如 IPv4 的 "0.0.0.0" 和 IPv6) 的 "：："。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-271">In the table below, "wildcard" denotes the wildcard address for the given protocol (such as "0.0.0.0" for IPv4 and "::" for IPv6).</span></span> <span data-ttu-id="cb8d0-272">「特定」代表指派了介面的特定 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-272">"Specific" denotes a specific IP address assigned an interface.</span></span> <span data-ttu-id="cb8d0-273">資料表資料格指出系結是否成功 ( 「成功」 ) 或針對 [WSAEADDRINUSE](windows-sockets-error-codes-2.md) 錯誤傳回 ( "INUSE" 的錯誤; [WSAEACCES](windows-sockets-error-codes-2.md) 錯誤) 的「存取」。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-273">The table cells indicate whether or not the bind is successful ("Success") or the error returned ("INUSE" for the [WSAEADDRINUSE](windows-sockets-error-codes-2.md) error; "ACCESS" for the [WSAEACCES](windows-sockets-error-codes-2.md) error).</span></span>
>
> <span data-ttu-id="cb8d0-274">另請注意，在這個特定的資料表中，這兩個系結 [**呼叫都是**](/windows/win32/api/winsock/nf-winsock-bind) 在同一個使用者帳戶下進行。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-274">Also note that in this specific table, both [**bind**](/windows/win32/api/winsock/nf-winsock-bind) calls are made under the same user account.</span></span>

<table>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2" rowspan="3"><span data-ttu-id="cb8d0-275">第 <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>一個</strong></a> 系結呼叫</span><span class="sxs-lookup"><span data-stu-id="cb8d0-275">First <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>bind</strong></a> call</span></span></td>
        <td bgcolor="#C0C0C0" colspan="6"><span data-ttu-id="cb8d0-276">第 <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>二</strong></a> 個系結呼叫</span><span class="sxs-lookup"><span data-stu-id="cb8d0-276">Second <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>bind</strong></a> call</span></span></td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2"><span data-ttu-id="cb8d0-277">預設</span><span class="sxs-lookup"><span data-stu-id="cb8d0-277">Default</span></span></td>
        <td bgcolor="#C0C0C0" colspan="2"><span data-ttu-id="cb8d0-278">SO_REUSEADDR</span><span class="sxs-lookup"><span data-stu-id="cb8d0-278">SO_REUSEADDR</span></span></td>
        <td bgcolor="#C0C0C0" colspan="2"><span data-ttu-id="cb8d0-279">SO_EXCLUSIVEADDRUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-279">SO_EXCLUSIVEADDRUSE</span></span></td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0"><span data-ttu-id="cb8d0-280">萬用字元</span><span class="sxs-lookup"><span data-stu-id="cb8d0-280">Wildcard</span></span></td>
        <td bgcolor="#C0C0C0"><span data-ttu-id="cb8d0-281">特定</span><span class="sxs-lookup"><span data-stu-id="cb8d0-281">Specific</span></span></td>
        <td bgcolor="#C0C0C0"><span data-ttu-id="cb8d0-282">萬用字元</span><span class="sxs-lookup"><span data-stu-id="cb8d0-282">Wildcard</span></span></td>
        <td bgcolor="#C0C0C0"><span data-ttu-id="cb8d0-283">特定</span><span class="sxs-lookup"><span data-stu-id="cb8d0-283">Specific</span></span></td>
        <td bgcolor="#C0C0C0"><span data-ttu-id="cb8d0-284">萬用字元</span><span class="sxs-lookup"><span data-stu-id="cb8d0-284">Wildcard</span></span></td>
        <td bgcolor="#C0C0C0"><span data-ttu-id="cb8d0-285">特定</span><span class="sxs-lookup"><span data-stu-id="cb8d0-285">Specific</span></span></td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2"><span data-ttu-id="cb8d0-286">預設</span><span class="sxs-lookup"><span data-stu-id="cb8d0-286">Default</span></span></td>
        <td bgcolor="#C0C0C0"><span data-ttu-id="cb8d0-287">萬用字元</span><span class="sxs-lookup"><span data-stu-id="cb8d0-287">Wildcard</span></span></td>
        <td><span data-ttu-id="cb8d0-288">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-288">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-289">Success</span><span class="sxs-lookup"><span data-stu-id="cb8d0-289">Success</span></span></td>
        <td><span data-ttu-id="cb8d0-290">ACCESS</span><span class="sxs-lookup"><span data-stu-id="cb8d0-290">ACCESS</span></span></td>
        <td><span data-ttu-id="cb8d0-291">Success</span><span class="sxs-lookup"><span data-stu-id="cb8d0-291">Success</span></span></td>
        <td><span data-ttu-id="cb8d0-292">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-292">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-293">Success</span><span class="sxs-lookup"><span data-stu-id="cb8d0-293">Success</span></span></td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0"><span data-ttu-id="cb8d0-294">特定</span><span class="sxs-lookup"><span data-stu-id="cb8d0-294">Specific</span></span></td>
        <td><span data-ttu-id="cb8d0-295">Success</span><span class="sxs-lookup"><span data-stu-id="cb8d0-295">Success</span></span></td>
        <td><span data-ttu-id="cb8d0-296">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-296">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-297">Success</span><span class="sxs-lookup"><span data-stu-id="cb8d0-297">Success</span></span></td>
        <td><span data-ttu-id="cb8d0-298">ACCESS</span><span class="sxs-lookup"><span data-stu-id="cb8d0-298">ACCESS</span></span></td>
        <td><span data-ttu-id="cb8d0-299">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-299">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-300">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-300">INUSE</span></span></td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2"><span data-ttu-id="cb8d0-301">SO_REUSEADDR</span><span class="sxs-lookup"><span data-stu-id="cb8d0-301">SO_REUSEADDR</span></span></td>
        <td bgcolor="#C0C0C0"><span data-ttu-id="cb8d0-302">萬用字元</span><span class="sxs-lookup"><span data-stu-id="cb8d0-302">Wildcard</span></span></td>
        <td><span data-ttu-id="cb8d0-303">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-303">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-304">成功</span><span class="sxs-lookup"><span data-stu-id="cb8d0-304">Success</span></span></td>
        <td><span data-ttu-id="cb8d0-305">成功</span><span class="sxs-lookup"><span data-stu-id="cb8d0-305">Success</span></span></td>
        <td><span data-ttu-id="cb8d0-306">成功</span><span class="sxs-lookup"><span data-stu-id="cb8d0-306">Success</span></span></td>
        <td><span data-ttu-id="cb8d0-307">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-307">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-308">Success</span><span class="sxs-lookup"><span data-stu-id="cb8d0-308">Success</span></span></td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0"><span data-ttu-id="cb8d0-309">特定</span><span class="sxs-lookup"><span data-stu-id="cb8d0-309">Specific</span></span></td>
        <td><span data-ttu-id="cb8d0-310">Success</span><span class="sxs-lookup"><span data-stu-id="cb8d0-310">Success</span></span></td>
        <td><span data-ttu-id="cb8d0-311">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-311">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-312">成功</span><span class="sxs-lookup"><span data-stu-id="cb8d0-312">Success</span></span></td>
        <td><span data-ttu-id="cb8d0-313">成功</span><span class="sxs-lookup"><span data-stu-id="cb8d0-313">Success</span></span></td>
        <td><span data-ttu-id="cb8d0-314">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-314">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-315">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-315">INUSE</span></span></td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2"><span data-ttu-id="cb8d0-316">SO_EXCLUSIVEADDRUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-316">SO_EXCLUSIVEADDRUSE</span></span></td>
        <td bgcolor="#C0C0C0"><span data-ttu-id="cb8d0-317">萬用字元</span><span class="sxs-lookup"><span data-stu-id="cb8d0-317">Wildcard</span></span></td>
        <td><span data-ttu-id="cb8d0-318">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-318">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-319">ACCESS</span><span class="sxs-lookup"><span data-stu-id="cb8d0-319">ACCESS</span></span></td>
        <td><span data-ttu-id="cb8d0-320">ACCESS</span><span class="sxs-lookup"><span data-stu-id="cb8d0-320">ACCESS</span></span></td>
        <td><span data-ttu-id="cb8d0-321">ACCESS</span><span class="sxs-lookup"><span data-stu-id="cb8d0-321">ACCESS</span></span></td>
        <td><span data-ttu-id="cb8d0-322">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-322">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-323">ACCESS</span><span class="sxs-lookup"><span data-stu-id="cb8d0-323">ACCESS</span></span></td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0"><span data-ttu-id="cb8d0-324">特定</span><span class="sxs-lookup"><span data-stu-id="cb8d0-324">Specific</span></span></td>
        <td><span data-ttu-id="cb8d0-325">Success</span><span class="sxs-lookup"><span data-stu-id="cb8d0-325">Success</span></span></td>
        <td><span data-ttu-id="cb8d0-326">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-326">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-327">Success</span><span class="sxs-lookup"><span data-stu-id="cb8d0-327">Success</span></span></td>
        <td><span data-ttu-id="cb8d0-328">ACCESS</span><span class="sxs-lookup"><span data-stu-id="cb8d0-328">ACCESS</span></span></td>
        <td><span data-ttu-id="cb8d0-329">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-329">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-330">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-330">INUSE</span></span></td>
    </tr>
</table>

<span data-ttu-id="cb8d0-331">上表中的幾個專案有提供說明。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-331">A few entries in the table above merit explanation.</span></span>

<span data-ttu-id="cb8d0-332">例如，如果第一個呼叫端將設定為在特定位址 **\_ EXCLUSIVEADDRUSE** ，而第二個呼叫端 [**嘗試使用相同埠上的萬用字元**](/windows/win32/api/winsock/nf-winsock-bind) 位址來呼叫系結，則第二個系 **結呼叫將** 會成功。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-332">For example, if the first caller sets **SO\_EXCLUSIVEADDRUSE** on a specific address, and second caller attempts to call [**bind**](/windows/win32/api/winsock/nf-winsock-bind) with a wildcard address on the same port, the second **bind** call will succeed.</span></span> <span data-ttu-id="cb8d0-333">在此特定案例中，第二個呼叫端會系結至所有介面，但第一個呼叫端所系結的特定位址除外。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-333">In this particular case, the second caller is bound to all interfaces except the specific address to which the first caller is bound.</span></span> <span data-ttu-id="cb8d0-334">請注意，此案例的反轉不成立：如果第一個呼叫端設定 **\_ EXCLUSIVEADDRUSE** ，並以萬用字元旗標呼叫系結，則第二個呼叫端就 **無法使用相同\*\*\*\*的埠呼叫系** 結。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-334">Note that the reverse of this case is not true: if the first caller sets **SO\_EXCLUSIVEADDRUSE** and calls **bind** with the wildcard flag, the second caller is not able to call **bind** with the same port.</span></span>

<span data-ttu-id="cb8d0-335">當通訊端系結呼叫是在不同的使用者帳戶下進行時，就會變更通訊端系結行為。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-335">The socket binding behavior changes when the socket bind calls are made under different user accounts.</span></span> <span data-ttu-id="cb8d0-336">下表指定當第二個通訊端使用特定通訊端選項和不同的使用者帳戶，嘗試系結先前由第一個通訊端所系結的位址時，在 Windows Server 2003 和更新版本的作業系統中發生的行為。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-336">The table below specifies the behavior that occurs in Windows Server 2003 and later operating systems when a second socket attempts to bind to an address previously bound to by a first socket using specific socket options and a different user account.</span></span>

<table>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2" rowspan="3"><span data-ttu-id="cb8d0-337">第 <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>一個</strong></a> 系結呼叫</span><span class="sxs-lookup"><span data-stu-id="cb8d0-337">First <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>bind</strong></a> call</span></span></td>
        <td bgcolor="#C0C0C0" colspan="6"><span data-ttu-id="cb8d0-338">第 <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>二</strong></a> 個系結呼叫</span><span class="sxs-lookup"><span data-stu-id="cb8d0-338">Second <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>bind</strong></a> call</span></span></td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2"><span data-ttu-id="cb8d0-339">預設</span><span class="sxs-lookup"><span data-stu-id="cb8d0-339">Default</span></span></td>
        <td bgcolor="#C0C0C0" colspan="2"><span data-ttu-id="cb8d0-340">SO_REUSEADDR</span><span class="sxs-lookup"><span data-stu-id="cb8d0-340">SO_REUSEADDR</span></span></td>
        <td bgcolor="#C0C0C0" colspan="2"><span data-ttu-id="cb8d0-341">SO_EXCLUSIVEADDRUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-341">SO_EXCLUSIVEADDRUSE</span></span></td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0"><span data-ttu-id="cb8d0-342">萬用字元</span><span class="sxs-lookup"><span data-stu-id="cb8d0-342">Wildcard</span></span></td>
        <td bgcolor="#C0C0C0"><span data-ttu-id="cb8d0-343">特定</span><span class="sxs-lookup"><span data-stu-id="cb8d0-343">Specific</span></span></td>
        <td bgcolor="#C0C0C0"><span data-ttu-id="cb8d0-344">萬用字元</span><span class="sxs-lookup"><span data-stu-id="cb8d0-344">Wildcard</span></span></td>
        <td bgcolor="#C0C0C0"><span data-ttu-id="cb8d0-345">特定</span><span class="sxs-lookup"><span data-stu-id="cb8d0-345">Specific</span></span></td>
        <td bgcolor="#C0C0C0"><span data-ttu-id="cb8d0-346">萬用字元</span><span class="sxs-lookup"><span data-stu-id="cb8d0-346">Wildcard</span></span></td>
        <td bgcolor="#C0C0C0"><span data-ttu-id="cb8d0-347">特定</span><span class="sxs-lookup"><span data-stu-id="cb8d0-347">Specific</span></span></td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2"><span data-ttu-id="cb8d0-348">預設</span><span class="sxs-lookup"><span data-stu-id="cb8d0-348">Default</span></span></td>
        <td bgcolor="#C0C0C0"><span data-ttu-id="cb8d0-349">萬用字元</span><span class="sxs-lookup"><span data-stu-id="cb8d0-349">Wildcard</span></span></td>
        <td><span data-ttu-id="cb8d0-350">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-350">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-351">ACCESS</span><span class="sxs-lookup"><span data-stu-id="cb8d0-351">ACCESS</span></span></td>
        <td><span data-ttu-id="cb8d0-352">ACCESS</span><span class="sxs-lookup"><span data-stu-id="cb8d0-352">ACCESS</span></span></td>
        <td><span data-ttu-id="cb8d0-353">ACCESS</span><span class="sxs-lookup"><span data-stu-id="cb8d0-353">ACCESS</span></span></td>
        <td><span data-ttu-id="cb8d0-354">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-354">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-355">ACCESS</span><span class="sxs-lookup"><span data-stu-id="cb8d0-355">ACCESS</span></span></td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0"><span data-ttu-id="cb8d0-356">特定</span><span class="sxs-lookup"><span data-stu-id="cb8d0-356">Specific</span></span></td>
        <td><span data-ttu-id="cb8d0-357">Success</span><span class="sxs-lookup"><span data-stu-id="cb8d0-357">Success</span></span></td>
        <td><span data-ttu-id="cb8d0-358">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-358">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-359">Success</span><span class="sxs-lookup"><span data-stu-id="cb8d0-359">Success</span></span></td>
        <td><span data-ttu-id="cb8d0-360">ACCESS</span><span class="sxs-lookup"><span data-stu-id="cb8d0-360">ACCESS</span></span></td>
        <td><span data-ttu-id="cb8d0-361">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-361">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-362">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-362">INUSE</span></span></td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2"><span data-ttu-id="cb8d0-363">SO_REUSEADDR</span><span class="sxs-lookup"><span data-stu-id="cb8d0-363">SO_REUSEADDR</span></span></td>
        <td bgcolor="#C0C0C0"><span data-ttu-id="cb8d0-364">萬用字元</span><span class="sxs-lookup"><span data-stu-id="cb8d0-364">Wildcard</span></span></td>
        <td><span data-ttu-id="cb8d0-365">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-365">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-366">ACCESS</span><span class="sxs-lookup"><span data-stu-id="cb8d0-366">ACCESS</span></span></td>
        <td><span data-ttu-id="cb8d0-367">成功</span><span class="sxs-lookup"><span data-stu-id="cb8d0-367">Success</span></span></td>
        <td><span data-ttu-id="cb8d0-368">成功</span><span class="sxs-lookup"><span data-stu-id="cb8d0-368">Success</span></span></td>
        <td><span data-ttu-id="cb8d0-369">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-369">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-370">ACCESS</span><span class="sxs-lookup"><span data-stu-id="cb8d0-370">ACCESS</span></span></td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0"><span data-ttu-id="cb8d0-371">特定</span><span class="sxs-lookup"><span data-stu-id="cb8d0-371">Specific</span></span></td>
        <td><span data-ttu-id="cb8d0-372">Success</span><span class="sxs-lookup"><span data-stu-id="cb8d0-372">Success</span></span></td>
        <td><span data-ttu-id="cb8d0-373">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-373">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-374">成功</span><span class="sxs-lookup"><span data-stu-id="cb8d0-374">Success</span></span></td>
        <td><span data-ttu-id="cb8d0-375">成功</span><span class="sxs-lookup"><span data-stu-id="cb8d0-375">Success</span></span></td>
        <td><span data-ttu-id="cb8d0-376">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-376">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-377">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-377">INUSE</span></span></td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2"><span data-ttu-id="cb8d0-378">SO_EXCLUSIVEADDRUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-378">SO_EXCLUSIVEADDRUSE</span></span></td>
        <td bgcolor="#C0C0C0"><span data-ttu-id="cb8d0-379">萬用字元</span><span class="sxs-lookup"><span data-stu-id="cb8d0-379">Wildcard</span></span></td>
        <td><span data-ttu-id="cb8d0-380">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-380">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-381">ACCESS</span><span class="sxs-lookup"><span data-stu-id="cb8d0-381">ACCESS</span></span></td>
        <td><span data-ttu-id="cb8d0-382">ACCESS</span><span class="sxs-lookup"><span data-stu-id="cb8d0-382">ACCESS</span></span></td>
        <td><span data-ttu-id="cb8d0-383">ACCESS</span><span class="sxs-lookup"><span data-stu-id="cb8d0-383">ACCESS</span></span></td>
        <td><span data-ttu-id="cb8d0-384">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-384">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-385">ACCESS</span><span class="sxs-lookup"><span data-stu-id="cb8d0-385">ACCESS</span></span></td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0"><span data-ttu-id="cb8d0-386">特定</span><span class="sxs-lookup"><span data-stu-id="cb8d0-386">Specific</span></span></td>
        <td><span data-ttu-id="cb8d0-387">Success</span><span class="sxs-lookup"><span data-stu-id="cb8d0-387">Success</span></span></td>
        <td><span data-ttu-id="cb8d0-388">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-388">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-389">Success</span><span class="sxs-lookup"><span data-stu-id="cb8d0-389">Success</span></span></td>
        <td><span data-ttu-id="cb8d0-390">ACCESS</span><span class="sxs-lookup"><span data-stu-id="cb8d0-390">ACCESS</span></span></td>
        <td><span data-ttu-id="cb8d0-391">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-391">INUSE</span></span></td>
        <td><span data-ttu-id="cb8d0-392">INUSE</span><span class="sxs-lookup"><span data-stu-id="cb8d0-392">INUSE</span></span></td>
    </tr>
</table>

<span data-ttu-id="cb8d0-393">請注意，當系 [**結呼叫是在不同**](/windows/win32/api/winsock/nf-winsock-bind) 的使用者帳戶下進行時，預設行為會有所不同。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-393">Note that the default behavior is different when the [**bind**](/windows/win32/api/winsock/nf-winsock-bind) calls are made under different user accounts.</span></span> <span data-ttu-id="cb8d0-394">如果第一個呼叫端未在通訊端上設定任何選項，且系結至萬用字元位址，則第二個呼叫端無法設定 **\_ REUSEADDR** 選項，並成功系結至相同的埠。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-394">If the first caller does not set any options on the socket and binds to the wildcard address, then the second caller cannot set the **SO\_REUSEADDR** option and successfully bind to the same port.</span></span> <span data-ttu-id="cb8d0-395">未設定任何選項的預設行為也會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-395">The default behavior with no options set returns an error, as well.</span></span>

<span data-ttu-id="cb8d0-396">在 Windows Vista 和更新版本上，可以建立可在 IPv6 和 IPv4 上運作的雙重堆疊通訊端。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-396">On Windows Vista and later, a dual stack socket can be created which operates over both IPv6 and IPv4.</span></span> <span data-ttu-id="cb8d0-397">當雙重堆疊通訊端系結至萬用字元位址時，會將指定的埠保留在 IPv4 和 IPv6 網路堆疊上，以及與 **\_ REUSEADDR** 建立關聯的檢查和 **\_ EXCLUSIVEADDRUSE** (（如果設定) ）。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-397">When a dual stack socket is bound to the wildcard address, the given port is reserved on both the IPv4 and IPv6 networking stacks and the checks associated with **SO\_REUSEADDR** and **SO\_EXCLUSIVEADDRUSE** (if set) are made.</span></span> <span data-ttu-id="cb8d0-398">這兩個網路堆疊上的這些檢查都必須成功。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-398">These checks must succeed on both networking stacks.</span></span> <span data-ttu-id="cb8d0-399">例如，如果雙堆疊 TCP 通訊端設定為 **\_ EXCLUSIVEADDRUSE** ，然後嘗試系結至埠5000，則其他 TCP 通訊端之前都不能系結至埠 5000 (萬用字元或特定) 。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-399">For example, if a dual stack TCP socket sets **SO\_EXCLUSIVEADDRUSE** and then tries to bind to port 5000, then no other TCP socket can be previously bound to port 5000 (either wildcard or specific).</span></span> <span data-ttu-id="cb8d0-400">在此情況下，如果 IPv4 TCP 通訊端之前系結至埠5000上的回送位址，則雙堆疊通訊端的系 [**結呼叫會**](/windows/win32/api/winsock/nf-winsock-bind) 失敗並出現 [WSAEACCES](windows-sockets-error-codes-2.md)。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-400">In this case if an IPv4 TCP socket was previously bound to the loopback address on port 5000, the [**bind**](/windows/win32/api/winsock/nf-winsock-bind) call for the dual stack socket would fail with [WSAEACCES](windows-sockets-error-codes-2.md).</span></span>

## <a name="application-strategies"></a><span data-ttu-id="cb8d0-401">應用程式策略</span><span class="sxs-lookup"><span data-stu-id="cb8d0-401">Application Strategies</span></span>

<span data-ttu-id="cb8d0-402">開發在通訊端層運作的網路應用程式時，請務必考慮需要的通訊端安全性類型。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-402">When developing network application that operate at the socket layer, it is important to consider the type of socket security necessary.</span></span> <span data-ttu-id="cb8d0-403">用戶端應用程式—連接或傳送資料至服務的應用程式，很少需要任何額外的步驟，因為它們系結至隨機的本機 (暫時) 埠。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-403">Client applications — applications that connect or send data to a service — rarely require any additional steps since they bind to a random local (ephemeral) port.</span></span> <span data-ttu-id="cb8d0-404">如果用戶端需要特定的本機埠系結才能正常運作，則您必須考慮通訊端安全性。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-404">If the client does require a specific local port binding in order to function correctly, then you must consider socket security.</span></span>

<span data-ttu-id="cb8d0-405">**\_ REUSEADDR** 選項在一般應用程式中，除了將資料傳遞至在相同埠上系結至所有通訊端的多播通訊端之外，還很少使用。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-405">The **SO\_REUSEADDR** option has very few uses in normal applications aside from multicast sockets where data is delivered to all of the sockets bound on the same port.</span></span> <span data-ttu-id="cb8d0-406">否則，任何設定此通訊端選項的應用程式都應該重新設計，以移除相依性，因為它 eminently 易受限於「通訊端劫持」。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-406">Otherwise, any application that sets this socket option should be redesigned to remove the dependency since it is eminently vulnerable to "socket hijacking".</span></span> <span data-ttu-id="cb8d0-407">只要 **\_ REUSEADDR** 通訊端選項可以用來在伺服器應用程式中劫持埠，就必須將應用程式視為不安全。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-407">As long as **SO\_REUSEADDR** socket option can be used to potentially hijack a port in a server application, the application must be considered to be not secure.</span></span>

<span data-ttu-id="cb8d0-408">所有伺服器應用程式都必須針對強式通訊端安全性設定 **\_ EXCLUSIVEADDRUSE** 。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-408">All server applications must set **SO\_EXCLUSIVEADDRUSE** for a strong level of socket security.</span></span> <span data-ttu-id="cb8d0-409">它不僅會防止惡意軟體劫持埠，也會指出是否有另一個應用程式系結至要求的埠。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-409">Not only does it prevent malicious software from hijacking the port, but it also indicates whether or not another application is bound to the requested port.</span></span> <span data-ttu-id="cb8d0-410">例如，如果另一個進程目前系結至特定介面上的相同埠，則使用 **\_ EXCLUSIVEADDRUSE** 通訊端選項設定的 [**進程在萬用字元位址上系**](/windows/win32/api/winsock/nf-winsock-bind)結的呼叫將會失敗。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-410">For example, a call to [**bind**](/windows/win32/api/winsock/nf-winsock-bind) on the wildcard address by a process with the **SO\_EXCLUSIVEADDRUSE** socket option set will fail if another process is currently bound to the same port on a specific interface.</span></span>

<span data-ttu-id="cb8d0-411">最後，即使已在 Windows Server 2003 中改善通訊端安全性，應用程式應該一律設定 **\_ EXCLUSIVEADDRUSE** 通訊端選項，以確保它會系結至進程要求的所有特定介面。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-411">Lastly, even though socket security has been improved in Windows Server 2003, an application should always set the **SO\_EXCLUSIVEADDRUSE** socket option to ensure that it binds to all the specific interfaces the process has requested.</span></span> <span data-ttu-id="cb8d0-412">Windows Server 2003 中的通訊端安全性為繼承應用程式增加了更高的安全性層級，但應用程式開發人員仍然必須設計其產品，並牢記安全性的所有層面。</span><span class="sxs-lookup"><span data-stu-id="cb8d0-412">The socket security in Windows Server 2003 adds an increased level of security for legacy applications, but application developers must still design their products with all aspects of security in mind.</span></span>

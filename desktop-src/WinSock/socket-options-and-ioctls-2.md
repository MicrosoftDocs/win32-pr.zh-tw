---
description: 下表摘要說明一些適用于 Windows 通訊端2的通訊端選項。
ms.assetid: 6731d27c-fb7d-421a-badf-0cad6a4712ea
title: 通訊端選項和 IOCTLs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472d37bd8d2d97eead66d7c9d2319e57fc5dafde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979956"
---
# <a name="socket-options-and-ioctls"></a><span data-ttu-id="36e48-103">通訊端選項和 IOCTLs</span><span class="sxs-lookup"><span data-stu-id="36e48-103">Socket Options and IOCTLs</span></span>

<span data-ttu-id="36e48-104">下表摘要說明一些適用于 Windows 通訊端2的通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="36e48-104">Some of the socket options for Windows Sockets 2 are summarized in the following table.</span></span> <span data-ttu-id="36e48-105">[**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85))和/或 [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85))的第4節提供更詳細的資訊。</span><span class="sxs-lookup"><span data-stu-id="36e48-105">More detailed information is provided in section 4 under [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) and/or [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)).</span></span> <span data-ttu-id="36e48-106">您可以在 Protocol-Specific 附錄中找到其他新的通訊協定特定通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="36e48-106">There are other new protocol-specific socket options which can be found in the Protocol-Specific Annex.</span></span> <span data-ttu-id="36e48-107">Winsock 參考中提供適用于 Windows 通訊端的 [**通訊端選項**](socket-options.md) 完整清單。</span><span class="sxs-lookup"><span data-stu-id="36e48-107">A complete list of [**Socket Options**](socket-options.md) for Windows Sockets are available in the Winsock reference.</span></span>

<span data-ttu-id="36e48-108">如需部分 Winsock Ioctls 的摘要，請參閱 [通訊端 Ioctl opcode 的摘要](summary-of-socket-ioctl-opcodes-2.md)。</span><span class="sxs-lookup"><span data-stu-id="36e48-108">For a a summary of some of the Winsock Ioctls, see [Summary of Socket Ioctl Opcodes](summary-of-socket-ioctl-opcodes-2.md).</span></span> <span data-ttu-id="36e48-109">Winsock 參考中提供完整的 [**Winsock IOCTLs**](winsock-ioctls.md) 清單。</span><span class="sxs-lookup"><span data-stu-id="36e48-109">A complete list of [**Winsock IOCTLs**](winsock-ioctls.md) are available in the Winsock reference.</span></span>

## <a name="summary-of-common-socket-options"></a><span data-ttu-id="36e48-110">一般通訊端選項的摘要</span><span class="sxs-lookup"><span data-stu-id="36e48-110">Summary of Common Socket Options</span></span>

<span data-ttu-id="36e48-111">Winsock 服務提供者必須辨識所有這些選項，而 [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) 的 () 會傳回每個選項的合理值。</span><span class="sxs-lookup"><span data-stu-id="36e48-111">A Winsock service provider must recognize all of these options, and (for [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85))) return plausible values for each.</span></span> <span data-ttu-id="36e48-112">下表顯示每個選項的預設值。</span><span class="sxs-lookup"><span data-stu-id="36e48-112">The default value for each option is shown in the following table.</span></span>

<span data-ttu-id="36e48-113">值</span><span class="sxs-lookup"><span data-stu-id="36e48-113">Value</span></span>

<span data-ttu-id="36e48-114">類型</span><span class="sxs-lookup"><span data-stu-id="36e48-114">Type</span></span>

<span data-ttu-id="36e48-115">意義</span><span class="sxs-lookup"><span data-stu-id="36e48-115">Meaning</span></span>

<span data-ttu-id="36e48-116">預設</span><span class="sxs-lookup"><span data-stu-id="36e48-116">Default</span></span>

<span data-ttu-id="36e48-117">注意</span><span class="sxs-lookup"><span data-stu-id="36e48-117">Note</span></span>

<span data-ttu-id="36e48-118"><span id="SO_ACCEPTCONN"></span><span id="so_acceptconn"></span>\_ACCEPTCONN</span><span class="sxs-lookup"><span data-stu-id="36e48-118"><span id="SO_ACCEPTCONN"></span><span id="so_acceptconn"></span>SO\_ACCEPTCONN</span></span>

<span data-ttu-id="36e48-119">BOOL</span><span class="sxs-lookup"><span data-stu-id="36e48-119">BOOL</span></span>

<span data-ttu-id="36e48-120">通訊端正在接聽。</span><span class="sxs-lookup"><span data-stu-id="36e48-120">Socket is listening.</span></span>

<span data-ttu-id="36e48-121">如果已執行 [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) ，則為 FALSE。</span><span class="sxs-lookup"><span data-stu-id="36e48-121">FALSE unless a [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) has been performed.</span></span>

<span data-ttu-id="36e48-122"><span id="SO_BROADCAST"></span><span id="so_broadcast"></span>\_廣播</span><span class="sxs-lookup"><span data-stu-id="36e48-122"><span id="SO_BROADCAST"></span><span id="so_broadcast"></span>SO\_BROADCAST</span></span>

<span data-ttu-id="36e48-123">BOOL</span><span class="sxs-lookup"><span data-stu-id="36e48-123">BOOL</span></span>

<span data-ttu-id="36e48-124">通訊端已設定為傳輸和接收廣播訊息。</span><span class="sxs-lookup"><span data-stu-id="36e48-124">Socket is configured for the transmission and receipt of broadcast messages.</span></span>

<span data-ttu-id="36e48-125">FALSE</span><span class="sxs-lookup"><span data-stu-id="36e48-125">FALSE</span></span>

<span data-ttu-id="36e48-126"><span id="SO_DEBUG"></span><span id="so_debug"></span>\_DEBUG</span><span class="sxs-lookup"><span data-stu-id="36e48-126"><span id="SO_DEBUG"></span><span id="so_debug"></span>SO\_DEBUG</span></span>

<span data-ttu-id="36e48-127">BOOL</span><span class="sxs-lookup"><span data-stu-id="36e48-127">BOOL</span></span>

<span data-ttu-id="36e48-128">已啟用偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="36e48-128">Debugging is enabled.</span></span>

<span data-ttu-id="36e48-129">FALSE</span><span class="sxs-lookup"><span data-stu-id="36e48-129">FALSE</span></span>

<span data-ttu-id="36e48-130"> (我) </span><span class="sxs-lookup"><span data-stu-id="36e48-130">(i)</span></span>

<span data-ttu-id="36e48-131"><span id="SO_DONTLINGER"></span><span id="so_dontlinger"></span>\_DONTLINGER</span><span class="sxs-lookup"><span data-stu-id="36e48-131"><span id="SO_DONTLINGER"></span><span id="so_dontlinger"></span>SO\_DONTLINGER</span></span>

<span data-ttu-id="36e48-132">BOOL</span><span class="sxs-lookup"><span data-stu-id="36e48-132">BOOL</span></span>

<span data-ttu-id="36e48-133">若為 true，則 \_ 會停用 [關閉] 選項。</span><span class="sxs-lookup"><span data-stu-id="36e48-133">If true, the SO\_LINGER option is disabled.</span></span>

<span data-ttu-id="36e48-134">true</span><span class="sxs-lookup"><span data-stu-id="36e48-134">TRUE</span></span>

<span data-ttu-id="36e48-135"><span id="SO_DONTROUTE"></span><span id="so_dontroute"></span>\_DONTROUTE</span><span class="sxs-lookup"><span data-stu-id="36e48-135"><span id="SO_DONTROUTE"></span><span id="so_dontroute"></span>SO\_DONTROUTE</span></span>

<span data-ttu-id="36e48-136">BOOL</span><span class="sxs-lookup"><span data-stu-id="36e48-136">BOOL</span></span>

<span data-ttu-id="36e48-137">路由已停用。</span><span class="sxs-lookup"><span data-stu-id="36e48-137">Routing is disabled.</span></span> <span data-ttu-id="36e48-138">成功，但在 AF INET 通訊端上會忽略， \_ 在 \_ 具有 [WSAENOPROTOOPT](windows-sockets-error-codes-2.md)的 af INET6 通訊端上失敗。</span><span class="sxs-lookup"><span data-stu-id="36e48-138">Succeeds but is ignored on AF\_INET sockets; fails on AF\_INET6 sockets with [WSAENOPROTOOPT](windows-sockets-error-codes-2.md).</span></span> <span data-ttu-id="36e48-139">在 ATM 通訊端上不受支援 (會導致錯誤) 。</span><span class="sxs-lookup"><span data-stu-id="36e48-139">Not supported on ATM sockets (results in an error).</span></span>

<span data-ttu-id="36e48-140">FALSE</span><span class="sxs-lookup"><span data-stu-id="36e48-140">FALSE</span></span>

<span data-ttu-id="36e48-141"> (我) </span><span class="sxs-lookup"><span data-stu-id="36e48-141">(i)</span></span>

<span data-ttu-id="36e48-142"><span id="SO_ERROR"></span><span id="so_error"></span>\_錯誤</span><span class="sxs-lookup"><span data-stu-id="36e48-142"><span id="SO_ERROR"></span><span id="so_error"></span>SO\_ERROR</span></span>

<span data-ttu-id="36e48-143">int</span><span class="sxs-lookup"><span data-stu-id="36e48-143">int</span></span>

<span data-ttu-id="36e48-144">捕獲錯誤狀態並清除。</span><span class="sxs-lookup"><span data-stu-id="36e48-144">Retrieves error status and clear.</span></span>

<span data-ttu-id="36e48-145">0</span><span class="sxs-lookup"><span data-stu-id="36e48-145">0</span></span>

<span data-ttu-id="36e48-146"><span id="SO_GROUP_ID"></span><span id="so_group_id"></span>\_群組 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="36e48-146"><span id="SO_GROUP_ID"></span><span id="so_group_id"></span>SO\_GROUP\_ID</span></span>

<span data-ttu-id="36e48-147">GROUP</span><span class="sxs-lookup"><span data-stu-id="36e48-147">GROUP</span></span>

<span data-ttu-id="36e48-148">保留的。</span><span class="sxs-lookup"><span data-stu-id="36e48-148">Reserved.</span></span>

<span data-ttu-id="36e48-149">NULL</span><span class="sxs-lookup"><span data-stu-id="36e48-149">NULL</span></span>

<span data-ttu-id="36e48-150">僅取得</span><span class="sxs-lookup"><span data-stu-id="36e48-150">Get only</span></span>

<span data-ttu-id="36e48-151"><span id="SO_GROUP_PRIORITY"></span><span id="so_group_priority"></span>\_群組 \_ 優先順序</span><span class="sxs-lookup"><span data-stu-id="36e48-151"><span id="SO_GROUP_PRIORITY"></span><span id="so_group_priority"></span>SO\_GROUP\_PRIORITY</span></span>

<span data-ttu-id="36e48-152">int</span><span class="sxs-lookup"><span data-stu-id="36e48-152">int</span></span>

<span data-ttu-id="36e48-153">保留的。</span><span class="sxs-lookup"><span data-stu-id="36e48-153">Reserved.</span></span>

<span data-ttu-id="36e48-154">0</span><span class="sxs-lookup"><span data-stu-id="36e48-154">0</span></span>

[<span data-ttu-id="36e48-155">**所以 \_ KEEPALIVE**</span><span class="sxs-lookup"><span data-stu-id="36e48-155">**SO\_KEEPALIVE**</span></span>](so-keepalive.md)

<span data-ttu-id="36e48-156">BOOL</span><span class="sxs-lookup"><span data-stu-id="36e48-156">BOOL</span></span>

<span data-ttu-id="36e48-157">正在傳送 keepalive。</span><span class="sxs-lookup"><span data-stu-id="36e48-157">Keepalives are being sent.</span></span> <span data-ttu-id="36e48-158">在 ATM 通訊端上不受支援 (會導致錯誤) 。</span><span class="sxs-lookup"><span data-stu-id="36e48-158">Not supported on ATM sockets (results in an error).</span></span>

<span data-ttu-id="36e48-159">FALSE</span><span class="sxs-lookup"><span data-stu-id="36e48-159">FALSE</span></span>

<span data-ttu-id="36e48-160"> (我) </span><span class="sxs-lookup"><span data-stu-id="36e48-160">(i)</span></span>

<span data-ttu-id="36e48-161"><span id="SO_LINGER"></span><span id="so_linger"></span>\_延遲</span><span class="sxs-lookup"><span data-stu-id="36e48-161"><span id="SO_LINGER"></span><span id="so_linger"></span>SO\_LINGER</span></span>

<span data-ttu-id="36e48-162">結構延遲</span><span class="sxs-lookup"><span data-stu-id="36e48-162">Structure linger</span></span>

<span data-ttu-id="36e48-163">傳回目前的延遲選項。</span><span class="sxs-lookup"><span data-stu-id="36e48-163">Returns the current linger options.</span></span>

<span data-ttu-id="36e48-164">l \_ onoff 是0</span><span class="sxs-lookup"><span data-stu-id="36e48-164">l\_onoff is 0</span></span>

<span data-ttu-id="36e48-165"><span id="SO_MAX_MSG_SIZE"></span><span id="so_max_msg_size"></span>\_最大 \_ 訊息 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="36e48-165"><span id="SO_MAX_MSG_SIZE"></span><span id="so_max_msg_size"></span>SO\_MAX\_MSG\_SIZE</span></span>

<span data-ttu-id="36e48-166">int</span><span class="sxs-lookup"><span data-stu-id="36e48-166">int</span></span>

<span data-ttu-id="36e48-167">訊息通訊端類型訊息的最大輸出大小。</span><span class="sxs-lookup"><span data-stu-id="36e48-167">Maximum outbound size of a message for message socket types.</span></span> <span data-ttu-id="36e48-168">沒有可決定輸入訊息大小上限的布建。</span><span class="sxs-lookup"><span data-stu-id="36e48-168">There is no provision to determine the maximum inbound message size.</span></span> <span data-ttu-id="36e48-169">對資料流程導向通訊端沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="36e48-169">Has no meaning for stream-oriented sockets.</span></span>

<span data-ttu-id="36e48-170">執行相依</span><span class="sxs-lookup"><span data-stu-id="36e48-170">Implementation dependent</span></span>

<span data-ttu-id="36e48-171">僅取得</span><span class="sxs-lookup"><span data-stu-id="36e48-171">Get only</span></span>

<span data-ttu-id="36e48-172"><span id="SO_OOBINLINE"></span><span id="so_oobinline"></span>\_OOBINLINE</span><span class="sxs-lookup"><span data-stu-id="36e48-172"><span id="SO_OOBINLINE"></span><span id="so_oobinline"></span>SO\_OOBINLINE</span></span>

<span data-ttu-id="36e48-173">BOOL</span><span class="sxs-lookup"><span data-stu-id="36e48-173">BOOL</span></span>

<span data-ttu-id="36e48-174">正在正常資料流程中接收 OOB 資料。</span><span class="sxs-lookup"><span data-stu-id="36e48-174">OOB data is being received in the normal data stream.</span></span>

<span data-ttu-id="36e48-175">FALSE</span><span class="sxs-lookup"><span data-stu-id="36e48-175">FALSE</span></span>

<span data-ttu-id="36e48-176"><span id="SO_PROTOCOL_INFOW"></span><span id="so_protocol_infow"></span>SO \_ PROTOCOL \_ INFOW</span><span class="sxs-lookup"><span data-stu-id="36e48-176"><span id="SO_PROTOCOL_INFOW"></span><span id="so_protocol_infow"></span>SO\_PROTOCOL\_INFOW</span></span>

<span data-ttu-id="36e48-177">結構 [ **WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)</span><span class="sxs-lookup"><span data-stu-id="36e48-177">structure [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)</span></span>

<span data-ttu-id="36e48-178">系結至此通訊端之通訊協定的通訊協定資訊描述。</span><span class="sxs-lookup"><span data-stu-id="36e48-178">Description of protocol information for the protocol that is bound to this socket.</span></span>

<span data-ttu-id="36e48-179">通訊協定相依</span><span class="sxs-lookup"><span data-stu-id="36e48-179">Protocol dependent</span></span>

<span data-ttu-id="36e48-180">僅取得</span><span class="sxs-lookup"><span data-stu-id="36e48-180">Get only</span></span>

<span data-ttu-id="36e48-181"><span id="SO_RCVBUF"></span><span id="so_rcvbuf"></span>\_RCVBUF</span><span class="sxs-lookup"><span data-stu-id="36e48-181"><span id="SO_RCVBUF"></span><span id="so_rcvbuf"></span>SO\_RCVBUF</span></span>

<span data-ttu-id="36e48-182">int</span><span class="sxs-lookup"><span data-stu-id="36e48-182">int</span></span>

<span data-ttu-id="36e48-183">保留給接收的每個通訊端緩衝區空間總數。</span><span class="sxs-lookup"><span data-stu-id="36e48-183">The total per-socket buffer space reserved for receives.</span></span> <span data-ttu-id="36e48-184">這與「 \_ 最大訊息 \_ 大小」無關 \_ ，而且不一定會對應到 TCP 接收視窗的大小。</span><span class="sxs-lookup"><span data-stu-id="36e48-184">This is unrelated to SO\_MAX\_MSG\_SIZE and does not necessarily correspond to the size of the TCP receive window.</span></span>

<span data-ttu-id="36e48-185">執行相依</span><span class="sxs-lookup"><span data-stu-id="36e48-185">Implementation dependent</span></span>

<span data-ttu-id="36e48-186"> (我) </span><span class="sxs-lookup"><span data-stu-id="36e48-186">(i)</span></span>

<span data-ttu-id="36e48-187"><span id="SO_REUSEADDR"></span><span id="so_reuseaddr"></span>\_REUSEADDR</span><span class="sxs-lookup"><span data-stu-id="36e48-187"><span id="SO_REUSEADDR"></span><span id="so_reuseaddr"></span>SO\_REUSEADDR</span></span>

<span data-ttu-id="36e48-188">BOOL</span><span class="sxs-lookup"><span data-stu-id="36e48-188">BOOL</span></span>

<span data-ttu-id="36e48-189">此通訊端所系結的位址可供其他人使用。</span><span class="sxs-lookup"><span data-stu-id="36e48-189">The address to which this socket is bound can be used by others.</span></span> <span data-ttu-id="36e48-190">不適用於 ATM 通訊端。</span><span class="sxs-lookup"><span data-stu-id="36e48-190">Not applicable on ATM sockets.</span></span>

<span data-ttu-id="36e48-191">FALSE</span><span class="sxs-lookup"><span data-stu-id="36e48-191">FALSE</span></span>

<span data-ttu-id="36e48-192"><span id="SO_SNDBUF"></span><span id="so_sndbuf"></span>\_SNDBUF</span><span class="sxs-lookup"><span data-stu-id="36e48-192"><span id="SO_SNDBUF"></span><span id="so_sndbuf"></span>SO\_SNDBUF</span></span>

<span data-ttu-id="36e48-193">int</span><span class="sxs-lookup"><span data-stu-id="36e48-193">int</span></span>

<span data-ttu-id="36e48-194">保留給傳送的每個通訊端緩衝區空間總數。</span><span class="sxs-lookup"><span data-stu-id="36e48-194">The total per-socket buffer space reserved for sends.</span></span> <span data-ttu-id="36e48-195">這與「 \_ 最大訊息 \_ 大小」無關 \_ ，而且不一定會對應至 TCP 傳送視窗的大小。</span><span class="sxs-lookup"><span data-stu-id="36e48-195">This is unrelated to SO\_MAX\_MSG\_SIZE and does not necessarily correspond to the size of a TCP send window.</span></span>

<span data-ttu-id="36e48-196">執行相依</span><span class="sxs-lookup"><span data-stu-id="36e48-196">Implementation dependent</span></span>

<span data-ttu-id="36e48-197"> (我) </span><span class="sxs-lookup"><span data-stu-id="36e48-197">(i)</span></span>

<span data-ttu-id="36e48-198"><span id="SO_TYPE"></span><span id="so_type"></span>\_請輸入</span><span class="sxs-lookup"><span data-stu-id="36e48-198"><span id="SO_TYPE"></span><span id="so_type"></span>SO\_TYPE</span></span>

<span data-ttu-id="36e48-199">int</span><span class="sxs-lookup"><span data-stu-id="36e48-199">int</span></span>

<span data-ttu-id="36e48-200">通訊端 (的類型，例如 SOCK \_ STREAM) 。</span><span class="sxs-lookup"><span data-stu-id="36e48-200">The type of the socket (for example, SOCK\_STREAM).</span></span>

<span data-ttu-id="36e48-201">透過通訊端建立。</span><span class="sxs-lookup"><span data-stu-id="36e48-201">As created through socket.</span></span>

<span data-ttu-id="36e48-202"><span id="PVD_CONFIG"></span><span id="pvd_config"></span>PVD \_ 設定</span><span class="sxs-lookup"><span data-stu-id="36e48-202"><span id="PVD_CONFIG"></span><span id="pvd_config"></span>PVD\_CONFIG</span></span>

<span data-ttu-id="36e48-203">字元遠 \*</span><span class="sxs-lookup"><span data-stu-id="36e48-203">char FAR \*</span></span>

<span data-ttu-id="36e48-204">不透明的資料結構物件，其中包含服務提供者的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="36e48-204">An opaque data structure object containing configuration information of the service provider.</span></span>

<span data-ttu-id="36e48-205">執行相依</span><span class="sxs-lookup"><span data-stu-id="36e48-205">Implementation dependent</span></span>

<span data-ttu-id="36e48-206"><span id="TCP_NODELAY"></span><span id="tcp_nodelay"></span>TCP \_ NODELAY</span><span class="sxs-lookup"><span data-stu-id="36e48-206"><span id="TCP_NODELAY"></span><span id="tcp_nodelay"></span>TCP\_NODELAY</span></span>

<span data-ttu-id="36e48-207">BOOL</span><span class="sxs-lookup"><span data-stu-id="36e48-207">BOOL</span></span>

<span data-ttu-id="36e48-208">停用用於傳送聯合的 Nagle 演算法。</span><span class="sxs-lookup"><span data-stu-id="36e48-208">Disables the Nagle algorithm for send coalescing.</span></span>

<span data-ttu-id="36e48-209">執行相依</span><span class="sxs-lookup"><span data-stu-id="36e48-209">Implementation dependent</span></span>

<span data-ttu-id="36e48-210"> (我) 服務提供者可能會在 [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) 上以無訊息方式忽略此選項，並傳回 [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85))的常數值，或可能接受 **WSPSetSockOpt** 的值，並傳回 **WSPGetSockOpt** 中的對應值，而不需以任何方式使用此值。</span><span class="sxs-lookup"><span data-stu-id="36e48-210">(i) A service provider may silently ignore this option on [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) and return a constant value for [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)), or it may accept a value for **WSPSetSockOpt** and return the corresponding value in **WSPGetSockOpt** without using the value in any way.</span></span>



 

## <a name="related-topics"></a><span data-ttu-id="36e48-211">相關主題</span><span class="sxs-lookup"><span data-stu-id="36e48-211">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36e48-212">**通訊端選項**</span><span class="sxs-lookup"><span data-stu-id="36e48-212">**Socket Options**</span></span>](socket-options.md)
</dt> <dt>

[<span data-ttu-id="36e48-213">**SOL \_ 通訊端通訊端選項**</span><span class="sxs-lookup"><span data-stu-id="36e48-213">**SOL\_SOCKET Socket Options**</span></span>](sol-socket-socket-options.md)
</dt> <dt>

[<span data-ttu-id="36e48-214">**IPPROTO \_ TCP 通訊端選項**</span><span class="sxs-lookup"><span data-stu-id="36e48-214">**IPPROTO\_TCP Socket Options**</span></span>](ipproto-tcp-socket-options.md)
</dt> <dt>

[<span data-ttu-id="36e48-215">**IPPROTO \_ UDP 通訊端選項**</span><span class="sxs-lookup"><span data-stu-id="36e48-215">**IPPROTO\_UDP Socket Options**</span></span>](ipproto-udp-socket-options.md)
</dt> <dt>

[<span data-ttu-id="36e48-216">**Winsock IOCTLs**</span><span class="sxs-lookup"><span data-stu-id="36e48-216">**Winsock IOCTLs**</span></span>](winsock-ioctls.md)
</dt> </dl>

 

 

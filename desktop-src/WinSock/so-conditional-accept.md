---
description: 的設計目的是讓應用程式決定是否要接受接聽通訊端上的連入連線。
ms.assetid: 964683eb-5dfc-4441-abb7-315be8b89a19
title: 'SO_CONDITIONAL_ACCEPT 通訊端選項 (Ws2def) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: badfdd1f8aac49ae05fa6b77dadb2561ba5ea02f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978071"
---
# <a name="so_conditional_accept-socket-option"></a><span data-ttu-id="b52c1-103">\_條件式 \_ 接受通訊端選項</span><span class="sxs-lookup"><span data-stu-id="b52c1-103">SO\_CONDITIONAL\_ACCEPT socket option</span></span>

<span data-ttu-id="b52c1-104">「 **\_ 條件式 \_ 接受** 」通訊端選項的設計目的，是要讓應用程式決定是否要接受接聽通訊端上的連入連線。</span><span class="sxs-lookup"><span data-stu-id="b52c1-104">The **SO\_CONDITIONAL\_ACCEPT** socket option is designed to allow an application to decide whether or not to accept an incoming connection on a listening socket.</span></span>

## <a name="socket-option-value"></a><span data-ttu-id="b52c1-105">通訊端選項值</span><span class="sxs-lookup"><span data-stu-id="b52c1-105">Socket option value</span></span>

<span data-ttu-id="b52c1-106">表示這個通訊端選項的常數是0x3002。</span><span class="sxs-lookup"><span data-stu-id="b52c1-106">The constant that represents this socket option is 0x3002.</span></span>

## <a name="syntax"></a><span data-ttu-id="b52c1-107">語法</span><span class="sxs-lookup"><span data-stu-id="b52c1-107">Syntax</span></span>


```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_CONDITIONAL_ACCEPT, // optname
  (char *) optval,         // input buffer,
  (int) optlen,       // size of input buffer
);
```



## <a name="parameters"></a><span data-ttu-id="b52c1-108">參數</span><span class="sxs-lookup"><span data-stu-id="b52c1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b52c1-109"> \[ 中的 s\]</span><span class="sxs-lookup"><span data-stu-id="b52c1-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b52c1-110">識別通訊端的描述元。</span><span class="sxs-lookup"><span data-stu-id="b52c1-110">A descriptor identifying the socket.</span></span>

</dd> <dt>

<span data-ttu-id="b52c1-111">*層級* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b52c1-111">*level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b52c1-112">定義選項的層級。</span><span class="sxs-lookup"><span data-stu-id="b52c1-112">The level at which the option is defined.</span></span> <span data-ttu-id="b52c1-113">使用 **SOL \_ 通訊端** 進行這種操作。</span><span class="sxs-lookup"><span data-stu-id="b52c1-113">Use **SOL\_SOCKET** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="b52c1-114">*optname* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b52c1-114">*optname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b52c1-115">要設定其值的通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="b52c1-115">The socket option for which the value is to be set.</span></span> <span data-ttu-id="b52c1-116">針對此作業，請使用 **\_ 條件式 \_ 接受** 。</span><span class="sxs-lookup"><span data-stu-id="b52c1-116">Use **SO\_CONDITIONAL\_ACCEPT** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="b52c1-117">*optval* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b52c1-117">*optval* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b52c1-118">緩衝區的指標，其中包含要設定之選項的值。</span><span class="sxs-lookup"><span data-stu-id="b52c1-118">A pointer to the buffer containing the value for the option to set.</span></span> <span data-ttu-id="b52c1-119">此參數應指向等於或大於 **DWORD** 值大小的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b52c1-119">This parameter should point to buffer equal to or larger than the size of a **DWORD** value.</span></span>

<span data-ttu-id="b52c1-120">此值會被視為布林值，0用來指出 **FALSE** (停用的) ，而非零值 **則表示 (啟用**) 。</span><span class="sxs-lookup"><span data-stu-id="b52c1-120">This value is treated as a boolean value with 0 used to indicate **FALSE** (disabled) and a nonzero value to indicate **TRUE** (enabled).</span></span>

</dd> <dt>

<span data-ttu-id="b52c1-121">*optlen* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="b52c1-121">*optlen* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b52c1-122">*Optval* 緩衝區大小的指標，以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="b52c1-122">A pointer to the size, in bytes, of the *optval* buffer.</span></span> <span data-ttu-id="b52c1-123">此大小必須等於或大於 **DWORD** 值的大小。</span><span class="sxs-lookup"><span data-stu-id="b52c1-123">This size must be equal to or larger than the size of a **DWORD** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b52c1-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="b52c1-124">Return value</span></span>

<span data-ttu-id="b52c1-125">如果作業順利完成， [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 會傳回零。</span><span class="sxs-lookup"><span data-stu-id="b52c1-125">If the operation completes successfully, [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) returns zero.</span></span>

<span data-ttu-id="b52c1-126">如果作業失敗， \_ 則會傳回 SOCKET 錯誤的值，並藉由呼叫 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)來取出特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b52c1-126">If the operation fails, a value of SOCKET\_ERROR is returned and a specific error code can be retrieved by calling [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>



| <span data-ttu-id="b52c1-127">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="b52c1-127">Error code</span></span>                                                                                                                                              | <span data-ttu-id="b52c1-128">意義</span><span class="sxs-lookup"><span data-stu-id="b52c1-128">Meaning</span></span>                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b52c1-129"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="b52c1-129"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span></span> </dl> | <span data-ttu-id="b52c1-130">在使用此函式之前，必須先進行成功的 [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) 呼叫。</span><span class="sxs-lookup"><span data-stu-id="b52c1-130">A successful [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) call must occur before using this function.</span></span><br/>                                                                                                                                                     |
| <dl> <span data-ttu-id="b52c1-131"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="b52c1-131"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="b52c1-132">網路子系統失敗。</span><span class="sxs-lookup"><span data-stu-id="b52c1-132">The network subsystem has failed.</span></span><br/>                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="b52c1-133"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="b52c1-133"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="b52c1-134">其中一個 *optval* 或 *optlen* 參數指向不在使用者位址空間有效部分的記憶體。</span><span class="sxs-lookup"><span data-stu-id="b52c1-134">One of the *optval* or the *optlen* parameters point to memory that is not in a valid part of the user address space.</span></span> <span data-ttu-id="b52c1-135">如果 *optlen* 參數所指向的值小於 **DWORD** 值的大小，也會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="b52c1-135">This error is also returned if the value pointed to by the *optlen* parameter is less than the size of a **DWORD** value.</span></span><br/> |
| <dl> <span data-ttu-id="b52c1-136"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="b52c1-136"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="b52c1-137">封鎖的 Windows 通訊端1.1 呼叫正在進行中，或服務提供者仍在處理回呼函數。</span><span class="sxs-lookup"><span data-stu-id="b52c1-137">A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="b52c1-138"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="b52c1-138"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="b52c1-139">*層級* 參數未知或無效。</span><span class="sxs-lookup"><span data-stu-id="b52c1-139">The *level* parameter is unknown or invalid.</span></span> <span data-ttu-id="b52c1-140">如果通訊端已處於接聽狀態，也會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="b52c1-140">This error is also returned if the socket was already in a listening state.</span></span><br/>                                                                                                                        |
| <dl> <span data-ttu-id="b52c1-141"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="b52c1-141"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="b52c1-142">指定的通訊協定系列未知或不支援此選項。</span><span class="sxs-lookup"><span data-stu-id="b52c1-142">The option is unknown or unsupported by the indicated protocol family.</span></span><br/>                                                                                                                                                                          |
| <dl> <span data-ttu-id="b52c1-143"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="b52c1-143"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="b52c1-144">描述項不是通訊端。</span><span class="sxs-lookup"><span data-stu-id="b52c1-144">The descriptor is not a socket.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="b52c1-145">備註</span><span class="sxs-lookup"><span data-stu-id="b52c1-145">Remarks</span></span>

<span data-ttu-id="b52c1-146">以 with **\_ 條件式 \_ 接受** 通訊端選項呼叫的 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)函式，可讓應用程式決定是否要接受接聽通訊端上的連入連線。</span><span class="sxs-lookup"><span data-stu-id="b52c1-146">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function called with the **SO\_CONDITIONAL\_ACCEPT** socket option allows an application to decide whether or not to accept an incoming connection on a listening socket.</span></span> <span data-ttu-id="b52c1-147">預設會停用通訊端的條件式接受選項 (設定為 **FALSE**) 。</span><span class="sxs-lookup"><span data-stu-id="b52c1-147">The conditional accept option for a socket is disabled (set to **FALSE**) by default.</span></span>

<span data-ttu-id="b52c1-148">啟用此通訊端選項時，TCP 堆疊不會自動接受連接。</span><span class="sxs-lookup"><span data-stu-id="b52c1-148">When this socket option is enabled, the TCP stack does not automatically accept connections.</span></span> <span data-ttu-id="b52c1-149">它會等待應用程式指出它會透過以 [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) 函式註冊的條件式接受回呼接受連接。</span><span class="sxs-lookup"><span data-stu-id="b52c1-149">It waits for the application to indicate that it accepts the connection via the conditional accept callback registered with [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) function.</span></span> <span data-ttu-id="b52c1-150">一旦收到連接要求，Winsock 會叫用應用程式所註冊的條件式接受回呼。</span><span class="sxs-lookup"><span data-stu-id="b52c1-150">Once a connection request is received, Winsock invokes the conditional accept callback registered by the application.</span></span> <span data-ttu-id="b52c1-151">只有當條件式接受回呼傳回 **CF \_ accept** 時，Winsock 才會通知傳輸，以完全接受連接。</span><span class="sxs-lookup"><span data-stu-id="b52c1-151">Only when the conditional accept callback returns **CF\_ACCEPT** will Winsock notify the transport to fully accept the connection.</span></span>

<span data-ttu-id="b52c1-152">當 [ **\_ 條件式 \_ 接受** 通訊端] 選項設為 [已啟用] 時 (設定為 [ **TRUE** ]) 時，會對通訊端產生數個副作用：</span><span class="sxs-lookup"><span data-stu-id="b52c1-152">When the **SO\_CONDITIONAL\_ACCEPT** socket option is set to enabled (set to **TRUE**), this has several side effects on the socket:</span></span>

-   <span data-ttu-id="b52c1-153">這會停用 TCP 堆疊的內建 SYN 攻擊保護防禦措施，因為應用程式現在會取得接受連線的擁有權。</span><span class="sxs-lookup"><span data-stu-id="b52c1-153">This disables the TCP stack's built-in SYN attack protection defenses, since the application is now taking ownership of accepting connections.</span></span>
-   <span data-ttu-id="b52c1-154">這會有效地停用接聽待處理專案，因為不會代表接聽通訊端接受連接。</span><span class="sxs-lookup"><span data-stu-id="b52c1-154">This effectively disables the listen backlog since connections aren't accepted on behalf of a listening socket.</span></span> <span data-ttu-id="b52c1-155">除非應用程式完全接受使用 **CF \_ 接受** 機制，否則永遠無法完全接受連接。</span><span class="sxs-lookup"><span data-stu-id="b52c1-155">A connection is never fully accepted until the application fully accepts using the **CF\_ACCEPT** mechanism.</span></span>
-   <span data-ttu-id="b52c1-156">這也表示應用程式必須一律處於狀態，才能立即處理接受回呼以接受連接。</span><span class="sxs-lookup"><span data-stu-id="b52c1-156">This also means the application take care to always be in a state to readily handle the accept callbacks to accept the connection.</span></span> <span data-ttu-id="b52c1-157">如果應用程式正在進行其他處理，用戶端可能會在應用程式實際接受連接之前停止運作。</span><span class="sxs-lookup"><span data-stu-id="b52c1-157">If the application is busy doing other processing, then the client side may time out before the application actually accepts the connection.</span></span> <span data-ttu-id="b52c1-158">這會導致用戶端體驗不佳。</span><span class="sxs-lookup"><span data-stu-id="b52c1-158">This leads to a poor client experience.</span></span>

<span data-ttu-id="b52c1-159">一般而言，應用程式使用條件式接受的主要原因是檢查連線用戶端所使用的來源 IP 位址或埠，然後決定要接受或拒絕連接。</span><span class="sxs-lookup"><span data-stu-id="b52c1-159">Generally, the main reason applications use conditional accept is to inspect the source IP address or port used by the connecting client and then decide to accept or reject the connection.</span></span> <span data-ttu-id="b52c1-160">但是，如果 \_ 未啟用「條件式接受」選項， \_ 且應用程式允許 TCP 堆疊和「接聽」待處理專案如預期般運作，則應用程式可能會執行得更好。</span><span class="sxs-lookup"><span data-stu-id="b52c1-160">However, applications are likely to perform better if the SO\_CONDITIONAL\_ACCEPT option is not enabled and the application allows the TCP stack and the listen backlog to work as expected.</span></span> <span data-ttu-id="b52c1-161">然後，當應用程式處理已接受的連線時，如果它來自不正確的 IP 來源位址或埠，則應用程式可以直接關閉通訊端。</span><span class="sxs-lookup"><span data-stu-id="b52c1-161">Then when the application handles the accepted connection, if it is from a improper IP source address or port, the application can just close the socket.</span></span> <span data-ttu-id="b52c1-162">此行為的安全性缺點是現在用戶端已確認應用程式正在接聽 IP 位址和埠，因為它已強制關閉先前接受的連線。</span><span class="sxs-lookup"><span data-stu-id="b52c1-162">The security drawback to this behavior is that now the client has confirmation that the application is listening on an IP address and port since it forcefully closed the previously accepted connection.</span></span> <span data-ttu-id="b52c1-163">不過，啟用 **\_ 條件式 \_ 接受** 的缺點通常超過這項限制。</span><span class="sxs-lookup"><span data-stu-id="b52c1-163">However, the drawbacks to enabling **SO\_CONDITIONAL\_ACCEPT** generally outweigh this limitation.</span></span>

<span data-ttu-id="b52c1-164">使用「 **\_ 條件式 \_ 接受** 通訊端」選項呼叫的 [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)函式，可讓應用程式抓取「條件式接受」選項的目前狀態，不過這是通常不使用的功能。</span><span class="sxs-lookup"><span data-stu-id="b52c1-164">The [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function called with the **SO\_CONDITIONAL\_ACCEPT** socket option allows an application to retrieve the current state of the conditional accept option, although this is feature not normally used.</span></span> <span data-ttu-id="b52c1-165">如果應用程式需要在通訊端上啟用條件式接受，則 justs 會呼叫 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 函式來啟用此選項。</span><span class="sxs-lookup"><span data-stu-id="b52c1-165">If an application needs to enable conditional accept on a socket, it justs calls the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function to enable the option.</span></span>

<span data-ttu-id="b52c1-166">請注意， *Ws2def .h* 標頭檔會自動包含在 *Winsock2* 中，而且絕不能直接使用。</span><span class="sxs-lookup"><span data-stu-id="b52c1-166">Note that the *Ws2def.h* header file is automatically included in *Winsock2.h*, and should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="b52c1-167">規格需求</span><span class="sxs-lookup"><span data-stu-id="b52c1-167">Requirements</span></span>



| <span data-ttu-id="b52c1-168">需求</span><span class="sxs-lookup"><span data-stu-id="b52c1-168">Requirement</span></span> | <span data-ttu-id="b52c1-169">值</span><span class="sxs-lookup"><span data-stu-id="b52c1-169">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b52c1-170">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b52c1-170">Minimum supported client</span></span><br/> | <span data-ttu-id="b52c1-171">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b52c1-171">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b52c1-172">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b52c1-172">Minimum supported server</span></span><br/> | <span data-ttu-id="b52c1-173">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b52c1-173">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b52c1-174">標頭</span><span class="sxs-lookup"><span data-stu-id="b52c1-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="b52c1-175"><dt>Ws2def (包含 Winsock2) </dt></span><span class="sxs-lookup"><span data-stu-id="b52c1-175"><dt>Ws2def.h (include Winsock2.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b52c1-176">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b52c1-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b52c1-177">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="b52c1-177">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="b52c1-178">**setsockopt**</span><span class="sxs-lookup"><span data-stu-id="b52c1-178">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[<span data-ttu-id="b52c1-179">**WSAAccept**</span><span class="sxs-lookup"><span data-stu-id="b52c1-179">**WSAAccept**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept)
</dt> </dl>

 

 





---
description: 傳回通訊端使用的本機位址、本機埠、遠端位址、遠端埠、通訊端類型和通訊協定。
ms.assetid: 2628f47e-3e73-4e02-91b8-ba4cb0800864
title: 'SO_BSP_STATE 通訊端選項 (Ws2def) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d10e391d70dd67190e1aec803036d019261c9000
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692207"
---
# <a name="so_bsp_state-socket-option"></a><span data-ttu-id="57a11-103">所以 \_ BSP \_ 狀態通訊端選項</span><span class="sxs-lookup"><span data-stu-id="57a11-103">SO\_BSP\_STATE socket option</span></span>

<span data-ttu-id="57a11-104">**所謂的 \_ BSP \_ 狀態** 通訊端選項會傳回本機位址、本機埠、遠端位址、遠端埠、通訊端類型，以及通訊端使用的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="57a11-104">The **SO\_BSP\_STATE** socket option returns the local address, local port, remote address, remote port, socket type, and protocol used by a socket.</span></span>

<span data-ttu-id="57a11-105">若要執行這項作業，請使用下列參數呼叫 [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) 函數。</span><span class="sxs-lookup"><span data-stu-id="57a11-105">To perform this operation, call the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function with the following parameters.</span></span>

## <a name="socket-option-value"></a><span data-ttu-id="57a11-106">通訊端選項值</span><span class="sxs-lookup"><span data-stu-id="57a11-106">Socket option value</span></span>

<span data-ttu-id="57a11-107">表示這個通訊端選項的常數是0x1009。</span><span class="sxs-lookup"><span data-stu-id="57a11-107">The constant that represents this socket option is 0x1009.</span></span>

## <a name="syntax"></a><span data-ttu-id="57a11-108">語法</span><span class="sxs-lookup"><span data-stu-id="57a11-108">Syntax</span></span>


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_BSP_STATE, // optname
  (char *) optval,         // output buffer,
  (int) *optlen,       // size of output buffer
);
```



## <a name="parameters"></a><span data-ttu-id="57a11-109">參數</span><span class="sxs-lookup"><span data-stu-id="57a11-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57a11-110"> \[ 中的 s\]</span><span class="sxs-lookup"><span data-stu-id="57a11-110">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57a11-111">識別通訊端的描述元。</span><span class="sxs-lookup"><span data-stu-id="57a11-111">A descriptor identifying the socket.</span></span>

</dd> <dt>

<span data-ttu-id="57a11-112">*層級* \[在\]</span><span class="sxs-lookup"><span data-stu-id="57a11-112">*level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57a11-113">定義選項的層級。</span><span class="sxs-lookup"><span data-stu-id="57a11-113">The level at which the option is defined.</span></span> <span data-ttu-id="57a11-114">使用 **SOL \_ 通訊端** 進行這種操作。</span><span class="sxs-lookup"><span data-stu-id="57a11-114">Use **SOL\_SOCKET** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="57a11-115">*optname* \[在\]</span><span class="sxs-lookup"><span data-stu-id="57a11-115">*optname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57a11-116">要抓取值的通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="57a11-116">The socket option for which the value is to be retrieved.</span></span> <span data-ttu-id="57a11-117">請使用此作業的 **\_ BSP \_ 狀態** 。</span><span class="sxs-lookup"><span data-stu-id="57a11-117">Use **SO\_BSP\_STATE** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="57a11-118">*optval* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="57a11-118">*optval* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57a11-119">緩衝區的指標，此緩衝區會傳回所要求選項的值。</span><span class="sxs-lookup"><span data-stu-id="57a11-119">A pointer to the buffer in which the value for the requested option is to be returned.</span></span> <span data-ttu-id="57a11-120">此參數應指向等於或大於 [**CSADDR \_ 資訊**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) 結構大小的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="57a11-120">This parameter should point to buffer equal to or larger than the size of a [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure.</span></span>

</dd> <dt>

<span data-ttu-id="57a11-121">*optlen* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="57a11-121">*optlen* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="57a11-122">*Optval* 緩衝區大小的指標，以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="57a11-122">A pointer to the size, in bytes, of the *optval* buffer.</span></span> <span data-ttu-id="57a11-123">此大小必須等於或大於 [**CSADDR \_ 資訊**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="57a11-123">This size must be equal to or larger than the size of a [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57a11-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="57a11-124">Return value</span></span>

<span data-ttu-id="57a11-125">如果作業順利完成， [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) 會傳回零。</span><span class="sxs-lookup"><span data-stu-id="57a11-125">If the operation completes successfully, [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) returns zero.</span></span>

<span data-ttu-id="57a11-126">如果作業失敗， \_ 則會傳回 SOCKET 錯誤的值，並藉由呼叫 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)來取出特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="57a11-126">If the operation fails, a value of SOCKET\_ERROR is returned and a specific error code can be retrieved by calling [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>



| <span data-ttu-id="57a11-127">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="57a11-127">Error code</span></span>                                                                                                                                              | <span data-ttu-id="57a11-128">意義</span><span class="sxs-lookup"><span data-stu-id="57a11-128">Meaning</span></span>                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="57a11-129"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="57a11-129"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span></span> </dl> | <span data-ttu-id="57a11-130">在使用此函式之前，必須先進行成功的 [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) 呼叫。</span><span class="sxs-lookup"><span data-stu-id="57a11-130">A successful [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) call must occur before using this function.</span></span><br/>                                                                                                                                                                                     |
| <dl> <span data-ttu-id="57a11-131"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="57a11-131"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="57a11-132">網路子系統失敗。</span><span class="sxs-lookup"><span data-stu-id="57a11-132">The network subsystem has failed.</span></span><br/>                                                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="57a11-133"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="57a11-133"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="57a11-134">其中一個 *optval* 或 *optlen* 參數指向不在使用者位址空間有效部分的記憶體。</span><span class="sxs-lookup"><span data-stu-id="57a11-134">One of the *optval* or the *optlen* parameters point to memory that is not in a valid part of the user address space.</span></span> <span data-ttu-id="57a11-135">如果 *optlen* 參數所指向的值小於 [**CSADDR \_ 資訊**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) 結構的大小，也會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="57a11-135">This error is also returned if the value pointed to by the *optlen* parameter is less than the size of a [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure.</span></span><br/> |
| <dl> <span data-ttu-id="57a11-136"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="57a11-136"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="57a11-137">封鎖的 Windows 通訊端1.1 呼叫正在進行中，或服務提供者仍在處理回呼函數。</span><span class="sxs-lookup"><span data-stu-id="57a11-137">A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.</span></span><br/>                                                                                                                                                            |
| <dl> <span data-ttu-id="57a11-138"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="57a11-138"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="57a11-139">*層級* 參數未知或無效。</span><span class="sxs-lookup"><span data-stu-id="57a11-139">The *level* parameter is unknown or invalid.</span></span><br/>                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="57a11-140"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="57a11-140"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="57a11-141">指定的通訊協定系列未知或不支援此選項。</span><span class="sxs-lookup"><span data-stu-id="57a11-141">The option is unknown or unsupported by the indicated protocol family.</span></span><br/>                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="57a11-142"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="57a11-142"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="57a11-143">描述項不是通訊端。</span><span class="sxs-lookup"><span data-stu-id="57a11-143">The descriptor is not a socket.</span></span><br/>                                                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="57a11-144">備註</span><span class="sxs-lookup"><span data-stu-id="57a11-144">Remarks</span></span>

<span data-ttu-id="57a11-145">使用 @ **\_ BSP \_ 狀態** 通訊端選項呼叫的 [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)函式會抓取通訊端使用的本機位址、本機埠、遠端位址、遠端埠、通訊端類型和通訊協定。</span><span class="sxs-lookup"><span data-stu-id="57a11-145">The [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function called with the **SO\_BSP\_STATE** socket option retrieves the local address, local port, remote address, remote port, socket type, and protocol used by a socket.</span></span> <span data-ttu-id="57a11-146">**這樣的 \_ BSP \_ 狀態** 通訊端選項適用于 IPv6 或 IPv4 通訊端， (**af \_ INET6** 和 **af \_ INET** 位址系列) 。</span><span class="sxs-lookup"><span data-stu-id="57a11-146">The **SO\_BSP\_STATE** socket option works with IPv6 or IPv4 sockets (the **AF\_INET6** and **AF\_INET** address families).</span></span>

<span data-ttu-id="57a11-147">如果 [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)函式成功，則會以 *optval* 參數所指向之緩衝區中的 [**CSADDR \_ 資訊**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)結構傳回信息。</span><span class="sxs-lookup"><span data-stu-id="57a11-147">If the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function is successful, the information is returned in a [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure in the buffer pointed to by the *optval* parameter.</span></span> <span data-ttu-id="57a11-148">*Optlen* 所指向的整數最初應該包含這個緩衝區的大小;傳回時，它會設定為 *optval* 參數中所傳回值的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="57a11-148">The integer pointed to by *optlen* should originally contain the size of this buffer; on return, it will be set to the length, in bytes, of the value returned in the *optval* parameter.</span></span>

<span data-ttu-id="57a11-149">傳回之 [**CSADDR \_ 資訊**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)結構中的 **iSocketType** 和 **iProtocol** 成員會填入 *s* 參數中的通訊端描述項。</span><span class="sxs-lookup"><span data-stu-id="57a11-149">The **iSocketType** and **iProtocol** members in the returned [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure are filled in for the socket descriptor in the *s* parameter.</span></span>

<span data-ttu-id="57a11-150">如果通訊端處於連接或系結狀態，則傳回之 [**CSADDR \_ 資訊**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)結構的 **LocalAddr** 成員將會設定為代表本機位址和埠的 [SOCKADDR](sockaddr-2.md)結構。</span><span class="sxs-lookup"><span data-stu-id="57a11-150">If the socket is in a connected or bound state, then the **LocalAddr** member of the returned [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure will be set to a [SOCKADDR](sockaddr-2.md) structure representing the local address and port.</span></span> <span data-ttu-id="57a11-151">如果通訊端處於連接狀態，則傳回之 **CSADDR \_ 資訊** 結構的 **RemoteAddr** 成員將會設定為代表遠端位址和埠的 SOCKADDR 結構。</span><span class="sxs-lookup"><span data-stu-id="57a11-151">If the socket is in a connected state, then the **RemoteAddr** member of the returned **CSADDR\_INFO** structure will be set to a SOCKADDR structure representing the remote address and port.</span></span>

<span data-ttu-id="57a11-152">如果通訊端不是處於連接或系結狀態，則會傳回傳回之 [**CSADDR \_ 資訊**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)結構的 **LocalAddr** 成員，並在 **lpSockaddr** 成員中傳回 **Null** 指標，並將 **iSockaddrLength** 成員設為零。</span><span class="sxs-lookup"><span data-stu-id="57a11-152">If the socket is not in a connected or bound state, then the **LocalAddr** member of the returned [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure is returned with a **NULL** pointer in the **lpSockaddr** member and the **iSockaddrLength** member set to zero.</span></span> <span data-ttu-id="57a11-153">如果通訊端不是處於系結狀態，則傳回之 **CSADDR \_ 資訊** 結構的 **RemoteAddr** 成員會以 **lpSockaddr** 成員中的 **Null** 指標和 **iSockaddrLength** 成員設定為零的方式傳回。</span><span class="sxs-lookup"><span data-stu-id="57a11-153">If the socket is not in a bound state, then the **RemoteAddr** member of the returned **CSADDR\_INFO** structure is returned with a **NULL** pointer in the **lpSockaddr** member and the **iSockaddrLength** member set to zero.</span></span>

<span data-ttu-id="57a11-154">如果 [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) 函式失敗， *optval* 和 *optlen* 參數會保持不變，而且 *Optval* 參數不會指向傳回的 [**CSADDR \_ 資訊**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) 結構。</span><span class="sxs-lookup"><span data-stu-id="57a11-154">If the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function fails, the *optval* and *optlen* parameters are left unchanged and the *optval* parameter does not point to a returned [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure.</span></span>

<span data-ttu-id="57a11-155">請注意， *Ws2def .h* 標頭檔會自動包含在 *Winsock2* 中，而且絕不能直接使用。</span><span class="sxs-lookup"><span data-stu-id="57a11-155">Note that the *Ws2def.h* header file is automatically included in *Winsock2.h*, and should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="57a11-156">規格需求</span><span class="sxs-lookup"><span data-stu-id="57a11-156">Requirements</span></span>



| <span data-ttu-id="57a11-157">需求</span><span class="sxs-lookup"><span data-stu-id="57a11-157">Requirement</span></span> | <span data-ttu-id="57a11-158">值</span><span class="sxs-lookup"><span data-stu-id="57a11-158">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57a11-159">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="57a11-159">Minimum supported client</span></span><br/> | <span data-ttu-id="57a11-160">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57a11-160">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="57a11-161">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="57a11-161">Minimum supported server</span></span><br/> | <span data-ttu-id="57a11-162">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57a11-162">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="57a11-163">標頭</span><span class="sxs-lookup"><span data-stu-id="57a11-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="57a11-164"><dt>Ws2def (包含 Winsock2) </dt></span><span class="sxs-lookup"><span data-stu-id="57a11-164"><dt>Ws2def.h (include Winsock2.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57a11-165">另請參閱</span><span class="sxs-lookup"><span data-stu-id="57a11-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57a11-166">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="57a11-166">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="57a11-167">**CSADDR \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="57a11-167">**CSADDR\_INFO**</span></span>](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)
</dt> <dt>

[<span data-ttu-id="57a11-168">SOCKADDR</span><span class="sxs-lookup"><span data-stu-id="57a11-168">SOCKADDR</span></span>](sockaddr-2.md)
</dt> </dl>

 

 

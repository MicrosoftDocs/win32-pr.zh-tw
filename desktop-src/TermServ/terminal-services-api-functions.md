---
title: 遠端桌面服務 API 函數
description: 下列函式會搭配遠端桌面服務使用。
ms.assetid: e99a86ee-af0e-46db-8dad-69703ca84fa0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e94a2168f5ad4501b9725b72923c98ea97cc707c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682527"
---
# <a name="remote-desktop-services-api-functions"></a><span data-ttu-id="ee12d-103">遠端桌面服務 API 函數</span><span class="sxs-lookup"><span data-stu-id="ee12d-103">Remote Desktop Services API Functions</span></span>

<span data-ttu-id="ee12d-104">下列函式會搭配遠端桌面服務使用。</span><span class="sxs-lookup"><span data-stu-id="ee12d-104">The following functions are used with Remote Desktop Services.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ee12d-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="ee12d-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="ee12d-106">**ProcessIdToSessionId**</span><span class="sxs-lookup"><span data-stu-id="ee12d-106">**ProcessIdToSessionId**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid)
</dt> <dd>

<span data-ttu-id="ee12d-107">抓取與指定進程相關聯的遠端桌面服務會話。</span><span class="sxs-lookup"><span data-stu-id="ee12d-107">Retrieves the Remote Desktop Services session associated with a specified process.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-108">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="ee12d-108">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dd>

<span data-ttu-id="ee12d-109">開啟指定之遠端桌面授權伺服器的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ee12d-109">Opens a handle to the specified Remote Desktop license server.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-110">**TLSDisconnectFromServer**</span><span class="sxs-lookup"><span data-stu-id="ee12d-110">**TLSDisconnectFromServer**</span></span>](tlsdisconnectfromserver.md)
</dt> <dd>

<span data-ttu-id="ee12d-111">關閉遠端桌面授權伺服器的開啟控制碼。</span><span class="sxs-lookup"><span data-stu-id="ee12d-111">Closes an open handle to a Remote Desktop license server.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-112">**TLSGetServerCertificate**</span><span class="sxs-lookup"><span data-stu-id="ee12d-112">**TLSGetServerCertificate**</span></span>](tlsgetservercertificate.md)
</dt> <dd>

<span data-ttu-id="ee12d-113">傳回到遠端桌面授權伺服器的憑證。</span><span class="sxs-lookup"><span data-stu-id="ee12d-113">Returns the certificate of the Remote Desktop license server.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-114">**TLSKeyPackEnumBegin**</span><span class="sxs-lookup"><span data-stu-id="ee12d-114">**TLSKeyPackEnumBegin**</span></span>](tlskeypackenumbegin.md)
</dt> <dd>

<span data-ttu-id="ee12d-115">根據搜尋準則，在遠端桌面授權伺服器上安裝的所有金鑰套件開始列舉。</span><span class="sxs-lookup"><span data-stu-id="ee12d-115">Begins enumeration through all key packs that are installed on a Remote Desktop license server based on search criteria.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-116">**TLSKeyPackEnumEnd**</span><span class="sxs-lookup"><span data-stu-id="ee12d-116">**TLSKeyPackEnumEnd**</span></span>](tlskeypackenumend.md)
</dt> <dd>

<span data-ttu-id="ee12d-117">從先前的 [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) 函式呼叫繼續，然後終止列舉。</span><span class="sxs-lookup"><span data-stu-id="ee12d-117">Continues from a previous call to the [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) function and terminates the enumeration.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-118">**TLSKeyPackEnumNext**</span><span class="sxs-lookup"><span data-stu-id="ee12d-118">**TLSKeyPackEnumNext**</span></span>](tlskeypackenumnext.md)
</dt> <dd>

<span data-ttu-id="ee12d-119">繼續進行先前的 [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) 函式呼叫，並傳回與搜尋條件相符的遠端桌面授權伺服器上所安裝的下一個金鑰套件。</span><span class="sxs-lookup"><span data-stu-id="ee12d-119">Continues from a previous call to the [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) function and returns the next key pack that is installed on a Remote Desktop license server that matches the search criteria.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-120">**TLSLicenseEnumBegin**</span><span class="sxs-lookup"><span data-stu-id="ee12d-120">**TLSLicenseEnumBegin**</span></span>](tlslicenseenumbegin.md)
</dt> <dd>

<span data-ttu-id="ee12d-121">根據搜尋準則開始列舉遠端桌面授權伺服器所發行的授權。</span><span class="sxs-lookup"><span data-stu-id="ee12d-121">Begins enumeration of licenses that are issued by the Remote Desktop license server based on search criteria.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-122">**TLSLicenseEnumEnd**</span><span class="sxs-lookup"><span data-stu-id="ee12d-122">**TLSLicenseEnumEnd**</span></span>](tlslicenseenumend.md)
</dt> <dd>

<span data-ttu-id="ee12d-123">從先前的 [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) 函式呼叫繼續，然後終止列舉。</span><span class="sxs-lookup"><span data-stu-id="ee12d-123">Continues from a previous call to the [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) function and terminates the enumeration.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-124">**TLSLicenseEnumNext**</span><span class="sxs-lookup"><span data-stu-id="ee12d-124">**TLSLicenseEnumNext**</span></span>](tlslicenseenumnext.md)
</dt> <dd>

<span data-ttu-id="ee12d-125">繼續進行先前的 [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) 函式呼叫，並傳回與搜尋條件相符的遠端桌面授權伺服器上所安裝的下一個授權。</span><span class="sxs-lookup"><span data-stu-id="ee12d-125">Continues from a previous call to the [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) function and returns the next license that is installed on a Remote Desktop license server that matches the search criteria.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-126">**VirtualChannelClose**</span><span class="sxs-lookup"><span data-stu-id="ee12d-126">**VirtualChannelClose**</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelclose)
</dt> <dd>

<span data-ttu-id="ee12d-127">關閉虛擬通道的用戶端。</span><span class="sxs-lookup"><span data-stu-id="ee12d-127">Closes the client end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-128">**VirtualChannelEntry**</span><span class="sxs-lookup"><span data-stu-id="ee12d-128">**VirtualChannelEntry**</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelentry)
</dt> <dd>

<span data-ttu-id="ee12d-129">應用程式的用戶端 DLL 的應用程式定義進入點，此應用程式會使用遠端桌面服務的虛擬通道。</span><span class="sxs-lookup"><span data-stu-id="ee12d-129">An application-defined entry point for the client-side DLL of an application that uses Remote Desktop Services virtual channels.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-130">**VirtualChannelInit**</span><span class="sxs-lookup"><span data-stu-id="ee12d-130">**VirtualChannelInit**</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit)
</dt> <dd>

<span data-ttu-id="ee12d-131">初始化用戶端 DLL 對遠端桌面服務虛擬通道的存取。</span><span class="sxs-lookup"><span data-stu-id="ee12d-131">Initializes a client DLL's access to Remote Desktop Services virtual channels.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-132">*VirtualChannelInitEvent*</span><span class="sxs-lookup"><span data-stu-id="ee12d-132">*VirtualChannelInitEvent*</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-channel_init_event_fn)
</dt> <dd>

<span data-ttu-id="ee12d-133">應用程式定義的回呼函式，遠端桌面服務呼叫以通知用戶端 DLL 的虛擬通道事件。</span><span class="sxs-lookup"><span data-stu-id="ee12d-133">An application-defined callback function that Remote Desktop Services calls to notify the client DLL of virtual channel events.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-134">**VirtualChannelOpen**</span><span class="sxs-lookup"><span data-stu-id="ee12d-134">**VirtualChannelOpen**</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen)
</dt> <dd>

<span data-ttu-id="ee12d-135">開啟虛擬通道的用戶端。</span><span class="sxs-lookup"><span data-stu-id="ee12d-135">Opens the client end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-136">*VirtualChannelOpenEvent*</span><span class="sxs-lookup"><span data-stu-id="ee12d-136">*VirtualChannelOpenEvent*</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn)
</dt> <dd>

<span data-ttu-id="ee12d-137">遠端桌面服務呼叫的應用程式定義回呼函式，以通知用戶端 DLL 特定虛擬通道的事件。</span><span class="sxs-lookup"><span data-stu-id="ee12d-137">An application-defined callback function that Remote Desktop Services calls to notify the client DLL of events for a specific virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-138">**VirtualChannelWrite**</span><span class="sxs-lookup"><span data-stu-id="ee12d-138">**VirtualChannelWrite**</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelwrite)
</dt> <dd>

<span data-ttu-id="ee12d-139">將資料從虛擬通道的用戶端端傳送到伺服器端上的夥伴應用程式。</span><span class="sxs-lookup"><span data-stu-id="ee12d-139">Sends data from the client end of a virtual channel to a partner application on the server end.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-140">**WTSCloseServer**</span><span class="sxs-lookup"><span data-stu-id="ee12d-140">**WTSCloseServer**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscloseserver)
</dt> <dd>

<span data-ttu-id="ee12d-141">關閉遠端桌面工作階段主機 (RD 工作階段主機) server 的開啟控制碼。</span><span class="sxs-lookup"><span data-stu-id="ee12d-141">Closes an open handle to a Remote Desktop Session Host (RD Session Host) server.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-142">**WTSConnectSession**</span><span class="sxs-lookup"><span data-stu-id="ee12d-142">**WTSConnectSession**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsconnectsessiona)
</dt> <dd>

<span data-ttu-id="ee12d-143">將遠端桌面服務會話連接到本機電腦上的現有會話。</span><span class="sxs-lookup"><span data-stu-id="ee12d-143">Connects a Remote Desktop Services session to an existing session on the local computer.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-144">**WTSCreateListener**</span><span class="sxs-lookup"><span data-stu-id="ee12d-144">**WTSCreateListener**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscreatelistenera)
</dt> <dd>

<span data-ttu-id="ee12d-145">建立新的遠端桌面服務接聽程式，或設定現有的接聽程式。</span><span class="sxs-lookup"><span data-stu-id="ee12d-145">Creates a new Remote Desktop Services listener or configures an existing listener.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-146">**WTSDisconnectSession**</span><span class="sxs-lookup"><span data-stu-id="ee12d-146">**WTSDisconnectSession**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsdisconnectsession)
</dt> <dd>

<span data-ttu-id="ee12d-147">中斷已登入的使用者與指定的遠端桌面服務會話的連線，而不關閉會話。</span><span class="sxs-lookup"><span data-stu-id="ee12d-147">Disconnects the logged-on user from the specified Remote Desktop Services session without closing the session.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-148">**WTSEnableChildSessions**</span><span class="sxs-lookup"><span data-stu-id="ee12d-148">**WTSEnableChildSessions**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions)
</dt> <dd>

<span data-ttu-id="ee12d-149">啟用或停用 [子會話](child-sessions.md)。</span><span class="sxs-lookup"><span data-stu-id="ee12d-149">Enables or disables [Child Sessions](child-sessions.md).</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-150">**WTSEnumerateListeners**</span><span class="sxs-lookup"><span data-stu-id="ee12d-150">**WTSEnumerateListeners**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratelistenersa)
</dt> <dd>

<span data-ttu-id="ee12d-151">列舉 RD 工作階段主機伺服器上的所有遠端桌面服務接聽程式。</span><span class="sxs-lookup"><span data-stu-id="ee12d-151">Enumerates all the Remote Desktop Services listeners on a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-152">**WTSEnumerateProcesses**</span><span class="sxs-lookup"><span data-stu-id="ee12d-152">**WTSEnumerateProcesses**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesa)
</dt> <dd>

<span data-ttu-id="ee12d-153">抓取指定 RD 工作階段主機伺服器上使用中進程的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ee12d-153">Retrieves information about the active processes on a specified RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-154">**WTSEnumerateProcessesEx**</span><span class="sxs-lookup"><span data-stu-id="ee12d-154">**WTSEnumerateProcessesEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesexa)
</dt> <dd>

<span data-ttu-id="ee12d-155">抓取指定 RD 工作階段主機伺服器上的作用中進程的相關資訊，或 (RD 虛擬化主機) 伺服器上的遠端桌面虛擬化主機。</span><span class="sxs-lookup"><span data-stu-id="ee12d-155">Retrieves information about the active processes on the specified RD Session Host server or Remote Desktop Virtualization Host (RD Virtualization Host) server.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-156">**WTSEnumerateServers**</span><span class="sxs-lookup"><span data-stu-id="ee12d-156">**WTSEnumerateServers**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateserversa)
</dt> <dd>

<span data-ttu-id="ee12d-157">傳回指定網域內所有 RD 工作階段主機伺服器的清單。</span><span class="sxs-lookup"><span data-stu-id="ee12d-157">Returns a list of all RD Session Host servers within the specified domain.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-158">**WTSEnumerateSessions**</span><span class="sxs-lookup"><span data-stu-id="ee12d-158">**WTSEnumerateSessions**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsa)
</dt> <dd>

<span data-ttu-id="ee12d-159">抓取 RD 工作階段主機伺服器上的會話清單。</span><span class="sxs-lookup"><span data-stu-id="ee12d-159">Retrieves a list of sessions on a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-160">**WTSEnumerateSessionsEx**</span><span class="sxs-lookup"><span data-stu-id="ee12d-160">**WTSEnumerateSessionsEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsexa)
</dt> <dd>

<span data-ttu-id="ee12d-161">抓取指定 RD 工作階段主機伺服器或 RD 虛擬化主機伺服器上的會話清單。</span><span class="sxs-lookup"><span data-stu-id="ee12d-161">Retrieves a list of sessions on a specified RD Session Host server or RD Virtualization Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-162">**WTSFreeMemory**</span><span class="sxs-lookup"><span data-stu-id="ee12d-162">**WTSFreeMemory**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememory)
</dt> <dd>

<span data-ttu-id="ee12d-163">釋出遠端桌面服務函數所配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="ee12d-163">Frees memory allocated by a Remote Desktop Services function.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-164">**WTSFreeMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="ee12d-164">**WTSFreeMemoryEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememoryexa)
</dt> <dd>

<span data-ttu-id="ee12d-165">釋放包含 [**WTS \_ 處理 \_ 資訊 \_**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa) 的記憶體，例如 [**或 \_ WTS 會話 \_ 資訊 \_ 1**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a) 結構（由遠端桌面服務函式所配置）。</span><span class="sxs-lookup"><span data-stu-id="ee12d-165">Frees memory that contains [**WTS\_PROCESS\_INFO\_EX**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa) or [**WTS\_SESSION\_INFO\_1**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a) structures allocated by a Remote Desktop Services function.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-166">**WTSGetActiveConsoleSessionId**</span><span class="sxs-lookup"><span data-stu-id="ee12d-166">**WTSGetActiveConsoleSessionId**</span></span>](/windows/desktop/api/Winbase/nf-winbase-wtsgetactiveconsolesessionid)
</dt> <dd>

<span data-ttu-id="ee12d-167">抓取主控台會話的會話識別碼。</span><span class="sxs-lookup"><span data-stu-id="ee12d-167">Retrieves the session identifier of the console session.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-168">**WTSGetChildSessionId**</span><span class="sxs-lookup"><span data-stu-id="ee12d-168">**WTSGetChildSessionId**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetchildsessionid)
</dt> <dd>

<span data-ttu-id="ee12d-169">抓取子會話識別碼（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="ee12d-169">Retrieves the child session identifier, if present.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-170">**WTSGetListenerSecurity**</span><span class="sxs-lookup"><span data-stu-id="ee12d-170">**WTSGetListenerSecurity**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetlistenersecuritya)
</dt> <dd>

<span data-ttu-id="ee12d-171">抓取遠端桌面服務接聽程式的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="ee12d-171">Retrieves the security descriptor of a Remote Desktop Services listener.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-172">**WTSIsChildSessionsEnabled**</span><span class="sxs-lookup"><span data-stu-id="ee12d-172">**WTSIsChildSessionsEnabled**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled)
</dt> <dd>

<span data-ttu-id="ee12d-173">判斷子會話是否已啟用。</span><span class="sxs-lookup"><span data-stu-id="ee12d-173">Determines whether child sessions are enabled.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-174">**WTSLogoffSession**</span><span class="sxs-lookup"><span data-stu-id="ee12d-174">**WTSLogoffSession**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtslogoffsession)
</dt> <dd>

<span data-ttu-id="ee12d-175">登出指定的遠端桌面服務會話。</span><span class="sxs-lookup"><span data-stu-id="ee12d-175">Logs off a specified Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-176">**WTSOpenServer**</span><span class="sxs-lookup"><span data-stu-id="ee12d-176">**WTSOpenServer**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenservera)
</dt> <dd>

<span data-ttu-id="ee12d-177">開啟指定 RD 工作階段主機伺服器的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ee12d-177">Opens a handle to the specified RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-178">**WTSOpenServerEx**</span><span class="sxs-lookup"><span data-stu-id="ee12d-178">**WTSOpenServerEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenserverexa)
</dt> <dd>

<span data-ttu-id="ee12d-179">開啟指定的 RD 工作階段主機伺服器或 RD 虛擬主機伺服器的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ee12d-179">Opens a handle to the specified RD Session Host server or RD Virtualization Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-180">**WTSQueryListenerConfig**</span><span class="sxs-lookup"><span data-stu-id="ee12d-180">**WTSQueryListenerConfig**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerylistenerconfiga)
</dt> <dd>

<span data-ttu-id="ee12d-181">抓取遠端桌面服務接聽程式的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="ee12d-181">Retrieves configuration information for a Remote Desktop Services listener.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-182">**WTSQuerySessionInformation**</span><span class="sxs-lookup"><span data-stu-id="ee12d-182">**WTSQuerySessionInformation**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa)
</dt> <dd>

<span data-ttu-id="ee12d-183">抓取指定 RD 工作階段主機伺服器上指定之會話的會話資訊。</span><span class="sxs-lookup"><span data-stu-id="ee12d-183">Retrieves session information for the specified session on the specified RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-184">**WTSQueryUserConfig**</span><span class="sxs-lookup"><span data-stu-id="ee12d-184">**WTSQueryUserConfig**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga)
</dt> <dd>

<span data-ttu-id="ee12d-185">抓取指定網域控制站或 RD 工作階段主機伺服器上指定之使用者的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="ee12d-185">Retrieves configuration information for the specified user on the specified domain controller or RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-186">**WTSQueryUserToken**</span><span class="sxs-lookup"><span data-stu-id="ee12d-186">**WTSQueryUserToken**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryusertoken)
</dt> <dd>

<span data-ttu-id="ee12d-187">取得會話識別碼所指定之已登入使用者的主要存取權杖。</span><span class="sxs-lookup"><span data-stu-id="ee12d-187">Obtains the primary access token of the logged-on user specified by the session ID.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-188">**WTSRegisterSessionNotification**</span><span class="sxs-lookup"><span data-stu-id="ee12d-188">**WTSRegisterSessionNotification**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification)
</dt> <dd>

<span data-ttu-id="ee12d-189">註冊指定的視窗，以接收會話變更通知。</span><span class="sxs-lookup"><span data-stu-id="ee12d-189">Registers the specified window to receive session change notifications.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-190">**WTSRegisterSessionNotificationEx**</span><span class="sxs-lookup"><span data-stu-id="ee12d-190">**WTSRegisterSessionNotificationEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotificationex)
</dt> <dd>

<span data-ttu-id="ee12d-191">註冊指定的視窗，以接收會話變更通知。</span><span class="sxs-lookup"><span data-stu-id="ee12d-191">Registers the specified window to receive session change notifications.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-192">**WTSSendMessage**</span><span class="sxs-lookup"><span data-stu-id="ee12d-192">**WTSSendMessage**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea)
</dt> <dd>

<span data-ttu-id="ee12d-193">在指定的遠端桌面服務會話的用戶端桌面上顯示訊息方塊。</span><span class="sxs-lookup"><span data-stu-id="ee12d-193">Displays a message box on the client desktop of a specified Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-194">**WTSSetListenerSecurity**</span><span class="sxs-lookup"><span data-stu-id="ee12d-194">**WTSSetListenerSecurity**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetlistenersecuritya)
</dt> <dd>

<span data-ttu-id="ee12d-195">設定遠端桌面服務接聽程式的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="ee12d-195">Configures the security descriptor of a Remote Desktop Services listener.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-196">**WTSSetUserConfig**</span><span class="sxs-lookup"><span data-stu-id="ee12d-196">**WTSSetUserConfig**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetuserconfiga)
</dt> <dd>

<span data-ttu-id="ee12d-197">修改指定網域控制站或 RD 工作階段主機伺服器上指定之使用者的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="ee12d-197">Modifies configuration information for the specified user on the specified domain controller or RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-198">**WTSShutdownSystem**</span><span class="sxs-lookup"><span data-stu-id="ee12d-198">**WTSShutdownSystem**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsshutdownsystem)
</dt> <dd>

<span data-ttu-id="ee12d-199">關閉 (，並選擇性地重新開機) 指定的 RD 工作階段主機伺服器。</span><span class="sxs-lookup"><span data-stu-id="ee12d-199">Shuts down (and optionally restarts) the specified RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-200">**WTSStartRemoteControlSession**</span><span class="sxs-lookup"><span data-stu-id="ee12d-200">**WTSStartRemoteControlSession**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstartremotecontrolsessiona)
</dt> <dd>

<span data-ttu-id="ee12d-201">啟動另一個遠端桌面服務會話的遠端控制。</span><span class="sxs-lookup"><span data-stu-id="ee12d-201">Starts the remote control of another Remote Desktop Services session.</span></span> <span data-ttu-id="ee12d-202">您必須從遠端會話呼叫這個函數。</span><span class="sxs-lookup"><span data-stu-id="ee12d-202">You must call this function from a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-203">**WTSStopRemoteControlSession**</span><span class="sxs-lookup"><span data-stu-id="ee12d-203">**WTSStopRemoteControlSession**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstopremotecontrolsession)
</dt> <dd>

<span data-ttu-id="ee12d-204">停止遠端控制會話。</span><span class="sxs-lookup"><span data-stu-id="ee12d-204">Stops a remote control session.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-205">**WTSTerminateProcess**</span><span class="sxs-lookup"><span data-stu-id="ee12d-205">**WTSTerminateProcess**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsterminateprocess)
</dt> <dd>

<span data-ttu-id="ee12d-206">終止指定的 RD 工作階段主機伺服器上指定的進程。</span><span class="sxs-lookup"><span data-stu-id="ee12d-206">Terminates the specified process on the specified RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-207">**WTSUnRegisterSessionNotification**</span><span class="sxs-lookup"><span data-stu-id="ee12d-207">**WTSUnRegisterSessionNotification**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotification)
</dt> <dd>

<span data-ttu-id="ee12d-208">取消註冊指定的視窗，使其不會收到任何進一步的會話變更通知。</span><span class="sxs-lookup"><span data-stu-id="ee12d-208">Unregisters the specified window so that it receives no further session change notifications.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-209">**WTSUnRegisterSessionNotificationEx**</span><span class="sxs-lookup"><span data-stu-id="ee12d-209">**WTSUnRegisterSessionNotificationEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotificationex)
</dt> <dd>

<span data-ttu-id="ee12d-210">取消註冊指定的視窗，使其不會收到任何進一步的會話變更通知。</span><span class="sxs-lookup"><span data-stu-id="ee12d-210">Unregisters the specified window so that it receives no further session change notifications.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-211">**WTSVirtualChannelClose**</span><span class="sxs-lookup"><span data-stu-id="ee12d-211">**WTSVirtualChannelClose**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelclose)
</dt> <dd>

<span data-ttu-id="ee12d-212">關閉開啟的虛擬通道控制碼。</span><span class="sxs-lookup"><span data-stu-id="ee12d-212">Closes an open virtual channel handle.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-213">**WTSVirtualChannelOpen**</span><span class="sxs-lookup"><span data-stu-id="ee12d-213">**WTSVirtualChannelOpen**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen)
</dt> <dd>

<span data-ttu-id="ee12d-214">開啟指定虛擬通道之伺服器端的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ee12d-214">Opens a handle to the server end of a specified virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-215">**WTSVirtualChannelOpenEx**</span><span class="sxs-lookup"><span data-stu-id="ee12d-215">**WTSVirtualChannelOpenEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex)
</dt> <dd>

<span data-ttu-id="ee12d-216">以類似于 [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen)的方式建立虛擬通道。</span><span class="sxs-lookup"><span data-stu-id="ee12d-216">Creates a virtual channel in a manner similar to [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen).</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-217">**WTSVirtualChannelPurgeInput**</span><span class="sxs-lookup"><span data-stu-id="ee12d-217">**WTSVirtualChannelPurgeInput**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeinput)
</dt> <dd>

<span data-ttu-id="ee12d-218">刪除從用戶端傳送到指定虛擬通道上伺服器的所有已排入佇列的輸入資料。</span><span class="sxs-lookup"><span data-stu-id="ee12d-218">Deletes all queued input data sent from the client to the server on a specified virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-219">**WTSVirtualChannelPurgeOutput**</span><span class="sxs-lookup"><span data-stu-id="ee12d-219">**WTSVirtualChannelPurgeOutput**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeoutput)
</dt> <dd>

<span data-ttu-id="ee12d-220">刪除從伺服器傳送至指定虛擬通道上之用戶端的所有已排入佇列的輸出資料。</span><span class="sxs-lookup"><span data-stu-id="ee12d-220">Deletes all queued output data sent from the server to the client on a specified virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-221">**WTSVirtualChannelQuery**</span><span class="sxs-lookup"><span data-stu-id="ee12d-221">**WTSVirtualChannelQuery**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery)
</dt> <dd>

<span data-ttu-id="ee12d-222">傳回指定虛擬通道的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ee12d-222">Returns information about a specified virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-223">**WTSVirtualChannelRead**</span><span class="sxs-lookup"><span data-stu-id="ee12d-223">**WTSVirtualChannelRead**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)
</dt> <dd>

<span data-ttu-id="ee12d-224">從虛擬通道的伺服器端讀取資料。</span><span class="sxs-lookup"><span data-stu-id="ee12d-224">Reads data from the server end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-225">**WTSVirtualChannelWrite**</span><span class="sxs-lookup"><span data-stu-id="ee12d-225">**WTSVirtualChannelWrite**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite)
</dt> <dd>

<span data-ttu-id="ee12d-226">將資料寫入虛擬通道的伺服器端。</span><span class="sxs-lookup"><span data-stu-id="ee12d-226">Writes data to the server end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="ee12d-227">**WTSWaitSystemEvent**</span><span class="sxs-lookup"><span data-stu-id="ee12d-227">**WTSWaitSystemEvent**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtswaitsystemevent)
</dt> <dd>

<span data-ttu-id="ee12d-228">先等候遠端桌面服務事件，再返回呼叫端。</span><span class="sxs-lookup"><span data-stu-id="ee12d-228">Waits for a Remote Desktop Services event before returning to the caller.</span></span>

</dd> </dl>

 

 
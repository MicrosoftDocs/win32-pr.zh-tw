---
title: AppIDFlags
description: 一組旗標，可控制 COM 伺服器的啟用行為。
ms.assetid: ab98e7d3-85c6-4328-84c4-1d4583df69ce
keywords:
- AppIDFlags 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdad2b80625d6a60460d43f242d7897e0ae7eb40
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106966062"
---
# <a name="appidflags"></a><span data-ttu-id="caf5f-104">AppIDFlags</span><span class="sxs-lookup"><span data-stu-id="caf5f-104">AppIDFlags</span></span>

<span data-ttu-id="caf5f-105">一組旗標，可控制 COM 伺服器的啟用行為。</span><span class="sxs-lookup"><span data-stu-id="caf5f-105">A set of flags that control the activation behavior of a COM server.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="caf5f-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="caf5f-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AppIDFlags = flags
```

## <a name="remarks"></a><span data-ttu-id="caf5f-107">備註</span><span class="sxs-lookup"><span data-stu-id="caf5f-107">Remarks</span></span>

<span data-ttu-id="caf5f-108">這是 **REG \_ DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="caf5f-108">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="caf5f-109">旗標值</span><span class="sxs-lookup"><span data-stu-id="caf5f-109">Flag Value</span></span> | <span data-ttu-id="caf5f-110">常數</span><span class="sxs-lookup"><span data-stu-id="caf5f-110">Constant</span></span>                                              |
|------------|-------------------------------------------------------|
| <span data-ttu-id="caf5f-111">0x1</span><span class="sxs-lookup"><span data-stu-id="caf5f-111">0x1</span></span>        | <span data-ttu-id="caf5f-112">APPIDREGFLAGS \_ 啟用 \_ IUSERVER \_ INDESKTOP</span><span class="sxs-lookup"><span data-stu-id="caf5f-112">APPIDREGFLAGS\_ACTIVATE\_IUSERVER\_INDESKTOP</span></span>          |
| <span data-ttu-id="caf5f-113">0x2</span><span class="sxs-lookup"><span data-stu-id="caf5f-113">0x2</span></span>        | <span data-ttu-id="caf5f-114">APPIDREGFLAGS \_ SECURE \_ SERVER \_ PROCESS \_ SD \_ 和 \_ BIND</span><span class="sxs-lookup"><span data-stu-id="caf5f-114">APPIDREGFLAGS\_SECURE\_SERVER\_PROCESS\_SD\_AND\_BIND</span></span> |
| <span data-ttu-id="caf5f-115">0x4</span><span class="sxs-lookup"><span data-stu-id="caf5f-115">0x4</span></span>        | <span data-ttu-id="caf5f-116">APPIDREGFLAGS \_ \_ \_ \_ 在識別時發出啟用 RPC \_</span><span class="sxs-lookup"><span data-stu-id="caf5f-116">APPIDREGFLAGS\_ISSUE\_ACTIVATION\_RPC\_AT\_IDENTIFY</span></span>   |



 

### <a name="appidregflags_activate_iuserver_indesktop-description"></a><span data-ttu-id="caf5f-117">APPIDREGFLAGS \_ 啟用 \_ IUSERVER \_ INDESKTOP 描述</span><span class="sxs-lookup"><span data-stu-id="caf5f-117">APPIDREGFLAGS\_ACTIVATE\_IUSERVER\_INDESKTOP Description</span></span>

<span data-ttu-id="caf5f-118">如果 **AppIDFlags** 中的 **APPIDREGFLAGS \_ ACTI加值稅E \_ IUSERVER \_ INDESKTOP** 旗標已清除，或如果沒有 **AppIDFlags** ，則在終端機伺服器會話中的用戶端會對 [互動式使用者](interactive-user.md)COM 伺服器進行啟用要求，將會系結至或啟動並系結至啟用要求中會話之 "winsta0"[視窗工作站](/windows/desktop/winstation/window-stations)的「預設」桌上型電腦中的 COM 伺服器。</span><span class="sxs-lookup"><span data-stu-id="caf5f-118">If the **APPIDREGFLAGS\_ACTIVATE\_IUSERVER\_INDESKTOP** flag is cleared in **AppIDFlags** or if **AppIDFlags** is not present, the client in a terminal server session making an activation request for an [Interactive User](interactive-user.md) COM server, will either bind to, or launch and bind to, the COM server in the "default" desktop of the "winsta0" [window station](/windows/desktop/winstation/window-stations) of the session in the activation request.</span></span> <span data-ttu-id="caf5f-119">例如，如果用戶端執行 \\ 的是會話3的 "winsta0 desktop1"，則會話3的啟用要求會系結至或啟動並系結至會話3的 "winsta0 default" 中的 com 伺服器， \\ 即使 com 伺服器的實例已經在會話3的 "winsta0 desktop1" 中執行也是如此 \\ 。</span><span class="sxs-lookup"><span data-stu-id="caf5f-119">For example, if the client is running "winsta0\\desktop1" of session 3, the activation request for session 3 will either bind to, or launch and bind to, the COM server in "winsta0\\default" of session 3, even if an instance of the COM server is already running in "winsta0\\desktop1" of session 3.</span></span>

<span data-ttu-id="caf5f-120">如果 **AppIDFlags** 值中設定了 **APPIDREGFLAGS \_ ACTI加值稅E \_ IUSERVER \_ INDESKTOP** 旗標，COM 將會系結至或啟動並系結至用戶端桌面上執行的伺服器進程，以及啟用要求中的會話。</span><span class="sxs-lookup"><span data-stu-id="caf5f-120">If the **APPIDREGFLAGS\_ACTIVATE\_IUSERVER\_INDESKTOP** flag is set in the **AppIDFlags** value, COM will either bind to, or launch and bind to, the server process running in the client's desktop and the session in the activation request.</span></span> <span data-ttu-id="caf5f-121">例如，如果用戶端 \\ 在會話3中執行 "winsta0 desktop1"，則會話3的啟用要求會系結至或啟動並系結至會話3中 "winsta0 desktop1" 的 com 伺服器， \\ 即使 com 伺服器的實例已經在會話3的 "winsta0 default" 中執行也是如此 \\ 。</span><span class="sxs-lookup"><span data-stu-id="caf5f-121">For example, if the client is running "winsta0\\desktop1" in session 3, the activation request for session 3 will either bind to, or launch and bind to, the COM server in "winsta0\\desktop1" in session 3, even if an instance of the COM server is already running in "winsta0\\default" in session 3.</span></span>

<span data-ttu-id="caf5f-122">用戶端可以使用會話的「 [標記](/windows/desktop/TermServ/session-monikers) 」來指定與用戶端會話進行啟用要求時不同的會話。</span><span class="sxs-lookup"><span data-stu-id="caf5f-122">The client can use the [session moniker](/windows/desktop/TermServ/session-monikers) to specify a session different than the client's session when it makes the activation request.</span></span>

<span data-ttu-id="caf5f-123">**APPIDREGFLAGS \_ ACTI加值稅E \_ IUSERVER \_ INDESKTOP** 旗標只適用于設定為 RunAs 「[互動式使用者](interactive-user.md)」的 COM 伺服器。</span><span class="sxs-lookup"><span data-stu-id="caf5f-123">The **APPIDREGFLAGS\_ACTIVATE\_IUSERVER\_INDESKTOP** flag applies only to COM servers that are configured to RunAs "[Interactive User](interactive-user.md)".</span></span>

### <a name="appidregflags_secure_server_process_sd_and_bind-description"></a><span data-ttu-id="caf5f-124">APPIDREGFLAGS \_ SECURE \_ SERVER \_ PROCESS \_ SD \_ 和 \_ BIND Description</span><span class="sxs-lookup"><span data-stu-id="caf5f-124">APPIDREGFLAGS\_SECURE\_SERVER\_PROCESS\_SD\_AND\_BIND Description</span></span>

<span data-ttu-id="caf5f-125">如果在 **AppIDFlags** 中設定 **APPIDREGFLAGS \_ SECURE \_ SERVER \_ PROCESS \_ SD \_ 和 \_ BIND** 旗標，則會啟動設定為 RunAs 為 "Activator" 的 COM 伺服器，並提供進程安全描述項，以允許處理處理常式權杖的 LogonID SID 的 [ \_ 所有 \_ 存取](/windows/desktop/ProcThread/process-security-and-access-rights)。</span><span class="sxs-lookup"><span data-stu-id="caf5f-125">If the **APPIDREGFLAGS\_SECURE\_SERVER\_PROCESS\_SD\_AND\_BIND** flag is set in **AppIDFlags**, COM servers that are configured to RunAs "Activator" will be launched with a process security descriptor that allows [PROCESS\_ALL\_ACCESS](/windows/desktop/ProcThread/process-security-and-access-rights) to the LogonID SID of the process token.</span></span> <span data-ttu-id="caf5f-126">此外，安全描述項的擁有者將會設定為進程權杖的 LogonID SID。</span><span class="sxs-lookup"><span data-stu-id="caf5f-126">In addition, the owner of the security descriptor will be set to the LogonID SID of the process token.</span></span>

<span data-ttu-id="caf5f-127">如果在 **AppIDFlags** 中設定 **APPIDREGFLAGS \_ SECURE \_ SERVER \_ PROCESS \_ SD \_ 和 \_ BIND** 旗標，則設定為 RunAs 「此使用者」的 COM 伺服器將會以進程安全描述項啟動，以允許處理常式權杖的 LogonID SID 中的 [ \_ 所有 \_ 存取](/windows/desktop/ProcThread/process-security-and-access-rights)。</span><span class="sxs-lookup"><span data-stu-id="caf5f-127">If the **APPIDREGFLAGS\_SECURE\_SERVER\_PROCESS\_SD\_AND\_BIND** flag is set in **AppIDFlags**, COM servers that are configured to RunAs "This User" will be launched with a process security descriptor that allows [PROCESS\_ALL\_ACCESS](/windows/desktop/ProcThread/process-security-and-access-rights) in the LogonID SID of the process token.</span></span> <span data-ttu-id="caf5f-128">此外，安全描述項的擁有者將會設定為進程權杖的 LogonID SID。</span><span class="sxs-lookup"><span data-stu-id="caf5f-128">In addition, the owner of the security descriptor will be set to the LogonID SID of the process token.</span></span> <span data-ttu-id="caf5f-129">此外，COM 服務控制管理員 (SCM) 修改 COM 伺服器進程的權杖，如下所示：</span><span class="sxs-lookup"><span data-stu-id="caf5f-129">Further, the COM Service Control Manager (SCM) modifies the token of the COM server process as follows:</span></span>

-   <span data-ttu-id="caf5f-130">它會將 APPID SID 新增至權杖。</span><span class="sxs-lookup"><span data-stu-id="caf5f-130">It adds an APPID SID to the token.</span></span> <span data-ttu-id="caf5f-131">它會在權杖預設任意存取控制清單 (DACL) 中，授與 APPID SID 的完整存取權。</span><span class="sxs-lookup"><span data-stu-id="caf5f-131">It grants the APPID SID full access in the token default discretionary access control list (DACL).</span></span> <span data-ttu-id="caf5f-132">在 Windows Vista 和更新版本的 Windows 中，它會授與 \_ 權杖預設 DACL 中的 OWNERRIGHTS SID 讀取控制許可權。</span><span class="sxs-lookup"><span data-stu-id="caf5f-132">In Windows Vista and later versions of Windows, it grants the OwnerRights SID READ\_CONTROL permission in the token default DACL.</span></span> <span data-ttu-id="caf5f-133">在 windows Vista 之前版本的 Windows 中，它會將權杖擁有者設定為 APPID SID。</span><span class="sxs-lookup"><span data-stu-id="caf5f-133">In pre-Windows Vista versions of Windows, it sets the token owner to the APPID SID.</span></span>

<span data-ttu-id="caf5f-134">使用 **APPIDREGFLAGS \_ SECURE \_ SERVER \_ PROCESS \_ SD \_ 和 \_ BIND** 旗標時，必須考慮下列安全性考慮：</span><span class="sxs-lookup"><span data-stu-id="caf5f-134">The following security considerations must be taken into account when using the **APPIDREGFLAGS\_SECURE\_SERVER\_PROCESS\_SD\_AND\_BIND** flag:</span></span>

-   <span data-ttu-id="caf5f-135">**APPIDREGFLAGS \_ SECURE \_ SERVER \_ PROCESS \_ SD \_ 和 \_ BIND** 旗標的設計目的，是由在其中一個內建服務安全性內容（NETWORKSERVICE 或 LocalService 帳戶）下啟動的 COM 伺服器設定。</span><span class="sxs-lookup"><span data-stu-id="caf5f-135">The **APPIDREGFLAGS\_SECURE\_SERVER\_PROCESS\_SD\_AND\_BIND** flag is meant to be set by COM servers that are launched under one of the built-in service security contexts; either the NetworkService or the LocalService accounts.</span></span> <span data-ttu-id="caf5f-136">如果伺服器模擬具有特殊許可權的用戶端，而且未設定 **APPIDREGFLAGS \_ SECURE \_ SERVER \_ PROCESS \_ SD \_ and \_ BIND** 旗標，則在其他具有相同安全性內容的進程中執行的惡意程式碼，可以藉由從 COM 伺服器進程劫持具特殊許可權之用戶端的模擬權杖來提高許可權。</span><span class="sxs-lookup"><span data-stu-id="caf5f-136">If the servers impersonate privileged clients and if the **APPIDREGFLAGS\_SECURE\_SERVER\_PROCESS\_SD\_AND\_BIND** flag is not set, malicious code running in other processes with the same security context can elevate privilege by hijacking the impersonation tokens of the privileged clients from the COM server process.</span></span>
-   <span data-ttu-id="caf5f-137">設定 **APPIDREGFLAGS \_ SECURE \_ SERVER \_ PROCESS \_ SD \_ 和 \_ BIND** 旗標時，com 會在 RunAs "Activator" COM 伺服器的情況下強化進程物件的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="caf5f-137">When the **APPIDREGFLAGS\_SECURE\_SERVER\_PROCESS\_SD\_AND\_BIND** flag is set, COM hardens the security descriptor of the process object in the case of RunAs "Activator" COM servers.</span></span> <span data-ttu-id="caf5f-138">針對這類伺服器，COM 用戶端必須強化它用於 COM 啟用的權杖。</span><span class="sxs-lookup"><span data-stu-id="caf5f-138">For such servers, the COM client is expected to harden the token that it uses for the COM activation.</span></span>
-   <span data-ttu-id="caf5f-139">設定 **APPIDREGFLAGS \_ SECURE \_ SERVER \_ PROCESS \_ SD \_ 和 \_ BIND** 旗標時，COM 會在 RunAs 「此使用者」 COM 伺服器的情況下強化處理常式物件的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="caf5f-139">When the **APPIDREGFLAGS\_SECURE\_SERVER\_PROCESS\_SD\_AND\_BIND** flag is set, COM hardens the security descriptor of the process object in the case of RunAs "This User" COM servers.</span></span> <span data-ttu-id="caf5f-140">它也會強化 COM 伺服器的進程 token，因為 COM SCM 是建立權杖的實體。</span><span class="sxs-lookup"><span data-stu-id="caf5f-140">It also hardens the process token of the COM server since the COM SCM is the entity that creates the token.</span></span>

<span data-ttu-id="caf5f-141">只有在套用 MSRC8322 patch (資訊 [安全佈告欄 MS09-012](https://support.microsoft.com/kb/959454)) 時，windows XP、windows server 2003、windows Vista 和 windows SERVER 2008 才支援 **APPIDREGFLAGS \_ SECURE \_ SERVER \_ PROCESS \_ SD \_ AND \_ BIND** 旗標。</span><span class="sxs-lookup"><span data-stu-id="caf5f-141">The **APPIDREGFLAGS\_SECURE\_SERVER\_PROCESS\_SD\_AND\_BIND** flag is supported in Windows XP, Windows Server 2003, Windows Vista, and Windows Server 2008 only when the MSRC8322 patch ([security bulletin MS09-012](https://support.microsoft.com/kb/959454)) is applied.</span></span> <span data-ttu-id="caf5f-142">Windows 7 和更新版本的 Windows 原本就支援此功能。</span><span class="sxs-lookup"><span data-stu-id="caf5f-142">It is natively supported in Windows 7 and later versions of Windows.</span></span>

<span data-ttu-id="caf5f-143">**APPIDREGFLAGS \_ SECURE \_ SERVER \_ PROCESS \_ SD \_ 和 \_ BIND** 旗標只適用于設定為 RunAs "ACTI加值稅OR" 或 "This User" 的 COM 伺服器。</span><span class="sxs-lookup"><span data-stu-id="caf5f-143">The **APPIDREGFLAGS\_SECURE\_SERVER\_PROCESS\_SD\_AND\_BIND** flag applies only to COM servers that are configured to RunAs "Activator" or "This User".</span></span> <span data-ttu-id="caf5f-144">它並不適用于 NT 服務的 COM 伺服器。</span><span class="sxs-lookup"><span data-stu-id="caf5f-144">It does not apply to COM servers that are NT services.</span></span>

### <a name="appidregflags_issue_activation_rpc_at_identify-description"></a><span data-ttu-id="caf5f-145">APPIDREGFLAGS \_ \_ \_ \_ 在 \_ 識別描述時發出啟用 RPC</span><span class="sxs-lookup"><span data-stu-id="caf5f-145">APPIDREGFLAGS\_ISSUE\_ACTIVATION\_RPC\_AT\_IDENTIFY Description</span></span>

<span data-ttu-id="caf5f-146">如果在 **AppIDFlags** 中設定了 **APPIDREGFLAGS \_ ISSUE \_ 啟用 \_ RPC \_ AT \_ 識別** 旗標，com SCM 將會使用 [RPC \_ C \_ IMP \_ 層級 \_ 識別](impersonation-levels.md)的模擬層級，將物件啟動要求發出至 COM 伺服器進程。</span><span class="sxs-lookup"><span data-stu-id="caf5f-146">If the **APPIDREGFLAGS\_ISSUE\_ACTIVATION\_RPC\_AT\_IDENTIFY** flag is set in **AppIDFlags**, the COM SCM will issue object activation requests to the COM server process using an impersonation level of [RPC\_C\_IMP\_LEVEL\_IDENTIFY](impersonation-levels.md).</span></span>

<span data-ttu-id="caf5f-147">如果未 **設定 \_ APPIDREGFLAGS \_ ISSUE \_ \_ 在 \_ 識別旗標上的啟用 RPC** ，則 com SCM 會將物件啟動要求發出至使用 [RPC \_ C \_ IMP \_ 層級 \_](impersonation-levels.md)模擬之模擬層級的 COM 伺服器處理常式。</span><span class="sxs-lookup"><span data-stu-id="caf5f-147">If the **APPIDREGFLAGS\_ISSUE\_ACTIVATION\_RPC\_AT\_IDENTIFY** flag is not set, the COM SCM will issue object activation requests to the COM server processes using an impersonation level of [RPC\_C\_IMP\_LEVEL\_IMPERSONATE](impersonation-levels.md).</span></span>

<span data-ttu-id="caf5f-148">在識別旗標 **上使用 APPIDREGFLAGS \_ ISSUE \_ 啟用 \_ RPC \_ \_** 時，必須考慮下列安全性考慮：</span><span class="sxs-lookup"><span data-stu-id="caf5f-148">The following security considerations must be taken into account when using the **APPIDREGFLAGS\_ISSUE\_ACTIVATION\_RPC\_AT\_IDENTIFY** flag:</span></span>

-   <span data-ttu-id="caf5f-149">**APPIDREGFLAGS \_ ISSUE \_ \_ \_ 在 \_ 識別** 旗標上的啟動 RPC 是為了讓未代表用戶端在物件啟動要求中執行工作的 COM 伺服器使用。</span><span class="sxs-lookup"><span data-stu-id="caf5f-149">The **APPIDREGFLAGS\_ISSUE\_ACTIVATION\_RPC\_AT\_IDENTIFY** flag is meant to be used by COM servers that do not perform work on behalf of clients in object activation requests.</span></span> <span data-ttu-id="caf5f-150">針對這類伺服器，在 [RPC \_ C \_ IMP \_ 層級 \_](impersonation-levels.md) 使用 COM SCM 發出物件啟動要求，可讓程式中出現具有 [**SE \_ 模擬 \_ 名稱**](/windows/desktop/SecAuthZ/privilege-constants) 層級的特殊許可權權杖機率降到最低。</span><span class="sxs-lookup"><span data-stu-id="caf5f-150">For such servers, having the COM SCM issue object activation requests at [RPC\_C\_IMP\_LEVEL\_IDENTIFY](impersonation-levels.md) minimizes the chances of privileged tokens with [**SE\_IMPERSONATE\_NAME**](/windows/desktop/SecAuthZ/privilege-constants) level appearing in the process.</span></span>

<span data-ttu-id="caf5f-151">在 Windows 7 和更新版本的 Windows 中，支援 **在識別旗標上的 APPIDREGFLAGS \_ 問題 \_ 啟用 \_ RPC \_ \_** 。</span><span class="sxs-lookup"><span data-stu-id="caf5f-151">The **APPIDREGFLAGS\_ISSUE\_ACTIVATION\_RPC\_AT\_IDENTIFY** flag is supported in Windows 7 and later versions of Windows.</span></span>

## <a name="related-topics"></a><span data-ttu-id="caf5f-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="caf5f-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="caf5f-153">桌上型電腦</span><span class="sxs-lookup"><span data-stu-id="caf5f-153">Desktops</span></span>](/windows/desktop/winstation/desktops)
</dt> <dt>

[<span data-ttu-id="caf5f-154">模擬層級</span><span class="sxs-lookup"><span data-stu-id="caf5f-154">Impersonation Levels</span></span>](impersonation-levels.md)
</dt> <dt>

[<span data-ttu-id="caf5f-155">互動式使用者</span><span class="sxs-lookup"><span data-stu-id="caf5f-155">Interactive User</span></span>](interactive-user.md)
</dt> <dt>

[<span data-ttu-id="caf5f-156">會話的名字</span><span class="sxs-lookup"><span data-stu-id="caf5f-156">Session Monikers</span></span>](/windows/desktop/TermServ/session-monikers)
</dt> <dt>

[<span data-ttu-id="caf5f-157">視窗工作站</span><span class="sxs-lookup"><span data-stu-id="caf5f-157">Window Stations</span></span>](/windows/desktop/winstation/window-stations)
</dt> </dl>

 

 
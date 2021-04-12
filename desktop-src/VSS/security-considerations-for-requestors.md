---
description: VSS 基礎結構需要 VSS 要求者（例如，備份應用程式）能夠以 COM 用戶端和伺服器的形式來運作。
ms.assetid: b01145c6-76ba-4a81-bca6-59c4ca488dac
title: 要求者的安全性考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3e989793dbf5a5dd1fac3224cf6f06958564de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318980"
---
# <a name="security-considerations-for-requesters"></a><span data-ttu-id="60b1a-103">要求者的安全性考慮</span><span class="sxs-lookup"><span data-stu-id="60b1a-103">Security Considerations for Requesters</span></span>

<span data-ttu-id="60b1a-104">VSS 基礎結構需要 VSS 要求者（例如，備份應用程式）能夠以 COM 用戶端和伺服器的形式來運作。</span><span class="sxs-lookup"><span data-stu-id="60b1a-104">The VSS infrastructure requires VSS requesters, such as backup applications, to be able to function both as COM clients and as a server.</span></span>

<span data-ttu-id="60b1a-105">當作為伺服器時，要求者會公開一組 COM 回呼介面，可從外部 (進程（例如，寫入器或 VSS 服務) ）叫用這些介面。</span><span class="sxs-lookup"><span data-stu-id="60b1a-105">When acting as a server, a requester exposes a set of COM callback interfaces that can be invoked from external processes (such as writers or the VSS service).</span></span> <span data-ttu-id="60b1a-106">因此，要求者需要安全地管理哪些 COM 用戶端能夠讓傳入的 COM 呼叫進入其進程。</span><span class="sxs-lookup"><span data-stu-id="60b1a-106">Therefore, requesters need to securely manage which COM clients are able to make incoming COM calls into its process.</span></span>

<span data-ttu-id="60b1a-107">同樣地，要求者可以作為 VSS 寫入器或 VSS 服務所提供之 COM Api 的 COM 用戶端。</span><span class="sxs-lookup"><span data-stu-id="60b1a-107">Similarly, requesters can act as a COM client for the COM APIs supplied by a VSS writer or by the VSS service.</span></span> <span data-ttu-id="60b1a-108">要求者特定的安全性設定必須允許來自要求者的傳出 COM 呼叫至這些其他進程。</span><span class="sxs-lookup"><span data-stu-id="60b1a-108">The requester-specific security settings must allow outgoing COM calls from the requester to these other processes.</span></span>

<span data-ttu-id="60b1a-109">管理要求者的安全性問題最簡單的機制，就是適當地選取執行它的使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="60b1a-109">The simplest mechanism for managing a requester's security issues involves proper selection of the user account under which it runs.</span></span>

<span data-ttu-id="60b1a-110">要求者通常需要以 Administrators 群組或 Backup Operators 群組成員的使用者身分執行，或是以本機系統帳戶的身分執行。</span><span class="sxs-lookup"><span data-stu-id="60b1a-110">A requester typically needs to run under a user that is a member of either the Administrators group or the Backup Operators group, or run as the Local System account.</span></span>

<span data-ttu-id="60b1a-111">根據預設，當要求者作為 COM 用戶端時，如果它不是在這些帳戶下執行，則任何 COM 呼叫都會自動被 **E \_ ACCESSDENIED** 拒絕，甚至不會進入 COM 方法的執行。</span><span class="sxs-lookup"><span data-stu-id="60b1a-111">By default, when a requester is acting as a COM client, if it does not run under these accounts, any COM call is automatically rejected with **E\_ACCESSDENIED**, without even getting to the COM method implementation.</span></span>

## <a name="disabling-com-exception-handling"></a><span data-ttu-id="60b1a-112">停用 COM 例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="60b1a-112">Disabling COM Exception Handling</span></span>

<span data-ttu-id="60b1a-113">開發要求者時，請將 [COM COMGLB \_ 例外狀況 \_ 沒有 \_ 處理全域選項] 旗標設定為停用 com 例外狀況處理。</span><span class="sxs-lookup"><span data-stu-id="60b1a-113">When developing a requester, set the COM COMGLB\_EXCEPTION\_DONOT\_HANDLE global options flag to disable COM exception handling.</span></span> <span data-ttu-id="60b1a-114">請務必這麼做，因為 COM 例外狀況處理可以遮罩 VSS 應用程式中的嚴重錯誤。</span><span class="sxs-lookup"><span data-stu-id="60b1a-114">It is important to do this because COM exception handling can mask fatal errors in a VSS application.</span></span> <span data-ttu-id="60b1a-115">遮罩的錯誤可能會讓進程處於不穩定且無法預測的狀態，而導致損毀和停止回應。</span><span class="sxs-lookup"><span data-stu-id="60b1a-115">The error that is masked can leave the process in an unstable and unpredictable state, which can lead to corruptions and hangs.</span></span> <span data-ttu-id="60b1a-116">如需此旗標的詳細資訊，請參閱 [IGlobalOptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions)。</span><span class="sxs-lookup"><span data-stu-id="60b1a-116">For more information about this flag, see [IGlobalOptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).</span></span>

## <a name="setting-requester-default-com-access-check-permission"></a><span data-ttu-id="60b1a-117">設定要求者預設 COM 存取檢查許可權</span><span class="sxs-lookup"><span data-stu-id="60b1a-117">Setting Requester Default COM Access Check Permission</span></span>

<span data-ttu-id="60b1a-118">要求者必須注意，當其程式做為伺服器 (例如，允許寫入器修改備份元件檔) 時，必須允許來自其他 VSS 參與者（例如，寫入器或 VSS 服務）的撥入電話。</span><span class="sxs-lookup"><span data-stu-id="60b1a-118">Requesters need to be aware that when their process acts as a server (for example, allowing writers to modify the Backup Components Document), they must allow incoming calls from other VSS participants, such as writers or the VSS service.</span></span>

<span data-ttu-id="60b1a-119">不過，根據預設，Windows 進程只會允許在相同登入會話下執行的 COM 用戶端 (自我 SID) 或在本機系統帳戶下執行。</span><span class="sxs-lookup"><span data-stu-id="60b1a-119">However, by default, a Windows process will allow only COM clients that are running under the same logon session (the SELF SID) or running under the Local System account.</span></span> <span data-ttu-id="60b1a-120">這是潛在問題，因為這些預設值對 VSS 基礎結構而言並不足夠。</span><span class="sxs-lookup"><span data-stu-id="60b1a-120">This is a potential problem because these defaults are not adequate for the VSS infrastructure.</span></span> <span data-ttu-id="60b1a-121">例如，寫入器可能會以「備份操作員」使用者帳戶的形式執行，該帳戶不在與要求者進程相同的登入會話中，也不是本機系統帳戶。</span><span class="sxs-lookup"><span data-stu-id="60b1a-121">For example, writers might run as a "Backup Operator" user account that is neither in the same logon session as the requester process nor a Local System account.</span></span>

<span data-ttu-id="60b1a-122">為了處理這種類型的問題，每個 COM 伺服器進程都可以進一步控制 RPC 或 COM 用戶端是否允許執行伺服器所執行的 COM 方法 (在此案例中，) 使用 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) 來設定整個進程的「預設 COM 存取檢查」許可權。</span><span class="sxs-lookup"><span data-stu-id="60b1a-122">To handle this type of problem, every COM server process can exercise further control over whether an RPC or COM client is allowed to perform a COM method implemented by the server (a requester in this case) by using [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) to set a process-wide "Default COM Access Check Permission".</span></span>

<span data-ttu-id="60b1a-123">要求者可以明確地執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="60b1a-123">Requesters can explicitly do the following:</span></span>

-   <span data-ttu-id="60b1a-124">允許所有進程存取要求者進程的呼叫。</span><span class="sxs-lookup"><span data-stu-id="60b1a-124">Allow all processes access to call into the requester process.</span></span>

    <span data-ttu-id="60b1a-125">此選項可能適用于大部分的要求者，且由其他 COM 伺服器使用，例如，所有 SVCHOST 型 Windows 服務都已使用此選項，預設為所有 COM + 服務。</span><span class="sxs-lookup"><span data-stu-id="60b1a-125">This option may be adequate for the vast majority of requesters, and is used by other COM servers—for example, all SVCHOST-based Windows services are already using this option, as are all COM+ Services by default.</span></span>

    <span data-ttu-id="60b1a-126">允許所有進程執行傳入的 COM 呼叫不一定是安全性弱點。</span><span class="sxs-lookup"><span data-stu-id="60b1a-126">Allowing all processes to perform incoming COM calls is not necessarily a security weakness.</span></span> <span data-ttu-id="60b1a-127">作為 COM 伺服器的要求者（如同所有其他 COM 伺服器），一律會保留此選項，以在其處理常式中執行的每個 COM 方法上授權其用戶端。</span><span class="sxs-lookup"><span data-stu-id="60b1a-127">A requester acting as a COM server, like all other COM servers, always retains the option to authorize its clients on every COM method implemented in its process.</span></span>

    <span data-ttu-id="60b1a-128">請注意，根據預設，VSS 所執行的內部 COM 回呼會受到保護。</span><span class="sxs-lookup"><span data-stu-id="60b1a-128">Note that internal COM callbacks implemented by VSS are secured by default.</span></span>

    <span data-ttu-id="60b1a-129">若要允許所有進程對要求者進行 COM 存取，您可以傳遞 **Null** 安全描述項作為 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)的第一個參數。</span><span class="sxs-lookup"><span data-stu-id="60b1a-129">To allow all processes COM access to a requester, you can pass a **NULL** security descriptor as the first parameter of [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="60b1a-130"> (請注意， **CoInitializeSecurity** 必須針對整個進程呼叫最多一次。</span><span class="sxs-lookup"><span data-stu-id="60b1a-130">(Note that **CoInitializeSecurity** must be called at most once for the entire process.</span></span> <span data-ttu-id="60b1a-131">如需 **CoInitializeSecurity** 呼叫的詳細資訊，請參閱 COM 檔或 MSDN。 ) </span><span class="sxs-lookup"><span data-stu-id="60b1a-131">Please see the COM documentation or MSDN for more information on **CoInitializeSecurity** calls.)</span></span>

    <span data-ttu-id="60b1a-132">下列程式碼範例顯示要求者如何在 Windows 8 和 Windows Server 2012 和更新版本中呼叫 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) ，以便與適用于遠端檔案共用的 VSS 相容 (RVSS) ：</span><span class="sxs-lookup"><span data-stu-id="60b1a-132">The following code example shows how a requester should call [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) in Windows 8 and Windows Server 2012 and later, in order to be compatible with VSS for remote file shares (RVSS):</span></span>

    ``` syntax
    // Initialize COM security.
       hr = CoInitializeSecurity(
            NULL,                          //  PSECURITY_DESCRIPTOR         pSecDesc,
            -1,                            //  LONG                         cAuthSvc,
            NULL,                          //  SOLE_AUTHENTICATION_SERVICE *asAuthSvc,
            NULL,                          //  void                        *pReserved1,
            RPC_C_AUTHN_LEVEL_PKT_PRIVACY, //  DWORD                        dwAuthnLevel,
            RPC_C_IMP_LEVEL_IMPERSONATE,   //  DWORD                        dwImpLevel,
            NULL,                          //  void                        *pAuthList,
            EOAC_STATIC,                   //  DWORD                        dwCapabilities,
            NULL                           //  void                        *pReserved3
            );
    ```

    <span data-ttu-id="60b1a-133">使用 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)明確設定要求者的 COM 層級安全性時，您應該執行下列作業：</span><span class="sxs-lookup"><span data-stu-id="60b1a-133">When explicitly setting a requester's COM level security with [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), you should do the following:</span></span>

    -   <span data-ttu-id="60b1a-134">將驗證等級設定為至少 **RPC \_ C \_ 驗證 \_ level \_ PKT \_ 完整性**。</span><span class="sxs-lookup"><span data-stu-id="60b1a-134">Set the authentication level to at least **RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY**.</span></span> <span data-ttu-id="60b1a-135">為了獲得更好的安全性，請考慮使用 **RPC \_ C \_ 驗證 \_ LEVEL \_ PKT \_ 隱私權**。</span><span class="sxs-lookup"><span data-stu-id="60b1a-135">For better security, consider using **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span>
    -   <span data-ttu-id="60b1a-136">將模擬層級設定為 **RPC \_ C \_ IMP \_ 層級 \_** 模擬。</span><span class="sxs-lookup"><span data-stu-id="60b1a-136">Set the impersonation level to **RPC\_C\_IMP\_LEVEL\_IMPERSONATE**.</span></span>
    -   <span data-ttu-id="60b1a-137">設定 **EOAC \_ 靜態** 的掩蓋安全性功能。</span><span class="sxs-lookup"><span data-stu-id="60b1a-137">Set the cloaking security capabilities to **EOAC\_STATIC**.</span></span> <span data-ttu-id="60b1a-138">如需有關掩蔽安全性的詳細資訊，請參閱「 [掩蔽](../com/cloaking.md)」。</span><span class="sxs-lookup"><span data-stu-id="60b1a-138">For more information about cloaking security, see [Cloaking](../com/cloaking.md).</span></span>

    <span data-ttu-id="60b1a-139">下列程式碼範例顯示要求者如何在 Windows 7 和 Windows Server 2008 R2 和更早版本的 (或 Windows 8 和 Windows Server 2012 和更新版本中呼叫 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) ，) 不需要 RVSS 相容性：</span><span class="sxs-lookup"><span data-stu-id="60b1a-139">The following code example shows how a requester should call [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) in Windows 7 and Windows Server 2008 R2 and earlier (or in Windows 8 and Windows Server 2012 and later, if RVSS compatibility is not needed):</span></span>

    ``` syntax
    // Initialize COM security.
       hr = CoInitializeSecurity(
            NULL,                          //  PSECURITY_DESCRIPTOR         pSecDesc,
            -1,                            //  LONG                         cAuthSvc,
            NULL,                          //  SOLE_AUTHENTICATION_SERVICE *asAuthSvc,
            NULL,                          //  void                        *pReserved1,
            RPC_C_AUTHN_LEVEL_PKT_PRIVACY, //  DWORD                        dwAuthnLevel,
            RPC_C_IMP_LEVEL_IDENTIFY,      //  DWORD                        dwImpLevel,
            NULL,                          //  void                        *pAuthList,
            EOAC_NONE,                     //  DWORD                        dwCapabilities,
            NULL                           //  void                        *pReserved3
            );
    ```

    <span data-ttu-id="60b1a-140">使用 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)明確設定要求者的 COM 層級安全性時，您應該執行下列作業：</span><span class="sxs-lookup"><span data-stu-id="60b1a-140">When explicitly setting a requester's COM level security with [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), you should do the following:</span></span>

    -   <span data-ttu-id="60b1a-141">將驗證等級設定為至少 **RPC \_ C \_ 驗證 \_ level \_ CONNECT**。</span><span class="sxs-lookup"><span data-stu-id="60b1a-141">Set the authentication level to at least **RPC\_C\_AUTHN\_LEVEL\_CONNECT**.</span></span> <span data-ttu-id="60b1a-142">為了獲得更好的安全性，請考慮使用 **RPC \_ C \_ 驗證 \_ LEVEL \_ PKT \_ 隱私權**。</span><span class="sxs-lookup"><span data-stu-id="60b1a-142">For better security, consider using **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span>
    -   <span data-ttu-id="60b1a-143">將模擬層級設定為 **RPC \_ C \_ IMP \_ level \_ 識別** ，除非要求者進程需要針對與 VSS 無關的特定 RPC 或 COM 呼叫，允許模擬。</span><span class="sxs-lookup"><span data-stu-id="60b1a-143">Set the impersonation level to **RPC\_C\_IMP\_LEVEL\_IDENTIFY** unless the requester process needs to allow impersonation for specific RPC or COM calls that are unrelated to VSS.</span></span>

-   <span data-ttu-id="60b1a-144">僅允許指定的進程存取要求者進程。</span><span class="sxs-lookup"><span data-stu-id="60b1a-144">Allow only specified processes access to call into the requester process.</span></span>

    <span data-ttu-id="60b1a-145">COM 伺服器 (例如要求者) ，其會使用非 **Null** 的安全描述項來呼叫 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) ，因為第一個參數可以使用描述項，將本身設定為僅接受屬於特定帳戶集的使用者的撥入電話。</span><span class="sxs-lookup"><span data-stu-id="60b1a-145">A COM server (such as a requester) that is calling [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) with a non-**NULL** security descriptor as the first parameter can use the descriptor to configure itself to accept incoming calls only from users that belong to a specific set of accounts.</span></span>

    <span data-ttu-id="60b1a-146">要求者必須確定在有效使用者下執行的 COM 用戶端已獲授權可呼叫其進程。</span><span class="sxs-lookup"><span data-stu-id="60b1a-146">A requester must ensure that COM clients running under valid users are authorized to call into its process.</span></span> <span data-ttu-id="60b1a-147">在第一個參數中指定安全描述項的要求者，必須允許下列使用者對要求者進程執行撥入電話：</span><span class="sxs-lookup"><span data-stu-id="60b1a-147">A requester that specifies a Security Descriptor in the first parameter must allow the following users to perform incoming calls into the requester process:</span></span>

    -   <span data-ttu-id="60b1a-148">[本機系統]</span><span class="sxs-lookup"><span data-stu-id="60b1a-148">Local System</span></span>
    -   <span data-ttu-id="60b1a-149">本機服務</span><span class="sxs-lookup"><span data-stu-id="60b1a-149">Local Service</span></span>

        <span data-ttu-id="60b1a-150">**WINDOWS XP：** 在 Windows Server 2003 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="60b1a-150">**Windows XP:** This value is not supported until Windows Server 2003.</span></span>

    -   <span data-ttu-id="60b1a-151">網路服務</span><span class="sxs-lookup"><span data-stu-id="60b1a-151">Network Service</span></span>

        <span data-ttu-id="60b1a-152">**WINDOWS XP：** 在 Windows Server 2003 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="60b1a-152">**Windows XP:** This value is not supported until Windows Server 2003.</span></span>

    -   <span data-ttu-id="60b1a-153">本機 Administrators 群組的成員</span><span class="sxs-lookup"><span data-stu-id="60b1a-153">Members of the local Administrators group</span></span>
    -   <span data-ttu-id="60b1a-154">本機備份操作員群組的成員</span><span class="sxs-lookup"><span data-stu-id="60b1a-154">Members of the local Backup Operators group</span></span>
    -   <span data-ttu-id="60b1a-155">在下列登錄位置中指定的特殊使用者，以 "1" 作為其 REG \_ DWORD 值</span><span class="sxs-lookup"><span data-stu-id="60b1a-155">Special users that are specified in the registry location below, with "1" as their REG\_DWORD value</span></span>

## <a name="explicitly-controlling-user-account-access-to-a-requester"></a><span data-ttu-id="60b1a-156">明確控制要求者的使用者帳戶存取權</span><span class="sxs-lookup"><span data-stu-id="60b1a-156">Explicitly Controlling User Account Access to a Requester</span></span>

<span data-ttu-id="60b1a-157">在某些情況下，會將要求者的存取許可權制為以本機系統或本機系統管理員或本機備份操作員群組執行的進程，可能太過嚴格。</span><span class="sxs-lookup"><span data-stu-id="60b1a-157">There are cases where restricting access to a requester to processes running as Local System, or under the local Administrators or local Backup Operators groups, may be too restrictive.</span></span>

<span data-ttu-id="60b1a-158">例如，指定的要求者進程通常不需要在系統管理員或備份操作員帳戶下執行。</span><span class="sxs-lookup"><span data-stu-id="60b1a-158">For example, a specified requester process might not ordinarily need to be run under an Administrator or Backup Operator account.</span></span> <span data-ttu-id="60b1a-159">基於安全性理由，最好不要以人為方式升級處理常式許可權以支援 VSS。</span><span class="sxs-lookup"><span data-stu-id="60b1a-159">For security reasons, it would be best not to artificially promote the processes privileges to support VSS.</span></span>

<span data-ttu-id="60b1a-160">在這些情況下，必須修改 **HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ **VSS** \\ **VssAccessControl** 登錄機碼，以指示 vss 指定的使用者可以安全地執行 vss 要求者。</span><span class="sxs-lookup"><span data-stu-id="60b1a-160">In these cases, the **HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**VSS**\\**VssAccessControl** registry key must be modified to instruct VSS that a specified user is safe to run a VSS requester.</span></span>

<span data-ttu-id="60b1a-161">在此機碼下，您必須建立與要授與或拒絕存取的帳戶名稱相同的子機碼。</span><span class="sxs-lookup"><span data-stu-id="60b1a-161">Under this key, you must create a subkey that has the same name as the account that is to be granted or denied access.</span></span> <span data-ttu-id="60b1a-162">此子機碼必須設定為下表中的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="60b1a-162">This subkey must be set to one of the values in the following table.</span></span>

| <span data-ttu-id="60b1a-163">值</span><span class="sxs-lookup"><span data-stu-id="60b1a-163">Value</span></span> | <span data-ttu-id="60b1a-164">意義</span><span class="sxs-lookup"><span data-stu-id="60b1a-164">Meaning</span></span>                                             |
|-------|-----------------------------------------------------|
| <span data-ttu-id="60b1a-165">0</span><span class="sxs-lookup"><span data-stu-id="60b1a-165">0</span></span>     | <span data-ttu-id="60b1a-166">拒絕使用者存取您的寫入器和要求者。</span><span class="sxs-lookup"><span data-stu-id="60b1a-166">Deny the user access to your writer and requester.</span></span>  |
| <span data-ttu-id="60b1a-167">1</span><span class="sxs-lookup"><span data-stu-id="60b1a-167">1</span></span>     | <span data-ttu-id="60b1a-168">授與使用者存取您的寫入器。</span><span class="sxs-lookup"><span data-stu-id="60b1a-168">Grant the user access to your writer.</span></span>               |
| <span data-ttu-id="60b1a-169">2</span><span class="sxs-lookup"><span data-stu-id="60b1a-169">2</span></span>     | <span data-ttu-id="60b1a-170">授與使用者對您要求者的存取權。</span><span class="sxs-lookup"><span data-stu-id="60b1a-170">Grant the user access to your requester.</span></span>            |
| <span data-ttu-id="60b1a-171">3</span><span class="sxs-lookup"><span data-stu-id="60b1a-171">3</span></span>     | <span data-ttu-id="60b1a-172">將您的寫入器和要求者的存取權授與使用者。</span><span class="sxs-lookup"><span data-stu-id="60b1a-172">Grant the user access to your writer and requester.</span></span> |



 

<span data-ttu-id="60b1a-173">下列範例會授與 "MyDomain \\ >myuser" 帳戶的存取權：</span><span class="sxs-lookup"><span data-stu-id="60b1a-173">The following example grants access to the "MyDomain\\MyUser" account:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            VSS
               VssAccessControl
                  MyDomain\MyUser = 2<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

<span data-ttu-id="60b1a-174">這種機制也可以用來明確地限制其他允許的使用者執行 VSS 要求者。</span><span class="sxs-lookup"><span data-stu-id="60b1a-174">This mechanism can also be used to explicitly restrict an otherwise permitted user from running a VSS requester.</span></span> <span data-ttu-id="60b1a-175">下列範例會限制來自 "ThatDomain \\ Administrator" 帳戶的存取：</span><span class="sxs-lookup"><span data-stu-id="60b1a-175">The following example will restrict access from the "ThatDomain\\Administrator" account:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            VSS
               VssAccessControl
                  ThatDomain\Administrator = 0<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

<span data-ttu-id="60b1a-176">使用者 ThatDomain \\ 系統管理員無法執行 VSS 要求者。</span><span class="sxs-lookup"><span data-stu-id="60b1a-176">The user ThatDomain\\Administrator would not be able to run a VSS requester.</span></span>

## <a name="performing-a-file-backup-of-the-system-state"></a><span data-ttu-id="60b1a-177">執行系統狀態的檔案備份</span><span class="sxs-lookup"><span data-stu-id="60b1a-177">Performing a File Backup of the System State</span></span>

<span data-ttu-id="60b1a-178">如果要求者藉由備份個別檔案來執行系統狀態備份，而不是使用磁片區映射進行備份，則必須呼叫 [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) 和 [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) 函式來列舉位於下列目錄之檔案的永久連結：</span><span class="sxs-lookup"><span data-stu-id="60b1a-178">If a requester performs system-state backup by backing up individual files instead of using a volume image for the backup, it must call the [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) and [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) functions to enumerate hard links on files that are located in the following directories:</span></span>

-   <span data-ttu-id="60b1a-179">Windows \\ system32 \\ WDI \\ perftrack</span><span class="sxs-lookup"><span data-stu-id="60b1a-179">Windows\\system32\\WDI\\perftrack</span></span>\\
-   <span data-ttu-id="60b1a-180">Windows \\ WINSXS</span><span class="sxs-lookup"><span data-stu-id="60b1a-180">Windows\\WINSXS</span></span>\\

<span data-ttu-id="60b1a-181">這些目錄只能由 Administrators 群組的成員存取。</span><span class="sxs-lookup"><span data-stu-id="60b1a-181">These directories can only be accessed by members of the Administrators group.</span></span> <span data-ttu-id="60b1a-182">基於這個理由，這類要求者必須在系統帳戶下執行，或是以 Administrators 群組成員的使用者帳戶執行。</span><span class="sxs-lookup"><span data-stu-id="60b1a-182">For this reason, such a requester must run under the system account or a user account that is a member of the Administrators group.</span></span>

<span data-ttu-id="60b1a-183">**WINDOWS XP 和 Windows Server 2003：** 在 Windows Vista 和 Windows Server 2008 之前，不支援 [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) 和 [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) 函數。</span><span class="sxs-lookup"><span data-stu-id="60b1a-183">**Windows XP and Windows Server 2003:** The [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) and [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) functions are not supported until Windows Vista and Windows Server 2008.</span></span>

 

 

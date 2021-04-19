---
description: VSS 基礎結構需要寫入器進程才能同時作為 COM 用戶端和伺服器。
ms.assetid: 59bb7a86-e874-45ce-abd6-cafd18802c4d
title: 寫入器的安全性考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea6f88243adbd62d928170a86ed57b91cbebe134
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980973"
---
# <a name="security-considerations-for-writers"></a><span data-ttu-id="470e6-103">寫入器的安全性考慮</span><span class="sxs-lookup"><span data-stu-id="470e6-103">Security Considerations for Writers</span></span>

<span data-ttu-id="470e6-104">VSS 基礎結構需要寫入器進程才能同時作為 COM 用戶端和伺服器。</span><span class="sxs-lookup"><span data-stu-id="470e6-104">The VSS infrastructure requires writer processes to be able to function both as COM clients and as servers.</span></span>

<span data-ttu-id="470e6-105">以伺服器的身分執行時，VSS 寫入器會公開 COM 介面 (例如， [**CVssWriter：： OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) 這類 vss 事件處理常式會) 並接收來自 vss 進程的傳入 com 呼叫 (例如要求者和 vss 服務) 或來自 vss 外部進程的 RPC 呼叫，通常是在這些進程產生 vss 事件時 (例如，當要求者呼叫 [**>ivssbackupcomponents：： GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)) 時。</span><span class="sxs-lookup"><span data-stu-id="470e6-105">When acting as servers, VSS writers expose COM interfaces (for example, the VSS event handlers such as [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)) and receive incoming COM calls from VSS processes (such as requesters and the VSS service) or RPC calls from processes that are external to VSS, typically when these processes generate VSS events (for example, when a requester calls [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)).</span></span> <span data-ttu-id="470e6-106">因此，VSS 寫入器需要安全地管理哪些 COM 用戶端能夠讓傳入的 COM 呼叫進入其進程。</span><span class="sxs-lookup"><span data-stu-id="470e6-106">Therefore, a VSS writer needs to securely manage which COM clients are able to make incoming COM calls into its process.</span></span>

<span data-ttu-id="470e6-107">同樣地，VSS 寫入器也可以做為 COM 用戶端，對 VSS 基礎結構所提供的回呼發出傳出的 COM 呼叫，或對 VSS 外部的進程發出 RPC 呼叫。</span><span class="sxs-lookup"><span data-stu-id="470e6-107">Similarly, VSS writers may also act as COM clients, making outgoing COM calls to callbacks supplied by the VSS infrastructure or RPC calls to processes that are external to VSS.</span></span> <span data-ttu-id="470e6-108">這些回呼是由備份應用程式或 VSS 服務所提供，可讓寫入器執行工作，例如透過 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 介面更新備份元件檔。</span><span class="sxs-lookup"><span data-stu-id="470e6-108">These callbacks that are provided either by a backup application or by the VSS service allow the writer to perform tasks such as updating the Backup Components Document through the [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) interface.</span></span> <span data-ttu-id="470e6-109">因此，VSS 安全性設定必須允許寫入器對其他 VSS 進程發出傳出的 COM 呼叫。</span><span class="sxs-lookup"><span data-stu-id="470e6-109">Therefore, VSS security settings must allow writers to make outgoing COM calls into other VSS processes.</span></span>

<span data-ttu-id="470e6-110">管理寫入器安全性問題最簡單的機制，就是適當選取執行它的使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="470e6-110">The simplest mechanism for managing writer security issues involves the proper selection of the user account under which it runs.</span></span> <span data-ttu-id="470e6-111">寫入器通常需要以 Administrators 群組或 Backup Operators 群組成員的使用者身分執行，或者必須以本機系統帳戶的身分執行。</span><span class="sxs-lookup"><span data-stu-id="470e6-111">A writer typically needs to run under a user who is a member of either the Administrators group or the Backup Operators group, or it needs to run as the Local System account.</span></span>

<span data-ttu-id="470e6-112">根據預設，當寫入器作為 COM 用戶端時，如果它不是在這些帳戶下執行，則它所做的任何 COM 呼叫都會自動被 **E \_ ACCESSDENIED** 拒絕，而不會取得 COM 方法的執行。</span><span class="sxs-lookup"><span data-stu-id="470e6-112">By default, when a writer is acting as a COM client, if it does not run under these accounts, any COM call it makes is automatically rejected with **E\_ACCESSDENIED** without even getting to the COM method implementation.</span></span>

## <a name="disabling-com-exception-handling"></a><span data-ttu-id="470e6-113">停用 COM 例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="470e6-113">Disabling COM Exception Handling</span></span>

<span data-ttu-id="470e6-114">開發寫入器時，請將 [COM COMGLB \_ 例外狀況 \_ 沒有 \_ 處理全域選項] 旗標設定為停用 com 例外狀況處理。</span><span class="sxs-lookup"><span data-stu-id="470e6-114">When developing a writer, set the COM COMGLB\_EXCEPTION\_DONOT\_HANDLE global options flag to disable COM exception handling.</span></span> <span data-ttu-id="470e6-115">請務必這麼做，因為 COM 例外狀況處理可以遮罩 VSS 應用程式中的嚴重錯誤。</span><span class="sxs-lookup"><span data-stu-id="470e6-115">It is important to do this because COM exception handling can mask fatal errors in a VSS application.</span></span> <span data-ttu-id="470e6-116">遮罩的錯誤可能會讓進程處於不穩定且無法預測的狀態，而導致損毀和停止回應。</span><span class="sxs-lookup"><span data-stu-id="470e6-116">The error that is masked can leave the process in an unstable and unpredictable state, which can lead to corruptions and hangs.</span></span> <span data-ttu-id="470e6-117">如需此旗標的詳細資訊，請參閱 [IGlobalOptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions)。</span><span class="sxs-lookup"><span data-stu-id="470e6-117">For more information about this flag, see [IGlobalOptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).</span></span>

## <a name="setting-writer-default-com-access-check-permission"></a><span data-ttu-id="470e6-118">設定寫入器預設 COM 存取檢查許可權</span><span class="sxs-lookup"><span data-stu-id="470e6-118">Setting Writer Default COM Access Check Permission</span></span>

<span data-ttu-id="470e6-119">撰寫者必須注意，當其進程作為伺服器時 (例如，為了處理) 的 VSS 事件，它們必須允許來自其他 VSS 參與者的連入呼叫，例如要求者或 VSS 服務。</span><span class="sxs-lookup"><span data-stu-id="470e6-119">Writers need to be aware that when their processes act as a server (for example, to handle VSS events), they must allow incoming calls from other VSS participants, such as requesters or the VSS service.</span></span>

<span data-ttu-id="470e6-120">不過，根據預設，處理常式只會允許在相同登入會話下執行的 COM 用戶端，) 或在本機系統帳戶下執行。</span><span class="sxs-lookup"><span data-stu-id="470e6-120">However, by default, a process will allow only COM clients that are running under the same logon session the SELF SID) or running under the Local System account.</span></span> <span data-ttu-id="470e6-121">這是潛在的問題，因為這些預設值不足以支援 VSS 基礎結構。</span><span class="sxs-lookup"><span data-stu-id="470e6-121">This is a potential problem because these defaults are not sufficient to support the VSS infrastructure.</span></span> <span data-ttu-id="470e6-122">例如，要求者可能會以「備份操作員」使用者帳戶執行，該帳戶不在與寫入器程式相同的登入會話中，也不是本機系統帳戶。</span><span class="sxs-lookup"><span data-stu-id="470e6-122">For example, requesters may run as a "Backup Operator" user account that is neither in the same logon session as the writer process nor a Local System account.</span></span>

<span data-ttu-id="470e6-123">為了處理這種類型的問題，每個 COM 伺服器進程都可以進一步控制 RPC 或 COM 用戶端是否能夠在此情況) 下，使用 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) 來設定整個進程的預設 com 存取檢查許可權，以進一步控制是否允許 RPC 或 com 用戶端執行 COM (方法。</span><span class="sxs-lookup"><span data-stu-id="470e6-123">To handle this type of problem, every COM server process can exercise further control over whether an RPC or COM client is allowed to perform a COM method the server (a writer in this case) implements by using [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) to set a process-wide default COM access check permission.</span></span>

<span data-ttu-id="470e6-124">寫入器可以明確地執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="470e6-124">Writers can explicitly do the following:</span></span>

-   <span data-ttu-id="470e6-125">允許所有進程存取寫入器進程。</span><span class="sxs-lookup"><span data-stu-id="470e6-125">Allow all processes access to call into the writer process.</span></span>

    <span data-ttu-id="470e6-126">此選項可能適用于許多寫入器，而其他 COM 伺服器會使用此選項，例如，所有以 SVCHOST 為基礎的 Windows 服務都已使用此選項，預設為所有 COM + 服務。</span><span class="sxs-lookup"><span data-stu-id="470e6-126">This option may be adequate for many writers, and is used by other COM servers—for example, all SVCHOST-based Windows services are already using this option, as are all COM+ Services by default.</span></span>

    <span data-ttu-id="470e6-127">允許所有進程執行傳入的 COM 呼叫不一定是安全性弱點。</span><span class="sxs-lookup"><span data-stu-id="470e6-127">Allowing all processes to perform incoming COM calls is not necessarily a security weakness.</span></span> <span data-ttu-id="470e6-128">作為 COM 伺服器的寫入器，就像所有其他 COM 伺服器一樣，一律會保留在其處理常式中所執行的每個 COM 方法上授權其用戶端的選項。</span><span class="sxs-lookup"><span data-stu-id="470e6-128">A writer acting as a COM server, like all other COM servers, always retains the option of authorizing its clients on every COM method implemented in its process.</span></span>

    <span data-ttu-id="470e6-129">若要允許所有進程對寫入器進行 COM 存取，您可以傳遞 **Null** 安全描述項作為 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)的第一個參數。</span><span class="sxs-lookup"><span data-stu-id="470e6-129">To allow all processes COM access to a writer, you can pass a **NULL** security descriptor as the first parameter of [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="470e6-130"> (請注意， **CoInitializeSecurity** 必須針對整個進程呼叫最多一次。</span><span class="sxs-lookup"><span data-stu-id="470e6-130">(Note that **CoInitializeSecurity** must be called at most once for the entire process.</span></span> <span data-ttu-id="470e6-131">如需 **CoInitializeSecurity** 的詳細資訊，請參閱 COM 檔。 ) </span><span class="sxs-lookup"><span data-stu-id="470e6-131">Please see the COM documentation for more details on **CoInitializeSecurity**.)</span></span>

    <span data-ttu-id="470e6-132">下列程式碼範例包含對 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)的呼叫：</span><span class="sxs-lookup"><span data-stu-id="470e6-132">The following is a code example that includes a call to [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity):</span></span>

    ``` syntax
    // Initialize COM security.
    hr = CoInitializeSecurity(
           NULL,                          // PSECURITY_DESCRIPTOR          pSecDesc,
           -1,                            // LONG                          cAuthSvc,
           NULL,                          // SOLE_AUTHENTICATION_SERVICE  *asAuthSvc,
           NULL,                          // void                         *pReserved1,
           RPC_C_AUTHN_LEVEL_PKT_PRIVACY, // DWORD                         dwAuthnLevel,
           RPC_C_IMP_LEVEL_IDENTIFY,      // DWORD                         dwImpLevel,
           NULL,                          // void                         *pAuthList,
           EOAC_NONE,                     // DWORD                         dwCapabilities,
           NULL                           // void                         *pReserved3
        );
    ```

    <span data-ttu-id="470e6-133">使用 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)明確設定寫入器的 COM 層級安全性時，您應該執行下列作業：</span><span class="sxs-lookup"><span data-stu-id="470e6-133">When explicitly setting a writer's COM-level security with [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), you should do the following:</span></span>

    -   <span data-ttu-id="470e6-134">將驗證等級設定為至少 **RPC \_ C \_ 驗證 \_ level \_ CONNECT**。</span><span class="sxs-lookup"><span data-stu-id="470e6-134">Set the authentication level to at least **RPC\_C\_AUTHN\_LEVEL\_CONNECT**.</span></span>

        <span data-ttu-id="470e6-135">為了獲得更好的安全性，請考慮使用 **RPC \_ C \_ 驗證 \_ LEVEL \_ PKT \_ 隱私權**。</span><span class="sxs-lookup"><span data-stu-id="470e6-135">For better security, consider using **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span>

    -   <span data-ttu-id="470e6-136">除非寫入器進程需要針對與 VSS 不相關的特定 RPC 或 COM 呼叫，才能進行模擬，否則請將模擬層級設定為 **RPC \_ C \_ IMP \_ 等級 \_ 識別** 。</span><span class="sxs-lookup"><span data-stu-id="470e6-136">Set the impersonation level to **RPC\_C\_IMP\_LEVEL\_IDENTIFY** unless the writer process needs to allow impersonation for specific RPC or COM calls that are unrelated to VSS.</span></span>

-   <span data-ttu-id="470e6-137">只允許指定的進程存取寫入器進程。</span><span class="sxs-lookup"><span data-stu-id="470e6-137">Allow only specified processes access to call into the writer process.</span></span>

    <span data-ttu-id="470e6-138">COM 伺服器 (例如，使用非 **Null** 安全描述項呼叫 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)的寫入器) 可以使用描述項，將本身設定為僅接受屬於特定帳戶集的使用者的來電。</span><span class="sxs-lookup"><span data-stu-id="470e6-138">A COM server (such as a writer) that is calling [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) with a non-**NULL** security descriptor can use the descriptor to configure itself to accept incoming calls only from users that belong to a specific set of accounts.</span></span>

    <span data-ttu-id="470e6-139">寫入器必須確保在有效使用者下執行的 COM 用戶端獲得授權可呼叫其進程。</span><span class="sxs-lookup"><span data-stu-id="470e6-139">A writer must ensure that COM clients running under valid users are authorized to call into its process.</span></span> <span data-ttu-id="470e6-140">在第一個參數中指定安全描述項的寫入器必須允許下列使用者對要求者進程執行撥入電話：</span><span class="sxs-lookup"><span data-stu-id="470e6-140">A writer that specifies a Security Descriptor in the first parameter must allow the following users to perform incoming calls into the requester process:</span></span>

    -   <span data-ttu-id="470e6-141">[本機系統]</span><span class="sxs-lookup"><span data-stu-id="470e6-141">Local System</span></span>
    -   <span data-ttu-id="470e6-142">本機 Administrators 群組的成員</span><span class="sxs-lookup"><span data-stu-id="470e6-142">Members of the local Administrators group</span></span>
    -   <span data-ttu-id="470e6-143">本機備份操作員群組的成員</span><span class="sxs-lookup"><span data-stu-id="470e6-143">Members of the local Backup Operators group</span></span>
    -   <span data-ttu-id="470e6-144">寫入器執行時所用的帳戶</span><span class="sxs-lookup"><span data-stu-id="470e6-144">The account under which the writer is running</span></span>

## <a name="explicitly-controlling-user-account-access-to-a-writer"></a><span data-ttu-id="470e6-145">明確控制寫入器的使用者帳戶存取權</span><span class="sxs-lookup"><span data-stu-id="470e6-145">Explicitly Controlling User Account Access to a Writer</span></span>

<span data-ttu-id="470e6-146">在某些情況下，將寫入器的存取許可權制為以本機系統或本機系統管理員或本機備份操作員本機群組執行的程式，可能會太嚴格。</span><span class="sxs-lookup"><span data-stu-id="470e6-146">There are cases where restricting access to a writer to processes running as Local System, or under the local Administrators or local Backup Operators local groups, may be too restrictive.</span></span>

<span data-ttu-id="470e6-147">例如，可能不需要在系統管理員或備份操作員帳戶下執行寫入程式 (可能是協力廠商的非系統寫入器) 。</span><span class="sxs-lookup"><span data-stu-id="470e6-147">For example, a writer process (perhaps a third-party non-system writer) might not ordinarily need to be run under an Administrator or Backup Operator account.</span></span> <span data-ttu-id="470e6-148">基於安全性理由，最好不要以人為方式升級進程的許可權以支援 VSS。</span><span class="sxs-lookup"><span data-stu-id="470e6-148">For security reasons, it would be best not to artificially promote the process's privileges to support VSS.</span></span>

<span data-ttu-id="470e6-149">在這些情況下，必須修改 **HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ **VSS** \\ **VssAccessControl** 登錄機碼，以指示 VSS 指定的使用者可以安全地執行 vss 寫入器。</span><span class="sxs-lookup"><span data-stu-id="470e6-149">In these cases, the **HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**VSS**\\**VssAccessControl** registry key must be modified to instruct VSS that a specified user is safe to run a VSS writer.</span></span>

<span data-ttu-id="470e6-150">在此機碼下，您必須建立與要授與或拒絕存取的帳戶名稱相同的子機碼。</span><span class="sxs-lookup"><span data-stu-id="470e6-150">Under this key, you must create a subkey that has the same name as the account that is to be granted or denied access.</span></span> <span data-ttu-id="470e6-151">此子機碼必須設定為下表中的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="470e6-151">This subkey must be set to one of the values in the following table.</span></span>

| <span data-ttu-id="470e6-152">值</span><span class="sxs-lookup"><span data-stu-id="470e6-152">Value</span></span> | <span data-ttu-id="470e6-153">意義</span><span class="sxs-lookup"><span data-stu-id="470e6-153">Meaning</span></span>                                             |
|-------|-----------------------------------------------------|
| <span data-ttu-id="470e6-154">0</span><span class="sxs-lookup"><span data-stu-id="470e6-154">0</span></span>     | <span data-ttu-id="470e6-155">拒絕使用者存取您的寫入器和要求者。</span><span class="sxs-lookup"><span data-stu-id="470e6-155">Deny the user access to your writer and requester.</span></span>  |
| <span data-ttu-id="470e6-156">1</span><span class="sxs-lookup"><span data-stu-id="470e6-156">1</span></span>     | <span data-ttu-id="470e6-157">授與使用者存取您的寫入器。</span><span class="sxs-lookup"><span data-stu-id="470e6-157">Grant the user access to your writer.</span></span>               |
| <span data-ttu-id="470e6-158">2</span><span class="sxs-lookup"><span data-stu-id="470e6-158">2</span></span>     | <span data-ttu-id="470e6-159">授與使用者對您要求者的存取權。</span><span class="sxs-lookup"><span data-stu-id="470e6-159">Grant the user access to your requester.</span></span>            |
| <span data-ttu-id="470e6-160">3</span><span class="sxs-lookup"><span data-stu-id="470e6-160">3</span></span>     | <span data-ttu-id="470e6-161">將您的寫入器和要求者的存取權授與使用者。</span><span class="sxs-lookup"><span data-stu-id="470e6-161">Grant the user access to your writer and requester.</span></span> |



 

<span data-ttu-id="470e6-162">下列範例會授與 "MyDomain \\ >myuser" 帳戶的存取權：</span><span class="sxs-lookup"><span data-stu-id="470e6-162">The following example grants access to the "MyDomain\\MyUser" account:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            VSS
               VssAccessControl
                  MyDomain\MyUser = 1<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

<span data-ttu-id="470e6-163">這種機制也可以用來明確地限制允許的使用者執行 VSS 寫入器。</span><span class="sxs-lookup"><span data-stu-id="470e6-163">This mechanism can also be used to explicitly restrict an otherwise permitted user from running a VSS writer.</span></span> <span data-ttu-id="470e6-164">下列範例會限制來自 "ThatDomain \\ Administrator" 帳戶的存取：</span><span class="sxs-lookup"><span data-stu-id="470e6-164">The following example will restrict access from the "ThatDomain\\Administrator" account:</span></span>

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

<span data-ttu-id="470e6-165">使用者 ThatDomain \\ 系統管理員無法執行 VSS 寫入器。</span><span class="sxs-lookup"><span data-stu-id="470e6-165">The user ThatDomain\\Administrator would not be able to run a VSS writer.</span></span>

 

 

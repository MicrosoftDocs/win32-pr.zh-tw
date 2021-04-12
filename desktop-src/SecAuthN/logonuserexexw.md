---
description: LogonUserExExW 函式會嘗試將使用者登入本機電腦。
ms.assetid: d90db4c6-a711-4519-8b91-5069cee07738
title: 'LogonUserExExW 函式 (Winbasep) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LogonUserExExW
api_type:
- DllExport
api_location:
- Advapi32.dll
ms.openlocfilehash: 35ec65e7899f45a5222ae12b08992e77ea67f306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027253"
---
# <a name="logonuserexexw-function"></a><span data-ttu-id="4c880-103">LogonUserExExW 函式</span><span class="sxs-lookup"><span data-stu-id="4c880-103">LogonUserExExW function</span></span>

<span data-ttu-id="4c880-104">**LogonUserExExW** 函式會嘗試將使用者登入本機電腦。</span><span class="sxs-lookup"><span data-stu-id="4c880-104">The **LogonUserExExW** function attempts to log a user on to the local computer.</span></span> <span data-ttu-id="4c880-105">本機電腦是用來呼叫 **LogonUserExExW** 的電腦。</span><span class="sxs-lookup"><span data-stu-id="4c880-105">The local computer is the computer from which **LogonUserExExW** was called.</span></span> <span data-ttu-id="4c880-106">您無法使用 **LogonUserExExW** 來登入遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="4c880-106">You cannot use **LogonUserExExW** to log on to a remote computer.</span></span> <span data-ttu-id="4c880-107">使用使用者名稱和網域來指定使用者，並使用純文字密碼來 [*驗證*](../secgloss/a-gly.md) 使用者。</span><span class="sxs-lookup"><span data-stu-id="4c880-107">Specify the user by using a user name and domain and [*authenticate*](../secgloss/a-gly.md) the user by using a plaintext password.</span></span> <span data-ttu-id="4c880-108">如果函式成功，則會接收代表已登入使用者之權杖的控制碼。</span><span class="sxs-lookup"><span data-stu-id="4c880-108">If the function succeeds, it receives a handle to a token that represents the logged-on user.</span></span> <span data-ttu-id="4c880-109">然後，您可以使用這個權杖控制碼來模擬指定的使用者，或在大部分情況下，建立在指定使用者的內容中執行的 [*處理*](../secgloss/p-gly.md) 程式。</span><span class="sxs-lookup"><span data-stu-id="4c880-109">You can then use this token handle to impersonate the specified user or, in most cases, to create a [*process*](../secgloss/p-gly.md) that runs in the context of the specified user.</span></span>

<span data-ttu-id="4c880-110">此函式類似于 [**LogonUserEx**](/windows/desktop/api/Winbase/nf-winbase-logonuserexa) 函式，不同之處在于它會採用額外的參數 *pTokenGroups*，也就是在登入成功時，新增至傳回給呼叫者的權杖中的一或多個 [*安全性識別碼*](../secgloss/s-gly.md) (sid) 。</span><span class="sxs-lookup"><span data-stu-id="4c880-110">This function is similar to the [**LogonUserEx**](/windows/desktop/api/Winbase/nf-winbase-logonuserexa) function, except that it takes the additional parameter, *pTokenGroups*, which is a set of one or more [*security identifiers*](../secgloss/s-gly.md) (SIDs) that are added to the token returned to the caller when the logon is successful.</span></span>

<span data-ttu-id="4c880-111">此函式未在公用標頭中宣告，且沒有相關聯的匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="4c880-111">This function is not declared in a public header and has no associated import library.</span></span> <span data-ttu-id="4c880-112">您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Advapi32.dll。</span><span class="sxs-lookup"><span data-stu-id="4c880-112">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Advapi32.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c880-113">語法</span><span class="sxs-lookup"><span data-stu-id="4c880-113">Syntax</span></span>


```C++
BOOL WINAPI LogonUserExExW(
  _In_      LPTSTR        lpszUsername,
  _In_opt_  LPTSTR        lpszDomain,
  _In_opt_  LPTSTR        lpszPassword,
  _In_      DWORD         dwLogonType,
  _In_      DWORD         dwLogonProvider,
  _In_opt_  PTOKEN_GROUPS pTokenGroups,
  _Out_opt_ PHANDLE       phToken,
  _Out_opt_ PSID          *ppLogonSid,
  _Out_opt_ PVOID         *ppProfileBuffer,
  _Out_opt_ LPDWORD       pdwProfileLength,
  _Out_opt_ PQUOTA_LIMITS pQuotaLimits
);
```



## <a name="parameters"></a><span data-ttu-id="4c880-114">參數</span><span class="sxs-lookup"><span data-stu-id="4c880-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c880-115">*lpszUsername* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4c880-115">*lpszUsername* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c880-116">指定使用者名稱之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="4c880-116">A pointer to a null-terminated string that specifies the name of the user.</span></span> <span data-ttu-id="4c880-117">這是要登入的使用者帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="4c880-117">This is the name of the user account to log on to.</span></span> <span data-ttu-id="4c880-118">如果您使用 (UPN) 格式的 [*使用者主體名稱*](../secgloss/u-gly.md) ，則 *lpszDomain* 參數必須為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4c880-118">If you use the [*user principal name*](../secgloss/u-gly.md) (UPN) format, the *lpszDomain* parameter must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4c880-119">*lpszDomain* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="4c880-119">*lpszDomain* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4c880-120">以 null 結束的字串指標，指定其帳戶資料庫包含 *lpszUsername* 帳戶之網域或伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="4c880-120">A pointer to a null-terminated string that specifies the name of the domain or server whose account database contains the *lpszUsername* account.</span></span> <span data-ttu-id="4c880-121">如果此參數為 **Null**，則必須以 UPN 格式指定使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="4c880-121">If this parameter is **NULL**, the user name must be specified in UPN format.</span></span> <span data-ttu-id="4c880-122">如果此參數為 "."，則此函式只會使用本機帳戶資料庫來驗證帳戶。</span><span class="sxs-lookup"><span data-stu-id="4c880-122">If this parameter is ".", the function validates the account by using only the local account database.</span></span>

</dd> <dt>

<span data-ttu-id="4c880-123">*lpszPassword* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="4c880-123">*lpszPassword* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4c880-124">以 null 結束的字串指標，指定 *lpszUsername* 所指定之使用者帳戶的純文字密碼。</span><span class="sxs-lookup"><span data-stu-id="4c880-124">A pointer to a null-terminated string that specifies the plaintext password for the user account specified by *lpszUsername*.</span></span> <span data-ttu-id="4c880-125">當您使用完密碼之後，請呼叫 [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) 函式來清除記憶體中的密碼。</span><span class="sxs-lookup"><span data-stu-id="4c880-125">When you have finished using the password, clear the password from memory by calling the [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) function.</span></span> <span data-ttu-id="4c880-126">如需保護密碼的詳細資訊，請參閱 [處理密碼](../secbp/handling-passwords.md)。</span><span class="sxs-lookup"><span data-stu-id="4c880-126">For more information about protecting passwords, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="4c880-127">*>dwlogontype* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4c880-127">*dwLogonType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c880-128">要執行的登入作業類型。</span><span class="sxs-lookup"><span data-stu-id="4c880-128">The type of logon operation to perform.</span></span> <span data-ttu-id="4c880-129">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="4c880-129">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="4c880-130">值</span><span class="sxs-lookup"><span data-stu-id="4c880-130">Value</span></span>                                                                                                                                                                                                                                                                        | <span data-ttu-id="4c880-131">意義</span><span class="sxs-lookup"><span data-stu-id="4c880-131">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOGON32_LOGON_INTERACTIVE"></span><span id="logon32_logon_interactive"></span><dl> <span data-ttu-id="4c880-132"><dt>**LOGON32 \_登入 \_ 互動式**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4c880-132"><dt>**LOGON32\_LOGON\_INTERACTIVE**</dt> <dt>2</dt></span></span> </dl>                    | <span data-ttu-id="4c880-133">這種登入類型適用于將以互動方式使用電腦的使用者，例如 [*終端*](../secgloss/t-gly.md) 機伺服器登入的使用者、遠端 shell 或類似的進程。</span><span class="sxs-lookup"><span data-stu-id="4c880-133">This logon type is intended for users who will be interactively using the computer, such as a user being logged on by a [*terminal*](../secgloss/t-gly.md) server, remote shell, or similar process.</span></span> <span data-ttu-id="4c880-134">這種登入類型有額外的費用，可快取已中斷連線作業的登入資訊;因此，它不適合某些用戶端/伺服器應用程式，例如郵件伺服器。</span><span class="sxs-lookup"><span data-stu-id="4c880-134">This logon type has the additional expense of caching logon information for disconnected operations; therefore, it is inappropriate for some client/server applications, such as a mail server.</span></span><br/>                                  |
| <span id="LOGON32_LOGON_NETWORK"></span><span id="logon32_logon_network"></span><dl> <span data-ttu-id="4c880-135"><dt>**LOGON32 \_登入 \_ 網路**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="4c880-135"><dt>**LOGON32\_LOGON\_NETWORK**</dt> <dt>3</dt></span></span> </dl>                                | <span data-ttu-id="4c880-136">此登入類型適用于高效能伺服器來驗證純文字密碼。</span><span class="sxs-lookup"><span data-stu-id="4c880-136">This logon type is intended for high performance servers to authenticate plaintext passwords.</span></span> <span data-ttu-id="4c880-137">**LogonUserExExW** 函數不會快取此登入類型的認證。</span><span class="sxs-lookup"><span data-stu-id="4c880-137">The **LogonUserExExW** function does not cache credentials for this logon type.</span></span><br/>                                                                                                                                                                                                                                                                                                 |
| <span id="LOGON32_LOGON_BATCH"></span><span id="logon32_logon_batch"></span><dl> <span data-ttu-id="4c880-138"><dt>**LOGON32 \_登入 \_ 批次**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="4c880-138"><dt>**LOGON32\_LOGON\_BATCH**</dt> <dt>4</dt></span></span> </dl>                                      | <span data-ttu-id="4c880-139">這種登入類型適用于批次伺服器，在此情況下，進程可能會代表使用者執行，而不需要直接介入。</span><span class="sxs-lookup"><span data-stu-id="4c880-139">This logon type is intended for batch servers, where processes may be executing on behalf of a user without their direct intervention.</span></span> <span data-ttu-id="4c880-140">此類型也適用于較高的效能伺服器，這些伺服器會一次處理許多純文字驗證嘗試，例如郵件或網頁伺服器。</span><span class="sxs-lookup"><span data-stu-id="4c880-140">This type is also for higher performance servers that process many plaintext authentication attempts at a time, such as mail or web servers.</span></span> <span data-ttu-id="4c880-141">**LogonUserExExW** 函數不會快取此登入類型的認證。</span><span class="sxs-lookup"><span data-stu-id="4c880-141">The **LogonUserExExW** function does not cache credentials for this logon type.</span></span><br/>                                                                                                           |
| <span id="LOGON32_LOGON_SERVICE"></span><span id="logon32_logon_service"></span><dl> <span data-ttu-id="4c880-142"><dt>**LOGON32 \_登入 \_ 服務**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="4c880-142"><dt>**LOGON32\_LOGON\_SERVICE**</dt> <dt>5</dt></span></span> </dl>                                | <span data-ttu-id="4c880-143">表示服務類型登入。</span><span class="sxs-lookup"><span data-stu-id="4c880-143">Indicates a service-type logon.</span></span> <span data-ttu-id="4c880-144">提供的帳戶必須啟用服務許可權。</span><span class="sxs-lookup"><span data-stu-id="4c880-144">The account provided must have the service privilege enabled.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="LOGON32_LOGON_UNLOCK"></span><span id="logon32_logon_unlock"></span><dl> <span data-ttu-id="4c880-145"><dt>**LOGON32 \_登入 \_ 解除鎖定**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="4c880-145"><dt>**LOGON32\_LOGON\_UNLOCK**</dt> <dt>7</dt></span></span> </dl>                                   | <span data-ttu-id="4c880-146">這種登入類型適用于登入將會以互動方式使用電腦之使用者的 [*GINA*](../secgloss/g-gly.md) dll。</span><span class="sxs-lookup"><span data-stu-id="4c880-146">This logon type is for [*GINA*](../secgloss/g-gly.md) DLLs that log on users who will be interactively using the computer.</span></span> <span data-ttu-id="4c880-147">此登入類型可以產生唯一的審核記錄，以顯示何時解除鎖定工作站。</span><span class="sxs-lookup"><span data-stu-id="4c880-147">This logon type can generate a unique audit record that shows when the workstation was unlocked.</span></span><br/>                                                                                                                                                                                                                   |
| <span id="LOGON32_LOGON_NETWORK_CLEARTEXT"></span><span id="logon32_logon_network_cleartext"></span><dl> <span data-ttu-id="4c880-148"><dt>**LOGON32 \_登入 \_ 網路 \_ 純**</dt>文本 <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="4c880-148"><dt>**LOGON32\_LOGON\_NETWORK\_CLEARTEXT**</dt> <dt>8</dt></span></span> </dl> | <span data-ttu-id="4c880-149">此登入類型會保留 [*驗證套件*](../secgloss/a-gly.md)中的名稱和密碼，可讓伺服器在模擬用戶端時，與其他網路伺服器進行連線。</span><span class="sxs-lookup"><span data-stu-id="4c880-149">This logon type preserves the name and password in the [*authentication package*](../secgloss/a-gly.md), which allows the server to make connections to other network servers while impersonating the client.</span></span> <span data-ttu-id="4c880-150">伺服器可以接受來自用戶端的純文字認證、呼叫 **LogonUserExExW**、驗證使用者是否可透過網路存取系統，並仍與其他伺服器通訊。</span><span class="sxs-lookup"><span data-stu-id="4c880-150">A server can accept plaintext credentials from a client, call **LogonUserExExW**, verify that the user can access the system across the network, and still communicate with other servers.</span></span> <br/> |
| <span id="LOGON32_LOGON_NEW_CREDENTIALS"></span><span id="logon32_logon_new_credentials"></span><dl> <span data-ttu-id="4c880-151"><dt>**LOGON32 \_登入 \_ 新 \_ 認證**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="4c880-151"><dt>**LOGON32\_LOGON\_NEW\_CREDENTIALS**</dt> <dt>9</dt></span></span> </dl>       | <span data-ttu-id="4c880-152">這種登入類型可讓呼叫者複製其目前的權杖，並為輸出連線指定新的認證。</span><span class="sxs-lookup"><span data-stu-id="4c880-152">This logon type allows the caller to clone its current token and specify new credentials for outbound connections.</span></span> <span data-ttu-id="4c880-153">新的登入會話具有相同的本機識別碼，但是針對其他網路連線使用不同的認證。</span><span class="sxs-lookup"><span data-stu-id="4c880-153">The new logon session has the same local identifier but uses different credentials for other network connections.</span></span><br/> <span data-ttu-id="4c880-154">只有 **LOGON32 \_ 提供者 \_ WINNT50** 登入提供者才支援此登入類型。</span><span class="sxs-lookup"><span data-stu-id="4c880-154">This logon type is supported only by the **LOGON32\_PROVIDER\_WINNT50** logon provider.</span></span><br/>                                                                                                                                       |



 

</dd> <dt>

<span data-ttu-id="4c880-155">*dwLogonProvider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4c880-155">*dwLogonProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c880-156">登入提供者。</span><span class="sxs-lookup"><span data-stu-id="4c880-156">The logon provider.</span></span> <span data-ttu-id="4c880-157">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="4c880-157">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="4c880-158">值</span><span class="sxs-lookup"><span data-stu-id="4c880-158">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="4c880-159">意義</span><span class="sxs-lookup"><span data-stu-id="4c880-159">Meaning</span></span>                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOGON32_PROVIDER_DEFAULT"></span><span id="logon32_provider_default"></span><dl> <span data-ttu-id="4c880-160"><dt>**LOGON32 \_ 提供者 \_ 預設值**</dt></span><span class="sxs-lookup"><span data-stu-id="4c880-160"><dt>**LOGON32\_PROVIDER\_DEFAULT**</dt></span></span> </dl> | <span data-ttu-id="4c880-161">使用系統的標準登入提供者。</span><span class="sxs-lookup"><span data-stu-id="4c880-161">Use the standard logon provider for the system.</span></span> <span data-ttu-id="4c880-162">預設的 [*安全性提供者*](../secgloss/s-gly.md) 是 NTLM。</span><span class="sxs-lookup"><span data-stu-id="4c880-162">The default [*security provider*](../secgloss/s-gly.md) is NTLM.</span></span><br/> |
| <span id="LOGON32_PROVIDER_WINNT50"></span><span id="logon32_provider_winnt50"></span><dl> <span data-ttu-id="4c880-163"><dt>**LOGON32 \_ 提供者 \_ WINNT50**</dt></span><span class="sxs-lookup"><span data-stu-id="4c880-163"><dt>**LOGON32\_PROVIDER\_WINNT50**</dt></span></span> </dl> | <span data-ttu-id="4c880-164">使用 negotiate 登入提供者。</span><span class="sxs-lookup"><span data-stu-id="4c880-164">Use the negotiate logon provider.</span></span> <br/>                                                                                                                                                         |
| <span id="LOGON32_PROVIDER_WINNT40"></span><span id="logon32_provider_winnt40"></span><dl> <span data-ttu-id="4c880-165"><dt>**LOGON32 \_ 提供者 \_ WINNT40**</dt></span><span class="sxs-lookup"><span data-stu-id="4c880-165"><dt>**LOGON32\_PROVIDER\_WINNT40**</dt></span></span> </dl> | <span data-ttu-id="4c880-166">使用 NTLM 登入提供者。</span><span class="sxs-lookup"><span data-stu-id="4c880-166">Use the NTLM logon provider.</span></span><br/>                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="4c880-167">*pTokenGroups* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="4c880-167">*pTokenGroups* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4c880-168">[**權杖 \_ 群組**](/windows/win32/api/winnt/ns-winnt-token_groups)結構的指標，指定新增至權杖的群組 sid 清單，此函式會在登入成功時收到此清單。</span><span class="sxs-lookup"><span data-stu-id="4c880-168">A pointer to a [**TOKEN\_GROUPS**](/windows/win32/api/winnt/ns-winnt-token_groups) structure that specifies a list of group SIDs that are added to the token that this function receives upon successful logon.</span></span> <span data-ttu-id="4c880-169">新增至權杖的任何 Sid 也會影響群組擴充。</span><span class="sxs-lookup"><span data-stu-id="4c880-169">Any SIDs added to the token also effect group expansion.</span></span> <span data-ttu-id="4c880-170">例如，如果新增的 Sid 是本機群組的成員，這些群組也會新增至接收的存取權杖。</span><span class="sxs-lookup"><span data-stu-id="4c880-170">For example, if the added SIDs are members of local groups, those groups are also added to the received access token.</span></span>

<span data-ttu-id="4c880-171">如果這個參數不是 **Null**，則此函式的呼叫者必須授與並啟用 **SE \_ TCB \_ 許可權** 許可權。</span><span class="sxs-lookup"><span data-stu-id="4c880-171">If this parameter is not **NULL**, the caller of this function must have the **SE\_TCB\_PRIVILEGE** privilege granted and enabled.</span></span>

</dd> <dt>

<span data-ttu-id="4c880-172">*phToken* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="4c880-172">*phToken* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4c880-173">控制碼變數的指標，此變數會接收代表指定使用者之 token 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="4c880-173">A pointer to a handle variable that receives a handle to a token that represents the specified user.</span></span>

<span data-ttu-id="4c880-174">您可以在 [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) 函數的呼叫中使用傳回的控制碼。</span><span class="sxs-lookup"><span data-stu-id="4c880-174">You can use the returned handle in calls to the [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) function.</span></span>

<span data-ttu-id="4c880-175">在大部分的情況下，傳回的控制碼是您可以在呼叫 [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)函式時使用的 [*主要權杖*](../secgloss/p-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="4c880-175">In most cases, the returned handle is a [*primary token*](../secgloss/p-gly.md) that you can use in calls to the [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) function.</span></span> <span data-ttu-id="4c880-176">但是，如果您指定 LOGON32 \_ LOGON \_ NETWORK 旗標，除非您呼叫 [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex)將模擬權杖轉換為主要權杖，否則 **LogonUserExExW** 會傳回您無法在 **CreateProcessAsUser** 中使用的模擬 [*權杖*](../secgloss/i-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="4c880-176">However, if you specify the LOGON32\_LOGON\_NETWORK flag, **LogonUserExExW** returns an [*impersonation token*](../secgloss/i-gly.md) that you cannot use in **CreateProcessAsUser** unless you call [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) to convert the impersonation token to a primary token.</span></span>

<span data-ttu-id="4c880-177">當您不再需要這個控制碼時，請呼叫 [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) 函式來關閉它。</span><span class="sxs-lookup"><span data-stu-id="4c880-177">When you no longer need this handle, close it by calling the [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) function.</span></span>

</dd> <dt>

<span data-ttu-id="4c880-178">*ppLogonSid* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="4c880-178">*ppLogonSid* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4c880-179">SID 指標的指標，此 SID 會接收使用者登入的 SID。</span><span class="sxs-lookup"><span data-stu-id="4c880-179">A pointer to a pointer to a SID that receives the SID of the user logged on.</span></span>

<span data-ttu-id="4c880-180">當您使用完 SID 之後，請呼叫 [**>localfree**](/windows/win32/api/winbase/nf-winbase-localfree) 函式來釋放它。</span><span class="sxs-lookup"><span data-stu-id="4c880-180">When you have finished using the SID, free it by calling the [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) function.</span></span>

</dd> <dt>

<span data-ttu-id="4c880-181">*ppProfileBuffer* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="4c880-181">*ppProfileBuffer* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4c880-182">指標的指標，該指標會接收包含已登入使用者之設定檔的緩衝區位址。</span><span class="sxs-lookup"><span data-stu-id="4c880-182">A pointer to a pointer that receives the address of a buffer that contains the logged on user's profile.</span></span>

</dd> <dt>

<span data-ttu-id="4c880-183">*pdwProfileLength* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="4c880-183">*pdwProfileLength* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4c880-184">接收配置檔案緩衝區長度之 **DWORD** 的指標。</span><span class="sxs-lookup"><span data-stu-id="4c880-184">A pointer to a **DWORD** that receives the length of the profile buffer.</span></span>

</dd> <dt>

<span data-ttu-id="4c880-185">*pQuotaLimits* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="4c880-185">*pQuotaLimits* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4c880-186">[**配額 \_ 限制**](/windows/desktop/api/Winnt/ns-winnt-quota_limits)結構的指標，此結構會接收已登入使用者之配額的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4c880-186">A pointer to a [**QUOTA\_LIMITS**](/windows/desktop/api/Winnt/ns-winnt-quota_limits) structure that receives information about the quotas for the logged on user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c880-187">傳回值</span><span class="sxs-lookup"><span data-stu-id="4c880-187">Return value</span></span>

<span data-ttu-id="4c880-188">如果函式成功，函數會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="4c880-188">If the function succeeds, the function returns nonzero.</span></span>

<span data-ttu-id="4c880-189">如果函式失敗，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="4c880-189">If the function fails, it returns zero.</span></span> <span data-ttu-id="4c880-190">若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="4c880-190">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="4c880-191">備註</span><span class="sxs-lookup"><span data-stu-id="4c880-191">Remarks</span></span>

<span data-ttu-id="4c880-192">**LOGON32 \_ logon \_ NETWORK** 登入類型是最快的，但有下列限制：</span><span class="sxs-lookup"><span data-stu-id="4c880-192">The **LOGON32\_LOGON\_NETWORK** logon type is fastest, but it has the following limitations:</span></span>

-   <span data-ttu-id="4c880-193">函數會傳回模擬 [*權杖*](../secgloss/i-gly.md)，而不是主要權杖。</span><span class="sxs-lookup"><span data-stu-id="4c880-193">The function returns an [*impersonation token*](../secgloss/i-gly.md), not a primary token.</span></span> <span data-ttu-id="4c880-194">您無法直接在 [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) 函式中使用此 token。</span><span class="sxs-lookup"><span data-stu-id="4c880-194">You cannot use this token directly in the [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) function.</span></span> <span data-ttu-id="4c880-195">不過，您可以呼叫 [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) 函式，將權杖轉換為主要權杖，然後在 **CreateProcessAsUser** 中使用它。</span><span class="sxs-lookup"><span data-stu-id="4c880-195">However, you can call the [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) function to convert the token to a primary token, and then use it in **CreateProcessAsUser**.</span></span>
-   <span data-ttu-id="4c880-196">如果您將權杖轉換為主要權杖，並在 [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) 中使用它來啟動處理常式，則新的進程無法透過重新導向器存取其他網路資源，例如遠端伺服器或印表機。</span><span class="sxs-lookup"><span data-stu-id="4c880-196">If you convert the token to a primary token and use it in [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) to start a process, the new process cannot access other network resources, such as remote servers or printers, through the redirector.</span></span> <span data-ttu-id="4c880-197">例外狀況是，如果網路資源不受存取控制，則新的進程將可以存取它。</span><span class="sxs-lookup"><span data-stu-id="4c880-197">An exception is that if the network resource is not access controlled, then the new process will be able to access it.</span></span>

<span data-ttu-id="4c880-198">*LpszUsername* 所指定的帳號必須具有必要的帳戶許可權。</span><span class="sxs-lookup"><span data-stu-id="4c880-198">The account specified by *lpszUsername* must have the necessary account rights.</span></span> <span data-ttu-id="4c880-199">例如，若要使用 **LOGON32 \_ 登入 \_ 互動式** 旗標登入使用者，使用者 (或使用者所屬的群組) 必須有「 **SE \_ 互動式 \_ 登錄 \_ 名稱** 」帳戶許可權。</span><span class="sxs-lookup"><span data-stu-id="4c880-199">For example, to log on a user with the **LOGON32\_LOGON\_INTERACTIVE** flag, the user (or a group to which the user belongs) must have the **SE\_INTERACTIVE\_LOGON\_NAME** account right.</span></span> <span data-ttu-id="4c880-200">如需影響各種登入作業的帳戶許可權清單，請參閱 [帳戶物件存取權限](../secmgmt/account-object-access-rights.md)。</span><span class="sxs-lookup"><span data-stu-id="4c880-200">For a list of the account rights that affect the various logon operations, see [Account Object Access Rights](../secmgmt/account-object-access-rights.md).</span></span>

<span data-ttu-id="4c880-201">如果至少有一個權杖存在，則會將使用者視為已登入。</span><span class="sxs-lookup"><span data-stu-id="4c880-201">A user is considered logged on if at least one token exists.</span></span> <span data-ttu-id="4c880-202">如果您呼叫 [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) ，然後關閉權杖，使用者仍會登入，直到處理程式 (和所有子進程) 結束為止。</span><span class="sxs-lookup"><span data-stu-id="4c880-202">If you call [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) and then close the token, the user is still logged on until the process (and all child processes) have ended.</span></span>

<span data-ttu-id="4c880-203">如果提供了選擇性的 *pTokenGroups* 參數，LSA 將不會自動新增本機 SID 或登入 SID。</span><span class="sxs-lookup"><span data-stu-id="4c880-203">If the optional *pTokenGroups* parameter is supplied, LSA will not add either the local SID or the logon SID automatically.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c880-204">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c880-204">Requirements</span></span>



| <span data-ttu-id="4c880-205">需求</span><span class="sxs-lookup"><span data-stu-id="4c880-205">Requirement</span></span> | <span data-ttu-id="4c880-206">值</span><span class="sxs-lookup"><span data-stu-id="4c880-206">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c880-207">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4c880-207">Minimum supported client</span></span><br/> | <span data-ttu-id="4c880-208">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c880-208">Windows Vista \[desktop apps only\]</span></span><br/>                                                                        |
| <span data-ttu-id="4c880-209">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4c880-209">Minimum supported server</span></span><br/> | <span data-ttu-id="4c880-210">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c880-210">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="4c880-211">版本</span><span class="sxs-lookup"><span data-stu-id="4c880-211">Version</span></span><br/>                  | <span data-ttu-id="4c880-212">LogonUserExExW 也提供于 windows Server 2003 或 Windows XPwith 一般發行版本。</span><span class="sxs-lookup"><span data-stu-id="4c880-212">LogonUserExExW is also available onWindows Server 2003 or Windows XPwith the General Distribution Release.</span></span><br/> |
| <span data-ttu-id="4c880-213">標頭</span><span class="sxs-lookup"><span data-stu-id="4c880-213">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c880-214"><dt>Winbasep。h</dt></span><span class="sxs-lookup"><span data-stu-id="4c880-214"><dt>Winbasep.h</dt></span></span> </dl>                                 |
| <span data-ttu-id="4c880-215">DLL</span><span class="sxs-lookup"><span data-stu-id="4c880-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c880-216"><dt>Advapi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c880-216"><dt>Advapi32.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="4c880-217">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c880-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c880-218">用戶端/伺服器存取控制</span><span class="sxs-lookup"><span data-stu-id="4c880-218">Client/Server Access Control</span></span>](../secauthz/client-server-access-control.md)
</dt> <dt>

[<span data-ttu-id="4c880-219">用戶端/伺服器存取控制功能</span><span class="sxs-lookup"><span data-stu-id="4c880-219">Client/Server Access Control Functions</span></span>](../secauthz/authorization-functions.md)
</dt> <dt>

[<span data-ttu-id="4c880-220">**CloseHandle**</span><span class="sxs-lookup"><span data-stu-id="4c880-220">**CloseHandle**</span></span>](/windows/win32/api/handleapi/nf-handleapi-closehandle)
</dt> <dt>

[<span data-ttu-id="4c880-221">**CreateProcessAsUser**</span><span class="sxs-lookup"><span data-stu-id="4c880-221">**CreateProcessAsUser**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)
</dt> <dt>

[<span data-ttu-id="4c880-222">**DuplicateTokenEx**</span><span class="sxs-lookup"><span data-stu-id="4c880-222">**DuplicateTokenEx**</span></span>](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex)
</dt> <dt>

[<span data-ttu-id="4c880-223">**ImpersonateLoggedOnUser**</span><span class="sxs-lookup"><span data-stu-id="4c880-223">**ImpersonateLoggedOnUser**</span></span>](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser)
</dt> <dt>

[<span data-ttu-id="4c880-224">**LogonUserEx**</span><span class="sxs-lookup"><span data-stu-id="4c880-224">**LogonUserEx**</span></span>](/windows/desktop/api/Winbase/nf-winbase-logonuserexa)
</dt> <dt>

[<span data-ttu-id="4c880-225">**配額 \_ 限制**</span><span class="sxs-lookup"><span data-stu-id="4c880-225">**QUOTA\_LIMITS**</span></span>](/windows/desktop/api/Winnt/ns-winnt-quota_limits)
</dt> </dl>

 

 

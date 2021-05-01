---
Description: 許可權會決定使用者帳戶可以執行的系統作業類型。 系統管理員將許可權指派給使用者和群組帳戶。 每個使用者的許可權包含授與使用者的許可權，以及使用者所屬的群組。
ms.assetid: 973796a6-bc2e-4e64-92db-5e17b9c25460
title: " (Winnt. h) 的許可權常數"
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: cd33cf947f6425d717b4d41524fe7cf0fed14cef
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327153"
---
# <a name="privilege-constants-authorization"></a><span data-ttu-id="fa27d-105">許可權常數 (授權) </span><span class="sxs-lookup"><span data-stu-id="fa27d-105">Privilege Constants (Authorization)</span></span>

<span data-ttu-id="fa27d-106">許可權會決定使用者帳戶可以執行的系統作業類型。</span><span class="sxs-lookup"><span data-stu-id="fa27d-106">Privileges determine the type of system operations that a user account can perform.</span></span> <span data-ttu-id="fa27d-107">系統管理員將許可權指派給使用者和群組帳戶。</span><span class="sxs-lookup"><span data-stu-id="fa27d-107">An administrator assigns privileges to user and group accounts.</span></span> <span data-ttu-id="fa27d-108">每個使用者的許可權包含授與使用者的許可權，以及使用者所屬的群組。</span><span class="sxs-lookup"><span data-stu-id="fa27d-108">Each user's privileges include those granted to the user and to the groups to which the user belongs.</span></span>

<span data-ttu-id="fa27d-109">取得和調整 [*存取權杖*](/windows/desktop/SecGloss/a-gly) 中之許可權的函式會使用 [*本機唯一識別碼*](/windows/desktop/SecGloss/l-gly) (LUID) 類型來識別許可權。</span><span class="sxs-lookup"><span data-stu-id="fa27d-109">The functions that get and adjust the privileges in an [*access token*](/windows/desktop/SecGloss/a-gly) use the [*locally unique identifier*](/windows/desktop/SecGloss/l-gly) (LUID) type to identify privileges.</span></span> <span data-ttu-id="fa27d-110">您可以使用 [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) 函數來判斷本機系統上對應到許可權常數的 [**LUID**](/windows/desktop/api/Winnt/ns-winnt-luid) 。</span><span class="sxs-lookup"><span data-stu-id="fa27d-110">Use the [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) function to determine the [**LUID**](/windows/desktop/api/Winnt/ns-winnt-luid) on the local system that corresponds to a privilege constant.</span></span> <span data-ttu-id="fa27d-111">您可以使用 [**LookupPrivilegeName**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegenamea) 函式，將 **LUID** 轉換為其對應的字串常數。</span><span class="sxs-lookup"><span data-stu-id="fa27d-111">Use the [**LookupPrivilegeName**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegenamea) function to convert a **LUID** to its corresponding string constant.</span></span>

<span data-ttu-id="fa27d-112">作業系統表示許可權，方法是使用下表的 [描述] 資料行中「使用者權限」之後的字串。</span><span class="sxs-lookup"><span data-stu-id="fa27d-112">The operating system represents a privilege by using the string that follows "User Right" in the Description column of the following table.</span></span> <span data-ttu-id="fa27d-113">作業系統會在 [本機安全性設定] Microsoft Management Console (MMC) 嵌入式管理單元中，于 [**使用者權限指派**] 節點的 [**原則**] 欄中顯示使用者右邊的字串。</span><span class="sxs-lookup"><span data-stu-id="fa27d-113">The operating system displays the user right strings in the **Policy** column of the **User Rights Assignment** node of the Local Security Settings Microsoft Management Console (MMC) snap-in.</span></span>

## <a name="example"></a><span data-ttu-id="fa27d-114">範例</span><span class="sxs-lookup"><span data-stu-id="fa27d-114">Example</span></span>

```cpp
BOOL EnablePrivilege()
{
    LUID PrivilegeRequired ;
    BOOL bRes = FALSE;
  
    bRes = LookupPrivilegeValue(NULL, SE_DEBUG_NAME, &PrivilegeRequired);

    // ...

    return bRes;
}
```
<span data-ttu-id="fa27d-115">從 GitHub 上的 [Windows 傳統範例](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/ManagementInfrastructure/cpp/Process/Provider/WindowsProcess.c) 取得的範例。</span><span class="sxs-lookup"><span data-stu-id="fa27d-115">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/ManagementInfrastructure/cpp/Process/Provider/WindowsProcess.c) on GitHub.</span></span>

## <a name="constants"></a><span data-ttu-id="fa27d-116">常數</span><span class="sxs-lookup"><span data-stu-id="fa27d-116">Constants</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="fa27d-117">常數/值</span><span class="sxs-lookup"><span data-stu-id="fa27d-117">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="fa27d-118">Description</span><span class="sxs-lookup"><span data-stu-id="fa27d-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="SE_ASSIGNPRIMARYTOKEN_NAME"></span><span id="se_assignprimarytoken_name"></span><dl> <span data-ttu-id="fa27d-119"><dt><strong>SE_ASSIGNPRIMARYTOKEN_NAME</strong></dt> <dt>文字 (&quot; SeAssignPrimaryTokenPrivilege &quot;) </dt> </span><span class="sxs-lookup"><span data-stu-id="fa27d-119"><dt><strong>SE_ASSIGNPRIMARYTOKEN_NAME</strong></dt> <dt>TEXT(&quot;SeAssignPrimaryTokenPrivilege&quot;)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa27d-120">指派進程 <a href="/windows/desktop/SecGloss/p-gly"><em>主要權杖</em></a> 的必要項。</span><span class="sxs-lookup"><span data-stu-id="fa27d-120">Required to assign the <a href="/windows/desktop/SecGloss/p-gly"><em>primary token</em></a> of a process.</span></span> <br/> <span data-ttu-id="fa27d-121">使用者權限：取代進程層級的 token。</span><span class="sxs-lookup"><span data-stu-id="fa27d-121">User Right: Replace a process-level token.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_AUDIT_NAME"></span><span id="se_audit_name"></span><dl> <span data-ttu-id="fa27d-122"><dt><strong>SE_AUDIT_NAME</strong></dt> <dt>文字 (&quot; SeAuditPrivilege &quot;) </dt> </span><span class="sxs-lookup"><span data-stu-id="fa27d-122"><dt><strong>SE_AUDIT_NAME</strong></dt> <dt>TEXT(&quot;SeAuditPrivilege&quot;)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa27d-123">產生 audit 記錄檔專案的必要專案。</span><span class="sxs-lookup"><span data-stu-id="fa27d-123">Required to generate audit-log entries.</span></span> <span data-ttu-id="fa27d-124">授與此許可權以保護伺服器。</span><span class="sxs-lookup"><span data-stu-id="fa27d-124">Give this privilege to secure servers.</span></span> <br/> <span data-ttu-id="fa27d-125">使用者權限：產生安全性審核。</span><span class="sxs-lookup"><span data-stu-id="fa27d-125">User Right: Generate security audits.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_BACKUP_NAME"></span><span id="se_backup_name"></span><dl> <span data-ttu-id="fa27d-126"><dt><strong>SE_BACKUP_NAME</strong></dt> <dt>文字 (&quot; SeBackupPrivilege &quot;) </dt> </span><span class="sxs-lookup"><span data-stu-id="fa27d-126"><dt><strong>SE_BACKUP_NAME</strong></dt> <dt>TEXT(&quot;SeBackupPrivilege&quot;)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa27d-127">執行備份作業所需。</span><span class="sxs-lookup"><span data-stu-id="fa27d-127">Required to perform backup operations.</span></span> <span data-ttu-id="fa27d-128">此許可權可讓系統將所有讀取存取控制授與任何檔案，而不論 (ACL) 為檔案指定的 <a href="/windows/desktop/SecGloss/a-gly"><em>存取控制清單</em></a> 。</span><span class="sxs-lookup"><span data-stu-id="fa27d-128">This privilege causes the system to grant all read access control to any file, regardless of the <a href="/windows/desktop/SecGloss/a-gly"><em>access control list</em></a> (ACL) specified for the file.</span></span> <span data-ttu-id="fa27d-129">除了讀取以外的任何存取要求仍會以 ACL 進行評估。</span><span class="sxs-lookup"><span data-stu-id="fa27d-129">Any access request other than read is still evaluated with the ACL.</span></span> <span data-ttu-id="fa27d-130"><a href="/windows/desktop/api/winreg/nf-winreg-regsavekeya"><strong>RegSaveKey</strong></a>和<a href="/windows/desktop/api/winreg/nf-winreg-regsavekeyexa"><strong>RegSaveKeyEx</strong></a>函數需要此許可權。</span><span class="sxs-lookup"><span data-stu-id="fa27d-130">This privilege is required by the <a href="/windows/desktop/api/winreg/nf-winreg-regsavekeya"><strong>RegSaveKey</strong></a> and <a href="/windows/desktop/api/winreg/nf-winreg-regsavekeyexa"><strong>RegSaveKeyEx</strong></a>functions.</span></span> <span data-ttu-id="fa27d-131">如果保留此許可權，則會授與下列存取權限：</span><span class="sxs-lookup"><span data-stu-id="fa27d-131">The following access rights are granted if this privilege is held:</span></span><br/>
<ul>
<li><span data-ttu-id="fa27d-132">READ_CONTROL</span><span class="sxs-lookup"><span data-stu-id="fa27d-132">READ_CONTROL</span></span></li>
<li><span data-ttu-id="fa27d-133">ACCESS_SYSTEM_SECURITY</span><span class="sxs-lookup"><span data-stu-id="fa27d-133">ACCESS_SYSTEM_SECURITY</span></span></li>
<li><span data-ttu-id="fa27d-134">FILE_GENERIC_READ</span><span class="sxs-lookup"><span data-stu-id="fa27d-134">FILE_GENERIC_READ</span></span></li>
<li><span data-ttu-id="fa27d-135">FILE_TRAVERSE</span><span class="sxs-lookup"><span data-stu-id="fa27d-135">FILE_TRAVERSE</span></span></li>
</ul>
<span data-ttu-id="fa27d-136">使用者權限：備份檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="fa27d-136">User Right: Back up files and directories.</span></span><br/><span data-ttu-id="fa27d-137">如果檔案位於卸載式磁片磁碟機上，且已啟用「Audit 卸除式存放裝置」，則 SE_SECURITY_NAME 必須有 ACCESS_SYSTEM_SECURITY。</span><span class="sxs-lookup"><span data-stu-id="fa27d-137">If the file is located on a removable drive and the "Audit Removable Storage" is enabled, the SE_SECURITY_NAME is required to have ACCESS_SYSTEM_SECURITY.</span></span></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_CHANGE_NOTIFY_NAME"></span><span id="se_change_notify_name"></span><dl> <span data-ttu-id="fa27d-138"><dt><strong>SE_CHANGE_NOTIFY_NAME</strong></dt> <dt>文字 (&quot; SeChangeNotifyPrivilege &quot;) </dt> </span><span class="sxs-lookup"><span data-stu-id="fa27d-138"><dt><strong>SE_CHANGE_NOTIFY_NAME</strong></dt> <dt>TEXT(&quot;SeChangeNotifyPrivilege&quot;)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa27d-139">需要接收檔案或目錄變更的通知。</span><span class="sxs-lookup"><span data-stu-id="fa27d-139">Required to receive notifications of changes to files or directories.</span></span> <span data-ttu-id="fa27d-140">此許可權也會導致系統略過所有的遍歷存取檢查。</span><span class="sxs-lookup"><span data-stu-id="fa27d-140">This privilege also causes the system to skip all traversal access checks.</span></span> <span data-ttu-id="fa27d-141">預設會針對所有使用者啟用。</span><span class="sxs-lookup"><span data-stu-id="fa27d-141">It is enabled by default for all users.</span></span> <br/> <span data-ttu-id="fa27d-142">使用者權限：略過遍歷檢查。</span><span class="sxs-lookup"><span data-stu-id="fa27d-142">User Right: Bypass traverse checking.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_CREATE_GLOBAL_NAME"></span><span id="se_create_global_name"></span><dl> <span data-ttu-id="fa27d-143"><dt><strong>SE_CREATE_GLOBAL_NAME</strong></dt> <dt>文字 (&quot; SeCreateGlobalPrivilege &quot;) </dt> </span><span class="sxs-lookup"><span data-stu-id="fa27d-143"><dt><strong>SE_CREATE_GLOBAL_NAME</strong></dt> <dt>TEXT(&quot;SeCreateGlobalPrivilege&quot;)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa27d-144">在終端機服務會話期間，必須在全域命名空間中建立指名的檔案對應物件。</span><span class="sxs-lookup"><span data-stu-id="fa27d-144">Required to create named file mapping objects in the global namespace during Terminal Services sessions.</span></span> <span data-ttu-id="fa27d-145">系統管理員、服務和本機系統帳戶預設會啟用此許可權。</span><span class="sxs-lookup"><span data-stu-id="fa27d-145">This privilege is enabled by default for administrators, services, and the local system account.</span></span><br/> <span data-ttu-id="fa27d-146">使用者權限：建立全域物件。</span><span class="sxs-lookup"><span data-stu-id="fa27d-146">User Right: Create global objects.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_CREATE_PAGEFILE_NAME"></span><span id="se_create_pagefile_name"></span><dl> <span data-ttu-id="fa27d-147"><dt><strong>SE_CREATE_PAGEFILE_NAME</strong></dt> <dt>文字 (&quot; SeCreatePagefilePrivilege &quot;) </dt> </span><span class="sxs-lookup"><span data-stu-id="fa27d-147"><dt><strong>SE_CREATE_PAGEFILE_NAME</strong></dt> <dt>TEXT(&quot;SeCreatePagefilePrivilege&quot;)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa27d-148">建立分頁檔案所需。</span><span class="sxs-lookup"><span data-stu-id="fa27d-148">Required to create a paging file.</span></span> <br/> <span data-ttu-id="fa27d-149">使用者權限：建立分頁檔。</span><span class="sxs-lookup"><span data-stu-id="fa27d-149">User Right: Create a pagefile.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_CREATE_PERMANENT_NAME"></span><span id="se_create_permanent_name"></span><dl> <span data-ttu-id="fa27d-150"><dt><strong>SE_CREATE_PERMANENT_NAME</strong></dt> <dt>文字 (&quot; SeCreatePermanentPrivilege &quot;) </dt> </span><span class="sxs-lookup"><span data-stu-id="fa27d-150"><dt><strong>SE_CREATE_PERMANENT_NAME</strong></dt> <dt>TEXT(&quot;SeCreatePermanentPrivilege&quot;)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa27d-151">建立永久物件時所需。</span><span class="sxs-lookup"><span data-stu-id="fa27d-151">Required to create a permanent object.</span></span> <br/> <span data-ttu-id="fa27d-152">使用者權限：建立永久共用物件。</span><span class="sxs-lookup"><span data-stu-id="fa27d-152">User Right: Create permanent shared objects.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_CREATE_SYMBOLIC_LINK_NAME"></span><span id="se_create_symbolic_link_name"></span><dl> <span data-ttu-id="fa27d-153"><dt><strong>SE_CREATE_SYMBOLIC_LINK_NAME</strong></dt> <dt>文字 (&quot; SeCreateSymbolicLinkPrivilege &quot;) </dt> </span><span class="sxs-lookup"><span data-stu-id="fa27d-153"><dt><strong>SE_CREATE_SYMBOLIC_LINK_NAME</strong></dt> <dt>TEXT(&quot;SeCreateSymbolicLinkPrivilege&quot;)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa27d-154">建立符號連結所需。</span><span class="sxs-lookup"><span data-stu-id="fa27d-154">Required to create a symbolic link.</span></span><br/> <span data-ttu-id="fa27d-155">使用者權限：建立符號連結。</span><span class="sxs-lookup"><span data-stu-id="fa27d-155">User Right: Create symbolic links.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_CREATE_TOKEN_NAME"></span><span id="se_create_token_name"></span><dl> <span data-ttu-id="fa27d-156"><dt><strong>SE_CREATE_TOKEN_NAME</strong></dt> <dt>文字 (&quot; SeCreateTokenPrivilege &quot;) </dt> </span><span class="sxs-lookup"><span data-stu-id="fa27d-156"><dt><strong>SE_CREATE_TOKEN_NAME</strong></dt> <dt>TEXT(&quot;SeCreateTokenPrivilege&quot;)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa27d-157">建立主要權杖所需。</span><span class="sxs-lookup"><span data-stu-id="fa27d-157">Required to create a primary token.</span></span> <br/> <span data-ttu-id="fa27d-158">使用者權限：建立 token 物件。</span><span class="sxs-lookup"><span data-stu-id="fa27d-158">User Right: Create a token object.</span></span><br/> <span data-ttu-id="fa27d-159">您無法使用 [ &quot; 建立權杖物件原則] 將此許可權新增至使用者帳戶 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="fa27d-159">You cannot add this privilege to a user account with the &quot;Create a token object&quot; policy.</span></span> <span data-ttu-id="fa27d-160">此外，您無法使用 Windows Api 將此許可權新增至擁有的進程。<strong>Windows Server 2003 和 WINDOWS XP （含 SP1）及更早版本：</strong> Windows Api 可以將此許可權新增至擁有的進程。</span><span class="sxs-lookup"><span data-stu-id="fa27d-160">Additionally, you cannot add this privilege to an owned process using Windows APIs.<strong>Windows Server 2003 and Windows XP with SP1 and earlier:</strong> Windows APIs can add this privilege to an owned process.</span></span><br/> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_DEBUG_NAME"></span><span id="se_debug_name"></span><dl> <span data-ttu-id="fa27d-161"><dt><strong>SE_DEBUG_NAME</strong></dt> <dt>文字 (&quot; SeDebugPrivilege &quot;) </dt> </span><span class="sxs-lookup"><span data-stu-id="fa27d-161"><dt><strong>SE_DEBUG_NAME</strong></dt> <dt>TEXT(&quot;SeDebugPrivilege&quot;)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa27d-162">需要對其他帳戶所擁有之進程的記憶體進行 debug 和調整。</span><span class="sxs-lookup"><span data-stu-id="fa27d-162">Required to debug and adjust the memory of a process owned by another account.</span></span> <br/> <span data-ttu-id="fa27d-163">使用者權限：偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="fa27d-163">User Right: Debug programs.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_DELEGATE_SESSION_USER_IMPERSONATE_NAME"></span><span id="se_delegate_session_user_impersonate_name"></span><dl> <span data-ttu-id="fa27d-164"><dt><strong>SE_DELEGATE_SESSION_USER_IMPERSONATE_NAME</strong></dt> <dt>文字 (&quot; SeDelegateSessionUserImpersonatePrivilege &quot;) </dt> </span><span class="sxs-lookup"><span data-stu-id="fa27d-164"><dt><strong>SE_DELEGATE_SESSION_USER_IMPERSONATE_NAME</strong></dt> <dt>TEXT(&quot;SeDelegateSessionUserImpersonatePrivilege&quot;)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa27d-165">需要在相同的會話中取得其他使用者的模擬權杖。</span><span class="sxs-lookup"><span data-stu-id="fa27d-165">Required to obtain an impersonation token for another user in the same session.</span></span> <br/> <span data-ttu-id="fa27d-166">使用者權限：模擬其他使用者。</span><span class="sxs-lookup"><span data-stu-id="fa27d-166">User Right: Impersonate other users.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_ENABLE_DELEGATION_NAME"></span><span id="se_enable_delegation_name"></span><dl> <span data-ttu-id="fa27d-167"><dt><strong>SE_ENABLE_DELEGATION_NAME</strong></dt> <dt>文字 (&quot; SeEnableDelegationPrivilege &quot;) </dt> </span><span class="sxs-lookup"><span data-stu-id="fa27d-167"><dt><strong>SE_ENABLE_DELEGATION_NAME</strong></dt> <dt>TEXT(&quot;SeEnableDelegationPrivilege&quot;)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa27d-168">將使用者和電腦帳戶標示為受信任以進行委派時，需要此參數。</span><span class="sxs-lookup"><span data-stu-id="fa27d-168">Required to mark user and computer accounts as trusted for delegation.</span></span><br/> <span data-ttu-id="fa27d-169">使用者權限：啟用受信任的電腦和使用者帳戶以進行委派。</span><span class="sxs-lookup"><span data-stu-id="fa27d-169">User Right: Enable computer and user accounts to be trusted for delegation.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_IMPERSONATE_NAME"></span><span id="se_impersonate_name"></span><dl> <span data-ttu-id="fa27d-170"><dt><strong>SE_IMPERSONATE_NAME</strong></dt> <dt>文字 (&quot; SeImpersonatePrivilege &quot;) </dt> </span><span class="sxs-lookup"><span data-stu-id="fa27d-170"><dt><strong>SE_IMPERSONATE_NAME</strong></dt> <dt>TEXT(&quot;SeImpersonatePrivilege&quot;)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa27d-171">需要模擬。</span><span class="sxs-lookup"><span data-stu-id="fa27d-171">Required to impersonate.</span></span><br/> <span data-ttu-id="fa27d-172">使用者權限：在驗證之後模擬用戶端。</span><span class="sxs-lookup"><span data-stu-id="fa27d-172">User Right: Impersonate a client after authentication.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_INC_BASE_PRIORITY_NAME"></span><span id="se_inc_base_priority_name"></span><dl> <span data-ttu-id="fa27d-173"><dt><strong>SE_INC_BASE_PRIORITY_NAME</strong></dt> <dt>文字 (&quot; SeIncreaseBasePriorityPrivilege &quot;) </dt> </span><span class="sxs-lookup"><span data-stu-id="fa27d-173"><dt><strong>SE_INC_BASE_PRIORITY_NAME</strong></dt> <dt>TEXT(&quot;SeIncreaseBasePriorityPrivilege&quot;)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa27d-174">需要提高進程的基本優先權。</span><span class="sxs-lookup"><span data-stu-id="fa27d-174">Required to increase the base priority of a process.</span></span> <br/> <span data-ttu-id="fa27d-175">使用者權限：提高排程優先權。</span><span class="sxs-lookup"><span data-stu-id="fa27d-175">User Right: Increase scheduling priority.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_INCREASE_QUOTA_NAME"></span><span id="se_increase_quota_name"></span><dl> <span data-ttu-id="fa27d-176"><dt><strong>SE_INCREASE_QUOTA_NAME</strong></dt> <dt>文字 (&quot; SeIncreaseQuotaPrivilege &quot;) </dt> </span><span class="sxs-lookup"><span data-stu-id="fa27d-176"><dt><strong>SE_INCREASE_QUOTA_NAME</strong></dt> <dt>TEXT(&quot;SeIncreaseQuotaPrivilege&quot;)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa27d-177">需要增加指派給處理常式的配額。</span><span class="sxs-lookup"><span data-stu-id="fa27d-177">Required to increase the quota assigned to a process.</span></span> <br/> <span data-ttu-id="fa27d-178">使用者權限：調整進程的記憶體配額。</span><span class="sxs-lookup"><span data-stu-id="fa27d-178">User Right: Adjust memory quotas for a process.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_INC_WORKING_SET_NAME"></span><span id="se_inc_working_set_name"></span><dl> <span data-ttu-id="fa27d-179"><dt><strong>SE_INC_WORKING_SET_NAME</strong></dt> <dt>文字 (&quot; SeIncreaseWorkingSetPrivilege &quot;) </dt> </span><span class="sxs-lookup"><span data-stu-id="fa27d-179"><dt><strong>SE_INC_WORKING_SET_NAME</strong></dt> <dt>TEXT(&quot;SeIncreaseWorkingSetPrivilege&quot;)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa27d-180">配置更多記憶體給在使用者的環境中執行的應用程式所需。</span><span class="sxs-lookup"><span data-stu-id="fa27d-180">Required to allocate more memory for applications that run in the context of users.</span></span><br/> <span data-ttu-id="fa27d-181">使用者權限：提高進程的工作集。</span><span class="sxs-lookup"><span data-stu-id="fa27d-181">User Right: Increase a process working set.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_LOAD_DRIVER_NAME"></span><span id="se_load_driver_name"></span><dl> <span data-ttu-id="fa27d-182"><dt><strong>SE_LOAD_DRIVER_NAME</strong></dt> <dt>文字 (&quot; SeLoadDriverPrivilege &quot;) </dt> </span><span class="sxs-lookup"><span data-stu-id="fa27d-182"><dt><strong>SE_LOAD_DRIVER_NAME</strong></dt> <dt>TEXT(&quot;SeLoadDriverPrivilege&quot;)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa27d-183">需要載入或卸載設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="fa27d-183">Required to load or unload a device driver.</span></span> <br/> <span data-ttu-id="fa27d-184">使用者權限：載入和卸載設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="fa27d-184">User Right: Load and unload device drivers.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_LOCK_MEMORY_NAME"></span><span id="se_lock_memory_name"></span><dl> <span data-ttu-id="fa27d-185"><dt><strong>SE_LOCK_MEMORY_NAME</strong></dt> <dt>文字 (&quot; SeLockMemoryPrivilege &quot;) </dt> </span><span class="sxs-lookup"><span data-stu-id="fa27d-185"><dt><strong>SE_LOCK_MEMORY_NAME</strong></dt> <dt>TEXT(&quot;SeLockMemoryPrivilege&quot;)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa27d-186">鎖定記憶體中的實體頁面所需。</span><span class="sxs-lookup"><span data-stu-id="fa27d-186">Required to lock physical pages in memory.</span></span> <br/> <span data-ttu-id="fa27d-187">使用者權限：鎖定記憶體中的分頁。</span><span class="sxs-lookup"><span data-stu-id="fa27d-187">User Right: Lock pages in memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_MACHINE_ACCOUNT_NAME"></span><span id="se_machine_account_name"></span><dl> <span data-ttu-id="fa27d-188"><dt><strong>SE_MACHINE_ACCOUNT_NAME</strong></dt> <dt>文字 (&quot; SeMachineAccountPrivilege &quot;) </dt> </span><span class="sxs-lookup"><span data-stu-id="fa27d-188"><dt><strong>SE_MACHINE_ACCOUNT_NAME</strong></dt> <dt>TEXT(&quot;SeMachineAccountPrivilege&quot;)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa27d-189">建立電腦帳戶所需。</span><span class="sxs-lookup"><span data-stu-id="fa27d-189">Required to create a computer account.</span></span> <br/> <span data-ttu-id="fa27d-190">使用者權限：將工作站新增到網域。</span><span class="sxs-lookup"><span data-stu-id="fa27d-190">User Right: Add workstations to domain.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_MANAGE_VOLUME_NAME"></span><span id="se_manage_volume_name"></span><dl> <span data-ttu-id="fa27d-191"><dt><strong>SE_MANAGE_VOLUME_NAME</strong></dt> <dt>文字 (&quot; SeManageVolumePrivilege &quot;) </dt> </span><span class="sxs-lookup"><span data-stu-id="fa27d-191"><dt><strong>SE_MANAGE_VOLUME_NAME</strong></dt> <dt>TEXT(&quot;SeManageVolumePrivilege&quot;)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa27d-192">啟用磁片區管理許可權的必要元件。</span><span class="sxs-lookup"><span data-stu-id="fa27d-192">Required to enable volume management privileges.</span></span> <br/> <span data-ttu-id="fa27d-193">使用者權限：管理磁片區上的檔案。</span><span class="sxs-lookup"><span data-stu-id="fa27d-193">User Right: Manage the files on a volume.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_PROF_SINGLE_PROCESS_NAME"></span><span id="se_prof_single_process_name"></span><dl> <span data-ttu-id="fa27d-194"><dt><strong>SE_PROF_SINGLE_PROCESS_NAME</strong></dt> <dt>文字 (&quot; SeProfileSingleProcessPrivilege &quot;) </dt> </span><span class="sxs-lookup"><span data-stu-id="fa27d-194"><dt><strong>SE_PROF_SINGLE_PROCESS_NAME</strong></dt> <dt>TEXT(&quot;SeProfileSingleProcessPrivilege&quot;)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa27d-195">需要收集單一進程的程式碼剖析資訊。</span><span class="sxs-lookup"><span data-stu-id="fa27d-195">Required to gather profiling information for a single process.</span></span> <br/> <span data-ttu-id="fa27d-196">使用者權限：設定檔單一進程。</span><span class="sxs-lookup"><span data-stu-id="fa27d-196">User Right: Profile single process.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_RELABEL_NAME"></span><span id="se_relabel_name"></span><dl> <span data-ttu-id="fa27d-197"><dt><strong>SE_RELABEL_NAME</strong></dt> <dt>文字 (&quot; SeRelabelPrivilege &quot;) </dt> </span><span class="sxs-lookup"><span data-stu-id="fa27d-197"><dt><strong>SE_RELABEL_NAME</strong></dt> <dt>TEXT(&quot;SeRelabelPrivilege&quot;)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa27d-198">修改物件的強制完整性層級所需。</span><span class="sxs-lookup"><span data-stu-id="fa27d-198">Required to modify the mandatory integrity level of an object.</span></span><br/> <span data-ttu-id="fa27d-199">使用者權限：修改物件標籤。</span><span class="sxs-lookup"><span data-stu-id="fa27d-199">User Right: Modify an object label.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_REMOTE_SHUTDOWN_NAME"></span><span id="se_remote_shutdown_name"></span><dl> <span data-ttu-id="fa27d-200"><dt><strong>SE_REMOTE_SHUTDOWN_NAME</strong></dt> <dt>文字 (&quot; SeRemoteShutdownPrivilege &quot;) </dt> </span><span class="sxs-lookup"><span data-stu-id="fa27d-200"><dt><strong>SE_REMOTE_SHUTDOWN_NAME</strong></dt> <dt>TEXT(&quot;SeRemoteShutdownPrivilege&quot;)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa27d-201">需要使用網路要求關閉系統。</span><span class="sxs-lookup"><span data-stu-id="fa27d-201">Required to shut down a system using a network request.</span></span> <br/> <span data-ttu-id="fa27d-202">使用者權限：強制從遠端系統關機。</span><span class="sxs-lookup"><span data-stu-id="fa27d-202">User Right: Force shutdown from a remote system.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_RESTORE_NAME"></span><span id="se_restore_name"></span><dl> <span data-ttu-id="fa27d-203"><dt><strong>SE_RESTORE_NAME</strong></dt> <dt>文字 (&quot; SeRestorePrivilege &quot;) </dt> </span><span class="sxs-lookup"><span data-stu-id="fa27d-203"><dt><strong>SE_RESTORE_NAME</strong></dt> <dt>TEXT(&quot;SeRestorePrivilege&quot;)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa27d-204">執行還原作業所需。</span><span class="sxs-lookup"><span data-stu-id="fa27d-204">Required to perform restore operations.</span></span> <span data-ttu-id="fa27d-205">無論為檔案指定的 ACL 為何，此許可權都會讓系統將所有寫入存取控制授與任何檔案。</span><span class="sxs-lookup"><span data-stu-id="fa27d-205">This privilege causes the system to grant all write access control to any file, regardless of the ACL specified for the file.</span></span> <span data-ttu-id="fa27d-206">寫入以外的任何存取要求仍會以 ACL 進行評估。</span><span class="sxs-lookup"><span data-stu-id="fa27d-206">Any access request other than write is still evaluated with the ACL.</span></span> <span data-ttu-id="fa27d-207">此外，此許可權可讓您將任何有效的使用者或群組 SID 設定為檔案的擁有者。</span><span class="sxs-lookup"><span data-stu-id="fa27d-207">Additionally, this privilege enables you to set any valid user or group SID as the owner of a file.</span></span> <span data-ttu-id="fa27d-208"><a href="/windows/desktop/api/winreg/nf-winreg-regloadkeya"><strong>RegLoadKey</strong></a>函式需要此許可權。</span><span class="sxs-lookup"><span data-stu-id="fa27d-208">This privilege is required by the <a href="/windows/desktop/api/winreg/nf-winreg-regloadkeya"><strong>RegLoadKey</strong></a> function.</span></span> <span data-ttu-id="fa27d-209">如果保留此許可權，則會授與下列存取權限：</span><span class="sxs-lookup"><span data-stu-id="fa27d-209">The following access rights are granted if this privilege is held:</span></span><br/>
<ul>
<li><span data-ttu-id="fa27d-210">WRITE_DAC</span><span class="sxs-lookup"><span data-stu-id="fa27d-210">WRITE_DAC</span></span></li>
<li><span data-ttu-id="fa27d-211">WRITE_OWNER</span><span class="sxs-lookup"><span data-stu-id="fa27d-211">WRITE_OWNER</span></span></li>
<li><span data-ttu-id="fa27d-212">ACCESS_SYSTEM_SECURITY</span><span class="sxs-lookup"><span data-stu-id="fa27d-212">ACCESS_SYSTEM_SECURITY</span></span></li>
<li><span data-ttu-id="fa27d-213">FILE_GENERIC_WRITE</span><span class="sxs-lookup"><span data-stu-id="fa27d-213">FILE_GENERIC_WRITE</span></span></li>
<li><span data-ttu-id="fa27d-214">FILE_ADD_FILE</span><span class="sxs-lookup"><span data-stu-id="fa27d-214">FILE_ADD_FILE</span></span></li>
<li><span data-ttu-id="fa27d-215">FILE_ADD_SUBDIRECTORY</span><span class="sxs-lookup"><span data-stu-id="fa27d-215">FILE_ADD_SUBDIRECTORY</span></span></li>
<li><span data-ttu-id="fa27d-216">刪除</span><span class="sxs-lookup"><span data-stu-id="fa27d-216">DELETE</span></span></li>
</ul>
<span data-ttu-id="fa27d-217">使用者權限：還原檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="fa27d-217">User Right: Restore files and directories.</span></span><br/><span data-ttu-id="fa27d-218">如果檔案位於卸載式磁片磁碟機上，且已啟用「Audit 卸除式存放裝置」，則 SE_SECURITY_NAME 必須有 ACCESS_SYSTEM_SECURITY。</span><span class="sxs-lookup"><span data-stu-id="fa27d-218">If the file is located on a removable drive and the "Audit Removable Storage" is enabled, the SE_SECURITY_NAME is required to have ACCESS_SYSTEM_SECURITY.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_SECURITY_NAME"></span><span id="se_security_name"></span><dl> <span data-ttu-id="fa27d-219"><dt><strong>SE_SECURITY_NAME</strong></dt> <dt>文字 (&quot; SeSecurityPrivilege &quot;) </dt> </span><span class="sxs-lookup"><span data-stu-id="fa27d-219"><dt><strong>SE_SECURITY_NAME</strong></dt> <dt>TEXT(&quot;SeSecurityPrivilege&quot;)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa27d-220">需要執行一些安全性相關的功能，例如控制和查看審核訊息。</span><span class="sxs-lookup"><span data-stu-id="fa27d-220">Required to perform a number of security-related functions, such as controlling and viewing audit messages.</span></span> <span data-ttu-id="fa27d-221">此許可權會將其持有者識別為安全性操作員。</span><span class="sxs-lookup"><span data-stu-id="fa27d-221">This privilege identifies its holder as a security operator.</span></span> <br/> <span data-ttu-id="fa27d-222">使用者權限：管理審核和安全性記錄。</span><span class="sxs-lookup"><span data-stu-id="fa27d-222">User Right: Manage auditing and security log.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_SHUTDOWN_NAME"></span><span id="se_shutdown_name"></span><dl> <span data-ttu-id="fa27d-223"><dt><strong>SE_SHUTDOWN_NAME</strong></dt> <dt>文字 (&quot; SeShutdownPrivilege &quot;) </dt> </span><span class="sxs-lookup"><span data-stu-id="fa27d-223"><dt><strong>SE_SHUTDOWN_NAME</strong></dt> <dt>TEXT(&quot;SeShutdownPrivilege&quot;)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa27d-224">關閉本機系統的必要參數。</span><span class="sxs-lookup"><span data-stu-id="fa27d-224">Required to shut down a local system.</span></span> <br/> <span data-ttu-id="fa27d-225">使用者權限：關閉系統。</span><span class="sxs-lookup"><span data-stu-id="fa27d-225">User Right: Shut down the system.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_SYNC_AGENT_NAME"></span><span id="se_sync_agent_name"></span><dl> <span data-ttu-id="fa27d-226"><dt><strong>SE_SYNC_AGENT_NAME</strong></dt> <dt>文字 (&quot; SeSyncAgentPrivilege &quot;) </dt> </span><span class="sxs-lookup"><span data-stu-id="fa27d-226"><dt><strong>SE_SYNC_AGENT_NAME</strong></dt> <dt>TEXT(&quot;SeSyncAgentPrivilege&quot;)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa27d-227">網域控制站在使用 <a href="/windows/desktop/SecGloss/l-gly"><em>輕量型目錄存取協定</em></a> 目錄同步處理服務時所需。</span><span class="sxs-lookup"><span data-stu-id="fa27d-227">Required for a domain controller to use the <a href="/windows/desktop/SecGloss/l-gly"><em>Lightweight Directory Access Protocol</em></a> directory synchronization services.</span></span> <span data-ttu-id="fa27d-228">此許可權可讓持有者讀取目錄中的所有物件和屬性，不論物件和屬性的保護為何。</span><span class="sxs-lookup"><span data-stu-id="fa27d-228">This privilege enables the holder to read all objects and properties in the directory, regardless of the protection on the objects and properties.</span></span> <span data-ttu-id="fa27d-229">依預設，它會指派給網域控制站上的系統管理員和 LocalSystem 帳戶。</span><span class="sxs-lookup"><span data-stu-id="fa27d-229">By default, it is assigned to the Administrator and LocalSystem accounts on domain controllers.</span></span> <br/> <span data-ttu-id="fa27d-230">使用者權限：同步目錄服務資料。</span><span class="sxs-lookup"><span data-stu-id="fa27d-230">User Right: Synchronize directory service data.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_SYSTEM_ENVIRONMENT_NAME"></span><span id="se_system_environment_name"></span><dl> <span data-ttu-id="fa27d-231"><dt><strong>SE_SYSTEM_ENVIRONMENT_NAME</strong></dt> <dt>文字 (&quot; SeSystemEnvironmentPrivilege &quot;) </dt> </span><span class="sxs-lookup"><span data-stu-id="fa27d-231"><dt><strong>SE_SYSTEM_ENVIRONMENT_NAME</strong></dt> <dt>TEXT(&quot;SeSystemEnvironmentPrivilege&quot;)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa27d-232">需要修改使用這種記憶體類型之系統的靜態 RAM 來儲存設定資訊。</span><span class="sxs-lookup"><span data-stu-id="fa27d-232">Required to modify the nonvolatile RAM of systems that use this type of memory to store configuration information.</span></span> <br/> <span data-ttu-id="fa27d-233">使用者權限：修改固件環境值。</span><span class="sxs-lookup"><span data-stu-id="fa27d-233">User Right: Modify firmware environment values.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_SYSTEM_PROFILE_NAME"></span><span id="se_system_profile_name"></span><dl> <span data-ttu-id="fa27d-234"><dt><strong>SE_SYSTEM_PROFILE_NAME</strong></dt> <dt>文字 (&quot; SeSystemProfilePrivilege &quot;) </dt> </span><span class="sxs-lookup"><span data-stu-id="fa27d-234"><dt><strong>SE_SYSTEM_PROFILE_NAME</strong></dt> <dt>TEXT(&quot;SeSystemProfilePrivilege&quot;)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa27d-235">需要收集整個系統的程式碼剖析資訊。</span><span class="sxs-lookup"><span data-stu-id="fa27d-235">Required to gather profiling information for the entire system.</span></span> <br/> <span data-ttu-id="fa27d-236">使用者權限：配置檔案系統效能。</span><span class="sxs-lookup"><span data-stu-id="fa27d-236">User Right: Profile system performance.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_SYSTEMTIME_NAME"></span><span id="se_systemtime_name"></span><dl> <span data-ttu-id="fa27d-237"><dt><strong>SE_SYSTEMTIME_NAME</strong></dt> <dt>文字 (&quot; SeSystemtimePrivilege &quot;) </dt> </span><span class="sxs-lookup"><span data-stu-id="fa27d-237"><dt><strong>SE_SYSTEMTIME_NAME</strong></dt> <dt>TEXT(&quot;SeSystemtimePrivilege&quot;)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa27d-238">修改系統時間所需。</span><span class="sxs-lookup"><span data-stu-id="fa27d-238">Required to modify the system time.</span></span> <br/> <span data-ttu-id="fa27d-239">使用者權限：變更系統時間。</span><span class="sxs-lookup"><span data-stu-id="fa27d-239">User Right: Change the system time.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_TAKE_OWNERSHIP_NAME"></span><span id="se_take_ownership_name"></span><dl> <span data-ttu-id="fa27d-240"><dt><strong>SE_TAKE_OWNERSHIP_NAME</strong></dt> <dt>文字 (&quot; SeTakeOwnershipPrivilege &quot;) </dt> </span><span class="sxs-lookup"><span data-stu-id="fa27d-240"><dt><strong>SE_TAKE_OWNERSHIP_NAME</strong></dt> <dt>TEXT(&quot;SeTakeOwnershipPrivilege&quot;)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa27d-241">取得物件擁有權而不授與任意存取權的必要項。</span><span class="sxs-lookup"><span data-stu-id="fa27d-241">Required to take ownership of an object without being granted discretionary access.</span></span> <span data-ttu-id="fa27d-242">此許可權允許將 [擁有者] 值設定為 [擁有者] 可合法指派為物件之擁有者的值。</span><span class="sxs-lookup"><span data-stu-id="fa27d-242">This privilege allows the owner value to be set only to those values that the holder may legitimately assign as the owner of an object.</span></span> <br/> <span data-ttu-id="fa27d-243">使用者權限：取得檔案或其他物件的擁有權。</span><span class="sxs-lookup"><span data-stu-id="fa27d-243">User Right: Take ownership of files or other objects.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_TCB_NAME"></span><span id="se_tcb_name"></span><dl> <span data-ttu-id="fa27d-244"><dt><strong>SE_TCB_NAME</strong></dt> <dt>文字 (&quot; SeTcbPrivilege &quot;) </dt> </span><span class="sxs-lookup"><span data-stu-id="fa27d-244"><dt><strong>SE_TCB_NAME</strong></dt> <dt>TEXT(&quot;SeTcbPrivilege&quot;)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa27d-245">此許可權會將其持有者識別為受信任電腦基礎的一部分。</span><span class="sxs-lookup"><span data-stu-id="fa27d-245">This privilege identifies its holder as part of the trusted computer base.</span></span> <span data-ttu-id="fa27d-246">某些受信任的受保護子系統被授與此許可權。</span><span class="sxs-lookup"><span data-stu-id="fa27d-246">Some trusted protected subsystems are granted this privilege.</span></span> <br/> <span data-ttu-id="fa27d-247">使用者權限：作為作業系統的一部分。</span><span class="sxs-lookup"><span data-stu-id="fa27d-247">User Right: Act as part of the operating system.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_TIME_ZONE_NAME"></span><span id="se_time_zone_name"></span><dl> <span data-ttu-id="fa27d-248"><dt><strong>SE_TIME_ZONE_NAME</strong></dt> <dt>文字 (&quot; SeTimeZonePrivilege &quot;) </dt> </span><span class="sxs-lookup"><span data-stu-id="fa27d-248"><dt><strong>SE_TIME_ZONE_NAME</strong></dt> <dt>TEXT(&quot;SeTimeZonePrivilege&quot;)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa27d-249">需要調整與電腦內部時鐘相關聯的時區。</span><span class="sxs-lookup"><span data-stu-id="fa27d-249">Required to adjust the time zone associated with the computer's internal clock.</span></span><br/> <span data-ttu-id="fa27d-250">使用者權限：變更時區。</span><span class="sxs-lookup"><span data-stu-id="fa27d-250">User Right: Change the time zone.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_TRUSTED_CREDMAN_ACCESS_NAME"></span><span id="se_trusted_credman_access_name"></span><dl> <span data-ttu-id="fa27d-251"><dt><strong>SE_TRUSTED_CREDMAN_ACCESS_NAME</strong></dt> <dt>文字 (&quot; SeTrustedCredManAccessPrivilege &quot;) </dt> </span><span class="sxs-lookup"><span data-stu-id="fa27d-251"><dt><strong>SE_TRUSTED_CREDMAN_ACCESS_NAME</strong></dt> <dt>TEXT(&quot;SeTrustedCredManAccessPrivilege&quot;)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa27d-252">以信任的呼叫端存取認證管理員所需。</span><span class="sxs-lookup"><span data-stu-id="fa27d-252">Required to access Credential Manager as a trusted caller.</span></span><br/> <span data-ttu-id="fa27d-253">使用者權限：存取認證管理員作為受信任的呼叫者。</span><span class="sxs-lookup"><span data-stu-id="fa27d-253">User Right: Access Credential Manager as a trusted caller.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_UNDOCK_NAME"></span><span id="se_undock_name"></span><dl> <span data-ttu-id="fa27d-254"><dt><strong>SE_UNDOCK_NAME</strong></dt> <dt>文字 (&quot; SeUndockPrivilege &quot;) </dt> </span><span class="sxs-lookup"><span data-stu-id="fa27d-254"><dt><strong>SE_UNDOCK_NAME</strong></dt> <dt>TEXT(&quot;SeUndockPrivilege&quot;)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa27d-255">卸載膝上型電腦的必要。</span><span class="sxs-lookup"><span data-stu-id="fa27d-255">Required to undock a laptop.</span></span><br/> <span data-ttu-id="fa27d-256">使用者權限：從銜接站移除電腦。</span><span class="sxs-lookup"><span data-stu-id="fa27d-256">User Right: Remove computer from docking station.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_UNSOLICITED_INPUT_NAME"></span><span id="se_unsolicited_input_name"></span><dl> <span data-ttu-id="fa27d-257"><dt><strong>SE_UNSOLICITED_INPUT_NAME</strong></dt> <dt>文字 (&quot; SeUnsolicitedInputPrivilege &quot;) </dt> </span><span class="sxs-lookup"><span data-stu-id="fa27d-257"><dt><strong>SE_UNSOLICITED_INPUT_NAME</strong></dt> <dt>TEXT(&quot;SeUnsolicitedInputPrivilege&quot;)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="fa27d-258">從 <a href="/windows/desktop/SecGloss/t-gly"><em>終端</em></a> 機裝置讀取未經要求的輸入時需要。</span><span class="sxs-lookup"><span data-stu-id="fa27d-258">Required to read unsolicited input from a <a href="/windows/desktop/SecGloss/t-gly"><em>terminal</em></a> device.</span></span><br/> <span data-ttu-id="fa27d-259">使用者權限：不適用。</span><span class="sxs-lookup"><span data-stu-id="fa27d-259">User Right: Not applicable.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="fa27d-260">備註</span><span class="sxs-lookup"><span data-stu-id="fa27d-260">Remarks</span></span>

<span data-ttu-id="fa27d-261">許可權常數在 Winnt 中會定義為字串。</span><span class="sxs-lookup"><span data-stu-id="fa27d-261">Privilege constants are defined as strings in Winnt.h.</span></span> <span data-ttu-id="fa27d-262">例如，SE \_ AUDIT \_ NAME 常數定義為 "SeAuditPrivilege"。</span><span class="sxs-lookup"><span data-stu-id="fa27d-262">For example, the SE\_AUDIT\_NAME constant is defined as "SeAuditPrivilege".</span></span>

## <a name="requirements"></a><span data-ttu-id="fa27d-263">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa27d-263">Requirements</span></span>



| <span data-ttu-id="fa27d-264">需求</span><span class="sxs-lookup"><span data-stu-id="fa27d-264">Requirement</span></span> | <span data-ttu-id="fa27d-265">值</span><span class="sxs-lookup"><span data-stu-id="fa27d-265">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fa27d-266">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fa27d-266">Minimum supported client</span></span><br/> | <span data-ttu-id="fa27d-267">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa27d-267">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fa27d-268">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fa27d-268">Minimum supported server</span></span><br/> | <span data-ttu-id="fa27d-269">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa27d-269">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fa27d-270">標頭</span><span class="sxs-lookup"><span data-stu-id="fa27d-270">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa27d-271"><dt>Winnt。h</dt></span><span class="sxs-lookup"><span data-stu-id="fa27d-271"><dt>Winnt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa27d-272">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa27d-272">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa27d-273">特權</span><span class="sxs-lookup"><span data-stu-id="fa27d-273">Privileges</span></span>](privileges.md)
</dt> </dl>


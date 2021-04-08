---
description: SWbemPrivilegeSet. AddAsString 方法的 strPrivilege 參數和 SWbemPrivilegeSet 的 iPrivilege 參數。 Add 需要 WbemPrivilegeEnum 的許可權字串。
ms.assetid: f9400597-81bb-44a8-80dc-aba0160aea26
ms.tgt_platform: multiple
title: '許可權常數 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- wbemPrivilegeCreateToken
- wbemPrivilegePrimaryToken
- wbemPrivilegeLockMemory
- wbemPrivilegeIncreaseQuota
- wbemPrivilegeMachineAccount
- wbemPrivilegeTcb
- wbemPrivilegeSecurity
- wbemPrivilegeTakeOwnership
- wbemPrivilegeLoadDriver
- wbemPrivilegeSystemProfile
- wbemPrivilegeSystemtime
- wbemPrivilegeProfileSingleProcess
- wbemPrivilegeIncreaseBasePriority
- wbemPrivilegeCreatePagefile
- wbemPrivilegeCreatePermanent
- wbemPrivilegeBackup
- wbemPrivilegeRestore
- wbemPrivilegeShutdown
- wbemPrivilegeDebug
- wbemPrivilegeAudit
- wbemPrivilegeSystemEnvironment
- wbemPrivilegeChangeNotify
- wbemPrivilegeRemoteShutdown
- wbemPrivilegeUndock
- wbemPrivilegeSyncAgent
- wbemPrivilegeEnableDelegation
- wbemPrivilegeManageVolume
api_type:
- HeaderDef
api_location:
- Wbemdisp.h
ms.openlocfilehash: 73fb9167af63f40f3a6e1c00470d871f749d228a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695152"
---
# <a name="privilege-constants"></a><span data-ttu-id="4fc32-103">許可權常數</span><span class="sxs-lookup"><span data-stu-id="4fc32-103">Privilege Constants</span></span>

<span data-ttu-id="4fc32-104">[**SWbemPrivilegeSet. AddAsString**](swbemprivilegeset-addasstring.md)方法的 *StrPrivilege* 參數和 SWbemPrivilegeSet 的 *IPrivilege* 參數 [**。 Add**](swbemprivilegeset-add.md)需要 [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)的許可權字串。</span><span class="sxs-lookup"><span data-stu-id="4fc32-104">The *strPrivilege* parameter of the [**SWbemPrivilegeSet.AddAsString**](swbemprivilegeset-addasstring.md) method and the *iPrivilege* parameter for [**SWbemPrivilegeSet.Add**](swbemprivilegeset-add.md) require privilege strings from [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).</span></span> <span data-ttu-id="4fc32-105">如需如何使用許可權常數的詳細資訊，請參閱 [執行特殊許可權作業](executing-privileged-operations.md)。</span><span class="sxs-lookup"><span data-stu-id="4fc32-105">For more information about how to use privilege constants, see [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

<span data-ttu-id="4fc32-106">下列常數定義于 [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)中。</span><span class="sxs-lookup"><span data-stu-id="4fc32-106">The following constants are defined in [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).</span></span> <span data-ttu-id="4fc32-107">下列清單包含 c + + 和字串的對等常數，用於編寫腳本。</span><span class="sxs-lookup"><span data-stu-id="4fc32-107">The following list includes the equivalent constants for C++ and strings for scripting.</span></span> <span data-ttu-id="4fc32-108">若要形成腳本簡短名稱，請從 c + + 常數名稱中移除「Se」和「許可權」。</span><span class="sxs-lookup"><span data-stu-id="4fc32-108">To form the scripting short name, remove the "Se" and "Privilege" from the C++ constant name.</span></span>

<span data-ttu-id="4fc32-109">下列 VBScript 程式碼範例顯示如何在腳本中啟用 RemoteShutdown 許可權。</span><span class="sxs-lookup"><span data-stu-id="4fc32-109">The following VBScript code example shows how to enable the RemoteShutdown privilege in a script.</span></span>


```VB
Set Service = GetObject("winmgmts:{impersonationLevel=impersonate, (RemoteShutdown)}")
```



<span data-ttu-id="4fc32-110">許多 WMI 方法都需要啟用一或多個許可權。</span><span class="sxs-lookup"><span data-stu-id="4fc32-110">Many WMI methods require that one or more permission be enabled.</span></span> <span data-ttu-id="4fc32-111">如果尚未授與帳戶許可權，就無法針對方法呼叫啟用該帳戶。</span><span class="sxs-lookup"><span data-stu-id="4fc32-111">If an account has not been granted a privilege, it cannot be enabled for the method call.</span></span>

<dl> <dt>

<span data-ttu-id="4fc32-112"><span id="wbemPrivilegeCreateToken"></span><span id="wbemprivilegecreatetoken"></span><span id="WBEMPRIVILEGECREATETOKEN"></span>**wbemPrivilegeCreateToken**</span><span class="sxs-lookup"><span data-stu-id="4fc32-112"><span id="wbemPrivilegeCreateToken"></span><span id="wbemprivilegecreatetoken"></span><span id="WBEMPRIVILEGECREATETOKEN"></span>**wbemPrivilegeCreateToken**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc32-113">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="4fc32-113">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="4fc32-114">C + + 常數： **SE \_ CREATE \_ TOKEN \_ NAME** string： **SeCreateTokenPrivilege**</span><span class="sxs-lookup"><span data-stu-id="4fc32-114">C++ constant: **SE\_CREATE\_TOKEN\_NAME** string: **SeCreateTokenPrivilege**</span></span>

<span data-ttu-id="4fc32-115">腳本簡短名稱： **CreateToken**</span><span class="sxs-lookup"><span data-stu-id="4fc32-115">Scripting short name: **CreateToken**</span></span>

<span data-ttu-id="4fc32-116">建立主要權杖物件的必要參數。</span><span class="sxs-lookup"><span data-stu-id="4fc32-116">Required to create a primary token object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc32-117"><span id="wbemPrivilegePrimaryToken"></span><span id="wbemprivilegeprimarytoken"></span><span id="WBEMPRIVILEGEPRIMARYTOKEN"></span>**wbemPrivilegePrimaryToken**</span><span class="sxs-lookup"><span data-stu-id="4fc32-117"><span id="wbemPrivilegePrimaryToken"></span><span id="wbemprivilegeprimarytoken"></span><span id="WBEMPRIVILEGEPRIMARYTOKEN"></span>**wbemPrivilegePrimaryToken**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc32-118">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="4fc32-118">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="4fc32-119">C + + 常數： **SeAssignPrimaryTokenPrivilege** 字串： **SeAssignPrimaryTokenPrivilege**</span><span class="sxs-lookup"><span data-stu-id="4fc32-119">C++ constant: **SeAssignPrimaryTokenPrivilege** string: **SeAssignPrimaryTokenPrivilege**</span></span>

<span data-ttu-id="4fc32-120">腳本簡短名稱： **AssignPrimaryToken**</span><span class="sxs-lookup"><span data-stu-id="4fc32-120">Scripting short name: **AssignPrimaryToken**</span></span>

<span data-ttu-id="4fc32-121">取代進程層級 token 所需。</span><span class="sxs-lookup"><span data-stu-id="4fc32-121">Required to replace a process-level token.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc32-122"><span id="wbemPrivilegeLockMemory"></span><span id="wbemprivilegelockmemory"></span><span id="WBEMPRIVILEGELOCKMEMORY"></span>**wbemPrivilegeLockMemory**</span><span class="sxs-lookup"><span data-stu-id="4fc32-122"><span id="wbemPrivilegeLockMemory"></span><span id="wbemprivilegelockmemory"></span><span id="WBEMPRIVILEGELOCKMEMORY"></span>**wbemPrivilegeLockMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc32-123">3 (0x3) </span><span class="sxs-lookup"><span data-stu-id="4fc32-123">3 (0x3)</span></span>
</dt> <dt>



<span data-ttu-id="4fc32-124">C + + 常數： **SE \_ 鎖定 \_ 記憶體 \_ 名稱** 字串： **SeLockMemoryPrivilege**</span><span class="sxs-lookup"><span data-stu-id="4fc32-124">C++ constant: **SE\_LOCK\_MEMORY\_NAME** string: **SeLockMemoryPrivilege**</span></span>

<span data-ttu-id="4fc32-125">腳本簡短名稱： **LockMemory**</span><span class="sxs-lookup"><span data-stu-id="4fc32-125">Scripting short name: **LockMemory**</span></span>

<span data-ttu-id="4fc32-126">鎖定記憶體中的分頁所需。</span><span class="sxs-lookup"><span data-stu-id="4fc32-126">Required to lock pages in memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc32-127"><span id="wbemPrivilegeIncreaseQuota"></span><span id="wbemprivilegeincreasequota"></span><span id="WBEMPRIVILEGEINCREASEQUOTA"></span>**wbemPrivilegeIncreaseQuota**</span><span class="sxs-lookup"><span data-stu-id="4fc32-127"><span id="wbemPrivilegeIncreaseQuota"></span><span id="wbemprivilegeincreasequota"></span><span id="WBEMPRIVILEGEINCREASEQUOTA"></span>**wbemPrivilegeIncreaseQuota**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc32-128">4 (0x4) </span><span class="sxs-lookup"><span data-stu-id="4fc32-128">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="4fc32-129">C + + 常數： **SE \_ 增加 \_ 配額 \_ 名稱** 字串： **SeIncreaseQuotaPrivilege**</span><span class="sxs-lookup"><span data-stu-id="4fc32-129">C++ constant: **SE\_INCREASE\_QUOTA\_NAME** string: **SeIncreaseQuotaPrivilege**</span></span>

<span data-ttu-id="4fc32-130">腳本簡短名稱： **IncreaseQuotaPrivilege**</span><span class="sxs-lookup"><span data-stu-id="4fc32-130">Scripting short name: **IncreaseQuotaPrivilege**</span></span>

<span data-ttu-id="4fc32-131">調整進程的記憶體配額所需。</span><span class="sxs-lookup"><span data-stu-id="4fc32-131">Required to adjust memory quotas for a process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc32-132"><span id="wbemPrivilegeMachineAccount"></span><span id="wbemprivilegemachineaccount"></span><span id="WBEMPRIVILEGEMACHINEACCOUNT"></span>**wbemPrivilegeMachineAccount**</span><span class="sxs-lookup"><span data-stu-id="4fc32-132"><span id="wbemPrivilegeMachineAccount"></span><span id="wbemprivilegemachineaccount"></span><span id="WBEMPRIVILEGEMACHINEACCOUNT"></span>**wbemPrivilegeMachineAccount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc32-133">5 (0x5) </span><span class="sxs-lookup"><span data-stu-id="4fc32-133">5 (0x5)</span></span>
</dt> <dt>



<span data-ttu-id="4fc32-134">C + + 常數： **SE \_ MACINE \_ ACCOUNT \_ NAME** string： **SeMachineAccountPrivilege**</span><span class="sxs-lookup"><span data-stu-id="4fc32-134">C++ constant: **SE\_MACINE\_ACCOUNT\_NAME** string: **SeMachineAccountPrivilege**</span></span>

<span data-ttu-id="4fc32-135">腳本簡短名稱： **MachineAccount**</span><span class="sxs-lookup"><span data-stu-id="4fc32-135">Scripting short name: **MachineAccount**</span></span>

<span data-ttu-id="4fc32-136">將工作站新增到網域的必要。</span><span class="sxs-lookup"><span data-stu-id="4fc32-136">Required to add workstations to a domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc32-137"><span id="wbemPrivilegeTcb"></span><span id="wbemprivilegetcb"></span><span id="WBEMPRIVILEGETCB"></span>**wbemPrivilegeTcb**</span><span class="sxs-lookup"><span data-stu-id="4fc32-137"><span id="wbemPrivilegeTcb"></span><span id="wbemprivilegetcb"></span><span id="WBEMPRIVILEGETCB"></span>**wbemPrivilegeTcb**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc32-138">6 (0x6) </span><span class="sxs-lookup"><span data-stu-id="4fc32-138">6 (0x6)</span></span>
</dt> <dt>



<span data-ttu-id="4fc32-139">C + + 常數： **SE \_ TCB \_ 名稱** 字串： **SeTcbPrivilege**</span><span class="sxs-lookup"><span data-stu-id="4fc32-139">C++ constant: **SE\_TCB\_NAME** string: **SeTcbPrivilege**</span></span>

<span data-ttu-id="4fc32-140">腳本簡短名稱： **Tcb**</span><span class="sxs-lookup"><span data-stu-id="4fc32-140">Scripting short name: **Tcb**</span></span>

<span data-ttu-id="4fc32-141">需要作為作業系統的一部分。</span><span class="sxs-lookup"><span data-stu-id="4fc32-141">Required to act as part of the operating system.</span></span> <span data-ttu-id="4fc32-142">持有者是受信任電腦基礎的一部分。</span><span class="sxs-lookup"><span data-stu-id="4fc32-142">The holder is part of the trusted computer base.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc32-143"><span id="wbemPrivilegeSecurity"></span><span id="wbemprivilegesecurity"></span><span id="WBEMPRIVILEGESECURITY"></span>**wbemPrivilegeSecurity**</span><span class="sxs-lookup"><span data-stu-id="4fc32-143"><span id="wbemPrivilegeSecurity"></span><span id="wbemprivilegesecurity"></span><span id="WBEMPRIVILEGESECURITY"></span>**wbemPrivilegeSecurity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc32-144">7 (0x7) </span><span class="sxs-lookup"><span data-stu-id="4fc32-144">7 (0x7)</span></span>
</dt> <dt>



<span data-ttu-id="4fc32-145">C + + 常數： **SE \_ 安全性 \_ 名稱** 字串： **SeSecurityPrivilege**</span><span class="sxs-lookup"><span data-stu-id="4fc32-145">C++ constant: **SE\_SECURITY\_NAME** string: **SeSecurityPrivilege**</span></span>

<span data-ttu-id="4fc32-146">腳本簡短名稱： **安全性**</span><span class="sxs-lookup"><span data-stu-id="4fc32-146">Scripting short name: **Security**</span></span>

<span data-ttu-id="4fc32-147">管理審核和 NT 安全性記錄檔所需。</span><span class="sxs-lookup"><span data-stu-id="4fc32-147">Required to manage auditing and the NT security log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc32-148"><span id="wbemPrivilegeTakeOwnership"></span><span id="wbemprivilegetakeownership"></span><span id="WBEMPRIVILEGETAKEOWNERSHIP"></span>**wbemPrivilegeTakeOwnership**</span><span class="sxs-lookup"><span data-stu-id="4fc32-148"><span id="wbemPrivilegeTakeOwnership"></span><span id="wbemprivilegetakeownership"></span><span id="WBEMPRIVILEGETAKEOWNERSHIP"></span>**wbemPrivilegeTakeOwnership**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc32-149">8 (0x8) </span><span class="sxs-lookup"><span data-stu-id="4fc32-149">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="4fc32-150">C + + 常數： **SE \_ 取得 \_ 擁有權 \_ 名稱** 字串： **SeTakeOwnershipPrivilege**</span><span class="sxs-lookup"><span data-stu-id="4fc32-150">C++ constant: **SE\_TAKE\_OWNERSHIP\_NAME** string: **SeTakeOwnershipPrivilege**</span></span>

<span data-ttu-id="4fc32-151">腳本簡短名稱： **TakeOwnership**</span><span class="sxs-lookup"><span data-stu-id="4fc32-151">Scripting short name: **TakeOwnership**</span></span>

<span data-ttu-id="4fc32-152">需要擁有檔案或其他物件的擁有權，而不需要 [*存取控制專案*](/windows/desktop/SecGloss/a-gly) (ACE) 在 *任意存取控制清單* (DACL) 中。</span><span class="sxs-lookup"><span data-stu-id="4fc32-152">Required to assume ownership of files or other objects without having an [*Access Control Entry*](/windows/desktop/SecGloss/a-gly) (ACE) in the *discretionary access control list* (DACL).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc32-153"><span id="wbemPrivilegeLoadDriver"></span><span id="wbemprivilegeloaddriver"></span><span id="WBEMPRIVILEGELOADDRIVER"></span>**wbemPrivilegeLoadDriver**</span><span class="sxs-lookup"><span data-stu-id="4fc32-153"><span id="wbemPrivilegeLoadDriver"></span><span id="wbemprivilegeloaddriver"></span><span id="WBEMPRIVILEGELOADDRIVER"></span>**wbemPrivilegeLoadDriver**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc32-154">9 (0x9) </span><span class="sxs-lookup"><span data-stu-id="4fc32-154">9 (0x9)</span></span>
</dt> <dt>



<span data-ttu-id="4fc32-155">C + + 常數： **SE \_ 載入 \_ 驅動程式** 字串： **SeLoadDriverPrivilege**</span><span class="sxs-lookup"><span data-stu-id="4fc32-155">C++ constant: **SE\_LOAD\_DRIVER** string: **SeLoadDriverPrivilege**</span></span>

<span data-ttu-id="4fc32-156">腳本簡短名稱： **LoadDriver**</span><span class="sxs-lookup"><span data-stu-id="4fc32-156">Scripting short name: **LoadDriver**</span></span>

<span data-ttu-id="4fc32-157">需要載入或卸載設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="4fc32-157">Required to load or unload a device driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc32-158"><span id="wbemPrivilegeSystemProfile"></span><span id="wbemprivilegesystemprofile"></span><span id="WBEMPRIVILEGESYSTEMPROFILE"></span>**wbemPrivilegeSystemProfile**</span><span class="sxs-lookup"><span data-stu-id="4fc32-158"><span id="wbemPrivilegeSystemProfile"></span><span id="wbemprivilegesystemprofile"></span><span id="WBEMPRIVILEGESYSTEMPROFILE"></span>**wbemPrivilegeSystemProfile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc32-159">10 (0xA) </span><span class="sxs-lookup"><span data-stu-id="4fc32-159">10 (0xA)</span></span>
</dt> <dt>



<span data-ttu-id="4fc32-160">C + + 常數： **SE \_ 系統 \_ 設定檔 \_ 名稱** 字串： **SeSystemProfilePrivilege**</span><span class="sxs-lookup"><span data-stu-id="4fc32-160">C++ constant: **SE\_SYSTEM\_PROFILE\_NAME** string: **SeSystemProfilePrivilege**</span></span>

<span data-ttu-id="4fc32-161">腳本簡短名稱： **SystemProfile**</span><span class="sxs-lookup"><span data-stu-id="4fc32-161">Scripting short name: **SystemProfile**</span></span>

<span data-ttu-id="4fc32-162">需要收集有關系統效能的設定檔資訊。</span><span class="sxs-lookup"><span data-stu-id="4fc32-162">Required to gather profile information about system performance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc32-163"><span id="wbemPrivilegeSystemtime"></span><span id="wbemprivilegesystemtime"></span><span id="WBEMPRIVILEGESYSTEMTIME"></span>**wbemPrivilegeSystemtime**</span><span class="sxs-lookup"><span data-stu-id="4fc32-163"><span id="wbemPrivilegeSystemtime"></span><span id="wbemprivilegesystemtime"></span><span id="WBEMPRIVILEGESYSTEMTIME"></span>**wbemPrivilegeSystemtime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc32-164">11 (0xB) </span><span class="sxs-lookup"><span data-stu-id="4fc32-164">11 (0xB)</span></span>
</dt> <dt>



<span data-ttu-id="4fc32-165">C + + 常數： **SE \_ SYSTEMTIME** \_ 名稱字串： **SeSystemtimePrivilege**</span><span class="sxs-lookup"><span data-stu-id="4fc32-165">C++ constant: **SE\_SYSTEMTIME**\_NAME string: **SeSystemtimePrivilege**</span></span>

<span data-ttu-id="4fc32-166">腳本簡短名稱： **Systemtime**</span><span class="sxs-lookup"><span data-stu-id="4fc32-166">Scripting short name: **Systemtime**</span></span>

<span data-ttu-id="4fc32-167">變更系統時間所需。</span><span class="sxs-lookup"><span data-stu-id="4fc32-167">Required to change the system time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc32-168"><span id="wbemPrivilegeProfileSingleProcess"></span><span id="wbemprivilegeprofilesingleprocess"></span><span id="WBEMPRIVILEGEPROFILESINGLEPROCESS"></span>**wbemPrivilegeProfileSingleProcess**</span><span class="sxs-lookup"><span data-stu-id="4fc32-168"><span id="wbemPrivilegeProfileSingleProcess"></span><span id="wbemprivilegeprofilesingleprocess"></span><span id="WBEMPRIVILEGEPROFILESINGLEPROCESS"></span>**wbemPrivilegeProfileSingleProcess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc32-169">12 (0xC) </span><span class="sxs-lookup"><span data-stu-id="4fc32-169">12 (0xC)</span></span>
</dt> <dt>



<span data-ttu-id="4fc32-170">C + + 常數： **SE \_ 獲 \_ 單一 \_ 進程 \_ 名稱** 字串： **SeProfileSingleProcessPrivilege**</span><span class="sxs-lookup"><span data-stu-id="4fc32-170">C++ constant: **SE\_PROF\_SINGLE\_PROCESS\_NAME** string: **SeProfileSingleProcessPrivilege**</span></span>

<span data-ttu-id="4fc32-171">腳本簡短名稱： **ProfileSingleProcess**</span><span class="sxs-lookup"><span data-stu-id="4fc32-171">Scripting short name: **ProfileSingleProcess**</span></span>

<span data-ttu-id="4fc32-172">需要收集單一進程的設定檔資訊。</span><span class="sxs-lookup"><span data-stu-id="4fc32-172">Required to gather profile information for a single process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc32-173"><span id="wbemPrivilegeIncreaseBasePriority"></span><span id="wbemprivilegeincreasebasepriority"></span><span id="WBEMPRIVILEGEINCREASEBASEPRIORITY"></span>**wbemPrivilegeIncreaseBasePriority**</span><span class="sxs-lookup"><span data-stu-id="4fc32-173"><span id="wbemPrivilegeIncreaseBasePriority"></span><span id="wbemprivilegeincreasebasepriority"></span><span id="WBEMPRIVILEGEINCREASEBASEPRIORITY"></span>**wbemPrivilegeIncreaseBasePriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc32-174">13 (0xD) </span><span class="sxs-lookup"><span data-stu-id="4fc32-174">13 (0xD)</span></span>
</dt> <dt>



<span data-ttu-id="4fc32-175">C + + 常數： **SE \_ Inc. \_ 基底 \_ 優先順序 \_ 名稱** 字串： **SeIncreaseBasePriorityPrivilege**</span><span class="sxs-lookup"><span data-stu-id="4fc32-175">C++ constant: **SE\_INC\_BASE\_PRIORITY\_NAME** string: **SeIncreaseBasePriorityPrivilege**</span></span>

<span data-ttu-id="4fc32-176">腳本簡短名稱： **IncreaseBasePriority**</span><span class="sxs-lookup"><span data-stu-id="4fc32-176">Scripting short name: **IncreaseBasePriority**</span></span>

<span data-ttu-id="4fc32-177">增加排程優先順序所需。</span><span class="sxs-lookup"><span data-stu-id="4fc32-177">Required to increase scheduling priority.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc32-178"><span id="wbemPrivilegeCreatePagefile"></span><span id="wbemprivilegecreatepagefile"></span><span id="WBEMPRIVILEGECREATEPAGEFILE"></span>**wbemPrivilegeCreatePagefile**</span><span class="sxs-lookup"><span data-stu-id="4fc32-178"><span id="wbemPrivilegeCreatePagefile"></span><span id="wbemprivilegecreatepagefile"></span><span id="WBEMPRIVILEGECREATEPAGEFILE"></span>**wbemPrivilegeCreatePagefile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc32-179">14 (0xE) </span><span class="sxs-lookup"><span data-stu-id="4fc32-179">14 (0xE)</span></span>
</dt> <dt>



<span data-ttu-id="4fc32-180">C + + 常數： **SE \_ 建立 \_ 分頁檔 \_ 名稱** 字串： **SeCreatePagefilePrivilege**</span><span class="sxs-lookup"><span data-stu-id="4fc32-180">C++ constant: **SE\_CREATE\_PAGEFILE\_NAME** string: **SeCreatePagefilePrivilege**</span></span>

<span data-ttu-id="4fc32-181">腳本簡短名稱： **CreatePagefile**</span><span class="sxs-lookup"><span data-stu-id="4fc32-181">Scripting short name: **CreatePagefile**</span></span>

<span data-ttu-id="4fc32-182">建立分頁檔所需。</span><span class="sxs-lookup"><span data-stu-id="4fc32-182">Required to create a pagefile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc32-183"><span id="wbemPrivilegeCreatePermanent"></span><span id="wbemprivilegecreatepermanent"></span><span id="WBEMPRIVILEGECREATEPERMANENT"></span>**wbemPrivilegeCreatePermanent**</span><span class="sxs-lookup"><span data-stu-id="4fc32-183"><span id="wbemPrivilegeCreatePermanent"></span><span id="wbemprivilegecreatepermanent"></span><span id="WBEMPRIVILEGECREATEPERMANENT"></span>**wbemPrivilegeCreatePermanent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc32-184">15 (0xF) </span><span class="sxs-lookup"><span data-stu-id="4fc32-184">15 (0xF)</span></span>
</dt> <dt>



<span data-ttu-id="4fc32-185">C + + 常數： **SE \_ 建立 \_ 永久 \_ 名稱** 字串： **SeCreatePermanentPrivilege**</span><span class="sxs-lookup"><span data-stu-id="4fc32-185">C++ constant: **SE\_CREATE\_PERMANENT\_NAME** string: **SeCreatePermanentPrivilege**</span></span>

<span data-ttu-id="4fc32-186">腳本簡短名稱： **CreatePermanent**</span><span class="sxs-lookup"><span data-stu-id="4fc32-186">Scripting short name: **CreatePermanent**</span></span>

<span data-ttu-id="4fc32-187">建立永久共用物件時所需。</span><span class="sxs-lookup"><span data-stu-id="4fc32-187">Required to create permanent shared objects.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc32-188"><span id="wbemPrivilegeBackup"></span><span id="wbemprivilegebackup"></span><span id="WBEMPRIVILEGEBACKUP"></span>**wbemPrivilegeBackup**</span><span class="sxs-lookup"><span data-stu-id="4fc32-188"><span id="wbemPrivilegeBackup"></span><span id="wbemprivilegebackup"></span><span id="WBEMPRIVILEGEBACKUP"></span>**wbemPrivilegeBackup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc32-189">16 (0x10) </span><span class="sxs-lookup"><span data-stu-id="4fc32-189">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="4fc32-190">C + + 常數： **SE \_ 備份 \_ 名稱** 字串： **SeBackupPrivilege**</span><span class="sxs-lookup"><span data-stu-id="4fc32-190">C++ constant: **SE\_BACKUP\_NAME** string: **SeBackupPrivilege**</span></span>

<span data-ttu-id="4fc32-191">腳本簡短名稱： **備份**</span><span class="sxs-lookup"><span data-stu-id="4fc32-191">Scripting short name: **Backup**</span></span>

<span data-ttu-id="4fc32-192">備份檔案和目錄的必要項，不論為檔案指定的 ACL 為何。</span><span class="sxs-lookup"><span data-stu-id="4fc32-192">Required to backup files and directories, regardless of the ACL specified for the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc32-193"><span id="wbemPrivilegeRestore"></span><span id="wbemprivilegerestore"></span><span id="WBEMPRIVILEGERESTORE"></span>**wbemPrivilegeRestore**</span><span class="sxs-lookup"><span data-stu-id="4fc32-193"><span id="wbemPrivilegeRestore"></span><span id="wbemprivilegerestore"></span><span id="WBEMPRIVILEGERESTORE"></span>**wbemPrivilegeRestore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc32-194">17 (0x11) </span><span class="sxs-lookup"><span data-stu-id="4fc32-194">17 (0x11)</span></span>
</dt> <dt>



<span data-ttu-id="4fc32-195">C + + 常數： **SE \_ 還原 \_ 名稱** 字串： **SeRestorePrivilege**</span><span class="sxs-lookup"><span data-stu-id="4fc32-195">C++ constant: **SE\_RESTORE\_NAME** string: **SeRestorePrivilege**</span></span>

<span data-ttu-id="4fc32-196">腳本簡短名稱： **還原**</span><span class="sxs-lookup"><span data-stu-id="4fc32-196">Scripting short name: **Restore**</span></span>

<span data-ttu-id="4fc32-197">還原檔案和目錄的必要項，不論為檔案指定的 ACL 為何。</span><span class="sxs-lookup"><span data-stu-id="4fc32-197">Required to restore files and directories, regardless of the ACL specified for the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc32-198"><span id="wbemPrivilegeShutdown"></span><span id="wbemprivilegeshutdown"></span><span id="WBEMPRIVILEGESHUTDOWN"></span>**wbemPrivilegeShutdown**</span><span class="sxs-lookup"><span data-stu-id="4fc32-198"><span id="wbemPrivilegeShutdown"></span><span id="wbemprivilegeshutdown"></span><span id="WBEMPRIVILEGESHUTDOWN"></span>**wbemPrivilegeShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc32-199">18 (0x12) </span><span class="sxs-lookup"><span data-stu-id="4fc32-199">18 (0x12)</span></span>
</dt> <dt>



<span data-ttu-id="4fc32-200">C + + 常數： **SE \_ 關閉 \_ 名稱** 字串： **SeShutdownPrivilege**</span><span class="sxs-lookup"><span data-stu-id="4fc32-200">C++ constant: **SE\_SHUTDOWN\_NAME** string: **SeShutdownPrivilege**</span></span>

<span data-ttu-id="4fc32-201">腳本簡短名稱： **關機**</span><span class="sxs-lookup"><span data-stu-id="4fc32-201">Scripting short name: **Shutdown**</span></span>

<span data-ttu-id="4fc32-202">關閉本機系統的必要參數。</span><span class="sxs-lookup"><span data-stu-id="4fc32-202">Required to shut down the local system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc32-203"><span id="wbemPrivilegeDebug"></span><span id="wbemprivilegedebug"></span><span id="WBEMPRIVILEGEDEBUG"></span>**wbemPrivilegeDebug**</span><span class="sxs-lookup"><span data-stu-id="4fc32-203"><span id="wbemPrivilegeDebug"></span><span id="wbemprivilegedebug"></span><span id="WBEMPRIVILEGEDEBUG"></span>**wbemPrivilegeDebug**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc32-204">19 (0x13) </span><span class="sxs-lookup"><span data-stu-id="4fc32-204">19 (0x13)</span></span>
</dt> <dt>



<span data-ttu-id="4fc32-205">C + + 常數： **SE \_ DEBUG \_ NAME** string： **SeDebugPrivilege**</span><span class="sxs-lookup"><span data-stu-id="4fc32-205">C++ constant: **SE\_DEBUG\_NAME** string: **SeDebugPrivilege**</span></span>

<span data-ttu-id="4fc32-206">腳本簡短名稱： **Debug**</span><span class="sxs-lookup"><span data-stu-id="4fc32-206">Scripting short name: **Debug**</span></span>

<span data-ttu-id="4fc32-207">需要對其他帳戶所擁有之進程的記憶體進行 debug 和調整。</span><span class="sxs-lookup"><span data-stu-id="4fc32-207">Required to debug and adjust the memory of a process owned by another account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc32-208"><span id="wbemPrivilegeAudit"></span><span id="wbemprivilegeaudit"></span><span id="WBEMPRIVILEGEAUDIT"></span>**wbemPrivilegeAudit**</span><span class="sxs-lookup"><span data-stu-id="4fc32-208"><span id="wbemPrivilegeAudit"></span><span id="wbemprivilegeaudit"></span><span id="WBEMPRIVILEGEAUDIT"></span>**wbemPrivilegeAudit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc32-209">20 (0x14) </span><span class="sxs-lookup"><span data-stu-id="4fc32-209">20 (0x14)</span></span>
</dt> <dt>



<span data-ttu-id="4fc32-210">C + + 常數： **SE \_ AUDIT \_ NAME** string： **SeAuditPrivilege**</span><span class="sxs-lookup"><span data-stu-id="4fc32-210">C++ constant: **SE\_AUDIT\_NAME** string: **SeAuditPrivilege**</span></span>

<span data-ttu-id="4fc32-211">腳本簡短名稱： **Audit**</span><span class="sxs-lookup"><span data-stu-id="4fc32-211">Scripting short name: **Audit**</span></span>

<span data-ttu-id="4fc32-212">在 NT 安全性記錄檔中產生 audit 專案的必要專案。</span><span class="sxs-lookup"><span data-stu-id="4fc32-212">Required to generate audit entries in the NT Security log.</span></span> <span data-ttu-id="4fc32-213">只有安全的伺服器才應該具有此許可權。</span><span class="sxs-lookup"><span data-stu-id="4fc32-213">Only secure servers should have this privilege.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc32-214"><span id="wbemPrivilegeSystemEnvironment"></span><span id="wbemprivilegesystemenvironment"></span><span id="WBEMPRIVILEGESYSTEMENVIRONMENT"></span>**wbemPrivilegeSystemEnvironment**</span><span class="sxs-lookup"><span data-stu-id="4fc32-214"><span id="wbemPrivilegeSystemEnvironment"></span><span id="wbemprivilegesystemenvironment"></span><span id="WBEMPRIVILEGESYSTEMENVIRONMENT"></span>**wbemPrivilegeSystemEnvironment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc32-215">21 (0x15) </span><span class="sxs-lookup"><span data-stu-id="4fc32-215">21 (0x15)</span></span>
</dt> <dt>



<span data-ttu-id="4fc32-216">C + + 常數： **SE \_ 系統 \_ 環境 \_ 名稱** 字串： **SeSystemEnvironmentPrivilege**</span><span class="sxs-lookup"><span data-stu-id="4fc32-216">C++ constant: **SE\_SYSTEM\_ENVIRONMENT\_NAME** string: **SeSystemEnvironmentPrivilege**</span></span>

<span data-ttu-id="4fc32-217">腳本簡短名稱： **SystemEnvironment**</span><span class="sxs-lookup"><span data-stu-id="4fc32-217">Scripting short name: **SystemEnvironment**</span></span>

<span data-ttu-id="4fc32-218">修改使用這種記憶體類型之系統的非靜態 RAM 來儲存設定資料時，需要用到。</span><span class="sxs-lookup"><span data-stu-id="4fc32-218">Required to modify the nonvolatile RAM of systems that use this type of memory to store configuration data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc32-219"><span id="wbemPrivilegeChangeNotify"></span><span id="wbemprivilegechangenotify"></span><span id="WBEMPRIVILEGECHANGENOTIFY"></span>**wbemPrivilegeChangeNotify**</span><span class="sxs-lookup"><span data-stu-id="4fc32-219"><span id="wbemPrivilegeChangeNotify"></span><span id="wbemprivilegechangenotify"></span><span id="WBEMPRIVILEGECHANGENOTIFY"></span>**wbemPrivilegeChangeNotify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc32-220">22 (0x16) </span><span class="sxs-lookup"><span data-stu-id="4fc32-220">22 (0x16)</span></span>
</dt> <dt>



<span data-ttu-id="4fc32-221">C + + 常數： **SE \_ 變更 \_ 通知 \_ 名稱** 字串： **SeChangeNotifyPrivilege**</span><span class="sxs-lookup"><span data-stu-id="4fc32-221">C++ constant: **SE\_CHANGE\_NOTIFY\_NAME** string: **SeChangeNotifyPrivilege**</span></span>

<span data-ttu-id="4fc32-222">腳本簡短名稱： **ChangeNotify**</span><span class="sxs-lookup"><span data-stu-id="4fc32-222">Scripting short name: **ChangeNotify**</span></span>

<span data-ttu-id="4fc32-223">需要接收檔案或目錄變更的通知，以及略過遍歷存取檢查。</span><span class="sxs-lookup"><span data-stu-id="4fc32-223">Required to receive notifications of changes to files or directories and bypass traversal access checks.</span></span> <span data-ttu-id="4fc32-224">依預設，所有使用者都會啟用此許可權。</span><span class="sxs-lookup"><span data-stu-id="4fc32-224">This privilege is enabled by default for all users.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc32-225"><span id="wbemPrivilegeRemoteShutdown"></span><span id="wbemprivilegeremoteshutdown"></span><span id="WBEMPRIVILEGEREMOTESHUTDOWN"></span>**wbemPrivilegeRemoteShutdown**</span><span class="sxs-lookup"><span data-stu-id="4fc32-225"><span id="wbemPrivilegeRemoteShutdown"></span><span id="wbemprivilegeremoteshutdown"></span><span id="WBEMPRIVILEGEREMOTESHUTDOWN"></span>**wbemPrivilegeRemoteShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc32-226">23 (0x17) </span><span class="sxs-lookup"><span data-stu-id="4fc32-226">23 (0x17)</span></span>
</dt> <dt>



<span data-ttu-id="4fc32-227">C + + 常數： **SE \_ 遠端 \_ 關閉 \_ 名稱** 字串： **SeRemoteShutdownPrivilege**</span><span class="sxs-lookup"><span data-stu-id="4fc32-227">C++ constant: **SE\_REMOTE\_SHUTDOWN\_NAME** string: **SeRemoteShutdownPrivilege**</span></span>

<span data-ttu-id="4fc32-228">腳本簡短名稱： **RemoteShutdown**</span><span class="sxs-lookup"><span data-stu-id="4fc32-228">Scripting short name: **RemoteShutdown**</span></span>

<span data-ttu-id="4fc32-229">關閉遠端電腦所需。</span><span class="sxs-lookup"><span data-stu-id="4fc32-229">Required to shut down a remote computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc32-230"><span id="wbemPrivilegeUndock"></span><span id="wbemprivilegeundock"></span><span id="WBEMPRIVILEGEUNDOCK"></span>**wbemPrivilegeUndock**</span><span class="sxs-lookup"><span data-stu-id="4fc32-230"><span id="wbemPrivilegeUndock"></span><span id="wbemprivilegeundock"></span><span id="WBEMPRIVILEGEUNDOCK"></span>**wbemPrivilegeUndock**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc32-231">24 (0x18) </span><span class="sxs-lookup"><span data-stu-id="4fc32-231">24 (0x18)</span></span>
</dt> <dt>



<span data-ttu-id="4fc32-232">C + + 常數： **SE \_ 移除 \_ 名稱** 字串： **SeUndockPrivilege**</span><span class="sxs-lookup"><span data-stu-id="4fc32-232">C++ constant: **SE\_UNDOCK\_NAME** string: **SeUndockPrivilege**</span></span>

<span data-ttu-id="4fc32-233">腳本簡短 **名稱：卸載**</span><span class="sxs-lookup"><span data-stu-id="4fc32-233">Scripting short name: **Undock**</span></span>

<span data-ttu-id="4fc32-234">從銜接站移除膝上型電腦的必要。</span><span class="sxs-lookup"><span data-stu-id="4fc32-234">Required to remove a laptop from a docking station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc32-235"><span id="wbemPrivilegeSyncAgent"></span><span id="wbemprivilegesyncagent"></span><span id="WBEMPRIVILEGESYNCAGENT"></span>**wbemPrivilegeSyncAgent**</span><span class="sxs-lookup"><span data-stu-id="4fc32-235"><span id="wbemPrivilegeSyncAgent"></span><span id="wbemprivilegesyncagent"></span><span id="WBEMPRIVILEGESYNCAGENT"></span>**wbemPrivilegeSyncAgent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc32-236">25 (0x19) </span><span class="sxs-lookup"><span data-stu-id="4fc32-236">25 (0x19)</span></span>
</dt> <dt>



<span data-ttu-id="4fc32-237">C + + 常數： **SE \_ 同步 \_ 代理程式 \_ 名稱** 字串： **SeSyncAgentPrivilege**</span><span class="sxs-lookup"><span data-stu-id="4fc32-237">C++ constant: **SE\_SYNC\_AGENT\_NAME** string: **SeSyncAgentPrivilege**</span></span>

<span data-ttu-id="4fc32-238">腳本簡短名稱： **SyncAgent**</span><span class="sxs-lookup"><span data-stu-id="4fc32-238">Scripting short name: **SyncAgent**</span></span>

<span data-ttu-id="4fc32-239">同步目錄服務資料所需。</span><span class="sxs-lookup"><span data-stu-id="4fc32-239">Required to synchronize directory service data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc32-240"><span id="wbemPrivilegeEnableDelegation"></span><span id="wbemprivilegeenabledelegation"></span><span id="WBEMPRIVILEGEENABLEDELEGATION"></span>**wbemPrivilegeEnableDelegation**</span><span class="sxs-lookup"><span data-stu-id="4fc32-240"><span id="wbemPrivilegeEnableDelegation"></span><span id="wbemprivilegeenabledelegation"></span><span id="WBEMPRIVILEGEENABLEDELEGATION"></span>**wbemPrivilegeEnableDelegation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc32-241">26 (0x1A) </span><span class="sxs-lookup"><span data-stu-id="4fc32-241">26 (0x1A)</span></span>
</dt> <dt>



<span data-ttu-id="4fc32-242">C + + 常數： **SE \_ 啟用 \_ 委派 \_ 名稱** 字串： **SeEnableDelegationPrivilege**</span><span class="sxs-lookup"><span data-stu-id="4fc32-242">C++ constant: **SE\_ENABLE\_DELEGATION\_NAME** string: **SeEnableDelegationPrivilege**</span></span>

<span data-ttu-id="4fc32-243">腳本簡短名稱： **EnableDelegation**</span><span class="sxs-lookup"><span data-stu-id="4fc32-243">Scripting short name: **EnableDelegation**</span></span>

<span data-ttu-id="4fc32-244">讓電腦和使用者帳戶受到信任以進行委派的必要。</span><span class="sxs-lookup"><span data-stu-id="4fc32-244">Required to enable computer and user accounts to be trusted for delegation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc32-245"><span id="wbemPrivilegeManageVolume"></span><span id="wbemprivilegemanagevolume"></span><span id="WBEMPRIVILEGEMANAGEVOLUME"></span>**wbemPrivilegeManageVolume**</span><span class="sxs-lookup"><span data-stu-id="4fc32-245"><span id="wbemPrivilegeManageVolume"></span><span id="wbemprivilegemanagevolume"></span><span id="WBEMPRIVILEGEMANAGEVOLUME"></span>**wbemPrivilegeManageVolume**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc32-246">27 (0x1B) </span><span class="sxs-lookup"><span data-stu-id="4fc32-246">27 (0x1B)</span></span>
</dt> <dt>



<span data-ttu-id="4fc32-247">C + + 常數： **SE \_ 管理 \_ 磁片區 \_ 名稱** 字串： **SeManageVolumePrivilege**</span><span class="sxs-lookup"><span data-stu-id="4fc32-247">C++ constant: **SE\_MANAGE\_VOLUME\_NAME** string: **SeManageVolumePrivilege**</span></span>

<span data-ttu-id="4fc32-248">腳本簡短名稱： **ManageVolume**</span><span class="sxs-lookup"><span data-stu-id="4fc32-248">Scripting short name: **ManageVolume**</span></span>

<span data-ttu-id="4fc32-249">執行磁片區維護工作的必要作業。</span><span class="sxs-lookup"><span data-stu-id="4fc32-249">Required to perform volume maintenance tasks.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4fc32-250">規格需求</span><span class="sxs-lookup"><span data-stu-id="4fc32-250">Requirements</span></span>



| <span data-ttu-id="4fc32-251">需求</span><span class="sxs-lookup"><span data-stu-id="4fc32-251">Requirement</span></span> | <span data-ttu-id="4fc32-252">值</span><span class="sxs-lookup"><span data-stu-id="4fc32-252">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4fc32-253">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4fc32-253">Minimum supported client</span></span><br/> | <span data-ttu-id="4fc32-254">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4fc32-254">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4fc32-255">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4fc32-255">Minimum supported server</span></span><br/> | <span data-ttu-id="4fc32-256">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4fc32-256">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4fc32-257">標頭</span><span class="sxs-lookup"><span data-stu-id="4fc32-257">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fc32-258"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="4fc32-258"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4fc32-259">Idl</span><span class="sxs-lookup"><span data-stu-id="4fc32-259">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4fc32-260"><dt>>wbemdisp.tlb .idl</dt></span><span class="sxs-lookup"><span data-stu-id="4fc32-260"><dt>Wbemdisp.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fc32-261">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4fc32-261">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fc32-262">腳本 API 常數</span><span class="sxs-lookup"><span data-stu-id="4fc32-262">Scripting API Constants</span></span>](scripting-api-constants.md)
</dt> <dt>

[<span data-ttu-id="4fc32-263">**SWbemSecurity**</span><span class="sxs-lookup"><span data-stu-id="4fc32-263">**SWbemSecurity**</span></span>](swbemsecurity.md)
</dt> <dt>

[<span data-ttu-id="4fc32-264">**WbemPrivilegeEnum**</span><span class="sxs-lookup"><span data-stu-id="4fc32-264">**WbemPrivilegeEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[<span data-ttu-id="4fc32-265">執行具有特殊許可權的作業</span><span class="sxs-lookup"><span data-stu-id="4fc32-265">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="4fc32-266">使用 VBScript 執行特殊許可權作業</span><span class="sxs-lookup"><span data-stu-id="4fc32-266">Executing Privileged Operations Using VBScript</span></span>](executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 


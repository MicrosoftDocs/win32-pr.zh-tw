---
description: 將電腦系統加入網域或工作組。
ms.assetid: b9421f04-9b56-4413-af5c-12dffeb6f0c8
ms.tgt_platform: multiple
title: Win32_ComputerSystem 類別的 JoinDomainOrWorkgroup 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem.JoinDomainOrWorkgroup
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 927dd6b2664c92ff07e94407fdc59fdd917363dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847495"
---
# <a name="joindomainorworkgroup-method-of-the-win32_computersystem-class"></a><span data-ttu-id="8ece1-103">Win32 JoinDomainOrWorkgroup 類別的方法 \_</span><span class="sxs-lookup"><span data-stu-id="8ece1-103">JoinDomainOrWorkgroup method of the Win32\_ComputerSystem class</span></span>

<span data-ttu-id="8ece1-104">**JoinDomainOrWorkgroup** 方法會將電腦系統加入網域或工作組。</span><span class="sxs-lookup"><span data-stu-id="8ece1-104">The **JoinDomainOrWorkgroup** method joins a computer system to a domain or workgroup.</span></span>

<span data-ttu-id="8ece1-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="8ece1-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8ece1-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="8ece1-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8ece1-107">語法</span><span class="sxs-lookup"><span data-stu-id="8ece1-107">Syntax</span></span>


```mof
uint32 JoinDomainOrWorkgroup(
  [in] string Name,
  [in] string Password,
  [in] string UserName,
  [in] string AccountOU,
  [in] uint32 FJoinOptions = 
);
```



## <a name="parameters"></a><span data-ttu-id="8ece1-108">參數</span><span class="sxs-lookup"><span data-stu-id="8ece1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ece1-109">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8ece1-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ece1-110">指定要加入的網域或工作組。</span><span class="sxs-lookup"><span data-stu-id="8ece1-110">Specifies the domain or workgroup to join.</span></span> <span data-ttu-id="8ece1-111">不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8ece1-111">Cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8ece1-112">*密碼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8ece1-112">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ece1-113">如果 *UserName* 參數指定帳戶名稱， *password* 參數必須指向連接到網域控制站時要使用的密碼。</span><span class="sxs-lookup"><span data-stu-id="8ece1-113">If the *UserName* parameter specifies an account name, the *Password* parameter must point to the password to use when connecting to the domain controller.</span></span> <span data-ttu-id="8ece1-114">否則，此參數必須為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8ece1-114">Otherwise, this parameter must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8ece1-115">使用者 *名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8ece1-115">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ece1-116">指向以 **null** 終止的常數位符串指標，指定連接到網域控制站時要使用的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="8ece1-116">Pointer to a constant **null**-terminated character string that specifies the account name to use when connecting to the domain controller.</span></span> <span data-ttu-id="8ece1-117">必須指定網域 NetBIOS 名稱和使用者帳戶，例如網域 \\ 使用者。</span><span class="sxs-lookup"><span data-stu-id="8ece1-117">Must specify a domain NetBIOS name and user account, for example, Domain\\user.</span></span> <span data-ttu-id="8ece1-118">如果此參數為 **Null**，則會使用呼叫端資訊。</span><span class="sxs-lookup"><span data-stu-id="8ece1-118">If this parameter is **NULL**, the caller information is used.</span></span>

<span data-ttu-id="8ece1-119">您也可以在表單中使用使用者主體名稱 (UPPED) user@domain 。</span><span class="sxs-lookup"><span data-stu-id="8ece1-119">You can also use the user principal name (UPPED) in the form user@domain.</span></span>

</dd> <dt>

<span data-ttu-id="8ece1-120">*AccountOU* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8ece1-120">*AccountOU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ece1-121">指定常數以 **null** 終止的字元字串指標，其中包含電腦帳戶 (OU) 之組織單位的 [RFC 1779](https://www.ietf.org/rfc/rfc1779.txt) 格式名稱。</span><span class="sxs-lookup"><span data-stu-id="8ece1-121">Specifies the pointer to a constant **null**-terminated character string that contains the [RFC 1779](https://www.ietf.org/rfc/rfc1779.txt) format name of the organizational unit (OU) for the computer account.</span></span> <span data-ttu-id="8ece1-122">如果您指定這個參數，字串就必須包含完整的路徑，否則 *輔色* 必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8ece1-122">If you specify this parameter, the string must contain a full path, otherwise *Accent* must be **NULL**.</span></span>

<span data-ttu-id="8ece1-123">範例： "OU = testOU;DC = 網域;DC = 網域;DC = com "</span><span class="sxs-lookup"><span data-stu-id="8ece1-123">Example: "OU=testOU; DC=domain; DC=Domain; DC=com"</span></span>

</dd> <dt>

<span data-ttu-id="8ece1-124">*Joindomainorworkgroup* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8ece1-124">*FJoinOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ece1-125">定義聯結選項的位旗標集合。</span><span class="sxs-lookup"><span data-stu-id="8ece1-125">Set of bit flags that define the join options.</span></span>

<dt>



 <span data-ttu-id="8ece1-126"> (0)</span><span class="sxs-lookup"><span data-stu-id="8ece1-126">(0)</span></span>


</dt> <dd>

<span data-ttu-id="8ece1-127">預設值。</span><span class="sxs-lookup"><span data-stu-id="8ece1-127">Default.</span></span> <span data-ttu-id="8ece1-128">沒有聯結選項。</span><span class="sxs-lookup"><span data-stu-id="8ece1-128">No join options.</span></span>

</dd> <dt>

<span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>

<span data-ttu-id="8ece1-129"><span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>**NETSETUP \_加入 \_ 網域** (0x00000001) </span><span class="sxs-lookup"><span data-stu-id="8ece1-129"><span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>**NETSETUP\_JOIN\_DOMAIN** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="8ece1-130">將電腦加入網域。</span><span class="sxs-lookup"><span data-stu-id="8ece1-130">Joins the computer to a domain.</span></span> <span data-ttu-id="8ece1-131">如果未指定此值，則會將電腦加入工作組。</span><span class="sxs-lookup"><span data-stu-id="8ece1-131">If this value is not specified, joins the computer to a workgroup.</span></span>

</dd> <dt>

<span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>

<span data-ttu-id="8ece1-132"><span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>**NETSETUP \_\_建立** (0x00000002) 的帳戶</span><span class="sxs-lookup"><span data-stu-id="8ece1-132"><span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>**NETSETUP\_ACCT\_CREATE** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="8ece1-133">在網域上建立帳戶。</span><span class="sxs-lookup"><span data-stu-id="8ece1-133">Creates the account on the domain.</span></span>

</dd> <dt>

<span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>

<span data-ttu-id="8ece1-134"><span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>**NETSETUP \_ (\_** 0x00000010) 的 WIN9X 升級</span><span class="sxs-lookup"><span data-stu-id="8ece1-134"><span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>**NETSETUP\_WIN9X\_UPGRADE** (0x00000010)</span></span>


</dt> <dd>

<span data-ttu-id="8ece1-135">聯結作業會在升級過程中發生。</span><span class="sxs-lookup"><span data-stu-id="8ece1-135">The join operation is occurring as part of an upgrade.</span></span>

</dd> <dt>

<span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>

<span data-ttu-id="8ece1-136"><span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>**NETSETUP \_\_ \_ \_ 加入** (0x00000020 的網域聯結) </span><span class="sxs-lookup"><span data-stu-id="8ece1-136"><span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>**NETSETUP\_DOMAIN\_JOIN\_IF\_JOINED** (0x00000020)</span></span>


</dt> <dd>

<span data-ttu-id="8ece1-137">即使電腦已經加入網域，也允許加入新網域。</span><span class="sxs-lookup"><span data-stu-id="8ece1-137">Allows a join to a new domain even if the computer is already joined to a domain.</span></span>

</dd> <dt>

<span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>

<span data-ttu-id="8ece1-138"><span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>**NETSETUP \_加入不 \_ 安全** 的 (0x00000040) </span><span class="sxs-lookup"><span data-stu-id="8ece1-138"><span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>**NETSETUP\_JOIN\_UNSECURE** (0x00000040)</span></span>


</dt> <dd>

<span data-ttu-id="8ece1-139">執行非安全性加入。</span><span class="sxs-lookup"><span data-stu-id="8ece1-139">Performs an unsecured join.</span></span>

<span data-ttu-id="8ece1-140">此選項會向預先建立的帳戶要求加入網域，而不需使用網域使用者認證進行驗證。</span><span class="sxs-lookup"><span data-stu-id="8ece1-140">This option requests a domain join to a pre-created account without authenticating with domain user credentials.</span></span> <span data-ttu-id="8ece1-141">此選項可與 **NETSETUP \_ MACHINE \_ PWD \_ 傳遞** 的選項搭配使用。</span><span class="sxs-lookup"><span data-stu-id="8ece1-141">This option can be used in conjunction with **NETSETUP\_MACHINE\_PWD\_PASSED** option.</span></span> <span data-ttu-id="8ece1-142">在此情況下， *password* 是預先建立之電腦帳戶的密碼。</span><span class="sxs-lookup"><span data-stu-id="8ece1-142">In this case, *Password* is the password of the pre-created machine account.</span></span>

<span data-ttu-id="8ece1-143">在 Windows Vista （含 SP1）和 Windows Server 2008 之前，不安全的聯結不會驗證網域控制站。</span><span class="sxs-lookup"><span data-stu-id="8ece1-143">Prior to Windows Vista with SP1 and Windows Server 2008, an unsecure join did not authenticate to the domain controller.</span></span> <span data-ttu-id="8ece1-144">所有通訊都是使用 null (未經驗證的) 會話來執行。</span><span class="sxs-lookup"><span data-stu-id="8ece1-144">All communication was performed using a null (unauthenticated) session.</span></span> <span data-ttu-id="8ece1-145">從 Windows Vista SP1 和 Windows Server 2008 開始，電腦帳戶名稱和密碼會用來驗證網域控制站。</span><span class="sxs-lookup"><span data-stu-id="8ece1-145">Starting with Windows Vista with SP1 and Windows Server 2008, the machine account name and password are used to authenticate to the domain controller.</span></span>

</dd> <dt>

<span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>

<span data-ttu-id="8ece1-146"><span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>**NETSETUP \_電腦 \_ PWD 已 \_ 通過** (0x00000080) </span><span class="sxs-lookup"><span data-stu-id="8ece1-146"><span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>**NETSETUP\_MACHINE\_PWD\_PASSED** (0x00000080)</span></span>


</dt> <dd>

<span data-ttu-id="8ece1-147">指出 *password* 參數指定本機電腦帳戶密碼，而不是使用者密碼。</span><span class="sxs-lookup"><span data-stu-id="8ece1-147">Indicates that the *Password* parameter specifies a local machine account password rather than a user password.</span></span> <span data-ttu-id="8ece1-148">此旗標只適用于不安全的聯結，您也必須設定 NETSETUP 聯結不 \_ 安全旗標來指出此旗標 \_ 。</span><span class="sxs-lookup"><span data-stu-id="8ece1-148">This flag is valid only for unsecured joins, which you must indicate by also setting the NETSETUP\_JOIN\_UNSECURE flag.</span></span>

<span data-ttu-id="8ece1-149">如果設定此旗標，則在聯結作業成功之後，如果該值為有效的電腦密碼，電腦密碼將會設定為 [ *密碼*] 的值。</span><span class="sxs-lookup"><span data-stu-id="8ece1-149">If you set this flag, then after the join operation succeeds, the machine password will be set to the value of *Password*, if that value is a valid machine password.</span></span>

</dd> <dt>

<span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>

<span data-ttu-id="8ece1-150"><span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>**NETSETUP \_延遲 \_ SPN \_ 設定** (0x00000100) </span><span class="sxs-lookup"><span data-stu-id="8ece1-150"><span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>**NETSETUP\_DEFER\_SPN\_SET** (0x00000100)</span></span>


</dt> <dd>

<span data-ttu-id="8ece1-151">指出服務主體名稱 (SPN) ，而且電腦物件上的 DnsHostName 屬性目前不應更新。</span><span class="sxs-lookup"><span data-stu-id="8ece1-151">Indicates that the service principal name (SPN) and the DnsHostName properties on the computer object should not be updated at this time.</span></span>

<span data-ttu-id="8ece1-152">一般而言，這些屬性會在聯結操作期間更新。</span><span class="sxs-lookup"><span data-stu-id="8ece1-152">Typically, these properties are updated during the join operation.</span></span> <span data-ttu-id="8ece1-153">相反地，您應該在後續呼叫 [**重新命名**](rename-method-in-class-win32-computersystem.md) 方法時更新這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8ece1-153">Instead, these properties should be updated during a subsequent call to the [**Rename**](rename-method-in-class-win32-computersystem.md) method.</span></span> <span data-ttu-id="8ece1-154">在重新命名作業期間，一律會更新這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8ece1-154">These properties are always updated during the rename operation.</span></span>

</dd> <dt>

<span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>

<span data-ttu-id="8ece1-155"><span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>**NETSETUP \_加入 \_ DC \_ 帳戶** (0x00000200) </span><span class="sxs-lookup"><span data-stu-id="8ece1-155"><span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>**NETSETUP\_JOIN\_DC\_ACCOUNT** (0x00000200)</span></span>


</dt> <dd>

<span data-ttu-id="8ece1-156">如果現有的帳戶是網域控制站，則允許加入網域。</span><span class="sxs-lookup"><span data-stu-id="8ece1-156">Allow the domain join if existing account is a domain controller.</span></span>

> [!Note]  
> <span data-ttu-id="8ece1-157">Windows Vista 及更新版本支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="8ece1-157">This flag is supported on Windows Vista and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>

<span data-ttu-id="8ece1-158"><span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>**NETSETUP \_不明確的 \_ DC** (0x00001000) </span><span class="sxs-lookup"><span data-stu-id="8ece1-158"><span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>**NETSETUP\_AMBIGUOUS\_DC** (0x00001000)</span></span>


</dt> <dd>

<span data-ttu-id="8ece1-159">加入網域時，請勿嘗試在登錄中設定慣用的網域控制站。</span><span class="sxs-lookup"><span data-stu-id="8ece1-159">When joining the domain don't try to set the preferred domain controller in the registry.</span></span>

> [!Note]  
> <span data-ttu-id="8ece1-160">Windows 7、Windows Server 2008 R2 及更新版本支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="8ece1-160">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>

<span data-ttu-id="8ece1-161"><span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>**NETSETUP \_沒有 \_ NETLOGON \_** 快取 (0x00002000) </span><span class="sxs-lookup"><span data-stu-id="8ece1-161"><span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>**NETSETUP\_NO\_NETLOGON\_CACHE** (0x00002000)</span></span>


</dt> <dd>

<span data-ttu-id="8ece1-162">加入網域時，不要建立 Netlogon 快取。</span><span class="sxs-lookup"><span data-stu-id="8ece1-162">When joining the domain don't create the Netlogon cache.</span></span>

> [!Note]  
> <span data-ttu-id="8ece1-163">Windows 7、Windows Server 2008 R2 及更新版本支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="8ece1-163">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>

<span data-ttu-id="8ece1-164"><span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>**NETSETUP \_不要 \_ 控制 \_ 服務** (0x00004000) </span><span class="sxs-lookup"><span data-stu-id="8ece1-164"><span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>**NETSETUP\_DONT\_CONTROL\_SERVICES** (0x00004000)</span></span>


</dt> <dd>

<span data-ttu-id="8ece1-165">加入網域時，不會強制啟動 Netlogon 服務。</span><span class="sxs-lookup"><span data-stu-id="8ece1-165">When joining the domain don't force Netlogon service to start.</span></span>

> [!Note]  
> <span data-ttu-id="8ece1-166">Windows 7、Windows Server 2008 R2 及更新版本支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="8ece1-166">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>

<span data-ttu-id="8ece1-167"><span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>**NETSETUP \_設定 \_ 電腦 \_ 名稱** (0x00008000) </span><span class="sxs-lookup"><span data-stu-id="8ece1-167"><span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>**NETSETUP\_SET\_MACHINE\_NAME** (0x00008000)</span></span>


</dt> <dd>

<span data-ttu-id="8ece1-168">加入網域以進行離線聯結時，請設定目的電腦主機名稱和 NetBIOS 名稱。</span><span class="sxs-lookup"><span data-stu-id="8ece1-168">When joining the domain for offline join only, set target machine hostname and NetBIOS name.</span></span>

> [!Note]  
> <span data-ttu-id="8ece1-169">Windows 7、Windows Server 2008 R2 及更新版本支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="8ece1-169">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>

<span data-ttu-id="8ece1-170"><span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>**NETSETUP \_強制 \_ SPN \_ 設定** (0x00010000) </span><span class="sxs-lookup"><span data-stu-id="8ece1-170"><span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>**NETSETUP\_FORCE\_SPN\_SET** (0x00010000)</span></span>


</dt> <dd>

<span data-ttu-id="8ece1-171">加入網域時，請在加入網域時覆寫其他設定，並將服務主體名稱設 (SPN) 。</span><span class="sxs-lookup"><span data-stu-id="8ece1-171">When joining the domain, override other settings during domain join and set the service principal name (SPN).</span></span>

> [!Note]  
> <span data-ttu-id="8ece1-172">Windows 7、Windows Server 2008 R2 及更新版本支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="8ece1-172">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>

<span data-ttu-id="8ece1-173"><span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>**NETSETUP \_沒有任何 (0x00020000 的 \_ 帳戶 \_ 重複使用**) </span><span class="sxs-lookup"><span data-stu-id="8ece1-173"><span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>**NETSETUP\_NO\_ACCT\_REUSE** (0x00020000)</span></span>


</dt> <dd>

<span data-ttu-id="8ece1-174">加入網域時，請勿重複使用現有的帳戶。</span><span class="sxs-lookup"><span data-stu-id="8ece1-174">When joining the domain, do not reuse an existing account.</span></span>

> [!Note]  
> <span data-ttu-id="8ece1-175">Windows 7、Windows Server 2008 R2 及更新版本支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="8ece1-175">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>

<span data-ttu-id="8ece1-176"><span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>**NETSETUP \_略過 \_ 不支援的 \_ 旗標** (0x10000000) </span><span class="sxs-lookup"><span data-stu-id="8ece1-176"><span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>**NETSETUP\_IGNORE\_UNSUPPORTED\_FLAGS** (0x10000000)</span></span>


</dt> <dd>

<span data-ttu-id="8ece1-177">如果設定此位， **JoinDomainOrWorkgroup** 函式將會忽略無法辨識的旗標，且 [**NetJoinDomain**](/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain) 的行為會如同未設定旗標。</span><span class="sxs-lookup"><span data-stu-id="8ece1-177">If this bit is set, unrecognized flags will be ignored by the **JoinDomainOrWorkgroup** function and [**NetJoinDomain**](/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain) will behave as if the flags were not set.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ece1-178">傳回值</span><span class="sxs-lookup"><span data-stu-id="8ece1-178">Return value</span></span>

<span data-ttu-id="8ece1-179">傳回 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)，此錯誤碼可能包含下列其中一個數值。</span><span class="sxs-lookup"><span data-stu-id="8ece1-179">Returns a [system error code](/windows/desktop/Debug/system-error-codes), which may include one of the following numeric values.</span></span> <span data-ttu-id="8ece1-180">任何其他數字表示發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="8ece1-180">Any other number indicates an error.</span></span> <span data-ttu-id="8ece1-181">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="8ece1-181">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

<dl> <dt>

<span data-ttu-id="8ece1-182">「成功」</span><span class="sxs-lookup"><span data-stu-id="8ece1-182">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="8ece1-183">0</span><span class="sxs-lookup"><span data-stu-id="8ece1-183">0</span></span>

</dd> <dt>

<span data-ttu-id="8ece1-184">**5**</span><span class="sxs-lookup"><span data-stu-id="8ece1-184">**5**</span></span>
</dt> <dd>

<span data-ttu-id="8ece1-185">存取遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="8ece1-185">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="8ece1-186">**87**</span><span class="sxs-lookup"><span data-stu-id="8ece1-186">**87**</span></span>
</dt> <dd>

<span data-ttu-id="8ece1-187">參數錯誤。</span><span class="sxs-lookup"><span data-stu-id="8ece1-187">The parameter is incorrect.</span></span>

</dd> <dt>

<span data-ttu-id="8ece1-188">**110**</span><span class="sxs-lookup"><span data-stu-id="8ece1-188">**110**</span></span>
</dt> <dd>

<span data-ttu-id="8ece1-189">他的系統無法開啟指定的物件。</span><span class="sxs-lookup"><span data-stu-id="8ece1-189">he system cannot open the specified object.</span></span>

</dd> <dt>

<span data-ttu-id="8ece1-190">**1323**</span><span class="sxs-lookup"><span data-stu-id="8ece1-190">**1323**</span></span>
</dt> <dd>

<span data-ttu-id="8ece1-191">無法更新密碼。</span><span class="sxs-lookup"><span data-stu-id="8ece1-191">Unable to update the password.</span></span>

</dd> <dt>

<span data-ttu-id="8ece1-192">**1326**</span><span class="sxs-lookup"><span data-stu-id="8ece1-192">**1326**</span></span>
</dt> <dd>

<span data-ttu-id="8ece1-193">登入失敗：未知的使用者名稱或密碼不正確。</span><span class="sxs-lookup"><span data-stu-id="8ece1-193">Logon failure: unknown username or bad password.</span></span>

</dd> <dt>

<span data-ttu-id="8ece1-194">**1355**</span><span class="sxs-lookup"><span data-stu-id="8ece1-194">**1355**</span></span>
</dt> <dd>

<span data-ttu-id="8ece1-195">指定的網域可能不存在或無法連絡。</span><span class="sxs-lookup"><span data-stu-id="8ece1-195">The specified domain either does not exist or could not be contacted.</span></span>

</dd> <dt>

<span data-ttu-id="8ece1-196">**2224**</span><span class="sxs-lookup"><span data-stu-id="8ece1-196">**2224**</span></span>
</dt> <dd>

<span data-ttu-id="8ece1-197">帳戶已存在。</span><span class="sxs-lookup"><span data-stu-id="8ece1-197">The account already exists.</span></span>

</dd> <dt>

<span data-ttu-id="8ece1-198">**2691**</span><span class="sxs-lookup"><span data-stu-id="8ece1-198">**2691**</span></span>
</dt> <dd>

<span data-ttu-id="8ece1-199">電腦已加入網域。</span><span class="sxs-lookup"><span data-stu-id="8ece1-199">The machine is already joined to the domain.</span></span>

</dd> <dt>

<span data-ttu-id="8ece1-200">**2692**</span><span class="sxs-lookup"><span data-stu-id="8ece1-200">**2692**</span></span>
</dt> <dd>

<span data-ttu-id="8ece1-201">電腦目前未加入網域。</span><span class="sxs-lookup"><span data-stu-id="8ece1-201">The machine is not currently joined to a domain.</span></span>

</dd> <dt>

<span data-ttu-id="8ece1-202">**\_需要 WBEM E \_ 加密 \_ 連接 \_**</span><span class="sxs-lookup"><span data-stu-id="8ece1-202">**WBEM\_E\_ENCRYPTED\_CONNECTION\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="8ece1-203">0x80041087</span><span class="sxs-lookup"><span data-stu-id="8ece1-203">0x80041087</span></span>

<span data-ttu-id="8ece1-204">已指定 *密碼* 和使用者 *名稱*，但驗證層級不是 **RPC \_ C \_ 驗證 \_ level \_ PKT \_ 隱私權**。</span><span class="sxs-lookup"><span data-stu-id="8ece1-204">*Password* and *UserName* are specified but the authentication level is not **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="8ece1-205">若為 Visual Basic，則會傳回 **wbemErrEncryptedConnectionRequired** 。</span><span class="sxs-lookup"><span data-stu-id="8ece1-205">For Visual Basic, **wbemErrEncryptedConnectionRequired** is returned.</span></span>

</dd> <dt>

<span data-ttu-id="8ece1-206">**其他**</span><span class="sxs-lookup"><span data-stu-id="8ece1-206">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="8ece1-207">1 4294967295</span><span class="sxs-lookup"><span data-stu-id="8ece1-207">1 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8ece1-208">備註</span><span class="sxs-lookup"><span data-stu-id="8ece1-208">Remarks</span></span>

<span data-ttu-id="8ece1-209">當您將電腦從網域移到工作組時，必須先呼叫 [**UnjoinDomainOrWorkgroup**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)) ，將電腦從網域 (移除，然後再呼叫這個方法，將工作組 (與 **JoinDomainOrWorkgroup**) 的呼叫聯結。</span><span class="sxs-lookup"><span data-stu-id="8ece1-209">When moving a computer from a domain to a workgroup, you must remove the computer from the domain (with a call to [**UnjoinDomainOrWorkgroup**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)) before calling this method to join a workgroup (with a call to **JoinDomainOrWorkgroup**).</span></span> <span data-ttu-id="8ece1-210">呼叫此方法之後，請重新開機受影響的電腦以套用變更。</span><span class="sxs-lookup"><span data-stu-id="8ece1-210">After calling this method, restart the affected computer to apply the changes.</span></span>

<span data-ttu-id="8ece1-211">使用者 *名稱* 和 *密碼* 可以保留 **null**。</span><span class="sxs-lookup"><span data-stu-id="8ece1-211">*UserName* and *Password* can be left **null**.</span></span> <span data-ttu-id="8ece1-212">不過，在 Visual Basic 的腳本或 **WbemAuthenticationLevelPktPrivacy** 中，對 WMI 的連線驗證必須是6，而且可以使用 [wbemdisp.dll](/windows/desktop/WmiSdk/using-the-wmi-scripting-type-library) 程式庫的其他語言。</span><span class="sxs-lookup"><span data-stu-id="8ece1-212">However, the authentication of the connection to WMI must be 6 in script or **WbemAuthenticationLevelPktPrivacy** in Visual Basic and other languages that can use the [wbemdisp.dll](/windows/desktop/WmiSdk/using-the-wmi-scripting-type-library) library.</span></span> <span data-ttu-id="8ece1-213">如需詳細資訊，請參閱 [使用 VBScript 設定預設進程安全性層級](/windows/desktop/WmiSdk/setting-the-default-process-security-level-using-vbscript)。</span><span class="sxs-lookup"><span data-stu-id="8ece1-213">For more information, see [Setting the Default Process Security Level Using VBScript](/windows/desktop/WmiSdk/setting-the-default-process-security-level-using-vbscript).</span></span>

<span data-ttu-id="8ece1-214">在 c + + 中，在 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)、整個進程或 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)中，針對 [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) proxy 的連接，設定 **RPC \_ C \_ 驗證 \_ 層級 \_ PKT \_ 隱私權** 的驗證。</span><span class="sxs-lookup"><span data-stu-id="8ece1-214">In C++, set the authentication at **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** either in [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), for the entire process, or in [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket), for a connection to the [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) proxy.</span></span> <span data-ttu-id="8ece1-215">如需詳細資訊，請參閱 [使用 c + + 設定驗證](/windows/desktop/WmiSdk/setting-authentication-using-c-) 和 [設定 IWbemServices 和其他 proxy 的安全性](/windows/desktop/WmiSdk/setting-the-security-on-iwbemservices-and-other-proxies)。</span><span class="sxs-lookup"><span data-stu-id="8ece1-215">For more information, see [Setting Authentication Using C++](/windows/desktop/WmiSdk/setting-authentication-using-c-) and [Setting the Security on IWbemServices and Other Proxies](/windows/desktop/WmiSdk/setting-the-security-on-iwbemservices-and-other-proxies).</span></span>

## <a name="examples"></a><span data-ttu-id="8ece1-216">範例</span><span class="sxs-lookup"><span data-stu-id="8ece1-216">Examples</span></span>

<span data-ttu-id="8ece1-217">將 [電腦加入網域](https://Gallery.TechNet.Microsoft.Com/Join-a-computer-to-a-domain-6e19d905) PowerShell 範例會將電腦加入網域。</span><span class="sxs-lookup"><span data-stu-id="8ece1-217">The [Join a computer to a domain](https://Gallery.TechNet.Microsoft.Com/Join-a-computer-to-a-domain-6e19d905) PowerShell example joins a computer to a domain.</span></span>

<span data-ttu-id="8ece1-218">下列 VBScript 程式碼範例會將電腦加入網域，並在 Active Directory 中建立電腦的帳戶。</span><span class="sxs-lookup"><span data-stu-id="8ece1-218">The following VBScript code example joins a computer to a domain and creates the computer's account in Active Directory.</span></span>


```VB
Const JOIN_DOMAIN             = 1
Const ACCT_CREATE             = 2
Const ACCT_DELETE             = 4
Const WIN9X_UPGRADE           = 16
Const DOMAIN_JOIN_IF_JOINED   = 32
Const JOIN_UNSECURE           = 64
Const MACHINE_PASSWORD_PASSED = 128
Const DEFERRED_SPN_SET        = 256
Const INSTALL_INVOCATION      = 262144
strDomain   = "FABRIKAM"
strPassword = "ls4k5ywA"
strUser     = "shenalan"
Set objNetwork = CreateObject("WScript.Network")
strComputer = objNetwork.ComputerName
Set objComputer = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" & strComputer & _
                            "\root\cimv2:Win32_ComputerSystem.Name='" & strComputer & "'")
ReturnValue = objComputer.JoinDomainOrWorkGroup(strDomain, _
                                                strPassword, _
                                                strDomain & "\" & strUser, _
                                                NULL, _
                                                JOIN_DOMAIN + ACCT_CREATE)
```



## <a name="requirements"></a><span data-ttu-id="8ece1-219">規格需求</span><span class="sxs-lookup"><span data-stu-id="8ece1-219">Requirements</span></span>



| <span data-ttu-id="8ece1-220">需求</span><span class="sxs-lookup"><span data-stu-id="8ece1-220">Requirement</span></span> | <span data-ttu-id="8ece1-221">值</span><span class="sxs-lookup"><span data-stu-id="8ece1-221">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ece1-222">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8ece1-222">Minimum supported client</span></span><br/> | <span data-ttu-id="8ece1-223">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8ece1-223">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8ece1-224">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8ece1-224">Minimum supported server</span></span><br/> | <span data-ttu-id="8ece1-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8ece1-225">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8ece1-226">命名空間</span><span class="sxs-lookup"><span data-stu-id="8ece1-226">Namespace</span></span><br/>                | <span data-ttu-id="8ece1-227">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8ece1-227">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8ece1-228">MOF</span><span class="sxs-lookup"><span data-stu-id="8ece1-228">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8ece1-229"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="8ece1-229"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8ece1-230">DLL</span><span class="sxs-lookup"><span data-stu-id="8ece1-230">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ece1-231"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ece1-231"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ece1-232">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8ece1-232">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ece1-233">**Win32 \_ 未進行**</span><span class="sxs-lookup"><span data-stu-id="8ece1-233">**Win32\_ComputerSystem**</span></span>](win32-computersystem.md)
</dt> <dt>

[<span data-ttu-id="8ece1-234">**UnjoinDomainOrWorkgroup 方法**</span><span class="sxs-lookup"><span data-stu-id="8ece1-234">**UnjoinDomainOrWorkgroup method**</span></span>](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)
</dt> </dl>

 


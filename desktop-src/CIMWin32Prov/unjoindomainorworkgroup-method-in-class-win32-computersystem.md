---
description: 從網域或工作組移除電腦系統。
ms.assetid: 79ee177e-81e2-441b-b39a-2fb53a0145bf
ms.tgt_platform: multiple
title: Win32_ComputerSystem 類別的 UnjoinDomainOrWorkgroup 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem.UnjoinDomainOrWorkgroup
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1c6942c5367b6deb02accd9d06927a4d923fa8f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847532"
---
# <a name="unjoindomainorworkgroup-method-of-the-win32_computersystem-class"></a><span data-ttu-id="7eaf0-103">Win32 UnjoinDomainOrWorkgroup 類別的方法 \_</span><span class="sxs-lookup"><span data-stu-id="7eaf0-103">UnjoinDomainOrWorkgroup method of the Win32\_ComputerSystem class</span></span>

<span data-ttu-id="7eaf0-104">**UnjoinDomainOrWorkgroup** 方法會從網域或工作組移除電腦系統。</span><span class="sxs-lookup"><span data-stu-id="7eaf0-104">The **UnjoinDomainOrWorkgroup** method removes a computer system from a domain or workgroup.</span></span>

<span data-ttu-id="7eaf0-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="7eaf0-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="7eaf0-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="7eaf0-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="7eaf0-107">語法</span><span class="sxs-lookup"><span data-stu-id="7eaf0-107">Syntax</span></span>


```mof
uint32 UnjoinDomainOrWorkgroup(
  [in] string Password,
  [in] string UserName,
  [in] uint32 FUnjoinOptions = 
);
```



## <a name="parameters"></a><span data-ttu-id="7eaf0-108">參數</span><span class="sxs-lookup"><span data-stu-id="7eaf0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7eaf0-109">*密碼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7eaf0-109">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7eaf0-110">如果 *UserName* 參數指定帳戶名稱， *password* 參數必須指向連接到網域控制站時要使用的密碼。</span><span class="sxs-lookup"><span data-stu-id="7eaf0-110">If the *UserName* parameter specifies an account name, the *Password* parameter must point to the password to use when connecting to the domain controller.</span></span> <span data-ttu-id="7eaf0-111">否則，此參數必須為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="7eaf0-111">Otherwise, this parameter must be **NULL**.</span></span>

> [!Note]  
> <span data-ttu-id="7eaf0-112">連接到 IWbemServices 或 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) on [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices)指標時，*密碼* 必須使用高驗證層級，而不是低於 **RPC \_ C \_ 驗證 \_ 層級的 \_ PKT \_ 隱私權**。</span><span class="sxs-lookup"><span data-stu-id="7eaf0-112">*Password* must use a high authentication level, not less than **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, when connecting to Winmgmt or [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) on the [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) pointer.</span></span> <span data-ttu-id="7eaf0-113">如果是本機到 Winmgmt，這就不是問題所在。</span><span class="sxs-lookup"><span data-stu-id="7eaf0-113">If local to Winmgmt, this is not a concern.</span></span>

 

</dd> <dt>

<span data-ttu-id="7eaf0-114">使用者 *名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7eaf0-114">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7eaf0-115">指向以 null 終止的常數位符串指標，指定連接到網域控制站時要使用的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="7eaf0-115">Pointer to a constant null-terminated character string that specifies the account name to use when connecting to the domain controller.</span></span> <span data-ttu-id="7eaf0-116">必須指定網域和使用者帳戶，例如「網域使用者」或「」 \\ user@domain 。</span><span class="sxs-lookup"><span data-stu-id="7eaf0-116">Must specify a domain and user account, for example, "domain\\user" or "user@domain".</span></span> <span data-ttu-id="7eaf0-117">如果這個參數為 **Null**，則會使用呼叫端內容。</span><span class="sxs-lookup"><span data-stu-id="7eaf0-117">If this parameter is **NULL**, the caller context is used.</span></span>

> [!Note]  
> <span data-ttu-id="7eaf0-118">連線到 [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices)指標上的 Winmgmt 或 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)時，使用者 *名稱* 必須使用高驗證層級，而非小於 **RPC \_ C \_ 驗證 \_ 層級的 \_ PKT \_ 隱私權**。</span><span class="sxs-lookup"><span data-stu-id="7eaf0-118">*UserName* must use a high authentication level, not less than **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, when connecting to Winmgmt or [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) on the [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) pointer.</span></span> <span data-ttu-id="7eaf0-119">如果是本機到 Winmgmt，這就不是問題所在。</span><span class="sxs-lookup"><span data-stu-id="7eaf0-119">If local to Winmgmt, this is not a concern.</span></span>

 

</dd> <dt>

<span data-ttu-id="7eaf0-120">*FUnjoinOptions* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7eaf0-120">*FUnjoinOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7eaf0-121">定義退出選項的位旗標集合。</span><span class="sxs-lookup"><span data-stu-id="7eaf0-121">Set of bit flags defining the unjoin options.</span></span>

<dt>



 <span data-ttu-id="7eaf0-122"> (0)</span><span class="sxs-lookup"><span data-stu-id="7eaf0-122">(0)</span></span>


</dt> <dd>

<span data-ttu-id="7eaf0-123">預設值。</span><span class="sxs-lookup"><span data-stu-id="7eaf0-123">Default.</span></span> <span data-ttu-id="7eaf0-124">沒有選項。</span><span class="sxs-lookup"><span data-stu-id="7eaf0-124">No options.</span></span>

</dd> <dt>

<span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>

<span data-ttu-id="7eaf0-125"><span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>**NETSETUP \_ (\_** 4) 的帳戶刪除</span><span class="sxs-lookup"><span data-stu-id="7eaf0-125"><span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>**NETSETUP\_ACCT\_DELETE** (4)</span></span>


</dt> <dd>

<span data-ttu-id="7eaf0-126">在退出作業之後停用 Active Directory 帳戶，但不要刪除帳戶。</span><span class="sxs-lookup"><span data-stu-id="7eaf0-126">Disable the Active Directory account after the unjoin operation, but do not delete the account.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7eaf0-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="7eaf0-127">Return value</span></span>

<span data-ttu-id="7eaf0-128">**UnjoinDomainOrWorkgroup** 方法會在成功時傳回 0 (零) ，或不涉及任何選項時傳回。</span><span class="sxs-lookup"><span data-stu-id="7eaf0-128">The **UnjoinDomainOrWorkgroup** method returns 0 (zero) on success or when no options are involved.</span></span> <span data-ttu-id="7eaf0-129">任何其他值則表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="7eaf0-129">Any other value indicates an error.</span></span> <span data-ttu-id="7eaf0-130">如需錯誤碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="7eaf0-130">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="7eaf0-131">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="7eaf0-131">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="7eaf0-132">**成功** (0) </span><span class="sxs-lookup"><span data-stu-id="7eaf0-132">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7eaf0-133">**其他** (1 4294967295) </span><span class="sxs-lookup"><span data-stu-id="7eaf0-133">**Other** (1 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="7eaf0-134">備註</span><span class="sxs-lookup"><span data-stu-id="7eaf0-134">Remarks</span></span>

<span data-ttu-id="7eaf0-135">呼叫此方法之後，請重新開機受影響的電腦以套用變更。</span><span class="sxs-lookup"><span data-stu-id="7eaf0-135">After calling this method, restart the affected computer to apply the changes.</span></span>

## <a name="examples"></a><span data-ttu-id="7eaf0-136">範例</span><span class="sxs-lookup"><span data-stu-id="7eaf0-136">Examples</span></span>

<span data-ttu-id="7eaf0-137">[從網域退出電腦](https://Gallery.TechNet.Microsoft.Com/c2025ace-cb51-4136-9de9-db8871f79f62) VBScript 範例會從目前的網域 unjoins 本機電腦，並停用電腦帳戶。</span><span class="sxs-lookup"><span data-stu-id="7eaf0-137">[The Unjoin a Computer from a Domain](https://Gallery.TechNet.Microsoft.Com/c2025ace-cb51-4136-9de9-db8871f79f62) VBScript sample unjoins the local computer from its current domain and disables the computer account.</span></span>

<span data-ttu-id="7eaf0-138">[使用 VBS 腳本範例從網域退出電腦](https://Gallery.TechNet.Microsoft.Com/Unjoin-a-Computer-from-a-825249e1)從網域 unjoins 指定的電腦。</span><span class="sxs-lookup"><span data-stu-id="7eaf0-138">The [Unjoin a Computer from a Domain using VBS script](https://Gallery.TechNet.Microsoft.Com/Unjoin-a-Computer-from-a-825249e1) sample unjoins a specified computer from a domain.</span></span> <span data-ttu-id="7eaf0-139">.</span><span class="sxs-lookup"><span data-stu-id="7eaf0-139">.</span></span>

## <a name="requirements"></a><span data-ttu-id="7eaf0-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="7eaf0-140">Requirements</span></span>



| <span data-ttu-id="7eaf0-141">需求</span><span class="sxs-lookup"><span data-stu-id="7eaf0-141">Requirement</span></span> | <span data-ttu-id="7eaf0-142">值</span><span class="sxs-lookup"><span data-stu-id="7eaf0-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7eaf0-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7eaf0-143">Minimum supported client</span></span><br/> | <span data-ttu-id="7eaf0-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7eaf0-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7eaf0-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7eaf0-145">Minimum supported server</span></span><br/> | <span data-ttu-id="7eaf0-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7eaf0-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7eaf0-147">命名空間</span><span class="sxs-lookup"><span data-stu-id="7eaf0-147">Namespace</span></span><br/>                | <span data-ttu-id="7eaf0-148">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7eaf0-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7eaf0-149">MOF</span><span class="sxs-lookup"><span data-stu-id="7eaf0-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7eaf0-150"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="7eaf0-150"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7eaf0-151">DLL</span><span class="sxs-lookup"><span data-stu-id="7eaf0-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7eaf0-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7eaf0-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7eaf0-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7eaf0-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7eaf0-154">**Win32 \_ 未進行**</span><span class="sxs-lookup"><span data-stu-id="7eaf0-154">**Win32\_ComputerSystem**</span></span>](win32-computersystem.md)
</dt> <dt>

[<span data-ttu-id="7eaf0-155">**JoinDomainOrWorkgroup 方法**</span><span class="sxs-lookup"><span data-stu-id="7eaf0-155">**JoinDomainOrWorkgroup method**</span></span>](joindomainorworkgroup-method-in-class-win32-computersystem.md)
</dt> </dl>

 


---
title: 'Win32_TSPermissionsSetting 類別的 AddAccount 方法 (Faxcomex) '
description: AddAccount 方法會準備將帳戶新增至具有指定許可權集合的終端機。 您可以新增使用者、群組或電腦。
ms.assetid: da4d8f5b-7aa2-4b55-bf0f-b3e98b70a06b
ms.tgt_platform: multiple
keywords:
- AddAccount 方法遠端桌面服務
- AddAccount 方法遠端桌面服務，Win32_TSPermissionsSetting 類別
- Win32_TSPermissionsSetting 類別遠端桌面服務，AddAccount 方法
topic_type:
- apiref
api_name:
- Win32_TSPermissionsSetting.AddAccount
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de89c34bd7aab20fbfbcbdedfd9d2f91bba866bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465961"
---
# <a name="addaccount-method-of-the-win32_tspermissionssetting-class"></a><span data-ttu-id="27350-107">Win32 TSPermissionsSetting 類別的 AddAccount 方法 \_</span><span class="sxs-lookup"><span data-stu-id="27350-107">AddAccount method of the Win32\_TSPermissionsSetting class</span></span>

<span data-ttu-id="27350-108">**AddAccount** 方法會準備將帳戶新增至具有指定許可權集合的終端機。</span><span class="sxs-lookup"><span data-stu-id="27350-108">The **AddAccount** method prepares to add an account to the terminal with the specified permission set.</span></span> <span data-ttu-id="27350-109">您可以新增使用者、群組或電腦。</span><span class="sxs-lookup"><span data-stu-id="27350-109">You can add users, groups, or computers.</span></span>

## <a name="syntax"></a><span data-ttu-id="27350-110">語法</span><span class="sxs-lookup"><span data-stu-id="27350-110">Syntax</span></span>


```mof
uint32 AddAccount(
  [in] string AccountName,
  [in] uint32 PermissionPreSet
);
```



## <a name="parameters"></a><span data-ttu-id="27350-111">參數</span><span class="sxs-lookup"><span data-stu-id="27350-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27350-112">*AccountName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="27350-112">*AccountName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27350-113">要新增至終端機的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="27350-113">The name of the account to add to the terminal.</span></span>

</dd> <dt>

<span data-ttu-id="27350-114">*PermissionPreSet* \[在\]</span><span class="sxs-lookup"><span data-stu-id="27350-114">*PermissionPreSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27350-115">要與指定的帳號相關聯的許可權集合。</span><span class="sxs-lookup"><span data-stu-id="27350-115">The set of permissions to associate with the specified account.</span></span> <span data-ttu-id="27350-116">這個參數可以是下列任何一個或所有的值。</span><span class="sxs-lookup"><span data-stu-id="27350-116">This parameter can be any or all of the following values.</span></span> <span data-ttu-id="27350-117">如需詳細資訊，請參閱 [遠端桌面服務許可權](terminal-services-permissions.md)。</span><span class="sxs-lookup"><span data-stu-id="27350-117">For more information, see [Remote Desktop Services Permissions](terminal-services-permissions.md).</span></span>

<dt>

<span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>

<span data-ttu-id="27350-118"><span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>**WINSTATION \_來賓 \_ 存取** (0) </span><span class="sxs-lookup"><span data-stu-id="27350-118"><span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>**WINSTATION\_GUEST\_ACCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="27350-119">帳戶具有登入許可權。</span><span class="sxs-lookup"><span data-stu-id="27350-119">The account has Logon permission.</span></span>

</dd> <dt>

<span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>

<span data-ttu-id="27350-120"><span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>**WINSTATION \_使用者 \_ 存取** (1) </span><span class="sxs-lookup"><span data-stu-id="27350-120"><span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>**WINSTATION\_USER\_ACCESS** (1)</span></span>


</dt> <dd>

<span data-ttu-id="27350-121">帳戶具有下列許可權： Logon、Query Information、Send Message 和 Connect。</span><span class="sxs-lookup"><span data-stu-id="27350-121">The account has the following permissions: Logon, Query Information, Send Message, and Connect.</span></span>

</dd> <dt>

<span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>

<span data-ttu-id="27350-122"><span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>**WINSTATION \_所有 \_ 存取** (2) </span><span class="sxs-lookup"><span data-stu-id="27350-122"><span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>**WINSTATION\_ALL\_ACCESS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="27350-123">此帳戶具有所有的遠端桌面服務許可權。</span><span class="sxs-lookup"><span data-stu-id="27350-123">The account has all Remote Desktop Services Permissions.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27350-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="27350-124">Return value</span></span>

<span data-ttu-id="27350-125">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="27350-125">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="27350-126">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="27350-126">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="27350-127">備註</span><span class="sxs-lookup"><span data-stu-id="27350-127">Remarks</span></span>

<span data-ttu-id="27350-128">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="27350-128">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="27350-129">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="27350-129">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="27350-130">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="27350-130">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="27350-131">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="27350-131">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="27350-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="27350-132">Requirements</span></span>



| <span data-ttu-id="27350-133">需求</span><span class="sxs-lookup"><span data-stu-id="27350-133">Requirement</span></span> | <span data-ttu-id="27350-134">值</span><span class="sxs-lookup"><span data-stu-id="27350-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="27350-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="27350-135">Minimum supported client</span></span><br/> | <span data-ttu-id="27350-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="27350-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="27350-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="27350-137">Minimum supported server</span></span><br/> | <span data-ttu-id="27350-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27350-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="27350-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="27350-139">Namespace</span></span><br/>                | <span data-ttu-id="27350-140">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="27350-140">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="27350-141">標頭</span><span class="sxs-lookup"><span data-stu-id="27350-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="27350-142"><dt>Faxcomex。h</dt></span><span class="sxs-lookup"><span data-stu-id="27350-142"><dt>Faxcomex.h</dt></span></span> </dl>   |
| <span data-ttu-id="27350-143">MOF</span><span class="sxs-lookup"><span data-stu-id="27350-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="27350-144"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="27350-144"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="27350-145">DLL</span><span class="sxs-lookup"><span data-stu-id="27350-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27350-146"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27350-146"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27350-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="27350-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27350-148">**Win32 \_ TSPermissionsSetting**</span><span class="sxs-lookup"><span data-stu-id="27350-148">**Win32\_TSPermissionsSetting**</span></span>](win32-tspermissionssetting.md)
</dt> </dl>

 


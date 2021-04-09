---
title: Win32_TSAccount 類別的 ModifyAuditPermissions 方法
description: 準備為指定的帳號設定更細微的 audit 許可權集。
ms.assetid: 7df44a37-257d-49c6-8193-f1e1c5ebbb57
ms.tgt_platform: multiple
keywords:
- ModifyAuditPermissions 方法遠端桌面服務
- ModifyAuditPermissions 方法遠端桌面服務，Win32_TSAccount 類別
- Win32_TSAccount 類別遠端桌面服務，ModifyAuditPermissions 方法
topic_type:
- apiref
api_name:
- Win32_TSAccount.ModifyAuditPermissions
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f19337cc6110a15b206fc437fb6ec594ded60640
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844212"
---
# <a name="modifyauditpermissions-method-of-the-win32_tsaccount-class"></a><span data-ttu-id="c0721-106">Win32 TSAccount 類別的 ModifyAuditPermissions 方法 \_</span><span class="sxs-lookup"><span data-stu-id="c0721-106">ModifyAuditPermissions method of the Win32\_TSAccount class</span></span>

<span data-ttu-id="c0721-107">**ModifyAuditPermissions** 方法會準備為指定的帳號設定更細微的 audit 許可權集。</span><span class="sxs-lookup"><span data-stu-id="c0721-107">The **ModifyAuditPermissions** method prepares to set a more granular set of audit permissions to the specified account.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0721-108">語法</span><span class="sxs-lookup"><span data-stu-id="c0721-108">Syntax</span></span>


```mof
uint32 ModifyAuditPermissions(
  [in] uint32  PermissionMask,
  [in] boolean Success
);
```



## <a name="parameters"></a><span data-ttu-id="c0721-109">參數</span><span class="sxs-lookup"><span data-stu-id="c0721-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0721-110">*PermissionMask* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c0721-110">*PermissionMask* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0721-111">要與指定的帳號相關聯的 [遠端桌面工作階段主機許可權](terminal-services-permissions.md) 集合。</span><span class="sxs-lookup"><span data-stu-id="c0721-111">The set of [Remote Desktop Session Host Permissions](terminal-services-permissions.md) to associate with the specified account.</span></span> <span data-ttu-id="c0721-112">此參數的值是點陣圖，而且可以選取下列任何或所有的值。</span><span class="sxs-lookup"><span data-stu-id="c0721-112">The value of this parameter is a bitmap, and any or all of the following values may be selected.</span></span>

<dt>

<span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>

<span data-ttu-id="c0721-113"><span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>**WINSTATION \_查詢** (0) </span><span class="sxs-lookup"><span data-stu-id="c0721-113"><span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>**WINSTATION\_QUERY** (0)</span></span>


</dt> <dd>

<span data-ttu-id="c0721-114">查詢會話相關資訊的許可權。</span><span class="sxs-lookup"><span data-stu-id="c0721-114">Permission to query information about a session.</span></span>

</dd> <dt>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>

<span data-ttu-id="c0721-115"><span id="WINSTATION_SET"></span><span id="winstation_set"></span>**WINSTATION \_設定** (1) </span><span class="sxs-lookup"><span data-stu-id="c0721-115"><span id="WINSTATION_SET"></span><span id="winstation_set"></span>**WINSTATION\_SET** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c0721-116">修改連接參數的許可權。</span><span class="sxs-lookup"><span data-stu-id="c0721-116">Permission to modify connection parameters.</span></span>

</dd> <dt>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>

<span data-ttu-id="c0721-117"><span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**WINSTATION \_重設** (6) </span><span class="sxs-lookup"><span data-stu-id="c0721-117"><span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**WINSTATION\_RESET** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c0721-118">重設或結束會話或連接的許可權。</span><span class="sxs-lookup"><span data-stu-id="c0721-118">Permission to reset or end a session or connection.</span></span>

</dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>

<span data-ttu-id="c0721-119"><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**WINSTATION \_\| \_ \_ 需要虛擬標準許可權** (3) </span><span class="sxs-lookup"><span data-stu-id="c0721-119"><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**WINSTATION\_VIRTUAL \| STANDARD\_RIGHTS\_REQUIRED** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c0721-120">使用虛擬通道的許可權。</span><span class="sxs-lookup"><span data-stu-id="c0721-120">Permission to use virtual channels.</span></span> <span data-ttu-id="c0721-121">虛擬通道可讓您從伺服器程式存取用戶端裝置。</span><span class="sxs-lookup"><span data-stu-id="c0721-121">Virtual channels provide access from a server program to client devices.</span></span>

</dd> <dt>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>

<span data-ttu-id="c0721-122"><span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**WINSTATION \_陰影** (4) </span><span class="sxs-lookup"><span data-stu-id="c0721-122"><span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**WINSTATION\_SHADOW** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c0721-123">陰影或遠端控制另一個使用者會話的許可權。</span><span class="sxs-lookup"><span data-stu-id="c0721-123">Permission to shadow or remotely control another user's session.</span></span>

</dd> <dt>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>

<span data-ttu-id="c0721-124"><span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**WINSTATION \_登** 入 (5) </span><span class="sxs-lookup"><span data-stu-id="c0721-124"><span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**WINSTATION\_LOGON** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c0721-125">登入伺服器上會話的許可權。</span><span class="sxs-lookup"><span data-stu-id="c0721-125">Permission to log on to a session on the server.</span></span>

</dd> <dt>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>

<span data-ttu-id="c0721-126"><span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**WINSTATION \_登出** (2) </span><span class="sxs-lookup"><span data-stu-id="c0721-126"><span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**WINSTATION\_LOGOFF** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c0721-127">從會話登出使用者的許可權。</span><span class="sxs-lookup"><span data-stu-id="c0721-127">Permission to log off a user from a session.</span></span>

</dd> <dt>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>

<span data-ttu-id="c0721-128"><span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**WINSTATION \_MSG** (7) </span><span class="sxs-lookup"><span data-stu-id="c0721-128"><span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**WINSTATION\_MSG** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c0721-129">將訊息傳送至另一個使用者會話的許可權。</span><span class="sxs-lookup"><span data-stu-id="c0721-129">Permission to send a message to another user's session.</span></span>

</dd> <dt>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>

<span data-ttu-id="c0721-130"><span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**WINSTATION \_連接** (8) </span><span class="sxs-lookup"><span data-stu-id="c0721-130"><span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**WINSTATION\_CONNECT** (8)</span></span>


</dt> <dd>

<span data-ttu-id="c0721-131">連接到另一個會話的許可權。</span><span class="sxs-lookup"><span data-stu-id="c0721-131">Permission to connect to another session.</span></span>

</dd> <dt>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>

<span data-ttu-id="c0721-132"><span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**WINSTATION \_中斷** (9) 的連線</span><span class="sxs-lookup"><span data-stu-id="c0721-132"><span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**WINSTATION\_DISCONNECT** (9)</span></span>


</dt> <dd>

<span data-ttu-id="c0721-133">中斷會話連接的許可權。</span><span class="sxs-lookup"><span data-stu-id="c0721-133">Permission to disconnect a session.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c0721-134">*成功* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c0721-134">*Success* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0721-135">指定是否允許或拒絕 *PermissionMask* 參數的值所指定的許可權集合。</span><span class="sxs-lookup"><span data-stu-id="c0721-135">Specifies if the permission set specified by the value of the *PermissionMask* parameter is allowed or denied.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="c0721-136"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="c0721-136"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="c0721-137">允許指定的許可權集合。</span><span class="sxs-lookup"><span data-stu-id="c0721-137">The specified permission set is allowed.</span></span>

</dd> <dt>

<span id="0"></span>

<span data-ttu-id="c0721-138"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="c0721-138"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="c0721-139">已拒絕指定的許可權集合。</span><span class="sxs-lookup"><span data-stu-id="c0721-139">The specified permission set is denied.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0721-140">傳回值</span><span class="sxs-lookup"><span data-stu-id="c0721-140">Return value</span></span>

<span data-ttu-id="c0721-141">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c0721-141">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="c0721-142">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="c0721-142">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0721-143">備註</span><span class="sxs-lookup"><span data-stu-id="c0721-143">Remarks</span></span>

<span data-ttu-id="c0721-144">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="c0721-144">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c0721-145">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="c0721-145">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c0721-146">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="c0721-146">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c0721-147">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="c0721-147">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0721-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="c0721-148">Requirements</span></span>



| <span data-ttu-id="c0721-149">需求</span><span class="sxs-lookup"><span data-stu-id="c0721-149">Requirement</span></span> | <span data-ttu-id="c0721-150">值</span><span class="sxs-lookup"><span data-stu-id="c0721-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0721-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c0721-151">Minimum supported client</span></span><br/> | <span data-ttu-id="c0721-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0721-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c0721-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c0721-153">Minimum supported server</span></span><br/> | <span data-ttu-id="c0721-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c0721-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c0721-155">命名空間</span><span class="sxs-lookup"><span data-stu-id="c0721-155">Namespace</span></span><br/>                | <span data-ttu-id="c0721-156">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="c0721-156">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="c0721-157">MOF</span><span class="sxs-lookup"><span data-stu-id="c0721-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c0721-158"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="c0721-158"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="c0721-159">DLL</span><span class="sxs-lookup"><span data-stu-id="c0721-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0721-160"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0721-160"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0721-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c0721-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0721-162">**Win32 \_ TSAccount**</span><span class="sxs-lookup"><span data-stu-id="c0721-162">**Win32\_TSAccount**</span></span>](win32-tsaccount.md)
</dt> </dl>

 


---
title: Win32_TSAccount 類別的 ModifyPermissions 方法
description: 設定指定之帳戶的許可權。
ms.assetid: cef36f7f-d327-4bb6-9bff-282036c1a5d5
ms.tgt_platform: multiple
keywords:
- ModifyPermissions 方法遠端桌面服務
- ModifyPermissions 方法遠端桌面服務，Win32_TSAccount 類別
- Win32_TSAccount 類別遠端桌面服務，ModifyPermissions 方法
topic_type:
- apiref
api_name:
- Win32_TSAccount.ModifyPermissions
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4bf6147c215475314f65bb8fa426442884bc82e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106991305"
---
# <a name="modifypermissions-method-of-the-win32_tsaccount-class"></a><span data-ttu-id="23644-106">Win32 TSAccount 類別的 ModifyPermissions 方法 \_</span><span class="sxs-lookup"><span data-stu-id="23644-106">ModifyPermissions method of the Win32\_TSAccount class</span></span>

<span data-ttu-id="23644-107">設定指定之帳戶的許可權。</span><span class="sxs-lookup"><span data-stu-id="23644-107">Sets a permission for the specified account.</span></span>

## <a name="syntax"></a><span data-ttu-id="23644-108">語法</span><span class="sxs-lookup"><span data-stu-id="23644-108">Syntax</span></span>


```mof
uint32 ModifyPermissions(
  [in] uint32  PermissionMask,
  [in] boolean Allow
);
```



## <a name="parameters"></a><span data-ttu-id="23644-109">參數</span><span class="sxs-lookup"><span data-stu-id="23644-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23644-110">*PermissionMask* \[在\]</span><span class="sxs-lookup"><span data-stu-id="23644-110">*PermissionMask* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23644-111">要設定的 [遠端桌面工作階段主機許可權](terminal-services-permissions.md) 。</span><span class="sxs-lookup"><span data-stu-id="23644-111">The [Remote Desktop Session Host Permission](terminal-services-permissions.md) to set.</span></span>

<span data-ttu-id="23644-112">可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="23644-112">The possible values are:</span></span>

<dt>

<span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>

<span data-ttu-id="23644-113"><span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>**WINSTATION \_查詢** (0) </span><span class="sxs-lookup"><span data-stu-id="23644-113"><span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>**WINSTATION\_QUERY** (0)</span></span>


</dt> <dd>

<span data-ttu-id="23644-114">查詢會話相關資訊的許可權。</span><span class="sxs-lookup"><span data-stu-id="23644-114">Permission to query information about a session.</span></span>

</dd> <dt>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>

<span data-ttu-id="23644-115"><span id="WINSTATION_SET"></span><span id="winstation_set"></span>**WINSTATION \_設定** (1) </span><span class="sxs-lookup"><span data-stu-id="23644-115"><span id="WINSTATION_SET"></span><span id="winstation_set"></span>**WINSTATION\_SET** (1)</span></span>


</dt> <dd>

<span data-ttu-id="23644-116">修改連接參數的許可權。</span><span class="sxs-lookup"><span data-stu-id="23644-116">Permission to modify connection parameters.</span></span>

</dd> <dt>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>

<span data-ttu-id="23644-117"><span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**WINSTATION \_重設** (6) </span><span class="sxs-lookup"><span data-stu-id="23644-117"><span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**WINSTATION\_RESET** (6)</span></span>


</dt> <dd>

<span data-ttu-id="23644-118">重設或結束會話或連接的許可權。</span><span class="sxs-lookup"><span data-stu-id="23644-118">Permission to reset or end a session or connection.</span></span>

</dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>

<span data-ttu-id="23644-119"><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**WINSTATION \_\| \_ \_ 需要虛擬標準許可權** (3) </span><span class="sxs-lookup"><span data-stu-id="23644-119"><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**WINSTATION\_VIRTUAL \| STANDARD\_RIGHTS\_REQUIRED** (3)</span></span>


</dt> <dd>

<span data-ttu-id="23644-120">使用虛擬通道的許可權。</span><span class="sxs-lookup"><span data-stu-id="23644-120">Permission to use virtual channels.</span></span> <span data-ttu-id="23644-121">虛擬通道可讓您從伺服器程式存取用戶端裝置。</span><span class="sxs-lookup"><span data-stu-id="23644-121">Virtual channels provide access from a server program to client devices.</span></span>

</dd> <dt>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>

<span data-ttu-id="23644-122"><span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**WINSTATION \_陰影** (4) </span><span class="sxs-lookup"><span data-stu-id="23644-122"><span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**WINSTATION\_SHADOW** (4)</span></span>


</dt> <dd>

<span data-ttu-id="23644-123">陰影或遠端控制另一個使用者會話的許可權。</span><span class="sxs-lookup"><span data-stu-id="23644-123">Permission to shadow or remotely control another user's session.</span></span>

</dd> <dt>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>

<span data-ttu-id="23644-124"><span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**WINSTATION \_登** 入 (5) </span><span class="sxs-lookup"><span data-stu-id="23644-124"><span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**WINSTATION\_LOGON** (5)</span></span>


</dt> <dd>

<span data-ttu-id="23644-125">登入伺服器上會話的許可權。</span><span class="sxs-lookup"><span data-stu-id="23644-125">Permission to log on to a session on the server.</span></span>

</dd> <dt>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>

<span data-ttu-id="23644-126"><span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**WINSTATION \_登出** (2) </span><span class="sxs-lookup"><span data-stu-id="23644-126"><span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**WINSTATION\_LOGOFF** (2)</span></span>


</dt> <dd>

<span data-ttu-id="23644-127">從會話登出使用者的許可權。</span><span class="sxs-lookup"><span data-stu-id="23644-127">Permission to log off a user from a session.</span></span>

</dd> <dt>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>

<span data-ttu-id="23644-128"><span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**WINSTATION \_MSG** (7) </span><span class="sxs-lookup"><span data-stu-id="23644-128"><span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**WINSTATION\_MSG** (7)</span></span>


</dt> <dd>

<span data-ttu-id="23644-129">將訊息傳送至另一個使用者會話的許可權。</span><span class="sxs-lookup"><span data-stu-id="23644-129">Permission to send a message to another user's session.</span></span>

</dd> <dt>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>

<span data-ttu-id="23644-130"><span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**WINSTATION \_連接** (8) </span><span class="sxs-lookup"><span data-stu-id="23644-130"><span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**WINSTATION\_CONNECT** (8)</span></span>


</dt> <dd>

<span data-ttu-id="23644-131">連接到另一個會話的許可權。</span><span class="sxs-lookup"><span data-stu-id="23644-131">Permission to connect to another session.</span></span>

</dd> <dt>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>

<span data-ttu-id="23644-132"><span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**WINSTATION \_中斷** (9) 的連線</span><span class="sxs-lookup"><span data-stu-id="23644-132"><span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**WINSTATION\_DISCONNECT** (9)</span></span>


</dt> <dd>

<span data-ttu-id="23644-133">中斷會話連接的許可權。</span><span class="sxs-lookup"><span data-stu-id="23644-133">Permission to disconnect a session.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="23644-134">*允許* \[在\]</span><span class="sxs-lookup"><span data-stu-id="23644-134">*Allow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23644-135">指定是否允許或拒絕 *PermissionMask* 參數中的許可權。</span><span class="sxs-lookup"><span data-stu-id="23644-135">Specifies whether the permission in the *PermissionMask* parameter is allowed or denied.</span></span>

<span data-ttu-id="23644-136">可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="23644-136">The possible values are:</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="23644-137"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="23644-137"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="23644-138">允許指定的許可權集合。</span><span class="sxs-lookup"><span data-stu-id="23644-138">The specified permission set is allowed.</span></span>

</dd> <dt>

<span id="0"></span>

<span data-ttu-id="23644-139"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="23644-139"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="23644-140">已拒絕指定的許可權集合。</span><span class="sxs-lookup"><span data-stu-id="23644-140">The specified permission set is denied.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23644-141">傳回值</span><span class="sxs-lookup"><span data-stu-id="23644-141">Return value</span></span>

<span data-ttu-id="23644-142">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="23644-142">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="23644-143">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="23644-143">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="23644-144">備註</span><span class="sxs-lookup"><span data-stu-id="23644-144">Remarks</span></span>

<span data-ttu-id="23644-145">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="23644-145">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="23644-146">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="23644-146">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="23644-147">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="23644-147">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="23644-148">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="23644-148">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="23644-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="23644-149">Requirements</span></span>



| <span data-ttu-id="23644-150">需求</span><span class="sxs-lookup"><span data-stu-id="23644-150">Requirement</span></span> | <span data-ttu-id="23644-151">值</span><span class="sxs-lookup"><span data-stu-id="23644-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23644-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="23644-152">Minimum supported client</span></span><br/> | <span data-ttu-id="23644-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="23644-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="23644-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="23644-154">Minimum supported server</span></span><br/> | <span data-ttu-id="23644-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="23644-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="23644-156">命名空間</span><span class="sxs-lookup"><span data-stu-id="23644-156">Namespace</span></span><br/>                | <span data-ttu-id="23644-157">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="23644-157">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="23644-158">MOF</span><span class="sxs-lookup"><span data-stu-id="23644-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="23644-159"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="23644-159"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="23644-160">DLL</span><span class="sxs-lookup"><span data-stu-id="23644-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23644-161"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23644-161"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23644-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="23644-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23644-163">**Win32 \_ TSAccount**</span><span class="sxs-lookup"><span data-stu-id="23644-163">**Win32\_TSAccount**</span></span>](win32-tsaccount.md)
</dt> </dl>

 


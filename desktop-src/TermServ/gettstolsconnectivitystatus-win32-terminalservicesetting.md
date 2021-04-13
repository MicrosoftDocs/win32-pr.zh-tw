---
title: Win32_TerminalServiceSetting 類別的 GetTStoLSConnectivityStatus 方法
description: 判斷遠端桌面服務與授權伺服器之間的連接狀態。
ms.assetid: 11fc5865-47e8-4be8-a526-53e29f72d0a4
ms.tgt_platform: multiple
keywords:
- GetTStoLSConnectivityStatus 方法遠端桌面服務
- GetTStoLSConnectivityStatus 方法遠端桌面服務，Win32_TerminalServiceSetting 類別
- Win32_TerminalServiceSetting 類別遠端桌面服務，GetTStoLSConnectivityStatus 方法
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetTStoLSConnectivityStatus
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fb73cd62c5ab5c343f44f24bbbd8de7f6343a21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465796"
---
# <a name="gettstolsconnectivitystatus-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="837b2-106">Win32 TerminalServiceSetting 類別的 GetTStoLSConnectivityStatus 方法 \_</span><span class="sxs-lookup"><span data-stu-id="837b2-106">GetTStoLSConnectivityStatus method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="837b2-107">判斷遠端桌面服務與授權伺服器之間的連接狀態。</span><span class="sxs-lookup"><span data-stu-id="837b2-107">Determines the connectivity status between Remote Desktop Services and a license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="837b2-108">語法</span><span class="sxs-lookup"><span data-stu-id="837b2-108">Syntax</span></span>


```mof
uint32 GetTStoLSConnectivityStatus(
  [in]  string ServerName,
  [out] uint32 TStoLSConnectivityStatus
);
```



## <a name="parameters"></a><span data-ttu-id="837b2-109">參數</span><span class="sxs-lookup"><span data-stu-id="837b2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="837b2-110">*ServerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="837b2-110">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="837b2-111">要檢查連接狀態的授權伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="837b2-111">The name of the license server to check the connectivity status of.</span></span>

</dd> <dt>

<span data-ttu-id="837b2-112">*TStoLSConnectivityStatus* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="837b2-112">*TStoLSConnectivityStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="837b2-113">值，這個值表示授權伺服器的連接狀態。</span><span class="sxs-lookup"><span data-stu-id="837b2-113">A value that indicates the connectivity status of the license server.</span></span> <span data-ttu-id="837b2-114">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="837b2-114">This can be one of the following values.</span></span>

<dt>

<span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>

<span data-ttu-id="837b2-115"><span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>**LS \_可 \_** 連接的未知 (0) </span><span class="sxs-lookup"><span data-stu-id="837b2-115"><span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>**LS\_CONNECTABLE\_UNKNOWN** (0)</span></span>


</dt> <dd>

<span data-ttu-id="837b2-116">無法判斷連接狀態。</span><span class="sxs-lookup"><span data-stu-id="837b2-116">The connectivity status cannot be determined.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>

<span data-ttu-id="837b2-117"><span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>**LS \_可連接的 \_ 有效 \_ WS08R2** (1) </span><span class="sxs-lookup"><span data-stu-id="837b2-117"><span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>**LS\_CONNECTABLE\_VALID\_WS08R2** (1)</span></span>


</dt> <dd>

<span data-ttu-id="837b2-118">遠端桌面服務可以連接至 Windows Server 2008 R2 授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="837b2-118">Remote Desktop Services can connect to the Windows Server 2008 R2 license server.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>

<span data-ttu-id="837b2-119"><span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>**LS \_可連接的 \_ 有效 \_ WS08** (2) </span><span class="sxs-lookup"><span data-stu-id="837b2-119"><span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>**LS\_CONNECTABLE\_VALID\_WS08** (2)</span></span>


</dt> <dd>

<span data-ttu-id="837b2-120">遠端桌面服務可以連接至 Windows Server 2008 授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="837b2-120">Remote Desktop Services can connect to the Windows Server 2008 license server.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>

<span data-ttu-id="837b2-121"><span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>**LS \_可連接的 \_ BETA \_ RTM \_ 不符** (3) </span><span class="sxs-lookup"><span data-stu-id="837b2-121"><span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>**LS\_CONNECTABLE\_BETA\_RTM\_MISMATCH** (3)</span></span>


</dt> <dd>

<span data-ttu-id="837b2-122">遠端桌面服務可以連線到授權伺服器，但其中一部伺服器正在執行 Beta 版作業系統。</span><span class="sxs-lookup"><span data-stu-id="837b2-122">Remote Desktop Services can connect to the license server, but one of the servers is running a beta version of the operating system.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>

<span data-ttu-id="837b2-123"><span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>**LS \_可連接的 \_ 較低 \_ 版本** (4) </span><span class="sxs-lookup"><span data-stu-id="837b2-123"><span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>**LS\_CONNECTABLE\_LOWER\_VERSION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="837b2-124">遠端桌面服務可以連線到授權伺服器，但授權伺服器與遠端桌面服務主機伺服器之間有不相容的情況。</span><span class="sxs-lookup"><span data-stu-id="837b2-124">Remote Desktop Services can connect to the license server, but there is an incompatibility between the license server and the Remote Desktop Services host server.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>

<span data-ttu-id="837b2-125"><span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>**LS \_可連接 \_ 不 \_ 在 \_ TSCGROUP** (5) </span><span class="sxs-lookup"><span data-stu-id="837b2-125"><span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>**LS\_CONNECTABLE\_NOT\_IN\_TSCGROUP** (5)</span></span>


</dt> <dd>

<span data-ttu-id="837b2-126">授權伺服器中已啟用安全性群組原則，但遠端桌面服務不是群組原則的一部分。</span><span class="sxs-lookup"><span data-stu-id="837b2-126">Security group policy is enabled in license server, but Remote Desktop Services is not a part of the group policy.</span></span>

</dd> <dt>

<span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>

<span data-ttu-id="837b2-127"><span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>**LS \_無法 \_** 連接 (6) </span><span class="sxs-lookup"><span data-stu-id="837b2-127"><span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>**LS\_NOT\_CONNECTABLE** (6)</span></span>


</dt> <dd>

<span data-ttu-id="837b2-128">遠端桌面服務無法連接至授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="837b2-128">Remote Desktop Services cannot connect to the license server.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>

<span data-ttu-id="837b2-129"><span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>**LS \_可連接的 \_ 未知 \_ 有效** (7) </span><span class="sxs-lookup"><span data-stu-id="837b2-129"><span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>**LS\_CONNECTABLE\_UNKNOWN\_VALIDITY** (7)</span></span>


</dt> <dd>

<span data-ttu-id="837b2-130">授權伺服器可以連接到，但無法判斷連接的有效性。</span><span class="sxs-lookup"><span data-stu-id="837b2-130">The license server can be connected to, but the validity of the connection cannot be determined.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>

<span data-ttu-id="837b2-131"><span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>**LS \_可 \_ 連接 \_ 但 \_ 拒絕存取** (8) </span><span class="sxs-lookup"><span data-stu-id="837b2-131"><span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>**LS\_CONNECTABLE\_BUT\_ACCESS\_DENIED** (8)</span></span>


</dt> <dd>

<span data-ttu-id="837b2-132">遠端桌面服務可以連接到授權伺服器，但使用者帳戶沒有授權伺服器的系統管理員許可權。</span><span class="sxs-lookup"><span data-stu-id="837b2-132">Remote Desktop Services can connect to the license server, but the user account does not have administrator privileges on the license server.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>

<span data-ttu-id="837b2-133"><span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>**LS \_可連接的 \_ 有效 \_ WS08R2 \_ VDI** (9) </span><span class="sxs-lookup"><span data-stu-id="837b2-133"><span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>**LS\_CONNECTABLE\_VALID\_WS08R2\_VDI** (9)</span></span>


</dt> <dd>

<span data-ttu-id="837b2-134">遠端桌面服務可以 (VDI) Server 連線至 Windows Server 2008 R2 虛擬桌面基礎結構。</span><span class="sxs-lookup"><span data-stu-id="837b2-134">Remote Desktop Services can connect to the Windows Server 2008 R2 Virtual Desktop Infrastructure (VDI) server.</span></span>

<span data-ttu-id="837b2-135">**Windows Server 2008 R2：** Windows Server 2012 之前不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="837b2-135">**Windows Server 2008 R2:** This value is not supported before Windows Server 2012.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>

<span data-ttu-id="837b2-136"><span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>**LS \_\_ \_ 不 \_ 支援** 可連接功能 (10) </span><span class="sxs-lookup"><span data-stu-id="837b2-136"><span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>**LS\_CONNECTABLE\_FEATURE\_NOT\_SUPPORTED** (10)</span></span>


</dt> <dd>

<span data-ttu-id="837b2-137">這項功能不受支援。</span><span class="sxs-lookup"><span data-stu-id="837b2-137">The feature is not supported.</span></span>

<span data-ttu-id="837b2-138">**Windows server 2008 r2 和 Windows server 2008 R2 SP1：** Windows Server 2012 之前不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="837b2-138">**Windows Server 2008 R2 and Windows Server 2008 R2 with SP1:** This value is not supported before Windows Server 2012.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>

<span data-ttu-id="837b2-139"><span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>**LS \_可連接的 \_ 有效 \_ LS** (11) </span><span class="sxs-lookup"><span data-stu-id="837b2-139"><span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>**LS\_CONNECTABLE\_VALID\_LS** (11)</span></span>


</dt> <dd>

<span data-ttu-id="837b2-140">授權伺服器有效。</span><span class="sxs-lookup"><span data-stu-id="837b2-140">The license server is valid.</span></span>

<span data-ttu-id="837b2-141">**Windows server 2008 r2 和 Windows server 2008 R2 SP1：** Windows Server 2012 之前不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="837b2-141">**Windows Server 2008 R2 and Windows Server 2008 R2 with SP1:** This value is not supported before Windows Server 2012.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="837b2-142">傳回值</span><span class="sxs-lookup"><span data-stu-id="837b2-142">Return value</span></span>

<span data-ttu-id="837b2-143">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="837b2-143">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="837b2-144">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="837b2-144">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="837b2-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="837b2-145">Requirements</span></span>



| <span data-ttu-id="837b2-146">需求</span><span class="sxs-lookup"><span data-stu-id="837b2-146">Requirement</span></span> | <span data-ttu-id="837b2-147">值</span><span class="sxs-lookup"><span data-stu-id="837b2-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="837b2-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="837b2-148">Minimum supported client</span></span><br/> | <span data-ttu-id="837b2-149">都不支援</span><span class="sxs-lookup"><span data-stu-id="837b2-149">None supported</span></span><br/>                                                               |
| <span data-ttu-id="837b2-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="837b2-150">Minimum supported server</span></span><br/> | <span data-ttu-id="837b2-151">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="837b2-151">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="837b2-152">命名空間</span><span class="sxs-lookup"><span data-stu-id="837b2-152">Namespace</span></span><br/>                | <span data-ttu-id="837b2-153">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="837b2-153">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="837b2-154">MOF</span><span class="sxs-lookup"><span data-stu-id="837b2-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="837b2-155"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="837b2-155"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="837b2-156">DLL</span><span class="sxs-lookup"><span data-stu-id="837b2-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="837b2-157"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="837b2-157"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="837b2-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="837b2-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="837b2-159">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="837b2-159">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

 






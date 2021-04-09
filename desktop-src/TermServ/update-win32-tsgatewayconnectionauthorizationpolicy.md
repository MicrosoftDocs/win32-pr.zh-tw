---
title: Win32_TSGatewayConnectionAuthorizationPolicy 類別的 Update 方法
description: 更新目前的遠端桌面連線授權原則 (RD \ 160;端點) 。
ms.assetid: 6d13d1b7-1c7d-4d22-b42c-36e0f4446e86
ms.tgt_platform: multiple
keywords:
- Update 方法遠端桌面服務
- Update 方法遠端桌面服務，Win32_TSGatewayConnectionAuthorizationPolicy 類別
- Win32_TSGatewayConnectionAuthorizationPolicy 類別遠端桌面服務，Update 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87b982030170e954342dc5ff99754dcb89afd0e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025170"
---
# <a name="update-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="19a20-106">Win32 TSGatewayConnectionAuthorizationPolicy 類別的 Update 方法 \_</span><span class="sxs-lookup"><span data-stu-id="19a20-106">Update method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="19a20-107"> (RD CAP) 更新目前的遠端桌面連線授權原則。</span><span class="sxs-lookup"><span data-stu-id="19a20-107">Updates the current Remote Desktop connection authorization policy (RD CAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="19a20-108">語法</span><span class="sxs-lookup"><span data-stu-id="19a20-108">Syntax</span></span>


```mof
uint32 Update(
  [in] string  Name,
  [in] string  UserGroupNames,
  [in] string  ComputerGroupNames,
  [in] boolean SmartCard,
  [in] boolean Password,
  [in] boolean SecureId,
  [in] boolean Enabled,
  [in] uint32  DeviceRedirectionType,
  [in] boolean DiskDrivesDisabled,
  [in] boolean PrintersDisabled,
  [in] boolean SerialPortsDisabled,
  [in] boolean ClipboardDisabled,
  [in] boolean PlugAndPlayDevicesDisabled,
  [in] uint32  IdleTimeout,
  [in] uint32  SessionTimeout,
  [in] uint32  SessionTimeoutAction,
  [in] boolean AllowOnlySDRServers,
  [in] boolean CookieAuthentication
);
```



## <a name="parameters"></a><span data-ttu-id="19a20-109">參數</span><span class="sxs-lookup"><span data-stu-id="19a20-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19a20-110">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19a20-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19a20-111">RD CAP 的名稱。</span><span class="sxs-lookup"><span data-stu-id="19a20-111">Name of the RD CAP.</span></span> <span data-ttu-id="19a20-112">名稱必須為64個字元或更少，) 會忽略唯一的 (大小寫，且不能包含下列保留字元：</span><span class="sxs-lookup"><span data-stu-id="19a20-112">The name must be 64 characters or less, unique (case is ignored), and cannot contain the following reserved characters:</span></span>

<span data-ttu-id="19a20-113"><> ：;" / \\ \| ?</span><span class="sxs-lookup"><span data-stu-id="19a20-113"><> : ; " / \\ \| ?</span></span> <span data-ttu-id="19a20-114">\*\[TAB\]</span><span class="sxs-lookup"><span data-stu-id="19a20-114">\* \[TAB\]</span></span>

</dd> <dt>

<span data-ttu-id="19a20-115">*UserGroupNames* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19a20-115">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19a20-116">分號分隔的使用者組名清單。</span><span class="sxs-lookup"><span data-stu-id="19a20-116">List of semicolon-separated user group names.</span></span> <span data-ttu-id="19a20-117">名稱的格式為 *網域 \\ UserGroupName*。</span><span class="sxs-lookup"><span data-stu-id="19a20-117">The names are of the format *Domain\\UserGroupName*.</span></span> <span data-ttu-id="19a20-118">如果使用者屬於這些使用者群組的任何一個，則會允許使用者存取 RD 閘道 server。</span><span class="sxs-lookup"><span data-stu-id="19a20-118">If the user belongs to any one of these user groups, the user will be permitted access to the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="19a20-119">*ComputerGroupNames* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19a20-119">*ComputerGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19a20-120">分號分隔的電腦群組名清單。</span><span class="sxs-lookup"><span data-stu-id="19a20-120">List of semicolon-separated machine group names.</span></span> <span data-ttu-id="19a20-121">這個值可以是空的。</span><span class="sxs-lookup"><span data-stu-id="19a20-121">This value can be empty.</span></span> <span data-ttu-id="19a20-122">名稱的格式為 *網域 \\ ComputerGroupName*。</span><span class="sxs-lookup"><span data-stu-id="19a20-122">The names are of the format *Domain\\ComputerGroupName*.</span></span> <span data-ttu-id="19a20-123">如果指定了值，用戶端電腦必須屬於其中一個電腦群組，使用者才能存取 RD 閘道 server。</span><span class="sxs-lookup"><span data-stu-id="19a20-123">If a value is specified, the client computer must belong to one of these computer groups for the user to access the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="19a20-124">*智慧卡* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19a20-124">*SmartCard* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19a20-125">指定是否可以使用智慧卡向 RD 閘道伺服器進行驗證。</span><span class="sxs-lookup"><span data-stu-id="19a20-125">Specifies whether smart cards can be used to authenticate with the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="19a20-126">*密碼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19a20-126">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19a20-127">指定是否可以使用密碼向 RD 閘道伺服器進行驗證。</span><span class="sxs-lookup"><span data-stu-id="19a20-127">Specifies whether passwords can be used to authenticate with the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="19a20-128">*SecureId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19a20-128">*SecureId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19a20-129">這個參數保留給未來使用。</span><span class="sxs-lookup"><span data-stu-id="19a20-129">This parameter is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="19a20-130">*已啟用* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19a20-130">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19a20-131">指定是否啟用此 RD CAP。</span><span class="sxs-lookup"><span data-stu-id="19a20-131">Specifies whether this RD CAP is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="19a20-132">*DeviceRedirectionType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19a20-132">*DeviceRedirectionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19a20-133">指定將會重新導向的裝置類型。</span><span class="sxs-lookup"><span data-stu-id="19a20-133">Specifies which device types will be redirected.</span></span>

<dt>

<span data-ttu-id="19a20-134">0</span><span class="sxs-lookup"><span data-stu-id="19a20-134">0</span></span>
</dt> <dd>

<span data-ttu-id="19a20-135">將會重新導向所有裝置。</span><span class="sxs-lookup"><span data-stu-id="19a20-135">All devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="19a20-136">1</span><span class="sxs-lookup"><span data-stu-id="19a20-136">1</span></span>
</dt> <dd>

<span data-ttu-id="19a20-137">將不會重新導向任何裝置。</span><span class="sxs-lookup"><span data-stu-id="19a20-137">No devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="19a20-138">2</span><span class="sxs-lookup"><span data-stu-id="19a20-138">2</span></span>
</dt> <dd>

<span data-ttu-id="19a20-139">將不會重新導向指定的裝置。</span><span class="sxs-lookup"><span data-stu-id="19a20-139">Specified devices will not be redirected.</span></span> <span data-ttu-id="19a20-140">*DiskDrivesDisabled*、 *PrintersDisabled*、 *SerialPortsDisabled*、 *ClipboardDisabled* 和 *PlugAndPlayDevicesDisabled* 參數控制哪些裝置將不會被重新導向。</span><span class="sxs-lookup"><span data-stu-id="19a20-140">The *DiskDrivesDisabled*, *PrintersDisabled*, *SerialPortsDisabled*, *ClipboardDisabled*, and *PlugAndPlayDevicesDisabled* parameters control which devices will not be redirected.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="19a20-141">*DiskDrivesDisabled* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19a20-141">*DiskDrivesDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19a20-142">指定 *DeviceRedirectionType* 參數為 "2" 時，是否要停用磁片磁碟機重新導向。</span><span class="sxs-lookup"><span data-stu-id="19a20-142">Specifies whether to disable disk drive redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="19a20-143">*PrintersDisabled* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19a20-143">*PrintersDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19a20-144">指定是否要在 *DeviceRedirectionType* 參數為 "2" 時，停用印表機重新導向。</span><span class="sxs-lookup"><span data-stu-id="19a20-144">Specifies whether to disable printer redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="19a20-145">*SerialPortsDisabled* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19a20-145">*SerialPortsDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19a20-146">指定 *DeviceRedirectionType* 參數為 "2" 時，是否要停用序列埠重新導向。</span><span class="sxs-lookup"><span data-stu-id="19a20-146">Specifies whether to disable serial port redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="19a20-147">*ClipboardDisabled* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19a20-147">*ClipboardDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19a20-148">指定 *DeviceRedirectionType* 參數為 "2" 時，是否要停用剪貼簿重新導向。</span><span class="sxs-lookup"><span data-stu-id="19a20-148">Specifies whether to disable clipboard redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="19a20-149">*PlugAndPlayDevicesDisabled* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19a20-149">*PlugAndPlayDevicesDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19a20-150">指定 *DeviceRedirectionType* 參數為 "2" 時，是否要停用隨插即用裝置的重新導向。</span><span class="sxs-lookup"><span data-stu-id="19a20-150">Specifies whether to disable redirection of Plug and Play devices if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="19a20-151">*IdleTimeout* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19a20-151">*IdleTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19a20-152">閒置超時值（分鐘）</span><span class="sxs-lookup"><span data-stu-id="19a20-152">Idle timeout value in minutes</span></span>

</dd> <dt>

<span data-ttu-id="19a20-153">*SessionTimeout* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19a20-153">*SessionTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19a20-154">會話超時值（分鐘）</span><span class="sxs-lookup"><span data-stu-id="19a20-154">Session timeout value in minutes</span></span>

</dd> <dt>

<span data-ttu-id="19a20-155">*SessionTimeoutAction* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19a20-155">*SessionTimeoutAction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19a20-156">會話超時動作（分鐘）</span><span class="sxs-lookup"><span data-stu-id="19a20-156">Session timeout action in minutes</span></span>

</dd> <dt>

<span data-ttu-id="19a20-157">*AllowOnlySDRServers* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19a20-157">*AllowOnlySDRServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19a20-158">連接是否只允許連線到 SDR TS 伺服器</span><span class="sxs-lookup"><span data-stu-id="19a20-158">Whether connections allowed only to SDR TS servers</span></span>

</dd> <dt>

<span data-ttu-id="19a20-159">*CookieAuthentication* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19a20-159">*CookieAuthentication* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19a20-160">指出是否可以使用 cookie 驗證來連線到 TS 閘道伺服器</span><span class="sxs-lookup"><span data-stu-id="19a20-160">Indicates whether cookie authentication can be used to connect to TS Gateway server</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19a20-161">傳回值</span><span class="sxs-lookup"><span data-stu-id="19a20-161">Return value</span></span>

<span data-ttu-id="19a20-162">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="19a20-162">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="19a20-163">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="19a20-163">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="19a20-164">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="19a20-164">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="19a20-165">備註</span><span class="sxs-lookup"><span data-stu-id="19a20-165">Remarks</span></span>

<span data-ttu-id="19a20-166">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="19a20-166">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="19a20-167">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="19a20-167">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="19a20-168">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="19a20-168">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="19a20-169">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="19a20-169">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="19a20-170">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="19a20-170">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="19a20-171">規格需求</span><span class="sxs-lookup"><span data-stu-id="19a20-171">Requirements</span></span>



| <span data-ttu-id="19a20-172">需求</span><span class="sxs-lookup"><span data-stu-id="19a20-172">Requirement</span></span> | <span data-ttu-id="19a20-173">值</span><span class="sxs-lookup"><span data-stu-id="19a20-173">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="19a20-174">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="19a20-174">Minimum supported client</span></span><br/> | <span data-ttu-id="19a20-175">都不支援</span><span class="sxs-lookup"><span data-stu-id="19a20-175">None supported</span></span><br/>                                                                |
| <span data-ttu-id="19a20-176">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="19a20-176">Minimum supported server</span></span><br/> | <span data-ttu-id="19a20-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19a20-177">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="19a20-178">命名空間</span><span class="sxs-lookup"><span data-stu-id="19a20-178">Namespace</span></span><br/>                | <span data-ttu-id="19a20-179">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="19a20-179">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="19a20-180">MOF</span><span class="sxs-lookup"><span data-stu-id="19a20-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19a20-181"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="19a20-181"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="19a20-182">DLL</span><span class="sxs-lookup"><span data-stu-id="19a20-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19a20-183"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19a20-183"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="19a20-184">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19a20-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19a20-185">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="19a20-185">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 


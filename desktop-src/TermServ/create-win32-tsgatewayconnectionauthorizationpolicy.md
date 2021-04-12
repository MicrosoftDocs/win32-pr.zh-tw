---
title: Win32_TSGatewayConnectionAuthorizationPolicy 類別的 Create 方法
description: " (RD \\ 160; 建立遠端桌面連線授權原則使用指定值的端點) 。 新的 RD \\ 160;將會在 RD \\ 160 的頂端插入上限;端點評估順序，順序屬性值為 \\ 0034; 1 \\ 0034;。"
ms.assetid: 0010cd2b-9c23-488a-9337-d2ed338136d3
ms.tgt_platform: multiple
keywords:
- 建立方法遠端桌面服務
- 建立方法遠端桌面服務、Win32_TSGatewayConnectionAuthorizationPolicy 類別
- Win32_TSGatewayConnectionAuthorizationPolicy 類別遠端桌面服務，Create 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.Create
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edc027c2f7fc90318bd1af6fd1254077a860a5d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024761"
---
# <a name="create-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="601df-107">Win32 TSGatewayConnectionAuthorizationPolicy 類別的 Create 方法 \_</span><span class="sxs-lookup"><span data-stu-id="601df-107">Create method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="601df-108">使用指定的值， (RD CAP) 建立遠端桌面連線授權原則。</span><span class="sxs-lookup"><span data-stu-id="601df-108">Creates a Remote Desktop connection authorization policy (RD CAP) by using the specified values.</span></span> <span data-ttu-id="601df-109">新的 RD CAP 將會插入 RD CAP 評估順序的頂端，而 **order** 屬性值為 "1"。</span><span class="sxs-lookup"><span data-stu-id="601df-109">The new RD CAP will be inserted at the top of the RD CAP evaluation order, with an **Order** property value of "1".</span></span>

## <a name="syntax"></a><span data-ttu-id="601df-110">語法</span><span class="sxs-lookup"><span data-stu-id="601df-110">Syntax</span></span>


```mof
uint32 Create(
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



## <a name="parameters"></a><span data-ttu-id="601df-111">參數</span><span class="sxs-lookup"><span data-stu-id="601df-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="601df-112">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="601df-112">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="601df-113">RD CAP 的名稱。</span><span class="sxs-lookup"><span data-stu-id="601df-113">Name of the RD CAP.</span></span> <span data-ttu-id="601df-114">名稱必須為64個字元或更少，) 會忽略唯一的 (大小寫，且不能包含下列保留字元：</span><span class="sxs-lookup"><span data-stu-id="601df-114">The name must be 64 characters or less, unique (case is ignored), and cannot contain the following reserved characters:</span></span>

<span data-ttu-id="601df-115"><> ：;" / \\ \| ?</span><span class="sxs-lookup"><span data-stu-id="601df-115"><> : ; " / \\ \| ?</span></span> <span data-ttu-id="601df-116">\*\[TAB\]</span><span class="sxs-lookup"><span data-stu-id="601df-116">\* \[TAB\]</span></span>

</dd> <dt>

<span data-ttu-id="601df-117">*UserGroupNames* \[在\]</span><span class="sxs-lookup"><span data-stu-id="601df-117">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="601df-118">新 RD CAP 的使用者組名清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="601df-118">List of user group names, separated by semicolons, for the new RD CAP.</span></span>

</dd> <dt>

<span data-ttu-id="601df-119">*ComputerGroupNames* \[在\]</span><span class="sxs-lookup"><span data-stu-id="601df-119">*ComputerGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="601df-120">新 RD CAP 的電腦群組名清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="601df-120">List of computer group names, separated by semicolons, for the new RD CAP.</span></span>

</dd> <dt>

<span data-ttu-id="601df-121">*智慧卡* \[在\]</span><span class="sxs-lookup"><span data-stu-id="601df-121">*SmartCard* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="601df-122">指定是否可以使用智慧卡向 RD 閘道伺服器進行驗證。</span><span class="sxs-lookup"><span data-stu-id="601df-122">Specifies whether smart cards can be used to authenticate with the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="601df-123">*密碼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="601df-123">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="601df-124">指定是否可以使用密碼向 RD 閘道伺服器進行驗證。</span><span class="sxs-lookup"><span data-stu-id="601df-124">Specifies whether passwords can be used to authenticate with the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="601df-125">*SecureId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="601df-125">*SecureId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="601df-126">這個參數保留給未來使用。</span><span class="sxs-lookup"><span data-stu-id="601df-126">This parameter is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="601df-127">*已啟用* \[在\]</span><span class="sxs-lookup"><span data-stu-id="601df-127">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="601df-128">指定是否啟用此 RD CAP。</span><span class="sxs-lookup"><span data-stu-id="601df-128">Specifies whether this RD CAP is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="601df-129">*DeviceRedirectionType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="601df-129">*DeviceRedirectionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="601df-130">指定將會重新導向的裝置類型。</span><span class="sxs-lookup"><span data-stu-id="601df-130">Specifies which device types will be redirected.</span></span>

<dt>

<span data-ttu-id="601df-131">0</span><span class="sxs-lookup"><span data-stu-id="601df-131">0</span></span>
</dt> <dd>

<span data-ttu-id="601df-132">將會重新導向所有裝置。</span><span class="sxs-lookup"><span data-stu-id="601df-132">All devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="601df-133">1</span><span class="sxs-lookup"><span data-stu-id="601df-133">1</span></span>
</dt> <dd>

<span data-ttu-id="601df-134">將不會重新導向任何裝置。</span><span class="sxs-lookup"><span data-stu-id="601df-134">No devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="601df-135">2</span><span class="sxs-lookup"><span data-stu-id="601df-135">2</span></span>
</dt> <dd>

<span data-ttu-id="601df-136">將不會重新導向指定的裝置。</span><span class="sxs-lookup"><span data-stu-id="601df-136">Specified devices will not be redirected.</span></span> <span data-ttu-id="601df-137">*DiskDrivesDisabled*、 *PrintersDisabled*、 *SerialPortsDisabled*、 *ClipboardDisabled* 和 *PlugAndPlayDevicesDisabled* 參數控制哪些裝置將不會被重新導向。</span><span class="sxs-lookup"><span data-stu-id="601df-137">The *DiskDrivesDisabled*, *PrintersDisabled*, *SerialPortsDisabled*, *ClipboardDisabled*, and *PlugAndPlayDevicesDisabled* parameters control which devices will not be redirected.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="601df-138">*DiskDrivesDisabled* \[在\]</span><span class="sxs-lookup"><span data-stu-id="601df-138">*DiskDrivesDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="601df-139">指定 *DeviceRedirectionType* 參數為 "2" 時，是否要停用磁片磁碟機重新導向。</span><span class="sxs-lookup"><span data-stu-id="601df-139">Specifies whether to disable disk drive redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="601df-140">*PrintersDisabled* \[在\]</span><span class="sxs-lookup"><span data-stu-id="601df-140">*PrintersDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="601df-141">指定是否要在 *DeviceRedirectionType* 參數為 "2" 時，停用印表機重新導向。</span><span class="sxs-lookup"><span data-stu-id="601df-141">Specifies whether to disable printer redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="601df-142">*SerialPortsDisabled* \[在\]</span><span class="sxs-lookup"><span data-stu-id="601df-142">*SerialPortsDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="601df-143">指定 *DeviceRedirectionType* 參數為 "2" 時，是否要停用序列埠重新導向。</span><span class="sxs-lookup"><span data-stu-id="601df-143">Specifies whether to disable serial port redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="601df-144">*ClipboardDisabled* \[在\]</span><span class="sxs-lookup"><span data-stu-id="601df-144">*ClipboardDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="601df-145">指定 *DeviceRedirectionType* 參數為 "2" 時，是否要停用剪貼簿重新導向。</span><span class="sxs-lookup"><span data-stu-id="601df-145">Specifies whether to disable clipboard redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="601df-146">*PlugAndPlayDevicesDisabled* \[在\]</span><span class="sxs-lookup"><span data-stu-id="601df-146">*PlugAndPlayDevicesDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="601df-147">指定 *DeviceRedirectionType* 參數為 "2" 時，是否要停用隨插即用裝置的重新導向。</span><span class="sxs-lookup"><span data-stu-id="601df-147">Specifies whether to disable redirection of Plug and Play devices if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="601df-148">*IdleTimeout* \[在\]</span><span class="sxs-lookup"><span data-stu-id="601df-148">*IdleTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="601df-149">閒置超時值（分鐘）</span><span class="sxs-lookup"><span data-stu-id="601df-149">Idle timeout value in minutes</span></span>

</dd> <dt>

<span data-ttu-id="601df-150">*SessionTimeout* \[在\]</span><span class="sxs-lookup"><span data-stu-id="601df-150">*SessionTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="601df-151">會話超時值（分鐘）</span><span class="sxs-lookup"><span data-stu-id="601df-151">Session timeout value in minutes</span></span>

</dd> <dt>

<span data-ttu-id="601df-152">*SessionTimeoutAction* \[在\]</span><span class="sxs-lookup"><span data-stu-id="601df-152">*SessionTimeoutAction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="601df-153">會話超時動作（分鐘）</span><span class="sxs-lookup"><span data-stu-id="601df-153">Session timeout action in minutes</span></span>

</dd> <dt>

<span data-ttu-id="601df-154">*AllowOnlySDRServers* \[在\]</span><span class="sxs-lookup"><span data-stu-id="601df-154">*AllowOnlySDRServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="601df-155">連接是否只允許連線到 SDR TS 伺服器</span><span class="sxs-lookup"><span data-stu-id="601df-155">Whether connections allowed only to SDR TS servers</span></span>

</dd> <dt>

<span data-ttu-id="601df-156">*CookieAuthentication* \[在\]</span><span class="sxs-lookup"><span data-stu-id="601df-156">*CookieAuthentication* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="601df-157">指出是否可以使用 cookie 驗證來連線到 TS 閘道伺服器</span><span class="sxs-lookup"><span data-stu-id="601df-157">Indicates whether cookie authentication can be used to connect to TS Gateway server</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="601df-158">傳回值</span><span class="sxs-lookup"><span data-stu-id="601df-158">Return value</span></span>

<span data-ttu-id="601df-159">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="601df-159">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="601df-160">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="601df-160">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="601df-161">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="601df-161">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="601df-162">備註</span><span class="sxs-lookup"><span data-stu-id="601df-162">Remarks</span></span>

<span data-ttu-id="601df-163">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="601df-163">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="601df-164">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="601df-164">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="601df-165">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="601df-165">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="601df-166">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="601df-166">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="601df-167">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="601df-167">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="601df-168">規格需求</span><span class="sxs-lookup"><span data-stu-id="601df-168">Requirements</span></span>



| <span data-ttu-id="601df-169">需求</span><span class="sxs-lookup"><span data-stu-id="601df-169">Requirement</span></span> | <span data-ttu-id="601df-170">值</span><span class="sxs-lookup"><span data-stu-id="601df-170">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="601df-171">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="601df-171">Minimum supported client</span></span><br/> | <span data-ttu-id="601df-172">都不支援</span><span class="sxs-lookup"><span data-stu-id="601df-172">None supported</span></span><br/>                                                                |
| <span data-ttu-id="601df-173">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="601df-173">Minimum supported server</span></span><br/> | <span data-ttu-id="601df-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="601df-174">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="601df-175">命名空間</span><span class="sxs-lookup"><span data-stu-id="601df-175">Namespace</span></span><br/>                | <span data-ttu-id="601df-176">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="601df-176">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="601df-177">MOF</span><span class="sxs-lookup"><span data-stu-id="601df-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="601df-178"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="601df-178"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="601df-179">DLL</span><span class="sxs-lookup"><span data-stu-id="601df-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="601df-180"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="601df-180"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="601df-181">另請參閱</span><span class="sxs-lookup"><span data-stu-id="601df-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="601df-182">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="601df-182">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 


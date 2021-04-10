---
title: 'Win32_Service 類別的 GetSecurityDescriptor 方法 (遠端桌面服務) '
description: 傳回控制服務存取的安全描述項。
ms.assetid: 9898091A-5BE2-42A0-BF81-13AB74696ACB
ms.tgt_platform: multiple
keywords:
- 腳本 Windows Management Instrumentation，安全性
- 安全性 Windows Management Instrumentation，腳本
- GetSecurityDescriptor 方法遠端桌面服務
- GetSecurityDescriptor 方法遠端桌面服務，Win32_Service 類別
- Win32_Service 類別遠端桌面服務，GetSecurityDescriptor 方法
topic_type:
- apiref
api_name:
- Win32_Service.GetSecurityDescriptor
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf8dc271d5498163352af10bcb0b9c55e2e81fb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934234"
---
# <a name="getsecuritydescriptor-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="1864f-108">Win32_Service 類別的 GetSecurityDescriptor 方法 (遠端桌面服務) </span><span class="sxs-lookup"><span data-stu-id="1864f-108">GetSecurityDescriptor method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="1864f-109">**GetSecurityDescriptor** 方法會傳回控制服務存取權的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="1864f-109">The **GetSecurityDescriptor** method returns the security descriptor that controls access to the service.</span></span> <span data-ttu-id="1864f-110">描述項會以 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)的實例傳回。</span><span class="sxs-lookup"><span data-stu-id="1864f-110">The descriptor is returned as an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span>

## <a name="syntax"></a><span data-ttu-id="1864f-111">語法</span><span class="sxs-lookup"><span data-stu-id="1864f-111">Syntax</span></span>


```mof
uint32 GetSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="1864f-112">參數</span><span class="sxs-lookup"><span data-stu-id="1864f-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1864f-113">*描述* \[ 項擴展\]</span><span class="sxs-lookup"><span data-stu-id="1864f-113">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1864f-114">與服務相關聯的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="1864f-114">The security descriptor associated with the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1864f-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="1864f-115">Return value</span></span>

<span data-ttu-id="1864f-116">傳回下列清單所列的其中一個值，或傳回不同的值來表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="1864f-116">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="1864f-117">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="1864f-117">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="1864f-118">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="1864f-118">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="1864f-119">**0**</span><span class="sxs-lookup"><span data-stu-id="1864f-119">**0**</span></span>
</dt> <dd>

<span data-ttu-id="1864f-120">要求已被接受。</span><span class="sxs-lookup"><span data-stu-id="1864f-120">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="1864f-121">**1**</span><span class="sxs-lookup"><span data-stu-id="1864f-121">**1**</span></span>
</dt> <dd>

<span data-ttu-id="1864f-122">不支援此要求。</span><span class="sxs-lookup"><span data-stu-id="1864f-122">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="1864f-123">**2**</span><span class="sxs-lookup"><span data-stu-id="1864f-123">**2**</span></span>
</dt> <dd>

<span data-ttu-id="1864f-124">使用者沒有必要的存取權。</span><span class="sxs-lookup"><span data-stu-id="1864f-124">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="1864f-125">**3**</span><span class="sxs-lookup"><span data-stu-id="1864f-125">**3**</span></span>
</dt> <dd>

<span data-ttu-id="1864f-126">無法停止此服務，因為與它相依的其他服務正在執行中。</span><span class="sxs-lookup"><span data-stu-id="1864f-126">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="1864f-127">**4**</span><span class="sxs-lookup"><span data-stu-id="1864f-127">**4**</span></span>
</dt> <dd>

<span data-ttu-id="1864f-128">要求的控制碼無效，或是服務不接受此控制碼。</span><span class="sxs-lookup"><span data-stu-id="1864f-128">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="1864f-129">**5**</span><span class="sxs-lookup"><span data-stu-id="1864f-129">**5**</span></span>
</dt> <dd>

<span data-ttu-id="1864f-130">因為服務的狀態 ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)，所以無法將要求的控制項程式碼傳送至服務。**State** 屬性) 等於0、1或2。</span><span class="sxs-lookup"><span data-stu-id="1864f-130">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="1864f-131">**6**</span><span class="sxs-lookup"><span data-stu-id="1864f-131">**6**</span></span>
</dt> <dd>

<span data-ttu-id="1864f-132">尚未啟動服務。</span><span class="sxs-lookup"><span data-stu-id="1864f-132">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="1864f-133">**7**</span><span class="sxs-lookup"><span data-stu-id="1864f-133">**7**</span></span>
</dt> <dd>

<span data-ttu-id="1864f-134">服務並未及時回應啟動要求。</span><span class="sxs-lookup"><span data-stu-id="1864f-134">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="1864f-135">**8**</span><span class="sxs-lookup"><span data-stu-id="1864f-135">**8**</span></span>
</dt> <dd>

<span data-ttu-id="1864f-136">啟動服務時發生未知的錯誤。</span><span class="sxs-lookup"><span data-stu-id="1864f-136">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="1864f-137">**9**</span><span class="sxs-lookup"><span data-stu-id="1864f-137">**9**</span></span>
</dt> <dd>

<span data-ttu-id="1864f-138">找不到服務可執行檔的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="1864f-138">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="1864f-139">**10**</span><span class="sxs-lookup"><span data-stu-id="1864f-139">**10**</span></span>
</dt> <dd>

<span data-ttu-id="1864f-140">服務已在執行中。</span><span class="sxs-lookup"><span data-stu-id="1864f-140">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="1864f-141">**11**</span><span class="sxs-lookup"><span data-stu-id="1864f-141">**11**</span></span>
</dt> <dd>

<span data-ttu-id="1864f-142">要加入新服務的資料庫已被鎖定。</span><span class="sxs-lookup"><span data-stu-id="1864f-142">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="1864f-143">**12**</span><span class="sxs-lookup"><span data-stu-id="1864f-143">**12**</span></span>
</dt> <dd>

<span data-ttu-id="1864f-144">這項服務所依賴的相依性已從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="1864f-144">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="1864f-145">**13**</span><span class="sxs-lookup"><span data-stu-id="1864f-145">**13**</span></span>
</dt> <dd>

<span data-ttu-id="1864f-146">服務在相依的服務中找不到所需的服務。</span><span class="sxs-lookup"><span data-stu-id="1864f-146">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="1864f-147">**14**</span><span class="sxs-lookup"><span data-stu-id="1864f-147">**14**</span></span>
</dt> <dd>

<span data-ttu-id="1864f-148">已經從系統中停用服務。</span><span class="sxs-lookup"><span data-stu-id="1864f-148">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="1864f-149">**15**</span><span class="sxs-lookup"><span data-stu-id="1864f-149">**15**</span></span>
</dt> <dd>

<span data-ttu-id="1864f-150">此服務未通過驗證，無法在系統上執行。</span><span class="sxs-lookup"><span data-stu-id="1864f-150">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="1864f-151">**16**</span><span class="sxs-lookup"><span data-stu-id="1864f-151">**16**</span></span>
</dt> <dd>

<span data-ttu-id="1864f-152">這項服務正在從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="1864f-152">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="1864f-153">**17**</span><span class="sxs-lookup"><span data-stu-id="1864f-153">**17**</span></span>
</dt> <dd>

<span data-ttu-id="1864f-154">服務沒有執行執行緒。</span><span class="sxs-lookup"><span data-stu-id="1864f-154">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="1864f-155">**達**</span><span class="sxs-lookup"><span data-stu-id="1864f-155">**18**</span></span>
</dt> <dd>

<span data-ttu-id="1864f-156">服務會在啟動時有迴圈相依性。</span><span class="sxs-lookup"><span data-stu-id="1864f-156">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="1864f-157">**診斷**</span><span class="sxs-lookup"><span data-stu-id="1864f-157">**19**</span></span>
</dt> <dd>

<span data-ttu-id="1864f-158">服務正在相同名稱下執行。</span><span class="sxs-lookup"><span data-stu-id="1864f-158">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="1864f-159">**20**</span><span class="sxs-lookup"><span data-stu-id="1864f-159">**20**</span></span>
</dt> <dd>

<span data-ttu-id="1864f-160">服務名稱包含不正確字元。</span><span class="sxs-lookup"><span data-stu-id="1864f-160">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="1864f-161">**21**</span><span class="sxs-lookup"><span data-stu-id="1864f-161">**21**</span></span>
</dt> <dd>

<span data-ttu-id="1864f-162">傳遞給服務的參數無效。</span><span class="sxs-lookup"><span data-stu-id="1864f-162">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="1864f-163">**22**</span><span class="sxs-lookup"><span data-stu-id="1864f-163">**22**</span></span>
</dt> <dd>

<span data-ttu-id="1864f-164">用來執行此服務的帳戶無效，或缺少執行服務的許可權。</span><span class="sxs-lookup"><span data-stu-id="1864f-164">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="1864f-165">**23**</span><span class="sxs-lookup"><span data-stu-id="1864f-165">**23**</span></span>
</dt> <dd>

<span data-ttu-id="1864f-166">服務存在於系統可使用之服務的資料庫中。</span><span class="sxs-lookup"><span data-stu-id="1864f-166">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="1864f-167">**24**</span><span class="sxs-lookup"><span data-stu-id="1864f-167">**24**</span></span>
</dt> <dd>

<span data-ttu-id="1864f-168">服務目前在系統中暫停。</span><span class="sxs-lookup"><span data-stu-id="1864f-168">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1864f-169">備註</span><span class="sxs-lookup"><span data-stu-id="1864f-169">Remarks</span></span>

<span data-ttu-id="1864f-170">[**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)實例代表 [**安全 \_ 描述項 \_ 控制項**](/windows/desktop/SecAuthZ/security-descriptor-control)資料類型，並包含 (DACL) 的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly)，以及 (SACL) 的 [*系統存取控制清單*](/windows/desktop/SecGloss/s-gly)。</span><span class="sxs-lookup"><span data-stu-id="1864f-170">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="1864f-171">如需詳細資訊，請參閱 [存取控制清單](/windows/desktop/SecAuthZ/access-control-lists)。</span><span class="sxs-lookup"><span data-stu-id="1864f-171">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="1864f-172">如果未在取得安全描述項時授與或啟用 **SeSecurityPrivilege** ，則只會傳回傳回的安全描述項中的 DACL。</span><span class="sxs-lookup"><span data-stu-id="1864f-172">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="1864f-173">如需詳細資訊，請參閱 [**許可權常數**](/windows/desktop/WmiSdk/privilege-constants) 和 [執行特殊許可權作業](/windows/desktop/WmiSdk/executing-privileged-operations)。</span><span class="sxs-lookup"><span data-stu-id="1864f-173">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="1864f-174">範例</span><span class="sxs-lookup"><span data-stu-id="1864f-174">Examples</span></span>

<span data-ttu-id="1864f-175">在 VBScript 中取出安全描述項時，請務必以系統管理員身分執行，並以系統管理員身分執行，如下列程式碼片段所示。</span><span class="sxs-lookup"><span data-stu-id="1864f-175">When retrieving a security descriptor in VBScript, be sure to "Security" and run as as Admin, as shown in the following code snippet.</span></span> <span data-ttu-id="1864f-176">否則，您的程式碼可能會擲回許可權錯誤。</span><span class="sxs-lookup"><span data-stu-id="1864f-176">Otherwise, your code may throw a permissions error.</span></span>


```VB
Set objWMIService = GetObject("winmgmts:" _
  & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")
```



<span data-ttu-id="1864f-177">同樣地，在 VB.NET 中，請務必設定 "EnablePrivileges = True"，並以系統管理員身分執行應用程式。</span><span class="sxs-lookup"><span data-stu-id="1864f-177">Similarly, in VB.NET, be sure to set "EnablePrivileges = True" and run the Application as Admin.</span></span>


```VB
Scope = New ManagementScope([String].Format("\\{0}\root\CIMV2", ComputerName), Nothing)
Scope.Options.EnablePrivileges = True
```



## <a name="requirements"></a><span data-ttu-id="1864f-178">規格需求</span><span class="sxs-lookup"><span data-stu-id="1864f-178">Requirements</span></span>



| <span data-ttu-id="1864f-179">需求</span><span class="sxs-lookup"><span data-stu-id="1864f-179">Requirement</span></span> | <span data-ttu-id="1864f-180">值</span><span class="sxs-lookup"><span data-stu-id="1864f-180">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1864f-181">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1864f-181">Minimum supported client</span></span><br/> | <span data-ttu-id="1864f-182">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1864f-182">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1864f-183">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1864f-183">Minimum supported server</span></span><br/> | <span data-ttu-id="1864f-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1864f-184">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1864f-185">命名空間</span><span class="sxs-lookup"><span data-stu-id="1864f-185">Namespace</span></span><br/>                | <span data-ttu-id="1864f-186">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="1864f-186">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="1864f-187">MOF</span><span class="sxs-lookup"><span data-stu-id="1864f-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1864f-188"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="1864f-188"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="1864f-189">DLL</span><span class="sxs-lookup"><span data-stu-id="1864f-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1864f-190"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1864f-190"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1864f-191">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1864f-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1864f-192">**Win32 \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="1864f-192">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="1864f-193">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="1864f-193">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="1864f-194">**許可權常數**</span><span class="sxs-lookup"><span data-stu-id="1864f-194">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="1864f-195">WMI 安全描述項物件</span><span class="sxs-lookup"><span data-stu-id="1864f-195">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="1864f-196">變更安全物件的存取安全性</span><span class="sxs-lookup"><span data-stu-id="1864f-196">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[<span data-ttu-id="1864f-197">使用者帳戶控制和 WMI</span><span class="sxs-lookup"><span data-stu-id="1864f-197">User Account Control and WMI</span></span>](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 


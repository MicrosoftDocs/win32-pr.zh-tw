---
title: 'Win32_Service 類別的 SetSecurityDescriptor 方法 (遠端桌面服務) '
description: 寫入安全描述項的更新版本，以控制服務的存取權。
ms.assetid: 4F03B798-0912-4A0D-B31E-419662D5849B
ms.tgt_platform: multiple
keywords:
- 腳本 Windows Management Instrumentation，安全性
- 安全性 Windows Management Instrumentation，腳本
- SetSecurityDescriptor 方法遠端桌面服務
- SetSecurityDescriptor 方法遠端桌面服務，Win32_Service 類別
- Win32_Service 類別遠端桌面服務，SetSecurityDescriptor 方法
topic_type:
- apiref
api_name:
- Win32_Service.SetSecurityDescriptor
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19a21f9730b4c1c0ab7b3ccf662ddb2d95da2ee2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686420"
---
# <a name="setsecuritydescriptor-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="d4590-108">Win32_Service 類別的 SetSecurityDescriptor 方法 (遠端桌面服務) </span><span class="sxs-lookup"><span data-stu-id="d4590-108">SetSecurityDescriptor method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="d4590-109">**SetSecurityDescriptor** 方法會寫入控制服務存取權之安全描述項的更新版本。</span><span class="sxs-lookup"><span data-stu-id="d4590-109">The **SetSecurityDescriptor** method writes an updated version of the security descriptor that controls access to the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4590-110">語法</span><span class="sxs-lookup"><span data-stu-id="d4590-110">Syntax</span></span>


```mof
uint32 SetSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="d4590-111">參數</span><span class="sxs-lookup"><span data-stu-id="d4590-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4590-112">*描述* \[ 項在\]</span><span class="sxs-lookup"><span data-stu-id="d4590-112">*Descriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4590-113">與服務相關聯的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="d4590-113">The security descriptor associated with the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4590-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="d4590-114">Return value</span></span>

<span data-ttu-id="d4590-115">傳回下列清單所列的其中一個值，或傳回不同的值來表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="d4590-115">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="d4590-116">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="d4590-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="d4590-117">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="d4590-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="d4590-118">**0**</span><span class="sxs-lookup"><span data-stu-id="d4590-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="d4590-119">要求已被接受。</span><span class="sxs-lookup"><span data-stu-id="d4590-119">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="d4590-120">**1**</span><span class="sxs-lookup"><span data-stu-id="d4590-120">**1**</span></span>
</dt> <dd>

<span data-ttu-id="d4590-121">不支援此要求。</span><span class="sxs-lookup"><span data-stu-id="d4590-121">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="d4590-122">**2**</span><span class="sxs-lookup"><span data-stu-id="d4590-122">**2**</span></span>
</dt> <dd>

<span data-ttu-id="d4590-123">使用者沒有必要的存取權。</span><span class="sxs-lookup"><span data-stu-id="d4590-123">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="d4590-124">**3**</span><span class="sxs-lookup"><span data-stu-id="d4590-124">**3**</span></span>
</dt> <dd>

<span data-ttu-id="d4590-125">無法停止此服務，因為與它相依的其他服務正在執行中。</span><span class="sxs-lookup"><span data-stu-id="d4590-125">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="d4590-126">**4**</span><span class="sxs-lookup"><span data-stu-id="d4590-126">**4**</span></span>
</dt> <dd>

<span data-ttu-id="d4590-127">要求的控制碼無效，或是服務不接受此控制碼。</span><span class="sxs-lookup"><span data-stu-id="d4590-127">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="d4590-128">**5**</span><span class="sxs-lookup"><span data-stu-id="d4590-128">**5**</span></span>
</dt> <dd>

<span data-ttu-id="d4590-129">因為服務的狀態 ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)，所以無法將要求的控制項程式碼傳送至服務。**State** 屬性) 等於0、1或2。</span><span class="sxs-lookup"><span data-stu-id="d4590-129">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="d4590-130">**6**</span><span class="sxs-lookup"><span data-stu-id="d4590-130">**6**</span></span>
</dt> <dd>

<span data-ttu-id="d4590-131">尚未啟動服務。</span><span class="sxs-lookup"><span data-stu-id="d4590-131">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="d4590-132">**7**</span><span class="sxs-lookup"><span data-stu-id="d4590-132">**7**</span></span>
</dt> <dd>

<span data-ttu-id="d4590-133">服務並未及時回應啟動要求。</span><span class="sxs-lookup"><span data-stu-id="d4590-133">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="d4590-134">**8**</span><span class="sxs-lookup"><span data-stu-id="d4590-134">**8**</span></span>
</dt> <dd>

<span data-ttu-id="d4590-135">啟動服務時發生未知的錯誤。</span><span class="sxs-lookup"><span data-stu-id="d4590-135">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="d4590-136">**9**</span><span class="sxs-lookup"><span data-stu-id="d4590-136">**9**</span></span>
</dt> <dd>

<span data-ttu-id="d4590-137">找不到服務可執行檔的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="d4590-137">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="d4590-138">**10**</span><span class="sxs-lookup"><span data-stu-id="d4590-138">**10**</span></span>
</dt> <dd>

<span data-ttu-id="d4590-139">服務已在執行中。</span><span class="sxs-lookup"><span data-stu-id="d4590-139">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="d4590-140">**11**</span><span class="sxs-lookup"><span data-stu-id="d4590-140">**11**</span></span>
</dt> <dd>

<span data-ttu-id="d4590-141">要加入新服務的資料庫已被鎖定。</span><span class="sxs-lookup"><span data-stu-id="d4590-141">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="d4590-142">**12**</span><span class="sxs-lookup"><span data-stu-id="d4590-142">**12**</span></span>
</dt> <dd>

<span data-ttu-id="d4590-143">這項服務所依賴的相依性已從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="d4590-143">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d4590-144">**13**</span><span class="sxs-lookup"><span data-stu-id="d4590-144">**13**</span></span>
</dt> <dd>

<span data-ttu-id="d4590-145">服務在相依的服務中找不到所需的服務。</span><span class="sxs-lookup"><span data-stu-id="d4590-145">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="d4590-146">**14**</span><span class="sxs-lookup"><span data-stu-id="d4590-146">**14**</span></span>
</dt> <dd>

<span data-ttu-id="d4590-147">已經從系統中停用服務。</span><span class="sxs-lookup"><span data-stu-id="d4590-147">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d4590-148">**15**</span><span class="sxs-lookup"><span data-stu-id="d4590-148">**15**</span></span>
</dt> <dd>

<span data-ttu-id="d4590-149">此服務未通過驗證，無法在系統上執行。</span><span class="sxs-lookup"><span data-stu-id="d4590-149">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="d4590-150">**16**</span><span class="sxs-lookup"><span data-stu-id="d4590-150">**16**</span></span>
</dt> <dd>

<span data-ttu-id="d4590-151">這項服務正在從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="d4590-151">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d4590-152">**17**</span><span class="sxs-lookup"><span data-stu-id="d4590-152">**17**</span></span>
</dt> <dd>

<span data-ttu-id="d4590-153">服務沒有執行執行緒。</span><span class="sxs-lookup"><span data-stu-id="d4590-153">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="d4590-154">**達**</span><span class="sxs-lookup"><span data-stu-id="d4590-154">**18**</span></span>
</dt> <dd>

<span data-ttu-id="d4590-155">服務會在啟動時有迴圈相依性。</span><span class="sxs-lookup"><span data-stu-id="d4590-155">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="d4590-156">**診斷**</span><span class="sxs-lookup"><span data-stu-id="d4590-156">**19**</span></span>
</dt> <dd>

<span data-ttu-id="d4590-157">服務正在相同名稱下執行。</span><span class="sxs-lookup"><span data-stu-id="d4590-157">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="d4590-158">**20**</span><span class="sxs-lookup"><span data-stu-id="d4590-158">**20**</span></span>
</dt> <dd>

<span data-ttu-id="d4590-159">服務名稱包含不正確字元。</span><span class="sxs-lookup"><span data-stu-id="d4590-159">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="d4590-160">**21**</span><span class="sxs-lookup"><span data-stu-id="d4590-160">**21**</span></span>
</dt> <dd>

<span data-ttu-id="d4590-161">傳遞給服務的參數無效。</span><span class="sxs-lookup"><span data-stu-id="d4590-161">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="d4590-162">**22**</span><span class="sxs-lookup"><span data-stu-id="d4590-162">**22**</span></span>
</dt> <dd>

<span data-ttu-id="d4590-163">用來執行此服務的帳戶無效，或缺少執行服務的許可權。</span><span class="sxs-lookup"><span data-stu-id="d4590-163">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="d4590-164">**23**</span><span class="sxs-lookup"><span data-stu-id="d4590-164">**23**</span></span>
</dt> <dd>

<span data-ttu-id="d4590-165">服務存在於系統可使用之服務的資料庫中。</span><span class="sxs-lookup"><span data-stu-id="d4590-165">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d4590-166">**24**</span><span class="sxs-lookup"><span data-stu-id="d4590-166">**24**</span></span>
</dt> <dd>

<span data-ttu-id="d4590-167">服務目前在系統中暫停。</span><span class="sxs-lookup"><span data-stu-id="d4590-167">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d4590-168">備註</span><span class="sxs-lookup"><span data-stu-id="d4590-168">Remarks</span></span>

<span data-ttu-id="d4590-169">[**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)實例代表 [**安全 \_ 描述項 \_ 控制項**](/windows/desktop/SecAuthZ/security-descriptor-control)資料類型，並包含 (DACL) 的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly)，以及 (SACL) 的 [*系統存取控制清單*](/windows/desktop/SecGloss/s-gly)。</span><span class="sxs-lookup"><span data-stu-id="d4590-169">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="d4590-170">如需詳細資訊，請參閱 [存取控制清單](/windows/desktop/SecAuthZ/access-control-lists)。</span><span class="sxs-lookup"><span data-stu-id="d4590-170">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="d4590-171">如果未在取得安全描述項時授與或啟用 **SeSecurityPrivilege** ，則只會傳回傳回的安全描述項中的 DACL。</span><span class="sxs-lookup"><span data-stu-id="d4590-171">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="d4590-172">如需詳細資訊，請參閱 [**許可權常數**](/windows/desktop/WmiSdk/privilege-constants) 和 [執行特殊許可權作業](/windows/desktop/WmiSdk/executing-privileged-operations)。</span><span class="sxs-lookup"><span data-stu-id="d4590-172">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

<span data-ttu-id="d4590-173">呼叫這個方法時，您可以同時更新 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) 實例中的 dacl 和 SACL，但是您也可以只更新 dacl 或只更新 sacl。</span><span class="sxs-lookup"><span data-stu-id="d4590-173">You can update both the DACL and the SACL in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance when calling this method, but you also can update only the DACL or only the SACL.</span></span>

<span data-ttu-id="d4590-174">下列 [**安全 \_ 描述項 \_ 控制項**](/windows/desktop/SecAuthZ/security-descriptor-control) 中的值會決定是否要更新 DACL、SACL 或兩者。</span><span class="sxs-lookup"><span data-stu-id="d4590-174">The following values in [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determine whether the DACL, the SACL, or both are updated.</span></span>

-   <span data-ttu-id="d4590-175">**\_有 SE DACL \_**</span><span class="sxs-lookup"><span data-stu-id="d4590-175">**SE\_DACL\_PRESENT**</span></span>

    <span data-ttu-id="d4590-176">表示 DACL 應該更新。</span><span class="sxs-lookup"><span data-stu-id="d4590-176">Indicates that the DACL should be updated.</span></span> <span data-ttu-id="d4590-177">如果未設定此值，WMI 就會保留 DACL 的原始值。</span><span class="sxs-lookup"><span data-stu-id="d4590-177">If this is not set, then WMI preserves the original value of the DACL.</span></span>

-   <span data-ttu-id="d4590-178">**\_出現 SE SACL \_**</span><span class="sxs-lookup"><span data-stu-id="d4590-178">**SE\_SACL\_PRESENT**</span></span>

    <span data-ttu-id="d4590-179">指出 SACL 應該更新。</span><span class="sxs-lookup"><span data-stu-id="d4590-179">Indicates that the SACL should be updated.</span></span> <span data-ttu-id="d4590-180">如果未設定此值，WMI 就會保留 SACL 的原始值。</span><span class="sxs-lookup"><span data-stu-id="d4590-180">If this is not set, then WMI preserves the original value of the SACL.</span></span> <span data-ttu-id="d4590-181">若要更新 SACL，帳戶必須啟用 **SeSecurityPrivilege** 許可權。</span><span class="sxs-lookup"><span data-stu-id="d4590-181">To update the SACL, the account must have the **SeSecurityPrivilege** privilege enabled.</span></span> <span data-ttu-id="d4590-182">針對腳本，許可權名稱為 **SeSecurityPrivilege**。</span><span class="sxs-lookup"><span data-stu-id="d4590-182">For scripting, the privilege name is **SeSecurityPrivilege**.</span></span> <span data-ttu-id="d4590-183">如需詳細資訊，請參閱 [**許可權常數**](/windows/desktop/WmiSdk/privilege-constants)。</span><span class="sxs-lookup"><span data-stu-id="d4590-183">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants).</span></span>

<span data-ttu-id="d4590-184">如果群組信任者和擁有者信任的屬性不是 **Null**，則會更新這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d4590-184">If the Group trustee and the Owner trustee properties are not **NULL**, then they are updated.</span></span> <span data-ttu-id="d4590-185">否則，WMI 會保留原始值。</span><span class="sxs-lookup"><span data-stu-id="d4590-185">Otherwise, WMI preserves the original values.</span></span> <span data-ttu-id="d4590-186">如需詳細資訊，請參閱 [WMI 安全描述項物件](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)。</span><span class="sxs-lookup"><span data-stu-id="d4590-186">For more information, see [WMI Security Descriptor Objects](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span></span>

<span data-ttu-id="d4590-187">當中的新 SACL 是 **Null** 時，在呼叫這個方法時，目標安全物件上的安全描述項 SACL 會保持不變。</span><span class="sxs-lookup"><span data-stu-id="d4590-187">When a new SACL is **NULL** in a call this method, then the security descriptor SACL on the target securable object is left unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4590-188">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4590-188">Requirements</span></span>



| <span data-ttu-id="d4590-189">需求</span><span class="sxs-lookup"><span data-stu-id="d4590-189">Requirement</span></span> | <span data-ttu-id="d4590-190">值</span><span class="sxs-lookup"><span data-stu-id="d4590-190">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4590-191">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d4590-191">Minimum supported client</span></span><br/> | <span data-ttu-id="d4590-192">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d4590-192">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d4590-193">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d4590-193">Minimum supported server</span></span><br/> | <span data-ttu-id="d4590-194">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d4590-194">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d4590-195">命名空間</span><span class="sxs-lookup"><span data-stu-id="d4590-195">Namespace</span></span><br/>                | <span data-ttu-id="d4590-196">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="d4590-196">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d4590-197">MOF</span><span class="sxs-lookup"><span data-stu-id="d4590-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d4590-198"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="d4590-198"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d4590-199">DLL</span><span class="sxs-lookup"><span data-stu-id="d4590-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4590-200"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4590-200"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4590-201">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4590-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4590-202">**Win32 \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="d4590-202">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="d4590-203">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="d4590-203">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="d4590-204">**許可權常數**</span><span class="sxs-lookup"><span data-stu-id="d4590-204">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="d4590-205">WMI 安全描述項物件</span><span class="sxs-lookup"><span data-stu-id="d4590-205">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="d4590-206">變更安全物件的存取安全性</span><span class="sxs-lookup"><span data-stu-id="d4590-206">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[<span data-ttu-id="d4590-207">使用者帳戶控制和 WMI</span><span class="sxs-lookup"><span data-stu-id="d4590-207">User Account Control and WMI</span></span>](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 


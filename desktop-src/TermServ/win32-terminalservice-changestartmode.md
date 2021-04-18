---
title: 'Win32_Service 類別的 ChangeStartMode 方法 (遠端桌面服務) '
description: 修改 Win32 TerminalService 的啟動模式 \_ 。
ms.assetid: 4F4B8CFC-B38C-47C6-A2BA-D498EC2B7F55
ms.tgt_platform: multiple
keywords:
- ChangeStartMode 方法遠端桌面服務
- ChangeStartMode 方法遠端桌面服務，Win32_Service 類別
- Win32_Service 類別遠端桌面服務，ChangeStartMode 方法
topic_type:
- apiref
api_name:
- Win32_Service.ChangeStartMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a46c6b72fbb070dac32b2b6990a217068c77da9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968961"
---
# <a name="changestartmode-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="edcab-106">Win32_Service 類別的 ChangeStartMode 方法 (遠端桌面服務) </span><span class="sxs-lookup"><span data-stu-id="edcab-106">ChangeStartMode method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="edcab-107">**ChangeStartMode** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會修改 [**Win32 \_ TerminalService**](win32-terminalservice.md)的啟動模式。</span><span class="sxs-lookup"><span data-stu-id="edcab-107">The **ChangeStartMode** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies the start mode of a [**Win32\_TerminalService**](win32-terminalservice.md).</span></span>

<span data-ttu-id="edcab-108">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="edcab-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="edcab-109">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="edcab-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="edcab-110">語法</span><span class="sxs-lookup"><span data-stu-id="edcab-110">Syntax</span></span>


```mof
uint32 ChangeStartMode(
  [in] string StartMode
);
```



## <a name="parameters"></a><span data-ttu-id="edcab-111">參數</span><span class="sxs-lookup"><span data-stu-id="edcab-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edcab-112">*StartMode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="edcab-112">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edcab-113">Windows 基底服務的啟動模式。</span><span class="sxs-lookup"><span data-stu-id="edcab-113">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="edcab-114"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**引導**</span><span class="sxs-lookup"><span data-stu-id="edcab-114"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot**</span></span>


</dt> <dd>

<span data-ttu-id="edcab-115">作業系統載入器啟動的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="edcab-115">Device driver started by the operating system loader.</span></span> <span data-ttu-id="edcab-116">這個值只適用於驅動程式服務。</span><span class="sxs-lookup"><span data-stu-id="edcab-116">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="edcab-117"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**系統**</span><span class="sxs-lookup"><span data-stu-id="edcab-117"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System**</span></span>


</dt> <dd>

<span data-ttu-id="edcab-118">由作業系統初始化程式啟動的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="edcab-118">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="edcab-119">這個值只適用於驅動程式服務。</span><span class="sxs-lookup"><span data-stu-id="edcab-119">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="edcab-120"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**自動**</span><span class="sxs-lookup"><span data-stu-id="edcab-120"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic**</span></span>


</dt> <dd>

<span data-ttu-id="edcab-121">服務控制管理員在系統啟動期間自動啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="edcab-121">Service to be started automatically by the Service Control Manager during system startup.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="edcab-122"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**手動**</span><span class="sxs-lookup"><span data-stu-id="edcab-122"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual**</span></span>


</dt> <dd>

<span data-ttu-id="edcab-123">當進程呼叫 [**StartService**](win32-terminalservice-startservice.md) 方法時，服務控制管理員要啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="edcab-123">Service to be started by the Service Control Manager when a process calls the [**StartService**](win32-terminalservice-startservice.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="edcab-124"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**禁用**</span><span class="sxs-lookup"><span data-stu-id="edcab-124"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled**</span></span>


</dt> <dd>

<span data-ttu-id="edcab-125">無法再啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="edcab-125">Service that can no longer be started.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edcab-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="edcab-126">Return value</span></span>

<span data-ttu-id="edcab-127">傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="edcab-127">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="edcab-128">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="edcab-128">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="edcab-129">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="edcab-129">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="edcab-130">**0**</span><span class="sxs-lookup"><span data-stu-id="edcab-130">**0**</span></span>
</dt> <dd>

<span data-ttu-id="edcab-131">要求已被接受。</span><span class="sxs-lookup"><span data-stu-id="edcab-131">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="edcab-132">**1**</span><span class="sxs-lookup"><span data-stu-id="edcab-132">**1**</span></span>
</dt> <dd>

<span data-ttu-id="edcab-133">不支援此要求。</span><span class="sxs-lookup"><span data-stu-id="edcab-133">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="edcab-134">**2**</span><span class="sxs-lookup"><span data-stu-id="edcab-134">**2**</span></span>
</dt> <dd>

<span data-ttu-id="edcab-135">使用者沒有必要的存取權。</span><span class="sxs-lookup"><span data-stu-id="edcab-135">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="edcab-136">**3**</span><span class="sxs-lookup"><span data-stu-id="edcab-136">**3**</span></span>
</dt> <dd>

<span data-ttu-id="edcab-137">無法停止此服務，因為與它相依的其他服務正在執行中。</span><span class="sxs-lookup"><span data-stu-id="edcab-137">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="edcab-138">**4**</span><span class="sxs-lookup"><span data-stu-id="edcab-138">**4**</span></span>
</dt> <dd>

<span data-ttu-id="edcab-139">要求的控制碼無效，或是服務不接受此控制碼。</span><span class="sxs-lookup"><span data-stu-id="edcab-139">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="edcab-140">**5**</span><span class="sxs-lookup"><span data-stu-id="edcab-140">**5**</span></span>
</dt> <dd>

<span data-ttu-id="edcab-141">因為服務的狀態 ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)，所以無法將要求的控制項程式碼傳送至服務。**State** 屬性) 等於0、1或2。</span><span class="sxs-lookup"><span data-stu-id="edcab-141">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="edcab-142">**6**</span><span class="sxs-lookup"><span data-stu-id="edcab-142">**6**</span></span>
</dt> <dd>

<span data-ttu-id="edcab-143">尚未啟動服務。</span><span class="sxs-lookup"><span data-stu-id="edcab-143">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="edcab-144">**7**</span><span class="sxs-lookup"><span data-stu-id="edcab-144">**7**</span></span>
</dt> <dd>

<span data-ttu-id="edcab-145">服務並未及時回應啟動要求。</span><span class="sxs-lookup"><span data-stu-id="edcab-145">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="edcab-146">**8**</span><span class="sxs-lookup"><span data-stu-id="edcab-146">**8**</span></span>
</dt> <dd>

<span data-ttu-id="edcab-147">啟動服務時發生未知的錯誤。</span><span class="sxs-lookup"><span data-stu-id="edcab-147">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="edcab-148">**9**</span><span class="sxs-lookup"><span data-stu-id="edcab-148">**9**</span></span>
</dt> <dd>

<span data-ttu-id="edcab-149">找不到服務可執行檔的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="edcab-149">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="edcab-150">**10**</span><span class="sxs-lookup"><span data-stu-id="edcab-150">**10**</span></span>
</dt> <dd>

<span data-ttu-id="edcab-151">服務已在執行中。</span><span class="sxs-lookup"><span data-stu-id="edcab-151">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="edcab-152">**11**</span><span class="sxs-lookup"><span data-stu-id="edcab-152">**11**</span></span>
</dt> <dd>

<span data-ttu-id="edcab-153">要加入新服務的資料庫已被鎖定。</span><span class="sxs-lookup"><span data-stu-id="edcab-153">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="edcab-154">**12**</span><span class="sxs-lookup"><span data-stu-id="edcab-154">**12**</span></span>
</dt> <dd>

<span data-ttu-id="edcab-155">這項服務所依賴的相依性已從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="edcab-155">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="edcab-156">**13**</span><span class="sxs-lookup"><span data-stu-id="edcab-156">**13**</span></span>
</dt> <dd>

<span data-ttu-id="edcab-157">服務在相依的服務中找不到所需的服務。</span><span class="sxs-lookup"><span data-stu-id="edcab-157">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="edcab-158">**14**</span><span class="sxs-lookup"><span data-stu-id="edcab-158">**14**</span></span>
</dt> <dd>

<span data-ttu-id="edcab-159">已經從系統中停用服務。</span><span class="sxs-lookup"><span data-stu-id="edcab-159">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="edcab-160">**15**</span><span class="sxs-lookup"><span data-stu-id="edcab-160">**15**</span></span>
</dt> <dd>

<span data-ttu-id="edcab-161">此服務未通過驗證，無法在系統上執行。</span><span class="sxs-lookup"><span data-stu-id="edcab-161">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="edcab-162">**16**</span><span class="sxs-lookup"><span data-stu-id="edcab-162">**16**</span></span>
</dt> <dd>

<span data-ttu-id="edcab-163">這項服務正在從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="edcab-163">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="edcab-164">**17**</span><span class="sxs-lookup"><span data-stu-id="edcab-164">**17**</span></span>
</dt> <dd>

<span data-ttu-id="edcab-165">服務沒有執行執行緒。</span><span class="sxs-lookup"><span data-stu-id="edcab-165">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="edcab-166">**達**</span><span class="sxs-lookup"><span data-stu-id="edcab-166">**18**</span></span>
</dt> <dd>

<span data-ttu-id="edcab-167">服務會在啟動時有迴圈相依性。</span><span class="sxs-lookup"><span data-stu-id="edcab-167">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="edcab-168">**診斷**</span><span class="sxs-lookup"><span data-stu-id="edcab-168">**19**</span></span>
</dt> <dd>

<span data-ttu-id="edcab-169">服務正在相同名稱下執行。</span><span class="sxs-lookup"><span data-stu-id="edcab-169">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="edcab-170">**20**</span><span class="sxs-lookup"><span data-stu-id="edcab-170">**20**</span></span>
</dt> <dd>

<span data-ttu-id="edcab-171">服務名稱包含不正確字元。</span><span class="sxs-lookup"><span data-stu-id="edcab-171">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="edcab-172">**21**</span><span class="sxs-lookup"><span data-stu-id="edcab-172">**21**</span></span>
</dt> <dd>

<span data-ttu-id="edcab-173">傳遞給服務的參數無效。</span><span class="sxs-lookup"><span data-stu-id="edcab-173">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="edcab-174">**22**</span><span class="sxs-lookup"><span data-stu-id="edcab-174">**22**</span></span>
</dt> <dd>

<span data-ttu-id="edcab-175">用來執行此服務的帳戶無效，或缺少執行服務的許可權。</span><span class="sxs-lookup"><span data-stu-id="edcab-175">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="edcab-176">**23**</span><span class="sxs-lookup"><span data-stu-id="edcab-176">**23**</span></span>
</dt> <dd>

<span data-ttu-id="edcab-177">服務存在於系統可使用之服務的資料庫中。</span><span class="sxs-lookup"><span data-stu-id="edcab-177">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="edcab-178">**24**</span><span class="sxs-lookup"><span data-stu-id="edcab-178">**24**</span></span>
</dt> <dd>

<span data-ttu-id="edcab-179">服務目前在系統中暫停。</span><span class="sxs-lookup"><span data-stu-id="edcab-179">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="edcab-180">範例</span><span class="sxs-lookup"><span data-stu-id="edcab-180">Examples</span></span>

<span data-ttu-id="edcab-181">從 TechNet 資源庫提取的服務 PowerShell 範例的下列 [變更 StartMode](https://Gallery.TechNet.Microsoft.Com/6d0f06ed-f840-4228-ad2d-e16ebe6a3aed) 會變更服務的啟動模式。</span><span class="sxs-lookup"><span data-stu-id="edcab-181">The following [Change StartMode of a Service](https://Gallery.TechNet.Microsoft.Com/6d0f06ed-f840-4228-ad2d-e16ebe6a3aed) PowerShell sample, pulled from TechNet Gallery, changes the start mode of a service.</span></span>


```PowerShell
$wmi = get-wmiobject -class win32_service -namespace root\cimv2 -computername lisbon | 
where-object { $_.name -eq 'bits' } 
 
$rtn = $wmi.changestartmode("manual") 
if($rtn.returnvalue -eq 0) { "success" } 
ELSE 
  { " $($rtn.returnvalue) was reported" }
```



## <a name="requirements"></a><span data-ttu-id="edcab-182">規格需求</span><span class="sxs-lookup"><span data-stu-id="edcab-182">Requirements</span></span>



| <span data-ttu-id="edcab-183">需求</span><span class="sxs-lookup"><span data-stu-id="edcab-183">Requirement</span></span> | <span data-ttu-id="edcab-184">值</span><span class="sxs-lookup"><span data-stu-id="edcab-184">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="edcab-185">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="edcab-185">Minimum supported client</span></span><br/> | <span data-ttu-id="edcab-186">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="edcab-186">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="edcab-187">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="edcab-187">Minimum supported server</span></span><br/> | <span data-ttu-id="edcab-188">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="edcab-188">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="edcab-189">命名空間</span><span class="sxs-lookup"><span data-stu-id="edcab-189">Namespace</span></span><br/>                | <span data-ttu-id="edcab-190">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="edcab-190">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="edcab-191">MOF</span><span class="sxs-lookup"><span data-stu-id="edcab-191">MOF</span></span><br/>                      | <dl> <span data-ttu-id="edcab-192"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="edcab-192"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="edcab-193">DLL</span><span class="sxs-lookup"><span data-stu-id="edcab-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="edcab-194"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="edcab-194"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edcab-195">另請參閱</span><span class="sxs-lookup"><span data-stu-id="edcab-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edcab-196">**Win32 \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="edcab-196">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="edcab-197">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="edcab-197">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="edcab-198">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="edcab-198">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="edcab-199">WMI 工作：服務</span><span class="sxs-lookup"><span data-stu-id="edcab-199">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 


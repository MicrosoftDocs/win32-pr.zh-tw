---
title: 'Win32_Service 類別的 ResumeService 方法 (遠端桌面服務) '
description: Win32_Service 類別的 ResumeService 方法 (遠端桌面服務) -嘗試將參考的服務放在恢復狀態。
ms.assetid: AA020A0A-E69C-44AB-B259-A73460728770
ms.tgt_platform: multiple
keywords:
- ResumeService 方法遠端桌面服務
- ResumeService 方法遠端桌面服務，Win32_Service 類別
- Win32_Service 類別遠端桌面服務，ResumeService 方法
topic_type:
- apiref
api_name:
- Win32_Service.ResumeService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94f8e7dcfc9b9bd5b408e36d8a909aa10c84519c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090586"
---
# <a name="resumeservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="98365-106">Win32_Service 類別的 ResumeService 方法 (遠端桌面服務) </span><span class="sxs-lookup"><span data-stu-id="98365-106">ResumeService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="98365-107">**ResumeService** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會嘗試將參考的服務放在恢復狀態。</span><span class="sxs-lookup"><span data-stu-id="98365-107">The **ResumeService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the referenced service in the resumed state.</span></span>

<span data-ttu-id="98365-108">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="98365-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="98365-109">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="98365-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="98365-110">語法</span><span class="sxs-lookup"><span data-stu-id="98365-110">Syntax</span></span>


```mof
uint32 ResumeService();
```



## <a name="parameters"></a><span data-ttu-id="98365-111">參數</span><span class="sxs-lookup"><span data-stu-id="98365-111">Parameters</span></span>

<span data-ttu-id="98365-112">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="98365-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="98365-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="98365-113">Return value</span></span>

<span data-ttu-id="98365-114">傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="98365-114">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="98365-115">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="98365-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="98365-116">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="98365-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="98365-117">**0**</span><span class="sxs-lookup"><span data-stu-id="98365-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="98365-118">要求已被接受。</span><span class="sxs-lookup"><span data-stu-id="98365-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="98365-119">**1**</span><span class="sxs-lookup"><span data-stu-id="98365-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="98365-120">不支援此要求。</span><span class="sxs-lookup"><span data-stu-id="98365-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="98365-121">**2**</span><span class="sxs-lookup"><span data-stu-id="98365-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="98365-122">使用者沒有必要的存取權。</span><span class="sxs-lookup"><span data-stu-id="98365-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="98365-123">**3**</span><span class="sxs-lookup"><span data-stu-id="98365-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="98365-124">無法停止此服務，因為與它相依的其他服務正在執行中。</span><span class="sxs-lookup"><span data-stu-id="98365-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="98365-125">**4**</span><span class="sxs-lookup"><span data-stu-id="98365-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="98365-126">要求的控制碼無效，或是服務不接受此控制碼。</span><span class="sxs-lookup"><span data-stu-id="98365-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="98365-127">**5**</span><span class="sxs-lookup"><span data-stu-id="98365-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="98365-128">因為服務的狀態 ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)，所以無法將要求的控制項程式碼傳送至服務。**State** 屬性) 等於0、1或2。</span><span class="sxs-lookup"><span data-stu-id="98365-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="98365-129">**6**</span><span class="sxs-lookup"><span data-stu-id="98365-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="98365-130">尚未啟動服務。</span><span class="sxs-lookup"><span data-stu-id="98365-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="98365-131">**7**</span><span class="sxs-lookup"><span data-stu-id="98365-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="98365-132">服務並未及時回應啟動要求。</span><span class="sxs-lookup"><span data-stu-id="98365-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="98365-133">**8**</span><span class="sxs-lookup"><span data-stu-id="98365-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="98365-134">啟動服務時發生未知的錯誤。</span><span class="sxs-lookup"><span data-stu-id="98365-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="98365-135">**9**</span><span class="sxs-lookup"><span data-stu-id="98365-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="98365-136">找不到服務可執行檔的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="98365-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="98365-137">**10**</span><span class="sxs-lookup"><span data-stu-id="98365-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="98365-138">服務已在執行中。</span><span class="sxs-lookup"><span data-stu-id="98365-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="98365-139">**11**</span><span class="sxs-lookup"><span data-stu-id="98365-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="98365-140">要加入新服務的資料庫已被鎖定。</span><span class="sxs-lookup"><span data-stu-id="98365-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="98365-141">**12**</span><span class="sxs-lookup"><span data-stu-id="98365-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="98365-142">這項服務所依賴的相依性已從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="98365-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="98365-143">**13**</span><span class="sxs-lookup"><span data-stu-id="98365-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="98365-144">服務在相依的服務中找不到所需的服務。</span><span class="sxs-lookup"><span data-stu-id="98365-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="98365-145">**14**</span><span class="sxs-lookup"><span data-stu-id="98365-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="98365-146">已經從系統中停用服務。</span><span class="sxs-lookup"><span data-stu-id="98365-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="98365-147">**15**</span><span class="sxs-lookup"><span data-stu-id="98365-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="98365-148">此服務未通過驗證，無法在系統上執行。</span><span class="sxs-lookup"><span data-stu-id="98365-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="98365-149">**16**</span><span class="sxs-lookup"><span data-stu-id="98365-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="98365-150">這項服務正在從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="98365-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="98365-151">**17**</span><span class="sxs-lookup"><span data-stu-id="98365-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="98365-152">服務沒有執行執行緒。</span><span class="sxs-lookup"><span data-stu-id="98365-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="98365-153">**達**</span><span class="sxs-lookup"><span data-stu-id="98365-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="98365-154">服務會在啟動時有迴圈相依性。</span><span class="sxs-lookup"><span data-stu-id="98365-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="98365-155">**診斷**</span><span class="sxs-lookup"><span data-stu-id="98365-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="98365-156">服務正在相同名稱下執行。</span><span class="sxs-lookup"><span data-stu-id="98365-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="98365-157">**20**</span><span class="sxs-lookup"><span data-stu-id="98365-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="98365-158">服務名稱包含不正確字元。</span><span class="sxs-lookup"><span data-stu-id="98365-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="98365-159">**21**</span><span class="sxs-lookup"><span data-stu-id="98365-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="98365-160">傳遞給服務的參數無效。</span><span class="sxs-lookup"><span data-stu-id="98365-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="98365-161">**22**</span><span class="sxs-lookup"><span data-stu-id="98365-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="98365-162">用來執行此服務的帳戶無效，或缺少執行服務的許可權。</span><span class="sxs-lookup"><span data-stu-id="98365-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="98365-163">**23**</span><span class="sxs-lookup"><span data-stu-id="98365-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="98365-164">服務存在於系統可使用之服務的資料庫中。</span><span class="sxs-lookup"><span data-stu-id="98365-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="98365-165">**24**</span><span class="sxs-lookup"><span data-stu-id="98365-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="98365-166">服務目前在系統中暫停。</span><span class="sxs-lookup"><span data-stu-id="98365-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="98365-167">備註</span><span class="sxs-lookup"><span data-stu-id="98365-167">Remarks</span></span>

<span data-ttu-id="98365-168">雖然已停止的服務和暫停的服務之間似乎沒有任何實際的差異，但是這兩個狀態會與 SCM 以不同方式顯示。</span><span class="sxs-lookup"><span data-stu-id="98365-168">Although there might appear to be no practical difference between a service that is stopped and a service that is paused, the two states appear differently to the SCM.</span></span> <span data-ttu-id="98365-169">已停止的服務是指未執行的服務，必須經過整個服務啟動程式。</span><span class="sxs-lookup"><span data-stu-id="98365-169">A stopped service is a service that is not running and must go through the entire service start procedure.</span></span> <span data-ttu-id="98365-170">不過，已暫停的服務仍在執行中，但其運作已暫止。</span><span class="sxs-lookup"><span data-stu-id="98365-170">A paused service, however, is still running but has had its functioning is suspended.</span></span> <span data-ttu-id="98365-171">因此，已暫停的服務不需要經過整個服務啟動程式，但需要不同的程式來繼續運作。</span><span class="sxs-lookup"><span data-stu-id="98365-171">Because of this, a paused service does not need to go through the entire service start procedure but needs a different procedure to resume functioning.</span></span>

<span data-ttu-id="98365-172">您必須使用適當的方法來啟動已停止的服務，或繼續已暫停的服務。</span><span class="sxs-lookup"><span data-stu-id="98365-172">You must use the proper method to start a service that has been stopped or to resume a service that has been paused.</span></span> <span data-ttu-id="98365-173">在下列情況下，應該使用 [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service) 方法 [**StartService**](win32-terminalservice-startservice.md) 和 **ResumeService** ：</span><span class="sxs-lookup"><span data-stu-id="98365-173">The [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) methods [**StartService**](win32-terminalservice-startservice.md) and **ResumeService** should be used in the following situations:</span></span>

-   <span data-ttu-id="98365-174">如果服務目前已停止，您必須使用 [**StartService**](win32-terminalservice-startservice.md) 方法來重新開機它。 **ResumeService** 無法啟動目前已停止的服務。</span><span class="sxs-lookup"><span data-stu-id="98365-174">If a service is currently stopped, you must use the [**StartService**](win32-terminalservice-startservice.md) method to restart it; **ResumeService** cannot start a service that is currently stopped.</span></span>
-   <span data-ttu-id="98365-175">如果服務暫停，您必須使用 **ResumeService**。</span><span class="sxs-lookup"><span data-stu-id="98365-175">If a service is paused, you must use **ResumeService**.</span></span> <span data-ttu-id="98365-176">如果您在已暫停的服務上使用 [**StartService**](win32-terminalservice-startservice.md) 方法，您會收到「服務已在執行中」的訊息。</span><span class="sxs-lookup"><span data-stu-id="98365-176">If you use the [**StartService**](win32-terminalservice-startservice.md) method on a paused service, you receive the message, "The service is already running."</span></span> <span data-ttu-id="98365-177">不過，在繼續服務控制程式代碼傳送給它之前，服務會保持暫停狀態。</span><span class="sxs-lookup"><span data-stu-id="98365-177">However, the service remains paused until the resume service control code is sent to it.</span></span>

## <a name="examples"></a><span data-ttu-id="98365-178">範例</span><span class="sxs-lookup"><span data-stu-id="98365-178">Examples</span></span>

<span data-ttu-id="98365-179">已暫停 VBScript 範例的 Resume 自動啟動 [服務會](https://Gallery.TechNet.Microsoft.Com/413f2896-e7f3-4b3e-96cb-5abdc9bb6c36) 重新開機已暫停的任何自動啟動服務。</span><span class="sxs-lookup"><span data-stu-id="98365-179">The [Resume AutoStart Services that are Paused](https://Gallery.TechNet.Microsoft.Com/413f2896-e7f3-4b3e-96cb-5abdc9bb6c36) VBScript sample restarts any auto-start services that have been paused.</span></span>

## <a name="requirements"></a><span data-ttu-id="98365-180">規格需求</span><span class="sxs-lookup"><span data-stu-id="98365-180">Requirements</span></span>



| <span data-ttu-id="98365-181">需求</span><span class="sxs-lookup"><span data-stu-id="98365-181">Requirement</span></span> | <span data-ttu-id="98365-182">值</span><span class="sxs-lookup"><span data-stu-id="98365-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="98365-183">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="98365-183">Minimum supported client</span></span><br/> | <span data-ttu-id="98365-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="98365-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="98365-185">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="98365-185">Minimum supported server</span></span><br/> | <span data-ttu-id="98365-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="98365-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="98365-187">命名空間</span><span class="sxs-lookup"><span data-stu-id="98365-187">Namespace</span></span><br/>                | <span data-ttu-id="98365-188">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="98365-188">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="98365-189">MOF</span><span class="sxs-lookup"><span data-stu-id="98365-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="98365-190"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="98365-190"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="98365-191">DLL</span><span class="sxs-lookup"><span data-stu-id="98365-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98365-192"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98365-192"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98365-193">另請參閱</span><span class="sxs-lookup"><span data-stu-id="98365-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98365-194">**Win32 \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="98365-194">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="98365-195">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="98365-195">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="98365-196">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="98365-196">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="98365-197">WMI 工作：服務</span><span class="sxs-lookup"><span data-stu-id="98365-197">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 


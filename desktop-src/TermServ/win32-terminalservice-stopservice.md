---
title: 'Win32_Service 類別的 StopService 方法 (Sdoias)  (終端機服務) '
description: 將由 Win32 TerminalService 物件表示的服務置於 \_ 已停止狀態。
ms.assetid: 228711DC-369B-48B6-96EE-DF4026904E26
ms.tgt_platform: multiple
keywords:
- StopService 方法遠端桌面服務
- StopService 方法遠端桌面服務，Win32_Service 類別
- Win32_Service 類別遠端桌面服務，StopService 方法
topic_type:
- apiref
api_name:
- Win32_Service.StopService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e1b21db330bb9111b96fb244200845cb83b3153
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/26/2021
ms.locfileid: "106997805"
---
# <a name="stopservice-method-of-the-win32_service-class-sdoiash-for-the-terminal-service"></a><span data-ttu-id="c1b06-106">適用于終端機服務的 Win32_Service 類別的 StopService 方法 (Sdoias .h) </span><span class="sxs-lookup"><span data-stu-id="c1b06-106">StopService method of the Win32_Service class (Sdoias.h) for the Terminal service</span></span>

<span data-ttu-id="c1b06-107">**StopService** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會將服務（由 [**Win32 \_ TerminalService**](win32-terminalservice.md)物件表示）置於已停止狀態。</span><span class="sxs-lookup"><span data-stu-id="c1b06-107">The **StopService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method places the service, represented by the [**Win32\_TerminalService**](win32-terminalservice.md) object, in the stopped state.</span></span>

<span data-ttu-id="c1b06-108">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="c1b06-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c1b06-109">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="c1b06-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c1b06-110">語法</span><span class="sxs-lookup"><span data-stu-id="c1b06-110">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="c1b06-111">參數</span><span class="sxs-lookup"><span data-stu-id="c1b06-111">Parameters</span></span>

<span data-ttu-id="c1b06-112">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="c1b06-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c1b06-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="c1b06-113">Return value</span></span>

<span data-ttu-id="c1b06-114">傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="c1b06-114">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="c1b06-115">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="c1b06-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="c1b06-116">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="c1b06-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="c1b06-117">**0**</span><span class="sxs-lookup"><span data-stu-id="c1b06-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="c1b06-118">要求已被接受。</span><span class="sxs-lookup"><span data-stu-id="c1b06-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="c1b06-119">**1**</span><span class="sxs-lookup"><span data-stu-id="c1b06-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="c1b06-120">不支援此要求。</span><span class="sxs-lookup"><span data-stu-id="c1b06-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="c1b06-121">**2**</span><span class="sxs-lookup"><span data-stu-id="c1b06-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="c1b06-122">使用者沒有必要的存取權。</span><span class="sxs-lookup"><span data-stu-id="c1b06-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="c1b06-123">**3**</span><span class="sxs-lookup"><span data-stu-id="c1b06-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="c1b06-124">無法停止此服務，因為與它相依的其他服務正在執行中。</span><span class="sxs-lookup"><span data-stu-id="c1b06-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="c1b06-125">**4**</span><span class="sxs-lookup"><span data-stu-id="c1b06-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="c1b06-126">要求的控制碼無效，或是服務不接受此控制碼。</span><span class="sxs-lookup"><span data-stu-id="c1b06-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="c1b06-127">**5**</span><span class="sxs-lookup"><span data-stu-id="c1b06-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="c1b06-128">因為服務的狀態 ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)，所以無法將要求的控制項程式碼傳送至服務。**State** 屬性) 等於0、1或2。</span><span class="sxs-lookup"><span data-stu-id="c1b06-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="c1b06-129">**6**</span><span class="sxs-lookup"><span data-stu-id="c1b06-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="c1b06-130">尚未啟動服務。</span><span class="sxs-lookup"><span data-stu-id="c1b06-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="c1b06-131">**7**</span><span class="sxs-lookup"><span data-stu-id="c1b06-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="c1b06-132">服務並未及時回應啟動要求。</span><span class="sxs-lookup"><span data-stu-id="c1b06-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="c1b06-133">**8**</span><span class="sxs-lookup"><span data-stu-id="c1b06-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="c1b06-134">啟動服務時發生未知的錯誤。</span><span class="sxs-lookup"><span data-stu-id="c1b06-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="c1b06-135">**9**</span><span class="sxs-lookup"><span data-stu-id="c1b06-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="c1b06-136">找不到服務可執行檔的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="c1b06-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="c1b06-137">**10**</span><span class="sxs-lookup"><span data-stu-id="c1b06-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="c1b06-138">服務已在執行中。</span><span class="sxs-lookup"><span data-stu-id="c1b06-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="c1b06-139">**11**</span><span class="sxs-lookup"><span data-stu-id="c1b06-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="c1b06-140">要加入新服務的資料庫已被鎖定。</span><span class="sxs-lookup"><span data-stu-id="c1b06-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="c1b06-141">**12**</span><span class="sxs-lookup"><span data-stu-id="c1b06-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="c1b06-142">這項服務所依賴的相依性已從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="c1b06-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c1b06-143">**13**</span><span class="sxs-lookup"><span data-stu-id="c1b06-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="c1b06-144">服務在相依的服務中找不到所需的服務。</span><span class="sxs-lookup"><span data-stu-id="c1b06-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="c1b06-145">**14**</span><span class="sxs-lookup"><span data-stu-id="c1b06-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="c1b06-146">已經從系統中停用服務。</span><span class="sxs-lookup"><span data-stu-id="c1b06-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c1b06-147">**15**</span><span class="sxs-lookup"><span data-stu-id="c1b06-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="c1b06-148">此服務未通過驗證，無法在系統上執行。</span><span class="sxs-lookup"><span data-stu-id="c1b06-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="c1b06-149">**16**</span><span class="sxs-lookup"><span data-stu-id="c1b06-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="c1b06-150">這項服務正在從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="c1b06-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c1b06-151">**17**</span><span class="sxs-lookup"><span data-stu-id="c1b06-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="c1b06-152">服務沒有執行執行緒。</span><span class="sxs-lookup"><span data-stu-id="c1b06-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="c1b06-153">**達**</span><span class="sxs-lookup"><span data-stu-id="c1b06-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="c1b06-154">服務會在啟動時有迴圈相依性。</span><span class="sxs-lookup"><span data-stu-id="c1b06-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="c1b06-155">**診斷**</span><span class="sxs-lookup"><span data-stu-id="c1b06-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="c1b06-156">服務正在相同名稱下執行。</span><span class="sxs-lookup"><span data-stu-id="c1b06-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="c1b06-157">**20**</span><span class="sxs-lookup"><span data-stu-id="c1b06-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="c1b06-158">服務名稱包含不正確字元。</span><span class="sxs-lookup"><span data-stu-id="c1b06-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="c1b06-159">**21**</span><span class="sxs-lookup"><span data-stu-id="c1b06-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="c1b06-160">傳遞給服務的參數無效。</span><span class="sxs-lookup"><span data-stu-id="c1b06-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="c1b06-161">**22**</span><span class="sxs-lookup"><span data-stu-id="c1b06-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="c1b06-162">用來執行此服務的帳戶無效，或缺少執行服務的許可權。</span><span class="sxs-lookup"><span data-stu-id="c1b06-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="c1b06-163">**23**</span><span class="sxs-lookup"><span data-stu-id="c1b06-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="c1b06-164">服務存在於系統可使用之服務的資料庫中。</span><span class="sxs-lookup"><span data-stu-id="c1b06-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c1b06-165">**24**</span><span class="sxs-lookup"><span data-stu-id="c1b06-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="c1b06-166">服務目前在系統中暫停。</span><span class="sxs-lookup"><span data-stu-id="c1b06-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c1b06-167">備註</span><span class="sxs-lookup"><span data-stu-id="c1b06-167">Remarks</span></span>

<span data-ttu-id="c1b06-168">確定可以停止或暫停的服務之後，您可以使用 **StopService** 和 [**PauseService**](win32-terminalservice-pauseservice.md) 方法來停止和暫停服務。</span><span class="sxs-lookup"><span data-stu-id="c1b06-168">After you have determined which services can be stopped or paused, you can use the **StopService** and [**PauseService**](win32-terminalservice-pauseservice.md) methods to stop and pause services.</span></span> <span data-ttu-id="c1b06-169">停止服務而非暫停服務（反之亦然）的決策取決於數個因素，包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="c1b06-169">The decision to stop a service rather than pause it, or vice versa, depends on several factors, including the following:</span></span>

-   <span data-ttu-id="c1b06-170">服務是否能夠暫停？</span><span class="sxs-lookup"><span data-stu-id="c1b06-170">Is the service capable of being paused?</span></span> <span data-ttu-id="c1b06-171">如果沒有，則您的唯一選項是停止服務。</span><span class="sxs-lookup"><span data-stu-id="c1b06-171">If not, your only option is the stop the service.</span></span>
-   <span data-ttu-id="c1b06-172">您是否需要繼續處理已連線到服務的任何人的用戶端要求？</span><span class="sxs-lookup"><span data-stu-id="c1b06-172">Do you need to continue handling client requests for anyone already connected to the service?</span></span> <span data-ttu-id="c1b06-173">若是如此，暫停服務通常會允許它處理現有的用戶端，同時拒絕存取新的用戶端。</span><span class="sxs-lookup"><span data-stu-id="c1b06-173">If so, pausing a service typically allows it to handle existing clients while denying access to new clients.</span></span> <span data-ttu-id="c1b06-174">相反地，當您停止服務時，所有用戶端都會立即中斷連線。</span><span class="sxs-lookup"><span data-stu-id="c1b06-174">By contrast, when you stop a service, all clients are immediately disconnected.</span></span>
-   <span data-ttu-id="c1b06-175">您是否需要重新設定服務，並讓變更立即生效？</span><span class="sxs-lookup"><span data-stu-id="c1b06-175">Do you need to reconfigure a service and have the changes take effect immediately?</span></span> <span data-ttu-id="c1b06-176">雖然服務屬性可以在服務暫停時變更，但大部分的服務都不會在服務實際停止並重新啟動之前生效。</span><span class="sxs-lookup"><span data-stu-id="c1b06-176">Although service properties can be changed while a service is paused, most of them do not take effect until the service is actually stopped and restarted.</span></span>

<span data-ttu-id="c1b06-177">停止服務所需的腳本程式碼與暫停服務所需的程式碼幾乎完全相同。</span><span class="sxs-lookup"><span data-stu-id="c1b06-177">The scripting code required to stop a service is almost identical to the code required to pause the service.</span></span>

<span data-ttu-id="c1b06-178">如果您嘗試停止具有相依服務的服務正在執行， **StopService** 方法會失敗，並傳回值3。</span><span class="sxs-lookup"><span data-stu-id="c1b06-178">If you attempt to stop a service which has dependent services running, the **StopService** method fails with a return value of 3.</span></span> <span data-ttu-id="c1b06-179">必須先停止相依的服務。</span><span class="sxs-lookup"><span data-stu-id="c1b06-179">The dependent services must be stopped first.</span></span>

<span data-ttu-id="c1b06-180">如果您停止服務，請立即檢查 [**Win32 \_ TerminalService**](win32-terminalservice.md)。**狀態** 屬性，因為值仍可能顯示服務為執行中。</span><span class="sxs-lookup"><span data-stu-id="c1b06-180">If you stop a service, then immediately check the [**Win32\_TerminalService**](win32-terminalservice.md).**State** property, as the value may still show the service as running.</span></span>

## <a name="examples"></a><span data-ttu-id="c1b06-181">範例</span><span class="sxs-lookup"><span data-stu-id="c1b06-181">Examples</span></span>

<span data-ttu-id="c1b06-182">[RemoteService](https://Gallery.TechNet.Microsoft.Com/79595ce9-bfc3-463e-9e84-d9e0b78590c1) PowerShell 範例會設定遠端電腦的服務狀態。</span><span class="sxs-lookup"><span data-stu-id="c1b06-182">[The Set-RemoteService](https://Gallery.TechNet.Microsoft.Com/79595ce9-bfc3-463e-9e84-d9e0b78590c1) PowerShell sample Sets service state for remote machines.</span></span>

<span data-ttu-id="c1b06-183">[停止服務及其相依的](https://Gallery.TechNet.Microsoft.Com/ae07e623-2cbd-4983-b991-aa4d1e6e2732)VBScript 範例會停止服務和所有相依的服務。</span><span class="sxs-lookup"><span data-stu-id="c1b06-183">The [Stop a Service and Its Dependents](https://Gallery.TechNet.Microsoft.Com/ae07e623-2cbd-4983-b991-aa4d1e6e2732) VBScript sample stops a service and all dependent services.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1b06-184">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1b06-184">Requirements</span></span>



| <span data-ttu-id="c1b06-185">需求</span><span class="sxs-lookup"><span data-stu-id="c1b06-185">Requirement</span></span> | <span data-ttu-id="c1b06-186">值</span><span class="sxs-lookup"><span data-stu-id="c1b06-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1b06-187">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c1b06-187">Minimum supported client</span></span><br/> | <span data-ttu-id="c1b06-188">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c1b06-188">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c1b06-189">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c1b06-189">Minimum supported server</span></span><br/> | <span data-ttu-id="c1b06-190">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c1b06-190">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c1b06-191">命名空間</span><span class="sxs-lookup"><span data-stu-id="c1b06-191">Namespace</span></span><br/>                | <span data-ttu-id="c1b06-192">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="c1b06-192">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="c1b06-193">標頭</span><span class="sxs-lookup"><span data-stu-id="c1b06-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1b06-194"><dt>Sdoias。h</dt></span><span class="sxs-lookup"><span data-stu-id="c1b06-194"><dt>Sdoias.h</dt></span></span> </dl>     |
| <span data-ttu-id="c1b06-195">MOF</span><span class="sxs-lookup"><span data-stu-id="c1b06-195">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c1b06-196"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="c1b06-196"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="c1b06-197">DLL</span><span class="sxs-lookup"><span data-stu-id="c1b06-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1b06-198"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1b06-198"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1b06-199">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c1b06-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1b06-200">**Win32 \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="c1b06-200">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="c1b06-201">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="c1b06-201">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="c1b06-202">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="c1b06-202">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="c1b06-203">WMI 工作：服務</span><span class="sxs-lookup"><span data-stu-id="c1b06-203">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[<span data-ttu-id="c1b06-204">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="c1b06-204">**PauseService**</span></span>](/windows/desktop/CIMWin32Prov/pauseservice-method-in-class-win32-systemdriver)
</dt> </dl>

 


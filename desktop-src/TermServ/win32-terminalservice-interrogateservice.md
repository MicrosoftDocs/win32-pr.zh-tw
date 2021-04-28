---
title: 'Win32_Service 類別的 InterrogateService 方法 (遠端桌面服務) '
description: Win32_Service 類別的 InterrogateService 方法 (遠端桌面服務) -要求參考的服務將其狀態更新為 Service manager。
ms.assetid: 7B572049-416E-4429-BD53-119FF570B2D8
ms.tgt_platform: multiple
keywords:
- InterrogateService 方法遠端桌面服務
- InterrogateService 方法遠端桌面服務，Win32_Service 類別
- Win32_Service 類別遠端桌面服務，InterrogateService 方法
topic_type:
- apiref
api_name:
- Win32_Service.InterrogateService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 850953b210ea11b9dd1000326d6793e3651ce538
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090656"
---
# <a name="interrogateservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="b73bd-106">Win32_Service 類別的 InterrogateService 方法 (遠端桌面服務) </span><span class="sxs-lookup"><span data-stu-id="b73bd-106">InterrogateService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="b73bd-107">**InterrogateService** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會要求參考的服務將其狀態更新為 service manager。</span><span class="sxs-lookup"><span data-stu-id="b73bd-107">The **InterrogateService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method requests that the referenced service update its state to the service manager.</span></span>

<span data-ttu-id="b73bd-108">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="b73bd-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b73bd-109">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="b73bd-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b73bd-110">語法</span><span class="sxs-lookup"><span data-stu-id="b73bd-110">Syntax</span></span>


```mof
uint32 InterrogateService();
```



## <a name="parameters"></a><span data-ttu-id="b73bd-111">參數</span><span class="sxs-lookup"><span data-stu-id="b73bd-111">Parameters</span></span>

<span data-ttu-id="b73bd-112">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="b73bd-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b73bd-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="b73bd-113">Return value</span></span>

<span data-ttu-id="b73bd-114">傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="b73bd-114">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="b73bd-115">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="b73bd-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="b73bd-116">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="b73bd-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="b73bd-117">**0**</span><span class="sxs-lookup"><span data-stu-id="b73bd-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="b73bd-118">要求已被接受。</span><span class="sxs-lookup"><span data-stu-id="b73bd-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="b73bd-119">**1**</span><span class="sxs-lookup"><span data-stu-id="b73bd-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="b73bd-120">不支援此要求。</span><span class="sxs-lookup"><span data-stu-id="b73bd-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="b73bd-121">**2**</span><span class="sxs-lookup"><span data-stu-id="b73bd-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="b73bd-122">使用者沒有必要的存取權。</span><span class="sxs-lookup"><span data-stu-id="b73bd-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="b73bd-123">**3**</span><span class="sxs-lookup"><span data-stu-id="b73bd-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="b73bd-124">無法停止此服務，因為與它相依的其他服務正在執行中。</span><span class="sxs-lookup"><span data-stu-id="b73bd-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="b73bd-125">**4**</span><span class="sxs-lookup"><span data-stu-id="b73bd-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="b73bd-126">要求的控制碼無效，或是服務不接受此控制碼。</span><span class="sxs-lookup"><span data-stu-id="b73bd-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="b73bd-127">**5**</span><span class="sxs-lookup"><span data-stu-id="b73bd-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="b73bd-128">因為服務的狀態 ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)，所以無法將要求的控制項程式碼傳送至服務。**State** 屬性) 等於0、1或2。</span><span class="sxs-lookup"><span data-stu-id="b73bd-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="b73bd-129">**6**</span><span class="sxs-lookup"><span data-stu-id="b73bd-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="b73bd-130">尚未啟動服務。</span><span class="sxs-lookup"><span data-stu-id="b73bd-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="b73bd-131">**7**</span><span class="sxs-lookup"><span data-stu-id="b73bd-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="b73bd-132">服務並未及時回應啟動要求。</span><span class="sxs-lookup"><span data-stu-id="b73bd-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="b73bd-133">**8**</span><span class="sxs-lookup"><span data-stu-id="b73bd-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="b73bd-134">啟動服務時發生未知的錯誤。</span><span class="sxs-lookup"><span data-stu-id="b73bd-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="b73bd-135">**9**</span><span class="sxs-lookup"><span data-stu-id="b73bd-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="b73bd-136">找不到服務可執行檔的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="b73bd-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="b73bd-137">**10**</span><span class="sxs-lookup"><span data-stu-id="b73bd-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="b73bd-138">服務已在執行中。</span><span class="sxs-lookup"><span data-stu-id="b73bd-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="b73bd-139">**11**</span><span class="sxs-lookup"><span data-stu-id="b73bd-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="b73bd-140">要加入新服務的資料庫已被鎖定。</span><span class="sxs-lookup"><span data-stu-id="b73bd-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="b73bd-141">**12**</span><span class="sxs-lookup"><span data-stu-id="b73bd-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="b73bd-142">這項服務所依賴的相依性已從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="b73bd-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="b73bd-143">**13**</span><span class="sxs-lookup"><span data-stu-id="b73bd-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="b73bd-144">服務在相依的服務中找不到所需的服務。</span><span class="sxs-lookup"><span data-stu-id="b73bd-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="b73bd-145">**14**</span><span class="sxs-lookup"><span data-stu-id="b73bd-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="b73bd-146">已經從系統中停用服務。</span><span class="sxs-lookup"><span data-stu-id="b73bd-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="b73bd-147">**15**</span><span class="sxs-lookup"><span data-stu-id="b73bd-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="b73bd-148">此服務未通過驗證，無法在系統上執行。</span><span class="sxs-lookup"><span data-stu-id="b73bd-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="b73bd-149">**16**</span><span class="sxs-lookup"><span data-stu-id="b73bd-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="b73bd-150">這項服務正在從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="b73bd-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="b73bd-151">**17**</span><span class="sxs-lookup"><span data-stu-id="b73bd-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="b73bd-152">服務沒有執行執行緒。</span><span class="sxs-lookup"><span data-stu-id="b73bd-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="b73bd-153">**達**</span><span class="sxs-lookup"><span data-stu-id="b73bd-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="b73bd-154">服務會在啟動時有迴圈相依性。</span><span class="sxs-lookup"><span data-stu-id="b73bd-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="b73bd-155">**診斷**</span><span class="sxs-lookup"><span data-stu-id="b73bd-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="b73bd-156">服務正在相同名稱下執行。</span><span class="sxs-lookup"><span data-stu-id="b73bd-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="b73bd-157">**20**</span><span class="sxs-lookup"><span data-stu-id="b73bd-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="b73bd-158">服務名稱包含不正確字元。</span><span class="sxs-lookup"><span data-stu-id="b73bd-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="b73bd-159">**21**</span><span class="sxs-lookup"><span data-stu-id="b73bd-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="b73bd-160">傳遞給服務的參數無效。</span><span class="sxs-lookup"><span data-stu-id="b73bd-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="b73bd-161">**22**</span><span class="sxs-lookup"><span data-stu-id="b73bd-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="b73bd-162">用來執行此服務的帳戶無效，或缺少執行服務的許可權。</span><span class="sxs-lookup"><span data-stu-id="b73bd-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="b73bd-163">**23**</span><span class="sxs-lookup"><span data-stu-id="b73bd-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="b73bd-164">服務存在於系統可使用之服務的資料庫中。</span><span class="sxs-lookup"><span data-stu-id="b73bd-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="b73bd-165">**24**</span><span class="sxs-lookup"><span data-stu-id="b73bd-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="b73bd-166">服務目前在系統中暫停。</span><span class="sxs-lookup"><span data-stu-id="b73bd-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b73bd-167">規格需求</span><span class="sxs-lookup"><span data-stu-id="b73bd-167">Requirements</span></span>



| <span data-ttu-id="b73bd-168">需求</span><span class="sxs-lookup"><span data-stu-id="b73bd-168">Requirement</span></span> | <span data-ttu-id="b73bd-169">值</span><span class="sxs-lookup"><span data-stu-id="b73bd-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b73bd-170">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b73bd-170">Minimum supported client</span></span><br/> | <span data-ttu-id="b73bd-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b73bd-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b73bd-172">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b73bd-172">Minimum supported server</span></span><br/> | <span data-ttu-id="b73bd-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b73bd-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b73bd-174">命名空間</span><span class="sxs-lookup"><span data-stu-id="b73bd-174">Namespace</span></span><br/>                | <span data-ttu-id="b73bd-175">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="b73bd-175">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="b73bd-176">MOF</span><span class="sxs-lookup"><span data-stu-id="b73bd-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b73bd-177"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="b73bd-177"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="b73bd-178">DLL</span><span class="sxs-lookup"><span data-stu-id="b73bd-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b73bd-179"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b73bd-179"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b73bd-180">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b73bd-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b73bd-181">**Win32 \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="b73bd-181">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="b73bd-182">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="b73bd-182">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="b73bd-183">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="b73bd-183">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="b73bd-184">WMI 工作：服務</span><span class="sxs-lookup"><span data-stu-id="b73bd-184">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 


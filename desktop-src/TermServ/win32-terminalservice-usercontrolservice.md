---
title: 'Win32_Service 類別的 UserControlService 方法 (遠端桌面服務) '
description: Win32_Service 類別的 UserControlService 方法 (遠端桌面服務) -嘗試傳送使用者定義的控制項程式碼至參考的服務。
ms.assetid: 7B9020C1-2183-4FC4-ABCF-CE34111FF5D3
ms.tgt_platform: multiple
keywords:
- UserControlService 方法遠端桌面服務
- UserControlService 方法遠端桌面服務，Win32_Service 類別
- Win32_Service 類別遠端桌面服務，UserControlService 方法
topic_type:
- apiref
api_name:
- Win32_Service.UserControlService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e71a33056f596afaf577968a5c725b3f64f79b6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090606"
---
# <a name="usercontrolservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="a1544-106">Win32_Service 類別的 UserControlService 方法 (遠端桌面服務) </span><span class="sxs-lookup"><span data-stu-id="a1544-106">UserControlService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="a1544-107">**UserControlService** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會嘗試將使用者定義的控制項程式碼傳送至參考的服務。</span><span class="sxs-lookup"><span data-stu-id="a1544-107">The **UserControlService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to send a user-defined control code to the referenced service.</span></span>

<span data-ttu-id="a1544-108">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="a1544-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a1544-109">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="a1544-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a1544-110">語法</span><span class="sxs-lookup"><span data-stu-id="a1544-110">Syntax</span></span>


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a><span data-ttu-id="a1544-111">參數</span><span class="sxs-lookup"><span data-stu-id="a1544-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1544-112">*ControlCode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a1544-112">*ControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1544-113">指定從128到 255) 的定義值，這些 (值會提供使用者特定的控制項命令。</span><span class="sxs-lookup"><span data-stu-id="a1544-113">Specifies defined values (from 128 to 255) that provide control commands specific to a user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1544-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="a1544-114">Return value</span></span>

<span data-ttu-id="a1544-115">傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="a1544-115">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="a1544-116">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="a1544-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="a1544-117">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="a1544-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="a1544-118">**0**</span><span class="sxs-lookup"><span data-stu-id="a1544-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="a1544-119">要求已被接受。</span><span class="sxs-lookup"><span data-stu-id="a1544-119">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="a1544-120">**1**</span><span class="sxs-lookup"><span data-stu-id="a1544-120">**1**</span></span>
</dt> <dd>

<span data-ttu-id="a1544-121">不支援此要求。</span><span class="sxs-lookup"><span data-stu-id="a1544-121">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="a1544-122">**2**</span><span class="sxs-lookup"><span data-stu-id="a1544-122">**2**</span></span>
</dt> <dd>

<span data-ttu-id="a1544-123">使用者沒有必要的存取權。</span><span class="sxs-lookup"><span data-stu-id="a1544-123">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="a1544-124">**3**</span><span class="sxs-lookup"><span data-stu-id="a1544-124">**3**</span></span>
</dt> <dd>

<span data-ttu-id="a1544-125">無法停止此服務，因為與它相依的其他服務正在執行中。</span><span class="sxs-lookup"><span data-stu-id="a1544-125">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="a1544-126">**4**</span><span class="sxs-lookup"><span data-stu-id="a1544-126">**4**</span></span>
</dt> <dd>

<span data-ttu-id="a1544-127">要求的控制碼無效，或是服務不接受此控制碼。</span><span class="sxs-lookup"><span data-stu-id="a1544-127">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="a1544-128">**5**</span><span class="sxs-lookup"><span data-stu-id="a1544-128">**5**</span></span>
</dt> <dd>

<span data-ttu-id="a1544-129">因為服務的狀態 ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)，所以無法將要求的控制項程式碼傳送至服務。**State** 屬性) 等於0、1或2。</span><span class="sxs-lookup"><span data-stu-id="a1544-129">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="a1544-130">**6**</span><span class="sxs-lookup"><span data-stu-id="a1544-130">**6**</span></span>
</dt> <dd>

<span data-ttu-id="a1544-131">尚未啟動服務。</span><span class="sxs-lookup"><span data-stu-id="a1544-131">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="a1544-132">**7**</span><span class="sxs-lookup"><span data-stu-id="a1544-132">**7**</span></span>
</dt> <dd>

<span data-ttu-id="a1544-133">服務並未及時回應啟動要求。</span><span class="sxs-lookup"><span data-stu-id="a1544-133">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="a1544-134">**8**</span><span class="sxs-lookup"><span data-stu-id="a1544-134">**8**</span></span>
</dt> <dd>

<span data-ttu-id="a1544-135">啟動服務時發生未知的錯誤。</span><span class="sxs-lookup"><span data-stu-id="a1544-135">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="a1544-136">**9**</span><span class="sxs-lookup"><span data-stu-id="a1544-136">**9**</span></span>
</dt> <dd>

<span data-ttu-id="a1544-137">找不到服務可執行檔的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="a1544-137">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="a1544-138">**10**</span><span class="sxs-lookup"><span data-stu-id="a1544-138">**10**</span></span>
</dt> <dd>

<span data-ttu-id="a1544-139">服務已在執行中。</span><span class="sxs-lookup"><span data-stu-id="a1544-139">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="a1544-140">**11**</span><span class="sxs-lookup"><span data-stu-id="a1544-140">**11**</span></span>
</dt> <dd>

<span data-ttu-id="a1544-141">要加入新服務的資料庫已被鎖定。</span><span class="sxs-lookup"><span data-stu-id="a1544-141">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="a1544-142">**12**</span><span class="sxs-lookup"><span data-stu-id="a1544-142">**12**</span></span>
</dt> <dd>

<span data-ttu-id="a1544-143">這項服務所依賴的相依性已從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="a1544-143">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a1544-144">**13**</span><span class="sxs-lookup"><span data-stu-id="a1544-144">**13**</span></span>
</dt> <dd>

<span data-ttu-id="a1544-145">服務在相依的服務中找不到所需的服務。</span><span class="sxs-lookup"><span data-stu-id="a1544-145">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="a1544-146">**14**</span><span class="sxs-lookup"><span data-stu-id="a1544-146">**14**</span></span>
</dt> <dd>

<span data-ttu-id="a1544-147">已經從系統中停用服務。</span><span class="sxs-lookup"><span data-stu-id="a1544-147">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a1544-148">**15**</span><span class="sxs-lookup"><span data-stu-id="a1544-148">**15**</span></span>
</dt> <dd>

<span data-ttu-id="a1544-149">此服務未通過驗證，無法在系統上執行。</span><span class="sxs-lookup"><span data-stu-id="a1544-149">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="a1544-150">**16**</span><span class="sxs-lookup"><span data-stu-id="a1544-150">**16**</span></span>
</dt> <dd>

<span data-ttu-id="a1544-151">這項服務正在從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="a1544-151">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a1544-152">**17**</span><span class="sxs-lookup"><span data-stu-id="a1544-152">**17**</span></span>
</dt> <dd>

<span data-ttu-id="a1544-153">服務沒有執行執行緒。</span><span class="sxs-lookup"><span data-stu-id="a1544-153">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="a1544-154">**達**</span><span class="sxs-lookup"><span data-stu-id="a1544-154">**18**</span></span>
</dt> <dd>

<span data-ttu-id="a1544-155">服務會在啟動時有迴圈相依性。</span><span class="sxs-lookup"><span data-stu-id="a1544-155">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="a1544-156">**診斷**</span><span class="sxs-lookup"><span data-stu-id="a1544-156">**19**</span></span>
</dt> <dd>

<span data-ttu-id="a1544-157">服務正在相同名稱下執行。</span><span class="sxs-lookup"><span data-stu-id="a1544-157">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="a1544-158">**20**</span><span class="sxs-lookup"><span data-stu-id="a1544-158">**20**</span></span>
</dt> <dd>

<span data-ttu-id="a1544-159">服務名稱包含不正確字元。</span><span class="sxs-lookup"><span data-stu-id="a1544-159">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="a1544-160">**21**</span><span class="sxs-lookup"><span data-stu-id="a1544-160">**21**</span></span>
</dt> <dd>

<span data-ttu-id="a1544-161">傳遞給服務的參數無效。</span><span class="sxs-lookup"><span data-stu-id="a1544-161">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="a1544-162">**22**</span><span class="sxs-lookup"><span data-stu-id="a1544-162">**22**</span></span>
</dt> <dd>

<span data-ttu-id="a1544-163">用來執行此服務的帳戶無效，或缺少執行服務的許可權。</span><span class="sxs-lookup"><span data-stu-id="a1544-163">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="a1544-164">**23**</span><span class="sxs-lookup"><span data-stu-id="a1544-164">**23**</span></span>
</dt> <dd>

<span data-ttu-id="a1544-165">服務存在於系統可使用之服務的資料庫中。</span><span class="sxs-lookup"><span data-stu-id="a1544-165">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a1544-166">**24**</span><span class="sxs-lookup"><span data-stu-id="a1544-166">**24**</span></span>
</dt> <dd>

<span data-ttu-id="a1544-167">服務目前在系統中暫停。</span><span class="sxs-lookup"><span data-stu-id="a1544-167">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a1544-168">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1544-168">Requirements</span></span>



| <span data-ttu-id="a1544-169">需求</span><span class="sxs-lookup"><span data-stu-id="a1544-169">Requirement</span></span> | <span data-ttu-id="a1544-170">值</span><span class="sxs-lookup"><span data-stu-id="a1544-170">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1544-171">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a1544-171">Minimum supported client</span></span><br/> | <span data-ttu-id="a1544-172">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a1544-172">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a1544-173">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a1544-173">Minimum supported server</span></span><br/> | <span data-ttu-id="a1544-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a1544-174">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a1544-175">命名空間</span><span class="sxs-lookup"><span data-stu-id="a1544-175">Namespace</span></span><br/>                | <span data-ttu-id="a1544-176">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="a1544-176">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="a1544-177">MOF</span><span class="sxs-lookup"><span data-stu-id="a1544-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a1544-178"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="a1544-178"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="a1544-179">DLL</span><span class="sxs-lookup"><span data-stu-id="a1544-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1544-180"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1544-180"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1544-181">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1544-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1544-182">**Win32 \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="a1544-182">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="a1544-183">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="a1544-183">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="a1544-184">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="a1544-184">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> </dl>

 


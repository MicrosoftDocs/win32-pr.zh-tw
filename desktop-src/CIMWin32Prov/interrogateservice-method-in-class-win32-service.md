---
description: Win32_Service 類別的 InterrogateService 方法 (CIMWin32 WMI 提供者) -要求參考的服務將其狀態更新為 Service manager。
ms.assetid: a4ea8753-1859-4d97-b9ca-47598c7e7654
ms.tgt_platform: multiple
title: " (CIMWin32 WMI 提供者的 Win32_Service 類別的 InterrogateService 方法) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.InterrogateService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9702bc3fbd0a9969db20a8f1326c31b9ea7d925d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096976"
---
# <a name="interrogateservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="43361-103"> (CIMWin32 WMI 提供者的 Win32_Service 類別的 InterrogateService 方法) </span><span class="sxs-lookup"><span data-stu-id="43361-103">InterrogateService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="43361-104">**InterrogateService** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會要求參考的服務將其狀態更新為 service manager。</span><span class="sxs-lookup"><span data-stu-id="43361-104">The **InterrogateService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method requests that the referenced service update its state to the service manager.</span></span>

<span data-ttu-id="43361-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="43361-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="43361-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="43361-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="43361-107">語法</span><span class="sxs-lookup"><span data-stu-id="43361-107">Syntax</span></span>


```mof
uint32 InterrogateService();
```



## <a name="parameters"></a><span data-ttu-id="43361-108">參數</span><span class="sxs-lookup"><span data-stu-id="43361-108">Parameters</span></span>

<span data-ttu-id="43361-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="43361-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="43361-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="43361-110">Return value</span></span>

<span data-ttu-id="43361-111">傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="43361-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="43361-112">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="43361-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="43361-113">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="43361-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="43361-114">**0**</span><span class="sxs-lookup"><span data-stu-id="43361-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="43361-115">要求已被接受。</span><span class="sxs-lookup"><span data-stu-id="43361-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="43361-116">**1**</span><span class="sxs-lookup"><span data-stu-id="43361-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="43361-117">不支援此要求。</span><span class="sxs-lookup"><span data-stu-id="43361-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="43361-118">**2**</span><span class="sxs-lookup"><span data-stu-id="43361-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="43361-119">使用者沒有必要的存取權。</span><span class="sxs-lookup"><span data-stu-id="43361-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="43361-120">**3**</span><span class="sxs-lookup"><span data-stu-id="43361-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="43361-121">無法停止此服務，因為與它相依的其他服務正在執行中。</span><span class="sxs-lookup"><span data-stu-id="43361-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="43361-122">**4**</span><span class="sxs-lookup"><span data-stu-id="43361-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="43361-123">要求的控制碼無效，或是服務不接受此控制碼。</span><span class="sxs-lookup"><span data-stu-id="43361-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="43361-124">**5**</span><span class="sxs-lookup"><span data-stu-id="43361-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="43361-125">因為服務的狀態 ([**Win32 \_ BaseService**](win32-baseservice.md)，所以無法將要求的控制項程式碼傳送至服務。**State** 屬性) 等於0、1或2。</span><span class="sxs-lookup"><span data-stu-id="43361-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="43361-126">**6**</span><span class="sxs-lookup"><span data-stu-id="43361-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="43361-127">尚未啟動服務。</span><span class="sxs-lookup"><span data-stu-id="43361-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="43361-128">**7**</span><span class="sxs-lookup"><span data-stu-id="43361-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="43361-129">服務並未及時回應啟動要求。</span><span class="sxs-lookup"><span data-stu-id="43361-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="43361-130">**8**</span><span class="sxs-lookup"><span data-stu-id="43361-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="43361-131">啟動服務時發生未知的錯誤。</span><span class="sxs-lookup"><span data-stu-id="43361-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="43361-132">**9**</span><span class="sxs-lookup"><span data-stu-id="43361-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="43361-133">找不到服務可執行檔的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="43361-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="43361-134">**10**</span><span class="sxs-lookup"><span data-stu-id="43361-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="43361-135">服務已在執行中。</span><span class="sxs-lookup"><span data-stu-id="43361-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="43361-136">**11**</span><span class="sxs-lookup"><span data-stu-id="43361-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="43361-137">要加入新服務的資料庫已被鎖定。</span><span class="sxs-lookup"><span data-stu-id="43361-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="43361-138">**12**</span><span class="sxs-lookup"><span data-stu-id="43361-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="43361-139">這項服務所依賴的相依性已從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="43361-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="43361-140">**13**</span><span class="sxs-lookup"><span data-stu-id="43361-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="43361-141">服務在相依的服務中找不到所需的服務。</span><span class="sxs-lookup"><span data-stu-id="43361-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="43361-142">**14**</span><span class="sxs-lookup"><span data-stu-id="43361-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="43361-143">已經從系統中停用服務。</span><span class="sxs-lookup"><span data-stu-id="43361-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="43361-144">**15**</span><span class="sxs-lookup"><span data-stu-id="43361-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="43361-145">此服務未通過驗證，無法在系統上執行。</span><span class="sxs-lookup"><span data-stu-id="43361-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="43361-146">**16**</span><span class="sxs-lookup"><span data-stu-id="43361-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="43361-147">這項服務正在從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="43361-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="43361-148">**17**</span><span class="sxs-lookup"><span data-stu-id="43361-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="43361-149">服務沒有執行執行緒。</span><span class="sxs-lookup"><span data-stu-id="43361-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="43361-150">**達**</span><span class="sxs-lookup"><span data-stu-id="43361-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="43361-151">服務會在啟動時有迴圈相依性。</span><span class="sxs-lookup"><span data-stu-id="43361-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="43361-152">**診斷**</span><span class="sxs-lookup"><span data-stu-id="43361-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="43361-153">服務正在相同名稱下執行。</span><span class="sxs-lookup"><span data-stu-id="43361-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="43361-154">**20**</span><span class="sxs-lookup"><span data-stu-id="43361-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="43361-155">服務名稱包含不正確字元。</span><span class="sxs-lookup"><span data-stu-id="43361-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="43361-156">**21**</span><span class="sxs-lookup"><span data-stu-id="43361-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="43361-157">傳遞給服務的參數無效。</span><span class="sxs-lookup"><span data-stu-id="43361-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="43361-158">**22**</span><span class="sxs-lookup"><span data-stu-id="43361-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="43361-159">用來執行此服務的帳戶無效，或缺少執行服務的許可權。</span><span class="sxs-lookup"><span data-stu-id="43361-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="43361-160">**23**</span><span class="sxs-lookup"><span data-stu-id="43361-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="43361-161">服務存在於系統可使用之服務的資料庫中。</span><span class="sxs-lookup"><span data-stu-id="43361-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="43361-162">**24**</span><span class="sxs-lookup"><span data-stu-id="43361-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="43361-163">服務目前在系統中暫停。</span><span class="sxs-lookup"><span data-stu-id="43361-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="43361-164">規格需求</span><span class="sxs-lookup"><span data-stu-id="43361-164">Requirements</span></span>



| <span data-ttu-id="43361-165">需求</span><span class="sxs-lookup"><span data-stu-id="43361-165">Requirement</span></span> | <span data-ttu-id="43361-166">值</span><span class="sxs-lookup"><span data-stu-id="43361-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43361-167">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="43361-167">Minimum supported client</span></span><br/> | <span data-ttu-id="43361-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="43361-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="43361-169">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="43361-169">Minimum supported server</span></span><br/> | <span data-ttu-id="43361-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="43361-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="43361-171">命名空間</span><span class="sxs-lookup"><span data-stu-id="43361-171">Namespace</span></span><br/>                | <span data-ttu-id="43361-172">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="43361-172">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="43361-173">MOF</span><span class="sxs-lookup"><span data-stu-id="43361-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="43361-174"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="43361-174"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="43361-175">DLL</span><span class="sxs-lookup"><span data-stu-id="43361-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43361-176"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43361-176"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43361-177">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43361-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43361-178">**Win32 \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="43361-178">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

<span data-ttu-id="43361-179">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="43361-179">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="43361-180">**Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="43361-180">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> <dt>

[<span data-ttu-id="43361-181">WMI 工作：服務</span><span class="sxs-lookup"><span data-stu-id="43361-181">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 


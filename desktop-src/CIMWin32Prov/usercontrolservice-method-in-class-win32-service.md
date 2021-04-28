---
description: Win32_Service 類別的 UserControlService 方法 (CIMWin32 WMI 提供者) -嘗試傳送使用者定義的控制項程式碼至參考的服務。
ms.assetid: a7132c9b-6faf-4182-a5b8-3f2334c1a74b
ms.tgt_platform: multiple
title: " (CIMWin32 WMI 提供者的 Win32_Service 類別的 UserControlService 方法) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.UserControlService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 455128b35c2645c6aa6ea10f64d12dff392fecca
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099998"
---
# <a name="usercontrolservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="a1b3e-103"> (CIMWin32 WMI 提供者的 Win32_Service 類別的 UserControlService 方法) </span><span class="sxs-lookup"><span data-stu-id="a1b3e-103">UserControlService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="a1b3e-104">**UserControlService** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會嘗試將使用者定義的控制項程式碼傳送至參考的服務。</span><span class="sxs-lookup"><span data-stu-id="a1b3e-104">The **UserControlService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to send a user-defined control code to the referenced service.</span></span>

<span data-ttu-id="a1b3e-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="a1b3e-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a1b3e-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="a1b3e-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a1b3e-107">語法</span><span class="sxs-lookup"><span data-stu-id="a1b3e-107">Syntax</span></span>


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a><span data-ttu-id="a1b3e-108">參數</span><span class="sxs-lookup"><span data-stu-id="a1b3e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1b3e-109">*ControlCode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a1b3e-109">*ControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1b3e-110">指定從128到 255) 的定義值，這些 (值會提供使用者特定的控制項命令。</span><span class="sxs-lookup"><span data-stu-id="a1b3e-110">Specifies defined values (from 128 to 255) that provide control commands specific to a user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1b3e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a1b3e-111">Return value</span></span>

<span data-ttu-id="a1b3e-112">傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="a1b3e-112">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="a1b3e-113">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="a1b3e-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="a1b3e-114">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="a1b3e-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="a1b3e-115">**0**</span><span class="sxs-lookup"><span data-stu-id="a1b3e-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="a1b3e-116">要求已被接受。</span><span class="sxs-lookup"><span data-stu-id="a1b3e-116">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="a1b3e-117">**1**</span><span class="sxs-lookup"><span data-stu-id="a1b3e-117">**1**</span></span>
</dt> <dd>

<span data-ttu-id="a1b3e-118">不支援此要求。</span><span class="sxs-lookup"><span data-stu-id="a1b3e-118">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="a1b3e-119">**2**</span><span class="sxs-lookup"><span data-stu-id="a1b3e-119">**2**</span></span>
</dt> <dd>

<span data-ttu-id="a1b3e-120">使用者沒有必要的存取權。</span><span class="sxs-lookup"><span data-stu-id="a1b3e-120">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="a1b3e-121">**3**</span><span class="sxs-lookup"><span data-stu-id="a1b3e-121">**3**</span></span>
</dt> <dd>

<span data-ttu-id="a1b3e-122">無法停止此服務，因為與它相依的其他服務正在執行中。</span><span class="sxs-lookup"><span data-stu-id="a1b3e-122">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="a1b3e-123">**4**</span><span class="sxs-lookup"><span data-stu-id="a1b3e-123">**4**</span></span>
</dt> <dd>

<span data-ttu-id="a1b3e-124">要求的控制碼無效，或是服務不接受此控制碼。</span><span class="sxs-lookup"><span data-stu-id="a1b3e-124">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="a1b3e-125">**5**</span><span class="sxs-lookup"><span data-stu-id="a1b3e-125">**5**</span></span>
</dt> <dd>

<span data-ttu-id="a1b3e-126">因為服務的狀態 ([**Win32 \_ BaseService**](win32-baseservice.md)，所以無法將要求的控制項程式碼傳送至服務。**State** 屬性) 等於0、1或2。</span><span class="sxs-lookup"><span data-stu-id="a1b3e-126">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="a1b3e-127">**6**</span><span class="sxs-lookup"><span data-stu-id="a1b3e-127">**6**</span></span>
</dt> <dd>

<span data-ttu-id="a1b3e-128">尚未啟動服務。</span><span class="sxs-lookup"><span data-stu-id="a1b3e-128">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="a1b3e-129">**7**</span><span class="sxs-lookup"><span data-stu-id="a1b3e-129">**7**</span></span>
</dt> <dd>

<span data-ttu-id="a1b3e-130">服務並未及時回應啟動要求。</span><span class="sxs-lookup"><span data-stu-id="a1b3e-130">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="a1b3e-131">**8**</span><span class="sxs-lookup"><span data-stu-id="a1b3e-131">**8**</span></span>
</dt> <dd>

<span data-ttu-id="a1b3e-132">啟動服務時發生未知的錯誤。</span><span class="sxs-lookup"><span data-stu-id="a1b3e-132">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="a1b3e-133">**9**</span><span class="sxs-lookup"><span data-stu-id="a1b3e-133">**9**</span></span>
</dt> <dd>

<span data-ttu-id="a1b3e-134">找不到服務可執行檔的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="a1b3e-134">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="a1b3e-135">**10**</span><span class="sxs-lookup"><span data-stu-id="a1b3e-135">**10**</span></span>
</dt> <dd>

<span data-ttu-id="a1b3e-136">服務已在執行中。</span><span class="sxs-lookup"><span data-stu-id="a1b3e-136">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="a1b3e-137">**11**</span><span class="sxs-lookup"><span data-stu-id="a1b3e-137">**11**</span></span>
</dt> <dd>

<span data-ttu-id="a1b3e-138">要加入新服務的資料庫已被鎖定。</span><span class="sxs-lookup"><span data-stu-id="a1b3e-138">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="a1b3e-139">**12**</span><span class="sxs-lookup"><span data-stu-id="a1b3e-139">**12**</span></span>
</dt> <dd>

<span data-ttu-id="a1b3e-140">這項服務所依賴的相依性已從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="a1b3e-140">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a1b3e-141">**13**</span><span class="sxs-lookup"><span data-stu-id="a1b3e-141">**13**</span></span>
</dt> <dd>

<span data-ttu-id="a1b3e-142">服務在相依的服務中找不到所需的服務。</span><span class="sxs-lookup"><span data-stu-id="a1b3e-142">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="a1b3e-143">**14**</span><span class="sxs-lookup"><span data-stu-id="a1b3e-143">**14**</span></span>
</dt> <dd>

<span data-ttu-id="a1b3e-144">已經從系統中停用服務。</span><span class="sxs-lookup"><span data-stu-id="a1b3e-144">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a1b3e-145">**15**</span><span class="sxs-lookup"><span data-stu-id="a1b3e-145">**15**</span></span>
</dt> <dd>

<span data-ttu-id="a1b3e-146">此服務未通過驗證，無法在系統上執行。</span><span class="sxs-lookup"><span data-stu-id="a1b3e-146">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="a1b3e-147">**16**</span><span class="sxs-lookup"><span data-stu-id="a1b3e-147">**16**</span></span>
</dt> <dd>

<span data-ttu-id="a1b3e-148">這項服務正在從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="a1b3e-148">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a1b3e-149">**17**</span><span class="sxs-lookup"><span data-stu-id="a1b3e-149">**17**</span></span>
</dt> <dd>

<span data-ttu-id="a1b3e-150">服務沒有執行執行緒。</span><span class="sxs-lookup"><span data-stu-id="a1b3e-150">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="a1b3e-151">**達**</span><span class="sxs-lookup"><span data-stu-id="a1b3e-151">**18**</span></span>
</dt> <dd>

<span data-ttu-id="a1b3e-152">服務會在啟動時有迴圈相依性。</span><span class="sxs-lookup"><span data-stu-id="a1b3e-152">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="a1b3e-153">**診斷**</span><span class="sxs-lookup"><span data-stu-id="a1b3e-153">**19**</span></span>
</dt> <dd>

<span data-ttu-id="a1b3e-154">服務正在相同名稱下執行。</span><span class="sxs-lookup"><span data-stu-id="a1b3e-154">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="a1b3e-155">**20**</span><span class="sxs-lookup"><span data-stu-id="a1b3e-155">**20**</span></span>
</dt> <dd>

<span data-ttu-id="a1b3e-156">服務名稱包含不正確字元。</span><span class="sxs-lookup"><span data-stu-id="a1b3e-156">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="a1b3e-157">**21**</span><span class="sxs-lookup"><span data-stu-id="a1b3e-157">**21**</span></span>
</dt> <dd>

<span data-ttu-id="a1b3e-158">傳遞給服務的參數無效。</span><span class="sxs-lookup"><span data-stu-id="a1b3e-158">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="a1b3e-159">**22**</span><span class="sxs-lookup"><span data-stu-id="a1b3e-159">**22**</span></span>
</dt> <dd>

<span data-ttu-id="a1b3e-160">用來執行此服務的帳戶無效，或缺少執行服務的許可權。</span><span class="sxs-lookup"><span data-stu-id="a1b3e-160">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="a1b3e-161">**23**</span><span class="sxs-lookup"><span data-stu-id="a1b3e-161">**23**</span></span>
</dt> <dd>

<span data-ttu-id="a1b3e-162">服務存在於系統可使用之服務的資料庫中。</span><span class="sxs-lookup"><span data-stu-id="a1b3e-162">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a1b3e-163">**24**</span><span class="sxs-lookup"><span data-stu-id="a1b3e-163">**24**</span></span>
</dt> <dd>

<span data-ttu-id="a1b3e-164">服務目前在系統中暫停。</span><span class="sxs-lookup"><span data-stu-id="a1b3e-164">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a1b3e-165">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1b3e-165">Requirements</span></span>



| <span data-ttu-id="a1b3e-166">需求</span><span class="sxs-lookup"><span data-stu-id="a1b3e-166">Requirement</span></span> | <span data-ttu-id="a1b3e-167">值</span><span class="sxs-lookup"><span data-stu-id="a1b3e-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1b3e-168">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a1b3e-168">Minimum supported client</span></span><br/> | <span data-ttu-id="a1b3e-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a1b3e-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a1b3e-170">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a1b3e-170">Minimum supported server</span></span><br/> | <span data-ttu-id="a1b3e-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a1b3e-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a1b3e-172">命名空間</span><span class="sxs-lookup"><span data-stu-id="a1b3e-172">Namespace</span></span><br/>                | <span data-ttu-id="a1b3e-173">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a1b3e-173">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a1b3e-174">MOF</span><span class="sxs-lookup"><span data-stu-id="a1b3e-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a1b3e-175"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="a1b3e-175"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a1b3e-176">DLL</span><span class="sxs-lookup"><span data-stu-id="a1b3e-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1b3e-177"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1b3e-177"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1b3e-178">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1b3e-178">See also</span></span>

<dl> <dt>

<span data-ttu-id="a1b3e-179">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a1b3e-179">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a1b3e-180">**Win32 \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="a1b3e-180">**Win32\_Service**</span></span>](win32-service.md)
</dt> </dl>

 


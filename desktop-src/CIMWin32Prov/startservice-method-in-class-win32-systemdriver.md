---
description: 嘗試將系統驅動程式所管理的服務置於啟動狀態。
ms.assetid: 3f9d29aa-b549-4a55-be9c-01fad4932fe6
ms.tgt_platform: multiple
title: Win32_SystemDriver 類別的 StartService 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2c189d9b5f24a3ccc803a588abb94337ee65a1da
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187733"
---
# <a name="startservice-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="41975-103">Win32 >systemdriver 類別的 StartService 方法 \_</span><span class="sxs-lookup"><span data-stu-id="41975-103">StartService method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="41975-104">**StartService** 方法會嘗試將系統驅動程式所管理的服務置於啟動狀態。</span><span class="sxs-lookup"><span data-stu-id="41975-104">The **StartService** method attempts to place the service managed by the system driver into its startup state.</span></span>

<span data-ttu-id="41975-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="41975-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="41975-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="41975-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="41975-107">語法</span><span class="sxs-lookup"><span data-stu-id="41975-107">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="41975-108">參數</span><span class="sxs-lookup"><span data-stu-id="41975-108">Parameters</span></span>

<span data-ttu-id="41975-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="41975-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="41975-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="41975-110">Return value</span></span>

<span data-ttu-id="41975-111">傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="41975-111">Returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="41975-112">**0**</span><span class="sxs-lookup"><span data-stu-id="41975-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="41975-113">要求已被接受。</span><span class="sxs-lookup"><span data-stu-id="41975-113">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="41975-114">**1**</span><span class="sxs-lookup"><span data-stu-id="41975-114">**1**</span></span>
</dt> <dd>

<span data-ttu-id="41975-115">不支援此要求。</span><span class="sxs-lookup"><span data-stu-id="41975-115">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="41975-116">**2**</span><span class="sxs-lookup"><span data-stu-id="41975-116">**2**</span></span>
</dt> <dd>

<span data-ttu-id="41975-117">使用者沒有必要的存取權。</span><span class="sxs-lookup"><span data-stu-id="41975-117">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="41975-118">**3**</span><span class="sxs-lookup"><span data-stu-id="41975-118">**3**</span></span>
</dt> <dd>

<span data-ttu-id="41975-119">無法停止此服務，因為與它相依的其他服務正在執行中。</span><span class="sxs-lookup"><span data-stu-id="41975-119">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="41975-120">**4**</span><span class="sxs-lookup"><span data-stu-id="41975-120">**4**</span></span>
</dt> <dd>

<span data-ttu-id="41975-121">要求的控制碼無效，或是服務不接受此控制碼。</span><span class="sxs-lookup"><span data-stu-id="41975-121">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="41975-122">**5**</span><span class="sxs-lookup"><span data-stu-id="41975-122">**5**</span></span>
</dt> <dd>

<span data-ttu-id="41975-123">因為服務的狀態 ([**Win32 \_ BaseService**](win32-baseservice.md)，所以無法將要求的控制項程式碼傳送至服務。**State** 屬性) 等於0、1或2。</span><span class="sxs-lookup"><span data-stu-id="41975-123">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="41975-124">**6**</span><span class="sxs-lookup"><span data-stu-id="41975-124">**6**</span></span>
</dt> <dd>

<span data-ttu-id="41975-125">尚未啟動服務。</span><span class="sxs-lookup"><span data-stu-id="41975-125">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="41975-126">**7**</span><span class="sxs-lookup"><span data-stu-id="41975-126">**7**</span></span>
</dt> <dd>

<span data-ttu-id="41975-127">服務並未及時回應啟動要求。</span><span class="sxs-lookup"><span data-stu-id="41975-127">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="41975-128">**8**</span><span class="sxs-lookup"><span data-stu-id="41975-128">**8**</span></span>
</dt> <dd>

<span data-ttu-id="41975-129">啟動服務時發生未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="41975-129">An unknown failure occurred when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="41975-130">**9**</span><span class="sxs-lookup"><span data-stu-id="41975-130">**9**</span></span>
</dt> <dd>

<span data-ttu-id="41975-131">找不到服務可執行檔的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="41975-131">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="41975-132">**10**</span><span class="sxs-lookup"><span data-stu-id="41975-132">**10**</span></span>
</dt> <dd>

<span data-ttu-id="41975-133">服務已在執行中。</span><span class="sxs-lookup"><span data-stu-id="41975-133">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="41975-134">**11**</span><span class="sxs-lookup"><span data-stu-id="41975-134">**11**</span></span>
</dt> <dd>

<span data-ttu-id="41975-135">要加入新服務的資料庫已被鎖定。</span><span class="sxs-lookup"><span data-stu-id="41975-135">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="41975-136">**12**</span><span class="sxs-lookup"><span data-stu-id="41975-136">**12**</span></span>
</dt> <dd>

<span data-ttu-id="41975-137">這項服務所依賴的相依性已從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="41975-137">A dependency for which this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="41975-138">**13**</span><span class="sxs-lookup"><span data-stu-id="41975-138">**13**</span></span>
</dt> <dd>

<span data-ttu-id="41975-139">服務在相依的服務中找不到所需的服務。</span><span class="sxs-lookup"><span data-stu-id="41975-139">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="41975-140">**14**</span><span class="sxs-lookup"><span data-stu-id="41975-140">**14**</span></span>
</dt> <dd>

<span data-ttu-id="41975-141">已經從系統中停用服務。</span><span class="sxs-lookup"><span data-stu-id="41975-141">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="41975-142">**15**</span><span class="sxs-lookup"><span data-stu-id="41975-142">**15**</span></span>
</dt> <dd>

<span data-ttu-id="41975-143">此服務未通過驗證，無法在系統上執行。</span><span class="sxs-lookup"><span data-stu-id="41975-143">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="41975-144">**16**</span><span class="sxs-lookup"><span data-stu-id="41975-144">**16**</span></span>
</dt> <dd>

<span data-ttu-id="41975-145">這項服務正在從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="41975-145">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="41975-146">**17**</span><span class="sxs-lookup"><span data-stu-id="41975-146">**17**</span></span>
</dt> <dd>

<span data-ttu-id="41975-147">服務沒有執行緒。</span><span class="sxs-lookup"><span data-stu-id="41975-147">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="41975-148">**達**</span><span class="sxs-lookup"><span data-stu-id="41975-148">**18**</span></span>
</dt> <dd>

<span data-ttu-id="41975-149">啟動服務時有循環的相依性。</span><span class="sxs-lookup"><span data-stu-id="41975-149">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="41975-150">**診斷**</span><span class="sxs-lookup"><span data-stu-id="41975-150">**19**</span></span>
</dt> <dd>

<span data-ttu-id="41975-151">有一個服務在相同名稱下執行。</span><span class="sxs-lookup"><span data-stu-id="41975-151">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="41975-152">**20**</span><span class="sxs-lookup"><span data-stu-id="41975-152">**20**</span></span>
</dt> <dd>

<span data-ttu-id="41975-153">服務名稱中有不正確字元。</span><span class="sxs-lookup"><span data-stu-id="41975-153">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="41975-154">**21**</span><span class="sxs-lookup"><span data-stu-id="41975-154">**21**</span></span>
</dt> <dd>

<span data-ttu-id="41975-155">傳遞給服務的參數無效。</span><span class="sxs-lookup"><span data-stu-id="41975-155">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="41975-156">**22**</span><span class="sxs-lookup"><span data-stu-id="41975-156">**22**</span></span>
</dt> <dd>

<span data-ttu-id="41975-157">用來執行此服務的帳戶無效，或缺少執行服務的許可權。</span><span class="sxs-lookup"><span data-stu-id="41975-157">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="41975-158">**23**</span><span class="sxs-lookup"><span data-stu-id="41975-158">**23**</span></span>
</dt> <dd>

<span data-ttu-id="41975-159">服務存在於系統可使用之服務的資料庫中。</span><span class="sxs-lookup"><span data-stu-id="41975-159">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="41975-160">**24**</span><span class="sxs-lookup"><span data-stu-id="41975-160">**24**</span></span>
</dt> <dd>

<span data-ttu-id="41975-161">服務目前在系統中暫停。</span><span class="sxs-lookup"><span data-stu-id="41975-161">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="41975-162">範例</span><span class="sxs-lookup"><span data-stu-id="41975-162">Examples</span></span>

<span data-ttu-id="41975-163">下列 PowerShell 程式碼會啟動「Microsoft USB 印表機類別」服務。</span><span class="sxs-lookup"><span data-stu-id="41975-163">The following PowerShell code starts the "Microsoft USB Printer class" service.</span></span>


```PowerShell
$usbPrintDriver = Get-WmiObject -query "SELECT * FROM Win32_SystemDriver WHERE Name = 'usbprint'"
$Return = $usbPrintDriver.StartService()
"Start Service Called. Return value is " + $return.ReturnValue + "."
"To figure out what this means, go look at the docs above this code snippet."
```



## <a name="requirements"></a><span data-ttu-id="41975-164">規格需求</span><span class="sxs-lookup"><span data-stu-id="41975-164">Requirements</span></span>



| <span data-ttu-id="41975-165">需求</span><span class="sxs-lookup"><span data-stu-id="41975-165">Requirement</span></span> | <span data-ttu-id="41975-166">值</span><span class="sxs-lookup"><span data-stu-id="41975-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41975-167">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="41975-167">Minimum supported client</span></span><br/> | <span data-ttu-id="41975-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="41975-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="41975-169">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="41975-169">Minimum supported server</span></span><br/> | <span data-ttu-id="41975-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="41975-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="41975-171">命名空間</span><span class="sxs-lookup"><span data-stu-id="41975-171">Namespace</span></span><br/>                | <span data-ttu-id="41975-172">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="41975-172">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="41975-173">MOF</span><span class="sxs-lookup"><span data-stu-id="41975-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="41975-174"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="41975-174"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="41975-175">DLL</span><span class="sxs-lookup"><span data-stu-id="41975-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41975-176"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41975-176"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41975-177">另請參閱</span><span class="sxs-lookup"><span data-stu-id="41975-177">See also</span></span>

<dl> <dt>

<span data-ttu-id="41975-178">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="41975-178">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="41975-179">**Win32 \_ >systemdriver**</span><span class="sxs-lookup"><span data-stu-id="41975-179">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 


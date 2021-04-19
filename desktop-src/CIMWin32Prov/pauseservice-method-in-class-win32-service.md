---
description: 嘗試將此服務置於暫停狀態。
ms.assetid: 5382457e-7f9c-48a5-9262-b815a1a4a605
ms.tgt_platform: multiple
title: " (CIMWin32 WMI 提供者的 Win32_Service 類別的 PauseService 方法) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.PauseService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1b1dfa0b956442f74c17dd6a8c054c229a92466a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970906"
---
# <a name="pauseservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="70c58-103"> (CIMWin32 WMI 提供者的 Win32_Service 類別的 PauseService 方法) </span><span class="sxs-lookup"><span data-stu-id="70c58-103">PauseService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="70c58-104">**PauseService** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會嘗試將服務置於暫停狀態。</span><span class="sxs-lookup"><span data-stu-id="70c58-104">The **PauseService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the service in the paused state.</span></span>

<span data-ttu-id="70c58-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="70c58-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="70c58-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="70c58-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="70c58-107">語法</span><span class="sxs-lookup"><span data-stu-id="70c58-107">Syntax</span></span>


```mof
uint32 PauseService();
```



## <a name="parameters"></a><span data-ttu-id="70c58-108">參數</span><span class="sxs-lookup"><span data-stu-id="70c58-108">Parameters</span></span>

<span data-ttu-id="70c58-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="70c58-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="70c58-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="70c58-110">Return value</span></span>

<span data-ttu-id="70c58-111">傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="70c58-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="70c58-112">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="70c58-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="70c58-113">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="70c58-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="70c58-114">**0**</span><span class="sxs-lookup"><span data-stu-id="70c58-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="70c58-115">要求已被接受。</span><span class="sxs-lookup"><span data-stu-id="70c58-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="70c58-116">**1**</span><span class="sxs-lookup"><span data-stu-id="70c58-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="70c58-117">不支援此要求。</span><span class="sxs-lookup"><span data-stu-id="70c58-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="70c58-118">**2**</span><span class="sxs-lookup"><span data-stu-id="70c58-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="70c58-119">使用者沒有必要的存取權。</span><span class="sxs-lookup"><span data-stu-id="70c58-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="70c58-120">**3**</span><span class="sxs-lookup"><span data-stu-id="70c58-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="70c58-121">無法停止此服務，因為與它相依的其他服務正在執行中。</span><span class="sxs-lookup"><span data-stu-id="70c58-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="70c58-122">**4**</span><span class="sxs-lookup"><span data-stu-id="70c58-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="70c58-123">要求的控制碼無效，或是服務不接受此控制碼。</span><span class="sxs-lookup"><span data-stu-id="70c58-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="70c58-124">**5**</span><span class="sxs-lookup"><span data-stu-id="70c58-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="70c58-125">因為服務的狀態 ([**Win32 \_ BaseService**](win32-baseservice.md)，所以無法將要求的控制項程式碼傳送至服務。**State** 屬性) 等於0、1或2。</span><span class="sxs-lookup"><span data-stu-id="70c58-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="70c58-126">**6**</span><span class="sxs-lookup"><span data-stu-id="70c58-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="70c58-127">尚未啟動服務。</span><span class="sxs-lookup"><span data-stu-id="70c58-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="70c58-128">**7**</span><span class="sxs-lookup"><span data-stu-id="70c58-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="70c58-129">服務並未及時回應啟動要求。</span><span class="sxs-lookup"><span data-stu-id="70c58-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="70c58-130">**8**</span><span class="sxs-lookup"><span data-stu-id="70c58-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="70c58-131">啟動服務時發生未知的錯誤。</span><span class="sxs-lookup"><span data-stu-id="70c58-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="70c58-132">**9**</span><span class="sxs-lookup"><span data-stu-id="70c58-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="70c58-133">找不到服務可執行檔的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="70c58-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="70c58-134">**10**</span><span class="sxs-lookup"><span data-stu-id="70c58-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="70c58-135">服務已在執行中。</span><span class="sxs-lookup"><span data-stu-id="70c58-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="70c58-136">**11**</span><span class="sxs-lookup"><span data-stu-id="70c58-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="70c58-137">要加入新服務的資料庫已被鎖定。</span><span class="sxs-lookup"><span data-stu-id="70c58-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="70c58-138">**12**</span><span class="sxs-lookup"><span data-stu-id="70c58-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="70c58-139">這項服務所依賴的相依性已從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="70c58-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="70c58-140">**13**</span><span class="sxs-lookup"><span data-stu-id="70c58-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="70c58-141">服務在相依的服務中找不到所需的服務。</span><span class="sxs-lookup"><span data-stu-id="70c58-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="70c58-142">**14**</span><span class="sxs-lookup"><span data-stu-id="70c58-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="70c58-143">已經從系統中停用服務。</span><span class="sxs-lookup"><span data-stu-id="70c58-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="70c58-144">**15**</span><span class="sxs-lookup"><span data-stu-id="70c58-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="70c58-145">此服務未通過驗證，無法在系統上執行。</span><span class="sxs-lookup"><span data-stu-id="70c58-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="70c58-146">**16**</span><span class="sxs-lookup"><span data-stu-id="70c58-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="70c58-147">這項服務正在從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="70c58-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="70c58-148">**17**</span><span class="sxs-lookup"><span data-stu-id="70c58-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="70c58-149">服務沒有執行執行緒。</span><span class="sxs-lookup"><span data-stu-id="70c58-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="70c58-150">**達**</span><span class="sxs-lookup"><span data-stu-id="70c58-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="70c58-151">服務會在啟動時有迴圈相依性。</span><span class="sxs-lookup"><span data-stu-id="70c58-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="70c58-152">**診斷**</span><span class="sxs-lookup"><span data-stu-id="70c58-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="70c58-153">服務正在相同名稱下執行。</span><span class="sxs-lookup"><span data-stu-id="70c58-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="70c58-154">**20**</span><span class="sxs-lookup"><span data-stu-id="70c58-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="70c58-155">服務名稱包含不正確字元。</span><span class="sxs-lookup"><span data-stu-id="70c58-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="70c58-156">**21**</span><span class="sxs-lookup"><span data-stu-id="70c58-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="70c58-157">傳遞給服務的參數無效。</span><span class="sxs-lookup"><span data-stu-id="70c58-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="70c58-158">**22**</span><span class="sxs-lookup"><span data-stu-id="70c58-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="70c58-159">用來執行此服務的帳戶無效，或缺少執行服務的許可權。</span><span class="sxs-lookup"><span data-stu-id="70c58-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="70c58-160">**23**</span><span class="sxs-lookup"><span data-stu-id="70c58-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="70c58-161">服務存在於系統可使用之服務的資料庫中。</span><span class="sxs-lookup"><span data-stu-id="70c58-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="70c58-162">**24**</span><span class="sxs-lookup"><span data-stu-id="70c58-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="70c58-163">服務目前在系統中暫停。</span><span class="sxs-lookup"><span data-stu-id="70c58-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="70c58-164">備註</span><span class="sxs-lookup"><span data-stu-id="70c58-164">Remarks</span></span>

<span data-ttu-id="70c58-165">確定可以停止或暫停的服務之後，您可以使用 [**StopService**](stopservice-method-in-class-win32-service.md) 和 [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md) 方法來停止和暫停服務。</span><span class="sxs-lookup"><span data-stu-id="70c58-165">After you have determined which services can be stopped or paused, you can use the [**StopService**](stopservice-method-in-class-win32-service.md) and [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md) methods to stop and pause services.</span></span> <span data-ttu-id="70c58-166">停止服務而非暫停服務（反之亦然）的決策取決於數個因素，包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="70c58-166">The decision to stop a service rather than pause it, or vice versa, depends on several factors, including the following:</span></span>

-   <span data-ttu-id="70c58-167">服務是否能夠暫停？</span><span class="sxs-lookup"><span data-stu-id="70c58-167">Is the service capable of being paused?</span></span> <span data-ttu-id="70c58-168">如果沒有，則您的唯一選項是停止服務。</span><span class="sxs-lookup"><span data-stu-id="70c58-168">If not, your only option is the stop the service.</span></span>
-   <span data-ttu-id="70c58-169">您是否需要繼續處理已連線到服務的任何人的用戶端要求？</span><span class="sxs-lookup"><span data-stu-id="70c58-169">Do you need to continue handling client requests for anyone already connected to the service?</span></span> <span data-ttu-id="70c58-170">若是如此，暫停服務通常會允許它處理現有的用戶端，同時拒絕存取新的用戶端。</span><span class="sxs-lookup"><span data-stu-id="70c58-170">If so, pausing a service typically allows it to handle existing clients while denying access to new clients.</span></span> <span data-ttu-id="70c58-171">相反地，當您停止服務時，所有用戶端都會立即中斷連線。</span><span class="sxs-lookup"><span data-stu-id="70c58-171">By contrast, when you stop a service, all clients are immediately disconnected.</span></span>
-   <span data-ttu-id="70c58-172">您是否需要重新設定服務，並讓變更立即生效？</span><span class="sxs-lookup"><span data-stu-id="70c58-172">Do you need to reconfigure a service and have the changes take effect immediately?</span></span> <span data-ttu-id="70c58-173">雖然服務屬性可以在服務暫停時變更，但大部分的服務都不會在服務實際停止並重新啟動之前生效。</span><span class="sxs-lookup"><span data-stu-id="70c58-173">Although service properties can be changed while a service is paused, most of them do not take effect until the service is actually stopped and restarted.</span></span>

<span data-ttu-id="70c58-174">停止服務所需的腳本程式碼與暫停服務所需的程式碼幾乎完全相同。</span><span class="sxs-lookup"><span data-stu-id="70c58-174">The scripting code required to stop a service is almost identical to the code required to pause the service.</span></span>

## <a name="examples"></a><span data-ttu-id="70c58-175">範例</span><span class="sxs-lookup"><span data-stu-id="70c58-175">Examples</span></span>

<span data-ttu-id="70c58-176">在 [特定帳戶中執行的暫停服務](https://Gallery.TechNet.Microsoft.Com/12a256dd-39da-4690-b3f0-f0adccaf25f1) VBScript 範例會暫停以假設服務帳戶 "Netsvc" 為下執行的所有服務。</span><span class="sxs-lookup"><span data-stu-id="70c58-176">The [Pause Services Running Under a Specific Account](https://Gallery.TechNet.Microsoft.Com/12a256dd-39da-4690-b3f0-f0adccaf25f1) VBScript sample Pauses all services running under the hypothetical service account "Netsvc".</span></span>

<span data-ttu-id="70c58-177">下列 VBScript 程式碼範例示範如何從 [**Win32 \_ 服務**](win32-service.md)的實例暫停特定的服務。</span><span class="sxs-lookup"><span data-stu-id="70c58-177">The following VBScript code sample demonstrates how to pause a specific service from instances of [**Win32\_Service**](win32-service.md).</span></span>

> [!Note]  
> <span data-ttu-id="70c58-178">服務必須支援暫停且已在執行中。</span><span class="sxs-lookup"><span data-stu-id="70c58-178">The service must support pausing and be running already.</span></span>

 


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='Schedule'")

for each Service in ServiceSet
 SupportsPause = Service.AcceptPause
 if SupportsPause = true then
  RetVal = Service.PauseService()
  if RetVal = 0 then 
   WScript.Echo "Service paused"   
  else
   if RetVal = 1 then 
    WScript.Echo "Pause not supported" 
   else WScript.Echo "An error occurred:" & RetVal
   End If
  End If
 else
  WScript.Echo "Service does not support pause"
 end if
next
```



<span data-ttu-id="70c58-179">下列 Perl 程式碼範例示範如何從 [**Win32 \_ 服務**](win32-service.md)的實例暫停特定的服務。</span><span class="sxs-lookup"><span data-stu-id="70c58-179">The following Perl code sample demonstrates how to pause a specific service from instances of [**Win32\_Service**](win32-service.md).</span></span>

> [!Note]  
> <span data-ttu-id="70c58-180">服務必須支援暫停且已在執行中。</span><span class="sxs-lookup"><span data-stu-id="70c58-180">The service must support pausing and be running already.</span></span>

 


```
use strict;
use Win32::OLE;

my ($ServiceSet, $SupportsPause, $RetVal);  
eval {$ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\Root\\CIMv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='Schedule'"); };
unless($@)
{
 foreach my $ServiceInst (in $ServiceSet)
 {
  if ($ServiceInst->{AcceptPause})
  {
   $RetVal = $ServiceInst->PauseService();
   if ($RetVal == 0)
   {
    print "\nService paused\n";
   }
   else
   {
    if ($RetVal == 1)
    {
     print "\nPause not supported\n" ;
    }
    else 
    {
     print "\nAn error occurred:", $RetVal, "\n";
    }
   } 
  }
  else
  {
   print "\nService does not support pause\n";
  }
 }
}
else
{
 print STDERR "\n", Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="70c58-181">規格需求</span><span class="sxs-lookup"><span data-stu-id="70c58-181">Requirements</span></span>



| <span data-ttu-id="70c58-182">需求</span><span class="sxs-lookup"><span data-stu-id="70c58-182">Requirement</span></span> | <span data-ttu-id="70c58-183">值</span><span class="sxs-lookup"><span data-stu-id="70c58-183">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="70c58-184">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="70c58-184">Minimum supported client</span></span><br/> | <span data-ttu-id="70c58-185">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="70c58-185">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="70c58-186">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="70c58-186">Minimum supported server</span></span><br/> | <span data-ttu-id="70c58-187">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="70c58-187">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="70c58-188">命名空間</span><span class="sxs-lookup"><span data-stu-id="70c58-188">Namespace</span></span><br/>                | <span data-ttu-id="70c58-189">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="70c58-189">Root\\CIMv2</span></span><br/>                                                                  |
| <span data-ttu-id="70c58-190">MOF</span><span class="sxs-lookup"><span data-stu-id="70c58-190">MOF</span></span><br/>                      | <dl> <span data-ttu-id="70c58-191"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="70c58-191"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="70c58-192">DLL</span><span class="sxs-lookup"><span data-stu-id="70c58-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70c58-193"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70c58-193"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70c58-194">另請參閱</span><span class="sxs-lookup"><span data-stu-id="70c58-194">See also</span></span>

<dl> <dt>

<span data-ttu-id="70c58-195">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="70c58-195">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="70c58-196">**Win32 \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="70c58-196">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="70c58-197">WMI 工作：服務</span><span class="sxs-lookup"><span data-stu-id="70c58-197">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[<span data-ttu-id="70c58-198">**StopService**</span><span class="sxs-lookup"><span data-stu-id="70c58-198">**StopService**</span></span>](stopservice-method-in-class-win32-service.md)
</dt> </dl>

 


---
description: 嘗試將參考的服務放在恢復狀態。
ms.assetid: 3b4228bf-9ff5-44ab-bfe2-f7dd8fb62007
ms.tgt_platform: multiple
title: " (CIMWin32 WMI 提供者的 Win32_Service 類別的 ResumeService 方法) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.ResumeService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ed4141b02d6e08bd4b106d2c1f72ce3fe0620fc7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847567"
---
# <a name="resumeservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="243f0-103"> (CIMWin32 WMI 提供者的 Win32_Service 類別的 ResumeService 方法) </span><span class="sxs-lookup"><span data-stu-id="243f0-103">ResumeService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="243f0-104">**ResumeService** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會嘗試將參考的服務放在恢復狀態。</span><span class="sxs-lookup"><span data-stu-id="243f0-104">The **ResumeService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the referenced service in the resumed state.</span></span>

<span data-ttu-id="243f0-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="243f0-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="243f0-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="243f0-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="243f0-107">語法</span><span class="sxs-lookup"><span data-stu-id="243f0-107">Syntax</span></span>


```mof
uint32 ResumeService();
```



## <a name="parameters"></a><span data-ttu-id="243f0-108">參數</span><span class="sxs-lookup"><span data-stu-id="243f0-108">Parameters</span></span>

<span data-ttu-id="243f0-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="243f0-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="243f0-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="243f0-110">Return value</span></span>

<span data-ttu-id="243f0-111">傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="243f0-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="243f0-112">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="243f0-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="243f0-113">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="243f0-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="243f0-114">**0**</span><span class="sxs-lookup"><span data-stu-id="243f0-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="243f0-115">要求已被接受。</span><span class="sxs-lookup"><span data-stu-id="243f0-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="243f0-116">**1**</span><span class="sxs-lookup"><span data-stu-id="243f0-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="243f0-117">不支援此要求。</span><span class="sxs-lookup"><span data-stu-id="243f0-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="243f0-118">**2**</span><span class="sxs-lookup"><span data-stu-id="243f0-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="243f0-119">使用者沒有必要的存取權。</span><span class="sxs-lookup"><span data-stu-id="243f0-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="243f0-120">**3**</span><span class="sxs-lookup"><span data-stu-id="243f0-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="243f0-121">無法停止此服務，因為與它相依的其他服務正在執行中。</span><span class="sxs-lookup"><span data-stu-id="243f0-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="243f0-122">**4**</span><span class="sxs-lookup"><span data-stu-id="243f0-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="243f0-123">要求的控制碼無效，或是服務不接受此控制碼。</span><span class="sxs-lookup"><span data-stu-id="243f0-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="243f0-124">**5**</span><span class="sxs-lookup"><span data-stu-id="243f0-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="243f0-125">因為服務的狀態 ([**Win32 \_ BaseService**](win32-baseservice.md)，所以無法將要求的控制項程式碼傳送至服務。**State** 屬性) 等於0、1或2。</span><span class="sxs-lookup"><span data-stu-id="243f0-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="243f0-126">**6**</span><span class="sxs-lookup"><span data-stu-id="243f0-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="243f0-127">尚未啟動服務。</span><span class="sxs-lookup"><span data-stu-id="243f0-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="243f0-128">**7**</span><span class="sxs-lookup"><span data-stu-id="243f0-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="243f0-129">服務並未及時回應啟動要求。</span><span class="sxs-lookup"><span data-stu-id="243f0-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="243f0-130">**8**</span><span class="sxs-lookup"><span data-stu-id="243f0-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="243f0-131">啟動服務時發生未知的錯誤。</span><span class="sxs-lookup"><span data-stu-id="243f0-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="243f0-132">**9**</span><span class="sxs-lookup"><span data-stu-id="243f0-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="243f0-133">找不到服務可執行檔的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="243f0-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="243f0-134">**10**</span><span class="sxs-lookup"><span data-stu-id="243f0-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="243f0-135">服務已在執行中。</span><span class="sxs-lookup"><span data-stu-id="243f0-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="243f0-136">**11**</span><span class="sxs-lookup"><span data-stu-id="243f0-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="243f0-137">要加入新服務的資料庫已被鎖定。</span><span class="sxs-lookup"><span data-stu-id="243f0-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="243f0-138">**12**</span><span class="sxs-lookup"><span data-stu-id="243f0-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="243f0-139">這項服務所依賴的相依性已從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="243f0-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="243f0-140">**13**</span><span class="sxs-lookup"><span data-stu-id="243f0-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="243f0-141">服務在相依的服務中找不到所需的服務。</span><span class="sxs-lookup"><span data-stu-id="243f0-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="243f0-142">**14**</span><span class="sxs-lookup"><span data-stu-id="243f0-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="243f0-143">已經從系統中停用服務。</span><span class="sxs-lookup"><span data-stu-id="243f0-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="243f0-144">**15**</span><span class="sxs-lookup"><span data-stu-id="243f0-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="243f0-145">此服務未通過驗證，無法在系統上執行。</span><span class="sxs-lookup"><span data-stu-id="243f0-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="243f0-146">**16**</span><span class="sxs-lookup"><span data-stu-id="243f0-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="243f0-147">這項服務正在從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="243f0-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="243f0-148">**17**</span><span class="sxs-lookup"><span data-stu-id="243f0-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="243f0-149">服務沒有執行執行緒。</span><span class="sxs-lookup"><span data-stu-id="243f0-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="243f0-150">**達**</span><span class="sxs-lookup"><span data-stu-id="243f0-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="243f0-151">服務會在啟動時有迴圈相依性。</span><span class="sxs-lookup"><span data-stu-id="243f0-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="243f0-152">**診斷**</span><span class="sxs-lookup"><span data-stu-id="243f0-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="243f0-153">服務正在相同名稱下執行。</span><span class="sxs-lookup"><span data-stu-id="243f0-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="243f0-154">**20**</span><span class="sxs-lookup"><span data-stu-id="243f0-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="243f0-155">服務名稱包含不正確字元。</span><span class="sxs-lookup"><span data-stu-id="243f0-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="243f0-156">**21**</span><span class="sxs-lookup"><span data-stu-id="243f0-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="243f0-157">傳遞給服務的參數無效。</span><span class="sxs-lookup"><span data-stu-id="243f0-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="243f0-158">**22**</span><span class="sxs-lookup"><span data-stu-id="243f0-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="243f0-159">用來執行此服務的帳戶無效，或缺少執行服務的許可權。</span><span class="sxs-lookup"><span data-stu-id="243f0-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="243f0-160">**23**</span><span class="sxs-lookup"><span data-stu-id="243f0-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="243f0-161">服務存在於系統可使用之服務的資料庫中。</span><span class="sxs-lookup"><span data-stu-id="243f0-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="243f0-162">**24**</span><span class="sxs-lookup"><span data-stu-id="243f0-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="243f0-163">服務目前在系統中暫停。</span><span class="sxs-lookup"><span data-stu-id="243f0-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="243f0-164">備註</span><span class="sxs-lookup"><span data-stu-id="243f0-164">Remarks</span></span>

<span data-ttu-id="243f0-165">雖然已停止的服務和暫停的服務之間似乎沒有任何實際的差異，但是這兩個狀態會與 SCM 以不同方式顯示。</span><span class="sxs-lookup"><span data-stu-id="243f0-165">Although there might appear to be no practical difference between a service that is stopped and a service that is paused, the two states appear differently to the SCM.</span></span> <span data-ttu-id="243f0-166">已停止的服務是指未執行的服務，必須經過整個服務啟動程式。</span><span class="sxs-lookup"><span data-stu-id="243f0-166">A stopped service is a service that is not running and must go through the entire service start procedure.</span></span> <span data-ttu-id="243f0-167">不過，已暫停的服務仍在執行中，但其運作已暫止。</span><span class="sxs-lookup"><span data-stu-id="243f0-167">A paused service, however, is still running but has had its functioning is suspended.</span></span> <span data-ttu-id="243f0-168">因此，已暫停的服務不需要經過整個服務啟動程式，但需要不同的程式來繼續運作。</span><span class="sxs-lookup"><span data-stu-id="243f0-168">Because of this, a paused service does not need to go through the entire service start procedure but needs a different procedure to resume functioning.</span></span>

<span data-ttu-id="243f0-169">您必須使用適當的方法來啟動已停止的服務，或繼續已暫停的服務。</span><span class="sxs-lookup"><span data-stu-id="243f0-169">You must use the proper method to start a service that has been stopped or to resume a service that has been paused.</span></span> <span data-ttu-id="243f0-170">在下列情況下，應該使用 [**Win32 \_ 服務**](win32-service.md) 方法 [**StartService**](startservice-method-in-class-win32-service.md) 和 **ResumeService** ：</span><span class="sxs-lookup"><span data-stu-id="243f0-170">The [**Win32\_Service**](win32-service.md) methods [**StartService**](startservice-method-in-class-win32-service.md) and **ResumeService** should be used in the following situations:</span></span>

-   <span data-ttu-id="243f0-171">如果服務目前已停止，您必須使用 [**StartService**](startservice-method-in-class-win32-service.md) 方法來重新開機它。 **ResumeService** 無法啟動目前已停止的服務。</span><span class="sxs-lookup"><span data-stu-id="243f0-171">If a service is currently stopped, you must use the [**StartService**](startservice-method-in-class-win32-service.md) method to restart it; **ResumeService** cannot start a service that is currently stopped.</span></span>
-   <span data-ttu-id="243f0-172">如果服務暫停，您必須使用 **ResumeService**。</span><span class="sxs-lookup"><span data-stu-id="243f0-172">If a service is paused, you must use **ResumeService**.</span></span> <span data-ttu-id="243f0-173">如果您在已暫停的服務上使用 [**StartService**](startservice-method-in-class-win32-service.md) 方法，您會收到「服務已在執行中」的訊息。</span><span class="sxs-lookup"><span data-stu-id="243f0-173">If you use the [**StartService**](startservice-method-in-class-win32-service.md) method on a paused service, you receive the message, "The service is already running."</span></span> <span data-ttu-id="243f0-174">不過，在繼續服務控制程式代碼傳送給它之前，服務會保持暫停狀態。</span><span class="sxs-lookup"><span data-stu-id="243f0-174">However, the service remains paused until the resume service control code is sent to it.</span></span>

## <a name="examples"></a><span data-ttu-id="243f0-175">範例</span><span class="sxs-lookup"><span data-stu-id="243f0-175">Examples</span></span>

<span data-ttu-id="243f0-176">已暫停 VBScript 範例的 Resume 自動啟動 [服務會](https://Gallery.TechNet.Microsoft.Com/413f2896-e7f3-4b3e-96cb-5abdc9bb6c36) 重新開機已暫停的任何自動啟動服務。</span><span class="sxs-lookup"><span data-stu-id="243f0-176">The [Resume AutoStart Services that are Paused](https://Gallery.TechNet.Microsoft.Com/413f2896-e7f3-4b3e-96cb-5abdc9bb6c36) VBScript sample restarts any auto-start services that have been paused.</span></span>

<span data-ttu-id="243f0-177">下列 VBScript 程式碼範例說明如何從 [**Win32 \_ 服務**](win32-service.md)的實例繼續已暫停的服務。</span><span class="sxs-lookup"><span data-stu-id="243f0-177">The following VBScript code sample describes how to resume a paused service from instances of [**Win32\_Service**](win32-service.md).</span></span>

> [!Note]  
> <span data-ttu-id="243f0-178">服務必須支援暫停且已在執行中。</span><span class="sxs-lookup"><span data-stu-id="243f0-178">The service must support pausing and be running already.</span></span>

 


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='Schedule'")

for each Service in ServiceSet
 SupportsPause = Service.AcceptPause
 if SupportsPause = true then
  RetVal = Service.ResumeService()
  if RetVal = 0 then 
   WScript.Echo "Service resumed"   
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



<span data-ttu-id="243f0-179">下列 Perl 程式碼範例說明如何從 [**Win32 \_ 服務**](win32-service.md)的實例繼續已暫停的服務。</span><span class="sxs-lookup"><span data-stu-id="243f0-179">The following Perl code sample describes how to resume a paused service from instances of [**Win32\_Service**](win32-service.md).</span></span>

> [!Note]  
> <span data-ttu-id="243f0-180">服務必須支援暫停且已在執行中。</span><span class="sxs-lookup"><span data-stu-id="243f0-180">The service must support pausing and be running already.</span></span>

 


```Perl
use strict;
use Win32::OLE;

my $ServiceSet;

eval { $ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\Root\\CIMv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='Schedule'"); };

if (!$@ && defined $ServiceSet)
{
 foreach my $Service (in $ServiceSet)
 {
  my $SupportsPause = $Service->{AcceptPause};
  if ($SupportsPause)
  {
   my $RetVal = $Service->ResumeService();
   if ($RetVal == 0)
   {
    print "\nService resumed\n";
   }
   else
   {
    if ($RetVal == 1)
    {
     print STDERR "\nPause not supported\n";
    }
    else
    {
     print STDERR "\nAn error occurred: ", $RetVal, "\n";
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
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="243f0-181">規格需求</span><span class="sxs-lookup"><span data-stu-id="243f0-181">Requirements</span></span>



| <span data-ttu-id="243f0-182">需求</span><span class="sxs-lookup"><span data-stu-id="243f0-182">Requirement</span></span> | <span data-ttu-id="243f0-183">值</span><span class="sxs-lookup"><span data-stu-id="243f0-183">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="243f0-184">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="243f0-184">Minimum supported client</span></span><br/> | <span data-ttu-id="243f0-185">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="243f0-185">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="243f0-186">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="243f0-186">Minimum supported server</span></span><br/> | <span data-ttu-id="243f0-187">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="243f0-187">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="243f0-188">命名空間</span><span class="sxs-lookup"><span data-stu-id="243f0-188">Namespace</span></span><br/>                | <span data-ttu-id="243f0-189">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="243f0-189">Root\\CIMv2</span></span><br/>                                                                  |
| <span data-ttu-id="243f0-190">MOF</span><span class="sxs-lookup"><span data-stu-id="243f0-190">MOF</span></span><br/>                      | <dl> <span data-ttu-id="243f0-191"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="243f0-191"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="243f0-192">DLL</span><span class="sxs-lookup"><span data-stu-id="243f0-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="243f0-193"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="243f0-193"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="243f0-194">另請參閱</span><span class="sxs-lookup"><span data-stu-id="243f0-194">See also</span></span>

<dl> <dt>

<span data-ttu-id="243f0-195">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="243f0-195">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="243f0-196">**Win32 \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="243f0-196">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="243f0-197">WMI 工作：服務</span><span class="sxs-lookup"><span data-stu-id="243f0-197">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 


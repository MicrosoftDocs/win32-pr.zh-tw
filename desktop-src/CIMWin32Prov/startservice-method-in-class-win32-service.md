---
description: Win32_Service 類別的 StartService 方法 (CIMWin32 WMI 提供者) -嘗試將參考的服務放入其啟動狀態。
ms.assetid: b7a815a2-7bf6-436f-b3b4-de55eeb2de0e
ms.tgt_platform: multiple
title: " (CIMWin32 WMI 提供者的 Win32_Service 類別的 StartService 方法) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a630b9d926ff5377312f1c67630a20816ab38b6c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086156"
---
# <a name="startservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="afacc-103"> (CIMWin32 WMI 提供者的 Win32_Service 類別的 StartService 方法) </span><span class="sxs-lookup"><span data-stu-id="afacc-103">StartService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="afacc-104">**StartService** 方法會嘗試將參考的服務置於啟動狀態。</span><span class="sxs-lookup"><span data-stu-id="afacc-104">The **StartService** method attempts to place the referenced service into its startup state.</span></span>

<span data-ttu-id="afacc-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="afacc-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="afacc-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="afacc-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="afacc-107">語法</span><span class="sxs-lookup"><span data-stu-id="afacc-107">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="afacc-108">參數</span><span class="sxs-lookup"><span data-stu-id="afacc-108">Parameters</span></span>

<span data-ttu-id="afacc-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="afacc-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="afacc-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="afacc-110">Return value</span></span>

<span data-ttu-id="afacc-111">傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="afacc-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="afacc-112">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="afacc-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="afacc-113">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="afacc-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="afacc-114">**0**</span><span class="sxs-lookup"><span data-stu-id="afacc-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="afacc-115">要求已被接受。</span><span class="sxs-lookup"><span data-stu-id="afacc-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="afacc-116">**1**</span><span class="sxs-lookup"><span data-stu-id="afacc-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="afacc-117">不支援此要求。</span><span class="sxs-lookup"><span data-stu-id="afacc-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="afacc-118">**2**</span><span class="sxs-lookup"><span data-stu-id="afacc-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="afacc-119">使用者沒有必要的存取權。</span><span class="sxs-lookup"><span data-stu-id="afacc-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="afacc-120">**3**</span><span class="sxs-lookup"><span data-stu-id="afacc-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="afacc-121">無法停止此服務，因為與它相依的其他服務正在執行中。</span><span class="sxs-lookup"><span data-stu-id="afacc-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="afacc-122">**4**</span><span class="sxs-lookup"><span data-stu-id="afacc-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="afacc-123">要求的控制碼無效，或是服務不接受此控制碼。</span><span class="sxs-lookup"><span data-stu-id="afacc-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="afacc-124">**5**</span><span class="sxs-lookup"><span data-stu-id="afacc-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="afacc-125">因為服務的狀態 ([**Win32 \_ BaseService**](win32-baseservice.md)，所以無法將要求的控制項程式碼傳送至服務。**State** 屬性) 等於0、1或2。</span><span class="sxs-lookup"><span data-stu-id="afacc-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="afacc-126">**6**</span><span class="sxs-lookup"><span data-stu-id="afacc-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="afacc-127">尚未啟動服務。</span><span class="sxs-lookup"><span data-stu-id="afacc-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="afacc-128">**7**</span><span class="sxs-lookup"><span data-stu-id="afacc-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="afacc-129">服務並未及時回應啟動要求。</span><span class="sxs-lookup"><span data-stu-id="afacc-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="afacc-130">**8**</span><span class="sxs-lookup"><span data-stu-id="afacc-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="afacc-131">啟動服務時發生未知的錯誤。</span><span class="sxs-lookup"><span data-stu-id="afacc-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="afacc-132">**9**</span><span class="sxs-lookup"><span data-stu-id="afacc-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="afacc-133">找不到服務可執行檔的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="afacc-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="afacc-134">**10**</span><span class="sxs-lookup"><span data-stu-id="afacc-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="afacc-135">服務已在執行中。</span><span class="sxs-lookup"><span data-stu-id="afacc-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="afacc-136">**11**</span><span class="sxs-lookup"><span data-stu-id="afacc-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="afacc-137">要加入新服務的資料庫已被鎖定。</span><span class="sxs-lookup"><span data-stu-id="afacc-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="afacc-138">**12**</span><span class="sxs-lookup"><span data-stu-id="afacc-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="afacc-139">這項服務所依賴的相依性已從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="afacc-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="afacc-140">**13**</span><span class="sxs-lookup"><span data-stu-id="afacc-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="afacc-141">服務在相依的服務中找不到所需的服務。</span><span class="sxs-lookup"><span data-stu-id="afacc-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="afacc-142">**14**</span><span class="sxs-lookup"><span data-stu-id="afacc-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="afacc-143">已經從系統中停用服務。</span><span class="sxs-lookup"><span data-stu-id="afacc-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="afacc-144">**15**</span><span class="sxs-lookup"><span data-stu-id="afacc-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="afacc-145">此服務未通過驗證，無法在系統上執行。</span><span class="sxs-lookup"><span data-stu-id="afacc-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="afacc-146">**16**</span><span class="sxs-lookup"><span data-stu-id="afacc-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="afacc-147">這項服務正在從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="afacc-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="afacc-148">**17**</span><span class="sxs-lookup"><span data-stu-id="afacc-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="afacc-149">服務沒有執行執行緒。</span><span class="sxs-lookup"><span data-stu-id="afacc-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="afacc-150">**達**</span><span class="sxs-lookup"><span data-stu-id="afacc-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="afacc-151">服務會在啟動時有迴圈相依性。</span><span class="sxs-lookup"><span data-stu-id="afacc-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="afacc-152">**診斷**</span><span class="sxs-lookup"><span data-stu-id="afacc-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="afacc-153">服務正在相同名稱下執行。</span><span class="sxs-lookup"><span data-stu-id="afacc-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="afacc-154">**20**</span><span class="sxs-lookup"><span data-stu-id="afacc-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="afacc-155">服務名稱包含不正確字元。</span><span class="sxs-lookup"><span data-stu-id="afacc-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="afacc-156">**21**</span><span class="sxs-lookup"><span data-stu-id="afacc-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="afacc-157">傳遞給服務的參數無效。</span><span class="sxs-lookup"><span data-stu-id="afacc-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="afacc-158">**22**</span><span class="sxs-lookup"><span data-stu-id="afacc-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="afacc-159">用來執行此服務的帳戶無效，或缺少執行服務的許可權。</span><span class="sxs-lookup"><span data-stu-id="afacc-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="afacc-160">**23**</span><span class="sxs-lookup"><span data-stu-id="afacc-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="afacc-161">服務存在於系統可使用之服務的資料庫中。</span><span class="sxs-lookup"><span data-stu-id="afacc-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="afacc-162">**24**</span><span class="sxs-lookup"><span data-stu-id="afacc-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="afacc-163">服務目前在系統中暫停。</span><span class="sxs-lookup"><span data-stu-id="afacc-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="afacc-164">備註</span><span class="sxs-lookup"><span data-stu-id="afacc-164">Remarks</span></span>

<span data-ttu-id="afacc-165">雖然已停止的服務和暫停的服務之間似乎沒有任何實際的差異，但是這兩個狀態會與 SCM 以不同方式顯示。</span><span class="sxs-lookup"><span data-stu-id="afacc-165">Although there might appear to be no practical difference between a service that is stopped and a service that is paused, the two states appear differently to the SCM.</span></span> <span data-ttu-id="afacc-166">已停止的服務是指未執行的服務，必須經過整個服務啟動程式。</span><span class="sxs-lookup"><span data-stu-id="afacc-166">A stopped service is a service that is not running and must go through the entire service start procedure.</span></span> <span data-ttu-id="afacc-167">不過，已暫停的服務仍在執行中，但其運作已暫止。</span><span class="sxs-lookup"><span data-stu-id="afacc-167">A paused service, however, is still running but has had its functioning is suspended.</span></span> <span data-ttu-id="afacc-168">因此，已暫停的服務不需要經過整個服務啟動程式，但需要不同的程式來繼續運作。</span><span class="sxs-lookup"><span data-stu-id="afacc-168">Because of this, a paused service does not need to go through the entire service start procedure but needs a different procedure to resume functioning.</span></span>

<span data-ttu-id="afacc-169">您必須使用適當的方法來啟動已停止的服務，或繼續已暫停的服務。</span><span class="sxs-lookup"><span data-stu-id="afacc-169">You must use the proper method to start a service that has been stopped or to resume a service that has been paused.</span></span> <span data-ttu-id="afacc-170">在下列情況下，應該使用 [**Win32 \_ 服務**](win32-service.md) 方法 **StartService** 和 [**ResumeService**](resumeservice-method-in-class-win32-service.md) ：</span><span class="sxs-lookup"><span data-stu-id="afacc-170">The [**Win32\_Service**](win32-service.md) methods **StartService** and [**ResumeService**](resumeservice-method-in-class-win32-service.md) should be used in the following situations:</span></span>

-   <span data-ttu-id="afacc-171">如果服務目前已停止，您必須使用 **StartService** 方法來重新開機它。 [**ResumeService**](resumeservice-method-in-class-win32-service.md) 無法啟動目前已停止的服務。</span><span class="sxs-lookup"><span data-stu-id="afacc-171">If a service is currently stopped, you must use the **StartService** method to restart it; [**ResumeService**](resumeservice-method-in-class-win32-service.md) cannot start a service that is currently stopped.</span></span>
-   <span data-ttu-id="afacc-172">如果服務暫停，您必須使用 [**ResumeService**](resumeservice-method-in-class-win32-service.md)。</span><span class="sxs-lookup"><span data-stu-id="afacc-172">If a service is paused, you must use [**ResumeService**](resumeservice-method-in-class-win32-service.md).</span></span> <span data-ttu-id="afacc-173">如果您在已暫停的服務上使用 **StartService** 方法，您會收到「服務已在執行中」的訊息。</span><span class="sxs-lookup"><span data-stu-id="afacc-173">If you use the **StartService** method on a paused service, you receive the message, "The service is already running."</span></span> <span data-ttu-id="afacc-174">不過，在繼續服務控制程式代碼傳送給它之前，服務會保持暫停狀態。</span><span class="sxs-lookup"><span data-stu-id="afacc-174">However, the service remains paused until the resume service control code is sent to it.</span></span>

<span data-ttu-id="afacc-175">如果您啟動相依于其他服務的已停止服務，則這兩個服務都會啟動。</span><span class="sxs-lookup"><span data-stu-id="afacc-175">If you start a stopped service that depends on another service, then both services are started.</span></span> <span data-ttu-id="afacc-176">使用這個方法啟動服務時，不會自動啟動任何相依的服務。</span><span class="sxs-lookup"><span data-stu-id="afacc-176">When a service is started with this method, any dependent services are not automatically started.</span></span> <span data-ttu-id="afacc-177">您必須使用 association 類別 [**Win32 \_ DependentService**](win32-dependentservice.md) 和查詢的 [associators of](/windows/desktop/WmiSdk/associators-of-statement) 來找出相依專案，然後個別啟動它們。</span><span class="sxs-lookup"><span data-stu-id="afacc-177">You must use the association class [**Win32\_DependentService**](win32-dependentservice.md) and the [Associators Of](/windows/desktop/WmiSdk/associators-of-statement) query to locate the dependents and start them separately.</span></span>

## <a name="examples"></a><span data-ttu-id="afacc-178">範例</span><span class="sxs-lookup"><span data-stu-id="afacc-178">Examples</span></span>

<span data-ttu-id="afacc-179">遠端 [啟用 RDP](https://Gallery.TechNet.Microsoft.Com/Remotely-Enable-RDP-855c3842) PowerShell 範例會啟用遠端桌面服務。</span><span class="sxs-lookup"><span data-stu-id="afacc-179">The [Remotely Enable RDP](https://Gallery.TechNet.Microsoft.Com/Remotely-Enable-RDP-855c3842) PowerShell sample remotely enables the Remote Desktop service.</span></span>

<span data-ttu-id="afacc-180">[停止、啟動、啟用或停用服務](https://Gallery.TechNet.Microsoft.Com/212e68f0-5279-4499-8e9e-6aa1807719c0)PowerShell 範例會啟動、停止、啟用或停用服務。</span><span class="sxs-lookup"><span data-stu-id="afacc-180">The [Stop, Start, Enable or Disable Service](https://Gallery.TechNet.Microsoft.Com/212e68f0-5279-4499-8e9e-6aa1807719c0) PowerShell sample starts, stops, enables, or disables a service.</span></span>

<span data-ttu-id="afacc-181">下列 VBSScript 程式碼範例示範如何從 [**Win32 \_ 服務**](win32-service.md)的實例啟動特定的服務。</span><span class="sxs-lookup"><span data-stu-id="afacc-181">The following VBSScript code sample demonstrates how to start a specific service from instances of [**Win32\_Service**](win32-service.md).</span></span>


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='ClipSrv'")

for each Service in ServiceSet
 RetVal = Service.StartService()
 if RetVal = 0 then WScript.Echo "Service started"
 if RetVal = 10 then WScript.Echo "Service already running"
next
```



<span data-ttu-id="afacc-182">下列 Perl 程式碼範例示範如何從 [**Win32 \_ 服務**](win32-service.md)的實例啟動特定的服務。</span><span class="sxs-lookup"><span data-stu-id="afacc-182">The following Perl code sample demonstrates how to start a specific service from instances of [**Win32\_Service**](win32-service.md).</span></span>


```
use strict;
use Win32::OLE;

my $ServiceSet;

eval { $ServiceSet = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='ClipSrv'"); };

if(!$@ && defined $ServiceSet)
{
 foreach my $service (in $ServiceSet)
 {
  my $Result = $service->StartService();
  if ($Result == 0) 
  {
   print "\nService started\n";
  }
  elsif ($Result == 10)
  {
   print "\nService already running\n";
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="afacc-183">下列 VBScript 程式碼範例（NetDDE）相依于 NetDDEDSDM 服務。</span><span class="sxs-lookup"><span data-stu-id="afacc-183">The following VBScript code example, NetDDE, is dependent on the NetDDEDSDM service.</span></span> <span data-ttu-id="afacc-184">腳本會找出 NetDDE 相依的類別，並加以啟動，而不會自動啟動 NetDDE。</span><span class="sxs-lookup"><span data-stu-id="afacc-184">The script locates the class on which NetDDE depends and starts it, which does not automatically start NetDDE.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

' Stop NetDDE if it is running
Set objNetDDEService = objWMIService.Get("Win32_Service.Name='NetDDE'")
Return = objNetDDEService.StopService()

' NetDDE is in the dependent role to another service
Set colServiceList = objWMIService.ExecQuery("Associators of " _
    & "{Win32_Service.Name='NetDDE'} Where " & "AssocClass=Win32_DependentService " & "Role=Dependent" )

' start the service on which NetDDE is dependent
For Each objService in colServiceList
    WScript.Echo "Starting " & objService.Name
    Return = objService.StartService()
    If Return = 0 Then
        WScript.Echo "Parent service " & objService.Name & " started successfully"
    Else
        WScript.Echo "Parent service " & objService.Name & " did not start. Return = " & Return
    End If
Next

' NetDDE is still stopped
Set objNetDDEService = _
    objWMIService.Get("Win32_Service.Name='NetDDE'")
WScript.Echo "Dependent NetDDE service is " & objNetDDEService.State
```



## <a name="requirements"></a><span data-ttu-id="afacc-185">規格需求</span><span class="sxs-lookup"><span data-stu-id="afacc-185">Requirements</span></span>



| <span data-ttu-id="afacc-186">需求</span><span class="sxs-lookup"><span data-stu-id="afacc-186">Requirement</span></span> | <span data-ttu-id="afacc-187">值</span><span class="sxs-lookup"><span data-stu-id="afacc-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="afacc-188">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="afacc-188">Minimum supported client</span></span><br/> | <span data-ttu-id="afacc-189">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="afacc-189">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="afacc-190">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="afacc-190">Minimum supported server</span></span><br/> | <span data-ttu-id="afacc-191">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="afacc-191">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="afacc-192">命名空間</span><span class="sxs-lookup"><span data-stu-id="afacc-192">Namespace</span></span><br/>                | <span data-ttu-id="afacc-193">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="afacc-193">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="afacc-194">MOF</span><span class="sxs-lookup"><span data-stu-id="afacc-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="afacc-195"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="afacc-195"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="afacc-196">DLL</span><span class="sxs-lookup"><span data-stu-id="afacc-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afacc-197"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afacc-197"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afacc-198">另請參閱</span><span class="sxs-lookup"><span data-stu-id="afacc-198">See also</span></span>

<dl> <dt>

<span data-ttu-id="afacc-199">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="afacc-199">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="afacc-200">**Win32 \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="afacc-200">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="afacc-201">WMI 工作：服務</span><span class="sxs-lookup"><span data-stu-id="afacc-201">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 


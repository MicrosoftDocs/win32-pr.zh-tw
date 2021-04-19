---
description: 將服務（由 Win32 \_ 服務物件表示）置於已停止狀態。
ms.assetid: cc2c71f7-12e6-4ba4-bfb4-f23845d798b5
ms.tgt_platform: multiple
title: 'Win32_Service 類別的 StopService 方法 (Sdoias) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 90d979754a3d6f034c353229dbaa1b1dbaedea79
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989894"
---
# <a name="stopservice-method-of-the-win32_service-class-sdoiash"></a><span data-ttu-id="bb058-103">Win32_Service 類別的 StopService 方法 (Sdoias) </span><span class="sxs-lookup"><span data-stu-id="bb058-103">StopService method of the Win32_Service class (Sdoias.h)</span></span>

<span data-ttu-id="bb058-104">**StopService** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會將服務（由 [**Win32 \_ 服務**](win32-service.md)物件表示）置於已停止狀態。</span><span class="sxs-lookup"><span data-stu-id="bb058-104">The **StopService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method places the service, represented by the [**Win32\_Service**](win32-service.md) object, in the stopped state.</span></span>

<span data-ttu-id="bb058-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="bb058-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="bb058-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="bb058-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="bb058-107">語法</span><span class="sxs-lookup"><span data-stu-id="bb058-107">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="bb058-108">參數</span><span class="sxs-lookup"><span data-stu-id="bb058-108">Parameters</span></span>

<span data-ttu-id="bb058-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="bb058-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bb058-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="bb058-110">Return value</span></span>

<span data-ttu-id="bb058-111">傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="bb058-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="bb058-112">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="bb058-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="bb058-113">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="bb058-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="bb058-114">**0**</span><span class="sxs-lookup"><span data-stu-id="bb058-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="bb058-115">要求已被接受。</span><span class="sxs-lookup"><span data-stu-id="bb058-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="bb058-116">**1**</span><span class="sxs-lookup"><span data-stu-id="bb058-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="bb058-117">不支援此要求。</span><span class="sxs-lookup"><span data-stu-id="bb058-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="bb058-118">**2**</span><span class="sxs-lookup"><span data-stu-id="bb058-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="bb058-119">使用者沒有必要的存取權。</span><span class="sxs-lookup"><span data-stu-id="bb058-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="bb058-120">**3**</span><span class="sxs-lookup"><span data-stu-id="bb058-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="bb058-121">無法停止此服務，因為與它相依的其他服務正在執行中。</span><span class="sxs-lookup"><span data-stu-id="bb058-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="bb058-122">**4**</span><span class="sxs-lookup"><span data-stu-id="bb058-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="bb058-123">要求的控制碼無效，或是服務不接受此控制碼。</span><span class="sxs-lookup"><span data-stu-id="bb058-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="bb058-124">**5**</span><span class="sxs-lookup"><span data-stu-id="bb058-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="bb058-125">因為服務的狀態 ([**Win32 \_ BaseService**](win32-baseservice.md)，所以無法將要求的控制項程式碼傳送至服務。**State** 屬性) 等於0、1或2。</span><span class="sxs-lookup"><span data-stu-id="bb058-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="bb058-126">**6**</span><span class="sxs-lookup"><span data-stu-id="bb058-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="bb058-127">尚未啟動服務。</span><span class="sxs-lookup"><span data-stu-id="bb058-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="bb058-128">**7**</span><span class="sxs-lookup"><span data-stu-id="bb058-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="bb058-129">服務並未及時回應啟動要求。</span><span class="sxs-lookup"><span data-stu-id="bb058-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="bb058-130">**8**</span><span class="sxs-lookup"><span data-stu-id="bb058-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="bb058-131">啟動服務時發生未知的錯誤。</span><span class="sxs-lookup"><span data-stu-id="bb058-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="bb058-132">**9**</span><span class="sxs-lookup"><span data-stu-id="bb058-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="bb058-133">找不到服務可執行檔的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="bb058-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="bb058-134">**10**</span><span class="sxs-lookup"><span data-stu-id="bb058-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="bb058-135">服務已在執行中。</span><span class="sxs-lookup"><span data-stu-id="bb058-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="bb058-136">**11**</span><span class="sxs-lookup"><span data-stu-id="bb058-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="bb058-137">要加入新服務的資料庫已被鎖定。</span><span class="sxs-lookup"><span data-stu-id="bb058-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="bb058-138">**12**</span><span class="sxs-lookup"><span data-stu-id="bb058-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="bb058-139">這項服務所依賴的相依性已從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="bb058-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="bb058-140">**13**</span><span class="sxs-lookup"><span data-stu-id="bb058-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="bb058-141">服務在相依的服務中找不到所需的服務。</span><span class="sxs-lookup"><span data-stu-id="bb058-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="bb058-142">**14**</span><span class="sxs-lookup"><span data-stu-id="bb058-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="bb058-143">已經從系統中停用服務。</span><span class="sxs-lookup"><span data-stu-id="bb058-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="bb058-144">**15**</span><span class="sxs-lookup"><span data-stu-id="bb058-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="bb058-145">此服務未通過驗證，無法在系統上執行。</span><span class="sxs-lookup"><span data-stu-id="bb058-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="bb058-146">**16**</span><span class="sxs-lookup"><span data-stu-id="bb058-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="bb058-147">這項服務正在從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="bb058-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="bb058-148">**17**</span><span class="sxs-lookup"><span data-stu-id="bb058-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="bb058-149">服務沒有執行執行緒。</span><span class="sxs-lookup"><span data-stu-id="bb058-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="bb058-150">**達**</span><span class="sxs-lookup"><span data-stu-id="bb058-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="bb058-151">服務會在啟動時有迴圈相依性。</span><span class="sxs-lookup"><span data-stu-id="bb058-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="bb058-152">**診斷**</span><span class="sxs-lookup"><span data-stu-id="bb058-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="bb058-153">服務正在相同名稱下執行。</span><span class="sxs-lookup"><span data-stu-id="bb058-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="bb058-154">**20**</span><span class="sxs-lookup"><span data-stu-id="bb058-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="bb058-155">服務名稱包含不正確字元。</span><span class="sxs-lookup"><span data-stu-id="bb058-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="bb058-156">**21**</span><span class="sxs-lookup"><span data-stu-id="bb058-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="bb058-157">傳遞給服務的參數無效。</span><span class="sxs-lookup"><span data-stu-id="bb058-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="bb058-158">**22**</span><span class="sxs-lookup"><span data-stu-id="bb058-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="bb058-159">用來執行此服務的帳戶無效，或缺少執行服務的許可權。</span><span class="sxs-lookup"><span data-stu-id="bb058-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="bb058-160">**23**</span><span class="sxs-lookup"><span data-stu-id="bb058-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="bb058-161">服務存在於系統可使用之服務的資料庫中。</span><span class="sxs-lookup"><span data-stu-id="bb058-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="bb058-162">**24**</span><span class="sxs-lookup"><span data-stu-id="bb058-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="bb058-163">服務目前在系統中暫停。</span><span class="sxs-lookup"><span data-stu-id="bb058-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bb058-164">備註</span><span class="sxs-lookup"><span data-stu-id="bb058-164">Remarks</span></span>

<span data-ttu-id="bb058-165">確定可以停止或暫停的服務之後，您可以使用 **StopService** 和 [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md) 方法來停止和暫停服務。</span><span class="sxs-lookup"><span data-stu-id="bb058-165">After you have determined which services can be stopped or paused, you can use the **StopService** and [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md) methods to stop and pause services.</span></span> <span data-ttu-id="bb058-166">停止服務而非暫停服務（反之亦然）的決策取決於數個因素，包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="bb058-166">The decision to stop a service rather than pause it, or vice versa, depends on several factors, including the following:</span></span>

-   <span data-ttu-id="bb058-167">服務是否能夠暫停？</span><span class="sxs-lookup"><span data-stu-id="bb058-167">Is the service capable of being paused?</span></span> <span data-ttu-id="bb058-168">如果沒有，則您的唯一選項是停止服務。</span><span class="sxs-lookup"><span data-stu-id="bb058-168">If not, your only option is the stop the service.</span></span>
-   <span data-ttu-id="bb058-169">您是否需要繼續處理已連線到服務的任何人的用戶端要求？</span><span class="sxs-lookup"><span data-stu-id="bb058-169">Do you need to continue handling client requests for anyone already connected to the service?</span></span> <span data-ttu-id="bb058-170">若是如此，暫停服務通常會允許它處理現有的用戶端，同時拒絕存取新的用戶端。</span><span class="sxs-lookup"><span data-stu-id="bb058-170">If so, pausing a service typically allows it to handle existing clients while denying access to new clients.</span></span> <span data-ttu-id="bb058-171">相反地，當您停止服務時，所有用戶端都會立即中斷連線。</span><span class="sxs-lookup"><span data-stu-id="bb058-171">By contrast, when you stop a service, all clients are immediately disconnected.</span></span>
-   <span data-ttu-id="bb058-172">您是否需要重新設定服務，並讓變更立即生效？</span><span class="sxs-lookup"><span data-stu-id="bb058-172">Do you need to reconfigure a service and have the changes take effect immediately?</span></span> <span data-ttu-id="bb058-173">雖然服務屬性可以在服務暫停時變更，但大部分的服務都不會在服務實際停止並重新啟動之前生效。</span><span class="sxs-lookup"><span data-stu-id="bb058-173">Although service properties can be changed while a service is paused, most of them do not take effect until the service is actually stopped and restarted.</span></span>

<span data-ttu-id="bb058-174">停止服務所需的腳本程式碼與暫停服務所需的程式碼幾乎完全相同。</span><span class="sxs-lookup"><span data-stu-id="bb058-174">The scripting code required to stop a service is almost identical to the code required to pause the service.</span></span>

<span data-ttu-id="bb058-175">如果您嘗試停止具有相依服務的服務正在執行， **StopService** 方法會失敗，並傳回值3。</span><span class="sxs-lookup"><span data-stu-id="bb058-175">If you attempt to stop a service which has dependent services running, the **StopService** method fails with a return value of 3.</span></span> <span data-ttu-id="bb058-176">必須先停止相依的服務。</span><span class="sxs-lookup"><span data-stu-id="bb058-176">The dependent services must be stopped first.</span></span>

<span data-ttu-id="bb058-177">如果您停止服務，請立即檢查 [**Win32 \_ 服務**](win32-service.md)。**狀態** 屬性，因為值仍可能顯示服務為執行中。</span><span class="sxs-lookup"><span data-stu-id="bb058-177">If you stop a service, then immediately check the [**Win32\_Service**](win32-service.md).**State** property, as the value may still show the service as running.</span></span>

## <a name="examples"></a><span data-ttu-id="bb058-178">範例</span><span class="sxs-lookup"><span data-stu-id="bb058-178">Examples</span></span>

<span data-ttu-id="bb058-179">[RemoteService](https://Gallery.TechNet.Microsoft.Com/79595ce9-bfc3-463e-9e84-d9e0b78590c1) PowerShell 範例會設定遠端電腦的服務狀態。</span><span class="sxs-lookup"><span data-stu-id="bb058-179">[The Set-RemoteService](https://Gallery.TechNet.Microsoft.Com/79595ce9-bfc3-463e-9e84-d9e0b78590c1) PowerShell sample Sets service state for remote machines.</span></span>

<span data-ttu-id="bb058-180">[停止服務及其相依的](https://Gallery.TechNet.Microsoft.Com/ae07e623-2cbd-4983-b991-aa4d1e6e2732)VBScript 範例會停止服務和所有相依的服務。</span><span class="sxs-lookup"><span data-stu-id="bb058-180">The [Stop a Service and Its Dependents](https://Gallery.TechNet.Microsoft.Com/ae07e623-2cbd-4983-b991-aa4d1e6e2732) VBScript sample stops a service and all dependent services.</span></span>

<span data-ttu-id="bb058-181">下列 VBScript 程式碼範例示範如何關閉服務。</span><span class="sxs-lookup"><span data-stu-id="bb058-181">The following VBScript code sample demonstrates how to shut down a service.</span></span>


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='ClipSrv'")

for each Service in ServiceSet
 RetVal = Service.StopService()
 if RetVal = 0 then 
  WScript.Echo "Service stopped" 
 elseif RetVal = 5 then 
  WScript.Echo "Service already stopped" 
 end if
next
```



<span data-ttu-id="bb058-182">下列 Perl 程式碼範例會示範如何關閉服務。</span><span class="sxs-lookup"><span data-stu-id="bb058-182">The following Perl code sample demonstrates how to shut down a service.</span></span>


```
use strict;
use Win32::OLE;

my $ServiceSet;

eval { $ServiceSet = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='ClipSrv'"); };

if (!$@ && defined $ServiceSet)
{
 foreach my $ServiceInst (in $ServiceSet)
 {
  my $Result = $ServiceInst->StopService();
  if ($Result == 0)
  {
   print "\nService stopped\n";
  }
  elsif ($Result == 5) 
  {
   print "\nService already stopped\n";
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="bb058-183">下列 VBScript 程式碼範例顯示在已停止相依服務之前，您無法停止 NetDDE 的服務。</span><span class="sxs-lookup"><span data-stu-id="bb058-183">The following VBScript code example shows that you cannot stop the NetDDE service until the dependent services have been stopped.</span></span> <span data-ttu-id="bb058-184">若要執行腳本，請使用 services.msc MMC 嵌入式管理單元或 **Net Start** 命令，確定 NetDDE 服務及其相依的服務是否正在執行。</span><span class="sxs-lookup"><span data-stu-id="bb058-184">To run the script, ensure that the NetDDE service and its dependent services are running by using the Services.msc MMC snap-in or the **Net Start** command.</span></span>

<span data-ttu-id="bb058-185">[**Win32 \_ DependentService**](win32-dependentservice.md)類別可讓您透過查詢 [associators of](/windows/desktop/WmiSdk/associators-of-statement)尋找服務相依性。</span><span class="sxs-lookup"><span data-stu-id="bb058-185">The [**Win32\_DependentService**](win32-dependentservice.md) class allows you to locate service dependencies through an [Associators Of](/windows/desktop/WmiSdk/associators-of-statement) query.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & _
    strComputer & "\root\cimv2")

Set objNetDDEservice = _
    objWMIService.Get("Win32_Service.Name='NetDDE'")

WScript.Echo "NetDDE service state: " & objNetDDEService.State
WScript.Echo "Stopping NetDDE service"
Return = objNetDDEService.StopService()
WScript.Echo "Return value: " & Return  & _
    "  Service cannot be stopped because " & _
    "dependent services are running"

Set colServiceList = objWMIService.ExecQuery("Associators of " _
    & "{Win32_Service.Name='NetDDE'} Where " _
        & "AssocClass=Win32_DependentService " & _
    "Role=Antecedent" )

For Each objService in colServiceList
   WScript.Echo "Dependent service: " & objService.Name & _
   "   State: " & objService.State
   WScript.Echo "Stopping dependent service " & objService.Name
   objService.StopService()    
Next

Wscript.Sleep 20000
WScript.Echo "Stopping NetDDE service"
Return = objNetDDEService.StopService()
WScript.Echo "Return value: " & Return
```



## <a name="requirements"></a><span data-ttu-id="bb058-186">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb058-186">Requirements</span></span>



| <span data-ttu-id="bb058-187">需求</span><span class="sxs-lookup"><span data-stu-id="bb058-187">Requirement</span></span> | <span data-ttu-id="bb058-188">值</span><span class="sxs-lookup"><span data-stu-id="bb058-188">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb058-189">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bb058-189">Minimum supported client</span></span><br/> | <span data-ttu-id="bb058-190">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bb058-190">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bb058-191">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bb058-191">Minimum supported server</span></span><br/> | <span data-ttu-id="bb058-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bb058-192">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bb058-193">命名空間</span><span class="sxs-lookup"><span data-stu-id="bb058-193">Namespace</span></span><br/>                | <span data-ttu-id="bb058-194">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="bb058-194">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bb058-195">標頭</span><span class="sxs-lookup"><span data-stu-id="bb058-195">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb058-196"><dt>Sdoias。h</dt></span><span class="sxs-lookup"><span data-stu-id="bb058-196"><dt>Sdoias.h</dt></span></span> </dl>     |
| <span data-ttu-id="bb058-197">MOF</span><span class="sxs-lookup"><span data-stu-id="bb058-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bb058-198"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="bb058-198"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bb058-199">DLL</span><span class="sxs-lookup"><span data-stu-id="bb058-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb058-200"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb058-200"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb058-201">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb058-201">See also</span></span>

<dl> <dt>

<span data-ttu-id="bb058-202">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bb058-202">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="bb058-203">**Win32 \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="bb058-203">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="bb058-204">WMI 工作：服務</span><span class="sxs-lookup"><span data-stu-id="bb058-204">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[<span data-ttu-id="bb058-205">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="bb058-205">**PauseService**</span></span>](pauseservice-method-in-class-win32-systemdriver.md)
</dt> </dl>

 


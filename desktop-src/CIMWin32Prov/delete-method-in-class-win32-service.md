---
description: Delete&\# 8194;WMI 類別方法會刪除現有的服務。
ms.assetid: aa4e7630-3b19-47dd-acd1-4d1735acb819
ms.tgt_platform: multiple
title: " (CIMWin32 WMI 提供者來刪除 Win32_Service 類別的方法) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d06301c3620e144d72c2d4c4f3d8bc90e642374a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187747"
---
# <a name="delete-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="0d81e-103"> (CIMWin32 WMI 提供者來刪除 Win32_Service 類別的方法) </span><span class="sxs-lookup"><span data-stu-id="0d81e-103">Delete method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="0d81e-104">**Delete** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會刪除現有的服務。</span><span class="sxs-lookup"><span data-stu-id="0d81e-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes an existing service.</span></span>

<span data-ttu-id="0d81e-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="0d81e-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0d81e-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="0d81e-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0d81e-107">語法</span><span class="sxs-lookup"><span data-stu-id="0d81e-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="0d81e-108">參數</span><span class="sxs-lookup"><span data-stu-id="0d81e-108">Parameters</span></span>

<span data-ttu-id="0d81e-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="0d81e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0d81e-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="0d81e-110">Return value</span></span>

<span data-ttu-id="0d81e-111">傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="0d81e-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="0d81e-112">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="0d81e-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="0d81e-113">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="0d81e-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="0d81e-114">**0**</span><span class="sxs-lookup"><span data-stu-id="0d81e-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="0d81e-115">要求已被接受。</span><span class="sxs-lookup"><span data-stu-id="0d81e-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="0d81e-116">**1**</span><span class="sxs-lookup"><span data-stu-id="0d81e-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="0d81e-117">不支援此要求。</span><span class="sxs-lookup"><span data-stu-id="0d81e-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="0d81e-118">**2**</span><span class="sxs-lookup"><span data-stu-id="0d81e-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="0d81e-119">使用者沒有必要的存取權。</span><span class="sxs-lookup"><span data-stu-id="0d81e-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="0d81e-120">**3**</span><span class="sxs-lookup"><span data-stu-id="0d81e-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="0d81e-121">無法停止此服務，因為與它相依的其他服務正在執行中。</span><span class="sxs-lookup"><span data-stu-id="0d81e-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="0d81e-122">**4**</span><span class="sxs-lookup"><span data-stu-id="0d81e-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="0d81e-123">要求的控制碼無效，或是服務不接受此控制碼。</span><span class="sxs-lookup"><span data-stu-id="0d81e-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="0d81e-124">**5**</span><span class="sxs-lookup"><span data-stu-id="0d81e-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="0d81e-125">因為服務的狀態 ([**Win32 \_ BaseService**](win32-baseservice.md)，所以無法將要求的控制項程式碼傳送至服務。**State** 屬性) 等於0、1或2。</span><span class="sxs-lookup"><span data-stu-id="0d81e-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="0d81e-126">**6**</span><span class="sxs-lookup"><span data-stu-id="0d81e-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="0d81e-127">尚未啟動服務。</span><span class="sxs-lookup"><span data-stu-id="0d81e-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="0d81e-128">**7**</span><span class="sxs-lookup"><span data-stu-id="0d81e-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="0d81e-129">服務並未及時回應啟動要求。</span><span class="sxs-lookup"><span data-stu-id="0d81e-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="0d81e-130">**8**</span><span class="sxs-lookup"><span data-stu-id="0d81e-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="0d81e-131">啟動服務時發生未知的錯誤。</span><span class="sxs-lookup"><span data-stu-id="0d81e-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="0d81e-132">**9**</span><span class="sxs-lookup"><span data-stu-id="0d81e-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="0d81e-133">找不到服務可執行檔的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="0d81e-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="0d81e-134">**10**</span><span class="sxs-lookup"><span data-stu-id="0d81e-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="0d81e-135">服務已在執行中。</span><span class="sxs-lookup"><span data-stu-id="0d81e-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="0d81e-136">**11**</span><span class="sxs-lookup"><span data-stu-id="0d81e-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="0d81e-137">要加入新服務的資料庫已被鎖定。</span><span class="sxs-lookup"><span data-stu-id="0d81e-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="0d81e-138">**12**</span><span class="sxs-lookup"><span data-stu-id="0d81e-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="0d81e-139">這項服務所依賴的相依性已從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="0d81e-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="0d81e-140">**13**</span><span class="sxs-lookup"><span data-stu-id="0d81e-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="0d81e-141">服務在相依的服務中找不到所需的服務。</span><span class="sxs-lookup"><span data-stu-id="0d81e-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="0d81e-142">**14**</span><span class="sxs-lookup"><span data-stu-id="0d81e-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="0d81e-143">已經從系統中停用服務。</span><span class="sxs-lookup"><span data-stu-id="0d81e-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="0d81e-144">**15**</span><span class="sxs-lookup"><span data-stu-id="0d81e-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="0d81e-145">此服務未通過驗證，無法在系統上執行。</span><span class="sxs-lookup"><span data-stu-id="0d81e-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="0d81e-146">**16**</span><span class="sxs-lookup"><span data-stu-id="0d81e-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="0d81e-147">這項服務正在從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="0d81e-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="0d81e-148">**17**</span><span class="sxs-lookup"><span data-stu-id="0d81e-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="0d81e-149">服務沒有執行執行緒。</span><span class="sxs-lookup"><span data-stu-id="0d81e-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="0d81e-150">**達**</span><span class="sxs-lookup"><span data-stu-id="0d81e-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="0d81e-151">服務會在啟動時有迴圈相依性。</span><span class="sxs-lookup"><span data-stu-id="0d81e-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="0d81e-152">**診斷**</span><span class="sxs-lookup"><span data-stu-id="0d81e-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="0d81e-153">服務正在相同名稱下執行。</span><span class="sxs-lookup"><span data-stu-id="0d81e-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="0d81e-154">**20**</span><span class="sxs-lookup"><span data-stu-id="0d81e-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="0d81e-155">服務名稱包含不正確字元。</span><span class="sxs-lookup"><span data-stu-id="0d81e-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="0d81e-156">**21**</span><span class="sxs-lookup"><span data-stu-id="0d81e-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="0d81e-157">傳遞給服務的參數無效。</span><span class="sxs-lookup"><span data-stu-id="0d81e-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="0d81e-158">**22**</span><span class="sxs-lookup"><span data-stu-id="0d81e-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="0d81e-159">用來執行此服務的帳戶無效，或缺少執行服務的許可權。</span><span class="sxs-lookup"><span data-stu-id="0d81e-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="0d81e-160">**23**</span><span class="sxs-lookup"><span data-stu-id="0d81e-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="0d81e-161">服務存在於系統可使用之服務的資料庫中。</span><span class="sxs-lookup"><span data-stu-id="0d81e-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="0d81e-162">**24**</span><span class="sxs-lookup"><span data-stu-id="0d81e-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="0d81e-163">服務目前在系統中暫停。</span><span class="sxs-lookup"><span data-stu-id="0d81e-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d81e-164">備註</span><span class="sxs-lookup"><span data-stu-id="0d81e-164">Remarks</span></span>

<span data-ttu-id="0d81e-165">當您的組織變更時，您可能會決定從特定電腦移除特定的服務。</span><span class="sxs-lookup"><span data-stu-id="0d81e-165">As your organization changes, you might decide to remove certain services from certain computers.</span></span> <span data-ttu-id="0d81e-166">您可以使用 WMI 來移除內部和協力廠商服務，也可以使用 Sysocmgr.exe 來移除作業系統服務。</span><span class="sxs-lookup"><span data-stu-id="0d81e-166">In-house and third-party services can be removed by using WMI, while operating system services can be removed by using Sysocmgr.exe.</span></span>

<span data-ttu-id="0d81e-167">準備移除服務時，請記住下列資訊：</span><span class="sxs-lookup"><span data-stu-id="0d81e-167">When preparing to remove services, keep the following information in mind:</span></span>

-   <span data-ttu-id="0d81e-168">您必須先停止服務，才能將其移除。</span><span class="sxs-lookup"><span data-stu-id="0d81e-168">Services must be stopped before you remove them.</span></span> <span data-ttu-id="0d81e-169">當您發出 delete 命令時，如果服務正在執行，則會將服務標示為要刪除，但它會繼續執行，直到停止並關閉所有開啟的控制碼為止。</span><span class="sxs-lookup"><span data-stu-id="0d81e-169">If the service is running when you issue the delete command, the service is marked for deletion, but it continues to run until it stops and all open handles are closed.</span></span>

    <span data-ttu-id="0d81e-170">如果服務永遠不會停止，則永遠不會刪除該服務。</span><span class="sxs-lookup"><span data-stu-id="0d81e-170">If the service is never stopped, that service will never be deleted.</span></span>

-   <span data-ttu-id="0d81e-171">移除服務並不會移除服務的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="0d81e-171">Removing a service does not remove the service's executable file.</span></span>

    <span data-ttu-id="0d81e-172">使用 WMI 移除服務會刪除 HKEY \_ LOCAL \_ MACHINE \\ SYSTEM \\ CurrentControlSet \\ Services 下的相關登錄專案。</span><span class="sxs-lookup"><span data-stu-id="0d81e-172">Removing a service by using WMI deletes the related registry entries under HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services.</span></span> <span data-ttu-id="0d81e-173">如此一來，就不會再安裝服務，也無法透過 [服務] 嵌入式管理單元使用。</span><span class="sxs-lookup"><span data-stu-id="0d81e-173">As a result, the service is no longer installed and is not available through the Services snap-in.</span></span> <span data-ttu-id="0d81e-174">不過，WMI 不會刪除可執行檔，這表示您可以輕鬆地重新安裝服務。</span><span class="sxs-lookup"><span data-stu-id="0d81e-174">However, WMI does not delete the executable file, meaning you could easily reinstall the service.</span></span> <span data-ttu-id="0d81e-175">若要刪除可執行檔，您必須先取出路徑名稱，然後再刪除該檔案。</span><span class="sxs-lookup"><span data-stu-id="0d81e-175">To delete the executable file, you must retrieve the path name and then delete the file.</span></span>

-   <span data-ttu-id="0d81e-176">移除基底 Windows 2000 服務 (例如，使用 WMI 的 DHCP) 會刪除該服務的登錄專案，但不會從 [系統管理工具] 功能表移除快捷方式，或從 Windows 元件嚮導移除此服務。</span><span class="sxs-lookup"><span data-stu-id="0d81e-176">Removing a base Windows 2000 service (for example, DHCP) by using WMI deletes the registry entries for that service but does not remove the shortcut from the Administrative Tools menu or remove the service from the Windows Components Wizard.</span></span> <span data-ttu-id="0d81e-177">這可能會讓任何嘗試判斷電腦設定方式的人混淆。</span><span class="sxs-lookup"><span data-stu-id="0d81e-177">This can confuse anyone trying to determine how the computer has been configured.</span></span>

    <span data-ttu-id="0d81e-178">例如，如果您使用 WMI 腳本移除 DHCP 服務，[服務] 嵌入式管理單元中將不再列出 DHCP 服務。</span><span class="sxs-lookup"><span data-stu-id="0d81e-178">For example, if you remove the DHCP service by using a WMI script, the DHCP service is no longer listed in the Services snap-in.</span></span> <span data-ttu-id="0d81e-179">不過，DHCP 主控台的 nonfunctioning 快捷方式仍會保留在 [系統管理工具] 功能表中，如果您啟動 [Windows 元件嚮導]，則表示已安裝 DHCP 服務。</span><span class="sxs-lookup"><span data-stu-id="0d81e-179">However, a nonfunctioning shortcut to the DHCP console remains in the Administrative Tools menu, and if you start the Windows Component Wizard, it indicates that the DHCP service is installed.</span></span>

    <span data-ttu-id="0d81e-180">因此，您應該一律使用 Sysocmgr.exe 以程式設計方式移除 Windows 2000 服務。</span><span class="sxs-lookup"><span data-stu-id="0d81e-180">Because of this, you should always use Sysocmgr.exe to programmatically remove Windows 2000 services.</span></span>

## <a name="examples"></a><span data-ttu-id="0d81e-181">範例</span><span class="sxs-lookup"><span data-stu-id="0d81e-181">Examples</span></span>

<span data-ttu-id="0d81e-182">下列 VBScript 程式碼範例說明如何刪除服務。</span><span class="sxs-lookup"><span data-stu-id="0d81e-182">The following VBScript code sample describes how to delete a service.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colListOfServices = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Service WHERE Name = 'DbService'")
For Each objService in colListOfServices
 objService.StopService()
 objService.Delete()
Next
```



<span data-ttu-id="0d81e-183">下列 Perl 程式碼範例說明如何刪除服務。</span><span class="sxs-lookup"><span data-stu-id="0d81e-183">The following Perl code sample describes how to delete a service.</span></span>


```
use strict;
use Win32::OLE;

my ($Service, $ServiceSet) ;
eval {$ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='MyService'");};
unless($@)
{
 foreach $Service (in $ServiceSet)
 {
  my $RetVal = $Service->Delete();
  if ($RetVal == 0)  
  {
   print "Service deleted \n"; 
  }
  else  
  {
   print "Delete failed: %d", $RetVal;
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="0d81e-184">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d81e-184">Requirements</span></span>



| <span data-ttu-id="0d81e-185">需求</span><span class="sxs-lookup"><span data-stu-id="0d81e-185">Requirement</span></span> | <span data-ttu-id="0d81e-186">值</span><span class="sxs-lookup"><span data-stu-id="0d81e-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d81e-187">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0d81e-187">Minimum supported client</span></span><br/> | <span data-ttu-id="0d81e-188">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d81e-188">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0d81e-189">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0d81e-189">Minimum supported server</span></span><br/> | <span data-ttu-id="0d81e-190">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d81e-190">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0d81e-191">命名空間</span><span class="sxs-lookup"><span data-stu-id="0d81e-191">Namespace</span></span><br/>                | <span data-ttu-id="0d81e-192">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0d81e-192">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0d81e-193">MOF</span><span class="sxs-lookup"><span data-stu-id="0d81e-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d81e-194"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d81e-194"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d81e-195">DLL</span><span class="sxs-lookup"><span data-stu-id="0d81e-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d81e-196"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d81e-196"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d81e-197">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d81e-197">See also</span></span>

<dl> <dt>

<span data-ttu-id="0d81e-198">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0d81e-198">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0d81e-199">**Win32 \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="0d81e-199">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="0d81e-200">WMI 工作：服務</span><span class="sxs-lookup"><span data-stu-id="0d81e-200">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 


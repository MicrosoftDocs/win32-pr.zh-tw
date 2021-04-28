---
description: Win32_Service 類別的 GetSecurityDescriptor 方法 (CIMWin32 WMI 提供者) -傳回控制服務存取的安全描述項。
ms.assetid: 99c8346e-e8d6-4f3c-bbdc-437dcf852b2a
ms.tgt_platform: multiple
title: " (CIMWin32 WMI 提供者的 Win32_Service 類別的 GetSecurityDescriptor 方法) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.GetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 44c19f22cf57a811a7caebfbcc9bf4202c8d2ad7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096986"
---
# <a name="getsecuritydescriptor-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="593c9-103"> (CIMWin32 WMI 提供者的 Win32_Service 類別的 GetSecurityDescriptor 方法) </span><span class="sxs-lookup"><span data-stu-id="593c9-103">GetSecurityDescriptor method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="593c9-104">**GetSecurityDescriptor** 方法會傳回控制服務存取權的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="593c9-104">The **GetSecurityDescriptor** method returns the security descriptor that controls access to the service.</span></span> <span data-ttu-id="593c9-105">描述項會以 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)的實例傳回。</span><span class="sxs-lookup"><span data-stu-id="593c9-105">The descriptor is returned as an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span>

## <a name="syntax"></a><span data-ttu-id="593c9-106">語法</span><span class="sxs-lookup"><span data-stu-id="593c9-106">Syntax</span></span>


```mof
uint32 GetSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="593c9-107">參數</span><span class="sxs-lookup"><span data-stu-id="593c9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="593c9-108">*描述* \[ 項擴展\]</span><span class="sxs-lookup"><span data-stu-id="593c9-108">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="593c9-109">與服務相關聯的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="593c9-109">The security descriptor associated with the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="593c9-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="593c9-110">Return value</span></span>

<span data-ttu-id="593c9-111">傳回下列清單所列的其中一個值，或傳回不同的值來表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="593c9-111">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="593c9-112">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="593c9-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="593c9-113">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="593c9-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="593c9-114">「成功」</span><span class="sxs-lookup"><span data-stu-id="593c9-114">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="593c9-115">0</span><span class="sxs-lookup"><span data-stu-id="593c9-115">0</span></span>

<span data-ttu-id="593c9-116">要求已被接受。</span><span class="sxs-lookup"><span data-stu-id="593c9-116">The request was accepted.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="593c9-117">1</span><span class="sxs-lookup"><span data-stu-id="593c9-117">1</span></span>

<span data-ttu-id="593c9-118">不支援此要求。</span><span class="sxs-lookup"><span data-stu-id="593c9-118">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="593c9-119">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="593c9-119">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="593c9-120">2</span><span class="sxs-lookup"><span data-stu-id="593c9-120">2</span></span>

<span data-ttu-id="593c9-121">使用者沒有必要的存取權。</span><span class="sxs-lookup"><span data-stu-id="593c9-121">The user did not have the necessary access.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="593c9-122">3</span><span class="sxs-lookup"><span data-stu-id="593c9-122">3</span></span>

<span data-ttu-id="593c9-123">無法停止此服務，因為與它相依的其他服務正在執行中。</span><span class="sxs-lookup"><span data-stu-id="593c9-123">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="593c9-124">4</span><span class="sxs-lookup"><span data-stu-id="593c9-124">4</span></span>

<span data-ttu-id="593c9-125">要求的控制碼無效，或是服務不接受此控制碼。</span><span class="sxs-lookup"><span data-stu-id="593c9-125">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="593c9-126">5</span><span class="sxs-lookup"><span data-stu-id="593c9-126">5</span></span>

<span data-ttu-id="593c9-127">因為服務的狀態 ([**Win32 \_ BaseService**](win32-baseservice.md)，所以無法將要求的控制項程式碼傳送至服務。**State** 屬性) 等於0、1或2。</span><span class="sxs-lookup"><span data-stu-id="593c9-127">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="593c9-128">6</span><span class="sxs-lookup"><span data-stu-id="593c9-128">6</span></span>

<span data-ttu-id="593c9-129">尚未啟動服務。</span><span class="sxs-lookup"><span data-stu-id="593c9-129">The service has not been started.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="593c9-130">7</span><span class="sxs-lookup"><span data-stu-id="593c9-130">7</span></span>

<span data-ttu-id="593c9-131">服務並未及時回應啟動要求。</span><span class="sxs-lookup"><span data-stu-id="593c9-131">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="593c9-132">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="593c9-132">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="593c9-133">8</span><span class="sxs-lookup"><span data-stu-id="593c9-133">8</span></span>

<span data-ttu-id="593c9-134">啟動服務時發生未知的錯誤。</span><span class="sxs-lookup"><span data-stu-id="593c9-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="593c9-135">**缺少許可權**</span><span class="sxs-lookup"><span data-stu-id="593c9-135">**Privilege missing**</span></span>
</dt> <dd>

<span data-ttu-id="593c9-136">9</span><span class="sxs-lookup"><span data-stu-id="593c9-136">9</span></span>

<span data-ttu-id="593c9-137">找不到服務可執行檔的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="593c9-137">The directory path to the service executable file was not found.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="593c9-138">10</span><span class="sxs-lookup"><span data-stu-id="593c9-138">10</span></span>

<span data-ttu-id="593c9-139">服務已在執行中。</span><span class="sxs-lookup"><span data-stu-id="593c9-139">The service is already running.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="593c9-140">11</span><span class="sxs-lookup"><span data-stu-id="593c9-140">11</span></span>

<span data-ttu-id="593c9-141">要加入新服務的資料庫已被鎖定。</span><span class="sxs-lookup"><span data-stu-id="593c9-141">The database to add a new service is locked.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="593c9-142">12</span><span class="sxs-lookup"><span data-stu-id="593c9-142">12</span></span>

<span data-ttu-id="593c9-143">這項服務所依賴的相依性已從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="593c9-143">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="593c9-144">13</span><span class="sxs-lookup"><span data-stu-id="593c9-144">13</span></span>

<span data-ttu-id="593c9-145">服務在相依的服務中找不到所需的服務。</span><span class="sxs-lookup"><span data-stu-id="593c9-145">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="593c9-146">14</span><span class="sxs-lookup"><span data-stu-id="593c9-146">14</span></span>

<span data-ttu-id="593c9-147">已經從系統中停用服務。</span><span class="sxs-lookup"><span data-stu-id="593c9-147">The service has been disabled from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="593c9-148">15</span><span class="sxs-lookup"><span data-stu-id="593c9-148">15</span></span>

<span data-ttu-id="593c9-149">此服務未通過驗證，無法在系統上執行。</span><span class="sxs-lookup"><span data-stu-id="593c9-149">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="593c9-150">16</span><span class="sxs-lookup"><span data-stu-id="593c9-150">16</span></span>

<span data-ttu-id="593c9-151">這項服務正在從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="593c9-151">This service is being removed from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="593c9-152">17</span><span class="sxs-lookup"><span data-stu-id="593c9-152">17</span></span>

<span data-ttu-id="593c9-153">服務沒有執行執行緒。</span><span class="sxs-lookup"><span data-stu-id="593c9-153">The service has no execution thread.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="593c9-154">18</span><span class="sxs-lookup"><span data-stu-id="593c9-154">18</span></span>

<span data-ttu-id="593c9-155">服務會在啟動時有迴圈相依性。</span><span class="sxs-lookup"><span data-stu-id="593c9-155">The service has circular dependencies when it starts.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="593c9-156">19</span><span class="sxs-lookup"><span data-stu-id="593c9-156">19</span></span>

<span data-ttu-id="593c9-157">服務正在相同名稱下執行。</span><span class="sxs-lookup"><span data-stu-id="593c9-157">A service is running under the same name.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="593c9-158">20</span><span class="sxs-lookup"><span data-stu-id="593c9-158">20</span></span>

<span data-ttu-id="593c9-159">服務名稱包含不正確字元。</span><span class="sxs-lookup"><span data-stu-id="593c9-159">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="593c9-160">**參數不正確**</span><span class="sxs-lookup"><span data-stu-id="593c9-160">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="593c9-161">21</span><span class="sxs-lookup"><span data-stu-id="593c9-161">21</span></span>

<span data-ttu-id="593c9-162">傳遞給服務的參數無效。</span><span class="sxs-lookup"><span data-stu-id="593c9-162">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="593c9-163">22</span><span class="sxs-lookup"><span data-stu-id="593c9-163">22</span></span>

<span data-ttu-id="593c9-164">用來執行此服務的帳戶無效，或缺少執行服務的許可權。</span><span class="sxs-lookup"><span data-stu-id="593c9-164">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="593c9-165">23</span><span class="sxs-lookup"><span data-stu-id="593c9-165">23</span></span>

<span data-ttu-id="593c9-166">服務存在於系統可使用之服務的資料庫中。</span><span class="sxs-lookup"><span data-stu-id="593c9-166">The service exists in the database of services available from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="593c9-167">24</span><span class="sxs-lookup"><span data-stu-id="593c9-167">24</span></span>

<span data-ttu-id="593c9-168">服務目前在系統中暫停。</span><span class="sxs-lookup"><span data-stu-id="593c9-168">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="593c9-169">**其他**</span><span class="sxs-lookup"><span data-stu-id="593c9-169">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="593c9-170">22 4294967295</span><span class="sxs-lookup"><span data-stu-id="593c9-170">22 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="593c9-171">備註</span><span class="sxs-lookup"><span data-stu-id="593c9-171">Remarks</span></span>

<span data-ttu-id="593c9-172">[**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)實例代表 [**安全 \_ 描述項 \_ 控制項**](/windows/desktop/SecAuthZ/security-descriptor-control)資料類型，並包含 (DACL) 的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly)，以及 (SACL) 的 [*系統存取控制清單*](/windows/desktop/SecGloss/s-gly)。</span><span class="sxs-lookup"><span data-stu-id="593c9-172">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="593c9-173">如需詳細資訊，請參閱 [存取控制清單](/windows/desktop/SecAuthZ/access-control-lists)。</span><span class="sxs-lookup"><span data-stu-id="593c9-173">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="593c9-174">如果未在取得安全描述項時授與或啟用 **SeSecurityPrivilege** ，則只會傳回傳回的安全描述項中的 DACL。</span><span class="sxs-lookup"><span data-stu-id="593c9-174">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="593c9-175">如需詳細資訊，請參閱 [**許可權常數**](/windows/desktop/WmiSdk/privilege-constants) 和 [執行特殊許可權作業](/windows/desktop/WmiSdk/executing-privileged-operations)。</span><span class="sxs-lookup"><span data-stu-id="593c9-175">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="593c9-176">範例</span><span class="sxs-lookup"><span data-stu-id="593c9-176">Examples</span></span>

<span data-ttu-id="593c9-177">在 VBScript 中取出安全描述項時，請務必以系統管理員身分執行，並以系統管理員身分執行，如下列程式碼片段所示。</span><span class="sxs-lookup"><span data-stu-id="593c9-177">When retrieving a security descriptor in VBScript, be sure to "Security" and run as as Admin, as shown in the following code snippet.</span></span> <span data-ttu-id="593c9-178">否則，您的程式碼可能會擲回許可權錯誤。</span><span class="sxs-lookup"><span data-stu-id="593c9-178">Otherwise, your code may throw a permissions error.</span></span>


```VB
Set objWMIService = GetObject("winmgmts:" _
  & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")
```



<span data-ttu-id="593c9-179">同樣地，在 VB.NET 中，請務必設定 "EnablePrivileges = True"，並以系統管理員身分執行應用程式。</span><span class="sxs-lookup"><span data-stu-id="593c9-179">Similarly, in VB.NET, be sure to set "EnablePrivileges = True" and run the Application as Admin.</span></span>


```VB
Scope = New ManagementScope([String].Format("\\{0}\root\CIMV2", ComputerName), Nothing)
Scope.Options.EnablePrivileges = True
```



## <a name="requirements"></a><span data-ttu-id="593c9-180">規格需求</span><span class="sxs-lookup"><span data-stu-id="593c9-180">Requirements</span></span>



| <span data-ttu-id="593c9-181">需求</span><span class="sxs-lookup"><span data-stu-id="593c9-181">Requirement</span></span> | <span data-ttu-id="593c9-182">值</span><span class="sxs-lookup"><span data-stu-id="593c9-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="593c9-183">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="593c9-183">Minimum supported client</span></span><br/> | <span data-ttu-id="593c9-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="593c9-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="593c9-185">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="593c9-185">Minimum supported server</span></span><br/> | <span data-ttu-id="593c9-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="593c9-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="593c9-187">命名空間</span><span class="sxs-lookup"><span data-stu-id="593c9-187">Namespace</span></span><br/>                | <span data-ttu-id="593c9-188">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="593c9-188">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="593c9-189">MOF</span><span class="sxs-lookup"><span data-stu-id="593c9-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="593c9-190"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="593c9-190"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="593c9-191">DLL</span><span class="sxs-lookup"><span data-stu-id="593c9-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="593c9-192"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="593c9-192"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="593c9-193">另請參閱</span><span class="sxs-lookup"><span data-stu-id="593c9-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="593c9-194">**Win32 \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="593c9-194">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="593c9-195">**許可權常數**</span><span class="sxs-lookup"><span data-stu-id="593c9-195">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="593c9-196">WMI 安全描述項物件</span><span class="sxs-lookup"><span data-stu-id="593c9-196">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="593c9-197">變更安全物件的存取安全性</span><span class="sxs-lookup"><span data-stu-id="593c9-197">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[<span data-ttu-id="593c9-198">使用者帳戶控制和 WMI</span><span class="sxs-lookup"><span data-stu-id="593c9-198">User Account Control and WMI</span></span>](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 


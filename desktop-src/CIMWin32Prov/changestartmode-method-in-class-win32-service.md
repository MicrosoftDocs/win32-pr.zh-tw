---
description: 修改 Win32 服務的啟動模式 \_ 。
ms.assetid: 4fd6a1eb-d2e0-4172-843d-24ae89c5bfcf
ms.tgt_platform: multiple
title: " (CIMWin32 WMI 提供者的 Win32_Service 類別的 ChangeStartMode 方法) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.ChangeStartMode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 06a4692996354614a685471f98b0243fc1091433
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025905"
---
# <a name="changestartmode-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="17313-103"> (CIMWin32 WMI 提供者的 Win32_Service 類別的 ChangeStartMode 方法) </span><span class="sxs-lookup"><span data-stu-id="17313-103">ChangeStartMode method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="17313-104">**ChangeStartMode** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會修改 [**Win32 \_ 服務**](win32-service.md)的啟動模式。</span><span class="sxs-lookup"><span data-stu-id="17313-104">The **ChangeStartMode** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies the start mode of a [**Win32\_Service**](win32-service.md).</span></span>

<span data-ttu-id="17313-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="17313-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="17313-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="17313-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="17313-107">語法</span><span class="sxs-lookup"><span data-stu-id="17313-107">Syntax</span></span>


```mof
uint32 ChangeStartMode(
  [in] string StartMode = Auto Start
);
```



## <a name="parameters"></a><span data-ttu-id="17313-108">參數</span><span class="sxs-lookup"><span data-stu-id="17313-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17313-109">*StartMode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="17313-109">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17313-110">Windows 基底服務的啟動模式。</span><span class="sxs-lookup"><span data-stu-id="17313-110">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="17313-111"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**開機開始 ( 「開機」** ) </span><span class="sxs-lookup"><span data-stu-id="17313-111"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="17313-112">作業系統載入器啟動的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="17313-112">Device driver started by the operating system loader.</span></span> <span data-ttu-id="17313-113">這個值只適用於驅動程式服務。</span><span class="sxs-lookup"><span data-stu-id="17313-113">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="17313-114"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ( "system" ) </span><span class="sxs-lookup"><span data-stu-id="17313-114"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="17313-115">由作業系統初始化程式啟動的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="17313-115">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="17313-116">這個值只適用於驅動程式服務。</span><span class="sxs-lookup"><span data-stu-id="17313-116">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="17313-117"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**自動啟動 ( 「自動」** ) </span><span class="sxs-lookup"><span data-stu-id="17313-117"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start** ("Automatic")</span></span>


</dt> <dd>

<span data-ttu-id="17313-118">要由服務控制管理員在系統啟動期間自動啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="17313-118">Service to be started automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="17313-119"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**需求開始 ( 「手動」** ) </span><span class="sxs-lookup"><span data-stu-id="17313-119"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="17313-120">當進程呼叫 [**StartService**](startservice-method-in-class-win32-service.md) 方法時，服務控制管理員要啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="17313-120">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-service.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="17313-121"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** ( [已停用] ) </span><span class="sxs-lookup"><span data-stu-id="17313-121"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="17313-122">無法再啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="17313-122">Service that can no longer be started.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17313-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="17313-123">Return value</span></span>

<span data-ttu-id="17313-124">傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="17313-124">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="17313-125">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="17313-125">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="17313-126">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="17313-126">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="17313-127">「成功」</span><span class="sxs-lookup"><span data-stu-id="17313-127">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="17313-128">0</span><span class="sxs-lookup"><span data-stu-id="17313-128">0</span></span>

<span data-ttu-id="17313-129">要求已被接受。</span><span class="sxs-lookup"><span data-stu-id="17313-129">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="17313-130">**不支援**</span><span class="sxs-lookup"><span data-stu-id="17313-130">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="17313-131">1</span><span class="sxs-lookup"><span data-stu-id="17313-131">1</span></span>

<span data-ttu-id="17313-132">不支援此要求。</span><span class="sxs-lookup"><span data-stu-id="17313-132">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="17313-133">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="17313-133">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="17313-134">2</span><span class="sxs-lookup"><span data-stu-id="17313-134">2</span></span>

<span data-ttu-id="17313-135">使用者沒有必要的存取權。</span><span class="sxs-lookup"><span data-stu-id="17313-135">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="17313-136">**相依服務正在執行**</span><span class="sxs-lookup"><span data-stu-id="17313-136">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="17313-137">3</span><span class="sxs-lookup"><span data-stu-id="17313-137">3</span></span>

<span data-ttu-id="17313-138">無法停止此服務，因為與它相依的其他服務正在執行中。</span><span class="sxs-lookup"><span data-stu-id="17313-138">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="17313-139">**不正確服務控制**</span><span class="sxs-lookup"><span data-stu-id="17313-139">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="17313-140">4</span><span class="sxs-lookup"><span data-stu-id="17313-140">4</span></span>

<span data-ttu-id="17313-141">要求的控制碼無效，或是服務不接受此控制碼。</span><span class="sxs-lookup"><span data-stu-id="17313-141">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="17313-142">**服務無法接受控制權**</span><span class="sxs-lookup"><span data-stu-id="17313-142">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="17313-143">5</span><span class="sxs-lookup"><span data-stu-id="17313-143">5</span></span>

<span data-ttu-id="17313-144">因為服務的狀態 ([**Win32 \_ BaseService**](win32-baseservice.md)，所以無法將要求的控制項程式碼傳送至服務。**State** 屬性) 等於0、1或2。</span><span class="sxs-lookup"><span data-stu-id="17313-144">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="17313-145">**服務非使用中**</span><span class="sxs-lookup"><span data-stu-id="17313-145">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="17313-146">6</span><span class="sxs-lookup"><span data-stu-id="17313-146">6</span></span>

<span data-ttu-id="17313-147">尚未啟動服務。</span><span class="sxs-lookup"><span data-stu-id="17313-147">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="17313-148">**服務要求超時**</span><span class="sxs-lookup"><span data-stu-id="17313-148">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="17313-149">7</span><span class="sxs-lookup"><span data-stu-id="17313-149">7</span></span>

<span data-ttu-id="17313-150">服務並未及時回應啟動要求。</span><span class="sxs-lookup"><span data-stu-id="17313-150">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="17313-151">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="17313-151">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="17313-152">8</span><span class="sxs-lookup"><span data-stu-id="17313-152">8</span></span>

<span data-ttu-id="17313-153">啟動服務時發生未知的錯誤。</span><span class="sxs-lookup"><span data-stu-id="17313-153">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="17313-154">**找不到路徑**</span><span class="sxs-lookup"><span data-stu-id="17313-154">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="17313-155">9</span><span class="sxs-lookup"><span data-stu-id="17313-155">9</span></span>

<span data-ttu-id="17313-156">找不到服務可執行檔的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="17313-156">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="17313-157">**服務已在執行**</span><span class="sxs-lookup"><span data-stu-id="17313-157">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="17313-158">10</span><span class="sxs-lookup"><span data-stu-id="17313-158">10</span></span>

<span data-ttu-id="17313-159">服務已在執行中。</span><span class="sxs-lookup"><span data-stu-id="17313-159">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="17313-160">**服務資料庫已鎖定**</span><span class="sxs-lookup"><span data-stu-id="17313-160">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="17313-161">11</span><span class="sxs-lookup"><span data-stu-id="17313-161">11</span></span>

<span data-ttu-id="17313-162">要加入新服務的資料庫已被鎖定。</span><span class="sxs-lookup"><span data-stu-id="17313-162">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="17313-163">**服務相依性已刪除**</span><span class="sxs-lookup"><span data-stu-id="17313-163">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="17313-164">12</span><span class="sxs-lookup"><span data-stu-id="17313-164">12</span></span>

<span data-ttu-id="17313-165">這項服務所依賴的相依性已從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="17313-165">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="17313-166">**服務相依性失敗**</span><span class="sxs-lookup"><span data-stu-id="17313-166">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="17313-167">13</span><span class="sxs-lookup"><span data-stu-id="17313-167">13</span></span>

<span data-ttu-id="17313-168">服務在相依的服務中找不到所需的服務。</span><span class="sxs-lookup"><span data-stu-id="17313-168">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="17313-169">**服務已停用**</span><span class="sxs-lookup"><span data-stu-id="17313-169">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="17313-170">14</span><span class="sxs-lookup"><span data-stu-id="17313-170">14</span></span>

<span data-ttu-id="17313-171">已經從系統中停用服務。</span><span class="sxs-lookup"><span data-stu-id="17313-171">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="17313-172">**服務登入失敗**</span><span class="sxs-lookup"><span data-stu-id="17313-172">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="17313-173">15</span><span class="sxs-lookup"><span data-stu-id="17313-173">15</span></span>

<span data-ttu-id="17313-174">此服務未通過驗證，無法在系統上執行。</span><span class="sxs-lookup"><span data-stu-id="17313-174">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="17313-175">**已標示為要刪除的服務**</span><span class="sxs-lookup"><span data-stu-id="17313-175">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="17313-176">16</span><span class="sxs-lookup"><span data-stu-id="17313-176">16</span></span>

<span data-ttu-id="17313-177">這項服務正在從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="17313-177">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="17313-178">**服務無線程**</span><span class="sxs-lookup"><span data-stu-id="17313-178">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="17313-179">17</span><span class="sxs-lookup"><span data-stu-id="17313-179">17</span></span>

<span data-ttu-id="17313-180">服務沒有執行執行緒。</span><span class="sxs-lookup"><span data-stu-id="17313-180">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="17313-181">**狀態迴圈相依性**</span><span class="sxs-lookup"><span data-stu-id="17313-181">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="17313-182">18</span><span class="sxs-lookup"><span data-stu-id="17313-182">18</span></span>

<span data-ttu-id="17313-183">服務會在啟動時有迴圈相依性。</span><span class="sxs-lookup"><span data-stu-id="17313-183">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="17313-184">**狀態重複名稱**</span><span class="sxs-lookup"><span data-stu-id="17313-184">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="17313-185">19</span><span class="sxs-lookup"><span data-stu-id="17313-185">19</span></span>

<span data-ttu-id="17313-186">服務正在相同名稱下執行。</span><span class="sxs-lookup"><span data-stu-id="17313-186">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="17313-187">**狀態不正確名稱**</span><span class="sxs-lookup"><span data-stu-id="17313-187">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="17313-188">20</span><span class="sxs-lookup"><span data-stu-id="17313-188">20</span></span>

<span data-ttu-id="17313-189">服務名稱包含不正確字元。</span><span class="sxs-lookup"><span data-stu-id="17313-189">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="17313-190">**狀態不正確參數**</span><span class="sxs-lookup"><span data-stu-id="17313-190">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="17313-191">21</span><span class="sxs-lookup"><span data-stu-id="17313-191">21</span></span>

<span data-ttu-id="17313-192">傳遞給服務的參數無效。</span><span class="sxs-lookup"><span data-stu-id="17313-192">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="17313-193">**狀態不正確服務帳戶**</span><span class="sxs-lookup"><span data-stu-id="17313-193">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="17313-194">22</span><span class="sxs-lookup"><span data-stu-id="17313-194">22</span></span>

<span data-ttu-id="17313-195">用來執行此服務的帳戶無效，或缺少執行服務的許可權。</span><span class="sxs-lookup"><span data-stu-id="17313-195">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="17313-196">**狀態服務存在**</span><span class="sxs-lookup"><span data-stu-id="17313-196">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="17313-197">23</span><span class="sxs-lookup"><span data-stu-id="17313-197">23</span></span>

<span data-ttu-id="17313-198">服務存在於系統可使用之服務的資料庫中。</span><span class="sxs-lookup"><span data-stu-id="17313-198">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="17313-199">**服務已暫停**</span><span class="sxs-lookup"><span data-stu-id="17313-199">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="17313-200">24</span><span class="sxs-lookup"><span data-stu-id="17313-200">24</span></span>

<span data-ttu-id="17313-201">服務目前在系統中暫停。</span><span class="sxs-lookup"><span data-stu-id="17313-201">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="17313-202">**其他**</span><span class="sxs-lookup"><span data-stu-id="17313-202">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="17313-203">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="17313-203">25 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="17313-204">範例</span><span class="sxs-lookup"><span data-stu-id="17313-204">Examples</span></span>

<span data-ttu-id="17313-205">從 TechNet 資源庫提取的服務 PowerShell 範例的下列 [變更 StartMode](https://Gallery.TechNet.Microsoft.Com/6d0f06ed-f840-4228-ad2d-e16ebe6a3aed) 會變更服務的啟動模式。</span><span class="sxs-lookup"><span data-stu-id="17313-205">The following [Change StartMode of a Service](https://Gallery.TechNet.Microsoft.Com/6d0f06ed-f840-4228-ad2d-e16ebe6a3aed) PowerShell sample, pulled from TechNet Gallery, changes the start mode of a service.</span></span>


```PowerShell
$wmi = get-wmiobject -class win32_service -namespace root\cimv2 -computername lisbon | 
where-object { $_.name -eq 'bits' } 
 
$rtn = $wmi.changestartmode("manual") 
if($rtn.returnvalue -eq 0) { "success" } 
ELSE 
  { " $($rtn.returnvalue) was reported" }
```



## <a name="requirements"></a><span data-ttu-id="17313-206">規格需求</span><span class="sxs-lookup"><span data-stu-id="17313-206">Requirements</span></span>



| <span data-ttu-id="17313-207">需求</span><span class="sxs-lookup"><span data-stu-id="17313-207">Requirement</span></span> | <span data-ttu-id="17313-208">值</span><span class="sxs-lookup"><span data-stu-id="17313-208">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17313-209">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="17313-209">Minimum supported client</span></span><br/> | <span data-ttu-id="17313-210">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="17313-210">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="17313-211">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="17313-211">Minimum supported server</span></span><br/> | <span data-ttu-id="17313-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17313-212">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="17313-213">命名空間</span><span class="sxs-lookup"><span data-stu-id="17313-213">Namespace</span></span><br/>                | <span data-ttu-id="17313-214">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="17313-214">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="17313-215">MOF</span><span class="sxs-lookup"><span data-stu-id="17313-215">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17313-216"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="17313-216"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="17313-217">DLL</span><span class="sxs-lookup"><span data-stu-id="17313-217">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17313-218"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17313-218"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17313-219">另請參閱</span><span class="sxs-lookup"><span data-stu-id="17313-219">See also</span></span>

<dl> <dt>

<span data-ttu-id="17313-220">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="17313-220">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="17313-221">**Win32 \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="17313-221">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="17313-222">WMI 工作：服務</span><span class="sxs-lookup"><span data-stu-id="17313-222">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 


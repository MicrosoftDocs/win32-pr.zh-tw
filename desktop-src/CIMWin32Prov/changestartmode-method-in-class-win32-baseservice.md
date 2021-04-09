---
description: 修改衍生自 Win32 BaseService 之服務物件的啟動模式 \_ 。
ms.assetid: 33040632-6c04-4084-af09-8e1b8bc29090
ms.tgt_platform: multiple
title: Win32_BaseService 類別的 ChangeStartMode 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.ChangeStartMode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9877300a2135b7082677193696cd2d11811ab3dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110625"
---
# <a name="changestartmode-method-of-the-win32_baseservice-class"></a><span data-ttu-id="3b915-103">Win32 BaseService 類別的 ChangeStartMode 方法 \_</span><span class="sxs-lookup"><span data-stu-id="3b915-103">ChangeStartMode method of the Win32\_BaseService class</span></span>

<span data-ttu-id="3b915-104">**ChangeStartMode** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會修改衍生自 [**Win32 \_ BaseService**](win32-baseservice.md)之服務物件的啟動模式。</span><span class="sxs-lookup"><span data-stu-id="3b915-104">The **ChangeStartMode** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies the start mode of a service object derived from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<span data-ttu-id="3b915-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="3b915-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3b915-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="3b915-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3b915-107">語法</span><span class="sxs-lookup"><span data-stu-id="3b915-107">Syntax</span></span>


```mof
uint32 ChangeStartMode(
  [in] string StartMode = Auto Start
);
```



## <a name="parameters"></a><span data-ttu-id="3b915-108">參數</span><span class="sxs-lookup"><span data-stu-id="3b915-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b915-109">*StartMode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3b915-109">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b915-110">Windows 基底服務的啟動模式。</span><span class="sxs-lookup"><span data-stu-id="3b915-110">Start mode of the Windows base service.</span></span> <span data-ttu-id="3b915-111">預設值為「自動」。</span><span class="sxs-lookup"><span data-stu-id="3b915-111">The default is "Automatic".</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="3b915-112"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**開機開始 ( 「開機」** ) </span><span class="sxs-lookup"><span data-stu-id="3b915-112"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="3b915-113">作業系統載入器啟動的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="3b915-113">Device driver started by the operating system loader.</span></span> <span data-ttu-id="3b915-114">這個值只適用於驅動程式服務。</span><span class="sxs-lookup"><span data-stu-id="3b915-114">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span data-ttu-id="3b915-115"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**系統啟動** ( "system" ) </span><span class="sxs-lookup"><span data-stu-id="3b915-115"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**System Start** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="3b915-116">由作業系統初始化程式啟動的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="3b915-116">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="3b915-117">這個值只適用於驅動程式服務。</span><span class="sxs-lookup"><span data-stu-id="3b915-117">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="3b915-118"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**自動啟動 ( 「自動」** ) </span><span class="sxs-lookup"><span data-stu-id="3b915-118"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start** ("Automatic")</span></span>


</dt> <dd>

<span data-ttu-id="3b915-119">要由服務控制管理員在系統啟動期間自動啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="3b915-119">Service to be started automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="3b915-120"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**需求開始 ( 「手動」** ) </span><span class="sxs-lookup"><span data-stu-id="3b915-120"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="3b915-121">當進程呼叫 [**StartService**](startservice-method-in-class-win32-baseservice.md) 方法時，服務控制管理員要啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="3b915-121">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-baseservice.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="3b915-122"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** ( [已停用] ) </span><span class="sxs-lookup"><span data-stu-id="3b915-122"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="3b915-123">服務已停用。</span><span class="sxs-lookup"><span data-stu-id="3b915-123">Service is disabled.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b915-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="3b915-124">Return value</span></span>

<span data-ttu-id="3b915-125">傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="3b915-125">Returns one of the values listed in the following list or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="3b915-126">「成功」</span><span class="sxs-lookup"><span data-stu-id="3b915-126">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="3b915-127">0</span><span class="sxs-lookup"><span data-stu-id="3b915-127">0</span></span>

<span data-ttu-id="3b915-128">要求已被接受。</span><span class="sxs-lookup"><span data-stu-id="3b915-128">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="3b915-129">**不支援**</span><span class="sxs-lookup"><span data-stu-id="3b915-129">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="3b915-130">1</span><span class="sxs-lookup"><span data-stu-id="3b915-130">1</span></span>

<span data-ttu-id="3b915-131">不支援此要求。</span><span class="sxs-lookup"><span data-stu-id="3b915-131">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="3b915-132">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="3b915-132">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="3b915-133">2</span><span class="sxs-lookup"><span data-stu-id="3b915-133">2</span></span>

<span data-ttu-id="3b915-134">使用者沒有必要的存取權。</span><span class="sxs-lookup"><span data-stu-id="3b915-134">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="3b915-135">**相依服務正在執行**</span><span class="sxs-lookup"><span data-stu-id="3b915-135">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="3b915-136">3</span><span class="sxs-lookup"><span data-stu-id="3b915-136">3</span></span>

<span data-ttu-id="3b915-137">無法停止此服務，因為與它相依的其他服務正在執行中。</span><span class="sxs-lookup"><span data-stu-id="3b915-137">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="3b915-138">**不正確服務控制**</span><span class="sxs-lookup"><span data-stu-id="3b915-138">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="3b915-139">4</span><span class="sxs-lookup"><span data-stu-id="3b915-139">4</span></span>

<span data-ttu-id="3b915-140">要求的控制碼無效，或是服務不接受此控制碼。</span><span class="sxs-lookup"><span data-stu-id="3b915-140">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="3b915-141">**服務無法接受控制權**</span><span class="sxs-lookup"><span data-stu-id="3b915-141">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="3b915-142">5</span><span class="sxs-lookup"><span data-stu-id="3b915-142">5</span></span>

<span data-ttu-id="3b915-143">要求的控制項程式碼無法傳送至服務，因為服務的狀態 ([**Win32 \_ BaseService**](win32-baseservice.md)[**state**](win32-baseservice.md) 屬性) 等於0、1或2。</span><span class="sxs-lookup"><span data-stu-id="3b915-143">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md)[**State**](win32-baseservice.md) property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="3b915-144">**服務非使用中**</span><span class="sxs-lookup"><span data-stu-id="3b915-144">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="3b915-145">6</span><span class="sxs-lookup"><span data-stu-id="3b915-145">6</span></span>

<span data-ttu-id="3b915-146">尚未啟動服務。</span><span class="sxs-lookup"><span data-stu-id="3b915-146">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="3b915-147">**服務要求超時**</span><span class="sxs-lookup"><span data-stu-id="3b915-147">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="3b915-148">7</span><span class="sxs-lookup"><span data-stu-id="3b915-148">7</span></span>

<span data-ttu-id="3b915-149">服務並未及時回應啟動要求。</span><span class="sxs-lookup"><span data-stu-id="3b915-149">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="3b915-150">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="3b915-150">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="3b915-151">8</span><span class="sxs-lookup"><span data-stu-id="3b915-151">8</span></span>

<span data-ttu-id="3b915-152">互動式進程。</span><span class="sxs-lookup"><span data-stu-id="3b915-152">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="3b915-153">**找不到路徑**</span><span class="sxs-lookup"><span data-stu-id="3b915-153">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="3b915-154">9</span><span class="sxs-lookup"><span data-stu-id="3b915-154">9</span></span>

<span data-ttu-id="3b915-155">找不到服務可執行檔的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="3b915-155">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="3b915-156">**服務已在執行**</span><span class="sxs-lookup"><span data-stu-id="3b915-156">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="3b915-157">10</span><span class="sxs-lookup"><span data-stu-id="3b915-157">10</span></span>

<span data-ttu-id="3b915-158">服務已在執行中。</span><span class="sxs-lookup"><span data-stu-id="3b915-158">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="3b915-159">**服務資料庫已鎖定**</span><span class="sxs-lookup"><span data-stu-id="3b915-159">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="3b915-160">11</span><span class="sxs-lookup"><span data-stu-id="3b915-160">11</span></span>

<span data-ttu-id="3b915-161">要加入新服務的資料庫已被鎖定。</span><span class="sxs-lookup"><span data-stu-id="3b915-161">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="3b915-162">**服務相依性已刪除**</span><span class="sxs-lookup"><span data-stu-id="3b915-162">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="3b915-163">12</span><span class="sxs-lookup"><span data-stu-id="3b915-163">12</span></span>

<span data-ttu-id="3b915-164">已經從系統中移除這個服務所依賴的相依性。</span><span class="sxs-lookup"><span data-stu-id="3b915-164">A dependency on which this service relies has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3b915-165">**服務相依性失敗**</span><span class="sxs-lookup"><span data-stu-id="3b915-165">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="3b915-166">13</span><span class="sxs-lookup"><span data-stu-id="3b915-166">13</span></span>

<span data-ttu-id="3b915-167">服務在相依的服務中找不到所需的服務。</span><span class="sxs-lookup"><span data-stu-id="3b915-167">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="3b915-168">**服務已停用**</span><span class="sxs-lookup"><span data-stu-id="3b915-168">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="3b915-169">14</span><span class="sxs-lookup"><span data-stu-id="3b915-169">14</span></span>

<span data-ttu-id="3b915-170">已經從系統中停用服務。</span><span class="sxs-lookup"><span data-stu-id="3b915-170">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3b915-171">**服務登入失敗**</span><span class="sxs-lookup"><span data-stu-id="3b915-171">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="3b915-172">15</span><span class="sxs-lookup"><span data-stu-id="3b915-172">15</span></span>

<span data-ttu-id="3b915-173">此服務未通過驗證，無法在系統上執行。</span><span class="sxs-lookup"><span data-stu-id="3b915-173">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="3b915-174">**已標示為要刪除的服務**</span><span class="sxs-lookup"><span data-stu-id="3b915-174">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="3b915-175">16</span><span class="sxs-lookup"><span data-stu-id="3b915-175">16</span></span>

<span data-ttu-id="3b915-176">這項服務正在從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="3b915-176">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3b915-177">**服務無線程**</span><span class="sxs-lookup"><span data-stu-id="3b915-177">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="3b915-178">17</span><span class="sxs-lookup"><span data-stu-id="3b915-178">17</span></span>

<span data-ttu-id="3b915-179">服務沒有執行緒。</span><span class="sxs-lookup"><span data-stu-id="3b915-179">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="3b915-180">**狀態迴圈相依性**</span><span class="sxs-lookup"><span data-stu-id="3b915-180">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="3b915-181">18</span><span class="sxs-lookup"><span data-stu-id="3b915-181">18</span></span>

<span data-ttu-id="3b915-182">啟動服務時有循環的相依性。</span><span class="sxs-lookup"><span data-stu-id="3b915-182">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="3b915-183">**狀態重複名稱**</span><span class="sxs-lookup"><span data-stu-id="3b915-183">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="3b915-184">19</span><span class="sxs-lookup"><span data-stu-id="3b915-184">19</span></span>

<span data-ttu-id="3b915-185">有一個服務在相同名稱下執行。</span><span class="sxs-lookup"><span data-stu-id="3b915-185">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="3b915-186">**狀態不正確名稱**</span><span class="sxs-lookup"><span data-stu-id="3b915-186">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="3b915-187">20</span><span class="sxs-lookup"><span data-stu-id="3b915-187">20</span></span>

<span data-ttu-id="3b915-188">服務名稱中有不正確字元。</span><span class="sxs-lookup"><span data-stu-id="3b915-188">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="3b915-189">**狀態不正確參數**</span><span class="sxs-lookup"><span data-stu-id="3b915-189">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="3b915-190">21</span><span class="sxs-lookup"><span data-stu-id="3b915-190">21</span></span>

<span data-ttu-id="3b915-191">傳遞給服務的參數無效。</span><span class="sxs-lookup"><span data-stu-id="3b915-191">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="3b915-192">**狀態不正確服務帳戶**</span><span class="sxs-lookup"><span data-stu-id="3b915-192">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="3b915-193">22</span><span class="sxs-lookup"><span data-stu-id="3b915-193">22</span></span>

<span data-ttu-id="3b915-194">用來執行此服務的帳戶無效，或缺少執行服務的許可權。</span><span class="sxs-lookup"><span data-stu-id="3b915-194">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="3b915-195">**狀態服務存在**</span><span class="sxs-lookup"><span data-stu-id="3b915-195">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="3b915-196">23</span><span class="sxs-lookup"><span data-stu-id="3b915-196">23</span></span>

<span data-ttu-id="3b915-197">服務存在於系統可使用之服務的資料庫中。</span><span class="sxs-lookup"><span data-stu-id="3b915-197">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3b915-198">**服務已暫停**</span><span class="sxs-lookup"><span data-stu-id="3b915-198">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="3b915-199">24</span><span class="sxs-lookup"><span data-stu-id="3b915-199">24</span></span>

<span data-ttu-id="3b915-200">服務目前在系統中暫停。</span><span class="sxs-lookup"><span data-stu-id="3b915-200">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="3b915-201">**其他**</span><span class="sxs-lookup"><span data-stu-id="3b915-201">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="3b915-202">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="3b915-202">25 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3b915-203">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b915-203">Requirements</span></span>



| <span data-ttu-id="3b915-204">需求</span><span class="sxs-lookup"><span data-stu-id="3b915-204">Requirement</span></span> | <span data-ttu-id="3b915-205">值</span><span class="sxs-lookup"><span data-stu-id="3b915-205">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b915-206">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3b915-206">Minimum supported client</span></span><br/> | <span data-ttu-id="3b915-207">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3b915-207">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3b915-208">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3b915-208">Minimum supported server</span></span><br/> | <span data-ttu-id="3b915-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3b915-209">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3b915-210">命名空間</span><span class="sxs-lookup"><span data-stu-id="3b915-210">Namespace</span></span><br/>                | <span data-ttu-id="3b915-211">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3b915-211">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3b915-212">MOF</span><span class="sxs-lookup"><span data-stu-id="3b915-212">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b915-213"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="3b915-213"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3b915-214">DLL</span><span class="sxs-lookup"><span data-stu-id="3b915-214">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b915-215"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b915-215"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b915-216">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b915-216">See also</span></span>

<dl> <dt>

<span data-ttu-id="3b915-217">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3b915-217">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3b915-218">**Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="3b915-218">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 


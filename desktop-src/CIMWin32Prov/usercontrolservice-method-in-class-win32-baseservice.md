---
description: 嘗試將使用者定義的控制項程式碼傳送至服務。
ms.assetid: d181dbf8-e1ad-47b2-9e64-4aabc77e64bd
ms.tgt_platform: multiple
title: Win32_BaseService 類別的 UserControlService 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.UserControlService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 55647524c8ba561716441976fe6654b933e1900b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847531"
---
# <a name="usercontrolservice-method-of-the-win32_baseservice-class"></a><span data-ttu-id="24edb-103">Win32 BaseService 類別的 UserControlService 方法 \_</span><span class="sxs-lookup"><span data-stu-id="24edb-103">UserControlService method of the Win32\_BaseService class</span></span>

<span data-ttu-id="24edb-104">[WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會嘗試將使用者定義的控制項程式碼傳送至服務。</span><span class="sxs-lookup"><span data-stu-id="24edb-104">The [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to send a user-defined control code to a service.</span></span>

<span data-ttu-id="24edb-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="24edb-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="24edb-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="24edb-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="24edb-107">語法</span><span class="sxs-lookup"><span data-stu-id="24edb-107">Syntax</span></span>


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a><span data-ttu-id="24edb-108">參數</span><span class="sxs-lookup"><span data-stu-id="24edb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24edb-109">*ControlCode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="24edb-109">*ControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24edb-110">值，指定服務的控制項命令。</span><span class="sxs-lookup"><span data-stu-id="24edb-110">Value that specifies a control command to a service.</span></span> <span data-ttu-id="24edb-111">例如，控制命令是「暫停」或「繼續」命令。</span><span class="sxs-lookup"><span data-stu-id="24edb-111">For example a control command is a "pause" or "continue" command.</span></span> <span data-ttu-id="24edb-112">值可以是預先定義的程式碼，或是服務定義的值和動作。</span><span class="sxs-lookup"><span data-stu-id="24edb-112">The value can be a predefined code, or a value and action that the service defines.</span></span> <span data-ttu-id="24edb-113">以下是預先定義的控制項代碼：</span><span class="sxs-lookup"><span data-stu-id="24edb-113">The following are the predefined control codes:</span></span>

<dt>

<span id="SERVICE_CONTROL_CONTINUE"></span><span id="service_control_continue"></span>

<span data-ttu-id="24edb-114"><span id="SERVICE_CONTROL_CONTINUE"></span><span id="service_control_continue"></span>**服務 \_ 控制 \_ 繼續**</span><span class="sxs-lookup"><span data-stu-id="24edb-114"><span id="SERVICE_CONTROL_CONTINUE"></span><span id="service_control_continue"></span>**SERVICE\_CONTROL\_CONTINUE**</span></span>


</dt> <dd>

<span data-ttu-id="24edb-115">通知暫停的服務繼續。</span><span class="sxs-lookup"><span data-stu-id="24edb-115">Notifies a paused service to resume.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_INTERROGATE"></span><span id="service_control_interrogate"></span>

<span data-ttu-id="24edb-116"><span id="SERVICE_CONTROL_INTERROGATE"></span><span id="service_control_interrogate"></span>**服務 \_ 控制 \_ 詢問**</span><span class="sxs-lookup"><span data-stu-id="24edb-116"><span id="SERVICE_CONTROL_INTERROGATE"></span><span id="service_control_interrogate"></span>**SERVICE\_CONTROL\_INTERROGATE**</span></span>


</dt> <dd>

<span data-ttu-id="24edb-117">通知服務向服務控制管理員報告目前的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="24edb-117">Notifies a service to report the current status information to the service control manager.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDADD"></span><span id="service_control_netbindadd"></span>

<span data-ttu-id="24edb-118"><span id="SERVICE_CONTROL_NETBINDADD"></span><span id="service_control_netbindadd"></span>**服務 \_ 控制 \_ NETBINDADD**</span><span class="sxs-lookup"><span data-stu-id="24edb-118"><span id="SERVICE_CONTROL_NETBINDADD"></span><span id="service_control_netbindadd"></span>**SERVICE\_CONTROL\_NETBINDADD**</span></span>


</dt> <dd>

<span data-ttu-id="24edb-119">通知網路服務有系結的新元件。</span><span class="sxs-lookup"><span data-stu-id="24edb-119">Notifies a network service that there is a new component for binding.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDDISABLE"></span><span id="service_control_netbinddisable"></span>

<span data-ttu-id="24edb-120"><span id="SERVICE_CONTROL_NETBINDDISABLE"></span><span id="service_control_netbinddisable"></span>**服務 \_ 控制 \_ NETBINDDISABLE**</span><span class="sxs-lookup"><span data-stu-id="24edb-120"><span id="SERVICE_CONTROL_NETBINDDISABLE"></span><span id="service_control_netbinddisable"></span>**SERVICE\_CONTROL\_NETBINDDISABLE**</span></span>


</dt> <dd>

<span data-ttu-id="24edb-121">通知網路服務，其中一個系結已停用。</span><span class="sxs-lookup"><span data-stu-id="24edb-121">Notifies a network service that one of its bindings is disabled.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDENABLE"></span><span id="service_control_netbindenable"></span>

<span data-ttu-id="24edb-122"><span id="SERVICE_CONTROL_NETBINDENABLE"></span><span id="service_control_netbindenable"></span>**服務 \_ 控制 \_ NETBINDENABLE**</span><span class="sxs-lookup"><span data-stu-id="24edb-122"><span id="SERVICE_CONTROL_NETBINDENABLE"></span><span id="service_control_netbindenable"></span>**SERVICE\_CONTROL\_NETBINDENABLE**</span></span>


</dt> <dd>

<span data-ttu-id="24edb-123">通知網路服務已停用已停用的系結。</span><span class="sxs-lookup"><span data-stu-id="24edb-123">Notifies a network service that a disabled binding is enabled.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDREMOVE"></span><span id="service_control_netbindremove"></span>

<span data-ttu-id="24edb-124"><span id="SERVICE_CONTROL_NETBINDREMOVE"></span><span id="service_control_netbindremove"></span>**服務 \_ 控制 \_ NETBINDREMOVE**</span><span class="sxs-lookup"><span data-stu-id="24edb-124"><span id="SERVICE_CONTROL_NETBINDREMOVE"></span><span id="service_control_netbindremove"></span>**SERVICE\_CONTROL\_NETBINDREMOVE**</span></span>


</dt> <dd>

<span data-ttu-id="24edb-125">通知網路服務已移除系結的元件。</span><span class="sxs-lookup"><span data-stu-id="24edb-125">Notifies a network service that a component for binding has been removed.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_PARAMCHANGE"></span><span id="service_control_paramchange"></span>

<span data-ttu-id="24edb-126"><span id="SERVICE_CONTROL_PARAMCHANGE"></span><span id="service_control_paramchange"></span>**服務 \_ 控制 \_ PARAMCHANGE**</span><span class="sxs-lookup"><span data-stu-id="24edb-126"><span id="SERVICE_CONTROL_PARAMCHANGE"></span><span id="service_control_paramchange"></span>**SERVICE\_CONTROL\_PARAMCHANGE**</span></span>


</dt> <dd>

<span data-ttu-id="24edb-127">通知服務其啟動參數已變更。</span><span class="sxs-lookup"><span data-stu-id="24edb-127">Notifies a service that its startup parameters are changed.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_PAUSE"></span><span id="service_control_pause"></span>

<span data-ttu-id="24edb-128"><span id="SERVICE_CONTROL_PAUSE"></span><span id="service_control_pause"></span>**服務 \_ 控制 \_ 暫停**</span><span class="sxs-lookup"><span data-stu-id="24edb-128"><span id="SERVICE_CONTROL_PAUSE"></span><span id="service_control_pause"></span>**SERVICE\_CONTROL\_PAUSE**</span></span>


</dt> <dd>

<span data-ttu-id="24edb-129">通知服務暫停。</span><span class="sxs-lookup"><span data-stu-id="24edb-129">Notifies a service to pause.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_STOP"></span><span id="service_control_stop"></span>

<span data-ttu-id="24edb-130"><span id="SERVICE_CONTROL_STOP"></span><span id="service_control_stop"></span>**服務 \_ 控制 \_ 停止**</span><span class="sxs-lookup"><span data-stu-id="24edb-130"><span id="SERVICE_CONTROL_STOP"></span><span id="service_control_stop"></span>**SERVICE\_CONTROL\_STOP**</span></span>


</dt> <dd>

<span data-ttu-id="24edb-131">通知服務停止。</span><span class="sxs-lookup"><span data-stu-id="24edb-131">Notifies a service to stop.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24edb-132">傳回值</span><span class="sxs-lookup"><span data-stu-id="24edb-132">Return value</span></span>

<span data-ttu-id="24edb-133">傳回下列清單所列的其中一個值，或傳回不同的值來表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="24edb-133">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="24edb-134">「成功」</span><span class="sxs-lookup"><span data-stu-id="24edb-134">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="24edb-135">0</span><span class="sxs-lookup"><span data-stu-id="24edb-135">0</span></span>

<span data-ttu-id="24edb-136">已接受要求。</span><span class="sxs-lookup"><span data-stu-id="24edb-136">The request is accepted.</span></span>

</dd> <dt>

<span data-ttu-id="24edb-137">**不支援**</span><span class="sxs-lookup"><span data-stu-id="24edb-137">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="24edb-138">1</span><span class="sxs-lookup"><span data-stu-id="24edb-138">1</span></span>

<span data-ttu-id="24edb-139">不支援此要求。</span><span class="sxs-lookup"><span data-stu-id="24edb-139">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="24edb-140">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="24edb-140">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="24edb-141">2</span><span class="sxs-lookup"><span data-stu-id="24edb-141">2</span></span>

<span data-ttu-id="24edb-142">使用者沒有必要的存取權限。</span><span class="sxs-lookup"><span data-stu-id="24edb-142">The user does not have the necessary access rights.</span></span>

</dd> <dt>

<span data-ttu-id="24edb-143">**相依服務正在執行**</span><span class="sxs-lookup"><span data-stu-id="24edb-143">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="24edb-144">3</span><span class="sxs-lookup"><span data-stu-id="24edb-144">3</span></span>

<span data-ttu-id="24edb-145">無法停止此服務，因為與它相依的其他服務正在執行中。</span><span class="sxs-lookup"><span data-stu-id="24edb-145">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="24edb-146">**不正確服務控制**</span><span class="sxs-lookup"><span data-stu-id="24edb-146">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="24edb-147">4</span><span class="sxs-lookup"><span data-stu-id="24edb-147">4</span></span>

<span data-ttu-id="24edb-148">要求的控制碼無效，或是服務不接受此控制碼。</span><span class="sxs-lookup"><span data-stu-id="24edb-148">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="24edb-149">**服務無法接受控制權**</span><span class="sxs-lookup"><span data-stu-id="24edb-149">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="24edb-150">5</span><span class="sxs-lookup"><span data-stu-id="24edb-150">5</span></span>

<span data-ttu-id="24edb-151">因為服務的狀態 ([**Win32 \_ BaseService**](win32-baseservice.md)，所以無法將要求的控制項程式碼傳送至服務。**State** 屬性) 等於0、1或2。</span><span class="sxs-lookup"><span data-stu-id="24edb-151">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="24edb-152">**服務非使用中**</span><span class="sxs-lookup"><span data-stu-id="24edb-152">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="24edb-153">6</span><span class="sxs-lookup"><span data-stu-id="24edb-153">6</span></span>

<span data-ttu-id="24edb-154">該服務已啟動。</span><span class="sxs-lookup"><span data-stu-id="24edb-154">The service has not started.</span></span>

</dd> <dt>

<span data-ttu-id="24edb-155">**服務要求超時**</span><span class="sxs-lookup"><span data-stu-id="24edb-155">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="24edb-156">7</span><span class="sxs-lookup"><span data-stu-id="24edb-156">7</span></span>

<span data-ttu-id="24edb-157">服務不會快速回應啟動要求。</span><span class="sxs-lookup"><span data-stu-id="24edb-157">The service does not respond to the start request quickly.</span></span>

</dd> <dt>

<span data-ttu-id="24edb-158">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="24edb-158">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="24edb-159">8</span><span class="sxs-lookup"><span data-stu-id="24edb-159">8</span></span>

<span data-ttu-id="24edb-160">互動式進程。</span><span class="sxs-lookup"><span data-stu-id="24edb-160">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="24edb-161">**找不到路徑**</span><span class="sxs-lookup"><span data-stu-id="24edb-161">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="24edb-162">9</span><span class="sxs-lookup"><span data-stu-id="24edb-162">9</span></span>

<span data-ttu-id="24edb-163">找不到服務可執行檔的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="24edb-163">The directory path to the service executable file is not found.</span></span>

</dd> <dt>

<span data-ttu-id="24edb-164">**服務已在執行**</span><span class="sxs-lookup"><span data-stu-id="24edb-164">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="24edb-165">10</span><span class="sxs-lookup"><span data-stu-id="24edb-165">10</span></span>

<span data-ttu-id="24edb-166">服務已在執行中。</span><span class="sxs-lookup"><span data-stu-id="24edb-166">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="24edb-167">**服務資料庫已鎖定**</span><span class="sxs-lookup"><span data-stu-id="24edb-167">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="24edb-168">11</span><span class="sxs-lookup"><span data-stu-id="24edb-168">11</span></span>

<span data-ttu-id="24edb-169">要加入新服務的資料庫已被鎖定。</span><span class="sxs-lookup"><span data-stu-id="24edb-169">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="24edb-170">**服務相依性已刪除**</span><span class="sxs-lookup"><span data-stu-id="24edb-170">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="24edb-171">12</span><span class="sxs-lookup"><span data-stu-id="24edb-171">12</span></span>

<span data-ttu-id="24edb-172">這項服務所依賴的相依性會從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="24edb-172">A dependency that this service relies on is removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="24edb-173">**服務相依性失敗**</span><span class="sxs-lookup"><span data-stu-id="24edb-173">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="24edb-174">13</span><span class="sxs-lookup"><span data-stu-id="24edb-174">13</span></span>

<span data-ttu-id="24edb-175">服務在相依的服務中找不到所需的服務。</span><span class="sxs-lookup"><span data-stu-id="24edb-175">The service does not find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="24edb-176">**服務已停用**</span><span class="sxs-lookup"><span data-stu-id="24edb-176">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="24edb-177">14</span><span class="sxs-lookup"><span data-stu-id="24edb-177">14</span></span>

<span data-ttu-id="24edb-178">系統會停用服務。</span><span class="sxs-lookup"><span data-stu-id="24edb-178">The service is disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="24edb-179">**服務登入失敗**</span><span class="sxs-lookup"><span data-stu-id="24edb-179">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="24edb-180">15</span><span class="sxs-lookup"><span data-stu-id="24edb-180">15</span></span>

<span data-ttu-id="24edb-181">此服務未通過驗證，無法在系統上執行。</span><span class="sxs-lookup"><span data-stu-id="24edb-181">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="24edb-182">**已標示為要刪除的服務**</span><span class="sxs-lookup"><span data-stu-id="24edb-182">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="24edb-183">16</span><span class="sxs-lookup"><span data-stu-id="24edb-183">16</span></span>

<span data-ttu-id="24edb-184">正在從系統中移除此服務。</span><span class="sxs-lookup"><span data-stu-id="24edb-184">The service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="24edb-185">**服務無線程**</span><span class="sxs-lookup"><span data-stu-id="24edb-185">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="24edb-186">17</span><span class="sxs-lookup"><span data-stu-id="24edb-186">17</span></span>

<span data-ttu-id="24edb-187">服務沒有執行緒。</span><span class="sxs-lookup"><span data-stu-id="24edb-187">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="24edb-188">**狀態迴圈相依性**</span><span class="sxs-lookup"><span data-stu-id="24edb-188">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="24edb-189">18</span><span class="sxs-lookup"><span data-stu-id="24edb-189">18</span></span>

<span data-ttu-id="24edb-190">啟動服務時有循環的相依性。</span><span class="sxs-lookup"><span data-stu-id="24edb-190">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="24edb-191">**狀態重複名稱**</span><span class="sxs-lookup"><span data-stu-id="24edb-191">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="24edb-192">19</span><span class="sxs-lookup"><span data-stu-id="24edb-192">19</span></span>

<span data-ttu-id="24edb-193">有一個服務在相同名稱下執行。</span><span class="sxs-lookup"><span data-stu-id="24edb-193">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="24edb-194">**狀態不正確名稱**</span><span class="sxs-lookup"><span data-stu-id="24edb-194">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="24edb-195">20</span><span class="sxs-lookup"><span data-stu-id="24edb-195">20</span></span>

<span data-ttu-id="24edb-196">服務名稱中有不正確字元。</span><span class="sxs-lookup"><span data-stu-id="24edb-196">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="24edb-197">**狀態不正確參數**</span><span class="sxs-lookup"><span data-stu-id="24edb-197">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="24edb-198">21</span><span class="sxs-lookup"><span data-stu-id="24edb-198">21</span></span>

<span data-ttu-id="24edb-199">傳遞給服務的參數無效。</span><span class="sxs-lookup"><span data-stu-id="24edb-199">Invalid parameters have passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="24edb-200">**狀態不正確服務帳戶**</span><span class="sxs-lookup"><span data-stu-id="24edb-200">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="24edb-201">22</span><span class="sxs-lookup"><span data-stu-id="24edb-201">22</span></span>

<span data-ttu-id="24edb-202">執行此服務的帳戶無效，或沒有執行此服務的許可權。</span><span class="sxs-lookup"><span data-stu-id="24edb-202">The account that this service runs under is not valid or does not have the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="24edb-203">**狀態服務存在**</span><span class="sxs-lookup"><span data-stu-id="24edb-203">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="24edb-204">23</span><span class="sxs-lookup"><span data-stu-id="24edb-204">23</span></span>

<span data-ttu-id="24edb-205">服務存在於系統可使用之服務的資料庫中。</span><span class="sxs-lookup"><span data-stu-id="24edb-205">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="24edb-206">**服務已暫停**</span><span class="sxs-lookup"><span data-stu-id="24edb-206">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="24edb-207">24</span><span class="sxs-lookup"><span data-stu-id="24edb-207">24</span></span>

<span data-ttu-id="24edb-208">服務目前在系統中暫停。</span><span class="sxs-lookup"><span data-stu-id="24edb-208">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="24edb-209">**其他**</span><span class="sxs-lookup"><span data-stu-id="24edb-209">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="24edb-210">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="24edb-210">25 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="24edb-211">規格需求</span><span class="sxs-lookup"><span data-stu-id="24edb-211">Requirements</span></span>



| <span data-ttu-id="24edb-212">需求</span><span class="sxs-lookup"><span data-stu-id="24edb-212">Requirement</span></span> | <span data-ttu-id="24edb-213">值</span><span class="sxs-lookup"><span data-stu-id="24edb-213">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24edb-214">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="24edb-214">Minimum supported client</span></span><br/> | <span data-ttu-id="24edb-215">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="24edb-215">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="24edb-216">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="24edb-216">Minimum supported server</span></span><br/> | <span data-ttu-id="24edb-217">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="24edb-217">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="24edb-218">命名空間</span><span class="sxs-lookup"><span data-stu-id="24edb-218">Namespace</span></span><br/>                | <span data-ttu-id="24edb-219">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="24edb-219">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="24edb-220">MOF</span><span class="sxs-lookup"><span data-stu-id="24edb-220">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24edb-221"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="24edb-221"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="24edb-222">DLL</span><span class="sxs-lookup"><span data-stu-id="24edb-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24edb-223"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24edb-223"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24edb-224">另請參閱</span><span class="sxs-lookup"><span data-stu-id="24edb-224">See also</span></span>

<dl> <dt>

<span data-ttu-id="24edb-225">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="24edb-225">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="24edb-226">**Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="24edb-226">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 


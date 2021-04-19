---
description: 嘗試將此服務置於繼續狀態。
ms.assetid: df582402-d932-4132-a1ad-257b2993bbf6
ms.tgt_platform: multiple
title: Win32_BaseService 類別的 ResumeService 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.ResumeService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bba09180121d5649542f70a01adf2cb3acd7b142
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973374"
---
# <a name="resumeservice-method-of-the-win32_baseservice-class"></a><span data-ttu-id="d06e4-103">Win32 BaseService 類別的 ResumeService 方法 \_</span><span class="sxs-lookup"><span data-stu-id="d06e4-103">ResumeService method of the Win32\_BaseService class</span></span>

<span data-ttu-id="d06e4-104">**ResumeService** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會嘗試將服務置於繼續狀態。</span><span class="sxs-lookup"><span data-stu-id="d06e4-104">The **ResumeService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the service in the resumed state.</span></span>

<span data-ttu-id="d06e4-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="d06e4-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d06e4-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="d06e4-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d06e4-107">語法</span><span class="sxs-lookup"><span data-stu-id="d06e4-107">Syntax</span></span>


```mof
uint32 ResumeService();
```



## <a name="parameters"></a><span data-ttu-id="d06e4-108">參數</span><span class="sxs-lookup"><span data-stu-id="d06e4-108">Parameters</span></span>

<span data-ttu-id="d06e4-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d06e4-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d06e4-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="d06e4-110">Return value</span></span>

<span data-ttu-id="d06e4-111">傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="d06e4-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="d06e4-112">「成功」</span><span class="sxs-lookup"><span data-stu-id="d06e4-112">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="d06e4-113">0</span><span class="sxs-lookup"><span data-stu-id="d06e4-113">0</span></span>

<span data-ttu-id="d06e4-114">要求已被接受。</span><span class="sxs-lookup"><span data-stu-id="d06e4-114">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="d06e4-115">**不支援**</span><span class="sxs-lookup"><span data-stu-id="d06e4-115">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="d06e4-116">1</span><span class="sxs-lookup"><span data-stu-id="d06e4-116">1</span></span>

<span data-ttu-id="d06e4-117">不支援此要求。</span><span class="sxs-lookup"><span data-stu-id="d06e4-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="d06e4-118">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="d06e4-118">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="d06e4-119">2</span><span class="sxs-lookup"><span data-stu-id="d06e4-119">2</span></span>

<span data-ttu-id="d06e4-120">使用者沒有必要的存取權。</span><span class="sxs-lookup"><span data-stu-id="d06e4-120">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="d06e4-121">**相依服務正在執行**</span><span class="sxs-lookup"><span data-stu-id="d06e4-121">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="d06e4-122">3</span><span class="sxs-lookup"><span data-stu-id="d06e4-122">3</span></span>

<span data-ttu-id="d06e4-123">無法停止此服務，因為與它相依的其他服務正在執行中。</span><span class="sxs-lookup"><span data-stu-id="d06e4-123">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="d06e4-124">**不正確服務控制**</span><span class="sxs-lookup"><span data-stu-id="d06e4-124">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="d06e4-125">4</span><span class="sxs-lookup"><span data-stu-id="d06e4-125">4</span></span>

<span data-ttu-id="d06e4-126">要求的控制碼無效，或是服務不接受此控制碼。</span><span class="sxs-lookup"><span data-stu-id="d06e4-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="d06e4-127">**服務無法接受控制權**</span><span class="sxs-lookup"><span data-stu-id="d06e4-127">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="d06e4-128">5</span><span class="sxs-lookup"><span data-stu-id="d06e4-128">5</span></span>

<span data-ttu-id="d06e4-129">要求的控制項程式碼無法傳送至服務，因為服務的狀態 ([**Win32 \_ BaseService**](win32-baseservice.md)[**state**](win32-baseservice.md) 屬性) 等於0、1或2。</span><span class="sxs-lookup"><span data-stu-id="d06e4-129">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md)[**State**](win32-baseservice.md) property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="d06e4-130">**服務非使用中**</span><span class="sxs-lookup"><span data-stu-id="d06e4-130">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="d06e4-131">6</span><span class="sxs-lookup"><span data-stu-id="d06e4-131">6</span></span>

<span data-ttu-id="d06e4-132">尚未啟動服務。</span><span class="sxs-lookup"><span data-stu-id="d06e4-132">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="d06e4-133">**服務要求超時**</span><span class="sxs-lookup"><span data-stu-id="d06e4-133">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="d06e4-134">7</span><span class="sxs-lookup"><span data-stu-id="d06e4-134">7</span></span>

<span data-ttu-id="d06e4-135">服務並未及時回應啟動要求。</span><span class="sxs-lookup"><span data-stu-id="d06e4-135">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="d06e4-136">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="d06e4-136">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="d06e4-137">8</span><span class="sxs-lookup"><span data-stu-id="d06e4-137">8</span></span>

<span data-ttu-id="d06e4-138">互動式進程。</span><span class="sxs-lookup"><span data-stu-id="d06e4-138">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="d06e4-139">**找不到路徑**</span><span class="sxs-lookup"><span data-stu-id="d06e4-139">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="d06e4-140">9</span><span class="sxs-lookup"><span data-stu-id="d06e4-140">9</span></span>

<span data-ttu-id="d06e4-141">找不到服務可執行檔的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="d06e4-141">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="d06e4-142">**服務已在執行**</span><span class="sxs-lookup"><span data-stu-id="d06e4-142">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="d06e4-143">10</span><span class="sxs-lookup"><span data-stu-id="d06e4-143">10</span></span>

<span data-ttu-id="d06e4-144">服務已在執行中。</span><span class="sxs-lookup"><span data-stu-id="d06e4-144">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="d06e4-145">**服務資料庫已鎖定**</span><span class="sxs-lookup"><span data-stu-id="d06e4-145">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="d06e4-146">11</span><span class="sxs-lookup"><span data-stu-id="d06e4-146">11</span></span>

<span data-ttu-id="d06e4-147">要加入新服務的資料庫已被鎖定。</span><span class="sxs-lookup"><span data-stu-id="d06e4-147">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="d06e4-148">**服務相依性已刪除**</span><span class="sxs-lookup"><span data-stu-id="d06e4-148">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="d06e4-149">12</span><span class="sxs-lookup"><span data-stu-id="d06e4-149">12</span></span>

<span data-ttu-id="d06e4-150">已經從系統中移除這個服務所依賴的相依性。</span><span class="sxs-lookup"><span data-stu-id="d06e4-150">A dependency on which this service relies has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d06e4-151">**服務相依性失敗**</span><span class="sxs-lookup"><span data-stu-id="d06e4-151">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="d06e4-152">13</span><span class="sxs-lookup"><span data-stu-id="d06e4-152">13</span></span>

<span data-ttu-id="d06e4-153">服務在相依的服務中找不到所需的服務。</span><span class="sxs-lookup"><span data-stu-id="d06e4-153">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="d06e4-154">**服務已停用**</span><span class="sxs-lookup"><span data-stu-id="d06e4-154">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="d06e4-155">14</span><span class="sxs-lookup"><span data-stu-id="d06e4-155">14</span></span>

<span data-ttu-id="d06e4-156">已經從系統中停用服務。</span><span class="sxs-lookup"><span data-stu-id="d06e4-156">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d06e4-157">**服務登入失敗**</span><span class="sxs-lookup"><span data-stu-id="d06e4-157">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="d06e4-158">15</span><span class="sxs-lookup"><span data-stu-id="d06e4-158">15</span></span>

<span data-ttu-id="d06e4-159">此服務未通過驗證，無法在系統上執行。</span><span class="sxs-lookup"><span data-stu-id="d06e4-159">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="d06e4-160">**已標示為要刪除的服務**</span><span class="sxs-lookup"><span data-stu-id="d06e4-160">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="d06e4-161">16</span><span class="sxs-lookup"><span data-stu-id="d06e4-161">16</span></span>

<span data-ttu-id="d06e4-162">這項服務正在從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="d06e4-162">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d06e4-163">**服務無線程**</span><span class="sxs-lookup"><span data-stu-id="d06e4-163">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="d06e4-164">17</span><span class="sxs-lookup"><span data-stu-id="d06e4-164">17</span></span>

<span data-ttu-id="d06e4-165">服務沒有執行緒。</span><span class="sxs-lookup"><span data-stu-id="d06e4-165">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="d06e4-166">**狀態迴圈相依性**</span><span class="sxs-lookup"><span data-stu-id="d06e4-166">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="d06e4-167">18</span><span class="sxs-lookup"><span data-stu-id="d06e4-167">18</span></span>

<span data-ttu-id="d06e4-168">啟動服務時有循環的相依性。</span><span class="sxs-lookup"><span data-stu-id="d06e4-168">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="d06e4-169">**狀態重複名稱**</span><span class="sxs-lookup"><span data-stu-id="d06e4-169">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="d06e4-170">19</span><span class="sxs-lookup"><span data-stu-id="d06e4-170">19</span></span>

<span data-ttu-id="d06e4-171">有一個服務在相同名稱下執行。</span><span class="sxs-lookup"><span data-stu-id="d06e4-171">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="d06e4-172">**狀態不正確名稱**</span><span class="sxs-lookup"><span data-stu-id="d06e4-172">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="d06e4-173">20</span><span class="sxs-lookup"><span data-stu-id="d06e4-173">20</span></span>

<span data-ttu-id="d06e4-174">服務名稱中有不正確字元。</span><span class="sxs-lookup"><span data-stu-id="d06e4-174">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="d06e4-175">**狀態不正確參數**</span><span class="sxs-lookup"><span data-stu-id="d06e4-175">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="d06e4-176">21</span><span class="sxs-lookup"><span data-stu-id="d06e4-176">21</span></span>

<span data-ttu-id="d06e4-177">傳遞給服務的參數無效。</span><span class="sxs-lookup"><span data-stu-id="d06e4-177">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="d06e4-178">**狀態不正確服務帳戶**</span><span class="sxs-lookup"><span data-stu-id="d06e4-178">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="d06e4-179">22</span><span class="sxs-lookup"><span data-stu-id="d06e4-179">22</span></span>

<span data-ttu-id="d06e4-180">用來執行此服務的帳戶無效，或缺少執行服務的許可權。</span><span class="sxs-lookup"><span data-stu-id="d06e4-180">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="d06e4-181">**狀態服務存在**</span><span class="sxs-lookup"><span data-stu-id="d06e4-181">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="d06e4-182">23</span><span class="sxs-lookup"><span data-stu-id="d06e4-182">23</span></span>

<span data-ttu-id="d06e4-183">服務存在於系統可使用之服務的資料庫中。</span><span class="sxs-lookup"><span data-stu-id="d06e4-183">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d06e4-184">**服務已暫停**</span><span class="sxs-lookup"><span data-stu-id="d06e4-184">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="d06e4-185">24</span><span class="sxs-lookup"><span data-stu-id="d06e4-185">24</span></span>

<span data-ttu-id="d06e4-186">服務目前在系統中暫停。</span><span class="sxs-lookup"><span data-stu-id="d06e4-186">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="d06e4-187">**其他**</span><span class="sxs-lookup"><span data-stu-id="d06e4-187">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="d06e4-188">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="d06e4-188">25 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d06e4-189">規格需求</span><span class="sxs-lookup"><span data-stu-id="d06e4-189">Requirements</span></span>



| <span data-ttu-id="d06e4-190">需求</span><span class="sxs-lookup"><span data-stu-id="d06e4-190">Requirement</span></span> | <span data-ttu-id="d06e4-191">值</span><span class="sxs-lookup"><span data-stu-id="d06e4-191">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d06e4-192">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d06e4-192">Minimum supported client</span></span><br/> | <span data-ttu-id="d06e4-193">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d06e4-193">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d06e4-194">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d06e4-194">Minimum supported server</span></span><br/> | <span data-ttu-id="d06e4-195">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d06e4-195">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d06e4-196">命名空間</span><span class="sxs-lookup"><span data-stu-id="d06e4-196">Namespace</span></span><br/>                | <span data-ttu-id="d06e4-197">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d06e4-197">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d06e4-198">MOF</span><span class="sxs-lookup"><span data-stu-id="d06e4-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d06e4-199"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="d06e4-199"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d06e4-200">DLL</span><span class="sxs-lookup"><span data-stu-id="d06e4-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d06e4-201"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d06e4-201"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d06e4-202">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d06e4-202">See also</span></span>

<dl> <dt>

<span data-ttu-id="d06e4-203">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d06e4-203">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d06e4-204">**Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="d06e4-204">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 


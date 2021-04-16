---
description: 修改 Win32 >systemdriver 服務的啟動模式 \_ 。
ms.assetid: 34f4e0ac-d8a0-4be7-8c84-0252e50db441
ms.tgt_platform: multiple
title: Win32_SystemDriver 類別的 ChangeStartMode 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.ChangeStartMode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: edb6dfc9d745f5e408871246b581e6fab7eb72d3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510535"
---
# <a name="changestartmode-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="1034a-103">Win32 >systemdriver 類別的 ChangeStartMode 方法 \_</span><span class="sxs-lookup"><span data-stu-id="1034a-103">ChangeStartMode method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="1034a-104">**ChangeStartMode** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會修改 [**Win32 \_ >systemdriver**](win32-systemdriver.md)服務的啟動模式。</span><span class="sxs-lookup"><span data-stu-id="1034a-104">The **ChangeStartMode** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies the start mode of a [**Win32\_SystemDriver**](win32-systemdriver.md) service.</span></span>

<span data-ttu-id="1034a-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="1034a-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1034a-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="1034a-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1034a-107">語法</span><span class="sxs-lookup"><span data-stu-id="1034a-107">Syntax</span></span>


```mof
uint32 ChangeStartMode(
  [in] string StartMode = Auto Start
);
```



## <a name="parameters"></a><span data-ttu-id="1034a-108">參數</span><span class="sxs-lookup"><span data-stu-id="1034a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1034a-109">*StartMode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1034a-109">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1034a-110">Windows 基底服務的啟動模式。</span><span class="sxs-lookup"><span data-stu-id="1034a-110">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="1034a-111"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**開機開始 ( 「開機」** ) </span><span class="sxs-lookup"><span data-stu-id="1034a-111"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="1034a-112">作業系統載入器啟動的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="1034a-112">Device driver started by the operating system loader.</span></span> <span data-ttu-id="1034a-113">這個值只適用於驅動程式服務。</span><span class="sxs-lookup"><span data-stu-id="1034a-113">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="1034a-114"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ( "system" ) </span><span class="sxs-lookup"><span data-stu-id="1034a-114"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="1034a-115">由作業系統初始化程式啟動的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="1034a-115">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="1034a-116">這個值只適用於驅動程式服務。</span><span class="sxs-lookup"><span data-stu-id="1034a-116">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="1034a-117"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**自動啟動 ( 「自動」** ) </span><span class="sxs-lookup"><span data-stu-id="1034a-117"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start** ("Automatic")</span></span>


</dt> <dd>

<span data-ttu-id="1034a-118">要由服務控制管理員在系統啟動期間自動啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="1034a-118">Service to be started automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="1034a-119"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**需求開始 ( 「手動」** ) </span><span class="sxs-lookup"><span data-stu-id="1034a-119"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="1034a-120">當進程呼叫 [**StartService**](startservice-method-in-class-win32-systemdriver.md) 方法時，服務控制管理員要啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="1034a-120">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-systemdriver.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="1034a-121"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** ( [已停用] ) </span><span class="sxs-lookup"><span data-stu-id="1034a-121"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="1034a-122">無法再啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="1034a-122">Service that can no longer be started.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1034a-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="1034a-123">Return value</span></span>

<span data-ttu-id="1034a-124">如果成功修改服務，則傳回 0 (零) 的值; 如果不支援要求，則傳回 1 (一個) ，以及指出錯誤的其他任何數位。</span><span class="sxs-lookup"><span data-stu-id="1034a-124">Returns a value of 0 (zero) if the service was successfully modified, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="1034a-125">**成功** (0) </span><span class="sxs-lookup"><span data-stu-id="1034a-125">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1034a-126">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="1034a-126">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1034a-127">**拒絕存取** (2) </span><span class="sxs-lookup"><span data-stu-id="1034a-127">**Access Denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1034a-128">正在執行 (3) 的 **相依服務**</span><span class="sxs-lookup"><span data-stu-id="1034a-128">**Dependent Services Running** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1034a-129">**不正確服務控制** (4) </span><span class="sxs-lookup"><span data-stu-id="1034a-129">**Invalid Service Control** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1034a-130">**服務無法接受 Control** (5) </span><span class="sxs-lookup"><span data-stu-id="1034a-130">**Service Cannot Accept Control** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1034a-131">**服務非** 使用中 (6) </span><span class="sxs-lookup"><span data-stu-id="1034a-131">**Service Not Active** (6)</span></span>
</dt> <dt>

<span data-ttu-id="1034a-132">**服務要求超時** (7) </span><span class="sxs-lookup"><span data-stu-id="1034a-132">**Service Request Timeout** (7)</span></span>
</dt> <dt>

<span data-ttu-id="1034a-133">**未知的失敗** (8) </span><span class="sxs-lookup"><span data-stu-id="1034a-133">**Unknown Failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="1034a-134"> (9) **找不到路徑**</span><span class="sxs-lookup"><span data-stu-id="1034a-134">**Path Not Found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="1034a-135">**服務已** 在執行 (10) </span><span class="sxs-lookup"><span data-stu-id="1034a-135">**Service Already Running** (10)</span></span>
</dt> <dt>

<span data-ttu-id="1034a-136">**服務資料庫已鎖定** (11) </span><span class="sxs-lookup"><span data-stu-id="1034a-136">**Service Database Locked** (11)</span></span>
</dt> <dt>

<span data-ttu-id="1034a-137">**服務相依性已刪除** (12) </span><span class="sxs-lookup"><span data-stu-id="1034a-137">**Service Dependency Deleted** (12)</span></span>
</dt> <dt>

<span data-ttu-id="1034a-138">**服務** 相依性失敗 (13) </span><span class="sxs-lookup"><span data-stu-id="1034a-138">**Service Dependency Failure** (13)</span></span>
</dt> <dt>

<span data-ttu-id="1034a-139">**服務已停用** (14) </span><span class="sxs-lookup"><span data-stu-id="1034a-139">**Service Disabled** (14)</span></span>
</dt> <dt>

<span data-ttu-id="1034a-140">**服務登入失敗** (15) </span><span class="sxs-lookup"><span data-stu-id="1034a-140">**Service Logon Failed** (15)</span></span>
</dt> <dt>

<span data-ttu-id="1034a-141">已 **標示為要刪除的服務** (16) </span><span class="sxs-lookup"><span data-stu-id="1034a-141">**Service Marked For Deletion** (16)</span></span>
</dt> <dt>

<span data-ttu-id="1034a-142">**服務沒有線程** (17) </span><span class="sxs-lookup"><span data-stu-id="1034a-142">**Service No Thread** (17)</span></span>
</dt> <dt>

<span data-ttu-id="1034a-143">**狀態迴圈** 相依性 (18) </span><span class="sxs-lookup"><span data-stu-id="1034a-143">**Status Circular Dependency** (18)</span></span>
</dt> <dt>

<span data-ttu-id="1034a-144">**狀態重複名稱** (19) </span><span class="sxs-lookup"><span data-stu-id="1034a-144">**Status Duplicate Name** (19)</span></span>
</dt> <dt>

<span data-ttu-id="1034a-145">**狀態不正確名稱** (20) </span><span class="sxs-lookup"><span data-stu-id="1034a-145">**Status Invalid Name** (20)</span></span>
</dt> <dt>

<span data-ttu-id="1034a-146">**狀態不正確參數** (21) </span><span class="sxs-lookup"><span data-stu-id="1034a-146">**Status Invalid Parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="1034a-147">**狀態不正確服務帳戶** (22) </span><span class="sxs-lookup"><span data-stu-id="1034a-147">**Status Invalid Service Account** (22)</span></span>
</dt> <dt>

<span data-ttu-id="1034a-148">**狀態服務存在** (23) </span><span class="sxs-lookup"><span data-stu-id="1034a-148">**Status Service Exists** (23)</span></span>
</dt> <dt>

<span data-ttu-id="1034a-149">**服務已暫停** (24) </span><span class="sxs-lookup"><span data-stu-id="1034a-149">**Service Already Paused** (24)</span></span>
</dt> <dt>

<span data-ttu-id="1034a-150">**其他** (25 4294967295) </span><span class="sxs-lookup"><span data-stu-id="1034a-150">**Other** (25 4294967295)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="1034a-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="1034a-151">Requirements</span></span>



| <span data-ttu-id="1034a-152">需求</span><span class="sxs-lookup"><span data-stu-id="1034a-152">Requirement</span></span> | <span data-ttu-id="1034a-153">值</span><span class="sxs-lookup"><span data-stu-id="1034a-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1034a-154">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1034a-154">Minimum supported client</span></span><br/> | <span data-ttu-id="1034a-155">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1034a-155">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1034a-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1034a-156">Minimum supported server</span></span><br/> | <span data-ttu-id="1034a-157">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1034a-157">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1034a-158">命名空間</span><span class="sxs-lookup"><span data-stu-id="1034a-158">Namespace</span></span><br/>                | <span data-ttu-id="1034a-159">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1034a-159">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1034a-160">MOF</span><span class="sxs-lookup"><span data-stu-id="1034a-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1034a-161"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="1034a-161"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1034a-162">DLL</span><span class="sxs-lookup"><span data-stu-id="1034a-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1034a-163"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1034a-163"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1034a-164">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1034a-164">See also</span></span>

<dl> <dt>

<span data-ttu-id="1034a-165">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1034a-165">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1034a-166">**Win32 \_ >systemdriver**</span><span class="sxs-lookup"><span data-stu-id="1034a-166">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 


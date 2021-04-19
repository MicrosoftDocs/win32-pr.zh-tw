---
title: 'MPSTATUS_FLAG 列舉 (MpClient .h) '
description: 可能的整體產品狀態位旗標。
ms.assetid: BF2E6506-E76A-4785-8E91-99937B413548
keywords:
- MPSTATUS_FLAG 列舉舊版 Windows 環境功能
- PMPSTATUS_FLAG 列舉指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPSTATUS_FLAG
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c7175980c09c63938be04626091c31b53335756
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969973"
---
# <a name="mpstatus_flag-enumeration"></a><span data-ttu-id="b144e-105">MPSTATUS \_ 旗標列舉</span><span class="sxs-lookup"><span data-stu-id="b144e-105">MPSTATUS\_FLAG enumeration</span></span>

<span data-ttu-id="b144e-106">可能的整體產品狀態位旗標。</span><span class="sxs-lookup"><span data-stu-id="b144e-106">Possible overall product status bit flags.</span></span>

## <a name="syntax"></a><span data-ttu-id="b144e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b144e-107">Syntax</span></span>


```C++
typedef enum tagMPSTATUS_FLAG { 
  MP_STATUS_FLAG_NONE                           = 0,
  MP_STATUS_FLAG_SERVICE_UNAVAILABLE            = 1 << 0,
  MP_STATUS_FLAG_MPENGINE_UNAVAILABLE           = 1 << 1,
  MP_STATUS_FLAG_THREAT_FULLSCAN_REQUIRED       = 1 << 2,
  MP_STATUS_FLAG_THREAT_REBOOT_REQUIRED         = 1 << 3,
  MP_STATUS_FLAG_THREAT_MANUAL_STEPS_REQUIRED   = 1 << 4,
  MP_STATUS_FLAG_DUE_AV_SIGNATURE               = 1 << 5,
  MP_STATUS_FLAG_DUE_AS_SIGNATURE               = 1 << 6,
  MP_STATUS_FLAG_DUE_QUICK_SCAN                 = 1 << 7,
  MP_STATUS_FLAG_DUE_FULL_SCAN                  = 1 << 8,
  MP_STATUS_FLAG_INPROGRESS_SYSTEM_SCAN         = 1 << 9,
  MP_STATUS_FLAG_INPROGRESS_ROUTINE_CLEANING    = 1 << 10,
  MP_STATUS_FLAG_DUE_SAMPLES                    = 1 << 11,
  MP_STATUS_FLAG_EVALUATION_MODE                = 1 << 12,
  MP_STATUS_FLAG_NONGENUINE                     = 1 << 13,
  MP_STATUS_FLAG_PRODUCT_EXPIRED                = 1 << 14,
  MP_STATUS_FLAG_THREAT_CALLISTO_REQUIRED       = 1 << 15,
  MP_STATUS_FLAG_SERVICE_ON_SYSTEM_SHUTDOWN     = 1 << 16,
  MP_STATUS_FLAG_SERVICE_CRITICAL_FAILURE       = 1 << 17,
  MP_STATUS_FLAG_SERVICE_NON_CRITICAL_FAILURE   = 1 << 18,
  MP_STATUS_FLAG_HEALTH_INITIALIZED             = 1 << 19,
  MP_STATUS_FLAG_DUE_PLATFORM_UPDATE            = 1 << 20,
  MP_STATUS_FLAG_INPROGRESS_PLATFORM_UPDATE     = 1 << 21,
  MP_STATUS_FLAG_PLATFORM_ABOUT_TO_BE_OUTDATED  = 1 << 22,
  MP_STATUS_FLAG_END_OF_LIFE                    = 1 << 23,
  MP_STATUS_FLAG_MAX                            = 1 << 23,
  MP_STATUS_FLAG_ALL                            = (1 << 24)-1
} MPSTATUS_FLAG, *PMPSTATUS_FLAG;
```



## <a name="constants"></a><span data-ttu-id="b144e-108">常數</span><span class="sxs-lookup"><span data-stu-id="b144e-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b144e-109"><span id="MP_STATUS_FLAG_NONE"></span><span id="mp_status_flag_none"></span>**MP \_ 狀態 \_ 旗標 \_ 無**</span><span class="sxs-lookup"><span data-stu-id="b144e-109"><span id="MP_STATUS_FLAG_NONE"></span><span id="mp_status_flag_none"></span>**MP\_STATUS\_FLAG\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="b144e-110">未將狀態旗標設定 (未初始化的狀態) 。</span><span class="sxs-lookup"><span data-stu-id="b144e-110">No status flags set (non-initialized state).</span></span>

</dd> <dt>

<span data-ttu-id="b144e-111"><span id="MP_STATUS_FLAG_SERVICE_UNAVAILABLE"></span><span id="mp_status_flag_service_unavailable"></span>**MP \_ 狀態 \_ 旗標 \_ 服務 \_ 無法使用**</span><span class="sxs-lookup"><span data-stu-id="b144e-111"><span id="MP_STATUS_FLAG_SERVICE_UNAVAILABLE"></span><span id="mp_status_flag_service_unavailable"></span>**MP\_STATUS\_FLAG\_SERVICE\_UNAVAILABLE**</span></span>
</dt> <dd>

<span data-ttu-id="b144e-112">服務未執行。</span><span class="sxs-lookup"><span data-stu-id="b144e-112">Service not running.</span></span>

</dd> <dt>

<span data-ttu-id="b144e-113"><span id="MP_STATUS_FLAG_MPENGINE_UNAVAILABLE"></span><span id="mp_status_flag_mpengine_unavailable"></span>**MP \_ 狀態 \_ 旗標 \_ MPENGINE \_ 無法使用**</span><span class="sxs-lookup"><span data-stu-id="b144e-113"><span id="MP_STATUS_FLAG_MPENGINE_UNAVAILABLE"></span><span id="mp_status_flag_mpengine_unavailable"></span>**MP\_STATUS\_FLAG\_MPENGINE\_UNAVAILABLE**</span></span>
</dt> <dd>

<span data-ttu-id="b144e-114">服務在沒有任何 malware protection 引擎的情況下啟動。</span><span class="sxs-lookup"><span data-stu-id="b144e-114">Service started without any malware protection engine.</span></span>

</dd> <dt>

<span data-ttu-id="b144e-115"><span id="MP_STATUS_FLAG_THREAT_FULLSCAN_REQUIRED"></span><span id="mp_status_flag_threat_fullscan_required"></span>**\_需要 MP 狀態 \_ 旗標 \_ 威脅 \_ FULLSCAN \_**</span><span class="sxs-lookup"><span data-stu-id="b144e-115"><span id="MP_STATUS_FLAG_THREAT_FULLSCAN_REQUIRED"></span><span id="mp_status_flag_threat_fullscan_required"></span>**MP\_STATUS\_FLAG\_THREAT\_FULLSCAN\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="b144e-116">因為威脅動作而暫止完整掃描。</span><span class="sxs-lookup"><span data-stu-id="b144e-116">Pending full scan due to threat action.</span></span>

</dd> <dt>

<span data-ttu-id="b144e-117"><span id="MP_STATUS_FLAG_THREAT_REBOOT_REQUIRED"></span><span id="mp_status_flag_threat_reboot_required"></span>**\_ \_ \_ \_ 需要重新開機 MP 狀態旗標威脅 \_**</span><span class="sxs-lookup"><span data-stu-id="b144e-117"><span id="MP_STATUS_FLAG_THREAT_REBOOT_REQUIRED"></span><span id="mp_status_flag_threat_reboot_required"></span>**MP\_STATUS\_FLAG\_THREAT\_REBOOT\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="b144e-118">因為威脅動作而擱置重新開機。</span><span class="sxs-lookup"><span data-stu-id="b144e-118">Pending reboot due to threat action.</span></span>

</dd> <dt>

<span data-ttu-id="b144e-119"><span id="MP_STATUS_FLAG_THREAT_MANUAL_STEPS_REQUIRED"></span><span id="mp_status_flag_threat_manual_steps_required"></span>**\_需要 MP 狀態 \_ 旗標 \_ 威脅 \_ 手動 \_ 步驟 \_**</span><span class="sxs-lookup"><span data-stu-id="b144e-119"><span id="MP_STATUS_FLAG_THREAT_MANUAL_STEPS_REQUIRED"></span><span id="mp_status_flag_threat_manual_steps_required"></span>**MP\_STATUS\_FLAG\_THREAT\_MANUAL\_STEPS\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="b144e-120">因威脅動作而暫止的手動步驟。</span><span class="sxs-lookup"><span data-stu-id="b144e-120">Pending manual steps due to threat action.</span></span>

</dd> <dt>

<span data-ttu-id="b144e-121"><span id="MP_STATUS_FLAG_DUE_AV_SIGNATURE"></span><span id="mp_status_flag_due_av_signature"></span>**MP \_ 狀態 \_ 旗標 \_ 到期的 \_ AV \_ 簽名**</span><span class="sxs-lookup"><span data-stu-id="b144e-121"><span id="MP_STATUS_FLAG_DUE_AV_SIGNATURE"></span><span id="mp_status_flag_due_av_signature"></span>**MP\_STATUS\_FLAG\_DUE\_AV\_SIGNATURE**</span></span>
</dt> <dd>

<span data-ttu-id="b144e-122">防毒軟體簽章已過期。</span><span class="sxs-lookup"><span data-stu-id="b144e-122">Antivirus signatures out of date.</span></span>

</dd> <dt>

<span data-ttu-id="b144e-123"><span id="MP_STATUS_FLAG_DUE_AS_SIGNATURE"></span><span id="mp_status_flag_due_as_signature"></span>**因為簽章 \_ \_ 而產生 \_ \_ 的 \_ MP 狀態旗標**</span><span class="sxs-lookup"><span data-stu-id="b144e-123"><span id="MP_STATUS_FLAG_DUE_AS_SIGNATURE"></span><span id="mp_status_flag_due_as_signature"></span>**MP\_STATUS\_FLAG\_DUE\_AS\_SIGNATURE**</span></span>
</dt> <dd>

<span data-ttu-id="b144e-124">防毒軟體簽章已過期。</span><span class="sxs-lookup"><span data-stu-id="b144e-124">Antispyware signatures out of date.</span></span>

</dd> <dt>

<span data-ttu-id="b144e-125"><span id="MP_STATUS_FLAG_DUE_QUICK_SCAN"></span><span id="mp_status_flag_due_quick_scan"></span>**\_ \_ \_ 因為 \_ 快速掃描，所以 MP 狀態旗標 \_**</span><span class="sxs-lookup"><span data-stu-id="b144e-125"><span id="MP_STATUS_FLAG_DUE_QUICK_SCAN"></span><span id="mp_status_flag_due_quick_scan"></span>**MP\_STATUS\_FLAG\_DUE\_QUICK\_SCAN**</span></span>
</dt> <dd>

<span data-ttu-id="b144e-126">未在指定的期間內進行快速掃描。</span><span class="sxs-lookup"><span data-stu-id="b144e-126">No quick scan has happened for a specified period.</span></span>

</dd> <dt>

<span data-ttu-id="b144e-127"><span id="MP_STATUS_FLAG_DUE_FULL_SCAN"></span><span id="mp_status_flag_due_full_scan"></span>**MP \_ 狀態 \_ 旗標 \_ 到期的 \_ 完整 \_ 掃描**</span><span class="sxs-lookup"><span data-stu-id="b144e-127"><span id="MP_STATUS_FLAG_DUE_FULL_SCAN"></span><span id="mp_status_flag_due_full_scan"></span>**MP\_STATUS\_FLAG\_DUE\_FULL\_SCAN**</span></span>
</dt> <dd>

<span data-ttu-id="b144e-128">未在指定的期間內進行完整掃描</span><span class="sxs-lookup"><span data-stu-id="b144e-128">no full scan has happened for a specified period</span></span>

</dd> <dt>

<span data-ttu-id="b144e-129"><span id="MP_STATUS_FLAG_INPROGRESS_SYSTEM_SCAN"></span><span id="mp_status_flag_inprogress_system_scan"></span>**MP \_ STATUS \_ 旗標 \_ INPROGRESS \_ 系統 \_ 掃描**</span><span class="sxs-lookup"><span data-stu-id="b144e-129"><span id="MP_STATUS_FLAG_INPROGRESS_SYSTEM_SCAN"></span><span id="mp_status_flag_inprogress_system_scan"></span>**MP\_STATUS\_FLAG\_INPROGRESS\_SYSTEM\_SCAN**</span></span>
</dt> <dd>

<span data-ttu-id="b144e-130">系統起始的掃描進行中。</span><span class="sxs-lookup"><span data-stu-id="b144e-130">System-initiated scan in progress.</span></span>

</dd> <dt>

<span data-ttu-id="b144e-131"><span id="MP_STATUS_FLAG_INPROGRESS_ROUTINE_CLEANING"></span><span id="mp_status_flag_inprogress_routine_cleaning"></span>**MP \_ 狀態旗標正在進行 \_ \_ \_ 例行 \_ 清理**</span><span class="sxs-lookup"><span data-stu-id="b144e-131"><span id="MP_STATUS_FLAG_INPROGRESS_ROUTINE_CLEANING"></span><span id="mp_status_flag_inprogress_routine_cleaning"></span>**MP\_STATUS\_FLAG\_INPROGRESS\_ROUTINE\_CLEANING**</span></span>
</dt> <dd>

<span data-ttu-id="b144e-132">系統起始的清理進行中。</span><span class="sxs-lookup"><span data-stu-id="b144e-132">System-initiated clean in progress.</span></span>

</dd> <dt>

<span data-ttu-id="b144e-133"><span id="MP_STATUS_FLAG_DUE_SAMPLES"></span><span id="mp_status_flag_due_samples"></span>**MP \_ 狀態 \_ 旗標 \_ 到期 \_ 範例**</span><span class="sxs-lookup"><span data-stu-id="b144e-133"><span id="MP_STATUS_FLAG_DUE_SAMPLES"></span><span id="mp_status_flag_due_samples"></span>**MP\_STATUS\_FLAG\_DUE\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="b144e-134">有一些範例暫止提交。</span><span class="sxs-lookup"><span data-stu-id="b144e-134">There are samples pending submission.</span></span>

</dd> <dt>

<span data-ttu-id="b144e-135"><span id="MP_STATUS_FLAG_EVALUATION_MODE"></span><span id="mp_status_flag_evaluation_mode"></span>**MP \_ 狀態 \_ 旗標 \_ 評估 \_ 模式**</span><span class="sxs-lookup"><span data-stu-id="b144e-135"><span id="MP_STATUS_FLAG_EVALUATION_MODE"></span><span id="mp_status_flag_evaluation_mode"></span>**MP\_STATUS\_FLAG\_EVALUATION\_MODE**</span></span>
</dt> <dd>

<span data-ttu-id="b144e-136">產品正在評估模式中執行。</span><span class="sxs-lookup"><span data-stu-id="b144e-136">Product is running in evaluation mode.</span></span>

</dd> <dt>

<span data-ttu-id="b144e-137"><span id="MP_STATUS_FLAG_NONGENUINE"></span><span id="mp_status_flag_nongenuine"></span>**MP \_ STATUS \_ 旗標 \_ NONGENUINE**</span><span class="sxs-lookup"><span data-stu-id="b144e-137"><span id="MP_STATUS_FLAG_NONGENUINE"></span><span id="mp_status_flag_nongenuine"></span>**MP\_STATUS\_FLAG\_NONGENUINE**</span></span>
</dt> <dd>

<span data-ttu-id="b144e-138">產品以非正版 Windows 模式執行。</span><span class="sxs-lookup"><span data-stu-id="b144e-138">Product is running in non-genuine Windows mode.</span></span>

</dd> <dt>

<span data-ttu-id="b144e-139"><span id="MP_STATUS_FLAG_PRODUCT_EXPIRED"></span><span id="mp_status_flag_product_expired"></span>**MP \_ 狀態 \_ 旗標 \_ 產品已 \_ 過期**</span><span class="sxs-lookup"><span data-stu-id="b144e-139"><span id="MP_STATUS_FLAG_PRODUCT_EXPIRED"></span><span id="mp_status_flag_product_expired"></span>**MP\_STATUS\_FLAG\_PRODUCT\_EXPIRED**</span></span>
</dt> <dd>

<span data-ttu-id="b144e-140">產品已過期。</span><span class="sxs-lookup"><span data-stu-id="b144e-140">Product expired.</span></span>

</dd> <dt>

<span data-ttu-id="b144e-141"><span id="MP_STATUS_FLAG_THREAT_CALLISTO_REQUIRED"></span><span id="mp_status_flag_threat_callisto_required"></span>**\_需要 MP 狀態 \_ 旗標 \_ 威脅 \_ CALLISTO \_**</span><span class="sxs-lookup"><span data-stu-id="b144e-141"><span id="MP_STATUS_FLAG_THREAT_CALLISTO_REQUIRED"></span><span id="mp_status_flag_threat_callisto_required"></span>**MP\_STATUS\_FLAG\_THREAT\_CALLISTO\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="b144e-142">Callisto 需要離線掃描。</span><span class="sxs-lookup"><span data-stu-id="b144e-142">Callisto off-line scan required.</span></span>

</dd> <dt>

<span data-ttu-id="b144e-143"><span id="MP_STATUS_FLAG_SERVICE_ON_SYSTEM_SHUTDOWN"></span><span id="mp_status_flag_service_on_system_shutdown"></span>**\_ \_ \_ \_ \_ 系統關機時的 \_ MP 狀態旗標服務**</span><span class="sxs-lookup"><span data-stu-id="b144e-143"><span id="MP_STATUS_FLAG_SERVICE_ON_SYSTEM_SHUTDOWN"></span><span id="mp_status_flag_service_on_system_shutdown"></span>**MP\_STATUS\_FLAG\_SERVICE\_ON\_SYSTEM\_SHUTDOWN**</span></span>
</dt> <dd>

<span data-ttu-id="b144e-144">當系統關機時，服務正在關閉中。</span><span class="sxs-lookup"><span data-stu-id="b144e-144">Service is shutting down as part of system shutdown.</span></span>

</dd> <dt>

<span data-ttu-id="b144e-145"><span id="MP_STATUS_FLAG_SERVICE_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_critical_failure"></span>**MP \_ 狀態 \_ 旗 \_ \_ 標服務嚴重 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="b144e-145"><span id="MP_STATUS_FLAG_SERVICE_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_critical_failure"></span>**MP\_STATUS\_FLAG\_SERVICE\_CRITICAL\_FAILURE**</span></span>
</dt> <dd>

<span data-ttu-id="b144e-146">威脅補救嚴重失敗。</span><span class="sxs-lookup"><span data-stu-id="b144e-146">Threat remediation failed critically.</span></span>

</dd> <dt>

<span data-ttu-id="b144e-147"><span id="MP_STATUS_FLAG_SERVICE_NON_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_non_critical_failure"></span>**MP \_ 狀態 \_ 旗 \_ \_ 標服務非 \_ 重大 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="b144e-147"><span id="MP_STATUS_FLAG_SERVICE_NON_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_non_critical_failure"></span>**MP\_STATUS\_FLAG\_SERVICE\_NON\_CRITICAL\_FAILURE**</span></span>
</dt> <dd>

<span data-ttu-id="b144e-148">威脅補救不嚴重。</span><span class="sxs-lookup"><span data-stu-id="b144e-148">Threat remediation failed non-critically.</span></span>

</dd> <dt>

<span data-ttu-id="b144e-149"><span id="MP_STATUS_FLAG_HEALTH_INITIALIZED"></span><span id="mp_status_flag_health_initialized"></span>**MP \_ 狀態 \_ 旗標 \_ 健全狀況已 \_ 初始化**</span><span class="sxs-lookup"><span data-stu-id="b144e-149"><span id="MP_STATUS_FLAG_HEALTH_INITIALIZED"></span><span id="mp_status_flag_health_initialized"></span>**MP\_STATUS\_FLAG\_HEALTH\_INITIALIZED**</span></span>
</dt> <dd>

<span data-ttu-id="b144e-150">未將狀態旗標設定 (妥善初始化的狀態) 。</span><span class="sxs-lookup"><span data-stu-id="b144e-150">No status flags set (well-initialized state).</span></span>

</dd> <dt>

<span data-ttu-id="b144e-151"><span id="MP_STATUS_FLAG_DUE_PLATFORM_UPDATE"></span><span id="mp_status_flag_due_platform_update"></span>**MP \_ 狀態 \_ 旗標 \_ 因為 \_ 平臺 \_ 更新**</span><span class="sxs-lookup"><span data-stu-id="b144e-151"><span id="MP_STATUS_FLAG_DUE_PLATFORM_UPDATE"></span><span id="mp_status_flag_due_platform_update"></span>**MP\_STATUS\_FLAG\_DUE\_PLATFORM\_UPDATE**</span></span>
</dt> <dd>

<span data-ttu-id="b144e-152">平臺已過期。</span><span class="sxs-lookup"><span data-stu-id="b144e-152">The platform is out of date.</span></span>

</dd> <dt>

<span data-ttu-id="b144e-153"><span id="MP_STATUS_FLAG_INPROGRESS_PLATFORM_UPDATE"></span><span id="mp_status_flag_inprogress_platform_update"></span>**MP \_ 狀態 \_ 旗標 \_ INPROGRESS \_ 平臺 \_ 更新**</span><span class="sxs-lookup"><span data-stu-id="b144e-153"><span id="MP_STATUS_FLAG_INPROGRESS_PLATFORM_UPDATE"></span><span id="mp_status_flag_inprogress_platform_update"></span>**MP\_STATUS\_FLAG\_INPROGRESS\_PLATFORM\_UPDATE**</span></span>
</dt> <dd>

<span data-ttu-id="b144e-154">平臺更新正在進行中。</span><span class="sxs-lookup"><span data-stu-id="b144e-154">Platform update is in progress.</span></span>

</dd> <dt>

<span data-ttu-id="b144e-155"><span id="MP_STATUS_FLAG_PLATFORM_ABOUT_TO_BE_OUTDATED"></span><span id="mp_status_flag_platform_about_to_be_outdated"></span>**MP \_ 狀態 \_ 旗 \_ 標 \_ 平臺 \_ 即將 \_ \_ 過期**</span><span class="sxs-lookup"><span data-stu-id="b144e-155"><span id="MP_STATUS_FLAG_PLATFORM_ABOUT_TO_BE_OUTDATED"></span><span id="mp_status_flag_platform_about_to_be_outdated"></span>**MP\_STATUS\_FLAG\_PLATFORM\_ABOUT\_TO\_BE\_OUTDATED**</span></span>
</dt> <dd>

<span data-ttu-id="b144e-156">平臺即將過期</span><span class="sxs-lookup"><span data-stu-id="b144e-156">The platform is about to be outdated</span></span>

</dd> <dt>

<span data-ttu-id="b144e-157"><span id="MP_STATUS_FLAG_END_OF_LIFE"></span><span id="mp_status_flag_end_of_life"></span>**MP \_ 狀態 \_ 旗 \_ 標 \_ \_ 生命週期結束**</span><span class="sxs-lookup"><span data-stu-id="b144e-157"><span id="MP_STATUS_FLAG_END_OF_LIFE"></span><span id="mp_status_flag_end_of_life"></span>**MP\_STATUS\_FLAG\_END\_OF\_LIFE**</span></span>
</dt> <dd>

<span data-ttu-id="b144e-158">簽章或平臺生命週期已過期或暫止。</span><span class="sxs-lookup"><span data-stu-id="b144e-158">The signature or platform end of life is past or is pending.</span></span>

</dd> <dt>

<span data-ttu-id="b144e-159"><span id="MP_STATUS_FLAG_MAX"></span><span id="mp_status_flag_max"></span>**MP \_ 狀態 \_ 旗標 \_ 最大值**</span><span class="sxs-lookup"><span data-stu-id="b144e-159"><span id="MP_STATUS_FLAG_MAX"></span><span id="mp_status_flag_max"></span>**MP\_STATUS\_FLAG\_MAX**</span></span>
</dt> <dd>

<span data-ttu-id="b144e-160">有效的最大旗標。</span><span class="sxs-lookup"><span data-stu-id="b144e-160">Maximum valid flag.</span></span>

</dd> <dt>

<span data-ttu-id="b144e-161"><span id="MP_STATUS_FLAG_ALL"></span><span id="mp_status_flag_all"></span>**MP \_ 狀態 \_ 旗標 \_ 全部**</span><span class="sxs-lookup"><span data-stu-id="b144e-161"><span id="MP_STATUS_FLAG_ALL"></span><span id="mp_status_flag_all"></span>**MP\_STATUS\_FLAG\_ALL**</span></span>
</dt> <dd>

<span data-ttu-id="b144e-162">可能的最大值。</span><span class="sxs-lookup"><span data-stu-id="b144e-162">Maximum value possible.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b144e-163">規格需求</span><span class="sxs-lookup"><span data-stu-id="b144e-163">Requirements</span></span>



| <span data-ttu-id="b144e-164">需求</span><span class="sxs-lookup"><span data-stu-id="b144e-164">Requirement</span></span> | <span data-ttu-id="b144e-165">值</span><span class="sxs-lookup"><span data-stu-id="b144e-165">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b144e-166">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b144e-166">Minimum supported client</span></span><br/> | <span data-ttu-id="b144e-167">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b144e-167">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="b144e-168">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b144e-168">Minimum supported server</span></span><br/> | <span data-ttu-id="b144e-169">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b144e-169">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b144e-170">標頭</span><span class="sxs-lookup"><span data-stu-id="b144e-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="b144e-171"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="b144e-171"><dt>MpClient.h</dt></span></span> </dl> |



 

 






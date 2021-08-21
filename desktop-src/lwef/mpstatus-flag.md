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
ms.openlocfilehash: 4d850f0e8de9a3b0ed18a1a1353dfdef40d41bcb1ce4d17265ec245e82ba73f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747032"
---
# <a name="mpstatus_flag-enumeration"></a>MPSTATUS \_ 旗標列舉

可能的整體產品狀態位旗標。

## <a name="syntax"></a>Syntax


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



## <a name="constants"></a>常數

<dl> <dt>

<span id="MP_STATUS_FLAG_NONE"></span><span id="mp_status_flag_none"></span>**MP \_ 狀態 \_ 旗標 \_ 無**
</dt> <dd>

未將狀態旗標設定 (未初始化的狀態) 。

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_UNAVAILABLE"></span><span id="mp_status_flag_service_unavailable"></span>**MP \_ 狀態 \_ 旗標 \_ 服務 \_ 無法使用**
</dt> <dd>

服務未執行。

</dd> <dt>

<span id="MP_STATUS_FLAG_MPENGINE_UNAVAILABLE"></span><span id="mp_status_flag_mpengine_unavailable"></span>**MP \_ 狀態 \_ 旗標 \_ MPENGINE \_ 無法使用**
</dt> <dd>

服務在沒有任何 malware protection 引擎的情況下啟動。

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_FULLSCAN_REQUIRED"></span><span id="mp_status_flag_threat_fullscan_required"></span>**\_需要 MP 狀態 \_ 旗標 \_ 威脅 \_ FULLSCAN \_**
</dt> <dd>

因為威脅動作而暫止完整掃描。

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_REBOOT_REQUIRED"></span><span id="mp_status_flag_threat_reboot_required"></span>**\_ \_ \_ \_ 需要重新開機 MP 狀態旗標威脅 \_**
</dt> <dd>

因為威脅動作而擱置重新開機。

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_MANUAL_STEPS_REQUIRED"></span><span id="mp_status_flag_threat_manual_steps_required"></span>**\_需要 MP 狀態 \_ 旗標 \_ 威脅 \_ 手動 \_ 步驟 \_**
</dt> <dd>

因威脅動作而暫止的手動步驟。

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_AV_SIGNATURE"></span><span id="mp_status_flag_due_av_signature"></span>**MP \_ 狀態 \_ 旗標 \_ 到期的 \_ AV \_ 簽名**
</dt> <dd>

防毒軟體簽章已過期。

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_AS_SIGNATURE"></span><span id="mp_status_flag_due_as_signature"></span>**因為簽章 \_ \_ 而產生 \_ \_ 的 \_ MP 狀態旗標**
</dt> <dd>

防毒軟體簽章已過期。

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_QUICK_SCAN"></span><span id="mp_status_flag_due_quick_scan"></span>**\_ \_ \_ 因為 \_ 快速掃描，所以 MP 狀態旗標 \_**
</dt> <dd>

未在指定的期間內進行快速掃描。

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_FULL_SCAN"></span><span id="mp_status_flag_due_full_scan"></span>**MP \_ 狀態 \_ 旗標 \_ 到期的 \_ 完整 \_ 掃描**
</dt> <dd>

未在指定的期間內進行完整掃描

</dd> <dt>

<span id="MP_STATUS_FLAG_INPROGRESS_SYSTEM_SCAN"></span><span id="mp_status_flag_inprogress_system_scan"></span>**MP \_ STATUS \_ 旗標 \_ INPROGRESS \_ 系統 \_ 掃描**
</dt> <dd>

系統起始的掃描進行中。

</dd> <dt>

<span id="MP_STATUS_FLAG_INPROGRESS_ROUTINE_CLEANING"></span><span id="mp_status_flag_inprogress_routine_cleaning"></span>**MP \_ 狀態旗標正在進行 \_ \_ \_ 例行 \_ 清理**
</dt> <dd>

系統起始的清理進行中。

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_SAMPLES"></span><span id="mp_status_flag_due_samples"></span>**MP \_ 狀態 \_ 旗標 \_ 到期 \_ 範例**
</dt> <dd>

有一些範例暫止提交。

</dd> <dt>

<span id="MP_STATUS_FLAG_EVALUATION_MODE"></span><span id="mp_status_flag_evaluation_mode"></span>**MP \_ 狀態 \_ 旗標 \_ 評估 \_ 模式**
</dt> <dd>

產品正在評估模式中執行。

</dd> <dt>

<span id="MP_STATUS_FLAG_NONGENUINE"></span><span id="mp_status_flag_nongenuine"></span>**MP \_ STATUS \_ 旗標 \_ NONGENUINE**
</dt> <dd>

產品處於非正版的 Windows 模式。

</dd> <dt>

<span id="MP_STATUS_FLAG_PRODUCT_EXPIRED"></span><span id="mp_status_flag_product_expired"></span>**MP \_ 狀態 \_ 旗標 \_ 產品已 \_ 過期**
</dt> <dd>

產品已過期。

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_CALLISTO_REQUIRED"></span><span id="mp_status_flag_threat_callisto_required"></span>**\_需要 MP 狀態 \_ 旗標 \_ 威脅 \_ CALLISTO \_**
</dt> <dd>

Callisto 需要離線掃描。

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_ON_SYSTEM_SHUTDOWN"></span><span id="mp_status_flag_service_on_system_shutdown"></span>**\_ \_ \_ \_ \_ 系統關機時的 \_ MP 狀態旗標服務**
</dt> <dd>

當系統關機時，服務正在關閉中。

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_critical_failure"></span>**MP \_ 狀態 \_ 旗 \_ \_ 標服務嚴重 \_ 失敗**
</dt> <dd>

威脅補救嚴重失敗。

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_NON_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_non_critical_failure"></span>**MP \_ 狀態 \_ 旗 \_ \_ 標服務非 \_ 重大 \_ 失敗**
</dt> <dd>

威脅補救不嚴重。

</dd> <dt>

<span id="MP_STATUS_FLAG_HEALTH_INITIALIZED"></span><span id="mp_status_flag_health_initialized"></span>**MP \_ 狀態 \_ 旗標 \_ 健全狀況已 \_ 初始化**
</dt> <dd>

未將狀態旗標設定 (妥善初始化的狀態) 。

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_PLATFORM_UPDATE"></span><span id="mp_status_flag_due_platform_update"></span>**MP \_ 狀態 \_ 旗標 \_ 因為 \_ 平臺 \_ 更新**
</dt> <dd>

平臺已過期。

</dd> <dt>

<span id="MP_STATUS_FLAG_INPROGRESS_PLATFORM_UPDATE"></span><span id="mp_status_flag_inprogress_platform_update"></span>**MP \_ 狀態 \_ 旗標 \_ INPROGRESS \_ 平臺 \_ 更新**
</dt> <dd>

平臺更新正在進行中。

</dd> <dt>

<span id="MP_STATUS_FLAG_PLATFORM_ABOUT_TO_BE_OUTDATED"></span><span id="mp_status_flag_platform_about_to_be_outdated"></span>**MP \_ 狀態 \_ 旗 \_ 標 \_ 平臺 \_ 即將 \_ \_ 過期**
</dt> <dd>

平臺即將過期

</dd> <dt>

<span id="MP_STATUS_FLAG_END_OF_LIFE"></span><span id="mp_status_flag_end_of_life"></span>**MP \_ 狀態 \_ 旗 \_ 標 \_ \_ 生命週期結束**
</dt> <dd>

簽章或平臺生命週期已過期或暫止。

</dd> <dt>

<span id="MP_STATUS_FLAG_MAX"></span><span id="mp_status_flag_max"></span>**MP \_ 狀態 \_ 旗標 \_ 最大值**
</dt> <dd>

有效的最大旗標。

</dd> <dt>

<span id="MP_STATUS_FLAG_ALL"></span><span id="mp_status_flag_all"></span>**MP \_ 狀態 \_ 旗標 \_ 全部**
</dt> <dd>

可能的最大值。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



 

 






---
title: 'MPNOTIFY 列舉 (MpClient) '
description: 可能的回呼通知。
ms.assetid: CCD0CD89-2C6E-453F-9437-E6ED87AD9F29
keywords:
- MPNOTIFY 列舉舊版 Windows 環境功能
- PMPNOTIFY 列舉指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPNOTIFY
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed62a9f868aa39cbc0cfc7702afc99849005a22106892696eca857ffb20673af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747786"
---
# <a name="mpnotify-enumeration"></a>MPNOTIFY 列舉

可能的回呼通知。

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMPNOTIFY { 
  MPNOTIFY_NONE,
  MPNOTIFY_CALL_START,
  MPNOTIFY_CALL_COMPLETE,
  MPNOTIFY_INTERNAL_FAILURE,
  MPNOTIFY_STATUS_SERVICE_START,
  MPNOTIFY_STATUS_SERVICE_RUNNING,
  MPNOTIFY_STATUS_SERVICE_STOP,
  MPNOTIFY_STATUS_COMPONENT,
  MPNOTIFY_STATUS_CHANGE,
  MPNOTIFY_STATUS_COMPONENT_CONFIGURATION,
  MPNOTIFY_STATUS_EXPIRATION_CHANGE,
  MPNOTIFY_STATUS_OFFLINE_SCAN_CHANGE,
  MPNOTIFY_SCAN_START,
  MPNOTIFY_SCAN_PAUSED,
  MPNOTIFY_SCAN_RESUMED,
  MPNOTIFY_SCAN_CANCEL,
  MPNOTIFY_SCAN_COMPLETE,
  MPNOTIFY_SCAN_PROGRESS,
  MPNOTIFY_SCAN_ERROR,
  MPNOTIFY_SCAN_INFECTED,
  MPNOTIFY_SCAN_MEMORYSTART,
  MPNOTIFY_SCAN_MEMORYCOMPLETE,
  MPNOTIFY_SCAN_SFC_BUILD_START,
  MPNOTIFY_SCAN_SFC_BUILD_COMPLETE,
  MPNOTIFY_SCAN_FASTPATH_START,
  MPNOTIFY_SCAN_FASTPATH_COMPLETE,
  MPNOTIFY_SCAN_FASTPATH_PROGRESS,
  MPNOTIFY_CLEAN_START,
  MPNOTIFY_CLEAN_COMPLETE,
  MPNOTIFY_CLEAN_RESTOREPOINT_START,
  MPNOTIFY_CLEAN_RESTOREPOINT_SUCCEEDED,
  MPNOTIFY_CLEAN_RESTOREPOINT_FAILED,
  MPNOTIFY_CLEAN_THREAT_START,
  MPNOTIFY_CLEAN_THREAT_SUCCEEDED,
  MPNOTIFY_CLEAN_THREAT_FAILED,
  MPNOTIFY_CLEAN_RESOURCE_SUCCEEDED,
  MPNOTIFY_CLEAN_RESOURCE_FAILED,
  MPNOTIFY_CLEAN_THREAT_COMPLETE,
  MPNOTIFY_PRECHECK_START,
  MPNOTIFY_PRECHECK_COMPLETE,
  MPNOTIFY_PRECHECK_RESOURCE_BLOCKED,
  MPNOTIFY_THREAT_DETECTED,
  MPNOTIFY_THREAT_MODIFIED,
  MPNOTIFY_THREAT_CLEAN_SUCCEEDED,
  MPNOTIFY_THREAT_CLEAN_FAILED,
  MPNOTIFY_THREAT_ABANDONED,
  MPNOTIFY_THREAT_CLEAN_EVENT_START,
  MPNOTIFY_THREAT_CLEAN_EVENT_COMPLETE,
  MPNOTIFY_SIGUPDATE_START,
  MPNOTIFY_SIGUPDATE_SEARCH_START,
  MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE,
  MPNOTIFY_SIGUPDATE_SOFTWARE_UPDATE_AVAILABLE,
  MPNOTIFY_SIGUPDATE_DOWNLOAD_START,
  MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS,
  MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE,
  MPNOTIFY_SIGUPDATE_INSTALL_START,
  MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS,
  MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE,
  MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED,
  MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED,
  MPNOTIFY_SIGUPDATE_COMPLETE,
  MPNOTIFY_SAMPLE_START,
  MPNOTIFY_SAMPLE_COMPLETE,
  MPNOTIFY_SAMPLE_ITEM_START,
  MPNOTIFY_SAMPLE_ITEM_SUCCEEDED,
  MPNOTIFY_SAMPLE_ITEM_FAILED,
  MPNOTIFY_RESERVED_DATA,
  MPNOTIFY_FASTPATH_SIG_ADDED,
  MPNOTIFY_FASTPATH_SIG_REMOVED,
  MPNOTIFY_NIS_PRIVATE,
  MPNOTIFY_HEALTH_CHANGE,
  MPNOTIFY_HEALTH_RECOVERY,
  MPNOTIFY_HEALTH_START,
  MPNOTIFY_ENDOFLIFE_CHANGE,
  MPNOTIFY_MALWARETOAST_DATA
} MPNOTIFY, *PMPNOTIFY;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="MPNOTIFY_NONE"></span><span id="mpnotify_none"></span>**MPNOTIFY \_ 無**
</dt> <dd></dd> <dt>

<span id="MPNOTIFY_CALL_START"></span><span id="mpnotify_call_start"></span>**MPNOTIFY \_ 呼叫 \_ 開始**
</dt> <dd>

通知呼叫開始。

</dd> <dt>

<span id="MPNOTIFY_CALL_COMPLETE"></span><span id="mpnotify_call_complete"></span>**MPNOTIFY \_ 呼叫 \_ 完成**
</dt> <dd>

通知呼叫已完成。

</dd> <dt>

<span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span>**MPNOTIFY \_ 內部 \_ 失敗**
</dt> <dd>

一般內部失敗。

</dd> <dt>

<span id="MPNOTIFY_STATUS_SERVICE_START"></span><span id="mpnotify_status_service_start"></span>**MPNOTIFY \_ 狀態 \_ 服務 \_ 啟動**
</dt> <dd>

惡意程式碼防護服務已開始。

</dd> <dt>

<span id="MPNOTIFY_STATUS_SERVICE_RUNNING"></span><span id="mpnotify_status_service_running"></span>**MPNOTIFY \_ 狀態 \_ 服務執行中 \_**
</dt> <dd>

惡意程式碼防護服務正在執行。

</dd> <dt>

<span id="MPNOTIFY_STATUS_SERVICE_STOP"></span><span id="mpnotify_status_service_stop"></span>**MPNOTIFY \_ 狀態 \_ 服務 \_ 停止**
</dt> <dd>

惡意程式碼防護服務已停止。

</dd> <dt>

<span id="MPNOTIFY_STATUS_COMPONENT"></span><span id="mpnotify_status_component"></span>**MPNOTIFY \_ 狀態 \_ 元件**
</dt> <dd>

特定元件啟用/停用狀態。

</dd> <dt>

<span id="MPNOTIFY_STATUS_CHANGE"></span><span id="mpnotify_status_change"></span>**MPNOTIFY \_ 狀態 \_ 變更**
</dt> <dd>

整體產品狀態已變更。 呼叫 [**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md) 以取得目前的狀態。

</dd> <dt>

<span id="MPNOTIFY_STATUS_COMPONENT_CONFIGURATION"></span><span id="mpnotify_status_component_configuration"></span>**MPNOTIFY \_ 狀態 \_ 元件 \_ 設定**
</dt> <dd>

特定元件的設定已變更。

</dd> <dt>

<span id="MPNOTIFY_STATUS_EXPIRATION_CHANGE"></span><span id="mpnotify_status_expiration_change"></span>**MPNOTIFY \_ 狀態 \_ 到期 \_ 變更**
</dt> <dd>

產品到期狀態已變更。

</dd> <dt>

<span id="MPNOTIFY_STATUS_OFFLINE_SCAN_CHANGE"></span><span id="mpnotify_status_offline_scan_change"></span>**MPNOTIFY \_ 狀態 \_ 離線 \_ 掃描 \_ 變更**
</dt> <dd>

離線掃描所需的狀態已變更。

</dd> <dt>

<span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span>**MPNOTIFY \_ 掃描 \_ 開始**
</dt> <dd>

掃描已開始。

</dd> <dt>

<span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span>**MPNOTIFY \_ 掃描 \_ 暫停**
</dt> <dd>

掃描已暫停。

</dd> <dt>

<span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span>**MPNOTIFY \_ 掃描已 \_ 繼續**
</dt> <dd>

掃描已繼續。

</dd> <dt>

<span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span>**MPNOTIFY \_ 掃描 \_ 取消**
</dt> <dd>

掃描已取消。

</dd> <dt>

<span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span>**MPNOTIFY \_ 掃描 \_ 完成**
</dt> <dd>

掃描已完成。

</dd> <dt>

<span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span>**MPNOTIFY \_ 掃描 \_ 進度**
</dt> <dd>

正在掃描的特定資源的進度通知。

</dd> <dt>

<span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span>**MPNOTIFY \_ 掃描 \_ 錯誤**
</dt> <dd>

無法掃描特定的資源。 掃描仍將繼續進行。

</dd> <dt>

<span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span>**\_ \_ 受感染的 MPNOTIFY 掃描**
</dt> <dd>

掃描找到受感染的資源。

</dd> <dt>

<span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span>**MPNOTIFY \_ 掃描 \_ MEMORYSTART**
</dt> <dd>

掃描進度以通知系統掃描的記憶體掃描部分已啟動。

</dd> <dt>

<span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span>**MPNOTIFY \_ 掃描 \_ MEMORYCOMPLETE**
</dt> <dd>

掃描進度以通知系統掃描的記憶體掃描部分已完成。

</dd> <dt>

<span id="MPNOTIFY_SCAN_SFC_BUILD_START"></span><span id="mpnotify_scan_sfc_build_start"></span>**MPNOTIFY \_ 掃描 \_ SFC \_ 組建 \_ 開始**
</dt> <dd>

掃描進度以通知 sfc 組建部分已開始。

</dd> <dt>

<span id="MPNOTIFY_SCAN_SFC_BUILD_COMPLETE"></span><span id="mpnotify_scan_sfc_build_complete"></span>**MPNOTIFY \_ 掃描 \_ SFC \_ 組建 \_ 完成**
</dt> <dd>

通知 sfc 組建部分的掃描進度已完成。

</dd> <dt>

<span id="MPNOTIFY_SCAN_FASTPATH_START"></span><span id="mpnotify_scan_fastpath_start"></span>**MPNOTIFY \_ 掃描 \_ FASTPATH \_ 開始**
</dt> <dd>

掃描 fastpath spynet 已開始。

</dd> <dt>

<span id="MPNOTIFY_SCAN_FASTPATH_COMPLETE"></span><span id="mpnotify_scan_fastpath_complete"></span>**MPNOTIFY \_ 掃描 \_ FASTPATH \_ 完成**
</dt> <dd>

掃描 fastpath spynet 已結束。

</dd> <dt>

<span id="MPNOTIFY_SCAN_FASTPATH_PROGRESS"></span><span id="mpnotify_scan_fastpath_progress"></span>**MPNOTIFY \_ 掃描 \_ FASTPATH \_ 進度**
</dt> <dd>

Fastpath 重新掃描的進度通知，會在內部使用，並轉換為外部的 **MPNOTIFY \_ 掃描 \_ 進度** 。

</dd> <dt>

<span id="MPNOTIFY_CLEAN_START"></span><span id="mpnotify_clean_start"></span>**MPNOTIFY \_ 清除 \_ 開始**
</dt> <dd>

清除已開始。

</dd> <dt>

<span id="MPNOTIFY_CLEAN_COMPLETE"></span><span id="mpnotify_clean_complete"></span>**MPNOTIFY \_ 清除 \_ 完成**
</dt> <dd>

清除完成。

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESTOREPOINT_START"></span><span id="mpnotify_clean_restorepoint_start"></span>**MPNOTIFY \_ CLEAN \_ RESTOREPOINT \_ START**
</dt> <dd>

已開始建立系統還原點。

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESTOREPOINT_SUCCEEDED"></span><span id="mpnotify_clean_restorepoint_succeeded"></span>**MPNOTIFY \_ CLEAN \_ RESTOREPOINT \_ 成功**
</dt> <dd>

已成功建立系統還原點。

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESTOREPOINT_FAILED"></span><span id="mpnotify_clean_restorepoint_failed"></span>**MPNOTIFY \_ CLEAN \_ RESTOREPOINT \_ 失敗**
</dt> <dd>

系統還原點建立失敗。

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_START"></span><span id="mpnotify_clean_threat_start"></span>**MPNOTIFY \_ 全新 \_ 威脅 \_ 開始**
</dt> <dd>

已針對特定威脅啟動清除。

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_SUCCEEDED"></span><span id="mpnotify_clean_threat_succeeded"></span>**MPNOTIFY \_ 乾淨 \_ 威脅 \_ 成功**
</dt> <dd>

針對特定的威脅清除成功。

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_FAILED"></span><span id="mpnotify_clean_threat_failed"></span>**MPNOTIFY \_ 清除 \_ 威脅 \_ 失敗**
</dt> <dd>

特定威脅的清除失敗。 **錯誤 \_\_ \_ \_ 找不到 MP 威脅** 的錯誤碼。錯誤碼指出找不到威脅 (，且不是清除) 的問題。

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESOURCE_SUCCEEDED"></span><span id="mpnotify_clean_resource_succeeded"></span>**MPNOTIFY \_ 清理 \_ 資源 \_ 成功**
</dt> <dd>

針對特定資源的清除成功。

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESOURCE_FAILED"></span><span id="mpnotify_clean_resource_failed"></span>**MPNOTIFY \_ 清理 \_ 資源 \_ 失敗**
</dt> <dd>

特定資源的清除失敗。

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_COMPLETE"></span><span id="mpnotify_clean_threat_complete"></span>**MPNOTIFY \_ 全新 \_ 威脅 \_ 完成**
</dt> <dd>

已完成特定威脅的清理。

</dd> <dt>

<span id="MPNOTIFY_PRECHECK_START"></span><span id="mpnotify_precheck_start"></span>**MPNOTIFY 前置檢查 \_ \_ 開始**
</dt> <dd>

已開始清除檢查。

</dd> <dt>

<span id="MPNOTIFY_PRECHECK_COMPLETE"></span><span id="mpnotify_precheck_complete"></span>**MPNOTIFY \_ 檢查 \_ 完成**
</dt> <dd>

清除檢查完成。

</dd> <dt>

<span id="MPNOTIFY_PRECHECK_RESOURCE_BLOCKED"></span><span id="mpnotify_precheck_resource_blocked"></span>**MPNOTIFY 檢查的已 \_ \_ \_ 封鎖資源**
</dt> <dd>

清除檢查已封鎖的資源。

</dd> <dt>

<span id="MPNOTIFY_THREAT_DETECTED"></span><span id="mpnotify_threat_detected"></span>**偵測 \_ 到 MPNOTIFY 威脅 \_**
</dt> <dd>

在系統中偵測到新威脅。

</dd> <dt>

<span id="MPNOTIFY_THREAT_MODIFIED"></span><span id="mpnotify_threat_modified"></span>**修改的 MPNOTIFY \_ 威脅 \_**
</dt> <dd>

修改的威脅資訊。 例如，已加入新的資源。

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_SUCCEEDED"></span><span id="mpnotify_threat_clean_succeeded"></span>**MPNOTIFY \_ 威脅 \_ 清除 \_ 成功**
</dt> <dd>

已成功清除對威脅的動作。

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_FAILED"></span><span id="mpnotify_threat_clean_failed"></span>**MPNOTIFY \_ 威脅 \_ 清除 \_ 失敗**
</dt> <dd>

對威脅進行清除動作失敗。 **錯誤 \_\_ \_ \_ 找不到 MP 威脅** 的錯誤碼。錯誤碼指出找不到威脅 (，且不是清除) 的問題。

</dd> <dt>

<span id="MPNOTIFY_THREAT_ABANDONED"></span><span id="mpnotify_threat_abandoned"></span>**已 \_ 放棄 MPNOTIFY 威脅 \_**
</dt> <dd>

停止服務之前未發生補救。

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_EVENT_START"></span><span id="mpnotify_threat_clean_event_start"></span>**MPNOTIFY \_ 威脅 \_ 清除 \_ 事件 \_ 開始**
</dt> <dd>

已啟動清除動作。

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_EVENT_COMPLETE"></span><span id="mpnotify_threat_clean_event_complete"></span>**MPNOTIFY \_ 威脅 \_ 清除 \_ 事件 \_ 完成**
</dt> <dd>

清除動作已結束。

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span>**MPNOTIFY \_ SIGUPDATE \_ 開始**
</dt> <dd>

已開始更新簽章。

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span>**MPNOTIFY \_ SIGUPDATE \_ 搜尋 \_ 開始**
</dt> <dd>

開始搜尋更新。

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span>**MPNOTIFY \_ SIGUPDATE \_ 搜尋 \_ 完成**
</dt> <dd>

搜尋已完成的更新。

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_SOFTWARE_UPDATE_AVAILABLE"></span><span id="mpnotify_sigupdate_software_update_available"></span>**MPNOTIFY \_ SIGUPDATE \_ 軟體 \_ 更新 \_ 可用**
</dt> <dd>

可用的軟體更新。

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span>**MPNOTIFY \_ SIGUPDATE \_ 下載 \_ 開始**
</dt> <dd>

下載已開始。

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span>**MPNOTIFY \_ SIGUPDATE \_ 下載 \_ 進度**
</dt> <dd>

下載進行中。 回呼資料包含進度。

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span>**MPNOTIFY \_ SIGUPDATE \_ 下載 \_ 完成**
</dt> <dd>

下載已完成。

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span>**MPNOTIFY \_ SIGUPDATE \_ 安裝 \_ 開始**
</dt> <dd>

安裝已開始。

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span>**MPNOTIFY \_ SIGUPDATE \_ 安裝 \_ 進度**
</dt> <dd>

安裝進行中。 回呼資料包含進度。

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span>**MPNOTIFY \_ SIGUPDATE \_ 安裝 \_ 完成**
</dt> <dd>

安裝完成。

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span>**\_ \_ 需要重新開機 MPNOTIFY SIGUPDATE \_**
</dt> <dd>

更新需要重新開機。

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span>**已 \_ 處理 MPNOTIFY SIGUPDATE \_ 要求 \_**
</dt> <dd>

服務已處理簽名更新要求。 回呼資料中的 **hResult** 會指出失敗或成功。

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span>**MPNOTIFY \_ SIGUPDATE \_ 完成**
</dt> <dd>

更新完成。 **S \_FALSE** 狀態表示不需要更新。

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_START"></span><span id="mpnotify_sample_start"></span>**MPNOTIFY \_ 範例 \_ 開始**
</dt> <dd>

範例提交已開始。

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_COMPLETE"></span><span id="mpnotify_sample_complete"></span>**MPNOTIFY \_ 範例 \_ 完成**
</dt> <dd>

範例提交已完成。

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_ITEM_START"></span><span id="mpnotify_sample_item_start"></span>**MPNOTIFY \_ 範例 \_ 專案 \_ 開始**
</dt> <dd>

已開始提交特定範例專案。 範例專案索引可在 [**MPSAMPLE \_ 資料**](mpsample-data.md)中取得。

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_ITEM_SUCCEEDED"></span><span id="mpnotify_sample_item_succeeded"></span>**MPNOTIFY \_ 範例 \_ 專案 \_ 成功**
</dt> <dd>

已成功提交特定範例專案。

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_ITEM_FAILED"></span><span id="mpnotify_sample_item_failed"></span>**MPNOTIFY \_ 範例 \_ 專案 \_ 失敗**
</dt> <dd>

特定的範例專案提交失敗。 錯誤碼適用于 [**MPCALLBACK \_ 資料**](mpcallback-data.md)。

</dd> <dt>

<span id="MPNOTIFY_RESERVED_DATA"></span><span id="mpnotify_reserved_data"></span>**MPNOTIFY \_ 保留的 \_ 資料**
</dt> <dd>

內部保留的資料。

</dd> <dt>

<span id="MPNOTIFY_FASTPATH_SIG_ADDED"></span><span id="mpnotify_fastpath_sig_added"></span>**\_ \_ 已新增 MPNOTIFY FASTPATH SIG \_**
</dt> <dd>

Fastpath 簽章已新增或停用簽章。

</dd> <dt>

<span id="MPNOTIFY_FASTPATH_SIG_REMOVED"></span><span id="mpnotify_fastpath_sig_removed"></span>**\_ \_ 已移除 MPNOTIFY FASTPATH SIG \_**
</dt> <dd>

已移除 FastPath 簽章。

</dd> <dt>

<span id="MPNOTIFY_NIS_PRIVATE"></span><span id="mpnotify_nis_private"></span>**MPNOTIFY \_ NIS \_ 私用**
</dt> <dd>

NIS 私用 notifcations。 沒有任何夥伴註冊此。

</dd> <dt>

<span id="MPNOTIFY_HEALTH_CHANGE"></span><span id="mpnotify_health_change"></span>**MPNOTIFY \_ 健康情況 \_ 變更**
</dt> <dd>

AM 服務已進入新的狀態。

</dd> <dt>

<span id="MPNOTIFY_HEALTH_RECOVERY"></span><span id="mpnotify_health_recovery"></span>**MPNOTIFY \_ HEALTH \_ RECOVERY**
</dt> <dd>

AM 服務已從狀態復原。

</dd> <dt>

<span id="MPNOTIFY_HEALTH_START"></span><span id="mpnotify_health_start"></span>**MPNOTIFY \_ HEALTH \_ 開始**
</dt> <dd>

AM 服務已初始化系統的健全狀況。

</dd> <dt>

<span id="MPNOTIFY_ENDOFLIFE_CHANGE"></span><span id="mpnotify_endoflife_change"></span>**MPNOTIFY \_ ENDOFLIFE \_ 變更**
</dt> <dd>

AM 服務的「生命週期結束」到期日期已變更。

</dd> <dt>

<span id="MPNOTIFY_MALWARETOAST_DATA"></span><span id="mpnotify_malwaretoast_data"></span>**MPNOTIFY \_ MALWARETOAST \_ 資料**
</dt> <dd>

AM 服務發現惡意程式碼可能導致電腦的重大設定變更。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md)
</dt> <dt>

[**MPCALLBACK \_ 資料**](mpcallback-data.md)
</dt> <dt>

[**MPSAMPLE \_ 資料**](mpsample-data.md)
</dt> </dl>

 

 






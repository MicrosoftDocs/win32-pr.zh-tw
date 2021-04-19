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
ms.openlocfilehash: afa0eeb6cb1d610f28cc82f578617f7bd71cf886
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106979684"
---
# <a name="mpnotify-enumeration"></a><span data-ttu-id="93758-105">MPNOTIFY 列舉</span><span class="sxs-lookup"><span data-stu-id="93758-105">MPNOTIFY enumeration</span></span>

<span data-ttu-id="93758-106">可能的回呼通知。</span><span class="sxs-lookup"><span data-stu-id="93758-106">Possible callback notifications.</span></span>

## <a name="syntax"></a><span data-ttu-id="93758-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="93758-107">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="93758-108">常數</span><span class="sxs-lookup"><span data-stu-id="93758-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="93758-109"><span id="MPNOTIFY_NONE"></span><span id="mpnotify_none"></span>**MPNOTIFY \_ 無**</span><span class="sxs-lookup"><span data-stu-id="93758-109"><span id="MPNOTIFY_NONE"></span><span id="mpnotify_none"></span>**MPNOTIFY\_NONE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="93758-110"><span id="MPNOTIFY_CALL_START"></span><span id="mpnotify_call_start"></span>**MPNOTIFY \_ 呼叫 \_ 開始**</span><span class="sxs-lookup"><span data-stu-id="93758-110"><span id="MPNOTIFY_CALL_START"></span><span id="mpnotify_call_start"></span>**MPNOTIFY\_CALL\_START**</span></span>
</dt> <dd>

<span data-ttu-id="93758-111">通知呼叫開始。</span><span class="sxs-lookup"><span data-stu-id="93758-111">Notification call start.</span></span>

</dd> <dt>

<span data-ttu-id="93758-112"><span id="MPNOTIFY_CALL_COMPLETE"></span><span id="mpnotify_call_complete"></span>**MPNOTIFY \_ 呼叫 \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="93758-112"><span id="MPNOTIFY_CALL_COMPLETE"></span><span id="mpnotify_call_complete"></span>**MPNOTIFY\_CALL\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="93758-113">通知呼叫已完成。</span><span class="sxs-lookup"><span data-stu-id="93758-113">Notification call completed.</span></span>

</dd> <dt>

<span data-ttu-id="93758-114"><span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span>**MPNOTIFY \_ 內部 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="93758-114"><span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span>**MPNOTIFY\_INTERNAL\_FAILURE**</span></span>
</dt> <dd>

<span data-ttu-id="93758-115">一般內部失敗。</span><span class="sxs-lookup"><span data-stu-id="93758-115">Generic internal failure.</span></span>

</dd> <dt>

<span data-ttu-id="93758-116"><span id="MPNOTIFY_STATUS_SERVICE_START"></span><span id="mpnotify_status_service_start"></span>**MPNOTIFY \_ 狀態 \_ 服務 \_ 啟動**</span><span class="sxs-lookup"><span data-stu-id="93758-116"><span id="MPNOTIFY_STATUS_SERVICE_START"></span><span id="mpnotify_status_service_start"></span>**MPNOTIFY\_STATUS\_SERVICE\_START**</span></span>
</dt> <dd>

<span data-ttu-id="93758-117">惡意程式碼防護服務已開始。</span><span class="sxs-lookup"><span data-stu-id="93758-117">Malware protection service has started.</span></span>

</dd> <dt>

<span data-ttu-id="93758-118"><span id="MPNOTIFY_STATUS_SERVICE_RUNNING"></span><span id="mpnotify_status_service_running"></span>**MPNOTIFY \_ 狀態 \_ 服務執行中 \_**</span><span class="sxs-lookup"><span data-stu-id="93758-118"><span id="MPNOTIFY_STATUS_SERVICE_RUNNING"></span><span id="mpnotify_status_service_running"></span>**MPNOTIFY\_STATUS\_SERVICE\_RUNNING**</span></span>
</dt> <dd>

<span data-ttu-id="93758-119">惡意程式碼防護服務正在執行。</span><span class="sxs-lookup"><span data-stu-id="93758-119">Malware protection service is running.</span></span>

</dd> <dt>

<span data-ttu-id="93758-120"><span id="MPNOTIFY_STATUS_SERVICE_STOP"></span><span id="mpnotify_status_service_stop"></span>**MPNOTIFY \_ 狀態 \_ 服務 \_ 停止**</span><span class="sxs-lookup"><span data-stu-id="93758-120"><span id="MPNOTIFY_STATUS_SERVICE_STOP"></span><span id="mpnotify_status_service_stop"></span>**MPNOTIFY\_STATUS\_SERVICE\_STOP**</span></span>
</dt> <dd>

<span data-ttu-id="93758-121">惡意程式碼防護服務已停止。</span><span class="sxs-lookup"><span data-stu-id="93758-121">Malware protection service has stopped.</span></span>

</dd> <dt>

<span data-ttu-id="93758-122"><span id="MPNOTIFY_STATUS_COMPONENT"></span><span id="mpnotify_status_component"></span>**MPNOTIFY \_ 狀態 \_ 元件**</span><span class="sxs-lookup"><span data-stu-id="93758-122"><span id="MPNOTIFY_STATUS_COMPONENT"></span><span id="mpnotify_status_component"></span>**MPNOTIFY\_STATUS\_COMPONENT**</span></span>
</dt> <dd>

<span data-ttu-id="93758-123">特定元件啟用/停用狀態。</span><span class="sxs-lookup"><span data-stu-id="93758-123">Particular component enable/disable status.</span></span>

</dd> <dt>

<span data-ttu-id="93758-124"><span id="MPNOTIFY_STATUS_CHANGE"></span><span id="mpnotify_status_change"></span>**MPNOTIFY \_ 狀態 \_ 變更**</span><span class="sxs-lookup"><span data-stu-id="93758-124"><span id="MPNOTIFY_STATUS_CHANGE"></span><span id="mpnotify_status_change"></span>**MPNOTIFY\_STATUS\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="93758-125">整體產品狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="93758-125">Overall product status has changed.</span></span> <span data-ttu-id="93758-126">呼叫 [**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md) 以取得目前的狀態。</span><span class="sxs-lookup"><span data-stu-id="93758-126">Call [**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md) to obtain the current status.</span></span>

</dd> <dt>

<span data-ttu-id="93758-127"><span id="MPNOTIFY_STATUS_COMPONENT_CONFIGURATION"></span><span id="mpnotify_status_component_configuration"></span>**MPNOTIFY \_ 狀態 \_ 元件 \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="93758-127"><span id="MPNOTIFY_STATUS_COMPONENT_CONFIGURATION"></span><span id="mpnotify_status_component_configuration"></span>**MPNOTIFY\_STATUS\_COMPONENT\_CONFIGURATION**</span></span>
</dt> <dd>

<span data-ttu-id="93758-128">特定元件的設定已變更。</span><span class="sxs-lookup"><span data-stu-id="93758-128">A particular component has changed configuration.</span></span>

</dd> <dt>

<span data-ttu-id="93758-129"><span id="MPNOTIFY_STATUS_EXPIRATION_CHANGE"></span><span id="mpnotify_status_expiration_change"></span>**MPNOTIFY \_ 狀態 \_ 到期 \_ 變更**</span><span class="sxs-lookup"><span data-stu-id="93758-129"><span id="MPNOTIFY_STATUS_EXPIRATION_CHANGE"></span><span id="mpnotify_status_expiration_change"></span>**MPNOTIFY\_STATUS\_EXPIRATION\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="93758-130">產品到期狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="93758-130">Product expiration status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="93758-131"><span id="MPNOTIFY_STATUS_OFFLINE_SCAN_CHANGE"></span><span id="mpnotify_status_offline_scan_change"></span>**MPNOTIFY \_ 狀態 \_ 離線 \_ 掃描 \_ 變更**</span><span class="sxs-lookup"><span data-stu-id="93758-131"><span id="MPNOTIFY_STATUS_OFFLINE_SCAN_CHANGE"></span><span id="mpnotify_status_offline_scan_change"></span>**MPNOTIFY\_STATUS\_OFFLINE\_SCAN\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="93758-132">離線掃描所需的狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="93758-132">Offline scan required state changed.</span></span>

</dd> <dt>

<span data-ttu-id="93758-133"><span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span>**MPNOTIFY \_ 掃描 \_ 開始**</span><span class="sxs-lookup"><span data-stu-id="93758-133"><span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span>**MPNOTIFY\_SCAN\_START**</span></span>
</dt> <dd>

<span data-ttu-id="93758-134">掃描已開始。</span><span class="sxs-lookup"><span data-stu-id="93758-134">Scan started.</span></span>

</dd> <dt>

<span data-ttu-id="93758-135"><span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span>**MPNOTIFY \_ 掃描 \_ 暫停**</span><span class="sxs-lookup"><span data-stu-id="93758-135"><span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span>**MPNOTIFY\_SCAN\_PAUSED**</span></span>
</dt> <dd>

<span data-ttu-id="93758-136">掃描已暫停。</span><span class="sxs-lookup"><span data-stu-id="93758-136">Scan paused.</span></span>

</dd> <dt>

<span data-ttu-id="93758-137"><span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span>**MPNOTIFY \_ 掃描已 \_ 繼續**</span><span class="sxs-lookup"><span data-stu-id="93758-137"><span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span>**MPNOTIFY\_SCAN\_RESUMED**</span></span>
</dt> <dd>

<span data-ttu-id="93758-138">掃描已繼續。</span><span class="sxs-lookup"><span data-stu-id="93758-138">scan resumed.</span></span>

</dd> <dt>

<span data-ttu-id="93758-139"><span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span>**MPNOTIFY \_ 掃描 \_ 取消**</span><span class="sxs-lookup"><span data-stu-id="93758-139"><span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span>**MPNOTIFY\_SCAN\_CANCEL**</span></span>
</dt> <dd>

<span data-ttu-id="93758-140">掃描已取消。</span><span class="sxs-lookup"><span data-stu-id="93758-140">Scan cancelled.</span></span>

</dd> <dt>

<span data-ttu-id="93758-141"><span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span>**MPNOTIFY \_ 掃描 \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="93758-141"><span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span>**MPNOTIFY\_SCAN\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="93758-142">掃描已完成。</span><span class="sxs-lookup"><span data-stu-id="93758-142">Scan completed.</span></span>

</dd> <dt>

<span data-ttu-id="93758-143"><span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span>**MPNOTIFY \_ 掃描 \_ 進度**</span><span class="sxs-lookup"><span data-stu-id="93758-143"><span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span>**MPNOTIFY\_SCAN\_PROGRESS**</span></span>
</dt> <dd>

<span data-ttu-id="93758-144">正在掃描的特定資源的進度通知。</span><span class="sxs-lookup"><span data-stu-id="93758-144">Progress notification for the specific resource being scanned.</span></span>

</dd> <dt>

<span data-ttu-id="93758-145"><span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span>**MPNOTIFY \_ 掃描 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="93758-145"><span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span>**MPNOTIFY\_SCAN\_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="93758-146">無法掃描特定的資源。</span><span class="sxs-lookup"><span data-stu-id="93758-146">Failure to scan a particular resource.</span></span> <span data-ttu-id="93758-147">掃描仍將繼續進行。</span><span class="sxs-lookup"><span data-stu-id="93758-147">Scan will still continue.</span></span>

</dd> <dt>

<span data-ttu-id="93758-148"><span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span>**\_ \_ 受感染的 MPNOTIFY 掃描**</span><span class="sxs-lookup"><span data-stu-id="93758-148"><span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span>**MPNOTIFY\_SCAN\_INFECTED**</span></span>
</dt> <dd>

<span data-ttu-id="93758-149">掃描找到受感染的資源。</span><span class="sxs-lookup"><span data-stu-id="93758-149">Scan found an infected resource.</span></span>

</dd> <dt>

<span data-ttu-id="93758-150"><span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span>**MPNOTIFY \_ 掃描 \_ MEMORYSTART**</span><span class="sxs-lookup"><span data-stu-id="93758-150"><span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span>**MPNOTIFY\_SCAN\_MEMORYSTART**</span></span>
</dt> <dd>

<span data-ttu-id="93758-151">掃描進度以通知系統掃描的記憶體掃描部分已啟動。</span><span class="sxs-lookup"><span data-stu-id="93758-151">Scan progress to notify memory scan portion of the system scan has started.</span></span>

</dd> <dt>

<span data-ttu-id="93758-152"><span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span>**MPNOTIFY \_ 掃描 \_ MEMORYCOMPLETE**</span><span class="sxs-lookup"><span data-stu-id="93758-152"><span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span>**MPNOTIFY\_SCAN\_MEMORYCOMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="93758-153">掃描進度以通知系統掃描的記憶體掃描部分已完成。</span><span class="sxs-lookup"><span data-stu-id="93758-153">Scan progress to notify memory scan portion of the system scan has completed.</span></span>

</dd> <dt>

<span data-ttu-id="93758-154"><span id="MPNOTIFY_SCAN_SFC_BUILD_START"></span><span id="mpnotify_scan_sfc_build_start"></span>**MPNOTIFY \_ 掃描 \_ SFC \_ 組建 \_ 開始**</span><span class="sxs-lookup"><span data-stu-id="93758-154"><span id="MPNOTIFY_SCAN_SFC_BUILD_START"></span><span id="mpnotify_scan_sfc_build_start"></span>**MPNOTIFY\_SCAN\_SFC\_BUILD\_START**</span></span>
</dt> <dd>

<span data-ttu-id="93758-155">掃描進度以通知 sfc 組建部分已開始。</span><span class="sxs-lookup"><span data-stu-id="93758-155">Scan progress to notify sfc build portion has started.</span></span>

</dd> <dt>

<span data-ttu-id="93758-156"><span id="MPNOTIFY_SCAN_SFC_BUILD_COMPLETE"></span><span id="mpnotify_scan_sfc_build_complete"></span>**MPNOTIFY \_ 掃描 \_ SFC \_ 組建 \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="93758-156"><span id="MPNOTIFY_SCAN_SFC_BUILD_COMPLETE"></span><span id="mpnotify_scan_sfc_build_complete"></span>**MPNOTIFY\_SCAN\_SFC\_BUILD\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="93758-157">通知 sfc 組建部分的掃描進度已完成。</span><span class="sxs-lookup"><span data-stu-id="93758-157">Scan progress to notify sfc build portion has completed.</span></span>

</dd> <dt>

<span data-ttu-id="93758-158"><span id="MPNOTIFY_SCAN_FASTPATH_START"></span><span id="mpnotify_scan_fastpath_start"></span>**MPNOTIFY \_ 掃描 \_ FASTPATH \_ 開始**</span><span class="sxs-lookup"><span data-stu-id="93758-158"><span id="MPNOTIFY_SCAN_FASTPATH_START"></span><span id="mpnotify_scan_fastpath_start"></span>**MPNOTIFY\_SCAN\_FASTPATH\_START**</span></span>
</dt> <dd>

<span data-ttu-id="93758-159">掃描 fastpath spynet 已開始。</span><span class="sxs-lookup"><span data-stu-id="93758-159">Scan fastpath spynet has begun.</span></span>

</dd> <dt>

<span data-ttu-id="93758-160"><span id="MPNOTIFY_SCAN_FASTPATH_COMPLETE"></span><span id="mpnotify_scan_fastpath_complete"></span>**MPNOTIFY \_ 掃描 \_ FASTPATH \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="93758-160"><span id="MPNOTIFY_SCAN_FASTPATH_COMPLETE"></span><span id="mpnotify_scan_fastpath_complete"></span>**MPNOTIFY\_SCAN\_FASTPATH\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="93758-161">掃描 fastpath spynet 已結束。</span><span class="sxs-lookup"><span data-stu-id="93758-161">Scan fastpath spynet has ended.</span></span>

</dd> <dt>

<span data-ttu-id="93758-162"><span id="MPNOTIFY_SCAN_FASTPATH_PROGRESS"></span><span id="mpnotify_scan_fastpath_progress"></span>**MPNOTIFY \_ 掃描 \_ FASTPATH \_ 進度**</span><span class="sxs-lookup"><span data-stu-id="93758-162"><span id="MPNOTIFY_SCAN_FASTPATH_PROGRESS"></span><span id="mpnotify_scan_fastpath_progress"></span>**MPNOTIFY\_SCAN\_FASTPATH\_PROGRESS**</span></span>
</dt> <dd>

<span data-ttu-id="93758-163">Fastpath 重新掃描的進度通知，會在內部使用，並轉換為外部的 **MPNOTIFY \_ 掃描 \_ 進度** 。</span><span class="sxs-lookup"><span data-stu-id="93758-163">Progress notification for fastpath rescans, used internally and converted to **MPNOTIFY\_SCAN\_PROGRESS** for external.</span></span>

</dd> <dt>

<span data-ttu-id="93758-164"><span id="MPNOTIFY_CLEAN_START"></span><span id="mpnotify_clean_start"></span>**MPNOTIFY \_ 清除 \_ 開始**</span><span class="sxs-lookup"><span data-stu-id="93758-164"><span id="MPNOTIFY_CLEAN_START"></span><span id="mpnotify_clean_start"></span>**MPNOTIFY\_CLEAN\_START**</span></span>
</dt> <dd>

<span data-ttu-id="93758-165">清除已開始。</span><span class="sxs-lookup"><span data-stu-id="93758-165">Cleaning started.</span></span>

</dd> <dt>

<span data-ttu-id="93758-166"><span id="MPNOTIFY_CLEAN_COMPLETE"></span><span id="mpnotify_clean_complete"></span>**MPNOTIFY \_ 清除 \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="93758-166"><span id="MPNOTIFY_CLEAN_COMPLETE"></span><span id="mpnotify_clean_complete"></span>**MPNOTIFY\_CLEAN\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="93758-167">清除完成。</span><span class="sxs-lookup"><span data-stu-id="93758-167">Cleaning completed.</span></span>

</dd> <dt>

<span data-ttu-id="93758-168"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_START"></span><span id="mpnotify_clean_restorepoint_start"></span>**MPNOTIFY \_ CLEAN \_ RESTOREPOINT \_ START**</span><span class="sxs-lookup"><span data-stu-id="93758-168"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_START"></span><span id="mpnotify_clean_restorepoint_start"></span>**MPNOTIFY\_CLEAN\_RESTOREPOINT\_START**</span></span>
</dt> <dd>

<span data-ttu-id="93758-169">已開始建立系統還原點。</span><span class="sxs-lookup"><span data-stu-id="93758-169">Started to create a system restore point.</span></span>

</dd> <dt>

<span data-ttu-id="93758-170"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_SUCCEEDED"></span><span id="mpnotify_clean_restorepoint_succeeded"></span>**MPNOTIFY \_ CLEAN \_ RESTOREPOINT \_ 成功**</span><span class="sxs-lookup"><span data-stu-id="93758-170"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_SUCCEEDED"></span><span id="mpnotify_clean_restorepoint_succeeded"></span>**MPNOTIFY\_CLEAN\_RESTOREPOINT\_SUCCEEDED**</span></span>
</dt> <dd>

<span data-ttu-id="93758-171">已成功建立系統還原點。</span><span class="sxs-lookup"><span data-stu-id="93758-171">System restore point successfully created.</span></span>

</dd> <dt>

<span data-ttu-id="93758-172"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_FAILED"></span><span id="mpnotify_clean_restorepoint_failed"></span>**MPNOTIFY \_ CLEAN \_ RESTOREPOINT \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="93758-172"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_FAILED"></span><span id="mpnotify_clean_restorepoint_failed"></span>**MPNOTIFY\_CLEAN\_RESTOREPOINT\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="93758-173">系統還原點建立失敗。</span><span class="sxs-lookup"><span data-stu-id="93758-173">System restore point creation failed.</span></span>

</dd> <dt>

<span data-ttu-id="93758-174"><span id="MPNOTIFY_CLEAN_THREAT_START"></span><span id="mpnotify_clean_threat_start"></span>**MPNOTIFY \_ 全新 \_ 威脅 \_ 開始**</span><span class="sxs-lookup"><span data-stu-id="93758-174"><span id="MPNOTIFY_CLEAN_THREAT_START"></span><span id="mpnotify_clean_threat_start"></span>**MPNOTIFY\_CLEAN\_THREAT\_START**</span></span>
</dt> <dd>

<span data-ttu-id="93758-175">已針對特定威脅啟動清除。</span><span class="sxs-lookup"><span data-stu-id="93758-175">Cleaning is started for a particular threat.</span></span>

</dd> <dt>

<span data-ttu-id="93758-176"><span id="MPNOTIFY_CLEAN_THREAT_SUCCEEDED"></span><span id="mpnotify_clean_threat_succeeded"></span>**MPNOTIFY \_ 乾淨 \_ 威脅 \_ 成功**</span><span class="sxs-lookup"><span data-stu-id="93758-176"><span id="MPNOTIFY_CLEAN_THREAT_SUCCEEDED"></span><span id="mpnotify_clean_threat_succeeded"></span>**MPNOTIFY\_CLEAN\_THREAT\_SUCCEEDED**</span></span>
</dt> <dd>

<span data-ttu-id="93758-177">針對特定的威脅清除成功。</span><span class="sxs-lookup"><span data-stu-id="93758-177">Cleaning is succeeded for a particular threat.</span></span>

</dd> <dt>

<span data-ttu-id="93758-178"><span id="MPNOTIFY_CLEAN_THREAT_FAILED"></span><span id="mpnotify_clean_threat_failed"></span>**MPNOTIFY \_ 清除 \_ 威脅 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="93758-178"><span id="MPNOTIFY_CLEAN_THREAT_FAILED"></span><span id="mpnotify_clean_threat_failed"></span>**MPNOTIFY\_CLEAN\_THREAT\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="93758-179">特定威脅的清除失敗。</span><span class="sxs-lookup"><span data-stu-id="93758-179">Cleaning has failed for a particular threat.</span></span> <span data-ttu-id="93758-180">**錯誤 \_\_ \_ \_ 找不到 MP 威脅** 的錯誤碼。錯誤碼指出找不到威脅 (，且不是清除) 的問題。</span><span class="sxs-lookup"><span data-stu-id="93758-180">**ERROR\_MP\_THREAT\_NOT\_FOUND** error code indicates that the threat was not found (and was not a failure to clean).</span></span>

</dd> <dt>

<span data-ttu-id="93758-181"><span id="MPNOTIFY_CLEAN_RESOURCE_SUCCEEDED"></span><span id="mpnotify_clean_resource_succeeded"></span>**MPNOTIFY \_ 清理 \_ 資源 \_ 成功**</span><span class="sxs-lookup"><span data-stu-id="93758-181"><span id="MPNOTIFY_CLEAN_RESOURCE_SUCCEEDED"></span><span id="mpnotify_clean_resource_succeeded"></span>**MPNOTIFY\_CLEAN\_RESOURCE\_SUCCEEDED**</span></span>
</dt> <dd>

<span data-ttu-id="93758-182">針對特定資源的清除成功。</span><span class="sxs-lookup"><span data-stu-id="93758-182">Cleaning is succeeded for a particular resource.</span></span>

</dd> <dt>

<span data-ttu-id="93758-183"><span id="MPNOTIFY_CLEAN_RESOURCE_FAILED"></span><span id="mpnotify_clean_resource_failed"></span>**MPNOTIFY \_ 清理 \_ 資源 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="93758-183"><span id="MPNOTIFY_CLEAN_RESOURCE_FAILED"></span><span id="mpnotify_clean_resource_failed"></span>**MPNOTIFY\_CLEAN\_RESOURCE\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="93758-184">特定資源的清除失敗。</span><span class="sxs-lookup"><span data-stu-id="93758-184">Cleaning has failed for a particular resource.</span></span>

</dd> <dt>

<span data-ttu-id="93758-185"><span id="MPNOTIFY_CLEAN_THREAT_COMPLETE"></span><span id="mpnotify_clean_threat_complete"></span>**MPNOTIFY \_ 全新 \_ 威脅 \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="93758-185"><span id="MPNOTIFY_CLEAN_THREAT_COMPLETE"></span><span id="mpnotify_clean_threat_complete"></span>**MPNOTIFY\_CLEAN\_THREAT\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="93758-186">已完成特定威脅的清理。</span><span class="sxs-lookup"><span data-stu-id="93758-186">Cleaning has completed for a particular threat.</span></span>

</dd> <dt>

<span data-ttu-id="93758-187"><span id="MPNOTIFY_PRECHECK_START"></span><span id="mpnotify_precheck_start"></span>**MPNOTIFY 前置檢查 \_ \_ 開始**</span><span class="sxs-lookup"><span data-stu-id="93758-187"><span id="MPNOTIFY_PRECHECK_START"></span><span id="mpnotify_precheck_start"></span>**MPNOTIFY\_PRECHECK\_START**</span></span>
</dt> <dd>

<span data-ttu-id="93758-188">已開始清除檢查。</span><span class="sxs-lookup"><span data-stu-id="93758-188">Clean precheck started.</span></span>

</dd> <dt>

<span data-ttu-id="93758-189"><span id="MPNOTIFY_PRECHECK_COMPLETE"></span><span id="mpnotify_precheck_complete"></span>**MPNOTIFY \_ 檢查 \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="93758-189"><span id="MPNOTIFY_PRECHECK_COMPLETE"></span><span id="mpnotify_precheck_complete"></span>**MPNOTIFY\_PRECHECK\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="93758-190">清除檢查完成。</span><span class="sxs-lookup"><span data-stu-id="93758-190">Clean precheck completed.</span></span>

</dd> <dt>

<span data-ttu-id="93758-191"><span id="MPNOTIFY_PRECHECK_RESOURCE_BLOCKED"></span><span id="mpnotify_precheck_resource_blocked"></span>**MPNOTIFY 檢查的已 \_ \_ \_ 封鎖資源**</span><span class="sxs-lookup"><span data-stu-id="93758-191"><span id="MPNOTIFY_PRECHECK_RESOURCE_BLOCKED"></span><span id="mpnotify_precheck_resource_blocked"></span>**MPNOTIFY\_PRECHECK\_RESOURCE\_BLOCKED**</span></span>
</dt> <dd>

<span data-ttu-id="93758-192">清除檢查已封鎖的資源。</span><span class="sxs-lookup"><span data-stu-id="93758-192">Clean precheck detected blocked resource.</span></span>

</dd> <dt>

<span data-ttu-id="93758-193"><span id="MPNOTIFY_THREAT_DETECTED"></span><span id="mpnotify_threat_detected"></span>**偵測 \_ 到 MPNOTIFY 威脅 \_**</span><span class="sxs-lookup"><span data-stu-id="93758-193"><span id="MPNOTIFY_THREAT_DETECTED"></span><span id="mpnotify_threat_detected"></span>**MPNOTIFY\_THREAT\_DETECTED**</span></span>
</dt> <dd>

<span data-ttu-id="93758-194">在系統中偵測到新威脅。</span><span class="sxs-lookup"><span data-stu-id="93758-194">New threat detected in system.</span></span>

</dd> <dt>

<span data-ttu-id="93758-195"><span id="MPNOTIFY_THREAT_MODIFIED"></span><span id="mpnotify_threat_modified"></span>**修改的 MPNOTIFY \_ 威脅 \_**</span><span class="sxs-lookup"><span data-stu-id="93758-195"><span id="MPNOTIFY_THREAT_MODIFIED"></span><span id="mpnotify_threat_modified"></span>**MPNOTIFY\_THREAT\_MODIFIED**</span></span>
</dt> <dd>

<span data-ttu-id="93758-196">修改的威脅資訊。</span><span class="sxs-lookup"><span data-stu-id="93758-196">Threat information modified.</span></span> <span data-ttu-id="93758-197">例如，已加入新的資源。</span><span class="sxs-lookup"><span data-stu-id="93758-197">For example, a new resource was added.</span></span>

</dd> <dt>

<span data-ttu-id="93758-198"><span id="MPNOTIFY_THREAT_CLEAN_SUCCEEDED"></span><span id="mpnotify_threat_clean_succeeded"></span>**MPNOTIFY \_ 威脅 \_ 清除 \_ 成功**</span><span class="sxs-lookup"><span data-stu-id="93758-198"><span id="MPNOTIFY_THREAT_CLEAN_SUCCEEDED"></span><span id="mpnotify_threat_clean_succeeded"></span>**MPNOTIFY\_THREAT\_CLEAN\_SUCCEEDED**</span></span>
</dt> <dd>

<span data-ttu-id="93758-199">已成功清除對威脅的動作。</span><span class="sxs-lookup"><span data-stu-id="93758-199">Cleaning action succeeded for a threat.</span></span>

</dd> <dt>

<span data-ttu-id="93758-200"><span id="MPNOTIFY_THREAT_CLEAN_FAILED"></span><span id="mpnotify_threat_clean_failed"></span>**MPNOTIFY \_ 威脅 \_ 清除 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="93758-200"><span id="MPNOTIFY_THREAT_CLEAN_FAILED"></span><span id="mpnotify_threat_clean_failed"></span>**MPNOTIFY\_THREAT\_CLEAN\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="93758-201">對威脅進行清除動作失敗。</span><span class="sxs-lookup"><span data-stu-id="93758-201">Cleaning action failed for a threat.</span></span> <span data-ttu-id="93758-202">**錯誤 \_\_ \_ \_ 找不到 MP 威脅** 的錯誤碼。錯誤碼指出找不到威脅 (，且不是清除) 的問題。</span><span class="sxs-lookup"><span data-stu-id="93758-202">**ERROR\_MP\_THREAT\_NOT\_FOUND** error code indicates that the threat was not found (and was not a failure to clean).</span></span>

</dd> <dt>

<span data-ttu-id="93758-203"><span id="MPNOTIFY_THREAT_ABANDONED"></span><span id="mpnotify_threat_abandoned"></span>**已 \_ 放棄 MPNOTIFY 威脅 \_**</span><span class="sxs-lookup"><span data-stu-id="93758-203"><span id="MPNOTIFY_THREAT_ABANDONED"></span><span id="mpnotify_threat_abandoned"></span>**MPNOTIFY\_THREAT\_ABANDONED**</span></span>
</dt> <dd>

<span data-ttu-id="93758-204">停止服務之前未發生補救。</span><span class="sxs-lookup"><span data-stu-id="93758-204">No remediation occurred before the service was stopped.</span></span>

</dd> <dt>

<span data-ttu-id="93758-205"><span id="MPNOTIFY_THREAT_CLEAN_EVENT_START"></span><span id="mpnotify_threat_clean_event_start"></span>**MPNOTIFY \_ 威脅 \_ 清除 \_ 事件 \_ 開始**</span><span class="sxs-lookup"><span data-stu-id="93758-205"><span id="MPNOTIFY_THREAT_CLEAN_EVENT_START"></span><span id="mpnotify_threat_clean_event_start"></span>**MPNOTIFY\_THREAT\_CLEAN\_EVENT\_START**</span></span>
</dt> <dd>

<span data-ttu-id="93758-206">已啟動清除動作。</span><span class="sxs-lookup"><span data-stu-id="93758-206">A cleaning action has been started.</span></span>

</dd> <dt>

<span data-ttu-id="93758-207"><span id="MPNOTIFY_THREAT_CLEAN_EVENT_COMPLETE"></span><span id="mpnotify_threat_clean_event_complete"></span>**MPNOTIFY \_ 威脅 \_ 清除 \_ 事件 \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="93758-207"><span id="MPNOTIFY_THREAT_CLEAN_EVENT_COMPLETE"></span><span id="mpnotify_threat_clean_event_complete"></span>**MPNOTIFY\_THREAT\_CLEAN\_EVENT\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="93758-208">清除動作已結束。</span><span class="sxs-lookup"><span data-stu-id="93758-208">A cleaning action has ended.</span></span>

</dd> <dt>

<span data-ttu-id="93758-209"><span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span>**MPNOTIFY \_ SIGUPDATE \_ 開始**</span><span class="sxs-lookup"><span data-stu-id="93758-209"><span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span>**MPNOTIFY\_SIGUPDATE\_START**</span></span>
</dt> <dd>

<span data-ttu-id="93758-210">已開始更新簽章。</span><span class="sxs-lookup"><span data-stu-id="93758-210">Signature update started.</span></span>

</dd> <dt>

<span data-ttu-id="93758-211"><span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span>**MPNOTIFY \_ SIGUPDATE \_ 搜尋 \_ 開始**</span><span class="sxs-lookup"><span data-stu-id="93758-211"><span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span>**MPNOTIFY\_SIGUPDATE\_SEARCH\_START**</span></span>
</dt> <dd>

<span data-ttu-id="93758-212">開始搜尋更新。</span><span class="sxs-lookup"><span data-stu-id="93758-212">Search for updates started.</span></span>

</dd> <dt>

<span data-ttu-id="93758-213"><span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span>**MPNOTIFY \_ SIGUPDATE \_ 搜尋 \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="93758-213"><span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span>**MPNOTIFY\_SIGUPDATE\_SEARCH\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="93758-214">搜尋已完成的更新。</span><span class="sxs-lookup"><span data-stu-id="93758-214">Search for updates completed.</span></span>

</dd> <dt>

<span data-ttu-id="93758-215"><span id="MPNOTIFY_SIGUPDATE_SOFTWARE_UPDATE_AVAILABLE"></span><span id="mpnotify_sigupdate_software_update_available"></span>**MPNOTIFY \_ SIGUPDATE \_ 軟體 \_ 更新 \_ 可用**</span><span class="sxs-lookup"><span data-stu-id="93758-215"><span id="MPNOTIFY_SIGUPDATE_SOFTWARE_UPDATE_AVAILABLE"></span><span id="mpnotify_sigupdate_software_update_available"></span>**MPNOTIFY\_SIGUPDATE\_SOFTWARE\_UPDATE\_AVAILABLE**</span></span>
</dt> <dd>

<span data-ttu-id="93758-216">可用的軟體更新。</span><span class="sxs-lookup"><span data-stu-id="93758-216">Software update available.</span></span>

</dd> <dt>

<span data-ttu-id="93758-217"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span>**MPNOTIFY \_ SIGUPDATE \_ 下載 \_ 開始**</span><span class="sxs-lookup"><span data-stu-id="93758-217"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_START**</span></span>
</dt> <dd>

<span data-ttu-id="93758-218">下載已開始。</span><span class="sxs-lookup"><span data-stu-id="93758-218">Download started.</span></span>

</dd> <dt>

<span data-ttu-id="93758-219"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span>**MPNOTIFY \_ SIGUPDATE \_ 下載 \_ 進度**</span><span class="sxs-lookup"><span data-stu-id="93758-219"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_PROGRESS**</span></span>
</dt> <dd>

<span data-ttu-id="93758-220">下載進行中。</span><span class="sxs-lookup"><span data-stu-id="93758-220">Download in progress.</span></span> <span data-ttu-id="93758-221">回呼資料包含進度。</span><span class="sxs-lookup"><span data-stu-id="93758-221">Callback data contains progress.</span></span>

</dd> <dt>

<span data-ttu-id="93758-222"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span>**MPNOTIFY \_ SIGUPDATE \_ 下載 \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="93758-222"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="93758-223">下載已完成。</span><span class="sxs-lookup"><span data-stu-id="93758-223">Download completed.</span></span>

</dd> <dt>

<span data-ttu-id="93758-224"><span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span>**MPNOTIFY \_ SIGUPDATE \_ 安裝 \_ 開始**</span><span class="sxs-lookup"><span data-stu-id="93758-224"><span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span>**MPNOTIFY\_SIGUPDATE\_INSTALL\_START**</span></span>
</dt> <dd>

<span data-ttu-id="93758-225">安裝已開始。</span><span class="sxs-lookup"><span data-stu-id="93758-225">Installation started.</span></span>

</dd> <dt>

<span data-ttu-id="93758-226"><span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span>**MPNOTIFY \_ SIGUPDATE \_ 安裝 \_ 進度**</span><span class="sxs-lookup"><span data-stu-id="93758-226"><span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span>**MPNOTIFY\_SIGUPDATE\_INSTALL\_PROGRESS**</span></span>
</dt> <dd>

<span data-ttu-id="93758-227">安裝進行中。</span><span class="sxs-lookup"><span data-stu-id="93758-227">Installation in progress.</span></span> <span data-ttu-id="93758-228">回呼資料包含進度。</span><span class="sxs-lookup"><span data-stu-id="93758-228">Callback data contains progress.</span></span>

</dd> <dt>

<span data-ttu-id="93758-229"><span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span>**MPNOTIFY \_ SIGUPDATE \_ 安裝 \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="93758-229"><span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span>**MPNOTIFY\_SIGUPDATE\_INSTALL\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="93758-230">安裝完成。</span><span class="sxs-lookup"><span data-stu-id="93758-230">Installation complete.</span></span>

</dd> <dt>

<span data-ttu-id="93758-231"><span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span>**\_ \_ 需要重新開機 MPNOTIFY SIGUPDATE \_**</span><span class="sxs-lookup"><span data-stu-id="93758-231"><span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span>**MPNOTIFY\_SIGUPDATE\_REBOOT\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="93758-232">更新需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="93758-232">Update requires reboot.</span></span>

</dd> <dt>

<span data-ttu-id="93758-233"><span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span>**已 \_ 處理 MPNOTIFY SIGUPDATE \_ 要求 \_**</span><span class="sxs-lookup"><span data-stu-id="93758-233"><span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span>**MPNOTIFY\_SIGUPDATE\_REQUEST\_PROCESSED**</span></span>
</dt> <dd>

<span data-ttu-id="93758-234">服務已處理簽名更新要求。</span><span class="sxs-lookup"><span data-stu-id="93758-234">Service processed a signature update request.</span></span> <span data-ttu-id="93758-235">回呼資料中的 **hResult** 會指出失敗或成功。</span><span class="sxs-lookup"><span data-stu-id="93758-235">Failure or success is indicated by **hResult** in the callback data.</span></span>

</dd> <dt>

<span data-ttu-id="93758-236"><span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span>**MPNOTIFY \_ SIGUPDATE \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="93758-236"><span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span>**MPNOTIFY\_SIGUPDATE\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="93758-237">更新完成。</span><span class="sxs-lookup"><span data-stu-id="93758-237">Update complete.</span></span> <span data-ttu-id="93758-238">**S \_FALSE** 狀態表示不需要更新。</span><span class="sxs-lookup"><span data-stu-id="93758-238">**S\_FALSE** status indicates that no updates were needed.</span></span>

</dd> <dt>

<span data-ttu-id="93758-239"><span id="MPNOTIFY_SAMPLE_START"></span><span id="mpnotify_sample_start"></span>**MPNOTIFY \_ 範例 \_ 開始**</span><span class="sxs-lookup"><span data-stu-id="93758-239"><span id="MPNOTIFY_SAMPLE_START"></span><span id="mpnotify_sample_start"></span>**MPNOTIFY\_SAMPLE\_START**</span></span>
</dt> <dd>

<span data-ttu-id="93758-240">範例提交已開始。</span><span class="sxs-lookup"><span data-stu-id="93758-240">Sample submission started.</span></span>

</dd> <dt>

<span data-ttu-id="93758-241"><span id="MPNOTIFY_SAMPLE_COMPLETE"></span><span id="mpnotify_sample_complete"></span>**MPNOTIFY \_ 範例 \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="93758-241"><span id="MPNOTIFY_SAMPLE_COMPLETE"></span><span id="mpnotify_sample_complete"></span>**MPNOTIFY\_SAMPLE\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="93758-242">範例提交已完成。</span><span class="sxs-lookup"><span data-stu-id="93758-242">Sample submission completed.</span></span>

</dd> <dt>

<span data-ttu-id="93758-243"><span id="MPNOTIFY_SAMPLE_ITEM_START"></span><span id="mpnotify_sample_item_start"></span>**MPNOTIFY \_ 範例 \_ 專案 \_ 開始**</span><span class="sxs-lookup"><span data-stu-id="93758-243"><span id="MPNOTIFY_SAMPLE_ITEM_START"></span><span id="mpnotify_sample_item_start"></span>**MPNOTIFY\_SAMPLE\_ITEM\_START**</span></span>
</dt> <dd>

<span data-ttu-id="93758-244">已開始提交特定範例專案。</span><span class="sxs-lookup"><span data-stu-id="93758-244">Specific sample item submission started.</span></span> <span data-ttu-id="93758-245">範例專案索引可在 [**MPSAMPLE \_ 資料**](mpsample-data.md)中取得。</span><span class="sxs-lookup"><span data-stu-id="93758-245">Sample item index is available in [**MPSAMPLE\_DATA**](mpsample-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="93758-246"><span id="MPNOTIFY_SAMPLE_ITEM_SUCCEEDED"></span><span id="mpnotify_sample_item_succeeded"></span>**MPNOTIFY \_ 範例 \_ 專案 \_ 成功**</span><span class="sxs-lookup"><span data-stu-id="93758-246"><span id="MPNOTIFY_SAMPLE_ITEM_SUCCEEDED"></span><span id="mpnotify_sample_item_succeeded"></span>**MPNOTIFY\_SAMPLE\_ITEM\_SUCCEEDED**</span></span>
</dt> <dd>

<span data-ttu-id="93758-247">已成功提交特定範例專案。</span><span class="sxs-lookup"><span data-stu-id="93758-247">Specific sample item submission succeeded.</span></span>

</dd> <dt>

<span data-ttu-id="93758-248"><span id="MPNOTIFY_SAMPLE_ITEM_FAILED"></span><span id="mpnotify_sample_item_failed"></span>**MPNOTIFY \_ 範例 \_ 專案 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="93758-248"><span id="MPNOTIFY_SAMPLE_ITEM_FAILED"></span><span id="mpnotify_sample_item_failed"></span>**MPNOTIFY\_SAMPLE\_ITEM\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="93758-249">特定的範例專案提交失敗。</span><span class="sxs-lookup"><span data-stu-id="93758-249">Specific sample item submission failed.</span></span> <span data-ttu-id="93758-250">錯誤碼適用于 [**MPCALLBACK \_ 資料**](mpcallback-data.md)。</span><span class="sxs-lookup"><span data-stu-id="93758-250">Error code is available in [**MPCALLBACK\_DATA**](mpcallback-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="93758-251"><span id="MPNOTIFY_RESERVED_DATA"></span><span id="mpnotify_reserved_data"></span>**MPNOTIFY \_ 保留的 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="93758-251"><span id="MPNOTIFY_RESERVED_DATA"></span><span id="mpnotify_reserved_data"></span>**MPNOTIFY\_RESERVED\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="93758-252">內部保留的資料。</span><span class="sxs-lookup"><span data-stu-id="93758-252">Internal reserved data.</span></span>

</dd> <dt>

<span data-ttu-id="93758-253"><span id="MPNOTIFY_FASTPATH_SIG_ADDED"></span><span id="mpnotify_fastpath_sig_added"></span>**\_ \_ 已新增 MPNOTIFY FASTPATH SIG \_**</span><span class="sxs-lookup"><span data-stu-id="93758-253"><span id="MPNOTIFY_FASTPATH_SIG_ADDED"></span><span id="mpnotify_fastpath_sig_added"></span>**MPNOTIFY\_FASTPATH\_SIG\_ADDED**</span></span>
</dt> <dd>

<span data-ttu-id="93758-254">Fastpath 簽章已新增或停用簽章。</span><span class="sxs-lookup"><span data-stu-id="93758-254">A Fastpath signature has either added or disabled a signature.</span></span>

</dd> <dt>

<span data-ttu-id="93758-255"><span id="MPNOTIFY_FASTPATH_SIG_REMOVED"></span><span id="mpnotify_fastpath_sig_removed"></span>**\_ \_ 已移除 MPNOTIFY FASTPATH SIG \_**</span><span class="sxs-lookup"><span data-stu-id="93758-255"><span id="MPNOTIFY_FASTPATH_SIG_REMOVED"></span><span id="mpnotify_fastpath_sig_removed"></span>**MPNOTIFY\_FASTPATH\_SIG\_REMOVED**</span></span>
</dt> <dd>

<span data-ttu-id="93758-256">已移除 FastPath 簽章。</span><span class="sxs-lookup"><span data-stu-id="93758-256">A FastPath signature has been removed.</span></span>

</dd> <dt>

<span data-ttu-id="93758-257"><span id="MPNOTIFY_NIS_PRIVATE"></span><span id="mpnotify_nis_private"></span>**MPNOTIFY \_ NIS \_ 私用**</span><span class="sxs-lookup"><span data-stu-id="93758-257"><span id="MPNOTIFY_NIS_PRIVATE"></span><span id="mpnotify_nis_private"></span>**MPNOTIFY\_NIS\_PRIVATE**</span></span>
</dt> <dd>

<span data-ttu-id="93758-258">NIS 私用 notifcations。</span><span class="sxs-lookup"><span data-stu-id="93758-258">NIS private notifcations.</span></span> <span data-ttu-id="93758-259">沒有任何夥伴註冊此。</span><span class="sxs-lookup"><span data-stu-id="93758-259">No partners should register for this.</span></span>

</dd> <dt>

<span data-ttu-id="93758-260"><span id="MPNOTIFY_HEALTH_CHANGE"></span><span id="mpnotify_health_change"></span>**MPNOTIFY \_ 健康情況 \_ 變更**</span><span class="sxs-lookup"><span data-stu-id="93758-260"><span id="MPNOTIFY_HEALTH_CHANGE"></span><span id="mpnotify_health_change"></span>**MPNOTIFY\_HEALTH\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="93758-261">AM 服務已進入新的狀態。</span><span class="sxs-lookup"><span data-stu-id="93758-261">The AM service has entered a new state.</span></span>

</dd> <dt>

<span data-ttu-id="93758-262"><span id="MPNOTIFY_HEALTH_RECOVERY"></span><span id="mpnotify_health_recovery"></span>**MPNOTIFY \_ HEALTH \_ RECOVERY**</span><span class="sxs-lookup"><span data-stu-id="93758-262"><span id="MPNOTIFY_HEALTH_RECOVERY"></span><span id="mpnotify_health_recovery"></span>**MPNOTIFY\_HEALTH\_RECOVERY**</span></span>
</dt> <dd>

<span data-ttu-id="93758-263">AM 服務已從狀態復原。</span><span class="sxs-lookup"><span data-stu-id="93758-263">The AM service has recovered from a state.</span></span>

</dd> <dt>

<span data-ttu-id="93758-264"><span id="MPNOTIFY_HEALTH_START"></span><span id="mpnotify_health_start"></span>**MPNOTIFY \_ HEALTH \_ 開始**</span><span class="sxs-lookup"><span data-stu-id="93758-264"><span id="MPNOTIFY_HEALTH_START"></span><span id="mpnotify_health_start"></span>**MPNOTIFY\_HEALTH\_START**</span></span>
</dt> <dd>

<span data-ttu-id="93758-265">AM 服務已初始化系統的健全狀況。</span><span class="sxs-lookup"><span data-stu-id="93758-265">The AM service has initialized the health of the system.</span></span>

</dd> <dt>

<span data-ttu-id="93758-266"><span id="MPNOTIFY_ENDOFLIFE_CHANGE"></span><span id="mpnotify_endoflife_change"></span>**MPNOTIFY \_ ENDOFLIFE \_ 變更**</span><span class="sxs-lookup"><span data-stu-id="93758-266"><span id="MPNOTIFY_ENDOFLIFE_CHANGE"></span><span id="mpnotify_endoflife_change"></span>**MPNOTIFY\_ENDOFLIFE\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="93758-267">AM 服務的「生命週期結束」到期日期已變更。</span><span class="sxs-lookup"><span data-stu-id="93758-267">The "End Of Life" expiry dates for the AM service have changed.</span></span>

</dd> <dt>

<span data-ttu-id="93758-268"><span id="MPNOTIFY_MALWARETOAST_DATA"></span><span id="mpnotify_malwaretoast_data"></span>**MPNOTIFY \_ MALWARETOAST \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="93758-268"><span id="MPNOTIFY_MALWARETOAST_DATA"></span><span id="mpnotify_malwaretoast_data"></span>**MPNOTIFY\_MALWARETOAST\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="93758-269">AM 服務發現惡意程式碼可能導致電腦的重大設定變更。</span><span class="sxs-lookup"><span data-stu-id="93758-269">The AM service has encountered malware that might have caused critical settings change in the machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="93758-270">規格需求</span><span class="sxs-lookup"><span data-stu-id="93758-270">Requirements</span></span>



| <span data-ttu-id="93758-271">需求</span><span class="sxs-lookup"><span data-stu-id="93758-271">Requirement</span></span> | <span data-ttu-id="93758-272">值</span><span class="sxs-lookup"><span data-stu-id="93758-272">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="93758-273">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="93758-273">Minimum supported client</span></span><br/> | <span data-ttu-id="93758-274">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93758-274">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="93758-275">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="93758-275">Minimum supported server</span></span><br/> | <span data-ttu-id="93758-276">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93758-276">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="93758-277">標頭</span><span class="sxs-lookup"><span data-stu-id="93758-277">Header</span></span><br/>                   | <dl> <span data-ttu-id="93758-278"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="93758-278"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93758-279">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93758-279">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93758-280">**MpManagerStatusQueryEx**</span><span class="sxs-lookup"><span data-stu-id="93758-280">**MpManagerStatusQueryEx**</span></span>](mpmanagerstatusqueryex.md)
</dt> <dt>

[<span data-ttu-id="93758-281">**MPCALLBACK \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="93758-281">**MPCALLBACK\_DATA**</span></span>](mpcallback-data.md)
</dt> <dt>

[<span data-ttu-id="93758-282">**MPSAMPLE \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="93758-282">**MPSAMPLE\_DATA**</span></span>](mpsample-data.md)
</dt> </dl>

 

 






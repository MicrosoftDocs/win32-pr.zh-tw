---
description: 下列清單列出 Windows Vista 和更新版本作業系統中的 WMI 記錄檔所支援的事件。
ms.assetid: ad8891cc-0b76-404d-81fc-961bcdbfae32
ms.tgt_platform: multiple
title: WMI 事件訊息
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 543e7131ac0c73a9f1e0f111dafe90197989a33d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979083"
---
# <a name="wmi-event-messages"></a>WMI 事件訊息

下列清單列出 Windows Vista 和更新版本作業系統中的 WMI 記錄檔所支援的事件。

> [!Note]  
> 下列檔是專為開發人員和 IT 系統管理員所設計。 如果您嘗試在家庭系統上解決 WMI 錯誤訊息，請參閱 [Microsoft 支援服務](https://support.microsoft.com/) 網站。

 

<dl> <dt>

<span id="WBEM_MC_REPOSITORY_INCONSISTENT"></span><span id="wbem_mc_repository_inconsistent"></span>**WBEM \_ MC 存放 \_ 庫 \_ 不一致**
</dt> <dd> <dl> <dt>

1073747424 (0x400015E0) 
</dt> <dt>



Windows Management Instrumentation 服務偵測到目錄 *% windir% \\ system32 \\ wbem 存放 \\ 庫* 中的 WMI 存放庫不一致，因此無法加以復原。 現在將刪除 WMI 儲存機制，系統會根據自動復原機制來建立新的存放庫。


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_PROVIDER_SUBSYSTEM_LOCALSYSTEM_PROVIDER_LOAD"></span><span id="wbem_mc_provider_subsystem_localsystem_provider_load"></span>**WBEM \_ MC \_ 提供者 \_ 子系統 \_ LOCALSYSTEM \_ 提供者 \_ 載入**
</dt> <dd> <dl> <dt>

2147483711 (0x8000003F) 
</dt> <dt>



已在 Windows Management Instrumentation 命名空間 %2 中註冊提供者 %1，以使用 LocalSystem 帳戶。 此帳戶具有特殊許可權，如果提供者未正確地模擬使用者要求，則可能會造成安全性違規。


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_MOF_NOT_LOADED_AT_RECOVERY"></span><span id="wbem_mc_mof_not_loaded_at_recovery"></span>**\_ \_ \_ 未 \_ 在復原時載入 \_ \_ WBEM MC MOF**
</dt> <dd> <dl> <dt>

3221225476 (0xC0000004) 
</dt> <dt>



復原時嘗試載入 MOF %2 時，發生錯誤 %1。標記為自動回復的 MOF 檔案。


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_CANNOT_ACTIVATE_FILTER"></span><span id="wbem_mc_cannot_activate_filter"></span>**WBEM \_ MC \_ 無法 \_ 啟動 \_ 篩選**
</dt> <dd> <dl> <dt>

3221225482 (0xC000000A) 
</dt> <dt>



因為發生錯誤 %3，所以無法在命名空間 "%1" 中重新開機具有查詢 "%2" 的事件篩選。 在問題修正之前，無法透過此篩選傳遞事件。


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_INVALID_EVENT_PROVIDER_QUERY"></span><span id="wbem_mc_invalid_event_provider_query"></span>**WBEM \_ MC \_ 不正確 \_ 事件 \_ 提供者 \_ 查詢**
</dt> <dd> <dl> <dt>

3221225493 (0xC0000015) 
</dt> <dt>



事件提供者 %1 嘗試註冊語法不正確查詢 "%2"。 查詢將會被忽略。 您可以使用 CIM studio 檢查 WMI 儲存機制，並更新所列提供者和查詢的永久訂閱，來修正此查詢。 如果永久訂用帳戶是使用隨附于已安裝產品的 MOF 檔案所建立，則必須聯繫應用程式廠商以修正錯誤的註冊。


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_INVALID_EVENT_PROVIDER_INTRINSIC_QUERY"></span><span id="wbem_mc_invalid_event_provider_intrinsic_query"></span>**WBEM \_ MC \_ 不正確 \_ 事件 \_ 提供者 \_ \_ 內建查詢**
</dt> <dd> <dl> <dt>

3221225494 (0xC0000016) 
</dt> <dt>



事件提供者 %1 嘗試在 %3 命名空間中註冊內建事件查詢 "%2"，但無法判斷其目標物件類別集合。 查詢將會被忽略。


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_EVENT_PROVIDER_QUERY_TOO_BROAD"></span><span id="wbem_mc_event_provider_query_too_broad"></span>**WBEM \_ MC \_ 事件 \_ 提供者 \_ 查詢 \_ 過於 \_ 廣泛**
</dt> <dd> <dl> <dt>

3221225495 (0xC0000017) 
</dt> <dt>



事件提供者 %1 嘗試註冊 %3 命名空間中太廣泛的查詢 "%2"。 事件提供者無法提供系統所提供的事件。 查詢將會被忽略。 洽詢應用程式廠商。


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_FOUND"></span><span id="wbem_mc_event_provider_query_not_found"></span>**\_ \_ \_ \_ \_ \_ 找不到 WBEM MC 事件提供者查詢**
</dt> <dd> <dl> <dt>

3221225496 (0xC0000018) 
</dt> <dt>



事件提供者 %1 嘗試註冊的查詢 "%2"，其目標類別 "%3" 在 %4 命名空間不存在。 查詢將會被忽略。


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_EVENT"></span><span id="wbem_mc_event_provider_query_not_event"></span>**WBEM \_ MC \_ 事件 \_ 提供者 \_ 查詢 \_ 不是 \_ 事件**
</dt> <dd> <dl> <dt>

3221225497 (0xC0000019) 
</dt> <dt>



事件提供者 %1 嘗試註冊查詢 &quot; %2， &quot; 其目標類別 &quot; %3 &quot; 不是事件類別。 查詢將會被忽略。 洽詢應用程式廠商。


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_CORE_FAILURE"></span><span id="wbem_mc_wbem_core_failure"></span>**WBEM \_ MC \_ WBEM \_ 核心 \_ 失敗**
</dt> <dd> <dl> <dt>

3221225500 (0xC000001C) 
</dt> <dt>



無法初始化 WMI 核心或提供者子系統或事件子系統，錯誤號碼為 %1。 這可能是因為 WMI 安裝不正確、WMI 存放庫升級失敗、磁碟空間不足或記憶體不足。


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_CONNECTION_FAILURE"></span><span id="wbem_mc_adap_connection_failure"></span>**WBEM \_ MC \_ ADAP \_ 連接 \_ 失敗**
</dt> <dd> <dl> <dt>

3221225515 (0xC000002B) 
</dt> <dt>



Windows Management Instrumentation ADAP 無法連接到命名空間 %1，錯誤： %2。


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_PERFLIB_PUTCLASS_FAILURE"></span><span id="wbem_mc_adap_perflib_putclass_failure"></span>**WBEM \_ MC \_ ADAP \_ PERFLIB \_ PUTCLASS \_ 失敗**
</dt> <dd> <dl> <dt>

3221225520 (0xC0000030) 
</dt> <dt>



Windows Management Instrumentation ADAP 無法在命名空間 %2 中儲存物件 %1，因為發生下列錯誤 %3。


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERF"></span><span id="wbem_mc_adap_unable_to_add_win32perf"></span>**WBEM \_ MC \_ ADAP \_ 無法 \_ \_ 新增 \_ WIN32PERF**
</dt> <dd> <dl> <dt>

3221225530 (0xC000003A) 
</dt> <dt>



Windows Management Instrumentation ADAP 無法 \_ 在 %1 中建立 Win32 效能基底類別：結果 = %2。


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERFRAWDATA"></span><span id="wbem_mc_adap_unable_to_add_win32perfrawdata"></span>**WBEM \_ MC \_ ADAP \_ 無法 \_ \_ 新增 \_ WIN32PERFRAWDATA**
</dt> <dd> <dl> <dt>

3221225531 (0xC000003B) 
</dt> <dt>



Windows Management Instrumentation ADAP 無法建立 Win32 \_ PerfRawData 基類 %1。


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_REPOSITORY_FAILED_TO_START"></span><span id="wbem_mc_repository_failed_to_start"></span>**WBEM \_ MC \_ 存放 \_ 庫 \_ 無法 \_ 啟動**
</dt> <dd> <dl> <dt>

3221231073 (0xC00015E1) 
</dt> <dt>



Windows Management Instrumentation 服務無法在目錄 *% windir% \\ system32 \\ wbem \\ 儲存* 機制下載入存放庫檔案。 這可能是因為存放庫檔案中的損毀、此目錄的安全性設定、磁碟空間不足或其他系統資源問題（例如記憶體不足）所造成。 如果每次電腦重新開機時都發生此錯誤，則這部電腦上的系統管理員可能需要停止 WMI 服務、檢查此資料夾和此資料夾下的檔案的安全性設定，然後執行 WMIDiag 來驗證 Windows Management Instrumentation 的健全狀況。


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_denied"></span>**WBEM \_ MC \_ WBEM \_ 要求 \_ \_ 拒絕加密**
</dt> <dd> <dl> <dt>

3221231077 (0xC00015E5) 
</dt> <dt>



已拒絕存取 %1 命名空間，因為命名空間標記為 RequiresEncryption，但腳本或應用程式嘗試連接到此命名空間，但其驗證等級低於 **Pkt \_ 隱私權**。 將驗證等級變更為 **Pkt \_ 隱私權** ，然後再次執行腳本或應用程式。


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_ASYNC_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_async_denied"></span>**WBEM \_ MC \_ WBEM \_ 需要 \_ 加密 \_ 非同步 \_ 拒絕**
</dt> <dd> <dl> <dt>

3221231078 (0xC00015E6) 
</dt> <dt>



Windows Management Instrumentation 服務無法以非同步方式傳遞 %1 命名空間的結果。 命名空間會以 RequiresEncryption 標示，但 WinMgmt 無法與用戶端電腦建立安全的連線。 請確定用戶端與伺服器電腦之間有信任關係，讓用戶端能夠辨識伺服器電腦帳戶。


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_HOST_KILLED"></span><span id="wbem_mc_wbem_host_killed"></span>**已 \_ 終止 WBEM MC \_ WBEM \_ 主機 \_**
</dt> <dd> <dl> <dt>

3221231084 (0xC00015EC) 
</dt> <dt>



Windows Management Instrumentation 已停止 WMIPRVSE.EXE，因為配額達到警告值。 配額： %1 值： %2 最大值： %3 WMIPRVSE PID： %4。


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REPFILESNOTFOUND"></span><span id="wbem_mc_wbem_repfilesnotfound"></span>**WBEM \_ MC \_ WBEM \_ REPFILESNOTFOUND**
</dt> <dd> <dl> <dt>

3221231086 (0xC00015EE) 
</dt> <dt>



在服務啟動期間，Windows Management Instrumentation 服務無法找到存放庫檔案。 系統會根據自動復原機制來建立新的存放庫。


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_STARTED_SUCESSFULLY"></span><span id="wbem_mc_wbem_started_sucessfully"></span>**\_ \_ \_ 已成功啟動 WBEM MC WBEM \_**
</dt> <dd> <dl> <dt>

3221231087 (0xC00015EF) 
</dt> <dt>



Windows Management Instrumentation 服務已順利啟動。


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_CORE_PSS_ESS_INITIALIZED"></span><span id="wbem_mc_wbem_core_pss_ess_initialized"></span>**WBEM \_ MC \_ WBEM \_ 核心 \_ PSS \_ ESS 已 \_ 初始化**
</dt> <dd> <dl> <dt>

3221231089 (0xC00015F1) 
</dt> <dt>



已成功初始化 Windows Management Instrumentation 服務子系統。


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_SERVICE_INIT_FAILURE"></span><span id="wbem_mc_wbem_service_init_failure"></span>**WBEM \_ MC \_ WBEM \_ 服務 \_ 初始化 \_ 失敗**
</dt> <dd> <dl> <dt>

3221225501 (0xC000001D) 
</dt> <dt>



嘗試初始化 Windows Management Instrumentation 服務時，傳回錯誤號碼 %1。 這可能是因為 WMI 安裝不正確、WMI 存放庫升級失敗、磁碟空間不足或記憶體不足。


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REPOSITORY_RECREATED"></span><span id="wbem_mc_wbem_repository_recreated"></span>**已 \_ 重建 WBEM MC \_ WBEM \_ 儲存 \_ 機制**
</dt> <dd> <dl> <dt>

3221231088 (0xC00015F0) 
</dt> <dt>



已使用自動復原機制成功重新建立 Windows Management Instrumentation 存放庫。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[WMI 事件](wmi-events.md)
</dt> <dt>

[WMI 疑難排解](wmi-troubleshooting.md) \(英文\)
</dt> </dl>

 

 





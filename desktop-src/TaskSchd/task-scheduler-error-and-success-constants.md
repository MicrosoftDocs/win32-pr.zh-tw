---
title: '工作排程器錯誤和成功常數 (Winerror.h) '
description: 如果發生錯誤，工作排程器 Api 可能會傳回下列其中一個錯誤碼作為 HRESULT 值。
ms.assetid: 54278bbd-7dca-438e-a771-5fcb08c4aa68
keywords:
- 工作排程器工作排程器、參考、錯誤和成功常數
topic_type:
- apiref
api_name:
- SCHED_S_TASK_READY
- SCHED_S_TASK_RUNNING
- SCHED_S_TASK_DISABLED
- SCHED_S_TASK_HAS_NOT_RUN
- SCHED_S_TASK_NO_MORE_RUNS
- SCHED_S_TASK_NOT_SCHEDULED
- SCHED_S_TASK_TERMINATED
- SCHED_S_TASK_NO_VALID_TRIGGERS
- SCHED_S_EVENT_TRIGGER
- SCHED_E_TRIGGER_NOT_FOUND
- SCHED_E_TASK_NOT_READY
- SCHED_E_TASK_NOT_RUNNING
- SCHED_E_SERVICE_NOT_INSTALLED
- SCHED_E_CANNOT_OPEN_TASK
- SCHED_E_INVALID_TASK
- SCHED_E_ACCOUNT_INFORMATION_NOT_SET
- SCHED_E_ACCOUNT_NAME_NOT_FOUND
- SCHED_E_ACCOUNT_DBASE_CORRUPT
- SCHED_E_NO_SECURITY_SERVICES
- SCHED_E_UNKNOWN_OBJECT_VERSION
- SCHED_E_UNSUPPORTED_ACCOUNT_OPTION
- SCHED_E_SERVICE_NOT_RUNNING
- SCHED_E_UNEXPECTEDNODE
- SCHED_E_NAMESPACE
- SCHED_E_INVALIDVALUE
- SCHED_E_MISSINGNODE
- SCHED_E_MALFORMEDXML
- SCHED_S_SOME_TRIGGERS_FAILED
- SCHED_S_BATCH_LOGON_PROBLEM
- SCHED_E_TOO_MANY_NODES
- SCHED_E_PAST_END_BOUNDARY
- SCHED_E_ALREADY_RUNNING
- SCHED_E_USER_NOT_LOGGED_ON
- SCHED_E_INVALID_TASK_HASH
- SCHED_E_SERVICE_NOT_AVAILABLE
- SCHED_E_SERVICE_TOO_BUSY
- SCHED_E_TASK_ATTEMPTED
- SCHED_S_TASK_QUEUED
- SCHED_E_TASK_DISABLED
- SCHED_E_TASK_NOT_V1_COMPAT
- SCHED_E_START_ON_DEMAND
api_location:
- WinError.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: a1d0347938020ca8937f2764e3b2c62a38fc9273
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993967"
---
# <a name="task-scheduler-error-and-success-constants"></a>工作排程器錯誤和成功常數

如果發生錯誤，工作排程器 Api 可能會傳回下列其中一個錯誤碼作為 **HRESULT** 值。

以已計畫的開頭的 \_ 常數 \_ 是成功常數，而以已計畫 E 開頭的 \_ 常數 \_ 則是錯誤常數。

```cpp
  HRESULT phrStatus;
  hr = pITask->GetStatus(&phrStatus);
  
  // Release the ITask interface.
  pITask->Release();
    
  switch(phrStatus)
  {
  case SCHED_S_TASK_READY:
       wprintf(L"  SCHED_S_TASK_READY\n");
       break;
  case SCHED_S_TASK_RUNNING:
       wprintf(L"  SCHED_S_TASK_RUNNING\n");
       break;

  //...
  }
```

[C/c + + 程式碼範例：正在](c-c-code-example-retrieving-task-status.md)抓取工作狀態。

> [!Note]  
> 某些工作排程器 Api 可能會傳回 (64 的系統和網路錯誤碼，例如) 。 您可以在 [命令提示字元] 視窗中，使用 **net helpmsg** 命令檢查這些類型之錯誤碼的定義。 例如， **net helpmsg 64** 命令會傳回訊息：指定的網路名稱已無法再使用。

 

如需事件和錯誤訊息的詳細資訊，請參閱 [事件和錯誤訊息中心](https://www.microsoft.com/technet/support/ee/ee_advanced.aspx)。

<dl> <dt>

<span id="SCHED_S_TASK_READY"></span><span id="sched_s_task_ready"></span>**已計畫的工作已 \_ \_ \_ 就緒**
</dt> <dd> <dl> <dt>

0x00041300
</dt> <dt>



工作已準備好在下次排程的時間執行。


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_RUNNING"></span><span id="sched_s_task_running"></span>**已計畫的工作 \_ \_ \_ 正在執行**
</dt> <dd> <dl> <dt>

0x00041301
</dt> <dt>



工作目前正在執行。


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_DISABLED"></span><span id="sched_s_task_disabled"></span>**\_ \_ \_ 已停用已計畫的工作**
</dt> <dd> <dl> <dt>

0x00041302
</dt> <dt>



工作將不會在排程的時間執行，因為它已停用。


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_HAS_NOT_RUN"></span><span id="sched_s_task_has_not_run"></span>**\_已計畫 \_ 的 \_ 工作 \_ 尚未 \_ 執行**
</dt> <dd> <dl> <dt>

0x00041303
</dt> <dt>



尚未執行此工作。


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_NO_MORE_RUNS"></span><span id="sched_s_task_no_more_runs"></span>**已計畫的工作 \_ \_ 不會 \_ 再 \_ \_ 執行**
</dt> <dd> <dl> <dt>

0x00041304
</dt> <dt>



尚未針對此工作排程執行任何執行。


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_NOT_SCHEDULED"></span><span id="sched_s_task_not_scheduled"></span>**\_ \_ \_ 未排程的已 \_ 計畫工作**
</dt> <dd> <dl> <dt>

0x00041305
</dt> <dt>



尚未設定在排程上執行此工作所需的一或多個屬性。


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_TERMINATED"></span><span id="sched_s_task_terminated"></span>**已計畫的工作 \_ \_ \_ 終止**
</dt> <dd> <dl> <dt>

0x00041306
</dt> <dt>



上次執行的工作是由使用者終止。


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_NO_VALID_TRIGGERS"></span><span id="sched_s_task_no_valid_triggers"></span>**已計畫的工作 \_ \_ \_ 沒有 \_ 有效的 \_ 觸發程式**
</dt> <dd> <dl> <dt>

0x00041307
</dt> <dt>



這項工作沒有觸發程式，或現有的觸發程式已停用或未設定。


</dt> </dl> </dd> <dt>

<span id="SCHED_S_EVENT_TRIGGER"></span><span id="sched_s_event_trigger"></span>**已計畫的 \_ S \_ 事件 \_ 觸發程式**
</dt> <dd> <dl> <dt>

0x00041308
</dt> <dt>



事件觸發程式沒有設定執行時間。


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TRIGGER_NOT_FOUND"></span><span id="sched_e_trigger_not_found"></span>**\_ \_ \_ \_ 找不到已計畫的電子觸發程式**
</dt> <dd> <dl> <dt>

0x80041309
</dt> <dt>



找不到工作的觸發程式。


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_NOT_READY"></span><span id="sched_e_task_not_ready"></span>**已計畫的 \_ 電子工作 \_ \_ 未 \_ 就緒**
</dt> <dd> <dl> <dt>

0x8004130A
</dt> <dt>



尚未設定執行此工作所需的一或多個屬性。


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_NOT_RUNNING"></span><span id="sched_e_task_not_running"></span>**已計畫的 \_ 電子工作 \_ \_ 未 \_ 執行**
</dt> <dd> <dl> <dt>

0x8004130B
</dt> <dt>



沒有任何正在執行的工作實例。


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_NOT_INSTALLED"></span><span id="sched_e_service_not_installed"></span>**\_ \_ \_ 未 \_ 安裝已計畫的電子服務**
</dt> <dd> <dl> <dt>

0x8004130C
</dt> <dt>



這部電腦上未安裝工作排程器服務。


</dt> </dl> </dd> <dt>

<span id="SCHED_E_CANNOT_OPEN_TASK"></span><span id="sched_e_cannot_open_task"></span>**已計畫的 \_ 電子 \_ 無法 \_ 開啟 \_ 工作**
</dt> <dd> <dl> <dt>

0x8004130D
</dt> <dt>



無法開啟工作物件。


</dt> </dl> </dd> <dt>

<span id="SCHED_E_INVALID_TASK"></span><span id="sched_e_invalid_task"></span>**已計畫 \_ 電子 \_ 不正確 \_ 工作**
</dt> <dd> <dl> <dt>

0x8004130E
</dt> <dt>



物件可能是不正確工作物件，或不是工作物件。


</dt> </dl> </dd> <dt>

<span id="SCHED_E_ACCOUNT_INFORMATION_NOT_SET"></span><span id="sched_e_account_information_not_set"></span>**未設定已計畫的 \_ 電子 \_ 帳戶 \_ 資訊 \_ \_**
</dt> <dd> <dl> <dt>

0x8004130F
</dt> <dt>



在指定之工作的工作排程器安全性資料庫中，找不到任何帳戶資訊。


</dt> </dl> </dd> <dt>

<span id="SCHED_E_ACCOUNT_NAME_NOT_FOUND"></span><span id="sched_e_account_name_not_found"></span>**\_ \_ \_ \_ \_ 找不到已計畫的電子帳戶名稱**
</dt> <dd> <dl> <dt>

0x80041310
</dt> <dt>



無法建立指定的帳號存在。


</dt> </dl> </dd> <dt>

<span id="SCHED_E_ACCOUNT_DBASE_CORRUPT"></span><span id="sched_e_account_dbase_corrupt"></span>**已計畫的 \_ 電子 \_ 帳戶 \_ DBASE \_ 損毀**
</dt> <dd> <dl> <dt>

0x80041311
</dt> <dt>



在工作排程器安全性資料庫中偵測到損毀;資料庫已重設。


</dt> </dl> </dd> <dt>

<span id="SCHED_E_NO_SECURITY_SERVICES"></span><span id="sched_e_no_security_services"></span>**未計畫的 \_ 電子 \_ \_ 安全性 \_ 服務**
</dt> <dd> <dl> <dt>

0x80041312
</dt> <dt>



工作排程器的安全性服務僅適用于 Windows NT。


</dt> </dl> </dd> <dt>

<span id="SCHED_E_UNKNOWN_OBJECT_VERSION"></span><span id="sched_e_unknown_object_version"></span>**已計畫 \_ 電子 \_ 未知 \_ 物件 \_ 版本**
</dt> <dd> <dl> <dt>

0x80041313
</dt> <dt>



工作物件版本可能不受支援或無效。


</dt> </dl> </dd> <dt>

<span id="SCHED_E_UNSUPPORTED_ACCOUNT_OPTION"></span><span id="sched_e_unsupported_account_option"></span>**已計畫 \_ 電子 \_ 不支援的 \_ 帳戶 \_ 選項**
</dt> <dd> <dl> <dt>

0x80041314
</dt> <dt>



已使用不支援的帳戶設定和執行時間選項群組合來設定工作。


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_NOT_RUNNING"></span><span id="sched_e_service_not_running"></span>**已計畫的 \_ E \_ 服務 \_ 未 \_ 執行**
</dt> <dd> <dl> <dt>

0x80041315
</dt> <dt>



工作排程器服務未執行。


</dt> </dl> </dd> <dt>

<span id="SCHED_E_UNEXPECTEDNODE"></span><span id="sched_e_unexpectednode"></span>**已計畫的 \_ 電子 \_ UNEXPECTEDNODE**
</dt> <dd> <dl> <dt>

0x80041316
</dt> <dt>



工作 XML 包含未預期的節點。


</dt> </dl> </dd> <dt>

<span id="SCHED_E_NAMESPACE"></span><span id="sched_e_namespace"></span>**已計畫的 \_ 電子 \_ 命名空間**
</dt> <dd> <dl> <dt>

0x80041317
</dt> <dt>



工作 XML 包含非預期命名空間中的元素或屬性。


</dt> </dl> </dd> <dt>

<span id="SCHED_E_INVALIDVALUE"></span><span id="sched_e_invalidvalue"></span>**已計畫的 \_ 電子 \_ INVALIDVALUE**
</dt> <dd> <dl> <dt>

0x80041318
</dt> <dt>



工作 XML 包含格式不正確或超出範圍的值。


</dt> </dl> </dd> <dt>

<span id="SCHED_E_MISSINGNODE"></span><span id="sched_e_missingnode"></span>**已計畫的 \_ 電子 \_ MISSINGNODE**
</dt> <dd> <dl> <dt>

0x80041319
</dt> <dt>



工作 XML 缺少必要的元素或屬性。


</dt> </dl> </dd> <dt>

<span id="SCHED_E_MALFORMEDXML"></span><span id="sched_e_malformedxml"></span>**已計畫的 \_ 電子 \_ MALFORMEDXML**
</dt> <dd> <dl> <dt>

0x8004131A
</dt> <dt>



工作 XML 的格式不正確。


</dt> </dl> </dd> <dt>

<span id="SCHED_S_SOME_TRIGGERS_FAILED"></span><span id="sched_s_some_triggers_failed"></span>**已計畫的 \_ \_ 部分 \_ 觸發程式 \_ 失敗**
</dt> <dd> <dl> <dt>

0x0004131B
</dt> <dt>



工作已註冊，但並非所有指定的觸發程式都會啟動工作。


</dt> </dl> </dd> <dt>

<span id="SCHED_S_BATCH_LOGON_PROBLEM"></span><span id="sched_s_batch_logon_problem"></span>**已計畫的 \_ \_ 批次 \_ 登入 \_ 問題**
</dt> <dd> <dl> <dt>

0x0004131C
</dt> <dt>



工作已註冊，但可能無法啟動。 必須啟用工作主體的批次登入許可權。


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TOO_MANY_NODES"></span><span id="sched_e_too_many_nodes"></span>**已計畫的 \_ 電子 \_ \_ 節點太多 \_**
</dt> <dd> <dl> <dt>

0x8004131D
</dt> <dt>



工作 XML 包含太多相同型別的節點。


</dt> </dl> </dd> <dt>

<span id="SCHED_E_PAST_END_BOUNDARY"></span><span id="sched_e_past_end_boundary"></span>**已計畫 \_ E \_ 超過 \_ 結束 \_ 界限**
</dt> <dd> <dl> <dt>

0x8004131E
</dt> <dt>



工作無法在觸發程式結束界限之後啟動。


</dt> </dl> </dd> <dt>

<span id="SCHED_E_ALREADY_RUNNING"></span><span id="sched_e_already_running"></span>**已計畫的 \_ 電子郵件 \_ 已在執行中 \_**
</dt> <dd> <dl> <dt>

0x8004131F
</dt> <dt>



這項工作的實例已經在執行。


</dt> </dl> </dd> <dt>

<span id="SCHED_E_USER_NOT_LOGGED_ON"></span><span id="sched_e_user_not_logged_on"></span>**\_已計畫 \_ 的電子使用者 \_ 未 \_ 登入 \_**
</dt> <dd> <dl> <dt>

0x80041320
</dt> <dt>



工作將不會執行，因為使用者未登入。


</dt> </dl> </dd> <dt>

<span id="SCHED_E_INVALID_TASK_HASH"></span><span id="sched_e_invalid_task_hash"></span>**已計畫 \_ 電子不正確工作 \_ \_ \_ 雜湊**
</dt> <dd> <dl> <dt>

0x80041321
</dt> <dt>



工作映射已損毀或已遭篡改。


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_NOT_AVAILABLE"></span><span id="sched_e_service_not_available"></span>**已計畫的 \_ 電子 \_ 服務 \_ 無法 \_ 使用**
</dt> <dd> <dl> <dt>

0x80041322
</dt> <dt>



工作排程器服務無法使用。


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_TOO_BUSY"></span><span id="sched_e_service_too_busy"></span>**已計畫的 \_ 電子 \_ 服務 \_ 太 \_ 忙碌**
</dt> <dd> <dl> <dt>

0x80041323
</dt> <dt>



工作排程器服務太忙碌，無法處理您的要求。 請稍後再試一次。


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_ATTEMPTED"></span><span id="sched_e_task_attempted"></span>**已計畫的電子工作已 \_ \_ \_ 嘗試**
</dt> <dd> <dl> <dt>

0x80041324
</dt> <dt>



工作排程器服務嘗試執行此工作，但是工作定義中的其中一個條件約束，因此工作並未執行。


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_QUEUED"></span><span id="sched_s_task_queued"></span>**已計畫的工作已 \_ \_ \_ 排入佇列**
</dt> <dd> <dl> <dt>

0x00041325
</dt> <dt>



工作排程器服務要求執行工作。


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_DISABLED"></span><span id="sched_e_task_disabled"></span>**已計畫的 \_ 電子工作 \_ \_ 已停用**
</dt> <dd> <dl> <dt>

0x80041326
</dt> <dt>



工作已停用。


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_NOT_V1_COMPAT"></span><span id="sched_e_task_not_v1_compat"></span>**已計畫的 \_ 電子工作 \_ 不是 \_ \_ V1 \_ 相容性**
</dt> <dd> <dl> <dt>

0x80041327
</dt> <dt>



此工作具有與舊版 Windows 不相容的屬性。


</dt> </dl> </dd> <dt>

<span id="SCHED_E_START_ON_DEMAND"></span><span id="sched_e_start_on_demand"></span>**依 \_ \_ 需求計畫 \_ 的 E 啟動 \_**
</dt> <dd> <dl> <dt>

0x80041328
</dt> <dt>



工作設定不允許工作隨選啟動。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Winerror.h。h</dt> </dl> |



 

 






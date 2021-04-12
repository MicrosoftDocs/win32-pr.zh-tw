---
title: TaskFolder. RegisterTaskDefinition 方法
description: 針對腳本，暫存器 (會使用 TaskDefinition 物件來定義工作，以在指定的位置建立) 工作。
ms.assetid: 198c8848-c89d-4883-b111-4ac0b009b7b3
keywords:
- RegisterTaskDefinition 方法工作排程器
- RegisterTaskDefinition 方法工作排程器，TaskFolder 物件
- TaskFolder 物件工作排程器，RegisterTaskDefinition 方法
topic_type:
- apiref
api_name:
- TaskFolder.RegisterTaskDefinition
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 616d917dd0bb5516fdf8d474d293ba370775c786
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384917"
---
# <a name="taskfolderregistertaskdefinition-method"></a>TaskFolder. RegisterTaskDefinition 方法

針對腳本，暫存器 (會使用 [**TaskDefinition**](taskdefinition.md) 物件來定義工作，以在指定的位置建立) 工作。

## <a name="syntax"></a>語法


```VB
TaskFolder.RegisterTaskDefinition( _
  ByVal path, _
  ByVal definition, _
  ByVal flags, _
  ByVal userId, _
  ByVal password, _
  ByVal logonType, _
  [ ByVal sddl ], _
  ByRef task _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*路徑* \[在\]
</dt> <dd>

工作的名稱。 如果此值為 **Nothing**，則會在根工作資料夾中註冊工作，且工作名稱將會是工作排程器服務所建立的 GUID 值。

工作名稱的開頭或結尾不能是空白字元。 '. ' 字元不能用來指定目前的工作資料夾與 ' ... ' 字元不能用來指定路徑中的父工作資料夾。

</dd> <dt>

*定義* \[在\]
</dt> <dd>

已註冊之工作的定義。

</dd> <dt>

*旗標* \[在\]
</dt> <dd>

工作 [**\_ 建立**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) 常數。



| 值                                                                                                                                                                                                                                                                                 | 意義                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_VALIDATE_ONLY"></span><span id="task_validate_only"></span><dl> <dt>**工作 \_\_僅驗證**</dt> <dt>0x1</dt> </dl>                                                | 工作排程器會檢查描述工作但未註冊工作的 XML 語法。 這個常數無法與工作 **\_ 建立**、工作 **\_ 更新** 或工作 **\_ 建立 \_ 或 \_ 更新** 值結合。<br/>                                                                                                                            |
| <span id="TASK_CREATE"></span><span id="task_create"></span><dl> <dt>**工作 \_建立**</dt> <dt>0x2</dt> </dl>                                                                      | 工作排程器會將工作註冊為新工作。<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TASK_UPDATE"></span><span id="task_update"></span><dl> <dt>**工作 \_UPDATE**</dt> <dt>0x4</dt> </dl>                                                                      | 工作排程器會將工作註冊為現有工作的更新版本。 更新註冊觸發程式的工作時，工作會在更新發生之後執行。<br/>                                                                                                                                                                      |
| <span id="TASK_CREATE_OR_UPDATE"></span><span id="task_create_or_update"></span><dl> <dt>**工作 \_建立 \_ 或 \_ 更新**</dt> <dt>0x6</dt> </dl>                                      | 如果工作已存在，工作排程器會將工作註冊為新工作或更新的版本。 相當於工作 \_ 建立 \| 工作 \_ 更新。<br/>                                                                                                                                                                                              |
| <span id="TASK_DISABLE"></span><span id="task_disable"></span><dl> <dt>**工作 \_停**</dt>用 <dt>0x8</dt> </dl>                                                                   | 工作排程器會停用現有的工作。<br/>                                                                                                                                                                                                                                                                                                           |
| <span id="TASK_DONT_ADD_PRINCIPAL_ACE"></span><span id="task_dont_add_principal_ace"></span><dl> <dt>**工作 \_不要 \_ 新增 \_ 主體 \_ ACE**</dt> <dt>0x10</dt> </dl>                  | 工作排程器無法新增內容主體的允許存取控制專案 (ACE) 。 使用這個旗標來呼叫 **TaskFolder. RegisterTaskDefinition** 函式來更新工作時，工作排程器服務不會為新的內容主體新增 ace，也不會從舊的內容主體移除 ace。<br/> |
| <span id="TASK_IGNORE_REGISTRATION_TRIGGERS"></span><span id="task_ignore_registration_triggers"></span><dl> <dt>**工作 \_忽略 \_ 註冊 \_ 觸發**</dt>程式 <dt>0x20</dt> </dl> | 工作排程器會建立工作，但會忽略工作中的註冊觸發程式。 藉由略過註冊觸發程式，除非以時間為基礎的觸發程式使其在註冊時執行，否則工作將無法在註冊時執行。<br/>                                                                                                         |



 

</dd> <dt>

*userId* \[在\]
</dt> <dd>

用來註冊工作的使用者認證。 如果存在，這些認證會優先于 *定義* 參數所指向的工作定義物件中所指定的認證。

> [!Note]  
> 如果工作定義為工作排程器1.0 工作，則請勿在此 userId 參數中使用組名 (，而不是特定的使用者名稱) 。 當工作設定中的 [ [**相容性**](tasksettings-compatibility.md) ] 屬性設定為 [1] 時，工作就會定義為工作排程器1.0 工作。

 

</dd> <dt>

*密碼* \[在\]
</dt> <dd>

用來註冊工作之 userId 的密碼。 \_使用工作登入 \_ 服務 \_ 帳戶登入類型時，密碼必須是空白的 **變異** 值，例如 **vt \_ Null** 或 **vt \_ 空白**。

</dd> <dt>

*logonType* \[在\]
</dt> <dd>

定義用來執行已註冊工作的登入技巧。



| 值                                                                                                                                                                                                                                                                                                     | 意義                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_LOGON_NONE"></span><span id="task_logon_none"></span><dl> <dt>**工作 \_登入 \_ 無**</dt> <dt>0</dt> </dl>                                                                               | 未指定登入方法。 用於非 NT 認證。 <br/>                                                                                                                                                                                                                           |
| <span id="TASK_LOGON_PASSWORD"></span><span id="task_logon_password"></span><dl> <dt>**工作 \_登入 \_ 密碼**</dt> <dt>1</dt> </dl>                                                                   | 使用密碼來登入使用者。 註冊時必須提供密碼。<br/>                                                                                                                                                                                                |
| <span id="TASK_LOGON_S4U"></span><span id="task_logon_s4u"></span><dl> <dt>**工作 \_登入 \_ S4U**</dt> <dt>2</dt> </dl>                                                                                  | 使用現有的互動式權杖來執行工作。 使用者必須使用服務登入使用者 (S4U) 登入。 使用 S4U 登入時，系統不會儲存任何密碼，也無法存取網路或加密的檔案。<br/>                                             |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN"></span><span id="task_logon_interactive_token"></span><dl> <dt>**工作 \_登入 \_ 互動式 \_ 權杖**</dt> <dt>3</dt> </dl>                                       | 使用者必須已經登入。 此工作只會在現有的互動式會話中執行。<br/>                                                                                                                                                                                              |
| <span id="TASK_LOGON_GROUP"></span><span id="task_logon_group"></span><dl> <dt>**工作 \_登入 \_ 群組**</dt> <dt>4</dt> </dl>                                                                            | 群組啟用。 **GroupId** 欄位會指定群組。<br/>                                                                                                                                                                                                                               |
| <span id="TASK_LOGON_SERVICE_ACCOUNT"></span><span id="task_logon_service_account"></span><dl> <dt>**工作 \_登入 \_ 服務 \_ 帳戶**</dt> <dt>5</dt> </dl>                                             | 表示使用本機系統、本機服務或網路服務帳戶做為執行工作的安全性內容。<br/>                                                                                                                                                              |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD"></span><span id="task_logon_interactive_token_or_password"></span><dl> <dt>**工作 \_登入 \_ 互動式 \_ 權杖 \_ 或 \_ 密碼**</dt> <dt>6</dt> </dl> | 首先使用互動式權杖。 如果使用者未登入 (沒有可使用的互動式權杖) ，則會使用密碼。 註冊工作時必須指定密碼。 因為新的工作比工作登入密碼更可靠，所以不建議使用此旗標 \_ \_ 。<br/> |



 

</dd> <dt>

*sddl* \[在中，選擇性\]
</dt> <dd>

與已註冊工作相關聯的安全描述項。 您可以在工作的安全描述項中指定 (ACL) 的存取控制清單，以允許或拒絕特定使用者和群組對工作的存取。

> [!Note]  
> 如果本機系統帳戶拒絕存取某項工作，工作排程器服務可能會產生非預期的結果。

 

</dd> <dt>

工作 \[擴展\]
</dt> <dd>

代表新工作的 [**RegisteredTask**](registeredtask.md) 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

對於包含訊息方塊動作的工作，如果工作已啟動且工作具有互動式登入類型，就會顯示訊息方塊。 若要將工作登入類型設定為 interactive，請在工作主體的 [**LogonType**](principal-logontype.md)屬性中，或在 [**TaskFolder. RegisterTask**](taskfolder-registertask.md)或 **TaskFolder** 的 *LogonType* 參數中指定 3 (工作登入 **\_ \_ 互動式 \_ 權杖**) 或 4 (工作 **登入 \_ \_ 群組**) 。

只有 Administrators 群組的成員可以建立具有開機觸發程式的工作。

您可以使用 *userId* 參數中所指定的群組來成功註冊工作，並在 [**TaskFolder. RegisterTask**](taskfolder-registertask.md)或 **TaskFolder** 的 *logonType* 參數中指定 3 (工作登入 **互動式) \_ \_ \_ 權杖**，但不會執行該工作。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> <dt>

[**TaskFolder**](taskfolder.md)
</dt> </dl>

 

 






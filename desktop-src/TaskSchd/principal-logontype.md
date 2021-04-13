---
title: Principal. LogonType 屬性
description: 針對腳本，取得或設定執行與主體相關聯之工作所需的安全性登入方法。
ms.assetid: ac6fd7a1-00ef-4478-920f-de391a5a2c8c
keywords:
- LogonType 屬性工作排程器
- LogonType 屬性工作排程器、Principal 物件
- Principal 物件工作排程器，LogonType 屬性
topic_type:
- apiref
api_name:
- Principal.LogonType
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4455fd273144b2d6abd81c78be31a1b037cd889
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465629"
---
# <a name="principallogontype-property"></a>Principal. LogonType 屬性

針對腳本，取得或設定執行與主體相關聯之工作所需的安全性登入方法。

## <a name="syntax"></a>Syntax


```VB
Principal.LogonType As Integer
```



## <a name="property-value"></a>屬性值

設定為下列其中一個工作 [**\_ 登入類型**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type) 列舉常數。



| 值                                                                                                                                                                                                                                                                                                     | 意義                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_LOGON_NONE"></span><span id="task_logon_none"></span><dl> <dt>**工作 \_登入 \_ 無**</dt> <dt>0</dt> </dl>                                                                               | 未指定登入方法。 用於非 NT 認證。 <br/>                                                                                                                                                                                                                           |
| <span id="TASK_LOGON_PASSWORD"></span><span id="task_logon_password"></span><dl> <dt>**工作 \_登入 \_ 密碼**</dt> <dt>1</dt> </dl>                                                                   | 使用密碼來登入使用者。 註冊時必須提供密碼。<br/>                                                                                                                                                                                                |
| <span id="TASK_LOGON_S4U"></span><span id="task_logon_s4u"></span><dl> <dt>**工作 \_登入 \_ S4U**</dt> <dt>2</dt> </dl>                                                                                  | 使用現有的互動式權杖來執行工作。 使用者必須使用服務登入使用者 (S4U) 登入。 使用 S4U 登入時，系統不會儲存任何密碼，也無法存取網路或加密的檔案。<br/>                                                |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN"></span><span id="task_logon_interactive_token"></span><dl> <dt>**工作 \_登入 \_ 互動式 \_ 權杖**</dt> <dt>3</dt> </dl>                                       | 使用者必須已經登入。 此工作只會在現有的互動式會話中執行。<br/>                                                                                                                                                                                              |
| <span id="TASK_LOGON_GROUP"></span><span id="task_logon_group"></span><dl> <dt>**工作 \_登入 \_ 群組**</dt> <dt>4</dt> </dl>                                                                            | 群組啟用。 UserId 欄位會指定群組。<br/>                                                                                                                                                                                                                                    |
| <span id="TASK_LOGON_SERVICE_ACCOUNT"></span><span id="task_logon_service_account"></span><dl> <dt>**工作 \_登入 \_ 服務 \_ 帳戶**</dt> <dt>5</dt> </dl>                                             | 表示使用本機系統、本機服務或網路服務帳戶做為執行工作的安全性內容。<br/>                                                                                                                                                              |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD"></span><span id="task_logon_interactive_token_or_password"></span><dl> <dt>**工作 \_登入 \_ 互動式 \_ 權杖 \_ 或 \_ 密碼**</dt> <dt>6</dt> </dl> | 首先使用互動式權杖。 如果使用者未登入 (沒有可使用的互動式權杖) ，則會使用密碼。 註冊工作時必須指定密碼。 因為新的工作比工作登入密碼更可靠，所以不建議使用此旗標 \_ \_ 。<br/> |



 

## <a name="remarks"></a>備註

只有當使用者識別碼是由 [**UserId**](principal-userid.md) 屬性指定時，這個屬性才有效。

讀取或寫入工作的 XML 時，登入類型會在 [**<LogonType>**](taskschedulerschema-logontype-principaltype-element.md) 工作排程器架構的元素中指定。

對於包含訊息方塊動作的工作，如果工作已啟動且工作具有互動式登入類型，就會顯示訊息方塊。 若要將工作登入類型設定為 interactive，請在工作主體的 **LogonType** 屬性中，或在 [**TaskFolder. RegisterTask**](taskfolder-registertask.md)或 [**TaskFolder**](taskfolder-registertaskdefinition.md)的 *LogonType* 參數中指定 3 (工作登入 **\_ \_ 互動式 \_ 權杖**) 或 4 (工作 **登入 \_ \_ 群組**) 。

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

[**主要**](principal.md)
</dt> </dl>

 

 






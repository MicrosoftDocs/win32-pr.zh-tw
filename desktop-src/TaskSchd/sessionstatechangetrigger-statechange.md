---
title: SessionStateChangeTrigger. StateChange 屬性
description: 針對腳本，取得或設定會觸發工作啟動的終端機伺服器會話變更類型。
ms.assetid: ae1460c7-2939-4fcb-b7fc-edc859596bc4
keywords:
- StateChange 屬性工作排程器
- StateChange 屬性工作排程器，SessionStateChangeTrigger 物件
- SessionStateChangeTrigger 物件工作排程器、StateChange 屬性
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger.StateChange
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfbd2037f19ca2d9fe8ec5d0ba046e69894f431b81d623b61b9474515bcef3a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100158"
---
# <a name="sessionstatechangetriggerstatechange-property"></a>SessionStateChangeTrigger. StateChange 屬性

針對腳本，取得或設定會觸發工作啟動的終端機伺服器會話變更類型。

## <a name="syntax"></a>Syntax


```VB
SessionStateChangeTrigger.StateChange As Integer
```



## <a name="property-value"></a>屬性值

觸發工作以啟動的終端機伺服器會話變更類型。

可能的值來自工作 [**\_ 會話 \_ 狀態 \_ 變更 \_ 類型**](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) 列舉。



| 值                                                                                                                                                                                                                                               | 意義                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_CONSOLE_CONNECT"></span><span id="task_console_connect"></span><dl> <dt>**工作 \_主控台 \_ 連接**</dt> <dt>1</dt> </dl>          | 終端機伺服器主控台連接狀態變更。 例如，當您藉由切換電腦上的使用者，連接到本機電腦上的使用者會話時。 <br/>                           |
| <span id="TASK_CONSOLE_DISCONNECT"></span><span id="task_console_disconnect"></span><dl> <dt>**工作 \_主控台 \_ 中斷**</dt>連線 <dt>2</dt> </dl> | 終端機伺服器主控台中斷連接狀態變更。 例如，當您藉由切換電腦上的使用者，在本機電腦上中斷使用者會話的連線時。<br/>                      |
| <span id="TASK_REMOTE_CONNECT"></span><span id="task_remote_connect"></span><dl> <dt>**工作 \_遠端 \_ 連接**</dt> <dt>3</dt> </dl>             | 終端機伺服器遠端線上狀態變更。 例如，當使用者從遠端電腦使用遠端桌面連線程式連接到使用者會話時。<br/>            |
| <span id="TASK_REMOTE_DISCONNECT"></span><span id="task_remote_disconnect"></span><dl> <dt>**工作 \_遠端 \_ 中斷**</dt>連線 <dt>4</dt> </dl>    | 終端機伺服器遠端中斷連接狀態變更。 例如，當使用者從遠端電腦使用遠端桌面連線程式時，從使用者會話中斷連線。<br/> |
| <span id="TASK_SESSION_LOCK"></span><span id="task_session_lock"></span><dl> <dt>**工作 \_會話 \_ 鎖定**</dt> <dt>7</dt> </dl>                   | 終端機伺服器會話鎖定狀態變更。 例如，此狀態變更會在電腦鎖定時執行工作。 <br/>                                                      |
| <span id="TASK_SESSION_UNLOCK"></span><span id="task_session_unlock"></span><dl> <dt>**工作 \_會話 \_ 解除鎖定**</dt> <dt>8</dt> </dl>             | 終端機伺服器會話已解除鎖定狀態變更。 例如，此狀態變更會在電腦解除鎖定時，讓工作執行。<br/>                                                   |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 






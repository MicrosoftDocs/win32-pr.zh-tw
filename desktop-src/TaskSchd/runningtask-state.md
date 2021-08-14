---
title: RunningTask。 State 屬性
description: 針對腳本，會取得正在執行之工作的狀態識別碼。
ms.assetid: 048863f4-b80b-42ab-bd74-ec761a8f03aa
keywords:
- State 屬性工作排程器
- State 屬性工作排程器，RunningTask 物件
- RunningTask 物件工作排程器，State 屬性
topic_type:
- apiref
api_name:
- RunningTask.State
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e3c83b35c348e3ab86eb04c03ef4c5d25a76ef3fe5040603ce32da54ec4e217
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975038"
---
# <a name="runningtaskstate-property"></a>RunningTask。 State 屬性

針對腳本，會取得正在執行之工作的狀態識別碼。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
RunningTask.State As String
```



## <a name="property-value"></a>屬性值

正在執行之工作的狀態識別碼。



| 值                                                                                                                                                                                                                                   | 意義                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_STATE_UNKNOWN"></span><span id="task_state_unknown"></span><dl> <dt>**工作 \_狀態 \_ 不明**</dt> <dt>0</dt> </dl>    | 工作的狀態未知。<br/>                                                                                                      |
| <span id="TASK_STATE_DISABLED"></span><span id="task_state_disabled"></span><dl> <dt>**工作 \_\_停用狀態**</dt> <dt>1</dt> </dl> | 工作已註冊但已停用，而且沒有工作的實例已排入佇列或正在執行中。 工作必須等到啟用之後才能執行。<br/> |
| <span id="TASK_STATE_QUEUED"></span><span id="task_state_queued"></span><dl> <dt>**工作 \_狀態已 \_ 排入佇列**</dt> <dt>2</dt> </dl>       | 工作的實例已排入佇列。<br/>                                                                                                      |
| <span id="TASK_STATE_READY"></span><span id="task_state_ready"></span><dl> <dt>**工作 \_狀態 \_ 就緒**</dt> <dt>3</dt> </dl>          | 工作已準備好執行，但沒有任何實例已排入佇列或正在執行中。<br/>                                                              |
| <span id="TASK_STATE_RUNNING"></span><span id="task_state_running"></span><dl> <dt>**工作 \_執行 \_**</dt> <dt>4</dt>的狀態 </dl>    | 工作的一或多個實例正在執行。<br/>                                                                                         |



 

## <a name="remarks"></a>備註

[**RunningTask**](runningtask-refresh.md)方法會在傳回屬性值之前呼叫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 






---
title: Action. Type 屬性
description: 針對腳本，會取得動作的類型。
ms.assetid: 6a0bca3d-9016-4167-9f6e-2cc95bafdb95
keywords:
- Type 屬性工作排程器
- Type 屬性工作排程器，Action 物件
- Action 物件工作排程器、Type 屬性
topic_type:
- apiref
api_name:
- Action.Type
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3db8ca46a80503136c5fbbe1240cba6c664bc1a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466037"
---
# <a name="actiontype-property"></a>Action. Type 屬性

針對腳本，會取得動作的類型。

## <a name="syntax"></a>Syntax


```VB
Action.Type As Integer
```



## <a name="property-value"></a>屬性值

這個屬性會傳回下列其中一個 [**工作 \_ 動作 \_ 類型**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) 列舉常數。



| 值                                                                                                                                                                                                                                                   | 意義                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_ACTION_EXEC"></span><span id="task_action_exec"></span><dl> <dt>**工作 \_動作 \_ EXEC**</dt> <dt>0</dt> </dl>                          | 此動作會執行命令列操作。 例如，動作可以執行腳本、啟動可執行檔，或者，如果提供檔的名稱，請尋找其相關聯的應用程式，並使用檔啟動應用程式。<br/> |
| <span id="TASK_ACTION_COM_HANDLER"></span><span id="task_action_com_handler"></span><dl> <dt>**工作 \_ACTION \_ COM \_ 處理常式**</dt> <dt>5</dt> </dl>    | 此動作會引發處理常式。<br/>                                                                                                                                                                                                              |
| <span id="TASK_ACTION_SEND_EMAIL"></span><span id="task_action_send_email"></span><dl> <dt>**工作 \_動作 \_ 傳送 \_ 電子郵件**</dt> <dt>6</dt> </dl>       | 此動作會傳送電子郵件訊息。<br/>                                                                                                                                                                                                       |
| <span id="TASK_ACTION_SHOW_MESSAGE"></span><span id="task_action_show_message"></span><dl> <dt>**工作 \_動作 \_ 顯示 \_ 訊息**</dt> <dt>7</dt> </dl> | 此動作會顯示訊息方塊。<br/>                                                                                                                                                                                                          |



 

## <a name="remarks"></a>備註

動作類型是在建立動作時定義的，而且稍後無法變更。 如需建立動作的詳細資訊，請參閱 [**actioncollection 動作。**](actioncollection-create.md)

如需動作和工作如何一起運作的詳細資訊，請參閱工作 [動作](task-actions.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**工作 \_ 動作 \_ 類型**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> <dt>

[**動作**](action.md)
</dt> </dl>

 

 






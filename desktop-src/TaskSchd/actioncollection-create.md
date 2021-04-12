---
title: Actioncollection 動作. Create 方法
description: 針對腳本，會建立新的動作，並將其加入至集合。
ms.assetid: f33542e1-ee49-4696-b2ab-c48a9b5440d4
keywords:
- 建立方法工作排程器
- 建立方法工作排程器，Actioncollection 動作物件
- Actioncollection 動作物件工作排程器，建立方法
topic_type:
- apiref
api_name:
- ActionCollection.Create
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50ec2ede228a27e753316860ac44e604d39e2e4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508879"
---
# <a name="actioncollectioncreate-method"></a>Actioncollection 動作. Create 方法

針對腳本，會建立新的動作，並將其加入至集合。

## <a name="syntax"></a>語法


```VB
ActionCollection.Create( _
  ByVal type _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*類型* \[在\]
</dt> <dd>

此參數會設定為下列其中一個工作 [**\_ 動作 \_ 類型**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) 列舉常數。



| 值                                                                                                                                                                                                                                                   | 意義                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_ACTION_EXEC"></span><span id="task_action_exec"></span><dl> <dt>**工作 \_動作 \_ EXEC**</dt> <dt>0</dt> </dl>                          | 動作會執行命令列操作。 例如，動作可以執行腳本、啟動可執行檔，或者，如果提供檔的名稱，請尋找其相關聯的應用程式，並使用檔啟動應用程式。<br/> |
| <span id="TASK_ACTION_COM_HANDLER"></span><span id="task_action_com_handler"></span><dl> <dt>**工作 \_ACTION \_ COM \_ 處理常式**</dt> <dt>5</dt> </dl>    | 動作會引發處理常式。<br/>                                                                                                                                                                                                              |
| <span id="TASK_ACTION_SEND_EMAIL"></span><span id="task_action_send_email"></span><dl> <dt>**工作 \_動作 \_ 傳送 \_ 電子郵件**</dt> <dt>6</dt> </dl>       | 此動作會傳送電子郵件訊息。<br/>                                                                                                                                                                                                         |
| <span id="TASK_ACTION_SHOW_MESSAGE"></span><span id="task_action_show_message"></span><dl> <dt>**工作 \_動作 \_ 顯示 \_ 訊息**</dt> <dt>7</dt> </dl> | 此動作會顯示訊息方塊。<br/>                                                                                                                                                                                                         |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

代表新動作的 [**動作**](action.md) 物件。

## <a name="remarks"></a>備註

您無法將32個以上的動作加入至集合。

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

[**Actioncollection 動作**](actioncollection.md)
</dt> <dt>

[**行動**](action.md)
</dt> <dt>

[**ExecAction**](execaction.md)
</dt> <dt>

[**EmailAction**](emailaction.md)
</dt> <dt>

[**ShowMessageAction**](showmessageaction.md)
</dt> <dt>

[**ComHandlerAction**](comhandleraction.md)
</dt> </dl>

 

 






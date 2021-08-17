---
title: 'EventTrigger 物件 (Windows.. h) '
description: 代表觸發程式的腳本物件，此觸發程式會在系統事件發生時啟動工作。
ms.assetid: 79cb6591-0919-441f-ad7f-4eb7cf0f9591
keywords:
- 事件觸發程式工作排程器，物件
- EventTrigger 物件工作排程器
- EventTrigger 物件工作排程器，說明
topic_type:
- apiref
api_name:
- EventTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a355106ee4fcd6756e7aaf59c19664f91204ffb1caae6ebc2dbe45575a5f2ec1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060165"
---
# <a name="eventtrigger-object"></a>EventTrigger 物件

代表觸發程式的腳本物件，此觸發程式會在系統事件發生時啟動工作。

## <a name="members"></a>成員

**EventTrigger** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**EventTrigger** 物件具有這些屬性。



| 屬性                                                            | 存取類型           | 描述                                                                                                                                                                                                                                                                                                                                                                              |
|:--------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**延遲**](eventtrigger-delay.md)<br/>                      | 讀取/寫入<br/> | 取得或設定值，這個值表示發生事件的時間與啟動工作的時間之間的時間長度。<br/>                                                                                                                                                                                                                                                            |
| [**啟用**](trigger-enabled.md)<br/>                       | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定布林值，這個值會指出是否已啟用觸發程式。<br/>                                                                                                                                                                                                                                             |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定停用觸發程式的日期和時間。 觸發程式在停用之後無法啟動工作。<br/>                                                                                                                                                                                              |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定允許執行此觸發程式之工作的最大時間量。<br/>                                                                                                                                                                                                                       |
| [**Id**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定觸發程式的識別碼。<br/>                                                                                                                                                                                                                                                                            |
| [**重複**](trigger-repetition.md)<br/>                 | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定工作的執行頻率，以及啟動工作之後重複模式重複的時間長度。<br/>                                                                                                                                                                                                       |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定啟動觸發程式的日期和時間。<br/>                                                                                                                                                                                                                                                           |
| [**訂用帳戶**](eventtrigger-subscription.md)<br/>        | 讀取/寫入<br/> | 取得或設定 XPath 查詢字串，這個字串會識別引發觸發程式的事件。<br/>                                                                                                                                                                                                                                                                                         |
| [**類型**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | 唯讀<br/>  | 繼承自 [**觸發**](trigger.md) 程式物件。 取得觸發程式的類型。<br/>                                                                                                                                                                                                                                                                                           |
| [**ValueQueries**](eventtrigger-valuequeries.md)<br/>        | 讀取/寫入<br/> | 取得或設定已命名 XPath 查詢的集合。 集合中的每個查詢都會套用至 [**訂閱**](eventtrigger-subscription.md) 屬性中指定之訂閱查詢所傳回的最後一個相符事件 XML。 查詢的名稱可以當做 [**ShowMessageAction**](showmessageaction.md) 動作訊息中的變數使用。<br/> |



 

## <a name="remarks"></a>備註

您可以建立最多500個具有事件訂閱的工作。 針對各種事件進行查詢的事件訂閱，可以用來觸發使用相同動作來回應所記錄事件的工作。

針對工作讀取或撰寫您自己的 XML 時，會使用工作排程器架構的 [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) 元素來指定事件觸發程式。

## <a name="examples"></a>範例

如需此腳本物件的詳細資訊和程式碼範例，請參閱 [事件觸發程式範例 (腳本) ](/previous-versions//aa446887(v=vs.85))。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                         |
| 標頭<br/>                   | <dl> <dt>Windows .xaml.。h</dt> </dl> |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl>      |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**觸發程序**](trigger.md)
</dt> <dt>

[**TriggerCollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection 建立**](triggercollection-create.md)
</dt> </dl>

 


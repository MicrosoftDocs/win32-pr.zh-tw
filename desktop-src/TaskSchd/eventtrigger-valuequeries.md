---
title: EventTrigger. ValueQueries 屬性
description: 針對腳本，取得或設定命名 XPath 查詢的集合。 集合中的每個查詢都會套用至訂閱屬性中指定之訂閱查詢所傳回的最後一個相符事件 XML。
ms.assetid: 9ff92b66-f63c-4736-b086-df7dd8cd2b10
keywords:
- ValueQueries 屬性工作排程器
- ValueQueries 屬性工作排程器，EventTrigger 物件
- EventTrigger 物件工作排程器、ValueQueries 屬性
topic_type:
- apiref
api_name:
- EventTrigger.ValueQueries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f8fd28cd616af56a9b51ecf4e709df5f07674c6d1f307320128645364f3bfc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119253878"
---
# <a name="eventtriggervaluequeries-property"></a>EventTrigger. ValueQueries 屬性

針對腳本，取得或設定命名 XPath 查詢的集合。 集合中的每個查詢都會套用至 [**訂閱**](eventtrigger-subscription.md) 屬性中指定之訂閱查詢所傳回的最後一個相符事件 XML。

## <a name="syntax"></a>Syntax


```VB
EventTrigger.ValueQueries As String
```



## <a name="property-value"></a>屬性值

成對名稱/值的集合。 集合中的每個名稱/值組都會針對觸發事件觸發程式的事件，定義其屬性值的唯一名稱。 事件的屬性值會定義為 XPath 事件查詢。 如需有關 XPath 事件查詢的詳細資訊，請參閱 [事件選取](/previous-versions//aa385231(v=vs.85))。

## <a name="remarks"></a>備註

查詢的名稱可以當做下列動作屬性中的變數使用：

-   [**ShowMessageAction. MessageBody**](showmessageaction-messagebody.md)
-   [**ShowMessageAction 標題**](showmessageaction-title.md)
-   [**ExecAction. 引數**](execaction-arguments.md)
-   [**ExecAction. WorkingDirectory**](execaction-workingdirectory.md)
-   [**EmailAction 伺服器**](emailaction-server.md)
-   [**EmailAction 主題**](emailaction-subject.md)
-   [**EmailAction.To**](emailaction-to.md)
-   [**EmailAction.Cc**](emailaction-cc.md)
-   [**EmailAction 密件副本**](emailaction-bcc.md)
-   [**EmailAction ReplyTo**](emailaction-replyto.md)
-   [**EmailAction**](emailaction-from.md)
-   [**EmailAction**](emailaction-body.md)
-   [**ComHandlerAction 資料**](comhandleraction-data.md)

下列程式碼範例字串顯示可用於名稱/值集合中的兩個名稱值組。 XPath 查詢所傳回的值可以取代動作屬性中的變數。 在 `$(user)` [動作] 屬性中，以 and 的名稱參考這些值 `$(machine)` 。 例如，如果在 `$(user)` `$(machine)` [**ShowMessageAction. MessageBody**](showmessageaction-messagebody.md) 字串中使用和變數，則 XPath 查詢的值會取代字串中的變數。

``` syntax
name: user
value: Event/UserData/SubjectUserName

name: machine
value: Event/UserData/MachineName
```

如需針對特定事件撰寫查詢字串的詳細資訊，請參閱 [事件選取](/previous-versions//aa385231(v=vs.85)) 和 [訂閱事件](../wes/subscribing-to-events.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> <dt>

[**EventTrigger**](eventtrigger.md)
</dt> </dl>

 


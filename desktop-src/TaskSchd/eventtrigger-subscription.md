---
title: EventTrigger. 訂用帳戶屬性
description: 針對腳本，取得或設定查詢字串，以識別引發觸發程式的事件。
ms.assetid: 31d32426-3dd7-41f9-89cc-b13767871b74
keywords:
- 訂用帳戶屬性工作排程器
- 訂用帳戶屬性工作排程器，EventTrigger 物件
- EventTrigger 物件工作排程器，訂用帳戶屬性
topic_type:
- apiref
api_name:
- EventTrigger.Subscription
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68ad05576e248d3ad6c2551a8654a9198ca3c0f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968192"
---
# <a name="eventtriggersubscription-property"></a>EventTrigger. 訂用帳戶屬性

針對腳本，取得或設定查詢字串，以識別引發觸發程式的事件。

## <a name="syntax"></a>Syntax


```VB
EventTrigger.Subscription As String
```



## <a name="property-value"></a>屬性值

識別引發觸發程式之事件的查詢字串。

## <a name="remarks"></a>備註

針對工作讀取或撰寫您自己的 XML 時，會使用工作排程器架構的 [**訂閱**](taskschedulerschema-subscription-eventtriggertype-element.md) 元素來指定事件訂閱。

如需針對特定事件撰寫查詢字串的詳細資訊，請參閱 [事件選取](/previous-versions//aa385231(v=vs.85)) 和 [訂閱事件](../wes/subscribing-to-events.md)。

## <a name="examples"></a>範例

下列查詢字串會定義系統通道中所有層級2事件的訂用帳戶：


```XML
"<QueryList>
    <Query Id='1'>
        <Select Path='System'>*[System/Level=2]</Select>
    </Query>
</QueryList>" 
```



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

[**EventTrigger**](eventtrigger.md)
</dt> </dl>

 


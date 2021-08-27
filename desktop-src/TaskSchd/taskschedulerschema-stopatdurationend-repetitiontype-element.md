---
title: StopAtDurationEnd (repetitionType) 元素
description: 指定在重複模式期間結束時停止執行中的工作實例。
ms.assetid: 4e34b5b2-ac93-4951-9de4-3e89614517d1
keywords:
- StopAtDurationEnd 元素工作排程器
topic_type:
- apiref
api_name:
- StopAtDurationEnd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 896aa6db4ce5bf2c0dddf666024c143754afc97ec76bfb557e6431f593689857
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010538"
---
# <a name="stopatdurationend-repetitiontype-element"></a>StopAtDurationEnd (repetitionType) 元素

指定在重複模式期間結束時停止執行中的工作實例。 這僅適用于已設定重複的情況。

``` syntax
<xs:element name="StopAtDurationEnd"
 type="boolean"
 />
```

**StopAtDurationEnd** 元素是由 [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素

| 元素 | 衍生自 | 描述 |
|-|-|-|
| [**重複**](taskschedulerschema-repetition-triggerbasetype-element.md) | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | 指定執行工作的頻率，以及啟動工作之後重複模式重複的時間長度。<br/> |

## <a name="remarks"></a>備註

針對腳本開發，此設定會使用 [**RepetitionPattern. StopAtDurationEnd**](repetitionpattern-stopatdurationend.md) 屬性來指定。

針對 c + + 開發，此設定會使用 [**IRepetitionPattern：： StopAtDurationEnd**](/windows/win32/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) 屬性來指定。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-|-|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |

## <a name="see-also"></a>另請參閱

[工作排程器架構元素](task-scheduler-schema-elements.md)

[工作排程器](task-scheduler-start-page.md)

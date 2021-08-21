---
description: 導致在特定時間于特定日期產生事件。
ms.assetid: bcb64c81-3b40-4665-a880-a100629656e0
ms.tgt_platform: multiple
title: __AbsoluteTimerInstruction 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __AbsoluteTimerInstruction
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 0797366a95931bec67805c9acd94e52fcab72669fe021efe6907e771a373db46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118821162"
---
# <a name="__absolutetimerinstruction-class"></a>\_\_AbsoluteTimerInstruction 類別

**\_ \_ AbsoluteTimerInstruction** 系統類別會在特定時間產生特定日期的事件。 事件取用者會藉由建立此類別的實例，註冊以接收絕對計時器事件。 事件會產生一次。

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
class __AbsoluteTimerInstruction : __TimerInstruction
{
  datetime EventDateTime;
  boolean  SkipIfPassed = FALSE;
  string   TimerId;
};
```

## <a name="members"></a>成員

**\_ \_ AbsoluteTimerInstruction** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**\_ \_ AbsoluteTimerInstruction** 類別具有這些屬性。

<dl> <dt>

**EventDateTime**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

採用 [DMTF 格式](date-and-time-format.md) 的固定長度字串，可指定計時器引發的時間。

</dd> <dt>

**SkipIfPassed**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 TRUE**，則如果 WMI 無法在正確的時間間隔內產生計時器事件，或要求接收事件的取用者無法使用，就會發生此事件。 若 **為 TRUE**，將不會發生此事件。 預設值為 **FALSE**。 當 WMI 或取用者變成可用時，就會產生並接收通知事件。 這個屬性繼承自 [**\_ \_ TimerInstruction**](--timerinstruction.md)。

<dt>

FALSE
</dt> <dd>

當 WMI 或取用者再次變成可用時，將會產生並接收通知事件。

</dd> <dt>

true
</dt> <dd>

如果 WMI 無法在適當的時間間隔內產生，或要求接收事件的取用者無法使用，就不會發生計時器事件。

</dd> </dl>

</dd> <dt>

**TimerId**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](standard-qualifiers.md)
</dt> </dl>

識別特定計時器事件的唯一使用者指派字串。 為了避免與其他計時器識別碼發生名稱衝突，可以使用分散式運算機環境樣式 GUID 的字串形式。 這個屬性繼承自 [**\_ \_ TimerInstruction**](--timerinstruction.md)。

</dd> </dl>

## <a name="remarks"></a>備註

**\_ \_ AbsoluteTimerInstruction** 類別衍生自 [**\_ \_ TimerInstruction**](--timerinstruction.md)。

WMI 藉由建立 [**\_ \_ TimerEvent**](--timerevent.md)類別的實例來產生絕對計時器事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |
| 命名空間<br/>                | 所有 WMI 命名空間<br/>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**\_\_TimerInstruction**](/windows/desktop/WmiSdk/--timerinstruction)
</dt> <dt>

[WMI 系統類別](wmi-system-classes.md)
</dt> <dt>

[接收計時或重複事件](receiving-a-timed-or-repeating-event.md)
</dt> <dt>

[隨時接收事件](receiving-events-at-all-times.md)
</dt> <dt>

[在您的應用程式期間接收事件](receiving-events-for-the-duration-of-your-application.md)
</dt> </dl>

 


---
description: 指定如何為取用者產生計時器事件的指示。
ms.assetid: b08edb25-bedf-4014-a835-4050f5749479
ms.tgt_platform: multiple
title: __TimerInstruction 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __TimerInstruction
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: d9081cef3ed58929fa976470b1c567c6accd0f60029f64f28ee7a90d16600d2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132011"
---
# <a name="__timerinstruction-class"></a>\_\_TimerInstruction 類別

**\_ \_ TimerInstruction** abstract system 類別指定如何為取用者產生 [計時器事件](receiving-a-timed-or-repeating-event.md)的指示。

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[abstract]
class __TimerInstruction : __EventGenerator
{
  boolean SkipIfPassed = FALSE;
  string  TimerId;
};
```

## <a name="members"></a>成員

**\_ \_ TimerInstruction** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**\_ \_ TimerInstruction** 類別具有這些屬性。

<dl> <dt>

**SkipIfPassed**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述當取用者可供使用時，是否會產生和接收通知事件。

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

識別此特定計時器事件的唯一使用者指派字串。 為了避免與其他計時器識別碼發生名稱衝突，可以使用分散式運算機環境的字串形式 (DCE) 樣式的 GUID。 這個屬性是代表事件的 [**\_ \_ TimerEvent**](--timerevent.md)實例的一部分。

</dd> </dl>

## <a name="remarks"></a>備註

**\_ \_ TimerInstruction** 類別衍生自 [**\_ \_ EventGenerator**](--eventgenerator.md)。

**\_ \_ TimerInstruction** 子類別會 [**\_ \_ AbsoluteTimerInstruction**](--absolutetimerinstruction.md)，供取用者用來註冊絕對計時器事件，以及用來註冊間隔計時器事件的 [**\_ \_ IntervalTimerInstruction**](--intervaltimerinstruction.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |
| 命名空間<br/>                | 所有 WMI 命名空間<br/>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**\_\_EventGenerator**](/windows/desktop/WmiSdk/--eventgenerator)
</dt> <dt>

[WMI 系統類別](wmi-system-classes.md)
</dt> </dl>

 


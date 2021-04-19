---
description: 報告 WMI 產生的事件，以回應間隔計時器事件或絕對計時器事件的取用者要求。
ms.assetid: 5ae29312-cfda-42c9-a154-e5bb31819be0
ms.tgt_platform: multiple
title: __TimerEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __TimerEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 2de8967110568e968bb241ebbf4942bf1504b332
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975335"
---
# <a name="__timerevent-class"></a>\_\_TimerEvent 類別

**\_ \_ TimerEvent** 系統類別會報告 WMI 產生的事件，以回應取用者對間隔計時器事件或絕對計時器事件的要求。 間隔計時器事件是定期發生的事件。 絕對計時器事件是在特定時間發生的事件。 計時器事件可能會發生在任何命名空間中。

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
class __TimerEvent : __Event
{
  uint32 NumFirings;
  uint8  SECURITY_DESCRIPTOR[];
  string TimerId;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>成員

**\_ \_ TimerEvent** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**\_ \_ TimerEvent** 類別具有這些屬性。

<dl> <dt>

**NumFirings**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

在通知傳遞給取用者之前，事件發生的次數。

</dd> <dt>

**安全 \_ 描述項**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

事件提供者用來判斷哪些使用者可以接收事件的描述項。 這個屬性繼承自 [**\_ \_ 事件**](--event.md)。

</dd> <dt>

**\_建立時間**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

唯一值，指出產生事件的時間。 這是64位值，代表1601年1月1日之後的 100-毫微秒間隔數目。 此資訊採用國際標準時間 (UTC) 格式。 這個屬性繼承自 [**\_ \_ 事件**](--event.md)。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。

</dd> <dt>

**TimerId**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

導致 WMI 引發這個事件的 [**\_ \_ TimerInstruction**](--timerinstruction.md)子類別的實例。 取用者會在其所建立的 **\_ \_ TimerInstruction** 子類別的 **TimerId** 屬性中指定計時器識別，以進行註冊。

</dd> </dl>

## <a name="remarks"></a>備註

**\_ \_ TimerEvent** 類別衍生自 [**\_ \_ Event**](--event.md)。

事件取用者會藉由建立 [**\_ \_ AbsoluteTimerInstruction**](--absolutetimerinstruction.md)系統類別的實例來註冊絕對計時器事件。 他們會藉由建立 [**\_ \_ IntervalTimerInstruction**](--intervaltimerinstruction.md)系統類別的實例來註冊間隔計時器事件。

在正常操作期間， **NumFirings** 屬性會設定為1。 如果無法觸達取用者或引發間隔的速度遠高於傳遞事件的能力， **NumFirings** 會設為大於1的數位。 當 **NumFirings** 大於1時，WMI 會自動將許多計時器事件彙總成相同的事件。 這項合併類似于在 Windows 程式設計中使用 [**WM \_ 計時器**](/windows/desktop/winmsg/wm-timer) 訊息時所發生的情況。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |
| 命名空間<br/>                | 所有 WMI 命名空間<br/>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**\_\_事件**](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[WMI 系統類別](wmi-system-classes.md)
</dt> <dt>

[接收計時或重複事件](receiving-a-timed-or-repeating-event.md)
</dt> <dt>

[隨時接收事件](receiving-events-at-all-times.md)
</dt> <dt>

[在您的應用程式期間接收事件](receiving-events-for-the-duration-of-your-application.md)
</dt> </dl>

 


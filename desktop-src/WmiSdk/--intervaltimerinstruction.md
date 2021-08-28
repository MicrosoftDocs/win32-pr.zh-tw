---
description: 依時間間隔產生事件，類似于 \_ Windows 程式設計中的 WM 計時器訊息。
ms.assetid: 0895a743-a0dd-4833-a2bf-0196369e18b9
ms.tgt_platform: multiple
title: __IntervalTimerInstruction 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __IntervalTimerInstruction
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 17f0c55edceb3c5fb009f49ae97e3765ec3e0255a82f8c75e133344379c24d90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640758"
---
# <a name="__intervaltimerinstruction-class"></a>\_\_IntervalTimerInstruction 類別

**\_ \_ IntervalTimerInstruction** 系統類別會依間隔產生事件，類似于 Windows 程式 \_ 設計中的 WM 計時器訊息。 事件取用者會藉由建立參考此類別的事件查詢，來註冊接收間隔計時器事件。 由於作業系統行為的緣故，因此不保證事件會精確地以要求的間隔傳遞。

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
class __IntervalTimerInstruction : __TimerInstruction
{
  uint32  IntervalBetweenEvents;
  boolean SkipIfPassed = FALSE;
  string  TimerId;
};
```

## <a name="members"></a>成員

**\_ \_ IntervalTimerInstruction** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**\_ \_ IntervalTimerInstruction** 類別具有這些屬性。

<dl> <dt>

**IntervalBetweenEvents**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](standard-qualifiers.md) (毫秒) 
</dt> </dl>

事件引發之間的毫秒數。

</dd> <dt>

**SkipIfPassed**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 TRUE**，則會略過此事件（如果已通過間隔）。 預設值為 **FALSE**。 這個屬性繼承自 [**\_ \_ TimerInstruction**](--timerinstruction.md)。

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

這個 **\_ \_ IntervalTimerInstruction** 物件的唯一識別碼。 這個屬性繼承自 [**\_ \_ TimerInstruction**](--timerinstruction.md)。

</dd> </dl>

## <a name="remarks"></a>備註

**\_ \_ IntervalTimerInstruction** 類別衍生自 [**\_ \_ TimerInstruction**](--timerinstruction.md)。

輸入以註冊間隔計時器事件的事件查詢，通常是以 **TimerId** 屬性為基礎。 從間隔計時器事件產生的通知事件包含屬性 **NumFirings** ，其中包含的資料會反映無法接收事件時所引發的事件數目。 如果 **SkipIfPassed** 設定為 **TRUE**，則會捨棄該資訊。

**IntervalBetweenEvents** 屬性的值應該相當大。 如果太小，WMI 可能會忽略它，而不會因為某些作業系統的限制而產生事件。

WMI 藉由建立 [**\_ \_ TimerEvent**](--timerevent.md)類別的實例來產生間隔計時器事件。

若要在暫存事件取用者中接收這些計時器事件，請使用下列事件查詢字串來執行 [**IWbemServices：： ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) ：


```sql
SELECT * FROM __TimerEvent WHERE TimerID = "MyEvent"
```



若要在永久事件取用者中接收這些計時器事件，您必須將先前的查詢載入事件篩選器、定義邏輯取用者，以及為篩選和取用者建立篩選至取用者系結。 如需詳細資訊，請參閱 [所有時間的接收事件](receiving-events-at-all-times.md)。

## <a name="examples"></a>範例

下列 MOF 宣告顯示如何產生間隔計時器事件，其索引鍵屬性每10秒設定為 "MyEvent"：


```mof
instance of __IntervalTimerInstruction
{
  TimerId = "MyEvent";     // inherited from __TimerInstruction
  SkipIfPassed = FALSE;    // also inherited
  IntervalBetweenEvents = 10000;
};
```



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
</dt> </dl>

 


---
description: 報告因為傳遞佇列溢位而捨棄事件。
ms.assetid: 7cb1ef3b-3b0a-4f72-96de-862022fd6db8
ms.tgt_platform: multiple
title: __EventQueueOverflowEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventQueueOverflowEvent
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 058b03b8a3311aad805f47a04d20e9f1fa8c2477
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994504"
---
# <a name="__eventqueueoverflowevent-class"></a>\_\_EventQueueOverflowEvent 類別

**\_ \_ EventQueueOverflowEvent** 系統類別會報告因為傳遞佇列溢位而卸載事件的時機。

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
class __EventQueueOverflowEvent : __EventDroppedEvent
{
  uint32              CurrentQueueSize;
  object              Event;
  __EventConsumer REF IntendedConsumer;
  uint8               SECURITY_DESCRIPTOR[];
  uint64              TIME_CREATED;
};
```

## <a name="members"></a>成員

**\_ \_ EventQueueOverflowEvent** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**\_ \_ EventQueueOverflowEvent** 類別具有這些屬性。

<dl> <dt>

**CurrentQueueSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

目前的佇列大小（以位元組為單位）。 所有結合的佇列，這個屬性的預設值為 10 MB。

</dd> <dt>

**事件**
</dt> <dd> <dl> <dt>

資料類型： **物件**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

感興趣的事件。 這個屬性繼承自 [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md)。

</dd> <dt>

**IntendedConsumer**
</dt> <dd> <dl> <dt>

資料類型： **\_ \_ EventConsumer**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

預定取用者的參考。 這個屬性繼承自 [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md)。

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

唯一值，指出產生事件的時間。 這是64位值，代表1601年1月1日之後的 100-毫微秒間隔數目。 這項資訊是 (UTC) 格式的國際標準時間。 這個屬性繼承自 [**\_ \_ 事件**](--event.md)。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。

</dd> </dl>

## <a name="remarks"></a>備註

只有具備系統管理員許可權的使用者能夠收到此事件。 **\_ \_ EventQueueOverflowEvent** 類別衍生自 [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md)。

如需詳細資訊，請參閱 [**\_ \_ EventConsumer**](--eventconsumer.md)類別中的 [**MaximumQueueSize**](--eventconsumer.md)屬性和 **Win32 \_ WMISetting** 類別中的 [**HighThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting)屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |
| 命名空間<br/>                | 所有 WMI 命名空間<br/>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**\_\_EventDroppedEvent**](/windows/desktop/WmiSdk/--eventdroppedevent)
</dt> <dt>

[WMI 系統類別](wmi-system-classes.md)
</dt> </dl>

 


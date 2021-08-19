---
description: 表示已卸載之事件的發生次數。 卸載的事件是未傳遞給事件取用者的事件。
ms.assetid: fae267a9-e0ec-43fa-a3c3-d50345775a1d
ms.tgt_platform: multiple
title: __EventDroppedEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventDroppedEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 695381a3471dcc744cae10622ee9e7935b2770941a770bd0e4e4e93e591a9220
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051086"
---
# <a name="__eventdroppedevent-class"></a>\_\_EventDroppedEvent 類別

**\_ \_ EventDroppedEvent** 系統類別代表已卸載之事件的發生次數。 卸載的事件是未傳遞給事件取用者的事件。

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
class __EventDroppedEvent : __SystemEvent
{
  __Event             Event;
  __EventConsumer REF IntendedConsumer;
  uint8               SECURITY_DESCRIPTOR[];
  uint64              TIME_CREATED;
};
```

## <a name="members"></a>成員

**\_ \_ EventDroppedEvent** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**\_ \_ EventDroppedEvent** 類別具有這些屬性。

<dl> <dt>

**事件**
</dt> <dd> <dl> <dt>

資料類型： **\_ \_ 事件**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

丟棄的事件。

</dd> <dt>

**IntendedConsumer**
</dt> <dd> <dl> <dt>

資料類型： **\_ \_ EventConsumer**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

[**\_ \_ EventConsumer**](--eventconsumer.md)實例的參考，代表您識別用來接收事件的永久取用者。 訂閱事件的不同永久取用者可以繼續接收事件。

</dd> <dt>

**安全 \_ 描述項**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

事件提供者用來判斷可以接收事件之使用者的描述項。 這個屬性繼承自 [**\_ \_ 事件**](--event.md)。

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

**\_ \_ EventDroppedEvent** 類別衍生自 [**\_ \_ SystemEvent**](--systemevent.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |
| 命名空間<br/>                | 所有 WMI 命名空間<br/>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**\_\_SystemEvent**](/windows/desktop/WmiSdk/--systemevent)
</dt> <dt>

[WMI 系統類別](wmi-system-classes.md)
</dt> </dl>

 


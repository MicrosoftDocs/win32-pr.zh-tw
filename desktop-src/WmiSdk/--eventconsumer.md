---
description: 是用來註冊永久事件取用者的抽象基類。
ms.assetid: c1dc9a91-76f9-4527-ad69-0323a9aef28a
ms.tgt_platform: multiple
title: __EventConsumer 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventConsumer
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: ba84549f1120f4f6d2045e9e9c999e56c38dd285e2ab25de5da1e1b12401f345
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120948"
---
# <a name="__eventconsumer-class"></a>\_\_EventConsumer 類別

**\_ \_ EventConsumer** 系統類別是用來註冊永久事件取用者的抽象基類。 您可以從 **\_ \_ EventConsumer** 衍生新的事件取用者類別。

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[abstract]
class __EventConsumer : __IndicationRelated
{
  uint8  CreatorSID[];
  string MachineName;
  uint32 MaximumQueueSize;
};
```

## <a name="members"></a>成員

**\_ \_ EventConsumer** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**\_ \_ EventConsumer** 類別具有這些屬性。

<dl> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

安全識別碼 (SID) ，可唯一識別建立篩選的使用者。 根據作業系統而定，WMI 會儲存建立 **\_ \_ EventConsumer** 實例或系統管理員 SID 之使用者的 SID。 如需詳細資訊，請參閱使用邏輯取用者來系結 [事件篩選器](binding-an-event-filter-with-a-logical-consumer.md) ，以及 [使用標準取用者來監視和回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

Windows Management Instrumentation (WMI) 傳送事件的電腦名稱稱。

</dd> <dt>

**MaximumQueueSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

特定取用者的佇列上限，以位元組為單位。

</dd> </dl>

## <a name="remarks"></a>備註

**\_ \_ EventConsumer** 類別衍生自 [**\_ \_ IndicationRelated**](--indicationrelated.md)，但沒有屬性。

永久取用者會定義新的取用者類別，以描述取用者接收事件通知時要採取的動作以及要處理的資料。 永久取用者有特殊的安全性考慮。 如需詳細資訊，請參閱 [保護 WMI 事件](securing-wmi-events.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |
| 命名空間<br/>                | 所有 WMI 命名空間<br/>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**\_\_IndicationRelated**](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[WMI 系統類別](wmi-system-classes.md)
</dt> <dt>

[隨時接收事件](receiving-events-at-all-times.md)
</dt> <dt>

[建立新的永久事件取用者類別](creating-a-new-permanent-event-consumer-class.md)
</dt> <dt>

[建立邏輯取用者](creating-a-logical-consumer.md)
</dt> <dt>

[保護 WMI 事件](securing-wmi-events.md)
</dt> </dl>

 


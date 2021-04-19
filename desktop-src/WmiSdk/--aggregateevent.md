---
description: 代表數個個別內建或外來事件的匯總事件。
ms.assetid: 99afa390-01fe-4a13-ba21-27587470f111
ms.tgt_platform: multiple
title: __AggregateEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __AggregateEvent
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: f93a962e57452ac555214e42f00af8ac8a4ea3db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975274"
---
# <a name="__aggregateevent-class"></a>\_\_AggregateEvent 類別

**\_ \_ AggregateEvent** 系統類別代表數個個別內建或外來事件的匯總事件。 當取用者向其事件查詢中的 [group](group-clause.md) in 子句註冊時，WMI 會產生 **\_ \_ AggregateEvent** 的實例，而不是 [**\_ \_ 事件**](--event.md)。

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
class __AggregateEvent : __IndicationRelated
{
  uint32 NumberOfEvents;
  object Representative;
};
```

## <a name="members"></a>成員

**\_ \_ AggregateEvent** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**\_ \_ AggregateEvent** 類別具有這些屬性。

<dl> <dt>

**NumberOfEvents**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

合併以產生這個單一摘要事件的事件數目。

</dd> <dt>

**Representative**
</dt> <dd> <dl> <dt>

資料類型： **物件**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

匯總間隔內傳遞的其中一個事件的複本。 例如，如果取用者已從登錄事件提供者註冊登錄機碼變更事件， **代表** 會保留 **RegistryKeyChangeEvent** 類別的實例。

</dd> </dl>

## <a name="remarks"></a>備註

**\_ \_ AggregateEvent** 類別衍生自 [**\_ \_ IndicationRelated**](--indicationrelated.md)，但沒有屬性。

事件提供者永遠不會產生匯總事件。 它們必須在處理事件查詢時，忽略子句內的群組。

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

[使用 WQL 查詢](querying-with-wql.md)
</dt> </dl>

 


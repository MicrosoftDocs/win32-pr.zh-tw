---
description: 是抽象基類，作為所有內建和外建事件的父類別。
ms.assetid: 4d2e4715-041c-49e9-b948-a148dfe85483
ms.tgt_platform: multiple
title: __Event 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Event
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: a74abb8a02676ba97ffb7a41df6ee4a3bd7f428d5288e376f85d61927fbb0e06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118821088"
---
# <a name="__event-class"></a>\_\_事件類別

**\_ \_ 事件** 系統類別是一個抽象基類，做為所有內建和外來事件的父類別。 所有新的事件種類最終都必須衍生自 **\_ \_ 事件**。 內部事件直接衍生自這個類別。 使用者定義的外建事件是衍生自這個類別的子類別，稱為 [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md)。

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[abstract]
class __Event : __IndicationRelated
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>成員

**\_ \_ 事件** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**\_ \_ 事件** 類別具有這些屬性。

<dl> <dt>

**安全 \_ 描述項**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

事件提供者用來判斷哪些使用者可以接收事件的描述項。 如需詳細資訊，請參閱 [WMI 安全性常數](wmi-security-constants.md)。

</dd> <dt>

**\_建立時間**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出事件產生時間的唯一值。 這是64位值，代表1601年1月1日之後的 100-毫微秒間隔數目。 這項資訊是 (UTC) 格式的國際標準時間。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。

</dd> </dl>

## <a name="remarks"></a>備註

**\_ \_ 事件** 類別衍生自沒有屬性的 [**\_ \_ IndicationRelated**](--indicationrelated.md)。

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

[判斷要接收的事件種類](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[**\_\_ClassOperationEvent**](--classoperationevent.md)
</dt> <dt>

[**\_\_InstanceOperationEvent**](--instanceoperationevent.md)
</dt> <dt>

[**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md)
</dt> </dl>

 


---
description: 報告命名空間建立事件，這是將新的命名空間新增至目前的命名空間時所產生的內建事件種類。
ms.assetid: 50b9860a-d6e8-4dab-a7d0-09da9dd37b6b
ms.tgt_platform: multiple
title: __NamespaceCreationEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceCreationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 2f84e0c584d3afb63b166523a5920d4d5b3367638bc0000c33a8cfba979e64c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320722"
---
# <a name="__namespacecreationevent-class"></a>\_\_NamespaceCreationEvent 類別

**\_ \_ NamespaceCreationEvent** 系統類別會報告命名空間建立事件，這是將新的命名空間新增至目前的命名空間時所產生的內建 [事件](determining-the-type-of-event-to-receive.md)類型。

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
class __NamespaceCreationEvent : __NamespaceOperationEvent
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a>成員

**\_ \_ NamespaceCreationEvent** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**\_ \_ NamespaceCreationEvent** 類別具有這些屬性。

<dl> <dt>

**安全 \_ 描述項**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

事件提供者用來判斷哪些使用者可以接收事件的描述項。 這個屬性繼承自 [**\_ \_ 事件**](--event.md)。

</dd> <dt>

**TargetNamespace**
</dt> <dd> <dl> <dt>

資料類型： **\_ \_ 命名空間**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

已建立之 [**\_ \_ 命名空間**](--namespace.md)實例的複本。 **\_ \_ 命名空間** 實例的 **Name** 屬性會指出已建立的命名空間。 這個屬性繼承自 [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md)。

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

**\_ \_ NamespaceCreationEvent** 類別衍生自 [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |
| 命名空間<br/>                | 所有 WMI 命名空間<br/>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**\_\_NamespaceOperationEvent**](/windows/desktop/WmiSdk/--namespaceoperationevent)
</dt> <dt>

[WMI 系統類別](wmi-system-classes.md)
</dt> </dl>

 


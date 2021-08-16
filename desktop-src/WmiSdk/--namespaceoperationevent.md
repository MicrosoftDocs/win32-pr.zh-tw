---
description: 所有與命名空間相關之內建事件的基類。
ms.assetid: 168637b1-217e-4b6d-bd07-25127b9e9f6c
ms.tgt_platform: multiple
title: __NamespaceOperationEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceOperationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: b5293f97eed0716b3add1d5f06513d556355b157d8e594b1f9e55cb8df6ca7ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320620"
---
# <a name="__namespaceoperationevent-class"></a>\_\_NamespaceOperationEvent 類別

**\_ \_ NamespaceOperationEvent** 系統類別是所有與命名空間相關之內建事件的基類。

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
class __NamespaceOperationEvent : __Event
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a>成員

**\_ \_ NamespaceOperationEvent** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**\_ \_ NamespaceOperationEvent** 類別具有這些屬性。

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

受事件影響的命名空間。 針對建立事件，這是新建立的命名空間。 針對修改事件，這是已變更的命名空間。 如果是刪除事件，這就是已刪除的命名空間。

</dd> <dt>

**\_建立時間**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

唯一值，指出產生事件的時間。 這是64位值，代表1601年1月1日之後的 100-毫微秒間隔數目。 此資訊採用國際標準時間 (UTC) 格式。 這個屬性繼承自 [**\_ \_ 事件**](--event.md)。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。

</dd> </dl>

## <a name="remarks"></a>備註

**\_ \_ NamespaceOperationEvent** 類別衍生自 [**\_ \_ Event**](--event.md)。

不會建立這個類別的實例。 WMI 會建立下列其中一個衍生自這個類別的類別實例：

[**\_\_NamespaceCreationEvent**](--namespacecreationevent.md)

[**\_\_NamespaceModificationEvent**](--namespacemodificationevent.md)

[**\_\_NamespaceDeletionEvent**](--namespacedeletionevent.md)

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

[判斷要接收的事件種類](determining-the-type-of-event-to-receive.md)
</dt> </dl>

 


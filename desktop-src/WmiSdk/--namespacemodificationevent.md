---
description: 報告命名空間修改事件，這是在修改命名空間時所產生的內建事件種類。
ms.assetid: 168505d7-4677-4f41-935e-149f22de2cb5
ms.tgt_platform: multiple
title: __NamespaceModificationEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceModificationEvent
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 3243afe0a8cae34e83ad85e2d89a3becab8d07775ba3ec0c3283fd4ea8ed8bbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557811"
---
# <a name="__namespacemodificationevent-class"></a>\_\_NamespaceModificationEvent 類別

**\_ \_ NamespaceModificationEvent** 系統類別會報告命名空間修改事件，這是在修改命名空間時所產生的內建 [事件](determining-the-type-of-event-to-receive.md)類型。

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
class __NamespaceModificationEvent : __NamespaceOperationEvent
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace PreviousNamespace;
  uint8       SECURITY_DESCRIPTOR [];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a>成員

**\_ \_ NamespaceModificationEvent** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**\_ \_ NamespaceModificationEvent** 類別具有這些屬性。

<dl> <dt>

**PreviousNamespace**
</dt> <dd> <dl> <dt>

資料類型： **\_ \_ 命名空間**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

[**\_ \_ 命名空間**](--namespace.md)實例的原始版本複本。 這個實例的 **Name** 屬性會識別修改過的命名空間。

</dd> <dt>

**安全 \_ 描述項**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

事件提供者用來判斷哪些使用者可以接收事件的描述項。 這個屬性繼承自 [**\_ \_ 事件**](--event.md)。

</dd> <dt>

**安全 \_ 描述項** 
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

事件提供者用來判斷可接收事件之使用者的描述項。 這個屬性繼承自 [**\_ \_ 事件**](--event.md)。

> [!Note]  
> 在 [**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)中 (ACL) 的 **Null** 存取控制清單會將無限存取權授與所有人。 如需詳細資訊，請參閱 [建立新物件的安全描述項](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--)。

 

</dd> <dt>

**TargetNamespace**
</dt> <dd> <dl> <dt>

資料類型： **\_ \_ 命名空間**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

已修改之 [**\_ \_ 命名空間**](--namespace.md)實例的複本。 **\_ \_ 命名空間** 實例的 **Name** 屬性，表示修改過的命名空間。 這個屬性繼承自類別 [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md)。

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

**\_ \_ NamespaceModificationEvent** 類別衍生自 [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md)。

目標命名空間和先前命名空間之間的唯一差異，在於 [**名稱**](--namespace.md)以外的限定詞和屬性。

請注意， **\_ \_ 命名空間** 實例的 [**Name**](--namespace.md)屬性無法變更，因為命名空間無法重新命名。 若要修改命名空間的名稱，必須刪除 **\_ \_ 命名空間** 實例，並使用新名稱重新建立。 因此，當 **名稱** 以外的限定詞和屬性發生變更時，就會產生命名空間修改事件。 命名空間中發生任何類型的變更時，不會產生命名空間修改事件。 只有在修改命名空間實例時，才會產生命名空間修改事件。

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

 


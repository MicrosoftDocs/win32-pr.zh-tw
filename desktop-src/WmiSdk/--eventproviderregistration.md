---
description: 用來向 Windows Management Instrumentation (WMI) 註冊事件提供者。
ms.assetid: d87f61a8-5549-4f33-ba67-31b5d72b5282
ms.tgt_platform: multiple
title: __EventProviderRegistration 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventProviderRegistration
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: caaad1b4ab03cfc1b43e4239b9144d3ceeade82f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994385"
---
# <a name="__eventproviderregistration-class"></a>\_\_EventProviderRegistration 類別

**\_ \_ EventProviderRegistration** 系統類別可用來向 Windows Management Instrumentation (WMI) 註冊事件提供者。

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
class __EventProviderRegistration : __ProviderRegistration
{
  string         EventQueryList[];
  __Provider REF provider;
};
```

## <a name="members"></a>成員

**\_ \_ EventProviderRegistration** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**\_ \_ EventProviderRegistration** 類別具有這些屬性。

<dl> <dt>

**EventQueryList**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

一或多個 Windows Management Instrumentation 查詢語言 (WQL) 查詢，描述事件提供者所支援的事件。

</dd> <dt>

**供應商**
</dt> <dd> <dl> <dt>

資料類型： **\_ \_ 提供者**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

事件提供者的物件路徑。 這個屬性繼承自 [**\_ \_ ProviderRegistration**](--providerregistration.md)。

</dd> </dl>

## <a name="remarks"></a>備註

只有系統管理員可以藉由建立 [**\_ \_ Win32Provider**](--win32provider.md)和 [**\_ \_ EventProviderRegistration**](--eventconsumerproviderregistration.md)的實例，來註冊或刪除事件提供者。 **\_ \_ EventProviderRegistration** 類別衍生自 [**\_ \_ ProviderRegistration**](--providerregistration.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |
| 命名空間<br/>                | 所有 WMI 命名空間<br/>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**\_\_ProviderRegistration**](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[WMI 系統類別](wmi-system-classes.md)
</dt> <dt>

[註冊事件提供者](registering-an-event-provider.md)
</dt> <dt>

[撰寫事件提供者](writing-an-event-provider.md)
</dt> </dl>

 


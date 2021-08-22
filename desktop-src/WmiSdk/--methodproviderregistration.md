---
description: 使用 WMI 註冊方法提供者。
ms.assetid: c5a8ccd3-487e-42a3-bb31-d27da9a711c4
ms.tgt_platform: multiple
title: __MethodProviderRegistration 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __MethodProviderRegistration
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 2a778e2d94c39448020d5a1b4a99e9030320dee4c8604d390c6008f29fabff4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118820936"
---
# <a name="__methodproviderregistration-class"></a>\_\_MethodProviderRegistration 類別

**\_ \_ MethodProviderRegistration** 系統類別會向 WMI 註冊方法提供者。

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
class __MethodProviderRegistration : __ProviderRegistration
{
  __Provider REF provider;
};
```

## <a name="members"></a>成員

**\_ \_ MethodProviderRegistration** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**\_ \_ MethodProviderRegistration** 類別具有這些屬性。

<dl> <dt>

**供應商**
</dt> <dd> <dl> <dt>

資料類型： **\_ \_ 提供者**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

[**\_ \_ 提供者**](--provider.md)實例的參考，代表方法提供者的物件路徑。 這個屬性繼承自 [**\_ \_ ProviderRegistration**](--providerregistration.md)。

</dd> </dl>

## <a name="remarks"></a>備註

**\_ \_ MethodProviderRegistration** 類別衍生自 [**\_ \_ ProviderRegistration**](--providerregistration.md)。 只有系統管理員可以藉由建立 [**\_ \_ Win32Provider**](--win32provider.md)和 **\_ \_ MethodProviderRegistration** 的實例來註冊或刪除方法提供者。

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

[註冊方法提供者](registering-a-method-provider.md)
</dt> </dl>

 


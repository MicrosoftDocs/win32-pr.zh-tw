---
description: 作為各種提供者類型之註冊類別的父類別。
ms.assetid: 1e5d95cb-0961-4be8-b80a-37b598c9ccfe
ms.tgt_platform: multiple
title: __ProviderRegistration 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ProviderRegistration
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 7359f3d5cdcfb2447b724fd6d369a1029d8fcd4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115656"
---
# <a name="__providerregistration-class"></a>\_\_ProviderRegistration 類別

**\_ \_ ProviderRegistration** 抽象系統類別可作為各種提供者類型之註冊類別的父類別。

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[abstract]
class __ProviderRegistration : __SystemClass
{
  __Provider REF provider;
};
```

## <a name="members"></a>成員

**\_ \_ ProviderRegistration** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**\_ \_ ProviderRegistration** 類別具有這些屬性。

<dl> <dt>

**供應商**
</dt> <dd> <dl> <dt>

資料類型： **\_ \_ 提供者**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

參考 [**\_ \_ 提供**](--provider.md)者的實例，表示提供者的物件路徑。

</dd> </dl>

## <a name="remarks"></a>備註

**\_ \_ ProviderRegistration** 類別衍生自 [**\_ \_ SystemClass**](--systemclass.md)，但沒有屬性。

永遠不會建立 **\_ \_ ProviderRegistration** 系統類別的實例。 提供者用來建立註冊實例的類別，可以直接或間接從此類別衍生。 這些類別是：

[**\_\_ClassProviderRegistration**](--classproviderregistration.md)

[**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md)

[**\_\_EventProviderRegistration**](--eventproviderregistration.md)

[**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md)

[**\_\_MethodProviderRegistration**](--methodproviderregistration.md)

[**\_\_ObjectProviderRegistration**](--objectproviderregistration.md)

[**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md)

只有系統管理員可以藉由建立 [**\_ \_ Win32Provider**](--win32provider.md)的實例並註冊，來註冊或刪除提供者。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |
| 命名空間<br/>                | 所有 WMI 命名空間<br/>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**\_\_SystemClass**](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[WMI 系統類別](wmi-system-classes.md)
</dt> <dt>

[註冊提供者](registering-a-provider.md)
</dt> </dl>

 


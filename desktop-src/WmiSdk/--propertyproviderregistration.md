---
description: 在 WMI 中註冊屬性提供者。
ms.assetid: 24792884-3fb9-4974-83d5-1c5fc1fa72a1
ms.tgt_platform: multiple
title: __PropertyProviderRegistration 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __PropertyProviderRegistration
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 6d618a62eab4ba799a2d0e152763fcef6567fd42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513532"
---
# <a name="__propertyproviderregistration-class"></a>\_\_PropertyProviderRegistration 類別

**\_ \_ PropertyProviderRegistration** 系統類別會在 WMI 中註冊屬性提供者。

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
class __PropertyProviderRegistration : __ProviderRegistration
{
  __Provider REF provider;
  boolean        SupportsPut = False;
  boolean        SupportsGet = False;
};
```

## <a name="members"></a>成員

**\_ \_ PropertyProviderRegistration** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**\_ \_ PropertyProviderRegistration** 類別具有這些屬性。

<dl> <dt>

**供應商**
</dt> <dd> <dl> <dt>

資料類型： **\_ \_ 提供者**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

[**\_ \_ 提供者**](--provider.md)實例的參考，代表屬性提供者的物件路徑。 這個屬性繼承自 [**\_ \_ ProviderRegistration**](--providerregistration.md)。

</dd> <dt>

**SupportsGet**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

描述類別或執行個體提供者是否支援資料抓取。

<dt>

對
</dt> <dd>

提供者可透過執行 [**IWbemServices：： GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)來支援資料抓取。

</dd> <dt>

否
</dt> <dd>

提供者不支援資料抓取，並傳回無法從 [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)執行的 **WBEM \_ E \_ 提供者 \_ \_** 。

</dd> </dl>

</dd> <dt>

**SupportsPut**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

描述類別或執行個體提供者是否支援資料修改。

<dt>

對
</dt> <dd>

提供者可透過執行下列其中一種方法來支援類別或實例修改：

-   [**IWbemServices：:P utclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (類別提供者) 
-   [**IWbemServices：:P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (類別提供者) 

</dd> <dt>

否
</dt> <dd>

提供者不支援資料修改，並傳回無法從 [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync)或 [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)進行的 **WBEM \_ E \_ 提供者 \_ \_** 。

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>備註

**\_ \_ PropertyProviderRegistration** 類別衍生自 [**\_ \_ ProviderRegistration**](--providerregistration.md)。 只有系統管理員可以藉由建立 [**\_ \_ Win32Provider**](--win32provider.md)和 **\_ \_ PropertyProviderRegistration** 的實例來註冊屬性提供者。 只有系統管理員可以刪除屬性提供者。

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

[註冊屬性提供者](registering-a-property-provider.md)
</dt> </dl>

 


---
description: 以安全描述項的形式保存命名空間的安全性許可權。
ms.assetid: 84e514f5-b114-4bfc-ab0b-9745f249168b
ms.tgt_platform: multiple
title: __thisNAMESPACE 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __thisNAMESPACE
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 440ccdf0eda794b5d648cae756f9a9c808eb2db6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996905"
---
# <a name="__thisnamespace-class"></a>\_\_thisNAMESPACE 類別

**\_ \_ ThisNAMESPACE** 系統類別會以安全描述項的形式保存命名空間的安全性許可權。 在所有命名空間中都可以找到這個類別和單一實例。

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[singleton]
class __thisNAMESPACE : __SystemClass
{
  uint8 SECURITY_DESCRIPTOR[];
};
```

## <a name="members"></a>成員

**\_ \_ ThisNAMESPACE** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**\_ \_ ThisNAMESPACE** 類別具有這些屬性。

<dl> <dt>

**安全 \_ 描述項**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

安全描述項，描述誰可以存取命名空間，以及誰可以讀取或寫入命名空間。 這個屬性繼承自 [**\_ \_ 事件**](--event.md)。 如需安全描述項格式的詳細資訊，請參閱 Windows SDK 的安全性一節中的 [安全描述項](/windows/desktop/SecAuthZ/security-descriptors) 。

</dd> </dl>

## <a name="remarks"></a>備註

**\_ \_ ThisNAMESPACE** 的單一實例是唯讀的。 若要變更安全描述項屬性的設定，請使用 [**\_ \_ SystemSecurity**](--systemsecurity.md)類別的方法。 **\_ \_ ThisNAMESPACE** 類別衍生自 [**\_ \_ SystemClass**](--systemclass.md)。

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
</dt> </dl>

 


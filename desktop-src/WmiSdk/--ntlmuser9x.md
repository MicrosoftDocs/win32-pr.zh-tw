---
description: 控制 Windows 不受支援版本的遠端存取。
ms.assetid: eb326bba-a011-4b9c-b4ee-fc08ae364f6f
ms.tgt_platform: multiple
title: __NTLMUser9X 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NTLMUser9X
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 2d05920b0936e8ff4de3eb338938e03e92edb4596efbf01f1064b6952a7df661
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320576"
---
# <a name="__ntlmuser9x-class"></a>\_\_NTLMUser9X 類別

**\_ \_ NTLMUser9X** 系統類別可控制 Windows 不受支援版本的遠端存取。 下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
class __NTLMUser9X : __SecurityRelatedClass
{
  string Authority;
  sint32 Flags;
  sint32 Mask;
  string Name;
  sint32 Type;
};
```

## <a name="members"></a>成員

**\_ \_ NTLMUser9X** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**\_ \_ NTLMUser9X** 類別具有這些屬性。

<dl> <dt>

**授權單位**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

要套用使用者名稱的網域。

</dd> <dt>

**旗標**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

繼承旗標。

<dt>

0
</dt> <dd>

無繼承。

</dd> <dt>

2
</dt> <dd>

除了目前的命名空間之外，也會套用至子命名空間。

</dd> </dl>

</dd> <dt>

**Mask**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

位元遮罩，指定 Windows Management Instrumentation (WMI) 存放庫中命名空間的存取權限。 如需位值，請參閱 [**命名空間存取權限常數**](namespace-access-rights-constants.md)。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

使用者名稱。

</dd> <dt>

**類型**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

允許存取。

<dt>

0
</dt> <dd>

允許存取。

</dd> <dt>

2
</dt> <dd>

拒絕存取。

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>備註

**\_ \_ NTLMUser9X** 類別用來做為 [**\_ \_ SystemSecurity：： Get9XUserList**](--systemsecurity-get9xuserlist.md)和 [**\_ \_ SystemSecurity：： Set9XUserList**](--systemsecurity-set9xuserlist.md)方法的輸入參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |
| 命名空間<br/>                | 所有 WMI 命名空間<br/>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**\_\_SecurityRelatedClass**](/windows/desktop/WmiSdk/--securityrelatedclass)
</dt> <dt>

[WMI 系統類別](wmi-system-classes.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> </dl>

 


---
description: 表示存取控制項目 (ACE)。
ms.assetid: 47daffd0-b9db-4367-b0b8-654a2da30fed
ms.tgt_platform: multiple
title: __ACE 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ACE
- All
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: ea2a765225145ce3d44e0aff89aeaca0a7563e0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104469464"
---
# <a name="__ace-class"></a>\_\_ACE 類別

**\_ \_ Ace** 抽象系統類別代表 ([*ACE*](/windows/desktop/SecGloss/a-gly)) 的存取控制專案。

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
class  __ACE : __SecurityRelatedClass
{
            AceFlags;
            AccessMask;
            AceType;
            GuidInheritedObjectType;
            GuidObjectType;
  uint64    TIME_CREATED;
  __Trustee Trustee;
};
```

## <a name="members"></a>成員

**\_ \_ ACE** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**\_ \_ ACE** 類別具有這些屬性。

<dl> <dt>

**AccessMask**
</dt> <dd> <dl> <dt>

資料類型: 
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

代表授與或拒絕信任者之許可權的位旗標。 如需詳細資訊和旗標的描述，請參閱 [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)類別中的 **AccessMask** 屬性。

</dd> <dt>

**AceFlags**
</dt> <dd> <dl> <dt>

資料類型: 
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指定 ACE 繼承的位旗標。 如需詳細資訊和旗標的描述，請參閱 [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)類別中的 **AceFlags** 屬性。

</dd> <dt>

**AceType**
</dt> <dd> <dl> <dt>

資料類型: 
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

此實例所表示之 ACE 專案的型別。

</dd> <dt>

**GuidInheritedObjectType**
</dt> <dd> <dl> <dt>

資料類型: 
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

**AccessMask** 屬性中的存取權限所套用之物件父系的 GUID。

</dd> <dt>

**GuidObjectType**
</dt> <dd> <dl> <dt>

資料類型: 
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

GUID，指出 **AccessMask** 屬性中的許可權所套用的物件類型。

</dd> <dt>

**\_建立時間**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

建立安全描述項時，採用 [CIM \_ 日期](cim-datetime.md) 時間格式的時間。

</dd> <dt>

**受託 人**
</dt> <dd> <dl> <dt>

資料類型： **[ **\_ \_ 信任者**](--trustee.md)**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

Ace 類別的這個實例所表示之 ace 專案的信任 **\_ \_** 者。

</dd> </dl>

## <a name="remarks"></a>備註

這個類別會提供 [**win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) 類別所繼承的屬性，該類別是 [**win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) 類別的成員。 如需詳細資訊，請參閱 [WMI 安全描述項物件](wmi-security-descriptor-objects.md) 和 [變更安全物件的存取安全性](changing-access-security-on-securable-objects.md)。 如需 Ace 的詳細資訊，請參閱 [存取控制元件](/windows/desktop/SecAuthZ/access-control-components)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |
| 命名空間<br/>                | 所有 WMI 命名空間<br/>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**\_\_SecurityRelatedClass**](--securityrelatedclass.md)
</dt> <dt>

[WMI 系統類別](wmi-system-classes.md)
</dt> <dt>

[**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[維護 WMI 安全性](maintaining-wmi-security.md)
</dt> </dl>

 


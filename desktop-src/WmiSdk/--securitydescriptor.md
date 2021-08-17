---
description: 代表安全性描述元。
ms.assetid: 1ade1751-52a2-4ada-8255-323321111663
ms.tgt_platform: multiple
title: __SecurityDescriptor 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SecurityDescriptor
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
ms.openlocfilehash: c248a437651396811f71c04e72dd8b209c5d10823f49d03abbe7e9d9ee6b6867
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118110195"
---
# <a name="__securitydescriptor-class"></a>\_\_SecurityDescriptor 類別

**\_ \_ SecurityDescriptor** 抽象系統類別代表 [*安全描述項*](/windows/desktop/SecGloss/s-gly)。

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
class __SecurityDescriptor
{
  uint32 ControlFlags;
  __ACE  DACL[];
  __ACE  Group;
  __ACE  Owner;
  __ACE  SACL;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>成員

**\_ \_ SecurityDescriptor** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**\_ \_ SecurityDescriptor** 類別具有這些屬性。

<dl> <dt>

**ControlFlags**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

提供描述項內容和格式相關資訊的位旗標。 如需旗標的描述，請參閱 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)類別中的 **ControlFlags** 屬性。

</dd> <dt>

**DACL**
</dt> <dd> <dl> <dt>

資料類型： **[**\_ \_ ACE**](--ace.md)** 陣列
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指定物件存取權之 [**\_ \_ ACE**](--ace.md)專案的陣列。

</dd> <dt>

**群組**
</dt> <dd> <dl> <dt>

資料類型： **[ **\_ \_ ACE**](--ace.md)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

識別代表物件群組之信任者的 ACE。

</dd> <dt>

**擁有者**
</dt> <dd> <dl> <dt>

資料類型： **[ **\_ \_ ACE**](--ace.md)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

識別代表物件擁有者之信任者的 ACE。

</dd> <dt>

**SACL**
</dt> <dd> <dl> <dt>

資料類型： **[ **\_ \_ ACE**](--ace.md)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

[**\_ \_ ACE**](--ace.md)專案的陣列，可識別所收集之審核資訊的使用者和群組。

</dd> <dt>

**\_建立時間**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

建立安全描述項時，採用 [CIM \_ DATETIME](cim-datetime.md) 格式的時間。

</dd> </dl>

## <a name="remarks"></a>備註

此類別提供 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)所繼承的屬性。 如需詳細資訊，請參閱 [WMI 安全描述項物件](wmi-security-descriptor-objects.md) 和 [變更安全物件的存取安全性](changing-access-security-on-securable-objects.md)。 如需 Ace 的詳細資訊，請參閱 [存取控制元件](/windows/desktop/SecAuthZ/access-control-components)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |
| 命名空間<br/>                | 所有 WMI 命名空間<br/>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[WMI 系統類別](wmi-system-classes.md)
</dt> <dt>

[**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[維護 WMI 安全性](maintaining-wmi-security.md)
</dt> </dl>

 


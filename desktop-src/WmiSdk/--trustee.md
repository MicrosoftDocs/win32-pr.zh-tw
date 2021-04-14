---
description: '\_ \_ 受信任的抽象系統類別代表信任者。 您可以使用 (位元組陣列的名稱或 SID) 。'
ms.assetid: 92d17c7c-ebca-4dd0-80d8-6edd999ca394
ms.tgt_platform: multiple
title: __Trustee 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Trustee
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
ms.openlocfilehash: 5c6ba04760e924ffe9d86916cffdb82ea2488219
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514240"
---
# <a name="__trustee-class"></a>\_\_信任類別

[**\_ \_ 受信任**](--securitydescriptor.md)的抽象系統類別代表 [*信任者*](/windows/desktop/SecGloss/t-gly)。 您可以使用 (位元組陣列的名稱或 SID) 。

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
class __Trustee
{
  string Domain;
  string Name;
  uint8  SID[];
  uint32 SidLength;
  string SidString;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>成員

**\_ \_ 信任者** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**\_ \_ 信任者** 類別具有這些屬性。

<dl> <dt>

**網域**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

帳戶的網域部分。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

帳戶的名稱部分。

</dd> <dt>

**SID**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

二進位位元組陣列形式之信任者的 SID。

</dd> <dt>

**SidLength**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

SID 的長度（以位元組為單位）。

</dd> <dt>

**SidString**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

具有字串格式之信任者的 SID，例如 "S-1-1-0"。

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

這個類別提供的屬性是由 [**win32 \_ 受信任**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) 類別所繼承，這是 [**win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) 類別的成員。 如需詳細資訊，請參閱 [WMI 安全描述項物件](wmi-security-descriptor-objects.md) 和 [變更安全物件的存取安全性](changing-access-security-on-securable-objects.md)。 如需 Ace 的詳細資訊，請參閱 [存取控制元件](/windows/desktop/SecAuthZ/access-control-components)。

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

[**Win32 \_ 信任者**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)
</dt> <dt>

[維護 WMI 安全性](maintaining-wmi-security.md)
</dt> </dl>

 


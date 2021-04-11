---
description: '>register-wmievent 類別是衍生所有 WMI 事件類別的基類。'
ms.assetid: 0393d3fc-7566-4eda-940e-248d622a903a
title: '>register-wmievent 類別'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WMIEvent
- WMIEvent.SECURITY_DESCRIPTOR
- WMIEvent.TIME_CREATED
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 99f6804ef1dad4f37bd2727da2e91e801fb0ece2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027314"
---
# <a name="wmievent-class"></a>>register-wmievent 類別

**>register-wmievent** 類別是衍生所有 WMI 事件類別的基類。

下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
[]
class WMIEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>成員

**>register-wmievent** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**>register-wmievent** 類別具有這些屬性。

<dl> <dt>

**安全 \_ 描述項**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

事件提供者用來判斷哪些使用者可以接收事件的描述項。 這個屬性繼承自 [**\_ \_ 事件**](/windows/desktop/WmiSdk/--event)。 如需有關用來設定此安全描述項之常數的詳細資訊，請參閱 [WMI 安全性常數](/windows/desktop/WmiSdk/wmi-security-constants)。

</dd> <dt>

**\_建立時間**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

唯一值，指出產生事件的時間。 這是64位值，代表1601年1月1日之後的 100-毫微秒間隔數目。 此資訊採用國際標準時間 (UTC) 格式。 這個屬性繼承自 [**\_ \_ 事件**](/windows/desktop/WmiSdk/--event)。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。

</dd> </dl>

## <a name="remarks"></a>備註

**>register-wmievent** 類別衍生自 [**\_ \_ ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                                                                              |
| 最低支援的伺服器<br/> | Windows Server 2003<br/>                                                                                                                        |
| 命名空間<br/>                | 根 \\ WMI<br/>                                                                                                                                  |
| MOF<br/>                      | <dl> <dt>Wmi. mof;</dt><dt>WmiCore mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl>                                                                |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[MSMCA 類別](msmca-classes.md)
</dt> <dt>

[**\_\_ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> </dl>

 


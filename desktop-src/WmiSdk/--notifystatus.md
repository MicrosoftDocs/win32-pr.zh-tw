---
description: 作為提供者定義之錯誤類別的父類別。
ms.assetid: fc2747f5-cfbc-4d61-894d-4585a03dda3f
ms.tgt_platform: multiple
title: __NotifyStatus 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NotifyStatus
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: f19ef1f6088b5a058f4483f197877358177c81f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694935"
---
# <a name="__notifystatus-class"></a>\_\_NotifyStatus 類別

**\_ \_ NotifyStatus** 抽象系統類別可作為提供者定義之錯誤類別的父類別。

下列語法簡化了受控物件格式 (MF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[abstract]
class __NotifyStatus
{
  uint32 StatusCode;
};
```

## <a name="members"></a>成員

**\_ \_ NotifyStatus** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**\_ \_ NotifyStatus** 類別具有這些屬性。

<dl> <dt>

**StatusCode**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

包含作業的錯誤或資訊代碼。 這可以是任何使用者定義的程式碼，但值 0 (零) 通常會保留以表示成功。

</dd> </dl>

## <a name="remarks"></a>備註

雖然 **\_ \_ NotifyStatus** 類別可以是提供者定義之錯誤類別的父類別，但建議提供者改為從 [**\_ \_ ExtendedStatus**](--extendedstatus.md)衍生錯誤類別。 使用 **\_ \_ ExtendedStatus** 可讓您更有效地標準化錯誤類別。

提供者永遠不應直接建立 **\_ \_ NotifyStatus** 的實例，因為這些實例所傳達的資訊不會超過簡單的傳回碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |
| 命名空間<br/>                | 所有 WMI 命名空間<br/>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[WMI 系統類別](wmi-system-classes.md)
</dt> </dl>

 

 





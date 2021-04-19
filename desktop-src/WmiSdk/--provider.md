---
description: 作為 \_ \_ Win32Provider 系統類別的父類別。
ms.assetid: e4cad7c6-4650-4334-b8c4-ac65381bced7
ms.tgt_platform: multiple
title: __Provider 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Provider
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 733323c106a5d682e7eddbe3a41bf9c156520c51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977955"
---
# <a name="__provider-class"></a>\_\_提供者類別

**\_ \_ Provider** system 類別是抽象基類，可做為 [**\_ \_ Win32Provider**](--win32provider.md)系統類別的父類別。

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[abstract]
class __Provider : __SystemClass
{
  string Name;
};
```

## <a name="members"></a>成員

**\_ \_ 提供者** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**\_ \_ 提供者** 類別具有這些屬性。

<dl> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞：索引 [**鍵**](standard-qualifiers.md)
</dt> </dl>

可唯一識別提供者的語言中性字元串。 建議採用下列格式來防止命名衝突：

廠商 \| 提供者 \| 版本

例如，此提供者名稱代表 Microsoft TestProvider 的1.0 版：

"Microsoft \| TestProvider v1.0 \| "

</dd> </dl>

## <a name="remarks"></a>備註

**\_ \_ 提供者** 類別衍生自沒有屬性的 [**\_ \_ SystemClass**](--systemclass.md)。

提供者會建立 [**\_ \_ Win32Provider**](--win32provider.md)實例，以指定其實體執行的相關資訊。

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

[**\_\_Win32Provider**](--win32provider.md)
</dt> </dl>

 


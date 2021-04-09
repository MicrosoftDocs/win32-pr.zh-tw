---
description: Win32 \_ LoggedOnUser 關聯 WMI 類別會建立會話與使用者帳戶的關聯。
ms.assetid: b1233f90-4898-4ced-84d2-0858027e935a
ms.tgt_platform: multiple
title: Win32_LoggedOnUser 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LoggedOnUser
- Win32_LoggedOnUser.Dependent
- Win32_LoggedOnUser.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0f851c85563095a66197b0dde8e6cbddc9581f07
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847527"
---
# <a name="win32_loggedonuser-class"></a>Win32 \_ LoggedOnUser 類別

**Win32 \_ LoggedOnUser** 關聯 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)會建立會話與使用者帳戶的關聯。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8BB5B3EC-E1F7-4b39-942A-605D5F55789A}"), AMENDMENT]
class Win32_LoggedOnUser : CIM_Dependency
{
  Win32_LogonSession REF Dependent;
  Win32_Account      REF Antecedent;
};
```

## <a name="members"></a>成員

**Win32 \_ LoggedOnUser** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ LoggedOnUser** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ 帳戶**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) () ，索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

[**Win32 \_ 帳戶**](win32-account.md)，描述在此會話起始時使用的帳戶。 帳戶可以是使用者帳戶或系統帳戶。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ LogonSession**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) (相依) ，索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

[**Win32 \_ LogonSession**](win32-logonsessionmappeddisk.md) ，描述帳戶目前所使用的會話。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ LoggedOnUser** 類別衍生自 CIM 相依 [**性 \_**](cim-dependency.md)。

## <a name="examples"></a>範例

[Loggedonuser 函式](https://Gallery.TechNet.Microsoft.Com/scriptcenter/0e43993a-895a-4afe-a2b2-045a5146048a)PowerShell 範例會取得本機或遠端電腦上已登入的使用者，以及會話資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ 相依性**](cim-dependency.md)
</dt> <dt>

[作業系統類別](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 


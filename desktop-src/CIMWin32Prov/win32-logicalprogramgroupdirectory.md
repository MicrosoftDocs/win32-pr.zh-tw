---
description: Win32 \_ LogicalProgramGroupDirectory 關聯 WMI 類別會將 [開始] 功能表) 中的邏輯程式群組和儲存它們的檔案目錄中的 (群組相關聯。
ms.assetid: 31a8b56a-d4fd-4cc5-9997-ec6211fe9425
ms.tgt_platform: multiple
title: Win32_LogicalProgramGroupDirectory 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroupDirectory
- Win32_LogicalProgramGroupDirectory.Antecedent
- Win32_LogicalProgramGroupDirectory.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d6ebaddd4455ba1b62832f940d78534c90cefeeb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973957"
---
# <a name="win32_logicalprogramgroupdirectory-class"></a>Win32 \_ LogicalProgramGroupDirectory 類別

**Win32 \_ LogicalProgramGroupDirectory** 關聯 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)會將邏輯程式群組與 [**開始**] 功能表中的 (群組) 和儲存它們的檔案目錄相關聯。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{F25FE467-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroupDirectory : CIM_Dependency
{
  Win32_LogicalProgramGroup REF Antecedent;
  Win32_Directory           REF Dependent;
};
```

## <a name="members"></a>成員

**Win32 \_ LogicalProgramGroupDirectory** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ LogicalProgramGroupDirectory** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ LogicalProgramGroup**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ LogicalProgramGroup" ) 
</dt> </dl>

代表邏輯程式群組之實例的參考。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ 目錄**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)、覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「WMI \| Win32 目錄」 \_ ) 
</dt> </dl>

代表邏輯程式群組之檔案目錄的實例參考。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ LogicalProgramGroupDirectory** 類別衍生自 CIM 相依 [**性 \_**](cim-dependency.md)。

使用這個類別的呼叫進程必須在登錄所在的電腦上具有「 **SE \_ 還原 \_ 名稱** 」許可權。 例如，如果您在本機電腦上列舉此類別，您的應用程式執行所在的帳戶必須具有此許可權。 如需詳細資訊，請參閱 [執行特殊許可權作業](/windows/desktop/WmiSdk/executing-privileged-operations)。

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

 


---
description: Win32 \_ LogicalProgramGroupItemDataFile 關聯 WMI 類別會將 [開始] 功能表的程式群組專案和儲存這些專案的檔案產生關聯。
ms.assetid: 9327c205-d0ad-4f2b-a65e-2a648e7c13e0
ms.tgt_platform: multiple
title: Win32_LogicalProgramGroupItemDataFile 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroupItemDataFile
- Win32_LogicalProgramGroupItemDataFile.Antecedent
- Win32_LogicalProgramGroupItemDataFile.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b6f69c23ae545de837e9d6578ba2f64eed51ecbc6f10780e40c809cb2e362b33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119973048"
---
# <a name="win32_logicalprogramgroupitemdatafile-class"></a>Win32 \_ LogicalProgramGroupItemDataFile 類別

**Win32 \_ LogicalProgramGroupItemDataFile** 關聯 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)會關聯 [**開始**] 功能表的程式群組專案和儲存這些專案的檔案。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{08FFAD62-8050-11d2-90CE-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroupItemDataFile : CIM_Dependency
{
  Win32_LogicalProgramGroupItem REF Antecedent;
  CIM_DataFile                  REF Dependent;
};
```

## <a name="members"></a>成員

**Win32 \_ LogicalProgramGroupItemDataFile** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ LogicalProgramGroupItemDataFile** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ LogicalProgramGroupItem**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ LogicalProgramGroupItem" ) 
</dt> </dl>

代表 [ **開始** ] 功能表中程式群組的實例參考。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **CIM 資料 \_ 檔**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「cim \| cim \_ 資料檔案」 ) 
</dt> </dl>

代表與程式群組相關聯之類別的實例參考。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ LogicalProgramGroupItemDataFile** 類別衍生自 CIM 相依 [**性 \_**](cim-dependency.md)。

使用這個類別的呼叫進程必須在登錄所在的電腦上具有 **SE \_ RESTORE \_ NAME** 許可權。 例如，如果您在本機電腦上列舉此類別，您的應用程式執行所在的帳戶必須具有此許可權。 如需詳細資訊，請參閱 [執行特殊許可權作業](/windows/desktop/WmiSdk/executing-privileged-operations)。

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

 


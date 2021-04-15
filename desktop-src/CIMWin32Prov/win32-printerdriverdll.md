---
description: Win32 \_ PrinterDriverDll 關聯 WMI 類別會建立本機印表機及其驅動程式檔案的關聯。
ms.assetid: decbd1de-8091-47f7-94a1-42862070b920
ms.tgt_platform: multiple
title: Win32_PrinterDriverDll 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriverDll
- Win32_PrinterDriverDll.Antecedent
- Win32_PrinterDriverDll.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 41484c39d9e1b59efd79d7aee08719b3a241de97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468433"
---
# <a name="win32_printerdriverdll-class"></a>Win32 \_ PrinterDriverDll 類別

**Win32 \_ PrinterDriverDll** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會建立本機印表機及其驅動程式檔案的關聯。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
class Win32_PrinterDriverDll : CIM_Dependency
{
  CIM_DataFile  REF Antecedent;
  Win32_Printer REF Dependent;
};
```

## <a name="members"></a>成員

**Win32 \_ PrinterDriverDll** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ PrinterDriverDll** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **CIM 資料 \_ 檔**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](../wmisdk/standard-qualifiers.md)
</dt> </dl>

參考 [**CIM \_ 資料檔案**](cim-datafile.md) 實例，表示此 Windows 印表機的驅動程式檔案。

這個屬性繼承自 [**CIM 相依 \_**](cim-dependency.md)性。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ 印表機**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](../wmisdk/standard-qualifiers.md)
</dt> </dl>

[**Win32 \_ 印表機**](win32-printer.md)實例的參考。

這個屬性繼承自 [**CIM 相依 \_**](cim-dependency.md)性。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ PrinterDriverDll** 類別衍生自 CIM 相依 [**性 \_**](cim-dependency.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                      |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ 印表機。 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ 相依性**](cim-dependency.md)
</dt> <dt>

[電腦系統硬體類別](computer-system-hardware-classes.md)
</dt> </dl>

 

 

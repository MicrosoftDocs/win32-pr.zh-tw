---
description: Win32 \_ SessionProcess 關聯 WMI 類別代表登入會話與與該會話相關聯之進程之間的關聯。
ms.assetid: 19d4ecf9-27b5-4a0b-9c76-7d10679aaf5e
ms.tgt_platform: multiple
title: Win32_SessionProcess 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SessionProcess
- Win32_SessionProcess.Antecedent
- Win32_SessionProcess.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f4090da88e8f5d31b0940b0c7d217a930a364b63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986245"
---
# <a name="win32_sessionprocess-class"></a>Win32 \_ SessionProcess 類別

**Win32 \_ SessionProcess** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)代表登入會話與與該會話相關聯之進程之間的關聯。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("9CD8E1CE-0D27-4a41-AADE-F8D200230FF4"), AMENDMENT]
class Win32_SessionProcess : Win32_SessionResource
{
  Win32_LogonSession REF Antecedent;
  Win32_Process      REF Dependent;
};
```

## <a name="members"></a>成員

**Win32 \_ SessionProcess** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ SessionProcess** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ LogonSession**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "Antecedent" ) ， [**Key**](../wmisdk/key-qualifier.md)
</dt> </dl>

[**Win32 \_ LogonSession**](win32-logonsessionmappeddisk.md) ，表示與進程相關的會話。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ 進程**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( 「相依」 ) ，索引 [**鍵**](../wmisdk/key-qualifier.md)
</dt> </dl>

[**Win32 \_ 進程**](win32-processor.md)，表示與會話相關聯的進程。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_** 當系統管理員已提高許可權或從遠端執行時，SessionProcess 會傳回系統管理員的所有會話。 這是類別行為的延伸。

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

[**Win32 \_ SessionResource**](win32-sessionresource.md)
</dt> <dt>

[作業系統類別](./operating-system-classes.md)
</dt> </dl>

 

 

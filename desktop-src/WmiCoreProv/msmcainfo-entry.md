---
description: 表示 MCA、已更正的機器檢查 (CMC) ，或已更正的平臺錯誤 (CPE) 資訊專案。 此類別僅適用于64位的 Windows 系統。
ms.assetid: 4edbca20-2525-4e35-ab79-8cf421343144
title: MSMCAInfo_Entry 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_Entry
- MSMCAInfo_Entry.Data
- MSMCAInfo_Entry.Length
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: cda6abba06dc4d4f3fec3a4763391eee1fa81274
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983831"
---
# <a name="msmcainfo_entry-class"></a>MSMCAInfo \_ 專案類別

**MSMCAInfo \_ 專案** 類別指出 MCA、已更正的機器檢查 (CMC) ，或已更正的平臺錯誤 (CPE) 資訊專案。 此類別僅適用于64位的 Windows 系統。

下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
class MSMCAInfo_Entry : MSMCAInfo
{
  uint8  Data[];
  uint32 Length;
};
```

## <a name="members"></a>成員

**MSMCAInfo \_ 專案** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MSMCAInfo \_ 專案** 類別具有這些屬性。

<dl> <dt>

**資料**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

包含完整 MCA 錯誤記錄的整數陣列，如系統抽象層 (SAL) 所報告。 SAL 是燒錄至 ROM 的程式碼，作業系統會呼叫該作業系統來執行與平臺相關的作業。 它類似于 x86 平臺上的 BIOS。

</dd> <dt>

**長度**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

錯誤記錄中的位元組數目。

</dd> </dl>

## <a name="remarks"></a>備註

**MSMCAInfo \_ 專案** 類別衍生自 [**MSMCAInfo**](msmcainfo.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows XP<br/>                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2003<br/>                                                         |
| 命名空間<br/>                | 根 \\ wmi<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Wmicore mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[MSMCA 類別](msmca-classes.md)
</dt> <dt>

[**MSMCAInfo**](msmcainfo.md)
</dt> </dl>

 

 





---
description: 指定 (MCA) 記錄的原始機器檢查架構。 此類別僅適用于64位 Windows 系統。
ms.assetid: d465ba8d-14b2-4911-ae19-19ebeb32126e
title: MSMCAInfo_RawMCAData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawMCAData
- MSMCAInfo_RawMCAData.Active
- MSMCAInfo_RawMCAData.Count
- MSMCAInfo_RawMCAData.InstanceName
- MSMCAInfo_RawMCAData.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 2b7ac9f8c474a1aee55d0dd70a5a838102aec66bc8b3ba3d867070430c38a3ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118821862"
---
# <a name="msmcainfo_rawmcadata-class"></a>MSMCAInfo \_ RawMCAData 類別

**MSMCAInfo \_ RawMCAData** 會將原始機器檢查架構指定 (MCA) 記錄。 此類別僅適用于64位 Windows 系統。

下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
class MSMCAInfo_RawMCAData : MSMCAInfo
{
  boolean         Active;
  uint32          Count;
  string          InstanceName;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a>成員

**MSMCAInfo \_ RawMCAData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MSMCAInfo \_ RawMCAData** 類別具有這些屬性。

<dl> <dt>

**使用中**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

如果此類別的實例為使用中，則為 TRUE;否則 **為 FALSE**。

</dd> <dt>

**Count**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

錯誤記錄的數目。

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

此類別實例的唯一識別碼。

</dd> <dt>

**記錄**
</dt> <dd> <dl> <dt>

資料類型： **MSMCAInfo \_ 專案** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

MCA 錯誤記錄的陣列。 陣列中的 MCA 錯誤記錄數目是由 **Count** 屬性指定。

</dd> </dl>

## <a name="remarks"></a>備註

**MSMCAInfo \_ RawMCAData** 類別衍生自 [**MSMCAInfo**](msmcainfo.md)。

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

 


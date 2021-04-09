---
description: 包含 (MCA) 事件的機器檢查架構。 此類別僅適用于64位的 Windows 系統。
ms.assetid: d1806b91-43a3-4329-8fe5-de1e4755740f
title: MSMCAInfo_RawMCAEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawMCAEvent
- MSMCAInfo_RawMCAEvent.Active
- MSMCAInfo_RawMCAEvent.Count
- MSMCAInfo_RawMCAEvent.InstanceName
- MSMCAInfo_RawMCAEvent.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: e15af79c67265823e0025849e4c2ef27f690265c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944935"
---
# <a name="msmcainfo_rawmcaevent-class"></a>MSMCAInfo \_ RawMCAEvent 類別

**MSMCAInfo \_ RawMCAEvent** 類別包含 (MCA) 事件的機器檢查架構。 此類別僅適用于64位的 Windows 系統。

下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
class MSMCAInfo_RawMCAEvent : WMIEvent
{
  boolean         Active;
  uint32          Count;
  string          InstanceName;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a>成員

**MSMCAInfo \_ RawMCAEvent** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MSMCAInfo \_ RawMCAEvent** 類別具有這些屬性。

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

可唯一識別這個 **MSMCAInfo \_ RawMCAEvent** 類別實例的字串。

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

**MSMCAInfo \_ RawMCAEvent** 類別衍生自 [**>register-wmievent**](wmievent.md)。

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

[**>register-wmievent**](wmievent.md)
</dt> </dl>

 


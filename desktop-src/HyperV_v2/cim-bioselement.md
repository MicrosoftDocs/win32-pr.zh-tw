---
description: 代表載入至非暫時性存放裝置的低層級軟體，用來啟動和設定電腦系統 (CIM 無系統 \_) 。
ms.assetid: e34c9b00-2723-4858-805e-5e3e51a5dfd2
title: 'CIM_BIOSElement 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSElement
- CIM_BIOSElement.Version
- CIM_BIOSElement.Manufacturer
- CIM_BIOSElement.PrimaryBIOS
- CIM_BIOSElement.ListOfLanguages
- CIM_BIOSElement.CurrentLanguage
- CIM_BIOSElement.LoadedStartingAddress
- CIM_BIOSElement.LoadedEndingAddress
- CIM_BIOSElement.LoadUtilityInformation
- CIM_BIOSElement.ReleaseDate
- CIM_BIOSElement.RegistryURIs
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f97cbb495fb8105be012c44942aeedb39377e3d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986404"
---
# <a name="cim_bioselement-class-hyper-v-management"></a>CIM_BIOSElement 類別 (Hyper-v 管理) 

代表載入至非暫時性存放裝置的低層級軟體，用來啟動和設定電腦系統 (CIM 無系統) [**\_**](cim-computersystem.md) 。

## <a name="syntax"></a>語法

``` syntax
[Abstract, Version("2.17.0"), UMLPackagePath("CIM::Application::BIOS"), AMENDMENT]
class CIM_BIOSElement : CIM_SoftwareElement
{
  string   Version;
  string   Manufacturer;
  boolean  PrimaryBIOS;
  string   ListOfLanguages[];
  string   CurrentLanguage;
  uint64   LoadedStartingAddress;
  uint64   LoadedEndingAddress;
  string   LoadUtilityInformation;
  datetime ReleaseDate;
  string   RegistryURIs[];
};
```

## <a name="members"></a>成員

**CIM \_ BIOSElement** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ BIOSElement** 類別具有這些屬性。

<dl> <dt>

**CurrentLanguage**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ BIOSElement**.**ListOfLanguages**") 
</dt> </dl>

BIOS 目前選取的語言。 這項資訊可從系統管理 BIOS (SMBIOS) 使用類型13結構的目前語言屬性來編制索引，以在結構後面的字串清單中編制索引。 這個屬性會使用 ISO 639 語言名稱進行格式化，並可在後面加上 ISO 3166 區功能變數名稱稱和編碼方法。

</dd> <dt>

**ListOfLanguages**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

適用于 BIOS 的可安裝語言清單。 此資訊可以從 SMBIOS 取得，從類型13結構後面的字串清單中取得。 必須使用 ISO 639 語言名稱來指定 BIOS 可安裝的語言。 您也可以依照語言名稱，指定 ISO 3166 區功能變數名稱稱和編碼方法。

</dd> <dt>

**LoadedEndingAddress**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| SYSTEM BIOS \| 001.6 ") 
</dt> </dl>

BIOS 所佔用記憶體的結束位址。

</dd> <dt>

**LoadedStartingAddress**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| SYSTEM BIOS \| 001.5 ") 
</dt> </dl>

BIOS 所佔用記憶體的起始位址。

</dd> <dt>

**LoadUtilityInformation**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| SYSTEM BIOS \| 001.7 ") 
</dt> </dl>

一個自由格式字串，描述更新 **CIM \_ BIOSElement** 物件所需的 BIOS flash/載入公用程式。 版本和其他資訊可能會顯示在此屬性中。

</dd> <dt>

**製造商**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "製造商" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| SYSTEM BIOS \| 001.2 ") 
</dt> </dl>

軟體元素的製造商。

</dd> <dt>

**PrimaryBIOS**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| SYSTEM BIOS \| 001.9 ") 
</dt> </dl>

如果這是電腦系統的主要 BIOS，則為 True;否則為 false。

</dd> <dt>

**RegistryURIs**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

BIOS 執行符合的 BIOS 屬性登錄的發佈位置。

</dd> <dt>

**ReleaseDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| SYSTEM BIOS \| 001.8 ") 
</dt> </dl>

此 BIOS 的發行日期。

</dd> <dt>

**版本**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Version" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| SYSTEM BIOS \| 001.3 ") 
</dt> </dl>

作業的版本。 作業的版本應該採用下列其中一種形式：

-   *<major>*.*<minor>*.*<revision>*
-   *<major>*.*<minor><letter><revision>*

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                                    |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ SoftwareElement**](cim-softwareelement.md)
</dt> </dl>

 


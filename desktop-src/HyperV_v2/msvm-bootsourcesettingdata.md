---
description: 代表用來設定虛擬機器開機來源的參數。
ms.assetid: 21CD4B71-3D05-469E-89BB-DC2C65F5AB10
title: Msvm_BootSourceSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BootSourceSettingData
- Msvm_BootSourceSettingData.Description
- Msvm_BootSourceSettingData.Caption
- Msvm_BootSourceSettingData.InstanceID
- Msvm_BootSourceSettingData.ElementName
- Msvm_BootSourceSettingData.BootSourceType
- Msvm_BootSourceSettingData.OtherLocation
- Msvm_BootSourceSettingData.FirmwareDevicePath
- Msvm_BootSourceSettingData.BootSourceDescription
- Msvm_BootSourceSettingData.OptionalData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0403846e10df4c9bd54146eea44e8e91c06d01c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974536"
---
# <a name="msvm_bootsourcesettingdata-class"></a>Msvm \_ BootSourceSettingData 類別

代表用來設定虛擬機器開機來源的參數。 此類別衍生自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BootSourceSettingData : CIM_SettingData
{
  string Description;
  string Caption;
  string InstanceID;
  string ElementName;
  uint32 BootSourceType;
  string OtherLocation;
  string FirmwareDevicePath;
  string BootSourceDescription;
  uint8  OptionalData[];
};
```

## <a name="members"></a>成員

**Msvm \_ BootSourceSettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ BootSourceSettingData** 類別具有這些屬性。

<dl> <dt>

**BootSourceDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

由固件提供的開機來源描述。

</dd> <dt>

**BootSourceType**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

列舉值，指定開機來源的類型。

這些是有效的值：

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Drive"></span><span id="drive"></span><span id="DRIVE"></span>

**磁片磁碟機** (1) 


</dt> <dd></dd> <dt>

<span id="Network"></span><span id="network"></span><span id="NETWORK"></span>

**Network** (2) 


</dt> <dd></dd> <dt>

<span id="File"></span><span id="file"></span><span id="FILE"></span>

**File** (3) 


</dt> <dd></dd> </dl>

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **MaxLen** ( 64 ) 
</dt> </dl>

物件的簡短文字描述。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的文字描述。

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此 SettingData 實例的顯示名稱。 此外，顯示名稱可以當做搜尋或查詢的索引屬性使用。  (附注：名稱在命名空間中不一定是唯一的。 ) 

</dd> <dt>

**FirmwareDevicePath**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

固件用來描述裝置的原生路徑。

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

在具現化命名空間的範圍內，InstanceID 會以不透明和唯一的方式識別此類別的實例。 若要確保命名空間中的唯一性，InstanceID 的值應使用下列「慣用」演算法來建立： *OrgID*：*LocalID* ，其中 *OrgID* 和 *LocalID* 會以冒號 (： ) ，而且 *OrgID* 必須包含受著作權、商標或其他唯一名稱，而該名稱是由建立或定義 InstanceID 的商務實體所擁有，或是由可辨識的全域授權單位指派給商務實體的註冊識別碼。  (這項需求類似于架構類別名稱的 *SchemaName* \_ *ClassName* 結構。 ) 此外，為了確保唯一性， *OrgID* 不能包含冒號 (： ) 。 使用此演算法時，InstanceID 中出現的第一個冒號必須出現在 *OrgID* 和 *LocalID* 之間。 *LocalID* 由商務實體選擇，不應重複使用，以找出不同的基礎 (真實世界) 元素。 如果未使用上述的慣用演算法，則定義實體必須確保產生的 InstanceID 不會在這個實例的命名空間或其他提供者所產生的任何 InstanceIDs 上重複使用。 針對 DMTF 定義的實例，您必須使用「慣用」演算法搭配將 *OrgID* 設定為 CIM。

</dd> <dt>

**OptionalData**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **OctetString**， [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) 
</dt> </dl>

由固件提供的選擇性資料。

> [!Note]  
> 在 Windows 10 中新增的屬性。

 

</dd> <dt>

**OtherLocation**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

其他位置資訊（如果有的話），以供固件用來進一步識別開機來源。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8.1 桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 R2 \[ desktop 應用程式\]<br/>                                                 |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> <dt>

[**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))
</dt> </dl>

 


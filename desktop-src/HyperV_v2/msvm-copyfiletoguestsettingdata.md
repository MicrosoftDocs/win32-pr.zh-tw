---
description: 代表將檔案從主機複製到來賓的參數。
ms.assetid: 255F4132-C212-4A3B-A9B8-3F531E7D1CF9
title: Msvm_CopyFileToGuestSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestSettingData
- Msvm_CopyFileToGuestSettingData.Description
- Msvm_CopyFileToGuestSettingData.Caption
- Msvm_CopyFileToGuestSettingData.InstanceID
- Msvm_CopyFileToGuestSettingData.ElementName
- Msvm_CopyFileToGuestSettingData.OverwriteExisting
- Msvm_CopyFileToGuestSettingData.CreateFullPath
- Msvm_CopyFileToGuestSettingData.SourcePath
- Msvm_CopyFileToGuestSettingData.DestinationPath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6eb011ec8d03153bd5f1b7d956775327d2582410e9ca12591e19a39ddb4af5fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118148837"
---
# <a name="msvm_copyfiletoguestsettingdata-class"></a>Msvm \_ CopyFileToGuestSettingData 類別

代表將檔案從主機複製到來賓的參數。 此類別衍生自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[AMENDMENT]
class Msvm_CopyFileToGuestSettingData : CIM_SettingData
{
  string  Description;
  string  Caption;
  string  InstanceID;
  string  ElementName;
  boolean OverwriteExisting;
  boolean CreateFullPath;
  string  SourcePath;
  string  DestinationPath;
};
```

## <a name="members"></a>成員

**Msvm \_ CopyFileToGuestSettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ CopyFileToGuestSettingData** 類別具有這些屬性。

<dl> <dt>

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

**CreateFullPath**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

表示複製檔案之前，是否必須先建立目的地檔案路徑中的遺失目錄。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的文字描述。

</dd> <dt>

**DestinationPath**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

要複製之目的檔的完整路徑。 此目的地檔案必須可供來賓存取，而且可以包含環境變數（由來賓展開）。 如果指定的路徑是來賓中的現有目錄，則會在此目錄中建立目的地檔案。 在此情況下， **SourcePath** 的檔案名會用來做為目的地檔案名。

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此 SettingData 實例的顯示名稱。 此外，顯示名稱可以當做搜尋或查詢的索引屬性使用。  (附注：名稱在命名空間中不一定是唯一的。 ) 

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

**OverwriteExisting**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否必須覆寫現有的目的地檔案。

</dd> <dt>

**SourcePath**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

要複製之原始程式檔的完整路徑。 Hyper-v 主機必須可存取此來源檔案，而且可以包含由 Hyper-v 主機擴充的環境變數。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[僅限桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | Windows Server 2012\[僅限 R2 desktop 應用程式\]<br/>                                                 |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> <dt>

[**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))
</dt> </dl>

 


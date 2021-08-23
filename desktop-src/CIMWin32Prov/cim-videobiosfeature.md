---
description: CIM \_ VideoBIOSFeature 類別代表用來設定及存取電腦系統之視訊控制器和顯示器的低層級軟體的功能。
ms.assetid: a12ca387-5b12-487f-84fd-381afe266338
ms.tgt_platform: multiple
title: CIM_VideoBIOSFeature 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoBIOSFeature
- CIM_VideoBIOSFeature.Caption
- CIM_VideoBIOSFeature.CharacteristicDescriptions
- CIM_VideoBIOSFeature.Characteristics
- CIM_VideoBIOSFeature.Description
- CIM_VideoBIOSFeature.IdentifyingNumber
- CIM_VideoBIOSFeature.InstallDate
- CIM_VideoBIOSFeature.Name
- CIM_VideoBIOSFeature.ProductName
- CIM_VideoBIOSFeature.Status
- CIM_VideoBIOSFeature.Vendor
- CIM_VideoBIOSFeature.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b84ec8a1f9a00b29e21706dd7fabe978740cb756675952b061d406dad8e233c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020756"
---
# <a name="cim_videobiosfeature-class"></a>CIM \_ VideoBIOSFeature 類別

**CIM \_ VideoBIOSFeature** 類別代表用來設定及存取電腦系統之視訊控制器和顯示器的低層級軟體的功能。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[UUID("{BAE20634-E3D4-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_VideoBIOSFeature : CIM_SoftwareFeature
{
  string   Caption;
  string   CharacteristicDescriptions[];
  uint16   Characteristics[];
  string   Description;
  string   IdentifyingNumber;
  datetime InstallDate;
  string   Name;
  string   ProductName;
  string   Status;
  string   Vendor;
  string   Version;
};
```

## <a name="members"></a>成員

**CIM \_ VideoBIOSFeature** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ VideoBIOSFeature** 類別具有這些屬性。

<dl> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) 
</dt> </dl>

物件的簡短文字描述。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**CharacteristicDescriptions**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| VIDEO BIOS 特性 \| 001.4 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VideoBIOSFeature**。**特性**") 
</dt> </dl>

提供 **特性** 陣列中所指出的影片 BIOS 功能詳細描述的自由格式字串。

> [!Note]  
> 這個陣列的每個專案都與 **特性** 陣列中位於相同索引的專案有關。

 

</dd> <dt>

**特性**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| VIDEO BIOS 特性 \| 001.3 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VideoBIOSFeature**。**CharacteristicDescriptions**") 
</dt> </dl>

影片 BIOS 所支援的功能。 例如，可能會指出支援 VESA 電源管理或影片 BIOS 遮蔽。 值 3 ( 「未知」 ) 在 CIM 架構中無效，因為它代表 DMI 中不支援任何 BIOS 功能。 在這種情況下，不應該具現化物件。

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (2) 


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

**未定義** (3) 


</dt> <dd></dd> <dt>

<span id="Standard_Video_BIOS"></span><span id="standard_video_bios"></span><span id="STANDARD_VIDEO_BIOS"></span>

**標準 VIDEO BIOS** (4) 


</dt> <dd></dd> <dt>

<span id="VESA_BIOS_Extensions_Supported"></span><span id="vesa_bios_extensions_supported"></span><span id="VESA_BIOS_EXTENSIONS_SUPPORTED"></span>

 (5) **支援 VESA BIOS 擴充** 功能


</dt> <dd></dd> <dt>

<span id="VESA_Power_Management_Supported"></span><span id="vesa_power_management_supported"></span><span id="VESA_POWER_MANAGEMENT_SUPPORTED"></span>

**支援的 VESA 電源管理** (6) 


</dt> <dd></dd> <dt>

<span id="VESA_Display_Data_Channel_Supported"></span><span id="vesa_display_data_channel_supported"></span><span id="VESA_DISPLAY_DATA_CHANNEL_SUPPORTED"></span>

**支援的 VESA 顯示資料通道** (7) 


</dt> <dd></dd> <dt>

<span id="Video_BIOS_Shadowing_Allowed"></span><span id="video_bios_shadowing_allowed"></span><span id="VIDEO_BIOS_SHADOWING_ALLOWED"></span>

允許 (8) 的 **影片 BIOS 遮蔽**


</dt> <dd></dd> <dt>

<span id="Video_BIOS_Upgradeable"></span><span id="video_bios_upgradeable"></span><span id="VIDEO_BIOS_UPGRADEABLE"></span>

 (9) 的 **影片 BIOS 可升級**


</dt> <dd></dd> </dl>

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) 
</dt> </dl>

物件的文字描述。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**IdentifyingNumber**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 產品**](cim-product.md)」。**IdentifyingNumber**") ， [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| 元件 \| 001.4 ") 
</dt> </dl>

產品識別，例如軟體上的序號或硬體晶片上的骰子編號。 這個屬性繼承自 [**CIM \_ SoftwareFeature**](cim-softwarefeature.md)。

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") 
</dt> </dl>

物件的安裝日期和時間。 這個屬性不需要值來表示已安裝物件。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

資料處理系統外部已知物件的標籤。 此標籤是可唯一識別元素命名空間內容中專案的名稱。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**ProductName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 產品**](cim-product.md)」。**Name**") ， [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| 元件 \| 001.2 ") 
</dt> </dl>

常用的產品名稱。

這個屬性繼承自 [**CIM \_ SoftwareFeature**](cim-softwarefeature.md)。

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) 
</dt> </dl>

物件的目前狀態。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

包括下列值：

<dt>

<span id="OK"></span><span id="ok"></span>

**確定** ( [確定] ) 


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**錯誤** ( 「錯誤」 ) 


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**降級** ( 「降級」 ) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 ( 「未知」 ) 


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred 失敗** ( 「Pred 失敗」 ) 


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**開始** ( 「開始」 ) 


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**停止** ( 「正在停止」 ) 


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**服務** ( 「服務」 ) 


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**壓力** ( 「壓力」 ) 


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ( "NonRecover" ) 


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**沒有連絡人** ( 「沒有連絡人」 ) 


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**遺失的 comm** ( 「遺失的通訊」 ) 


</dt> <dd></dd> </dl>

</dd> <dt>

**廠商**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 產品**](cim-product.md)」。**廠商**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| 元件 \| 001.1 ") 
</dt> </dl>

產品供應商的名稱，其對應至 DMTF 解決方案之 product 物件中的 **廠商** 屬性，Exchange Standard (SES) 。

這個屬性繼承自 [**CIM \_ SoftwareFeature**](cim-softwarefeature.md)。

</dd> <dt>

**版本**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 產品**](cim-product.md)」。**Version**") 、 [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| 元件 \| 001.3 ") 
</dt> </dl>

產品版本資訊，對應至 DMTF SES product 物件中的 **version** 屬性。

這個屬性繼承自 [**CIM \_ SoftwareFeature**](cim-softwarefeature.md)。

</dd> </dl>

## <a name="remarks"></a>備註

**Cim \_ VideoBIOSFeature** 類別衍生自 [**cim \_ SoftwareFeature**](cim-softwarefeature.md)。

WMI 不會執行這個類別。

此檔衍生自 DMTF 所發佈的 CIM 類別描述。 Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。

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

[**CIM \_ SoftwareFeature**](cim-softwarefeature.md)
</dt> </dl>

 


---
description: 定義由 CIM VirtualSystemMigrationService 類別的實例所管理之虛擬系統移轉的設定 \_ 。
ms.assetid: c28ed48b-bacc-49c8-9131-2543c0edb3fd
title: CIM_VirtualSystemMigrationSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationSettingData
- CIM_VirtualSystemMigrationSettingData.MigrationType
- CIM_VirtualSystemMigrationSettingData.Priority
- CIM_VirtualSystemMigrationSettingData.Bandwidth
- CIM_VirtualSystemMigrationSettingData.BandwidthUnit
- CIM_VirtualSystemMigrationSettingData.OtherTransportType
- CIM_VirtualSystemMigrationSettingData.TransportType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 24a48877a4195d17398457912314186d0220ace8016a4c9cc3edd3e06c378ee4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950667"
---
# <a name="cim_virtualsystemmigrationsettingdata-class"></a>CIM \_ VirtualSystemMigrationSettingData 類別

定義由 [**CIM \_ VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) 類別的實例所管理之虛擬系統移轉的設定。

## <a name="syntax"></a>語法

``` syntax
[Experimental, Abstract, Version("2.20.0"), UMLPackagePath("CIM::System::Virtualization"), AMENDMENT]
class CIM_VirtualSystemMigrationSettingData : CIM_SettingData
{
  uint16 MigrationType;
  uint16 Priority;
  uint16 Bandwidth;
  string BandwidthUnit;
  string OtherTransportType;
  uint16 TransportType;
};
```

## <a name="members"></a>成員

**CIM \_ VirtualSystemMigrationSettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ VirtualSystemMigrationSettingData** 類別具有這些屬性。

<dl> <dt>

**頻寬**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：量測 [**計、**](/windows/desktop/WmiSdk/standard-qualifiers) [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (」**CIM \_ VirtualSystemMigrationSettingData**。**BandwidthUnit**") 
</dt> </dl>

指派給或要求進行虛擬系統移轉操作的頻寬。 "0" 是遷移要求的預設頻寬。

**頻寬** 和 **優先順序** 屬性可以搭配使用。 具有最高相等 **優先權** 值的遷移程式會根據其要求的頻寬共用可用的頻寬。 如果並非所有的頻寬都是由這組進程取用，則具有下一個較低 **優先順序** 值的遷移程式會共用剩餘的頻寬。 如果保留更多頻寬，則會考慮具有下一個較低 **優先順序** 值的遷移程式。

[ **頻寬** ] 屬性中所使用的單位是由 [ **BandwidthUnit** ] 屬性的值所指定。

如果 **BandwidthUnit** 屬性的值為 "percent"，則適用下列規則：

-   **頻寬** 屬性的值必須介於 "0" 和 "100" 之間，且值越高，表示較高的頻寬。
-   值為 "100" 表示執行虛擬系統移轉作業的所有可用頻寬。
-   "1" 和 "100" 之間的值會以線性方式與可用的頻寬範圍產生關聯。 例如，值為50時，會要求一半的可用頻寬。

</dd> <dt>

**BandwidthUnit**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ VirtualSystemMigrationSettingData**.**頻寬**」 ) 、 **IsPUnit**
</dt> </dl>

**頻寬** 屬性所使用的單位。 這個屬性的值應該是 DSP0004 2.4 或更新版本的附錄 C 中所定義之程式設計單位辨識符號的合法值。

> [!Note]  
> 諸如 DMTF DSP1081 等設定檔會定義用戶端如何探索執行所支援的單位集合，以及 **頻寬** 屬性值的範圍和增量。

 

</dd> <dt>

**MigrationType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

要執行的遷移作業類型。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Live"></span><span id="live"></span><span id="LIVE"></span>

**Live** (2) 


</dt> <dd></dd> <dt>

<span id="Resume"></span><span id="resume"></span><span id="RESUME"></span>

**繼續** (3) 


</dt> <dd></dd> <dt>

<span id="Restart"></span><span id="restart"></span><span id="RESTART"></span>

**重新開機** (4) 


</dt> <dd></dd> </dl>

</dd> <dt>

**OtherTransportType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ VirtualSystemMigrationSettingData**.**TransportType**") 
</dt> </dl>

如果 **TransportType** 的值為 "1" (其他) ，則為要套用的傳輸類型。

</dd> <dt>

**優先順序**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬系統移轉程式可能用來在多個暫止的遷移要求之間訂購或指派喜好設定的相對遷移重要性。 值愈低，優先順序愈高。 "0" 是遷移要求的預設頻寬。

</dd> <dt>

**TransportType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ VirtualSystemMigrationSettingData**.**OtherTransportType**") 
</dt> </dl>

要套用至虛擬系統移轉作業的傳輸類型。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="SSH"></span><span id="ssh"></span>

**SSH** (2) 


</dt> <dd></dd> <dt>

<span id="TLS"></span><span id="tls"></span>

**TLS** (3) 


</dt> <dd></dd> <dt>

<span id="TLS_Strict"></span><span id="tls_strict"></span><span id="TLS_STRICT"></span>

**TLS Strict** (4) 


</dt> <dd></dd> <dt>

<span id="TCP"></span><span id="tcp"></span>

**TCP** (5) 


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

**IPC** (6) 


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF 保留** ( .。。) 


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**廠商保留** (32768 ) 


</dt> <dd></dd> </dl>

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

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> </dl>

 


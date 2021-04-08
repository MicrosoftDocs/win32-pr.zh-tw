---
description: 代表遷移虛擬系統和附加至虛擬系統之存放裝置的遷移設定。
ms.assetid: 2d632fe2-31ee-4e4d-b2a6-c1d1f3b4d624
title: Msvm_VirtualSystemMigrationSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationSettingData
- Msvm_VirtualSystemMigrationSettingData.InstanceID
- Msvm_VirtualSystemMigrationSettingData.Caption
- Msvm_VirtualSystemMigrationSettingData.Description
- Msvm_VirtualSystemMigrationSettingData.ElementName
- Msvm_VirtualSystemMigrationSettingData.MigrationType
- Msvm_VirtualSystemMigrationSettingData.Priority
- Msvm_VirtualSystemMigrationSettingData.Bandwidth
- Msvm_VirtualSystemMigrationSettingData.BandwidthUnit
- Msvm_VirtualSystemMigrationSettingData.OtherTransportType
- Msvm_VirtualSystemMigrationSettingData.TransportType
- Msvm_VirtualSystemMigrationSettingData.RemoveSourceUnmanagedVhds
- Msvm_VirtualSystemMigrationSettingData.AvoidRemovingVHDs
- Msvm_VirtualSystemMigrationSettingData.CPUCappingMagnitude
- Msvm_VirtualSystemMigrationSettingData.CancelIfBlackoutThresholdExceeded
- Msvm_VirtualSystemMigrationSettingData.AllowOverwriteExistingFile
- Msvm_VirtualSystemMigrationSettingData.UnmanagedVhds
- Msvm_VirtualSystemMigrationSettingData.DestinationPlannedVirtualSystemId
- Msvm_VirtualSystemMigrationSettingData.DestinationIPAddressList
- Msvm_VirtualSystemMigrationSettingData.RetainVhdCopiesOnSource
- Msvm_VirtualSystemMigrationSettingData.EnableCompression
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 254884153b3f733691b1103a6eb57f204b5d1764
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847759"
---
# <a name="msvm_virtualsystemmigrationsettingdata-class"></a>Msvm \_ VirtualSystemMigrationSettingData 類別

代表遷移虛擬系統和附加至虛擬系統之存放裝置的遷移設定。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationSettingData : CIM_VirtualSystemMigrationSettingData
{
  string  InstanceID;
  string  Caption = "Migration Setting Data";
  string  Description = "Virtual System Migration Setting Data";
  string  ElementName;
  uint16  MigrationType;
  uint16  Priority;
  uint16  Bandwidth;
  string  BandwidthUnit;
  string  OtherTransportType;
  uint16  TransportType;
  boolean RemoveSourceUnmanagedVhds;
  boolean AvoidRemovingVHDs;
  uint16  CPUCappingMagnitude;
  boolean CancelIfBlackoutThresholdExceeded;
  boolean AllowOverwriteExistingFile;
  string  UnmanagedVhds[];
  string  DestinationPlannedVirtualSystemId;
  string  DestinationIPAddressList[];
  boolean RetainVhdCopiesOnSource;
  boolean EnableCompression;
};
```

## <a name="members"></a>成員

**Msvm \_ VirtualSystemMigrationSettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ VirtualSystemMigrationSettingData** 類別具有這些屬性。

<dl> <dt>

**AllowOverwriteExistingFile**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

允許儲存體遷移作業覆寫現有的 .vhdx 檔案。

> [!Note]  
> 這個屬性是在 Windows 10 1703 版中加入的。

 

</dd> <dt>

**AvoidRemovingVHDs**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

請勿在遷移期間移除任何 Vhd，也就是在目的地的 successand Vhd 中，來源的 Vhd 失敗。

> [!Note]  
> 已在 Windows 10、1703版和 Windows Server 2016 中新增。

 

</dd> <dt>

**頻寬**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定指派給或要求進行虛擬系統移轉作業的頻寬。 頻寬單位是由 **BandwidthUnit** 屬性所指定。 在遷移期間，0值表示預設頻寬。 否則，值為0表示不支援頻寬。

**頻寬** 和 **優先順序** 可以搭配使用。 具有最高相等優先權值的遷移程式會根據其要求的頻寬共用可用的頻寬。 如果並非所有的頻寬都是由這組進程取用，則下一個較低優先順序的遷移程式會共用剩餘的頻寬。 如果仍然有更多頻寬，則會考慮下一個較低優先順序的遷移程式等等。

這個屬性繼承自 **CIM \_ VirtualSystemMigrationSettingData**。

</dd> <dt>

**BandwidthUnit**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定 **頻寬** 屬性所使用的單位。 這個屬性的值必須是程式設計單位辨識符號的合法值，如 DSP0004 2.4 或更新版本的附錄 C. 1 中所定義。

如果這個屬性的值是 "percent"， **頻寬** 屬性的值必須介於0到100之間，且值越高，表示較高的頻寬。 值為100時，表示用來執行虛擬系統移轉作業的總可用頻寬。 介於1和100之間的值應與可用的頻寬範圍呈線性關聯。 例如，值為50時，應要求一半的可用頻寬。

這個屬性繼承自 **CIM \_ VirtualSystemMigrationSettingData**。

</dd> <dt>

**CancelIfBlackoutThresholdExceeded**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

如果超過掉電閾值時間，則取消遷移。

> [!Note]  
> 在 Windows 10 1709 版中新增。

 

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的簡短描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**CPUCappingMagnitude**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "CPUCappingMagnitude" ) 
</dt> </dl>

遷移期間 CPU 限定的程度。

> [!Note]  
> 在 Windows 10 1709 版中新增。

 

<dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

**一般** (0) 


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

**低** (1) 


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

**高** (2) 


</dt> <dd></dd> </dl>

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對物件的描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**DestinationIPAddressList**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

儲存體遷移將會是 **Null** 。 若為虛擬系統移轉，這可以包含目的地主機的 IP 位址清單。

</dd> <dt>

**DestinationPlannedVirtualSystemId**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

如果已規劃的虛擬機器存在於遷移目的地，則此屬性會設定為虛擬機器需要遷移的目的地已規劃虛擬機器的 GUID。 當使用者已在目的地建立計畫的虛擬機器，以及資源設定，並想要讓來源的虛擬機器遷移到此計畫的虛擬機器時，這非常有用。

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的顯示名稱。 這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。

</dd> <dt>

**EnableCompression**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出是否壓縮即時移轉流量。 **True** 表示要壓縮;否則 **為 False**。

**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

唯一識別此類別的實例。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**MigrationType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MigrationType" ) 
</dt> </dl>

指定要執行的遷移操作類型。 這個屬性繼承自 **CIM \_ VirtualSystemMigrationSettingData**。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="VirtualSystem"></span><span id="virtualsystem"></span><span id="VIRTUALSYSTEM"></span>

<span id="VirtualSystem"></span><span id="virtualsystem"></span><span id="VIRTUALSYSTEM"></span>**VirtualSystem** (32768) 


</dt> <dd>

將虛擬系統移轉至目的地主機。

</dd> <dt>

<span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>

<span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>**儲存體** (32769) 


</dt> <dd>

只遷移虛擬系統的儲存體資源。

</dd> <dt>

<span id="Staged"></span><span id="staged"></span><span id="STAGED"></span>

<span id="Staged"></span><span id="staged"></span><span id="STAGED"></span>**暫存** (32770) 


</dt> <dd>

使用虛擬系統設定，在目的地主機上建立已規劃的虛擬系統。

</dd> <dt>

<span id="VirtualSystemAndStorage"></span><span id="virtualsystemandstorage"></span><span id="VIRTUALSYSTEMANDSTORAGE"></span>

<span id="VirtualSystemAndStorage"></span><span id="virtualsystemandstorage"></span><span id="VIRTUALSYSTEMANDSTORAGE"></span>**VirtualSystemAndStorage** (32771) 


</dt> <dd>

將虛擬系統及其存放裝置遷移至目的地主機。

</dd> <dt>

<span id="StorageDeepCheck"></span><span id="storagedeepcheck"></span><span id="STORAGEDEEPCHECK"></span>

<span id="StorageDeepCheck"></span><span id="storagedeepcheck"></span><span id="STORAGEDEEPCHECK"></span>**StorageDeepCheck** (32772) 


</dt> <dd>

在目的地主機上執行虛擬系統儲存體資源遷移功能檢查。

</dd> </dl>

</dd> <dt>

**OtherTransportType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

如果 **TransportType** 的值為 1 (其他) ，則指定要套用的傳輸類型。 這個屬性繼承自 **CIM \_ VirtualSystemMigrationSettingData**。

</dd> <dt>

**優先順序**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定相對遷移的重要性，讓遷移系統可以用來排序，或在多個擱置中的遷移要求之間提供喜好設定。 值愈低，優先順序愈高。 在遷移期間，0值表示預設優先權。 否則，值為0表示不支援優先權。

這個屬性繼承自 **CIM \_ VirtualSystemMigrationSettingData**。

</dd> <dt>

**RemoveSourceUnmanagedVhds**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

移除來源非受控 Vhd。

> [!Note]  
> 在 Windows 10 和 Windows Server 2016 中新增。

 

</dd> <dt>

**RetainVhdCopiesOnSource**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

針對儲存體遷移，這會指定在完成遷移之後是否應移除來源主機上的唯讀 Vhd。

</dd> <dt>

**TransportType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "TransportType" ) 
</dt> </dl>

指定要套用至虛擬系統移轉作業的傳輸類型。 這個屬性繼承自 **CIM \_ VirtualSystemMigrationSettingData**。

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

針對即時移轉，此屬性會指定要用來將虛擬系統狀態傳送至目的地主機的傳輸類型。 支援的值為：

<dt>

<span id="TCP"></span><span id="tcp"></span>

<span id="TCP"></span><span id="tcp"></span>**TCP** (5) 


</dt> <dd>

指出 TCP 傳輸類型。

</dd> <dt>

<span id="SMB"></span><span id="smb"></span>

<span id="SMB"></span><span id="smb"></span>**SMB** (32768) 


</dt> <dd>

指出傳輸虛擬機器狀態的傳輸類型為 SMB。

</dd> </dl>

</dd> <dt>

**UnmanagedVhds**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， **HyperVEmbeddedInstance** ( "Msvm \_ MoveUnmanagedVhd" ) 
</dt> </dl>

內嵌 [**Msvm \_ MoveUnmanagedVhd**](msvm-moveunmanagedvhd.md) 實例的陣列，其中包含未受管理的 vhd 資訊。

> [!Note]  
> 在 Windows 10 和 Windows Server 2016 中新增。

 

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md)
</dt> <dt>

[**MigrateVirtualSystemToHost**](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 


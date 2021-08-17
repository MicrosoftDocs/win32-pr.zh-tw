---
description: 代表虛擬機器的虛擬化特定設定。
ms.assetid: BE81405E-E773-41CE-9441-33D60B63550E
title: Msvm_VirtualSystemSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSettingData
- Msvm_VirtualSystemSettingData.InstanceID
- Msvm_VirtualSystemSettingData.Caption
- Msvm_VirtualSystemSettingData.Description
- Msvm_VirtualSystemSettingData.ElementName
- Msvm_VirtualSystemSettingData.VirtualSystemIdentifier
- Msvm_VirtualSystemSettingData.VirtualSystemType
- Msvm_VirtualSystemSettingData.Notes
- Msvm_VirtualSystemSettingData.CreationTime
- Msvm_VirtualSystemSettingData.ConfigurationID
- Msvm_VirtualSystemSettingData.ConfigurationDataRoot
- Msvm_VirtualSystemSettingData.ConfigurationFile
- Msvm_VirtualSystemSettingData.SnapshotDataRoot
- Msvm_VirtualSystemSettingData.SuspendDataRoot
- Msvm_VirtualSystemSettingData.SwapFileDataRoot
- Msvm_VirtualSystemSettingData.LogDataRoot
- Msvm_VirtualSystemSettingData.AutomaticStartupAction
- Msvm_VirtualSystemSettingData.AutomaticStartupActionDelay
- Msvm_VirtualSystemSettingData.AutomaticStartupActionSequenceNumber
- Msvm_VirtualSystemSettingData.AutomaticShutdownAction
- Msvm_VirtualSystemSettingData.AutomaticRecoveryAction
- Msvm_VirtualSystemSettingData.RecoveryFile
- Msvm_VirtualSystemSettingData.BIOSGUID
- Msvm_VirtualSystemSettingData.BIOSSerialNumber
- Msvm_VirtualSystemSettingData.BaseBoardSerialNumber
- Msvm_VirtualSystemSettingData.ChassisSerialNumber
- Msvm_VirtualSystemSettingData.Architecture
- Msvm_VirtualSystemSettingData.ChassisAssetTag
- Msvm_VirtualSystemSettingData.BIOSNumLock
- Msvm_VirtualSystemSettingData.BootOrder
- Msvm_VirtualSystemSettingData.Parent
- Msvm_VirtualSystemSettingData.UserSnapshotType
- Msvm_VirtualSystemSettingData.IsSaved
- Msvm_VirtualSystemSettingData.AdditionalRecoveryInformation
- Msvm_VirtualSystemSettingData.AllowFullSCSICommandSet
- Msvm_VirtualSystemSettingData.DebugChannelId
- Msvm_VirtualSystemSettingData.DebugPortEnabled
- Msvm_VirtualSystemSettingData.DebugPort
- Msvm_VirtualSystemSettingData.Version
- Msvm_VirtualSystemSettingData.IncrementalBackupEnabled
- Msvm_VirtualSystemSettingData.VirtualNumaEnabled
- Msvm_VirtualSystemSettingData.AllowReducedFcRedundancy
- Msvm_VirtualSystemSettingData.VirtualSystemSubType
- Msvm_VirtualSystemSettingData.BootSourceOrder
- Msvm_VirtualSystemSettingData.PauseAfterBootFailure
- Msvm_VirtualSystemSettingData.NetworkBootPreferredProtocol
- Msvm_VirtualSystemSettingData.GuestControlledCacheTypes
- Msvm_VirtualSystemSettingData.AutomaticSnapshotsEnabled
- Msvm_VirtualSystemSettingData.IsAutomaticSnapshot
- Msvm_VirtualSystemSettingData.GuestStateFile
- Msvm_VirtualSystemSettingData.GuestStateDataRoot
- Msvm_VirtualSystemSettingData.LockOnDisconnect
- Msvm_VirtualSystemSettingData.ParentPackage
- Msvm_VirtualSystemSettingData.AutomaticCriticalErrorActionTimeout
- Msvm_VirtualSystemSettingData.AutomaticCriticalErrorAction
- Msvm_VirtualSystemSettingData.ConsoleMode
- Msvm_VirtualSystemSettingData.SecureBootEnabled
- Msvm_VirtualSystemSettingData.SecureBootTemplateId
- Msvm_VirtualSystemSettingData.LowMmioGapSize
- Msvm_VirtualSystemSettingData.HighMmioGapSize
- Msvm_VirtualSystemSettingData.EnhancedSessionTransportType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fb57c7b96a6e2cd1839f4d830074bb69d742aef688325a37d61b67589d026436
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147891"
---
# <a name="msvm_virtualsystemsettingdata-class"></a>Msvm \_ VirtualSystemSettingData 類別

代表虛擬機器的虛擬化特定設定。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemSettingData : CIM_VirtualSystemSettingData
{
  string   InstanceID;
  string   Caption = "Virtual Machine Settings";
  string   Description;
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
  string   BIOSGUID;
  string   BIOSSerialNumber;
  string   BaseBoardSerialNumber;
  string   ChassisSerialNumber;
  string   Architecture;
  string   ChassisAssetTag;
  boolean  BIOSNumLock;
  uint16   BootOrder[];
  string   Parent;
  uint16   UserSnapshotType;
  boolean  IsSaved;
  string   AdditionalRecoveryInformation;
  boolean  AllowFullSCSICommandSet;
  uint32   DebugChannelId;
  uint16   DebugPortEnabled;
  uint32   DebugPort;
  string   Version;
  boolean  IncrementalBackupEnabled;
  boolean  VirtualNumaEnabled;
  boolean  AllowReducedFcRedundancy = False;
  string   VirtualSystemSubType;
  string   BootSourceOrder[];
  boolean  PauseAfterBootFailure;
  uint16   NetworkBootPreferredProtocol;
  boolean  GuestControlledCacheTypes;
  boolean  AutomaticSnapshotsEnabled;
  boolean  IsAutomaticSnapshot;
  string   GuestStateFile;
  string   GuestStateDataRoot;
  boolean  LockOnDisconnect;
  string   ParentPackage;
  datetime AutomaticCriticalErrorActionTimeout;
  uint16   AutomaticCriticalErrorAction;
  uint16   ConsoleMode;
  boolean  SecureBootEnabled;
  string   SecureBootTemplateId;
  uint64   LowMmioGapSize;
  uint64   HighMmioGapSize;
  uint16   EnhancedSessionTransportType;
};
```

## <a name="members"></a>成員

**Msvm \_ VirtualSystemSettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ VirtualSystemSettingData** 類別具有這些屬性。

<dl> <dt>

**AdditionalRecoveryInformation**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

針對復原動作提供的任何其他資訊。 這個屬性的意義是由 **AutomaticRecoveryAction** 中的動作所定義。 如果 **AutomaticRecoveryAction** 為 0 ( 「無」 ) 或 1 ( 「重新開機」 ) ，則此值為 **Null**。 如果 **AutomaticRecoveryAction** 為 2 ( 「還原為快照集」 ) ，這就是在虛擬機器工作者進程失敗時應套用的快照集的物件路徑。

</dd> <dt>

**AllowFullSCSICommandSet**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

如果從客體作業系統的 SCSI 命令傳遞至傳遞磁片，**則為 True** 。否則 **為 False**。 若 **為 True**，則不會篩選由客體作業系統向傳遞磁片發出的 SCSI 命令。 我們建議在生產環境部署中維持 SCSI 篩選功能。

</dd> <dt>

**AllowReducedFcRedundancy**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指定是否允許以虛擬光纖通道介面卡設定的虛擬機器進行即時移轉至目的地電腦，該目的地電腦的目標光纖通道裝置可能沒有或減少路徑。 這個屬性應該在即時移轉後清除。



| 值                                                                            | 意義                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>False</dt> </dl> | 虛擬機器無法即時移轉到目的電腦上，目標光纖通道裝置可能沒有或減少路徑。<br/>                                                                                                     |
| <dl> <dt>True</dt> </dl>  | 虛擬機器可以即時移轉至目的電腦，而目的電腦的目標光纖通道裝置可能沒有或減少路徑。 客體作業系統可能會中斷與儲存體的連線，而且可能會以無法預期的方式運作。<br/> |



 

</dd> <dt>

**架構**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此系統的架構。

> [!Note]  
> 在 Windows 10 1709 版中新增。

 

<dt>

<span id="x64"></span><span id="X64"></span>

**x64** () 


</dt> <dd></dd> <dt>

<span id="arm64"></span><span id="ARM64"></span>

**arm64** () 


</dt> <dd></dd> </dl>

</dd> <dt>

**AutomaticCriticalErrorAction**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

識別當發生重大錯誤（例如儲存體中斷連線）時，要在 VM 上採取的動作。

> [!Note]  
> 加入 Windows 10 和 Windows Server 2016。

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**無** (0) 


</dt> <dd>

對於重大錯誤狀況，並不會採取任何特定動作。

</dd> <dt>

<span id="Pause_Resume"></span><span id="pause_resume"></span><span id="PAUSE_RESUME"></span>

<span id="Pause_Resume"></span><span id="pause_resume"></span><span id="PAUSE_RESUME"></span>**暫停繼續** (1) 


</dt> <dd>

導致 VM 暫停，並在嚴重錯誤狀況解決時自動繼續。

</dd> </dl>

</dd> <dt>

**AutomaticCriticalErrorActionTimeout**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**子類型**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "interval" ) 
</dt> </dl>

識別將執行 **AutomaticCriticalErrorAction** 以解決重大錯誤的最長持續時間。 只有當 **AutomaticCriticalErrorAction** 屬性的值不是 0 (無) 時，才適用這種情況。 當超時時間過期時，VM 將會關閉電源。 此值會無條件進位到最接近的分鐘數。 值為0表示 VM 應該在遇到重大錯誤狀況時立即關閉電源。

> [!Note]  
> 加入 Windows 10 和 Windows Server 2016。

 

</dd> <dt>

**AutomaticRecoveryAction**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

當虛擬機器執行的軟體失敗時，針對虛擬機器所採取的動作。 在此情況下，失敗表示主機平臺偵測到失敗，例如不可中斷等候狀態條件。 這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。

這可以是下列其中一個值。



| 值                                                                               | 意義                        |
|-------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>2</dt> </dl>        | 無。<br/>               |
| <dl> <dt>3</dt> </dl>        | 重新啟動。<br/>            |
| <dl> <dt>4</dt> </dl>        | 還原為快照集。<br/> |
| <dl> <dt>5. 32768</dt> </dl> | 保留的。<br/>           |



 

</dd> <dt>

**AutomaticShutdownAction**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

當主機關閉時，為虛擬機器採取的動作。 這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。

這可以是下列其中一個值。



| 值                                                                               | 意義                |
|-------------------------------------------------------------------------------------|------------------------|
| <dl> <dt>2</dt> </dl>        | 關閉。<br/>   |
| <dl> <dt>3</dt> </dl>        | 儲存狀態。<br/> |
| <dl> <dt>4</dt> </dl>        | 關機。<br/>   |
| <dl> <dt>5. 32768</dt> </dl> | 保留的。<br/>   |



 

</dd> <dt>

**AutomaticSnapshotsEnabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出此虛擬機器是否應啟用自動快照集。

> [!Note]  
> 在 Windows 10 1709 版中新增。

 

</dd> <dt>

**AutomaticStartupAction**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

當主機啟動時，對虛擬機器採取的動作。 這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。

這可以是下列其中一個值。



| 值                                                                               | 意義                                  |
|-------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>2</dt> </dl>        | 無。<br/>                         |
| <dl> <dt>3</dt> </dl>        | 如果之前為作用中，則重新開機。<br/> |
| <dl> <dt>4</dt> </dl>        | 永遠啟動。<br/>                 |
| <dl> <dt>5. 32768</dt> </dl> | 保留的。<br/>                     |



 

</dd> <dt>

**AutomaticStartupActionDelay**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬機器自動啟動之前的延遲時間。 這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。

</dd> <dt>

**AutomaticStartupActionSequenceNumber**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

數位，指出主機系統啟動時的虛擬機器啟用的相對順序。 較低的數位表示先前的啟用。 如果有一或多個設定顯示相同的值，則序列會相依。 值為0時，表示序列與實值相依。 這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。

</dd> <dt>

**BaseBoardSerialNumber**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

虛擬機器基本板的序號。

</dd> <dt>

**BIOSGUID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

虛擬機器之 BIOS 的全域唯一識別碼。

</dd> <dt>

**BIOSNumLock**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

如果 BIOS 將 num lock 鍵設為 on，則為 **True** ;如果 BIOS 將 num lock 鍵設定為 off，則 **為 False** 。

</dd> <dt>

**BIOSSerialNumber**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

虛擬機器之 BIOS 的序號。

</dd> <dt>

**BootOrder**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (4) 
</dt> </dl>

在虛擬機器的 BIOS 內設定的開機順序。 這個屬性是值的陣列， **BootOrder** \[ 0 \] 到 **BootOrder** \[ 3 （含）， \] 其中每個值表示要開機的裝置。 陣列中的每個值都必須設定，而且不得與陣列中的另一個值相同。 虛擬機器將會先嘗試從陣列中第一個值所指示的裝置開機。 如果該裝置不包含開機磁區，虛擬機器將會嘗試從 **BootOrder** 屬性所指定的下一個裝置開機，依此類推。 如果 **BootOrder** 中未指定任何裝置包含開機磁區，則虛擬機器將無法開機。 虛擬機器的預設值為 \[ 0、1、2、3 \] 。

<dt>

<span id="Floppy"></span><span id="floppy"></span><span id="FLOPPY"></span>

<span id="Floppy"></span><span id="floppy"></span><span id="FLOPPY"></span>**軟盤機** (0) 


</dt> <dd>

虛擬機器會嘗試從磁片磁碟機中的磁片磁碟機開機。

</dd> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>

<span id="CD-ROM"></span><span id="cd-rom"></span>**Cd-rom** (1) 


</dt> <dd>

虛擬機器會嘗試從第一部 CD 或以開機磁區找到的 DVD 磁片開機。

</dd> <dt>

<span id="IDE_Hard_Drive"></span><span id="ide_hard_drive"></span><span id="IDE_HARD_DRIVE"></span>

<span id="IDE_Hard_Drive"></span><span id="ide_hard_drive"></span><span id="IDE_HARD_DRIVE"></span>**IDE 硬碟** (2) 


</dt> <dd>

虛擬機器會嘗試從開機磁區所找到的第一個硬碟機開機。

</dd> <dt>

<span id="PXE_Boot"></span><span id="pxe_boot"></span><span id="PXE_BOOT"></span>

<span id="PXE_Boot"></span><span id="pxe_boot"></span><span id="PXE_BOOT"></span>**PXE 開機** (3) 


</dt> <dd>

虛擬機器會嘗試從網路進行 PXE 開機。

</dd> <dt>

<span id="SCSI_Hard_Drive"></span><span id="scsi_hard_drive"></span><span id="SCSI_HARD_DRIVE"></span>

<span id="SCSI_Hard_Drive"></span><span id="scsi_hard_drive"></span><span id="SCSI_HARD_DRIVE"></span>**SCSI 硬碟** (4) 


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**保留** (5. 65535) 


</dt> <dd></dd> </dl>

</dd> <dt>

**BootSourceOrder**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

虛擬機器的開機來源順序。

**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的簡短描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**ChassisAssetTag**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

虛擬機器底座的資產標記。

</dd> <dt>

**ChassisSerialNumber**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

虛擬機器底座的序號。

</dd> <dt>

**ConfigurationDataRoot**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

儲存虛擬機器設定相關資訊之目錄的路徑。 這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。

</dd> <dt>

**ConfigurationFile**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

儲存虛擬機器設定相關資訊之檔案的相對路徑和檔案名。 此路徑相對於 **ConfigurationDataRoot** 屬性。 這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。

</dd> <dt>

**ConfigurationID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬機器設定的唯一識別碼。 這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。

</dd> <dt>

**ConsoleMode**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

識別 VM 的主控台模式。

> [!Note]  
> 此屬性已加入 Windows 10 和 Windows Server 2016 中。

 

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

**預設** (0) 


</dt> <dd></dd> <dt>

<span id="COM1"></span><span id="com1"></span>

**COM1** (1) 


</dt> <dd></dd> <dt>

<span id="COM2"></span><span id="com2"></span>

**COM2** (2) 


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**無** (3) 


</dt> <dd></dd> </dl>

</dd> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

建立虛擬機器設定的日期和時間。 如果此物件代表目前的虛擬機器設定，則此值會是系統建立的時間。 如果此物件代表虛擬機器的快照集設定，則此值會是拍攝快照集的時間。 這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。

</dd> <dt>

**DebugChannelId**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

用來使用統一的偵錯工具來偵測虛擬機器的通道識別碼。

</dd> <dt>

**DebugPort**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

用來使用綜合調試來偵測虛擬機器的 TCP/IP 通訊埠。

</dd> <dt>

**DebugPortEnabled**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指定虛擬機器是否正在使用綜合的偵錯工具。 這可以是下列其中一個值。

<dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>**Off** (0) 


</dt> <dd></dd> <dt>

<span id="On"></span><span id="on"></span><span id="ON"></span>

<span id="On"></span><span id="on"></span><span id="ON"></span>**(1**) 


</dt> <dd></dd> <dt>

<span id="OnAutoAssigned"></span><span id="onautoassigned"></span><span id="ONAUTOASSIGNED"></span>

<span id="OnAutoAssigned"></span><span id="onautoassigned"></span><span id="ONAUTOASSIGNED"></span>**OnAutoAssigned** (2) 


</dt> <dd>

自動指派

</dd> </dl>

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對物件的描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為下列其中一個值。



| 值                                                                                                                  | 意義                                               |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>「虛擬機器的作用中設定」</dt> </dl>   | 此實例會參考虛擬機器。<br/> |
| <dl> <dt>「虛擬機器的快照集設定」</dt> </dl> | 此實例會參考快照集。<br/>        |



 

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的顯示名稱。 這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，而且一律設定為電腦的顯示名稱。 此名稱的長度不得超過100個字元。

</dd> <dt>

**EnhancedSessionTransportType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

表示連接到增強的會話時要使用的傳輸類型。

> [!Note]  
> 這個屬性是在 Windows 10 1803 版中加入的。

 

<dt>

<span id="VMBus_Pipe"></span><span id="vmbus_pipe"></span><span id="VMBUS_PIPE"></span>

**VMBus 管道** (0) 


</dt> <dd></dd> <dt>

<span id="Hyper-V_Socket"></span><span id="hyper-v_socket"></span><span id="HYPER-V_SOCKET"></span>

**Hyper-v 通訊端** (1) 


</dt> <dd></dd> </dl>

</dd> <dt>

**GuestControlledCacheTypes**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出來賓是否可以控制快取類型。

> [!Note]  
> 加入 Windows 10 和 Windows Server 2016。

 

</dd> <dt>

**GuestStateDataRoot**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

儲存來賓執行時間狀態相關資訊之目錄的 Filepath。

> [!Note]  
> 在 Windows 10 1709 版中新增。

 

</dd> <dt>

**GuestStateFile**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

儲存來賓執行時間狀態相關資訊之檔案的檔路徑。 相對路徑會附加至 **GuestStateDataRoot** 屬性的值。

> [!Note]  
> 在 Windows 10 1709 版中新增。

 

</dd> <dt>

**HighMmioGapSize**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

高 (超過 4GB) Memory-Mapped IO 間隙（MB）的大小

> [!Note]  
> 這個屬性是在 Windows 10 1703 版中加入的。

 

</dd> <dt>

**IncrementalBackupEnabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出 Hyper-v VSS 寫入器是否支援採用此虛擬機器的增量備份。

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

唯一識別此類別的實例。 這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。

</dd> <dt>

**IsAutomaticSnapshot**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出這是否為使用者自動建立的快照集。

> [!Note]  
> 在 Windows 10 1709 版中新增。

 

</dd> <dt>

**IsSaved**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

如果設定具有已儲存狀態檔案的參考，則 **為 True** ;否則 **為 False**。 這並不表示這類檔案是否存在，只是設定會指定一個。

</dd> <dt>

**LockOnDisconnect**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

中斷與 vmconnect 的連線時，請鎖定主控台。

> [!Note]  
> 加入 Windows 10 和 Windows Server 2016。

 

</dd> <dt>

**LogDataRoot**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

儲存虛擬機器記錄資訊之目錄的路徑。 這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。

</dd> <dt>

**LowMmioGapSize**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

設定虛擬機器 (VM) 的第一個 MMIO 間距大小（以 mb 為單位）。

**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。

範圍： 128 3584

</dd> <dt>

**NetworkBootPreferredProtocol**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

判斷 PXE 開機慣用的通訊協定是 IPv4 或 IPv6。

**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。

<dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

**IPv4** (4096) 


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

**IPv6** (4097) 


</dt> <dd></dd> </dl>

</dd> <dt>

**注意事項**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

與虛擬機器相關的使用者提供的附注。 這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。

</dd> <dt>

**父系**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

如果這個實例不是以虛擬機器的快照集為基礎的系統，則此屬性為 **Null**。 否則，屬性會保存這個實例所依據之 **Msvm \_ VirtualSystemSettingData** 物件的物件路徑。 建立虛擬機器的快照集樹狀結構階層時，這個屬性會參考目前的實例所衍生的物件 (目前的實例是子節點，而且這個屬性中所參考的物件是父節點。 ) 

</dd> <dt>

**ParentPackage**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

如果此系統為容器，則為 \_ 此系統所依據之 Msvm ContainerPackage 的路徑。

> [!Note]  
> 新增于 Windows 10;已在 Windows 10 1703 版中移除。

 

</dd> <dt>

**PauseAfterBootFailure**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出在每次開機專案失敗並等候使用者按下按鍵之後，BIOS 是否會暫停。 如果 BIOS 暫停，**則為 True** ;否則 **為 False**。

**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。

</dd> <dt>

**RecoveryFile**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

儲存虛擬機器修復相關資訊之檔案的完整路徑。 這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。

</dd> <dt>

**SecureBootEnabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出是否已啟用虛擬機器 (VM) 的安全開機。 如果已啟用，則 **為 True** ;否則 **為 False**。

> [!Note]  
> 只有第2代 Vm 才能啟用安全開機。

 

**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。

</dd> <dt>

**SecureBootTemplateId**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

UEFI 安全開機相關變數的初始值之範本的全域唯一識別碼。

這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyVirtualSystem**](https://www.bing.com/search?q=**ModifyVirtualSystem**)方法來變更。

> [!Note]  
> 加入 Windows 10 和 Windows Server 2016。

 

</dd> <dt>

**SnapshotDataRoot**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

儲存虛擬機器快照集相關資訊之目錄的路徑。 這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。

</dd> <dt>

**SuspendDataRoot**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

儲存虛擬機器暫停相關資訊之相關資訊的目錄路徑。 這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。

</dd> <dt>

**SwapFileDataRoot**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

儲存虛擬機器之交換檔的目錄路徑。 這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。

</dd> <dt>

**UserSnapshotType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

表示使用者定義的快照集類型。

> [!Note]  
> 加入 Windows 10 和 Windows Server 2016。

 

<dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**停** 用 (2) 


</dt> <dd>

停用建立任何快照集。

</dd> <dt>

<span id="ProductionFallbackToTest"></span><span id="productionfallbacktotest"></span><span id="PRODUCTIONFALLBACKTOTEST"></span>

<span id="ProductionFallbackToTest"></span><span id="productionfallbacktotest"></span><span id="PRODUCTIONFALLBACKTOTEST"></span>**ProductionFallbackToTest** (3) 


</dt> <dd>

要在生產環境中使用的資料一致性快照集。當無法使用建立資料一致快照集的功能時，執行具有應用程式狀態的快照集。

</dd> <dt>

<span id="ProductionNoFallback"></span><span id="productionnofallback"></span><span id="PRODUCTIONNOFALLBACK"></span>

<span id="ProductionNoFallback"></span><span id="productionnofallback"></span><span id="PRODUCTIONNOFALLBACK"></span>**ProductionNoFallback** (4) 


</dt> <dd>

要在生產環境中使用的資料一致性快照集。如果無法建立資料一致的快照集，則不會建立具有應用程式狀態的快照集。

</dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>**測試** (5) 


</dt> <dd>

包含適用于測試和開發用途之記憶體和裝置資訊的快照集。

</dd> </dl>

</dd> <dt>

**版本**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬機器的版本，格式為「主要. 次要」，例如 "2.0"。

</dd> <dt>

**VirtualNumaEnabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**Msvm \_ ProcessorSettingData**](msvm-processorsettingdata.md)。**MaxProcessorsPerNumaNode**"，"[**Msvm \_ MemorySettingData**](msvm-memorysettingdata.md)。**MaxMemoryBlocksPerNumaNode**") 
</dt> </dl>

如果虛擬的非統一記憶體存取 (NUMA) 節點投射到虛擬機器，則 **為 True** ;如果虛擬機器將會有單一節點，則 **為 False** 。 若 **為 True**，則會從 [**Msvm \_ ProcessorSettingData. MaxProcessorsPerNumaNode**](msvm-processorsettingdata.md) 和 [**Msvm \_ MemorySettingData. MaxMemoryBlocksPerNumaNode**](msvm-memorysettingdata.md) 屬性的值判斷投影到虛擬機器的虛擬 NUMA 節點數目。

</dd> <dt>

**VirtualSystemIdentifier**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "cim \_ VirtualSystemSettingData. VirtualSystemIdentifier" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**cim \_**](cim-computersystem.md)。**名稱**") 
</dt> </dl>

這項設定資料所屬之 CIM 非程式物件的名稱。 [**\_**](/windows/desktop/CIMWin32Prov/cim-computersystem) 這個屬性是 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))的覆寫。

</dd> <dt>

**VirtualSystemSubType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性的有效值為 Microsoft： Hyper-v：子類型：1和 Microsoft： Hyper-v：子類型：2。 第1代 VM 是子類型1。 第2代 VM 是子類型2。

**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

**Microsoft： hyper-v：子類型： 1** ( "Microsoft： Hyper-v：子類型： 1" ) 


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

**Microsoft： hyper-v：子類型： 2** ( "Microsoft： Hyper-v：子類型： 2" ) 


</dt> <dd></dd> </dl>

</dd> <dt>

**VirtualSystemType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定設定資料所代表的虛擬機器類型。 這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) 類別。 這會是下列其中一個值。



| 值                                                                                                                                 | 意義                                              |
|---------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>「Microsoft： Hyper-v： System：認識」</dt> </dl>                        | 已實現的虛擬機器。<br/>               |
| <dl> <dt>「Microsoft： Hyper-v： System：已規劃」</dt> </dl>                         | 規劃的虛擬機器。<br/>                |
| <dl> <dt>「Microsoft： Hyper-v： Snapshot：已實現」</dt> </dl>                      | 已實現之虛擬機器的快照集。<br/> |
| <dl> <dt>「Microsoft： Hyper-v： Snapshot： Recovery」</dt> </dl>                      | 復原虛擬機器的快照集。<br/> |
| <dl> <dt>「Microsoft： Hyper-v：快照集：已規劃」</dt> </dl>                       | 規劃之虛擬機器的快照集。<br/>  |
| <dl> <dt>「Microsoft： Hyper-v： Snapshot：缺少」</dt> </dl>                       | 遺漏的快照集。<br/>                       |
| <dl> <dt>"Microsoft： Hyper-v： Snapshot： Replica： Standard"</dt> </dl>              | 以時間為基礎的複寫點快照集。<br/>  |
| <dl> <dt>"Microsoft： Hyper-v： Snapshot： Replica： ApplicationConsistent"</dt> </dl> | VSS 複寫點快照集。<br/>         |
| <dl> <dt>"Microsoft： Hyper-v： Snapshot： Replica： PlannedFailover"</dt> </dl>       | 規劃的複寫快照集。<br/>           |



 

</dd> </dl>

## <a name="remarks"></a>備註

存取 **Msvm \_ VirtualSystemSettingData** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md)
</dt> <dt>

[**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))
</dt> <dt>

[虛擬系統類別](virtual-system-classes.md)
</dt> </dl>

 


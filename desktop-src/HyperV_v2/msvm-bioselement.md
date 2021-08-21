---
description: 代表載入 RAM 以設定及啟動系統的低層級軟體。
ms.assetid: D123601A-DEE6-43EA-BD95-1F7F0F2C2B43
title: Msvm_BIOSElement 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BIOSElement
- Msvm_BIOSElement.InstanceID
- Msvm_BIOSElement.Caption
- Msvm_BIOSElement.Description
- Msvm_BIOSElement.ElementName
- Msvm_BIOSElement.InstallDate
- Msvm_BIOSElement.OperationalStatus
- Msvm_BIOSElement.StatusDescriptions
- Msvm_BIOSElement.Status
- Msvm_BIOSElement.HealthState
- Msvm_BIOSElement.CommunicationStatus
- Msvm_BIOSElement.DetailedStatus
- Msvm_BIOSElement.OperatingStatus
- Msvm_BIOSElement.PrimaryStatus
- Msvm_BIOSElement.Name
- Msvm_BIOSElement.SoftwareElementState
- Msvm_BIOSElement.SoftwareElementID
- Msvm_BIOSElement.TargetOperatingSystem
- Msvm_BIOSElement.OtherTargetOS
- Msvm_BIOSElement.BuildNumber
- Msvm_BIOSElement.SerialNumber
- Msvm_BIOSElement.CodeSet
- Msvm_BIOSElement.IdentificationCode
- Msvm_BIOSElement.LanguageEdition
- Msvm_BIOSElement.Version
- Msvm_BIOSElement.Manufacturer
- Msvm_BIOSElement.PrimaryBIOS
- Msvm_BIOSElement.ListOfLanguages
- Msvm_BIOSElement.CurrentLanguage
- Msvm_BIOSElement.LoadedStartingAddress
- Msvm_BIOSElement.LoadedEndingAddress
- Msvm_BIOSElement.LoadUtilityInformation
- Msvm_BIOSElement.ReleaseDate
- Msvm_BIOSElement.RegistryURIs
- Msvm_BIOSElement.BIOSGUID
- Msvm_BIOSElement.BIOSSerialNumber
- Msvm_BIOSElement.BaseBoardSerialNumber
- Msvm_BIOSElement.ChassisSerialNumber
- Msvm_BIOSElement.ChassisAssetTag
- Msvm_BIOSElement.BIOSNumLock
- Msvm_BIOSElement.BootOrder
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8433c8fda6d438e4f77fb763be42467aab05ab976927f018e895a30d5f9c6226
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118149298"
---
# <a name="msvm_bioselement-class"></a>Msvm \_ BIOSElement 類別

代表載入 RAM 以設定及啟動系統的低層級軟體。 BIOS 不是邏輯裝置，因此不應該將虛擬 BIOS 視為虛擬機器裝置。 因為它不是裝置，所以沒有對應的資源集區。 BIOS 物件透過 [**Msvm \_ SystemBIOS**](msvm-systembios.md) 關聯與虛擬機器相關聯。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BIOSElement : CIM_BIOSElement
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   Name = "BIOS";
  uint16   SoftwareElementState = 2;
  string   SoftwareElementID = "Microsoft:GUID\device-specific data";
  uint16   TargetOperatingSystem = 0;
  string   OtherTargetOS;
  string   BuildNumber = 14;
  string   SerialNumber;
  string   CodeSet;
  string   IdentificationCode;
  string   LanguageEdition;
  string   Version = "8.02.00";
  string   Manufacturer = "Microsoft Corporation";
  boolean  PrimaryBIOS = True;
  string   ListOfLanguages[] = "en|US|iso8859-1";
  string   CurrentLanguage = "en|US|iso8859-1";
  unit64   LoadedStartingAddress = 0xE0000;
  unit64   LoadedEndingAddress = 0xFFFFF;
  string   LoadUtilityInformation;
  datetime ReleaseDate;
  string   RegistryURIs[];
  string   BIOSGUID;
  string   BIOSSerialNumber;
  string   BaseBoardSerialNumber;
  string   ChassisSerialNumber;
  string   ChassisAssetTag;
  boolean  BIOSNumLock;
  uint16   BootOrder[];
};
```

## <a name="members"></a>成員

**Msvm \_ BIOSElement** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ BIOSElement** 類別具有這些屬性。

<dl> <dt>

**BaseBoardSerialNumber**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬機器上基本板的序號。

</dd> <dt>

**BIOSGUID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

BIOS 的唯一識別碼。

</dd> <dt>

**BIOSNumLock**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

BIOS 中 Num Lock 的啟用狀態。

</dd> <dt>

**BIOSSerialNumber**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

BIOS 的序號。

</dd> <dt>

**BootOrder**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (4) 
</dt> </dl>

裝置將在啟動時搜尋開機磁區的順序。

</dd> <dt>

**BuildNumber**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **MaxLen** (64) 
</dt> </dl>

此軟體專案編譯的內部識別碼。 這個屬性繼承自 [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)，而且一律設定為14。

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **MaxLen** (64) 
</dt> </dl>

物件的簡短描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**ChassisAssetTag**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

建立虛擬機器時，會自動填入 BIOS。

</dd> <dt>

**ChassisSerialNumber**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

建立虛擬機器時，會自動填入 BIOS。

</dd> <dt>

**CodeSet**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **MaxLen** (64) 
</dt> </dl>

Software 元素所使用的程式碼集。 這個屬性繼承自 [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)，而且一律設定為 **Null**。

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出檢測與基礎受管理元素通訊的能力。 **Null** 值表示不會執行此屬性。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**CurrentLanguage**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

BIOS 目前選取的語言。 這個屬性繼承自 [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)，而且一律設定為 "en-us \| US \| iso8859-1"。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對物件的描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

補充具有其他狀態詳細資料的 **PrimaryStatus** 屬性。 **Null** 值表示不會執行此屬性。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

元素的顯示名稱。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定元素目前的健康情況。 這個屬性會表示此元素的健全狀況，但不一定是它的子元件。

發生重大錯誤時，請檢查事件記錄檔以取得詳細資料。 **EnabledState** 屬性也可以包含詳細資訊。 例如，當磁碟空間不足時， **HealthState** 會設定為25、虛擬機器暫停，而 **EnabledState** 設定為 32768 (暫停) 。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。



| 值                                                                                                                                                                                                                                                            | 意義                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <dt>**確定**</dt> <dt>5</dt> </dl>                                                                               | 虛擬機器完全正常運作，且在正常指令引數內運作，而且沒有錯誤。<br/>                                                                                                                                                                                    |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <dt>**重大失敗**</dt> <dt>20</dt> </dl>             | 虛擬機器發生重大故障。 當包含虛擬機器 Vhd 的一或多個磁片的磁碟空間不足，且虛擬機器已暫停時，就會使用此值。<br/>                                                                                                   |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <dt>**重大失敗**</dt> <dt>25</dt> </dl> | 元素沒有作用，而且可能無法復原。 這可能表示虛擬機器 (Vmwp.exe) 的工作者進程沒有回應控制或資訊要求，或是包含虛擬機器 Vhd 的一或多個磁片磁碟空間不足。<br/> |



 

</dd> <dt>

**IdentificationCode**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **MaxLen** (64) 
</dt> </dl>

此軟體元素的製造商識別碼。 通常這會是 (SKU) 或元件編號的庫存單位。 這個屬性繼承自 [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)，而且一律設定為 **Null**。

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

建立虛擬機器時，會自動填入 BIOS。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

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

**LanguageEdition**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **MaxLen** (32) 
</dt> </dl>

此軟體元素的語言版本。 這個屬性繼承自 [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)，而且一律設定為 **Null**。

</dd> <dt>

**ListOfLanguages**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

適用于 BIOS 的可安裝語言清單。 這個屬性繼承自 [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)，而且一律設定為 "en-us \| US \| iso8859-1"。

</dd> <dt>

**LoadedEndingAddress**
</dt> <dd> <dl> <dt>

資料類型： **unit64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此 BIOS 所佔用記憶體的結束位址。 這個屬性繼承自 [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)，而且一律設定為0xFFFFF。

</dd> <dt>

**LoadedStartingAddress**
</dt> <dd> <dl> <dt>

資料類型： **unit64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此 BIOS 所佔用記憶體的起始位址。 這個屬性繼承自 [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)，而且一律設定為0xE0000。

</dd> <dt>

**LoadUtilityInformation**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述更新 BIOS 元素所需的 BIOS flash/load 公用程式字串。 版本和其他資訊可能會顯示在此屬性中。 這個屬性繼承自 [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)，而且一律設定為 **Null**。

</dd> <dt>

**製造商**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **MaxLen** (256) 
</dt> </dl>

此 BIOS 的製造商。 這個屬性繼承自 [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)，而且一律設定為 "Microsoft Corporation"。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **MaxLen** (1024) 
</dt> </dl>

用來識別此軟體元素的名稱。 子類別化時，可以將這個屬性覆寫為索引鍵屬性。 這個屬性繼承自 [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)，一律設為 "BIOS"。

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。 **Null** 值表示不會執行此屬性。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

陣列，其中包含物件的目前狀態。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。 位於索引零 (0) 的值是下列其中一個值。



| 值                                                                                                                                                                                                                                                                   | 意義                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <dt>**確定**</dt> <dt>2</dt> </dl>                                                                                      | 虛擬機器正常運作，且正常運作。<br/>                                                                                                                                                                                              |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <dt>**降級**</dt> <dt>3</dt> </dl>                                         | 虛擬機器只能部分運作。 這表示無法存取包含設定的儲存體。 處於此狀態的虛擬機器只可關閉或刪除。 <br/>                                               |
| <span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span><dl> <dt>**預測性失敗**</dt> <dt>5</dt> </dl> | 虛擬機器可正常運作，但未來可能會失敗。 這表示包含虛擬機器虛擬硬碟的存放裝置可用空間不足。 如果沒有可用的磁碟空間，將會暫停虛擬機器。<br/> |
| <span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span><dl> <dt>**已停止**</dt> <dt>10</dt> </dl>                                            | 不支援這個值。 如果虛擬機器已停止，則 [ **EnabledState** ] 屬性的值會是3， ([已停用]) 。<br/>                                                                                                                       |
| <span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span><dl> <dt>**在服務**</dt> <dt>11</dt>中 </dl>                                | 虛擬機器正在處理要求。<br/>                                                                                                                                                                                                           |
| <span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span><dl> <dt>**休眠**</dt> <dt>15</dt> </dl>                                            | 不支援這個值。 如果虛擬機器已暫停或暫停，則 [ **EnabledState** ] 屬性的值會是 32769 ([已暫停]) 或 32768 (暫停) 。<br/>                                                                                    |



 

位於索引 1 (1) 的值是選擇性的，並包含次要狀態資訊。 用戶端應該使用索引零 (0) 的主要狀態，以判斷是否可以將新的要求發行至虛擬機器。 如果 **operationalstatus** \[ 0 \] 是 2 (確定) ，則由 **OperationalStatus** 1 指出的作業 \[ \] 可能會中斷。

在 **OperationalStatus** \[ 1 的值 \] 是下列其中一個值。



| 值                                                                                                                                                                                                                                                                                                   | 意義                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Creating_Snapshot"></span><span id="creating_snapshot"></span><span id="CREATING_SNAPSHOT"></span><dl> <dt>**正在建立快照**</dt>集 <dt>32768</dt> </dl>                                 | 正在為虛擬機器建立快照集。<br/>             |
| <span id="Applying_Snapshot"></span><span id="applying_snapshot"></span><span id="APPLYING_SNAPSHOT"></span><dl> 正在套用 <dt>**快照**</dt>集 <dt>32769</dt> </dl>                                 | 正在將快照集套用到虛擬機器。<br/>              |
| <span id="Deleting_Snapshot"></span><span id="deleting_snapshot"></span><span id="DELETING_SNAPSHOT"></span><dl> <dt>**正在刪除快照**</dt>集 <dt>32770</dt> </dl>                                 | 正在從虛擬機器刪除快照集。<br/>            |
| <span id="Waiting_to_Start"></span><span id="waiting_to_start"></span><span id="WAITING_TO_START"></span><dl> <dt>**正在等候開始**</dt> <dt>32771</dt> </dl>                                     | 虛擬機器將會在自動啟動延遲經過之後啟動。<br/> |
| <span id="Merging_Disks"></span><span id="merging_disks"></span><span id="MERGING_DISKS"></span><dl> <dt>**合併磁片**</dt> <dt>32772</dt> </dl>                                                 | 先前已刪除之快照集的虛擬硬碟正在合併。<br/>             |
| <span id="Exporting_Virtual_Machine"></span><span id="exporting_virtual_machine"></span><span id="EXPORTING_VIRTUAL_MACHINE"></span><dl> <dt>**正在匯出虛擬機器**</dt> <dt>32773</dt> </dl> | 正在匯出虛擬機器。<br/>                                             |
| <span id="Migrating_Virtual_Machine"></span><span id="migrating_virtual_machine"></span><span id="MIGRATING_VIRTUAL_MACHINE"></span><dl> 正在 <dt>**遷移虛擬機器**</dt> <dt>32774</dt> </dl> | 虛擬機器正在從一部實體電腦即時移轉至另一部電腦。<br/>  |



 

</dd> <dt>

**OtherTargetOS**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **MaxLen** (64) 
</dt> </dl>

當 **TargetOperatingSystem** 屬性的值為 1 (其他) （需要 **OtherTargetOS** 屬性必須有非 **Null** 值）時，軟體元素的製造商和作業系統。 對於 **TargetOperatingSystem** 的所有其他值， **OtherTargetOS** 屬性必須是 **Null**。 這個屬性繼承自 [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)，而且一律設定為 **Null**。

</dd> <dt>

**PrimaryBIOS**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若為 True，則這是電腦系統的主要 BIOS。 這個屬性繼承自 [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)，而且一律設定為 **True**。

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

提供高層級的狀態資訊。 這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態資訊。 **Null** 值表示不會執行此屬性。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**RegistryURIs**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

字串的陣列，表示執行符合的 BIOS 屬性登錄或登錄的發行位置。 這個屬性繼承自 [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)。

</dd> <dt>

**ReleaseDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

BIOS 的發行日期。 這個屬性繼承自 [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)。

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **MaxLen** (64) 
</dt> </dl>

指派的 BIOS 序號。 這個屬性繼承自 [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)。

</dd> <dt>

**SoftwareElementID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **MaxLen** (256) 
</dt> </dl>

Software 元素的識別碼。 這個屬性繼承自 [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)，且一律設定為 "Microsoft：*GUID* \\ *裝置特定資料*"。

</dd> <dt>

**SoftwareElementState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

軟體元素生命週期的狀態。 這個屬性繼承自 [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)，而且一律設定為 2 (可執行檔) 。

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **ArrayType** ( 「已編制索引」 ) 
</dt> </dl>

陣列，其中包含描述對應之 **OperationalStatus** 陣列值的字串。 例如，如果服務) 中的 11 (是指派給 **OperationalStatus** \[ 0 的值 \] ，則 **StatusDescriptions** \[ 0 \] 可能會包含虛擬機器處理要求的原因說明。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**TargetOperatingSystem**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

元素的作業系統環境。 這個屬性繼承自 [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)，且一律設定為 0 (未知) 。

</dd> <dt>

**版本**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **MaxLen** (64) 
</dt> </dl>

BIOS 的版本。 這個屬性繼承自 [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)，而且一律設定為 "8.02.00"。

</dd> </dl>

## <a name="remarks"></a>備註

存取 **Msvm \_ BIOSElement** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

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

[**CIM \_ BIOSElement**](cim-bioselement.md)
</dt> <dt>

[BIOS 類別](bios-classes.md)
</dt> <dt>

[**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)
</dt> </dl>

 


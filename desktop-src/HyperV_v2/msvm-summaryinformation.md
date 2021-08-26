---
description: 用於 Msvm VirtualSystemManagementService 類別中的 GetSummaryInformation 和 GetDefinitionFileSummaryInformation 方法 \_ ，以快速取得與虛擬機器或快照集相關的一般資訊。
ms.assetid: 8D188BB2-4A56-4738-94DD-64D9F9B90B73
title: Msvm_SummaryInformation 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SummaryInformation
- Msvm_SummaryInformation.InstanceID
- Msvm_SummaryInformation.AllocatedGPU
- Msvm_SummaryInformation.Shielded
- Msvm_SummaryInformation.AsynchronousTasks
- Msvm_SummaryInformation.CreationTime
- Msvm_SummaryInformation.ElementName
- Msvm_SummaryInformation.EnabledState
- Msvm_SummaryInformation.OtherEnabledState
- Msvm_SummaryInformation.GuestOperatingSystem
- Msvm_SummaryInformation.HealthState
- Msvm_SummaryInformation.Heartbeat
- Msvm_SummaryInformation.MemoryUsage
- Msvm_SummaryInformation.MemoryAvailable
- Msvm_SummaryInformation.AvailableMemoryBuffer
- Msvm_SummaryInformation.SwapFilesInUse
- Msvm_SummaryInformation.Name
- Msvm_SummaryInformation.Notes
- Msvm_SummaryInformation.Version
- Msvm_SummaryInformation.NumberOfProcessors
- Msvm_SummaryInformation.OperationalStatus
- Msvm_SummaryInformation.ProcessorLoad
- Msvm_SummaryInformation.ProcessorLoadHistory
- Msvm_SummaryInformation.Snapshots
- Msvm_SummaryInformation.StatusDescriptions
- Msvm_SummaryInformation.ThumbnailImage
- Msvm_SummaryInformation.ThumbnailImageHeight
- Msvm_SummaryInformation.ThumbnailImageWidth
- Msvm_SummaryInformation.UpTime
- Msvm_SummaryInformation.ReplicationState
- Msvm_SummaryInformation.ReplicationStateEx
- Msvm_SummaryInformation.ReplicationHealth
- Msvm_SummaryInformation.ReplicationHealthEx
- Msvm_SummaryInformation.ReplicationMode
- Msvm_SummaryInformation.TestReplicaSystem
- Msvm_SummaryInformation.ApplicationHealth
- Msvm_SummaryInformation.IntegrationServicesVersionState
- Msvm_SummaryInformation.MemorySpansPhysicalNumaNodes
- Msvm_SummaryInformation.ReplicationProviderId
- Msvm_SummaryInformation.EnhancedSessionModeState
- Msvm_SummaryInformation.VirtualSwitchNames
- Msvm_SummaryInformation.VirtualSystemSubType
- Msvm_SummaryInformation.HostComputerSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1f7cefc27c0e4adc507276d118bcca95c274d121
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886603"
---
# <a name="msvm_summaryinformation-class"></a>Msvm \_ SummaryInformation 類別

用於 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別中的 [**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)和 [**GetDefinitionFileSummaryInformation**](getdefinitionfilesummaryinformation-msvm-virtualsystemmanagementservice.md)方法，以快速取得與虛擬機器或快照集相關的一般資訊。

下列語法已簡化受控物件格式 (MOF) 程式碼。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SummaryInformation : Msvm_SummaryInformationBase
{
  string                       InstanceID;
  string                       AllocatedGPU;
  boolean                      Shielded;
  CIM_ConcreteJob              AsynchronousTasks[];
  DateTime                     CreationTime;
  string                       ElementName;
  uint16                       EnabledState;
  string                       OtherEnabledState;
  string                       GuestOperatingSystem;
  uint16                       HealthState;
  uint16                       Heartbeat;
  uint64                       MemoryUsage;
  sint32                       MemoryAvailable;
  sint32                       AvailableMemoryBuffer;
  boolean                      SwapFilesInUse;
  string                       Name;
  string                       Notes;
  string                       Version;
  uint16                       NumberOfProcessors;
  uint16                       OperationalStatus[];
  uint16                       ProcessorLoad;
  uint16                       ProcessorLoadHistory[];
  CIM_VirtualSystemSettingData Snapshots[];
  string                       StatusDescriptions[];
  uint8                        ThumbnailImage[];
  uint16                       ThumbnailImageHeight;
  uint16                       ThumbnailImageWidth;
  uint64                       UpTime;
  uint16                       ReplicationState;
  uint16                       ReplicationStateEx[];
  uint16                       ReplicationHealth;
  uint16                       ReplicationHealthEx[];
  uint16                       ReplicationMode;
  CIM_ComputerSystem       REF TestReplicaSystem;
  uint16                       ApplicationHealth;
  uint16                       IntegrationServicesVersionState;
  boolean                      MemorySpansPhysicalNumaNodes;
  string                       ReplicationProviderId[];
  uint16                       EnhancedSessionModeState;
  string                       VirtualSwitchNames[];
  string                       VirtualSystemSubType;
  string                       HostComputerSystemName;
};
```

## <a name="members"></a>成員

**Msvm \_ SummaryInformation** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ SummaryInformation** 類別具有這些屬性。

<dl> <dt>

**AllocatedGPU**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

實體圖形處理單元的識別碼 (GPU) 配置給此虛擬機器。 這個屬性只適用于使用 RemoteFX 的虛擬機器。

</dd> <dt>

**ApplicationHealth**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬機器目前的應用程式健康情況狀態。 對於代表虛擬機器快照集的 **Msvm \_ SummaryInformation** 實例而言，這個屬性是不正確。

<dt>

<span id="OK"></span><span id="ok"></span>

**確定** (2) 


</dt> <dd></dd> <dt>

<span id="Application_Critical"></span><span id="application_critical"></span><span id="APPLICATION_CRITICAL"></span>

**應用程式關鍵性** (32782) 


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**停用** (32896) 


</dt> <dd></dd> </dl>

</dd> <dt>

**AsynchronousTasks**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ ConcreteJob** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) 
</dt> </dl>

[**Msvm \_ ConcreteJob**](msvm-concretejob.md)實例的陣列，代表與目前正在執行之虛擬機器相關的任何非同步作業。 對於代表虛擬機器快照集的 **Msvm \_ SummaryInformation** 實例而言，這個屬性是不正確。

</dd> <dt>

**AvailableMemoryBuffer**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬機器的可用記憶體緩衝區百分比。 當虛擬機器啟用動態記憶體時，此屬性會表示可用記憶體緩衝區與虛擬機器理想記憶體緩衝區的比率。 理想的記憶體緩衝區大小是使用 [**Msvm \_ MemorySettingData**](msvm-memorysettingdata.md)類別的 **TargetMemoryBuffer** 屬性來設定。

對於代表未啟用動態記憶體之虛擬機器的 **Msvm \_ SummaryInformation** 類別實例而言，這個屬性是不正確。

這個屬性對於代表虛擬機器快照集的 **Msvm \_ SummaryInformation** 類別的實例而言是不正確。

</dd> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

資料類型： **DateTime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

建立虛擬機器或快照集的時間。

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬機器或快照的顯示名稱。

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬機器或快照的目前狀態。 如需可能的值，請參閱 Msvm 非程式類型類別的 **EnabledState** 屬性。 [**\_**](msvm-computersystem.md)

</dd> <dt>

**EnhancedSessionModeState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出主機是否允許增強模式連接，以及是否允許虛擬機器使用。

**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

**允許和可用** (2) 


</dt> <dd></dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

**不允許** (3) 


</dt> <dd></dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

**允許但無法使用** (6 ) 


</dt> <dd></dd> </dl>

</dd> <dt>

**GuestOperatingSystem**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

客體作業系統的名稱（如果有的話）。 如果無法使用這項資訊，則此屬性的值為 **Null**。 對於代表虛擬機器快照集的 **Msvm \_ SummaryInformation** 實例而言，這個屬性是不正確。

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬機器目前的健全狀況狀態。 對於代表虛擬機器快照集的 **Msvm \_ SummaryInformation** 實例而言，這個屬性是不正確。

</dd> <dt>

**活動訊號**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬機器目前的信號狀態。 如需詳細資訊，請參閱 **Msvm \_ HeartbeatComponent** 類別的 [**StatusDescriptions**](msvm-heartbeatcomponent.md)屬性檔。 對於代表虛擬機器快照集的 **Msvm \_ SummaryInformation** 實例而言，這個屬性是不正確。

<dl> <dt>

<span id="OK"></span><span id="ok"></span>**確定** (2) 
</dt> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (6) 
</dt> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (12) 
</dt> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (13) 
</dt> </dl>

</dd> <dt>

**HostComputerSystemName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

裝載此虛擬機器的電腦名稱稱。

> [!Note]  
> 已在 Windows 10 中新增。

 

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "CIM \_ ManagedElement. InstanceID" ) ， [**Key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

InstanceID 是選擇性屬性，可在具現化命名空間的範圍內，用來以不透明和唯一的方式識別此類別的實例。 此類別的各種子類別可覆寫這個屬性，使其成為必要或索引鍵。 這類子類別也可以修改慣用的演算法，以確保以下定義的唯一性。

為確保命名空間中的唯一性，InstanceID 的值應使用下列「慣用」演算法來建立：

&lt;OrgID &gt; ： &lt; LocalID&gt;

其中 &lt; OrgID &gt; 和 &lt; LocalID &gt; 是以冒號 (： ) ，而 &lt; OrgID &gt; 必須包含受著作權、商標或其他唯一名稱，而該實體是由建立或定義 InstanceID 的商務實體所擁有，或是由可辨識的全域授權單位指派給商務實體的註冊識別碼。  (這項需求與 <Schema Name> \_ <Class Name> 架構類別名稱的結構相似。 ) 此外，為了確保唯一性， &lt; OrgID &gt; 不能包含冒號 (： ) 。 使用此演算法時，InstanceID 中出現的第一個冒號必須出現在 &lt; OrgID &gt; 和 &lt; LocalID 之間 &gt; 。

&lt;LocalID &gt; 由商務實體選擇，不應重複使用，以找出不同的基礎 (真實世界) 元素。 如果不是 null，而且未使用上述的「慣用」演算法，則定義實體必須確保產生的 InstanceID 不會在這個實例的命名空間或其他提供者所產生的任何 InstanceIDs 上重複使用。

如果未針對 DMTF 定義的實例將設定為 null，就必須使用「慣用」演算法，並將 &lt; OrgID &gt; 設定為 CIM。

> [!Note]  
> 已在 Windows 10 中新增。

 

</dd> <dt>

**IntegrationServicesVersionState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出安裝在虛擬機器中的 integration services 是否為最新狀態。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="UpToDate"></span><span id="uptodate"></span><span id="UPTODATE"></span>

**UpToDate** (1) 


</dt> <dd></dd> <dt>

<span id="Mismatch"></span><span id="mismatch"></span><span id="MISMATCH"></span>

 (2) **不符**


</dt> <dd></dd> </dl>

</dd> <dt>

**MemoryAvailable**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬機器目前可用記憶體的百分比。 當虛擬機器啟用動態記憶體時，此屬性會代表虛擬機器的可用記憶體與指派給虛擬機器的實體記憶體總計的比率。 當虛擬機器沒有可用的記憶體時，這個屬性會是負數，而且會包含虛擬機器所需的記憶體與指派給虛擬機器的總實體記憶體的比率。

對於代表未啟用動態記憶體之虛擬機器的 **Msvm \_ SummaryInformation** 類別實例而言，這個屬性是不正確。

這個屬性對於代表虛擬機器快照集的 **Msvm \_ SummaryInformation** 類別的實例而言是不正確。

</dd> <dt>

**MemorySpansPhysicalNumaNodes**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出虛擬機器的一或多個虛擬非統一記憶體存取 (NUMA) 節點的記憶體是否跨越裝載電腦系統的多個實體 NUMA 節點。 如果記憶體跨越多個實體 NUMA 節點，則包含 **True** ，否則為 **False** 。

</dd> <dt>

**MemoryUsage**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬機器目前的記憶體使用量（以 mb 為單位）。 對於代表虛擬機器快照集的 **Msvm \_ SummaryInformation** 實例而言，這個屬性是不正確。

</dd> <dt>

名稱
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬機器或快照的唯一名稱。

</dd> <dt>

**注意事項**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

與虛擬機器或快照集相關的附注。

</dd> <dt>

**NumberOfProcessors**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

配置給虛擬機器或快照集的虛擬處理器總數。

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) 
</dt> </dl>

虛擬機器目前的操作狀態。 如需可能的值，請參閱 Msvm 非程式類型類別的 **OperationalStatus** 屬性。 [**\_**](msvm-computersystem.md)

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

字串，描述當 **EnabledState** 屬性設定為1時，元素的啟用或停用狀態。 當 **EnabledState** 是1以外的任何值時，這個屬性會設定為 **Null** 。

</dd> <dt>

**ProcessorLoad**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬機器目前的處理器使用量（以百分比為單位）。 對於代表虛擬機器快照集的 **Msvm \_ SummaryInformation** 實例而言，這個屬性是不正確。

</dd> <dt>

**ProcessorLoadHistory**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) 
</dt> </dl>

虛擬機器之處理器使用量的先前100範例陣列（以百分比表示）。 對於代表虛擬機器快照集的 **Msvm \_ SummaryInformation** 實例而言，這個屬性是不正確。

</dd> <dt>

**ReplicationHealth**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "**Msvm \_ SummaryInformation**.**ReplicationHealthEx**") 
</dt> </dl>

虛擬機器的複寫健全狀況。 如需可能的值，請參閱 [**Msvm \_**](msvm-computersystem.md)的 [ **ReplicationHealth** ] 屬性。

> [!Note]  
> 從 Windows 8.1 開始，這個屬性已被取代。相反地，請使用 **ReplicationHealthEx**。

 

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**不適用** (0) 


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

**確定** (1) 


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**警告** (2) 


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**重大** (3) 


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationHealthEx**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) 
</dt> </dl>

虛擬機器的各種複寫關聯性的複寫健全狀況值陣列。 如需可能的值，請參閱 [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md)類別的 **ReplicationHealth** 屬性。

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**不適用** (0) 


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

**確定** (1) 


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**警告** (2) 


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**重大** (3) 


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationMode**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬機器的複寫類型。 如需可能的值，請參閱 [**Msvm \_**](msvm-computersystem.md)的 [ **ReplicationMode** ] 屬性。

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**無** (0) 


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

**主要** (1) 


</dt> <dd></dd> <dt>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>

**複本** (2) 


</dt> <dd></dd> <dt>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>

**測試複本** (3) 


</dt> <dd></dd> <dt>

<span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>

**擴充複本** (4) 


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationProviderId**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) 
</dt> </dl>

針對主要或擴展複本虛擬機器，這是主要複寫提供者識別碼。 若為複本虛擬機器，而且如果已啟用延伸複寫，這就是延伸關聯性的提供者識別碼。

**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。

</dd> <dt>

**ReplicationState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "**Msvm \_ SummaryInformation**.**ReplicationStateEx**") 
</dt> </dl>

虛擬機器的複寫狀態。 如需可能的值，請參閱 [**Msvm \_**](msvm-computersystem.md)的 [ **ReplicationState** ] 屬性。

> [!Note]  
> 從 Windows 8.1 開始，這個屬性已被取代。相反地，請使用 **ReplicationStateEx**。

 

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**停用** (0) 


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

**準備好** 複寫 (1) 


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

**等候完成初始** 複寫 (2) 


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

複寫 **(3**) 


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

**同步複寫完成** (4) 


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

已 **復原** (5) 


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

**認可** (6) 


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

已 **暫** 止 (7) 


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**重大** (8) 


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

**等候啟動重新同步** (9) 


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

重新 **同步** 處理 (10) 


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

**重新同步** 處理已暫停 (11) 


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

**正在進行容錯移轉** (12) 


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationStateEx**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) 
</dt> </dl>

虛擬機器的各種複寫關聯性的複寫狀態值陣列。 如需可能的值，請參閱 [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md)類別的 **ReplicationState** 屬性。

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (0) 


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>**準備好** 複寫 (1) 


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**等候完成初始** 複寫 (2) 


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>複寫 **(3**) 


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**同步複寫完成** (4) 


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>已 **復原** (5) 


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>**認可** (6) 


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>已 **暫** 止 (7) 


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**重大** (8) 


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>**等候啟動重新同步** (9) 


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>重新 **同步** 處理 (10) 


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>**重新同步** 處理已暫停 (11) 


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>**正在進行容錯移轉** (12) 


</dt> <dd></dd> <dt>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>**正在進行容錯回復** (13) 


</dt> <dd></dd> <dt>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>容錯 **回復完成** (14) 


</dt> <dd></dd> <dt>

<span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>

<span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>**磁片更新進行中** (15) 


</dt> <dd>

> [!Note]  
> 在 Windows 10、1703版和 Windows Server 2016 中新增。

 

</dd> <dt>

<span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>

<span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>**磁片更新嚴重** (16) 


</dt> <dd>

> [!Note]  
> 在 Windows 10、1703版和 Windows Server 2016 中新增。

 

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (17) 


</dt> <dd>

> [!Note]  
> 在 Windows 10、1703版和 Windows Server 2016 中新增。

 

</dd> <dt>

<span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>

<span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>**進行複寫的** 重設用途 (18) 


</dt> <dd>

> [!Note]  
> 在 Windows 10、1703版和 Windows Server 2016 中新增。

 

</dd> <dt>

<span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>

<span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>已 **準備同步** 複寫 (19) 


</dt> <dd>

> [!Note]  
> 在 Windows 10、1703版和 Windows Server 2016 中新增。

 

</dd> <dt>

<span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>

<span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>**針對群組反向複寫做好準備** (20) 


</dt> <dd>

> [!Note]  
> 在 Windows 10、1703版和 Windows Server 2016 中新增。

 

</dd> <dt>

<span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>

<span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>**Firedrill 進行中** (21) 


</dt> <dd>

> [!Note]  
> 在 Windows 10、1703版和 Windows Server 2016 中新增。

 

</dd> </dl>

</dd> <dt>

**受防護**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否已為虛擬機器設定防護。

> [!Note]  
> 在 Windows 10、1703版和 Windows Server 2016 中新增。

 

</dd> <dt>

**快照集**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ VirtualSystemSettingData** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) 
</dt> </dl>

[**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)實例的陣列，代表虛擬機器的快照集。 對於代表虛擬機器快照集的 **Msvm \_ SummaryInformation** 實例而言，這個屬性是不正確。

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) 
</dt> </dl>

描述對應之 **OperationalStatus** 陣列值的字串。 這會對應到 [**Msvm \_**](msvm-computersystem.md)的 [ **StatusDescriptions** ] 屬性。

</dd> <dt>

**SwapFilesInUse**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出第二層分頁是否為使用中狀態。 如果第二層分頁為使用中，則包含 **True** ，否則為 **False** 。

</dd> <dt>

**TestReplicaSystem**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_** 未執行
</dt> <dt>

存取類型：唯讀
</dt> </dl>

參考代表虛擬機器之測試複本虛擬機器的 [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem) 實例實例。 對於代表虛擬機器快照集的 **Msvm \_ SummaryInformation** 實例而言，這個屬性是不正確。

</dd> <dt>

**ThumbnailImage**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **OctetString**、 [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) 、 [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**Msvm \_ SummaryInformation**。**ThumbnailImageWidth**"，"**Msvm \_ SummaryInformation**。**ThumbnailImageHeight**") 
</dt> </dl>

陣列，其中包含 RGB565 格式之虛擬機器或快照的小型、縮圖大小的影像。

</dd> <dt>

**ThumbnailImageHeight**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**Msvm \_ SummaryInformation**。**ThumbnailImage**") 
</dt> </dl>

ThumbnailImage 屬性中影像的高度（以圖元為單位）。

> [!Note]  
> 已在 Windows 10 中新增。

 

</dd> <dt>

**ThumbnailImageWidth**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**Msvm \_ SummaryInformation**。**ThumbnailImage**") 
</dt> </dl>

ThumbnailImage 屬性中影像的寬度（以圖元為單位）。

> [!Note]  
> 已在 Windows 10 中新增。

 

</dd> <dt>

**99.99**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬機器上次開機之後的時間量。 對於代表虛擬機器快照集的 **Msvm \_ SummaryInformation** 實例而言，這個屬性是不正確。

</dd> <dt>

**版本**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬系統的版本，格式為「主要. 次要」，例如 "2.0"。

> [!Note]  
> 已在 Windows 10 中新增。

 

</dd> <dt>

**VirtualSwitchNames**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) 
</dt> </dl>

字串，指定虛擬機器所連接之虛擬交換器的易記名稱。

**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。

</dd> <dt>

**VirtualSystemSubType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬系統的子類型。

**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

**Microsoft： hyper-v：子類型： 1** () 


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

**Microsoft： hyper-v：子類型： 2** () 


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>備註

存取 **Msvm \_ SummaryInformation** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

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

[**Msvm \_ SummaryInformationBase**](msvm-summaryinformationbase.md)
</dt> <dt>

[虛擬系統類別](virtual-system-classes.md)
</dt> </dl>

 


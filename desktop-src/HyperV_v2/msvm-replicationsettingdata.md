---
description: 代表虛擬機器的複寫特定設定。
ms.assetid: f6f6a413-a949-4aca-930b-37e39bdc1fdb
title: Msvm_ReplicationSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationSettingData
- Msvm_ReplicationSettingData.InstanceID
- Msvm_ReplicationSettingData.Caption
- Msvm_ReplicationSettingData.Description
- Msvm_ReplicationSettingData.ElementName
- Msvm_ReplicationSettingData.VirtualSystemIdentifier
- Msvm_ReplicationSettingData.VirtualSystemType
- Msvm_ReplicationSettingData.Notes
- Msvm_ReplicationSettingData.CreationTime
- Msvm_ReplicationSettingData.ConfigurationID
- Msvm_ReplicationSettingData.ConfigurationDataRoot
- Msvm_ReplicationSettingData.ConfigurationFile
- Msvm_ReplicationSettingData.SnapshotDataRoot
- Msvm_ReplicationSettingData.SuspendDataRoot
- Msvm_ReplicationSettingData.SwapFileDataRoot
- Msvm_ReplicationSettingData.LogDataRoot
- Msvm_ReplicationSettingData.AutomaticStartupAction
- Msvm_ReplicationSettingData.AutomaticStartupActionDelay
- Msvm_ReplicationSettingData.AutomaticStartupActionSequenceNumber
- Msvm_ReplicationSettingData.AutomaticShutdownAction
- Msvm_ReplicationSettingData.AutomaticRecoveryAction
- Msvm_ReplicationSettingData.RecoveryFile
- Msvm_ReplicationSettingData.AuthenticationType
- Msvm_ReplicationSettingData.CertificateThumbPrint
- Msvm_ReplicationSettingData.RootCertificateThumbPrint
- Msvm_ReplicationSettingData.CompressionEnabled
- Msvm_ReplicationSettingData.BypassProxyServer
- Msvm_ReplicationSettingData.RecoveryConnectionPoint
- Msvm_ReplicationSettingData.RecoveryHostSystem
- Msvm_ReplicationSettingData.PrimaryConnectionPoint
- Msvm_ReplicationSettingData.PrimaryHostSystem
- Msvm_ReplicationSettingData.RecoveryServerPortNumber
- Msvm_ReplicationSettingData.ReplicateHostKvpItems
- Msvm_ReplicationSettingData.ApplicationConsistentSnapshotInterval
- Msvm_ReplicationSettingData.RecoveryHistory
- Msvm_ReplicationSettingData.IncludedDisks
- Msvm_ReplicationSettingData.AutoResynchronizeEnabled
- Msvm_ReplicationSettingData.AutoResynchronizeIntervalStart
- Msvm_ReplicationSettingData.AutoResynchronizeIntervalEnd
- Msvm_ReplicationSettingData.EnableWriteOrderPreservationAcrossDisks
- Msvm_ReplicationSettingData.ReplicationProvider
- Msvm_ReplicationSettingData.AdditionalSettings
- Msvm_ReplicationSettingData.ReplicationInterval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 90e16e70f7b5bd0a075ffdef54cf0c591719d4993031f3abee19dd8186ec5996
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148251"
---
# <a name="msvm_replicationsettingdata-class"></a>Msvm \_ ReplicationSettingData 類別

代表虛擬機器的複寫特定設定。 用戶端會將這個類別的實例傳遞至 [**Msvm \_ ReplicationService >createreplicationrelationship**](createreplicationrelationship-msvm-replicationservice.md) ，以建立複寫關聯性。 用戶端無法直接變更這個類別之任何屬性的值;它必須呼叫 [**Msvm \_ ReplicationService. ModifyReplicationSettings**](modifyreplicationsettings-msvm-replicationservice.md) 方法來變更值。 每個複寫關聯性都有單一的設定實例。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationSettingData : CIM_VirtualSystemSettingData
{
  string   InstanceID = "Microsoft:Virtual Machine GUID\HVR";
  string   Caption = "Replication Settings";
  string   Description = "Virtual Machine Replication Settings Data";
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType = "Microsoft:Hyper-V:Replica";
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
  uint16   AuthenticationType;
  string   CertificateThumbPrint;
  string   RootCertificateThumbPrint;
  boolean  CompressionEnabled;
  boolean  BypassProxyServer;
  string   RecoveryConnectionPoint;
  string   RecoveryHostSystem;
  string   PrimaryConnectionPoint;
  string   PrimaryHostSystem;
  uint16   RecoveryServerPortNumber = 0;
  boolean  ReplicateHostKvpItems = True;
  uint16   ApplicationConsistentSnapshotInterval;
  uint16   RecoveryHistory = 0;
  string   IncludedDisks[];
  boolean  AutoResynchronizeEnabled = False;
  datetime AutoResynchronizeIntervalStart = 00000000183000.000000:000;
  datetime AutoResynchronizeIntervalEnd = 00000000060000.000000:000;
  boolean  EnableWriteOrderPreservationAcrossDisks;
  string   ReplicationProvider;
  string   AdditionalSettings;
  uint16   ReplicationInterval = 300;
};
```

## <a name="members"></a>成員

**Msvm \_ ReplicationSettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ ReplicationSettingData** 類別具有這些屬性。

<dl> <dt>

**AdditionalSettings**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

端點提供者可以使用的其他複寫設定。

**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。

</dd> <dt>

**ApplicationConsistentSnapshotInterval**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

應用程式一致快照集之間的時間間隔，以小時為單位指定。 有效的值為1小時到12小時。

</dd> <dt>

**AuthenticationType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

定義用來連接到復原伺服器的驗證模式。

<dt>

<span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>

<span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>**Kerberos 驗證** (1) 


</dt> <dd>

Kerberos 驗證。

</dd> <dt>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>以 **憑證為基礎的驗證** (2) 


</dt> <dd>

以憑證為基礎的驗證。

</dd> </dl>

</dd> <dt>

**AutomaticRecoveryAction**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

未使用。

這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。

</dd> <dt>

**AutomaticShutdownAction**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

未使用。

這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。

</dd> <dt>

**AutomaticStartupAction**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

未使用。

這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。

</dd> <dt>

**AutomaticStartupActionDelay**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬機器自動啟動之前的延遲時間。 這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，但不會使用它。

</dd> <dt>

**AutomaticStartupActionSequenceNumber**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

數位，指出主機系統啟動時的虛擬機器啟用的相對順序。 這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，但不會使用它。

</dd> <dt>

**AutoResynchronizeEnabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定是否在由於電源和硬體故障而發生複寫錯誤時，自動觸發重新同步作業。 只有在 **AutoResynchronizeIntervalStart** 和 **AutoResynchronizeIntervalEnd** 屬性所指定的時間之間發生失敗時，才會觸發重新同步作業。

預設值為 **[False]** 。

</dd> <dt>

**AutoResynchronizeIntervalEnd**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定要觸發自動重新同步處理作業的結束時間。 這個值是當地時間。 預設值為 06:00 (6:00 A.M. ) 。

只有在 **AutoResynchronizeIntervalStart** 和 **AutoResynchronizeIntervalEnd** 屬性所指定的時間之間發生失敗時，才會觸發重新同步作業。

重新同步處理作業也可以排程，以便在下一個間隔期間觸發。

</dd> <dt>

**AutoResynchronizeIntervalStart**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定要觸發自動重新同步處理作業的開始時間。 這個值是當地時間。 預設值為 18:30 (6:30 P.M. ) 。

只有在 **AutoResynchronizeIntervalStart** 和 **AutoResynchronizeIntervalEnd** 屬性所指定的時間之間發生失敗時，才會觸發重新同步作業。

重新同步處理作業也可以排程，以便在下一個間隔期間觸發。

</dd> <dt>

**BypassProxyServer**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定在連接到復原伺服器時是否應略過 proxy 伺服器。

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的簡短描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為 "Replication 設定"。

</dd> <dt>

**CertificateThumbPrint**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128) 
</dt> </dl>

**AuthenticationType** 屬性為以憑證為基礎的驗證時，所要使用的憑證指紋。

</dd> <dt>

**CompressionEnabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定將複寫資料傳送到復原伺服器時，是否要將它壓縮。

</dd> <dt>

**ConfigurationDataRoot**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

未使用。

這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。

</dd> <dt>

**ConfigurationFile**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

儲存虛擬機器設定相關資訊之檔案的相對路徑和檔案名。 此路徑相對於 **ConfigurationDataRoot** 屬性。 這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，但不會使用它。

</dd> <dt>

**ConfigurationID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬機器設定的唯一識別碼。 這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，但不會使用它。

</dd> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

建立虛擬機器設定的日期和時間。 如果此物件代表目前的虛擬機器設定，則此值會是系統建立的時間。 如果此物件代表虛擬機器的快照集設定，則此值會是拍攝快照集的時間。 這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。

這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifySystemSettings**](modifysystemsettings-msvm-virtualsystemmanagementservice.md)方法來變更。

這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對物件的描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「虛擬機器複寫設定資料」。

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的顯示名稱。 這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，它會設定為虛擬機器的顯示名稱。

</dd> <dt>

**EnableWriteOrderPreservationAcrossDisks**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( 「沒有值」 ) 
</dt> </dl>

指定是否將虛擬機器的所有複寫虛擬硬碟複寫到相同的時間點。 這可確保複寫在虛擬機器中接受應用程式的寫入順序。

**Windows 8.1：** 從 Windows 8.1 和 Windows Server 2012 R2 開始，這個屬性已被取代，而且一律設定為 **TRUE**。

</dd> <dt>

**IncludedDisks**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **HyperVEmbeddedInstance** ( "CIM \_ StorageAllocationSettingData" ) ， [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) 
</dt> </dl>

虛擬硬碟 (Vhd 的清單) 附加至複寫引擎將複寫的系統。 這是字串的陣列，每個字串都包含代表 VHD 之 [**Msvm \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md)的 **InstanceID** 。

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

唯一識別此類別的實例。 這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。 針對 Windows 8，它一律會設定為 "Microsoft：*Virtual MACHINE GUID* \\ HVR"。 針對 Windows 8.1，它會設定為 "Microsoft：*Virtual Machine GUID* \\ HVR \\<0/1>"。 在 Windows 8.1 值中，0表示 primary，1表示擴充複寫。 如需擴充複寫的詳細資訊，請參閱 [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md)。

</dd> <dt>

**LogDataRoot**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

儲存虛擬機器記錄資訊之目錄的路徑。 這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，但不會使用它。

</dd> <dt>

**注意事項**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

未使用且無法設定。

這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。

</dd> <dt>

**PrimaryConnectionPoint**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

主要連接點的名稱。 在主要叢集的案例中，這是 broker CAP 名稱。 在獨立主伺服器的情況下，這是主機系統名稱。

</dd> <dt>

**PrimaryHostSystem**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

裝載虛擬機器之主要主機系統的完整功能變數名稱。

</dd> <dt>

**RecoveryConnectionPoint**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

復原連接點的名稱。 在復原叢集的情況下，這是 broker CAP 名稱。 在獨立復原伺服器的情況下，這是主機系統名稱。

</dd> <dt>

**RecoveryFile**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

儲存虛擬機器修復相關資訊之檔案的完整路徑。 這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，但不會使用它。

</dd> <dt>

**RecoveryHistory**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

復原伺服器上將儲存的復原快照集數目上限。 有效的值是從0到24。

</dd> <dt>

**RecoveryHostSystem**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

裝載虛擬機器之復原主機系統的完整功能變數名稱。

</dd> <dt>

**RecoveryServerPortNumber**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

建立安全連線以進行複寫時要使用的復原伺服器埠號碼。

</dd> <dt>

**ReplicateHostKvpItems**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定是否應該將主機專用的 [**Msvm \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md)從主要虛擬機器複寫到復原虛擬機器。

</dd> <dt>

**ReplicationInterval**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

複寫關聯性的複寫間隔（以秒為單位）。 有效值為：

30

300

900

預設值為300秒。

**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。

</dd> <dt>

**ReplicationProvider**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

識別複寫提供者端點之 [**Msvm \_ ReplicationProvider**](msvm-replicationprovider.md) 類別實例的路徑。

**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。

</dd> <dt>

**RootCertificateThumbPrint**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128) 
</dt> </dl>

當 **AuthenticationType** 為 2 (以憑證為基礎的授權) 時，所使用之憑證的根憑證指紋。

</dd> <dt>

**SnapshotDataRoot**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

儲存虛擬機器快照集相關資訊之目錄的路徑。 這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，但不會使用它。

</dd> <dt>

**SuspendDataRoot**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

儲存虛擬機器暫停相關資訊之相關資訊的目錄路徑。 這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，但不會使用它。

</dd> <dt>

**SwapFileDataRoot**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

儲存虛擬機器之交換檔的目錄路徑。 這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，但不會使用它。

</dd> <dt>

**VirtualSystemIdentifier**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這項設定資料所屬之 CIM 非程式物件的名稱。 [**\_**](/windows/desktop/CIMWin32Prov/cim-computersystem) 這個屬性是 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))的覆寫。

</dd> <dt>

**VirtualSystemType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定設定資料所代表的虛擬機器類型。 這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，且一律設定為 "Microsoft： hyper-v： Replica"。

</dd> </dl>

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

[**ModifyReplicationSettings**](modifyreplicationsettings-msvm-replicationservice.md)
</dt> </dl>

 


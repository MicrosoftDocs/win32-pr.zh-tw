---
description: 代表靜態或動態切換埠的配置要求，或代表目前配置之靜態或動態切換埠的使用中設定。
ms.assetid: ef70b72f-75a0-448e-a648-6a28c12f0da1
title: Msvm_EthernetPortAllocationSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortAllocationSettingData
- Msvm_EthernetPortAllocationSettingData.InstanceID
- Msvm_EthernetPortAllocationSettingData.Caption
- Msvm_EthernetPortAllocationSettingData.Description
- Msvm_EthernetPortAllocationSettingData.ElementName
- Msvm_EthernetPortAllocationSettingData.ResourceType
- Msvm_EthernetPortAllocationSettingData.OtherResourceType
- Msvm_EthernetPortAllocationSettingData.ResourceSubType
- Msvm_EthernetPortAllocationSettingData.PoolID
- Msvm_EthernetPortAllocationSettingData.ConsumerVisibility
- Msvm_EthernetPortAllocationSettingData.HostResource
- Msvm_EthernetPortAllocationSettingData.AllocationUnits
- Msvm_EthernetPortAllocationSettingData.VirtualQuantity
- Msvm_EthernetPortAllocationSettingData.Reservation
- Msvm_EthernetPortAllocationSettingData.Limit
- Msvm_EthernetPortAllocationSettingData.Weight
- Msvm_EthernetPortAllocationSettingData.AutomaticAllocation
- Msvm_EthernetPortAllocationSettingData.AutomaticDeallocation
- Msvm_EthernetPortAllocationSettingData.Parent
- Msvm_EthernetPortAllocationSettingData.Connection
- Msvm_EthernetPortAllocationSettingData.Address
- Msvm_EthernetPortAllocationSettingData.MappingBehavior
- Msvm_EthernetPortAllocationSettingData.AddressOnParent
- Msvm_EthernetPortAllocationSettingData.VirtualQuantityUnits
- Msvm_EthernetPortAllocationSettingData.DesiredVLANEndpointMode
- Msvm_EthernetPortAllocationSettingData.OtherEndpointMode
- Msvm_EthernetPortAllocationSettingData.EnabledState
- Msvm_EthernetPortAllocationSettingData.LastKnownSwitchName
- Msvm_EthernetPortAllocationSettingData.RequiredFeatures
- Msvm_EthernetPortAllocationSettingData.RequiredFeatureHints
- Msvm_EthernetPortAllocationSettingData.TestReplicaPoolID
- Msvm_EthernetPortAllocationSettingData.TestReplicaSwitchName
- Msvm_EthernetPortAllocationSettingData.CompartmentGuid
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: be3968f52065259cb69ad35721dffd3ac606da98e4189edaad1b762120f5a008
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681578"
---
# <a name="msvm_ethernetportallocationsettingdata-class"></a>Msvm \_ EthernetPortAllocationSettingData 類別

代表靜態或動態切換埠的配置要求，或代表目前配置之靜態或動態切換埠的使用中設定。 動態交換器埠的配置要求也稱為連接要求。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortAllocationSettingData : CIM_EthernetPortAllocationSettingData
{
  string  InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string  Caption = "Ethernet Switch Port Settings";
  string  Description = "Ethernet Switch Port Settings";
  string  ElementName;
  uint16  ResourceType = 33;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
  string  AllocationUnits;
  uint64  VirtualQuantity;
  uint64  Reservation;
  uint64  Limit;
  uint32  Weight = 0;
  boolean AutomaticAllocation;
  boolean AutomaticDeallocation;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
  uint16  DesiredVLANEndpointMode;
  string  OtherEndpointMode;
  uint16  EnabledState;
  string  LastKnownSwitchName;
  string  RequiredFeatures[];
  string  RequiredFeatureHints[];
  string  TestReplicaPoolID;
  string  TestReplicaSwitchName;
  string  CompartmentGuid;
};
```

## <a name="members"></a>成員

**Msvm \_ EthernetPortAllocationSettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ EthernetPortAllocationSettingData** 類別具有這些屬性。

<dl> <dt>

**位址**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

資源的位址。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。

</dd> <dt>

**AddressOnParent**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述此資源在父系內容中的位址。 **Parent** 和 **AddressOnParent** 屬性是用來描述控制器的關聯性，以及控制器上的裝置順序。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。

</dd> <dt>

**AllocationUnits**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

**保留** 和 **限制** 屬性所使用的配置單位。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。

</dd> <dt>

**AutomaticAllocation**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否會自動設定資源。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。

</dd> <dt>

**AutomaticDeallocation**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否將自動解除配置資源。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **MaxLen** (64) 
</dt> </dl>

物件的簡短描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「Ethernet 交換器埠設定」。

</dd> <dt>

**CompartmentGuid**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

這個屬性會指定埠的目標網路區間。 只有內部介面卡支援此功能。

> [!Note]  
> 在 Windows 10 中新增的屬性。

 

</dd> <dt>

**[連接]**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此資源所連接的裝置。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。

</dd> <dt>

**ConsumerVisibility**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取用者對已配置資源的可見度。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)，且一律設定為 3 (虛擬) 。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對物件的描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「Ethernet 交換器埠設定」。

</dd> <dt>

**DesiredVLANEndpointMode**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

VLAN 端點所需的設定模式。 這個屬性是用來設定與目標 Ethernet 埠相關聯之 [**Msvm \_ VLANEndpoint**](msvm-vlanendpoint.md)類別的實例中的初始 **OperationalEndpointMode** 屬性值。 如需可能的值，請參閱 **Msvm \_ VLANEndpoint** 類別的 **OperationalEndpointMode** 屬性。 這個屬性繼承自 **CIM \_ EthernetPortAllocationSettingData**。

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的顯示名稱。 這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。 變更此屬性將會變更相關聯之邏輯裝置衍生的元素名稱。

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出配置要求是否已啟用或停用。 當配置要求標記為停用時 (3) ，則不會處理配置。 作用中設定的 **EnabledState** 一律會標示為已啟用 (2) 。

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**已啟用** (2) 


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**停用** (3) 


</dt> <dd></dd> </dl>

</dd> <dt>

**HostResource**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

只有一個主機資源可以指派給虛擬交換器中的每個裝置，因此只能設定此陣列的第一個元素。 針對支援此功能的裝置，請將 **HostResource** 陣列的第一個元素設定為包含要指派之基礎主機資源的參考。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

唯一識別此類別的實例。 這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))，一律設定為 "Microsoft：*GUID* \\ *DeviceSpecificData*"。

</dd> <dt>

**LastKnownSwitchName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

交換器的最後已知易記名稱（如果有的話）。

> [!Note]  
> 在 Windows 10 中新增的屬性。

 

</dd> <dt>

**限制**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬交換器可以取用的相對應主機資源數量上限。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。

</dd> <dt>

**MappingBehavior**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定此資源對應至基礎資源的方式。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。

</dd> <dt>

**OtherEndpointMode**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

字串，描述此 VLAN 端點所支援的 VLAN 端點模型類型。 只有當 **DesiredVLANEndpointMode** 屬性設定為 1 (其他) 時，才會使用這個屬性。 當 **DesiredVLANEndpointMode** 屬性是1以外的任何值時，這個屬性應該設為 **Null** 。 這個屬性繼承自 **CIM \_ EthernetPortAllocationSettingData**。

</dd> <dt>

**OtherResourceType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述資源類型的字串，當定義完善的值無法使用且 [**ResourceType**](msvm-processorsettingdata.md) 的值為1時 (其他) 。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)，而且不會使用它。

</dd> <dt>

**父系**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

資源的父系。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。

</dd> <dt>

**PoolID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

配置此資源的來源資源集區識別碼。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。

</dd> <dt>

**RequiredFeatureHints**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對應至 **RequiredFeatures** 陣列中每個專案的顯示名稱清單。

</dd> <dt>

**RequiredFeatures**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

功能識別碼的清單，代表埠所需的所有功能。

</dd> <dt>

**保留容量**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

保留供虛擬交換器使用的資源數量。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。

</dd> <dt>

**ResourceSubType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

字串，描述此資源的執行特定子類型。 例如，這可用來區分相同資源類型的不同模型。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此配置設定所代表的資源類型。 這個屬性會繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)，而且一律會設定為 33 (Ethernet 連接) 。

</dd> <dt>

**TestReplicaPoolID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指定當建立連接時，會將連接配置給測試複本系統的網路資源集區。

</dd> <dt>

**TestReplicaSwitchName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指定虛擬網路交換器的顯示名稱，該名稱會在建立時為測試複本系統組態連接。

</dd> <dt>

**VirtualQuantity**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬交換器中的埠總數。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。

</dd> <dt>

**VirtualQuantityUnits**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定 **VirtualQuantity** 屬性的度量單位。 這個屬性的值必須是程式設計單位辨識符號的合法值，如 DSP0004 2.5 或更新版本的附錄 C. 1 中所定義。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。

</dd> <dt>

**Weight**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

定義每個虛擬交換器之權數的整數。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。

範圍： 0 1000

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 


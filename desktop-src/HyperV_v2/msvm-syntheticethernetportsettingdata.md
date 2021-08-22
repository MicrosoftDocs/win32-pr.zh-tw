---
description: 代表綜合乙太網路介面卡已設定的狀態。
ms.assetid: BE895BAF-7766-43A2-9659-3ABA97A16134
title: Msvm_SyntheticEthernetPortSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticEthernetPortSettingData
- Msvm_SyntheticEthernetPortSettingData.InstanceID
- Msvm_SyntheticEthernetPortSettingData.Caption
- Msvm_SyntheticEthernetPortSettingData.Description
- Msvm_SyntheticEthernetPortSettingData.ElementName
- Msvm_SyntheticEthernetPortSettingData.ResourceType
- Msvm_SyntheticEthernetPortSettingData.OtherResourceType
- Msvm_SyntheticEthernetPortSettingData.ResourceSubType
- Msvm_SyntheticEthernetPortSettingData.PoolID
- Msvm_SyntheticEthernetPortSettingData.ConsumerVisibility
- Msvm_SyntheticEthernetPortSettingData.HostResource
- Msvm_SyntheticEthernetPortSettingData.AllocationUnits
- Msvm_SyntheticEthernetPortSettingData.VirtualQuantity
- Msvm_SyntheticEthernetPortSettingData.Reservation
- Msvm_SyntheticEthernetPortSettingData.Limit
- Msvm_SyntheticEthernetPortSettingData.Weight
- Msvm_SyntheticEthernetPortSettingData.AutomaticAllocation
- Msvm_SyntheticEthernetPortSettingData.AutomaticDeallocation
- Msvm_SyntheticEthernetPortSettingData.Parent
- Msvm_SyntheticEthernetPortSettingData.Connection
- Msvm_SyntheticEthernetPortSettingData.Address
- Msvm_SyntheticEthernetPortSettingData.MappingBehavior
- Msvm_SyntheticEthernetPortSettingData.AddressOnParent
- Msvm_SyntheticEthernetPortSettingData.VirtualQuantityUnits
- Msvm_SyntheticEthernetPortSettingData.DesiredVLANEndpointMode
- Msvm_SyntheticEthernetPortSettingData.OtherEndpointMode
- Msvm_SyntheticEthernetPortSettingData.VirtualSystemIdentifiers
- Msvm_SyntheticEthernetPortSettingData.DeviceNamingEnabled
- Msvm_SyntheticEthernetPortSettingData.AllowPacketDirect
- Msvm_SyntheticEthernetPortSettingData.StaticMacAddress
- Msvm_SyntheticEthernetPortSettingData.ClusterMonitored
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d82c1826b865d94ae0a9a9d5a63fb535ad804ad5e874dec9563c5b5e74bd67f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949787"
---
# <a name="msvm_syntheticethernetportsettingdata-class"></a>Msvm \_ SyntheticEthernetPortSettingData 類別

代表綜合乙太網路介面卡已設定的狀態。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticEthernetPortSettingData : CIM_EthernetPortAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Virtual Ethernet Port Default Settings";
  string  Description = "Describes the default settings for the virtual Ethernet port resources.";
  string  ElementName;
  uint16  ResourceType = 10;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft:Hyper-V:Synthetic Ethernet Port";
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
  string  AllocationUnits = "count";
  uint64  VirtualQuantity = 1;
  uint64  Reservation = 1;
  uint64  Limit = 1;
  uint32  Weight = 0;
  boolean AutomaticAllocation = True;
  boolean AutomaticDeallocation = True;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
  uint16  DesiredVLANEndpointMode;
  string  OtherEndpointMode;
  string  VirtualSystemIdentifiers[];
  boolean DeviceNamingEnabled = FALSE;
  boolean AllowPacketDirect = FALSE;
  boolean StaticMacAddress = False;
  boolean ClusterMonitored = TRUE;
};
```

## <a name="members"></a>成員

**Msvm \_ SyntheticEthernetPortSettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ SyntheticEthernetPortSettingData** 類別具有這些屬性。

<dl> <dt>

**位址**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

資源的位址。 例如，乙太網路埠的 MAC 位址。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。

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

**AllowPacketDirect**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出是否已啟用 VM 的 PacketDirect 投影。

> [!Note]  
> 在 Windows 10、1703版和 Windows Server 2016 中新增。

 

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
</dt> </dl>

物件的簡短描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**ClusterMonitored**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出此乙太網路介面卡是否由叢集監視。 如果未設定，此屬性會預設為 true。

這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)方法來變更。

**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。

</dd> <dt>

**[連接]**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此資源所連接的目標。 例如，名為網路或交換器埠。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。

</dd> <dt>

**ConsumerVisibility**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取用者會看到已配置的資源。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)，且一律設定為 3 (虛擬) 。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對物件的描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**DesiredVLANEndpointMode**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

VLAN 端點所需的設定模式。 這個屬性是用來設定與目標 Ethernet 埠相關聯之 [**Msvm \_ VLANEndpoint**](msvm-vlanendpoint.md)類別的實例中的初始 **OperationalEndpointMode** 屬性值。 如需可能的值，請參閱 **Msvm \_ VLANEndpoint** 類別的 **OperationalEndpointMode** 屬性。 這個屬性繼承自 **CIM \_ EthernetPortAllocationSettingData**。

</dd> <dt>

**DeviceNamingEnabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出此乙太網路介面卡是否支援裝置命名。

這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyVirtualSystemResources**](https://www.bing.com/search?q=**ModifyVirtualSystemResources**)方法來變更。

> [!Note]  
> 加入 Windows 10 和 Windows Server 2016。

 

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的簡短描述。 這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。

</dd> <dt>

**HostResource**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)，而且一律設定為 **Null**。

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

**限制**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此配置將授與的上限或最大資源量。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。

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

當定義完善的值無法使用且 **ResourceType** 設定為 "Other" (0) 時，描述資源類型的字串。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)，而且不會使用它。

</dd> <dt>

**父系**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

資源的父系。 例如，目前配置的控制器。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。

</dd> <dt>

**PoolID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

資源目前配置來源的集區，或當配置發生時，將配置資源的集區。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。

</dd> <dt>

**保留容量**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

保證可用於此配置的資源數量。 在支援過度使用資源的系統上，此值通常用於許可控制，以防止配置被接受。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。

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

套用此設定的資源類型。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)，且一律設定為 10 (乙太網路介面卡) 。

</dd> <dt>

**StaticMacAddress**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定 MAC 位址是否為靜態。

</dd> <dt>

**VirtualQuantity**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

向取用者呈現的資源數量。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。

</dd> <dt>

**VirtualQuantityUnits**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定 **VirtualQuantity** 屬性的度量單位。 這個屬性的值必須是程式設計單位辨識符號的合法值，如 DSP0004 2.5 或更新版本的附錄 C. 1 中所定義。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。

</dd> <dt>

**VirtualSystemIdentifiers**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) 
</dt> </dl>

此資源的識別碼字串陣列，會呈現給虛擬機器的作業系統。 每個索引的索引和值都是以每個資源為基礎來定義 (也就是每個列舉 **ResourceType** 屬性值) 。

</dd> <dt>

**Weight**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

相對於相同資源集區中的其他配置，此配置的相對優先權。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。

</dd> </dl>

## <a name="remarks"></a>備註

存取 **Msvm \_ SyntheticEthernetPortSettingData** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

## <a name="examples"></a>範例

請參閱 [查詢網路物件](querying-networking-objects.md)。

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

[**CIM \_ EthernetPortAllocationSettingData**](cim-ethernetportallocationsettingdata.md)
</dt> <dt>

[**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 


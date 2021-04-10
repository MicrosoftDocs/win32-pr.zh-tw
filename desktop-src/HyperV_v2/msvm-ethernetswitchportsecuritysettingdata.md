---
description: 表示設定資料的安全性功能。
ms.assetid: 98e0de24-ccdc-4fc7-86a5-b68d454fde9d
title: Msvm_EthernetSwitchPortSecuritySettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortSecuritySettingData
- Msvm_EthernetSwitchPortSecuritySettingData.InstanceID
- Msvm_EthernetSwitchPortSecuritySettingData.Caption
- Msvm_EthernetSwitchPortSecuritySettingData.Description
- Msvm_EthernetSwitchPortSecuritySettingData.ElementName
- Msvm_EthernetSwitchPortSecuritySettingData.AllowMacSpoofing
- Msvm_EthernetSwitchPortSecuritySettingData.EnableDhcpGuard
- Msvm_EthernetSwitchPortSecuritySettingData.EnableRouterGuard
- Msvm_EthernetSwitchPortSecuritySettingData.MonitorMode
- Msvm_EthernetSwitchPortSecuritySettingData.MonitorSession
- Msvm_EthernetSwitchPortSecuritySettingData.AllowIeeePriorityTag
- Msvm_EthernetSwitchPortSecuritySettingData.VirtualSubnetId
- Msvm_EthernetSwitchPortSecuritySettingData.AllowTeaming
- Msvm_EthernetSwitchPortSecuritySettingData.TeamName
- Msvm_EthernetSwitchPortSecuritySettingData.TeamNumber
- Msvm_EthernetSwitchPortSecuritySettingData.EnableFixSpeed10G
- Msvm_EthernetSwitchPortSecuritySettingData.Reserved
- Msvm_EthernetSwitchPortSecuritySettingData.DynamicIPAddressLimit
- Msvm_EthernetSwitchPortSecuritySettingData.StormLimit
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8d37913f015a3ffbfaa751a7bbb10f79cea2fb39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103853152"
---
# <a name="msvm_ethernetswitchportsecuritysettingdata-class"></a>Msvm \_ EthernetSwitchPortSecuritySettingData 類別

表示設定資料的安全性功能。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("776E0BA7-94A1-41C8-8F28-951F524251B5"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("3"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Security Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortSecuritySettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  InstanceID;
  string  Caption = "Ethernet Switch Port Security Settings";
  string  Description = "Represents the security feature setting data.";
  string  ElementName = "Ethernet Switch Port Security Settings";
  boolean AllowMacSpoofing = FALSE;
  boolean EnableDhcpGuard = FALSE;
  boolean EnableRouterGuard = FALSE;
  uint8   MonitorMode = 0;
  uint8   MonitorSession = 0;
  boolean AllowIeeePriorityTag = FALSE;
  uint32  VirtualSubnetId = 0;
  boolean AllowTeaming = FALSE;
  string  TeamName = ;
  uint32  TeamNumber = 0;
  boolean EnableFixSpeed10G = FALSE;
  boolean Reserved = FALSE;
  uint32  DynamicIPAddressLimit = 0;
  uint32  StormLimit = 0;
};
```

## <a name="members"></a>成員

**Msvm \_ EthernetSwitchPortSecuritySettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ EthernetSwitchPortSecuritySettingData** 類別具有這些屬性。

<dl> <dt>

**AllowIeeePriorityTag**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (6) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

指定進出埠的流量是否保留 802.1 P 資訊。 如果埠的流量保留 802.1 P 資訊，則包含 **True** ，否則為 **False** 。 預設值為 **[False]** 。

</dd> <dt>

**AllowMacSpoofing**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (1) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

指出埠是否會允許 MAC 詐騙。 如果這個屬性為 **True**，埠將允許 MAC 位址成為詐騙。 允許所有有效的單播 MAC 位址值。 如果此屬性為 **False**，埠將只允許使用在 hyper-v 管理內設定的 MAC 位址。 預設值為 **[False]** 。

</dd> <dt>

**AllowTeaming**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (8) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

指出連線到埠的 Nic 是否可以是小組的一部分。 這僅適用于連線至虛擬機器的 Nic。 如果允許 NIC 小組，則包含 **True** ，否則為 **False** 。 預設值為 **[False]** 。

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的簡短描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「乙太網路交換器通訊埠安全性設定」。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對物件的描述。 這個屬性是從 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)繼承而來，而且一律設定為「代表安全性功能設定資料」。

</dd> <dt>

**DynamicIPAddressLimit**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (12) 、 **InterfaceVersion** (2) 、 **InterfaceRevision** (0) 
</dt> </dl>

定義所學到的動態 IP 位址數目限制。 預設值為 none。

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的顯示名稱。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「乙太網路交換器通訊埠安全性設定」。

</dd> <dt>

**EnableDhcpGuard**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (2) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

指定是否封鎖來自埠的 DHCP 供應專案。 如果從埠封鎖 DHCP 供應專案，則包含 **True** ，否則為 **False** 。 預設值為 **[False]** 。

</dd> <dt>

**EnableFixSpeed10G**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (14) 、 **InterfaceVersion** (3) 、 **InterfaceRevision** (0) 
</dt> </dl>

如果已啟用固定速度10G，則設定為 TRUE，否則為 FALSE。 預設值為 FALSE。

> [!Note]  
> 在 Windows 10 中新增的屬性。

 

</dd> <dt>

**EnableRouterGuard**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (3) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

指定是否封鎖來自埠的路由器通告和路由器重新導向。 如果從埠封鎖路由器通告和路由器重新導向，則包含 **True** ，否則為 **False** 。 預設值為 **[False]** 。

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

**MonitorMode**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (4) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

這表示埠的監視器模式。

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**無** (0) 


</dt> <dd></dd> <dt>

<span id="Destination"></span><span id="destination"></span><span id="DESTINATION"></span>

**目的地** (1) 


</dt> <dd></dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>

**來源** (2) 


</dt> <dd></dd> </dl>

</dd> <dt>

**MonitorSession**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (5) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

指定此埠所屬監視會話的識別碼。

</dd> <dt>

**已保留**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( 「沒有值」 ) 、 **WmiDataId** (13) 、 **InterfaceVersion** (3) 、 **InterfaceRevision** (0) 
</dt> </dl>

保留

> [!Note]  
> 在 Windows 10 中新增的屬性。

 

</dd> <dt>

**StormLimit**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (11) 、 **InterfaceVersion** (2) 、 **InterfaceRevision** (0) 
</dt> </dl>

定義廣播和多播流量的每秒封包限制。 預設值為 none。

</dd> <dt>

**TeamName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127) 、 **WmiDataId** (9) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

保留供未來使用。

</dd> <dt>

**TeamNumber**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (10) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

保留供未來使用。

</dd> <dt>

**VirtualSubnetId**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (7) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 、 [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0 [**) 、int32.maxvalue (16777215)**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

指定埠為其成員之虛擬子網的識別碼。 預設值是 [none]。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 


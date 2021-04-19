---
description: 代表切換埠設定 (ACL) 的存取控制清單。
ms.assetid: c0d6dfa1-017c-4e66-9ee3-425182d84231
title: Msvm_EthernetSwitchPortAclSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortAclSettingData
- Msvm_EthernetSwitchPortAclSettingData.InstanceID
- Msvm_EthernetSwitchPortAclSettingData.Caption
- Msvm_EthernetSwitchPortAclSettingData.Description
- Msvm_EthernetSwitchPortAclSettingData.ElementName
- Msvm_EthernetSwitchPortAclSettingData.Name
- Msvm_EthernetSwitchPortAclSettingData.Direction
- Msvm_EthernetSwitchPortAclSettingData.Applicability
- Msvm_EthernetSwitchPortAclSettingData.AclType
- Msvm_EthernetSwitchPortAclSettingData.Action
- Msvm_EthernetSwitchPortAclSettingData.LocalAddress
- Msvm_EthernetSwitchPortAclSettingData.LocalAddressPrefixLength
- Msvm_EthernetSwitchPortAclSettingData.RemoteAddress
- Msvm_EthernetSwitchPortAclSettingData.RemoteAddressPrefixLength
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 92735718e339a0caf33910dec703276aea946a67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985509"
---
# <a name="msvm_ethernetswitchportaclsettingdata-class"></a>Msvm \_ EthernetSwitchPortAclSettingData 類別

代表切換埠設定 (ACL) 的存取控制清單。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, UUID("998BEF4A-5D55-492A-9C43-8B2F5EAE9F2B"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), Provider("VmmsWmiInstanceAndMethodProvider"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port ACL Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortAclSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port ACL Settings";
  string Description = "Represents the base class for switch port settings.";
  string ElementName = "Ethernet Switch Port ACL Settings";
  string Name = "";
  uint8  Direction = 0;
  uint8  Applicability = 0;
  uint8  AclType = 0;
  uint8  Action = 0;
  string LocalAddress = "";
  uint8  LocalAddressPrefixLength = 0;
  string RemoteAddress = length = 0;
  uint8  RemoteAddressPrefixLength = 0;
};
```

## <a name="members"></a>成員

**Msvm \_ EthernetSwitchPortAclSettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ EthernetSwitchPortAclSettingData** 類別具有這些屬性。

<dl> <dt>

**AclType**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (4) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

這表示 ACL 端點的類型。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="MAC_Acl"></span><span id="mac_acl"></span><span id="MAC_ACL"></span>

**MAC Acl** (1) 


</dt> <dd></dd> <dt>

<span id="IPv4_Acl"></span><span id="ipv4_acl"></span><span id="IPV4_ACL"></span>

**IPv4 Acl** (2) 


</dt> <dd></dd> <dt>

<span id="IPv6_Acl"></span><span id="ipv6_acl"></span><span id="IPV6_ACL"></span>

**IPv6 Acl** (3) 


</dt> <dd></dd> </dl>

</dd> <dt>

**動作**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (5) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

這表示 ACL 的動作。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>

**允許** (1) 


</dt> <dd></dd> <dt>

<span id="Deny"></span><span id="deny"></span><span id="DENY"></span>

**拒絕** (2) 


</dt> <dd></dd> <dt>

<span id="Meter"></span><span id="meter"></span><span id="METER"></span>

**計量** (3) 


</dt> <dd></dd> </dl>

</dd> <dt>

**適用性**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (3) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

這表示 ACL 是否適用于本機或遠端端點。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Local"></span><span id="local"></span><span id="LOCAL"></span>

**本機** (1) 


</dt> <dd></dd> <dt>

<span id="Remote"></span><span id="remote"></span><span id="REMOTE"></span>

**遠端** (2) 


</dt> <dd></dd> </dl>

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的簡短描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「乙太網路交換器通訊埠 ACL 設定」。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對物件的描述。 這個屬性是從 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)繼承而來，而且一律設定為「代表交換器埠設定的基類」。

</dd> <dt>

[方向]
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (2) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

這表示 ACL 是否適用于輸入或輸出方向。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Incoming"></span><span id="incoming"></span><span id="INCOMING"></span>

**傳入** 的 (1) 


</dt> <dd></dd> <dt>

<span id="Outgoing"></span><span id="outgoing"></span><span id="OUTGOING"></span>

連 **出** (2) 


</dt> <dd></dd> </dl>

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的顯示名稱。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「乙太網路交換器通訊埠 ACL 設定」。

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

**LocalAddress**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40) 、 **WmiDataId** (6) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

虛擬機器的本機位址。 這可以是 IPv4、IPv6 或 MAC 位址。

</dd> <dt>

**LocalAddressPrefixLength**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (7) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

本機位址前置長度。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 、 **WmiDataId** (1) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

ACL 的顯示名稱。

</dd> <dt>

**RemoteAddress**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40) 、 **WmiDataId** (8) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

虛擬機器的遠端位址。 這可以是 IPv4、IPv6 或 MAC 位址。

</dd> <dt>

**RemoteAddressPrefixLength**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (9) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

遠端位址前置長度。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 


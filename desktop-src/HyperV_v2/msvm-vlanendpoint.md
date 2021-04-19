---
description: 代表交換器埠的 VLAN 端點。
ms.assetid: 82F2EC39-0C9C-4A9D-A6C4-1543A62A341D
title: Msvm_VLANEndpoint 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VLANEndpoint
- Msvm_VLANEndpoint.InstanceID
- Msvm_VLANEndpoint.Caption
- Msvm_VLANEndpoint.Description
- Msvm_VLANEndpoint.ElementName
- Msvm_VLANEndpoint.InstallDate
- Msvm_VLANEndpoint.Name
- Msvm_VLANEndpoint.OperationalStatus
- Msvm_VLANEndpoint.StatusDescriptions
- Msvm_VLANEndpoint.Status
- Msvm_VLANEndpoint.HealthState
- Msvm_VLANEndpoint.CommunicationStatus
- Msvm_VLANEndpoint.DetailedStatus
- Msvm_VLANEndpoint.OperatingStatus
- Msvm_VLANEndpoint.PrimaryStatus
- Msvm_VLANEndpoint.EnabledState
- Msvm_VLANEndpoint.OtherEnabledState
- Msvm_VLANEndpoint.RequestedState
- Msvm_VLANEndpoint.EnabledDefault
- Msvm_VLANEndpoint.TimeOfLastStateChange
- Msvm_VLANEndpoint.AvailableRequestedStates
- Msvm_VLANEndpoint.TransitioningToState
- Msvm_VLANEndpoint.SystemCreationClassName
- Msvm_VLANEndpoint.SystemName
- Msvm_VLANEndpoint.CreationClassName
- Msvm_VLANEndpoint.NameFormat
- Msvm_VLANEndpoint.ProtocolType
- Msvm_VLANEndpoint.ProtocolIFType
- Msvm_VLANEndpoint.OtherTypeDescription
- Msvm_VLANEndpoint.DesiredEndpointMode
- Msvm_VLANEndpoint.OtherEndpointMode
- Msvm_VLANEndpoint.OperationalEndpointMode
- Msvm_VLANEndpoint.DesiredVLANTrunkEncapsulation
- Msvm_VLANEndpoint.OtherTrunkEncapsulation
- Msvm_VLANEndpoint.OperationalVLANTrunkEncapsulation
- Msvm_VLANEndpoint.GVRPStatus
- Msvm_VLANEndpoint.SupportedEndpointModes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5606e18fd1327f17feaac07570e5bf8c0c8eb59d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991988"
---
# <a name="msvm_vlanendpoint-class"></a>Msvm \_ VLANEndpoint 類別

代表交換器埠的 VLAN 端點。 此端點的設定將會變更交換器埠透過交換器傳送 VLAN 封包的方式。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VLANEndpoint : CIM_VLANEndpoint
{
  string   InstanceID;
  String   Caption = "VLAN Endpoint";
  string   Description = "Microsoft VLAN Endpoint";
  String   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  String   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_VirtualSwitch";
  string   SystemName;
  String   CreationClassName = "Msvm_VLANEndpoint";
  String   NameFormat;
  uint16   ProtocolType;
  uint16   ProtocolIFType = 1;
  String   OtherTypeDescription = "Virtual Ethernet";
  uint16   DesiredEndpointMode;
  string   OtherEndpointMode;
  uint16   OperationalEndpointMode;
  uint16   DesiredVLANTrunkEncapsulation;
  string   OtherTrunkEncapsulation;
  uint16   OperationalVLANTrunkEncapsulation;
  uint16   GVRPStatus;
  uint16   SupportedEndpointModes[];
};
```

## <a name="members"></a>成員

**Msvm \_ VLANEndpoint** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Msvm \_ VLANEndpoint** 類別具有這些方法。



| 方法                                                             | 描述                         |
|:-------------------------------------------------------------------|:------------------------------------|
| [**RequestStateChange**](msvm-vlanendpoint-requeststatechange.md) | 要求狀態變更。<br/> |



 

### <a name="properties"></a>屬性

**Msvm \_ VLANEndpoint** 類別具有這些屬性。

<dl> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出用於起始狀態變更之 [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement)方法的 *RequestedState* 參數可能的值。 列出的值將會是與 **cim \_ EnabledLogicalElementCapabilities** 相關聯的實例之 **RequestedStatesSupported** 屬性中所含值的子集，其中選取的值是 [**cim \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))目前狀態的函式。 如果實作為目前狀態的函式，則這個屬性可以是非 **Null** 的值。 如果實作為目前狀態的函式無法判斷可能的值集，這個屬性將會是 **Null** 。

這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。

<dl> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (2) 
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (3) 
</dt> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**關機** (4) 
</dt> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**離線** (6) 
</dt> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>**測試** (7) 
</dt> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**延** 後 (8) 
</dt> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**靜止** (9) 
</dt> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**重新開機** (10) 
</dt> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**重設** (11) 
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF 保留** ( .。。 )
</dt> </dl>

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的簡短描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「VLAN 端點」。

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出檢測與基礎受管理元素通訊的能力。 **Null** 值表示不會執行此屬性。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

建立實例時所使用之類別或子類別的名稱。 這個屬性繼承自 [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)，而且一律設定為 "Msvm \_ VLANEndpoint"。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對物件的描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為「Microsoft VLAN 端點」。

</dd> <dt>

**DesiredEndpointMode**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：僅限寫入
</dt> </dl>

要求使用的所需 VLAN 模式。 目前的模式是由 **OperationalEndpointMode** 屬性所指定。 這個屬性繼承自 [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint)。



| 值                                                                                                                                                                                                                                                                     | 意義                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF 保留**</dt> <dt>0</dt> </dl>                       |                                                                                                                                                                                                                                                                                  |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**其他**</dt> <dt>1</dt> </dl>                                                       |                                                                                                                                                                                                                                                                                  |
| <span id="Access"></span><span id="access"></span><span id="ACCESS"></span><dl> <dt>**存取**</dt> <dt>2</dt> </dl>                                                   | 將端點/切換埠置於永久 nontrunking 模式，並協調以將連結轉換成 nontrunk 連結。 端點會變成 nontrunk 介面。<br/>                                                                                                     |
| <span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span><dl> <dt>**動態 Auto**</dt> <dt>3</dt> </dl>                           | 讓端點能夠將連結轉換為主幹連結。 如果相鄰介面設定為主幹或理想模式，則端點會變成主幹介面。<br/>                                                                                                   |
| <span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span><dl> <dt>**動態預期**</dt> <dt>4</dt> </dl>       | 讓端點主動嘗試將連結轉換成主幹連結。 如果相鄰介面設定為主幹、理想或自動模式，則端點會變成主幹介面。 所有乙太網路介面的預設交換器埠模式都是動態的。<br/> |
| <span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span><dl> <dt>**主幹**</dt> <dt>5</dt> </dl>                                                       | 將端點置於永久的中繼模式，並協調以將連結轉換成主幹連結。 即使相鄰介面不是主幹介面，端點仍會變成主幹介面。<br/>                                                               |
| <span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span><dl> <dt>**Dot1Q**</dt>通道 <dt>6</dt> </dl>                           | 將介面設定為通道， (nontrunking) 端點/埠連接到具有 802.1 Q 主幹埠的非對稱連結。 802.1 q 通道是用來維護服務提供者網路間客戶的 VLAN 完整性。<br/>                                     |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF 保留**</dt>的 <dt>7 32767</dt> </dl>                 |                                                                                                                                                                                                                                                                                  |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <dt>**廠商保留**</dt>的 <dt>32768 65535</dt> </dl> |                                                                                                                                                                                                                                                                                  |



 

</dd> <dt>

**DesiredVLANTrunkEncapsulation**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

要求使用的 VLAN 封裝類型。 目前使用的封裝是由 **OperationalVLANTrunkEncapsulation** 屬性所指定。 只有當端點以中繼模式運作時，才適用此屬性 (如需其他詳細資料) ，請參閱 **OperationalEndpointMode** 屬性。 此屬性為 2 (不適用)  (也就是端點永遠不會置於中繼模式) 、特定類型 (802.1 Q 或 Cisco ISL) ，或 5 (協商) ，也就是此介面與其鄰近 (之間的協商結果。 如果端點不支援協商，則不允許值 5 (協商) 。 這項功能與硬體和廠商相依。 這個屬性繼承自 [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint)。

<dl> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** (0) 
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 
</dt> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (2) 
</dt> <dt>

<span id="802.1Q"></span><span id="802.1q"></span>**802.1 q** (3) 
</dt> <dt>

<span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>**CISCO ISL** (4) 
</dt> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**協商** (5) 
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** 的 (6 32767) 
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (32768 65535) 
</dt> </dl>

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

物件的顯示名稱。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

系統管理員的預設或啟動設定，適用于元素的啟用狀態。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) ，而且一律設定為 2 (啟用) 。

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此元素的已啟用和停用狀態。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 5 (不適用) 。

</dd> <dt>

**GVRPStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否已在主幹端點/埠上啟用或停用 GARP VLAN 註冊通訊協定 (GVRP) 。 除非端點支援 GVRP，否則此屬性為 2 (不適用) 。 只有當端點以中繼模式運作時，才適用此屬性 (如需其他詳細資料) ，請參閱 **OperationalEndpointMode** 屬性。 這個屬性繼承自 [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint)。

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 
</dt> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (2) 
</dt> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) 
</dt> <dt>

<span id="Disabled_"></span><span id="disabled_"></span><span id="DISABLED_"></span>**已停用** (4 ) 
</dt> </dl>

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

專案目前的健康情況。 這個屬性會表示此元素的健全狀況，但不一定是它的子元件。 可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 5 (確定) 。

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

安裝物件的日期和時間。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且不會使用它。

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

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

已知物件的標籤。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

為確保 **Name** 屬性的值是唯一的，所選取的命名啟發式。 這個屬性是從 [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint) 繼承而來的。

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。 **Null** 值表示不會執行此屬性。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**OperationalEndpointMode**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

VLAN 端點的設定模式。 這個屬性繼承自 [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint)。



| 值                                                                                                                                                                                                                                                                     | 意義                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF 保留**</dt> <dt>0</dt> </dl>                       |                                                                                                                                                                                                                                                                     |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**其他**</dt> <dt>1</dt> </dl>                                                       | 端點不是 VLAN 感知。<br/>                                                                                                                                                                                                                          |
| <span id="Access"></span><span id="access"></span><span id="ACCESS"></span><dl> <dt>**存取**</dt> <dt>2</dt> </dl>                                                   | 將端點置於永久 nontrunking 模式，並協調以將連結轉換成 nontrunk 連結。 端點會變成 nontrunk 介面。<br/>                                                                                                    |
| <span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span><dl> <dt>**動態 Auto**</dt> <dt>3</dt> </dl>                           | 讓端點能夠將連結轉換為主幹連結。 如果相鄰介面設定為主幹或理想模式，則端點會變成主幹介面。<br/>                                                                                      |
| <span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span><dl> <dt>**動態預期**</dt> <dt>4</dt> </dl>       | 讓端點主動嘗試將連結轉換成主幹連結。 如果相鄰介面設定為主幹、理想或自動模式，則端點會變成主幹介面。 這是所有乙太網路介面的預設交換器埠模式。<br/> |
| <span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span><dl> <dt>**主幹**</dt> <dt>5</dt> </dl>                                                       | 將端點置於永久的中繼模式，並協調以將連結轉換成主幹連結。 即使相鄰介面不是主幹介面，端點仍會變成主幹介面。<br/>                                                  |
| <span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span><dl> <dt>**Dot1Q**</dt>通道 <dt>6</dt> </dl>                           | 將介面設定為通道， (nontrunking) 端點/埠連接到具有 802.1 Q 主幹埠的非對稱連結。 802.1 q 通道是用來維護服務提供者網路間客戶的 VLAN 完整性。<br/>                        |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF 保留**</dt>的 <dt>7 32767</dt> </dl>                 |                                                                                                                                                                                                                                                                     |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <dt>**廠商保留**</dt>的 <dt>32768 65535</dt> </dl> |                                                                                                                                                                                                                                                                     |



 

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的目前狀態。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為 2 (確定) 。

</dd> <dt>

**OperationalVLANTrunkEncapsulation**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

在主幹端點/埠上使用的 VLAN 封裝類型。 此屬性為 2 (不適用)  (也就是端點未在中繼模式中運作) 、特定類型 (3 802.1 Q 或 4-Cisco ISL) 、5 (協商) ，也就是端點正在協調封裝類型 (。 只有當端點以中繼模式運作時，才適用此屬性 (如需其他詳細資料) ，請參閱 **OperationalEndpointMode** 屬性。 這個屬性繼承自 [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint)。

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 
</dt> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (2) 
</dt> <dt>

<span id="802.1Q"></span><span id="802.1q"></span>**802.1 q** (3) 
</dt> <dt>

<span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>**CISCO ISL** (4) 
</dt> <dt>

<span id="Negotiating"></span><span id="negotiating"></span><span id="NEGOTIATING"></span>**協商** (5) 
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** 的 (6 32767) 
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (32768 65535) 
</dt> </dl>

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述當 **EnabledState** 屬性設定為 1 ( "Other" ) 時，專案已啟用或停用狀態的字串。 當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。

</dd> <dt>

**OtherEndpointMode**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

當 **OperationalEndpointMode** 屬性的值設定為1時，此 vlan 端點所支援的 vlan 端點模型類型 (其他) 。 當 **OperationalEndpointMode** 屬性是1以外的任何值時，這個屬性應該設為 **Null** 。 這個屬性繼承自 [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint)。

</dd> <dt>

**OtherTrunkEncapsulation**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

當 **OperationalVLANTrunkEncapsulation** 屬性的值設定為 1 (其他) 時，此 vlan 端點所支援的 vlan 封裝類型。 當所需的封裝屬性是1以外的任何值時，這個屬性應該設為 **Null** 。 這個屬性繼承自 [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint)。

</dd> <dt>

**OtherTypeDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

當這個類別的 **型** 別屬性 (或其任何子類別) 設定為 1 (其他) 時，通訊協定端點的類型。 這個屬性繼承自 [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)，一律設為「虛擬乙太網路」。

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

提供高層級的狀態資訊。 這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態資訊。 **Null** 值表示不會執行此屬性。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**ProtocolIFType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

[IANA IFTYPE MIB](https://www.iana.org/assignments/ianaiftype-mib)。 這個屬性繼承自 [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)，且一律設定為 1 (其他) 。

</dd> <dt>

**ProtocolType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性是從 [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint) 繼承而來的。

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

上次要求或預期的管理服務狀態。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 12 (不適用) 。



| 值                                                                         | 意義                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>12</dt> </dl> | 不適用。<br/> |



 

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述元素的狀態。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

正常

錯誤

降級

不明

「Pred 失敗」

入門

從而

維護

強調

"NonRecover"

「無連絡人」

「遺失通訊」

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述各種 **OperationalStatus** 陣列值的字串。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為 "OK"。

</dd> <dt>

**SupportedEndpointModes**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) 
</dt> </dl>

此埠所支援的端點模式。

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

範圍系統的建立類別名稱。 這個屬性繼承自 [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)，且一律設定為 "Msvm \_ VirtualSwitch"

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

範圍系統的系統名稱。 這個屬性繼承自 [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)。

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

專案的已啟用狀態上次變更的日期和時間。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，但不受支援。

</dd> <dt>

**TransitioningToState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出實例正在轉換的目標狀態。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，但不會使用它。

</dd> </dl>

## <a name="remarks"></a>備註

存取 **Msvm \_ VLANEndpoint** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

## <a name="examples"></a>範例

請參閱 [查詢網路物件](querying-networking-objects.md)。

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

[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md)
</dt> <dt>

[**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint)
</dt> </dl>

 


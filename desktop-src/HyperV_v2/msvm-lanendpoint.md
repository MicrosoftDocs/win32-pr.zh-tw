---
description: 代表網路介面卡的邏輯連接點。 當 LAN 端點連接到交換器埠時，連接到 LAN 端點的網路介面卡會具有網路連線能力。
ms.assetid: 68aad05e-64b5-44dc-ab5b-8f3051fa77ca
title: Msvm_LANEndpoint 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LANEndpoint
- Msvm_LANEndpoint.InstanceID
- Msvm_LANEndpoint.Caption
- Msvm_LANEndpoint.Description
- Msvm_LANEndpoint.ElementName
- Msvm_LANEndpoint.InstallDate
- Msvm_LANEndpoint.Name
- Msvm_LANEndpoint.OperationalStatus
- Msvm_LANEndpoint.StatusDescriptions
- Msvm_LANEndpoint.Status
- Msvm_LANEndpoint.HealthState
- Msvm_LANEndpoint.CommunicationStatus
- Msvm_LANEndpoint.DetailedStatus
- Msvm_LANEndpoint.OperatingStatus
- Msvm_LANEndpoint.PrimaryStatus
- Msvm_LANEndpoint.EnabledState
- Msvm_LANEndpoint.OtherEnabledState
- Msvm_LANEndpoint.RequestedState
- Msvm_LANEndpoint.EnabledDefault
- Msvm_LANEndpoint.TimeOfLastStateChange
- Msvm_LANEndpoint.AvailableRequestedStates
- Msvm_LANEndpoint.TransitioningToState
- Msvm_LANEndpoint.SystemCreationClassName
- Msvm_LANEndpoint.SystemName
- Msvm_LANEndpoint.CreationClassName
- Msvm_LANEndpoint.NameFormat
- Msvm_LANEndpoint.ProtocolType
- Msvm_LANEndpoint.ProtocolIFType
- Msvm_LANEndpoint.OtherTypeDescription
- Msvm_LANEndpoint.LANID
- Msvm_LANEndpoint.LANType
- Msvm_LANEndpoint.OtherLANType
- Msvm_LANEndpoint.MACAddress
- Msvm_LANEndpoint.AliasAddresses
- Msvm_LANEndpoint.GroupAddresses
- Msvm_LANEndpoint.MaxDataSize
- Msvm_LANEndpoint.Connected
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7585b92461b435b99a05ed198c4c501e10703439
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192991"
---
# <a name="msvm_lanendpoint-class"></a>Msvm \_ LANEndpoint 類別

代表網路介面卡的邏輯連接點。 當 LAN 端點連接到交換器埠時，連接到 LAN 端點的網路介面卡會具有網路連線能力。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LANEndpoint : CIM_LANEndpoint
{
  string   InstanceID;
  string   Caption = "LAN Endpoint";
  string   Description = "Microsoft Virtual LAN Endpoint";
  string   ElementName;
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
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_LANEndpoint";
  string   NameFormat = "Microsoft Virtual Device ID";
  uint16   ProtocolType;
  uint16   ProtocolIFType;
  string   OtherTypeDescription;
  string   LANID;
  uint16   LANType;
  string   OtherLANType;
  string   MACAddress;
  string   AliasAddresses[];
  string   GroupAddresses[];
  uint32   MaxDataSize;
  boolean  Connected;
};
```

## <a name="members"></a>成員

**Msvm \_ LANEndpoint** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Msvm \_ LANEndpoint** 類別具有這些方法。



| 方法                                                            | 描述                         |
|:------------------------------------------------------------------|:------------------------------------|
| [**RequestStateChange**](msvm-lanendpoint-requeststatechange.md) | 要求狀態變更。<br/> |



 

### <a name="properties"></a>屬性

**Msvm \_ LANEndpoint** 類別具有這些屬性。

<dl> <dt>

**AliasAddresses**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

可能用來與 LAN 端點通訊的其他單播位址。 這個屬性繼承自 [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85))。

</dd> <dt>

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

物件的簡短描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為「LAN 端點」。

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出檢測與基礎受管理元素通訊的能力。 **Null** 值表示不會執行此屬性。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**已連接**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

如果 LAN 端點連接到交換器埠，這個屬性會設定為 **True** 。

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **Key**、 **MaxLen** ( 256 ) 
</dt> </dl>

建立實例時所使用之類別或子類別的名稱。 這個屬性繼承自 [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)，而且一律設定為 "Msvm \_ LANEndpoint"。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對物件的描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為「Microsoft 虛擬 LAN 端點」。

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

系統管理員的預設或啟動設定，適用于元素的啟用狀態。 這個屬性會繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) ，而且會是下列其中一個值。

<dl> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (2) 
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (3) 
</dt> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**已啟用但離線** (6) 
</dt> </dl>

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定已規劃系統的啟用狀態。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，它可以是下列值之一。



| 值                                                                                                                                                                                                                                                                       | 意義                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**停用**</dt> <dt>3</dt> </dl>                                             | 系統已關閉。<br/>                                             |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <dt>**不適用**</dt> <dt>5</dt> </dl>                     | 元素不支援啟用或停用。<br/>               |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <dt>**已啟用但離線**</dt> <dt>6</dt> </dl> | 系統已啟用但離線。 將會捨棄任何新的要求。<br/> |



 

</dd> <dt>

**GroupAddresses**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

LAN 端點接聽的多播位址。 這個屬性繼承自 [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85))。

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

專案目前的健康情況。 這個屬性會表示此元素的健全狀況，但不一定是它的子元件。 可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 5 (確定) 。



| 值                                                                        | 意義                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>5</dt> </dl> | 健全狀況狀態為 [正常]。<br/> |



 

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

建立虛擬機器設定的日期和時間。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

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

**LANID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

端點所連接之 LAN 區段的標籤或識別碼。 如果端點目前非使用中/已連線，或這項資訊未知，則這個屬性會是 **Null**。 這個屬性繼承自 [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85))。

</dd> <dt>

**LANType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性已被取代，代替 **ProtocolType** 屬性。 這個屬性繼承自 [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85))。

</dd> <dt>

**MACAddress**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **MaxLen** ( 12 ) 
</dt> </dl>

與 LAN 端點通訊時使用的 MAC 位址。 MAC 位址的格式為十二個十六進位數位 (例如 "010203040506" ) ，其中每一組代表根據 RFC 2469 的標準位順序，其中一個 MAC 位址的六個八位。 這個屬性繼承自 [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85))。

</dd> <dt>

**MaxDataSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **單位** ( "Bits" ) 
</dt> </dl>

LAN 端點可能傳送或接收之資訊欄位的最大大小（以位數為單位）。 這個屬性繼承自 [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85))。

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
</dt> <dt>

限定詞： **MaxLen** ( 256 ) 
</dt> </dl>

包含已選取的命名啟發式，以確保 **Name** 屬性的值是唯一的。 這個屬性會繼承自 [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)，而且會設定為「MICROSOFT 虛擬裝置識別碼」。

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

物件的目前狀態。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為 2 (確定) 。

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述當 **EnabledState** 屬性設定為 1 ( "Other" ) 時，專案已啟用或停用狀態的字串。 當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。

</dd> <dt>

**OtherLANType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性已被取代，代替 **OtherTypeDescription** 屬性。 這個屬性繼承自 [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85))。

</dd> <dt>

**OtherTypeDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **MaxLen** ( 64 ) 
</dt> </dl>

描述當這個類別的 **ProtocolIFType** 屬性 (或其任何子類別) 設定為 1 (其他) 時，通訊協定端點型別的字串。 當 **ProtocolIFType** 屬性是1以外的任何值時，這個屬性應該設為 **Null** 。 這個屬性繼承自 [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)。

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

屬性是用來分類和分類這個類別的實例。 如果 **ProtocolIFType** 設定為 1 (其他) ，則應該在 **OtherTypeDescription** 屬性中提供類型資訊。 這個屬性繼承自 [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)。

> [!Note]  
> **ProtocolIFType** 是與 [IANA ifType MIB](https://www.iana.org/assignments/ianaiftype-mib)同步的列舉。 也會包含其他以 DMTF 定義的值。

 

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 
</dt> <dt>

<span id="Regular_1822"></span><span id="regular_1822"></span><span id="REGULAR_1822"></span>**一般 1822** (2) 
</dt> <dt>

<span id="HDH_1822"></span><span id="hdh_1822"></span>**HDH 1822** (3) 
</dt> <dt>

<span id="DDN_X.25"></span><span id="ddn_x.25"></span>**DDN** (4) 
</dt> <dt>

<span id="RFC877_X.25"></span><span id="rfc877_x.25"></span>**RFC877 X. 25** (5) 
</dt> <dt>

<span id="Ethernet_CSMA_CD"></span><span id="ethernet_csma_cd"></span><span id="ETHERNET_CSMA_CD"></span>**ETHERNET CSMA/CD** (6) 
</dt> <dt>

<span id="ISO_802.3_CSMA_CD"></span><span id="iso_802.3_csma_cd"></span>**ISO 802.3 CSMA/CD** (7) 
</dt> <dt>

<span id="ISO_802.4_Token_Bus"></span><span id="iso_802.4_token_bus"></span><span id="ISO_802.4_TOKEN_BUS"></span>**ISO 802.4 權杖匯流排** (8) 
</dt> <dt>

<span id="ISO_802.5_Token_Ring"></span><span id="iso_802.5_token_ring"></span><span id="ISO_802.5_TOKEN_RING"></span>**ISO 802.5 權杖環** (9) 
</dt> <dt>

<span id="ISO_802.6_MAN"></span><span id="iso_802.6_man"></span>**ISO 802.6 MAN** (10) 
</dt> <dt>

<span id="StarLAN"></span><span id="starlan"></span><span id="STARLAN"></span>**StarLAN** (11) 
</dt> <dt>

<span id="Proteon_10Mbit"></span><span id="proteon_10mbit"></span><span id="PROTEON_10MBIT"></span>**Proteon 10Mbit** (12) 
</dt> <dt>

<span id="Proteon_80Mbit"></span><span id="proteon_80mbit"></span><span id="PROTEON_80MBIT"></span>**Proteon 80Mbit** (13) 
</dt> <dt>

<span id="HyperChannel"></span><span id="hyperchannel"></span><span id="HYPERCHANNEL"></span>**HyperChannel** (14) 
</dt> <dt>

<span id="FDDI"></span><span id="fddi"></span>**FDDI** (15) 
</dt> <dt>

<span id="LAP-B"></span><span id="lap-b"></span>**膝上-B** (16) 
</dt> <dt>

<span id="SDLC"></span><span id="sdlc"></span>**SDLC** (17) 
</dt> <dt>

<span id="DS1"></span><span id="ds1"></span>**DS1** (18) 
</dt> <dt>

<span id="E1"></span><span id="e1"></span>**E1** (19) 
</dt> <dt>

<span id="Basic_ISDN"></span><span id="basic_isdn"></span><span id="BASIC_ISDN"></span>**基本 ISDN** (20) 
</dt> <dt>

<span id="Primary_ISDN"></span><span id="primary_isdn"></span><span id="PRIMARY_ISDN"></span>**主要 ISDN** (21) 
</dt> <dt>

<span id="Proprietary_Point-to-Point_Serial"></span><span id="proprietary_point-to-point_serial"></span><span id="PROPRIETARY_POINT-TO-POINT_SERIAL"></span>**專屬點對點序列** (22) 
</dt> <dt>

<span id="PPP"></span><span id="ppp"></span>**PPP** (23) 
</dt> <dt>

<span id="Software_Loopback"></span><span id="software_loopback"></span><span id="SOFTWARE_LOOPBACK"></span>**軟體回送** (24) 
</dt> <dt>

<span id="EON"></span><span id="eon"></span>**EON** (25) 
</dt> <dt>

<span id="Ethernet_3Mbit"></span><span id="ethernet_3mbit"></span><span id="ETHERNET_3MBIT"></span>**Ethernet 3Mbit** (26) 
</dt> <dt>

<span id="NSIP"></span><span id="nsip"></span>**NSIP** (27) 
</dt> <dt>

<span id="SLIP"></span><span id="slip"></span>**SLIP** (28) 
</dt> <dt>

<span id="Ultra"></span><span id="ultra"></span><span id="ULTRA"></span>**Ultra** (29) 
</dt> <dt>

<span id="DS3"></span><span id="ds3"></span>**DS3** (30) 
</dt> <dt>

<span id="SIP"></span><span id="sip"></span>**SIP** (31) 
</dt> <dt>

<span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**框架轉送** (32) 
</dt> <dt>

<span id="RS-232"></span><span id="rs-232"></span>**RS-232** (33) 
</dt> <dt>

<span id="Parallel"></span><span id="parallel"></span><span id="PARALLEL"></span>**平行** (34) 
</dt> <dt>

<span id="ARCNet"></span><span id="arcnet"></span><span id="ARCNET"></span>**ARCNet** (35) 
</dt> <dt>

<span id="ARCNet_Plus"></span><span id="arcnet_plus"></span><span id="ARCNET_PLUS"></span>**ARCNet Plus** (36) 
</dt> <dt>

<span id="ATM"></span><span id="atm"></span>**ATM** (37) 
</dt> <dt>

<span id="MIO_X.25"></span><span id="mio_x.25"></span>MIO (38) **的**
</dt> <dt>

<span id="SONET"></span><span id="sonet"></span>**SONET** (39) 
</dt> <dt>

<span id="X.25_PLE"></span><span id="x.25_ple"></span>**PLE** (40) 
</dt> <dt>

<span id="ISO_802.211c"></span><span id="iso_802.211c"></span><span id="ISO_802.211C"></span>**ISO 802.211 c** (41) 
</dt> <dt>

<span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>**LocalTalk** (42) 
</dt> <dt>

<span id="SMDS_DXI"></span><span id="smds_dxi"></span>**SMDS DXI** (43) 
</dt> <dt>

<span id="Frame_Relay_Service"></span><span id="frame_relay_service"></span><span id="FRAME_RELAY_SERVICE"></span>**框架轉送服務** (44) 
</dt> <dt>

<span id="V.35"></span><span id="v.35"></span>**V. 35** (45) 
</dt> <dt>

<span id="HSSI"></span><span id="hssi"></span>**HSSI** (46) 
</dt> <dt>

<span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (47) 
</dt> <dt>

<span id="Modem"></span><span id="modem"></span><span id="MODEM"></span>**數據機** (48) 
</dt> <dt>

<span id="AAL5"></span><span id="aal5"></span>**AAL5** (49) 
</dt> <dt>

<span id="SONET_Path"></span><span id="sonet_path"></span><span id="SONET_PATH"></span>**SONET 路徑** (50) 
</dt> <dt>

<span id="SONET_VT"></span><span id="sonet_vt"></span>**SONET VT** (51) 
</dt> <dt>

<span id="SMDS_ICIP"></span><span id="smds_icip"></span>**SMDS ICIP** (52) 
</dt> <dt>

<span id="Proprietary_Virtual_Internal"></span><span id="proprietary_virtual_internal"></span><span id="PROPRIETARY_VIRTUAL_INTERNAL"></span>**專屬的 Virtual/Internal** (53) 
</dt> <dt>

<span id="Proprietary_Multiplexor"></span><span id="proprietary_multiplexor"></span><span id="PROPRIETARY_MULTIPLEXOR"></span>**專屬多重通道** (54) 
</dt> <dt>

<span id="IEEE_802.12"></span><span id="ieee_802.12"></span>**IEEE 802.12** (55) 
</dt> <dt>

<span id="Fibre_Channel"></span><span id="fibre_channel"></span><span id="FIBRE_CHANNEL"></span>**光纖通道** (56) 
</dt> <dt>

<span id="HIPPI_Interface"></span><span id="hippi_interface"></span><span id="HIPPI_INTERFACE"></span>**HIPPI 介面** (57) 
</dt> <dt>

<span id="Frame_Relay_Interconnect"></span><span id="frame_relay_interconnect"></span><span id="FRAME_RELAY_INTERCONNECT"></span>**框架轉送互連** (58) 
</dt> <dt>

<span id="ATM_Emulated_LAN_for_802.3"></span><span id="atm_emulated_lan_for_802.3"></span><span id="ATM_EMULATED_LAN_FOR_802.3"></span>**適用于 802.3 (59) 的 ATM 模擬 LAN**
</dt> <dt>

<span id="ATM_Emulated_LAN_for_802.5"></span><span id="atm_emulated_lan_for_802.5"></span><span id="ATM_EMULATED_LAN_FOR_802.5"></span>**適用于 802.5 (60) 的 ATM 模擬 LAN**
</dt> <dt>

<span id="ATM_Emulated_Circuit"></span><span id="atm_emulated_circuit"></span><span id="ATM_EMULATED_CIRCUIT"></span>**ATM 模擬線路** (61) 
</dt> <dt>

<span id="Fast_Ethernet__100BaseT_"></span><span id="fast_ethernet__100baset_"></span><span id="FAST_ETHERNET__100BASET_"></span>**快速乙太網路 (100BaseT)** (62) 
</dt> <dt>

<span id="ISDN"></span><span id="isdn"></span>**ISDN** (63) 
</dt> <dt>

<span id="V.11"></span><span id="v.11"></span>**11** (64) 
</dt> <dt>

<span id="V.36"></span><span id="v.36"></span>**5v** (65) 
</dt> <dt>

<span id="G703_at_64K"></span><span id="g703_at_64k"></span><span id="G703_AT_64K"></span>**G703 在 64k** (66) 
</dt> <dt>

<span id="G703_at_2Mb"></span><span id="g703_at_2mb"></span><span id="G703_AT_2MB"></span>**G703，以 2mb** (67) 
</dt> <dt>

<span id="QLLC"></span><span id="qllc"></span>**QLLC** (68) 
</dt> <dt>

<span id="Fast_Ethernet_100BaseFX"></span><span id="fast_ethernet_100basefx"></span><span id="FAST_ETHERNET_100BASEFX"></span>**快速 Ethernet 100BaseFX** (69) 
</dt> <dt>

<span id="Channel"></span><span id="channel"></span><span id="CHANNEL"></span>**Channel** (70) 
</dt> <dt>

<span id="IEEE_802.11"></span><span id="ieee_802.11"></span>**IEEE 802.11** (71) 
</dt> <dt>

<span id="IBM_260_370_OEMI_Channel"></span><span id="ibm_260_370_oemi_channel"></span><span id="IBM_260_370_OEMI_CHANNEL"></span>**IBM 260/370 OEMI Channel** (72) 
</dt> <dt>

<span id="ESCON"></span><span id="escon"></span>**ESCON** (73) 
</dt> <dt>

<span id="Data_Link_Switching"></span><span id="data_link_switching"></span><span id="DATA_LINK_SWITCHING"></span> (74) 的 **資料連結切換**
</dt> <dt>

<span id="ISDN_S_T_Interface"></span><span id="isdn_s_t_interface"></span><span id="ISDN_S_T_INTERFACE"></span>**ISDN S/T 介面** (75) 
</dt> <dt>

<span id="ISDN_U_Interface"></span><span id="isdn_u_interface"></span><span id="ISDN_U_INTERFACE"></span>**ISDN U 介面** (76) 
</dt> <dt>

<span id="LAP-D"></span><span id="lap-d"></span>**膝上-D** (77) 
</dt> <dt>

<span id="IP_Switch"></span><span id="ip_switch"></span><span id="IP_SWITCH"></span>**IP 交換器** (78) 
</dt> <dt>

<span id="Remote_Source_Route_Bridging"></span><span id="remote_source_route_bridging"></span><span id="REMOTE_SOURCE_ROUTE_BRIDGING"></span>**遠端來源路由橋接** (79) 
</dt> <dt>

<span id="ATM_Logical"></span><span id="atm_logical"></span><span id="ATM_LOGICAL"></span>**ATM Logical** (80) 
</dt> <dt>

<span id="DS0"></span><span id="ds0"></span>**DS0** (81) 
</dt> <dt>

<span id="DS0_Bundle"></span><span id="ds0_bundle"></span><span id="DS0_BUNDLE"></span>**DS0** 組合 (82) 
</dt> <dt>

<span id="BSC"></span><span id="bsc"></span>**.Bsc** (83) 
</dt> <dt>

<span id="Async"></span><span id="async"></span><span id="ASYNC"></span>**非同步** (84) 
</dt> <dt>

<span id="Combat_Net_Radio"></span><span id="combat_net_radio"></span><span id="COMBAT_NET_RADIO"></span>**對抗網路廣播** (85) 
</dt> <dt>

<span id="ISO_802.5r_DTR"></span><span id="iso_802.5r_dtr"></span><span id="ISO_802.5R_DTR"></span>**ISO 802.5 r DTR** (86) 
</dt> <dt>

<span id="Ext_Pos_Loc_Report_System"></span><span id="ext_pos_loc_report_system"></span><span id="EXT_POS_LOC_REPORT_SYSTEM"></span>**Ext Pos Loc 報表系統** (87) 
</dt> <dt>

<span id="AppleTalk_Remote_Access_Protocol"></span><span id="appletalk_remote_access_protocol"></span><span id="APPLETALK_REMOTE_ACCESS_PROTOCOL"></span>**AppleTalk 遠端存取通訊協定** (88) 
</dt> <dt>

<span id="Proprietary_Connectionless"></span><span id="proprietary_connectionless"></span><span id="PROPRIETARY_CONNECTIONLESS"></span>**專屬的無連接** (89) 
</dt> <dt>

<span id="ITU_X.29_Host_PAD"></span><span id="itu_x.29_host_pad"></span><span id="ITU_X.29_HOST_PAD"></span>**ITU X. 29 主機板** (90) 
</dt> <dt>

<span id="ITU_X.3_Terminal_PAD"></span><span id="itu_x.3_terminal_pad"></span><span id="ITU_X.3_TERMINAL_PAD"></span>**ITU X. 3 終端機板** (91) 
</dt> <dt>

<span id="Frame_Relay_MPI"></span><span id="frame_relay_mpi"></span><span id="FRAME_RELAY_MPI"></span>**框架轉送 MPI** (92) 
</dt> <dt>

<span id="ITU_X.213"></span><span id="itu_x.213"></span>**ITU X 213** (93) 
</dt> <dt>

<span id="ADSL"></span><span id="adsl"></span>**ADSL** (94) 
</dt> <dt>

<span id="RADSL"></span><span id="radsl"></span>**RADSL** (95) 
</dt> <dt>

<span id="SDSL"></span><span id="sdsl"></span>**SDSL** (96) 
</dt> <dt>

<span id="VDSL"></span><span id="vdsl"></span>**VDSL** (97) 
</dt> <dt>

<span id="ISO_802.5_CRFP"></span><span id="iso_802.5_crfp"></span>**ISO 802.5 CRFP** (98) 
</dt> <dt>

<span id="Myrinet"></span><span id="myrinet"></span><span id="MYRINET"></span>**Myrinet** (99) 
</dt> <dt>

<span id="Voice_Receive_and_Transmit"></span><span id="voice_receive_and_transmit"></span><span id="VOICE_RECEIVE_AND_TRANSMIT"></span>**語音接收和傳輸** (100) 
</dt> <dt>

<span id="Voice_Foreign_Exchange_Office"></span><span id="voice_foreign_exchange_office"></span><span id="VOICE_FOREIGN_EXCHANGE_OFFICE"></span>**語音外部 Exchange 辦公室** (101) 
</dt> <dt>

<span id="Voice_Foreign_Exchange_Service"></span><span id="voice_foreign_exchange_service"></span><span id="VOICE_FOREIGN_EXCHANGE_SERVICE"></span>**語音外部交換服務** (102) 
</dt> <dt>

<span id="Voice_Encapsulation"></span><span id="voice_encapsulation"></span><span id="VOICE_ENCAPSULATION"></span>**語音封裝** (103) 
</dt> <dt>

<span id="Voice_over_IP"></span><span id="voice_over_ip"></span><span id="VOICE_OVER_IP"></span>**語音 OVER IP** (104) 
</dt> <dt>

<span id="ATM_DXI"></span><span id="atm_dxi"></span>**ATM DXI** (105) 
</dt> <dt>

<span id="ATM_FUNI"></span><span id="atm_funi"></span>**ATM FUNI** (106) 
</dt> <dt>

<span id="ATM_IMA"></span><span id="atm_ima"></span>**ATM IMA** (107) 
</dt> <dt>

<span id="PPP_Multilink_Bundle"></span><span id="ppp_multilink_bundle"></span><span id="PPP_MULTILINK_BUNDLE"></span>**PPP 多重連結** 組合 (108) 
</dt> <dt>

<span id="IP_over_CDLC"></span><span id="ip_over_cdlc"></span><span id="IP_OVER_CDLC"></span>**IP OVER CDLC** (109) 
</dt> <dt>

<span id="IP_over_CLAW"></span><span id="ip_over_claw"></span><span id="IP_OVER_CLAW"></span>**IP OVER 進儉樸爬** (110) 
</dt> <dt>

<span id="Stack_to_Stack"></span><span id="stack_to_stack"></span><span id="STACK_TO_STACK"></span>**堆疊至堆疊** (111) 
</dt> <dt>

<span id="Virtual_IP_Address"></span><span id="virtual_ip_address"></span><span id="VIRTUAL_IP_ADDRESS"></span>**虛擬 IP 位址** (112) 
</dt> <dt>

<span id="MPC"></span><span id="mpc"></span>**MPC** (113) 
</dt> <dt>

<span id="IP_over_ATM"></span><span id="ip_over_atm"></span><span id="IP_OVER_ATM"></span>透過 **ATM 的 IP** (114) 
</dt> <dt>

<span id="ISO_802.5j_Fibre_Token_Ring"></span><span id="iso_802.5j_fibre_token_ring"></span><span id="ISO_802.5J_FIBRE_TOKEN_RING"></span>**ISO 802.5 j 光纖權杖環** (115) 
</dt> <dt>

<span id="TDLC"></span><span id="tdlc"></span>**TDLC** (116) 
</dt> <dt>

<span id="Gigabit_Ethernet"></span><span id="gigabit_ethernet"></span><span id="GIGABIT_ETHERNET"></span>**Gigabit Ethernet** (117) 
</dt> <dt>

<span id="HDLC"></span><span id="hdlc"></span>**HDLC** (118) 
</dt> <dt>

<span id="LAP-F"></span><span id="lap-f"></span>**膝上-F** (119) 
</dt> <dt>

<span id="V.37"></span><span id="v.37"></span>**37** (120) 
</dt> <dt>

<span id="X.25_MLP"></span><span id="x.25_mlp"></span>**MLP** (121) 
</dt> <dt>

<span id="X.25_Hunt_Group"></span><span id="x.25_hunt_group"></span><span id="X.25_HUNT_GROUP"></span> (122) **的25個搜尋群組**
</dt> <dt>

<span id="Transp_HDLC"></span><span id="transp_hdlc"></span><span id="TRANSP_HDLC"></span>**TRANSP HDLC** (123) 
</dt> <dt>

<span id="Interleave_Channel"></span><span id="interleave_channel"></span><span id="INTERLEAVE_CHANNEL"></span>**交錯通道** (124) 
</dt> <dt>

<span id="FAST_Channel"></span><span id="fast_channel"></span><span id="FAST_CHANNEL"></span>**FAST Channel** (125) 
</dt> <dt>

<span id="IP__for_APPN_HPR_in_IP_Networks_"></span><span id="ip__for_appn_hpr_in_ip_networks_"></span><span id="IP__FOR_APPN_HPR_IN_IP_NETWORKS_"></span>**Ip 網路中 APPN HPR 的 ip ()** (126) 
</dt> <dt>

<span id="CATV_MAC_Layer"></span><span id="catv_mac_layer"></span><span id="CATV_MAC_LAYER"></span>**CATV MAC 層** (127) 
</dt> <dt>

<span id="CATV_Downstream"></span><span id="catv_downstream"></span><span id="CATV_DOWNSTREAM"></span>**CATV 下游** (128) 
</dt> <dt>

<span id="CATV_Upstream"></span><span id="catv_upstream"></span><span id="CATV_UPSTREAM"></span>**CATV 上游** (129) 
</dt> <dt>

<span id="Avalon_12MPP_Switch"></span><span id="avalon_12mpp_switch"></span><span id="AVALON_12MPP_SWITCH"></span>**AVALON 12MPP 交換器** (130) 
</dt> <dt>

<span id="Tunnel"></span><span id="tunnel"></span><span id="TUNNEL"></span>通道 **(131**) 
</dt> <dt>

<span id="Coffee"></span><span id="coffee"></span><span id="COFFEE"></span>**咖啡** (132) 
</dt> <dt>

<span id="Circuit_Emulation_Service"></span><span id="circuit_emulation_service"></span><span id="CIRCUIT_EMULATION_SERVICE"></span>**線路模擬服務** (133) 
</dt> <dt>

<span id="ATM_SubInterface"></span><span id="atm_subinterface"></span><span id="ATM_SUBINTERFACE"></span>**ATM 子介面** (134) 
</dt> <dt>

<span id="Layer_2_VLAN_using_802.1Q"></span><span id="layer_2_vlan_using_802.1q"></span><span id="LAYER_2_VLAN_USING_802.1Q"></span>**使用 802.1 q (135 的第2層 VLAN**) 
</dt> <dt>

<span id="Layer_3_VLAN_using_IP"></span><span id="layer_3_vlan_using_ip"></span><span id="LAYER_3_VLAN_USING_IP"></span>**使用 IP (136 的第3層 VLAN**) 
</dt> <dt>

<span id="Layer_3_VLAN_using_IPX"></span><span id="layer_3_vlan_using_ipx"></span><span id="LAYER_3_VLAN_USING_IPX"></span>**使用 IPX 的第3層 VLAN** (137) 
</dt> <dt>

<span id="Digital_Power_Line"></span><span id="digital_power_line"></span><span id="DIGITAL_POWER_LINE"></span>**數位電源線** (138) 
</dt> <dt>

<span id="Multimedia_Mail_over_IP"></span><span id="multimedia_mail_over_ip"></span><span id="MULTIMEDIA_MAIL_OVER_IP"></span>IP (139) 的 **多媒體郵件**
</dt> <dt>

<span id="DTM"></span><span id="dtm"></span>**DTM** (140) 
</dt> <dt>

<span id="DCN"></span><span id="dcn"></span>**DCN** (141) 
</dt> <dt>

<span id="IP_Forwarding"></span><span id="ip_forwarding"></span><span id="IP_FORWARDING"></span>**IP 轉送** (142) 
</dt> <dt>

<span id="MSDSL"></span><span id="msdsl"></span>**MSDSL** (143) 
</dt> <dt>

<span id="IEEE_1394"></span><span id="ieee_1394"></span>**IEEE 1394** (144) 
</dt> <dt>

<span id="IF-GSN_HIPPI-6400"></span><span id="if-gsn_hippi-6400"></span>**IF-GSN/HIPPI-6400** (145) 
</dt> <dt>

<span id="DVB-RCC_MAC_Layer"></span><span id="dvb-rcc_mac_layer"></span><span id="DVB-RCC_MAC_LAYER"></span>**RCC MAC 層** (146) 
</dt> <dt>

<span id="DVB-RCC_Downstream"></span><span id="dvb-rcc_downstream"></span><span id="DVB-RCC_DOWNSTREAM"></span>**DVB-T RCC 下游** (147) 
</dt> <dt>

<span id="DVB-RCC_Upstream"></span><span id="dvb-rcc_upstream"></span><span id="DVB-RCC_UPSTREAM"></span>**DVB-T RCC 上游** (148) 
</dt> <dt>

<span id="ATM_Virtual"></span><span id="atm_virtual"></span><span id="ATM_VIRTUAL"></span>**ATM 虛擬** (149) 
</dt> <dt>

<span id="MPLS_Tunnel"></span><span id="mpls_tunnel"></span><span id="MPLS_TUNNEL"></span>**MPLS** 通道 (150) 
</dt> <dt>

<span id="SRP"></span><span id="srp"></span>**SRP** (151) 
</dt> <dt>

<span id="Voice_over_ATM"></span><span id="voice_over_atm"></span><span id="VOICE_OVER_ATM"></span>透過 **ATM 的語音** (152) 
</dt> <dt>

<span id="Voice_over_Frame_Relay"></span><span id="voice_over_frame_relay"></span><span id="VOICE_OVER_FRAME_RELAY"></span>**語音 Over 框架轉送** (153) 
</dt> <dt>

<span id="ISDL"></span><span id="isdl"></span>**ISDL** (154) 
</dt> <dt>

<span id="Composite_Link"></span><span id="composite_link"></span><span id="COMPOSITE_LINK"></span>**複合連結** (155) 
</dt> <dt>

<span id="SS7_Signaling_Link"></span><span id="ss7_signaling_link"></span><span id="SS7_SIGNALING_LINK"></span>**SS7 信號連結** (156) 
</dt> <dt>

<span id="Proprietary_P2P_Wireless"></span><span id="proprietary_p2p_wireless"></span><span id="PROPRIETARY_P2P_WIRELESS"></span>**專屬 P2P 無線** (157) 
</dt> <dt>

<span id="Frame_Forward"></span><span id="frame_forward"></span><span id="FRAME_FORWARD"></span>**向前框架** (158) 
</dt> <dt>

<span id="RFC1483_Multiprotocol_over_ATM"></span><span id="rfc1483_multiprotocol_over_atm"></span><span id="RFC1483_MULTIPROTOCOL_OVER_ATM"></span>透過 ATM (159) **RFC1483 多重通訊協定**
</dt> <dt>

<span id="USB"></span><span id="usb"></span>**USB** (160) 
</dt> <dt>

<span id="IEEE_802.3ad_Link_Aggregate"></span><span id="ieee_802.3ad_link_aggregate"></span><span id="IEEE_802.3AD_LINK_AGGREGATE"></span>**IEEE 802.3 Ad 連結匯總** (161) 
</dt> <dt>

<span id="BGP_Policy_Accounting"></span><span id="bgp_policy_accounting"></span><span id="BGP_POLICY_ACCOUNTING"></span>**BGP 原則帳戶** 處理 (162) 
</dt> <dt>

<span id="FRF_.16_Multilink_FR"></span><span id="frf_.16_multilink_fr"></span><span id="FRF_.16_MULTILINK_FR"></span>**FRF .16 多重連結 FR** (163) 
</dt> <dt>

<span id="H.323_Gatekeeper"></span><span id="h.323_gatekeeper"></span><span id="H.323_GATEKEEPER"></span>**H. 323 閘道管理員** (164) 
</dt> <dt>

<span id="H.323_Proxy"></span><span id="h.323_proxy"></span><span id="H.323_PROXY"></span>**H. 323 Proxy** (165) 
</dt> <dt>

<span id="MPLS"></span><span id="mpls"></span>**MPLS** (166) 
</dt> <dt>

<span id="Multi-Frequency_Signaling_Link"></span><span id="multi-frequency_signaling_link"></span><span id="MULTI-FREQUENCY_SIGNALING_LINK"></span>**多重頻率的信號連結** (167) 
</dt> <dt>

<span id="HDSL-2"></span><span id="hdsl-2"></span>**HDSL-2** (168) 
</dt> <dt>

<span id="S-HDSL"></span><span id="s-hdsl"></span>**S-HDSL** (169) 
</dt> <dt>

<span id="DS1_Facility_Data_Link"></span><span id="ds1_facility_data_link"></span><span id="DS1_FACILITY_DATA_LINK"></span>**DS1 設備資料連結** (170) 
</dt> <dt>

<span id="Packet_over_SONET_SDH"></span><span id="packet_over_sonet_sdh"></span><span id="PACKET_OVER_SONET_SDH"></span>透過 **SONET/SDH** (171) 的封包
</dt> <dt>

<span id="DVB-ASI_Input"></span><span id="dvb-asi_input"></span><span id="DVB-ASI_INPUT"></span>**ASI 輸入** (172) 
</dt> <dt>

<span id="DVB-ASI_Output"></span><span id="dvb-asi_output"></span><span id="DVB-ASI_OUTPUT"></span>**ASI 輸出** (173) 
</dt> <dt>

<span id="Power_Line"></span><span id="power_line"></span><span id="POWER_LINE"></span>**電源線** (174) 
</dt> <dt>

<span id="Non_Facility_Associated_Signaling"></span><span id="non_facility_associated_signaling"></span><span id="NON_FACILITY_ASSOCIATED_SIGNALING"></span>**非設備相關信號** (175) 
</dt> <dt>

<span id="TR008"></span><span id="tr008"></span>**TR008** (176) 
</dt> <dt>

<span id="GR303_RDT"></span><span id="gr303_rdt"></span>**GR303 RDT** (177) 
</dt> <dt>

<span id="GR303_IDT"></span><span id="gr303_idt"></span>**GR303 IDT** (178) 
</dt> <dt>

<span id="ISUP"></span><span id="isup"></span>**ISUP** (179) 
</dt> <dt>

<span id="Proprietary_Wireless_MAC_Layer"></span><span id="proprietary_wireless_mac_layer"></span><span id="PROPRIETARY_WIRELESS_MAC_LAYER"></span>**專屬的無線 MAC 層** (180) 
</dt> <dt>

<span id="Proprietary_Wireless_Downstream"></span><span id="proprietary_wireless_downstream"></span><span id="PROPRIETARY_WIRELESS_DOWNSTREAM"></span>**專屬無線下游** (181) 
</dt> <dt>

<span id="Proprietary_Wireless_Upstream"></span><span id="proprietary_wireless_upstream"></span><span id="PROPRIETARY_WIRELESS_UPSTREAM"></span>**專屬無線上游** (182) 
</dt> <dt>

<span id="HIPERLAN_Type_2"></span><span id="hiperlan_type_2"></span><span id="HIPERLAN_TYPE_2"></span>**HIPERLAN 類型 2** (183) 
</dt> <dt>

<span id="Proprietary_Broadband_Wireless_Access_Point_to_Multipoint"></span><span id="proprietary_broadband_wireless_access_point_to_multipoint"></span><span id="PROPRIETARY_BROADBAND_WIRELESS_ACCESS_POINT_TO_MULTIPOINT"></span>**Multipoint 的專用寬頻無線存取點** (184) 
</dt> <dt>

<span id="SONET_Overhead_Channel"></span><span id="sonet_overhead_channel"></span><span id="SONET_OVERHEAD_CHANNEL"></span>**SONET 額外負荷通道** (185) 
</dt> <dt>

<span id="Digital_Wrapper_Overhead_Channel"></span><span id="digital_wrapper_overhead_channel"></span><span id="DIGITAL_WRAPPER_OVERHEAD_CHANNEL"></span>**數位包裝程式額外負荷通道** (186) 
</dt> <dt>

<span id="ATM_Adaptation_Layer_2"></span><span id="atm_adaptation_layer_2"></span><span id="ATM_ADAPTATION_LAYER_2"></span>**ATM 調適層 2** (187) 
</dt> <dt>

<span id="Radio_MAC"></span><span id="radio_mac"></span><span id="RADIO_MAC"></span>**無線電 MAC** (188) 
</dt> <dt>

<span id="ATM_Radio"></span><span id="atm_radio"></span><span id="ATM_RADIO"></span>**ATM 無線電** (189) 
</dt> <dt>

<span id="Inter_Machine_Trunk"></span><span id="inter_machine_trunk"></span><span id="INTER_MACHINE_TRUNK"></span>**電腦間主幹** (190) 
</dt> <dt>

<span id="MVL_DSL"></span><span id="mvl_dsl"></span>**MVL DSL** (191) 
</dt> <dt>

<span id="Long_Read_DSL"></span><span id="long_read_dsl"></span><span id="LONG_READ_DSL"></span>**Long READ DSL** (192) 
</dt> <dt>

<span id="Frame_Relay_DLCI_Endpoint"></span><span id="frame_relay_dlci_endpoint"></span><span id="FRAME_RELAY_DLCI_ENDPOINT"></span>**框架轉送 DLCI 端點** (193) 
</dt> <dt>

<span id="ATM_VCI_Endpoint"></span><span id="atm_vci_endpoint"></span><span id="ATM_VCI_ENDPOINT"></span>**ATM VCI 端點** (194) 
</dt> <dt>

<span id="Optical_Channel"></span><span id="optical_channel"></span><span id="OPTICAL_CHANNEL"></span>**光學通道** (195) 
</dt> <dt>

<span id="Optical_Transport"></span><span id="optical_transport"></span><span id="OPTICAL_TRANSPORT"></span>**光學傳輸** (196) 
</dt> <dt>

<span id="Proprietary_ATM"></span><span id="proprietary_atm"></span><span id="PROPRIETARY_ATM"></span>**專屬的 ATM** (197) 
</dt> <dt>

<span id="Voice_over_Cable"></span><span id="voice_over_cable"></span><span id="VOICE_OVER_CABLE"></span>**語音 Over 纜線** (198) 
</dt> <dt>

<span id="Infiniband"></span><span id="infiniband"></span><span id="INFINIBAND"></span>**(199**) 的不限
</dt> <dt>

<span id="TE_Link"></span><span id="te_link"></span><span id="TE_LINK"></span>**連結** (200) 
</dt> <dt>

<span id="Q.2931"></span><span id="q.2931"></span>**2931** (201) 
</dt> <dt>

<span id="Virtual_Trunk_Group"></span><span id="virtual_trunk_group"></span><span id="VIRTUAL_TRUNK_GROUP"></span>**虛擬主幹群組** (202) 
</dt> <dt>

<span id="SIP_Trunk_Group"></span><span id="sip_trunk_group"></span><span id="SIP_TRUNK_GROUP"></span>**SIP 主幹群組** (203) 
</dt> <dt>

<span id="SIP_Signaling"></span><span id="sip_signaling"></span><span id="SIP_SIGNALING"></span>**SIP 信號** (204) 
</dt> <dt>

<span id="CATV_Upstream_Channel"></span><span id="catv_upstream_channel"></span><span id="CATV_UPSTREAM_CHANNEL"></span>**CATV 上游通道** (205) 
</dt> <dt>

<span id="Econet"></span><span id="econet"></span><span id="ECONET"></span>**Econet** (206) 
</dt> <dt>

<span id="FSAN_155Mb_PON"></span><span id="fsan_155mb_pon"></span><span id="FSAN_155MB_PON"></span>**FSAN 155MB PON** (207) 
</dt> <dt>

<span id="FSAN_622Mb_PON"></span><span id="fsan_622mb_pon"></span><span id="FSAN_622MB_PON"></span>**FSAN 622MB PON** (208) 
</dt> <dt>

<span id="Transparent_Bridge"></span><span id="transparent_bridge"></span><span id="TRANSPARENT_BRIDGE"></span>**透明橋接器** (209) 
</dt> <dt>

<span id="Line_Group"></span><span id="line_group"></span><span id="LINE_GROUP"></span>**行群組** (210) 
</dt> <dt>

<span id="Voice___Feature_Group"></span><span id="voice___feature_group"></span><span id="VOICE___FEATURE_GROUP"></span>**語音 & 功能群組** (211) 
</dt> <dt>

<span id="Voice_FGD_EANA"></span><span id="voice_fgd_eana"></span><span id="VOICE_FGD_EANA"></span>**VOICE FGD EANA** (212) 
</dt> <dt>

<span id="Voice_DID"></span><span id="voice_did"></span><span id="VOICE_DID"></span>**語音** (213) 
</dt> <dt>

<span id="MPEG_Transport"></span><span id="mpeg_transport"></span><span id="MPEG_TRANSPORT"></span>**MPEG 傳輸** (214) 
</dt> <dt>

<span id="6To4"></span><span id="6to4"></span><span id="6TO4"></span>**6to4** (215) 
</dt> <dt>

<span id="GTP"></span><span id="gtp"></span>**GTP** (216) 
</dt> <dt>

<span id="Paradyne_EtherLoop_1"></span><span id="paradyne_etherloop_1"></span><span id="PARADYNE_ETHERLOOP_1"></span>**Paradyne EtherLoop 1** (217) 
</dt> <dt>

<span id="Paradyne_EtherLoop_2"></span><span id="paradyne_etherloop_2"></span><span id="PARADYNE_ETHERLOOP_2"></span>**Paradyne EtherLoop 2** (218) 
</dt> <dt>

<span id="Optical_Channel_Group"></span><span id="optical_channel_group"></span><span id="OPTICAL_CHANNEL_GROUP"></span>**光學通道群組** (219) 
</dt> <dt>

<span id="HomePNA"></span><span id="homepna"></span><span id="HOMEPNA"></span>**HomePNA** (220) 
</dt> <dt>

<span id="GFP"></span><span id="gfp"></span>**GFP** (221) 
</dt> <dt>

<span id="ciscoISLvlan"></span><span id="ciscoislvlan"></span><span id="CISCOISLVLAN"></span>**ciscoISLvlan** (222) 
</dt> <dt>

<span id="actelisMetaLOOP"></span><span id="actelismetaloop"></span><span id="ACTELISMETALOOP"></span>**actelisMetaLOOP** (223) 
</dt> <dt>

<span id="Fcip"></span><span id="fcip"></span><span id="FCIP"></span>**Fcip** (224) 
</dt> <dt>

<span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>**IANA 保留** (225. 4095) 
</dt> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>**IPv4** (4096) 
</dt> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>**IPv6** (4097) 
</dt> <dt>

<span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>**IPv4/v6** (4098) 
</dt> <dt>

<span id="IPX"></span><span id="ipx"></span>**IPX** (4099) 
</dt> <dt>

<span id="DECnet"></span><span id="decnet"></span><span id="DECNET"></span>**DECnet** (4100) 
</dt> <dt>

<span id="SNA"></span><span id="sna"></span>**SNA** (4101) 
</dt> <dt>

<span id="CONP"></span><span id="conp"></span>**CONP** (4102) 
</dt> <dt>

<span id="CLNP"></span><span id="clnp"></span>**CLNP** (4103) 
</dt> <dt>

<span id="VINES"></span><span id="vines"></span>**VINES** (4104) 
</dt> <dt>

<span id="XNS"></span><span id="xns"></span>**XNS** (4105) 
</dt> <dt>

<span id="ISDN_B_Channel_Endpoint"></span><span id="isdn_b_channel_endpoint"></span><span id="ISDN_B_CHANNEL_ENDPOINT"></span>**ISDN B 通道端點** (4106) 
</dt> <dt>

<span id="ISDN_D_Channel_Endpoint"></span><span id="isdn_d_channel_endpoint"></span><span id="ISDN_D_CHANNEL_ENDPOINT"></span>**ISDN 資料通道端點** (4107) 
</dt> <dt>

<span id="BGP"></span><span id="bgp"></span>**BGP** (4108) 
</dt> <dt>

<span id="OSPF"></span><span id="ospf"></span>**OSPF** (4109) 
</dt> <dt>

<span id="UDP"></span><span id="udp"></span>**UDP** (4110) 
</dt> <dt>

<span id="TCP"></span><span id="tcp"></span>**TCP** (4111) 
</dt> <dt>

<span id="802.11a"></span><span id="802.11A"></span>**802.11 a** (4112) 
</dt> <dt>

<span id="802.11b"></span><span id="802.11B"></span>**802.11 b** (4113) 
</dt> <dt>

<span id="802.11g"></span><span id="802.11G"></span>**802.11 g** (4114) 
</dt> <dt>

<span id="802.11h"></span><span id="802.11H"></span>**802.11 h** (4115) 
</dt> <dt>

<span id="NFS"></span><span id="nfs"></span>**NFS** (4200) 
</dt> <dt>

<span id="CIFS"></span><span id="cifs"></span>**CIFS** (4201) 
</dt> <dt>

<span id="DAFS"></span><span id="dafs"></span>**DAFS** (4202) 
</dt> <dt>

<span id="WebDAV"></span><span id="webdav"></span><span id="WEBDAV"></span>**WebDAV** (4203) 
</dt> <dt>

<span id="HTTP"></span><span id="http"></span>**HTTP** (4204) 
</dt> <dt>

<span id="FTP"></span><span id="ftp"></span>**FTP** (4205) 
</dt> <dt>

<span id="NDMP"></span><span id="ndmp"></span>**NDMP** (4300) 
</dt> <dt>

<span id="Telnet"></span><span id="telnet"></span><span id="TELNET"></span>**Telnet** (4400) 
</dt> <dt>

<span id="SSH"></span><span id="ssh"></span>**SSH** (4401) 
</dt> <dt>

<span id="SM_CLP"></span><span id="sm_clp"></span>**SM CLP** (4402) 
</dt> <dt>

<span id="SMTP"></span><span id="smtp"></span>**SMTP** (4403) 
</dt> <dt>

<span id="LDAP"></span><span id="ldap"></span>**LDAP** (4404) 
</dt> <dt>

<span id="RDP"></span><span id="rdp"></span>**RDP** (4405) 
</dt> <dt>

<span id="HTTPS"></span><span id="https"></span>**HTTPS** (4406) 
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) 
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (32768。 )
</dt> </dl>

</dd> <dt>

**ProtocolType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性已被取代，代替 **ProtocolIFType** 屬性。 這個屬性繼承自 [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)。

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

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

裝載系統的建立類別名稱。 這個屬性繼承自 [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)。

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **Key**、 **MaxLen** ( 256 ) 
</dt> </dl>

主控系統的名稱。 這個屬性繼承自 [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)。

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

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 


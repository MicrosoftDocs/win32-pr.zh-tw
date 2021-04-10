---
description: 代表網路介面卡的邏輯連接點。 當 Wi-Fi 端點連線到交換器埠時，連接到 Wi-Fi 端點的網路介面卡具有網路連線能力。
ms.assetid: 66ed1503-9c11-4a51-a3a5-21e5d7021197
title: Msvm_WiFiEndpoint 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_WiFiEndpoint
- Msvm_WiFiEndpoint.RequestStateChange
- Msvm_WiFiEndpoint.InstanceID
- Msvm_WiFiEndpoint.Caption
- Msvm_WiFiEndpoint.Description
- Msvm_WiFiEndpoint.ElementName
- Msvm_WiFiEndpoint.InstallDate
- Msvm_WiFiEndpoint.Name
- Msvm_WiFiEndpoint.OperationalStatus
- Msvm_WiFiEndpoint.StatusDescriptions
- Msvm_WiFiEndpoint.Status
- Msvm_WiFiEndpoint.HealthState
- Msvm_WiFiEndpoint.CommunicationStatus
- Msvm_WiFiEndpoint.DetailedStatus
- Msvm_WiFiEndpoint.OperatingStatus
- Msvm_WiFiEndpoint.PrimaryStatus
- Msvm_WiFiEndpoint.EnabledState
- Msvm_WiFiEndpoint.OtherEnabledState
- Msvm_WiFiEndpoint.RequestedState
- Msvm_WiFiEndpoint.EnabledDefault
- Msvm_WiFiEndpoint.TimeOfLastStateChange
- Msvm_WiFiEndpoint.AvailableRequestedStates
- Msvm_WiFiEndpoint.TransitioningToState
- Msvm_WiFiEndpoint.SystemCreationClassName
- Msvm_WiFiEndpoint.SystemName
- Msvm_WiFiEndpoint.CreationClassName
- Msvm_WiFiEndpoint.NameFormat
- Msvm_WiFiEndpoint.ProtocolType
- Msvm_WiFiEndpoint.ProtocolIFType
- Msvm_WiFiEndpoint.OtherTypeDescription
- Msvm_WiFiEndpoint.LANID
- Msvm_WiFiEndpoint.LANType
- Msvm_WiFiEndpoint.OtherLANType
- Msvm_WiFiEndpoint.MACAddress
- Msvm_WiFiEndpoint.AliasAddresses
- Msvm_WiFiEndpoint.GroupAddresses
- Msvm_WiFiEndpoint.MaxDataSize
- Msvm_WiFiEndpoint.Connected
- Msvm_WiFiEndpoint.EncryptionMethod
- Msvm_WiFiEndpoint.OtherEncryptionMethod
- Msvm_WiFiEndpoint.AuthenticationMethod
- Msvm_WiFiEndpoint.OtherAuthenticationMethod
- Msvm_WiFiEndpoint.IEEE8021xAuthenticationProtocol
- Msvm_WiFiEndpoint.AccessPointAddress
- Msvm_WiFiEndpoint.BSSType
- Msvm_WiFiEndpoint.Associated
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f4a0a287d85b7a229b0e8e50a10c402fca734429
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943385"
---
# <a name="msvm_wifiendpoint-class"></a><span data-ttu-id="a1823-104">Msvm \_ WiFiEndpoint 類別</span><span class="sxs-lookup"><span data-stu-id="a1823-104">Msvm\_WiFiEndpoint class</span></span>

<span data-ttu-id="a1823-105">代表網路介面卡的邏輯連接點。</span><span class="sxs-lookup"><span data-stu-id="a1823-105">Represents the logical connection point for a network adapter.</span></span> <span data-ttu-id="a1823-106">當 Wi-Fi 端點連線到交換器埠時，連接到 Wi-Fi 端點的網路介面卡具有網路連線能力。</span><span class="sxs-lookup"><span data-stu-id="a1823-106">When the Wi-Fi endpoint is connected to a switch port, the network adapter connected to the Wi-Fi endpoint has network connectivity.</span></span>

<span data-ttu-id="a1823-107">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a1823-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1823-108">語法</span><span class="sxs-lookup"><span data-stu-id="a1823-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_WiFiEndpoint : CIM_WiFiEndpoint
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
  string   NameFormat;
  uint16   ProtocolType;
  uint16   ProtocolIFType = 71;
  string   OtherTypeDescription;
  string   LANID;
  uint16   LANType;
  string   OtherLANType;
  string   MACAddress;
  string   AliasAddresses[];
  string   GroupAddresses[];
  uint32   MaxDataSize;
  boolean  Connected;
  uint16   EncryptionMethod;
  string   OtherEncryptionMethod;
  uint16   AuthenticationMethod;
  string   OtherAuthenticationMethod;
  uint16   IEEE8021xAuthenticationProtocol;
  string   AccessPointAddress;
  uint16   BSSType;
  boolean  Associated;
};
```

## <a name="members"></a><span data-ttu-id="a1823-109">成員</span><span class="sxs-lookup"><span data-stu-id="a1823-109">Members</span></span>

<span data-ttu-id="a1823-110">**Msvm \_ WiFiEndpoint** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a1823-110">The **Msvm\_WiFiEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="a1823-111">方法</span><span class="sxs-lookup"><span data-stu-id="a1823-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="a1823-112">屬性</span><span class="sxs-lookup"><span data-stu-id="a1823-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a1823-113">方法</span><span class="sxs-lookup"><span data-stu-id="a1823-113">Methods</span></span>

<span data-ttu-id="a1823-114">**Msvm \_ WiFiEndpoint** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="a1823-114">The **Msvm\_WiFiEndpoint** class has these methods.</span></span>



| <span data-ttu-id="a1823-115">方法</span><span class="sxs-lookup"><span data-stu-id="a1823-115">Method</span></span>                 | <span data-ttu-id="a1823-116">描述</span><span class="sxs-lookup"><span data-stu-id="a1823-116">Description</span></span>                              |
|:-----------------------|:-----------------------------------------|
| <span data-ttu-id="a1823-117">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="a1823-117">**RequestStateChange**</span></span> | <span data-ttu-id="a1823-118">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="a1823-118">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a1823-119">屬性</span><span class="sxs-lookup"><span data-stu-id="a1823-119">Properties</span></span>

<span data-ttu-id="a1823-120">**Msvm \_ WiFiEndpoint** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a1823-120">The **Msvm\_WiFiEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a1823-121">**AccessPointAddress**</span><span class="sxs-lookup"><span data-stu-id="a1823-121">**AccessPointAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a1823-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1823-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1823-124">包含目前與 Wi-Fi 端點相關聯之存取點的 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="a1823-124">Contains the MAC address of the access point with which the Wi-Fi endpoint is currently associated.</span></span> <span data-ttu-id="a1823-125">如果 Wi-Fi 端點目前沒有相關聯，則 **AccessPointAddress** 應該是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a1823-125">If the Wi-Fi endpoint is not currently associated, then **AccessPointAddress** should be **Null**.</span></span> <span data-ttu-id="a1823-126">MAC 位址的格式應為12個十六進位數位 (例如 "010203040506" ) ，每一組代表以標準位 (順序表示之 MAC 位址的六個八位八位組中的其中一個（例如，在字串) 的第一個字元的低序位位中找到群組位址位）。</span><span class="sxs-lookup"><span data-stu-id="a1823-126">The MAC address should be formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order (for example, the Group address bit is found in the low order bit of the first character of the string).</span></span>

</dd> <dt>

<span data-ttu-id="a1823-127">**AliasAddresses**</span><span class="sxs-lookup"><span data-stu-id="a1823-127">**AliasAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-128">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="a1823-128">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a1823-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1823-130">可能用來與 LAN 端點通訊的其他單播位址。</span><span class="sxs-lookup"><span data-stu-id="a1823-130">Other unicast addresses that may be used to communicate with the LAN endpoint.</span></span> <span data-ttu-id="a1823-131">這個屬性繼承自 [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="a1823-131">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a1823-132">**相關聯**</span><span class="sxs-lookup"><span data-stu-id="a1823-132">**Associated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-133">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a1823-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a1823-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1823-135">指出 Wi-Fi 端點目前是否與存取點或用戶端相關聯。</span><span class="sxs-lookup"><span data-stu-id="a1823-135">Indicates whether the Wi-Fi endpoint is currently associated to an access point or client station.</span></span>

<span data-ttu-id="a1823-136">如果 Wi-Fi 端點與存取點或用戶端工作站相關聯，則會包含 **True** ;否則 **為 False**。</span><span class="sxs-lookup"><span data-stu-id="a1823-136">Contains **True** if the Wi-Fi endpoint is associated to an access point or client station; otherwise, **False**.</span></span>

</dd> <dt>

<span data-ttu-id="a1823-137">**AuthenticationMethod**</span><span class="sxs-lookup"><span data-stu-id="a1823-137">**AuthenticationMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-138">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a1823-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1823-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1823-140">指定用來驗證 Wi-Fi 端點和網路彼此的方法。</span><span class="sxs-lookup"><span data-stu-id="a1823-140">Specifies the method used to authenticate the Wi-Fi endpoint and the network to one another.</span></span>

<dl> <dt>

<span data-ttu-id="a1823-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="a1823-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-142"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="a1823-142"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-143"><span id="Open_System"></span><span id="open_system"></span><span id="OPEN_SYSTEM"></span>**開啟 System** (2) </span><span class="sxs-lookup"><span data-stu-id="a1823-143"><span id="Open_System"></span><span id="open_system"></span><span id="OPEN_SYSTEM"></span>**Open System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-144"><span id="Shared_Key"></span><span id="shared_key"></span><span id="SHARED_KEY"></span>**共用金鑰** (3) </span><span class="sxs-lookup"><span data-stu-id="a1823-144"><span id="Shared_Key"></span><span id="shared_key"></span><span id="SHARED_KEY"></span>**Shared Key** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-145"><span id="WPA_PSK"></span><span id="wpa_psk"></span>**WPA PSK** (4) </span><span class="sxs-lookup"><span data-stu-id="a1823-145"><span id="WPA_PSK"></span><span id="wpa_psk"></span>**WPA PSK** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-146"><span id="WPA_IEEE_802.1x"></span><span id="wpa_ieee_802.1x"></span><span id="WPA_IEEE_802.1X"></span>**WPA IEEE 802.1 x** (5) </span><span class="sxs-lookup"><span data-stu-id="a1823-146"><span id="WPA_IEEE_802.1x"></span><span id="wpa_ieee_802.1x"></span><span id="WPA_IEEE_802.1X"></span>**WPA IEEE 802.1x** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-147"><span id="WPA2_PSK"></span><span id="wpa2_psk"></span>**WPA2 PSK** (6) </span><span class="sxs-lookup"><span data-stu-id="a1823-147"><span id="WPA2_PSK"></span><span id="wpa2_psk"></span>**WPA2 PSK** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-148"><span id="WPA2_IEEE_802.1x"></span><span id="wpa2_ieee_802.1x"></span><span id="WPA2_IEEE_802.1X"></span>**WPA2 IEEE 802.1 x** (7) </span><span class="sxs-lookup"><span data-stu-id="a1823-148"><span id="WPA2_IEEE_802.1x"></span><span id="wpa2_ieee_802.1x"></span><span id="WPA2_IEEE_802.1X"></span>**WPA2 IEEE 802.1x** (7)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-149"><span id="CCKM_IEEE_802.1x"></span><span id="cckm_ieee_802.1x"></span><span id="CCKM_IEEE_802.1X"></span>**CCKM IEEE 802.1 x** (8) </span><span class="sxs-lookup"><span data-stu-id="a1823-149"><span id="CCKM_IEEE_802.1x"></span><span id="cckm_ieee_802.1x"></span><span id="CCKM_IEEE_802.1X"></span>**CCKM IEEE 802.1x** (8)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-150"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF 保留** (9。</span><span class="sxs-lookup"><span data-stu-id="a1823-150"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (9..</span></span> <span data-ttu-id="a1823-151">)</span><span class="sxs-lookup"><span data-stu-id="a1823-151">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a1823-152">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="a1823-152">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-153">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="a1823-153">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a1823-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1823-155">指出用於起始狀態變更之 [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement)方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="a1823-155">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="a1823-156">列出的值將會是與 **cim \_ EnabledLogicalElementCapabilities** 相關聯的實例之 **RequestedStatesSupported** 屬性中所含值的子集，其中選取的值是 [**cim \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))目前狀態的函式。</span><span class="sxs-lookup"><span data-stu-id="a1823-156">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="a1823-157">如果實作為目前狀態的函式，則這個屬性可以是非 **Null** 的值。</span><span class="sxs-lookup"><span data-stu-id="a1823-157">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="a1823-158">如果實作為目前狀態的函式無法判斷可能的值集，這個屬性將會是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="a1823-158">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="a1823-159">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="a1823-159">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="a1823-160"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="a1823-160"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-161"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="a1823-161"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-162"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**關機** (4) </span><span class="sxs-lookup"><span data-stu-id="a1823-162"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-163"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**離線** (6) </span><span class="sxs-lookup"><span data-stu-id="a1823-163"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-164"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**測試** (7) </span><span class="sxs-lookup"><span data-stu-id="a1823-164"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-165"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**延** 後 (8) </span><span class="sxs-lookup"><span data-stu-id="a1823-165"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-166"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**靜止** (9) </span><span class="sxs-lookup"><span data-stu-id="a1823-166"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-167"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**重新開機** (10) </span><span class="sxs-lookup"><span data-stu-id="a1823-167"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-168"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**重設** (11) </span><span class="sxs-lookup"><span data-stu-id="a1823-168"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-169"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF 保留** ( .。。</span><span class="sxs-lookup"><span data-stu-id="a1823-169"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="a1823-170">)</span><span class="sxs-lookup"><span data-stu-id="a1823-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a1823-171">**BSSType**</span><span class="sxs-lookup"><span data-stu-id="a1823-171">**BSSType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-172">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a1823-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1823-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1823-174">指出對應至實例之網路的基本服務集 (BSS) 類型。</span><span class="sxs-lookup"><span data-stu-id="a1823-174">Indicates the Basic Service Set (BSS) type of the network that corresponds to the instance.</span></span> <span data-ttu-id="a1823-175">基本服務集是由單一協調功能所控制的一組工作站。</span><span class="sxs-lookup"><span data-stu-id="a1823-175">A Basic Service Set is a set of stations controlled by a single coordination function.</span></span>



| <span data-ttu-id="a1823-176">值</span><span class="sxs-lookup"><span data-stu-id="a1823-176">Value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="a1823-177">意義</span><span class="sxs-lookup"><span data-stu-id="a1823-177">Meaning</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="a1823-178"><dt>**未知**</dt>的 <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a1823-178"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                |                                                                                    |
| <span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span><dl> <span data-ttu-id="a1823-179"><dt>**獨立**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a1823-179"><dt>**Independent**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="a1823-180">Wi-Fi 端點會直接關聯至另一個用戶端工作站。</span><span class="sxs-lookup"><span data-stu-id="a1823-180">The Wi-Fi endpoint is associated directly to another client station.</span></span><br/>    |
| <span id="Infrastructure"></span><span id="infrastructure"></span><span id="INFRASTRUCTURE"></span><dl> <span data-ttu-id="a1823-181"><dt>**基礎結構**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="a1823-181"><dt>**Infrastructure**</dt> <dt>3</dt></span></span> </dl>    | <span data-ttu-id="a1823-182">Wi-Fi 端點會使用存取點與網路相關聯。</span><span class="sxs-lookup"><span data-stu-id="a1823-182">The Wi-Fi endpoint is associated to a network by using an access point.</span></span><br/> |
| <span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span><dl> <span data-ttu-id="a1823-183"><dt> **DMTF 保留**</dt> <dt>4。</dt></span><span class="sxs-lookup"><span data-stu-id="a1823-183"><dt>**DMTF Reserved** </dt> <dt>4.. </dt></span></span> </dl> |                                                                                    |



 

</dd> <dt>

<span data-ttu-id="a1823-184">**標題**</span><span class="sxs-lookup"><span data-stu-id="a1823-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-185">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a1823-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1823-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1823-187">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="a1823-187">A short description of the object.</span></span> <span data-ttu-id="a1823-188">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="a1823-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a1823-189">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="a1823-189">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-190">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a1823-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1823-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1823-192">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="a1823-192">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="a1823-193">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="a1823-193">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a1823-194">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="a1823-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a1823-195">**已連接**</span><span class="sxs-lookup"><span data-stu-id="a1823-195">**Connected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-196">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a1823-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a1823-197">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1823-198">如果 Wi-Fi 端點連接到交換器埠，這個屬性會設定為 **True** 。</span><span class="sxs-lookup"><span data-stu-id="a1823-198">This property is set to **True** if the Wi-Fi endpoint is connected to a switch port.</span></span>

</dd> <dt>

<span data-ttu-id="a1823-199">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a1823-199">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-200">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a1823-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1823-201">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1823-202">限定詞： **Key**、 **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="a1823-202">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="a1823-203">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1823-203">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="a1823-204">這個屬性繼承自 [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)。</span><span class="sxs-lookup"><span data-stu-id="a1823-204">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="a1823-205">**說明**</span><span class="sxs-lookup"><span data-stu-id="a1823-205">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-206">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a1823-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1823-207">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1823-208">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="a1823-208">A description of the object.</span></span> <span data-ttu-id="a1823-209">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="a1823-209">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a1823-210">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="a1823-210">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-211">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a1823-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1823-212">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1823-213">補充具有其他狀態詳細資料的 **PrimaryStatus** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a1823-213">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="a1823-214">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="a1823-214">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a1823-215">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="a1823-215">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a1823-216">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="a1823-216">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-217">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a1823-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1823-218">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1823-219">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="a1823-219">A display name for the object.</span></span> <span data-ttu-id="a1823-220">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="a1823-220">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a1823-221">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="a1823-221">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-222">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a1823-222">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1823-223">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1823-224">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="a1823-224">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="a1823-225">這個屬性會繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) ，而且會是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a1823-225">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a1823-226"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="a1823-226"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-227"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="a1823-227"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-228"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**已啟用但離線** (6) </span><span class="sxs-lookup"><span data-stu-id="a1823-228"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a1823-229">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="a1823-229">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-230">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a1823-230">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1823-231">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1823-232">指定已規劃系統的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="a1823-232">Specifies the enabled state of the planned system.</span></span> <span data-ttu-id="a1823-233">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，它可以是下列值之一。</span><span class="sxs-lookup"><span data-stu-id="a1823-233">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it can be one of the following values.</span></span>



| <span data-ttu-id="a1823-234">值</span><span class="sxs-lookup"><span data-stu-id="a1823-234">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="a1823-235">意義</span><span class="sxs-lookup"><span data-stu-id="a1823-235">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="a1823-236"><dt>**停用**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="a1823-236"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="a1823-237">系統已關閉。</span><span class="sxs-lookup"><span data-stu-id="a1823-237">The system is turned off.</span></span><br/>                                             |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="a1823-238"><dt>**不適用**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="a1823-238"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="a1823-239">元素不支援啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="a1823-239">The element does not support being enabled or disabled.</span></span><br/>               |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="a1823-240"><dt>**已啟用但離線**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="a1823-240"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="a1823-241">系統已啟用但離線。</span><span class="sxs-lookup"><span data-stu-id="a1823-241">The system is enabled, but offline.</span></span> <span data-ttu-id="a1823-242">將會捨棄任何新的要求。</span><span class="sxs-lookup"><span data-stu-id="a1823-242">Any new requests will be dropped.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a1823-243">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="a1823-243">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-244">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a1823-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1823-245">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1823-246">指定用來保護 Wi-Fi 端點所傳送和接收之資料機密性的加密方法。</span><span class="sxs-lookup"><span data-stu-id="a1823-246">Specifies the encryption method in use to protect the confidentiality of data sent and received by the Wi-Fi endpoint.</span></span>

<dl> <dt>

<span data-ttu-id="a1823-247"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="a1823-247"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-248"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="a1823-248"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-249"><span id="WEP"></span><span id="wep"></span>**WEP** (2) </span><span class="sxs-lookup"><span data-stu-id="a1823-249"><span id="WEP"></span><span id="wep"></span>**WEP** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-250"><span id="TKIP"></span><span id="tkip"></span>**TKIP** (3) </span><span class="sxs-lookup"><span data-stu-id="a1823-250"><span id="TKIP"></span><span id="tkip"></span>**TKIP** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-251"><span id="CCMP"></span><span id="ccmp"></span>**CCMP** (4) </span><span class="sxs-lookup"><span data-stu-id="a1823-251"><span id="CCMP"></span><span id="ccmp"></span>**CCMP** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-252"><span id="None"></span><span id="none"></span><span id="NONE"></span>**無** (5) </span><span class="sxs-lookup"><span data-stu-id="a1823-252"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-253"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF 保留** (6。</span><span class="sxs-lookup"><span data-stu-id="a1823-253"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (6..</span></span> <span data-ttu-id="a1823-254">)</span><span class="sxs-lookup"><span data-stu-id="a1823-254">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a1823-255">**GroupAddresses**</span><span class="sxs-lookup"><span data-stu-id="a1823-255">**GroupAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-256">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="a1823-256">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a1823-257">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1823-258">LAN 端點接聽的多播位址。</span><span class="sxs-lookup"><span data-stu-id="a1823-258">Multicast addresses to which the LAN endpoint listens.</span></span> <span data-ttu-id="a1823-259">這個屬性繼承自 [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="a1823-259">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a1823-260">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="a1823-260">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-261">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a1823-261">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1823-262">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1823-263">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="a1823-263">The current health of the element.</span></span> <span data-ttu-id="a1823-264">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="a1823-264">This property expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="a1823-265">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="a1823-265">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="a1823-266">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="a1823-266">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a1823-267">**IEEE8021xAuthenticationProtocol**</span><span class="sxs-lookup"><span data-stu-id="a1823-267">**IEEE8021xAuthenticationProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-268">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a1823-268">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1823-269">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1823-270">包含可延伸的驗證通訊協定 (EAP) 類型，只有在 **AuthenticationMethod** 包含 5 (WPA ieee 802.1 x) 、7 (WPA2 ieee 802.1 x) 或 8 (CCKM ieee 802.1 x) 時才適用。</span><span class="sxs-lookup"><span data-stu-id="a1823-270">Contains the Extensible Authentication Protocol (EAP) type if and only if **AuthenticationMethod** contains 5 (WPA IEEE 802.1x), 7 (WPA2 IEEE 802.1x), or 8 (CCKM IEEE 802.1x).</span></span>

<dl> <dt>

<span data-ttu-id="a1823-271"><span id="EAP-TLS"></span><span id="eap-tls"></span>**Eap-tls** (0) </span><span class="sxs-lookup"><span data-stu-id="a1823-271"><span id="EAP-TLS"></span><span id="eap-tls"></span>**EAP-TLS** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-272"><span id="EAP-TTLS_MSCHAPv2"></span><span id="eap-ttls_mschapv2"></span><span id="EAP-TTLS_MSCHAPV2"></span>**EAP-TTLS/eap-mschapv2** (1) </span><span class="sxs-lookup"><span data-stu-id="a1823-272"><span id="EAP-TTLS_MSCHAPv2"></span><span id="eap-ttls_mschapv2"></span><span id="EAP-TTLS_MSCHAPV2"></span>**EAP-TTLS/MSCHAPv2** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-273"><span id="PEAPv0_EAP-MSCHAPv2"></span><span id="peapv0_eap-mschapv2"></span><span id="PEAPV0_EAP-MSCHAPV2"></span>**PEAPv0/EAP-eap-mschapv2** (2) </span><span class="sxs-lookup"><span data-stu-id="a1823-273"><span id="PEAPv0_EAP-MSCHAPv2"></span><span id="peapv0_eap-mschapv2"></span><span id="PEAPV0_EAP-MSCHAPV2"></span>**PEAPv0/EAP-MSCHAPv2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-274"><span id="PEAPv1_EAP-GTC"></span><span id="peapv1_eap-gtc"></span><span id="PEAPV1_EAP-GTC"></span>**PEAPv1/EAP-GTC** (3) </span><span class="sxs-lookup"><span data-stu-id="a1823-274"><span id="PEAPv1_EAP-GTC"></span><span id="peapv1_eap-gtc"></span><span id="PEAPV1_EAP-GTC"></span>**PEAPv1/EAP-GTC** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-275"><span id="EAP-FAST_MSCHAPv2"></span><span id="eap-fast_mschapv2"></span><span id="EAP-FAST_MSCHAPV2"></span>**Eap-fast/eap-mschapv2** (4) </span><span class="sxs-lookup"><span data-stu-id="a1823-275"><span id="EAP-FAST_MSCHAPv2"></span><span id="eap-fast_mschapv2"></span><span id="EAP-FAST_MSCHAPV2"></span>**EAP-FAST/MSCHAPv2** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-276"><span id="EAP-FAST_GTC"></span><span id="eap-fast_gtc"></span>**Eap-fast/GTC** (5) </span><span class="sxs-lookup"><span data-stu-id="a1823-276"><span id="EAP-FAST_GTC"></span><span id="eap-fast_gtc"></span>**EAP-FAST/GTC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-277"><span id="EAP-MD5"></span><span id="eap-md5"></span>**EAP-MD5** (6) </span><span class="sxs-lookup"><span data-stu-id="a1823-277"><span id="EAP-MD5"></span><span id="eap-md5"></span>**EAP-MD5** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-278"><span id="EAP-PSK"></span><span id="eap-psk"></span>**Eap-tls** (7) </span><span class="sxs-lookup"><span data-stu-id="a1823-278"><span id="EAP-PSK"></span><span id="eap-psk"></span>**EAP-PSK** (7)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-279"><span id="EAP-SIM"></span><span id="eap-sim"></span>**EAP-SIM** (8) </span><span class="sxs-lookup"><span data-stu-id="a1823-279"><span id="EAP-SIM"></span><span id="eap-sim"></span>**EAP-SIM** (8)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-280"><span id="EAP-AKA"></span><span id="eap-aka"></span>**EAP-也稱為** (9) </span><span class="sxs-lookup"><span data-stu-id="a1823-280"><span id="EAP-AKA"></span><span id="eap-aka"></span>**EAP-AKA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-281"><span id="EAP-FAST_TLS"></span><span id="eap-fast_tls"></span>**Eap-fast/TLS** (10) </span><span class="sxs-lookup"><span data-stu-id="a1823-281"><span id="EAP-FAST_TLS"></span><span id="eap-fast_tls"></span>**EAP-FAST/TLS** (10)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-282"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF 保留** (11</span><span class="sxs-lookup"><span data-stu-id="a1823-282"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (11..</span></span> <span data-ttu-id="a1823-283">)</span><span class="sxs-lookup"><span data-stu-id="a1823-283">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a1823-284">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a1823-284">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-285">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="a1823-285">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a1823-286">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1823-287">建立虛擬機器設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="a1823-287">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="a1823-288">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="a1823-288">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a1823-289">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a1823-289">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-290">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a1823-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1823-291">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1823-292">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="a1823-292">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="a1823-293">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="a1823-293">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="a1823-294">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="a1823-294">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a1823-295">**LANID**</span><span class="sxs-lookup"><span data-stu-id="a1823-295">**LANID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-296">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a1823-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1823-297">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1823-298">端點所連接之 LAN 區段的標籤或識別碼。</span><span class="sxs-lookup"><span data-stu-id="a1823-298">A label or identifier for the LAN segment to which the endpoint is connected.</span></span> <span data-ttu-id="a1823-299">如果端點目前非使用中/已連線，或這項資訊未知，則這個屬性會是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a1823-299">If the endpoint is not currently active/connected, or this information is not known, then this property will be **Null**.</span></span> <span data-ttu-id="a1823-300">這個屬性繼承自 [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="a1823-300">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a1823-301">**LANType**</span><span class="sxs-lookup"><span data-stu-id="a1823-301">**LANType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-302">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a1823-302">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1823-303">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1823-304">這個屬性已被取代，代替 **ProtocolType** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a1823-304">This property is deprecated in lieu of the **ProtocolType** property.</span></span> <span data-ttu-id="a1823-305">這個屬性繼承自 [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="a1823-305">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a1823-306">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="a1823-306">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-307">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a1823-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1823-308">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1823-309">限定詞： **MaxLen** ( 12 ) </span><span class="sxs-lookup"><span data-stu-id="a1823-309">Qualifiers: **MaxLen** ( 12 )</span></span>
</dt> </dl>

<span data-ttu-id="a1823-310">與 LAN 端點通訊時使用的 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="a1823-310">The MAC address used in communication with the LAN endpoint.</span></span> <span data-ttu-id="a1823-311">MAC 位址的格式為十二個十六進位數位 (例如 "010203040506" ) ，其中每一組代表根據 RFC 2469 的標準位順序，其中一個 MAC 位址的六個八位。</span><span class="sxs-lookup"><span data-stu-id="a1823-311">The MAC address is formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order according to RFC 2469.</span></span> <span data-ttu-id="a1823-312">這個屬性繼承自 [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="a1823-312">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a1823-313">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="a1823-313">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-314">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a1823-314">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a1823-315">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1823-316">限定詞： **單位** ( "Bits" ) </span><span class="sxs-lookup"><span data-stu-id="a1823-316">Qualifiers: **Units** ("Bits")</span></span>
</dt> </dl>

<span data-ttu-id="a1823-317">LAN 端點可能傳送或接收之資訊欄位的最大大小（以位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="a1823-317">The largest size, in number of bits, of the information field that may be sent or received by the LAN endpoint.</span></span> <span data-ttu-id="a1823-318">這個屬性繼承自 [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="a1823-318">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a1823-319">**名稱**</span><span class="sxs-lookup"><span data-stu-id="a1823-319">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-320">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a1823-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1823-321">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1823-322">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="a1823-322">The label by which the object is known.</span></span> <span data-ttu-id="a1823-323">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="a1823-323">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a1823-324">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="a1823-324">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-325">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a1823-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1823-326">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1823-327">限定詞： **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="a1823-327">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="a1823-328">包含已選取的命名啟發式，以確保 **Name** 屬性的值是唯一的。</span><span class="sxs-lookup"><span data-stu-id="a1823-328">Contains the naming heuristic that is selected to ensure that the value of the **Name** property is unique.</span></span> <span data-ttu-id="a1823-329">這個屬性繼承自 [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)。</span><span class="sxs-lookup"><span data-stu-id="a1823-329">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="a1823-330">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="a1823-330">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-331">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a1823-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1823-332">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1823-333">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a1823-333">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="a1823-334">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="a1823-334">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a1823-335">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="a1823-335">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a1823-336">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="a1823-336">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-337">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="a1823-337">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a1823-338">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1823-339">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="a1823-339">The current statuses of the object.</span></span> <span data-ttu-id="a1823-340">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="a1823-340">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a1823-341">**OtherAuthenticationMethod**</span><span class="sxs-lookup"><span data-stu-id="a1823-341">**OtherAuthenticationMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-342">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a1823-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1823-343">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1823-344">只有當 **AuthenticationMethod** 包含 1 (其他) 時，才會指定802.11 驗證方法。</span><span class="sxs-lookup"><span data-stu-id="a1823-344">Specifies the 802.11 authentication method if and only if **AuthenticationMethod** contains 1 (Other).</span></span> <span data-ttu-id="a1823-345">此字串的格式為廠商專屬。</span><span class="sxs-lookup"><span data-stu-id="a1823-345">The format of this string is vendor specific.</span></span>

</dd> <dt>

<span data-ttu-id="a1823-346">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="a1823-346">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-347">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a1823-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1823-348">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1823-349">描述當 **EnabledState** 屬性設定為 1 ( "Other" ) 時，專案已啟用或停用狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="a1823-349">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="a1823-350">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="a1823-350">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="a1823-351">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="a1823-351">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a1823-352">**OtherEncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="a1823-352">**OtherEncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-353">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a1823-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1823-354">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1823-355">只有在 **EncryptionMethod** 包含 1 (其他) 時，才會指定802.11 加密方法。</span><span class="sxs-lookup"><span data-stu-id="a1823-355">Specifies the 802.11 encryption method if and only if **EncryptionMethod** contains 1 (Other).</span></span> <span data-ttu-id="a1823-356">此字串的格式為廠商專屬。</span><span class="sxs-lookup"><span data-stu-id="a1823-356">The format of this string is vendor specific.</span></span>

</dd> <dt>

<span data-ttu-id="a1823-357">**OtherLANType**</span><span class="sxs-lookup"><span data-stu-id="a1823-357">**OtherLANType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-358">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a1823-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1823-359">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1823-360">這個屬性已被取代，代替 **OtherTypeDescription** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a1823-360">This property is deprecated in lieu of the **OtherTypeDescription** property.</span></span> <span data-ttu-id="a1823-361">這個屬性繼承自 [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="a1823-361">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a1823-362">**OtherTypeDescription**</span><span class="sxs-lookup"><span data-stu-id="a1823-362">**OtherTypeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-363">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a1823-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1823-364">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1823-365">限定詞： **MaxLen** ( 64 ) </span><span class="sxs-lookup"><span data-stu-id="a1823-365">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="a1823-366">描述當這個類別的 **ProtocolIFType** 屬性 (或其任何子類別) 設定為 1 (其他) 時，通訊協定端點型別的字串。</span><span class="sxs-lookup"><span data-stu-id="a1823-366">A string that describes the type of protocol endpoint when the **ProtocolIFType** property of this class (or any of its subclasses) is set to 1 (Other).</span></span> <span data-ttu-id="a1823-367">當 **ProtocolIFType** 屬性是1以外的任何值時，這個屬性應該設為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="a1823-367">This property should be set to **Null** when the **ProtocolIFType** property is any value other than 1.</span></span> <span data-ttu-id="a1823-368">這個屬性繼承自 [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)。</span><span class="sxs-lookup"><span data-stu-id="a1823-368">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="a1823-369">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="a1823-369">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-370">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a1823-370">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1823-371">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1823-372">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="a1823-372">Provides high level status information.</span></span> <span data-ttu-id="a1823-373">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="a1823-373">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="a1823-374">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="a1823-374">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a1823-375">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="a1823-375">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a1823-376">**ProtocolIFType**</span><span class="sxs-lookup"><span data-stu-id="a1823-376">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-377">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a1823-377">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1823-378">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1823-379">屬性是用來分類和分類這個類別的實例。</span><span class="sxs-lookup"><span data-stu-id="a1823-379">The property is used to categorize and classify instances of this class.</span></span> <span data-ttu-id="a1823-380">如果 **ProtocolIFType** 設定為 1 (其他) ，則應該在 **OtherTypeDescription** 屬性中提供類型資訊。</span><span class="sxs-lookup"><span data-stu-id="a1823-380">If the **ProtocolIFType** is set to 1 (Other), then the type information should be provided in the **OtherTypeDescription** property.</span></span> <span data-ttu-id="a1823-381">這個屬性繼承自 [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)。</span><span class="sxs-lookup"><span data-stu-id="a1823-381">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

> [!Note]  
> <span data-ttu-id="a1823-382">**ProtocolIFType** 是與 [IANA ifType MIB](https://www.iana.org/assignments/ianaiftype-mib)同步的列舉。</span><span class="sxs-lookup"><span data-stu-id="a1823-382">**ProtocolIFType** is an enumeration that is synchronized with the [IANA ifType MIB](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <span data-ttu-id="a1823-383">也會包含其他以 DMTF 定義的值。</span><span class="sxs-lookup"><span data-stu-id="a1823-383">Additional values defined by the DMTF are also included.</span></span>

 

<dl> <dt>

<span data-ttu-id="a1823-384"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="a1823-384"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-385"><span id="IEEE_802.11"></span><span id="ieee_802.11"></span>**IEEE 802.11** (71) </span><span class="sxs-lookup"><span data-stu-id="a1823-385"><span id="IEEE_802.11"></span><span id="ieee_802.11"></span>**IEEE 802.11** (71)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-386"><span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>**IANA 保留** (225. 4095) </span><span class="sxs-lookup"><span data-stu-id="a1823-386"><span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>**IANA Reserved** (225..4095)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-387"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** 的 (a334-18f799d361d1. 32767) </span><span class="sxs-lookup"><span data-stu-id="a1823-387"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (4301..32767)</span></span>
</dt> <dt>

<span data-ttu-id="a1823-388"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (32768。</span><span class="sxs-lookup"><span data-stu-id="a1823-388"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32768..</span></span> <span data-ttu-id="a1823-389">)</span><span class="sxs-lookup"><span data-stu-id="a1823-389">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a1823-390">**ProtocolType**</span><span class="sxs-lookup"><span data-stu-id="a1823-390">**ProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-391">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a1823-391">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1823-392">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1823-393">這個屬性已被取代，代替 **ProtocolIFType** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a1823-393">This property is deprecated in lieu of the **ProtocolIFType** property.</span></span> <span data-ttu-id="a1823-394">這個屬性繼承自 [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)。</span><span class="sxs-lookup"><span data-stu-id="a1823-394">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="a1823-395">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="a1823-395">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-396">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a1823-396">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1823-397">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1823-398">上次要求或預期的管理服務狀態。</span><span class="sxs-lookup"><span data-stu-id="a1823-398">The last requested or desired state for the management service.</span></span> <span data-ttu-id="a1823-399">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="a1823-399">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a1823-400">**狀態**</span><span class="sxs-lookup"><span data-stu-id="a1823-400">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-401">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a1823-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1823-402">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1823-403">描述元素的狀態。</span><span class="sxs-lookup"><span data-stu-id="a1823-403">Describes the status of the element.</span></span> <span data-ttu-id="a1823-404">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="a1823-404">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="a1823-405">正常</span><span class="sxs-lookup"><span data-stu-id="a1823-405">"OK"</span></span>

<span data-ttu-id="a1823-406">錯誤</span><span class="sxs-lookup"><span data-stu-id="a1823-406">"Error"</span></span>

<span data-ttu-id="a1823-407">降級</span><span class="sxs-lookup"><span data-stu-id="a1823-407">"Degraded"</span></span>

<span data-ttu-id="a1823-408">不明</span><span class="sxs-lookup"><span data-stu-id="a1823-408">"Unknown"</span></span>

<span data-ttu-id="a1823-409">「Pred 失敗」</span><span class="sxs-lookup"><span data-stu-id="a1823-409">"Pred Fail"</span></span>

<span data-ttu-id="a1823-410">入門</span><span class="sxs-lookup"><span data-stu-id="a1823-410">"Starting"</span></span>

<span data-ttu-id="a1823-411">從而</span><span class="sxs-lookup"><span data-stu-id="a1823-411">"Stopping"</span></span>

<span data-ttu-id="a1823-412">維護</span><span class="sxs-lookup"><span data-stu-id="a1823-412">"Service"</span></span>

<span data-ttu-id="a1823-413">強調</span><span class="sxs-lookup"><span data-stu-id="a1823-413">"Stressed"</span></span>

<span data-ttu-id="a1823-414">"NonRecover"</span><span class="sxs-lookup"><span data-stu-id="a1823-414">"NonRecover"</span></span>

<span data-ttu-id="a1823-415">「無連絡人」</span><span class="sxs-lookup"><span data-stu-id="a1823-415">"No Contact"</span></span>

<span data-ttu-id="a1823-416">「遺失通訊」</span><span class="sxs-lookup"><span data-stu-id="a1823-416">"Lost Comm"</span></span>

</dd> <dt>

<span data-ttu-id="a1823-417">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="a1823-417">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-418">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="a1823-418">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a1823-419">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1823-420">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="a1823-420">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="a1823-421">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="a1823-421">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a1823-422">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a1823-422">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-423">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a1823-423">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1823-424">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-424">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1823-425">裝載系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="a1823-425">The hosting system's creation class name.</span></span> <span data-ttu-id="a1823-426">這個屬性繼承自 [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)。</span><span class="sxs-lookup"><span data-stu-id="a1823-426">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="a1823-427">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="a1823-427">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-428">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a1823-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1823-429">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1823-430">限定詞： **Key**、 **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="a1823-430">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="a1823-431">主控系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1823-431">The name of the hosting system.</span></span> <span data-ttu-id="a1823-432">這個屬性繼承自 [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)。</span><span class="sxs-lookup"><span data-stu-id="a1823-432">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="a1823-433">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="a1823-433">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-434">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="a1823-434">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a1823-435">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1823-436">專案的已啟用狀態上次變更的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="a1823-436">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="a1823-437">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="a1823-437">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a1823-438">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="a1823-438">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1823-439">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a1823-439">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1823-440">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1823-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1823-441">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="a1823-441">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="a1823-442">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="a1823-442">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a1823-443">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1823-443">Requirements</span></span>



| <span data-ttu-id="a1823-444">需求</span><span class="sxs-lookup"><span data-stu-id="a1823-444">Requirement</span></span> | <span data-ttu-id="a1823-445">值</span><span class="sxs-lookup"><span data-stu-id="a1823-445">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1823-446">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a1823-446">Minimum supported client</span></span><br/> | <span data-ttu-id="a1823-447">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a1823-447">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a1823-448">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a1823-448">Minimum supported server</span></span><br/> | <span data-ttu-id="a1823-449">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a1823-449">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a1823-450">命名空間</span><span class="sxs-lookup"><span data-stu-id="a1823-450">Namespace</span></span><br/>                | <span data-ttu-id="a1823-451">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="a1823-451">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a1823-452">MOF</span><span class="sxs-lookup"><span data-stu-id="a1823-452">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a1823-453"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="a1823-453"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a1823-454">DLL</span><span class="sxs-lookup"><span data-stu-id="a1823-454">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1823-455"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a1823-455"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


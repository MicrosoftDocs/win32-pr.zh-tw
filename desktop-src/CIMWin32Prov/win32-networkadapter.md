---
description: Win32 \_ NetworkAdapter 類別已被取代。 請改用 MSFT \_ get-netadapter 類別。 Win32 \_ NetworkAdapterWMI 類別代表執行 Windows 作業系統之電腦的網路介面卡。
ms.assetid: f79cb2a1-a249-479d-a495-37a44fdea995
ms.tgt_platform: multiple
title: Win32_NetworkAdapter 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapter
- Win32_NetworkAdapter.Reset
- Win32_NetworkAdapter.SetPowerState
- Win32_NetworkAdapter.AdapterType
- Win32_NetworkAdapter.AdapterTypeID
- Win32_NetworkAdapter.AutoSense
- Win32_NetworkAdapter.Availability
- Win32_NetworkAdapter.Caption
- Win32_NetworkAdapter.ConfigManagerErrorCode
- Win32_NetworkAdapter.ConfigManagerUserConfig
- Win32_NetworkAdapter.CreationClassName
- Win32_NetworkAdapter.Description
- Win32_NetworkAdapter.DeviceID
- Win32_NetworkAdapter.ErrorCleared
- Win32_NetworkAdapter.ErrorDescription
- Win32_NetworkAdapter.GUID
- Win32_NetworkAdapter.Index
- Win32_NetworkAdapter.InstallDate
- Win32_NetworkAdapter.Installed
- Win32_NetworkAdapter.InterfaceIndex
- Win32_NetworkAdapter.LastErrorCode
- Win32_NetworkAdapter.MACAddress
- Win32_NetworkAdapter.Manufacturer
- Win32_NetworkAdapter.MaxNumberControlled
- Win32_NetworkAdapter.MaxSpeed
- Win32_NetworkAdapter.Name
- Win32_NetworkAdapter.NetConnectionID
- Win32_NetworkAdapter.NetConnectionStatus
- Win32_NetworkAdapter.NetEnabled
- Win32_NetworkAdapter.NetworkAddresses
- Win32_NetworkAdapter.PermanentAddress
- Win32_NetworkAdapter.PhysicalAdapter
- Win32_NetworkAdapter.PNPDeviceID
- Win32_NetworkAdapter.PowerManagementCapabilities
- Win32_NetworkAdapter.PowerManagementSupported
- Win32_NetworkAdapter.ProductName
- Win32_NetworkAdapter.ServiceName
- Win32_NetworkAdapter.Speed
- Win32_NetworkAdapter.Status
- Win32_NetworkAdapter.StatusInfo
- Win32_NetworkAdapter.SystemCreationClassName
- Win32_NetworkAdapter.SystemName
- Win32_NetworkAdapter.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 22718802370995cc0515e3f63e731cc86d37eb0f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468485"
---
# <a name="win32_networkadapter-class"></a><span data-ttu-id="f6b38-105">Win32 \_ NetworkAdapter 類別</span><span class="sxs-lookup"><span data-stu-id="f6b38-105">Win32\_NetworkAdapter class</span></span>

<span data-ttu-id="f6b38-106">**Win32 \_ NetworkAdapter** 類別已被取代。</span><span class="sxs-lookup"><span data-stu-id="f6b38-106">The **Win32\_NetworkAdapter** class is deprecated.</span></span> <span data-ttu-id="f6b38-107">請改用 [**MSFT \_ get-netadapter**](/previous-versions/windows/desktop/legacy/hh968170(v=vs.85)) 類別。</span><span class="sxs-lookup"><span data-stu-id="f6b38-107">Use the [**MSFT\_NetAdapter**](/previous-versions/windows/desktop/legacy/hh968170(v=vs.85)) class instead.</span></span> <span data-ttu-id="f6b38-108">**Win32 \_ NetworkAdapter**[WMI 類別](../wmisdk/retrieving-a-class.md)代表執行 Windows 作業系統之電腦的網路介面卡。</span><span class="sxs-lookup"><span data-stu-id="f6b38-108">The **Win32\_NetworkAdapter**[WMI class](../wmisdk/retrieving-a-class.md) represents a network adapter of a computer running a Windows operating system.</span></span>

<span data-ttu-id="f6b38-109">**Win32 \_NetworkAdapter** 只會提供 IPv4 資料。</span><span class="sxs-lookup"><span data-stu-id="f6b38-109">**Win32\_NetworkAdapter** only supplies IPv4 data.</span></span> <span data-ttu-id="f6b38-110">如需詳細資訊，請參閱 [WMI 中的 IPv6 和 IPv4 支援](../wmisdk/ipv6-and-ipv4-support-in-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="f6b38-110">For more information, see [IPv6 and IPv4 Support in WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md).</span></span>

<span data-ttu-id="f6b38-111">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="f6b38-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="f6b38-112">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="f6b38-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6b38-113">語法</span><span class="sxs-lookup"><span data-stu-id="f6b38-113">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkAdapter : CIM_NetworkAdapter
{
  string   AdapterType;
  uint16   AdapterTypeID;
  boolean  AutoSense;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   GUID;
  uint32   Index;
  datetime InstallDate;
  boolean  Installed;
  uint32   InterfaceIndex;
  uint32   LastErrorCode;
  string   MACAddress;
  string   Manufacturer;
  uint32   MaxNumberControlled;
  uint64   MaxSpeed;
  string   Name;
  string   NetConnectionID;
  uint16   NetConnectionStatus;
  boolean  NetEnabled;
  string   NetworkAddresses[];
  string   PermanentAddress;
  boolean  PhysicalAdapter;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   ProductName;
  string   ServiceName;
  uint64   Speed;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="f6b38-114">成員</span><span class="sxs-lookup"><span data-stu-id="f6b38-114">Members</span></span>

<span data-ttu-id="f6b38-115">**Win32 \_ NetworkAdapter** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f6b38-115">The **Win32\_NetworkAdapter** class has these types of members:</span></span>

-   [<span data-ttu-id="f6b38-116">方法</span><span class="sxs-lookup"><span data-stu-id="f6b38-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="f6b38-117">屬性</span><span class="sxs-lookup"><span data-stu-id="f6b38-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f6b38-118">方法</span><span class="sxs-lookup"><span data-stu-id="f6b38-118">Methods</span></span>

<span data-ttu-id="f6b38-119">**Win32 \_ NetworkAdapter** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="f6b38-119">The **Win32\_NetworkAdapter** class has these methods.</span></span>



| <span data-ttu-id="f6b38-120">方法</span><span class="sxs-lookup"><span data-stu-id="f6b38-120">Method</span></span>                                                          | <span data-ttu-id="f6b38-121">描述</span><span class="sxs-lookup"><span data-stu-id="f6b38-121">Description</span></span>                                                                                                                                                                                                                     |
|:----------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f6b38-122">**停用**</span><span class="sxs-lookup"><span data-stu-id="f6b38-122">**Disable**</span></span>](disable-method-in-class-win32-networkadapter.md) | <span data-ttu-id="f6b38-123">停用網路介面卡。</span><span class="sxs-lookup"><span data-stu-id="f6b38-123">Disables the network adapter.</span></span><br/>                                                                                                                                                                                        |
| [<span data-ttu-id="f6b38-124">**啟用**</span><span class="sxs-lookup"><span data-stu-id="f6b38-124">**Enable**</span></span>](enable-method-in-class-win32-networkadapter.md)   | <span data-ttu-id="f6b38-125">啟用網路介面卡。</span><span class="sxs-lookup"><span data-stu-id="f6b38-125">Enables the network adapter.</span></span><br/>                                                                                                                                                                                         |
| <span data-ttu-id="f6b38-126">**重設**</span><span class="sxs-lookup"><span data-stu-id="f6b38-126">**Reset**</span></span>                                                       | <span data-ttu-id="f6b38-127">未實作。</span><span class="sxs-lookup"><span data-stu-id="f6b38-127">Not implemented.</span></span> <span data-ttu-id="f6b38-128">如需如何執行此方法的詳細資訊，請參閱 [**CIM \_ NetworkAdapter**](cim-networkadapter.md)中的 [**Reset**](reset-method-in-class-cim-controller.md)方法。</span><span class="sxs-lookup"><span data-stu-id="f6b38-128">For more information about how to implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span><br/>                 |
| <span data-ttu-id="f6b38-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="f6b38-129">**SetPowerState**</span></span>                                               | <span data-ttu-id="f6b38-130">未實作。</span><span class="sxs-lookup"><span data-stu-id="f6b38-130">Not implemented.</span></span> <span data-ttu-id="f6b38-131">如需如何執行此方法的詳細資訊，請參閱 [**CIM \_ NetworkAdapter**](cim-networkadapter.md)中的 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md)方法。</span><span class="sxs-lookup"><span data-stu-id="f6b38-131">For more information about how to implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f6b38-132">屬性</span><span class="sxs-lookup"><span data-stu-id="f6b38-132">Properties</span></span>

<span data-ttu-id="f6b38-133">**Win32 \_ NetworkAdapter** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f6b38-133">The **Win32\_NetworkAdapter** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f6b38-134">**AdapterType**</span><span class="sxs-lookup"><span data-stu-id="f6b38-134">**AdapterType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6b38-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b38-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-137">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)：：[OID \_ GEN \_ MEDIA \_ IN \_ USE](/windows-hardware/drivers/network/oid-gen-media-in-use)" ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)::[OID\_GEN\_MEDIA\_IN\_USE](/windows-hardware/drivers/network/oid-gen-media-in-use)")</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-138">網路媒體使用中。</span><span class="sxs-lookup"><span data-stu-id="f6b38-138">Network medium in use.</span></span> <span data-ttu-id="f6b38-139">網路介面卡如下所示：</span><span class="sxs-lookup"><span data-stu-id="f6b38-139">The network adapters are as follows:</span></span>

<dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

<span data-ttu-id="f6b38-140">**Ethernet 802.3** ( 「ethernet 802.3」 ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-140">**Ethernet 802.3** ("Ethernet 802.3")</span></span>


</dt> <dd></dd> <dt>

<span id="Token_Ring_802.5"></span><span id="token_ring_802.5"></span><span id="TOKEN_RING_802.5"></span>

<span data-ttu-id="f6b38-141">**權杖響鈴 802.5** ( 「權杖環形802.5」 ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-141">**Token Ring 802.5** ("Token Ring 802.5")</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber_Distributed_Data_Interface__FDDI_"></span><span id="fiber_distributed_data_interface__fddi_"></span><span id="FIBER_DISTRIBUTED_DATA_INTERFACE__FDDI_"></span>

<span data-ttu-id="f6b38-142">**光纖分散式資料介面 (fddi)** ( 「光纖分散式資料介面 (FDDI) 」 ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-142">**Fiber Distributed Data Interface (FDDI)** ("Fiber Distributed Data Interface (FDDI)")</span></span>


</dt> <dd></dd> <dt>

<span id="Wide_Area_Network__WAN_"></span><span id="wide_area_network__wan_"></span><span id="WIDE_AREA_NETWORK__WAN_"></span>

<span data-ttu-id="f6b38-143">廣域網路 **(wan)** ( 「廣域網路 (wan) 」 ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-143">**Wide Area Network (WAN)** ("Wide Area Network (WAN)")</span></span>


</dt> <dd></dd> <dt>

<span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>

<span data-ttu-id="f6b38-144">**LocalTalk** ( "LocalTalk" ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-144">**LocalTalk** ("LocalTalk")</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_using_DIX_header_format"></span><span id="ethernet_using_dix_header_format"></span><span id="ETHERNET_USING_DIX_HEADER_FORMAT"></span>

<span data-ttu-id="f6b38-145">**使用 DIX 標頭格式的乙太** 網路 ( 「使用 DIX 標頭格式的乙太網路」 ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-145">**Ethernet using DIX header format** ("Ethernet using DIX header format")</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNET"></span><span id="arcnet"></span>

<span data-ttu-id="f6b38-146">**ARCNET** ( "ARCNET" ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-146">**ARCNET** ("ARCNET")</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNET__878.2_"></span><span id="arcnet__878.2_"></span>

<span data-ttu-id="f6b38-147">**ARCNET (878.2)** ( "ARCNET (878.2) " ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-147">**ARCNET (878.2)** ("ARCNET (878.2)")</span></span>


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

<span data-ttu-id="f6b38-148">**Atm** ( 「atm」 ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-148">**ATM** ("ATM")</span></span>


</dt> <dd></dd> <dt>

<span id="Wireless"></span><span id="wireless"></span><span id="WIRELESS"></span>

<span data-ttu-id="f6b38-149">**無線** ( 「無線」 ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-149">**Wireless** ("Wireless")</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared_Wireless"></span><span id="infrared_wireless"></span><span id="INFRARED_WIRELESS"></span>

<span data-ttu-id="f6b38-150">**紅外線無線** ( 「紅外線無線」 ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-150">**Infrared Wireless** ("Infrared Wireless")</span></span>


</dt> <dd></dd> <dt>

<span id="Bpc"></span><span id="bpc"></span><span id="BPC"></span>

<span data-ttu-id="f6b38-151">**Bpc** ( "bpc" ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-151">**Bpc** ("Bpc")</span></span>


</dt> <dd></dd> <dt>

<span id="CoWan"></span><span id="cowan"></span><span id="COWAN"></span>

<span data-ttu-id="f6b38-152">**CoWan** ( "CoWan" ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-152">**CoWan** ("CoWan")</span></span>


</dt> <dd></dd> <dt>

<span id="1394"></span>

<span data-ttu-id="f6b38-153">**1394** ( "1394" ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-153">**1394** ("1394")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f6b38-154">**AdapterTypeID**</span><span class="sxs-lookup"><span data-stu-id="f6b38-154">**AdapterTypeID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-155">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f6b38-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b38-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-157">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)：：[OID \_ GEN \_ MEDIA \_ IN \_ USE](/windows-hardware/drivers/network/oid-gen-media-in-use)" ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-157">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)::[OID\_GEN\_MEDIA\_IN\_USE](/windows-hardware/drivers/network/oid-gen-media-in-use)")</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-158">網路媒體使用中。</span><span class="sxs-lookup"><span data-stu-id="f6b38-158">Network medium in use.</span></span> <span data-ttu-id="f6b38-159">傳回與 **AdapterType** 屬性相同的資訊，但資訊是以整數形式表示。</span><span class="sxs-lookup"><span data-stu-id="f6b38-159">Returns the same information as the **AdapterType** property, except that the information is in the form of an integer.</span></span>

<dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

<span data-ttu-id="f6b38-160">**Ethernet 802.3** (0) </span><span class="sxs-lookup"><span data-stu-id="f6b38-160">**Ethernet 802.3** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Token_Ring_802.5"></span><span id="token_ring_802.5"></span><span id="TOKEN_RING_802.5"></span>

<span data-ttu-id="f6b38-161">**權杖響鈴 802.5** (1) </span><span class="sxs-lookup"><span data-stu-id="f6b38-161">**Token Ring 802.5** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber_Distributed_Data_Interface__FDDI_"></span><span id="fiber_distributed_data_interface__fddi_"></span><span id="FIBER_DISTRIBUTED_DATA_INTERFACE__FDDI_"></span>

<span data-ttu-id="f6b38-162">**光纖分散式資料介面 (FDDI)** (2) </span><span class="sxs-lookup"><span data-stu-id="f6b38-162">**Fiber Distributed Data Interface (FDDI)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Wide_Area_Network__WAN_"></span><span id="wide_area_network__wan_"></span><span id="WIDE_AREA_NETWORK__WAN_"></span>

<span data-ttu-id="f6b38-163">廣域網路 **(WAN)** (3) </span><span class="sxs-lookup"><span data-stu-id="f6b38-163">**Wide Area Network (WAN)** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>

<span data-ttu-id="f6b38-164">**LocalTalk** (4) </span><span class="sxs-lookup"><span data-stu-id="f6b38-164">**LocalTalk** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_using_DIX_header_format"></span><span id="ethernet_using_dix_header_format"></span><span id="ETHERNET_USING_DIX_HEADER_FORMAT"></span>

<span data-ttu-id="f6b38-165">**使用 DIX 標頭格式的乙太** 網路 (5) </span><span class="sxs-lookup"><span data-stu-id="f6b38-165">**Ethernet using DIX header format** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNET"></span><span id="arcnet"></span>

<span data-ttu-id="f6b38-166">**ARCNET** (6) </span><span class="sxs-lookup"><span data-stu-id="f6b38-166">**ARCNET** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNET__878.2_"></span><span id="arcnet__878.2_"></span>

<span data-ttu-id="f6b38-167">**ARCNET (878.2)** (7) </span><span class="sxs-lookup"><span data-stu-id="f6b38-167">**ARCNET (878.2)** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

<span data-ttu-id="f6b38-168">**ATM** (8) </span><span class="sxs-lookup"><span data-stu-id="f6b38-168">**ATM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Wireless"></span><span id="wireless"></span><span id="WIRELESS"></span>

<span data-ttu-id="f6b38-169">**無線** (9) </span><span class="sxs-lookup"><span data-stu-id="f6b38-169">**Wireless** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared_Wireless"></span><span id="infrared_wireless"></span><span id="INFRARED_WIRELESS"></span>

<span data-ttu-id="f6b38-170">**紅外線無線** (10) </span><span class="sxs-lookup"><span data-stu-id="f6b38-170">**Infrared Wireless** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Bpc"></span><span id="bpc"></span><span id="BPC"></span>

<span data-ttu-id="f6b38-171">**Bpc** (11) </span><span class="sxs-lookup"><span data-stu-id="f6b38-171">**Bpc** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="CoWan"></span><span id="cowan"></span><span id="COWAN"></span>

<span data-ttu-id="f6b38-172">**CoWan** (12) </span><span class="sxs-lookup"><span data-stu-id="f6b38-172">**CoWan** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="1394"></span>

<span data-ttu-id="f6b38-173">**1394** (13) </span><span class="sxs-lookup"><span data-stu-id="f6b38-173">**1394** (13)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f6b38-174">**自動感測**</span><span class="sxs-lookup"><span data-stu-id="f6b38-174">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-175">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="f6b38-175">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b38-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-177">若 **為 True**，則網路介面卡可以自動判斷所連接或網路媒體的速度。</span><span class="sxs-lookup"><span data-stu-id="f6b38-177">If **True**, the network adapter can automatically determine the speed of the attached or network media.</span></span>

<span data-ttu-id="f6b38-178">這個屬性繼承自 [**CIM \_ NetworkAdapter**](cim-networkadapter.md)。</span><span class="sxs-lookup"><span data-stu-id="f6b38-178">This property is inherited from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="f6b38-179">這個屬性尚未執行。</span><span class="sxs-lookup"><span data-stu-id="f6b38-179">This property has not been implemented yet.</span></span> <span data-ttu-id="f6b38-180">根據預設，它會傳回 **Null** 值。</span><span class="sxs-lookup"><span data-stu-id="f6b38-180">It returns a **NULL** value by default.</span></span>

</dd> <dt>

<span data-ttu-id="f6b38-181">**可用性**</span><span class="sxs-lookup"><span data-stu-id="f6b38-181">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-182">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f6b38-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b38-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-184">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="f6b38-184">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-185">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="f6b38-185">Availability and status of the device.</span></span>

<span data-ttu-id="f6b38-186">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f6b38-186">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f6b38-187"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="f6b38-187"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f6b38-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="f6b38-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="f6b38-189"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="f6b38-189"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-190">執行中或完整電源</span><span class="sxs-lookup"><span data-stu-id="f6b38-190">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="f6b38-191"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="f6b38-191"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="f6b38-192"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="f6b38-192"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f6b38-193"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="f6b38-193"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="f6b38-194"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="f6b38-194"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="f6b38-195"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="f6b38-195"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="f6b38-196"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="f6b38-196"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f6b38-197"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="f6b38-197"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="f6b38-198"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="f6b38-198"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="f6b38-199"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="f6b38-199"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="f6b38-200"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="f6b38-200"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-201">裝置已知處於省電狀態，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="f6b38-201">The device is known to be in a power save state, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="f6b38-202"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="f6b38-202"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-203">裝置處於省電狀態，但仍正常運作，而且可能會顯示效能下降。</span><span class="sxs-lookup"><span data-stu-id="f6b38-203">The device is in a power save state, but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="f6b38-204"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="f6b38-204"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-205">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="f6b38-205">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="f6b38-206"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="f6b38-206"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="f6b38-207"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="f6b38-207"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-208">裝置處於警告狀態，但也處於省電狀態。</span><span class="sxs-lookup"><span data-stu-id="f6b38-208">The device is in a warning state, though also in a power save state.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="f6b38-209"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="f6b38-209"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-210">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="f6b38-210">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="f6b38-211"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="f6b38-211"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-212">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="f6b38-212">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="f6b38-213"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="f6b38-213"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-214">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="f6b38-214">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="f6b38-215"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="f6b38-215"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-216">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="f6b38-216">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f6b38-217">**標題**</span><span class="sxs-lookup"><span data-stu-id="f6b38-217">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-218">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6b38-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-219">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b38-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-220">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-220">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-221">物件的簡短描述（單行字串）。</span><span class="sxs-lookup"><span data-stu-id="f6b38-221">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="f6b38-222">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f6b38-222">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6b38-223">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="f6b38-223">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-224">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f6b38-224">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-225">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b38-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-226">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-226">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-227">Windows 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f6b38-227">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="f6b38-228">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f6b38-228">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="f6b38-229"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="f6b38-229"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="f6b38-230"> (0)</span><span class="sxs-lookup"><span data-stu-id="f6b38-230">(0)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-231">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="f6b38-231">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="f6b38-232"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="f6b38-232"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="f6b38-233">(1)</span><span class="sxs-lookup"><span data-stu-id="f6b38-233">(1)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-234">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="f6b38-234">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f6b38-235"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="f6b38-235"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="f6b38-236">(2)</span><span class="sxs-lookup"><span data-stu-id="f6b38-236">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="f6b38-237"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="f6b38-237"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="f6b38-238">(3)</span><span class="sxs-lookup"><span data-stu-id="f6b38-238">(3)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-239">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="f6b38-239">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="f6b38-240"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="f6b38-240"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="f6b38-241">(4)</span><span class="sxs-lookup"><span data-stu-id="f6b38-241">(4)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-242">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="f6b38-242">Device is not working properly.</span></span> <span data-ttu-id="f6b38-243">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="f6b38-243">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="f6b38-244"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="f6b38-244"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="f6b38-245">(5)</span><span class="sxs-lookup"><span data-stu-id="f6b38-245">(5)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-246">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="f6b38-246">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="f6b38-247"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="f6b38-247"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="f6b38-248">(6)</span><span class="sxs-lookup"><span data-stu-id="f6b38-248">(6)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-249">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="f6b38-249">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="f6b38-250"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="f6b38-250"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="f6b38-251">(7)</span><span class="sxs-lookup"><span data-stu-id="f6b38-251">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="f6b38-252"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="f6b38-252"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="f6b38-253">(8)</span><span class="sxs-lookup"><span data-stu-id="f6b38-253">(8)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-254">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="f6b38-254">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="f6b38-255"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="f6b38-255"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="f6b38-256">(9)</span><span class="sxs-lookup"><span data-stu-id="f6b38-256">(9)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-257">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="f6b38-257">Device is not working properly.</span></span> <span data-ttu-id="f6b38-258">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="f6b38-258">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="f6b38-259"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="f6b38-259"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="f6b38-260">(10)</span><span class="sxs-lookup"><span data-stu-id="f6b38-260">(10)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-261">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="f6b38-261">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="f6b38-262"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="f6b38-262"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="f6b38-263">(11)</span><span class="sxs-lookup"><span data-stu-id="f6b38-263">(11)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-264">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="f6b38-264">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="f6b38-265"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="f6b38-265"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="f6b38-266"> (12) </span><span class="sxs-lookup"><span data-stu-id="f6b38-266">(12)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-267">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="f6b38-267">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="f6b38-268"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="f6b38-268"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="f6b38-269">(13)</span><span class="sxs-lookup"><span data-stu-id="f6b38-269">(13)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-270">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="f6b38-270">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="f6b38-271"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="f6b38-271"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="f6b38-272">(14)</span><span class="sxs-lookup"><span data-stu-id="f6b38-272">(14)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-273">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="f6b38-273">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="f6b38-274"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="f6b38-274"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="f6b38-275">(15)</span><span class="sxs-lookup"><span data-stu-id="f6b38-275">(15)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-276">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="f6b38-276">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="f6b38-277"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="f6b38-277"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="f6b38-278">(16)</span><span class="sxs-lookup"><span data-stu-id="f6b38-278">(16)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-279">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="f6b38-279">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="f6b38-280"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="f6b38-280"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="f6b38-281">(17)</span><span class="sxs-lookup"><span data-stu-id="f6b38-281">(17)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-282">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="f6b38-282">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f6b38-283"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="f6b38-283"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="f6b38-284">(18)</span><span class="sxs-lookup"><span data-stu-id="f6b38-284">(18)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-285">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="f6b38-285">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="f6b38-286"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="f6b38-286"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="f6b38-287">(19)</span><span class="sxs-lookup"><span data-stu-id="f6b38-287">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="f6b38-288"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="f6b38-288"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="f6b38-289">(20)</span><span class="sxs-lookup"><span data-stu-id="f6b38-289">(20)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-290">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="f6b38-290">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="f6b38-291"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="f6b38-291"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="f6b38-292">(21)</span><span class="sxs-lookup"><span data-stu-id="f6b38-292">(21)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-293">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="f6b38-293">System failure.</span></span> <span data-ttu-id="f6b38-294">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="f6b38-294">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="f6b38-295">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="f6b38-295">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="f6b38-296"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="f6b38-296"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="f6b38-297">(22)</span><span class="sxs-lookup"><span data-stu-id="f6b38-297">(22)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-298">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="f6b38-298">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="f6b38-299"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="f6b38-299"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="f6b38-300">(23)</span><span class="sxs-lookup"><span data-stu-id="f6b38-300">(23)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-301">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="f6b38-301">System failure.</span></span> <span data-ttu-id="f6b38-302">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="f6b38-302">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="f6b38-303"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="f6b38-303"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="f6b38-304">(24)</span><span class="sxs-lookup"><span data-stu-id="f6b38-304">(24)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-305">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="f6b38-305">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="f6b38-306"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="f6b38-306"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="f6b38-307">(25)</span><span class="sxs-lookup"><span data-stu-id="f6b38-307">(25)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-308">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="f6b38-308">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="f6b38-309"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="f6b38-309"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="f6b38-310">(26)</span><span class="sxs-lookup"><span data-stu-id="f6b38-310">(26)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-311">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="f6b38-311">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="f6b38-312"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="f6b38-312"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="f6b38-313">(27)</span><span class="sxs-lookup"><span data-stu-id="f6b38-313">(27)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-314">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="f6b38-314">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="f6b38-315"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="f6b38-315"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="f6b38-316">(28)</span><span class="sxs-lookup"><span data-stu-id="f6b38-316">(28)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-317">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="f6b38-317">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="f6b38-318"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="f6b38-318"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="f6b38-319">(29)</span><span class="sxs-lookup"><span data-stu-id="f6b38-319">(29)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-320">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="f6b38-320">Device is disabled.</span></span> <span data-ttu-id="f6b38-321">裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="f6b38-321">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="f6b38-322"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="f6b38-322"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="f6b38-323">(30)</span><span class="sxs-lookup"><span data-stu-id="f6b38-323">(30)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-324">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="f6b38-324">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f6b38-325"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="f6b38-325"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="f6b38-326"> (31) </span><span class="sxs-lookup"><span data-stu-id="f6b38-326">(31)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-327">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="f6b38-327">Device is not working properly.</span></span> <span data-ttu-id="f6b38-328">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="f6b38-328">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f6b38-329">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="f6b38-329">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-330">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="f6b38-330">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-331">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b38-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-332">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-332">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-333">若 **為 True**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="f6b38-333">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="f6b38-334">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f6b38-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6b38-335">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f6b38-335">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-336">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6b38-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-337">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b38-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-338">限定詞： [ **CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="f6b38-338">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-339">第一個具體類別的名稱，這個類別會出現在建立實例時所使用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="f6b38-339">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="f6b38-340">搭配類別的其他索引鍵屬性使用時，屬性可讓這個類別的所有實例和其子類別都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="f6b38-340">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="f6b38-341">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f6b38-341">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6b38-342">**說明**</span><span class="sxs-lookup"><span data-stu-id="f6b38-342">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-343">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6b38-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-344">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b38-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-345">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-345">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-346">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="f6b38-346">Description of the object.</span></span>

<span data-ttu-id="f6b38-347">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f6b38-347">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6b38-348">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="f6b38-348">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-349">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6b38-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-350">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b38-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-351">限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "DeviceId" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \\ \\ {4D36E972-E325-11CE-BFC1-08002BE10318}" ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-351">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Class\\\\{4D36E972-E325-11CE-BFC1-08002BE10318}")</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-352">系統上其他裝置之網路介面卡的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="f6b38-352">Unique identifier of the network adapter from other devices on the system.</span></span>

<span data-ttu-id="f6b38-353">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f6b38-353">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6b38-354">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="f6b38-354">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-355">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="f6b38-355">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-356">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b38-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-357">若 **為 True**，則表示 **LastErrorCode** 中回報的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="f6b38-357">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="f6b38-358">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f6b38-358">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6b38-359">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="f6b38-359">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-360">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6b38-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-361">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b38-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-362">**LastErrorCode** 中所記錄錯誤的詳細資訊，以及任何可能採取之矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f6b38-362">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="f6b38-363">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f6b38-363">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6b38-364">**GUID**</span><span class="sxs-lookup"><span data-stu-id="f6b38-364">**GUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-365">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6b38-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-366">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b38-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-367">連接的全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="f6b38-367">Globally unique identifier for the connection.</span></span>

</dd> <dt>

<span data-ttu-id="f6b38-368">**Index**</span><span class="sxs-lookup"><span data-stu-id="f6b38-368">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-369">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f6b38-369">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-370">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b38-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-371">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \\ \\ {4D36E972-E325-11CE-BFC1-08002BE10318}" ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-371">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Class\\\\{4D36E972-E325-11CE-BFC1-08002BE10318}")</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-372">網路介面卡的索引編號，儲存在系統登錄中。</span><span class="sxs-lookup"><span data-stu-id="f6b38-372">Index number of the network adapter, stored in the system registry.</span></span>

<span data-ttu-id="f6b38-373">範例：0</span><span class="sxs-lookup"><span data-stu-id="f6b38-373">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="f6b38-374">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f6b38-374">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-375">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="f6b38-375">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-376">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b38-376">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-377">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="f6b38-377">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-378">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="f6b38-378">Date and time the object was installed.</span></span> <span data-ttu-id="f6b38-379">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="f6b38-379">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="f6b38-380">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f6b38-380">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f6b38-381">這個屬性尚未執行。</span><span class="sxs-lookup"><span data-stu-id="f6b38-381">This property has not been implemented yet.</span></span> <span data-ttu-id="f6b38-382">根據預設，它會傳回 **Null** 值。</span><span class="sxs-lookup"><span data-stu-id="f6b38-382">It returns a **NULL** value by default.</span></span>

</dd> <dt>

<span data-ttu-id="f6b38-383">**已安裝**</span><span class="sxs-lookup"><span data-stu-id="f6b38-383">**Installed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-384">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="f6b38-384">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-385">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b38-385">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-386">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ NetworkCards \| DriverDate" ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-386">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\NetworkCards\|DriverDate")</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-387">若 **為 True**，則會在系統中安裝網路介面卡。</span><span class="sxs-lookup"><span data-stu-id="f6b38-387">If **True**, the network adapter is installed in the system.</span></span>

</dd> <dt>

<span data-ttu-id="f6b38-388">**InterfaceIndex**</span><span class="sxs-lookup"><span data-stu-id="f6b38-388">**InterfaceIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-389">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f6b38-389">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-390">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b38-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-391">可唯一識別區域網路介面的索引值。</span><span class="sxs-lookup"><span data-stu-id="f6b38-391">Index value that uniquely identifies the local network interface.</span></span> <span data-ttu-id="f6b38-392">這個屬性中的值與 [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable)實例（代表路由表中的網路介面）的 **InterfaceIndex** 屬性值相同。</span><span class="sxs-lookup"><span data-stu-id="f6b38-392">The value in this property is the same as the value in the **InterfaceIndex** property in the instance of [**Win32\_IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) that represents the network interface in the route table.</span></span>

</dd> <dt>

<span data-ttu-id="f6b38-393">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="f6b38-393">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-394">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f6b38-394">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-395">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b38-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-396">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f6b38-396">Last error code reported by the logical device.</span></span>

<span data-ttu-id="f6b38-397">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f6b38-397">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6b38-398">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="f6b38-398">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-399">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6b38-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-400">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b38-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-401">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Device Input and Output 函數 \| [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)" ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-401">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Input and Output Functions\|[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)")</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-402">此網路介面卡的媒體存取控制位址。</span><span class="sxs-lookup"><span data-stu-id="f6b38-402">Media access control address for this network adapter.</span></span> <span data-ttu-id="f6b38-403">MAC 位址是由製造商指派給網路介面卡的唯一48位號碼。</span><span class="sxs-lookup"><span data-stu-id="f6b38-403">A MAC address is a unique 48-bit number assigned to the network adapter by the manufacturer.</span></span> <span data-ttu-id="f6b38-404">它會唯一識別此網路介面卡，並用於對應 TCP/IP 網路通訊。</span><span class="sxs-lookup"><span data-stu-id="f6b38-404">It uniquely identifies this network adapter and is used for mapping TCP/IP network communications.</span></span>

</dd> <dt>

<span data-ttu-id="f6b38-405">**製造商**</span><span class="sxs-lookup"><span data-stu-id="f6b38-405">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-406">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6b38-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-407">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b38-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-408">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ NetworkCards \| 製造商" ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-408">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\NetworkCards\|Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-409">網路介面卡的製造商名稱。</span><span class="sxs-lookup"><span data-stu-id="f6b38-409">Name of the network adapter's manufacturer.</span></span>

<span data-ttu-id="f6b38-410">範例： "3COM"</span><span class="sxs-lookup"><span data-stu-id="f6b38-410">Example: "3COM"</span></span>

</dd> <dt>

<span data-ttu-id="f6b38-411">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="f6b38-411">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-412">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f6b38-412">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-413">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b38-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-414">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 匯流排埠 \| 001.9 \| 最大附件數目 ") </span><span class="sxs-lookup"><span data-stu-id="f6b38-414">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.9\|Maximum Number of Attachments")</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-415">此網路介面卡支援的直接可定址埠數目上限。</span><span class="sxs-lookup"><span data-stu-id="f6b38-415">Maximum number of directly addressable ports supported by this network adapter.</span></span> <span data-ttu-id="f6b38-416">值為 0 (零) 如果數位未知，則應使用此值。</span><span class="sxs-lookup"><span data-stu-id="f6b38-416">A value of 0 (zero) should be used if the number is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="f6b38-417">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="f6b38-417">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-418">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="f6b38-418">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-419">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b38-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-420">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( 「每秒位數」 ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-420">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-421">網路介面卡的最大速度（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="f6b38-421">Maximum speed, in bits per second, for the network adapter.</span></span>

<span data-ttu-id="f6b38-422">這個屬性繼承自 [**CIM \_ NetworkAdapter**](cim-networkadapter.md)。</span><span class="sxs-lookup"><span data-stu-id="f6b38-422">This property is inherited from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="f6b38-423">這個屬性尚未執行。</span><span class="sxs-lookup"><span data-stu-id="f6b38-423">This property has not been implemented yet.</span></span> <span data-ttu-id="f6b38-424">根據預設，它會傳回 **Null** 值。</span><span class="sxs-lookup"><span data-stu-id="f6b38-424">It returns a **NULL** value by default.</span></span>

<span data-ttu-id="f6b38-425">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="f6b38-425">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f6b38-426">**名稱**</span><span class="sxs-lookup"><span data-stu-id="f6b38-426">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-427">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6b38-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-428">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b38-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-429">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-429">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-430">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="f6b38-430">Label by which the object is known.</span></span> <span data-ttu-id="f6b38-431">子類別化時，可以將屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="f6b38-431">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="f6b38-432">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f6b38-432">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6b38-433">**NetConnectionID**</span><span class="sxs-lookup"><span data-stu-id="f6b38-433">**NetConnectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-434">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6b38-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-435">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f6b38-435">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-436">**網路連線主控台程式** 中顯示的網路連線名稱。</span><span class="sxs-lookup"><span data-stu-id="f6b38-436">Name of the network connection as it appears in the **Network Connections** Control Panel program.</span></span>

</dd> <dt>

<span data-ttu-id="f6b38-437">**NetConnectionStatus**</span><span class="sxs-lookup"><span data-stu-id="f6b38-437">**NetConnectionStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-438">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f6b38-438">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-439">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b38-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-440">網路介面卡連線到網路的狀態。</span><span class="sxs-lookup"><span data-stu-id="f6b38-440">State of the network adapter connection to the network.</span></span>

<dt>

<span id="Disconnected"></span><span id="disconnected"></span><span id="DISCONNECTED"></span>

<span data-ttu-id="f6b38-441">已 **中斷** 連線 (0) </span><span class="sxs-lookup"><span data-stu-id="f6b38-441">**Disconnected** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Connecting"></span><span id="connecting"></span><span id="CONNECTING"></span>

<span data-ttu-id="f6b38-442">**連接** (1) </span><span class="sxs-lookup"><span data-stu-id="f6b38-442">**Connecting** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Connected"></span><span id="connected"></span><span id="CONNECTED"></span>

<span data-ttu-id="f6b38-443">**連接** (2) </span><span class="sxs-lookup"><span data-stu-id="f6b38-443">**Connected** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disconnecting"></span><span id="disconnecting"></span><span id="DISCONNECTING"></span>

<span data-ttu-id="f6b38-444">**中斷** (3) 的連線</span><span class="sxs-lookup"><span data-stu-id="f6b38-444">**Disconnecting** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Hardware_Not_Present"></span><span id="hardware_not_present"></span><span id="HARDWARE_NOT_PRESENT"></span>

<span data-ttu-id="f6b38-445">**硬體不存在** (4) </span><span class="sxs-lookup"><span data-stu-id="f6b38-445">**Hardware Not Present** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Hardware_Disabled"></span><span id="hardware_disabled"></span><span id="HARDWARE_DISABLED"></span>

<span data-ttu-id="f6b38-446">**硬體已停用** (5) </span><span class="sxs-lookup"><span data-stu-id="f6b38-446">**Hardware Disabled** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Hardware_Malfunction"></span><span id="hardware_malfunction"></span><span id="HARDWARE_MALFUNCTION"></span>

<span data-ttu-id="f6b38-447">**硬體故障** (6) </span><span class="sxs-lookup"><span data-stu-id="f6b38-447">**Hardware Malfunction** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Media_Disconnected"></span><span id="media_disconnected"></span><span id="MEDIA_DISCONNECTED"></span>

<span data-ttu-id="f6b38-448">**媒體已中斷** 連線 (7) </span><span class="sxs-lookup"><span data-stu-id="f6b38-448">**Media Disconnected** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Authenticating"></span><span id="authenticating"></span><span id="AUTHENTICATING"></span>

<span data-ttu-id="f6b38-449">**驗證** (8) </span><span class="sxs-lookup"><span data-stu-id="f6b38-449">**Authenticating** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Authentication_Succeeded"></span><span id="authentication_succeeded"></span><span id="AUTHENTICATION_SUCCEEDED"></span>

<span data-ttu-id="f6b38-450">**驗證成功** (9) </span><span class="sxs-lookup"><span data-stu-id="f6b38-450">**Authentication Succeeded** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Authentication_Failed"></span><span id="authentication_failed"></span><span id="AUTHENTICATION_FAILED"></span>

<span data-ttu-id="f6b38-451">**驗證失敗** (10) </span><span class="sxs-lookup"><span data-stu-id="f6b38-451">**Authentication Failed** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Invalid_Address"></span><span id="invalid_address"></span><span id="INVALID_ADDRESS"></span>

<span data-ttu-id="f6b38-452">**不正確位址** (11) </span><span class="sxs-lookup"><span data-stu-id="f6b38-452">**Invalid Address** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Credentials_Required"></span><span id="credentials_required"></span><span id="CREDENTIALS_REQUIRED"></span>

<span data-ttu-id="f6b38-453">**需要認證** (12) </span><span class="sxs-lookup"><span data-stu-id="f6b38-453">**Credentials Required** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f6b38-454">**其他**</span><span class="sxs-lookup"><span data-stu-id="f6b38-454">**Other**</span></span>


</dt> <dd><span data-ttu-id="f6b38-455">13–65535</span><span class="sxs-lookup"><span data-stu-id="f6b38-455">13–65535</span></span></dd> </dl>

</dd> <dt>

<span data-ttu-id="f6b38-456">**NetEnabled**</span><span class="sxs-lookup"><span data-stu-id="f6b38-456">**NetEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-457">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="f6b38-457">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-458">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b38-458">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-459">指出是否已啟用介面卡。</span><span class="sxs-lookup"><span data-stu-id="f6b38-459">Indicates whether the adapter is enabled or not.</span></span> <span data-ttu-id="f6b38-460">若 **為 True**，則會啟用介面卡。</span><span class="sxs-lookup"><span data-stu-id="f6b38-460">If **True**, the adapter is enabled.</span></span> <span data-ttu-id="f6b38-461">您可以使用 [**enable**](enable-method-in-class-win32-networkadapter.md) 和 [**disable**](disable-method-in-class-win32-networkadapter.md) 方法來啟用或停用 NIC。</span><span class="sxs-lookup"><span data-stu-id="f6b38-461">You can enable or disable the NIC by using the [**Enable**](enable-method-in-class-win32-networkadapter.md) and [**Disable**](disable-method-in-class-win32-networkadapter.md) methods.</span></span>

</dd> <dt>

<span data-ttu-id="f6b38-462">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="f6b38-462">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-463">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="f6b38-463">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-464">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b38-464">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-465">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) (」 MIF。DMTF \| 網路介面卡802埠 \| 001.3 ") </span><span class="sxs-lookup"><span data-stu-id="f6b38-465">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Network Adapter 802 Port\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-466">介面卡的網路位址陣列。</span><span class="sxs-lookup"><span data-stu-id="f6b38-466">Array of network addresses for an adapter.</span></span>

<span data-ttu-id="f6b38-467">這個屬性繼承自 [**CIM \_ NetworkAdapter**](cim-networkadapter.md)。</span><span class="sxs-lookup"><span data-stu-id="f6b38-467">This property is inherited from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="f6b38-468">這個屬性尚未執行。</span><span class="sxs-lookup"><span data-stu-id="f6b38-468">This property has not been implemented yet.</span></span> <span data-ttu-id="f6b38-469">根據預設，它會傳回 **Null** 值。</span><span class="sxs-lookup"><span data-stu-id="f6b38-469">It returns a **NULL** value by default.</span></span>

</dd> <dt>

<span data-ttu-id="f6b38-470">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="f6b38-470">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-471">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6b38-471">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-472">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b38-472">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-473">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) (」 MIF。DMTF \| 網路介面卡802埠 \| 001.2 ") </span><span class="sxs-lookup"><span data-stu-id="f6b38-473">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Network Adapter 802 Port\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-474">將網路位址硬式編碼為介面卡。</span><span class="sxs-lookup"><span data-stu-id="f6b38-474">Network address hard-coded into an adapter.</span></span> <span data-ttu-id="f6b38-475">此硬式編碼的位址可能會因固件升級或軟體設定而變更。</span><span class="sxs-lookup"><span data-stu-id="f6b38-475">This hard-coded address may be changed by firmware upgrade or software configuration.</span></span> <span data-ttu-id="f6b38-476">如果是，則在進行變更時應該更新此欄位。</span><span class="sxs-lookup"><span data-stu-id="f6b38-476">If so, this field should be updated when the change is made.</span></span> <span data-ttu-id="f6b38-477">如果網路介面卡沒有硬式編碼的位址，則此屬性應該保留空白。</span><span class="sxs-lookup"><span data-stu-id="f6b38-477">The property should be left blank if no hard-coded address exists for the network adapter.</span></span>

<span data-ttu-id="f6b38-478">這個屬性繼承自 [**CIM \_ NetworkAdapter**](cim-networkadapter.md)。</span><span class="sxs-lookup"><span data-stu-id="f6b38-478">This property is inherited from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="f6b38-479">這個屬性尚未執行。</span><span class="sxs-lookup"><span data-stu-id="f6b38-479">This property has not been implemented yet.</span></span> <span data-ttu-id="f6b38-480">根據預設，它會傳回 **Null** 值。</span><span class="sxs-lookup"><span data-stu-id="f6b38-480">It returns a **NULL** value by default.</span></span>

</dd> <dt>

<span data-ttu-id="f6b38-481">**PhysicalAdapter**</span><span class="sxs-lookup"><span data-stu-id="f6b38-481">**PhysicalAdapter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-482">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="f6b38-482">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-483">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b38-483">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-484">指出介面卡是否為實體或邏輯配接器。</span><span class="sxs-lookup"><span data-stu-id="f6b38-484">Indicates whether the adapter is a physical or a logical adapter.</span></span> <span data-ttu-id="f6b38-485">若 **為 True**，則介面卡是實體的。</span><span class="sxs-lookup"><span data-stu-id="f6b38-485">If **True**, the adapter is physical.</span></span>

</dd> <dt>

<span data-ttu-id="f6b38-486">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="f6b38-486">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-487">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6b38-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-488">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b38-488">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-489">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-489">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-490">Windows 隨插即用邏輯裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="f6b38-490">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="f6b38-491">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f6b38-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="f6b38-492">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="f6b38-492">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="f6b38-493">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="f6b38-493">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-494">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="f6b38-494">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-495">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b38-495">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-496">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="f6b38-496">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="f6b38-497">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f6b38-497">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f6b38-498"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="f6b38-498"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="f6b38-499"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="f6b38-499"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f6b38-500"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="f6b38-500"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f6b38-501"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="f6b38-501"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-502">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="f6b38-502">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="f6b38-503"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="f6b38-503"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-504">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="f6b38-504">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="f6b38-505"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="f6b38-505"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-506">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="f6b38-506">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="f6b38-507">這個方法可在父 [**CIM \_ LogicalDevice**](cim-logicaldevice.md) 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="f6b38-507">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="f6b38-508">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](../wmisdk/designing-managed-object-format--mof--classes.md)。</span><span class="sxs-lookup"><span data-stu-id="f6b38-508">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="f6b38-509"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="f6b38-509"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-510">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="f6b38-510">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="f6b38-511"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="f6b38-511"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="f6b38-512">支援計時 Power-On</span><span class="sxs-lookup"><span data-stu-id="f6b38-512">Timed Power-On Supported</span></span>

<span data-ttu-id="f6b38-513">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="f6b38-513">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f6b38-514">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="f6b38-514">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-515">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="f6b38-515">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-516">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b38-516">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-517">若 **為 True**，則裝置可以是電源管理 (可進入暫停模式，依此類推) 。</span><span class="sxs-lookup"><span data-stu-id="f6b38-517">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="f6b38-518">屬性不表示電源管理功能目前已啟用，只有邏輯裝置能夠進行電源管理。</span><span class="sxs-lookup"><span data-stu-id="f6b38-518">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="f6b38-519">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f6b38-519">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6b38-520">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="f6b38-520">**ProductName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-521">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6b38-521">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-522">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b38-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-523">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ NetworkCards \| ServiceName" ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-523">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\NetworkCards\|ServiceName")</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-524">網路介面卡的產品名稱。</span><span class="sxs-lookup"><span data-stu-id="f6b38-524">Product name of the network adapter.</span></span>

<span data-ttu-id="f6b38-525">範例： "Fast EtherLink XL"</span><span class="sxs-lookup"><span data-stu-id="f6b38-525">Example: "Fast EtherLink XL"</span></span>

</dd> <dt>

<span data-ttu-id="f6b38-526">**ServiceName**</span><span class="sxs-lookup"><span data-stu-id="f6b38-526">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-527">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6b38-527">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-528">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b38-528">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-529">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ NetworkCards \| ProductName" ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-529">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\NetworkCards\|ProductName")</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-530">網路介面卡的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="f6b38-530">Service name of the network adapter.</span></span> <span data-ttu-id="f6b38-531">這個名稱通常比完整的產品名稱短。</span><span class="sxs-lookup"><span data-stu-id="f6b38-531">This name is usually shorter than the full product name.</span></span>

<span data-ttu-id="f6b38-532">範例： "Elnkii"</span><span class="sxs-lookup"><span data-stu-id="f6b38-532">Example: "Elnkii"</span></span>

</dd> <dt>

<span data-ttu-id="f6b38-533">**速度**</span><span class="sxs-lookup"><span data-stu-id="f6b38-533">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-534">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="f6b38-534">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-535">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b38-535">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-536">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIB。IETF \| RFC1213-MIB. ifSpeed "，" MIF。「DMTF \| 網路介面卡802埠 \| 001.5」 ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( 每秒「位數」 ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-536">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|RFC1213-MIB.ifSpeed", "MIF.DMTF\|Network Adapter 802 Port\|001.5"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-537">估計目前的頻寬（以位/秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="f6b38-537">Estimate of the current bandwidth in bits per second.</span></span> <span data-ttu-id="f6b38-538">針對因頻寬而異的端點，或無法進行精確估計的端點，這個屬性應該包含名義的頻寬。</span><span class="sxs-lookup"><span data-stu-id="f6b38-538">For endpoints which vary in bandwidth or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span>

<span data-ttu-id="f6b38-539">這個屬性繼承自 [**CIM \_ NetworkAdapter**](cim-networkadapter.md)。</span><span class="sxs-lookup"><span data-stu-id="f6b38-539">This property is inherited from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="f6b38-540">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="f6b38-540">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f6b38-541">**狀態**</span><span class="sxs-lookup"><span data-stu-id="f6b38-541">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-542">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6b38-542">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-543">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b38-543">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-544">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-544">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-545">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="f6b38-545">Current status of the object.</span></span> <span data-ttu-id="f6b38-546">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f6b38-546">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f6b38-547">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="f6b38-547">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f6b38-548">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-548">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f6b38-549">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-549">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f6b38-550">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-550">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f6b38-551">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-551">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f6b38-552">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-552">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f6b38-553">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-553">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f6b38-554">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-554">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f6b38-555">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-555">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f6b38-556">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-556">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f6b38-557">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-557">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f6b38-558">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-558">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f6b38-559">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-559">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f6b38-560">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="f6b38-560">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-561">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f6b38-561">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-562">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b38-562">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-563">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="f6b38-563">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-564">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="f6b38-564">State of the logical device.</span></span> <span data-ttu-id="f6b38-565">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="f6b38-565">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="f6b38-566">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f6b38-566">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f6b38-567">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="f6b38-567">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f6b38-568">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="f6b38-568">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f6b38-569">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="f6b38-569">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f6b38-570">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="f6b38-570">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f6b38-571">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="f6b38-571">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f6b38-572">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f6b38-572">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-573">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6b38-573">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-574">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b38-574">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-575">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="f6b38-575">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-576">範圍電腦之 **CreationClassName** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="f6b38-576">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="f6b38-577">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f6b38-577">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6b38-578">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="f6b38-578">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-579">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6b38-579">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-580">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b38-580">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-581">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="f6b38-581">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-582">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6b38-582">Name of the scoping system.</span></span>

<span data-ttu-id="f6b38-583">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f6b38-583">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6b38-584">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="f6b38-584">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b38-585">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="f6b38-585">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-586">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6b38-586">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6b38-587">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SOFTWARE \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ Perflib \\ \\ 009 \| System Up Time" ) </span><span class="sxs-lookup"><span data-stu-id="f6b38-587">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Perflib\\\\009\|System Up Time")</span></span>
</dt> </dl>

<span data-ttu-id="f6b38-588">上次重設網路介面卡的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="f6b38-588">Date and time the network adapter was last reset.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f6b38-589">備註</span><span class="sxs-lookup"><span data-stu-id="f6b38-589">Remarks</span></span>

<span data-ttu-id="f6b38-590">**Win32 \_ NetworkAdapter** 類別衍生自 [**CIM \_ NetworkAdapter**](cim-networkadapter.md)。</span><span class="sxs-lookup"><span data-stu-id="f6b38-590">The **Win32\_NetworkAdapter** class is derived from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="f6b38-591">下列清單描述 **Win32 \_ NetworkAdapter** 的 Associator 類別：</span><span class="sxs-lookup"><span data-stu-id="f6b38-591">The following list describes the Associator classes for **Win32\_NetworkAdapter**:</span></span>

-   [<span data-ttu-id="f6b38-592">**Win32 \_ PnPEntity**</span><span class="sxs-lookup"><span data-stu-id="f6b38-592">**Win32\_PnPEntity**</span></span>](win32-pnpentity.md)
-   [<span data-ttu-id="f6b38-593">**Win32 \_ 未進行**</span><span class="sxs-lookup"><span data-stu-id="f6b38-593">**Win32\_ComputerSystem**</span></span>](win32-computersystem.md)
-   [<span data-ttu-id="f6b38-594">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="f6b38-594">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
-   [<span data-ttu-id="f6b38-595">**Win32 \_ IRQResource**</span><span class="sxs-lookup"><span data-stu-id="f6b38-595">**Win32\_IRQResource**</span></span>](win32-irqresource.md)
-   [<span data-ttu-id="f6b38-596">**Win32 \_ DeviceMemoryAddress**</span><span class="sxs-lookup"><span data-stu-id="f6b38-596">**Win32\_DeviceMemoryAddress**</span></span>](win32-devicememoryaddress.md)
-   [<span data-ttu-id="f6b38-597">**Win32 \_ PortResource**</span><span class="sxs-lookup"><span data-stu-id="f6b38-597">**Win32\_PortResource**</span></span>](win32-portresource.md)
-   [<span data-ttu-id="f6b38-598">**Win32 \_ NetworkProtocol**</span><span class="sxs-lookup"><span data-stu-id="f6b38-598">**Win32\_NetworkProtocol**</span></span>](win32-networkprotocol.md)
-   [<span data-ttu-id="f6b38-599">**Win32 \_ >systemdriver**</span><span class="sxs-lookup"><span data-stu-id="f6b38-599">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)

<span data-ttu-id="f6b38-600">許多系統上有多個網路介面卡。</span><span class="sxs-lookup"><span data-stu-id="f6b38-600">Many systems have a number of network adapters on them.</span></span> <span data-ttu-id="f6b38-601">請考慮使用下列所示的參考來尋找目前的介面卡：</span><span class="sxs-lookup"><span data-stu-id="f6b38-601">Consider using the following as a reference to find the current adapters:</span></span>

``` syntax
AdapterType: "Ethernet 802.3"
MACAddress: String Length > 16
Availability: 3
PNPDeviceID: InStr ( PNPDeviceID, "PCI") = 1
Installed: vbTrue
ConfigManagerErrorCode: 0
: <keep this as an index to Win32_NetworkAdapterConfiguration>
```

<span data-ttu-id="f6b38-602">即使使用上述的限定詞，您也可能會抓取一個以上的有效網路介面卡。</span><span class="sxs-lookup"><span data-stu-id="f6b38-602">Even using the above qualifiers, you will likely retrieve more than one valid network adapter.</span></span> <span data-ttu-id="f6b38-603">如果是這種情況，您可以使用下列資訊來進一步限定您的 Win32 \_ >networkadapterconfiguration 搜尋：</span><span class="sxs-lookup"><span data-stu-id="f6b38-603">If that is the case, Then you can use the following information to further qualify your search of the Win32\_NetworkAdapterConfiguration:</span></span>

``` syntax
Index: <match to DeviceID above>
MACAddress: Length > 16
DefaultIPGateway: String Length > 6
DNSServerSearchOrder: Array of strings with length > 6
IPEnabled: vbTrue
IPAddress: Array of strings with length > 6
```

<span data-ttu-id="f6b38-604">完成之後，您可能會將清單縮減為一或兩個已設定的介面卡。</span><span class="sxs-lookup"><span data-stu-id="f6b38-604">Once you have done so, you will likely have reduced your list to one or two configured adapters.</span></span>

<span data-ttu-id="f6b38-605">您也可以使用下列程式來尋找預設的介面卡：</span><span class="sxs-lookup"><span data-stu-id="f6b38-605">You can also use the following procedure to find the default adapter:</span></span>

1.  <span data-ttu-id="f6b38-606">執行下列查詢：</span><span class="sxs-lookup"><span data-stu-id="f6b38-606">Run the following query:</span></span>

    `"SELECT InterfaceIndex, Destination FROM Win32_IP4RouteTable WHERE Destination='0.0.0.0'"`

    <span data-ttu-id="f6b38-607">您只能有一個預設的網路目的地0.0.0.0。</span><span class="sxs-lookup"><span data-stu-id="f6b38-607">You should only have one default network destination 0.0.0.0.</span></span>

2.  <span data-ttu-id="f6b38-608">使用 **InterfaceIndex** 來取出您要的網路介面卡。</span><span class="sxs-lookup"><span data-stu-id="f6b38-608">Use the **InterfaceIndex** to retrieve the Network Adapter you want.</span></span>

    `"SELECT * FROM Win32_NetworkAdapter WHERE InterfaceIndex=" + insertVariableHere`

## <a name="examples"></a><span data-ttu-id="f6b38-609">範例</span><span class="sxs-lookup"><span data-stu-id="f6b38-609">Examples</span></span>

<span data-ttu-id="f6b38-610">TechNet 元件庫中的 [兩個 WMI](https://Gallery.TechNet.Microsoft.Com/Two-WMI-Functions-94c31b5f) 函式 PowerShell 程式碼範例會使用 **Win32 \_ NetworkAdapter** 來重新建立 Windows [get-netadapter](/powershell/module/netadapter/get-netadapter?view=win10-ps) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6b38-610">The [Two WMI Functions](https://Gallery.TechNet.Microsoft.Com/Two-WMI-Functions-94c31b5f) PowerShell code example in the TechNet Gallery uses **Win32\_NetworkAdapter** to re-create the Windows [Get-NetAdapter](/powershell/module/netadapter/get-netadapter?view=win10-ps) cmdlet.</span></span>

<span data-ttu-id="f6b38-611">[本機/遠端電腦上的 Get-computerinfo 查詢電腦資訊（ (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell 範例（英文）： TechNet 資源庫上的 PowerShell 範例會使用一些硬體和軟體的呼叫，包括 **Win32 \_ NetworkAdapter**，以顯示本機或遠端系統的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f6b38-611">The [Get-ComputerInfo - Query Computer Info From Local/Remote Computers - (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell sample on TechNet Gallery uses a number of calls to hardware and software, including **Win32\_NetworkAdapter**, to display information about a local or remote system.</span></span>

<span data-ttu-id="f6b38-612">下列 C 程式 \# 代碼範例會使用 [Microsoft. 基礎結構](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) 命名空間來抓取本機電腦上目前的網路介面卡。</span><span class="sxs-lookup"><span data-stu-id="f6b38-612">The following C\# code sample uses [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) namespace to retrieve the current network adapters on the local machine.</span></span>


```CSharp
using Microsoft.Management.Infrastructure;
...
static void QueryInstanceFunc()
        {
 
            CimSession session = CimSession.Create("localHost");
            IEnumerable<CimInstance> queryInstance = session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_NetworkAdapter");

            foreach (CimInstance cimObj in queryInstance)
            {
                Console.WriteLine(cimObj.CimInstanceProperties["Name"].ToString());
                Console.WriteLine(cimObj.CimInstanceProperties["Description"].ToString());
                Console.WriteLine();
            }

            Console.ReadLine();
        }
```



<span data-ttu-id="f6b38-613">下列 C 程式 \# 代碼範例使用 https://msdn.microsoft.com/library/system.management.aspx 命名空間來抓取本機電腦上目前的網路介面卡。</span><span class="sxs-lookup"><span data-stu-id="f6b38-613">The following C\# code sample uses https://msdn.microsoft.com/library/system.management.aspx namespace to retrieve the current network adapters on the local machine.</span></span>

> [!Note]  
> <span data-ttu-id="f6b38-614"> https://msdn.microsoft.com/library/system.management.aspx 包含用來存取 WMI 的原始類別;不過，它們會被視為較慢，而且通常不會進行調整，而且也不會調整其 [Microsoft. 基礎結構](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) 的對應專案。</span><span class="sxs-lookup"><span data-stu-id="f6b38-614">https://msdn.microsoft.com/library/system.management.aspx contains the original classes used to access WMI; however, they are considered slower and generally do not scale as well as their [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) counterparts.</span></span>

 


```CSharp
using System.Management;
...
        static void oldSchoolQueryInstanceFunc()
        {

            ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_NetworkAdapter");
            ManagementObjectSearcher searcher = new ManagementObjectSearcher(query);


            ManagementObjectCollection queryCollection = searcher.Get();
            foreach (ManagementObject m in queryCollection)
            {
                Console.WriteLine("ServiceName : {0}", m["Name"]);
                Console.WriteLine("MACAddress : {0}", m["Description"]);
                Console.WriteLine();
            }
            Console.ReadLine();

        }
```



<span data-ttu-id="f6b38-615">下列 VBScript 程式碼範例說明如何在本機電腦上取出目前的網路介面卡。</span><span class="sxs-lookup"><span data-stu-id="f6b38-615">The following VBScript code sample describes how to retrieve the current network adapters on the local machine.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_NetworkAdapter")

For Each objItem in colItems 
    Wscript.Echo "Name: " & objItem.Name
    Wscript.Echo "Description: " & objItem.Description
    Wscript.Echo
Next
```



## <a name="requirements"></a><span data-ttu-id="f6b38-616">規格需求</span><span class="sxs-lookup"><span data-stu-id="f6b38-616">Requirements</span></span>



| <span data-ttu-id="f6b38-617">需求</span><span class="sxs-lookup"><span data-stu-id="f6b38-617">Requirement</span></span> | <span data-ttu-id="f6b38-618">值</span><span class="sxs-lookup"><span data-stu-id="f6b38-618">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6b38-619">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f6b38-619">Minimum supported client</span></span><br/> | <span data-ttu-id="f6b38-620">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f6b38-620">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f6b38-621">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f6b38-621">Minimum supported server</span></span><br/> | <span data-ttu-id="f6b38-622">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f6b38-622">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f6b38-623">命名空間</span><span class="sxs-lookup"><span data-stu-id="f6b38-623">Namespace</span></span><br/>                | <span data-ttu-id="f6b38-624">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f6b38-624">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f6b38-625">MOF</span><span class="sxs-lookup"><span data-stu-id="f6b38-625">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6b38-626"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="f6b38-626"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6b38-627">DLL</span><span class="sxs-lookup"><span data-stu-id="f6b38-627">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6b38-628"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6b38-628"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6b38-629">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f6b38-629">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6b38-630">**CIM \_ NetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="f6b38-630">**CIM\_NetworkAdapter**</span></span>](cim-networkadapter.md)
</dt> <dt>

[<span data-ttu-id="f6b38-631">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="f6b38-631">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="f6b38-632">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="f6b38-632">WMI Tasks: Networking</span></span>](../wmisdk/wmi-tasks--networking.md)
</dt> <dt>

[<span data-ttu-id="f6b38-633">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="f6b38-633">IPv6 and IPv4 Support in WMI</span></span>](../wmisdk/ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 

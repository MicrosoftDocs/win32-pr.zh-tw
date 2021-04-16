---
description: 網路裝置上網路埠的邏輯標記法。
ms.assetid: afcfc93d-174e-43b5-a16f-28937b4bf81a
title: CIM_NetworkPort 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NetworkPort
- CIM_NetworkPort.Speed
- CIM_NetworkPort.OtherNetworkPortType
- CIM_NetworkPort.PortNumber
- CIM_NetworkPort.LinkTechnology
- CIM_NetworkPort.OtherLinkTechnology
- CIM_NetworkPort.PermanentAddress
- CIM_NetworkPort.NetworkAddresses
- CIM_NetworkPort.FullDuplex
- CIM_NetworkPort.AutoSense
- CIM_NetworkPort.SupportedMaximumTransmissionUnit
- CIM_NetworkPort.ActiveMaximumTransmissionUnit
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9e3ac64b55e17d0526527ebbaca168c3f7b289f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194559"
---
# <a name="cim_networkport-class"></a><span data-ttu-id="b458c-103">CIM \_ NetworkPort 類別</span><span class="sxs-lookup"><span data-stu-id="b458c-103">CIM\_NetworkPort class</span></span>

<span data-ttu-id="b458c-104">網路裝置上網路埠的邏輯標記法。</span><span class="sxs-lookup"><span data-stu-id="b458c-104">A logical representation of a network port on a network device.</span></span>

## <a name="syntax"></a><span data-ttu-id="b458c-105">語法</span><span class="sxs-lookup"><span data-stu-id="b458c-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_NetworkPort : CIM_LogicalPort
{
  uint64  Speed;
  string  OtherNetworkPortType;
  uint16  PortNumber;
  uint16  LinkTechnology;
  string  OtherLinkTechnology;
  string  PermanentAddress;
  string  NetworkAddresses[];
  boolean FullDuplex;
  boolean AutoSense;
  uint64  SupportedMaximumTransmissionUnit;
  uint64  ActiveMaximumTransmissionUnit;
};
```

## <a name="members"></a><span data-ttu-id="b458c-106">成員</span><span class="sxs-lookup"><span data-stu-id="b458c-106">Members</span></span>

<span data-ttu-id="b458c-107">**CIM \_ NetworkPort** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b458c-107">The **CIM\_NetworkPort** class has these types of members:</span></span>

-   [<span data-ttu-id="b458c-108">屬性</span><span class="sxs-lookup"><span data-stu-id="b458c-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b458c-109">屬性</span><span class="sxs-lookup"><span data-stu-id="b458c-109">Properties</span></span>

<span data-ttu-id="b458c-110">**CIM \_ NetworkPort** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b458c-110">The **CIM\_NetworkPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b458c-111">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="b458c-111">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b458c-112">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="b458c-112">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b458c-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b458c-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b458c-114">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Bytes" ) ， **PUnit** ( "byte" ) </span><span class="sxs-lookup"><span data-stu-id="b458c-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="b458c-115">埠支援的作用中或已協商的最大傳輸單位 (MTU) 。</span><span class="sxs-lookup"><span data-stu-id="b458c-115">The active or negotiated maximum transmission unit (MTU) that is supported by the port.</span></span>

</dd> <dt>

<span data-ttu-id="b458c-116">**自動感測**</span><span class="sxs-lookup"><span data-stu-id="b458c-116">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b458c-117">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b458c-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b458c-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b458c-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b458c-119">如果埠可以自動判斷連接之網路媒體的速度或其他通訊特性，則 **為 true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="b458c-119">**true** if the port can automatically determine the speed or other communications characteristic of the attached network media; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="b458c-120">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="b458c-120">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b458c-121">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b458c-121">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b458c-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b458c-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b458c-123">如果埠是以全雙工模式運作，則為 **true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="b458c-123">**true** if the port is operating in full duplex mode; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="b458c-124">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="b458c-124">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b458c-125">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b458c-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b458c-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b458c-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b458c-127">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ NetworkPort**.**OtherLinkTechnology**") </span><span class="sxs-lookup"><span data-stu-id="b458c-127">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_NetworkPort**.**OtherLinkTechnology**")</span></span>
</dt> </dl>

<span data-ttu-id="b458c-128">埠所使用的連結技術。</span><span class="sxs-lookup"><span data-stu-id="b458c-128">The link technology used by the port.</span></span> <span data-ttu-id="b458c-129">當設定為 "1" (其他) 時， **OtherLinkTechnology** 屬性會包含連結類型的描述。</span><span class="sxs-lookup"><span data-stu-id="b458c-129">When set to "1" (other), the **OtherLinkTechnology** property contains a description of the link type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b458c-130">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="b458c-130">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b458c-131">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="b458c-131">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="b458c-132">**Ethernet** (2) </span><span class="sxs-lookup"><span data-stu-id="b458c-132">**Ethernet** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IB"></span><span id="ib"></span>

<span data-ttu-id="b458c-133">**IB** (3) </span><span class="sxs-lookup"><span data-stu-id="b458c-133">**IB** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="FC"></span><span id="fc"></span>

<span data-ttu-id="b458c-134">**FC** (4) </span><span class="sxs-lookup"><span data-stu-id="b458c-134">**FC** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

<span data-ttu-id="b458c-135">**FDDI** (5) </span><span class="sxs-lookup"><span data-stu-id="b458c-135">**FDDI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

<span data-ttu-id="b458c-136">**ATM** (6) </span><span class="sxs-lookup"><span data-stu-id="b458c-136">**ATM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

<span data-ttu-id="b458c-137">**權杖環** (7) </span><span class="sxs-lookup"><span data-stu-id="b458c-137">**Token Ring** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>

<span data-ttu-id="b458c-138">**框架轉送** (8) </span><span class="sxs-lookup"><span data-stu-id="b458c-138">**Frame Relay** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

<span data-ttu-id="b458c-139">**紅外線** (9) </span><span class="sxs-lookup"><span data-stu-id="b458c-139">**Infrared** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>

<span data-ttu-id="b458c-140">**藍牙** (10) </span><span class="sxs-lookup"><span data-stu-id="b458c-140">**BlueTooth** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Wireless_LAN"></span><span id="wireless_lan"></span><span id="WIRELESS_LAN"></span>

<span data-ttu-id="b458c-141">**無線區域網路** (11) </span><span class="sxs-lookup"><span data-stu-id="b458c-141">**Wireless LAN** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b458c-142">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="b458c-142">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b458c-143">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="b458c-143">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b458c-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b458c-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b458c-145">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 網路介面卡802埠 \| 001.3 ") </span><span class="sxs-lookup"><span data-stu-id="b458c-145">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Network Adapter 802 Port\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="b458c-146">陣列，其中包含埠的網路位址。</span><span class="sxs-lookup"><span data-stu-id="b458c-146">An array that contains the network addresses for the port.</span></span>

</dd> <dt>

<span data-ttu-id="b458c-147">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="b458c-147">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b458c-148">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b458c-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b458c-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b458c-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b458c-150">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ NetworkPort**.**LinkTechnology**") </span><span class="sxs-lookup"><span data-stu-id="b458c-150">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_NetworkPort**.**LinkTechnology**")</span></span>
</dt> </dl>

<span data-ttu-id="b458c-151">當 **LinkTechnology** 設定為 "1" 時，連結技術 (其他) 。</span><span class="sxs-lookup"><span data-stu-id="b458c-151">The link technology when **LinkTechnology** is set to "1", (other).</span></span>

</dd> <dt>

<span data-ttu-id="b458c-152">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="b458c-152">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b458c-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b458c-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b458c-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b458c-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b458c-155">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( 「**CIM \_ NetworkPort**。**OtherPortType**") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ LogicalPort**](cim-logicalport.md)。**PortType**") </span><span class="sxs-lookup"><span data-stu-id="b458c-155">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM\_NetworkPort**.**OtherPortType**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalPort**](cim-logicalport.md).**PortType**")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="b458c-156">已淘汰的描述：當 **PortType** 屬性包含 1 (其他) 時，埠的模組類型。</span><span class="sxs-lookup"><span data-stu-id="b458c-156">Deprecated description: The module type of the port, when the **PortType** property contains 1 (other).</span></span>

 

<span data-ttu-id="b458c-157">此屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="b458c-157">This property is deprecated.</span></span> <span data-ttu-id="b458c-158">相反地，我們建議 [**CIM \_ LogicalPort**](cim-logicalport.md)類別中的 **PortType** 屬性。</span><span class="sxs-lookup"><span data-stu-id="b458c-158">Instead, we recommend the **PortType** property in the [**CIM\_LogicalPort**](cim-logicalport.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="b458c-159">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="b458c-159">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b458c-160">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b458c-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b458c-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b458c-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b458c-162">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 網路介面卡802埠 \| 001.2 ") </span><span class="sxs-lookup"><span data-stu-id="b458c-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Network Adapter 802 Port\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="b458c-163">硬式編碼在埠中的網路位址。</span><span class="sxs-lookup"><span data-stu-id="b458c-163">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="b458c-164">您可以使用固件升級或軟體設定來變更硬式編碼的位址。</span><span class="sxs-lookup"><span data-stu-id="b458c-164">The hardcoded address can be changed using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="b458c-165">進行這項變更時，應同時更新此屬性。</span><span class="sxs-lookup"><span data-stu-id="b458c-165">When this change is made, this property should be updated at the same time.</span></span> <span data-ttu-id="b458c-166">如果位址不存在， **PermanentAddress** 應該保留空白。</span><span class="sxs-lookup"><span data-stu-id="b458c-166">**PermanentAddress** should be left blank if the address doesn't exist.</span></span>

</dd> <dt>

<span data-ttu-id="b458c-167">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="b458c-167">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b458c-168">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b458c-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b458c-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b458c-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b458c-170">網路埠的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="b458c-170">The port number of the network port.</span></span> <span data-ttu-id="b458c-171">網路埠的編號通常相對於邏輯模組或網路元素。</span><span class="sxs-lookup"><span data-stu-id="b458c-171">Network ports are often numbered relative to either a logical module or a network element.</span></span>

</dd> <dt>

<span data-ttu-id="b458c-172">**速度**</span><span class="sxs-lookup"><span data-stu-id="b458c-172">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b458c-173">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="b458c-173">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b458c-174">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b458c-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b458c-175">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "速度" ) 、 [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "每秒位數" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| Mib-ii ifSpeed "，" MIF。DMTF \| Network Adapter 802 Port \| 001.5 ") ， **PUnit** (" bit/second ") </span><span class="sxs-lookup"><span data-stu-id="b458c-175">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Speed"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|MIB-II.ifSpeed", "MIF.DMTF\|Network Adapter 802 Port\|001.5"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="b458c-176">埠目前的頻寬（以位/秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="b458c-176">The current bandwidth of the port in bits per second.</span></span> <span data-ttu-id="b458c-177">針對因頻寬而異的埠，或無法進行準確估計的埠，此屬性應該包含名義頻寬。</span><span class="sxs-lookup"><span data-stu-id="b458c-177">For ports that vary in bandwidth, or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span>

</dd> <dt>

<span data-ttu-id="b458c-178">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="b458c-178">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b458c-179">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="b458c-179">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b458c-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b458c-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b458c-181">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Bytes" ) ， **PUnit** ( "byte" ) </span><span class="sxs-lookup"><span data-stu-id="b458c-181">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="b458c-182">埠所支援的最大傳輸單位 (MTU) 。</span><span class="sxs-lookup"><span data-stu-id="b458c-182">The maximum transmission unit (MTU) that is supported by the port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b458c-183">規格需求</span><span class="sxs-lookup"><span data-stu-id="b458c-183">Requirements</span></span>



| <span data-ttu-id="b458c-184">需求</span><span class="sxs-lookup"><span data-stu-id="b458c-184">Requirement</span></span> | <span data-ttu-id="b458c-185">值</span><span class="sxs-lookup"><span data-stu-id="b458c-185">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b458c-186">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b458c-186">Minimum supported client</span></span><br/> | <span data-ttu-id="b458c-187">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b458c-187">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="b458c-188">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b458c-188">Minimum supported server</span></span><br/> | <span data-ttu-id="b458c-189">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b458c-189">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="b458c-190">命名空間</span><span class="sxs-lookup"><span data-stu-id="b458c-190">Namespace</span></span><br/>                | <span data-ttu-id="b458c-191">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="b458c-191">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b458c-192">MOF</span><span class="sxs-lookup"><span data-stu-id="b458c-192">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b458c-193"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="b458c-193"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b458c-194">DLL</span><span class="sxs-lookup"><span data-stu-id="b458c-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b458c-195"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b458c-195"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b458c-196">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b458c-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b458c-197">**CIM \_ LogicalPort**</span><span class="sxs-lookup"><span data-stu-id="b458c-197">**CIM\_LogicalPort**</span></span>](cim-logicalport.md)
</dt> </dl>

 


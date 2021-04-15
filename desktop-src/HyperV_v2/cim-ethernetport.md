---
description: 表示乙太網路埠。
ms.assetid: c9a148c2-cf02-466f-b8ca-b1bf616d75dc
title: CIM_EthernetPort 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EthernetPort
- CIM_EthernetPort.PortType
- CIM_EthernetPort.NetworkAddresses
- CIM_EthernetPort.MaxDataSize
- CIM_EthernetPort.Capabilities
- CIM_EthernetPort.CapabilityDescriptions
- CIM_EthernetPort.EnabledCapabilities
- CIM_EthernetPort.OtherEnabledCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a44e93f84178fa2714d3c823735b3d90922e04be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510903"
---
# <a name="cim_ethernetport-class"></a><span data-ttu-id="2c5e4-103">CIM \_ EthernetPort 類別</span><span class="sxs-lookup"><span data-stu-id="2c5e4-103">CIM\_EthernetPort class</span></span>

<span data-ttu-id="2c5e4-104">表示乙太網路埠。</span><span class="sxs-lookup"><span data-stu-id="2c5e4-104">Represents an ethernet port.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c5e4-105">語法</span><span class="sxs-lookup"><span data-stu-id="2c5e4-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_EthernetPort : CIM_NetworkPort
{
  uint16 PortType;
  string NetworkAddresses[];
  uint32 MaxDataSize;
  uint16 Capabilities[];
  string CapabilityDescriptions[];
  uint16 EnabledCapabilities[];
  string OtherEnabledCapabilities[];
};
```

## <a name="members"></a><span data-ttu-id="2c5e4-106">成員</span><span class="sxs-lookup"><span data-stu-id="2c5e4-106">Members</span></span>

<span data-ttu-id="2c5e4-107">**CIM \_ EthernetPort** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2c5e4-107">The **CIM\_EthernetPort** class has these types of members:</span></span>

-   [<span data-ttu-id="2c5e4-108">屬性</span><span class="sxs-lookup"><span data-stu-id="2c5e4-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2c5e4-109">屬性</span><span class="sxs-lookup"><span data-stu-id="2c5e4-109">Properties</span></span>

<span data-ttu-id="2c5e4-110">**CIM \_ EthernetPort** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2c5e4-110">The **CIM\_EthernetPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2c5e4-111">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="2c5e4-111">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c5e4-112">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="2c5e4-112">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2c5e4-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2c5e4-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c5e4-114">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ EthernetPort**。**CapabilityDescriptions**") </span><span class="sxs-lookup"><span data-stu-id="2c5e4-114">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EthernetPort**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="2c5e4-115">Ethernet 埠的功能。</span><span class="sxs-lookup"><span data-stu-id="2c5e4-115">The capabilities of the ethernet port.</span></span>

> [!Note]  
> <span data-ttu-id="2c5e4-116">如果啟用容錯移轉或負載平衡功能，則應該也要定義 [**cim \_ SpareGroup**](/windows/desktop/CIMWin32Prov/cim-sparegroup) (容錯移轉) 或 [**cim \_ ExtraCapacityGroup**](/windows/desktop/CIMWin32Prov/cim-extracapacitygroup) (負載平衡) 物件，以完整描述該功能。</span><span class="sxs-lookup"><span data-stu-id="2c5e4-116">If failover or load balancing capabilities are enabled, a [**CIM\_SpareGroup**](/windows/desktop/CIMWin32Prov/cim-sparegroup) (failover) or [**CIM\_ExtraCapacityGroup**](/windows/desktop/CIMWin32Prov/cim-extracapacitygroup) (load balancing) object should also be defined to completely describe the capability.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2c5e4-117">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="2c5e4-117">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2c5e4-118">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="2c5e4-118">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>

<span data-ttu-id="2c5e4-119">**AlertOnLan** (2) </span><span class="sxs-lookup"><span data-stu-id="2c5e4-119">**AlertOnLan** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>

<span data-ttu-id="2c5e4-120">**WakeOnLan** (3) </span><span class="sxs-lookup"><span data-stu-id="2c5e4-120">**WakeOnLan** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>

<span data-ttu-id="2c5e4-121">**容錯移轉** (4) </span><span class="sxs-lookup"><span data-stu-id="2c5e4-121">**FailOver** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>

<span data-ttu-id="2c5e4-122">**負載平衡** (5) </span><span class="sxs-lookup"><span data-stu-id="2c5e4-122">**LoadBalancing** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2c5e4-123">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="2c5e4-123">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c5e4-124">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="2c5e4-124">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2c5e4-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2c5e4-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c5e4-126">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ EthernetPort**。**功能**") </span><span class="sxs-lookup"><span data-stu-id="2c5e4-126">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EthernetPort**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="2c5e4-127">自由格式字串的陣列，可針對功能陣列中所指出的任何功能提供更詳細的說明。</span><span class="sxs-lookup"><span data-stu-id="2c5e4-127">An array of free-form strings that provides more detailed explanations for any of the features that are indicated in the Capabilities array.</span></span> <span data-ttu-id="2c5e4-128">這個陣列中的專案會對應至功能陣列中的專案。</span><span class="sxs-lookup"><span data-stu-id="2c5e4-128">The items in this array correspond to the items in the Capabilities array.</span></span>

</dd> <dt>

<span data-ttu-id="2c5e4-129">**EnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="2c5e4-129">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c5e4-130">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="2c5e4-130">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2c5e4-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2c5e4-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c5e4-132">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ EthernetPort**。**功能**"、"**CIM \_ EthernetPort**。**OtherEnabledCapabilities**") </span><span class="sxs-lookup"><span data-stu-id="2c5e4-132">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EthernetPort**.**Capabilities**", "**CIM\_EthernetPort**.**OtherEnabledCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="2c5e4-133">指出功能陣列中啟用的功能。</span><span class="sxs-lookup"><span data-stu-id="2c5e4-133">Indicates which capabilities are enabled in the Capabilities array.</span></span> <span data-ttu-id="2c5e4-134">這個陣列中的專案會對應至功能陣列中的專案。</span><span class="sxs-lookup"><span data-stu-id="2c5e4-134">The items in this array correspond to the items in the Capabilities array.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2c5e4-135">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="2c5e4-135">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2c5e4-136">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="2c5e4-136">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>

<span data-ttu-id="2c5e4-137">**AlertOnLan** (2) </span><span class="sxs-lookup"><span data-stu-id="2c5e4-137">**AlertOnLan** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>

<span data-ttu-id="2c5e4-138">**WakeOnLan** (3) </span><span class="sxs-lookup"><span data-stu-id="2c5e4-138">**WakeOnLan** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>

<span data-ttu-id="2c5e4-139">**容錯移轉** (4) </span><span class="sxs-lookup"><span data-stu-id="2c5e4-139">**FailOver** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>

<span data-ttu-id="2c5e4-140">**負載平衡** (5) </span><span class="sxs-lookup"><span data-stu-id="2c5e4-140">**LoadBalancing** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2c5e4-141">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="2c5e4-141">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c5e4-142">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2c5e4-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c5e4-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2c5e4-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c5e4-144">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| BRIDGE-dot1dTpPortMaxInfo ") </span><span class="sxs-lookup"><span data-stu-id="2c5e4-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dTpPortMaxInfo")</span></span>
</dt> </dl>

<span data-ttu-id="2c5e4-145">將接收或傳送的資訊 (非 MAC) 欄位的大小上限。</span><span class="sxs-lookup"><span data-stu-id="2c5e4-145">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span>

</dd> <dt>

<span data-ttu-id="2c5e4-146">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="2c5e4-146">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c5e4-147">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="2c5e4-147">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2c5e4-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2c5e4-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c5e4-149">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "NetworkAddresses" ) </span><span class="sxs-lookup"><span data-stu-id="2c5e4-149">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NetworkAddresses")</span></span>
</dt> </dl>

<span data-ttu-id="2c5e4-150">指派給埠的網路位址。</span><span class="sxs-lookup"><span data-stu-id="2c5e4-150">The network addresses assigned to the port.</span></span> <span data-ttu-id="2c5e4-151">位址是 802.3 MAC，格式為十二個十六進位數位 (例如 "010203040506" ) ，其中每一組數位代表以標準位順序表示之 MAC 位址的六個八位組中的其中一個。</span><span class="sxs-lookup"><span data-stu-id="2c5e4-151">The address is a 802.3 MAC that is formatted as twelve hexadecimal digits (for example, "010203040506"), where each pair of digits represents one of the six octets of the MAC address in canonical bit order.</span></span>

</dd> <dt>

<span data-ttu-id="2c5e4-152">**OtherEnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="2c5e4-152">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c5e4-153">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="2c5e4-153">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2c5e4-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2c5e4-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c5e4-155">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ EthernetPort**。**EnabledCapabilities**") </span><span class="sxs-lookup"><span data-stu-id="2c5e4-155">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EthernetPort**.**EnabledCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="2c5e4-156">自由格式字串的陣列，可針對設定為 1 (其他) 的任何 **EnabledCapabilities** 陣列專案，提供更詳細的說明。</span><span class="sxs-lookup"><span data-stu-id="2c5e4-156">An array of free-form strings that provide more detailed explanations for any of the **EnabledCapabilities** array items that are set to 1 (Other).</span></span> <span data-ttu-id="2c5e4-157">這個陣列中的專案會對應至 **EnabledCapabilities** 陣列中的專案。</span><span class="sxs-lookup"><span data-stu-id="2c5e4-157">The items in this array correspond to the items in the **EnabledCapabilities** array.</span></span>

</dd> <dt>

<span data-ttu-id="2c5e4-158">**PortType**</span><span class="sxs-lookup"><span data-stu-id="2c5e4-158">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c5e4-159">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2c5e4-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2c5e4-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2c5e4-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c5e4-161">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PortType" ) </span><span class="sxs-lookup"><span data-stu-id="2c5e4-161">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PortType")</span></span>
</dt> </dl>

<span data-ttu-id="2c5e4-162">在埠上啟用的模式。</span><span class="sxs-lookup"><span data-stu-id="2c5e4-162">The mode that is enabled on the port.</span></span> <span data-ttu-id="2c5e4-163">當設定為1時 (其他) ， **OtherPortType** 屬性會描述模式。</span><span class="sxs-lookup"><span data-stu-id="2c5e4-163">When set to 1 (Other), the **OtherPortType** property describes the mode.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2c5e4-164">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="2c5e4-164">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2c5e4-165">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="2c5e4-165">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="10BaseT"></span><span id="10baset"></span><span id="10BASET"></span>

<span data-ttu-id="2c5e4-166">**10baset** (50) </span><span class="sxs-lookup"><span data-stu-id="2c5e4-166">**10BaseT** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>

<span data-ttu-id="2c5e4-167">**10-100BaseT** (51) </span><span class="sxs-lookup"><span data-stu-id="2c5e4-167">**10-100BaseT** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>

<span data-ttu-id="2c5e4-168">**100BaseT** (52) </span><span class="sxs-lookup"><span data-stu-id="2c5e4-168">**100BaseT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>

<span data-ttu-id="2c5e4-169">**1000BaseT** (53) </span><span class="sxs-lookup"><span data-stu-id="2c5e4-169">**1000BaseT** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>

<span data-ttu-id="2c5e4-170">**2500BaseT** (54) </span><span class="sxs-lookup"><span data-stu-id="2c5e4-170">**2500BaseT** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>

<span data-ttu-id="2c5e4-171">**10GBaseT** (55) </span><span class="sxs-lookup"><span data-stu-id="2c5e4-171">**10GBaseT** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>

<span data-ttu-id="2c5e4-172">**10gbase-t-CX4** (56) </span><span class="sxs-lookup"><span data-stu-id="2c5e4-172">**10GBase-CX4** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="100Base-FX"></span><span id="100base-fx"></span><span id="100BASE-FX"></span>

<span data-ttu-id="2c5e4-173">**100base-tx-FX** (100) </span><span class="sxs-lookup"><span data-stu-id="2c5e4-173">**100Base-FX** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>

<span data-ttu-id="2c5e4-174">**100base-tx-SX** (101) </span><span class="sxs-lookup"><span data-stu-id="2c5e4-174">**100Base-SX** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>

<span data-ttu-id="2c5e4-175">**1000base-t-SX** (102) </span><span class="sxs-lookup"><span data-stu-id="2c5e4-175">**1000Base-SX** (102)</span></span>


</dt> <dd></dd> <dt>

<span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>

<span data-ttu-id="2c5e4-176">**1000base-t-LX** (103) </span><span class="sxs-lookup"><span data-stu-id="2c5e4-176">**1000Base-LX** (103)</span></span>


</dt> <dd></dd> <dt>

<span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>

<span data-ttu-id="2c5e4-177">**1000base-t-CX** (104) </span><span class="sxs-lookup"><span data-stu-id="2c5e4-177">**1000Base-CX** (104)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>

<span data-ttu-id="2c5e4-178">**10gbase-t-SR** (105) </span><span class="sxs-lookup"><span data-stu-id="2c5e4-178">**10GBase-SR** (105)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>

<span data-ttu-id="2c5e4-179">**10gbase-t-SW** (106) </span><span class="sxs-lookup"><span data-stu-id="2c5e4-179">**10GBase-SW** (106)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>

<span data-ttu-id="2c5e4-180">**LX4** (107) </span><span class="sxs-lookup"><span data-stu-id="2c5e4-180">**10GBase-LX4** (107)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>

<span data-ttu-id="2c5e4-181">**10gbase-t-LR** (108) </span><span class="sxs-lookup"><span data-stu-id="2c5e4-181">**10GBase-LR** (108)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>

<span data-ttu-id="2c5e4-182">**LW** (109) </span><span class="sxs-lookup"><span data-stu-id="2c5e4-182">**10GBase-LW** (109)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>

<span data-ttu-id="2c5e4-183">**10gbase-t-ER** (110) </span><span class="sxs-lookup"><span data-stu-id="2c5e4-183">**10GBase-ER** (110)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>

<span data-ttu-id="2c5e4-184"> (111) **的**</span><span class="sxs-lookup"><span data-stu-id="2c5e4-184">**10GBase-EW** (111)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="2c5e4-185">**廠商保留** (16，000. 65535) </span><span class="sxs-lookup"><span data-stu-id="2c5e4-185">**Vendor Reserved** (16000..65535)</span></span>


<span data-ttu-id="2c5e4-186"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="2c5e4-186"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="2c5e4-187">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c5e4-187">Requirements</span></span>



| <span data-ttu-id="2c5e4-188">需求</span><span class="sxs-lookup"><span data-stu-id="2c5e4-188">Requirement</span></span> | <span data-ttu-id="2c5e4-189">值</span><span class="sxs-lookup"><span data-stu-id="2c5e4-189">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c5e4-190">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2c5e4-190">Minimum supported client</span></span><br/> | <span data-ttu-id="2c5e4-191">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2c5e4-191">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="2c5e4-192">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2c5e4-192">Minimum supported server</span></span><br/> | <span data-ttu-id="2c5e4-193">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2c5e4-193">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="2c5e4-194">命名空間</span><span class="sxs-lookup"><span data-stu-id="2c5e4-194">Namespace</span></span><br/>                | <span data-ttu-id="2c5e4-195">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="2c5e4-195">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2c5e4-196">MOF</span><span class="sxs-lookup"><span data-stu-id="2c5e4-196">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c5e4-197"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="2c5e4-197"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2c5e4-198">DLL</span><span class="sxs-lookup"><span data-stu-id="2c5e4-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c5e4-199"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2c5e4-199"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2c5e4-200">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c5e4-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c5e4-201">**CIM \_ NetworkPort**</span><span class="sxs-lookup"><span data-stu-id="2c5e4-201">**CIM\_NetworkPort**</span></span>](cim-networkport.md)
</dt> </dl>

 


---
description: 代表符合 IEEE 802.11 規格系列的無線區域網路通訊裝置。
ms.assetid: c4e3345f-5c7d-4d1d-9a94-64112d7334ff
title: CIM_WiFiPort 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_WiFiPort
- CIM_WiFiPort.Speed
- CIM_WiFiPort.MaxSpeed
- CIM_WiFiPort.PortType
- CIM_WiFiPort.PermanentAddress
- CIM_WiFiPort.NetworkAddresses
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 098bd0a3795f3e8e0531be5286a65b79d9f6ee0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849663"
---
# <a name="cim_wifiport-class"></a><span data-ttu-id="b1bc6-103">CIM \_ WiFiPort 類別</span><span class="sxs-lookup"><span data-stu-id="b1bc6-103">CIM\_WiFiPort class</span></span>

<span data-ttu-id="b1bc6-104">代表符合 IEEE 802.11 規格系列的無線區域網路通訊裝置。</span><span class="sxs-lookup"><span data-stu-id="b1bc6-104">Represents a wireless local area network communications device that conforms to the IEEE 802.11 series of specifications.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1bc6-105">語法</span><span class="sxs-lookup"><span data-stu-id="b1bc6-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_WiFiPort : CIM_NetworkPort
{
  uint64 Speed;
  uint64 MaxSpeed;
  uint16 PortType;
  string PermanentAddress;
  string NetworkAddresses[];
};
```

## <a name="members"></a><span data-ttu-id="b1bc6-106">成員</span><span class="sxs-lookup"><span data-stu-id="b1bc6-106">Members</span></span>

<span data-ttu-id="b1bc6-107">**CIM \_ WiFiPort** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b1bc6-107">The **CIM\_WiFiPort** class has these types of members:</span></span>

-   [<span data-ttu-id="b1bc6-108">屬性</span><span class="sxs-lookup"><span data-stu-id="b1bc6-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b1bc6-109">屬性</span><span class="sxs-lookup"><span data-stu-id="b1bc6-109">Properties</span></span>

<span data-ttu-id="b1bc6-110">**CIM \_ WiFiPort** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b1bc6-110">The **CIM\_WiFiPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b1bc6-111">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="b1bc6-111">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1bc6-112">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="b1bc6-112">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b1bc6-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1bc6-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1bc6-114">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MaxSpeed" ) </span><span class="sxs-lookup"><span data-stu-id="b1bc6-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxSpeed")</span></span>
</dt> </dl>

<span data-ttu-id="b1bc6-115">支援的最大頻寬（以每秒位數為單位），以 **PortType** 屬性中指定的作業模式為基礎。</span><span class="sxs-lookup"><span data-stu-id="b1bc6-115">The maximum supported bandwidth, in bits per second, based on the operating mode specified in the **PortType** property.</span></span> <span data-ttu-id="b1bc6-116">例如，如果 **PortType** 包含 "71" (802.11 b) ，則 **MaxSpeed** 是 "11000000"。</span><span class="sxs-lookup"><span data-stu-id="b1bc6-116">For example, **MaxSpeed** is "11000000" if **PortType** contains "71" (802.11b).</span></span>

</dd> <dt>

<span data-ttu-id="b1bc6-117">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="b1bc6-117">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1bc6-118">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="b1bc6-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b1bc6-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1bc6-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1bc6-120">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "NetworkAddresses" ) </span><span class="sxs-lookup"><span data-stu-id="b1bc6-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NetworkAddresses")</span></span>
</dt> </dl>

<span data-ttu-id="b1bc6-121">包含 IEEE 802 EUI-48 MAC 位址的陣列。</span><span class="sxs-lookup"><span data-stu-id="b1bc6-121">An array that contains the IEEE 802 EUI-48 MAC addresses.</span></span> <span data-ttu-id="b1bc6-122">MAC 位址的格式為十二個十六進位數位，每一組代表以標準位順序表示之 MAC 位址的六個八位組中的其中一個。</span><span class="sxs-lookup"><span data-stu-id="b1bc6-122">The MAC address is formatted as twelve hexadecimal digits, with each pair representing one of the six octets of the MAC address in canonical bit order.</span></span>

</dd> <dt>

<span data-ttu-id="b1bc6-123">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="b1bc6-123">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1bc6-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b1bc6-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1bc6-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1bc6-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1bc6-126">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PermanentAddress" ) </span><span class="sxs-lookup"><span data-stu-id="b1bc6-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PermanentAddress")</span></span>
</dt> </dl>

<span data-ttu-id="b1bc6-127">埠的 IEEE 802 EUI-48 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="b1bc6-127">The IEEE 802 EUI-48 MAC address of the port.</span></span> <span data-ttu-id="b1bc6-128">MAC 位址的格式為十二個十六進位數位，每一組代表以標準位順序表示之 MAC 位址的六個八位組中的其中一個。</span><span class="sxs-lookup"><span data-stu-id="b1bc6-128">The MAC address is formatted as twelve hexadecimal digits, with each pair representing one of the six octets of the MAC address in canonical bit order.</span></span>

</dd> <dt>

<span data-ttu-id="b1bc6-129">**PortType**</span><span class="sxs-lookup"><span data-stu-id="b1bc6-129">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1bc6-130">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b1bc6-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b1bc6-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1bc6-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1bc6-132">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PortType" ) </span><span class="sxs-lookup"><span data-stu-id="b1bc6-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PortType")</span></span>
</dt> </dl>

<span data-ttu-id="b1bc6-133">在埠上啟用的802.11 操作模式。</span><span class="sxs-lookup"><span data-stu-id="b1bc6-133">The 802.11 operating mode that is enabled on the port.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b1bc6-134">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="b1bc6-134">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b1bc6-135">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="b1bc6-135">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="802.11a"></span><span id="802.11A"></span>

<span data-ttu-id="b1bc6-136">**802.11 a** (70) </span><span class="sxs-lookup"><span data-stu-id="b1bc6-136">**802.11a** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="802.11b"></span><span id="802.11B"></span>

<span data-ttu-id="b1bc6-137">**802.11 b** (71) </span><span class="sxs-lookup"><span data-stu-id="b1bc6-137">**802.11b** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="802.11g"></span><span id="802.11G"></span>

<span data-ttu-id="b1bc6-138">**802.11 g** (72) </span><span class="sxs-lookup"><span data-stu-id="b1bc6-138">**802.11g** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="802.11n"></span><span id="802.11N"></span>

<span data-ttu-id="b1bc6-139">**802.11 n** (73) </span><span class="sxs-lookup"><span data-stu-id="b1bc6-139">**802.11n** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="b1bc6-140">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="b1bc6-140">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="b1bc6-141">**廠商保留** (16000 ) </span><span class="sxs-lookup"><span data-stu-id="b1bc6-141">**Vendor Reserved** (16000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b1bc6-142">**速度**</span><span class="sxs-lookup"><span data-stu-id="b1bc6-142">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1bc6-143">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="b1bc6-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b1bc6-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1bc6-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1bc6-145">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "速度" ) </span><span class="sxs-lookup"><span data-stu-id="b1bc6-145">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Speed")</span></span>
</dt> </dl>

<span data-ttu-id="b1bc6-146">收到目前 PPDU (PLCP (實體層聚合通訊協定) 通訊協定資料單位) 的資料速率（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="b1bc6-146">The data rate at which the current PPDU (PLCP (Physical Layer Convergence Protocol) Protocol Data Unit) was received, in bits per second.</span></span> <span data-ttu-id="b1bc6-147">此值會在每個 PLCP 畫面格的 PLCP 標頭的前4個位進行編碼。</span><span class="sxs-lookup"><span data-stu-id="b1bc6-147">This value is encoded in the first 4 bits of the PLCP header in each PLCP frame.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b1bc6-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="b1bc6-148">Requirements</span></span>



| <span data-ttu-id="b1bc6-149">需求</span><span class="sxs-lookup"><span data-stu-id="b1bc6-149">Requirement</span></span> | <span data-ttu-id="b1bc6-150">值</span><span class="sxs-lookup"><span data-stu-id="b1bc6-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1bc6-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b1bc6-151">Minimum supported client</span></span><br/> | <span data-ttu-id="b1bc6-152">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b1bc6-152">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="b1bc6-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b1bc6-153">Minimum supported server</span></span><br/> | <span data-ttu-id="b1bc6-154">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b1bc6-154">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="b1bc6-155">命名空間</span><span class="sxs-lookup"><span data-stu-id="b1bc6-155">Namespace</span></span><br/>                | <span data-ttu-id="b1bc6-156">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="b1bc6-156">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b1bc6-157">MOF</span><span class="sxs-lookup"><span data-stu-id="b1bc6-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b1bc6-158"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="b1bc6-158"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b1bc6-159">DLL</span><span class="sxs-lookup"><span data-stu-id="b1bc6-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1bc6-160"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b1bc6-160"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b1bc6-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b1bc6-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1bc6-162">**CIM \_ NetworkPort**</span><span class="sxs-lookup"><span data-stu-id="b1bc6-162">**CIM\_NetworkPort**</span></span>](cim-networkport.md)
</dt> </dl>

 


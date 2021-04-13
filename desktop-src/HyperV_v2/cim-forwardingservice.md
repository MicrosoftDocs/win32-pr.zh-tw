---
description: 代表網路流量的轉送服務。 服務會藉由捨棄封包或將封包傳送至其他通訊協定端點，來處理其接收的通訊協定端點。
ms.assetid: 366ae2bf-a436-4ad2-b212-39958a7fbc43
title: CIM_ForwardingService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ForwardingService
- CIM_ForwardingService.ProtocolType
- CIM_ForwardingService.OtherProtocolType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 12ebb33d6c63b637c9342bd7a869993019abb26b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386081"
---
# <a name="cim_forwardingservice-class"></a><span data-ttu-id="0b628-104">CIM \_ ForwardingService 類別</span><span class="sxs-lookup"><span data-stu-id="0b628-104">CIM\_ForwardingService class</span></span>

<span data-ttu-id="0b628-105">代表網路流量的轉送服務。</span><span class="sxs-lookup"><span data-stu-id="0b628-105">Represents a forwarding service for network traffic.</span></span> <span data-ttu-id="0b628-106">服務會藉由捨棄封包或將封包傳送至其他通訊協定端點，來處理其接收的通訊協定端點。</span><span class="sxs-lookup"><span data-stu-id="0b628-106">The service processes packets received protocol endpoints by discarding them, or sending the packets to other protocol endpoints.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b628-107">語法</span><span class="sxs-lookup"><span data-stu-id="0b628-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::RoutingForwarding"), AMENDMENT]
class CIM_ForwardingService : CIM_NetworkService
{
  uint16 ProtocolType;
  string OtherProtocolType;
};
```

## <a name="members"></a><span data-ttu-id="0b628-108">成員</span><span class="sxs-lookup"><span data-stu-id="0b628-108">Members</span></span>

<span data-ttu-id="0b628-109">**CIM \_ ForwardingService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0b628-109">The **CIM\_ForwardingService** class has these types of members:</span></span>

-   [<span data-ttu-id="0b628-110">屬性</span><span class="sxs-lookup"><span data-stu-id="0b628-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0b628-111">屬性</span><span class="sxs-lookup"><span data-stu-id="0b628-111">Properties</span></span>

<span data-ttu-id="0b628-112">**CIM \_ ForwardingService** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0b628-112">The **CIM\_ForwardingService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0b628-113">**OtherProtocolType**</span><span class="sxs-lookup"><span data-stu-id="0b628-113">**OtherProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b628-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b628-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b628-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b628-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b628-116">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (32) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ ForwardingService**。**ProtocolType**") </span><span class="sxs-lookup"><span data-stu-id="0b628-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ForwardingService**.**ProtocolType**")</span></span>
</dt> </dl>

<span data-ttu-id="0b628-117">定義 **ProtocolType** 屬性的值為 1 (其他) 時要轉寄的通訊協定類型。</span><span class="sxs-lookup"><span data-stu-id="0b628-117">Defines the type of protocol to forward when the value of the **ProtocolType** property is 1 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="0b628-118">**ProtocolType**</span><span class="sxs-lookup"><span data-stu-id="0b628-118">**ProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b628-119">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0b628-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b628-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b628-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b628-121">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ ForwardingService**.**OtherProtocolType**") </span><span class="sxs-lookup"><span data-stu-id="0b628-121">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ForwardingService**.**OtherProtocolType**")</span></span>
</dt> </dl>

<span data-ttu-id="0b628-122">要轉送的通訊協定類型。</span><span class="sxs-lookup"><span data-stu-id="0b628-122">The type of protocol to forward.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0b628-123">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="0b628-123">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0b628-124">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="0b628-124">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

<span data-ttu-id="0b628-125">**IPv4** (2) </span><span class="sxs-lookup"><span data-stu-id="0b628-125">**IPv4** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

<span data-ttu-id="0b628-126">**IPv6** (3) </span><span class="sxs-lookup"><span data-stu-id="0b628-126">**IPv6** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4_IPv6"></span><span id="ipv4_ipv6"></span><span id="IPV4_IPV6"></span>

<span data-ttu-id="0b628-127">**IPv4/IPv6** (4) </span><span class="sxs-lookup"><span data-stu-id="0b628-127">**IPv4/IPv6** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

<span data-ttu-id="0b628-128">**IPX** (5) </span><span class="sxs-lookup"><span data-stu-id="0b628-128">**IPX** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="AppleTalk"></span><span id="appletalk"></span><span id="APPLETALK"></span>

<span data-ttu-id="0b628-129">**AppleTalk** (6) </span><span class="sxs-lookup"><span data-stu-id="0b628-129">**AppleTalk** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="DECnet"></span><span id="decnet"></span><span id="DECNET"></span>

<span data-ttu-id="0b628-130">**DECnet** (7) </span><span class="sxs-lookup"><span data-stu-id="0b628-130">**DECnet** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

<span data-ttu-id="0b628-131">**SNA** (8) </span><span class="sxs-lookup"><span data-stu-id="0b628-131">**SNA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="CONP"></span><span id="conp"></span>

<span data-ttu-id="0b628-132">**CONP** (9) </span><span class="sxs-lookup"><span data-stu-id="0b628-132">**CONP** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="CLNP"></span><span id="clnp"></span>

<span data-ttu-id="0b628-133">**CLNP** (10) </span><span class="sxs-lookup"><span data-stu-id="0b628-133">**CLNP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="VINES"></span><span id="vines"></span>

<span data-ttu-id="0b628-134">**VINES** (11) </span><span class="sxs-lookup"><span data-stu-id="0b628-134">**VINES** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="XNS"></span><span id="xns"></span>

<span data-ttu-id="0b628-135">**XNS** (12) </span><span class="sxs-lookup"><span data-stu-id="0b628-135">**XNS** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

<span data-ttu-id="0b628-136">**ATM** (13) </span><span class="sxs-lookup"><span data-stu-id="0b628-136">**ATM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>

<span data-ttu-id="0b628-137">**框架轉送** (14) </span><span class="sxs-lookup"><span data-stu-id="0b628-137">**Frame Relay** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="0b628-138">**Ethernet** (15) </span><span class="sxs-lookup"><span data-stu-id="0b628-138">**Ethernet** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="TokenRing"></span><span id="tokenring"></span><span id="TOKENRING"></span>

<span data-ttu-id="0b628-139">**TokenRing** (16) </span><span class="sxs-lookup"><span data-stu-id="0b628-139">**TokenRing** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

<span data-ttu-id="0b628-140">**FDDI** (17) </span><span class="sxs-lookup"><span data-stu-id="0b628-140">**FDDI** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Infiniband"></span><span id="infiniband"></span><span id="INFINIBAND"></span>

<span data-ttu-id="0b628-141">未 **(18**) </span><span class="sxs-lookup"><span data-stu-id="0b628-141">**Infiniband** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Fibre_Channel"></span><span id="fibre_channel"></span><span id="FIBRE_CHANNEL"></span>

<span data-ttu-id="0b628-142">**光纖通道** (19) </span><span class="sxs-lookup"><span data-stu-id="0b628-142">**Fibre Channel** (19)</span></span>


<span data-ttu-id="0b628-143"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0b628-143"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="0b628-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="0b628-144">Requirements</span></span>



| <span data-ttu-id="0b628-145">需求</span><span class="sxs-lookup"><span data-stu-id="0b628-145">Requirement</span></span> | <span data-ttu-id="0b628-146">值</span><span class="sxs-lookup"><span data-stu-id="0b628-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b628-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0b628-147">Minimum supported client</span></span><br/> | <span data-ttu-id="0b628-148">Windows 8</span><span class="sxs-lookup"><span data-stu-id="0b628-148">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="0b628-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0b628-149">Minimum supported server</span></span><br/> | <span data-ttu-id="0b628-150">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0b628-150">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="0b628-151">命名空間</span><span class="sxs-lookup"><span data-stu-id="0b628-151">Namespace</span></span><br/>                | <span data-ttu-id="0b628-152">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="0b628-152">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0b628-153">MOF</span><span class="sxs-lookup"><span data-stu-id="0b628-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b628-154"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="0b628-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b628-155">DLL</span><span class="sxs-lookup"><span data-stu-id="0b628-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b628-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0b628-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0b628-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0b628-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b628-158">**CIM \_ NetworkService**</span><span class="sxs-lookup"><span data-stu-id="0b628-158">**CIM\_NetworkService**</span></span>](cim-networkservice.md)
</dt> </dl>

 


---
description: 可以連接到 LAN 以傳送及接收資料框架的通訊端點。 LAN 端點包括乙太網路、權杖環和 FDDI 介面。
ms.assetid: c69464cf-00a9-476d-a494-2d7d65776334
title: CIM_LANEndpoint 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LANEndpoint
- CIM_LANEndpoint.LANID
- CIM_LANEndpoint.LANType
- CIM_LANEndpoint.OtherLANType
- CIM_LANEndpoint.MACAddress
- CIM_LANEndpoint.AliasAddresses
- CIM_LANEndpoint.GroupAddresses
- CIM_LANEndpoint.MaxDataSize
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c924d175cb48e53346daff59a6317a4a0f241f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992619"
---
# <a name="cim_lanendpoint-class"></a><span data-ttu-id="42d0e-104">CIM \_ LANEndpoint 類別</span><span class="sxs-lookup"><span data-stu-id="42d0e-104">CIM\_LANEndpoint class</span></span>

<span data-ttu-id="42d0e-105">可以連接到 LAN 以傳送及接收資料框架的通訊端點。</span><span class="sxs-lookup"><span data-stu-id="42d0e-105">A communication endpoint that can connect to a LAN to send and receive data frames.</span></span> <span data-ttu-id="42d0e-106">LAN 端點包括乙太網路、權杖環和 FDDI 介面。</span><span class="sxs-lookup"><span data-stu-id="42d0e-106">LAN endpoints include ethernet, token Ring, and FDDI interfaces.</span></span>

## <a name="syntax"></a><span data-ttu-id="42d0e-107">語法</span><span class="sxs-lookup"><span data-stu-id="42d0e-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::ProtocolEndpoints"), AMENDMENT]
class CIM_LANEndpoint : CIM_ProtocolEndpoint
{
  string LANID;
  uint16 LANType;
  string OtherLANType;
  string MACAddress;
  string AliasAddresses[];
  string GroupAddresses[];
  uint32 MaxDataSize;
};
```

## <a name="members"></a><span data-ttu-id="42d0e-108">成員</span><span class="sxs-lookup"><span data-stu-id="42d0e-108">Members</span></span>

<span data-ttu-id="42d0e-109">**CIM \_ LANEndpoint** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="42d0e-109">The **CIM\_LANEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="42d0e-110">屬性</span><span class="sxs-lookup"><span data-stu-id="42d0e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="42d0e-111">屬性</span><span class="sxs-lookup"><span data-stu-id="42d0e-111">Properties</span></span>

<span data-ttu-id="42d0e-112">**CIM \_ LANEndpoint** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="42d0e-112">The **CIM\_LANEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="42d0e-113">**AliasAddresses**</span><span class="sxs-lookup"><span data-stu-id="42d0e-113">**AliasAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42d0e-114">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="42d0e-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="42d0e-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42d0e-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42d0e-116">陣列，其中包含可用來與 LAN 端點通訊的其他單播位址。</span><span class="sxs-lookup"><span data-stu-id="42d0e-116">An array that contains other unicast addresses that may be used to communicate with the LAN endpoint.</span></span>

</dd> <dt>

<span data-ttu-id="42d0e-117">**GroupAddresses**</span><span class="sxs-lookup"><span data-stu-id="42d0e-117">**GroupAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42d0e-118">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="42d0e-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="42d0e-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42d0e-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42d0e-120">陣列，包含 LAN 端點接聽的多播位址。</span><span class="sxs-lookup"><span data-stu-id="42d0e-120">An array that contains the multicast addresses to which the LAN endpoint listens.</span></span>

</dd> <dt>

<span data-ttu-id="42d0e-121">**LANID**</span><span class="sxs-lookup"><span data-stu-id="42d0e-121">**LANID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42d0e-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="42d0e-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42d0e-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42d0e-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42d0e-124">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "cim \_ LANConnectivitySegment. LANID，CIM \_ LANSegment. LANID" ) </span><span class="sxs-lookup"><span data-stu-id="42d0e-124">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_LANConnectivitySegment.LANID, CIM\_LANSegment.LANID")</span></span>
</dt> </dl>

<span data-ttu-id="42d0e-125">端點所連接之 LAN 區段的標籤或識別碼。</span><span class="sxs-lookup"><span data-stu-id="42d0e-125">A label or identifier for the LAN segment to which the endpoint is connected.</span></span> <span data-ttu-id="42d0e-126">如果端點目前未連線或此資訊未知，則 **LANID** 為 Null。</span><span class="sxs-lookup"><span data-stu-id="42d0e-126">If the endpoint is not currently connected or if this information is unknown, then **LANID** is NULL.</span></span>

</dd> <dt>

<span data-ttu-id="42d0e-127">**LANType**</span><span class="sxs-lookup"><span data-stu-id="42d0e-127">**LANType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42d0e-128">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="42d0e-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="42d0e-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42d0e-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42d0e-130">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( 「[**CIM \_ ProtocolEndpoint**](cim-protocolendpoint.md)」。**ProtocolType**") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ LANCONNECTIVITYSEGMENT. >connectivitytype，cim \_ LANSegment. LANType ") </span><span class="sxs-lookup"><span data-stu-id="42d0e-130">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM\_ProtocolEndpoint**](cim-protocolendpoint.md).**ProtocolType**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_LANConnectivitySegment.ConnectivityType, CIM\_LANSegment.LANType")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="42d0e-131">已淘汰的描述： LAN 上使用的技術種類。</span><span class="sxs-lookup"><span data-stu-id="42d0e-131">Deprecated description: The kind of technology used on the LAN.</span></span>

 

<span data-ttu-id="42d0e-132">此屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="42d0e-132">This property is deprecated.</span></span> <span data-ttu-id="42d0e-133">相反地，我們建議使用 **ProtocolType** 屬性。</span><span class="sxs-lookup"><span data-stu-id="42d0e-133">Instead we recommend that you use the **ProtocolType** property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="42d0e-134">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="42d0e-134">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="42d0e-135">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="42d0e-135">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="42d0e-136">**Ethernet** (2) </span><span class="sxs-lookup"><span data-stu-id="42d0e-136">**Ethernet** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="TokenRing"></span><span id="tokenring"></span><span id="TOKENRING"></span>

<span data-ttu-id="42d0e-137">**TokenRing** (3) </span><span class="sxs-lookup"><span data-stu-id="42d0e-137">**TokenRing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

<span data-ttu-id="42d0e-138">**FDDI** (4) </span><span class="sxs-lookup"><span data-stu-id="42d0e-138">**FDDI** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="42d0e-139">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="42d0e-139">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42d0e-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="42d0e-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42d0e-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42d0e-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42d0e-142">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (12) </span><span class="sxs-lookup"><span data-stu-id="42d0e-142">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (12)</span></span>
</dt> </dl>

<span data-ttu-id="42d0e-143">LAN 端點所使用的主體單播位址。</span><span class="sxs-lookup"><span data-stu-id="42d0e-143">The principal unicast address used by the LAN endpoint.</span></span>

<span data-ttu-id="42d0e-144">MAC 位址的格式必須為下列特性：</span><span class="sxs-lookup"><span data-stu-id="42d0e-144">The MAC address must be formatted with the following characteristics:</span></span>

-   <span data-ttu-id="42d0e-145">位址包含十二個十六進位數位。</span><span class="sxs-lookup"><span data-stu-id="42d0e-145">The address consists of twelve hexadecimal digits.</span></span>
-   <span data-ttu-id="42d0e-146">每一組數位代表 MAC 位址中六個八位的其中一個。</span><span class="sxs-lookup"><span data-stu-id="42d0e-146">Each pair of digits represents one of the six octets of the MAC address.</span></span>
-   <span data-ttu-id="42d0e-147">每一對數位都必須根據 RFC 2469 以標準的位順序表示。</span><span class="sxs-lookup"><span data-stu-id="42d0e-147">Each pair of digits must be in canonical bit order according to RFC 2469.</span></span>

</dd> <dt>

<span data-ttu-id="42d0e-148">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="42d0e-148">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42d0e-149">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="42d0e-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42d0e-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42d0e-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42d0e-151">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Bits" ) </span><span class="sxs-lookup"><span data-stu-id="42d0e-151">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits")</span></span>
</dt> </dl>

<span data-ttu-id="42d0e-152">LAN 端點所傳送或接收之資料欄位的大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="42d0e-152">The maximum size, in bytes, of data fields sent or received by the LAN endpoint.</span></span>

</dd> <dt>

<span data-ttu-id="42d0e-153">**OtherLANType**</span><span class="sxs-lookup"><span data-stu-id="42d0e-153">**OtherLANType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42d0e-154">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="42d0e-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42d0e-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42d0e-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42d0e-156">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( 「[**CIM \_ ProtocolEndpoint**](cim-protocolendpoint.md)」。**OtherTypeDescription**") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" Cim \_ LANConnectivitySegment. OtherTypeDescription "，"**cim \_ LANEndpoint**.**LANType**") </span><span class="sxs-lookup"><span data-stu-id="42d0e-156">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM\_ProtocolEndpoint**](cim-protocolendpoint.md).**OtherTypeDescription**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_LANConnectivitySegment.OtherTypeDescription", "**CIM\_LANEndpoint**.**LANType**")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="42d0e-157">已淘汰的描述：當 **LANType** 屬性設定為 "1" (其他) 時，LAN 所使用的技術類型。</span><span class="sxs-lookup"><span data-stu-id="42d0e-157">Deprecated description: The type of technology used on the LAN when the **LANType** property is set to "1" (Other).</span></span>

 

<span data-ttu-id="42d0e-158">此屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="42d0e-158">This property is deprecated.</span></span> <span data-ttu-id="42d0e-159">相反地，我們建議使用 **OtherTypeDescription** 屬性。</span><span class="sxs-lookup"><span data-stu-id="42d0e-159">Instead we recommend that you use the **OtherTypeDescription** property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="42d0e-160">規格需求</span><span class="sxs-lookup"><span data-stu-id="42d0e-160">Requirements</span></span>



| <span data-ttu-id="42d0e-161">需求</span><span class="sxs-lookup"><span data-stu-id="42d0e-161">Requirement</span></span> | <span data-ttu-id="42d0e-162">值</span><span class="sxs-lookup"><span data-stu-id="42d0e-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42d0e-163">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="42d0e-163">Minimum supported client</span></span><br/> | <span data-ttu-id="42d0e-164">Windows 8</span><span class="sxs-lookup"><span data-stu-id="42d0e-164">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="42d0e-165">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="42d0e-165">Minimum supported server</span></span><br/> | <span data-ttu-id="42d0e-166">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="42d0e-166">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="42d0e-167">命名空間</span><span class="sxs-lookup"><span data-stu-id="42d0e-167">Namespace</span></span><br/>                | <span data-ttu-id="42d0e-168">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="42d0e-168">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="42d0e-169">MOF</span><span class="sxs-lookup"><span data-stu-id="42d0e-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="42d0e-170"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="42d0e-170"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="42d0e-171">DLL</span><span class="sxs-lookup"><span data-stu-id="42d0e-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42d0e-172"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="42d0e-172"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="42d0e-173">另請參閱</span><span class="sxs-lookup"><span data-stu-id="42d0e-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42d0e-174">**CIM \_ ProtocolEndpoint**</span><span class="sxs-lookup"><span data-stu-id="42d0e-174">**CIM\_ProtocolEndpoint**</span></span>](cim-protocolendpoint.md)
</dt> </dl>

 


---
description: 指派給 VLAN 或接受來自一或多個 Vlan 之流量的交換器或終端工作站上的端點。
ms.assetid: 20943be3-35c3-4bf5-8f1a-d4095fa6897e
title: CIM_VLANEndpoint 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VLANEndpoint
- CIM_VLANEndpoint.DesiredEndpointMode
- CIM_VLANEndpoint.OtherEndpointMode
- CIM_VLANEndpoint.OperationalEndpointMode
- CIM_VLANEndpoint.DesiredVLANTrunkEncapsulation
- CIM_VLANEndpoint.OtherTrunkEncapsulation
- CIM_VLANEndpoint.OperationalVLANTrunkEncapsulation
- CIM_VLANEndpoint.GVRPStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0f7b0d1318e4c24ab7381032877d16a8ea83868b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112008"
---
# <a name="cim_vlanendpoint-class"></a><span data-ttu-id="e1620-103">CIM \_ VLANEndpoint 類別</span><span class="sxs-lookup"><span data-stu-id="e1620-103">CIM\_VLANEndpoint class</span></span>

<span data-ttu-id="e1620-104">指派給 VLAN 或接受來自一或多個 Vlan 之流量的交換器或終端工作站上的端點。</span><span class="sxs-lookup"><span data-stu-id="e1620-104">An endpoint on a switch or end station that is assigned to a VLAN, or accepts traffic from one or more VLANs.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1620-105">語法</span><span class="sxs-lookup"><span data-stu-id="e1620-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.26.0"), UMLPackagePath("CIM::Network::VLAN"), AMENDMENT]
class CIM_VLANEndpoint : CIM_ProtocolEndpoint
{
  uint16 DesiredEndpointMode;
  string OtherEndpointMode;
  uint16 OperationalEndpointMode;
  uint16 DesiredVLANTrunkEncapsulation;
  string OtherTrunkEncapsulation;
  uint16 OperationalVLANTrunkEncapsulation;
  uint16 GVRPStatus;
};
```

## <a name="members"></a><span data-ttu-id="e1620-106">成員</span><span class="sxs-lookup"><span data-stu-id="e1620-106">Members</span></span>

<span data-ttu-id="e1620-107">**CIM \_ VLANEndpoint** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e1620-107">The **CIM\_VLANEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="e1620-108">屬性</span><span class="sxs-lookup"><span data-stu-id="e1620-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e1620-109">屬性</span><span class="sxs-lookup"><span data-stu-id="e1620-109">Properties</span></span>

<span data-ttu-id="e1620-110">**CIM \_ VLANEndpoint** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e1620-110">The **CIM\_VLANEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e1620-111">**DesiredEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="e1620-111">**DesiredEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1620-112">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e1620-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e1620-113">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e1620-113">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e1620-114">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ VLANEndpoint**.**OperationalEndpointMode**"，"**CIM \_ VLANEndpoint**.**OtherEndpointMode**") </span><span class="sxs-lookup"><span data-stu-id="e1620-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**OperationalEndpointMode**", "**CIM\_VLANEndpoint**.**OtherEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="e1620-115">端點要求的 VLAN 模式。</span><span class="sxs-lookup"><span data-stu-id="e1620-115">The requested VLAN mode for the endpoint.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e1620-116">**DMTF 保留** (0) </span><span class="sxs-lookup"><span data-stu-id="e1620-116">**DMTF Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e1620-117">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="e1620-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

<span data-ttu-id="e1620-118">**存取** (2) </span><span class="sxs-lookup"><span data-stu-id="e1620-118">**Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span>

<span data-ttu-id="e1620-119">**動態自動** (3) </span><span class="sxs-lookup"><span data-stu-id="e1620-119">**Dynamic Auto** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span>

<span data-ttu-id="e1620-120">**動態需要** (4) </span><span class="sxs-lookup"><span data-stu-id="e1620-120">**Dynamic Desirable** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

<span data-ttu-id="e1620-121">**主幹** (5) </span><span class="sxs-lookup"><span data-stu-id="e1620-121">**Trunk** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span>

<span data-ttu-id="e1620-122">**Dot1Q** 通道 (6) </span><span class="sxs-lookup"><span data-stu-id="e1620-122">**Dot1Q Tunnel** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e1620-123">**DMTF 保留** (7. 32767) </span><span class="sxs-lookup"><span data-stu-id="e1620-123">**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="e1620-124">**廠商保留** 的 (。) </span><span class="sxs-lookup"><span data-stu-id="e1620-124">**Vendor Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e1620-125">**DesiredVLANTrunkEncapsulation**</span><span class="sxs-lookup"><span data-stu-id="e1620-125">**DesiredVLANTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1620-126">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e1620-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e1620-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e1620-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e1620-128">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "cim \_ VLANEndpointCapabilities. SupportsTrunkEncapsulationNegotiation"，"**cim \_ VLANEndpoint**.**OperationalVLANTrunkEncapsulation**"，"**CIM \_ VLANEndpoint**.**OtherTrunkEncapsulation**") </span><span class="sxs-lookup"><span data-stu-id="e1620-128">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VLANEndpointCapabilities.SupportsTrunkEncapsulationNegotiation", "**CIM\_VLANEndpoint**.**OperationalVLANTrunkEncapsulation**", "**CIM\_VLANEndpoint**.**OtherTrunkEncapsulation**")</span></span>
</dt> </dl>

<span data-ttu-id="e1620-129">要求的 VLAN 封裝類型。</span><span class="sxs-lookup"><span data-stu-id="e1620-129">The requested VLAN encapsulation type.</span></span>

> [!Note]  
> <span data-ttu-id="e1620-130">只有當 VLAN 端點處於中繼模式時，才會使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="e1620-130">This property is only used when the VLAN endpoint is in trunking mode.</span></span>

 

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e1620-131">**DMTF 保留** (0) </span><span class="sxs-lookup"><span data-stu-id="e1620-131">**DMTF Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e1620-132">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="e1620-132">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e1620-133">**不適用** (2) </span><span class="sxs-lookup"><span data-stu-id="e1620-133">**Not Applicable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="802.1q"></span><span id="802.1Q"></span>

<span data-ttu-id="e1620-134">**802.1 q** (3) </span><span class="sxs-lookup"><span data-stu-id="e1620-134">**802.1q** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>

<span data-ttu-id="e1620-135">**CISCO ISL** (4) </span><span class="sxs-lookup"><span data-stu-id="e1620-135">**Cisco ISL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

<span data-ttu-id="e1620-136">**協商** (5) </span><span class="sxs-lookup"><span data-stu-id="e1620-136">**Negotiate** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e1620-137">**DMTF 保留** (6. 32767) </span><span class="sxs-lookup"><span data-stu-id="e1620-137">**DMTF Reserved** (6..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="e1620-138">**廠商保留** (32768 ) </span><span class="sxs-lookup"><span data-stu-id="e1620-138">**Vendor Reserved** (32768..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e1620-139">**GVRPStatus**</span><span class="sxs-lookup"><span data-stu-id="e1620-139">**GVRPStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1620-140">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e1620-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e1620-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e1620-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1620-142">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ VLANEndpoint**.**OperationalEndpointMode**，CIM \_ VLANEndpointCapabilities. Dot1QTagging ") </span><span class="sxs-lookup"><span data-stu-id="e1620-142">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**OperationalEndpointMode**, CIM\_VLANEndpointCapabilities.Dot1QTagging")</span></span>
</dt> </dl>

<span data-ttu-id="e1620-143">指出是否已在主幹端點上啟用或停用 GARP VLAN 註冊通訊協定 (GVRP) 。</span><span class="sxs-lookup"><span data-stu-id="e1620-143">Indicates whether GARP VLAN Registration Protocol (GVRP) is enabled or disabled on the trunk endpoint.</span></span>

> [!Note]  
> <span data-ttu-id="e1620-144">只有當端點支援 GVRP 且已啟用中繼模式時，才會使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="e1620-144">This property is only used when GVRP is supported by the endpoint, and trunking mode is enabled.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e1620-145">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="e1620-145">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e1620-146">**不適用** (2) </span><span class="sxs-lookup"><span data-stu-id="e1620-146">**Not Applicable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e1620-147">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="e1620-147">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e1620-148">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="e1620-148">**Disabled** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e1620-149">**OperationalEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="e1620-149">**OperationalEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1620-150">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e1620-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e1620-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e1620-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1620-152">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ VLANEndpoint**.**DesiredEndpointMode**"，"**CIM \_ VLANEndpoint**.**OtherEndpointMode**") </span><span class="sxs-lookup"><span data-stu-id="e1620-152">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**DesiredEndpointMode**", "**CIM\_VLANEndpoint**.**OtherEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="e1620-153">端點目前的 VLAN 模式。</span><span class="sxs-lookup"><span data-stu-id="e1620-153">The current VLAN mode for the endpoint.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e1620-154">**DMTF 保留** (0) </span><span class="sxs-lookup"><span data-stu-id="e1620-154">**DMTF Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e1620-155">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="e1620-155">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

<span data-ttu-id="e1620-156">**存取** (2) </span><span class="sxs-lookup"><span data-stu-id="e1620-156">**Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span>

<span data-ttu-id="e1620-157">**動態自動** (3) </span><span class="sxs-lookup"><span data-stu-id="e1620-157">**Dynamic Auto** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span>

<span data-ttu-id="e1620-158">**動態需要** (4) </span><span class="sxs-lookup"><span data-stu-id="e1620-158">**Dynamic Desirable** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

<span data-ttu-id="e1620-159">**主幹** (5) </span><span class="sxs-lookup"><span data-stu-id="e1620-159">**Trunk** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span>

<span data-ttu-id="e1620-160">**Dot1Q** 通道 (6) </span><span class="sxs-lookup"><span data-stu-id="e1620-160">**Dot1Q Tunnel** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e1620-161">**DMTF 保留** (7. 32767) </span><span class="sxs-lookup"><span data-stu-id="e1620-161">**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="e1620-162">**廠商保留** 的 (。) </span><span class="sxs-lookup"><span data-stu-id="e1620-162">**Vendor Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e1620-163">**OperationalVLANTrunkEncapsulation**</span><span class="sxs-lookup"><span data-stu-id="e1620-163">**OperationalVLANTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1620-164">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e1620-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e1620-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e1620-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1620-166">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ VLANEndpoint**.**OtherTrunkEncapsulation**"，"**CIM \_ VLANEndpoint**.**DesiredVLANTrunkEncapsulation**") </span><span class="sxs-lookup"><span data-stu-id="e1620-166">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**OtherTrunkEncapsulation**", "**CIM\_VLANEndpoint**.**DesiredVLANTrunkEncapsulation**")</span></span>
</dt> </dl>

<span data-ttu-id="e1620-167">目前的 VLAN 封裝類型。</span><span class="sxs-lookup"><span data-stu-id="e1620-167">The current VLAN encapsulation type.</span></span>

> [!Note]  
> <span data-ttu-id="e1620-168">只有當 VLAN 端點處於中繼模式時，才會使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="e1620-168">This property is only used when the VLAN endpoint is in trunking mode.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e1620-169">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="e1620-169">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e1620-170">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="e1620-170">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e1620-171">**不適用** (2) </span><span class="sxs-lookup"><span data-stu-id="e1620-171">**Not Applicable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="802.1q"></span><span id="802.1Q"></span>

<span data-ttu-id="e1620-172">**802.1 q** (3) </span><span class="sxs-lookup"><span data-stu-id="e1620-172">**802.1q** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>

<span data-ttu-id="e1620-173">**CISCO ISL** (4) </span><span class="sxs-lookup"><span data-stu-id="e1620-173">**Cisco ISL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Negotiating"></span><span id="negotiating"></span><span id="NEGOTIATING"></span>

<span data-ttu-id="e1620-174">**協商** (5) </span><span class="sxs-lookup"><span data-stu-id="e1620-174">**Negotiating** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e1620-175">**DMTF 保留** (6. 32767) </span><span class="sxs-lookup"><span data-stu-id="e1620-175">**DMTF Reserved** (6..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="e1620-176">**廠商保留** (32768 ) </span><span class="sxs-lookup"><span data-stu-id="e1620-176">**Vendor Reserved** (32768..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e1620-177">**OtherEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="e1620-177">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1620-178">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e1620-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1620-179">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e1620-179">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e1620-180">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ VLANEndpoint**.**DesiredEndpointMode**"，"**CIM \_ VLANEndpoint**.**OperationalEndpointMode**") </span><span class="sxs-lookup"><span data-stu-id="e1620-180">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**DesiredEndpointMode**", "**CIM\_VLANEndpoint**.**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="e1620-181">當 **DesiredEndpointMode** 的值設定為 "1" (其他) 時，VLANEndpoint 所支援的 VLAN 端點模型類型;否則 **為 Null**。</span><span class="sxs-lookup"><span data-stu-id="e1620-181">The type of VLAN endpoint model that is supported by the VLANEndpoint when the value of **DesiredEndpointMode** is set to "1" (other); otherwise, **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e1620-182">**OtherTrunkEncapsulation**</span><span class="sxs-lookup"><span data-stu-id="e1620-182">**OtherTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1620-183">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e1620-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1620-184">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e1620-184">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e1620-185">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ VLANEndpoint**.**DesiredVLANTrunkEncapsulation**"，"**CIM \_ VLANEndpoint**.**OperationalVLANTrunkEncapsulation**") </span><span class="sxs-lookup"><span data-stu-id="e1620-185">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**DesiredVLANTrunkEncapsulation**", "**CIM\_VLANEndpoint**.**OperationalVLANTrunkEncapsulation**")</span></span>
</dt> </dl>

<span data-ttu-id="e1620-186">當 **DesiredVLANTrunkEncapsulation** 屬性的值設定為 1 (其他) 時，vlan 端點所支援的 vlan 封裝類型;否則 **為 Null**。</span><span class="sxs-lookup"><span data-stu-id="e1620-186">The type of VLAN encapsulation that is supported by the VLAN endpoint when the value of the **DesiredVLANTrunkEncapsulation** property is set to 1 (other); otherwise, **NULL**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e1620-187">規格需求</span><span class="sxs-lookup"><span data-stu-id="e1620-187">Requirements</span></span>



| <span data-ttu-id="e1620-188">需求</span><span class="sxs-lookup"><span data-stu-id="e1620-188">Requirement</span></span> | <span data-ttu-id="e1620-189">值</span><span class="sxs-lookup"><span data-stu-id="e1620-189">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1620-190">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e1620-190">Minimum supported client</span></span><br/> | <span data-ttu-id="e1620-191">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e1620-191">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="e1620-192">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e1620-192">Minimum supported server</span></span><br/> | <span data-ttu-id="e1620-193">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e1620-193">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="e1620-194">命名空間</span><span class="sxs-lookup"><span data-stu-id="e1620-194">Namespace</span></span><br/>                | <span data-ttu-id="e1620-195">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="e1620-195">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e1620-196">MOF</span><span class="sxs-lookup"><span data-stu-id="e1620-196">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e1620-197"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="e1620-197"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e1620-198">DLL</span><span class="sxs-lookup"><span data-stu-id="e1620-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1620-199"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e1620-199"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e1620-200">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e1620-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1620-201">**CIM \_ ProtocolEndpoint**</span><span class="sxs-lookup"><span data-stu-id="e1620-201">**CIM\_ProtocolEndpoint**</span></span>](cim-protocolendpoint.md)
</dt> </dl>

 


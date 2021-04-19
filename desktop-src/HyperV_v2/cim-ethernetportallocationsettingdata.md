---
description: 表示除了 CIM EthernetPort 類別所提供的設定之外，用於配置乙太網路埠的設定 \_ 。 這些設定是用來提供資源本身的特定資訊。
ms.assetid: f59ebaf1-60dd-49bd-b48e-d7a6c2650909
title: CIM_EthernetPortAllocationSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EthernetPortAllocationSettingData
- CIM_EthernetPortAllocationSettingData.DesiredVLANEndpointMode
- CIM_EthernetPortAllocationSettingData.OtherEndpointMode
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e77b4387f77e88ceaff273b8be72a354c989e7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972586"
---
# <a name="cim_ethernetportallocationsettingdata-class"></a><span data-ttu-id="dff08-104">CIM \_ EthernetPortAllocationSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="dff08-104">CIM\_EthernetPortAllocationSettingData class</span></span>

<span data-ttu-id="dff08-105">表示除了 [**CIM \_ EthernetPort**](cim-ethernetport.md) 類別所提供的設定之外，用於配置乙太網路埠的設定。</span><span class="sxs-lookup"><span data-stu-id="dff08-105">Represents settings for the allocation of the ethernet port, in addition to the settings provided by the [**CIM\_EthernetPort**](cim-ethernetport.md) class.</span></span> <span data-ttu-id="dff08-106">這些設定是用來提供資源本身的特定資訊。</span><span class="sxs-lookup"><span data-stu-id="dff08-106">These settings are used to provide information specific to the resource itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="dff08-107">語法</span><span class="sxs-lookup"><span data-stu-id="dff08-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.26.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_EthernetPortAllocationSettingData : CIM_ResourceAllocationSettingData
{
  uint16 DesiredVLANEndpointMode;
  string OtherEndpointMode;
};
```

## <a name="members"></a><span data-ttu-id="dff08-108">成員</span><span class="sxs-lookup"><span data-stu-id="dff08-108">Members</span></span>

<span data-ttu-id="dff08-109">**CIM \_ EthernetPortAllocationSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="dff08-109">The **CIM\_EthernetPortAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="dff08-110">屬性</span><span class="sxs-lookup"><span data-stu-id="dff08-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dff08-111">屬性</span><span class="sxs-lookup"><span data-stu-id="dff08-111">Properties</span></span>

<span data-ttu-id="dff08-112">**CIM \_ EthernetPortAllocationSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="dff08-112">The **CIM\_EthernetPortAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dff08-113">**DesiredVLANEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="dff08-113">**DesiredVLANEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dff08-114">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="dff08-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dff08-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dff08-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dff08-116">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**"，"**CIM \_ VLANEndpoint**.**DesiredEndpointMode**"，"**CIM \_ EthernetPortAllocationSettingData**.**OtherEndpointMode**") </span><span class="sxs-lookup"><span data-stu-id="dff08-116">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**", "**CIM\_VLANEndpoint**.**DesiredEndpointMode**", "**CIM\_EthernetPortAllocationSettingData**.**OtherEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="dff08-117">要求的 VLAN 模式。</span><span class="sxs-lookup"><span data-stu-id="dff08-117">The requested VLAN mode.</span></span> <span data-ttu-id="dff08-118">這個屬性是用來設定與乙太網路埠相關聯之 **CIM \_ VLANEndpoint** 實例中的初始 **OperationalEndpointMode** 屬性值。</span><span class="sxs-lookup"><span data-stu-id="dff08-118">This property is used to set the initial **OperationalEndpointMode** property value in the instance of **CIM\_VLANEndpoint** associated with the ethernet port.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="dff08-119">**DMTF 保留** (0) </span><span class="sxs-lookup"><span data-stu-id="dff08-119">**DMTF Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dff08-120">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="dff08-120">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

<span data-ttu-id="dff08-121">**存取** (2) </span><span class="sxs-lookup"><span data-stu-id="dff08-121">**Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span>

<span data-ttu-id="dff08-122">**動態自動** (3) </span><span class="sxs-lookup"><span data-stu-id="dff08-122">**Dynamic Auto** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span>

<span data-ttu-id="dff08-123">**動態需要** (4) </span><span class="sxs-lookup"><span data-stu-id="dff08-123">**Dynamic Desirable** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

<span data-ttu-id="dff08-124">**主幹** (5) </span><span class="sxs-lookup"><span data-stu-id="dff08-124">**Trunk** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span>

<span data-ttu-id="dff08-125">**Dot1Q** 通道 (6) </span><span class="sxs-lookup"><span data-stu-id="dff08-125">**Dot1Q Tunnel** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="dff08-126">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="dff08-126">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="dff08-127">**廠商保留** (0x8000。0xFFFF) </span><span class="sxs-lookup"><span data-stu-id="dff08-127">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dff08-128">**OtherEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="dff08-128">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dff08-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dff08-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dff08-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dff08-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dff08-131">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ EthernetPortAllocationSettingData**.**DesiredVLANEndpointMode**") </span><span class="sxs-lookup"><span data-stu-id="dff08-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EthernetPortAllocationSettingData**.**DesiredVLANEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="dff08-132">當 mode 屬性的值設定為 "1" 時，此 VLAN 端點所支援的 VLAN 端點模型類型 (其他) 。</span><span class="sxs-lookup"><span data-stu-id="dff08-132">The type of VLAN endpoint model that is supported by this VLAN endpoint, when the value of the mode property is set to "1" (Other).</span></span> <span data-ttu-id="dff08-133">當 mode 屬性是 "1" 以外的任何值時，這個屬性應該設為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="dff08-133">This property should be set to **NULL** when the mode property is any value other than "1".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dff08-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="dff08-134">Requirements</span></span>



| <span data-ttu-id="dff08-135">需求</span><span class="sxs-lookup"><span data-stu-id="dff08-135">Requirement</span></span> | <span data-ttu-id="dff08-136">值</span><span class="sxs-lookup"><span data-stu-id="dff08-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dff08-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dff08-137">Minimum supported client</span></span><br/> | <span data-ttu-id="dff08-138">Windows 8</span><span class="sxs-lookup"><span data-stu-id="dff08-138">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="dff08-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dff08-139">Minimum supported server</span></span><br/> | <span data-ttu-id="dff08-140">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dff08-140">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="dff08-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="dff08-141">Namespace</span></span><br/>                | <span data-ttu-id="dff08-142">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="dff08-142">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="dff08-143">MOF</span><span class="sxs-lookup"><span data-stu-id="dff08-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dff08-144"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="dff08-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dff08-145">DLL</span><span class="sxs-lookup"><span data-stu-id="dff08-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dff08-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dff08-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dff08-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dff08-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dff08-148">**CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="dff08-148">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 


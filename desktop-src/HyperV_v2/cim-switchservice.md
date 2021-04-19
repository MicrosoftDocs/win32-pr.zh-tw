---
description: 表示 switch 服務。
ms.assetid: cf6319fa-7d69-4820-b0e0-775aad8b190c
title: CIM_SwitchService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchService
- CIM_SwitchService.BridgeAddress
- CIM_SwitchService.NumPorts
- CIM_SwitchService.BridgeType
- CIM_SwitchService.BridgeAddressType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9abe6869c5b8ac61630091315e476ae232630717
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976830"
---
# <a name="cim_switchservice-class"></a><span data-ttu-id="aef88-103">CIM \_ SwitchService 類別</span><span class="sxs-lookup"><span data-stu-id="aef88-103">CIM\_SwitchService class</span></span>

<span data-ttu-id="aef88-104">表示 switch 服務。</span><span class="sxs-lookup"><span data-stu-id="aef88-104">Represents a switch service.</span></span>

## <a name="syntax"></a><span data-ttu-id="aef88-105">語法</span><span class="sxs-lookup"><span data-stu-id="aef88-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging")]
class CIM_SwitchService : CIM_ForwardingService
{
  string BridgeAddress;
  uint16 NumPorts;
  uint8  BridgeType;
  uint16 BridgeAddressType;
};
```

## <a name="members"></a><span data-ttu-id="aef88-106">成員</span><span class="sxs-lookup"><span data-stu-id="aef88-106">Members</span></span>

<span data-ttu-id="aef88-107">**CIM \_ SwitchService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="aef88-107">The **CIM\_SwitchService** class has these types of members:</span></span>

-   [<span data-ttu-id="aef88-108">屬性</span><span class="sxs-lookup"><span data-stu-id="aef88-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aef88-109">屬性</span><span class="sxs-lookup"><span data-stu-id="aef88-109">Properties</span></span>

<span data-ttu-id="aef88-110">**CIM \_ SwitchService** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="aef88-110">The **CIM\_SwitchService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aef88-111">**BridgeAddress**</span><span class="sxs-lookup"><span data-stu-id="aef88-111">**BridgeAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aef88-112">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aef88-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aef88-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aef88-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aef88-114">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (32) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIB。IETF \| BRIDGE-MIB. dot1dBaseBridgeAddress ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SwitchService**。**BridgeAddressType**") </span><span class="sxs-lookup"><span data-stu-id="aef88-114">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dBaseBridgeAddress"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SwitchService**.**BridgeAddressType**")</span></span>
</dt> </dl>

<span data-ttu-id="aef88-115">交換器服務的位址，這是服務之唯一識別碼的一部分。</span><span class="sxs-lookup"><span data-stu-id="aef88-115">The address of the switch service, which is a portion of the unique identifier of the service.</span></span>

</dd> <dt>

<span data-ttu-id="aef88-116">**BridgeAddressType**</span><span class="sxs-lookup"><span data-stu-id="aef88-116">**BridgeAddressType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aef88-117">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="aef88-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aef88-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aef88-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aef88-119">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ SwitchService**.**BridgeAddress**") </span><span class="sxs-lookup"><span data-stu-id="aef88-119">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SwitchService**.**BridgeAddress**")</span></span>
</dt> </dl>

<span data-ttu-id="aef88-120">用於橋接器和 **BridgeAddress** 屬性的定址格式。</span><span class="sxs-lookup"><span data-stu-id="aef88-120">The addressing format used for the bridge and the **BridgeAddress** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="aef88-121">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="aef88-121">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

<span data-ttu-id="aef88-122">**IPv4** (2) </span><span class="sxs-lookup"><span data-stu-id="aef88-122">**IPv4** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

<span data-ttu-id="aef88-123">**IPv6** (3) </span><span class="sxs-lookup"><span data-stu-id="aef88-123">**IPv6** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="MAC"></span><span id="mac"></span>

<span data-ttu-id="aef88-124">**MAC** (4) </span><span class="sxs-lookup"><span data-stu-id="aef88-124">**MAC** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="MAC___Spanning_Tree_Priority"></span><span id="mac___spanning_tree_priority"></span><span id="MAC___SPANNING_TREE_PRIORITY"></span>

<span data-ttu-id="aef88-125">**MAC + 跨越樹狀目錄優先順序** (5) </span><span class="sxs-lookup"><span data-stu-id="aef88-125">**MAC + Spanning Tree Priority** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="aef88-126">**BridgeType**</span><span class="sxs-lookup"><span data-stu-id="aef88-126">**BridgeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aef88-127">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="aef88-127">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="aef88-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aef88-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aef88-129">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| BRIDGE-dot1dBaseType ") </span><span class="sxs-lookup"><span data-stu-id="aef88-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dBaseType")</span></span>
</dt> </dl>

<span data-ttu-id="aef88-130">要執行的切換服務類型。</span><span class="sxs-lookup"><span data-stu-id="aef88-130">The type of switching service to perform.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aef88-131">**未知** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="aef88-131">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparent-only"></span><span id="transparent-only"></span><span id="TRANSPARENT-ONLY"></span>

<span data-ttu-id="aef88-132">**僅限透明** (2) </span><span class="sxs-lookup"><span data-stu-id="aef88-132">**Transparent-only** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SourceRoute-only"></span><span id="sourceroute-only"></span><span id="SOURCEROUTE-ONLY"></span>

<span data-ttu-id="aef88-133">**僅限 SourceRoute** (3) </span><span class="sxs-lookup"><span data-stu-id="aef88-133">**SourceRoute-only** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SRT"></span><span id="srt"></span>

<span data-ttu-id="aef88-134">**SRT** (4) </span><span class="sxs-lookup"><span data-stu-id="aef88-134">**SRT** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="aef88-135">**NumPorts**</span><span class="sxs-lookup"><span data-stu-id="aef88-135">**NumPorts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aef88-136">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="aef88-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aef88-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aef88-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aef88-138">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| BRIDGE-dot1dBaseNumPorts ") </span><span class="sxs-lookup"><span data-stu-id="aef88-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dBaseNumPorts")</span></span>
</dt> </dl>

<span data-ttu-id="aef88-139">由此切換服務控制的交換器埠數目。</span><span class="sxs-lookup"><span data-stu-id="aef88-139">The number of switch ports controlled by this switching service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aef88-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="aef88-140">Requirements</span></span>



| <span data-ttu-id="aef88-141">需求</span><span class="sxs-lookup"><span data-stu-id="aef88-141">Requirement</span></span> | <span data-ttu-id="aef88-142">值</span><span class="sxs-lookup"><span data-stu-id="aef88-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aef88-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aef88-143">Minimum supported client</span></span><br/> | <span data-ttu-id="aef88-144">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="aef88-144">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="aef88-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aef88-145">Minimum supported server</span></span><br/> | <span data-ttu-id="aef88-146">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="aef88-146">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="aef88-147">命名空間</span><span class="sxs-lookup"><span data-stu-id="aef88-147">Namespace</span></span><br/>                | <span data-ttu-id="aef88-148">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="aef88-148">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="aef88-149">MOF</span><span class="sxs-lookup"><span data-stu-id="aef88-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aef88-150"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="aef88-150"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="aef88-151">DLL</span><span class="sxs-lookup"><span data-stu-id="aef88-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aef88-152"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="aef88-152"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="aef88-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aef88-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aef88-154">**CIM \_ ForwardingService**</span><span class="sxs-lookup"><span data-stu-id="aef88-154">**CIM\_ForwardingService**</span></span>](cim-forwardingservice.md)
</dt> </dl>

 


---
description: 表示 CIM \_ ServiceAccessPoint 或 cim \_ ProtocolEndpoint 物件相依于 \_ 相同系統上的基礎 CIM LANEndpoint 物件的關聯。
ms.assetid: 3c015fbd-0611-41e8-a79a-01c980eedfd3
title: CIM_BindsToLANEndpoint 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BindsToLANEndpoint
- CIM_BindsToLANEndpoint.Antecedent
- CIM_BindsToLANEndpoint.Dependent
- CIM_BindsToLANEndpoint.FrameType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dff1cf243b54739509343d6d8958aa2a54f464b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987295"
---
# <a name="cim_bindstolanendpoint-class"></a><span data-ttu-id="a89b7-103">CIM \_ BindsToLANEndpoint 類別</span><span class="sxs-lookup"><span data-stu-id="a89b7-103">CIM\_BindsToLANEndpoint class</span></span>

<span data-ttu-id="a89b7-104">表示 [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md) 或 [**cim \_ ProtocolEndpoint**](cim-protocolendpoint.md) 物件相依于相同系統上的基礎 [**CIM \_ LANEndpoint**](cim-lanendpoint.md) 物件的關聯。</span><span class="sxs-lookup"><span data-stu-id="a89b7-104">Represents an association where a [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) or [**CIM\_ProtocolEndpoint**](cim-protocolendpoint.md) object depends on an underlying [**CIM\_LANEndpoint**](cim-lanendpoint.md) object on the same system.</span></span>

## <a name="syntax"></a><span data-ttu-id="a89b7-105">語法</span><span class="sxs-lookup"><span data-stu-id="a89b7-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::ProtocolEndpoints"), AMENDMENT]
class CIM_BindsToLANEndpoint : CIM_BindsTo
{
  CIM_LANEndpoint        REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
  uint16                     FrameType;
};
```

## <a name="members"></a><span data-ttu-id="a89b7-106">成員</span><span class="sxs-lookup"><span data-stu-id="a89b7-106">Members</span></span>

<span data-ttu-id="a89b7-107">**CIM \_ BindsToLANEndpoint** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a89b7-107">The **CIM\_BindsToLANEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="a89b7-108">屬性</span><span class="sxs-lookup"><span data-stu-id="a89b7-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a89b7-109">屬性</span><span class="sxs-lookup"><span data-stu-id="a89b7-109">Properties</span></span>

<span data-ttu-id="a89b7-110">**CIM \_ BindsToLANEndpoint** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a89b7-110">The **CIM\_BindsToLANEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a89b7-111">**先行**</span><span class="sxs-lookup"><span data-stu-id="a89b7-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a89b7-112">資料類型： **CIM \_ LANEndpoint**</span><span class="sxs-lookup"><span data-stu-id="a89b7-112">Data type: **CIM\_LANEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="a89b7-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a89b7-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a89b7-114">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="a89b7-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="a89b7-115">基礎 [**CIM \_ LANEndpoint**](cim-lanendpoint.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="a89b7-115">The underlying [**CIM\_LANEndpoint**](cim-lanendpoint.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="a89b7-116">**依賴**</span><span class="sxs-lookup"><span data-stu-id="a89b7-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a89b7-117">資料類型： **CIM \_ ServiceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="a89b7-117">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="a89b7-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a89b7-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a89b7-119">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="a89b7-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="a89b7-120">相依于 [**cim \_ LANEndpoint**](cim-lanendpoint.md)的 [**cim \_ ServiceAccessPoint**](cim-serviceaccesspoint.md)或 [**cim \_ ProtocolEndpoint**](cim-protocolendpoint.md)物件。</span><span class="sxs-lookup"><span data-stu-id="a89b7-120">The [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) or [**CIM\_ProtocolEndpoint**](cim-protocolendpoint.md) object that is dependent on the [**CIM\_LANEndpoint**](cim-lanendpoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="a89b7-121">**FrameType**</span><span class="sxs-lookup"><span data-stu-id="a89b7-121">**FrameType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a89b7-122">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a89b7-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a89b7-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a89b7-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a89b7-124">上層服務存取點或通訊協定端點的框架方法。</span><span class="sxs-lookup"><span data-stu-id="a89b7-124">The framing method for the upper layer service access point or protocol endpoint.</span></span>

> [!Note]  
> <span data-ttu-id="a89b7-125">只有在使用 IPX 通訊協定時，才會知道原始802.3。</span><span class="sxs-lookup"><span data-stu-id="a89b7-125">Raw802.3 is only known to be used with the IPX protocol.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a89b7-126">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="a89b7-126">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="a89b7-127">**Ethernet** (1) </span><span class="sxs-lookup"><span data-stu-id="a89b7-127">**Ethernet** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="802.2"></span>

<span data-ttu-id="a89b7-128">**802.2** (2) </span><span class="sxs-lookup"><span data-stu-id="a89b7-128">**802.2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SNAP"></span><span id="snap"></span>

<span data-ttu-id="a89b7-129">**貼齊** (3) </span><span class="sxs-lookup"><span data-stu-id="a89b7-129">**SNAP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Raw802.3"></span><span id="raw802.3"></span><span id="RAW802.3"></span>

<span data-ttu-id="a89b7-130">**原始的 802.3** (4) </span><span class="sxs-lookup"><span data-stu-id="a89b7-130">**Raw802.3** (4)</span></span>


<span data-ttu-id="a89b7-131"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a89b7-131"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="a89b7-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="a89b7-132">Requirements</span></span>



| <span data-ttu-id="a89b7-133">需求</span><span class="sxs-lookup"><span data-stu-id="a89b7-133">Requirement</span></span> | <span data-ttu-id="a89b7-134">值</span><span class="sxs-lookup"><span data-stu-id="a89b7-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a89b7-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a89b7-135">Minimum supported client</span></span><br/> | <span data-ttu-id="a89b7-136">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a89b7-136">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="a89b7-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a89b7-137">Minimum supported server</span></span><br/> | <span data-ttu-id="a89b7-138">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a89b7-138">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="a89b7-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="a89b7-139">Namespace</span></span><br/>                | <span data-ttu-id="a89b7-140">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="a89b7-140">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a89b7-141">MOF</span><span class="sxs-lookup"><span data-stu-id="a89b7-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a89b7-142"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="a89b7-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a89b7-143">DLL</span><span class="sxs-lookup"><span data-stu-id="a89b7-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a89b7-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a89b7-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a89b7-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a89b7-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a89b7-146">**CIM \_ BindsTo**</span><span class="sxs-lookup"><span data-stu-id="a89b7-146">**CIM\_BindsTo**</span></span>](cim-bindsto.md)
</dt> </dl>

 


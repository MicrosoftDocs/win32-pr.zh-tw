---
description: 裝置之埠或連接點的抽象概念。
ms.assetid: ee725c64-587b-4e5f-9b1c-7a58902b0631
title: CIM_LogicalPort 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalPort
- CIM_LogicalPort.Speed
- CIM_LogicalPort.MaxSpeed
- CIM_LogicalPort.RequestedSpeed
- CIM_LogicalPort.UsageRestriction
- CIM_LogicalPort.PortType
- CIM_LogicalPort.OtherPortType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: eeed69e9669048377340cb0ca21e7a2e89f4baff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936593"
---
# <a name="cim_logicalport-class"></a><span data-ttu-id="d47cb-103">CIM \_ LogicalPort 類別</span><span class="sxs-lookup"><span data-stu-id="d47cb-103">CIM\_LogicalPort class</span></span>

<span data-ttu-id="d47cb-104">裝置之埠或連接點的抽象概念。</span><span class="sxs-lookup"><span data-stu-id="d47cb-104">The abstraction of a port or connection point of a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="d47cb-105">語法</span><span class="sxs-lookup"><span data-stu-id="d47cb-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_LogicalPort : CIM_LogicalDevice
{
  uint64 Speed;
  uint64 MaxSpeed;
  uint64 RequestedSpeed;
  uint16 UsageRestriction;
  uint16 PortType;
  string OtherPortType;
};
```

## <a name="members"></a><span data-ttu-id="d47cb-106">成員</span><span class="sxs-lookup"><span data-stu-id="d47cb-106">Members</span></span>

<span data-ttu-id="d47cb-107">**CIM \_ LogicalPort** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d47cb-107">The **CIM\_LogicalPort** class has these types of members:</span></span>

-   [<span data-ttu-id="d47cb-108">屬性</span><span class="sxs-lookup"><span data-stu-id="d47cb-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d47cb-109">屬性</span><span class="sxs-lookup"><span data-stu-id="d47cb-109">Properties</span></span>

<span data-ttu-id="d47cb-110">**CIM \_ LogicalPort** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d47cb-110">The **CIM\_LogicalPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d47cb-111">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="d47cb-111">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d47cb-112">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="d47cb-112">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d47cb-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d47cb-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d47cb-114">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「每秒位數」 ) ， **PUnit** ( 「位/秒」 ) </span><span class="sxs-lookup"><span data-stu-id="d47cb-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="d47cb-115">埠的最大頻寬（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="d47cb-115">The maximum bandwidth of the port, in bits per second.</span></span>

</dd> <dt>

<span data-ttu-id="d47cb-116">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="d47cb-116">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d47cb-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d47cb-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d47cb-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d47cb-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d47cb-119">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ LogicalPort**.**PortType**") </span><span class="sxs-lookup"><span data-stu-id="d47cb-119">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalPort**.**PortType**")</span></span>
</dt> </dl>

<span data-ttu-id="d47cb-120">描述當 **PortType** 設定為 **其他** ( "1" ) 時，模組的類型。</span><span class="sxs-lookup"><span data-stu-id="d47cb-120">Describes the type of module, when **PortType** is set to **Other** ("1").</span></span>

</dd> <dt>

<span data-ttu-id="d47cb-121">**PortType**</span><span class="sxs-lookup"><span data-stu-id="d47cb-121">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d47cb-122">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d47cb-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d47cb-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d47cb-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d47cb-124">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ NetworkPort**](cim-networkport.md).**OtherNetworkPortType**") </span><span class="sxs-lookup"><span data-stu-id="d47cb-124">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_NetworkPort**](cim-networkport.md).**OtherNetworkPortType**")</span></span>
</dt> </dl>

<span data-ttu-id="d47cb-125">埠類型。</span><span class="sxs-lookup"><span data-stu-id="d47cb-125">The port type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d47cb-126">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="d47cb-126">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d47cb-127">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="d47cb-127">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d47cb-128">**不適用** (2) </span><span class="sxs-lookup"><span data-stu-id="d47cb-128">**Not Applicable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="d47cb-129">**DMTF 保留** (3. 15999) </span><span class="sxs-lookup"><span data-stu-id="d47cb-129">**DMTF Reserved** (3..15999)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="d47cb-130">**廠商保留** (16，000. 65535) </span><span class="sxs-lookup"><span data-stu-id="d47cb-130">**Vendor Reserved** (16000..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d47cb-131">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="d47cb-131">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d47cb-132">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="d47cb-132">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d47cb-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d47cb-133">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d47cb-134">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「每秒位數」 ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (」**CIM \_ LogicalPort**。**速度**") ， **PUnit** (" bit/second ") </span><span class="sxs-lookup"><span data-stu-id="d47cb-134">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalPort**.**Speed**"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="d47cb-135">要求的埠頻寬（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="d47cb-135">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="d47cb-136">實際的頻寬會在 [ **速度** ] 屬性中報告。</span><span class="sxs-lookup"><span data-stu-id="d47cb-136">The actual bandwidth is reported in the **Speed** property.</span></span>

</dd> <dt>

<span data-ttu-id="d47cb-137">**速度**</span><span class="sxs-lookup"><span data-stu-id="d47cb-137">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d47cb-138">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="d47cb-138">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d47cb-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d47cb-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d47cb-140">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「每秒位數」 ) ， **PUnit** ( 「位/秒」 ) </span><span class="sxs-lookup"><span data-stu-id="d47cb-140">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="d47cb-141">埠的頻寬（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="d47cb-141">The bandwidth of the port, in bits per second.</span></span>

</dd> <dt>

<span data-ttu-id="d47cb-142">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="d47cb-142">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d47cb-143">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d47cb-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d47cb-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d47cb-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d47cb-145">指出埠是否限制為前端或後端埠。</span><span class="sxs-lookup"><span data-stu-id="d47cb-145">Indicates whether the port is restricted to being a front-end or back-end port.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d47cb-146">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="d47cb-146">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>

<span data-ttu-id="d47cb-147">**前端** (2) </span><span class="sxs-lookup"><span data-stu-id="d47cb-147">**Front-end only** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>

<span data-ttu-id="d47cb-148"> (3) 的 **後端**</span><span class="sxs-lookup"><span data-stu-id="d47cb-148">**Back-end only** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_restricted"></span><span id="not_restricted"></span><span id="NOT_RESTRICTED"></span>

<span data-ttu-id="d47cb-149">**不受限制** (4) </span><span class="sxs-lookup"><span data-stu-id="d47cb-149">**Not restricted** (4)</span></span>


<span data-ttu-id="d47cb-150"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d47cb-150"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="d47cb-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="d47cb-151">Requirements</span></span>



| <span data-ttu-id="d47cb-152">需求</span><span class="sxs-lookup"><span data-stu-id="d47cb-152">Requirement</span></span> | <span data-ttu-id="d47cb-153">值</span><span class="sxs-lookup"><span data-stu-id="d47cb-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d47cb-154">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d47cb-154">Minimum supported client</span></span><br/> | <span data-ttu-id="d47cb-155">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d47cb-155">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="d47cb-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d47cb-156">Minimum supported server</span></span><br/> | <span data-ttu-id="d47cb-157">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d47cb-157">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="d47cb-158">命名空間</span><span class="sxs-lookup"><span data-stu-id="d47cb-158">Namespace</span></span><br/>                | <span data-ttu-id="d47cb-159">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="d47cb-159">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d47cb-160">MOF</span><span class="sxs-lookup"><span data-stu-id="d47cb-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d47cb-161"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="d47cb-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d47cb-162">DLL</span><span class="sxs-lookup"><span data-stu-id="d47cb-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d47cb-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d47cb-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d47cb-164">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d47cb-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d47cb-165">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="d47cb-165">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 


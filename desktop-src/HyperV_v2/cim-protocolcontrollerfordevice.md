---
description: 代表邏輯裝置與連線到裝置的通訊協定控制器之間的關聯。
ms.assetid: 1a1efc60-6108-4376-9f73-d2dd41443645
title: CIM_ProtocolControllerForDevice 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProtocolControllerForDevice
- CIM_ProtocolControllerForDevice.Antecedent
- CIM_ProtocolControllerForDevice.Dependent
- CIM_ProtocolControllerForDevice.DeviceNumber
- CIM_ProtocolControllerForDevice.AccessPriority
- CIM_ProtocolControllerForDevice.AccessState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7d3ef7799cccc6e8fe8e219cddfba37cf12b8637
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850619"
---
# <a name="cim_protocolcontrollerfordevice-class"></a><span data-ttu-id="f886c-103">CIM \_ ProtocolControllerForDevice 類別</span><span class="sxs-lookup"><span data-stu-id="f886c-103">CIM\_ProtocolControllerForDevice class</span></span>

<span data-ttu-id="f886c-104">代表邏輯裝置與連線到裝置的通訊協定控制器之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="f886c-104">Represents an association between a logical device and a protocol controller that is connected to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="f886c-105">語法</span><span class="sxs-lookup"><span data-stu-id="f886c-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.8.1000"), UMLPackagePath("CIM::Device::ProtocolController"), AMENDMENT]
class CIM_ProtocolControllerForDevice : CIM_Dependency
{
  CIM_ProtocolController REF Antecedent;
  CIM_LogicalDevice      REF Dependent;
  string                     DeviceNumber;
  uint16                     AccessPriority;
  uint16                     AccessState;
};
```

## <a name="members"></a><span data-ttu-id="f886c-106">成員</span><span class="sxs-lookup"><span data-stu-id="f886c-106">Members</span></span>

<span data-ttu-id="f886c-107">**CIM \_ ProtocolControllerForDevice** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f886c-107">The **CIM\_ProtocolControllerForDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="f886c-108">屬性</span><span class="sxs-lookup"><span data-stu-id="f886c-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f886c-109">屬性</span><span class="sxs-lookup"><span data-stu-id="f886c-109">Properties</span></span>

<span data-ttu-id="f886c-110">**CIM \_ ProtocolControllerForDevice** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f886c-110">The **CIM\_ProtocolControllerForDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f886c-111">**AccessPriority**</span><span class="sxs-lookup"><span data-stu-id="f886c-111">**AccessPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f886c-112">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f886c-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f886c-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f886c-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f886c-114">透過通訊協定控制器提供給裝置的存取優先權。</span><span class="sxs-lookup"><span data-stu-id="f886c-114">The access priority given to the device through the protocol controller.</span></span> <span data-ttu-id="f886c-115">最高優先順序的值最低。</span><span class="sxs-lookup"><span data-stu-id="f886c-115">The highest priority has the lowest value.</span></span>

</dd> <dt>

<span data-ttu-id="f886c-116">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="f886c-116">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f886c-117">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f886c-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f886c-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f886c-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f886c-119">邏輯裝置透過通訊協定控制器的存取範圍</span><span class="sxs-lookup"><span data-stu-id="f886c-119">The accessibility of the logical device through the protocol controller</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f886c-120">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="f886c-120">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="f886c-121">**Active** (2) </span><span class="sxs-lookup"><span data-stu-id="f886c-121">**Active** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="f886c-122">**非** 使用中 (3) </span><span class="sxs-lookup"><span data-stu-id="f886c-122">**Inactive** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Replication_In_Progress"></span><span id="replication_in_progress"></span><span id="REPLICATION_IN_PROGRESS"></span>

<span data-ttu-id="f886c-123">複寫 **進行中** (4) </span><span class="sxs-lookup"><span data-stu-id="f886c-123">**Replication In Progress** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Mapping_Inconsistency"></span><span id="mapping_inconsistency"></span><span id="MAPPING_INCONSISTENCY"></span>

<span data-ttu-id="f886c-124">**對應不一致** (5) </span><span class="sxs-lookup"><span data-stu-id="f886c-124">**Mapping Inconsistency** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f886c-125">**先行**</span><span class="sxs-lookup"><span data-stu-id="f886c-125">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f886c-126">資料類型： **CIM \_ ProtocolController**</span><span class="sxs-lookup"><span data-stu-id="f886c-126">Data type: **CIM\_ProtocolController**</span></span>
</dt> <dt>

<span data-ttu-id="f886c-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f886c-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f886c-128">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="f886c-128">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="f886c-129">關聯中的通訊協定控制器。</span><span class="sxs-lookup"><span data-stu-id="f886c-129">The protocol controller in the association.</span></span>

</dd> <dt>

<span data-ttu-id="f886c-130">**依賴**</span><span class="sxs-lookup"><span data-stu-id="f886c-130">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f886c-131">資料類型： **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="f886c-131">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="f886c-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f886c-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f886c-133">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="f886c-133">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="f886c-134">關聯中的邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="f886c-134">The logical device in the association.</span></span>

</dd> <dt>

<span data-ttu-id="f886c-135">**DeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="f886c-135">**DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f886c-136">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f886c-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f886c-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f886c-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f886c-138">通訊協定控制器內容中相關聯裝置的位址。</span><span class="sxs-lookup"><span data-stu-id="f886c-138">The address of the associated device in the context of the protocol controler.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f886c-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="f886c-139">Requirements</span></span>



| <span data-ttu-id="f886c-140">需求</span><span class="sxs-lookup"><span data-stu-id="f886c-140">Requirement</span></span> | <span data-ttu-id="f886c-141">值</span><span class="sxs-lookup"><span data-stu-id="f886c-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f886c-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f886c-142">Minimum supported client</span></span><br/> | <span data-ttu-id="f886c-143">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f886c-143">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="f886c-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f886c-144">Minimum supported server</span></span><br/> | <span data-ttu-id="f886c-145">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f886c-145">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="f886c-146">命名空間</span><span class="sxs-lookup"><span data-stu-id="f886c-146">Namespace</span></span><br/>                | <span data-ttu-id="f886c-147">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="f886c-147">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f886c-148">MOF</span><span class="sxs-lookup"><span data-stu-id="f886c-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f886c-149"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="f886c-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f886c-150">DLL</span><span class="sxs-lookup"><span data-stu-id="f886c-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f886c-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f886c-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f886c-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f886c-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f886c-153">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="f886c-153">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 


---
description: 代表 CIM \_ VirtualSystemSettingData 實例與一組 cim ResourceAllocationSettingData 實例之間關聯性的一部分 \_ 。
ms.assetid: 4f167517-079e-4b5f-885a-741ac1d1dc71
title: CIM_VirtualSystemSettingDataComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSettingDataComponent
- CIM_VirtualSystemSettingDataComponent.GroupComponent
- CIM_VirtualSystemSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: afbd7ab192c65e99f4479e5380e57dc78c8a0a9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115884"
---
# <a name="cim_virtualsystemsettingdatacomponent-class"></a><span data-ttu-id="e88c6-103">CIM \_ VirtualSystemSettingDataComponent 類別</span><span class="sxs-lookup"><span data-stu-id="e88c6-103">CIM\_VirtualSystemSettingDataComponent class</span></span>

<span data-ttu-id="e88c6-104">代表 [**cim \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) 實例與一組 [**cim \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) 實例之間關聯性的一部分。</span><span class="sxs-lookup"><span data-stu-id="e88c6-104">Represents a portion of a relationship between a [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) instance and a set of [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="e88c6-105">語法</span><span class="sxs-lookup"><span data-stu-id="e88c6-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.22.0"), UMLPackagePath("CIM::System::SystemElements"), AMENDMENT]
class CIM_VirtualSystemSettingDataComponent : CIM_Component
{
  CIM_VirtualSystemSettingData      REF GroupComponent;
  CIM_ResourceAllocationSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="e88c6-106">成員</span><span class="sxs-lookup"><span data-stu-id="e88c6-106">Members</span></span>

<span data-ttu-id="e88c6-107">**CIM \_ VirtualSystemSettingDataComponent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e88c6-107">The **CIM\_VirtualSystemSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="e88c6-108">屬性</span><span class="sxs-lookup"><span data-stu-id="e88c6-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e88c6-109">屬性</span><span class="sxs-lookup"><span data-stu-id="e88c6-109">Properties</span></span>

<span data-ttu-id="e88c6-110">**CIM \_ VirtualSystemSettingDataComponent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e88c6-110">The **CIM\_VirtualSystemSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e88c6-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="e88c6-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e88c6-112">資料類型： **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="e88c6-112">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="e88c6-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e88c6-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e88c6-114">限定詞： [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) </span><span class="sxs-lookup"><span data-stu-id="e88c6-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="e88c6-115">虛擬系統組態的最上層 [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) 物件的參考。</span><span class="sxs-lookup"><span data-stu-id="e88c6-115">A reference to the top-level [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) object of the virtual system configuration.</span></span>

</dd> <dt>

<span data-ttu-id="e88c6-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="e88c6-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e88c6-117">資料類型： **CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="e88c6-117">Data type: **CIM\_ResourceAllocationSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="e88c6-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e88c6-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e88c6-119">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) </span><span class="sxs-lookup"><span data-stu-id="e88c6-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="e88c6-120">參考表示虛擬系統組態一部分的 [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="e88c6-120">A reference the [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) object that represents a part of the virtual system configuration.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e88c6-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="e88c6-121">Requirements</span></span>



| <span data-ttu-id="e88c6-122">需求</span><span class="sxs-lookup"><span data-stu-id="e88c6-122">Requirement</span></span> | <span data-ttu-id="e88c6-123">值</span><span class="sxs-lookup"><span data-stu-id="e88c6-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e88c6-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e88c6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e88c6-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e88c6-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="e88c6-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e88c6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e88c6-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e88c6-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="e88c6-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="e88c6-128">Namespace</span></span><br/>                | <span data-ttu-id="e88c6-129">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="e88c6-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e88c6-130">MOF</span><span class="sxs-lookup"><span data-stu-id="e88c6-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e88c6-131"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="e88c6-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e88c6-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e88c6-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e88c6-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e88c6-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e88c6-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e88c6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e88c6-135">**CIM \_ 元件**</span><span class="sxs-lookup"><span data-stu-id="e88c6-135">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 


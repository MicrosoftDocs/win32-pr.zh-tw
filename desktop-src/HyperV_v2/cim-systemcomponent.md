---
description: 代表系統與組成它的其中一個專案之間的關聯。
ms.assetid: 728f25bf-3d52-4b1c-bf72-51e8ed0a4e72
title: 'CIM_SystemComponent 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemComponent
- CIM_SystemComponent.GroupComponent
- CIM_SystemComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 79bb7d3807a93b2d29157a3377d6e6a9079bfe16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848791"
---
# <a name="cim_systemcomponent-class-hyper-v-management"></a><span data-ttu-id="10819-103">CIM_SystemComponent 類別 (Hyper-v 管理) </span><span class="sxs-lookup"><span data-stu-id="10819-103">CIM_SystemComponent class (Hyper-V management)</span></span>

<span data-ttu-id="10819-104">代表系統與組成它的其中一個專案之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="10819-104">Represents an association between a system and one of the elements that compose it.</span></span>

## <a name="syntax"></a><span data-ttu-id="10819-105">語法</span><span class="sxs-lookup"><span data-stu-id="10819-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_SystemComponent : CIM_Component
{
  CIM_System               REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="10819-106">成員</span><span class="sxs-lookup"><span data-stu-id="10819-106">Members</span></span>

<span data-ttu-id="10819-107">**CIM \_ SystemComponent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="10819-107">The **CIM\_SystemComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="10819-108">屬性</span><span class="sxs-lookup"><span data-stu-id="10819-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="10819-109">屬性</span><span class="sxs-lookup"><span data-stu-id="10819-109">Properties</span></span>

<span data-ttu-id="10819-110">**CIM \_ SystemComponent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="10819-110">The **CIM\_SystemComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="10819-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="10819-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10819-112">資料類型： **CIM \_ 系統**</span><span class="sxs-lookup"><span data-stu-id="10819-112">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="10819-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10819-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10819-114">限定詞： [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) </span><span class="sxs-lookup"><span data-stu-id="10819-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="10819-115">包含 **PartComponent** 的 [**CIM \_ 系統**](cim-system.md)。</span><span class="sxs-lookup"><span data-stu-id="10819-115">The [**CIM\_System**](cim-system.md) that contains the **PartComponent**.</span></span>

</dd> <dt>

<span data-ttu-id="10819-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="10819-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10819-117">資料類型： **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="10819-117">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="10819-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10819-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10819-119">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) </span><span class="sxs-lookup"><span data-stu-id="10819-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="10819-120">屬於系統元件的子 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) 。</span><span class="sxs-lookup"><span data-stu-id="10819-120">The child [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) that is a component of the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="10819-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="10819-121">Requirements</span></span>



| <span data-ttu-id="10819-122">需求</span><span class="sxs-lookup"><span data-stu-id="10819-122">Requirement</span></span> | <span data-ttu-id="10819-123">值</span><span class="sxs-lookup"><span data-stu-id="10819-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10819-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="10819-124">Minimum supported client</span></span><br/> | <span data-ttu-id="10819-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="10819-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="10819-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="10819-126">Minimum supported server</span></span><br/> | <span data-ttu-id="10819-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="10819-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="10819-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="10819-128">Namespace</span></span><br/>                | <span data-ttu-id="10819-129">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="10819-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="10819-130">MOF</span><span class="sxs-lookup"><span data-stu-id="10819-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10819-131"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="10819-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="10819-132">DLL</span><span class="sxs-lookup"><span data-stu-id="10819-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10819-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="10819-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="10819-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10819-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10819-135">**CIM \_ 元件**</span><span class="sxs-lookup"><span data-stu-id="10819-135">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 


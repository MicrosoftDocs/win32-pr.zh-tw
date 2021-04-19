---
description: 代表系統與資源集區（系統的元件）之間的關聯。
ms.assetid: 0ac60dbd-0498-4978-b2d6-f4c9926a83a8
title: CIM_HostedResourcePool 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedResourcePool
- CIM_HostedResourcePool.GroupComponent
- CIM_HostedResourcePool.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dbb6d523b533d6e8b2f5bc1e21de93962cfd860f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973803"
---
# <a name="cim_hostedresourcepool-class"></a><span data-ttu-id="25ef9-103">CIM \_ HostedResourcePool 類別</span><span class="sxs-lookup"><span data-stu-id="25ef9-103">CIM\_HostedResourcePool class</span></span>

<span data-ttu-id="25ef9-104">代表系統與資源集區（系統的元件）之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="25ef9-104">Represents an association between a system and a resource pool that is a component of the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="25ef9-105">語法</span><span class="sxs-lookup"><span data-stu-id="25ef9-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Composition, Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource")]
class CIM_HostedResourcePool : CIM_SystemComponent
{
  CIM_System       REF GroupComponent;
  CIM_ResourcePool REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="25ef9-106">成員</span><span class="sxs-lookup"><span data-stu-id="25ef9-106">Members</span></span>

<span data-ttu-id="25ef9-107">**CIM \_ HostedResourcePool** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="25ef9-107">The **CIM\_HostedResourcePool** class has these types of members:</span></span>

-   [<span data-ttu-id="25ef9-108">屬性</span><span class="sxs-lookup"><span data-stu-id="25ef9-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="25ef9-109">屬性</span><span class="sxs-lookup"><span data-stu-id="25ef9-109">Properties</span></span>

<span data-ttu-id="25ef9-110">**CIM \_ HostedResourcePool** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="25ef9-110">The **CIM\_HostedResourcePool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="25ef9-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="25ef9-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25ef9-112">資料類型： **CIM \_ 系統**</span><span class="sxs-lookup"><span data-stu-id="25ef9-112">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="25ef9-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="25ef9-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25ef9-114">限定詞： [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) 、 [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="25ef9-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="25ef9-115">關聯中的父系統。</span><span class="sxs-lookup"><span data-stu-id="25ef9-115">The parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="25ef9-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="25ef9-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25ef9-117">資料類型： **CIM \_ ResourcePool**</span><span class="sxs-lookup"><span data-stu-id="25ef9-117">Data type: **CIM\_ResourcePool**</span></span>
</dt> <dt>

<span data-ttu-id="25ef9-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="25ef9-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25ef9-119">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) </span><span class="sxs-lookup"><span data-stu-id="25ef9-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="25ef9-120">系統元件的資源集區。</span><span class="sxs-lookup"><span data-stu-id="25ef9-120">The resource pool that is a component of the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="25ef9-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="25ef9-121">Requirements</span></span>



| <span data-ttu-id="25ef9-122">需求</span><span class="sxs-lookup"><span data-stu-id="25ef9-122">Requirement</span></span> | <span data-ttu-id="25ef9-123">值</span><span class="sxs-lookup"><span data-stu-id="25ef9-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25ef9-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="25ef9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="25ef9-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="25ef9-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="25ef9-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="25ef9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="25ef9-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="25ef9-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="25ef9-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="25ef9-128">Namespace</span></span><br/>                | <span data-ttu-id="25ef9-129">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="25ef9-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="25ef9-130">MOF</span><span class="sxs-lookup"><span data-stu-id="25ef9-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="25ef9-131"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="25ef9-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="25ef9-132">DLL</span><span class="sxs-lookup"><span data-stu-id="25ef9-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25ef9-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="25ef9-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="25ef9-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="25ef9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25ef9-135">**CIM \_ SystemComponent**</span><span class="sxs-lookup"><span data-stu-id="25ef9-135">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 


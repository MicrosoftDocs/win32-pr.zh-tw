---
description: 表示系統元件關聯的特製化，該關聯會建立資源集區是在系統的內容中定義的。
ms.assetid: 72b68687-2b5f-4fef-bdca-a5c0bbfa3564
title: Msvm_HostedResourcePool 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedResourcePool
- Msvm_HostedResourcePool.GroupComponent
- Msvm_HostedResourcePool.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d64488a845e8d51bfe27829b01ebcf0ac7d944c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847767"
---
# <a name="msvm_hostedresourcepool-class"></a><span data-ttu-id="388ff-103">Msvm \_ HostedResourcePool 類別</span><span class="sxs-lookup"><span data-stu-id="388ff-103">Msvm\_HostedResourcePool class</span></span>

<span data-ttu-id="388ff-104">表示系統元件關聯的特製化，該關聯會建立資源集區是在系統的內容中定義的。</span><span class="sxs-lookup"><span data-stu-id="388ff-104">Represents a specialization of the system component association that establishes that the resource pool is defined in the context of the system.</span></span>

<span data-ttu-id="388ff-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="388ff-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="388ff-106">語法</span><span class="sxs-lookup"><span data-stu-id="388ff-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Composition, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedResourcePool : CIM_SystemComponent
{
  Msvm_ComputerSystem REF GroupComponent;
  CIM_ResourcePool    REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="388ff-107">成員</span><span class="sxs-lookup"><span data-stu-id="388ff-107">Members</span></span>

<span data-ttu-id="388ff-108">**Msvm \_ HostedResourcePool** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="388ff-108">The **Msvm\_HostedResourcePool** class has these types of members:</span></span>

-   [<span data-ttu-id="388ff-109">屬性</span><span class="sxs-lookup"><span data-stu-id="388ff-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="388ff-110">屬性</span><span class="sxs-lookup"><span data-stu-id="388ff-110">Properties</span></span>

<span data-ttu-id="388ff-111">**Msvm \_ HostedResourcePool** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="388ff-111">The **Msvm\_HostedResourcePool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="388ff-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="388ff-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="388ff-113">資料類型： **[ **Msvm \_**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="388ff-113">Data type: **[**Msvm\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="388ff-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="388ff-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="388ff-115">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) 、 [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)、 [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="388ff-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="388ff-116">關聯中的父系統。</span><span class="sxs-lookup"><span data-stu-id="388ff-116">The parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="388ff-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="388ff-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="388ff-118">資料類型： **[ **CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="388ff-118">Data type: **[**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="388ff-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="388ff-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="388ff-120">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) </span><span class="sxs-lookup"><span data-stu-id="388ff-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="388ff-121">系統元件的資源集區。</span><span class="sxs-lookup"><span data-stu-id="388ff-121">The resource pool that is a component of the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="388ff-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="388ff-122">Requirements</span></span>



| <span data-ttu-id="388ff-123">需求</span><span class="sxs-lookup"><span data-stu-id="388ff-123">Requirement</span></span> | <span data-ttu-id="388ff-124">值</span><span class="sxs-lookup"><span data-stu-id="388ff-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="388ff-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="388ff-125">Minimum supported client</span></span><br/> | <span data-ttu-id="388ff-126">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="388ff-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="388ff-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="388ff-127">Minimum supported server</span></span><br/> | <span data-ttu-id="388ff-128">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="388ff-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="388ff-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="388ff-129">Namespace</span></span><br/>                | <span data-ttu-id="388ff-130">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="388ff-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="388ff-131">MOF</span><span class="sxs-lookup"><span data-stu-id="388ff-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="388ff-132"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="388ff-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="388ff-133">DLL</span><span class="sxs-lookup"><span data-stu-id="388ff-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="388ff-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="388ff-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


---
description: 將資源配置的實例與其配置來源的資源集區產生關聯。
ms.assetid: A2B3996D-7886-4B5F-BC89-EFDC1A48249B
title: Msvm_ResourceAllocationFromPool 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourceAllocationFromPool
- Msvm_ResourceAllocationFromPool.Antecedent
- Msvm_ResourceAllocationFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5bb3db9bce86731b12730966a7a2f6d1c9dc8946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978198"
---
# <a name="msvm_resourceallocationfrompool-class"></a><span data-ttu-id="32b01-103">Msvm \_ ResourceAllocationFromPool 類別</span><span class="sxs-lookup"><span data-stu-id="32b01-103">Msvm\_ResourceAllocationFromPool class</span></span>

<span data-ttu-id="32b01-104">將資源配置的實例與其配置來源的資源集區產生關聯。</span><span class="sxs-lookup"><span data-stu-id="32b01-104">Associates an instance of a resource allocation with the resource pool from which it is allocated.</span></span>

<span data-ttu-id="32b01-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="32b01-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="32b01-106">語法</span><span class="sxs-lookup"><span data-stu-id="32b01-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourceAllocationFromPool : CIM_ResourceAllocationFromPool
{
  CIM_ResourcePool                  REF Antecedent;
  CIM_ResourceAllocationSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="32b01-107">成員</span><span class="sxs-lookup"><span data-stu-id="32b01-107">Members</span></span>

<span data-ttu-id="32b01-108">**Msvm \_ ResourceAllocationFromPool** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="32b01-108">The **Msvm\_ResourceAllocationFromPool** class has these types of members:</span></span>

-   [<span data-ttu-id="32b01-109">屬性</span><span class="sxs-lookup"><span data-stu-id="32b01-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="32b01-110">屬性</span><span class="sxs-lookup"><span data-stu-id="32b01-110">Properties</span></span>

<span data-ttu-id="32b01-111">**Msvm \_ ResourceAllocationFromPool** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="32b01-111">The **Msvm\_ResourceAllocationFromPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="32b01-112">**先行**</span><span class="sxs-lookup"><span data-stu-id="32b01-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32b01-113">資料類型： **[ **CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="32b01-113">Data type: **[**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="32b01-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="32b01-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32b01-115">限定詞：覆 **寫**、 **最大** (1) </span><span class="sxs-lookup"><span data-stu-id="32b01-115">Qualifiers: **Override**, **Max** (1)</span></span>
</dt> </dl>

<span data-ttu-id="32b01-116">資源集區。</span><span class="sxs-lookup"><span data-stu-id="32b01-116">The resource pool.</span></span> <span data-ttu-id="32b01-117">這個屬性繼承自 [**CIM \_ ResourceAllocationFromPool**](/previous-versions//cc150673(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="32b01-117">This property is inherited from [**CIM\_ResourceAllocationFromPool**](/previous-versions//cc150673(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="32b01-118">**依賴**</span><span class="sxs-lookup"><span data-stu-id="32b01-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32b01-119">資料類型： **[ **CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span><span class="sxs-lookup"><span data-stu-id="32b01-119">Data type: **[**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span></span>
</dt> <dt>

<span data-ttu-id="32b01-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="32b01-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32b01-121">資源配置。</span><span class="sxs-lookup"><span data-stu-id="32b01-121">The resource allocation.</span></span> <span data-ttu-id="32b01-122">這個屬性繼承自 [**CIM \_ ResourceAllocationFromPool**](/previous-versions//cc150673(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="32b01-122">This property is inherited from [**CIM\_ResourceAllocationFromPool**](/previous-versions//cc150673(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="32b01-123">備註</span><span class="sxs-lookup"><span data-stu-id="32b01-123">Remarks</span></span>

<span data-ttu-id="32b01-124">存取 **Msvm \_ ResourceAllocationFromPool** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="32b01-124">Access to the **Msvm\_ResourceAllocationFromPool** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="32b01-125">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="32b01-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="32b01-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="32b01-126">Requirements</span></span>



| <span data-ttu-id="32b01-127">需求</span><span class="sxs-lookup"><span data-stu-id="32b01-127">Requirement</span></span> | <span data-ttu-id="32b01-128">值</span><span class="sxs-lookup"><span data-stu-id="32b01-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32b01-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="32b01-129">Minimum supported client</span></span><br/> | <span data-ttu-id="32b01-130">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32b01-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="32b01-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="32b01-131">Minimum supported server</span></span><br/> | <span data-ttu-id="32b01-132">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32b01-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="32b01-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="32b01-133">Namespace</span></span><br/>                | <span data-ttu-id="32b01-134">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="32b01-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="32b01-135">MOF</span><span class="sxs-lookup"><span data-stu-id="32b01-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32b01-136"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="32b01-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="32b01-137">DLL</span><span class="sxs-lookup"><span data-stu-id="32b01-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32b01-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="32b01-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="32b01-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32b01-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32b01-140">**CIM \_ ResourceAllocationFromPool**</span><span class="sxs-lookup"><span data-stu-id="32b01-140">**CIM\_ResourceAllocationFromPool**</span></span>](cim-resourceallocationfrompool.md)
</dt> <dt>

<span data-ttu-id="32b01-141">[**CIM \_ ResourceAllocationFromPool**](/previous-versions//cc150673(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="32b01-141">[**CIM\_ResourceAllocationFromPool**](/previous-versions//cc150673(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="32b01-142">**Msvm \_ ResourceAllocationFromPool (V1)**</span><span class="sxs-lookup"><span data-stu-id="32b01-142">**Msvm\_ResourceAllocationFromPool (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-resourceallocationfrompool)
</dt> <dt>

[<span data-ttu-id="32b01-143">資源管理類別</span><span class="sxs-lookup"><span data-stu-id="32b01-143">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 


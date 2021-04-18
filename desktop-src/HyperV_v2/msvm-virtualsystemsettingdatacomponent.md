---
description: 泛型關聯，用來建立一個 CIM \_ VirtualSystemSettingData 實例與一或多個 cim ResourceAllocationSettingData 實例之間的關聯性部分 \_ 。
ms.assetid: 936B41E7-1B3B-4A7B-86F0-E2F4497CE610
title: Msvm_VirtualSystemSettingDataComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSettingDataComponent
- Msvm_VirtualSystemSettingDataComponent.GroupComponent
- Msvm_VirtualSystemSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bfff3981d6fdb9fdb0368fa887c559026fc10af3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971355"
---
# <a name="msvm_virtualsystemsettingdatacomponent-class"></a><span data-ttu-id="bed4f-103">Msvm \_ VirtualSystemSettingDataComponent 類別</span><span class="sxs-lookup"><span data-stu-id="bed4f-103">Msvm\_VirtualSystemSettingDataComponent class</span></span>

<span data-ttu-id="bed4f-104">泛型關聯，用來建立一個 [**cim \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) 實例與一或多個 [**cim \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)實例之間的「部分」關聯性。</span><span class="sxs-lookup"><span data-stu-id="bed4f-104">A generic association used to establish 'part of' relationships between one instance of [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) and one or more instances of [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="bed4f-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="bed4f-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bed4f-106">語法</span><span class="sxs-lookup"><span data-stu-id="bed4f-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemSettingDataComponent : CIM_VirtualSystemSettingDataComponent
{
  CIM_VirtualSystemSettingData      REF GroupComponent;
  CIM_ResourceAllocationSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="bed4f-107">成員</span><span class="sxs-lookup"><span data-stu-id="bed4f-107">Members</span></span>

<span data-ttu-id="bed4f-108">**Msvm \_ VirtualSystemSettingDataComponent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="bed4f-108">The **Msvm\_VirtualSystemSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="bed4f-109">屬性</span><span class="sxs-lookup"><span data-stu-id="bed4f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bed4f-110">屬性</span><span class="sxs-lookup"><span data-stu-id="bed4f-110">Properties</span></span>

<span data-ttu-id="bed4f-111">**Msvm \_ VirtualSystemSettingDataComponent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="bed4f-111">The **Msvm\_VirtualSystemSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bed4f-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="bed4f-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bed4f-113">資料類型： **[ **CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="bed4f-113">Data type: **[**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="bed4f-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bed4f-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bed4f-115">限定詞：覆 **寫**、 **最小** (1) 、 **最大** (1) </span><span class="sxs-lookup"><span data-stu-id="bed4f-115">Qualifiers: **Override**, **Min** (1), **Max** (1)</span></span>
</dt> </dl>

<span data-ttu-id="bed4f-116">關聯中的父元素。</span><span class="sxs-lookup"><span data-stu-id="bed4f-116">The parent element in the association.</span></span> <span data-ttu-id="bed4f-117">這個屬性繼承自 [**CIM \_ VirtualSystemSettingDataComponent**](/previous-versions//cc150674(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="bed4f-117">This property is inherited from [**CIM\_VirtualSystemSettingDataComponent**](/previous-versions//cc150674(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="bed4f-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="bed4f-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bed4f-119">資料類型： **[ **CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span><span class="sxs-lookup"><span data-stu-id="bed4f-119">Data type: **[**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span></span>
</dt> <dt>

<span data-ttu-id="bed4f-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bed4f-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bed4f-121">關聯中的子項目。</span><span class="sxs-lookup"><span data-stu-id="bed4f-121">The child element in the association.</span></span> <span data-ttu-id="bed4f-122">這個屬性繼承自 [**CIM \_ VirtualSystemSettingDataComponent**](/previous-versions//cc150674(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="bed4f-122">This property is inherited from [**CIM\_VirtualSystemSettingDataComponent**](/previous-versions//cc150674(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bed4f-123">備註</span><span class="sxs-lookup"><span data-stu-id="bed4f-123">Remarks</span></span>

<span data-ttu-id="bed4f-124">存取 **Msvm \_ VirtualSystemSettingDataComponent** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="bed4f-124">Access to the **Msvm\_VirtualSystemSettingDataComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="bed4f-125">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="bed4f-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="bed4f-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="bed4f-126">Requirements</span></span>



| <span data-ttu-id="bed4f-127">需求</span><span class="sxs-lookup"><span data-stu-id="bed4f-127">Requirement</span></span> | <span data-ttu-id="bed4f-128">值</span><span class="sxs-lookup"><span data-stu-id="bed4f-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bed4f-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bed4f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="bed4f-130">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bed4f-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bed4f-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bed4f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="bed4f-132">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bed4f-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bed4f-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="bed4f-133">Namespace</span></span><br/>                | <span data-ttu-id="bed4f-134">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="bed4f-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bed4f-135">MOF</span><span class="sxs-lookup"><span data-stu-id="bed4f-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bed4f-136"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="bed4f-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bed4f-137">DLL</span><span class="sxs-lookup"><span data-stu-id="bed4f-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bed4f-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bed4f-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bed4f-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bed4f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bed4f-140">**CIM \_ VirtualSystemSettingDataComponent**</span><span class="sxs-lookup"><span data-stu-id="bed4f-140">**CIM\_VirtualSystemSettingDataComponent**</span></span>](cim-virtualsystemsettingdatacomponent.md)
</dt> <dt>

<span data-ttu-id="bed4f-141">[**CIM \_ VirtualSystemSettingDataComponent**](/previous-versions//cc150674(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bed4f-141">[**CIM\_VirtualSystemSettingDataComponent**](/previous-versions//cc150674(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="bed4f-142">虛擬系統類別</span><span class="sxs-lookup"><span data-stu-id="bed4f-142">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 


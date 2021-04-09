---
description: 將虛擬機器實例與代表實體、裝載系統的電腦系統物件產生關聯。
ms.assetid: 755624D7-04D0-47EA-8623-DEDE6B1D5CBC
title: Msvm_HostedDependency 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedDependency
- Msvm_HostedDependency.Antecedent
- Msvm_HostedDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ce580e6b478dbdf320377c2738708d0eb7689fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847768"
---
# <a name="msvm_hosteddependency-class"></a><span data-ttu-id="258c1-103">Msvm \_ HostedDependency 類別</span><span class="sxs-lookup"><span data-stu-id="258c1-103">Msvm\_HostedDependency class</span></span>

<span data-ttu-id="258c1-104">將虛擬機器實例與代表實體、裝載系統的電腦系統物件產生關聯。</span><span class="sxs-lookup"><span data-stu-id="258c1-104">Associates a virtual machine instance with the computer system object that represents the physical, hosting system.</span></span>

<span data-ttu-id="258c1-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="258c1-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="258c1-106">語法</span><span class="sxs-lookup"><span data-stu-id="258c1-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedDependency : CIM_HostedDependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="258c1-107">成員</span><span class="sxs-lookup"><span data-stu-id="258c1-107">Members</span></span>

<span data-ttu-id="258c1-108">**Msvm \_ HostedDependency** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="258c1-108">The **Msvm\_HostedDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="258c1-109">屬性</span><span class="sxs-lookup"><span data-stu-id="258c1-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="258c1-110">屬性</span><span class="sxs-lookup"><span data-stu-id="258c1-110">Properties</span></span>

<span data-ttu-id="258c1-111">**Msvm \_ HostedDependency** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="258c1-111">The **Msvm\_HostedDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="258c1-112">**先行**</span><span class="sxs-lookup"><span data-stu-id="258c1-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="258c1-113">資料類型： **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="258c1-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="258c1-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="258c1-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="258c1-115">主控電腦系統的參考。</span><span class="sxs-lookup"><span data-stu-id="258c1-115">A reference to the hosting computer system.</span></span> <span data-ttu-id="258c1-116">這個屬性繼承自 [**CIM \_ HostedDependency**](/previous-versions//cc136861(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="258c1-116">This property is inherited from [**CIM\_HostedDependency**](/previous-versions//cc136861(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="258c1-117">**依賴**</span><span class="sxs-lookup"><span data-stu-id="258c1-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="258c1-118">資料類型： **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="258c1-118">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="258c1-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="258c1-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="258c1-120">虛擬機器的參考。</span><span class="sxs-lookup"><span data-stu-id="258c1-120">A reference to the virtual machine.</span></span> <span data-ttu-id="258c1-121">這個屬性繼承自 [**CIM \_ HostedDependency**](/previous-versions//cc136861(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="258c1-121">This property is inherited from [**CIM\_HostedDependency**](/previous-versions//cc136861(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="258c1-122">備註</span><span class="sxs-lookup"><span data-stu-id="258c1-122">Remarks</span></span>

<span data-ttu-id="258c1-123">存取 **Msvm \_ HostedDependency** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="258c1-123">Access to the **Msvm\_HostedDependency** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="258c1-124">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="258c1-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="258c1-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="258c1-125">Requirements</span></span>



| <span data-ttu-id="258c1-126">需求</span><span class="sxs-lookup"><span data-stu-id="258c1-126">Requirement</span></span> | <span data-ttu-id="258c1-127">值</span><span class="sxs-lookup"><span data-stu-id="258c1-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="258c1-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="258c1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="258c1-129">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="258c1-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="258c1-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="258c1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="258c1-131">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="258c1-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="258c1-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="258c1-132">Namespace</span></span><br/>                | <span data-ttu-id="258c1-133">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="258c1-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="258c1-134">MOF</span><span class="sxs-lookup"><span data-stu-id="258c1-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="258c1-135"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="258c1-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="258c1-136">DLL</span><span class="sxs-lookup"><span data-stu-id="258c1-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="258c1-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="258c1-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="258c1-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="258c1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="258c1-139">**CIM \_ HostedDependency**</span><span class="sxs-lookup"><span data-stu-id="258c1-139">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> <dt>

<span data-ttu-id="258c1-140">[**CIM \_ HostedDependency**](/previous-versions//cc136861(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="258c1-140">[**CIM\_HostedDependency**](/previous-versions//cc136861(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="258c1-141">虛擬系統管理類別</span><span class="sxs-lookup"><span data-stu-id="258c1-141">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 


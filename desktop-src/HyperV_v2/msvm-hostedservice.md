---
description: 將服務與其主控電腦系統產生關聯。
ms.assetid: 888ABA71-6D67-4933-89E6-40F731AA7153
title: Msvm_HostedService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedService
- Msvm_HostedService.Antecedent
- Msvm_HostedService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 284254d32e788e374d56b3822f5c00868552e1f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996596"
---
# <a name="msvm_hostedservice-class"></a><span data-ttu-id="35300-103">Msvm \_ HostedService 類別</span><span class="sxs-lookup"><span data-stu-id="35300-103">Msvm\_HostedService class</span></span>

<span data-ttu-id="35300-104">將服務與其主控電腦系統產生關聯。</span><span class="sxs-lookup"><span data-stu-id="35300-104">Associates a service with its hosting computer system.</span></span> <span data-ttu-id="35300-105">您可以透過與主機之間的關聯，探索 [**Msvm \_ VirtualizationManagementService**](msvm-virtualsystemmanagementservice.md) 的實例。</span><span class="sxs-lookup"><span data-stu-id="35300-105">Instances of [**Msvm\_VirtualizationManagementService**](msvm-virtualsystemmanagementservice.md) can be discovered through their association with a host.</span></span>

<span data-ttu-id="35300-106">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="35300-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="35300-107">語法</span><span class="sxs-lookup"><span data-stu-id="35300-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedService : CIM_HostedService
{
  CIM_ManagedElement REF Antecedent;
  CIM_Service        REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="35300-108">成員</span><span class="sxs-lookup"><span data-stu-id="35300-108">Members</span></span>

<span data-ttu-id="35300-109">**Msvm 的 \_ HostedService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="35300-109">The **Msvm\_HostedService** class has these types of members:</span></span>

-   [<span data-ttu-id="35300-110">屬性</span><span class="sxs-lookup"><span data-stu-id="35300-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="35300-111">屬性</span><span class="sxs-lookup"><span data-stu-id="35300-111">Properties</span></span>

<span data-ttu-id="35300-112">**Msvm 的 \_ HostedService** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="35300-112">The **Msvm\_HostedService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="35300-113">**先行**</span><span class="sxs-lookup"><span data-stu-id="35300-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35300-114">資料類型： **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="35300-114">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="35300-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="35300-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35300-116">主控電腦系統的參考。</span><span class="sxs-lookup"><span data-stu-id="35300-116">A reference to the hosting computer system.</span></span> <span data-ttu-id="35300-117">這個屬性繼承自 [**CIM \_ HostedService**](/windows/desktop/CIMWin32Prov/cim-hostedservice)。</span><span class="sxs-lookup"><span data-stu-id="35300-117">This property is inherited from [**CIM\_HostedService**](/windows/desktop/CIMWin32Prov/cim-hostedservice).</span></span>

</dd> <dt>

<span data-ttu-id="35300-118">**依賴**</span><span class="sxs-lookup"><span data-stu-id="35300-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35300-119">資料類型： **[ **CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)**</span><span class="sxs-lookup"><span data-stu-id="35300-119">Data type: **[**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service)**</span></span>
</dt> <dt>

<span data-ttu-id="35300-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="35300-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35300-121">所裝載之服務的參考。</span><span class="sxs-lookup"><span data-stu-id="35300-121">A reference to the service being hosted.</span></span> <span data-ttu-id="35300-122">這個屬性繼承自 [**CIM \_ HostedService**](/windows/desktop/CIMWin32Prov/cim-hostedservice)。</span><span class="sxs-lookup"><span data-stu-id="35300-122">This property is inherited from [**CIM\_HostedService**](/windows/desktop/CIMWin32Prov/cim-hostedservice).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="35300-123">備註</span><span class="sxs-lookup"><span data-stu-id="35300-123">Remarks</span></span>

<span data-ttu-id="35300-124">**Msvm \_ HostedService** 類別的存取權可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="35300-124">Access to the **Msvm\_HostedService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="35300-125">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="35300-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="35300-126">範例</span><span class="sxs-lookup"><span data-stu-id="35300-126">Examples</span></span>

<span data-ttu-id="35300-127">請參閱 [查詢網路物件](querying-networking-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="35300-127">See [Querying Networking Objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="35300-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="35300-128">Requirements</span></span>



| <span data-ttu-id="35300-129">需求</span><span class="sxs-lookup"><span data-stu-id="35300-129">Requirement</span></span> | <span data-ttu-id="35300-130">值</span><span class="sxs-lookup"><span data-stu-id="35300-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35300-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="35300-131">Minimum supported client</span></span><br/> | <span data-ttu-id="35300-132">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="35300-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="35300-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="35300-133">Minimum supported server</span></span><br/> | <span data-ttu-id="35300-134">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="35300-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="35300-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="35300-135">Namespace</span></span><br/>                | <span data-ttu-id="35300-136">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="35300-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="35300-137">MOF</span><span class="sxs-lookup"><span data-stu-id="35300-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35300-138"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="35300-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="35300-139">DLL</span><span class="sxs-lookup"><span data-stu-id="35300-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35300-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="35300-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="35300-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35300-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35300-142">**CIM \_ HostedService**</span><span class="sxs-lookup"><span data-stu-id="35300-142">**CIM\_HostedService**</span></span>](cim-hostedservice.md)
</dt> <dt>

[<span data-ttu-id="35300-143">**CIM \_ HostedService**</span><span class="sxs-lookup"><span data-stu-id="35300-143">**CIM\_HostedService**</span></span>](/windows/desktop/CIMWin32Prov/cim-hostedservice)
</dt> <dt>

[<span data-ttu-id="35300-144">虛擬系統管理類別</span><span class="sxs-lookup"><span data-stu-id="35300-144">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 


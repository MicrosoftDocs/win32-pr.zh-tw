---
description: 服務存取點之間的關聯 (SAP) 與其如何實行。
ms.assetid: 36108521-A699-4498-A962-DC0801D9EE81
title: Msvm_DeviceSAPImplementation 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DeviceSAPImplementation
- Msvm_DeviceSAPImplementation.Antecedent
- Msvm_DeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9551d4409edfdfca18b66e3a3b86d6adcb28b19c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983755"
---
# <a name="msvm_devicesapimplementation-class"></a><span data-ttu-id="cddba-103">Msvm \_ DeviceSAPImplementation 類別</span><span class="sxs-lookup"><span data-stu-id="cddba-103">Msvm\_DeviceSAPImplementation class</span></span>

<span data-ttu-id="cddba-104">服務存取點之間的關聯 (SAP) 與其如何實行。</span><span class="sxs-lookup"><span data-stu-id="cddba-104">An association between a service access point (SAP) and how it is implemented.</span></span> <span data-ttu-id="cddba-105">此關聯的基數為多對多。</span><span class="sxs-lookup"><span data-stu-id="cddba-105">The cardinality of this association is many-to-many.</span></span> <span data-ttu-id="cddba-106">SAP 可由一個以上的邏輯裝置提供，並結合運作。</span><span class="sxs-lookup"><span data-stu-id="cddba-106">A SAP can be provided by more than one logical device, operating in conjunction.</span></span> <span data-ttu-id="cddba-107">任何裝置都可以提供一個以上的 SAP。</span><span class="sxs-lookup"><span data-stu-id="cddba-107">Any device can provide more than one SAP.</span></span> <span data-ttu-id="cddba-108">當有許多邏輯裝置與單一 SAP 相關聯時，會假設這些專案會一起運作以提供存取點。</span><span class="sxs-lookup"><span data-stu-id="cddba-108">When many logical devices are associated with a single SAP, it is assumed that these elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="cddba-109">如果有不同的 SAP 執行，則每個執行都會導致 SAP 物件的個別具現化。</span><span class="sxs-lookup"><span data-stu-id="cddba-109">If different implementations of a SAP exist, each of these implementations would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="cddba-110">這些個別的具現化會與唯一的實作為關聯。</span><span class="sxs-lookup"><span data-stu-id="cddba-110">These individual instantiations would then have associations to the unique implementations.</span></span>

<span data-ttu-id="cddba-111">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="cddba-111">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cddba-112">語法</span><span class="sxs-lookup"><span data-stu-id="cddba-112">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_LogicalDevice      REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="cddba-113">成員</span><span class="sxs-lookup"><span data-stu-id="cddba-113">Members</span></span>

<span data-ttu-id="cddba-114">**Msvm \_ DeviceSAPImplementation** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="cddba-114">The **Msvm\_DeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="cddba-115">屬性</span><span class="sxs-lookup"><span data-stu-id="cddba-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cddba-116">屬性</span><span class="sxs-lookup"><span data-stu-id="cddba-116">Properties</span></span>

<span data-ttu-id="cddba-117">**Msvm \_ DeviceSAPImplementation** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="cddba-117">The **Msvm\_DeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cddba-118">**先行**</span><span class="sxs-lookup"><span data-stu-id="cddba-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cddba-119">資料類型： **[ **CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span><span class="sxs-lookup"><span data-stu-id="cddba-119">Data type: **[**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span></span>
</dt> <dt>

<span data-ttu-id="cddba-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cddba-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cddba-121">邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="cddba-121">The logical device.</span></span> <span data-ttu-id="cddba-122">這個屬性繼承自 [**CIM \_ DeviceSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation)。</span><span class="sxs-lookup"><span data-stu-id="cddba-122">This property is inherited from [**CIM\_DeviceSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).</span></span>

</dd> <dt>

<span data-ttu-id="cddba-123">**依賴**</span><span class="sxs-lookup"><span data-stu-id="cddba-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cddba-124">資料類型： **[ **CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)**</span><span class="sxs-lookup"><span data-stu-id="cddba-124">Data type: **[**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)**</span></span>
</dt> <dt>

<span data-ttu-id="cddba-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cddba-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cddba-126">使用邏輯裝置執行的服務存取點。</span><span class="sxs-lookup"><span data-stu-id="cddba-126">The service access point implemented using the logical device.</span></span> <span data-ttu-id="cddba-127">這個屬性繼承自 [**CIM \_ DeviceSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation)。</span><span class="sxs-lookup"><span data-stu-id="cddba-127">This property is inherited from [**CIM\_DeviceSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cddba-128">備註</span><span class="sxs-lookup"><span data-stu-id="cddba-128">Remarks</span></span>

<span data-ttu-id="cddba-129">存取 **Msvm \_ DeviceSAPImplementation** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="cddba-129">Access to the **Msvm\_DeviceSAPImplementation** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="cddba-130">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="cddba-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="cddba-131">範例</span><span class="sxs-lookup"><span data-stu-id="cddba-131">Examples</span></span>

<span data-ttu-id="cddba-132">請參閱 [查詢網路物件](querying-networking-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="cddba-132">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cddba-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="cddba-133">Requirements</span></span>



| <span data-ttu-id="cddba-134">需求</span><span class="sxs-lookup"><span data-stu-id="cddba-134">Requirement</span></span> | <span data-ttu-id="cddba-135">值</span><span class="sxs-lookup"><span data-stu-id="cddba-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cddba-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cddba-136">Minimum supported client</span></span><br/> | <span data-ttu-id="cddba-137">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cddba-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="cddba-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cddba-138">Minimum supported server</span></span><br/> | <span data-ttu-id="cddba-139">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cddba-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cddba-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="cddba-140">Namespace</span></span><br/>                | <span data-ttu-id="cddba-141">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="cddba-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="cddba-142">MOF</span><span class="sxs-lookup"><span data-stu-id="cddba-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cddba-143"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="cddba-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cddba-144">DLL</span><span class="sxs-lookup"><span data-stu-id="cddba-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cddba-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cddba-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cddba-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cddba-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cddba-147">**CIM \_ DeviceSAPImplementation**</span><span class="sxs-lookup"><span data-stu-id="cddba-147">**CIM\_DeviceSAPImplementation**</span></span>](cim-devicesapimplementation.md)
</dt> <dt>

[<span data-ttu-id="cddba-148">**CIM \_ DeviceSAPImplementation**</span><span class="sxs-lookup"><span data-stu-id="cddba-148">**CIM\_DeviceSAPImplementation**</span></span>](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation)
</dt> </dl>

 


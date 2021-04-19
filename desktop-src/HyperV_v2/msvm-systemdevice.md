---
description: 將邏輯裝置與父系統產生關聯。
ms.assetid: 2BEAAEC8-F8F2-4CC7-A209-EE3EE3C6FA90
title: Msvm_SystemDevice 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemDevice
- Msvm_SystemDevice.GroupComponent
- Msvm_SystemDevice.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: be31a51ad4e24bd31785e64400bf5b266624d8d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998059"
---
# <a name="msvm_systemdevice-class"></a><span data-ttu-id="99d09-103">Msvm \_ SystemDevice 類別</span><span class="sxs-lookup"><span data-stu-id="99d09-103">Msvm\_SystemDevice class</span></span>

<span data-ttu-id="99d09-104">邏輯裝置可由系統匯總。</span><span class="sxs-lookup"><span data-stu-id="99d09-104">Logical devices can be aggregated by a system.</span></span> <span data-ttu-id="99d09-105">此關聯性是由系統裝置關聯明確進行。</span><span class="sxs-lookup"><span data-stu-id="99d09-105">This relationship is made explicit by the system device association.</span></span>

<span data-ttu-id="99d09-106">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="99d09-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="99d09-107">語法</span><span class="sxs-lookup"><span data-stu-id="99d09-107">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemDevice : CIM_SystemDevice
{
  CIM_System        REF GroupComponent;
  CIM_LogicalDevice REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="99d09-108">成員</span><span class="sxs-lookup"><span data-stu-id="99d09-108">Members</span></span>

<span data-ttu-id="99d09-109">**Msvm \_ SystemDevice** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="99d09-109">The **Msvm\_SystemDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="99d09-110">屬性</span><span class="sxs-lookup"><span data-stu-id="99d09-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="99d09-111">屬性</span><span class="sxs-lookup"><span data-stu-id="99d09-111">Properties</span></span>

<span data-ttu-id="99d09-112">**Msvm \_ SystemDevice** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="99d09-112">The **Msvm\_SystemDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="99d09-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="99d09-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="99d09-114">資料類型： **[ **CIM \_ 系統**](/windows/desktop/CIMWin32Prov/cim-system)**</span><span class="sxs-lookup"><span data-stu-id="99d09-114">Data type: **[**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system)**</span></span>
</dt> <dt>

<span data-ttu-id="99d09-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="99d09-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="99d09-116">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers)、 [**最小**](/windows/desktop/WmiSdk/standard-qualifiers) ( 1 ) 、 [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) ( 1 ) </span><span class="sxs-lookup"><span data-stu-id="99d09-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) ( 1 ), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) ( 1 )</span></span>
</dt> </dl>

<span data-ttu-id="99d09-117">關聯中的父系統。</span><span class="sxs-lookup"><span data-stu-id="99d09-117">The parent system in the association.</span></span> <span data-ttu-id="99d09-118">這個屬性繼承自 [**CIM \_ 元件**](/windows/desktop/CIMWin32Prov/cim-component)。</span><span class="sxs-lookup"><span data-stu-id="99d09-118">This property is inherited from [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component).</span></span>

</dd> <dt>

<span data-ttu-id="99d09-119">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="99d09-119">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="99d09-120">資料類型： **[ **CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span><span class="sxs-lookup"><span data-stu-id="99d09-120">Data type: **[**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span></span>
</dt> <dt>

<span data-ttu-id="99d09-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="99d09-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="99d09-122">屬於系統元素的邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="99d09-122">The logical device that is an element of a system.</span></span> <span data-ttu-id="99d09-123">這個屬性繼承自 [**CIM \_ 元件**](/windows/desktop/CIMWin32Prov/cim-component)。</span><span class="sxs-lookup"><span data-stu-id="99d09-123">This property is inherited from [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="99d09-124">備註</span><span class="sxs-lookup"><span data-stu-id="99d09-124">Remarks</span></span>

<span data-ttu-id="99d09-125">存取 **Msvm \_ SystemDevice** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="99d09-125">Access to the **Msvm\_SystemDevice** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="99d09-126">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="99d09-126">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="99d09-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="99d09-127">Requirements</span></span>



| <span data-ttu-id="99d09-128">需求</span><span class="sxs-lookup"><span data-stu-id="99d09-128">Requirement</span></span> | <span data-ttu-id="99d09-129">值</span><span class="sxs-lookup"><span data-stu-id="99d09-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99d09-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="99d09-130">Minimum supported client</span></span><br/> | <span data-ttu-id="99d09-131">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="99d09-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="99d09-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="99d09-132">Minimum supported server</span></span><br/> | <span data-ttu-id="99d09-133">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="99d09-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="99d09-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="99d09-134">Namespace</span></span><br/>                | <span data-ttu-id="99d09-135">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="99d09-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="99d09-136">MOF</span><span class="sxs-lookup"><span data-stu-id="99d09-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="99d09-137"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="99d09-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="99d09-138">DLL</span><span class="sxs-lookup"><span data-stu-id="99d09-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99d09-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="99d09-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="99d09-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="99d09-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99d09-141">**CIM \_ SystemDevice**</span><span class="sxs-lookup"><span data-stu-id="99d09-141">**CIM\_SystemDevice**</span></span>](cim-systemdevice.md)
</dt> <dt>

[<span data-ttu-id="99d09-142">**CIM \_ SystemDevice**</span><span class="sxs-lookup"><span data-stu-id="99d09-142">**CIM\_SystemDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-systemdevice)
</dt> <dt>

[<span data-ttu-id="99d09-143">虛擬系統類別</span><span class="sxs-lookup"><span data-stu-id="99d09-143">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 


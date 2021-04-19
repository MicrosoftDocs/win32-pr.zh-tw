---
description: 將已配置資源的實例與從中配置資源的資源集區產生關聯。
ms.assetid: BA3168C7-E4F1-414B-827B-1A811069F223
title: Msvm_ElementAllocatedFromPool 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementAllocatedFromPool
- Msvm_ElementAllocatedFromPool.Antecedent
- Msvm_ElementAllocatedFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4d798c31fbcd8429007c53f3b156fc7c5922e7ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987246"
---
# <a name="msvm_elementallocatedfrompool-class"></a><span data-ttu-id="84f44-103">Msvm \_ ElementAllocatedFromPool 類別</span><span class="sxs-lookup"><span data-stu-id="84f44-103">Msvm\_ElementAllocatedFromPool class</span></span>

<span data-ttu-id="84f44-104">將已配置資源的實例與從中配置資源的資源集區產生關聯。</span><span class="sxs-lookup"><span data-stu-id="84f44-104">Associates an instance of an allocated resource with the resource pool from which it was allocated.</span></span>

<span data-ttu-id="84f44-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="84f44-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="84f44-106">語法</span><span class="sxs-lookup"><span data-stu-id="84f44-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementAllocatedFromPool : CIM_ElementAllocatedFromPool
{
  CIM_ResourcePool   REF Antecedent;
  CIM_LogicalElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="84f44-107">成員</span><span class="sxs-lookup"><span data-stu-id="84f44-107">Members</span></span>

<span data-ttu-id="84f44-108">**Msvm \_ ElementAllocatedFromPool** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="84f44-108">The **Msvm\_ElementAllocatedFromPool** class has these types of members:</span></span>

-   [<span data-ttu-id="84f44-109">屬性</span><span class="sxs-lookup"><span data-stu-id="84f44-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="84f44-110">屬性</span><span class="sxs-lookup"><span data-stu-id="84f44-110">Properties</span></span>

<span data-ttu-id="84f44-111">**Msvm \_ ElementAllocatedFromPool** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="84f44-111">The **Msvm\_ElementAllocatedFromPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="84f44-112">**先行**</span><span class="sxs-lookup"><span data-stu-id="84f44-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f44-113">資料類型： **[ **CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="84f44-113">Data type: **[**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="84f44-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f44-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84f44-115">限定詞：覆 **寫**、 **最大** (1) </span><span class="sxs-lookup"><span data-stu-id="84f44-115">Qualifiers: **Override**, **Max** (1)</span></span>
</dt> </dl>

<span data-ttu-id="84f44-116">資源集區。</span><span class="sxs-lookup"><span data-stu-id="84f44-116">The resource pool.</span></span> <span data-ttu-id="84f44-117">這個屬性繼承自 [**CIM \_ ElementAllocatedFromPool**](/previous-versions//cc150668(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="84f44-117">This property is inherited from [**CIM\_ElementAllocatedFromPool**](/previous-versions//cc150668(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="84f44-118">**依賴**</span><span class="sxs-lookup"><span data-stu-id="84f44-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f44-119">資料類型： **[ **CIM \_ LogicalElement**](/windows/desktop/CIMWin32Prov/cim-logicalelement)**</span><span class="sxs-lookup"><span data-stu-id="84f44-119">Data type: **[**CIM\_LogicalElement**](/windows/desktop/CIMWin32Prov/cim-logicalelement)**</span></span>
</dt> <dt>

<span data-ttu-id="84f44-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f44-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f44-121">配置的資源。</span><span class="sxs-lookup"><span data-stu-id="84f44-121">The allocated resource.</span></span> <span data-ttu-id="84f44-122">這個屬性繼承自 [**CIM \_ ElementAllocatedFromPool**](/previous-versions//cc150668(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="84f44-122">This property is inherited from [**CIM\_ElementAllocatedFromPool**](/previous-versions//cc150668(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="84f44-123">備註</span><span class="sxs-lookup"><span data-stu-id="84f44-123">Remarks</span></span>

<span data-ttu-id="84f44-124">存取 **Msvm \_ ElementAllocatedFromPool** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="84f44-124">Access to the **Msvm\_ElementAllocatedFromPool** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="84f44-125">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="84f44-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="84f44-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="84f44-126">Requirements</span></span>



| <span data-ttu-id="84f44-127">需求</span><span class="sxs-lookup"><span data-stu-id="84f44-127">Requirement</span></span> | <span data-ttu-id="84f44-128">值</span><span class="sxs-lookup"><span data-stu-id="84f44-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84f44-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="84f44-129">Minimum supported client</span></span><br/> | <span data-ttu-id="84f44-130">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="84f44-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="84f44-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="84f44-131">Minimum supported server</span></span><br/> | <span data-ttu-id="84f44-132">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="84f44-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="84f44-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="84f44-133">Namespace</span></span><br/>                | <span data-ttu-id="84f44-134">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="84f44-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="84f44-135">MOF</span><span class="sxs-lookup"><span data-stu-id="84f44-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84f44-136"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="84f44-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="84f44-137">DLL</span><span class="sxs-lookup"><span data-stu-id="84f44-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84f44-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="84f44-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="84f44-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="84f44-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84f44-140">**CIM \_ ElementAllocatedFromPool**</span><span class="sxs-lookup"><span data-stu-id="84f44-140">**CIM\_ElementAllocatedFromPool**</span></span>](cim-elementallocatedfrompool.md)
</dt> <dt>

<span data-ttu-id="84f44-141">[**CIM \_ ElementAllocatedFromPool**](/previous-versions//cc150668(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="84f44-141">[**CIM\_ElementAllocatedFromPool**](/previous-versions//cc150668(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="84f44-142">**Msvm \_ ElementAllocatedFromPool (V1)**</span><span class="sxs-lookup"><span data-stu-id="84f44-142">**Msvm\_ElementAllocatedFromPool (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-elementallocatedfrompool)
</dt> <dt>

[<span data-ttu-id="84f44-143">資源管理類別</span><span class="sxs-lookup"><span data-stu-id="84f44-143">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 


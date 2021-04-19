---
description: 代表 managed 元素與其功能之間的關聯。
ms.assetid: F083E6D2-CC74-4DAD-8FF7-3FE3CA4EEFFF
title: Msvm_ElementCapabilities 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementCapabilities
- Msvm_ElementCapabilities.ManagedElement
- Msvm_ElementCapabilities.Capabilities
- Msvm_ElementCapabilities.Characteristics
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d7602de569a51aec73130a4b5f4d3ba339cb29c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975165"
---
# <a name="msvm_elementcapabilities-class"></a><span data-ttu-id="6ced8-103">Msvm \_ ElementCapabilities 類別</span><span class="sxs-lookup"><span data-stu-id="6ced8-103">Msvm\_ElementCapabilities class</span></span>

<span data-ttu-id="6ced8-104">代表 managed 元素與其功能之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="6ced8-104">Represents the association between managed elements and their capabilities.</span></span>

<span data-ttu-id="6ced8-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="6ced8-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ced8-106">語法</span><span class="sxs-lookup"><span data-stu-id="6ced8-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementCapabilities : CIM_ElementCapabilities
{
  CIM_ManagedElement REF ManagedElement;
  CIM_Capabilities   REF Capabilities;
  uint16                 Characteristics[];
};
```

## <a name="members"></a><span data-ttu-id="6ced8-107">成員</span><span class="sxs-lookup"><span data-stu-id="6ced8-107">Members</span></span>

<span data-ttu-id="6ced8-108">**Msvm \_ ElementCapabilities** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6ced8-108">The **Msvm\_ElementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="6ced8-109">屬性</span><span class="sxs-lookup"><span data-stu-id="6ced8-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6ced8-110">屬性</span><span class="sxs-lookup"><span data-stu-id="6ced8-110">Properties</span></span>

<span data-ttu-id="6ced8-111">**Msvm \_ ElementCapabilities** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6ced8-111">The **Msvm\_ElementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6ced8-112">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="6ced8-112">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ced8-113">資料類型： **[ **CIM \_ 功能**](/previous-versions//cc136806(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="6ced8-113">Data type: **[**CIM\_Capabilities**](/previous-versions//cc136806(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="6ced8-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ced8-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ced8-115">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="6ced8-115">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="6ced8-116">與元素相關聯的功能物件。</span><span class="sxs-lookup"><span data-stu-id="6ced8-116">The capabilities object associated with the element.</span></span> <span data-ttu-id="6ced8-117">這個屬性繼承自 [**CIM \_ ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)。</span><span class="sxs-lookup"><span data-stu-id="6ced8-117">This property is inherited from [**CIM\_ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span></span>

</dd> <dt>

<span data-ttu-id="6ced8-118">**特性**</span><span class="sxs-lookup"><span data-stu-id="6ced8-118">**Characteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ced8-119">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="6ced8-119">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6ced8-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ced8-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ced8-121">提供有關功能的描述性資訊。</span><span class="sxs-lookup"><span data-stu-id="6ced8-121">Provides descriptive information about the capabilities.</span></span> <span data-ttu-id="6ced8-122">這個屬性繼承自 [**CIM \_ ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)。</span><span class="sxs-lookup"><span data-stu-id="6ced8-122">This property is inherited from [**CIM\_ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span></span>



| <span data-ttu-id="6ced8-123">值</span><span class="sxs-lookup"><span data-stu-id="6ced8-123">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="6ced8-124">意義</span><span class="sxs-lookup"><span data-stu-id="6ced8-124">Meaning</span></span>                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="Default"></span><span id="default"></span><span id="DEFAULT"></span><dl> <span data-ttu-id="6ced8-125"><dt>**預設值**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6ced8-125"><dt>**Default**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="6ced8-126">相關聯的功能代表 managed 元素的預設功能。</span><span class="sxs-lookup"><span data-stu-id="6ced8-126">The associated capabilities represent the default capabilities of the managed element.</span></span><br/> |
| <span id="Current"></span><span id="current"></span><span id="CURRENT"></span><dl> <span data-ttu-id="6ced8-127"><dt>**目前**</dt>的 <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="6ced8-127"><dt>**Current**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="6ced8-128">相關聯的功能代表 managed 元素目前的功能。</span><span class="sxs-lookup"><span data-stu-id="6ced8-128">The associated capabilities represent the current capabilities of the managed element.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6ced8-129">**ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="6ced8-129">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ced8-130">資料類型： **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="6ced8-130">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="6ced8-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6ced8-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ced8-132">限定詞： **Key**、 **Min** ( 1 ) </span><span class="sxs-lookup"><span data-stu-id="6ced8-132">Qualifiers: **Key**, **Min** ( 1 )</span></span>
</dt> </dl>

<span data-ttu-id="6ced8-133">Managed 元素。</span><span class="sxs-lookup"><span data-stu-id="6ced8-133">The managed element.</span></span> <span data-ttu-id="6ced8-134">這個屬性繼承自 [**CIM \_ ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)。</span><span class="sxs-lookup"><span data-stu-id="6ced8-134">This property is inherited from [**CIM\_ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6ced8-135">備註</span><span class="sxs-lookup"><span data-stu-id="6ced8-135">Remarks</span></span>

<span data-ttu-id="6ced8-136">存取 **Msvm \_ ElementCapabilities** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="6ced8-136">Access to the **Msvm\_ElementCapabilities** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="6ced8-137">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="6ced8-137">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="6ced8-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ced8-138">Requirements</span></span>



| <span data-ttu-id="6ced8-139">需求</span><span class="sxs-lookup"><span data-stu-id="6ced8-139">Requirement</span></span> | <span data-ttu-id="6ced8-140">值</span><span class="sxs-lookup"><span data-stu-id="6ced8-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ced8-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6ced8-141">Minimum supported client</span></span><br/> | <span data-ttu-id="6ced8-142">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6ced8-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6ced8-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6ced8-143">Minimum supported server</span></span><br/> | <span data-ttu-id="6ced8-144">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6ced8-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6ced8-145">命名空間</span><span class="sxs-lookup"><span data-stu-id="6ced8-145">Namespace</span></span><br/>                | <span data-ttu-id="6ced8-146">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="6ced8-146">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6ced8-147">MOF</span><span class="sxs-lookup"><span data-stu-id="6ced8-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ced8-148"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="6ced8-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ced8-149">DLL</span><span class="sxs-lookup"><span data-stu-id="6ced8-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ced8-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6ced8-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6ced8-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6ced8-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ced8-152">**CIM \_ ElementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="6ced8-152">**CIM\_ElementCapabilities**</span></span>](cim-elementcapabilities.md)
</dt> <dt>

[<span data-ttu-id="6ced8-153">**CIM \_ ElementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="6ced8-153">**CIM\_ElementCapabilities**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)
</dt> <dt>

[<span data-ttu-id="6ced8-154">**Msvm \_ ElementCapabilities (V1)**</span><span class="sxs-lookup"><span data-stu-id="6ced8-154">**Msvm\_ElementCapabilities (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-elementcapabilities)
</dt> </dl>

 


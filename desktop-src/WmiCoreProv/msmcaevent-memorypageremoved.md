---
description: 指出記憶體頁面已從系統使用中移除，因為發生過多的硬體錯誤檢查，並修正 (ECC) 錯誤。 此類別僅適用于64位的 Windows 系統。
ms.assetid: 364a2520-8d7c-44f2-95f6-eea9a5531975
title: MSMCAEvent_MemoryPageRemoved 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_MemoryPageRemoved
- MSMCAEvent_MemoryPageRemoved.Active
- MSMCAEvent_MemoryPageRemoved.InstanceName
- MSMCAEvent_MemoryPageRemoved.PhysicalAddress
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: dc29c5b51531e204ab50f062dd08ef8d5abf1bbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985053"
---
# <a name="msmcaevent_memorypageremoved-class"></a><span data-ttu-id="968f9-104">MSMCAEvent \_ MemoryPageRemoved 類別</span><span class="sxs-lookup"><span data-stu-id="968f9-104">MSMCAEvent\_MemoryPageRemoved class</span></span>

<span data-ttu-id="968f9-105">**MSMCAEvent \_ MemoryPageRemoved** 類別指出記憶體頁面已從系統使用中移除，因為發生過多硬體錯誤檢查和修正 (ECC) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="968f9-105">The **MSMCAEvent\_MemoryPageRemoved** class indicates that a memory page has been removed from system use due to excessive hardware Error Checking and Correcting (ECC) errors.</span></span> <span data-ttu-id="968f9-106">此類別僅適用于64位的 Windows 系統。</span><span class="sxs-lookup"><span data-stu-id="968f9-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="968f9-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="968f9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="968f9-108">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="968f9-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="968f9-109">語法</span><span class="sxs-lookup"><span data-stu-id="968f9-109">Syntax</span></span>

``` syntax
class MSMCAEvent_MemoryPageRemoved : WmiEvent
{
  boolean Active;
  string  InstanceName;
  uint64  PhysicalAddress;
};
```

## <a name="members"></a><span data-ttu-id="968f9-110">成員</span><span class="sxs-lookup"><span data-stu-id="968f9-110">Members</span></span>

<span data-ttu-id="968f9-111">**MSMCAEvent \_ MemoryPageRemoved** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="968f9-111">The **MSMCAEvent\_MemoryPageRemoved** class has these types of members:</span></span>

-   [<span data-ttu-id="968f9-112">屬性</span><span class="sxs-lookup"><span data-stu-id="968f9-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="968f9-113">屬性</span><span class="sxs-lookup"><span data-stu-id="968f9-113">Properties</span></span>

<span data-ttu-id="968f9-114">**MSMCAEvent \_ MemoryPageRemoved** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="968f9-114">The **MSMCAEvent\_MemoryPageRemoved** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="968f9-115">**使用中**</span><span class="sxs-lookup"><span data-stu-id="968f9-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="968f9-116">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="968f9-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="968f9-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="968f9-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="968f9-118">如果此類別的實例為使用中，則 **為 TRUE**;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="968f9-118">**TRUE**, if this instance of the class is active; otherwise **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="968f9-119">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="968f9-119">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="968f9-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="968f9-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="968f9-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="968f9-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="968f9-122">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="968f9-122">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="968f9-123">這個類別實例的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="968f9-123">Unique identifier for this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="968f9-124">**PhysicalAddress**</span><span class="sxs-lookup"><span data-stu-id="968f9-124">**PhysicalAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="968f9-125">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="968f9-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="968f9-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="968f9-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="968f9-127">已移除之記憶體頁面的位址。</span><span class="sxs-lookup"><span data-stu-id="968f9-127">Address of the page of memory that has been removed.</span></span>

<span data-ttu-id="968f9-128">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="968f9-128">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="968f9-129">備註</span><span class="sxs-lookup"><span data-stu-id="968f9-129">Remarks</span></span>

<span data-ttu-id="968f9-130">**MSMCAEvent \_ MemoryPageRemoved** 類別衍生自 [**>register-wmievent**](wmievent.md)。</span><span class="sxs-lookup"><span data-stu-id="968f9-130">The **MSMCAEvent\_MemoryPageRemoved** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="968f9-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="968f9-131">Requirements</span></span>



| <span data-ttu-id="968f9-132">需求</span><span class="sxs-lookup"><span data-stu-id="968f9-132">Requirement</span></span> | <span data-ttu-id="968f9-133">值</span><span class="sxs-lookup"><span data-stu-id="968f9-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="968f9-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="968f9-134">Minimum supported client</span></span><br/> | <span data-ttu-id="968f9-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="968f9-135">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="968f9-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="968f9-136">Minimum supported server</span></span><br/> | <span data-ttu-id="968f9-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="968f9-137">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="968f9-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="968f9-138">Namespace</span></span><br/>                | <span data-ttu-id="968f9-139">根 \\ wmi</span><span class="sxs-lookup"><span data-stu-id="968f9-139">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="968f9-140">MOF</span><span class="sxs-lookup"><span data-stu-id="968f9-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="968f9-141"><dt>Wmicore mof</dt></span><span class="sxs-lookup"><span data-stu-id="968f9-141"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="968f9-142">DLL</span><span class="sxs-lookup"><span data-stu-id="968f9-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="968f9-143"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="968f9-143"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="968f9-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="968f9-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="968f9-145">MSMCA 類別</span><span class="sxs-lookup"><span data-stu-id="968f9-145">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="968f9-146">**>register-wmievent**</span><span class="sxs-lookup"><span data-stu-id="968f9-146">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 


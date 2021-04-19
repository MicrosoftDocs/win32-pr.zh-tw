---
description: 包含已更正的平臺事件 (CPE) 。 此類別僅適用于64位的 Windows 系統。
ms.assetid: b24a390e-293d-4dd4-b747-33c298a5d45f
title: MSMCAInfo_RawCorrectedPlatformEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawCorrectedPlatformEvent
- MSMCAInfo_RawCorrectedPlatformEvent.Active
- MSMCAInfo_RawCorrectedPlatformEvent.Count
- MSMCAInfo_RawCorrectedPlatformEvent.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 906587ca9ee153eb93542c3e749e8164e6a5ee7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988950"
---
# <a name="msmcainfo_rawcorrectedplatformevent-class"></a><span data-ttu-id="0ca32-104">MSMCAInfo \_ RawCorrectedPlatformEvent 類別</span><span class="sxs-lookup"><span data-stu-id="0ca32-104">MSMCAInfo\_RawCorrectedPlatformEvent class</span></span>

<span data-ttu-id="0ca32-105">**MSMCAInfo \_ RawCorrectedPlatformEvent** 類別包含已更正的平臺事件 (CPE) 。</span><span class="sxs-lookup"><span data-stu-id="0ca32-105">The **MSMCAInfo\_RawCorrectedPlatformEvent** class contains a Corrected Platform Event (CPE).</span></span> <span data-ttu-id="0ca32-106">此類別僅適用于64位的 Windows 系統。</span><span class="sxs-lookup"><span data-stu-id="0ca32-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="0ca32-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="0ca32-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="0ca32-108">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="0ca32-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ca32-109">語法</span><span class="sxs-lookup"><span data-stu-id="0ca32-109">Syntax</span></span>

``` syntax
class MSMCAInfo_RawCorrectedPlatformEvent : WMIEvent
{
  boolean         Active;
  uint32          Count;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a><span data-ttu-id="0ca32-110">成員</span><span class="sxs-lookup"><span data-stu-id="0ca32-110">Members</span></span>

<span data-ttu-id="0ca32-111">**MSMCAInfo \_ RawCorrectedPlatformEvent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0ca32-111">The **MSMCAInfo\_RawCorrectedPlatformEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="0ca32-112">屬性</span><span class="sxs-lookup"><span data-stu-id="0ca32-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0ca32-113">屬性</span><span class="sxs-lookup"><span data-stu-id="0ca32-113">Properties</span></span>

<span data-ttu-id="0ca32-114">**MSMCAInfo \_ RawCorrectedPlatformEvent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0ca32-114">The **MSMCAInfo\_RawCorrectedPlatformEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0ca32-115">**使用中**</span><span class="sxs-lookup"><span data-stu-id="0ca32-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ca32-116">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0ca32-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0ca32-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ca32-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ca32-118">如果此類別的實例為使用中，則為 TRUE;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="0ca32-118">TRUE, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="0ca32-119">**Count**</span><span class="sxs-lookup"><span data-stu-id="0ca32-119">**Count**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ca32-120">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0ca32-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ca32-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ca32-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ca32-122">錯誤記錄的數目。</span><span class="sxs-lookup"><span data-stu-id="0ca32-122">Number of error records.</span></span>

</dd> <dt>

<span data-ttu-id="0ca32-123">**記錄**</span><span class="sxs-lookup"><span data-stu-id="0ca32-123">**Records**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ca32-124">資料類型： **MSMCAInfo \_ 專案** 陣列</span><span class="sxs-lookup"><span data-stu-id="0ca32-124">Data type: **MSMCAInfo\_Entry** array</span></span>
</dt> <dt>

<span data-ttu-id="0ca32-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ca32-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ca32-126">MCA 錯誤記錄的陣列。</span><span class="sxs-lookup"><span data-stu-id="0ca32-126">Array of MCA error records.</span></span> <span data-ttu-id="0ca32-127">陣列中的 MCA 錯誤記錄數目是由 **Count** 屬性指定。</span><span class="sxs-lookup"><span data-stu-id="0ca32-127">The number of MCA error records in the array is specified by the **Count** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0ca32-128">備註</span><span class="sxs-lookup"><span data-stu-id="0ca32-128">Remarks</span></span>

<span data-ttu-id="0ca32-129">**MSMCAInfo \_ RawCorrectedPlatformEvent** 類別衍生自 [**>register-wmievent**](wmievent.md)。</span><span class="sxs-lookup"><span data-stu-id="0ca32-129">The **MSMCAInfo\_RawCorrectedPlatformEvent** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0ca32-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="0ca32-130">Requirements</span></span>



| <span data-ttu-id="0ca32-131">需求</span><span class="sxs-lookup"><span data-stu-id="0ca32-131">Requirement</span></span> | <span data-ttu-id="0ca32-132">值</span><span class="sxs-lookup"><span data-stu-id="0ca32-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ca32-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0ca32-133">Minimum supported client</span></span><br/> | <span data-ttu-id="0ca32-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0ca32-134">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="0ca32-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0ca32-135">Minimum supported server</span></span><br/> | <span data-ttu-id="0ca32-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0ca32-136">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="0ca32-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="0ca32-137">Namespace</span></span><br/>                | <span data-ttu-id="0ca32-138">根 \\ wmi</span><span class="sxs-lookup"><span data-stu-id="0ca32-138">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="0ca32-139">MOF</span><span class="sxs-lookup"><span data-stu-id="0ca32-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0ca32-140"><dt>Wmicore mof</dt></span><span class="sxs-lookup"><span data-stu-id="0ca32-140"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="0ca32-141">DLL</span><span class="sxs-lookup"><span data-stu-id="0ca32-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ca32-142"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ca32-142"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ca32-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0ca32-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ca32-144">MSMCA 類別</span><span class="sxs-lookup"><span data-stu-id="0ca32-144">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="0ca32-145">**>register-wmievent**</span><span class="sxs-lookup"><span data-stu-id="0ca32-145">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

 





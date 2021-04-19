---
description: 包含已更正的電腦檢查 (CMC) 事件。 此類別僅適用于64位的 Windows 系統。
ms.assetid: e12efbf7-7d53-415a-bc48-90d33e4ce16d
title: MSMCAInfo_RawCMCEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawCMCEvent
- MSMCAInfo_RawCMCEvent.Active
- MSMCAInfo_RawCMCEvent.Count
- MSMCAInfo_RawCMCEvent.InstanceName
- MSMCAInfo_RawCMCEvent.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 1bb60d5fbcf004b924a91e640d8cd8a8c5ad3c25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987320"
---
# <a name="msmcainfo_rawcmcevent-class"></a><span data-ttu-id="2c645-104">MSMCAInfo \_ RawCMCEvent 類別</span><span class="sxs-lookup"><span data-stu-id="2c645-104">MSMCAInfo\_RawCMCEvent class</span></span>

<span data-ttu-id="2c645-105">**MSMCAInfo \_ RawCMCEvent** 類別包含已更正的電腦檢查 (CMC) 事件。</span><span class="sxs-lookup"><span data-stu-id="2c645-105">The **MSMCAInfo\_RawCMCEvent** class contains a Corrected Machine Check (CMC) event.</span></span> <span data-ttu-id="2c645-106">此類別僅適用于64位的 Windows 系統。</span><span class="sxs-lookup"><span data-stu-id="2c645-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="2c645-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="2c645-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="2c645-108">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="2c645-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c645-109">語法</span><span class="sxs-lookup"><span data-stu-id="2c645-109">Syntax</span></span>

``` syntax
class MSMCAInfo_RawCMCEvent : WMIEvent
{
  boolean         Active;
  uint32          Count;
  string          InstanceName;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a><span data-ttu-id="2c645-110">成員</span><span class="sxs-lookup"><span data-stu-id="2c645-110">Members</span></span>

<span data-ttu-id="2c645-111">**MSMCAInfo \_ RawCMCEvent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2c645-111">The **MSMCAInfo\_RawCMCEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="2c645-112">屬性</span><span class="sxs-lookup"><span data-stu-id="2c645-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2c645-113">屬性</span><span class="sxs-lookup"><span data-stu-id="2c645-113">Properties</span></span>

<span data-ttu-id="2c645-114">**MSMCAInfo \_ RawCMCEvent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2c645-114">The **MSMCAInfo\_RawCMCEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2c645-115">**使用中**</span><span class="sxs-lookup"><span data-stu-id="2c645-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c645-116">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2c645-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2c645-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2c645-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c645-118">如果此類別的實例為使用中，則為 TRUE;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="2c645-118">TRUE, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="2c645-119">**Count**</span><span class="sxs-lookup"><span data-stu-id="2c645-119">**Count**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c645-120">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2c645-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c645-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2c645-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c645-122">錯誤記錄的數目。</span><span class="sxs-lookup"><span data-stu-id="2c645-122">Number of error records.</span></span>

</dd> <dt>

<span data-ttu-id="2c645-123">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="2c645-123">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c645-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2c645-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c645-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2c645-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c645-126">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2c645-126">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2c645-127">此類別實例的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="2c645-127">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="2c645-128">**記錄**</span><span class="sxs-lookup"><span data-stu-id="2c645-128">**Records**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c645-129">資料類型： **MSMCAInfo \_ 專案** 陣列</span><span class="sxs-lookup"><span data-stu-id="2c645-129">Data type: **MSMCAInfo\_Entry** array</span></span>
</dt> <dt>

<span data-ttu-id="2c645-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2c645-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c645-131">機器檢查架構的陣列 (MCA) 錯誤記錄。</span><span class="sxs-lookup"><span data-stu-id="2c645-131">Array of Machine Check Architecture (MCA) error records.</span></span> <span data-ttu-id="2c645-132">陣列中的 MCA 錯誤記錄數目是由 **Count** 屬性指定。</span><span class="sxs-lookup"><span data-stu-id="2c645-132">The number of MCA error records in the array is specified by the **Count** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2c645-133">備註</span><span class="sxs-lookup"><span data-stu-id="2c645-133">Remarks</span></span>

<span data-ttu-id="2c645-134">**MSMCAInfo \_ RawCMCEvent** 類別衍生自 [**>register-wmievent**](wmievent.md)。</span><span class="sxs-lookup"><span data-stu-id="2c645-134">The **MSMCAInfo\_RawCMCEvent** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c645-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c645-135">Requirements</span></span>



| <span data-ttu-id="2c645-136">需求</span><span class="sxs-lookup"><span data-stu-id="2c645-136">Requirement</span></span> | <span data-ttu-id="2c645-137">值</span><span class="sxs-lookup"><span data-stu-id="2c645-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c645-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2c645-138">Minimum supported client</span></span><br/> | <span data-ttu-id="2c645-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2c645-139">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="2c645-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2c645-140">Minimum supported server</span></span><br/> | <span data-ttu-id="2c645-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2c645-141">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="2c645-142">命名空間</span><span class="sxs-lookup"><span data-stu-id="2c645-142">Namespace</span></span><br/>                | <span data-ttu-id="2c645-143">根 \\ wmi</span><span class="sxs-lookup"><span data-stu-id="2c645-143">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="2c645-144">MOF</span><span class="sxs-lookup"><span data-stu-id="2c645-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c645-145"><dt>Wmicore mof</dt></span><span class="sxs-lookup"><span data-stu-id="2c645-145"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="2c645-146">DLL</span><span class="sxs-lookup"><span data-stu-id="2c645-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c645-147"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c645-147"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c645-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c645-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c645-149">MSMCA 類別</span><span class="sxs-lookup"><span data-stu-id="2c645-149">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="2c645-150">**>register-wmievent**</span><span class="sxs-lookup"><span data-stu-id="2c645-150">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 


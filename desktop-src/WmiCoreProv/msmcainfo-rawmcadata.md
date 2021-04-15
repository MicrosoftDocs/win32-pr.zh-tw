---
description: 指定 (MCA) 記錄的原始機器檢查架構。 此類別僅適用于64位的 Windows 系統。
ms.assetid: d465ba8d-14b2-4911-ae19-19ebeb32126e
title: MSMCAInfo_RawMCAData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawMCAData
- MSMCAInfo_RawMCAData.Active
- MSMCAInfo_RawMCAData.Count
- MSMCAInfo_RawMCAData.InstanceName
- MSMCAInfo_RawMCAData.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 6cafc16ddbc91181cc2114def07a193941988228
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511396"
---
# <a name="msmcainfo_rawmcadata-class"></a><span data-ttu-id="67ef5-104">MSMCAInfo \_ RawMCAData 類別</span><span class="sxs-lookup"><span data-stu-id="67ef5-104">MSMCAInfo\_RawMCAData class</span></span>

<span data-ttu-id="67ef5-105">**MSMCAInfo \_ RawMCAData** 會將原始機器檢查架構指定 (MCA) 記錄。</span><span class="sxs-lookup"><span data-stu-id="67ef5-105">The **MSMCAInfo\_RawMCAData** specifies the raw Machine Check Architecture (MCA) logs.</span></span> <span data-ttu-id="67ef5-106">此類別僅適用于64位的 Windows 系統。</span><span class="sxs-lookup"><span data-stu-id="67ef5-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="67ef5-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="67ef5-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="67ef5-108">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="67ef5-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="67ef5-109">語法</span><span class="sxs-lookup"><span data-stu-id="67ef5-109">Syntax</span></span>

``` syntax
class MSMCAInfo_RawMCAData : MSMCAInfo
{
  boolean         Active;
  uint32          Count;
  string          InstanceName;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a><span data-ttu-id="67ef5-110">成員</span><span class="sxs-lookup"><span data-stu-id="67ef5-110">Members</span></span>

<span data-ttu-id="67ef5-111">**MSMCAInfo \_ RawMCAData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="67ef5-111">The **MSMCAInfo\_RawMCAData** class has these types of members:</span></span>

-   [<span data-ttu-id="67ef5-112">屬性</span><span class="sxs-lookup"><span data-stu-id="67ef5-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="67ef5-113">屬性</span><span class="sxs-lookup"><span data-stu-id="67ef5-113">Properties</span></span>

<span data-ttu-id="67ef5-114">**MSMCAInfo \_ RawMCAData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="67ef5-114">The **MSMCAInfo\_RawMCAData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="67ef5-115">**使用中**</span><span class="sxs-lookup"><span data-stu-id="67ef5-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ef5-116">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="67ef5-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="67ef5-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="67ef5-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ef5-118">如果此類別的實例為使用中，則為 TRUE;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="67ef5-118">TRUE, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="67ef5-119">**Count**</span><span class="sxs-lookup"><span data-stu-id="67ef5-119">**Count**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ef5-120">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="67ef5-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67ef5-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="67ef5-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ef5-122">錯誤記錄的數目。</span><span class="sxs-lookup"><span data-stu-id="67ef5-122">Number of error records.</span></span>

</dd> <dt>

<span data-ttu-id="67ef5-123">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="67ef5-123">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ef5-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="67ef5-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67ef5-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="67ef5-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67ef5-126">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="67ef5-126">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="67ef5-127">此類別實例的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="67ef5-127">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="67ef5-128">**記錄**</span><span class="sxs-lookup"><span data-stu-id="67ef5-128">**Records**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ef5-129">資料類型： **MSMCAInfo \_ 專案** 陣列</span><span class="sxs-lookup"><span data-stu-id="67ef5-129">Data type: **MSMCAInfo\_Entry** array</span></span>
</dt> <dt>

<span data-ttu-id="67ef5-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="67ef5-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ef5-131">MCA 錯誤記錄的陣列。</span><span class="sxs-lookup"><span data-stu-id="67ef5-131">Array of MCA error records.</span></span> <span data-ttu-id="67ef5-132">陣列中的 MCA 錯誤記錄數目是由 **Count** 屬性指定。</span><span class="sxs-lookup"><span data-stu-id="67ef5-132">The number of MCA error records in the array is specified by the **Count** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="67ef5-133">備註</span><span class="sxs-lookup"><span data-stu-id="67ef5-133">Remarks</span></span>

<span data-ttu-id="67ef5-134">**MSMCAInfo \_ RawMCAData** 類別衍生自 [**MSMCAInfo**](msmcainfo.md)。</span><span class="sxs-lookup"><span data-stu-id="67ef5-134">The **MSMCAInfo\_RawMCAData** class is derived from [**MSMCAInfo**](msmcainfo.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="67ef5-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="67ef5-135">Requirements</span></span>



| <span data-ttu-id="67ef5-136">需求</span><span class="sxs-lookup"><span data-stu-id="67ef5-136">Requirement</span></span> | <span data-ttu-id="67ef5-137">值</span><span class="sxs-lookup"><span data-stu-id="67ef5-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="67ef5-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="67ef5-138">Minimum supported client</span></span><br/> | <span data-ttu-id="67ef5-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="67ef5-139">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="67ef5-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="67ef5-140">Minimum supported server</span></span><br/> | <span data-ttu-id="67ef5-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="67ef5-141">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="67ef5-142">命名空間</span><span class="sxs-lookup"><span data-stu-id="67ef5-142">Namespace</span></span><br/>                | <span data-ttu-id="67ef5-143">根 \\ wmi</span><span class="sxs-lookup"><span data-stu-id="67ef5-143">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="67ef5-144">MOF</span><span class="sxs-lookup"><span data-stu-id="67ef5-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="67ef5-145"><dt>Wmicore mof</dt></span><span class="sxs-lookup"><span data-stu-id="67ef5-145"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="67ef5-146">DLL</span><span class="sxs-lookup"><span data-stu-id="67ef5-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67ef5-147"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67ef5-147"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67ef5-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="67ef5-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67ef5-149">MSMCA 類別</span><span class="sxs-lookup"><span data-stu-id="67ef5-149">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="67ef5-150">**MSMCAInfo**</span><span class="sxs-lookup"><span data-stu-id="67ef5-150">**MSMCAInfo**</span></span>](msmcainfo.md)
</dt> </dl>

 


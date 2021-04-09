---
description: 包含 (MCA) 事件的機器檢查架構。 此類別僅適用于64位的 Windows 系統。
ms.assetid: d1806b91-43a3-4329-8fe5-de1e4755740f
title: MSMCAInfo_RawMCAEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawMCAEvent
- MSMCAInfo_RawMCAEvent.Active
- MSMCAInfo_RawMCAEvent.Count
- MSMCAInfo_RawMCAEvent.InstanceName
- MSMCAInfo_RawMCAEvent.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: e15af79c67265823e0025849e4c2ef27f690265c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944935"
---
# <a name="msmcainfo_rawmcaevent-class"></a><span data-ttu-id="e0b1f-104">MSMCAInfo \_ RawMCAEvent 類別</span><span class="sxs-lookup"><span data-stu-id="e0b1f-104">MSMCAInfo\_RawMCAEvent class</span></span>

<span data-ttu-id="e0b1f-105">**MSMCAInfo \_ RawMCAEvent** 類別包含 (MCA) 事件的機器檢查架構。</span><span class="sxs-lookup"><span data-stu-id="e0b1f-105">The **MSMCAInfo\_RawMCAEvent** class contains a Machine Check Architecture (MCA) event.</span></span> <span data-ttu-id="e0b1f-106">此類別僅適用于64位的 Windows 系統。</span><span class="sxs-lookup"><span data-stu-id="e0b1f-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="e0b1f-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e0b1f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="e0b1f-108">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="e0b1f-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0b1f-109">語法</span><span class="sxs-lookup"><span data-stu-id="e0b1f-109">Syntax</span></span>

``` syntax
class MSMCAInfo_RawMCAEvent : WMIEvent
{
  boolean         Active;
  uint32          Count;
  string          InstanceName;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a><span data-ttu-id="e0b1f-110">成員</span><span class="sxs-lookup"><span data-stu-id="e0b1f-110">Members</span></span>

<span data-ttu-id="e0b1f-111">**MSMCAInfo \_ RawMCAEvent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e0b1f-111">The **MSMCAInfo\_RawMCAEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="e0b1f-112">屬性</span><span class="sxs-lookup"><span data-stu-id="e0b1f-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e0b1f-113">屬性</span><span class="sxs-lookup"><span data-stu-id="e0b1f-113">Properties</span></span>

<span data-ttu-id="e0b1f-114">**MSMCAInfo \_ RawMCAEvent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e0b1f-114">The **MSMCAInfo\_RawMCAEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e0b1f-115">**使用中**</span><span class="sxs-lookup"><span data-stu-id="e0b1f-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0b1f-116">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e0b1f-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e0b1f-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e0b1f-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0b1f-118">如果此類別的實例為使用中，則為 TRUE;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="e0b1f-118">TRUE, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="e0b1f-119">**Count**</span><span class="sxs-lookup"><span data-stu-id="e0b1f-119">**Count**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0b1f-120">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e0b1f-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e0b1f-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e0b1f-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0b1f-122">錯誤記錄的數目。</span><span class="sxs-lookup"><span data-stu-id="e0b1f-122">Number of error records.</span></span>

</dd> <dt>

<span data-ttu-id="e0b1f-123">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="e0b1f-123">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0b1f-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e0b1f-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0b1f-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e0b1f-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0b1f-126">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e0b1f-126">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e0b1f-127">可唯一識別這個 **MSMCAInfo \_ RawMCAEvent** 類別實例的字串。</span><span class="sxs-lookup"><span data-stu-id="e0b1f-127">String that uniquely identifies this instance of the **MSMCAInfo\_RawMCAEvent** class.</span></span>

</dd> <dt>

<span data-ttu-id="e0b1f-128">**記錄**</span><span class="sxs-lookup"><span data-stu-id="e0b1f-128">**Records**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0b1f-129">資料類型： **MSMCAInfo \_ 專案** 陣列</span><span class="sxs-lookup"><span data-stu-id="e0b1f-129">Data type: **MSMCAInfo\_Entry** array</span></span>
</dt> <dt>

<span data-ttu-id="e0b1f-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e0b1f-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0b1f-131">MCA 錯誤記錄的陣列。</span><span class="sxs-lookup"><span data-stu-id="e0b1f-131">Array of MCA error records.</span></span> <span data-ttu-id="e0b1f-132">陣列中的 MCA 錯誤記錄數目是由 **Count** 屬性指定。</span><span class="sxs-lookup"><span data-stu-id="e0b1f-132">The number of MCA error records in the array is specified by the **Count** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e0b1f-133">備註</span><span class="sxs-lookup"><span data-stu-id="e0b1f-133">Remarks</span></span>

<span data-ttu-id="e0b1f-134">**MSMCAInfo \_ RawMCAEvent** 類別衍生自 [**>register-wmievent**](wmievent.md)。</span><span class="sxs-lookup"><span data-stu-id="e0b1f-134">The **MSMCAInfo\_RawMCAEvent** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e0b1f-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="e0b1f-135">Requirements</span></span>



| <span data-ttu-id="e0b1f-136">需求</span><span class="sxs-lookup"><span data-stu-id="e0b1f-136">Requirement</span></span> | <span data-ttu-id="e0b1f-137">值</span><span class="sxs-lookup"><span data-stu-id="e0b1f-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0b1f-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e0b1f-138">Minimum supported client</span></span><br/> | <span data-ttu-id="e0b1f-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e0b1f-139">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="e0b1f-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e0b1f-140">Minimum supported server</span></span><br/> | <span data-ttu-id="e0b1f-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e0b1f-141">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="e0b1f-142">命名空間</span><span class="sxs-lookup"><span data-stu-id="e0b1f-142">Namespace</span></span><br/>                | <span data-ttu-id="e0b1f-143">根 \\ wmi</span><span class="sxs-lookup"><span data-stu-id="e0b1f-143">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="e0b1f-144">MOF</span><span class="sxs-lookup"><span data-stu-id="e0b1f-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e0b1f-145"><dt>Wmicore mof</dt></span><span class="sxs-lookup"><span data-stu-id="e0b1f-145"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="e0b1f-146">DLL</span><span class="sxs-lookup"><span data-stu-id="e0b1f-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0b1f-147"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0b1f-147"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0b1f-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e0b1f-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0b1f-149">MSMCA 類別</span><span class="sxs-lookup"><span data-stu-id="e0b1f-149">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="e0b1f-150">**>register-wmievent**</span><span class="sxs-lookup"><span data-stu-id="e0b1f-150">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 


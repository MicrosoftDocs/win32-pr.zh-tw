---
description: 表示 MCA、已更正的機器檢查 (CMC) ，或已更正的平臺錯誤 (CPE) 資訊專案。 此類別僅適用于64位的 Windows 系統。
ms.assetid: 4edbca20-2525-4e35-ab79-8cf421343144
title: MSMCAInfo_Entry 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_Entry
- MSMCAInfo_Entry.Data
- MSMCAInfo_Entry.Length
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: cda6abba06dc4d4f3fec3a4763391eee1fa81274
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983831"
---
# <a name="msmcainfo_entry-class"></a><span data-ttu-id="00836-104">MSMCAInfo \_ 專案類別</span><span class="sxs-lookup"><span data-stu-id="00836-104">MSMCAInfo\_Entry class</span></span>

<span data-ttu-id="00836-105">**MSMCAInfo \_ 專案** 類別指出 MCA、已更正的機器檢查 (CMC) ，或已更正的平臺錯誤 (CPE) 資訊專案。</span><span class="sxs-lookup"><span data-stu-id="00836-105">The **MSMCAInfo\_Entry** class indicates an MCA, corrected machine check (CMC), or corrected platform error (CPE) information entry.</span></span> <span data-ttu-id="00836-106">此類別僅適用于64位的 Windows 系統。</span><span class="sxs-lookup"><span data-stu-id="00836-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="00836-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="00836-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="00836-108">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="00836-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="00836-109">語法</span><span class="sxs-lookup"><span data-stu-id="00836-109">Syntax</span></span>

``` syntax
class MSMCAInfo_Entry : MSMCAInfo
{
  uint8  Data[];
  uint32 Length;
};
```

## <a name="members"></a><span data-ttu-id="00836-110">成員</span><span class="sxs-lookup"><span data-stu-id="00836-110">Members</span></span>

<span data-ttu-id="00836-111">**MSMCAInfo \_ 專案** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="00836-111">The **MSMCAInfo\_Entry** class has these types of members:</span></span>

-   [<span data-ttu-id="00836-112">屬性</span><span class="sxs-lookup"><span data-stu-id="00836-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="00836-113">屬性</span><span class="sxs-lookup"><span data-stu-id="00836-113">Properties</span></span>

<span data-ttu-id="00836-114">**MSMCAInfo \_ 專案** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="00836-114">The **MSMCAInfo\_Entry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="00836-115">**資料**</span><span class="sxs-lookup"><span data-stu-id="00836-115">**Data**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00836-116">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="00836-116">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="00836-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="00836-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00836-118">包含完整 MCA 錯誤記錄的整數陣列，如系統抽象層 (SAL) 所報告。</span><span class="sxs-lookup"><span data-stu-id="00836-118">Integer array that contains a complete MCA error record as reported by the system abstraction layer (SAL).</span></span> <span data-ttu-id="00836-119">SAL 是燒錄至 ROM 的程式碼，作業系統會呼叫該作業系統來執行與平臺相關的作業。</span><span class="sxs-lookup"><span data-stu-id="00836-119">The SAL is code burned into ROM that the operating system calls to perform platform-dependent operations.</span></span> <span data-ttu-id="00836-120">它類似于 x86 平臺上的 BIOS。</span><span class="sxs-lookup"><span data-stu-id="00836-120">It is similar to the BIOS on an x86 platform.</span></span>

</dd> <dt>

<span data-ttu-id="00836-121">**長度**</span><span class="sxs-lookup"><span data-stu-id="00836-121">**Length**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00836-122">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="00836-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="00836-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="00836-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00836-124">錯誤記錄中的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="00836-124">Number of bytes in the error record.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="00836-125">備註</span><span class="sxs-lookup"><span data-stu-id="00836-125">Remarks</span></span>

<span data-ttu-id="00836-126">**MSMCAInfo \_ 專案** 類別衍生自 [**MSMCAInfo**](msmcainfo.md)。</span><span class="sxs-lookup"><span data-stu-id="00836-126">The **MSMCAInfo\_Entry** class is derived from [**MSMCAInfo**](msmcainfo.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="00836-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="00836-127">Requirements</span></span>



| <span data-ttu-id="00836-128">需求</span><span class="sxs-lookup"><span data-stu-id="00836-128">Requirement</span></span> | <span data-ttu-id="00836-129">值</span><span class="sxs-lookup"><span data-stu-id="00836-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="00836-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="00836-130">Minimum supported client</span></span><br/> | <span data-ttu-id="00836-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="00836-131">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="00836-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="00836-132">Minimum supported server</span></span><br/> | <span data-ttu-id="00836-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="00836-133">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="00836-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="00836-134">Namespace</span></span><br/>                | <span data-ttu-id="00836-135">根 \\ wmi</span><span class="sxs-lookup"><span data-stu-id="00836-135">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="00836-136">MOF</span><span class="sxs-lookup"><span data-stu-id="00836-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="00836-137"><dt>Wmicore mof</dt></span><span class="sxs-lookup"><span data-stu-id="00836-137"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="00836-138">DLL</span><span class="sxs-lookup"><span data-stu-id="00836-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00836-139"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00836-139"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00836-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="00836-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00836-141">MSMCA 類別</span><span class="sxs-lookup"><span data-stu-id="00836-141">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="00836-142">**MSMCAInfo**</span><span class="sxs-lookup"><span data-stu-id="00836-142">**MSMCAInfo**</span></span>](msmcainfo.md)
</dt> </dl>

 

 





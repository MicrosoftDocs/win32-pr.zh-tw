---
description: 代表已更正的電腦檢查 (CMC) 處理，以從插斷驅動程式切換至輪詢。 此類別僅適用于64位的 Windows 系統。
ms.assetid: c5e99e13-0f65-40bc-8863-b2ca7ea221df
title: MSMCAEvent_SwitchToCMCPolling 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_SwitchToCMCPolling
- MSMCAEvent_SwitchToCMCPolling.Active
- MSMCAEvent_SwitchToCMCPolling.InstanceName
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: f7d0d543dc36054550d4ddf6cc1a77ce80cf1647
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318355"
---
# <a name="msmcaevent_switchtocmcpolling-class"></a><span data-ttu-id="3b6ed-104">MSMCAEvent \_ SwitchToCMCPolling 類別</span><span class="sxs-lookup"><span data-stu-id="3b6ed-104">MSMCAEvent\_SwitchToCMCPolling class</span></span>

<span data-ttu-id="3b6ed-105">**MSMCAEvent \_ SwitchToCMCPolling** 類別代表已更正的電腦檢查 (CMC) 處理，以從插斷驅動程式切換至輪詢。</span><span class="sxs-lookup"><span data-stu-id="3b6ed-105">The **MSMCAEvent\_SwitchToCMCPolling** class represents the corrected machine check (CMC) handling to be switched from the interrupt driver to polling.</span></span> <span data-ttu-id="3b6ed-106">在某些情況下，核心會輪詢系統抽象層 (SAL) 是否有任何 CMC 或已更正的平臺錯誤 (CPE) 發生在先前輪詢間隔內。</span><span class="sxs-lookup"><span data-stu-id="3b6ed-106">In some cases, the kernel polls the system abstraction layer (SAL) for any CMC or corrected platform error (CPE) that occurred within the previous polling interval.</span></span> <span data-ttu-id="3b6ed-107">此類別僅適用于64位的 Windows 系統。</span><span class="sxs-lookup"><span data-stu-id="3b6ed-107">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="3b6ed-108">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="3b6ed-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="3b6ed-109">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="3b6ed-109">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b6ed-110">語法</span><span class="sxs-lookup"><span data-stu-id="3b6ed-110">Syntax</span></span>

``` syntax
class MSMCAEvent_SwitchToCMCPolling : WMIEvent
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a><span data-ttu-id="3b6ed-111">成員</span><span class="sxs-lookup"><span data-stu-id="3b6ed-111">Members</span></span>

<span data-ttu-id="3b6ed-112">**MSMCAEvent \_ SwitchToCMCPolling** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3b6ed-112">The **MSMCAEvent\_SwitchToCMCPolling** class has these types of members:</span></span>

-   [<span data-ttu-id="3b6ed-113">屬性</span><span class="sxs-lookup"><span data-stu-id="3b6ed-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3b6ed-114">屬性</span><span class="sxs-lookup"><span data-stu-id="3b6ed-114">Properties</span></span>

<span data-ttu-id="3b6ed-115">**MSMCAEvent \_ SwitchToCMCPolling** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3b6ed-115">The **MSMCAEvent\_SwitchToCMCPolling** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3b6ed-116">**使用中**</span><span class="sxs-lookup"><span data-stu-id="3b6ed-116">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b6ed-117">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3b6ed-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3b6ed-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b6ed-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b6ed-119">如果此類別的實例為使用中，則 **為 TRUE**;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="3b6ed-119">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="3b6ed-120">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="3b6ed-120">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b6ed-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3b6ed-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b6ed-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b6ed-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b6ed-123">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3b6ed-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3b6ed-124">此類別實例的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="3b6ed-124">Unique identifier of this instance of the class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3b6ed-125">備註</span><span class="sxs-lookup"><span data-stu-id="3b6ed-125">Remarks</span></span>

<span data-ttu-id="3b6ed-126">**MSMCAEvent \_ SwitchToCMCPolling** 類別衍生自 [**>register-wmievent**](wmievent.md)。</span><span class="sxs-lookup"><span data-stu-id="3b6ed-126">The **MSMCAEvent\_SwitchToCMCPolling** class is derived from [**WMIEvent**](wmievent.md).</span></span>

<span data-ttu-id="3b6ed-127">系統抽象層 (SAL) 是將程式碼燒錄到作業系統呼叫以執行與平臺相關的作業。</span><span class="sxs-lookup"><span data-stu-id="3b6ed-127">The system abstraction layer (SAL) is code burned onto ROM that the operating system calls to perform platform-dependent operations.</span></span> <span data-ttu-id="3b6ed-128">它類似于 x86 平臺上的 BIOS。</span><span class="sxs-lookup"><span data-stu-id="3b6ed-128">It is similar to the BIOS on an x86 platform.</span></span> <span data-ttu-id="3b6ed-129">如果平臺不支援 CMC 或 CPE 輪詢的中斷，作業系統會每分鐘輪詢一次，檢查先前是否發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="3b6ed-129">In cases where the platform does not support interrupts for CMC or CPE polling, the operating system polls every minute, checking if an error occurred previously.</span></span> <span data-ttu-id="3b6ed-130">如果平臺支援中斷，且作業系統在一分鐘內收到使用者定義的 CMC 或 CPE 輪詢數量，則會停用中斷和輪詢。</span><span class="sxs-lookup"><span data-stu-id="3b6ed-130">If the platform does support interrupts and the operating system receives a user defined amount of CMC or CPE polls within one minute, then it disables the interrupt and poll.</span></span> <span data-ttu-id="3b6ed-131">如果使用者未在一分鐘內定義投票次數，系統會將預設值設定為每分鐘10個輪詢。</span><span class="sxs-lookup"><span data-stu-id="3b6ed-131">If the user does not define the number of polls within one minute, the system sets a default to 10 polls per minute.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b6ed-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b6ed-132">Requirements</span></span>



| <span data-ttu-id="3b6ed-133">需求</span><span class="sxs-lookup"><span data-stu-id="3b6ed-133">Requirement</span></span> | <span data-ttu-id="3b6ed-134">值</span><span class="sxs-lookup"><span data-stu-id="3b6ed-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b6ed-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3b6ed-135">Minimum supported client</span></span><br/> | <span data-ttu-id="3b6ed-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3b6ed-136">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="3b6ed-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3b6ed-137">Minimum supported server</span></span><br/> | <span data-ttu-id="3b6ed-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3b6ed-138">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="3b6ed-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="3b6ed-139">Namespace</span></span><br/>                | <span data-ttu-id="3b6ed-140">根 \\ wmi</span><span class="sxs-lookup"><span data-stu-id="3b6ed-140">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="3b6ed-141">MOF</span><span class="sxs-lookup"><span data-stu-id="3b6ed-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b6ed-142"><dt>Wmicore mof</dt></span><span class="sxs-lookup"><span data-stu-id="3b6ed-142"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="3b6ed-143">DLL</span><span class="sxs-lookup"><span data-stu-id="3b6ed-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b6ed-144"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b6ed-144"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b6ed-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b6ed-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b6ed-146">MSMCA 類別</span><span class="sxs-lookup"><span data-stu-id="3b6ed-146">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="3b6ed-147">**>register-wmievent**</span><span class="sxs-lookup"><span data-stu-id="3b6ed-147">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 


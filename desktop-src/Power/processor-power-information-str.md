---
description: 包含處理器的相關資訊。
ms.assetid: fa8c533c-3a54-4eb5-893f-649dfd8b4609
title: PROCESSOR_POWER_INFORMATION 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROCESSOR_POWER_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 500a346080d7bf0c44d392a63a71310db74225a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319171"
---
# <a name="processor_power_information-structure"></a><span data-ttu-id="3fb83-103">處理器 \_ 電源 \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="3fb83-103">PROCESSOR\_POWER\_INFORMATION structure</span></span>

<span data-ttu-id="3fb83-104">包含處理器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3fb83-104">Contains information about a processor.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fb83-105">語法</span><span class="sxs-lookup"><span data-stu-id="3fb83-105">Syntax</span></span>


```C++
typedef struct _PROCESSOR_POWER_INFORMATION {
  ULONG Number;
  ULONG MaxMhz;
  ULONG CurrentMhz;
  ULONG MhzLimit;
  ULONG MaxIdleState;
  ULONG CurrentIdleState;
} PROCESSOR_POWER_INFORMATION, *PPROCESSOR_POWER_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="3fb83-106">成員</span><span class="sxs-lookup"><span data-stu-id="3fb83-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3fb83-107">**Number**</span><span class="sxs-lookup"><span data-stu-id="3fb83-107">**Number**</span></span>
</dt> <dd>

<span data-ttu-id="3fb83-108">系統處理器號碼。</span><span class="sxs-lookup"><span data-stu-id="3fb83-108">The system processor number.</span></span>

</dd> <dt>

<span data-ttu-id="3fb83-109">**MaxMhz**</span><span class="sxs-lookup"><span data-stu-id="3fb83-109">**MaxMhz**</span></span>
</dt> <dd>

<span data-ttu-id="3fb83-110">系統處理器指定的最大頻率（以 mhz 為單位）。</span><span class="sxs-lookup"><span data-stu-id="3fb83-110">The maximum specified clock frequency of the system processor, in megahertz.</span></span>

</dd> <dt>

<span data-ttu-id="3fb83-111">**CurrentMhz**</span><span class="sxs-lookup"><span data-stu-id="3fb83-111">**CurrentMhz**</span></span>
</dt> <dd>

<span data-ttu-id="3fb83-112">處理器時鐘頻率（以 mhz 為單位）。</span><span class="sxs-lookup"><span data-stu-id="3fb83-112">The processor clock frequency, in megahertz.</span></span> <span data-ttu-id="3fb83-113">此數位是指定的處理器頻率頻率上限乘以目前的處理器節流。</span><span class="sxs-lookup"><span data-stu-id="3fb83-113">This number is the maximum specified processor clock frequency multiplied by the current processor throttle.</span></span>

</dd> <dt>

<span data-ttu-id="3fb83-114">**MhzLimit**</span><span class="sxs-lookup"><span data-stu-id="3fb83-114">**MhzLimit**</span></span>
</dt> <dd>

<span data-ttu-id="3fb83-115">處理器時鐘頻率的限制（以 mhz 為單位）。</span><span class="sxs-lookup"><span data-stu-id="3fb83-115">The limit on the processor clock frequency, in megahertz.</span></span> <span data-ttu-id="3fb83-116">此數位是指定的處理器頻率頻率上限乘以目前的處理器熱節流限制。</span><span class="sxs-lookup"><span data-stu-id="3fb83-116">This number is the maximum specified processor clock frequency multiplied by the current processor thermal throttle limit.</span></span>

</dd> <dt>

<span data-ttu-id="3fb83-117">**MaxIdleState**</span><span class="sxs-lookup"><span data-stu-id="3fb83-117">**MaxIdleState**</span></span>
</dt> <dd>

<span data-ttu-id="3fb83-118">此處理器的最大閒置狀態。</span><span class="sxs-lookup"><span data-stu-id="3fb83-118">The maximum idle state of this processor.</span></span>

</dd> <dt>

<span data-ttu-id="3fb83-119">**CurrentIdleState**</span><span class="sxs-lookup"><span data-stu-id="3fb83-119">**CurrentIdleState**</span></span>
</dt> <dd>

<span data-ttu-id="3fb83-120">此處理器的目前空閒狀態。</span><span class="sxs-lookup"><span data-stu-id="3fb83-120">The current idle state of this processor.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3fb83-121">備註</span><span class="sxs-lookup"><span data-stu-id="3fb83-121">Remarks</span></span>

<span data-ttu-id="3fb83-122">請注意，在 WinNT 中不小心省略此結構定義。</span><span class="sxs-lookup"><span data-stu-id="3fb83-122">Note that this structure definition was accidentally omitted from WinNT.h.</span></span> <span data-ttu-id="3fb83-123">此錯誤會在未來修正。</span><span class="sxs-lookup"><span data-stu-id="3fb83-123">This error will be corrected in the future.</span></span> <span data-ttu-id="3fb83-124">在此同時，若要編譯您的應用程式，請將本主題中所包含的結構定義包含在原始程式碼中。</span><span class="sxs-lookup"><span data-stu-id="3fb83-124">In the meantime, to compile your application, include the structure definition contained in this topic in your source code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fb83-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="3fb83-125">Requirements</span></span>



| <span data-ttu-id="3fb83-126">需求</span><span class="sxs-lookup"><span data-stu-id="3fb83-126">Requirement</span></span> | <span data-ttu-id="3fb83-127">值</span><span class="sxs-lookup"><span data-stu-id="3fb83-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3fb83-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3fb83-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3fb83-129">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3fb83-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="3fb83-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3fb83-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3fb83-131">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3fb83-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3fb83-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3fb83-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fb83-133">**CallNtPowerInformation**</span><span class="sxs-lookup"><span data-stu-id="3fb83-133">**CallNtPowerInformation**</span></span>](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation)
</dt> </dl>

 

 





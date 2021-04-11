---
description: 包含系統之空閒的相關資訊。
ms.assetid: f6349b7c-1835-4492-95e3-9ce142628804
title: SYSTEM_POWER_INFORMATION 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SYSTEM_POWER_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: c32a8ad86b71ea680bd2961c9196a0896b055e5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944230"
---
# <a name="system_power_information-structure"></a><span data-ttu-id="f4edc-103">系統 \_ 電源 \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="f4edc-103">SYSTEM\_POWER\_INFORMATION structure</span></span>

<span data-ttu-id="f4edc-104">包含系統之空閒的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f4edc-104">Contains information about the idleness of the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4edc-105">語法</span><span class="sxs-lookup"><span data-stu-id="f4edc-105">Syntax</span></span>


```C++
typedef struct _SYSTEM_POWER_INFORMATION {
  ULONG MaxIdlenessAllowed;
  ULONG Idleness;
  ULONG TimeRemaining;
  UCHAR CoolingMode;
} SYSTEM_POWER_INFORMATION, *PSYSTEM_POWER_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="f4edc-106">成員</span><span class="sxs-lookup"><span data-stu-id="f4edc-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f4edc-107">**MaxIdlenessAllowed**</span><span class="sxs-lookup"><span data-stu-id="f4edc-107">**MaxIdlenessAllowed**</span></span>
</dt> <dd>

<span data-ttu-id="f4edc-108">系統被視為閒置且空閒超時時間開始計數的閒置時間，以百分比表示。</span><span class="sxs-lookup"><span data-stu-id="f4edc-108">The idleness at which the system is considered idle and the idle time-out begins counting, expressed as a percentage.</span></span> <span data-ttu-id="f4edc-109">放在此數位下面會導致計時器取消。</span><span class="sxs-lookup"><span data-stu-id="f4edc-109">Dropping below this number causes the timer to be canceled.</span></span>

</dd> <dt>

<span data-ttu-id="f4edc-110">**閒置**</span><span class="sxs-lookup"><span data-stu-id="f4edc-110">**Idleness**</span></span>
</dt> <dd>

<span data-ttu-id="f4edc-111">目前的閒置層級，以百分比表示。</span><span class="sxs-lookup"><span data-stu-id="f4edc-111">The current idle level, expressed as a percentage.</span></span>

</dd> <dt>

<span data-ttu-id="f4edc-112">**TimeRemaining**</span><span class="sxs-lookup"><span data-stu-id="f4edc-112">**TimeRemaining**</span></span>
</dt> <dd>

<span data-ttu-id="f4edc-113">閒置計時器的剩餘時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="f4edc-113">The time remaining in the idle timer, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="f4edc-114">**CoolingMode**</span><span class="sxs-lookup"><span data-stu-id="f4edc-114">**CoolingMode**</span></span>
</dt> <dd>

<span data-ttu-id="f4edc-115">目前的系統冷卻模式。</span><span class="sxs-lookup"><span data-stu-id="f4edc-115">The current system cooling mode.</span></span> <span data-ttu-id="f4edc-116">此成員必須是下列值之一。</span><span class="sxs-lookup"><span data-stu-id="f4edc-116">This member must one of the following values.</span></span>



| <span data-ttu-id="f4edc-117">值</span><span class="sxs-lookup"><span data-stu-id="f4edc-117">Value</span></span>                                                                                                                                                                                                                                 | <span data-ttu-id="f4edc-118">意義</span><span class="sxs-lookup"><span data-stu-id="f4edc-118">Meaning</span></span>                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="PO_TZ_ACTIVE"></span><span id="po_tz_active"></span><dl> <span data-ttu-id="f4edc-119"><dt>**PO \_TZ \_ 活動**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f4edc-119"><dt>**PO\_TZ\_ACTIVE**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="f4edc-120">系統目前處於主動冷卻模式。</span><span class="sxs-lookup"><span data-stu-id="f4edc-120">The system is currently in Active cooling mode.</span></span><br/>                                                |
| <span id="PO_TZ_INVALID_MODE"></span><span id="po_tz_invalid_mode"></span><dl> <span data-ttu-id="f4edc-121"><dt>**PO \_TZ \_ 無效 \_ 模式**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f4edc-121"><dt>**PO\_TZ\_INVALID\_MODE**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="f4edc-122">系統不支援 CPU 節流，或系統中未定義任何熱區域。</span><span class="sxs-lookup"><span data-stu-id="f4edc-122">The system does not support CPU throttling, or there is no thermal zone defined in the system.</span></span><br/> |
| <span id="PO_TZ_PASSIVE"></span><span id="po_tz_passive"></span><dl> <span data-ttu-id="f4edc-123"><dt>**PO \_TZ \_ 被動**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f4edc-123"><dt>**PO\_TZ\_PASSIVE**</dt> <dt>1</dt></span></span> </dl>                 | <span data-ttu-id="f4edc-124">系統目前處於被動冷卻模式。</span><span class="sxs-lookup"><span data-stu-id="f4edc-124">The system is currently in Passive cooling mode.</span></span><br/>                                               |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f4edc-125">備註</span><span class="sxs-lookup"><span data-stu-id="f4edc-125">Remarks</span></span>

<span data-ttu-id="f4edc-126">請注意，在 WinNT 中不小心省略此結構定義。</span><span class="sxs-lookup"><span data-stu-id="f4edc-126">Note that this structure definition was accidentally omitted from WinNT.h.</span></span> <span data-ttu-id="f4edc-127">此錯誤會在未來修正。</span><span class="sxs-lookup"><span data-stu-id="f4edc-127">This error will be corrected in the future.</span></span> <span data-ttu-id="f4edc-128">在此同時，若要編譯您的應用程式，請將本主題中所包含的結構定義包含在原始程式碼中。</span><span class="sxs-lookup"><span data-stu-id="f4edc-128">In the meantime, to compile your application, include the structure definition contained in this topic in your source code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4edc-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="f4edc-129">Requirements</span></span>



| <span data-ttu-id="f4edc-130">需求</span><span class="sxs-lookup"><span data-stu-id="f4edc-130">Requirement</span></span> | <span data-ttu-id="f4edc-131">值</span><span class="sxs-lookup"><span data-stu-id="f4edc-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f4edc-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f4edc-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f4edc-133">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f4edc-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="f4edc-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f4edc-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f4edc-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f4edc-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f4edc-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f4edc-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4edc-137">**CallNtPowerInformation**</span><span class="sxs-lookup"><span data-stu-id="f4edc-137">**CallNtPowerInformation**</span></span>](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation)
</dt> </dl>

 

 





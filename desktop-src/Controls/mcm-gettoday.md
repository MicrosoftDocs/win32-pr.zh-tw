---
title: 'MCM_GETTODAY 訊息 (Commctrl .h) '
description: 抓取指定為 \ 0034; today \ 0034; 的日期資訊。月曆控制項的。 您可以使用 MonthCal GetToday 宏明確地傳送此訊息 \_ 。
ms.assetid: a79feb57-6aa3-4c96-95f3-7018b6b8327f
keywords:
- MCM_GETTODAY message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_GETTODAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21538af3c573b3d972b7f16bfe024e0d36211644
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934447"
---
# <a name="mcm_gettoday-message"></a><span data-ttu-id="f6f83-105">MCM \_ GETTODAY 訊息</span><span class="sxs-lookup"><span data-stu-id="f6f83-105">MCM\_GETTODAY message</span></span>

<span data-ttu-id="f6f83-106">針對月曆控制項的日期，抓取指定為 "today" 的日期資訊。</span><span class="sxs-lookup"><span data-stu-id="f6f83-106">Retrieves the date information for the date specified as "today" for a month calendar control.</span></span> <span data-ttu-id="f6f83-107">您可以使用 [**MonthCal \_ GetToday**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_gettoday) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="f6f83-107">You can send this message explicitly or by using the [**MonthCal\_GetToday**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_gettoday) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f6f83-108">參數</span><span class="sxs-lookup"><span data-stu-id="f6f83-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6f83-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f6f83-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f6f83-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="f6f83-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f6f83-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f6f83-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f6f83-112">[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)結構的指標，此結構會接收日期資訊。</span><span class="sxs-lookup"><span data-stu-id="f6f83-112">Pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that will receive the date information.</span></span> <span data-ttu-id="f6f83-113">此參數必須是有效的位址，而且不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f6f83-113">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6f83-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="f6f83-114">Return value</span></span>

<span data-ttu-id="f6f83-115">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="f6f83-115">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6f83-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="f6f83-116">Requirements</span></span>



| <span data-ttu-id="f6f83-117">需求</span><span class="sxs-lookup"><span data-stu-id="f6f83-117">Requirement</span></span> | <span data-ttu-id="f6f83-118">值</span><span class="sxs-lookup"><span data-stu-id="f6f83-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f6f83-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f6f83-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f6f83-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f6f83-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f6f83-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f6f83-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f6f83-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f6f83-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f6f83-123">標頭</span><span class="sxs-lookup"><span data-stu-id="f6f83-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6f83-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f6f83-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6f83-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f6f83-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6f83-126">月曆控制項中的時間</span><span class="sxs-lookup"><span data-stu-id="f6f83-126">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 


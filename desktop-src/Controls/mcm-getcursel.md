---
title: 'MCM_GETCURSEL 訊息 (Commctrl .h) '
description: 抓取目前選取的日期。 您可以使用 MonthCal GetCurSel 宏明確地傳送此訊息 \_ 。
ms.assetid: d4edc9ed-7c92-4ec8-bfa1-8ae597826b3f
keywords:
- MCM_GETCURSEL message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_GETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dece95c65e900119c7043c0d5eda22bf473e6c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465868"
---
# <a name="mcm_getcursel-message"></a><span data-ttu-id="65486-105">MCM \_ GETCURSEL 訊息</span><span class="sxs-lookup"><span data-stu-id="65486-105">MCM\_GETCURSEL message</span></span>

<span data-ttu-id="65486-106">抓取目前選取的日期。</span><span class="sxs-lookup"><span data-stu-id="65486-106">Retrieves the currently selected date.</span></span> <span data-ttu-id="65486-107">您可以使用 [**MonthCal \_ GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcursel) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="65486-107">You can send this message explicitly or by using the [**MonthCal\_GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcursel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="65486-108">參數</span><span class="sxs-lookup"><span data-stu-id="65486-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65486-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="65486-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="65486-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="65486-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="65486-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="65486-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="65486-112">[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)結構的指標，此結構會接收目前選取的日期資訊。</span><span class="sxs-lookup"><span data-stu-id="65486-112">Pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that will receive the currently selected date information.</span></span> <span data-ttu-id="65486-113">此參數必須是有效的位址，而且不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="65486-113">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65486-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="65486-114">Return value</span></span>

<span data-ttu-id="65486-115">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="65486-115">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="65486-116">當將月曆控制項設定為 [**MCS \_ 多重選**](month-calendar-control-styles.md) 樣式時，此訊息一律會失敗。</span><span class="sxs-lookup"><span data-stu-id="65486-116">This message will always fail when applied to month calendar controls set to the [**MCS\_MULTISELECT**](month-calendar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="65486-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="65486-117">Requirements</span></span>



| <span data-ttu-id="65486-118">需求</span><span class="sxs-lookup"><span data-stu-id="65486-118">Requirement</span></span> | <span data-ttu-id="65486-119">值</span><span class="sxs-lookup"><span data-stu-id="65486-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="65486-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="65486-120">Minimum supported client</span></span><br/> | <span data-ttu-id="65486-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65486-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="65486-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="65486-122">Minimum supported server</span></span><br/> | <span data-ttu-id="65486-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65486-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="65486-124">標頭</span><span class="sxs-lookup"><span data-stu-id="65486-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="65486-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="65486-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65486-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65486-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65486-127">月曆控制項中的時間</span><span class="sxs-lookup"><span data-stu-id="65486-127">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 


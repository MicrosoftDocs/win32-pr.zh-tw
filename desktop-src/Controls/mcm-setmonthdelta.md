---
title: 'MCM_SETMONTHDELTA 訊息 (Commctrl .h) '
description: 設定月曆控制項的滾動速率。 捲軸速率是當使用者按一下滾動按鈕時，控制項移動其顯示的月數。 您可以使用 MonthCal SetMonthDelta 宏明確地傳送此訊息 \_ 。
ms.assetid: 2d01b95f-3be8-4548-80b5-ac01d3e49e9f
keywords:
- MCM_SETMONTHDELTA message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_SETMONTHDELTA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 123eddb55a7ee8ddf8e3f6d8136e9ee57dfc8681
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969624"
---
# <a name="mcm_setmonthdelta-message"></a><span data-ttu-id="78043-106">MCM \_ SETMONTHDELTA 訊息</span><span class="sxs-lookup"><span data-stu-id="78043-106">MCM\_SETMONTHDELTA message</span></span>

<span data-ttu-id="78043-107">設定月曆控制項的滾動速率。</span><span class="sxs-lookup"><span data-stu-id="78043-107">Sets the scroll rate for a month calendar control.</span></span> <span data-ttu-id="78043-108">捲軸速率是當使用者按一下滾動按鈕時，控制項移動其顯示的月數。</span><span class="sxs-lookup"><span data-stu-id="78043-108">The scroll rate is the number of months that the control moves its display when the user clicks a scroll button.</span></span> <span data-ttu-id="78043-109">您可以使用 [**MonthCal \_ SetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmonthdelta) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="78043-109">You can send this message explicitly or by using the [**MonthCal\_SetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmonthdelta) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="78043-110">參數</span><span class="sxs-lookup"><span data-stu-id="78043-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78043-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="78043-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="78043-112">值，代表要設定為控制項滾動速率的月數。</span><span class="sxs-lookup"><span data-stu-id="78043-112">Value representing the number of months to be set as the control's scroll rate.</span></span> <span data-ttu-id="78043-113">如果此值為零，則會將月份差異重設為預設值，也就是顯示在控制項中的月份數。</span><span class="sxs-lookup"><span data-stu-id="78043-113">If this value is zero, the month delta is reset to the default, which is the number of months displayed in the control.</span></span>

</dd> <dt>

<span data-ttu-id="78043-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="78043-114">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="78043-115">必須為零。</span><span class="sxs-lookup"><span data-stu-id="78043-115">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78043-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="78043-116">Return value</span></span>

<span data-ttu-id="78043-117">傳回代表前一個滾動速率的 INT 值。</span><span class="sxs-lookup"><span data-stu-id="78043-117">Returns an INT value that represents the previous scroll rate.</span></span> <span data-ttu-id="78043-118">如果之前未設定捲軸速率，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="78043-118">If the scroll rate was not previously set, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="78043-119">備註</span><span class="sxs-lookup"><span data-stu-id="78043-119">Remarks</span></span>

<span data-ttu-id="78043-120">PAGE UP 和 PAGE DOWN 鍵，VK \_ 上 \_ 一步和 VK 下一步，不論顯示的月份數或 **MCM \_ SETMONTHDELTA** 設定的值為何，都會將選取的月份變更為1。</span><span class="sxs-lookup"><span data-stu-id="78043-120">The PAGE UP and PAGE DOWN keys, VK\_PRIOR and VK\_NEXT, change the selected month by one, regardless of the number of months displayed or the value set by **MCM\_SETMONTHDELTA**.</span></span>

## <a name="requirements"></a><span data-ttu-id="78043-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="78043-121">Requirements</span></span>



| <span data-ttu-id="78043-122">需求</span><span class="sxs-lookup"><span data-stu-id="78043-122">Requirement</span></span> | <span data-ttu-id="78043-123">值</span><span class="sxs-lookup"><span data-stu-id="78043-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="78043-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="78043-124">Minimum supported client</span></span><br/> | <span data-ttu-id="78043-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="78043-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="78043-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="78043-126">Minimum supported server</span></span><br/> | <span data-ttu-id="78043-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="78043-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="78043-128">標頭</span><span class="sxs-lookup"><span data-stu-id="78043-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="78043-129"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="78043-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






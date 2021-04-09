---
title: 'TCM_SETCURFOCUS 訊息 (Commctrl .h) '
description: 將焦點設定至索引標籤控制項中的指定索引標籤。 您可以使用 TabCtrl SetCurFocus 宏明確地傳送此訊息 \_ 。
ms.assetid: bcbd5f26-b54e-492b-aff3-357b8ae23969
keywords:
- TCM_SETCURFOCUS message Windows 控制項
topic_type:
- apiref
api_name:
- TCM_SETCURFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abe566d1e1b3cc7d257c4756fe123423fc344a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934405"
---
# <a name="tcm_setcurfocus-message"></a><span data-ttu-id="5d1b2-105">TCM \_ SETCURFOCUS 訊息</span><span class="sxs-lookup"><span data-stu-id="5d1b2-105">TCM\_SETCURFOCUS message</span></span>

<span data-ttu-id="5d1b2-106">將焦點設定至索引標籤控制項中的指定索引標籤。</span><span class="sxs-lookup"><span data-stu-id="5d1b2-106">Sets the focus to a specified tab in a tab control.</span></span> <span data-ttu-id="5d1b2-107">您可以使用 [**TabCtrl \_ SetCurFocus**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcurfocus) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="5d1b2-107">You can send this message explicitly or by using the [**TabCtrl\_SetCurFocus**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcurfocus) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5d1b2-108">參數</span><span class="sxs-lookup"><span data-stu-id="5d1b2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d1b2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5d1b2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5d1b2-110">取得焦點之索引標籤的索引。</span><span class="sxs-lookup"><span data-stu-id="5d1b2-110">Index of the tab that gets the focus.</span></span>

</dd> <dt>

<span data-ttu-id="5d1b2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5d1b2-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5d1b2-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="5d1b2-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d1b2-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5d1b2-113">Return value</span></span>

<span data-ttu-id="5d1b2-114">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="5d1b2-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d1b2-115">備註</span><span class="sxs-lookup"><span data-stu-id="5d1b2-115">Remarks</span></span>

<span data-ttu-id="5d1b2-116">如果索引標籤控制項具有 [ [**TCS \_**](tab-control-styles.md) ] 按鈕樣式 (按鈕模式) ，則具有焦點的索引標籤可能會與選取的索引標籤不同。例如，選取索引標籤時，使用者可以按方向鍵將焦點設定至不同的索引標籤，而不變更選取的索引標籤。在 [按鈕] 模式中， **TCM \_ SETCURFOCUS** 會將輸入焦點設定為與指定索引標籤相關聯的按鈕，但不會變更選取的索引標籤。</span><span class="sxs-lookup"><span data-stu-id="5d1b2-116">If the tab control has the [**TCS\_BUTTONS**](tab-control-styles.md) style (button mode), the tab with the focus may be different from the selected tab. For example, when a tab is selected, the user can press the arrow keys to set the focus to a different tab without changing the selected tab. In button mode, **TCM\_SETCURFOCUS** sets the input focus to the button associated with the specified tab, but it does not change the selected tab.</span></span>

<span data-ttu-id="5d1b2-117">如果索引標籤控制項沒有 [TCS] [**\_ 按鈕**](tab-control-styles.md) 樣式，則變更焦點也會變更選取的索引標籤。在此情況下，索引標籤控制項會將 [TCN \_ SELCHANGING](tcn-selchanging.md) 和 [TCN \_ SELCHANGE](tcn-selchange.md) 通知碼傳送至其父視窗。</span><span class="sxs-lookup"><span data-stu-id="5d1b2-117">If the tab control does not have the [**TCS\_BUTTONS**](tab-control-styles.md) style, changing the focus also changes the selected tab. In this case, the tab control sends the [TCN\_SELCHANGING](tcn-selchanging.md) and [TCN\_SELCHANGE](tcn-selchange.md) notification codes to its parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d1b2-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="5d1b2-118">Requirements</span></span>



| <span data-ttu-id="5d1b2-119">需求</span><span class="sxs-lookup"><span data-stu-id="5d1b2-119">Requirement</span></span> | <span data-ttu-id="5d1b2-120">值</span><span class="sxs-lookup"><span data-stu-id="5d1b2-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5d1b2-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5d1b2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5d1b2-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5d1b2-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5d1b2-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5d1b2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5d1b2-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5d1b2-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5d1b2-125">標頭</span><span class="sxs-lookup"><span data-stu-id="5d1b2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d1b2-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="5d1b2-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d1b2-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d1b2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d1b2-128">**TCM \_ GETCURFOCUS**</span><span class="sxs-lookup"><span data-stu-id="5d1b2-128">**TCM\_GETCURFOCUS**</span></span>](tcm-getcurfocus.md)
</dt> </dl>

 

 






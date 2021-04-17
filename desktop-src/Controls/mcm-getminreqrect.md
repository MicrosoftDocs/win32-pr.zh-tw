---
title: 'MCM_GETMINREQRECT 訊息 (Commctrl .h) '
description: 抓取在月曆控制項中顯示全月所需的最小大小。 您可以使用 MonthCal GetMinReqRect 宏明確地傳送此訊息 \_ 。
ms.assetid: f0378338-4809-48e9-9387-ed8b79356f95
keywords:
- MCM_GETMINREQRECT message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_GETMINREQRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac6b2e2b16a70841836a277ffe55e030a6d6a241
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464877"
---
# <a name="mcm_getminreqrect-message"></a><span data-ttu-id="0b03a-105">MCM \_ GETMINREQRECT 訊息</span><span class="sxs-lookup"><span data-stu-id="0b03a-105">MCM\_GETMINREQRECT message</span></span>

<span data-ttu-id="0b03a-106">抓取在月曆控制項中顯示全月所需的最小大小。</span><span class="sxs-lookup"><span data-stu-id="0b03a-106">Retrieves the minimum size required to display a full month in a month calendar control.</span></span> <span data-ttu-id="0b03a-107">您可以使用 [**MonthCal \_ GetMinReqRect**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="0b03a-107">You can send this message explicitly or by using the [**MonthCal\_GetMinReqRect**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0b03a-108">參數</span><span class="sxs-lookup"><span data-stu-id="0b03a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b03a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0b03a-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0b03a-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="0b03a-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0b03a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0b03a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0b03a-112">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，此結構會接收周框的資訊。</span><span class="sxs-lookup"><span data-stu-id="0b03a-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive bounding rectangle information.</span></span> <span data-ttu-id="0b03a-113">此參數必須是有效的位址，而且不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0b03a-113">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b03a-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="0b03a-114">Return value</span></span>

<span data-ttu-id="0b03a-115">如果成功，則傳回非零和 *lParam* 接收適用的界限資訊。</span><span class="sxs-lookup"><span data-stu-id="0b03a-115">Returns nonzero and *lParam* receives the applicable bounding information if successful.</span></span> <span data-ttu-id="0b03a-116">否則，訊息會傳回零。</span><span class="sxs-lookup"><span data-stu-id="0b03a-116">Otherwise, the message returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b03a-117">備註</span><span class="sxs-lookup"><span data-stu-id="0b03a-117">Remarks</span></span>

<span data-ttu-id="0b03a-118">月曆控制項的最小必要視窗大小取決於目前選取的字型、控制項樣式、系統計量和地區設定。</span><span class="sxs-lookup"><span data-stu-id="0b03a-118">The minimum required window size for a month calendar control depends on the currently selected font, control styles, system metrics, and regional settings.</span></span> <span data-ttu-id="0b03a-119">當應用程式變更任何會影響最小視窗大小的任何值，或處理 [**WM \_ SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) 訊息時，它應該傳送 **MCM \_ GETMINREQRECT** 來判斷新的最小大小。</span><span class="sxs-lookup"><span data-stu-id="0b03a-119">When an application changes anything that affects the minimum window size, or processes a [**WM\_SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) message, it should send **MCM\_GETMINREQRECT** to determine the new minimum size.</span></span>

> [!Note]  
> <span data-ttu-id="0b03a-120">**MCM \_ GETMINREQRECT** 所傳回的矩形不包含 "Today" 字串的寬度（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="0b03a-120">The rectangle returned by **MCM\_GETMINREQRECT** does not include the width of the "Today" string, if it is present.</span></span> <span data-ttu-id="0b03a-121">如果未設定 [**MCS \_ NOTODAY**](month-calendar-control-styles.md) 樣式，您的應用程式也應該藉由傳送 [**MCM \_ GETMAXTODAYWIDTH**](mcm-getmaxtodaywidth.md) 訊息，來取得定義 "Today" 字串寬度的矩形。</span><span class="sxs-lookup"><span data-stu-id="0b03a-121">If the [**MCS\_NOTODAY**](month-calendar-control-styles.md) style is not set, your application should also retrieve the rectangle that defines the "Today" string width by sending a [**MCM\_GETMAXTODAYWIDTH**](mcm-getmaxtodaywidth.md) message.</span></span> <span data-ttu-id="0b03a-122">使用兩個矩形中較大的，以確保不會裁剪 "Today" 字串。</span><span class="sxs-lookup"><span data-stu-id="0b03a-122">Use the larger of the two rectangles to ensure that the "Today" string is not clipped.</span></span>

 

<span data-ttu-id="0b03a-123">*LParam* 所指向之結構的 **top** 和 **left** 成員永遠為零。</span><span class="sxs-lookup"><span data-stu-id="0b03a-123">The **top** and **left** members of the structure pointed to by *lParam* will always be zero.</span></span> <span data-ttu-id="0b03a-124">**右邊** 和 **底部** 的成員代表控制項所需的最小 *cx* 和 *cy* 。</span><span class="sxs-lookup"><span data-stu-id="0b03a-124">The **right** and **bottom** members represent the minimum *cx* and *cy* required for the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b03a-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="0b03a-125">Requirements</span></span>



| <span data-ttu-id="0b03a-126">需求</span><span class="sxs-lookup"><span data-stu-id="0b03a-126">Requirement</span></span> | <span data-ttu-id="0b03a-127">值</span><span class="sxs-lookup"><span data-stu-id="0b03a-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0b03a-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0b03a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0b03a-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0b03a-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0b03a-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0b03a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0b03a-131">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0b03a-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0b03a-132">標頭</span><span class="sxs-lookup"><span data-stu-id="0b03a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b03a-133"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0b03a-133"><dt>Commctrl.h</dt></span></span> </dl> |



 


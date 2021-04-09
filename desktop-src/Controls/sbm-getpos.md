---
title: 'SBM_GETPOS 訊息 (Winuser .h) '
description: 傳送 SBM \_ GETPOS 訊息，以抓取捲軸控制項捲動方塊的目前位置。
ms.assetid: 00344d93-f205-4cda-aa25-6dd065f41b6e
keywords:
- SBM_GETPOS message Windows 控制項
topic_type:
- apiref
api_name:
- SBM_GETPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d088fc790985e57928f1ab56cd42254b1a087dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934789"
---
# <a name="sbm_getpos-message"></a><span data-ttu-id="d93cb-104">SBM \_ GETPOS 訊息</span><span class="sxs-lookup"><span data-stu-id="d93cb-104">SBM\_GETPOS message</span></span>

<span data-ttu-id="d93cb-105">傳送 **SBM \_ GETPOS** 訊息，以抓取捲軸控制項捲動方塊的目前位置。</span><span class="sxs-lookup"><span data-stu-id="d93cb-105">The **SBM\_GETPOS** message is sent to retrieve the current position of the scroll box of a scroll bar control.</span></span> <span data-ttu-id="d93cb-106">目前的位置是相依于目前滾動範圍的相對值。</span><span class="sxs-lookup"><span data-stu-id="d93cb-106">The current position is a relative value that depends on the current scrolling range.</span></span> <span data-ttu-id="d93cb-107">例如，如果滾動的範圍是0到100，而且捲動方塊位於橫條的中間，則目前的位置是50。</span><span class="sxs-lookup"><span data-stu-id="d93cb-107">For example, if the scrolling range is 0 through 100 and the scroll box is in the middle of the bar, the current position is 50.</span></span>

<span data-ttu-id="d93cb-108">應用程式不應直接傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="d93cb-108">Applications should not send this message directly.</span></span> <span data-ttu-id="d93cb-109">相反地，它們應該使用 [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos) 函數。</span><span class="sxs-lookup"><span data-stu-id="d93cb-109">Instead, they should use the [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos) function.</span></span> <span data-ttu-id="d93cb-110">視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="d93cb-110">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="d93cb-111">執行自訂捲軸控制項的應用程式必須回應這些訊息， **GetScrollPos** 函數才能正常運作。</span><span class="sxs-lookup"><span data-stu-id="d93cb-111">Applications which implement a custom scroll bar control must respond to these messages for the **GetScrollPos** function to function properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="d93cb-112">參數</span><span class="sxs-lookup"><span data-stu-id="d93cb-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d93cb-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d93cb-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d93cb-114">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="d93cb-114">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d93cb-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d93cb-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d93cb-116">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="d93cb-116">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d93cb-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="d93cb-117">Return value</span></span>

<span data-ttu-id="d93cb-118">傳回值是捲軸中捲動方塊的目前位置。</span><span class="sxs-lookup"><span data-stu-id="d93cb-118">The return value is the current position of the scroll box in the scroll bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="d93cb-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="d93cb-119">Requirements</span></span>



| <span data-ttu-id="d93cb-120">需求</span><span class="sxs-lookup"><span data-stu-id="d93cb-120">Requirement</span></span> | <span data-ttu-id="d93cb-121">值</span><span class="sxs-lookup"><span data-stu-id="d93cb-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d93cb-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d93cb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d93cb-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d93cb-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d93cb-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d93cb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d93cb-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d93cb-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d93cb-126">標頭</span><span class="sxs-lookup"><span data-stu-id="d93cb-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d93cb-127"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="d93cb-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d93cb-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d93cb-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="d93cb-129">**參考**</span><span class="sxs-lookup"><span data-stu-id="d93cb-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d93cb-130">**SBM \_ GETRANGE**</span><span class="sxs-lookup"><span data-stu-id="d93cb-130">**SBM\_GETRANGE**</span></span>](sbm-getrange.md)
</dt> <dt>

[<span data-ttu-id="d93cb-131">**SBM \_ SETPOS**</span><span class="sxs-lookup"><span data-stu-id="d93cb-131">**SBM\_SETPOS**</span></span>](sbm-setpos.md)
</dt> <dt>

[<span data-ttu-id="d93cb-132">**SBM \_ SETRANGE**</span><span class="sxs-lookup"><span data-stu-id="d93cb-132">**SBM\_SETRANGE**</span></span>](sbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="d93cb-133">**SBM \_ SETRANGEREDRAW**</span><span class="sxs-lookup"><span data-stu-id="d93cb-133">**SBM\_SETRANGEREDRAW**</span></span>](sbm-setrangeredraw.md)
</dt> </dl>

 


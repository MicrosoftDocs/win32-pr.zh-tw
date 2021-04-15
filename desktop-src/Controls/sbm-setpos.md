---
title: 'SBM_SETPOS 訊息 (Winuser .h) '
description: 傳送 SBM \_ SETPOS 訊息來設定捲動方塊 (thumb 的位置) 並在要求時，重繪捲軸以反映捲動方塊的新位置。
ms.assetid: 6b3c16ba-1cdf-41ff-8546-ba98477af334
keywords:
- SBM_SETPOS message Windows 控制項
topic_type:
- apiref
api_name:
- SBM_SETPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7a7dc99da5f4b3dbb301f15ddd722f1d664932f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466933"
---
# <a name="sbm_setpos-message"></a><span data-ttu-id="c95d1-104">SBM \_ SETPOS 訊息</span><span class="sxs-lookup"><span data-stu-id="c95d1-104">SBM\_SETPOS message</span></span>

<span data-ttu-id="c95d1-105">傳送 **SBM \_ SETPOS** 訊息來設定捲動方塊 (thumb 的位置) 並在要求時，重繪捲軸以反映捲動方塊的新位置。</span><span class="sxs-lookup"><span data-stu-id="c95d1-105">The **SBM\_SETPOS** message is sent to set the position of the scroll box (thumb) and, if requested, redraw the scroll bar to reflect the new position of the scroll box.</span></span>

<span data-ttu-id="c95d1-106">應用程式不應直接傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="c95d1-106">Applications should not send this message directly.</span></span> <span data-ttu-id="c95d1-107">相反地，它們應該使用 [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) 函數。</span><span class="sxs-lookup"><span data-stu-id="c95d1-107">Instead, they should use the [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) function.</span></span> <span data-ttu-id="c95d1-108">視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="c95d1-108">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="c95d1-109">執行自訂捲軸控制項的應用程式必須回應這些訊息， **SetScrollPos** 函數才能正常運作。</span><span class="sxs-lookup"><span data-stu-id="c95d1-109">Applications which implement a custom scroll bar control must respond to these messages for the **SetScrollPos** function to work properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="c95d1-110">參數</span><span class="sxs-lookup"><span data-stu-id="c95d1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c95d1-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c95d1-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c95d1-112">指定捲動方塊的新位置。</span><span class="sxs-lookup"><span data-stu-id="c95d1-112">Specifies the new position of the scroll box.</span></span> <span data-ttu-id="c95d1-113">它必須在滾動範圍內。</span><span class="sxs-lookup"><span data-stu-id="c95d1-113">It must be within the scrolling range.</span></span> <span data-ttu-id="c95d1-114">如果這個參數超出滾動範圍，此值會向上或向下舍入為最接近的有效值。</span><span class="sxs-lookup"><span data-stu-id="c95d1-114">If this parameter is outside of the scrolling range, the value is rounded up or down to the nearest valid value.</span></span>

</dd> <dt>

<span data-ttu-id="c95d1-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c95d1-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c95d1-116">指定是否應該重新繪製捲軸，以反映新的捲動方塊位置。</span><span class="sxs-lookup"><span data-stu-id="c95d1-116">Specifies whether the scroll bar should be redrawn to reflect the new scroll box position.</span></span> <span data-ttu-id="c95d1-117">如果此參數為 **TRUE**，則會重新繪製捲軸。</span><span class="sxs-lookup"><span data-stu-id="c95d1-117">If this parameter is **TRUE**, the scroll bar is redrawn.</span></span> <span data-ttu-id="c95d1-118">如果為 **FALSE**，則不會重新繪製捲軸。</span><span class="sxs-lookup"><span data-stu-id="c95d1-118">If it is **FALSE**, the scroll bar is not redrawn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c95d1-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="c95d1-119">Return value</span></span>

<span data-ttu-id="c95d1-120">**ComCtl32.dll 5.0 版**：如果捲動方塊的位置已變更，則傳回值是捲動方塊的先前位置;否則，它是零。</span><span class="sxs-lookup"><span data-stu-id="c95d1-120">**ComCtl32.dll version 5.0**: If the position of the scroll box changed, the return value is the previous position of the scroll box; otherwise, it is zero.</span></span>

<span data-ttu-id="c95d1-121">**ComCtl32.dll 版本 6.0**：捲動方塊的目前位置，不論是否已變更。</span><span class="sxs-lookup"><span data-stu-id="c95d1-121">**ComCtl32.dll version 6.0**: The current position of the scroll box, regardless of whether it has changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="c95d1-122">備註</span><span class="sxs-lookup"><span data-stu-id="c95d1-122">Remarks</span></span>

<span data-ttu-id="c95d1-123">如果對另一個函式的後續呼叫重新繪製捲軸控制項，將 *lParam* 參數設定為 **FALSE** 會很有用。</span><span class="sxs-lookup"><span data-stu-id="c95d1-123">If the scroll bar control is redrawn by a subsequent call to another function, setting the *lParam* parameter to **FALSE** is useful.</span></span>

## <a name="requirements"></a><span data-ttu-id="c95d1-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="c95d1-124">Requirements</span></span>



| <span data-ttu-id="c95d1-125">需求</span><span class="sxs-lookup"><span data-stu-id="c95d1-125">Requirement</span></span> | <span data-ttu-id="c95d1-126">值</span><span class="sxs-lookup"><span data-stu-id="c95d1-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c95d1-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c95d1-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c95d1-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c95d1-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c95d1-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c95d1-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c95d1-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c95d1-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c95d1-131">標頭</span><span class="sxs-lookup"><span data-stu-id="c95d1-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="c95d1-132"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="c95d1-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c95d1-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c95d1-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="c95d1-134">**參考**</span><span class="sxs-lookup"><span data-stu-id="c95d1-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c95d1-135">**SBM \_ GETPOS**</span><span class="sxs-lookup"><span data-stu-id="c95d1-135">**SBM\_GETPOS**</span></span>](sbm-getpos.md)
</dt> <dt>

[<span data-ttu-id="c95d1-136">**SBM \_ GETRANGE**</span><span class="sxs-lookup"><span data-stu-id="c95d1-136">**SBM\_GETRANGE**</span></span>](sbm-getrange.md)
</dt> <dt>

[<span data-ttu-id="c95d1-137">**SBM \_ SETRANGE**</span><span class="sxs-lookup"><span data-stu-id="c95d1-137">**SBM\_SETRANGE**</span></span>](sbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="c95d1-138">**SBM \_ SETRANGEREDRAW**</span><span class="sxs-lookup"><span data-stu-id="c95d1-138">**SBM\_SETRANGEREDRAW**</span></span>](sbm-setrangeredraw.md)
</dt> </dl>

 


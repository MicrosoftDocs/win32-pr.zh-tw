---
title: 'SBM_SETRANGE 訊息 (Winuser .h) '
description: 傳送 SBM \_ SETRANGE 訊息來設定捲軸控制項的最小和最大位置值。
ms.assetid: 9cf84354-3944-4c10-9b59-39427b840868
keywords:
- SBM_SETRANGE message Windows 控制項
topic_type:
- apiref
api_name:
- SBM_SETRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7a720531ae58fdb0712b8f23fd1aef88b3e4caa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844192"
---
# <a name="sbm_setrange-message"></a><span data-ttu-id="9c6cc-104">SBM \_ SETRANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="9c6cc-104">SBM\_SETRANGE message</span></span>

<span data-ttu-id="9c6cc-105">傳送 **SBM \_ SETRANGE** 訊息來設定捲軸控制項的最小和最大位置值。</span><span class="sxs-lookup"><span data-stu-id="9c6cc-105">The **SBM\_SETRANGE** message is sent to set the minimum and maximum position values for the scroll bar control.</span></span>

<span data-ttu-id="9c6cc-106">應用程式不應直接傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="9c6cc-106">Applications should not send this message directly.</span></span> <span data-ttu-id="9c6cc-107">相反地，它們應該使用 [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange) 函數。</span><span class="sxs-lookup"><span data-stu-id="9c6cc-107">Instead, they should use the [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange) function.</span></span> <span data-ttu-id="9c6cc-108">視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="9c6cc-108">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="9c6cc-109">執行自訂捲軸控制項的應用程式必須回應這些訊息， **SetScrollRange** 函數才能正常運作。</span><span class="sxs-lookup"><span data-stu-id="9c6cc-109">Applications which implement a custom scroll bar control must respond to these messages for the **SetScrollRange** function to work properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="9c6cc-110">參數</span><span class="sxs-lookup"><span data-stu-id="9c6cc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c6cc-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9c6cc-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c6cc-112">指定最小滾動位置。</span><span class="sxs-lookup"><span data-stu-id="9c6cc-112">Specifies the minimum scrolling position.</span></span>

</dd> <dt>

<span data-ttu-id="9c6cc-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9c6cc-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c6cc-114">指定最大滾動位置。</span><span class="sxs-lookup"><span data-stu-id="9c6cc-114">Specifies the maximum scrolling position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c6cc-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="9c6cc-115">Return value</span></span>

<span data-ttu-id="9c6cc-116">**ComCtl32.dll 5.0 版**：如果捲動方塊的位置已變更，則傳回值是捲動方塊的先前位置;否則，它是零。</span><span class="sxs-lookup"><span data-stu-id="9c6cc-116">**ComCtl32.dll version 5.0**: If the position of the scroll box changed, the return value is the previous position of the scroll box; otherwise, it is zero.</span></span>

<span data-ttu-id="9c6cc-117">**ComCtl32.dll 版本 6.0**：捲動方塊的目前位置，不論是否已變更。</span><span class="sxs-lookup"><span data-stu-id="9c6cc-117">**ComCtl32.dll version 6.0**: The current position of the scroll box, regardless of whether it has changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c6cc-118">備註</span><span class="sxs-lookup"><span data-stu-id="9c6cc-118">Remarks</span></span>

<span data-ttu-id="9c6cc-119">預設的最小和最大位置值為零。</span><span class="sxs-lookup"><span data-stu-id="9c6cc-119">The default minimum and maximum position values are zero.</span></span> <span data-ttu-id="9c6cc-120">*WParam* 和 *lParam* 參數所指定值之間的差異不得大於 MAXLONG。</span><span class="sxs-lookup"><span data-stu-id="9c6cc-120">The difference between the values specified by the *wParam* and *lParam* parameters must not be greater than MAXLONG.</span></span>

<span data-ttu-id="9c6cc-121">如果最小和最大位置值相等，則捲軸控制項是隱藏的，且實際上是停用的。</span><span class="sxs-lookup"><span data-stu-id="9c6cc-121">If the minimum and maximum position values are equal, the scroll bar control is hidden and, in effect, disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c6cc-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="9c6cc-122">Requirements</span></span>



| <span data-ttu-id="9c6cc-123">需求</span><span class="sxs-lookup"><span data-stu-id="9c6cc-123">Requirement</span></span> | <span data-ttu-id="9c6cc-124">值</span><span class="sxs-lookup"><span data-stu-id="9c6cc-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c6cc-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9c6cc-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9c6cc-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9c6cc-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9c6cc-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9c6cc-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9c6cc-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9c6cc-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9c6cc-129">標頭</span><span class="sxs-lookup"><span data-stu-id="9c6cc-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c6cc-130"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="9c6cc-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c6cc-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9c6cc-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="9c6cc-132">**參考**</span><span class="sxs-lookup"><span data-stu-id="9c6cc-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9c6cc-133">**SBM \_ GETPOS**</span><span class="sxs-lookup"><span data-stu-id="9c6cc-133">**SBM\_GETPOS**</span></span>](sbm-getpos.md)
</dt> <dt>

[<span data-ttu-id="9c6cc-134">**SBM \_ GETRANGE**</span><span class="sxs-lookup"><span data-stu-id="9c6cc-134">**SBM\_GETRANGE**</span></span>](sbm-getrange.md)
</dt> <dt>

[<span data-ttu-id="9c6cc-135">**SBM \_ SETPOS**</span><span class="sxs-lookup"><span data-stu-id="9c6cc-135">**SBM\_SETPOS**</span></span>](sbm-setpos.md)
</dt> <dt>

[<span data-ttu-id="9c6cc-136">**SBM \_ SETRANGEREDRAW**</span><span class="sxs-lookup"><span data-stu-id="9c6cc-136">**SBM\_SETRANGEREDRAW**</span></span>](sbm-setrangeredraw.md)
</dt> </dl>

 


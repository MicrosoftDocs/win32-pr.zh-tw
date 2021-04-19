---
description: 當工作區的非工作區需要變更以表示使用中或非作用中狀態時，傳送至視窗。
ms.assetid: d25732b9-b9ab-4754-a4cf-002d32e3945e
title: 'WM_NCACTI加值稅E 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a23cc5e0495d6679efea805eab80290b209906d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974457"
---
# <a name="wm_ncactivate-message"></a><span data-ttu-id="236b5-103">WM \_ NCACTI加值稅E 訊息</span><span class="sxs-lookup"><span data-stu-id="236b5-103">WM\_NCACTIVATE message</span></span>

<span data-ttu-id="236b5-104">當工作區的非工作區需要變更以表示使用中或非作用中狀態時，傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="236b5-104">Sent to a window when its nonclient area needs to be changed to indicate an active or inactive state.</span></span>

<span data-ttu-id="236b5-105">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="236b5-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCACTIVATE                   0x0086
```



## <a name="parameters"></a><span data-ttu-id="236b5-106">參數</span><span class="sxs-lookup"><span data-stu-id="236b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="236b5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="236b5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="236b5-108">指出何時需要變更標題列或圖示，以指出作用中或非作用中狀態。</span><span class="sxs-lookup"><span data-stu-id="236b5-108">Indicates when a title bar or icon needs to be changed to indicate an active or inactive state.</span></span> <span data-ttu-id="236b5-109">如果要繪製現用標題列或圖示， *wParam* 參數就是 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="236b5-109">If an active title bar or icon is to be drawn, the *wParam* parameter is **TRUE**.</span></span> <span data-ttu-id="236b5-110">如果要繪製非使用中的標題列或圖示， *wParam* 是 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="236b5-110">If an inactive title bar or icon is to be drawn, *wParam* is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="236b5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="236b5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="236b5-112">當 [視覺效果樣式](../controls/themes-overview.md) 在此視窗中為作用中時，不會使用此參數。</span><span class="sxs-lookup"><span data-stu-id="236b5-112">When a [visual style](../controls/themes-overview.md) is active for this window, this parameter is not used.</span></span>

<span data-ttu-id="236b5-113">當此視窗的視覺化樣式不在作用中時，此參數是視窗非工作區之選擇性更新區域的控制碼。</span><span class="sxs-lookup"><span data-stu-id="236b5-113">When a visual style is not active for this window, this parameter is a handle to an optional update region for the nonclient area of the window.</span></span> <span data-ttu-id="236b5-114">如果此參數設定為-1， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 就不會重新繪製非工作區，以反映狀態變更。</span><span class="sxs-lookup"><span data-stu-id="236b5-114">If this parameter is set to -1, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) does not repaint the nonclient area to reflect the state change.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="236b5-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="236b5-115">Return value</span></span>

<span data-ttu-id="236b5-116">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="236b5-116">Type: **LRESULT**</span></span>

<span data-ttu-id="236b5-117">當 *wParam* 參數為 **FALSE** 時，應用程式應該傳回 **TRUE** ，表示系統應繼續進行預設處理，否則應該傳回 **FALSE** 以防止變更。</span><span class="sxs-lookup"><span data-stu-id="236b5-117">When the *wParam* parameter is **FALSE**, an application should return **TRUE** to indicate that the system should proceed with the default processing, or it should return **FALSE** to prevent the change.</span></span> <span data-ttu-id="236b5-118">當 *wParam* 為 **TRUE** 時，會忽略傳回值。</span><span class="sxs-lookup"><span data-stu-id="236b5-118">When *wParam* is **TRUE**, the return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="236b5-119">備註</span><span class="sxs-lookup"><span data-stu-id="236b5-119">Remarks</span></span>

<span data-ttu-id="236b5-120">不建議處理與標準視窗的非工作區相關的訊息，因為應用程式必須能夠為視窗的非工作區繪製所有必要的部分。</span><span class="sxs-lookup"><span data-stu-id="236b5-120">Processing messages related to the nonclient area of a standard window is not recommended, because the application must be able to draw all the required parts of the nonclient area for the window.</span></span> <span data-ttu-id="236b5-121">如果應用程式處理此訊息，則必須傳回 **TRUE** ，以指示系統完成使用中視窗的變更。</span><span class="sxs-lookup"><span data-stu-id="236b5-121">If an application does process this message, it must return **TRUE** to direct the system to complete the change of active window.</span></span> <span data-ttu-id="236b5-122">如果接收到此訊息時視窗最小化，則應用程式應該將訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式。</span><span class="sxs-lookup"><span data-stu-id="236b5-122">If the window is minimized when this message is received, the application should pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span>

<span data-ttu-id="236b5-123">當 *wParam* 參數為 **TRUE** 時， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會使用其使用中色彩來繪製標題列或圖示標題，當 *wParam* 為 **FALSE** 時，則會以其非作用中色彩來繪製。</span><span class="sxs-lookup"><span data-stu-id="236b5-123">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function draws the title bar or icon title in its active colors when the *wParam* parameter is **TRUE** and in its inactive colors when *wParam* is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="236b5-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="236b5-124">Requirements</span></span>



| <span data-ttu-id="236b5-125">需求</span><span class="sxs-lookup"><span data-stu-id="236b5-125">Requirement</span></span> | <span data-ttu-id="236b5-126">值</span><span class="sxs-lookup"><span data-stu-id="236b5-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="236b5-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="236b5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="236b5-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="236b5-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="236b5-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="236b5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="236b5-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="236b5-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="236b5-131">標頭</span><span class="sxs-lookup"><span data-stu-id="236b5-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="236b5-132"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="236b5-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="236b5-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="236b5-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="236b5-134">**參考**</span><span class="sxs-lookup"><span data-stu-id="236b5-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="236b5-135">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="236b5-135">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

<span data-ttu-id="236b5-136">**概念**</span><span class="sxs-lookup"><span data-stu-id="236b5-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="236b5-137">Windows</span><span class="sxs-lookup"><span data-stu-id="236b5-137">Windows</span></span>](windows.md)
</dt> </dl>

 

 

---
description: 當使用者要求視窗還原為先前的大小和位置時，傳送至圖示。
ms.assetid: 6e14d5fd-6598-4d2e-a463-2b153c9c2aa3
title: 'WM_QUERYOPEN 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 582fcfce280c0bf98fdf92234b7fab8aaa103a91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026767"
---
# <a name="wm_queryopen-message"></a><span data-ttu-id="b464b-103">WM \_ QUERYOPEN 訊息</span><span class="sxs-lookup"><span data-stu-id="b464b-103">WM\_QUERYOPEN message</span></span>

<span data-ttu-id="b464b-104">當使用者要求視窗還原為先前的大小和位置時，傳送至圖示。</span><span class="sxs-lookup"><span data-stu-id="b464b-104">Sent to an icon when the user requests that the window be restored to its previous size and position.</span></span>

<span data-ttu-id="b464b-105">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="b464b-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_QUERYOPEN                    0x0013
```



## <a name="parameters"></a><span data-ttu-id="b464b-106">參數</span><span class="sxs-lookup"><span data-stu-id="b464b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b464b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b464b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b464b-108">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="b464b-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b464b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b464b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b464b-110">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="b464b-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b464b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b464b-111">Return value</span></span>

<span data-ttu-id="b464b-112">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="b464b-112">Type: **LRESULT**</span></span>

<span data-ttu-id="b464b-113">如果可以開啟圖示，處理此訊息的應用程式應該會傳回 **TRUE**;否則，它應該會傳回 **FALSE** ，以防止開啟圖示。</span><span class="sxs-lookup"><span data-stu-id="b464b-113">If the icon can be opened, an application that processes this message should return **TRUE**; otherwise, it should return **FALSE** to prevent the icon from being opened.</span></span>

## <a name="remarks"></a><span data-ttu-id="b464b-114">備註</span><span class="sxs-lookup"><span data-stu-id="b464b-114">Remarks</span></span>

<span data-ttu-id="b464b-115">根據預設， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函數會傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="b464b-115">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns **TRUE**.</span></span>

<span data-ttu-id="b464b-116">處理此訊息時，應用程式不應該執行任何會導致啟用或焦點變更 (例如，建立對話方塊) 的動作。</span><span class="sxs-lookup"><span data-stu-id="b464b-116">While processing this message, the application should not perform any action that would cause an activation or focus change (for example, creating a dialog box).</span></span>

## <a name="requirements"></a><span data-ttu-id="b464b-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="b464b-117">Requirements</span></span>



| <span data-ttu-id="b464b-118">需求</span><span class="sxs-lookup"><span data-stu-id="b464b-118">Requirement</span></span> | <span data-ttu-id="b464b-119">值</span><span class="sxs-lookup"><span data-stu-id="b464b-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b464b-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b464b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b464b-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b464b-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b464b-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b464b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b464b-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b464b-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b464b-124">標頭</span><span class="sxs-lookup"><span data-stu-id="b464b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b464b-125"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="b464b-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b464b-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b464b-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="b464b-127">**參考**</span><span class="sxs-lookup"><span data-stu-id="b464b-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b464b-128">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="b464b-128">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

<span data-ttu-id="b464b-129">**概念**</span><span class="sxs-lookup"><span data-stu-id="b464b-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b464b-130">Windows</span><span class="sxs-lookup"><span data-stu-id="b464b-130">Windows</span></span>](windows.md)
</dt> </dl>

 

 

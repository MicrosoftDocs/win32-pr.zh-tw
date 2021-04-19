---
description: 當應用程式變更視窗的啟用狀態時傳送。
ms.assetid: df2cf953-121f-43bb-a06c-d10e445bfb5e
title: 'WM_ENABLE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82bc83b84cbbf8e0c0145ef7d2730179cab54a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985233"
---
# <a name="wm_enable-message"></a><span data-ttu-id="e777c-103">WM \_ 啟用訊息</span><span class="sxs-lookup"><span data-stu-id="e777c-103">WM\_ENABLE message</span></span>

<span data-ttu-id="e777c-104">當應用程式變更視窗的啟用狀態時傳送。</span><span class="sxs-lookup"><span data-stu-id="e777c-104">Sent when an application changes the enabled state of a window.</span></span> <span data-ttu-id="e777c-105">它會傳送至已啟用狀態變更的視窗。</span><span class="sxs-lookup"><span data-stu-id="e777c-105">It is sent to the window whose enabled state is changing.</span></span> <span data-ttu-id="e777c-106">這則訊息會在 [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) 函式傳回之前傳送，但在啟用狀態之後 (視窗的 [**WS \_ 停用**](window-styles.md) 樣式位) 已變更。</span><span class="sxs-lookup"><span data-stu-id="e777c-106">This message is sent before the [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) function returns, but after the enabled state ([**WS\_DISABLED**](window-styles.md) style bit) of the window has changed.</span></span>

<span data-ttu-id="e777c-107">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="e777c-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_ENABLE                       0x000A
```



## <a name="parameters"></a><span data-ttu-id="e777c-108">參數</span><span class="sxs-lookup"><span data-stu-id="e777c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e777c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e777c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e777c-110">指出視窗是否已啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="e777c-110">Indicates whether the window has been enabled or disabled.</span></span> <span data-ttu-id="e777c-111">如果已啟用視窗，此參數為 **TRUE** ，如果視窗已停用，則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="e777c-111">This parameter is **TRUE** if the window has been enabled or **FALSE** if the window has been disabled.</span></span>

</dd> <dt>

<span data-ttu-id="e777c-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e777c-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e777c-113">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="e777c-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e777c-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="e777c-114">Return value</span></span>

<span data-ttu-id="e777c-115">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="e777c-115">Type: **LRESULT**</span></span>

<span data-ttu-id="e777c-116">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="e777c-116">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="e777c-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="e777c-117">Requirements</span></span>



| <span data-ttu-id="e777c-118">需求</span><span class="sxs-lookup"><span data-stu-id="e777c-118">Requirement</span></span> | <span data-ttu-id="e777c-119">值</span><span class="sxs-lookup"><span data-stu-id="e777c-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e777c-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e777c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e777c-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e777c-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e777c-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e777c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e777c-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e777c-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e777c-124">標頭</span><span class="sxs-lookup"><span data-stu-id="e777c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e777c-125"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="e777c-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e777c-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e777c-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="e777c-127">**參考**</span><span class="sxs-lookup"><span data-stu-id="e777c-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e777c-128">**EnableWindow**</span><span class="sxs-lookup"><span data-stu-id="e777c-128">**EnableWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-enablewindow)
</dt> <dt>

<span data-ttu-id="e777c-129">**概念**</span><span class="sxs-lookup"><span data-stu-id="e777c-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e777c-130">Windows</span><span class="sxs-lookup"><span data-stu-id="e777c-130">Windows</span></span>](windows.md)
</dt> </dl>

 

 

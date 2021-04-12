---
description: 將新的大型或小型圖示與視窗產生關聯。 系統會在 ALT + TAB 對話方塊中顯示大型圖示，並在視窗標題中顯示小圖示。
ms.assetid: c86620f2-893b-46f8-8254-1d7c4c142f37
title: 'WM_SETICON 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88bec7fc653123ba0a950c96bc1f54ebf436b0d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192784"
---
# <a name="wm_seticon-message"></a><span data-ttu-id="33baa-104">WM \_ SETICON 訊息</span><span class="sxs-lookup"><span data-stu-id="33baa-104">WM\_SETICON message</span></span>

<span data-ttu-id="33baa-105">將新的大型或小型圖示與視窗產生關聯。</span><span class="sxs-lookup"><span data-stu-id="33baa-105">Associates a new large or small icon with a window.</span></span> <span data-ttu-id="33baa-106">系統會在 ALT + TAB 對話方塊中顯示大型圖示，並在視窗標題中顯示小圖示。</span><span class="sxs-lookup"><span data-stu-id="33baa-106">The system displays the large icon in the ALT+TAB dialog box, and the small icon in the window caption.</span></span>


```C++
#define WM_SETICON                      0x0080
```



## <a name="parameters"></a><span data-ttu-id="33baa-107">參數</span><span class="sxs-lookup"><span data-stu-id="33baa-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33baa-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="33baa-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="33baa-109">要設定的圖示類型。</span><span class="sxs-lookup"><span data-stu-id="33baa-109">The type of icon to be set.</span></span> <span data-ttu-id="33baa-110">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="33baa-110">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="33baa-111">值</span><span class="sxs-lookup"><span data-stu-id="33baa-111">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="33baa-112">意義</span><span class="sxs-lookup"><span data-stu-id="33baa-112">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="ICON_BIG"></span><span id="icon_big"></span><dl> <span data-ttu-id="33baa-113"><dt>**圖示 \_BIG**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="33baa-113"><dt>**ICON\_BIG**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="33baa-114">設定視窗的大型圖示。</span><span class="sxs-lookup"><span data-stu-id="33baa-114">Set the large icon for the window.</span></span><br/> |
| <span id="ICON_SMALL"></span><span id="icon_small"></span><dl> <span data-ttu-id="33baa-115"><dt>**圖示 \_小**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="33baa-115"><dt>**ICON\_SMALL**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="33baa-116">設定視窗的小圖示。</span><span class="sxs-lookup"><span data-stu-id="33baa-116">Set the small icon for the window.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="33baa-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="33baa-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="33baa-118">新大或小圖示的控制碼。</span><span class="sxs-lookup"><span data-stu-id="33baa-118">A handle to the new large or small icon.</span></span> <span data-ttu-id="33baa-119">如果此參數為 **Null**，則會移除 *wParam* 所指出的圖示。</span><span class="sxs-lookup"><span data-stu-id="33baa-119">If this parameter is **NULL**, the icon indicated by *wParam* is removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33baa-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="33baa-120">Return value</span></span>

<span data-ttu-id="33baa-121">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="33baa-121">Type: **LRESULT**</span></span>

<span data-ttu-id="33baa-122">傳回值是先前大型或小型圖示的控制碼，取決於 *wParam* 的值。</span><span class="sxs-lookup"><span data-stu-id="33baa-122">The return value is a handle to the previous large or small icon, depending on the value of *wParam*.</span></span> <span data-ttu-id="33baa-123">如果視窗之前沒有 *wParam* 所指定之類型的圖示，則為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="33baa-123">It is **NULL** if the window previously had no icon of the type indicated by *wParam*.</span></span>

## <a name="remarks"></a><span data-ttu-id="33baa-124">備註</span><span class="sxs-lookup"><span data-stu-id="33baa-124">Remarks</span></span>

<span data-ttu-id="33baa-125">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會根據 *wParam* 的值，傳回與視窗相關聯的先前大型或小型圖示控制碼。</span><span class="sxs-lookup"><span data-stu-id="33baa-125">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns a handle to the previous large or small icon associated with the window, depending on the value of *wParam*.</span></span>

## <a name="requirements"></a><span data-ttu-id="33baa-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="33baa-126">Requirements</span></span>



| <span data-ttu-id="33baa-127">需求</span><span class="sxs-lookup"><span data-stu-id="33baa-127">Requirement</span></span> | <span data-ttu-id="33baa-128">值</span><span class="sxs-lookup"><span data-stu-id="33baa-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33baa-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="33baa-129">Minimum supported client</span></span><br/> | <span data-ttu-id="33baa-130">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33baa-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="33baa-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="33baa-131">Minimum supported server</span></span><br/> | <span data-ttu-id="33baa-132">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33baa-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="33baa-133">標頭</span><span class="sxs-lookup"><span data-stu-id="33baa-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="33baa-134"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="33baa-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33baa-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="33baa-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="33baa-136">**參考**</span><span class="sxs-lookup"><span data-stu-id="33baa-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="33baa-137">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="33baa-137">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="33baa-138">**WM \_ GETICON**</span><span class="sxs-lookup"><span data-stu-id="33baa-138">**WM\_GETICON**</span></span>](wm-geticon.md)
</dt> <dt>

<span data-ttu-id="33baa-139">**概念**</span><span class="sxs-lookup"><span data-stu-id="33baa-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="33baa-140">Windows</span><span class="sxs-lookup"><span data-stu-id="33baa-140">Windows</span></span>](windows.md)
</dt> </dl>

 

 

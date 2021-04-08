---
description: 在主題變更事件之後廣播至每個視窗。 主題變更事件的範例包括啟用主題、停用主題，或從某個主題轉換成另一個主題。
ms.assetid: 1a4051ac-cc6e-4520-ab66-d0a41a8a4c73
title: 'WM_THEMECHANGED 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bc15ab64126ff8972b858ef43ddd4d92cd62f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690276"
---
# <a name="wm_themechanged-message"></a><span data-ttu-id="d78ff-104">WM \_ THEMECHANGED 訊息</span><span class="sxs-lookup"><span data-stu-id="d78ff-104">WM\_THEMECHANGED message</span></span>

<span data-ttu-id="d78ff-105">在主題變更事件之後廣播至每個視窗。</span><span class="sxs-lookup"><span data-stu-id="d78ff-105">Broadcast to every window following a theme change event.</span></span> <span data-ttu-id="d78ff-106">主題變更事件的範例包括啟用主題、停用主題，或從某個主題轉換成另一個主題。</span><span class="sxs-lookup"><span data-stu-id="d78ff-106">Examples of theme change events are the activation of a theme, the deactivation of a theme, or a transition from one theme to another.</span></span>


```C++
#define WM_THEMECHANGED                 0x031A
```



## <a name="parameters"></a><span data-ttu-id="d78ff-107">參數</span><span class="sxs-lookup"><span data-stu-id="d78ff-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d78ff-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d78ff-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d78ff-109">此參數已保留備用。</span><span class="sxs-lookup"><span data-stu-id="d78ff-109">This parameter is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="d78ff-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d78ff-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d78ff-111">此參數已保留備用。</span><span class="sxs-lookup"><span data-stu-id="d78ff-111">This parameter is reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d78ff-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d78ff-112">Return value</span></span>

<span data-ttu-id="d78ff-113">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="d78ff-113">Type: **LRESULT**</span></span>

<span data-ttu-id="d78ff-114">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="d78ff-114">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d78ff-115">備註</span><span class="sxs-lookup"><span data-stu-id="d78ff-115">Remarks</span></span>

<span data-ttu-id="d78ff-116">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="d78ff-116">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> [!Note]  
> <span data-ttu-id="d78ff-117">此訊息是由作業系統所公佈。</span><span class="sxs-lookup"><span data-stu-id="d78ff-117">This message is posted by the operating system.</span></span> <span data-ttu-id="d78ff-118">應用程式通常不會傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="d78ff-118">Applications typically do not send this message.</span></span>

 

<span data-ttu-id="d78ff-119">主題是控制面板的規格，因此會將控制項的視覺元素與功能分開處理。</span><span class="sxs-lookup"><span data-stu-id="d78ff-119">Themes are specifications for the appearance of controls, so that the visual element of a control is treated separately from its functionality.</span></span>

<span data-ttu-id="d78ff-120">若要釋放現有的主題控制碼，請呼叫 [**CloseThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-closethemedata)。</span><span class="sxs-lookup"><span data-stu-id="d78ff-120">To release an existing theme handle, call [**CloseThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-closethemedata).</span></span> <span data-ttu-id="d78ff-121">若要取得新的主題控制碼，請使用 [**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata)。</span><span class="sxs-lookup"><span data-stu-id="d78ff-121">To acquire a new theme handle, use [**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata).</span></span>

<span data-ttu-id="d78ff-122">在 **WM \_ THEMECHANGED** 廣播之後，任何現有的主題控制碼都無效。</span><span class="sxs-lookup"><span data-stu-id="d78ff-122">Following the **WM\_THEMECHANGED** broadcast, any existing theme handles are invalid.</span></span> <span data-ttu-id="d78ff-123">有主題感知的視窗應該在收到 **WM \_ THEMECHANGED** 訊息時，釋放並重新開啟其任何既有的主題控制碼。</span><span class="sxs-lookup"><span data-stu-id="d78ff-123">A theme-aware window should release and reopen any of its pre-existing theme handles when it receives the **WM\_THEMECHANGED** message.</span></span> <span data-ttu-id="d78ff-124">如果 [**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata) 函式傳回 **Null**，則視窗應該繪製 unthemed。</span><span class="sxs-lookup"><span data-stu-id="d78ff-124">If the [**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata) function returns **NULL**, the window should paint unthemed.</span></span>

## <a name="requirements"></a><span data-ttu-id="d78ff-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="d78ff-125">Requirements</span></span>



| <span data-ttu-id="d78ff-126">需求</span><span class="sxs-lookup"><span data-stu-id="d78ff-126">Requirement</span></span> | <span data-ttu-id="d78ff-127">值</span><span class="sxs-lookup"><span data-stu-id="d78ff-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d78ff-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d78ff-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d78ff-129">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d78ff-129">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d78ff-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d78ff-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d78ff-131">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d78ff-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d78ff-132">標頭</span><span class="sxs-lookup"><span data-stu-id="d78ff-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d78ff-133"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="d78ff-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d78ff-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d78ff-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="d78ff-135">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="d78ff-135">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="d78ff-136">**CloseThemeData**</span><span class="sxs-lookup"><span data-stu-id="d78ff-136">**CloseThemeData**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-closethemedata)
</dt> <dt>

[<span data-ttu-id="d78ff-137">**IsThemeActive**</span><span class="sxs-lookup"><span data-stu-id="d78ff-137">**IsThemeActive**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-isthemeactive)
</dt> <dt>

[<span data-ttu-id="d78ff-138">**OpenThemeData**</span><span class="sxs-lookup"><span data-stu-id="d78ff-138">**OpenThemeData**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata)
</dt> </dl>

 

 

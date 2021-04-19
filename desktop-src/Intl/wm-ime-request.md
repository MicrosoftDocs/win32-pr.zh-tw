---
description: 傳送至應用程式以提供命令和要求資訊。 視窗會透過其 WindowProc 函數接收此訊息。
ms.assetid: c5e9f256-eed2-46cb-bb33-0e640a975f1f
title: 'WM_IME_REQUEST 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d0cea120d088fe1423b1d7dcb822307886675b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966721"
---
# <a name="wm_ime_request-message"></a><span data-ttu-id="93991-104">WM_IME_REQUEST 訊息</span><span class="sxs-lookup"><span data-stu-id="93991-104">WM_IME_REQUEST message</span></span>

<span data-ttu-id="93991-105">傳送至應用程式以提供命令和要求資訊。</span><span class="sxs-lookup"><span data-stu-id="93991-105">Sent to an application to provide commands and request information.</span></span> <span data-ttu-id="93991-106">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="93991-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,       
  WM_IME_REQUEST,  
  WPARAM wParam,   
  LPARAM lParam    
);
```



## <a name="parameters"></a><span data-ttu-id="93991-107">參數</span><span class="sxs-lookup"><span data-stu-id="93991-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93991-108">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="93991-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="93991-109">視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="93991-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="93991-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="93991-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="93991-111">命令。</span><span class="sxs-lookup"><span data-stu-id="93991-111">Command.</span></span> <span data-ttu-id="93991-112">這個參數的值可以是下列其中一個：</span><span class="sxs-lookup"><span data-stu-id="93991-112">This parameter can have one of the following values:</span></span>

<dl> 
<dd><span data-ttu-id="93991-113"><a href="imr-candidatewindow.md">IMR_CANDIDATEWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="93991-113"><a href="imr-candidatewindow.md">IMR_CANDIDATEWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="93991-114"><a href="imr-compositionfont.md">IMR_COMPOSITIONFONT</a></span><span class="sxs-lookup"><span data-stu-id="93991-114"><a href="imr-compositionfont.md">IMR_COMPOSITIONFONT</a></span></span></dd> 
<dd><span data-ttu-id="93991-115"><a href="imr-compositionwindow.md">IMR_COMPOSITIONWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="93991-115"><a href="imr-compositionwindow.md">IMR_COMPOSITIONWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="93991-116"><a href="imr-confirmreconvertstring.md">IMR_CONFIRMRECONVERTSTRING</a></span><span class="sxs-lookup"><span data-stu-id="93991-116"><a href="imr-confirmreconvertstring.md">IMR_CONFIRMRECONVERTSTRING</a></span></span></dd> 
<dd><span data-ttu-id="93991-117"><a href="imr-documentfeed.md">IMR_DOCUMENTFEED</a></span><span class="sxs-lookup"><span data-stu-id="93991-117"><a href="imr-documentfeed.md">IMR_DOCUMENTFEED</a></span></span></dd> 
<dd><span data-ttu-id="93991-118"><a href="imr-querycharposition.md">IMR_QUERYCHARPOSITION</a></span><span class="sxs-lookup"><span data-stu-id="93991-118"><a href="imr-querycharposition.md">IMR_QUERYCHARPOSITION</a></span></span></dd> 
<dd><span data-ttu-id="93991-119"><a href="imr-reconvertstring.md">IMR_RECONVERTSTRING</a></span><span class="sxs-lookup"><span data-stu-id="93991-119"><a href="imr-reconvertstring.md">IMR_RECONVERTSTRING</a></span></span></dd> 
</dl> 
</dd> 
<dt>

<span data-ttu-id="93991-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="93991-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="93991-121">命令特有的資料。</span><span class="sxs-lookup"><span data-stu-id="93991-121">Command-specific data.</span></span> <span data-ttu-id="93991-122">如需詳細資訊，請參閱每個命令的描述。</span><span class="sxs-lookup"><span data-stu-id="93991-122">For more information, see the description for each command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93991-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="93991-123">Return value</span></span>

<span data-ttu-id="93991-124">傳回命令特定的值。</span><span class="sxs-lookup"><span data-stu-id="93991-124">Returns a command-specific value.</span></span>

## <a name="requirements"></a><span data-ttu-id="93991-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="93991-125">Requirements</span></span>



| <span data-ttu-id="93991-126">需求</span><span class="sxs-lookup"><span data-stu-id="93991-126">Requirement</span></span> | <span data-ttu-id="93991-127">值</span><span class="sxs-lookup"><span data-stu-id="93991-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93991-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="93991-128">Minimum supported client</span></span><br/> | <span data-ttu-id="93991-129">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93991-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                                                |
| <span data-ttu-id="93991-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="93991-130">Minimum supported server</span></span><br/> | <span data-ttu-id="93991-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93991-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="93991-132">標頭</span><span class="sxs-lookup"><span data-stu-id="93991-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="93991-133"><dt>Winuser (包含 Windows .h) ;</dt><dt>Imm (包括 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="93991-133"><dt>Winuser.h (include Windows.h); </dt> <dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93991-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93991-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93991-135">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="93991-135">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="93991-136">輸入方法管理員訊息</span><span class="sxs-lookup"><span data-stu-id="93991-136">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="93991-137">IMR_CANDIDATEWINDOW</span><span class="sxs-lookup"><span data-stu-id="93991-137">IMR_CANDIDATEWINDOW</span></span>](imr-candidatewindow.md)
</dt> <dt>

[<span data-ttu-id="93991-138">IMR_COMPOSITIONFONT</span><span class="sxs-lookup"><span data-stu-id="93991-138">IMR_COMPOSITIONFONT</span></span>](imr-compositionfont.md)
</dt> <dt>

[<span data-ttu-id="93991-139">IMR_COMPOSITIONWINDOW</span><span class="sxs-lookup"><span data-stu-id="93991-139">IMR_COMPOSITIONWINDOW</span></span>](imr-compositionwindow.md)
</dt> <dt>

[<span data-ttu-id="93991-140">IMR_CONFIRMRECONVERTSTRING</span><span class="sxs-lookup"><span data-stu-id="93991-140">IMR_CONFIRMRECONVERTSTRING</span></span>](imr-confirmreconvertstring.md)
</dt> <dt>

[<span data-ttu-id="93991-141">IMR_DOCUMENTFEED</span><span class="sxs-lookup"><span data-stu-id="93991-141">IMR_DOCUMENTFEED</span></span>](imr-documentfeed.md)
</dt> <dt>

[<span data-ttu-id="93991-142">IMR_QUERYCHARPOSITION</span><span class="sxs-lookup"><span data-stu-id="93991-142">IMR_QUERYCHARPOSITION</span></span>](imr-querycharposition.md)
</dt> <dt>

[<span data-ttu-id="93991-143">IMR_RECONVERTSTRING</span><span class="sxs-lookup"><span data-stu-id="93991-143">IMR_RECONVERTSTRING</span></span>](imr-reconvertstring.md)
</dt> </dl>

 

 

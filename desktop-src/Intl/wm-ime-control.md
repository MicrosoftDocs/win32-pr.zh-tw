---
description: 由應用程式傳送以指示輸入法視窗執行要求的命令。
ms.assetid: 5d3b7f8a-57c9-41e3-8022-9a3f515fc32e
title: 'WM_IME_CONTROL 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd0adc534883bc0b31984c8d3e9b57a04b555987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848057"
---
# <a name="wm_ime_control-message"></a><span data-ttu-id="78f10-103">WM_IME_CONTROL 訊息</span><span class="sxs-lookup"><span data-stu-id="78f10-103">WM_IME_CONTROL message</span></span>

<span data-ttu-id="78f10-104">由應用程式傳送以指示輸入法視窗執行要求的命令。</span><span class="sxs-lookup"><span data-stu-id="78f10-104">Sent by an application to direct the IME window to carry out the requested command.</span></span> <span data-ttu-id="78f10-105">應用程式會使用這個訊息來控制它所建立的 IME 視窗。</span><span class="sxs-lookup"><span data-stu-id="78f10-105">The application uses this message to control the IME window that it has created.</span></span> <span data-ttu-id="78f10-106">為了傳送此訊息，應用程式會使用下列參數呼叫 [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) 函數。</span><span class="sxs-lookup"><span data-stu-id="78f10-106">To send this message, the application calls the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function with the following parameters.</span></span>


```C++
SendMessage(
  HWND   hwnd,
  WM_IME_CONTROL, 
  WPARAM wParam,
  LPARAM lParam             
);
```



## <a name="parameters"></a><span data-ttu-id="78f10-107">參數</span><span class="sxs-lookup"><span data-stu-id="78f10-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78f10-108">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="78f10-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="78f10-109">視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="78f10-109">Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="78f10-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="78f10-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="78f10-111">命令。</span><span class="sxs-lookup"><span data-stu-id="78f10-111">The command.</span></span> <span data-ttu-id="78f10-112">這個參數的值可以是下列其中一個：</span><span class="sxs-lookup"><span data-stu-id="78f10-112">This parameter can have one of the following values:</span></span>

<dl>
<dd><span data-ttu-id="78f10-113"><a href="imc-closestatuswindow.md">IMC_CLOSESTATUSWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="78f10-113"><a href="imc-closestatuswindow.md">IMC_CLOSESTATUSWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="78f10-114"><a href="imc-getcandidatepos.md">IMC_GETCANDIDATEPOS</a></span><span class="sxs-lookup"><span data-stu-id="78f10-114"><a href="imc-getcandidatepos.md">IMC_GETCANDIDATEPOS</a></span></span></dd> 
<dd><span data-ttu-id="78f10-115"><a href="imc-getcompositionfont.md">IMC_GETCOMPOSITIONFONT</a></span><span class="sxs-lookup"><span data-stu-id="78f10-115"><a href="imc-getcompositionfont.md">IMC_GETCOMPOSITIONFONT</a></span></span></dd> 
<dd><span data-ttu-id="78f10-116"><a href="imc-getcompositionwindow.md">IMC_GETCOMPOSITIONWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="78f10-116"><a href="imc-getcompositionwindow.md">IMC_GETCOMPOSITIONWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="78f10-117"><a href="imc-getstatuswindowpos.md">IMC_GETSTATUSWINDOWPOS</a></span><span class="sxs-lookup"><span data-stu-id="78f10-117"><a href="imc-getstatuswindowpos.md">IMC_GETSTATUSWINDOWPOS</a></span></span></dd> 
<dd><span data-ttu-id="78f10-118"><a href="imc-openstatuswindow.md">IMC_OPENSTATUSWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="78f10-118"><a href="imc-openstatuswindow.md">IMC_OPENSTATUSWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="78f10-119"><a href="imc-setcandidatepos.md">IMC_SETCANDIDATEPOS</a></span><span class="sxs-lookup"><span data-stu-id="78f10-119"><a href="imc-setcandidatepos.md">IMC_SETCANDIDATEPOS</a></span></span></dd> 
<dd><span data-ttu-id="78f10-120"><a href="imc-setcompositionfont.md">IMC_SETCOMPOSITIONFONT</a>></span><span class="sxs-lookup"><span data-stu-id="78f10-120"><a href="imc-setcompositionfont.md">IMC_SETCOMPOSITIONFONT</a>></span></span></dd> 
<dd><span data-ttu-id="78f10-121"><a href="imc-setcompositionwindow.md">IMC_SETCOMPOSITIONWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="78f10-121"><a href="imc-setcompositionwindow.md">IMC_SETCOMPOSITIONWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="78f10-122"><a href="imc-setstatuswindowpos.md">IMC_SETSTATUSWINDOWPOS</a></span><span class="sxs-lookup"><span data-stu-id="78f10-122"><a href="imc-setstatuswindowpos.md">IMC_SETSTATUSWINDOWPOS</a></span></span></dd> 
</dl>
</dd>

<dt>

<span data-ttu-id="78f10-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="78f10-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="78f10-124">命令特有的資料，其格式取決於 *wParam* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="78f10-124">Command-specific data, with format dependent on the value of the *wParam* parameter.</span></span> <span data-ttu-id="78f10-125">如需詳細資訊，請參閱每個命令的說明文件。</span><span class="sxs-lookup"><span data-stu-id="78f10-125">For more information, refer to the documentation for each command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78f10-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="78f10-126">Return value</span></span>

<span data-ttu-id="78f10-127">訊息會傳回命令特定的值。</span><span class="sxs-lookup"><span data-stu-id="78f10-127">The message returns a command-specific value.</span></span>

## <a name="requirements"></a><span data-ttu-id="78f10-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="78f10-128">Requirements</span></span>



| <span data-ttu-id="78f10-129">需求</span><span class="sxs-lookup"><span data-stu-id="78f10-129">Requirement</span></span> | <span data-ttu-id="78f10-130">值</span><span class="sxs-lookup"><span data-stu-id="78f10-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78f10-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="78f10-131">Minimum supported client</span></span><br/> | <span data-ttu-id="78f10-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="78f10-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                                                |
| <span data-ttu-id="78f10-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="78f10-133">Minimum supported server</span></span><br/> | <span data-ttu-id="78f10-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="78f10-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="78f10-135">標頭</span><span class="sxs-lookup"><span data-stu-id="78f10-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="78f10-136"><dt>Winuser (包含 Windows .h) ;</dt><dt>Imm (包括 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="78f10-136"><dt>Winuser.h (include Windows.h); </dt> <dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78f10-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="78f10-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78f10-138">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="78f10-138">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="78f10-139">輸入方法管理員訊息</span><span class="sxs-lookup"><span data-stu-id="78f10-139">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="78f10-140">IMC_CLOSESTATUSWINDOW</span><span class="sxs-lookup"><span data-stu-id="78f10-140">IMC_CLOSESTATUSWINDOW</span></span>](imc-closestatuswindow.md)
</dt> <dt>

[<span data-ttu-id="78f10-141">IMC_GETCANDIDATEPOS</span><span class="sxs-lookup"><span data-stu-id="78f10-141">IMC_GETCANDIDATEPOS</span></span>](imc-getcandidatepos.md)
</dt> <dt>

[<span data-ttu-id="78f10-142">IMC_GETCOMPOSITIONFONT</span><span class="sxs-lookup"><span data-stu-id="78f10-142">IMC_GETCOMPOSITIONFONT</span></span>](imc-getcompositionfont.md)
</dt> <dt>

[<span data-ttu-id="78f10-143">IMC_GETCOMPOSITIONWINDOW</span><span class="sxs-lookup"><span data-stu-id="78f10-143">IMC_GETCOMPOSITIONWINDOW</span></span>](imc-getcompositionwindow.md)
</dt> <dt>

[<span data-ttu-id="78f10-144">IMC_GETSTATUSWINDOWPOS</span><span class="sxs-lookup"><span data-stu-id="78f10-144">IMC_GETSTATUSWINDOWPOS</span></span>](imc-getstatuswindowpos.md)
</dt> <dt>

[<span data-ttu-id="78f10-145">IMC_OPENSTATUSWINDOW</span><span class="sxs-lookup"><span data-stu-id="78f10-145">IMC_OPENSTATUSWINDOW</span></span>](imc-openstatuswindow.md)
</dt> <dt>

[<span data-ttu-id="78f10-146">IMC_SETCANDIDATEPOS</span><span class="sxs-lookup"><span data-stu-id="78f10-146">IMC_SETCANDIDATEPOS</span></span>](imc-setcandidatepos.md)
</dt> <dt>

[<span data-ttu-id="78f10-147">IMC_SETCOMPOSITIONFONT</span><span class="sxs-lookup"><span data-stu-id="78f10-147">IMC_SETCOMPOSITIONFONT</span></span>](imc-setcompositionfont.md)
</dt> <dt>

[<span data-ttu-id="78f10-148">IMC_SETCOMPOSITIONWINDOW</span><span class="sxs-lookup"><span data-stu-id="78f10-148">IMC_SETCOMPOSITIONWINDOW</span></span>](imc-setcompositionwindow.md)
</dt> <dt>

[<span data-ttu-id="78f10-149">IMC_SETSTATUSWINDOWPOS</span><span class="sxs-lookup"><span data-stu-id="78f10-149">IMC_SETSTATUSWINDOWPOS</span></span>](imc-setstatuswindowpos.md)
</dt> </dl>

 

 

---
description: 當 IME 取得轉換結果的字元時，傳送至應用程式。 視窗會透過其 WindowProc 函數接收此訊息。
ms.assetid: 1e1353c3-5215-4829-a00a-2fee47a430eb
title: 'WM_IME_CHAR 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be0e2df06d9d837b0c1fbc0f9c9d9eb852252c47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104386283"
---
# <a name="wm_ime_char-message"></a><span data-ttu-id="cc4e5-104">WM \_ IME \_ 字元訊息</span><span class="sxs-lookup"><span data-stu-id="cc4e5-104">WM\_IME\_CHAR message</span></span>

<span data-ttu-id="cc4e5-105">當 IME 取得轉換結果的字元時，傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="cc4e5-105">Sent to an application when the IME gets a character of the conversion result.</span></span> <span data-ttu-id="cc4e5-106">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="cc4e5-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
 HWND  hwnd,
 WM_IME_CHAR,
 WPARAM wParam,
 LPARAM lParam   
);
```



## <a name="parameters"></a><span data-ttu-id="cc4e5-107">參數</span><span class="sxs-lookup"><span data-stu-id="cc4e5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc4e5-108">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="cc4e5-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="cc4e5-109">視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="cc4e5-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="cc4e5-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cc4e5-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cc4e5-111">**DBCS：** 單一位元組或雙位元組字元值。</span><span class="sxs-lookup"><span data-stu-id="cc4e5-111">**DBCS:** A single-byte or double-byte character value.</span></span> <span data-ttu-id="cc4e5-112">若為雙位元組字元， (位元組)  (wParam >> 8) 包含前導位元組。</span><span class="sxs-lookup"><span data-stu-id="cc4e5-112">For a double-byte character, (BYTE)(wParam >> 8) contains the lead byte.</span></span> <span data-ttu-id="cc4e5-113">請注意，括弧是必要的，因為 cast 運算子的優先順序高於移位運算子。</span><span class="sxs-lookup"><span data-stu-id="cc4e5-113">Note that the parentheses are necessary because the cast operator has higher precedence than the shift operator.</span></span>

<span data-ttu-id="cc4e5-114">**Unicode：** Unicode 字元值。</span><span class="sxs-lookup"><span data-stu-id="cc4e5-114">**Unicode:** A Unicode character value.</span></span>

</dd> <dt>

<span data-ttu-id="cc4e5-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cc4e5-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cc4e5-116">重複計數、掃描程式碼、擴充按鍵旗標、內容程式碼、先前的金鑰狀態旗標，以及轉換狀態旗標，其值如下所定義。</span><span class="sxs-lookup"><span data-stu-id="cc4e5-116">The repeat count, scan code, extended key flag, context code, previous key state flag, and transition state flag, with values as defined below.</span></span>



| <span data-ttu-id="cc4e5-117">bit</span><span class="sxs-lookup"><span data-stu-id="cc4e5-117">Bit</span></span>   | <span data-ttu-id="cc4e5-118">意義</span><span class="sxs-lookup"><span data-stu-id="cc4e5-118">Meaning</span></span>                                                                              |
|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cc4e5-119">0-15</span><span class="sxs-lookup"><span data-stu-id="cc4e5-119">0-15</span></span>  | <span data-ttu-id="cc4e5-120">重複計數。</span><span class="sxs-lookup"><span data-stu-id="cc4e5-120">Repeat count.</span></span> <span data-ttu-id="cc4e5-121">因為第一個位元組和第二個位元組是連續的，所以這一律為1。</span><span class="sxs-lookup"><span data-stu-id="cc4e5-121">Since the first byte and second byte are continuous, this is always 1.</span></span> |
| <span data-ttu-id="cc4e5-122">16-23</span><span class="sxs-lookup"><span data-stu-id="cc4e5-122">16-23</span></span> | <span data-ttu-id="cc4e5-123">掃描完整亞洲字元的程式碼。</span><span class="sxs-lookup"><span data-stu-id="cc4e5-123">Scan code for a complete Asian character.</span></span>                                            |
| <span data-ttu-id="cc4e5-124">24</span><span class="sxs-lookup"><span data-stu-id="cc4e5-124">24</span></span>    | <span data-ttu-id="cc4e5-125">擴充金鑰。</span><span class="sxs-lookup"><span data-stu-id="cc4e5-125">Extended key.</span></span>                                                                        |
| <span data-ttu-id="cc4e5-126">25-28</span><span class="sxs-lookup"><span data-stu-id="cc4e5-126">25-28</span></span> | <span data-ttu-id="cc4e5-127">未使用。</span><span class="sxs-lookup"><span data-stu-id="cc4e5-127">Not used.</span></span>                                                                            |
| <span data-ttu-id="cc4e5-128">29</span><span class="sxs-lookup"><span data-stu-id="cc4e5-128">29</span></span>    | <span data-ttu-id="cc4e5-129">內容程式碼。</span><span class="sxs-lookup"><span data-stu-id="cc4e5-129">Context code.</span></span>                                                                        |
| <span data-ttu-id="cc4e5-130">30</span><span class="sxs-lookup"><span data-stu-id="cc4e5-130">30</span></span>    | <span data-ttu-id="cc4e5-131">先前的金鑰狀態。</span><span class="sxs-lookup"><span data-stu-id="cc4e5-131">Previous key state.</span></span>                                                                  |
| <span data-ttu-id="cc4e5-132">31</span><span class="sxs-lookup"><span data-stu-id="cc4e5-132">31</span></span>    | <span data-ttu-id="cc4e5-133">轉換狀態。</span><span class="sxs-lookup"><span data-stu-id="cc4e5-133">Transition state.</span></span>                                                                    |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cc4e5-134">備註</span><span class="sxs-lookup"><span data-stu-id="cc4e5-134">Remarks</span></span>

<span data-ttu-id="cc4e5-135">不同于非 Unicode 視窗的 [**WM \_ CHAR**](../inputdev/wm-char.md) 訊息，此訊息可以包含雙位元組和單一位元組字元值。</span><span class="sxs-lookup"><span data-stu-id="cc4e5-135">Unlike the [**WM\_CHAR**](../inputdev/wm-char.md) message for a non-Unicode window, this message can include double-byte and single-byte character values.</span></span> <span data-ttu-id="cc4e5-136">若為 Unicode 視窗，此訊息與 WM \_ 字元相同。</span><span class="sxs-lookup"><span data-stu-id="cc4e5-136">For a Unicode window, this message is the same as WM\_CHAR.</span></span>

<span data-ttu-id="cc4e5-137">針對非 Unicode 視窗，如果 WM \_ IME \_ 字元訊息包含雙位元組字元，而且應用程式將此訊息傳遞給 [**DEFWINDOWPROC**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)，則 IME 會將此訊息轉換成兩個 WM \_ 字元訊息，每個字元都包含一個位元組的雙位元組字元。</span><span class="sxs-lookup"><span data-stu-id="cc4e5-137">For a non-Unicode window, if the WM\_IME\_CHAR message includes a double-byte character and the application passes this message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), the IME converts this message into two WM\_CHAR messages, each containing one byte of the double-byte character.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc4e5-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="cc4e5-138">Requirements</span></span>



| <span data-ttu-id="cc4e5-139">需求</span><span class="sxs-lookup"><span data-stu-id="cc4e5-139">Requirement</span></span> | <span data-ttu-id="cc4e5-140">值</span><span class="sxs-lookup"><span data-stu-id="cc4e5-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc4e5-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cc4e5-141">Minimum supported client</span></span><br/> | <span data-ttu-id="cc4e5-142">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cc4e5-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="cc4e5-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cc4e5-143">Minimum supported server</span></span><br/> | <span data-ttu-id="cc4e5-144">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cc4e5-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cc4e5-145">標頭</span><span class="sxs-lookup"><span data-stu-id="cc4e5-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc4e5-146"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="cc4e5-146"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc4e5-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cc4e5-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc4e5-148">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="cc4e5-148">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="cc4e5-149">輸入方法管理員訊息</span><span class="sxs-lookup"><span data-stu-id="cc4e5-149">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 

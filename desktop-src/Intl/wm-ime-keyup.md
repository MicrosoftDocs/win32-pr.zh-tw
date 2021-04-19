---
description: 由 IME 傳送至應用程式，以通知應用程式金鑰版本並保持訊息順序。 視窗會透過其 WindowProc 函數接收此訊息。
ms.assetid: 652f951f-4e9f-407c-844c-b250b6a9e6f5
title: 'WM_IME_KEYUP 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e0eb6c6701510a373573ff6d85d5b50a8541b4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973071"
---
# <a name="wm_ime_keyup-message"></a><span data-ttu-id="36da3-104">WM \_ 輸入法 \_ KEYUP 訊息</span><span class="sxs-lookup"><span data-stu-id="36da3-104">WM\_IME\_KEYUP message</span></span>

<span data-ttu-id="36da3-105">由 IME 傳送至應用程式，以通知應用程式金鑰版本並保持訊息順序。</span><span class="sxs-lookup"><span data-stu-id="36da3-105">Sent to an application by the IME to notify the application of a key release and to keep message order.</span></span> <span data-ttu-id="36da3-106">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="36da3-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,       
  WM_IME_KEYUP,    
  WPARAM wParam,   
  LPARAM lParam    
);
```



## <a name="parameters"></a><span data-ttu-id="36da3-107">參數</span><span class="sxs-lookup"><span data-stu-id="36da3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36da3-108">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="36da3-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="36da3-109">視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="36da3-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="36da3-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="36da3-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36da3-111">金鑰的虛擬按鍵碼。</span><span class="sxs-lookup"><span data-stu-id="36da3-111">Virtual key code of the key.</span></span>

</dd> <dt>

<span data-ttu-id="36da3-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="36da3-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36da3-113">重複計數、掃描程式碼、擴充按鍵旗標、內容程式碼、先前的金鑰狀態旗標和轉換狀態旗標，如下所示。</span><span class="sxs-lookup"><span data-stu-id="36da3-113">Repeat count, scan code, extended key flag, context code, previous key state flag, and transition state flag, as shown below.</span></span>



| <span data-ttu-id="36da3-114">bit</span><span class="sxs-lookup"><span data-stu-id="36da3-114">Bit</span></span>   | <span data-ttu-id="36da3-115">意義</span><span class="sxs-lookup"><span data-stu-id="36da3-115">Meaning</span></span>                                                                     |
|-------|-----------------------------------------------------------------------------|
| <span data-ttu-id="36da3-116">0-15</span><span class="sxs-lookup"><span data-stu-id="36da3-116">0-15</span></span>  | <span data-ttu-id="36da3-117">重複計數。</span><span class="sxs-lookup"><span data-stu-id="36da3-117">Repeat count.</span></span> <span data-ttu-id="36da3-118">這個值一律是 1。</span><span class="sxs-lookup"><span data-stu-id="36da3-118">This value is always 1.</span></span>                                       |
| <span data-ttu-id="36da3-119">16-23</span><span class="sxs-lookup"><span data-stu-id="36da3-119">16-23</span></span> | <span data-ttu-id="36da3-120">掃描程式碼。</span><span class="sxs-lookup"><span data-stu-id="36da3-120">Scan code.</span></span>                                                                  |
| <span data-ttu-id="36da3-121">24</span><span class="sxs-lookup"><span data-stu-id="36da3-121">24</span></span>    | <span data-ttu-id="36da3-122">擴充金鑰。</span><span class="sxs-lookup"><span data-stu-id="36da3-122">Extended key.</span></span> <span data-ttu-id="36da3-123">如果這個值是擴充索引鍵，則此值為1。</span><span class="sxs-lookup"><span data-stu-id="36da3-123">This value is 1 if it is an extended key.</span></span> <span data-ttu-id="36da3-124">否則，它是0。</span><span class="sxs-lookup"><span data-stu-id="36da3-124">Otherwise, it is 0.</span></span> |
| <span data-ttu-id="36da3-125">25-28</span><span class="sxs-lookup"><span data-stu-id="36da3-125">25-28</span></span> | <span data-ttu-id="36da3-126">未使用。</span><span class="sxs-lookup"><span data-stu-id="36da3-126">Not used.</span></span>                                                                   |
| <span data-ttu-id="36da3-127">29</span><span class="sxs-lookup"><span data-stu-id="36da3-127">29</span></span>    | <span data-ttu-id="36da3-128">內容程式碼。</span><span class="sxs-lookup"><span data-stu-id="36da3-128">Context code.</span></span> <span data-ttu-id="36da3-129">這個值一定是 0。</span><span class="sxs-lookup"><span data-stu-id="36da3-129">This value is always 0.</span></span>                                       |
| <span data-ttu-id="36da3-130">30</span><span class="sxs-lookup"><span data-stu-id="36da3-130">30</span></span>    | <span data-ttu-id="36da3-131">先前的金鑰狀態。</span><span class="sxs-lookup"><span data-stu-id="36da3-131">Previous key state.</span></span> <span data-ttu-id="36da3-132">這個值一律是 1。</span><span class="sxs-lookup"><span data-stu-id="36da3-132">This value is always 1.</span></span>                                 |
| <span data-ttu-id="36da3-133">31</span><span class="sxs-lookup"><span data-stu-id="36da3-133">31</span></span>    | <span data-ttu-id="36da3-134">轉換狀態。</span><span class="sxs-lookup"><span data-stu-id="36da3-134">Transition state.</span></span> <span data-ttu-id="36da3-135">這個值一律是 1。</span><span class="sxs-lookup"><span data-stu-id="36da3-135">This value is always 1.</span></span>                                   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36da3-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="36da3-136">Return value</span></span>

<span data-ttu-id="36da3-137">如果應用程式處理此訊息，則應該會傳回0。</span><span class="sxs-lookup"><span data-stu-id="36da3-137">An application should return 0 if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="36da3-138">備註</span><span class="sxs-lookup"><span data-stu-id="36da3-138">Remarks</span></span>

<span data-ttu-id="36da3-139">應用程式可處理此訊息，或將其傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  函式，以產生相符的 [**WM \_ KEYUP**](../inputdev/wm-keyup.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="36da3-139">An application can process this message or pass it to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function to generate a matching [**WM\_KEYUP**](../inputdev/wm-keyup.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="36da3-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="36da3-140">Requirements</span></span>



| <span data-ttu-id="36da3-141">需求</span><span class="sxs-lookup"><span data-stu-id="36da3-141">Requirement</span></span> | <span data-ttu-id="36da3-142">值</span><span class="sxs-lookup"><span data-stu-id="36da3-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36da3-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="36da3-143">Minimum supported client</span></span><br/> | <span data-ttu-id="36da3-144">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36da3-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="36da3-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="36da3-145">Minimum supported server</span></span><br/> | <span data-ttu-id="36da3-146">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36da3-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="36da3-147">標頭</span><span class="sxs-lookup"><span data-stu-id="36da3-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="36da3-148"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="36da3-148"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36da3-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36da3-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36da3-150">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="36da3-150">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="36da3-151">輸入方法管理員訊息</span><span class="sxs-lookup"><span data-stu-id="36da3-151">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 

---
description: 由 IME 傳送至應用程式，以通知應用程式按鍵，並保留訊息順序。 視窗會透過其 WindowProc 函數接收此訊息。
ms.assetid: db7075fb-b3d4-4d32-a0db-096d17d67c72
title: 'WM_IME_KEYDOWN 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3089af3c839f70e7f55895ae13158e7b2240605
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191381"
---
# <a name="wm_ime_keydown-message"></a><span data-ttu-id="05a98-104">WM \_ 輸入法 \_ KEYDOWN 訊息</span><span class="sxs-lookup"><span data-stu-id="05a98-104">WM\_IME\_KEYDOWN message</span></span>

<span data-ttu-id="05a98-105">由 IME 傳送至應用程式，以通知應用程式按鍵，並保留訊息順序。</span><span class="sxs-lookup"><span data-stu-id="05a98-105">Sent to an application by the IME to notify the application of a key press and to keep message order.</span></span> <span data-ttu-id="05a98-106">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="05a98-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,        
  WM_IME_KEYDOWN,  
  WPARAM wParam, 
  LPARAM lParam      
);
```



## <a name="parameters"></a><span data-ttu-id="05a98-107">參數</span><span class="sxs-lookup"><span data-stu-id="05a98-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05a98-108">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="05a98-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="05a98-109">視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="05a98-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="05a98-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="05a98-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="05a98-111">金鑰的虛擬按鍵碼。</span><span class="sxs-lookup"><span data-stu-id="05a98-111">Virtual key code of the key.</span></span>

</dd> <dt>

<span data-ttu-id="05a98-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="05a98-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="05a98-113">[重複計數]、[掃描程式碼]、[擴充按鍵旗標]、[內容程式碼]、[先前的金鑰狀態旗標] 和 [轉換狀態] 旗標，如下表</span><span class="sxs-lookup"><span data-stu-id="05a98-113">Repeat count, scan code, extended key flag, context code, previous key state flag, and transition state flag, as shown in the following table.</span></span>



| <span data-ttu-id="05a98-114">bit</span><span class="sxs-lookup"><span data-stu-id="05a98-114">Bit</span></span>   | <span data-ttu-id="05a98-115">意義</span><span class="sxs-lookup"><span data-stu-id="05a98-115">Meaning</span></span>                                                                     |
|-------|-----------------------------------------------------------------------------|
| <span data-ttu-id="05a98-116">0-15</span><span class="sxs-lookup"><span data-stu-id="05a98-116">0-15</span></span>  | <span data-ttu-id="05a98-117">重複計數。</span><span class="sxs-lookup"><span data-stu-id="05a98-117">Repeat count.</span></span>                                                               |
| <span data-ttu-id="05a98-118">16-23</span><span class="sxs-lookup"><span data-stu-id="05a98-118">16-23</span></span> | <span data-ttu-id="05a98-119">掃描程式碼。</span><span class="sxs-lookup"><span data-stu-id="05a98-119">Scan code.</span></span>                                                                  |
| <span data-ttu-id="05a98-120">24</span><span class="sxs-lookup"><span data-stu-id="05a98-120">24</span></span>    | <span data-ttu-id="05a98-121">擴充金鑰。</span><span class="sxs-lookup"><span data-stu-id="05a98-121">Extended key.</span></span> <span data-ttu-id="05a98-122">如果這個值是擴充索引鍵，則此值為1。</span><span class="sxs-lookup"><span data-stu-id="05a98-122">This value is 1 if it is an extended key.</span></span> <span data-ttu-id="05a98-123">否則，它是0。</span><span class="sxs-lookup"><span data-stu-id="05a98-123">Otherwise, it is 0.</span></span> |
| <span data-ttu-id="05a98-124">25-28</span><span class="sxs-lookup"><span data-stu-id="05a98-124">25-28</span></span> | <span data-ttu-id="05a98-125">未使用。</span><span class="sxs-lookup"><span data-stu-id="05a98-125">Not used.</span></span>                                                                   |
| <span data-ttu-id="05a98-126">29</span><span class="sxs-lookup"><span data-stu-id="05a98-126">29</span></span>    | <span data-ttu-id="05a98-127">內容程式碼。</span><span class="sxs-lookup"><span data-stu-id="05a98-127">Context code.</span></span> <span data-ttu-id="05a98-128">這個值一定是 0。</span><span class="sxs-lookup"><span data-stu-id="05a98-128">This value is always 0.</span></span>                                       |
| <span data-ttu-id="05a98-129">30</span><span class="sxs-lookup"><span data-stu-id="05a98-129">30</span></span>    | <span data-ttu-id="05a98-130">先前的金鑰狀態。</span><span class="sxs-lookup"><span data-stu-id="05a98-130">Previous key state.</span></span> <span data-ttu-id="05a98-131">如果機碼已關閉，則此值為1，如果已啟動則為0。</span><span class="sxs-lookup"><span data-stu-id="05a98-131">This value is 1 if the key is down or 0 if it is up.</span></span>    |
| <span data-ttu-id="05a98-132">31</span><span class="sxs-lookup"><span data-stu-id="05a98-132">31</span></span>    | <span data-ttu-id="05a98-133">轉換狀態。</span><span class="sxs-lookup"><span data-stu-id="05a98-133">Transition state.</span></span> <span data-ttu-id="05a98-134">這個值一定是 0。</span><span class="sxs-lookup"><span data-stu-id="05a98-134">This value is always 0.</span></span>                                   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05a98-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="05a98-135">Return value</span></span>

<span data-ttu-id="05a98-136">如果應用程式處理此訊息，則應該會傳回0。</span><span class="sxs-lookup"><span data-stu-id="05a98-136">An application should return 0 if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="05a98-137">備註</span><span class="sxs-lookup"><span data-stu-id="05a98-137">Remarks</span></span>

<span data-ttu-id="05a98-138">應用程式可處理此訊息，或將其傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  函式，以產生相符的 [**WM \_ KEYDOWN**](../inputdev/wm-keydown.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="05a98-138">An application can process this message or pass it to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function to generate a matching [**WM\_KEYDOWN**](../inputdev/wm-keydown.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="05a98-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="05a98-139">Requirements</span></span>



| <span data-ttu-id="05a98-140">需求</span><span class="sxs-lookup"><span data-stu-id="05a98-140">Requirement</span></span> | <span data-ttu-id="05a98-141">值</span><span class="sxs-lookup"><span data-stu-id="05a98-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05a98-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="05a98-142">Minimum supported client</span></span><br/> | <span data-ttu-id="05a98-143">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05a98-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="05a98-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="05a98-144">Minimum supported server</span></span><br/> | <span data-ttu-id="05a98-145">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05a98-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="05a98-146">標頭</span><span class="sxs-lookup"><span data-stu-id="05a98-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="05a98-147"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="05a98-147"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05a98-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="05a98-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05a98-149">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="05a98-149">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="05a98-150">輸入方法管理員訊息</span><span class="sxs-lookup"><span data-stu-id="05a98-150">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 

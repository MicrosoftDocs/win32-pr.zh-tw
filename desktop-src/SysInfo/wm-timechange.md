---
description: 每當系統時間變更時，就會傳送一則訊息。
ms.assetid: 94b5b6f7-04bb-4e0a-848b-e2b31ffc2938
title: 'WM_TIMECHANGE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d43bb5cd4284813c45ab074a93a9cd9699883aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978913"
---
# <a name="wm_timechange-message"></a><span data-ttu-id="646b4-103">WM \_ TIMECHANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="646b4-103">WM\_TIMECHANGE message</span></span>

<span data-ttu-id="646b4-104">每當系統時間變更時，就會傳送一則訊息。</span><span class="sxs-lookup"><span data-stu-id="646b4-104">A message that is sent whenever there is a change in the system time.</span></span>

<span data-ttu-id="646b4-105">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="646b4-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // message identifier
  WPARAM wParam,   // not used; must be zero
  LPARAM lParam    // not used; must be zero
);
```



## <a name="parameters"></a><span data-ttu-id="646b4-106">參數</span><span class="sxs-lookup"><span data-stu-id="646b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="646b4-107">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="646b4-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="646b4-108">視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="646b4-108">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="646b4-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="646b4-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="646b4-110">**WM \_TIMECHANGE** 識別碼。</span><span class="sxs-lookup"><span data-stu-id="646b4-110">**WM\_TIMECHANGE** identifier.</span></span>

</dd> <dt>

<span data-ttu-id="646b4-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="646b4-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="646b4-112">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="646b4-112">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="646b4-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="646b4-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="646b4-114">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="646b4-114">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="646b4-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="646b4-115">Return value</span></span>

<span data-ttu-id="646b4-116">如果應用程式處理此訊息，則應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="646b4-116">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="646b4-117">備註</span><span class="sxs-lookup"><span data-stu-id="646b4-117">Remarks</span></span>

<span data-ttu-id="646b4-118">應用程式不應廣播此訊息，因為當應用程式變更系統時間時，系統會廣播此訊息。</span><span class="sxs-lookup"><span data-stu-id="646b4-118">An application should not broadcast this message, because the system will broadcast this message when the application changes the system time.</span></span>

## <a name="requirements"></a><span data-ttu-id="646b4-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="646b4-119">Requirements</span></span>



| <span data-ttu-id="646b4-120">需求</span><span class="sxs-lookup"><span data-stu-id="646b4-120">Requirement</span></span> | <span data-ttu-id="646b4-121">值</span><span class="sxs-lookup"><span data-stu-id="646b4-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="646b4-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="646b4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="646b4-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="646b4-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="646b4-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="646b4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="646b4-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="646b4-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="646b4-126">標頭</span><span class="sxs-lookup"><span data-stu-id="646b4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="646b4-127"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="646b4-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="646b4-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="646b4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="646b4-129">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="646b4-129">**SendMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 


---
description: '\_當您第一次建立視窗時，于 WM 建立訊息之前傳送。'
ms.assetid: 5dd0eda3-83a6-4077-a7a3-e371c9413b0f
title: 'WM_NCCREATE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8757cbdeba49d54f6e5d842a5b40c7f7ae61cac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982433"
---
# <a name="wm_nccreate-message"></a><span data-ttu-id="3cb43-103">WM \_ NCCREATE 訊息</span><span class="sxs-lookup"><span data-stu-id="3cb43-103">WM\_NCCREATE message</span></span>

<span data-ttu-id="3cb43-104">當您第一次建立視窗時，于 [**WM \_ 建立**](wm-create.md) 訊息之前傳送。</span><span class="sxs-lookup"><span data-stu-id="3cb43-104">Sent prior to the [**WM\_CREATE**](wm-create.md) message when a window is first created.</span></span>

<span data-ttu-id="3cb43-105">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="3cb43-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCCREATE                     0x0081
```



## <a name="parameters"></a><span data-ttu-id="3cb43-106">參數</span><span class="sxs-lookup"><span data-stu-id="3cb43-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cb43-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3cb43-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3cb43-108">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="3cb43-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3cb43-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3cb43-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3cb43-110">[**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa)結構的指標，其中包含所要建立之視窗的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3cb43-110">A pointer to the [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure that contains information about the window being created.</span></span> <span data-ttu-id="3cb43-111">**CREATESTRUCT** 的成員與 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)函數的參數相同。</span><span class="sxs-lookup"><span data-stu-id="3cb43-111">The members of **CREATESTRUCT** are identical to the parameters of the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cb43-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="3cb43-112">Return value</span></span>

<span data-ttu-id="3cb43-113">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="3cb43-113">Type: **LRESULT**</span></span>

<span data-ttu-id="3cb43-114">如果應用程式處理此訊息，則應該傳回 **TRUE** 以繼續建立視窗。</span><span class="sxs-lookup"><span data-stu-id="3cb43-114">If an application processes this message, it should return **TRUE** to continue creation of the window.</span></span> <span data-ttu-id="3cb43-115">如果應用程式傳回 **FALSE**，則 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) 或 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 函數會傳回 **Null** 控制碼。</span><span class="sxs-lookup"><span data-stu-id="3cb43-115">If the application returns **FALSE**, the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function will return a **NULL** handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cb43-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="3cb43-116">Requirements</span></span>



| <span data-ttu-id="3cb43-117">需求</span><span class="sxs-lookup"><span data-stu-id="3cb43-117">Requirement</span></span> | <span data-ttu-id="3cb43-118">值</span><span class="sxs-lookup"><span data-stu-id="3cb43-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cb43-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3cb43-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3cb43-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3cb43-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3cb43-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3cb43-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3cb43-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3cb43-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3cb43-123">標頭</span><span class="sxs-lookup"><span data-stu-id="3cb43-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3cb43-124"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="3cb43-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cb43-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3cb43-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="3cb43-126">**參考**</span><span class="sxs-lookup"><span data-stu-id="3cb43-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3cb43-127">**CreateWindow**</span><span class="sxs-lookup"><span data-stu-id="3cb43-127">**CreateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[<span data-ttu-id="3cb43-128">**CreateWindowEx**</span><span class="sxs-lookup"><span data-stu-id="3cb43-128">**CreateWindowEx**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[<span data-ttu-id="3cb43-129">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="3cb43-129">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="3cb43-130">**CREATESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="3cb43-130">**CREATESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[<span data-ttu-id="3cb43-131">**WM \_ 建立**</span><span class="sxs-lookup"><span data-stu-id="3cb43-131">**WM\_CREATE**</span></span>](wm-create.md)
</dt> <dt>

<span data-ttu-id="3cb43-132">**概念**</span><span class="sxs-lookup"><span data-stu-id="3cb43-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3cb43-133">Windows</span><span class="sxs-lookup"><span data-stu-id="3cb43-133">Windows</span></span>](windows.md)
</dt> </dl>

 

 

---
title: 'WM_SETFOCUS 訊息 (Winuser .h) '
description: 在取得鍵盤焦點之後傳送至視窗。
ms.assetid: 77180e4c-95a6-41a4-93d9-033381ae7543
keywords:
- WM_SETFOCUS 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b304d7f7739ce551c1efc6a1d33a934c48dc8b4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466669"
---
# <a name="wm_setfocus-message"></a><span data-ttu-id="c5c87-104">WM \_ SETFOCUS 訊息</span><span class="sxs-lookup"><span data-stu-id="c5c87-104">WM\_SETFOCUS message</span></span>

<span data-ttu-id="c5c87-105">在取得鍵盤焦點之後傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="c5c87-105">Sent to a window after it has gained the keyboard focus.</span></span>


```C++
#define WM_SETFOCUS                     0x0007
```



## <a name="parameters"></a><span data-ttu-id="c5c87-106">參數</span><span class="sxs-lookup"><span data-stu-id="c5c87-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5c87-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c5c87-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c5c87-108">已失去鍵盤焦點的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="c5c87-108">A handle to the window that has lost the keyboard focus.</span></span> <span data-ttu-id="c5c87-109">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c5c87-109">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c5c87-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c5c87-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c5c87-111">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="c5c87-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5c87-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="c5c87-112">Return value</span></span>

<span data-ttu-id="c5c87-113">如果應用程式處理此訊息，則應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="c5c87-113">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5c87-114">備註</span><span class="sxs-lookup"><span data-stu-id="c5c87-114">Remarks</span></span>

<span data-ttu-id="c5c87-115">若要顯示插入號，應用程式應該在收到 **WM \_ SETFOCUS** 訊息時呼叫適當的插入號函式。</span><span class="sxs-lookup"><span data-stu-id="c5c87-115">To display a caret, an application should call the appropriate caret functions when it receives the **WM\_SETFOCUS** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5c87-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5c87-116">Requirements</span></span>



| <span data-ttu-id="c5c87-117">需求</span><span class="sxs-lookup"><span data-stu-id="c5c87-117">Requirement</span></span> | <span data-ttu-id="c5c87-118">值</span><span class="sxs-lookup"><span data-stu-id="c5c87-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5c87-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c5c87-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c5c87-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5c87-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c5c87-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c5c87-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c5c87-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5c87-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c5c87-123">標頭</span><span class="sxs-lookup"><span data-stu-id="c5c87-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5c87-124"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="c5c87-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5c87-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5c87-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="c5c87-126">**參考**</span><span class="sxs-lookup"><span data-stu-id="c5c87-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c5c87-127">**SetFocus**</span><span class="sxs-lookup"><span data-stu-id="c5c87-127">**SetFocus**</span></span>](/windows/win32/api/winuser/nf-winuser-setfocus)
</dt> <dt>

[<span data-ttu-id="c5c87-128">**WM \_ KILLFOCUS**</span><span class="sxs-lookup"><span data-stu-id="c5c87-128">**WM\_KILLFOCUS**</span></span>](wm-killfocus.md)
</dt> <dt>

<span data-ttu-id="c5c87-129">**概念**</span><span class="sxs-lookup"><span data-stu-id="c5c87-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c5c87-130">鍵盤輸入</span><span class="sxs-lookup"><span data-stu-id="c5c87-130">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 


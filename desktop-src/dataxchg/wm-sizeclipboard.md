---
title: 'WM_SIZECLIPBOARD 訊息 (Winuser .h) '
description: 當剪貼簿包含 CF \_ OWNERDISPLAY 格式的資料，而剪貼簿檢視器的工作區已變更時，由剪貼簿檢視器視窗傳送給剪貼簿擁有者。
ms.assetid: 95991d03-8677-4dde-b72a-082dec4834b3
keywords:
- WM_SIZECLIPBOARD 訊息資料交換
topic_type:
- apiref
api_name:
- WM_SIZECLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 235de630b20757a571b1917a975d1425bee06cde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685998"
---
# <a name="wm_sizeclipboard-message"></a><span data-ttu-id="2e04e-104">WM \_ SIZECLIPBOARD 訊息</span><span class="sxs-lookup"><span data-stu-id="2e04e-104">WM\_SIZECLIPBOARD message</span></span>

<span data-ttu-id="2e04e-105">當剪貼簿包含 [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) 格式的資料，而剪貼簿檢視器的工作區已變更時，由剪貼簿檢視器視窗傳送給剪貼簿擁有者。</span><span class="sxs-lookup"><span data-stu-id="2e04e-105">Sent to the clipboard owner by a clipboard viewer window when the clipboard contains data in the [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) format and the clipboard viewer's client area has changed size.</span></span>


```C++
#define WM_SIZECLIPBOARD                0x030B
```



## <a name="parameters"></a><span data-ttu-id="2e04e-106">參數</span><span class="sxs-lookup"><span data-stu-id="2e04e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e04e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2e04e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e04e-108">剪貼簿檢視器視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="2e04e-108">A handle to the clipboard viewer window.</span></span>

</dd> <dt>

<span data-ttu-id="2e04e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2e04e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e04e-110">全域記憶體物件的控制碼，其中包含 [**矩形**](/previous-versions//dd162897(v=vs.85)) 結構。</span><span class="sxs-lookup"><span data-stu-id="2e04e-110">A handle to a global memory object that contains a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="2e04e-111">結構會指定剪貼簿檢視器工作區的新維度。</span><span class="sxs-lookup"><span data-stu-id="2e04e-111">The structure specifies the new dimensions of the clipboard viewer's client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e04e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="2e04e-112">Return value</span></span>

<span data-ttu-id="2e04e-113">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="2e04e-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e04e-114">備註</span><span class="sxs-lookup"><span data-stu-id="2e04e-114">Remarks</span></span>

<span data-ttu-id="2e04e-115">當剪貼簿檢視器視窗即將終結或調整大小時，會以 null 矩形傳送 **WM \_ SIZECLIPBOARD** 訊息 (0、0、0、0) 作為新的大小。</span><span class="sxs-lookup"><span data-stu-id="2e04e-115">When the clipboard viewer window is about to be destroyed or resized, a **WM\_SIZECLIPBOARD** message is sent with a null rectangle (0, 0, 0, 0) as the new size.</span></span> <span data-ttu-id="2e04e-116">這可讓剪貼簿擁有者釋放其顯示資源。</span><span class="sxs-lookup"><span data-stu-id="2e04e-116">This permits the clipboard owner to free its display resources.</span></span>

<span data-ttu-id="2e04e-117">剪貼簿擁有者必須使用 [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) 函式來鎖定包含 [**RECT**](/previous-versions//dd162897(v=vs.85))的記憶體物件。</span><span class="sxs-lookup"><span data-stu-id="2e04e-117">The clipboard owner must use the [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) function to lock the memory object that contains [**RECT**](/previous-versions//dd162897(v=vs.85)).</span></span> <span data-ttu-id="2e04e-118">在傳回之前，剪貼簿擁有者必須使用 [**GlobalUnlock**](/windows/desktop/api/winbase/nf-winbase-globalunlock) 函數來解除鎖定物件。</span><span class="sxs-lookup"><span data-stu-id="2e04e-118">Before returning, the clipboard owner must unlock the object by using the [**GlobalUnlock**](/windows/desktop/api/winbase/nf-winbase-globalunlock) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e04e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="2e04e-119">Requirements</span></span>



| <span data-ttu-id="2e04e-120">需求</span><span class="sxs-lookup"><span data-stu-id="2e04e-120">Requirement</span></span> | <span data-ttu-id="2e04e-121">值</span><span class="sxs-lookup"><span data-stu-id="2e04e-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e04e-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2e04e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2e04e-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2e04e-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2e04e-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2e04e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2e04e-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2e04e-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2e04e-126">標頭</span><span class="sxs-lookup"><span data-stu-id="2e04e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e04e-127"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="2e04e-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e04e-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2e04e-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="2e04e-129">**概念**</span><span class="sxs-lookup"><span data-stu-id="2e04e-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2e04e-130">剪貼簿</span><span class="sxs-lookup"><span data-stu-id="2e04e-130">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 


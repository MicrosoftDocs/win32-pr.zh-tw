---
title: 'WM_DESTROYCLIPBOARD 訊息 (Winuser .h) '
description: 當 EmptyClipboard 函式的呼叫清空剪貼簿時，傳送給剪貼簿擁有者。 視窗會透過其 WindowProc 函數接收此訊息。
ms.assetid: 9f75b7fb-e9ae-4876-ba99-7db931b9c2ff
keywords:
- WM_DESTROYCLIPBOARD 訊息資料交換
topic_type:
- apiref
api_name:
- WM_DESTROYCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c3e4b6c2e2d378d0f78cee1824b1e4ce17a433a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935105"
---
# <a name="wm_destroyclipboard-message"></a><span data-ttu-id="d408d-105">WM \_ DESTROYCLIPBOARD 訊息</span><span class="sxs-lookup"><span data-stu-id="d408d-105">WM\_DESTROYCLIPBOARD message</span></span>

<span data-ttu-id="d408d-106">當 [**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) 函式的呼叫清空剪貼簿時，傳送給剪貼簿擁有者。</span><span class="sxs-lookup"><span data-stu-id="d408d-106">Sent to the clipboard owner when a call to the [**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) function empties the clipboard.</span></span>

<span data-ttu-id="d408d-107">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="d408d-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_DESTROYCLIPBOARD             0x0307
```



## <a name="parameters"></a><span data-ttu-id="d408d-108">參數</span><span class="sxs-lookup"><span data-stu-id="d408d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d408d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d408d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d408d-110">未使用此參數，且必須為零。</span><span class="sxs-lookup"><span data-stu-id="d408d-110">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d408d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d408d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d408d-112">未使用此參數，且必須為零。</span><span class="sxs-lookup"><span data-stu-id="d408d-112">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d408d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d408d-113">Return value</span></span>

<span data-ttu-id="d408d-114">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="d408d-114">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="d408d-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="d408d-115">Requirements</span></span>



| <span data-ttu-id="d408d-116">需求</span><span class="sxs-lookup"><span data-stu-id="d408d-116">Requirement</span></span> | <span data-ttu-id="d408d-117">值</span><span class="sxs-lookup"><span data-stu-id="d408d-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d408d-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d408d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d408d-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d408d-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d408d-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d408d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d408d-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d408d-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d408d-122">標頭</span><span class="sxs-lookup"><span data-stu-id="d408d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d408d-123"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="d408d-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d408d-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d408d-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="d408d-125">**參考**</span><span class="sxs-lookup"><span data-stu-id="d408d-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d408d-126">**EmptyClipboard**</span><span class="sxs-lookup"><span data-stu-id="d408d-126">**EmptyClipboard**</span></span>](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard)
</dt> <dt>

<span data-ttu-id="d408d-127">**概念**</span><span class="sxs-lookup"><span data-stu-id="d408d-127">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d408d-128">剪貼簿</span><span class="sxs-lookup"><span data-stu-id="d408d-128">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 


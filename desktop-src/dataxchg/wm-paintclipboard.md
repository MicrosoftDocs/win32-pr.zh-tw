---
title: 'WM_PAINTCLIPBOARD 訊息 (Winuser .h) '
description: 當剪貼簿包含 CF \_ OWNERDISPLAY 格式的資料，而剪貼簿檢視器的工作區需要重新繪製時，由剪貼簿檢視器視窗傳送給剪貼簿擁有者。
ms.assetid: 85aeefa5-e3d9-4689-a068-47b59ec7b571
keywords:
- WM_PAINTCLIPBOARD 訊息資料交換
topic_type:
- apiref
api_name:
- WM_PAINTCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8148af6b513fd1fa956d48f22dc86e618544b073
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966304"
---
# <a name="wm_paintclipboard-message"></a><span data-ttu-id="677e9-104">WM \_ PAINTCLIPBOARD 訊息</span><span class="sxs-lookup"><span data-stu-id="677e9-104">WM\_PAINTCLIPBOARD message</span></span>

<span data-ttu-id="677e9-105">當剪貼簿包含 [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) 格式的資料，而剪貼簿檢視器的工作區需要重新繪製時，由剪貼簿檢視器視窗傳送給剪貼簿擁有者。</span><span class="sxs-lookup"><span data-stu-id="677e9-105">Sent to the clipboard owner by a clipboard viewer window when the clipboard contains data in the [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) format and the clipboard viewer's client area needs repainting.</span></span>


```C++
#define WM_PAINTCLIPBOARD               0x0309
```



## <a name="parameters"></a><span data-ttu-id="677e9-106">參數</span><span class="sxs-lookup"><span data-stu-id="677e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="677e9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="677e9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="677e9-108">剪貼簿檢視器視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="677e9-108">A handle to the clipboard viewer window.</span></span>

</dd> <dt>

<span data-ttu-id="677e9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="677e9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="677e9-110">全域記憶體物件的控制碼，其中包含 [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) 結構。</span><span class="sxs-lookup"><span data-stu-id="677e9-110">A handle to a global memory object that contains a [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) structure.</span></span> <span data-ttu-id="677e9-111">結構會定義要繪製之工作區的部分。</span><span class="sxs-lookup"><span data-stu-id="677e9-111">The structure defines the part of the client area to paint.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="677e9-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="677e9-112">Return value</span></span>

<span data-ttu-id="677e9-113">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="677e9-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="677e9-114">備註</span><span class="sxs-lookup"><span data-stu-id="677e9-114">Remarks</span></span>

<span data-ttu-id="677e9-115">若要判斷整個工作區或其中一部分是否需要重新繪製，剪貼簿擁有者必須將 [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct)的 **rcPaint** 成員中提供的繪圖區域尺寸，與最新的 [**WM \_ SIZECLIPBOARD**](wm-sizeclipboard.md)訊息中提供的維度進行比較。</span><span class="sxs-lookup"><span data-stu-id="677e9-115">To determine whether the entire client area or just a portion of it needs repainting, the clipboard owner must compare the dimensions of the drawing area given in the **rcPaint** member of [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) to the dimensions given in the most recent [**WM\_SIZECLIPBOARD**](wm-sizeclipboard.md) message.</span></span>

<span data-ttu-id="677e9-116">剪貼簿擁有者必須使用 [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) 函數來鎖定包含 [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) 結構的記憶體。</span><span class="sxs-lookup"><span data-stu-id="677e9-116">The clipboard owner must use the [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) function to lock the memory that contains the [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) structure.</span></span> <span data-ttu-id="677e9-117">在傳回之前，剪貼簿擁有者必須使用 [**GlobalUnlock**](/windows/desktop/api/winbase/nf-winbase-globalunlock) 函數來解除鎖定該記憶體。</span><span class="sxs-lookup"><span data-stu-id="677e9-117">Before returning, the clipboard owner must unlock that memory by using the [**GlobalUnlock**](/windows/desktop/api/winbase/nf-winbase-globalunlock) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="677e9-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="677e9-118">Requirements</span></span>



| <span data-ttu-id="677e9-119">需求</span><span class="sxs-lookup"><span data-stu-id="677e9-119">Requirement</span></span> | <span data-ttu-id="677e9-120">值</span><span class="sxs-lookup"><span data-stu-id="677e9-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="677e9-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="677e9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="677e9-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="677e9-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="677e9-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="677e9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="677e9-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="677e9-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="677e9-125">標頭</span><span class="sxs-lookup"><span data-stu-id="677e9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="677e9-126"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="677e9-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="677e9-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="677e9-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="677e9-128">**參考**</span><span class="sxs-lookup"><span data-stu-id="677e9-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="677e9-129">**WM \_ SIZECLIPBOARD**</span><span class="sxs-lookup"><span data-stu-id="677e9-129">**WM\_SIZECLIPBOARD**</span></span>](wm-sizeclipboard.md)
</dt> <dt>

<span data-ttu-id="677e9-130">**概念**</span><span class="sxs-lookup"><span data-stu-id="677e9-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="677e9-131">剪貼簿</span><span class="sxs-lookup"><span data-stu-id="677e9-131">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 


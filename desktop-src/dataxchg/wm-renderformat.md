---
title: 'WM_RENDERFORMAT 訊息 (Winuser .h) '
description: 如果已延遲轉譯特定的剪貼簿格式，且應用程式已要求該格式的資料，則傳送給剪貼簿擁有者。
ms.assetid: 81638109-4c5e-4b4c-b2db-4208b6ee83cc
keywords:
- WM_RENDERFORMAT 訊息資料交換
topic_type:
- apiref
api_name:
- WM_RENDERFORMAT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab9d0e8539dc666c7a791a24c9ba7ac772c3c2c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317260"
---
# <a name="wm_renderformat-message"></a><span data-ttu-id="9adb6-104">WM \_ RENDERFORMAT 訊息</span><span class="sxs-lookup"><span data-stu-id="9adb6-104">WM\_RENDERFORMAT message</span></span>

<span data-ttu-id="9adb6-105">如果已延遲轉譯特定的剪貼簿格式，且應用程式已要求該格式的資料，則傳送給剪貼簿擁有者。</span><span class="sxs-lookup"><span data-stu-id="9adb6-105">Sent to the clipboard owner if it has delayed rendering a specific clipboard format and if an application has requested data in that format.</span></span> <span data-ttu-id="9adb6-106">剪貼簿擁有者必須以指定的格式轉譯資料，並藉由呼叫 [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) 函式將其放在剪貼簿上。</span><span class="sxs-lookup"><span data-stu-id="9adb6-106">The clipboard owner must render data in the specified format and place it on the clipboard by calling the [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) function.</span></span>


```C++
#define WM_RENDERFORMAT                 0x0305
```



## <a name="parameters"></a><span data-ttu-id="9adb6-107">參數</span><span class="sxs-lookup"><span data-stu-id="9adb6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9adb6-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9adb6-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9adb6-109">要呈現的 [剪貼簿格式](standard-clipboard-formats.md) 。</span><span class="sxs-lookup"><span data-stu-id="9adb6-109">The [clipboard format](standard-clipboard-formats.md) to be rendered.</span></span>

</dd> <dt>

<span data-ttu-id="9adb6-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9adb6-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9adb6-111">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="9adb6-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9adb6-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="9adb6-112">Return value</span></span>

<span data-ttu-id="9adb6-113">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="9adb6-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9adb6-114">備註</span><span class="sxs-lookup"><span data-stu-id="9adb6-114">Remarks</span></span>

<span data-ttu-id="9adb6-115">回應 **WM \_ RENDERFORMAT** 訊息時，剪貼簿擁有者必須先開啟剪貼簿，然後再呼叫 [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)。</span><span class="sxs-lookup"><span data-stu-id="9adb6-115">When responding to a **WM\_RENDERFORMAT** message, the clipboard owner must not open the clipboard before calling [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata).</span></span> <span data-ttu-id="9adb6-116">在將資料放入資料以回應 **WM \_ RENDERFORMAT** 之前，不需要開啟剪貼簿，而任何開啟剪貼簿的嘗試都會失敗，因為剪貼簿目前正由要求轉譯格式的應用程式開啟。</span><span class="sxs-lookup"><span data-stu-id="9adb6-116">Opening the clipboard is not necessary before placing data in response to **WM\_RENDERFORMAT**, and any attempt to open the clipboard will fail because the clipboard is currently being held open by the application that requested the format to be rendered.</span></span>

## <a name="requirements"></a><span data-ttu-id="9adb6-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="9adb6-117">Requirements</span></span>



| <span data-ttu-id="9adb6-118">需求</span><span class="sxs-lookup"><span data-stu-id="9adb6-118">Requirement</span></span> | <span data-ttu-id="9adb6-119">值</span><span class="sxs-lookup"><span data-stu-id="9adb6-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9adb6-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9adb6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9adb6-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9adb6-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9adb6-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9adb6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9adb6-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9adb6-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9adb6-124">標頭</span><span class="sxs-lookup"><span data-stu-id="9adb6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9adb6-125"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="9adb6-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9adb6-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9adb6-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="9adb6-127">**參考**</span><span class="sxs-lookup"><span data-stu-id="9adb6-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9adb6-128">**SetClipboardData**</span><span class="sxs-lookup"><span data-stu-id="9adb6-128">**SetClipboardData**</span></span>](/windows/win32/api/winuser/nf-winuser-setclipboarddata)
</dt> <dt>

[<span data-ttu-id="9adb6-129">**WM \_ RENDERALLFORMATS**</span><span class="sxs-lookup"><span data-stu-id="9adb6-129">**WM\_RENDERALLFORMATS**</span></span>](wm-renderallformats.md)
</dt> <dt>

<span data-ttu-id="9adb6-130">**概念**</span><span class="sxs-lookup"><span data-stu-id="9adb6-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9adb6-131">剪貼簿</span><span class="sxs-lookup"><span data-stu-id="9adb6-131">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

 






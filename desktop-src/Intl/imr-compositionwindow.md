---
description: 當選取的輸入法需要組合視窗的相關資訊時，通知應用程式。 應用程式會透過 WM \_ IME 要求訊息接收此命令 \_ ，並使用如下所示的參數設定。
ms.assetid: 08fd7119-d225-4a78-b2cd-8b58887c9139
title: 'IMR_COMPOSITIONWINDOW 通知碼 (Imm) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6af0481ccebc59968fe85a489c856388a04dbece
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983484"
---
# <a name="imr_compositionwindow-notification-code"></a><span data-ttu-id="cfec6-104">IMR \_ COMPOSITIONWINDOW 通知碼</span><span class="sxs-lookup"><span data-stu-id="cfec6-104">IMR\_COMPOSITIONWINDOW notification code</span></span>

<span data-ttu-id="cfec6-105">當選取的輸入法需要組合視窗的相關資訊時，通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="cfec6-105">Notifies an application when a selected IME needs information about the composition window.</span></span> <span data-ttu-id="cfec6-106">應用程式會透過 [**WM \_ IME \_ 要求**](wm-ime-request.md) 訊息接收此命令，並使用如下所示的參數設定。</span><span class="sxs-lookup"><span data-stu-id="cfec6-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameters set as shown below.</span></span>


```C++
LRESULT IMR_COMPOSITIONWINDOW
```



## <a name="parameters"></a><span data-ttu-id="cfec6-107">參數</span><span class="sxs-lookup"><span data-stu-id="cfec6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfec6-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="cfec6-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="cfec6-109">設定為 IMR \_ COMPOSITIONWINDOW。</span><span class="sxs-lookup"><span data-stu-id="cfec6-109">Set to IMR\_COMPOSITIONWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="cfec6-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="cfec6-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="cfec6-111">包含 [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) 結構之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="cfec6-111">Pointer to a buffer containing a [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfec6-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="cfec6-112">Return Value</span></span>

<span data-ttu-id="cfec6-113">如果應用程式填滿 [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) 結構，則傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="cfec6-113">Returns a nonzero value if the application fills in the [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) structure.</span></span> <span data-ttu-id="cfec6-114">否則，此命令會傳回0。</span><span class="sxs-lookup"><span data-stu-id="cfec6-114">Otherwise, the command returns 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfec6-115">備註</span><span class="sxs-lookup"><span data-stu-id="cfec6-115">Remarks</span></span>

<span data-ttu-id="cfec6-116">此命令可由 IME 傳送至已 \_ 在 [**WM \_ IME \_ SETCONTEXT**](wm-ime-setcontext.md) 訊息處理常式中清除 ISC SHOWUICOMPOSITIONWINDOW 旗標的視窗。</span><span class="sxs-lookup"><span data-stu-id="cfec6-116">This command can be sent by the IME to a window that has cleared the ISC\_SHOWUICOMPOSITIONWINDOW flag in the [**WM\_IME\_SETCONTEXT**](wm-ime-setcontext.md) message handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfec6-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="cfec6-117">Requirements</span></span>



| <span data-ttu-id="cfec6-118">需求</span><span class="sxs-lookup"><span data-stu-id="cfec6-118">Requirement</span></span> | <span data-ttu-id="cfec6-119">值</span><span class="sxs-lookup"><span data-stu-id="cfec6-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfec6-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cfec6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cfec6-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cfec6-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="cfec6-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cfec6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cfec6-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cfec6-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cfec6-124">標頭</span><span class="sxs-lookup"><span data-stu-id="cfec6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfec6-125"><dt>Imm (包括 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="cfec6-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfec6-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cfec6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfec6-127">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="cfec6-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="cfec6-128">輸入方法管理員命令</span><span class="sxs-lookup"><span data-stu-id="cfec6-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="cfec6-129">**COMPOSITIONFORM**</span><span class="sxs-lookup"><span data-stu-id="cfec6-129">**COMPOSITIONFORM**</span></span>](/windows/win32/api/imm/ns-imm-compositionform)
</dt> <dt>

[<span data-ttu-id="cfec6-130">**WM \_ IME \_ 要求**</span><span class="sxs-lookup"><span data-stu-id="cfec6-130">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> <dt>

[<span data-ttu-id="cfec6-131">**WM \_ IME \_ SETCONTEXT**</span><span class="sxs-lookup"><span data-stu-id="cfec6-131">**WM\_IME\_SETCONTEXT**</span></span>](wm-ime-setcontext.md)
</dt> </dl>

 

 





---
description: 當選取的輸入法需要組合視窗所使用之字型的相關資訊時，就會通知應用程式。 應用程式會透過包含參數的 WM \_ IME 要求訊息接收此命令， \_ 如下所示。
ms.assetid: 46bb71ee-8dc9-4ef0-bc4e-59866c122bf7
title: 'IMR_COMPOSITIONFONT 通知碼 (Imm) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8be2751944e451475fd0bde9a34d8902dcaf30e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980840"
---
# <a name="imr_compositionfont-notification-code"></a><span data-ttu-id="24a4a-104">IMR \_ COMPOSITIONFONT 通知碼</span><span class="sxs-lookup"><span data-stu-id="24a4a-104">IMR\_COMPOSITIONFONT notification code</span></span>

<span data-ttu-id="24a4a-105">當選取的輸入法需要組合視窗所使用之字型的相關資訊時，就會通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="24a4a-105">Notifies an application when a selected IME needs information about the font used by the composition window.</span></span> <span data-ttu-id="24a4a-106">應用程式會透過包含參數的 [**WM \_ IME \_ 要求**](wm-ime-request.md) 訊息接收此命令，如下所示。</span><span class="sxs-lookup"><span data-stu-id="24a4a-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameters as shown below.</span></span>


```C++
LRESULT IMR_COMPOSITIONFONT
```



## <a name="parameters"></a><span data-ttu-id="24a4a-107">參數</span><span class="sxs-lookup"><span data-stu-id="24a4a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24a4a-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="24a4a-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="24a4a-109">設定為 IMR \_ COMPOSITIONFONT。</span><span class="sxs-lookup"><span data-stu-id="24a4a-109">Set to IMR\_COMPOSITIONFONT.</span></span>

</dd> <dt>

<span data-ttu-id="24a4a-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="24a4a-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="24a4a-111">包含 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) 結構之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="24a4a-111">Pointer to a buffer containing a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span> <span data-ttu-id="24a4a-112">應用程式會填入目前撰寫視窗的值。</span><span class="sxs-lookup"><span data-stu-id="24a4a-112">The application fills in the values for the current composition window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24a4a-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="24a4a-113">Return Value</span></span>

<span data-ttu-id="24a4a-114">如果應用程式填滿 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) 結構，則傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="24a4a-114">Returns a nonzero value if the application fills in the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span> <span data-ttu-id="24a4a-115">否則，此命令會傳回0。</span><span class="sxs-lookup"><span data-stu-id="24a4a-115">Otherwise, the command returns 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="24a4a-116">備註</span><span class="sxs-lookup"><span data-stu-id="24a4a-116">Remarks</span></span>

<span data-ttu-id="24a4a-117">此命令可由 IME 傳送至在 \_ [**WM \_ IME \_ SETCONTEXT**](wm-ime-setcontext.md) 訊息處理常式中清除 ISC SHOWUICOMPOSITIONWINDOW 旗標的視窗。</span><span class="sxs-lookup"><span data-stu-id="24a4a-117">This command can be sent by the IME to a window that cleared the ISC\_SHOWUICOMPOSITIONWINDOW flag in the [**WM\_IME\_SETCONTEXT**](wm-ime-setcontext.md) message handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="24a4a-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="24a4a-118">Requirements</span></span>



| <span data-ttu-id="24a4a-119">需求</span><span class="sxs-lookup"><span data-stu-id="24a4a-119">Requirement</span></span> | <span data-ttu-id="24a4a-120">值</span><span class="sxs-lookup"><span data-stu-id="24a4a-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24a4a-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="24a4a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="24a4a-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="24a4a-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="24a4a-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="24a4a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="24a4a-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="24a4a-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="24a4a-125">標頭</span><span class="sxs-lookup"><span data-stu-id="24a4a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="24a4a-126"><dt>Imm (包括 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="24a4a-126"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24a4a-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="24a4a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24a4a-128">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="24a4a-128">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="24a4a-129">輸入方法管理員命令</span><span class="sxs-lookup"><span data-stu-id="24a4a-129">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="24a4a-130">**WM \_ IME \_ 要求**</span><span class="sxs-lookup"><span data-stu-id="24a4a-130">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> <dt>

[<span data-ttu-id="24a4a-131">**WM \_ IME \_ SETCONTEXT**</span><span class="sxs-lookup"><span data-stu-id="24a4a-131">**WM\_IME\_SETCONTEXT**</span></span>](wm-ime-setcontext.md)
</dt> </dl>

 

 

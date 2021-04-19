---
description: 當選取的輸入法需要候選視窗的相關資訊時，Notfies 應用程式。 應用程式會透過 \_ 包含參數設定的 WM IME 要求訊息接收此命令， \_ 如下所示。
ms.assetid: 35849290-a5be-406f-82f5-4a7e2af48586
title: 'IMR_CANDIDATEWINDOW 通知碼 (Imm) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edb905acace27cc9bb04ce2b14dc6a685b7c4f8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993122"
---
# <a name="imr_candidatewindow-notification-code"></a><span data-ttu-id="d37b3-104">IMR \_ CANDIDATEWINDOW 通知碼</span><span class="sxs-lookup"><span data-stu-id="d37b3-104">IMR\_CANDIDATEWINDOW notification code</span></span>

<span data-ttu-id="d37b3-105">當選取的輸入法需要候選視窗的相關資訊時，Notfies 應用程式。</span><span class="sxs-lookup"><span data-stu-id="d37b3-105">Notfies an application when a selected IME needs information about the candidate window.</span></span> <span data-ttu-id="d37b3-106">應用程式會透過包含參數設定的 [**WM \_ IME \_ 要求**](wm-ime-request.md) 訊息接收此命令，如下所示。</span><span class="sxs-lookup"><span data-stu-id="d37b3-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameter settings as shown below.</span></span>


```C++
LRESULT IMR_CANDIDATEWINDOW
```



## <a name="parameters"></a><span data-ttu-id="d37b3-107">參數</span><span class="sxs-lookup"><span data-stu-id="d37b3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d37b3-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="d37b3-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="d37b3-109">設定為 IMR \_ CANDIDATEWINDOW。</span><span class="sxs-lookup"><span data-stu-id="d37b3-109">Set to IMR\_CANDIDATEWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="d37b3-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="d37b3-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="d37b3-111">包含 [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) 結構之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="d37b3-111">Pointer to a buffer containing a [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) structure.</span></span> <span data-ttu-id="d37b3-112">其 **dwIndex** 成員包含參考之候選視窗的索引。</span><span class="sxs-lookup"><span data-stu-id="d37b3-112">Its **dwIndex** member contains the index to the candidate window referenced.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d37b3-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d37b3-113">Return Value</span></span>

<span data-ttu-id="d37b3-114">如果應用程式填滿 [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) 結構，則傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="d37b3-114">Returns a nonzero value if the application fills in the [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) structure.</span></span> <span data-ttu-id="d37b3-115">否則，此命令會傳回0。</span><span class="sxs-lookup"><span data-stu-id="d37b3-115">Otherwise, the command returns 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="d37b3-116">備註</span><span class="sxs-lookup"><span data-stu-id="d37b3-116">Remarks</span></span>

<span data-ttu-id="d37b3-117">此命令可由 IME 傳送至已 \_ 在 [**WM \_ IME \_ SETCONTEXT**](wm-ime-setcontext.md) 訊息處理常式中清除 ISC SHOWUICANDIDATEWINDOW 旗標的視窗。</span><span class="sxs-lookup"><span data-stu-id="d37b3-117">This command can be sent by the IME to a window that has cleared the ISC\_SHOWUICANDIDATEWINDOW flag in the [**WM\_IME\_SETCONTEXT**](wm-ime-setcontext.md) message handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="d37b3-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="d37b3-118">Requirements</span></span>



| <span data-ttu-id="d37b3-119">需求</span><span class="sxs-lookup"><span data-stu-id="d37b3-119">Requirement</span></span> | <span data-ttu-id="d37b3-120">值</span><span class="sxs-lookup"><span data-stu-id="d37b3-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d37b3-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d37b3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d37b3-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d37b3-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d37b3-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d37b3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d37b3-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d37b3-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d37b3-125">標頭</span><span class="sxs-lookup"><span data-stu-id="d37b3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d37b3-126"><dt>Imm (包括 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d37b3-126"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d37b3-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d37b3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d37b3-128">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="d37b3-128">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="d37b3-129">輸入方法管理員命令</span><span class="sxs-lookup"><span data-stu-id="d37b3-129">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="d37b3-130">**CANDIDATEFORM**</span><span class="sxs-lookup"><span data-stu-id="d37b3-130">**CANDIDATEFORM**</span></span>](/windows/win32/api/imm/ns-imm-candidateform)
</dt> <dt>

[<span data-ttu-id="d37b3-131">**WM \_ IME \_ 要求**</span><span class="sxs-lookup"><span data-stu-id="d37b3-131">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> <dt>

[<span data-ttu-id="d37b3-132">**WM \_ IME \_ SETCONTEXT**</span><span class="sxs-lookup"><span data-stu-id="d37b3-132">**WM\_IME\_SETCONTEXT**</span></span>](wm-ime-setcontext.md)
</dt> </dl>

 

 





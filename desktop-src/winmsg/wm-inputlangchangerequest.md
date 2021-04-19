---
description: 當使用者選擇新的輸入語言時，會使用鍵盤控制台應用程式中所指定的熱鍵 () 或從系統工作列上的指標，張貼至視窗。
ms.assetid: db38c31c-6ae4-4401-82b8-7fd220c1678c
title: 'WM_INPUTLANGCHANGEREQUEST 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1df361c479978083c29281764e65c48b131c22b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982434"
---
# <a name="wm_inputlangchangerequest-message"></a><span data-ttu-id="c2541-103">WM \_ INPUTLANGCHANGEREQUEST 訊息</span><span class="sxs-lookup"><span data-stu-id="c2541-103">WM\_INPUTLANGCHANGEREQUEST message</span></span>

<span data-ttu-id="c2541-104">當使用者選擇新的輸入語言時，會使用鍵盤控制台應用程式中所指定的熱鍵 () 或從系統工作列上的指標，張貼至視窗。</span><span class="sxs-lookup"><span data-stu-id="c2541-104">Posted to the window with the focus when the user chooses a new input language, either with the hotkey (specified in the Keyboard control panel application) or from the indicator on the system taskbar.</span></span> <span data-ttu-id="c2541-105">應用程式可以藉由將訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式或拒絕變更 (來接受變更，並使其無法在不) 的情況下立即返回。</span><span class="sxs-lookup"><span data-stu-id="c2541-105">An application can accept the change by passing the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function or reject the change (and prevent it from taking place) by returning immediately.</span></span>

<span data-ttu-id="c2541-106">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="c2541-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_INPUTLANGCHANGEREQUEST       0x0050
```



## <a name="parameters"></a><span data-ttu-id="c2541-107">參數</span><span class="sxs-lookup"><span data-stu-id="c2541-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2541-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c2541-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c2541-109">新的輸入地區設定。</span><span class="sxs-lookup"><span data-stu-id="c2541-109">The new input locale.</span></span> <span data-ttu-id="c2541-110">這個參數可以是下列旗標的組合。</span><span class="sxs-lookup"><span data-stu-id="c2541-110">This parameter can be a combination of the following flags.</span></span>



| <span data-ttu-id="c2541-111">值</span><span class="sxs-lookup"><span data-stu-id="c2541-111">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="c2541-112">意義</span><span class="sxs-lookup"><span data-stu-id="c2541-112">Meaning</span></span>                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INPUTLANGCHANGE_BACKWARD"></span><span id="inputlangchange_backward"></span><dl> <span data-ttu-id="c2541-113"><dt>**INPUTLANGCHANGE \_反向**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="c2541-113"><dt>**INPUTLANGCHANGE\_BACKWARD**</dt> <dt>0x0004</dt></span></span> </dl>       | <span data-ttu-id="c2541-114">快速鍵是用來在已安裝的輸入地區設定清單中，選擇先前的輸入地區設定。</span><span class="sxs-lookup"><span data-stu-id="c2541-114">A hot key was used to choose the previous input locale in the installed list of input locales.</span></span> <span data-ttu-id="c2541-115">此旗標不可與 INPUTLANGCHANGE 轉寄旗標一起使用 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c2541-115">This flag cannot be used with the INPUTLANGCHANGE\_FORWARD flag.</span></span><br/> |
| <span id="INPUTLANGCHANGE_FORWARD"></span><span id="inputlangchange_forward"></span><dl> <span data-ttu-id="c2541-116"><dt>**INPUTLANGCHANGE \_轉寄**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="c2541-116"><dt>**INPUTLANGCHANGE\_FORWARD**</dt> <dt>0x0002</dt></span></span> </dl>          | <span data-ttu-id="c2541-117">快速鍵是用來選擇已安裝之輸入地區設定清單中的下一個輸入地區設定。</span><span class="sxs-lookup"><span data-stu-id="c2541-117">A hot key was used to choose the next input locale in the installed list of input locales.</span></span> <span data-ttu-id="c2541-118">此旗標不可與 INPUTLANGCHANGE 回溯旗標一起使用 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c2541-118">This flag cannot be used with the INPUTLANGCHANGE\_BACKWARD flag.</span></span><br/>    |
| <span id="INPUTLANGCHANGE_SYSCHARSET"></span><span id="inputlangchange_syscharset"></span><dl> <span data-ttu-id="c2541-119"><dt>**INPUTLANGCHANGE \_SYSCHARSET**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="c2541-119"><dt>**INPUTLANGCHANGE\_SYSCHARSET**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="c2541-120">新輸入地區設定的鍵盤配置可以搭配系統字元集使用。</span><span class="sxs-lookup"><span data-stu-id="c2541-120">The new input locale's keyboard layout can be used with the system character set.</span></span><br/>                                                                               |



 

</dd> <dt>

<span data-ttu-id="c2541-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c2541-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c2541-122">輸入地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="c2541-122">The input locale identifier.</span></span> <span data-ttu-id="c2541-123">如需詳細資訊，請參閱 [語言、地區設定和鍵盤配置](../inputdev/about-keyboard-input.md)。</span><span class="sxs-lookup"><span data-stu-id="c2541-123">For more information, see [Languages, Locales, and Keyboard Layouts](../inputdev/about-keyboard-input.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2541-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="c2541-124">Return value</span></span>

<span data-ttu-id="c2541-125">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="c2541-125">Type: **LRESULT**</span></span>

<span data-ttu-id="c2541-126">這則訊息會張貼至應用程式，而不會傳送給應用程式，因此會忽略傳回值。</span><span class="sxs-lookup"><span data-stu-id="c2541-126">This message is posted, not sent, to the application, so the return value is ignored.</span></span> <span data-ttu-id="c2541-127">若要接受變更，應用程式應該將訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)。</span><span class="sxs-lookup"><span data-stu-id="c2541-127">To accept the change, the application should pass the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="c2541-128">若要拒絕變更，應用程式應該在不呼叫 **DefWindowProc** 的情況下傳回零。</span><span class="sxs-lookup"><span data-stu-id="c2541-128">To reject the change, the application should return zero without calling **DefWindowProc**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2541-129">備註</span><span class="sxs-lookup"><span data-stu-id="c2541-129">Remarks</span></span>

<span data-ttu-id="c2541-130">當 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式收到 **WM \_ INPUTLANGCHANGEREQUEST** 訊息時，它會啟用新的輸入地區設定，並藉由傳送 [**WM \_ INPUTLANGCHANGE**](wm-inputlangchange.md) 訊息來通知應用程式變更。</span><span class="sxs-lookup"><span data-stu-id="c2541-130">When the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function receives the **WM\_INPUTLANGCHANGEREQUEST** message, it activates the new input locale and notifies the application of the change by sending the [**WM\_INPUTLANGCHANGE**](wm-inputlangchange.md) message.</span></span>

<span data-ttu-id="c2541-131">只有當您已安裝多個鍵盤配置，且已使用鍵盤 [控制台] 應用程式啟用指標時，才會在工作列上顯示語言指標。</span><span class="sxs-lookup"><span data-stu-id="c2541-131">The language indicator is present on the taskbar only if you have installed more than one keyboard layout and if you have enabled the indicator using the Keyboard control panel application.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2541-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="c2541-132">Requirements</span></span>



| <span data-ttu-id="c2541-133">需求</span><span class="sxs-lookup"><span data-stu-id="c2541-133">Requirement</span></span> | <span data-ttu-id="c2541-134">值</span><span class="sxs-lookup"><span data-stu-id="c2541-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2541-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c2541-135">Minimum supported client</span></span><br/> | <span data-ttu-id="c2541-136">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2541-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c2541-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c2541-137">Minimum supported server</span></span><br/> | <span data-ttu-id="c2541-138">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2541-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c2541-139">標頭</span><span class="sxs-lookup"><span data-stu-id="c2541-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2541-140"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="c2541-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2541-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c2541-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="c2541-142">**參考**</span><span class="sxs-lookup"><span data-stu-id="c2541-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c2541-143">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="c2541-143">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="c2541-144">**WM \_ INPUTLANGCHANGE**</span><span class="sxs-lookup"><span data-stu-id="c2541-144">**WM\_INPUTLANGCHANGE**</span></span>](wm-inputlangchange.md)
</dt> <dt>

<span data-ttu-id="c2541-145">**概念**</span><span class="sxs-lookup"><span data-stu-id="c2541-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c2541-146">Windows</span><span class="sxs-lookup"><span data-stu-id="c2541-146">Windows</span></span>](windows.md)
</dt> </dl>

 

 

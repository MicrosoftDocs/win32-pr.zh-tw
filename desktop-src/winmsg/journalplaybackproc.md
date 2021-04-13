---
UID: ''
title: JournalPlaybackProc 回呼函式
description: 播放一系列先前錄製的滑鼠和鍵盤訊息。
old-location: ''
ms.assetid: na
ms.date: 04/05/2019
ms.keywords: ''
ms.topic: reference
req.header: ''
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location: ''
api_name: ''
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 9bceede3cd6ab009aace4679dfb3d4d85bd37276
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/11/2020
ms.locfileid: "104374901"
---
# <a name="journalplaybackproc-function"></a><span data-ttu-id="36c60-103">JournalPlaybackProc 函式</span><span class="sxs-lookup"><span data-stu-id="36c60-103">JournalPlaybackProc function</span></span>

## <a name="description"></a><span data-ttu-id="36c60-104">Description</span><span class="sxs-lookup"><span data-stu-id="36c60-104">Description</span></span>

<span data-ttu-id="36c60-105">搭配 [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) 函式使用的應用程式定義或程式庫定義的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="36c60-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="36c60-106">一般而言，應用程式會使用此函式來播放一系列 **JournalRecordProc** 攔截程式先前錄製的滑鼠和鍵盤訊息。</span><span class="sxs-lookup"><span data-stu-id="36c60-106">Typically, an application uses this function to play back a series of mouse and keyboard messages recorded previously by the **JournalRecordProc** hook procedure.</span></span>
<span data-ttu-id="36c60-107">只要安裝了 **JournalPlaybackProc** 勾點程式，就會停用一般的滑鼠和鍵盤輸入。</span><span class="sxs-lookup"><span data-stu-id="36c60-107">As long as a **JournalPlaybackProc** hook procedure is installed, regular mouse and keyboard input is disabled.</span></span>

<span data-ttu-id="36c60-108">**HOOKPROC** 型別定義此回呼函數的指標。</span><span class="sxs-lookup"><span data-stu-id="36c60-108">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="36c60-109">**JournalPlaybackProc** 是應用程式定義或程式庫定義函數名稱的預留位置。</span><span class="sxs-lookup"><span data-stu-id="36c60-109">**JournalPlaybackProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK JournalPlaybackProc(
  _In_ int    code,
       WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="36c60-110">參數</span><span class="sxs-lookup"><span data-stu-id="36c60-110">Parameters</span></span>

### <a name="code-in"></a><span data-ttu-id="36c60-111">程式碼 [in]</span><span class="sxs-lookup"><span data-stu-id="36c60-111">code [in]</span></span>

<span data-ttu-id="36c60-112">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="36c60-112">Type: **int**</span></span>

<span data-ttu-id="36c60-113">攔截程式用來判斷如何處理訊息的程式碼。</span><span class="sxs-lookup"><span data-stu-id="36c60-113">A code the hook procedure uses to determine how to process the message.</span></span>
<span data-ttu-id="36c60-114">如果程式 *代碼* 小於零，則攔截程式必須將訊息傳遞至 [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) 函式，而不需要進一步處理，並且應該傳回 **CallNextHookEx** 所傳回的值。</span><span class="sxs-lookup"><span data-stu-id="36c60-114">If *code* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="36c60-115">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="36c60-115">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="36c60-116">值</span><span class="sxs-lookup"><span data-stu-id="36c60-116">Value</span></span> | <span data-ttu-id="36c60-117">意義</span><span class="sxs-lookup"><span data-stu-id="36c60-117">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="36c60-118">**HC_GETNEXT** 1</span><span class="sxs-lookup"><span data-stu-id="36c60-118">**HC_GETNEXT** 1</span></span> | <span data-ttu-id="36c60-119">攔截程式必須將目前的滑鼠或鍵盤訊息複製到 *lParam* 參數所指向的 [EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg)結構。</span><span class="sxs-lookup"><span data-stu-id="36c60-119">The hook procedure must copy the current mouse or keyboard message to the [EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg) structure pointed to by the *lParam* parameter.</span></span> |
| <span data-ttu-id="36c60-120">**HC_NOREMOVE** 3</span><span class="sxs-lookup"><span data-stu-id="36c60-120">**HC_NOREMOVE** 3</span></span> | <span data-ttu-id="36c60-121">應用程式已呼叫 [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) 函式，並將 wRemoveMsg 設定為 **PM_NOREMOVE**，表示不會在 **PeekMessage** 處理之後從訊息佇列中移除訊息。</span><span class="sxs-lookup"><span data-stu-id="36c60-121">An application has called the [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) function with wRemoveMsg set to **PM_NOREMOVE**, indicating that the message is not removed from the message queue after **PeekMessage** processing.</span></span> |
| <span data-ttu-id="36c60-122">**HC_NOREMOVE** 2</span><span class="sxs-lookup"><span data-stu-id="36c60-122">**HC_NOREMOVE** 2</span></span> | <span data-ttu-id="36c60-123">攔截程式必須做好準備，才能將下一個滑鼠或鍵盤訊息複製到 *lParam* 所指向的 **EVENTMSG** 結構。</span><span class="sxs-lookup"><span data-stu-id="36c60-123">The hook procedure must prepare to copy the next mouse or keyboard message to the **EVENTMSG** structure pointed to by *lParam*.</span></span> <span data-ttu-id="36c60-124">收到 **HC_GETNEXT** 程式碼時，攔截程式必須將訊息複製到結構中。</span><span class="sxs-lookup"><span data-stu-id="36c60-124">Upon receiving the **HC_GETNEXT** code, the hook procedure must copy the message to the structure.</span></span> |
| <span data-ttu-id="36c60-125">**HC_SYSMODALOFF** 5</span><span class="sxs-lookup"><span data-stu-id="36c60-125">**HC_SYSMODALOFF** 5</span></span> | <span data-ttu-id="36c60-126">系統強制回應對話方塊已損毀。</span><span class="sxs-lookup"><span data-stu-id="36c60-126">A system-modal dialog box has been destroyed.</span></span> <span data-ttu-id="36c60-127">攔截程式必須繼續播放訊息。</span><span class="sxs-lookup"><span data-stu-id="36c60-127">The hook procedure must resume playing back the messages.</span></span> |
| <span data-ttu-id="36c60-128">**HC_SYSMODALON** 4</span><span class="sxs-lookup"><span data-stu-id="36c60-128">**HC_SYSMODALON** 4</span></span> | <span data-ttu-id="36c60-129">系統強制回應對話方塊隨即顯示。</span><span class="sxs-lookup"><span data-stu-id="36c60-129">A system-modal dialog box is being displayed.</span></span> <span data-ttu-id="36c60-130">在對話方塊損毀之前，攔截程式必須停止播放訊息。</span><span class="sxs-lookup"><span data-stu-id="36c60-130">Until the dialog box is destroyed, the hook procedure must stop playing back messages.</span></span> |

### <a name="wparam"></a><span data-ttu-id="36c60-131">wParam</span><span class="sxs-lookup"><span data-stu-id="36c60-131">wParam</span></span>

<span data-ttu-id="36c60-132">類型： **WPARAM**</span><span class="sxs-lookup"><span data-stu-id="36c60-132">Type: **WPARAM**</span></span>

<span data-ttu-id="36c60-133">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="36c60-133">This parameter is not used.</span></span>

### <a name="lparam"></a><span data-ttu-id="36c60-134">lParam</span><span class="sxs-lookup"><span data-stu-id="36c60-134">lParam</span></span>

<span data-ttu-id="36c60-135">類型： **LPARAM**</span><span class="sxs-lookup"><span data-stu-id="36c60-135">Type: **LPARAM**</span></span>

<span data-ttu-id="36c60-136">**EVENTMSG** 結構的指標，代表由攔截程式處理的訊息。</span><span class="sxs-lookup"><span data-stu-id="36c60-136">A pointer to an **EVENTMSG** structure that represents a message being processed by the hook procedure.</span></span>
<span data-ttu-id="36c60-137">只有在 **HC_GETNEXT** 程式 *代碼* 參數時，此參數才有效。</span><span class="sxs-lookup"><span data-stu-id="36c60-137">This parameter is valid only when the *code* parameter is **HC_GETNEXT**.</span></span>

## <a name="returns"></a><span data-ttu-id="36c60-138">傳回</span><span class="sxs-lookup"><span data-stu-id="36c60-138">Returns</span></span>

<span data-ttu-id="36c60-139">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="36c60-139">Type: **LRESULT**</span></span>

<span data-ttu-id="36c60-140">若要讓系統在處理訊息之前先等待，傳回值必須是系統應等候的時間量（以時鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="36c60-140">To have the system wait before processing the message, the return value must be the amount of time, in clock ticks, that the system should wait.</span></span>

<span data-ttu-id="36c60-141"> (可以計算目前和先前輸入訊息中的時間成員之間的差異來計算這個值。 ) </span><span class="sxs-lookup"><span data-stu-id="36c60-141">(This value can be computed by calculating the difference between the time members in the current and previous input messages.)</span></span>

<span data-ttu-id="36c60-142">若要立即處理訊息，傳回值應為零。</span><span class="sxs-lookup"><span data-stu-id="36c60-142">To process the message immediately, the return value should be zero.</span></span> <span data-ttu-id="36c60-143">只有當攔截程式碼 **HC_GETNEXT** 時，才會使用傳回值;否則會予以忽略。</span><span class="sxs-lookup"><span data-stu-id="36c60-143">The return value is used only if the hook code is **HC_GETNEXT**; otherwise, it is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="36c60-144">備註</span><span class="sxs-lookup"><span data-stu-id="36c60-144">Remarks</span></span>

<span data-ttu-id="36c60-145">**JournalPlaybackProc** 攔截程式應將輸入訊息複製到 *lParam* 參數。</span><span class="sxs-lookup"><span data-stu-id="36c60-145">A **JournalPlaybackProc** hook procedure should copy an input message to The *lParam* parameter.</span></span>
<span data-ttu-id="36c60-146">訊息必須先前使用 **JournalRecordProc** 攔截程式記錄，而不應該修改訊息。</span><span class="sxs-lookup"><span data-stu-id="36c60-146">The message must have been previously recorded by using a **JournalRecordProc** hook procedure, which should not modify the message.</span></span>

<span data-ttu-id="36c60-147">若要一次或一次取出相同的訊息，您可以呼叫攔截程式，將程式 *代碼* 參數設定為 **HC_GETNEXT** ，而不需要將程式 *代碼* 設為 **HC_SKIP** 的中間呼叫。</span><span class="sxs-lookup"><span data-stu-id="36c60-147">To retrieve the same message over and over, the hook procedure can be called several times with the *code* parameter set to **HC_GETNEXT** without an intervening call with *code* set to **HC_SKIP**.</span></span>

<span data-ttu-id="36c60-148">如果程式 *代碼* 是 **HC_GETNEXT** ，且傳回值大於零，則系統會睡眠傳回值所指定的毫秒數。</span><span class="sxs-lookup"><span data-stu-id="36c60-148">If *code* is **HC_GETNEXT** and the return value is greater than zero, the system sleeps for the number of milliseconds specified by the return value.</span></span> <span data-ttu-id="36c60-149">當系統繼續時，它會再呼叫一次攔截程式，將程式 *代碼* 設為 **HC_GETNEXT** ，以取得相同的訊息。</span><span class="sxs-lookup"><span data-stu-id="36c60-149">When the system continues, it calls the hook procedure again with *code* set to **HC_GETNEXT** to retrieve the same message.</span></span>
<span data-ttu-id="36c60-150">這個新呼叫 **JournalPlaybackProc** 的傳回值應為零。否則，系統會返回 [睡眠]，以取得傳回值所指定的毫秒數、再次呼叫 **JournalPlaybackProc** 等等。</span><span class="sxs-lookup"><span data-stu-id="36c60-150">The return value from this new call to **JournalPlaybackProc** should be zero; otherwise, the system will go back to sleep for the number of milliseconds specified by the return value, call **JournalPlaybackProc** again, and so on.</span></span>
<span data-ttu-id="36c60-151">系統會顯示為沒有回應。</span><span class="sxs-lookup"><span data-stu-id="36c60-151">The system will appear to be not responding.</span></span>

<span data-ttu-id="36c60-152">與大部分其他全域攔截程式不同的是， **JournalRecordProc** 和 **JournalPlaybackProc** 攔截程式永遠會在設定攔截的執行緒內容中呼叫。</span><span class="sxs-lookup"><span data-stu-id="36c60-152">Unlike most other global hook procedures, the **JournalRecordProc** and **JournalPlaybackProc** hook procedures are always called in the context of the thread that set the hook.</span></span>

<span data-ttu-id="36c60-153">當攔截程式將控制權傳回到系統之後，就會繼續處理訊息。</span><span class="sxs-lookup"><span data-stu-id="36c60-153">After the hook procedure returns control to the system, the message continues to be processed.</span></span> <span data-ttu-id="36c60-154">如果 **HC_SKIP** 程式 *代碼*，攔截程式必須做好準備，以便在下一次呼叫時傳回下一個記錄的事件訊息。</span><span class="sxs-lookup"><span data-stu-id="36c60-154">If *code* is **HC_SKIP**, the hook procedure must prepare to return the next recorded event message on its next call.</span></span>

<span data-ttu-id="36c60-155">在 **SetWindowsHookEx** 函式的呼叫中指定 [WH_JOURNALPLAYBACK](about-hooks.md)類型和攔截程式指標，以安裝 **JournalPlaybackProc** 攔截程式。</span><span class="sxs-lookup"><span data-stu-id="36c60-155">Install the **JournalPlaybackProc** hook procedure by specifying the [WH_JOURNALPLAYBACK](about-hooks.md) type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="36c60-156">如果使用者在日誌播放期間按下 CTRL + ESC 或 CTRL + ALT + DEL，系統會停止播放、解除與日誌播放程式的掛鉤，然後將 [WM_CANCELJOURNAL](wm-canceljournal.md) 訊息張貼至日誌應用程式。</span><span class="sxs-lookup"><span data-stu-id="36c60-156">If the user presses CTRL+ESC OR CTRL+ALT+DEL during journal playback, the system stops the playback, unhooks the journal playback procedure, and posts a [WM_CANCELJOURNAL](wm-canceljournal.md) message to the journaling application.</span></span>

<span data-ttu-id="36c60-157">如果攔截程式傳回 **WM_KEYLAST** 範圍 **WM_KEYFIRST** 中的訊息，則適用下列條件：</span><span class="sxs-lookup"><span data-stu-id="36c60-157">If the hook procedure returns a message in the range **WM_KEYFIRST** to **WM_KEYLAST**, the following conditions apply:</span></span>

* <span data-ttu-id="36c60-158">**EVENTMSG** 結構的 **paramL** 成員會指定已按下之索引鍵的虛擬按鍵碼。</span><span class="sxs-lookup"><span data-stu-id="36c60-158">The **paramL** member of the **EVENTMSG** structure specifies the virtual key code of the key that was pressed.</span></span>
* <span data-ttu-id="36c60-159">**EVENTMSG** 結構的 **paramH** 成員會指定掃描程式碼。</span><span class="sxs-lookup"><span data-stu-id="36c60-159">The **paramH** member of the **EVENTMSG** structure specifies the scan code.</span></span>
* <span data-ttu-id="36c60-160">沒有任何方法可以指定重複計數。</span><span class="sxs-lookup"><span data-stu-id="36c60-160">There's no way to specify a repeat count.</span></span>
<span data-ttu-id="36c60-161">事件一律會用來代表一個關鍵事件。</span><span class="sxs-lookup"><span data-stu-id="36c60-161">The event is always taken to represent one key event.</span></span>

## <a name="see-also"></a><span data-ttu-id="36c60-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36c60-162">See also</span></span>

[<span data-ttu-id="36c60-163">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="36c60-163">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="36c60-164">EVENTMSG</span><span class="sxs-lookup"><span data-stu-id="36c60-164">EVENTMSG</span></span>](/windows/desktop/api/winuser/ns-winuser-eventmsg)

[<span data-ttu-id="36c60-165">JournalRecordProc</span><span class="sxs-lookup"><span data-stu-id="36c60-165">JournalRecordProc</span></span>](journalrecordproc.md)

[<span data-ttu-id="36c60-166">PeekMessage</span><span class="sxs-lookup"><span data-stu-id="36c60-166">PeekMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[<span data-ttu-id="36c60-167">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="36c60-167">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="36c60-168">WM_CANCELJOURNAL</span><span class="sxs-lookup"><span data-stu-id="36c60-168">WM_CANCELJOURNAL</span></span>](wm-canceljournal.md)

[<span data-ttu-id="36c60-169">鉤</span><span class="sxs-lookup"><span data-stu-id="36c60-169">Hooks</span></span>](hooks.md)

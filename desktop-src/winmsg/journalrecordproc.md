---
UID: ''
title: JournalRecordProc 回呼函式
description: 此函數會記錄系統從系統訊息佇列中移除的訊息。
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
ms.openlocfilehash: bc255441ca82c86542dd8dd4729564122df6c719
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/11/2020
ms.locfileid: "103933033"
---
# <a name="journalrecordproc-function"></a><span data-ttu-id="710f1-103">JournalRecordProc 函式</span><span class="sxs-lookup"><span data-stu-id="710f1-103">JournalRecordProc function</span></span>

## <a name="description"></a><span data-ttu-id="710f1-104">Description</span><span class="sxs-lookup"><span data-stu-id="710f1-104">Description</span></span>

<span data-ttu-id="710f1-105">搭配 [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) 函式使用的應用程式定義或程式庫定義的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="710f1-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="710f1-106">此函數會記錄系統從系統訊息佇列中移除的訊息。</span><span class="sxs-lookup"><span data-stu-id="710f1-106">The function records messages the system removes from the system message queue.</span></span>
<span data-ttu-id="710f1-107">之後，應用程式可以使用 [JournalPlaybackProc](journalplaybackproc.md) 勾點來播放訊息。</span><span class="sxs-lookup"><span data-stu-id="710f1-107">Later, an application can use a [JournalPlaybackProc](journalplaybackproc.md) hook procedure to play back the messages.</span></span>

<span data-ttu-id="710f1-108">**HOOKPROC** 型別定義此回呼函數的指標。</span><span class="sxs-lookup"><span data-stu-id="710f1-108">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="710f1-109">**JournalRecordProc** 是應用程式定義或程式庫定義函數名稱的預留位置。</span><span class="sxs-lookup"><span data-stu-id="710f1-109">**JournalRecordProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK JournalRecordProc(
  _In_ int    code,
       WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="710f1-110">參數</span><span class="sxs-lookup"><span data-stu-id="710f1-110">Parameters</span></span>

### <a name="code-in"></a><span data-ttu-id="710f1-111">程式碼 [in]</span><span class="sxs-lookup"><span data-stu-id="710f1-111">code [in]</span></span>

<span data-ttu-id="710f1-112">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="710f1-112">Type: **int**</span></span>

<span data-ttu-id="710f1-113">指定如何處理訊息。</span><span class="sxs-lookup"><span data-stu-id="710f1-113">Specifies how to process the message.</span></span>
<span data-ttu-id="710f1-114">如果程式 *代碼* 小於零，則攔截程式必須將訊息傳遞至 [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) 函式，而不需要進一步處理，並且應該傳回 **CallNextHookEx** 所傳回的值。</span><span class="sxs-lookup"><span data-stu-id="710f1-114">If *code* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="710f1-115">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="710f1-115">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="710f1-116">值</span><span class="sxs-lookup"><span data-stu-id="710f1-116">Value</span></span> | <span data-ttu-id="710f1-117">意義</span><span class="sxs-lookup"><span data-stu-id="710f1-117">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="710f1-118">**HC_ACTION** 0</span><span class="sxs-lookup"><span data-stu-id="710f1-118">**HC_ACTION** 0</span></span> | <span data-ttu-id="710f1-119">*LParam* 參數是 [EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg)結構的指標，其中包含從系統佇列移除之訊息的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="710f1-119">The *lParam* parameter is a pointer to an [EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg) structure containing information about a message removed from the system queue.</span></span> <span data-ttu-id="710f1-120">攔截程式必須將結構的內容複寫到緩衝區或檔案來記錄。</span><span class="sxs-lookup"><span data-stu-id="710f1-120">The hook procedure must record the contents of the structure by copying them to a buffer or file.</span></span> |
| <span data-ttu-id="710f1-121">**HC_SYSMODALOFF** 5</span><span class="sxs-lookup"><span data-stu-id="710f1-121">**HC_SYSMODALOFF** 5</span></span> | <span data-ttu-id="710f1-122">系統強制回應對話方塊已損毀。</span><span class="sxs-lookup"><span data-stu-id="710f1-122">A system-modal dialog box has been destroyed.</span></span> <span data-ttu-id="710f1-123">攔截程式必須繼續錄製。</span><span class="sxs-lookup"><span data-stu-id="710f1-123">The hook procedure must resume recording.</span></span> |
| <span data-ttu-id="710f1-124">**HC_SYSMODALON** 4</span><span class="sxs-lookup"><span data-stu-id="710f1-124">**HC_SYSMODALON** 4</span></span> | <span data-ttu-id="710f1-125">系統強制回應對話方塊隨即顯示。</span><span class="sxs-lookup"><span data-stu-id="710f1-125">A system-modal dialog box is being displayed.</span></span> <span data-ttu-id="710f1-126">在對話方塊損毀之前，攔截程式必須停止錄製。</span><span class="sxs-lookup"><span data-stu-id="710f1-126">Until the dialog box is destroyed, the hook procedure must stop recording.</span></span> |

### <a name="wparam"></a><span data-ttu-id="710f1-127">wParam</span><span class="sxs-lookup"><span data-stu-id="710f1-127">wParam</span></span>

<span data-ttu-id="710f1-128">類型： **WPARAM**</span><span class="sxs-lookup"><span data-stu-id="710f1-128">Type: **WPARAM**</span></span>

<span data-ttu-id="710f1-129">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="710f1-129">This parameter is not used.</span></span>

### <a name="lparam-in"></a><span data-ttu-id="710f1-130">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="710f1-130">lParam [in]</span></span>

<span data-ttu-id="710f1-131">類型： **LPARAM**</span><span class="sxs-lookup"><span data-stu-id="710f1-131">Type: **LPARAM**</span></span>

<span data-ttu-id="710f1-132">**EVENTMSG** 結構的指標，其中包含要記錄的訊息。</span><span class="sxs-lookup"><span data-stu-id="710f1-132">A pointer to an **EVENTMSG** structure that contains the message to be recorded.</span></span>

## <a name="returns"></a><span data-ttu-id="710f1-133">傳回</span><span class="sxs-lookup"><span data-stu-id="710f1-133">Returns</span></span>

<span data-ttu-id="710f1-134">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="710f1-134">Type: **LRESULT**</span></span>

<span data-ttu-id="710f1-135">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="710f1-135">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="710f1-136">備註</span><span class="sxs-lookup"><span data-stu-id="710f1-136">Remarks</span></span>

<span data-ttu-id="710f1-137">**JournalRecordProc** 勾點程式必須複製但不能修改訊息。</span><span class="sxs-lookup"><span data-stu-id="710f1-137">A **JournalRecordProc** hook procedure must copy but not modify the messages.</span></span>
<span data-ttu-id="710f1-138">當攔截程式將控制權傳回到系統之後，就會繼續處理訊息。</span><span class="sxs-lookup"><span data-stu-id="710f1-138">After the hook procedure returns control to the system, the message continues to be processed.</span></span>

<span data-ttu-id="710f1-139">在 **SetWindowsHookEx** 函式的呼叫中指定 [WH_JOURNALRECORD](about-hooks.md)類型和攔截程式指標，以安裝 **JournalRecordProc** 攔截程式。</span><span class="sxs-lookup"><span data-stu-id="710f1-139">Install the **JournalRecordProc** hook procedure by specifying the [WH_JOURNALRECORD](about-hooks.md) type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="710f1-140">**JournalRecordProc** 攔截程式不需要存留在動態連結程式庫中。</span><span class="sxs-lookup"><span data-stu-id="710f1-140">A **JournalRecordProc** hook procedure does not need to live in a dynamic-link library.</span></span>
<span data-ttu-id="710f1-141">**JournalRecordProc** 勾點程式可以存留在應用程式本身。</span><span class="sxs-lookup"><span data-stu-id="710f1-141">A **JournalRecordProc** hook procedure can live in the application itself.</span></span>

<span data-ttu-id="710f1-142">與大部分其他全域攔截程式不同的是， **JournalRecordProc** 和 [JournalPlaybackProc](journalplaybackproc.md) 攔截程式永遠會在設定攔截的執行緒內容中呼叫。</span><span class="sxs-lookup"><span data-stu-id="710f1-142">Unlike most other global hook procedures, the **JournalRecordProc** and [JournalPlaybackProc](journalplaybackproc.md) hook procedures are always called in the context of the thread that set the hook.</span></span>

<span data-ttu-id="710f1-143">已安裝 **JournalRecordProc** 攔截程式的應用程式應該會監看 [VK_CANCEL](/windows/desktop/inputdev/virtual-key-codes) 的虛擬機器碼 (，其實作為大部分鍵盤) 的 CTRL + BREAK 按鍵組合。</span><span class="sxs-lookup"><span data-stu-id="710f1-143">An application that has installed a **JournalRecordProc** hook procedure should watch for the [VK_CANCEL](/windows/desktop/inputdev/virtual-key-codes) virtual key code (which is implemented as the CTRL+BREAK key combination on most keyboards).</span></span>
<span data-ttu-id="710f1-144">應用程式應該將此虛擬金鑰程式碼解釋為使用者想要停止記錄的信號。</span><span class="sxs-lookup"><span data-stu-id="710f1-144">This virtual key code should be interpreted by the application as a signal that the user wishes to stop journal recording.</span></span>
<span data-ttu-id="710f1-145">應用程式應該藉由結束錄製順序和移除 **JournalRecordProc** 攔截程式來回應。</span><span class="sxs-lookup"><span data-stu-id="710f1-145">The application should respond by ending the recording sequence and removing the **JournalRecordProc** hook procedure.</span></span>
<span data-ttu-id="710f1-146">移除是很重要的。</span><span class="sxs-lookup"><span data-stu-id="710f1-146">Removal is important.</span></span>
<span data-ttu-id="710f1-147">它會防止日誌應用程式在攔截程式內停滯，而無法鎖定系統。</span><span class="sxs-lookup"><span data-stu-id="710f1-147">It prevents a journaling application from locking up the system by hanging inside a hook procedure.</span></span>

<span data-ttu-id="710f1-148">此角色是停止 journl 錄製的信號，表示 CTRL + BREAK 按鍵組合本身無法錄製。</span><span class="sxs-lookup"><span data-stu-id="710f1-148">This role as a signal to stop journl recording means that a CTRL+BREAK key combination cannot itself be recorded.</span></span>
<span data-ttu-id="710f1-149">由於 CTRL + C 按鍵組合沒有這類角色做為日誌通知，因此可以記錄。</span><span class="sxs-lookup"><span data-stu-id="710f1-149">Since the CTRL+C key combination has no such role as a journaling signal, it can be recorded.</span></span>
<span data-ttu-id="710f1-150">另外還有兩個無法錄製的按鍵組合： CTRL + ESC 和 CTRL + ALT + DEL。</span><span class="sxs-lookup"><span data-stu-id="710f1-150">There are two other key combinations that cannot be recorded: CTRL+ESC and CTRL+ALT+DEL.</span></span>
<span data-ttu-id="710f1-151">這兩個按鍵組合會導致系統停止所有的記錄活動， (記錄或播放) 、移除所有日誌勾點，並將 [WM_CANCELJOURNAL](wm-canceljournal.md) 訊息張貼至日誌應用程式。</span><span class="sxs-lookup"><span data-stu-id="710f1-151">Those two key combinations cause the system to stop all journaling activities (record or playback), remove all journaling hooks, and post a [WM_CANCELJOURNAL](wm-canceljournal.md) message to the journaling application.</span></span>

## <a name="see-also"></a><span data-ttu-id="710f1-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="710f1-152">See also</span></span>

[<span data-ttu-id="710f1-153">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="710f1-153">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="710f1-154">EVENTMSG</span><span class="sxs-lookup"><span data-stu-id="710f1-154">EVENTMSG</span></span>](/windows/desktop/api/winuser/ns-winuser-eventmsg)

[<span data-ttu-id="710f1-155">JournalPlaybackProc</span><span class="sxs-lookup"><span data-stu-id="710f1-155">JournalPlaybackProc</span></span>](journalplaybackproc.md)

[<span data-ttu-id="710f1-156">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="710f1-156">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="710f1-157">WM_CANCELJOURNAL</span><span class="sxs-lookup"><span data-stu-id="710f1-157">WM_CANCELJOURNAL</span></span>](wm-canceljournal.md)

[<span data-ttu-id="710f1-158">鉤</span><span class="sxs-lookup"><span data-stu-id="710f1-158">Hooks</span></span>](hooks.md)

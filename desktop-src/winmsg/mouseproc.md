---
UID: ''
title: MouseProc 回呼函式
description: 當應用程式呼叫訊息函式時，系統會呼叫此函式，而且會有要處理的滑鼠訊息。
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
ms.openlocfilehash: abdd74b5fed93e2c2ddbc8d037a657b779a62a05
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/11/2020
ms.locfileid: "106969697"
---
# <a name="mouseproc-function"></a><span data-ttu-id="89c4b-103">MouseProc 函式</span><span class="sxs-lookup"><span data-stu-id="89c4b-103">MouseProc function</span></span>

## <a name="description"></a><span data-ttu-id="89c4b-104">Description</span><span class="sxs-lookup"><span data-stu-id="89c4b-104">Description</span></span>

<span data-ttu-id="89c4b-105">搭配 [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) 函式使用的應用程式定義或程式庫定義的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="89c4b-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="89c4b-106">每當應用程式呼叫 [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) 或 [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) 函式，且有要處理的滑鼠訊息時，系統就會呼叫這個函式。</span><span class="sxs-lookup"><span data-stu-id="89c4b-106">The system calls this function whenever an application calls the [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) or [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) function and there is a mouse message to be processed.</span></span>

<span data-ttu-id="89c4b-107">**HOOKPROC** 型別定義此回呼函數的指標。</span><span class="sxs-lookup"><span data-stu-id="89c4b-107">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="89c4b-108">**MouseProc** 是應用程式定義或程式庫定義函數名稱的預留位置。</span><span class="sxs-lookup"><span data-stu-id="89c4b-108">**MouseProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK MouseProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="89c4b-109">參數</span><span class="sxs-lookup"><span data-stu-id="89c4b-109">Parameters</span></span>

### <a name="ncode-in"></a><span data-ttu-id="89c4b-110">nCode [in]</span><span class="sxs-lookup"><span data-stu-id="89c4b-110">nCode [in]</span></span>

<span data-ttu-id="89c4b-111">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="89c4b-111">Type: **int**</span></span>

<span data-ttu-id="89c4b-112">攔截程式用來判斷如何處理訊息的程式碼。</span><span class="sxs-lookup"><span data-stu-id="89c4b-112">A code that the hook procedure uses to determine how to process the message.</span></span>
<span data-ttu-id="89c4b-113">如果 *nCode* 小於零，則攔截程式必須將訊息傳遞至 [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) 函式，而不需要進一步處理，並且應該傳回 **CallNextHookEx** 所傳回的值。</span><span class="sxs-lookup"><span data-stu-id="89c4b-113">If *nCode* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="89c4b-114">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="89c4b-114">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="89c4b-115">值</span><span class="sxs-lookup"><span data-stu-id="89c4b-115">Value</span></span> | <span data-ttu-id="89c4b-116">意義</span><span class="sxs-lookup"><span data-stu-id="89c4b-116">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="89c4b-117">**HC_ACTION** 0</span><span class="sxs-lookup"><span data-stu-id="89c4b-117">**HC_ACTION** 0</span></span> | <span data-ttu-id="89c4b-118">*WParam* 和 *lParam* 參數包含滑鼠訊息的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="89c4b-118">The *wParam* and *lParam* parameters contain information about a mouse message.</span></span> |
| <span data-ttu-id="89c4b-119">**HC_NOREMOVE** 3</span><span class="sxs-lookup"><span data-stu-id="89c4b-119">**HC_NOREMOVE** 3</span></span> | <span data-ttu-id="89c4b-120">*WParam* 和 *lParam* 參數包含滑鼠訊息的相關資訊，而且滑鼠訊息尚未從訊息佇列中移除。</span><span class="sxs-lookup"><span data-stu-id="89c4b-120">The *wParam* and *lParam* parameters contain information about a mouse message, and the mouse message has not been removed from the message queue.</span></span> <span data-ttu-id="89c4b-121"> (名為 **PeekMessage** 函式的應用程式，並指定 **PM_NOREMOVE** 旗標。 ) </span><span class="sxs-lookup"><span data-stu-id="89c4b-121">(An application called the **PeekMessage** function, specifying the **PM_NOREMOVE** flag.)</span></span> |

### <a name="wparam-in"></a><span data-ttu-id="89c4b-122">wParam [in]</span><span class="sxs-lookup"><span data-stu-id="89c4b-122">wParam [in]</span></span>

<span data-ttu-id="89c4b-123">類型： **WPARAM**</span><span class="sxs-lookup"><span data-stu-id="89c4b-123">Type: **WPARAM**</span></span>

<span data-ttu-id="89c4b-124">滑鼠訊息的識別碼。</span><span class="sxs-lookup"><span data-stu-id="89c4b-124">The identifier of the mouse message.</span></span>

### <a name="lparam-in"></a><span data-ttu-id="89c4b-125">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="89c4b-125">lParam [in]</span></span>

<span data-ttu-id="89c4b-126">類型： **LPARAM**</span><span class="sxs-lookup"><span data-stu-id="89c4b-126">Type: **LPARAM**</span></span>

<span data-ttu-id="89c4b-127">[MOUSEHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-mousehookstruct)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="89c4b-127">A pointer to a [MOUSEHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-mousehookstruct) structure.</span></span>

## <a name="returns"></a><span data-ttu-id="89c4b-128">傳回</span><span class="sxs-lookup"><span data-stu-id="89c4b-128">Returns</span></span>

<span data-ttu-id="89c4b-129">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="89c4b-129">Type: **LRESULT**</span></span>

<span data-ttu-id="89c4b-130">如果 *nCode* 小於零，則攔截程式必須傳回 **CallNextHookEx** 所傳回的值。</span><span class="sxs-lookup"><span data-stu-id="89c4b-130">If *nCode* is less than zero, the hook procedure must return the value returned by **CallNextHookEx**.</span></span>

<span data-ttu-id="89c4b-131">如果 *nCode* 大於或等於零，且攔截程式未處理訊息，強烈建議您呼叫 **CallNextHookEx** 並傳回傳回的值;否則，已安裝 [WH_MOUSE](about-hooks.md) 勾點的其他應用程式將不會收到攔截通知，而且可能會導致不正確的行為。</span><span class="sxs-lookup"><span data-stu-id="89c4b-131">If *nCode* is greater than or equal to zero, and the hook procedure did not process the message, it is highly recommended that you call **CallNextHookEx** and return the value it returns; otherwise, other applications that have installed [WH_MOUSE](about-hooks.md) hooks will not receive hook notifications and may behave incorrectly as a result.</span></span>
<span data-ttu-id="89c4b-132">如果攔截程式處理訊息，它可能會傳回非零值，以防止系統將訊息傳遞至目標視窗程式。</span><span class="sxs-lookup"><span data-stu-id="89c4b-132">If the hook procedure processed the message, it may return a nonzero value to prevent the system from passing the message to the target window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="89c4b-133">備註</span><span class="sxs-lookup"><span data-stu-id="89c4b-133">Remarks</span></span>

<span data-ttu-id="89c4b-134">應用程式會在 **SetWindowsHookEx** 函式的呼叫中指定 WH_MOUSE 攔截類型和攔截程式指標，以安裝攔截程式。</span><span class="sxs-lookup"><span data-stu-id="89c4b-134">An application installs the hook procedure by specifying the WH_MOUSE hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="89c4b-135">攔截程式不得安裝 [WH_JOURNALPLAYBACK](about-hooks.md) 回呼函數。</span><span class="sxs-lookup"><span data-stu-id="89c4b-135">The hook procedure must not install a [WH_JOURNALPLAYBACK](about-hooks.md) callback function.</span></span>

<span data-ttu-id="89c4b-136">此攔截可能會在其安裝所在的執行緒內容中呼叫。</span><span class="sxs-lookup"><span data-stu-id="89c4b-136">This hook may be called in the context of the thread that installed it.</span></span>
<span data-ttu-id="89c4b-137">呼叫是藉由將訊息傳送至已安裝攔截器的執行緒進行。</span><span class="sxs-lookup"><span data-stu-id="89c4b-137">The call is made by sending a message to the thread that installed the hook.</span></span>
<span data-ttu-id="89c4b-138">因此，安裝攔截的執行緒必須有訊息迴圈。</span><span class="sxs-lookup"><span data-stu-id="89c4b-138">Therefore, the thread that installed the hook must have a message loop.</span></span>

## <a name="see-also"></a><span data-ttu-id="89c4b-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="89c4b-139">See also</span></span>

[<span data-ttu-id="89c4b-140">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="89c4b-140">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="89c4b-141">GetMessage</span><span class="sxs-lookup"><span data-stu-id="89c4b-141">GetMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-getmessage)

[<span data-ttu-id="89c4b-142">MOUSEHOOKSTRUCT</span><span class="sxs-lookup"><span data-stu-id="89c4b-142">MOUSEHOOKSTRUCT</span></span>](/windows/desktop/api/winuser/ns-winuser-mousehookstruct)

[<span data-ttu-id="89c4b-143">PeekMessage</span><span class="sxs-lookup"><span data-stu-id="89c4b-143">PeekMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[<span data-ttu-id="89c4b-144">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="89c4b-144">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="89c4b-145">鉤</span><span class="sxs-lookup"><span data-stu-id="89c4b-145">Hooks</span></span>](hooks.md)

[<span data-ttu-id="89c4b-146">關於勾點</span><span class="sxs-lookup"><span data-stu-id="89c4b-146">About Hooks</span></span>](about-hooks.md)

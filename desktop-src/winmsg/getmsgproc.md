---
UID: ''
title: GetMsgProc 回呼函式
description: 當訊息函式從應用程式訊息佇列取得訊息時，系統會呼叫此函數。
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
ms.openlocfilehash: aa055e4184cdc9be5bb60a421ad5937bbfd15393
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "106966595"
---
# <a name="getmsgproc-function"></a><span data-ttu-id="3204c-103">GetMsgProc 函式</span><span class="sxs-lookup"><span data-stu-id="3204c-103">GetMsgProc function</span></span>

## <a name="-description"></a><span data-ttu-id="3204c-104">-description</span><span class="sxs-lookup"><span data-stu-id="3204c-104">-description</span></span>

<span data-ttu-id="3204c-105">搭配 [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) 函式使用的應用程式定義或程式庫定義的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="3204c-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span> <span data-ttu-id="3204c-106">每當 [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) 或 [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) 函式從應用程式訊息佇列抓取訊息時，系統就會呼叫這個函式。</span><span class="sxs-lookup"><span data-stu-id="3204c-106">The system calls this function whenever the [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) or [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) function has retrieved a message from an application message queue.</span></span>
<span data-ttu-id="3204c-107">將抓取的訊息傳回給呼叫者之前，系統會將訊息傳遞至攔截程式。</span><span class="sxs-lookup"><span data-stu-id="3204c-107">Before returning the retrieved message to the caller, the system passes the message to the hook procedure.</span></span>

<span data-ttu-id="3204c-108">**HOOKPROC** 型別定義此回呼函數的指標。</span><span class="sxs-lookup"><span data-stu-id="3204c-108">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="3204c-109">**GetMsgProc** 是應用程式定義或程式庫定義函數名稱的預留位置。</span><span class="sxs-lookup"><span data-stu-id="3204c-109">**GetMsgProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK GetMsgProc(
  _In_ int    code,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="-parameters"></a><span data-ttu-id="3204c-110">-參數</span><span class="sxs-lookup"><span data-stu-id="3204c-110">-parameters</span></span>

### <a name="code-in"></a><span data-ttu-id="3204c-111">程式碼 [in]</span><span class="sxs-lookup"><span data-stu-id="3204c-111">code [in]</span></span>

<span data-ttu-id="3204c-112">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="3204c-112">Type: **int**</span></span>

<span data-ttu-id="3204c-113">指定攔截程式是否必須處理訊息。</span><span class="sxs-lookup"><span data-stu-id="3204c-113">Specifies whether the hook procedure must process the message.</span></span>
<span data-ttu-id="3204c-114">如果 **HC_ACTION** 程式 *代碼*，則攔截程式必須處理訊息。</span><span class="sxs-lookup"><span data-stu-id="3204c-114">If *code* is **HC_ACTION**, the hook procedure must process the message.</span></span>
<span data-ttu-id="3204c-115">如果程式 *代碼* 小於零，則攔截程式必須將訊息傳遞至 [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) 函式，而不需要進一步處理，並且應該傳回 **CallNextHookEx** 所傳回的值。</span><span class="sxs-lookup"><span data-stu-id="3204c-115">If *code* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>

### <a name="wparam-in"></a><span data-ttu-id="3204c-116">wParam [in]</span><span class="sxs-lookup"><span data-stu-id="3204c-116">wParam [in]</span></span>

<span data-ttu-id="3204c-117">類型： **WPARAM**</span><span class="sxs-lookup"><span data-stu-id="3204c-117">Type: **WPARAM**</span></span>

<span data-ttu-id="3204c-118">指定是否已從佇列中移除訊息。</span><span class="sxs-lookup"><span data-stu-id="3204c-118">Specifies whether the message has been removed from the queue.</span></span>
<span data-ttu-id="3204c-119">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="3204c-119">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="3204c-120">值</span><span class="sxs-lookup"><span data-stu-id="3204c-120">Value</span></span> | <span data-ttu-id="3204c-121">意義</span><span class="sxs-lookup"><span data-stu-id="3204c-121">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="3204c-122">**PM_NOREMOVE** 0x0000</span><span class="sxs-lookup"><span data-stu-id="3204c-122">**PM_NOREMOVE** 0x0000</span></span> | <span data-ttu-id="3204c-123">尚未從佇列中移除訊息。</span><span class="sxs-lookup"><span data-stu-id="3204c-123">The message has not been removed from the queue.</span></span> <span data-ttu-id="3204c-124"> (名為 **PeekMessage** 函式的應用程式，並指定 **PM_NOREMOVE** 旗標。 ) </span><span class="sxs-lookup"><span data-stu-id="3204c-124">(An application called the **PeekMessage** function, specifying the **PM_NOREMOVE** flag.)</span></span> |
| <span data-ttu-id="3204c-125">**PM_REMOVE** 0x0001</span><span class="sxs-lookup"><span data-stu-id="3204c-125">**PM_REMOVE** 0x0001</span></span> | <span data-ttu-id="3204c-126">已從佇列中移除訊息。</span><span class="sxs-lookup"><span data-stu-id="3204c-126">The message has been removed from the queue.</span></span> <span data-ttu-id="3204c-127"> (名為 **GetMessage** 的應用程式，或指定 **PM_REMOVE** 旗標的應用程式，稱為 **PeekMessage** 函數。 ) </span><span class="sxs-lookup"><span data-stu-id="3204c-127">(An application called **GetMessage**, or it called the  **PeekMessage** function, specifying the **PM_REMOVE** flag.)</span></span>|

### <a name="lparam-in"></a><span data-ttu-id="3204c-128">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="3204c-128">lParam [in]</span></span>

<span data-ttu-id="3204c-129">類型： **LPARAM**</span><span class="sxs-lookup"><span data-stu-id="3204c-129">Type: **LPARAM**</span></span>

<span data-ttu-id="3204c-130">訊息 [結構的](/windows/desktop/api/winuser/ns-winuser-msg) 指標，其中包含有關訊息的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3204c-130">A pointer to an [MSG](/windows/desktop/api/winuser/ns-winuser-msg) structure that contains details about the message.</span></span>

## <a name="-returns"></a><span data-ttu-id="3204c-131">-傳回</span><span class="sxs-lookup"><span data-stu-id="3204c-131">-returns</span></span>

<span data-ttu-id="3204c-132">如果程式 *代碼* 小於零，則攔截程式必須傳回 [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)傳回的值。</span><span class="sxs-lookup"><span data-stu-id="3204c-132">If *code* is less than zero, the hook procedure must return the value returned by [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex).</span></span>

<span data-ttu-id="3204c-133">如果程式 *代碼* 大於或等於零，強烈建議您呼叫 **CallNextHookEx** 並傳回傳回的值;否則，已安裝 [WH_GETMESSAGE](about-hooks.md) 勾點的其他應用程式將不會收到攔截通知，而且可能會導致不正確的行為。</span><span class="sxs-lookup"><span data-stu-id="3204c-133">If *code* is greater than or equal to zero, it is highly recommended that you call **CallNextHookEx** and return the value it returns; otherwise, other applications that have installed [WH_GETMESSAGE](about-hooks.md) hooks will not receive hook notifications and may behave incorrectly as a result.</span></span>
<span data-ttu-id="3204c-134">如果攔截程式未呼叫 **CallNextHookEx**，則傳回值應該為零。</span><span class="sxs-lookup"><span data-stu-id="3204c-134">If the hook procedure does not call **CallNextHookEx**, the return value should be zero.</span></span>

## <a name="-remarks"></a><span data-ttu-id="3204c-135">-備註</span><span class="sxs-lookup"><span data-stu-id="3204c-135">-remarks</span></span>

<span data-ttu-id="3204c-136">**GetMsgProc** 攔截程式可以檢查或修改訊息。</span><span class="sxs-lookup"><span data-stu-id="3204c-136">The **GetMsgProc** hook procedure can examine or modify the message.</span></span>
<span data-ttu-id="3204c-137">在攔截程式將控制權傳回給系統之後， **GetMessage** 或 **PeekMessage** 函式會將訊息連同任何修改傳回給原本呼叫它的應用程式。</span><span class="sxs-lookup"><span data-stu-id="3204c-137">After the hook procedure returns control to the system, the **GetMessage** or **PeekMessage** function returns the message, along with any modifications, to the application that originally called it.</span></span>

<span data-ttu-id="3204c-138">應用程式會藉由在 **SetWindowsHookEx** 函式的呼叫中指定 **WH_GETMESSAGE** 攔截類型和攔截程式的指標，來安裝此攔截程式。</span><span class="sxs-lookup"><span data-stu-id="3204c-138">An application installs this hook procedure by specifying the **WH_GETMESSAGE** hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

## <a name="see-also"></a><span data-ttu-id="3204c-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3204c-139">See also</span></span>

[<span data-ttu-id="3204c-140">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="3204c-140">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="3204c-141">GetMessage</span><span class="sxs-lookup"><span data-stu-id="3204c-141">GetMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-getmessage)

[<span data-ttu-id="3204c-142">味精</span><span class="sxs-lookup"><span data-stu-id="3204c-142">MSG</span></span>](/windows/desktop/api/winuser/ns-winuser-msg)

[<span data-ttu-id="3204c-143">PeekMessage</span><span class="sxs-lookup"><span data-stu-id="3204c-143">PeekMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[<span data-ttu-id="3204c-144">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="3204c-144">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="3204c-145">鉤</span><span class="sxs-lookup"><span data-stu-id="3204c-145">Hooks</span></span>](hooks.md)

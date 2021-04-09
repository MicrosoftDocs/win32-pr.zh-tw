---
description: 進程可以監視通訊資源中發生的一組事件。 例如，應用程式可以使用事件監視來判斷 CTS (清除傳送) 和 DSR (資料集就緒) 發出變更狀態。
ms.assetid: 5d2a7bf3-a972-474b-b8ca-da3351f1e59c
title: 通訊事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 466bd5076405427c7c348c1df3706cb7b5c3edc4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110704"
---
# <a name="communications-events"></a><span data-ttu-id="3ee3b-104">通訊事件</span><span class="sxs-lookup"><span data-stu-id="3ee3b-104">Communications Events</span></span>

<span data-ttu-id="3ee3b-105">進程可以監視通訊資源中發生的一組事件。</span><span class="sxs-lookup"><span data-stu-id="3ee3b-105">A process can monitor a set of events that occur in a communications resource.</span></span> <span data-ttu-id="3ee3b-106">例如，應用程式可以使用事件監視來判斷 CTS (清除傳送) 和 DSR (資料集就緒) 發出變更狀態。</span><span class="sxs-lookup"><span data-stu-id="3ee3b-106">For example, an application can use event monitoring to determine when the CTS (clear-to-send) and DSR (data-set-ready) signals change state.</span></span>

<span data-ttu-id="3ee3b-107">進程可以使用 [**SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask) 函式來建立事件遮罩，以監視指定通訊資源上的事件。</span><span class="sxs-lookup"><span data-stu-id="3ee3b-107">A process can monitor events on a given communications resource by using the [**SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask) function to create an event mask.</span></span> <span data-ttu-id="3ee3b-108">若要判斷通訊資源的目前事件遮罩，處理常式可以使用 [**GetCommMask**](/windows/desktop/api/Winbase/nf-winbase-getcommmask) 函數。</span><span class="sxs-lookup"><span data-stu-id="3ee3b-108">To determine the current event mask for a communications resource, a process can use the [**GetCommMask**](/windows/desktop/api/Winbase/nf-winbase-getcommmask) function.</span></span> <span data-ttu-id="3ee3b-109">下列值會指定可以監視的事件。</span><span class="sxs-lookup"><span data-stu-id="3ee3b-109">The following values specify events that can be monitored.</span></span>



| <span data-ttu-id="3ee3b-110">值</span><span class="sxs-lookup"><span data-stu-id="3ee3b-110">Value</span></span>           | <span data-ttu-id="3ee3b-111">意義</span><span class="sxs-lookup"><span data-stu-id="3ee3b-111">Meaning</span></span>                                                                                                                                                                                                                                           |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ee3b-112">**EV \_ 中斷**</span><span class="sxs-lookup"><span data-stu-id="3ee3b-112">**EV\_BREAK**</span></span>   | <span data-ttu-id="3ee3b-113">在輸入時偵測到中斷。</span><span class="sxs-lookup"><span data-stu-id="3ee3b-113">A break was detected on input.</span></span>                                                                                                                                                                                                                    |
| <span data-ttu-id="3ee3b-114">**EV \_ CTS**</span><span class="sxs-lookup"><span data-stu-id="3ee3b-114">**EV\_CTS**</span></span>     | <span data-ttu-id="3ee3b-115">CTS (清除傳送) 信號變更狀態。</span><span class="sxs-lookup"><span data-stu-id="3ee3b-115">The CTS (clear-to-send) signal changed state.</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="3ee3b-116">**EV \_ DSR**</span><span class="sxs-lookup"><span data-stu-id="3ee3b-116">**EV\_DSR**</span></span>     | <span data-ttu-id="3ee3b-117">DSR (資料集就緒) 信號已變更狀態。</span><span class="sxs-lookup"><span data-stu-id="3ee3b-117">The DSR (data-set-ready) signal changed state.</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="3ee3b-118">**EV \_ ERR**</span><span class="sxs-lookup"><span data-stu-id="3ee3b-118">**EV\_ERR**</span></span>     | <span data-ttu-id="3ee3b-119">發生行狀態錯誤。</span><span class="sxs-lookup"><span data-stu-id="3ee3b-119">A line-status error occurred.</span></span> <span data-ttu-id="3ee3b-120">行狀態錯誤為 **ce \_ 框架**、 **ce \_ 溢出** 和 **ce \_ RXPARITY**。</span><span class="sxs-lookup"><span data-stu-id="3ee3b-120">Line-status errors are **CE\_FRAME**, **CE\_OVERRUN**, and **CE\_RXPARITY**.</span></span>                                                                                                                                        |
| <span data-ttu-id="3ee3b-121">**EV \_ 環形**</span><span class="sxs-lookup"><span data-stu-id="3ee3b-121">**EV\_RING**</span></span>    | <span data-ttu-id="3ee3b-122">偵測到鈴聲指示器 (Indicator)。</span><span class="sxs-lookup"><span data-stu-id="3ee3b-122">A ring indicator was detected.</span></span>                                                                                                                                                                                                                    |
| <span data-ttu-id="3ee3b-123">**EV \_ RLSD**</span><span class="sxs-lookup"><span data-stu-id="3ee3b-123">**EV\_RLSD**</span></span>    | <span data-ttu-id="3ee3b-124">RLSD (接收行信號偵測) 信號已變更狀態。</span><span class="sxs-lookup"><span data-stu-id="3ee3b-124">The RLSD (receive-line-signal-detect) signal changed state.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="3ee3b-125">**EV \_ RXCHAR**</span><span class="sxs-lookup"><span data-stu-id="3ee3b-125">**EV\_RXCHAR**</span></span>  | <span data-ttu-id="3ee3b-126">會接收字元並放到輸入緩衝區。</span><span class="sxs-lookup"><span data-stu-id="3ee3b-126">A character was received and placed in the input buffer.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="3ee3b-127">**EV \_ RXFLAG**</span><span class="sxs-lookup"><span data-stu-id="3ee3b-127">**EV\_RXFLAG**</span></span>  | <span data-ttu-id="3ee3b-128">已收到事件字元，並將其放在輸入緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="3ee3b-128">The event character was received and placed in the input buffer.</span></span> <span data-ttu-id="3ee3b-129">事件字元是在裝置的 [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) 結構中指定的，此結構會使用 [**SetCommState**](/windows/desktop/api/Winbase/nf-winbase-setcommstate) 函數套用至序列埠。</span><span class="sxs-lookup"><span data-stu-id="3ee3b-129">The event character is specified in the device's [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) structure, which is applied to a serial port by using the [**SetCommState**](/windows/desktop/api/Winbase/nf-winbase-setcommstate) function.</span></span> |
| <span data-ttu-id="3ee3b-130">**EV \_ TXEMPTY**</span><span class="sxs-lookup"><span data-stu-id="3ee3b-130">**EV\_TXEMPTY**</span></span> | <span data-ttu-id="3ee3b-131">輸出緩衝區中的最後一個字元已傳送。</span><span class="sxs-lookup"><span data-stu-id="3ee3b-131">The last character in the output buffer was sent.</span></span>                                                                                                                                                                                                 |



 

<span data-ttu-id="3ee3b-132">在指定一組事件之後，進程會使用 [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) 函數來等候其中一個事件發生。</span><span class="sxs-lookup"><span data-stu-id="3ee3b-132">After a set of events is specified, a process uses the [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) function to wait for one of the events to occur.</span></span> <span data-ttu-id="3ee3b-133">**WaitCommEvent** 可以同步使用，或做為重迭的作業。</span><span class="sxs-lookup"><span data-stu-id="3ee3b-133">**WaitCommEvent** can be used synchronously or as an overlapped operation.</span></span> <span data-ttu-id="3ee3b-134">如需以重迭作業的形式執行函數的詳細資訊，請參閱 [同步](/windows/desktop/Sync/synchronization)處理。</span><span class="sxs-lookup"><span data-stu-id="3ee3b-134">For additional information about executing a function as an overlapped operation, see [Synchronization](/windows/desktop/Sync/synchronization).</span></span>

<span data-ttu-id="3ee3b-135">當事件遮罩中指定的其中一個事件發生時，程式會完成等候作業，並設定事件遮罩變數來指出偵測到的事件種類。</span><span class="sxs-lookup"><span data-stu-id="3ee3b-135">When one of the events specified in the event mask occurs, the process completes the wait operation and sets an event mask variable to indicate the type of event detected.</span></span> <span data-ttu-id="3ee3b-136">如果針對通訊資源呼叫 [**SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask) ，但該資源的等候暫止，則 [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="3ee3b-136">If the [**SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask) is called for a communications resource while a wait is pending for that resource, [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) returns an error.</span></span>

<span data-ttu-id="3ee3b-137">[**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent)函式會偵測自上一次呼叫 [**SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask)或 **WaitCommEvent** 之後發生的事件。</span><span class="sxs-lookup"><span data-stu-id="3ee3b-137">The [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) function detects events that have occurred since the last call to [**SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask) or **WaitCommEvent**.</span></span> <span data-ttu-id="3ee3b-138">例如，如果您將 **EV \_ RXCHAR** 事件指定為等待滿足的事件，當驅動程式輸入緩衝區中的字元自上一次呼叫 **WaitCommEvent** 或 **SetCommMask** 之後，就會滿足 **WaitCommEvent** 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="3ee3b-138">For example, if you specify the **EV\_RXCHAR** event as a wait-satisfying event, a call to **WaitCommEvent** will be satisfied if there are characters in the driver's input buffer that have arrived since the last call to **WaitCommEvent** or **SetCommMask**.</span></span> <span data-ttu-id="3ee3b-139">因此，假設有下列的虛擬化，在 T1 和 T2 之間收到的任何字元都會滿足下一次的 **WaitCommEvent** 呼叫。</span><span class="sxs-lookup"><span data-stu-id="3ee3b-139">Thus, given the following pseudocode, any characters received between T1 and T2 will satisfy the next call to **WaitCommEvent**.</span></span>


```C++
while (!bFinished) 
{ 
    WaitCommEvent(args)
 
T1: // Read bytes 
    // Process bytes 

T2: 
}
```



<span data-ttu-id="3ee3b-140">當您監視當信號 (CTS、DSR 等) 變更狀態時所發生的事件時， [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) 會回報變更，但不會報告目前的狀態。</span><span class="sxs-lookup"><span data-stu-id="3ee3b-140">When monitoring an event that occurs when a signal (CTS, DSR, and so on) changes state, [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) reports the change, but not the current state.</span></span> <span data-ttu-id="3ee3b-141">若要查詢 CTS 的目前狀態 (清除傳送) 、DSR (資料準備就緒) 、RLSD (接收行信號偵測) 和環形指標信號，處理常式可以使用 [**GetCommModemStatus**](/windows/desktop/api/Winbase/nf-winbase-getcommmodemstatus) 函式。</span><span class="sxs-lookup"><span data-stu-id="3ee3b-141">To query the current state of the CTS (clear-to-send), DSR (data-set-ready), RLSD (receive-line-signal-detect), and ring indicator signals, a process can use the [**GetCommModemStatus**](/windows/desktop/api/Winbase/nf-winbase-getcommmodemstatus) function.</span></span>

 

 

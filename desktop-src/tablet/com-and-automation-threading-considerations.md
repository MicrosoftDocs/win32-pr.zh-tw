---
description: 當使用元件物件模型 (COM) 和自動化時，會指定下列 Tablet PC 執行緒考慮。
ms.assetid: cf8feba5-a391-4396-a5d8-1ef58df304a7
title: COM 和自動化執行緒考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afe0cf67d427ce89074a605f664e94f35d3d3eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971346"
---
# <a name="com-and-automation-threading-considerations"></a><span data-ttu-id="c5788-103">COM 和自動化執行緒考慮</span><span class="sxs-lookup"><span data-stu-id="c5788-103">COM and Automation Threading Considerations</span></span>

<span data-ttu-id="c5788-104">當使用元件物件模型 (COM) 和自動化時，會指定下列 Tablet PC 執行緒考慮。</span><span class="sxs-lookup"><span data-stu-id="c5788-104">The following Tablet PC threading considerations are specific to when Component Object Model (COM) and Automation are used.</span></span>

-   [<span data-ttu-id="c5788-105">執行緒安全性</span><span class="sxs-lookup"><span data-stu-id="c5788-105">Thread Safety</span></span>](#thread-safety)
-   [<span data-ttu-id="c5788-106">STA 和 MTA 應用程式</span><span class="sxs-lookup"><span data-stu-id="c5788-106">STA and MTA Applications</span></span>](#sta-and-mta-applications)
-   [<span data-ttu-id="c5788-107">InkCollector 和 InkOverlay</span><span class="sxs-lookup"><span data-stu-id="c5788-107">InkCollector and InkOverlay</span></span>](#inkcollector-and-inkoverlay)
-   [<span data-ttu-id="c5788-108">事件接收器</span><span class="sxs-lookup"><span data-stu-id="c5788-108">Event Sinks</span></span>](#event-sinks)
-   [<span data-ttu-id="c5788-109">事件處理常式內的例外狀況</span><span class="sxs-lookup"><span data-stu-id="c5788-109">Exceptions within Event Handlers</span></span>](#exceptions-within-event-handlers)
-   [<span data-ttu-id="c5788-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="c5788-110">Related topics</span></span>](#related-topics)

## <a name="thread-safety"></a><span data-ttu-id="c5788-111">執行緒安全性</span><span class="sxs-lookup"><span data-stu-id="c5788-111">Thread Safety</span></span>

<span data-ttu-id="c5788-112">除了 [InkPicture](inkpicture-control.md) 和 [InkEdit](inkedit-control.md) 控制項以外，Tablet PC 物件是安全線程，而且會標示為兩者。</span><span class="sxs-lookup"><span data-stu-id="c5788-112">Except for the [InkPicture](inkpicture-control.md) and [InkEdit](inkedit-control.md) controls, Tablet PC objects are thread-safe and are marked as both.</span></span> <span data-ttu-id="c5788-113">藉由標示為兩者，它們可以在單一執行緒的單元 (STA) 或多執行緒的單元 (MTA) 中執行。</span><span class="sxs-lookup"><span data-stu-id="c5788-113">By being marked as both, they can run in either a single threaded apartment (STA) or a multithreaded apartment (MTA).</span></span>

<span data-ttu-id="c5788-114">Windows form 使用 STA 模型，因為 windows form 是以原生 Win32 視窗為基礎，而原生 Win32 視窗原本就是單元執行緒。</span><span class="sxs-lookup"><span data-stu-id="c5788-114">Windows forms use the STA model because windows forms are based on native Win32 windows that are inherently apartment threaded.</span></span>

## <a name="sta-and-mta-applications"></a><span data-ttu-id="c5788-115">STA 和 MTA 應用程式</span><span class="sxs-lookup"><span data-stu-id="c5788-115">STA and MTA Applications</span></span>

<span data-ttu-id="c5788-116">如果您的應用程式在 MTA 中執行，或使用自由執行緒封送處理器 (FTM) ，您必須撰寫安全線程的程式碼;不過，藉由這麼做，您就可以改善某些事件處理效能問題。</span><span class="sxs-lookup"><span data-stu-id="c5788-116">If your application runs in an MTA or uses the free threaded marshaler (FTM), you must write thread-safe code; however, by doing so you can improve certain event handling performance issues.</span></span>

## <a name="inkcollector-and-inkoverlay"></a><span data-ttu-id="c5788-117">InkCollector 和 InkOverlay</span><span class="sxs-lookup"><span data-stu-id="c5788-117">InkCollector and InkOverlay</span></span>

<span data-ttu-id="c5788-118">您的應用程式不應該釋出其最終的 [**InkCollector**](inkcollector-class.md) 或 [**InkOverlay**](inkoverlay-class.md) 物件參考，因而直接從筆墨線程終結物件。</span><span class="sxs-lookup"><span data-stu-id="c5788-118">Your application should not release its final reference to the [**InkCollector**](inkcollector-class.md) or the [**InkOverlay**](inkoverlay-class.md) object, thus destroying the object, directly from the ink thread.</span></span> <span data-ttu-id="c5788-119">相反地，應用程式應該從應用程式執行緒釋放 **InkCollector** 或 **InkOverlay** 物件。</span><span class="sxs-lookup"><span data-stu-id="c5788-119">Instead, the application should release the **InkCollector** or the **InkOverlay** object from an application thread.</span></span>

<span data-ttu-id="c5788-120">**注意：** 標示為 MTA 或使用 FTM 的應用程式（允許從筆墨線程直接呼叫應用程式的公寓）可以直接從筆墨線程釋放其 [**InkCollector**](inkcollector-class.md) 或 [**InkOverlay**](inkoverlay-class.md) 物件的最終參考;不過，這會導致無法復原的應用程式失敗。</span><span class="sxs-lookup"><span data-stu-id="c5788-120">**Caution:** An application that is marked MTA or uses the FTM, which allows direct calls from the ink thread into the application's apartment, can release its final reference to the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object directly from the ink thread; however, this causes unrecoverable application failure.</span></span>

## <a name="event-sinks"></a><span data-ttu-id="c5788-121">事件接收器</span><span class="sxs-lookup"><span data-stu-id="c5788-121">Event Sinks</span></span>

<span data-ttu-id="c5788-122">如果您的應用程式未使用 FTM，而且在不同的單元中建立物件和其事件接收器，則事件會在服務事件接收器的執行緒上執行。</span><span class="sxs-lookup"><span data-stu-id="c5788-122">If your application is not using the FTM and an object and its event sink are created in different apartments, then the event executes on the thread servicing the event sink.</span></span>

## <a name="exceptions-within-event-handlers"></a><span data-ttu-id="c5788-123">事件處理常式內的例外狀況</span><span class="sxs-lookup"><span data-stu-id="c5788-123">Exceptions within Event Handlers</span></span>

<span data-ttu-id="c5788-124">從 Tablet PC 事件處理常式內擲回的例外狀況會取用，而其餘或您的應用程式看不到這些例外狀況。</span><span class="sxs-lookup"><span data-stu-id="c5788-124">Exceptions thrown from within Tablet PC event handlers are consumed and are not visible to the rest or your application.</span></span> <span data-ttu-id="c5788-125">同樣地，也不會從 Tablet PC 事件處理常式傳播 HRESULT 值。</span><span class="sxs-lookup"><span data-stu-id="c5788-125">Likewise, HRESULT values are not propagated from Tablet PC event handlers.</span></span> <span data-ttu-id="c5788-126">如果使用 COM 層的應用程式擲回例外狀況，背景執行緒就會終止，而例外狀況將會遺失。</span><span class="sxs-lookup"><span data-stu-id="c5788-126">If an application using the COM layer throws an exception, the background thread terminates, and the exception will be lost.</span></span> <span data-ttu-id="c5788-127">不會呼叫任何其他事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="c5788-127">No additional event handlers will be called.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c5788-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="c5788-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5788-129">C + + 事件接收器範例</span><span class="sxs-lookup"><span data-stu-id="c5788-129">C++ Event Sinks Sample</span></span>](c---event-sinks-sample.md)
</dt> <dt>

[<span data-ttu-id="c5788-130">一般執行緒考慮</span><span class="sxs-lookup"><span data-stu-id="c5788-130">General Threading Considerations</span></span>](general-threading-considerations.md)
</dt> <dt>

[<span data-ttu-id="c5788-131">Managed 程式庫執行緒考慮</span><span class="sxs-lookup"><span data-stu-id="c5788-131">Managed Library Threading Considerations</span></span>](managed-library-threading-considerations.md)
</dt> </dl>

 

 




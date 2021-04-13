---
description: 品質訊息
ms.assetid: ff98cb51-6300-470d-b696-5e27591c6b3f
title: 品質訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b290833be7550e255590a5bcda449ce19743c0b4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509993"
---
# <a name="quality-messages"></a><span data-ttu-id="e5e66-103">品質訊息</span><span class="sxs-lookup"><span data-stu-id="e5e66-103">Quality Messages</span></span>

<span data-ttu-id="e5e66-104">品質訊息是以 [**品質**](/windows/win32/api/strmif/ns-strmif-quality) 結構來定義。</span><span class="sxs-lookup"><span data-stu-id="e5e66-104">Quality messages are defined with the [**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure.</span></span> <span data-ttu-id="e5e66-105">此結構包含下列成員：</span><span class="sxs-lookup"><span data-stu-id="e5e66-105">This structure contains the following members:</span></span>

-   <span data-ttu-id="e5e66-106">**輸入：** 由 [**QualityMessageType**](/windows/win32/api/strmif/ne-strmif-qualitymessagetype) 列舉所定義;可能是 Famine，表示篩選接收太少資料或洪水，表示篩選器收到太多資料。</span><span class="sxs-lookup"><span data-stu-id="e5e66-106">**Type:** Defined by the [**QualityMessageType**](/windows/win32/api/strmif/ne-strmif-qualitymessagetype) enumeration; either Famine, indicating that the filter is receiving too little data, or Flood, indicating that the filter is receiving too much data.</span></span>
-   <span data-ttu-id="e5e66-107">**比例：** 從基準1000開始，資料速率中所要求的調整。</span><span class="sxs-lookup"><span data-stu-id="e5e66-107">**Proportion:** The requested adjustment in the data rate, from a baseline of 1000.</span></span> <span data-ttu-id="e5e66-108">例如，750表示75% 和1500表示150%。</span><span class="sxs-lookup"><span data-stu-id="e5e66-108">For example, 750 indicates 75% and 1500 indicates 150%.</span></span>
-   <span data-ttu-id="e5e66-109">**晚期：** 指出最近範例抵達的延遲時間的參考時間。</span><span class="sxs-lookup"><span data-stu-id="e5e66-109">**Late:** Reference time indicating how late the most recent sample arrived.</span></span> <span data-ttu-id="e5e66-110">如果範例提早抵達，此值會是負數。</span><span class="sxs-lookup"><span data-stu-id="e5e66-110">The value is negative if the sample arrived early.</span></span>
-   <span data-ttu-id="e5e66-111">**時間戳記：** 最新樣本上的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="e5e66-111">**TimeStamp:** The time stamp on the most recent sample.</span></span>

<span data-ttu-id="e5e66-112">例如，假設有時間戳記為240毫秒 (ms) 的範例會在280毫秒（資料流程時間）到達轉譯器。</span><span class="sxs-lookup"><span data-stu-id="e5e66-112">For example, suppose that a sample with a time stamp of 240 milliseconds (ms) reaches the renderer at 280 ms, stream time.</span></span> <span data-ttu-id="e5e66-113">轉譯器會建立 Famine 型別的品質訊息。</span><span class="sxs-lookup"><span data-stu-id="e5e66-113">The renderer creates a quality message of type Famine.</span></span> <span data-ttu-id="e5e66-114">此範例遲到了40毫秒，因此 **晚期** 成員是400000。</span><span class="sxs-lookup"><span data-stu-id="e5e66-114">The sample arrived 40 ms late, so the **Late** member is 400000.</span></span> <span data-ttu-id="e5e66-115"> (所有參考時間都是 100-毫微秒單位。 ) **時間戳記** 成員是2400000。</span><span class="sxs-lookup"><span data-stu-id="e5e66-115">(All reference times are in 100-nanosecond units.) The **TimeStamp** member is 2400000.</span></span>

<span data-ttu-id="e5e66-116">針對 **比例** 成員，轉譯器可能會使用執行中的平均值來計算值。</span><span class="sxs-lookup"><span data-stu-id="e5e66-116">For the **Proportion** member, the renderer might use a running average to calculate the value.</span></span> <span data-ttu-id="e5e66-117">也許範例已準時抵達，此範例是異常。</span><span class="sxs-lookup"><span data-stu-id="e5e66-117">Perhaps samples have been arriving on time, and this sample is an anomaly.</span></span> <span data-ttu-id="e5e66-118">在這種情況下，轉譯器可能只會要求小型更正。</span><span class="sxs-lookup"><span data-stu-id="e5e66-118">In that case the renderer might request only a small correction.</span></span> <span data-ttu-id="e5e66-119">另一方面，如果範例一直延遲，轉譯器可能會要求較大的修正。</span><span class="sxs-lookup"><span data-stu-id="e5e66-119">On the other hand, if samples are consistently late, the renderer might request a larger correction.</span></span>

<span data-ttu-id="e5e66-120">品質控制是透過 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) 介面處理。</span><span class="sxs-lookup"><span data-stu-id="e5e66-120">Quality control is handled through the [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) interface.</span></span> <span data-ttu-id="e5e66-121">它包含兩個方法。</span><span class="sxs-lookup"><span data-stu-id="e5e66-121">It contains two methods.</span></span>

-   <span data-ttu-id="e5e66-122">[**通知**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify)：傳送品質訊息。</span><span class="sxs-lookup"><span data-stu-id="e5e66-122">[**Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify): Sends a quality message.</span></span>
-   <span data-ttu-id="e5e66-123">[**SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink)：指定自訂品質管制員。</span><span class="sxs-lookup"><span data-stu-id="e5e66-123">[**SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink): Specifies a custom quality manager.</span></span>

<span data-ttu-id="e5e66-124">執行 **IQualityControl** 的物件會透過其 **通知** 方法接收品質訊息。</span><span class="sxs-lookup"><span data-stu-id="e5e66-124">An object that implements **IQualityControl** receives quality messages through its **Notify** method.</span></span> <span data-ttu-id="e5e66-125">它可以處理訊息或將訊息傳遞至另一個物件。</span><span class="sxs-lookup"><span data-stu-id="e5e66-125">It can either handle the message or pass the message to another object.</span></span> <span data-ttu-id="e5e66-126">如果應用程式呼叫物件的 **SetSink** 方法，則物件應該將品質控制項委派給指定的品質管制員。</span><span class="sxs-lookup"><span data-stu-id="e5e66-126">If the application calls the object's **SetSink** method, the object should delegate quality control to the specified quality manager.</span></span>

 

 




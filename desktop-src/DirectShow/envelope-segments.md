---
description: 信封區段
ms.assetid: 1b59cd1c-7c37-4c70-a36c-2ee1f42b42c5
title: 信封區段
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bac997667f52ef9bbf14760584889fa16cbbd04
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510070"
---
# <a name="envelope-segments"></a><span data-ttu-id="885df-103">信封區段</span><span class="sxs-lookup"><span data-stu-id="885df-103">Envelope Segments</span></span>

<span data-ttu-id="885df-104">參數曲線是由一或多個使用 [**MP \_ 信封 \_ 區段**](/previous-versions/windows/desktop/api/Medparam/ns-medparam-mp_envelope_segment) 結構所定義的信封區段所組成。</span><span class="sxs-lookup"><span data-stu-id="885df-104">A parameter curve consists of one or more envelope segments, defined using the [**MP\_ENVELOPE\_SEGMENT**](/previous-versions/windows/desktop/api/Medparam/ns-medparam-mp_envelope_segment) structure.</span></span> <span data-ttu-id="885df-105">此結構包含下列資訊：</span><span class="sxs-lookup"><span data-stu-id="885df-105">This structure contains the following information:</span></span>

-   <span data-ttu-id="885df-106">開始和結束時間。</span><span class="sxs-lookup"><span data-stu-id="885df-106">The start and end times.</span></span>
-   <span data-ttu-id="885df-107">開始和結束值。</span><span class="sxs-lookup"><span data-stu-id="885df-107">The starting and ending values.</span></span>
-   <span data-ttu-id="885df-108">曲線類型 (線性、正方形等) 。</span><span class="sxs-lookup"><span data-stu-id="885df-108">The curve type (linear, square, and so forth).</span></span>
-   <span data-ttu-id="885df-109">選擇性旗標，稍後說明。</span><span class="sxs-lookup"><span data-stu-id="885df-109">Optional flags, described shortly.</span></span>

<span data-ttu-id="885df-110">用戶端會藉由呼叫 [**IMediaParams：： AddEnvelope**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-addenvelope) 方法並傳入 **MP \_ 信封 \_ 區段** 結構的陣列，將信封區段新增至參數。</span><span class="sxs-lookup"><span data-stu-id="885df-110">The client adds envelope segments to a parameter by calling the [**IMediaParams::AddEnvelope**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-addenvelope) method and passing in an array of **MP\_ENVELOPE\_SEGMENT** structures.</span></span> <span data-ttu-id="885df-111">在呼叫方法之前，用戶端應該將區段排序成遞增的時間順序。</span><span class="sxs-lookup"><span data-stu-id="885df-111">The client should sort the segments into ascending time order before calling the method.</span></span> <span data-ttu-id="885df-112">當您處理資料時，可以想像出每個信封區段的參數移動，例如一系列 hills 的車輛駕駛。</span><span class="sxs-lookup"><span data-stu-id="885df-112">As the DMO processes data, you can imagine the parameter traveling over each envelope segment, like a car driving over a series of hills.</span></span> <span data-ttu-id="885df-113">[**IMediaParams：： GetParam**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-getparam)方法會傳回最新的值。</span><span class="sxs-lookup"><span data-stu-id="885df-113">The [**IMediaParams::GetParam**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-getparam) method returns the most recent value.</span></span>

<span data-ttu-id="885df-114">兩個連續的區段之間可能會有間距。</span><span class="sxs-lookup"><span data-stu-id="885df-114">Two adjacent segments can have a gap between them.</span></span> <span data-ttu-id="885df-115">在間距之間，參數會保留先前的值，如下所示：</span><span class="sxs-lookup"><span data-stu-id="885df-115">During gaps, the parameter retains its previous value, as follows:</span></span>

-   <span data-ttu-id="885df-116">在第一個區段之前，值是中性值。</span><span class="sxs-lookup"><span data-stu-id="885df-116">Before the first segment, the value is the neutral value.</span></span>
-   <span data-ttu-id="885df-117">在區段之間，值是上一個區段的結束值。</span><span class="sxs-lookup"><span data-stu-id="885df-117">Between segments, the value is the ending value of the previous segment.</span></span>
-   <span data-ttu-id="885df-118">在最後一個區段之後，值會維持在該區段的結束值。</span><span class="sxs-lookup"><span data-stu-id="885df-118">After the last segment, the value remains at the ending value of that segment.</span></span>
-   <span data-ttu-id="885df-119">如果用戶端排清了，則值會還原為中性值。</span><span class="sxs-lookup"><span data-stu-id="885df-119">If the client flushes the DMO, the value reverts to the neutral value.</span></span>

<span data-ttu-id="885df-120">您可以設定下列其中一個旗標來改變區段：</span><span class="sxs-lookup"><span data-stu-id="885df-120">You can alter a segment by setting either of the following flags:</span></span>

-   <span data-ttu-id="885df-121">MPF \_ ENVLP \_ 開始 \_ CURRENTVAL。</span><span class="sxs-lookup"><span data-stu-id="885df-121">MPF\_ENVLP\_BEGIN\_CURRENTVAL.</span></span> <span data-ttu-id="885df-122">SQL-DMO 使用參數的最新值做為區段的起始值。</span><span class="sxs-lookup"><span data-stu-id="885df-122">The DMO uses the most recent value of the parameter as the starting value for the segment.</span></span> <span data-ttu-id="885df-123">這可能是中性值，或上一個區段的結束值。</span><span class="sxs-lookup"><span data-stu-id="885df-123">This might be the neutral value, or the ending value from the previous segment.</span></span> <span data-ttu-id="885df-124">SQL-DMO 會忽略 **MP \_ 信封 \_ 區段** 結構的 **valStart** 成員。</span><span class="sxs-lookup"><span data-stu-id="885df-124">The DMO ignores the **valStart** member of the **MP\_ENVELOPE\_SEGMENT** structure.</span></span>
-   <span data-ttu-id="885df-125">MPF \_ ENVLP \_ 開始 \_ NEUTRALVAL。</span><span class="sxs-lookup"><span data-stu-id="885df-125">MPF\_ENVLP\_BEGIN\_NEUTRALVAL.</span></span> <span data-ttu-id="885df-126">SQL-DMO 使用參數的中性值作為區段的起始值。</span><span class="sxs-lookup"><span data-stu-id="885df-126">The DMO uses the neutral value of the parameter as the starting value for the segment.</span></span> <span data-ttu-id="885df-127">它會忽略 **valStart**。</span><span class="sxs-lookup"><span data-stu-id="885df-127">It ignores **valStart**.</span></span>

<span data-ttu-id="885df-128">您可以將這些旗標視為抓取區段的起點，並向上或向下移動，而結束值仍保持固定。</span><span class="sxs-lookup"><span data-stu-id="885df-128">You can think of these flags as grabbing the starting point of the segment and moving it up or down, while the ending value remains fixed.</span></span> <span data-ttu-id="885df-129">區段會據以「延展」。</span><span class="sxs-lookup"><span data-stu-id="885df-129">The segment will "stretch" accordingly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="885df-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="885df-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="885df-131">媒體參數</span><span class="sxs-lookup"><span data-stu-id="885df-131">Media Parameters</span></span>](media-parameters.md)
</dt> </dl>

 

 




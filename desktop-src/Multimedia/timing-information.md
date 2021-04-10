---
title: 計時資訊
description: 計時資訊
ms.assetid: ff9d6fb2-1387-49ce-a4de-1b2f67353628
keywords:
- 音樂檢測數位介面 (MIDI) ，時間資訊
- MIDI (音樂檢測數位介面) ，時間資訊
- 串流緩衝區，計時資訊
- MIDIEVENT 結構
- 串流緩衝區，SMPTE 格式
- 串流緩衝區，季備註時間
- 資料流程緩衝區，刻度
- SMPTE 格式
- 季備註時間
- 刻度
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2daf5b1847456e8fb518665521e484118fead79
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092656"
---
# <a name="timing-information"></a><span data-ttu-id="3e479-113">計時資訊</span><span class="sxs-lookup"><span data-stu-id="3e479-113">Timing Information</span></span>

<span data-ttu-id="3e479-114">MIDI 事件的計時資訊儲存在 [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent)結構的 **dwDeltaTime** 成員中。</span><span class="sxs-lookup"><span data-stu-id="3e479-114">Timing information for a MIDI event is stored in the **dwDeltaTime** member of the [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) structure.</span></span> <span data-ttu-id="3e479-115">時間會以刻度提供，如 *標準的 MIDI 檔案 1.0* 規格中所定義。</span><span class="sxs-lookup"><span data-stu-id="3e479-115">Time is given in ticks, as defined in the *Standard MIDI Files 1.0* specification.</span></span> <span data-ttu-id="3e479-116">刻度的長度是以時間格式定義的，可能是與資料流程相關聯的節奏。</span><span class="sxs-lookup"><span data-stu-id="3e479-116">The length of a tick is defined by the time format and possibly the tempo associated with the stream.</span></span> <span data-ttu-id="3e479-117">如需有關資料流程的詳細資訊，請參閱 [MIDI 串流](midi-streams.md)。</span><span class="sxs-lookup"><span data-stu-id="3e479-117">For more information about streams, see [MIDI Streams](midi-streams.md).</span></span>

<span data-ttu-id="3e479-118">刻度的表示方式是以每季的微秒數表示，或以 SMPTE (社會的運動圖片和電視工程師) 時程表示。</span><span class="sxs-lookup"><span data-stu-id="3e479-118">A tick is expressed either as microseconds per quarter note or as ticks of SMPTE (Society of Motion Picture and Television Engineers) time.</span></span> <span data-ttu-id="3e479-119">個別傳送 MIDI 訊息或使用未處理之 MIDI 訊息的應用程式，會使用季記時間和節奏資訊來判斷刻度的持續時間。</span><span class="sxs-lookup"><span data-stu-id="3e479-119">Applications that send MIDI messages individually or use unprocessed MIDI messages use quarter note time and tempo information to determine the duration of a tick.</span></span> <span data-ttu-id="3e479-120">前置處理 MIDI 訊息的應用程式可以將經過時間儲存為所使用之 SMPTE 單位的計數。</span><span class="sxs-lookup"><span data-stu-id="3e479-120">Applications that preprocess MIDI messages can store the elapsed time as a count of the SMPTE units being used.</span></span>

<span data-ttu-id="3e479-121">四分之一附注時間會以零表示，在時間單位的單字 (位 15) 。</span><span class="sxs-lookup"><span data-stu-id="3e479-121">Quarter note time is indicated with a zero in the high-word bit (bit 15) of the time-division word.</span></span> <span data-ttu-id="3e479-122">單字的其餘部分包含每季附注的刻度。</span><span class="sxs-lookup"><span data-stu-id="3e479-122">The remainder of the word contains the ticks per quarter note.</span></span> <span data-ttu-id="3e479-123">與 MIDI 資料串流相關聯的節奏會以每季 (微秒數表示) 與標準的 MIDI 檔案 *1.0* 規格保持一致。</span><span class="sxs-lookup"><span data-stu-id="3e479-123">A tempo associated with a stream of MIDI data is kept in units (microseconds per quarter note) consistent with the *Standard MIDI Files 1.0* specification.</span></span> <span data-ttu-id="3e479-124">例如，在4/4 時間中，使用每季500000微秒節奏的季附注會以每分鐘120的速率來播放。</span><span class="sxs-lookup"><span data-stu-id="3e479-124">For example, a quarter note in 4/4 time that uses a tempo of 500,000 microseconds per quarter note plays at the rate of 120 beats per minute.</span></span>

<span data-ttu-id="3e479-125">SMPTE 時間分割格式會完全指定滴答的長度，而不需要節奏資訊。</span><span class="sxs-lookup"><span data-stu-id="3e479-125">SMPTE time division formats completely specify the length of a tick without the need for tempo information.</span></span> <span data-ttu-id="3e479-126">使用 SMPTE 時間格式時，可以與其他的 SMPTE 事件（例如影片或等量音訊）同步處理 MIDI 序列。</span><span class="sxs-lookup"><span data-stu-id="3e479-126">In using SMPTE time formats, MIDI sequences can be synchronized with other SMPTE events, such as video or striped audio.</span></span> <span data-ttu-id="3e479-127">「SMPTE 時間」以高序位位中的1表示，以時間為單位的單字 (位 15) 。</span><span class="sxs-lookup"><span data-stu-id="3e479-127">SMPTE time is indicated with a 1 in the high-order bit (bit 15) of the time-division word.</span></span> <span data-ttu-id="3e479-128">最重要位元組的其餘部分會將使用中的 SMPTE 格式指定為負數值。</span><span class="sxs-lookup"><span data-stu-id="3e479-128">The rest of the most-significant byte specifies the SMPTE format in use as negative values.</span></span> <span data-ttu-id="3e479-129">支援的 SMPTE 格式及其對應的值 (在括弧中) 為 24 (-24) 、25 (-25) 、30 (-30) 和30卸載 (-29) 。</span><span class="sxs-lookup"><span data-stu-id="3e479-129">The supported SMPTE formats and their corresponding values (in parentheses) are 24 (-24), 25 (-25), 30 (-30), and 30 drop (-29).</span></span> <span data-ttu-id="3e479-130">時間除法單字的低位元組會指定每個 SMPTE 框架的刻度數目。</span><span class="sxs-lookup"><span data-stu-id="3e479-130">The low byte of the time-division word specifies the number of ticks per SMPTE frame.</span></span>

 

 
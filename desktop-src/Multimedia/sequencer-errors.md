---
title: Sequencer 錯誤
description: Sequencer 錯誤
ms.assetid: 07f2d6c5-8c23-4f3e-8b8a-4f659eda57f7
keywords:
- MCIERR 傳回值，sequencer 錯誤
- 多媒體參考，sequencer 錯誤
- 多媒體的參考、sequencer 錯誤
- 媒體控制介面 (MCI) 、sequencer 錯誤
- MCI (媒體控制介面) 、sequencer 錯誤
- MCI、sequencer 錯誤的參考
- MCI 參考，sequencer 錯誤
- 媒體控制介面 (MCI) ，錯誤
- MCI (媒體控制介面) ，錯誤
- MCI 的參考，錯誤
- MCI 參考，錯誤
- sequencer 錯誤
- MCI sequencer 錯誤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dd7d55d3b49be3d641f7396148d98766b224a58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673160"
---
# <a name="sequencer-errors"></a><span data-ttu-id="193de-116">Sequencer 錯誤</span><span class="sxs-lookup"><span data-stu-id="193de-116">Sequencer Errors</span></span>

<span data-ttu-id="193de-117">下列額外的傳回值是針對 MCI sequencers 所定義：</span><span class="sxs-lookup"><span data-stu-id="193de-117">The following additional return values are defined for MCI sequencers:</span></span>



| <span data-ttu-id="193de-118">值</span><span class="sxs-lookup"><span data-stu-id="193de-118">Value</span></span>                          | <span data-ttu-id="193de-119">意義</span><span class="sxs-lookup"><span data-stu-id="193de-119">Meaning</span></span>                                                                                                                                                  |
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="193de-120">MCIERR \_ SEQ \_ DIV \_ 不相容</span><span class="sxs-lookup"><span data-stu-id="193de-120">MCIERR\_SEQ\_DIV\_INCOMPATIBLE</span></span> | <span data-ttu-id="193de-121">"Song 指標" 和 SMPTE 的時間格式為單數。</span><span class="sxs-lookup"><span data-stu-id="193de-121">The time formats of the "song pointer" and SMPTE are singular.</span></span> <span data-ttu-id="193de-122">您無法一起使用它們。</span><span class="sxs-lookup"><span data-stu-id="193de-122">You can't use them together.</span></span>                                                              |
| <span data-ttu-id="193de-123">MCIERR \_ SEQ \_ NOMIDIPRESENT</span><span class="sxs-lookup"><span data-stu-id="193de-123">MCIERR\_SEQ\_NOMIDIPRESENT</span></span>     | <span data-ttu-id="193de-124">此系統沒有任何已安裝的 MIDI 裝置。</span><span class="sxs-lookup"><span data-stu-id="193de-124">This system has no installed MIDI devices.</span></span> <span data-ttu-id="193de-125">使用主控台的 [驅動程式] 選項來安裝 MIDI 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="193de-125">Use the Drivers option from the Control Panel to install a MIDI driver.</span></span>                                       |
| <span data-ttu-id="193de-126">MCIERR \_ SEQ \_ PORT \_ INUSE</span><span class="sxs-lookup"><span data-stu-id="193de-126">MCIERR\_SEQ\_PORT\_INUSE</span></span>       | <span data-ttu-id="193de-127">指定的 MIDI 埠已在使用中。</span><span class="sxs-lookup"><span data-stu-id="193de-127">The specified MIDI port is already in use.</span></span> <span data-ttu-id="193de-128">等到免費為止;然後再試一次。</span><span class="sxs-lookup"><span data-stu-id="193de-128">Wait until it is free; then, try again.</span></span>                                                                       |
| <span data-ttu-id="193de-129">MCIERR \_ SEQ \_ PORT \_ MAPNODEVICE</span><span class="sxs-lookup"><span data-stu-id="193de-129">MCIERR\_SEQ\_PORT\_MAPNODEVICE</span></span> | <span data-ttu-id="193de-130">目前的 MIDI 對應程式安裝程式指的是未安裝在系統上的 MIDI 裝置。</span><span class="sxs-lookup"><span data-stu-id="193de-130">The current MIDI Mapper setup refers to a MIDI device that is not installed on the system.</span></span> <span data-ttu-id="193de-131">使用主控台的 MIDI 對應程式來編輯安裝程式。</span><span class="sxs-lookup"><span data-stu-id="193de-131">Use the MIDI Mapper from the Control Panel to edit the setup.</span></span> |
| <span data-ttu-id="193de-132">MCIERR \_ SEQ \_ PORT \_ MISCERROR</span><span class="sxs-lookup"><span data-stu-id="193de-132">MCIERR\_SEQ\_PORT\_MISCERROR</span></span>   | <span data-ttu-id="193de-133">指定的埠發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="193de-133">An error occurred with specified port.</span></span>                                                                                                                   |
| <span data-ttu-id="193de-134">MCIERR \_ SEQ \_ 埠不 \_ 存在</span><span class="sxs-lookup"><span data-stu-id="193de-134">MCIERR\_SEQ\_PORT\_NONEXISTENT</span></span> | <span data-ttu-id="193de-135">系統上未安裝指定的 MIDI 裝置。</span><span class="sxs-lookup"><span data-stu-id="193de-135">The specified MIDI device is not installed on the system.</span></span> <span data-ttu-id="193de-136">使用主控台的 [驅動程式] 選項來安裝 MIDI 裝置。</span><span class="sxs-lookup"><span data-stu-id="193de-136">Use the Drivers option from the Control Panel to install a MIDI device.</span></span>                        |
| <span data-ttu-id="193de-137">MCIERR \_ SEQ \_ PORTUNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="193de-137">MCIERR\_SEQ\_PORTUNSPECIFIED</span></span>   | <span data-ttu-id="193de-138">系統未指定目前的 MIDI 埠。</span><span class="sxs-lookup"><span data-stu-id="193de-138">The system does not have a current MIDI port specified.</span></span>                                                                                                  |
| <span data-ttu-id="193de-139">MCIERR \_ SEQ \_ 計時器</span><span class="sxs-lookup"><span data-stu-id="193de-139">MCIERR\_SEQ\_TIMER</span></span>             | <span data-ttu-id="193de-140">所有的多媒體計時器都是由其他應用程式使用中。</span><span class="sxs-lookup"><span data-stu-id="193de-140">All multimedia timers are being used by other applications.</span></span> <span data-ttu-id="193de-141">結束其中一個應用程式;然後再試一次。</span><span class="sxs-lookup"><span data-stu-id="193de-141">Quit one of these applications; then, try again.</span></span>                                             |



 

 

 





---
title: 重設 MIDI 輸出
description: 重設 MIDI 輸出
ms.assetid: 281a7cfa-f274-4c7a-b63a-c0573b9f1169
keywords:
- " (MIDI) 的音樂檢測數位介面，重設輸出裝置"
- MIDI (的音樂檢測數位介面) ，重設輸出裝置
- 播放 MIDI 檔案，重設輸出裝置
- 重設輸出裝置
- 音樂檢測數位介面 (MIDI) 、輸出裝置
- MIDI (的音樂檢測數位介面) ，輸出裝置
- 播放 MIDI 檔案，輸出裝置
- MIDI 輸出裝置
- 'EOX (結束專屬) '
- 'EOX 結尾 (的) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15778fc8a1a48c34b69915aafb7e3139153b5882
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314686"
---
# <a name="resetting-midi-output"></a><span data-ttu-id="ddbd2-113">重設 MIDI 輸出</span><span class="sxs-lookup"><span data-stu-id="ddbd2-113">Resetting MIDI Output</span></span>

<span data-ttu-id="ddbd2-114">[**MidiOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset)函式會關閉指定之 midi 裝置的所有 MIDI 通道上的所有便箋。</span><span class="sxs-lookup"><span data-stu-id="ddbd2-114">The [**midiOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset) function turns off all notes on all MIDI channels for a specified MIDI device.</span></span> <span data-ttu-id="ddbd2-115">然後，此函式會將任何擱置中的系統專屬緩衝區標示為已完成，並將它們傳回給應用程式。</span><span class="sxs-lookup"><span data-stu-id="ddbd2-115">Then, the function marks any pending system-exclusive buffers as done and returns them to the application.</span></span> <span data-ttu-id="ddbd2-116">此函式可用於使用 MIDI 輸出的應用程式，讓使用者能夠重設 MIDI 輸出。</span><span class="sxs-lookup"><span data-stu-id="ddbd2-116">This function can be useful in an application that uses MIDI output to provide the user with the ability to reset MIDI output.</span></span>

> [!Note]  
> <span data-ttu-id="ddbd2-117">在不傳送 EOX 的情況下終止系統專屬的訊息， (端) 位元組會導致接收裝置發生問題。</span><span class="sxs-lookup"><span data-stu-id="ddbd2-117">Terminating a system-exclusive message without sending an EOX (end-of-exclusive) byte can cause problems for the receiving device.</span></span> <span data-ttu-id="ddbd2-118">**MidiOutReset** 函式會在終止系統專屬的訊息時，不會傳送 EOX 位元組，因為應用程式會負責執行此工作。</span><span class="sxs-lookup"><span data-stu-id="ddbd2-118">The **midiOutReset** function does not send an EOX byte when it terminates a system-exclusive message, because applications are responsible for doing this.</span></span>

 

 

 
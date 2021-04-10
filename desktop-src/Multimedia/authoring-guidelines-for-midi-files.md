---
title: 適用于 MIDI 檔案的撰寫指導方針
description: 適用于 MIDI 檔案的撰寫指導方針
ms.assetid: 57e3d260-d275-4b0c-9db0-d036dd12fdb8
keywords:
- " (MIDI) 的音樂檢測數位介面，檔案撰寫指導方針"
- MIDI (的音樂檢測數位介面) ，檔案撰寫指導方針
- 建立 MIDI 檔案，檔案撰寫指導方針
- 標準 MIDI 修補程式指派
- 標準 MIDI 金鑰指派
- 音樂檢測數位介面 (MIDI) 、標準修補程式指派
- MIDI (的音樂檢測數位介面) ，標準修補程式指派
- " (MIDI) 的音樂檢測數位介面，標準金鑰指派"
- MIDI (的音樂檢測數位介面) ，標準金鑰指派
- 建立 MIDI 檔案，標準修補程式指派
- 建立 MIDI 檔案，標準金鑰指派
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6fcfec1b5089fa3c58c18eb8990156df12db0ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022005"
---
# <a name="authoring-guidelines-for-midi-files"></a><span data-ttu-id="7f38a-114">適用于 MIDI 檔案的撰寫指導方針</span><span class="sxs-lookup"><span data-stu-id="7f38a-114">Authoring Guidelines for MIDI Files</span></span>

<span data-ttu-id="7f38a-115">遵循這些指導方針來撰寫適用于 Windows 的裝置獨立 MIDI 檔案：</span><span class="sxs-lookup"><span data-stu-id="7f38a-115">Follow these guidelines to author device-independent MIDI files for Windows:</span></span>

-   <span data-ttu-id="7f38a-116">使用 [標準的 Midi 修補程式指派](standard-midi-patch-assignments.md) 和 [標準的 midi 金鑰指派](standard-midi-key-assignments.md)。</span><span class="sxs-lookup"><span data-stu-id="7f38a-116">Use the [Standard MIDI Patch Assignments](standard-midi-patch-assignments.md) and [Standard MIDI Key Assignments](standard-midi-key-assignments.md).</span></span>
-   <span data-ttu-id="7f38a-117">一律將程式變更訊息傳送至通道以選取修補程式，然後再將其他訊息傳送至該通道。</span><span class="sxs-lookup"><span data-stu-id="7f38a-117">Always send a program-change message to a channel to select a patch before sending other messages to that channel.</span></span> <span data-ttu-id="7f38a-118">針對兩個 percussion 通道 (10 和 16) ，請選取 [程式編號 0]。</span><span class="sxs-lookup"><span data-stu-id="7f38a-118">For the two percussion channels (10 and 16), select program number 0.</span></span>
-   <span data-ttu-id="7f38a-119">一律遵循 MIDI 程式-變更訊息與 MIDI 主要磁片區控制器訊息 (控制器編號 7) 來設定修補程式的相對磁片區。</span><span class="sxs-lookup"><span data-stu-id="7f38a-119">Always follow a MIDI program-change message with a MIDI main-volume controller message (controller number 7) to set the relative volume of the patch.</span></span>
-   <span data-ttu-id="7f38a-120">針對一般接聽層級，使用主要磁片區控制器的 80 (0x50) 。</span><span class="sxs-lookup"><span data-stu-id="7f38a-120">Use a value of 80 (0x50) for the main-volume controller for normal listening levels.</span></span> <span data-ttu-id="7f38a-121">如需更安靜或更高的層級，您可以使用較低或更高的值。</span><span class="sxs-lookup"><span data-stu-id="7f38a-121">For quieter or louder levels, you can use lower or higher values.</span></span>
-   <span data-ttu-id="7f38a-122">僅使用下列 MIDI 訊息：注意：具有速度、附注關閉、程式變更、音調彎曲、主要磁片區 (控制器 7) 和氣流踏板 (控制器 64) 。</span><span class="sxs-lookup"><span data-stu-id="7f38a-122">Use only the following MIDI messages: note-on with velocity, note-off, program change, pitch bend, main volume (controller 7), and damper pedal (controller 64).</span></span> <span data-ttu-id="7f38a-123">需要內部合成者才能回應這些訊息，而大部分的 MIDI 樂器也會回應這些訊息。</span><span class="sxs-lookup"><span data-stu-id="7f38a-123">Internal synthesizers are required to respond to these messages and most MIDI musical instruments respond to them as well.</span></span>

 

 





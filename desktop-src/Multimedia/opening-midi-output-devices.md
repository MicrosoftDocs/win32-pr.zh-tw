---
title: 開啟 MIDI 輸出裝置
description: 開啟 MIDI 輸出裝置
ms.assetid: 0a06611b-c0cd-4884-bc17-761c4aec4418
keywords:
- 音樂檢測數位介面 (MIDI) 、輸出裝置
- MIDI (的音樂檢測數位介面) ，輸出裝置
- 播放 MIDI 檔案，輸出裝置
- MIDI 輸出裝置
- 音樂檢測數位介面 (MIDI) ，開啟輸出裝置
- MIDI (的音樂檢測數位介面) ，開啟輸出裝置
- 播放 MIDI 檔案，開啟輸出裝置
- 開啟 MIDI 輸出裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ca7a7e1db461b29700ec7c7c61ee140073bc345
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463068"
---
# <a name="opening-midi-output-devices"></a><span data-ttu-id="2cec8-111">開啟 MIDI 輸出裝置</span><span class="sxs-lookup"><span data-stu-id="2cec8-111">Opening MIDI Output Devices</span></span>

<span data-ttu-id="2cec8-112">若要開啟 MIDI 輸出裝置來播放，請使用 [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) 函式。</span><span class="sxs-lookup"><span data-stu-id="2cec8-112">To open a MIDI output device for playback, use the [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function.</span></span> <span data-ttu-id="2cec8-113">此函式會開啟與指定裝置識別碼相關聯的裝置，並將控制碼寫入指定的記憶體位置，以傳回開啟裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="2cec8-113">This function opens the device associated with the specified device identifier and returns a handle of the open device by writing the handle to a specified memory location.</span></span>

<span data-ttu-id="2cec8-114">**MidiOutOpen** 的其中一個參數是雙值。</span><span class="sxs-lookup"><span data-stu-id="2cec8-114">One of the parameters of **midiOutOpen** is a doubleword value.</span></span> <span data-ttu-id="2cec8-115">這個值會指定視窗或執行緒控制碼、事件控制碼或回呼函式的位址，用來監視 MIDI 系統專屬資料和資料流程緩衝區的播放進度。</span><span class="sxs-lookup"><span data-stu-id="2cec8-115">This value specifies a window or thread handle, an event handle, or the address of a callback function that is used to monitor the progress of the playback of MIDI system-exclusive data and stream buffers.</span></span> <span data-ttu-id="2cec8-116">監視可讓應用程式判斷何時傳送額外的資料區塊，以及何時釋放已傳送的資料區塊。</span><span class="sxs-lookup"><span data-stu-id="2cec8-116">Monitoring enables the application to determine when to send additional data blocks and when to free data blocks that have been sent.</span></span> <span data-ttu-id="2cec8-117">如需這些方法的詳細資訊，請參閱 [管理 MIDI 資料區塊](managing-midi-data-blocks.md)。</span><span class="sxs-lookup"><span data-stu-id="2cec8-117">For more information about these methods, see [Managing MIDI Data Blocks](managing-midi-data-blocks.md).</span></span>

 

 
---
title: 開啟和關閉設備磁碟機
description: 開啟和關閉設備磁碟機
ms.assetid: 441bc0ec-41c9-4595-92f9-4c2304b10f16
keywords:
- 音樂檢測數位介面 (MIDI) ，開啟裝置
- MIDI (的音樂檢測數位介面) ，開啟裝置
- MIDI 服務，開啟裝置
- 開啟 MIDI 裝置
- 音樂檢測數位介面 (MIDI) ，關閉裝置
- MIDI (的音樂檢測數位介面) ，關閉裝置
- MIDI 服務，關閉裝置
- 關閉 MIDI 裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53d7035455baa067b81af7da980a4ae043500c7b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681802"
---
# <a name="opening-and-closing-device-drivers"></a><span data-ttu-id="e7f74-111">開啟和關閉設備磁碟機</span><span class="sxs-lookup"><span data-stu-id="e7f74-111">Opening and Closing Device Drivers</span></span>

<span data-ttu-id="e7f74-112">您必須在使用前先開啟 MIDI 裝置，並在使用完畢後立即關閉裝置。</span><span class="sxs-lookup"><span data-stu-id="e7f74-112">You must open a MIDI device before using it, and you should close the device as soon as you finish using it.</span></span> <span data-ttu-id="e7f74-113">Windows 提供下列功能來開啟和關閉不同類型的 MIDI 裝置。</span><span class="sxs-lookup"><span data-stu-id="e7f74-113">Windows provides the following functions to open and close different types of MIDI devices.</span></span>



| <span data-ttu-id="e7f74-114">值</span><span class="sxs-lookup"><span data-stu-id="e7f74-114">Value</span></span>                                | <span data-ttu-id="e7f74-115">意義</span><span class="sxs-lookup"><span data-stu-id="e7f74-115">Meaning</span></span>                                            |
|--------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="e7f74-116">**midiInClose**</span><span class="sxs-lookup"><span data-stu-id="e7f74-116">**midiInClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose)   | <span data-ttu-id="e7f74-117">關閉指定的 MIDI 輸入裝置。</span><span class="sxs-lookup"><span data-stu-id="e7f74-117">Closes a specified MIDI input device.</span></span>              |
| [<span data-ttu-id="e7f74-118">**midiInOpen**</span><span class="sxs-lookup"><span data-stu-id="e7f74-118">**midiInOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)     | <span data-ttu-id="e7f74-119">開啟指定的 MIDI 輸入裝置以進行錄製。</span><span class="sxs-lookup"><span data-stu-id="e7f74-119">Opens a specified MIDI input device for recording.</span></span> |
| [<span data-ttu-id="e7f74-120">**midiOutClose**</span><span class="sxs-lookup"><span data-stu-id="e7f74-120">**midiOutClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) | <span data-ttu-id="e7f74-121">關閉指定的 MIDI 輸出裝置。</span><span class="sxs-lookup"><span data-stu-id="e7f74-121">Closes a specified MIDI output device.</span></span>             |
| [<span data-ttu-id="e7f74-122">**midiOutOpen**</span><span class="sxs-lookup"><span data-stu-id="e7f74-122">**midiOutOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)   | <span data-ttu-id="e7f74-123">開啟 MIDI 輸出裝置以供播放。</span><span class="sxs-lookup"><span data-stu-id="e7f74-123">Opens a MIDI output device for playback.</span></span>           |



 

<span data-ttu-id="e7f74-124">開啟 MIDI 裝置的每個函式會以裝置識別碼、記憶體位置的位址，以及一些 MIDI 裝置特有的參數作為參數。</span><span class="sxs-lookup"><span data-stu-id="e7f74-124">Each function that opens a MIDI device takes as parameters a device identifier, an address of a memory location, and some parameters unique to MIDI devices.</span></span> <span data-ttu-id="e7f74-125">記憶體位置會以裝置控制碼填滿，用來識別呼叫其他音訊函式的開放式音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="e7f74-125">The memory location is filled with a device handle, which is used to identify the open audio device in calls to other audio functions.</span></span>

<span data-ttu-id="e7f74-126">許多 MIDI 函數可以接受裝置控制碼或裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="e7f74-126">Many MIDI functions can accept either a device handle or a device identifier.</span></span> <span data-ttu-id="e7f74-127">雖然您可以在使用裝置識別碼的任何地方使用裝置控制碼，但在呼叫控制碼時，不能一律使用裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="e7f74-127">Although you can use a device handle wherever you would use a device identifier, you cannot always use a device identifier when a handle is called for.</span></span>

> [!Note]  
> <span data-ttu-id="e7f74-128">MIDI 裝置不一定可共用，因此當使用者要求時，可能無法使用特定的裝置。</span><span class="sxs-lookup"><span data-stu-id="e7f74-128">MIDI devices are not necessarily sharable, so a particular device may not be available when a user requests it.</span></span> <span data-ttu-id="e7f74-129">如果發生這種情況，應用程式應該會通知使用者，並讓使用者嘗試再次開啟裝置。</span><span class="sxs-lookup"><span data-stu-id="e7f74-129">If this happens, the application should notify the user and allow the user to try to open the device again.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e7f74-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="e7f74-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7f74-131">MIDI 服務</span><span class="sxs-lookup"><span data-stu-id="e7f74-131">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 
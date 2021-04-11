---
title: MIDI 對應程式和 Windows
description: MIDI 對應程式和 Windows
ms.assetid: a077f935-e085-4148-9975-7926ac018f0c
keywords:
- 音樂檢測數位介面 (MIDI) 、MIDI 對應程式
- MIDI (的音樂檢測數位介面) 、MIDI 對應程式
- MIDI 對應工具，架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951ad3cee4fb37de6ecbfdc4f81860afcb9f589d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023409"
---
# <a name="the-midi-mapper-and-windows"></a><span data-ttu-id="c4aad-106">MIDI 對應程式和 Windows</span><span class="sxs-lookup"><span data-stu-id="c4aad-106">The MIDI Mapper and Windows</span></span>

<span data-ttu-id="c4aad-107">MIDI 對應工具是系統軟體的一部分。</span><span class="sxs-lookup"><span data-stu-id="c4aad-107">The MIDI Mapper is part of the system software.</span></span> <span data-ttu-id="c4aad-108">下圖顯示 MIDI 對應工具與音訊服務的其他元素之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="c4aad-108">The following illustration shows how the MIDI Mapper relates to other elements of the audio services.</span></span>

![midi 對應工具與音訊服務映射的其他元素之間的關聯](images/mmap-a01.gif)

<span data-ttu-id="c4aad-110">從應用程式的觀點來看，MIDI 對應工具看起來像另一個 MIDI 輸出裝置。</span><span class="sxs-lookup"><span data-stu-id="c4aad-110">From the viewpoint of an application, the MIDI Mapper looks like another MIDI output device.</span></span> <span data-ttu-id="c4aad-111">MIDI 對應工具會接收由低層級 MIDI 輸出函式 [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) 和 [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)傳送給它的訊息。</span><span class="sxs-lookup"><span data-stu-id="c4aad-111">The MIDI Mapper receives messages sent to it by the low-level MIDI output functions [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) and [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg).</span></span> <span data-ttu-id="c4aad-112">MIDI 對應程式會修改這些訊息，並根據目前的 MIDI 安裝對應，將它們重新導向至 MIDI 輸出裝置。</span><span class="sxs-lookup"><span data-stu-id="c4aad-112">The MIDI Mapper modifies these messages and redirects them to a MIDI output device according to the current MIDI setup map.</span></span> <span data-ttu-id="c4aad-113">目前的 MIDI 安裝對應是由使用者透過 MIDI 主控台選項所選取。</span><span class="sxs-lookup"><span data-stu-id="c4aad-113">The current MIDI setup map is selected by the user by means of the MIDI Control Panel option.</span></span> <span data-ttu-id="c4aad-114">只有使用者可以選取目前的設定對應;應用程式無法變更目前的設定對應。</span><span class="sxs-lookup"><span data-stu-id="c4aad-114">Only the user can select the current setup map; applications cannot change the current setup map.</span></span>

 

 
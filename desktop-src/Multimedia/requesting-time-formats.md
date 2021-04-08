---
title: 要求時間格式
description: 要求時間格式
ms.assetid: 3492dfe3-ed54-405a-aa4f-b17abbd1e07f
keywords:
- " (MIDI) ，時間格式的音樂檢測數位介面"
- MIDI (的音樂檢測數位介面) ，時間格式
- MIDI 服務，時間格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf191c857c45896c916ace4656d33bd3dd558f04
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681734"
---
# <a name="requesting-time-formats"></a><span data-ttu-id="6cc3a-106">要求時間格式</span><span class="sxs-lookup"><span data-stu-id="6cc3a-106">Requesting Time Formats</span></span>

<span data-ttu-id="6cc3a-107">Windows 會使用 [**MMTIME**](/previous-versions//dd757347(v=vs.85)) 結構以一或多個不同的格式來表示時間，包括毫秒、範例、SMPTE 和 MIDI 歌曲指標格式。</span><span class="sxs-lookup"><span data-stu-id="6cc3a-107">Windows uses the [**MMTIME**](/previous-versions//dd757347(v=vs.85)) structure to represent time in one or more different formats, including milliseconds, samples, SMPTE, and MIDI song pointer formats.</span></span> <span data-ttu-id="6cc3a-108">**WType** 成員會指定時間格式。</span><span class="sxs-lookup"><span data-stu-id="6cc3a-108">The **wType** member specifies the time format.</span></span>

<span data-ttu-id="6cc3a-109">[**MidiStreamPosition**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition)函數會使用 **MMTIME** 結構。</span><span class="sxs-lookup"><span data-stu-id="6cc3a-109">The [**midiStreamPosition**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition) function uses the **MMTIME** structure.</span></span> <span data-ttu-id="6cc3a-110">在呼叫此函式之前，您必須先設定 **wType** 成員，以指出您所要求的時間格式。</span><span class="sxs-lookup"><span data-stu-id="6cc3a-110">Before calling this function, you must set the **wType** member to indicate your requested time format.</span></span> <span data-ttu-id="6cc3a-111">若要查看是否支援要求的時間格式，請在呼叫後檢查 **wType** 。</span><span class="sxs-lookup"><span data-stu-id="6cc3a-111">To see if the requested time format is supported, check **wType** after the call.</span></span> <span data-ttu-id="6cc3a-112">如果不支援要求的時間格式，則會以設備磁碟機所選取的替代時間格式來指定時間，而 **wType** 成員會變更以指出選取的時間格式。</span><span class="sxs-lookup"><span data-stu-id="6cc3a-112">If the requested time format is not supported, the time is specified in an alternate time format selected by the device driver and the **wType** member is changed to indicate the selected time format.</span></span>

<span data-ttu-id="6cc3a-113">如需 **MMTIME** 結構的詳細資訊，請參閱 [多媒體計時器](multimedia-timers.md)。</span><span class="sxs-lookup"><span data-stu-id="6cc3a-113">For more information about the **MMTIME** structure, see [Multimedia Timers](multimedia-timers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6cc3a-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="6cc3a-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6cc3a-115">MIDI 服務</span><span class="sxs-lookup"><span data-stu-id="6cc3a-115">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 
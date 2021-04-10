---
title: 簡易音訊播放
description: 簡易音訊播放
ms.assetid: 51a0244d-123d-4efe-92e9-972e914cef78
keywords:
- 多媒體音訊、波形
- 音訊、波形
- 波形音訊，簡單播放
- MessageBeep 函式
- sndPlaySound 函式
- PlaySound 函式，簡單播放
- 多媒體音訊，PlaySound 函式
- 音訊、PlaySound 函式
- 波形音訊，PlaySound 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 256feded06de4ee92ee415f14bb08adc7fb4456e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933159"
---
# <a name="simple-audio-playback"></a><span data-ttu-id="d3155-112">簡易音訊播放</span><span class="sxs-lookup"><span data-stu-id="d3155-112">Simple Audio Playback</span></span>

<span data-ttu-id="d3155-113">您可以使用下列函式，在單一函式呼叫中播放應用程式中的波形音訊。</span><span class="sxs-lookup"><span data-stu-id="d3155-113">You can use the following functions to play waveform audio in your application in a single function call.</span></span>



| <span data-ttu-id="d3155-114">函式</span><span class="sxs-lookup"><span data-stu-id="d3155-114">Function</span></span>                                                      | <span data-ttu-id="d3155-115">描述</span><span class="sxs-lookup"><span data-stu-id="d3155-115">Description</span></span>                                                                                                         |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d3155-116">MessageBeep</span><span class="sxs-lookup"><span data-stu-id="d3155-116">MessageBeep</span></span>](/windows/win32/api/winuser/nf-winuser-messagebeep) | <span data-ttu-id="d3155-117">播放對應到指定系統警示等級的音效。</span><span class="sxs-lookup"><span data-stu-id="d3155-117">Plays the sound that corresponds to a specified system-alert level.</span></span>                                                 |
| <span data-ttu-id="d3155-118">[**sndPlaySound**](/previous-versions//dd798676(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d3155-118">[**sndPlaySound**](/previous-versions//dd798676(v=vs.85))</span></span>                          | <span data-ttu-id="d3155-119">播放的音效與登錄中輸入的系統音效或指定檔案的內容相對應。</span><span class="sxs-lookup"><span data-stu-id="d3155-119">Plays the sound that corresponds to the system sound entered in the registry or the contents of the specified file.</span></span> |
| <span data-ttu-id="d3155-120">[**PlaySound**](/previous-versions//dd743680(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d3155-120">[**PlaySound**](/previous-versions//dd743680(v=vs.85))</span></span>                                | <span data-ttu-id="d3155-121">提供 [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) 的所有功能，而且可以直接存取資源。</span><span class="sxs-lookup"><span data-stu-id="d3155-121">Provides all the functionality of [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) and can directly access resources.</span></span>           |



 

<span data-ttu-id="d3155-122">**MessageBeep** 函式是 WIN32 API 的標準元件;因為其功能非常有限，並記載于其他地方，所以不會在這裡討論。</span><span class="sxs-lookup"><span data-stu-id="d3155-122">The **MessageBeep** function is a standard part of the Win32 API; because its capabilities are very limited and it is documented elsewhere, it is not discussed here.</span></span>

<span data-ttu-id="d3155-123">列出的函式支援下列波形音訊來源：</span><span class="sxs-lookup"><span data-stu-id="d3155-123">The functions listed support the following sources of waveform audio:</span></span>

-   <span data-ttu-id="d3155-124">波形-與系統警示等級相關聯的音訊檔案</span><span class="sxs-lookup"><span data-stu-id="d3155-124">Waveform-audio files associated with system-alert levels</span></span>
-   <span data-ttu-id="d3155-125">由登錄中的專案所指定的波形音訊檔案</span><span class="sxs-lookup"><span data-stu-id="d3155-125">Waveform-audio files specified by entries in the registry</span></span>
-   <span data-ttu-id="d3155-126">記憶體中的 WAVE 資源</span><span class="sxs-lookup"><span data-stu-id="d3155-126">In-memory WAVE resources</span></span>
-   <span data-ttu-id="d3155-127">波形-依名稱指定的音訊檔案</span><span class="sxs-lookup"><span data-stu-id="d3155-127">Waveform-audio files specified by name</span></span>

<span data-ttu-id="d3155-128">[**SndPlaySound**](/previous-versions//dd798676(v=vs.85))和 [**PlaySound**](/previous-versions//dd743680(v=vs.85))函式會將整個波形-音訊檔案載入記憶體中，而且實際上會限制它們可以播放的檔案大小。</span><span class="sxs-lookup"><span data-stu-id="d3155-128">The [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) and [**PlaySound**](/previous-versions//dd743680(v=vs.85)) functions load an entire waveform-audio file into memory and, in effect, limit the size of the file they can play.</span></span> <span data-ttu-id="d3155-129">使用 **sndPlaySound** 和 **PlaySound** 來播放很小的波形音訊檔案，最多可達100k。</span><span class="sxs-lookup"><span data-stu-id="d3155-129">Use **sndPlaySound** and **PlaySound** to play waveform-audio files that are small — up to about 100K.</span></span> <span data-ttu-id="d3155-130">這兩個函式也需要音效資料的格式，可由其中一個已安裝的波形音訊驅動程式（包括 wave 對應程式）播放。</span><span class="sxs-lookup"><span data-stu-id="d3155-130">These two functions also require the sound data to be in a format that is playable by one of the installed waveform-audio drivers, including the wave mapper.</span></span>

<span data-ttu-id="d3155-131">針對較大的音效檔，請使用 Media Control 介面 (MCI) 服務。</span><span class="sxs-lookup"><span data-stu-id="d3155-131">For larger sound files, use the Media Control Interface (MCI) services.</span></span> <span data-ttu-id="d3155-132">如需詳細資訊，請參閱 [MCI](mci.md)。</span><span class="sxs-lookup"><span data-stu-id="d3155-132">For more information, see [MCI](mci.md).</span></span>

 

 
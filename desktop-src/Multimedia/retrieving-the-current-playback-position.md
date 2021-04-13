---
title: 正在抓取目前的播放位置
description: 正在抓取目前的播放位置
ms.assetid: a08fe5da-8945-486f-9413-877c7d13d5de
keywords:
- 波形音訊、目前的播放位置
- 波形-音訊介面、目前的播放位置
- 播放波形-音訊檔案，目前的播放位置
- waveOutGetPosition 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28737cfc292dc8779b21756f38813642b82e452
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314674"
---
# <a name="retrieving-the-current-playback-position"></a><span data-ttu-id="a1958-107">正在抓取目前的播放位置</span><span class="sxs-lookup"><span data-stu-id="a1958-107">Retrieving the Current Playback Position</span></span>

<span data-ttu-id="a1958-108">您可以使用 [**waveOutGetPosition**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetposition) 函式，在聲音音訊播放時，監視檔案內目前的播放位置。</span><span class="sxs-lookup"><span data-stu-id="a1958-108">You can monitor the current playback position within the file while waveform audio is playing by using the [**waveOutGetPosition**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetposition) function.</span></span>

<span data-ttu-id="a1958-109">針對波形音訊裝置，範例是慣用的時間格式，用來表示目前的位置。</span><span class="sxs-lookup"><span data-stu-id="a1958-109">For waveform-audio devices, samples are the preferred time format in which to represent the current position.</span></span> <span data-ttu-id="a1958-110">因此，波形音訊裝置的目前位置會指定為波形音訊檔案開頭的一個通道樣本數。</span><span class="sxs-lookup"><span data-stu-id="a1958-110">Thus, the current position of a waveform-audio device is specified as the number of samples for one channel from the beginning of the waveform-audio file.</span></span> <span data-ttu-id="a1958-111">若要查詢波形音訊裝置的目前位置，請將 [**MMTIME**](/previous-versions//dd757347(v=vs.85))結構的 **wType** 成員設定為時間範例， \_ 並將此結構傳遞至 **waveOutGetPosition**。</span><span class="sxs-lookup"><span data-stu-id="a1958-111">To query the current position of a waveform-audio device, set the **wType** member of the [**MMTIME**](/previous-versions//dd757347(v=vs.85)) structure to TIME\_SAMPLES and pass this structure to **waveOutGetPosition**.</span></span>

<span data-ttu-id="a1958-112">**MMTIME** 結構可代表一或多個不同格式的時間，包括毫秒、範例、SMPTE (的運動圖片和電視工程師) ，以及 MIDI 歌曲指標格式。</span><span class="sxs-lookup"><span data-stu-id="a1958-112">The **MMTIME** structure can represent time in one or more different formats, including milliseconds, samples, SMPTE (Society of Motion Picture and Television Engineers), and MIDI song pointer formats.</span></span> <span data-ttu-id="a1958-113">**WType** 成員會指定用來代表時間的格式。</span><span class="sxs-lookup"><span data-stu-id="a1958-113">The **wType** member specifies the format used to represent time.</span></span> <span data-ttu-id="a1958-114">在呼叫使用 **MMTIME** 結構的函式之前，您必須先設定 **wType** ，以指出您所要求的時間格式。</span><span class="sxs-lookup"><span data-stu-id="a1958-114">Before calling a function that uses the **MMTIME** structure, you must set **wType** to indicate your requested time format.</span></span> <span data-ttu-id="a1958-115">請務必在呼叫之後檢查 **wType** ，以查看是否支援要求的時間格式。</span><span class="sxs-lookup"><span data-stu-id="a1958-115">Be sure to check **wType** after the call to see whether the requested time format is supported.</span></span> <span data-ttu-id="a1958-116">如果不支援要求的時間格式，設備磁碟機會以替代時間格式指定時間，並將 **wType** 成員變更為選取的時間格式。</span><span class="sxs-lookup"><span data-stu-id="a1958-116">If the requested time format is not supported, the device driver specifies the time in an alternate time format and changes the **wType** member to the selected time format.</span></span>

<span data-ttu-id="a1958-117">如需 **MMTIME** 結構的詳細資訊，請參閱 [多媒體計時器](multimedia-timers.md)。</span><span class="sxs-lookup"><span data-stu-id="a1958-117">For more information about the **MMTIME** structure, see [Multimedia Timers](multimedia-timers.md).</span></span>

 

 
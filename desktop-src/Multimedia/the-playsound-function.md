---
title: PlaySound 函式
description: PlaySound 函式
ms.assetid: ce405a13-c4ab-4c9a-bcfe-8d4427b3d2d8
keywords:
- 多媒體音訊，PlaySound 函式
- 音訊、PlaySound 函式
- 波形音訊，PlaySound 函式
- PlaySound 函式，關於
- sndPlaySound 函式
- PlaySound 函式，相較于 sndPlaySound 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5723b1937c974e6c622c1f2010e8d2129e787cdd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104185612"
---
# <a name="the-playsound-function"></a><span data-ttu-id="b516d-109">PlaySound 函式</span><span class="sxs-lookup"><span data-stu-id="b516d-109">The PlaySound Function</span></span>

<span data-ttu-id="b516d-110">如果音效符合可用記憶體，您可以使用 [**PlaySound**](/previous-versions//dd743680(v=vs.85)) 函式來播放波形音訊。</span><span class="sxs-lookup"><span data-stu-id="b516d-110">You can use the [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function to play waveform audio if the sound fits into available memory.</span></span> <span data-ttu-id="b516d-111"> ([**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) 函式會提供 PlaySound 功能的子集。</span><span class="sxs-lookup"><span data-stu-id="b516d-111">(The [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) function offers a subset of the capabilities of PlaySound.</span></span> <span data-ttu-id="b516d-112">若要最大化 Win32 應用程式的可攜性，請使用 **PlaySound**，而不是 **sndPlaySound**。 ) </span><span class="sxs-lookup"><span data-stu-id="b516d-112">To maximize the portability of your Win32-based application, use **PlaySound**, not **sndPlaySound**.)</span></span>

<span data-ttu-id="b516d-113">**PlaySound** 函數可讓您以下列三種方式之一來指定音效：</span><span class="sxs-lookup"><span data-stu-id="b516d-113">The **PlaySound** function allows you to specify a sound in one of three ways:</span></span>

-   <span data-ttu-id="b516d-114">作為系統警示，使用儲存在 WIN.INI 檔案或登錄中的別名</span><span class="sxs-lookup"><span data-stu-id="b516d-114">As a system alert, using the alias stored in the WIN.INI file or the registry</span></span>
-   <span data-ttu-id="b516d-115">作為檔案名</span><span class="sxs-lookup"><span data-stu-id="b516d-115">As a filename</span></span>
-   <span data-ttu-id="b516d-116">作為資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b516d-116">As a resource identifier</span></span>

<span data-ttu-id="b516d-117">[**PlaySound**](/previous-versions//dd743680(v=vs.85))函式可讓您在連續迴圈中播放音效，只有當您再次呼叫 **PlaySound** 時，才會結束，指定 *pszSound* 參數的另一個音效的 **Null** 或音效識別碼。</span><span class="sxs-lookup"><span data-stu-id="b516d-117">The [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function allows you to play a sound in a continuous loop, ending only when you call **PlaySound** again, specifying either **NULL** or the sound identifier of another sound for the *pszSound* parameter.</span></span>

<span data-ttu-id="b516d-118">您可以使用 **PlaySound** 以同步或非同步方式播放音效，並以其他方式控制函式的行為（當它必須共用系統資源時）。</span><span class="sxs-lookup"><span data-stu-id="b516d-118">You can use **PlaySound** to play the sound synchronously or asynchronously, and to control the behavior of the function in other ways when it must share system resources.</span></span>

<span data-ttu-id="b516d-119">如需有關使用 PlaySound 的詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="b516d-119">For more information about using PlaySound, see the following topics:</span></span>

-   [<span data-ttu-id="b516d-120">使用 PlaySound 來播放 Waveform-Audio 檔案</span><span class="sxs-lookup"><span data-stu-id="b516d-120">Using PlaySound to Play Waveform-Audio Files</span></span>](using-playsound-to-play-waveform-audio-files.md)
-   [<span data-ttu-id="b516d-121">使用 PlaySound 來迴圈聲音</span><span class="sxs-lookup"><span data-stu-id="b516d-121">Using PlaySound to Loop Sounds</span></span>](using-playsound-to-loop-sounds.md)
-   [<span data-ttu-id="b516d-122">使用 PlaySound 來播放系統音效</span><span class="sxs-lookup"><span data-stu-id="b516d-122">Using PlaySound to Play System Sounds</span></span>](using-playsound-to-play-system-sounds.md)

<span data-ttu-id="b516d-123">如需有關如何在 Win32 應用程式中使用 **PlaySound** 的更多範例，請參閱 [播放 WAVE 資源](playing-wave-resources.md)。</span><span class="sxs-lookup"><span data-stu-id="b516d-123">For more examples of how to use **PlaySound** in your Win32-based applications, see [Playing WAVE Resources](playing-wave-resources.md).</span></span>

 

 
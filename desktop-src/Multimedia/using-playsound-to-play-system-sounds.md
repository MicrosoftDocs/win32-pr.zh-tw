---
title: 使用 PlaySound 來播放系統音效
description: 使用 PlaySound 來播放系統音效
ms.assetid: b645c488-8b76-4886-8909-75f0342263db
keywords:
- 波形音訊，PlaySound 函式
- 波形音訊，播放系統音效
- 波形音訊、音效事件
- PlaySound 函式，播放系統音效
- PlaySound 函式，音效事件
- 播放波形-音訊系統音效
- 音效活動
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1940ee9f207213c4337c9b6bb0a0d58b0f471000
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842284"
---
# <a name="using-playsound-to-play-system-sounds"></a><span data-ttu-id="2e1c7-110">使用 PlaySound 來播放系統音效</span><span class="sxs-lookup"><span data-stu-id="2e1c7-110">Using PlaySound to Play System Sounds</span></span>

<span data-ttu-id="2e1c7-111">[**PlaySound**](/previous-versions//dd743680(v=vs.85))函式也會播放登錄中的 keyname 所參考的聲音。</span><span class="sxs-lookup"><span data-stu-id="2e1c7-111">The [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function will also play sounds referred to by a keyname in the registry.</span></span> <span data-ttu-id="2e1c7-112">使用者可以將自己的音效指派給系統警示和警告，或指派給使用者動作，例如按一下滑鼠按鍵。</span><span class="sxs-lookup"><span data-stu-id="2e1c7-112">Users can assign their own sounds to system alerts and warnings, or to user actions, such as a mouse button click.</span></span> <span data-ttu-id="2e1c7-113">與系統警示和警告相關的音效稱為「 *音效事件*」。</span><span class="sxs-lookup"><span data-stu-id="2e1c7-113">Sounds that are associated with system alerts and warnings are called *sound events*.</span></span>

<span data-ttu-id="2e1c7-114">若要播放音效事件，請呼叫 **PlaySound** ，並將 *pszSound* 參數指向包含可識別音效之登錄專案名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="2e1c7-114">To play a sound event, call **PlaySound** with the *pszSound* parameter pointing to a string containing the name of the registry entry that identifies the sound.</span></span> <span data-ttu-id="2e1c7-115">例如，若要播放與 "MouseClick" 專案相關的音效，並等候音效完成後再返回，請使用下列語句：</span><span class="sxs-lookup"><span data-stu-id="2e1c7-115">For example, to play the sound associated with the "MouseClick" entry and to wait for the sound to complete before returning, use the following statement:</span></span>


```C++
PlaySound("MouseClick", NULL, SND_SYNC); 
```



<span data-ttu-id="2e1c7-116">如果指定的登錄專案或其識別的波形音訊檔案不存在，或檔案無法放入可用的記憶體中， **PlaySound** 會播放預設的系統音效。</span><span class="sxs-lookup"><span data-stu-id="2e1c7-116">If the specified registry entry or the waveform-audio file it identifies does not exist, or if the file does not fit into the available memory, **PlaySound** plays the default system sound.</span></span>

<span data-ttu-id="2e1c7-117">系統預先定義的音效事件可能會因平臺而異。</span><span class="sxs-lookup"><span data-stu-id="2e1c7-117">The sound events that are predefined by the system can vary with the platform.</span></span> <span data-ttu-id="2e1c7-118">下列清單提供針對 WIN32 API 的所有執行所定義的音效事件：</span><span class="sxs-lookup"><span data-stu-id="2e1c7-118">The following list gives the sound events that are defined for all implementations of the Win32 API:</span></span>

-   <span data-ttu-id="2e1c7-119">SystemAsterisk</span><span class="sxs-lookup"><span data-stu-id="2e1c7-119">SystemAsterisk</span></span>
-   <span data-ttu-id="2e1c7-120">SystemExclamation</span><span class="sxs-lookup"><span data-stu-id="2e1c7-120">SystemExclamation</span></span>
-   <span data-ttu-id="2e1c7-121">發生 systemexit 時</span><span class="sxs-lookup"><span data-stu-id="2e1c7-121">SystemExit</span></span>
-   <span data-ttu-id="2e1c7-122">SystemHand</span><span class="sxs-lookup"><span data-stu-id="2e1c7-122">SystemHand</span></span>
-   <span data-ttu-id="2e1c7-123">SystemQuestion</span><span class="sxs-lookup"><span data-stu-id="2e1c7-123">SystemQuestion</span></span>
-   <span data-ttu-id="2e1c7-124">SystemStart</span><span class="sxs-lookup"><span data-stu-id="2e1c7-124">SystemStart</span></span>

<span data-ttu-id="2e1c7-125">如果應用程式註冊自己的音效事件，則使用者可以使用標準主控台介面設定音效事件。</span><span class="sxs-lookup"><span data-stu-id="2e1c7-125">If an application registers its own sound events, the user can configure the sound event by using the standard Control Panel interface.</span></span> <span data-ttu-id="2e1c7-126">應用程式應該使用標準登錄函式來註冊音效事件;如需詳細資訊，請參閱 [Registry](../sysinfo/registry.md)。</span><span class="sxs-lookup"><span data-stu-id="2e1c7-126">The application should register the sound event by using the standard registry functions; for more information, see [Registry](../sysinfo/registry.md).</span></span> <span data-ttu-id="2e1c7-127">專案與其余的音效事件位於登錄階層中的相同位置。</span><span class="sxs-lookup"><span data-stu-id="2e1c7-127">The entries belong at the same position in the registry hierarchy as the rest of the sound events.</span></span> <span data-ttu-id="2e1c7-128">這個位置會隨著 Win32 的執行而不同。</span><span class="sxs-lookup"><span data-stu-id="2e1c7-128">This position varies with the Win32 implementation.</span></span> <span data-ttu-id="2e1c7-129">適當的資料值也會隨著執行而有所不同。</span><span class="sxs-lookup"><span data-stu-id="2e1c7-129">The appropriate data value also varies with the implementation.</span></span>

<span data-ttu-id="2e1c7-130">在嘗試載入具有這個名稱的檔案之前， [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) 函式一律會在登錄中搜尋符合 *lpszSound* 的 keyname。</span><span class="sxs-lookup"><span data-stu-id="2e1c7-130">The [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) function always searches the registry for a keyname matching *lpszSound* before attempting to load a file with this name.</span></span> <span data-ttu-id="2e1c7-131">[**PlaySound**](/previous-versions//dd743680(v=vs.85))函式會接受指定音效位置的旗標。</span><span class="sxs-lookup"><span data-stu-id="2e1c7-131">The [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function accepts flags that specify the location of the sound.</span></span>

 

 
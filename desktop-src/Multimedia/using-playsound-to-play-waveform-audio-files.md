---
title: 使用 PlaySound 來播放 Waveform-Audio 檔案
description: 使用 PlaySound 來播放 Waveform-Audio 檔案
ms.assetid: 8b7d191b-6b0c-4dff-84de-cb3a5c314b80
keywords:
- 波形音訊，PlaySound 函式
- 波形音訊，播放檔案
- 波形音訊、WAV 副檔名
- PlaySound 函式，播放波形-音訊檔案
- 播放波形-音訊檔案，PlaySound 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9d5dde46827b7892217f760c749e75e19f368f5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933232"
---
# <a name="using-playsound-to-play-waveform-audio-files"></a><span data-ttu-id="9c129-108">使用 PlaySound 來播放 Waveform-Audio 檔案</span><span class="sxs-lookup"><span data-stu-id="9c129-108">Using PlaySound to Play Waveform-Audio Files</span></span>

<span data-ttu-id="9c129-109">大部分的波形音訊檔案都使用。WAV 副檔名。</span><span class="sxs-lookup"><span data-stu-id="9c129-109">Most waveform-audio files use the .WAV filename extension.</span></span>

<span data-ttu-id="9c129-110">下列語句會播放 C：音效 \\ \\ 功能對。WAV 檔：</span><span class="sxs-lookup"><span data-stu-id="9c129-110">The following statement plays the C:\\SOUNDS\\BELLS.WAV file:</span></span>


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_SYNC); 
```



<span data-ttu-id="9c129-111">如果指定的檔案不存在，或檔案無法放入可用的記憶體中， [**PlaySound**](/previous-versions//dd743680(v=vs.85)) 會播放預設的系統音效。</span><span class="sxs-lookup"><span data-stu-id="9c129-111">If the specified file does not exist, or if the file does not fit into the available memory, [**PlaySound**](/previous-versions//dd743680(v=vs.85)) plays the default system sound.</span></span> <span data-ttu-id="9c129-112">如果未定義任何預設系統音效， **PlaySound** 會失敗，而不會產生任何音效。</span><span class="sxs-lookup"><span data-stu-id="9c129-112">If no default system sound has been defined, **PlaySound** fails without producing any sound.</span></span> <span data-ttu-id="9c129-113">如果您不想讓預設系統音效播放，請指定 OPERATORS.SND \_ NODEFAULT 旗標，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="9c129-113">If you do not want the default system sound to play, specify the SND\_NODEFAULT flag, as shown in the following example:</span></span>


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_SYNC | SND_NODEFAULT); 
```



 

 
---
description: 本主題說明如何使用來源語音上的 SetFrequencyRatio 函式變更播放速率來提高或降低音訊資料的音調。
ms.assetid: 93408116-1c1f-307f-7e1f-090f2663ff0b
title: 如何：變更聲音音調
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7143dda30eae48bd8ed966c4170da2884d2633ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113656"
---
# <a name="how-to-change-voice-pitch"></a><span data-ttu-id="044bf-103">如何：變更聲音音調</span><span class="sxs-lookup"><span data-stu-id="044bf-103">How to: Change Voice Pitch</span></span>

<span data-ttu-id="044bf-104">本主題說明如何使用來源語音上的 [**SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) 函式變更播放速率來提高或降低音訊資料的音調。</span><span class="sxs-lookup"><span data-stu-id="044bf-104">This topic shows you how you can raise or lower the pitch of audio data by changing its rate of playback using the [**SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) function on a source voice.</span></span>

## <a name="to-change-the-pitch-of-a-source-voice"></a><span data-ttu-id="044bf-105">變更來源聲音的音調</span><span class="sxs-lookup"><span data-stu-id="044bf-105">To change the pitch of a source voice</span></span>

1.  <span data-ttu-id="044bf-106">判斷 [**來源語音**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)所需的頻率比例。</span><span class="sxs-lookup"><span data-stu-id="044bf-106">Determine the desired frequency ratio for the [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice).</span></span>

    <span data-ttu-id="044bf-107">如需計算頻率比例的詳細資訊，請參閱 [XAudio2 音量和音調控制](xaudio2-volume-and-pitch-control.md) 。</span><span class="sxs-lookup"><span data-stu-id="044bf-107">See [XAudio2 Volume and Pitch Control](xaudio2-volume-and-pitch-control.md) for more information about calculating the frequency ratio.</span></span>

    ```
    float frequencyRatio = sourceRate / targetRate;
    ```

    

2.  <span data-ttu-id="044bf-108">使用 [**SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) 函式來設定來源聲音的頻率比例。</span><span class="sxs-lookup"><span data-stu-id="044bf-108">Use the [**SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) function to set the frequency ratio of the source voice.</span></span>

    ```
    pSourceVoice->SetFrequencyRatio(frequencyRatio);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="044bf-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="044bf-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="044bf-110">XAudio2 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="044bf-110">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="044bf-111">使用方法：建立基本音訊處理圖形</span><span class="sxs-lookup"><span data-stu-id="044bf-111">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="044bf-112">XAudio2 音量和音調控制</span><span class="sxs-lookup"><span data-stu-id="044bf-112">XAudio2 Volume and Pitch Control</span></span>](volume-and-pitch-control.md)
</dt> </dl>

 

 

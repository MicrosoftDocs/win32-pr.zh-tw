---
description: 您可以隨時變更音訊圖形，以新增或移除語音或整個 subgraphs。
ms.assetid: b2f9ec6a-4b5b-e618-759b-d7dbc0d97ac4
title: 使用方法：從音訊圖形動態新增或移除聲音
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdb26150b5614ec53e4cc4de5af74e9a14ee2a94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113652"
---
# <a name="how-to-dynamically-add-or-remove-voices-from-an-audio-graph"></a><span data-ttu-id="92e19-103">使用方法：從音訊圖形動態新增或移除聲音</span><span class="sxs-lookup"><span data-stu-id="92e19-103">How to: Dynamically Add or Remove Voices From an Audio Graph</span></span>

<span data-ttu-id="92e19-104">您可以隨時變更音訊圖形，以新增或移除語音或整個 subgraphs。</span><span class="sxs-lookup"><span data-stu-id="92e19-104">You can change audio graphs at any time to add or remove voices or entire subgraphs.</span></span> <span data-ttu-id="92e19-105">本主題說明如何在下列步驟中，新增或移除已依照 how [to：建立基本音訊處理圖形](how-to--build-a-basic-audio-processing-graph.md)中的步驟所建立的 submix 語音。</span><span class="sxs-lookup"><span data-stu-id="92e19-105">This topic shows you how to add or remove submix voices from a graph that has been created following the steps in [How to: Build a Basic Audio Processing Graph](how-to--build-a-basic-audio-processing-graph.md).</span></span> <span data-ttu-id="92e19-106">單一語音可以將其輸出傳送到數個聲音或一環長的聲音。</span><span class="sxs-lookup"><span data-stu-id="92e19-106">A single voice can send its output to several voices or to a long chain of voices.</span></span> <span data-ttu-id="92e19-107">移除或新增單一聲音可能會對音訊圖形產生很大的影響。</span><span class="sxs-lookup"><span data-stu-id="92e19-107">Removing or adding a single voice can have a large effect on an audio graph.</span></span>

## <a name="to-dynamically-change-an-audio-graph"></a><span data-ttu-id="92e19-108">動態變更音訊圖形</span><span class="sxs-lookup"><span data-stu-id="92e19-108">To dynamically change an audio graph</span></span>

<span data-ttu-id="92e19-109">從音訊圖形新增和移除語音，與從單一連結清單或圖形新增或移除節點非常類似。</span><span class="sxs-lookup"><span data-stu-id="92e19-109">Adding and removing voices from an audio graph is very similar to adding or removing nodes from a single-linked list or graph.</span></span>

-   <span data-ttu-id="92e19-110">將語音或性子圖形新增至音訊圖形</span><span class="sxs-lookup"><span data-stu-id="92e19-110">To add a voice or subgraph to an audio graph</span></span>

    <span data-ttu-id="92e19-111">使用 [**SetOutputVoices**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputvoices) 函式將圖形中的聲音輸出（父語音）設定為要新增的聲音。</span><span class="sxs-lookup"><span data-stu-id="92e19-111">Set the output of a voice in the graph, the parent voice, to the voice to be added using the [**SetOutputVoices**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputvoices) function.</span></span> <span data-ttu-id="92e19-112">將新聲音的輸出設定為父系聲音的原始子系。</span><span class="sxs-lookup"><span data-stu-id="92e19-112">Set the output of the new voice to the original child of the parent voice.</span></span>

    ```
    XAUDIO2_SEND_DESCRIPTOR send = {0, pNewVoice};
    XAUDIO2_VOICE_SENDS sendlist = {1, &send};
    pParentVoice->SetOutputVoices(&sendlist);
    send.pOutputVoice = pChildVoice;
    pNewVoice->SetOutputVoices(&sendlist);
    ```

    

-   <span data-ttu-id="92e19-113">移除音訊圖形中的聲音或性子圖形</span><span class="sxs-lookup"><span data-stu-id="92e19-113">To remove a voice or subgraph from an audio graph</span></span>

    <span data-ttu-id="92e19-114">將正在移除的聲音父系的輸出聲音設定為已移除的聲音子系。</span><span class="sxs-lookup"><span data-stu-id="92e19-114">Set the output voice of the parent of the voice being removed to the child of the voice being removed.</span></span> <span data-ttu-id="92e19-115">如果要移除的聲音是在圖形的結尾，則應該將父系聲音變更為指向主要語音。</span><span class="sxs-lookup"><span data-stu-id="92e19-115">If the voice being removed is at the end of the graph, the parent voice should be changed to point to the master voice.</span></span>

    ```
    XAUDIO2_SEND_DESCRIPTOR send = {0, pChildVoice};
    XAUDIO2_VOICE_SENDS sendlist = {1, &send};
    pParentVoice->SetOutputVoices(&sendlist);
    ```

    

<span data-ttu-id="92e19-116">請注意，為了清楚起見，每個父系在這些範例中只有一個子系。</span><span class="sxs-lookup"><span data-stu-id="92e19-116">Note that for clarity each parent only has one child in these examples.</span></span> <span data-ttu-id="92e19-117">如果父節點有多個子節點，它的 sendlist 會包含一組語音，而不是只包含一個語音的指標。</span><span class="sxs-lookup"><span data-stu-id="92e19-117">If a parent node has multiple children, its sendlist will contain an array of voices instead of a pointer to just one voice.</span></span>

## <a name="related-topics"></a><span data-ttu-id="92e19-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="92e19-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92e19-119">音訊圖形</span><span class="sxs-lookup"><span data-stu-id="92e19-119">Audio Graphs</span></span>](audio-graphs.md)
</dt> <dt>

[<span data-ttu-id="92e19-120">XAudio2 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="92e19-120">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="92e19-121">使用方法：建立基本音訊處理圖形</span><span class="sxs-lookup"><span data-stu-id="92e19-121">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="92e19-122">使用方法：使用次混音聲音</span><span class="sxs-lookup"><span data-stu-id="92e19-122">How to: Use Submix Voices</span></span>](how-to--use-submix-voices.md)
</dt> <dt>

[<span data-ttu-id="92e19-123">使用方法：建立效果鏈</span><span class="sxs-lookup"><span data-stu-id="92e19-123">How to: Create an Effect Chain</span></span>](how-to--create-an-effect-chain.md)
</dt> </dl>

 

 

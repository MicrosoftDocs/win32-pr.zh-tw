---
description: 所有語音的組合（包含其內含效果和其相互連線）稱為音訊處理圖形。
ms.assetid: 4fa45dbf-3811-c91c-7561-3b896e9e1f03
title: XAudio2 音訊圖形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eb265bd6bc2547acd04ca41cceb58ad12896fbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195300"
---
# <a name="xaudio2-audio-graph"></a><span data-ttu-id="bf9fc-103">XAudio2 音訊圖形</span><span class="sxs-lookup"><span data-stu-id="bf9fc-103">XAudio2 Audio Graph</span></span>

<span data-ttu-id="bf9fc-104">所有語音的組合（包含其內含效果和其相互連線）稱為音訊處理圖形。</span><span class="sxs-lookup"><span data-stu-id="bf9fc-104">The set of all voices, with their contained effects and their interconnections, is referred to as the audio processing graph.</span></span> <span data-ttu-id="bf9fc-105">圖形會接受來自用戶端的一組音訊串流作為輸入、進行處理，並將最終結果傳遞給音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="bf9fc-105">The graph takes a set of audio streams from the client as input, processes them, and delivers the final result to an audio device.</span></span> <span data-ttu-id="bf9fc-106">所有音訊處理都是在不同的執行緒中進行，而且其週期性是由圖形的量子所定義 (目前在 Microsoft Windows 上為10毫秒，Xbox 360) 則為 5 1/3 毫秒。</span><span class="sxs-lookup"><span data-stu-id="bf9fc-106">All audio processing takes place in a separate thread with a periodicity defined by the graph's quantum (currently 10 milliseconds on Microsoft Windows, and 5 1/3 milliseconds on Xbox 360).</span></span> <span data-ttu-id="bf9fc-107">在每個量子毫秒，執行緒會透過整個圖形喚醒和 disperses 音訊資料的量子毫秒。</span><span class="sxs-lookup"><span data-stu-id="bf9fc-107">Every quantum milliseconds, the thread wakes up and disperses quantum milliseconds of audio data through the entire graph.</span></span> <span data-ttu-id="bf9fc-108">如需建立基本音訊圖形的範例，請參閱 how to： [建立基本音訊處理圖形](how-to--build-a-basic-audio-processing-graph.md)。</span><span class="sxs-lookup"><span data-stu-id="bf9fc-108">For an example of building a basic audio graph, see How to: [Build a Basic Audio Processing Graph](how-to--build-a-basic-audio-processing-graph.md).</span></span>

<span data-ttu-id="bf9fc-109">簡單的音訊圖形：</span><span class="sxs-lookup"><span data-stu-id="bf9fc-109">A simple audio graph:</span></span>

![簡單的音訊圖形](images/xaudio2-audio-graph.png)

<span data-ttu-id="bf9fc-111">用戶端可以在執行時動態控制圖形的狀態。</span><span class="sxs-lookup"><span data-stu-id="bf9fc-111">The client can control the graph's state dynamically while it is running.</span></span> <span data-ttu-id="bf9fc-112">控制動作可能包括新增和移除輸入和輸出、變更內部效果和互相連線、設定效果的參數、啟用和停用圖形的元件等等。</span><span class="sxs-lookup"><span data-stu-id="bf9fc-112">Control actions might include adding and removing inputs and outputs, changing the internal effects and interconnections, setting parameters on the effects, enabling and disabling parts of the graph, and so on.</span></span> <span data-ttu-id="bf9fc-113">如需動態變更音訊圖形的範例，請參閱 [如何：以動態方式新增或移除音訊圖形中的聲音](how-to--dynamically-add-or-remove-voices-from-an-audio-graph.md)。</span><span class="sxs-lookup"><span data-stu-id="bf9fc-113">For an example of dynamically changing an audio graph, see [How to: Dynamically Add or Remove Voices From an Audio Graph](how-to--dynamically-add-or-remove-voices-from-an-audio-graph.md).</span></span>

## <a name="processing-the-graph"></a><span data-ttu-id="bf9fc-114">處理圖形</span><span class="sxs-lookup"><span data-stu-id="bf9fc-114">Processing the Graph</span></span>

<span data-ttu-id="bf9fc-115">任何會影響圖形中任何物件的方法呼叫都會被視為影響圖形狀態變更。</span><span class="sxs-lookup"><span data-stu-id="bf9fc-115">Any method call that affects any object in the graph is considered to be effecting a graph state change.</span></span> <span data-ttu-id="bf9fc-116">圖形狀態變更包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="bf9fc-116">Graph state changes include the following:</span></span>

-   <span data-ttu-id="bf9fc-117">建立和終結語音</span><span class="sxs-lookup"><span data-stu-id="bf9fc-117">Creating and destroying voices</span></span>
-   <span data-ttu-id="bf9fc-118">啟動或停止語音</span><span class="sxs-lookup"><span data-stu-id="bf9fc-118">Starting or stopping voices</span></span>
-   <span data-ttu-id="bf9fc-119">變更聲音的目的地</span><span class="sxs-lookup"><span data-stu-id="bf9fc-119">Changing the destinations of a voice</span></span>
-   <span data-ttu-id="bf9fc-120">修改效果鏈</span><span class="sxs-lookup"><span data-stu-id="bf9fc-120">Modifying effect chains</span></span>
-   <span data-ttu-id="bf9fc-121">啟用或停用效果</span><span class="sxs-lookup"><span data-stu-id="bf9fc-121">Enabling or disabling effects</span></span>
-   <span data-ttu-id="bf9fc-122">設定效果或內建 SRCs、篩選、磁片區和 mixers 的參數</span><span class="sxs-lookup"><span data-stu-id="bf9fc-122">Setting parameters on the effects or on the built-in SRCs, filters, volumes, and mixers</span></span>

<span data-ttu-id="bf9fc-123">任何一組圖形狀態變更都可以合併並執行為不可部分完成的交易。</span><span class="sxs-lookup"><span data-stu-id="bf9fc-123">Any set of graph state changes can be combined and performed as an atomic transaction.</span></span> <span data-ttu-id="bf9fc-124">這些不可部分完成的作業稱為操作集。</span><span class="sxs-lookup"><span data-stu-id="bf9fc-124">These atomic operations are known as operation sets.</span></span> <span data-ttu-id="bf9fc-125">它們會在 XAudio2 作業 [集](xaudio2-operation-sets.md) 總覽中討論。</span><span class="sxs-lookup"><span data-stu-id="bf9fc-125">They are discussed in the [XAudio2 Operation Sets](xaudio2-operation-sets.md) overview.</span></span>

## <a name="internal-data-representation"></a><span data-ttu-id="bf9fc-126">內部資料表示</span><span class="sxs-lookup"><span data-stu-id="bf9fc-126">Internal Data Representation</span></span>

<span data-ttu-id="bf9fc-127">XAudio2 圖內的音訊資料一律會以32位浮點 PCM 形式儲存和處理。</span><span class="sxs-lookup"><span data-stu-id="bf9fc-127">Audio data within the XAudio2 graph is always stored and processed in 32-bit floating-point PCM form.</span></span> <span data-ttu-id="bf9fc-128">不過，圖表內的頻道計數和取樣率可能會有所不同。</span><span class="sxs-lookup"><span data-stu-id="bf9fc-128">However, the channel count and sample rate can vary within the graph.</span></span> <span data-ttu-id="bf9fc-129">指定語音處理音訊的格式是由用來建立語音的語音類型和參數所決定。</span><span class="sxs-lookup"><span data-stu-id="bf9fc-129">The format in which a given voice processes audio is determined by the voice type and parameters used to create the voice.</span></span>



| <span data-ttu-id="bf9fc-130">語音類型</span><span class="sxs-lookup"><span data-stu-id="bf9fc-130">Voice Type</span></span>                                                                                                      | <span data-ttu-id="bf9fc-131">參數</span><span class="sxs-lookup"><span data-stu-id="bf9fc-131">Parameters</span></span>                                                                                     |
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bf9fc-132">**IXAudio2SourceVoice**</span><span class="sxs-lookup"><span data-stu-id="bf9fc-132">**IXAudio2SourceVoice**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)                                                              | <span data-ttu-id="bf9fc-133">來源聲音傳送音訊的語音聲道計數和取樣率。</span><span class="sxs-lookup"><span data-stu-id="bf9fc-133">The channel count and sample rate of the voices to which the source voice sends audio.</span></span>         |
| <span data-ttu-id="bf9fc-134">[**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)和 [ **IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)</span><span class="sxs-lookup"><span data-stu-id="bf9fc-134">[**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) and [**IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)</span></span> | <span data-ttu-id="bf9fc-135">用來建立 submix/主控聲音的 *InputChannels* 和 *InputSampleRate* 引數。</span><span class="sxs-lookup"><span data-stu-id="bf9fc-135">The *InputChannels* and *InputSampleRate* arguments used to create the submix/mastering voice.</span></span> |



 

## <a name="format-conversion"></a><span data-ttu-id="bf9fc-136">格式轉換</span><span class="sxs-lookup"><span data-stu-id="bf9fc-136">Format Conversion</span></span>

<span data-ttu-id="bf9fc-137">XAudio2 會處理音訊從某個語音傳送到另一個語音時所需的任何取樣率或通道轉換，但有下列限制：</span><span class="sxs-lookup"><span data-stu-id="bf9fc-137">XAudio2 handles any sample rate or channel conversions that are required as audio travels from one voice to another, with the following limitations:</span></span>

-   <span data-ttu-id="bf9fc-138">特定語音的所有目的地語音都必須以相同的取樣率執行</span><span class="sxs-lookup"><span data-stu-id="bf9fc-138">All destination voices for a particular voice must be running at the same sample rate</span></span>
-   <span data-ttu-id="bf9fc-139">效果鏈中的效果可能會變更音訊的頻道計數，但不能變更其取樣率</span><span class="sxs-lookup"><span data-stu-id="bf9fc-139">Effects in an effect chain can change the audio's channel count, but not its sample rate</span></span>
-   <span data-ttu-id="bf9fc-140">效果鏈的輸出通道計數必須符合其傳送的聲音</span><span class="sxs-lookup"><span data-stu-id="bf9fc-140">An effect chain's output channel count must match that of the voices to which it sends</span></span>
-   <span data-ttu-id="bf9fc-141">無法進行動態圖形變更，因此會中斷上述規則</span><span class="sxs-lookup"><span data-stu-id="bf9fc-141">No dynamic graph change can be made which would break the rules above</span></span>

<span data-ttu-id="bf9fc-142">在輸入端，來源語音可以讀取任何有效 PCM 格式的資料，或是 XAudio2 所支援的任何壓縮格式的資料。</span><span class="sxs-lookup"><span data-stu-id="bf9fc-142">On the input side, source voices can read data in any valid PCM format, or in any of the compressed formats supported by XAudio2.</span></span> <span data-ttu-id="bf9fc-143">如果輸入資料已壓縮，則會先將其解碼為浮點 PCM，再進行任何進一步的處理。</span><span class="sxs-lookup"><span data-stu-id="bf9fc-143">If the input data is compressed, it is decoded to floating-point PCM before any further processing is done.</span></span>

<span data-ttu-id="bf9fc-144">在輸出端，主控語音只能產生 PCM 資料。</span><span class="sxs-lookup"><span data-stu-id="bf9fc-144">On the output side, mastering voices can only produce PCM data.</span></span> <span data-ttu-id="bf9fc-145">這種資料一律會滿足上述對輸入 PCM 資料所述的相同限制。</span><span class="sxs-lookup"><span data-stu-id="bf9fc-145">This data will always satisfy the same restrictions described above for input PCM data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf9fc-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="bf9fc-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf9fc-147">音訊圖形</span><span class="sxs-lookup"><span data-stu-id="bf9fc-147">Audio Graphs</span></span>](audio-graphs.md)
</dt> <dt>

[<span data-ttu-id="bf9fc-148">XAudio2 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="bf9fc-148">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="bf9fc-149">使用方法：建立基本音訊處理圖形</span><span class="sxs-lookup"><span data-stu-id="bf9fc-149">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="bf9fc-150">使用方法：從音訊圖形動態新增或移除聲音</span><span class="sxs-lookup"><span data-stu-id="bf9fc-150">How to: Dynamically Add or Remove Voices From an Audio Graph</span></span>](how-to--dynamically-add-or-remove-voices-from-an-audio-graph.md)
</dt> <dt>

[<span data-ttu-id="bf9fc-151">使用方法：使用次混音聲音</span><span class="sxs-lookup"><span data-stu-id="bf9fc-151">How to: Use Submix Voices</span></span>](how-to--use-submix-voices.md)
</dt> <dt>

[<span data-ttu-id="bf9fc-152">使用方法：建立效果鏈</span><span class="sxs-lookup"><span data-stu-id="bf9fc-152">How to: Create an Effect Chain</span></span>](how-to--create-an-effect-chain.md)
</dt> </dl>

 

 




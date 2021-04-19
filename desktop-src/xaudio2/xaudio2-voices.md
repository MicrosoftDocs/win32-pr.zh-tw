---
description: 有三種類型的 XAudio2 語音物件：來源、submix 和主控語音。
ms.assetid: 3a4acc03-e47a-ff33-dee8-a374051f85f6
title: XAudio2 聲音
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b11300cea770f59485e8a78b0d30110b5469befe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980026"
---
# <a name="xaudio2-voices"></a><span data-ttu-id="8d096-103">XAudio2 聲音</span><span class="sxs-lookup"><span data-stu-id="8d096-103">XAudio2 Voices</span></span>

<span data-ttu-id="8d096-104">有三種類型的 XAudio2 語音物件： *來源*、 *submix* 和 *主控* 語音。</span><span class="sxs-lookup"><span data-stu-id="8d096-104">There are three types of XAudio2 voice objects: *source*, *submix*, and *mastering* voices.</span></span> <span data-ttu-id="8d096-105">來源聲音在用戶端提供的音訊資料上操作。</span><span class="sxs-lookup"><span data-stu-id="8d096-105">Source voices operate on audio data provided by the client.</span></span> <span data-ttu-id="8d096-106">來源和次混音聲音會將它們的輸出傳送到一或多個次混音或主播放聲音。</span><span class="sxs-lookup"><span data-stu-id="8d096-106">Source and submix voices send their output to one or more submix or mastering voices.</span></span> <span data-ttu-id="8d096-107">次混音和主播放聲音會將傳入的所有聲音的音訊混合在一起，然後在結果上操作。</span><span class="sxs-lookup"><span data-stu-id="8d096-107">Submix and mastering voices mix the audio from all voices feeding them, and operate on the result.</span></span> <span data-ttu-id="8d096-108">主播放聲音會將音訊資料寫入音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="8d096-108">Mastering voices write audio data to an audio device.</span></span>

## <a name="actions-performed-by-all-voices"></a><span data-ttu-id="8d096-109">所有語音執行的動作</span><span class="sxs-lookup"><span data-stu-id="8d096-109">Actions Performed by All Voices</span></span>

<span data-ttu-id="8d096-110">所有語音都會在移動時的音訊上依序執行下列動作。</span><span class="sxs-lookup"><span data-stu-id="8d096-110">All voices perform the following actions in order on the audio that travels though them.</span></span>

1.  <span data-ttu-id="8d096-111">整體磁片區調整，會影響所有音訊頻道。</span><span class="sxs-lookup"><span data-stu-id="8d096-111">Overall volume adjustment, affecting all audio channels.</span></span> <span data-ttu-id="8d096-112">請參閱 [**IXAudio2Voice：： SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume)。</span><span class="sxs-lookup"><span data-stu-id="8d096-112">See [**IXAudio2Voice::SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume).</span></span>
2.  <span data-ttu-id="8d096-113">一或多個 DSP 效果的選擇性用戶端指定鏈，例如內建的回音或 [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) 介面所定義的使用者效果。</span><span class="sxs-lookup"><span data-stu-id="8d096-113">An optional client-specified chain of one or more DSP effects, such as the built-in reverb or a user effect defined by the [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) interface.</span></span> <span data-ttu-id="8d096-114">請參閱 [XAudio2 音訊效果](xaudio2-audio-effects.md)。</span><span class="sxs-lookup"><span data-stu-id="8d096-114">See [XAudio2 Audio Effects](xaudio2-audio-effects.md).</span></span>
3.  <span data-ttu-id="8d096-115">每個通道的輸出磁片區調整。</span><span class="sxs-lookup"><span data-stu-id="8d096-115">Per-channel output volume adjustment.</span></span> <span data-ttu-id="8d096-116">請參閱 [**IXAudio2Voice：： SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes)。</span><span class="sxs-lookup"><span data-stu-id="8d096-116">See [**IXAudio2Voice::SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes).</span></span>
4.  <span data-ttu-id="8d096-117">將矩陣混合到每個目的地語音或音訊輸出裝置，以取得語音。</span><span class="sxs-lookup"><span data-stu-id="8d096-117">Separate matrix mix to each of the destination voices or to the audio output device for mastering voices.</span></span> <span data-ttu-id="8d096-118">此混合會視需要變更音訊中的通道數目。</span><span class="sxs-lookup"><span data-stu-id="8d096-118">This mix changes the number of channels in the audio, if necessary.</span></span>

## <a name="source-voices"></a><span data-ttu-id="8d096-119">來源語音</span><span class="sxs-lookup"><span data-stu-id="8d096-119">Source Voices</span></span>

<span data-ttu-id="8d096-120">使用來源語音將音訊資料提交至 XAudio2 處理管線。</span><span class="sxs-lookup"><span data-stu-id="8d096-120">Use source voices to submit audio data into the XAudio2 processing pipeline.</span></span> <span data-ttu-id="8d096-121">它們是 [XAudio2 音訊圖形](xaudio2-audio-graph.md)的進入點。</span><span class="sxs-lookup"><span data-stu-id="8d096-121">They are the entry points into the [XAudio2 Audio Graph](xaudio2-audio-graph.md).</span></span> <span data-ttu-id="8d096-122">您必須直接或透過中繼 submix 語音，將語音資料傳送給要聽到的主控聲音。</span><span class="sxs-lookup"><span data-stu-id="8d096-122">You must send voice data to a mastering voice to be heard, either directly or through intermediate submix voices.</span></span>

<span data-ttu-id="8d096-123">除了所有語音執行的動作之外，來源語音也會執行下列動作。</span><span class="sxs-lookup"><span data-stu-id="8d096-123">In addition to the actions performed by all voices, source voices perform the following actions.</span></span>

-   <span data-ttu-id="8d096-124">必要時，會先執行一個解碼，將編碼的來源資料轉換成脈衝程式碼， (PCM) 。</span><span class="sxs-lookup"><span data-stu-id="8d096-124">If necessary, a decoder runs first to convert encoded source data to Pulse Code Modulation (PCM).</span></span>
-   <span data-ttu-id="8d096-125">可變速率的取樣率轉換 (SRC) 將語音的來源音訊資料轉換為目的地語音預期的取樣率（如有必要），也支援動態的音調變更。</span><span class="sxs-lookup"><span data-stu-id="8d096-125">A variable-rate sample rate conversion (SRC) converts the voice's source audio data to the sample rate expected by its destination voices, if necessary, and also supports dynamic pitch changes.</span></span>
-   <span data-ttu-id="8d096-126">您可以使用選擇性的狀態變數篩選器，以各種方式將音效色彩。</span><span class="sxs-lookup"><span data-stu-id="8d096-126">An optional state-variable filter can be used to color the sound in various ways.</span></span> <span data-ttu-id="8d096-127">請參閱 [**IXAudio2Voice：： SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters)。</span><span class="sxs-lookup"><span data-stu-id="8d096-127">See [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).</span></span>
-   <span data-ttu-id="8d096-128">選擇性篩選準則可以套用至語音的輸出。</span><span class="sxs-lookup"><span data-stu-id="8d096-128">An optional filter can be applied to the voice's outputs.</span></span> <span data-ttu-id="8d096-129">請參閱 [**IXAudio2Voice：： SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters)。</span><span class="sxs-lookup"><span data-stu-id="8d096-129">See [**IXAudio2Voice::SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).</span></span>

## <a name="submix-voices"></a><span data-ttu-id="8d096-130">Submix 語音</span><span class="sxs-lookup"><span data-stu-id="8d096-130">Submix Voices</span></span>

<span data-ttu-id="8d096-131">Submix 語音主要用於效能改進和效果處理。</span><span class="sxs-lookup"><span data-stu-id="8d096-131">A submix voice is used primarily for performance improvements and effects processing.</span></span> <span data-ttu-id="8d096-132">您無法將資料緩衝區直接提交至 submix 語音。</span><span class="sxs-lookup"><span data-stu-id="8d096-132">You cannot submit data buffers directly to submix voices.</span></span> <span data-ttu-id="8d096-133">除非您將它提交給「主控」聲音，否則它將不會有任何聲音。</span><span class="sxs-lookup"><span data-stu-id="8d096-133">It will not be audible unless you submit it to a mastering voice.</span></span> <span data-ttu-id="8d096-134">您可以使用 submix 語音來確保一組特定的語音資料會轉換成相同的格式，並在集體結果上處理特定的效果鏈。</span><span class="sxs-lookup"><span data-stu-id="8d096-134">You can use a submix voice to ensure that a particular set of voice data is converted to the same format and to have a particular effect chain processed on the collective result.</span></span>

<span data-ttu-id="8d096-135">除了所有語音執行的動作之外，submix 語音也會執行下列動作。</span><span class="sxs-lookup"><span data-stu-id="8d096-135">In addition to the actions performed by all voices, submix voices perform the following actions.</span></span>

-   <span data-ttu-id="8d096-136">如果有需要，固定速率的 SRC 會在聲音的輸出上執行，以將音訊轉換為目的地語音預期的取樣率。</span><span class="sxs-lookup"><span data-stu-id="8d096-136">A fixed-rate SRC runs on the voice's output, if necessary, to convert the audio to the sample rate expected by its destination voices.</span></span>
-   <span data-ttu-id="8d096-137">您可以使用選擇性的狀態變數篩選器，以各種方式將音效色彩。</span><span class="sxs-lookup"><span data-stu-id="8d096-137">An optional state-variable filter can be used to color the sound in various ways.</span></span> <span data-ttu-id="8d096-138">請參閱 [**IXAudio2Voice：： SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters)。</span><span class="sxs-lookup"><span data-stu-id="8d096-138">See [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).</span></span>
-   <span data-ttu-id="8d096-139">選擇性篩選準則可以套用至語音的輸出。</span><span class="sxs-lookup"><span data-stu-id="8d096-139">An optional filter can be applied to the voice's outputs.</span></span> <span data-ttu-id="8d096-140">請參閱 [**IXAudio2Voice：： SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters)。</span><span class="sxs-lookup"><span data-stu-id="8d096-140">See [**IXAudio2Voice::SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).</span></span>

## <a name="mastering-voices"></a><span data-ttu-id="8d096-141">主控語音</span><span class="sxs-lookup"><span data-stu-id="8d096-141">Mastering Voices</span></span>

<span data-ttu-id="8d096-142">使用主控語音來代表音訊輸出裝置。</span><span class="sxs-lookup"><span data-stu-id="8d096-142">Use a mastering voice to represent the audio output device.</span></span> <span data-ttu-id="8d096-143">您無法直接提交資料緩衝區來掌控聲音，但提交給其他類型語音的資料必須移至要聽到的主控聲音。</span><span class="sxs-lookup"><span data-stu-id="8d096-143">You cannot submit data buffers directly to mastering voices, but data submitted to other types of voices must go to a mastering voice to be heard.</span></span>

<span data-ttu-id="8d096-144">除了所有語音執行的動作之外，主控語音也會執行下列動作。</span><span class="sxs-lookup"><span data-stu-id="8d096-144">In addition to the actions performed by all voices, mastering voices perform the following actions.</span></span>

-   <span data-ttu-id="8d096-145">如果您使用音訊裝置不支援的明確 *InputSampleRate* 值來建立主控語音，則會使用固定速率的 SRC 來轉換成裝置所支援的最接近取樣率。</span><span class="sxs-lookup"><span data-stu-id="8d096-145">If you create the mastering voice with an explicit *InputSampleRate* value that is not supported by the audio device, a fixed-rate SRC is used to convert to the closest sample rate supported by the device.</span></span>
-   <span data-ttu-id="8d096-146">如果輸出裝置需要，請裁剪最終輸出音訊。</span><span class="sxs-lookup"><span data-stu-id="8d096-146">Clip the final output audio, if it is required by the output device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8d096-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="8d096-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d096-148">語音</span><span class="sxs-lookup"><span data-stu-id="8d096-148">Voices</span></span>](voices.md)
</dt> <dt>

[<span data-ttu-id="8d096-149">XAudio2 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="8d096-149">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="8d096-150">**IXAudio2SourceVoice**</span><span class="sxs-lookup"><span data-stu-id="8d096-150">**IXAudio2SourceVoice**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)
</dt> <dt>

[<span data-ttu-id="8d096-151">**IXAudio2SubmixVoice**</span><span class="sxs-lookup"><span data-stu-id="8d096-151">**IXAudio2SubmixVoice**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)
</dt> <dt>

[<span data-ttu-id="8d096-152">**IXAudio2MasteringVoice**</span><span class="sxs-lookup"><span data-stu-id="8d096-152">**IXAudio2MasteringVoice**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)
</dt> </dl>

 

 

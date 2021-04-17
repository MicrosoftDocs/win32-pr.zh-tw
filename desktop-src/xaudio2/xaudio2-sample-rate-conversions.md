---
description: 如果 XAudio2 語音的輸入取樣率與輸出語音的輸入取樣率不同，則可以執行自動取樣速率轉換。
ms.assetid: be34ce62-6552-45e2-a247-830ab55ea9ec
title: XAudio2 取樣率轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d437a45f9e896826bedc1418382fb257201722d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195296"
---
# <a name="xaudio2-sample-rate-conversions"></a><span data-ttu-id="548b6-103">XAudio2 取樣率轉換</span><span class="sxs-lookup"><span data-stu-id="548b6-103">XAudio2 Sample Rate Conversions</span></span>

<span data-ttu-id="548b6-104">如果 XAudio2 語音的輸入取樣率與輸出語音的輸入取樣率不同，則可以執行自動取樣速率轉換。</span><span class="sxs-lookup"><span data-stu-id="548b6-104">XAudio2 voices can perform automatic sample rate conversions if their input sample rate is different from the input sample rate of their output voices.</span></span>

<span data-ttu-id="548b6-105">取樣率轉換會遵循下列規則：</span><span class="sxs-lookup"><span data-stu-id="548b6-105">Sample rate conversions follow these rules:</span></span>

-   <span data-ttu-id="548b6-106">語音輸入取樣率已修正。</span><span class="sxs-lookup"><span data-stu-id="548b6-106">Voice input sample rate is fixed.</span></span>

    <span data-ttu-id="548b6-107">語音只能處理建立時所指定的輸入取樣率。</span><span class="sxs-lookup"><span data-stu-id="548b6-107">Voices can only handle the input sample rate specified when they were created.</span></span> <span data-ttu-id="548b6-108">針對精通 [**語音**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)和 [**submix 聲音**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)，輸入取樣率會以 [**IXAudio2：： CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice)和 [**IXAudio2：： CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice)函式的 *InputSampleRate* 引數來指定。</span><span class="sxs-lookup"><span data-stu-id="548b6-108">For [**mastering voices**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice) and [**submix voices**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice), the input sample rate is specified with the *InputSampleRate* argument to the [**IXAudio2::CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) and [**IXAudio2::CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice) functions.</span></span> <span data-ttu-id="548b6-109">針對來源語音，語音的輸入取樣率是由 [**IXAudio2：： CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) 函式的 pSourceFormat 引數所指定。</span><span class="sxs-lookup"><span data-stu-id="548b6-109">For source voices, the input sample rate of the voice is specified by the pSourceFormat argument to the [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) function.</span></span>

-   <span data-ttu-id="548b6-110">所有聲音的輸出語音都必須有相同的輸入取樣率。</span><span class="sxs-lookup"><span data-stu-id="548b6-110">All of a voice's output voices must have the same input sample rate.</span></span>

    <span data-ttu-id="548b6-111">語音可以從其輸入取樣率轉換成任何輸出取樣率，但所有聲音的輸出語音都必須具有相同的輸入取樣率。</span><span class="sxs-lookup"><span data-stu-id="548b6-111">Voices can convert from their input sample rate to any output sample rate, but all of the voice's output voices must have the same input sample rate.</span></span> <span data-ttu-id="548b6-112">例如，語音可以輸出到任何數目的語音，輸入取樣率為 22 kHz。</span><span class="sxs-lookup"><span data-stu-id="548b6-112">For example, a voice could output to any number of voices with an input sample rate of 22 kHz.</span></span> <span data-ttu-id="548b6-113">不過，如果相同的聲音有數個輸出語音，每個輸出都有不同的輸入取樣率，音訊圖形將會無效。</span><span class="sxs-lookup"><span data-stu-id="548b6-113">However, if that same voice had several output voices, each of which had a different input sample rate, the audio graph would not be valid.</span></span>

-   <span data-ttu-id="548b6-114">取樣率轉換處理只會在必要時進行。</span><span class="sxs-lookup"><span data-stu-id="548b6-114">Sample rate conversion processing only occurs when necessary.</span></span>

    <span data-ttu-id="548b6-115">將音訊資料轉換成不同的取樣率會產生更多處理額外負荷，因此最好避免使用。</span><span class="sxs-lookup"><span data-stu-id="548b6-115">Converting audio data to a different sample rate incurs more processing overhead, which it is preferable to avoid.</span></span> <span data-ttu-id="548b6-116">如果語音的輸入取樣率符合輸出語音的輸入取樣率，則不會進行這項轉換，而且會縮短處理時間。</span><span class="sxs-lookup"><span data-stu-id="548b6-116">If a voice's input sample rate matches the input sample rate of its output voices, this conversion is not done and processing time is shortened.</span></span>

-   <span data-ttu-id="548b6-117">輸出取樣率可能會隨著聲音的存留期而改變。</span><span class="sxs-lookup"><span data-stu-id="548b6-117">Output sample rate can vary over the life of a voice.</span></span>

    <span data-ttu-id="548b6-118">語音的輸出取樣率不是固定的。</span><span class="sxs-lookup"><span data-stu-id="548b6-118">The output sample rate of a voice is not fixed.</span></span> <span data-ttu-id="548b6-119">只要其所有輸出語音都有相同的輸入取樣率，音訊圖表就會是有效的。</span><span class="sxs-lookup"><span data-stu-id="548b6-119">As long as all of its output voices have the same input sample rate, the audio graph will be valid.</span></span> <span data-ttu-id="548b6-120">如果聲音變更為輸出到具有不同輸入取樣率的新語音，則語音會轉換成新聲音的輸入取樣率。</span><span class="sxs-lookup"><span data-stu-id="548b6-120">If a voice is changed to output to new voices with a different input sample rate, the voice will convert to the input sample rate of the new voices.</span></span>

<span data-ttu-id="548b6-121">在某些情況下，必須新增 submix 聲音以執行語音之間的取樣率轉換。</span><span class="sxs-lookup"><span data-stu-id="548b6-121">There are some scenarios in which it is necessary to add a submix voice to perform sample rate conversion between voices.</span></span> <span data-ttu-id="548b6-122">如果聲音需要以各種輸入取樣率輸出至語音，則只有其中一個語音可以是原始語音的直接輸出。</span><span class="sxs-lookup"><span data-stu-id="548b6-122">If a voice needs to output to voices with various input sample rates, only one of the voices can be a direct output of the original voice.</span></span> <span data-ttu-id="548b6-123">因為所有聲音的輸出語音都必須具有相同的輸入取樣率，所以其他語音會間接接收輸出。</span><span class="sxs-lookup"><span data-stu-id="548b6-123">Because all of a voice's output voices must have the same input sample rate, the other voices receive output indirectly.</span></span> <span data-ttu-id="548b6-124">必須有一個 submix 的語音，並具有正確的輸入取樣率，以在原始語音和預期的輸出語音之間進行。</span><span class="sxs-lookup"><span data-stu-id="548b6-124">There must be a submix voice with the correct input sample rate that comes between the original voice and the intended output voice.</span></span>

<span data-ttu-id="548b6-125">例如，假設來源語音的輸入取樣率為 22 kHz，這需要輸出至輸入取樣率為 11 kHz 的 submix 語音，以及輸入取樣率為 44.1 kHz 的主控語音。</span><span class="sxs-lookup"><span data-stu-id="548b6-125">For example, consider a source voice with an input sample rate of 22 kHz, which needs to output to a submix voice with an input sample rate of 11 kHz and a mastering voice with an input sample rate of 44.1 kHz.</span></span> <span data-ttu-id="548b6-126">因為這兩個輸出語音的輸入取樣率不同，所以您必須在原始語音和其預期的輸出語音之間插入更 submix 的聲音。</span><span class="sxs-lookup"><span data-stu-id="548b6-126">Because the two output voices have different input sample rates, you need to insert more submix voices between the original voice and its intended output voices.</span></span> <span data-ttu-id="548b6-127">為了保持來源語音的精確度，並避免不必要的昂貴轉換成較高的取樣率，您需要在圖形中插入兩個 submix 的語音，並以 22 khz 的取樣輸入費率。</span><span class="sxs-lookup"><span data-stu-id="548b6-127">To maintain the fidelity of the source voice and avoid unnecessary expensive conversions to higher sample rates, you need to insert two submix voices with 22 khz sample input rates into the graph.</span></span> <span data-ttu-id="548b6-128">其中一個 submix 聲音會以 submix 聲音輸出至語音，並使用「回音」效果，而其他 submix 聲音則會輸出至 44.1 khz 的「控制」聲音。</span><span class="sxs-lookup"><span data-stu-id="548b6-128">One submix voice would output at 11 khz to the submix voice with the reverb effect, and the other submix voice would output to the mastering voice at 44.1 khz.</span></span>

## <a name="examples-of-sample-rate-conversion-in-audio-graphs"></a><span data-ttu-id="548b6-129">音訊圖形中的取樣率轉換範例</span><span class="sxs-lookup"><span data-stu-id="548b6-129">Examples of Sample Rate Conversion in Audio Graphs</span></span>

<span data-ttu-id="548b6-130">所有語音都有相同的取樣輸入率;在音訊圖形中未進行採樣速率轉換。</span><span class="sxs-lookup"><span data-stu-id="548b6-130">All voices have the same sample input rate; no sample rate conversion is done in the audio graph.</span></span>![在音訊圖形中未進行採樣速率轉換。](images/xaudio2-sample-rate-conversions-1.png)

<span data-ttu-id="548b6-132">所有語音都有相同的取樣輸入率，但不含「控制」聲音;取樣率轉換只會在資料進入「主控」聲音的資料上執行。</span><span class="sxs-lookup"><span data-stu-id="548b6-132">All voices have the same sample input rate except the mastering voice; sample rate conversion is only performed on data going to the mastering voice.</span></span> ![取樣率轉換只會在資料進入「主控」聲音的資料上執行。](images/xaudio2-sample-rate-conversions-2.png)

<span data-ttu-id="548b6-134">語音具有不同的取樣輸入率，而且需要更 submix 的語音來執行取樣率轉換;取樣速率轉換會在音訊圖形中的多個位置執行。</span><span class="sxs-lookup"><span data-stu-id="548b6-134">Voices have different sample input rates and require more submix voices to perform sample rate conversions; sample rate conversion is performed in multiple places in the audio graph.</span></span> ![取樣速率轉換會在音訊圖形中的多個位置執行。](images/xaudio2-sample-rate-conversions-3.png)

## <a name="related-topics"></a><span data-ttu-id="548b6-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="548b6-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="548b6-137">語音</span><span class="sxs-lookup"><span data-stu-id="548b6-137">Voices</span></span>](voices.md)
</dt> <dt>

[<span data-ttu-id="548b6-138">XAudio2 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="548b6-138">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 

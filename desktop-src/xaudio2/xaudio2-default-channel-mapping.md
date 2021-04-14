---
description: XAudio2 用戶端具有從語音通道到每個目的地語音通道的完全控制。
ms.assetid: 219d5b70-3f07-f973-f9ec-1cb3cf0be37e
title: XAudio2 預設通道對應
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06d77371223ccef02d6f0831a7aea182326f8477
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104469516"
---
# <a name="xaudio2-default-channel-mapping"></a><span data-ttu-id="edd9c-103">XAudio2 預設通道對應</span><span class="sxs-lookup"><span data-stu-id="edd9c-103">XAudio2 Default Channel Mapping</span></span>

<span data-ttu-id="edd9c-104">XAudio2 用戶端具有從語音通道到其每個目的地 voicesIt 的通道的完整控制權，可透過使用 [**IXAudio2Voice：： SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) 方法來控制對應。</span><span class="sxs-lookup"><span data-stu-id="edd9c-104">An XAudio2 client has full control of the mapping from the channels of a voice to the channels of each of its destination voicesIt controls the mapping through the use of the [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) method.</span></span> <span data-ttu-id="edd9c-105">不過，在某些情況下，XAudio2 會自動設定預設的傳送矩陣，以簡化這項工作。</span><span class="sxs-lookup"><span data-stu-id="edd9c-105">In some circumstances, however, XAudio2 simplifies this task by setting up a default send matrix automatically.</span></span> <span data-ttu-id="edd9c-106">它會使用與聲音音訊頻道相關聯的通道遮罩（如果有的話）來執行這項工作。</span><span class="sxs-lookup"><span data-stu-id="edd9c-106">It does this by using the channel mask, if any, associated with a voice's audio channels.</span></span> <span data-ttu-id="edd9c-107">通道遮罩是 \_ X3DAudio 和其他地方所定義的喇叭 xxx 位遮罩的組合。</span><span class="sxs-lookup"><span data-stu-id="edd9c-107">A channel mask is a combination of SPEAKER\_xxx bit masks as defined in X3DAudio.h and elsewhere.</span></span> <span data-ttu-id="edd9c-108">XAudio2 要求通道遮罩必須為0，或將相同數目的位設定為通道數目。</span><span class="sxs-lookup"><span data-stu-id="edd9c-108">XAudio2 requires channel masks to be 0 or have the same number of bits set as the number of channels.</span></span>

<span data-ttu-id="edd9c-109">下表顯示 XAudio2 所支援格式的通道遮罩需求和預設值。</span><span class="sxs-lookup"><span data-stu-id="edd9c-109">The following table shows the channel mask requirements and defaults for the formats supported by XAudio2.</span></span> 

| <span data-ttu-id="edd9c-110">格式</span><span class="sxs-lookup"><span data-stu-id="edd9c-110">Format</span></span> | <span data-ttu-id="edd9c-111">通道遮罩需求</span><span class="sxs-lookup"><span data-stu-id="edd9c-111">Channel Mask Requirement</span></span>             | <span data-ttu-id="edd9c-112">預設遮罩</span><span class="sxs-lookup"><span data-stu-id="edd9c-112">Default Mask</span></span>                        | <span data-ttu-id="edd9c-113">對應的結構成員</span><span class="sxs-lookup"><span data-stu-id="edd9c-113">Corresponding Structure Member</span></span>                            |
|--------|--------------------------------------|-------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="edd9c-114">PCM</span><span class="sxs-lookup"><span data-stu-id="edd9c-114">PCM</span></span>    | <span data-ttu-id="edd9c-115">檔案可能包含通道遮罩</span><span class="sxs-lookup"><span data-stu-id="edd9c-115">File might contain a channel mask</span></span>    | <span data-ttu-id="edd9c-116">通道遮罩為0或不存在</span><span class="sxs-lookup"><span data-stu-id="edd9c-116">Channel mask is 0, or absent</span></span>        | <span data-ttu-id="edd9c-117">WAVEFORMATEXTENSIBLE. dwChannelMask 或 none (WAVEFORMATEX) </span><span class="sxs-lookup"><span data-stu-id="edd9c-117">WAVEFORMATEXTENSIBLE.dwChannelMask or none (WAVEFORMATEX)</span></span> |
| <span data-ttu-id="edd9c-118">ADPCM</span><span class="sxs-lookup"><span data-stu-id="edd9c-118">ADPCM</span></span>  | <span data-ttu-id="edd9c-119">檔案不包含通道遮罩</span><span class="sxs-lookup"><span data-stu-id="edd9c-119">File does not contain a channel mask</span></span> | <span data-ttu-id="edd9c-120">一律使用預設通道遮罩</span><span class="sxs-lookup"><span data-stu-id="edd9c-120">Default Channel Mask is always used</span></span> | <span data-ttu-id="edd9c-121">無 (ADPCMWAVEFORMAT) </span><span class="sxs-lookup"><span data-stu-id="edd9c-121">None (ADPCMWAVEFORMAT)</span></span>                                    |



 

<span data-ttu-id="edd9c-122">針對 submix 和掌控語音，以及沒有通道遮罩或通道遮罩為0的來源語音，XAudio2 會根據下表來採用預設的喇叭位置。</span><span class="sxs-lookup"><span data-stu-id="edd9c-122">For submix and mastering voices, and for source voices without a channel mask or a channel mask of 0, XAudio2 assumes default speaker positions according to the following table.</span></span> 

| <span data-ttu-id="edd9c-123">通道</span><span class="sxs-lookup"><span data-stu-id="edd9c-123">Channels</span></span>  | <span data-ttu-id="edd9c-124">隱含通道位置</span><span class="sxs-lookup"><span data-stu-id="edd9c-124">Implicit Channel Positions</span></span>                                                                                            |
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edd9c-125">1</span><span class="sxs-lookup"><span data-stu-id="edd9c-125">1</span></span>         | <span data-ttu-id="edd9c-126">一律對應至 FrontLeft，並在兩個喇叭中以完整的 FrontRight， (mono 音效的特殊情況) </span><span class="sxs-lookup"><span data-stu-id="edd9c-126">Always maps to FrontLeft and FrontRight at full scale in both speakers (special case for mono sounds)</span></span>                 |
| <span data-ttu-id="edd9c-127">2</span><span class="sxs-lookup"><span data-stu-id="edd9c-127">2</span></span>         | <span data-ttu-id="edd9c-128">FrontLeft，FrontRight (基本身歷聲配置) </span><span class="sxs-lookup"><span data-stu-id="edd9c-128">FrontLeft, FrontRight (basic stereo configuration)</span></span>                                                                    |
| <span data-ttu-id="edd9c-129">3</span><span class="sxs-lookup"><span data-stu-id="edd9c-129">3</span></span>         | <span data-ttu-id="edd9c-130">FrontLeft、FrontRight、LowFrequency (2.1 configuration) </span><span class="sxs-lookup"><span data-stu-id="edd9c-130">FrontLeft, FrontRight, LowFrequency (2.1 configuration)</span></span>                                                               |
| <span data-ttu-id="edd9c-131">4</span><span class="sxs-lookup"><span data-stu-id="edd9c-131">4</span></span>         | <span data-ttu-id="edd9c-132">FrontLeft、FrontRight、BackLeft、BackRight (quadraphonic) </span><span class="sxs-lookup"><span data-stu-id="edd9c-132">FrontLeft, FrontRight, BackLeft, BackRight (quadraphonic)</span></span>                                                             |
| <span data-ttu-id="edd9c-133">5</span><span class="sxs-lookup"><span data-stu-id="edd9c-133">5</span></span>         | <span data-ttu-id="edd9c-134">FrontLeft、FrontRight、FrontCenter、SideLeft、SideRight (5.0 configuration) </span><span class="sxs-lookup"><span data-stu-id="edd9c-134">FrontLeft, FrontRight, FrontCenter, SideLeft, SideRight (5.0 configuration)</span></span>                                           |
| <span data-ttu-id="edd9c-135">6</span><span class="sxs-lookup"><span data-stu-id="edd9c-135">6</span></span>         | <span data-ttu-id="edd9c-136">FrontLeft、FrontRight、FrontCenter、LowFrequency、SideLeft、SideRight (5.1 configuration)  (請參閱下列備註) </span><span class="sxs-lookup"><span data-stu-id="edd9c-136">FrontLeft, FrontRight, FrontCenter, LowFrequency, SideLeft, SideRight (5.1 configuration) (see the following remarks)</span></span> |
| <span data-ttu-id="edd9c-137">7</span><span class="sxs-lookup"><span data-stu-id="edd9c-137">7</span></span>         | <span data-ttu-id="edd9c-138">FrontLeft、FrontRight、FrontCenter、LowFrequency、SideLeft、SideRight、BackCenter (6.1 configuration) </span><span class="sxs-lookup"><span data-stu-id="edd9c-138">FrontLeft, FrontRight, FrontCenter, LowFrequency, SideLeft, SideRight, BackCenter (6.1 configuration)</span></span>                 |
| <span data-ttu-id="edd9c-139">8</span><span class="sxs-lookup"><span data-stu-id="edd9c-139">8</span></span>         | <span data-ttu-id="edd9c-140">FrontLeft、FrontRight、FrontCenter、LowFrequency、BackLeft、BackRight、SideLeft、SideRight (7.1 configuration) </span><span class="sxs-lookup"><span data-stu-id="edd9c-140">FrontLeft, FrontRight, FrontCenter, LowFrequency, BackLeft, BackRight, SideLeft, SideRight (7.1 configuration)</span></span>        |
| <span data-ttu-id="edd9c-141">9個以上</span><span class="sxs-lookup"><span data-stu-id="edd9c-141">9 or more</span></span> | <span data-ttu-id="edd9c-142"> (一對一的對應沒有隱含的位置) </span><span class="sxs-lookup"><span data-stu-id="edd9c-142">No implicit positions (one-to-one mapping)</span></span>                                                                            |



 

<span data-ttu-id="edd9c-143">如果音訊圖形中指定的語音配對沒有與來源或目標語音相關聯的喇叭位置 (一個語音有八個以上的頻道) ，則在來源語音使用 [**IXAudio2Voice：： SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) 方法明確設定傳送矩陣之前，都不會播放語音。</span><span class="sxs-lookup"><span data-stu-id="edd9c-143">If a given voice pair in the audio graph has no speaker positions associated with either its source or target voice (one voice has more than eight channels), neither voice is playable until the source voice has a send matrix set explicitly using the [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) method.</span></span> <span data-ttu-id="edd9c-144">針對任一個聲音呼叫 [**IXAudio2SourceVoice：： Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) 方法將會失敗，直到您這樣做為止。</span><span class="sxs-lookup"><span data-stu-id="edd9c-144">Calling the [**IXAudio2SourceVoice::Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) method for either voice will fail until you do this.</span></span>

<span data-ttu-id="edd9c-145">如果來源語音和目標聲音具有不同的說話者位置數目，而 [**IXAudio2Voice：： SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) 尚未在來源語音上呼叫，則 XAudio2 會將每個來源頻道傳送到最接近的目標喇叭 (或說話者) 可供使用，按比例排列到預期的喇叭。</span><span class="sxs-lookup"><span data-stu-id="edd9c-145">If the source voice and target voice have different numbers of speaker positions and [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) has not been called on the source voice, XAudio2 sends each source channel to the nearest target speaker (or speakers) available, proportionally to how close they are to the intended speaker.</span></span> <span data-ttu-id="edd9c-146">有兩個特殊案例，預設行為是不同的。</span><span class="sxs-lookup"><span data-stu-id="edd9c-146">There are two special cases where the default behavior is different.</span></span>

1.  <span data-ttu-id="edd9c-147">如果來源音訊為 mono，且位於喇叭 \_ 前端 \_ 或沒有定義的位置，則一律會傳送給說話者 \_ \_ 的左側，而如果在 \_ \_ 輸出音訊中，則會直接傳送給講師前方。</span><span class="sxs-lookup"><span data-stu-id="edd9c-147">If the source audio is mono and is positioned at SPEAKER\_FRONT\_CENTER or has no defined position, it is always sent to SPEAKER\_FRONT\_LEFT and SPEAKER\_FRONT\_RIGHT if they exist in the output audio.</span></span> <span data-ttu-id="edd9c-148">如果不存在，則會回復為正常情況。</span><span class="sxs-lookup"><span data-stu-id="edd9c-148">If they do not exist, it falls back to the normal case.</span></span>
2.  <span data-ttu-id="edd9c-149">如果來源和目的地都是6通道，而且位於標準5.1 說話者的任何一項， (Left + Right + Center + Sub + BackL + BackR 或 Left + Right + Center + Sub + SideL + Client-sider-monitoring) ，則通道會透過一個對應到一個。</span><span class="sxs-lookup"><span data-stu-id="edd9c-149">If the source and destination are both 6-channel and are positioned at either of the standard 5.1 speaker setups (Left+Right+Center+Sub+BackL+BackR or Left+Right+Center+Sub+SideL+SideR), channels are mapped through one to one.</span></span> <span data-ttu-id="edd9c-150">換句話說，SideLeft/Right 和 BackLeft/Right 被視為同等的。</span><span class="sxs-lookup"><span data-stu-id="edd9c-150">In other words, SideLeft/Right and BackLeft/Right are treated equivalently.</span></span> <span data-ttu-id="edd9c-151">這是因為這項設置的歷程記錄有混淆。</span><span class="sxs-lookup"><span data-stu-id="edd9c-151">This is because there has been historical confusion around these setups.</span></span> <span data-ttu-id="edd9c-152">因此，假設的意圖一律會對應到一個。</span><span class="sxs-lookup"><span data-stu-id="edd9c-152">Therefore, the assumed intent is always to map one to one.</span></span>

## <a name="related-topics"></a><span data-ttu-id="edd9c-153">相關主題</span><span class="sxs-lookup"><span data-stu-id="edd9c-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edd9c-154">語音</span><span class="sxs-lookup"><span data-stu-id="edd9c-154">Voices</span></span>](voices.md)
</dt> <dt>

[<span data-ttu-id="edd9c-155">XAudio2 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="edd9c-155">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="edd9c-156">**GetChannelMask**</span><span class="sxs-lookup"><span data-stu-id="edd9c-156">**GetChannelMask**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask)
</dt> </dl>

 

 

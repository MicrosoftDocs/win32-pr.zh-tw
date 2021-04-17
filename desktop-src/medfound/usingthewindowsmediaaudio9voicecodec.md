---
description: 使用 Windows Media 音訊語音編解碼器
ms.assetid: 771acb04-33a4-4ea3-8f50-e5e3dbdf9495
title: 使用 Windows Media 音訊語音編解碼器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d636bd97b76e23acc6b68da87c8a206b17dea60a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104514305"
---
# <a name="using-the-windows-media-audio-voice-codec"></a><span data-ttu-id="aa115-103">使用 Windows Media 音訊語音編解碼器</span><span class="sxs-lookup"><span data-stu-id="aa115-103">Using the Windows Media Audio Voice Codec</span></span>

<span data-ttu-id="aa115-104">Windows Media 音訊語音編解碼器可針對包含語音的音訊提供較低的位元速率壓縮。</span><span class="sxs-lookup"><span data-stu-id="aa115-104">The Windows Media Audio Voice codec provides low bit-rate compression optimized for audio containing speech.</span></span> <span data-ttu-id="aa115-105">編解碼器產生這類小型範例的能力，是因為人類聲音的音效範圍有限。</span><span class="sxs-lookup"><span data-stu-id="aa115-105">The ability of the codec to produce such small samples is due to the limited frequency range of the sounds of the human voice.</span></span> <span data-ttu-id="aa115-106">這種優化表示專用的語音編碼器會針對包含更複雜聲音的內容（例如音樂）建立品質不良的輸出。</span><span class="sxs-lookup"><span data-stu-id="aa115-106">This optimization means that a dedicated voice encoder creates poor-quality output for content that contains more complicated sounds, like music.</span></span> <span data-ttu-id="aa115-107">不過，Windows Media 音訊語音編解碼器會針對語音、音樂和混合內容提供不同的模式，以彌補此潛在品質問題。</span><span class="sxs-lookup"><span data-stu-id="aa115-107">However, the Windows Media Audio Voice codec compensates for this potential quality issue by providing separate modes for voice, music, and mixed content.</span></span> <span data-ttu-id="aa115-108">編解碼器會分析混合的內容，以決定要針對檔案的每個部分使用哪一個模式。</span><span class="sxs-lookup"><span data-stu-id="aa115-108">The codec analyzes mixed content to determine which mode to use for each portion of the file.</span></span>

<span data-ttu-id="aa115-109">Windows Media 音訊語音編解碼器會在類別識別碼 CLSID CWMSPEncMediaObject2 所識別的編碼器物件中執行 \_ ，並在類別識別碼 clsid CWMSPDecMediaObject 所識別的解碼器物件中執行 \_ 。</span><span class="sxs-lookup"><span data-stu-id="aa115-109">The Windows Media Audio Voice codec is implemented in the encoder object identified by the class identifier CLSID\_CWMSPEncMediaObject2, and in the decoder object identified by the class identifier CLSID\_CWMSPDecMediaObject.</span></span> <span data-ttu-id="aa115-110">使用此編解碼器之媒體類型的格式標記為0x00A。</span><span class="sxs-lookup"><span data-stu-id="aa115-110">The format tag of media types using this codec is 0x00A.</span></span>

## <a name="configuring-the-encoder"></a><span data-ttu-id="aa115-111">設定編碼器</span><span class="sxs-lookup"><span data-stu-id="aa115-111">Configuring the Encoder</span></span>

<span data-ttu-id="aa115-112">語音編碼器支援三種模式：語音、音樂和混合。</span><span class="sxs-lookup"><span data-stu-id="aa115-112">The voice encoder supports three modes: speech, music, and mixed.</span></span> <span data-ttu-id="aa115-113">每個模式都經過優化，以取得該內容類型的最佳結果。</span><span class="sxs-lookup"><span data-stu-id="aa115-113">Each mode is optimized to get the best results for that type of content.</span></span> <span data-ttu-id="aa115-114">您可以使用 **IPropertyStore** 的方法設定 [MFPKEY \_ WMAVOICE \_ ENC \_ MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) 屬性，設定語音編碼器的模式。</span><span class="sxs-lookup"><span data-stu-id="aa115-114">You can configure the mode of the voice encoder by using the methods of **IPropertyStore** to set the [MFPKEY\_WMAVOICE\_ENC\_MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) property.</span></span>

<span data-ttu-id="aa115-115">針對混合內容設定時，Windows Media 音訊的語音編解碼器會自動偵測內容中的音樂段落。</span><span class="sxs-lookup"><span data-stu-id="aa115-115">When configured for mixed content, the Windows Media Audio Voice codec will automatically detect passages of music in the content.</span></span> <span data-ttu-id="aa115-116">如果您對結果不滿意，您可以使用編輯決策清單 (EDL) ，在內容中指定音樂的位置。</span><span class="sxs-lookup"><span data-stu-id="aa115-116">If you are not satisfied with the results, you can specify the location of music in the content using an editing decision list (EDL).</span></span> <span data-ttu-id="aa115-117">如需詳細資訊，請參閱 [使用編碼語音的編輯決策清單](usingavoiceeditingdecisionlist.md)。</span><span class="sxs-lookup"><span data-stu-id="aa115-117">For more information, see [Using an Editing Decision List for Encoding Voice](usingavoiceeditingdecisionlist.md).</span></span>

<span data-ttu-id="aa115-118">不同于其他音訊編碼器，您可以使用 [MFPKEY \_ WMAVOICE \_ ENC \_ BufferWindow](mfpkey-wmavoice-enc-bufferwindowproperty.md) 屬性來設定語音內容的緩衝區視窗值。</span><span class="sxs-lookup"><span data-stu-id="aa115-118">Unlike the other audio encoders, you can set the buffer window value for voice content by using the [MFPKEY\_WMAVOICE\_ENC\_BufferWindow](mfpkey-wmavoice-enc-bufferwindowproperty.md) property.</span></span> <span data-ttu-id="aa115-119">不過，在大部分情況下，預設值應該會正常運作。</span><span class="sxs-lookup"><span data-stu-id="aa115-119">However, the default values should work fine in most cases.</span></span>

> [!Note]  
>    <span data-ttu-id="aa115-120">設定語音編碼器時，請務必先設定輸出類型，然後再設定輸入類型。</span><span class="sxs-lookup"><span data-stu-id="aa115-120">When configuring the voice encoder, it is very important that you set the output type before you set the input type.</span></span> <span data-ttu-id="aa115-121">這是建議的所有音訊編解碼器作業順序，但如果在您呼叫 **IMediaObject：： GetOutputType** 或 **IMFTransform：： GetOutputType** 時設定輸入，則語音編碼器可以報告錯誤的輸出類型。</span><span class="sxs-lookup"><span data-stu-id="aa115-121">This is the recommended order of operations for all of the audio codecs, but the voice encoder can report erroneous output types if an input is set when you call **IMediaObject::GetOutputType** or **IMFTransform::GetOutputType**.</span></span>

 

## <a name="decoding"></a><span data-ttu-id="aa115-122">解碼</span><span class="sxs-lookup"><span data-stu-id="aa115-122">Decoding</span></span>

<span data-ttu-id="aa115-123">解碼語音音訊沒有特殊需求。</span><span class="sxs-lookup"><span data-stu-id="aa115-123">There are no special requirements for decoding voice audio.</span></span> <span data-ttu-id="aa115-124">如需詳細資訊，請參閱設定 [音訊解碼](configuringaudiodecoding.md)。</span><span class="sxs-lookup"><span data-stu-id="aa115-124">Form more information, see [Configuring Audio Decoding](configuringaudiodecoding.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa115-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="aa115-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa115-126">使用音訊</span><span class="sxs-lookup"><span data-stu-id="aa115-126">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 




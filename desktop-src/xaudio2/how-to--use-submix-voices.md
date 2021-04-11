---
description: 本主題說明如何設定語音群組，以將其輸出傳送至相同的 submix 語音。 這可讓 submix 語音的單一變更影響整個語音群組。
ms.assetid: 76c1c138-4846-9c4f-7875-446867436ee9
title: 使用方法：使用次混音聲音
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7152c3224d6528ac52651f2ca2f433631b347c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193534"
---
# <a name="how-to-use-submix-voices"></a><span data-ttu-id="ceefe-104">使用方法：使用次混音聲音</span><span class="sxs-lookup"><span data-stu-id="ceefe-104">How to: Use Submix Voices</span></span>

<span data-ttu-id="ceefe-105">本主題說明如何設定語音群組，以將其輸出傳送至相同的 submix 語音。</span><span class="sxs-lookup"><span data-stu-id="ceefe-105">This topic shows you how you can set groups of voices to send their output to the same submix voice.</span></span> <span data-ttu-id="ceefe-106">這可讓 submix 語音的單一變更影響整個語音群組。</span><span class="sxs-lookup"><span data-stu-id="ceefe-106">This enables a single change to a submix voice to affect a whole group of voices.</span></span>

1.  <span data-ttu-id="ceefe-107">建立 [**submix 聲音**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) ，讓所有遊戲的音效效果都能傳送。</span><span class="sxs-lookup"><span data-stu-id="ceefe-107">Create a [**submix voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) to which all of the game's sound effect voices will send.</span></span>
    ```
    IXAudio2SubmixVoice * pSFXSubmixVoice;
    pXAudio2->CreateSubmixVoice(&pSFXSubmixVoice,1,44100,0,0,0,0);
    ```

    

2.  <span data-ttu-id="ceefe-108">建立 [**XAUDIO2 \_ voice \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) 傳送結構，其中包含 submix 聲音的參考。</span><span class="sxs-lookup"><span data-stu-id="ceefe-108">Create an [**XAUDIO2\_VOICE\_SENDS**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) structure that contains a reference to the submix voice.</span></span>
    ```
    XAUDIO2_SEND_DESCRIPTOR SFXSend = {0, pSFXSubmixVoice};
    XAUDIO2_VOICE_SENDS SFXSendList = {1, &SFXSend};
    ```

    

3.  <span data-ttu-id="ceefe-109">將 [**XAUDIO2 \_ VOICE \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) 傳送結構傳遞給新的來源語音。</span><span class="sxs-lookup"><span data-stu-id="ceefe-109">Pass the [**XAUDIO2\_VOICE\_SENDS**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) structure to new source voices as they are created.</span></span>
    ```
    IXAudio2SourceVoice* pSFXSourceVoice;
    if( FAILED(hr = pXaudio2->CreateSourceVoice( &pSFXSourceVoice, (WAVEFORMATEX*)&wfx,
        0, XAUDIO2_DEFAULT_FREQ_RATIO, pCallback, pSFXSendList, NULL ) ) )
        return hr;
    ```

    

4.  <span data-ttu-id="ceefe-110">藉由調整 submix 聲音，將變更套用至所有音效效果的聲音。</span><span class="sxs-lookup"><span data-stu-id="ceefe-110">Apply changes to all sound effect voices by adjusting the submix voice.</span></span>

    <span data-ttu-id="ceefe-111">在此範例中，使用 [**SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) 函式來變更 submix 聲音的音量，實際上會變更輸出的所有語音音量。</span><span class="sxs-lookup"><span data-stu-id="ceefe-111">In this example, changing the volume of the submix voice with the [**SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) function effectively changes the volume of all voices that output to it.</span></span>

    ```
    pSFXSubmixVoice->SetVolume(0.1);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="ceefe-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="ceefe-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ceefe-113">語音</span><span class="sxs-lookup"><span data-stu-id="ceefe-113">Voices</span></span>](voices.md)
</dt> <dt>

[<span data-ttu-id="ceefe-114">XAudio2 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="ceefe-114">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="ceefe-115">使用方法：建立基本音訊處理圖形</span><span class="sxs-lookup"><span data-stu-id="ceefe-115">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> </dl>

 

 

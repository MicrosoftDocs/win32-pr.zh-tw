---
description: 本主題說明如何在整體層級、每個輸出頻道，或在聲音的每個通道與 sendlist 中的另一個聲音之間變更聲音的音量。
ms.assetid: 40004128-4abb-4bcd-fe76-91276be8abec
title: 如何：變更聲音音量
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a307c5585e56fb6dc4dbdc40386c6844607498ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693771"
---
# <a name="how-to-change-voice-volume"></a><span data-ttu-id="5e927-103">如何：變更聲音音量</span><span class="sxs-lookup"><span data-stu-id="5e927-103">How to: Change Voice Volume</span></span>

<span data-ttu-id="5e927-104">本主題說明如何在整體層級、每個輸出頻道，或在聲音的每個通道與 [**sendlist**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends)中的另一個聲音之間變更聲音的音量。</span><span class="sxs-lookup"><span data-stu-id="5e927-104">This topic shows you how you can change the volume of a voice at an overall level, at each output channel, or between each channel of a voice and another voice in its [**sendlist**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends).</span></span>

## <a name="to-set-an-overall-volume-level-for-the-voices-input"></a><span data-ttu-id="5e927-105">設定語音輸入的整體音量層級</span><span class="sxs-lookup"><span data-stu-id="5e927-105">To set an overall volume level for the voice's input</span></span>

-   <span data-ttu-id="5e927-106">使用 [**SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) 函數。</span><span class="sxs-lookup"><span data-stu-id="5e927-106">Use the [**SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) function.</span></span>

    ```
    pSourceVoice->SetVolume(1.0);
    ```

    

## <a name="to-set-the-volume-of-the-voices-output-channels"></a><span data-ttu-id="5e927-107">設定語音輸出通道的音量</span><span class="sxs-lookup"><span data-stu-id="5e927-107">To set the volume of the voice's output channels</span></span>

1.  <span data-ttu-id="5e927-108">建立浮點數的陣列，其中包含語音中所有輸出通道所需的磁片區。</span><span class="sxs-lookup"><span data-stu-id="5e927-108">Create an array of floating point numbers that contain the desired volumes of all the output channels in the voice.</span></span>

    <span data-ttu-id="5e927-109">陣列中的每個通道都會有一個專案。</span><span class="sxs-lookup"><span data-stu-id="5e927-109">The array will have one entry for each channel in the voice.</span></span>

    ```
    float SourceVoiceChannelVolumes[1] = {1.0};
    ```

    

2.  <span data-ttu-id="5e927-110">您可以使用 [**SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes) 函數來設定輸出通道的音量。</span><span class="sxs-lookup"><span data-stu-id="5e927-110">Use the [**SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes) function to set the volume of the output channels.</span></span>

    ```
    hr = pSourceVoice->SetChannelVolumes(1,SourceVoiceChannelVolumes);
    ```

    

## <a name="to-set-the-volume-of-connections"></a><span data-ttu-id="5e927-111">設定連接的數量</span><span class="sxs-lookup"><span data-stu-id="5e927-111">To set the volume of connections</span></span>

<span data-ttu-id="5e927-112">在語音和語音之間的 [**sendlist**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends)中設定連接量。</span><span class="sxs-lookup"><span data-stu-id="5e927-112">Set the connection volume between the voice and a voice in its [**sendlist**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends).</span></span>

1.  <span data-ttu-id="5e927-113">建立浮點數的陣列，以定義輸出矩陣（如果語音傳送至另一個聲音）。</span><span class="sxs-lookup"><span data-stu-id="5e927-113">Create an array of floating point numbers that defines an output matrix if the voice sends to another voice.</span></span>

    > [!Note]  
    > <span data-ttu-id="5e927-114">陣列的專案數目必須等於來源語音通道×目的地語音訊道。</span><span class="sxs-lookup"><span data-stu-id="5e927-114">The array must have a number of entries equal to source voice channels × destination voice channels.</span></span> <span data-ttu-id="5e927-115">在此範例中，對應是從具有一個通道的語音，到具有兩個通道的聲音。</span><span class="sxs-lookup"><span data-stu-id="5e927-115">In this example, the mapping is from a voice with one channel to a voice with two channels.</span></span>

     

    ```
    float outputMatrix[2] = {1.0f,0.05f};
    ```

    

2.  <span data-ttu-id="5e927-116">您可以使用 [**SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) 函數來設定輸出矩陣。</span><span class="sxs-lookup"><span data-stu-id="5e927-116">Use the [**SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) function to set the output matrix.</span></span>

    ```
    pSourceVoice->SetOutputMatrix(pSubmixVoice,1,2,outputMatrix);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="5e927-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="5e927-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e927-118">XAudio2 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="5e927-118">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="5e927-119">使用方法：建立基本音訊處理圖形</span><span class="sxs-lookup"><span data-stu-id="5e927-119">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="5e927-120">XAudio2 音量和音調控制</span><span class="sxs-lookup"><span data-stu-id="5e927-120">XAudio2 Volume and Pitch Control</span></span>](volume-and-pitch-control.md)
</dt> </dl>

 

 

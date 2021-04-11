---
description: 本主題說明如何整合 X3DAudio 與 XAudio2。
ms.assetid: a8f41f0d-b284-aefa-923b-471b13b4a3ec
title: 使用方法：整合 X3DAudio 與 XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dc54fa5f673e319712808ca6d2b587b8ad2d0fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693768"
---
# <a name="how-to-integrate-x3daudio-with-xaudio2"></a><span data-ttu-id="05fdd-103">使用方法：整合 X3DAudio 與 XAudio2</span><span class="sxs-lookup"><span data-stu-id="05fdd-103">How to: Integrate X3DAudio with XAudio2</span></span>

<span data-ttu-id="05fdd-104">本主題說明如何整合 X3DAudio 與 XAudio2。</span><span class="sxs-lookup"><span data-stu-id="05fdd-104">This topic shows how to integrate X3DAudio with XAudio2.</span></span> <span data-ttu-id="05fdd-105">您可以使用 X3DAudio 來提供 XAudio2 聲音的音量和音調值，以及 XAudio2 內建的回音效果參數。</span><span class="sxs-lookup"><span data-stu-id="05fdd-105">You can use X3DAudio to provide the volume and pitch values for XAudio2 voices and the parameters for the XAudio2 built in reverb effect.</span></span> <span data-ttu-id="05fdd-106">本主題假設您已依照 [如何：建立基本音訊處理圖形](how-to--build-a-basic-audio-processing-graph.md)中所述的方式建立音訊圖表。</span><span class="sxs-lookup"><span data-stu-id="05fdd-106">This topic assumes that you have created an audio graph as described in [How to: Build a Basic Audio Processing Graph](how-to--build-a-basic-audio-processing-graph.md).</span></span> <span data-ttu-id="05fdd-107">如果您尚未建立音訊圖形， [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="05fdd-107">If you have not already created an audio graph, [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) will fail.</span></span>

<span data-ttu-id="05fdd-108">**若要初始化 X3DAudio**</span><span class="sxs-lookup"><span data-stu-id="05fdd-108">**To initialize X3DAudio**</span></span>

1.  <span data-ttu-id="05fdd-109">藉由呼叫 [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize)來初始化 X3DAudio。</span><span class="sxs-lookup"><span data-stu-id="05fdd-109">Initialize X3DAudio by calling [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize).</span></span>

    <span data-ttu-id="05fdd-110">[**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize)函式會接受旗標，指出喇叭設定、使用者定義的世界單位中的音效速度，以及傳回 X3DAudio 引擎實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="05fdd-110">The [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) function takes flags indicating the speaker setup, the speed of sound in user-defined world units per second, and a handle to return an instance of the X3DAudio engine.</span></span> <span data-ttu-id="05fdd-111">呼叫 [**IXAudio2MasteringVoice：： GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask) 以取得輸出格式的通道遮罩。</span><span class="sxs-lookup"><span data-stu-id="05fdd-111">Call [**IXAudio2MasteringVoice::GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask) to get the output format's channel mask.</span></span>

    ```
    DWORD dwChannelMask;       
    pMasteringVoice->GetChannelMask( &dwChannelMask );       

    X3DAUDIO_HANDLE X3DInstance;
    X3DAudioInitialize( dwChannelMask, X3DAUDIO_SPEED_OF_SOUND, X3DInstance );
    ```

    

2.  <span data-ttu-id="05fdd-112">建立 [**X3DAUDIO \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) 接聽程式和 [**X3DAUDIO \_ 發射器**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) 結構的實例。</span><span class="sxs-lookup"><span data-stu-id="05fdd-112">Create instances of the [**X3DAUDIO\_LISTENER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) and [**X3DAUDIO\_EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) structures.</span></span>

    <span data-ttu-id="05fdd-113">[**X3DAUDIO 接聽 \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener)程式結構代表聽聽音效的位置。</span><span class="sxs-lookup"><span data-stu-id="05fdd-113">The [**X3DAUDIO\_LISTENER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) structure represents the position of whatever is hearing the sound.</span></span> <span data-ttu-id="05fdd-114">一般來說，這是相機的位置或接近的位置。</span><span class="sxs-lookup"><span data-stu-id="05fdd-114">Generally, this is the position of the camera or a position close to it.</span></span> <span data-ttu-id="05fdd-115">[**X3DAUDIO \_ 發射器**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter)結構代表製作音效的位置。</span><span class="sxs-lookup"><span data-stu-id="05fdd-115">The [**X3DAUDIO\_EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) structure represents the position of the thing making the sound.</span></span> <span data-ttu-id="05fdd-116">每個要追蹤的音效都會有一個 **X3DAUDIO 的 \_ 發射器** 結構。</span><span class="sxs-lookup"><span data-stu-id="05fdd-116">There will be one **X3DAUDIO\_EMITTER** structure for each sound that is being tracked.</span></span>

    <span data-ttu-id="05fdd-117">將不會在遊戲迴圈中更新之結構的成員應在此初始化。</span><span class="sxs-lookup"><span data-stu-id="05fdd-117">Members of the structures that will not be updated in a game loop should be initialized here.</span></span> <span data-ttu-id="05fdd-118">結構的大部分成員都可以直接初始化為零。</span><span class="sxs-lookup"><span data-stu-id="05fdd-118">Most members of the structures can simply be initialized to zero.</span></span> <span data-ttu-id="05fdd-119">不過， [**X3DAUDIO \_ 發射器**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) 的某些成員必須設定為初始化為非零值。</span><span class="sxs-lookup"><span data-stu-id="05fdd-119">However, some members of [**X3DAUDIO\_EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) need to be set to be initialized to non-zero values.</span></span> <span data-ttu-id="05fdd-120">**X3DAUDIO \_ 發射器** 的 ChannelCount 成員必須初始化為發射器所代表之聲音中的通道數目。</span><span class="sxs-lookup"><span data-stu-id="05fdd-120">The ChannelCount member of the **X3DAUDIO\_EMITTER** needs to be initialized to the number of channels in the voice the emitter represents.</span></span> <span data-ttu-id="05fdd-121">此外， **X3DAUDIO \_ 發射器** 的 CurveDistanceScaler 成員必須在 FLT \_ MIN 到 FLT MAX 的範圍內 \_ 。</span><span class="sxs-lookup"><span data-stu-id="05fdd-121">Also, the CurveDistanceScaler member of **X3DAUDIO\_EMITTER** must be in the range FLT\_MIN to FLT\_MAX.</span></span>

    ```
    X3DAUDIO_LISTENER Listener = {0};
    X3DAUDIO_EMITTER Emitter = {0};
    Emitter.ChannelCount = 1;
    Emitter.CurveDistanceScaler = FLT_MIN;
    ```

    

3.  <span data-ttu-id="05fdd-122">建立 [**X3DAUDIO \_ DSP \_ 設定**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) 結構的實例。</span><span class="sxs-lookup"><span data-stu-id="05fdd-122">Create an instance of the [**X3DAUDIO\_DSP\_SETTINGS**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) structure.</span></span>

    <span data-ttu-id="05fdd-123">[**X3DAUDIO 的 \_ DSP \_ 設定**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings)結構是用來傳回 [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate)所計算的結果。</span><span class="sxs-lookup"><span data-stu-id="05fdd-123">The [**X3DAUDIO\_DSP\_SETTINGS**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) structure is used to return results calculated by [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate).</span></span> <span data-ttu-id="05fdd-124">**X3DAudioCalculate** 函式不會為其任何參數配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="05fdd-124">The **X3DAudioCalculate** function does not allocate memory for any of its parameters.</span></span> <span data-ttu-id="05fdd-125">這表示，如果您想要使用 **X3DAUDIO \_ DSP \_ 設定** 結構的 pMatrixCoefficients 和 pDelayTimes 成員，您必須為這些成員配置陣列。</span><span class="sxs-lookup"><span data-stu-id="05fdd-125">This means that you need to allocate arrays for the **X3DAUDIO\_DSP\_SETTINGS** structure's pMatrixCoefficients and pDelayTimes members if you intend to use them.</span></span> <span data-ttu-id="05fdd-126">此外，您還需要將 SrcChannelCount 和 DstChannelCount 成員設定為發射器的來源和目的地語音中的通道數目。</span><span class="sxs-lookup"><span data-stu-id="05fdd-126">In addition, you need to set the SrcChannelCount and DstChannelCount members to the number of channels in the emitter's source and destination voices.</span></span>

    ```
    X3DAUDIO_DSP_SETTINGS DSPSettings = {0};
    FLOAT32 * matrix = new FLOAT32[deviceDetails.OutputFormat.Format.nChannels];
    DSPSettings.SrcChannelCount = 1;
    DSPSettings.DstChannelCount = deviceDetails.OutputFormat.Format.nChannels;
    DSPSettings.pMatrixCoefficients = matrix;
    ```

    

    > [!Note]  
    > <span data-ttu-id="05fdd-127">在「控制」聲音上使用 [**IXAudio2Voice：： GetVoiceDetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails) ，以取得 **nChannels** 的 InputChannels 數目。</span><span class="sxs-lookup"><span data-stu-id="05fdd-127">Use [**IXAudio2Voice::GetVoiceDetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails) on the mastering voice to obtain the number of InputChannels for **nChannels**.</span></span> <span data-ttu-id="05fdd-128">針對 XAUDIO2 Windows 8 之前的 DirectX SDK 版本，請使用 IXAudio2：： GetDeviceDetails。</span><span class="sxs-lookup"><span data-stu-id="05fdd-128">For DirectX SDK versions of XAUDIO2 prior to Windows 8, use IXAudio2::GetDeviceDetails.</span></span>

     

<span data-ttu-id="05fdd-129">每兩到三個框架執行這些步驟一次，以計算新的設定並加以套用。</span><span class="sxs-lookup"><span data-stu-id="05fdd-129">Perform these steps once every two to three frames to calculate new settings and apply them.</span></span> <span data-ttu-id="05fdd-130">在此範例中，來源語音會直接傳送至「控制」語音，並傳送至 submix 的語音，並套用「回音」效果。</span><span class="sxs-lookup"><span data-stu-id="05fdd-130">In this example, a source voice is sending directly to the mastering voice and to a submix voice with a reverb effect applied to it.</span></span>

<span data-ttu-id="05fdd-131">**使用 X3DAudio 來計算及套用新的3D 音訊設定**</span><span class="sxs-lookup"><span data-stu-id="05fdd-131">**To use X3DAudio to calculate and apply new 3D audio settings**</span></span>

1.  <span data-ttu-id="05fdd-132">以目前的位置、速度和方向，更新 [**X3DAUDIO \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) 接聽程式和 [**X3DAUDIO \_ 發射器**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) 結構。</span><span class="sxs-lookup"><span data-stu-id="05fdd-132">Update the [**X3DAUDIO\_LISTENER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) and [**X3DAUDIO\_EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) structures with their current position, velocity, and orientation.</span></span>

    ```
    Emitter.OrientFront = EmitterOrientFront;
    Emitter.OrientTop = EmitterOrientTop;
    Emitter.Position = EmitterPosition;
    Emitter.Velocity = EmitterVelocity;
    Listener.OrientFront = ListenerOrientFront;
    Listener.OrientTop = ListenerOrientTop;
    Listener.Position = ListenerPosition;
    Listener.Velocity = ListenerVelocity;
    ```

    

2.  <span data-ttu-id="05fdd-133">呼叫 [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) 來計算語音的新設定。</span><span class="sxs-lookup"><span data-stu-id="05fdd-133">Call [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) to calculate new settings for the voices.</span></span>

    <span data-ttu-id="05fdd-134">[**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate)的參數將會是已更新的 X3DAUDIO 接聽程式和 [**X3DAUDIO 的 \_ 發射器**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter)結構。 [**\_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener)</span><span class="sxs-lookup"><span data-stu-id="05fdd-134">The parameters for [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) will be the updated [**X3DAUDIO\_LISTENER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) and [**X3DAUDIO\_EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) structures.</span></span> <span data-ttu-id="05fdd-135">旗標會指出 **X3DAudioCalculate** 應該計算的值，以及哪個 [**X3DAUDIO 的 \_ DSP \_ 設定**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) 結構會保存所執行計算的結果。</span><span class="sxs-lookup"><span data-stu-id="05fdd-135">The flags will indicate what values **X3DAudioCalculate** should calculate, and which [**X3DAUDIO\_DSP\_SETTINGS**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) structure will hold the results of the calculations performed.</span></span>

    ```
    X3DAudioCalculate(X3DInstance, &Listener, &Emitter,
        X3DAUDIO_CALCULATE_MATRIX | X3DAUDIO_CALCULATE_DOPPLER | X3DAUDIO_CALCULATE_LPF_DIRECT | X3DAUDIO_CALCULATE_REVERB,
        &DSPSettings );
    ```

    

3.  <span data-ttu-id="05fdd-136">使用 [**IXAudio2Voice：： SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) 和 [**IXAudio2SourceVoice：： SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) 將磁片區和音調值套用至來源聲音。</span><span class="sxs-lookup"><span data-stu-id="05fdd-136">Use [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) and [**IXAudio2SourceVoice::SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) to apply the volume and pitch values to the source voice.</span></span>

    ```
    pSFXSourceVoice->SetOutputMatrix( pMasterVoice, 1, deviceDetails.OutputFormat.Format.nChannels, DSPSettings.pMatrixCoefficients ) ;
    pSFXSourceVoice->SetFrequencyRatio(DSPSettings.DopplerFactor);
    ```

    

4.  <span data-ttu-id="05fdd-137">您可以使用 [**IXAudio2Voice：： SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) 將計算的回音等級套用至 submix 語音。</span><span class="sxs-lookup"><span data-stu-id="05fdd-137">Use [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) to apply the calculated reverb level to the submix voice.</span></span>

    ```
    pSFXSourceVoice->SetOutputMatrix(pSubmixVoice, 1, 1, &DSPSettings.ReverbLevel);
    ```

    

5.  <span data-ttu-id="05fdd-138">使用 [**IXAudio2Voice：： SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters) 將計算出的低通過篩選準則直接係數套用至來源聲音。</span><span class="sxs-lookup"><span data-stu-id="05fdd-138">Use [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters) to apply the calculated low pass filter direct coefficient to the source voice.</span></span>

    ```
    XAUDIO2_FILTER_PARAMETERS FilterParameters = { LowPassFilter, 2.0f * sinf(X3DAUDIO_PI/6.0f * DSPSettings.LPFDirectCoefficient), 1.0f };
    pSFXSourceVoice->SetFilterParameters(&FilterParameters);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="05fdd-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="05fdd-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05fdd-140">X3DAudio</span><span class="sxs-lookup"><span data-stu-id="05fdd-140">X3DAudio</span></span>](x3daudio.md)
</dt> <dt>

[<span data-ttu-id="05fdd-141">X3DAudio 總覽</span><span class="sxs-lookup"><span data-stu-id="05fdd-141">X3DAudio Overview</span></span>](x3daudio-overview.md)
</dt> <dt>

[<span data-ttu-id="05fdd-142">XAudio2 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="05fdd-142">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="05fdd-143">XAudio2 音量和音調控制</span><span class="sxs-lookup"><span data-stu-id="05fdd-143">XAudio2 Volume and Pitch Control</span></span>](volume-and-pitch-control.md)
</dt> </dl>

 

 
